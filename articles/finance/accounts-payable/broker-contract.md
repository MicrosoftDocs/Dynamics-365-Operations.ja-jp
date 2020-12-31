---
title: ブローカー契約管理
description: このトピックでは、構成する管理タスクを自動化することによるブローカー契約管理について説明します。
author: t-benebo
manager: AnnBe
ms.date: 08/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: MCRBrokerContractManagement, MCRCustCategory, MCRCustCategoryHierarchy, PdsRebateAgreementLineInfoPart, MCRRoyaltyTable
audience: IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 307d1e3b5d7e9e24b0ba8fd4e923189bb08dca42
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409469"
---
# <a name="broker-contract-management"></a><span data-ttu-id="5e8be-103">ブローカー契約管理</span><span class="sxs-lookup"><span data-stu-id="5e8be-103">Broker contract management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e8be-104">ブローカー契約管理により、企業は、ブローカーに支払う手数料の管理、追跡、支払に関連するタスクを自動化することにより、仲介契約を効率的に管理できます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-104">Broker contract management helps companies better manage their brokerage agreements by automating tasks that are involved in administering, tracking, and paying the fees that are due to brokers.</span></span>

<span data-ttu-id="5e8be-105">ここでは、ブローカー手数料を処理するための標準的なプロセスの概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="5e8be-105">This topic provides a broad overview of the typical process for handling broker fees:</span></span>

- <span data-ttu-id="5e8be-106">取り決めブローカー契約の詳細を登録する</span><span class="sxs-lookup"><span data-stu-id="5e8be-106">Registering details of the negotiated broker contract</span></span>
- <span data-ttu-id="5e8be-107">継続的な販売を通して交渉された契約を実行し、ブローカー請求を生成する</span><span class="sxs-lookup"><span data-stu-id="5e8be-107">Running the negotiated contracts through ongoing sales and generating broker claims</span></span>
- <span data-ttu-id="5e8be-108">生成された請求を承認し、支払のために買掛金勘定 (A/P) に渡せるようにする</span><span class="sxs-lookup"><span data-stu-id="5e8be-108">Approving the generated claims, so that they can be passed on to Accounts payable (A/P) for payment</span></span>
- <span data-ttu-id="5e8be-109">部分請求承認と差分会計の状況を処理する</span><span class="sxs-lookup"><span data-stu-id="5e8be-109">Handling situations for partial claim approval and differential accounting</span></span>

## <a name="audience-and-purpose"></a><span data-ttu-id="5e8be-110">対象者および目的</span><span class="sxs-lookup"><span data-stu-id="5e8be-110">Audience and purpose</span></span>

<span data-ttu-id="5e8be-111">このトピックの情報は、以下の触接を持つ、セールス マネージャー、会計マネージャー、A/P マネージャーなどの立場にいる、エンタープライズの会社での業務の意思決定者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="5e8be-111">The information in this topic is intended for business decision makers in enterprise companies, in capacities such as sales manager, accounting manager, and A/P manager, who have the following responsibilities:</span></span>

- <span data-ttu-id="5e8be-112">ブローカーとの契約を交渉する</span><span class="sxs-lookup"><span data-stu-id="5e8be-112">Negotiating contracts with brokers</span></span>
- <span data-ttu-id="5e8be-113">ブローカー請求を処理し、手数料の支払を行うスタッフの管理</span><span class="sxs-lookup"><span data-stu-id="5e8be-113">Managing staff that processes broker claims and makes fee payments</span></span>

<span data-ttu-id="5e8be-114">これらのロールのユーザーは、以下の目標を達成する方法を求めています:</span><span class="sxs-lookup"><span data-stu-id="5e8be-114">People in these roles are looking for ways to achieve these goals:</span></span>

- <span data-ttu-id="5e8be-115">ブローカー契約とその状況の各種の定義に柔軟に対応します。</span><span class="sxs-lookup"><span data-stu-id="5e8be-115">Flexibly accommodate various definitions of broker contracts and their conditions.</span></span>
- <span data-ttu-id="5e8be-116">管理の負担、およびブローカー請求の追跡と処理に関連付けられるエラーを減らします。</span><span class="sxs-lookup"><span data-stu-id="5e8be-116">Reduce the administrative burden and errors that are associated with tracking and processing broker claims.</span></span>
- <span data-ttu-id="5e8be-117">将来の買掛金の見越計上によりキャッシュフロー予測の精度を高めます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-117">Improve cash flow forecasts by accruing for future payables.</span></span>

## <a name="broker-contract"></a><span data-ttu-id="5e8be-118">ブローカー契約</span><span class="sxs-lookup"><span data-stu-id="5e8be-118">Broker contract</span></span>

<span data-ttu-id="5e8be-119">ブローカー契約は、ブローカーとの契約のレコードです。</span><span class="sxs-lookup"><span data-stu-id="5e8be-119">A broker contract is a record of an agreement with a broker.</span></span> <span data-ttu-id="5e8be-120">事前に設定された売上目標の達成と引き換えに仲介企業が金銭的報酬を受け取るすることを認める交渉済み条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="5e8be-120">It specifies the negotiated terms and conditions under which the brokerage company qualifies for a monetary reward in return for achieving preset sales targets.</span></span>

<span data-ttu-id="5e8be-121">ブローカー契約は、**ブローカー契約** ページで登録されます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-121">Broker contracts are registered on the **Broker contracts** page.</span></span> <span data-ttu-id="5e8be-122">**ブローカー契約** ページを開くには、**買掛金勘定** \> **ブローカーおよびロイヤルティ** \> **ブローカー契約** を選びます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-122">To open the **Broker contracts** page, select **Accounts payable** \> **Broker and royalties** \> **Broker contracts**.</span></span>


<span data-ttu-id="5e8be-123">![ブローカー請求ページ](./media/broker-contract-management-contract-page.png "ブローカー請求ページ")</span><span class="sxs-lookup"><span data-stu-id="5e8be-123">![Broker claims page](./media/broker-contract-management-contract-page.png "Broker claims page")</span></span>

<span data-ttu-id="5e8be-124">契約には、ブローカー手数料を支払う当事者 (製品を購入する顧客または販売会社) に関する取り決め条件が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5e8be-124">The contract includes a negotiated condition about who will incur in the broker fee (the customer that buys the product or the selling company).</span></span> <span data-ttu-id="5e8be-125">この条件は、**諸費用コード** ページで設定されます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-125">This condition is set up on the associated **Charges codes** page.</span></span>

<span data-ttu-id="5e8be-126">**契約の詳細** セクションには、仲介の対象となる条件と品目が示されます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-126">The **Contract details** section shows the conditions and the item that qualifies for brokerage.</span></span> <span data-ttu-id="5e8be-127">売上目標の達成に対してブローカーが受け取る金銭的報酬は、**分割** に表示されます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-127">The monetary reward that the broker will receive for achieving the sales objective is shown under **Break**.</span></span>

<span data-ttu-id="5e8be-128">**ブローカー手数料** 請求金額の設定は、顧客がブローカー サービスの手数料を負担しないことを示します。</span><span class="sxs-lookup"><span data-stu-id="5e8be-128">The setup of the **Broker Fees** charge indicates that the customer won't incur the fee for the broker services.</span></span> <span data-ttu-id="5e8be-129">代わりに、販売会社が販売経費としてブローカー手数料を負担します。</span><span class="sxs-lookup"><span data-stu-id="5e8be-129">Instead, the selling company will incur the broker fee as a sales expense.</span></span>


> [!NOTE]
> <span data-ttu-id="5e8be-130">契約に、顧客がブローカー サービスの手数料を負担すると規定されている場合、**借方** セクションの **タイプ** フィールドが **顧客/仕入先** に設定されるように、関連付けられている雑費を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e8be-130">If a contract stipulates that the customer will incur the fee for the broker services, the associated charge must be set up so that the **Type** field in the **Debit** section is set to **Customer/Vendor**.</span></span> <span data-ttu-id="5e8be-131">この場合は、会社はまず、顧客から手数料の支払を受け取り、ブローカーに負債を支払います。</span><span class="sxs-lookup"><span data-stu-id="5e8be-131">In this case, the company first receives the fee payment from the customer and then pays its liability to the broker.</span></span> <span data-ttu-id="5e8be-132">販売の経費としてブローカー手数料を負担する販売会社である場合、**借方** および **貸方** セクションの両方の **タイプ** フィールドが **勘定科目** に設定されるように、関連付けられている雑費を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e8be-132">If it is the selling company that will incur the broker fee as a sales expense, then the associated charge must be set up so that the **Type** field both in the **Debit** and **Credit** sections is set to **Ledger account**.</span></span> 

<span data-ttu-id="5e8be-133">借方勘定は、損益計算書の中間経費を受け取ります。貸方勘定は、請求金額が転記されたときからブローカー請求が承認され、請求書の転記の結果として実際の買掛金に移動されたときまで請求金額 (手数料) をホストする中間負債勘定です。</span><span class="sxs-lookup"><span data-stu-id="5e8be-133">The debit account receives the intermediary expenses on the income statement, and the credit account is an interim liability account that hosts the charge (fee) amount from the time when the charge is posted to the time when the broker claim is approved and moved to the real payable as a result of invoice posting.</span></span>

<span data-ttu-id="5e8be-134">ブローカー契約の **契約の詳細** セクションには、仲介の対象となる条件と品目が示されます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-134">The **Contract details** section of the broker contract shows the conditions and the item that qualifies for brokerage.</span></span> <span data-ttu-id="5e8be-135">売上目標の達成に対してブローカーが受け取る金銭的報酬は、**分割** に表示されます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-135">The monetary reward that the broker will receive for achieving the sales objective is shown under **Break**.</span></span>

<span data-ttu-id="5e8be-136">条件に一致する販売注文に適用するには、契約の **ステータス** が **承認済** でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="5e8be-136">The contract **Status** has to be **Approved** to be applied to sales orders that meet its conditions.</span></span>

## <a name="sell-products-that-qualify-for-a-broker-commission-and-generate-a-claim"></a><span data-ttu-id="5e8be-137">ブローカー コミッションの対象となり、請求を生成する製品を販売します。</span><span class="sxs-lookup"><span data-stu-id="5e8be-137">Sell products that qualify for a broker commission and generate a claim</span></span>

<span data-ttu-id="5e8be-138">ブローカー契約の条件を満たす明細行を持つ販売注文を作成する場合、**販売注文** ページで **販売注文明細行** \> **表示** \> **ブローカー コミッション** の順に選択して関連する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="5e8be-138">When you create a sales order that has lines that fulfill the requirements of the broker contract, you can view the related information on the **Sales order** page by selecting **Sales order line** \> **View** \> **Broker commissions**.</span></span>

<span data-ttu-id="5e8be-139">ブローカー手数料の見越計上は費用として処理されるため、販売注文から標準雑費ページを開いてブローカー コミッションにアクセスすることもできます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-139">Because broker fee accruals are handled as a charge, you can also access the broker commission by opening the standard charges page from the sales order.</span></span> <span data-ttu-id="5e8be-140">注文明細行を選択し、**販売注文明細行**\>**財務**\>**雑費の管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5e8be-140">Select the order line, and then select **Sales order line** \> **Financials** \> **Manage charges**.</span></span>

<span data-ttu-id="5e8be-141">販売注文の請求書を転記するとき、通常の売上請求書のトランザクションだけでなく、次の転記が行われます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-141">When you post the invoice for the sales order, in addition to the regular sales invoice transactions, the following postings occur:</span></span>

- <span data-ttu-id="5e8be-142">請求明細行のブローカー請求が生成されます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-142">The broker claim is generated for the invoice line.</span></span>
- <span data-ttu-id="5e8be-143">ブローカー手数料を表す未収費用は、必要に応じて、中間負債および経費勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-143">The accrued charge that represents the broker fee is posted to the interim liability and expense accounts, as appropriate.</span></span>

<span data-ttu-id="5e8be-144">売上請求書仕訳帳に関連付けられている伝票トランザクションで、未収ブローカー手数料の転記を表示できます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-144">The accrued broker fee posting can be viewed on the voucher transactions associated with the sales invoice journal.</span></span>

## <a name="review-and-process-claims"></a><span data-ttu-id="5e8be-145">請求を確認および処理する</span><span class="sxs-lookup"><span data-stu-id="5e8be-145">Review and process claims</span></span>

<span data-ttu-id="5e8be-146">請求が完全または部分的に承認されると、転記が A/P ポリシーによりサポートされている場合、仕入先請求書が作成されて天気されます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-146">After claims are either fully or partially approved, the vendor invoice is created and posted, if posting is supported by the A/P policy.</span></span> <span data-ttu-id="5e8be-147">これにより、仕入先請求の貸方は、通常の買掛金の処理に渡されます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-147">In this way, the vendor credit is passed to the regular payable processing.</span></span>

<span data-ttu-id="5e8be-148">すべての請求は、**ブローカー請求** ページで表示できます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-148">You can view all the claims on the **Broker claims** page.</span></span> <span data-ttu-id="5e8be-149">手数料ごとに、**修飾** フィールドは、承認された後に仲介サービスのベンダーに支払われる手数料の金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="5e8be-149">For each fee, the **Qualified** field specifies the amount of the fee that, after it's approved, will be paid to vendor of brokerage services.</span></span>

<span data-ttu-id="5e8be-150">![ブローカー請求ページ](./media/broker-contract-management-contract-page.png "ブローカー請求ページ")</span><span class="sxs-lookup"><span data-stu-id="5e8be-150">![Broker claims page](./media/broker-contract-management-contract-page.png "Broker claims page")</span></span>

<span data-ttu-id="5e8be-151">ページの下部セクションのフィールドは、請求書番号、請求書明細行の正味金額、および関連付けられている顧客トランザクションなど、発生元となる販売の請求書に関する詳細を指定することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="5e8be-151">Note that the fields in the lower section of the page specify details about the originating sales invoice, such as the invoice number, invoice line net amount, and associated customer transactions.</span></span>

<span data-ttu-id="5e8be-152">請求を承認するには、**マーク** 列で、明細行のチェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="5e8be-152">To approve a claim, in the **Mark** column, select the check box for the line.</span></span> <span data-ttu-id="5e8be-153">アクション ウィンドウで、**承認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5e8be-153">Then, on the Action Pane, select **Approve**.</span></span>

<span data-ttu-id="5e8be-154">承認の結果として、次のイベントが発生します。</span><span class="sxs-lookup"><span data-stu-id="5e8be-154">As a result of the approval, the following events will occur:</span></span>

- <span data-ttu-id="5e8be-155">経費計上仕訳帳の転記が、見越負債勘定および見越経費勘定の両方の以前の中間納付を取り消します。</span><span class="sxs-lookup"><span data-stu-id="5e8be-155">An Expense journal posting has reversed the previous interim amount on both the accrual liability account and the accrual expense account.</span></span>
- <span data-ttu-id="5e8be-156">承認済ブローカー手数料の金額のブローカー要求 (仕入先) の請求書が作成されています。</span><span class="sxs-lookup"><span data-stu-id="5e8be-156">A broker claim (vendor) invoice for the approved broker fee amount has been created.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5e8be-157">請求書承認プロセスの一部として自動的に、または手動で、ブローカー請求書の請求書を転記できます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-157">A broker claim invoice can be posted either automatically as part of the claim approval process or manually.</span></span> <span data-ttu-id="5e8be-158">**買掛金勘定パラメーター** ページの **ブローカーとロイヤリティ** タブの **手動転記** フィールドは、転記の動作を制御するポリシーを指定します。</span><span class="sxs-lookup"><span data-stu-id="5e8be-158">The **Manual posting** field on the **Broker and royalty** tab of the **Accounts payable parameters** page specifies the policy that controls the posting behavior.</span></span>

- <span data-ttu-id="5e8be-159">ブローカー請求請求の転記の結果として、経費勘定が借方に転記されており、仕入先の買掛金勘定が貸方に転記されています。</span><span class="sxs-lookup"><span data-stu-id="5e8be-159">As a result of posting the broker claim invoice, the expense account has been debited, and the vendor payable account has been credited.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5e8be-160">発注書の経費転記の購買支出が設定されている場合に、調達カテゴリの経費勘定番号が指定されます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-160">The expense account number is specified for the procurement category when purchase expenditure for expense posting is set up for purchase orders.</span></span> <span data-ttu-id="5e8be-161">調達カテゴリ自体は、**買掛金勘定パラメーター** ページの **ブローカーとロイヤリティ** タブで定義されます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-161">The procurement category itself is defined on the **Broker and royalty** tab of the **Accounts payable parameters** page.</span></span>
    
<span data-ttu-id="5e8be-162">**ブローカー請求** ページで、請求書に関連付けれている転記とドキュメント、ブローカーに作成された仕入先請求書番号を確認できます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-162">On the **Broker claims** page, you can review the postings and documents associated with the claim, a vendor invoice number that was created for the broker.</span></span> <span data-ttu-id="5e8be-163">仕入先請求書が転記された場合 (自動または手動で) **請求書** タブの **日付** および **トランザクション通貨での金額** 適切な値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-163">If the vendor invoice was posted (automatically or manually), on the **Invoices** tab, the **Date** and **Amount in transaction currency** fields contain the appropiate values.</span></span> <span data-ttu-id="5e8be-164">請求書がまだ保留中の場合は、これらのフィールドは空白になります。</span><span class="sxs-lookup"><span data-stu-id="5e8be-164">If the invoice is still pending, those fields are blank.</span></span>    

<span data-ttu-id="5e8be-165">請求明細行の **承認済** フィールドに **見込み** フィールドと同じ金額が含まれていて、**差額** フィールドに 0 が含まれる場合、請求が未決済の問題がないため、閉じることができることを意味します。</span><span class="sxs-lookup"><span data-stu-id="5e8be-165">If the **Approved** field for the claim line contains the same amount as the **Qualified** field, whereas the **Difference** field contains 0, it means that the claim has no unsettled issues and can now be closed.</span></span>

## <a name="partially-process-claims"></a><span data-ttu-id="5e8be-166">請求の部分処理</span><span class="sxs-lookup"><span data-stu-id="5e8be-166">Partially process claims</span></span>

<span data-ttu-id="5e8be-167">顧客が販売注文の一部の単位を返品した場合、ブローカーは返品された数量に関連する手数料を得る資格を失った可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5e8be-167">If a customer returns some units of a sales order, the broker might no longer qualify for the fee that is related to the returned quantity.</span></span> <span data-ttu-id="5e8be-168">この場合、一部の金額の 2 つ目の請求を承認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e8be-168">In this case, the second claim for the partial amount must be approved.</span></span> <span data-ttu-id="5e8be-169">**買掛金管理** \> **ブローカーおよびロイヤリティ** \> **ブローカー請求** を選択し、請求を選択します。</span><span class="sxs-lookup"><span data-stu-id="5e8be-169">Select **Accounts payable** \> **Broker and royalties** \> **Broker claims**, and select the claim.</span></span> <span data-ttu-id="5e8be-170">**承認** フィールドに、合計数量から返品単位を引いた数を入力します。</span><span class="sxs-lookup"><span data-stu-id="5e8be-170">In the **Approving** field, enter the total quantity minus the returned units.</span></span> <span data-ttu-id="5e8be-171">アクション ウィンドウで、**承認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5e8be-171">Then, on the Action Pane, select **Approve**.</span></span>

<span data-ttu-id="5e8be-172">![請求の部分処理](./media/broker-contract-management-process-claim.png "請求の部分処理")</span><span class="sxs-lookup"><span data-stu-id="5e8be-172">![Partially processing a claim](./media/broker-contract-management-process-claim.png "Partially processing a claim")</span></span>

<span data-ttu-id="5e8be-173">**承認済** フィールドの値と **修飾** フィールドの値の間に違いがある場合、**差額** フィールドに記録されます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-173">If there is a difference between the value in the **Approved** field and the value in the **Qualified** field, it is recorded in the **Difference** field.</span></span> <span data-ttu-id="5e8be-174">これらの値は、請求がまだ未決済であることと、請求が終了と見なされる前に差額を処理する必要があることを示しています。</span><span class="sxs-lookup"><span data-stu-id="5e8be-174">These values indicate that the claim is still outstanding, and that the difference must be handled before the claim can be considered closed.</span></span>

<span data-ttu-id="5e8be-175">差額は、未決済の請求明細行を選択し、アクション ウィンドウで **終了** をクリックして処理される必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e8be-175">The difference must be handled selecting the unsettled claim line, and then, on the Action Pane, clicking **Close**.</span></span>

<span data-ttu-id="5e8be-176">システムは、請求にはまだ未払単位の数があることを識別し、差額を説明する理由コードを入力するようにユーザーに求めます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-176">The system identifies that the claim still has an outstanding number of units and prompts the user to enter the reason code that explains the difference.</span></span>

<span data-ttu-id="5e8be-177">請求を閉じた後は、次のイベントが発生します。</span><span class="sxs-lookup"><span data-stu-id="5e8be-177">After closing the claim, the following events occur:</span></span>

- <span data-ttu-id="5e8be-178">経費計上仕訳帳の転記が、見越経費勘定の以前の中間納付を取り消します。</span><span class="sxs-lookup"><span data-stu-id="5e8be-178">An expense journal posting has reversed the previous interim amount on the accrual expense account</span></span>
- <span data-ttu-id="5e8be-179">同じ転記が、見越負債勘定の以前の中間納付を取り消します。</span><span class="sxs-lookup"><span data-stu-id="5e8be-179">The same posting reversed the previous interim amount on the accrual liability account</span></span>

<span data-ttu-id="5e8be-180">**差異** タブの下の明細行は、支払いの承認が取り消されたブローカー手数料の金額を示しています。</span><span class="sxs-lookup"><span data-stu-id="5e8be-180">The line under the **Differentials** tab specifies the broker fee amount that was disapproved for payout.</span></span>

<span data-ttu-id="5e8be-181">顧客ではなく会社がブローカー手数料を支払うシナリオの場合、手数料の過剰支払または過少支払に関連付けられている利益または損失を損益計算書で考慮する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="5e8be-181">In the scenario where your company, not the customer, pays the broker fee, profit or loss that is associated with the overpayment or underpayment of a fee doesn't have to be accounted for the income statement.</span></span> <span data-ttu-id="5e8be-182">この場は、差額仕訳は差額の明細行に関連付けられません。</span><span class="sxs-lookup"><span data-stu-id="5e8be-182">In this case, no differential journal will be associated with the differential line.</span></span> 

<span data-ttu-id="5e8be-183">顧客がブローカー手数料を支払う手数料シナリオで差額を処理する場合、システムが請求決算で差分仕訳を転記されることがわかります。</span><span class="sxs-lookup"><span data-stu-id="5e8be-183">If you were handling differences in a fee scenario where the customer pays the broker fee, you would notice that the system posts a differential journal at claim closing.</span></span> <span data-ttu-id="5e8be-184">この仕訳は、ブローカー手数料損金処理勘定を借方/貸方に登録し、中間負債勘定を借方/貸方に登録します。</span><span class="sxs-lookup"><span data-stu-id="5e8be-184">This journal debits/credits the broker fee write-off account and credits/debits the interim liability account.</span></span> 

> [!NOTE]
> <span data-ttu-id="5e8be-185">損金処理経費勘定番号は、**差異の理由** ページの **主勘定** フィールドで、特定の理由コードにより指定されます。</span><span class="sxs-lookup"><span data-stu-id="5e8be-185">The write-off expense account number is specified in the **Main account** field for a specific reason code on the **Differential reasons** page.</span></span>

