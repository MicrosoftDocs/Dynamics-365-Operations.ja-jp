---
title: "与信および回収管理 Power BI コンテンツ"
description: "このトピックでは、与信および回収管理 Power BI コンテンツの内容について説明します。 Power BI レポートにアクセスする方法を説明し、コンテンツを作成するために使用するデータ モデルおよびエンティティについての情報を提供します。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations. Core
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5f08df6cb8549e87e123b10c5a771ae1c60ff39c
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="credit-and-collections-management-power-bi-content"></a><span data-ttu-id="2ebba-104">与信および回収管理 Power BI コンテンツ</span><span class="sxs-lookup"><span data-stu-id="2ebba-104">Credit and collections management Power BI content</span></span>

<span data-ttu-id="2ebba-105">このトピックでは、**与信および回収管理** Microsoft Power BI コンテンツの内容について説明します。</span><span class="sxs-lookup"><span data-stu-id="2ebba-105">This topic describes what is included in the **Credit and collections management** Microsoft Power BI content.</span></span> <span data-ttu-id="2ebba-106">Power BI レポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="2ebba-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="2ebba-107">概要</span><span class="sxs-lookup"><span data-stu-id="2ebba-107">Overview</span></span>

<span data-ttu-id="2ebba-108">**与信および回収管理** Power BI コンテンツは、与信および回収マネージャー、そして回収係のために作成されています。</span><span class="sxs-lookup"><span data-stu-id="2ebba-108">The **Credit and collections management** Power BI content was created for credit and collections managers, and collections clerks.</span></span> <span data-ttu-id="2ebba-109">売掛債権回転日数、延滞残高、クレジット エクスポージャ、与信限度額を超えた顧客など、主要な与信および回収のメトリックスを提供します。</span><span class="sxs-lookup"><span data-stu-id="2ebba-109">It provides key credit and collections metrics, such as days sales outstanding, balance overdue, credit exposure, and customers that are over their credit limit.</span></span> <span data-ttu-id="2ebba-110">トランザクション データを使用し、すべての会社の与信および回収の集計ビューを提供します。</span><span class="sxs-lookup"><span data-stu-id="2ebba-110">It uses transactional data, and provides aggregate views of credit and collections across all companies.</span></span> <span data-ttu-id="2ebba-111">会社、顧客グループ、および顧客ごとの内訳も提供します。</span><span class="sxs-lookup"><span data-stu-id="2ebba-111">It also provides a breakdown per company, customer group, and customer.</span></span>

<span data-ttu-id="2ebba-112">この Power BI コンテンツは、10 のレポート ページで構成されます。</span><span class="sxs-lookup"><span data-stu-id="2ebba-112">This Power BI content consists of 10 report pages:</span></span>

- <span data-ttu-id="2ebba-113">2 つの概要ページ (与信の概要に 1 ページと回収の概要に 1 ページ)</span><span class="sxs-lookup"><span data-stu-id="2ebba-113">Two overview pages (one page for a credit overview and one page for a collections overview)</span></span>
- <span data-ttu-id="2ebba-114">さまざまな分析コードで解析された与信および回収のメトリックスの詳細を提供する 8 つの詳細ページ</span><span class="sxs-lookup"><span data-stu-id="2ebba-114">Eight details pages that provide details of credit and collections metrics that are sliced and diced across various dimensions</span></span>

<span data-ttu-id="2ebba-115">すべての金額はシステム通貨で表示されます。</span><span class="sxs-lookup"><span data-stu-id="2ebba-115">All the amounts are shown in the system currency.</span></span> <span data-ttu-id="2ebba-116">システム通貨は、[**システム パラメーター**] ページで設定できます。</span><span class="sxs-lookup"><span data-stu-id="2ebba-116">You can set the system currency on the **Systems parameters** page.</span></span>

<span data-ttu-id="2ebba-117">既定では、現在の会社の与信および回収のデータが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2ebba-117">By default, the credit and collections data for the current company is shown.</span></span> <span data-ttu-id="2ebba-118">すべての会社のデータを表示するには、**CustCollectionsBICrossCompany** 職務権限をロールに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="2ebba-118">To see the data across all companies, assign the **CustCollectionsBICrossCompany** duty to the role.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="2ebba-119">Power BI コンテンツへのアクセス</span><span class="sxs-lookup"><span data-stu-id="2ebba-119">Accessing the Power BI content</span></span>
<span data-ttu-id="2ebba-120">Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition (2017 年 7 月) を使用している場合、**与信および回収管理** Power BI コンテンツは**顧客の与信および回収**ワークスペースで表示されます。</span><span class="sxs-lookup"><span data-stu-id="2ebba-120">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), the **Credit and collections management** Power BI content is shown in the **Customer credit and collections** workspace.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="2ebba-121">Power BI コンテンツに含まれるレポート</span><span class="sxs-lookup"><span data-stu-id="2ebba-121">Reports that are included in the Power BI content</span></span>

<span data-ttu-id="2ebba-122">**CustCollectionsBICrossCompany** Power BI コンテンツには、一連のメトリックスで構成されるレポートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2ebba-122">The **CustCollectionsBICrossCompany** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="2ebba-123">これらのメトリックスはグラフ、タイル、表として視覚化されます。</span><span class="sxs-lookup"><span data-stu-id="2ebba-123">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="2ebba-124">次の表に、**CustCollectionsBICrossCompany** Power BI コンテンツの表示の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="2ebba-124">The following table provides an overview of the visualizations in the **CustCollectionsBICrossCompany** Power BI content.</span></span>

| <span data-ttu-id="2ebba-125">レポート ページ</span><span class="sxs-lookup"><span data-stu-id="2ebba-125">Report page</span></span>                 | <span data-ttu-id="2ebba-126">視覚化</span><span class="sxs-lookup"><span data-stu-id="2ebba-126">Visualization</span></span> |
|-----------------------------|---------------|
| <span data-ttu-id="2ebba-127">回収の概要</span><span class="sxs-lookup"><span data-stu-id="2ebba-127">Collections overview</span></span>        | <ul><li><span data-ttu-id="2ebba-128">期日が経過した顧客</span><span class="sxs-lookup"><span data-stu-id="2ebba-128">Customers past due</span></span></li><li><span data-ttu-id="2ebba-129">与信限度額を超えた顧客</span><span class="sxs-lookup"><span data-stu-id="2ebba-129">Customers over credit limit</span></span></li><li><span data-ttu-id="2ebba-130">DSO 30 日間</span><span class="sxs-lookup"><span data-stu-id="2ebba-130">DSO 30 days</span></span></li><li><span data-ttu-id="2ebba-131">オープンなケース</span><span class="sxs-lookup"><span data-stu-id="2ebba-131">Open cases</span></span></li><li><span data-ttu-id="2ebba-132">ケースがクローズするまでの平均日数</span><span class="sxs-lookup"><span data-stu-id="2ebba-132">Average days to close case</span></span></li><li><span data-ttu-id="2ebba-133">オープンな活動</span><span class="sxs-lookup"><span data-stu-id="2ebba-133">Open activities</span></span></li><li><span data-ttu-id="2ebba-134">活動をクローズするまでの平均日数</span><span class="sxs-lookup"><span data-stu-id="2ebba-134">Average days to close activities</span></span></li><li><span data-ttu-id="2ebba-135">利子計算書を開く</span><span class="sxs-lookup"><span data-stu-id="2ebba-135">Open interest notes</span></span></li><li><span data-ttu-id="2ebba-136">督促状を開く</span><span class="sxs-lookup"><span data-stu-id="2ebba-136">Open collections letters</span></span></li><li><span data-ttu-id="2ebba-137">顧客保留</span><span class="sxs-lookup"><span data-stu-id="2ebba-137">Customer hold</span></span></li><li><span data-ttu-id="2ebba-138">販売保留</span><span class="sxs-lookup"><span data-stu-id="2ebba-138">Sales hold</span></span></li><li><span data-ttu-id="2ebba-139">指定の期間に達している残高</span><span class="sxs-lookup"><span data-stu-id="2ebba-139">Aged balances</span></span></li><li><span data-ttu-id="2ebba-140">回収状態の金額</span><span class="sxs-lookup"><span data-stu-id="2ebba-140">Collections status amounts</span></span></li><li><span data-ttu-id="2ebba-141">回収コードの金額</span><span class="sxs-lookup"><span data-stu-id="2ebba-141">Collections code amounts</span></span></li><li><span data-ttu-id="2ebba-142">理由ごとの損金処理</span><span class="sxs-lookup"><span data-stu-id="2ebba-142">Write-off by reason</span></span></li><li><span data-ttu-id="2ebba-143">地域ごとの未払い残高</span><span class="sxs-lookup"><span data-stu-id="2ebba-143">Balance due by region</span></span></li><li><span data-ttu-id="2ebba-144">支払予定</span><span class="sxs-lookup"><span data-stu-id="2ebba-144">Expected payments</span></span></li></ul> |
| <span data-ttu-id="2ebba-145">与信の概要</span><span class="sxs-lookup"><span data-stu-id="2ebba-145">Credit overview</span></span>             | <ul><li><span data-ttu-id="2ebba-146">期日が経過した顧客</span><span class="sxs-lookup"><span data-stu-id="2ebba-146">Customers past due</span></span></li><li><span data-ttu-id="2ebba-147">与信限度額と未払い残高</span><span class="sxs-lookup"><span data-stu-id="2ebba-147">Credit limit Vs balance due</span></span></li><li><span data-ttu-id="2ebba-148">与信限度額グリッドを超えた顧客</span><span class="sxs-lookup"><span data-stu-id="2ebba-148">Customers over credit limit grid</span></span></li><li><span data-ttu-id="2ebba-149">会社ごとの与信限度額を超えた顧客</span><span class="sxs-lookup"><span data-stu-id="2ebba-149">Customers over credit limit per company</span></span></li><li><span data-ttu-id="2ebba-150">使用されたクレジットと与信限度額合計</span><span class="sxs-lookup"><span data-stu-id="2ebba-150">Credit used Vs total credit limit</span></span></li><li><span data-ttu-id="2ebba-151">与信限度額と地域ごとの使用されたクレジット</span><span class="sxs-lookup"><span data-stu-id="2ebba-151">Credit limit Vs Credit used by region</span></span></li><li><span data-ttu-id="2ebba-152">信用格付けごとの顧客</span><span class="sxs-lookup"><span data-stu-id="2ebba-152">Customers per credit rating</span></span></li></ul> |
| <span data-ttu-id="2ebba-153">与信限度額</span><span class="sxs-lookup"><span data-stu-id="2ebba-153">Credit limit</span></span>                | <ul><li><span data-ttu-id="2ebba-154">与信限度額</span><span class="sxs-lookup"><span data-stu-id="2ebba-154">Credit limit</span></span></li><li><span data-ttu-id="2ebba-155">与信限度額詳細</span><span class="sxs-lookup"><span data-stu-id="2ebba-155">Credit limit details</span></span></li><li><span data-ttu-id="2ebba-156">顧客ごとの与信限度額</span><span class="sxs-lookup"><span data-stu-id="2ebba-156">Credit limit per customer</span></span></li><li><span data-ttu-id="2ebba-157">顧客グループごとの与信限度額</span><span class="sxs-lookup"><span data-stu-id="2ebba-157">Credit limit per customer group</span></span></li><li><span data-ttu-id="2ebba-158">会社ごと、信用格付けごとの与信限度額</span><span class="sxs-lookup"><span data-stu-id="2ebba-158">Credit limit per credit rating per company</span></span></li><li><span data-ttu-id="2ebba-159">与信限度額と地域で使用されたクレジット</span><span class="sxs-lookup"><span data-stu-id="2ebba-159">Credit limit vs credit used by region</span></span></li></ul> |
| <span data-ttu-id="2ebba-160">与信限度額を超えた顧客</span><span class="sxs-lookup"><span data-stu-id="2ebba-160">Customers over credit limit</span></span> | <ul><li><span data-ttu-id="2ebba-161">与信限度額を超えた顧客</span><span class="sxs-lookup"><span data-stu-id="2ebba-161">Customers over credit limit</span></span></li><li><span data-ttu-id="2ebba-162">与信限度額を超えた顧客の詳細</span><span class="sxs-lookup"><span data-stu-id="2ebba-162">Customers over credit limit detail</span></span></li><li><span data-ttu-id="2ebba-163">会社ごとの与信限度額を超えた顧客</span><span class="sxs-lookup"><span data-stu-id="2ebba-163">Customers over credit limit per company</span></span></li><li><span data-ttu-id="2ebba-164">顧客グループごとの与信限度額を超えた顧客</span><span class="sxs-lookup"><span data-stu-id="2ebba-164">Customer over credit limit per customer group</span></span></li><li><span data-ttu-id="2ebba-165">地域ごとの与信限度額を超えた顧客</span><span class="sxs-lookup"><span data-stu-id="2ebba-165">Customers over credit limit by region</span></span></li></ul> |
| <span data-ttu-id="2ebba-166">期日が経過した顧客</span><span class="sxs-lookup"><span data-stu-id="2ebba-166">Customers past due</span></span>          | <ul><li><span data-ttu-id="2ebba-167">期日が経過した顧客</span><span class="sxs-lookup"><span data-stu-id="2ebba-167">Customers past due</span></span></li><li><span data-ttu-id="2ebba-168">期日が経過した顧客の詳細</span><span class="sxs-lookup"><span data-stu-id="2ebba-168">Customer past due details</span></span></li><li><span data-ttu-id="2ebba-169">会社ごとの期日が経過した顧客</span><span class="sxs-lookup"><span data-stu-id="2ebba-169">Customer past due per company</span></span></li><li><span data-ttu-id="2ebba-170">顧客グループごとの期日が経過した顧客</span><span class="sxs-lookup"><span data-stu-id="2ebba-170">Customer past due per customer group</span></span></li><li><span data-ttu-id="2ebba-171">地域ごとの期日が経過した顧客</span><span class="sxs-lookup"><span data-stu-id="2ebba-171">Customer past due by region</span></span></li></ul> |
| <span data-ttu-id="2ebba-172">指定の期間に達している残高</span><span class="sxs-lookup"><span data-stu-id="2ebba-172">Aged balances</span></span>               | <ul><li><span data-ttu-id="2ebba-173">指定の期間に達している残高</span><span class="sxs-lookup"><span data-stu-id="2ebba-173">Aged balances</span></span></li><li><span data-ttu-id="2ebba-174">指定の期間に達している残高の詳細</span><span class="sxs-lookup"><span data-stu-id="2ebba-174">Aged balances details</span></span></li><li><span data-ttu-id="2ebba-175">会社ごとの指定の期間に達している残高</span><span class="sxs-lookup"><span data-stu-id="2ebba-175">Aged balances per company</span></span></li><li><span data-ttu-id="2ebba-176">顧客グループごとの指定の期間に達している残高</span><span class="sxs-lookup"><span data-stu-id="2ebba-176">Aged balances per customer group</span></span></li></ul> |
| <span data-ttu-id="2ebba-177">支払予定</span><span class="sxs-lookup"><span data-stu-id="2ebba-177">Expected payments</span></span>           | <ul><li><span data-ttu-id="2ebba-178">支払予定</span><span class="sxs-lookup"><span data-stu-id="2ebba-178">Expected payments</span></span></li><li><span data-ttu-id="2ebba-179">支払予定の詳細</span><span class="sxs-lookup"><span data-stu-id="2ebba-179">Expected payments details</span></span></li><li><span data-ttu-id="2ebba-180">会社ごとの予期される支払い</span><span class="sxs-lookup"><span data-stu-id="2ebba-180">Expected payments per company</span></span></li><li><span data-ttu-id="2ebba-181">顧客グループごとの予期される支払い</span><span class="sxs-lookup"><span data-stu-id="2ebba-181">Expected payments per customer group</span></span></li><li><span data-ttu-id="2ebba-182">地域ごとの予期される支払い</span><span class="sxs-lookup"><span data-stu-id="2ebba-182">Expected payments by region</span></span></li></ul> |
| <span data-ttu-id="2ebba-183">損金処理</span><span class="sxs-lookup"><span data-stu-id="2ebba-183">Write-offs</span></span>                  | <ul><li><span data-ttu-id="2ebba-184">地域による損金処理</span><span class="sxs-lookup"><span data-stu-id="2ebba-184">Write-offs by region</span></span></li><li><span data-ttu-id="2ebba-185">損金処理の詳細</span><span class="sxs-lookup"><span data-stu-id="2ebba-185">Write-offs details</span></span></li><li><span data-ttu-id="2ebba-186">主勘定による損金処理</span><span class="sxs-lookup"><span data-stu-id="2ebba-186">Write-offs by main account</span></span></li><li><span data-ttu-id="2ebba-187">会社ごとの損金処理</span><span class="sxs-lookup"><span data-stu-id="2ebba-187">Write-offs per company</span></span></li><li><span data-ttu-id="2ebba-188">顧客グループごとの損金処理</span><span class="sxs-lookup"><span data-stu-id="2ebba-188">Write-offs per customer group</span></span></li><li><span data-ttu-id="2ebba-189">地域による損金処理</span><span class="sxs-lookup"><span data-stu-id="2ebba-189">Write-offs by region</span></span></li></ul> |
| <span data-ttu-id="2ebba-190">回収状態</span><span class="sxs-lookup"><span data-stu-id="2ebba-190">Collections status</span></span>          | <ul><li><span data-ttu-id="2ebba-191">争議中</span><span class="sxs-lookup"><span data-stu-id="2ebba-191">Disputed</span></span></li><li><span data-ttu-id="2ebba-192">支払の約束が破棄されました</span><span class="sxs-lookup"><span data-stu-id="2ebba-192">Promise to pay broken</span></span></li><li><span data-ttu-id="2ebba-193">支払約束</span><span class="sxs-lookup"><span data-stu-id="2ebba-193">Promise to pay</span></span></li><li><span data-ttu-id="2ebba-194">回収状態の詳細</span><span class="sxs-lookup"><span data-stu-id="2ebba-194">Collections status details</span></span></li><li><span data-ttu-id="2ebba-195">回収状態の金額</span><span class="sxs-lookup"><span data-stu-id="2ebba-195">Collections status amounts</span></span></li><li><span data-ttu-id="2ebba-196">オープンなケース</span><span class="sxs-lookup"><span data-stu-id="2ebba-196">Open cases</span></span></li><li><span data-ttu-id="2ebba-197">オープンな活動</span><span class="sxs-lookup"><span data-stu-id="2ebba-197">Open activities</span></span></li></ul> |
| <span data-ttu-id="2ebba-198">督促状</span><span class="sxs-lookup"><span data-stu-id="2ebba-198">Collections letters</span></span>         | <ul><li><span data-ttu-id="2ebba-199">督促状コードの金額</span><span class="sxs-lookup"><span data-stu-id="2ebba-199">Collection code amounts</span></span></li><li><span data-ttu-id="2ebba-200">回収コードの量の詳細</span><span class="sxs-lookup"><span data-stu-id="2ebba-200">Collection code amount details</span></span></li><li><span data-ttu-id="2ebba-201">会社別の督促状の量</span><span class="sxs-lookup"><span data-stu-id="2ebba-201">Collection letter amount per company</span></span></li><li><span data-ttu-id="2ebba-202">顧客グループ別の督促状の量</span><span class="sxs-lookup"><span data-stu-id="2ebba-202">Collection letter amount per customer group</span></span></li><li><span data-ttu-id="2ebba-203">地域ごとの督促状の量</span><span class="sxs-lookup"><span data-stu-id="2ebba-203">Collection letter amount by region</span></span></li></ul> |

<span data-ttu-id="2ebba-204">これらすべてのレポートのグラフとタイルはフィルター処理し、ダッシュボードに固定することができます。</span><span class="sxs-lookup"><span data-stu-id="2ebba-204">The charts and tiles on all these reports can be filtered and pinned to the dashboard.</span></span> <span data-ttu-id="2ebba-205">Power BI のフィルター処理と固定方法の詳細については、[ダッシュボードの作成およびコンフィギュレーション](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ebba-205">For more information about how to filter and pin in Power BI, see [Create and Configure a Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/).</span></span> <span data-ttu-id="2ebba-206">また、基になるデータのエクスポート機能を使用して、視覚化で要約されている基になるデータをエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="2ebba-206">You can also use the export underlying data functionality to export underlying data that is summarized on a visualization.</span></span>

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="2ebba-207">Power BI コンテンツの拡張</span><span class="sxs-lookup"><span data-stu-id="2ebba-207">Extending the Power BI content</span></span>
<span data-ttu-id="2ebba-208">Microsoft Dynamics Lifecycle Services (LCS) で利用できるコンテンツ パックを使用すると、Finance and Operations にログインしない人々に関する優れた分析ができます。</span><span class="sxs-lookup"><span data-stu-id="2ebba-208">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Finance and Operations.</span></span> <span data-ttu-id="2ebba-209">ほかのレポートまたはビジュアルを含めるよう、これらのコンテンツ パックを変更できます。次いで分析のためにコンテンツ パックを Power BI.com テナントに発行します。</span><span class="sxs-lookup"><span data-stu-id="2ebba-209">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span>

<span data-ttu-id="2ebba-210">LCS の共有資産ライブラリに **与信および回収管理** Power BI コンテンツがあります。</span><span class="sxs-lookup"><span data-stu-id="2ebba-210">You can find the **Credit and collections management** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="2ebba-211">コンテンツのダウンロード方法および組織で実装する方法の詳細については、「[Microsoft およびパートナーからの LCS での Power BI コンテンツ](../../dev-itpro/analytics/power-bi-content-microsoft-partners.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ebba-211">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](../../dev-itpro/analytics/power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="2ebba-212">Power BI コンテンツの実装方法を示すデモを視聴するには、「[Microsoft の Power BI コンテンツおよび Dynamics Lifecycle Services のパートナー](https://mix.office.com/watch/9puyb1b2xs1w)」の Office Mix を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ebba-212">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

<span data-ttu-id="2ebba-213">ご使用のバージョンの Finance and Operations に適用する **与信および回収管理** Power BI コンテンツをダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="2ebba-213">Be sure to download the **Credit and collections management** Power BI content that applies to the version of Finance and Operations that you're using.</span></span>

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="2ebba-214">データ モデルおよびエンティティの理解</span><span class="sxs-lookup"><span data-stu-id="2ebba-214">Understanding the data model and entities</span></span>

<span data-ttu-id="2ebba-215">次のデータは、**与信および回収管理** Power BI コンテンツのレポートに入力するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2ebba-215">The following data is used to fill the report in the **Credit and collections management** Power BI content.</span></span> <span data-ttu-id="2ebba-216">このデータは、エンティティ ストアで実施される集計の測定として表されます。</span><span class="sxs-lookup"><span data-stu-id="2ebba-216">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="2ebba-217">エンティティ ストアは、分析に最適化された Microsoft SQL Server データベースです。</span><span class="sxs-lookup"><span data-stu-id="2ebba-217">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="2ebba-218">詳細については、「[エンティティ ストアとの Power BI の統合](../../dev-itpro/analytics/power-bi-integration-entity-store.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ebba-218">For more information, see [Overview of Power BI integration with Entity store](../../dev-itpro/analytics/power-bi-integration-entity-store.md).</span></span>

| <span data-ttu-id="2ebba-219">エンティティ</span><span class="sxs-lookup"><span data-stu-id="2ebba-219">Entity</span></span>                                      | <span data-ttu-id="2ebba-220">キー集計の測定</span><span class="sxs-lookup"><span data-stu-id="2ebba-220">Key aggregate measurements</span></span>           | <span data-ttu-id="2ebba-221">データ ソース</span><span class="sxs-lookup"><span data-stu-id="2ebba-221">Data source</span></span>                                 | <span data-ttu-id="2ebba-222">フィールド</span><span class="sxs-lookup"><span data-stu-id="2ebba-222">Field</span></span>                                                      | <span data-ttu-id="2ebba-223">説明</span><span class="sxs-lookup"><span data-stu-id="2ebba-223">Description</span></span> |
|---------------------------------------------|--------------------------------------|---------------------------------------------|------------------------------------------------------------|-------------|
| <span data-ttu-id="2ebba-224">CustCollectionsBIActivitiesAverageCloseTime</span><span class="sxs-lookup"><span data-stu-id="2ebba-224">CustCollectionsBIActivitiesAverageCloseTime</span></span> | <span data-ttu-id="2ebba-225">NumOfActivities, AveragecClosedTime</span><span class="sxs-lookup"><span data-stu-id="2ebba-225">NumOfActivities, AveragecClosedTime</span></span>  | <span data-ttu-id="2ebba-226">smmActivities</span><span class="sxs-lookup"><span data-stu-id="2ebba-226">smmActivities</span></span>                               | <span data-ttu-id="2ebba-227">AverageOfChildren(AverageClosedTime) Count(ActivityNumber)</span><span class="sxs-lookup"><span data-stu-id="2ebba-227">AverageOfChildren(AverageClosedTime) Count(ActivityNumber)</span></span> | <span data-ttu-id="2ebba-228">終了した活動の数およびそれらの活動を終了する平均時間。</span><span class="sxs-lookup"><span data-stu-id="2ebba-228">The count of closed activities and average time to close those activities.</span></span> |
| <span data-ttu-id="2ebba-229">CustCollectionsBIActivitiesOpen</span><span class="sxs-lookup"><span data-stu-id="2ebba-229">CustCollectionsBIActivitiesOpen</span></span>             | <span data-ttu-id="2ebba-230">ActivityNumber</span><span class="sxs-lookup"><span data-stu-id="2ebba-230">ActivityNumber</span></span>                       | <span data-ttu-id="2ebba-231">smmActivities</span><span class="sxs-lookup"><span data-stu-id="2ebba-231">smmActivities</span></span>                               | <span data-ttu-id="2ebba-232">Count(ActivityNumber)</span><span class="sxs-lookup"><span data-stu-id="2ebba-232">Count(ActivityNumber)</span></span>                                      | <span data-ttu-id="2ebba-233">オープンな活動の数。</span><span class="sxs-lookup"><span data-stu-id="2ebba-233">The count of open activities.</span></span> |
| <span data-ttu-id="2ebba-234">CustCollectionsBIAgedBalances</span><span class="sxs-lookup"><span data-stu-id="2ebba-234">CustCollectionsBIAgedBalances</span></span>               | <span data-ttu-id="2ebba-235">AgedBalances</span><span class="sxs-lookup"><span data-stu-id="2ebba-235">AgedBalances</span></span>                         | <span data-ttu-id="2ebba-236">CustCollectionsBIAgedBalancesView</span><span class="sxs-lookup"><span data-stu-id="2ebba-236">CustCollectionsBIAgedBalancesView</span></span>           | <span data-ttu-id="2ebba-237">Sum(SystemCurrencyBalance)</span><span class="sxs-lookup"><span data-stu-id="2ebba-237">Sum(SystemCurrencyBalance)</span></span>                                 | <span data-ttu-id="2ebba-238">指定の期間に達している残高の合計。</span><span class="sxs-lookup"><span data-stu-id="2ebba-238">The sum of aged balances.</span></span> |
| <span data-ttu-id="2ebba-239">CustCollectionsBIBalancesDue</span><span class="sxs-lookup"><span data-stu-id="2ebba-239">CustCollectionsBIBalancesDue</span></span>                | <span data-ttu-id="2ebba-240">SystemCurrencyAmount</span><span class="sxs-lookup"><span data-stu-id="2ebba-240">SystemCurrencyAmount</span></span>                 | <span data-ttu-id="2ebba-241">CustCollectionsBIBalanceDueView</span><span class="sxs-lookup"><span data-stu-id="2ebba-241">CustCollectionsBIBalanceDueView</span></span>             | <span data-ttu-id="2ebba-242">Sum(SystemCurrencyAmount)</span><span class="sxs-lookup"><span data-stu-id="2ebba-242">Sum(SystemCurrencyAmount)</span></span>                                  | <span data-ttu-id="2ebba-243">期限切れの金額。</span><span class="sxs-lookup"><span data-stu-id="2ebba-243">The amounts that are overdue.</span></span> |
| <span data-ttu-id="2ebba-244">CustCollectionsBICaseAverageCloseTIme</span><span class="sxs-lookup"><span data-stu-id="2ebba-244">CustCollectionsBICaseAverageCloseTIme</span></span>       | <span data-ttu-id="2ebba-245">NumOfCases, CaseAverageClosedTime</span><span class="sxs-lookup"><span data-stu-id="2ebba-245">NumOfCases, CaseAverageClosedTime</span></span>    | <span data-ttu-id="2ebba-246">CustCollectionsCaseDetail</span><span class="sxs-lookup"><span data-stu-id="2ebba-246">CustCollectionsCaseDetail</span></span>                   | <span data-ttu-id="2ebba-247">AverageOfChildren(CaseAverageClosedTime) Count(NumOfCases)</span><span class="sxs-lookup"><span data-stu-id="2ebba-247">AverageOfChildren(CaseAverageClosedTime) Count(NumOfCases)</span></span> | <span data-ttu-id="2ebba-248">終了したケースの数およびそれらのケースを終了する平均時間。</span><span class="sxs-lookup"><span data-stu-id="2ebba-248">The count of closed cases and the average time to close those cases.</span></span> |
| <span data-ttu-id="2ebba-249">CustCollectionsBICasesOpen</span><span class="sxs-lookup"><span data-stu-id="2ebba-249">CustCollectionsBICasesOpen</span></span>                  | <span data-ttu-id="2ebba-250">CaseId</span><span class="sxs-lookup"><span data-stu-id="2ebba-250">CaseId</span></span>                               | <span data-ttu-id="2ebba-251">CustCollectionsCaseDetail</span><span class="sxs-lookup"><span data-stu-id="2ebba-251">CustCollectionsCaseDetail</span></span>                   | <span data-ttu-id="2ebba-252">Count(CaseId)</span><span class="sxs-lookup"><span data-stu-id="2ebba-252">Count(CaseId)</span></span>                                              | <span data-ttu-id="2ebba-253">オープンなケースの数。</span><span class="sxs-lookup"><span data-stu-id="2ebba-253">The count of open cases.</span></span> |
| <span data-ttu-id="2ebba-254">CustCollectionsBICollectionLetter</span><span class="sxs-lookup"><span data-stu-id="2ebba-254">CustCollectionsBICollectionLetter</span></span>           | <span data-ttu-id="2ebba-255">CollectionLetterNum</span><span class="sxs-lookup"><span data-stu-id="2ebba-255">CollectionLetterNum</span></span>                  | <span data-ttu-id="2ebba-256">CustCollectionLetterJour</span><span class="sxs-lookup"><span data-stu-id="2ebba-256">CustCollectionLetterJour</span></span>                    | <span data-ttu-id="2ebba-257">Count(CollectionLetterNum)</span><span class="sxs-lookup"><span data-stu-id="2ebba-257">Count(CollectionLetterNum)</span></span>                                 | <span data-ttu-id="2ebba-258">オープンな督促状の数。</span><span class="sxs-lookup"><span data-stu-id="2ebba-258">The count of open collection letters.</span></span> |
| <span data-ttu-id="2ebba-259">CustCollectionsBICollectionLetterAmount</span><span class="sxs-lookup"><span data-stu-id="2ebba-259">CustCollectionsBICollectionLetterAmount</span></span>     | <span data-ttu-id="2ebba-260">CollectionLetterAmounts</span><span class="sxs-lookup"><span data-stu-id="2ebba-260">CollectionLetterAmounts</span></span>              | <span data-ttu-id="2ebba-261">CustCollectionsBIAccountsReceivables</span><span class="sxs-lookup"><span data-stu-id="2ebba-261">CustCollectionsBIAccountsReceivables</span></span>        | <span data-ttu-id="2ebba-262">Sum(SystemCurrencyAmount)</span><span class="sxs-lookup"><span data-stu-id="2ebba-262">Sum(SystemCurrencyAmount)</span></span>                                  | <span data-ttu-id="2ebba-263">転記済督促状の残高。</span><span class="sxs-lookup"><span data-stu-id="2ebba-263">The balance of posted collection letters.</span></span> |
| <span data-ttu-id="2ebba-264">CustCollectionsBICollectionStatus</span><span class="sxs-lookup"><span data-stu-id="2ebba-264">CustCollectionsBICollectionStatus</span></span>           | <span data-ttu-id="2ebba-265">CollectionStatusAmounts</span><span class="sxs-lookup"><span data-stu-id="2ebba-265">CollectionStatusAmounts</span></span>              | <span data-ttu-id="2ebba-266">CustCollectionsBIAccountsReceivables</span><span class="sxs-lookup"><span data-stu-id="2ebba-266">CustCollectionsBIAccountsReceivables</span></span>        | <span data-ttu-id="2ebba-267">Sum(SystemCurrencyAmount)</span><span class="sxs-lookup"><span data-stu-id="2ebba-267">Sum(SystemCurrencyAmount)</span></span>                                  | <span data-ttu-id="2ebba-268">回収状態のトランザクションの残高。</span><span class="sxs-lookup"><span data-stu-id="2ebba-268">The balance of transactions with collection status.</span></span> |
| <span data-ttu-id="2ebba-269">CustCollectionsBICredit</span><span class="sxs-lookup"><span data-stu-id="2ebba-269">CustCollectionsBICredit</span></span>                     | <span data-ttu-id="2ebba-270">CreditExposed, AmountOverCreditLimit</span><span class="sxs-lookup"><span data-stu-id="2ebba-270">CreditExposed, AmountOverCreditLimit</span></span> | <span data-ttu-id="2ebba-271">CustCollectionsBICreditView</span><span class="sxs-lookup"><span data-stu-id="2ebba-271">CustCollectionsBICreditView</span></span>                 | <span data-ttu-id="2ebba-272">Sum(CreditExposed), Sum(AmountOverCreditLimit)</span><span class="sxs-lookup"><span data-stu-id="2ebba-272">Sum(CreditExposed), Sum(AmountOverCreditLimit)</span></span>             | <span data-ttu-id="2ebba-273">クレジット エクスポージャおよび顧客が与信限度額を超えている金額の合計値。</span><span class="sxs-lookup"><span data-stu-id="2ebba-273">The sum of credit exposure and amounts that customers are over their credit limit.</span></span> |
| <span data-ttu-id="2ebba-274">CustCollectionsBICustOnHold</span><span class="sxs-lookup"><span data-stu-id="2ebba-274">CustCollectionsBICustOnHold</span></span>                 | <span data-ttu-id="2ebba-275">ブロック</span><span class="sxs-lookup"><span data-stu-id="2ebba-275">Blocked</span></span>                              | <span data-ttu-id="2ebba-276">CustCollectionsBICustTable</span><span class="sxs-lookup"><span data-stu-id="2ebba-276">CustCollectionsBICustTable</span></span>                  | <span data-ttu-id="2ebba-277">Count(Blocked)</span><span class="sxs-lookup"><span data-stu-id="2ebba-277">Count(Blocked)</span></span>                                             | <span data-ttu-id="2ebba-278">保留中の顧客の数。</span><span class="sxs-lookup"><span data-stu-id="2ebba-278">The number of customers that are on hold.</span></span> |
| <span data-ttu-id="2ebba-279">CustCollectionsBIDSO</span><span class="sxs-lookup"><span data-stu-id="2ebba-279">CustCollectionsBIDSO</span></span>                        | <span data-ttu-id="2ebba-280">DSO30</span><span class="sxs-lookup"><span data-stu-id="2ebba-280">DSO30</span></span>                                | <span data-ttu-id="2ebba-281">CustCollectionsBIDSOView</span><span class="sxs-lookup"><span data-stu-id="2ebba-281">CustCollectionsBIDSOView</span></span>                    | <span data-ttu-id="2ebba-282">AverageOfChildren(DSO30)</span><span class="sxs-lookup"><span data-stu-id="2ebba-282">AverageOfChildren(DSO30)</span></span>                                   | <span data-ttu-id="2ebba-283">30 日の売掛債権回転日数</span><span class="sxs-lookup"><span data-stu-id="2ebba-283">Days sales outstanding for 30 days.</span></span> |
| <span data-ttu-id="2ebba-284">CustCollectionsBIExpectedPayment</span><span class="sxs-lookup"><span data-stu-id="2ebba-284">CustCollectionsBIExpectedPayment</span></span>            | <span data-ttu-id="2ebba-285">ExpectedPayment</span><span class="sxs-lookup"><span data-stu-id="2ebba-285">ExpectedPayment</span></span>                      | <span data-ttu-id="2ebba-286">CustCollectionsBIExpectedPaymentView</span><span class="sxs-lookup"><span data-stu-id="2ebba-286">CustCollectionsBIExpectedPaymentView</span></span>        | <span data-ttu-id="2ebba-287">Sum(SystemCurrencyAmounts)</span><span class="sxs-lookup"><span data-stu-id="2ebba-287">Sum(SystemCurrencyAmounts)</span></span>                                 | <span data-ttu-id="2ebba-288">翌年度内の予期される支払いの合計。</span><span class="sxs-lookup"><span data-stu-id="2ebba-288">The sum of expected payments within the next year.</span></span> |
| <span data-ttu-id="2ebba-289">CustCollectionsBIInterestNote</span><span class="sxs-lookup"><span data-stu-id="2ebba-289">CustCollectionsBIInterestNote</span></span>               | <span data-ttu-id="2ebba-290">InterestNote</span><span class="sxs-lookup"><span data-stu-id="2ebba-290">InterestNote</span></span>                         | <span data-ttu-id="2ebba-291">CustInterestJour</span><span class="sxs-lookup"><span data-stu-id="2ebba-291">CustInterestJour</span></span>                            | <span data-ttu-id="2ebba-292">Count(InterestNote)</span><span class="sxs-lookup"><span data-stu-id="2ebba-292">Count(InterestNote)</span></span>                                        | <span data-ttu-id="2ebba-293">作成済の利子計算書の数。</span><span class="sxs-lookup"><span data-stu-id="2ebba-293">The number of interest notes that have been created.</span></span> |
| <span data-ttu-id="2ebba-294">CustCollectionsBISalesOnHold</span><span class="sxs-lookup"><span data-stu-id="2ebba-294">CustCollectionsBISalesOnHold</span></span>                | <span data-ttu-id="2ebba-295">SalesId</span><span class="sxs-lookup"><span data-stu-id="2ebba-295">SalesId</span></span>                              | <span data-ttu-id="2ebba-296">SalesTable</span><span class="sxs-lookup"><span data-stu-id="2ebba-296">SalesTable</span></span>                                  | <span data-ttu-id="2ebba-297">Count(SalesId)</span><span class="sxs-lookup"><span data-stu-id="2ebba-297">Count(SalesId)</span></span>                                             | <span data-ttu-id="2ebba-298">保留中の販売注文の合計数。</span><span class="sxs-lookup"><span data-stu-id="2ebba-298">The number of total sales orders that are on hold.</span></span> |
| <span data-ttu-id="2ebba-299">CustCollectionsBIWriteOff</span><span class="sxs-lookup"><span data-stu-id="2ebba-299">CustCollectionsBIWriteOff</span></span>                   | <span data-ttu-id="2ebba-300">WriteOffAmount</span><span class="sxs-lookup"><span data-stu-id="2ebba-300">WriteOffAmount</span></span>                       | <span data-ttu-id="2ebba-301">CustCollectionsBIWriteOffView</span><span class="sxs-lookup"><span data-stu-id="2ebba-301">CustCollectionsBIWriteOffView</span></span>               | <span data-ttu-id="2ebba-302">Sum(SystemCurrencyAmount)</span><span class="sxs-lookup"><span data-stu-id="2ebba-302">Sum(SystemCurrencyAmount)</span></span>                                  | <span data-ttu-id="2ebba-303">損金処理済のトランザクションの合計。</span><span class="sxs-lookup"><span data-stu-id="2ebba-303">The sum of transactions that have been written off.</span></span> |
