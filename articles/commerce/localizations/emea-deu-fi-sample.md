---
title: ドイツ向け会計登録サービス統合サンプル
description: このトピックでは、Microsoft Dynamics 365 Commerce のドイツ向け会計統合サンプルの概要について説明します。
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2020-5-29
ms.openlocfilehash: 65315a9fd6bc1af26bc225220e096aee4da09be2
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388162"
---
# <a name="fiscal-registration-service-integration-sample-for-germany"></a>ドイツ向け会計登録サービス統合サンプル

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce のドイツ向け会計統合サンプルの概要について説明します。

ドイツのキャッシュ レジスターにおける現地の財政要件を満たすため、ドイツ向け Microsoft Dynamics 365 Commerce 機能には、販売時点管理 (POS) と外部財政登録サービスとの統合例が含まれています。 このサンプルは [会計統合機能](fiscal-integration-for-retail-channel.md) を拡張します。 これは [EFSTA](https://www.efsta.eu/de/) の [EFR (電子会計登録)](https://www.efsta.eu/de/fiskalloesungen/deutschland) ソリューションに基づいており、HTTPS プロトコルによる EFR サービスとの通信を実現します。 Retail ハードウェア ステーション、またはハードウェア ステーションから接続できる別のコンピューターのいずれかで、EFR サービスをホストする必要があります。 このサンプルはソース コード形式で提供され、Retail ソフトウェア開発キット (SDK) に含まれます。

マイクロソフトは、EFSTA によるハードウェア、ソフトウェア、ドキュメントをリリースしません。 EFR ソリューションを入手して操作する方法については [EFSTA](https://www.efsta.eu/de/kontakt/kontakt) に問い合わせてください。

## <a name="scenarios"></a>シナリオ

ドイツ向けの会計登録サービス統合サンプルでは、以下のシナリオをカバーしています:

### <a name="sales-operations"></a>販売操作

- **現金払い販売の登録と、会計登録サービスの戻り値:**

    販売業務の登録は、次の手順を含みます。

    1. トランザクション開始の登録

        各トランザクションの開始は、EFR サービスと連携した技術的セキュリティ要素 (TSE) に登録されます。 登録の結果、TSE はトランザクション ID (TID) を割り当てます。

    2. トランザクション終了の登録

        POS でトランザクションが完了すると、トランザクション開始の登録時に割り当てたものと同じ TID を使用して登録されます。 その時点で、会計登録サービスに詳細なトランザクション データが送信されます。 このデータは、販売明細行情報、割引、支払い、税金に関する情報を含みます。

    3. 会計登録サービスからの応答をキャプチャする

        セキュリティ データを応答の一部として TSE から受信し、チャネル データベースのトランザクションに保存します。 セキュリティ データは次の情報で構成されます。

        - TID
        - トランザクション開始の日時。
        - トランザクション終了の日時。
        - 署名カウンター
        - 確認値
        - TSE のシリアル番号

- **会計登録サービスでの顧客注文の登録:** この登録プロセスは、現金売り販売と返品のプロセスと同じです。
- **ギフト カードと前金を伴う業務の登録:** この登録プロセスは、現金売り販売と返品のプロセスと同じです。

#### <a name="notifying-users-about-fiscal-registration-failures"></a>ユーザーに会計登録の失敗を通知する

会計登録で発生した失敗について、会計登録サービスがユーザーに通知する方法には 2 種類あります。

- 領収書の **情報メッセージ** フィールドの応答から追加情報を印刷します。
- POS のユーザー メッセージとして会計サービスからの通知を表示します。

    > [!NOTE]
    > この通知メカニズムを使用するには、**コネクタ技術プロファイル** ページの **会計登録通知を表示する** パラメーターをオンにする必要があります。

#### <a name="printing-receipts"></a>領収書を印刷する

ドイツでは領収書の印刷が義務付けられています。 すべての領収書には、少なくとも次の情報を含める必要があります。

- 会社の名前と住所
- 価格や数量など、商品に関する情報
- 受け取った支払に関する情報
- 税率ごとの合計金額を含む、税金に関する情報
- セキュリティ データ。

    - TID
    - トランザクション開始の日時。
    - トランザクション終了の日時。
    - 署名カウンター
    - 確認値
    - TSE のシリアル番号

- 情報メッセージ。

> [!NOTE]
> また、領収書には QRコードを印刷できます。 この QR コードはオプションですが、強く推奨します。 会計登録サービスによる応答の一部として QR コードを取得する方法の詳細については、[EFSTA ドキュメント](https://public.efsta.net/efr/) Web サイトで公開されている "EFR ガイド \[DE\]" ドキュメントをご覧ください。
>
> 領収書の **情報メッセージ** フィールドには、会計登録サービスによる通知が表示されます。 たとえば、署名デバイスが壊れている場合は領収書に特別なテキストを印刷できます。

#### <a name="voided-suspended-and-recalled-transactions"></a>無効、一時停止、トランザクションの取り消し

- 無効になったトランザクションは、トランザクション中止の要求として会計登録サービスに登録されます。
- 中止されたトランザクションは、トランザクション中止の要求として会計登録サービスに登録されます。
- 一時停止されたトランザクションの取り消しは、新しいトランザクション開始として会計登録サービスに登録されます。

### <a name="non-sales-transactions-and-shift-closing"></a>非販売トランザクションとシフトのクローズ

以下の非販売トランザクションは、**NFS** タグを使用して、会計登録サービスに非会計操作として登録されます。

- 開始金額の申告
- 釣銭入力
- 支払/入金の削除
- 金庫保管
- 銀行入金
- 収益勘定
- 経費勘定

また、**シフト クローズ** 操作も、**NFS** タグを使用して、会計登録サービスに非会計操作として登録されます。

### <a name="data-export-and-audit"></a>データのインポートと監査

整合性、信頼性、完全性を確保し、記録したデータの操作を防ぐために、すべてのトランザクションに TSE が署名する必要があります。

> [!WARNING]
> 認定済みの TSE のみを使用できます。 EFR ソリューションがサポートする TSE の種類とモデルについては、[EFSTA ドキュメント](https://public.efsta.net/efr/) Web サイトで硬化されている "EFR ガイド \[DE\]" ドキュメントをご覧ください。 TSE を選択して導入する方法については [EFSTA](https://www.efsta.eu/at/kontakt) にお問い合わせください。

ドイツの規制により DSFinV-K のエクスポートに対応する必要があります。 EFR ソリューションで DSFinV-K エクスポートをトリガーできます。 DSFinV-K エクスポートの詳細については、[EFSTA ドキュメント](https://public.efsta.net/efr/) Web サイトで公開されている "EFR ガイド \[DE\]" ドキュメントをご覧ください。

### <a name="limitations-of-the-sample"></a>サンプルの制限事項

会計登録サービスは、消費税が価格に含まれているシナリオのみをサポートします。 したがって、**税込価格** オプションは、店舗と顧客の両方で **はい** に設定する必要があります。

会計サービスは、同じトランザクション明細行に複数の消費税コードを適用する状況に対応していません。

会計統合フレームワークは販売見積に対応していません。 そのため、これらの操作は会計サービスに登録されません。

## <a name="set-up-commerce-for-germany"></a>ドイツ向け Commerce を設定する

このセクションでは、ドイツに固有で推奨される Commerce 設定について説明します。 設定の詳細については、[Commerce のホーム ページ](../index.md) を参照してください。

ドイツに固有の機能を使用する際は、次の設定を指定する必要があります。

- 法人の基本住所で、**国/地域** フィールドを **DEU** (ドイツ) に設定します。
- ドイツにあるすべての店舗の POS 機能プロファイルで、 **ISO コード フィールド** を **DE** (ドイツ) に設定します。

ドイツに対応する次の設定を指定する必要があります。 設定が完了したら、必ず適切な配布ジョブを実行します。

### <a name="set-up-vat-per-german-requirements"></a>ドイツの要件に従って VAT を設定する

消費税コード、消費税グループ、品目の消費税グループを作成する必要があります。 また、製品やサービスの消費税情報を設定する必要があります。 消費税機能の設定と使用方法の詳細については、[消費税の概要](../../finance/general-ledger/indirect-taxes-overview.md)を参照してください。

消費税コードの省略コードを領収書に印刷できます (例: "A" や "B")。 この機能の使用を有効化する場合は、**消費税コード** ページで **印刷用コード** フィールドを設定します。

### <a name="set-up-stores"></a>店舗を設定する

**すべての店舗** ページで店舗の詳細を更新します。 具体的には、次のパラメーターを設定する必要があります:

- **消費税グループ** フィールドで、既定の顧客への販売に使用するべき消費税グループを指定します。
- **税込価格** オプションに **はい** をセットします。
- **名前** フィールドに会社名を設定します。 この変更により、会社名が領収書に確実に表示されます。 または、会社名を自由形式のテキストとして領収書のレイアウトに追加できます。
- **税 ID 番号 (TIN)** フィールドに会社識別番号を設定します。 この変更により、会社の ID 番号が領収書に確実に表示されます。 または、会社 ID 番号を自由形式のテキストとして領収書のレイアウトに追加できます。

### <a name="set-up-functionality-profiles"></a>機能プロファイルを設定する

POS 機能プロファイルを設定します。 **領収書番号** ファストタブ で、**販売**、**販売注文**、**返品** の領収書トランザクション タイプに対してレコードの作成や更新を行い、領収書番号を設定します。

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>カスタム フィールドを設定して、販売領収書の領収書形式で使用できるようにする

POS 領収書形式で使用される言語テキストおよびカスタム フィールドを構成することができます。 領収書設定を作成するユーザーの既定の会社は、言語テキスト設定が作成された法人と同じである必要があります。 または、ユーザーの既定の会社、および設定の作成対象の店舗の法人の両方で、同じ言語テキストを作成する必要があります。

**言語テキスト** ページで、領収書 レイアウト用のカスタム フィールドのラベルに次のレコードを追加します。 テーブルに表示されている **言語 ID**、**テキスト ID**、および **テキスト** の値は、単なる例に過ぎません。 要件に合わせてそれらを変更できます。 ただし、使用する **テキスト ID** の値は一意である必要があり、900001 以上である必要があります。

**言語テキスト** ページの **POS** セクションに、次の POS ラベル を追加します。

| 言語 ID | テキスト ID | テキスト                                  |
|-------------|---------|---------------------------------------|
| ja       | 900001  | QR コード                               |
| ja       | 900002  | 取引 ID                        |
| ja       | 900003  | 税小売印刷コード                 |
| ja       | 900004  | 税額 (売上)                    |
| ja       | 900005  | 課税基準 (売上)                     |
| ja       | 900006  | トランザクション開始日時           |
| ja       | 900007  | トランザクション終了日時             |
| ja       | 900008  | セキュリティ要素のシリアル番号 |
| ja       | 900009  | 署名カウンター                     |
| ja       | 900010  | 確認値                           |
| ja       | 900011  | 情報メッセージ                          |

**カスタム フィールド** ページで、領収書 レイアウトのカスタム フィールドに次のレコードを追加します。 **キャプション テキスト ID** の値は、**言語テキスト** ページで指定した **テキスト ID** の値に対応している必要があることに注意してください。

| Name                            | 種類    | キャプション テキスト ID |
|---------------------------------|---------|-----------------|
| QRCODE\_DE                      | 受信 | 900001          |
| TRANSACTIONID\_DE               | 受信 | 900002          |
| RETAILPRINTCODE\_DE             | 受信 | 900003          |
| SALESTAXAMOUNT\_DE              | 受信 | 900004          |
| SALESTAXBASIS\_DE               | 受信 | 900005          |
| TRANSACTIONSTARTDATETIME\_DE    | 受信 | 900006          |
| TRANSACTIONENDDATETIME\_DE      | 受信 | 900007          |
| SECURITYELEMENTSERIALNUMBER\_DE | 受信 | 900008          |
| SIGNCOUNTER\_DE                 | 受信 | 900009          |
| SIGN\_DE                        | 受信 | 900010          |
| INFOMESSAGE\_DE                 | 受信 | 900011          |

> [!NOTE]
> 上記の表にあるように、正しいカスタム フィールド名を指定することが重要です。 カスタム フィールド名が正確でない場合、領収書のデータが失われます。

### <a name="configure-receipt-formats"></a>レシート形式を設定する

必要な領収書の形式ごとに、**印刷動作** フィールドの値を **常に印刷** に変更します。

領収書の形式デザイナーで、次のカスタム フィールドを適切な領収書セクションに追加します。 フィールド名は、前のセクションで定義した言語テキストに対応していることに注意してください。

- **ヘッダー:** 次のフィールドを追加します。

    - **店舗名** と **税 ID 番号** フィールド。領収書に会社名と ID 番号を印刷する際に使用します。 または、会社名と ID 番号を自由形式のテキストとしてレイアウトに追加できます。
    - **店舗住所**、**日付**、**時刻 24H**、**受領番号**、**登録番号** フィールド。

- **明細行:** 次のフィールドを追加します。

    - **品目名** フィールド
    - **数量** フィールド
    - **税込合計価格** フィールド
    - **税小売印刷コード** フィールド。品目に適用する消費税コードに対応した、省略コードの印刷に使用します

- **フッター:** 次のフィールドを追加します。

    - 支払フィールド。支払方法ごとに支払金額を印刷します。 たとえば、**支払名** と **支払金額** のフィールドをレイアウトの 1 行に追加します。
    - **税内訳** フィールド グループのフィールド。 このフィールド グループが含むすべてのフィールドは、個別の 1 行に印刷する必要があります。

        - **税 ID** フィールド。消費税コードごとに消費税の概要を印刷できるようにする標準フィールド。 このフィールドは新しい行に追加する必要があります。
        - **税率** フィールド。消費税コードの実効税率の印刷に使用する標準フィールド。
        - **課税基準 (売上)** フィールド。消費税コードに対する領収書の現金販売合計額の印刷に使用します。 前払いとギフト カードの操作は除きます。
        - **税額 (売上)** フィールド。消費税コードに対する現金販売の、領収書の税額を印刷するために使用します。
        - **税小売印刷コード** フィールド。消費税コードに対応した省略コードの印刷に使用します。

    - 会計登録サービスが返す保護されたトランザクション データを含むフィールド。

        - **トランザクション ID** フィールド。会計登録サービスで現金トランザクションの件数を特定します
        - **トランザクションの開始日時** フィールド
        - **トランザクションの終了日時** フィールド
        - **セキュリティ要素のシリアル番号** フィールド
        - **署名カウンター** フィールド
        - **確認値** フィールド
        - **QR コード** フィールド。登録した現金トランザクションの参照を QR コード形式で印刷するために使用します

        > [!NOTE]
        > **QR Code** 値は会計レジスターの応答から取得します。 EFR 構成の **属性** フィールドの値を EFSTA ドキュメントに記載する場合のみ、EFR は応答で QR コードを返します。 EFR 構成の **属性** フィールドの QR コード形式は **BMP** に設定する必要があります。

    - **情報メッセージ** フィールド。会計登録サービスからの通知メッセージを領収書に表示できるようにします。 たとえば、署名デバイスが壊れている場合は領収書に特別なテキストを印刷できます。

領収書形式の使用方法の詳細については、[領収書形式の設定とデザイン](../receipt-templates-printing.md)を参照してください。

## <a name="set-up-fiscal-integration-for-germany"></a>ドイツ向け会計統合を設定する

ドイツの会計登録サービス統合サンプルは、[会計統合機能](fiscal-integration-for-retail-channel.md) に基づいており、Retail SDK に含まれています。 サンプルは [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) リポジトリの **src\\FiscalIntegration\\Efr** フォルダにあります (例: [release/9.33 のサンプル](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)) サンプルは、Commerce Runtime (CRT) の拡張である会計ドキュメント プロバイダーと、Commerce ハードウェア ステーションの拡張である会計コネクタで [構成されています](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)。 Retail SDK の使用方法の詳細については [Retail SDK のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) と [独立したパッケージ SDK のビルド パイプラインを設定する](../dev-itpro/build-pipeline.md) を参照してください。

> [!WARNING]
> [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、この会計統合サンプルでは使用できません。 Microsoft Dynamics Lifecycle Services (LCS) の開発者仮想マシン (VM) で、Retail SDK の以前のバージョンを使用する必要があります。 詳細については、[ドイツ向け会計統合サンプルの展開ガイドライン (レガシ)](emea-deu-fi-sample-sdk.md) を参照してください。
>
> 今後のバージョンで、会計統合サンプルの新しい独立したパッケージと拡張モデルのサポートを計画しています。

[Commerce チャンネルの会計統合を設定する](setting-up-fiscal-integration-for-retail-channel.md) で説明されている会計統合の設定手順を実行します。

1. [会計登録プロセスの設定](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process)。 また、[今回の会計登録サービス統合サンプルに固有](#set-up-the-registration-process)の会計登録処理の設定をメモしておきます。
1. [エラーの処理の設定](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings)。

    > [!WARNING]
    > 会計統合フレームワークのエラー処理機能は、地域の会計規制と完全に一致していない可能性があります。
    >
    > - 会計登録の最初の実行が成功しなかった場合でも、すべてのトランザクションを正しく登録する必要があるため、**会計登録プロセス** ページの **エラーでも続行** オプションをオフのままにすることを推奨します。
    > - **会計登録プロセス** ページで **スキップ** や **登録済としてマーク** オプションをオンにする前に、会計登録プロセスに対するこれらの変更について、税理士や地域の税務署と協議する必要があります。

1. [延期された会計登録の手動実行を可能にする](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration)。
1. [チャネル コンポーネントの構成](#configure-channel-components)。

### <a name="set-up-the-registration-process"></a>登録プロセスの設定

登録プロセスを有効化する場合は、次の手順に従って Commerce Headquarters を設定します。 詳細情報については、[コマース チャネルの会計統合の設定](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) を参照してください。

1. 会計ドキュメント プロバイダーと会計コネクタの構成ファイルをダウンロードします。

    1. [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) レポジトリ を開きます。
    1. SDK/アプリケーションのバージョンに応じた適切なリリース ブランチ バージョンを選択します (例: **[リリース/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**)。
    1. **src \> FiscalIntegration \> Efr** を開きます。
    1. **Configurations \> DocumentProviders \> DocumentProviderFiscalEFRSampleGermany.xml** で会計ドキュメント プロバイダー構成ファイルをダウンロードします (例: [リリース/9.33 のファイル](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleGermany.xml))。
    1. **Configurations \> Connectors \> ConnectorEFRSample.xml** から会計コネクタ構成ファイルをダウンロードします (例: [リリース/9.33 のファイル](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml))。

    > [!WARNING]
    > [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、この会計統合サンプルでは使用できません。 LCS の開発者 VM では以前のバージョンの Retail SDK を使用する必要があります。 この会計統合サンプルの構成ファイルは、LCS の開発者 VM 上の Retail SDK が含む次のフォルダーに存在します。
    >
    > - **会計ドキュメント プロバイダ構成ファイル:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration\\DocumentProviderFiscalEFRSampleGermany.xml
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

- **テンダー タイプのマッピング** – 会計サービスに送信する要求の、**PayG** (支払グループ) 属性の値に対する支払方法のマッピング。 既定のマッピングを次に示します。

    ```
    1: 0; 2: 1; 3: 3; 4: 8; 5: 2; 6: 0; 7: 7; 8: 6; 9: 0; 10: 8; 11: 1
    ```

    各ペアの最初のコンポーネントは、ストアに設定されている支払い方法を表しています。 2つ目のコンポーネントは、EFR 会計登録サービスでサポートされている対応する支払グループを表します。 EFR がドイツでサポートする支払グループの詳細については、[EFR のリファレンス](https://public.efsta.net/efr/) をご覧ください。

    支払方法のサンプル マッピングは、標準のデモ データで構成された店舗の支払方法に対応します。

    | 支払方法 | 支払方法名 |
    |----------------|---------------------|
    | 1              | 現金                |
    | 2              | 検査               |
    | 3              | カード                |
    | 4              | 顧客 ID    |
    | 5              | その他               |
    | 6              | 通貨            |
    | 7              | 伝票             |
    | 8              | ギフト カード           |
    | 9              | 支払/入金の削除/釣銭入力 |
    | 10             | ロイヤルティ カード       |
    | 11             | 非ローカル小切手    |

    したがって、アプリケーションで構成されている支払い方法に合わせて、サンプルのマッピングを変更する必要があります。

- **顧客データを含める** – このパラメーターをオンにすると、顧客をトランザクションに追加した場合に、名前や住所などの顧客情報を会計サービスへの要求に含めます。
- **付加価値税 (VAT) 税率マッピング** – 税率値のマッピング。会計サービスに送信する要求の **TaxG** (税グループ) 属性の値に対する消費税コードに対して設定します。 既定のマッピングを次に示します。

    ```
    A: 19.00; B: 7.00; C: 10.70; D: 5.50; E: 0.00
    ```

    それぞれのペアの最初のコンポーネントは、EFR 会計登録サービスがサポートする VAT 税グループを表します。 2 番目のコンポーネントは対応する VAT 率を表します。 EFR がドイツでサポートする VAT 税グループの詳細については、[EFR のリファレンス](https://public.efsta.net/efr/) をご覧ください。

- **ギフト カードと前金の税グループ** – ギフト カードや前金を含む操作に基づいて、会計サービスに送信する要求の **TaxG** 属性の値。 既定のマッピングを次に示します。

    ```
    G
    ```

- **VAT 控除の税グループ** – 納税義務を免除された業務に基づいて、会計サービスに送信する要求の **TaxG** 属性の値。 既定のマッピングを次に示します。

    ```
    F
    ```

> [!NOTE]
> 既定データ マッピングの税設定によって、システムの税設定と EFR サービスの税グループを一致させます。 税グループを領収書に印刷できるのは、**消費税コード** ページで **印刷用コード** フィールドを設定した場合のみです。

#### <a name="fiscal-connector-settings"></a>会計コネクタの設定

次の設定は、会計統合サンプルの一部として提供される会計コネクタ構成に含まれています。

- **エンドポイント アドレス** – 会計登録サービスの URL。
- **タイムアウト** – ミリ秒単位で表した時間。会計コネクタは会計登録サービスからの応答を待機します。
- **会計登録通知を表示する** – 会計登録サービスが返す通知をオペレーターに表示するかどうかを、このフラグによって制御します。

### <a name="configure-channel-components"></a>チャネル コンポーネントの構成

> [!WARNING]
> [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、この会計統合サンプルでは使用できません。 LCS の開発者 VM では以前のバージョンの Retail SDK を使用する必要があります。 詳細については、[ドイツ向け会計統合サンプルの展開ガイドライン (レガシ)](emea-deu-fi-sample-sdk.md) を参照してください。
>
> 今後のバージョンで、会計統合サンプルの新しい独立したパッケージと拡張モデルのサポートを計画しています。

#### <a name="set-up-the-development-environment"></a>開発環境の設定

開発環境を設定してサンプルのテストと拡張を行う際は、次の手順に従います。

1. [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions) リポジトリをクローンまたはダウンロードします。 SDK/アプリケーションのバージョンに応じた適切なリリース ブランチ バージョンを選択します。 詳細については、[GitHub と NuGet から Retail SDK サンプルと参照パッケージをダウンロードする](../dev-itpro/retail-sdk/sdk-github.md) を参照してください。
1. **Dynamics365Commerce.Solutions\\FiscalIntegration\\Efr\\EFR.sln** で EFR ソリューションを開き、ビルドします。
1. Commerce Runtime 拡張機能をインストールします。

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

ドイツの会計登録サービス統合サンプルは、[会計統合機能](fiscal-integration-for-retail-channel.md) に基づいており、Retail SDK に含まれています。 サンプルは [Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) リポジトリの **src\\FiscalIntegration\\Efr** フォルダにあります (例: [release/9.33 のサンプル](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)) サンプルは、CRT の拡張である会計ドキュメント プロバイダーと、Commerce ハードウェア ステーションの拡張である会計コネクタで [構成されています](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)。 Retail SDK の使用方法の詳細については [Retail SDK のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) と [独立したパッケージ SDK のビルド パイプラインを設定する](../dev-itpro/build-pipeline.md) を参照してください。

> [!WARNING]
> [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、この会計統合サンプルでは使用できません。 LCS の開発者 VM では以前のバージョンの Retail SDK を使用する必要があります。 詳細については、[ドイツ向け会計統合サンプルの展開ガイドライン (レガシ)](emea-deu-fi-sample-sdk.md) を参照してください。 今後のバージョンで、会計統合サンプルの新しい独立したパッケージと拡張モデルのサポートを計画しています。

### <a name="crt-extension-design"></a>CRT 拡張機能の設計

会計ドキュメント プロバイダーである拡張機能の目的は、サービスに特化したドキュメントを生成して会計登録サービスからの応答を処理することです。

#### <a name="request-handler"></a>要求ハンドラー

ドキュメント プロバイダーに対応した要求ハンドラーが 1 つあります: **DocumentProviderEFRFiscalDEU**。 このハンドラーは、会計登録サービスの会計ドキュメントを生成する際に使用します。 これは **INamedRequestHandler** インターフェイスから継承します。 **HandlerName** メソッドの機能がハンドラーの名前を返します。 このハンドラー名は、Commerce headquarters で指定したコネクタ ドキュメント プロバイダーの名前と一致する必要があります。

このコネクタは次の要求をサポートします。

- **GetFiscalDocumentDocumentProviderRequest** – この要求は生成するべきドキュメントに関する情報を含みます。 これは会計登録サービスに登録するべきサービス固有のドキュメントを返します。
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** – この要求は拡張データとともに応答を返します。

#### <a name="configuration"></a>構成

会計ドキュメント プロバイダーの構成ファイルは、[Dynamics 365 Commerce ソリューション](https://github.com/microsoft/Dynamics365Commerce.Solutions/) レポジトリの **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders\\DocumentProviderFiscalEFRSampleGermany.xml** にあります。 このファイルによって、Commerce Headquarters から会計ドキュメント プロバイダーの設定を構成できるようになります。 ファイル形式は会計統合構成の要件に従います。

### <a name="hardware-station-extension-design"></a>ハードウェア ステーション拡張機能の設計

会計コネクタである拡張機能によって、会計登録サービスと通信できます。

ハードウェア ステーション拡張機能は **HardwareStation.Extension.EFRSample** です。 これは HTTP プロトコルを使用し、CRT 拡張機能が生成するドキュメントを会計登録サービスに送信します。 また、会計登録サービスから受信した応答も処理します。

#### <a name="request-handler"></a>要求ハンドラー

**EFRHandler** 要求ハンドラーは、会計登録サービスへの要求を処理するエントリ ポイントです。 このハンドラは **INamedRequestHandler** インターフェイスから継承します。 **HandlerName** メソッドの機能がハンドラーの名前を返します。 このハンドラー名は、Commerce headquarters で指定した会計コネクタの名前と一致する必要があります。

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
