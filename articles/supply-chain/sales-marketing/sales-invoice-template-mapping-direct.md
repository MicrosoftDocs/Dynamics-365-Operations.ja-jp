---
title: 売上請求書のヘッダーおよび明細行の Supply Chain Management から Sales への直接同期
description: このトピックでは、Dynamics 365 Supply Chain Management から Dynamics 365 Sales に売上請求書ヘッダーおよび明細行を直接同期するために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
manager: tfehr
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 6cbc4d86ac41d90480428ec5439d1360c4d67137
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215979"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="f0db3-103">Finance and Operations から Sales への請求書ヘッダーおよび明細行の直接同期</span><span class="sxs-lookup"><span data-stu-id="f0db3-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0db3-104">このトピックでは、Dynamics 365 Supply Chain Management から Dynamics 365 Sales に売上請求書ヘッダーおよび明細行を直接同期するために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f0db3-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="f0db3-105">見込み客の現金化へのデータフロー</span><span class="sxs-lookup"><span data-stu-id="f0db3-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="f0db3-106">見込み客の現金化ソリューションは、Supply Chain Management と Sales のインスタンス間でデータを同期するため、データの統合機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="f0db3-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="f0db3-107">データ統合機能で利用可能な見込み顧客を現金化するテンプレートにより、Supply Chain Management と Sales 間での勘定、連絡先、製品および販売見積、販売注文、および売上請求書のデータの流れが可能になります。</span><span class="sxs-lookup"><span data-stu-id="f0db3-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="f0db3-108">次の図は、Supply Chain Management と Sales の間でデータを同期させる方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="f0db3-108">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="f0db3-109">[![見込み客の現金化へのデータフロー](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="f0db3-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="f0db3-110">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="f0db3-110">Templates and tasks</span></span>

<span data-ttu-id="f0db3-111">利用可能なテンプレートにアクセスするには、[Power Apps 管理者センター](https://preview.admin.powerapps.com/dataintegration)を開きます。</span><span class="sxs-lookup"><span data-stu-id="f0db3-111">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="f0db3-112">**プロジェクト**を選択した後、右上隅にある **新しいプロジェクト** を選択してパブリック テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="f0db3-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="f0db3-113">Supply Chain Management から Sales への販売請求書ヘッダーと明細行の同期には、以下のテンプレートと基本的なタスクが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f0db3-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Supply Chain Management to Sales:</span></span>

- <span data-ttu-id="f0db3-114">**データ統合における テンプレートの名前:** 売上請求書 (Finance and Operations から Sales) - 直接</span><span class="sxs-lookup"><span data-stu-id="f0db3-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="f0db3-115">**データ統合プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="f0db3-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="f0db3-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="f0db3-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="f0db3-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="f0db3-117">SalesInvoiceLine</span></span>

<span data-ttu-id="f0db3-118">販売請求書ヘッダーと明細行を同期させるには、次の同期タスクが必要です。</span><span class="sxs-lookup"><span data-stu-id="f0db3-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="f0db3-119">製品 (Supply Chain Management から Sales) - 直接</span><span class="sxs-lookup"><span data-stu-id="f0db3-119">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="f0db3-120">勘定 (Sales から Supply Chain Management) - ダイレクト (使用する場合)</span><span class="sxs-lookup"><span data-stu-id="f0db3-120">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="f0db3-121">連絡先 (Sales から Supply Chain Management) - ダイレクト (使用する場合)</span><span class="sxs-lookup"><span data-stu-id="f0db3-121">Contacts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="f0db3-122">販売注文ヘッダーおよび明細行 (Supply Chain Management から Sales) - ダイレクト</span><span class="sxs-lookup"><span data-stu-id="f0db3-122">Sales order header and lines (Supply Chain Management to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="f0db3-123">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="f0db3-123">Entity set</span></span>

| <span data-ttu-id="f0db3-124">サプライ チェーン マネジメント</span><span class="sxs-lookup"><span data-stu-id="f0db3-124">Supply Chain Management</span></span>                              | <span data-ttu-id="f0db3-125">販売注文</span><span class="sxs-lookup"><span data-stu-id="f0db3-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="f0db3-126">外部的に管理された顧客の売上請求書ヘッダー</span><span class="sxs-lookup"><span data-stu-id="f0db3-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="f0db3-127">請求書</span><span class="sxs-lookup"><span data-stu-id="f0db3-127">Invoices</span></span>       |
| <span data-ttu-id="f0db3-128">外部的に管理された顧客の売上請求書明細行</span><span class="sxs-lookup"><span data-stu-id="f0db3-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="f0db3-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="f0db3-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="f0db3-130">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="f0db3-130">Entity flow</span></span>

<span data-ttu-id="f0db3-131">売上請求書が Supply Chain Management で作成され、Sales に同期されます。</span><span class="sxs-lookup"><span data-stu-id="f0db3-131">Sales invoices are created in Supply Chain Management and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="f0db3-132">現在、売上請求書ヘッダー上の税に関連する費用は、Supply Chain Managements から Sales への同期には含まれていません。</span><span class="sxs-lookup"><span data-stu-id="f0db3-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Supply Chain Managements to Sales.</span></span> <span data-ttu-id="f0db3-133">これは Sales がヘッダー レベルでの税金情報をサポートしていないためです。</span><span class="sxs-lookup"><span data-stu-id="f0db3-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="f0db3-134">ただし、同期の明細行レベルでの税に関連する費用が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f0db3-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="f0db3-135">売上の見込顧客を現金化するソリューション</span><span class="sxs-lookup"><span data-stu-id="f0db3-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="f0db3-136">**請求書番号**フィールドが**請求書**エンティティに追加され、ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f0db3-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="f0db3-137">請求書が Supply Chain Management で作成され、Sales に同期されるため、**販売注文**ページの**請求書の作成**ボタンは非表示になります。</span><span class="sxs-lookup"><span data-stu-id="f0db3-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="f0db3-138">請求書が Supply Chain Management から同期されるため、**請求書**ページは編集できません。</span><span class="sxs-lookup"><span data-stu-id="f0db3-138">The **Invoice** page can't be edited, because invoices will be synchronized from Supply Chain Management.</span></span>
- <span data-ttu-id="f0db3-139">Supply Chain Management からの関連請求書が Sales に同期されると、**販売注文状態**値は自動的に**請求済**に変更されます。</span><span class="sxs-lookup"><span data-stu-id="f0db3-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Supply Chain Management has been synchronized to Sales.</span></span> <span data-ttu-id="f0db3-140">さらに、請求書の作成元である販売注文の所有者は、請求書の所有者として割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="f0db3-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="f0db3-141">したがって、販売注文書の所有者は、請求書を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="f0db3-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="f0db3-142">前提条件とマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="f0db3-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="f0db3-143">売上請求書を同期する前に、システムで以下の設定を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0db3-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="f0db3-144">Sales での設定</span><span class="sxs-lookup"><span data-stu-id="f0db3-144">Setup in Sales</span></span>

<span data-ttu-id="f0db3-145">**設定** > **管理** > **システムの設定** > **Sales** の順に移動し、次の設定を使用することを確認します。</span><span class="sxs-lookup"><span data-stu-id="f0db3-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="f0db3-146">**システム プライジング計算システムの使用** オプションが、**はい** に設定されている。</span><span class="sxs-lookup"><span data-stu-id="f0db3-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="f0db3-147">**割引の計算方法**フィールドが、**明細行品目**に設定されている。</span><span class="sxs-lookup"><span data-stu-id="f0db3-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="f0db3-148">データ統合プロジェクトでの設定</span><span class="sxs-lookup"><span data-stu-id="f0db3-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="f0db3-149">SalesInvoiceHeader タスク</span><span class="sxs-lookup"><span data-stu-id="f0db3-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="f0db3-150">**InvoiceCountryRegionId** から **BillingAddress\_Country** に必要なマッピングが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="f0db3-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="f0db3-151">テンプレートの値は、複数の国または地域がマップされている値マップです。</span><span class="sxs-lookup"><span data-stu-id="f0db3-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="f0db3-152">Sales で請求書を作成するには価格リストが必要です。</span><span class="sxs-lookup"><span data-stu-id="f0db3-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="f0db3-153">Sales で通貨ごとに使用される価格リストへの **pricelevelid.name \[価格リスト名\]** の値マップを更新します。</span><span class="sxs-lookup"><span data-stu-id="f0db3-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="f0db3-154">1つの通貨に対する既定の価格リストを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="f0db3-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="f0db3-155">または、複数の通貨で価格リストがある場合、値マップを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="f0db3-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="f0db3-156">**pricelevelid.name\[価格リスト名\]** のテンプレート値は、USD = CRM サービス USA (サンプル) のように通貨に基づく値マップです。</span><span class="sxs-lookup"><span data-stu-id="f0db3-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="f0db3-157">SalesInvoiceLine タスク</span><span class="sxs-lookup"><span data-stu-id="f0db3-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="f0db3-158">**測定単位**で必要なマッピングが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="f0db3-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="f0db3-159">Supply Chain Management の **SalesUnitSymbol** に必要な値マップが存在することを確認して下さい。</span><span class="sxs-lookup"><span data-stu-id="f0db3-159">Make sure that the required value map for **SalesUnitSymbol** in Supply Chain Management exists.</span></span>

    <span data-ttu-id="f0db3-160">**SalesUnitSymbol** から **Quantity\_** UMO に対して値マップを持つテンプレート値が定義されます。</span><span class="sxs-lookup"><span data-stu-id="f0db3-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f0db3-161">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="f0db3-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="f0db3-162">**支払条件**、**運賃条件**、**配送条件**、**送付方法**、および **配送モード** フィールドは、既定のマッピングには含まれていません。</span><span class="sxs-lookup"><span data-stu-id="f0db3-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="f0db3-163">これらのフィールドをマップするには、エンティティ間で同期される組織内のデータに固有の値マッピングを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0db3-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="f0db3-164">次の図は、データ統合のテンプレート マッピングの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="f0db3-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="f0db3-165">マッピングは、Sales から Supply Chain Management にどのフィールド情報を同期するかを表示します。</span><span class="sxs-lookup"><span data-stu-id="f0db3-165">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="f0db3-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="f0db3-166">SalesInvoiceHeader</span></span>

![データ統合のテンプレートのマッピング](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="f0db3-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="f0db3-168">SalesInvoiceLine</span></span>

![データ統合のテンプレートのマッピング](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="f0db3-170">関連トピック</span><span class="sxs-lookup"><span data-stu-id="f0db3-170">Related topics</span></span>

[<span data-ttu-id="f0db3-171">見込顧客を現金化</span><span class="sxs-lookup"><span data-stu-id="f0db3-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="f0db3-172">Supply Chain Management の顧客への Sales の勘定の直接同期</span><span class="sxs-lookup"><span data-stu-id="f0db3-172">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="f0db3-173">製品を Supply Chain Management から Sales の製品に直接同期する</span><span class="sxs-lookup"><span data-stu-id="f0db3-173">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="f0db3-174">Supply Chain Management の連絡先または顧客への Sales の連絡先の直接同期</span><span class="sxs-lookup"><span data-stu-id="f0db3-174">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="f0db3-175">販売注文の Sales と Supply Chain Management の間の直接同期</span><span class="sxs-lookup"><span data-stu-id="f0db3-175">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)
