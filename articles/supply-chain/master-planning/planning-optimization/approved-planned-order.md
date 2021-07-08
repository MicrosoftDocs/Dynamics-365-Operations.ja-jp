---
title: 計画オーダーの表示、管理、および承認
description: このトピックでは、計画最適化で計画された注文の表示、管理、および承認を行う方法について説明します。
author: ChristianRytt
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 71ec26bea2063bcf8b6d302a7ece804b3ac934b3
ms.sourcegitcommit: 3673eeca1ada0f3e4ec277176515a946706f8a41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304370"
---
# <a name="view-manage-and-approve-planned-orders"></a><span data-ttu-id="0d5f0-103">計画オーダーの表示、管理、および承認</span><span class="sxs-lookup"><span data-stu-id="0d5f0-103">View, manage, and approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0d5f0-104">このトピックでは、計画最適化で計画された注文の表示、管理、および承認を行う方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-104">This topic provides information about how to view, manage, and approve planned orders in Planning Optimization.</span></span>

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a><span data-ttu-id="0d5f0-105">計画オーダーの表示と管理</span><span class="sxs-lookup"><span data-stu-id="0d5f0-105">View and manage planned orders</span></span>

<span data-ttu-id="0d5f0-106">すべての計画オーダー リスト ページで計画オーダーの表示と管理を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-106">You can view and manage planned orders on any planned orders list page.</span></span> <span data-ttu-id="0d5f0-107">操作する計画オーダーのタイプに応じて、次のいずれかの場所に移動します。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-107">Go to one of the following places, depending on the type of planned orders that you want to work with:</span></span>

- <span data-ttu-id="0d5f0-108">マスター プラン \> ワークスペース \> マスター プラン</span><span class="sxs-lookup"><span data-stu-id="0d5f0-108">Master planning \> Workspaces \> Master planning</span></span>
- <span data-ttu-id="0d5f0-109">マスター プラン \> マスター プラン \> 計画オーダー</span><span class="sxs-lookup"><span data-stu-id="0d5f0-109">Master planning \> Master planning \> Planned orders</span></span>
- <span data-ttu-id="0d5f0-110">生産管理 \> 製造オーダー \> 計画製造オーダー</span><span class="sxs-lookup"><span data-stu-id="0d5f0-110">Production control \> Production orders \> Planned production orders</span></span>
- <span data-ttu-id="0d5f0-111">調達 \> 発注書 \> 計画発注書</span><span class="sxs-lookup"><span data-stu-id="0d5f0-111">Procurement and sourcing \> Purchase orders \> Planned purchase orders</span></span>
- <span data-ttu-id="0d5f0-112">在庫管理 \> 入荷注文 \>> 計画移動</span><span class="sxs-lookup"><span data-stu-id="0d5f0-112">Inventory management \> Inbound orders \> Planned transfers</span></span>
- <span data-ttu-id="0d5f0-113">在庫管理 \> 出荷注文 \>> 計画移動</span><span class="sxs-lookup"><span data-stu-id="0d5f0-113">Inventory management \> Outbound orders \> Planned transfers</span></span>

## <a name="view-and-edit-the-status-of-planned-orders"></a><span data-ttu-id="0d5f0-114">計画オーダーの状態の表示と編集</span><span class="sxs-lookup"><span data-stu-id="0d5f0-114">View and edit the status of planned orders</span></span>

<span data-ttu-id="0d5f0-115">各計画オーダーの **状態** フィールドを使用して、進捗の追跡や計画オーダーの処理方法の変更を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-115">You can use the **Status** field of each planned order to help track your progress or change how a planned order will be processed.</span></span> <span data-ttu-id="0d5f0-116">以下の **状態** の値を使用できます。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-116">The following **Status** values are available:</span></span>

- <span data-ttu-id="0d5f0-117">**未処理** – マスター プランによって計画オーダーが生成されるとき、この状態になります。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-117">**Unprocessed** – When master planning generates planned orders, they are given this status.</span></span> <span data-ttu-id="0d5f0-118">この状態になっている計画オーダーは、次の計画の実行中に削除されます。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-118">Planned orders that have this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="0d5f0-119">**完了** – この状態は、計画オーダーが完了していることをを示します。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-119">**Completed** – This status indicates that the planned order has been completed.</span></span> <span data-ttu-id="0d5f0-120">計画オーダーを確定しない決定をした場合、手動で状態を *完了* に設定できます。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-120">If you decide not to firm a planned order, you can manually change its status to *Completed*.</span></span> <span data-ttu-id="0d5f0-121">*未処理* と *完了* の状態は、システムによって同じように扱われることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-121">Note that the system treats the *Unprocessed* and *Completed* statuses in the same way.</span></span>
- <span data-ttu-id="0d5f0-122">**承認済** – この状態は、計画オーダーの確定を承認していることを示します。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-122">**Approved** – This status indicates that the planned order is approved for firming.</span></span> <span data-ttu-id="0d5f0-123">計画済オーダーを確定する場合は、その状態を *承認済* に変更できます。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-123">If you want to firm a planned order, you can change its status to *Approved*.</span></span> <span data-ttu-id="0d5f0-124">計画オーダーに対して行われた編集を維持する場合、または計画オーダーの確定を予定している場合は、その状態を *承認済* に変更します。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-124">If you want to keep the edits that have been made to a planned order, or if you're planning to firm a planned order, change its status to *Approved*.</span></span> <span data-ttu-id="0d5f0-125">状態が *承認済* である計画オーダーは、マスター プランにより固定され、供給が見込まれているとみなされます。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-125">Planned orders that have a status of *Approved* are considered fixed and expected supply by master planning.</span></span> <span data-ttu-id="0d5f0-126">そのため、後でマスター プランを実行している間、変更または削除はされません。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-126">Therefore, they aren't modified or deleted during later master planning runs.</span></span> <span data-ttu-id="0d5f0-127">この動作を達成するため、計画ロジックは、マスター プラン中に状態が *承認済* である計画オーダーを古い計画バージョンから新しい計画バージョンにコピーします。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-127">To achieve this behavior, the planning logic copies planned orders that have a status of *Approved* from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="0d5f0-128">状態が *承認済* の計画オーダーは、特定のマスター プラン内でのみ供給されると見なされることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-128">Note that planned orders that have a status of *Approved* are considered supply only within the specific master plan.</span></span>

<span data-ttu-id="0d5f0-129">1 つの計画オーダーの状態を変更するには、[計画オーダー リスト ページを開き](#view-planned-orders)、そのオーダーを開いてから、次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-129">To change the status of a single planned order, [open any planned orders list page](#view-planned-orders), open the order, and then follow one of these steps:</span></span>

- <span data-ttu-id="0d5f0-130">**一般** クイックタブで、**状態** フィールドの値を変更します。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-130">On the **General** FastTab, change the value of the **Status** field.</span></span>
- <span data-ttu-id="0d5f0-131">アクション ウィンドウの **計画オーダー** タブにおいて、**処理** グループで **状態の変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-131">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="0d5f0-132">アクション ウィンドウで **承認** を選択して、オーダーを承認済みとしてマークします。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-132">On the Action Pane, select **Approve** to mark the order as approved.</span></span>

<span data-ttu-id="0d5f0-133">複数の計画オーダーの状態を同時に変更するには、[計画オーダー リスト ページを開き](#view-planned-orders)、変更するオーダーのチェックボックスを選択して、次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-133">To change the status of several planned orders at the same time, [open any planned orders list page](#view-planned-orders), select the check box for each order that you want to change, and then follow one of these steps:</span></span>

- <span data-ttu-id="0d5f0-134">アクション ウィンドウの **計画オーダー** タブにおいて、**処理** グループで **状態の変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-134">On the Action Pane, on the **Planned order** tab, in the **Process** group, select **Change status**.</span></span>
- <span data-ttu-id="0d5f0-135">アクション ウィンドウで **承認** を選択して、オーダーを承認済みとしてマークします。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-135">On the Action Pane, select **Approve** to mark the orders as approved.</span></span>

## <a name="approve-planned-orders"></a><span data-ttu-id="0d5f0-136">計画オーダーの承認</span><span class="sxs-lookup"><span data-stu-id="0d5f0-136">Approve planned orders</span></span>

<span data-ttu-id="0d5f0-137">計画オーダーの承認は、計画オーダーから確定された注文を作成するプロセスにおける任意のステップです。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-137">Approval of planned orders is an optional step in the process of creating a firmed order from a planned order.</span></span>

<span data-ttu-id="0d5f0-138">次の図で、各計画オーダーに割り当てられている **状態** の値を使用して承認ワークフローを実装する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-138">The following illustration shows how you can use the **Status** value that is assigned to each planned order to implement an approval workflow.</span></span> <span data-ttu-id="0d5f0-139">承認プロセスを実装するには、前のセクションでの記載に従って、各計画オーダーの **状態** の値を手動で調整します。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-139">To implement an approval process, manually adjust the **Status** value for each planned order as described in the previous section.</span></span>

![計画された注文フロー](media/approved-planned-orders-1.png)

> [!TIP]
> <span data-ttu-id="0d5f0-141">変更された計画オーダーのいずれかを承認することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-141">We recommend that you approve any modified planned orders.</span></span> <span data-ttu-id="0d5f0-142">それ以外の場合は、編集は次の計画の実行により無視され、上書きされます。</span><span class="sxs-lookup"><span data-stu-id="0d5f0-142">Otherwise, the edits will be ignored and overwritten by the next planning run.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0d5f0-143">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0d5f0-143">Additional resources</span></span>

- [<span data-ttu-id="0d5f0-144">計画オーダーの確定</span><span class="sxs-lookup"><span data-stu-id="0d5f0-144">Firm planned orders</span></span>](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
