---
title: プロセス インサイトの採用に分析レポートを使用する
description: このトピックでは、Attract の分析レポートについて説明します。
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: 33ed6072a9ad99144fb96ad19389a57461324f71
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1516563"
---
# <a name="use-analytic-reports-for-hiring-process-insights"></a><span data-ttu-id="8c010-103">プロセス インサイトの採用に分析レポートを使用する</span><span class="sxs-lookup"><span data-stu-id="8c010-103">Use analytic reports for hiring process insights</span></span>

<span data-ttu-id="8c010-104">Attract の分析レポートは、プロセス インサイトを採用するためにそのまま使用できる (OOTB) ソリューションを提供します。</span><span class="sxs-lookup"><span data-stu-id="8c010-104">Analytic reports in Attract provide an out-of-the-box (OOTB) solution for hiring process insights.</span></span> <span data-ttu-id="8c010-105">利用可能な機能は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="8c010-105">Availabe features include:</span></span>

- <span data-ttu-id="8c010-106">**職務分析 :** 職務申請者に関するメトリックスについては、職務内の**分析**タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8c010-106">**Job analytics:** Click the **Analytics** tab within a job for metrics on the job's applicants.</span></span>
- <span data-ttu-id="8c010-107">**分析ハブ :** 職務間で集計されたメトリックスについては、左側のナビゲーションで**分析**をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="8c010-107">**Analytics hub:** Click **Analytics** on the left navigation for aggregated metrics across jobs.</span></span>
- <span data-ttu-id="8c010-108">**ユーザー固有のセキュリティ :** レポートへのアクセスは Attract [ロール](security-attract.md) および職務参加者ロールによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="8c010-108">**User-specific security:** Access to reports is controlled by Attract [role](security-attract.md) and job participant role.</span></span>
- <span data-ttu-id="8c010-109">**クロス フィルター処理 :** レポート内のビジュアルをクリックして、選択したデータによってフィルター処理された他のメトリックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="8c010-109">**Cross-filtering:** Click visuals within a report to view other metrics filtered by selected data.</span></span>

>[!NOTE] 
>- <span data-ttu-id="8c010-110">この機能は現在[プレビュー](access-preview-feature.md)にあります。</span><span class="sxs-lookup"><span data-stu-id="8c010-110">This feature is currently in [preview](access-preview-feature.md).</span></span> <span data-ttu-id="8c010-111">これを実行するには、[**包括採用アドオン**](attract-comprehensive-hiring.md)が必要です。</span><span class="sxs-lookup"><span data-stu-id="8c010-111">To try it, you must have the [**Comprehensive Hiring Add-On**](attract-comprehensive-hiring.md).</span></span>
>- <span data-ttu-id="8c010-112">すべてのパブリック プレビュー レポートは英語で表示されます。</span><span class="sxs-lookup"><span data-stu-id="8c010-112">All public preview reports are displayed in English.</span></span>
>- <span data-ttu-id="8c010-113">レポートは 3 時間ごとに更新されます。</span><span class="sxs-lookup"><span data-stu-id="8c010-113">Reports refresh every 3 hours.</span></span> <span data-ttu-id="8c010-114">最新の更新時刻 (ローカル タイムゾーン) は、レポートの最上部に表示されます。</span><span class="sxs-lookup"><span data-stu-id="8c010-114">The last refresh time (in the local timezone) is located at the top of the report.</span></span> <span data-ttu-id="8c010-115">更新時刻は概算であり、地域のデータ量とリソースの負荷によって異なります。</span><span class="sxs-lookup"><span data-stu-id="8c010-115">Refresh times are an approximation and vary based on data volume and resource load in your region.</span></span>

## <a name="job-analytics"></a><span data-ttu-id="8c010-116">職務分析</span><span class="sxs-lookup"><span data-stu-id="8c010-116">Job Analytics</span></span>

<span data-ttu-id="8c010-117">職務分析レポートは、職務の採用プロセスのスナップショットです。</span><span class="sxs-lookup"><span data-stu-id="8c010-117">Job Analytics reports are a snapshot of the hiring process for a job.</span></span>  <span data-ttu-id="8c010-118">主なメトリックスは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="8c010-118">Key metrics include:</span></span>

- <span data-ttu-id="8c010-119">ステージごとの有効な申請者</span><span class="sxs-lookup"><span data-stu-id="8c010-119">Active applicants by stage</span></span>
- <span data-ttu-id="8c010-120">申請者ソース</span><span class="sxs-lookup"><span data-stu-id="8c010-120">Applicant source</span></span>
- <span data-ttu-id="8c010-121">申請者のタイプ (内部と外部)</span><span class="sxs-lookup"><span data-stu-id="8c010-121">Applicant type (internal or external)</span></span>

## <a name="analytics-hub"></a><span data-ttu-id="8c010-122">分析ハブ</span><span class="sxs-lookup"><span data-stu-id="8c010-122">Analytics Hub</span></span>

<span data-ttu-id="8c010-123">分析ハブは、採用プロセスにおける傾向を提示するために、職務間で集計されたデータをレポートします。</span><span class="sxs-lookup"><span data-stu-id="8c010-123">Analytics Hub reports aggregate data across jobs to surface trends in the hiring process.</span></span> <span data-ttu-id="8c010-124">Attract には、パイプラインの概要とじょうご分析の 2 つの OOTB レポートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8c010-124">Attract includes two OOTB reports: Pipeline Summary and Funnel Analysis.</span></span>

### <a name="pipeline-summary"></a><span data-ttu-id="8c010-125">パイプラインの概要</span><span class="sxs-lookup"><span data-stu-id="8c010-125">Pipeline Summary</span></span>

<span data-ttu-id="8c010-126">パイプラインの概要レポートは、欠員がある職務のデータを集計します。</span><span class="sxs-lookup"><span data-stu-id="8c010-126">The Pipeline Summary report aggregates data for open jobs.</span></span> <span data-ttu-id="8c010-127">主なメトリックスは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="8c010-127">Key metrics include:</span></span>

- <span data-ttu-id="8c010-128">ステージごとのすべての職務間の申請者</span><span class="sxs-lookup"><span data-stu-id="8c010-128">Applicants across all jobs by stage</span></span>
- <span data-ttu-id="8c010-129">申請者ソース</span><span class="sxs-lookup"><span data-stu-id="8c010-129">Applicant source</span></span>
- <span data-ttu-id="8c010-130">勤続レベル別の欠員のある職務</span><span class="sxs-lookup"><span data-stu-id="8c010-130">Open jobs by seniority level</span></span>

### <a name="funnel-analysis"></a><span data-ttu-id="8c010-131">じょうご分析</span><span class="sxs-lookup"><span data-stu-id="8c010-131">Funnel Analysis</span></span>

<span data-ttu-id="8c010-132">じょうご分析レポートでは、採用済みとして終了した職務のデータが集計されます。</span><span class="sxs-lookup"><span data-stu-id="8c010-132">The Funnel Analysis report aggregates data for jobs that have been closed as filled.</span></span> <span data-ttu-id="8c010-133">主なメトリックスは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="8c010-133">Key metrics include:</span></span>

- <span data-ttu-id="8c010-134">採用する時期</span><span class="sxs-lookup"><span data-stu-id="8c010-134">Time to hire</span></span>
- <span data-ttu-id="8c010-135">変換メトリックス (ポイント時)</span><span class="sxs-lookup"><span data-stu-id="8c010-135">Conversion metrics (on hover)</span></span>
- <span data-ttu-id="8c010-136">受入率の提示</span><span class="sxs-lookup"><span data-stu-id="8c010-136">Offer acceptance rate</span></span>

<span data-ttu-id="8c010-137">注記 : 最も正確な時期にレポートを採用するためには、包括採用アドオンの一部として利用可能な機能である[オファー管理](offer-setup.md)を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8c010-137">Note: For the most accurate time to hire reporting, it is recommended that you use [Offer management](offer-setup.md), a feature available as part of the Comprehensive Hiring Add-On.</span></span>

>[!TIP] 
><span data-ttu-id="8c010-138">ビジュアルの上にポインターを移動して、追加情報を確認してください。</span><span class="sxs-lookup"><span data-stu-id="8c010-138">Try hovering over visuals for additional information.</span></span> <span data-ttu-id="8c010-139">たとえば、**有効な申請者**のビジュアルにポインターを移動すると、ステージの平均日数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8c010-139">For example, hovering over **Active applicants** visuals will display the average days in stage.</span></span> <span data-ttu-id="8c010-140">この情報を分析することにより、採用にかかる時間を短縮し、採用担当者が各ステージで費やす時間を短縮する方法に関する重要な情報を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="8c010-140">Analyzing this information can provide insights critical to reducing time to hire and enable recruiters to focus on ways to reduce the time spent in each stage.</span></span>

## <a name="user-specific-security"></a><span data-ttu-id="8c010-141">ユーザー固有のセキュリティ</span><span class="sxs-lookup"><span data-stu-id="8c010-141">User-specific security</span></span>

<span data-ttu-id="8c010-142">Attract レポートには、管理者、すべて読み取り、採用担当者、および採用マネージャー[各ロール](security-attract.md)がアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="8c010-142">Attract reports are accessible for Admin, Read All, Recruiter, and Hiring Manager [roles](security-attract.md).</span></span> <span data-ttu-id="8c010-143">割り当てられていないユーザーは、どちらの分析レポートのページ (職務分析または分析ハブ) にもアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="8c010-143">Unassigned users do not have access to either of the analytic report pages (Job Analytics or Analytics Hub).</span></span>

<span data-ttu-id="8c010-144">職務分析レポートには、選択した職務のデータが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8c010-144">Job Analytics reports display data for the selected job.</span></span> <span data-ttu-id="8c010-145">分析ハブ レポートでは、ユーザーが表示できるすべての職務のデータを集計します。</span><span class="sxs-lookup"><span data-stu-id="8c010-145">Analytics Hub reports aggregate data across all jobs a user can view.</span></span> <span data-ttu-id="8c010-146">職務ページで自分の職務とすべての職務の両方を表示できるユーザーは、分析ハブでも同じビューを使用できます。</span><span class="sxs-lookup"><span data-stu-id="8c010-146">Users that can view both My jobs and All jobs on the Jobs page have the same views available in the Analytics Hub.</span></span>

## <a name="cross-filter"></a><span data-ttu-id="8c010-147">クロス フィルター</span><span class="sxs-lookup"><span data-stu-id="8c010-147">Cross-filter</span></span>

<span data-ttu-id="8c010-148">Power BI の優れた機能の 1 つは、レポート ページのすべてのビジュアルを連結できることです。</span><span class="sxs-lookup"><span data-stu-id="8c010-148">One of the great features of Power BI is the way all visuals on a report page are interconnected.</span></span> <span data-ttu-id="8c010-149">いずれかのビジュアルでデータ ポイントを選択すると、その選択に基づいて、そのデータを含むページ上の他のすべてのビジュアルが変更されます。</span><span class="sxs-lookup"><span data-stu-id="8c010-149">If you select a data point on one of the visuals, all the other visuals on the page that contain that data change, based on that selection.</span></span> <span data-ttu-id="8c010-150">詳細については、[Power BI レポートでのビジュアルのクロス フィルター](https://docs.microsoft.com/en-us/power-bi/consumer/end-user-interactions)の例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8c010-150">Find out more and see an example in [How visuals cross-filter each other in a Power BI report](https://docs.microsoft.com/en-us/power-bi/consumer/end-user-interactions).</span></span>

## <a name="export-to-excel"></a><span data-ttu-id="8c010-151">Excel にエクスポート</span><span class="sxs-lookup"><span data-stu-id="8c010-151">Export to Excel</span></span>

<span data-ttu-id="8c010-152">レポート データを Excel で表示するには、ビジュアル上のオプション メニュー (3 つのドット) をクリックし、**基になるデータのエクスポート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c010-152">To view report data in Excel, you can click the options menu (three dots) on a visual and select **Export underlying data**.</span></span> <span data-ttu-id="8c010-153">エクスポートされたデータは、Attract ユーザーのアクセス許可に従い、フィルタリングされ、エクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="8c010-153">Exported data will export as filtered, respecting user permissions in Attract.</span></span> <span data-ttu-id="8c010-154">詳細については[視覚エフェクトからのデータのエクスポート](https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-export-data)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8c010-154">For more information, see [Export data from visualizations](https://docs.microsoft.com/en-us/power-bi/visuals/power-bi-visualization-export-data).</span></span>
