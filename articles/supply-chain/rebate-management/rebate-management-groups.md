---
title: リベート管理グループ
description: このトピックでは、リベート管理グループの設定方法について説明します。 リベート管理グループは、リベートの計算中に使用し、マスタ レコードに関連付けできます。
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee5a195b3d2881ff70fb1f0d4063ed681e874648
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271080"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="ce965-104">リベート管理グループ</span><span class="sxs-lookup"><span data-stu-id="ce965-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce965-105">リベート管理の計算は、グループ別に行うことができます。</span><span class="sxs-lookup"><span data-stu-id="ce965-105">Rebate management calculations can be driven by groups.</span></span> <span data-ttu-id="ce965-106">リベート管理グループは、顧客、仕入先、および品目に対して作成できます。</span><span class="sxs-lookup"><span data-stu-id="ce965-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="ce965-107">これらは、マスタ レコードに関連付けできます。</span><span class="sxs-lookup"><span data-stu-id="ce965-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="ce965-108">リベート管理の顧客グループ</span><span class="sxs-lookup"><span data-stu-id="ce965-108">Rebate management customer groups</span></span>

<span data-ttu-id="ce965-109">顧客グループの計算は、スーパーマーケット チェーンやフランチャイズ企業などの企業チェーンに対して作成されることが多くあります。</span><span class="sxs-lookup"><span data-stu-id="ce965-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="ce965-110">通常、このタイプの計算はリベートに関連します。</span><span class="sxs-lookup"><span data-stu-id="ce965-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="ce965-111">控除は、対象となる注文の販売先を考慮せずに計算されることがよくあります。</span><span class="sxs-lookup"><span data-stu-id="ce965-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="ce965-112">ただし、例外があります。</span><span class="sxs-lookup"><span data-stu-id="ce965-112">However, there are exceptions.</span></span> <span data-ttu-id="ce965-113">たとえば、ライセンシーは、顧客グループ A が 4% を受け取り、顧客グループ B が 3% のみを受け取る控除スキームを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="ce965-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="ce965-114">顧客グループを設定します</span><span class="sxs-lookup"><span data-stu-id="ce965-114">Set up customer groups</span></span>

<span data-ttu-id="ce965-115">リベート管理顧客グループを使用するには、**リベート管理 \> リベート管理グループ設定 \> 顧客グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ce965-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="ce965-116">アクション ペインのボタンを使用して、必要に応じてグループを追加および削除できます。</span><span class="sxs-lookup"><span data-stu-id="ce965-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="ce965-117">グループごとに、次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="ce965-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="ce965-118">**リベート管理グループ** – グループに固有の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="ce965-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="ce965-119">**説明** – グループの説明を入力して、グループの使用方法に関する詳細情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="ce965-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="ce965-120">顧客グループの割り当ての管理</span><span class="sxs-lookup"><span data-stu-id="ce965-120">Manage customer group assignments</span></span>

<span data-ttu-id="ce965-121">各顧客は、任意の数のリベート管理グループに属することができます。</span><span class="sxs-lookup"><span data-stu-id="ce965-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="ce965-122">グループ メンバーを表示および割り当てるには、グループ リストまたは顧客リストのいずれからでも開始できます。</span><span class="sxs-lookup"><span data-stu-id="ce965-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="ce965-123">選択したグループの顧客を表示、追加、または削除するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ce965-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="ce965-124">**リベート管理 \> リベート管理グループ設定 \> 顧客グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ce965-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="ce965-125">管理するグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-125">Select the group to manage.</span></span>
1. <span data-ttu-id="ce965-126">アクション ペインで、**顧客** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="ce965-127">**リベート管理グループ** ページが表示され、選択したグループのメンバーである顧客リストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ce965-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="ce965-128">グループに新しい顧客を追加するには、アクション ペインで **新規** を選択してグリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="ce965-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="ce965-129">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="ce965-129">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="ce965-130">**顧客アカウント** – 顧客アカウント ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-130">**Customer account** – Select the customer account ID.</span></span>

1. <span data-ttu-id="ce965-131">グループから顧客を削除するには、顧客を選択し、アクション ペインの **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-131">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="ce965-132">選択した顧客のグループの割り当てを表示、追加、または削除するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ce965-132">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="ce965-133">**売掛金勘定 \> 顧客 \> すべての顧客** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ce965-133">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="ce965-134">作業を行う顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-134">Select the customer to work with.</span></span>
1. <span data-ttu-id="ce965-135">アクション ペインの **顧客** タブにある **リベート管理** グループで、**リベート管理グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-135">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="ce965-136">**リベート管理グループ** ページが表示され、選択した顧客がすでに所属しているグループのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ce965-136">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="ce965-137">顧客を新しいグループに追加するには、アクション ペインで **新規** を選択してグリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="ce965-137">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="ce965-138">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="ce965-138">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="ce965-139">**リベート管理グループ** – 顧客を追加するグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-139">**Rebate management group** – Select the group to add the customer to.</span></span>

1. <span data-ttu-id="ce965-140">グループから顧客を削除するには、グループを選択し、アクション ペインの **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-140">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="ce965-141">リベート管理の仕入先グループ</span><span class="sxs-lookup"><span data-stu-id="ce965-141">Rebate management vendor groups</span></span>

<span data-ttu-id="ce965-142">仕入先グループの計算は、多くの場合、納入場所のグループに対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="ce965-142">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="ce965-143">通常、このタイプの計算はリベートに関連します。</span><span class="sxs-lookup"><span data-stu-id="ce965-143">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="ce965-144">仕入先グループの設定</span><span class="sxs-lookup"><span data-stu-id="ce965-144">Set up vendor groups</span></span>

<span data-ttu-id="ce965-145">リベート管理の仕入先グループで作業を行うには、**リベート管理 \> リベート管理グループ設定 \> 仕入先グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ce965-145">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="ce965-146">アクション ペインのボタンを使用して、必要に応じてグループを追加および削除できます。</span><span class="sxs-lookup"><span data-stu-id="ce965-146">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="ce965-147">グループごとに、次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="ce965-147">For each group, set the following fields:</span></span>

- <span data-ttu-id="ce965-148">**リベート管理グループ** – グループに固有の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="ce965-148">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="ce965-149">**説明** – グループの説明を入力して、グループの使用方法に関する詳細情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="ce965-149">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="ce965-150">仕入先グループの割り当ての管理</span><span class="sxs-lookup"><span data-stu-id="ce965-150">Manage vendor group assignments</span></span>

<span data-ttu-id="ce965-151">各仕入先は、任意の数のリベート管理グループに属することができます。</span><span class="sxs-lookup"><span data-stu-id="ce965-151">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="ce965-152">グループ メンバーを表示および割り当てるには、グループ リストまたは仕入先リストのいずれからでも開始できます。</span><span class="sxs-lookup"><span data-stu-id="ce965-152">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="ce965-153">選択したグループの仕入先を表示、追加、または削除するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ce965-153">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="ce965-154">**リベート管理 \> リベート管理グループ設定 \> 仕入先グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ce965-154">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="ce965-155">管理するグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-155">Select the group to manage.</span></span>
1. <span data-ttu-id="ce965-156">アクション ペインで、**仕入先** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-156">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="ce965-157">**リベート管理グループ** ページが表示され、選択したグループのメンバーである仕入先リストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ce965-157">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="ce965-158">新しい仕入先をグループに追加するには、アクション ペインで **新規** を選択してグリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="ce965-158">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="ce965-159">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="ce965-159">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="ce965-160">**仕入先アカウント** – 仕入先アカウント ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-160">**Vendor account** – Select the vendor account ID.</span></span>

1. <span data-ttu-id="ce965-161">グループから仕入先を削除するには、仕入先を選択し、アクション ペインの **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-161">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="ce965-162">選択した仕入先のグループの割り当てを表示、追加、または削除するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ce965-162">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="ce965-163">**買掛金勘定 \> 仕入先 \> すべての仕入先** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ce965-163">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="ce965-164">作業を行う仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-164">Select the vendor to work with.</span></span>
1. <span data-ttu-id="ce965-165">アクション ペインの **仕入先** タブにある **リベート管理** グループで、**リベート管理グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-165">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="ce965-166">**リベート管理グループ** ページが表示され、選択した仕入先がすでに所属しているグループのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ce965-166">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="ce965-167">仕入先を新しいグループに追加するには、アクション ペインで **新規** を選択してグリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="ce965-167">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="ce965-168">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="ce965-168">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="ce965-169">**リベート管理グループ** – 仕入先を追加するグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-169">**Rebate management group** – Select the group to add the vendor to.</span></span>

1. <span data-ttu-id="ce965-170">グループから仕入先を削除するには、グループを選択し、アクション ペインの **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-170">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="ce965-171">品目リベート グループ (複数)</span><span class="sxs-lookup"><span data-stu-id="ce965-171">Item rebate groups</span></span>

<span data-ttu-id="ce965-172">品目をグループ化することで、リベートおよび控除を計算する際の柔軟性が高まります。</span><span class="sxs-lookup"><span data-stu-id="ce965-172">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="ce965-173">この方法は、多くの場合、顧客や仕入先のリベートや控除を設定するためのより効率的な方法です。</span><span class="sxs-lookup"><span data-stu-id="ce965-173">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="ce965-174">品目グループを設定します</span><span class="sxs-lookup"><span data-stu-id="ce965-174">Set up item groups</span></span>

<span data-ttu-id="ce965-175">リベート管理の品目グループで作業を行うには、**リベート管理 \> リベート管理グループ設定 \> 品目グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ce965-175">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="ce965-176">アクション ペインのボタンを使用して、必要に応じてグループを追加および削除できます。</span><span class="sxs-lookup"><span data-stu-id="ce965-176">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="ce965-177">グループごとに、次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="ce965-177">For each group, set the following fields:</span></span>

- <span data-ttu-id="ce965-178">**リベート管理グループ** – グループに固有の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="ce965-178">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="ce965-179">**説明** – グループの説明を入力して、グループの使用方法に関する詳細情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="ce965-179">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="ce965-180">品目グループの割り当ての管理</span><span class="sxs-lookup"><span data-stu-id="ce965-180">Manage item group assignments</span></span>

<span data-ttu-id="ce965-181">各品目は、任意の数のリベート管理グループに属することができます。</span><span class="sxs-lookup"><span data-stu-id="ce965-181">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="ce965-182">グループ メンバーを表示および割り当てるには、グループ リストまたは品目リストのいずれからでも開始できます。</span><span class="sxs-lookup"><span data-stu-id="ce965-182">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="ce965-183">カテゴリ階層に基づいて品目を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="ce965-183">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="ce965-184">選択したグループの品目を表示、追加、または削除するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ce965-184">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="ce965-185">**リベート管理 \> リベート管理グループ設定 \> 品目グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ce965-185">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="ce965-186">管理するグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-186">Select the group to manage.</span></span>
1. <span data-ttu-id="ce965-187">アクション ペインで、**品目** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-187">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="ce965-188">**リベート管理グループ** ページが表示され、選択したグループのメンバーである品目リストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ce965-188">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="ce965-189">新しい品目をグループに追加するには、アクション ペインで **新規** を選択してグリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="ce965-189">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="ce965-190">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="ce965-190">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="ce965-191">**品目アカウント** – 品目アカウント ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-191">**Item account** – Select the item account ID.</span></span>

1. <span data-ttu-id="ce965-192">グループから品目を削除するには、品目を選択し、アクション ペインの **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-192">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="ce965-193">選択した品目のグループの割り当てを表示、追加、または削除するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ce965-193">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="ce965-194">**製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ce965-194">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="ce965-195">作業を行う品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-195">Select the item to work with.</span></span>
1. <span data-ttu-id="ce965-196">アクション ペインの **製品** タブにある **リベート管理** グループで、**リベート管理グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-196">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="ce965-197">**リベート管理グループ** ページが表示され、選択した品目がすでに所属しているグループのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ce965-197">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="ce965-198">品目を新しいグループに追加するには、アクション ペインで **新規** を選択してグリッドに行を追加します。</span><span class="sxs-lookup"><span data-stu-id="ce965-198">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="ce965-199">続いて、新しい行に次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="ce965-199">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="ce965-200">**リベート管理グループ** – 品目を追加するグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-200">**Rebate management group** – Select the group to add the item to.</span></span>

1. <span data-ttu-id="ce965-201">グループから品目を削除するには、グループを選択し、アクション ペインの **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-201">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="ce965-202">カテゴリ階層に基づいてグループに品目を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ce965-202">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="ce965-203">**リベート管理 \> リベート管理グループ設定 \> 品目グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ce965-203">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="ce965-204">管理するグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-204">Select the group to manage.</span></span>
1. <span data-ttu-id="ce965-205">アクション ペインで、**品目の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-205">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="ce965-206">**品目の追加** ダイアログ ボックスの **カテゴリ階層** フィールドで、トップレベルのカテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-206">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="ce965-207">品目階層が左ペインで開きます。</span><span class="sxs-lookup"><span data-stu-id="ce965-207">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="ce965-208">検索する階層レベルを選択します。</span><span class="sxs-lookup"><span data-stu-id="ce965-208">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="ce965-209">選択した階層および階層レベルの品目が右ペインに一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="ce965-209">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="ce965-210">以下のステップに従って、ペインを操作します:</span><span class="sxs-lookup"><span data-stu-id="ce965-210">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="ce965-211">追加する各品目のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="ce965-211">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="ce965-212">一覧表示されている全品目を選択するには、グリッド ヘッダーのチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="ce965-212">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="ce965-213">**選択項目の表示** ボタンを選択して、グリッドをフィルターし、これまでに選択した品目のみが表示されるようにします。</span><span class="sxs-lookup"><span data-stu-id="ce965-213">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="ce965-214">ボタンを再度選択すると、完全なリストに戻ります。</span><span class="sxs-lookup"><span data-stu-id="ce965-214">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="ce965-215">**OK** を選択して、選択したグループに品目選択を適用します。</span><span class="sxs-lookup"><span data-stu-id="ce965-215">Select **OK** to apply your item selection to the selected group.</span></span>
