---
title: 原価配賦ポリシーの作成と原価管理単位への割り当て
description: 原価配賦ポリシーと対応ルールを原価管理単位に作成し割り当てるには、この手順を使用します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
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
ms.openlocfilehash: 2f0422a9aaf95184b556293bf6ebcaf4dcfb5b59
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178662"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="b9fc2-103">原価配賦ポリシーの作成と原価管理単位への割り当て</span><span class="sxs-lookup"><span data-stu-id="b9fc2-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b9fc2-104">原価配賦ポリシーと対応ルールを原価管理単位に作成し割り当てるには、この手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="b9fc2-105">この記録では、USP2 デモ データ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="b9fc2-106">ポリシーの作成</span><span class="sxs-lookup"><span data-stu-id="b9fc2-106">Create a policy</span></span>
1. <span data-ttu-id="b9fc2-107">[原価会計] > [ポリシー] > [原価配賦ポリシー] へ移動します。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="b9fc2-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-108">Click New.</span></span>
3. <span data-ttu-id="b9fc2-109">[ポリシー名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="b9fc2-110">[原価オブジェクト分析コード階層] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="b9fc2-111">[組織] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-111">Select Organization.</span></span>  
5. <span data-ttu-id="b9fc2-112">[統計分析コード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="b9fc2-113">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="b9fc2-114">配賦ルールの作成</span><span class="sxs-lookup"><span data-stu-id="b9fc2-114">Create allocation rules</span></span>
1. <span data-ttu-id="b9fc2-115">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-115">Click New.</span></span>
2. <span data-ttu-id="b9fc2-116">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="b9fc2-117">[原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="b9fc2-118">[原価動作] フィールドで、[合計] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="b9fc2-119">[配賦基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="b9fc2-120">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-120">Click New.</span></span>
7. <span data-ttu-id="b9fc2-121">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="b9fc2-122">[原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="b9fc2-123">[原価動作] フィールドで、[合計] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="b9fc2-124">[配賦基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="b9fc2-125">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-125">Click New.</span></span>
12. <span data-ttu-id="b9fc2-126">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="b9fc2-127">[原価オブジェクト分析コード階層ノード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="b9fc2-128">[原価動作] フィールドで、[合計] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="b9fc2-129">[配賦基準] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="b9fc2-130">すべてのルールを作成するまで、続行します。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="b9fc2-131">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="b9fc2-132">原価管理単位へポリシーを割り当て</span><span class="sxs-lookup"><span data-stu-id="b9fc2-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="b9fc2-133">原価管理単位の [ポリシーの割り当て] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="b9fc2-134">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-134">Click New.</span></span>
3. <span data-ttu-id="b9fc2-135">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="b9fc2-136">[会計日から有効] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="b9fc2-137">ルールの日付は有効です。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-137">The rules are date-effective.</span></span> <span data-ttu-id="b9fc2-138">新しいバージョンが作成された場合、ユーザーまたはシステムは、そのルールの期限を切ることが可能です。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="b9fc2-139">[原価管理単位] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="b9fc2-140">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b9fc2-140">Click Save.</span></span>
