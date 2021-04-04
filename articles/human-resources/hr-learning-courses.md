---
title: トレーニング コースの設定
description: 人事管理の管理者とマネージャーは、作業者に提供されるトレーニングに関する情報を管理するためにコース機能を使用できます。
author: andreabichsel
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: e642146701edad6b2275156e89048bc5a418c8a0
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467918"
---
# <a name="set-up-training-courses"></a><span data-ttu-id="56cd0-103">トレーニング コースの設定</span><span class="sxs-lookup"><span data-stu-id="56cd0-103">Set up training courses</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="56cd0-104">人事管理の管理者とマネージャーは、作業者に提供されるトレーニングに関する情報を管理するためにコース機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="56cd0-104">Human resources administrators and managers can use the courses features to maintain information about the training that's offered to workers.</span></span>

 <a name="set-up-prerequisites"></a><span data-ttu-id="56cd0-105"> 前提条件の設定</span><span class="sxs-lookup"><span data-stu-id="56cd0-105">Set up prerequisites</span></span>
---------------------

<span data-ttu-id="56cd0-106">次の情報は、必須でコースを作成する前に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="56cd0-106">The following information is required and must be set up before you create courses.</span></span>
-   <span data-ttu-id="56cd0-107">**コースのタイプ**</span><span class="sxs-lookup"><span data-stu-id="56cd0-107">**Course types**</span></span>

<span data-ttu-id="56cd0-108">次の情報は、コースに対して指定できるオプションの情報です。</span><span class="sxs-lookup"><span data-stu-id="56cd0-108">The following information is optional information that you can specify for courses.</span></span> <span data-ttu-id="56cd0-109">コースのこの情報を入力することがわかっている場合は、コースのレコードを作成する前にこの情報を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="56cd0-109">If you know that you will be entering this information for courses, you should set up this information before you create course records.</span></span>
-   <span data-ttu-id="56cd0-110">**教室グループ**</span><span class="sxs-lookup"><span data-stu-id="56cd0-110">**Classroom groups**</span></span>
-   <span data-ttu-id="56cd0-111">**コース グループ**</span><span class="sxs-lookup"><span data-stu-id="56cd0-111">**Course groups**</span></span>
-   <span data-ttu-id="56cd0-112">**コースの開催場所**</span><span class="sxs-lookup"><span data-stu-id="56cd0-112">**Course locations**</span></span>
-   <span data-ttu-id="56cd0-113">**教室**</span><span class="sxs-lookup"><span data-stu-id="56cd0-113">**Classrooms**</span></span>
-   <span data-ttu-id="56cd0-114">**講師**</span><span class="sxs-lookup"><span data-stu-id="56cd0-114">**Instructors**</span></span>

## <a name="course-types"></a><span data-ttu-id="56cd0-115">コースのタイプ</span><span class="sxs-lookup"><span data-stu-id="56cd0-115">Course types</span></span>
<span data-ttu-id="56cd0-116">コース構造または内容によってコースを分類するために、コース タイプを使用できます。</span><span class="sxs-lookup"><span data-stu-id="56cd0-116">You can use course types to categorize courses according to the structure or content of the course.</span></span> <span data-ttu-id="56cd0-117">**コース タイプ** ページでコースのタイプを作成できます。</span><span class="sxs-lookup"><span data-stu-id="56cd0-117">You can create course types on the **Course types** page.</span></span> <span data-ttu-id="56cd0-118">コースのレコードを作成するときにコース タイプを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="56cd0-118">You must select a course type when you create a course record.</span></span>

## <a name="course-setup-type"></a><span data-ttu-id="56cd0-119">コース設定のタイプ</span><span class="sxs-lookup"><span data-stu-id="56cd0-119">Course setup type</span></span>
<span data-ttu-id="56cd0-120">次の表に、コースの 3 種類の設定タイプの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="56cd0-120">The following table lists the three setup types for courses.</span></span> <span data-ttu-id="56cd0-121">設定タイプによって、コースの構造が決まります。</span><span class="sxs-lookup"><span data-stu-id="56cd0-121">Setup types determine the structure of the course.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="56cd0-122">設定タイプ</span><span class="sxs-lookup"><span data-stu-id="56cd0-122">Setup type</span></span></th>
<th><span data-ttu-id="56cd0-123">説明</span><span class="sxs-lookup"><span data-stu-id="56cd0-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="56cd0-124"><strong>標準</strong></span><span class="sxs-lookup"><span data-stu-id="56cd0-124"><strong>Standard</strong></span></span></td>
<td><span data-ttu-id="56cd0-125">毎日の議題がないコースのこのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="56cd0-125">Select this type for courses that will not have a daily agenda.</span></span> <span data-ttu-id="56cd0-126">これは、新しいコースを作成するときの既定の設定のタイプです。</span><span class="sxs-lookup"><span data-stu-id="56cd0-126">This is the default setup type when you create a new course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56cd0-127"><strong>議題</strong></span><span class="sxs-lookup"><span data-stu-id="56cd0-127"><strong>Agenda</strong></span></span></td>
<td><span data-ttu-id="56cd0-128">複数の日数かけて実施するコースの日々の詳細を計画する場合は、このタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="56cd0-128">Select this type to plan the details of each day of a course that takes place over multiple days.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56cd0-129"><strong>議題 + セッション</strong></span><span class="sxs-lookup"><span data-stu-id="56cd0-129"><strong>Agenda + session</strong></span></span></td>
<td><span data-ttu-id="56cd0-130">より複雑なコースに対してこのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="56cd0-130">Select this type for the more complex courses.</span></span> <span data-ttu-id="56cd0-131">たとえば、追跡およびセッションにコースの議題を分割できます。</span><span class="sxs-lookup"><span data-stu-id="56cd0-131">For example, you can divide the agenda for the course into tracks and sessions.</span></span>
<ul>
<li><span data-ttu-id="56cd0-132"><strong>トラック</strong> – トラックは、コースの特定のサブジェクト領域です。</span><span class="sxs-lookup"><span data-stu-id="56cd0-132"><strong>Track</strong> – Tracks are specific subject areas for a course.</span></span></li>
<li><span data-ttu-id="56cd0-133"><strong>セッション</strong> - セッションはトラックに分割され、トラックに関連する特定プロセスまたは技術を識別できます。</span><span class="sxs-lookup"><span data-stu-id="56cd0-133"><strong>Sessions</strong> – Sessions divide up tracks and help identify specific processes or techniques that are relevant to the track.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a><span data-ttu-id="56cd0-134">コースのタスク</span><span class="sxs-lookup"><span data-stu-id="56cd0-134">Course tasks</span></span>
<span data-ttu-id="56cd0-135">コースごとに、次のタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="56cd0-135">For each course, you can complete the following tasks.</span></span>
- <span data-ttu-id="56cd0-136">参加者の登録</span><span class="sxs-lookup"><span data-stu-id="56cd0-136">Register participants</span></span>
- <span data-ttu-id="56cd0-137">登録期限の指定</span><span class="sxs-lookup"><span data-stu-id="56cd0-137">Specify a registration deadline</span></span>
- <span data-ttu-id="56cd0-138">参加者の最小数と最大数の定義</span><span class="sxs-lookup"><span data-stu-id="56cd0-138">Define the minimum and maximum number of participants</span></span>
- <span data-ttu-id="56cd0-139">コースの開催場所と教室の割り当て</span><span class="sxs-lookup"><span data-stu-id="56cd0-139">Assign a course location and classroom</span></span>
- <span data-ttu-id="56cd0-140">コース参加者へのホテルの推奨</span><span class="sxs-lookup"><span data-stu-id="56cd0-140">Recommend hotels to course participants</span></span>
- <span data-ttu-id="56cd0-141">コースの説明の作成 (作成後は従業員セルフ サービスで通知することが可能)</span><span class="sxs-lookup"><span data-stu-id="56cd0-141">Create a course description, which you can then advertise on Employee self service</span></span>

  ><span data-ttu-id="56cd0-142">**注記** 登録者がいない場合のみコースを削除できます。</span><span class="sxs-lookup"><span data-stu-id="56cd0-142">**Note** You can delete a course only if no one has registered for it.</span></span> 

## <a name="course-statuses"></a><span data-ttu-id="56cd0-143">コースのステータス</span><span class="sxs-lookup"><span data-stu-id="56cd0-143">Course statuses</span></span>
<span data-ttu-id="56cd0-144">次の表に、可能なコースのステータスとコースに特定のステータスがある場合に実行するアクションを示します。</span><span class="sxs-lookup"><span data-stu-id="56cd0-144">The following table lists the possible course statuses and the actions that you can complete when the course has a specific status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="56cd0-145">ステータス</span><span class="sxs-lookup"><span data-stu-id="56cd0-145">Status</span></span></th>
<th><span data-ttu-id="56cd0-146">アクション</span><span class="sxs-lookup"><span data-stu-id="56cd0-146">Actions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="56cd0-147"><strong>作成済</strong></span><span class="sxs-lookup"><span data-stu-id="56cd0-147"><strong>Created</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="56cd0-148">コース情報を入力および修正します。</span><span class="sxs-lookup"><span data-stu-id="56cd0-148">Enter and modify course information.</span></span></li>
<li><span data-ttu-id="56cd0-149">作業者がコースに登録できるように <strong>オープン</strong> にコースのステータスを変更します。</span><span class="sxs-lookup"><span data-stu-id="56cd0-149">Change the course status to <strong>Open</strong> so that workers can register for the course.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56cd0-150"><strong>開始</strong></span><span class="sxs-lookup"><span data-stu-id="56cd0-150"><strong>Open</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="56cd0-151">コースの参加者を登録します。</span><span class="sxs-lookup"><span data-stu-id="56cd0-151">Register participants for the course.</span></span></li>
<li><span data-ttu-id="56cd0-152">コースの参加者をコースから削除します。</span><span class="sxs-lookup"><span data-stu-id="56cd0-152">Remove participants from the course.</span></span></li>
<li><span data-ttu-id="56cd0-153">コースの参加者を確認します。</span><span class="sxs-lookup"><span data-stu-id="56cd0-153">Confirm participants for the course.</span></span></li>
<li><span data-ttu-id="56cd0-154">コースのステータスを <strong> クローズ</strong> または <strong>キャンセル</strong> に変更します。</span><span class="sxs-lookup"><span data-stu-id="56cd0-154">Change the course status to <strong>Closed</strong> or <strong>Canceled</strong>.</span></span></li>
<li><span data-ttu-id="56cd0-155">ステータスが <strong>確認済み</strong> の参加者用のアンケートを計画します。</span><span class="sxs-lookup"><span data-stu-id="56cd0-155">Plan questionnaires for participants whose status is <strong>Confirmed</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56cd0-156"><strong>クローズ済</strong></span><span class="sxs-lookup"><span data-stu-id="56cd0-156"><strong>Closed</strong></span></span></td>
<td><span data-ttu-id="56cd0-157">コースを再度開くことができます。</span><span class="sxs-lookup"><span data-stu-id="56cd0-157">You can reopen the course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56cd0-158"><strong>キャンセル済</strong></span><span class="sxs-lookup"><span data-stu-id="56cd0-158"><strong>Canceled</strong></span></span></td>
<td><span data-ttu-id="56cd0-159">コースを再度開くことができます。</span><span class="sxs-lookup"><span data-stu-id="56cd0-159">You can reopen the course.</span></span></td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a><span data-ttu-id="56cd0-160">コース参加者</span><span class="sxs-lookup"><span data-stu-id="56cd0-160">Course participants</span></span>
<span data-ttu-id="56cd0-161">コース参加者は、トレーニング コースまたはイベントに参加する作業者です。</span><span class="sxs-lookup"><span data-stu-id="56cd0-161">Course participants are workers who participate in a training course or event.</span></span> <span data-ttu-id="56cd0-162">オープン コースの参加者のみを登録できます。</span><span class="sxs-lookup"><span data-stu-id="56cd0-162">You can only register participants for open courses.</span></span> <span data-ttu-id="56cd0-163">コースに登録できる参加者の最小数と最大数は、**コース** ページの **全般** クイック タブで定義されます。</span><span class="sxs-lookup"><span data-stu-id="56cd0-163">The minimum and maximum number of participants that you can register for a course is defined on the **General** FastTab on the **Courses** page.</span></span>

<a name="workflow"></a><span data-ttu-id="56cd0-164">ワークフロー</span><span class="sxs-lookup"><span data-stu-id="56cd0-164">Workflow</span></span>
--------

<span data-ttu-id="56cd0-165">**従業員セルフ サービス** ページからコースに登録する従業員は、承認のワークフローを経て登録することができます。</span><span class="sxs-lookup"><span data-stu-id="56cd0-165">Employees who register for a course through the **Employee self service** page can have their registration routed through workflow for approval.</span></span> <span data-ttu-id="56cd0-166">**コース** ページの **一般** クイック タブで、コースにワークフローを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="56cd0-166">You can assign a workflow to a course on the **General** FastTab on the **Courses** page.</span></span>







[!INCLUDE[footer-include](../includes/footer-banner.md)]