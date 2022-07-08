---
title: イタリア向け会計プリンター統合サンプル
description: この記事では、Microsoft Dynamics 365 Commerce のイタリア向け会計統合サンプルの概要について説明します。
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2018-11-1
ms.openlocfilehash: 2aa1851fe5fe447ba2dd4640be9881b37e54216e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909393"
---
# <a name="fiscal-printer-integration-sample-for-italy"></a>イタリア向け会計プリンター統合サンプル

[!include[banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce のイタリア向け会計統合サンプルの概要について説明します。

イタリア向け Commerce 機能は、販売時点管理 (POS) と会計プリンターのサンプル統合を含みます。 サンプルは [会計統合機能](fiscal-integration-for-retail-channel.md) を拡張して Epson 製の [Epson FP-90III シリーズ](https://www.epson.it/products/sd/pos-printer/epson-fp-90iii-series) プリンターを利用できるようにし、Fiscal ePOS-Print API を使用した EpsonFPMate Web サービスを介した Web サーバー モードで会計プリンターとの通信を実現します。 サンプルは Registratore Telematico (RT) モードのみをサポートします。 このサンプルはソース コード形式で提供され、Retail ソフトウェア開発キット (SDK) に含まれます。

マイクロソフトは、Epson によるハードウェア、ソフトウェア、ドキュメントをリリースしません。 会計プリンターの入手方法や操作方法については [Epson Italia S.p.A](https://www.epson.it) にお問い合わせください。

## <a name="scenarios"></a>シナリオ

イタリア向けの会計プリンター統合サンプルでは、以下のシナリオをカバーしています:

- 販売シナリオ:

    - 現金払いで持ち帰りの販売と返品の会計レシートを印刷します。
    - 会計プリンターからの応答をキャプチャして、チャネル データベースに格納します。
    - 税金:

        - 会計プリンターの税コード (部門) にマッピングします。
        - マッピングされた税データを会計プリンタに転送します。
        - 会計領収書に税を印刷します。

    - 支払:

        - 会計プリンターの支払い方法に対応したマッピング。
        - 会計のレシートに支払を印刷します。
        - 変更情報を印刷します。

    - 明細の割引を印刷します。
    - ギフト カード:

        - 販売の会計レシートから、発行/再チャージされたギフトカードの明細行を除外します。
        - ギフト カードを通常の支払い方法として使用する支払いを印刷します。

    - 顧客の注文操作に伴う会計の領収書の印刷:

        - 顧客注文の入金で、会計のレシートが印刷されません。
        - ハイブリッド顧客注文のキャリーアウト明細行の会計領収書を印刷します。
        - 顧客の注文に対する集荷作業の会計レシートを印刷します。
        - 返品注文の会計レシートを印刷します。

    - 領収書に領収書番号を表すバーコードを印刷します。
    - 販売トランザクションで指定された[顧客情報](emea-ita-customer-information.md)を会計領収書に印刷します。 この情報の一例は、顧客の抽選コードです。 

- 終了日に関する明細書 (会計年度 X レポートと会計年度 Z レポート)。
- 次のオプションなど、エラー処理。

    - 会計プリンターが接続されていない、準備ができていない、応答がない、プリンターの紙切れ、紙詰まりなど、再試行が可能な場合は、会計登録を再試行します。
    - 会計登録の延期。
    - 会計登録をスキップするか、またはトランザクションを登録済みとしてマークして、失敗した理由と追加情報を取得するための情報コードを含めます。
    - 新しい販売トランザクションの開始時や販売トランザクション確定時に、会計用プリンターの使用可能性を確認します。

### <a name="gift-cards"></a>ギフト カード

会計プリンターの統合サンプルでは、ギフト カードに関連する以下のルールを実装しています:

- *ギフトカードの発行* と *ギフトカード* への追加の操作に関連する販売明細行を会計の領収書から除外します。
- ギフト カードの明細行だけで構成される場合、会計領収書を印刷しません。
- ギフトカードを発行したり、再チャージしたりした場合、その合計金額を会計上の領収書の支払い明細行から差し引きます。
- 対応する会計トランザクションを参照して、支払明細行の計算した調整をチャネル データベースに保存します。
- ギフト カードによる支払を通常の支払と見なします。

### <a name="customer-deposits-and-customer-order-deposits"></a>顧客前金と顧客手付金

会計プリンターの統合サンプルでは、顧客預金と顧客注文預金に関連した以下のルールを実装しています:

- トランザクションが顧客の預金である場合、会計上の領収書を印刷しません。
- トランザクションに顧客注文の預金や顧客注文の預金の払い戻しのみが含まれている場合は、会計レシートを印刷しません。
- 顧客の注文を集荷するオペレーションの会計レシートに、先に支払った預金の金額を印刷します。
- ハイブリッド顧客注文の作成時に、支払明細行から顧客手付金を差し引きます。
- ハイブリッド顧客注文の会計トランザクションを参照して、支払明細行の計算した調整をチャネル データベースに保存します。

### <a name="limitations-of-the-sample"></a>サンプルの制限事項

- 会計プリンタは、消費税が価格に含まれているシナリオのみに対応しています。 したがって、**税込価格** オプションは、店舗と顧客の両方で **はい** に設定する必要があります。
- 日次レポート (X 年度、Z 年度) は、会計プリンターのファームウェアに埋め込まれた形式を使用して印刷します。
- 会計プリンタでは、混合トランザクションをサポートしていません。 POS 機能のプロファイルでは、**1 枚のレシートに販売と返品の混在禁止** オプションを **はい** に設定する必要があります。
- サンプルは Registratore Telematico (RT) モードで動作する会計プリンターとの統合のみに対応します。

## <a name="set-up-fiscal-integration-for-italy"></a>イタリア向け会計統合を設定する

イタリア向けの会計プリンター統合サンプルは、[会計統合機能](fiscal-integration-for-retail-channel.md)に基づいており、Retail SDK に含まれています。 サンプルは [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) リポジトリの **src\\FiscalIntegration\\EpsonFP90IIISample** フォルダーにあります (例: [リリース/9.33 のサンプル](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample)) サンプルは、Commerce Runtime (CRT) の拡張である会計ドキュメント プロバイダーと、Commerce ハードウェア ステーションの拡張である会計コネクタで [構成されています](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)。 Retail SDK の使用方法の詳細については [Retail SDK のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) と [独立したパッケージ SDK のビルド パイプラインを設定する](../dev-itpro/build-pipeline.md) を参照してください。

> [!WARNING]
> [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、この会計統合サンプルでは使用できません。 Microsoft Dynamics Lifecycle Services (LCS) の開発者仮想マシン (VM) で、Retail SDK の以前のバージョンを使用する必要があります。 詳細については、[イタリア向け会計年度プリンター統合サンプルの展開ガイドライン (レガシ)](emea-ita-fpi-sample-sdk.md)を参照してください。
>
> 今後のバージョンで、会計統合サンプルの新しい独立したパッケージと拡張モデルのサポートを計画しています。

[Commerce チャンネルの会計統合を設定する](setting-up-fiscal-integration-for-retail-channel.md)で説明されている会計統合の設定手順を実行します。

1. [会計登録プロセスの設定](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process)。 また、[今回の会計プリンター統合サンプルに固有](#set-up-the-registration-process)の会計登録処理の設定をメモしておきます。
1. [割引用の会計テキストを設定します](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts)。
1. [エラーの処理の設定](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings)。
1. [POS からの会計 X/Z レポートの設定](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos)。
1. [延期された会計登録の手動実行を可能にする](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration)。
1. [POS に顧客情報を管理する機能を設定します](emea-ita-customer-information.md#setup)。
1. [チャネル コンポーネントの構成](#configure-channel-components)。

### <a name="set-up-the-registration-process"></a>登録プロセスの設定

登録プロセスを有効化する場合は、次の手順に従って Commerce Headquarters を設定します。 詳細情報については、[コマース チャネルの会計統合の設定](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) を参照してください。

1. 会計ドキュメント プロバイダーと会計コネクタの構成ファイルをダウンロードします。

    1. [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) レポジトリ を開きます。
    1. SDK/アプリケーションのバージョンに応じた適切なリリース ブランチ バージョンを選択します (例: **[リリース/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**)。
    1. **src \> FiscalIntegration \> EpsonFP90IIISample** を開きます。
    1. 会計ドキュメント プロバイダー構成ファイルを **CommerceRuntime \> DocumentProvider.EpsonFP90IIISample \> Configuration \> DocumentProviderEpsonFP90IIISample.xml** (例: [リリース/9.33 のファイル](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/CommerceRuntime/DocumentProvider.EpsonFP90IIISample/Configuration/DocumentProviderEpsonFP90IIISample.xml)) でダウンロードします。
    1. 会計コネクター構成ファイルを **HardwareStation \> EpsonFP90IIIFiscalDeviceSample \> Configuration \> ConnectorEpsonFP90IIISample.xml** (例: [リリース/9.33 のファイル](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/HardwareStation/EpsonFP90IIIFiscalDeviceSample/Configuration/ConnectorEpsonFP90IIISample.xml)) でダウンロードします。

    > [!WARNING]
    > [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、この会計統合サンプルでは使用できません。 LCS の開発者 VM では以前のバージョンの Retail SDK を使用する必要があります。 この会計統合サンプルの構成ファイルは、LCS の開発者 VM 上の Retail SDK が含む次のフォルダーに存在します。
    >
    > - **会計ドキュメント プロバイダー構成ファイル:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extension.DocumentProvider.EpsonFP90IIISample\\Configuration\\DocumentProviderEpsonFP90IIISample.xml
    > - **会計コネクタ 構成ファイル:**  RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EpsonFP90IIIFiscalDeviceSample\\Configuration\\ConnectorEpsonFP90IIISample.xml
    > 
    > 今後のバージョンで、会計統合サンプルの新しい独立したパッケージと拡張モデルのサポートを計画しています。

1. **Retail とコマース \> 本社の設定 \> パラメーター \> コマース共有パラメーター** の順に移動します。 **一般** タブで、**会計統合の有効化** オプションを **はい** に設定します。
1. **Retail と Commerce \> チャネル設定 \> 会計統合 \> 会計ドキュメント プロバイダー** に移動し、先ほどダウンロードした会計ドキュメント プロバイダー コンフィギュレーション ファイルを読み込みます。
1. **Retail と Commerce \> チャネル設定 \> 会計統合 \> 会計コネクタ** に移動し、先ほどダウンロードした会計コネクタ コンフィギュレーション ファイルを読み込みます。
1. **Retail と Commerce \> チャネル設定 \> 会計統合 \> コネクタ機能プロファイル** の順に移動します。 新しいコネクタ機能プロファイルを作成します。 以前に読み込んだドキュメント プロバイダーとコネクタを選択します。 必要に応じて [データ マッピング設定](#default-data-mapping) を更新します。
1. **Retail とコマース \> チャネル設定 \> 会計統合 \> コネクタ技術プロファイル** の順に移動します。 新しいコネクタ テクニカル プロファイルを作成し、先に読み込んだ会計コネクタを選択します。 必要に応じて [コネクタの設定](#fiscal-connector-settings) を更新します。
6. **Retail と Commerc \> チャネル設定 \> 会計統合 \> 会計コネクタ グループ** の順に移動します。 以前に作成したコネクタ機能プロファイルに、新しい会計コネクタ グループを作成します。
7. **Retail と Commerce \> チャネル設定 \> 会計統合 \> 会計登録プロセス** の順に移動します。 新しい会計登録プロセスと会計登録プロセス ステップを作成し、以前に作成した会計コネクタ グループを選択します。
8. **Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> 機能プロファイル** の順に移動します。 登録プロセスを有効化する、店舗にリンクされている機能プロファイルを選択します。 **会計登録プロセス** クイックタブで、以前に作成した会計登録プロセスを選択します。
9. **Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> ハードウェア プロファイル** の順に移動します。 会計プリンターの接続先のハードウェア ステーションにリンクされているハードウェア プロファイルを選択します。 **会計周辺機器** クイックタブで、先ほど作成したコネクタ テクニカル プロファイルを選択します。
10. 配布スケジュール (**Retail と Commerce \> Retail と Commerce IT \> 配送スケジュール**) を開き、ジョブ **1070** と **1090** を選択してチャネル データベースにデータを転送します。

#### <a name="default-data-mapping"></a>既定のデータ マッピング

次の既定のデータ マッピングは、会計統合サンプルの一部として提供される会計ドキュメント プロバイダー構成に含まれています。

- **テンダー タイプのマッピング**- 店舗に構成されている支払い方法と、会計プリンターが対応する支払タイプのマッピング。 次の例は、既定のマッピングを示します。

    ```JSON
    {"PaymentMethods": [
        {"StorePaymentMethod":"1", "PrinterPaymentType":"0", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"3", "PrinterPaymentType":"2", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"4", "PrinterPaymentType":"2", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"6", "PrinterPaymentType":"0", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"8", "PrinterPaymentType":"6", "PrinterPaymentIndex":"01"}
        ],
        "DepositPaymentMethod": {"PrinterPaymentType":"2", "PrinterPaymentIndex":"00"}}
    ```

    このマッピングの属性に関する説明を次に示します。

    - **StorePaymentMethod** は、**小売とコマース \> チャネル設定 \> 支払方法 \> 支払方法** で店舗に対して設定した支払方法です。
    - **PrinterPaymentType** と **PrinterPaymentIndex** は、Epson 会計プリンター ドキュメントで定義された、対応する支払の種類とインデックスです。
    - **DepositPaymentMethod** は、顧客注文の前金で決済する顧客注文の受取金額の一部に対して、プリンターの支払種類とインデックスを指定するために使用します。

    次のテーブルは、支払方法のサンプル マッピングを、標準のデモ データで構成された店舗の支払方法に対応させる方法を示します。

    | 支払方法 | 支払方法名 |
    |----------------|---------------------|
    | 1              | 現金                |
    | 3              | カード                |
    | 4              | 顧客 ID    |
    | 6              | 通貨            |
    | 8              | ギフト カード           |

    アプリケーションで構成されている支払い方法に合わせて、サンプルのマッピングを変更する必要があります。

- **領収書番号のバーコード タイプ** – 会計領収書に領収書番号を表示するために使用するバーコードの種類。 既定のマッピングは **CODE128** です。
- **領収書ヘッダーに会計データを印刷する** – このパラメーターをオンにすると、店舗情報を会計領収書に印刷します。 この情報は、店舗の名前、住所、税 ID 番号、レジ担当者の名前を含みます。
- **会計プリンター部門のマッピング** – 会計プリンターの部門と、付加価値税 (VAT) 率、VAT 控除の性質、製品の種類のマッピング。 次の例は、既定のマッピングを示します。

    ```JSON
    {"Departments": [
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"01"},
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"02"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"03"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"04"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"05"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"06"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"07"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"08"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"09"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"10"},
        {"VATRate":"0000", "VATExemptNature":"NS", "ProductType":"0", "DepartmentNumber":"99"}]}
    ```

    このマッピングの属性に関する説明を次に示します。

    - **VATRate** は、消費税コードとして構成された対応する VAT 率です。 マッピングの値には小数点以下 2 桁が表示されますが、小数点は使用しません。 たとえば **2200** は 22% を表し、**1000** は 10% を表します。
    - **VATExemptNature** は、無税の場合を含め、VAT 率が 0 (ゼロ) の場合にのみ適用します。 現在、**VATExemptNature** に対応するのはギフト カードのみであり、このマッピングの値は XML 構成ファイルの **VATExemptNatureForGiftCard** プロパティ値と対応する必要があります。
    - **ProductType** は製品の種類です。 値 **0** は商品を表し、値 **1** はサービスを表します。
    - **DepartmentNumber** はプリンターで構成した部門の数を表し、前の 3 つの属性と対応します。

    アプリケーションで構成した VAT 率と、会計プリンターで構成した対応する部門に従って、サンプル マッピングを変更する必要があります。

- **ギフト カードの VAT 免税の性質** – ギフト カードの発行や補充で適用する VAT 免税の性質。 この値は、会計プリンター部門マッピングの一部の入力と対応させる必要があります。 既定のマッピングは **NS** です。
- **無料品目を有効化する** – このパラメーターをオンにすると、100% 割引を適用する品目に対する特別な *omaggio* 割引調整タイプを有効化します。
- **返品元の情報コード** – 元の領収書を提供しない場合に、返品トランザクションの元を取得するために使用する情報コード。 このパラメーターは **元の販売日の情報コード** と **返品元のマッピング** パラメーターと一緒に使用し、元の販売トランザクションが存在しない場合に、返品トランザクションの発生元に関する、会計領収書の正しいメッセージを生成します。 

    返品が発生した可能性のある元を、ユーザーが店舗で選択または入力できるように、この情報コードを構成する必要があります。 たとえば、サブコードのリストとして構成できます (**サイトからの返品** や **キオスクからの返品** など)。 次に、**返品元のマッピング** パラメーターを使用して、情報コードの値を会計プリンターのコマンドに変換します。

    **返品元の情報コード** に対して選択した情報コードは、販売トランザクションごとに 1 回発生する必須の情報コードとして設定する必要があります。 これは POS 機能プロファイルで **返品** 情報コードとして割り当てる必要があるため、**返品** 操作の実行時に発生します。

    このマッピングに既定値を指定していません。 アプリケーションで設定した情報コードを選択する必要があります。

- **元の販売日の情報コード** – 元の領収書を提供しない場合に、返品トランザクションの元の販売日を取得するために使用する情報コード。 このパラメーターは **返品元の情報コード** と **返品元のマッピング** パラメーターと一緒に使用し、元の販売トランザクションが存在しない場合に、返品トランザクションの発生元に関する、会計領収書の正しいメッセージを生成します。

    **入力タイプ** フィールドが **日付** に設定されるように、情報コードを構成する必要があります。 これは販売トランザクションごとに 1 回発行する必須の情報コードとして構成する必要があります。 また、**返品元の情報コード** パラメーターに対して選択した情報コードの **リンクされた情報コード** として割り当てる必要があるため、2 つの情報コードが順次発行されます。

    このマッピングに既定値を指定していません。 アプリケーションで設定した情報コードを選択する必要があります。

- **返品元のマッピング** – 元の領収書を提供しない場合に、返品トランザクションの元を印刷するために使用する返品元のマッピング。 このパラメーターは **返品元の情報コード** と **元の販売日の情報コード** パラメーターと一緒に使用し、元の販売トランザクションが存在しない場合に、返品トランザクションの発生元に関する、会計領収書の正しいメッセージを生成します。 次の例は、既定のマッピングを示します。

    ```JSON
    {"ReturnOrigins": [
        {"ReturnOrigin":"1", "PrinterReturnOrigin":"POS"},
        {"ReturnOrigin":"2", "PrinterReturnOrigin":"ND"}
        ],
        "PrinterReturnOriginWithoutFiscalData":"POS"}
    ```

    このマッピングの属性に関する説明を次に示します。

    - **ReturnOrigin** は、店舗での返品元の可能性の 1 つです。 この値は **返品元の情報コード** パラメーターの値と対応させる必要があります。
    - **PrinterReturnOrigin** は、会計プリンターが受け付ける返品元の 1 つです (**POS**、**VR**、**ND**)。
    - **PrinterReturnOriginWithoutFiscalData** は会計プリンターが受け付ける返品元であり、会計プリンターから登録していないため、会計データをリンクしていない元の販売トランザクションとリンクされている返品トランザクションに対応します。 この場合、元の販売日を元の販売トランザクションの日付として識別します。

次の既定データ マッピングは非推奨であり、下位互換性のみを維持しています。

- 付加価値税 (VAT) コード マッピング
- 預金の支払タイプ

#### <a name="fiscal-connector-settings"></a>会計コネクタの設定

次の設定は、会計統合サンプルの一部として提供される会計コネクタ構成に含まれています。

- **エンドポイント アドレス** – プリンターの URL。
- **日時の同期** – プリンターの日時を接続したハードウェア ステーションと同期する必要があるかどうかを指定する値。

### <a name="configure-channel-components"></a>チャネル コンポーネントの構成

> [!WARNING]
> [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、この会計統合サンプルでは使用できません。 LCS の開発者 VM では以前のバージョンの Retail SDK を使用する必要があります。 詳細については、[イタリア向け会計年度プリンター統合サンプルの展開ガイドライン (レガシ)](emea-ita-fpi-sample-sdk.md)を参照してください。
>
> 今後のバージョンで、会計統合サンプルの新しい独立したパッケージと拡張モデルのサポートを計画しています。

#### <a name="set-up-the-development-environment"></a>開発環境の設定

開発環境を設定してサンプルのテストと拡張を行う際は、次の手順に従います。

1. [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions) リポジトリをクローンまたはダウンロードします。 SDK/アプリケーションのバージョンに応じた適切なリリース ブランチ バージョンを選択します。 詳細については、[GitHub と NuGet から Retail SDK サンプルと参照パッケージをダウンロードする](../dev-itpro/retail-sdk/sdk-github.md) を参照してください。
1. **Dynamics365Commerce.Solutions\\FiscalIntegration\\EpsonFP90IIISample\\EpsonFP90IIISample.sln** で会計プリンター統合ソリューションを開き、ビルドします。
1. CRT 拡張機能をインストールします:

    1. CRT 拡張機能のインストーラを見つけます。

        - **Commerce Scale Unit:** **EpsonFP90IIISample\\ScaleUnit\\ScaleUnit.EpsonFP90III.Installer\\bin\\Debug\\net461** フォルダーで、**ScaleUnit.EpsonFP90III.Installer** インストーラーを見つけます。
        - **Modern POS 上のローカル CRT:** **EpsonFP90IIISample\\ModernPOS\\ModernPOS.EpsonFP90III.Installer\\bin\\Debug\\net461** フォルダーで、**ModernPOS.EpsonFP90III.Installer** インストーラーを見つけます。

    1. コマンド ラインから CRT 拡張機能インストーラーを起動します。

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.EpsonFP90III.Installer.exe install --verbosity 0
            ```

        - **最新 POS のローカル CRT:**

            ```Console
            ModernPOS.EpsonFP90III.Installer.exe install --verbosity 0
            ```

1. ハードウェア ステーション拡張機能をインストールする。

    1. **EpsonFP90IIISample\\HardwareStation\\HardwareStation.EpsonFP90III.Installer\\bin\\Debug\\net461** フォルダーで、**HardwareStation.EpsonFP90III.Installer** インストーラーを見つけます。
    1. コマンド ラインから拡張機能インストーラーを起動します。

        ```Console
        HardwareStation.EpsonFP90III.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>運用環境

[会計統合サンプルのビルド パイプラインを設定する](fiscal-integration-sample-build-pipeline.md) の手順に従って、会計統合サンプルの Cloud Scale Unit とセルフサービスの展開可能なパッケージを生成し、リリースします。 **EpsonFP90III build-pipeline.yml** テンプレートの YAML ファイルは、[Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions) リポジトリの **パイプライン\\YAML_Files** フォルダにあります。

## <a name="design-of-extensions"></a>拡張機能の設計

イタリア向けの会計プリンター統合サンプルは、[会計統合機能](fiscal-integration-for-retail-channel.md)に基づいており、Retail SDK に含まれています。 サンプルは [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) リポジトリの **src\\FiscalIntegration\\EpsonFP90IIISample** フォルダーにあります (例: [リリース/9.33 のサンプル](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample)) サンプルは、CRT の拡張である会計ドキュメント プロバイダーと、Commerce ハードウェア ステーションの拡張である会計コネクタで [構成されています](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)。 Retail SDK の使用方法の詳細については [Retail SDK のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) と [独立したパッケージ SDK のビルド パイプラインを設定する](../dev-itpro/build-pipeline.md) を参照してください。

> [!WARNING]
> [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、この会計統合サンプルでは使用できません。 LCS の開発者 VM では以前のバージョンの Retail SDK を使用する必要があります。 詳細については、[イタリア向け会計年度プリンター統合サンプルの展開ガイドライン (レガシ)](emea-ita-fpi-sample-sdk.md)を参照してください。 今後のバージョンで、会計統合サンプルの新しい独立したパッケージと拡張モデルのサポートを計画しています。

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime 拡張機能の設計

会計ドキュメント プロバイダーである拡張機能の目的は、プリンターに特化したドキュメントを生成して会計プリンターからの応答を処理することです。

#### <a name="request-handler"></a>要求ハンドラー

**DocumentProviderEpsonFP90III** 要求ハンドラーは、会計プリンタからドキュメントを生成するリクエストのエントリ ポイントです。

ハンドラは **INamedRequestHandler** インターフェイスから継承します。 **HandlerName** メソッドの機能がハンドラーの名前を返します。 このハンドラー名は、Commerce headquarters で指定したコネクタ ドキュメント プロバイダーの名前と一致する必要があります。

このコネクタは次の要求をサポートします。

- **GetFiscalDocumentDocumentProviderRequest** – この要求は生成するべきドキュメントに関する情報を含みます。 これは会計プリンターに登録するべきプリンター固有のドキュメントを返します。
- **GetSupportedRegistrableEventsDocumentProviderRequest** – この要求はサブスクライブするイベントのリストを返します。 現在サポートするイベントを次に示します: 販売、X レポートの印刷、Z レポートの印刷。

#### <a name="configuration"></a>構成

会計ドキュメント プロバイダーの構成ファイルは、[Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) レポジトリの **src\\FiscalIntegration\\EpsonFP90IIISample\\CommerceRuntime\\DocumentProvider.EpsonFP90IIISample\\Configuration\\DocumentProviderEpsonFP90IIISample.xml** にあります。 このファイルによって、Commerce Headquarters からドキュメント プロバイダーの設定を構成できるようになります。 ファイル形式は会計統合構成の要件に従います。

### <a name="hardware-station-extension-design"></a>ハードウェア ステーション拡張機能の設計

会計コネクタである拡張機能によって、会計プリンターと通信できます。 この拡張機能は HTTP プロトコルを使用し、CRT 拡張機能が生成するドキュメントを会計プリンターに送信します。 また、会計プリンターから受信した応答も処理します。

#### <a name="request-handler"></a>要求ハンドラー

**EpsonFP90IIISample** 要求ハンドラーは、会計の周辺機器への要求を処理するエントリ ポイントです。

ハンドラは **INamedRequestHandler** インターフェイスから継承します。 **HandlerName** メソッドの機能がハンドラーの名前を返します。 このハンドラー名は、Commerce headquarters で指定した会計コネクタの名前と一致する必要があります。

このコネクタは次の要求をサポートします。

- **SubmitDocumentFiscalDeviceRequest** – この要求はドキュメントをプリンターに送信し、会計プリンターからの応答を返します。
- **IsReadyFiscalDeviceRequest** – この要求はデバイスの正常性確認に使用します。
- **InitializeFiscalDeviceRequest** – この要求はプリンターの初期化に使用します。

#### <a name="configuration"></a>構成

会計コネクタの構成ファイルは、[Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) リポジトリの **src\\FiscalIntegration\\EpsonFP90IIISample\\HardwareStation\\EpsonFP90IIIFiscalDeviceSample\\Configuration\\ConnectorEpsonFP90IIISample.xml** にあります。 このファイルによって、Commerce Headquarters からコネクタの設定を構成できるようになります。 ファイル形式は会計統合構成の要件に従います。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
