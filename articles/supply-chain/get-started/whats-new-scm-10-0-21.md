---
title: Dynamics 365 Supply Chain Management 10.0.21 (2021 年 10 月) のプレビュー
description: このトピックでは、Dynamics 365 Supply Chain Management 10.0.21 の新機能または変更された機能について説明します。
author: kamaybac
ms.date: 08/02/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 517411512760374f1d1fd3b8ea3615563c47202c2e847569d00cb17a94657630
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012040"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10021-october-2021"></a>Dynamics 365 Supply Chain Management 10.0.21 (2021 年 10 月) のプレビュー

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

このトピックでは、バージョン 10.0.21 の Microsoft Dynamics 365 Supply Chain Management プレビューの新機能または変更された機能について一覧表示します。 このバージョンには 10.0.960 のビルド番号が含まれており、次のように使用できます。

- **リリースのプレビュー:** 2021 年 8 月
- **リリースの一般提供 (手動更新):** 2021 年 9 月
- **リリースの一般提供 (自動更新):** 2021 年 10 月

## <a name="known-deployment-issue"></a>配置に関する既知の問題
IaaS にリリース 10.0.21 を配置する場合、次のような配置警告が表示される場合があります。

**警告コード:** 95017

**警告メッセージ:** スクリプト [SetupDiagnostics] が VM に対して実行に失敗

警告があっても配置は機能しますが、Lifecycle Services (LCS) では次のような既知の問題が発生する可能性があります。

-   **環境の監視** ページでは、**詳細バージョン情報の表示** リンクは表示されません。したがって、環境にインストールされているモジュールの特定のバージョンは表示されません。 このデータがないと、修正プログラムを適用するプロセスがこのデータを使用して、モジュール バージョンの前提条件が満たされていることを確認するため、後続の修正プログラムが失敗することがあります。 PEAP/プレビュー ビルドを生産で使用したり、修正プログラムを適用することができないため、影響は最小限に抑える必要があります。
-   SQL インサイトの **環境監視** ページの **パフォーマンス メトリックス** タブと **インデックス分析** タブでは、データは表示されません。 その他の **環境監視** 機能は、意図したとおりに機能します。
-   **フル システム診断** ページにはアクセスできません。 夜間のコレクター実行のステータスとそのルールによって検出された問題に関する関連データも表示されません。

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 *機能* 列には、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) へのリンクがあり、各機能の公式リリース日を確認できます。 *詳細情報* 列には、詳細情報や関連ドキュメントへのリンクが表示されます。

これらの機能のほとんどは、使用する前に[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用して有効にする必要があります。 一覧表示された機能の一部はプレビューのままですが、他の機能はすでに一般提供されている可能性があります。

| 機能領域 | 機能 | 詳細 |
|---|---|---|
| 在庫&nbsp;および&nbsp;物流 | [Dynamics 365 Supply Chain Management のグローバル在庫会計アドイン](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/global-inventory-accounting-add-in-dynamics-365-supply-chain-management) | [グローバル在庫会計ホーム ページ](../global-inventory-accounting/global-inventory-accounting-home.md) |
| 在庫&nbsp;および&nbsp;物流 | [相手勘定に接続されたコードを使用した手当調整の転記](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/post-on-hand-adjustments-using-configurable-reason-codes-connected-offset-accounts) | [在庫棚卸の理由コード](../warehousing/reason-codes-for-counting-journals.md) |
| 在庫&nbsp;および&nbsp;物流 | [販売見積参照データ エクスポート ポリシー](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy) | 見積書で参照されているデータを変更すると、それらの見積書 (または明細行) が次の増分エクスポートに含まれるかどうかを選択します。 そのような見積書または明細行を含めない場合は、増分エクスポートがより迅速に実行します。<br><br>この機能は、**変更追跡中に販売見積参照データをスキップ** という設定を **売掛金勘定パラメーター** ページに追加します。 |
| 在庫&nbsp;および&nbsp;物流 | [GS1 形式標準を使用した倉庫内のバーコードのスキャン](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | *間もなく公開*<!-- KFM: Add doc link when ready. --> |
| 在庫&nbsp;および&nbsp;物流 | シールド入札 <!-- KFM: Add RP link when available --> | *間もなく公開*<!-- KFM: Add doc link when ready. --> |
| 在庫&nbsp;および&nbsp;物流 | [リベート管理の控除および Catch Weight の強化](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/deduction-catch-weight-enhancements-rebate-management) | [控除ワークベンチを使用した控除の管理](../rebate-management/deduction-workbench.md )<br><br>[リベートの処理、確認、および転記](../rebate-management/process-review-post.md)<br><br>[リベート管理取引](../rebate-management/rebate-management-deals.md) |
| 在庫&nbsp;および&nbsp;物流 | [倉庫アプリのステップ指示](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | *間もなく公開*<!-- KFM: Add doc link when ready --> |
| 在庫&nbsp;および&nbsp;物流 | [陸揚原価の作業の分割と追跡の更新](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/work-breaks-tracking-updates-landed-cost) | [プット アウェイの更新追跡](../landed-cost/update-tracking-putaway.md )<br><br>[輸送中の商品の処理](../landed-cost/in-transit-processing.md) |
| マスター プラン | [計画の最適化のマイナス在庫日数](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/negative-days-support-planning-optimization) | [遅延許容範囲 (マイナス日数)](../master-planning/planning-optimization/delay-tolerance.md) |

## <a name="feature-enhancements-included-in-this-release"></a>このリリースに含まれる機能拡張

次の表に、このリリースに含まれる機能拡張の一覧を示します。 これらの機能は、それぞれ既存の機能を段階的に改善します。 これらは拡張機能にすぎないため、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) には記載されません。 ただし、これらの拡張機能が既存のカスタマイズや基本設定と競合しないように、各機能は (特に断りのない限り) 既定でオフになっています。 これらの機能を使用する場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) で明示的にそれらを有効にする必要があります。

| 機能領域 | 機能&nbsp;管理の機能&nbsp;名&nbsp; | 詳細 |
|---|---|---|
| 原価管理 | 在庫決算の進捗状況の詳細 | このプレビュー機能により、在庫決算の進捗を詳細に表示できます。 |
| マスター プラン | (プレビュー) 計画最適化に対して優先順位によって推進される MRP のサポート | この計画最適化のプレビュー機能を使用すると、再発注時点での計画の優先順位によってマスター プラン駆動型を有効にできます。 強調表示される変更には、販売注文明細行、発注書明細行、需要予測、および計画オーダーの **計画の優先順位**; 再発注時点の **品目補充** フィールド; 計画の優先順位設定を制御するマスター プランの設定フォーム; および計画の優先順位を設定および適用する計画最適化計算ロジックが含まれます。 |
| 調達 | 複数の購買要求がワークフロー内にある場合に一般予算引当の過剰消費を防止する | このプレビュー機能により、一般予算引当行の残りの残高を超える購買要求をユーザーが送信および承認する際のエラー チェックが向上します。 これにより、複数の購買要求がワークフローに含まれる場合に、一般予算引当の超過消費を防ぐのに役立ちます。 |
| 生産管理 | 生産フロア実行インターフェイスの完全なシリアル番号、バッチ番号、ライセンス プレート番号を表示する | この機能により、生産現場の実行インターフェイスでシリアル番号、バッチ番号、およびライセンス プレート番号のリストを表示し、さらに効率が向上します。 表示は、限られた文字数のカード ビューから、完全な値を表示するのに十分なスペースを提供するリスト ビューに変わります。 このリストは、特定の番号を検索する機能も提供します。 |
| 倉庫管理 | ASN からのプットアウェイ作業を切り離す | この機能は、スケール 単位で (分散ハイブリッド トポロジの一部として) 倉庫管理ワークロードを実行している場合に、事前出荷明細通知 (ASN)を送受信するために必要です。 また、プットアウェイ作業に関する情報を格納するための専用の新しいデータベース テーブルが追加されます。 以前は、この情報は ASN 用のテーブルに格納されていました。 |
| 倉庫管理 | スロット混合単位 | システムでは、品目を混合ユニット (ボックスとケースの両方など) を含む場所に入れ込みます。 この機能を使用すると、スロッティングのテンプレート行ごとに、品目を混合ユニットまたは単一ユニットのどちらの場所にスロットするかを選択できます。 |
| 倉庫管理 | 梱包ステーションでコンテナーの終了/再オープンのために高速 API を使用する | このプレビュー機能を有効にすると、コンテナーに関連する在庫トランザクションが、新しい明るいプロセスを使用して作成されます。このプロセスにより、手作業の梱包ステーションを行う際のコンテナーの決算または再オープンのパフォーマンスが向上します。 |

## <a name="new-and-updated-documentation-resources"></a>新しいドキュメント リソースおよび更新されたドキュメント リソース

次のヘルプ トピックが最近追加されたか大幅に更新されました。 前のセクションに示したように、このリリースで追加された新しい機能に関連するとは限りませんが、既存の機能をさらに活用するために役立つ場合があります。

| 機能領域 | 新規または更新されたトピック |
|---|---|
| マスター プラン | [在庫予測](../master-planning/inventory-forecast.md) |
| マスター プラン | [計画の最適化で使用されないパラメーター](../master-planning/planning-optimization/not-used-parameters.md) |
| マスター プラン | [補充方法と数量の変更](../master-planning/planning-optimization/replenishment-methods-quantity-modification.md) |
| マスター プラン | [無限能力を使用したスケジューリング](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| マスター プラン | [計画履歴と計画ログの表示](../master-planning/planning-optimization/plan-history-logs.md) |
| 倉庫管理 | [コンテナー梱包戦略](../warehousing/container-packing-strategy-overview.md) |
| 倉庫管理 | [循環棚卸のシナリオ例](../warehousing/cycle-counting-scenarios.md) |
| 倉庫管理 | [V2 データ エンティティによる入庫 ASN のインポート](../warehousing/import-asn-v2-data-entity.md) |
| 倉庫管理 | [販売注文および移動オーダーの超過ピッキング](../warehousing/over-picking-for-sales-and-transfer-orders.md) |
| 倉庫管理 | [ウェーブ中のウェーブ ラベル印刷をスケジュールする](../warehousing/configure-task-based-wave-label-printing.md) |
| 倉庫管理 | [Warehouse Management モバイル アプリの新機能または変更された機能](../warehousing/whats-new-wma.md) |

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations アプリのプラットフォーム更新プログラム

Microsoft Dynamics 365 Supply Chain Management 10.0.21 には、Platform updates が含まれています。 詳細については、[Finance and Operations アプリのバージョン 10.0.21 (2021 年 10 月) のプラットフォーム アップデート](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正

10.0.21 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=605166&dbType=3&qc=4b9449bf0d947113983bd0697140bf4d8727bfafd5566aa682cb38db343374de) を参照してください。

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 および業界のクラウド: 2021年リリース ウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365 および業界のクラウド: 2021年リリース ウェーブ 2 プラン](/dynamics365-release-plan/2021wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-supply-chain-management-features"></a>削除済みおよび非推奨の Supply Chain Management 機能

[Dynamics 365 Supply Chain Management の削除済みおよび非推奨の機能](removed-deprecated-features-scm-updates.md)トピックは、Supply Chain Management で削除または非推奨となる予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Supply Chain Management の削除済みまたは非推奨の機能](removed-deprecated-features-scm-updates.md)のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
