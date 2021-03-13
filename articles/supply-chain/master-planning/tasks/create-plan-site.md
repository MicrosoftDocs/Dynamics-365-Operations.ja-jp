---
title: サイトの計画の作成
description: 生産計画担当者は、特定品目を生産するための材料と能力要件を計算します。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1b6d433257056c604500953060bf11ce3a3f5866
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007944"
---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="fbbf3-103">サイトの計画の作成</span><span class="sxs-lookup"><span data-stu-id="fbbf3-103">Create a plan for a site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fbbf3-104">生産計画担当者は、特定品目を生産するための材料と能力要件を計算します。</span><span class="sxs-lookup"><span data-stu-id="fbbf3-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="fbbf3-105">調達提案が作成された後、計画している注文を検索し、注文を確定し、緊急を要する注文から始めます。</span><span class="sxs-lookup"><span data-stu-id="fbbf3-105">After the sourcing suggestions are created, he finds the orders at the site for which he is planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="fbbf3-106">最も緊急な注文とは、現在の日付で確定される必要があるものです。</span><span class="sxs-lookup"><span data-stu-id="fbbf3-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="fbbf3-107">デモ データの会社 USMF を使用して、これらのタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="fbbf3-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="fbbf3-108">品目の材料および能力計画を作成します</span><span class="sxs-lookup"><span data-stu-id="fbbf3-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="fbbf3-109">[マスター プラン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbbf3-109">Click Master planning.</span></span>
    * <span data-ttu-id="fbbf3-110">既定のダッシュボードに移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbbf3-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="fbbf3-111">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbbf3-111">Click Run.</span></span>
3. <span data-ttu-id="fbbf3-112">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="fbbf3-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="fbbf3-113">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbbf3-113">Click Filter.</span></span>
5. <span data-ttu-id="fbbf3-114">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="fbbf3-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="fbbf3-115">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="fbbf3-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="fbbf3-116">例: D0001</span><span class="sxs-lookup"><span data-stu-id="fbbf3-116">Example: D0001</span></span>  
7. <span data-ttu-id="fbbf3-117">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbbf3-117">Click OK.</span></span>
8. <span data-ttu-id="fbbf3-118">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbbf3-118">Click OK.</span></span>
    * <span data-ttu-id="fbbf3-119">これには数分かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="fbbf3-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="fbbf3-120">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="fbbf3-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="fbbf3-121">品目の緊急計画注文を識別します</span><span class="sxs-lookup"><span data-stu-id="fbbf3-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="fbbf3-122">[品目番号列] フィルターを開きます。</span><span class="sxs-lookup"><span data-stu-id="fbbf3-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="fbbf3-123">[品目番号] フィールドで "次の値で始まる" フィルター演算子を使用して、値 "D0001" でフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="fbbf3-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="fbbf3-124">[注文の日付列フィルター] を開きます。</span><span class="sxs-lookup"><span data-stu-id="fbbf3-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="fbbf3-125">[次の値と完全に一致する] フィルタ演算子を使用して、[注文日付] フィールドに値「現在の日付」でフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="fbbf3-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="fbbf3-126">品目のすべての緊急注文を確定します</span><span class="sxs-lookup"><span data-stu-id="fbbf3-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="fbbf3-127">一覧で、すべての行のマークを設定または解除します。</span><span class="sxs-lookup"><span data-stu-id="fbbf3-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="fbbf3-128">[確定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbbf3-128">Click Firm.</span></span>
3. <span data-ttu-id="fbbf3-129">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbbf3-129">Click OK.</span></span>

