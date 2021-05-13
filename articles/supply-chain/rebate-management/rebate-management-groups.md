---
title: リベート管理グループ
description: このトピックでは、リベート管理グループの設定方法について説明します。 リベート管理グループは、リベートの計算中に使用し、マスタ レコードに関連付けできます。
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: cef7abbbf2a94e26b6b9e66492cd7347d3b4d1f2
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920064"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="614b0-104">リベート管理グループ</span><span class="sxs-lookup"><span data-stu-id="614b0-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="614b0-105">リベートおよび控除の計算は、グループ別に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="614b0-105">Rebate and deduction calculations can be driven by groups.</span></span> <span data-ttu-id="614b0-106">リベート管理グループは、顧客、仕入先、および品目に対して作成できます。</span><span class="sxs-lookup"><span data-stu-id="614b0-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="614b0-107">これらは、マスタ レコードに関連付けできます。</span><span class="sxs-lookup"><span data-stu-id="614b0-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="614b0-108">リベート管理の顧客グループ</span><span class="sxs-lookup"><span data-stu-id="614b0-108">Rebate management customer groups</span></span>

<span data-ttu-id="614b0-109">顧客グループの計算は、スーパーマーケット チェーンやフランチャイズ企業などの企業チェーンに対して作成されることが多くあります。</span><span class="sxs-lookup"><span data-stu-id="614b0-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="614b0-110">通常、このタイプの計算はリベートに関連します。</span><span class="sxs-lookup"><span data-stu-id="614b0-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="614b0-111">控除は、対象となる注文の販売先を考慮せずに計算されることがよくあります。</span><span class="sxs-lookup"><span data-stu-id="614b0-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="614b0-112">ただし、例外があります。</span><span class="sxs-lookup"><span data-stu-id="614b0-112">However, there are exceptions.</span></span> <span data-ttu-id="614b0-113">たとえば、ライセンシーは、顧客グループ A が 4% を受け取り、顧客グループ B が 3% のみを受け取る控除スキームを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="614b0-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="614b0-114">顧客グループを設定します</span><span class="sxs-lookup"><span data-stu-id="614b0-114">Set up customer groups</span></span>

<span data-ttu-id="614b0-115">リベート管理顧客グループを使用するには、**リベート管理 \> リベート管理グループ設定 \> 顧客グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="614b0-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="614b0-116">アクション ペインのボタンを使用して、必要に応じてグループを追加および削除できます。</span><span class="sxs-lookup"><span data-stu-id="614b0-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="614b0-117">グループごとに、次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="614b0-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="614b0-118">**リベート管理グループ** – グループに固有の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="614b0-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="614b0-119">**説明** – グループの説明を入力して、グループの使用方法に関する詳細情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="614b0-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="614b0-120">顧客グループの割り当ての管理</span><span class="sxs-lookup"><span data-stu-id="614b0-120">Manage customer group assignments</span></span>

<span data-ttu-id="614b0-121">各顧客は、任意の数のリベート管理グループに属することができます。</span><span class="sxs-lookup"><span data-stu-id="614b0-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="614b0-122">グループ メンバーを表示および割り当てるには、グループ リストまたは顧客リストのいずれからでも開始できます。</span><span class="sxs-lookup"><span data-stu-id="614b0-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="614b0-123">選択したグループの顧客を表示、追加、または削除するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="614b0-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="614b0-124">**リベート管理 \> リベート管理グループ設定 \> 顧客グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="614b0-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="614b0-125">管理するグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-125">Select the group to manage.</span></span>
1. <span data-ttu-id="614b0-126">アクション ペインで、**顧客** を選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="614b0-127">**リベート管理グループ** ページが表示され、選択したグループのメンバーである顧客リストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="614b0-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="614b0-128">グループに新しい顧客を追加するには、アクション ペインで **新規** を選択してグリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="614b0-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="614b0-129">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="614b0-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="614b0-130">**顧客アカウント** – 顧客アカウント ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-130">**Customer account** – Select the customer account ID.</span></span>
    - <span data-ttu-id="614b0-131">**名前** – 顧客の名前と説明の両方またはいずれか一方を入力します。</span><span class="sxs-lookup"><span data-stu-id="614b0-131">**Name** – Enter a name and/or description of the customer.</span></span>

1. <span data-ttu-id="614b0-132">グループから顧客を削除するには、顧客を選択し、アクション ペインの **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-132">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="614b0-133">選択した顧客のグループの割り当てを表示、追加、または削除するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="614b0-133">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="614b0-134">**売掛金勘定 \> 顧客 \> すべての顧客** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="614b0-134">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="614b0-135">作業を行う顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-135">Select the customer to work with.</span></span>
1. <span data-ttu-id="614b0-136">アクション ペインの **顧客** タブにある **リベート管理** グループで、**リベート管理グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-136">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="614b0-137">**リベート管理グループ** ページが表示され、選択した顧客がすでに所属しているグループのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="614b0-137">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="614b0-138">顧客を新しいグループに追加するには、アクション ペインで **新規** を選択してグリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="614b0-138">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="614b0-139">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="614b0-139">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="614b0-140">**リベート管理グループ** – 顧客を追加するグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-140">**Rebate management group** – Select the group to add the customer to.</span></span>
    - <span data-ttu-id="614b0-141">**説明** – グループの説明 (たとえば、顧客がそのメンバーである理由など) を入力します。</span><span class="sxs-lookup"><span data-stu-id="614b0-141">**Description** – Enter a description of the group (for example, to explain why the customer is a member of it).</span></span>

1. <span data-ttu-id="614b0-142">グループから顧客を削除するには、グループを選択し、アクション ペインの **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-142">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="614b0-143">リベート管理の仕入先グループ</span><span class="sxs-lookup"><span data-stu-id="614b0-143">Rebate management vendor groups</span></span>

<span data-ttu-id="614b0-144">仕入先グループの計算は、多くの場合、納入場所のグループに対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="614b0-144">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="614b0-145">通常、このタイプの計算はリベートに関連します。</span><span class="sxs-lookup"><span data-stu-id="614b0-145">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="614b0-146">仕入先グループの設定</span><span class="sxs-lookup"><span data-stu-id="614b0-146">Set up vendor groups</span></span>

<span data-ttu-id="614b0-147">リベート管理の仕入先グループで作業を行うには、**リベート管理 \> リベート管理グループ設定 \> 仕入先グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="614b0-147">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="614b0-148">アクション ペインのボタンを使用して、必要に応じてグループを追加および削除できます。</span><span class="sxs-lookup"><span data-stu-id="614b0-148">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="614b0-149">グループごとに、次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="614b0-149">For each group, set the following fields:</span></span>

- <span data-ttu-id="614b0-150">**リベート管理グループ** – グループに固有の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="614b0-150">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="614b0-151">**説明** – グループの説明を入力して、グループの使用方法に関する詳細情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="614b0-151">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="614b0-152">仕入先グループの割り当ての管理</span><span class="sxs-lookup"><span data-stu-id="614b0-152">Manage vendor group assignments</span></span>

<span data-ttu-id="614b0-153">各仕入先は、任意の数のリベート管理グループに属することができます。</span><span class="sxs-lookup"><span data-stu-id="614b0-153">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="614b0-154">グループ メンバーを表示および割り当てるには、グループ リストまたは仕入先リストのいずれからでも開始できます。</span><span class="sxs-lookup"><span data-stu-id="614b0-154">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="614b0-155">選択したグループの仕入先を表示、追加、または削除するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="614b0-155">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="614b0-156">**リベート管理 \> リベート管理グループ設定 \> 仕入先グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="614b0-156">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="614b0-157">管理するグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-157">Select the group to manage.</span></span>
1. <span data-ttu-id="614b0-158">アクション ペインで、**仕入先** を選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-158">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="614b0-159">**リベート管理グループ** ページが表示され、選択したグループのメンバーである仕入先リストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="614b0-159">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="614b0-160">新しい仕入先をグループに追加するには、アクション ペインで **新規** を選択してグリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="614b0-160">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="614b0-161">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="614b0-161">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="614b0-162">**仕入先アカウント** – 仕入先アカウント ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-162">**Vendor account** – Select the vendor account ID.</span></span>
    - <span data-ttu-id="614b0-163">**名前** – 仕入先の名前と説明の両方またはいずれか一方を入力します。</span><span class="sxs-lookup"><span data-stu-id="614b0-163">**Name** – Enter a name and/or description of the vendor.</span></span>

1. <span data-ttu-id="614b0-164">グループから仕入先を削除するには、仕入先を選択し、アクション ペインの **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-164">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="614b0-165">選択した仕入先のグループの割り当てを表示、追加、または削除するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="614b0-165">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="614b0-166">**買掛金勘定 \> 仕入先 \> すべての仕入先** に移動します。</span><span class="sxs-lookup"><span data-stu-id="614b0-166">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="614b0-167">作業を行う仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-167">Select the vendor to work with.</span></span>
1. <span data-ttu-id="614b0-168">アクション ペインの **仕入先** タブにある **リベート管理** グループで、**リベート管理グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-168">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="614b0-169">**リベート管理グループ** ページが表示され、選択した仕入先がすでに所属しているグループのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="614b0-169">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="614b0-170">仕入先を新しいグループに追加するには、アクション ペインで **新規** を選択してグリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="614b0-170">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="614b0-171">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="614b0-171">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="614b0-172">**リベート管理グループ** – 仕入先を追加するグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-172">**Rebate management group** – Select the group to add the vendor to.</span></span>
    - <span data-ttu-id="614b0-173">**説明** – グループの説明 (たとえば、仕入先がそのメンバーである理由など) を入力します。</span><span class="sxs-lookup"><span data-stu-id="614b0-173">**Description** – Enter a description of the group (for example, to explain why the vendor is a member of it).</span></span>

1. <span data-ttu-id="614b0-174">グループから仕入先を削除するには、グループを選択し、アクション ペインの **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-174">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="614b0-175">品目リベート グループ (複数)</span><span class="sxs-lookup"><span data-stu-id="614b0-175">Item rebate groups</span></span>

<span data-ttu-id="614b0-176">品目をグループ化することで、リベートおよび控除を計算する際の柔軟性が高まります。</span><span class="sxs-lookup"><span data-stu-id="614b0-176">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="614b0-177">この方法は、多くの場合、顧客や仕入先のリベートや控除を設定するためのより効率的な方法です。</span><span class="sxs-lookup"><span data-stu-id="614b0-177">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="614b0-178">品目グループを設定します</span><span class="sxs-lookup"><span data-stu-id="614b0-178">Set up item groups</span></span>

<span data-ttu-id="614b0-179">リベート管理の品目グループで作業を行うには、**リベート管理 \> リベート管理グループ設定 \> 品目グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="614b0-179">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="614b0-180">アクション ペインのボタンを使用して、必要に応じてグループを追加および削除できます。</span><span class="sxs-lookup"><span data-stu-id="614b0-180">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="614b0-181">グループごとに、次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="614b0-181">For each group, set the following fields:</span></span>

- <span data-ttu-id="614b0-182">**リベート管理グループ** – グループに固有の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="614b0-182">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="614b0-183">**説明** – グループの説明を入力して、グループの使用方法に関する詳細情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="614b0-183">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="614b0-184">品目グループの割り当ての管理</span><span class="sxs-lookup"><span data-stu-id="614b0-184">Manage item group assignments</span></span>

<span data-ttu-id="614b0-185">各品目は、任意の数のリベート管理グループに属することができます。</span><span class="sxs-lookup"><span data-stu-id="614b0-185">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="614b0-186">グループ メンバーを表示および割り当てるには、グループ リストまたは品目リストのいずれからでも開始できます。</span><span class="sxs-lookup"><span data-stu-id="614b0-186">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="614b0-187">カテゴリ階層に基づいて品目を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="614b0-187">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="614b0-188">選択したグループの品目を表示、追加、または削除するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="614b0-188">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="614b0-189">**リベート管理 \> リベート管理グループ設定 \> 品目グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="614b0-189">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="614b0-190">管理するグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-190">Select the group to manage.</span></span>
1. <span data-ttu-id="614b0-191">アクション ペインで、**品目** を選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-191">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="614b0-192">**リベート管理グループ** ページが表示され、選択したグループのメンバーである品目リストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="614b0-192">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="614b0-193">新しい品目をグループに追加するには、アクション ペインで **新規** を選択してグリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="614b0-193">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="614b0-194">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="614b0-194">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="614b0-195">**品目アカウント** – 品目アカウント ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-195">**Item account** – Select the item account ID.</span></span>
    - <span data-ttu-id="614b0-196">**製品名** – 品目の名前と説明の両方またはいずれか一方を入力します。</span><span class="sxs-lookup"><span data-stu-id="614b0-196">**Product name** – Enter a name and/or description of the item.</span></span>

1. <span data-ttu-id="614b0-197">グループから品目を削除するには、品目を選択し、アクション ペインの **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-197">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="614b0-198">選択した品目のグループの割り当てを表示、追加、または削除するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="614b0-198">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="614b0-199">**製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="614b0-199">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="614b0-200">作業を行う品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-200">Select the item to work with.</span></span>
1. <span data-ttu-id="614b0-201">アクション ペインの **製品** タブにある **リベート管理** グループで、**リベート管理グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-201">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="614b0-202">**リベート管理グループ** ページが表示され、選択した品目がすでに所属しているグループのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="614b0-202">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="614b0-203">品目を新しいグループに追加するには、アクション ペインで **新規** を選択してグリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="614b0-203">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="614b0-204">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="614b0-204">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="614b0-205">**リベート管理グループ** – 品目を追加するグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-205">**Rebate management group** – Select the group to add the item to.</span></span>
    - <span data-ttu-id="614b0-206">**説明** – グループの説明 (たとえば、品目がそのメンバーである理由など) を入力します。</span><span class="sxs-lookup"><span data-stu-id="614b0-206">**Description** – Enter a description of the group (for example, to explain why the item is a member of it).</span></span>

1. <span data-ttu-id="614b0-207">グループから品目を削除するには、グループを選択し、アクション ペインの **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-207">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="614b0-208">カテゴリ階層に基づいてグループに品目を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="614b0-208">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="614b0-209">**リベート管理 \> リベート管理グループ設定 \> 品目グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="614b0-209">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="614b0-210">管理するグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-210">Select the group to manage.</span></span>
1. <span data-ttu-id="614b0-211">アクション ペインで、**品目の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-211">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="614b0-212">**品目の追加** ダイアログ ボックスの **カテゴリ階層** フィールドで、トップレベルのカテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-212">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="614b0-213">品目階層が左ペインで開きます。</span><span class="sxs-lookup"><span data-stu-id="614b0-213">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="614b0-214">検索する階層レベルを選択します。</span><span class="sxs-lookup"><span data-stu-id="614b0-214">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="614b0-215">選択した階層および階層レベルの品目が右ペインに一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="614b0-215">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="614b0-216">以下のステップに従って、ペインを操作します:</span><span class="sxs-lookup"><span data-stu-id="614b0-216">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="614b0-217">追加する各品目のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="614b0-217">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="614b0-218">一覧表示されている全品目を選択するには、グリッド ヘッダーのチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="614b0-218">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="614b0-219">**選択項目の表示** ボタンを選択して、グリッドをフィルターし、これまでに選択した品目のみが表示されるようにします。</span><span class="sxs-lookup"><span data-stu-id="614b0-219">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="614b0-220">ボタンを再度選択すると、完全なリストに戻ります。</span><span class="sxs-lookup"><span data-stu-id="614b0-220">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="614b0-221">**OK** を選択して、選択したグループに品目選択を適用します。</span><span class="sxs-lookup"><span data-stu-id="614b0-221">Select **OK** to apply your item selection to the selected group.</span></span>
