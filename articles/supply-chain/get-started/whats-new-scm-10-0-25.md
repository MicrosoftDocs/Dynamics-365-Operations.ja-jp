---
title: Dynamics 365 Supply Chain Management 10.0.25 (2022 年 4 月) の新機能および変更された機能
description: この記事では、Microsoft Dynamics 365 Supply Chain Management 10.0.25 の新機能または変更された機能について説明します。
author: kamaybac
ms.date: 03/14/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: d6aa5a0cb49e5871a50a2ac5ac2c29cc09e232fc
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403685"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10025-april-2022"></a>Dynamics 365 Supply Chain Management 10.0.25 (2022 年 4 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Supply Chain Management バージョン 10.0.25 の新機能または変更された機能について一覧表示します。 このバージョンには 10.0.1149 のビルド番号が含まれており、次のように使用できます。

- **リリースのプレビュー:** 2022 年 2 月
- **リリースの一般提供 (自己更新):** 2022 年 3 月
- **リリースの一般提供 (自動更新):** 2022 年 4 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 この記事が最初に公開された後に、ビルドに加えた機能を含めるために、この記事を更新することがあります。

| 機能領域 | フィーチャー | 詳細 |  に  によって有効化 |
|---|---|---|---|
| 在庫&nbsp;および&nbsp;物流 | [危険物の拡張機能](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/hazardous-materials-enhancements) | 間もなく公開 | 機能管理:<br>*危険物の拡張機能* |
| 在庫&nbsp;および&nbsp;物流 | [梱包ステーションの梱包作業](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/packing-work-packing-stations) | [出荷コンテナーの梱包と出荷処理に関する梱包作業](../warehousing/packing-work.md) | 機能管理:<br>*梱包ステーションの梱包作業* |
| 在庫&nbsp;および&nbsp;物流 | [GS1 形式標準を使用した倉庫内のバーコードのスキャン](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | [GS1 バーコードと QR コード](../warehousing/gs1-barcodes.md) | 機能管理:<br>*GS1 バーコードのスキャン* |
| 製造 | [生産現場の実行インターフェースで材料消費と予約する](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/material-consumption-reservations-production-floor-execution-interface) | [生産現場の実行インターフェイスを作業者が使用する方法](../production-control/production-floor-execution-use.md) | 機能管理:<br>*生産現場の実行インターフェースで材料消費を登録する (WMS 非対応)*<br><br>かつ/または:<br><br>機能管理:<br>*(プレビュー) 生産現場の実行インターフェイス (WMS 対応) で材料消費を登録* |
| 計画 | [計画の最適化集中カレンダーのメンテナンス](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-centralized-calendar-maintenance) | [カレンダーおよびマスター プラン](../master-planning/supply-chain-calendars-master-planning.md) | 既定で有効 |
| 計画 | [既存の供給を最適化するための計画の最適化に関する提案](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-suggestions-optimize-existing-supply) | [アクション メッセージ](../master-planning/action-messages.md) | 既定で有効 |
| 計画 | 簡易計画オーダー | [簡易計画オーダー](../master-planning/planning-optimization/planned-orders-simplified.md ) | 機能管理:<br>*簡易計画オーダー* |

## <a name="feature-enhancements-included-in-this-release"></a>このリリースに含まれる機能拡張

次の表に、このリリースに含まれる機能拡張の一覧を示します。 これらの機能拡張は、それぞれ既存の機能を段階的に改善します。 これらは拡張機能にすぎないため、[リリース計画](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) には記載されません。 ただし、これらの拡張機能が既存のカスタマイズや基本設定と競合しないように、各機能は (特に断りのない限り) 既定でオフになっています。

これらの機能をオンまたはオフにする場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) で実行する必要があります。

| モジュール | 機能管理の機能名 | 詳細 |
|---|---|---|
| 在庫および倉庫管理 | (ポーランド) 複数の SAD 請求書を 1 つの SAD の 1 つの発注書明細行にリンクすることを許可する | この機能を使用すると、複数の異なる請求書 (複数の出荷の場合など) にそれらの購買注文明細行が転記された場合に、購買注文明細行を分割し、単一の管理ドキュメント (SAD) にリンクできます。 |
| 調達 | 複数の購買要求を転記日別に 1 つの発注書に連結 | この機能により、異なる購買要求の会計日付が異なる場合に、複数の購買要求を 1 つの購買注文に連結できます。 発注書の作成および需要連結の購買ポリシー ルールを設定すると、購買注文レベルで要求明細行を会計日付別にグループ化する決定が自動化されます。 会計日が予算の予約と債務に使用されるため、予算管理が有効になっている場合、会計日付による発注書連結はサポートされません。 したがって、これは、購買要求から発注書への移行中に保持する必要があります。 |
| 調達 | レガシ既定の RFQ 返信フィールド設定を表示する | この機能は、以前にユーザー インターフェイスから削除された、レガシの規定見積依頼 (RFQ) の返信フィールド設定を再導入します。 これらの設定は、ボックスの外に任意の機能を提供しますが、必要に応じてカスタマイズできます。 組織で既定の RFQ 返信フィールド設定の機能が既に追加されている場合、または追加する予定の場合は、この機能を有効にします。 この機能が有効な場合は、**調達パラメータ** ページに移動し、**見積依頼** タブを開き、**見積依頼の返信の既定の返信** フィールドを選択することで、この設定にアクセスできます。 |
| 調達 | 仕入先の財務分析コードと発注書の有効な分析コード リンクの財務分析コードを結合 | この機能により、財務分析コードとサイト在庫分析コードとの間にリンクを設定している場合は、アクティブな分析コードリンク購買要求を持つベンダーからの財務分析コードをマージできるようになります。 発注書の作成と需要連結の購買ポリシー ルールを設定することで、発注書ヘッダー レベルで有効な分析コード リンク財務分析コードを持つ仕入先から財務分析コードをマージする決定を強化できます。 |
| 生産管理 | (ロシア語) 生産で生産フォーミュラ/BOM の既定の場所の設定と GTD 自動予約/消費を有効にする | この機能は、インポートされた原材料からの生産に関する追加オプションを有効にします (ロシア語翻訳のみ)。<ul><li>リソース グループと倉庫の両方で生産フォーミュラと部品表の自動既定の場所を設定するオプション。</li><li>非 WMS 予約アルゴリズムに基いた、WMS 有効化倉庫での *GTD 番号* 分析コードによる原材料の自動予約。 これは、*原材料ピッキング* の作業ポリシーが **作業の作成方法** を *設定しない* に設定し、倉庫、場所、および品目番号の設定が生産 (バッチ) オーダーの在庫トランザクションと一致する場合に適用されます。</li><li>ピッキング リストの転記時に 、*GTD 番号* 分析コードによる原材料の自動消費 (前述の取得済予約に従います)。</li></ul> |
| 倉庫管理 | (プレビュー) 入庫および出庫倉庫オーダーに対するスケール ユニットのサポート | この機能により、システムはリリースから倉庫へのプロセス中に出庫倉庫注文を作成し、さらに移動オーダーが出荷として転記される際に入庫倉庫注文を作成します。 その後、システムは各入庫倉庫注文または出庫倉庫注文が、注文の出荷または入庫を担当するスケール ユニットに同期されます。 この機能を有効にした後で、倉庫の実行ワークロードをアップグレードする必要があります。 詳細については、[クラウドおよびエッジのスケール ユニットに対する倉庫管理ワークロード](../cloud-edge/cloud-edge-workload-warehousing.md) を参照してください。<br><br>この機能には、*ASNs からのプットアウェイ作業を切り離す* 機能が必要で、Warehouse Management モバイル アプリでライセンス プレート入庫プロセスを使用した移動注文のキャパシティを有効にします。 |

## <a name="feature-state-changes-in-this-release"></a>このリリースでの機能の状態変更

次の表に、10.0.25 以降必須となった、または規定でオンになった機能の一覧を示します。 これらのすべての機能は、10.0.25 に更新すると、システムに対して自動的に有効になります。 必須機能はオフにできませんが、既定で有効になっている機能は [機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を使用してオフにすることができます。

このテーブルには、以前はパブリック プレビューにあった機能も一覧表示していますが、10.0.25 で一般に利用できるように変更されました。つまり、これらの機能は運用環境での使用が推奨されています。 特に断りのない限り、これらの機能は既定でオフになっています。そのため、機能管理を使用する場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を使用して有効にする必要があります。

| モジュール | 機能名 | 機能状態 |
| --- | --- | --- |
| 資産管理 | [メンテナンス計画の実行中に作業指示書のグループ化に関するルールを適用する](../asset-management/preventive-and-reactive-maintenance/creating-work-orders.md) | 一般に入手可能 |
| 資産管理 | [カウンターに基づくメンテナンス機能拡張](../asset-management/preventive-and-reactive-maintenance/maintenance-plans.md) | 一般に入手可能 |
| 原価管理 | [原価計算レベル](../cost-management/cost-calculation-level.md) | 一般に入手可能 |
| 原価管理 | 在庫決算の取り消しに対してユーザー定義のバッチ番号設定を有効にする | 一般に入手可能 |
| 原価管理 | [在庫決算の進捗状況の詳細](whats-new-scm-10-0-21.md) | 一般に入手可能 |
| 原価管理 | [在庫の標準原価再評価用財務分析コードの既定値のオプション](../cost-management/manage-standard-cost-updates.md) | 一般に入手可能 |
| 原価管理 | 在庫金額レポート データのクリーンアップ | 既定で有効 |
| 原価管理 | [在庫金額レポート ストレージ](../cost-management/inventory-value-report-storage.md) | 既定で有効 |
| 原価管理 | 在庫決算ログをグリッドに表示する | 既定で有効 |
| エンジニアリング変更管理 | [既存の製品の変更管理の有効化](../engineering-change-management/change-management-existing-products.md) | 既定で有効 |
| エンジニアリング変更管理 | [エンジニアリング変更管理](../engineering-change-management/product-engineering-overview.md) | 既定で有効 |
| エンジニアリング変更管理 | [生産向けのエンジニアリング通知](../engineering-change-management/engineering-change-management.md) | 既定で有効 |
| エンジニアリング変更管理 | [エンジニアリング変更管理の属性継承の改善](../engineering-change-management/engineering-attributes-and-search.md) | 既定で有効 |
| エンジニアリング変更管理 | [フォーミュラとその成分に対する変更の管理](../engineering-change-management/manage-formula-changes.md) | 既定で有効 |
| エンジニアリング変更管理 | [製品準備完了チェック](../engineering-change-management/product-readiness.md) | 既定で有効 |
| エンジニアリング変更管理 | [エンジニアリング製品のバリアントの生成](../engineering-change-management/engineering-variants.md) | 既定で有効 |
| 在庫および倉庫管理 | BOM 明細行から BOM バージョンへのナビゲーション | 必須 |
| マスター プラン | [計画バルク オーダーおよび梱包バッチ オーダーのバッチ処理可能な確定と連結](whats-new-scm-10-0-20.md) | 一般に入手可能 |
| マスター プラン | リソース計画とメンテナンス | 一般に入手可能 |
| マスター プラン | マスター プラン設定ウィザード機能の有効化 | 必須 |
| マスター プラン | [需要予測の詳細に対する予測モデルの選択](../master-planning/manual-adjustments-baseline-forecast.md) | 必須 |
| マスター プラン | [マスター プランの進行状況の視覚化](../master-planning/tasks/monitor-master-planning-run.md) | 必須 |
| マスター プラン | [計画オーダーの並行確定](../master-planning/planning-optimization/planned-order-firming.md) | 必須 |
| マスター プラン | [フィルター処理された計画オーダーの確定](../master-planning/planning-optimization/planned-order-firming.md) | 既定で有効 |
| マスター プラン | [計画オーダーの保存済みビュー](saved-views-scm.md) | 既定で有効 |
| 調達 | 購買要求配分のリセット ボタンの無効化 | 一般に入手可能 |
| 調達 | [調達関連ワークフローのリセットを有効にする](whats-new-scm-10-0-20.md) | 一般に入手可能 |
| 調達 | バッチで仕入先コラボレーションにて受領した発注書の確認 | 必須 |
| 調達 | 購買契約の終了状態 | 必須 |
| 調達 | 購買契約書に関連付けられている発注書請求書に明細行を追加する | 既定で有効 |
| 調達 | [製品受領書の転記] ページに [注文済数量] フィールドを追加 | 既定で有効 |
| 調達 | [仕入先コラボレーションを通じて仕入先が調達カテゴリに適用できるようにする](../procurement/category-requests-from-vendors.md) | 既定で有効 |
| 調達 | 発注書の請求金額の最低金額および最高金額 | 既定で有効 |
| 調達 | サイトおよび倉庫の諸費用の設定 | 既定で有効 |
| 調達 | 年間関税に基づく仕入関税計算を有効にする | 既定で有効 |
| 調達 | [購買契約責任者](../procurement/purchase-agreements.md) | 既定で有効 |
| 調達 | [発注書用に保存されているビュー](saved-views-scm.md) | 既定で有効 |
| 製品情報管理 | [既定の注文数量の厳密な検証](../production-control/default-order-settings.md) | 必須 |
| 製品情報管理 | タイムアウトを回避するための部品表レポートの前処理 | 既定で有効 |
| 製品情報管理 | 品目テンプレートを使用するときに個別に既定の財務分析コードを使用する | 既定で有効 |
| 製品情報管理 | 品目テンプレートの製品分析コード グループの有効化 | 既定で有効 |
| 製品情報管理 | 用語に基づく製品バリアント名の再生成 | 既定で有効 |
| 製品情報管理 | [バリアント修正候補ページの改善](../pim/tasks/create-predefined-product-variants.md) | 既定で有効 |
| 生産管理 | 改善された生産 CW 数量ピッキング | 一般に入手可能 |
| 生産管理 | 新しいボタンが [ジョブ カード ターミナル] ページに追加されました | 必須 |
| 生産管理 | [ジョブ カード デバイスでの完了報告時に、ライセンス プレート番号の自動生成を有効にする](../production-control/production-floor-execution-configure.md) | 必須 |
| 生産管理 | 外注品目の部分入庫が有効になり、仕入先タイプの BOM 明細行の仕損計算に関する問題を修正しました | 必須 |
| 生産管理 | [画面ジョブカード デバイスとジョブ カード端末を除菌できるようにロックする機能](../production-control/production-floor-execution-configure.md) | 必須 |
| 生産管理 | [承認ジョブ] と [転送ジョブ] ダイアログの機能強化 | 必須 |
| 生産管理 | [完了報告用ライセンス プレートをジョブ カード デバイスに追加](../production-control/production-floor-execution-configure.md) | 必須 |
| 生産管理 | [ジョブ カード デバイスからラベルを印刷](../production-control/production-floor-execution-configure.md) | 必須 |
| 生産管理 | [生産現場の実行](../production-control/production-floor-execution-configure.md) | 必須 |
| 生産管理 | [生産現場の実行インターフェースの資産管理機能](../production-control/production-floor-execution-configure.md) | 既定で有効 |
| 生産管理 | [生産現場の実行インターフェイスのジョブ検索](../production-control/production-floor-execution-configure.md) | 既定で有効 |
| 生産管理 | [既定の生産引当のオーバーライド](../production-control/override-default-reservation-principle.md) | 既定で有効 |
| 生産管理 | [生産フロア実行インターフェイスの完全なシリアル番号、バッチ番号、ライセンス プレート番号を表示する](whats-new-scm-10-0-21.md) | 既定で有効 |
| 販売とマーケティング | [販売注文詳細のパフォーマンスの向上](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | 一般に入手可能 |
| 販売とマーケティング | 販売見積詳細のパフォーマンスの向上 | 一般に入手可能 |
| 販売とマーケティング | 販売注文参照データ エクスポート ポリシー | 必須 |
| 販売とマーケティング | [販売注文から発注書に対する明細行の削除ポリシー](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-purchase-order-line-deletion-policy) | 必須 |
| 販売とマーケティング | [販売見積参照データ エクスポート ポリシー](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy)| 必須 |
| 販売とマーケティング | [連絡担当者データ エンティティのエクスポートの最適化](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | 既定で有効 |
| 販売とマーケティング | 販売見積書の概要と文書の結びのフィールドのルックアップを有効にする | 既定で有効 |
| 販売とマーケティング | ["上位 100" の顧客レポートのパフォーマンスを向上する](whats-new-scm-10-0-23.md) | 既定で有効 |
| 販売とマーケティング | 見積顧客残高を再計算する | 既定で有効 |
| 販売とマーケティング | [CW を使用する場合と使用しない場合の小数点以下の精度での販売返品注文明細行の登録](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | 既定で有効 |
| 販売とマーケティング | [販売とマーケティング用の保存されているビュー](saved-views-scm.md) | 既定で有効 |
| 販売とマーケティング | 1 度クリックして販売注文を確認 | 既定で有効 |
| 倉庫管理 | [クロスドッキング テンプレートと場所ディレクティブ](../warehousing/planned-cross-docking.md) | 一般に入手可能 |
| 倉庫管理 | [ブロックされた在庫をサンプルした品質指示の予定入庫を無効にする](../inventory/inventory-blocking.md) | 一般に入手可能 |
| 倉庫管理 | ライセンス プレートの受取履歴 | 一般に入手可能 |
| 倉庫管理 | [材料取り扱い設備のインターフェイス](../warehousing/mhax.md) | 一般に入手可能 |
| 倉庫管理 | [倉庫へのリリース時に数量を最も近い販売単位に切り捨てる](whats-new-scm-10-0-19.md) | 一般に入手可能 |
| 倉庫管理 | 倉庫アプリ作業一覧用のスケール ユニットのサポート | 一般に入手可能 |
| 倉庫管理 | 出荷ウェーブ ラベルの詳細 | 一般に入手可能 |
| 倉庫管理 | [梱包ステーションでコンテナーの終了/再オープンのために高速 API を使用する](whats-new-scm-10-0-21.md) | 一般に入手可能 |
| 倉庫管理 | [補充ジョブに選択されているテンプレートの検証](whats-new-scm-10-0-20.md) | 一般に入手可能 |
| 倉庫管理 | 既存の即時補充作業 (全単位間) の使用を補充テンプレートに許可する | 必須 |
| 倉庫管理 | WHS ユーザー作成時の GUID の自動割り当て | 必須 |
| 倉庫管理 | 積荷品目入庫中に、倉庫管理アプリの製品バリアントと追跡用分析コードをキャプチャします | 必須 |
| 倉庫管理 | [追跡用分析コードによって制御される品目の在庫状態を変更する](../inventory/inventory-statuses.md) | 必須 |
| 倉庫管理 | [作業での作業プールの変更](../warehousing/change-work-pool-on-work.md) | 必須 |
| 倉庫管理 | [クラスター位置フル](../warehousing/cluster-position-full.md) | 必須 |
| 倉庫管理 | [クラスター プットアウェイ機能](../warehousing/putaway-clusters.md) | 必須 |
| 倉庫管理 | [確認および転送](../warehousing/confirm-and-transfer.md) | 必須 |
| 倉庫管理 | [バッチ ジョブからの出荷の確認](../warehousing/confirm-outbound-shipments-from-batch-jobs.md) | 必須 |
| 倉庫管理 | [モバイル デバイスで入荷の概要ページを表示するかどうかを制御する](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | 必須 |
| 倉庫管理 | [手動在庫移動操作の遅延処理](../warehousing/deferred-processing-manual-inventory-movement.md) | 必須 |
| 倉庫管理 | ウェーブ積荷構築テンプレートの要件を満たしていない積荷を作成することは許可されません | 必須 |
| 倉庫管理 | [拡張ライセンス プレート ラベルのレイアウト](../warehousing/document-routing-layout-for-license-plates.md) | 必須 |
| 倉庫管理 | [複数 SKU の場所ディレクティブのすべてのアクションを評価する](/troubleshoot/dynamics-365/supply-chain/warehousing/evaluate-multiple-location-directive-actions) | 必須 |
| 倉庫管理 | [すべての積荷] ページおよび [積荷詳細] ページの [合計値] フィールドを非表示にします | 必須 |
| 倉庫管理 | ライセンス プレート ラベルのビルド コンフィギュレーション | 必須 |
| 倉庫管理 | 管理者または類似の信頼されたユーザーの積荷明細行の手動修正 | 必須 |
| 倉庫管理 | [場所ライセンス プレートの配置](../warehousing/location-license-plate-positioning.md) | 必須 |
| 倉庫管理 | [場所の製品分析コードの混在](../warehousing/location-product-dimension-mixing.md) | 必須 |
| 倉庫管理 | モバイル デバイスの在庫移動の在庫状態フィールドを編集できるようにする | 必須 |
| 倉庫管理 | [管理者または同様の信頼できるユーザーのための販売明細行手動ピッキング サービス](../warehousing/manual-order-line-picking-exception-handling.md) | 必須 |
| 倉庫管理 | [移動オーダー出荷済ライセンス プレートを出荷先倉庫以外の倉庫で使用することを禁止する](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | 必須 |
| 倉庫管理 | あいまいな [場所/ライセンス プレート] の名前の解決を確認する | 必須 |
| 倉庫管理 | [品質チェック](../warehousing/quality-check.md) | 必須 |
| 倉庫管理 | [新しい倉庫アプリのユーザー設定、アイコン、ステップ タイトル](../warehousing/install-configure-warehouse-management-app.md) | 必須 |
| 倉庫管理 | [追加の場所ゾーン](../warehousing/additional-location-zones.md) | 既定で有効 |
| 倉庫管理 | [倉庫アプリからの移動オーダーを作成および処理します](../warehousing/create-transfer-order-from-warehouse-app.md) | 既定で有効 |
| 倉庫管理 | 倉庫モバイル デバイスの高速検証を有効にする | 既定で有効 |
| 倉庫管理 | [倉庫管理の手持在庫エントリ クリーンアップ ジョブの最大実行時間](../warehousing/onhand-cleanup.md) | 既定で有効 |
| 倉庫管理 | [出庫ワークロードの視覚化](../warehousing/outbound-workload-visualization.md) | 既定で有効 |
| 倉庫管理 | [倉庫アプリ イベントの処理](../warehousing/warehouse-app-events.md) | 既定で有効 |
| 倉庫管理 | [積荷計画ワークベンチ用に保存されているビュー](saved-views-scm.md) | 既定で有効 |
| 倉庫管理 | [作業の詳細ページ用に保存されているビュー](saved-views-scm.md) | 既定で有効 |
| 倉庫管理 | [ウェーブ処理用に保存されているビュー](saved-views-scm.md) | 既定で有効 |
| 倉庫管理 | [積荷処理用に保存されているビュー](saved-views-scm.md) | 既定で有効 |
| 倉庫管理 | [出荷処理用に保存されているビュー](saved-views-scm.md) | 既定で有効 |
| 倉庫管理 | [ウェーブ バッチ ジョブの詳細](../warehousing/wave-processing.md) | 既定で有効 |
| 倉庫管理 | [ウェーブの実行通知](../warehousing/wave-execution-notifications.md) | 既定で有効 |

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Microsoft Dynamics 365 Supply Chain Management 10.0.25 には、Platform updates が含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.25 のプラットフォーム更新プログラム (2022 年 4 月)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-25.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正

10.0.25 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=654580&dbType=3&qc=3799fa965b008dd980d27cf740e4582e6384ec6601ae8a35b7eaec6f1287a868) を参照してください。

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 および業界クラウド: 2022 年リリース ウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365 および業界クラウド: 2022 年リリース ウェーブ 1 プラン](/dynamics365-release-plan/2022wave1/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-supply-chain-management-features"></a>削除済みおよび非推奨の Supply Chain Management 機能

[Dynamics 365 Supply Chain Management の削除済みおよび非推奨の機能](removed-deprecated-features-scm-updates.md)の記事は、Supply Chain Management で削除または非推奨となる予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Supply Chain Management の削除済みまたは非推奨の機能](removed-deprecated-features-scm-updates.md)の記事に発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および運用環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

