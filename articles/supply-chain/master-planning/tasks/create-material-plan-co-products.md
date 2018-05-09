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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f3a411e8fc773957b5ce3f24749242d9d0c6ffd0
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="8b76e-103">連産品の材料計画の作成</span><span class="sxs-lookup"><span data-stu-id="8b76e-103">Create a material plan for co-products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8b76e-104">生産計画担当者は、フォーミュラ連産品である品目の材料要求を計画します。</span><span class="sxs-lookup"><span data-stu-id="8b76e-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="8b76e-105">この手順の作成に使用するデモ データの会社は USP2 です。</span><span class="sxs-lookup"><span data-stu-id="8b76e-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="8b76e-106">連産品要求の作成</span><span class="sxs-lookup"><span data-stu-id="8b76e-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="8b76e-107">[既定のダッシュボード] に移動します。</span><span class="sxs-lookup"><span data-stu-id="8b76e-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="8b76e-108">[販売注文の処理と照会] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b76e-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="8b76e-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b76e-109">Click New.</span></span>
4. <span data-ttu-id="8b76e-110">[販売注文] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b76e-110">Click Sales order.</span></span>
5. <span data-ttu-id="8b76e-111">[顧客口座] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8b76e-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="8b76e-112">例: US-001</span><span class="sxs-lookup"><span data-stu-id="8b76e-112">Example: US-001</span></span>  
6. <span data-ttu-id="8b76e-113">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b76e-113">Click OK.</span></span>
7. <span data-ttu-id="8b76e-114">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8b76e-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="8b76e-115">例: P6003</span><span class="sxs-lookup"><span data-stu-id="8b76e-115">Example: P6003</span></span>  
8. <span data-ttu-id="8b76e-116">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8b76e-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="8b76e-117">例: 50000</span><span class="sxs-lookup"><span data-stu-id="8b76e-117">Example: 50000</span></span>  
9. <span data-ttu-id="8b76e-118">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b76e-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="8b76e-119">連産品の材料計画の作成</span><span class="sxs-lookup"><span data-stu-id="8b76e-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="8b76e-120">[マスター プラン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b76e-120">Click Master planning.</span></span>
2. <span data-ttu-id="8b76e-121">[計画] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="8b76e-121">In the Plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="8b76e-122">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b76e-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8b76e-123">例: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="8b76e-123">Example: MasterPlan</span></span>  
4. <span data-ttu-id="8b76e-124">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b76e-124">Click Run.</span></span>
5. <span data-ttu-id="8b76e-125">[対象に含めるレコード] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="8b76e-125">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="8b76e-126">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b76e-126">Click Filter.</span></span>
7. <span data-ttu-id="8b76e-127">リストで、フィールド = 品目番号の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b76e-127">In the list, select the row for Field = Item number.</span></span>
8. <span data-ttu-id="8b76e-128">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8b76e-128">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="8b76e-129">例: P6003</span><span class="sxs-lookup"><span data-stu-id="8b76e-129">Example: P6003</span></span>  
9. <span data-ttu-id="8b76e-130">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b76e-130">Click OK.</span></span>
10. <span data-ttu-id="8b76e-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b76e-131">Click OK.</span></span>
11. <span data-ttu-id="8b76e-132">[計画オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b76e-132">Click Planned orders.</span></span>
12. <span data-ttu-id="8b76e-133">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="8b76e-133">Use the Quick Filter to find records.</span></span> <span data-ttu-id="8b76e-134">たとえば、「P6000」という値を含む [品目番号] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="8b76e-134">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="8b76e-135">販売注文を作成した品目の連産品としてのフォーミュラ品目でフィルター抽出します。</span><span class="sxs-lookup"><span data-stu-id="8b76e-135">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
13. <span data-ttu-id="8b76e-136">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="8b76e-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8b76e-137">フィルターによって返された行を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b76e-137">Select any of the rows returned by the filter.</span></span>  
14. <span data-ttu-id="8b76e-138">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b76e-138">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="8b76e-139">[ペギング] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="8b76e-139">Expand or collapse the Pegging section.</span></span>
16. <span data-ttu-id="8b76e-140">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8b76e-140">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8b76e-141">計画オーダーは、連産品の販売注文にペギングされます。</span><span class="sxs-lookup"><span data-stu-id="8b76e-141">The planned order is pegged to the sales order for the co-product.</span></span>  
17. <span data-ttu-id="8b76e-142">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8b76e-142">Close the page.</span></span>


