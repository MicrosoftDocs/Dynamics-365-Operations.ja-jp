---
title: 販売注文の Sales と Supply Chain Management の間の直接同期
description: このトピックでは、Dynamics 365 Sales と Dynamics 365 Supply Chain Management の間での販売注文の直接同期の実行に使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
manager: AnnBe
ms.date: 05/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 7c8831203ae30991ff8acf1926aafc2d1839aeb2
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251273"
---
# <a name="synchronization-of-sales-orders-directly-between-sales-and-supply-chain-management"></a><span data-ttu-id="63f39-103">販売注文の Sales と Supply Chain Management の間の直接同期</span><span class="sxs-lookup"><span data-stu-id="63f39-103">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63f39-104">このトピックでは、Dynamics 365 Sales と Dynamics 365 Supply Chain Management の間での販売注文の直接同期の実行に使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="63f39-104">The topic discusses the templates and underlying tasks that are used to run synchronization of sales orders directly between Dynamics 365 Sales and Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="63f39-105">見込み客の現金化へのデータフロー</span><span class="sxs-lookup"><span data-stu-id="63f39-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="63f39-106">見込み客の現金化ソリューションは、Supply Chain Management と Sales のインスタンス間でデータを同期するため、データの統合機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="63f39-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="63f39-107">データ統合機能で利用可能な見込み顧客を現金化するテンプレートにより、Supply Chain Management と Sales 間での勘定、連絡先、製品および販売見積、販売注文、および売上請求書のデータの流れが可能になります。</span><span class="sxs-lookup"><span data-stu-id="63f39-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="63f39-108">次の図は、Supply Chain Management と Sales の間でデータを同期させる方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="63f39-108">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="63f39-109">[![見込み客の現金化へのデータフロー](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="63f39-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="63f39-110">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="63f39-110">Templates and tasks</span></span>

<span data-ttu-id="63f39-111">利用可能なテンプレートにアクセスするには、[PowerApps 管理者センター](https://preview.admin.powerapps.com/dataintegration) を開きます。</span><span class="sxs-lookup"><span data-stu-id="63f39-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="63f39-112">**プロジェクト**を選択した後、右上隅にある **新しいプロジェクト** を選択してパブリック テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="63f39-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="63f39-113">Sales と Supply Chain Management との間での販売注文の直接同期の実行には、以下のテンプレートと基本的なタスクが使用されます。</span><span class="sxs-lookup"><span data-stu-id="63f39-113">The following templates and underlying tasks are used to run synchronization of sales orders directly between Sales and Supply Chain Management.</span></span>

- <span data-ttu-id="63f39-114">**データ統合でのテンプレートの名前:**</span><span class="sxs-lookup"><span data-stu-id="63f39-114">**Names of the templates in Data integration:**</span></span> 

    - <span data-ttu-id="63f39-115">販売注文 (Sales から Supply Chain Management) - 直接</span><span class="sxs-lookup"><span data-stu-id="63f39-115">Sales Orders (Sales to Supply Chain Management) - Direct</span></span>
    - <span data-ttu-id="63f39-116">販売注文 (Supply Chain Management から Sales) - 直接</span><span class="sxs-lookup"><span data-stu-id="63f39-116">Sales Orders (Supply Chain Management to Sales) - Direct</span></span>

- <span data-ttu-id="63f39-117">**データ統合プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="63f39-117">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="63f39-118">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="63f39-118">OrderHeader</span></span>
    - <span data-ttu-id="63f39-119">OrderLine</span><span class="sxs-lookup"><span data-stu-id="63f39-119">OrderLine</span></span>

<span data-ttu-id="63f39-120">販売請求書ヘッダーと明細行を同期させるには、次の同期タスクが必要です。</span><span class="sxs-lookup"><span data-stu-id="63f39-120">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="63f39-121">製品 (Supply Chain Management から Sales) - 直接</span><span class="sxs-lookup"><span data-stu-id="63f39-121">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="63f39-122">勘定 (Sales から Supply Chain Management) - ダイレクト (使用する場合)</span><span class="sxs-lookup"><span data-stu-id="63f39-122">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="63f39-123">顧客への連絡先 (Sales から Supply Chain Management) - ダイレクト (使用する場合)</span><span class="sxs-lookup"><span data-stu-id="63f39-123">Contacts to Customers (Sales to Supply Chain Management) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="63f39-124">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="63f39-124">Entity set</span></span>

| <span data-ttu-id="63f39-125">サプライ チェーン マネジメント</span><span class="sxs-lookup"><span data-stu-id="63f39-125">Supply Chain Management</span></span>  | <span data-ttu-id="63f39-126">販売注文</span><span class="sxs-lookup"><span data-stu-id="63f39-126">Sales</span></span>             |
|-------------------------|-------------------|
| <span data-ttu-id="63f39-127">CDS 販売注文ヘッダー</span><span class="sxs-lookup"><span data-stu-id="63f39-127">CDS sales order headers</span></span> | <span data-ttu-id="63f39-128">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="63f39-128">SalesOrders</span></span>       |
| <span data-ttu-id="63f39-129">CDS 販売注文明細行</span><span class="sxs-lookup"><span data-stu-id="63f39-129">CDS sales order lines</span></span>   | <span data-ttu-id="63f39-130">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="63f39-130">SalesOrderDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="63f39-131">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="63f39-131">Entity flow</span></span>

<span data-ttu-id="63f39-132">**販売注文 (Sales から Supply Chain Management) - 直接** テンプレートに基づいたプロジェクトに対して **プロジェクトの実行** が発生する場合、Sales で作成された販売注文が Supply Chain Management に同期されます。</span><span class="sxs-lookup"><span data-stu-id="63f39-132">Sales orders are created in Sales and synchronized to Supply Chain Management when **Run project** is triggered for a project based on the **Sales Orders (Sales to Supply Chain Management) - Direct** template.</span></span> <span data-ttu-id="63f39-133">全ての**受注製品**が外部で管理される製品で構成されている場合にのみ、Sales からの販売注文を同期できます。</span><span class="sxs-lookup"><span data-stu-id="63f39-133">You can only activate and synchronize orders from Sales if all **Order Products** consist of products that are externally maintained.</span></span> <span data-ttu-id="63f39-134">したがって、リスト外製品は存在しません。</span><span class="sxs-lookup"><span data-stu-id="63f39-134">Therefore, there can be no write-in products.</span></span> <span data-ttu-id="63f39-135">注文を有効にすると、販売注文はユーザー インターフェイス (UI) で読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="63f39-135">After the order is activated, the sales order becomes read-only in the user interface (UI).</span></span> <span data-ttu-id="63f39-136">この時点で、更新は Supply Chain Management から行われます。</span><span class="sxs-lookup"><span data-stu-id="63f39-136">At that point, the updates are made from Supply Chain Management.</span></span> <span data-ttu-id="63f39-137">販売注文が **確認済** 状態となった後に、**販売注文 (Supply Chain Management から Sales) － 直接** テンプレートに基づいたプロジェクトは Supply Chain Management から Sales に更新またはフルフィルメントの状態を同期するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="63f39-137">After the sales order has a status of **Confirmed**, the a project based on the **Sales Orders (Supply Chain Management to Sales) - Direct** template can be used to synchronize updates or fulfillment status from Supply Chain Management to Sales.</span></span>

<span data-ttu-id="63f39-138">Sales で注文を作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="63f39-138">You don't have to create orders in Sales.</span></span> <span data-ttu-id="63f39-139">代わりに、Supply Chain Management で新しい販売注文を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="63f39-139">You can create new sales orders in Supply Chain Management instead.</span></span> <span data-ttu-id="63f39-140">販売注文が**確認済**のステータスになった後、前の段落で説明するように Sales に同期されます。</span><span class="sxs-lookup"><span data-stu-id="63f39-140">After a sales order has a status of **Confirmed**, it's synchronized to Sales as described in the previous paragraph.</span></span>

<span data-ttu-id="63f39-141">Supply Chain Management では、テンプレートのフィルタは関連する販売注文のみが同期に含まれていることを保証します。</span><span class="sxs-lookup"><span data-stu-id="63f39-141">In Supply Chain Management, filters in the template help guarantee that only the relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="63f39-142">販売注文では、受注顧客と請求顧客の両方が Sales から生成されて同期に含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="63f39-142">On the sales order, both the ordering customer and the invoicing customer have to originate from Sales to be included in the synchronization.</span></span> <span data-ttu-id="63f39-143">Supply Chain Management で、**OrderingCustomerIsExternallyMaintained** および **InvoiceCustomerIsExternallyMaintained** フィールドは、データ エンティティからの販売注文をフィルタするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="63f39-143">In Supply Chain Management, the **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** fields are used to filter sales orders from the data entities.</span></span>
- <span data-ttu-id="63f39-144">Supply Chain Management で販売注文を確定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63f39-144">The sales order in Supply Chain Management must be confirmed.</span></span> <span data-ttu-id="63f39-145">**出荷済** や **請求済** など、確認済の販売注文または処理ステータスの高い販売注文のみが Sales に同期されます。</span><span class="sxs-lookup"><span data-stu-id="63f39-145">Only confirmed sales orders or sales orders that have a higher processing status, such as **Shipped** or **Invoiced**, are synchronized to Sales.</span></span>
- <span data-ttu-id="63f39-146">販売注文を作成または変更した後、Supply Chain Management で **販売合計の計算** のバッチ ジョブを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63f39-146">After a sales order is created or modified, the **Calculate sales totals** batch job in Supply Chain Management must be run.</span></span> <span data-ttu-id="63f39-147">販売合計が計算された販売注文のみが Sales に同期されます。</span><span class="sxs-lookup"><span data-stu-id="63f39-147">Only sales orders where sales totals are calculated will be synchronized to Sales.</span></span>

## <a name="freight-tax"></a><span data-ttu-id="63f39-148">運賃税</span><span class="sxs-lookup"><span data-stu-id="63f39-148">Freight tax</span></span>

<span data-ttu-id="63f39-149">Sales は、明細行レベルで税が格納されるため、ヘッダー レベルでの税をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="63f39-149">Sales doesn't support tax at the header level, because tax is stored at the line level.</span></span> <span data-ttu-id="63f39-150">運賃税など Supply Chain Management からヘッダー レベルでの税をサポートするためには、システムは **運賃税** と呼ぶリスト外製品として税を Sales に同期して、Supply Chain Management からの税額を含めます。</span><span class="sxs-lookup"><span data-stu-id="63f39-150">To support tax at the header level from Supply Chain Management, such as tax on freight, the system synchronizes tax to Sales as a write-in product that is named **Freight Tax**, and that has the tax amount from Supply Chain Management.</span></span> <span data-ttu-id="63f39-151">これにより、Sales での標準価の計算は、Supply Chain Management からヘッダー レベルで税がある場合でも合計金額として使用できます。</span><span class="sxs-lookup"><span data-stu-id="63f39-151">In this way, the standard price calculation in Sales can be used for totals, even when there is tax at the header level from Supply Chain Management.</span></span>

## <a name="discount-calculation-and-rounding"></a><span data-ttu-id="63f39-152">割引計算と丸め</span><span class="sxs-lookup"><span data-stu-id="63f39-152">Discount calculation and rounding</span></span>

<span data-ttu-id="63f39-153">Sales での割引計算モデルは、Supply Chain Management の割引計算モデルとは異なります。</span><span class="sxs-lookup"><span data-stu-id="63f39-153">The discount calculation model in Sales differs from the discount calculation model in Supply Chain Management.</span></span> <span data-ttu-id="63f39-154">Supply Chain Management では、販売注文明細行の最終的な割引金額は、割引額と割引率の組み合わせの結果です。</span><span class="sxs-lookup"><span data-stu-id="63f39-154">In Supply Chain Management, the final discount amount on a sales line can be the result of a combination of discount amounts and discount percentages.</span></span> <span data-ttu-id="63f39-155">この最終割引額をライン上の数量で割ると、丸め処理が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="63f39-155">If this final discount amount is divided by the quantity on the line, rounding can occur.</span></span> <span data-ttu-id="63f39-156">ただし、この丸め処理単位の割引額が Sales に同期されている場合は、この丸め処理は考慮されません。</span><span class="sxs-lookup"><span data-stu-id="63f39-156">However, this rounding isn't considered if a rounded per-unit discount amount is synchronized to Sales.</span></span> <span data-ttu-id="63f39-157">Supply Chain Management の販売ラインからの全額割引が Sales に正しく同期されるようにするには、全額を明細行の数量で除算せずに同期させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="63f39-157">To help guarantee that the full discount amount from a sales line in Supply Chain Management is correctly synchronized to Sales, the full amount must be synchronized without being divided by the line quantity.</span></span> <span data-ttu-id="63f39-158">したがって、Sales で **割引の計算方法** を **明細行品目** として定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63f39-158">Therefore, you must define the **Discount calculation method** as **Line item** in Sales.</span></span>

<span data-ttu-id="63f39-159">販売注文行が Sales から Supply Chain Management に同期される場合、明細行全体の割引額が使用されます。</span><span class="sxs-lookup"><span data-stu-id="63f39-159">When a sales order line is synchronized from Sales to Supply Chain Management, the full line discount amount is used.</span></span> <span data-ttu-id="63f39-160">Supply Chain Management には、明細行の完全な割引金額を格納できるフィールドがないため、金額は数量で除算されて、**行割引**フィールドに格納されます。</span><span class="sxs-lookup"><span data-stu-id="63f39-160">Because Supply Chain Management has no field that can store the full discount amount for a line, the amount is divided by the quantity and stored in the **Line discount** field.</span></span> <span data-ttu-id="63f39-161">この区分中に発生する丸め処理は販売注文明細行の**売上諸掛**フィールドに格納されます。</span><span class="sxs-lookup"><span data-stu-id="63f39-161">Any rounding that occurs in this division is stored in the **Sales charges** field on the sales line.</span></span>

### <a name="example"></a><span data-ttu-id="63f39-162">例</span><span class="sxs-lookup"><span data-stu-id="63f39-162">Example</span></span>

<span data-ttu-id="63f39-163">**Sales から Supply Chain Management への同期**</span><span class="sxs-lookup"><span data-stu-id="63f39-163">**Synchronization from Sales to Supply Chain Management**</span></span>

- <span data-ttu-id="63f39-164">**Sales:** 数量 = 3、行あたりの割引 = 10.00 USD</span><span class="sxs-lookup"><span data-stu-id="63f39-164">**Sales:** Quantity = 3, per-line discount = $10.00</span></span>
- <span data-ttu-id="63f39-165">**サプライ チェーン マネジメント:** 数量 = 3、明細行割引金額 = $3.33、売上諸掛 = -$0.01</span><span class="sxs-lookup"><span data-stu-id="63f39-165">**Supply Chain Management:** Quantity = 3, line discount amount = $3.33, sales charge = -$0.01</span></span> 

<span data-ttu-id="63f39-166">**Supply Chain Management から Sales への同期**</span><span class="sxs-lookup"><span data-stu-id="63f39-166">**Synchronization from Supply Chain Management to Sales**</span></span>

- <span data-ttu-id="63f39-167">**サプライ チェーン マネジメント:** 数量 = 3、明細行割引金額 = $3.33、売上諸掛 = -$0.01</span><span class="sxs-lookup"><span data-stu-id="63f39-167">**Supply Chain Management:** Quantity = 3, line discount amount = $3.33, sales charge = -$0.01</span></span>
- <span data-ttu-id="63f39-168">**Sales:** 数量 = 3、行あたりの割引 = (3 × 3.33 USD) + 0.01 USD = 10.00 USD</span><span class="sxs-lookup"><span data-stu-id="63f39-168">**Sales:** Quantity = 3, per-line discount = (3 × $3.33) + $0.01 = $10.00</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="63f39-169">売上の見込顧客を現金化するソリューション</span><span class="sxs-lookup"><span data-stu-id="63f39-169">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="63f39-170">新しいフィールドが **注文** エンティティに追加され、ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="63f39-170">New fields have been added to the **Order** entity and appear on the page:</span></span>

- <span data-ttu-id="63f39-171">**外部で管理** - 注文が Supply Chain Management から来る場合、このオプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="63f39-171">**Is Maintained Externally** – Set this option to **Yes** when the order is coming from Supply Chain Management.</span></span>
- <span data-ttu-id="63f39-172">**処理状態** - このフィールドには、Supply Chain Management の注文の処理状態が表示されます。</span><span class="sxs-lookup"><span data-stu-id="63f39-172">**Processing status** – This field shows the processing status of the order in Supply Chain Management.</span></span> <span data-ttu-id="63f39-173">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="63f39-173">The following values are available:</span></span>

    - <span data-ttu-id="63f39-174">**ドラフト** – Sales で受注が作成される場合の初期ステータス。</span><span class="sxs-lookup"><span data-stu-id="63f39-174">**Draft** – The initial status when an order is created in Sales.</span></span> <span data-ttu-id="63f39-175">Sales では、この処理ステータスの注文のみ編集することができます。</span><span class="sxs-lookup"><span data-stu-id="63f39-175">In Sales, only orders with this processing status can be edited.</span></span>
    - <span data-ttu-id="63f39-176">**有効** – **有効**ボタンを使用すると、受注後のステータスが Sales で有効になります。</span><span class="sxs-lookup"><span data-stu-id="63f39-176">**Active** – The status after the order is activated in Sales by using the **Activate** button.</span></span>
    - <span data-ttu-id="63f39-177">**確認済**</span><span class="sxs-lookup"><span data-stu-id="63f39-177">**Confirmed**</span></span>
    - <span data-ttu-id="63f39-178">**梱包明細**</span><span class="sxs-lookup"><span data-stu-id="63f39-178">**Packing Slip**</span></span>
    - <span data-ttu-id="63f39-179">**請求済**</span><span class="sxs-lookup"><span data-stu-id="63f39-179">**Invoiced**</span></span>
    - <span data-ttu-id="63f39-180">**ピッキング済**</span><span class="sxs-lookup"><span data-stu-id="63f39-180">**Picked**</span></span>
    - <span data-ttu-id="63f39-181">**一部ピック済**</span><span class="sxs-lookup"><span data-stu-id="63f39-181">**Partially Picked**</span></span>
    - <span data-ttu-id="63f39-182">**一部ピック済**</span><span class="sxs-lookup"><span data-stu-id="63f39-182">**Partially Packed**</span></span>
    - <span data-ttu-id="63f39-183">**出荷済**</span><span class="sxs-lookup"><span data-stu-id="63f39-183">**Shipped**</span></span>
    - <span data-ttu-id="63f39-184">**一部出荷済**</span><span class="sxs-lookup"><span data-stu-id="63f39-184">**Partially Shipped**</span></span>
    - <span data-ttu-id="63f39-185">**一部請求済**</span><span class="sxs-lookup"><span data-stu-id="63f39-185">**Partially Invoiced**</span></span>
    - <span data-ttu-id="63f39-186">**キャンセル済**</span><span class="sxs-lookup"><span data-stu-id="63f39-186">**Cancelled**</span></span>

<span data-ttu-id="63f39-187">**外部で管理される製品のみ** 設定が注文時に使用され、販売注文が外部から管理された製品で完全に構成されているかどうかが一貫して追跡されます。</span><span class="sxs-lookup"><span data-stu-id="63f39-187">The **Has Externally Maintained Products Only** setting is used during order activation to consistently track whether a sales order consists entirely of externally maintained products.</span></span> <span data-ttu-id="63f39-188">受注が外部から管理された製品で完全に構成されている場合、製品は Supply Chain Management で管理されます。</span><span class="sxs-lookup"><span data-stu-id="63f39-188">If a sales order consists entirely of externally maintained products, the products are maintained in Supply Chain Management.</span></span> <span data-ttu-id="63f39-189">この設定は、Supply Chain Management に不明な製品を含む販売注文明細行を有効化したり、同期化しようとするのを防ぐのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="63f39-189">This setting helps guarantee that you don't activate and try to synchronize sales order lines that have products that are unknown to Supply Chain Management.</span></span>

<span data-ttu-id="63f39-190">**販売注文**ページで、**請求書の作成**、**注文のキャンセル**、**再計算**、**製品の取得**および**ルックアップ アドレス**ボタンは外部で管理される注文用に非表示となります。それは Supply Chain Management で請求書が作成され Sales に同期されるためです。</span><span class="sxs-lookup"><span data-stu-id="63f39-190">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products**, and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders, because invoices will be created in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="63f39-191">これらの注文は、販売注文情報が有効化後に Supply Chain Management から同期されるため編集することができません。</span><span class="sxs-lookup"><span data-stu-id="63f39-191">These orders can't be edited, because sales order information will be synchronized from Supply Chain Management after activation.</span></span>

<span data-ttu-id="63f39-192">販売発注状況は**有効**のままにすると、Supply Chain Management からの変更が Sales の販売注文に流れることを保証します。</span><span class="sxs-lookup"><span data-stu-id="63f39-192">The sales order status will remain **Active** to help guarantee that changes from Supply Chain Management can flow to the sales order in Sales.</span></span> <span data-ttu-id="63f39-193">この動作を制御するためには、データ統合プロジェクトで、既定の **Statecode \[状態\]** を**有効**に設定します。</span><span class="sxs-lookup"><span data-stu-id="63f39-193">To control this behavior, set the default **Statecode \[Status\]** value to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="63f39-194">前提条件とマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="63f39-194">Preconditions and mapping setup</span></span>

<span data-ttu-id="63f39-195">販売注文を同期する前に、システムで以下の設定を更新することが重要です。</span><span class="sxs-lookup"><span data-stu-id="63f39-195">Before you synchronize sales orders, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="63f39-196">Sales での設定</span><span class="sxs-lookup"><span data-stu-id="63f39-196">Setup in Sales</span></span>

- <span data-ttu-id="63f39-197">Sales で設定された接続のユーザーが割り当てられているチームのアクセス許可として設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="63f39-197">Make sure that permissions are set up for the team that the user from your Sales connection set is assigned to.</span></span> <span data-ttu-id="63f39-198">デモデータを使用している場合、通常、ユーザーは管理者権限を持っていますが、チームには管理者権限がありません。</span><span class="sxs-lookup"><span data-stu-id="63f39-198">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="63f39-199">データ統合からプロジェクトを実行するときにチームに管理者権限がない場合、主要なチームがないというエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="63f39-199">If the team doesn't have admin access, when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="63f39-200">**設定** &gt; **セキュリティ** &gt; **チーム**の順に移動し、関連チームを選択してから、**ロール管理** をクリックして **システム管理者** などの必要なアクセス許可を持つロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="63f39-200">Go to **Settings** &gt; **Security** &gt; **Teams**, select the relevant team, select **Manage Roles**, and select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="63f39-201">Sales および Supply Chain Management の両方で割引の計算が正しいことを確認するには、**割引の計算方法**が**行項目**に設定される必要があります。</span><span class="sxs-lookup"><span data-stu-id="63f39-201">To ensure correct calculation of discounts in both Sales and Supply Chain Management **Discount calculation method** must be set to **Line item**.</span></span>
- <span data-ttu-id="63f39-202">**設定** &gt; **管理** &gt; **システム設定** &gt; **Sales** へと順に進み、次の設定が使用されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="63f39-202">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="63f39-203">**システム プライジング計算システムの使用** オプションが、**はい** に設定されている。</span><span class="sxs-lookup"><span data-stu-id="63f39-203">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="63f39-204">**割引の計算方法** フィールドが、**明細行品目** に設定されている。</span><span class="sxs-lookup"><span data-stu-id="63f39-204">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-supply-chain-management"></a><span data-ttu-id="63f39-205">Supply Chain Management での設定</span><span class="sxs-lookup"><span data-stu-id="63f39-205">Setup in Supply Chain Management</span></span>

- <span data-ttu-id="63f39-206">**販売とマーケティング**&gt;**定期処理のタスク**&gt;**販売合計を計算する**の順に移動してから、バッチ ジョブとして実行されるようにジョブを設定します。</span><span class="sxs-lookup"><span data-stu-id="63f39-206">Go to **Sales and marketing** &gt; **Periodic tasks** &gt; **Calculate sales totals**, and set the job to run as a batch job.</span></span> <span data-ttu-id="63f39-207">**販売注文合計を計算する**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="63f39-207">Set the **Calculate totals for sales orders** option to **Yes**.</span></span> <span data-ttu-id="63f39-208">販売合計が計算された販売注文のみが Sales に同期されるため、このステップは重要です。</span><span class="sxs-lookup"><span data-stu-id="63f39-208">This step is important, because only sales orders where sales totals are calculated will be synchronized to Sales.</span></span> <span data-ttu-id="63f39-209">バッチジョブの頻度は、販売注文同期の頻度と一致させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="63f39-209">The frequency of the batch job should be aligned with the frequency of sales order synchronization.</span></span>

<span data-ttu-id="63f39-210">ワークオーダー統合も使用する場合は、販売元を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63f39-210">If you also use work order integration, you need to set up the sales origin.</span></span> <span data-ttu-id="63f39-211">販売元は、Field Service のワーク オーダーから作成された Supply Chain Management の販売注文を区別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="63f39-211">The sales origin is used to distinguish sales orders in Supply Chain Management that were created from work orders in Field Service.</span></span> <span data-ttu-id="63f39-212">販売注文に**ワーク オーダー統合**タイプの販売元がある場合、**外部ワーク オーダー ステータス** フィールドが販売注文ヘッダーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="63f39-212">When a sales order has a sales origin of the **Work order integration** type, the **External work order status** field appears on the sales order header.</span></span> <span data-ttu-id="63f39-213">また販売元は、Field Service のワーク オーダーから作成された販売注文が、Supply Chain Management から Field Service への販売注文同期の間に除外されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="63f39-213">Additionally, the sales origin ensures that sales orders that were created from work orders in Field Service are filtered out during sales order synchronization from Supply Chain Management to Field Service.</span></span>

1. <span data-ttu-id="63f39-214">**販売とマーケティング** \> **設定** \> **販売注文** \> **販売元** に移動します。</span><span class="sxs-lookup"><span data-stu-id="63f39-214">Go to **Sales and marketing** \> **Setup** \> **Sales orders** \> **Sales origin**.</span></span>
2. <span data-ttu-id="63f39-215">**新規**を選択し、新しい販売元を作成します。</span><span class="sxs-lookup"><span data-stu-id="63f39-215">Select **New** to create a new sales origin.</span></span>
3. <span data-ttu-id="63f39-216">**販売元**フィールドに、**SalesOrder** のような販売元の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="63f39-216">In the **Sales origin** field, enter a name for the sales origin, such as **SalesOrder**.</span></span>
4. <span data-ttu-id="63f39-217">**説明**フィールドに、**販売からの販売注文**のような説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="63f39-217">In the **Description** field, enter a description, such as **Sales Order from Sales**.</span></span>
5. <span data-ttu-id="63f39-218">**発生元タイプの割り当て** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="63f39-218">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="63f39-219">**販売元タイプ**フィールドを**販売注文統合**に設定します。</span><span class="sxs-lookup"><span data-stu-id="63f39-219">Set the **Sales origin type** field to **Sales order integration**.</span></span>
7. <span data-ttu-id="63f39-220">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="63f39-220">Select **Save**.</span></span>

### <a name="setup-in-the-sales-orders-sales-to-supply-chain-management---direct-data-integration-project"></a><span data-ttu-id="63f39-221">販売注文のセット アップ (Sales から Supply Chain Management) - ダイレクト データ統合プロジェクト</span><span class="sxs-lookup"><span data-stu-id="63f39-221">Setup in the Sales Orders (Sales to Supply Chain Management) - Direct Data integration project</span></span>

- <span data-ttu-id="63f39-222">必要なマッピングが **Shipto\_country** から **DeliveryAddressCountryRegionISOCode** に存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="63f39-222">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="63f39-223">値マップで既定値を空白にして、国内の注文の国を入力を回避することができます。</span><span class="sxs-lookup"><span data-stu-id="63f39-223">You can make blank a default value in the value map to avoid having to type country for national orders.</span></span> <span data-ttu-id="63f39-224">左側を「空白」のままにして、右側を希望する国または地域に設定します。</span><span class="sxs-lookup"><span data-stu-id="63f39-224">Set the left side to 'Blank', and set the right side to the desired country or region.</span></span>

    <span data-ttu-id="63f39-225">テンプレート値は、いくつかの国または地域がマップされている値マップで、「空白」= アメリカ合衆国です。</span><span class="sxs-lookup"><span data-stu-id="63f39-225">The template value is a value map where several countries or regions are mapped, and where 'Blank' = US.</span></span>

### <a name="setup-in-the-sales-orders-supply-chain-management-to-sales---direct-data-integration-project"></a><span data-ttu-id="63f39-226">販売注文のセット アップ (Supply Chain Management から Sales) - ダイレクト データ統合プロジェクト</span><span class="sxs-lookup"><span data-stu-id="63f39-226">Setup in the Sales Orders (Supply Chain Management to Sales) - Direct Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="63f39-227">SalesHeader タスク</span><span class="sxs-lookup"><span data-stu-id="63f39-227">SalesHeader task</span></span>

- <span data-ttu-id="63f39-228">価格リストは、Sales で注文を作成するために必要です。</span><span class="sxs-lookup"><span data-stu-id="63f39-228">A price list is required in order to create orders in Sales.</span></span> <span data-ttu-id="63f39-229">Sales で通貨ごとに使用される価格リストへの **pricelevelid.name \[価格リスト名\]** の値マップを更新します。</span><span class="sxs-lookup"><span data-stu-id="63f39-229">Update the value map for **pricelevelid.name \[Price List Name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="63f39-230">1つの通貨に対する既定の価格リストを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="63f39-230">You can use the default price list for a single currency.</span></span> <span data-ttu-id="63f39-231">または、複数の通貨で価格リストがある場合、値マップを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="63f39-231">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="63f39-232">**pricelevelid.name\[価格リスト名\]** の既定のテンプレートの値は、**CRM サービス USA (サンプル)** です。</span><span class="sxs-lookup"><span data-stu-id="63f39-232">The default template value for **pricelevelid.name \[Price List Name\]** is **CRM Service USA (sample)**.</span></span>

#### <a name="salesline-task"></a><span data-ttu-id="63f39-233">SalesLine タスク</span><span class="sxs-lookup"><span data-stu-id="63f39-233">SalesLine task</span></span>

- <span data-ttu-id="63f39-234">Supply Chain Management の **SalesUnitSymbol** に必要な値マップが存在することを確認して下さい。</span><span class="sxs-lookup"><span data-stu-id="63f39-234">Make sure that the required value map for **SalesUnitSymbol** in Supply Chain Management exists.</span></span>
- <span data-ttu-id="63f39-235">Sales に必要な単位が定義されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="63f39-235">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="63f39-236">値マップを持つテンプレート値は、**SalesUnitSymbol** から **oumid.name** に対して定義されています。</span><span class="sxs-lookup"><span data-stu-id="63f39-236">A template value that has a value map is defined for **SalesUnitSymbol** to **oumid.name**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="63f39-237">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="63f39-237">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="63f39-238">**支払条件**、**運賃条件**、**配送条件**、**送付方法**、および **配送モード** フィールドは、既定のマッピングの一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="63f39-238">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="63f39-239">これらのフィールドをマップするには、エンティティ間で同期される組織内のデータに固有の値マッピングを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63f39-239">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="63f39-240">次の図は、データ統合のテンプレート マッピングの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="63f39-240">The following illustrations show an example of a template mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="63f39-241">マッピングでは、Supply Chain Management に、または Supply Chain Management から Sales に同期するフィールド情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="63f39-241">The mapping shows which field information will be synchronized from Sales to Supply Chain Management, or from Supply Chain Management to Sales.</span></span>

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderheader"></a><span data-ttu-id="63f39-242">販売注文 (Supply Chain Management から Sales) - 直接: OrderHeader</span><span class="sxs-lookup"><span data-stu-id="63f39-242">Sales Orders (Supply Chain Management to Sales) - Direct: OrderHeader</span></span>

<span data-ttu-id="63f39-243">[![データ統合のテンプレートのマッピング](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)</span><span class="sxs-lookup"><span data-stu-id="63f39-243">[![Template mapping in Data integration](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)</span></span>

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderline"></a><span data-ttu-id="63f39-244">販売注文 (Supply Chain Management から Sales) - 直接: OrderLine</span><span class="sxs-lookup"><span data-stu-id="63f39-244">Sales Orders (Supply Chain Management to Sales) - Direct: OrderLine</span></span>

<span data-ttu-id="63f39-245">[![データ統合のテンプレートのマッピング](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)</span><span class="sxs-lookup"><span data-stu-id="63f39-245">[![Template mapping in Data integration](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)</span></span>

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderheader"></a><span data-ttu-id="63f39-246">販売注文 (Sales から Supply Chain Management) - 直接: OrderHeader</span><span class="sxs-lookup"><span data-stu-id="63f39-246">Sales Orders (Sales to Supply Chain Management) - Direct: OrderHeader</span></span>

<span data-ttu-id="63f39-247">[![データ統合のテンプレートのマッピング](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)</span><span class="sxs-lookup"><span data-stu-id="63f39-247">[![Template mapping in Data integration](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)</span></span>

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderline"></a><span data-ttu-id="63f39-248">販売注文 (Sales から Supply Chain Management) - 直接: OrderLine</span><span class="sxs-lookup"><span data-stu-id="63f39-248">Sales Orders (Sales to Supply Chain Management) - Direct: OrderLine</span></span>

<span data-ttu-id="63f39-249">[![データ統合のテンプレートのマッピング](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)</span><span class="sxs-lookup"><span data-stu-id="63f39-249">[![Template mapping in Data integration](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)</span></span>

## <a name="related-topics"></a><span data-ttu-id="63f39-250">関連トピック</span><span class="sxs-lookup"><span data-stu-id="63f39-250">Related topics</span></span>

[<span data-ttu-id="63f39-251">見込顧客を現金化</span><span class="sxs-lookup"><span data-stu-id="63f39-251">Prospect to cash</span></span>](prospect-to-cash.md)
