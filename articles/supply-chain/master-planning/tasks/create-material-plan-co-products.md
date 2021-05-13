---
title: 連産品の材料計画の作成
description: 生産計画担当者は、フォーミュラ連産品である品目の材料要求を計画します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b51e4b4d00da2babb5128d8c4c22139b0c1853d4
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920732"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="7d61d-103">連産品の材料計画の作成</span><span class="sxs-lookup"><span data-stu-id="7d61d-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7d61d-104">生産計画担当者は、フォーミュラ連産品である品目の材料要求を計画します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="7d61d-105">この手順の作成に使用するデモ データの会社は USP2 です。</span><span class="sxs-lookup"><span data-stu-id="7d61d-105">The demo data company used to create this procedure is USP2.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="7d61d-106">連産品要求の作成</span><span class="sxs-lookup"><span data-stu-id="7d61d-106">Create requirement for a co-product</span></span>

1. <span data-ttu-id="7d61d-107">**販売とマーケティング\>ワークスペース\>販売注文の処理と照会** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d61d-107">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="7d61d-108">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-108">Select **New**.</span></span>
1. <span data-ttu-id="7d61d-109">**販売注文** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-109">Select **Sales order**.</span></span>
1. <span data-ttu-id="7d61d-110">**顧客口座** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-110">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="7d61d-111">例: US-001</span><span class="sxs-lookup"><span data-stu-id="7d61d-111">Example: US-001</span></span>  
1. <span data-ttu-id="7d61d-112">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-112">Select **OK**.</span></span>
1. <span data-ttu-id="7d61d-113">**品目番号** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-113">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="7d61d-114">例: P6003</span><span class="sxs-lookup"><span data-stu-id="7d61d-114">Example: P6003</span></span>  
1. <span data-ttu-id="7d61d-115">**数量** フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-115">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="7d61d-116">例: 50000</span><span class="sxs-lookup"><span data-stu-id="7d61d-116">Example: 50000</span></span>  
1. <span data-ttu-id="7d61d-117">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-117">Select **Save**.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="7d61d-118">連産品の材料計画の作成</span><span class="sxs-lookup"><span data-stu-id="7d61d-118">Create a material plan for co-products</span></span>

1. <span data-ttu-id="7d61d-119">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7d61d-119">Close the page.</span></span>
1. <span data-ttu-id="7d61d-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7d61d-120">Close the page.</span></span>
1. <span data-ttu-id="7d61d-121">**マスター プラン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-121">Select **Master planning**.</span></span>
1. <span data-ttu-id="7d61d-122">**計画** フィールドで、ドロップ ダウン ボタンを選択し、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="7d61d-122">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
1. <span data-ttu-id="7d61d-123">一覧で、選択した行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-123">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="7d61d-124">例: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="7d61d-124">Example: MasterPlan</span></span>  
1. <span data-ttu-id="7d61d-125">**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-125">Select **Run**.</span></span>
1. <span data-ttu-id="7d61d-126">**対象に含めるレコード** セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="7d61d-126">Expand or collapse the **Records to include** section.</span></span>
1. <span data-ttu-id="7d61d-127">**フィルター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-127">Select **Filter**.</span></span>
1. <span data-ttu-id="7d61d-128">一覧で、**フィールド** = *品目番号* の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-128">In the list, select the row for **Field** = *Item number*.</span></span>
1. <span data-ttu-id="7d61d-129">**基準** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-129">In the **Criteria** field, type a value.</span></span>
    * <span data-ttu-id="7d61d-130">例: P6003</span><span class="sxs-lookup"><span data-stu-id="7d61d-130">Example: P6003</span></span>  
1. <span data-ttu-id="7d61d-131">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-131">Select **OK**.</span></span>
1. <span data-ttu-id="7d61d-132">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-132">Select **OK**.</span></span>
1. <span data-ttu-id="7d61d-133">**計画オーダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-133">Select **Planned orders**.</span></span>
1. <span data-ttu-id="7d61d-134">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="7d61d-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="7d61d-135">たとえば、「P6000」 という値を含む **品目番号** フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-135">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="7d61d-136">販売注文を作成した品目の連産品としてのフォーミュラ品目でフィルター抽出します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-136">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
1. <span data-ttu-id="7d61d-137">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="7d61d-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7d61d-138">フィルターによって返された行を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-138">Select any of the rows returned by the filter.</span></span>  
1. <span data-ttu-id="7d61d-139">一覧で、選択した行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-139">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="7d61d-140">**ペギング** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-140">Expand the **Pegging** section.</span></span>
1. <span data-ttu-id="7d61d-141">一覧で、選択した行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-141">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="7d61d-142">計画オーダーは、連産品の販売注文にペギングされます。</span><span class="sxs-lookup"><span data-stu-id="7d61d-142">The planned order is pegged to the sales order for the co-product.</span></span>  
1. <span data-ttu-id="7d61d-143">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7d61d-143">Close the page.</span></span>

## <a name="create-a-second-requirement-for-a-co-product"></a><span data-ttu-id="7d61d-144">連産品の第 2 要求の作成</span><span class="sxs-lookup"><span data-stu-id="7d61d-144">Create a second requirement for a co-product</span></span>

1. <span data-ttu-id="7d61d-145">**販売とマーケティング\>ワークスペース\>販売注文の処理と照会** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="7d61d-145">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="7d61d-146">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-146">Select **New**.</span></span>
1. <span data-ttu-id="7d61d-147">**販売注文** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-147">Select **Sales order**.</span></span>
1. <span data-ttu-id="7d61d-148">**顧客口座** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-148">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="7d61d-149">例: US-001</span><span class="sxs-lookup"><span data-stu-id="7d61d-149">Example: US-001</span></span>  
1. <span data-ttu-id="7d61d-150">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-150">Select **OK**.</span></span>
1. <span data-ttu-id="7d61d-151">**品目番号** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-151">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="7d61d-152">例: P6003</span><span class="sxs-lookup"><span data-stu-id="7d61d-152">Example: P6003</span></span>  
1. <span data-ttu-id="7d61d-153">**数量** フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-153">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="7d61d-154">例: 50000</span><span class="sxs-lookup"><span data-stu-id="7d61d-154">Example: 50000</span></span>  
1. <span data-ttu-id="7d61d-155">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-155">Select **Save**.</span></span>

## <a name="create-a-second-material-plan-for-co-products"></a><span data-ttu-id="7d61d-156">連産品の第 2 材料計画の作成</span><span class="sxs-lookup"><span data-stu-id="7d61d-156">Create a second material plan for co-products</span></span>

1. <span data-ttu-id="7d61d-157">**計画** フィールドで、ドロップ ダウン ボタンを選択し、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="7d61d-157">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="7d61d-158">一覧で、選択した行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-158">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="7d61d-159">例: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="7d61d-159">Example: MasterPlan</span></span>  
3. <span data-ttu-id="7d61d-160">**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-160">Select **Run**.</span></span>
4. <span data-ttu-id="7d61d-161">**対象に含めるレコード** セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="7d61d-161">Expand or collapse the **Records to include** section.</span></span>
5. <span data-ttu-id="7d61d-162">**フィルター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-162">Select **Filter**.</span></span>
6. <span data-ttu-id="7d61d-163">一覧で、**フィールド** = *品目番号* の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-163">In the list, select the row for **Field** = *Item number*.</span></span>
7. <span data-ttu-id="7d61d-164">*基準* フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-164">In the *Criteria* field, type a value.</span></span>
    * <span data-ttu-id="7d61d-165">例: P6003</span><span class="sxs-lookup"><span data-stu-id="7d61d-165">Example: P6003</span></span>  
8. <span data-ttu-id="7d61d-166">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-166">Select **OK**.</span></span>
9. <span data-ttu-id="7d61d-167">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-167">Select **OK**.</span></span>
10. <span data-ttu-id="7d61d-168">**計画オーダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-168">Select **Planned orders**.</span></span>
11. <span data-ttu-id="7d61d-169">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="7d61d-169">Use the Quick Filter to find records.</span></span> <span data-ttu-id="7d61d-170">たとえば、「P6000」 という値を含む **品目番号** フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-170">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="7d61d-171">販売注文を作成した品目の連産品としてのフォーミュラ品目でフィルター抽出します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-171">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="7d61d-172">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="7d61d-172">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7d61d-173">フィルターによって返された行を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-173">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="7d61d-174">一覧で、選択した行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-174">In the list, select the link in the selected row.</span></span>
14. <span data-ttu-id="7d61d-175">**ペギング** セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="7d61d-175">Expand or collapse the **Pegging** section.</span></span>
15. <span data-ttu-id="7d61d-176">一覧で、選択した行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-176">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="7d61d-177">計画オーダーは、連産品の販売注文にペギングされます。</span><span class="sxs-lookup"><span data-stu-id="7d61d-177">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="7d61d-178">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7d61d-178">Close the page.</span></span>
17. <span data-ttu-id="7d61d-179">**マスター プラン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-179">Select **Master planning**.</span></span>
18. <span data-ttu-id="7d61d-180">**マスター プラン \> 設定 \> マスター プランのパラメータ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-180">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
19. <span data-ttu-id="7d61d-181">**すべての計画プロセスの無効化** フィールドで、*いいえ* を選択します。</span><span class="sxs-lookup"><span data-stu-id="7d61d-181">Select *No* in the **Disable all planning processes** field.</span></span>
20. <span data-ttu-id="7d61d-182">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="7d61d-182">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]