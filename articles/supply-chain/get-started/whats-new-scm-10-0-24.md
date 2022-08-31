---
title: Dynamics 365 Supply Chain Management 10.0.24 の新機能および変更された機能 (2022 年 2 月)
description: この記事では、Microsoft Dynamics 365 Supply Chain Management 10.0.24 の新機能または変更された機能について説明します。
author: kamaybac
ms.date: 12/03/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 9b4b538e6d50013626739e19fee2a050b630bf7f
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334808"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10024-february-2022"></a>Dynamics 365 Supply Chain Management 10.0.24 の新機能および変更された機能 (2022 年 2 月)

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Supply Chain Management バージョン 10.0.24 の新機能または変更された機能について一覧表示します。 このバージョンには 10.0.1084 のビルド番号が含まれており、次のように使用できます。

- **リリースのプレビュー:** 2021 年 12 月
- **リリースの一般提供 (手動更新):** 2022 年 1 月
- **リリースの一般提供 (自動更新):** 2022 年 2 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 この記事が最初に公開された後に、ビルドに加えた機能を含めるために、この記事を更新することがあります。

| 機能領域 | フィーチャー | 詳細 |  に  によって有効化 |
|---|---|---|---|
| 配分済みハイブリッド トポロジ | [スケール ユニットでの倉庫実行ワークロードの拡張](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-warehouse-execution-workloads-scale-units) | [クラウドおよびエッジのスケール ユニットに対する倉庫管理ワークロード](../cloud-edge/cloud-edge-workload-warehousing.md) | 既定で有効になっています。 |
| 配分済みハイブリッド トポロジ | [クラウドおよびエッジ スケール ユニットに対する倉庫管理ワークロードでの製造オーダーの開始](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-manufacturing-execution-workloads-scale-units) | [クラウドおよびエッジのスケール ユニットに対する製造実行ワークロード](../cloud-edge/cloud-edge-workload-manufacturing.md) | 機能管理 (*クラウドおよびエッジ スケール ユニットに対する倉庫管理ワークロードでの製造オーダーの開始*)  |
| 計画 | [再発注マージンと発行マージンに対する計画最適化サポート](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-reorder-margin-issue-margin) | [安全マージン](../master-planning/planning-optimization/safety-margins.md) | 既定で有効になっています。 |

## <a name="feature-enhancements-included-in-this-release"></a>このリリースに含まれる機能拡張

次の表に、このリリースに含まれる機能拡張の一覧を示します。 これらの機能拡張は、それぞれ既存の機能を段階的に改善します。 これらは拡張機能にすぎないため、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) には記載されません。 ただし、これらの拡張機能が既存のカスタマイズや基本設定と競合しないように、各機能は (特に断りのない限り) 既定でオフになっています。

これらの機能をオンまたはオフにする場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) で実行する必要があります。

| モジュール | 機能管理の機能名 | 詳細 |
|---|---|---|
| 生産管理 | 製造オーダーの材料の在庫状態のオンデマンド チェック | この機能を使用すると、**生産フロアの管理** ワークスペースから使用できる **リリースする製造オーダー** ページをすばやく開くことができます。 この機能がない場合は、ページを開くとすぐに、リストされている製造オーダーすべてに対して資材が使用可能かどうかをシステムが自動的に確認するため、大量の注文がある場合はかなりの時間がかかる場合があります。 この機能を有効にすると、システムはツール バー ボタンを代わりに提供し、選択した注文に対してのみ必要な場合に資材の確認を開始できます。 |
| 生産管理 | 生産現場の実行インターフェースで材料消費を登録する (WMS 非対応) | この機能により、作業員は生産フロア実行インターフェイスを使用して材料消費、バッチ番号、およびシリアル番号を登録できます。 この機能では、倉庫管理プロセス (WMS) を使用できない品目のみをサポートします。 WMS 対応の品目のサポートは、今後のリリースで予定されています。<p>一部のメーカー、特にプロセス業界のメーカーでは、各バッチまたは製造オーダーで消費される材料の量を明示的に登録する必要があります。 たとえば、作業者はスケールを使用して、作業時に消費される材料の量を計量できます。 完全な材料トレーサビリティを確保するために、組織では各製品の生産時に消費されたバッチ番号も登録する必要があります。 |
| 生産管理 | クラウドおよびエッジ スケール ユニットに対する倉庫管理ワークロードの完了レポート | この機能を使用すると、作業者は、Warehouse Management モバイル アプリを使用して、クラウドまたはエッジ スケール ユニットの倉庫管理ワークロードに対してアプリが実行されている場合に、製造オーダーまたはバッチ オーダーを完了として報告できます。 詳細については、[スケール ユニットでの完了レポートとプットアウェイ レポート](../cloud-edge/cloud-edge-workload-manufacturing.md#RAF) を参照してください。 |
| 倉庫管理 | 新しい積荷計画ワークベンチ ページ | 2 つの新しい積荷計画ワークベンチ ページを追加しました: **入庫積荷計画ワークベンチ** と **出庫積荷計画ワークベンチ**。 |

## <a name="new-and-updated-documentation-resources"></a>新しいドキュメント リソースおよび更新されたドキュメント リソース

次のヘルプ記事を最近追加、または大幅に更新しました。 これらの記事は、前のセクションに示したように、このリリースで追加された新しい機能に関連するとは限りません。 ただし、これらの機能は既存の機能をさらに活用するために役立つ場合があります。

| 機能領域 | 新規または更新された記事 |
|---|---|
| 原価管理 | [在庫金額レポート](../cost-management/inventory-value-report-storage.md) |
| 原価管理 | [在庫金額レポートの例とロジック](../cost-management/inventory-value-report-examples.md) |
| マスター プラン | [計画の最適化で使用される日付と時刻のパラメーター](../master-planning/planning-optimization/date-time-used.md) |
| マスター プラン | [需要予測の設定](../master-planning/demand-forecasting-setup.md) |
| マスター プラン | [安全在庫仕訳帳を使用して品目の最小補充を更新します](../master-planning/safety-stock-journal.md) |
| 生産管理 | [生産現場の実行インターフェースのカスタマイズ](../production-control/production-floor-execution-customize.md) |
| 生産管理 | [生産現場の実行インターフェースのスタイル](../production-control/production-floor-execution-styles.md) |
| 販売とマーケティング | [販売履歴データのクリーンアップをスケジュールする](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) |
| 倉庫管理 | [モバイル デバイスのユーザー アカウント](../warehousing/mobile-device-work-users.md) |

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Microsoft Dynamics 365 Supply Chain Management 10.0.24 には、Platform updates が含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.24 のプラットフォーム更新プログラム (2022 年 2 月)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-24.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正

10.0.24 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=641306&dbType=3&qc=5b1d5e49c96b8a5cfb5601889a413e6f3773ba6500f9bc47310dcc5c54fff42f) を参照してください。

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 および業界のクラウド: 2021年リリース ウェーブ 2 プラン

当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365 および業界のクラウド: 2021年リリース ウェーブ 2 プラン](/dynamics365-release-plan/2021wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-supply-chain-management-features"></a>削除済みおよび非推奨の Supply Chain Management 機能

[Dynamics 365 Supply Chain Management の削除済みおよび非推奨の機能](removed-deprecated-features-scm-updates.md)の記事は、Supply Chain Management で削除または非推奨となる予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Dynamics 365 Supply Chain Management の削除済みまたは非推奨の機能](removed-deprecated-features-scm-updates.md)の記事に発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および運用環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

