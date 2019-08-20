---
title: 安全在庫仕訳帳を使用した最小補充の更新
description: この手順では、履歴トランザクションに基づいて最小補充提案を計算し、提案を使用して品目補充を更新する方法を示します。
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3b2916d6d2f24579fd9795c0e0bc548b6c2b747
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835785"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="53ef1-103">安全在庫仕訳帳を使用した最小補充の更新</span><span class="sxs-lookup"><span data-stu-id="53ef1-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="53ef1-104">この手順では、履歴トランザクションに基づいて最小補充提案を計算し、提案を使用して品目補充を更新する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="53ef1-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="53ef1-105">これは安全在庫仕訳帳を使用して実行されます。</span><span class="sxs-lookup"><span data-stu-id="53ef1-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="53ef1-106">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="53ef1-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="53ef1-107">このタスクは、生産計画担当者による最小補充の維持を支援することを意図しています。</span><span class="sxs-lookup"><span data-stu-id="53ef1-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="53ef1-108">新しい安全在庫仕訳帳名を作成します。</span><span class="sxs-lookup"><span data-stu-id="53ef1-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="53ef1-109">[安全在庫仕訳帳名] に移動します。</span><span class="sxs-lookup"><span data-stu-id="53ef1-109">Go to Safety stock journal names.</span></span>
2. <span data-ttu-id="53ef1-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53ef1-110">Click New.</span></span>
3. <span data-ttu-id="53ef1-111">[名前] フィールドに、「材料」と入力します。</span><span class="sxs-lookup"><span data-stu-id="53ef1-111">In the Name field, type 'Material'.</span></span>
4. <span data-ttu-id="53ef1-112">[説明] フィールドで「材料」と入力します。</span><span class="sxs-lookup"><span data-stu-id="53ef1-112">In the Description field, type 'Material'.</span></span>
5. <span data-ttu-id="53ef1-113">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="53ef1-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="53ef1-114">安全在庫仕訳帳の作成</span><span class="sxs-lookup"><span data-stu-id="53ef1-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="53ef1-115">[安全在庫の計算] に移動します。</span><span class="sxs-lookup"><span data-stu-id="53ef1-115">Go to Safety stock calculation.</span></span>
2. <span data-ttu-id="53ef1-116">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53ef1-116">Click New.</span></span>
3. <span data-ttu-id="53ef1-117">[名前] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="53ef1-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="53ef1-118">作成した安全在庫仕訳帳名、たとえば「材料」を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ef1-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="53ef1-119">[行の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53ef1-119">Click Create lines.</span></span>
5. <span data-ttu-id="53ef1-120">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="53ef1-120">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="53ef1-121">日付を「2015-01-02」に設定します。</span><span class="sxs-lookup"><span data-stu-id="53ef1-121">Set the date to '2015-01-02'.</span></span>  
6. <span data-ttu-id="53ef1-122">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="53ef1-122">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="53ef1-123">日付を「2015-12-30」に設定します。</span><span class="sxs-lookup"><span data-stu-id="53ef1-123">Set the date to '2015-12-30'.</span></span>  
7. <span data-ttu-id="53ef1-124">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53ef1-124">Click OK.</span></span>
    * <span data-ttu-id="53ef1-125">これにより、在庫トランザクションがある分析コードの行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="53ef1-125">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="53ef1-126">提案の計算</span><span class="sxs-lookup"><span data-stu-id="53ef1-126">Calculate proposal</span></span>
1. <span data-ttu-id="53ef1-127">[提案の計算] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53ef1-127">Click Calculate proposal.</span></span>
2. <span data-ttu-id="53ef1-128">[リード タイムで平均払出を使用] を選択します。</span><span class="sxs-lookup"><span data-stu-id="53ef1-128">Select the Use average issue during lead time option.</span></span>
3. <span data-ttu-id="53ef1-129">[乗算の係数] を「10」に設定します。</span><span class="sxs-lookup"><span data-stu-id="53ef1-129">Set Multiplication factor to '10'.</span></span>
    * <span data-ttu-id="53ef1-130">提案を調整するために倍率が使用されます。</span><span class="sxs-lookup"><span data-stu-id="53ef1-130">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="53ef1-131">デモ データにはわずかなトランザクションしかないため、現実的な提案を得るためにはこの係数を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53ef1-131">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="53ef1-132">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53ef1-132">Click OK.</span></span>
    * <span data-ttu-id="53ef1-133">下へスクロールして M0002 と M0003 を見つけます。</span><span class="sxs-lookup"><span data-stu-id="53ef1-133">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="53ef1-134">[算出された最小数量] 列を表示します。</span><span class="sxs-lookup"><span data-stu-id="53ef1-134">View the Calculated minimum quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="53ef1-135">最小数量の更新</span><span class="sxs-lookup"><span data-stu-id="53ef1-135">Update minimum quantity</span></span>
1. <span data-ttu-id="53ef1-136">[最小数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="53ef1-136">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="53ef1-137">[算出された最小数量] の値と一致するように新しい最小数量を更新します。</span><span class="sxs-lookup"><span data-stu-id="53ef1-137">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="53ef1-138">算出された最小がゼロの場合は、必要な将来価値を入力できます。</span><span class="sxs-lookup"><span data-stu-id="53ef1-138">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="53ef1-139">たとえば、倉庫 12 がある M0002 のこのフィールドに、[算出された最小数量] を入力できます。</span><span class="sxs-lookup"><span data-stu-id="53ef1-139">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="53ef1-140">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="53ef1-140">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="53ef1-141">たとえば、倉庫 12 がある M0002 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="53ef1-141">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="53ef1-142">[最小数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="53ef1-142">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="53ef1-143">[算出された最小数量] の値と一致するように新しい最小数量を更新します。</span><span class="sxs-lookup"><span data-stu-id="53ef1-143">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="53ef1-144">算出された最小がゼロの場合は、必要な将来価値を入力できます。</span><span class="sxs-lookup"><span data-stu-id="53ef1-144">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="53ef1-145">新しい最小数量を転記して結果を検証</span><span class="sxs-lookup"><span data-stu-id="53ef1-145">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="53ef1-146">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53ef1-146">Click Post.</span></span>
2. <span data-ttu-id="53ef1-147">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53ef1-147">Click OK.</span></span>
3. <span data-ttu-id="53ef1-148">クリックして、[品目番号] フィールドのリンク先を表示します。</span><span class="sxs-lookup"><span data-stu-id="53ef1-148">Click to follow the link in the Item number field.</span></span>
4. <span data-ttu-id="53ef1-149">クリックして、[品目番号] フィールドのリンク先を表示します。</span><span class="sxs-lookup"><span data-stu-id="53ef1-149">Click to follow the link in the Item number field.</span></span>
5. <span data-ttu-id="53ef1-150">アクション ウィンドウで、[計画] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53ef1-150">On the Action Pane, click Plan.</span></span>
6. <span data-ttu-id="53ef1-151">[品目補充] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="53ef1-151">Click Item coverage.</span></span>
    * <span data-ttu-id="53ef1-152">最小数量が、安全在庫仕訳帳からの新しい最小数量で更新されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="53ef1-152">Notice that the Minimum quantity has been updated with the new minimum quantity from the safety stock journal.</span></span>  

