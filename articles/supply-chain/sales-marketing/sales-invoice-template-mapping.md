---
title: "売上請求書ヘッダーおよび明細行の Finance and Operations から Sales への同期"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations, Enterprise edition から Microsoft Dynamics 365 for Sales に対して、売上請求書ヘッダーと明細行を同期するために使用されるテンプレートと基本的なタスクについて説明します。"
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 22ab02555dcac850b18aac9564af41d6c627eade
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="3894d-103">売上請求書ヘッダーおよび明細行の Finance and Operations から Sales への同期</span><span class="sxs-lookup"><span data-stu-id="3894d-103">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3894d-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations, Enterprise edition から Microsoft Dynamics 365 for Sales に対して、売上請求書ヘッダーと明細行を同期するために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="3894d-104">The topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="3894d-105">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="3894d-105">Templates and tasks</span></span>

<span data-ttu-id="3894d-106">Finance and Operations から Sales への売上請求書ヘッダーと明細行の同期には、以下のテンプレートと基本的なタスクが使用されます。</span><span class="sxs-lookup"><span data-stu-id="3894d-106">The following templates and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="3894d-107">**データ統合でのテンプレートの名前**</span><span class="sxs-lookup"><span data-stu-id="3894d-107">**Name of the template in Data integration**</span></span> 

     - <span data-ttu-id="3894d-108">売上請求書 (Finance and Operations から Sales)</span><span class="sxs-lookup"><span data-stu-id="3894d-108">Sales Invoices (Fin and Ops to Sales)</span></span>

- <span data-ttu-id="3894d-109">**データ統合プロジェクトのタスク名**</span><span class="sxs-lookup"><span data-stu-id="3894d-109">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="3894d-110">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="3894d-110">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="3894d-111">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="3894d-111">SalesInvoiceLine</span></span>

<span data-ttu-id="3894d-112">売上請求書ヘッダーおよび明細行の同期より前に必要な同期タスク。</span><span class="sxs-lookup"><span data-stu-id="3894d-112">Sync tasks required prior to Sales invoice header and lines synchronization:</span></span>
-   <span data-ttu-id="3894d-113">製品 (Finance and Operations から Sales)</span><span class="sxs-lookup"><span data-stu-id="3894d-113">Products (Fin and Ops to Sales)</span></span>
-   <span data-ttu-id="3894d-114">勘定 (Sales から Finance and Operations) (使用されている場合)</span><span class="sxs-lookup"><span data-stu-id="3894d-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="3894d-115">連絡先 (Sales から Finance and Operations) (使用されている場合)</span><span class="sxs-lookup"><span data-stu-id="3894d-115">Contacts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="3894d-116">販売注文ヘッダーおよび明細行 (Finance and Operations から Sales)</span><span class="sxs-lookup"><span data-stu-id="3894d-116">Sales order header and lines (Fin and Ops to Sales)</span></span>

## <a name="entity-set"></a><span data-ttu-id="3894d-117">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="3894d-117">Entity set</span></span>

| <span data-ttu-id="3894d-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3894d-118">Finance and Operations</span></span>                               | <span data-ttu-id="3894d-119">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="3894d-119">Common Data Service (CDS)</span></span>              | <span data-ttu-id="3894d-120">売上</span><span class="sxs-lookup"><span data-stu-id="3894d-120">Sales</span></span>          |
|------------------------------------------------------|------------------|----------------|
| <span data-ttu-id="3894d-121">外部的に管理された顧客の売上請求書ヘッダー</span><span class="sxs-lookup"><span data-stu-id="3894d-121">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="3894d-122">SalesInvoice</span><span class="sxs-lookup"><span data-stu-id="3894d-122">SalesInvoice</span></span>     | <span data-ttu-id="3894d-123">請求書</span><span class="sxs-lookup"><span data-stu-id="3894d-123">Invoices</span></span>       |
| <span data-ttu-id="3894d-124">外部的に管理された顧客の売上請求書明細行</span><span class="sxs-lookup"><span data-stu-id="3894d-124">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="3894d-125">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="3894d-125">SalesInvoiceLine</span></span> | <span data-ttu-id="3894d-126">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="3894d-126">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="3894d-127">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="3894d-127">Entity flow</span></span>

<span data-ttu-id="3894d-128">売上請求書が Finance and Operations で作成され Sales に同期されます。</span><span class="sxs-lookup"><span data-stu-id="3894d-128">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="3894d-129">[**売上請求書ヘッダー**] での税に関連する費用は、現在 Finance and Operations から Sales への同期に含まれていません。</span><span class="sxs-lookup"><span data-stu-id="3894d-129">Tax related to charges on the **Sales invoice header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="3894d-130">これは Sales がヘッダー レベルでの税金情報をサポートしていないためです。</span><span class="sxs-lookup"><span data-stu-id="3894d-130">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="3894d-131">明細行レベルでの税に関連する費用が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3894d-131">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="3894d-132">売上の見込顧客を現金化するソリューション</span><span class="sxs-lookup"><span data-stu-id="3894d-132">Prospect to cash solution for Sales</span></span>

-  <span data-ttu-id="3894d-133">[**請求書番号フィールドで**] が [**請求書**] エンティティに追加され、ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="3894d-133">An **Invoice number field** is added to the **Invoice** entity and displayed on the page.</span></span>
 
-  <span data-ttu-id="3894d-134">請求書が Finance and Operations で作成され Sales に同期されるため、[**販売注文**] ページで [**請求書の作成**] ボタンは非表示になります。</span><span class="sxs-lookup"><span data-stu-id="3894d-134">The **Create invoice** button on the **Sales order** page is hidden because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="3894d-135">請求書は Finance and Operations から同期されるため、[**請求書**] ページは編集できません。</span><span class="sxs-lookup"><span data-stu-id="3894d-135">The **Invoice** page is non-editable because invoices will be synced from Finance and Operations.</span></span>
 
-  <span data-ttu-id="3894d-136">Finance and Operations からの関連する請求書が Sales に同期されると、[**販売注文状態**] は自動的に [**請求済**] に変更します。</span><span class="sxs-lookup"><span data-stu-id="3894d-136">The **Sales order status** changes automatically to **Invoiced** when the related invoice from Finance and Operations has been  synchronized to Sales.</span></span> <span data-ttu-id="3894d-137">また、請求書の作成元である販売注文の所有者は、請求書の所有者として割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="3894d-137">Also, the owner of the sales order from which the invoice was created is assigned as the owner of the invoice.</span></span> <span data-ttu-id="3894d-138">これにより、販売注文書の所有者は、請求書を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="3894d-138">This gives the owner of the sales order the ability to view the invoice.</span></span>
 
## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="3894d-139">前提条件とマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="3894d-139">Preconditions and mapping setup</span></span>

<span data-ttu-id="3894d-140">売上請求書を同期する前に、次の設定でシステムを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3894d-140">Before synchronizing sales invoices, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="3894d-141">Sales での設定</span><span class="sxs-lookup"><span data-stu-id="3894d-141">Setup in Sales</span></span>

- <span data-ttu-id="3894d-142">[**設定**] > [**管理**] > [**システム設定**] > [**販売**] で、[**システム プライジング計算システムの使用**] が [**はい**] に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3894d-142">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="3894d-143">[**設定**] > [**管理**] > [**システム設定**] > [**販売**] で、[**割引の計算方法**] が [**明細行品目**] に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3894d-143">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="3894d-144">データ統合プロジェクトでの設定</span><span class="sxs-lookup"><span data-stu-id="3894d-144">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="3894d-145">SalesInvoiceHeader タスク</span><span class="sxs-lookup"><span data-stu-id="3894d-145">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="3894d-146">[**ソース**] > [**CDS**] で [**CDS 組織 ID**] のマッピングを更新します。</span><span class="sxs-lookup"><span data-stu-id="3894d-146">Update the mapping for **CDS Organization ID** in **Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="3894d-147">[**SalesOrder_Organization_OrganizationId**] の規定のテンプレート値は ORG001 です。</span><span class="sxs-lookup"><span data-stu-id="3894d-147">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="3894d-148">[**Account_Organization_OrganizationId**] の既定のテンプレート値は ORG001 です。</span><span class="sxs-lookup"><span data-stu-id="3894d-148">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="3894d-149">[**Organization_OrganizationId**] の既定のテンプレート値は ORG001 です。</span><span class="sxs-lookup"><span data-stu-id="3894d-149">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="3894d-150">[**ソース**] > [**InvoiceCountryRegionId 用 CDs**] で [**BillingAddress_Country**] に必要なマッピングが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="3894d-150">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId** to **BillingAddress_Country**.</span></span>

    -  <span data-ttu-id="3894d-151">マップされている国の数のテンプレート値は [**ValueMap**] です。</span><span class="sxs-lookup"><span data-stu-id="3894d-151">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="3894d-152">Sales で売上請求書を作成するために [**価格リスト**] が必要です。</span><span class="sxs-lookup"><span data-stu-id="3894d-152">**Price list** is required to create invoices in Sales.</span></span> <span data-ttu-id="3894d-153">[**CDS**] > [**pricelevelid.name [価格リスト名] の出力先**] で、Sales で通貨ごとに使用される [**価格リスト**] への [**ValueMap**] を更新します。</span><span class="sxs-lookup"><span data-stu-id="3894d-153">Update the **ValueMap** in **CDS** > **Destination for pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="3894d-154">1 つの通貨に対する既定の [**価格リスト**] を使用するか、または複数の通貨で [**価格リスト**] がある場合 [**ValueMap**] を使用するかのいずれかができます。</span><span class="sxs-lookup"><span data-stu-id="3894d-154">You can either use the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>

    -  <span data-ttu-id="3894d-155">[**pricelevelid.name [価格リスト名]**] のテンプレート値は [**通貨**] に基づく [**ValueMap**] です。</span><span class="sxs-lookup"><span data-stu-id="3894d-155">Template value for **pricelevelid.name [Price List Name]** is **ValueMap** based on **Currency**.</span></span>
    -  <span data-ttu-id="3894d-156">usd: CRM サービス USA (サンプル)。</span><span class="sxs-lookup"><span data-stu-id="3894d-156">usd: CRM Service USA (sample).</span></span> 

#### <a name="salesinvoiceline-task"></a><span data-ttu-id="3894d-157">SalesInvoiceLine タスク</span><span class="sxs-lookup"><span data-stu-id="3894d-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="3894d-158">[**ソース**] > [**測定単位の CDS**] で必要なマッピングが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="3894d-158">Ensure that the needed mapping exists in **Source** > **CDS for Unit of measure**.</span></span>

- <span data-ttu-id="3894d-159">[**ソース**] > [**CDマッピング**] に存在する Finance and Operations で、[**SalesUnitSymbol**] 用の必要な [**ValueMap**] を確認します。</span><span class="sxs-lookup"><span data-stu-id="3894d-159">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span> 
    
    - <span data-ttu-id="3894d-160">[**Quantity_UOMにSalesUnitSymbol**] に対して [**ValueMap**] を持つテンプレート値が定義されます。</span><span class="sxs-lookup"><span data-stu-id="3894d-160">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>
    
-  <span data-ttu-id="3894d-161">[**ソースでの CDS 組織 ID**] > [**CDS**] に対するマッピングを更新します。</span><span class="sxs-lookup"><span data-stu-id="3894d-161">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="3894d-162">[**SalesInvoicer_Organization_OrganizationId**] の規定のテンプレート値は ORG001 です。</span><span class="sxs-lookup"><span data-stu-id="3894d-162">Default template value for **SalesInvoicer_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="3894d-163">[**Product_Organization_OrganizationId**] の既定のテンプレート値は ORG001 です。</span><span class="sxs-lookup"><span data-stu-id="3894d-163">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>
 
## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="3894d-164">データ インテグレーターのテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="3894d-164">Template mapping in Data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="3894d-165">[**支払条件**]、[**運賃条件**]、[**配送条件**]、[**送付方法**]、および [**配送モード**] は、既定のマッピングの一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="3894d-165">**Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** are not part of the default mappings.</span></span> <span data-ttu-id="3894d-166">これらのフィールドのマッピングには、エンティティ間で同期される組織内のデータに固有の、設定される値マッピングが必要になります。</span><span class="sxs-lookup"><span data-stu-id="3894d-166">Mapping of these fields requires value mapping to be set up, which is specific to the data in the organizations between which the entity is synchronized.</span></span>

<span data-ttu-id="3894d-167">次の図は、データ インテグレーターのテンプレート マッピングの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="3894d-167">The following illustrations show an example of a template mapping in data integrator.</span></span>

![データ インテグレーターでテンプレートのマッピング](./media/sales-invoice-template-mapping-data-integrator-1.png)

![データ インテグレーターでテンプレートのマッピング](./media/sales-invoice-template-mapping-data-integrator-2.png)

![データ インテグレーターでテンプレートのマッピング](./media/sales-invoice-template-mapping-data-integrator-3.png)

![データ インテグレーターでテンプレートのマッピング](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="3894d-172">関連トピック</span><span class="sxs-lookup"><span data-stu-id="3894d-172">Related topics</span></span>

[<span data-ttu-id="3894d-173">Finance and Operations の製品を売上の製品に同期する</span><span class="sxs-lookup"><span data-stu-id="3894d-173">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="3894d-174">Finance and Operations の顧客への Sales の勘定の同期</span><span class="sxs-lookup"><span data-stu-id="3894d-174">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="3894d-175">Finance and Operations の連絡先または顧客への Sales の連絡先の同期</span><span class="sxs-lookup"><span data-stu-id="3894d-175">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="3894d-176">販売見積ヘッダーおよび明細行の Sales から Finance and Operations への同期</span><span class="sxs-lookup"><span data-stu-id="3894d-176">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="3894d-177">販売注文ヘッダーおよび明細行の Finance and Operations から Sales への同期</span><span class="sxs-lookup"><span data-stu-id="3894d-177">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)


