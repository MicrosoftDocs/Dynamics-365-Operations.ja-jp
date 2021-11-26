---
title: Dynamics 365 Supply Chain Management 10.0.21 (2021 年 10 月) の新機能または変更された機能
description: このトピックでは、Dynamics 365 Supply Chain Management 10.0.21 の新機能または変更された機能について説明します。
author: kamaybac
ms.date: 10/28/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 3b5f0c6947944ec875c30fa912f830f245b5a48e
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/09/2021
ms.locfileid: "7777940"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10021-october-2021"></a>Dynamics 365 Supply Chain Management 10.0.21 (2021 年 10 月) の新機能または変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management バージョン 10.0.21 の新機能または変更された機能について一覧表示します。 このバージョンには 10.0.960 のビルド番号が含まれており、次のように使用できます。

- **リリースのプレビュー:** 2021 年 8 月
- **リリースの一般提供 (手動更新):** 2021 年 9 月
- **リリースの一般提供 (自動更新):** 2021 年 10 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 *機能* 列には、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) へのリンクがあり、各機能の公式リリース日を確認できます。 *詳細情報* 列には、詳細情報や関連ドキュメントへのリンクが表示されます。

これらの機能のほとんどは、使用する前に[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)を使用して有効にする必要があります。

| 機能領域 | フィーチャー | 詳細 |
|---|---|---|
| 在庫&nbsp;および&nbsp;物流 | [Dynamics 365 Supply Chain Management のグローバル在庫会計アドイン](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/global-inventory-accounting-add-in-dynamics-365-supply-chain-management) | [グローバル在庫会計ホーム ページ](../global-inventory-accounting/global-inventory-accounting-home.md) |
| 在庫&nbsp;および&nbsp;物流 | [相手勘定に接続されたコードを使用した手当調整の転記](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/post-on-hand-adjustments-using-configurable-reason-codes-connected-offset-accounts) | [在庫棚卸の理由コード](../warehousing/reason-codes-for-counting-journals.md) |
| 在庫&nbsp;および&nbsp;物流 | [販売見積参照データ エクスポート ポリシー](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy) | 見積書で参照されているデータを変更すると、それらの見積書 (または明細行) が次の増分エクスポートに含まれるかどうかを選択します。 そのような見積書または明細行を含めない場合は、増分エクスポートがより迅速に実行します。<br><br>この機能は、**変更追跡中に販売見積参照データをスキップ** という設定を **売掛金勘定パラメーター** ページに追加します。 |
| 在庫&nbsp;および&nbsp;物流 | [シールド入札](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sealed-bidding) | [RFQ の封緘入札](../procurement/sealed-bidding.md) |
| 在庫&nbsp;および&nbsp;物流 | [GS1 形式標準を使用した倉庫内のバーコードのスキャン](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | [GS1 バーコードと QR コード](../warehousing/gs1-barcodes.md) |
| 在庫&nbsp;および&nbsp;物流 | [在庫の可視化アドインの仮引当](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/soft-reservation-inventory-visibility-add-in) | [在庫の視覚化引当](../inventory/inventory-visibility-reservations.md) |
| 在庫&nbsp;および&nbsp;物流 | [リベート管理の控除および Catch Weight の強化](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/deduction-catch-weight-enhancements-rebate-management) | [控除ワークベンチを使用した控除の管理](../rebate-management/deduction-workbench.md )<br><br>[リベートの処理、確認、および転記](../rebate-management/process-review-post.md)<br><br>[リベート管理取引](../rebate-management/rebate-management-deals.md) |
| 在庫&nbsp;および&nbsp;物流 | [倉庫アプリのステップ指示](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [Warehouse Management モバイル アプリのステップ タイトルと手順のカスタマイズ](../warehousing/mobile-app-titles-instructions.md) |
| 在庫&nbsp;および&nbsp;物流 | [陸揚原価の作業の分割と追跡の更新](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/work-breaks-tracking-updates-landed-cost) | [プット アウェイの更新追跡](../landed-cost/update-tracking-putaway.md )<br><br>[輸送中の商品の処理](../landed-cost/in-transit-processing.md) |
| マスター プラン | [計画の最適化のマイナス在庫日数](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/negative-days-support-planning-optimization) | [遅延許容範囲 (マイナス日数)](../master-planning/planning-optimization/delay-tolerance.md) |

## <a name="feature-enhancements-included-in-this-release"></a>このリリースに含まれる機能拡張

次の表に、このリリースに含まれる機能拡張の一覧を示します。 これらの機能は、それぞれ既存の機能を段階的に改善します。 これらは拡張機能にすぎないため、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) には記載されません。 ただし、これらの拡張機能が既存のカスタマイズや基本設定と競合しないように、各機能は (特に断りのない限り) 既定でオフになっています。 これらの機能を使用する場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) で明示的にそれらを有効にする必要があります。

| モジュール | 機能&nbsp;管理の機能&nbsp;名&nbsp; | 詳細 |
|---|---|---|
| 原価管理 | 在庫決算の進捗状況の詳細 | このプレビュー機能により、在庫決算の進捗を詳細に表示できます。 |
| 調達 | 複数の購買要求がワークフロー内にある場合に一般予算引当の過剰消費を防止する | このプレビュー機能により、一般予算引当行の残りの残高を超える購買要求をユーザーが送信および承認する際のエラー チェックが向上します。 これにより、複数の購買要求がワークフローに含まれる場合に、一般予算引当の超過消費を防ぐのに役立ちます。 |
| 生産管理 | 生産フロア実行インターフェイスの完全なシリアル番号、バッチ番号、ライセンス プレート番号を表示する | この機能により、生産現場の実行インターフェイスでシリアル番号、バッチ番号、およびライセンス プレート番号のリストを表示し、さらに効率が向上します。 表示は、限られた文字数のカード ビューから、完全な値を表示するのに十分なスペースを提供するリスト ビューに変わります。 このリストは、特定の番号を検索する機能も提供します。 |
| 販売とマーケティング | 転記用に選択できる販売注文数を制限する | この機能を使用すると、販売注文リスト ページから確認書、ピッキング リスト、梱包明細、および請求書を転記する際に選択できる販売注文の最大数を定義できます。 自動的に有効になります。 この機能により、**転記用の最大販売注文数** という設定が、**売掛金勘定パラメータ** ページに追加されます。 新しい設定の既定値は *100* です。 この機能により、多数の販売注文が選択された場合に、販売注文リスト ページのパフォーマンスが向上します。 定期処理タスクで処理できる販売注文の数には影響しません。 |
| 倉庫管理 | ASN からのプットアウェイ作業を切り離す | この機能は、スケール 単位で (分散ハイブリッド トポロジの一部として) 倉庫管理ワークロードを実行している場合に、事前出荷明細通知 (ASN)を送受信するために必要です。 また、プットアウェイ作業に関する情報を格納するための専用の新しいデータベース テーブルが追加されます。 以前は、この情報は ASN 用のテーブルに格納されていました。 |
| 倉庫管理 | スロット混合単位 | システムでは、品目を混合ユニット (ボックスとケースの両方など) を含む場所に入れ込みます。 この機能を使用すると、スロッティングのテンプレート行ごとに、品目を混合ユニットまたは単一ユニットのどちらの場所にスロットするかを選択できます。 |
| 倉庫管理 | 梱包ステーションでコンテナーの終了/再オープンのために高速 API を使用する | このプレビュー機能を有効にすると、コンテナーに関連する在庫トランザクションが、新しい明るいプロセスを使用して作成されます。このプロセスにより、手作業の梱包ステーションを行う際のコンテナーの決算または再オープンのパフォーマンスが向上します。 |

## <a name="features-turned-on-by-default-in-this-release"></a>このリリースで、既定で有効になる機能

次の表に、10.0.21 で既定で有効になる機能の一覧を示します。 有効にした機能のほとんどは [機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) でオフにできます。

| 機能名 | 日付を有効にする | 機能の追加日 | 機能状態 | モジュール |
| :--- | :--- | :--- | :--- | :--- |
| 手持在庫レポート ストレージ | 2021/9/1 | 2020/4/1 | 既定で有効 | 在庫および倉庫管理 |
| 移動オーダーのキャンセル | 2021/9/1 | 2020/7/13 | 既定で有効 | 在庫および倉庫管理 |
| 在庫仕訳帳のロック解除 | 2021/9/1 | 2020/8/17 | 既定で有効 | 在庫および倉庫管理 |
| 在庫管理用に保存されているビュー | 2021/9/1 | 2020/9/30 | 既定で有効 | 在庫および倉庫管理 |
| BOM 明細行から BOM バージョンへのナビゲーション | 2021/9/1 | 2019/11/11 | 既定で有効 | 在庫および倉庫管理 |
| 在庫仕訳帳の測定単位と単位数量を使用する | 2021/9/1 | 2019/11/11 | 既定で有効 | 在庫および倉庫管理 |
| 空のバッチ属性値を許可する | 2021/9/1 | 2019/11/11 | 既定で有効 | 在庫および倉庫管理 |
| 在庫移動指示明細行の自動増分行番号 | 2021/9/1 | 2019/10/11 | 既定で有効 | 在庫および倉庫管理 |
| 在庫仕訳帳の承認ワークフロー | 2021/9/1 | 2020/1/6 | 既定で有効 | 在庫および倉庫管理 |
| 在庫品質管理パラメーターの警告機能の有効化 | 2021/9/1 | 2019/10/7 | 既定で有効 | 在庫および倉庫管理 |
| 販売明細行から移動オーダーを作成します | 2021/9/1 | 2019/8/31 | 既定で有効 | 在庫および倉庫管理 |
| 需要予測の詳細に対する予測モデルの選択 | 2021/9/1 | 2019/10/11 | 既定で有効 | マスター プラン |
| マスター プランの進行状況の視覚化 | 2021/9/1 | 2019/10/7 | 既定で有効 | マスター プラン |
| 計画最適化の自動確定 | 2021/9/1 | 2019/10/11 | 既定で有効 | マスター プラン |
| 計画オーダーの並行確定 | 2021/9/1 | 2019/8/31 | 既定で有効 | マスター プラン |
| 入札送信の成功メッセージ | 2021/9/1 | 2019/5/15 | 既定で有効 | 調達 |
| PO に追加された RFQ 参照リンク | 2021/9/1 | 2019/8/31 | 既定で有効 | 調達 |
| バッチで仕入先コラボレーションから受け入れた発注書を確認できます | 2021/9/1 | 2019/9/10 | 既定で有効 | 調達 |
| cXML の拡張機能の購入 | 2021/9/1 | 2019/11/11 | 既定で有効 | 調達 |
| &quot;公開済見積依頼を開く&quot; リンクをタイルとして表示する | 2021/9/1 | 2020/9/30 | 既定で有効 | 調達 |
| RFQ 質問と回答 | 2021/9/1 | 2020/2/19 | 既定で有効 | 調達 |
| 危険物の製品情報と出荷ドキュメント | 2021/9/1 | 2020/6/14 | 既定で有効 | 製品情報管理 |
| 既定の注文数量の厳密な検証 | 2021/9/1 | 2020/6/24 | 既定で有効 | 製品情報管理 |
| 原産国の管理機能 | 2021/9/1 | 2020/7/13 | 既定で有効 | 製品情報管理 |
| リリースされた製品用に保存されているビュー | 2021/9/1 | 2020/9/30 | 既定で有効 | 製品情報管理 |
| [承認ジョブ] と [転送ジョブ] ダイアログの機能強化 | 2021/9/1 | 2019/10/11 | 既定で有効 | 生産管理 |
| 完了報告用ライセンス プレートをジョブ カード デバイスに追加 | 2021/9/1 | 2019/8/31 | 既定で有効 | 生産管理 |
| 新しいボタンが [ジョブ カード ターミナル] ページに追加されました | 2021/9/1 | 2020/2/19 | 既定で有効 | 生産管理 |
| 外注品目の部分入庫を有効にし、仕入先タイプの BOM 明細行の仕損計算に関する問題を修正します。 | 2021/9/1 | 2019/11/11 | 既定で有効 | 生産管理 |
| 生産管理用に保存されているビュー | 2021/9/1 | 2020/8/17 | 既定で有効 | 生産管理 |
| 製造のための Dynamics 365 Guides | 2021/9/1 | 2020/7/13 | 既定で有効 | 生産管理 |
| 生産現場の実行 | 2021/9/1 | 2020/9/30 | 既定で有効 | 生産管理 |
| 画面ジョブカード デバイスとジョブ カード端末を除菌できるようにロックする機能 | 2021/9/1 | 2020/5/10 | 既定で有効 | 生産管理 |
| 販売注文の諸費用配賦 | 2021/9/1 | 2020/9/30 | 既定で有効 | 販売とマーケティング |
| 転記用に選択できる販売注文数を制限する | 2021/9/1 | 2021/9/1 | 既定で有効 | 販売とマーケティング |
| 販売注文更新履歴のクリーンアップ | 2021/9/1 | 2021/9/1 | 既定で有効 | 販売とマーケティング |
| 循環棚卸作業の番号順序の変更 | 2021/9/1 | 2019/10/7 | 既定で有効 | 倉庫管理 |
| タスクに基づくウェーブ需要補充 | 2021/9/1 | 2019/10/7 | 必須 | 倉庫管理 |
| &quot;すべての積荷&quot; ページおよび &quot;積荷詳細&quot; ページの [合計値] フィールドを非表示にする | 2021/9/1 | 2019/10/7 | 既定で有効 | 倉庫管理 |
| ウェーブ ラベル印刷 | 2021/9/1 | 2020/2/19 | 必須 | 倉庫管理 |
| 購買注文在庫トランザクションを積荷に関連付けます | 2021/9/1 | 2020/1/6 | 必須 | 倉庫管理 |
| 拡張ライセンス プレート ラベルのレイアウト | 2021/9/1 | 2020/2/19 | 既定で有効 | 倉庫管理 |
| 組織全体の作業のブロック | 2021/9/1 | 2020/2/19 | 必須 | 倉庫管理 |
| 作業ラインの詳細 | 2021/9/1 | 2019/10/11 | 既定で有効 | 倉庫管理 |
| モバイル デバイスの在庫移動の在庫状態フィールドを編集できるようにする | 2021/9/1 | 2019/10/16 | 既定で有効 | 倉庫管理 |
| バッチ ジョブからの出荷の確認 | 2021/9/1 | 2020/7/13 | 既定で有効 | 倉庫管理 |
| モバイル デバイスで入荷の概要ページを表示するかどうかを制御する | 2021/9/1 | 2020/4/1 | 既定で有効 | 倉庫管理 |
| あいまいな &#39;場所/ライセンス プレート&#39; の名前の解決を確認する | 2021/9/1 | 2020/4/1 | 既定で有効 | 倉庫管理 |
| 積荷品目入庫中に、倉庫管理アプリの製品バリアントと追跡用分析コードをキャプチャします | 2021/9/1 | 2020/5/10 | 既定で有効 | 倉庫管理 |
| ウェーブ積荷構築テンプレートの要件を満たしていない積荷を作成することは許可されません。 | 2021/9/1 | 2020/8/17 | 既定で有効 | 倉庫管理 |
| 複数 SKU の場所ディレクティブのすべてのアクションを評価する | 2021/9/1 | 2020/9/30 | 既定で有効 | 倉庫管理 |

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
