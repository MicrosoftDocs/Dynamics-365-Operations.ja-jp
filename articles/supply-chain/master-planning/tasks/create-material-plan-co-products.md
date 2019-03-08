---
title: 連産品の材料計画の作成
description: 生産計画担当者は、フォーミュラ連産品である品目の材料要求を計画します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2958f1e5c2e8a0cfa9cc6312f688d3b11b8e013c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "337144"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="3e938-103">連産品の材料計画の作成</span><span class="sxs-lookup"><span data-stu-id="3e938-103">Create a material plan for co products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3e938-104">生産計画担当者は、フォーミュラ連産品である品目の材料要求を計画します。</span><span class="sxs-lookup"><span data-stu-id="3e938-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="3e938-105">この手順の作成に使用するデモ データの会社は USP2 です。</span><span class="sxs-lookup"><span data-stu-id="3e938-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="3e938-106">連産品要求の作成</span><span class="sxs-lookup"><span data-stu-id="3e938-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="3e938-107">[既定のダッシュボード] に移動します。</span><span class="sxs-lookup"><span data-stu-id="3e938-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="3e938-108">[販売注文の処理と照会] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="3e938-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-109">Click New.</span></span>
4. <span data-ttu-id="3e938-110">[販売注文] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-110">Click Sales order.</span></span>
5. <span data-ttu-id="3e938-111">[顧客口座] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3e938-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="3e938-112">例: US-001</span><span class="sxs-lookup"><span data-stu-id="3e938-112">Example: US-001</span></span>  
6. <span data-ttu-id="3e938-113">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-113">Click OK.</span></span>
7. <span data-ttu-id="3e938-114">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3e938-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="3e938-115">例: P6003</span><span class="sxs-lookup"><span data-stu-id="3e938-115">Example: P6003</span></span>  
8. <span data-ttu-id="3e938-116">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3e938-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="3e938-117">例: 50000</span><span class="sxs-lookup"><span data-stu-id="3e938-117">Example: 50000</span></span>  
9. <span data-ttu-id="3e938-118">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="3e938-119">連産品の材料計画の作成</span><span class="sxs-lookup"><span data-stu-id="3e938-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="3e938-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3e938-120">Close the page.</span></span>
2. <span data-ttu-id="3e938-121">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3e938-121">Close the page.</span></span>
3. <span data-ttu-id="3e938-122">[マスター プラン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-122">Click Master planning.</span></span>
4. <span data-ttu-id="3e938-123">[計画] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="3e938-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="3e938-124">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3e938-125">例: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="3e938-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="3e938-126">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-126">Click Run.</span></span>
7. <span data-ttu-id="3e938-127">[対象に含めるレコード] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="3e938-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="3e938-128">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-128">Click Filter.</span></span>
9. <span data-ttu-id="3e938-129">リストで、フィールド = 品目番号の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="3e938-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="3e938-130">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3e938-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="3e938-131">例: P6003</span><span class="sxs-lookup"><span data-stu-id="3e938-131">Example: P6003</span></span>  
11. <span data-ttu-id="3e938-132">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-132">Click OK.</span></span>
12. <span data-ttu-id="3e938-133">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-133">Click OK.</span></span>
13. <span data-ttu-id="3e938-134">[計画オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-134">Click Planned orders.</span></span>
14. <span data-ttu-id="3e938-135">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="3e938-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="3e938-136">たとえば、「P6000」という値を含む [品目番号] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="3e938-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="3e938-137">販売注文を作成した品目の連産品としてのフォーミュラ品目でフィルター抽出します。</span><span class="sxs-lookup"><span data-stu-id="3e938-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="3e938-138">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="3e938-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="3e938-139">フィルターによって返された行を選択します。</span><span class="sxs-lookup"><span data-stu-id="3e938-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="3e938-140">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="3e938-141">[ペギング] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="3e938-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="3e938-142">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3e938-143">計画オーダーは、連産品の販売注文にペギングされます。</span><span class="sxs-lookup"><span data-stu-id="3e938-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="3e938-144">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3e938-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="3e938-145">連産品要求の作成</span><span class="sxs-lookup"><span data-stu-id="3e938-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="3e938-146">[既定のダッシュボード] に移動します。</span><span class="sxs-lookup"><span data-stu-id="3e938-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="3e938-147">[販売注文の処理と照会] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="3e938-148">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-148">Click New.</span></span>
4. <span data-ttu-id="3e938-149">[販売注文] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-149">Click Sales order.</span></span>
5. <span data-ttu-id="3e938-150">[顧客口座] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3e938-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="3e938-151">例: US-001</span><span class="sxs-lookup"><span data-stu-id="3e938-151">Example: US-001</span></span>  
6. <span data-ttu-id="3e938-152">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-152">Click OK.</span></span>
7. <span data-ttu-id="3e938-153">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3e938-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="3e938-154">例: P6003</span><span class="sxs-lookup"><span data-stu-id="3e938-154">Example: P6003</span></span>  
8. <span data-ttu-id="3e938-155">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3e938-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="3e938-156">例: 50000</span><span class="sxs-lookup"><span data-stu-id="3e938-156">Example: 50000</span></span>  
9. <span data-ttu-id="3e938-157">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="3e938-158">連産品の材料計画の作成</span><span class="sxs-lookup"><span data-stu-id="3e938-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="3e938-159">[計画] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="3e938-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="3e938-160">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3e938-161">例: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="3e938-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="3e938-162">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-162">Click Run.</span></span>
4. <span data-ttu-id="3e938-163">[対象に含めるレコード] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="3e938-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="3e938-164">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-164">Click Filter.</span></span>
6. <span data-ttu-id="3e938-165">リストで、フィールド = 品目番号の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="3e938-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="3e938-166">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3e938-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="3e938-167">例: P6003</span><span class="sxs-lookup"><span data-stu-id="3e938-167">Example: P6003</span></span>  
8. <span data-ttu-id="3e938-168">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-168">Click OK.</span></span>
9. <span data-ttu-id="3e938-169">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-169">Click OK.</span></span>
10. <span data-ttu-id="3e938-170">[計画オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-170">Click Planned orders.</span></span>
11. <span data-ttu-id="3e938-171">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="3e938-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="3e938-172">たとえば、「P6000」という値を含む [品目番号] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="3e938-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="3e938-173">販売注文を作成した品目の連産品としてのフォーミュラ品目でフィルター抽出します。</span><span class="sxs-lookup"><span data-stu-id="3e938-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="3e938-174">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="3e938-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="3e938-175">フィルターによって返された行を選択します。</span><span class="sxs-lookup"><span data-stu-id="3e938-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="3e938-176">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="3e938-177">[ペギング] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="3e938-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="3e938-178">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3e938-179">計画オーダーは、連産品の販売注文にペギングされます。</span><span class="sxs-lookup"><span data-stu-id="3e938-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="3e938-180">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3e938-180">Close the page.</span></span>
17. <span data-ttu-id="3e938-181">[マスター プラン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e938-181">Click Master planning.</span></span>
18. <span data-ttu-id="3e938-182">マスター プラン > 設定 > マスター プラン パラメーターへ移動します。</span><span class="sxs-lookup"><span data-stu-id="3e938-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="3e938-183">すべての計画プロセス フィールドを無効にするには、いいえを選択します。</span><span class="sxs-lookup"><span data-stu-id="3e938-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="3e938-184">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3e938-184">Close the page.</span></span>

