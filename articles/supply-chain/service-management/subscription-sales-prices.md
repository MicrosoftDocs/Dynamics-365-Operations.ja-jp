---
title: 定期売買販売価格
description: 定期売買を作成すると、販売価格 (定期売買) フォームで作成した販売価格設定から販売価格が派生します。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f03efbbca4fc9da76c6ead7566457beb79c8c249
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985868"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="2ffdd-103">定期売買販売価格</span><span class="sxs-lookup"><span data-stu-id="2ffdd-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="2ffdd-104">定期売買を作成すると、**販売価格 (定期売買)** フォームで作成した販売価格設定から販売価格が派生します。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="2ffdd-105">**販売価格 (定期売買)** フォームでは、特定の定期売買用の販売価格、または、より広範囲に適用される販売価格を作成できます。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="2ffdd-106">定期売買に適用される販売価格については、定期売買と販売価格の期間コードと通貨が一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="2ffdd-107">定期売買と販売価格で期間コードと通貨が一致する場合は、定期売買販売価格が次の表の優先順位に従って選択されます。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="2ffdd-108">表の空白セルは空白のフィールドを示し、X はトランザクションの生成元である定期売買の値と等しい値であることを示します。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2ffdd-109">優先順位</span><span class="sxs-lookup"><span data-stu-id="2ffdd-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-110"><strong>カテゴリ</strong></span><span class="sxs-lookup"><span data-stu-id="2ffdd-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="2ffdd-111"><strong>プロジェクト ID</strong></span><span class="sxs-lookup"><span data-stu-id="2ffdd-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="2ffdd-112"><strong>定期売買</strong></span><span class="sxs-lookup"><span data-stu-id="2ffdd-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="2ffdd-113"><strong>販売通貨</strong></span><span class="sxs-lookup"><span data-stu-id="2ffdd-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="2ffdd-114"><strong>期間コード</strong></span><span class="sxs-lookup"><span data-stu-id="2ffdd-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2ffdd-115">1</span><span class="sxs-lookup"><span data-stu-id="2ffdd-115">1</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-116">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-116">X</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-117">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-117">X</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-118">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-118">X</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-119">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-119">X</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-120">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ffdd-121">2</span><span class="sxs-lookup"><span data-stu-id="2ffdd-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2ffdd-122">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-122">X</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-123">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-123">X</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-124">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-124">X</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-125">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ffdd-126">3</span><span class="sxs-lookup"><span data-stu-id="2ffdd-126">3</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-127">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2ffdd-128">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-128">X</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-129">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-129">X</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-130">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ffdd-131">4</span><span class="sxs-lookup"><span data-stu-id="2ffdd-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2ffdd-132">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-132">X</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-133">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-133">X</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-134">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ffdd-135">5</span><span class="sxs-lookup"><span data-stu-id="2ffdd-135">5</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-136">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-136">X</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-137">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2ffdd-138">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-138">X</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-139">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ffdd-140">6</span><span class="sxs-lookup"><span data-stu-id="2ffdd-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2ffdd-141">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2ffdd-142">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-142">X</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-143">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ffdd-144">7</span><span class="sxs-lookup"><span data-stu-id="2ffdd-144">7</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-145">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2ffdd-146">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-146">X</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-147">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ffdd-148">8</span><span class="sxs-lookup"><span data-stu-id="2ffdd-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="2ffdd-149">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-149">X</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-150">x</span><span class="sxs-lookup"><span data-stu-id="2ffdd-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2ffdd-151">定期売買手数料を作成すると、詳細レベルが最も高い販売価格 (上の表を参照) が定期売買販売価格として選択されます。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="2ffdd-152">定期売買販売価格の更新および指数化</span><span class="sxs-lookup"><span data-stu-id="2ffdd-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="2ffdd-153">定期売買販売価格を更新するには、基準価格または指数を更新します。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="2ffdd-154">割合で更新するか、または新しい値に更新できます。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="2ffdd-155">定期売買手数料の販売価格</span><span class="sxs-lookup"><span data-stu-id="2ffdd-155">Subscription fee sales prices</span></span>

<span data-ttu-id="2ffdd-156">定期売買手数料を作成するときは、定期売買の販売価格設定に基づいて販売価格が決定されます。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="2ffdd-157">その場合、定期売買価格設定の基準価格を使用するか、または指標化された販売価格を作成できます。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="2ffdd-158">例</span><span class="sxs-lookup"><span data-stu-id="2ffdd-158">Example</span></span>

<span data-ttu-id="2ffdd-159">新しいプロジェクト 9030 に対し、EUR 500 の定期売買販売価格を設定するとします。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="2ffdd-160">**販売価格 (定期売買)** フォームで、次の表に示すように、定期売買販売価格の明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2ffdd-161">発効日</span><span class="sxs-lookup"><span data-stu-id="2ffdd-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-162">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="2ffdd-162">Category</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-163">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="2ffdd-163">Project</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-164">定期売買</span><span class="sxs-lookup"><span data-stu-id="2ffdd-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-165">期間コード</span><span class="sxs-lookup"><span data-stu-id="2ffdd-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-166">販売通貨</span><span class="sxs-lookup"><span data-stu-id="2ffdd-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-167">販売価格</span><span class="sxs-lookup"><span data-stu-id="2ffdd-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2ffdd-168">2006 - 08 - 28</span><span class="sxs-lookup"><span data-stu-id="2ffdd-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="2ffdd-169">9030</span><span class="sxs-lookup"><span data-stu-id="2ffdd-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="2ffdd-170">月</span><span class="sxs-lookup"><span data-stu-id="2ffdd-170">Month</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-171">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="2ffdd-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-172">500</span><span class="sxs-lookup"><span data-stu-id="2ffdd-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2ffdd-173">**カテゴリ**および**定期売買**フィールドが空白であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="2ffdd-174">次に、以下の定期売買を作成します。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-174">You then create the following subscriptions.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2ffdd-175">サービスの定期売買</span><span class="sxs-lookup"><span data-stu-id="2ffdd-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-176">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="2ffdd-176">Project</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-177">定期売買グループ</span><span class="sxs-lookup"><span data-stu-id="2ffdd-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-178">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="2ffdd-178">Category</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-179">通貨</span><span class="sxs-lookup"><span data-stu-id="2ffdd-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-180">期間コード</span><span class="sxs-lookup"><span data-stu-id="2ffdd-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2ffdd-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="2ffdd-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-182">9030</span><span class="sxs-lookup"><span data-stu-id="2ffdd-182">9030</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-183">Sub1</span><span class="sxs-lookup"><span data-stu-id="2ffdd-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-184">SubCat1</span><span class="sxs-lookup"><span data-stu-id="2ffdd-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-185">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="2ffdd-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-186">毎月</span><span class="sxs-lookup"><span data-stu-id="2ffdd-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ffdd-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="2ffdd-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-188">9030</span><span class="sxs-lookup"><span data-stu-id="2ffdd-188">9030</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-189">Sub1</span><span class="sxs-lookup"><span data-stu-id="2ffdd-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-190">SubCat2</span><span class="sxs-lookup"><span data-stu-id="2ffdd-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-191">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="2ffdd-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-192">毎月</span><span class="sxs-lookup"><span data-stu-id="2ffdd-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2ffdd-193">次に、定期売買グループ Sub1 内の両方の定期売買に定期売買手数料を作成します。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="2ffdd-194">**サービス管理** \> **設定** \> **サービスの定期売買** \> **定期売買グループ**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="2ffdd-195">**定期売買グループ**フォームで、**関数** \> **定期売買手数料の作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="2ffdd-196">**定期売買手数料の作成**フォームに、適切な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="2ffdd-197">詳細については、[定期売買手数料トランザクションの作成](create-subscription-fee-transactions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="2ffdd-198">販売価格 EUR 500 を持つ定期売買手数料は、次の表に示すように、両方の定期売買で作成されます。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2ffdd-199">プロジェクト日付</span><span class="sxs-lookup"><span data-stu-id="2ffdd-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-200">サービスの定期売買</span><span class="sxs-lookup"><span data-stu-id="2ffdd-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-201">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="2ffdd-201">Project</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-202">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="2ffdd-202">Category</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-203">開始日</span><span class="sxs-lookup"><span data-stu-id="2ffdd-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-204">終了日</span><span class="sxs-lookup"><span data-stu-id="2ffdd-204">End date</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-205">販売通貨</span><span class="sxs-lookup"><span data-stu-id="2ffdd-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-206">販売価格</span><span class="sxs-lookup"><span data-stu-id="2ffdd-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2ffdd-207">2006 - 08 - 28</span><span class="sxs-lookup"><span data-stu-id="2ffdd-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="2ffdd-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-209">9030</span><span class="sxs-lookup"><span data-stu-id="2ffdd-209">9030</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-210">SubCat1</span><span class="sxs-lookup"><span data-stu-id="2ffdd-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-211">2007 - 01 - 01</span><span class="sxs-lookup"><span data-stu-id="2ffdd-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-212">2007 - 03 - 31</span><span class="sxs-lookup"><span data-stu-id="2ffdd-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-213">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="2ffdd-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-214">500</span><span class="sxs-lookup"><span data-stu-id="2ffdd-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ffdd-215">2006 - 08 - 28</span><span class="sxs-lookup"><span data-stu-id="2ffdd-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="2ffdd-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-217">9030</span><span class="sxs-lookup"><span data-stu-id="2ffdd-217">9030</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-218">SubCat2</span><span class="sxs-lookup"><span data-stu-id="2ffdd-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-219">2007 - 01 - 01</span><span class="sxs-lookup"><span data-stu-id="2ffdd-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-220">2007 - 03 - 31</span><span class="sxs-lookup"><span data-stu-id="2ffdd-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-221">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="2ffdd-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-222">500</span><span class="sxs-lookup"><span data-stu-id="2ffdd-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2ffdd-223">その後、プロジェクト 9030 に対するカテゴリ SubCat1 の販売価格を指定するよう決定します。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="2ffdd-224">したがって、プロジェクト 9030 および手数料カテゴリ SubCat1 の組み合わせに対して EUR 550 の販売価格を持つ、新しい販売価格明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="2ffdd-225">これで、次の図に示すように、プロジェクト 9030 の定期売買販売価格明細行が 2 行になります。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2ffdd-226">発効日</span><span class="sxs-lookup"><span data-stu-id="2ffdd-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-227">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="2ffdd-227">Category</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-228">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="2ffdd-228">Project</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-229">定期売買</span><span class="sxs-lookup"><span data-stu-id="2ffdd-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-230">期間コード</span><span class="sxs-lookup"><span data-stu-id="2ffdd-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-231">通貨</span><span class="sxs-lookup"><span data-stu-id="2ffdd-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-232">販売価格</span><span class="sxs-lookup"><span data-stu-id="2ffdd-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2ffdd-233">2007 - 08 - 28</span><span class="sxs-lookup"><span data-stu-id="2ffdd-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="2ffdd-234">9030</span><span class="sxs-lookup"><span data-stu-id="2ffdd-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="2ffdd-235">月</span><span class="sxs-lookup"><span data-stu-id="2ffdd-235">Month</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-236">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="2ffdd-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-237">500</span><span class="sxs-lookup"><span data-stu-id="2ffdd-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ffdd-238">2007 - 08 - 28</span><span class="sxs-lookup"><span data-stu-id="2ffdd-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-239">SubCat1</span><span class="sxs-lookup"><span data-stu-id="2ffdd-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-240">9030</span><span class="sxs-lookup"><span data-stu-id="2ffdd-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="2ffdd-241">月</span><span class="sxs-lookup"><span data-stu-id="2ffdd-241">Month</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-242">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="2ffdd-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-243">550</span><span class="sxs-lookup"><span data-stu-id="2ffdd-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2ffdd-244">上記の手順を繰り返して、定期売買グループ Sub1 の両方の定期売買に定期売買手数料を作成します。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="2ffdd-245">次の表に、定期売買グループに関連付けられる各定期売買に対して作成されたトランザクションを示します。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2ffdd-246">プロジェクト日付</span><span class="sxs-lookup"><span data-stu-id="2ffdd-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-247">定期売買</span><span class="sxs-lookup"><span data-stu-id="2ffdd-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-248">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="2ffdd-248">Project</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-249">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="2ffdd-249">Category</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-250">開始日</span><span class="sxs-lookup"><span data-stu-id="2ffdd-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-251">終了日</span><span class="sxs-lookup"><span data-stu-id="2ffdd-251">End date</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-252">販売通貨</span><span class="sxs-lookup"><span data-stu-id="2ffdd-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="2ffdd-253">販売価格</span><span class="sxs-lookup"><span data-stu-id="2ffdd-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2ffdd-254">2007 - 07 - 28</span><span class="sxs-lookup"><span data-stu-id="2ffdd-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="2ffdd-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-256">9030</span><span class="sxs-lookup"><span data-stu-id="2ffdd-256">9030</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-257">SubCat1</span><span class="sxs-lookup"><span data-stu-id="2ffdd-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-258">2008 - 01 - 01</span><span class="sxs-lookup"><span data-stu-id="2ffdd-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-259">2008 - 03 - 31</span><span class="sxs-lookup"><span data-stu-id="2ffdd-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-260">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="2ffdd-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-261">550</span><span class="sxs-lookup"><span data-stu-id="2ffdd-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ffdd-262">2008 - 07 - 28</span><span class="sxs-lookup"><span data-stu-id="2ffdd-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="2ffdd-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-264">9030</span><span class="sxs-lookup"><span data-stu-id="2ffdd-264">9030</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-265">SubCat2</span><span class="sxs-lookup"><span data-stu-id="2ffdd-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-266">2008 - 01 - 01</span><span class="sxs-lookup"><span data-stu-id="2ffdd-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-267">2008 - 03 - 31</span><span class="sxs-lookup"><span data-stu-id="2ffdd-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-268">EUR / EUR</span><span class="sxs-lookup"><span data-stu-id="2ffdd-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="2ffdd-269">500</span><span class="sxs-lookup"><span data-stu-id="2ffdd-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2ffdd-270">定期売買 00020\_135 に対する最初のトランザクションでは、特定のプロジェクトとカテゴリの組み合わせに対して設定された定期売買販売価格から、販売価格 EUR 550 が派生します。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="2ffdd-271">定期売買 00021\_135 に対する 2 番目のトランザクションでは、プロジェクト 9030 とカテゴリ SubCat2 の組み合わせに対して価格が設定されていないため、販売価格 EUR 500 がプロジェクトの定期売買販売価格として使用されます。</span><span class="sxs-lookup"><span data-stu-id="2ffdd-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="2ffdd-272">参照</span><span class="sxs-lookup"><span data-stu-id="2ffdd-272">See also</span></span>

[<span data-ttu-id="2ffdd-273">定期売買販売価格の更新および指数化</span><span class="sxs-lookup"><span data-stu-id="2ffdd-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  


