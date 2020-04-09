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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 714f0c5f014aac1f006b8356de8570ad7d7e0d47
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148081"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="6a0fd-103">連産品の材料計画の作成</span><span class="sxs-lookup"><span data-stu-id="6a0fd-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6a0fd-104">生産計画担当者は、フォーミュラ連産品である品目の材料要求を計画します。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="6a0fd-105">この手順の作成に使用するデモ データの会社は USP2 です。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="6a0fd-106">連産品要求の作成</span><span class="sxs-lookup"><span data-stu-id="6a0fd-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="6a0fd-107">[既定のダッシュボード] に移動します。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="6a0fd-108">[販売注文の処理と照会] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="6a0fd-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-109">Click New.</span></span>
4. <span data-ttu-id="6a0fd-110">[販売注文] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-110">Click Sales order.</span></span>
5. <span data-ttu-id="6a0fd-111">[顧客口座] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="6a0fd-112">例: US-001</span><span class="sxs-lookup"><span data-stu-id="6a0fd-112">Example: US-001</span></span>  
6. <span data-ttu-id="6a0fd-113">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-113">Click OK.</span></span>
7. <span data-ttu-id="6a0fd-114">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="6a0fd-115">例: P6003</span><span class="sxs-lookup"><span data-stu-id="6a0fd-115">Example: P6003</span></span>  
8. <span data-ttu-id="6a0fd-116">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="6a0fd-117">例: 50000</span><span class="sxs-lookup"><span data-stu-id="6a0fd-117">Example: 50000</span></span>  
9. <span data-ttu-id="6a0fd-118">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="6a0fd-119">連産品の材料計画の作成</span><span class="sxs-lookup"><span data-stu-id="6a0fd-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="6a0fd-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-120">Close the page.</span></span>
2. <span data-ttu-id="6a0fd-121">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-121">Close the page.</span></span>
3. <span data-ttu-id="6a0fd-122">[マスター プラン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-122">Click Master planning.</span></span>
4. <span data-ttu-id="6a0fd-123">[計画] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="6a0fd-124">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6a0fd-125">例: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="6a0fd-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="6a0fd-126">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-126">Click Run.</span></span>
7. <span data-ttu-id="6a0fd-127">[対象に含めるレコード] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="6a0fd-128">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-128">Click Filter.</span></span>
9. <span data-ttu-id="6a0fd-129">リストで、フィールド = 品目番号の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="6a0fd-130">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="6a0fd-131">例: P6003</span><span class="sxs-lookup"><span data-stu-id="6a0fd-131">Example: P6003</span></span>  
11. <span data-ttu-id="6a0fd-132">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-132">Click OK.</span></span>
12. <span data-ttu-id="6a0fd-133">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-133">Click OK.</span></span>
13. <span data-ttu-id="6a0fd-134">[計画オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-134">Click Planned orders.</span></span>
14. <span data-ttu-id="6a0fd-135">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6a0fd-136">たとえば、「P6000」という値を含む [品目番号] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="6a0fd-137">販売注文を作成した品目の連産品としてのフォーミュラ品目でフィルター抽出します。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="6a0fd-138">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6a0fd-139">フィルターによって返された行を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="6a0fd-140">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="6a0fd-141">[ペギング] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="6a0fd-142">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6a0fd-143">計画オーダーは、連産品の販売注文にペギングされます。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="6a0fd-144">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="6a0fd-145">連産品要求の作成</span><span class="sxs-lookup"><span data-stu-id="6a0fd-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="6a0fd-146">[既定のダッシュボード] に移動します。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="6a0fd-147">[販売注文の処理と照会] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="6a0fd-148">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-148">Click New.</span></span>
4. <span data-ttu-id="6a0fd-149">[販売注文] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-149">Click Sales order.</span></span>
5. <span data-ttu-id="6a0fd-150">[顧客口座] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="6a0fd-151">例: US-001</span><span class="sxs-lookup"><span data-stu-id="6a0fd-151">Example: US-001</span></span>  
6. <span data-ttu-id="6a0fd-152">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-152">Click OK.</span></span>
7. <span data-ttu-id="6a0fd-153">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="6a0fd-154">例: P6003</span><span class="sxs-lookup"><span data-stu-id="6a0fd-154">Example: P6003</span></span>  
8. <span data-ttu-id="6a0fd-155">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="6a0fd-156">例: 50000</span><span class="sxs-lookup"><span data-stu-id="6a0fd-156">Example: 50000</span></span>  
9. <span data-ttu-id="6a0fd-157">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="6a0fd-158">連産品の材料計画の作成</span><span class="sxs-lookup"><span data-stu-id="6a0fd-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="6a0fd-159">[計画] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="6a0fd-160">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6a0fd-161">例: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="6a0fd-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="6a0fd-162">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-162">Click Run.</span></span>
4. <span data-ttu-id="6a0fd-163">[対象に含めるレコード] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="6a0fd-164">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-164">Click Filter.</span></span>
6. <span data-ttu-id="6a0fd-165">リストで、フィールド = 品目番号の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="6a0fd-166">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="6a0fd-167">例: P6003</span><span class="sxs-lookup"><span data-stu-id="6a0fd-167">Example: P6003</span></span>  
8. <span data-ttu-id="6a0fd-168">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-168">Click OK.</span></span>
9. <span data-ttu-id="6a0fd-169">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-169">Click OK.</span></span>
10. <span data-ttu-id="6a0fd-170">[計画オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-170">Click Planned orders.</span></span>
11. <span data-ttu-id="6a0fd-171">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6a0fd-172">たとえば、「P6000」という値を含む [品目番号] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="6a0fd-173">販売注文を作成した品目の連産品としてのフォーミュラ品目でフィルター抽出します。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="6a0fd-174">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6a0fd-175">フィルターによって返された行を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="6a0fd-176">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="6a0fd-177">[ペギング] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="6a0fd-178">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="6a0fd-179">計画オーダーは、連産品の販売注文にペギングされます。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="6a0fd-180">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-180">Close the page.</span></span>
17. <span data-ttu-id="6a0fd-181">[マスター プラン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-181">Click Master planning.</span></span>
18. <span data-ttu-id="6a0fd-182">マスター プラン > 設定 > マスター プラン パラメーターへ移動します。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="6a0fd-183">すべての計画プロセス フィールドを無効にするには、いいえを選択します。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="6a0fd-184">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6a0fd-184">Close the page.</span></span>

