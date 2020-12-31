---
title: 転記の定義の例
description: この記事では、発注書の債務および予算割り当てに対する転記の定義の使用方法を示す例を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 301f15f1d7d8f0e10bbaf2546fcf727aff284624
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445073"
---
# <a name="posting-definition-examples"></a><span data-ttu-id="b57e2-103">転記の定義の例</span><span class="sxs-lookup"><span data-stu-id="b57e2-103">Posting definition examples</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b57e2-104">この記事では、発注書の債務および予算割り当てに対する転記の定義の使用方法を示す例を示します。</span><span class="sxs-lookup"><span data-stu-id="b57e2-104">This article provides examples that show how posting definitions are used for purchase order encumbrances and budget appropriations.</span></span>

<span data-ttu-id="b57e2-105">このトピックの読み取る前に、転記の定義とトランザクションの転記の定義をよく理解しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="b57e2-105">Before you read this topic, you should be familiar with posting definitions and transaction posting definitions.</span></span> <span data-ttu-id="b57e2-106">詳細については、「[転記の定義](posting-definitions.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b57e2-106">For information, see [Posting definitions](posting-definitions.md).</span></span> <span data-ttu-id="b57e2-107">次の例は、**転記の定義** ページで設定できます。</span><span class="sxs-lookup"><span data-stu-id="b57e2-107">The following examples can be set up on the **Posting definitions** page.</span></span> <span data-ttu-id="b57e2-108">各例には、次のセクションが含まれています:</span><span class="sxs-lookup"><span data-stu-id="b57e2-108">Each example contains these sections:</span></span>

-   <span data-ttu-id="b57e2-109">転記の定義 – 照合基準</span><span class="sxs-lookup"><span data-stu-id="b57e2-109">Posting definition – Match criteria</span></span>
-   <span data-ttu-id="b57e2-110">転記の定義 – 生成されたエントリ</span><span class="sxs-lookup"><span data-stu-id="b57e2-110">Posting definition – Generated entries</span></span>
-   <span data-ttu-id="b57e2-111">勘定、分析コード値、および金額を含むトランザクション</span><span class="sxs-lookup"><span data-stu-id="b57e2-111">Transactions with the accounts, dimension values, and amounts</span></span>
-   <span data-ttu-id="b57e2-112">転記の定義から生成された元帳エントリ</span><span class="sxs-lookup"><span data-stu-id="b57e2-112">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="b57e2-113">転記の定義と、トランザクションの勘定と分析コード値について **照合基準** ページで、勘定と分析コード値の間に一致があった場合、転記の定義の **生成されたエントリ** ペインに基づいて、元帳エントリが生成されます。</span><span class="sxs-lookup"><span data-stu-id="b57e2-113">When a match occurs between the accounts and dimension values in the **Match criteria** pane for the posting definition and the accounts and dimension values on the transaction, ledger entries are generated based on the **Generated entries** pane for the posting definition.</span></span> 
> [!NOTE]
> <span data-ttu-id="b57e2-114">転記の定義を特定のトランザクション タイプに関連付けるには、**トランザクションの転記の定義** ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="b57e2-114">To associate a posting definition with a specific transaction type, use the **Transaction posting definitions** page.</span></span> <span data-ttu-id="b57e2-115">転記の定義をトランザクション タイプに関連付け、**一般会計パラメーター** ページで **転記の定義の使用** を選択した後、選択されたトランザクション タイプのすべてのトランザクションでは、転記の定義を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b57e2-115">After you associate a posting definition with a transaction type and select **Use posting definitions** on the **General ledger parameters** page, all transactions of the selected transaction type must use posting definitions.</span></span>

## <a name="example-purchase-order-encumbrances"></a><span data-ttu-id="b57e2-116">例: 発注書の債務</span><span class="sxs-lookup"><span data-stu-id="b57e2-116">Example: Purchase order encumbrances</span></span>
<span data-ttu-id="b57e2-117">**総勘定元帳パラメーター** ページの **債務プロセスの有効化** を選択して債務処理を有効にした場合、転記の定義を使用して、引当対象の勘定の総勘定元帳に債務を記録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b57e2-117">When you enable encumbrance processing by selecting **Enable encumbrance process** on the **General ledger parameters** page, posting definitions must be used to record encumbrances to the general ledger for any accounts that should be reserved.</span></span> <span data-ttu-id="b57e2-118">ほとんどの場合、すべての経費勘定は、貸借対照表で引当が行われます。</span><span class="sxs-lookup"><span data-stu-id="b57e2-118">In most cases, all expense accounts are reserved on the balance sheet.</span></span> 

<span data-ttu-id="b57e2-119">債務の転記の定義は、**転記の定義** ページの **購買** モジュールに対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="b57e2-119">Posting definitions for encumbrances are set up for the **Purchasing** module on the **Posting definitions** page.</span></span> <span data-ttu-id="b57e2-120">その後、**トランザクションの転記の定義** ページの **購買** の領域で、**発注書** のトランザクション タイプを選択して、転記の定義を発注書に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="b57e2-120">Then, in the **Purchasing** area of the **Transaction posting definitions** page, you can select the **Purchase order** transaction type to associate the posting definition with purchase orders.</span></span> 

<span data-ttu-id="b57e2-121">発注書の債務のすべての伝票トランザクションは、伝票の一意の分析コードで精算する (借方と貸方が等しくなる必要がある) 必要があります。</span><span class="sxs-lookup"><span data-stu-id="b57e2-121">All voucher transactions for purchase order encumbrances must balance (that is, debits must equal credits) in each unique dimension on a voucher.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="b57e2-122">転記の定義 – 照合基準</span><span class="sxs-lookup"><span data-stu-id="b57e2-122">Posting definition – Match criteria</span></span>

| <span data-ttu-id="b57e2-123">勘定構造</span><span class="sxs-lookup"><span data-stu-id="b57e2-123">Account structure</span></span>       | <span data-ttu-id="b57e2-124">照合勘定番号</span><span class="sxs-lookup"><span data-stu-id="b57e2-124">Match account number</span></span> | <span data-ttu-id="b57e2-125">優先順位</span><span class="sxs-lookup"><span data-stu-id="b57e2-125">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="b57e2-126">勘定構造 - P&L</span><span class="sxs-lookup"><span data-stu-id="b57e2-126">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="b57e2-127">1</span><span class="sxs-lookup"><span data-stu-id="b57e2-127">1</span></span>        |

<span data-ttu-id="b57e2-128"><em>\**照合勘定番号</em>* フィールドの空白の値は、定義された勘定構造のすべての照合勘定が一致するルールの一部になります。</span><span class="sxs-lookup"><span data-stu-id="b57e2-128"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="b57e2-129">転記の定義 – 生成されたエントリ</span><span class="sxs-lookup"><span data-stu-id="b57e2-129">Posting definition – Generated entries</span></span>

| <span data-ttu-id="b57e2-130">勘定構造</span><span class="sxs-lookup"><span data-stu-id="b57e2-130">Account structure</span></span> | <span data-ttu-id="b57e2-131">生成された勘定番号</span><span class="sxs-lookup"><span data-stu-id="b57e2-131">Generated account number</span></span>                    | <span data-ttu-id="b57e2-132">生成された借方/貸方</span><span class="sxs-lookup"><span data-stu-id="b57e2-132">Generated debit/credit</span></span> |
|-------------------|---------------------------------------------|------------------------|
| <span data-ttu-id="b57e2-133">残高</span><span class="sxs-lookup"><span data-stu-id="b57e2-133">Balance</span></span>           | <span data-ttu-id="b57e2-134">300143 - -(債務口座)</span><span class="sxs-lookup"><span data-stu-id="b57e2-134">300143 - -(Encumbrance account)</span></span>             | <span data-ttu-id="b57e2-135">同じ</span><span class="sxs-lookup"><span data-stu-id="b57e2-135">Same</span></span>                   |
| <span data-ttu-id="b57e2-136">残高</span><span class="sxs-lookup"><span data-stu-id="b57e2-136">Balance</span></span>           | <span data-ttu-id="b57e2-137">300144 - -(債務口座の引当)</span><span class="sxs-lookup"><span data-stu-id="b57e2-137">300144 - -(Reserve for encumbrance account)</span></span> | <span data-ttu-id="b57e2-138">バランスをとる</span><span class="sxs-lookup"><span data-stu-id="b57e2-138">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="b57e2-139">勘定、分析コード値、および金額を含むトランザクション</span><span class="sxs-lookup"><span data-stu-id="b57e2-139">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="b57e2-140">勘定および分析コード値は、購買注文明細行に対して入力する勘定配布から来ているか、または仕入先、品目、カテゴリ、および分析コードのテンプレートの既定の設定に基づいて自動的に生成される分析コードと勘定から来ています。</span><span class="sxs-lookup"><span data-stu-id="b57e2-140">The accounts and dimension values come either from the accounting distributions that you enter for a purchase order line, or from the accounts and dimensions that are automatically generated based on the default settings for vendors, items, categories, and dimension templates.</span></span>

| <span data-ttu-id="b57e2-141">口座 + 分析コード</span><span class="sxs-lookup"><span data-stu-id="b57e2-141">Account + dimensions</span></span>           | <span data-ttu-id="b57e2-142">デビット</span><span class="sxs-lookup"><span data-stu-id="b57e2-142">Debit</span></span>  | <span data-ttu-id="b57e2-143">クレジット</span><span class="sxs-lookup"><span data-stu-id="b57e2-143">Credit</span></span> | <span data-ttu-id="b57e2-144">コメント</span><span class="sxs-lookup"><span data-stu-id="b57e2-144">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="b57e2-145">606400-OU\_1-OU\_3566-トレーニング</span><span class="sxs-lookup"><span data-stu-id="b57e2-145">606400-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="b57e2-146">250.00</span><span class="sxs-lookup"><span data-stu-id="b57e2-146">250.00</span></span> |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="b57e2-147">転記の定義から生成された元帳エントリ</span><span class="sxs-lookup"><span data-stu-id="b57e2-147">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="b57e2-148">生成された元帳エントリは債務を記録するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="b57e2-148">Generated ledger entries are created to record the encumbrances.</span></span>

| <span data-ttu-id="b57e2-149">口座 + 分析コード</span><span class="sxs-lookup"><span data-stu-id="b57e2-149">Account + dimensions</span></span>           | <span data-ttu-id="b57e2-150">デビット</span><span class="sxs-lookup"><span data-stu-id="b57e2-150">Debit</span></span>  | <span data-ttu-id="b57e2-151">クレジット</span><span class="sxs-lookup"><span data-stu-id="b57e2-151">Credit</span></span> | <span data-ttu-id="b57e2-152">コメント</span><span class="sxs-lookup"><span data-stu-id="b57e2-152">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="b57e2-153">300143-OU\_1-OU\_3566-トレーニング</span><span class="sxs-lookup"><span data-stu-id="b57e2-153">300143-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="b57e2-154">250.00</span><span class="sxs-lookup"><span data-stu-id="b57e2-154">250.00</span></span> |        |         |
| <span data-ttu-id="b57e2-155">300144-OU\_1-OU\_3566-トレーニング</span><span class="sxs-lookup"><span data-stu-id="b57e2-155">300144-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="b57e2-156">250.00</span><span class="sxs-lookup"><span data-stu-id="b57e2-156">250.00</span></span> |         |

<span data-ttu-id="b57e2-157">この例では、勘定構造 - P&L の一部であるいずれかの口座が転記の定義の基準に一致します。</span><span class="sxs-lookup"><span data-stu-id="b57e2-157">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="b57e2-158">したがって、606500-OU\_1-OU\_3566-トレーニングが評価されると、生成されたエントリは転記の定義の **生成されたエントリ** ペインで定義された勘定に対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="b57e2-158">Therefore, when 606500-OU\_1-OU\_3566-Training is evaluated, generated entries are created for the accounts that are defined in the **Generated entries** pane for the posting definition.</span></span>

## <a name="example-budget-appropriations"></a><span data-ttu-id="b57e2-159">例: 予算割り当て</span><span class="sxs-lookup"><span data-stu-id="b57e2-159">Example: Budget appropriations</span></span>
<span data-ttu-id="b57e2-160">**総勘定元帳パラメーター** ページの **予算割り当ての有効化** を選択して予算割り当てを有効にすると、一般会計への予算登録のエントリを記録するためには、転記の定義を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b57e2-160">When you enable budget appropriation by selecting **Enable budget appropriation** on the **General ledger parameters** page, posting definitions must be used to record budget register entries to the general ledger.</span></span> <span data-ttu-id="b57e2-161">予算管理コンフィギュレーションが有効な場合、一般会計に対して、割り当て、変更、転送、プロジェクト、固定資産、および供給と需要予測のエントリの記録をサポートするために、転記の定義とトランザクションの転記の定義を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b57e2-161">When a budget control configuration is active and is turned on, posting definitions and transaction posting definitions can be used to support the recording of entries for appropriations, revisions, transfers, projects, fixed assets, and supply and demand forecasts to the general ledger.</span></span> 

<span data-ttu-id="b57e2-162">**元の予算** の予算タイプがあり、有効な割り当てがある予算登録エントリの転記の定義を設定するには、**転記の定義** ページで **予算** モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="b57e2-162">To set up a posting definition for budget register entries that has a budget type of **Original budget**, and that has appropriations enabled, select the **Budget** module on the **Posting definitions** page.</span></span> <span data-ttu-id="b57e2-163">その後、**トランザクションの転記の定義** ページの **予算** 領域で、予算コードを使用して、転記の定義を **元の予算** の予算タイプを持つ予算登録エントリに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="b57e2-163">Then, in the **Budget** area of the **Transaction posting definitions** page, you can use budget codes to associate the posting definition with budget register entries that have a budget type of **Original budget**.</span></span> 

<span data-ttu-id="b57e2-164">予算割り当ておよび転記の定義が有効な場合、予算登録のエントリは予算管理のために、一般会計に記録されます。</span><span class="sxs-lookup"><span data-stu-id="b57e2-164">When budget appropriations and posting definitions are enabled, the budget register entries are recorded for budget control and in the general ledger.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="b57e2-165">転記の定義 – 照合基準</span><span class="sxs-lookup"><span data-stu-id="b57e2-165">Posting definition – Match criteria</span></span>

| <span data-ttu-id="b57e2-166">勘定構造</span><span class="sxs-lookup"><span data-stu-id="b57e2-166">Account structure</span></span>       | <span data-ttu-id="b57e2-167">照合勘定番号</span><span class="sxs-lookup"><span data-stu-id="b57e2-167">Match account number</span></span> | <span data-ttu-id="b57e2-168">優先順位</span><span class="sxs-lookup"><span data-stu-id="b57e2-168">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="b57e2-169">勘定構造 - P&L</span><span class="sxs-lookup"><span data-stu-id="b57e2-169">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="b57e2-170">1</span><span class="sxs-lookup"><span data-stu-id="b57e2-170">1</span></span>        |

<span data-ttu-id="b57e2-171"><em>\**照合勘定番号</em>* フィールドの空白の値は、定義された勘定構造のすべての照合勘定が一致するルールの一部になります。</span><span class="sxs-lookup"><span data-stu-id="b57e2-171"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="b57e2-172">転記の定義 – 生成されたエントリ</span><span class="sxs-lookup"><span data-stu-id="b57e2-172">Posting definition – Generated entries</span></span>

| <span data-ttu-id="b57e2-173">勘定構造</span><span class="sxs-lookup"><span data-stu-id="b57e2-173">Account structure</span></span> | <span data-ttu-id="b57e2-174">生成された勘定番号</span><span class="sxs-lookup"><span data-stu-id="b57e2-174">Generated account number</span></span>              | <span data-ttu-id="b57e2-175">生成された借方/貸方</span><span class="sxs-lookup"><span data-stu-id="b57e2-175">Generated debit/credit</span></span> |
|-------------------|---------------------------------------|------------------------|
| <span data-ttu-id="b57e2-176">勘定構造</span><span class="sxs-lookup"><span data-stu-id="b57e2-176">Account structure</span></span> | <span data-ttu-id="b57e2-177">300145 - -(見積られた収益口座)</span><span class="sxs-lookup"><span data-stu-id="b57e2-177">300145 - -(Estimated revenue account)</span></span> | <span data-ttu-id="b57e2-178">同じ</span><span class="sxs-lookup"><span data-stu-id="b57e2-178">Same</span></span>                   |
| <span data-ttu-id="b57e2-179">勘定構造</span><span class="sxs-lookup"><span data-stu-id="b57e2-179">Account structure</span></span> | <span data-ttu-id="b57e2-180">300146 - -(割り当て口座)</span><span class="sxs-lookup"><span data-stu-id="b57e2-180">300146 - -(Appropriation account)</span></span>     | <span data-ttu-id="b57e2-181">バランスをとる</span><span class="sxs-lookup"><span data-stu-id="b57e2-181">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="b57e2-182">勘定、分析コード値、および金額を含むトランザクション</span><span class="sxs-lookup"><span data-stu-id="b57e2-182">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="b57e2-183">**予算登録エントリ** ページで、予算勘定項目の勘定、分析コード値、金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="b57e2-183">You enter the accounts, dimension values, and amounts for the budget account entry on the **Budget register entry** page.</span></span>

| <span data-ttu-id="b57e2-184">口座 + 分析コード</span><span class="sxs-lookup"><span data-stu-id="b57e2-184">Account + dimensions</span></span>           | <span data-ttu-id="b57e2-185">デビット</span><span class="sxs-lookup"><span data-stu-id="b57e2-185">Debit</span></span> | <span data-ttu-id="b57e2-186">クレジット</span><span class="sxs-lookup"><span data-stu-id="b57e2-186">Credit</span></span> | <span data-ttu-id="b57e2-187">コメント</span><span class="sxs-lookup"><span data-stu-id="b57e2-187">Comment</span></span> |
|--------------------------------|-------|--------|---------|
| <span data-ttu-id="b57e2-188">606400-OU\_1-OU\_3566-トレーニング</span><span class="sxs-lookup"><span data-stu-id="b57e2-188">606400-OU\_1-OU\_3566-Training</span></span> |       | <span data-ttu-id="b57e2-189">250.00</span><span class="sxs-lookup"><span data-stu-id="b57e2-189">250.00</span></span> |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="b57e2-190">転記の定義から生成された元帳エントリ</span><span class="sxs-lookup"><span data-stu-id="b57e2-190">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="b57e2-191">生成された元帳エントリは各分析コードの元の予算を記録するために作成されます。</span><span class="sxs-lookup"><span data-stu-id="b57e2-191">Generated ledger entries are created to record the original budget in each dimension.</span></span>

| <span data-ttu-id="b57e2-192">口座 + 分析コード</span><span class="sxs-lookup"><span data-stu-id="b57e2-192">Account + dimensions</span></span>           | <span data-ttu-id="b57e2-193">デビット</span><span class="sxs-lookup"><span data-stu-id="b57e2-193">Debit</span></span>  | <span data-ttu-id="b57e2-194">クレジット</span><span class="sxs-lookup"><span data-stu-id="b57e2-194">Credit</span></span> | <span data-ttu-id="b57e2-195">コメント</span><span class="sxs-lookup"><span data-stu-id="b57e2-195">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="b57e2-196">300145-OU\_1-OU\_3566-トレーニング</span><span class="sxs-lookup"><span data-stu-id="b57e2-196">300145-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="b57e2-197">250.00</span><span class="sxs-lookup"><span data-stu-id="b57e2-197">250.00</span></span> |         |
| <span data-ttu-id="b57e2-198">300146-OU\_1-OU\_3566-トレーニング</span><span class="sxs-lookup"><span data-stu-id="b57e2-198">300146-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="b57e2-199">250.00</span><span class="sxs-lookup"><span data-stu-id="b57e2-199">250.00</span></span> |        |         |

<span data-ttu-id="b57e2-200">この例では、勘定構造 - P&L の一部であるいずれかの口座が転記の定義の基準に一致します。</span><span class="sxs-lookup"><span data-stu-id="b57e2-200">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="b57e2-201">したがって、606400-OU\_1-OU\_3566-トレーニングが評価されると、生成された元帳エントリが作成されます。</span><span class="sxs-lookup"><span data-stu-id="b57e2-201">Therefore, when 606400-OU\_1-OU\_3566-Training is evaluated, the generated ledger entries are created.</span></span>





