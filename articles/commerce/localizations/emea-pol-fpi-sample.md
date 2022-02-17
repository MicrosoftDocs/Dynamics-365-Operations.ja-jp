---
title: ポーランド向け会計プリンター統合サンプル
description: このトピックでは、Microsoft Dynamics 365 Commerce のポーランド向け会計統合サンプルの概要について説明します。
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-2-1
ms.openlocfilehash: 43d9a54334d97a65a1f9a356daf54154f6c069b3
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076839"
---
# <a name="fiscal-printer-integration-sample-for-poland"></a>ポーランド向け会計プリンター統合サンプル

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce のポーランド向け会計統合サンプルの概要について説明します。

ポーランド向け Dynamics 365 Commerce 機能には、POSと会計用プリンターの連携のサンプルが含まれています。 このサンプルは、[会計統合機能](fiscal-integration-for-retail-channel.md)を拡張し、[Posnet Polska S.A.](https://www.posnet.com.pl) の会計プリンタ用プロトコル POSNET THERMAL HD 2.02 をサポートしており、COM ポートで接続された会計プリンタと、ネイティブ ソフトウェア ドライバを使用して通信することができます。 Posnet Thermal HD FV EJ は、Posnet が提供している Posnet Thermal HD FV EJ のソフトウェア エミュレータを使って実装し、テストを行いました。 このサンプルはソース コード形式で提供され、Retail ソフトウェア開発キット (SDK) に含まれます。

マイクロソフトは、Posnet からハードウェア、ソフトウェア、ドキュメントをリリースしていません。 会計プリンタの入手方法や操作方法については、[Posnet Polska S.A.](https://www.posnet.com.pl) にお問い合わせください

## <a name="scenarios"></a>シナリオ

ポーランド向けの会計プリンター統合サンプルでは、以下のシナリオをカバーしています:

- 販売シナリオ:

    - 現金払いで持ち帰りの販売と返品の会計レシートを印刷します。
    - 会計プリンターからの応答をキャプチャして、チャネル データベースに格納します。
    - 税金:

        - 会計プリンターの税コード (部門) にマッピングします。
        - マッピングされた税データを会計プリンタに転送します。

    - 支払:

        - 会計プリンターの支払い方法に対応したマッピング。
        - 会計のレシートに支払を印刷します。
        - 変更情報を印刷します。

    - 明細の割引を印刷します。
    - ギフト カード:

        - 販売の会計レシートから、発行/際チャージされたギフトカードの明細行を除外します。
        - ギフト カードを通常の支払い方法として使用する支払いを印刷します。

    - 顧客の注文操作に伴う会計の領収書の印刷:

        - 顧客注文の入金で、会計のレシートが印刷されません。
        - ハイブリッドド顧客注文の繰り出し明細行の会計レシートを印刷します。
        - 顧客の注文に対する集荷作業の会計レシートを印刷します。
        - 返品注文の会計レシートを印刷します。

    - 販売トランザクションで指定された[顧客情報](emea-pol-customer-information.md)を会計レシートに印刷します。 この情報の例として、顧客の VAT 番号が使用されます。

- 終了日に関する明細書 (会計年度 X レポートと会計年度 Z レポート)。
- 次のオプションなど、エラー処理。

    - 会計プリンターが接続されていない、準備ができていない、応答がない、プリンターの紙切れ、紙詰まりなど、再試行が可能な場合は、会計登録を再試行します。
    - 会計登録の延期。
    - 会計登録をスキップするか、またはトランザクションを登録済みとしてマークして、失敗した理由と追加情報を取得するための情報コードを含めます。
    - 新しい販売トランザクションの開始時や販売トランザクション確定時に、会計用プリンターの使用可能性を確認します。

### <a name="gift-cards"></a>ギフト カード

会計プリンターの統合サンプルでは、ギフト カードに関連する以下のルールを実装しています:

- *ギフトカードの発行* と *ギフトカード* への追加の操作に関連する販売明細行を会計の領収書から除外します。
- ギフトカードの明細行だけで構成される会計レシートは印刷しません。
- ギフトカードを発行したり、チャージしたりした場合、その合計金額を会計上の領収書の支払い明細行から差し引きます。
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
- 日次レポート (X 年度、Z 年度) は、埋め込み式の *シフト レポート* 形式で印刷します。
- 会計のレシートにバーコードを印刷することは、潜在的なカスタマイズと考えられます。なぜなら、この機能は埋め込みフォーマットではサポートされておらず、カスタマイズ可能な **スーパーフォーマット** レポートを使用してのみ実装できるためです。
- 会計プリンタでは、混合トランザクションをサポートしていません。 POS 機能のプロファイルでは、**1 枚のレシートに販売と返品の混在禁止** オプションを **はい** に設定する必要があります。

## <a name="set-up-fiscal-integration-for-poland"></a>ポーランド向け、会計統合の設定

ポーランド向けの会計プリンター統合サンプルは、[会計統合機能](fiscal-integration-for-retail-channel.md)に基づいており、Retail SDK に含まれています。 サンプルは [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) リポジトリの **src\\FiscalIntegration\\Posnet** フォルダにあります (例: [release/9.33 のサンプル](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet)) サンプルは、Commerce Runtime (CRT) の拡張である会計ドキュメント プロバイダーと、Commerce ハードウェア ステーションの拡張である会計コネクタで [構成されています](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)。 Retail SDK の使用方法の詳細については [Retail SDK のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) と [独立したパッケージ SDK のビルド パイプラインを設定する](../dev-itpro/build-pipeline.md) を参照してください。

> [!WARNING]
> [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、この会計統合サンプルでは使用できません。 Microsoft Dynamics Lifecycle Services (LCS) の開発者仮想マシン (VM) で、Retail SDK の以前のバージョンを使用する必要があります。 詳細については、[ポーランド向け会計年度プリンター統合サンプルの配置ガイドライン (レガシ)](emea-pol-fpi-sample-sdk.md)を参照してください。
>
> 今後のバージョンで、会計統合サンプルの新しい独立したパッケージと拡張モデルのサポートを計画しています。

[Commerce チャンネルの会計統合を設定する](setting-up-fiscal-integration-for-retail-channel.md)で説明されている会計統合の設定手順を実行します。

1. [会計登録プロセスの設定](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process)。 また、[今回の会計プリンター統合サンプルに固有](#set-up-the-registration-process)の会計登録処理の設定をメモしておきます。
1. [エラーの処理の設定](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings)。
1. [POS からの会計 X/Z レポートの設定](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos)。
1. [延期された会計登録の手動実行を可能にする](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration)。
1. [チャネル コンポーネントの構成](#configure-channel-components)。

### <a name="set-up-the-registration-process"></a>登録プロセスの設定

登録プロセスを有効化する場合は、次の手順に従って Commerce Headquarters を設定します。 詳細情報については、[コマース チャネルの会計統合の設定](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) を参照してください。

1. 会計ドキュメント プロバイダーと会計コネクタの構成ファイルをダウンロードします。

    1. [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) レポジトリ を開きます。
    1. SDK/アプリケーションのバージョンに応じた適切なリリース ブランチ バージョンを選択します (例: **[リリース/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**)。
    1. **src \>FiscalIntegration \>Posnet** を開きます。
    1. 会計ドキュメント プロバイダ構成ファイルを **CommerceRuntime \> DocumentProvider.PosnetSample \> Configuration \> DocumentProviderPosnetSample.xml** (例: [release/9.33 のファイルなど](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/CommerceRuntime/DocumentProvider.PosnetSample/Configuration/DocumentProviderPosnetSample.xml)) でダウンロードします。
    1. 会計コネクター構成ファイルを **HardwareStation \> ThermalDeviceSample \> Configuration \> ConnectorPosnetThermalFVEJ.xml** (例: [release/9.33 のファイル](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/HardwareStation/ThermalDeviceSample/Configuration/ConnectorPosnetThermalFVEJ.xml)) でダウンロードします。

    > [!WARNING]
    > [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、この会計統合サンプルでは使用できません。 LCS の開発者 VM では以前のバージョンの Retail SDK を使用する必要があります。 この会計統合サンプルの構成ファイルは、LCS の開発者 VM 上の Retail SDK が含む次のフォルダーに存在します。
    >
    > - **会計ドキュメント プロバイダ構成ファイル:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extension.DocumentProvider.PosnetSample\\Configuration\\DocumentProviderPosnetSample.xml
    > - **会計コネクタ 構成ファイル:**  RetailSdk\\SampleExtensions\\HardwareStation\\Extension.Posnet.ThermalDeviceSample\\Configuration\\ConnectorPosnetThermalFVEJ.xml
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

- **付加価値税 (VAT) レート マッピング** - 消費税コードに設定されている税のパーセンテージ値と、会計プリンタ固有の VAT レートとのマッピングです。 既定のマッピングを次に示します。

    ```
    0 : 23.00 ; 1 : 8.00 ; 2 : 5.00 ; 3 : 0.00
    ```

    各ペアの最初のコンポーネントは、会計プリンタに設定されている VAT レート番号を表しています。 2 番目のコンポーネントは対応する VAT 率を表します。 会計プリンターの VAT レートの構成については、POSNET ドライバのドキュメントを参照してください。

- **テンダー タイプのマッピング**- 店舗に構成されている支払い方法と、会計プリンターが対応している支払いフォームのマッピング。 既定のマッピングを次に示します。

    ```
    0 : 0 ; 1 : 0 ; 2 : 2 ; 3 : 2 ; 4 : 0 ; 5 : 0 ; 6 : 0 ; 7 : 2 ; 8 : 0
    ```

    各ペアの最初のコンポーネントは、ストアに設定されている支払い方法を表しています。 2つ目のコンポーネントは、会計プリンターでサポートされている対応する支払いフォームを表します。 会計プリンターがサポートしている支払いフォームについては、POSNET ドライバーのドキュメントを参照してください。 アプリケーションで構成されている支払い方法に合わせて、サンプルのマッピングを変更する必要があります。

#### <a name="fiscal-connector-settings"></a>会計コネクタの設定

次の設定は、会計統合サンプルの一部として提供される会計コネクタ構成に含まれています。

- **接続文字列** – デバイスへの接続の詳細を、ドライバーがサポートしているフォーマットで記述した文字列です。 詳細については、POSNET ドライバーのドキュメントを参照してください。
- **日時の同期** – プリンターの日時を接続したハードウェア ステーションと同期する必要があるかどうかを指定する値。
- **デバイスのタイムアウト** – ドライバーがデバイスからの応答を待機する時間を、ミリ秒単位 (ms) で表します。 詳細については、POSNET ドライバーのドキュメントを参照してください。

### <a name="configure-channel-components"></a>チャネル コンポーネントの構成

> [!WARNING]
> [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、この会計統合サンプルでは使用できません。 LCS の開発者 VM では以前のバージョンの Retail SDK を使用する必要があります。 詳細については、[ポーランド向け会計年度プリンター統合サンプルの配置ガイドライン (レガシ)](emea-pol-fpi-sample-sdk.md)を参照してください。
>
> 今後のバージョンで、会計統合サンプルの新しい独立したパッケージと拡張モデルのサポートを計画しています。

#### <a name="set-up-the-development-environment"></a>開発環境の設定

開発環境を設定してサンプルのテストと拡張を行う際は、次の手順に従います。

1. [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions) リポジトリをクローンまたはダウンロードします。 SDK/アプリケーションのバージョンに応じた適切なリリース ブランチ バージョンを選択します。 詳細については、[GitHub と NuGet から Retail SDK サンプルと参照パッケージをダウンロードする](../dev-itpro/retail-sdk/sdk-github.md) を参照してください。
1. **Dynamics365Commerce.Solutions\\FiscalIntegration\\Posnet\\Posnet.sln** で会計プリンター統合ソリューションを開き、ビルドします。
1. CRT 拡張機能をインストールします:

    1. CRT 拡張機能のインストーラを見つけます。

        - **Commerce Scale Unit:**  **Posnet\\ScaleUnit\\ScaleUnit.Posnet.Installer\\bin\\Debug\\net461** フォルダで、**ScaleUnit.Posnet.Installer** インストーラーを探します。
        - **Modern POS 上のローカル CRT:** **Posnet\\ModernPOS\\ModernPOS.Posnet.Installer\\bin\\Debug\\net461** フォルダ内で、**ModernPOS.Posnet.Installer** インストーラーを探します。

    1. コマンド ラインから CRT 拡張機能インストーラーを起動します。

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.Posnet.Installer.exe install --verbosity 0
            ```

        - **最新 POS のローカル CRT:**

            ```Console
            ModernPOS.Posnet.Installer.exe install --verbosity 0
            ```

1. ハードウェア ステーション拡張機能をインストールする。

    1. **Posnet\\HardwareStation\\HardwareStation.PosnetThermalFVFiscalPrinter.Installer\\bin\\Debug\\net461** フォルダで、**HardwareStation.PosnetThermalFVFiscalPrinter.Installer** インストーラーを探します。
    1. コマンド ラインから拡張機能インストーラーを起動します。

        ```Console
        HardwareStation.PosnetThermalFVFiscalPrinter.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>実稼働環境

[会計統合サンプルのビルド パイプラインを設定する](fiscal-integration-sample-build-pipeline.md) の手順に従って、会計統合サンプルの Cloud Scale Unit とセルフサービスの展開可能なパッケージを生成し、リリースします。 **Posnet build-pipeline.yml** テンプレートの YAML ファイルは、[Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions) リポジトリの **パイプライン\\YAML_Files** フォルダにあります。

## <a name="design-of-extensions"></a>拡張機能の設計

ポーランド向けの会計プリンター統合サンプルは、[会計統合機能](fiscal-integration-for-retail-channel.md)に基づいており、Retail SDK に含まれています。 サンプルは [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) リポジトリの **src\\FiscalIntegration\\Posnet** フォルダにあります (例: [release/9.33 のサンプル](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet)) サンプルは、CRT の拡張である会計ドキュメント プロバイダーと、Commerce ハードウェア ステーションの拡張である会計コネクタで [構成されています](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)。 Retail SDK の使用方法の詳細については [Retail SDK のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) と [独立したパッケージ SDK のビルド パイプラインを設定する](../dev-itpro/build-pipeline.md) を参照してください。

> [!WARNING]
> [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、この会計統合サンプルでは使用できません。 LCS の開発者 VM では以前のバージョンの Retail SDK を使用する必要があります。 詳細については、[ポーランド向け会計年度プリンター統合サンプルの配置ガイドライン (レガシ)](emea-pol-fpi-sample-sdk.md)を参照してください。 今後のバージョンで、会計統合サンプルの新しい独立したパッケージと拡張モデルのサポートを計画しています。

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime 拡張機能の設計

会計ドキュメント プロバイダーである拡張機能の目的は、プリンターに特化したドキュメントを生成して会計プリンターからの応答を処理することです。 この拡張機能は、POSNET 仕様 19-3678 で定義されている JavaScript Object Notation (JSON) 形式のプリンタ固有のコマンドセットを生成します。

#### <a name="request-handler"></a>要求ハンドラー

**DocumentProviderPosnetProtocol** 要求ハンドラーは、会計プリンタからドキュメントを生成するリクエストのエントリ ポイントです。

ハンドラは **INamedRequestHandler** インターフェイスから継承します。 **HandlerName** メソッドの機能がハンドラーの名前を返します。 このハンドラー名は、Commerce headquarters で指定したコネクタ ドキュメント プロバイダーの名前と一致する必要があります。

このコネクタは次の要求をサポートします。

- **GetFiscalDocumentDocumentProviderRequest** – この要求は生成するべきドキュメントに関する情報を含みます。 これは会計プリンターに登録するべきプリンター固有のドキュメントを返します。
- **GetSupportedRegistrableEventsDocumentProviderRequest** – この要求はサブスクライブするイベントのリストを返します。 現在サポートするイベントを次に示します: 販売、X レポートの印刷、Z レポートの印刷。

#### <a name="configuration"></a>構成

会計ドキュメント プロバイダーの構成ファイルは、[Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) レポジトリの **src\\FiscalIntegration\\Posnet\\CommerceRuntime\\DocumentProvider.PosnetSample\\Configuration\\DocumentProviderPosnetSample.xml** にあります。 このファイルによって、Commerce Headquarters から会計ドキュメント プロバイダーの設定を構成できるようになります。 ファイル形式は会計統合構成の要件に従います。

### <a name="hardware-station-extension-design"></a>ハードウェア ステーション拡張機能の設計

会計コネクタである拡張機能によって、会計プリンターと通信できます。 この拡張機能は、POSNET ドライバの機能を呼び出して、CRT の拡張機能が生成したコマンドを会計プリンターに送信します。 また、デバイス エラーも処理します。

#### <a name="request-handler"></a>要求ハンドラー

**FiscalPrinterHandler** リクエスト ハンドラーは、会計の周辺機器への要求を処理するエントリ ポイントです。

ハンドラは **INamedRequestHandler** インターフェイスから継承します。 **HandlerName** メソッドの機能がハンドラーの名前を返します。 このハンドラー名は、Commerce headquarters で指定した会計コネクタの名前と一致する必要があります。

このコネクタは次の要求をサポートします。

- **SubmitDocumentFiscalDeviceRequest** – この要求はドキュメントをプリンターに送信し、会計プリンターからの応答を返します。
- **IsReadyFiscalDeviceRequest** – この要求はデバイスの正常性確認に使用します。
- **InitializeFiscalDeviceRequest** – この要求はプリンターの初期化に使用します。

#### <a name="configuration"></a>構成

会計コネクタの構成ファイルは、[Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) リポジトリの **src\\FiscalIntegration\\Posnet\\HardwareStation\\ThermalDeviceSample\\Configuration\\ConnectorPosnetThermalFVEJ.xml** にあります。 このファイルによって、Commerce Headquarters から会計コネクタの設定を構成できるようになります。 ファイル形式は会計統合構成の要件に従います。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
