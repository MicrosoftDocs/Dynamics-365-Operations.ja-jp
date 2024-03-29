---
title: データ パッケージを使用してデモ データを生成します
description: この記事では、デモ データ パッケージを使用して、システムのデータを生成する方法について説明します。
author: panolte
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 77523
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2017-11-30
ms.dyn365.ops.version: Platform update 12
ms.openlocfilehash: 3d6e8c808165dab239ce6587de60198f20d44596
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109408"
---
# <a name="generate-demo-data-by-using-data-packages"></a>データ パッケージを使用してデモ データを生成します

[!include [banner](../includes/banner.md)]

以前のリリースでは、デモ データはデータベースとして提供されました。 Microsoft Dynamics 365 Finance Enterprise edition 7.3では、デモ データのサブセットは、データ パッケージとしてリリースされています。 これらのパッケージは、Microsoft Dynamics Lifecycle Services (LCS) の共有アセット ライブラリで使用できます。 パッケージは、空の環境に読み込むことができるように設計されています。

デモ データを配信するため、データベースの代わりにデータ パッケージを使用する利点を次に示します。

- ダウンロード時間が大幅に短縮されます。
- 必要なデータ パッケージのみをインポートすることができます。
- スプレッドシートを編集して、顧客のためにデータをカスタマイズすることができます。
- 更新されたデモ データは、LCS を通じて迅速に提供できます。

> [!NOTE]
> デモ データ パッケージは、現在提供されているデモ データベースの完全な置き換えではありません。

## <a name="how-the-packages-are-organized"></a>パッケージが管理される方法

デモ データ パッケージは、次の図に示すように、お互いの最上部に重ねて表示されるように設計されています。

![デモ データ パッケージ。](./media/demodatapackages_layers.png)

ただし、1 つのデモ シナリオのグローバル情報には、別のデモ シナリオのグローバル情報とは全く異なる要求がある場合があります。 たとえば、1 つのシナリオの分析コードは、別のシナリオの分析コードを妨げます。 この場合、個別のグローバル情報パッケージが作成され、グローバル情報に関連するパッケージのみをパッケージの最上部に重ねることができます。

たとえば、現在、商業用システムと共有パッケージ、ならびに公的機関用システムおよび共に使用することができない共有パッケージがあります。

### <a name="system-and-shared-package"></a>システムと共有パッケージ

基本パッケージであるシステムと共有は、その他のすべてのパッケージの基盤です。 このパッケージは法人を作成し、グローバル アドレス帳を読み込み、他の共有情報を追加します。 残りのすべてのパッケージをサポートするために最初にロードする必要があります。 このパッケージの名前は、**100-System and Shared.zip** です。

システムと共有のパッケージがロードされた後、次の法人の 1 つ以上が表示されます。

| 個法 | 説明 |
|--------------|-------------|
| HQUS | デモ会社の米国本社。 この会社は元の USMF データに基づいていますが、名前の製造フォーカスを削除するように変更されました。 これには、米国企業を意図とした設定情報が含まれます。 |
| HQEU | デモ会社の米国以外の本社。 この会社は元の DEMF データに基づいていますが、名前の製造フォーカスを削除するように変更されました。 これには、米国外の企業を意図とした設定情報が含まれます。 |
| 短所 | 小さな連結会社。 |
| PICH | 化学物質に特化したプロセス工業会社。 |
| PIFB | 食品と飲料に特化した加工業会社。 |

### <a name="financials"></a>Financials

財務データ パッケージには、1 つの会社の一般会計、銀行、買掛金勘定、税金、売掛金勘定、固定資産、予算のデータが含まれます。 これらのデータ パッケージの名前は、**200-Financials** で構成され、後にパッケージが意図する法人が続きます。 たとえば、HQUS 法人の Financials データ パッケージは、**200-Financials-HQUS.zip** と呼ばれます。

集中支払などの会社間タスクには少なくとも 2 つの金融会社が必要です。 企業間の業務を容易にするため、すべての顧客と仕入先が各法人に追加されています。 CONS 法人は、連結を実行する場合に必要です。

財務データ パッケージには、売掛金勘定と買掛金勘定プロセスを通じて移動できる請求書の作成をサポートするための 5 つの在庫商品もあります。 これらの項目は、これらのプロセスをサポートするために、最小限の在庫と製品機能を使用します。 ただし、財務機能のみを説明するときに、製品を設定する必要がなくなりました。 サプライ チェーン データ パッケージをインポートすると、より完全な製品が追加されます。

### <a name="expense-management"></a>経費管理
経費管理データ パッケージには、経費管理のデータが含まれており、プロジェクト管理に固有ではありません。 これらのデータ パッケージの名前は、**225- 経費** で構成され、後にパッケージが意図する法人が続きます。 たとえば、HQUS 法人の経費管理データ パッケージは、**225- 経費管理 HQUS.zip** と呼ばれます。

### <a name="project-management-and-accounting"></a>プロジェクト管理および会計

プロジェクト管理と会計データ パッケージには、プロジェクトの計算と経費の管理用のデータが含まれます。 これらのデータ パッケージの名前は、**250-プロジェクト管理と会計** で構成され、後にパッケージが意図する法人が続きます。 たとえば、HQUS 法人のプロジェクト管理および会計データ パッケージは **250- プロジェクト管理と会計 -HQUS.zip** と呼ばれます。

### <a name="supply-chain"></a>サプライ チェーン

サプライ チェーン データ パッケージには、1 社の在庫管理、製品情報、調達およびソーシング、販売およびマーケティング、品質管理、倉庫管理、輸送管理、生産管理、プロセス製造、原価計算、およびマスター プランのデータが含まれています。 エンティティの数が多いため、一部の会社のサプライ チェーン パッケージは 2 つのパッケージに分割されています。 サプライ チェーンのシナリオを完了させるために、両方のパッケージを読み込む必要があります。 ただし、これらのパッケージを 2 つの個別のプロジェクトとして読み込むことができます。

これらのデータ パッケージの名前は、**300-Supply chain** で構成され、後にパッケージが意図する法人が続きます。 たとえば、HQUS 法人のサプライ チェーン データ パッケージは、**300- サプライ チェーン -PICH.zip** と呼ばれます。 HQUS の法人組織のサプライチェーン パッケージは、**300-Supply chain 1 (2-HQUS.zip)** と **300-Supply chain 2 (2-HQUS.zip)** というパッケージに分割されています。

## <a name="demo-data-package-releases"></a>デモ データ パッケージをリリースします

デモ データ パッケージは LCS を通じてリリースされ、リリースに特有のものとなります。 さらにデモ シナリオを追加してパッケージを調整するため、特定のパッケージの内容が変わることに注意してください。 さらに多くのモジュール エリアと業界特有のシナリオを追加して、追加のパッケージもリリースされる予定です。

パッケージ名には、リリース ID が含まれます。 たとえば、財務と運用 7.3 に対して、**デモ データ -7.3-** は、前述の名前付け規則を使用するパッケージ名に先行します。 たとえば、財務と運用 7.3 の HQUS 法人に対する Financials パッケージの正式名称は、**デモ データ -7.3-200-Financials-HQUS.zip** になります。

## <a name="before-you-load-the-packages"></a>パッケージを読み込む前に

データ パッケージをロードする前に、以下の手順を手動で行なう必要があります。

1. 特定のユーザーとしてログインする場合は、ユーザーの電子メール アドレスを、使用するサインイン アドレスに変更します。 **ユーザー情報** データ エンティティ スプレッドシートで、またはデータを読み込んだ後に **ユーザー** ページ (**システム管理** &gt; **ユーザー**) でこの変更を加えることができます。
2. **投稿準備完了** バッチ スケジューラーを起動します。 このバッチ ジョブは、取引を自動的に転記します。 データが処理されるすべての法人のスケジューラを起動する必要があります。 この記事で後述する「プロセス転記の準備完了」セクションの手順に従います。
3. en-us ロケールを使用していない場合、パッケージが構築された形式と一致するようにソース データ形式を変更する必要があります。 データ エンティティを読み込んだら、ソース データ形式列をクリックします。値が Excel として指定される必要があります。 次のページから、Excel をもう一度選択します。 ソース データ形式ページでは、下部の高速タブは地域の設定となります。 en-us が指定されていない場合は、言語ロケールを en-us に変更します。 パッケージをロードしたら、元の en-us 以外の値に戻すことができます。 

## <a name="load-the-packages"></a>パッケージの読み込み

データ パッケージは、特定の法人に特定の順序でロードする必要があります。 パッケージの名前の前の番号は、データを読み込む必要のある順序についてのガイダンスを提供します。 たとえば、HQUS 法人 **200-Financials-HQUS.zip** に対する Financials パッケージを読み込む前に、**100-System and Shared.zip** をインポートする必要があります。 その後、サプライ チェーン データを HQUS 法人に追加するために、**300-Supply chain 1 of 2-HQUS.zip** および **300-Supply chain 2 of 2-HQUS.zip** を読み込めます。

パッケージを読み込むには、これらの手順に従います。

1. データがロードされていない空のインスタンスを使用して開始します。
2. **データ管理** ワークスペースを開きます。
3. **インポート** タイルを選択し、インポート ジョブを作成します。
4. 職務の名前を入力します。 たとえば、**共有情報のインポート** を入力します。
5. **ファイルの追加** を選択してください。
6. **アップロードおよび追加** を選択し、インポートするデータ パッケージを参照します。 システムおよび共有データ パッケージで開始する必要があります。
7. データ パッケージを選択し、読み込むデータを待ちます。
8. データが読み込まれた後、ダイアログ ボックスを閉じ、**インポート** を選択します。
9. 読み込む必要のあるすべての追加パッケージに対して手順 5 ～ 8 を繰り返します。 データ パッケージが意図している法人に切り替えます。

### <a name="loading-package-combinations"></a>パッケージ読み込みの組み合わせ

次のパッケージを読み込むことができます。 システムおよび共有パッケージ以外のパッケージをインポートするときは、パッケージ名に記載されている法人に所属している必要があります。 システムおよび共有パッケージは、すべての法人から読み込むことができます。 ただし、通常既定の会社 DAT から読み込まれます。

商業データ

| 説明 | 摘要 |
|-------------|-------|
| 100 - システムと共有 | その他のパッケージの前に、このパッケージを読み込みます。 |
| 200 - 財務 - HQUS | このパッケージは単独で、または別の財務パッケージと共に読み込むことができます。 |
| 200 - 財務 - HQEU | このパッケージは単独で、または別の財務パッケージと共に読み込むことができます。 |
| 200 - 財務 - CONS | このパッケージは単独で、または別の財務パッケージと共に読み込むことができます。 |
| 200 - 財務 - PICH | このパッケージは単独で、または別の財務パッケージと共に読み込むことができます。 |
| 200 - 財務 - PIFB | このパッケージは単独で、または別の財務パッケージと共に読み込むことができます。 |
| 225 - 経費管理 - HQUS | インポートを開始する前に、前提条件の手順に従ってください。 HQUS の Financials パッケージの後に、このパッケージを読み込みます。 |
| 250 - プロジェクト管理 - HQUS | HQUS の財務または経費パッケージの後に、このパッケージを読み込みます。 サプライ チェーンも使用する場合は、このパッケージを最初にインポートする必要があります。 |
| 300 - サプライ チェーン 2 の 1 (基本) - HQUS | HQUS の Financials パッケージの後に、このパッケージを読み込みます。 プロジェクト管理も使用する場合、このパッケージをインポートする前に最初にプロジェクト管理パッケージをインポートする必要があります。 |
| 310 - サプライ チェーン 2 の 2 (個別) - HQUS | HQUS サプライ チェーン 基本パッケージの後に、このパッケージを読み込みます。 |
| 300 - サプライ チェーン - PIFB | PICH サプライ チェーン パッケージの後に、このパッケージを読み込みます。 |
| 300 - サプライ チェーン - PICH | PIFB サプライ チェーン パッケージの後に、このパッケージを読み込みます。 |
| 900 - 財務トランザクション - HQUS | HQUS の Financials パッケージの後に、このパッケージを読み込みます。 |
| 900 - 財務トランザクション - HQEU | このパッケージは単独で、または別の財務パッケージと共に読み込むことができます。 |

公的機関のデータ

| 説明 | 摘要 |
|-------------|-------|
| 100 - 公的機関システムと共有 | その他のパッケージの前に、このパッケージを読み込みます。 |
| 200 -PSUS Financials | このパッケージだけを読み込むことができます。 |
| 900 - PSUS 財務トランザクション | PSUS の Financials パッケージの後に、このパッケージを読み込みます。 |

データを正常に読み込むには、一度に 1 つのパッケージを読み込んでインポートし、インポートが完了したら次のパッケージを読み込む必要があります。 プロセスを向上させるために、デモ データを読み込むための追加の方法を検討しています。

### <a name="troubleshooting-and-known-issues"></a>トラブルシューティングと既知の問題
> [!NOTE]
> パッケージ内のデータは正しいけれども、インポート時にランダムな障害を発生する番号順序参照エンティティに問題があることが判明しました。 番号シーケンス参照のインポート中にエラーが表示された場合は、次の手順に従って失敗したレコードを処理します。
>
> 1. エンティティ (**番号順序の参照**) の名前をクリックすると、データ パッケージ内のすべてのレコードを一覧表示するフォームが表示されます。
> 2. **データをターゲットにコピー** をクリックします。
> 3. **実行** 値を **基準**、および **前のエラーがある行の変更** を **はい** に変更します。
> 4. **Ok** をクリックし、表示されるフォームで **実行** をクリックします。
> 5. エラーなしですべてのレコードがインポートされるまで、次の手順を繰り返します。

> [!NOTE]
> 一部のデータ エンティティが同じ名前であるという問題が現在あります。つまり、**200 - 財務** パッケージの **ドキュメント タイプ** と **日付間隔** のインポートに失敗する可能性があります。 これらのエンティティのインポートが、作成された .zip ファイルから書き込みおよび自動的にインポートしている間にエラーが表示された場合、**DocuTypeEntity** を指す **ドキュメント タイプ** と **LedgerDateIntervalEntity** を指す **日付間隔** を使用します。 一度インポートされると、**200 - 財務** パッケージから失敗したレコードを再試行できます。 

### <a name="after-you-load-the-packages"></a>パッケージをロードした後

何か投稿する必要がある場合は、**投稿準備完了** をチェックします。 場合によっては、個々のデモ スクリプトはこのデータを読み込む前にいくつかの設定を実行するよう勧める可能性があります。

場合によっては、特別なシナリオまたは欠落しているエンティティが原因で追加するデータが存在する場合があります。 データ パッケージをロードが完了したら、そのデータを追加します。 手動で追加のトランザクションを転記するか、またはデモ操作性を強化するために独自のデータ パッケージを追加することもできます。

データ パッケージをロードした後、以下の手順も手動で行なう必要があります。

1. ワークフロー ジョブを開始します。 **システム管理** &gt; **ワークフロー インフラストラクチャ コンフィギュレーション** を選択し、**OK** を選択します。
2. ポリシー優先順位ルールを設定します。 **調達** &gt; **設定** &gt; **ポリシー** &gt; **購入ポリシー** を選択し、**パラメーター** を選択します。 その後、**会社** を選択し、右の列に移動します。
3. 経費パッケージをインポートする前に、ポリシーの優先順位を設定します。 **経費管理** &gt; **設定** &gt; **ポリシー** &gt; **経費レポート** を選び、**パラメーター** を選択します。 その後、**会社** を選択し、右の列に移動します。
4. プロジェクト管理および会計パッケージをロードした後、**リソース能力のロールアップ** バッチ ジョブを実行する必要があります。 このジョブは **リソース能力のロールアップを同期** ページ (**プロジェクト管理と会計** &gt; **定期処理** &gt; **能力の同期** &gt; **リソース能力のロールアップを同期**) から実行することができます。 将来の長い期間リソースをスケジュールすることができる終了日を指定します。 バッチ ジョブを実行した後、チーム機能の自動生成は、プロジェクトの作業分解構造 (WBS) で有効になります。
5. 各モジュールの印刷管理設定を追加します。

## <a name="transactions-and-automatic-posting"></a>トランザクションと自動転記

デモ データの多くのシナリオでは、インポート後にトランザクションを処理する必要があります。 投稿準備機能を使用することにより、トランザクションを処理することができます。 この機能には、転記すべき取引を定義するページと、定義をインポートして自動的に実行できるエンティティの両方が含まれます。

デモ データの転記時には、次のトランザクション タイプがサポートされています。

| 書類 | エンティティ ドキュメント ID | 日付フィルター | ID フィルター | その他のフィルター |
|----------|--------------------|-------------|------------|---------------|
| 予算レジストリの更新 | BudgetRegistryUpdate | 既定の日付 | 予算エントリ番号 | 使用されていない、ステータス = ドラフト |
| 原価バージョン | CostingVersion | 該当なし | バージョン ID | バージョンの有効化のブロック = いいえ | 
| 顧客支払の仕訳帳 | CustomerPaymentJournal | 取引日付 | 仕訳帳番号 | 転記されていない、ワークフローではない、システムにブロックされていない | 
| 日次仕訳帳 | GeneralJournal | 取引日付 | 仕訳帳番号 | 転記されていない、ワークフローではない、システムにブロックされていない |
| 固定資産仕訳帳 | FixedAssetsJournal | 取引日付 | 仕訳帳番号 | 転記されていない、ワークフローではない、システムにブロックされていない |
| 自由書式の請求書 | FreeTextInvoice | 請求日 | 該当なし | |
| 在庫調整仕訳帳 | InventoryAdjustmentJournal | 取引日付 | 仕訳帳番号 | 未転記 |
| 請求仕訳帳 | InvoiceJournal |取引日付 | 仕訳帳番号 | 転記されていない、ワークフローではない、システムにブロックされていない |
| 価格計算 | PriceCalculation | 該当なし | バージョン ID | バージョンの有効化のブロック = いいえ |
| 発注書 | PurchaseOrder | 出荷日 | 発注書 ID | /PR/仕入先/請求書の確認が可能 |
| 販売注文 | SalesOrder | 出荷日 | 販売注文 ID | /梱包明細/請求書の確認が可能 |
| 売買契約 | TradeAgreement | 該当なし | 価格/割引仕訳帳番号 | |
| 仕入先請求書 | VendorInvoice |転記日付 | 請求書番号 | 承認済、使用されていない、まだ |
| ベンダー支払仕訳帳 | VendorPaymentJournal | 取引日付 | 仕訳帳番号 | 転記されていない、ワークフローではない、システムにブロックされていない |

日付範囲をサポートする仕訳帳については、プロセス転記の準備完了は、指定された範囲内になる日付のすべての仕訳帳明細行を検討します。 仕訳帳のすべての明細行が期間内に入る場合、検索が停止され、全体のバッチが転記されます。

### <a name="the-ready-to-post-process"></a>転記準備完了プロセス

転記準備完了機能は、バッチを使用して、転記するトランザクション タイプの一覧を監視します。 モニターは、転記するタイプのトランザクションを検出すると、そのトランザクション タイプを使用して、それらのトランザクションを転記するバッチを生成します。 作成されるバッチは、そのトランザクション タイプのユーザー インターフェイスの使用時に作成されるバッチと同じタイプです。 トランザクション バッチが完了したら、転記の準備完了の監視によって、リストは処理の結果で更新されます。 また、バッチおよび元のトランザクションへのリンクを追加します。

#### <a name="use-the-ready-to-post-page-to-process-transactions"></a>転記準備完了ページを使用して、トランザクションを処理します。

1. **システム管理** &gt; **定期処理タスク** &gt; **バッチ ジョブを送信する準備** を選択し、**送信する準備** ページを開きます。
2. **転記監視の作成** を選択し、定期的なバッチが実行されるように、バッチ パラメーターを設定します。 転記のためのバッチ処理を開始するには、法人ごとに 1 回のみ、このステップを完了する必要があります。
3. **新規作成** を選択し、デモ データ ジョブの名前を入力します。 ジョブ名は、すべての会社で一意である必要があります。
4. **明細行を追加** を選択してトランザクション タイプを追加します。
5. トランザクションのターゲットを選択します。 仕訳帳については、ターゲットは **転記** になります。 その他のトランザクションでは、ターゲットは、トランザクション タイプによって異なります。
6. 処理されるトランザクション (使用可能な場合) を制限するには、開始日と終了日 (つまり、日付範囲) を指定します。
7. 処理されるトランザクション (使用可能な場合) を制限するには、"開始" ドキュメントと "終了" ドキュメント (つまり、ドキュメントの範囲) を指定します。
8. **明細行を追加** を選択してト追加のランザクション タイプを追加します。 同じラインに複数のタイプを使用することができます。
9. **マークを転記する準備ができました** を選択します。 バッチの状態が **未処理** から **準備完了** に変更され、転記モニターが各明細行の処理を開始します。
10. ドキュメントをすぐに処理するには、**ドキュメントの処理** を選択します。 バッチの状態が **スケジュール済** に変更され、転記モニターを使用せずにバッチが開始されます。

バッチを実行しているときは、ステータスは **進行中** に変更されます。

バッチが完了したら、ステータスは、結果にもとづいて、**成功** または **エラー** に変更されます。 転記の結果は、ページの下部に表示されます。

#### <a name="use-the-ready-to-post-entity-to-process-transactions"></a>転記準備完了エンティティを使用して、トランザクションを処理します。

**デモ データ転記** という名前のエンティティを転記したいドキュメント タイプの一覧からインポートすることができます。 エンティティは、**投稿準備完了** ページにデモ データのジョブを作成します。 転記モニターを開始した場合、トランザクションはエンティティを使用してデータをインポートした後に自動的に転記されます。

**投稿準備完了** エンティティに次の列が表示されます。

| 円柱 | 目的 |
|--------|---------|
| DemoDataJob | 実行するデモ データ ジョブの一意の ID。 1 つのジョブに属するすべての明細行に同一の ID を使用します。 |
| LineNum | タスクが実行される順序。 |
| DataProjectId | **投稿準備完了** エンティティを含むデータ プロジェクトへのリンク。 この情報はエクスポート専用です。 |
| DemoDataJobStatus | デモ データ プロジェクトの状態。 この情報はエクスポート専用です。 |
| 書類 | 処理するドキュメント タイプ。 |
| DocumentTarget | 実行するプロセス。 仕訳帳については、ターゲットは **転記** である必要があります。 販売注文などのトランザクションについては、ターゲットは、タスクを追加する際にページに表示されるオプションと一致します。 |
| EndDate | 処理されるトランザクションを制限するオプションの終了日です。 |
| FromDocument | 処理されるトランザクションを制限するオプションの「from」ドキュメント。 |
| ProcessOnImport | 値を **はい** に変更すると、デモ データのジョブが **準備完了** に設定され、プロセス モニターはそれを自動的にピッキングします。 必要なアクションはありません。 |
| StartDate | 処理されるトランザクションを制限するオプションの開始日です。 |
| ToDocument | 処理されるトランザクションを制限するオプションの「to」ドキュメント。 |

すべてのトランザクション エンティティの後でデータ プロジェクトの最後に **投稿準備完了** エンティティを挿入します。 データ プロジェクトで、トランザクション エンティティに使用される順序番号より大きい順序番号を指定します。

複数のトランザクションが混在している場合、一部のトランザクションを処理する必要がある一方で、その他のトランザクションは処理できないため、日付とドキュメントの範囲を使用し処理されるトランザクションを制限します。 範囲を使用できない場合は、未転記のトランザクションの個別のデータ パッケージを使用する必要があります。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

