---
title: "転記の定義"
description: "この記事では、発注書の債務および予算割り当てに対する転記の定義の使用方法を示す例を示します。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 004f3f24ec410d9f0e7d1e7264ec2730b9467410
ms.contentlocale: ja-jp
ms.lasthandoff: 06/29/2017


---

# <a name="posting-definition-examples"></a><span data-ttu-id="cfc0d-103">転記の定義の例</span><span class="sxs-lookup"><span data-stu-id="cfc0d-103">Posting definition examples</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="cfc0d-104">この記事では、発注書の債務および予算割り当てに対する転記の定義の使用方法を示す例を示します。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-104">This article provides examples that show how posting definitions are used for purchase order encumbrances and budget appropriations.</span></span>

<span data-ttu-id="cfc0d-105">このトピックの読み取る前に、転記の定義とトランザクションの転記の定義をよく理解しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-105">Before you read this topic, you should be familiar with posting definitions and transaction posting definitions.</span></span> <span data-ttu-id="cfc0d-106">詳細については、「[転記の定義](posting-definitions.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-106">For information, see [Posting definitions](posting-definitions.md).</span></span> <span data-ttu-id="cfc0d-107">次の例は、**転記の定義**ページで設定できます。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-107">The following examples can be set up on the **Posting definitions** page.</span></span> <span data-ttu-id="cfc0d-108">各例には、次のセクションが含まれています:</span><span class="sxs-lookup"><span data-stu-id="cfc0d-108">Each example contains these sections:</span></span>

-   <span data-ttu-id="cfc0d-109">転記の定義 – 照合基準</span><span class="sxs-lookup"><span data-stu-id="cfc0d-109">Posting definition – Match criteria</span></span>
-   <span data-ttu-id="cfc0d-110">転記の定義 – 生成されたエントリ</span><span class="sxs-lookup"><span data-stu-id="cfc0d-110">Posting definition – Generated entries</span></span>
-   <span data-ttu-id="cfc0d-111">勘定、分析コード値、および金額を含むトランザクション</span><span class="sxs-lookup"><span data-stu-id="cfc0d-111">Transactions with the accounts, dimension values, and amounts</span></span>
-   <span data-ttu-id="cfc0d-112">転記の定義から生成された元帳エントリ</span><span class="sxs-lookup"><span data-stu-id="cfc0d-112">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="cfc0d-113">転記の定義と、トランザクションの勘定と分析コード値について**照合基準**ページで、勘定と分析コード値の間に一致があった場合、転記の定義の**生成されたエントリ** ペインに基づいて、元帳エントリが生成されます。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-113">When a match occurs between the accounts and dimension values in the **Match criteria** pane for the posting definition and the accounts and dimension values on the transaction, ledger entries are generated based on the **Generated entries** pane for the posting definition.</span></span> 
> [!NOTE]
> <span data-ttu-id="cfc0d-114">転記の定義を特定のトランザクション タイプに関連付けるには、**トランザクションの転記の定義**ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-114">To associate a posting definition with a specific transaction type, use the **Transaction posting definitions** page.</span></span> <span data-ttu-id="cfc0d-115">転記の定義をトランザクション タイプに関連付け、**一般会計パラメーター** ページで [**転記の定義の使用**] を選択した後、選択されたトランザクション タイプのすべてのトランザクションでは、転記の定義を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-115">After you associate a posting definition with a transaction type and select **Use posting definitions** on the **General ledger parameters** page, all transactions of the selected transaction type must use posting definitions.</span></span>

## <a name="example-purchase-order-encumbrances"></a><span data-ttu-id="cfc0d-116">例: 発注書の債務</span><span class="sxs-lookup"><span data-stu-id="cfc0d-116">Example: Purchase order encumbrances</span></span>
<span data-ttu-id="cfc0d-117">**総勘定元帳パラメーター** ページの**債務プロセスの有効化**を選択して債務処理を有効にした場合、転記の定義を使用して、引当対象の勘定の総勘定元帳に債務を記録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-117">When you enable encumbrance processing by selecting **Enable encumbrance process** on the **General ledger parameters** page, posting definitions must be used to record encumbrances to the general ledger for any accounts that should be reserved.</span></span> <span data-ttu-id="cfc0d-118">ほとんどの場合、すべての経費勘定は、貸借対照表で引当が行われます。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-118">In most cases, all expense accounts are reserved on the balance sheet.</span></span> 

<span data-ttu-id="cfc0d-119">債務の転記の定義は、**転記の定義**ページの**購買**モジュールに対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-119">Posting definitions for encumbrances are set up for the **Purchasing** module on the **Posting definitions** page.</span></span> <span data-ttu-id="cfc0d-120">その後、**トランザクションの転記の定義**ページの**購買**の領域で、**発注書**のトランザクション タイプを選択して、転記の定義を発注書に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-120">Then, in the **Purchasing** area of the **Transaction posting definitions** page, you can select the **Purchase order** transaction type to associate the posting definition with purchase orders.</span></span> 

<span data-ttu-id="cfc0d-121">発注書の債務のすべての伝票トランザクションは、伝票の一意の分析コードで精算する (借方と貸方が等しくなる必要がある) 必要があります。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-121">All voucher transactions for purchase order encumbrances must balance (that is, debits must equal credits) in each unique dimension on a voucher.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="cfc0d-122">転記の定義 – 照合基準</span><span class="sxs-lookup"><span data-stu-id="cfc0d-122">Posting definition – Match criteria</span></span>

| <span data-ttu-id="cfc0d-123">勘定構造</span><span class="sxs-lookup"><span data-stu-id="cfc0d-123">Account structure</span></span>       | <span data-ttu-id="cfc0d-124">照合勘定番号</span><span class="sxs-lookup"><span data-stu-id="cfc0d-124">Match account number</span></span> | <span data-ttu-id="cfc0d-125">優先順位</span><span class="sxs-lookup"><span data-stu-id="cfc0d-125">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="cfc0d-126">勘定構造 - P&L</span><span class="sxs-lookup"><span data-stu-id="cfc0d-126">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="cfc0d-127">1</span><span class="sxs-lookup"><span data-stu-id="cfc0d-127">1</span></span>        |

<span data-ttu-id="cfc0d-128">* **照合勘定番号**フィールドの空白の値は、定義された勘定構造のすべての照合勘定が一致するルールの一部になります。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-128">*A blank value in the **Match account number** field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="cfc0d-129">転記の定義 – 生成されたエントリ</span><span class="sxs-lookup"><span data-stu-id="cfc0d-129">Posting definition – Generated entries</span></span>

| <span data-ttu-id="cfc0d-130">勘定構造</span><span class="sxs-lookup"><span data-stu-id="cfc0d-130">Account structure</span></span> | <span data-ttu-id="cfc0d-131">生成された勘定番号</span><span class="sxs-lookup"><span data-stu-id="cfc0d-131">Generated account number</span></span>                    | <span data-ttu-id="cfc0d-132">生成された借方/貸方</span><span class="sxs-lookup"><span data-stu-id="cfc0d-132">Generated debit/credit</span></span> |
|-------------------|---------------------------------------------|------------------------|
| <span data-ttu-id="cfc0d-133">残高</span><span class="sxs-lookup"><span data-stu-id="cfc0d-133">Balance</span></span>           | <span data-ttu-id="cfc0d-134">300143 - -(債務口座)</span><span class="sxs-lookup"><span data-stu-id="cfc0d-134">300143 - -(Encumbrance account)</span></span>             | <span data-ttu-id="cfc0d-135">同じ</span><span class="sxs-lookup"><span data-stu-id="cfc0d-135">Same</span></span>                   |
| <span data-ttu-id="cfc0d-136">残高</span><span class="sxs-lookup"><span data-stu-id="cfc0d-136">Balance</span></span>           | <span data-ttu-id="cfc0d-137">300144 - -(債務口座の引当)</span><span class="sxs-lookup"><span data-stu-id="cfc0d-137">300144 - -(Reserve for encumbrance account)</span></span> | <span data-ttu-id="cfc0d-138">バランスをとる</span><span class="sxs-lookup"><span data-stu-id="cfc0d-138">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="cfc0d-139">勘定、分析コード値、および金額を含むトランザクション</span><span class="sxs-lookup"><span data-stu-id="cfc0d-139">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="cfc0d-140">勘定および分析コード値は、購買注文明細行に対して入力する勘定配布から来ているか、または仕入先、品目、カテゴリ、および分析コードのテンプレートの既定の設定に基づいて自動的に生成される分析コードと勘定から来ています。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-140">The accounts and dimension values come either from the accounting distributions that you enter for a purchase order line, or from the accounts and dimensions that are automatically generated based on the default settings for vendors, items, categories, and dimension templates.</span></span>

| <span data-ttu-id="cfc0d-141">口座 + 分析コード</span><span class="sxs-lookup"><span data-stu-id="cfc0d-141">Account + dimensions</span></span>           | <span data-ttu-id="cfc0d-142">デビット</span><span class="sxs-lookup"><span data-stu-id="cfc0d-142">Debit</span></span>  | <span data-ttu-id="cfc0d-143">クレジット</span><span class="sxs-lookup"><span data-stu-id="cfc0d-143">Credit</span></span> | <span data-ttu-id="cfc0d-144">コメント</span><span class="sxs-lookup"><span data-stu-id="cfc0d-144">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="cfc0d-145">606400-OU\_1-OU\_3566-トレーニング</span><span class="sxs-lookup"><span data-stu-id="cfc0d-145">606400-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="cfc0d-146">250.00</span><span class="sxs-lookup"><span data-stu-id="cfc0d-146">250.00</span></span> |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="cfc0d-147">転記の定義から生成された元帳エントリ</span><span class="sxs-lookup"><span data-stu-id="cfc0d-147">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="cfc0d-148">生成された元帳エントリは債務を記録するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-148">Generated ledger entries are created to record the encumbrances.</span></span>

| <span data-ttu-id="cfc0d-149">口座 + 分析コード</span><span class="sxs-lookup"><span data-stu-id="cfc0d-149">Account + dimensions</span></span>           | <span data-ttu-id="cfc0d-150">デビット</span><span class="sxs-lookup"><span data-stu-id="cfc0d-150">Debit</span></span>  | <span data-ttu-id="cfc0d-151">クレジット</span><span class="sxs-lookup"><span data-stu-id="cfc0d-151">Credit</span></span> | <span data-ttu-id="cfc0d-152">コメント</span><span class="sxs-lookup"><span data-stu-id="cfc0d-152">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="cfc0d-153">300143-OU\_1-OU\_3566-トレーニング</span><span class="sxs-lookup"><span data-stu-id="cfc0d-153">300143-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="cfc0d-154">250.00</span><span class="sxs-lookup"><span data-stu-id="cfc0d-154">250.00</span></span> |        |         |
| <span data-ttu-id="cfc0d-155">300144-OU\_1-OU\_3566-トレーニング</span><span class="sxs-lookup"><span data-stu-id="cfc0d-155">300144-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="cfc0d-156">250.00</span><span class="sxs-lookup"><span data-stu-id="cfc0d-156">250.00</span></span> |         |

<span data-ttu-id="cfc0d-157">この例では、勘定構造 - P&L の一部であるいずれかの口座が転記の定義の基準に一致します。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-157">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="cfc0d-158">したがって、606500-OU\_1-OU\_3566-トレーニングが評価されると、生成されたエントリは転記の定義の**生成されたエントリ** ペインで定義された勘定に対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-158">Therefore, when 606500-OU\_1-OU\_3566-Training is evaluated, generated entries are created for the accounts that are defined in the **Generated entries** pane for the posting definition.</span></span>

## <a name="example-budget-appropriations"></a><span data-ttu-id="cfc0d-159">例: 予算割り当て</span><span class="sxs-lookup"><span data-stu-id="cfc0d-159">Example: Budget appropriations</span></span>
<span data-ttu-id="cfc0d-160">**総勘定元帳パラメーター** ページの **予算割り当ての有効化**を選択して予算割り当てを有効にすると、一般会計への予算登録のエントリを記録するためには、転記の定義を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-160">When you enable budget appropriation by selecting **Enable budget appropriation** on the **General ledger parameters** page, posting definitions must be used to record budget register entries to the general ledger.</span></span> <span data-ttu-id="cfc0d-161">予算管理コンフィギュレーションが有効な場合、一般会計に対して、割り当て、変更、転送、プロジェクト、固定資産、および供給と需要予測のエントリの記録をサポートするために、転記の定義とトランザクションの転記の定義を使用できます。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-161">When a budget control configuration is active and is turned on, posting definitions and transaction posting definitions can be used to support the recording of entries for appropriations, revisions, transfers, projects, fixed assets, and supply and demand forecasts to the general ledger.</span></span> 

<span data-ttu-id="cfc0d-162">**元の予算**の予算タイプがあり、有効な割り当てがある予算登録エントリの転記の定義を設定するには、**転記の定義**ページで**予算**モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-162">To set up a posting definition for budget register entries that has a budget type of **Original budget**, and that has appropriations enabled, select the **Budget** module on the **Posting definitions** page.</span></span> <span data-ttu-id="cfc0d-163">その後、**トランザクションの転記の定義**ページの**予算**領域で、予算コードを使用して、転記の定義を**元の予算**の予算タイプを持つ予算登録エントリに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-163">Then, in the **Budget** area of the **Transaction posting definitions** page, you can use budget codes to associate the posting definition with budget register entries that have a budget type of **Original budget**.</span></span> 

<span data-ttu-id="cfc0d-164">予算割り当ておよび転記の定義が有効な場合、予算登録のエントリは予算管理のために、一般会計に記録されます。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-164">When budget appropriations and posting definitions are enabled, the budget register entries are recorded for budget control and in the general ledger.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="cfc0d-165">転記の定義 – 照合基準</span><span class="sxs-lookup"><span data-stu-id="cfc0d-165">Posting definition – Match criteria</span></span>

| <span data-ttu-id="cfc0d-166">勘定構造</span><span class="sxs-lookup"><span data-stu-id="cfc0d-166">Account structure</span></span>       | <span data-ttu-id="cfc0d-167">照合勘定番号</span><span class="sxs-lookup"><span data-stu-id="cfc0d-167">Match account number</span></span> | <span data-ttu-id="cfc0d-168">優先順位</span><span class="sxs-lookup"><span data-stu-id="cfc0d-168">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="cfc0d-169">勘定構造 - P&L</span><span class="sxs-lookup"><span data-stu-id="cfc0d-169">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="cfc0d-170">1</span><span class="sxs-lookup"><span data-stu-id="cfc0d-170">1</span></span>        |

<span data-ttu-id="cfc0d-171">* **照合勘定番号**フィールドの空白の値は、定義された勘定構造のすべての照合勘定が一致するルールの一部になります。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-171">*A blank value in the **Match account number** field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="cfc0d-172">転記の定義 – 生成されたエントリ</span><span class="sxs-lookup"><span data-stu-id="cfc0d-172">Posting definition – Generated entries</span></span>

| <span data-ttu-id="cfc0d-173">勘定構造</span><span class="sxs-lookup"><span data-stu-id="cfc0d-173">Account structure</span></span> | <span data-ttu-id="cfc0d-174">生成された勘定番号</span><span class="sxs-lookup"><span data-stu-id="cfc0d-174">Generated account number</span></span>              | <span data-ttu-id="cfc0d-175">生成された借方/貸方</span><span class="sxs-lookup"><span data-stu-id="cfc0d-175">Generated debit/credit</span></span> |
|-------------------|---------------------------------------|------------------------|
| <span data-ttu-id="cfc0d-176">勘定構造</span><span class="sxs-lookup"><span data-stu-id="cfc0d-176">Account structure</span></span> | <span data-ttu-id="cfc0d-177">300145 - -(見積られた収益口座)</span><span class="sxs-lookup"><span data-stu-id="cfc0d-177">300145 - -(Estimated revenue account)</span></span> | <span data-ttu-id="cfc0d-178">同じ</span><span class="sxs-lookup"><span data-stu-id="cfc0d-178">Same</span></span>                   |
| <span data-ttu-id="cfc0d-179">勘定構造</span><span class="sxs-lookup"><span data-stu-id="cfc0d-179">Account structure</span></span> | <span data-ttu-id="cfc0d-180">300146 - -(割り当て口座)</span><span class="sxs-lookup"><span data-stu-id="cfc0d-180">300146 - -(Appropriation account)</span></span>     | <span data-ttu-id="cfc0d-181">バランスをとる</span><span class="sxs-lookup"><span data-stu-id="cfc0d-181">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="cfc0d-182">勘定、分析コード値、および金額を含むトランザクション</span><span class="sxs-lookup"><span data-stu-id="cfc0d-182">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="cfc0d-183">**予算登録エントリ** ページで、予算勘定項目の勘定、分析コード値、金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-183">You enter the accounts, dimension values, and amounts for the budget account entry on the **Budget register entry** page.</span></span>

| <span data-ttu-id="cfc0d-184">口座 + 分析コード</span><span class="sxs-lookup"><span data-stu-id="cfc0d-184">Account + dimensions</span></span>           | <span data-ttu-id="cfc0d-185">デビット</span><span class="sxs-lookup"><span data-stu-id="cfc0d-185">Debit</span></span> | <span data-ttu-id="cfc0d-186">クレジット</span><span class="sxs-lookup"><span data-stu-id="cfc0d-186">Credit</span></span> | <span data-ttu-id="cfc0d-187">コメント</span><span class="sxs-lookup"><span data-stu-id="cfc0d-187">Comment</span></span> |
|--------------------------------|-------|--------|---------|
| <span data-ttu-id="cfc0d-188">606400-OU\_1-OU\_3566-トレーニング</span><span class="sxs-lookup"><span data-stu-id="cfc0d-188">606400-OU\_1-OU\_3566-Training</span></span> |       | <span data-ttu-id="cfc0d-189">250.00</span><span class="sxs-lookup"><span data-stu-id="cfc0d-189">250.00</span></span> |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="cfc0d-190">転記の定義から生成された元帳エントリ</span><span class="sxs-lookup"><span data-stu-id="cfc0d-190">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="cfc0d-191">生成された元帳エントリは各分析コードの元の予算を記録するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-191">Generated ledger entries are created to record the original budget in each dimension.</span></span>

| <span data-ttu-id="cfc0d-192">口座 + 分析コード</span><span class="sxs-lookup"><span data-stu-id="cfc0d-192">Account + dimensions</span></span>           | <span data-ttu-id="cfc0d-193">デビット</span><span class="sxs-lookup"><span data-stu-id="cfc0d-193">Debit</span></span>  | <span data-ttu-id="cfc0d-194">クレジット</span><span class="sxs-lookup"><span data-stu-id="cfc0d-194">Credit</span></span> | <span data-ttu-id="cfc0d-195">コメント</span><span class="sxs-lookup"><span data-stu-id="cfc0d-195">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="cfc0d-196">300145-OU\_1-OU\_3566-トレーニング</span><span class="sxs-lookup"><span data-stu-id="cfc0d-196">300145-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="cfc0d-197">250.00</span><span class="sxs-lookup"><span data-stu-id="cfc0d-197">250.00</span></span> |         |
| <span data-ttu-id="cfc0d-198">300146-OU\_1-OU\_3566-トレーニング</span><span class="sxs-lookup"><span data-stu-id="cfc0d-198">300146-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="cfc0d-199">250.00</span><span class="sxs-lookup"><span data-stu-id="cfc0d-199">250.00</span></span> |        |         |

<span data-ttu-id="cfc0d-200">この例では、勘定構造 - P&L の一部であるいずれかの口座が転記の定義の基準に一致します。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-200">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="cfc0d-201">したがって、606400-OU\_1-OU\_3566-トレーニングが評価されると、生成された元帳エントリが作成されます。</span><span class="sxs-lookup"><span data-stu-id="cfc0d-201">Therefore, when 606400-OU\_1-OU\_3566-Training is evaluated, the generated ledger entries are created.</span></span>






