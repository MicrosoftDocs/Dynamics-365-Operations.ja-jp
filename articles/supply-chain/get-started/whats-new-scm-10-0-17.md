---
title: Dynamics 365 Supply Chain Management 10.0.17 の新機能または変更された機能 (2021 年 4 月)
description: このトピックでは、Dynamics 365 Supply Chain Management 10.0.17 の新機能または変更された機能について説明します。
author: kamaybac
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: fd8c306dd6c3aeb7ef41b4eb3f6f8bad040035c2
ms.sourcegitcommit: 9283caad2d0636f98579c995784abec19fda2e3f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935608"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10017-april-2021"></a>Dynamics 365 Supply Chain Management 10.0.17 の新機能または変更された機能 (2021 年 4 月)

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management バージョン 10.0.17 の新機能または変更された機能について一覧表示します。 このバージョンには 10.0.761 のビルド番号が含まれており、次のように使用できます。

- **リリースのプレビュー:** 2021 年 2 月
- **リリースの一般提供 (自己更新):** 2021 年 3 月
- **リリースの一般提供 (自動更新):** 2021 年 4 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

このリリースでは次の機能が含まれています。  [リリース計画](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) へのリンクに従って、各機能の公式リリース日を確認してください。

これらの機能のほとんどは、使用する前に[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用して有効にする必要があります。

### <a name="asset-management"></a>資産管理

- [メンテナンス計画の実行中に作業指示書をグループ化するルールの適用](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/apply-rules-grouping-work-orders-while-running-maintenance-plan)<br> - 詳細については、[ワークフローの作成](../asset-management/preventive-and-reactive-maintenance/creating-work-orders.md) を参照してください。

- [顧客に対するメンテナンス作業への請求](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/bill-customers-maintenance-work)<br> - 詳細については、[顧客所有の資産のメンテナンスの請求](../asset-management/integration-to-project-management-and-accounting/customer-billing.md) を参照してください。

- [資産カウンターの値の累計に基づくメンテナンスの計画](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/plan-maintenance-based-accumulated-asset-counter-values)<br> - 詳細については、[メンテナンス計画](../asset-management/preventive-and-reactive-maintenance/maintenance-plans.md) を参照してください。

### <a name="inventory-and-logistics"></a>在庫および物流

- [自動化倉庫プロセス (以前の MHAX) における材料取り扱い設備の統合フレームワーク](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/integration-framework-material-handling-equipment-automated-warehouse-processes-previously-mhax)<br> - 詳細については、[材料取り扱い設備のインターフェイス (MHAX)](../warehousing/mhax.md) を参照してください。

- [陸揚原価](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/landed-cost)<br> - 詳細については、[陸揚原価モジュール](../landed-cost/landed-cost-overview.md) を参照してください。

- [梱包対保管分析コード](/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/packing-vs.-storage-dimensions)<br> - 詳細については、[梱包と保管へのさまざまな分析コードの設定](../warehousing/packing-vs-storage-dimensions.md) を参照してください。

- [在庫および物流の保存済みビュー](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/saved-views-inventory-logistics)<br> - 詳細については、[Supply Chain Management の標準の保存済みビュー](saved-views-scm.md) を参照してください。

- [倉庫作業作成のスケジュール](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/schedule-warehouse-work-creation)<br> - 詳細については、[サイクル中に作業の作成をスケジュールする](../warehousing/configure-wave-schedule-work-creation.md) を参照してください。

- [在庫標準原価再評価伝票に対する既定の財務分析コードの設定](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/set-default-financial-dimensions-inventory-standard-cost-revaluation-vouchers)<br> - 詳細については、[標準原価の更新の管理](../cost-management/manage-standard-cost-updates.md) を参照してください。

- [小型小包の出荷 (SPS)](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/small-parcel-shipping-sps)<br> - 詳細については、[小型パーセルの出荷](../warehousing/small-parcel-shipping.md) を参照してください。

- [スケール単位をクラウドに含む倉庫の実行](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-scale-units-cloud)<br> - 詳細については、[クラウドとエッジのスケールユニットの倉庫管理ワークロード](../cloud-edge/cloud-edge-workload-warehousing.md) と [クラウドとエッジのスケールユニットの倉庫オーダー](../cloud-edge/cloud-edge-warehouse-order.md) を参照してください。

- [倉庫管理モバイル アプリケーション](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application)<br> - 詳細については、 [倉庫管理アプリをインストールして接続](../warehousing/install-configure-warehouse-management-app.md) および[モバイル デバイス ユーザー設定](../warehousing/mobile-device-user-settings.md) を参照してください。

- ウェーブの実行通知<br> - 詳細については、[ウェーブ処理の通知](../warehousing/wave-execution-notifications.md) を参照してください

### <a name="manufacturing"></a>製造

- [生産フロア実行インターフェイスの資産管理機能](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/asset-management-capabilities-production-floor-execution-interface)<br> - 詳細情報については、[生産現場の実行インターフェースを構成する](../production-control/production-floor-execution-configure.md) を参照してください。

- [スケール単位をクラウドに含む製造の実行](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-scale-units-cloud)<br> - 詳細については、[クラウドおよびエッジのスケール ユニットの製造実行ワークロード](../cloud-edge/cloud-edge-workload-manufacturing.md) を参照してください。

- [生産材料の既定の予約原則の上書き](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/override-default-reservation-principle-materials-production)<br> - 詳細については、[生産材料の既定の予約原則の上書き](../production-control/override-default-reservation-principle.md) を参照してください。

- [製造制御の保存済みビュー](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/saved-views-production-control)<br> - 詳細については、[Supply Chain Management の標準の保存済みビュー](saved-views-scm.md) を参照してください。

- ジョブ ID の統合番号順序<br> - 詳細については、[ジョブ ID の統合番号順序](../production-control/unified-job-ids.md)を参照してください。

### <a name="planning"></a>計画

- [計画の最適化に対する補充タイム フェンスのサポート](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/coverage-time-fence-support-planning-optimization)<br> - 詳細については、[補充タイム フェンス](../master-planning/planning-optimization/coverage-time-fence.md) を参照してください。

- [計画最適化の予測下位モデルのサポート](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/forecast-submodel-support-planning-optimization)<br> - 詳細については、[需要予測を使ったマスター プラン](../master-planning/planning-optimization/demand-forecast.md) を参照してください。

- [計画の最適化の購買要求サポート](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/purchase-requisition-support-planning-optimization)<br> - 詳細については、[購買要求](../master-planning/planning-optimization/purchase-requisitions.md) を参照してください。

- [計画オーダー用に保存されているビュー](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/saved-views-planned-orders)<br> - 詳細については、[Supply Chain Management の標準の保存済みビュー](saved-views-scm.md) を参照してください。

### <a name="product-information-management"></a>製品情報管理

- [既存の製品の変更管理の有効化](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enable-change-management-existing-products)<br> - 詳細については、[既存の製品の変更管理を有効にする](../engineering-change-management/change-management-existing-products.md) を参照してください。

## <a name="new-and-updated-documentation-resources"></a>新しいドキュメント リソースおよび更新されたドキュメント リソース

次のヘルプ トピックが最近追加されたか大幅に更新されました。 前のセクションに示したように、このリリースで追加された新しい機能に関連するとは限りませんが、既存の機能をさらに活用するために役立つ場合があります。

### <a name="cost-management"></a>原価管理

- [コスト管理のトラブルシューティング](../cost-management/troubleshoot-costmanagement.md)

### <a name="asset-management"></a>資産管理

- [資産管理モバイル ワークスペースの設定](../asset-management/set-up-asset-management-mobile.md)

### <a name="inventory-and-logistics"></a>在庫および物流

- [倉庫トランザクション用の製品フィルターのコンフィギュレーション](../warehousing/filters-and-filter-codes.md)

- [部分的な場所の循環棚卸](../warehousing/partial-location-cycle-counting.md)

- [ピッキング行のグループ化](../warehousing/pick-line-grouping.md)

- [在庫操作のトラブルシューティング](../inventory/troubleshoot-inventory-operations.md)

- [倉庫のスロッティング](../warehousing/warehouse-slotting.md)

### <a name="manufacturing"></a>製造

- [生産現場の実行インターフェースをデザインする](../production-control/production-floor-execution-tabs.md)

### <a name="planning"></a>計画

- [会社間計画](../master-planning/planning-optimization/Intercompany-planning.md)

- [計画最適化を使用した在庫マーキング](../master-planning/planning-optimization/marking.md)

- [生産計画](../master-planning/planning-optimization/production-planning.md)

- [マスター プランの購買要求](../master-planning/planning-optimization/purchase-requisitions.md)

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations アプリのプラットフォーム更新プログラム

Microsoft Dynamics 365 Supply Chain Management 10.0.17 には、Platform updates が含まれています。 詳細については、[アプリのバージョン 10.0.17 (2021 年 4 月) のプラットフォーム アップデート](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md)Finance and Operations を参照してください。

### <a name="bug-fixes"></a>バグ修正

10.0.17 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=551039&dbType=3&qc=91219e7c3fc585acb17b810c915c3cbea499403538520c40e54de43a53aea6a8) を参照してください。

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
