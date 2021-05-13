---
title: Dynamics 365 Supply Chain Management 10.0.19 のプレビュー (2021 年 7 月)
description: このトピックでは、Dynamics 365 Supply Chain Management 10.0.19 の新機能または変更された機能について説明します。
author: kamaybac
ms.date: 04/23/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-23
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8bb4a7c8085b40ab3eca72675dbe7a3be412d8c1
ms.sourcegitcommit: 2eb7a9ae544f504155657c5c584cbac66c21dba4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/29/2021
ms.locfileid: "5961684"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10019-july-2021"></a>Dynamics 365 Supply Chain Management 10.0.19 のプレビュー (2021 年 7 月)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

このトピックでは、バージョン 10.0.19 の Microsoft Dynamics 365 Supply Chain Management プレビューの新機能または変更された機能について一覧表示します。 このバージョンには 10.0.837 のビルド番号が含まれており、次のように使用できます。

- **リリースのプレビュー:** 2021 年 4 月
- **リリースの一般提供 (手動更新):** 2021 年 6 月
- **リリースの一般提供 (自動更新):** 2021 年 7 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 *機能* 列には、[リリース計画](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) へのリンクがあり、各機能の公式リリース日を確認できます。 *詳細情報* 列には、関連ドキュメントへのリンクが表示されています。

これらの機能のほとんどは、使用する前に[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用して有効にする必要があります。 一覧表示された機能の一部はプレビューのままですが、他の機能はすでに一般提供されている可能性があります。

| 機能領域 | 機能 | 詳細 |
|---|---|---|
| 在庫および物流 | [連絡担当者データ エンティティのエクスポートの最適化](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization)  | *使用不可* |
| 在庫および物流 | [スケール単位を使用する倉庫の実行機能の差分機能強化](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/incremental-enhancements-warehouse-execution-capabilities-scale-units) |[メッセージ プロセッサのメッセージ](../cloud-edge/cloud-edge-message-processor-messages.md)<br><br>[倉庫在庫調整](../cloud-edge/cloud-edge-warehouse-inventory-adjustment.md)<br><br>[クラウドおよびエッジのスケール ユニットに対する倉庫管理ワークロード](../cloud-edge/cloud-edge-workload-warehousing.md) |
| 在庫および物流 | [販売見積ページのドキュメントの序文フィールドおよびドキュメントの結びフィールドのルックアップ機能](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | *使用不可* |
| 在庫および物流 | [カスタム ハードウェア上のエッジのスケール ユニットを使用した倉庫の実行](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-edge-scale-units-custom-hardware) | [LBD を使用してカスタム ハードウェアにエッジのスケール ユニットを配置する](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| 製造 | [カスタム ハードウェア上のエッジのスケール ユニットを使用した製造実行](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-edge-scale-units-custom-hardware) | [LBD を使用してカスタム ハードウェアにエッジのスケール ユニットを配置する](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| 計画 | クエリ ベースの計画オーダーの作成 | [計画オーダーの確定](../master-planning/planning-optimization/planned-order-firming.md) |
| 製品情報管理 | [バリアント修正候補ページの改善](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/variant-suggestions-page-improvements) | [事前定義された製品バリアントの作成](../pim/tasks/create-predefined-product-variants.md) |

## <a name="new-and-updated-documentation-resources"></a>新しいドキュメント リソースおよび更新されたドキュメント リソース

次のヘルプ トピックが最近追加されたか大幅に更新されました。 前のセクションに示したように、このリリースで追加された新しい機能に関連するとは限りませんが、既存の機能をさらに活用するために役立つ場合があります。

| 機能領域 | 新規または更新されたトピック |
|---|---|
| エンジニアリング変更管理 | [エンジニアリング変更管理 FAQ](../engineering-change-management/change-management-faq.md) |
| 調達 | [仕入先からのカテゴリ要求](../procurement/category-requests-from-vendors.md) |
| 製品情報管理 | [測定単位の管理](../pim/tasks/manage-unit-measure.md)<br><br>[製品コンフィギュレーション モデルの計算](../pim/config-model-calculations.md) |
| 生産管理 | [ジョブ ID の統合番号順序](../production-control/unified-job-ids.md) |
| 輸送管理 | [LTL クラス](../transportation/ltl-class.md)<br><br>[NMFC コード](../transportation/nmfc-codes.md) |
| 倉庫管理 | [倉庫バッチおよびシリアル予約階層のトラブルシューティング](../warehousing/troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md) |
| 倉庫管理、ウェーブの作成と処理 | [ウェーブの作成と処理](../warehousing/wave-processing.md)<br><br>[ウェーブ処理用の倉庫パラメーター](../warehousing/wave-warehouse-parameters.md)<br><br>[ウェーブ テンプレート](../warehousing/wave-templates.md)<br><br>[ウェーブ配賦](../warehousing/wave-allocation-method.md)<br><br>[ウェーブ中の作業作成のスケジュール](../warehousing/configure-wave-schedule-work-creation.md)<br><br>[コンテナー詰め](../warehousing/wave-containerization.md)<br><br>[ウェーブの実行通知](../warehousing/wave-execution-notifications.md) |

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations アプリのプラットフォーム更新プログラム

Microsoft Dynamics 365 Supply Chain Management 10.0.19 には、Platform updates が含まれています。 詳細については、[Finance and Operations アプリ バージョン 10.0.19 のプラットフォーム更新プログラム (2021 年 7 月)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正

10.0.19 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=575415) を参照してください。

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
