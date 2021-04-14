---
title: 顧客集荷の時間帯の作成と更新
description: このトピックでは、Commerce 本社で顧客集配時間帯を作成、構成、および更新する方法について説明します。
author: anupamar-ms
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.15 update
ms.openlocfilehash: c3da7474f9a61e97ee11688a18cb91a5ad1ccb5c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791168"
---
# <a name="create-and-update-time-slots-for-customer-pickup"></a><span data-ttu-id="f83fb-103">顧客集荷の時間帯の作成と更新</span><span class="sxs-lookup"><span data-stu-id="f83fb-103">Create and update time slots for customer pickup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f83fb-104">このトピックでは、Commerce 本社で顧客集配時間帯を作成、構成、および更新する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f83fb-104">This topic describes how to create, configure, and update customer pickup time slots in Commerce headquarters.</span></span>

<span data-ttu-id="f83fb-105">時間帯機能を使用すると、小売業者は、顧客集配出荷モードが有効になっている品目の時間帯を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-105">The time slot feature gives retailers a way to define a time slot for items that the customer pickup delivery mode is turned on for.</span></span> <span data-ttu-id="f83fb-106">時間帯タイムスロットを使用すると、小売業者は注文をストアから集荷する際の日付と時刻を定義できます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-106">Time slots let retailers define the days and times when orders can be picked up from a store.</span></span> <span data-ttu-id="f83fb-107">小売業者は、特定の期間に集荷できる注文の数を定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-107">Retailers can also define the number of orders that can be picked up during a given period.</span></span> <span data-ttu-id="f83fb-108">このようにして、小売業者は特定の日に指定された期間に集荷できる注文の数を制限することができます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-108">In this way, retailers can limit the number of orders that can be picked up on a given day and at a given time.</span></span> <span data-ttu-id="f83fb-109">その結果、顧客に対して品質の向上を実感できます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-109">The result is a better-quality experience for their customers.</span></span>

> [!NOTE]
> <span data-ttu-id="f83fb-110">時間帯機能は、Microsoft Dynamics 365 Commerce バージョン 10.0.15 以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-110">The time slot feature is available in Microsoft Dynamics 365 Commerce version 10.0.15 and later.</span></span>

<span data-ttu-id="f83fb-111">次の図は、電子商取引のチェックアウト時に選択される時間帯の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="f83fb-111">The following illustration shows an example of time slot selection during e-commerce checkout.</span></span>

![電子商取引のチェックアウト時の時間帯の選択例](../dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="time-slot-properties"></a><span data-ttu-id="f83fb-113">時間帯のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f83fb-113">Time slot properties</span></span>

<span data-ttu-id="f83fb-114">時間帯は、顧客が特定のストアまたは場所から注文を取得することを選択できる特定の間隔です。</span><span class="sxs-lookup"><span data-stu-id="f83fb-114">A time slot is a specific interval when a customer can choose to pick up an order from a specific store or location.</span></span> <span data-ttu-id="f83fb-115">時間帯管理機能は、Dynamics 365 Commerce で顧客集荷配送モードがコンフィギュレーションされている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-115">The time slot management feature is available only when the customer pickup delivery mode is configured in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f83fb-116">時間帯は、次のプロパティを使用して定義します。</span><span class="sxs-lookup"><span data-stu-id="f83fb-116">A time slot is defined by using the following properties:</span></span>

- <span data-ttu-id="f83fb-117">**配送モード** – 時間帯が適用される集荷配送モードを指定します。</span><span class="sxs-lookup"><span data-stu-id="f83fb-117">**Mode of delivery** – Specify the pickup mode of delivery that the time slot applies to.</span></span>
- <span data-ttu-id="f83fb-118">**最小日数** と **最大日数** – 注文が行われた日付を基準に、集配対象として選択できる最も早い日付と最も遅い日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="f83fb-118">**Minimum Days** and **Maximum Days** – Specify the earliest and latest dates that can be selected for pickup relative to the date when the order is placed.</span></span> 

    <span data-ttu-id="f83fb-119">**最小日数** プロパティは、小売業者が集荷の準備が整う前に注文を処理するのに十分な時間があることを保証します。</span><span class="sxs-lookup"><span data-stu-id="f83fb-119">The **Minimum Days** property ensures that there is enough time for the retailer to process the order before it's ready for pickup.</span></span> <span data-ttu-id="f83fb-120">**最大日数** プロパティにより、ユーザーは将来の日付を選択できなくなります。</span><span class="sxs-lookup"><span data-stu-id="f83fb-120">The **Maximum Days** property ensures that the user can't select a date that is too far in the future.</span></span> <span data-ttu-id="f83fb-121">たとえば、最小値が **1** に設定されている場合、9 月 20 日に注文が行われると、その注文が集荷可能な最も早い日は次の適格日 (9 月 21 日) になります。</span><span class="sxs-lookup"><span data-stu-id="f83fb-121">For example, if the minimum value is set to **1**, and an order is placed on September 20, the earliest day that the order will be available for pickup is the next eligible day (September 21).</span></span> <span data-ttu-id="f83fb-122">同様の方法で、最大値を設定することにより、注文を集荷できる最大日数を定義できます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-122">In a similar way, by setting a maximum value, you can define the maximum number of days that an order can be picked up.</span></span> <span data-ttu-id="f83fb-123">最小値と最大値が定義されている場合、サイトのユーザーは、各自のチェックアウト時に、特定の日付のセットのみを表示および選択できます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-123">When minimum and maximum values are defined, site users can see and select only a specific set of days during their checkout experience.</span></span>

    <span data-ttu-id="f83fb-124">最小値は、1 未満の 10 進値に設定できます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-124">You can set the minimum value to a decimal value that is less than 1.</span></span> <span data-ttu-id="f83fb-125">たとえば、発注後 4 時間使用可能な集配の場合は、最小値を **0.17** (= 4 ÷ 24、小数点以下 2 桁に切り上げ) に設定します。</span><span class="sxs-lookup"><span data-stu-id="f83fb-125">For example, if pickup is available four hours after an order is placed, set the minimum value to **0.17** (= 4 ÷ 24, rounded up to two decimal places).</span></span> <span data-ttu-id="f83fb-126">ただし、最小値を 1 より大きい 10 進値に設定した場合は、常に最も近い整数に丸められます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-126">However, if you set the minimum value to a decimal value that is more than 1, it's always rounded up to the nearest whole number.</span></span> <span data-ttu-id="f83fb-127">たとえば、値 **1.2** は **2** に切り上げられます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-127">For example, a value of **1.2** will be rounded up to **2**.</span></span> <span data-ttu-id="f83fb-128">同様に、最大値を 10 進値に設定した場合は、常に最も近い整数に丸められます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-128">Similarly, if you set the maximum value to a decimal value, it's always rounded up to the nearest whole number.</span></span> 

- <span data-ttu-id="f83fb-129">**開始日** および **終了日** – 時間帯の開始日と終了日を指定します。</span><span class="sxs-lookup"><span data-stu-id="f83fb-129">**Start Date** and **End Date** – Specify the start and end dates of the time slot.</span></span> <span data-ttu-id="f83fb-130">各時間帯エントリには、開始日と終了日があります。</span><span class="sxs-lookup"><span data-stu-id="f83fb-130">Each time slot entry has a start date and an end date.</span></span> <span data-ttu-id="f83fb-131">したがって、1 年にさまざまな時間帯を追加することができます (たとえば、休日の時間帯の集荷)。</span><span class="sxs-lookup"><span data-stu-id="f83fb-131">Therefore, you have the flexibility to add different time slots throughout the year (for example, pickups during holiday hours).</span></span> <span data-ttu-id="f83fb-132">注文が行われた後に、時間帯の開始日と日付を変更すると、その変更はその注文に適用されません。</span><span class="sxs-lookup"><span data-stu-id="f83fb-132">If a time slot's start and dates are changed after an order is placed, the changes won't apply to that order.</span></span> <span data-ttu-id="f83fb-133">開始日と終了日を定義する場合は、ストアの休業日 (クリスマス日など) を考慮し、その日に対して時間枠が定義されていないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f83fb-133">When you define start and end dates, you must consider store closure dates (for example, Christmas day) and ensure that time slots aren't defined for those days.</span></span>
- <span data-ttu-id="f83fb-134">**集荷の有効時間** – 集荷が可能な期間を指定します。</span><span class="sxs-lookup"><span data-stu-id="f83fb-134">**Active Hours of Pickup** – Specify the period when pickup is allowed.</span></span> <span data-ttu-id="f83fb-135">たとえば、集荷時間は午後 2 時から午後 5 時までの間である場合があります。</span><span class="sxs-lookup"><span data-stu-id="f83fb-135">For example, the pickup times might be between 2 PM and 5 PM every day.</span></span> <span data-ttu-id="f83fb-136">このプロパティを使用すると、集荷時間がストア時間に依存しないようにできます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-136">This property enables the pickup times to be independent of store hours.</span></span> <span data-ttu-id="f83fb-137">したがって、小売業者は、特定の業務要件を満たす集配時間を構成することができます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-137">Therefore, the retailer can configure pickup times that meet its specific business requirements.</span></span> <span data-ttu-id="f83fb-138">集荷の有効時間を定義する場合は、保管時間を考慮して、ストアが決算されるときに集荷時間が定義されないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f83fb-138">When you define the active hours of pickup, you must consider store hours and ensure that pickup times aren't defined for times when the store is closed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f83fb-139">ストアの集荷時間は、適切なストアの時間帯で定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f83fb-139">The hours for store pickup must be defined in the time zone of the appropriate store.</span></span>

- <span data-ttu-id="f83fb-140">**時間帯の間隔** – 各時間枠に割り当てることができる期間を指定します。</span><span class="sxs-lookup"><span data-stu-id="f83fb-140">**Time Slot Interval** – Specify the duration that can be allotted to each time slot.</span></span> <span data-ttu-id="f83fb-141">たとえば、各時間枠の期間を 15 分、30 分、または 1 時間の単位で指定することができます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-141">For example, the duration of each time slot might be in increments of 15 minutes, 30 minutes, or one hour.</span></span> <span data-ttu-id="f83fb-142">タイム スロットの値が 0 の場合、開始時刻から終了時刻の間の期間全体でタイム スロットを使用できます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-142">If time slot value is 0, the time slot is available for the entire duration between the start and end time.</span></span>
- <span data-ttu-id="f83fb-143">**間隔ごとの時間帯** – 各時間帯間隔で集配できる顧客または注文の数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f83fb-143">**Slots Per Interval** – Specify the number of customer or orders that can be served for pickup during each time slot interval.</span></span> <span data-ttu-id="f83fb-144">たとえば、**1**、**2**、**3**、またはその他の任意の整数を入力します。</span><span class="sxs-lookup"><span data-stu-id="f83fb-144">For example, enter **1**, **2**, **3**, or any other whole number.</span></span>
- <span data-ttu-id="f83fb-145">**有効日** – 集荷時間帯が有効な曜日を指定します。</span><span class="sxs-lookup"><span data-stu-id="f83fb-145">**Active Days** – Specify the days of the week when the pickup time slots are active.</span></span> <span data-ttu-id="f83fb-146">このプロパティを使用すると、集荷注文をサポートする必要がある日を小売業者が定義できます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-146">This property lets the retailer define the days when it wants to support pickup orders.</span></span>
- <span data-ttu-id="f83fb-147">**小売チャネル** – 小売チャネルを指定します。</span><span class="sxs-lookup"><span data-stu-id="f83fb-147">**Retail Channels** – Specify the retail channels.</span></span> <span data-ttu-id="f83fb-148">各時間帯は、1 つ以上の小売ストアに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-148">Each time slot can be associated with one or more retail stores.</span></span> <span data-ttu-id="f83fb-149">各ストアの工程時間に応じて、1 つ以上の時間帯エントリを作成し、チャネルに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-149">Depending on each store's hours of operation, one or more time slot entries can be created and associated with a channel.</span></span> 

<!-- ![HQ Timeslot overview](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

<span data-ttu-id="f83fb-150">チャネルごとに 1 つの時間帯テンプレートのみをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-150">Only one time slot template can be configured per channel.</span></span> <span data-ttu-id="f83fb-151">これらチャネルには、従来型の店舗、コール センター、モバイル デバイス、および電子商取引サイトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-151">These channels include brick-and-mortar stores, call centers, mobile devices, and e-Commerce sites.</span></span>

## <a name="configure-the-time-slot-feature-in-commerce-headquarters"></a><span data-ttu-id="f83fb-152">Commerce 本社の時間帯機能のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="f83fb-152">Configure the time slot feature in Commerce headquarters</span></span>

<span data-ttu-id="f83fb-153">時間帯は、販売時点管理 (POS) および E コマース チャネルがそれらを参照できるように、Commerce 本社の集荷配送モードごとに定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f83fb-153">Time slots must be defined for each pickup mode of delivery in Commerce headquarters, so that point of sale (POS) and e-commerce channels can reference them.</span></span>

- <span data-ttu-id="f83fb-154">各ストアまたはチャネルに関連付けることができる時間帯テンプレートは 1 つだけです。</span><span class="sxs-lookup"><span data-stu-id="f83fb-154">Only one time slot template can be associated with each store or channel.</span></span>
- <span data-ttu-id="f83fb-155">作成される各時間帯は、各テンプレートの各配送モードで一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="f83fb-155">Each time slot that is created should be unique to each delivery mode in each template.</span></span>
- <span data-ttu-id="f83fb-156">時間帯機能を構成すると、選択した店舗または店舗グループで時間帯のカレンダーを使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="f83fb-156">After the time slot feature is configured, the time slot calendar will be available to the selected stores or store groups.</span></span> <span data-ttu-id="f83fb-157">また、POS で参照するために表示されます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-157">It will also be visible at the POS, for reference.</span></span>

<span data-ttu-id="f83fb-158">Commerce 本社の時間帯機能を構成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f83fb-158">To configure the time slot feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f83fb-159">**Commerce** \> **チャネルの設定** \> **店舗集配時間帯** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f83fb-159">Go to **Commerce** \> **Channel setup** \> **Store pickup time slot**.</span></span>
1. <span data-ttu-id="f83fb-160">**新規** を選択して、新しい時間帯テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="f83fb-160">Select **New** to create a new time slot template.</span></span> <span data-ttu-id="f83fb-161">既存のテンプレートを使用するには、左ウィンドウでテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="f83fb-161">To use an existing template, select the template in the left pane.</span></span>
1. <span data-ttu-id="f83fb-162">**時間帯 ID** および **説明** のフィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="f83fb-162">Enter values in the **Time Slot ID** and **Description** fields.</span></span>
1. <span data-ttu-id="f83fb-163">**注文の集荷 - 時間の設定** クイック タブで、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f83fb-163">On the **Order Pickup - Time Settings** FastTab, select **Add**.</span></span>
1. <span data-ttu-id="f83fb-164">**注文の集荷 - 時間の設定** ダイアログ ボックスで、日付範囲、出荷方法、出荷時の有効時間、有効な日数、時間帯の間隔、間隔ごとの時間帯などの設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="f83fb-164">In the **Order Pickup - Time Settings** dialog box, define the date range, mode of delivery, active hours of delivery, active days, time slot interval, slots per interval, and other settings.</span></span>

    <span data-ttu-id="f83fb-165">近い将来に時間帯が固定される場合は、**終了日** フィールドを **設定しない** に設定します。</span><span class="sxs-lookup"><span data-stu-id="f83fb-165">If time slots will be static for the foreseeable future, set the **End Date** field to **Never**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f83fb-166">複数のテンプレートを作成できますが、1 つのチャネルまたはストアに関連付けることができるテンプレートは 1 つだけです。</span><span class="sxs-lookup"><span data-stu-id="f83fb-166">You can create multiple templates, but only one template can be associated with a single channel or store.</span></span>

    ![注文の集荷 - 時間設定ダイアログ ボックス](../dev-itpro/media/Curbside_timeslot_Settings_Page.PNG)

1. <span data-ttu-id="f83fb-168">完了したら、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f83fb-168">When you've finished, select **OK**.</span></span>
1. <span data-ttu-id="f83fb-169">1 日の時間帯が異なる場合は、**注文の集荷 - 時間の設定** クイック タブで追加のエントリを作成して、日付と時刻が重複しないようにします。</span><span class="sxs-lookup"><span data-stu-id="f83fb-169">If the time slots in a day will vary, create additional entries on the **Order Pickup - Time Settings** FastTab to ensure that the dates and times don't overlap.</span></span>
1. <span data-ttu-id="f83fb-170">**小売チャネル** クイック タブで **追加** を選択し、使用するストアまたはチャネルに時間帯テンプレートを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-170">On the **Retail Channels** FastTab, select **Add** to associate the time slot template with the stores or channels where it will be used.</span></span>
1. <span data-ttu-id="f83fb-171">**組織ノードの選択** ダイアログ ボックスで、矢印ボタンを使用してテンプレートが関連付けられているストア、地域、および組織を選択 (または選択を解除) します。</span><span class="sxs-lookup"><span data-stu-id="f83fb-171">In the **Choose organization nodes** dialog box, use the arrow buttons to select (or clear the selection of) the stores, regions, and organizations that the template should be associated with.</span></span>

    <!-- ![HQ Timeslot overview](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

1. <span data-ttu-id="f83fb-172">完了したら、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f83fb-172">When you've finished, select **OK**.</span></span>
1. <span data-ttu-id="f83fb-173">**配送スケジュール** ページで、**1070** および **1135** ジョブを実行してチャネル データベースにデータを同期します。</span><span class="sxs-lookup"><span data-stu-id="f83fb-173">On the **Distribution schedule** page, run the **1070** and **1135** jobs to sync the data to the channels.</span></span>

## <a name="time-slot-selection-for-pos-orders"></a><span data-ttu-id="f83fb-174">POS 注文の時間帯の選択</span><span class="sxs-lookup"><span data-stu-id="f83fb-174">Time slot selection for POS orders</span></span>

<span data-ttu-id="f83fb-175">POS で注文または注文明細行が集荷に対して識別されると、レジ担当者は集荷のストアまたは場所、および日付と時間帯を選択できます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-175">At the POS, when an order or order line is identified for pickup, the cashier can select the pickup store or location, and a date and time slot.</span></span> <span data-ttu-id="f83fb-176">顧客が別の店舗の集荷注文を持っている場合、レジ担当者はその店舗で集荷できる日付を選択できます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-176">If a customer has a pickup order for a different store, the cashier can select dates when the pickup will be available in that store.</span></span> <span data-ttu-id="f83fb-177">店舗ルックアップでは、日付と店舗の営業時間を参照できます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-177">The store lookup will provide a reference to the dates and store times.</span></span>

<span data-ttu-id="f83fb-178">次の図は、POS 注文で選択された時間帯の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="f83fb-178">The following illustration shows an example of time slot selection for a POS order.</span></span>

![POS 注文の時間帯の選択例](../dev-itpro/media/Curbside_timeslot_POS.png)

## <a name="time-slot-selection-for-e-commerce-orders"></a><span data-ttu-id="f83fb-180">電子商取引注文の時間帯の選択</span><span class="sxs-lookup"><span data-stu-id="f83fb-180">Time slot selection for e-commerce orders</span></span>

<span data-ttu-id="f83fb-181">電子商取引の注文に対して時間帯を選択できるようにする方法については、[集荷情報モジュール](../pickup-info-module.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f83fb-181">For information about how to make time slot selection available for e-commerce orders, see [Pickup information module](../pickup-info-module.md).</span></span>

> [!NOTE]
> <span data-ttu-id="f83fb-182">ユーザーは、集荷情報モジュールがそのページに追加されている場合にのみ、Commerce サイトのチェックアウト ページの集荷時間帯を表示または編集できます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-182">Users can view or edit pickup time slots on a Commerce site's checkout page only if the pickup information module has been added to that page.</span></span> <span data-ttu-id="f83fb-183">チェックアウト ページに集荷情報モジュールが含まれていない場合は、ユーザーが時間帯情報を指定または表示できないように、注文が発注されます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-183">If the checkout page doesn't include the pickup information module, orders will be placed without letting users specify or view time slot information.</span></span>

<span data-ttu-id="f83fb-184">次の図は、集荷時間帯が選択されている電子商取引の注文の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="f83fb-184">The following illustration shows an example of an e-commerce order where a pickup time slot has been selected.</span></span>

![集荷時間帯が選択されている e コマース注文の例](../dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="time-slot-selection-for-call-center-orders"></a><span data-ttu-id="f83fb-186">コールセンター注文の時間帯の選択</span><span class="sxs-lookup"><span data-stu-id="f83fb-186">Time slot selection for call center orders</span></span>

<span data-ttu-id="f83fb-187">コール センター アプリでは、コール センターの担当者が、次の図で強調表示されている集荷店舗または場所、および日付とタイム スロットを選択できます。</span><span class="sxs-lookup"><span data-stu-id="f83fb-187">In the call center app, call center agents can select the pickup store or location, as well as a date and time slot as highlighted in the following illustration.</span></span>

![集荷時間帯が選択されているコールセンター注文の例](../dev-itpro/media/Curbside_timeslot_callcenter.png)

## <a name="additional-resources"></a><span data-ttu-id="f83fb-189">追加リソース</span><span class="sxs-lookup"><span data-stu-id="f83fb-189">Additional resources</span></span>

[<span data-ttu-id="f83fb-190">集荷情報モジュール</span><span class="sxs-lookup"><span data-stu-id="f83fb-190">Pickup information module</span></span>](../pickup-info-module.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]