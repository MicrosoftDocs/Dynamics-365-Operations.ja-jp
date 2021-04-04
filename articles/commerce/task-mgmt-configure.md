---
title: タスク管理のコンフィギュレーション
description: このトピックでは、Microsoft Dynamics 365 Commerce においてタスク管理機能をコンフィギュレーションする方法について説明します。
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
ms.openlocfilehash: ba2283bbfa2fdce75d3fbef6fcff47dd872c7998
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478047"
---
# <a name="configure-task-management"></a><span data-ttu-id="6e446-103">タスク管理のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6e446-103">Configure task management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6e446-104">このトピックでは、Microsoft Dynamics 365 Commerce においてタスク管理機能をコンフィギュレーションする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6e446-104">This topic describes how to configure task management features in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6e446-105">Dynamics 365 Commerce のマネージャーおよび従業員が Commerce のタスク管理機能を使用できるようにする前に、タスク管理をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e446-105">Before Dynamics 365 Commerce managers and employees can use the task management features in Commerce, task management must be configured.</span></span> <span data-ttu-id="6e446-106">コンフィギュレーションの手順には、マネージャーおよび従業員へのアクセス許可の付与、販売時点管理 (POS) クライアントへのアクセス許可の配分、POS 通知の設定、および POS アプリケーションのホーム ページでの **タスク** タイルのコンフィギュレーションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6e446-106">Configuration steps include granting permissions to managers and employees, distributing permissions to point of sale (POS) clients, setting up POS notifications, and configuring the **Tasks** tile on the home page of a POS application.</span></span>

## <a name="configure-permissions-for-store-managers"></a><span data-ttu-id="6e446-107">店舗マネージャーのアクセス許可のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6e446-107">Configure permissions for store managers</span></span>

<span data-ttu-id="6e446-108">指定された店舗の作業者はすべて、店舗に割り当てられているすべてのタスクを表示できます。</span><span class="sxs-lookup"><span data-stu-id="6e446-108">Every worker in a given store can view all tasks that are assigned to that store.</span></span> <span data-ttu-id="6e446-109">また、割り当てられているタスクの状態を更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="6e446-109">They can also update the status of the tasks that are assigned to them.</span></span> <span data-ttu-id="6e446-110">ただし、店舗のマネージャーなどのペルソナは、店舗に割り当てられているタスクを管理したり、単一目的のタスクを作成したりするするには、タスク管理のアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="6e446-110">However, personas such as store managers must have task management permissions to manage tasks that are assigned to the store and to create single-purpose tasks.</span></span>

<span data-ttu-id="6e446-111">店舗のマネージャーに対してタスク管理のアクセス許可をコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6e446-111">To configure task management permissions for store managers, follow these steps.</span></span>

1. <span data-ttu-id="6e446-112">**Retail と Commerce \> 従業員 \> アクセス許可グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6e446-112">Go to **Retail and Commerce \> Employees \> Permission groups**.</span></span>
1. <span data-ttu-id="6e446-113">特定のアクセス許可グループ (たとえば、**マネージャー** など) を選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e446-113">Select a specific permission group (for example, **Manager**), and then select **Edit**.</span></span>
1. <span data-ttu-id="6e446-114">**アクセス許可** クイック タブで、**タスク管理を許可** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="6e446-114">On the **Permissions** FastTab, set the **Allow task management** option to **Yes**.</span></span>
1. <span data-ttu-id="6e446-115">**通知** クイック タブで **タスク管理** 操作を追加し、**表示順序** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6e446-115">On the **Notifications** FastTab, add the **Task management** operation, and enter a value in the **Display order** field.</span></span> <span data-ttu-id="6e446-116">たとえば、**注文のフルフィルメント** 操作の **表示順序** がすでに **1** である場合、**2** を入力します。</span><span class="sxs-lookup"><span data-stu-id="6e446-116">For example, enter **2** if the **Order fulfillment** operation already has a **Display order** value of **1**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="6e446-117">マネージャー以外のペルソナに POS におけるタスク管理のアクセス許可がある場合、個々のユーザーにアクセス許可を付与できます。</span><span class="sxs-lookup"><span data-stu-id="6e446-117">If a non-manager persona must have task management permissions in the POS, you can grant permission to the individual.</span></span> <span data-ttu-id="6e446-118">または、マネージャー以外に対してアクセス許可グループを作成し、**タスク管理を許可** オプションを **はい** に設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="6e446-118">Alternatively, you can create a new permission group for non-managers and set the **Allow task management** option to **Yes**.</span></span>

<span data-ttu-id="6e446-119">次の図は、店舗のマネージャーに対してタスク管理のアクセス許可をコンフィギュレーションする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="6e446-119">The following illustration shows how to configure task management permissions for store managers.</span></span>

![店舗のマネージャーに対するタスク管理のアクセス許可のコンフィギュレーション](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a><span data-ttu-id="6e446-121">従業員のアクセス許可のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6e446-121">Configure permissions for employees</span></span>

<span data-ttu-id="6e446-122">従業員がタスク リストの作成、割り当て基準の管理、および定期的なアイテムのタスク リストのコンフィギュレーションを行うには、アクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="6e446-122">Employees must have permissions to create task lists, manage assignment criteria, and configure the recurrence of any task list.</span></span> <span data-ttu-id="6e446-123">これらのアクセス許可をコンフィギュレーションするには、従業員を **Retail タスク マネージャー** ロールに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="6e446-123">To configure these permissions, you assign employees to the **Retail task manager** role.</span></span>

<span data-ttu-id="6e446-124">従業員に対してアクセス許可をコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6e446-124">To configure permissions for an employee, follow these steps.</span></span>

1. <span data-ttu-id="6e446-125">**Retail と Commerce \> 従業員 \> ユーザー** へ移動します。</span><span class="sxs-lookup"><span data-stu-id="6e446-125">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="6e446-126">従業員を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e446-126">Select an employee.</span></span>
1. <span data-ttu-id="6e446-127">**ユーザーのロール** クイック タブで、**ロールの割り当て** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6e446-127">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="6e446-128">**ユーザーへのロールの割り当て** ダイアログ ボックスで **Retail タスク マネージャー** ロールを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e446-128">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

## <a name="distribute-permissions-to-pos-clients"></a><span data-ttu-id="6e446-129">POS クライアントへのアクセス許可の配分</span><span class="sxs-lookup"><span data-stu-id="6e446-129">Distribute permissions to POS clients</span></span>

<span data-ttu-id="6e446-130">従業員が POS クライアントを使用できるようにする前に、それらのクライアントにアクセス許可を配分し、同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e446-130">Before employees can use POS clients, permissions must be distributed and synced to those clients.</span></span>

<span data-ttu-id="6e446-131">POS クライアントにアクセス許可を配分するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6e446-131">To distribute permissions to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="6e446-132">**Retail とコマース \> Retail とコマース IT \> 配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6e446-132">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="6e446-133">**1060** (**スタッフ**) 配分スケジュールを選択し、**今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e446-133">Select the **1060** (**Staff**) distribution schedule, and then select **Run now**.</span></span>
1. <span data-ttu-id="6e446-134">**1070** (**チャンルのコンフィギュレーション**) 配分スケジュールを選択し、**今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e446-134">Select the **1070** (**Channel configuration**) distribution schedule, and then select **Run now**.</span></span>

## <a name="configure-pos-notifications-for-tasks"></a><span data-ttu-id="6e446-135">タスクの POS 通知のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6e446-135">Configure POS notifications for tasks</span></span>

<span data-ttu-id="6e446-136">POS アプリケーションで通知を使用可能にするには、タスク管理をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6e446-136">Task management must be configured so that notifications are available in the POS application.</span></span>

<span data-ttu-id="6e446-137">タスクに対して POS 通知をコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6e446-137">To configure POS notifications for tasks, follow these steps.</span></span>

1. <span data-ttu-id="6e446-138">**Retail および Commerce \> チャネル設定 \> POS 設定 \> POS \> POS 操作** に移動します。</span><span class="sxs-lookup"><span data-stu-id="6e446-138">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="6e446-139">**1400** (**タスク管理**) 操作を検索し、**通知の有効化** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="6e446-139">Find operation **1400** (**Task management**), and select the **Enable notifications** check box for it.</span></span>

<span data-ttu-id="6e446-140">次の図は、**POS 操作** ページの **タスク管理** 操作を示しています。</span><span class="sxs-lookup"><span data-stu-id="6e446-140">The following illustration shows the **Task management** operation on the **POS operations** page.</span></span>

![POS 操作ページのタスク管理操作](media/HQ-POS-Tasks-Notifications.png)

<span data-ttu-id="6e446-142">POS 通知をコンフィギュレーションする方法の詳細については、[販売時点管理 (POS) の注文通知の表示](notifications-pos.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6e446-142">For more information about how to configure POS notifications, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a><span data-ttu-id="6e446-143">POS アプリケーションのホーム ページのタスク タイルのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6e446-143">Configure the Tasks tile on a POS application home page</span></span>

<span data-ttu-id="6e446-144">POS アプリケーションのホーム ページの **タスク** タイルをコンフィギュレーションする前に、POS 画面レイアウトへ新しいボタンのコンフィギュレーションおよび追加を行う方法の詳細について、[販売時点管理 (POS) の画面レイアウト](pos-screen-layouts.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6e446-144">Before you configure the **Tasks** tile on the home page of a POS application, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information about how to configure and add new buttons to a POS screen layout.</span></span>

<span data-ttu-id="6e446-145">POS アプリケーションのホーム ページの **タスク** タイルをコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6e446-145">To configure the **Tasks** tile on a POS application home page, follow these steps.</span></span>

1. <span data-ttu-id="6e446-146">**Retail とコマース \> チャネル設定 \> POS 設定 \> POS \> 画面レイアウト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6e446-146">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> Screen layouts**.</span></span>
1. <span data-ttu-id="6e446-147">画面レイアウトを選択し、レイアウト サイズを選択して、ボタン グリッドを選択します。</span><span class="sxs-lookup"><span data-stu-id="6e446-147">Select a screen layout, select a layout size, and select a button grid.</span></span>
1. <span data-ttu-id="6e446-148">**ボタン グリッド** クイック タブで、**デザイナー** を選択して、選択したボタン グリッドを編集します。</span><span class="sxs-lookup"><span data-stu-id="6e446-148">On the **Button grids** FastTab, select **Designer** to edit the selected button grid.</span></span>
1. <span data-ttu-id="6e446-149">ホーム ページの適切なセクションに **タスク** タイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="6e446-149">Add a **Tasks** tile to the appropriate section of the home page.</span></span>

<span data-ttu-id="6e446-150">次の図は、POS ホーム ページの **タスク** タイルの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="6e446-150">The following illustration shows an example of a **Tasks** tile on a POS home page.</span></span>

![POS ホーム ページのタスク タイル](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a><span data-ttu-id="6e446-152">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6e446-152">Additional resources</span></span>

[<span data-ttu-id="6e446-153">タスク管理の概要</span><span class="sxs-lookup"><span data-stu-id="6e446-153">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="6e446-154">タスク リストの作成およびタスクの追加</span><span class="sxs-lookup"><span data-stu-id="6e446-154">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="6e446-155">店舗または従業員へのタスク リストの割り当て</span><span class="sxs-lookup"><span data-stu-id="6e446-155">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="6e446-156">POS におけるタスクの管理</span><span class="sxs-lookup"><span data-stu-id="6e446-156">Task management in POS</span></span>](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
