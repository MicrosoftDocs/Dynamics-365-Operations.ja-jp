---
title: 制約付き計画の生成
description: このトピックでは、材料制約と能力制約の両方を考慮した計画の作成方法を説明します。
author: ShylaThompson
manager: tfehr
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8b9d5712dd1b4f9958de775e1a2224b64485d05
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431984"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="8603d-103">制約付き計画の生成</span><span class="sxs-lookup"><span data-stu-id="8603d-103">Generate a constrained plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8603d-104">このトピックでは、材料制約と能力制約の両方を考慮した計画の作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="8603d-104">This topic explains how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="8603d-105">計画により、材料が利用可能でないうちに生産が開始しないように、またリソースが予約超過にならないようにします。</span><span class="sxs-lookup"><span data-stu-id="8603d-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="8603d-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="8603d-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8603d-107">この手順は、生産の計画者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="8603d-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="8603d-108">制約付き計画の設定</span><span class="sxs-lookup"><span data-stu-id="8603d-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="8603d-109">ホーム ページで、**マスター プラン** ワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="8603d-109">In the home page, select the **Master planning** workspace.</span></span>
2. <span data-ttu-id="8603d-110">ワークスペースの右側にあるリンクの一覧から、**マスター プラン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8603d-110">Select **Master plans** in the list of links on the far right side of the workspace.</span></span>
3. <span data-ttu-id="8603d-111">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="8603d-111">In the list, find and select the desired record.</span></span> <span data-ttu-id="8603d-112">例: **StaticPlan**</span><span class="sxs-lookup"><span data-stu-id="8603d-112">Example: **StaticPlan**</span></span>  
4. <span data-ttu-id="8603d-113">**有限能力** フィールドで **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8603d-113">Select **Yes** in the **Finite capacity** field.</span></span>
5. <span data-ttu-id="8603d-114">**有限能力タイム フェンス** フィールドに `30` と入力します。</span><span class="sxs-lookup"><span data-stu-id="8603d-114">In the **Finite capacity time fence** field, enter `30`.</span></span>
6. <span data-ttu-id="8603d-115">**タイム フェンス (日)** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="8603d-115">Expand the **Time fences in days** section.</span></span>
7. <span data-ttu-id="8603d-116">**能力** フィールドで **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8603d-116">Select **Yes** in the **Capacity** field.</span></span>
8. <span data-ttu-id="8603d-117">**能力スケジューリング タイム フェンス (日)** フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8603d-117">In the **Capacity scheduling time fence (days)** field, enter a number.</span></span> <span data-ttu-id="8603d-118">例: `60`</span><span class="sxs-lookup"><span data-stu-id="8603d-118">Example: `60`</span></span>  
9. <span data-ttu-id="8603d-119">**計算済遅延** フィールドで、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8603d-119">Select **Yes** in the **Calculated delays** field.</span></span>
10. <span data-ttu-id="8603d-120">**遅延の計算タイム フェンス (日)** フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8603d-120">In the **Calculate delays time fence (days)** field, enter a number.</span></span> <span data-ttu-id="8603d-121">例: `60`</span><span class="sxs-lookup"><span data-stu-id="8603d-121">Example: `60`</span></span> 
11. <span data-ttu-id="8603d-122">**計算済遅延** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="8603d-122">Expand the **Calculated delays** section.</span></span>
12. <span data-ttu-id="8603d-123">**計算済遅延を要求日に追加** フィールドで **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8603d-123">Select **Yes** in all **Add the calculated delay to the requirement date** fields.</span></span>
13. <span data-ttu-id="8603d-124">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8603d-124">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="8603d-125">制約付き計画の作成</span><span class="sxs-lookup"><span data-stu-id="8603d-125">Create a constrained plan</span></span>
1. <span data-ttu-id="8603d-126">**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8603d-126">Select **Run**.</span></span>
2. <span data-ttu-id="8603d-127">**マスター プラン** フィールドで、制約を設定した計画を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="8603d-127">In the **Master plan** field, enter or select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="8603d-128">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8603d-128">Select **OK**.</span></span>
4. <span data-ttu-id="8603d-129">**計画オーダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8603d-129">Select **Planned orders**.</span></span>

