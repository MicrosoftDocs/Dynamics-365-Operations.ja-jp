---
title: Dynamics 365 Supply Chain Management 10.0.30 のプレビュー (2022 年 11 月)
description: この記事では、Microsoft Dynamics 365 Supply Chain Management 10.0.30 の新機能または変更された機能について説明します。
author: kamaybac
ms.date: 09/08/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-09-08
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 18fec49f2388159cae0809c63685102a04e90c57
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689192"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10030-november-2022"></a>Dynamics 365 Supply Chain Management 10.0.30 (2022 年 11 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Supply Chain Management バージョン 10.0.30 の新機能または変更された機能について一覧表示します。 このバージョンのビルド番号は 10.0.1362 で、次のスケジュールで使用できます。

- **リリースのプレビュー:** 2022 年 9 月
- **リリースの一般提供 (手動更新):** 2022 年 10 月
- **リリースの一般提供 (自動更新):** 2022 年 11 月

## <a name="features-included-in-this-release"></a>このリリースに含まれる機能

次の表に、このリリースに含まれる機能の一覧を示します。 この記事が最初に公開された後に、ビルドに追加された機能を含めるために、この記事を更新することがあります。

| 機能領域 | フィーチャー | 詳細 |  に  によって有効化 |
|---|---|---|---|
| 製造 | [Sensor Data Intelligence を使用した機器の監視](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/monitor-equipment-sensor-data-intelligence) | [Sensor Data Intelligence のホーム ページ](../sensor-data-intelligence/sdi-home-page.md) | 機能管理:<br>*(プレビュー) センサー データ インテリジェンス* |
| 倉庫管理 | [Warehouse Management モバイル アプリの複数レベルの迂回](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/multi-level-detours-warehouse-management-mobile-app) | [モバイル デバイス メニュー項目のステップの迂回を構成する](../warehousing/warehouse-app-detours.md) | 機能管理:<br>*Warehouse Management モバイル アプリの複数レベルの迂回* |

## <a name="feature-enhancements-included-in-this-release"></a>このリリースに含まれる機能拡張

次の表に、このリリースに含まれる機能拡張の一覧を示します。 これらの機能拡張は、それぞれ既存の機能を段階的に改善します。 これらは拡張機能にすぎないため、[リリース計画](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) には記載されません。 ただし、これらの拡張機能が既存のカスタマイズや基本設定と競合しないように、各機能は (特に断りのない限り) 既定でオフになっています。

これらの機能をオンまたはオフにする場合、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)で実行する必要があります。

| モジュール | 機能管理の機能名 | 詳細 |
|---|---|---|
| 生産管理 | リリース ページへの製造オーダーが含む手持在庫情報 | **リリースする製造オーダー** ページの明細行セクションにある明細行品目の手持在庫数量に列を追加しました。 |
| 輸送管理 | 関連するルート区分への出荷の割り当て | この機能により、1 つのルートに沿ってさまざまな区分の出荷先に出荷される複数の出荷を含む荷物の場合も含め、出荷運賃の正確な償却が可能になります。 各出荷は、出荷とセグメントの送付先住所に基づいて、各出荷を最も適切なルート セグメントに割り当てる必要があります。 次に、この機能は、各出荷の運賃コストを、出荷の相対的な重量、量、数量、および移動距離に基づいて、荷物の合計運賃の割合として計算します。 この機能は、輸送管理 (KMS) モジュールを使用して管理される出荷にのみ適用されます。 |

## <a name="additional-resources"></a>追加リソース

### <a name="platform-updates-for-finance-and-operations-apps"></a>財務と運用アプリのプラットフォーム更新プログラム

Microsoft Dynamics 365 Supply Chain Management 10.0.30 には、Platform updates が含まれています。 詳細については、[財務と運用アプリのバージョン 10.0.30 のプラットフォーム更新プログラム (2022 年 11 月)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md) を参照してください。

### <a name="bug-fixes"></a>バグ修正

バージョン 10.0.29 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468) を参照してください。

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
