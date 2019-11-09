---
title: 日本の均等償却方法
description: 日本では、一括比例配分資産、低価額資産、および繰延資産は耐用年数期間中、毎年均等額で減価償却されます。 この記事は、均等減価償却についてよく寄せられる質問に回答します。
author: yijialuan
manager: AnnBe
ms.date: 03/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 10154
ms.assetid: da3d689f-3625-4896-a74a-7890e4fa26eb
ms.search.region: Japan
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 98bbff9aaf1bbd1a112cbae4dd5ed905ecd0c25a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175797"
---
# <a name="equally-divided-depreciation-method-for-japan"></a><span data-ttu-id="47131-104">日本の均等償却方法</span><span class="sxs-lookup"><span data-stu-id="47131-104">Equally divided depreciation method for Japan</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47131-105">日本では、一括比例配分資産、低価額資産、および繰延資産は耐用年数期間中、毎年均等額で減価償却されます。</span><span class="sxs-lookup"><span data-stu-id="47131-105">In Japan, lump-sum assets, low-value assets, and deferred assets are depreciated in equal amounts in each year of the service life.</span></span> <span data-ttu-id="47131-106">この記事は、均等減価償却についてよく寄せられる質問に回答します。</span><span class="sxs-lookup"><span data-stu-id="47131-106">This article answers some frequently asked questions about equally divided depreciation.</span></span>

<span data-ttu-id="47131-107">均等償却予定表で、固定資産の耐用年数内の 1 つまたは複数の会計年度期間の、繰延、少額、または一括比例配分の固定資産を均等減価償却できます。</span><span class="sxs-lookup"><span data-stu-id="47131-107">Equally divided depreciation lets you depreciate a deferred, low-value, or lump-sum fixed asset equally over one or more fiscal periods within the useful life of the fixed asset.</span></span> <span data-ttu-id="47131-108">**減価償却プロファイル** ページで均等減価償却法を設定できます。</span><span class="sxs-lookup"><span data-stu-id="47131-108">You can set up the equally divided depreciation method on the **Depreciation profiles** page.</span></span>

## <a name="what-types-of-fixed-assets-can-i-depreciate-by-using-the-equally-divided-depreciation-method"></a><span data-ttu-id="47131-109">均等減価償却法を使用して、どの固定資産の種類を減価償却できますか。</span><span class="sxs-lookup"><span data-stu-id="47131-109">What types of fixed assets can I depreciate by using the equally divided depreciation method?</span></span>
<span data-ttu-id="47131-110">均等減価償却法を使用して、繰延、少額、および一括比例配分の固定資産を減価償却できます。</span><span class="sxs-lookup"><span data-stu-id="47131-110">You can use the equally divided depreciation method to depreciate deferred, low-value, and lump-sum fixed assets.</span></span> <span data-ttu-id="47131-111">次に、一つ以上の会計年度期間における資産の減価償却費を表示するレポートを生成できます。</span><span class="sxs-lookup"><span data-stu-id="47131-111">You can then generate reports to view the depreciation expenses for the assets over one or more fiscal periods.</span></span>

## <a name="how-is-depreciation-calculated-using-the-equally-divided-depreciation-method"></a><span data-ttu-id="47131-112">均等減価償却法を使用して、どのように減価償却を計算しますか。</span><span class="sxs-lookup"><span data-stu-id="47131-112">How is depreciation calculated using the equally divided depreciation method?</span></span>
<span data-ttu-id="47131-113">**減価償却プロファイル** ページの**方式**フィールドで、減価償却方法として**均等**を選択して、減価償却プロファイルを設定できます。</span><span class="sxs-lookup"><span data-stu-id="47131-113">You can set up a depreciation profile by selecting **Equally divided** as the depreciation method in the **Method** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="47131-114">均等減価償却プロファイルを使用して固定資産を減価償却するとき、次の式を使用して減価償却金額を計算します。減価償却 = 残余量 × 四捨五入した (1 ÷ 残りの年数) × 四捨五入した (1 ÷ 現在の年の期間数)。次の式は、残りの量の計算に使用します。残余量 = 取得コスト – 減価償却累計額。減価償却量の計算に均等減価償却法を使用するとき、**減価償却プロファイル**ページの**均等償却年数**フィールドの値は、**帳簿**ページで指定した耐用年数および減価償却期間ではなく、固定資産の耐用年数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="47131-114">When you use the equally divided depreciation profile to depreciate a fixed asset, depreciation amounts are calculated by using the following formula: Depreciation = Remaining amount × rounding (1 ÷ Number of remaining years) × rounding (1 ÷ Number of periods in the current year) The following formula is used to calculate the remaining amount: Remaining amount = Acquisition cost – Accumulated depreciation When you use the equally divided depreciation method to calculate the depreciation amount, the value in the **Number of years to equally divide depreciation amounts** field on the **Depreciation profiles** page indicates the useful life of the fixed asset instead of the service life and the depreciation period that you specified on the **Books** page.</span></span>

## <a name="does-the-depreciation-amount-that-is-calculated-by-using-the-equally-divided-depreciation-method-change-if-its-calculated-at-the-beginning-of-the-month-instead-of-in-the-middle-of-the-month"></a><span data-ttu-id="47131-115">均等減価償却法を使用して計算された減価償却量は、月の中間に計算された場合ではなく月初めに計算された場合に異なりますか。</span><span class="sxs-lookup"><span data-stu-id="47131-115">Does the depreciation amount that is calculated by using the equally divided depreciation method change if it's calculated at the beginning of the month instead of in the middle of the month?</span></span>
<span data-ttu-id="47131-116">一連番号</span><span class="sxs-lookup"><span data-stu-id="47131-116">No.</span></span> <span data-ttu-id="47131-117">減価償却量は、月内のいつ計算されるかによって変化しません。</span><span class="sxs-lookup"><span data-stu-id="47131-117">The depreciation amount does not change, depending upon when it's calculated during the month.</span></span> <span data-ttu-id="47131-118">たとえば、以下の一括比例配分の固定資産を取得します。</span><span class="sxs-lookup"><span data-stu-id="47131-118">For example, you acquire a lump-sum fixed asset:</span></span>

-   <span data-ttu-id="47131-119">一括比例配分の固定資産の取得値 = 150,000 円 (JPY)</span><span class="sxs-lookup"><span data-stu-id="47131-119">Acquisition value of the lump-sum fixed asset = 150,000 Japanese yen (JPY)</span></span>
-   <span data-ttu-id="47131-120">取得日付 = April 1, 2013</span><span class="sxs-lookup"><span data-stu-id="47131-120">Acquisition date = April 1, 2013</span></span>
-   <span data-ttu-id="47131-121">均等減価償却量に対する年数 = 3 年</span><span class="sxs-lookup"><span data-stu-id="47131-121">Number of years to equally divide the depreciation amount = 3 years</span></span>

<span data-ttu-id="47131-122">均等減価償却法を使用すると、計算が月初めまたは月の中間にかかわらず、この固定資産の各月の減価償却量は JPY 4,166.67 です。</span><span class="sxs-lookup"><span data-stu-id="47131-122">When the equally divided depreciation method is used, the depreciation amount for this fixed asset is JPY 4,166.67 for each month, regardless of whether you calculate it at the beginning of the month or in the middle of the month.</span></span>

## <a name="how-is-equally-divided-depreciation-calculated-for-a-lowvalue-asset-that-is-acquired-midyear"></a><span data-ttu-id="47131-123">年の中ごろに取得された低価格資産の均等減価償却を、どのように計算しますか。</span><span class="sxs-lookup"><span data-stu-id="47131-123">How is equally divided depreciation calculated for a lowvalue asset that is acquired midyear?</span></span>
<span data-ttu-id="47131-124">会計年度の中ごろに低価額の固定資産を購入した場合、Dynamics 365 Finance は、現在の会計年度を減価償却計算の最初の会計年度であると仮定します。</span><span class="sxs-lookup"><span data-stu-id="47131-124">If you purchase a low-value fixed asset in the middle of a fiscal year, Dynamics 365 Finance considers the current fiscal year to be the first fiscal year for the depreciation calculation.</span></span> <span data-ttu-id="47131-125">たとえば、会計年度の中ごろに、低価額の固定資産を取得します。</span><span class="sxs-lookup"><span data-stu-id="47131-125">For example, you acquire a low-value fixed asset in the middle of a fiscal year:</span></span>

-   <span data-ttu-id="47131-126">会計年度 = 4 月 1 日から 3 月 31 日</span><span class="sxs-lookup"><span data-stu-id="47131-126">Fiscal year = April 1 to March 31</span></span>
-   <span data-ttu-id="47131-127">低価格固定資産の取得値 = JPY 100,000</span><span class="sxs-lookup"><span data-stu-id="47131-127">Acquisition value of the low-value fixed asset = JPY 100,000</span></span>
-   <span data-ttu-id="47131-128">取得日付け= 2012 年 12 月 1 日</span><span class="sxs-lookup"><span data-stu-id="47131-128">Acquisition date = December 1, 2012</span></span>
-   <span data-ttu-id="47131-129">均等減価償却量に対する年数 = 1 年</span><span class="sxs-lookup"><span data-stu-id="47131-129">Number of years to equally divide the depreciation amount = 1 year</span></span>

<span data-ttu-id="47131-130">次の表に示すように、2012 年 4 月 1 日から 2013 年 3 月 31 日までの会計年に対し、減価償却を計算します。</span><span class="sxs-lookup"><span data-stu-id="47131-130">The depreciation for the fiscal year from April 1, 2012, to March 31, 2013, is calculated as shown in the following table.</span></span>

| <span data-ttu-id="47131-131">入社日</span><span class="sxs-lookup"><span data-stu-id="47131-131">Start date</span></span>    | <span data-ttu-id="47131-132">終了日</span><span class="sxs-lookup"><span data-stu-id="47131-132">End date</span></span>       | <span data-ttu-id="47131-133">会計年度期間の減価償却量</span><span class="sxs-lookup"><span data-stu-id="47131-133">Depreciation amount for the fiscal period</span></span> | <span data-ttu-id="47131-134">減価償却累計額</span><span class="sxs-lookup"><span data-stu-id="47131-134">Accumulated depreciation</span></span> | <span data-ttu-id="47131-135">残りの減価償却量</span><span class="sxs-lookup"><span data-stu-id="47131-135">Remaining depreciation amount</span></span> | <span data-ttu-id="47131-136">その月の減価償却量</span><span class="sxs-lookup"><span data-stu-id="47131-136">Depreciation amount for the month</span></span> |
|---------------|----------------|-------------------------------------------|--------------------------|-------------------------------|-----------------------------------|
| <span data-ttu-id="47131-137">2012 年 4 月 1 日</span><span class="sxs-lookup"><span data-stu-id="47131-137">April 1, 2012</span></span> | <span data-ttu-id="47131-138">2013 年 3 月 31 日</span><span class="sxs-lookup"><span data-stu-id="47131-138">March 31, 2013</span></span> | <span data-ttu-id="47131-139">JPY 100,000</span><span class="sxs-lookup"><span data-stu-id="47131-139">JPY 100,000</span></span>                               | <span data-ttu-id="47131-140">JPY 100,000</span><span class="sxs-lookup"><span data-stu-id="47131-140">JPY 100,000</span></span>              | <span data-ttu-id="47131-141">0</span><span class="sxs-lookup"><span data-stu-id="47131-141">0</span></span>                             | <span data-ttu-id="47131-142">JPY 100,000</span><span class="sxs-lookup"><span data-stu-id="47131-142">JPY 100, 000</span></span>                      |

## <a name="how-is-equally-divided-depreciation-calculated-for-a-lumpsum-asset-that-is-acquired-midyear"></a><span data-ttu-id="47131-143">年の中ごろに取得された一括比例配分資産の均等減価償却を、どのように計算しますか。</span><span class="sxs-lookup"><span data-stu-id="47131-143">How is equally divided depreciation calculated for a lumpsum asset that is acquired midyear?</span></span>
<span data-ttu-id="47131-144">会計年度の中ごろに一括比例配分の固定資産を購入した場合、Finance は固定資産の購買日付から現在の会計年度を計算します。</span><span class="sxs-lookup"><span data-stu-id="47131-144">If you purchase a lump-sum fixed asset in the middle of a fiscal year, Finance calculates the current fiscal year from the purchase date of the fixed asset.</span></span> <span data-ttu-id="47131-145">たとえば、会計年度の中ごろに、一括比例配分の固定資産を取得します。</span><span class="sxs-lookup"><span data-stu-id="47131-145">For example, you acquire a lump-sum fixed asset in the middle of a fiscal year:</span></span>

-   <span data-ttu-id="47131-146">会計年度 = 4 月 1 日から 3 月 31 日</span><span class="sxs-lookup"><span data-stu-id="47131-146">Fiscal year = April 1 to March 31</span></span>
-   <span data-ttu-id="47131-147">一括比例配分の固定資産の取得値 = JPY 150,000</span><span class="sxs-lookup"><span data-stu-id="47131-147">Acquisition value of the lump-sum fixed asset = JPY 150,000</span></span>
-   <span data-ttu-id="47131-148">取得日付け= 2012 年 12 月 1 日</span><span class="sxs-lookup"><span data-stu-id="47131-148">Acquisition date = December 1, 2012</span></span>
-   <span data-ttu-id="47131-149">均等減価償却量に対する年数 = 3 年</span><span class="sxs-lookup"><span data-stu-id="47131-149">Number of years to equally divide the depreciation amount = 3 years</span></span>

<span data-ttu-id="47131-150">次の表に示すように、2012 年 12 月 1 日から 2013 年 3 月 31 日までの初年度に対し、減価償却を計算します。</span><span class="sxs-lookup"><span data-stu-id="47131-150">The depreciation for the first year from December 1, 2012, to March 31, 2013, is calculated as shown in the following table.</span></span>

| <span data-ttu-id="47131-151">入社日</span><span class="sxs-lookup"><span data-stu-id="47131-151">Start date</span></span>       | <span data-ttu-id="47131-152">終了日</span><span class="sxs-lookup"><span data-stu-id="47131-152">End date</span></span>       | <span data-ttu-id="47131-153">会計年度期間の減価償却量</span><span class="sxs-lookup"><span data-stu-id="47131-153">Depreciation amount for a fiscal period</span></span> | <span data-ttu-id="47131-154">減価償却累計額</span><span class="sxs-lookup"><span data-stu-id="47131-154">Accumulated depreciation</span></span> | <span data-ttu-id="47131-155">残りの減価償却量</span><span class="sxs-lookup"><span data-stu-id="47131-155">Remaining depreciation amount</span></span> | <span data-ttu-id="47131-156">月の減価償却量</span><span class="sxs-lookup"><span data-stu-id="47131-156">Depreciation amount for a month</span></span> |
|------------------|----------------|-----------------------------------------|--------------------------|-------------------------------|---------------------------------|
| <span data-ttu-id="47131-157">2012 年 12 月 1 日</span><span class="sxs-lookup"><span data-stu-id="47131-157">December 1, 2012</span></span> | <span data-ttu-id="47131-158">2013 年 3 月 31 日</span><span class="sxs-lookup"><span data-stu-id="47131-158">March 31, 2013</span></span> | <span data-ttu-id="47131-159">JPY 50,000</span><span class="sxs-lookup"><span data-stu-id="47131-159">JPY 50,000</span></span>                              | <span data-ttu-id="47131-160">JPY 50,000</span><span class="sxs-lookup"><span data-stu-id="47131-160">JPY 50,000</span></span>               | <span data-ttu-id="47131-161">JPY 100,000</span><span class="sxs-lookup"><span data-stu-id="47131-161">JPY 100,000</span></span>                   | <span data-ttu-id="47131-162">JPY 12,500</span><span class="sxs-lookup"><span data-stu-id="47131-162">JPY 12,500</span></span>                      |
| <span data-ttu-id="47131-163">2013 年 4 月 1 日</span><span class="sxs-lookup"><span data-stu-id="47131-163">April 1, 2013</span></span>    | <span data-ttu-id="47131-164">2014 年 3 月 31 日</span><span class="sxs-lookup"><span data-stu-id="47131-164">March 31, 2014</span></span> | <span data-ttu-id="47131-165">JPY 50,000</span><span class="sxs-lookup"><span data-stu-id="47131-165">JPY 50,000</span></span>                              | <span data-ttu-id="47131-166">JPY 100,000</span><span class="sxs-lookup"><span data-stu-id="47131-166">JPY 100,000</span></span>              | <span data-ttu-id="47131-167">JPY 50,000</span><span class="sxs-lookup"><span data-stu-id="47131-167">JPY 50,000</span></span>                    | <span data-ttu-id="47131-168">JPY 4,167</span><span class="sxs-lookup"><span data-stu-id="47131-168">JPY 4,167</span></span>                       |
| <span data-ttu-id="47131-169">2014 年 4 月 1 日</span><span class="sxs-lookup"><span data-stu-id="47131-169">April 1, 2014</span></span>    | <span data-ttu-id="47131-170">2015 年 3 月 31 日</span><span class="sxs-lookup"><span data-stu-id="47131-170">March 31, 2015</span></span> | <span data-ttu-id="47131-171">JPY 50,000</span><span class="sxs-lookup"><span data-stu-id="47131-171">JPY 50,000</span></span>                              | <span data-ttu-id="47131-172">JPY 150,000</span><span class="sxs-lookup"><span data-stu-id="47131-172">JPY 150,000</span></span>              | <span data-ttu-id="47131-173">0</span><span class="sxs-lookup"><span data-stu-id="47131-173">0</span></span>                             | <span data-ttu-id="47131-174">JPY 4,167</span><span class="sxs-lookup"><span data-stu-id="47131-174">JPY 4,167</span></span>                       |

## <a name="how-is-depreciation-calculated-using-the-equally-divided-depreciation-method-if-the-asset-calendar-is-changed-during-the-asset-life-cycle"></a><span data-ttu-id="47131-175">試算カレンダーが資産の有効期間中に変更される場合、均等減価償却法を使用してどのように減価償却を計算しますか。</span><span class="sxs-lookup"><span data-stu-id="47131-175">How is depreciation calculated using the equally divided depreciation method if the asset calendar is changed during the asset life cycle?</span></span>
<span data-ttu-id="47131-176">Finance が均等減価償却法を使用して減価償却を計算する場合、**帳簿**ページの**カレンダー**フィールドで選択された会計カレンダーに基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="47131-176">When Finance calculates depreciation by using the equally divided depreciation method, the calculation is based on the fiscal calendar that is selected in the **Calendar** field on the **Books** page.</span></span> <span data-ttu-id="47131-177">資産カレンダーが資産の有効期間中に変更された場合、現在のカレンダーに基づいて、会計年度内の月または四半期などの会計年度期間の数を計算します。</span><span class="sxs-lookup"><span data-stu-id="47131-177">If an asset calendar is changed during the asset life cycle, the number of fiscal periods, such as months or quarters, in a fiscal year is calculated based on the current calendar.</span></span> <span data-ttu-id="47131-178">たとえば、以下の一括比例配分の固定資産を取得します。</span><span class="sxs-lookup"><span data-stu-id="47131-178">For example, you acquire a lump-sum fixed asset:</span></span>

-   <span data-ttu-id="47131-179">会計カレンダー = 4 月 1 日から 3 月 31 日</span><span class="sxs-lookup"><span data-stu-id="47131-179">Fiscal calendar = April 1 to March 31</span></span>
-   <span data-ttu-id="47131-180">一括比例配分の固定資産の取得日付 = 2012 年 4 月 1 日</span><span class="sxs-lookup"><span data-stu-id="47131-180">Acquisition date of the lump-sum fixed asset = April 1, 2012</span></span>
-   <span data-ttu-id="47131-181">均等減価償却量に対する年数 = 3 年</span><span class="sxs-lookup"><span data-stu-id="47131-181">Number of years to equally divide the depreciation amount = 3 years</span></span>

<span data-ttu-id="47131-182">2013 年 4 月、第 2 会計年度中に、会計カレンダー 4 月 1 日～ 3 月 31 日を 1 月 1 日～ 12 月 31 日に変更すると、次の表のように会計年度の減価償却期間の数が計算されます。</span><span class="sxs-lookup"><span data-stu-id="47131-182">In April 2013, during the second fiscal year, if you change the fiscal calendar from April 1 through March 31 to January 1 through December 31, the number of depreciation periods for the fiscal years are calculated as shown in the following table.</span></span>

| <span data-ttu-id="47131-183">年度</span><span class="sxs-lookup"><span data-stu-id="47131-183">Fiscal year</span></span>                                | <span data-ttu-id="47131-184">減価償却期間の数</span><span class="sxs-lookup"><span data-stu-id="47131-184">Number of depreciation periods</span></span> |
|--------------------------------------------|--------------------------------|
| <span data-ttu-id="47131-185">2012 年 4 月 1 日～ 2013 年 3 月 31 日</span><span class="sxs-lookup"><span data-stu-id="47131-185">April 1, 2012, through March 31, 2013</span></span>      | <span data-ttu-id="47131-186">12 期間</span><span class="sxs-lookup"><span data-stu-id="47131-186">12 periods</span></span>                     |
| <span data-ttu-id="47131-187">2013 年 4 月 1 日～2013 年 12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="47131-187">April 1, 2013, through December 31, 2013</span></span>   | <span data-ttu-id="47131-188">9 期間</span><span class="sxs-lookup"><span data-stu-id="47131-188">9 periods</span></span>                      |
| <span data-ttu-id="47131-189">2014 年 1 月 1 日～2014 年 12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="47131-189">January 1, 2014, through December 31, 2014</span></span> | <span data-ttu-id="47131-190">12 期間</span><span class="sxs-lookup"><span data-stu-id="47131-190">12 periods</span></span>                     |
| <span data-ttu-id="47131-191">2015 年 1 月 1 日～ 2015 年 3 月 31 日</span><span class="sxs-lookup"><span data-stu-id="47131-191">January 1, 2015, through March 31, 2015</span></span>    | <span data-ttu-id="47131-192">3 期間</span><span class="sxs-lookup"><span data-stu-id="47131-192">3 periods</span></span>                      |

## <a name="can-i-modify-the-equally-divided-depreciation-method-during-the-life-cycle-of-a-fixed-asset"></a><span data-ttu-id="47131-193">固定資産の有効期間中に均等減価償却法を変更できますか。</span><span class="sxs-lookup"><span data-stu-id="47131-193">Can I modify the equally divided depreciation method during the life cycle of a fixed asset?</span></span>
<span data-ttu-id="47131-194">一連番号</span><span class="sxs-lookup"><span data-stu-id="47131-194">No.</span></span> <span data-ttu-id="47131-195">均等減価償却法を使用して固定資産を減価償却するとき、減価償却量は、固定資産の耐用期間内の会計年度期間中に均等分割されます。</span><span class="sxs-lookup"><span data-stu-id="47131-195">When you depreciate a fixed asset by using the equally divided depreciation method, the depreciation amount is equally divided among the fiscal periods within the useful life of the fixed asset.</span></span> <span data-ttu-id="47131-196">したがって、固定資産の有効期間中は減価償却方法を変更できません。</span><span class="sxs-lookup"><span data-stu-id="47131-196">Therefore, you can't change the depreciation method during the life cycle of the fixed asset.</span></span>

## <a name="can-i-change-the-depreciation-period-for-an-equally-divided-depreciation-profile"></a><span data-ttu-id="47131-197">均等減価償却法プロファイルの減価償却期間を変更できますか。</span><span class="sxs-lookup"><span data-stu-id="47131-197">Can I change the depreciation period for an equally divided depreciation profile?</span></span>
<span data-ttu-id="47131-198">一連番号</span><span class="sxs-lookup"><span data-stu-id="47131-198">No.</span></span> <span data-ttu-id="47131-199">**減価償却簿**ページで均等減価償却法プロファイルを選択した場合、減価償却プロファイルの**減価償却プロファイル**ページの**均等償却年数**フィールドの値は変更できません。</span><span class="sxs-lookup"><span data-stu-id="47131-199">If you selected an equally divided depreciation profile on the **Books** page, you can't change the value in the **Number of years to equally divide depreciation amounts** field on the **Depreciation profiles** page for the depreciation profile.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="47131-200">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="47131-200">Additional resources</span></span>
- [<span data-ttu-id="47131-201">固定資産減価償却の FAQ</span><span class="sxs-lookup"><span data-stu-id="47131-201">Fixed asset depreciation FAQ</span></span>](apac-jpn-fixed-asset-depreciation.md)
- [<span data-ttu-id="47131-202">均等償却を使用した一括比例配分減価償却資産の作成</span><span class="sxs-lookup"><span data-stu-id="47131-202">Create lump-sum depreciation assets using equally-divided method</span></span>](./tasks/create-lump-sum-depreciation-assets-equally-divided-method.md)


