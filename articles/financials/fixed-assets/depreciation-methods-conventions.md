---
title: 減価償却方法
description: この記事は、Microsoft Dynamics 365 for Finance and Operations にサポートされた減価償却方法および減価償却方式の概要を提供します。
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a7bce93c955ce64da129bdb1a3e9905279838c3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840628"
---
# <a name="depreciation-methods-and-conventions"></a><span data-ttu-id="d1fad-103">減価償却方法</span><span class="sxs-lookup"><span data-stu-id="d1fad-103">Depreciation methods and conventions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1fad-104">この記事は、Microsoft Dynamics 365 for Finance and Operations にサポートされた減価償却方法および減価償却方式の概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="d1fad-104">This article provides an overview of the depreciation conventions and depreciation methods that are supported by Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="d1fad-105">さまざまな減価償却方法を選択できます。</span><span class="sxs-lookup"><span data-stu-id="d1fad-105">You can select various depreciation methods and conventions.</span></span> <span data-ttu-id="d1fad-106">減価償却方法の目的は、固定資産の減価償却が可能な値を各会計年度期間に配賦することです。</span><span class="sxs-lookup"><span data-stu-id="d1fad-106">The purpose of the methods is to allocate the depreciable value of the fixed asset into fiscal periods.</span></span> <span data-ttu-id="d1fad-107">固定資産の減価償却が可能な値は、取得価格から仕損価格 (存在する場合) を差し引いた値です。</span><span class="sxs-lookup"><span data-stu-id="d1fad-107">The depreciable value of the fixed asset is the acquisition price, reduced by a scrap value, if any.</span></span> 

<span data-ttu-id="d1fad-108">減価償却法を使用している場合、ある資産の最後の減価償却日を変更すると、一部の減価償却がスキップされ、最終年度の減価償却が予定よりも多くなったり少なくなったりすることがあります。</span><span class="sxs-lookup"><span data-stu-id="d1fad-108">If you are using depreciation conventions and you modify the last depreciation run date for an asset, which then causes some depreciations to be skipped, the depreciation for the last year might be more than or less than is expected.</span></span> <span data-ttu-id="d1fad-109">減価償却は、最後の減価償却日の変更によって影響される減価償却期間の数で調整されます。</span><span class="sxs-lookup"><span data-stu-id="d1fad-109">The depreciation is adjusted by the number of depreciation periods affected by the modification of the last depreciation run date.</span></span>

<span data-ttu-id="d1fad-110">たとえば、[半年] の減価償却方法を 3 年以上採用している場合、通常は 3 年半にわたって減価償却が行われます。</span><span class="sxs-lookup"><span data-stu-id="d1fad-110">For example, if you are using the Half year depreciation convention over three years, depreciation ordinarily occurs over 3 1/2 years.</span></span> <span data-ttu-id="d1fad-111">この 3 年半の間に最後の減価償却日を変更すると、その変更の影響を受ける期間の数だけ最終年度の減価償却が移動します。</span><span class="sxs-lookup"><span data-stu-id="d1fad-111">If you change the last depreciation run date during the 3 1/2 years, the last year of depreciation moves out the number of periods affected.</span></span> <span data-ttu-id="d1fad-112">最後の減価償却日を 3 か月先送りした場合、通常であれば 6 か月分である最終年度の減価償却が 9 か月分になります。</span><span class="sxs-lookup"><span data-stu-id="d1fad-112">If you move the date by three months, the last year will have nine months’ worth of depreciation, when ordinarily there would be six months’ worth of depreciation.</span></span>

<span data-ttu-id="d1fad-113">次のいずれかの減価償却方法を選択できます。</span><span class="sxs-lookup"><span data-stu-id="d1fad-113">You can select from the following depreciation conventions.</span></span>


-   <span data-ttu-id="d1fad-114">半年</span><span class="sxs-lookup"><span data-stu-id="d1fad-114">Half year</span></span>
-   <span data-ttu-id="d1fad-115">全月</span><span class="sxs-lookup"><span data-stu-id="d1fad-115">Full month</span></span>
-   <span data-ttu-id="d1fad-116">四半期の期中</span><span class="sxs-lookup"><span data-stu-id="d1fad-116">Mid quarter</span></span>
-   <span data-ttu-id="d1fad-117">月中 (月の 1 日)</span><span class="sxs-lookup"><span data-stu-id="d1fad-117">Mid month (1st of month)</span></span>
-   <span data-ttu-id="d1fad-118">月中 (月の 15 日)</span><span class="sxs-lookup"><span data-stu-id="d1fad-118">Mid month (15th of month)</span></span>
-   <span data-ttu-id="d1fad-119">半年 (開始年)</span><span class="sxs-lookup"><span data-stu-id="d1fad-119">Half year (start of year)</span></span>
-   <span data-ttu-id="d1fad-120">半年 (来年)</span><span class="sxs-lookup"><span data-stu-id="d1fad-120">Half year (next year)</span></span>

<span data-ttu-id="d1fad-121">減価償却方法は次の中から選択できます。</span><span class="sxs-lookup"><span data-stu-id="d1fad-121">You can select from the following depreciation methods.</span></span>
-   <span data-ttu-id="d1fad-122">定額法耐用年数</span><span class="sxs-lookup"><span data-stu-id="d1fad-122">Straight line service life</span></span>
-   <span data-ttu-id="d1fad-123">逓減残高</span><span class="sxs-lookup"><span data-stu-id="d1fad-123">Reducing balance</span></span>
-   <span data-ttu-id="d1fad-124">マニュアル</span><span class="sxs-lookup"><span data-stu-id="d1fad-124">Manual</span></span>
-   <span data-ttu-id="d1fad-125">係数</span><span class="sxs-lookup"><span data-stu-id="d1fad-125">Factor</span></span>
-   <span data-ttu-id="d1fad-126">消耗</span><span class="sxs-lookup"><span data-stu-id="d1fad-126">Consumption</span></span>
-   <span data-ttu-id="d1fad-127">定額法残余耐用年数</span><span class="sxs-lookup"><span data-stu-id="d1fad-127">Straight line life remaining</span></span>
-   <span data-ttu-id="d1fad-128">200% 逓減残高</span><span class="sxs-lookup"><span data-stu-id="d1fad-128">200% reducing balance</span></span>
-   <span data-ttu-id="d1fad-129">175% 逓減残高</span><span class="sxs-lookup"><span data-stu-id="d1fad-129">175% reducing balance</span></span>
-   <span data-ttu-id="d1fad-130">150% 逓減残高</span><span class="sxs-lookup"><span data-stu-id="d1fad-130">150% reducing balance</span></span>
-   <span data-ttu-id="d1fad-131">125% 逓減残高</span><span class="sxs-lookup"><span data-stu-id="d1fad-131">125% reducing balance</span></span>





<a name="additional-resources"></a><span data-ttu-id="d1fad-132">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="d1fad-132">Additional resources</span></span>
--------

[<span data-ttu-id="d1fad-133">固定資産の減価償却</span><span class="sxs-lookup"><span data-stu-id="d1fad-133">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)

[<span data-ttu-id="d1fad-134">耐用年数定額減価償却</span><span class="sxs-lookup"><span data-stu-id="d1fad-134">Straight line service life depreciation</span></span>](Straight-line-service-life-depreciation.md)

[<span data-ttu-id="d1fad-135">減価償却費残高の削減</span><span class="sxs-lookup"><span data-stu-id="d1fad-135">Reducing balance depreciation</span></span>](reduce-balance-depreciation.md)

[<span data-ttu-id="d1fad-136">手動減価償却</span><span class="sxs-lookup"><span data-stu-id="d1fad-136">Manual depreciation</span></span>](manual-depreciation.md)

[<span data-ttu-id="d1fad-137">係数減価償却</span><span class="sxs-lookup"><span data-stu-id="d1fad-137">Factor depreciation</span></span>](factor-depreciation.md)

[<span data-ttu-id="d1fad-138">消費減価償却</span><span class="sxs-lookup"><span data-stu-id="d1fad-138">Consumption depreciation</span></span>](consumption-depreciation.md)

[<span data-ttu-id="d1fad-139">直線償却耐用年数</span><span class="sxs-lookup"><span data-stu-id="d1fad-139">Straight line life remaining depreciation</span></span>](straight-line-life-remaining-depreciation.md)

[<span data-ttu-id="d1fad-140">125% 逓減残高による減価償却</span><span class="sxs-lookup"><span data-stu-id="d1fad-140">125 percent reducing balance depreciation</span></span>](125-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="d1fad-141">150% 逓減残高による減価償却</span><span class="sxs-lookup"><span data-stu-id="d1fad-141">150 percent reducing balance depreciation</span></span>](150-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="d1fad-142">175% 逓減残高による減価償却</span><span class="sxs-lookup"><span data-stu-id="d1fad-142">175 percent reducing balance depreciation</span></span>](175-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="d1fad-143">200% 逓減残高による減価償却</span><span class="sxs-lookup"><span data-stu-id="d1fad-143">200 percent reducing balance depreciation</span></span>](200-percent-reducing-balance-depreciation.md)



