---
title: ロイヤルティ報酬ポイントの定義
description: この手順では、ロイヤルティ報酬ポイントを定義する方法を説明します。
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyRewardPoints
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e40ebcbf3ab1befc641ae34571a8b974bd0425a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413796"
---
# <a name="define-loyalty-reward-points"></a><span data-ttu-id="1622c-103">ロイヤルティ報酬ポイントの定義</span><span class="sxs-lookup"><span data-stu-id="1622c-103">Define loyalty reward points</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1622c-104">この手順では、ロイヤルティ報酬ポイントを定義する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="1622c-104">This procedure walks through defining loyalty reward points.</span></span> <span data-ttu-id="1622c-105">ロイヤルティ プログラムを設定する前に、ロイヤルティ報酬ポイントを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1622c-105">You should set up loyalty reward points before you set up a loyalty program.</span></span> <span data-ttu-id="1622c-106">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="1622c-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="1622c-107">Retail と Commerce > 顧客 > ロイヤルティ > ロイヤルティ報酬ポイントに移動します。</span><span class="sxs-lookup"><span data-stu-id="1622c-107">Go to Retail and Commerce > Customers > Loyalty > Loyalty reward points.</span></span>
2. <span data-ttu-id="1622c-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1622c-108">Click New.</span></span>
3. <span data-ttu-id="1622c-109">[報酬ポイント ID] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1622c-109">In the Reward point ID field, type a value.</span></span>
4. <span data-ttu-id="1622c-110">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1622c-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1622c-111">[報酬ポイント タイプ] フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="1622c-111">In the Reward point type field, select an option.</span></span>
    * <span data-ttu-id="1622c-112">報酬ポイントに最も近い整数に四捨五入する場合は、[数量] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1622c-112">Select Quantity if you want the reward points to be rounded to the nearest integer.</span></span> <span data-ttu-id="1622c-113">通貨の丸めに関するルールに従って報酬ポイントが端数処理される場合は、[金額] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1622c-113">Select Amount if you want the reward points to be rounded according to currency rounding rules.</span></span> <span data-ttu-id="1622c-114">[数量] を選択した場合、この手順の次のステップは省略されます。</span><span class="sxs-lookup"><span data-stu-id="1622c-114">If you select Quantity, skip the next step of this procedure..</span></span>  
6. <span data-ttu-id="1622c-115">[通貨] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1622c-115">In the Currency field, type a value.</span></span>
    * <span data-ttu-id="1622c-116">[金額のタイプ] の報酬ポイントの場合、発行されたすべてのポイントは選択した通貨となります。</span><span class="sxs-lookup"><span data-stu-id="1622c-116">For Amount type reward points, all points issued will have the selected currency.</span></span> <span data-ttu-id="1622c-117">[数量タイプ] の報酬ポイントの場合、このフィールドは適用されません。この手順はスキップされます。</span><span class="sxs-lookup"><span data-stu-id="1622c-117">For Quantity type reward points, this field doesn't apply—skip this step.</span></span>  
7. <span data-ttu-id="1622c-118">[引換可能] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="1622c-118">Check or uncheck the Redeemable checkbox.</span></span>
8. <span data-ttu-id="1622c-119">[引換ランキング] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1622c-119">In the Redeem ranking field, enter a number.</span></span>
    * <span data-ttu-id="1622c-120">製品の支払に複数の償還可能な報酬ポイントが使用できる場合、引換ランキングが使用されます。</span><span class="sxs-lookup"><span data-stu-id="1622c-120">Redeem ranking is used when two or more redeemable reward points can be used to pay for products.</span></span> <span data-ttu-id="1622c-121">二つの報酬ポイントの引換ランキングが同じ場合、より小さなポイント数を必要とするものが使用されます。</span><span class="sxs-lookup"><span data-stu-id="1622c-121">If the two reward points have the same redeem ranking, then the one that needs to lower number of points will be used.</span></span>  
9. <span data-ttu-id="1622c-122">[有効期限の時刻] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1622c-122">In the Expiration time value field, enter a number.</span></span>
    * <span data-ttu-id="1622c-123">報酬ポイントは、指定された日数、月数、または年数、ポイントが発行された後、有効になります。</span><span class="sxs-lookup"><span data-stu-id="1622c-123">The reward points will expire the specified number of days, months, or years after when the points are issued.</span></span> <span data-ttu-id="1622c-124">「0」 という値は、ロイヤルティ報酬ポイントに有効期限がないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="1622c-124">A value of '0' means the loyalty reward points will never expire.</span></span>  
10. <span data-ttu-id="1622c-125">[有効期限の単位] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="1622c-125">In the Expiration time unit field, select an option.</span></span>
11. <span data-ttu-id="1622c-126">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1622c-126">Click Save.</span></span>

