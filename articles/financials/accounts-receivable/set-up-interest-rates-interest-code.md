---
title: "利息コードに対する金利の設定"
description: "利息コードには、利息がかかる日付と、支払期限を過ぎた勘定における計算方法を決める設定値が含まれます。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 59acfaa93b1352f2be6d750dea6bdd740bac0312
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="fc980-103">利息コードに対する金利の設定</span><span class="sxs-lookup"><span data-stu-id="fc980-103">Set up interest rates for an interest code</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="fc980-104">利息コードには、利息がかかる日付と、支払期限を過ぎた勘定における計算方法を決める設定値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="fc980-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="fc980-105">一つの利息コードを設定すれば、それを、複数の顧客の転記プロファイル、請求コード、または特定の請求明細行に適用できます。</span><span class="sxs-lookup"><span data-stu-id="fc980-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="fc980-106">利息コードの詳細情報を変更すると、そのコードを使用するすべての機能が新しいトランザクションにその変更を自動的に反映します。</span><span class="sxs-lookup"><span data-stu-id="fc980-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="fc980-107">各利息コードに対して、2 つのタイプを設定できます。</span><span class="sxs-lookup"><span data-stu-id="fc980-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="fc980-108">利子所得の利率 − 請求書や利子計算書に利息を掛けて得られた収益を表します。</span><span class="sxs-lookup"><span data-stu-id="fc980-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="fc980-109">利息支払いの利率 − 負担額通知書の利息に支払われるコストを表します。</span><span class="sxs-lookup"><span data-stu-id="fc980-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="fc980-110">いずれの利率タイプも、同じ利息コードに同時に設定できます。</span><span class="sxs-lookup"><span data-stu-id="fc980-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="fc980-111">利率の計算タイプは、3 つあります。</span><span class="sxs-lookup"><span data-stu-id="fc980-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="fc980-112">割合ごとの利息。</span><span class="sxs-lookup"><span data-stu-id="fc980-112">Interest by percentage.</span></span>
-   <span data-ttu-id="fc980-113">金額ごとの利息。</span><span class="sxs-lookup"><span data-stu-id="fc980-113">Interest by amount.</span></span>
-   <span data-ttu-id="fc980-114">範囲ごとの利息。結果は一つの割合または金額。</span><span class="sxs-lookup"><span data-stu-id="fc980-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="fc980-115">利息コードを利息の計算に使用すると、支払いがトランザクションの期日を過ぎて有効な利率ごとに個別に利子計算書が作成されます。</span><span class="sxs-lookup"><span data-stu-id="fc980-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="fc980-116">**利息コード** ページの [**受取利息**] タブを使用して、利息を掛けて得られる利率を設定します。</span><span class="sxs-lookup"><span data-stu-id="fc980-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="fc980-117">[**支払利息**] タブを使用して、支払う利息の利率を設定します。</span><span class="sxs-lookup"><span data-stu-id="fc980-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="fc980-118">割合に基づいた利率</span><span class="sxs-lookup"><span data-stu-id="fc980-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="fc980-119">指定した割合を計算する利率を設定できます。</span><span class="sxs-lookup"><span data-stu-id="fc980-119">You can set up interest rates that calculate a specified percentage.</span></span>

-   <span data-ttu-id="fc980-120">利息金額はすべての通貨に適用されます。</span><span class="sxs-lookup"><span data-stu-id="fc980-120">Interest amount applies to all currencies.</span></span>
-   <span data-ttu-id="fc980-121">オプションの利子の限度額を入力できます。</span><span class="sxs-lookup"><span data-stu-id="fc980-121">Optional interest amount limits can be entered.</span></span>
-   <span data-ttu-id="fc980-122">**パーセンテージ** が、** ** [**利息コードの設定**] ページの [**次に基づいて利息を計算**] フィールドで選択されます。</span><span class="sxs-lookup"><span data-stu-id="fc980-122">**Percentage** is selected** **in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="fc980-123">たとえば、請求書の支払がトランザクション期日を超えると 2 か月ごとに 5% の利息が付く利子コードを設定するには、[**利息の計算間隔**] フィールドに 2 を入力し、 [**月**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc980-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="fc980-124">金額に基づいた利率</span><span class="sxs-lookup"><span data-stu-id="fc980-124">Interest rates based on amounts</span></span>
<span data-ttu-id="fc980-125">通貨ごとの指定金額を計算する利率を設定できます。</span><span class="sxs-lookup"><span data-stu-id="fc980-125">You can set up interest rates that calculate a specified amount per currency.</span></span>
-   <span data-ttu-id="fc980-126">利息金額は、利息コードで通貨ごとに指定されます。</span><span class="sxs-lookup"><span data-stu-id="fc980-126">An interest amount is specified for each currency in the interest code.</span></span>
-   <span data-ttu-id="fc980-127">オプションの利子の限度額を入力できます。</span><span class="sxs-lookup"><span data-stu-id="fc980-127">Optional interest amount limits can be entered.</span></span>
-   <span data-ttu-id="fc980-128">**金額**が、[**利息コードの設定**] ページの [**次に基づいて利息を計算**] フィールドで選択されます。</span><span class="sxs-lookup"><span data-stu-id="fc980-128">**Amount **is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="fc980-129">たとえば、請求書支払がトランザクション期日を過ぎると 20 日ごとに 25.00 の利息が付く利息コードを設定するには、[**利息の計算間隔**] フィールドに 20 を入力し、[**日付**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc980-129">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="fc980-130">範囲に基づいた利率</span><span class="sxs-lookup"><span data-stu-id="fc980-130">Interest rates based on ranges</span></span>
<span data-ttu-id="fc980-131">支払い期限切れの金額、その金額が支払い期限を過ぎた日数、または金額が支払い期限を過ぎた月数によって異なる利率を設定できます。</span><span class="sxs-lookup"><span data-stu-id="fc980-131">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="fc980-132">[**通貨別受取利息**] タブを使用して、通貨ごとの特定の利息の設定を定義できます。</span><span class="sxs-lookup"><span data-stu-id="fc980-132">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="fc980-133">ここでは、範囲も定義します。</span><span class="sxs-lookup"><span data-stu-id="fc980-133">This is also where you will define the range.</span></span>
-   <span data-ttu-id="fc980-134">[**範囲**] ボタンを使用して、設定する範囲を表す行を追加します。</span><span class="sxs-lookup"><span data-stu-id="fc980-134">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="fc980-135">**開始**値は、範囲の開始を表し、**利息値**の数字は、**利息コードの設定**ページの [**次に基づいて利息を計算**] フィールドでの選択に応じた割合や金額を表します。</span><span class="sxs-lookup"><span data-stu-id="fc980-135">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="fc980-136">例 1: 利息/範囲 = 金額</span><span class="sxs-lookup"><span data-stu-id="fc980-136">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="fc980-137">請求書支払がトランザクションの期日を超えると、3 か月おきに利息を 1 回計算する利息コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="fc980-137">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="fc980-138">段階的な金額差に応じて、割合利息値を基準に計算します。</span><span class="sxs-lookup"><span data-stu-id="fc980-138">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="fc980-139">利息値は､最大請求金額 1,000.00 まで 1%、金額 1,001.00 から 5,000.00 まで 2%、金額 5,000.00 を超えると 3% になります。</span><span class="sxs-lookup"><span data-stu-id="fc980-139">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="fc980-140">利息コードのフィールド値は次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="fc980-140">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="fc980-141">**フィールド名**</span><span class="sxs-lookup"><span data-stu-id="fc980-141">**Field name**</span></span>                  | <span data-ttu-id="fc980-142">**フィールド値**</span><span class="sxs-lookup"><span data-stu-id="fc980-142">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="fc980-143">**利息コード**</span><span class="sxs-lookup"><span data-stu-id="fc980-143">**Interest code**</span></span>               | <span data-ttu-id="fc980-144">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="fc980-144">3M%ByAmt</span></span>        |
| <span data-ttu-id="fc980-145">**利息の計算間隔**</span><span class="sxs-lookup"><span data-stu-id="fc980-145">**Calculate interest every**</span></span>    | <span data-ttu-id="fc980-146">3/月</span><span class="sxs-lookup"><span data-stu-id="fc980-146">3/Month</span></span>         |
| <span data-ttu-id="fc980-147">**範囲別の利息**</span><span class="sxs-lookup"><span data-stu-id="fc980-147">**Interest by range**</span></span>           | <span data-ttu-id="fc980-148">金額</span><span class="sxs-lookup"><span data-stu-id="fc980-148">Amount</span></span>          |
| <span data-ttu-id="fc980-149">**次に基づいて利息を計算**</span><span class="sxs-lookup"><span data-stu-id="fc980-149">**Calculate interest based on**</span></span> | <span data-ttu-id="fc980-150">パーセンテージ</span><span class="sxs-lookup"><span data-stu-id="fc980-150">Percentage</span></span>      |

<span data-ttu-id="fc980-151">範囲情報を次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="fc980-151">You set up the range information as follows.</span></span>

| <span data-ttu-id="fc980-152">**範囲の開始値 (From)**</span><span class="sxs-lookup"><span data-stu-id="fc980-152">**From value**</span></span> | <span data-ttu-id="fc980-153">**利息値**</span><span class="sxs-lookup"><span data-stu-id="fc980-153">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="fc980-154">0</span><span class="sxs-lookup"><span data-stu-id="fc980-154">0</span></span>              | <span data-ttu-id="fc980-155">1</span><span class="sxs-lookup"><span data-stu-id="fc980-155">1</span></span>                  |
| <span data-ttu-id="fc980-156">1,001</span><span class="sxs-lookup"><span data-stu-id="fc980-156">1,001</span></span>          | <span data-ttu-id="fc980-157">2</span><span class="sxs-lookup"><span data-stu-id="fc980-157">2</span></span>                  |
| <span data-ttu-id="fc980-158">5,001</span><span class="sxs-lookup"><span data-stu-id="fc980-158">5,001</span></span>          | <span data-ttu-id="fc980-159">3</span><span class="sxs-lookup"><span data-stu-id="fc980-159">3</span></span>                  |

 
## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="fc980-160">例 2: 利息/範囲 = 日数</span><span class="sxs-lookup"><span data-stu-id="fc980-160">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="fc980-161">請求書支払がトランザクションの期日を超えると、15 日おきに利息を 1 回計算する利息コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="fc980-161">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="fc980-162">段階的な日数間隔に応じて、金額利息値を基準に計算します。</span><span class="sxs-lookup"><span data-stu-id="fc980-162">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="fc980-163">利息値は、最初の 60 日まで 15 日あたり 10.00、61 日から 90 日まで 15.00、91 日以降は 15 日あたり 20.00 です。</span><span class="sxs-lookup"><span data-stu-id="fc980-163">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="fc980-164">利息コードのフィールド値は次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="fc980-164">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="fc980-165">**フィールド名**</span><span class="sxs-lookup"><span data-stu-id="fc980-165">**Field name**</span></span>                  | <span data-ttu-id="fc980-166">**フィールド値**</span><span class="sxs-lookup"><span data-stu-id="fc980-166">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="fc980-167">**利息コード**</span><span class="sxs-lookup"><span data-stu-id="fc980-167">**Interest code**</span></span>               | <span data-ttu-id="fc980-168">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="fc980-168">15DAmtXDay</span></span>      |
| <span data-ttu-id="fc980-169">**利息の計算間隔**</span><span class="sxs-lookup"><span data-stu-id="fc980-169">**Calculate interest every**</span></span>    | <span data-ttu-id="fc980-170">15/日</span><span class="sxs-lookup"><span data-stu-id="fc980-170">15/Day</span></span>          |
| <span data-ttu-id="fc980-171">**範囲別の利息**</span><span class="sxs-lookup"><span data-stu-id="fc980-171">**Interest by range**</span></span>           | <span data-ttu-id="fc980-172">日</span><span class="sxs-lookup"><span data-stu-id="fc980-172">Days</span></span>            |
| <span data-ttu-id="fc980-173">**次に基づいて利息を計算**</span><span class="sxs-lookup"><span data-stu-id="fc980-173">**Calculate interest based on**</span></span> | <span data-ttu-id="fc980-174">金額</span><span class="sxs-lookup"><span data-stu-id="fc980-174">Amount</span></span>          |

<span data-ttu-id="fc980-175">範囲情報を次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="fc980-175">You set up the range information as follows.</span></span>

| <span data-ttu-id="fc980-176">**範囲の開始値 (From)**</span><span class="sxs-lookup"><span data-stu-id="fc980-176">**From value**</span></span> | <span data-ttu-id="fc980-177">**利息値**</span><span class="sxs-lookup"><span data-stu-id="fc980-177">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="fc980-178">0</span><span class="sxs-lookup"><span data-stu-id="fc980-178">0</span></span>              | <span data-ttu-id="fc980-179">10</span><span class="sxs-lookup"><span data-stu-id="fc980-179">10</span></span>                 |
| <span data-ttu-id="fc980-180">61</span><span class="sxs-lookup"><span data-stu-id="fc980-180">61</span></span>             | <span data-ttu-id="fc980-181">15</span><span class="sxs-lookup"><span data-stu-id="fc980-181">15</span></span>                 |
| <span data-ttu-id="fc980-182">91</span><span class="sxs-lookup"><span data-stu-id="fc980-182">91</span></span>             | <span data-ttu-id="fc980-183">20</span><span class="sxs-lookup"><span data-stu-id="fc980-183">20</span></span>                 |

 
## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="fc980-184">例 3: 利息/範囲 = 月数</span><span class="sxs-lookup"><span data-stu-id="fc980-184">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="fc980-185">請求書支払がトランザクションの期日を超えると、毎月利息を 1 回計算する利息コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="fc980-185">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="fc980-186">段階的な月間隔に応じて、割合利息値を基準に計算します。</span><span class="sxs-lookup"><span data-stu-id="fc980-186">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="fc980-187">利息の値は、支払い期限を過ぎて最初の 3 か月は毎月 1.5%、次の 3 か月が毎月 2.0% が、最初の 6 か月を過ぎると毎月 2.5% です。</span><span class="sxs-lookup"><span data-stu-id="fc980-187">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="fc980-188">利息コードのフィールド値は次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="fc980-188">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="fc980-189">**フィールド名**</span><span class="sxs-lookup"><span data-stu-id="fc980-189">**Field name**</span></span>                  | <span data-ttu-id="fc980-190">**フィールド値**</span><span class="sxs-lookup"><span data-stu-id="fc980-190">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="fc980-191">**利息コード**</span><span class="sxs-lookup"><span data-stu-id="fc980-191">**Interest code**</span></span>               | <span data-ttu-id="fc980-192">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="fc980-192">1M%ByMth</span></span>        |
| <span data-ttu-id="fc980-193">**利息の計算間隔**</span><span class="sxs-lookup"><span data-stu-id="fc980-193">**Calculate interest every**</span></span>    | <span data-ttu-id="fc980-194">1/月</span><span class="sxs-lookup"><span data-stu-id="fc980-194">1/Month</span></span>         |
| <span data-ttu-id="fc980-195">**範囲別の利息**</span><span class="sxs-lookup"><span data-stu-id="fc980-195">**Interest by range**</span></span>           | <span data-ttu-id="fc980-196">月</span><span class="sxs-lookup"><span data-stu-id="fc980-196">Months</span></span>          |
| <span data-ttu-id="fc980-197">**次に基づいて利息を計算**</span><span class="sxs-lookup"><span data-stu-id="fc980-197">**Calculate interest based on**</span></span> | <span data-ttu-id="fc980-198">パーセンテージ</span><span class="sxs-lookup"><span data-stu-id="fc980-198">Percentage</span></span>      |

<span data-ttu-id="fc980-199">範囲情報を次のように設定します。</span><span class="sxs-lookup"><span data-stu-id="fc980-199">You set up the range information as follows.</span></span>

| <span data-ttu-id="fc980-200">**範囲の開始値 (From)**</span><span class="sxs-lookup"><span data-stu-id="fc980-200">**From value**</span></span> | <span data-ttu-id="fc980-201">**利息値**</span><span class="sxs-lookup"><span data-stu-id="fc980-201">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="fc980-202">0</span><span class="sxs-lookup"><span data-stu-id="fc980-202">0</span></span>              | <span data-ttu-id="fc980-203">1.5</span><span class="sxs-lookup"><span data-stu-id="fc980-203">1.5</span></span>                |
| <span data-ttu-id="fc980-204">4</span><span class="sxs-lookup"><span data-stu-id="fc980-204">4</span></span>              | <span data-ttu-id="fc980-205">2</span><span class="sxs-lookup"><span data-stu-id="fc980-205">2</span></span>                  |
| <span data-ttu-id="fc980-206">7</span><span class="sxs-lookup"><span data-stu-id="fc980-206">7</span></span>              | <span data-ttu-id="fc980-207">2.5</span><span class="sxs-lookup"><span data-stu-id="fc980-207">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="fc980-208">新しいバージョン</span><span class="sxs-lookup"><span data-stu-id="fc980-208">New versions</span></span>
<span data-ttu-id="fc980-209">利息コードは有効日です。</span><span class="sxs-lookup"><span data-stu-id="fc980-209">Interest codes are date effective.</span></span> <span data-ttu-id="fc980-210">金利を変更する場合は、将来の日付で有効になる**新バージョン**を作成できます。</span><span class="sxs-lookup"><span data-stu-id="fc980-210">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="fc980-211">異なるバージョンを表示するには、[**現在の日付**] メニューを使用して締日を選択できます。</span><span class="sxs-lookup"><span data-stu-id="fc980-211">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="fc980-212">また、[**すべてのレコードを表示**] を選択してページのすべての利息コードを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="fc980-212">You can also select the **Display all records** to view all interest codes in the page.</span></span>




