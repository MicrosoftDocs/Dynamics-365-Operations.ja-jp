---
title: Finance and Operations バージョン 10.0.4 (2019 年 7 月) の機能のプレビュー
description: このトピックでは、Dynamics 365 for Finance and Operations バージョン 10.0.4 の新機能または変更された機能について説明します。 このバージョンは 7 月にリリースされます。
author: tonyafehr
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.4
ms.openlocfilehash: 51f2740f629a12ff9e144aa70b02928a61e886a3
ms.sourcegitcommit: c576b81dc3c93c09fb08fb0ba0c19f417360c5ab
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/05/2019
ms.locfileid: "1620003"
---
# <a name="preview-features-in-finance-and-operations-version-1004-july-2019"></a><span data-ttu-id="d4025-104">Finance and Operations バージョン 10.0.4 (2019 年 7 月) の機能のプレビュー</span><span class="sxs-lookup"><span data-stu-id="d4025-104">Preview features in Finance and Operations version 10.0.4 (July 2019)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="d4025-105">このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.4 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="d4025-105">This topic describes features that are either new or changed in Microsoft Dynamics 365 for Finance and Operations version 10.0.4.</span></span> <span data-ttu-id="d4025-106">このバージョンは 7 月にリリースされ、ビルド番号は 10.0.136 です。</span><span class="sxs-lookup"><span data-stu-id="d4025-106">This version will be released in July and has a build number of 10.0.136.</span></span> <span data-ttu-id="d4025-107">バージョン 10.0.4 の詳細については [追加リソース](whats-new-changed-10-0-4.md#additional-resources) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d4025-107">For more information about version 10.0.4, see [Additional resources](whats-new-changed-10-0-4.md#additional-resources).</span></span>



## <a name="set-up-interest-distribution-for-cash-accounts"></a><span data-ttu-id="d4025-108">現金勘定の利息配分の設定</span><span class="sxs-lookup"><span data-stu-id="d4025-108">Set up interest distribution for cash accounts</span></span>
<span data-ttu-id="d4025-109">代理店は、現金勘定の日毎の平均残高に基づいて、銀行口座の利子を特定の総勘定元帳に割り当てる (分配する) ことができます。</span><span class="sxs-lookup"><span data-stu-id="d4025-109">Your agency can allocate (distribute) the interest on a bank account to specific General ledger accounts, based on the average daily balance in cash accounts.</span></span> <span data-ttu-id="d4025-110">このプロセスを使用して、利息金額の詳細な元帳エントリを生成できます。</span><span class="sxs-lookup"><span data-stu-id="d4025-110">You can use this process to generate an advanced ledger entry for the interest amounts.</span></span> <span data-ttu-id="d4025-111">また、転記せずにレビュー用の利息額を生成できます。</span><span class="sxs-lookup"><span data-stu-id="d4025-111">Alternatively, you can generate the interest amounts for review, without posting them.</span></span>

<span data-ttu-id="d4025-112">詳細については [現金勘定の利息配布](https://go.microsoft.com/fwlink/?linkid=2088607) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d4025-112">For more information, see [Interest distribution for cash accounts](https://go.microsoft.com/fwlink/?linkid=2088607).</span></span>

## <a name="budget-analysis-report-public-sector"></a><span data-ttu-id="d4025-113">予算分析レポート (公共部門)</span><span class="sxs-lookup"><span data-stu-id="d4025-113">Budget analysis report (Public Sector)</span></span>
<span data-ttu-id="d4025-114">予算分析の照会と同様に、新しい **予算分析** レポートを使用して、予算金額を指定期間中の実績費用および収益活動と比較する集計レポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="d4025-114">Similar to the Budget analysis inquiry, you can now use the new **Budget analysis** report to generate a summarized report that compares budgeted amounts to actual expense and revenue activity during a period that you specify.</span></span> <span data-ttu-id="d4025-115">勘定科目ごとに、予算金額、実績費用または収益、発注からの予算引当金額および購買依頼からの予算引当金額がレポート上で一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="d4025-115">For each account, the report lists budgeted amounts, actual expenses or revenue, encumbrance amounts from purchase orders, and pre-encumbrance amounts from purchase requisitions.</span></span> <span data-ttu-id="d4025-116">さらに、このレポートには、各勘定科目および資金の予算残高が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="d4025-116">Additionally, the report lists the remaining budget amount for each account and fund.</span></span>

<span data-ttu-id="d4025-117">詳細については、 [予算分析レポート](https://go.microsoft.com/fwlink/?linkid=2087447)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d4025-117">For more information, see [Budget analysis report](https://go.microsoft.com/fwlink/?linkid=2087447).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d4025-118">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d4025-118">Additional resources</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d4025-119">バグ修正</span><span class="sxs-lookup"><span data-stu-id="d4025-119">Bug fixes</span></span>
<span data-ttu-id="d4025-120">Finance and Operations 10.0.4 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=328732&dbType=3&qc=cdb2117c03722ee9cdbcb2a2e0558dd5b40a37e3caa32850aca4c9a89c476eb2)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d4025-120">For information about the bug fixes included in each of the updates that are part of Finance and Operations version 10.0.4, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=328732&dbType=3&qc=cdb2117c03722ee9cdbcb2a2e0558dd5b40a37e3caa32850aca4c9a89c476eb2).</span></span>

### <a name="platform-update-28"></a><span data-ttu-id="d4025-121">プラットフォーム update 28</span><span class="sxs-lookup"><span data-stu-id="d4025-121">Platform update 28</span></span>
<span data-ttu-id="d4025-122">Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.4 には、プラットフォーム更新プログラム 28 が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d4025-122">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 includes Platform update 28.</span></span> <span data-ttu-id="d4025-123">プラットフォーム更新プログラム 28 については [Finance and Operations プラットフォーム更新プログラム 28 (2019 年 7 月) のプレビュー機能](whats-new-platform-update-28.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d4025-123">To learn more about Platform update 28, see [Preview features in Finance and Operations platform update 28 (July 2019)](whats-new-platform-update-28.md).</span></span>

### <a name="dynamics-365-april-19-release-notes"></a><span data-ttu-id="d4025-124">Dynamics 365 2019 年 4 月 リリース ノート</span><span class="sxs-lookup"><span data-stu-id="d4025-124">Dynamics 365 April '19 release notes</span></span>
<span data-ttu-id="d4025-125">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="d4025-125">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="d4025-126">[2019 年 4 月リリース ノートをご覧ください](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/index)。</span><span class="sxs-lookup"><span data-stu-id="d4025-126">[Check out the April '19 release notes](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/index).</span></span> <span data-ttu-id="d4025-127">あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="d4025-127">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-features"></a><span data-ttu-id="d4025-128">削除済みおよび非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="d4025-128">Removed and deprecated features</span></span>
<span data-ttu-id="d4025-129">[削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックは Dynamics 365 for Finance and Operations の削除済みまたは非推奨の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="d4025-129">The [Removed or deprecated features](../../dev-itpro/migration-upgrade/deprecated-features.md) topic describes features that have been removed or deprecated for Dynamics 365 for Finance and Operations.</span></span>

- <span data-ttu-id="d4025-130">*削除された*機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="d4025-130">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="d4025-131">*削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d4025-131">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="d4025-132">製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。</span><span class="sxs-lookup"><span data-stu-id="d4025-132">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features](../../dev-itpro/migration-upgrade/deprecated-features.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="d4025-133">コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。</span><span class="sxs-lookup"><span data-stu-id="d4025-133">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="d4025-134">通常、これらはコンパイラに加える必要がある機能の更新です。</span><span class="sxs-lookup"><span data-stu-id="d4025-134">Typically, these are functional updates that need to be made to the compiler.</span></span>
