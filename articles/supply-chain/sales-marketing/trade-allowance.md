---
title: 取引割引管理
description: このトピックでは、Dynamics 365 Supply Chain Management の取引割引管理について説明します。
author: t-benebo
manager: AnnBe
ms.date: 08/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: t-benebo
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 623c25490964ccdf6abc37acaffee7ac0844cf39
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251158"
---
# <a name="trade-allowance-management"></a><span data-ttu-id="a62a4-103">取引割引管理</span><span class="sxs-lookup"><span data-stu-id="a62a4-103">Trade allowance management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a62a4-104">取引割引管理により、会社が量および行動目標を達成する顧客に対して小売の「能力給」金銭的報奨を提供する販売プロモーション プログラムを管理するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-104">Trade allowance management helps companies manage sales promotion programs that offer retail "pay-for-performance" monetary rewards to customers that achieve volume and behavioral goals.</span></span> <span data-ttu-id="a62a4-105">機能の処理能力は、プロモーション資金の予算および配賦から、割引契約の設定、請求の作成と処理、支払い処理、プロモーション効果分析まで、包括的な利益のレベル上げプロセスに重点を置く企業向けに設計されています。</span><span class="sxs-lookup"><span data-stu-id="a62a4-105">The feature’s capabilities are designed for companies that focus on comprehensive promote-to-profit processes, from promotion fund budgeting and allocation, to allowance contract setup, to claims creation and processing, to payment processing, to promotion effectiveness analysis.</span></span>


<span data-ttu-id="a62a4-106">この記事では、取引割引管理機能の広範な概要を提供し、販売プロモーション プログラムの管理に関連する標準的な一連のタスクを理解します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-106">This article will provide a broad overview of the Trade allowance management feature and will familiarize you with the typical set of tasks that are involved in managing a sales promotion program.</span></span> <span data-ttu-id="a62a4-107">運営および意思決定責任を持つ複数タイプのユーザーは、この機能を使用してそれぞれの目標を達成します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-107">Several types of users who have operational and decision making responsibilities are expected to use this functionality to achieve their respective goals:</span></span>

- <span data-ttu-id="a62a4-108">払戻計算および 1 回限りの一括比例配分支払 (合意のサービス) に基づいて、選択した口座に裁量的資金を割り当て、プロモーションの取引割引管理を設定します</span><span class="sxs-lookup"><span data-stu-id="a62a4-108">Allocating discretionary funds to the selected accounts, and setting up trade allowance agreements for promotions, based on bill-backs and one-off lump sum payments (for an agreed service)</span></span>
- <span data-ttu-id="a62a4-109">継続的な販売を通して交渉されたプロモーション契約を実行し、払戻計算を生成します</span><span class="sxs-lookup"><span data-stu-id="a62a4-109">Running the negotiated promotion contracts through ongoing sales and generating bill-back claims</span></span>
- <span data-ttu-id="a62a4-110">計算、承認、生成された請求の処理、および支払決済の控除として売掛金勘定 (A/R) に転送</span><span class="sxs-lookup"><span data-stu-id="a62a4-110">Calculating, approving, and processing the generated claims, and passing them on to Accounts receivable (A/R) as deductions for payment settlement</span></span>
- <span data-ttu-id="a62a4-111">期日を迎える控除に対する顧客の短期支払の調整</span><span class="sxs-lookup"><span data-stu-id="a62a4-111">Reconciling the customer’s short-pay with the deduction that is due</span></span>
- <span data-ttu-id="a62a4-112">プロモーション資金の使用を追跡し、プログラムの収益性と有効性を評価します</span><span class="sxs-lookup"><span data-stu-id="a62a4-112">Tracking use of the promotional fund, and evaluating program profitability and effectiveness</span></span>

## <a name="audience-and-purpose"></a><span data-ttu-id="a62a4-113">対象者および目的</span><span class="sxs-lookup"><span data-stu-id="a62a4-113">Audience and purpose</span></span>

<span data-ttu-id="a62a4-114">このドキュメントの情報は、エンタープライズの会社での業務の意思決定者、購買マネージャーなどの職位、最高財務責任者 (CFO)、および会計マネージャーなどの、次の職責を対象としています。</span><span class="sxs-lookup"><span data-stu-id="a62a4-114">The information in this document is intended for business decision makers in enterprise companies, in positions such as purchase manager, chief financial officer (CFO), and accounting manager, who have the following responsibilities:</span></span>

- <span data-ttu-id="a62a4-115">高レベル予算と資金配賦</span><span class="sxs-lookup"><span data-stu-id="a62a4-115">High-level budgets and fund allocation</span></span>
- <span data-ttu-id="a62a4-116">販売プロモーションの計画および分析</span><span class="sxs-lookup"><span data-stu-id="a62a4-116">Planning and analyzing sales promotions</span></span>
- <span data-ttu-id="a62a4-117">払戻計算の処理、販売促進イベントに基づいて支払の実行、および短期支払や控除を決済するスタッフの管理</span><span class="sxs-lookup"><span data-stu-id="a62a4-117">Managing staff that processes bill-back claims, runs payments based on merchandizing events, and settles short-pays and deductions</span></span>

<span data-ttu-id="a62a4-118">これらのロールのユーザーは、以下の目標を達成する方法を求めています:</span><span class="sxs-lookup"><span data-stu-id="a62a4-118">People in these roles are looking for ways to achieve these goals:</span></span>

- <span data-ttu-id="a62a4-119">マーケティング プロモーション資金を有効に利用します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-119">Better use marketing promotional funds.</span></span>
- <span data-ttu-id="a62a4-120">さまざまなタイプのプロモーションプログラムおよび割引に柔軟に対応します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-120">Flexibly accommodate different types of promotion programs and allowances.</span></span>
- <span data-ttu-id="a62a4-121">管理の負担、およびプロモーションのパフォーマンスの監視と請求の処理に関連付けられるエラーを減らします。</span><span class="sxs-lookup"><span data-stu-id="a62a4-121">Reduce the administrative burden and errors that are associated with monitoring promotion performance and processing claims.</span></span>
- <span data-ttu-id="a62a4-122">将来の負債の見越計上によりキャッシュフロー予測の精度を高めます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-122">Improve cash flow forecasts by accruing for future liability.</span></span>
- <span data-ttu-id="a62a4-123">プロモーションについて、顧客との進行中および将来の交渉に関する定量化された基準があります。</span><span class="sxs-lookup"><span data-stu-id="a62a4-123">Have a quantified basis for ongoing and future negotiations with customers about promotions.</span></span>

## <a name="promotional-fund-and-trade-allowance-agreement"></a><span data-ttu-id="a62a4-124">プロモーション資金および取引割引契約書</span><span class="sxs-lookup"><span data-stu-id="a62a4-124">Promotional fund and Trade allowance agreement</span></span>

<span data-ttu-id="a62a4-125">取引割引契約は、特定の量ターゲットや行動目標を達成する顧客に能力給の金銭的報奨を提供するインセンティブ プログラムです。</span><span class="sxs-lookup"><span data-stu-id="a62a4-125">A trade allowance agreement is an incentive program where pay-for-performance monetary rewards are offered to customers that achieve specific volume targets and/or behavioral goals.</span></span> <span data-ttu-id="a62a4-126">プロモーション資金は予算経費です。</span><span class="sxs-lookup"><span data-stu-id="a62a4-126">Promotional funds are budgeted expenditures.</span></span> <span data-ttu-id="a62a4-127">この方法により、プロモーション キャンペーンをキャプチャできます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-127">In that way, the promotional campaigns can be captured.</span></span>

### <a name="promotional-fund"></a><span data-ttu-id="a62a4-128">プロモーション資金</span><span class="sxs-lookup"><span data-stu-id="a62a4-128">Promotional fund</span></span>

<span data-ttu-id="a62a4-129">取引割引契約に割り当てられる資金は、**資金**ページに記録されます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-129">Funds that are allocated to trade allowance agreements are recorded on the **Funds** page.</span></span> <span data-ttu-id="a62a4-130">**資金**ページを開くには、**販売およびマーケティング** \> **取引割引** \> **資金** \> **資金**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-130">To open the **Funds** page, select **Sales and marketing** \> **Trade allowances** \> **Funds** \> **Funds**.</span></span>

<span data-ttu-id="a62a4-131">![資金ページ](./media/trade-allowance-management-funds-page.png "資金ページ")</span><span class="sxs-lookup"><span data-stu-id="a62a4-131">![Funds page](./media/trade-allowance-management-funds-page.png "Funds page")</span></span>

<span data-ttu-id="a62a4-132">**資金**ページで、プロモーション資金の詳細を表示できます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-132">On the **Funds** page, you can view the details of promotional funds.</span></span>

<span data-ttu-id="a62a4-133">**一般**クイック タブでは、資金が有効である期間と予算金額を表示します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-133">The **General** FastTab shows the period that the fund is valid for and its budgeted amount.</span></span> <span data-ttu-id="a62a4-134">プロモーション契約に割り当てられる資金に対して、**ステータス**フィールドは**承認済**の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a62a4-134">In order for the fund to be allocated to the promotion agreement, the **Status** field must have a value of **Approved**.</span></span>

<span data-ttu-id="a62a4-135">**顧客**クイック タブでは顧客階層が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-135">The **Customers** FastTab shows the customer hierarchy.</span></span> <span data-ttu-id="a62a4-136">資金がターゲットとする顧客を選択するには、**資金顧客**の下になるようドラッグします。</span><span class="sxs-lookup"><span data-stu-id="a62a4-136">To select the customers that the fund targets, drag them so that they are under **Fund customers**.</span></span> <span data-ttu-id="a62a4-137">このクイック タブでは、資金の合計金額が配分される方法も示されます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-137">This FastTab also shows how the total amount of the fund is distributed.</span></span>

<span data-ttu-id="a62a4-138">**品目**クイック タブではプロモーションに含まれる品目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-138">The **Items** FastTab shows the items that are included in the promotion.</span></span>

### <a name="trade-allowance-agreement"></a><span data-ttu-id="a62a4-139">取引割引契約</span><span class="sxs-lookup"><span data-stu-id="a62a4-139">Trade allowance agreement</span></span>

<span data-ttu-id="a62a4-140">ファンドの定義が完了した後、プロモーション計画の次のステップはプロモーション契約 (貿易手当契約と呼ばれる) を登録し、資金を割り当て、各販売促進イベントに対するパフォーマンス目標を定義することです。</span><span class="sxs-lookup"><span data-stu-id="a62a4-140">After the fund definition is in place, the next step in promotion planning is to register promotion contracts (which are known as trade allowance agreements), allocate funds, and define performance goals for each merchandizing event.</span></span>

<span data-ttu-id="a62a4-141">取引割引契約は**取引割引契約**ページに記録されます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-141">Trade allowance agreements are recorded on the **Trade allowance agreements** page.</span></span> <span data-ttu-id="a62a4-142">**取引割引契約**ページを開き、**販売およびマーケティング** \> **取引割引** \> **取引割引契約**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-142">To open the **Trade allowance agreements** page, select **Sales and marketing** \> **Trade allowances** \> **Trade allowance agreements**.</span></span>

<span data-ttu-id="a62a4-143">![取引割引契約ページ](./media/trade-allowance-management-agreements-page.png "取引割引契約ページ")</span><span class="sxs-lookup"><span data-stu-id="a62a4-143">![Trade allowance agreements page](./media/trade-allowance-management-agreements-page.png "Trade allowance agreements page")</span></span>

#### <a name="header"></a><span data-ttu-id="a62a4-144">表題</span><span class="sxs-lookup"><span data-stu-id="a62a4-144">Header</span></span>

<span data-ttu-id="a62a4-145">**ヘッダー**を選択してヘッダー ビューに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-145">Select **Header** to switch to the Header view.</span></span>

<span data-ttu-id="a62a4-146">**一般**クイック タブで、契約が有効な期間が**注文終了日**および**注文開始日**フィールドで定義されます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-146">On the **General** FastTab, the **Order to** and **Order from** fields define the period when the agreement is valid.</span></span> <span data-ttu-id="a62a4-147">契約に対する**社内承認済**の承認ステータスは、契約がまだ有効ではなく、販売注文処理中に適用できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-147">An approval status of **Internal approved** for the agreement indicates that the agreement isn't yet valid and can't be applied during sales order processing.</span></span>

<span data-ttu-id="a62a4-148">**一般**クイック タブの**分析**セクションには、プロモーション評価に対して使用される数量および原価を定義する重要なフィールドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-148">The **Analysis** section of the **General** FastTab contains important fields that define the quantities and costs that are used for promotion evaluation:</span></span>

- <span data-ttu-id="a62a4-149">**基本単位**フィールドでは、プロモーションが適用される前に、選択した顧客に販売される必要がある製品の数量が指定されます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-149">The **Base units** field specifies the quantity of products that must be sold to the selected customers before the promotion is applied.</span></span>
- <span data-ttu-id="a62a4-150">**計算済出荷数量**値は**リフト率**の値に基づいて計算され、このプロモーションの目標達成昇給となります。</span><span class="sxs-lookup"><span data-stu-id="a62a4-150">The **Calculated ship quantity** value is calculated based on the **Lift percent** value, which is a planned target increase for this promotion.</span></span>
- <span data-ttu-id="a62a4-151">取引割引契約でのさまざまなイベントの数量に基づいて、**取引割引コスト**フィールドが計算されます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-151">The **Trade allowance cost** field is calculated based on the quantities of the various events in the trade allowance agreement.</span></span>

<span data-ttu-id="a62a4-152">左側のリストの**顧客**クイック タブで、顧客グループを選択および表示でき、事前定義された階層として設定されます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-152">On the **Customers** FastTab, in the list on the left, you can select and view customer groups, which are set up as predefined hierarchies.</span></span> <span data-ttu-id="a62a4-153">割引契約のターゲットとして、階層全体または特定の勘定を選択できます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-153">You can then select the whole hierarchy or specific accounts as targets for the allowance agreement.</span></span>

<span data-ttu-id="a62a4-154">**資金**ページの**品目**クイック タブと同じように、**品目**クイック タブで、その販売を合意した割引に関連付けるための契約に製品が追加されます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-154">On the **Items** FastTab, as on the **Items** FastTab of the **Funds** page, products are added to the agreement to associate its sales with the allowance that was agreed on.</span></span>

<span data-ttu-id="a62a4-155">**資金**クイック タブで、この契約に関連付けられているプロモーション資金を表示できます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-155">On the **Funds** FastTab, you can view the promotion funds that are associated with this contract.</span></span> <span data-ttu-id="a62a4-156">また、契約のイベント原価配賦を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-156">You can also view the contract's event cost allocation.</span></span> <span data-ttu-id="a62a4-157">100% のイベント原価配賦とは、このプロモーションが 1 つの資金からのみ資金調達することを意味します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-157">An event cost allocation of 100 percent means that this promotion will be financed exclusively from one fund.</span></span> <span data-ttu-id="a62a4-158">または、プロモーション契約はいくつかの資金を活用し、同等または異なる配賦割合を使用できます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-158">Alternatively, a promotion agreement can draw on several funds, and can use equal or differential percentage allocation.</span></span>

#### <a name="lines"></a><span data-ttu-id="a62a4-159">ライン</span><span class="sxs-lookup"><span data-stu-id="a62a4-159">Lines</span></span>

<span data-ttu-id="a62a4-160">次に、**明細行**を選択して明細行ビューに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-160">Next, select **Lines** to switch to the Lines view.</span></span>

<span data-ttu-id="a62a4-161">**販売促進イベント**タブで、契約の対象となるイベントのタイプが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-161">The **Merchandizing events** tab shows the types of events covered by an agreement.</span></span> <span data-ttu-id="a62a4-162">次の 3 つのタイプがあります: 払戻計算、一括比例配分および定率割引。</span><span class="sxs-lookup"><span data-stu-id="a62a4-162">There are three types: bill back, lump sum and off-invoice.</span></span>

<span data-ttu-id="a62a4-163">販売促進イベントを選択し**金額**タブを選択すると、イベントの詳細が検出されます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-163">When you select the merchandizing event and then select the **Amounts** tab, the details for the event are found.</span></span>

<span data-ttu-id="a62a4-164">![取引割引契約明細行](./media/trade-allowance-management-agreements-lines.png "取引割引契約明細行")</span><span class="sxs-lookup"><span data-stu-id="a62a4-164">![Trade allowance agreement lines](./media/trade-allowance-management-agreements-lines.png "Trade allowance agreement lines")</span></span>

<span data-ttu-id="a62a4-165">**取引割引明細行**セクションで、報奨を取得するための定義に対して顧客が達成する必要がある数量または金額の範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-165">In the **Trade allowance lines** section, you specify the quantity or amount ranges that the customer must achieve for definitions to obtain the rewards.</span></span>

<span data-ttu-id="a62a4-166">**払戻計算**タイプの販売促進イベントの場合、**金額**タブの上部セクションで払戻計算の適用、生成、支払のルールを定義します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-166">In the case of a merchandizing event of the **Bill back** type, the upper section the **Amounts** tab defines the rules that the bill back will be applied, generated, and paid under.</span></span> <span data-ttu-id="a62a4-167">たとえば、ルールは、払戻計算請求に対する次の条件を指定する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a62a4-167">For example, the rules may specify the following conditions for the bill back claim:</span></span>

- <span data-ttu-id="a62a4-168">販売注文 (**計算日タイプ**値が**作成済**である) の作成日に基づきます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-168">It’s based on the creation date of the sales order (the **Calculation date type** value is **Created**).</span></span>
- <span data-ttu-id="a62a4-169">正味金額ではなく、割引前の販売注文明細行の金額に基づいて計算され、それには割引 (**取得元**値が**総計**である) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-169">It’s calculated based on the sales order line’s amount before discounts, not the net amount, which includes discounts (the **Taken from** value is **Gross**).</span></span>
- <span data-ttu-id="a62a4-170">金額 (**リベート改行タイプ**値が**数量**である) ではなく、販売済製品の量に基づきます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-170">It’s based on the volume of the sold products, not the amount (the **Rebate line break type** value is **Quantity**).</span></span>
- <span data-ttu-id="a62a4-171">1 か月 (**売上を累計する単位**の値が**月**である) の期間あたりで計算されます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-171">It’s calculated per period of a month (the **Cumulate sales by** value is **Month**).</span></span> 
- <span data-ttu-id="a62a4-172">A/P (**支払タイプ**値が**顧客控除**である) を使用するのではなく、控除として決済されます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-172">It’s settled as a deduction, not by using A/P (the **Payment type** value is **Customer deductions**).</span></span>

<span data-ttu-id="a62a4-173">**一括比例配分**の販売促進イベントの場合、**金額**タブでは、顧客が特定のパフォーマンスを達成する場合に、控除のフォームで顧客に支払われる数量が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-173">In the case of a merchandizing event of the **Lump sum** type, the **Amounts** tab shows the quantity that will be paid to the customer in the form of a deduction when the customer achieves specific performance.</span></span> <span data-ttu-id="a62a4-174">**未処理**の承認ステータスは、一括比例配分まだ支払われていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-174">An approval status of **Open** indicates that the lump sum hasn't yet been paid.</span></span>

<span data-ttu-id="a62a4-175">契約条件を満たす販売注文に契約を適用するには、契約のステータスが**確認済**である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a62a4-175">To apply the agreement to sales orders that meet the agreement's conditions, the agreement's status must be **Confirmed**.</span></span> 

## <a name="perform-sales-under-the-planned-merchandising-event-and-generate-bill-back-claims"></a><span data-ttu-id="a62a4-176">計画された販売促進イベントの下での売り込みの実行および払戻計算請求の生成</span><span class="sxs-lookup"><span data-stu-id="a62a4-176">Perform sales under the planned merchandising event and generate bill-back claims</span></span>

<span data-ttu-id="a62a4-177">契約の条件を満たす明細行を持つ販売注文を作成する場合、**販売注文**ページで**販売注文明細行** \> **表示** \> **価格の詳細**の順に選択して関連する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-177">When you create a sales order that has lines that fulfill the requirements of the agreement, you can view the related information on the **Sales order** page by selecting **Sales order line** \> **View** \> **Price details**.</span></span>

<span data-ttu-id="a62a4-178">**価格の詳細**ページの**リベート**クイック タブで、販売員は、有効な取引割引契約 (リベート プログラム ID が表示される) からの払戻計算および明細行に適用される合計金額を参照できます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-178">On the **Price details** page, on the **Rebates** FastTab, the sales clerk can see a bill back from the valid trade allowance agreement (the rebate program ID is shown) and the total amount that is applied to the line.</span></span> <span data-ttu-id="a62a4-179">この金額は、**価格の詳細**ページの**利益見積**のセクションにある**リベート金額**フィールドでも表示されます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-179">This amount is also shown in the **Rebate amount** field in the **Margin estimation** section of the **Price details** page.</span></span>

<span data-ttu-id="a62a4-180">売上請求書が転記されると、各請求明細行に対応する払戻計算請求が生成されます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-180">When the sales invoice is posted, a corresponding bill-back claim is generated for each invoice line.</span></span>

> [!NOTE]
> <span data-ttu-id="a62a4-181">**価格の詳細**ページを表示するには、**売掛金勘定パラメーター**ページの**価格**タブで、**価格の詳細の有効化**チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a62a4-181">To see the **Price details** page, on the **Accounts receivable parameters** page, on the **Prices** tab, select the **Enable price details** check box.</span></span> <span data-ttu-id="a62a4-182">I</span><span class="sxs-lookup"><span data-stu-id="a62a4-182">I</span></span>

## <a name="process-claims-and-pass-them-as-deductions-to-ar"></a><span data-ttu-id="a62a4-183">請求を処理し A/R に控除として渡します</span><span class="sxs-lookup"><span data-stu-id="a62a4-183">Process claims and pass them as deductions to A/R</span></span>

<span data-ttu-id="a62a4-184">払戻計算を処理するプロセスでの次の手順は、確認、計算、請求の承認、および控除への変換です。</span><span class="sxs-lookup"><span data-stu-id="a62a4-184">The next steps in the process for handling bill-backs are to review, calculate, and approve claims, and then convert them into deductions.</span></span>

<span data-ttu-id="a62a4-185">払戻計算ワークベンチでは、プロモーション契約の所有者が生成される請求を定期的にレビューおよび処理します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-185">The Bill back workbench is where the promotion agreement owner periodically reviews and processes the claims that are generated.</span></span> <span data-ttu-id="a62a4-186">また、請求の支払方法に応じて A/R 管理者が承認済請求を控除または定期的な支払に変換します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-186">It's also where the A/R administrator converts the approved claims into deductions or regular payments, depending on the payment method for the claim.</span></span>

<span data-ttu-id="a62a4-187">**払戻計算ワークベンチ**ページで、請求明細行を確認できます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-187">On the **Bill back workbench** page, you can review the claim lines.</span></span> <span data-ttu-id="a62a4-188">請求が**再計算する**ステータスである場合、任意の累積効果に対して再計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a62a4-188">If the claims are in **To be recalculated** status, they must be recalculated for any cumulative effect.</span></span>

### <a name="recalculate-claims"></a><span data-ttu-id="a62a4-189">請求の再計算</span><span class="sxs-lookup"><span data-stu-id="a62a4-189">Recalculate claims</span></span>

<span data-ttu-id="a62a4-190">請求を再計算するには、アクション ウィンドウで、**累計**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-190">To recalculate the claims, on the Action Pane, select **Cumulate**.</span></span> <span data-ttu-id="a62a4-191">次に、**リベートの累計**ダイアログ ボックスで顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-191">Then, in the **Cumulate rebates** dialog box, select the customer.</span></span>

<span data-ttu-id="a62a4-192">再計算の結果として、プログラムでは、元の請求から各単位の特定の金額へと調整するその金額に対して、新しい請求を生成します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-192">As a result of the recalculation, the program generates new claims for the amounts to adjust the original claims to the qualifying amount per unit.</span></span> <span data-ttu-id="a62a4-193">顧客、品目、通貨、測定単位、在庫分析コード、財務分析コード、および売上税グループの固有の組み合わせごとに 1 つの調整請求が生成されます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-193">One adjustment claim is generated for each unique combination of a customer, an item, a currency, a unit of measure, inventory dimensions, financial dimensions, and a sales tax group.</span></span> <span data-ttu-id="a62a4-194">これらの調整請求には、販売注文および調整される請求として請求書番号への同じ参照 (販売ドキュメントから作成された請求) があります。</span><span class="sxs-lookup"><span data-stu-id="a62a4-194">These adjustment claims have the same reference to the sales order and invoice number as the claims that are being adjusted (that is, the claims that were originally created from the sales document).</span></span> <span data-ttu-id="a62a4-195">元の請求とは異なり、調整請求には元の販売注文明細行の金額と数量を表すフィールドに値がありません。</span><span class="sxs-lookup"><span data-stu-id="a62a4-195">Unlike the original claim, the adjustment claim doesn’t have values in the fields that describe the original sales order line’s amounts and quantity.</span></span>

<span data-ttu-id="a62a4-196">再計算が完了したらすると、請求のステータスが**計算済**に変更されます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-196">After the recalculation is completed, the status of the claims is changed to **Calculated**.</span></span> <span data-ttu-id="a62a4-197">請求を承認するには、アクション ウィンドウで、**承認**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-197">To approve the claims, on the Action Pane, select **Approve**.</span></span>

### <a name="process-claims-and-pass-them-to-ar"></a><span data-ttu-id="a62a4-198">請求を処理し A/R に渡します</span><span class="sxs-lookup"><span data-stu-id="a62a4-198">Process claims and pass them to A/R</span></span>

<span data-ttu-id="a62a4-199">請求は、A/R 処理の準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="a62a4-199">The claims are now ready for A/R processing.</span></span> <span data-ttu-id="a62a4-200">それらを処理するには、アクション ウィンドウで**プロセス**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-200">To process them, on the Action Pane, select **Process**.</span></span> 

<span data-ttu-id="a62a4-201">請求の処理時に、ステータスが**マーク**に変更され、仕訳帳の転記 (A/R パラメーターで指定されているように、転記された仕訳帳がリベート見越計上仕訳帳である) が次のイベントを発生させる原因であることを示します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-201">Upon processing the claims, the status has changed to **Mark** and indicates that a journal posting (the journal that is posted is the Rebate accrual journal, as specified in the A/R parameters) has caused the following events to occur:</span></span> 

- <span data-ttu-id="a62a4-202">請求は、控除として一時顧客残高に転送されました。</span><span class="sxs-lookup"><span data-stu-id="a62a4-202">The claims have been transferred to the temporary customer balance as deductions.</span></span>
- <span data-ttu-id="a62a4-203">リベート見越勘定は、顧客の将来の負債を表すよう貸方に転記されました。</span><span class="sxs-lookup"><span data-stu-id="a62a4-203">The rebate accrual account has been credited to represent the future liability for the customer.</span></span>
- <span data-ttu-id="a62a4-204">リベート経費勘定が販売に関連して発生した原価を認識するよう借方に転記されました。</span><span class="sxs-lookup"><span data-stu-id="a62a4-204">The rebate expense account has been debited to recognize the cost that was incurred in connection with the sales.</span></span>

<span data-ttu-id="a62a4-205">プロセスを完了するには、A/R 係は貸方票 (負債) として顧客残高に転送することで見越計上の控除を処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a62a4-205">To complete the process, the A/R clerk must now handle the accrual deductions by transferring them to the customers balance as a credit note (liability).</span></span> 

<span data-ttu-id="a62a4-206">タスクを開始するには、**顧客**ページのアクション ウィンドウで、**収集** \> **トランザクションの決済**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-206">To start the task, on the Action Pane of the **Customer** page, select **Collect** \> **Settle transactions**.</span></span> <span data-ttu-id="a62a4-207">次に、**トランザクションの決済**ページで、**機能** \> **払戻計算プログラム**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-207">Then, on the **Settle transactions** page, select **Functions** \> **Bill back program**.</span></span> <span data-ttu-id="a62a4-208">このリベート ページには、以前に処理されたすべての払戻計算請求が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-208">This rebate page shows all the bill-back claims that were previously processed.</span></span>

<span data-ttu-id="a62a4-209">貸方票を作成する場合は、すべての明細行の**マーク**チェック ボックスを選択し、**機能** \> **貸方票の作成**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-209">If you want to create a credit note, select the **Mark** check box for all lines, and then select **Functions** \> **Create credit note**.</span></span>

<span data-ttu-id="a62a4-210">貸方票の作成時に、仕訳帳が転記されます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-210">Upon credit note creation, a journal is posted.</span></span> <span data-ttu-id="a62a4-211">(A/R パラメーターで指定されている通り、転記される仕訳帳は AR 消費仕訳帳です。) その結果、実際の負債 (貸方) 金額が顧客残高に移動しました。</span><span class="sxs-lookup"><span data-stu-id="a62a4-211">(The journal that is posted is the AR consumption journal, as specified in the A/R parameters.) As a result, the real liability (credit) amount has been moved to the customer balance.</span></span> <span data-ttu-id="a62a4-212">財務的には、この状況は次のイベントが発生したことを意味します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-212">Financially, this situation implies that the following events have occurred:</span></span>

- <span data-ttu-id="a62a4-213">顧客の売掛金勘定が貸方に転記されました。</span><span class="sxs-lookup"><span data-stu-id="a62a4-213">The customer's receivable account has been credited.</span></span>
- <span data-ttu-id="a62a4-214">リベート見越計上勘定が借方に転記されました。</span><span class="sxs-lookup"><span data-stu-id="a62a4-214">The rebate accrual account has been debited.</span></span>

<span data-ttu-id="a62a4-215">**一括比例配分**タイプの販売促進イベントを承認するには、**取引割引契約**ページでイベントを選択し、次に**金額**タブで**承認**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-215">To approve a merchandising event of the **Lump sum** type, select the event on the **Trade allowance agreements** page, and then, on the **Amount** tab, select **Approve**.</span></span>

## <a name="settle-the-deduction-that-is-due-and-the-customer-short-pay-by-using-the-deduction-workbench"></a><span data-ttu-id="a62a4-216">期日控除の決済および控除ワークベンチを使用する顧客の短期支払</span><span class="sxs-lookup"><span data-stu-id="a62a4-216">Settle the deduction that is due and the customer short-pay by using the Deduction workbench</span></span>

<span data-ttu-id="a62a4-217">多くの場合、払戻計算を見越して、顧客は選択した請求書の短期支払を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-217">Often, in anticipation of bill-backs, customers choose to short-pay selected invoices.</span></span> <span data-ttu-id="a62a4-218">将来の支払調整の問題を防ぐために、 A/R 係は実際の顧客支払を記録する際に控除としてそれらの短期支払を登録します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-218">To prevent payment reconciliation issues in the future, the A/R clerk registers those short-pays as deductions when he or she records the actual customer payments.</span></span> <span data-ttu-id="a62a4-219">次に、控除ワークベンチで、それらの顧客控除は会社から支払われる請求金額に対して簡単に決済できます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-219">Then, on the Deduction workbench, those customer deductions can easily be settled against the claim amounts that are due from the company.</span></span>

<span data-ttu-id="a62a4-220">支払仕訳帳で顧客の短期支払を登録するには、**売掛金勘定** \> **支払** \> **支払仕訳帳**の順に選択し、新しい支払仕訳帳を作成します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-220">To register a customer's short-pay in the Payment journal, select **Accounts receivable** \> **Payments** \> **Payment journal**, and create a new payment journal.</span></span> <span data-ttu-id="a62a4-221">アクション ウィンドウで、**控除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-221">Then, on the Action Pane, select **Deductions**.</span></span> <span data-ttu-id="a62a4-222">**控除**ページで、短期で支払われた金額を作成および追跡できます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-222">On the **Deduction** page, you can create and track the amount that was short-paid.</span></span>

<span data-ttu-id="a62a4-223">コレクション マネージャは、未処理の貸方票トランザクションおよび短期支払トランザクションを控除ワークベンチで互いに決済する責任があります。</span><span class="sxs-lookup"><span data-stu-id="a62a4-223">The collection manager is now responsible for settling the open credit note transaction and the short-pay transaction against each other in the Deduction workbench.</span></span>

<span data-ttu-id="a62a4-224">控除を管理するには、**販売およびマーケティング** \> **取引割引** \> **控除** \> **控除ワークベンチ**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-224">To manage deductions, select **Sales and marketing** \> **Trade allowances** \> **Deductions** \> **Deduction workbench**.</span></span> <span data-ttu-id="a62a4-225">ページの上部セクションには、顧客からの短期支払を表す明細行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-225">The upper section of the page contains lines that represent the short-pays from the customer.</span></span> <span data-ttu-id="a62a4-226">ページの下部セクションには、顧客の未処理の貸方トランザクションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-226">The lower section of the page contains the customers open credit transactions.</span></span> 

<span data-ttu-id="a62a4-227">未処理のトランザクションに対して控除を決済するには、控除明細行をマークし、次に未処理トランザクション タブで、明細行をマークします。</span><span class="sxs-lookup"><span data-stu-id="a62a4-227">To settle the deduction against the open transaction, mark the deduction line, and then, on the Open transactions tab, mark the line.</span></span> <span data-ttu-id="a62a4-228">アクション ウィンドウで、管理 > 照合をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62a4-228">On the Action Pane, click Maintain > Match.</span></span>

<span data-ttu-id="a62a4-229">元の請求のステータスを、**完了**に設定します。</span><span class="sxs-lookup"><span data-stu-id="a62a4-229">The status of the originating claims is now set to **Completed**.</span></span>

## <a name="analyze-the-effectiveness-of-the-promotion-and-fund-consumption"></a><span data-ttu-id="a62a4-230">プロモーションと資金消費の有効性の分析</span><span class="sxs-lookup"><span data-stu-id="a62a4-230">Analyze the effectiveness of the promotion and fund consumption</span></span>

<span data-ttu-id="a62a4-231">プログラムの主要な統計情報および資金活用の概要を取得するには、取引割引管理で利用可能ないくつかのレポートおよび分析ビューを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-231">To get an overview of the program's key statistics and fund use, you can use several reports and analytical views that are available in Trade allowance management.</span></span>

<span data-ttu-id="a62a4-232">**取引割引活動**ページで、**概要**タブには取引割引契約の主要な詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-232">On the **Trade allowance activity** page, the **Overview** tab shows the main details of the trade allowance agreement.</span></span> <span data-ttu-id="a62a4-233">他のタブでは、関連するドキュメント、支払、およびプログラムに関連する他のイベントに関する詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-233">The other tabs show more specific details about the associated documents, payments, and other events that are related to the program.</span></span>

<span data-ttu-id="a62a4-234">**集計**タブでは、プロモーションの下で販売した製品の合計数量、請求済の売上金額、および支払済の払戻計算および一括比例配分が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-234">The **Summary** tab shows the total quantity of products that have been sold under the promotion, the sales amount that has been invoiced, and the bill-backs and lump sums that have been paid.</span></span>

<span data-ttu-id="a62a4-235">**払戻計算クレジット**タブには、顧客に対して貸方に転記された個々の払戻計算の詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-235">The **Bill back credits** tab contains the details of individual bill-backs that have been credited to the customer.</span></span>

<span data-ttu-id="a62a4-236">プロモーションに対するさまざまなパフォーマンス測定の分析概要をさらに取得するには、分析ビューを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-236">To get a more analytical overview of the various performance measures for the promotion, you can use the Analysis view.</span></span> <span data-ttu-id="a62a4-237">分析ビューに移動するには、**販売およびマーケティング** \> **取引割引** \> **取引割引契約**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62a4-237">To go to the Analysis view, click **Sales and marketing** \> **Trade allowances** \> **Trade allowance agreements**.</span></span> <span data-ttu-id="a62a4-238">アクション ウィンドウで、**分析**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62a4-238">On the Action Pane, click **Analysis**.</span></span>  

<span data-ttu-id="a62a4-239">プロモーションに対するさまざまなパフォーマンス測定の分析概要をさらに取得するには、分析ビューを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a62a4-239">To get a more analytical overview of the various performance measures for the promotion, you can use the Analysis view.</span></span> <span data-ttu-id="a62a4-240">分析ビューに移動するには、**販売およびマーケティング** \> **取引割引** \> **取引割引契約**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62a4-240">To go to the Analysis view, click **Sales and marketing** \> **Trade allowances** \> **Trade allowance agreements**.</span></span> <span data-ttu-id="a62a4-241">アクション ウィンドウで、**分析**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a62a4-241">On the Action Pane, click **Analysis**.</span></span> 

