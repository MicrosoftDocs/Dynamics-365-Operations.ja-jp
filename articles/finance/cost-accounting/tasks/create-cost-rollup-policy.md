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
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: facffeaf8d880bad01877b420197e29b6791ebbf
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187777"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="cf169-103">原価ロールアップ ポリシーの作成</span><span class="sxs-lookup"><span data-stu-id="cf169-103">Create a cost rollup policy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cf169-104">この手順では、原価ロールアップ ポリシーとポリシーのルールを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="cf169-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="cf169-105">この手順の作成に使用されたデモ データの会社は、USP2 です。</span><span class="sxs-lookup"><span data-stu-id="cf169-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="cf169-106">ポリシーの作成</span><span class="sxs-lookup"><span data-stu-id="cf169-106">Create a policy</span></span>
1. <span data-ttu-id="cf169-107">[原価会計] > [ポリシー] > [原価ロールアップ ポリシー] へ移動します。</span><span class="sxs-lookup"><span data-stu-id="cf169-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="cf169-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf169-108">Click New.</span></span>
3. <span data-ttu-id="cf169-109">[ポリシー名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf169-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="cf169-110">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf169-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="cf169-111">[原価オブジェクト分析コード階層] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cf169-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="cf169-112">[原価ロールアップ CC] を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf169-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="cf169-113">[原価要素分析コード階層] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cf169-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="cf169-114">[原価ロールアップ CC] を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf169-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="cf169-115">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf169-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="cf169-116">原価ロールアップ ポリシーのルールを作成</span><span class="sxs-lookup"><span data-stu-id="cf169-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="cf169-117">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf169-117">Click New.</span></span>
2. <span data-ttu-id="cf169-118">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="cf169-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="cf169-119">[原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cf169-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="cf169-120">007 を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf169-120">Select 007.</span></span>  
4. <span data-ttu-id="cf169-121">[原価要素分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cf169-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="cf169-122">[原価ロールアップ CE] を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf169-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="cf169-123">[第 2 原価要素] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cf169-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="cf169-124">この例の場合、コスト センターに第 2 原価要素 [CC-007] を位置づけます。</span><span class="sxs-lookup"><span data-stu-id="cf169-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="cf169-125">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf169-125">Click New.</span></span>
7. <span data-ttu-id="cf169-126">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="cf169-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="cf169-127">[原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cf169-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="cf169-128">008 を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf169-128">Select 008.</span></span>  
9. <span data-ttu-id="cf169-129">[原価要素分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cf169-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="cf169-130">[原価ロールアップ CE] を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf169-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="cf169-131">[第 2 原価要素] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cf169-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="cf169-132">この例の場合、コスト センターに第 2 原価要素 [CC-008] を位置づけます。</span><span class="sxs-lookup"><span data-stu-id="cf169-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="cf169-133">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf169-133">Click New.</span></span>
12. <span data-ttu-id="cf169-134">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="cf169-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="cf169-135">[原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cf169-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="cf169-136">009 を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf169-136">Select 009.</span></span>  
14. <span data-ttu-id="cf169-137">[原価要素分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cf169-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="cf169-138">[原価ロールアップ CE] を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf169-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="cf169-139">[第 2 原価要素] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="cf169-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="cf169-140">この例の場合、コスト センターに第 2 原価要素 [CC-009] を位置づけます。</span><span class="sxs-lookup"><span data-stu-id="cf169-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="cf169-141">全てのコスト センターに、対応する第 2 原価要素が位置づけされるまで続けます。</span><span class="sxs-lookup"><span data-stu-id="cf169-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="cf169-142">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf169-142">Click Save.</span></span>

