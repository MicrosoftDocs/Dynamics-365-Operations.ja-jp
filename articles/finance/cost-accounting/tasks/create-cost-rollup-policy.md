---
title: 原価ロールアップ ポリシーの作成
description: この手順では、原価ロールアップ ポリシーとポリシーのルールを作成する方法を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b6d32cc2c1844c6c334dd00b249c736e153f13d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445324"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="b35e5-103">原価ロールアップ ポリシーの作成</span><span class="sxs-lookup"><span data-stu-id="b35e5-103">Create a cost rollup policy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b35e5-104">この手順では、原価ロールアップ ポリシーとポリシーのルールを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b35e5-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="b35e5-105">この手順の作成に使用されたデモ データの会社は、USP2 です。</span><span class="sxs-lookup"><span data-stu-id="b35e5-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="b35e5-106">ポリシーの作成</span><span class="sxs-lookup"><span data-stu-id="b35e5-106">Create a policy</span></span>
1. <span data-ttu-id="b35e5-107">[原価会計] > [ポリシー] > [原価ロールアップ ポリシー] へ移動します。</span><span class="sxs-lookup"><span data-stu-id="b35e5-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="b35e5-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b35e5-108">Click New.</span></span>
3. <span data-ttu-id="b35e5-109">[ポリシー名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b35e5-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="b35e5-110">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b35e5-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b35e5-111">[原価オブジェクト分析コード階層] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b35e5-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="b35e5-112">[原価ロールアップ CC] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b35e5-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="b35e5-113">[原価要素分析コード階層] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b35e5-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="b35e5-114">[原価ロールアップ CC] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b35e5-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="b35e5-115">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b35e5-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="b35e5-116">原価ロールアップ ポリシーのルールを作成</span><span class="sxs-lookup"><span data-stu-id="b35e5-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="b35e5-117">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b35e5-117">Click New.</span></span>
2. <span data-ttu-id="b35e5-118">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b35e5-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="b35e5-119">[原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b35e5-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="b35e5-120">007 を選択します。</span><span class="sxs-lookup"><span data-stu-id="b35e5-120">Select 007.</span></span>  
4. <span data-ttu-id="b35e5-121">[原価要素分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b35e5-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="b35e5-122">[原価ロールアップ CE] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b35e5-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="b35e5-123">[第 2 原価要素] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b35e5-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="b35e5-124">この例の場合、コスト センターに第 2 原価要素 [CC-007] を位置づけます。</span><span class="sxs-lookup"><span data-stu-id="b35e5-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="b35e5-125">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b35e5-125">Click New.</span></span>
7. <span data-ttu-id="b35e5-126">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b35e5-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="b35e5-127">[原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b35e5-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="b35e5-128">008 を選択します。</span><span class="sxs-lookup"><span data-stu-id="b35e5-128">Select 008.</span></span>  
9. <span data-ttu-id="b35e5-129">[原価要素分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b35e5-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="b35e5-130">[原価ロールアップ CE] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b35e5-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="b35e5-131">[第 2 原価要素] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b35e5-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="b35e5-132">この例の場合、コスト センターに第 2 原価要素 [CC-008] を位置づけます。</span><span class="sxs-lookup"><span data-stu-id="b35e5-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="b35e5-133">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b35e5-133">Click New.</span></span>
12. <span data-ttu-id="b35e5-134">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b35e5-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="b35e5-135">[原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b35e5-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="b35e5-136">009 を選択します。</span><span class="sxs-lookup"><span data-stu-id="b35e5-136">Select 009.</span></span>  
14. <span data-ttu-id="b35e5-137">[原価要素分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b35e5-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="b35e5-138">[原価ロールアップ CE] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b35e5-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="b35e5-139">[第 2 原価要素] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b35e5-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="b35e5-140">この例の場合、コスト センターに第 2 原価要素 [CC-009] を位置づけます。</span><span class="sxs-lookup"><span data-stu-id="b35e5-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="b35e5-141">全てのコスト センターに、対応する第 2 原価要素が位置づけされるまで続けます。</span><span class="sxs-lookup"><span data-stu-id="b35e5-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="b35e5-142">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b35e5-142">Click Save.</span></span>

