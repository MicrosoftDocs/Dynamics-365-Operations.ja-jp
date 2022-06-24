---
title: Dynamics 365 Supply Chain Management 10.0.27 のプレビュー (2022 年 7 月)
description: この記事では、Microsoft Dynamics 365 Supply Chain Management 10.0.27 の新機能または変更された機能について説明します。
author: kamaybac
ms.date: 04/22/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: a91f2cdae0fed75f07d6cae86d24aeedfca80e94
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844499"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10027-july-2022"></a>Dynamics 365 Supply Chain Management 10.0.27 のプレビュー (2022 年 7 月)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

この記事では、Microsoft Dynamics 365 Supply Chain Management プレビュー バージョン 10.0.27 の新機能または変更された機能について一覧表示します。 このバージョンのビルド番号は 10.0.1227 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2022 年 4 月
- **リリースの一般提供 (手動更新):** 2022 年 6 月
- **リリースの一般提供 (自動更新):** 2022 年 7 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 この記事が最初に公開された後に、ビルドに追加された機能を含めるために、この記事を更新することがあります。

| 機能領域 | フィーチャー | 詳細 |  に  によって有効化 |
|---|---|---|---|
| 在庫および物流 | [在庫の可視化アドインの在庫配賦](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-allocation-inventory-visibility-add-in) | [在庫の可視化の在庫配賦](../inventory/inventory-visibility-allocation.md) | 既定で有効 |
| 製造 | 生産現場の実行インターフェイスの [自分の 1 日の職務] ビュー | [作業者が生産フロア実行インターフェイスを使用する方法](../production-control/production-floor-execution-use.md)および[生産フロア実行インターフェイスで休暇残高を表示する](../production-control/production-floor-execution-payroll-stats.md) | 機能管理:<br>*生産現場の実行インターフェイスの [自分の 1 日の職務] ビュー* |
| 計画 | [外注の最適化サポートの計画](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-subcontracting) | [生産における外注作業の管理](../production-control/manage-subcontract-work-production.md) | 既定で有効 |

## <a name="feature-enhancements-included-in-this-release"></a>このリリースに含まれる機能拡張

次の表に、このリリースに含まれる機能拡張の一覧を示します。 これらの機能拡張は、それぞれ既存の機能を段階的に改善します。 これらは拡張機能にすぎないため、[リリース計画](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) には記載されません。 ただし、これらの拡張機能が既存のカスタマイズや基本設定と競合しないように、各機能は (特に断りのない限り) 既定でオフになっています。

これらの機能をオンまたはオフにする場合、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)で実行する必要があります。

| モジュール | 機能管理の機能名 | 詳細 |
|---|---|---|
| マスター プラン | 計画移動オーダーの作成時に在庫のリード タイムを考慮する | この機能は、計画移動オーダーの作成時、配送日管理設定の計画移動オーダーの入荷日を計算するときに、*なし* または *販売* タイプのリード タイムとして、品目の既定の注文設定で指定されている在庫のリード タイムを考慮します。 移動リード タイムが指定されている場合は、その値が入荷日の計算に使用され、配送日数は無視されます。 |
| 調達 | 仕入先請求明細行の既定のブローカー契約の税情報 | この機能は、ブローカー契約の仕入先請求明細行の **消費税** および **品目消費税** フィールドの既定値を設定するロジックを導入します。 このロジックは、ブローカー契約明細行の料金タイプが元帳/元帳の場合にのみ適用されます。 品目消費税グループは、仲買調達カテゴリ (設定されている場合) または費用タイプから既定値を取得します。 消費税グループは、仕入先アカウントから既定値を取得します。 |
| 調達 | バッチ タスクあたりの発注書明細行数の制限 | この機能により、確認および製品受領書を転記する時のシステムのパフォーマンスを最適化できます。 **タスクあたりの明細行数** という名前の新しい設定が、**調達パラメーター** ページの **配送** タブに追加されます。 この新しい設定により、各バッチ タスクで処理する購買注文明細行の数を制限することができます。 したがって、大規模なバッチ タスクによるシステムのパフォーマンスの低下を回避できます。 |
| 製品情報管理 | 製品属性値の設定 | この機能により、*製品属性値の設定* という名前の定期処理タスクが追加されます。 この新しい定期処理タスクでは、製品カテゴリを介して製品に関連付けられている属性に対して、欠けている製品属性値レコードが作成されます。 |
| 生産管理 | 生産現場の実行インターフェイス上の追加の構成 | <p>この機能は、**生産現場の実行の構成** ページに次のオプションを追加します。</p><ul><li>**検索の完了時に開始ダイアログを自動的に開く** – このオプションが有効にされている場合、作業者が検索バーを使用してジョブを検索すると、**ジョブの開始** ダイアログ ボックスが自動的に開きます。</li><li>**検索の完了時にレポート進捗状況ダイアログを自動的に開く** – このオプションが有効な場合、作業者が検索バーを使用してジョブを検索すると、ジョブの **レポート進捗状況** ダイアログ ボックスが自動的に開きます。</li><li>**レポート進捗状況ダイアログの既定の残余数量** – このオプションが有効な場合、**レポート進捗状況** ダイアログ ボックスに、生産ジョブで報告する残余数量が表示されます。</li></ul><p>詳細情報については、[生産現場の実行インターフェースを構成する](../production-control/production-floor-execution-configure.md)を参照してください。</p> |
| 生産管理 | 生産現場の実行インターフェイスの生産チーム | <p>同じ生産ジョブに複数の作業者が割り当てられた場合、1 人の作業者をパイロットとして推薦できるようになりました。 残りの作業者は自動的にそのパイロットのアシスタントになります。 それによって編成されたチームでは、パイロットのみがジョブの状態を登録する必要があります。一方、時間レコードはすべてのチーム メンバーに適用されます。 この機能は、*アシスト リソース* という名前のシナリオもサポートしています。 このシナリオでは、ある作業者が別の作業者のアシスタントとして登録され、新たに編成されたグループのパイロットにすることができます。</p><p>詳細情報については、[作業者が生産現場の実行インターフェースを使用する方法](../production-control/production-floor-execution-use.md)を参照してください。</p> |
| 生産管理 | 生産現場の実行インターフェイスでの計画品目に関するレポート | この機能により、生産フロア実行インターフェイス内の計画品目のバッチ オーダーに関するレポート プロセスが簡略化されます。 生産タイプが *計画品目* の製品に対してバッチ オーダーを作成した場合は、そのバッチ オーダーの連産品および副産物においてのみ、完了として報告することができます。 計画品目のバッチ オーダーは、原材料製品が複数の特徴的製品に分解される分解プロセスをサポートするために通常使用されます。 作業者が計画品目のバッチ オーダーを完了として報告すると、**レポートの進捗状況** ダイアログ ボックスに連産品と副産物のみが表示されるようになりました。 以前は計画品目も表示されていたため、この動作は作業者に混乱を招いていました。 |

## <a name="new-and-updated-documentation-resources"></a>新しいドキュメント リソースおよび更新されたドキュメント リソース

次のヘルプ記事を最近追加、または大幅に更新しました。 これらの記事は、前のセクションに示したように、このリリースで追加された新しい機能に関連するとは限りません。 ただし、これらの機能は既存の機能をさらに活用するために役立つ場合があります。

| 機能領域 | 新規または更新された記事 |
|---|---|
| 原価管理 | [現物価格とマーキングを含めた加重平均](../cost-management/weighted-average-date.md) |
| 配分済みハイブリッド トポロジ | [分散ハイブリッド トポロジのスケール ユニットを試す](../cloud-edge/cloud-edge-try-out.md) |
| 二重書き込み | [Supply Chain Management の価格決定エンジンとのオンデマンド同期](../../fin-ops-core/dev-itpro/data-entities/dual-write/pricing-engine.md) |
| 倉庫管理 | [倉庫へのリリース](../warehousing/release-to-warehouse-process.md) |

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Microsoft Dynamics 365 Supply Chain Management 10.0.27 には、Platform updates が含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.27 のプラットフォーム更新プログラム (2022 年 6 月)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-27.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正

10.0.27 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271) を参照してください。

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 および業界クラウド: 2022 年リリース ウェーブ 1 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365 および業界クラウド: 2022 年リリース ウェーブ 1 プラン](/dynamics365-release-plan/2022wave1/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-supply-chain-management-features"></a>削除済みおよび非推奨の Supply Chain Management 機能

[Dynamics 365 Supply Chain Management の削除済みおよび非推奨の機能](removed-deprecated-features-scm-updates.md)の記事は、Supply Chain Management で削除または非推奨となる予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Supply Chain Management の削除済みまたは非推奨の機能](removed-deprecated-features-scm-updates.md)の記事に発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
