---
title: "減価償却計算の丸め金額"
description: "この記事は、帳簿設定ページの [減価償却の丸め] フィールドについて説明します。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0ad57b076542c38d3c29dba4caacf830de6f7200
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="round-off-amount-for-depreciation-calculations"></a><span data-ttu-id="6282b-103">減価償却計算の丸め金額</span><span class="sxs-lookup"><span data-stu-id="6282b-103">Round-off amount for depreciation calculations</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6282b-104">この記事は、帳簿設定ページの [減価償却の丸め] フィールドについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6282b-104">This article discusses the Round-off depreciation field that is found on the Book setup pages.</span></span>

<span data-ttu-id="6282b-105">減価償却の丸め金額は各帳簿で設定されます。</span><span class="sxs-lookup"><span data-stu-id="6282b-105">Round-off depreciation amounts are set for each book.</span></span> <span data-ttu-id="6282b-106">減価償却の丸め金額は、固定資産の将来の減価償却と価値を示す固定資産減価償却プロファイルで使用されます。</span><span class="sxs-lookup"><span data-stu-id="6282b-106">Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals.</span></span> <span data-ttu-id="6282b-107">この帳簿で許可される減価償却の最小金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="6282b-107">Enter the lowest depreciation amount that is allowed for the book.</span></span> 

<span data-ttu-id="6282b-108">丸め設定に関係なく、最後の減価償却期間の減価償却金額の丸めはおこなわれません。</span><span class="sxs-lookup"><span data-stu-id="6282b-108">Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded.</span></span> <span data-ttu-id="6282b-109">最後の償却期間の最後に、固定資産の金額は 0 (ゼロ) になるか、または仕損価格を使用する場合は仕損価格となる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6282b-109">At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.</span></span>

### <a name="example"></a><span data-ttu-id="6282b-110">例</span><span class="sxs-lookup"><span data-stu-id="6282b-110">Example</span></span>

<span data-ttu-id="6282b-111">丸めを使用しない減価償却は、2,444.44 として計算されます。</span><span class="sxs-lookup"><span data-stu-id="6282b-111">Depreciation without rounding is calculated as 2,444.44.</span></span> <span data-ttu-id="6282b-112">次の表に示すように、丸めの設定に応じてさまざまな金額が提示されます。</span><span class="sxs-lookup"><span data-stu-id="6282b-112">As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.</span></span>

| <span data-ttu-id="6282b-113">丸め方法</span><span class="sxs-lookup"><span data-stu-id="6282b-113">Rounding method</span></span> | <span data-ttu-id="6282b-114">算出償却額</span><span class="sxs-lookup"><span data-stu-id="6282b-114">Depreciation amount</span></span> |
|-----------------|---------------------|
| <span data-ttu-id="6282b-115">0.1 の丸め</span><span class="sxs-lookup"><span data-stu-id="6282b-115">Rounding 0.1</span></span>    | <span data-ttu-id="6282b-116">2,444.40</span><span class="sxs-lookup"><span data-stu-id="6282b-116">2,444.40</span></span>            |
| <span data-ttu-id="6282b-117">1.00 の丸め</span><span class="sxs-lookup"><span data-stu-id="6282b-117">Rounding 1.00</span></span>   | <span data-ttu-id="6282b-118">2,444.00</span><span class="sxs-lookup"><span data-stu-id="6282b-118">2,444.00</span></span>            |
| <span data-ttu-id="6282b-119">10.00 の丸め</span><span class="sxs-lookup"><span data-stu-id="6282b-119">Rounding 10.00</span></span>  | <span data-ttu-id="6282b-120">2,440.00</span><span class="sxs-lookup"><span data-stu-id="6282b-120">2,440.00</span></span>            |
| <span data-ttu-id="6282b-121">100.00 の丸め</span><span class="sxs-lookup"><span data-stu-id="6282b-121">Rounding 100.00</span></span> | <span data-ttu-id="6282b-122">2,400.00</span><span class="sxs-lookup"><span data-stu-id="6282b-122">2,400.00</span></span>            |






