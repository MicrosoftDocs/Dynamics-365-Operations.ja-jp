---
title: ロイヤルティ契約管理
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のロイヤルティ契約管理について説明します。
author: t-benebo
manager: AnnBe
ms.date: 08/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: t-benebo
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 50e4215957aa248de4f56754e465a4180a841426
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834549"
---
# <a name="royalty-contract-management"></a><span data-ttu-id="31361-103">ロイヤルティ契約管理</span><span class="sxs-lookup"><span data-stu-id="31361-103">Royalty contract management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31361-104">ロイヤルティ契約管理は、サード パーティの資産や知的財産権を使用する権利を行使する会社を対象としています。</span><span class="sxs-lookup"><span data-stu-id="31361-104">Royalty contract management is intended for companies that exercise the right to use a third party's assets and/or intellectual property.</span></span> <span data-ttu-id="31361-105">会社がロイヤリティの支払の管理、追跡、実行に関連するタスクを自動化することにより、ロイヤルティ契約を効率的に管理するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="31361-105">It helps companies better manage their royalty agreements by automating tasks that are involved in administering, tracking, and making royalty payments.</span></span>

<span data-ttu-id="31361-106">ここでは、ロイヤルティ手数料を処理するための標準的なプロセスの概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="31361-106">This topic provides a broad overview of the typical process for handling royalty fees:</span></span>

- <span data-ttu-id="31361-107">取り決めロイヤルティ契約の詳細を登録します。</span><span class="sxs-lookup"><span data-stu-id="31361-107">Register details of the negotiated royalty contract.</span></span>
- <span data-ttu-id="31361-108">継続的な販売を通して交渉された契約を実行し、ロイヤルティ請求を生成します。</span><span class="sxs-lookup"><span data-stu-id="31361-108">Run negotiated contracts through ongoing sales, and generate royalty claims.</span></span>
- <span data-ttu-id="31361-109">生成された請求を承認および処理し、支払のために買掛金勘定 (A/P) に渡せるようにします。</span><span class="sxs-lookup"><span data-stu-id="31361-109">Approve and process the generated claims, so that they can be passed on to Accounts payable (A/P) for payment.</span></span>

## <a name="audience-and-purpose"></a><span data-ttu-id="31361-110">対象者および目的</span><span class="sxs-lookup"><span data-stu-id="31361-110">Audience and purpose</span></span>

<span data-ttu-id="31361-111">このトピックの情報は、以下の触接を持つ、セールス マネージャー、会計マネージャー、A/P マネージャーなどの立場にいる、エンタープライズの会社での業務の意思決定者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="31361-111">The information in this topic is intended for business decision makers in enterprise companies, in capacities such as sales manager, accounting manager, and A/P manager, who have the following responsibilities:</span></span>

- <span data-ttu-id="31361-112">ライセンサーとの契約の交渉</span><span class="sxs-lookup"><span data-stu-id="31361-112">Negotiating contracts with the licensor</span></span>
- <span data-ttu-id="31361-113">システムへのロイヤルティ契約条件と手数料率の記録</span><span class="sxs-lookup"><span data-stu-id="31361-113">Recording royalty agreement terms and fee rates in the system</span></span>
- <span data-ttu-id="31361-114">ロイヤルティ請求を処理し、手数料の支払を行うスタッフの管理</span><span class="sxs-lookup"><span data-stu-id="31361-114">Managing staff that processes royalty claims and makes fee payments</span></span>

<span data-ttu-id="31361-115">これらのロールのユーザーは、以下の目標を達成する方法を求めています:</span><span class="sxs-lookup"><span data-stu-id="31361-115">People in these roles are looking for ways to achieve these goals:</span></span>

- <span data-ttu-id="31361-116">ロイヤルティ契約とその状況の各種の定義に柔軟に対応します。</span><span class="sxs-lookup"><span data-stu-id="31361-116">Flexibly accommodate different definitions of royalty contracts and their conditions.</span></span>
- <span data-ttu-id="31361-117">管理の負担、およびロイヤルティ請求の追跡と処理に関連付けられるエラーを減らします。</span><span class="sxs-lookup"><span data-stu-id="31361-117">Reduce the administrative burden and errors that are associated with tracking and processing royalty claims.</span></span>
- <span data-ttu-id="31361-118">将来の買掛金を見越計上し、支払遅延に対する利息を回避することによって、キャッシュ フロー予測を向上します。</span><span class="sxs-lookup"><span data-stu-id="31361-118">Improve cash flow forecasts by accruing for future payables and avoiding interest on delayed payments.</span></span>

## <a name="royalty-contracts"></a><span data-ttu-id="31361-119">ロイヤルティ契約</span><span class="sxs-lookup"><span data-stu-id="31361-119">Royalty contracts</span></span>

<span data-ttu-id="31361-120">ロイヤルティ契約は、資産勘定または知的財産所有者との間のレコードです。</span><span class="sxs-lookup"><span data-stu-id="31361-120">A royalty contract is a record of an agreement with an asset or intellectual property owner.</span></span> <span data-ttu-id="31361-121">ライセンシーがそのプロパティを使用して収益を得る場合にライセンサーが金銭的報酬を得ることができる交渉済みの条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="31361-121">It specifies the negotiated terms and conditions under which the licensor qualifies for a monetary reward when the licensee uses its property to obtain revenue.</span></span>

<span data-ttu-id="31361-122">ロイヤルティ契約は、**ロイヤリティ契約**ページで登録されます。</span><span class="sxs-lookup"><span data-stu-id="31361-122">Royalty contracts are registered on the **Royalty contracts** page.</span></span> <span data-ttu-id="31361-123">**ロイヤルティ契約** ページを開くには、**買掛金勘定 \> ブローカーおよびロイヤルティ \> ロイヤルティ契約** を選びます。</span><span class="sxs-lookup"><span data-stu-id="31361-123">To open the **Royalty contracts** page, select **Accounts payable \> Broker and royalties \> Royalty agreements**.</span></span>

<span data-ttu-id="31361-124">![ロイヤルティ契約ページ](./media/royalty-contract-management-royalty-agreements-page.png "ロイヤルティ契約ページ")</span><span class="sxs-lookup"><span data-stu-id="31361-124">![Royalty agreements page](./media/royalty-contract-management-royalty-agreements-page.png "Royalty agreements page")</span></span>

<span data-ttu-id="31361-125">ページの下の部分の **選択** タブは、ロイヤリティ手数料の対象製品を示しています。</span><span class="sxs-lookup"><span data-stu-id="31361-125">The **Selection** tab in the lower part of the page shows the products that qualify for a royalty fee.</span></span>

<span data-ttu-id="31361-126">ページの上部にある **全般** タブでは、いくつかのフィールドにライセンサーと交渉した契約の条件の詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="31361-126">On the **General** tab in the upper part of the page, several fields provide more details about the agreement's conditions as they were negotiated with the licensor:</span></span>

- <span data-ttu-id="31361-127">**売上を累計する単位** フィールドは、累積的な販売に基づき、ロイヤリティ金額が計算される期間を指定します。</span><span class="sxs-lookup"><span data-stu-id="31361-127">The **Cumulate sales by** field specifies the period that a royalty amount will be calculated for, based on cumulative sales.</span></span> <span data-ttu-id="31361-128">たとえば、期間には 1 か月があります。</span><span class="sxs-lookup"><span data-stu-id="31361-128">For example, the period might be a month.</span></span> <span data-ttu-id="31361-129">または、販売注文明細行が請求されるたびにロイヤリティ金額を計算するには、**請求書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="31361-129">Alternatively, to calculate the royalty amount every time that a sales order line is invoiced, select **Invoice**.</span></span>
- <span data-ttu-id="31361-130">**承認が必要** オプションが **はい** に設定されている場合、ロイヤルティがライセンサーに支払われる請求書に変換する前に、ロイヤルティ プログラムの所有者が請求を承認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31361-130">If the **Approval required** option is set to **Yes**, a royalty program owner must approve the claims before a royalty can be turned into an invoice that is payable to the licensor.</span></span>
- <span data-ttu-id="31361-131">**見越勘定**および**経費勘定**フィールドは、承認と処理の間の中間のステージで受け取る未収リベート金額の勘定番号を示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="31361-131">The **Accrual account** and **Expense account** fields must specify account numbers that will receive accrued amounts during the intermediate stage between approval and processing.</span></span>

<span data-ttu-id="31361-132">ページの下にある **ロイヤリティ金額** タブでロイヤリティ レートを設定します。</span><span class="sxs-lookup"><span data-stu-id="31361-132">You set up royalty rates on the **Royalty amounts** tab in the lower part of the page.</span></span> <span data-ttu-id="31361-133">階層としてレートを設定するには、階層ごとに行を追加し、**範囲の開始値** および **範囲の終了値** フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="31361-133">To set up the rates as tiers, add a line for each tier, and set the **From value** and **To value** fields.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="31361-134">契約を有効にするには、アクション ウィンドウで **検証** を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31361-134">To make an agreement valid, you must select **Validation** on the Action Pane.</span></span> <span data-ttu-id="31361-135">ページの上部の **全般** タブにある **検証済み** オプションが **はい** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="31361-135">The **Validated** option on the **General** tab in the upper part of the page will then be set to **Yes**.</span></span>

## <a name="sell-products-that-qualify-for-a-royalty-fee-and-generate-a-claim"></a><span data-ttu-id="31361-136">ロイヤルティ手数料の対象となり、請求を生成する製品を販売する</span><span class="sxs-lookup"><span data-stu-id="31361-136">Sell products that qualify for a royalty fee and generate a claim</span></span>

<span data-ttu-id="31361-137">販売処理担当者が会社がロイヤルティ契約を持っている製品の販売注文を作成するとき、注文明細行の詳細がロイヤルティの対象となる場合、プログラムは将来のロイヤルティ手数料を識別します。</span><span class="sxs-lookup"><span data-stu-id="31361-137">When a sales processor creates a sales order for a product that the company has a royalty contract for, if the order line's details qualify for the royalty, the program identifies the future royalty fee.</span></span>

<span data-ttu-id="31361-138">販売注文明細行がロイヤリティ手数料の対象となるかどうかを確認するには、**販売注文明細行 \> 表示 \> 価格の詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="31361-138">To see whether a sales order line qualifies for a royalty fee, select **Sales order line \> View \> Price details**.</span></span> <span data-ttu-id="31361-139">**価格の詳細**ページで、**ロイヤルティ**クイックタブを選択します。</span><span class="sxs-lookup"><span data-stu-id="31361-139">On the **Price details** page, select the **Royalty** FastTab.</span></span>

<span data-ttu-id="31361-140">![価格の詳細ページのロイヤリティ クイック タブ](./media/royalty-contract-management-price-details.png "価格の詳細ページのロイヤリティ クイック タブ")</span><span class="sxs-lookup"><span data-stu-id="31361-140">![Royalty FastTab on the Price details page](./media/royalty-contract-management-price-details.png "Royalty FastTab on the Price details page")</span></span>

<span data-ttu-id="31361-141">**ロイヤリティ** クイック タブは、明細行に適用される有効な契約コードからのロイヤリティ手数料を示しています。</span><span class="sxs-lookup"><span data-stu-id="31361-141">The **Royalty** FastTab shows the royalty fee from the valid contract code that is applied to a line.</span></span> <span data-ttu-id="31361-142">また、**詳細** クイック タブの **利益見積** にある **ロイヤリティ金額** フィールドは、製品単位あたりのロイヤリティ手数料を指定します。</span><span class="sxs-lookup"><span data-stu-id="31361-142">Additionally, the **Royalty amount** field under **Margin estimation** on the **Detail** FastTab specifies the royalty fee per product unit.</span></span>

> [!NOTE]
> <span data-ttu-id="31361-143">**価格の詳細** ページにアクセスするには、**売掛金勘定パラメーター** ページの **価格** タブの **価格の詳細** クイック タブで、**価格の詳細の有効化** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="31361-143">To access the **Price details** page, on the **Accounts receivable parameters** page, on the **Prices** tab, on the **Price details** FastTab, set the **Enable price details** option to **Yes**.</span></span>

<span data-ttu-id="31361-144">販売注文の請求時に、ロイヤルティ請求が作成されます。</span><span class="sxs-lookup"><span data-stu-id="31361-144">The royalty claim is created when the sales order is invoiced.</span></span>

## <a name="process-claims-and-pass-them-as-payable-to-ap"></a><span data-ttu-id="31361-145">請求を処理し A/R に買掛金として渡す</span><span class="sxs-lookup"><span data-stu-id="31361-145">Process claims and pass them as payable to A/P</span></span>

<span data-ttu-id="31361-146">生成されるロイヤルティ請求は、ライセンサーに対する将来の支払を表します。</span><span class="sxs-lookup"><span data-stu-id="31361-146">Royalty claims that are generated represent future payments to the licensor.</span></span> <span data-ttu-id="31361-147">契約所有者は、関連する期間の請求を累積し、これらの請求を承認することによってライセンサーの中間負債を作成します。</span><span class="sxs-lookup"><span data-stu-id="31361-147">The contract owner cumulates the claims for the relevant period and then creates an interim liability for the licensor by approving those claims.</span></span>

<span data-ttu-id="31361-148">ロイヤルティ契約所有者は、生成された請求を定期的に確認し、会社のポリシーによって要求されているように承認する責任を負っています。</span><span class="sxs-lookup"><span data-stu-id="31361-148">The royalty agreement owner is responsible for periodically reviewing and, as required by the company's policy, approving the claims that are generated.</span></span> <span data-ttu-id="31361-149">請求が承認されると、A/P 管理者は発注請求書として請求を通常の買掛金処理に渡します。</span><span class="sxs-lookup"><span data-stu-id="31361-149">After the claims are approved, the A/P administrator passes them as purchase invoices to the regular payable processing.</span></span>

<span data-ttu-id="31361-150">すべての請求を表示するには、**買掛金管理 \> ブローカーおよびロイヤリティ \> ロイヤルティ請求** を選択します。</span><span class="sxs-lookup"><span data-stu-id="31361-150">To view all the claims, select **Accounts payable \> Broker and royalties \> Royalty claims**.</span></span>

<span data-ttu-id="31361-151">**ロイヤリティ請求** ページの **開始時ロイヤルティ金額** フィールドは、承認および処理された後、仕入先にロイヤルティとして支払われる手数料の金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="31361-151">On the **Royalty claims** page, the **Starting royalty amount** field specifies the fee amount that, after it's approved and processed, will be paid to the vendor as a royalty.</span></span>

<span data-ttu-id="31361-152">ページの **売上** セクションのフィールドは、請求書番号、請求書明細行の正味金額、および数量など、発生元となる販売の請求書に関する詳細を指定することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="31361-152">The fields in the **Sales** section of the page specify the details about the originating sales invoice, such as the invoice number, invoice line net amount, and quantity.</span></span>

<span data-ttu-id="31361-153">時間ベースで請求が生成されると、そのステータスが **計算対象** に設定される点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="31361-153">Note that when a claim is generated on a time basis, its status is set to **To be calculated**.</span></span> <span data-ttu-id="31361-154">このステータスは、ロイヤリティがその時間単位で付与されるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="31361-154">This status is used because the royalty is granted on that time basis.</span></span> <span data-ttu-id="31361-155">請求は、期間の終わりまで、他の請求と共に累積的な計算に含められません。</span><span class="sxs-lookup"><span data-stu-id="31361-155">The claim won't be included, together with other claims, in the cumulative calculation until the end of the period.</span></span>

<span data-ttu-id="31361-156">同じ仕入先の複数の販売注文がある場合、任意の累積効果が考慮されるように請求を再計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31361-156">If there are multiple sales orders for the same vendor, the claims must be recalculated so that any cumulative effect is considered.</span></span> <span data-ttu-id="31361-157">アクション ウィンドウで、**累計**を選択します。</span><span class="sxs-lookup"><span data-stu-id="31361-157">On the Action Pane, select **Cumulate**.</span></span>

<span data-ttu-id="31361-158">**累計**アクションが実行されると、請求金額の見越し計上仕訳帳が転記されます。</span><span class="sxs-lookup"><span data-stu-id="31361-158">When the **Cumulate** action is run, an accrual journal for the claim amounts is posted.</span></span> <span data-ttu-id="31361-159">転記の詳細を表示するには、ロイヤルティ請求の一覧で請求を見つけ、アクション ペインで **ロイヤリティ トランザクション** を選択して見越し計上仕訳帳を表示してアクセスします。</span><span class="sxs-lookup"><span data-stu-id="31361-159">To view the details of the posting, find the claim in the list of royalty claims, and then, on the Action Pane, select **Royalty transactions** to see and access the accrual journal.</span></span>

<span data-ttu-id="31361-160">転記済の伝票は、予定ロイヤルティのロイヤルティ見越勘定が貸方に転記されることと、予想される経費の中間見越ロイヤリティ経費勘定が借方に転記されることを指定します。</span><span class="sxs-lookup"><span data-stu-id="31361-160">The posted voucher specifies that the royalty accrual account is credited for the expected royalty fee, and that the interim accrued royalty expense account is debited for the expected expense.</span></span>

<span data-ttu-id="31361-161">通常の A/P プロセスに請求を移動するためには、A/P 係はロイヤルティ請求を完了していなければなりません。</span><span class="sxs-lookup"><span data-stu-id="31361-161">To move the claims to the regular A/P process, the A/P clerk must complete the royalty claim.</span></span> <span data-ttu-id="31361-162">**ロイヤルティ請求** ページのアクション ウィンドウで **処理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="31361-162">On the **Royalty claims** page, on the Action Pane, select **Process**.</span></span>

<span data-ttu-id="31361-163">次のイベントが発生し、請求のステータスが **完了** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="31361-163">The following events occur, and the claim's status is changed to **Completed**:</span></span>

- <span data-ttu-id="31361-164">ロイヤルティ見越し計上仕訳帳の転記が、見越し買掛金、および経費金額の以前の中間納付を取り消します。</span><span class="sxs-lookup"><span data-stu-id="31361-164">A Royalty accrual journal posting reverses the previous interim amounts on the accrual payable and expense amounts.</span></span>
- <span data-ttu-id="31361-165">ロイヤリティ金額に対する仕入先請求書が作成され、転記されます。</span><span class="sxs-lookup"><span data-stu-id="31361-165">A vendor invoice for the royalty amount is created and posted.</span></span>
- <span data-ttu-id="31361-166">その結果、仕入先の買掛金勘定が貸方に転記され、ロイヤリティ手数料の勘定が借方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="31361-166">As a result, the vendor's payable account is credited, and the royalty fees account is debited.</span></span>

> [!NOTE]
> <span data-ttu-id="31361-167">ロイヤルティの仕入請求書明細行に使用された調達カテゴリに、ロイヤルティ手数料の勘定番号が指定されます。</span><span class="sxs-lookup"><span data-stu-id="31361-167">The account number for royalty fees is specified for the procurement category that is used on the purchase invoice line for the royalty.</span></span> <span data-ttu-id="31361-168">言い換えると、調達カテゴリは、**買掛金勘定パラメーター**ページの**ブローカーとロイヤリティ** タブで設定されます。</span><span class="sxs-lookup"><span data-stu-id="31361-168">That procurement category, in turn, is set on the **Broker and royalty** tab of the **Accounts payable parameters** page.</span></span>

<span data-ttu-id="31361-169">仕入先請求書番号を表示するには、ロイヤルティ請求から **ロイヤルティ トランザクション** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="31361-169">To see the vendor invoice number, open the **Royalty transactions** page from the royalty claim.</span></span>

## <a name="summary"></a><span data-ttu-id="31361-170">集計</span><span class="sxs-lookup"><span data-stu-id="31361-170">Summary</span></span>

<span data-ttu-id="31361-171">ロイヤルティの処理には、うんざりさせられる手動での複数の追跡タスクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="31361-171">The process for handling royalties involves multiple manual tracking tasks that are often tedious.</span></span> <span data-ttu-id="31361-172">ロイヤルティ契約の管理機能はこれらのタスクを自動化することにより、次のプロセスへの移行が容易になります。</span><span class="sxs-lookup"><span data-stu-id="31361-172">By automating those tasks, the royalty contract management feature helps you move through the following process:</span></span>

- <span data-ttu-id="31361-173">正確なロイヤルティ請求の作成</span><span class="sxs-lookup"><span data-stu-id="31361-173">Generating accurate royalty claims</span></span>
- <span data-ttu-id="31361-174">一般会計で予定された買掛金および中間経費の発生</span><span class="sxs-lookup"><span data-stu-id="31361-174">Accruing the expected payables and interim expense in the general ledger</span></span>
- <span data-ttu-id="31361-175">ロイヤルティの期日を迎えた仕入先残高と損益計算書の更新</span><span class="sxs-lookup"><span data-stu-id="31361-175">Updating the vendor balance and the income statement with the royalties that are due</span></span>

<span data-ttu-id="31361-176">このように、この機能は、潜在的なエラーや未払いロイヤルティに対する利息を回避するのに役立ち、会社にとって適切なタイミングのキャッシュ フロー予測に貢献します。</span><span class="sxs-lookup"><span data-stu-id="31361-176">In this way, the feature helps you avoid potential errors and interest on unpaid royalties, and contributes to a timely cash flow forecast for the company.</span></span>
