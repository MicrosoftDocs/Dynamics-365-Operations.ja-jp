--- 
title: "資産除去責務の支払利子の減価償却および見越計上 (日本)"
description: "日本では、資産除去責務 (ARO) の減価償却は固定資産と一緒に処理されます。"
author: ShylaThompson
manager: AnnBe
ms.date: 02/15/2016
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
ms.openlocfilehash: b3d7bd868a9c8b60140f4093e36ab086ece954d6
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="depreciate-and-accrue-the-interest-expense-for-asset-retirement-obligations-japan"></a><span data-ttu-id="49e83-103">資産除去責務の支払利子の減価償却および見越計上 (日本)</span><span class="sxs-lookup"><span data-stu-id="49e83-103">Depreciate and accrue the interest expense for asset retirement obligations (Japan)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="49e83-104">日本では、資産除去責務 (ARO) の減価償却は固定資産と一緒に処理されます。</span><span class="sxs-lookup"><span data-stu-id="49e83-104">For Japan, the depreciation of the asset retirement obligations (ARO) is processed along with the fixed asset.</span></span> <span data-ttu-id="49e83-105">また、ARO の総額を認識するためには、支払利子を見越計上する必要があります。</span><span class="sxs-lookup"><span data-stu-id="49e83-105">In addition, interest expenses need to be accrued to recognize the full amount of the ARO.</span></span>



<span data-ttu-id="49e83-106">このタスクを使用して、ARO を減価償却し支払利子を見越計上します。</span><span class="sxs-lookup"><span data-stu-id="49e83-106">Use this task to depreciate the ARO and accrue the interest expense.</span></span> 



<span data-ttu-id="49e83-107">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="49e83-107">In order to complete this task, the Fixed Assets configuration key must be selected.</span></span>



<span data-ttu-id="49e83-108">このタスクはデモ会社 JPMF のデータを使用して完了しました。</span><span class="sxs-lookup"><span data-stu-id="49e83-108">This task was completed using the JPMF demo company data.</span></span>


## <a name="depreciate-a-fixed-asset-with-asset-retirement-obligation"></a><span data-ttu-id="49e83-109">資産除去責務がある固定資産の減価償却</span><span class="sxs-lookup"><span data-stu-id="49e83-109">Depreciate a fixed asset with asset retirement obligation</span></span>
1. <span data-ttu-id="49e83-110">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="49e83-110">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="49e83-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="49e83-111">Click New.</span></span>
3. <span data-ttu-id="49e83-112">[名前] フィールドで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="49e83-112">In the Name field, select a value.</span></span>
4. <span data-ttu-id="49e83-113">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="49e83-113">Click Save.</span></span>
5. <span data-ttu-id="49e83-114">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="49e83-114">Click Lines.</span></span>
6. <span data-ttu-id="49e83-115">[提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="49e83-115">Click Proposals.</span></span>
7. <span data-ttu-id="49e83-116">[償却提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="49e83-116">Click Depreciation proposal.</span></span>
8. <span data-ttu-id="49e83-117">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="49e83-117">In the To date field, enter a date.</span></span>
9. <span data-ttu-id="49e83-118">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="49e83-118">Click Filter.</span></span>
10. <span data-ttu-id="49e83-119">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="49e83-119">In the Criteria field, type a value.</span></span>
11. <span data-ttu-id="49e83-120">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="49e83-120">Click OK.</span></span>
12. <span data-ttu-id="49e83-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="49e83-121">Click OK.</span></span>
    * <span data-ttu-id="49e83-122">資産除去責務の減価償却は、[ドキュメント タイプ] フィールドごとに示されます。</span><span class="sxs-lookup"><span data-stu-id="49e83-122">The depreciation of asset retirement obligation is indicated by Document type field.</span></span>  
13. <span data-ttu-id="49e83-123">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="49e83-123">Click Post.</span></span>

## <a name="accrue-the-interest-expense"></a><span data-ttu-id="49e83-124">支払利子の計上</span><span class="sxs-lookup"><span data-stu-id="49e83-124">Accrue the interest expense</span></span>
1. <span data-ttu-id="49e83-125">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="49e83-125">Close the page.</span></span>
2. <span data-ttu-id="49e83-126">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="49e83-126">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
3. <span data-ttu-id="49e83-127">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="49e83-127">Click New.</span></span>
4. <span data-ttu-id="49e83-128">[名前] フィールドで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="49e83-128">In the Name field, select a value.</span></span>
5. <span data-ttu-id="49e83-129">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="49e83-129">Click Save.</span></span>
6. <span data-ttu-id="49e83-130">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="49e83-130">Click Lines.</span></span>
7. <span data-ttu-id="49e83-131">[提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="49e83-131">Click Proposals.</span></span>
8. <span data-ttu-id="49e83-132">[除去費用の費用配分] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="49e83-132">Click Asset retirement obligation - accretion expense.</span></span>
9. <span data-ttu-id="49e83-133">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="49e83-133">In the To date field, enter a date.</span></span>
10. <span data-ttu-id="49e83-134">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="49e83-134">Click Filter.</span></span>
11. <span data-ttu-id="49e83-135">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="49e83-135">In the Criteria field, type a value.</span></span>
12. <span data-ttu-id="49e83-136">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="49e83-136">Click OK.</span></span>
13. <span data-ttu-id="49e83-137">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="49e83-137">Click OK.</span></span>
    * <span data-ttu-id="49e83-138">支払利子のレコードが提案されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="49e83-138">Confirm that the records for interest expenses are proposed.</span></span>  
    * <span data-ttu-id="49e83-139">支払利子は、トランザクション タイプごとに示されます。</span><span class="sxs-lookup"><span data-stu-id="49e83-139">The interest expenses are indicated by Transaction type</span></span>  
14. <span data-ttu-id="49e83-140">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="49e83-140">Click Post.</span></span>


