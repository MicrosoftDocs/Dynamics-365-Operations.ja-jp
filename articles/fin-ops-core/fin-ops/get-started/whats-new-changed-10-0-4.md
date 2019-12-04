---
title: Finance and Operations バージョン 10.0.4 (2019 年 7 月) の新機能および変更点
description: このトピックでは、Dynamics 365 for Finance and Operations バージョン 10.0.4 の新機能または変更された機能について説明します。 このバージョンは 7 月にリリースされます。
author: tonyafehr
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.4
ms.openlocfilehash: 06457de238fbb49f8b3b30ed69fb935219bb5544
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811471"
---
# <a name="whats-new-or-changed-in-finance-and-operations-version-1004-july-2019"></a>Finance and Operations バージョン 10.0.4 (2019 年 7 月) の新機能および変更点

[!include [banner](../includes/banner.md)]


このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.4 の新機能または変更された機能について説明します。 このバージョンは 7 月にリリースされ、ビルド番号は 10.0.136 です。 バージョン 10.0.4 の詳細については [追加リソース](whats-new-changed-10-0-4.md#additional-resources) を参照してください。



## <a name="set-up-interest-distribution-for-cash-accounts-public-sector"></a>現金勘定の利息配分の設定 (公的機関)
代理店は、現金勘定の日毎の平均残高に基づいて、銀行口座の利子を特定の総勘定元帳に割り当てる (分配する) ことができます。 このプロセスを使用して、利息金額の詳細な元帳エントリを生成できます。 また、転記せずにレビュー用の利息額を生成できます。

詳細については [現金勘定の利息配布の設定](https://go.microsoft.com/fwlink/?linkid=2088607) を参照してください。

## <a name="budget-analysis-report-public-sector"></a>予算分析レポート (公共部門)
予算分析の照会と同様に、新しい **予算分析** レポートを使用して、予算金額を指定期間中の実績費用および収益活動と比較する集計レポートを生成します。 勘定科目ごとに、予算金額、実績費用または収益、発注からの予算引当金額および購買依頼からの予算引当金額がレポート上で一覧表示されます。 さらに、このレポートには、各勘定科目および資金の予算残高が一覧表示されます。

詳細については、 [予算分析レポート](https://go.microsoft.com/fwlink/?linkid=2087447)を参照してください。

## <a name="regulatory-updates"></a>規制の更新
Finance and Operations の規制の更新については、[規制の更新](../../../finance/localizations/regulatory-updates.md) を参照してください。 また、Lifecycle Services (LCS) にログインし、国、機能のタイプ、およびリリースを検索できる問題検索ツールを使用して、計画された規制の更新を表示することができます。

## <a name="additional-resources"></a>追加リソース

### <a name="bug-fixes"></a>バグ修正
Finance and Operations 10.0.4 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=328732&dbType=3&qc=cdb2117c03722ee9cdbcb2a2e0558dd5b40a37e3caa32850aca4c9a89c476eb2)を参照してください。

### <a name="platform-update-28"></a>プラットフォーム update 28
Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.4 には、プラットフォーム更新プログラム 28 が含まれています。 プラットフォーム更新プログラム 28 の詳細については、[Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 28 (2019 年 7 月) の新機能または変更された機能について](whats-new-platform-update-28.md)を参照してください。

### <a name="dynamics-365-april-19-release-notes"></a>Dynamics 365 2019 年 4 月 リリース ノート
当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[2019 年 4 月リリース ノートをご覧ください](https://docs.microsoft.com/business-applications-release-notes/April19/index)。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能
[Finance and Operations の削除済みまたは推奨されない機能](../../dev-itpro/migration-upgrade/deprecated-features.md)のトピックでは、Dynamics 365 for Finance and Operations の削除済みまたは非推奨の機能について説明します。

- *削除された*機能は製品では使用できません。
- *削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に[Finance and Operations の削除済みまたは推奨されない機能](../../dev-itpro/migration-upgrade/deprecated-features.md)のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。
