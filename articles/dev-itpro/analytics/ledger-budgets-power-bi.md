---
title: "実績対予算 Power BI コンテンツ"
description: "このトピックでは、実績対予算 Power BI コンテンツについて説明します。 コンテンツに含まれているレポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。"
author: ryansandness
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: 2a0ad5af4e4d7da09690331dc9d1a51d2e97a664
ms.contentlocale: ja-jp
ms.lasthandoff: 12/01/2017

---

# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="39dd7-104">実績対予算 Power BI コンテンツ</span><span class="sxs-lookup"><span data-stu-id="39dd7-104">Actual vs budget Power BI content</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="39dd7-105">このトピックでは、[**実績対予算**] Microsoft Power BI コンテンツについて説明します。</span><span class="sxs-lookup"><span data-stu-id="39dd7-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="39dd7-106">Power BI レポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="39dd7-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span> 

# <a name="overview"></a><span data-ttu-id="39dd7-107">概要</span><span class="sxs-lookup"><span data-stu-id="39dd7-107">Overview</span></span>

<span data-ttu-id="39dd7-108">[**実績対予算**] Power BI コンテンツは、組織内で実績対予算パフォーマンスの監視を担当する各個人に対して作成されました。</span><span class="sxs-lookup"><span data-stu-id="39dd7-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="39dd7-109">[**実績対予算**] Power BI コンテンツは、予算差異の可視性を提供します。</span><span class="sxs-lookup"><span data-stu-id="39dd7-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="39dd7-110">勘定カテゴリ、予算コード、主勘定、主勘定の説明、または差異の原因をより良く理解するための会計年度期間ごとに、今年度の予算を分析できます。</span><span class="sxs-lookup"><span data-stu-id="39dd7-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span> 

# <a name="accessing-the-power-bi-content"></a><span data-ttu-id="39dd7-111">Power BI コンテンツへのアクセス</span><span class="sxs-lookup"><span data-stu-id="39dd7-111">Accessing the Power BI content</span></span>
<span data-ttu-id="39dd7-112">**実績対予算** Power BI コンテンツからのレポートは、**元帳予算および予測** および **CFO** ワークスペースで表示されます。</span><span class="sxs-lookup"><span data-stu-id="39dd7-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

# <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="39dd7-113">Power BI コンテンツに含まれるレポート</span><span class="sxs-lookup"><span data-stu-id="39dd7-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="39dd7-114">次の表は、[**実績対予算**] Power BI コンテンツの各レポート ページに表示されるメトリックスの詳細について説明しています。</span><span class="sxs-lookup"><span data-stu-id="39dd7-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="39dd7-115">レポート </span><span class="sxs-lookup"><span data-stu-id="39dd7-115">Report</span></span>                      | <span data-ttu-id="39dd7-116">メトリックス</span><span class="sxs-lookup"><span data-stu-id="39dd7-116">Metrics</span></span> |
|-----------------------------|---------|
| <span data-ttu-id="39dd7-117">経費 - 実績対予算</span><span class="sxs-lookup"><span data-stu-id="39dd7-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="39dd7-118">今年度の経費合計</span><span class="sxs-lookup"><span data-stu-id="39dd7-118">Total expenses this year</span></span></li><li><span data-ttu-id="39dd7-119">今年度の合計経費予算</span><span class="sxs-lookup"><span data-stu-id="39dd7-119">Budget total expenses this year</span></span></li></ul> |
| <span data-ttu-id="39dd7-120">収益 - 実績対予算</span><span class="sxs-lookup"><span data-stu-id="39dd7-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="39dd7-121">今年度の総収益</span><span class="sxs-lookup"><span data-stu-id="39dd7-121">Total revenue this year</span></span></li><li><span data-ttu-id="39dd7-122">今年度の予算の総収益</span><span class="sxs-lookup"><span data-stu-id="39dd7-122">Budget total revenue this year</span></span></li><ul> |
| <span data-ttu-id="39dd7-123">支出</span><span class="sxs-lookup"><span data-stu-id="39dd7-123">Expense</span></span>                     | <ul><li><span data-ttu-id="39dd7-124">今年度の経費合計</span><span class="sxs-lookup"><span data-stu-id="39dd7-124">Total expenses this year</span></span></li><li><span data-ttu-id="39dd7-125">予算に基づく経費目標</span><span class="sxs-lookup"><span data-stu-id="39dd7-125">Goal for expenses based on budget</span></span> </li><ul> |
| <span data-ttu-id="39dd7-126">収益</span><span class="sxs-lookup"><span data-stu-id="39dd7-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="39dd7-127">今年度の総収益</span><span class="sxs-lookup"><span data-stu-id="39dd7-127">Total revenue this year</span></span></li><li><span data-ttu-id="39dd7-128">予算に基づく収益目標</span><span class="sxs-lookup"><span data-stu-id="39dd7-128">Goal for revenue based on budget</span></span> </li><ul> |
| <span data-ttu-id="39dd7-129">純利益</span><span class="sxs-lookup"><span data-stu-id="39dd7-129">Net income</span></span>                  | <ul><li><span data-ttu-id="39dd7-130">今年度の純利益</span><span class="sxs-lookup"><span data-stu-id="39dd7-130">Net income this year</span></span></li><li><span data-ttu-id="39dd7-131">予算に基づく目標純利益</span><span class="sxs-lookup"><span data-stu-id="39dd7-131">Goal for net income based on budget</span></span> </li><ul> |

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="39dd7-132">Power BI コンテンツの拡張</span><span class="sxs-lookup"><span data-stu-id="39dd7-132">Extending the Power BI content</span></span>
<span data-ttu-id="39dd7-133">Microsoft Dynamics Lifecycle Services (LCS) で利用できるコンテンツ パックを使用すると、Microsoft Dynamics 365 にログインしない人々に関する優れた分析ができます。</span><span class="sxs-lookup"><span data-stu-id="39dd7-133">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="39dd7-134">ほかのレポートまたはビジュアルを含めるよう、これらのコンテンツ パックを変更できます。次いで分析のためにコンテンツ パックを Power BI.com テナントに発行します。</span><span class="sxs-lookup"><span data-stu-id="39dd7-134">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="39dd7-135">LCS の共有資産ライブラリに [**実績対予算**] Power BI コンテンツがあります。</span><span class="sxs-lookup"><span data-stu-id="39dd7-135">You can find the **Actual vs budget** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="39dd7-136">コンテンツのダウンロード方法および組織で実装する方法の詳細については、「[Microsoft およびパートナーからの LCS での Power BI コンテンツ](power-bi-content-microsoft-partners.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39dd7-136">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="39dd7-137">Power BI コンテンツの実装方法を示すデモを視聴するには、「[Microsoft の Power BI コンテンツおよび Dynamics Lifecycle Services のパートナー](https://mix.office.com/watch/9puyb1b2xs1w)」の Office Mix を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39dd7-137">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

# <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="39dd7-138">データ モデルおよびエンティティの理解</span><span class="sxs-lookup"><span data-stu-id="39dd7-138">Understanding the data model and entities</span></span>

| <span data-ttu-id="39dd7-139">エンティティ</span><span class="sxs-lookup"><span data-stu-id="39dd7-139">Entity</span></span>                    | <span data-ttu-id="39dd7-140">コンテンツ</span><span class="sxs-lookup"><span data-stu-id="39dd7-140">Contents</span></span> |
|---------------------------|----------|
| <span data-ttu-id="39dd7-141">総勘定元帳アクティビティ</span><span class="sxs-lookup"><span data-stu-id="39dd7-141">General Ledger Activities</span></span> | <span data-ttu-id="39dd7-142">総勘定元帳のトランザクション金額</span><span class="sxs-lookup"><span data-stu-id="39dd7-142">Transaction amounts for the general ledger</span></span> |
| <span data-ttu-id="39dd7-143">予算アクティビティ</span><span class="sxs-lookup"><span data-stu-id="39dd7-143">Budget Activities</span></span>         | <span data-ttu-id="39dd7-144">予算登録のトランザクション金額</span><span class="sxs-lookup"><span data-stu-id="39dd7-144">Transaction amounts for the budget register</span></span> |
| <span data-ttu-id="39dd7-145">主勘定</span><span class="sxs-lookup"><span data-stu-id="39dd7-145">Main Accounts</span></span>             | <span data-ttu-id="39dd7-146">レポートをフィルター処理する主勘定</span><span class="sxs-lookup"><span data-stu-id="39dd7-146">Main accounts to filter reports by</span></span> |
| <span data-ttu-id="39dd7-147">会計カレンダー</span><span class="sxs-lookup"><span data-stu-id="39dd7-147">Fiscal Calendars</span></span>          | <span data-ttu-id="39dd7-148">レポートをフィルター処理する会計カレンダー</span><span class="sxs-lookup"><span data-stu-id="39dd7-148">Fiscal calendars to filter reports by</span></span> |
| <span data-ttu-id="39dd7-149">元帳</span><span class="sxs-lookup"><span data-stu-id="39dd7-149">Ledgers</span></span>                   | <span data-ttu-id="39dd7-150">現在の元帳へのレポートをフィルター処理するために使用される元帳</span><span class="sxs-lookup"><span data-stu-id="39dd7-150">Ledgers that can be used to filter the report to the current ledger</span></span> |
| <span data-ttu-id="39dd7-151">予算コード</span><span class="sxs-lookup"><span data-stu-id="39dd7-151">Budget Codes</span></span>              | <span data-ttu-id="39dd7-152">レポートをフィルター処理する予算コード</span><span class="sxs-lookup"><span data-stu-id="39dd7-152">Budget codes to filter reports by</span></span> |
| <span data-ttu-id="39dd7-153">法人</span><span class="sxs-lookup"><span data-stu-id="39dd7-153">Legal Entities</span></span>            | <span data-ttu-id="39dd7-154">現在の法人へのレポートをフィルター処理するために使用される法人</span><span class="sxs-lookup"><span data-stu-id="39dd7-154">Legal entities that can be used to filter the report to the current legal entity</span></span> |

