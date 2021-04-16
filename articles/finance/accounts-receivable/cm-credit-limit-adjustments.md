---
title: 与信限度額の調整
description: このトピックでは、与信限度額調整の設定および追加方法について説明します。
author: mikefalkner
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: b1669029f28cef924170b47340567af49525e1b7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835367"
---
# <a name="credit-limit-adjustments"></a><span data-ttu-id="c216b-103">与信限度額の調整</span><span class="sxs-lookup"><span data-stu-id="c216b-103">Credit limit adjustments</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c216b-104">与信限度額調整では、単一の顧客、顧客グループ、またはすべての顧客について、転記プロセスを通じて与信限度額と有効期限を更新します。</span><span class="sxs-lookup"><span data-stu-id="c216b-104">Credit limit adjustments let credit managers update the credit limits and expiration dates of a single customer, a group of customers, or all customers through a posting process.</span></span> <span data-ttu-id="c216b-105">与信限度額調整エントリを追加して顧客や顧客の与信グループを更新したり、それらを使用して自動与信限度額を計算したりできます。</span><span class="sxs-lookup"><span data-stu-id="c216b-105">You can add credit limit adjustment entries to update customers and customer credit groups, or you can use them to calculate automatic credit limits.</span></span> <span data-ttu-id="c216b-106">その後、エントリを確認し、ワークフローを通じて承認を受けるために送信して、顧客アカウントに転記できます。</span><span class="sxs-lookup"><span data-stu-id="c216b-106">The entries can then be reviewed, sent for approval through a workflow, and posted to customer accounts.</span></span>

## <a name="set-up-credit-limit-adjustments"></a><span data-ttu-id="c216b-107">与信限度額調整の設定</span><span class="sxs-lookup"><span data-stu-id="c216b-107">Set up credit limit adjustments</span></span>

<span data-ttu-id="c216b-108">**与信限度額調整** ページ (**与信管理 \> 与信限度額調整 \> 与信限度額調整**) で、与信限度額調整仕訳帳にエントリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="c216b-108">You can create entries in the Credit limit adjustment journal on the **Credit limit adjustment** page (**Credit management \> Credit limit adjustments \> Credit limit adjustments**).</span></span>

1. <span data-ttu-id="c216b-109">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c216b-109">Select **New**.</span></span> <span data-ttu-id="c216b-110">与信限度額調整番号を持つ新しいエントリグループが作成されます。</span><span class="sxs-lookup"><span data-stu-id="c216b-110">A new group of entries is created that has a credit limit adjustment number.</span></span>
2. <span data-ttu-id="c216b-111">与信限度額調整タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="c216b-111">Select the credit limit adjustment type:</span></span>

    - <span data-ttu-id="c216b-112">**与信限度額** を選択して、顧客の与信限度額を変更します。</span><span class="sxs-lookup"><span data-stu-id="c216b-112">Select **Credit limit** to change the customer's credit limit.</span></span>
    - <span data-ttu-id="c216b-113">顧客の現在の与信限度額を変更するのではなく、一時的な与信限度額を作成するには、**一時的な与信限度額** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c216b-113">Select **Temporary credit limit** to create a temporary credit limit instead of changing the customer's current credit limit.</span></span> <span data-ttu-id="c216b-114">一時的な与信限度額は、定義された期間顧客の与信限度額よりも優先されます。</span><span class="sxs-lookup"><span data-stu-id="c216b-114">Temporary credit limits override a customer's credit limit for a defined period.</span></span> <span data-ttu-id="c216b-115">その期間が終了した後、顧客の与信限度額が再度使用されます。</span><span class="sxs-lookup"><span data-stu-id="c216b-115">After that period ends, the customer's credit limit is used again.</span></span>
3. <span data-ttu-id="c216b-116">説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="c216b-116">Enter a description.</span></span> 

<span data-ttu-id="c216b-117">**転記済** チェック ボックスがオンになっている場合は、与信限度額が適用されています。</span><span class="sxs-lookup"><span data-stu-id="c216b-117">If the **Posted** check box is selected, the credit limits have been applied.</span></span> <span data-ttu-id="c216b-118">**承認ステータス** フィールドは、仕訳帳のワークフローのステータスを示します。</span><span class="sxs-lookup"><span data-stu-id="c216b-118">The **Approval status** field indicates the workflow status of the journal.</span></span> <span data-ttu-id="c216b-119">ワークフローはオプションです。</span><span class="sxs-lookup"><span data-stu-id="c216b-119">A workflow is optional.</span></span>

### <a name="add-credit-limit-adjustments"></a><span data-ttu-id="c216b-120">与信限度額調整の追加</span><span class="sxs-lookup"><span data-stu-id="c216b-120">Add credit limit adjustments</span></span>

<span data-ttu-id="c216b-121">与信限度額調整を手動で追加するには、**明細行** を選択してから次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c216b-121">To manually add credit limit adjustments, select **Lines**, and then follow these steps.</span></span>

1. <span data-ttu-id="c216b-122">顧客の与信限度額調整を追加するには、**顧客調整** メニューを使用します。</span><span class="sxs-lookup"><span data-stu-id="c216b-122">To add a credit limit adjustment for a customer, use the **Customer adjustments** menu.</span></span> <span data-ttu-id="c216b-123">顧客の与信グループの与信限度額を追加するには、**顧客の与信グループ調整** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c216b-123">To add a credit limit for a customer credit group, select **Customer credit group adjustments**.</span></span>
2. <span data-ttu-id="c216b-124">新しい与信限度額で更新される請求書顧客口座の顧客口座を入力します。</span><span class="sxs-lookup"><span data-stu-id="c216b-124">Enter a customer account for the invoice customer account that should be updated with the new credit limit.</span></span> <span data-ttu-id="c216b-125">手順 1 で **顧客の与信グループ調整** を選択した場合は、顧客の与信グループを入力します。</span><span class="sxs-lookup"><span data-stu-id="c216b-125">If you selected **Customer credit group adjustments** in step 1, enter the customer credit group.</span></span> <span data-ttu-id="c216b-126">同じ仕訳帳明細行に顧客口座と顧客与信グループの両方の ID を入力することはできません。</span><span class="sxs-lookup"><span data-stu-id="c216b-126">You can't enter both a customer account and a customer credit group ID on the same journal line.</span></span>

    <span data-ttu-id="c216b-127">現在の与信限度額が表示されるので、この名前は自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="c216b-127">The current credit limit is shown, and the name automatically appears.</span></span>

3. <span data-ttu-id="c216b-128">与信限度額エントリが転記されるときに、現在の与信限度額を置き換える新しい与信限度額を入力します。</span><span class="sxs-lookup"><span data-stu-id="c216b-128">Enter the new credit limit that should replace the current credit limit when the credit limit entry is posted.</span></span>
4. <span data-ttu-id="c216b-129">顧客の与信限度額の新しい有効期限を定義する日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c216b-129">Enter a date to define the new expiration date for the customer credit limit.</span></span> <span data-ttu-id="c216b-130">与信限度額調整を作成するときは、与信限度額の有効期限を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c216b-130">You must enter a credit limit expiration date when you create a credit limit adjustment.</span></span>

<span data-ttu-id="c216b-131">**承認ステータス** フィールドは、仕訳帳明細行のワークフローのステータスを示します。</span><span class="sxs-lookup"><span data-stu-id="c216b-131">The **Approval status** field indicates the workflow status of the journal line.</span></span>

<span data-ttu-id="c216b-132">与信限度額調整を自動的に生成する場合は、アクション ウィンドウの **生成** メニューを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c216b-132">If you want the credit limit adjustments to be automatically generated, you can use the **Generate** menu on the Action Pane.</span></span>
 
### <a name="add-temporary-credit-limit-adjustments"></a><span data-ttu-id="c216b-133">一時的な与信限度額調整の追加</span><span class="sxs-lookup"><span data-stu-id="c216b-133">Add temporary credit limit adjustments</span></span>

<span data-ttu-id="c216b-134">一時的な与信限度額調整を手動で追加するには、仕訳帳明細行で次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c216b-134">To manually add temporary credit limit adjustments, follow these steps for the journal lines.</span></span>

1. <span data-ttu-id="c216b-135">顧客の与信限度額調整を追加するには、**顧客調整** メニューを使用します。</span><span class="sxs-lookup"><span data-stu-id="c216b-135">To add a credit limit adjustment for a customer, use the **Customer adjustments** menu.</span></span> <span data-ttu-id="c216b-136">顧客の与信グループの与信限度額を追加するには、**顧客の与信グループ調整** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c216b-136">To add a credit limit for a customer credit group, select **Customer credit group adjustments**.</span></span>
2. <span data-ttu-id="c216b-137">新しい与信限度額で更新される請求書顧客口座の顧客口座を入力します。</span><span class="sxs-lookup"><span data-stu-id="c216b-137">Enter a customer account for the invoice customer account that should be updated with the new credit limit.</span></span> <span data-ttu-id="c216b-138">手順 1 で **顧客の与信グループ調整** を選択した場合は、顧客の与信グループを入力します。</span><span class="sxs-lookup"><span data-stu-id="c216b-138">If you selected **Customer credit group adjustments** in step 1, enter the customer credit group.</span></span> <span data-ttu-id="c216b-139">同じ仕訳帳明細行に顧客口座と顧客与信グループの両方の ID を入力することはできません。</span><span class="sxs-lookup"><span data-stu-id="c216b-139">You can't enter both a customer account and a customer credit group ID on the same journal line.</span></span>

    <span data-ttu-id="c216b-140">現在または将来の一時的な与信限度額が既に存在する場合は、現在の一時的な与信限度額と日付範囲が、各一時的な与信限度に対して表示されます。</span><span class="sxs-lookup"><span data-stu-id="c216b-140">If an active or future temporary credit limit already exists, the current temporary credit limit and date ranges appear for each temporary credit limit.</span></span> <span data-ttu-id="c216b-141">名前が自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="c216b-141">The name automatically appears.</span></span>

3. <span data-ttu-id="c216b-142">現在の与信限度額を置き換える新しい与信限度額を入力します。</span><span class="sxs-lookup"><span data-stu-id="c216b-142">Enter the new credit limit that should replace the current credit limit.</span></span>
4. <span data-ttu-id="c216b-143">**新しい開始日** フィールドと **新しい終了日** フィールドで、与信限度額の詳細が有効である場合に期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="c216b-143">In the **New from date** and **New to date** fields, define the period when the advanced credit limit is valid.</span></span> <span data-ttu-id="c216b-144">与信限度額調整仕訳帳を作成するときは、与信限度額の有効期限を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c216b-144">You must enter credit limit expiration dates when you create a credit limit adjustment journal.</span></span>

<span data-ttu-id="c216b-145">**承認ステータス** フィールドは、仕訳帳明細行のワークフローのステータスを示します。</span><span class="sxs-lookup"><span data-stu-id="c216b-145">The **Approval status** field indicates the workflow status of the journal line.</span></span>

## <a name="generate-credit-limit-adjustments"></a><span data-ttu-id="c216b-146">与信限度額調整の生成</span><span class="sxs-lookup"><span data-stu-id="c216b-146">Generate credit limit adjustments</span></span>

<span data-ttu-id="c216b-147">与信限度額を自動的に調整することもできます。</span><span class="sxs-lookup"><span data-stu-id="c216b-147">You can also have credit limits automatically adjusted.</span></span> <span data-ttu-id="c216b-148">アクション ウィンドウの **生成** を選択し、次のオプションのいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="c216b-148">On the Action Pane, select **Generate**, and then select one of the following options:</span></span>

- <span data-ttu-id="c216b-149">既存の顧客から</span><span class="sxs-lookup"><span data-stu-id="c216b-149">From existing customer</span></span>
- <span data-ttu-id="c216b-150">既存の顧客与信グループから</span><span class="sxs-lookup"><span data-stu-id="c216b-150">From existing customer credit group</span></span>
- <span data-ttu-id="c216b-151">自動与信限度額</span><span class="sxs-lookup"><span data-stu-id="c216b-151">Automatic credit limits</span></span>

### <a name="from-existing-customer"></a><span data-ttu-id="c216b-152">既存の顧客から</span><span class="sxs-lookup"><span data-stu-id="c216b-152">From existing customer</span></span>

<span data-ttu-id="c216b-153">既存の顧客から仕訳帳明細行を作成できます。</span><span class="sxs-lookup"><span data-stu-id="c216b-153">You can create journal lines from existing customers.</span></span> <span data-ttu-id="c216b-154">**生成 \> 既存の顧客から** を選択すると、ダイアログ ボックスが表示され、顧客を選択し、新しい制限を計算するための基準を指定できます。</span><span class="sxs-lookup"><span data-stu-id="c216b-154">When you select **Generate \> From existing customer**, a dialog box appears where you can provide criteria for selecting customers and calculating the new limits.</span></span>

1. <span data-ttu-id="c216b-155">与信限度額を加算または減算する調整値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c216b-155">Enter an adjustment value to add or subtract an amount from the credit limit.</span></span> <span data-ttu-id="c216b-156">現在の与信限度額を減少させる場合は負の値を入力し、加算する場合は正の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c216b-156">Enter a negative value to decrease the current credit limit or a positive value to increase it.</span></span>
2. <span data-ttu-id="c216b-157">**値の型** フィールドで、手順 1 で入力した値を使用して新しい与信限度額を計算する方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="c216b-157">In the **Value type** field, select how the value that you entered in step 1 should be used to calculate the new credit limit:</span></span>

    - <span data-ttu-id="c216b-158">与信限度額を金額で変更する場合は、**固定値** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c216b-158">Select **Fixed value** to change the credit limit by an amount.</span></span>
    - <span data-ttu-id="c216b-159">与信限度額をパーセンテージで変更する場合は、**パーセンテージ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c216b-159">Select **Percentage** to change the credit limit by a percentage.</span></span>

3. <span data-ttu-id="c216b-160">計算された与信限度額を丸めるための値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c216b-160">Enter a value that is used to round the calculated credit limit.</span></span> <span data-ttu-id="c216b-161">たとえば、**10.00** と入力して、与信限度額を最も近い 10.00 通貨単位に丸めます。</span><span class="sxs-lookup"><span data-stu-id="c216b-161">For example, enter **10.00** to round the credit limit to the nearest 10.00 currency units.</span></span>
4. <span data-ttu-id="c216b-162">残余を切り上げるか切り下げるかを指定するには、**丸めフォーム** フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="c216b-162">Set the **Rounding form** field to specify whether the remainder should be rounded up or down.</span></span>
5. <span data-ttu-id="c216b-163">日付の調整に使用する手法を選択します。</span><span class="sxs-lookup"><span data-stu-id="c216b-163">Select the method that is used to adjust dates.</span></span>

    - <span data-ttu-id="c216b-164">**絶対** を選択した場合は、与信限度額の日付範囲を定義する日付を入力できます。</span><span class="sxs-lookup"><span data-stu-id="c216b-164">If you select **Absolute**, you can enter dates that define the date range for the credit limits.</span></span>
    - <span data-ttu-id="c216b-165">**相対** を選択した場合は、範囲のオフセット日付を入力できます。</span><span class="sxs-lookup"><span data-stu-id="c216b-165">If you select **Relative**, you can enter offset dates for the range.</span></span> <span data-ttu-id="c216b-166">与信限度額の現在の日付範囲は、オフセットによって調整されます。</span><span class="sxs-lookup"><span data-stu-id="c216b-166">The current date range for the credit limit will be adjusted by the offset.</span></span>

6. <span data-ttu-id="c216b-167">含まれている顧客の一覧をフィルター処理するには、**対象に含めるレコード** クイックタブを使用します。</span><span class="sxs-lookup"><span data-stu-id="c216b-167">Use the **Records to include** FastTab to filter the list of customers that are included.</span></span> <span data-ttu-id="c216b-168">フィルタを含めない場合は、すべての顧客に対して与信限度額エントリが生成されます。</span><span class="sxs-lookup"><span data-stu-id="c216b-168">If you don't include filters, credit limit entries will be generated for all customers.</span></span>
7. <span data-ttu-id="c216b-169">**OK** をクリックして、与信限度額調整エントリを作成します。</span><span class="sxs-lookup"><span data-stu-id="c216b-169">Select **OK** to create the credit limit adjustment entries.</span></span>

### <a name="from-existing-customer-credit-group"></a><span data-ttu-id="c216b-170">既存の顧客与信グループから</span><span class="sxs-lookup"><span data-stu-id="c216b-170">From existing customer credit group</span></span>

<span data-ttu-id="c216b-171">既存の顧客与信グループから仕訳帳明細行を作成できます。</span><span class="sxs-lookup"><span data-stu-id="c216b-171">You can create journal lines from existing customer credit groups.</span></span> <span data-ttu-id="c216b-172">**生成 \> 既存の顧客与信グループから** を選択すると、ダイアログが表示され、顧客与信グループを選択し、新しい制限を計算するための基準を指定できます。</span><span class="sxs-lookup"><span data-stu-id="c216b-172">When you select **Generate \> From existing customer credit group**, a dialog appears where you can provide criteria for selecting customer credit groups and calculating the new limits.</span></span> <span data-ttu-id="c216b-173">基準は、既存の顧客から仕訳帳明細行を作成する際に使用する基準と同じです。</span><span class="sxs-lookup"><span data-stu-id="c216b-173">The criteria are the same criteria that are used to create journal lines from existing customers.</span></span> <span data-ttu-id="c216b-174">前のセクションの手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c216b-174">See the steps in the previous section.</span></span>

### <a name="automatic-credit-limits"></a><span data-ttu-id="c216b-175">自動与信限度額</span><span class="sxs-lookup"><span data-stu-id="c216b-175">Automatic credit limits</span></span>

<span data-ttu-id="c216b-176">顧客の与信限度額を定義および更新するための自動与信限度額を作成できます。</span><span class="sxs-lookup"><span data-stu-id="c216b-176">You can create automatic credit limits to define and update customer credit limits.</span></span> <span data-ttu-id="c216b-177">自動与信限度額は、リスク グループに対してスコアリング グループで使用される特定の値に基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="c216b-177">The automatic credit limits are created for a risk group, and they are based on specific values that are used in the scoring groups.</span></span> <span data-ttu-id="c216b-178">これらの自動与信限度額は、与信限度額エントリを生成するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="c216b-178">You can use these automatic credit limits to generate credit limit entries.</span></span> <span data-ttu-id="c216b-179">顧客が特定のリスク グループに割り当てられており、顧客の与信情報が自動与信限度の基準に一致している場合は、与信限度額調整エントリが作成されます。</span><span class="sxs-lookup"><span data-stu-id="c216b-179">If a customer has been assigned to a specific risk group, and the customer's credit information matches the criteria for an automatic credit limit, a credit limit adjustment entry is created.</span></span>

#### <a name="create-automatic-credit-limits"></a><span data-ttu-id="c216b-180">自動与信限度額の作成</span><span class="sxs-lookup"><span data-stu-id="c216b-180">Create automatic credit limits</span></span>

<span data-ttu-id="c216b-181">与信限度額調整を使用して、自動与信限度額を作成します。</span><span class="sxs-lookup"><span data-stu-id="c216b-181">You create automatic credit limits by using credit limit adjustments.</span></span> <span data-ttu-id="c216b-182">**生成 \> 自動与信限度額** を選択した場合、顧客が割り当てられているリスク グループに基づいて作成される新しい与信限度額に対して有効期限を設定できるダイアログが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c216b-182">When you select **Generate \> Automatic credit limits**, a dialog appears where you can set an expiration date for the new credit limits that will be created based on the risk groups that customers are assigned to.</span></span> <span data-ttu-id="c216b-183">完了したら、**OK** を選択して与信限度額調整明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="c216b-183">When you've finished, select **OK** to create the credit limit adjustment lines.</span></span>

### <a name="post-adjustments"></a><span data-ttu-id="c216b-184">調整の転記</span><span class="sxs-lookup"><span data-stu-id="c216b-184">Post adjustments</span></span>

<span data-ttu-id="c216b-185">与信限度額調整明細行を作成した後、アクション ウィンドウの **転記** ボタンを使用して、エントリを転記し、顧客の与信限度額を更新できます。</span><span class="sxs-lookup"><span data-stu-id="c216b-185">After you've created credit limit adjustment lines, you can use the **Post** button on the Action Pane to post the entries and update the customer credit limits.</span></span> <span data-ttu-id="c216b-186">ただし、ワークフローを設定した場合は、アクション ウィンドウで **ワークフロー \> 送信** を選択して、承認のために仕訳帳を送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c216b-186">However, if you've set up a workflow, you must select **Workflow \> Submit** on the Action Pane to submit the journal for approval.</span></span>

### <a name="credit-limit-adjustments-workflows"></a><span data-ttu-id="c216b-187">与信限度額調整のワークフロー</span><span class="sxs-lookup"><span data-stu-id="c216b-187">Credit limit adjustments workflows</span></span>

<span data-ttu-id="c216b-188">**与信限度額調整** ワークフローは、ワークフローの承認プロセスを使用して与信限度額調整を送信するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="c216b-188">The **Credit limit adjustments** workflows can be used to send credit limit adjustments through a workflow approval process.</span></span> <span data-ttu-id="c216b-189">**与信管理のワークフロー** ページ (**与信管理 \> 設定 \> 与信管理ワークフロー**) で、2つのワークフローを作成できます。</span><span class="sxs-lookup"><span data-stu-id="c216b-189">You can create two workflows on the **Credit management worfklow** page (**Credit management \> Setup \> Credit management worfklow**):</span></span>

- <span data-ttu-id="c216b-190">**与信限度額の調整** – このワークフローは、ヘッダー レベルでエントリを承認するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="c216b-190">**Credit limit adjustments** – This workflow can be used to approve entries at the header level.</span></span>
- <span data-ttu-id="c216b-191">**与信限度額調整** – このワークフローを使用すると、調整エントリを承認して、ワークフローの基準に基づいて別のユーザーがエントリを承認することができます。</span><span class="sxs-lookup"><span data-stu-id="c216b-191">**Credit limit adjustments line** – This workflow can be used to approve the adjustment entries so that the entries can be approved by different people, based on the criteria in the workflow.</span></span>

> [!NOTE]
> <span data-ttu-id="c216b-192">**与信限度額調整** ワークフローを作成するときに、明細行が承認された後に自動的に調整が転記されるように、この設定を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="c216b-192">When you create the **Credit limit adjustments** workflow, you can set it up so that the adjustments are automatically posted after the lines are approved.</span></span> <span data-ttu-id="c216b-193">**仕訳帳の自動転記** タスクをワークフローに含めるだけです。</span><span class="sxs-lookup"><span data-stu-id="c216b-193">Just include the **Post Journal automatically** task in the workflow.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]