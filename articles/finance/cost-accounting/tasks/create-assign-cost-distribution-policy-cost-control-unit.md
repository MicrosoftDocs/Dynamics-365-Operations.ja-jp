---
title: 原価配分ポリシーの作成と原価管理単位への割り当て
description: '[原価配分ルール] は、集団コスト センターごとに集計される原価を配分するために使用されます。'
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostDistributionRule
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 736b537958f65fb54d0829cfbcc819fd315b530c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810129"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="a5bd5-103">原価配分ポリシーの作成と原価管理単位への割り当て</span><span class="sxs-lookup"><span data-stu-id="a5bd5-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a5bd5-104">[原価配分ルール] は、集団コスト センターごとに集計される原価を配分するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="a5bd5-105">コスト経理担当は、原価が配賦基準に基づいて、コスト センターに配分されるか確認します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="a5bd5-106">ポリシーと対応ルールは、原価管理単位に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="a5bd5-107">このタスク ガイドでは、原価配分ポリシーと対応ルールを作成する方法を示す例を使用します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="a5bd5-108">ポリシーの作成</span><span class="sxs-lookup"><span data-stu-id="a5bd5-108">Create a policy</span></span>
1. <span data-ttu-id="a5bd5-109">[原価会計] > [ポリシー] > [原価配布ポリシー] へ移動します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="a5bd5-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-110">Click New.</span></span>
3. <span data-ttu-id="a5bd5-111">[ポリシー名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="a5bd5-112">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a5bd5-113">[原価オブジェクト分析コード階層] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="a5bd5-114">[組織] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-114">Select Organization.</span></span>  
6. <span data-ttu-id="a5bd5-115">[原価要素分析コード階層] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="a5bd5-116">[CDS P/L] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="a5bd5-117">[統計分析コード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="a5bd5-118">[統計要素] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="a5bd5-119">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="a5bd5-120">ポリシーのルールを作成</span><span class="sxs-lookup"><span data-stu-id="a5bd5-120">Create rules for the policy</span></span>
1. <span data-ttu-id="a5bd5-121">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-121">Click New.</span></span>
2. <span data-ttu-id="a5bd5-122">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="a5bd5-123">[原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="a5bd5-124">階層を展開し、094 を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="a5bd5-125">[原価要素分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="a5bd5-126">[その他の営業経費] を選択し、[605110 クリーニング] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="a5bd5-127">[原価動作] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="a5bd5-128">[固定値] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="a5bd5-129">[配賦基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="a5bd5-130">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-130">Click New.</span></span>
8. <span data-ttu-id="a5bd5-131">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="a5bd5-132">[原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="a5bd5-133">階層を展開し、094 を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="a5bd5-134">[原価要素分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="a5bd5-135">[その他の営業経費] を選択し、[605150 賃貸] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="a5bd5-136">[原価動作] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="a5bd5-137">[固定値] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="a5bd5-138">[配賦基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="a5bd5-139">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="a5bd5-140">原価管理単位へルールを割り当て</span><span class="sxs-lookup"><span data-stu-id="a5bd5-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="a5bd5-141">原価管理単位の [ポリシーの割り当て] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="a5bd5-142">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-142">Click New.</span></span>
3. <span data-ttu-id="a5bd5-143">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a5bd5-144">[会計日から有効] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="a5bd5-145">有効な会計年度で、[9 月 1 日] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="a5bd5-146">[原価管理単位] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="a5bd5-147">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a5bd5-147">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]