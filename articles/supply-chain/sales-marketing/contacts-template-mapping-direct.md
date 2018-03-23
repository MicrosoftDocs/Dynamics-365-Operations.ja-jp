---
title: "Sales から Finance and Operations の連絡先または顧客への連絡先の直接同期"
description: "このトピックでは、Microsoft Dynamics 365 for Sales から Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition に対して、連絡先 (連絡先) と連絡先 (顧客) エンティティを同期するために使用されるテンプレートと基本的なタスクについて説明します。"
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.sourcegitcommit: 0d409b3b7f19ca31d9c720bca191f1ddba81caa3
ms.openlocfilehash: 6269b73dfca46d455784046199463d3f86e653ae
ms.contentlocale: ja-jp
ms.lasthandoff: 03/13/2018

---

# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="29c8b-103">Sales から Finance and Operations の連絡先または顧客への連絡先の直接同期</span><span class="sxs-lookup"><span data-stu-id="29c8b-103">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="29c8b-104">見込顧客を現金化するソリューションを使用する前に、[Dynamics 365 データ統合](/common-data-service/entity-reference/dynamics-365-integration) をよく理解しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="29c8b-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="29c8b-105">このトピックでは、Microsoft Dynamics 365 for Sales から Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition に対して、連絡先 (連絡先) と連絡先 (顧客) エンティティを直接同期するために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="29c8b-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) and Contact (Customers) entities directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="29c8b-106">見込み客の現金化へのデータフロー</span><span class="sxs-lookup"><span data-stu-id="29c8b-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="29c8b-107">見込み客の現金化ソリューションは、Finance and Operations と Sales のインスタンス間でデータを同期するため、データの統合機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="29c8b-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="29c8b-108">データ統合機能で利用可能な見込み顧客を現金化するテンプレートは、Finance and Operations と Sales 間での勘定、連絡先、製品および販売見積、販売注文、および売上請求書データの流れを可能にします。</span><span class="sxs-lookup"><span data-stu-id="29c8b-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="29c8b-109">次の図は、Finance and Operations と Sales の間でデータを同期させる方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="29c8b-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="29c8b-110">[![見込み客の現金化へのデータフロー](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="29c8b-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="29c8b-111">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="29c8b-111">Templates and tasks</span></span>

<span data-ttu-id="29c8b-112">利用可能なテンプレートにアクセスするには、[PowerApps 管理者センター](https://preview.admin.powerapps.com/dataintegration) を開きます。</span><span class="sxs-lookup"><span data-stu-id="29c8b-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="29c8b-113">**プロジェクト**を選択した後、右上隅にある **新しいプロジェクト** を選択してパブリック テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="29c8b-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="29c8b-114">Sales から Finance and Operations へ連絡先 (連絡先) エンティティと連絡先 (顧客) エンティティを同期するには、以下のテンプレートと基本的なタスクが使用されます。</span><span class="sxs-lookup"><span data-stu-id="29c8b-114">The following templates and underlying tasks are used to synchronize Contact (Contacts) entities in Sales to Contact (Customers) entities in Finance and Operations:</span></span>

- <span data-ttu-id="29c8b-115">**データ統合でのテンプレートの名前:**</span><span class="sxs-lookup"><span data-stu-id="29c8b-115">**Names of the templates in Data integration:**</span></span>

    - <span data-ttu-id="29c8b-116">連絡先 (Sales から Finance and Operations) - 直接</span><span class="sxs-lookup"><span data-stu-id="29c8b-116">Contacts (Sales to Fin and Ops) - Direct</span></span>
    - <span data-ttu-id="29c8b-117">連絡先から顧客 (Sales から Finance and Operations) - 直接</span><span class="sxs-lookup"><span data-stu-id="29c8b-117">Contacts to Customer (Sales to Fin and Ops) - Direct</span></span>

- <span data-ttu-id="29c8b-118">**データ統合プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="29c8b-118">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="29c8b-119">連絡先</span><span class="sxs-lookup"><span data-stu-id="29c8b-119">Contacts</span></span>
    - <span data-ttu-id="29c8b-120">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="29c8b-120">ContactToCustomer</span></span>

<span data-ttu-id="29c8b-121">連絡先の同期には、まず次の同期タスクが必要です。 勘定 (Sales から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="29c8b-121">The following synchronization task is required before contact synchronization can occur: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="29c8b-122">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="29c8b-122">Entity sets</span></span>

| <span data-ttu-id="29c8b-123">売上</span><span class="sxs-lookup"><span data-stu-id="29c8b-123">Sales</span></span>    | <span data-ttu-id="29c8b-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="29c8b-124">Finance and Operations</span></span> |
|----------|------------------------|
| <span data-ttu-id="29c8b-125">連絡先</span><span class="sxs-lookup"><span data-stu-id="29c8b-125">Contacts</span></span> | <span data-ttu-id="29c8b-126">CDS 連絡先</span><span class="sxs-lookup"><span data-stu-id="29c8b-126">CDS Contacts</span></span>           |
| <span data-ttu-id="29c8b-127">連絡先</span><span class="sxs-lookup"><span data-stu-id="29c8b-127">Contacts</span></span> | <span data-ttu-id="29c8b-128">顧客 V2</span><span class="sxs-lookup"><span data-stu-id="29c8b-128">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="29c8b-129">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="29c8b-129">Entity flow</span></span>

<span data-ttu-id="29c8b-130">連絡先は Sales で管理され、Finance and Operations に同期されます。</span><span class="sxs-lookup"><span data-stu-id="29c8b-130">Contacts are managed in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="29c8b-131">Sales の連絡先は Finance and Operations の連絡先または顧客になります。</span><span class="sxs-lookup"><span data-stu-id="29c8b-131">A contact in Sales can become either a contact or a customer in Finance and Operations.</span></span> <span data-ttu-id="29c8b-132">Sales の連絡先を Finance and Operations の連絡先または顧客として同期する必要があるかどうかを判断するために、システムは Sales の連絡先の次のプロパティを調べます。</span><span class="sxs-lookup"><span data-stu-id="29c8b-132">To determine whether a contact in Sales should be synchronized to Finance and Operations as a contact or a customer, the system looks at the following properties on the contact in Sales:</span></span>

- <span data-ttu-id="29c8b-133">**Finance and Operations の顧客への同期:** [有効な顧客] が [はい] に設定されている連絡先</span><span class="sxs-lookup"><span data-stu-id="29c8b-133">**Synchronization to a customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="29c8b-134">**Finance and Operations の連絡先との同期:** [有効な顧客] が [いいえ] に設定され、**会社** (親勘定/連絡先) がアカウント (連絡先ではない) を表す連絡先</span><span class="sxs-lookup"><span data-stu-id="29c8b-134">**Synchronization to a contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (parent account/contact) points to an account (not a contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="29c8b-135">売上の見込顧客を現金化するソリューション</span><span class="sxs-lookup"><span data-stu-id="29c8b-135">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="29c8b-136">新しい [有効な顧客] フィールドが連絡先に追加されました。</span><span class="sxs-lookup"><span data-stu-id="29c8b-136">A new **Is Active Customer** field has been added to the contact.</span></span> <span data-ttu-id="29c8b-137">このフィールドは、営業活動を持つ連絡先と営業活動を持たない連絡先を区別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="29c8b-137">This field is used to differentiate contacts that have sales activity and contacts that don't have sales activity.</span></span> <span data-ttu-id="29c8b-138">[有効な顧客] は、関連する見積書、注文、または請求書を持つ連絡先に対してのみ [はい] に設定されます。</span><span class="sxs-lookup"><span data-stu-id="29c8b-138">**Is Active Customer** is set to **Yes** only for contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="29c8b-139">これらの連絡先のみが顧客として Finance and Operations に同期されます。</span><span class="sxs-lookup"><span data-stu-id="29c8b-139">Only those contacts are synchronized to Finance and Operations as customers.</span></span>

<span data-ttu-id="29c8b-140">新しい [IsCompanyAnAccount] フィールドが連絡先に追加されました。</span><span class="sxs-lookup"><span data-stu-id="29c8b-140">A new **IsCompanyAnAccount** field has been added to the contact.</span></span> <span data-ttu-id="29c8b-141">このフィールドは、連絡先が**アカウント**タイプの会社 (親勘定/連絡先) にリンクされているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="29c8b-141">This field indicates whether a contact is linked to a company (parent account/contact) of the **Account** type.</span></span> <span data-ttu-id="29c8b-142">この情報は、Finance and Operations の連絡先として同期する必要がある連絡先を識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="29c8b-142">This information is used to identify contacts that should be synchronized to Finance and Operations as contacts.</span></span>

<span data-ttu-id="29c8b-143">新しい [連絡先番号] フィールドが連絡先に追加され、統合をサポートするための固有のナチュラル キーが保証されます。</span><span class="sxs-lookup"><span data-stu-id="29c8b-143">A new **Contact Number** field has been added to the contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="29c8b-144">新しい連絡先が作成されると、**連絡先番号**値は、番号順序を使用して自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="29c8b-144">When a new contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="29c8b-145">値は **CON** で構成され、続いて番号順序が増加し、6 文字の接尾辞が続きます。</span><span class="sxs-lookup"><span data-stu-id="29c8b-145">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="29c8b-146">次に例を示します: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="29c8b-146">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="29c8b-147">Sales の統合ソリューションが適用されている場合、アップグレード スクリプトは、先に述べた番号順序を使用して、既存の連絡先の [連絡先番号] フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="29c8b-147">When the integration solution for Sales is applied, an upgrade script sets the **Contact Number** field for existing contacts by using the number sequence that was mentioned earlier.</span></span> <span data-ttu-id="29c8b-148">また、アップグレード スクリプトでは、営業活動を持っている任意の連絡先の [有効な顧客] フィールドが [はい] に設定されます。</span><span class="sxs-lookup"><span data-stu-id="29c8b-148">The upgrade script also sets the **Is Active Customer** field to **Yes** for any contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="29c8b-149">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="29c8b-149">In Finance and Operations</span></span>

<span data-ttu-id="29c8b-150">[IsContactPersonExternallyMaintained] プロパティを使用し、連絡先をタグ付けします。</span><span class="sxs-lookup"><span data-stu-id="29c8b-150">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="29c8b-151">このプロパティは、指定された連絡先が外部で管理されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="29c8b-151">This property indicates that a given contact is maintained externally.</span></span> <span data-ttu-id="29c8b-152">この場合、外部で管理されている連絡先は Sales に保持されます。</span><span class="sxs-lookup"><span data-stu-id="29c8b-152">In this case, externally maintained contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="29c8b-153">前提条件とマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="29c8b-153">Preconditions and mapping setup</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="29c8b-154">連絡先から顧客へ</span><span class="sxs-lookup"><span data-stu-id="29c8b-154">Contact to customer</span></span>

- <span data-ttu-id="29c8b-155">**CustomerGroup** は Finance and Operations で必須です。</span><span class="sxs-lookup"><span data-stu-id="29c8b-155">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="29c8b-156">同期エラーを防ぐために、マッピングで既定値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="29c8b-156">To help prevent synchronization errors, you can specify a default value in the mapping.</span></span> <span data-ttu-id="29c8b-157">販売でこのフィールドが空白の場合、既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="29c8b-157">That default value is then used if the field is left blank in Sales.</span></span>

    <span data-ttu-id="29c8b-158">既定のテンプレートの値は **10** です。</span><span class="sxs-lookup"><span data-stu-id="29c8b-158">The default template value is **10**.</span></span>

- <span data-ttu-id="29c8b-159">次のマッピングを追加することによって、Finance and Operations で必要な手動更新の数を減らすことができます。</span><span class="sxs-lookup"><span data-stu-id="29c8b-159">By adding the following mappings, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="29c8b-160">たとえば、**国/地域**または**市町村**のデフォルト値または値マップを使用できます。</span><span class="sxs-lookup"><span data-stu-id="29c8b-160">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="29c8b-161">**SiteId** – Finance and Operations の製品に対して既定のサイトを定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="29c8b-161">**SiteId** – A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="29c8b-162">Finance and Operations で見積書および販売注文を生成するにはサイトが必要です。</span><span class="sxs-lookup"><span data-stu-id="29c8b-162">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span>

        <span data-ttu-id="29c8b-163">**SiteId** のテンプレートの値が定義されていません。</span><span class="sxs-lookup"><span data-stu-id="29c8b-163">A template value for **SiteId** isn't defined.</span></span>

    - <span data-ttu-id="29c8b-164">**WarehouseId** – Finance and Operations の製品に対して既定の倉庫を定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="29c8b-164">**WarehouseId** – A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="29c8b-165">Finance and Operations で見積書および販売注文を生成するには倉庫が必要です。</span><span class="sxs-lookup"><span data-stu-id="29c8b-165">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span>

        <span data-ttu-id="29c8b-166">**WarehouseId** のテンプレートの値が定義されていません。</span><span class="sxs-lookup"><span data-stu-id="29c8b-166">A template value for **WarehouseId** isn't defined.</span></span>

    - <span data-ttu-id="29c8b-167">**LanguageId** – Finance and Operations で見積書および販売注文を生成するには言語が必要です。</span><span class="sxs-lookup"><span data-stu-id="29c8b-167">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span>
    
        <span data-ttu-id="29c8b-168">既定のテンプレートの値は **アメリカ英語** です。</span><span class="sxs-lookup"><span data-stu-id="29c8b-168">The default template value for is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="29c8b-169">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="29c8b-169">Template mapping in Data integration</span></span>

<span data-ttu-id="29c8b-170">次の図は、データ統合のテンプレート マッピングの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="29c8b-170">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="29c8b-171">マッピングは、Sales から Finance and Operations にどのフィールド情報を同期するかを表示します。</span><span class="sxs-lookup"><span data-stu-id="29c8b-171">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="29c8b-172">連絡先から連絡先へ</span><span class="sxs-lookup"><span data-stu-id="29c8b-172">Contact to contact</span></span>

![データ インテグレーターのテンプレートのマッピング](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a><span data-ttu-id="29c8b-174">連絡先から顧客へ</span><span class="sxs-lookup"><span data-stu-id="29c8b-174">Contact to customer</span></span>

![データ インテグレーターのテンプレートのマッピング](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a><span data-ttu-id="29c8b-176">関連トピック</span><span class="sxs-lookup"><span data-stu-id="29c8b-176">Related topics</span></span>

[<span data-ttu-id="29c8b-177">見込顧客を現金化</span><span class="sxs-lookup"><span data-stu-id="29c8b-177">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="29c8b-178">Sales から Finance and Operations の顧客への勘定の直接同期</span><span class="sxs-lookup"><span data-stu-id="29c8b-178">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="29c8b-179">Sales 製品への Finance and Operations 製品の直接同期</span><span class="sxs-lookup"><span data-stu-id="29c8b-179">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="29c8b-180">販売注文ヘッダーおよび明細行の Finance and Operations から Sales への直接同期</span><span class="sxs-lookup"><span data-stu-id="29c8b-180">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="29c8b-181">売上請求書ヘッダーおよび直接明細行の Finance and Operations から Sales への直接同期</span><span class="sxs-lookup"><span data-stu-id="29c8b-181">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)



