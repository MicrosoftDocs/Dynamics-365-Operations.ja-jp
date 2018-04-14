--- 
title: "償却超過額および償却不足額の定期決済 (日本)"
description: "このタスクでは、損金の減価償却費を計算および記録する方法を説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a25665f6031269a8ba332f0d411638569243e341
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="periodic-settlement-of-over-and-under-depreciation-japan"></a><span data-ttu-id="3e3c9-103">償却超過額および償却不足額の定期決済 (日本)</span><span class="sxs-lookup"><span data-stu-id="3e3c9-103">Periodic settlement of over and under depreciation (Japan)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3e3c9-104">このタスクでは、損金の減価償却費を計算および記録する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-104">Use this task to learn how to calculate and record depreciation expense for deductible expense.</span></span>



<span data-ttu-id="3e3c9-105">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-105">This task uses the JPMF demo company data.</span></span>




## <a name="fixed-asset-depreciation"></a><span data-ttu-id="3e3c9-106">固定資産の減価償却</span><span class="sxs-lookup"><span data-stu-id="3e3c9-106">Fixed asset depreciation</span></span>
1. <span data-ttu-id="3e3c9-107">次の順に移動します: [固定資産] ></span><span class="sxs-lookup"><span data-stu-id="3e3c9-107">Go to Fixed assets > ..</span></span> <span data-ttu-id="3e3c9-108">> [固定資産仕訳帳]。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-108">> Fixed assets journal.</span></span>
2. <span data-ttu-id="3e3c9-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-109">Click New.</span></span>
3. <span data-ttu-id="3e3c9-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="3e3c9-111">例: FAD</span><span class="sxs-lookup"><span data-stu-id="3e3c9-111">Example: FAD</span></span>  
4. <span data-ttu-id="3e3c9-112">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-112">Click Lines.</span></span>
5. <span data-ttu-id="3e3c9-113">[提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-113">Click Proposals.</span></span>
6. <span data-ttu-id="3e3c9-114">[償却提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-114">Click Depreciation proposal.</span></span>
7. <span data-ttu-id="3e3c9-115">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-115">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="3e3c9-116">例: 3/31/ 2016</span><span class="sxs-lookup"><span data-stu-id="3e3c9-116">Example: 3/31/2016</span></span>  
8. <span data-ttu-id="3e3c9-117">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-117">Click Filter.</span></span>
9. <span data-ttu-id="3e3c9-118">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-118">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="3e3c9-119">たとえば、固定資産番号 = BUILM-000005 に設定します。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-119">For example, set Fixed asset number = BUILM-000005</span></span>  
10. <span data-ttu-id="3e3c9-120">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-120">Click OK.</span></span>
11. <span data-ttu-id="3e3c9-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-121">Click OK.</span></span>
    * <span data-ttu-id="3e3c9-122">原価償却仕訳帳が作成されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-122">Verify that the depreciation journal  was created.</span></span>  
12. <span data-ttu-id="3e3c9-123">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-123">Click Post.</span></span>

## <a name="over-and-under-depr-settlements"></a><span data-ttu-id="3e3c9-124">償却超過/償却不足決済</span><span class="sxs-lookup"><span data-stu-id="3e3c9-124">Over and under depr settlements</span></span>
1. <span data-ttu-id="3e3c9-125">[固定資産] > [定期処理のタスク] > [償却超過/償却不足額の決済] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-125">Go to Fixed assets > Periodic tasks > Settlement of over depreciation or under depreciation amount.</span></span>
2. <span data-ttu-id="3e3c9-126">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-126">Click New.</span></span>
3. <span data-ttu-id="3e3c9-127">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-127">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="3e3c9-128">例: 03/31/2016</span><span class="sxs-lookup"><span data-stu-id="3e3c9-128">Example: 03/31/2016</span></span>  
4. <span data-ttu-id="3e3c9-129">[仕訳帳名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-129">In the Journal name field, type a value.</span></span>
    * <span data-ttu-id="3e3c9-130">例: FAD_TAX</span><span class="sxs-lookup"><span data-stu-id="3e3c9-130">Example: FAD_TAX</span></span>  
5. <span data-ttu-id="3e3c9-131">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-131">Expand the Records to include section.</span></span>
6. <span data-ttu-id="3e3c9-132">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-132">Click Filter.</span></span>
7. <span data-ttu-id="3e3c9-133">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-133">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="3e3c9-134">たとえば、固定資産番号 = BUILM-000005 に設定します。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-134">For example, set the Fixed asset number = BUILM-000005</span></span>  
8. <span data-ttu-id="3e3c9-135">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-135">Click OK.</span></span>
9. <span data-ttu-id="3e3c9-136">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-136">Click OK.</span></span>
10. <span data-ttu-id="3e3c9-137">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-137">Refresh the page.</span></span>
    * <span data-ttu-id="3e3c9-138">結果はすぐに表示されないことがあります。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-138">The results may not appear instantly.</span></span> <span data-ttu-id="3e3c9-139">更新をクリックして、結果が作成されたか表示します。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-139">Click refresh to see if the result is created.</span></span>  
11. <span data-ttu-id="3e3c9-140">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-140">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3e3c9-141">[ステータス] = [ドラフト] である新しい結果をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-141">Click the new result with Status = Draft.</span></span>  
12. <span data-ttu-id="3e3c9-142">[決済結果の表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-142">Click View settlement results.</span></span>
    * <span data-ttu-id="3e3c9-143">正しい結果が作成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-143">Verify that the correct result is created.</span></span>  
13. <span data-ttu-id="3e3c9-144">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e3c9-144">Click Post.</span></span>


