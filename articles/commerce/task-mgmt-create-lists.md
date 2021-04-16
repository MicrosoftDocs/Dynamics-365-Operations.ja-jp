---
title: タスク リストの作成とタスクの追加
description: このトピックでは、Microsoft Dynamics 365 Commerce でタスク リストの作成およびタスクの追加を行う方法について説明します。
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: a0e49d1eced3bb62e78c630b137a5b86121682f3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795240"
---
# <a name="create-task-lists-and-add-tasks"></a><span data-ttu-id="9664d-103">タスク リストの作成とタスクの追加</span><span class="sxs-lookup"><span data-stu-id="9664d-103">Create task lists and add tasks</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9664d-104">このトピックでは、Microsoft Dynamics 365 Commerce でタスク リストの作成およびタスクの追加を行う方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9664d-104">This topic describes how to create task lists and add tasks to them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="9664d-105">*タスク* により、特定の期日、またはそれより前に完了する必要のある特定の作業またはアクションを定義します。</span><span class="sxs-lookup"><span data-stu-id="9664d-105">A *task* defines a specific piece of work or an action that someone must complete on or before a specified due date.</span></span> <span data-ttu-id="9664d-106">Dynamics 365 Commerce において、タスクには詳細な指示および連絡担当者に関する情報を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="9664d-106">In Dynamics 365 Commerce, a task can include detailed instructions and information about a contact person.</span></span> <span data-ttu-id="9664d-107">また、バックオフィスによる操作、販売時点管理 (POS) の操作、またはサイト ページへのリンクを含めることにより、生産性を向上させ、タスクの所有者がタスクを効率的に完了するために必要とするコンテキストを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="9664d-107">It can also include links to back-office operations, point of sale (POS) operations, or site pages, to help improve productivity and provide the context that the task owner requires to complete the task efficiently.</span></span>

<span data-ttu-id="9664d-108">*タスク リスト* は、業務プロセスの一部として完了する必要があるタスクの集合です。</span><span class="sxs-lookup"><span data-stu-id="9664d-108">A *task list* is a collection of tasks that must be completed as part of a business process.</span></span> <span data-ttu-id="9664d-109">たとえば、新しい作業者が研修中に完了する必要のあるタスク リスト、準夜勤のレジ担当者のタスク リスト、または次回の休暇シーズンに向けた店舗の準備のために完了する必要のあるタスク リストなどがあります。</span><span class="sxs-lookup"><span data-stu-id="9664d-109">For example, there might be a task list that a new worker must complete during onboarding, a task list for cashiers who work evening shifts, or a task list that must be completed to prepare the store for an upcoming holiday season.</span></span> <span data-ttu-id="9664d-110">Commerce では、目標期日のあるタスク リストすべてを任意の数の店舗または従業員に割り当てることができ、また繰り返すようにコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="9664d-110">In Commerce, every task list that has a target date can be assigned to any number of stores or employees, and it can be configured to recur.</span></span>

<span data-ttu-id="9664d-111">マネージャーと作業者の両方が、Commerce バックオフィスでタスク リストを作成し、一連の店舗に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="9664d-111">Both managers and workers can create task lists in Commerce back office, and then assign them to a set of stores.</span></span>

## <a name="create-a-task-list"></a><span data-ttu-id="9664d-112">タスク リストの作成</span><span class="sxs-lookup"><span data-stu-id="9664d-112">Create a task list</span></span>

<span data-ttu-id="9664d-113">タスク リストを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9664d-113">To create a task list, follow these steps.</span></span>

1. <span data-ttu-id="9664d-114">**Retail と Commerce \>タスク管理\>タスク管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="9664d-114">Go to **Retail and Commerce \> Task management \> Task management administration**.</span></span>
1. <span data-ttu-id="9664d-115">**新規** を選択し、**名前**、**説明**、および **所有者** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9664d-115">Select **New**, and then enter values in the **Name**, **Description**, and **Owner** fields.</span></span>
1. <span data-ttu-id="9664d-116">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9664d-116">Select **Save**.</span></span>

## <a name="add-tasks-to-a-task-list"></a><span data-ttu-id="9664d-117">タスク リストへのタスクの追加</span><span class="sxs-lookup"><span data-stu-id="9664d-117">Add tasks to a task list</span></span>

<span data-ttu-id="9664d-118">タスク リストにタスクを追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9664d-118">To add tasks to a task list, follow these steps.</span></span>
 
1. <span data-ttu-id="9664d-119">既存のタスク リストの **タスク** クイック タブで、**新規** を選択してタスクを追加します。</span><span class="sxs-lookup"><span data-stu-id="9664d-119">On the **Tasks** FastTab of an existing task list, select **New** to add a task.</span></span>
1. <span data-ttu-id="9664d-120">**新しいタスクの作成** ダイアログ ボックスの **名前** フィールドにタスクの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="9664d-120">In the **Create a new task** dialog box, in the **Name** field, enter a name for the task.</span></span>
1. <span data-ttu-id="9664d-121">**目標期日からの期日のオフセット** フィールドに、正または負の整数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9664d-121">In the **Due data offset from target date** field, enter a positive or negative integer value.</span></span> <span data-ttu-id="9664d-122">たとえば、タスクをタスク リストの期日の 2 日前に完了する必要がある場合、**-2** と入力します。</span><span class="sxs-lookup"><span data-stu-id="9664d-122">For example, enter **-2** if the task should be completed two days before the task list's due date.</span></span>
1. <span data-ttu-id="9664d-123">**メモ** フィールドに、詳細な指示を入力します。</span><span class="sxs-lookup"><span data-stu-id="9664d-123">In the **Notes** field, enter detailed instructions.</span></span>
1. <span data-ttu-id="9664d-124">**連絡担当者** フィールドに、支援が必要な時にタスクの所有者が連絡できる専門家の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="9664d-124">In the **Contact person** field, enter the name of a subject matter expert that the task owner can contact if he or she needs help.</span></span>
1. <span data-ttu-id="9664d-125">**タスクのリンク** フィールドに、タスクの性質に基づいてリンクを入力します。</span><span class="sxs-lookup"><span data-stu-id="9664d-125">In the **Task link** field, enter a link, based on the nature of the task.</span></span>

> [!TIP]
> <span data-ttu-id="9664d-126">タスク リストを作成する時に、**割り当て先** フィールドを使用して別のユーザーにタスクを割り当てることもできますが、タスク リストの作成中にタスクを割り当てないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9664d-126">Although you can use the **Assigned to** field to assign tasks to someone while you're creating a task list, we recommend that you avoid assigning tasks during task list creation.</span></span> <span data-ttu-id="9664d-127">代わりに、個別の店舗に対してリストをインスタンス化した後にタスクを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="9664d-127">Instead, assign the tasks after the list is instantiated for individual stores.</span></span>

## <a name="use-task-links-to-help-improve-worker-productivity"></a><span data-ttu-id="9664d-128">タスクのリンクを使用して作業者の生産性を向上させる</span><span class="sxs-lookup"><span data-stu-id="9664d-128">Use task links to help improve worker productivity</span></span>

<span data-ttu-id="9664d-129">Commerce により、売上レポートの実行、新しい従業員のオリエンテーション用のオンライン トレーニング ビデオの表示、バックオフィス操作の実行など、特定の POS 操作にタスクをリンクすることができます。</span><span class="sxs-lookup"><span data-stu-id="9664d-129">Commerce lets you link tasks to specific POS operations, such as running a sales report, viewing an online training video for new employee orientation, or performing a back-office operation.</span></span> <span data-ttu-id="9664d-130">この機能により、タスクの所有者はタスクを効率的に完了するために必要な情報を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="9664d-130">This feature helps task owners get the information that they need to complete a task efficiently.</span></span>

<span data-ttu-id="9664d-131">タスクの作成時にタスクのリンクを追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9664d-131">To add task links while you create a task, follow these steps.</span></span>

1. <span data-ttu-id="9664d-132">既存のタスク リストの **タスク** クイック タブで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9664d-132">On the **Tasks** FastTab of an existing task list, select **Edit**.</span></span>
1. <span data-ttu-id="9664d-133">**タスクの編集** ダイアログ ボックスの **タスクのリンク** フィールドで、1 つまたは複数のオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="9664d-133">In the **Edit task** dialog box, in the **Task link** field, select one or more of the following options:</span></span>

    - <span data-ttu-id="9664d-134">製品キットなどのバックオフィス操作をコンフィギュレーションするには、**メニュー項目** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9664d-134">Select **Menu item** to configure a back-office operation, such as "Product kits."</span></span>
    - <span data-ttu-id="9664d-135">「売上レポート」などの POS 操作をコンフィギュレーションするには、**POS 操作** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9664d-135">Select **POS Operation** to configure a POS operation, such as "Sales reports."</span></span>
    - <span data-ttu-id="9664d-136">絶対 URL をコンフィギュレーションするには、**URL** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9664d-136">Select **URL** to configure an absolute URL.</span></span>

<span data-ttu-id="9664d-137">次の図は、**タスクの編集** ダイアログ ボックスで選択されたタスクのリンクを示しています。</span><span class="sxs-lookup"><span data-stu-id="9664d-137">The following illustration shows the selection of task links in the **Edit task** dialog box.</span></span>

![タスクの編集ダイアログ ボックスでのタスクのリンクの選択](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a><span data-ttu-id="9664d-139">タスクにリンクするための POS 操作のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="9664d-139">Configure a POS operation so that it can be linked to a task</span></span>

<span data-ttu-id="9664d-140">POS 操作をコンフィギュレーションしてタスクにリンクするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9664d-140">To configure a POS operation so that it can be linked to a task, follow these steps.</span></span>

1. <span data-ttu-id="9664d-141">**Retail および Commerce \> チャネル設定 \> POS 設定 \> POS \> POS 操作** に移動します。</span><span class="sxs-lookup"><span data-stu-id="9664d-141">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="9664d-142">**編集** を選択して、POS 操作を検索し、**タスク管理の有効化** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="9664d-142">Select **Edit**, find the POS operation, and then select the **Enable Task Management** check box for it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9664d-143">追加リソース</span><span class="sxs-lookup"><span data-stu-id="9664d-143">Additional resources</span></span>

[<span data-ttu-id="9664d-144">タスク管理の概要</span><span class="sxs-lookup"><span data-stu-id="9664d-144">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="9664d-145">タスク管理のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="9664d-145">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="9664d-146">店舗または従業員へのタスク リストの割り当て</span><span class="sxs-lookup"><span data-stu-id="9664d-146">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="9664d-147">POS におけるタスクの管理</span><span class="sxs-lookup"><span data-stu-id="9664d-147">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
