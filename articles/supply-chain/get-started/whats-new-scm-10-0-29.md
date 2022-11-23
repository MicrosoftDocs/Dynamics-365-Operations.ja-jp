---
title: Dynamics 365 Supply Chain Management 10.0.29 (2022 年 10 月) の新機能や変更された機能
description: この記事では、Microsoft Dynamics 365 Supply Chain Management 10.0.29 の新機能または変更された機能について説明します。
author: kamaybac
ms.date: 08/12/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 8f6ba18096cffe907c339ad525c99535bc5ee568
ms.sourcegitcommit: 7745c4bd3ab3aace4b4cb814eaf0cfdbae4a0cbd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2022
ms.locfileid: "9784694"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10029-october-2022"></a>Dynamics 365 Supply Chain Management 10.0.29 (2022 年 10 月) の新機能や変更された機能

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Supply Chain Management バージョン 10.0.29 の新機能または変更された機能について一覧表示します。 このバージョンのビルド番号は 10.0.1326 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2022 年 8 月
- **リリースの一般提供 (自己更新)**: 2022 年 9 月
- **リリースの一般提供 (自動更新)**: 2022 年 10 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 この記事が最初に公開された後に、ビルドに追加された機能を含めるために、この記事を更新することがあります。

| 機能領域 | フィーチャー | 詳細 | 次により有効化 |
|---|---|---|---|
| 在庫および物流 | [Inventory Visibility の WMS 品目の配賦と引当](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/allocate-reserve-whs-items-inventory-visibility) | [WMS 品目に対応した Inventory Visibility](../inventory/inventory-visibility-whs-support.md) | 既定で有効 |
| 在庫および物流 | [合理化された手持在庫リストの事前読み込み](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/query-inventory-visibility-summary-entity) | [Inventory Visibility アプリを使用する](../inventory/inventory-visibility-power-platform.md) | サービス コンフィギュレーションによって有効 |
| 受注生産供給の自動化 | [受注生産供給の自動化](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-to-order-supply-automation) | [受注生産供給の自動化](../master-planning/make-to-order-supply-automation.md) | 機能管理:<br>*受注生産供給の自動化* |
| 計画 | [DDMRP の詳細な分析情報の表示と適用](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/view-apply-detailed-insights-ddmrp) | [需要主導型材料所要量計画の概要](../master-planning/planning-optimization/ddmrp-overview.md) | 機能管理:<br>*(プレビュー) 計画最適化のための DDMRP* |
| 生産管理 | [完成品を仕訳帳に転記する前に現物在庫にする](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-finished-goods-physically-before-posting) | [完成品を仕訳帳に転記する前に現物在庫にする](../production-control/deferred-posting.md) | 機能管理:<br>*(プレビュー) 完成品を仕訳帳に転記する前に現物在庫にする* |
| 倉庫管理 | [Warehouse Mobile App 内で関連データを検索する](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/look-up-relevant-data-within-warehouse-mobile-app) | [Warehouse Management モバイル アプリの迂回を使用してデータをクエリする](../warehousing/warehouse-app-data-inquiry.md) | 機能管理:<br>*Warehouse Management アプリのデータ照会フロー* |

## <a name="feature-enhancements-included-in-this-release"></a>このリリースに含まれる機能拡張

次の表に、このリリースに含まれる機能拡張の一覧を示します。 これらの機能拡張は、それぞれ既存の機能を段階的に改善します。 これらは拡張機能にすぎないため、[リリース計画](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) には記載されません。 ただし、これらの拡張機能が既存のカスタマイズや基本設定と競合しないように、各機能は (特に断りのない限り) 既定でオフになっています。

これらの機能をオンまたはオフにする場合、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)で実行する必要があります。

| モジュール | 機能管理の機能名 | 詳細 |
|---|---|---|
| 原価管理 | 価格計算が保留中の連産品の最適化 | この機能で、複数のスレッドを使用して連産品価格を計算する場合にまれに発生する競合を修正します。 これにより、システムで、各連産品価格を 1 回だけ計算するようにします。 その計算の結果は。他のすべての計算の入力として使用されます。 保留中の価格が既に存在する場合は、その価格が使用されます。 |
| マスター プラン | 計画の最適化でのトランザクションのグループ化 | この機能を使用すると、計画の最適化を使用するときに、単一の販売注文明細行への供給に生成される計画オーダーの数を減らすことができます。 この機能をオンにすると、計画の最適化では、注文明細行のすべての在庫トランザクションを、全数量の単一の要件にグループ化します。 (これは組み込みの計画エンジンの動作と一致します。) 供給と需要は個別にグループ化されます。 そのため、この機能により、トランザクションを分割した場合や、補充分析コードではない分析コード (バッチ番号やシリアル番号など) を使用している場合に、トランザクション量を削減できます。 |
| 調達 | 仕入先を発注書保留中にする | この機能を使用すると、仕入先を発注書保留中にすることができます。 また、仕入先を発注書保留中とマークする新しい *発注書* 保留タイプが追加されます。 発注書保留中の仕入先に対して新しい発注書を作成することはできませんが、この仕入先に対する未処理の請求書や支払を続行することはできます。 |
| 販売とマーケティング | インポート時の明細行の正味金額の計算 | この機能を使用すると、OData とデュアル書き込みを使用して *販売注文明細行*、*販売見積明細行*、または *返品注文明細行* エンティティを介してデータをインポートする際に、明細行合計を再計算するかどうかを制御できます。 これは、売買契約評価ポリシーが設定されていて、販売注文明細行、販売見積明細行、返品注文明細行の **正味金額** フィールドへの変更が制限されている場合にのみ効果があります。 これにより、**売掛金勘定 > 設定> 売掛金勘定パラメーター** ページに **明細行の正味金額の計算** という設定が追加されます。 この設定が *はい* に設定されている場合、システムは必要に応じて常に明細行金額を再計算します (したがって、明細行正味金額の売買契約評価ポリシーは無視されます)。 設定が *いいえ* に設定されている場合、明細行の価格、数量、割引の変更のために明細行の正味金額の再計算を行う必要がある場合でも、システムは明細行の正味金額を自動的に計算しません。 この機能は既定で有効になっており、初期設定では **明細行の正味金額の計算** は *はい* に設定されています。 *いいえ* の設定は、バージョン 10.0.23 以前のシステム動作と一致し、主にレガシー統合シナリオをサポートするために提供されています。<br><br>詳細については、[販売注文、見積、および返品のインポート時に明細行の正味金額を再計算する](../sales-marketing/calc-line-net-amounts-import.md)を参照してください。 |
| 販売とマーケティング | 複数のスレッドを使用して販売合計を計算 | この機能を使用すると、販売合計をバッチ計算する際に並列処理を使用することで、システムのパフォーマンスを向上できます。 この機能は、新しい **スレッド数** フィールドを **販売合計の計算** ダイアログ ボックスに追加します。 計算をバッチで実行することを選択した場合は、このフィールドを使用してスレッドの最大数を設定することができます。 値を *0* (ゼロ) または *1* に設定した場合は、1 つのスレッドが使用されます。 1 より大きい値の場合はマルチスレッドが有効になります。 |
| 販売とマーケティング | 会社間に手動で入力された価格と割引の更新 | この機能により、会社間注文に対する手動変更ポリシーのサポートが追加されます。 これには、会社間販売と発注書の間で手動変更ポリシーを転送するサポートも含まれます。 以前は、手動変更ポリシーは、会社間以外の注文でのみサポートされていました。 この機能を有効にすると、会社間注文に対する変更を保存した後に価格と割引を更新できます。 このオプションを使用すると、新しい価格および割引の詳細を会社間注文に適用するか、注文を変更しないかを選択できます。 |

## <a name="new-and-updated-documentation-resources"></a>新しいドキュメント リソースおよび更新されたドキュメント リソース

次のヘルプ記事を最近追加、または大幅に更新しました。 これらの記事は、前のセクションに示したように、このリリースで追加された新しい機能に関連するとは限りません。 ただし、これらの機能は既存の機能をさらに活用するために役立つ場合があります。

| 機能領域 | 新規または更新された記事 |
|---|---|
| マスター プラン、CTP | [CTP を使用した販売注文配送日の計算](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) |
| マスター プラン、DDMRP | [需要主導型材料所要量計画の概要](../master-planning/planning-optimization/ddmrp-overview.md)<br>[システムで DDMRP 機能を有効化する](../master-planning/planning-optimization/ddmrp-enable.md)<br>[在庫配置](../master-planning/planning-optimization/ddmrp-inventory-positioning.md)<br>[バッファー プロファイルおよびレベル](../master-planning/planning-optimization/ddmrp-buffer-profile-and-levels.md)<br>[需要主導型計画](../master-planning/planning-optimization/ddmrp-planning.md)<br>[可視性および協調性の実行](../master-planning/planning-optimization/ddmrp-visual-and-collaborative-execution.md) |
| 倉庫管理 | [出荷用のコンテナーを梱包する](../warehousing/packing-containers.md)<br>[出荷コンテナーの梱包と出荷処理に関する梱包作業](../warehousing/packing-work.md) |

## <a name="feature-state-changes-in-this-release"></a>このリリースでの機能の状態変更

次の表に、バージョン 10.0.29 で必須となった、または既定でオンになった機能の一覧を示します。 これらのすべての機能は、バージョン 10.0.29 に更新すると、システムに対して自動的に有効になります。 必須機能はオフにできませんが、既定で有効になっている機能は[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用してオフにすることができます。

テーブルには、以前はパブリック プレビューでしたが、バージョン 10.0.29 で一般に利用できるように変更された機能も一覧表示しています。 この変更は、これらの機能は現在運用環境での使用が推奨されることを示しています。 特に断りのない限り、既定では、これらの機能は無効になっています。 そのため、使用する場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用してこれらの機能を有効にする必要があります。

| モジュール | 機能名 | 新しい機能の状態 |
| --- | --- | --- |
| 資産管理 | [生産現場の実行インターフェースの資産管理機能](../production-control/production-floor-execution-configure.md) | 必須 |
| 原価管理 | [決算と調整の取消のラベルを "取消" に変更](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/change-terminology-inventory-closing-cancellation-inventory-closing-reverse) | 必須 |
| 原価管理 | BOM 計算の詳細クロス原価計算バージョンのクリーンアップ | 必須 |
| 原価管理 | [品目価格の比較ストレージ](../cost-management/compare-item-price.md) | 必須 |
| 原価管理 | [原価計算レベル](../cost-management/cost-calculation-level.md) | 既定で有効 |
| 原価管理 | 在庫決算の取り消しに対してユーザー定義のバッチ番号設定を有効にする | 既定で有効 |
| 原価管理 | [在庫決算の進捗状況の詳細](whats-new-scm-10-0-21.md) | 既定で有効 |
| 原価管理 | [在庫金額レポート ストレージ](../cost-management/inventory-value-report-storage.md) | 必須 |
| 原価管理 | 在庫金額レポート データのクリーンアップ | 必須 |
| 原価管理 | 移動平均、代替原価の順序 | 必須 |
| 原価管理 | 在庫決算ログをグリッドに表示する | 必須 |
| 原価管理 | 完全に決済されたトランザクションが集計形式ではない品目を表示します | 必須 |
| 在庫および倉庫管理 | 空のバッチ属性値を許可する | 必須 |
| 在庫および倉庫管理 | 在庫移動指示明細行の自動増分行番号 | 必須 |
| 在庫および倉庫管理 | 販売明細行から移動オーダーを作成します | 必須 |
| 在庫および倉庫管理 | ワークフローの在庫仕訳帳明細行フィールドを無効にする | 必須 |
| 在庫および倉庫管理 | 在庫品質管理パラメーターの警告機能の有効化 | 必須 |
| 在庫および倉庫管理 | (中国) 現物入庫および出庫原価を月平均原価から除外する | 既定で有効 |
| 在庫および倉庫管理 | [在庫仕訳帳の承認ワークフロー](../inventory/inventory-journal-workflow.md) | 必須 |
| 在庫および倉庫管理 | [手持在庫レポート ストレージ](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/inventory-on-hand-report-storage) | 必須 |
| 在庫および倉庫管理 | [在庫管理用に保存されているビュー](saved-views-scm.md) | 必須 |
| 在庫および倉庫管理 | 移動オーダーのキャンセル | 必須 |
| 在庫および倉庫管理 | 在庫仕訳帳の測定単位と単位数量を使用する | 必須 |
| 在庫および倉庫管理 | 在庫仕訳帳のロックを解除する | 必須 |
| 製造 | [自動転記されたピッキング リストの倉庫対応材料の自動ピッキング](whats-new-scm-10-0-23.md) | 一般に入手可能 |
| 製造 | 生産工順の工程の材料リストで在庫分析コードの表示を有効にする | 必須 |
| 製造 | [ジョブ カード デバイスからの完了報告時に、バッチ番号とシリアル番号を入力できるようにします。](../production-control/report-finished-job-device.md) | 既定で有効 |
| 製造 | 改善された生産 CW 数量ピッキング | 既定で有効 |
| 製造 | [生産現場の実行インターフェイスのジョブ検索](../production-control/production-floor-execution-configure.md) | 必須 |
| 製造 | [製造実行システム統合](../production-control/mes-integration.md) | 既定で有効 |
| 製造 | [生産現場の実行インターフェイスの [自分の 1 日の職務] ビュー](../production-control/production-floor-execution-configure.md) | 既定で有効 |
| 製造 | [製造オーダーの材料の在庫状態のオンデマンド チェック](whats-new-scm-10-0-24.md) | 既定で有効 |
| 製造 | [既定の生産引当のオーバーライド](../production-control/override-default-reservation-principle.md) | 必須 |
| 製造 | [生産現場の実行インターフェースで材料消費を登録する (WMS 非対応)](../production-control/production-floor-execution-configure.md) | 一般に入手可能 |
| 製造 | [生産現場の実行インターフェイスからの CW 品目に関するレポート](../production-control/production-floor-execution-configure.md) | 一般に入手可能 |
| 製造 | [生産現場の実行インターフェースの連産品と副産物に関するレポート](../production-control/production-floor-execution-configure.md) | 既定で有効 |
| 製造 | [生産現場の実行インターフェイスでの計画品目に関するレポート](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | 既定で有効 |
| 製造 | [製造制御の保存済みビュー](saved-views-scm.md) | 必須 |
| 製造 | [生産フロア実行インターフェイスの完全なシリアル番号、バッチ番号、ライセンス プレート番号を表示する](../production-control/production-floor-execution-configure.md) | 必須 |
| 製造 | [予定消費日と対する原材料の有効期限の検証](whats-new-scm-10-0-23.md) | 既定で有効 |
| マスター プラン | [計画最適化の自動確定](../master-planning/planning-optimization/planned-order-firming.md) | 必須 |
| マスター プラン | [計画バルク オーダーおよび梱包バッチ オーダーのバッチ処理可能な確定と連結](whats-new-scm-10-0-20.md) | 既定で有効 |
| マスター プラン | [前処理フィルターが有効な場合、手持在庫がある品目を含める](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/master-planning-include-items-on-hand-when-pre-processing-filters-are-enabled) | 既定で有効 |
| マスター プラン | [計画最適化の無限キャパシティ スケジューリング](../master-planning/planning-optimization/infinite-capacity-planning.md) | 既定で有効 |
| マスター プラン | [計画最適化の利益幅](../master-planning/planning-optimization/safety-margins.md) | 必須 |
| マスター プラン | [計画の最適化のマイナス在庫日数](../master-planning/planning-optimization/delay-tolerance.md) | 必須 |
| マスター プラン | [調整された需要予測の並列承認](whats-new-scm-10-0-20.md) | 必須 |
| マスター プラン | [フィルター処理された計画オーダーの確定](../master-planning/planning-optimization/planned-order-firming.md) | 必須 |
| マスター プラン | [計画最適化の計画製造オーダー](../master-planning/planning-optimization/production-planning.md) | 必須 |
| マスター プラン | [計画最適化のための購買契約](../master-planning/planning-optimization/purchase-trade-agreement.md) | 必須 |
| マスター プラン | [計画オーダーの保存済みビュー](saved-views-scm.md) | 必須 |
| 調達 | 発注書の請求金額の最低金額および最高金額 | 必須 |
| 調達 | 購買要求配分のリセット ボタンの無効化 | 既定で有効 |
| 調達 | [調達関連ワークフローのリセットを有効にする](whats-new-scm-10-0-20.md) | 既定で有効 |
| 調達 | [バッチ タスクあたりの発注書明細行数の制限](whats-new-scm-10-0-27.md) | 既定で有効 |
| 調達 | [仕入先の財務分析コードと発注書の有効な分析コード リンクの財務分析コードを結合](whats-new-scm-10-0-25.md) | 必須 |
| 調達 | [受領書および仕入先請求書に対して在庫製品の登録数量と非在庫製品の残余を転記する](whats-new-scm-10-0-26.md) | 一般に入手可能 |
| 調達 | [複数の購買要求がワークフロー内にある場合に一般予算引当の過剰消費を防止する](whats-new-scm-10-0-21.md) | 既定で有効 |
| 調達 | [購買契約責任者](../procurement/purchase-agreements.md) | 必須 |
| 調達 | [発注書用に保存されているビュー](saved-views-scm.md) | 必須 |
| 製品情報管理 | タイムアウトを回避するための部品表レポートの前処理 | 必須 |
| 製品情報管理 | 品目テンプレートを使用するときに個別に既定の財務分析コードを使用する | 必須 |
| 製品情報管理 | 品目テンプレートの製品分析コード グループの有効化 | 必須 |
| 製品情報管理 | 品目 - バーコード エンティティの改善 | 必須 |
| 製品情報管理 | 用語に基づく製品バリアント名の再生成 | 必須 |
| 製品情報管理 | [リリースされた製品用に保存されているビュー](saved-views-scm.md) | 必須 |
| 製品情報管理 | [バリアント修正候補ページの改善](../pim/tasks/create-predefined-product-variants.md) | 必須 |
| 販売とマーケティング | [販売注文の諸費用配賦](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/miscellaneous-charges-enhancements) | 必須 |
| 販売とマーケティング | 販売注文更新履歴のクリーンアップ | 必須 |
| 販売とマーケティング | [経過日数に基づいて販売更新履歴をクリーンアップする](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) | 必須 |
| 販売とマーケティング | [連絡担当者データ エンティティのエクスポートの最適化](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | 必須 |
| 販売とマーケティング | 売上訂正票の合計割引グループのコピー | 必須 |
| 販売とマーケティング | [販売見積書の概要と文書の結びのフィールドのルックアップを有効にする](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | 必須 |
| 販売とマーケティング | ["上位 100" の顧客レポートのパフォーマンスを向上する](whats-new-scm-10-0-23.md) | 必須 |
| 販売とマーケティング | 待機中のレコードを履歴クリーンアップ タスクに含める | 必須 |
| 販売とマーケティング | バッチ タスクあたりの販売注文明細行数の制限 | 既定で有効 |
| 販売とマーケティング | [転記用に選択できる販売注文数を制限する](whats-new-scm-10-0-21.md) | 必須 |
| 販売とマーケティング | 見積顧客残高を再計算する | 必須 |
| 販売とマーケティング | [CW を使用する場合と使用しない場合の小数点以下の精度での販売返品注文明細行の登録](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | 必須 |
| 販売とマーケティング | [Sales およびマーケティング用に保存済みビュー](saved-views-scm.md) | 必須 |
| 販売とマーケティング | [1 度クリックして販売注文を確認](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/single-click-sales-order-confirmation) | 必須 |
| 輸送管理 | 転記済の仕入先請求仕訳帳を使用しない、運賃請求書明細行の運賃請求書の照合解除を許可します | 既定で有効 |
| 輸送管理 | [運賃請求書を破棄する際に仕入先請求仕訳帳の作成を有効にする](whats-new-scm-10-0-20.md) | 既定で有効 |
| 輸送管理 | [小型パーセルの出荷](../warehousing/small-parcel-shipping.md) | 必須 |
| 輸送管理 | [USMCA 原産地証明書](../transportation/usmca-certification-of-origin.md) | 既定で有効 |
| 倉庫管理 | [追加の場所ゾーン](../warehousing/additional-location-zones.md) | 必須 |
| 倉庫管理 | [作業のキャンセル](../warehousing/cancel-warehouse-work.md) | 必須 |
| 倉庫管理 | [出荷の連結](../warehousing/configure-shipment-consolidation-policies.md) | 必須 |
| 倉庫管理 | [倉庫アプリからの移動オーダーを作成および処理します](../warehousing/create-transfer-order-from-warehouse-app.md) | 必須 |
| 倉庫管理 | クロスドッキング テンプレートと場所ディレクティブ | 既定で有効 |
| 倉庫管理 | [ASN からのプットアウェイ作業を切り離す](whats-new-scm-10-0-21.md) | 必須 |
| 倉庫管理 | [遅延プット オペレーション](../warehousing/deferred-processing-manual-inventory-movement.md) | 必須 |
| 倉庫管理 | 遅延プット - コンテナー | 既定で有効 |
| 倉庫管理 | 遅延プット処理 – トリガーイベントが [前] に設定されている監査テンプレート機能を有効にします | 必須 |
| 倉庫管理 | [ブロックされた在庫をサンプルした品質指示の予定入庫を無効にする](../inventory/inventory-blocking.md) | 既定で有効 |
| 倉庫管理 | 倉庫モバイル デバイスの高速検証を有効にする | 必須 |
| 倉庫管理 | [GS1 バーコードの拡張パーサー](../warehousing/gs1-barcodes.md) | 一般に入手可能 |
| 倉庫管理 | [柔軟な注文 - コミットされたライセンス プレート引当](../warehousing/flexible-warehouse-level-dimension-reservation.md) | 必須 |
| 倉庫管理 | [柔軟な倉庫レベル分析コードの引当](../warehousing/flexible-warehouse-level-dimension-reservation.md) | 必須 |
| 倉庫管理 | [品目の連結場所の使用率](../warehousing/item-consolidation-location-utilization.md) | 既定で有効 |
| 倉庫管理 | ライセンス プレートの受取履歴 | 既定で有効 |
| 倉庫管理 | [手動による出荷の連結](../warehousing/consolidate-shipments-manual-workbench.md) | 既定で有効 |
| 倉庫管理 | [管理者または同様の信頼できるユーザーのための移動明細行手動ピッキング サービス](whats-new-scm-10-0-28.md) | 一般に入手可能 |
| 倉庫管理 | [材料取り扱い設備のインターフェイス](../warehousing/mhax.md) | 必須 |
| 倉庫管理 | [新しい積荷計画ワークベンチ ページ](whats-new-scm-10-0-24.md) | 一般に入手可能 |
| 倉庫管理 | [出庫ワークロードの視覚化](../warehousing/outbound-workload-visualization.md) | 必須 |
| 倉庫管理 | [計画済クロスドッキング](../warehousing/planned-cross-docking.md) | 必須 |
| 倉庫管理 | [倉庫アプリ イベントの処理](../warehousing/warehouse-app-events.md) | 必須 |
| 倉庫管理 | 連産品と副産物のプット アウェイ作業テンプレートのクエリの拡張 | 必須 |
| 倉庫管理 | [倉庫へのリリース時に数量を最も近い販売単位に切り捨てる](whats-new-scm-10-0-19.md) | 必須 |
| 倉庫管理 | [積荷計画ワークベンチ用に保存されているビュー](saved-views-scm.md) | 必須 |
| 倉庫管理 | [作業の詳細ページ用に保存されているビュー](saved-views-scm.md) | 必須 |
| 倉庫管理 | [ウェーブ処理用に保存されているビュー](saved-views-scm.md) | 必須 |
| 倉庫管理 | [積荷処理用に保存されているビュー](saved-views-scm.md) | 必須 |
| 倉庫管理 | [出荷処理用に保存されているビュー](saved-views-scm.md) | 必須 |
| 倉庫管理 | [GS1 バーコードのスキャン](../warehousing/gs1-barcodes.md) | 一般に入手可能 |
| 倉庫管理 | 出荷ウェーブ ラベルの詳細 | 必須 |
| 倉庫管理 | [スロット混合単位](whats-new-scm-10-0-21.md) | 必須 |
| 倉庫管理 | [梱包ステーションでコンテナーの終了/再オープンのために高速 API を使用する](whats-new-scm-10-0-21.md) | 既定で有効 |
| 倉庫管理 | [補充ジョブに選択されているテンプレートの検証](whats-new-scm-10-0-20.md) | 既定で有効 |
| 倉庫管理 | [倉庫アプリのプロモーション フィールド](../warehousing/warehouse-app-promoted-fields.md) | 必須 |
| 倉庫管理 | [倉庫アプリのステップ指示](../warehousing/mobile-app-titles-instructions.md) | 必須 |
| 倉庫管理 | [倉庫の場所の状態](../warehousing/warehouse-location-status.md) | 必須 |
| 倉庫管理 | [Warehouse Management アプリの迂回](../warehousing/warehouse-app-detours.md) | 既定で有効 |
| 倉庫管理 | [ウェーブ バッチ ジョブの詳細](../warehousing/wave-processing.md) | 必須 |
| 倉庫管理 | [ウェーブの実行通知](../warehousing/wave-execution-notifications.md) | 必須 |

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Microsoft Dynamics 365 Supply Chain Management 10.0.29 には、Platform updates が含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.29 のプラットフォーム更新プログラム (2022 年 10 月)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md). を参照してください。

### <a name="bug-fixes"></a>バグ修正

バージョン 10.0.29 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559) を参照してください。

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 および業界クラウド: 2022 年リリース ウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365 および業界クラウド: 2022 年リリース ウェーブ 2 プラン](/dynamics365-release-plan/2022wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-supply-chain-management-features"></a>削除済みおよび非推奨の Supply Chain Management 機能

[Dynamics 365 Supply Chain Management の削除済みおよび非推奨の機能](removed-deprecated-features-scm-updates.md)の記事は、Supply Chain Management で削除または非推奨となる予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Supply Chain Management の削除済みまたは非推奨の機能](removed-deprecated-features-scm-updates.md)の記事に発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および運用環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
