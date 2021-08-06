---
title: Dynamics 365 Supply Chain Management 10.0.20 (2021 年 8 月) の新機能または変更された機能
description: このトピックでは、Dynamics 365 Supply Chain Management 10.0.20 の新機能または変更された機能について説明します。
author: kamaybac
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 09cdb039b9bde3f97db012f1aaaeaf4c8a7df944
ms.sourcegitcommit: 908a85987b604a7782407da70fb70ef75c07989f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/19/2021
ms.locfileid: "6641059"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10020-august-2021"></a>Dynamics 365 Supply Chain Management 10.0.20 (2021 年 8 月) の新機能または変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management バージョン 10.0.20 の新機能または変更された機能について一覧表示します。 このバージョンには 10.0.886 のビルド番号が含まれており、次のように使用できます。

- **リリースのプレビュー:** 2021 年 5 月
- **リリースの一般提供 (手動更新):** 2021 年 7 月
- **リリースの一般提供 (自動更新):** 2021 年 8 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 *機能* 列には、[リリース計画](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) へのリンクがあり、各機能の公式リリース日を確認できます。 *詳細情報* 列には、詳細情報や関連ドキュメントへのリンクが表示されます。

これらの機能のほとんどは、使用する前に[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用して有効にする必要があります。

| 機能領域 | 機能 | 詳細 |
|---|---|---|
| 在庫&nbsp;および&nbsp;物流 | [販売注文詳細のパフォーマンスの向上](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | この機能により、販売注文、特に多数の明細行を含む注文を開くときに、ユーザー インターフェイスの応答性が向上します。 |
| 製造 | [プロセス自動化フローを呼び出して品質指示を作成する](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/invoke-process-automation-flows-create-quality-orders) | [プロセス自動化フローを呼び出して品質指示を作成する](../production-control/process-automation-quality-orders.md ) |
| 製造 | [製造用の強化された生産フロア実行インターフェイス](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-manufacturing) | [生産現場の実行インターフェースを構成する](../production-control/production-floor-execution-configure.md) |
| 製品情報管理 | [フォーミュラとその成分の変更の管理](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/engineering-change-management-support-process-manufacturing) | [フォーミュラとその成分の変更の管理](../engineering-change-management/manage-formula-changes.md) |
| 製品情報管理 | [製品準備完了チェック](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/product-readiness-checks) | [製品準備完了](../engineering-change-management/product-readiness.md) |

## <a name="feature-enhancements-included-in-this-release"></a>このリリースに含まれる機能拡張

次の表に、このリリースに含まれる機能拡張の一覧を示します。 これらの機能は、それぞれ既存の機能を段階的に改善します。 これらは拡張機能にすぎないため、[リリース計画](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) には記載されません。 ただし、これらの拡張機能が既存のカスタマイズや基本設定と競合しないように、各機能は (特に断りのない限り) 既定でオフになっています。 これらの機能を使用する場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) で明示的にそれらを有効にする必要があります。

| 機能領域 | 機能&nbsp;管理の機能&nbsp;名&nbsp; | 詳細 |
|---|---|---|
| マスター プラン | 計画の最適化のマイナス在庫日数 | この機能により、計画の最適化では、補充グループで定義された **マイナス在庫日数** パラメーターに基づいて遅延許容範囲を考慮できます。 |
| マスター プラン | 調整された需要予測の並列承認 | この機能により、**調整された需要予測** ページから調整済需要予測を並行して承認できます。 この機能の目的は、多数の予測が承認されている場合のパフォーマンスを向上させることです。 承認時に、ユーザーは、承認するダイアログで **スレッド数** を指定できます。 |
| マスター プラン | (プレビュー) 計画バルク オーダーおよび梱包バッチ オーダーのバッチ処理可能な確定と連結 | この機能を使用すると、バッチ ジョブを使用して、計画バルク オーダーと梱包オーダーを確定および連結できます。 |
| 生産管理 | 汎用工順のコピー | この機能により、工順コピー機能が強化され、ユーザーは品目固有ではない工順をコピーできます。 工順コピー機能を使用して品目にまだ割り当てられていない工順を上書きした後で、システムはすべての関連情報 (サイト、工順グループ、リソース要件、各種の時間など) を更新できます。 |
| 生産管理 | 工順工程の変更時に関連するリソース要件を更新する | システムはこの機能により、既存の工順ステップの工程をユーザーが変更した後に、関連するリソース要件を更新できます。 |
| 製品情報管理 | タイムアウトを回避するための部品表レポートの前処理 | この機能により、部品表レポートが前処理されます。 これにより、レポートに対するデータ負荷が大きい場合にタイムアウトの問題が回避されます。 |
| 調達 | 調達関連ワークフローのリセットを有効にする | このプレビュー機能を使用すると、次のワークフローをドラフト状態 (発注書、仕入先変更、購買要求) にリセットできます。 |
| 輸送管理 | 運賃請求書を破棄する際に仕入先請求仕訳帳の作成を有効にする | この機能を有効にすると、対応する仕入先請求仕訳帳は、支払 - 仕入先オプションを使用している場合に、調整理由でのみ作成されます。 それ以外の場合、常に請求仕訳帳が作成されます。 |
| 倉庫管理 | 補充ジョブに選択されているテンプレートの検証 | この機能により、ユーザーが補充ジョブを設定する際に有効な補充テンプレートを選択できます。 これにより、ユーザーはテンプレートを使用せずに補充ジョブを作成したり、補充作業が作成されず、処理に時間がかかる可能性がある、タイプ *ウェーブ需要* のテンプレートを選択したりできなくなります。 |

## <a name="new-and-updated-documentation-resources"></a>新しいドキュメント リソースおよび更新されたドキュメント リソース

次のヘルプ トピックが最近追加されたか大幅に更新されました。 前のセクションに示したように、このリリースで追加された新しい機能に関連するとは限りませんが、既存の機能をさらに活用するために役立つ場合があります。

| 機能領域 | 新規または更新されたトピック |
|---|---|
| エンジニアリング変更管理 | [製品ライフサイクルの状態とトランザクション](../engineering-change-management/product-lifecycle-state-transactions.md) |
| 在庫管理 | [在庫の視覚化アドイン](../inventory/inventory-visibility.md)<br><br>[品質および不適合管理の概要](../inventory/quality-management-processes.md) (および関連するすべての品質管理トピック) |
| 調達 | [仕入先証明の管理](../../finance/public-sector/manage-vendor-certification.md) |
| 生産管理 | [生産現場の実行インターフェースのスタイル](../production-control/production-floor-execution-styles.md) |
| 倉庫管理 | [Warehouse Management モバイル アプリのステップ アイコンとタイトルの割り当て](../warehousing/step-icons-titles.md)<br><br>[手動在庫移動の繰延処理](../warehousing/deferred-processing-manual-inventory-movement.md) |

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations アプリのプラットフォーム更新プログラム

Microsoft Dynamics 365 Supply Chain Management 10.0.20 には、Platform updates が含まれています。 詳細については、[Finance and Operations アプリ バージョン 10.0.20 のプラットフォーム更新プログラム (2021 年 7 月)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正

10.0.20 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=586707&dbType=3&qc=d0dad8eee2af234e8c288e2a7df14c579004518673d014be511f900cfed008f8) を参照してください。 

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: 2021 リリースのウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2021 リリース ウェーブ 1 プラン](/dynamics365-release-plan/2021wave1/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-supply-chain-management-features"></a>削除済みおよび非推奨の Supply Chain Management 機能

[Dynamics 365 Supply Chain Management の削除済みおよび非推奨の機能](removed-deprecated-features-scm-updates.md)トピックは、Supply Chain Management で削除または非推奨となる予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Supply Chain Management の削除済みまたは非推奨の機能](removed-deprecated-features-scm-updates.md)のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
