---
title: オーストリア向け会計登録サービス統合のサンプル
description: このトピックでは、Microsoft Dynamics 365 Commerce のオーストリア向け会計統合サンプルの概要について説明します。
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 826c1cb0fba7025b16dadbfa6157683392945103
ms.sourcegitcommit: 7faf82fa7ce269c0201abb8473af861ef7ce00bf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/19/2022
ms.locfileid: "8614154"
---
# <a name="fiscal-registration-service-integration-sample-for-austria"></a>オーストリア向け会計登録サービス統合のサンプル

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce のオーストリア向け会計統合サンプルの概要について説明します。

オーストリアのキャッシュ レジスターにおける現地の財政要件を満たすため、オーストリア向け Dynamics 365 Retail 機能には、販売時点管理 (POS) と外部財政登録サービスとの統合例が含まれています。 このサンプルは [会計統合機能](fiscal-integration-for-retail-channel.md) を拡張します。 これは [EFSTA](https://www.efsta.eu/at/) の [EFR (電子会計登録)](https://www.efsta.eu/at/fiskalloesungen/oesterreich) ソリューションに基づいており、HTTPS プロトコルによる EFR サービスとの通信を実現します。 Retail ハードウェア ステーション、またはハードウェア ステーションから接続できる別のマシンのいずれかで、EFR サービスをホストする必要があります。 このサンプルはソース コード形式で提供され、Retail ソフトウェア開発キット (SDK) に含まれます。

マイクロソフトは、EFSTA によるハードウェア、ソフトウェア、ドキュメントをリリースしません。 EFR ソリューションを入手して操作する方法については [EFSTA](https://www.efsta.eu/at/kontakt) に問い合わせてください。

## <a name="scenarios"></a>シナリオ

オーストリア向けの会計登録サービス統合サンプルでは、以下のシナリオをカバーしています:

- 会計登録サービスへの現金トランザクションの登録:

    - 詳細なトランザクション データを会計登録サービスに送信します。 このデータは、販売明細行情報、割引、支払い、税金に関する情報を含みます。
    - 会計登録サービスからの応答を取得します。 この応答は、デジタル署名と登録済みのトランザクションへのリンクを含みます。
    - 税を登録して、会計登録サービスの税コードにマッピングします。
    - 登録したトランザクションの QR コードを領収書に印刷します。

- 会計登録サービスでの非現金トランザクションとして、ギフト カードの操作と顧客前金の登録を行う。

    - ギフト カードの発行や入金を行います。
    - 顧客前金口座を登録します。
    - 顧客手付金を登録します。

- 会計登録サービスでの非現金トランザクションとして、販売以外のトランザクションとイベントの登録を行う。

    - シフトを開き、シフトを閉じる
    - 開始金額、フロート エントリ、支払/入金の削除
    - 価格変更
    - 税の上書き
    - 受領書のコピーの印刷
    - ドロワーを開く
    - X レポートの印刷
    - Z レポートの印刷

- オーストリア固有のフィールドを持つ、営業終了時の明細書 (X/Z レポート) の印刷。

    - 顧客に配送した製品やサービスの総数
    - 税率ごとの売上内訳
    - レジ担当者ごとの支払内訳
    - 毎日の売上を減らす価格割引と返品
    - 売上ゼロ (景品)

- 次のオプションなど、エラー処理。

    - 会計登録サービスが利用できない場合、準備ができていない場合、応答していない場合など、再試行できるときは会計登録をやり直します。
    - 会計登録の延期。
    - 会計登録をスキップするか、またはトランザクションを登録済みとしてマークして、失敗した理由と追加情報を取得するための情報コードを含めます。
    - 新しい販売トランザクションの開始時や販売トランザクション確定時に、会計登録サービスの使用可能性を確認します。

### <a name="gift-cards"></a>ギフト カード

会計登録サービス統合サンプルでは、ギフト カードに関連する以下のルールを実装しています:

- *ギフトカードの発行* と *ギフトカード* への追加の操作に関連する販売明細行を現金トランザクションから除外します。 これらの明細行を現金トランザクションの一部として登録せずに、それらを個別の非現金トランザクションとして会計登録サービスに登録します。
- 領収書をギフト カード明細行でのみ構成している場合、領収書に税グループの内訳と QR コードを印刷しません。
- トランザクションで発行や際チャージを行ったギフト カードの合計金額を、現金取引金額とは別に領収書に印刷します。
- 対応する会計トランザクションを参照して、支払明細行の計算した調整をチャネル データベースに保存します。
- ギフト カードによる支払を通常の支払と見なします。

### <a name="customer-deposits-and-customer-order-deposits"></a>顧客前金と顧客手付金

会計登録サービス統合サンプルでは、顧客前金と顧客注文前金に関連した以下のルールを実装しています:

- トランザクションが顧客前金である場合に、非現金トランザクションを登録します。
- トランザクションに顧客注文の前金や顧客注文の前金の払い戻しのみが含まれている場合は、非現金トランザクションを登録します。
- ハイブリッド顧客注文の作成時に、支払明細行から顧客手付金を差し引きます。
- ハイブリッド顧客注文の会計トランザクションを参照して、支払明細行の計算した調整をチャネル データベースに保存します。

### <a name="limitations-of-the-sample"></a>サンプルの制限事項

会計登録サービスは、消費税が価格に含まれているシナリオのみをサポートします。 したがって、**税込価格** オプションは、店舗と顧客の両方で **はい** に設定する必要があります。

## <a name="set-up-commerce-for-austria"></a>オーストリア向け Commerce を設定する

このセクションでは、オーストリアに固有で推奨される Commerce 設定について説明します。 詳細な設定情報については、[Commerce のホーム ページ](../index.md) を参照してください。

オーストリアに固有の機能を使用する際は、次の設定を指定してください。

- 法人の基本住所で、**国/地域** フィールドを **AUT** (オーストリア) に設定します。
- オーストリアにあるすべての店舗の POS 機能プロファイルで、 **ISO コード フィールド** を **AT** (オーストリア) に設定します。

オーストリアに対応する次の設定を指定する必要があります。 設定が完了したら、必ず適切な配布ジョブを実行します。

### <a name="set-up-vat-per-austrian-requirements"></a>オーストリアの要件に従って VAT を設定する

消費税コード、消費税グループ、品目の消費税グループを作成する必要があります。 また、製品やサービスの消費税情報を設定する必要があります。 消費税機能の設定と使用方法の詳細については、[消費税の概要](../../finance/general-ledger/indirect-taxes-overview.md)を参照してください。

消費税コードの省略コードを領収書に印刷できます (例: "A" や "B")。 この機能の使用を有効化する場合は、**消費税コード** ページで **印刷コード** フィールドを設定します。

### <a name="set-up-stores"></a>店舗を設定する

**すべての店舗** ページで店舗の詳細を更新します。 具体的には、次のパラメーターを設定する必要があります:

- **消費税グループ** フィールドで、既定の顧客への販売に使用するべき消費税グループを指定します。
- **税込価格** オプションに **はい** をセットします。
- **名前** フィールドに会社名を設定します。 この変更により、会社名が領収書に確実に表示されます。 または、会社名を自由形式のテキストとして領収書のレイアウトに追加できます。
- **税 ID 番号 (TIN)** フィールドに会社識別番号を設定します。 この変更により、会社の ID 番号が領収書に確実に表示されます。 または、会社 ID 番号を自由形式のテキストとして領収書のレイアウトに追加できます。

### <a name="set-up-functionality-profiles"></a>機能プロファイルを設定する

POS 機能プロファイルを設定する

- **領収書番号** ファストタブ で、**販売**、**販売注文**、**返品** の領収書トランザクション タイプに対してレコードの作成や更新を行い、領収書番号を設定します。

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>カスタム フィールドを設定して、販売領収書の領収書形式で使用できるようにする

POS 領収書形式で使用される言語テキストおよびカスタム フィールドを構成することができます。 領収書設定を作成するユーザーの既定の会社は、言語テキスト設定が作成された法人と同じである必要があります。 または、ユーザーの既定の会社、および設定の作成対象の店舗の法人の両方で、同じ言語テキストを作成する必要があります。

**言語テキスト** ページで、領収書 レイアウト用のカスタム フィールドのラベルに次のレコードを追加します。 テーブルに表示されている **言語 ID**、**テキスト ID**、および **テキスト** の値は、単なる例に過ぎません。 要件に合わせてそれらを変更できます。 ただし、使用する **テキスト ID** の値は一意である必要があり、900001 以上である必要があります。

テーブルの **言語テキスト** が含む **POS** セクションに、次の POS ラベルを追加します。

| 言語 ID | テキスト ID | テキスト                      |
|-------------|---------|---------------------------|
| ja       | 900001  | QR コード                   |
| ja       | 900002  | 連続する番号         |
| ja       | 900003  | 税小売印刷コード     |
| ja       | 900004  | 合計 (販売)             |
| ja       | 900005  | 税合計 (売上)         |
| ja       | 900006  | 税込価格 (売上) |
| ja       | 900007  | 税額 (売上)        |
| ja       | 900008  | 課税基準 (売上)         |

**カスタム フィールド** ページで、領収書 レイアウトのカスタム フィールドに次のレコードを追加します。 **キャプション テキスト ID** の値は、**言語テキスト** ページで指定した **テキスト ID** の値に対応している必要があることに注意してください。

| Name                 | 種類    | キャプション テキスト ID |
|----------------------|---------|-----------------|
| QRCODE               | 受信 | 900001          |
| CONTINUOUSNUMBER     | 受信 | 900002          |
| RETAILPRINTCODE      | 受信 | 900003          |
| SALESTOTAL           | 受信 | 900004          |
| SALESTOTALTAX        | 受信 | 900005          |
| SALESTOTALINCLUDETAX | 受信 | 900006          |
| SALESTAXAMOUNT       | 受信 | 900007          |
| SALESTAXBASIS        | 受信 | 900008          |

> [!NOTE]
> 上記の表にあるように、正しいカスタム フィールド名を指定することが重要です。 カスタム フィールド名が正確でない場合、領収書のデータが失われます。

### <a name="configure-receipt-formats"></a>領収書形式を設定する

必要な領収書形式ごとに、**印刷動作** フィールドを **常に印刷** にします。

領収書の形式デザイナーで、次のカスタム フィールドを適切な領収書セクションに追加します。 フィールド名は、前のセクションで定義した言語テキストに対応していることに注意してください。

- **ヘッダー:** 次のフィールドを追加します。

    - **店舗名** と **税 ID 番号** フィールド。領収書に会社名と ID 番号を印刷する際に使用します。 または、会社名と ID 番号を自由形式のテキストとしてレイアウトに追加できます。
    - **店舗住所**、**日付**、**時刻 24H**、**受領番号**、**登録番号** フィールド。
    - **連続する番号** フィールド。会計登録サービスで現金トランザクションの件数を特定します。

- **明細行:** 次のフィールドを追加します。

    - **品目名**。
    - **数量/単位**。
    - **税込合計価格**。
    - **税小売印刷コード**。品目に適用する消費税コードに対応した、省略コードの印刷に使用します。

- **フッター:** 次のフィールドを追加します。

    - 支払フィールド。支払方法ごとに支払金額を印刷します。 たとえば、**支払名** と **支払金額** のフィールドをレイアウトの 1 行に追加します。
    - **売上合計** フィールド グループ。

        - **合計 (売上)** フィールド。領収書の現金販売合計額の印刷に使用します。 税抜金額。 前払いとギフト カードの操作は除きます。
        - **税込合計 (売上)** フィールド。領収書の現金販売合計額の印刷に使用します。 税込金額。 前払いとギフト カードの操作は除きます。
        - **税込合計 (売上)** フィールド。領収書の現金販売合計税額の印刷に使用します。 前払いとギフト カードの操作は除きます。

    - **税内訳** フィールド グループ。 このフィールド グループが含むすべてのフィールドは、個別の 1 行に印刷する必要があります。

        - **税 ID** フィールド。消費税コードごとに消費税の概要を印刷できるようにする標準フィールド。 このフィールドは新しい行に追加する必要があります。
        - **税率** フィールド。消費税コードの実効税率の印刷に使用する標準フィールド。
        - **課税基準 (売上)** フィールド。消費税コードに対する領収書の現金販売合計額の印刷に使用します。 前払いとギフト カードの操作は除きます。
        - **税額 (売上)** フィールド。消費税コードに対する現金販売の、領収書の税額を印刷するために使用します。
        - **税小売印刷コード** フィールド。消費税コードに対応した省略コードの印刷に使用します。

    - **QR コード** フィールド。登録した現金トランザクションの参照を QR コード形式で印刷するために使用します。

        > [!NOTE]
        > **QR Code** 値は会計レジスターの応答から取得します。 EFR 構成の **属性** フィールドの値を EFSTA ドキュメントに記載する場合のみ、EFR は応答で QR コードを返します。 EFR 構成の **属性** フィールドの QR コード形式は **BMP** に設定する必要があります。

領収書形式の使用方法の詳細については、[領収書形式の設定とデザイン](../receipt-templates-printing.md)を参照してください。

## <a name="set-up-fiscal-integration-for-austria"></a>オーストリア向け会計統合を設定する

オーストリアの会計登録サービス統合サンプルは、[会計統合機能](fiscal-integration-for-retail-channel.md) に基づいており、Retail SDK に含まれています。 サンプルは [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) リポジトリの **src\\FiscalIntegration\\Efr** フォルダにあります (例: [release/9.33 のサンプル](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)) サンプルは、Commerce Runtime (CRT) の拡張である会計ドキュメント プロバイダーと、Commerce ハードウェア ステーションの拡張である会計コネクタで [構成されています](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)。 Retail SDK の使用方法の詳細については [Retail SDK のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) と [独立したパッケージ SDK のビルド パイプラインを設定する](../dev-itpro/build-pipeline.md) を参照してください。

> [!WARNING]
> [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、この会計統合サンプルでは使用できません。 Microsoft Dynamics Lifecycle Services (LCS) の開発者仮想マシン (VM) で、Retail SDK の以前のバージョンを使用する必要があります。 詳細については、[オーストリア向け会計統合サンプルの展開ガイドライン (レガシ)](emea-aut-fi-sample-sdk.md) を参照してください。 今後のバージョンで、会計統合サンプルの新しい独立したパッケージと拡張モデルのサポートを計画しています。

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
    1. **Configurations \> DocumentProviders** を開き、次の会計ドキュメント プロバイダー構成ファイルをダウンロードします: **DocumentProviderFiscalEFRSampleAustria.xml** と **DocumentProviderNonFiscalEFRSampleAustria.xml** (例: [リリースするファイルの場所/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders))。
    1. **Configurations \> Connectors \> ConnectorEFRSample.xml** から会計コネクタ構成ファイルをダウンロードします (例: [リリース/9.33 のファイル](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml))。

    > [!WARNING]
    > [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、この会計統合サンプルでは使用できません。 LCS の開発者 VM では以前のバージョンの Retail SDK を使用する必要があります。 この会計統合サンプルの構成ファイルは、LCS の開発者 VM 上の Retail SDK が含む次のフォルダーに存在します。
    >
    > - **会計ドキュメント プロバイダー構成ファイル:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration
    > - **会計コネクタ構成ファイル:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration
    > 
    > 今後のバージョンで、会計統合サンプルの新しい独立したパッケージと拡張モデルのサポートを計画しています。

1. **Retail とコマース \> 本社の設定 \> パラメーター \> コマース共有パラメーター** の順に移動します。 **一般** タブで、**会計統合の有効化** オプションを **はい** に設定します。
1. **Retail と Commerce \> チャネル設定 \> 会計統合 \> 会計ドキュメント プロバイダー** に移動し、先ほどダウンロードした会計ドキュメント プロバイダー コンフィギュレーション ファイルを読み込みます。
1. **Retail と Commerce \> チャネル設定 \> 会計統合 \> 会計コネクタ** に移動し、先ほどダウンロードした会計コネクタ コンフィギュレーション ファイルを読み込みます。
1. **Retail と Commerce \> チャネル設定 \> 会計統合 \> コネクタ機能プロファイル** の順に移動します。 以前に読み込んだ会計ドキュメント プロバイダーごとに 1 つずつ、新しいコネクタ機能プロファイルを 2 つ作成し、以前に読み込んだ会計コネクタを選択します。 必要に応じて [データ マッピング設定](#default-data-mapping) を更新します。
1. **Retail とコマース \> チャネル設定 \> 会計統合 \> コネクタ技術プロファイル** の順に移動します。 新しいコネクタ テクニカル プロファイルを作成し、先に読み込んだ会計コネクタを選択します。 必要に応じて [コネクタの設定](#fiscal-connector-settings) を更新します。
1. **Retail と Commerc \> チャネル設定 \> 会計統合 \> 会計コネクタ グループ** の順に移動します。 既に作成した各コネクタ機能プロファイル用に 2 つの新しい会計コネクタ グループを作成します。
1. **Retail と Commerce \> チャネル設定 \> 会計統合 \> 会計登録プロセス** の順に移動します。 新しい会計登録プロセスと会計登録プロセス ステップを 2 つ作成し、以前に作成した会計コネクタ グループを選択します。
1. **Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> 機能プロファイル** の順に移動します。 登録プロセスを有効化する、店舗にリンクされている機能プロファイルを選択します。 **会計登録プロセス** クイックタブで、以前に作成した会計登録プロセスを選択します。 POS で非会計イベントの登録を有効化する際は、**機能** クイック タブの **POS** 配下で、**監査** オプションに **はい** と設定します。
1. **Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> ハードウェア プロファイル** の順に移動します。 会計プリンターの接続先のハードウェア ステーションにリンクされているハードウェア プロファイルを選択します。 **会計周辺機器** クイックタブで、先ほど作成したコネクタ テクニカル プロファイルを選択します。
1. 配布スケジュール (**Retail と Commerce \> Retail と Commerce IT \> 配送スケジュール**) を開き、ジョブ **1070** と **1090** を選択してチャネル データベースにデータを転送します。

#### <a name="default-data-mapping"></a>既定のデータ マッピング

次の既定のデータ マッピングは、会計統合サンプルの一部として提供される会計ドキュメント プロバイダー構成に含まれています。

- **付加価値税 (VAT) 税率マッピング** – 税率値のマッピング。会計サービスに送信する要求の **TaxG** (税グループ) 属性の値に対する消費税コードに対して設定します。 既定のマッピングを次に示します。

    ```
    A: 20.00; B: 10.00; C: 13.00; D: 0.00; E: 19.00; F: 7.00
    ```

    それぞれのペアの最初のコンポーネントは、EFR 会計登録サービスがサポートする VAT 税グループを表します。 2 番目のコンポーネントは対応する VAT 率を表します。 EFR がオーストリアでサポートする VAT 税グループの詳細については、[EFR のリファレンス](https://public.efsta.net/efr/) をご覧ください。

#### <a name="fiscal-connector-settings"></a>会計コネクタの設定

次の設定は、会計統合サンプルの一部として提供される会計コネクタ構成に含まれています。

- **エンドポイント アドレス** – 会計登録サービスの URL。
- **デバイスのタイムアウト** – ミリ秒単位で表した時間。会計コネクタは会計登録サービスからの応答を待機します。
- **会計登録通知を表示する** – 会計登録サービスが返す通知をオペレーターに表示するかどうかを、このフラグによって制御します。

### <a name="configure-channel-components"></a>チャネル コンポーネントの構成

> [!WARNING]
> [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、この会計統合サンプルでは使用できません。 LCS の開発者 VM では以前のバージョンの Retail SDK を使用する必要があります。 詳細については、[オーストリア向け会計統合サンプルの展開ガイドライン (レガシ)](emea-aut-fi-sample-sdk.md) を参照してください。
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

#### <a name="production-environment"></a>実稼働環境

[会計統合サンプルのビルド パイプラインを設定する](fiscal-integration-sample-build-pipeline.md) の手順に従って、会計統合サンプルの Cloud Scale Unit とセルフサービスの展開可能なパッケージを生成し、リリースします。 **EFR build-pipeline.yml** テンプレートの YAML ファイルは、[Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions) リポジトリの **Pipeline\\YAML_Files** フォルダーに存在します。

## <a name="design-of-extensions"></a>拡張機能の設計

オーストリアの会計登録サービス統合サンプルは、[会計統合機能](fiscal-integration-for-retail-channel.md) に基づいており、Retail SDK に含まれています。 サンプルは [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) リポジトリの **src\\FiscalIntegration\\Efr** フォルダにあります (例: [release/9.33 のサンプル](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)) サンプルは、CRT の拡張である会計ドキュメント プロバイダーと、Commerce ハードウェア ステーションの拡張である会計コネクタで [構成されています](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)。 Retail SDK の使用方法の詳細については [Retail SDK のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) と [独立したパッケージ SDK のビルド パイプラインを設定する](../dev-itpro/build-pipeline.md) を参照してください。

> [!WARNING]
> [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、この会計統合サンプルでは使用できません。 LCS の開発者 VM では以前のバージョンの Retail SDK を使用する必要があります。 詳細については、[オーストリア向け会計統合サンプルの展開ガイドライン (レガシ)](emea-aut-fi-sample-sdk.md) を参照してください。 今後のバージョンで、会計統合サンプルの新しい独立したパッケージと拡張モデルのサポートを計画しています。

### <a name="commerce-runtime-extension-design"></a>Commerce Runtime 拡張機能の設計 

会計ドキュメント プロバイダーである拡張機能の目的は、サービスに特化したドキュメントを生成して会計登録サービスからの応答を処理することです。

#### <a name="request-handler"></a>要求ハンドラー

ドキュメント プロバイダーには、次の 2 つの要求ハンドラーがあります。

- **DocumentProviderEFRFiscalAUT** – このハンドラーを使用して会計登録サービスの会計ドキュメントを生成します。
- **DocumentProviderEFRNonFiscalAUT** – このハンドラーを使用して会計登録サービスの非会計ドキュメントを生成します。

これらのハンドラーは **INamedRequestHandler** インターフェイスから継承します。 **HandlerName** メソッドの機能がハンドラーの名前を返します。 このハンドラー名は、Commerce headquarters で指定したコネクタ ドキュメント プロバイダーの名前と一致する必要があります。

このコネクタは次の要求をサポートします。

- **GetFiscalDocumentDocumentProviderRequest** – この要求は生成するべきドキュメントに関する情報を含みます。 これは会計登録サービスに登録するべきサービス固有のドキュメントを返します。
- **GetNonFiscalDocumentDocumentProviderRequest** – この要求は生成するべき非会計ドキュメントに関する情報を含みます。 これは会計登録サービスに登録するべきサービス固有のドキュメントを返します。
- **GetSupportedRegistrableEventsDocumentProviderRequest** – この要求はサブスクライブするイベントのリストを返します。 現在サポートするイベントを次に示します: 販売、X レポートの印刷、Z レポートの印刷、顧客前金口座、顧客手付金、監査イベント、非販売トランザクション。
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – この要求は会計登録サービスによる応答を返します。 この応答は保存できるように文字列形式にシリアル化されます。

#### <a name="configuration"></a>構成

会計ドキュメント プロバイダーの構成ファイルは、[Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) リポジトリの **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders** フォルダーにあります。

- **DocumentProviderFiscalEFRSampleAustria** – 会計ドキュメントの会計ドキュメント プロバイダーの構成ファイル。
- **DocumentProviderNonFiscalEFRSampleAustria** – 非会計ドキュメントの会計ドキュメント プロバイダーの構成ファイル。

これらのファイルによって、Commerce Headquarters から会計ドキュメント プロバイダーの設定を構成できるようになります。 ファイル形式は会計統合構成の要件に従います。

### <a name="hardware-station-extension-design"></a>ハードウェア ステーション拡張機能の設計

会計コネクタ拡張機能の目的は、会計登録サービスと通信することです。 ハードウェア ステーション拡張機能は HTTP プロトコルを使用し、CRT 拡張機能が生成するドキュメントを会計登録サービスに送信します。 また、会計登録サービスから受信した応答も処理します。

#### <a name="request-handler"></a>要求ハンドラー

**EFRHandler** 要求ハンドラーは、会計登録サービスへの要求を処理するエントリ ポイントです。

ハンドラは **INamedRequestHandler** インターフェイスから継承します。 **HandlerName** メソッドの機能がハンドラーの名前を返します。 このハンドラー名は、Commerce headquarters で指定した会計コネクタの名前と一致する必要があります。

この会計コネクタは次の要求をサポートします。

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
