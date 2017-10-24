---
title: "販売注文ヘッダーおよび明細行の Finance and Operations から Sales への同期"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations, Enterprise edition から Microsoft Dynamics 365 for Sales に対して、販売注文ヘッダーと明細行を同期するために使用されるテンプレートと基本的なタスクについて説明します。"
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
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 707efc97afc0679ed1fc22539789e98cbabcb581
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="83d8f-103">販売注文ヘッダーおよび明細行の Finance and Operations から Sales への同期</span><span class="sxs-lookup"><span data-stu-id="83d8f-103">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="83d8f-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations, Enterprise edition から Microsoft Dynamics 365 for Sales に対して、販売注文ヘッダーと明細行を同期するために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="83d8f-104">The topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="83d8f-105">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="83d8f-105">Template and tasks</span></span>

<span data-ttu-id="83d8f-106">Finance and Operations から Sales への販売注文ヘッダーと明細行の同期には、以下のテンプレートと基本的なタスクが使用されます。</span><span class="sxs-lookup"><span data-stu-id="83d8f-106">The following templates and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="83d8f-107">[**データ統合でのテンプレートの名前**]</span><span class="sxs-lookup"><span data-stu-id="83d8f-107">**Name of template in Data integration**</span></span> 

    - <span data-ttu-id="83d8f-108">販売注文 (Finance and Operations から Sales)</span><span class="sxs-lookup"><span data-stu-id="83d8f-108">Sales Orders (Fin and Ops to Sales)</span></span>
    
- <span data-ttu-id="83d8f-109">[**データ統合プロジェクトのタスク名**]</span><span class="sxs-lookup"><span data-stu-id="83d8f-109">**Names of tasks in Data integration project**</span></span>

    - <span data-ttu-id="83d8f-110">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="83d8f-110">OrderHeader</span></span>
    - <span data-ttu-id="83d8f-111">OrderLine</span><span class="sxs-lookup"><span data-stu-id="83d8f-111">OrderLine</span></span>

<span data-ttu-id="83d8f-112">売上請求書ヘッダーおよび明細行の同期より前に必要な同期タスク。</span><span class="sxs-lookup"><span data-stu-id="83d8f-112">Sync tasks required prior to Sales invoice header and lines sync:</span></span>

- <span data-ttu-id="83d8f-113">製品 (Finance and Operations から Sales)</span><span class="sxs-lookup"><span data-stu-id="83d8f-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="83d8f-114">勘定 (Sales から Finance and Operations) (使用されている場合)</span><span class="sxs-lookup"><span data-stu-id="83d8f-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="83d8f-115">顧客への連絡先 (Sales から Finance and Operations) (使用されている場合)</span><span class="sxs-lookup"><span data-stu-id="83d8f-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="83d8f-116">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="83d8f-116">Entity set</span></span>

| <span data-ttu-id="83d8f-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="83d8f-117">Finance and Operations</span></span> |    <span data-ttu-id="83d8f-118">Common Data Service (CDS)</span><span class="sxs-lookup"><span data-stu-id="83d8f-118">Common Data Service (CDS)</span></span>         |     <span data-ttu-id="83d8f-119">売上</span><span class="sxs-lookup"><span data-stu-id="83d8f-119">Sales</span></span>      |
|------------------------|----------------|----------------|
| <span data-ttu-id="83d8f-120">CDS 販売注文ヘッダー</span><span class="sxs-lookup"><span data-stu-id="83d8f-120">CDS sales order headers</span></span>| <span data-ttu-id="83d8f-121">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="83d8f-121">SalesOrder</span></span>     | <span data-ttu-id="83d8f-122">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="83d8f-122">SalesOrders</span></span> |
| <span data-ttu-id="83d8f-123">CDS 販売注文明細行</span><span class="sxs-lookup"><span data-stu-id="83d8f-123">CDS sales order lines</span></span>  | <span data-ttu-id="83d8f-124">SalesOrderLine</span><span class="sxs-lookup"><span data-stu-id="83d8f-124">SalesOrderLine</span></span> | <span data-ttu-id="83d8f-125">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="83d8f-125">SalesOrderDetails</span></span>|

## <a name="entity-flow"></a><span data-ttu-id="83d8f-126">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="83d8f-126">Entity flow</span></span>

<span data-ttu-id="83d8f-127">販売注文が Finance and Operations で作成され Sales に同期されます。</span><span class="sxs-lookup"><span data-stu-id="83d8f-127">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="83d8f-128">テンプレートのフィルターは、関連する販売注文のみが同期に含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="83d8f-128">Filters in the template ensure that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="83d8f-129">Sales からの販売注文で、注文と請求の両方の顧客が同期に含まれます。</span><span class="sxs-lookup"><span data-stu-id="83d8f-129">Both ordering and invoicing customer on the sales order that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="83d8f-130">Finance and Operations で、フィールドの [**OrderingCustomerIsExternallyMaintained**] および [**InvoiceCustomerIsExternallyMaintained**] は、データ エンティティの同期を追跡するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="83d8f-130">In Finance and Operations, the fields **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** are used to track the synchronization in the data entities.</span></span>

- <span data-ttu-id="83d8f-131">Finance and Operations で [**販売注文**] を確定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="83d8f-131">The **Sales order** in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="83d8f-132">出荷済や請求済ステータスなどの、確定済販売注文または処理ステータスの大きい販売注文のみが、Sales に同期されます。</span><span class="sxs-lookup"><span data-stu-id="83d8f-132">Only the confirmed sales orders or sales orders with higher processing status, for example, Shipped or Invoiced status, are synchronized to Sales.</span></span>

- <span data-ttu-id="83d8f-133">販売注文を作成または変更した後、Finance and Operations でバッチ ジョブの [**販売合計の計算**] を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="83d8f-133">After creating or modifying a sales order, the batch job **Calculate sales totals** in Finance and Operations must be executed.</span></span> <span data-ttu-id="83d8f-134">売上合計が計算された販売注文のみが CDS と Sales に同期されます。</span><span class="sxs-lookup"><span data-stu-id="83d8f-134">Only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="83d8f-135">[**販売注文ヘッダー**] での税に関連する費用は、現在 Finance and Operations から Sales への同期に含まれていません。</span><span class="sxs-lookup"><span data-stu-id="83d8f-135">Tax related to charges on the **Sales order header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="83d8f-136">これは Sales がヘッダー レベルでの税金情報をサポートしていないためです。</span><span class="sxs-lookup"><span data-stu-id="83d8f-136">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="83d8f-137">明細行レベルでの税に関連する費用が含まれます。</span><span class="sxs-lookup"><span data-stu-id="83d8f-137">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="83d8f-138">売上の見込顧客を現金化するソリューション</span><span class="sxs-lookup"><span data-stu-id="83d8f-138">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="83d8f-139">新しいフィールドが [**注文**] エンティティに追加され、ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="83d8f-139">New fields are added to the **Order** entity and displayed on the page:</span></span>

- <span data-ttu-id="83d8f-140">注文が Finance and Operations から来る場合、[**外部で管理**] - を [**はい**] に設定します。</span><span class="sxs-lookup"><span data-stu-id="83d8f-140">**Is Maintained Externally** - Set to **Yes** when the order is coming from Finance and Operations.</span></span>

- <span data-ttu-id="83d8f-141">[**処理状態**] - Finance and Operations で注文の処理状態を表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="83d8f-141">**Processing status** - Used to show the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="83d8f-142">値は、</span><span class="sxs-lookup"><span data-stu-id="83d8f-142">Values are:</span></span>

    - <span data-ttu-id="83d8f-143">使用可能</span><span class="sxs-lookup"><span data-stu-id="83d8f-143">Active</span></span>
    - <span data-ttu-id="83d8f-144">確認済</span><span class="sxs-lookup"><span data-stu-id="83d8f-144">Confirmed</span></span>
    - <span data-ttu-id="83d8f-145">梱包明細</span><span class="sxs-lookup"><span data-stu-id="83d8f-145">Packing Slip</span></span>
    - <span data-ttu-id="83d8f-146">請求済</span><span class="sxs-lookup"><span data-stu-id="83d8f-146">Invoiced</span></span>
    - <span data-ttu-id="83d8f-147">ピッキング済</span><span class="sxs-lookup"><span data-stu-id="83d8f-147">Picked</span></span>
    - <span data-ttu-id="83d8f-148">一部ピック済</span><span class="sxs-lookup"><span data-stu-id="83d8f-148">Partially Picked</span></span>
    - <span data-ttu-id="83d8f-149">一部ピック済</span><span class="sxs-lookup"><span data-stu-id="83d8f-149">Partially Packed</span></span>
    - <span data-ttu-id="83d8f-150">出荷済</span><span class="sxs-lookup"><span data-stu-id="83d8f-150">Shipped</span></span>
    - <span data-ttu-id="83d8f-151">一部出荷済</span><span class="sxs-lookup"><span data-stu-id="83d8f-151">Partially Shipped</span></span>
    - <span data-ttu-id="83d8f-152">一部請求済</span><span class="sxs-lookup"><span data-stu-id="83d8f-152">Partially Invoiced</span></span>
    - <span data-ttu-id="83d8f-153">キャンセル済</span><span class="sxs-lookup"><span data-stu-id="83d8f-153">Cancelled</span></span>

<span data-ttu-id="83d8f-154">[**外部で管理される製品のみの見積**] 設定は、販売注文が完全に [**外部で管理される製品**] で構成されているかを一貫して追跡するよう、別の販売注文のシナリオ (Sales から Finance and Operation 同期) で使用されます。その場合、製品は Finance and Operations で管理されます。</span><span class="sxs-lookup"><span data-stu-id="83d8f-154">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (from Sales to Finance and Operation sync) to consistently keep track of whether the sales order is made up entirely of **Externally Maintained Products**, in which case products are maintained in Finance and Operations.</span></span> <span data-ttu-id="83d8f-155">これにより、Finance and Operations で不明な製品と販売注文明細行を同期しなくなります。</span><span class="sxs-lookup"><span data-stu-id="83d8f-155">This ensures that you don't try to sync sales order lines with products that are unknown to Finance and Operations.</span></span>
 
<span data-ttu-id="83d8f-156">[**販売注文**] ページで、[**請求書の作成**]、[**注文のキャンセル**]、[**再計算**]、[**製品の取得**] および [**ルックアップ アドレス**] ボタンは外部で管理される注文用に非表示となります。それは Finance and Operations で請求書が作成され Sales に同期されるためです。</span><span class="sxs-lookup"><span data-stu-id="83d8f-156">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products** and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="83d8f-157">販売注文情報は Finance and Operations から同期されるため、注文ページは編集できません。</span><span class="sxs-lookup"><span data-stu-id="83d8f-157">The order page is non-editable because sales order information will be synced from Finance and Operations.</span></span>
 
<span data-ttu-id="83d8f-158">Finance and Operations からの変更が Sales での [**販売注文**] にフローするよう、[**販売注文状態**] は有効になります。</span><span class="sxs-lookup"><span data-stu-id="83d8f-158">The **Sales order status** will remain active to ensure that changes from Finance and Operations can flow to the **Sales order** in Sales.</span></span> <span data-ttu-id="83d8f-159">これは、データ統合プロジェクトで、既定の [**Statecode [状態]**] を [**有効**] に設定することにより制御されます。</span><span class="sxs-lookup"><span data-stu-id="83d8f-159">This is controlled by setting the default **Statecode [Status]** to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="83d8f-160">前提条件とマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="83d8f-160">Preconditions and mapping setup</span></span> 

<span data-ttu-id="83d8f-161">販売注文を同期する前に、次の設定でシステムを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="83d8f-161">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="83d8f-162">Sales での設定</span><span class="sxs-lookup"><span data-stu-id="83d8f-162">Setup in Sales</span></span>

- <span data-ttu-id="83d8f-163">割り当てられるユーザー (Sales [**接続設定**] から) のチームに対するアクセス許可を確保します。</span><span class="sxs-lookup"><span data-stu-id="83d8f-163">Ensure permissions for the team that the user (from your Sales **Connection set**) is assigned to.</span></span> <span data-ttu-id="83d8f-164">デモ データを使用している場合は、通常ユーザーに管理者アクセスがあり、チームにはありません。</span><span class="sxs-lookup"><span data-stu-id="83d8f-164">If you are using demo data, usually the user has admin access, but not the team.</span></span> <span data-ttu-id="83d8f-165">これがないと、データ インテグレーターからプロジェクトを実行するときに主要なチームがないという、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="83d8f-165">Without this you will get an error that Principal team is missing when running the project from Data integrator.</span></span> 

    - <span data-ttu-id="83d8f-166">[**設定**] > [**セキュリティ**] > [**チーム**] で、関連チームを選択し、[**ロール管理**] をクリックして [システム管理者] などの必要なアクセス許可を持つロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="83d8f-166">Under **Settings** > **Security** > **Teams**, select the relevant team, click **Manage Roles** and select a role with the desired permissions e.g. System Administrator.</span></span>

- <span data-ttu-id="83d8f-167">[**設定**] > [**管理**] > [**システム設定**] > [**販売**] で、[**システム プライジング計算システムの使用**] が [**はい**] に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="83d8f-167">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="83d8f-168">[**設定**] > [**管理**] > [**システム設定**] > [**販売**] で、[**割引の計算方法**] が [**明細行品目**] に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="83d8f-168">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="83d8f-169">Finance and Operations での設定</span><span class="sxs-lookup"><span data-stu-id="83d8f-169">Setup in Finance and Operations</span></span>

<span data-ttu-id="83d8f-170">[**販売およびマーケティング**] > [**定期処理のタスク**] > [**販売合計の計算**] を設定してバッチ ジョブとして実行し、[**販売注文合計の計算**] を [**はい**] に設定します。</span><span class="sxs-lookup"><span data-stu-id="83d8f-170">Set **Sales and marketing** > **Periodic tasks** > **Calculate sales totals** to run as a batch job, with **Calculate totals for sales orders** set to **Yes**.</span></span> <span data-ttu-id="83d8f-171">売上合計が計算された販売注文のみが CDS と Sales に同期されるため、これは重要です。</span><span class="sxs-lookup"><span data-stu-id="83d8f-171">This is important because only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span> <span data-ttu-id="83d8f-172">バッチ ジョブの頻度は、販売注文の同期の頻度に対応している必要があります。</span><span class="sxs-lookup"><span data-stu-id="83d8f-172">The frequence of the batch job should be alligned with the frequence of the sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="83d8f-173">データ統合プロジェクトでの設定</span><span class="sxs-lookup"><span data-stu-id="83d8f-173">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="83d8f-174">SalesHeader タスク</span><span class="sxs-lookup"><span data-stu-id="83d8f-174">SalesHeader task</span></span>

- <span data-ttu-id="83d8f-175">[**ソースでの CDS 組織 ID**] > [**CDS**] に対するマッピングを更新します。</span><span class="sxs-lookup"><span data-stu-id="83d8f-175">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span>

    - <span data-ttu-id="83d8f-176">[**Account_Organization_OrganizationId**] の既定のテンプレート値は ORG001 です。</span><span class="sxs-lookup"><span data-stu-id="83d8f-176">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="83d8f-177">[**InvoiceAccount_Organization_OrganizationId**] の既定のテンプレート値は ORG001 です。</span><span class="sxs-lookup"><span data-stu-id="83d8f-177">Default template value for **InvoiceAccount_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="83d8f-178">[**Organization_OrganizationId**] の既定のテンプレート値は ORG001 です。</span><span class="sxs-lookup"><span data-stu-id="83d8f-178">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="83d8f-179">[**ソース**] > [**BillingAddress_Country への InvoiceCountryRegionId 用 CDS**] および [**DeliveryAddress_Country への DeliveryCountryRegionId**] 用に必要なマッピングが存在することを確認します。。</span><span class="sxs-lookup"><span data-stu-id="83d8f-179">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId to BillingAddress_Country** and for **DeliveryCountryRegionId to DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="83d8f-180">マップされている国の数のテンプレート値は [**ValueMap**] です。</span><span class="sxs-lookup"><span data-stu-id="83d8f-180">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="83d8f-181">Sales で注文を作成するために [**価格リスト**] が必要です。</span><span class="sxs-lookup"><span data-stu-id="83d8f-181">**Price list** is required to create orders in Sales.</span></span> <span data-ttu-id="83d8f-182">[**pricelevelid.name [価格リスト名]**] の [**CDS**] > [**出力先**] で、Sales で通貨ごとに使用される [**価格リスト**] への [**ValueMap**] を更新します。</span><span class="sxs-lookup"><span data-stu-id="83d8f-182">Update the **ValueMap** in **CDS** > **Destination** for **pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="83d8f-183">1 つの通貨に対する既定の [**価格リスト**] を使用するか、または複数の通貨で [**価格リスト**] がある場合 [**ValueMap**] を使用するかのいずれかができます。</span><span class="sxs-lookup"><span data-stu-id="83d8f-183">You can either used the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>
    
    - <span data-ttu-id="83d8f-184">[**pricelevelid.name [価格リスト名]**] の既定のテンプレートの値は CRM サービス USA (サンプル) です。</span><span class="sxs-lookup"><span data-stu-id="83d8f-184">Default template value for **pricelevelid.name [Price List Name]** is CRM Service USA (sample).</span></span> 

#### <a name="salesline-task"></a><span data-ttu-id="83d8f-185">SalesLine タスク</span><span class="sxs-lookup"><span data-stu-id="83d8f-185">SalesLine task</span></span>

- <span data-ttu-id="83d8f-186">[**ソースでの CDS 組織 ID**] > [**CDS**] に対するマッピングを更新します。</span><span class="sxs-lookup"><span data-stu-id="83d8f-186">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 
    
    - <span data-ttu-id="83d8f-187">[**SalesOrder_Organization_OrganizationId**] の規定のテンプレート値は ORG001 です。</span><span class="sxs-lookup"><span data-stu-id="83d8f-187">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="83d8f-188">[**Product_Organization_OrganizationId**] の既定のテンプレート値は ORG001 です。</span><span class="sxs-lookup"><span data-stu-id="83d8f-188">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="83d8f-189">[**DeliveryCountryRegionId**] の [**ソース**] > [**CDS**] で、[**DeliveryAddress_Country**] に必要なマッピングが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="83d8f-189">Ensure that the needed mapping exists in **Source** > **CDS** for **DeliveryCountryRegionId** to **DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="83d8f-190">マップされている国の数のテンプレート値は [**ValueMap**] です。</span><span class="sxs-lookup"><span data-stu-id="83d8f-190">Template value is **ValueMap** with a number of countries mapped.</span></span>
    
- <span data-ttu-id="83d8f-191">[**ソース**] > [**CDマッピング**] に存在する Finance and Operations で、[**SalesUnitSymbol**] 用の必要な [**ValueMap**] を確認します。</span><span class="sxs-lookup"><span data-stu-id="83d8f-191">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span>

    - <span data-ttu-id="83d8f-192">[**Quantity_UOMにSalesUnitSymbol**] に対して [**ValueMap**] を持つテンプレート値が定義されます。</span><span class="sxs-lookup"><span data-stu-id="83d8f-192">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="83d8f-193">データ インテグレーターでテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="83d8f-193">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="83d8f-194">[**支払条件**]、[**運賃条件**]、[**配送条件**]、[**送付方法**]、および [**配送モード**] フィールドは、既定のマッピングの一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="83d8f-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="83d8f-195">これらのフィールドをマップするには、エンティティ間で同期される組織内のデータに固有の値マッピングを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="83d8f-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="83d8f-196">次の図は、データ インテグレーターのテンプレート マッピングの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="83d8f-196">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="orderheader"></a><span data-ttu-id="83d8f-197">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="83d8f-197">OrderHeader</span></span>

![データ インテグレーターでテンプレートのマッピング](./media/sales-order-template-mapping-data-integrator-1.png)

![データ インテグレーターでテンプレートのマッピング](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a><span data-ttu-id="83d8f-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="83d8f-200">OrderLine</span></span>

![データ インテグレーターでテンプレートのマッピング](./media/sales-order-template-mapping-data-integrator-3.png)

![データ インテグレーターでテンプレートのマッピング](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="83d8f-203">関連トピック</span><span class="sxs-lookup"><span data-stu-id="83d8f-203">Related topics</span></span>

[<span data-ttu-id="83d8f-204">Finance and Operations の製品を売上の製品に同期する</span><span class="sxs-lookup"><span data-stu-id="83d8f-204">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="83d8f-205">Finance and Operations の顧客への Sales の勘定の同期</span><span class="sxs-lookup"><span data-stu-id="83d8f-205">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="83d8f-206">Finance and Operations の連絡先または顧客への Sales の連絡先の同期</span><span class="sxs-lookup"><span data-stu-id="83d8f-206">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="83d8f-207">販売見積ヘッダーおよび明細行の Sales から Finance and Operations への同期</span><span class="sxs-lookup"><span data-stu-id="83d8f-207">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="83d8f-208">売上請求書ヘッダーおよび明細行の Finance and Operations から Sales への同期</span><span class="sxs-lookup"><span data-stu-id="83d8f-208">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


