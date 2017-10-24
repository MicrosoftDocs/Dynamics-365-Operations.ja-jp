---
title: "番号順序"
description: "番号順序は、ID が必要なマスター データ レコードおよびトランザクション レコードに対して読みやすい固有の ID を生成するために使用されます。"
author: MargoC
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bd1f4d383848e6205d64be160da4c529adeaccf2
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="number-sequences"></a><span data-ttu-id="f41e0-103">番号順序</span><span class="sxs-lookup"><span data-stu-id="f41e0-103">Number sequences</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f41e0-104">番号順序は、ID が必要なマスター データ レコードおよびトランザクション レコードに対して読みやすい固有の ID を生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="f41e0-105">ID が必要なマスタ データ レコードまたはトランザクション レコードは、*参照*と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-105">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span>

<span data-ttu-id="f41e0-106">参照先に新しいレコードを作成するには、事前に番号順序を設定して参照先に関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="f41e0-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="f41e0-107">[**組織管理**] のページを使用して番号順序を設定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f41e0-107">We recommend that you use the pages in **Organization administration** to set up number sequences.</span></span> <span data-ttu-id="f41e0-108">モジュール固有の設定が必要な場合、モジュールのパラメータ ページを使用してそのモジュールでの参照用に番号順序を指定できます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-108">If module-specific settings are required, you can use the parameters page in a module to specify number sequences for the references in that module.</span></span> <span data-ttu-id="f41e0-109">たとえば、[**売掛金勘定**] および [**買掛金勘定**] で、特定の顧客または仕入先に固有の番号順序を割り当てるために番号順序グループを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-109">For example, in **Accounts receivable** and **Accounts payable**, you can set up number sequence groups to allocate specific number sequences to specific customers or vendors.</span></span> 

<span data-ttu-id="f41e0-110">番号順序を設定した場合、番号順序を使用する組織を定義する範囲を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f41e0-110">When you set up a number sequence, you must specify a scope, which defines which organization uses the number sequence.</span></span> <span data-ttu-id="f41e0-111">範囲は、**共有**、**会社**、**法人**、または**作業単位**のいずれかにすることができます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-111">The scope can be **Shared**, **Company**, **Legal entity**, or **Operating unit**.</span></span> <span data-ttu-id="f41e0-112">**法人**および**会社**の範囲は、**会計カレンダー期間**と組み合わせ、より具体的な番号順序を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-112">**Legal entity** and **Company** scopes can be combined with **Fiscal calendar period** to create even more specific number sequences.</span></span> 

<span data-ttu-id="f41e0-113">番号順序の形式は、区分で構成されます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-113">Number sequence formats consist of segments.</span></span> <span data-ttu-id="f41e0-114">**共有**以外の範囲の番号順序には、その範囲に対応する区分を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-114">Number sequences with a scope other than **Shared** can contain segments that correspond to the scope.</span></span> <span data-ttu-id="f41e0-115">たとえば、**法人**の範囲の番号順序には、法人の区分を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-115">For example, a number sequence with a scope of **Legal entity** can contain a legal entity segment.</span></span> <span data-ttu-id="f41e0-116">番号順序の形式で範囲の区分を含めることで、その番号を見て特定のレコードの範囲を識別できます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-116">By including a scope segment in the number sequence format, you can identify the scope of a particular record by looking at its number.</span></span> 

<span data-ttu-id="f41e0-117">範囲に対応する区分に加え、番号順序の形式には**定数**および**英数字区分**を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-117">In addition to segments that correspond to scopes, number sequence formats can contain **Constant** and **Alphanumeric segments**.</span></span> <span data-ttu-id="f41e0-118">**定数**の区分には、変更されない一連の文字、番号、または記号が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-118">A **Constant** segment contains a set of letters, numbers, or symbols that does not change.</span></span> <span data-ttu-id="f41e0-119">**英数区分**の区分には、番号が使用されるたびに繰り上げる一連の文字または番号が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-119">An **Alphanumeric** segment contains a set of letters or numbers that increment every time that a number is used.</span></span> <span data-ttu-id="f41e0-120">番号記号 (\#) は数字の繰り上げに、アンパサンド (&) は文字の繰り上げに使用します。</span><span class="sxs-lookup"><span data-stu-id="f41e0-120">Use a number sign (\#) to represent incrementing numbers and an ampersand (&) to represent incrementing letters.</span></span> <span data-ttu-id="f41e0-121">たとえば、\#\#\#\#\#\_2017 という形式を指定した場合、00001\_2017, 00002\_2017 という順序で番号が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-121">For example, the format \#\#\#\#\#\_2017 creates the sequence 00001\_2017, 00002\_2017, and so on.</span></span>

<a name="number-sequence-examples"></a><span data-ttu-id="f41e0-122">番号順序の例</span><span class="sxs-lookup"><span data-stu-id="f41e0-122">Number sequence examples</span></span>
------------------------

<span data-ttu-id="f41e0-123">次の例では、区分を使用して番号順序の形式を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f41e0-123">The following examples show how to use segments to create number sequence formats.</span></span> <span data-ttu-id="f41e0-124">特に、例では、範囲の区分を使用した場合の影響を示します。</span><span class="sxs-lookup"><span data-stu-id="f41e0-124">In particular, the examples demonstrate the effects of using scope segments.</span></span>

### <a name="expense-report-numbers"></a><span data-ttu-id="f41e0-125">経費精算書番号</span><span class="sxs-lookup"><span data-stu-id="f41e0-125">Expense report numbers</span></span>

<span data-ttu-id="f41e0-126">次の例では、経費精算書番号が **CS** という名前の法人に設定されます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-126">In the following example, expense report numbers are set up for the legal entity that is titled **CS**.</span></span> 

- <span data-ttu-id="f41e0-127">[**地域:**] 旅費交通費</span><span class="sxs-lookup"><span data-stu-id="f41e0-127">**Area:** Travel and expense</span></span> 
- <span data-ttu-id="f41e0-128">[**参照:**] 経費精算書番号</span><span class="sxs-lookup"><span data-stu-id="f41e0-128">**Reference:** Expense report number</span></span> 
- <span data-ttu-id="f41e0-129">[**スコープ:**] 法人</span><span class="sxs-lookup"><span data-stu-id="f41e0-129">**Scope:** Legal entity</span></span> 
- <span data-ttu-id="f41e0-130">[**法人:**] CS</span><span class="sxs-lookup"><span data-stu-id="f41e0-130">**Legal entity:** CS</span></span>

| <span data-ttu-id="f41e0-131">区分</span><span class="sxs-lookup"><span data-stu-id="f41e0-131">Segments</span></span>  | <span data-ttu-id="f41e0-132">区分のタイプ</span><span class="sxs-lookup"><span data-stu-id="f41e0-132">Segment type</span></span> | <span data-ttu-id="f41e0-133">値</span><span class="sxs-lookup"><span data-stu-id="f41e0-133">Value</span></span>     |
|-----------|--------------|-----------|
| <span data-ttu-id="f41e0-134">区分 1</span><span class="sxs-lookup"><span data-stu-id="f41e0-134">Segment 1</span></span> | <span data-ttu-id="f41e0-135">個法</span><span class="sxs-lookup"><span data-stu-id="f41e0-135">Legal entity</span></span> | <span data-ttu-id="f41e0-136">CS</span><span class="sxs-lookup"><span data-stu-id="f41e0-136">CS</span></span>        |
| <span data-ttu-id="f41e0-137">区分 2</span><span class="sxs-lookup"><span data-stu-id="f41e0-137">Segment 2</span></span> | <span data-ttu-id="f41e0-138">定数</span><span class="sxs-lookup"><span data-stu-id="f41e0-138">Constant</span></span>     | <span data-ttu-id="f41e0-139">-EXPENSE-</span><span class="sxs-lookup"><span data-stu-id="f41e0-139">-EXPENSE-</span></span> |
| <span data-ttu-id="f41e0-140">区分 3</span><span class="sxs-lookup"><span data-stu-id="f41e0-140">Segment 3</span></span> | <span data-ttu-id="f41e0-141">英数字</span><span class="sxs-lookup"><span data-stu-id="f41e0-141">Alphanumeric</span></span> | \#\#\#\#  |

<span data-ttu-id="f41e0-142">**書式設定された番号の例**: CS-EXPENSE-0039</span><span class="sxs-lookup"><span data-stu-id="f41e0-142">**Example of formatted number**: CS-EXPENSE-0039</span></span> 

<span data-ttu-id="f41e0-143">他の法人に対して同様の番号順序の形式を設定できます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-143">You can set up a similar number sequence format for other legal entities.</span></span> <span data-ttu-id="f41e0-144">たとえば、**RW** という名前の法人の場合、法人の区分の値のみ変更すると、書式設定された番号は RW-EXPENSE-0039 です。</span><span class="sxs-lookup"><span data-stu-id="f41e0-144">For example, for a legal entity that is named **RW**, if you change only the value of the legal entity segment, the formatted number is RW-EXPENSE-0039.</span></span> <span data-ttu-id="f41e0-145">また、他の法人について番号順序全体の形式を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-145">You can also change the whole number sequence format for other legal entities.</span></span> <span data-ttu-id="f41e0-146">たとえば、法人の範囲の区分を省略して、Exp-0001 のような書式設定された番号を作成できます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-146">For example, you can omit the legal entity scope segment to create a formatted number such as Exp-0001.</span></span>

### <a name="sales-order-numbers"></a><span data-ttu-id="f41e0-147">販売注文番号</span><span class="sxs-lookup"><span data-stu-id="f41e0-147">Sales order numbers</span></span>

<span data-ttu-id="f41e0-148">次の例では、会社 ID **CEU** に対して販売注文番号を設定します。</span><span class="sxs-lookup"><span data-stu-id="f41e0-148">In the following example, sales order numbers are set up for the company ID **CEU**.</span></span> 

- <span data-ttu-id="f41e0-149">[**領域:**] 販売</span><span class="sxs-lookup"><span data-stu-id="f41e0-149">**Area:** Sales</span></span> 
- <span data-ttu-id="f41e0-150">[**参照:**] 販売注文</span><span class="sxs-lookup"><span data-stu-id="f41e0-150">**Reference:** Sales order</span></span> 
- <span data-ttu-id="f41e0-151">[**スコープ:**] 会社</span><span class="sxs-lookup"><span data-stu-id="f41e0-151">**Scope:** Company</span></span> 
- <span data-ttu-id="f41e0-152">[**会社:**] CEU</span><span class="sxs-lookup"><span data-stu-id="f41e0-152">**Company:** CEU</span></span>

| <span data-ttu-id="f41e0-153">区分</span><span class="sxs-lookup"><span data-stu-id="f41e0-153">Segments</span></span>  | <span data-ttu-id="f41e0-154">セグメント タイプ</span><span class="sxs-lookup"><span data-stu-id="f41e0-154">Segment type</span></span> | <span data-ttu-id="f41e0-155">先頭値</span><span class="sxs-lookup"><span data-stu-id="f41e0-155">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="f41e0-156">区分 1</span><span class="sxs-lookup"><span data-stu-id="f41e0-156">Segment 1</span></span> | <span data-ttu-id="f41e0-157">定数</span><span class="sxs-lookup"><span data-stu-id="f41e0-157">Constant</span></span>     | <span data-ttu-id="f41e0-158">SO-</span><span class="sxs-lookup"><span data-stu-id="f41e0-158">SO-</span></span>      |
| <span data-ttu-id="f41e0-159">区分 2</span><span class="sxs-lookup"><span data-stu-id="f41e0-159">Segment 2</span></span> | <span data-ttu-id="f41e0-160">英数字</span><span class="sxs-lookup"><span data-stu-id="f41e0-160">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="f41e0-161">:**書式設定された番号の例**: SO-0029</span><span class="sxs-lookup"><span data-stu-id="f41e0-161">**Example of formatted number**: SO-0029</span></span> 

<span data-ttu-id="f41e0-162">範囲の区分が形式に含まれていない場合でも、法人 ID の番号付けが再開されます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-162">Even though a scope segment is not included in the format, numbering restarts for each company ID.</span></span> <span data-ttu-id="f41e0-163">すべての法人 ID に同じ形式を使用した場合、各法人で同じ番号が使用されます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-163">If you use the same format for all company IDs, the same numbers are used in each company.</span></span> <span data-ttu-id="f41e0-164">たとえば、販売注文番号 SO-0029 が各法人で使用されます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-164">For example, sales order number SO-0029 is used in each company.</span></span> <span data-ttu-id="f41e0-165">また、他の法人 ID について番号順序全体の形式を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-165">You can also change the whole number sequence format for other company IDs.</span></span>

### <a name="purchase-requisition-numbers"></a><span data-ttu-id="f41e0-166">購買要求番号</span><span class="sxs-lookup"><span data-stu-id="f41e0-166">Purchase requisition numbers</span></span>

<span data-ttu-id="f41e0-167">次の例では、購買要求番号が組織全体で使用されます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-167">In the following example, purchase requisition numbers are organization-wide.</span></span> 

- <span data-ttu-id="f41e0-168">[**領域:**] 購買</span><span class="sxs-lookup"><span data-stu-id="f41e0-168">**Area:** Purchase</span></span> 
- <span data-ttu-id="f41e0-169">[**参照:**] 購買要求</span><span class="sxs-lookup"><span data-stu-id="f41e0-169">**Reference:** Purchase requisition</span></span> 
- <span data-ttu-id="f41e0-170">[**スコープ:**] 共有</span><span class="sxs-lookup"><span data-stu-id="f41e0-170">**Scope:** Shared</span></span>

| <span data-ttu-id="f41e0-171">区分</span><span class="sxs-lookup"><span data-stu-id="f41e0-171">Segments</span></span>  | <span data-ttu-id="f41e0-172">セグメント タイプ</span><span class="sxs-lookup"><span data-stu-id="f41e0-172">Segment type</span></span> | <span data-ttu-id="f41e0-173">先頭値</span><span class="sxs-lookup"><span data-stu-id="f41e0-173">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="f41e0-174">区分 1</span><span class="sxs-lookup"><span data-stu-id="f41e0-174">Segment 1</span></span> | <span data-ttu-id="f41e0-175">定数</span><span class="sxs-lookup"><span data-stu-id="f41e0-175">Constant</span></span>     | <span data-ttu-id="f41e0-176">要求</span><span class="sxs-lookup"><span data-stu-id="f41e0-176">Req</span></span>      |
| <span data-ttu-id="f41e0-177">区分 2</span><span class="sxs-lookup"><span data-stu-id="f41e0-177">Segment 2</span></span> | <span data-ttu-id="f41e0-178">英数字</span><span class="sxs-lookup"><span data-stu-id="f41e0-178">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="f41e0-179">**書式設定された番号の例**: Req0052</span><span class="sxs-lookup"><span data-stu-id="f41e0-179">**Example of formatted number**: Req0052</span></span> 

<span data-ttu-id="f41e0-180">範囲が [**共有**] であるため、番号順序の形式は組織全体で使用されます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-180">Because the scope is **Shared**, the number sequence format is used across the organization.</span></span> <span data-ttu-id="f41e0-181">組織の一部に異なる番号順序の形式を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="f41e0-181">You cannot set up different number sequence formats for different parts of the organization.</span></span> 

<a name="performance-considerations-for-number-sequences"></a><span data-ttu-id="f41e0-182">番号順序のパフォーマンスに関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="f41e0-182">Performance considerations for number sequences</span></span>
-----------------------------------------------

<span data-ttu-id="f41e0-183">番号順序を設定する前に、番号順序のコンフィギュレーションがシステムのパフォーマンスにどのように影響を及ぼすかについて次の情報を考慮してください。</span><span class="sxs-lookup"><span data-stu-id="f41e0-183">Consider the following information about how the configuration of number sequences can affect system performance before you set up number sequences.</span></span>

### <a name="continuous-and-non-continuous-number-sequences"></a><span data-ttu-id="f41e0-184">連続する番号順序と連続しない番号順序</span><span class="sxs-lookup"><span data-stu-id="f41e0-184">Continuous and non-continuous number sequences</span></span>

<span data-ttu-id="f41e0-185">番号順序は、連続または非連続にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-185">Number sequences can be continuous or non-continuous.</span></span> <span data-ttu-id="f41e0-186">連続する番号順序は番号をスキップしませんが、番号が順次に使用されないことがあります。</span><span class="sxs-lookup"><span data-stu-id="f41e0-186">A continuous number sequence does not skip any numbers, but numbers may not be used sequentially.</span></span> <span data-ttu-id="f41e0-187">連続しない番号順序の番号は順次に使用されますが、番号がスキップされることがあります。</span><span class="sxs-lookup"><span data-stu-id="f41e0-187">Numbers from a non-continuous number sequence are used sequentially, but the number sequence may skip numbers.</span></span> <span data-ttu-id="f41e0-188">たとえば、ユーザーがトランザクションをキャンセルした場合、番号は生成されますが、使用されません。</span><span class="sxs-lookup"><span data-stu-id="f41e0-188">For example, if a user cancels a transaction, a number is generated, but not used.</span></span> <span data-ttu-id="f41e0-189">連続する番号順序では、その番号は後で再利用されます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-189">In a continuous number sequence, that number is recycled later.</span></span> <span data-ttu-id="f41e0-190">連続しない番号順では、その番号は使用されません。</span><span class="sxs-lookup"><span data-stu-id="f41e0-190">In a non-continuous number sequence, the number is not used.</span></span> 

<span data-ttu-id="f41e0-191">通常、連続する番号順序は、発注書、販売注文、請求書などの外部ドキュメントに必要です。</span><span class="sxs-lookup"><span data-stu-id="f41e0-191">Continuous number sequences are typically required for external documents, such as purchase orders, sales orders, and invoices.</span></span> <span data-ttu-id="f41e0-192">ただし、新しいドキュメントまたはレコードが作成されるたびにシステムがデータベースから番号を要求するため、連続する番号順序がシステムの応答時間に悪影響を及ぼすことがあります。</span><span class="sxs-lookup"><span data-stu-id="f41e0-192">However, continuous number sequences can adversely affect system response times because the system must request a number from the database every time that a new document or record is created.</span></span> 

<span data-ttu-id="f41e0-193">連続しない番号順序を使用する場合、[**番号順序**] ページにある [**パフォーマンス**] クイック タブの [**事前割り当て**] を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-193">If you use a non-continuous number sequence, you can enable **Preallocation** on the **Performance** FastTab of the **Number sequences** page.</span></span> <span data-ttu-id="f41e0-194">事前に割り当てする番号の数量を指定すると、システムではそれらの番号を選択し、メモリに格納します。</span><span class="sxs-lookup"><span data-stu-id="f41e0-194">When you specify a quantity of numbers to preallocate, the system selects those numbers and stores them in memory.</span></span> <span data-ttu-id="f41e0-195">事前に割り当てた数量を使用した後にのみ、新しい番号がデータベースから要求されます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-195">New numbers are requested from the database only after the preallocated quantity has been used.</span></span> 

<span data-ttu-id="f41e0-196">連続する番号順序の使用が法的な要求事項でない限り、パフォーマンス向上のために連続しない番号順序を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f41e0-196">Unless there is a regulatory requirement that you use continuous number sequences, we recommend that you use non-continuous number sequences for better performance.</span></span>

### <a name="automatic-cleanup-of-number-sequences"></a><span data-ttu-id="f41e0-197">番号順序の自動クリーンアップ</span><span class="sxs-lookup"><span data-stu-id="f41e0-197">Automatic cleanup of number sequences</span></span>

<span data-ttu-id="f41e0-198">電源障碍、アプリケーションのエラー、またはその他の予期しないエラーが発生した場合、システムでは連続する番号順序に対して番号を自動的に再利用できません。</span><span class="sxs-lookup"><span data-stu-id="f41e0-198">In case of a power failure, an application error, or other unexpected failure, the system cannot recycle numbers automatically for continuous number sequences.</span></span> <span data-ttu-id="f41e0-199">クリーンアップ プロセスを手動または自動で実行して、失われた番号を復元することができます。</span><span class="sxs-lookup"><span data-stu-id="f41e0-199">You can run the cleanup process manually or automatically to recover the lost numbers.</span></span> 

<span data-ttu-id="f41e0-200">クリーンアップ プロセスを計画する際は、サーバーの使用を慎重に検討してください。</span><span class="sxs-lookup"><span data-stu-id="f41e0-200">Carefully consider server usage when you plan the cleanup process.</span></span> <span data-ttu-id="f41e0-201">クリーンアップはピーク時間外にバッチ ジョブで実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f41e0-201">We recommend that you perform the cleanup as a batch job during non-peak hours.</span></span>






