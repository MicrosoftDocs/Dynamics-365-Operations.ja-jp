---
title: 手動減価償却
description: この記事は、手動減価償却方法の減価償却の概要を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 84cde511ab0b5cbe4b99e72832bf548336b6b28c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187225"
---
# <a name="manual-depreciation"></a><span data-ttu-id="77901-103">手動減価償却</span><span class="sxs-lookup"><span data-stu-id="77901-103">Manual depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77901-104">この記事は、手動減価償却方法の減価償却の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="77901-104">This article gives an overview of the manual depreciation method.</span></span>

<span data-ttu-id="77901-105">固定資産減価償却プロファイルを設定し、**減価償却プロファイル** ページの **メソッド** フィールドで **マニュアル** を選択すると、この減価償却プロファイルに割り当てられる固定資産の減価償却は、暦年内の期間ごとに入力した比率によって決定されることになります。</span><span class="sxs-lookup"><span data-stu-id="77901-105">When you set up a fixed asset depreciation profile and select **Manual** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is determined by the percentage that you enter for each interval in the calendar year.</span></span> <span data-ttu-id="77901-106">比率を設定した期間は、**減価償却プロファイル** ページの **一般** クイック タブにある **期間の頻度** フィールドで選択した値に従って転記されます。</span><span class="sxs-lookup"><span data-stu-id="77901-106">The intervals that you set up percentages for are posted according to the value that you select in the **Period frequency** field on the **General** FastTab of the **Depreciation profiles** page.</span></span> <span data-ttu-id="77901-107">選択できる値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="77901-107">Here are the values that you can select:</span></span>

-   <span data-ttu-id="77901-108">年 1 回</span><span class="sxs-lookup"><span data-stu-id="77901-108">Yearly</span></span>
-   <span data-ttu-id="77901-109">毎月</span><span class="sxs-lookup"><span data-stu-id="77901-109">Monthly</span></span>
-   <span data-ttu-id="77901-110">四半期に 1 回</span><span class="sxs-lookup"><span data-stu-id="77901-110">Quarterly</span></span>
-   <span data-ttu-id="77901-111">半期に 1 回</span><span class="sxs-lookup"><span data-stu-id="77901-111">Half-Yearly</span></span>
-   <span data-ttu-id="77901-112">毎日</span><span class="sxs-lookup"><span data-stu-id="77901-112">Daily</span></span>

<span data-ttu-id="77901-113">期間の頻度を選択したら、**手動のスケジュール** をクリックし、転記期間ごとに比率を設定します。</span><span class="sxs-lookup"><span data-stu-id="77901-113">After you select the period frequency, click **Manual schedules**, and set up percentages for each posting interval.</span></span> <span data-ttu-id="77901-114">手動のスケジュールと転記期間は、この記事の後半にある例が示すように、減価償却額を一緒に定義します。</span><span class="sxs-lookup"><span data-stu-id="77901-114">Together, the manual schedules and the posting intervals define the depreciation amount, as shown in the examples later in this article.</span></span> <span data-ttu-id="77901-115">手動減価償却は、常に取得価格の比率として計算されます。</span><span class="sxs-lookup"><span data-stu-id="77901-115">Manual depreciation is always calculated as a percentage of the acquisition price.</span></span> <span data-ttu-id="77901-116">手動減価償却については、減価償却期間に入力した割合は合計すると 100 パーセントになる必要はありません。</span><span class="sxs-lookup"><span data-stu-id="77901-116">For manual depreciation, the percentages that you enter in the intervals of the depreciation don't have to add up to 100 percent.</span></span> <span data-ttu-id="77901-117">手動減価償却とは、特別な目的 (たとえば、税金など) のための非期間原価焼却などの、特別な減価償却プロファイルを **帳簿** ページで定義するためにしばしば使用される柔軟な減価償却方法です。</span><span class="sxs-lookup"><span data-stu-id="77901-117">Manual depreciation is a flexible depreciation method that is often used to define an extraordinary depreciation profile on the **Books** page, such as a non-periodic depreciation for special purposes (for example, tax).</span></span>

## <a name="examples"></a><span data-ttu-id="77901-118">例</span><span class="sxs-lookup"><span data-stu-id="77901-118">Examples</span></span>
<span data-ttu-id="77901-119">取得価格: 11,000.00 予定仕損価格: 1,000.00 次の表に、**固定資産減価償却プロファイル スケジュール** ページで設定する期間と比率が表示されます。</span><span class="sxs-lookup"><span data-stu-id="77901-119">Acquisition price: 11,000.00 Expected scrap value: 1,000.00 The following table shows the intervals and percentages that you set up on the **Fixed asset depreciation profile schedules** page.</span></span>

| <span data-ttu-id="77901-120">間隔数</span><span class="sxs-lookup"><span data-stu-id="77901-120">Interval number</span></span> | <span data-ttu-id="77901-121">パーセンテージ</span><span class="sxs-lookup"><span data-stu-id="77901-121">Percentage</span></span> |
|-----------------|------------|
| <span data-ttu-id="77901-122">1</span><span class="sxs-lookup"><span data-stu-id="77901-122">1</span></span>               | <span data-ttu-id="77901-123">10.00</span><span class="sxs-lookup"><span data-stu-id="77901-123">10.00</span></span>      |
| <span data-ttu-id="77901-124">2</span><span class="sxs-lookup"><span data-stu-id="77901-124">2</span></span>               | <span data-ttu-id="77901-125">50.00</span><span class="sxs-lookup"><span data-stu-id="77901-125">50.00</span></span>      |
| <span data-ttu-id="77901-126">3</span><span class="sxs-lookup"><span data-stu-id="77901-126">3</span></span>               | <span data-ttu-id="77901-127">8.00</span><span class="sxs-lookup"><span data-stu-id="77901-127">8.00</span></span>       |

<span data-ttu-id="77901-128">以下の表には各期間の減価償却の計算方法が表示されます。</span><span class="sxs-lookup"><span data-stu-id="77901-128">The following table shows how the depreciation for each interval is calculated.</span></span>

|  <span data-ttu-id="77901-129">間隔数</span><span class="sxs-lookup"><span data-stu-id="77901-129">Interval number</span></span> | <span data-ttu-id="77901-130">年次減価償却額の計算</span><span class="sxs-lookup"><span data-stu-id="77901-130">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="77901-131">期間の終了時の正味簿価額</span><span class="sxs-lookup"><span data-stu-id="77901-131">Net book value at the end of the interval</span></span> |
|------------------|-----------------------------------------------|-------------------------------------------|
| <span data-ttu-id="77901-132">1</span><span class="sxs-lookup"><span data-stu-id="77901-132">1</span></span>                | <span data-ttu-id="77901-133">(11,000 – 1,000) × 10% = 1,000</span><span class="sxs-lookup"><span data-stu-id="77901-133">(11,000 – 1,000) × 10% = 1,000</span></span>                | <span data-ttu-id="77901-134">10,000 (11,000 – 1,000)</span><span class="sxs-lookup"><span data-stu-id="77901-134">10,000 (11,000 – 1,000)</span></span>                   |
| <span data-ttu-id="77901-135">2</span><span class="sxs-lookup"><span data-stu-id="77901-135">2</span></span>                | <span data-ttu-id="77901-136">(11,000 – 1,000) × 50% = 5,000</span><span class="sxs-lookup"><span data-stu-id="77901-136">(11,000 – 1,000) × 50% = 5,000</span></span>                | <span data-ttu-id="77901-137">5,000 (10,000 – 5,000)</span><span class="sxs-lookup"><span data-stu-id="77901-137">5,000 (10,000 – 5,000)</span></span>                    |
| <span data-ttu-id="77901-138">3</span><span class="sxs-lookup"><span data-stu-id="77901-138">3</span></span>                | <span data-ttu-id="77901-139">(11,000 – 1,000) × 8% = 800</span><span class="sxs-lookup"><span data-stu-id="77901-139">(11,000 – 1,000) × 8% = 800</span></span>                   | <span data-ttu-id="77901-140">4,200 (5,000 – 800)</span><span class="sxs-lookup"><span data-stu-id="77901-140">4,200 (5,000 – 800)</span></span>                       |

<span data-ttu-id="77901-141">**期間の頻度** フィールドで **毎月** を選択した場合は、手動のスケジュールで 12 の期間を設定します。</span><span class="sxs-lookup"><span data-stu-id="77901-141">If you select **Monthly** in the **Period frequency** field, you set up 12 manual schedule intervals.</span></span> <span data-ttu-id="77901-142">次の表には最初の 2 間隔の減価償却量が表示されます。</span><span class="sxs-lookup"><span data-stu-id="77901-142">The following table shows the depreciation amounts for the first two intervals.</span></span>

| <span data-ttu-id="77901-143">間隔</span><span class="sxs-lookup"><span data-stu-id="77901-143">Interval</span></span> | <span data-ttu-id="77901-144">算出償却額</span><span class="sxs-lookup"><span data-stu-id="77901-144">Depreciation amount</span></span>            |
|----------|--------------------------------|
| <span data-ttu-id="77901-145">1 月</span><span class="sxs-lookup"><span data-stu-id="77901-145">January</span></span>  | <span data-ttu-id="77901-146">(11,000 – 1,000) × 10% = 1,000</span><span class="sxs-lookup"><span data-stu-id="77901-146">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="77901-147">2 月</span><span class="sxs-lookup"><span data-stu-id="77901-147">February</span></span> | <span data-ttu-id="77901-148">(11,000 – 1,000) × 50% = 5,000</span><span class="sxs-lookup"><span data-stu-id="77901-148">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="77901-149">*<strong><em>期間の頻度</em>* フィールド</strong>で <strong>半期に 1 回</strong> を選択した場合は、2 つの手動スケジュール間隔が設定されます。</span><span class="sxs-lookup"><span data-stu-id="77901-149">If you select <strong>Half-Yearly</strong> in the *<strong><em>Period frequency</em>* field</strong>, you set up two manual schedule intervals.</span></span> <span data-ttu-id="77901-150">次の表にはこれら 2 間隔の減価償却量が表示されます。</span><span class="sxs-lookup"><span data-stu-id="77901-150">The following table shows the depreciation amounts for those two intervals.</span></span>

| <span data-ttu-id="77901-151">間隔</span><span class="sxs-lookup"><span data-stu-id="77901-151">Interval</span></span>    | <span data-ttu-id="77901-152">算出償却額</span><span class="sxs-lookup"><span data-stu-id="77901-152">Depreciation amount</span></span>            |
|-------------|--------------------------------|
| <span data-ttu-id="77901-153">6 月 30 日</span><span class="sxs-lookup"><span data-stu-id="77901-153">June 30</span></span>     | <span data-ttu-id="77901-154">(11,000 – 1,000) × 10% = 1,000</span><span class="sxs-lookup"><span data-stu-id="77901-154">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="77901-155">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="77901-155">December 31</span></span> | <span data-ttu-id="77901-156">(11,000 – 1,000) × 50% = 5,000</span><span class="sxs-lookup"><span data-stu-id="77901-156">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="77901-157">全期間の比率の合計を 100 にする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="77901-157">The total of percentages for all intervals doesn't have to be 100.</span></span> <span data-ttu-id="77901-158">ただし、**固定資産減価償却プロファイル スケジュール** ページの **累積比率** フィールドの値が **100** ではない場合、メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="77901-158">However, you receive a message if the value in the **Cumulative percentage** field on the **Fixed asset depreciation profile schedules** page isn't **100**.</span></span>



