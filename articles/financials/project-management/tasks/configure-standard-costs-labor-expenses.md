--- 
title: "労務および経費の標準原価のコンフィギュレーション"
description: "この手順では、労働者の標準原価とプロジェクトの経費を設定する方法を示します。"
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: f89590c87aec1a7200e95aeac6b2765fc64bb623
ms.contentlocale: ja-jp
ms.lasthandoff: 09/14/2018

---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="6cce9-103">労務および経費の標準原価のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6cce9-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6cce9-104">この手順では、労働者の標準原価とプロジェクトの経費を設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="6cce9-104">This procedure shows you how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="6cce9-105">このタスクでは、USSI データ セットを使用します。</span><span class="sxs-lookup"><span data-stu-id="6cce9-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="6cce9-106">[プロジェクト管理および会計] > [設定] > [価格] > [原価価格 (時間)] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6cce9-106">Go to Project management and accounting > Setup > Prices > Cost price (hour).</span></span>
2. <span data-ttu-id="6cce9-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6cce9-107">Click New.</span></span>
3. <span data-ttu-id="6cce9-108">[有効日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="6cce9-108">In the Effective date field, enter a date.</span></span>
4. <span data-ttu-id="6cce9-109">[原価価格] フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="6cce9-109">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="6cce9-110">プロジェクト カテゴリの標準原価価格を設定したり、作業者番号、プロジェクト番号、カテゴリ、日付、またはそれらの組み合わせによって原価価格を設定したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="6cce9-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="6cce9-111">適用される原価価格は、詳細度が最も高い原価価格です。</span><span class="sxs-lookup"><span data-stu-id="6cce9-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="6cce9-112">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6cce9-112">Click Save.</span></span>
6. <span data-ttu-id="6cce9-113">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6cce9-113">Close the page.</span></span>
7. <span data-ttu-id="6cce9-114">[プロジェクト管理および会計] > [設定] > [価格] > [販売価格 (時間)] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6cce9-114">Go to Project management and accounting > Setup > Prices > Sales price (hour).</span></span>
8. <span data-ttu-id="6cce9-115">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6cce9-115">Click New.</span></span>
9. <span data-ttu-id="6cce9-116">[有効日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="6cce9-116">In the Effective date field, enter a date.</span></span>
10. <span data-ttu-id="6cce9-117">[有効] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6cce9-117">In the Valid for field, select an option.</span></span>
11. <span data-ttu-id="6cce9-118">[価格決定] フィールドに、数を入力します。</span><span class="sxs-lookup"><span data-stu-id="6cce9-118">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="6cce9-119">時間トランザクションまたはプロジェクト カテゴリに対して標準販売価格を設定できます。</span><span class="sxs-lookup"><span data-stu-id="6cce9-119">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="6cce9-120">また、作業者番号別、プロジェクト番号別、カテゴリ別、トランザクション日別、あるいはこれらを任意に組み合わせて販売価格を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="6cce9-120">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="6cce9-121">作業者が時間仕訳帳にトランザクションを入力したときに適用される実際の販売価格が、最も詳細な販売価格です。</span><span class="sxs-lookup"><span data-stu-id="6cce9-121">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="6cce9-122">たとえば、一般的な販売価格と作業者固有の販売価格の両方が設定されている場合、作業者固有の販売価格が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6cce9-122">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
12. <span data-ttu-id="6cce9-123">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6cce9-123">Click Save.</span></span>
13. <span data-ttu-id="6cce9-124">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6cce9-124">Close the page.</span></span>
14. <span data-ttu-id="6cce9-125">[プロジェクト管理および会計] > [設定] > [価格] > [原価価格 (経費)] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6cce9-125">Go to Project management and accounting > Setup > Prices > Cost price (expense).</span></span>
15. <span data-ttu-id="6cce9-126">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6cce9-126">Click New.</span></span>
16. <span data-ttu-id="6cce9-127">[有効日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="6cce9-127">In the Effective date field, enter a date.</span></span>
17. <span data-ttu-id="6cce9-128">[原価価格] フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="6cce9-128">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="6cce9-129">複数のフィールドに入力することができますが、これがレコードを保存するために必要な最小値です。</span><span class="sxs-lookup"><span data-stu-id="6cce9-129">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
18. <span data-ttu-id="6cce9-130">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6cce9-130">Click Save.</span></span>
19. <span data-ttu-id="6cce9-131">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6cce9-131">Close the page.</span></span>
20. <span data-ttu-id="6cce9-132">[プロジェクト管理および会計] > [設定] > [価格] > [販売価格 (経費)] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6cce9-132">Go to Project management and accounting > Setup > Prices > Sales price (expense).</span></span>
21. <span data-ttu-id="6cce9-133">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6cce9-133">Click New.</span></span>
22. <span data-ttu-id="6cce9-134">[有効日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="6cce9-134">In the Effective date field, enter a date.</span></span>
23. <span data-ttu-id="6cce9-135">[有効] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6cce9-135">In the Valid for field, select an option.</span></span>
24. <span data-ttu-id="6cce9-136">[価格決定] フィールドに、数を入力します。</span><span class="sxs-lookup"><span data-stu-id="6cce9-136">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="6cce9-137">作業者が経費仕訳帳にトランザクションを入力するときに適用される実際の販売価格は、最高レベルの詳細を持つ販売価格です。</span><span class="sxs-lookup"><span data-stu-id="6cce9-137">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="6cce9-138">たとえば、一般的および作業者固有の販売価格の両方が設定されている場合、作業者固有の販売価格が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6cce9-138">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
25. <span data-ttu-id="6cce9-139">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6cce9-139">Click Save.</span></span>


