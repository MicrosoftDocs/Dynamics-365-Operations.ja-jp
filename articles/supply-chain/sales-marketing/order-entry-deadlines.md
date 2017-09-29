---
title: "注文入力期限"
description: "この記事は、注文入力期日に関する情報を提供します。 注文入力期日は、顧客注文を当日または翌日に受信されたかのように処理 (および履行) するかどうかを決定する締切り時間です。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOrderEntryDeadlineGroup, InventOrderEntryDeadlineParameters, InventOrderEntryDeadlineTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 7151
ms.assetid: bbc4f9a2-df4b-4d92-9f18-25282a85541f
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 9e9d1912abf9a356542ce2c317fa717bc991dbf9
ms.contentlocale: ja-jp
ms.lasthandoff: 07/18/2017

---

# <a name="order-entry-deadlines"></a><span data-ttu-id="9c22a-104">注文入力期限</span><span class="sxs-lookup"><span data-stu-id="9c22a-104">Order entry deadlines</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9c22a-105">この記事は、注文入力期日に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="9c22a-105">This article provides information about order entry deadlines.</span></span> <span data-ttu-id="9c22a-106">注文入力期日は、顧客注文を当日または翌日に受信されたかのように処理 (および履行) するかどうかを決定する締切り時間です。</span><span class="sxs-lookup"><span data-stu-id="9c22a-106">An order entry deadline is a cut-off time that determines whether a customer order is treated (and fulfilled) as if it was received on the current day or the next day.</span></span>

<span data-ttu-id="9c22a-107">多くの会社では、1 日の特定の時間より前に受信された販売注文のみを、その日に受信したものとしてみなします。</span><span class="sxs-lookup"><span data-stu-id="9c22a-107">In many companies, only sales orders that are received before a certain time of day are treated as if they were received on that day.</span></span> <span data-ttu-id="9c22a-108">その時間以降に受信した注文は、翌営業日に受信したものとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="9c22a-108">Any orders that are received after that time are treated as if they are received on the next business day.</span></span> <span data-ttu-id="9c22a-109">このような注文の締切り時間は、「注文入力期限」と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="9c22a-109">This cut-off time for orders is known as the order entry deadline.</span></span>  

<span data-ttu-id="9c22a-110">注文入力期限は、注文納期の入力に使用されます。</span><span class="sxs-lookup"><span data-stu-id="9c22a-110">Order entry deadlines are used as input for order promising.</span></span> <span data-ttu-id="9c22a-111">したがって、これらを使用すると、注文の出荷に関する顧客の期待を管理できます。</span><span class="sxs-lookup"><span data-stu-id="9c22a-111">Therefore, they help you manage customer expectations about order deliveries.</span></span> <span data-ttu-id="9c22a-112">たとえば、顧客は、特定の時間より前に注文を行うことで、同日に商品の出荷が行われるとみなすことができます。</span><span class="sxs-lookup"><span data-stu-id="9c22a-112">For example, customers can see that, if they place an order with you before a specific time, you will commit to shipping the goods on the same day.</span></span> <span data-ttu-id="9c22a-113">ただし、締め切りが間に合わない場合は、翌営業日にのみ出荷を期待することができます。</span><span class="sxs-lookup"><span data-stu-id="9c22a-113">However, if they miss that deadline, they can expect the shipment only on the next business day.</span></span> <span data-ttu-id="9c22a-114">倉庫機能と配送業者のスケジュールに基づいて注文入力期限を設定します。</span><span class="sxs-lookup"><span data-stu-id="9c22a-114">You set order entry deadlines based on your warehouse capabilities and shipping carrier schedules.</span></span>  

<span data-ttu-id="9c22a-115">**注文入力期限**ページで、1 週間の全曜日における注文入力期限の時間を設定します。</span><span class="sxs-lookup"><span data-stu-id="9c22a-115">On the **Order entry deadlines** page, you set up order entry deadline times for all the days of the week.</span></span> <span data-ttu-id="9c22a-116">その時間以降に受信した注文は、翌日に受信したものとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="9c22a-116">If orders are received after the specified times, they are treated as if they are received on the next day.</span></span> <span data-ttu-id="9c22a-117">既定では、この時間は 23:59 (つまり該当する日が終了する夜 12 時の 1 分前) に設定されています。</span><span class="sxs-lookup"><span data-stu-id="9c22a-117">By default, these times are set to 23:59 (that is, one minute before midnight at the end of the relevant day).</span></span> <span data-ttu-id="9c22a-118">この既定の時間は、実際の出荷または受入の期限時間に合わせて変更できます。</span><span class="sxs-lookup"><span data-stu-id="9c22a-118">You can change the default times so that they coincide with actual ship or receipt deadline times.</span></span>  

<span data-ttu-id="9c22a-119">特定の顧客グループに対して注文入力期限を定義できます。</span><span class="sxs-lookup"><span data-stu-id="9c22a-119">You can define order entry deadlines for a specific group of customers.</span></span> <span data-ttu-id="9c22a-120">たとえば、一部の顧客グループの注文入力期限を大多数の顧客よりも延ばしたい場合があります。</span><span class="sxs-lookup"><span data-stu-id="9c22a-120">For example, you might want a specific group of customers to have order entry deadlines that are later than those of other customers.</span></span> <span data-ttu-id="9c22a-121">この場合、最初に**注文入力期限グループ**ページで、注文入力期限のグループを定義します。</span><span class="sxs-lookup"><span data-stu-id="9c22a-121">In this case, you first define groups for order entry deadlines on the **Order entry deadline groups** page.</span></span> <span data-ttu-id="9c22a-122">その後、**顧客**ページの顧客に対してグループを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="9c22a-122">You then assign the groups to customers on the **Customers** page.</span></span>  

<span data-ttu-id="9c22a-123">会社に複数のサイトがある場合は、サイトごとに注文入力期限を設定できます。</span><span class="sxs-lookup"><span data-stu-id="9c22a-123">If your company consists of several sites, you can set up order entry deadlines for each site.</span></span> <span data-ttu-id="9c22a-124">サイトのタイム ゾーンがそれぞれに異なる場合は、注文入力期限は各サイトのタイム ゾーンで設定されます。</span><span class="sxs-lookup"><span data-stu-id="9c22a-124">If the sites are located in different time zones, the order entry deadlines are set up in each site's time zone.</span></span> <span data-ttu-id="9c22a-125">ただし、販売注文と販売見積を処理する場合は、注文入力期限が**出荷可能日および入荷可能日付**ページのタイム ゾーンに変換されます。</span><span class="sxs-lookup"><span data-stu-id="9c22a-125">However, when you work with sales orders and sales quotations, the order entry deadline is converted to your time zone on the **Available ship and receipt dates** page.</span></span>  

<span data-ttu-id="9c22a-126">**注文入力期日の組み合わせの有効化** ページで、サイトと注文入力期限グループの許可する組み合わせを定義します。</span><span class="sxs-lookup"><span data-stu-id="9c22a-126">On the **Activate order entry deadline combinations** page, you define the combinations of sites and order entry deadline groups that are allowed.</span></span>

## <a name="example-order-entry-deadline"></a><span data-ttu-id="9c22a-127">例 : 注文入力期限</span><span class="sxs-lookup"><span data-stu-id="9c22a-127">Example: Order entry deadline</span></span>
<span data-ttu-id="9c22a-128">火曜日の注文入力期限を 16:00 に設定します。</span><span class="sxs-lookup"><span data-stu-id="9c22a-128">The order entry deadline on Tuesdays has been set to 16:00.</span></span> <span data-ttu-id="9c22a-129">特定の火曜日の 17:00 に、現在の日付を出荷日として設定しようとします。</span><span class="sxs-lookup"><span data-stu-id="9c22a-129">On a particular Tuesday, at 17:00, you try to set the current date as the ship date.</span></span> <span data-ttu-id="9c22a-130">(この例ではリード タイムはないことに注意してください) [**配送日の管理**] チェック ボックスがオンの場合、日付が無効であるとの警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9c22a-130">(Note that there is no lead time for this example.) If the **Delivery date control** check box is selected, you receive a warning that states that the date isn't valid.</span></span> <span data-ttu-id="9c22a-131">この警告は**出荷可能日および入荷可能日付**ページに表示され、代替日付を選択することができます。</span><span class="sxs-lookup"><span data-stu-id="9c22a-131">This warning appears on the **Available ship and receipt dates** page, where you can then select alternative dates.</span></span>

## <a name="example-different-order-entry-deadlines-per-site"></a><span data-ttu-id="9c22a-132">例 : 各サイトで注文入力期限が異なる場合</span><span class="sxs-lookup"><span data-stu-id="9c22a-132">Example: Different order entry deadlines per site</span></span>
<span data-ttu-id="9c22a-133">この法人は、2 種類のサイトで構成されます。</span><span class="sxs-lookup"><span data-stu-id="9c22a-133">Your company consists of two sites.</span></span> <span data-ttu-id="9c22a-134">サイトは、次の表に示すように、異なるタイム ゾーンにあります。</span><span class="sxs-lookup"><span data-stu-id="9c22a-134">The sites are located in different time zones, as shown in the following table.</span></span>

| <span data-ttu-id="9c22a-135">サイト A</span><span class="sxs-lookup"><span data-stu-id="9c22a-135">Site A</span></span>                      | <span data-ttu-id="9c22a-136">サイト B</span><span class="sxs-lookup"><span data-stu-id="9c22a-136">Site B</span></span>                      |
|-----------------------------|-----------------------------|
| <span data-ttu-id="9c22a-137">カリフォルニア</span><span class="sxs-lookup"><span data-stu-id="9c22a-137">California</span></span>                  | <span data-ttu-id="9c22a-138">フロリダ</span><span class="sxs-lookup"><span data-stu-id="9c22a-138">Florida</span></span>                     |
| <span data-ttu-id="9c22a-139">PST (太平洋標準時)</span><span class="sxs-lookup"><span data-stu-id="9c22a-139">PST (Pacific Standard Time)</span></span> | <span data-ttu-id="9c22a-140">EST (東部標準時)</span><span class="sxs-lookup"><span data-stu-id="9c22a-140">EST (Eastern Standard Time)</span></span> |

<span data-ttu-id="9c22a-141">サイト A とサイト B には、次の注文入力期限が定義されています。</span><span class="sxs-lookup"><span data-stu-id="9c22a-141">Sites A and B have defined the following order entry deadlines.</span></span>

| <span data-ttu-id="9c22a-142">曜日</span><span class="sxs-lookup"><span data-stu-id="9c22a-142">Day of the week</span></span>             | <span data-ttu-id="9c22a-143">注文入力期限 (PST)</span><span class="sxs-lookup"><span data-stu-id="9c22a-143">A: Order entry deadlines (PST)</span></span> | <span data-ttu-id="9c22a-144">注文入力期限 (EST)</span><span class="sxs-lookup"><span data-stu-id="9c22a-144">B: Order entry deadlines (EST)</span></span> |
|-----------------------------|--------------------------------|--------------------------------|
| <span data-ttu-id="9c22a-145">月曜</span><span class="sxs-lookup"><span data-stu-id="9c22a-145">Monday</span></span>                      | <span data-ttu-id="9c22a-146">13:00</span><span class="sxs-lookup"><span data-stu-id="9c22a-146">13:00</span></span>                          | <span data-ttu-id="9c22a-147">14:00</span><span class="sxs-lookup"><span data-stu-id="9c22a-147">14:00</span></span>                          |
| <span data-ttu-id="9c22a-148">火曜</span><span class="sxs-lookup"><span data-stu-id="9c22a-148">Tuesday</span></span>                     | <span data-ttu-id="9c22a-149">13:00</span><span class="sxs-lookup"><span data-stu-id="9c22a-149">13:00</span></span>                          | <span data-ttu-id="9c22a-150">14:00</span><span class="sxs-lookup"><span data-stu-id="9c22a-150">14:00</span></span>                          |
| <span data-ttu-id="9c22a-151">水曜</span><span class="sxs-lookup"><span data-stu-id="9c22a-151">Wednesday</span></span>                   | <span data-ttu-id="9c22a-152">13:00</span><span class="sxs-lookup"><span data-stu-id="9c22a-152">13:00</span></span>                          | <span data-ttu-id="9c22a-153">14:00</span><span class="sxs-lookup"><span data-stu-id="9c22a-153">14:00</span></span>                          |
| <span data-ttu-id="9c22a-154">木曜</span><span class="sxs-lookup"><span data-stu-id="9c22a-154">Thursday</span></span>                    | <span data-ttu-id="9c22a-155">13:00</span><span class="sxs-lookup"><span data-stu-id="9c22a-155">13:00</span></span>                          | <span data-ttu-id="9c22a-156">14:00</span><span class="sxs-lookup"><span data-stu-id="9c22a-156">14:00</span></span>                          |
| <span data-ttu-id="9c22a-157">金曜</span><span class="sxs-lookup"><span data-stu-id="9c22a-157">Friday</span></span>                      | <span data-ttu-id="9c22a-158">13:00</span><span class="sxs-lookup"><span data-stu-id="9c22a-158">13:00</span></span>                          | <span data-ttu-id="9c22a-159">14:00</span><span class="sxs-lookup"><span data-stu-id="9c22a-159">14:00</span></span>                          |

<span data-ttu-id="9c22a-160">注文処理担当者はユタ州にいます。タイム ゾーンは MST (山地標準時) です。</span><span class="sxs-lookup"><span data-stu-id="9c22a-160">You're an order processor in Utah, where the time zone is MST (Mountain Standard Time).</span></span> <span data-ttu-id="9c22a-161">つまり、サイト A で MST 14:00 より前、サイト B で MST 12:00 より前に注文を行えば、どちらのサイトでも注文入力期限に間に合います。</span><span class="sxs-lookup"><span data-stu-id="9c22a-161">Therefore, provided that you place orders with site A before 14:00 MST and place orders with site B before 12:00 MST, you meet the order entry deadlines for both sites.</span></span>  

<span data-ttu-id="9c22a-162">次の表に、サイト A とサイト B の注文入力期限がどのように MST 時間に変換されるかを示します。</span><span class="sxs-lookup"><span data-stu-id="9c22a-162">The following table shows how the order entry deadlines for sites A and B are converted to MST time.</span></span>

| <span data-ttu-id="9c22a-163">サイト A: PST</span><span class="sxs-lookup"><span data-stu-id="9c22a-163">Site A: PST</span></span>         | <span data-ttu-id="9c22a-164">サイト A: MST</span><span class="sxs-lookup"><span data-stu-id="9c22a-164">Site A: MST</span></span>        | <span data-ttu-id="9c22a-165">サイト B: EST</span><span class="sxs-lookup"><span data-stu-id="9c22a-165">Site B: EST</span></span>           | <span data-ttu-id="9c22a-166">サイト B: MST</span><span class="sxs-lookup"><span data-stu-id="9c22a-166">Site B: MST</span></span>        |
|---------------------|--------------------|-----------------------|--------------------|
| <span data-ttu-id="9c22a-167">13:00</span><span class="sxs-lookup"><span data-stu-id="9c22a-167">13:00</span></span>               | <span data-ttu-id="9c22a-168">14:00</span><span class="sxs-lookup"><span data-stu-id="9c22a-168">14:00</span></span>              | <span data-ttu-id="9c22a-169">14:00</span><span class="sxs-lookup"><span data-stu-id="9c22a-169">14:00</span></span>                 | <span data-ttu-id="9c22a-170">12:00</span><span class="sxs-lookup"><span data-stu-id="9c22a-170">12:00</span></span>              |

<span data-ttu-id="9c22a-171">**注記:** 夏時間調整が有効である場合は、それに合わせて注文入力期限も調整されます。</span><span class="sxs-lookup"><span data-stu-id="9c22a-171">**Note:** If adjustment for daylight saving time is in effect, the order entry deadlines are adjusted accordingly.</span></span>

## <a name="example-same-order-entry-deadline-per-site"></a><span data-ttu-id="9c22a-172">例 : 各サイトで注文入力期限が同じである場合</span><span class="sxs-lookup"><span data-stu-id="9c22a-172">Example: Same order entry deadline per site</span></span>
<span data-ttu-id="9c22a-173">この法人は、2 種類のサイトで構成されます。</span><span class="sxs-lookup"><span data-stu-id="9c22a-173">Your company consists of two sites.</span></span> <span data-ttu-id="9c22a-174">サイトは、次の表に示すように、異なるタイム ゾーンにあります。</span><span class="sxs-lookup"><span data-stu-id="9c22a-174">The sites are located in different time zones, as shown in the following table.</span></span>

| <span data-ttu-id="9c22a-175">サイト A</span><span class="sxs-lookup"><span data-stu-id="9c22a-175">Site A</span></span>                      | <span data-ttu-id="9c22a-176">サイト B</span><span class="sxs-lookup"><span data-stu-id="9c22a-176">Site B</span></span>                      |
|-----------------------------|-----------------------------|
| <span data-ttu-id="9c22a-177">カリフォルニア</span><span class="sxs-lookup"><span data-stu-id="9c22a-177">California</span></span>                  | <span data-ttu-id="9c22a-178">フロリダ</span><span class="sxs-lookup"><span data-stu-id="9c22a-178">Florida</span></span>                     |
| <span data-ttu-id="9c22a-179">PST (太平洋標準時)</span><span class="sxs-lookup"><span data-stu-id="9c22a-179">PST (Pacific Standard Time)</span></span> | <span data-ttu-id="9c22a-180">EST (東部標準時)</span><span class="sxs-lookup"><span data-stu-id="9c22a-180">EST (Eastern Standard Time)</span></span> |

<span data-ttu-id="9c22a-181">サイト A とサイト B には、次の注文入力期限が定義されています。</span><span class="sxs-lookup"><span data-stu-id="9c22a-181">Sites A and B have defined the following order entry deadlines.</span></span>

| <span data-ttu-id="9c22a-182">曜日</span><span class="sxs-lookup"><span data-stu-id="9c22a-182">Day of the week</span></span> | <span data-ttu-id="9c22a-183">PST および EST</span><span class="sxs-lookup"><span data-stu-id="9c22a-183">PST and EST</span></span> |
|-----------------|-------------|
| <span data-ttu-id="9c22a-184">月曜</span><span class="sxs-lookup"><span data-stu-id="9c22a-184">Monday</span></span>          | <span data-ttu-id="9c22a-185">13:00</span><span class="sxs-lookup"><span data-stu-id="9c22a-185">13:00</span></span>       |
| <span data-ttu-id="9c22a-186">火曜</span><span class="sxs-lookup"><span data-stu-id="9c22a-186">Tuesday</span></span>         | <span data-ttu-id="9c22a-187">13:00</span><span class="sxs-lookup"><span data-stu-id="9c22a-187">13:00</span></span>       |
| <span data-ttu-id="9c22a-188">水曜</span><span class="sxs-lookup"><span data-stu-id="9c22a-188">Wednesday</span></span>       | <span data-ttu-id="9c22a-189">13:00</span><span class="sxs-lookup"><span data-stu-id="9c22a-189">13:00</span></span>       |
| <span data-ttu-id="9c22a-190">木曜</span><span class="sxs-lookup"><span data-stu-id="9c22a-190">Thursday</span></span>        | <span data-ttu-id="9c22a-191">13:00</span><span class="sxs-lookup"><span data-stu-id="9c22a-191">13:00</span></span>       |
| <span data-ttu-id="9c22a-192">金曜</span><span class="sxs-lookup"><span data-stu-id="9c22a-192">Friday</span></span>          | <span data-ttu-id="9c22a-193">13:00</span><span class="sxs-lookup"><span data-stu-id="9c22a-193">13:00</span></span>       |

<span data-ttu-id="9c22a-194">注文処理担当者はユタ州にいます。タイム ゾーンは MST です。</span><span class="sxs-lookup"><span data-stu-id="9c22a-194">You're an order processor in Utah, where the time zone is MST.</span></span> <span data-ttu-id="9c22a-195">つまり、サイト A で MST 14:00 より前、サイト B で MST 11:00 より前に注文を行えば、どちらのサイトでも注文入力期限に間に合います。</span><span class="sxs-lookup"><span data-stu-id="9c22a-195">Therefore, provided that you place orders with site A before 14:00 MST and place orders with site B before 11:00 MST, you meet the order entry deadlines for both sites.</span></span> 

<span data-ttu-id="9c22a-196">次の表に、サイト A とサイト B の注文入力期限がどのように MST 時間に変換されるかを示します。</span><span class="sxs-lookup"><span data-stu-id="9c22a-196">The following table shows how the order entry deadlines for sites A and B are converted to MST time.</span></span>

| <span data-ttu-id="9c22a-197">サイト A: PST</span><span class="sxs-lookup"><span data-stu-id="9c22a-197">Site A: PST</span></span>         | <span data-ttu-id="9c22a-198">サイト A: MST</span><span class="sxs-lookup"><span data-stu-id="9c22a-198">Site A: MST</span></span>        | <span data-ttu-id="9c22a-199">サイト B: EST</span><span class="sxs-lookup"><span data-stu-id="9c22a-199">Site B: EST</span></span>           | <span data-ttu-id="9c22a-200">サイト B: MST</span><span class="sxs-lookup"><span data-stu-id="9c22a-200">Site B: MST</span></span>        |
|---------------------|--------------------|-----------------------|--------------------|
| <span data-ttu-id="9c22a-201">13:00</span><span class="sxs-lookup"><span data-stu-id="9c22a-201">13:00</span></span>               | <span data-ttu-id="9c22a-202">14:00</span><span class="sxs-lookup"><span data-stu-id="9c22a-202">14:00</span></span>              | <span data-ttu-id="9c22a-203">13:00</span><span class="sxs-lookup"><span data-stu-id="9c22a-203">13:00</span></span>                 | <span data-ttu-id="9c22a-204">11:00</span><span class="sxs-lookup"><span data-stu-id="9c22a-204">11:00</span></span>              |

<span data-ttu-id="9c22a-205">**注記:** 夏時間調整が有効である場合は、それに合わせて注文入力期限も調整されます。</span><span class="sxs-lookup"><span data-stu-id="9c22a-205">**Note:** If adjustment for daylight saving time is in effect, the order entry deadlines are adjusted accordingly.</span></span>

<a name="see-also"></a><span data-ttu-id="9c22a-206">参照</span><span class="sxs-lookup"><span data-stu-id="9c22a-206">See also</span></span>
--------

[<span data-ttu-id="9c22a-207">配送スケジュール</span><span class="sxs-lookup"><span data-stu-id="9c22a-207">Delivery schedules</span></span>](delivery-schedules.md)




