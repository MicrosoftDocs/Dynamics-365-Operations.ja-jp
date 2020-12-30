---
title: 連産品の材料計画の作成
description: 生産計画担当者は、フォーミュラ連産品である品目の材料要求を計画します。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 14de9a1085ac1cae88ad93c35385dd43c60ed4d1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431983"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="480be-103">連産品の材料計画の作成</span><span class="sxs-lookup"><span data-stu-id="480be-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="480be-104">生産計画担当者は、フォーミュラ連産品である品目の材料要求を計画します。</span><span class="sxs-lookup"><span data-stu-id="480be-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="480be-105">この手順の作成に使用するデモ データの会社は USP2 です。</span><span class="sxs-lookup"><span data-stu-id="480be-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="480be-106">連産品要求の作成</span><span class="sxs-lookup"><span data-stu-id="480be-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="480be-107">[既定のダッシュボード] に移動します。</span><span class="sxs-lookup"><span data-stu-id="480be-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="480be-108">[販売注文の処理と照会] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="480be-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-109">Click New.</span></span>
4. <span data-ttu-id="480be-110">[販売注文] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-110">Click Sales order.</span></span>
5. <span data-ttu-id="480be-111">[顧客口座] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="480be-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="480be-112">例: US-001</span><span class="sxs-lookup"><span data-stu-id="480be-112">Example: US-001</span></span>  
6. <span data-ttu-id="480be-113">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-113">Click OK.</span></span>
7. <span data-ttu-id="480be-114">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="480be-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="480be-115">例: P6003</span><span class="sxs-lookup"><span data-stu-id="480be-115">Example: P6003</span></span>  
8. <span data-ttu-id="480be-116">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="480be-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="480be-117">例: 50000</span><span class="sxs-lookup"><span data-stu-id="480be-117">Example: 50000</span></span>  
9. <span data-ttu-id="480be-118">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="480be-119">連産品の材料計画の作成</span><span class="sxs-lookup"><span data-stu-id="480be-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="480be-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="480be-120">Close the page.</span></span>
2. <span data-ttu-id="480be-121">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="480be-121">Close the page.</span></span>
3. <span data-ttu-id="480be-122">[マスター プラン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-122">Click Master planning.</span></span>
4. <span data-ttu-id="480be-123">[計画] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="480be-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="480be-124">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="480be-125">例: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="480be-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="480be-126">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-126">Click Run.</span></span>
7. <span data-ttu-id="480be-127">[対象に含めるレコード] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="480be-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="480be-128">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-128">Click Filter.</span></span>
9. <span data-ttu-id="480be-129">リストで、フィールド = 品目番号の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="480be-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="480be-130">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="480be-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="480be-131">例: P6003</span><span class="sxs-lookup"><span data-stu-id="480be-131">Example: P6003</span></span>  
11. <span data-ttu-id="480be-132">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-132">Click OK.</span></span>
12. <span data-ttu-id="480be-133">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-133">Click OK.</span></span>
13. <span data-ttu-id="480be-134">[計画オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-134">Click Planned orders.</span></span>
14. <span data-ttu-id="480be-135">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="480be-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="480be-136">たとえば、「P6000」という値を含む [品目番号] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="480be-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="480be-137">販売注文を作成した品目の連産品としてのフォーミュラ品目でフィルター抽出します。</span><span class="sxs-lookup"><span data-stu-id="480be-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="480be-138">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="480be-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="480be-139">フィルターによって返された行を選択します。</span><span class="sxs-lookup"><span data-stu-id="480be-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="480be-140">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="480be-141">[ペギング] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="480be-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="480be-142">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="480be-143">計画オーダーは、連産品の販売注文にペギングされます。</span><span class="sxs-lookup"><span data-stu-id="480be-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="480be-144">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="480be-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="480be-145">連産品要求の作成</span><span class="sxs-lookup"><span data-stu-id="480be-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="480be-146">[既定のダッシュボード] に移動します。</span><span class="sxs-lookup"><span data-stu-id="480be-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="480be-147">[販売注文の処理と照会] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="480be-148">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-148">Click New.</span></span>
4. <span data-ttu-id="480be-149">[販売注文] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-149">Click Sales order.</span></span>
5. <span data-ttu-id="480be-150">[顧客口座] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="480be-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="480be-151">例: US-001</span><span class="sxs-lookup"><span data-stu-id="480be-151">Example: US-001</span></span>  
6. <span data-ttu-id="480be-152">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-152">Click OK.</span></span>
7. <span data-ttu-id="480be-153">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="480be-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="480be-154">例: P6003</span><span class="sxs-lookup"><span data-stu-id="480be-154">Example: P6003</span></span>  
8. <span data-ttu-id="480be-155">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="480be-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="480be-156">例: 50000</span><span class="sxs-lookup"><span data-stu-id="480be-156">Example: 50000</span></span>  
9. <span data-ttu-id="480be-157">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="480be-158">連産品の材料計画の作成</span><span class="sxs-lookup"><span data-stu-id="480be-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="480be-159">[計画] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="480be-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="480be-160">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="480be-161">例: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="480be-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="480be-162">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-162">Click Run.</span></span>
4. <span data-ttu-id="480be-163">[対象に含めるレコード] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="480be-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="480be-164">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-164">Click Filter.</span></span>
6. <span data-ttu-id="480be-165">リストで、フィールド = 品目番号の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="480be-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="480be-166">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="480be-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="480be-167">例: P6003</span><span class="sxs-lookup"><span data-stu-id="480be-167">Example: P6003</span></span>  
8. <span data-ttu-id="480be-168">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-168">Click OK.</span></span>
9. <span data-ttu-id="480be-169">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-169">Click OK.</span></span>
10. <span data-ttu-id="480be-170">[計画オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-170">Click Planned orders.</span></span>
11. <span data-ttu-id="480be-171">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="480be-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="480be-172">たとえば、「P6000」という値を含む [品目番号] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="480be-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="480be-173">販売注文を作成した品目の連産品としてのフォーミュラ品目でフィルター抽出します。</span><span class="sxs-lookup"><span data-stu-id="480be-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="480be-174">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="480be-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="480be-175">フィルターによって返された行を選択します。</span><span class="sxs-lookup"><span data-stu-id="480be-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="480be-176">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="480be-177">[ペギング] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="480be-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="480be-178">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="480be-179">計画オーダーは、連産品の販売注文にペギングされます。</span><span class="sxs-lookup"><span data-stu-id="480be-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="480be-180">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="480be-180">Close the page.</span></span>
17. <span data-ttu-id="480be-181">[マスター プラン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="480be-181">Click Master planning.</span></span>
18. <span data-ttu-id="480be-182">マスター プラン > 設定 > マスター プラン パラメーターへ移動します。</span><span class="sxs-lookup"><span data-stu-id="480be-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="480be-183">すべての計画プロセス フィールドを無効にするには、いいえを選択します。</span><span class="sxs-lookup"><span data-stu-id="480be-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="480be-184">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="480be-184">Close the page.</span></span>

