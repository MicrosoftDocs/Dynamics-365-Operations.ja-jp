---
title: "大量雇用プロジェクト"
description: "大量雇用プロジェクトにより、人事管理の専門家が複数の職位を作成し、これらの職位に作業者を効率的に採用することができます。"
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HRMMassHireProject
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 7481
ms.assetid: 5f5eb271-76eb-4305-bd1c-5d171dafccc9
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 0904db82b006f874594881afdb5d568afff575eb
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="mass-hire-projects"></a><span data-ttu-id="61b8c-103">大量雇用プロジェクト</span><span class="sxs-lookup"><span data-stu-id="61b8c-103">Mass hire projects</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="61b8c-104">大量雇用プロジェクトにより、人事管理の専門家が複数の職位を作成し、これらの職位に作業者を効率的に採用することができます。</span><span class="sxs-lookup"><span data-stu-id="61b8c-104">Mass hire projects allow human resources specialists to create multiple positions and efficiently hire workers into those positions.</span></span>

<a name="overview"></a><span data-ttu-id="61b8c-105">概要</span><span class="sxs-lookup"><span data-stu-id="61b8c-105">Overview</span></span>
--------

<span data-ttu-id="61b8c-106">シーズン需要を満たすための採用など、複数の作業者を一度に採用する場合には、大量採用プロジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="61b8c-106">Use mass hire projects when you hire multiple workers at one time, such as when you hire to meet a seasonal demand.</span></span> <span data-ttu-id="61b8c-107">大量採用プロジェクトを作成すると、職位レコード、作業者レコード、および職位への作業者の割り当てを同時に作成できるので便利です。</span><span class="sxs-lookup"><span data-stu-id="61b8c-107">Creating a mass hire project is useful because you can create position records, worker records, and worker assignments for positions at the same time.</span></span> <span data-ttu-id="61b8c-108">大量雇用プロジェクトの職位を作成すると、次の情報を指定できます:</span><span class="sxs-lookup"><span data-stu-id="61b8c-108">When you create positions for a mass hire project, you can specify the following information:</span></span>
-   <span data-ttu-id="61b8c-109">作成する職位の数</span><span class="sxs-lookup"><span data-stu-id="61b8c-109">The number of positions to create</span></span>
-   <span data-ttu-id="61b8c-110">職位に雇用した人員の作業者タイプ</span><span class="sxs-lookup"><span data-stu-id="61b8c-110">The worker type of the people that you will hire for the positions</span></span>
-   <span data-ttu-id="61b8c-111">職位に関連付けられているジョブと部門</span><span class="sxs-lookup"><span data-stu-id="61b8c-111">The department and the job that are associated with the positions</span></span>
-   <span data-ttu-id="61b8c-112">職位のフルタイム相当値</span><span class="sxs-lookup"><span data-stu-id="61b8c-112">The full-time equivalent value of the position</span></span>

## <a name="example"></a><span data-ttu-id="61b8c-113">例</span><span class="sxs-lookup"><span data-stu-id="61b8c-113">Example</span></span>
<span data-ttu-id="61b8c-114">夏に、通常は会社で使用できる見習い期間に対応するために 15-20 人のパートタイムの大学生を雇用します。</span><span class="sxs-lookup"><span data-stu-id="61b8c-114">In the summer, you usually hire 15-20 part-time college students to fill available internships in your company.</span></span> <span data-ttu-id="61b8c-115">今年、5 人の経理担当者、5 人の注文処理担当者および 5 人のレジ担当者を雇用しようとしているとします。</span><span class="sxs-lookup"><span data-stu-id="61b8c-115">This year, you want to hire five accountants, five order processors, and five cashiers.</span></span> <span data-ttu-id="61b8c-116">各職位のレコードと作業者レコードを個別に作成する代わりに、「サマー インターン」と呼ばれる大量雇用プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="61b8c-116">Instead of creating each position record and worker record separately, you create one mass hire project called “SummerInterns”.</span></span> <span data-ttu-id="61b8c-117">プロジェクトの開始日および終了日は、大量雇用プロジェクトに対して作成した職位の職位期間の開始日および終了日と関連付けます。</span><span class="sxs-lookup"><span data-stu-id="61b8c-117">The project start and end dates correlate with the start and end dates of the position durations for the positions you create for the mass hire project.</span></span> 

<span data-ttu-id="61b8c-118">**大量雇用プロジェクト** ページで、「サマー インターン」プロジェクトを選択してから、[**プロジェクトを開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="61b8c-118">In the **Mass hire projects** page, select the “SummerInterns” project and then click **Open project**.</span></span> <span data-ttu-id="61b8c-119">未処理の大量雇用プロジェクトで、[**職位の作成**] をクリックし、経理担当者の職位に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="61b8c-119">In the open mass hire project, click **Create positions** and enter information about the accountant position.</span></span> <span data-ttu-id="61b8c-120">5 人の経理担当者の職位をそれぞれ同じ情報で作成することを指定でき、それから [OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="61b8c-120">You can indicate that five accountant positions should be created using the same information for each one, and then click OK.</span></span> <span data-ttu-id="61b8c-121">注文処理担当者と注文レジ担当者の職位についてもこのプロセスを繰り返します。</span><span class="sxs-lookup"><span data-stu-id="61b8c-121">Repeat this process for the order processor and cashier positions.</span></span> 

<span data-ttu-id="61b8c-122">インターンシップの職位に雇用する学生を選択した後、雇用する職位の [**職位の詳細**] に各学生の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="61b8c-122">After selecting students to hire for the internship positions, you'll enter each student’s information in the **Position details** for the position that you're hiring them for.</span></span> <span data-ttu-id="61b8c-123">職位の詳細のすべてを入力して、大量雇用プロジェクト ページの職位を選択してから、[**採用**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="61b8c-123">When you have entered all of the position details, select the position in the Mass hire projects page, and then click **Hire**.</span></span> <span data-ttu-id="61b8c-124">職位レコードは、各職位に作成され、作業者レコードは、雇用従業員ごとに適切な職位に作成され、割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="61b8c-124">A position record will be created for each position and a worker record will be created and assigned to the correct position for each person who you hire.</span></span>

## <a name="mass-hire-project-statuses"></a><span data-ttu-id="61b8c-125">大量採用プロジェクトのステータス</span><span class="sxs-lookup"><span data-stu-id="61b8c-125">Mass hire project statuses</span></span>
<span data-ttu-id="61b8c-126">大量採用プロジェクトでは、次のステータスを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="61b8c-126">A mass hire project can have the following statuses.</span></span>
-   <span data-ttu-id="61b8c-127">作成済み</span><span class="sxs-lookup"><span data-stu-id="61b8c-127">Created</span></span>
-   <span data-ttu-id="61b8c-128">未解決</span><span class="sxs-lookup"><span data-stu-id="61b8c-128">Open</span></span>
-   <span data-ttu-id="61b8c-129">クローズ</span><span class="sxs-lookup"><span data-stu-id="61b8c-129">Closed</span></span>

<span data-ttu-id="61b8c-130">**大量雇用プロジェクト** ページで、[**プロジェクトを開く**] または [**プロジェクトを閉じる**] をクリックして大量採用プロジェクトのステータスを変更します。</span><span class="sxs-lookup"><span data-stu-id="61b8c-130">On the **Mass hire project** page, click **Open project** or **Close project** to change the status of a mass hire project.</span></span> <span data-ttu-id="61b8c-131">次の表に、プロジェクトをそのステータスに応じてどのように処理できるかを示します。</span><span class="sxs-lookup"><span data-stu-id="61b8c-131">The following table describes what you can do with a project according to its status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="61b8c-132">ステータス</span><span class="sxs-lookup"><span data-stu-id="61b8c-132">Status</span></span></th>
<th><span data-ttu-id="61b8c-133">説明</span><span class="sxs-lookup"><span data-stu-id="61b8c-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="61b8c-134">作成済み</span><span class="sxs-lookup"><span data-stu-id="61b8c-134">Created</span></span></td>
<td><span data-ttu-id="61b8c-135">情報の作成と変更は可能ですが、プロジェクトの職位は作成できません。</span><span class="sxs-lookup"><span data-stu-id="61b8c-135">You can create and modify information, but cannot create positions for the project.</span></span> <span data-ttu-id="61b8c-136">これは新規プロジェクトの既定のステータスです。</span><span class="sxs-lookup"><span data-stu-id="61b8c-136">This is the default status for new projects.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61b8c-137">未解決</span><span class="sxs-lookup"><span data-stu-id="61b8c-137">Open</span></span></td>
<td><span data-ttu-id="61b8c-138">プロジェクトの詳細の変更、大量雇用プロジェクトの職位の作成、および職位への人員の採用を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="61b8c-138">You can modify the project details, create positions for the mass hire project, and hire people for the positions.</span></span> <span data-ttu-id="61b8c-139">これは有効なプロジェクトのステータスです。</span><span class="sxs-lookup"><span data-stu-id="61b8c-139">This is the status for active projects.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61b8c-140">クローズ</span><span class="sxs-lookup"><span data-stu-id="61b8c-140">Closed</span></span></td>
<td><span data-ttu-id="61b8c-141">プロジェクトに職位を追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="61b8c-141">You cannot add positions to the project.</span></span> <span data-ttu-id="61b8c-142">大量雇用プロジェクトに職位を追加するには、プロジェクトを再度開きます。</span><span class="sxs-lookup"><span data-stu-id="61b8c-142">To add positions to the mass hire project, open the project again.</span></span> <span data-ttu-id="61b8c-143">これは完了したプロジェクトのステータスです。</span><span class="sxs-lookup"><span data-stu-id="61b8c-143">This is the status for completed projects.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="61b8c-144"><strong>メモ </strong></span><span class="sxs-lookup"><span data-stu-id="61b8c-144"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="61b8c-145">大量採用プロジェクトを閉じるには、プロジェクトのすべての職位のステータスが [作成済み] または [クローズ] であることが必要です。</span><span class="sxs-lookup"><span data-stu-id="61b8c-145">Before you can close a mass hire project, all positions in the project must have a status of either Created or Closed.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
</tbody>
</table>

 






