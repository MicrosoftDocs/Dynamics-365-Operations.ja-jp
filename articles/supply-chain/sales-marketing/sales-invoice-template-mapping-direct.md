---
title: "売上請求書ヘッダーおよび明細行の Finance and Operations から Sales への直接同期"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Sales に対して、売上請求書ヘッダーと明細行を直接同期するために使用されるテンプレートと基本的なタスクについて説明します。"
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fda4dff829f933eca8b1e3e6bba5e56dd3304190
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="2d91d-103">売上請求書ヘッダーおよび明細行の Finance and Operations から Sales への直接同期</span><span class="sxs-lookup"><span data-stu-id="2d91d-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d91d-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Sales に対して、売上請求書ヘッダーと明細行を直接同期するために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2d91d-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="2d91d-105">見込み客の現金化へのデータフロー</span><span class="sxs-lookup"><span data-stu-id="2d91d-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="2d91d-106">見込み客の現金化ソリューションは、Finance and Operations と Sales のインスタンス間でデータを同期するため、データの統合機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="2d91d-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="2d91d-107">データ統合機能で利用可能な見込み顧客を現金化するテンプレートは、Finance and Operations と Sales 間での勘定、連絡先、製品および販売見積、販売注文、および売上請求書データの流れを可能にします。</span><span class="sxs-lookup"><span data-stu-id="2d91d-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="2d91d-108">次の図は、Finance and Operations と Sales の間でデータを同期させる方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="2d91d-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="2d91d-109">[![見込み客の現金化へのデータフロー](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="2d91d-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="2d91d-110">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="2d91d-110">Templates and tasks</span></span>

<span data-ttu-id="2d91d-111">利用可能なテンプレートにアクセスするには、[PowerApps 管理者センター](https://preview.admin.powerapps.com/dataintegration) を開きます。</span><span class="sxs-lookup"><span data-stu-id="2d91d-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="2d91d-112">**プロジェクト**を選択した後、右上隅にある **新しいプロジェクト** を選択してパブリック テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="2d91d-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="2d91d-113">Finance and Operations から Sales への売上請求書ヘッダーと明細行の同期には、以下のテンプレートと基本的なタスクが使用されます。</span><span class="sxs-lookup"><span data-stu-id="2d91d-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="2d91d-114">**データ統合における テンプレートの名前:** 売上請求書 (Finance and Operations から Sales) - 直接</span><span class="sxs-lookup"><span data-stu-id="2d91d-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="2d91d-115">**データ統合プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="2d91d-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="2d91d-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="2d91d-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="2d91d-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="2d91d-117">SalesInvoiceLine</span></span>

<span data-ttu-id="2d91d-118">販売請求書ヘッダーと明細行を同期させるには、次の同期タスクが必要です。</span><span class="sxs-lookup"><span data-stu-id="2d91d-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="2d91d-119">製品 (Finance and Operations から Sales) - 直接</span><span class="sxs-lookup"><span data-stu-id="2d91d-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="2d91d-120">勘定 (Sales から Finance and Operations) - 直接(使用されている場合)</span><span class="sxs-lookup"><span data-stu-id="2d91d-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="2d91d-121">連絡先 (Sales から Finance and Operations) - 直接(使用されている場合)</span><span class="sxs-lookup"><span data-stu-id="2d91d-121">Contacts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="2d91d-122">販売注文ヘッダーおよび明細行 (Finance and Operations から Sales) - ダイレクト</span><span class="sxs-lookup"><span data-stu-id="2d91d-122">Sales order header and lines (Fin and Ops to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="2d91d-123">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="2d91d-123">Entity set</span></span>

| <span data-ttu-id="2d91d-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2d91d-124">Finance and Operations</span></span>                               | <span data-ttu-id="2d91d-125">売上</span><span class="sxs-lookup"><span data-stu-id="2d91d-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="2d91d-126">外部的に管理された顧客の売上請求書ヘッダー</span><span class="sxs-lookup"><span data-stu-id="2d91d-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="2d91d-127">請求書</span><span class="sxs-lookup"><span data-stu-id="2d91d-127">Invoices</span></span>       |
| <span data-ttu-id="2d91d-128">外部的に管理された顧客の売上請求書明細行</span><span class="sxs-lookup"><span data-stu-id="2d91d-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="2d91d-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="2d91d-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="2d91d-130">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="2d91d-130">Entity flow</span></span>

<span data-ttu-id="2d91d-131">売上請求書が Finance and Operations で作成され Sales に同期されます。</span><span class="sxs-lookup"><span data-stu-id="2d91d-131">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="2d91d-132">売上請求書ヘッダーでの税に関連する費用は、現在 Finance and Operations から Sales への同期に含まれていません。</span><span class="sxs-lookup"><span data-stu-id="2d91d-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="2d91d-133">これは Sales がヘッダー レベルでの税金情報をサポートしていないためです。</span><span class="sxs-lookup"><span data-stu-id="2d91d-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="2d91d-134">ただし、同期の明細行レベルでの税に関連する費用が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2d91d-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="2d91d-135">売上の見込顧客を現金化するソリューション</span><span class="sxs-lookup"><span data-stu-id="2d91d-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="2d91d-136">[請求書番号] フィールドが [請求書] エンティティに追加され、ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="2d91d-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="2d91d-137">請求書が Finance and Operations で作成され Sales に同期されるため、[販売注文] ページで [請求書の作成] ボタンは非表示になります。</span><span class="sxs-lookup"><span data-stu-id="2d91d-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="2d91d-138">請求書は Finance and Operations から同期されるため、[請求書] ページは編集できません。</span><span class="sxs-lookup"><span data-stu-id="2d91d-138">The **Invoice** page can't be edited, because invoices will be synchronized from Finance and Operations.</span></span>
- <span data-ttu-id="2d91d-139">Finance and Operations からの関連する請求書が Sales に同期されると、[販売注文状態] 値は自動的に [請求済] に変更します。</span><span class="sxs-lookup"><span data-stu-id="2d91d-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Finance and Operations has been synchronized to Sales.</span></span> <span data-ttu-id="2d91d-140">さらに、請求書の作成元である販売注文の所有者は、請求書の所有者として割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="2d91d-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="2d91d-141">したがって、販売注文書の所有者は、請求書を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="2d91d-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="2d91d-142">前提条件とマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="2d91d-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="2d91d-143">売上請求書を同期する前に、システムで以下の設定を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2d91d-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="2d91d-144">Sales での設定</span><span class="sxs-lookup"><span data-stu-id="2d91d-144">Setup in Sales</span></span>

<span data-ttu-id="2d91d-145">[設定] > [管理] > [システムの設定] > [Sales] の順に移動し、次の設定を使用することを確認します。</span><span class="sxs-lookup"><span data-stu-id="2d91d-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="2d91d-146">[**システム プライジング計算システムの使用**] オプションが、[**はい**] に設定されている。</span><span class="sxs-lookup"><span data-stu-id="2d91d-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="2d91d-147">[割引の計算方法] フィールドが、[明細行品目] に設定されている。</span><span class="sxs-lookup"><span data-stu-id="2d91d-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="2d91d-148">データ統合プロジェクトでの設定</span><span class="sxs-lookup"><span data-stu-id="2d91d-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="2d91d-149">SalesInvoiceHeader タスク</span><span class="sxs-lookup"><span data-stu-id="2d91d-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="2d91d-150">[InvoiceCountryRegionId] から [BillingAddress\_Country] に必要なマッピングが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="2d91d-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="2d91d-151">テンプレートの値は、複数の国または地域がマップされている値マップです。</span><span class="sxs-lookup"><span data-stu-id="2d91d-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="2d91d-152">Sales で請求書を作成するには価格リストが必要です。</span><span class="sxs-lookup"><span data-stu-id="2d91d-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="2d91d-153">Sales で通貨ごとに使用される価格リストへの [pricelevelid.name \[価格リスト名\]] の値マップを更新します。</span><span class="sxs-lookup"><span data-stu-id="2d91d-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="2d91d-154">1つの通貨に対する既定の価格リストを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="2d91d-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="2d91d-155">または、複数の通貨で価格リストがある場合、値マップを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="2d91d-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="2d91d-156">[pricelevelid.name\[価格リスト名\]] のテンプレート値は、USD = CRM サービス USA (サンプル) のように通貨に基づく値マップです。</span><span class="sxs-lookup"><span data-stu-id="2d91d-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="2d91d-157">SalesInvoiceLine タスク</span><span class="sxs-lookup"><span data-stu-id="2d91d-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="2d91d-158">[測定単位] で必要なマッピングが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="2d91d-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="2d91d-159">Finance and Operation で [SalesUnitSymbol] 用の必要な値マップを確認します。</span><span class="sxs-lookup"><span data-stu-id="2d91d-159">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="2d91d-160">[**SalesUnitSymbol**] から [**Quantity\_** UMO] に対して値マップを持つテンプレート値が定義されます。</span><span class="sxs-lookup"><span data-stu-id="2d91d-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="2d91d-161">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="2d91d-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="2d91d-162">[**支払条件**]、[**運賃条件**]、[**配送条件**]、[**送付方法**]、および [**配送モード**] フィールドは、既定のマッピングには含まれていません。</span><span class="sxs-lookup"><span data-stu-id="2d91d-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="2d91d-163">これらのフィールドをマップするには、エンティティ間で同期される組織内のデータに固有の値マッピングを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2d91d-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="2d91d-164">次の図は、データ統合のテンプレート マッピングの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="2d91d-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="2d91d-165">マッピングは、Sales から Finance and Operations にどのフィールド情報を同期するかを表示します。</span><span class="sxs-lookup"><span data-stu-id="2d91d-165">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="2d91d-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="2d91d-166">SalesInvoiceHeader</span></span>

![データ統合のテンプレートのマッピング](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="2d91d-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="2d91d-168">SalesInvoiceLine</span></span>

![データ統合のテンプレートのマッピング](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="2d91d-170">関連トピック</span><span class="sxs-lookup"><span data-stu-id="2d91d-170">Related topics</span></span>

[<span data-ttu-id="2d91d-171">見込顧客を現金化</span><span class="sxs-lookup"><span data-stu-id="2d91d-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="2d91d-172">Sales から Finance and Operations の顧客への勘定の直接同期</span><span class="sxs-lookup"><span data-stu-id="2d91d-172">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="2d91d-173">Sales 製品への Finance and Operations の製品の直接同期</span><span class="sxs-lookup"><span data-stu-id="2d91d-173">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="2d91d-174">Finance and Operations の連絡先または顧客への Sales の連絡先の直接同期</span><span class="sxs-lookup"><span data-stu-id="2d91d-174">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="2d91d-175">販売注文ヘッダーおよび明細行の Finance and Operations から Sales への直接同期</span><span class="sxs-lookup"><span data-stu-id="2d91d-175">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)







