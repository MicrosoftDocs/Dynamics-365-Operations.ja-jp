---
title: 分割後の逓減残高による減価償却
description: このトピックでは、定率法を使用して資産を分割した後に減価償却を計算する方法 (固定資産で使用) について説明します。
author: moaamer
manager: Ann Beebe
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 615d17c71b904d426081d4c57492ba7e95c2c749
ms.sourcegitcommit: 65f9e2584c0530b1a71655aae09101691726b47f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/01/2020
ms.locfileid: "4650671"
---
# <a name="reduce-balance-depreciation-after-a-split"></a><span data-ttu-id="e8dcf-103">分割後の逓減残高による減価償却</span><span class="sxs-lookup"><span data-stu-id="e8dcf-103">Reduce balance depreciation after a split</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e8dcf-104">このトピックでは、定率法を使用して資産を他の資産に分割した後に減価償却を計算する方法 (固定資産で使用) について説明します。</span><span class="sxs-lookup"><span data-stu-id="e8dcf-104">This topic describes the method that is used in Fixed assets to calculate depreciation after an asset is split to another asset by using the reduce balance method.</span></span> <span data-ttu-id="e8dcf-105">資産帳簿で構成されている減価償却年度は会計年度です。</span><span class="sxs-lookup"><span data-stu-id="e8dcf-105">The depreciation year that is configured in the asset book is the fiscal year.</span></span> <span data-ttu-id="e8dcf-106">詳細については、[逓減残高による減価償却](reduce-balance-depreciation.md) および [固定資産の分割](tasks/split-fixed-asset.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e8dcf-106">For more information, see [Reduce balance depreciation](reduce-balance-depreciation.md) and [Split a fixed asset](tasks/split-fixed-asset.md).</span></span>

<span data-ttu-id="e8dcf-107">資産の取得時よりも後の会計年度期間中に固定資産を分割した場合、逓減残高による減価償却は、前年度の資産正味簿価額 (NBV) を含みます。</span><span class="sxs-lookup"><span data-stu-id="e8dcf-107">If you split a fixed asset during a fiscal period that is later than the period when the asset was acquired, the reduced balance depreciation will account for the asset's net book value (NBV) for the previous year.</span></span> <span data-ttu-id="e8dcf-108">また、資産を分割するトランザクションから生成された取得および減価償却調整トランザクションも含まれます。</span><span class="sxs-lookup"><span data-stu-id="e8dcf-108">It will also account for the acquisition and depreciation adjustment transactions that were generated from the transaction that split the asset.</span></span> <span data-ttu-id="e8dcf-109">この現象は、資産が 1 会計年度に取得され、将来の会計年度に分割されたことを想定しています。</span><span class="sxs-lookup"><span data-stu-id="e8dcf-109">This behavior assumes that the asset was acquired in one fiscal year and split in a later fiscal year.</span></span> <span data-ttu-id="e8dcf-110">分割後に元の資産に対して減価償却が必要な金額は、資産が分割される前の資産 NBV と、分割に対して転記された取得および減価償却調整トランザクションが反映されます。</span><span class="sxs-lookup"><span data-stu-id="e8dcf-110">The amount that must be depreciated for the original asset after the split reflects the asset's NBV before the asset was split, and the acquisition and depreciation adjustment transaction that was posted for the split.</span></span>

<span data-ttu-id="e8dcf-111">たとえば、次の条件は、</span><span class="sxs-lookup"><span data-stu-id="e8dcf-111">For example, the following conditions are in effect:</span></span>

- <span data-ttu-id="e8dcf-112">会計年度期間は 6 月 30 日から 7 月 1 日まで有効です。</span><span class="sxs-lookup"><span data-stu-id="e8dcf-112">The fiscal period is from June 30 to July 1.</span></span>
- <span data-ttu-id="e8dcf-113">逓減残高の割合は 18% で、資産は USD 10,000 の取得価格で 2019 年 6 月に取得されます。</span><span class="sxs-lookup"><span data-stu-id="e8dcf-113">The reducing balance percentage is 18 percent, and an asset is acquired in June 2019 at an acquisition price of $10,000.</span></span>
- <span data-ttu-id="e8dcf-114">最初の会計年度の減価償却は USD18,000、月々の減価償却は USD150、そして資産は 2019 年 11 月まで USD738.75 の金額で償却されます。</span><span class="sxs-lookup"><span data-stu-id="e8dcf-114">The depreciation of the first fiscal year equals $18,000, the monthly depreciation equals $150, and the asset is then depreciated until November 2019, in the amount of $738.75.</span></span>
- <span data-ttu-id="e8dcf-115">2019 年 11 月 には、資産の 80% が別の固定資産に分割されます。</span><span class="sxs-lookup"><span data-stu-id="e8dcf-115">In November 2019, 80 percent of the asset is split to another fixed asset.</span></span>

<span data-ttu-id="e8dcf-116">[![分割後の逓減残高による減価償却](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span><span class="sxs-lookup"><span data-stu-id="e8dcf-116">[![Reduce balance depreciation after a split](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span></span>

<span data-ttu-id="e8dcf-117">元の資産に対して減価償却する金額は USD1,822.25 です。</span><span class="sxs-lookup"><span data-stu-id="e8dcf-117">The amount to depreciate for the original asset is $1,822.25.</span></span> <span data-ttu-id="e8dcf-118">この金額は、分割トランザクションが転記される前の (USD9,111.25) NBV、分割トランザクション (-USD8,000) の転記中に生成される取得原価調整、分割トランザクション中 (USD711) に生成される減価償却調整と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="e8dcf-118">This amount equals the NBV before the split transaction is posted ($9,111.25), plus the acquisition adjustment that is generated during posting of the split transaction (-$8,000), plus the depreciation adjustment that is generated during the split transaction ($711).</span></span> <span data-ttu-id="e8dcf-119">したがって、2 年目の減価償却は (1,822.25 × 18 パーセント) ÷ 12 = USD27.33です。</span><span class="sxs-lookup"><span data-stu-id="e8dcf-119">Therefore, the depreciation for the second year is (1,822.25 × 18 percent) ÷ 12 = $27.33.</span></span>

<span data-ttu-id="e8dcf-120">初年度の新しい固定資産に対して減価償却する金額は (8,000 × 18 パーセント) ÷ 12 = USD120 です。</span><span class="sxs-lookup"><span data-stu-id="e8dcf-120">The amount to depreciate for the new fixed asset in the first year is (8,000 × 18 percent) ÷ 12 = $120.</span></span>
