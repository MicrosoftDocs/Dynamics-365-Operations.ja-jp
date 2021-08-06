---
title: Dynamics 365 Supply Chain Management バージョン 10.0.19 (2021 年 6 月) の新機能および変更された機能
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
ms.openlocfilehash: 98f9fffcbf93871de302a0d8b4b9675889ef5e40
ms.sourcegitcommit: 908a85987b604a7782407da70fb70ef75c07989f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/19/2021
ms.locfileid: "6641131"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-version-10019-june-2021"></a>Dynamics 365 Supply Chain Management バージョン 10.0.19 (2021 年 6 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management バージョン 10.0.19 の新機能または変更された機能について一覧表示します。 このバージョンには 10.0.837 のビルド番号が含まれており、次のように使用できます。

- **リリースのプレビュー:** 2021 年 4 月
- **リリースの一般提供 (手動更新):** 2021 年 6 月
- **リリースの一般提供 (自動更新):** 2021 年 6 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 *機能* 列には、[リリース計画](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) へのリンクがあり、各機能の公式リリース日を確認できます。 *詳細情報* 列には、詳細情報や関連ドキュメントへのリンクが表示されます。

これらの機能のほとんどは、使用する前に[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用して有効にする必要があります。

| 機能領域 | 機能 | 詳細 |
|---|---|---|
| 在庫および物流 | [連絡担当者データ エンティティのエクスポートの最適化](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization)  | この機能を有効にすると、参照データを変更しても、関連する連絡先が次の増分エクスポートに含まれることはありません。 この機能を無効にすると、参照データに変更があると、関連する連絡先が次の増分エクスポートに含まれます。 |
| 在庫および物流 | [スケール単位を使用する倉庫の実行機能の差分機能強化](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/incremental-enhancements-warehouse-execution-capabilities-scale-units) |[メッセージ プロセッサのメッセージ](../cloud-edge/cloud-edge-message-processor-messages.md)<br><br>[倉庫在庫調整](../cloud-edge/cloud-edge-warehouse-inventory-adjustment.md)<br><br>[クラウドおよびエッジのスケール ユニットに対する倉庫管理ワークロード](../cloud-edge/cloud-edge-workload-warehousing.md) |
| 在庫および物流 | [販売見積ページのドキュメントの序文フィールドおよびドキュメントの結びフィールドのルックアップ機能](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | この機能により、**販売見積** ページの **ドキュメントの序文** フィールドと **ドキュメントの結び** フィールドにルックアップ機能が追加されます。<br><br>この機能は、既定で有効になっています。 |
| 在庫および物流 | [カスタム ハードウェア上のエッジのスケール ユニットを使用した倉庫の実行](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-edge-scale-units-custom-hardware) | [LBD を使用してカスタム ハードウェアにエッジのスケール ユニットを配置する](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| 製造 | [カスタム ハードウェア上のエッジのスケール ユニットを使用した製造実行](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-edge-scale-units-custom-hardware) | [LBD を使用したカスタム ハードウェアへのエッジのスケール ユニットの展開](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| 計画 | [計画最適化の無限キャパシティ スケジューリング](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/schedule-infinite-capacity-support-planning-optimization) | この機能により、計画の最適化において、無限容量を持つキャパシティ スケジューリングが有効になります。 この機能がない場合、計画製造オーダーは、スケジューリング タイム フェンスに関係なく、リリースされた製品の在庫リード タイムからリード タイムを取得します。 |
| 計画 | クエリ ベースの計画オーダーの作成 | [計画オーダーの確定](../master-planning/planning-optimization/planned-order-firming.md) |
| 製品情報管理 | [バリアント修正候補ページの改善](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/variant-suggestions-page-improvements) | [事前定義された製品バリアントの作成](../pim/tasks/create-predefined-product-variants.md) |

## <a name="feature-enhancements-included-in-this-release"></a>このリリースに含まれる機能拡張

次の表に、このリリースに含まれる機能拡張の一覧を示します。 これらの機能は、それぞれ既存の機能を段階的に改善します。 これらは拡張機能にすぎないため、[リリース計画](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) には記載されません。 ただし、これらの拡張機能が既存のカスタマイズや基本設定と競合しないように、各機能は (特に断りのない限り) 既定でオフになっています。 これらの機能を使用する場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) で明示的にそれらを有効にする必要があります。

| 機能領域 | 機能&nbsp;管理の機能&nbsp;名&nbsp; | 詳細 |
|---|---|---|
| 販売とマーケティング | 販売履歴クリーンアップ パフォーマンスの向上 | 販売履歴のクリーンアップは、大量の販売更新がある環境で頻繁に実行されない場合、時間がかかることがあります。 時間を短縮し、信頼性を向上させるために、この機能では、限られた期間で実行されるバッチにクリーンアップを分割します。 可能であれば、データベース機能を活用して、ロックを最小限にし、クリーンアップ中にトランザクション テーブルが結合しないようにします。 |
| 販売とマーケティング | 入荷希望日を会社間注文の確認日で更新する | この機能により、会社間直納を使用する場合に、販売日フィールドおよび購入日フィールドの値に何が起こるかを管理できます。 システムが要求日を更新するか、更新をスキップするかを選択できます。 更新をスキップした場合、要求日は顧客が要求したものを表します。 更新を有効にした場合、(配送日管理を使用している場合) 要求日は、最初に顧客が要求したものだけを表します。 配送日管理は、*なし* 以外の場合、最初に要求されたものを変更します。 このオプションは、会社間仕入先または顧客設定で新しい **入荷希望日を確定日で更新** 設定を使用して設定できます。<br><br>この機能が無効の場合、システムは元の販売注文で入荷希望日を配送日管理ルールに基づいて上書きしますが、要求出荷日はそのままです。 |
| 倉庫管理 | 倉庫へのリリース時に数量を最も近い販売単位に切り捨てる | この機能により、倉庫へのリリース時に注文数量を制限できるオプションが追加されます。 有効にすると、注文数量は最も近い整数の販売単位に切り捨てされ、1 販売単位未満の注文はリリースを拒否されます。 |
| 倉庫管理 | 組織全体の "作業作成のスケジュール" ウェーブ メソッド | この機能を有効にすると、*作業作成のスケジュール* ウェーブ メソッドは、すべての法人に並行して実行されるように設定されます。 いくつかの追加設定も影響を受けます。 詳細については、[ウェーブ中の作業作成のスケジュール](../warehousing/configure-wave-schedule-work-creation.md) を参照してください。 |

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

Microsoft Dynamics 365 Supply Chain Management 10.0.19 には、Platform updates が含まれています。 詳細については、[Finance and Operations アプリ バージョン 10.0.19 のプラットフォーム更新プログラム (2021 年 6 月)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19.md) を参照してください。

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
