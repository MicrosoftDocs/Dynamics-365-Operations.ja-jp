--- 
title: "連産品の材料計画の作成"
description: "生産計画担当者は、フォーミュラ連産品である品目の材料要求を計画します。"
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c8805ca02525ae001fbd5e10ad9405fe60c7473e
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="375ce-103">連産品の材料計画の作成</span><span class="sxs-lookup"><span data-stu-id="375ce-103">Create a material plan for co-products</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="375ce-104">生産計画担当者は、フォーミュラ連産品である品目の材料要求を計画します。</span><span class="sxs-lookup"><span data-stu-id="375ce-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="375ce-105">この手順の作成に使用するデモ データの会社は USP2 です。</span><span class="sxs-lookup"><span data-stu-id="375ce-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="375ce-106">連産品要求の作成</span><span class="sxs-lookup"><span data-stu-id="375ce-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="375ce-107">[既定のダッシュボード] に移動します。</span><span class="sxs-lookup"><span data-stu-id="375ce-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="375ce-108">[販売注文の処理と照会] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="375ce-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="375ce-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="375ce-109">Click New.</span></span>
4. <span data-ttu-id="375ce-110">[販売注文] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="375ce-110">Click Sales order.</span></span>
5. <span data-ttu-id="375ce-111">[顧客口座] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="375ce-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="375ce-112">例: US-001</span><span class="sxs-lookup"><span data-stu-id="375ce-112">Example: US-001</span></span>  
6. <span data-ttu-id="375ce-113">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="375ce-113">Click OK.</span></span>
7. <span data-ttu-id="375ce-114">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="375ce-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="375ce-115">例: P6003</span><span class="sxs-lookup"><span data-stu-id="375ce-115">Example: P6003</span></span>  
8. <span data-ttu-id="375ce-116">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="375ce-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="375ce-117">例: 50000</span><span class="sxs-lookup"><span data-stu-id="375ce-117">Example: 50000</span></span>  
9. <span data-ttu-id="375ce-118">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="375ce-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="375ce-119">連産品の材料計画の作成</span><span class="sxs-lookup"><span data-stu-id="375ce-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="375ce-120">[マスター プラン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="375ce-120">Click Master planning.</span></span>
2. <span data-ttu-id="375ce-121">[計画] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="375ce-121">In the Plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="375ce-122">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="375ce-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="375ce-123">例: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="375ce-123">Example: MasterPlan</span></span>  
4. <span data-ttu-id="375ce-124">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="375ce-124">Click Run.</span></span>
5. <span data-ttu-id="375ce-125">[対象に含めるレコード] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="375ce-125">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="375ce-126">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="375ce-126">Click Filter.</span></span>
7. <span data-ttu-id="375ce-127">リストで、フィールド = 品目番号の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="375ce-127">In the list, select the row for Field = Item number.</span></span>
8. <span data-ttu-id="375ce-128">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="375ce-128">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="375ce-129">例: P6003</span><span class="sxs-lookup"><span data-stu-id="375ce-129">Example: P6003</span></span>  
9. <span data-ttu-id="375ce-130">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="375ce-130">Click OK.</span></span>
10. <span data-ttu-id="375ce-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="375ce-131">Click OK.</span></span>
11. <span data-ttu-id="375ce-132">[計画オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="375ce-132">Click Planned orders.</span></span>
12. <span data-ttu-id="375ce-133">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="375ce-133">Use the Quick Filter to find records.</span></span> <span data-ttu-id="375ce-134">たとえば、「P6000」という値を含む [品目番号] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="375ce-134">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="375ce-135">販売注文を作成した品目の連産品としてのフォーミュラ品目でフィルター抽出します。</span><span class="sxs-lookup"><span data-stu-id="375ce-135">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
13. <span data-ttu-id="375ce-136">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="375ce-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="375ce-137">フィルターによって返された行を選択します。</span><span class="sxs-lookup"><span data-stu-id="375ce-137">Select any of the rows returned by the filter.</span></span>  
14. <span data-ttu-id="375ce-138">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="375ce-138">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="375ce-139">[ペギング] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="375ce-139">Expand or collapse the Pegging section.</span></span>
16. <span data-ttu-id="375ce-140">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="375ce-140">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="375ce-141">計画オーダーは、連産品の販売注文にペギングされます。</span><span class="sxs-lookup"><span data-stu-id="375ce-141">The planned order is pegged to the sales order for the co-product.</span></span>  
17. <span data-ttu-id="375ce-142">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="375ce-142">Close the page.</span></span>


