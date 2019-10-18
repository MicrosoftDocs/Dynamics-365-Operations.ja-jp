---
title: Recruiting Power BI コンテンツ
description: このトピックでは、Recruiting Power BI コンテンツについて説明します。 レポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: HcmRecruitmentWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b92078ca2bc89d752895bf3b4f2f3cdb2c2fd2f6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185224"
---
# <a name="recruiting-power-bi-content"></a><span data-ttu-id="d2332-104">Recruiting Power BI コンテンツ</span><span class="sxs-lookup"><span data-stu-id="d2332-104">Recruiting Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2332-105">このトピックでは、**Recruiting** Microsoft Power BI コンテンツについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d2332-105">This topic describes the **Recruiting** Microsoft Power BI content.</span></span> <span data-ttu-id="d2332-106">Power BI レポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="d2332-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="d2332-107">Power BI コンテンツへのアクセス</span><span class="sxs-lookup"><span data-stu-id="d2332-107">Accessing the Power BI content</span></span>
<span data-ttu-id="d2332-108">**Recruiting** Power BI コンテンツが**採用管理**ワークスペースで表示されます。</span><span class="sxs-lookup"><span data-stu-id="d2332-108">The **Recruiting** Power BI content is shown in the **Recruitment management** workspace.</span></span>

## <a name="reports-and-visuals-in-the-recruitment-management-workspace"></a><span data-ttu-id="d2332-109">採用管理ワークスペースでのレポートおよびビジュアル</span><span class="sxs-lookup"><span data-stu-id="d2332-109">Reports and visuals in the Recruitment management workspace</span></span>
<span data-ttu-id="d2332-110">**採用管理**ワークスペースは、**分析**タブを含みます。このタブには、採用のための埋め込み Power BI コンテンツが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d2332-110">The **Recruitment management** workspace contains an **Analytics** tab. This tab contains the embedded Power BI content for recruiting.</span></span> <span data-ttu-id="d2332-111">このコンテンツには、[概要] タブと詳細が含まれる追加のタブがあります。</span><span class="sxs-lookup"><span data-stu-id="d2332-111">The content consists of an overview tab and additional tabs that contain details.</span></span> <span data-ttu-id="d2332-112">次の表に各タブのレポートを示します。</span><span class="sxs-lookup"><span data-stu-id="d2332-112">The following table describes the reports on each tab.</span></span>

| <span data-ttu-id="d2332-113">レポート </span><span class="sxs-lookup"><span data-stu-id="d2332-113">Report</span></span>               | <span data-ttu-id="d2332-114">コンテンツ</span><span class="sxs-lookup"><span data-stu-id="d2332-114">Contents</span></span> |
|----------------------|----------|
| <span data-ttu-id="d2332-115">採用の概要</span><span class="sxs-lookup"><span data-stu-id="d2332-115">Recruitment Overview</span></span> | <span data-ttu-id="d2332-116">他のレポートの集計</span><span class="sxs-lookup"><span data-stu-id="d2332-116">Summarizes other reports</span></span> |
| <span data-ttu-id="d2332-117">申請者の分析</span><span class="sxs-lookup"><span data-stu-id="d2332-117">Applicant Analysis</span></span>   | <span data-ttu-id="d2332-118">申請者の総数、ジョブ別申請者、申請者ソース、男性申請者に対する女性申請者、場所別申請者</span><span class="sxs-lookup"><span data-stu-id="d2332-118">Total number of applicants, applicants by job, applicant sources, female to male applicants, and applicants by location</span></span> |
| <span data-ttu-id="d2332-119">申請者のステータス</span><span class="sxs-lookup"><span data-stu-id="d2332-119">Applicant Status</span></span>     | <span data-ttu-id="d2332-120">タイプおよびステータス別申請者および申請者のステータス</span><span class="sxs-lookup"><span data-stu-id="d2332-120">Applicants by type and status, and applicant status</span></span> |
| <span data-ttu-id="d2332-121">採用分析</span><span class="sxs-lookup"><span data-stu-id="d2332-121">Recruiting Analysis</span></span>  | <span data-ttu-id="d2332-122">正味採用率、平均雇用日数、悪い雇用者の割合、採用にかかる費用、採用プロジェクト数、申請者に対する雇用者数、採用プロジェクトによる申請者数と空き状況</span><span class="sxs-lookup"><span data-stu-id="d2332-122">Net hire ratio, average days to hire, percentage of bad hires, recruiting costs, number of recruitment projects, hire to applied, and applicants versus openings by recruitment project</span></span> |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="d2332-123">データ モデルおよびエンティティの理解</span><span class="sxs-lookup"><span data-stu-id="d2332-123">Understanding the data model and entities</span></span>
<span data-ttu-id="d2332-124">これらのレポートのグラフとタイルをフィルター処理し、ダッシュボードに固定することができます。</span><span class="sxs-lookup"><span data-stu-id="d2332-124">You can filter the charts and tiles on these reports, and pin the charts and tiles to the dashboard.</span></span> <span data-ttu-id="d2332-125">Power BI のフィルター処理と固定方法の詳細については、[ダッシュボードの作成およびコンフィギュレーション](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2332-125">For more information about how to filter and pin in Power BI, see [Create and Configure A Dashboard](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).</span></span>

<span data-ttu-id="d2332-126">次の表に、**Recruiting** Power BI コンテンツが基づいているエンティティを示します。</span><span class="sxs-lookup"><span data-stu-id="d2332-126">The following table shows the entities that the **Recruiting** Power BI content was based on.</span></span>

| <span data-ttu-id="d2332-127">エンティティ</span><span class="sxs-lookup"><span data-stu-id="d2332-127">Entity</span></span>               | <span data-ttu-id="d2332-128">コンテンツ</span><span class="sxs-lookup"><span data-stu-id="d2332-128">Contents</span></span>                                                         | <span data-ttu-id="d2332-129">他のエンティティとの関係</span><span class="sxs-lookup"><span data-stu-id="d2332-129">Relationships with other entities</span></span> |
|----------------------|------------------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="d2332-130">申請者</span><span class="sxs-lookup"><span data-stu-id="d2332-130">Applicant</span></span>            | <span data-ttu-id="d2332-131">応募者、雇用申請者、正味雇用率、および費用</span><span class="sxs-lookup"><span data-stu-id="d2332-131">Applicants, hired applicants, net hire ratio, and costs</span></span>          | <span data-ttu-id="d2332-132">申請者名、会社、カレンダーのオフセット、日付、地理的な場所、人口統計、ジョブ、メディア、採用プロジェクト</span><span class="sxs-lookup"><span data-stu-id="d2332-132">Applicant Name, Company, Calendar Offset, Date, Geographic Location, Demographics, Job, Media, Recruitment Project</span></span> |
| <span data-ttu-id="d2332-133">申請者名</span><span class="sxs-lookup"><span data-stu-id="d2332-133">Applicant Name</span></span>       | <span data-ttu-id="d2332-134">申請者の名、姓、フルネーム</span><span class="sxs-lookup"><span data-stu-id="d2332-134">Applicant first name, last name, and full name</span></span>                   | <span data-ttu-id="d2332-135">申請者、採用済申請者、退職済申請者</span><span class="sxs-lookup"><span data-stu-id="d2332-135">Applicant, Employed Applicant, Terminated Applicant</span></span> |
| <span data-ttu-id="d2332-136">カレンダーのオフセット</span><span class="sxs-lookup"><span data-stu-id="d2332-136">Calendar Offset</span></span>      | <span data-ttu-id="d2332-137">レポートをスライスするカレンダーのオフセット</span><span class="sxs-lookup"><span data-stu-id="d2332-137">Calendar offsets to slice reports</span></span>                                | <span data-ttu-id="d2332-138">申請者、採用済申請者、退職済申請者</span><span class="sxs-lookup"><span data-stu-id="d2332-138">Applicant, Employed Applicant, Terminated Applicant</span></span> |
| <span data-ttu-id="d2332-139">法人</span><span class="sxs-lookup"><span data-stu-id="d2332-139">Company</span></span>              | <span data-ttu-id="d2332-140">レポートをフィルター処理する会社</span><span class="sxs-lookup"><span data-stu-id="d2332-140">Companies to filter reports by</span></span>                                   | <span data-ttu-id="d2332-141">申請者、採用済申請者、退職済申請者</span><span class="sxs-lookup"><span data-stu-id="d2332-141">Applicant, Employed Applicant, Terminated Applicant</span></span> |
| <span data-ttu-id="d2332-142">日</span><span class="sxs-lookup"><span data-stu-id="d2332-142">Date</span></span>                 | <span data-ttu-id="d2332-143">日、週、月、年</span><span class="sxs-lookup"><span data-stu-id="d2332-143">Days, weeks, months, and years</span></span>                                   | <span data-ttu-id="d2332-144">申請者、採用済申請者、退職済申請者</span><span class="sxs-lookup"><span data-stu-id="d2332-144">Applicant, Employed Applicant, Terminated Applicant</span></span> |
| <span data-ttu-id="d2332-145">顧客情報</span><span class="sxs-lookup"><span data-stu-id="d2332-145">Demographics</span></span>         | <span data-ttu-id="d2332-146">生年月日、性別、出身民族、配偶者の有無</span><span class="sxs-lookup"><span data-stu-id="d2332-146">Date of birth, gender, ethnic origin, and marital status</span></span>         | <span data-ttu-id="d2332-147">申請者、採用済申請者、退職済申請者</span><span class="sxs-lookup"><span data-stu-id="d2332-147">Applicant, Employed Applicant, Terminated Applicant</span></span> |
| <span data-ttu-id="d2332-148">採用済申請者</span><span class="sxs-lookup"><span data-stu-id="d2332-148">Employed Applicant</span></span>   | <span data-ttu-id="d2332-149">申請者、パフォーマンス、開始日、および申請者のタイプ</span><span class="sxs-lookup"><span data-stu-id="d2332-149">Applicant, performance, start date, and applicant type</span></span>           | <span data-ttu-id="d2332-150">会社、カレンダーのオフセット、日付、地理的な場所、申請者名、雇用、パフォーマンス、ジョブ、メディア、採用プロジェクト</span><span class="sxs-lookup"><span data-stu-id="d2332-150">Company, Calendar Offset, Date, Geographic Location, Applicant Name, Employment, Performance, Job, Media, Recruitment Project</span></span> |
| <span data-ttu-id="d2332-151">雇用</span><span class="sxs-lookup"><span data-stu-id="d2332-151">Employment</span></span>           | <span data-ttu-id="d2332-152">開始日、終了日、移行日</span><span class="sxs-lookup"><span data-stu-id="d2332-152">Start date, end date, and transition date</span></span>                        | <span data-ttu-id="d2332-153">申請者、採用済申請者、退職済申請者</span><span class="sxs-lookup"><span data-stu-id="d2332-153">Applicant, Employed Applicant, Terminated Applicant</span></span> |
| <span data-ttu-id="d2332-154">地理的な場所</span><span class="sxs-lookup"><span data-stu-id="d2332-154">Geographic Location</span></span>  | <span data-ttu-id="d2332-155">市町村、市区郡、郵便番号、都道府県</span><span class="sxs-lookup"><span data-stu-id="d2332-155">City, county, postal code, and state or province</span></span>                 | <span data-ttu-id="d2332-156">申請者、採用済申請者、退職済申請者</span><span class="sxs-lookup"><span data-stu-id="d2332-156">Applicant, Employed Applicant, Terminated Applicant</span></span> |
| <span data-ttu-id="d2332-157">ジョブ</span><span class="sxs-lookup"><span data-stu-id="d2332-157">Job</span></span>                  | <span data-ttu-id="d2332-158">職務、タイプ、役職</span><span class="sxs-lookup"><span data-stu-id="d2332-158">Function, type, and title</span></span>                                        | <span data-ttu-id="d2332-159">申請者、採用済申請者、退職済申請者</span><span class="sxs-lookup"><span data-stu-id="d2332-159">Applicant, Employed Applicant, Terminated Applicant</span></span> |
| <span data-ttu-id="d2332-160">メディア</span><span class="sxs-lookup"><span data-stu-id="d2332-160">Media</span></span>                | <span data-ttu-id="d2332-161">申請者のソース</span><span class="sxs-lookup"><span data-stu-id="d2332-161">Source of applicants</span></span>                                             | <span data-ttu-id="d2332-162">申請者、採用済申請者、退職済申請者</span><span class="sxs-lookup"><span data-stu-id="d2332-162">Applicant, Employed Applicant, Terminated Applicant</span></span> |
| <span data-ttu-id="d2332-163">パフォーマンス</span><span class="sxs-lookup"><span data-stu-id="d2332-163">Performance</span></span>          | <span data-ttu-id="d2332-164">評価、説明、評価モデル</span><span class="sxs-lookup"><span data-stu-id="d2332-164">Rating, description, and rating model</span></span>                            | <span data-ttu-id="d2332-165">申請者、採用済申請者、退職済申請者</span><span class="sxs-lookup"><span data-stu-id="d2332-165">Applicant, Employed Applicant, Terminated Applicant</span></span> |
| <span data-ttu-id="d2332-166">採用プロジェクト</span><span class="sxs-lookup"><span data-stu-id="d2332-166">Recruitment Project</span></span>  | <span data-ttu-id="d2332-167">プロジェクト説明、プロジェクト ステータス、空き状況</span><span class="sxs-lookup"><span data-stu-id="d2332-167">Project description, project status, and openings</span></span>                | <span data-ttu-id="d2332-168">申請者、採用済申請者、退職済申請者</span><span class="sxs-lookup"><span data-stu-id="d2332-168">Applicant, Employed Applicant, Terminated Applicant</span></span> |
| <span data-ttu-id="d2332-169">退職済申請者</span><span class="sxs-lookup"><span data-stu-id="d2332-169">Terminated Applicant</span></span> | <span data-ttu-id="d2332-170">退職済申請者、理由、パフォーマンス、終了日</span><span class="sxs-lookup"><span data-stu-id="d2332-170">Terminated applicants, reason, performance, and termination date</span></span> | <span data-ttu-id="d2332-171">会社、カレンダーのオフセット、日付、地理的な場所、パフォーマンス、人口統計、雇用、メディア、採用プロジェクト、申請者名</span><span class="sxs-lookup"><span data-stu-id="d2332-171">Company, Calendar Offset, Date, Geographic Location, Performance, Demographics, Employment, Media, Recruitment Project, Applicant Name</span></span> |