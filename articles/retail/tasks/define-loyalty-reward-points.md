--- 
title: "ロイヤルティ報酬ポイントの定義"
description: "この手順では、ロイヤルティ報酬ポイントを定義する方法を説明します。"
author: scott-tucker
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 07fa9b2afd40305fc95e8c49428c5b1ccb177f1d
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="define-loyalty-reward-points"></a><span data-ttu-id="5cf98-103">ロイヤルティ報酬ポイントの定義</span><span class="sxs-lookup"><span data-stu-id="5cf98-103">Define loyalty reward points</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="5cf98-104">この手順では、ロイヤルティ報酬ポイントを定義する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="5cf98-104">This procedure walks through defining loyalty reward points.</span></span> <span data-ttu-id="5cf98-105">ロイヤルティ プログラムを設定する前に、ロイヤルティ報酬ポイントを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5cf98-105">You should set up loyalty reward points before you set up a loyalty program.</span></span> <span data-ttu-id="5cf98-106">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="5cf98-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="5cf98-107">[小売りとコマース] > [顧客] > [ロイヤルティ] > [ロイヤルティ報酬ポイント] に移動します。</span><span class="sxs-lookup"><span data-stu-id="5cf98-107">Go to Retail and commerce > Customers > Loyalty > Loyalty reward points.</span></span>
2. <span data-ttu-id="5cf98-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5cf98-108">Click New.</span></span>
3. <span data-ttu-id="5cf98-109">[報酬ポイント ID] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5cf98-109">In the Reward point ID field, type a value.</span></span>
4. <span data-ttu-id="5cf98-110">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5cf98-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5cf98-111">[報酬ポイント タイプ] フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="5cf98-111">In the Reward point type field, select an option.</span></span>
    * <span data-ttu-id="5cf98-112">報酬ポイントに最も近い整数に四捨五入する場合は、[数量] を選択します。</span><span class="sxs-lookup"><span data-stu-id="5cf98-112">Select Quantity if you want the reward points to be rounded to the nearest integer.</span></span> <span data-ttu-id="5cf98-113">通貨の丸めに関するルールに従って報酬ポイントが端数処理される場合は、[金額] を選択します。</span><span class="sxs-lookup"><span data-stu-id="5cf98-113">Select Amount if you want the reward points to be rounded according to currency rounding rules.</span></span> <span data-ttu-id="5cf98-114">[数量] を選択した場合、この手順の次のステップは省略されます。</span><span class="sxs-lookup"><span data-stu-id="5cf98-114">If you select Quantity, skip the next step of this procedure..</span></span>  
6. <span data-ttu-id="5cf98-115">[通貨] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5cf98-115">In the Currency field, type a value.</span></span>
    * <span data-ttu-id="5cf98-116">[金額のタイプ] の報酬ポイントの場合、発行されたすべてのポイントは選択した通貨となります。</span><span class="sxs-lookup"><span data-stu-id="5cf98-116">For Amount type reward points, all points issued will have the selected currency.</span></span> <span data-ttu-id="5cf98-117">[数量タイプ] の報酬ポイントの場合、このフィールドは適用されません。この手順はスキップされます。</span><span class="sxs-lookup"><span data-stu-id="5cf98-117">For Quantity type reward points, this field doesn't apply—skip this step.</span></span>  
7. <span data-ttu-id="5cf98-118">[引換可能] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="5cf98-118">Check or uncheck the Redeemable checkbox.</span></span>
8. <span data-ttu-id="5cf98-119">[引換ランキング] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5cf98-119">In the Redeem ranking field, enter a number.</span></span>
    * <span data-ttu-id="5cf98-120">製品の支払に複数の償還可能な報酬ポイントが使用できる場合、引換ランキングが使用されます。</span><span class="sxs-lookup"><span data-stu-id="5cf98-120">Redeem ranking is used when two or more redeemable reward points can be used to pay for products.</span></span> <span data-ttu-id="5cf98-121">二つの報酬ポイントの引換ランキングが同じ場合、より小さなポイント数を必要とするものが使用されます。</span><span class="sxs-lookup"><span data-stu-id="5cf98-121">If the two reward points have the same redeem ranking, then the one that needs to lower number of points will be used.</span></span>  
9. <span data-ttu-id="5cf98-122">[有効期限の時刻] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5cf98-122">In the Expiration time value field, enter a number.</span></span>
    * <span data-ttu-id="5cf98-123">報酬ポイントは、指定された日数、月数、または年数、ポイントが発行された後、有効になります。</span><span class="sxs-lookup"><span data-stu-id="5cf98-123">The reward points will expire the specified number of days, months, or years after when the points are issued.</span></span> <span data-ttu-id="5cf98-124">「0」という値は、ロイヤルティ報酬ポイントに有効期限がないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="5cf98-124">A value of ‘0’ means the loyalty reward points will never expire.</span></span>  
10. <span data-ttu-id="5cf98-125">[有効期限の単位] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="5cf98-125">In the Expiration time unit field, select an option.</span></span>
11. <span data-ttu-id="5cf98-126">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5cf98-126">Click Save.</span></span>


