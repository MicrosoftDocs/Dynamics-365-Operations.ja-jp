---
title: 安全在庫仕訳帳を使用した最小補充の更新
description: この手順では、履歴トランザクションに基づいて最小補充提案を計算し、提案を使用して品目補充を更新する方法を示します。
author: ChristianRytt
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 95dec1dba97923e58cfb603434a01cab6f66a3de
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252801"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="59195-103">安全在庫仕訳帳を使用した最小補充の更新</span><span class="sxs-lookup"><span data-stu-id="59195-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="59195-104">この手順では、履歴トランザクションに基づいて最小補充提案を計算し、提案を使用して品目補充を更新する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="59195-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="59195-105">これは安全在庫仕訳帳を使用して実行されます。</span><span class="sxs-lookup"><span data-stu-id="59195-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="59195-106">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="59195-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="59195-107">このタスクは、生産計画担当者による最小補充の維持を支援することを意図しています。</span><span class="sxs-lookup"><span data-stu-id="59195-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="59195-108">新しい安全在庫仕訳帳名を作成します。</span><span class="sxs-lookup"><span data-stu-id="59195-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="59195-109">**ナビゲーション ウィンドウ** で、**マスター プラン > 設定 > 安全在庫仕訳帳名** に移動します。</span><span class="sxs-lookup"><span data-stu-id="59195-109">In the **Navigation pane**, go to **Master planning > Setup > Safety stock journal names**.</span></span>
2. <span data-ttu-id="59195-110">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="59195-110">Click **New**.</span></span>
3. <span data-ttu-id="59195-111">**名前** フィールドに、「材料」と入力します。</span><span class="sxs-lookup"><span data-stu-id="59195-111">In the **Name** field, type 'Material'.</span></span>
4. <span data-ttu-id="59195-112">**説明** フィールドに、「材料」と入力します。</span><span class="sxs-lookup"><span data-stu-id="59195-112">In the **Description** field, type 'Material'.</span></span>
5. <span data-ttu-id="59195-113">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="59195-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="59195-114">安全在庫仕訳帳の作成</span><span class="sxs-lookup"><span data-stu-id="59195-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="59195-115">**ナビゲーション ウィンドウ** で、**マスター プラン > マスター プラン > 実行 > 安全在庫の計算** に移動します。</span><span class="sxs-lookup"><span data-stu-id="59195-115">In the **Navigation pane**, go to **Master planning > Master planning > Run > Safety stock calculation**.</span></span>
2. <span data-ttu-id="59195-116">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="59195-116">Click **New**.</span></span>
3. <span data-ttu-id="59195-117">**名前** フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="59195-117">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="59195-118">作成した安全在庫仕訳帳名、たとえば「材料」を選択します。</span><span class="sxs-lookup"><span data-stu-id="59195-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="59195-119">**明細行の作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="59195-119">Click **Create lines**.</span></span>
5. <span data-ttu-id="59195-120">**開始日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="59195-120">In the **From date** field, enter a date.</span></span>  
6. <span data-ttu-id="59195-121">**終了日** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="59195-121">In the **To date** field, enter a date.</span></span>
7. <span data-ttu-id="59195-122">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="59195-122">Click **OK**.</span></span> <span data-ttu-id="59195-123">これにより、在庫トランザクションがある分析コードの行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="59195-123">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="59195-124">提案の計算</span><span class="sxs-lookup"><span data-stu-id="59195-124">Calculate proposal</span></span>
1. <span data-ttu-id="59195-125">**提案の計算** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="59195-125">Click **Calculate proposal**.</span></span>
2. <span data-ttu-id="59195-126">**リード タイムで平均払出を使用** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="59195-126">Select the **Use average issue during lead time** option.</span></span>
3. <span data-ttu-id="59195-127">**乗算の係数** を「10」に設定します。</span><span class="sxs-lookup"><span data-stu-id="59195-127">Set **Multiplication factor** to '10'.</span></span> <span data-ttu-id="59195-128">提案を調整するために倍率が使用されます。</span><span class="sxs-lookup"><span data-stu-id="59195-128">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="59195-129">デモ データにはわずかなトランザクションしかないため、現実的な提案を得るためにはこの係数を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59195-129">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="59195-130">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="59195-130">Click **OK**.</span></span> <span data-ttu-id="59195-131">下へスクロールして M0002 と M0003 を見つけます。</span><span class="sxs-lookup"><span data-stu-id="59195-131">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="59195-132">**算出された最小** 数量列を表示します。</span><span class="sxs-lookup"><span data-stu-id="59195-132">View the **Calculated minimum** quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="59195-133">最小数量の更新</span><span class="sxs-lookup"><span data-stu-id="59195-133">Update minimum quantity</span></span>
1. <span data-ttu-id="59195-134">**新しい最小数量** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="59195-134">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="59195-135">[算出された最小数量] の値と一致するように新しい最小数量を更新します。</span><span class="sxs-lookup"><span data-stu-id="59195-135">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="59195-136">算出された最小がゼロの場合は、必要な将来価値を入力できます。</span><span class="sxs-lookup"><span data-stu-id="59195-136">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="59195-137">たとえば、倉庫 12 がある M0002 のこのフィールドに、[算出された最小数量] を入力できます。</span><span class="sxs-lookup"><span data-stu-id="59195-137">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="59195-138">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="59195-138">In the list, find and select the desired record.</span></span> <span data-ttu-id="59195-139">たとえば、倉庫 12 がある M0002 を選択できます。</span><span class="sxs-lookup"><span data-stu-id="59195-139">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="59195-140">**新しい最小数量** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="59195-140">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="59195-141">[算出された最小数量] の値と一致するように新しい最小数量を更新します。</span><span class="sxs-lookup"><span data-stu-id="59195-141">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="59195-142">算出された最小がゼロの場合は、必要な将来価値を入力できます。</span><span class="sxs-lookup"><span data-stu-id="59195-142">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="59195-143">新しい最小数量を転記して結果を検証</span><span class="sxs-lookup"><span data-stu-id="59195-143">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="59195-144">**転記** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="59195-144">Click **Post**.</span></span>
2. <span data-ttu-id="59195-145">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="59195-145">Click **OK**.</span></span>
3. <span data-ttu-id="59195-146">クリックして、**品目番号** フィールドのリンク先を表示します。</span><span class="sxs-lookup"><span data-stu-id="59195-146">Click to follow the link in the **Item number** field.</span></span>
4. <span data-ttu-id="59195-147">クリックして、**品目番号** フィールドのリンク先を表示します。</span><span class="sxs-lookup"><span data-stu-id="59195-147">Click to follow the link in the **Item number** field.</span></span>
5. <span data-ttu-id="59195-148">**アクション ウィンドウ** で計画をクリックします。</span><span class="sxs-lookup"><span data-stu-id="59195-148">On the **Action Pane**, click Plan.</span></span>
6. <span data-ttu-id="59195-149">**品目補充** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="59195-149">Click **Item coverage**.</span></span> <span data-ttu-id="59195-150">**最小数量** が、安全在庫仕訳帳からの新しい最小数量で更新されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="59195-150">Notice that the **Minimum quantity** has been updated with the new minimum quantity from the safety stock journal.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]