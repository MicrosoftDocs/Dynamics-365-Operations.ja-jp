---
title: "販売注文の Sales、Finance and Operations 間の直接同期"
description: "このトピックでは、Microsoft Dynamics 365 for Sales と Microsoft Dynamics 365 for Finance and Operations との間で、販売注文の直接同期を実行させるために使用されるテンプレートと基本的なタスクについて説明します。"
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: e26244ffc380291a40edfbd2c2cb5911b0d8b3cb
ms.contentlocale: ja-jp
ms.lasthandoff: 03/26/2018

---

# <a name="synchronization-of-sales-orders-directly-between-sales-and-finance-and-operations"></a><span data-ttu-id="e2753-103">販売注文の Sales、Finance and Operations 間の直接同期</span><span class="sxs-lookup"><span data-stu-id="e2753-103">Synchronization of sales orders directly between Sales and Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e2753-104">このトピックでは、Microsoft Dynamics 365 for Sales と Microsoft Dynamics 365 for Finance and Operations との間で、販売注文の直接同期を実行させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e2753-104">The topic discusses the templates and underlying tasks that are used to run synchronization of sales orders directly between Microsoft Dynamics 365 for Sales and Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="e2753-105">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="e2753-105">Templates and tasks</span></span>

<span data-ttu-id="e2753-106">利用可能なテンプレートにアクセスするには、[PowerApps 管理者センター](https://preview.admin.powerapps.com/dataintegration) を開きます。</span><span class="sxs-lookup"><span data-stu-id="e2753-106">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="e2753-107">**プロジェクト**を選択した後、右上隅にある **新しいプロジェクト** を選択してパブリック テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="e2753-107">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="e2753-108">Finance and Operations と Sales の間での販売注文の直接同期の実行には、以下のテンプレートと基本的なタスクが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e2753-108">The following templates and underlying tasks are used to run synchronization of sales orders directly between Sales and Finance and Operations:</span></span>

- <span data-ttu-id="e2753-109">**データ統合でのテンプレートの名前:**</span><span class="sxs-lookup"><span data-stu-id="e2753-109">**Names of the templates in Data integration:**</span></span> 

    - <span data-ttu-id="e2753-110">販売注文 (Sales から Finance and Operations) - ダイレクト</span><span class="sxs-lookup"><span data-stu-id="e2753-110">Sales Orders (Sales to Fin and Ops) - Direct</span></span>
    - <span data-ttu-id="e2753-111">販売注文 (Finance and Operations から Sales) - ダイレクト</span><span class="sxs-lookup"><span data-stu-id="e2753-111">Sales Orders (Fin and Ops to Sales) - Direct</span></span>

- <span data-ttu-id="e2753-112">**データ統合プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="e2753-112">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="e2753-113">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="e2753-113">OrderHeader</span></span>
    - <span data-ttu-id="e2753-114">OrderLine</span><span class="sxs-lookup"><span data-stu-id="e2753-114">OrderLine</span></span>

<span data-ttu-id="e2753-115">販売請求書ヘッダーと明細行を同期させるには、次の同期タスクが必要です。</span><span class="sxs-lookup"><span data-stu-id="e2753-115">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="e2753-116">製品 (Finance and Operations から Sales) - 直接</span><span class="sxs-lookup"><span data-stu-id="e2753-116">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="e2753-117">勘定 (Sales から Finance and Operations) - 直接(使用されている場合)</span><span class="sxs-lookup"><span data-stu-id="e2753-117">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="e2753-118">顧客への連絡先 (Sales から Finance and Operations) - ダイレクト (使用されている場合)</span><span class="sxs-lookup"><span data-stu-id="e2753-118">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="e2753-119">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="e2753-119">Entity set</span></span>

| <span data-ttu-id="e2753-120">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e2753-120">Finance and Operations</span></span>  | <span data-ttu-id="e2753-121">売上</span><span class="sxs-lookup"><span data-stu-id="e2753-121">Sales</span></span>             |
|-------------------------|-------------------|
| <span data-ttu-id="e2753-122">CDS 販売注文ヘッダー</span><span class="sxs-lookup"><span data-stu-id="e2753-122">CDS sales order headers</span></span> | <span data-ttu-id="e2753-123">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="e2753-123">SalesOrders</span></span>       |
| <span data-ttu-id="e2753-124">CDS 販売注文明細行</span><span class="sxs-lookup"><span data-stu-id="e2753-124">CDS sales order lines</span></span>   | <span data-ttu-id="e2753-125">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="e2753-125">SalesOrderDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="e2753-126">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="e2753-126">Entity flow</span></span>

<span data-ttu-id="e2753-127">**販売注文 (Sales からFinance and Operations) - 直接** テンプレートに基づいたプロジェクトに対して **プロジェクトの実行** が発生する場合、Sales で作成された販売注文が Finance and Operations に同期されます。</span><span class="sxs-lookup"><span data-stu-id="e2753-127">Sales orders are created in Sales and synchronized to Finance and Operations when **Run project** is triggered for a project based on the **Sales Orders (Sales to Fin and Ops) - Direct** template.</span></span> <span data-ttu-id="e2753-128">全ての**受注製品**が外部で管理される製品で構成されている場合にのみ、Sales からの販売注文を同期できます。</span><span class="sxs-lookup"><span data-stu-id="e2753-128">You can only activate and synchronize orders from Sales if all **Order Products** consist of products that are externally maintained.</span></span> <span data-ttu-id="e2753-129">したがって、リスト外製品は存在しません。</span><span class="sxs-lookup"><span data-stu-id="e2753-129">Therefore, there can be no write-in products.</span></span> <span data-ttu-id="e2753-130">注文を有効にすると、販売注文はユーザー インターフェイス (UI) で読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="e2753-130">After the order is activated, the sales order becomes read-only in the user interface (UI).</span></span> <span data-ttu-id="e2753-131">この時点で、更新は Finance and Operations から行われます。</span><span class="sxs-lookup"><span data-stu-id="e2753-131">At that point, the updates are made from Finance and Operations.</span></span> <span data-ttu-id="e2753-132">販売注文が **確認済** 状態となった後に、**販売注文 (Finance and Operations から Sales) － 直接** テンプレートに基づいたプロジェクトは Finance and Operations から Sales に更新またはフルフィルメントの状態を同期するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="e2753-132">After the sales order has a status of **Confirmed**, the a project based on the **Sales Orders (Fin and Ops to Sales) - Direct** template can be used to synchronize updates or fulfillment status from Finance and Operations to Sales.</span></span>

<span data-ttu-id="e2753-133">Sales で注文を作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e2753-133">You don't have to create orders in Sales.</span></span> <span data-ttu-id="e2753-134">代わりに、Finance and Operations で新しい販売注文を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="e2753-134">You can create new sales orders in Finance and Operations instead.</span></span> <span data-ttu-id="e2753-135">販売注文が**確認済**のステータスになった後、前の段落で説明するように Sales に同期されます。</span><span class="sxs-lookup"><span data-stu-id="e2753-135">After a sales order has a status of **Confirmed**, it's synchronized to Sales as described in the previous paragraph.</span></span>

<span data-ttu-id="e2753-136">Finance and Operations では、テンプレートのフィルタは関連する販売注文のみが同期に含まれていることを保証します。</span><span class="sxs-lookup"><span data-stu-id="e2753-136">In Finance and operations, filters in the template help guarantee that only the relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="e2753-137">販売注文では、受注顧客と請求顧客の両方が Sales から生成されて同期に含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2753-137">On the sales order, both the ordering customer and the invoicing customer have to originate from Sales to be included in the synchronization.</span></span> <span data-ttu-id="e2753-138">Finance and Operations で、[**OrderingCustomerIsExternallyMaintained**] および [**InvoiceCustomerIsExternallyMaintained**] フィールドは、データ エンティティからの販売注文をフィルタするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e2753-138">In Finance and Operations, the **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** fields are used to filter sales orders from the data entities.</span></span>
- <span data-ttu-id="e2753-139">Finance and Operations で [販売注文] を確定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2753-139">The sales order in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="e2753-140">[**出荷済**] や [**請求済**] など、確認済の販売注文または処理ステータスの高い販売注文のみが Sales に同期されます。</span><span class="sxs-lookup"><span data-stu-id="e2753-140">Only confirmed sales orders or sales orders that have a higher processing status, such as **Shipped** or **Invoiced**, are synchronized to Sales.</span></span>
- <span data-ttu-id="e2753-141">販売注文を作成または変更した後、Finance and Operations で [**販売合計の計算**] のバッチ ジョブを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2753-141">After a sales order is created or modified, the **Calculate sales totals** batch job in Finance and Operations must be run.</span></span> <span data-ttu-id="e2753-142">販売合計が計算された販売注文のみが Sales に同期されます。</span><span class="sxs-lookup"><span data-stu-id="e2753-142">Only sales orders where sales totals are calculated will be synchronized to Sales.</span></span>

## <a name="freight-tax"></a><span data-ttu-id="e2753-143">運賃税</span><span class="sxs-lookup"><span data-stu-id="e2753-143">Freight tax</span></span>

<span data-ttu-id="e2753-144">Sales は、明細行レベルで税が格納されるため、ヘッダー レベルでの税をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="e2753-144">Sales doesn't support tax at the header level, because tax is stored at the line level.</span></span> <span data-ttu-id="e2753-145">運賃税など Finance and Operations からヘッダー レベルでの税をサポートするためには、システムは **運賃税** と呼ぶリスト外製品として税を Sales に同期して、Finance and Operations からの税額を含めます。</span><span class="sxs-lookup"><span data-stu-id="e2753-145">To support tax at the header level from Finance and Operations, such as tax on freight, the system synchronizes tax to Sales as a write-in product that is named **Freight Tax**, and that has the tax amount from Finance and Operations.</span></span> <span data-ttu-id="e2753-146">これにより、Sales での標準価の計算は、Finance and Operations からヘッダー レベルで税がある場合でも合計金額として使用できます。</span><span class="sxs-lookup"><span data-stu-id="e2753-146">In this way, the standard price calculation in Sales can be used for totals, even when there is tax at the header level from Finance and Operations.</span></span>

## <a name="discount-calculation-and-rounding"></a><span data-ttu-id="e2753-147">割引計算と丸め</span><span class="sxs-lookup"><span data-stu-id="e2753-147">Discount calculation and rounding</span></span>

<span data-ttu-id="e2753-148">Sales での割引計算モデルは、Finance and Operations の割引計算モデルとは異なります。</span><span class="sxs-lookup"><span data-stu-id="e2753-148">The discount calculation model in Sales differs from the discount calculation model in Finance and Operations.</span></span> <span data-ttu-id="e2753-149">Finance and Operations では、販売注文明細行の最終的な割引金額は、割引額と割引率の組み合わせの結果です。</span><span class="sxs-lookup"><span data-stu-id="e2753-149">In Finance and Operations, the final discount amount on a sales line can be the result of a combination of discount amounts and discount percentages.</span></span> <span data-ttu-id="e2753-150">この最終割引額をライン上の数量で割ると、丸め処理が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e2753-150">If this final discount amount is divided by the quantity on the line, rounding can occur.</span></span> <span data-ttu-id="e2753-151">ただし、この丸め処理単位の割引額が Sales に同期されている場合は、この丸め処理は考慮されません。</span><span class="sxs-lookup"><span data-stu-id="e2753-151">However, this rounding isn't considered if a rounded per-unit discount amount is synchronized to Sales.</span></span> <span data-ttu-id="e2753-152">Finance and Operations の販売ラインからの全額割引が Sales に正しく同期されるようにするには、全額を明細行の数量で除算せずに同期させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2753-152">To help guarantee that the full discount amount from a sales line in Finance and Operations is correctly synchronized to Sales, the full amount must be synchronized without being divided by the line quantity.</span></span> <span data-ttu-id="e2753-153">したがって、Sales で **割引の計算方法** を **明細行品目** として定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2753-153">Therefore, you must define the **Discount calculation method** as **Line item** in Sales.</span></span>

<span data-ttu-id="e2753-154">販売注文行が Sales から Finance and Operations に同期される場合、明細行全体の割引額が使用されます。</span><span class="sxs-lookup"><span data-stu-id="e2753-154">When a sales order line is synchronized from Sales to Finance and Operations, the full line discount amount is used.</span></span> <span data-ttu-id="e2753-155">Finance and Operations には、明細行の完全な割引金額を格納できるフィールドがないため、金額は数量で除算されて、[**行割引**] フィールドに格納されます。</span><span class="sxs-lookup"><span data-stu-id="e2753-155">Because Finance and Operations has no field that can store the full discount amount for a line, the amount is divided by the quantity and stored in the **Line discount** field.</span></span> <span data-ttu-id="e2753-156">この区分中に発生する丸め処理は販売注文明細行の**売上諸掛**フィールドに格納されます。</span><span class="sxs-lookup"><span data-stu-id="e2753-156">Any rounding that occurs in this division is stored in the **Sales charges** field on the sales line.</span></span>

### <a name="example"></a><span data-ttu-id="e2753-157">例</span><span class="sxs-lookup"><span data-stu-id="e2753-157">Example</span></span>

<span data-ttu-id="e2753-158">**Sales から Finance and Operations への同期**</span><span class="sxs-lookup"><span data-stu-id="e2753-158">**Synchronization from Sales to Finance and Operations**</span></span>

- <span data-ttu-id="e2753-159">[**Sales:**] 数量 = 3、行あたりの割引 = 10.00 USD</span><span class="sxs-lookup"><span data-stu-id="e2753-159">**Sales:** Quantity = 3, per-line discount = $10.00</span></span>
- <span data-ttu-id="e2753-160">**Finance and Operations:** 数量 = 3、行割引金額 = 3.33 USD、販売手数料 = -0.01 USD</span><span class="sxs-lookup"><span data-stu-id="e2753-160">**Finance and Operations:** Quantity = 3, line discount amount = $3.33, sales charge = -$0.01</span></span> 

<span data-ttu-id="e2753-161">**Finance and Operations から Sales への同期**</span><span class="sxs-lookup"><span data-stu-id="e2753-161">**Synchronization from Finance and Operations to Sales**</span></span>

- <span data-ttu-id="e2753-162">**Finance and Operations:** 数量 = 3、行割引金額 = 3.33 USD、販売手数料 = -0.01 USD</span><span class="sxs-lookup"><span data-stu-id="e2753-162">**Finance and Operations:** Quantity = 3, line discount amount = $3.33, sales charge = -$0.01</span></span>
- <span data-ttu-id="e2753-163">**Sales:** 数量 = 3、行あたりの割引 = (3 × 3.33 USD) + 0.01 USD = 10.00 USD</span><span class="sxs-lookup"><span data-stu-id="e2753-163">**Sales:** Quantity = 3, per-line discount = (3 × $3.33) + $0.01 = $10.00</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="e2753-164">売上の見込顧客を現金化するソリューション</span><span class="sxs-lookup"><span data-stu-id="e2753-164">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="e2753-165">新しいフィールドが [**注文**] エンティティに追加され、ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e2753-165">New fields have been added to the **Order** entity and appear on the page:</span></span>

- <span data-ttu-id="e2753-166">[**外部で管理**] - 注文が Finance and Operations から来る場合、このオプションを [**はい**] に設定します。</span><span class="sxs-lookup"><span data-stu-id="e2753-166">**Is Maintained Externally** – Set this option to **Yes** when the order is coming from Finance and Operations.</span></span>
- <span data-ttu-id="e2753-167">[**処理状態**] - このフィールドには、Finance and Operations の注文の処理状態が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e2753-167">**Processing status** – This field shows the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="e2753-168">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e2753-168">The following values are available:</span></span>

    - <span data-ttu-id="e2753-169">**ドラフト** – Sales で受注が作成される場合の初期ステータス。</span><span class="sxs-lookup"><span data-stu-id="e2753-169">**Draft** – The initial status when an order is created in Sales.</span></span> <span data-ttu-id="e2753-170">Sales では、この処理ステータスの注文のみ編集することができます。</span><span class="sxs-lookup"><span data-stu-id="e2753-170">In Sales, only orders with this processing status can be edited.</span></span>
    - <span data-ttu-id="e2753-171">**有効** – **有効**ボタンを使用すると、受注後のステータスが Sales で有効になります。</span><span class="sxs-lookup"><span data-stu-id="e2753-171">**Active** – The status after the order is activated in Sales by using the **Activate** button.</span></span>
    - <span data-ttu-id="e2753-172">**確認済**</span><span class="sxs-lookup"><span data-stu-id="e2753-172">**Confirmed**</span></span>
    - <span data-ttu-id="e2753-173">**梱包明細**</span><span class="sxs-lookup"><span data-stu-id="e2753-173">**Packing Slip**</span></span>
    - <span data-ttu-id="e2753-174">**請求済**</span><span class="sxs-lookup"><span data-stu-id="e2753-174">**Invoiced**</span></span>
    - <span data-ttu-id="e2753-175">**ピッキング済**</span><span class="sxs-lookup"><span data-stu-id="e2753-175">**Picked**</span></span>
    - <span data-ttu-id="e2753-176">**一部ピック済**</span><span class="sxs-lookup"><span data-stu-id="e2753-176">**Partially Picked**</span></span>
    - <span data-ttu-id="e2753-177">**一部ピック済**</span><span class="sxs-lookup"><span data-stu-id="e2753-177">**Partially Packed**</span></span>
    - <span data-ttu-id="e2753-178">**出荷済**</span><span class="sxs-lookup"><span data-stu-id="e2753-178">**Shipped**</span></span>
    - <span data-ttu-id="e2753-179">**一部出荷済**</span><span class="sxs-lookup"><span data-stu-id="e2753-179">**Partially Shipped**</span></span>
    - <span data-ttu-id="e2753-180">**一部請求済**</span><span class="sxs-lookup"><span data-stu-id="e2753-180">**Partially Invoiced**</span></span>
    - <span data-ttu-id="e2753-181">**キャンセル済**</span><span class="sxs-lookup"><span data-stu-id="e2753-181">**Cancelled**</span></span>

<span data-ttu-id="e2753-182">[**外部で管理される製品のみ**] 設定が注文時に使用され、販売注文が外部から管理された製品で完全に構成されているかどうかが一貫して追跡されます。</span><span class="sxs-lookup"><span data-stu-id="e2753-182">The **Has Externally Maintained Products Only** setting is used during order activation to consistently track whether a sales order consists entirely of externally maintained products.</span></span> <span data-ttu-id="e2753-183">受注が外部から管理された製品で完全に構成されている場合、製品は Finance and Operations で管理されます。</span><span class="sxs-lookup"><span data-stu-id="e2753-183">If a sales order consists entirely of externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="e2753-184">この設定は、Finance and Operations に不明な製品を含む販売注文明細行を有効化したり、同期化しようとするのを防ぐのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="e2753-184">This setting helps guarantee that you don't activate and try to synchronize sales order lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="e2753-185">[**販売注文**] ページで、[**請求書の作成**]、[**注文のキャンセル**]、[**再計算**]、[**製品の取得**] および [**ルックアップ アドレス**] ボタンは外部で管理される注文用に非表示となります。それは Finance and Operations で請求書が作成され Sales に同期されるためです。</span><span class="sxs-lookup"><span data-stu-id="e2753-185">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products**, and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="e2753-186">これらの注文は、販売注文情報が有効化後に Finance and Operations から同期されるため編集することができません。</span><span class="sxs-lookup"><span data-stu-id="e2753-186">These orders can't be edited, because sales order information will be synchronized from Finance and Operations after activation.</span></span>

<span data-ttu-id="e2753-187">販売発注状況は**有効** のままにすると、Finance and Operations からの変更が Sales の販売注文に流れることを保証します。</span><span class="sxs-lookup"><span data-stu-id="e2753-187">The sales order status will remain **Active** to help guarantee that changes from Finance and Operations can flow to the sales order in Sales.</span></span> <span data-ttu-id="e2753-188">この動作を制御するためには、データ統合プロジェクトで、既定の [**Statecode\[状態\]**] を [**有効**] に設定します。</span><span class="sxs-lookup"><span data-stu-id="e2753-188">To control this behavior, set the default **Statecode \[Status\]** value to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="e2753-189">前提条件とマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="e2753-189">Preconditions and mapping setup</span></span>

<span data-ttu-id="e2753-190">販売注文を同期する前に、システムで以下の設定を更新することが重要です。</span><span class="sxs-lookup"><span data-stu-id="e2753-190">Before you synchronize sales orders, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="e2753-191">Sales での設定</span><span class="sxs-lookup"><span data-stu-id="e2753-191">Setup in Sales</span></span>

- <span data-ttu-id="e2753-192">Sales で設定された接続のユーザーが割り当てられているチームのアクセス許可として設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e2753-192">Make sure that permissions are set up for the team that the user from your Sales connection set is assigned to.</span></span> <span data-ttu-id="e2753-193">デモデータを使用している場合、通常、ユーザーは管理者権限を持っていますが、チームには管理者権限がありません。</span><span class="sxs-lookup"><span data-stu-id="e2753-193">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="e2753-194">データ統合からプロジェクトを実行するときにチームに管理者権限がない場合、主要なチームがないというエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e2753-194">If the team doesn't have admin access, when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="e2753-195">**設定** &gt; **セキュリティ** &gt; **チーム**の順に移動し、関連チームを選択してから、**ロール管理** をクリックして **システム管理者** などの必要なアクセス許可を持つロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="e2753-195">Go to **Settings** &gt; **Security** &gt; **Teams**, select the relevant team, select **Manage Roles**, and select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="e2753-196">Sales および Finance and Operations の両方で割引の計算が正しいことを確認するには、**割引の計算方法** が **行項目** に設定される必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2753-196">To ensure correct calculation of discounts in both Sales and Finance and Operations **Discount calculation method** must be set to **Line item**.</span></span>
- <span data-ttu-id="e2753-197">[**設定**] &gt; [**管理**] &gt; [**システム設定**] &gt; [**Sales**] へと順に進み、次の設定が使用されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="e2753-197">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="e2753-198">[**システム プライジング計算システムの使用**] オプションが、[**はい**] に設定されている。</span><span class="sxs-lookup"><span data-stu-id="e2753-198">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="e2753-199">[**割引の計算方法**] フィールドが、[**明細行品目**] に設定されている。</span><span class="sxs-lookup"><span data-stu-id="e2753-199">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="e2753-200">Finance and Operations での設定</span><span class="sxs-lookup"><span data-stu-id="e2753-200">Setup in Finance and Operations</span></span>

- <span data-ttu-id="e2753-201">**販売とマーケティング**&gt;**定期処理のタスク**&gt;**販売合計を計算する**の順に移動してから、バッチ ジョブとして実行されるようにジョブを設定します。</span><span class="sxs-lookup"><span data-stu-id="e2753-201">Go to **Sales and marketing** &gt; **Periodic tasks** &gt; **Calculate sales totals**, and set the job to run as a batch job.</span></span> <span data-ttu-id="e2753-202">**販売注文合計を計算する**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="e2753-202">Set the **Calculate totals for sales orders** option to **Yes**.</span></span> <span data-ttu-id="e2753-203">販売合計が計算された販売注文のみが Sales に同期されるため、このステップは重要です。</span><span class="sxs-lookup"><span data-stu-id="e2753-203">This step is important, because only sales orders where sales totals are calculated will be synchronized to Sales.</span></span> <span data-ttu-id="e2753-204">バッチジョブの頻度は、販売注文同期の頻度と一致させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2753-204">The frequency of the batch job should be aligned with the frequency of sales order synchronization.</span></span>

### <a name="setup-in-the-sales-orders-sales-to-fin-and-ops---direct-data-integration-project"></a><span data-ttu-id="e2753-205">販売注文のセット アップ (Sales から Finance and Operations) - ダイレクト データ統合プロジェクト</span><span class="sxs-lookup"><span data-stu-id="e2753-205">Setup in the Sales Orders (Sales to Fin and Ops) - Direct Data integration project</span></span>

- <span data-ttu-id="e2753-206">必要なマッピングが [**Shipto\_country**] から [**DeliveryAddressCountryRegionISOCode**] に存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="e2753-206">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="e2753-207">値マップで既定値を空白にして、国内の注文の国を入力を回避することができます。</span><span class="sxs-lookup"><span data-stu-id="e2753-207">You can make blank a default value in the value map to avoid having to type country for national orders.</span></span> <span data-ttu-id="e2753-208">左側を「空白」のままにして、右側を希望する国または地域に設定します。</span><span class="sxs-lookup"><span data-stu-id="e2753-208">Set the left side to 'Blank', and set the right side to the desired country or region.</span></span>

    <span data-ttu-id="e2753-209">テンプレート値は、いくつかの国または地域がマップされている値マップで、「空白」= アメリカ合衆国です。</span><span class="sxs-lookup"><span data-stu-id="e2753-209">The template value is a value map where several countries or regions are mapped, and where 'Blank' = US.</span></span>

### <a name="setup-in-the-sales-orders-fin-and-ops-to-sales---direct-data-integration-project"></a><span data-ttu-id="e2753-210">販売注文の設定 (Finance and Operations から Sales) - ダイレクト データ統合プロジェクト</span><span class="sxs-lookup"><span data-stu-id="e2753-210">Setup in the Sales Orders (Fin and Ops to Sales) - Direct Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="e2753-211">SalesHeader タスク</span><span class="sxs-lookup"><span data-stu-id="e2753-211">SalesHeader task</span></span>

- <span data-ttu-id="e2753-212">価格リストは、Sales で注文を作成するために必要です。</span><span class="sxs-lookup"><span data-stu-id="e2753-212">A price list is required in order to create orders in Sales.</span></span> <span data-ttu-id="e2753-213">Sales で通貨ごとに使用される価格リストへの [**pricelevelid.name \[価格リスト名\]**] の値マップを更新します。</span><span class="sxs-lookup"><span data-stu-id="e2753-213">Update the value map for **pricelevelid.name \[Price List Name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="e2753-214">1つの通貨に対する既定の価格リストを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="e2753-214">You can use the default price list for a single currency.</span></span> <span data-ttu-id="e2753-215">または、複数の通貨で価格リストがある場合、値マップを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="e2753-215">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="e2753-216">[**pricelevelid.name\[価格リスト名\]**] の既定のテンプレートの値は、[**CRM サービス USA (サンプル)**] です。</span><span class="sxs-lookup"><span data-stu-id="e2753-216">The default template value for **pricelevelid.name \[Price List Name\]** is **CRM Service USA (sample)**.</span></span>

#### <a name="salesline-task"></a><span data-ttu-id="e2753-217">SalesLine タスク</span><span class="sxs-lookup"><span data-stu-id="e2753-217">SalesLine task</span></span>

- <span data-ttu-id="e2753-218">Finance and Operation で [**SalesUnitSymbol**] 用の必要な値マップを確認します。</span><span class="sxs-lookup"><span data-stu-id="e2753-218">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>
- <span data-ttu-id="e2753-219">Sales に必要な単位が定義されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e2753-219">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="e2753-220">値マップを持つテンプレート値は、[**SalesUnitSymbol**] から [**oumid.name**] に対して定義されています。</span><span class="sxs-lookup"><span data-stu-id="e2753-220">A template value that has a value map is defined for **SalesUnitSymbol** to **oumid.name**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e2753-221">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="e2753-221">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="e2753-222">[**支払条件**]、[**運賃条件**]、[**配送条件**]、[**送付方法**]、および [**配送モード**] フィールドは、既定のマッピングの一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="e2753-222">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="e2753-223">これらのフィールドをマップするには、エンティティ間で同期される組織内のデータに固有の値マッピングを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2753-223">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="e2753-224">次の図は、データ統合のテンプレート マッピングの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="e2753-224">The following illustrations show an example of a template mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="e2753-225">マッピングでは、Sales から Finance and Operations に、または Finance and Operations から Sales に同期するフィールド情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="e2753-225">The mapping shows which field information will be synchronized from Sales to Finance and Operations, or from Finance and Operations to Sales.</span></span>

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderheader"></a><span data-ttu-id="e2753-226">販売注文 (Finance and Operations から Sales) - 直接: OrderHeader</span><span class="sxs-lookup"><span data-stu-id="e2753-226">Sales Orders (Fin and Ops to Sales) - Direct: OrderHeader</span></span>

<span data-ttu-id="e2753-227">[![データ統合のテンプレートのマッピング](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)</span><span class="sxs-lookup"><span data-stu-id="e2753-227">[![Template mapping in Data integration](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)</span></span>

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderline"></a><span data-ttu-id="e2753-228">販売注文 (Finance and Operations から Sales) - 直接: OrderLine</span><span class="sxs-lookup"><span data-stu-id="e2753-228">Sales Orders (Fin and Ops to Sales) - Direct: OrderLine</span></span>

<span data-ttu-id="e2753-229">[![データ統合のテンプレートのマッピング](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)</span><span class="sxs-lookup"><span data-stu-id="e2753-229">[![Template mapping in Data integration](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)</span></span>

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderheader"></a><span data-ttu-id="e2753-230">販売注文 (Sales から Finance and Operations) - 直接: OrderHeader</span><span class="sxs-lookup"><span data-stu-id="e2753-230">Sales Orders (Sales to Fin and Ops) - Direct: OrderHeader</span></span>

<span data-ttu-id="e2753-231">[![データ統合のテンプレートのマッピング](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)</span><span class="sxs-lookup"><span data-stu-id="e2753-231">[![Template mapping in Data integration](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)</span></span>

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderline"></a><span data-ttu-id="e2753-232">販売注文 (Sales から Finance and Operations) - 直接: OrderLine</span><span class="sxs-lookup"><span data-stu-id="e2753-232">Sales Orders (Sales to Fin and Ops) - Direct: OrderLine</span></span>

<span data-ttu-id="e2753-233">[![データ統合のテンプレートのマッピング](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)</span><span class="sxs-lookup"><span data-stu-id="e2753-233">[![Template mapping in Data integration](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2753-234">関連トピック</span><span class="sxs-lookup"><span data-stu-id="e2753-234">Related topics</span></span>

[<span data-ttu-id="e2753-235">見込顧客を現金化</span><span class="sxs-lookup"><span data-stu-id="e2753-235">Prospect to cash</span></span>](prospect-to-cash.md)

