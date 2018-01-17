---
title: "仕入先請求書の概要"
description: "この記事は、仕入先請求書に関する一般情報を示します。 仕入先請求書は、受領した製品とサービスに対する支払請求です。 仕入先請求書は、進行中のサービスの請求書を表すことができます。または特定の品目およびサービスの発注書に基づくことができます。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13971
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 3d02b2ee0ee748546158bce1094d2b343afef7c5
ms.contentlocale: ja-jp
ms.lasthandoff: 01/17/2018

---

# <a name="vendor-invoices-overview"></a><span data-ttu-id="84720-105">仕入先請求書の概要</span><span class="sxs-lookup"><span data-stu-id="84720-105">Vendor invoices overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="84720-106">この記事は、仕入先請求書に関する一般情報を示します。</span><span class="sxs-lookup"><span data-stu-id="84720-106">This article provides general information about vendor invoices.</span></span> <span data-ttu-id="84720-107">仕入先請求書は、受領した製品とサービスに対する支払請求です。</span><span class="sxs-lookup"><span data-stu-id="84720-107">Vendor invoices are requests for payment for products and services that were received.</span></span> <span data-ttu-id="84720-108">仕入先請求書は、進行中のサービスの請求書を表すことができます。または特定の品目およびサービスの発注書に基づくことができます。</span><span class="sxs-lookup"><span data-stu-id="84720-108">Vendor invoices can represent a bill for ongoing services, or they can be based on purchase orders for specific items and services.</span></span> 

<a name="vendor-invoices"></a><span data-ttu-id="84720-109">仕入先請求書</span><span class="sxs-lookup"><span data-stu-id="84720-109">Vendor invoices</span></span>
---------------

<span data-ttu-id="84720-110">発注書からの仕入先請求書は、仕入先に配置された発注書に従って製品またはサービスを受けるときに生成される請求書です。</span><span class="sxs-lookup"><span data-stu-id="84720-110">A vendor invoice from a purchase order is an invoice that is produced when products or services are received according to a purchase order that was placed with a vendor.</span></span> <span data-ttu-id="84720-111">これには、ヘッダーと品目、またはサービスの 1 つ以上の明細行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="84720-111">The vendor invoice contains a header, and one or more lines for items or services.</span></span> <span data-ttu-id="84720-112">仕入先請求書は、発注書から製品受領書、仕入先請求書のサイクルを完了します。</span><span class="sxs-lookup"><span data-stu-id="84720-112">A vendor invoice completes the cycle from purchase order to product receipt to vendor invoice.</span></span> 

<span data-ttu-id="84720-113">発注書に結合されている仕入先請求書があっても、購買注文明細行に対応しない明細行も仕入先請求書に含めることができます。</span><span class="sxs-lookup"><span data-stu-id="84720-113">Although some vendor invoices are connected to a purchase order, vendor invoices can also contain lines that don't correspond to purchase order lines.</span></span> <span data-ttu-id="84720-114">どの発注書にも関連付けられていない仕入先請求書も作成できます。</span><span class="sxs-lookup"><span data-stu-id="84720-114">You can also create vendor invoices that aren't associated with any purchase order.</span></span> <span data-ttu-id="84720-115">これらの仕入先請求書は、公共料金など進行中のサービスを表す場合があり、追加時に発注書を参照する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="84720-115">These vendor invoices might represent ongoing services, such as a utility bill, and you don't have to reference a purchase order when you add them.</span></span> 

<span data-ttu-id="84720-116">仕入先請求書を入力するいくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="84720-116">There are several ways to enter a vendor invoice:</span></span>

-   <span data-ttu-id="84720-117">仕入先仕入帳を使用すると、発注書を参照しない請求書をすばやく入力して経費を計上できます。</span><span class="sxs-lookup"><span data-stu-id="84720-117">The vendor invoice register lets you quickly enter invoices that don't reference a purchase order, so that you can accrue the expense.</span></span> <span data-ttu-id="84720-118">仕入先請求書承認仕訳帳を使用して、それらの請求書を選択し、仕入先の残高に転記して見越計上を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="84720-118">By using the vendor invoice approval journal, you can select those invoices and post them to the vendor balance to reverse the accrual.</span></span>
-   <span data-ttu-id="84720-119">仕入先請求仕訳帳を使用すると、発注書を参照しない請求書をすばやくワンステップで入力できます。</span><span class="sxs-lookup"><span data-stu-id="84720-119">The vendor invoice journal lets you quickly enter invoices that don't reference a purchase order, in a single step.</span></span>
-   <span data-ttu-id="84720-120">仕入先請求管理グループとともに仕入先仕入帳を使用すると、請求書をすばやく入力して経費を計上できます。</span><span class="sxs-lookup"><span data-stu-id="84720-120">Together with the vendor invoice pool, the vendor invoice register lets you quickly enter invoices to accrue the expense.</span></span> <span data-ttu-id="84720-121">後で発注書を開いて、経費勘定に対する請求書を転記することができます。</span><span class="sxs-lookup"><span data-stu-id="84720-121">You can open the associated purchase orders later to post the invoice against the expense account.</span></span>
-   <span data-ttu-id="84720-122">**未処理の仕入先請求書**ページおよび**保留中の仕入先請求書**ページで、確認済発注書から仕入先請求書を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="84720-122">The **Open vendor invoices** and **Pending vendor invoices** pages let you create vendor invoices from confirmed purchase orders.</span></span>

<span data-ttu-id="84720-123">次のディスカッションは、発注書から仕入先請求書を作成する場合の**未処理の仕入先請求書**ページまたは**保留中の仕入先請求書**ページの使用方法の詳細について示しています。</span><span class="sxs-lookup"><span data-stu-id="84720-123">The following discussion provide more information about how to use the **Open vendor invoices** or **Pending vendor invoices** page to create a vendor invoice from a purchase order.</span></span>

## <a name="understanding-invoice-line-quantities"></a><span data-ttu-id="84720-124">請求明細行の数量の理解</span><span class="sxs-lookup"><span data-stu-id="84720-124">Understanding invoice line quantities</span></span>
<span data-ttu-id="84720-125">関連する発注書から仕入先請求書を開くと、請求明細行が発注書から作成されます。</span><span class="sxs-lookup"><span data-stu-id="84720-125">When you open a vendor invoice from a related purchase order, invoice lines are created from the purchase order.</span></span> <span data-ttu-id="84720-126">既定では、数量は製品受領書の数量から取得されます。</span><span class="sxs-lookup"><span data-stu-id="84720-126">By default, the quantities are taken from the product receipt quantity.</span></span> <span data-ttu-id="84720-127">ただし、次の既定の動作を使用できます。</span><span class="sxs-lookup"><span data-stu-id="84720-127">However, you can use any of the following default behaviors:</span></span>

-   <span data-ttu-id="84720-128">**入庫数量** – 部分出荷にこのオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="84720-128">**Receive now quantity** – Use this option for partial shipments.</span></span> <span data-ttu-id="84720-129">[**数量**] フィールドの既定値は、発注書の [**今回受入**] の数量フィールドから取得されます。</span><span class="sxs-lookup"><span data-stu-id="84720-129">The default value in the **Quantity** field is taken from the **Receive now** quantity field on the purchase order.</span></span>
-   <span data-ttu-id="84720-130">**注文済数量** – 出荷全体にこのオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="84720-130">**Ordered quantity** – Use this option for complete shipments.</span></span> <span data-ttu-id="84720-131">[**数量**] フィールドの既定値は、発注書の [**注文済**] 数量フィールドから取得されます。</span><span class="sxs-lookup"><span data-stu-id="84720-131">The default value in the **Quantity** field is taken from the **Ordered** quantity field on the purchase order.</span></span>
-   <span data-ttu-id="84720-132">**登録済数量** – **品目モデル グループ** ページで指定した登録が品目に必要な場合にこのオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="84720-132">**Registered quantity** – Use this option if the item requires registration, as specified on the **Item model groups** page.</span></span> <span data-ttu-id="84720-133">[**数量**] フィールドの既定値は登録済の現物更新数量です。</span><span class="sxs-lookup"><span data-stu-id="84720-133">The default value in the **Quantity** field is the physical update quantity that has been registered.</span></span>
-   <span data-ttu-id="84720-134">**製品受領書の数量** – 注文に対する製品受領書をすでに受領している場合にこのオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="84720-134">**Product receipt quantity** – Use this option if a product receipt has already been received for the order.</span></span> <span data-ttu-id="84720-135">[**数量**] フィールドの既定値は、利用可能な製品受領書の合計数量から取得されます。</span><span class="sxs-lookup"><span data-stu-id="84720-135">The default value in the **Quantity** field is taken from the total quantity of available product receipts.</span></span>
-   <span data-ttu-id="84720-136">**登録された数量とサービス** – 在庫品目や在庫のない品目に対する数量が着荷仕訳帳に登録されている場合にこのオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="84720-136">**Registered quantity and services** – Use this option if quantities have been registered in arrival journals for stocked items or items that aren't stocked.</span></span> <span data-ttu-id="84720-137">登録済みかどうかに関係なく、このオプションにはサービスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="84720-137">This option also includes services, regardless of whether they are registered.</span></span>

<span data-ttu-id="84720-138">法人が請求書照合を使用している場合、[**製品受領書の数量の照合**] 列に数量の照合結果を表示できます。</span><span class="sxs-lookup"><span data-stu-id="84720-138">If your legal entity uses invoice matching, you can view the results of the quantity matching in the **Product receipt quantity match** column.</span></span> <span data-ttu-id="84720-139">また、[**確認**] タブの [**照合の詳細**] メニュー コマンドを使用して、数量の照合結果を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="84720-139">You can also use the **Matching details** menu command on the **Review** tab to view the results of the quantity matching.</span></span>

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a><span data-ttu-id="84720-140">発注書にない明細行の追加</span><span class="sxs-lookup"><span data-stu-id="84720-140">Adding a line that wasn't on the purchase order</span></span>
<span data-ttu-id="84720-141">仕入先請求書には、発注書にない新しい明細行を追加できます。</span><span class="sxs-lookup"><span data-stu-id="84720-141">You can add a new line that wasn't on the purchase order to the vendor invoice.</span></span> <span data-ttu-id="84720-142">品目番号または調達カテゴリを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84720-142">You must select an item number or procurement category.</span></span> <span data-ttu-id="84720-143">次に、明細行に数量、価格、および金額を追加できます。</span><span class="sxs-lookup"><span data-stu-id="84720-143">You can then add quantities, prices, and amounts to the line.</span></span> <span data-ttu-id="84720-144">明細行は、請求合計の照合ポリシーにのみ含まれます。</span><span class="sxs-lookup"><span data-stu-id="84720-144">The line will be included only in matching policies for invoice totals.</span></span>

## <a name="submitting-a-vendor-invoice-for-review"></a><span data-ttu-id="84720-145">確認用の仕入先請求書の送信</span><span class="sxs-lookup"><span data-stu-id="84720-145">Submitting a vendor invoice for review</span></span>
<span data-ttu-id="84720-146">組織は、仕入先請求書の確認プロセスの管理にワークフローを使用する場合があります。</span><span class="sxs-lookup"><span data-stu-id="84720-146">Your organization might use workflows to manage the review process for vendor invoices.</span></span> <span data-ttu-id="84720-147">ワークフローの確認は、請求書ヘッダー、請求書明細行、または両方で要求できます。</span><span class="sxs-lookup"><span data-stu-id="84720-147">Workflow review can be required for the invoice header, the invoice line, or both.</span></span> <span data-ttu-id="84720-148">ワークフローの制御は、制御をクリックするときにフォーカスがある場所に応じて、ヘッダーまたは明細行に適用されます。</span><span class="sxs-lookup"><span data-stu-id="84720-148">The workflow controls apply to the header or the line, depending on where the focus is when you click the control.</span></span> <span data-ttu-id="84720-149">[**転記**] ボタンの代わりに、確認プロセスで仕入先請求書を送る場合に使用できる [**送信**] ボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="84720-149">Instead of the **Post** button, you will see a **Submit** button that you can use to send the vendor invoice through the review process.</span></span>

## <a name="matching-vendor-invoices-to-product-receipts"></a><span data-ttu-id="84720-150">仕入先請求書の製品受領書との照合</span><span class="sxs-lookup"><span data-stu-id="84720-150">Matching vendor invoices to product receipts</span></span>
<span data-ttu-id="84720-151">仕入先請求書の情報を入力および保存し、請求書の明細行を製品受領書の明細行と照合できます。</span><span class="sxs-lookup"><span data-stu-id="84720-151">You can enter and save information for vendor invoices, and you can match invoice lines to product receipt lines.</span></span> <span data-ttu-id="84720-152">また、明細行の部分的な数量を照合できます。</span><span class="sxs-lookup"><span data-stu-id="84720-152">You can also match partial quantities for a line.</span></span> 

<span data-ttu-id="84720-153">特定の発注書のすべての品目がまだ入荷していなくても、それまでに入荷した製品受領書明細行の品目に基づいて仕入先請求書を作成できます。</span><span class="sxs-lookup"><span data-stu-id="84720-153">You can create a vendor invoice that is based on the product receipt line items that have been received to date, even if all the items for a particular purchase order haven't yet been received.</span></span> <span data-ttu-id="84720-154">たとえば、その月のすべての仕入先からの配送を記載した 1 つの請求書が、仕入先から月ごとに送られてくる場合などにこのオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="84720-154">For example, you might use this option if a vendor sends one invoice per month that covers all the deliveries that the vendor shipped during that month.</span></span> <span data-ttu-id="84720-155">各製品受領書は、発注書の品目の一部またはすべての配送を表します。</span><span class="sxs-lookup"><span data-stu-id="84720-155">Each product receipt represents a partial or complete delivery of the items on the purchase order.</span></span> 

<span data-ttu-id="84720-156">請求書を転記すると、各品目の [**請求残金**] の数量は、選択した製品受領書の受領した数量の合計で更新されます。</span><span class="sxs-lookup"><span data-stu-id="84720-156">When you post the invoice, the **Invoice remainder** quantity for each item is updated with the total of the received quantities from the selected product receipts.</span></span> <span data-ttu-id="84720-157">発注書のすべての品目の [**請求残金**] の数量と [**出荷更新待ち**] の数量が両方とも 0 (ゼロ) の場合、発注書のステータスが [**請求済**] に変更されます。</span><span class="sxs-lookup"><span data-stu-id="84720-157">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the purchase order are 0 (zero), the status of the purchase order is changed to **Invoiced**.</span></span> <span data-ttu-id="84720-158">[**請求残金**] の数量が 0 (ゼロ) でない場合は、発注書のステータスが変更されず、追加の請求書を入力できます。</span><span class="sxs-lookup"><span data-stu-id="84720-158">If the **Invoice remainder** quantity isn't 0, the status of the purchase order remains unchanged, and additional invoices can be entered for it.</span></span>

<span data-ttu-id="84720-159">このオプションでは、発注書に対して少なくとも 1 つの製品受領書が転記されていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="84720-159">This option assumes that at least one product receipt has been posted for the purchase order.</span></span> <span data-ttu-id="84720-160">それらの製品受領書に基づいて仕入先請求書が作成され、その数量が反映されます。</span><span class="sxs-lookup"><span data-stu-id="84720-160">The vendor invoice is based on these product receipts and reflects the quantities from them.</span></span> <span data-ttu-id="84720-161">請求書の財務情報は、請求書の転記時に入力する情報に基づいて指定されます。</span><span class="sxs-lookup"><span data-stu-id="84720-161">The financial information for the invoice is based on the information that is entered when you post the invoice.</span></span>

<span data-ttu-id="84720-162">詳細については、[仕入先の請求書を記録し、入庫済数量と一致](../accounts-receivable/tasks/record-vendor-invoice-match-against-received-quantity.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84720-162">For more information, see [Record vendor invoice and match against received quantity](../accounts-receivable/tasks/record-vendor-invoice-match-against-received-quantity.md).</span></span>

## <a name="working-with-multiple-invoices"></a><span data-ttu-id="84720-163">複数の請求書の処理</span><span class="sxs-lookup"><span data-stu-id="84720-163">Working with multiple invoices</span></span>

<span data-ttu-id="84720-164">複数の請求書で同時に作業し、それらの請求書をすべて同時に転記できます。</span><span class="sxs-lookup"><span data-stu-id="84720-164">You can work with multiple invoices at the same time and post them all at the same time.</span></span> <span data-ttu-id="84720-165">複数の請求書を作成する必要がある場合、**保留中の仕入先請求書**ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="84720-165">If you must create multiple invoices, use the **Pending vendor invoices** page.</span></span> <span data-ttu-id="84720-166">複数の仕入先請求書の転記および印刷が必要な場合、請求書承認仕訳帳ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="84720-166">If you must post and print multiple vendor invoices, use the invoice approval journal page.</span></span> <span data-ttu-id="84720-167">請求書承認仕訳帳を使用している場合、発注書に対して少なくとも 1 つの製品受領書を転記し、発注書に対する請求書を仕入帳に転記している必要があります。</span><span class="sxs-lookup"><span data-stu-id="84720-167">If you're using the invoice approval journal, at least one product receipt must be posted for the purchase order, and an invoice for the purchase order must be posted in an invoice register.</span></span> <span data-ttu-id="84720-168">請求書の財務情報は、仕入帳に転記された請求書から取得されます。</span><span class="sxs-lookup"><span data-stu-id="84720-168">The financial information for the invoice comes from the invoice that was posted in the register.</span></span>


<span data-ttu-id="84720-169">詳細については、「」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84720-169">For more information see:</span></span>

 - [<span data-ttu-id="84720-170">仕入先請求ポリシーの設定</span><span class="sxs-lookup"><span data-stu-id="84720-170">Set up vendor invoice policies</span></span>](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md) 

 - [<span data-ttu-id="84720-171">仕入先請求書を使用した買掛金勘定への請求書データの入力</span><span class="sxs-lookup"><span data-stu-id="84720-171">Key invoice data into accounts payable using a vendor invoice</span></span>](tasks/key-invoice-data-ap-system-vendor-invoice.md)
 
 - [<span data-ttu-id="84720-172">承認仕訳帳を使用した買掛金勘定への請求書データの入力</span><span class="sxs-lookup"><span data-stu-id="84720-172">Key invoice data into accounts payable using an approval journal</span></span>](tasks/key-invoice-data-into-ap-system-approval-journal.md)
  
 - [<span data-ttu-id="84720-173">請求管理グループを使用した AP システムへの請求書データの入力</span><span class="sxs-lookup"><span data-stu-id="84720-173">Key invoice data into the AP system using invoice pool</span></span>](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
 
 - [<span data-ttu-id="84720-174">請求仕訳帳の仕入先請求書の記録</span><span class="sxs-lookup"><span data-stu-id="84720-174">Record a vendor invoice in the invoice journal</span></span>](tasks/record-vendor-invoice-invoice-journal.md)


