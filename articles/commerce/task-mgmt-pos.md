---
title: POS におけるタスクの管理
description: このトピックでは、Microsoft Dynamics 365 Commerce 販売時点管理 (POS) アプリケーションにおけるタスク管理について説明します。
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: cc685fcd584fe2ab5cd9282e8fbefbd284d5b2a2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413815"
---
# <a name="task-management-in-pos"></a><span data-ttu-id="5fbae-103">POS におけるタスクの管理</span><span class="sxs-lookup"><span data-stu-id="5fbae-103">Task management in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5fbae-104">このトピックでは、Microsoft Dynamics 365 Commerce 販売時点管理 (POS) アプリケーションにおけるタスク管理について説明します。</span><span class="sxs-lookup"><span data-stu-id="5fbae-104">This topic describes task management in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

## <a name="overview"></a><span data-ttu-id="5fbae-105">概要</span><span class="sxs-lookup"><span data-stu-id="5fbae-105">Overview</span></span>

<span data-ttu-id="5fbae-106">Dynamics 365 Commerce POS アプリケーションにはタスク管理機能があり、店舗の管理者および作業者がタスクを管理したり、タスクの状態を更新したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="5fbae-106">The Dynamics 365 Commerce POS application has task management features that let store managers and workers manage tasks and update task status.</span></span> <span data-ttu-id="5fbae-107">店舗の作業者は、POS ホームページの **タスク** タイルを選択するか、またはタスクの通知を選択することにより、タスクにアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="5fbae-107">Store workers can access tasks either by selecting the **Tasks** tile on the POS home page or by selecting task notifications.</span></span> <span data-ttu-id="5fbae-108">既定では、店舗の作業者は **自分のタスク** タブに移動し、割り当てられているタスクを確認できます。</span><span class="sxs-lookup"><span data-stu-id="5fbae-108">By default, store workers are taken to the **My tasks** tab, where they can view the tasks that are assigned to them.</span></span> <span data-ttu-id="5fbae-109">ただし、**期限超過のタスク**、**タスクを開く**、および **タスク リスト** タブに簡単に切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="5fbae-109">However, they can easily switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs.</span></span>

## <a name="task-operations-for-store-managers"></a><span data-ttu-id="5fbae-110">店舗マネージャーのタスク操作</span><span class="sxs-lookup"><span data-stu-id="5fbae-110">Task operations for store managers</span></span>

<span data-ttu-id="5fbae-111">店舗のマネージャーは、コマンド バーのボタンを使用して、POS アプリケーションで次のタスク操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="5fbae-111">Store managers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="5fbae-112">**割り当て** – 選択したタスクを店舗の作業者に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="5fbae-112">**Assign** – Assign selected tasks to a store worker.</span></span>
- <span data-ttu-id="5fbae-113">**タスクの状態** – 選択したタスクの状態を変更します。</span><span class="sxs-lookup"><span data-stu-id="5fbae-113">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="5fbae-114">**フィルター** – 既定では、有効なタスクのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5fbae-114">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="5fbae-115">ただし、フィルターを適用することにより、マネージャーは完了またはキャンセルしたタスクを含め、すべてのタスクを表示できます。</span><span class="sxs-lookup"><span data-stu-id="5fbae-115">However, by applying filters, managers can view all tasks, even tasks that have been completed or canceled.</span></span>
- <span data-ttu-id="5fbae-116">**新しいタスク** – 既存のタスク リストの下にタスクを作成するか、または単一目的のタスクを作成します。</span><span class="sxs-lookup"><span data-stu-id="5fbae-116">**New task** – Create a task under an existing task list, or create an single-purpose task.</span></span>

<span data-ttu-id="5fbae-117">店舗の作業者は、コマンド バーのボタンを使用して、POS アプリケーションで次のタスク操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="5fbae-117">Store workers can perform the following task operations in the POS application by using the buttons on the command bar:</span></span>

- <span data-ttu-id="5fbae-118">**タスクの状態** – 選択したタスクの状態を変更します。</span><span class="sxs-lookup"><span data-stu-id="5fbae-118">**Task status** – Change the status of selected tasks.</span></span>
- <span data-ttu-id="5fbae-119">**フィルター** – 既定では、有効なタスクのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5fbae-119">**Filter** – By default, only active tasks are shown.</span></span> <span data-ttu-id="5fbae-120">ただし、フィルターを適用することにより、作業者は完了またはキャンセルしたタスクを含め、すべてのタスクを表示できます。</span><span class="sxs-lookup"><span data-stu-id="5fbae-120">However, by applying filters, workers can view all tasks, even tasks that have been completed or canceled.</span></span>

<span data-ttu-id="5fbae-121">次の図は、Commerce POS アプリケーションの **自分のタスク** タブを示しています。</span><span class="sxs-lookup"><span data-stu-id="5fbae-121">The following illustration shows the **My tasks** tab in the Commerce POS application.</span></span>

![Commerce POS アプリケーションの自分のタスク タブ](media/POS-task-management.png)

<span data-ttu-id="5fbae-123">次の図は、**タスク リスト** タブを示しています。</span><span class="sxs-lookup"><span data-stu-id="5fbae-123">The following illustration shows the **Task lists** tab.</span></span>

![Commerce POS アプリケーションのタスク リスト タブ](media/POS-task-lists-management.png)

## <a name="additional-resources"></a><span data-ttu-id="5fbae-125">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5fbae-125">Additional resources</span></span>

[<span data-ttu-id="5fbae-126">タスク管理の概要</span><span class="sxs-lookup"><span data-stu-id="5fbae-126">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="5fbae-127">タスク管理のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5fbae-127">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="5fbae-128">タスク リストの作成およびタスクの追加</span><span class="sxs-lookup"><span data-stu-id="5fbae-128">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="5fbae-129">店舗または従業員へのタスク リストの割り当て</span><span class="sxs-lookup"><span data-stu-id="5fbae-129">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)
