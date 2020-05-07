---
title: 注文納期日
description: このトピックでは、オーダー納期処理について説明します。 注文納期を使用すると、顧客への出荷日を確実性をもって約束し、柔軟性を持たせた上でこれらの日付を守るようにすることができます。
author: ShylaThompson
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesATP, SalesAvailableDlvDates
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ccb7ef432553c0516eb49013eaad68dd21bf752c
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/17/2020
ms.locfileid: "3270030"
---
# <a name="order-promising"></a><span data-ttu-id="dc699-104">注文納期日</span><span class="sxs-lookup"><span data-stu-id="dc699-104">Order promising</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc699-105">このトピックでは、オーダー納期処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="dc699-105">This topic provides information about order promising.</span></span> <span data-ttu-id="dc699-106">注文納期を使用すると、顧客への出荷日を確実性をもって約束し、柔軟性を持たせた上でこれらの日付を守るようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="dc699-106">Order promising helps you reliably promise delivery dates to your customers and gives you flexibility so that you can meet those dates.</span></span>

<span data-ttu-id="dc699-107">注文納期は、最も早い出荷日および入荷日を計算し、配送日の管理方法、および配送日数に基づいています。</span><span class="sxs-lookup"><span data-stu-id="dc699-107">Order promising calculates the earliest ship and receipt dates, and is based on the delivery date control method and transport days.</span></span> <span data-ttu-id="dc699-108">4 つの配送日の管理方法から選択できます。</span><span class="sxs-lookup"><span data-stu-id="dc699-108">You can select among four delivery date control methods:</span></span>

-   <span data-ttu-id="dc699-109">**販売リード タイム** – 販売リード タイムは、販売注文の作成から品目の出荷までの時間です。</span><span class="sxs-lookup"><span data-stu-id="dc699-109">**Sales lead time** – Sales lead time is the time between creation of the sales order and shipment of the items.</span></span> <span data-ttu-id="dc699-110">配送日の計算は日数の既定値に基づき、有効在庫数、既知の要求、または供給計画は考慮されません。</span><span class="sxs-lookup"><span data-stu-id="dc699-110">The delivery date calculation is based on a default number of days, and does not consider stock availability, known demand, or planned supply.</span></span>
-   <span data-ttu-id="dc699-111">**ATP (納期回答可能在庫)** – ATP は、顧客に特定の日付で納期を回答できる使用可能な品目の数量です。</span><span class="sxs-lookup"><span data-stu-id="dc699-111">**ATP (available-to-promise)** – ATP is the quantity of an item that is available and can be promised to a customer on a specific date.</span></span> <span data-ttu-id="dc699-112">ATP の計算には、未コミット在庫、リード タイム、計画受入と払出が含まれます。</span><span class="sxs-lookup"><span data-stu-id="dc699-112">The ATP calculation includes uncommitted inventory, lead times, planned receipts, and issues.</span></span>
-   <span data-ttu-id="dc699-113">**ATP + 払出安全日数**– 出荷日は、ATP に品目の払出安全日数を加えた日付と同じになります。</span><span class="sxs-lookup"><span data-stu-id="dc699-113">**ATP + Issue margin** – The shipping date is equal to the ATP date plus the issue margin for the item.</span></span> <span data-ttu-id="dc699-114">払出安全日数は、品目を出荷する準備にかかる時間です。</span><span class="sxs-lookup"><span data-stu-id="dc699-114">The issue margin is the time that is required to prepare the items for shipment.</span></span>
-   <span data-ttu-id="dc699-115">**CTP (生産可能在庫)**– 在庫状態が展開して計算されます。</span><span class="sxs-lookup"><span data-stu-id="dc699-115">**CTP (capable-to-promise)** – Availability is calculated through explosion.</span></span>

## <a name="atp-calculations"></a><span data-ttu-id="dc699-116">ATP の計算</span><span class="sxs-lookup"><span data-stu-id="dc699-116">ATP calculations</span></span>
<span data-ttu-id="dc699-117">ATP 数量は。"先読みによる累計 ATP" 手法を使用して計算されます。</span><span class="sxs-lookup"><span data-stu-id="dc699-117">The ATP quantity is calculated by using the “cumulative ATP with look-ahead” method.</span></span> <span data-ttu-id="dc699-118">この ATP 計算手法の主な利点は、入庫間の出庫の合計が最新の入庫よりも大きい状況 (たとえば、要求を満たすために以前の入庫からの数量を使用する必要がある場合) を処理できることです。</span><span class="sxs-lookup"><span data-stu-id="dc699-118">The main advantage of this ATP calculation method is that it can handle cases where the sum of issues among receipts is more than the latest receipt (for example, when a quantity from an earlier receipt must be used to meet a requirement).</span></span> <span data-ttu-id="dc699-119">"先読みによる累計 ATP" 手法には、入庫する累計数量が出庫する累計数量を超えるまでのすべての出庫が含まれます。</span><span class="sxs-lookup"><span data-stu-id="dc699-119">The “cumulative ATP with look-ahead” calculation method includes all issues until the cumulative quantity to receive exceeds the cumulative quantity to issue.</span></span> <span data-ttu-id="dc699-120">したがって、この ATP 計算方式で、早い時期からの数量の一部をその後の期間に使用できるかどうかを評価します。</span><span class="sxs-lookup"><span data-stu-id="dc699-120">Therefore, this ATP calculation method evaluates whether some of the quantity from an earlier period can be used in a later period.</span></span>  

<span data-ttu-id="dc699-121">ATP 数量は、最初の期間の未コミット在庫残高です。</span><span class="sxs-lookup"><span data-stu-id="dc699-121">The ATP quantity is the uncommitted inventory balance in the first period.</span></span> <span data-ttu-id="dc699-122">通常、これは入庫がスケジュールされる期間中、計算されます。</span><span class="sxs-lookup"><span data-stu-id="dc699-122">Typically, it's calculated for each period in which a receipt is scheduled.</span></span> <span data-ttu-id="dc699-123">プログラムは、ATP 期間を日数で計算し、現在の日付を ATP 数量の初日として計算します。</span><span class="sxs-lookup"><span data-stu-id="dc699-123">The program calculates the ATP period in days and calculates the current date as the first date for the ATP quantity.</span></span> <span data-ttu-id="dc699-124">最初の期間では、手持在庫から期日または期日超過の顧客注文を引いた値が ATP に含まれます。</span><span class="sxs-lookup"><span data-stu-id="dc699-124">In the first period, ATP includes on-hand inventory minus customer orders that are due and overdue.</span></span>  

<span data-ttu-id="dc699-125">ATP は、次の式を使用して計算されます。</span><span class="sxs-lookup"><span data-stu-id="dc699-125">ATP is calculated by using the following formula:</span></span>  

<span data-ttu-id="dc699-126">ATP = 直前の期間の ATP + 現在の期間の入庫 - 現在の期間の出庫 - 将来のすべての期間 (対象の将来期間を含む) の入庫の合計が出庫の合計 (対象の将来期間を含む) よりも大きくなるまでの、各将来期間の正味出庫数量。</span><span class="sxs-lookup"><span data-stu-id="dc699-126">ATP = ATP for the previous period + Receipts for the current period – Issues for the current period – Net issue quantity for each future period until the period when the sum of receipts for all future periods, up to and including the future period, exceeds the sum of issues up to and including the future period.</span></span>  

<span data-ttu-id="dc699-127">ATP 計算では、有効期限に関する情報や、任意の数量を約束するときにシステムが期待する ATP タイム フェンスを超える情報が含まれていないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="dc699-127">Notice that the ATP calculation does not include information around expiry date and beyond the ATP time fence that the system expects when any quantity can be promised.</span></span>

<span data-ttu-id="dc699-128">考慮する出庫または入庫がこれだけである場合は、次の日付の ATP 数量が、最新の計算済み ATP 数量と同じになります。</span><span class="sxs-lookup"><span data-stu-id="dc699-128">When there are no more issues or receipts to consider, the ATP quantity for the following dates is the same as the latest calculated ATP quantity.</span></span>  

<span data-ttu-id="dc699-129">ATP チェックが完了したときに、品目に使用される分析コードが与えられていないものがある場合は、それらを出庫および入庫で指定できます。</span><span class="sxs-lookup"><span data-stu-id="dc699-129">If not all the dimensions that are used for an item are given when the ATP check is completed, they can still be specified on the issue and receipts.</span></span> <span data-ttu-id="dc699-130">この場合は、ATP 計算で、入庫および出庫を既存の分析コードに集計して、ATP 計算で使用される入庫および出庫の明細行を減らす必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc699-130">In this case, in the ATP calculation, the receipts and issues must be aggregated to the existing dimensions to reduce the number of receipt and issue lines that are used in the ATP calculation.</span></span>  

<span data-ttu-id="dc699-131">表示される ATP 数量は、常に 0 (ゼロ) 以上です。</span><span class="sxs-lookup"><span data-stu-id="dc699-131">The ATP quantity that is shown is always greater than or equal to 0 (zero).</span></span> <span data-ttu-id="dc699-132">計算で負の ATP 数量が返される場合 (たとえば、以前に回答されている納期の数量が使用可能な数量を超える場合)、プログラムは自動的に数量を 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="dc699-132">If the calculation returns a negative ATP quantity (for example, if the quantity that was previously promised exceeds the available quantity), the quantity is automatically set to 0.</span></span>

### <a name="example"></a><span data-ttu-id="dc699-133">例</span><span class="sxs-lookup"><span data-stu-id="dc699-133">Example</span></span>

<span data-ttu-id="dc699-134">**ATP 後方需要タイム フェンス**フィールドは、遅延需要注文または在庫払出をどの位時間を遡って検索するかを制御します。</span><span class="sxs-lookup"><span data-stu-id="dc699-134">The **ATP backward demand time fence** field controls how far back in time to look for delayed demand orders or inventory issues.</span></span> <span data-ttu-id="dc699-135">**ATP 後方供給タイム フェンス**フィールドは、遅延供給注文または在庫入庫をどの位時間を遡って検索するかを制御します。</span><span class="sxs-lookup"><span data-stu-id="dc699-135">The **ATP backward supply time fence** field controls how far back in time to look for delayed supply orders or inventory receipts.</span></span> <span data-ttu-id="dc699-136">たとえば、7 日だけ遅延した注文を ATP 計算で考慮する必要がある場合、フィールドを両方とも **7** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc699-136">For example, if orders that are delayed by only seven days should be considered in the ATP calculation, both fields should be set to **7**.</span></span>  

<span data-ttu-id="dc699-137">**ATP 遅延需要相殺時間**と **ATP 遅延供給相殺時間**のフィールドは、遅延需要または遅延供給を ATP 計算でいつ考慮するかを制御します。</span><span class="sxs-lookup"><span data-stu-id="dc699-137">The **ATP delayed demand offset time** and **ATP delayed supply offset time** fields control when the delayed demand or supply will be considered in the ATP calculation.</span></span> <span data-ttu-id="dc699-138">遅延供給と遅延需給を ATP 計算で明後日考慮する必要がある場合、フィールドを両方とも **2** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc699-138">For example, if the delayed supply and demand should be considered in the ATP calculation the day after tomorrow, both fields should be set to **2**.</span></span> <span data-ttu-id="dc699-139">**2** という値は、ATP 計算で考慮する必要のある遅延発注書の品目の数量は、現在の日付から 2 日後に入手可能と見られることを意味します。</span><span class="sxs-lookup"><span data-stu-id="dc699-139">A value of **2** means that the quantity of an item on a delayed purchase order that should be considered in the ATP calculation will be seen as available two days after the current date.</span></span>  

<span data-ttu-id="dc699-140">次の例では、**7** が **ATP 後方需要タイム フェンス**フィールドと **ATP 後方供給タイム フェンス**フィールドに入力され、**1** が **ATP 遅延需要相殺時間**フィールドと **ATP 遅延供給相殺時間**フィールドに入力されます。</span><span class="sxs-lookup"><span data-stu-id="dc699-140">For the following example, **7** is entered in the **ATP backward demand time fence** and **ATP backward supply time fence** fields, and **1** is entered in the **ATP delayed demand offset time** and **ATP delayed supply offset time** fields.</span></span>  

<span data-ttu-id="dc699-141">3 日前に入庫するはずであった製品 200 個の発注書がまだ入庫されていません。</span><span class="sxs-lookup"><span data-stu-id="dc699-141">A purchase order for 200 pieces of a product that should have been received three days ago hasn't been received yet.</span></span> <span data-ttu-id="dc699-142">そのため、昨日出荷されるはずであった同じ製品 75 個の販売注文明細行が出荷されていません。</span><span class="sxs-lookup"><span data-stu-id="dc699-142">Therefore, a sales order line for 75 pieces of the same product that should have been shipped yesterday hasn't been shipped.</span></span>  

<span data-ttu-id="dc699-143">顧客から電話があり、同じ製品 150 個の注文を希望しています。</span><span class="sxs-lookup"><span data-stu-id="dc699-143">A customer calls and wants to order 150 pieces of the same product.</span></span> <span data-ttu-id="dc699-144">製品の在庫状態を確認すると、10 日後に 100 個の製品の別の発注書が出荷されることが判明します。</span><span class="sxs-lookup"><span data-stu-id="dc699-144">When you verify the availability of the product, you find that another purchase order for 100 pieces of the product will be delivered 10 days later.</span></span>  

<span data-ttu-id="dc699-145">製品の販売注文明細行を作成し、数量として **150** を入力します。</span><span class="sxs-lookup"><span data-stu-id="dc699-145">You create a sales order line for the product and enter **150** as the quantity.</span></span>  

<span data-ttu-id="dc699-146">配送日の管理方式は ATP であるため、最も早い出荷日を検索するために、ATP データが計算されます。</span><span class="sxs-lookup"><span data-stu-id="dc699-146">Because the delivery date control is method is ATP, the ATP data is calculated to find the earliest possible ship date.</span></span> <span data-ttu-id="dc699-147">設定に基づいて、遅延発注書および販売注文が考慮され、その結果での現在の日付の ATP 数量は 0 です。</span><span class="sxs-lookup"><span data-stu-id="dc699-147">Based on the settings, the delayed purchase order and sales order are considered, and the resulting ATP quantity for the current date is 0.</span></span> <span data-ttu-id="dc699-148">明日、遅延発注書の入庫が予定されているとき、ATP 数量は 0 より大きいと計算されます (この場合は 125 と計算されます)。</span><span class="sxs-lookup"><span data-stu-id="dc699-148">Tomorrow, when the delayed purchase order is expected to be received, the ATP quantity is calculated as more than 0 (in this case, it's calculated as 125).</span></span> <span data-ttu-id="dc699-149">ただし、今より 10 日後、100 個の追加の発注書の入庫が予定されているとき、ATP 数量は 150 よりも大きくなります。</span><span class="sxs-lookup"><span data-stu-id="dc699-149">However, 10 days from now, when the additional purchase order for 100 pieces is expected to be received, the ATP quantity becomes more than 150.</span></span>  

<span data-ttu-id="dc699-150">したがって、出荷日は、ATP 計算に基づいて、今日より 10 日後に設定されます。</span><span class="sxs-lookup"><span data-stu-id="dc699-150">Therefore, the ship date is set to 10 days from now, based on the ATP calculation.</span></span> <span data-ttu-id="dc699-151">このため、要求された数量を今日より 10 日後に納入できることを顧客に伝えます。</span><span class="sxs-lookup"><span data-stu-id="dc699-151">Therefore, you tell the customer that the requested quantity can be delivered 10 days from now.</span></span>



