---
title: 労務および経費の標準原価のコンフィギュレーション
description: このトピックでは、労働者の標準原価とプロジェクトの経費を設定する方法を説明します。
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60ab8eb94d4a8a0fb2c1e732ec7b25bfd5e7611e
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867729"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="b8a54-103">労務および経費の標準原価のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b8a54-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b8a54-104">このトピックでは、労働者の標準原価とプロジェクトの経費を設定する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="b8a54-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="b8a54-105">このタスクでは、USSI データ セットを使用します。</span><span class="sxs-lookup"><span data-stu-id="b8a54-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="b8a54-106">ナビゲーション ウィンドウで、**モジュール > プロジェクト管理および会計 > 設定 > 価格 > 原価価格 (時間)** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b8a54-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="b8a54-107">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8a54-107">Select **New**.</span></span>
3. <span data-ttu-id="b8a54-108">**有効日**フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8a54-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="b8a54-109">**原価価格**フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8a54-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="b8a54-110">プロジェクト カテゴリの標準原価価格を設定したり、作業者番号、プロジェクト番号、カテゴリ、日付、またはそれらの組み合わせによって原価価格を設定したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="b8a54-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="b8a54-111">適用される原価価格は、詳細度が最も高い原価価格です。</span><span class="sxs-lookup"><span data-stu-id="b8a54-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="b8a54-112">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8a54-112">Select **Save**.</span></span>
6. <span data-ttu-id="b8a54-113">ナビゲーション ウィンドウで、**モジュール > プロジェクト管理および会計 > 設定 > 価格 > 販売価格 (時間)** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b8a54-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="b8a54-114">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8a54-114">Select **New**.</span></span>
8. <span data-ttu-id="b8a54-115">**有効日**フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8a54-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="b8a54-116">**有効**フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="b8a54-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="b8a54-117">**価格決定**フィールドに、数を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8a54-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="b8a54-118">時間トランザクションまたはプロジェクト カテゴリに対して標準販売価格を設定できます。</span><span class="sxs-lookup"><span data-stu-id="b8a54-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="b8a54-119">また、作業者番号別、プロジェクト番号別、カテゴリ別、トランザクション日別、あるいはこれらを任意に組み合わせて販売価格を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="b8a54-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="b8a54-120">作業者が時間仕訳帳にトランザクションを入力したときに適用される実際の販売価格が、最も詳細な販売価格です。</span><span class="sxs-lookup"><span data-stu-id="b8a54-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="b8a54-121">たとえば、一般的な販売価格と作業者固有の販売価格の両方が設定されている場合、作業者固有の販売価格が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b8a54-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="b8a54-122">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8a54-122">Select **Save**.</span></span>
12. <span data-ttu-id="b8a54-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b8a54-123">Close the page.</span></span>
13. <span data-ttu-id="b8a54-124">ナビゲーション ウィンドウで、**モジュール > プロジェクト管理および会計 > 設定 > 価格 > 原価価格 (経費)** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b8a54-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="b8a54-125">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8a54-125">Select **New**.</span></span>
15. <span data-ttu-id="b8a54-126">**有効日**フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8a54-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="b8a54-127">**原価価格**フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8a54-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="b8a54-128">複数のフィールドに入力することができますが、これがレコードを保存するために必要な最小値です。</span><span class="sxs-lookup"><span data-stu-id="b8a54-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="b8a54-129">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8a54-129">Select **Save**.</span></span>
18. <span data-ttu-id="b8a54-130">ナビゲーション ウィンドウで、**モジュール > プロジェクト管理および会計 > 設定 > 価格 > 販売価格 (経費)** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b8a54-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="b8a54-131">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8a54-131">Select **New**.</span></span>
20. <span data-ttu-id="b8a54-132">**有効日**フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8a54-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="b8a54-133">**有効**フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="b8a54-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="b8a54-134">**価格決定**フィールドに、数を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8a54-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="b8a54-135">作業者が経費仕訳帳にトランザクションを入力するときに適用される実際の販売価格は、最高レベルの詳細を持つ販売価格です。</span><span class="sxs-lookup"><span data-stu-id="b8a54-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="b8a54-136">たとえば、一般的および作業者固有の販売価格の両方が設定されている場合、作業者固有の販売価格が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b8a54-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="b8a54-137">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8a54-137">Select **Save**.</span></span>

