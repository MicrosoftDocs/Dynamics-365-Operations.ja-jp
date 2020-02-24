---
title: 職務のコンポーネントの設定
description: この記事では、ジョブに含められる概念に関する要素の説明、および組織内の要素の使用方法の例を示します。
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.author: anbichse
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources, Retail
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 02475cdc23565c1d49c9f1bb6901101b16acf3a5
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009707"
---
# <a name="set-up-the-components-of-a-job"></a><span data-ttu-id="1b90a-103">職務のコンポーネントの設定</span><span class="sxs-lookup"><span data-stu-id="1b90a-103">Set up the components of a job</span></span>

<span data-ttu-id="1b90a-104">この記事では、ジョブに含められる概念に関する要素の説明、および組織内の要素の使用方法の例を示します。</span><span class="sxs-lookup"><span data-stu-id="1b90a-104">This article describes the conceptual elements that a job can include and provides examples of how you can use those elements in your organization.</span></span> 

<span data-ttu-id="1b90a-105">ジョブを作成できるようになる前に、いくつか参照情報を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b90a-105">Before you can create jobs, you must set up some reference information.</span></span> <span data-ttu-id="1b90a-106">名前だけあるジョブを作成できます。</span><span class="sxs-lookup"><span data-stu-id="1b90a-106">You can create a job that has only a name.</span></span> <span data-ttu-id="1b90a-107">ただし、職位などの追加の情報を含めることで、ジョブに割り当てられた職位の既定値を提供します。</span><span class="sxs-lookup"><span data-stu-id="1b90a-107">However, by including additional information, such as a job title, you provide default values for the positions that are assigned to the job.</span></span> <span data-ttu-id="1b90a-108">また、入力する情報には、特定のジョブに対する報酬プランのフィルター処理に使用できるものもあります。</span><span class="sxs-lookup"><span data-stu-id="1b90a-108">Additionally, some of the information that you enter can be used to filter compensation plans to specific jobs.</span></span> <span data-ttu-id="1b90a-109">特定のジョブに対する報酬プランをフィルター処理で使用できる資格を設定する場合、ジョブを設定する前に、職務権限とジョブ タイプを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b90a-109">If you want to set up eligibility that you can use to filter compensation plans to a specific job, you should set up job functions and job types before you set up jobs.</span></span> <span data-ttu-id="1b90a-110">使用できるこれらの既定値があることによって、ジョブに職位を追加する際に時間を節約できます。</span><span class="sxs-lookup"><span data-stu-id="1b90a-110">By having these default values available, you will save time when you add positions to the job.</span></span> 

<span data-ttu-id="1b90a-111">職位、ジョブ タイプ、職務権限など一部のジョブの詳細は、有効日を伴います。</span><span class="sxs-lookup"><span data-stu-id="1b90a-111">Some job details, such as the job title, type, and function, are date-effective.</span></span> <span data-ttu-id="1b90a-112">今日ジョブを作成して、後日まで詳細を追加せず、作成日時点でジョブを表示した場合、詳細は表示されません。</span><span class="sxs-lookup"><span data-stu-id="1b90a-112">If you create a job today but don't add these details until later, and you then look at the job as of the creation date, these details won't appear.</span></span> <span data-ttu-id="1b90a-113">したがって、必要になる前にこの参照情報を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b90a-113">Therefore, you should create some of this reference information before you require it.</span></span> <span data-ttu-id="1b90a-114">そうすれば、新しいジョブの作成時に情報を追加できます。</span><span class="sxs-lookup"><span data-stu-id="1b90a-114">That way, you can add the information to new jobs when you create them.</span></span>

## <a name="job-titles"></a><span data-ttu-id="1b90a-115">職位</span><span class="sxs-lookup"><span data-stu-id="1b90a-115">Job titles</span></span>
<span data-ttu-id="1b90a-116">ジョブを作成する前に、それらの職位を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b90a-116">Before you create jobs, you must set up titles for those jobs.</span></span> <span data-ttu-id="1b90a-117">職位は、その職位が関連付けられているジョブの職位を継承します。</span><span class="sxs-lookup"><span data-stu-id="1b90a-117">Positions inherit job titles from the jobs that the positions are associated with.</span></span> 

<span data-ttu-id="1b90a-118">検索機能を使って開ける**職位**ページを使用して職位を管理します。</span><span class="sxs-lookup"><span data-stu-id="1b90a-118">Maintain job titles using the **Titles** page, which you can open by using the Search function.</span></span> <span data-ttu-id="1b90a-119">**職位**ページで、ジョブに使用を予定している職位を入力します。</span><span class="sxs-lookup"><span data-stu-id="1b90a-119">On the \*\*Titles \*\*page, enter the titles that you plan to use for your jobs.</span></span>

## <a name="job-types"></a><span data-ttu-id="1b90a-120">ジョブ タイプ</span><span class="sxs-lookup"><span data-stu-id="1b90a-120">Job types</span></span>
<span data-ttu-id="1b90a-121">ジョブ タイプを使用して、類似したジョブをカテゴリにグループ化します。</span><span class="sxs-lookup"><span data-stu-id="1b90a-121">You use job types to group similar jobs into categories.</span></span> <span data-ttu-id="1b90a-122">ジョブ タイプは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="1b90a-122">Job types aren't required.</span></span> <span data-ttu-id="1b90a-123">ただし、報酬管理の適格性ルールを設定する際にジョブ タイプを使用する予定の場合は、ジョブを設定する前にジョブ タイプを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b90a-123">However, if you plan to use job types when you set up eligibility rules for compensation management, you should set up job types before you set up jobs.</span></span> <span data-ttu-id="1b90a-124">ジョブ タイプの例は、フルタイムおよびパートタイム、または給与および時給があります。</span><span class="sxs-lookup"><span data-stu-id="1b90a-124">Some examples of job types are full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="1b90a-125">**ジョブ タイプ** ページを使用してジョブ タイプを管理します。</span><span class="sxs-lookup"><span data-stu-id="1b90a-125">You maintain job types by using the **Job types** page.</span></span> <span data-ttu-id="1b90a-126">**ジョブ タイプ** ページで、ジョブ タイプの名前と簡単な説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="1b90a-126">On the **Job types** page, enter a name and a brief description for the job type.</span></span> <span data-ttu-id="1b90a-127">**控除ステータス**フィールドで、次のいずれかのオプションを選択して、このジョブ タイプが含まれるジョブの公正労働基準法 (FLSA) 控除状況を示します。</span><span class="sxs-lookup"><span data-stu-id="1b90a-127">In the **Exempt status** field, select one of the following options to indicate the Fair Labor Standards Act (FLSA) exempt status of jobs that have this job type:</span></span>

-   <span data-ttu-id="1b90a-128">**免税** – ジョブは FLSA に基づいた残業時間から免税されます。</span><span class="sxs-lookup"><span data-stu-id="1b90a-128">**Exempt** – Jobs are exempt from overtime under the FLSA.</span></span>
-   <span data-ttu-id="1b90a-129">**非控除** – ジョブは FLSA に基づいた残業時間から除外されません。</span><span class="sxs-lookup"><span data-stu-id="1b90a-129">**Non-exempt** – Jobs aren't exempt from overtime under the FLSA.</span></span>
-   <span data-ttu-id="1b90a-130">**適用しない** – FLSA は適用できません。</span><span class="sxs-lookup"><span data-stu-id="1b90a-130">**Does not apply** – FLSA coverage isn't applicable.</span></span>

## <a name="job-functions"></a><span data-ttu-id="1b90a-131">ジョブ機能</span><span class="sxs-lookup"><span data-stu-id="1b90a-131">Job functions</span></span>
<span data-ttu-id="1b90a-132">ジョブ ジャンクションは、高レベルの機能カテゴリについて説明し、高レベルの職務に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="1b90a-132">Job junctions describe high-level functional categories and relate high-level duties.</span></span> <span data-ttu-id="1b90a-133">ジョブ ジャンクションは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="1b90a-133">Job functions aren't required.</span></span> <span data-ttu-id="1b90a-134">職務権限をジョブ タイプと組み合わせて使用すると、特定のジョブに対する報酬プランをフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="1b90a-134">You can use job functions, together with job types, to filter compensation plans to specific jobs.</span></span> <span data-ttu-id="1b90a-135">職務権限とジョブ タイプを報酬プランに関連付けるには、**適格性ルール** ページで適格性ルールを設定します。</span><span class="sxs-lookup"><span data-stu-id="1b90a-135">You associate job functions and job types with compensation plans by setting up eligibility rules on the **Eligibility rules** page.</span></span> <span data-ttu-id="1b90a-136">その後、適格性ルールで定義した特定のジョブ タイプと職務権限の組み合わせに適用される報酬プランに、レベルのセットを関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="1b90a-136">You can then attach a set of levels to a compensation plan that apply to the specific combination of a job type and job function that you've defined through an eligibility rule.</span></span> <span data-ttu-id="1b90a-137">(これらの機能は、固定報酬プランと変動報酬プランの両方に適用されます)。ただし、報酬管理の適格性ルールを設定する際に職務権限を使用する予定の場合は、ジョブを設定する前に職務権限を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b90a-137">(These features apply to both fixed compensation plans and variable compensation plans.) However, if you plan to use job functions when you set up eligibility rules for compensation management, you should set up job functions before you set up jobs.</span></span> <span data-ttu-id="1b90a-138">次の表では、職務権限の例を示します。</span><span class="sxs-lookup"><span data-stu-id="1b90a-138">The following table shows some examples of job functions.</span></span>

| <span data-ttu-id="1b90a-139">ジョブ</span><span class="sxs-lookup"><span data-stu-id="1b90a-139">Job</span></span>           | <span data-ttu-id="1b90a-140">職務権限</span><span class="sxs-lookup"><span data-stu-id="1b90a-140">Job function</span></span>         |
|---------------|----------------------|
| <span data-ttu-id="1b90a-141">販売マネージャー</span><span class="sxs-lookup"><span data-stu-id="1b90a-141">Sales manager</span></span> | <span data-ttu-id="1b90a-142">中間レベル マネージャー</span><span class="sxs-lookup"><span data-stu-id="1b90a-142">Mid-level Manager</span></span>    |
| <span data-ttu-id="1b90a-143">経理担当</span><span class="sxs-lookup"><span data-stu-id="1b90a-143">Accountant</span></span>    | <span data-ttu-id="1b90a-144">職務</span><span class="sxs-lookup"><span data-stu-id="1b90a-144">Professionals</span></span>        |

<span data-ttu-id="1b90a-145">**職務権限**ページを使用して職務権限を管理します。</span><span class="sxs-lookup"><span data-stu-id="1b90a-145">You maintain job functions by using the **Job functions** page.</span></span> <span data-ttu-id="1b90a-146">**職務権限**ページで、職務権限の ID コードと簡単な説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="1b90a-146">On the **Job functions** page, enter an identification code and a brief description for the job function.</span></span>

## <a name="job-tasks"></a><span data-ttu-id="1b90a-147">職務</span><span class="sxs-lookup"><span data-stu-id="1b90a-147">Job tasks</span></span>
<span data-ttu-id="1b90a-148">職務は、ジョブの職位に就く作業者が実行しなければならない基本タスクを表します。</span><span class="sxs-lookup"><span data-stu-id="1b90a-148">Job tasks describe the basic tasks that a worker who is in a position for a job must complete.</span></span> <span data-ttu-id="1b90a-149">同じ職務は、複数のジョブおよびそれらの職務を使用する職位に追加できます。</span><span class="sxs-lookup"><span data-stu-id="1b90a-149">The same job task can be added to multiple jobs, and to positions for the jobs that use those job tasks.</span></span> <span data-ttu-id="1b90a-150">次の表では、職務の例を示します。</span><span class="sxs-lookup"><span data-stu-id="1b90a-150">The following table shows some examples of job tasks.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1b90a-151">ジョブ</span><span class="sxs-lookup"><span data-stu-id="1b90a-151">Job</span></span></th>
<th><span data-ttu-id="1b90a-152">職務</span><span class="sxs-lookup"><span data-stu-id="1b90a-152">Job task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b90a-153">販売マネージャー</span><span class="sxs-lookup"><span data-stu-id="1b90a-153">Sales manager</span></span></td>
<td><ul>
<li><span data-ttu-id="1b90a-154"><strong>実績の確認</strong> – 各販売担当者の業績を確認します。</span><span class="sxs-lookup"><span data-stu-id="1b90a-154"><strong>Perf-review</strong> – Review each salesperson&#39;s job performance.</span></span></li>
<li><span data-ttu-id="1b90a-155"><strong>ABS 確認</strong> – 各販売担当者の登録または休暇要求を承認または却下します。</span><span class="sxs-lookup"><span data-stu-id="1b90a-155"><strong>Abs-review</strong> – Approve or reject each salesperson&#39;s absence requests or registrations.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b90a-156">経理担当</span><span class="sxs-lookup"><span data-stu-id="1b90a-156">Accountant</span></span></td>
<td><span data-ttu-id="1b90a-157"><strong>FIN レポート</strong> - 最高財務責任者に提出する現在の週財務レポート。</span><span class="sxs-lookup"><span data-stu-id="1b90a-157"><strong>FIN-Report</strong> – Present weekly financial reports to the chief financial officer.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1b90a-158">**職務** ページを使用して職務を管理します。</span><span class="sxs-lookup"><span data-stu-id="1b90a-158">You maintain job tasks by using the **Job tasks** page.</span></span> <span data-ttu-id="1b90a-159">**職務** ページで、職務の名前と簡単な説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="1b90a-159">On the **Job tasks** page, enter a name and description for the job task.</span></span> <span data-ttu-id="1b90a-160">**メモ**フィールドで、追加情報をオプションで入力できます。</span><span class="sxs-lookup"><span data-stu-id="1b90a-160">In the **Note** field, you can optionally enter additional information.</span></span> <span data-ttu-id="1b90a-161">メモは、ここで入力したメモを変更しないで特定のジョブに対して更新できます。</span><span class="sxs-lookup"><span data-stu-id="1b90a-161">The notes can be updated for a specific job without changing the notes that you entered here.</span></span>

## <a name="areas-of-responsibility"></a><span data-ttu-id="1b90a-162">担当領域</span><span class="sxs-lookup"><span data-stu-id="1b90a-162">Areas of responsibility</span></span>
<span data-ttu-id="1b90a-163">職位の作業者が担当する作業の役割、プロセス、および製品を示す担当領域を使用します。</span><span class="sxs-lookup"><span data-stu-id="1b90a-163">You use areas of responsibility to indicate the work roles, processes, and products that a worker who is in a position for a job is responsible for.</span></span> <span data-ttu-id="1b90a-164">たとえば、「経理担当」というジョブの場合、担当領域には、「製品 A の財務報告」があります。</span><span class="sxs-lookup"><span data-stu-id="1b90a-164">For example, for a job that is named "Accountant," one area of responsibility might be "Financial reporting for product A."</span></span> <span data-ttu-id="1b90a-165">検索機能を使用して開ける**担当領域**ページを使用して担当領域を管理します。</span><span class="sxs-lookup"><span data-stu-id="1b90a-165">You maintain areas of responsibility by using the **Areas of responsibility** page, which you can find by using the Search function.</span></span> <span data-ttu-id="1b90a-166">**担当領域**ページで、担当領域の名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="1b90a-166">On the **Areas of responsibility** page, enter a name and description for the responsibility.</span></span> <span data-ttu-id="1b90a-167">**メモ**フィールドで、追加情報をオプションで入力できます。</span><span class="sxs-lookup"><span data-stu-id="1b90a-167">In the **Note** field, you can optionally enter additional information.</span></span> <span data-ttu-id="1b90a-168">メモは、ここで入力したメモを変更しないで特定のジョブに対して更新できます。</span><span class="sxs-lookup"><span data-stu-id="1b90a-168">The notes can be updated for a specific job without changing the notes that you entered here.</span></span>

## <a name="steps-for-creating-a-job"></a><span data-ttu-id="1b90a-169">ジョブを作成する手順</span><span class="sxs-lookup"><span data-stu-id="1b90a-169">Steps for creating a job</span></span>
<span data-ttu-id="1b90a-170">新しいジョブを作成するためのステップ バイ ステップの手順については次の記事 [新しいジョブの定義](../fin-and-ops/hr/tasks/define-new-jobs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1b90a-170">Refer to the [Define new jobs](../fin-and-ops/hr/tasks/define-new-jobs.md) article for the step-by-step procedure for creating a new job.</span></span> 
