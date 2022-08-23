---
title: チェコ共和国向け会計登録サービス統合サンプル
description: この記事では、Microsoft Dynamics 365 Commerce のチェコ共和国向け会計統合サンプルの概要について説明します。
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: dc7ef27954de2bb10bbaf91fc5a3aa14d6ee6ffd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280336"
---
# <a name="fiscal-registration-service-integration-sample-for-the-czech-republic"></a>チェコ共和国向け会計登録サービス統合サンプル

[!include[banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce のチェコ共和国向け会計統合サンプルの概要について説明します。

チェコ共和国のキャッシュ レジスターにおける現地の財政要件を満たすため、Dynamics 365 Commerce のチェコ共和国向け機能には、販売時点管理 (POS) と外部財政登録サービスとの統合例が含まれています。 このサンプルは [会計統合機能](fiscal-integration-for-retail-channel.md) を拡張します。 これは [EFSTA](https://efsta.org/) の [EFR (電子会計登録)](https://efsta.org/sicherheitsloesungen/) ソリューションに基づいており、HTTPS プロトコルによる EFR サービスとの通信を実現します。 EFR サービスは確実な販売の電子登録 (EET - Elektronická evidence tržeb) を実現します。つまり、税所轄官庁の会計 Web サービスに販売データをオンラインで送信します。

Commerce ハードウェア ステーション、またはハードウェア ステーションから接続できる別のマシンのいずれかで、EFR サービスをホストする必要があります。 このサンプルはソース コード形式で提供され、Retail ソフトウェア開発キット (SDK) に含まれます。

マイクロソフトは、EFSTA によるハードウェア、ソフトウェア、ドキュメントをリリースしません。 EFR ソリューションを入手して操作する方法については [EFSTA](https://efsta.org/kontakt/) に問い合わせてください。

## <a name="scenarios"></a>シナリオ

チェコ共和国向けの会計登録サービス統合サンプルでは、以下のシナリオをカバーしています:

- 会計登録サービスへの現金トランザクションの登録。

    - 詳細なトランザクション データを会計登録サービスに送信します。 このデータは、販売明細行情報、割引、支払い、税金に関する情報を含みます。 さらに会計登録サービスは、税所轄官庁の Web サービスにデータを送信し、トランザクションの会計識別コードを含む確認を受信します。
    - 会計登録サービスからの応答を取得します。 この応答は、トランザクションの会計識別コードやセキュリティ コードなどの会計データを含みます。
    - 登録したトランザクションの会計データを領収書に印刷します。

- 会計登録サービスでギフト カードの操作と顧客前金の登録を行う。

    - ギフト カードの発行や入金を行います。
    - 顧客前金口座を登録します。
    - 顧客注文を作成し、注文の前金を登録します。
    - 顧客注文を編集して注文の前金を上書きします。
    - 顧客注文をキャンセルして注文の前金を返金します。

- 次のオプションなど、エラー処理。

    - 会計登録サービスが利用できない場合、準備ができていない場合、応答していない場合など、再試行できるときは会計登録をやり直します。
    - 会計登録の延期。
    - 会計登録をスキップするか、またはトランザクションを登録済みとしてマークして、失敗した理由と追加情報を取得するための情報コードを含めます。
    - 新しい販売トランザクションの開始時や販売トランザクション確定時に、会計登録サービスの使用可能性を確認します。

### <a name="gift-cards"></a>ギフト カード

会計登録サービス統合サンプルでは、ギフト カードに関連する以下のルールを実装しています。

- トランザクションを会計登録サービスに登録する際に、販売トランザクションの *ギフト カードの発行* や *ギフト カードへの追加* の操作に関連する販売明細行を、特別な属性でマークします。
- ギフト カードによる支払を通常の支払と見なし、トランザクションを会計登録サービスに登録する際に特別な属性でマークします。

### <a name="customer-account-deposits-and-customer-order-deposits"></a>顧客前金口座と顧客手付金

会計登録サービス統合サンプルでは、顧客前金口座と顧客注文前金に関連した以下のルールを実装しています。

- 顧客前金口座や顧客手付金に関連するトランザクションを、単一明細行トランザクションとして会計登録サービスに登録して、特別な属性でマークします。 この明細行で前金 VAT グループを指定します。
- ハイブリッド顧客注文を作成した際は、つまり顧客が店舗から実行できる製品を含む顧客注文の場合や、後で集荷や発送を行う商品の場合は、会計登録サービスに登録するトランザクションに、実行した製品明細行と注文前金の明細行を含みます。
- 顧客口座による支払を通常の支払と見なし、トランザクションを会計登録サービスに登録する際に特別な属性でマークします。
- 顧客注文の集荷操作に適用される顧客注文前金の金額を通常の支払と見なし、トランザクションを会計登録サービスに登録する際に特別な属性でマークします。

### <a name="offline-registration"></a>オフライン登録

会計登録サービスが税所轄官庁の会計 Web サービスにトランザクション データを送信できず (例: 応答タイムアウトの発生)、さらに Web サービスから確認を受け取る場合 (つまりトランザクションの会計識別コード)、トランザクションのローカル署名を生成して、それに加えて特別なエラー コードを応答に含めます。 ネットワーク接続が回復するとすぐに、会計登録サービスはバックグラウンドで元の注文のトランザクションを再送信します。

### <a name="limitations-of-the-sample"></a>サンプルの制限事項

会計登録サービスは、消費税が価格に含まれているシナリオのみをサポートします。 したがって、**税込価格** オプションは、店舗と顧客の両方で **はい** に設定する必要があります。

## <a name="set-up-commerce-for-the-czech-republic"></a>チェコ共和国向け Commerce ローカライズの設定

このセクションでは、チェコ共和国に固有で推奨される Commerce 設定について説明します。 詳細については [Commerce のホーム ページ](../index.md) を参照してください。

チェコ共和国に固有の機能を使用する際は、次の設定を指定してください。

- 法人の基本住所で、**国/地域** フィールドを **CZE** (チェコ共和国) に設定します。
- チェコ共和国にあるすべての店舗の POS 機能プロファイルで、 **ISO コード フィールド** を **CZ** (チェコ共和国) に設定します。

チェコ共和国に対応する次の設定を指定する必要があります。 設定が完了したら、必ず適切な配布ジョブを実行します。

### <a name="set-up-vat-per-czech-republic-requirements"></a>チェコ共和国の要件に従って VAT を設定する


消費税コード、消費税グループ、品目の消費税グループを作成する必要があります。 また、製品やサービスの消費税情報を設定する必要があります。 消費税機能の設定と使用方法の詳細については、[消費税の概要](../../finance/general-ledger/indirect-taxes-overview.md)を参照してください。

### <a name="set-up-stores"></a>店舗を設定する

**すべての店舗** ページで店舗の詳細を更新します。 具体的には、次のパラメーターを設定します。

- **消費税グループ** フィールドで、既定の顧客への販売に使用するべき消費税グループを指定します。
- **税込価格** オプションに **はい** をセットします。
- **名前** フィールドに会社名を設定します。 この変更により、会社名が領収書に確実に表示されます。 または、会社名を自由形式のテキストとして領収書のレイアウトに追加できます。
- **税 ID 番号 (TIN)** フィールドに会社識別番号を設定します。 この変更により、会社の ID 番号が領収書に確実に表示されます。 または、会社 ID 番号を自由形式のテキストとして領収書のレイアウトに追加できます。

### <a name="set-up-functionality-profiles"></a>機能プロファイルを設定する

POS 機能プロファイルを設定します。

- **領収書番号** ファストタブ で、**販売**、**販売注文**、**返品** の領収書トランザクション タイプに対してレコードの作成や更新を行い、領収書番号を設定します。

### <a name="set-up-registration-numbers"></a>登録番号を設定する

1. **組織管理 \> グローバル アドレス帳 \> 登録タイプ \> 登録タイプ** の順に移動します。 登録タイプを作成します。 **国/地域** フィールドに **CZE** (チェコ共和国) を指定し、組織に制限を加えます。
2. **組織管理 \> グローバル アドレス帳 \> 登録タイプ \> 登録タイプ** の順に移動します。 新しい登録カテゴリを作成します。 前の手順で登録タイプを選択し、**登録カテゴリ** に **事業所 ID** を設定します。
3. **組織管理 \> 組織 \> 作業単位** の順に移動します。 チェコ共和国にある店舗ごとに、その店舗に関連する単位を選択します。 **住所** クイックタブで **その他のオプション** ドロップダウン リストを展開して **詳細** を選択します。 
4. 開いた **住所の管理** ページで、次の設定を指定する必要があります。

    - **住所** クイックタブで **国/地域** フィールドを **CZE** に設定します。
    - **登録 ID** クイックタブで新しいレコードを作成します。 以前作成した登録タイプを選択して、登録番号を設定します。

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>カスタム フィールドを設定して、販売領収書の領収書形式で使用できるようにする

POS 領収書形式で使用される言語テキストおよびカスタム フィールドを構成することができます。 領収書設定を作成するユーザーの既定の会社は、言語テキスト設定が作成された法人と同じである必要があります。 または、ユーザーの既定の会社、および設定の作成対象の店舗の法人の両方で、同じ言語テキストを作成する必要があります。

**言語テキスト** ページで、領収書 レイアウト用のカスタム フィールドのラベルに次のレコードを追加します。 テーブルに表示されている **言語 ID**、**テキスト ID**、および **テキスト** の値は、単なる例に過ぎません。 要件に合わせてそれらを変更できます。 ただし、使用する **テキスト ID** の値は一意である必要があり、900001 以上である必要があります。

テーブルの **言語テキスト** が含む **POS** セクションに、次の POS ラベルを追加します。

| 言語 ID | テキスト ID | テキスト                   |
|-------------|---------|------------------------|
| ja       | 900001  | ID provozovny/pokladny |
| ja       | 900002  | BKP                    |
| ja       | 900003  | PKP                    |
| ja       | 900004  | FIK                    |
| ja       | 900005  | 情報                   |
| ja       | 900006  | 一連番号        |

**カスタム フィールド** ページで、領収書 レイアウトのカスタム フィールドに次のレコードを追加します。 **キャプション テキスト ID** の値は、**言語テキスト** ページで指定した **テキスト ID** の値に対応している必要があることに注意してください。

| Name                 | 種類    | キャプション テキスト ID |
|----------------------|---------|-----------------|
| TLT                  | 受信 | 900001          |
| SEC                  | 受信 | 900002          |
| SIGN                 | 受信 | 900003          |
| FISCAL               | 受信 | 900004          |
| INFO                 | 受信 | 900005          |
| CONTINUOUSNUMBER     | 受信 | 900006          |

> [!NOTE]
> 上記の表にあるように、正しいカスタム フィールド名を指定することが重要です。 カスタム フィールド名が正確でない場合、領収書のデータが失われます。

### <a name="configure-receipt-formats"></a>領収書形式を設定する

必要な領収書形式ごとに、**印刷動作** フィールドを **常に印刷** にします。

領収書の形式デザイナーで、次のカスタム フィールドを適切な領収書セクションに追加します。 フィールド名は、前のセクションで定義した言語テキストに対応していることに注意してください。

- **ヘッダー:** 次のフィールドを追加します。

    - **店舗名** と **税 ID 番号** フィールド。領収書に会社名と ID 番号を印刷する際に使用します。 または、会社名と ID 番号を自由形式のテキストとしてレイアウトに追加できます。
    - **店舗住所**、**日付**、**時刻 24H**、**受領番号**、**登録番号**。
    - **シーケンス番号**: このフィールドは会計登録サービスで現金トランザクションの件数を特定します。

- **明細行:** 次のフィールドを追加します。

    - **品目名**
    - **数量**
    - **税込合計価格**

- **フッター:** 次のフィールドを追加します。

    - 支払フィールド。支払方法ごとに支払金額を印刷します。 たとえば、**支払名** と **支払金額** のフィールドをレイアウトの 1 行に追加します。
    - **ID provozovny/pokladny**: このフィールドには事業所とレジ機器の識別子を印刷します。
    - **BKP**: このフィールドには、会計登録サービスが割り当てた納税者セキュリティ コードを印刷します。
    - **FIK**: このフィールドには、オンライン登録が成功した場合に税所轄官庁の Web サービスが割り当てたトランザクションの会計識別コードを印刷します。
    - **PKP**: このフィールドには、オフライン登録の場合に会計登録サービスが生成する納税者の署名コードを印刷します。
    - **Info**: このフィールドには、会計登録サービスによる追加情報を印刷します。

領収書形式の使用方法の詳細については、[領収書形式の設定とデザイン](../receipt-templates-printing.md)を参照してください。

## <a name="set-up-fiscal-integration-for-the-czech-republic"></a>チェコ共和国の財政統合を設定する

チェコ共和国の会計登録サービス統合サンプルは、[会計統合機能](fiscal-integration-for-retail-channel.md) に基づいており、Retail SDK に含まれています。 サンプルは [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) リポジトリの **src\\FiscalIntegration\\Efr** フォルダにあります (例: [release/9.33 のサンプル](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)) サンプルは、Commerce Runtime (CRT) の拡張である会計ドキュメント プロバイダーと、Commerce ハードウェア ステーションの拡張である会計コネクタで [構成されています](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)。 Retail SDK の使用方法の詳細については [Retail SDK のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) と [独立したパッケージ SDK のビルド パイプラインを設定する](../dev-itpro/build-pipeline.md) を参照してください。

> [!WARNING]
> [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、この会計統合サンプルでは使用できません。 Microsoft Dynamics Lifecycle Services (LCS) の開発者仮想マシン (VM) で、Retail SDK の以前のバージョンを使用する必要があります。 詳細については、[チェコ共和国向け会計統合サンプルの展開ガイドライン (レガシ)](emea-cze-fi-sample-sdk.md) を参照してください。
>
> 今後のバージョンで、会計統合サンプルの新しい独立したパッケージと拡張モデルのサポートを計画しています。

[Commerce チャンネルの会計統合を設定する](setting-up-fiscal-integration-for-retail-channel.md) で説明されている会計統合の設定手順を実行します。

1. [会計登録プロセスの設定](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process)。 また、[今回の会計登録サービス統合サンプルに固有](#set-up-the-registration-process)の会計登録処理の設定をメモしておきます。
1. [エラーの処理の設定](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings)。
1. [延期された会計登録の手動実行を可能にする](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration)。
1. [チャネル コンポーネントの構成](#configure-channel-components)。

### <a name="set-up-the-registration-process"></a>登録プロセスの設定

登録プロセスを有効化する場合は、次の手順に従って Commerce Headquarters を設定します。 詳細情報については、[コマース チャネルの会計統合の設定](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) を参照してください。

1. 会計ドキュメント プロバイダーと会計コネクタの構成ファイルをダウンロードします。

    1. [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) レポジトリ を開きます。
    1. SDK/アプリケーションのバージョンに応じた適切なリリース ブランチ バージョンを選択します (例: **[リリース/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**)。
    1. **src \> FiscalIntegration \> Efr** を開きます。
    1. **Configurations \> DocumentProviders \> DocumentProviderFiscalEFRSampleCzech.xml** で会計ドキュメント プロバイダー構成ファイルをダウンロードします (例: [リリース/9.33 のファイル](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleCzech.xml))。
    1. **Configurations \> Connectors \> ConnectorEFRSample.xml** から会計コネクタ構成ファイルをダウンロードします (例: [リリース/9.33 のファイル](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml))。

    > [!WARNING]
    > [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、この会計統合サンプルでは使用できません。 LCS の開発者 VM では以前のバージョンの Retail SDK を使用する必要があります。 この会計統合サンプルの構成ファイルは、LCS の開発者 VM 上の Retail SDK が含む次のフォルダーに存在します。
    >
    > - **会計ドキュメント プロバイダ構成ファイル:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration\\DocumentProviderFiscalEFRSampleCzech.xml
    > - **会計コネクタ構成ファイル:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration\\ConnectorEFRSample.xml
    > 
    > 今後のバージョンで、会計統合サンプルの新しい独立したパッケージと拡張モデルのサポートを計画しています。

1. **Retail とコマース \> 本社の設定 \> パラメーター \> コマース共有パラメーター** の順に移動します。 **一般** タブで、**会計統合の有効化** オプションを **はい** に設定します。
1. **Retail と Commerce \> チャネル設定 \> 会計統合 \> 会計ドキュメント プロバイダー** に移動し、先ほどダウンロードした会計ドキュメント プロバイダー コンフィギュレーション ファイルを読み込みます。
1. **Retail と Commerce \> チャネル設定 \> 会計統合 \> 会計コネクタ** に移動し、先ほどダウンロードした会計コネクタ コンフィギュレーション ファイルを読み込みます。
1. **Retail と Commerce \> チャネル設定 \> 会計統合 \> コネクタ機能プロファイル** の順に移動します。 新しいコネクタ機能プロファイルを作成します。 以前に読み込んだドキュメント プロバイダーとコネクタを選択します。 必要に応じて [データ マッピング設定](#default-data-mapping) を更新します。
1. **Retail とコマース \> チャネル設定 \> 会計統合 \> コネクタ技術プロファイル** の順に移動します。 新しいコネクタ テクニカル プロファイルを作成し、先に読み込んだ会計コネクタを選択します。 必要に応じて [コネクタの設定](#fiscal-connector-settings) を更新します。
1. **Retail と Commerc \> チャネル設定 \> 会計統合 \> 会計コネクタ グループ** の順に移動します。 以前に作成したコネクタ機能プロファイルに、新しい会計コネクタ グループを作成します。
1. **Retail と Commerce \> チャネル設定 \> 会計統合 \> 会計登録プロセス** の順に移動します。 新しい会計登録プロセスと会計登録プロセス ステップを作成し、以前に作成した会計コネクタ グループを選択します。
1. **Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> 機能プロファイル** の順に移動します。 登録プロセスを有効化する、店舗にリンクされている機能プロファイルを選択します。 **会計登録プロセス** クイックタブで、以前に作成した会計登録プロセスを選択します。
1. **Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> ハードウェア プロファイル** の順に移動します。 会計プリンターの接続先のハードウェア ステーションにリンクされているハードウェア プロファイルを選択します。 **会計周辺機器** クイックタブで、先ほど作成したコネクタ テクニカル プロファイルを選択します。
1. 配布スケジュール (**Retail と Commerce \> Retail と Commerce IT \> 配送スケジュール**) を開き、ジョブ **1070** と **1090** を選択してチャネル データベースにデータを転送します。

#### <a name="default-data-mapping"></a>既定のデータ マッピング

次の既定のデータ マッピングは、会計統合サンプルの一部として提供される会計ドキュメント プロバイダー構成に含まれています。

- **付加価値税 (VAT) 税率マッピング** – 税率値のマッピング。会計サービスに送信する要求の **TaxG** (税グループ) 属性の値に対する消費税コードに対して設定します。 既定のマッピングを次に示します。

    ```
    A: 21.00; B: 15.00; C: 10.00; Z: 0.00
    ```

    それぞれのペアの最初のコンポーネントは、EFR 会計登録サービスがサポートする VAT 税グループを表します。 2 番目のコンポーネントは対応する VAT 率を表します。 EFR がチェコ共和国でサポートする VAT 税グループの詳細については、[EFR のリファレンス](https://public.efsta.net/efr/) をご覧ください。

- **既定の VAT グループ マッピング** – 事前に決定した VAT グループの 1 つにマッピングできない VAT 金額は、既定の (基本) VAT グループに帰属します。 既定のマッピングを次に示します。

    ```
    A
    ```

- **前金 VAT グループ マッピング** – 顧客前金額と顧客注文前金額は、前金 VAT グループに帰属します。 既定のマッピングを次に示します。

    ```
    Z
    ```

#### <a name="fiscal-connector-settings"></a>会計コネクタの設定

次の設定は、会計統合サンプルの一部として提供される会計コネクタ構成に含まれています。

- **エンドポイント アドレス** – 会計登録サービスの URL。
- **タイムアウト** – ミリ秒単位で表した時間。会計コネクタは会計登録サービスからの応答を待機します。

### <a name="configure-channel-components"></a>チャネル コンポーネントの構成

> [!WARNING]
> [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、この会計統合サンプルでは使用できません。 LCS の開発者 VM では以前のバージョンの Retail SDK を使用する必要があります。 詳細については、[チェコ共和国向け会計統合サンプルの展開ガイドライン (レガシ)](emea-cze-fi-sample-sdk.md) を参照してください。
>
> 今後のバージョンで、会計統合サンプルの新しい独立したパッケージと拡張モデルのサポートを計画しています。

#### <a name="set-up-the-development-environment"></a>開発環境の設定

開発環境を設定してサンプルのテストと拡張を行う際は、次の手順に従います。

1. [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions) リポジトリをクローンまたはダウンロードします。 SDK/アプリケーションのバージョンに応じた適切なリリース ブランチ バージョンを選択します。 詳細については、[GitHub と NuGet から Retail SDK サンプルと参照パッケージをダウンロードする](../dev-itpro/retail-sdk/sdk-github.md) を参照してください。
1. **Dynamics365Commerce.Solutions\\FiscalIntegration\\Efr\\EFR.sln** で EFR ソリューションを開き、ビルドします。
1. CRT 拡張機能をインストールします:

    1. CRT 拡張機能のインストーラを見つけます。

        - **Commerce Scale Unit:** **Efr\\ScaleUnit\\ScaleUnit.EFR.Installer\\bin\\Debug\\net461** folder, find the **ScaleUnit.EFR.Installer** インストーラーを見つけます。
        - **Modern POS 上のローカル CRT:** **Efr\\ModernPOS\\ModernPOS.EFR.Installer\\bin\\Debug\\net461** フォルダ内で、**ModernPOS.EFR.Installer** インストーラーを見つけます。

    1. コマンド ラインから CRT 拡張機能インストーラーを起動します。

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **最新 POS のローカル CRT:**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. 会計コネクタ拡張機能のインストール:

    [ハードウェア ステーション](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) または [POS レジスター](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network) で会計コネクタ拡張機能をインストールにできます。

    1. ハードウェア ステーション拡張機能をインストールする。

        1. **Efr\\HardwareStation\\HardwareStation.EFR.Installer\\bin\\Debug\\net461** フォルダーで **HardwareStation.EFR.Installer** インストーラーを見つけます。
        1. 次のコマンドを実行してるコマンド ラインから拡張機能インストーラーを起動します。

            ```Console
            HardwareStation.EFR.Installer.exe install --verbosity 0
            ```

    1. POS 拡張機能をインストールします:

        1. **Dynamics365Commerce.Solutions\\FiscalIntegration\\PosFiscalConnectorSample\\Contoso.PosFiscalConnectorSample.sln** でPOS 会計コネクタ サンプル ソリューションを開き、それを構築します。
        1. **PosFiscalConnectorSample\\StoreCommerce.Installer\\bin\\Debug\\net461** フォルダで、**Contoso.PosFiscalConnectorSample.StoreCommerce.Installer** インストーラーを探します。
        1. 次のコマンドを実行してるコマンド ラインから拡張機能インストーラーを起動します。

            ```Console
            Contoso.PosFiscalConnectorSample.StoreCommerce.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>運用環境

[会計統合サンプルのビルド パイプラインを設定する](fiscal-integration-sample-build-pipeline.md) の手順に従って、会計統合サンプルの Cloud Scale Unit とセルフサービスの展開可能なパッケージを生成し、リリースします。 **EFR build-pipeline.yml** テンプレートの YAML ファイルは、[Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions) リポジトリの **Pipeline\\YAML_Files** フォルダーに存在します。

## <a name="design-of-extensions"></a>拡張機能の設計

チェコ共和国の会計登録サービス統合サンプルは、[会計統合機能](fiscal-integration-for-retail-channel.md) に基づいており、Retail SDK に含まれています。 サンプルは [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) リポジトリの **src\\FiscalIntegration\\Efr** フォルダにあります (例: [release/9.33 のサンプル](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)) サンプルは、CRT の拡張である会計ドキュメント プロバイダーと、Commerce ハードウェア ステーションの拡張である会計コネクタで [構成されています](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)。 Retail SDK の使用方法の詳細については [Retail SDK のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) と [独立したパッケージ SDK のビルド パイプラインを設定する](../dev-itpro/build-pipeline.md) を参照してください。

> [!WARNING]
> [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、この会計統合サンプルでは使用できません。 LCS の開発者 VM では以前のバージョンの Retail SDK を使用する必要があります。 詳細については、[チェコ共和国向け会計統合サンプルの展開ガイドライン (レガシ)](emea-cze-fi-sample-sdk.md) を参照してください。 今後のバージョンで、会計統合サンプルの新しい独立したパッケージと拡張モデルのサポートを計画しています。

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime 拡張機能の設計

会計ドキュメント プロバイダーである拡張機能の目的は、サービスに特化したドキュメントを生成して会計登録サービスからの応答を処理することです。

#### <a name="request-handler"></a>要求ハンドラー

ドキュメント プロバイダーが使用する単一の **DocumentProviderEFRFiscalCZE** 要求ハンドラーがあり、これを使用して会計登録サービスの会計ドキュメントを生成します。

このハンドラは **INamedRequestHandler** インターフェイスから継承します。 **HandlerName** メソッドの機能がハンドラーの名前を返します。 このハンドラー名は、Commerce headquarters で指定したコネクタ ドキュメント プロバイダーの名前と一致する必要があります。

このコネクタは次の要求をサポートします。

- **GetFiscalDocumentDocumentProviderRequest** – この要求は生成するべきドキュメントに関する情報を含みます。 これは会計登録サービスに登録するべきサービス固有のドキュメントを返します。
- **GetSupportedRegistrableEventsDocumentProviderRequest** – この要求はサブスクライブするイベントのリストを返します。 現在サポートするのは次のイベントです: 販売、顧客前金口座、顧客手付金。
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – この要求は会計登録サービスによる応答を返します。 この応答は保存できるように文字列形式にシリアル化されます。

#### <a name="configuration"></a>構成

会計ドキュメント プロバイダーの構成ファイルは、[Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) レポジトリの **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders\\DocumentProviderFiscalEFRSampleCzech.xml** にあります。 このファイルによって、Commerce Headquarters から会計ドキュメント プロバイダーの設定を構成できるようになります。 ファイル形式は会計統合構成の要件に従います。

### <a name="hardware-station-extension-design"></a>ハードウェア ステーション拡張機能の設計

会計コネクタである拡張機能によって、会計登録サービスと通信できます。 ハードウェア ステーション拡張機能は HTTP プロトコルを使用し、CRT 拡張機能が生成するドキュメントを会計登録サービスに送信します。 また、会計登録サービスから受信した応答も処理します。

#### <a name="request-handler"></a>要求ハンドラー

**EFRHandler** 要求ハンドラーは、会計登録サービスへの要求を処理するエントリ ポイントです。

ハンドラは **INamedRequestHandler** インターフェイスから継承します。 **HandlerName** メソッドの機能がハンドラーの名前を返します。 このハンドラー名は、Commerce headquarters で指定した会計コネクタの名前と一致する必要があります。

このコネクタは次の要求をサポートします。

- **SubmitDocumentFiscalDeviceRequest** – この要求はドキュメントを会計登録サービスに送信し、その応答を返します。
- **IsReadyFiscalDeviceRequest** – この要求は会計登録サービスの正常性確認に使用します。
- **InitializeFiscalDeviceRequest** – この要求は会計登録サービスの初期化に使用します。

#### <a name="configuration"></a>構成

会計コネクタの構成ファイルは、[Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) リポジトリの **src\\FiscalIntegration\\Efr\\Configurations\\Connectors\\ConnectorEFRSample.xml** に存在します。 このファイルによって、Commerce Headquarters から会計コネクタの設定を構成できるようになります。 ファイル形式は会計統合構成の要件に従います。

### <a name="pos-fiscal-connector-extension-design"></a>POS 会計コネクタ拡張機能の設計

POS 会計コネクタ拡張機能の目的は、POS からの会計登録サービスと通信することです。 これは通信に HTTPS プロトコルを使用します。

#### <a name="fiscal-connector-factory"></a>会計コネクタ ファクトリー

会計コネクタ ファクトリーは、コネクタ名を会計コネクタの実装にマップし、これは  **Pos.Extension\\Connectors\\FiscalConnectorFactory.ts** ファイルにあります。 このコネクタ名は、Commerce 本部で指定した会計コネクタの名前と一致する必要があります。

#### <a name="efr-fiscal-connector"></a>EFR 会計コネクタ

EFR 会計コネクタは **Pos.Extension\\Connectors\\Efr\\EfrFiscalConnector.ts** ファイルにあります。 これは、次の要求をサポートする **IFiscalConnector** インターフェイスを実装します。

- **FiscalRegisterSubmitDocumentClientRequest** – この要求はドキュメントを会計登録サービスに送信し、その応答を返します。
- **FiscalRegisterIsReadyClientRequest** – この要求は会計登録サービスの正常性確認に使用します。
- **FiscalRegisterInitializeClientRequest** – この要求は会計登録サービスの初期化に使用します。

#### <a name="configuration"></a>構成

この構成ファイルは、[Dynamics 365 Commerce ソリュション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) リポジトリの **src\\FiscalIntegration\\Efr\\Configurations\\Connectors** フォルダーにあります。 このファイルによって、Commerce Headquarters から会計コネクタの設定を構成できるようになります。 ファイル形式は会計統合構成の要件に従います。 以下の設定を追加します:

- **エンドポイント アドレス** – 会計登録サービスの URL。
- **タイムアウト** – ミリ秒単位 (ms) で表した時間。このコネクタは会計登録サービスからの応答を待機します。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
