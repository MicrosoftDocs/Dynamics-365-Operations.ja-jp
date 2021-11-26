---
title: Dynamics 365 Supply Chain Management 10.0.22 (2021 年 11 月) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management 10.0.22 の新機能または変更された機能について説明します。
author: kamaybac
ms.date: 08/09/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: a795f88aed78582ad4a2faa90ab1c2529017850f
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778160"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10022-november-2021"></a>Dynamics 365 Supply Chain Management 10.0.22 (2021 年 11 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management バージョン 10.0.22 の新機能または変更された機能について一覧表示します。 このバージョンには 10.0.995 のビルド番号が含まれており、次のように使用できます。

- **リリースのプレビュー:** 2021 年 9 月
- **リリースの一般提供 (手動更新):** 2021 年 10 月
- **リリースの一般提供 (自動更新):** 2021 年 11 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 *機能* 列には、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) へのリンクがあり、各機能の公式リリース日を確認できます。 *詳細情報* 列には、詳細情報や関連ドキュメントへのリンクが表示されます。 機能を有効にする方法を確認するには、*有効化* 列を参照してください。 機能管理の使用方法の詳細については [機能管理の概要](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。 このトピックが最初に公開された後に、ビルドに加えた機能を含めるために、このトピックを更新することがあります。

| 機能領域 | フィーチャー | 詳細 |  に  によって有効化 |
|---|---|---|---|
| 計画 | [機能ベースのリソース割り当ての最適化サポート計画](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capability-based-resource-allocation) | [能力に基づいたリソースの選択を使用したスケジュール設定](../master-planning/planning-optimization/capability-based-scheduling.md) | 機能管理 (*計画最適化の無限能力のスケジューリング*) |

## <a name="feature-enhancements-included-in-this-release"></a>このリリースに含まれる機能拡張

次の表に、このリリースに含まれる機能拡張の一覧を示します。 これらの機能拡張は、それぞれ既存の機能を段階的に改善します。 これらは拡張機能にすぎないため、[リリース計画](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) には記載されません。 ただし、これらの拡張機能が既存のカスタマイズや基本設定と競合しないように、各機能は (特に断りのない限り) 既定でオフになっています。 これらの機能を使用する場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) で明示的にそれらを有効にする必要があります。

| モジュール | 機能管理の機能名 | 詳細 |
|---|---|---|
| 配分済みハイブリッド トポロジ | *(機能管理は必要ありません。)* | <p>このリリースでは、クラウドおよびエッジのスケール ユニットの倉庫管理ワークロードに対する出庫積荷計画機能が展開されます。</p><p>詳細については、[クラウドおよびエッジのスケール ユニットに対する倉庫管理ワークロード](../cloud-edge/cloud-edge-workload-warehousing.md) を参照してください。</p> |
| エンジニアリング変更管理 | エンジニアリング製品のバリアントの生成 | <p>この機能により、エンジニアリング製品に対して、その色、サイズ、スタイル、またはコンフィギュレーションの分析コードに基づいて複数のバリアントを生成できます。</p><p>詳細については、[エンジニアリング製品のバリアントの生成](../engineering-change-management/engineering-variants.md) を参照してください。</p> |
| 在庫および倉庫管理 | 引当相殺との在庫品目一覧の統合 | <p>この機能を有効にできるのは、*在庫の視覚化統合* 機能を有効にした後のみです。 在庫の視覚化で作成された引当を相殺する機能を提供します。</p><p>詳細については、[在庫の視覚化引当](../inventory/inventory-visibility-reservations.md) を参照してください。</p> |

## <a name="new-and-updated-documentation-resources"></a>新しいドキュメント リソースおよび更新されたドキュメント リソース

次のヘルプ トピックが最近追加されたか大幅に更新されました。 これらのトピックは、前のセクションに示したように、このリリースで追加された新しい機能に関連するとは限りません。 ただし、これらの機能は既存の機能をさらに活用するために役立つ場合があります。

| 機能領域 | 新規または更新されたトピック |
|---|---|
| エンジニアリング変更管理 | [エンジニアリング変更管理の概要](../engineering-change-management/product-engineering-overview.md) に、機能管理で使用できるすべての関連機能およびオプション機能が一覧表示するようになりました |
| マスター プラン | [需要予測の設定](../master-planning/demand-forecasting-setup.md) |
| マスター プラン | [計画の最適化を使用した正味必要量およびペギング情報](../master-planning/planning-optimization/net-requirements.md) |
| 倉庫管理 | [倉庫へのリリース ](../warehousing/release-to-warehouse-process.md) では、倉庫プロセスへの完全リリースの詳細な概要が提供されます |

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations アプリのプラットフォーム更新プログラム

Microsoft Dynamics 365 Supply Chain Management 10.0.22 には、Platform updates が含まれています。 詳細については、[Finance and Operations アプリのバージョン 10.0.22 (2021 年 11 月) のプラットフォーム更新プログラム](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正

10.0.22 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=615299) を参照してください。

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
