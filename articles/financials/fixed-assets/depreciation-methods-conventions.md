---
title: "減価償却方法"
description: "この記事は、Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition にサポートされた減価償却方法および減価償却方式の概要を提供します。"
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 69e0decd3ffbdf1f64fa4fbfe070927990f880ad
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="depreciation-methods-and-conventions"></a><span data-ttu-id="da0f1-103">減価償却方法</span><span class="sxs-lookup"><span data-stu-id="da0f1-103">Depreciation methods and conventions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="da0f1-104">この記事は、Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition にサポートされた減価償却方法および減価償却方式の概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="da0f1-104">This article provides an overview of the depreciation conventions and depreciation methods that are supported by Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

<span data-ttu-id="da0f1-105">さまざまな減価償却方法を選択できます。</span><span class="sxs-lookup"><span data-stu-id="da0f1-105">You can select various depreciation methods and conventions.</span></span> <span data-ttu-id="da0f1-106">減価償却方法の目的は、固定資産の減価償却が可能な値を各会計年度期間に配賦することです。</span><span class="sxs-lookup"><span data-stu-id="da0f1-106">The purpose of the methods is to allocate the depreciable value of the fixed asset into fiscal periods.</span></span> <span data-ttu-id="da0f1-107">固定資産の減価償却が可能な値は、取得価格から仕損価格 (存在する場合) を差し引いた値です。</span><span class="sxs-lookup"><span data-stu-id="da0f1-107">The depreciable value of the fixed asset is the acquisition price, reduced by a scrap value, if any.</span></span> 

<span data-ttu-id="da0f1-108">減価償却法を使用している場合、ある資産の最後の減価償却日を変更すると、一部の減価償却がスキップされ、最終年度の減価償却が予定よりも多くなったり少なくなったりすることがあります。</span><span class="sxs-lookup"><span data-stu-id="da0f1-108">If you are using depreciation conventions and you modify the last depreciation run date for an asset, which then causes some depreciations to be skipped, the depreciation for the last year might be more than or less than is expected.</span></span> <span data-ttu-id="da0f1-109">減価償却は、最後の減価償却日の変更によって影響される減価償却期間の数で調整されます。</span><span class="sxs-lookup"><span data-stu-id="da0f1-109">The depreciation is adjusted by the number of depreciation periods affected by the modification of the last depreciation run date.</span></span>

<span data-ttu-id="da0f1-110">たとえば、[半年] の減価償却方法を 3 年以上採用している場合、通常は 3 年半にわたって減価償却が行われます。</span><span class="sxs-lookup"><span data-stu-id="da0f1-110">For example, if you are using the Half year depreciation convention over three years, depreciation ordinarily occurs over 3 1/2 years.</span></span> <span data-ttu-id="da0f1-111">この 3 年半の間に最後の減価償却日を変更すると、その変更の影響を受ける期間の数だけ最終年度の減価償却が移動します。</span><span class="sxs-lookup"><span data-stu-id="da0f1-111">If you change the last depreciation run date during the 3 1/2 years, the last year of depreciation moves out the number of periods affected.</span></span> <span data-ttu-id="da0f1-112">最後の減価償却日を 3 か月先送りした場合、通常であれば 6 か月分である最終年度の減価償却が 9 か月分になります。</span><span class="sxs-lookup"><span data-stu-id="da0f1-112">If you move the date by three months, the last year will have nine months’ worth of depreciation, when ordinarily there would be six months’ worth of depreciation.</span></span>

<span data-ttu-id="da0f1-113">次のいずれかの減価償却方法を選択できます。</span><span class="sxs-lookup"><span data-stu-id="da0f1-113">You can select from the following depreciation conventions.</span></span>


-   <span data-ttu-id="da0f1-114">半年</span><span class="sxs-lookup"><span data-stu-id="da0f1-114">Half year</span></span>
-   <span data-ttu-id="da0f1-115">全月</span><span class="sxs-lookup"><span data-stu-id="da0f1-115">Full month</span></span>
-   <span data-ttu-id="da0f1-116">四半期の期中</span><span class="sxs-lookup"><span data-stu-id="da0f1-116">Mid quarter</span></span>
-   <span data-ttu-id="da0f1-117">月中 (月の 1 日)</span><span class="sxs-lookup"><span data-stu-id="da0f1-117">Mid month (1st of month)</span></span>
-   <span data-ttu-id="da0f1-118">月中 (月の 15 日)</span><span class="sxs-lookup"><span data-stu-id="da0f1-118">Mid month (15th of month)</span></span>
-   <span data-ttu-id="da0f1-119">半年 (開始年)</span><span class="sxs-lookup"><span data-stu-id="da0f1-119">Half year (start of year)</span></span>
-   <span data-ttu-id="da0f1-120">半年 (来年)</span><span class="sxs-lookup"><span data-stu-id="da0f1-120">Half year (next year)</span></span>

<span data-ttu-id="da0f1-121">減価償却方法は次の中から選択できます。</span><span class="sxs-lookup"><span data-stu-id="da0f1-121">You can select from the following depreciation methods.</span></span>
-   <span data-ttu-id="da0f1-122">定額法耐用年数</span><span class="sxs-lookup"><span data-stu-id="da0f1-122">Straight line service life</span></span>
-   <span data-ttu-id="da0f1-123">逓減残高</span><span class="sxs-lookup"><span data-stu-id="da0f1-123">Reducing balance</span></span>
-   <span data-ttu-id="da0f1-124">マニュアル</span><span class="sxs-lookup"><span data-stu-id="da0f1-124">Manual</span></span>
-   <span data-ttu-id="da0f1-125">係数</span><span class="sxs-lookup"><span data-stu-id="da0f1-125">Factor</span></span>
-   <span data-ttu-id="da0f1-126">消耗</span><span class="sxs-lookup"><span data-stu-id="da0f1-126">Consumption</span></span>
-   <span data-ttu-id="da0f1-127">定額法残余耐用年数</span><span class="sxs-lookup"><span data-stu-id="da0f1-127">Straight line life remaining</span></span>
-   <span data-ttu-id="da0f1-128">200% 逓減残高</span><span class="sxs-lookup"><span data-stu-id="da0f1-128">200% reducing balance</span></span>
-   <span data-ttu-id="da0f1-129">175% 逓減残高</span><span class="sxs-lookup"><span data-stu-id="da0f1-129">175% reducing balance</span></span>
-   <span data-ttu-id="da0f1-130">150% 逓減残高</span><span class="sxs-lookup"><span data-stu-id="da0f1-130">150% reducing balance</span></span>
-   <span data-ttu-id="da0f1-131">125% 逓減残高</span><span class="sxs-lookup"><span data-stu-id="da0f1-131">125% reducing balance</span></span>

 



<a name="see-also"></a><span data-ttu-id="da0f1-132">参照</span><span class="sxs-lookup"><span data-stu-id="da0f1-132">See also</span></span>
--------

[<span data-ttu-id="da0f1-133">固定資産減価償却</span><span class="sxs-lookup"><span data-stu-id="da0f1-133">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)

[<span data-ttu-id="da0f1-134">直線償却耐用年数</span><span class="sxs-lookup"><span data-stu-id="da0f1-134">Straight line service life depreciation</span></span>](Straight-line-service-life-depreciation.md)

[<span data-ttu-id="da0f1-135">減価償却費残高の削減</span><span class="sxs-lookup"><span data-stu-id="da0f1-135">Reducing balance depreciation</span></span>](reduce-balance-depreciation.md)

[<span data-ttu-id="da0f1-136">手動減価償却</span><span class="sxs-lookup"><span data-stu-id="da0f1-136">Manual depreciation</span></span>](manual-depreciation.md)

[<span data-ttu-id="da0f1-137">係数減価償却</span><span class="sxs-lookup"><span data-stu-id="da0f1-137">Factor depreciation</span></span>](factor-depreciation.md)

[<span data-ttu-id="da0f1-138">消費減価償却</span><span class="sxs-lookup"><span data-stu-id="da0f1-138">Consumption depreciation</span></span>](consumption-depreciation.md)

[<span data-ttu-id="da0f1-139">直線償却耐用年数</span><span class="sxs-lookup"><span data-stu-id="da0f1-139">Straight line life remaining depreciation</span></span>](straight-line-life-remaining-depreciation.md)

[<span data-ttu-id="da0f1-140">125% 逓減残高による減価償却</span><span class="sxs-lookup"><span data-stu-id="da0f1-140">125 percent reducing balance depreciation</span></span>](125-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="da0f1-141">150% 逓減残高による減価償却</span><span class="sxs-lookup"><span data-stu-id="da0f1-141">150 percent reducing balance depreciation</span></span>](150-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="da0f1-142">175% 逓減残高による減価償却</span><span class="sxs-lookup"><span data-stu-id="da0f1-142">175 percent reducing balance depreciation</span></span>](175-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="da0f1-143">200% 逓減残高による減価償却</span><span class="sxs-lookup"><span data-stu-id="da0f1-143">200 percent reducing balance depreciation</span></span>](200-percent-reducing-balance-depreciation.md)




