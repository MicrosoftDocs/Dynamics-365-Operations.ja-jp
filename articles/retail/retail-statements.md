---
title: "小売明細書"
description: "このトピックでは、明細書を作成および転記する方法について説明します。"
author: ashishmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core, Retail
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail Version
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: aeb851587cc40828088dfa22fda1d70f49561c3a
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---

# <a name="retail-statements"></a><span data-ttu-id="a29bc-103">小売明細書</span><span class="sxs-lookup"><span data-stu-id="a29bc-103">Retail statements</span></span>
<span data-ttu-id="a29bc-104">Microsoft Dynamics 365 for Retail では、クラウド販売時点管理 (POS) または Modern POS (MPOS) で発生するトランザクションに対して、明細書の転記プロセスが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-104">In Microsoft Dynamics 365 for Retail, the statement posting process is used to account for the transactions that occur in Cloud point of sale (POS) or Modern POS (MPOS).</span></span> <span data-ttu-id="a29bc-105">明細書の転記プロセスでは、配送スケジュールを使用して、一連の POS トランザクションを本社 (HQ) クライアントに引き渡します。</span><span class="sxs-lookup"><span data-stu-id="a29bc-105">The statement posting process uses the distribution schedule to pull a set of POS transactions into the headquarters (HQ) client.</span></span> <span data-ttu-id="a29bc-106">[**小売パラメーター**] および [**店舗**] ページで定義されているパラメーターは、個々のステートメントに引き込まれたトランザクションを選択するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-106">The parameters that are defined on the **Retail parameters** and **Stores** pages are used to select the transactions that are pulled into individual statements.</span></span>  

<span data-ttu-id="a29bc-107">次の図は、明細書の転記プロセスを示しています。</span><span class="sxs-lookup"><span data-stu-id="a29bc-107">The following illustration shows the statement posting process.</span></span> <span data-ttu-id="a29bc-108">このプロセスでは、POS に記録されているトランザクションは、小売り用スケジューラを使用してクライアントに送信されます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-108">In this process, transactions that are recorded in the POS are transmitted to the client by using the Retail scheduler.</span></span> <span data-ttu-id="a29bc-109">クライアントがトランザクションを受け入れた後、ストアのトランザクション明細書を作成し、計算および転記できます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-109">After the client receives the transactions, you can create, calculate, and post the transaction statement for the store.</span></span> 

<span data-ttu-id="a29bc-110">[![明細書転記プロセス](./media/retail-statements.png)](./media/retail-statements.png)</span><span class="sxs-lookup"><span data-stu-id="a29bc-110">[![Statement posting process](./media/retail-statements.png)](./media/retail-statements.png)</span></span>

## <a name="creating-and-posting-statements"></a><span data-ttu-id="a29bc-111">明細書を作成および転記する</span><span class="sxs-lookup"><span data-stu-id="a29bc-111">Creating and posting statements</span></span>
<span data-ttu-id="a29bc-112">明細書は、手動で作成するか、終日にわたって定期的に実行するように設定したバッチ処理を使用して作成できます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-112">You can create a statement manually or by using batch processes that you set up to run periodically throughout the day.</span></span> <span data-ttu-id="a29bc-113">どちらの場合も、次の手順が明細書の作成および転記に使用されます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-113">In both cases, the following steps are used to create and post statements.</span></span>

###  <a name="create-the-statement"></a><span data-ttu-id="a29bc-114">明細書を作成する</span><span class="sxs-lookup"><span data-stu-id="a29bc-114">Create the statement</span></span>
<span data-ttu-id="a29bc-115">この手順では、明細書を手動で作成する店舗を識別します。</span><span class="sxs-lookup"><span data-stu-id="a29bc-115">This step identifies the store that the statement is manually created for.</span></span> <span data-ttu-id="a29bc-116">バッチ処理をコンフィギュレーションすると、定義したスケジュールに基づいて自動的にすべての店舗の明細書を作成できます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-116">If you configure a batch process, you can automatically create statements for all stores, based on a schedule that you define.</span></span> 

### <a name="calculate-the-statement"></a><span data-ttu-id="a29bc-117">明細書を計算する</span><span class="sxs-lookup"><span data-stu-id="a29bc-117">Calculate the statement</span></span>
<span data-ttu-id="a29bc-118">このステップでは、[**小売パラメーター**] および [**店舗**] ページで各店舗に対して定義される基準を基に、トランザクション明細行が選択されます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-118">In this step, the transaction lines are selected based on criteria that are defined for each store on the **Retail parameters** and **Stores** pages.</span></span> <span data-ttu-id="a29bc-119">これらのページで、基準を定義し、トランザクションの計算方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="a29bc-119">On these pages, you define the criteria and specify how the transactions are calculated.</span></span> <span data-ttu-id="a29bc-120">明細書の計算前に、明細書に含まれるトランザクションのリストを表示するには、[**トランザクション**] ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="a29bc-120">To view a list of the transactions that are included in the statement before you calculate the statement, use the **Transactions** page.</span></span> 

<span data-ttu-id="a29bc-121">明細書の計算では、計算済金額としてレジスターからの支払/入金申告を使用します。</span><span class="sxs-lookup"><span data-stu-id="a29bc-121">Statement calculation uses tender declarations from the registers as the counted amount.</span></span> <span data-ttu-id="a29bc-122">計算済金額は手動で入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-122">Alternatively, you can enter the counted amount manually.</span></span> <span data-ttu-id="a29bc-123">明細書には、すべての支払方法のトランザクション売上量と実際の計算量の差額が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-123">The statement shows the difference between the sales amount for the transactions and the actual counted amount in all payment methods.</span></span> <span data-ttu-id="a29bc-124">明細書は、この差額が店舗で定義された最大転記差の範囲内に収まる場合にのみ転記されます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-124">The statement is posted only if this difference is less than the maximum posting difference that is defined for the store.</span></span> 

> [!NOTE]
> <span data-ttu-id="a29bc-125">明細書の計算プロセスでは、グローバル番号順序を使用します。</span><span class="sxs-lookup"><span data-stu-id="a29bc-125">The statement calculation process uses the global number sequence.</span></span>

<span data-ttu-id="a29bc-126">明細書の計算時、計算には次のタスクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-126">When you calculate a statement, the calculation includes the following tasks:</span></span>

- <span data-ttu-id="a29bc-127">選択した日付範囲で、前の明細書の計算に含まれなかったトランザクションをマークします。</span><span class="sxs-lookup"><span data-stu-id="a29bc-127">For the selected date range, mark transactions that weren't included in a previous statement calculation.</span></span> 
- <span data-ttu-id="a29bc-128">選択したトランザクションの支払/入金の合計金額を計算します。</span><span class="sxs-lookup"><span data-stu-id="a29bc-128">Calculate the total amounts that were tendered in the selected transactions.</span></span> <span data-ttu-id="a29bc-129">以下の明細書の方法に基づき、結果が明細行に表示されます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-129">The results are shown on the statement lines, depending on the statement method:</span></span>

  - <span data-ttu-id="a29bc-130">明細書の方法が [**合計**] である場合は、選択したトランザクションの各支払方法に対して明細行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-130">If the statement method is **Total**, a line is created for each payment method in the selected transactions.</span></span> 
  - <span data-ttu-id="a29bc-131">明細書の方法が [**スタッフ**] である場合は、選択したスタッフ メンバーによって実行されたトランザクションの各支払方法に対して明細行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-131">If the statement method is **Staff**, a line is created for each payment method in transactions that were performed by the selected staff member.</span></span> 
  - <span data-ttu-id="a29bc-132">明細書の方法が [**POS 端末**] である場合は、選択したレジスターで実行されたトランザクションの各支払方法に対して明細行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-132">If the statement method is **POS terminal**, a line is created for each payment method in transactions that were performed on the selected register.</span></span> 
  - <span data-ttu-id="a29bc-133">明細書の方法が [**シフト**] である場合は、シフト中に実行されたトランザクションの各支払方法に対して明細行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-133">If the statement method is **Shift**, a line is created for each payment method in transactions that were performed during a shift.</span></span>

<span data-ttu-id="a29bc-134">[**明細書の方法別分割**] チェック ボックスが [**店舗**] ページで選択済みの場合、[**明細書の方法**] フィールドで選択した値に基づき個別の明細書が作成されます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-134">If the **Split by Statement method** check box is selected on the **Stores** page, a separate statement is created based on the value that is selected in the **Statement method** field.</span></span>

<span data-ttu-id="a29bc-135">店舗の操業時間が深夜を超える場合、カレンダー日付の終わりではなく、業務日付の終わりに基づいて明細書を転記するように設定できます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-135">If your store's operating hours extend past midnight, you can configure statement posting so that it's based on the end of the business day instead of the end of the calendar day.</span></span> 

<span data-ttu-id="a29bc-136">[**店舗**] ページの、[**明細書/決済**] クイックタブの、[**営業日の終了**] フィールドで、最後のトランザクションが記録されて業務日付の明細書に含められる時間を入力します。</span><span class="sxs-lookup"><span data-stu-id="a29bc-136">On the **Stores** page, on the **Statement/closing** FastTab, in the **End of business day** field, enter the time that the last transaction must be recorded to be included in the business day’s statement.</span></span> <span data-ttu-id="a29bc-137">同じ業務日付内にトランザクションを転記するには、[**営業日として転記する**] チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="a29bc-137">Select the **Post as business day** check box to post the transactions within the same business day.</span></span> <span data-ttu-id="a29bc-138">明細書が転記されるとき、同じ業務日付内に記録されるトランザクションは、深夜の前および深夜の後に発生した他のトランザクションのいずれであっても、同じ販売注文に含めることができます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-138">When the statement is posted, transactions that are recorded within the same business day can be included on the same sales order, even if some transactions occur before midnight and other transactions occur after midnight.</span></span> 

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a><span data-ttu-id="a29bc-139">例: カレンダー日付 2 日に及ぶ業務日付の明細書を転記する</span><span class="sxs-lookup"><span data-stu-id="a29bc-139">Example: Post a statement for a business day that extends over two calendar days</span></span> 

<span data-ttu-id="a29bc-140">店舗は午前 8 時から午前 3 時まで営業しており、店舗のコンフィギュレーションでは [**営業日として転記する**] チェック ボックスが選択されています。</span><span class="sxs-lookup"><span data-stu-id="a29bc-140">A store is open between 8:00 AM and 3:00 AM, and the **Post as business day** check box is selected in the store's configuration.</span></span> <span data-ttu-id="a29bc-141">5 月 31 日に、店舗は午前 8 時から真夜中までの取引を記録します。</span><span class="sxs-lookup"><span data-stu-id="a29bc-141">On May 31, the store records transactions between 8:00 AM and midnight.</span></span> <span data-ttu-id="a29bc-142">店舗では 6 月 1 日の午前 12 時 1 分から午前 3 時までのトランザクションも記録されます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-142">The store also records transactions between 12:01 AM and 3:00 AM on June 1.</span></span> 

<span data-ttu-id="a29bc-143">店舗が業務日付の終了の明細書を転記するとき、販売注文が生成されます。トランザクションは 5 月 31 日と 6 月 1 日の 2 日間に発生しましたが、その販売注文には午前 8 時から午前 3 時までの業務時間に記録されたすべてのトランザクションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-143">When the store posts its statement for the close of the business day, the sales order that is generated includes all transactions that were recorded between the business hours of 8:00 AM and 3:00 AM, even though the transactions occurred on two days, May 31 and June 1.</span></span> 

<span data-ttu-id="a29bc-144">同じ店舗が [**営業日として転記する**] チェック ボックスの選択をオフにして構成される場合、店舗の業務日付の終了で明細書を転記するとき、別個の販売注文が生成されます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-144">If the **Post as business day** check box is cleared for the same store, separate sales orders are generated when the store posts its statement for the close of the business day.</span></span> <span data-ttu-id="a29bc-145">1 つ目の販売注文には、5 月 31 日の業務時間午前 8 時から深夜までに記録されたトランザクションが含まれ、2 番目の販売注文には、6 月 1 日の午前 12 時 1 分から午前 3 時までの業務時間に記録されたトランザクションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-145">One sales order includes the transactions that were recorded between the business hours of 8:00 AM and midnight on May 31, and the second sales order includes the transactions that were recorded between the business hours of 12:01 AM and 3:00 AM on June 1.</span></span>
 
> [!NOTE]
> <span data-ttu-id="a29bc-146">明細書を作成する前に、明細書の期間のシフトをクローズする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a29bc-146">Before you can create statements, you should close the shifts in the statement period.</span></span> 

### <a name="post-the-statement"></a><span data-ttu-id="a29bc-147">明細書を転記する</span><span class="sxs-lookup"><span data-stu-id="a29bc-147">Post the statement</span></span>
<span data-ttu-id="a29bc-148">明細書を転記すると、小売り販売用の販売注文および請求書が明細書内に作成されます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-148">When you post a statement, sales orders and invoices are created for the retail sales in the statement.</span></span>

- <span data-ttu-id="a29bc-149">現金払いの販売は、店舗に割り当てられている既定の顧客の 1 つの販売注文に集計されて請求されます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-149">Cash and carry sales are aggregated onto one sales order, and are invoiced for the default customer who is assigned to the store.</span></span> 
- <span data-ttu-id="a29bc-150">Microsoft Dynamics 365 for Retail POS のトランザクションに顧客が追加された小売販売により、個別の販売注文と請求書が固有の顧客ごとに 1 つずつ生成されます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-150">Retail sales for which a customer was added to the transaction in Microsoft Dynamics 365 for Retail POS generate separate sales orders and invoices, one for each unique customer.</span></span> 

<span data-ttu-id="a29bc-151">支払仕訳帳は明細書の支払に対して自動的に作成され、在庫は POS 店舗に更新されます。</span><span class="sxs-lookup"><span data-stu-id="a29bc-151">Payment journals are automatically created for the payments in the statement, and the inventory is updated for the POS store.</span></span>

