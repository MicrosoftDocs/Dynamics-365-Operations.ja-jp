---
title: 店舗または従業員へのタスク リストの割り当て
description: このトピックでは、Microsoft Dynamics 365 Commerce の店舗または従業員にタスク リストを割り当てる方法について説明します。
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 3d249809f15b50c59620d69a901a427dc3ecb2f0
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477587"
---
# <a name="assign-task-lists-to-stores-or-employees"></a><span data-ttu-id="c9c43-103">タスク リストを店舗または従業員に割り当てる</span><span class="sxs-lookup"><span data-stu-id="c9c43-103">Assign task lists to stores or employees</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c9c43-104">このトピックでは、Microsoft Dynamics 365 Commerce の店舗または従業員にタスク リストを割り当てる方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c9c43-104">This topic describes how to assign task lists to stores or employees in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c9c43-105">Dynamics 365 Commerce のタスク管理では、タスク リストを複数の店舗または従業員に割り当てることも、店舗と従業員の組み合わせに割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="c9c43-105">Task management in Dynamics 365 Commerce lets you assign a task list to multiple stores or employees, or to a combination of stores and employees.</span></span> <span data-ttu-id="c9c43-106">たとえば、20 店舗の地域のマネージャーは、**休暇シーズン準備** のタスク リストを 20 店舗すべてに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="c9c43-106">For example, a regional manager for 20 stores might want to assign the **Holiday season preparation** task list to all 20 stores.</span></span>

## <a name="start-the-task-list-assignment-process"></a><span data-ttu-id="c9c43-107">タスク リストの割り当てプロセスを開始する</span><span class="sxs-lookup"><span data-stu-id="c9c43-107">Start the task list assignment process</span></span>

<span data-ttu-id="c9c43-108">タスク リストの割り当てプロセスを開始するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c9c43-108">To start the process of assigning a task list, follow these steps.</span></span>

1. <span data-ttu-id="c9c43-109">**Retail と Commerce \>タスク管理\>タスク管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c9c43-109">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="c9c43-110">割り当てるタスク リストを選択します。</span><span class="sxs-lookup"><span data-stu-id="c9c43-110">Select the task list to assign.</span></span>
1. <span data-ttu-id="c9c43-111">**処理の開始** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9c43-111">Select **Start process**.</span></span>
1. <span data-ttu-id="c9c43-112">**処理の開始** ダイアログ ボックスの、**全般** タブで、**プロセス名** のフィールドに名前を入力します (たとえば、**東地域の店舗**)。</span><span class="sxs-lookup"><span data-stu-id="c9c43-112">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name (for example, **East region stores**).</span></span>
1. <span data-ttu-id="c9c43-113">**目標期日** のフィールドに日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="c9c43-113">In the **Target date** field, specify a date.</span></span>
1. <span data-ttu-id="c9c43-114">タスク リストを店舗に割り当てるには、**店舗** タブで **組織階層** フィルターを使用して、店舗を検索および選択します。</span><span class="sxs-lookup"><span data-stu-id="c9c43-114">To assign the task list to stores, on the **Stores** tab, use the **Organization hierarchy** filter to find and select the stores.</span></span>

    <span data-ttu-id="c9c43-115">従業員にタスク リストを割り当てるには、**作業者** タブで従業員を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="c9c43-115">To assign the task list to employees, on the **Workers** tab, find and select the employees.</span></span>

1. <span data-ttu-id="c9c43-116">**OK** を選択し、処理を開始します。</span><span class="sxs-lookup"><span data-stu-id="c9c43-116">Select **OK** to start the process.</span></span> <span data-ttu-id="c9c43-117">タスク リストは、選択した店舗または従業員に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="c9c43-117">The tasks list is assigned to the selected stores or employees.</span></span>

<span data-ttu-id="c9c43-118">次の図は、**処理の開始** ダイアログ ボックスで店舗を検索および選択する方法の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="c9c43-118">The following illustration shows an example of how to find and select stores in the **Start process** dialog box.</span></span>

![プロセスの開始ダイアログ ボックスでの店舗の検索と選択](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a><span data-ttu-id="c9c43-120">定期的なタスク リストの割り当て</span><span class="sxs-lookup"><span data-stu-id="c9c43-120">Assign task lists on a recurring basis</span></span>

<span data-ttu-id="c9c43-121">小売業者は、「木曜休業日のチェックリスト」や 「月の初日のチェックリスト」などの反復タスクを実行している場合があります。</span><span class="sxs-lookup"><span data-stu-id="c9c43-121">Retailer sometimes have recurrent tasks, such as "Thursday closure checklist" or "First day of the month checklist."</span></span> <span data-ttu-id="c9c43-122">したがって、タスク リストを定期的に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="c9c43-122">Therefore, they might want to assign the task list on a recurring basis.</span></span>

1. <span data-ttu-id="c9c43-123">**Retail と Commerce \>タスク管理\>タスク管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c9c43-123">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="c9c43-124">割り当てるタスク リストを選択します。</span><span class="sxs-lookup"><span data-stu-id="c9c43-124">Select the task list to assign.</span></span>
1. <span data-ttu-id="c9c43-125">**処理の開始** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9c43-125">Select **Start process**.</span></span>
1. <span data-ttu-id="c9c43-126">**処理の開始** ダイアログ ボックスの **全般** タブで、**プロセス名** のフィールドに名前を入力します (たとえば、東地域の店舗)。</span><span class="sxs-lookup"><span data-stu-id="c9c43-126">In the **Start process** dialog box, on the **General** tab, in the **Process name** field, enter a name.</span></span>
1. <span data-ttu-id="c9c43-127">**反復** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="c9c43-127">Set the **Recurrence** option to **Yes**.</span></span>
1. <span data-ttu-id="c9c43-128">**日単位の反復目標期日オフセット** フィールドに日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="c9c43-128">In the **Recurrence target date offset in days** field, enter a number of days.</span></span> <span data-ttu-id="c9c43-129">たとえば、**4** を入力すると、目標期日は、反復する期日に 4 日を加えた日付となります。</span><span class="sxs-lookup"><span data-stu-id="c9c43-129">For example, if you enter **4**, the target date is the recurrence date plus four days.</span></span>
1. <span data-ttu-id="c9c43-130">**バックグラウンドで実行** タブで、**反復** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9c43-130">On the **Run in the background** tab, select **Recurrence**.</span></span>
1. <span data-ttu-id="c9c43-131">**定期的なアイテムの定義** ダイアログ ボックスで、頻度の条件を入力し **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9c43-131">In the **Define recurrence** dialog box, enter the frequency criteria, and then select **OK**.</span></span>

<span data-ttu-id="c9c43-132">次の図は、**定期的なアイテムの定義** ダイアログ ボックスで頻度の条件を入力する方法の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="c9c43-132">The following illustration shows an example of how to enter frequency criteria in the **Define recurrence** dialog box.</span></span>

![定期的なアイテムの定義のダイアログ ボックスで、頻度条件を入力する](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a><span data-ttu-id="c9c43-134">タスク リストのステータスの追跡</span><span class="sxs-lookup"><span data-stu-id="c9c43-134">Track task list status</span></span>

<span data-ttu-id="c9c43-135">地域のマネージャーまたは店舗マネージャーである場合は、複数の店舗または従業員に割り当てられているタスク リストのステータスを追跡することができます。</span><span class="sxs-lookup"><span data-stu-id="c9c43-135">If you're a regional manager or store manager, you might want to track the status of task lists that have been assigned to multiple stores or employees.</span></span> <span data-ttu-id="c9c43-136">これにより、割り当てられたタスクを期限までに完了しなかった店舗や作業者をフォローアップすることができます。</span><span class="sxs-lookup"><span data-stu-id="c9c43-136">You can then follow up with stores or workers that didn't complete their assigned tasks on time.</span></span> <span data-ttu-id="c9c43-137">Commerce バック オフィスを使用して、タスク リストのステータスを表示したり、タスクを再割り当てしたり、タスクのステータスを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="c9c43-137">Commerce back office lets you view the status of task lists, reassign tasks, or change the status of a task.</span></span>

<span data-ttu-id="c9c43-138">すべてのタスクのタスク リストのステータスを追跡するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c9c43-138">To track the task list status for all tasks, follow these steps.</span></span>

1. <span data-ttu-id="c9c43-139">**Retail と Commerce \>タスク管理\>タスク管理処理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c9c43-139">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="c9c43-140">さまざまな店舗に割り当てられているすべてのタスク リストのステータスを表示するには、**すべてのタスク リスト** のタブを選択します。</span><span class="sxs-lookup"><span data-stu-id="c9c43-140">Select the **All task lists** tab to view the status of all task lists that are assigned to various stores.</span></span>

<span data-ttu-id="c9c43-141">自分に割り当てられたすべてのタスクのタスク リストのステータスを追跡するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c9c43-141">To track the task list status for all tasks that are assigned to you, follow these steps.</span></span>

1. <span data-ttu-id="c9c43-142">**Retail と Commerce \>タスク管理\>タスク管理処理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c9c43-142">Go to **Retail and Commerce \> Task management \> Task management processes**.</span></span>
1. <span data-ttu-id="c9c43-143">**自分のタスク** または **すべてのタスク** タブを選択し、自分に割り当てられたタスクのステータスを表示または更新します。</span><span class="sxs-lookup"><span data-stu-id="c9c43-143">Select the **My tasks** or **All tasks** tab to view or update the status of tasks that are assigned to you.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c9c43-144">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c9c43-144">Additional resources</span></span>

[<span data-ttu-id="c9c43-145">タスク管理の概要</span><span class="sxs-lookup"><span data-stu-id="c9c43-145">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="c9c43-146">タスク管理のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="c9c43-146">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="c9c43-147">タスク リストの作成およびタスクの追加</span><span class="sxs-lookup"><span data-stu-id="c9c43-147">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="c9c43-148">POS におけるタスクの管理</span><span class="sxs-lookup"><span data-stu-id="c9c43-148">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
