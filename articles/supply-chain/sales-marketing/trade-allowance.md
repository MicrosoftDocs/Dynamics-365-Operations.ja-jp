---
title: "取引割引管理"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations の取引割引管理ついて説明します。"
author: t-benebo
manager: AnnBe
ms.date: 08/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: t-benebo
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 735e9c95d30860b3a28951cedbccf3ed009321ff
ms.openlocfilehash: 2f40262573eaeee24889e5234561f89e7620c4f7
ms.contentlocale: ja-jp
ms.lasthandoff: 08/17/2018

---

# <a name="trade-allowance-management"></a><span data-ttu-id="add7b-103">取引割引管理</span><span class="sxs-lookup"><span data-stu-id="add7b-103">Trade allowance management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="add7b-104">取引割引管理により、会社が量および行動目標を達成する顧客に対して小売の「能力給」金銭的報奨を提供する販売プロモーション プログラムを管理するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="add7b-104">Trade allowance management helps companies manage sales promotion programs that offer retail "pay-for-performance" monetary rewards to customers that achieve volume and behavioral goals.</span></span>

<span data-ttu-id="add7b-105">このトピックでは、販売プロモーション プログラムの管理に関連する一般的なタスクの概要を示します。</span><span class="sxs-lookup"><span data-stu-id="add7b-105">This topic provides an overview for the most common tasks that are involved in managing a sales promotion program.</span></span> <span data-ttu-id="add7b-106">概要では、次の作業について説明します。</span><span class="sxs-lookup"><span data-stu-id="add7b-106">The overview covers the following tasks:</span></span>

- <span data-ttu-id="add7b-107">プロモーション資金および取引割引契約書を確認します。</span><span class="sxs-lookup"><span data-stu-id="add7b-107">Review the promotional fund and a trade allowance agreement.</span></span>
- <span data-ttu-id="add7b-108">計画された販売促進イベントの下で売り込みを実行し、払戻計算請求を生成します。</span><span class="sxs-lookup"><span data-stu-id="add7b-108">Perform sales under the planned merchandising event, and generate bill-back claims.</span></span>
- <span data-ttu-id="add7b-109">請求を処理し、売掛金 (A/R) に控除として渡します。</span><span class="sxs-lookup"><span data-stu-id="add7b-109">Process claims, and pass them as deductions to Accounts receivable (A/R).</span></span>
- <span data-ttu-id="add7b-110">期日控除の決済および控除ワークベンチでの顧客の短期支払を行います。</span><span class="sxs-lookup"><span data-stu-id="add7b-110">Settle deductions that are due and customer short-pays on the Deduction workbench.</span></span>
- <span data-ttu-id="add7b-111">プロモーションと資金消費の有効性を分析します。</span><span class="sxs-lookup"><span data-stu-id="add7b-111">Analyze the effectiveness of the promotion and fund consumption.</span></span>

## <a name="audience-and-purpose"></a><span data-ttu-id="add7b-112">対象者および目的</span><span class="sxs-lookup"><span data-stu-id="add7b-112">Audience and purpose</span></span>

<span data-ttu-id="add7b-113">このドキュメントの情報は、エンタープライズの会社での業務の意思決定者、購買マネージャーなどの職位、最高財務責任者 (CFO)、および会計マネージャーなどの、次の職責を対象としています。</span><span class="sxs-lookup"><span data-stu-id="add7b-113">The information in this document is intended for business decision makers in enterprise companies, in positions such as purchase manager, chief financial officer (CFO), and accounting manager, who have the following responsibilities:</span></span>

- <span data-ttu-id="add7b-114">高レベル予算と資金配賦</span><span class="sxs-lookup"><span data-stu-id="add7b-114">High-level budgets and fund allocation</span></span>
- <span data-ttu-id="add7b-115">販売プロモーションの計画および分析</span><span class="sxs-lookup"><span data-stu-id="add7b-115">Planning and analyzing sales promotions</span></span>
- <span data-ttu-id="add7b-116">払戻計算の処理、販売促進イベントに基づいて支払の実行、および短期支払や控除を決済するスタッフの管理</span><span class="sxs-lookup"><span data-stu-id="add7b-116">Managing staff that processes bill-back claims, runs payments based on merchandizing events, and settles short-pays and deductions</span></span>

<span data-ttu-id="add7b-117">これらのロールのユーザーは、以下の目標を達成する方法を求めています:</span><span class="sxs-lookup"><span data-stu-id="add7b-117">People in these roles are looking for ways to achieve these goals:</span></span>

- <span data-ttu-id="add7b-118">マーケティング プロモーション資金を有効に利用します。</span><span class="sxs-lookup"><span data-stu-id="add7b-118">Better use marketing promotional funds.</span></span>
- <span data-ttu-id="add7b-119">さまざまなタイプのプロモーションプログラムおよび割引に柔軟に対応します。</span><span class="sxs-lookup"><span data-stu-id="add7b-119">Flexibly accommodate different types of promotion programs and allowances.</span></span>
- <span data-ttu-id="add7b-120">管理の負担、およびプロモーションのパフォーマンスの監視と請求の処理に関連付けられるエラーを減らします。</span><span class="sxs-lookup"><span data-stu-id="add7b-120">Reduce the administrative burden and errors that are associated with monitoring promotion performance and processing claims.</span></span>
- <span data-ttu-id="add7b-121">将来の負債の見越計上によりキャッシュフロー予測の精度を高めます。</span><span class="sxs-lookup"><span data-stu-id="add7b-121">Improve cash flow forecasts by accruing for future liability.</span></span>
- <span data-ttu-id="add7b-122">プロモーションについて、顧客との進行中および将来の交渉に関する定量化された基準があります。</span><span class="sxs-lookup"><span data-stu-id="add7b-122">Have a quantified basis for ongoing and future negotiations with customers about promotions.</span></span>

## <a name="review-details-of-a-promotional-fund-and-trade-allowance-agreement"></a><span data-ttu-id="add7b-123">プロモーション資金および取引割引契約書の詳細を確認する</span><span class="sxs-lookup"><span data-stu-id="add7b-123">Review details of a promotional fund and trade allowance agreement</span></span>

<span data-ttu-id="add7b-124">取引割引契約は、特定の量ターゲットや行動目標を達成する顧客に能力給の金銭的報奨を提供するインセンティブ プログラムです。</span><span class="sxs-lookup"><span data-stu-id="add7b-124">A trade allowance agreement is an incentive program where pay-for-performance monetary rewards are offered to customers that achieve specific volume targets and/or behavioral goals.</span></span> <span data-ttu-id="add7b-125">プロモーション資金は予算経費です。</span><span class="sxs-lookup"><span data-stu-id="add7b-125">Promotional funds are budgeted expenditures.</span></span> <span data-ttu-id="add7b-126">この方法により、プロモーション キャンペーンをキャプチャできます。</span><span class="sxs-lookup"><span data-stu-id="add7b-126">In that way, the promotional campaigns can be captured.</span></span>

### <a name="promotional-fund"></a><span data-ttu-id="add7b-127">プロモーション資金</span><span class="sxs-lookup"><span data-stu-id="add7b-127">Promotional fund</span></span>

<span data-ttu-id="add7b-128">取引割引契約に割り当てられる資金は、**資金**ページに記録されます。</span><span class="sxs-lookup"><span data-stu-id="add7b-128">Funds that are allocated to trade allowance agreements are recorded on the **Funds** page.</span></span> <span data-ttu-id="add7b-129">**資金**ページを開くには、**販売およびマーケティング** \> **取引割引** \> **資金** \> **資金**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="add7b-129">To open the **Funds** page, select **Sales and marketing** \> **Trade allowances** \> **Funds** \> **Funds**.</span></span>

<span data-ttu-id="add7b-130">![資金ページ](./media/trade-allowance-management-funds-page.png "資金ページ")</span><span class="sxs-lookup"><span data-stu-id="add7b-130">![Funds page](./media/trade-allowance-management-funds-page.png "Funds page")</span></span>

<span data-ttu-id="add7b-131">**資金**ページで、プロモーション資金の詳細を表示できます。</span><span class="sxs-lookup"><span data-stu-id="add7b-131">On the **Funds** page, you can view the details of promotional funds.</span></span>

<span data-ttu-id="add7b-132">**一般**クイック タブでは、資金が有効である期間と予算金額を表示します。</span><span class="sxs-lookup"><span data-stu-id="add7b-132">The **General** FastTab shows the period that the fund is valid for and its budgeted amount.</span></span> <span data-ttu-id="add7b-133">**ステータス**フィールドで、**承認済**の値は、プロモーション契約に割り当てられる資金を示しています。</span><span class="sxs-lookup"><span data-stu-id="add7b-133">In the **Status** field, a value of **Approved** indicates that the fund is ready to be allocated to promotion agreements.</span></span>

<span data-ttu-id="add7b-134">**顧客**クイック タブでは顧客階層が表示されます。</span><span class="sxs-lookup"><span data-stu-id="add7b-134">The **Customers** FastTab shows the customer hierarchy.</span></span> <span data-ttu-id="add7b-135">資金がターゲットとする顧客を選択するには、**資金顧客**の下になるようドラッグします。</span><span class="sxs-lookup"><span data-stu-id="add7b-135">To select the customers that the fund targets, drag them so that they are under **Fund customers**.</span></span> <span data-ttu-id="add7b-136">このクイック タブでは、資金の合計金額が配分される方法も示されます。</span><span class="sxs-lookup"><span data-stu-id="add7b-136">This FastTab also shows how the total amount of the fund is distributed.</span></span>

<span data-ttu-id="add7b-137">**品目**クイック タブではプロモーションに含まれる品目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="add7b-137">The **Items** FastTab shows the items that are included in the promotion.</span></span>

### <a name="trade-allowance-agreement"></a><span data-ttu-id="add7b-138">取引割引契約</span><span class="sxs-lookup"><span data-stu-id="add7b-138">Trade allowance agreement</span></span>

<span data-ttu-id="add7b-139">ファンドの定義が完了した後、プロモーション計画の次のステップはプロモーション契約 (貿易手当契約と呼ばれる) を登録し、資金を割り当て、各販売促進イベントに対するパフォーマンス目標を定義することです。</span><span class="sxs-lookup"><span data-stu-id="add7b-139">After the fund definition is in place, the next step in promotion planning is to register promotion contracts (which are known as trade allowance agreements), allocate funds, and define performance goals for each merchandizing event.</span></span>

<span data-ttu-id="add7b-140">取引割引契約は**取引割引契約**ページに記録されます。</span><span class="sxs-lookup"><span data-stu-id="add7b-140">Trade allowance agreements are recorded on the **Trade allowance agreements** page.</span></span> <span data-ttu-id="add7b-141">**取引割引契約**ページを開き、**販売およびマーケティング** \> **取引割引** \> **取引割引契約**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="add7b-141">To open the **Trade allowance agreements** page, select **Sales and marketing** \> **Trade allowances** \> **Trade allowance agreements**.</span></span>

<span data-ttu-id="add7b-142">![取引割引契約ページ](./media/trade-allowance-management-agreements-page.png "取引割引契約ページ")</span><span class="sxs-lookup"><span data-stu-id="add7b-142">![Trade allowance agreements page](./media/trade-allowance-management-agreements-page.png "Trade allowance agreements page")</span></span>

#### <a name="header"></a><span data-ttu-id="add7b-143">表題</span><span class="sxs-lookup"><span data-stu-id="add7b-143">Header</span></span>

<span data-ttu-id="add7b-144">**ヘッダー**を選択してヘッダー ビューに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="add7b-144">Select **Header** to switch to the Header view.</span></span>

<span data-ttu-id="add7b-145">**一般**クイック タブで、契約が有効な期間が**注文終了日**および**注文開始日**フィールドで定義されます。</span><span class="sxs-lookup"><span data-stu-id="add7b-145">On the **General** FastTab, the **Order to** and **Order from** fields define the period when the agreement is valid.</span></span> <span data-ttu-id="add7b-146">契約に対する**社内承認済**の承認ステータスは、契約がまだ有効ではなく、販売注文処理中に適用できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="add7b-146">An approval status of **Internal approved** for the agreement indicates that the agreement isn't yet valid and can't be applied during sales order processing.</span></span>

<span data-ttu-id="add7b-147">**一般**クイック タブの**分析**セクションには、プロモーション評価に対して使用される数量および原価を定義する重要なフィールドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="add7b-147">The **Analysis** section of the **General** FastTab contains important fields that define the quantities and costs that are used for promotion evaluation:</span></span>

- <span data-ttu-id="add7b-148">**基本単位**フィールドでは、プロモーションが適用される前に、選択した顧客に販売される必要がある製品の数量が指定されます。</span><span class="sxs-lookup"><span data-stu-id="add7b-148">The **Base units** field specifies the quantity of products that must be sold to the selected customers before the promotion is applied.</span></span>
- <span data-ttu-id="add7b-149">**計算済出荷数量**値は**リフト率**の値に基づいて計算され、このプロモーションの目標達成昇給となります。</span><span class="sxs-lookup"><span data-stu-id="add7b-149">The **Calculated ship quantity** value is calculated based on the **Lift percent** value, which is a planned target increase for this promotion.</span></span>
- <span data-ttu-id="add7b-150">取引割引契約でのさまざまなイベントの数量に基づいて、**取引割引コスト**フィールドが計算されます。</span><span class="sxs-lookup"><span data-stu-id="add7b-150">The **Trade allowance cost** field is calculated based on the quantities of the various events in the trade allowance agreement.</span></span>

<span data-ttu-id="add7b-151">左側のリストの**顧客**クイック タブで、顧客グループを選択および表示でき、事前定義された階層として設定されます。</span><span class="sxs-lookup"><span data-stu-id="add7b-151">On the **Customers** FastTab, in the list on the left, you can select and view customer groups, which are set up as predefined hierarchies.</span></span> <span data-ttu-id="add7b-152">割引契約のターゲットとして、階層全体または特定の勘定を選択できます。</span><span class="sxs-lookup"><span data-stu-id="add7b-152">You can then select the whole hierarchy or specific accounts as targets for the allowance agreement.</span></span>

<span data-ttu-id="add7b-153">**資金**ページの**品目**クイック タブと同じように、**品目**クイック タブで、その販売を合意した割引に関連付けるための契約に製品が追加されます。</span><span class="sxs-lookup"><span data-stu-id="add7b-153">On the **Items** FastTab, as on the **Items** FastTab of the **Funds** page, products are added to the agreement to associate its sales with the allowance that was agreed on.</span></span>

<span data-ttu-id="add7b-154">**資金**クイック タブで、この契約に関連付けられているプロモーション資金を表示できます。</span><span class="sxs-lookup"><span data-stu-id="add7b-154">On the **Funds** FastTab, you can view the promotion funds that are associated with this contract.</span></span> <span data-ttu-id="add7b-155">また、契約のイベント原価配賦を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="add7b-155">You can also view the contract's event cost allocation.</span></span> <span data-ttu-id="add7b-156">100% のイベント原価配賦とは、このプロモーションが 1 つの資金からのみ資金調達することを意味します。</span><span class="sxs-lookup"><span data-stu-id="add7b-156">An event cost allocation of 100 percent means that this promotion will be financed exclusively from one fund.</span></span> <span data-ttu-id="add7b-157">または、プロモーション契約はいくつかの資金を活用し、同等または異なる配賦割合を使用できます。</span><span class="sxs-lookup"><span data-stu-id="add7b-157">Alternatively, a promotion agreement can draw on several funds, and can use equal or differential percentage allocation.</span></span>

#### <a name="lines"></a><span data-ttu-id="add7b-158">ライン</span><span class="sxs-lookup"><span data-stu-id="add7b-158">Lines</span></span>

<span data-ttu-id="add7b-159">次に、**明細行**を選択して明細行ビューに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="add7b-159">Next, select **Lines** to switch to the Lines view.</span></span>

<span data-ttu-id="add7b-160">**販売促進イベント**タブで、この契約の対象となるイベントのタイプが表示されます。</span><span class="sxs-lookup"><span data-stu-id="add7b-160">The **Merchandizing events** tab shows the types of events that this agreement covers.</span></span> <span data-ttu-id="add7b-161">例には、払戻計算イベントおよび一括比例配分イベントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="add7b-161">Examples include bill-back events and lump sum events.</span></span>

<span data-ttu-id="add7b-162">販売促進イベントを選択し**金額**タブを選択すると、イベントの詳細が検出されます。</span><span class="sxs-lookup"><span data-stu-id="add7b-162">When you select the merchandizing event and then select the **Amounts** tab, the details for the event are found.</span></span>

<span data-ttu-id="add7b-163">![取引割引契約明細行](./media/trade-allowance-management-agreements-lines.png "取引割引契約明細行")</span><span class="sxs-lookup"><span data-stu-id="add7b-163">![Trade allowance agreement lines](./media/trade-allowance-management-agreements-lines.png "Trade allowance agreement lines")</span></span>

<span data-ttu-id="add7b-164">**取引割引明細行**セクションで、報奨を取得するための定義に対して顧客が達成する必要がある数量または金額の範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="add7b-164">In the **Trade allowance lines** section, you specify the quantity or amount ranges that the customer must achieve for definitions to obtain the rewards.</span></span>

<span data-ttu-id="add7b-165">**一括比例配分**の販売促進イベントの場合、**金額**タブでは、顧客が特定のパフォーマンスを達成する場合に、控除のフォームで顧客に支払われる数量が表示されます。</span><span class="sxs-lookup"><span data-stu-id="add7b-165">In the case of a merchandizing event of the **Lump sum** type, the **Amounts** tab shows the quantity that will be paid to the customer in the form of a deduction when the customer achieves specific performance.</span></span> <span data-ttu-id="add7b-166">**未処理**の承認ステータスは、一括比例配分まだ支払われていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="add7b-166">An approval status of **Open** indicates that the lump sum hasn't yet been paid.</span></span>

<span data-ttu-id="add7b-167">最後に、契約条件を満たす販売注文に契約を適用するには、契約のステータスを**確認済**に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="add7b-167">Finally, to apply the agreement to sales orders that meet the agreement's conditions, you must set the agreement's status to **Confirmed**.</span></span> <span data-ttu-id="add7b-168">**取引割引** ページのアクション ウィンドウで **確認済** を選択します。</span><span class="sxs-lookup"><span data-stu-id="add7b-168">On the **Trade allowance** page, on the Action Pane, select **Confirmed**.</span></span>

## <a name="perform-sales-under-the-planned-merchandising-event-and-generate-bill-back-claims"></a><span data-ttu-id="add7b-169">計画された販売促進イベントの下での売り込みの実行および払戻計算請求の生成</span><span class="sxs-lookup"><span data-stu-id="add7b-169">Perform sales under the planned merchandising event and generate bill-back claims</span></span>

<span data-ttu-id="add7b-170">契約の条件を満たす明細行を持つ販売注文を作成する場合、**販売注文**ページで**販売注文明細行** \> **表示** \> **価格の詳細**の順に選択して関連する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="add7b-170">When you create a sales order that has lines that fulfill the requirements of the agreement, you can view the related information on the **Sales order** page by selecting **Sales order line** \> **View** \> **Price details**.</span></span>

<span data-ttu-id="add7b-171">**価格の詳細**ページの**リベート**クイック タブで、販売員は、有効な取引割引契約 (リベート プログラム ID が表示される) からの払戻計算および明細行に適用される合計金額を参照できます。</span><span class="sxs-lookup"><span data-stu-id="add7b-171">On the **Price details** page, on the **Rebates** FastTab, the sales clerk can see a bill-back from the valid trade allowance agreement (the rebate program ID is shown) and the total amount that is applied to the line.</span></span> <span data-ttu-id="add7b-172">この金額は、払戻計算契約の条件に従って、明細行の数量に適用される製品単位ごとの払戻計算金額を掛けて計算されます。</span><span class="sxs-lookup"><span data-stu-id="add7b-172">This amount is calculated by multiplying the line quantity by the bill-back amount per product unit that applies, according to the conditions of the bill-back agreement.</span></span> <span data-ttu-id="add7b-173">この金額は、**価格の詳細**ページの**利益見積**のセクションにある**リベート金額**フィールドでも表示されます。</span><span class="sxs-lookup"><span data-stu-id="add7b-173">This amount is also shown in the **Rebate amount** field in the **Margin estimation** section of the **Price details** page.</span></span>

<span data-ttu-id="add7b-174">**販売注文**ページから販売注文の請求書を生成できます。</span><span class="sxs-lookup"><span data-stu-id="add7b-174">You can generate the invoice for the sales order from the **Sales order** page.</span></span> <span data-ttu-id="add7b-175">アクション ウィンドウの、**請求書**タブで、**生成**グループから**請求書**を選択します。</span><span class="sxs-lookup"><span data-stu-id="add7b-175">On the Action Pane, on the **Invoice** tab, in the **Generate** group, select **Invoice**.</span></span> <span data-ttu-id="add7b-176">次に、**請求の転記** ページで **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="add7b-176">Then, on the **Posting invoice** page, select **OK**.</span></span> <span data-ttu-id="add7b-177">売上請求書が転記されると、各請求明細行に対応する払戻計算請求が生成されます。</span><span class="sxs-lookup"><span data-stu-id="add7b-177">When the sales invoice is posted, a corresponding bill-back claim is generated for each invoice line.</span></span>

<span data-ttu-id="add7b-178">**販売とマーケティング** \> **取引割引** \> **払戻計算ワークベンチ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="add7b-178">Select **Sales and marketing** \> **Trade allowances** \> **Bill back workbench**.</span></span> <span data-ttu-id="add7b-179">**払戻計算ワークベンチ** ページでは、販売注文に対して作成された請求のステータスが **計算対象** であることに注目してください。</span><span class="sxs-lookup"><span data-stu-id="add7b-179">On the **Bill back workbench** page, notice that the claims that were created for the sales order have a status of **To be calculated**.</span></span>

> [!NOTE]
> <span data-ttu-id="add7b-180">**調達パラメーター**ページの**価格**タブで、**価格の詳細の有効化**オプションが**はい**に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="add7b-180">On the **Procurement and sourcing parameters** page, on the **Prices** tab, verify that the **Enable price details** option is set to **Yes**.</span></span> <span data-ttu-id="add7b-181">オプションが**いいえ**に設定されている場合、リベートを表示することはできません。</span><span class="sxs-lookup"><span data-stu-id="add7b-181">If the option is set to **No**, you won't be able to view the rebates.</span></span>

## <a name="process-claims-and-pass-them-as-deductions-to-ar"></a><span data-ttu-id="add7b-182">請求を処理し A/R に控除として渡します</span><span class="sxs-lookup"><span data-stu-id="add7b-182">Process claims and pass them as deductions to A/R</span></span>

<span data-ttu-id="add7b-183">払戻計算を処理するプロセスでの次の手順は、確認、計算、請求の承認、および控除への変換です。</span><span class="sxs-lookup"><span data-stu-id="add7b-183">The next steps in the process for handling bill-backs are to review, calculate, and approve claims, and then convert them into deductions.</span></span>

<span data-ttu-id="add7b-184">払戻計算ワークベンチでは、プロモーション契約の所有者が生成される請求を定期的にレビューおよび処理します。</span><span class="sxs-lookup"><span data-stu-id="add7b-184">The Bill back workbench is where the promotion agreement owner periodically reviews and processes the claims that are generated.</span></span> <span data-ttu-id="add7b-185">また、請求の支払方法に応じて A/R 管理者が承認済請求を控除または定期的な支払に変換します。</span><span class="sxs-lookup"><span data-stu-id="add7b-185">It's also where the A/R administrator converts the approved claims into deductions or regular payments, depending on the payment method for the claim.</span></span>

<span data-ttu-id="add7b-186">**払戻計算ワークベンチ**ページで、請求明細行を確認できます。</span><span class="sxs-lookup"><span data-stu-id="add7b-186">On the **Bill back workbench** page, you can review the claim lines.</span></span> <span data-ttu-id="add7b-187">数量を持つ別の明細行がある場合、および払戻計算が数量の範囲に依存している場合は、すべての累積効果に対して請求を再計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="add7b-187">If there are different lines that have quantities, and if the bill-back depends on ranges of quantities, the claims must be recalculated for any cumulative effect.</span></span>

### <a name="recalculate-claims"></a><span data-ttu-id="add7b-188">請求の再計算</span><span class="sxs-lookup"><span data-stu-id="add7b-188">Recalculate claims</span></span>

<span data-ttu-id="add7b-189">請求を再計算するには、アクション ウィンドウで、**累計**を選択します。</span><span class="sxs-lookup"><span data-stu-id="add7b-189">To recalculate the claims, on the Action Pane, select **Cumulate**.</span></span> <span data-ttu-id="add7b-190">次に、**リベートの累計**ダイアログ ボックスで顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="add7b-190">Then, in the **Cumulate rebates** dialog box, select the customer.</span></span>

<span data-ttu-id="add7b-191">再計算の結果として、プログラムでは、元の請求から各単位の特定の金額へと調整するその金額に対して、新しい請求を生成します。</span><span class="sxs-lookup"><span data-stu-id="add7b-191">As a result of the recalculation, the program generates new claims for the amounts to adjust the original claims to the qualifying amount per unit.</span></span> <span data-ttu-id="add7b-192">顧客、品目、通貨、測定単位、在庫分析コード、財務分析コード、および売上税グループの固有の組み合わせごとに 1 つの調整請求が生成されます。</span><span class="sxs-lookup"><span data-stu-id="add7b-192">One adjustment claim is generated for each unique combination of a customer, an item, a currency, a unit of measure, inventory dimensions, financial dimensions, and a sales tax group.</span></span> <span data-ttu-id="add7b-193">これらの調整請求には、販売注文および調整される請求として請求書番号への同じ参照 (販売ドキュメントから作成された請求) があります。</span><span class="sxs-lookup"><span data-stu-id="add7b-193">These adjustment claims have the same reference to the sales order and invoice number as the claims that are being adjusted (that is, the claims that were originally created from the sales document).</span></span>

<span data-ttu-id="add7b-194">再計算が完了したら、請求のステータスが**計算済**に変更され、**払戻計算ワークベンチ**ページに請求の再計算が表示されます。</span><span class="sxs-lookup"><span data-stu-id="add7b-194">After the recalculation is completed, the status of the claims is changed to **Calculated**, and the **Bill back workbench** page shows the claim recalculations.</span></span> <span data-ttu-id="add7b-195">再計算を承認するには、アクション ウィンドウで、**承認**を選択します。</span><span class="sxs-lookup"><span data-stu-id="add7b-195">To approve the recalculations, on the Action Pane, select **Approve**.</span></span>

### <a name="process-claims-and-pass-them-to-ar"></a><span data-ttu-id="add7b-196">請求を処理し A/R に渡します</span><span class="sxs-lookup"><span data-stu-id="add7b-196">Process claims and pass them to A/R</span></span>

<span data-ttu-id="add7b-197">請求は、A/R 処理の準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="add7b-197">The claims are now ready for A/R processing.</span></span> <span data-ttu-id="add7b-198">それらを処理するには、アクション ウィンドウで**プロセス**を選択します。</span><span class="sxs-lookup"><span data-stu-id="add7b-198">To process them, on the Action Pane, select **Process**.</span></span> <span data-ttu-id="add7b-199">次に、**リベートの処理**ダイアログ ボックスで顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="add7b-199">Then, in the **Process rebates** dialog box, select the customer.</span></span>

<span data-ttu-id="add7b-200">メッセージ センターメッセージと、請求のステータスが**マーク**に変わったという事実はどちらも、仕訳の転記によって次のイベントが発生したことを示します。</span><span class="sxs-lookup"><span data-stu-id="add7b-200">Together, the messages in the Message Center and the fact that the status of the claims has changed to **Mark** indicate that a journal posting has caused the following events to occur.</span></span> <span data-ttu-id="add7b-201">(転記される仕訳は、A/R パラメーターで指定されているとおりリベート見越計上仕訳です)。</span><span class="sxs-lookup"><span data-stu-id="add7b-201">(The journal that is posted is the Rebate accrual journal, as specified in the A/R parameters.)</span></span>

- <span data-ttu-id="add7b-202">請求は、控除として一時顧客残高に転送されました。</span><span class="sxs-lookup"><span data-stu-id="add7b-202">The claims have been transferred to the temporary customer balance as deductions.</span></span>
- <span data-ttu-id="add7b-203">リベート見越勘定は、顧客の将来の負債を表すよう貸方に転記されました。</span><span class="sxs-lookup"><span data-stu-id="add7b-203">The Rebate accrual account has been credited to represent the future liability for the customer.</span></span>
- <span data-ttu-id="add7b-204">リベート経費勘定が販売に関連して発生した原価を認識するよう借方に転記されました。</span><span class="sxs-lookup"><span data-stu-id="add7b-204">The Rebate expense account has been debited to recognize the cost that was incurred in connection with the sales.</span></span>

<span data-ttu-id="add7b-205">プロセスを完了するには、A/R 係は貸方票 (負債) として顧客残高に転送することで見越計上の控除を処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="add7b-205">To complete the process, the A/R clerk must now handle the accrual deductions by transferring them to the customers balance as a credit note (liability).</span></span>

<span data-ttu-id="add7b-206">**販売とマーケティング** \> **顧客** \> **すべての顧客** を選択し、フィルタを使用して目的の顧客を見つけます。</span><span class="sxs-lookup"><span data-stu-id="add7b-206">Select **Sales and marketing** \> **Customers** \> **All customers**, and use the filter to find the desired customer.</span></span> <span data-ttu-id="add7b-207">アクション ウィンドウで **収集** \> **トランザクションの決済** を選択します。</span><span class="sxs-lookup"><span data-stu-id="add7b-207">On the Action Pane, select **Collect** \> **Settle transactions**.</span></span> <span data-ttu-id="add7b-208">次に、**トランザクションの決済**ページで、**機能** \> **払戻計算プログラム**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="add7b-208">Then, on the **Settle transactions** page, select **Functions** \> **Bill back program**.</span></span> <span data-ttu-id="add7b-209">このリベート ページには、以前に処理されたすべての払戻計算請求が表示されます。</span><span class="sxs-lookup"><span data-stu-id="add7b-209">This rebate page shows all the bill-back claims that were previously processed.</span></span>

<span data-ttu-id="add7b-210">貸方票を作成する場合は、すべての明細行の**マーク**チェック ボックスを選択し、**機能** \> **貸方票の作成**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="add7b-210">If you want to create a credit note, select the **Mark** check box for all lines, and then select **Functions** \> **Create credit note**.</span></span>

<span data-ttu-id="add7b-211">メッセージ バーに、仕訳が転記されたことが表示されます。</span><span class="sxs-lookup"><span data-stu-id="add7b-211">A message bar informs you that a journal has been posted.</span></span> <span data-ttu-id="add7b-212">(A/R パラメーターで指定されている通り、転記される仕訳帳は AR 消費仕訳帳です。) その結果、実際の負債 (貸方) 金額が顧客残高に移動しました。</span><span class="sxs-lookup"><span data-stu-id="add7b-212">(The journal that is posted is the AR consumption journal, as specified in the A/R parameters.) As a result, the real liability (credit) amount has been moved to the customer balance.</span></span> <span data-ttu-id="add7b-213">財務的には、この状況は次のイベントが発生したことを意味します。</span><span class="sxs-lookup"><span data-stu-id="add7b-213">Financially, this situation implies that the following events have occurred:</span></span>

- <span data-ttu-id="add7b-214">顧客の売掛金勘定が貸方に転記されました。</span><span class="sxs-lookup"><span data-stu-id="add7b-214">The customer's Receivable account has been credited.</span></span>
- <span data-ttu-id="add7b-215">リベート見越計上勘定が借方に転記されました。</span><span class="sxs-lookup"><span data-stu-id="add7b-215">The Rebate accrual account has been debited.</span></span>

<span data-ttu-id="add7b-216">**一括比例配分**タイプの販売促進イベントを承認するには、**取引割引契約**ページでイベントを選択し、次に**金額**タブで**承認**を選択します。</span><span class="sxs-lookup"><span data-stu-id="add7b-216">To approve a merchandising event of the **Lump sum** type, select the event on the **Trade allowance agreements** page, and then, on the **Amount** tab, select **Approve**.</span></span>

## <a name="settle-the-deduction-that-is-due-and-the-customer-short-pay-by-using-the-deduction-workbench"></a><span data-ttu-id="add7b-217">期日控除の決済および控除ワークベンチを使用する顧客の短期支払</span><span class="sxs-lookup"><span data-stu-id="add7b-217">Settle the deduction that is due and the customer short-pay by using the Deduction workbench</span></span>

<span data-ttu-id="add7b-218">多くの場合、払戻計算を見越して、顧客は選択した請求書の短期支払を選択します。</span><span class="sxs-lookup"><span data-stu-id="add7b-218">Often, in anticipation of bill-backs, customer choose to short-pay selected invoices.</span></span> <span data-ttu-id="add7b-219">将来の支払調整の問題を防ぐために、 A/R 係は実際の顧客支払を記録する際に控除としてそれらの短期支払を登録します。</span><span class="sxs-lookup"><span data-stu-id="add7b-219">To prevent payment reconciliation issues in the future, the A/R clerk registers those short-pays as deductions when he or she records the actual customer payments.</span></span> <span data-ttu-id="add7b-220">次に、控除ワークベンチで、それらの顧客控除は会社から支払われる請求金額に対して簡単に決済できます。</span><span class="sxs-lookup"><span data-stu-id="add7b-220">Then, on the Deduction workbench, those customer deductions can easily be settled against the claim amounts that are due from the company.</span></span>

<span data-ttu-id="add7b-221">支払仕訳帳で顧客の短期支払を登録するには、**売掛金勘定** \> **支払** \> **支払仕訳帳**の順に選択し、新しい支払仕訳帳を作成します。</span><span class="sxs-lookup"><span data-stu-id="add7b-221">To register a customer's short-pay in the Payment journal, select **Accounts receivable** \> **Payments** \> **Payment journal**, and create a new payment journal.</span></span> <span data-ttu-id="add7b-222">アクション ウィンドウで、**控除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="add7b-222">Then, on the Action Pane, select **Deductions**.</span></span> <span data-ttu-id="add7b-223">**控除**ページで、短期で支払われた金額を作成および追跡できます。</span><span class="sxs-lookup"><span data-stu-id="add7b-223">On the **Deduction** page, you can create and track the amount that was short-paid.</span></span>

## <a name="analyze-the-effectiveness-of-the-promotion-and-fund-consumption"></a><span data-ttu-id="add7b-224">プロモーションと資金消費の有効性の分析</span><span class="sxs-lookup"><span data-stu-id="add7b-224">Analyze the effectiveness of the promotion and fund consumption</span></span>

<span data-ttu-id="add7b-225">プログラムの主要な統計情報および資金活用の概要を取得するには、取引割引管理で利用可能ないくつかのレポートおよび分析ビューを使用できます。</span><span class="sxs-lookup"><span data-stu-id="add7b-225">To get an overview of the program's key statistics and fund use, you can use several reports and analytical views that are available in Trade allowance management.</span></span>

<span data-ttu-id="add7b-226">**販売とマーケティング** \> **取引割引** \> **取引割引活動**\>**取引割引活動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="add7b-226">Select **Sales and marketing** \> **Trade allowances** \> **Trade allowance activity** \> **Trade allowance activity**.</span></span>

<span data-ttu-id="add7b-227">**取引割引活動**ページで、**概要**タブには取引割引契約の主要な詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="add7b-227">On the **Trade allowance activity** page, the **Overview** tab shows the main details of the trade allowance agreement.</span></span> <span data-ttu-id="add7b-228">他のタブでは、関連するドキュメント、支払、およびプログラムに関連する他のイベントに関する詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="add7b-228">The other tabs show more specific details about the associated documents, payments, and other events that are related to the program.</span></span>

<span data-ttu-id="add7b-229">**集計**タブを選択すると、プロモーションの下で販売した製品の合計数量、請求済の売上金額、および支払済の払戻計算および一括比例配分が表示されます。</span><span class="sxs-lookup"><span data-stu-id="add7b-229">Select the **Summary** tab to view the total quantity of products that have been sold under the promotion, the sales amount that has been invoiced, and the bill-backs and lump sums that have been paid.</span></span>

<span data-ttu-id="add7b-230">**払戻計算クレジット**タブを選択すると、顧客に対して貸方に転記された個々の払戻計算の詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="add7b-230">Select the **Bill back credits** tab to view the details of individual bill-backs that have been credited to the customer.</span></span>

<span data-ttu-id="add7b-231">プロモーションに対するさまざまなパフォーマンス測定の分析概要をさらに取得するには、分析ビューを使用できます。</span><span class="sxs-lookup"><span data-stu-id="add7b-231">To get a more analytical overview of the various performance measures for the promotion, you can use the Analysis view.</span></span>

<span data-ttu-id="add7b-232">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="add7b-232">Select **Save**.</span></span>

