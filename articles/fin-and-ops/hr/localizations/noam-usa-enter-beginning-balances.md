---
title: "給与の期首残高を入力します。"
description: "所得コード、控除、福利厚生、および税額の期首残高を入力するための手順を説明します。 この情報は、パートナーが別のシステムから新しい給与実装のデータを移行または転送する場合に役立ちます。"
author: kherr75
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 736eedf270ac08b0bdf9364821f8a7bae981ade9
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---

# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="8c606-104">給与の期首残高を入力します。</span><span class="sxs-lookup"><span data-stu-id="8c606-104">Enter payroll beginning balances</span></span>

[!include[banner](../../includes/banner.md)]

<span data-ttu-id="8c606-105">所得コード、控除、福利厚生、および税額の期首残高を入力するための手順を説明します。</span><span class="sxs-lookup"><span data-stu-id="8c606-105">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="8c606-106">この情報は、パートナーが別のシステムから新しい給与実装のデータを転送する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="8c606-106">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="8c606-107">給与の期首残高を入力を準備する上で、次の情報を確認します。</span><span class="sxs-lookup"><span data-stu-id="8c606-107">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

> * <span data-ttu-id="8c606-108">従業員レコードがシステムに入力され、利用可能となっている</span><span class="sxs-lookup"><span data-stu-id="8c606-108">Employee records are entered and available in the system</span></span>
> * <span data-ttu-id="8c606-109">次のデータを設定し、従業員に割り当てられている</span><span class="sxs-lookup"><span data-stu-id="8c606-109">The following data is set up and assigned to employees:</span></span>

> > * <span data-ttu-id="8c606-110">支払サイクルと支払期間</span><span class="sxs-lookup"><span data-stu-id="8c606-110">Pay cycles and pay periods</span></span>
> > * <span data-ttu-id="8c606-111">所得コード</span><span class="sxs-lookup"><span data-stu-id="8c606-111">Earning codes</span></span>
> > * <span data-ttu-id="8c606-112">税申告</span><span class="sxs-lookup"><span data-stu-id="8c606-112">Taxes</span></span>
> > * <span data-ttu-id="8c606-113">福利厚生と控除</span><span class="sxs-lookup"><span data-stu-id="8c606-113">Benefits and deductions</span></span>

> * <span data-ttu-id="8c606-114">会社は給与の期首残高を設定できる日付が選択している必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c606-114">The company should have chosen a date where payroll beginning balances can be set.</span></span>

> * <span data-ttu-id="8c606-115">レガシ システムからのすべての収益、給付/控除、給付金負担、従業員税、雇用者税、および YTD 金額に関する情報が収集されました。</span><span class="sxs-lookup"><span data-stu-id="8c606-115">Information were gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="8c606-116">期首残高を入力する場合は、データがどの程度詳細になる必要があるかを検討します。</span><span class="sxs-lookup"><span data-stu-id="8c606-116">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="8c606-117">ほとんどの企業では、連結の年度累計金額を 1 つ入力します。</span><span class="sxs-lookup"><span data-stu-id="8c606-117">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="8c606-118">ただし、より詳細な情報が必要な場合、残高は、四半期単位で入力できます。</span><span class="sxs-lookup"><span data-stu-id="8c606-118">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="8c606-119">必要な詳細レベルを決定することにより、作業者ごとに手動支払明細書の数をどれだけ作成する必要があるかが分かります。</span><span class="sxs-lookup"><span data-stu-id="8c606-119">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="8c606-120">1 つの年度累計金額は、各従業員に対して 1 つの手動支払明細書が必要です。</span><span class="sxs-lookup"><span data-stu-id="8c606-120">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="8c606-121">これを実行するには、新しい給与計算システムに入力された金額として、以前のシステムからの最終支払明細から年度累計金額を使用します。</span><span class="sxs-lookup"><span data-stu-id="8c606-121">To do this use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="8c606-122">次の例では、取得コード、手当/控除、および税額を含む従業員の給与の期首残高を入力する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="8c606-122">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="8c606-123">現実の例では、収益コード、給付控除、給付金負担、従業員税、雇用者税ごとに明細行品目があり、入力された金額を年度累計金額とします。</span><span class="sxs-lookup"><span data-stu-id="8c606-123">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="8c606-124">そのコードと金額の一覧を使用して、給与計算に対して期首残高を引き出すために無効にした会計で、手動の所得と支払明細書を作成する手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8c606-124">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span>  <span data-ttu-id="8c606-125">この期首残高の支払明細書を総勘定元帳に転記されないようにするためにな、会計を無効にします。</span><span class="sxs-lookup"><span data-stu-id="8c606-125">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="8c606-126">これはレガシ システムで行われ、総勘定元帳で期首残高を設定すると、新しいシステムに引き継がれます。</span><span class="sxs-lookup"><span data-stu-id="8c606-126">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="8c606-127">A.</span><span class="sxs-lookup"><span data-stu-id="8c606-127">A.</span></span> <span data-ttu-id="8c606-128">給与の期首残高に使用される収益のコードを設定する方法</span><span class="sxs-lookup"><span data-stu-id="8c606-128">How to set up earnings codes to be used on payroll beginning balances</span></span>
<span data-ttu-id="8c606-129">給与の期首残高を入力すると、使用する収益コードの「所得明細書レートの編集を許可する」オプションが有効になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8c606-129">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="8c606-130">これにより、レガシ システムからの金額を手動で入力できるようになります。</span><span class="sxs-lookup"><span data-stu-id="8c606-130">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="8c606-131">B.</span><span class="sxs-lookup"><span data-stu-id="8c606-131">B.</span></span> <span data-ttu-id="8c606-132">従業員が期首残高を持つための所得明細書を作成する</span><span class="sxs-lookup"><span data-stu-id="8c606-132">Create earnings statement for an employee to have a beginning balance</span></span>
<span data-ttu-id="8c606-133">この手順では、レガシ システムの最終支払期間に各作業員の収益明細書が手動で作成され、新しい給与管理システムに取得明細行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="8c606-133">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="8c606-134">収益コードと YTD の金額と時間に対して 1 行入力します。</span><span class="sxs-lookup"><span data-stu-id="8c606-134">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="8c606-135">手順を次の例に示します。</span><span class="sxs-lookup"><span data-stu-id="8c606-135">The sample steps are as follows:</span></span>

1. <span data-ttu-id="8c606-136">[**すべての所得明細書**] ページを開き、[**新規**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8c606-136">Open the **All earnings statements** page and click **New**.</span></span>  

<span data-ttu-id="8c606-137">次の内容を入力します。</span><span class="sxs-lookup"><span data-stu-id="8c606-137">Enter the following:</span></span> 

| <span data-ttu-id="8c606-138">フィールド</span><span class="sxs-lookup"><span data-stu-id="8c606-138">Field</span></span>      | <span data-ttu-id="8c606-139">先頭値</span><span class="sxs-lookup"><span data-stu-id="8c606-139">Value</span></span>                 |
|------------|-----------------------|
| <span data-ttu-id="8c606-140">ワーカー</span><span class="sxs-lookup"><span data-stu-id="8c606-140">Worker</span></span>     | <span data-ttu-id="8c606-141">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="8c606-141">Michael Redmond</span></span>       |
| <span data-ttu-id="8c606-142">支払サイクル</span><span class="sxs-lookup"><span data-stu-id="8c606-142">Pay cycle</span></span>  | <span data-ttu-id="8c606-143">sm</span><span class="sxs-lookup"><span data-stu-id="8c606-143">sm</span></span>                    |
| <span data-ttu-id="8c606-144">支払期間</span><span class="sxs-lookup"><span data-stu-id="8c606-144">Pay period</span></span> | <span data-ttu-id="8c606-145">6/16/2017 - 6/30/2017</span><span class="sxs-lookup"><span data-stu-id="8c606-145">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="8c606-146">[**所得明細行**] タブで、次を入力します。</span><span class="sxs-lookup"><span data-stu-id="8c606-146">In the **Earnings statement line** tab, enter the following:</span></span>

<span data-ttu-id="8c606-147">行 1: [**所得明細行**] タブ</span><span class="sxs-lookup"><span data-stu-id="8c606-147">Line 1: **Earning statement line** tab</span></span>

| <span data-ttu-id="8c606-148">フィールド</span><span class="sxs-lookup"><span data-stu-id="8c606-148">Field</span></span>            | <span data-ttu-id="8c606-149">先頭値</span><span class="sxs-lookup"><span data-stu-id="8c606-149">Value</span></span>       |
|------------------|-------------|
| <span data-ttu-id="8c606-150">所得コード</span><span class="sxs-lookup"><span data-stu-id="8c606-150">Earnings code</span></span>    | <span data-ttu-id="8c606-151">通常の支払</span><span class="sxs-lookup"><span data-stu-id="8c606-151">Regular pay</span></span> |
| <span data-ttu-id="8c606-152">件数</span><span class="sxs-lookup"><span data-stu-id="8c606-152">Quantity</span></span>         | <span data-ttu-id="8c606-153">1.00</span><span class="sxs-lookup"><span data-stu-id="8c606-153">1.00</span></span>        |
| <span data-ttu-id="8c606-154">平均</span><span class="sxs-lookup"><span data-stu-id="8c606-154">Rage</span></span>             | <span data-ttu-id="8c606-155">30,000</span><span class="sxs-lookup"><span data-stu-id="8c606-155">30,000</span></span>      |
| <span data-ttu-id="8c606-156">[行の詳細] タブ</span><span class="sxs-lookup"><span data-stu-id="8c606-156">Line details tab</span></span> |             |
| <span data-ttu-id="8c606-157">手動</span><span class="sxs-lookup"><span data-stu-id="8c606-157">Manual</span></span>           | <span data-ttu-id="8c606-158">(マーク済)</span><span class="sxs-lookup"><span data-stu-id="8c606-158">(marked)</span></span>    |

<span data-ttu-id="8c606-159">行 2: [**所得明細行**] タブ</span><span class="sxs-lookup"><span data-stu-id="8c606-159">Line 2: **Earning statement line** tab</span></span>

| <span data-ttu-id="8c606-160">フィールド</span><span class="sxs-lookup"><span data-stu-id="8c606-160">Field</span></span>            | <span data-ttu-id="8c606-161">先頭値</span><span class="sxs-lookup"><span data-stu-id="8c606-161">Value</span></span>    |
|------------------|----------|
| <span data-ttu-id="8c606-162">所得コード</span><span class="sxs-lookup"><span data-stu-id="8c606-162">Earnings code</span></span>    | <span data-ttu-id="8c606-163">賞与</span><span class="sxs-lookup"><span data-stu-id="8c606-163">Bonus</span></span>    |
| <span data-ttu-id="8c606-164">件数</span><span class="sxs-lookup"><span data-stu-id="8c606-164">Quantity</span></span>         | <span data-ttu-id="8c606-165">1.0000</span><span class="sxs-lookup"><span data-stu-id="8c606-165">1.0000</span></span>   |
| <span data-ttu-id="8c606-166">率</span><span class="sxs-lookup"><span data-stu-id="8c606-166">Rate</span></span>             | <span data-ttu-id="8c606-167">4250.00</span><span class="sxs-lookup"><span data-stu-id="8c606-167">4250.00</span></span>  |
| <span data-ttu-id="8c606-168">[行の詳細] タブ</span><span class="sxs-lookup"><span data-stu-id="8c606-168">Line details tab</span></span> |          |
| <span data-ttu-id="8c606-169">手動</span><span class="sxs-lookup"><span data-stu-id="8c606-169">Manual</span></span>           | <span data-ttu-id="8c606-170">(マーク済)</span><span class="sxs-lookup"><span data-stu-id="8c606-170">(marked)</span></span> |

<span data-ttu-id="8c606-171">行 3: [**所得明細行**] タブ</span><span class="sxs-lookup"><span data-stu-id="8c606-171">Line 3: **Earning statement line** tab</span></span>

| <span data-ttu-id="8c606-172">フィールド</span><span class="sxs-lookup"><span data-stu-id="8c606-172">Field</span></span>           | <span data-ttu-id="8c606-173">先頭値</span><span class="sxs-lookup"><span data-stu-id="8c606-173">Value</span></span>      |
|-----------------|------------|
| <span data-ttu-id="8c606-174">所得コード</span><span class="sxs-lookup"><span data-stu-id="8c606-174">Earnings code</span></span>   | <span data-ttu-id="8c606-175">コミッション</span><span class="sxs-lookup"><span data-stu-id="8c606-175">Commission</span></span> |
| <span data-ttu-id="8c606-176">件数</span><span class="sxs-lookup"><span data-stu-id="8c606-176">Quantity</span></span>        | <span data-ttu-id="8c606-177">1.0000</span><span class="sxs-lookup"><span data-stu-id="8c606-177">1.0000</span></span>     |
| <span data-ttu-id="8c606-178">率</span><span class="sxs-lookup"><span data-stu-id="8c606-178">Rate</span></span>            | <span data-ttu-id="8c606-179">!,299.00</span><span class="sxs-lookup"><span data-stu-id="8c606-179">!,299.00</span></span>   |
| <span data-ttu-id="8c606-180">率</span><span class="sxs-lookup"><span data-stu-id="8c606-180">Rate</span></span>            | <span data-ttu-id="8c606-181">1,299.00</span><span class="sxs-lookup"><span data-stu-id="8c606-181">1,299.00</span></span>   |
| <span data-ttu-id="8c606-182">[行の詳細] タブ</span><span class="sxs-lookup"><span data-stu-id="8c606-182">Line detail tab</span></span> |            |
| <span data-ttu-id="8c606-183">手動</span><span class="sxs-lookup"><span data-stu-id="8c606-183">Manual</span></span>          | <span data-ttu-id="8c606-184">(マーク済)</span><span class="sxs-lookup"><span data-stu-id="8c606-184">(Marked)</span></span>   |

> [!NOTE]
> <span data-ttu-id="8c606-185">各明細行の [**明細書行の詳細**] タブにある [**手動**] スライダーを [**はい**] に設定することは、各作業員の給与の期首残高を設定するのに重要です。</span><span class="sxs-lookup"><span data-stu-id="8c606-185">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="8c606-186">[**アクション**] ウィンドウの [**収益明細書のリリース**] USA-FED-ER-FICA をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8c606-186">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>

4. <span data-ttu-id="8c606-187">[**アクション**] ウィンドウの [**支払明細書**] をクリックし、[**支払明細書の生成**] ページを開き、以下を設定します。</span><span class="sxs-lookup"><span data-stu-id="8c606-187">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

| <span data-ttu-id="8c606-188">フィールド</span><span class="sxs-lookup"><span data-stu-id="8c606-188">Field</span></span>              | <span data-ttu-id="8c606-189">先頭値</span><span class="sxs-lookup"><span data-stu-id="8c606-189">Value</span></span>     |
|--------------------|-----------|
| <span data-ttu-id="8c606-190">支払期日</span><span class="sxs-lookup"><span data-stu-id="8c606-190">Payment date</span></span>       | <span data-ttu-id="8c606-191">6/30/2017</span><span class="sxs-lookup"><span data-stu-id="8c606-191">6/30/2017</span></span> |
| <span data-ttu-id="8c606-192">支払実行タイプ</span><span class="sxs-lookup"><span data-stu-id="8c606-192">Payment run type</span></span>   | <span data-ttu-id="8c606-193">手動</span><span class="sxs-lookup"><span data-stu-id="8c606-193">Manual</span></span>    |
| <span data-ttu-id="8c606-194">会計の無効化</span><span class="sxs-lookup"><span data-stu-id="8c606-194">Disable accounting</span></span> |   <span data-ttu-id="8c606-195">有</span><span class="sxs-lookup"><span data-stu-id="8c606-195">Yes</span></span>     |

> [!NOTE] 
> <span data-ttu-id="8c606-196">これは、支払実行タイプが手動であり、支払実行の会計を無効にする場合にのみ使用可能です。</span><span class="sxs-lookup"><span data-stu-id="8c606-196">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

<span data-ttu-id="8c606-197">[**OK**] をクリックし、[**Infolog**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c606-197">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="8c606-198">なぜ [会計の無効化] スライダーを、支払明細書を生成する場合に [はい] に設定する必要があるか。</span><span class="sxs-lookup"><span data-stu-id="8c606-198">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>
<span data-ttu-id="8c606-199">スライダーを [**はい**] と設定することにより、明細行が支払明細書から総勘定元帳に配分されなくなります。</span><span class="sxs-lookup"><span data-stu-id="8c606-199">Setting the slider to **Yes** prevents lines in the pay statement from being districuted to General ledger.</span></span> <span data-ttu-id="8c606-200">レガシー システムからの勘定残高が入力されたときに、総勘定元帳の金額が以前より更新されていました。</span><span class="sxs-lookup"><span data-stu-id="8c606-200">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="8c606-201">給与計算の開始時残高を入力すると、前年度の情報を含むレポートを生成することができます。また、給付と税金の限度額を特定することもできます。</span><span class="sxs-lookup"><span data-stu-id="8c606-201">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>   

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="8c606-202">C.</span><span class="sxs-lookup"><span data-stu-id="8c606-202">C.</span></span> <span data-ttu-id="8c606-203">従業員への支払明細書の生成</span><span class="sxs-lookup"><span data-stu-id="8c606-203">Create pay statements for employees</span></span>
<span data-ttu-id="8c606-204">期首残高がある支払明細書を生成した後、支払明細書に、給与データが正確に反映されているかを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c606-204">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="8c606-205">福利厚生と税の情報を手動で更新し、以前の給与システムで値を一致させる必要もあります。</span><span class="sxs-lookup"><span data-stu-id="8c606-205">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="8c606-206">前の給与システムからの金額と現在の支払明細書の金額が一致していることが確認された後に、支払明細書を確定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c606-206">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="8c606-207">[**すべての支払明細書**] ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="8c606-207">Open the **All pay statements** page.</span></span>

2. <span data-ttu-id="8c606-208">最後に生成された Michael Redmond の支払明細書の強調表示</span><span class="sxs-lookup"><span data-stu-id="8c606-208">Highlight the last generated pay statement for Michael Redmond</span></span>

3. <span data-ttu-id="8c606-209">[**編集**] をクリックし、[**支払明細書**] ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="8c606-209">Click **Edit** to open the **Pay statement** page.</span></span>

4. <span data-ttu-id="8c606-210">[**給付金控除**] タブを開き、次を入力します。</span><span class="sxs-lookup"><span data-stu-id="8c606-210">Open the **Benefit deductions** tab and enter the following:</span></span>

| <span data-ttu-id="8c606-211">フィールド</span><span class="sxs-lookup"><span data-stu-id="8c606-211">Field</span></span>                           | <span data-ttu-id="8c606-212">先頭値</span><span class="sxs-lookup"><span data-stu-id="8c606-212">Value</span></span>            |
|---------------------------------|------------------|
| <span data-ttu-id="8c606-213">福利厚生</span><span class="sxs-lookup"><span data-stu-id="8c606-213">Benefit</span></span>                         | <span data-ttu-id="8c606-214">控除額</span><span class="sxs-lookup"><span data-stu-id="8c606-214">Deduction amount</span></span> |
| <span data-ttu-id="8c606-215">401K</span><span class="sxs-lookup"><span data-stu-id="8c606-215">401K</span></span> | <span data-ttu-id="8c606-216">参加</span><span class="sxs-lookup"><span data-stu-id="8c606-216">Participate</span></span>              | <span data-ttu-id="8c606-217">3000.00</span><span class="sxs-lookup"><span data-stu-id="8c606-217">3000.00</span></span>          |
| <span data-ttu-id="8c606-218">歯科保険</span><span class="sxs-lookup"><span data-stu-id="8c606-218">Dental</span></span> | <span data-ttu-id="8c606-219">SubSp</span><span class="sxs-lookup"><span data-stu-id="8c606-219">SubSp</span></span>                  | <span data-ttu-id="8c606-220">495.00</span><span class="sxs-lookup"><span data-stu-id="8c606-220">495.00</span></span>           |
| <span data-ttu-id="8c606-221">扶養者ケア支出</span><span class="sxs-lookup"><span data-stu-id="8c606-221">Dep care spending</span></span> | <span data-ttu-id="8c606-222">参加</span><span class="sxs-lookup"><span data-stu-id="8c606-222">Participate</span></span> | <span data-ttu-id="8c606-223">2500.00</span><span class="sxs-lookup"><span data-stu-id="8c606-223">2500.00</span></span>          |
| <span data-ttu-id="8c606-224">ビジョン</span><span class="sxs-lookup"><span data-stu-id="8c606-224">Vision</span></span> | <span data-ttu-id="8c606-225">SupSp</span><span class="sxs-lookup"><span data-stu-id="8c606-225">SupSp</span></span>                  | <span data-ttu-id="8c606-226">500.00</span><span class="sxs-lookup"><span data-stu-id="8c606-226">500.00</span></span>           |

5. <span data-ttu-id="8c606-227">[**給付金負担**] タブで次を入力します。</span><span class="sxs-lookup"><span data-stu-id="8c606-227">In the **Benefit contributions** tab and enter the following:</span></span>

| <span data-ttu-id="8c606-228">フィールド</span><span class="sxs-lookup"><span data-stu-id="8c606-228">Field</span></span>              | <span data-ttu-id="8c606-229">先頭値</span><span class="sxs-lookup"><span data-stu-id="8c606-229">Value</span></span>               |
|--------------------|---------------------|
| <span data-ttu-id="8c606-230">福利厚生</span><span class="sxs-lookup"><span data-stu-id="8c606-230">Benefit</span></span>            | <span data-ttu-id="8c606-231">負担額</span><span class="sxs-lookup"><span data-stu-id="8c606-231">Contribution amount</span></span> |
| <span data-ttu-id="8c606-232">401K</span><span class="sxs-lookup"><span data-stu-id="8c606-232">401K</span></span> | <span data-ttu-id="8c606-233">参加</span><span class="sxs-lookup"><span data-stu-id="8c606-233">Participate</span></span> | <span data-ttu-id="8c606-234">3000,00</span><span class="sxs-lookup"><span data-stu-id="8c606-234">3000,00</span></span>             |
| <span data-ttu-id="8c606-235">歯科保険</span><span class="sxs-lookup"><span data-stu-id="8c606-235">Dental</span></span> | <span data-ttu-id="8c606-236">SubSp</span><span class="sxs-lookup"><span data-stu-id="8c606-236">SubSp</span></span>     | <span data-ttu-id="8c606-237">495.00</span><span class="sxs-lookup"><span data-stu-id="8c606-237">495.00</span></span>              |
| <span data-ttu-id="8c606-238">ビジョン</span><span class="sxs-lookup"><span data-stu-id="8c606-238">Vision</span></span> | <span data-ttu-id="8c606-239">SubSp</span><span class="sxs-lookup"><span data-stu-id="8c606-239">SubSp</span></span>     | <span data-ttu-id="8c606-240">500.00</span><span class="sxs-lookup"><span data-stu-id="8c606-240">500.00</span></span>              |

6. <span data-ttu-id="8c606-241">[**税額控除**] タブで次を入力します。</span><span class="sxs-lookup"><span data-stu-id="8c606-241">In the **Tax deductions** tab, enter the following:</span></span>

| <span data-ttu-id="8c606-242">フィールド</span><span class="sxs-lookup"><span data-stu-id="8c606-242">Field</span></span>           | <span data-ttu-id="8c606-243">先頭値</span><span class="sxs-lookup"><span data-stu-id="8c606-243">Value</span></span>            |
|-----------------|------------------|
| <span data-ttu-id="8c606-244">税コード</span><span class="sxs-lookup"><span data-stu-id="8c606-244">Tax code</span></span>        | <span data-ttu-id="8c606-245">控除額</span><span class="sxs-lookup"><span data-stu-id="8c606-245">Deduction amount</span></span> |
| <span data-ttu-id="8c606-246">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="8c606-246">USA-FED-ER-FICA</span></span> | <span data-ttu-id="8c606-247">1600.00</span><span class="sxs-lookup"><span data-stu-id="8c606-247">1600.00</span></span>          |
| <span data-ttu-id="8c606-248">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="8c606-248">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="8c606-249">825.75</span><span class="sxs-lookup"><span data-stu-id="8c606-249">825.75</span></span>           |

7. <span data-ttu-id="8c606-250">[**税負担**] タブで次を入力します。</span><span class="sxs-lookup"><span data-stu-id="8c606-250">In the **Tax contributions** tab enter the following:</span></span>

8. <span data-ttu-id="8c606-251">[**計算**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8c606-251">Click **Calculate**.</span></span>
> [!IMPORTANT] 
> <span data-ttu-id="8c606-252">作業者のレガシ システムの YTD と一致している支払明細書の合計を検証します。</span><span class="sxs-lookup"><span data-stu-id="8c606-252">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="8c606-253">次の手順で終了処理を保留にし、すべての支払明細書の集計を全体的に検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c606-253">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="8c606-254">検証されたら、すべての支払明細書を実行し、確定します。</span><span class="sxs-lookup"><span data-stu-id="8c606-254">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="8c606-255">必要に応じて、毎年の前四半期に、同じ手順を四半期単位で行うことができます。</span><span class="sxs-lookup"><span data-stu-id="8c606-255">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="8c606-256">お客様が、レガシ システムにアクセスせずに、四半期ごとのデータを表示する必要がある場合にのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="8c606-256">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="8c606-257">従業員の期首残高を間違って入力した場合</span><span class="sxs-lookup"><span data-stu-id="8c606-257">If you make a mistake Entering Beginning Balances for an Employee</span></span>
<span data-ttu-id="8c606-258">トランザクションを取消し、再入力することは可能です。</span><span class="sxs-lookup"><span data-stu-id="8c606-258">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="8c606-259">トランザクションを取り消すには、[**すべての支払明細書**] ページで次の手順を完了するのみです。</span><span class="sxs-lookup"><span data-stu-id="8c606-259">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="8c606-260">[**取消**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8c606-260">Click **Reverse**.</span></span>

2. <span data-ttu-id="8c606-261">[**はい**] をクリックするのは、「この支払明細書を相殺するために取消支払明細書が作成されます。</span><span class="sxs-lookup"><span data-stu-id="8c606-261">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="8c606-262">支払明細書を編集することもできません。</span><span class="sxs-lookup"><span data-stu-id="8c606-262">Neither pay statement can be edited.</span></span> <span data-ttu-id="8c606-263">この支払明細書を取り消しますか」</span><span class="sxs-lookup"><span data-stu-id="8c606-263">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="8c606-264">というメッセージが表示されたときです。</span><span class="sxs-lookup"><span data-stu-id="8c606-264">displays.</span></span> 

<span data-ttu-id="8c606-265">支払明細書を取り消した後、前に作成した損益計算書から新しい支払明細書を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="8c606-265">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="8c606-266">新しい支払明細書を生成する前に、損益計算書に誤った行を修正してから、正しい金額の新しい支払明細書を生成します。</span><span class="sxs-lookup"><span data-stu-id="8c606-266">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 

