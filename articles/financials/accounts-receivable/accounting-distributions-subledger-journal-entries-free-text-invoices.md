---
title: "自由書式の請求書の勘定配布と補助元帳仕訳"
description: "勘定配布は収益、税金、雑費などの金額がどのように自由書式の請求書に計上されるかを定義するために使用されます。 自由書式の請求書が仕訳されたときに計上する必要のあるすべての金額に勘定配布があります。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 5d1546e8537110daec5d6655f68d3328a58ca1cb
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---

# <a name="accounting-distributions-and-subledger-journal-entries-for-free-text-invoices"></a><span data-ttu-id="1bd32-104">自由書式の請求書の勘定配布と補助元帳仕訳</span><span class="sxs-lookup"><span data-stu-id="1bd32-104">Accounting distributions and subledger journal entries for free text invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1bd32-105">勘定配布は収益、税金、雑費などの金額がどのように自由書式の請求書に計上されるかを定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1bd32-105">Accounting distributions are used to define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span> <span data-ttu-id="1bd32-106">自由書式の請求書が仕訳されたときに計上する必要のあるすべての金額に勘定配布があります。</span><span class="sxs-lookup"><span data-stu-id="1bd32-106">Every amount that must be accounted for when the free text invoice is journalized will have one or more accounting distributions.</span></span>

<a name="accounting-distributions"></a><span data-ttu-id="1bd32-107">勘定配布</span><span class="sxs-lookup"><span data-stu-id="1bd32-107">Accounting distributions</span></span>
------------------------

<span data-ttu-id="1bd32-108">自由書式の請求書ページで次のボタンを使用して、自由書式の請求の各金額の勘定配布を表示すること、また場合によっては変更することができます。</span><span class="sxs-lookup"><span data-stu-id="1bd32-108">You can use the following buttons in the Free text invoice page to view, and possibly change, the accounting distributions for each amount on the free text invoice.</span></span>

-   <span data-ttu-id="1bd32-109">**金額の配分**—税または請求金額などの明細行と子明細行の勘定配布を表示または変更します。</span><span class="sxs-lookup"><span data-stu-id="1bd32-109">**Distribute amounts**—View and change the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="1bd32-110">売上税トランザクション ページまたは諸費用トランザクション ページから子明細行の勘定配布を直接表示または変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="1bd32-110">You can also view and change the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="1bd32-111">請求金額または通貨の丸めなど、自由書式の請求書ヘッダーの金額を変更します。</span><span class="sxs-lookup"><span data-stu-id="1bd32-111">Change free text invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="1bd32-112">自由書式の請求明細行金額を変更します。</span><span class="sxs-lookup"><span data-stu-id="1bd32-112">Change free text invoice line amounts.</span></span>
-   <span data-ttu-id="1bd32-113">**配分の表示**—すべての伝票の明細行の勘定配布を表示します。</span><span class="sxs-lookup"><span data-stu-id="1bd32-113">**View distributions**—View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="1bd32-114">このビューで勘定配布を変更できません。</span><span class="sxs-lookup"><span data-stu-id="1bd32-114">You can't change the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="1bd32-115">表示のヘッダーと明細金額。</span><span class="sxs-lookup"><span data-stu-id="1bd32-115">View header and line amounts.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="1bd32-116">金額の配分</span><span class="sxs-lookup"><span data-stu-id="1bd32-116">Distributing amounts</span></span>
<span data-ttu-id="1bd32-117">自由書式の請求書を入力すると、各金額は次のように配分されます。</span><span class="sxs-lookup"><span data-stu-id="1bd32-117">When you enter a free text invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1bd32-118">金額のタイプ</span><span class="sxs-lookup"><span data-stu-id="1bd32-118">Type of monetary amount</span></span></th>
<th><span data-ttu-id="1bd32-119">主勘定の表示元</span><span class="sxs-lookup"><span data-stu-id="1bd32-119">Where the main account is displayed from</span></span></th>
<th><span data-ttu-id="1bd32-120">表示される既定の財務分析コードを決定する優先順位</span><span class="sxs-lookup"><span data-stu-id="1bd32-120">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1bd32-121">自由書式の請求明細行</span><span class="sxs-lookup"><span data-stu-id="1bd32-121">Free text invoice line</span></span></td>
<td><span data-ttu-id="1bd32-122">自由書式の請求明細行の勘定科目。</span><span class="sxs-lookup"><span data-stu-id="1bd32-122">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="1bd32-123">主勘定が配賦勘定の場合、配賦勘定定義の既定値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1bd32-123">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="1bd32-124">主勘定が配賦勘定でない場合は、自由書式の請求明細行の財務分析コードの既定のテンプレートを使用します。</span><span class="sxs-lookup"><span data-stu-id="1bd32-124">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="1bd32-125">自由書式の請求明細行の既定の財務分析コードの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1bd32-125">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="1bd32-126">勘定科目表ページで、勘定科目の既定の財務分析コードの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1bd32-126">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1bd32-127">固定資産番号と価値モデルの組み合わせの自由書式の請求明細行</span><span class="sxs-lookup"><span data-stu-id="1bd32-127">Free text invoice line for a fixed asset number and value model combination</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1bd32-128"><strong>メモ </strong></span><span class="sxs-lookup"><span data-stu-id="1bd32-128"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1bd32-129">自由書式の請求明細行の主勘定は固定資産の処分勘定になります。</span><span class="sxs-lookup"><span data-stu-id="1bd32-129">The main account on the free text invoice line will be the fixed asset disposal account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
<td><span data-ttu-id="1bd32-130">自由書式の請求明細行の勘定科目。</span><span class="sxs-lookup"><span data-stu-id="1bd32-130">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="1bd32-131">自由書式の請求明細行の既定の財務分析コードの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1bd32-131">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="1bd32-132">勘定科目表ページで、勘定科目の既定の財務分析コードの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1bd32-132">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1bd32-133">自由書式の請求書の割引金額</span><span class="sxs-lookup"><span data-stu-id="1bd32-133">Free text invoice discount amount</span></span></td>
<td><span data-ttu-id="1bd32-134">現金割引ページの [顧客割引の主勘定] フィールド。</span><span class="sxs-lookup"><span data-stu-id="1bd32-134">The Main account for customer discounts field in the Cash discounts page.</span></span></td>
<td><ol>
<li><span data-ttu-id="1bd32-135">主勘定が配賦勘定の場合、配賦勘定定義の既定値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1bd32-135">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="1bd32-136">主勘定が配賦勘定でない場合は、自由書式の請求明細行の財務分析コードの既定のテンプレートを使用します。</span><span class="sxs-lookup"><span data-stu-id="1bd32-136">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="1bd32-137">自由書式の請求明細行の既定の財務分析コードの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1bd32-137">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="1bd32-138">勘定科目表ページで、勘定科目の既定の財務分析コードの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1bd32-138">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1bd32-139">自由書式の請求書の売上税金額</span><span class="sxs-lookup"><span data-stu-id="1bd32-139">Free text invoice sales tax amount</span></span></td>
<td><span data-ttu-id="1bd32-140">元帳転記グループ ページの [売上税支払] フィールド。</span><span class="sxs-lookup"><span data-stu-id="1bd32-140">The Sales tax payable field in the Ledger posting groups page.</span></span></td>
<td><ol>
<li><span data-ttu-id="1bd32-141">自由書式の請求明細行金額または費用明細金額の配賦で定義された財務分析コードを使用します。</span><span class="sxs-lookup"><span data-stu-id="1bd32-141">Use the financial dimensions that are defined on the free text invoice line amount or the distributions for the charge line amount.</span></span></li>
<li><span data-ttu-id="1bd32-142">自由書式の請求明細行の既定の財務分析コードの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1bd32-142">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="1bd32-143">勘定科目表ページで、勘定科目の既定の財務分析コードの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1bd32-143">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1bd32-144">自由書式の請求書の費用明細金額</span><span class="sxs-lookup"><span data-stu-id="1bd32-144">Free text invoice charge line amount</span></span></td>
<td><span data-ttu-id="1bd32-145">諸費用コード ページの [貸方勘定] フィールド。</span><span class="sxs-lookup"><span data-stu-id="1bd32-145">The Credit account field in the Charges code page.</span></span></td>
<td><ol>
<li><span data-ttu-id="1bd32-146">主勘定が配賦勘定の場合、配賦勘定定義の既定値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1bd32-146">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="1bd32-147">主勘定が配賦勘定でない場合は、自由書式の請求明細行の財務分析コードの既定のテンプレートを使用します。</span><span class="sxs-lookup"><span data-stu-id="1bd32-147">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="1bd32-148">自由書式の請求明細行の既定の財務分析コードの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1bd32-148">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="1bd32-149">勘定科目表ページで、勘定科目の既定の財務分析コードの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1bd32-149">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a><span data-ttu-id="1bd32-150">税の配分</span><span class="sxs-lookup"><span data-stu-id="1bd32-150">Distributing taxes</span></span>
<span data-ttu-id="1bd32-151">税金の勘定配布は、税金が計算されるまで作成できません。</span><span class="sxs-lookup"><span data-stu-id="1bd32-151">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="1bd32-152">売上税を計算するには、[自由書式の請求書] フォームで次の作業のいずれかを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bd32-152">To calculate sales taxes, you must complete one of the following tasks in the Free text invoice form:</span></span>
-   <span data-ttu-id="1bd32-153">売上税を表示する。</span><span class="sxs-lookup"><span data-stu-id="1bd32-153">View the sales tax.</span></span>
-   <span data-ttu-id="1bd32-154">請求金額の合計を表示する。</span><span class="sxs-lookup"><span data-stu-id="1bd32-154">View the invoice total.</span></span>
-   <span data-ttu-id="1bd32-155">キャッシュ フローを表示する。</span><span class="sxs-lookup"><span data-stu-id="1bd32-155">View the cash flow.</span></span>
-   <span data-ttu-id="1bd32-156">自由書式の請求書全体の勘定配布を表示する。</span><span class="sxs-lookup"><span data-stu-id="1bd32-156">View accounting distributions for the whole free text invoice.</span></span>
-   <span data-ttu-id="1bd32-157">補助元帳を表示する。</span><span class="sxs-lookup"><span data-stu-id="1bd32-157">View the subledger journal.</span></span>

## <a name="subledger-journals-for-free-text-invoices"></a><span data-ttu-id="1bd32-158">自由書式の請求書の補助元帳</span><span class="sxs-lookup"><span data-stu-id="1bd32-158">Subledger journals for free text invoices</span></span>
<span data-ttu-id="1bd32-159">自由書式の請求書を転記する前に、請求書が適切な勘定に転記されることを保証するために借方と貸方が含まれる請求書の完全な勘定項目を表示できます。</span><span class="sxs-lookup"><span data-stu-id="1bd32-159">Before you post a free text invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="1bd32-160">全勘定項目の表示は補助元帳と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="1bd32-160">This view of the full accounting entry is called a subledger journal.</span></span> <span data-ttu-id="1bd32-161">自由書式の請求書を仕訳入力する前に、プレビューした結果、補助元帳仕訳が正しくない場合、補助元帳仕訳は変更できません。</span><span class="sxs-lookup"><span data-stu-id="1bd32-161">If the subledger journal entry is incorrect when you preview it before you journalize the free text invoice, you can't change the subledger journal entry.</span></span> <span data-ttu-id="1bd32-162">代わりに、勘定配布または転記プロファイルを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1bd32-162">Instead, you must change the accounting distributions or the posting profile.</span></span> <span data-ttu-id="1bd32-163">勘定配布は、勘定項目の借方または貸方のいずれか一方を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1bd32-163">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="1bd32-164">相殺補助元帳仕訳勘定項目は、顧客勘定または税などの転記プロファイルから作成されます。</span><span class="sxs-lookup"><span data-stu-id="1bd32-164">The offsetting subledger journal account entry is created from the posting profiles, such as from the customer account or the tax.</span></span>




