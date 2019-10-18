---
title: 顧客請求書の作成
description: '**販売注文の顧客請求書**は、売上に関連し、組織が顧客に提供する請求書です。'
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa49b70b07ac3dc6cbc5989b11981098f22be89c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189157"
---
# <a name="create-a-customer-invoice"></a><span data-ttu-id="c88a8-103">顧客請求書の作成</span><span class="sxs-lookup"><span data-stu-id="c88a8-103">Create a customer invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c88a8-104">**販売注文の顧客請求書**は、売上に関連し、組織が顧客に提供する請求書です。</span><span class="sxs-lookup"><span data-stu-id="c88a8-104">A **customer invoice for a sales order** is a bill that is related to a sale, and that an organization gives to a customer.</span></span> <span data-ttu-id="c88a8-105">この種類の顧客請求書は、注文明細行および品目番号を含む販売注文に基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-105">This type of customer invoice is created based on a sales order, which includes order lines and item numbers.</span></span> <span data-ttu-id="c88a8-106">品目番号が指定され、元帳に転記されます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-106">Item numbers are specified and posted in the ledger.</span></span> <span data-ttu-id="c88a8-107">補助元帳仕訳帳は、販売注文の顧客請求書では使用できません。</span><span class="sxs-lookup"><span data-stu-id="c88a8-107">Subledger journal entries aren't available for a customer invoice for a sales order.</span></span> <span data-ttu-id="c88a8-108">詳細については、「[販売注文請求書の作成](tasks/create-sales-order-invoices.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c88a8-108">For more information, see [Create sales order invoices](tasks/create-sales-order-invoices.md).</span></span>

<span data-ttu-id="c88a8-109">**自由書式の請求書**は販売注文に関連しません。</span><span class="sxs-lookup"><span data-stu-id="c88a8-109">A **free text invoice** isn't related to a sales order.</span></span> <span data-ttu-id="c88a8-110">この請求書には、勘定科目、自由書式の説明、および自分で入力する売上金額を含む注文明細行が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c88a8-110">It contains order lines that include ledger accounts, free-text descriptions, and a sales amount that you enter.</span></span> <span data-ttu-id="c88a8-111">この種類の請求書では、品目番号を入力することはできません。</span><span class="sxs-lookup"><span data-stu-id="c88a8-111">You can't enter an item number on this kind of invoice.</span></span> <span data-ttu-id="c88a8-112">適切な売上税情報を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c88a8-112">You must enter the appropriate sales tax information.</span></span> <span data-ttu-id="c88a8-113">販売の主勘定は、各請求明細行に表示されます。その明細行は、**自由書式の請求書**ページの**金額の配分**をクリックすると、複数の勘定科目に配分できます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-113">A main account for the sale is indicated on each invoice line, which you can distribute to multiple ledger accounts by clicking **Distribute amounts** on the **Free text invoice** page.</span></span> <span data-ttu-id="c88a8-114">また、顧客残高は自由書式の請求書に使用される転記プロファイルの集計勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-114">Additionally, the customer balance is posted to the summary account from the posting profile that is used for the free text invoice.</span></span>

<span data-ttu-id="c88a8-115">詳細については、「」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c88a8-115">For more information see:</span></span>

[<span data-ttu-id="c88a8-116">自由書式の請求書の作成</span><span class="sxs-lookup"><span data-stu-id="c88a8-116">Create a free text invoice</span></span>](../accounts-receivable/create-free-text-invoice-new.md)

[<span data-ttu-id="c88a8-117">自由書式のテンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="c88a8-117">Create a free text template</span></span>](../accounts-receivable/create-free-text-invoice-template-new.md)

[<span data-ttu-id="c88a8-118">顧客への自由書式の請求書テンプレートの割り当て</span><span class="sxs-lookup"><span data-stu-id="c88a8-118">Assign a free text invoice template to a customer</span></span>](tasks/assign-free-text-invoice-template-customer.md)

[<span data-ttu-id="c88a8-119">定期的な自由書式の請求書の生成と転記</span><span class="sxs-lookup"><span data-stu-id="c88a8-119">Generate and post recurring free text invoices</span></span>](tasks/post-recurring-free-text-invoices.md)


<span data-ttu-id="c88a8-120">**見積送り状**は、請求書が転記される前に実際の請求金額の見積として準備される請求書です。</span><span class="sxs-lookup"><span data-stu-id="c88a8-120">A **pro forma invoice** is an invoice that is prepared as an estimate of the actual invoice amounts before the invoice is posted.</span></span> <span data-ttu-id="c88a8-121">販売注文か自由書式の請求書いずれかの顧客請求書用に見積送り状を印刷できます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-121">You can print a pro forma invoice either for a customer invoice for a sales order or for a free text invoice.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a><span data-ttu-id="c88a8-122">販売注文に基づく個々の顧客請求書の転記および印刷</span><span class="sxs-lookup"><span data-stu-id="c88a8-122">Post and print individual customer invoices that are based on sales orders</span></span>
<span data-ttu-id="c88a8-123">販売注文に基づいて請求書を作成するには、次のプロセスを使用します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-123">Use this process to create an invoice that is based on a sales order.</span></span> <span data-ttu-id="c88a8-124">商品やサービスを提供する前に、顧客に請求することに決めた場合に、これを行うことがあります。</span><span class="sxs-lookup"><span data-stu-id="c88a8-124">You might do this if you decide to invoice the customer before you deliver the goods or services.</span></span> 

<span data-ttu-id="c88a8-125">請求書を転記すると、各品目の**請求残金**の数量は、選択した販売注文の請求された数量の合計で更新されます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-125">When you post an invoice, the **Invoice remainder** quantity for each item is updated with the total of the invoiced quantities from the selected sales order.</span></span> <span data-ttu-id="c88a8-126">販売注文のすべての品目の**請求残金**の数量と**出荷更新待ち**の数量が両方とも 0 (ゼロ) の場合、販売注文のステータスが**請求済**に変更されます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-126">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="c88a8-127">**請求残金**の数量が 0 (ゼロ) でない場合は、販売注文のステータスが変更されず、追加の請求書を入力できます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-127">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span>

<span data-ttu-id="c88a8-128">**すべての販売注文**リスト ページで、販売注文のステータスを確認できます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-128">You can view the status of the sales orders on the **All sales orders** list page.</span></span> <span data-ttu-id="c88a8-129">転記済みの請求書を表示するには、**未処理の顧客請求書**リスト ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-129">Use the **Open customer invoices** list page to view the invoices that you posted.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a><span data-ttu-id="c88a8-130">梱包明細と日付に基づく個々の顧客請求書の転記および印刷</span><span class="sxs-lookup"><span data-stu-id="c88a8-130">Post and print individual customer invoices that are based on packing slips and the date</span></span>
<span data-ttu-id="c88a8-131">販売注文に対して 1 つ以上の梱包明細が転記されている場合に、このプロセスを使用します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-131">Use this process when one or more packing slips have been posted for the sales order.</span></span> <span data-ttu-id="c88a8-132">それらの梱包明細に基づいて顧客請求書が作成され、その数量が反映されます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-132">The customer invoice is based on these packing slips and reflects the quantities from them.</span></span> <span data-ttu-id="c88a8-133">請求書の財務情報は、請求書の転記時に入力する情報に基づいて指定されます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-133">The financial information for the invoice is based on the information that is entered when you post the invoice.</span></span> 

<span data-ttu-id="c88a8-134">特定の販売注文の品目がまだすべて出荷されていなくても、それまでに出荷された梱包明細行の品目に基づいて顧客請求書を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-134">You can create a customer invoice that is based on the packing slip line items that have been shipped to date, even if all the items for a particular sales order haven't yet been shipped.</span></span> <span data-ttu-id="c88a8-135">たとえば、法人で各顧客に対してその月のすべての出荷を網羅した 1 つの請求書を月ごとに発行する場合などにこの機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-135">You might do this if, for example, your legal entity issues one invoice per customer per month that covers all the deliveries that you ship during that month.</span></span> <span data-ttu-id="c88a8-136">各梱包明細は、販売注文の品目の一部またはすべての出荷を表します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-136">Each packing slip represents a partial or complete delivery of the items on the sales order.</span></span> 

<span data-ttu-id="c88a8-137">請求書を転記すると、各品目の**請求残金**の数量は、選択した梱包明細の出荷された数量の合計で更新されます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-137">When you post the invoice, the **Invoice remainder** quantity for each item is updated with the total of the delivered quantities from the selected packing slips.</span></span> <span data-ttu-id="c88a8-138">販売注文のすべての品目の**請求残金**の数量と**出荷更新待ち**の数量が両方とも 0 (ゼロ) の場合、販売注文のステータスが**請求済**に変更されます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-138">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="c88a8-139">**請求残金**の数量が 0 (ゼロ) でない場合は、販売注文のステータスが変更されず、追加の請求書を入力できます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-139">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span> 

<span data-ttu-id="c88a8-140">在庫トランザクションが請求書番号で更新され、販売注文の**行ステータス**フィールドのステータスが**請求済**に変更されます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-140">Inventory transactions are updated with the invoice number, and the status in the **Line status** field on the sales order is changed to **Invoiced**.</span></span> 

<span data-ttu-id="c88a8-141">**すべての販売注文**リスト ページで、販売注文のステータスを確認します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-141">View the status of the sales orders in the **All sales orders** list page.</span></span>

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a><span data-ttu-id="c88a8-142">転記のための販売注文または梱包明細の連結</span><span class="sxs-lookup"><span data-stu-id="c88a8-142">Consolidate sales orders or packing slips for posting</span></span>
<span data-ttu-id="c88a8-143">1 つ以上の販売注文の請求の準備が整っていて、1 つの請求書に連結する場合に、このプロセスを使用します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-143">Use this process when one or more sales orders are ready to be invoiced, and you want to consolidate them into a single invoice.</span></span> 

<span data-ttu-id="c88a8-144">**販売注文**リスト ページの複数の請求書を選択し、**請求書の生成**を使用して連結します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-144">You can select multiple invoices on the **Sales order** list page and then use **Generate invoices** to consolidate them.</span></span> <span data-ttu-id="c88a8-145">**請求の転記**ページで、**注文集計表**設定を変更して、注文番号 (1 つの販売注文に対して複数の梱包明細がある場合) や請求先 (1 つの請求先/元 ID に対して複数の販売注文がある場合) で集計できます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-145">On the **Posting invoice** page, you can change the **Summary order** setting to summarize by order number (where there are multiple packing slips for a single sales order) or by invoice account (where there are multiple sales orders for a single invoice account).</span></span> <span data-ttu-id="c88a8-146">**調整**ボタンを使用すると、**注文集計表**に基づいて販売注文を 1 つの請求書に連結します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-146">Use the **Arrange** button to consolidate sales orders into single invoices, based on the **Summary order** settings.</span></span>

## <a name="additional-settings-that-change-the-posting-behavior"></a><span data-ttu-id="c88a8-147">転記動作を変更する追加設定</span><span class="sxs-lookup"><span data-stu-id="c88a8-147">Additional settings that change the posting behavior</span></span>
<span data-ttu-id="c88a8-148">次のフィールドで転記プロセスの動作を変更します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-148">The following fields change the behavior of the posting process.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c88a8-149">フィールド</span><span class="sxs-lookup"><span data-stu-id="c88a8-149">Field</span></span></th>
<th><span data-ttu-id="c88a8-150">説明</span><span class="sxs-lookup"><span data-stu-id="c88a8-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c88a8-151">件数</span><span class="sxs-lookup"><span data-stu-id="c88a8-151">Quantity</span></span></td>
<td><span data-ttu-id="c88a8-152">ドキュメントの転記の基になる数量を選択します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-152">Select the quantities to base the posting of the document on.</span></span> <span data-ttu-id="c88a8-153">使用できるオプションは、転記するドキュメントのタイプ (梱包明細や請求書など) によって異なります。</span><span class="sxs-lookup"><span data-stu-id="c88a8-153">The options that are available vary, depending on the type of document that you are posting, such as a packing slip or an invoice.</span></span>
<ul>
<li><span data-ttu-id="c88a8-154"><strong>今回出荷数量</strong> – <strong>今回出荷数量</strong> フィールドに入力したすべての数量を選択します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-154"><strong>Deliver now</strong> – Select all quantities that are entered in the <strong>Deliver now</strong> field.</span></span> <span data-ttu-id="c88a8-155">部分注文の確認または配送を行う場合は、このオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-155">Use this option to confirm or deliver a partial order.</span></span></li>
<li><span data-ttu-id="c88a8-156"><strong>ピッキング済</strong> – ピッキングされたすべての数量を選択します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-156"><strong>Picked</strong> – Select all quantities that have been picked.</span></span></li>
<li><span data-ttu-id="c88a8-157"><strong>すべて</strong> – 現在のドキュメント タイプによって更新されていないすべての販売注文数量を選択します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-157"><strong>All</strong> – Select all quantities on the sales order that haven&#39;t yet been updated by the current document type.</span></span></li>
<li><span data-ttu-id="c88a8-158"><strong>梱包明細</strong> – 梱包明細で更新されたすべての数量を選択します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-158"><strong>Packing slip</strong> – Select all quantities that have been updated by a packing slip.</span></span></li>
<li><span data-ttu-id="c88a8-159"><strong>ピッキング済数量で、在庫製品ではありません</strong> – ピッキング済のすべての数量および在庫にないすべての数量を選択します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-159"><strong>Picked quantity and not stocked products</strong> – Select all quantities that have been picked and all product quantities that aren&#39;t stocked.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c88a8-160">転記</span><span class="sxs-lookup"><span data-stu-id="c88a8-160">Posting</span></span></td>
<td><ul>
<li><span data-ttu-id="c88a8-161">発注書の仕訳を行うには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-161">Select this option to journalize the sales order.</span></span></li>
<li><span data-ttu-id="c88a8-162">見積販売注文を印刷するには、このオプションの選択を解除します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-162">Clear this option to print a pro forma sales order.</span></span> <span data-ttu-id="c88a8-163"><strong>注記:</strong> 支払スケジュールに関する契約がある場合、支払スケジュールは見積販売注文に表示されません。</span><span class="sxs-lookup"><span data-stu-id="c88a8-163"><strong>Note:</strong> If you made an agreement for a payment schedule, the payment schedule isn&#39;t shown on the pro forma sales order.</span></span> <span data-ttu-id="c88a8-164">支払スケジュールは実際の販売注文にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-164">Payment schedules are shown only on actual sales orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c88a8-165">遅延選択</span><span class="sxs-lookup"><span data-stu-id="c88a8-165">Late selection</span></span></td>
<td><span data-ttu-id="c88a8-166">後で選択するクエリを適用するには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-166">Select this option to apply the selected query later.</span></span> <span data-ttu-id="c88a8-167">このオプションはバッチ ジョブに使用されます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-167">This option is used for batch jobs.</span></span> <span data-ttu-id="c88a8-168">クエリは、バッチ ジョブの実行時に実行されます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-168">The query is run when the batch job is run.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c88a8-169">数量の削減</span><span class="sxs-lookup"><span data-stu-id="c88a8-169">Reduce quantity</span></span></td>
<td><span data-ttu-id="c88a8-170">出荷済数量が利用可能在庫と等しくなるように、ドキュメントの転記時に自動的に出荷済数量を減らすには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-170">Select this option to automatically reduce the delivered quantity when the document is posted, so that the delivered quantity equals the available inventory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c88a8-171">印刷</span><span class="sxs-lookup"><span data-stu-id="c88a8-171">Print</span></span></td>
<td><span data-ttu-id="c88a8-172">ドキュメントをいつ印刷するかを選択します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-172">Select when to print documents:</span></span>
<ul>
<li><span data-ttu-id="c88a8-173"><strong>現在</strong> – 請求書ごとに更新された後でドキュメントを印刷します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-173"><strong>Current</strong> – Print documents after each invoice has been updated.</span></span></li>
<li><span data-ttu-id="c88a8-174"><strong>変更後</strong> – すべての請求書が更新された時点でドキュメントを印刷します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-174"><strong>After</strong> – Print documents after all the invoices have been updated.</span></span></li>
</ul><span data-ttu-id="c88a8-175">
<strong>注記:</strong> <strong>請求書の印刷</strong>、<strong>確認の印刷</strong>、<strong>ピッキング リストの印刷</strong>、または <strong>梱包明細の印刷</strong> オプションを選択した場合にのみ、<strong>印刷</strong> フィールドを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-175">
<strong>Note:</strong> The <strong>Print</strong> field is available only if you select the <strong>Print invoice</strong>, <strong>Print confirmation</strong>, <strong>Print picking list</strong>, or <strong>Print packing slip</strong> option.</span></span> <span data-ttu-id="c88a8-176">たとえば、<strong>フォームの並べ替え</strong>ページで、請求先/元 ID ごとに情報を並べ替えるようにシステムを設定したとします。</span><span class="sxs-lookup"><span data-stu-id="c88a8-176">For example, on the <strong>Form sorting</strong> page, you have set up the system to sort the information by invoice account.</span></span> <span data-ttu-id="c88a8-177"><strong>変更後</strong> を選択して、請求先/元 ID ごとにドキュメントをバッチ印刷することができます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-177">You can then select <strong>After</strong> to print the documents in a batch that is sorted by invoice account.</span></span> <span data-ttu-id="c88a8-178">それ以外の場合、ドキュメントは処理が完了する前に印刷され、ドキュメントは<strong>フォームの並べ替え</strong>ページ指定された順序では並べ替えられません。</span><span class="sxs-lookup"><span data-stu-id="c88a8-178">Otherwise, the documents are printed before processing is completed, and the documents aren&#39;t sorted in the order that is specified on the <strong>Form sorting</strong> page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c88a8-179">請求書の印刷</span><span class="sxs-lookup"><span data-stu-id="c88a8-179">Print invoice</span></span></td>
<td><span data-ttu-id="c88a8-180">請求書を印刷するには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-180">Select this option to print the invoice.</span></span> <span data-ttu-id="c88a8-181">このオプションをオフにすると、印刷しないで請求書を転記できます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-181">If this option is turned off, you can post an invoice without printing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c88a8-182">電子メールの送信</span><span class="sxs-lookup"><span data-stu-id="c88a8-182">Send e-mail</span></span></td>
<td><span data-ttu-id="c88a8-183">請求書の転記後に電子メール添付ファイルで顧客に販売注文の請求書を送信する場合、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-183">Select this option to send the invoice for a sales order to the customer as an email attachment after the invoice is posted.</span></span> <span data-ttu-id="c88a8-184">添付ファイルは PDF および XML ファイルで送信されます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-184">Attachments are sent as PDF and XML files.</span></span> <span data-ttu-id="c88a8-185">このオプションは、<strong>電子請求書のパラメーター</strong> ページの <strong>CFD (電子請求書) の有効化</strong> オプションを選択している場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-185">This option is available only if you select the <strong>Enable CFD (electronic invoices)</strong> option on the <strong>Electronic invoice parameters</strong> page.</span></span> <span data-ttu-id="c88a8-186"><strong>注記:</strong> (MEX) このコントロールは、基本住所がメキシコにある法人にのみ使用可能です。</span><span class="sxs-lookup"><span data-stu-id="c88a8-186"><strong>Note:</strong> (MEX) This control is available only to legal entities whose primary address is in Mexico.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c88a8-187">印刷管理先の使用</span><span class="sxs-lookup"><span data-stu-id="c88a8-187">Use print management destination</span></span></td>
<td><span data-ttu-id="c88a8-188"><strong>印刷管理の設定</strong>ページのトランザクション、ドキュメント、またはモジュールに対して指定されている印刷設定を使用する場合、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-188">Select this option to use the print settings that are specified for the transaction, document, or module on the <strong>Print management setup</strong> page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c88a8-189">与信限度額の確認</span><span class="sxs-lookup"><span data-stu-id="c88a8-189">Check credit limit</span></span></td>
<td><span data-ttu-id="c88a8-190">与信限度額チェックの実行時に分析する必要のある情報を選択します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-190">Select the information that should be analyzed when a credit limit check is performed.</span></span>
<ul>
<li><span data-ttu-id="c88a8-191"><strong>なし</strong> – 与信限度額の確認に対する要件はありません。</span><span class="sxs-lookup"><span data-stu-id="c88a8-191"><strong>None</strong> – There is no requirement for the credit limit check.</span></span></li>
<li><span data-ttu-id="c88a8-192"><strong>残高</strong> – 与信限度額が顧客残高と照らしてチェックされます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-192"><strong>Balance</strong> – The credit limit is checked against the customer balance.</span></span></li>
<li><span data-ttu-id="c88a8-193"><strong>残高 + 梱包明細または製品受領書</strong> – 顧客残高および出荷に照らして与信限度額をチェックします。</span><span class="sxs-lookup"><span data-stu-id="c88a8-193"><strong>Balance + packing slip or product receipt</strong> – The credit limit is checked against the customer balance and deliveries.</span></span></li>
<li><span data-ttu-id="c88a8-194"><strong>残高 + すべて</strong>: 与信限度額が顧客残高、出荷、および未処理注文に照らしてチェックされます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-194"><strong>Balance+All</strong> – The credit limit is checked against the customer balance, deliveries, and open orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c88a8-195">貸方訂正</span><span class="sxs-lookup"><span data-stu-id="c88a8-195">Credit correction</span></span></td>
<td><span data-ttu-id="c88a8-196">貸方票を伝票トランザクションの借方として表示するには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-196">Select this option to display the credit note as a debit in the voucher transactions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c88a8-197">残余数量を貸方転記</span><span class="sxs-lookup"><span data-stu-id="c88a8-197">Credit remaining quantity</span></span></td>
<td><span data-ttu-id="c88a8-198">貸方票を転記している場合は、このオプションを選択して注文の残余数量を維持します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-198">If you&#39;re posting a credit note, select this option to keep the remaining quantity on order.</span></span> <span data-ttu-id="c88a8-199">このオプションの選択を解除すると、残余数量は 0 (ゼロ) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-199">If this option is cleared, the remaining quantity is set to 0 (zero).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c88a8-200">集計更新</span><span class="sxs-lookup"><span data-stu-id="c88a8-200">Summary update for</span></span></td>
<td><span data-ttu-id="c88a8-201">複数の販売注文を集計する方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-201">Select how multiple sales orders should be summarized:</span></span>
<ul>
<li><span data-ttu-id="c88a8-202"><strong>なし</strong> – 販売注文を集計しません。</span><span class="sxs-lookup"><span data-stu-id="c88a8-202"><strong>None</strong> – Don&#39;t summarize sales orders.</span></span> <span data-ttu-id="c88a8-203">たとえば、販売注文ごとに個別の請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-203">For example, a separate invoice will be created for each sales order.</span></span></li>
<li><span data-ttu-id="c88a8-204"><strong>請求先/元 ID</strong> – <strong>集計更新パラメーター</strong> ページに設定されている条件に基づいて、選択されているすべての注文を集計します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-204"><strong>Invoice account</strong> – Summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span></li>
<li><span data-ttu-id="c88a8-205"><strong>注文</strong>: 選択した範囲の注文を、指定した 1 つの注文に集計します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-205"><strong>Order</strong> – Summarize a selected range of orders into one order that you specify.</span></span> <span data-ttu-id="c88a8-206">注文は、<strong>集計更新パラメーター</strong> ページに設定されている条件に基づいて集計されます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-206">The orders are summarized based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="c88a8-207">このオプションを選択した場合、<strong>販売注文</strong>フィールドの値を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c88a8-207">If you select this option, you must select a value in the <strong>Sales order</strong> field.</span></span></li>
<li><span data-ttu-id="c88a8-208"><strong>自動集計</strong> – <strong>集計の更新</strong>ページで集計更新が指定されている場合、選択されているすべての注文が、<strong>集計更新パラメーター</strong> ページに設定されている条件に基づいて集計されます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-208"><strong>Automatic summary</strong> – If summary updates have been specified on the <strong>Summary update</strong> page, summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="c88a8-209">集計更新が指定されていない場合、注文は個別に転記されます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-209">If summary updates haven&#39;t been specified, the order is posted separately.</span></span></li>
<li><span data-ttu-id="c88a8-210"><strong>梱包明細</strong> – 選択した範囲の注文を、梱包明細ごとに 1 つの請求書に集計します。</span><span class="sxs-lookup"><span data-stu-id="c88a8-210"><strong>Packing slip</strong> – Summarize a selected range of orders into one invoice for each packing slip.</span></span> <span data-ttu-id="c88a8-211">このオプションは、<strong>数量</strong> フィールドで <strong>梱包明細</strong>が選択されている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="c88a8-211">This option is available only if <strong>Packing slip</strong> is selected in the <strong>Quantity</strong> field.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>





