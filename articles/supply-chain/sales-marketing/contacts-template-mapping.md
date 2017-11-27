---
title: "売上の連絡先を Finance and Operations の連絡先または顧客に同期させる"
description: "このトピックでは、Microsoft Dynamics 365 for Sales から Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition に対して、連絡先 (連絡先) と連絡先 (顧客) を同期するために使用されるテンプレートと基本的なタスクについて説明します。"
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
ms.openlocfilehash: c838fef502f643c764fade9cd79ae770ffc36974
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="35995-103">売上の連絡先を Finance and Operations の連絡先または顧客に同期させる</span><span class="sxs-lookup"><span data-stu-id="35995-103">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="35995-104">見込顧客を現金化するソリューションを使用する前に、[Dynamics 365 データ統合](/common-data-service/entity-reference/dynamics-365-integration) をよく理解しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="35995-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="35995-105">このトピックでは、Microsoft Dynamics 365 for Sales (Sales) から Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Finance and Operations) に対して、連絡先 (連絡先) エンティティと連絡先 (顧客) を同期するために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="35995-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) entities and Contact (Customers) from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="35995-106">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="35995-106">Templates and tasks</span></span>

<span data-ttu-id="35995-107">売上から Finance and Operations へ連絡先 (連絡先) と連絡先 (顧客) を同期するには、以下のテンプレートと基本的なタスクが使用されます。</span><span class="sxs-lookup"><span data-stu-id="35995-107">The following templates and underlying tasks are used to synchronize Contact (Contacts) in Sales to Contact (Customers) in Finance and Operations:</span></span>

- <span data-ttu-id="35995-108">**テンプレートの名前:**</span><span class="sxs-lookup"><span data-stu-id="35995-108">**Names of the templates:**</span></span>

    - <span data-ttu-id="35995-109">連絡先 (Sales から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="35995-109">Contacts (Sales to Fin and Ops)</span></span>
    - <span data-ttu-id="35995-110">連絡先から顧客 (売上から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="35995-110">Contacts to Customer (Sales to Fin and Ops)</span></span>

- <span data-ttu-id="35995-111">**プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="35995-111">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="35995-112">連絡先</span><span class="sxs-lookup"><span data-stu-id="35995-112">Contacts</span></span>
    - <span data-ttu-id="35995-113">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="35995-113">ContactToCustomer</span></span>

<span data-ttu-id="35995-114">連絡先の同期の前に、次の同期タスクが必要です: 勘定 (売上から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="35995-114">The following synchronization task is required before Contact synchronization: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="35995-115">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="35995-115">Entity sets</span></span>

| <span data-ttu-id="35995-116">売上</span><span class="sxs-lookup"><span data-stu-id="35995-116">Sales</span></span>    | <span data-ttu-id="35995-117">CDS</span><span class="sxs-lookup"><span data-stu-id="35995-117">CDS</span></span>     | <span data-ttu-id="35995-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="35995-118">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="35995-119">連絡先</span><span class="sxs-lookup"><span data-stu-id="35995-119">Contacts</span></span> | <span data-ttu-id="35995-120">連絡</span><span class="sxs-lookup"><span data-stu-id="35995-120">Contact</span></span> | <span data-ttu-id="35995-121">CDS 連絡先</span><span class="sxs-lookup"><span data-stu-id="35995-121">CDS Contacts</span></span>           |
| <span data-ttu-id="35995-122">連絡先</span><span class="sxs-lookup"><span data-stu-id="35995-122">Contacts</span></span> | <span data-ttu-id="35995-123">アカウント</span><span class="sxs-lookup"><span data-stu-id="35995-123">Account</span></span> | <span data-ttu-id="35995-124">顧客 V2</span><span class="sxs-lookup"><span data-stu-id="35995-124">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="35995-125">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="35995-125">Entity flow</span></span>

<span data-ttu-id="35995-126">連絡先は、販売で管理され、一般的なデータ サービス (CDS) および Finance and Operations に同期されます。</span><span class="sxs-lookup"><span data-stu-id="35995-126">Contacts are managed in Sales, and are synchronized to Common Data Service (CDS) and Finance and Operations.</span></span>

<span data-ttu-id="35995-127">売上の連絡先は CD および Finance and Operations の連絡先になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="35995-127">A Contact in Sales can become a Contact in CDS and Finance and Operations.</span></span> <span data-ttu-id="35995-128">また、CDS の勘定および Finance and Operations の顧客になることがあります。</span><span class="sxs-lookup"><span data-stu-id="35995-128">Alternatively, it can become an Account in CDS and a Customer in Finance and Operations.</span></span> <span data-ttu-id="35995-129">CDS と Finance and Operations に同期する上で、連絡先を売上でピックアップする必要があるかどうかを判断するには (例: 売上の連絡先 &gt; CDS の連絡先 &gt; Finance and Operations の連絡先)、システムは売上の連絡先の次のプロパティを検索します。</span><span class="sxs-lookup"><span data-stu-id="35995-129">To determine whether a contact should be picked up in Sales for synchronization to CDS and Finance and Operations (for example, Contacts in Sales &gt; Contact in CDS &gt; Contacts in Finance and Operations), the system looks at the following properties on Contact in Sales:</span></span>

- <span data-ttu-id="35995-130">**CDS の勘定と Finance and Operations での顧客への同期:** [**有効な顧客**] が [**はい**] に設定されている連絡先</span><span class="sxs-lookup"><span data-stu-id="35995-130">**Sync to Account in CDS and Customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="35995-131">**CDS の連絡先と Finance and Operations の連絡先との同期:** [**有効な顧客**] が [**いいえ**] に設定され、**会社** (親勘定/連絡先) がアカウント (連絡先ではない) を表す連絡先</span><span class="sxs-lookup"><span data-stu-id="35995-131">**Sync to Contact in CDS and Contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (Parent Account/Contact) points to an Account (not a Contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="35995-132">売上の見込顧客を現金化するソリューション</span><span class="sxs-lookup"><span data-stu-id="35995-132">Prospect to cash solution for Sales</span></span> 

<span data-ttu-id="35995-133">新しい [**有効な顧客**] フィールドが連絡先に追加されました。</span><span class="sxs-lookup"><span data-stu-id="35995-133">A new **Is Active Customer** field has been added to the Contact.</span></span> <span data-ttu-id="35995-134">このフィールドは、営業活動を持つ連絡先と営業活動を持たない連絡先を区別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="35995-134">This field is used to differentiate Contacts that have sales activity and Contacts that don't have sales activity.</span></span> <span data-ttu-id="35995-135">[**有効な顧客**] は、関連する見積書、注文、または請求書を持つ連絡先に対してのみ [**はい**] に設定されます。</span><span class="sxs-lookup"><span data-stu-id="35995-135">**Is Active Customer** is set to **Yes** only for Contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="35995-136">これらの連絡先のみが顧客として Finance and Operations に同期されます。</span><span class="sxs-lookup"><span data-stu-id="35995-136">Only those Contacts are synchronized to Finance and Operations as Customers.</span></span>

<span data-ttu-id="35995-137">新しい [**IsCompanyAnAccount**] フィールドが連絡先に追加されました。</span><span class="sxs-lookup"><span data-stu-id="35995-137">A new **IsCompanyAnAccount** field has been added to the Contact.</span></span> <span data-ttu-id="35995-138">このフィールドは、連絡先が**アカウント** タイプの会社 (親アカウント/連絡先) にリンクされているかどうかを示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="35995-138">This field is used to indicate whether a Contact is linked to a Company (Parent Account/Contact) of the **Account** type.</span></span> <span data-ttu-id="35995-139">この情報は、Finance and Operations の連絡先として同期する必要がある連絡先を識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="35995-139">This information is used to identify Contacts that should be synchronized to Finance and Operations as Contacts.</span></span>

<span data-ttu-id="35995-140">新しい [**連絡先番号**] フィールドが連絡先に追加され、統合をサポートするための自然で固有のキーが保証されます。</span><span class="sxs-lookup"><span data-stu-id="35995-140">A new **Contact Number** field has been added to the Contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="35995-141">新しい連絡先が作成されると、**連絡先番号**値は、番号順序を使用して自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="35995-141">When a new Contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="35995-142">値は **CON** で構成され、続いて番号順序が増加し、6 文字の接尾辞が続きます。</span><span class="sxs-lookup"><span data-stu-id="35995-142">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="35995-143">次に例を示します: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="35995-143">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="35995-144">売上の統合ソリューションが売上に追加されると、アップグレード スクリプトは、先に説明した番号シーケンスを使用して、既存の連絡先の [**連絡先番号**] フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="35995-144">When the integration solution for Sales is added to Sales, an upgrade script sets the **Contact Number** field for existing Contacts by using the number sequence that was discussed earlier.</span></span> <span data-ttu-id="35995-145">また、アップグレード スクリプトでは、営業活動を持っている任意の連絡先の [**有効な顧客**] フィールドが [**はい**] に設定されます。</span><span class="sxs-lookup"><span data-stu-id="35995-145">The upgrade script also sets the **Is Active Customer** field to **Yes** for any Contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="35995-146">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="35995-146">In Finance and Operations</span></span> 

<span data-ttu-id="35995-147">[**IsContactPersonExternallyMaintained**] プロパティを使用し、連絡先をタグ付けします。</span><span class="sxs-lookup"><span data-stu-id="35995-147">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="35995-148">このプロパティは、指定された連絡先が外部で管理されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="35995-148">This property indicates that a given Contact is maintained externally.</span></span> <span data-ttu-id="35995-149">この場合、外部で管理されている連絡先は売上に保持されます。</span><span class="sxs-lookup"><span data-stu-id="35995-149">In this case, externally maintained Contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="35995-150">前提条件とマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="35995-150">Preconditions and mapping setup</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="35995-151">連絡先から連絡先へ</span><span class="sxs-lookup"><span data-stu-id="35995-151">Contact to Contact</span></span>

- <span data-ttu-id="35995-152">**ソース&gt; CDS** マッピングの順に **CDS 組織 ID** を更新します。</span><span class="sxs-lookup"><span data-stu-id="35995-152">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span>

    - <span data-ttu-id="35995-153">**Organization_OrganizationId [Organization ID]** の既定のテンプレート値は [**ORG001**] です。</span><span class="sxs-lookup"><span data-stu-id="35995-153">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
    - <span data-ttu-id="35995-154">**PrimaryAccount_Organization_OrganizationId [Organization ID]** の既定のテンプレート値は [**ORG001**] です。</span><span class="sxs-lookup"><span data-stu-id="35995-154">The default template value for **PrimaryAccount_Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>

- <span data-ttu-id="35995-155">**住所/国の地域コード** は Finance and Operations では必須です。</span><span class="sxs-lookup"><span data-stu-id="35995-155">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="35995-156">同期エラーを回避するために、**CDS &gt; Operations** マッピングで既定値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="35995-156">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Operations** mapping.</span></span> <span data-ttu-id="35995-157">販売でこのフィールドが空白の場合、既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="35995-157">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="35995-158">**PrimaryAddressCountryRegionISOCode** の既定のテンプレート値は **USA** です。</span><span class="sxs-lookup"><span data-stu-id="35995-158">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="35995-159">Finance and Operation に次のフィールドの値が存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="35995-159">Make sure that a value for the following field exists in Finance and Operations.</span></span> <span data-ttu-id="35995-160">この情報が Finance and Operations で必要ではない場合は、**CD&gt; 出力先** マッピングの順にマッピングを削除できます。</span><span class="sxs-lookup"><span data-stu-id="35995-160">If the information isn't required in Finance and Operations, you can remove the mapping from the **CDS &gt; Destination** mapping.</span></span>

    - <span data-ttu-id="35995-161">**Finance and Operations のフィールド名:** 意思決定</span><span class="sxs-lookup"><span data-stu-id="35995-161">**Field name in Finance and Operations:** Decision</span></span>
    - <span data-ttu-id="35995-162">**マッピング:** PrimaryAccountRole = DecisionMakingRole</span><span class="sxs-lookup"><span data-stu-id="35995-162">**Mapping:** PrimaryAccountRole = DecisionMakingRole</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="35995-163">連絡先から顧客へ</span><span class="sxs-lookup"><span data-stu-id="35995-163">Contact to Customer</span></span>

- <span data-ttu-id="35995-164">**ソース&gt; CDS** マッピングの順に **CDS 組織 ID** を更新します。</span><span class="sxs-lookup"><span data-stu-id="35995-164">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="35995-165">**Organization_OrganizationId [Organization ID]** の既定のテンプレート値は [**ORG001**] です。</span><span class="sxs-lookup"><span data-stu-id="35995-165">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
- <span data-ttu-id="35995-166">**住所/国の地域コード** は Finance and Operations では必須です。</span><span class="sxs-lookup"><span data-stu-id="35995-166">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="35995-167">同期エラーを回避するために、**CDS &gt; 出力先** マッピングの順に既定値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="35995-167">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="35995-168">販売でこのフィールドが空白の場合、既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="35995-168">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="35995-169">**PrimaryAddressCountryRegionISOCode** の既定のテンプレート値は **USA** です。</span><span class="sxs-lookup"><span data-stu-id="35995-169">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="35995-170">**CustomerGroup** は Finance and Operations で必須です。</span><span class="sxs-lookup"><span data-stu-id="35995-170">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="35995-171">同期エラーを回避するために、**CDS &gt; 出力先** マッピングの順に既定値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="35995-171">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="35995-172">販売でこのフィールドが空白の場合、既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="35995-172">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="35995-173">**CustomerGroupId** の既定のテンプレート値は **10** です。</span><span class="sxs-lookup"><span data-stu-id="35995-173">The default template value for **CustomerGroupId** is **10**.</span></span>
- <span data-ttu-id="35995-174">次のマッピングを **CD&gt;出力先** から追加することによって、Finance and Operations の手動更新の数を減らすことができます。</span><span class="sxs-lookup"><span data-stu-id="35995-174">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are in Finance and Operations.</span></span> <span data-ttu-id="35995-175">たとえば、**国/地域**または**市町村**のデフォルト値または値マップを使用できます。</span><span class="sxs-lookup"><span data-stu-id="35995-175">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="35995-176">**SiteId** - Finance and Operation の製品に対して既定のサイトを定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="35995-176">**SiteId** - A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="35995-177">Finance and Operations で見積書および販売注文を生成するにはサイトが必要です。</span><span class="sxs-lookup"><span data-stu-id="35995-177">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="35995-178">**SiteId** のテンプレートの値が定義されていません。</span><span class="sxs-lookup"><span data-stu-id="35995-178">A template value for **SiteId** isn't defined.</span></span>
    - <span data-ttu-id="35995-179">**WarehouseId** - Finance and Operation の製品に対して既定の倉庫を定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="35995-179">**WarehouseId** - A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="35995-180">Finance and Operations で見積書および販売注文を生成するには倉庫が必要です。</span><span class="sxs-lookup"><span data-stu-id="35995-180">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="35995-181">**WarehouseId** のテンプレートの値が定義されていません。</span><span class="sxs-lookup"><span data-stu-id="35995-181">A template value for **WarehouseId** isn't defined.</span></span>
    - <span data-ttu-id="35995-182">**LanguageId** – Finance and Operations で見積書および販売注文を生成するには言語が必要です。</span><span class="sxs-lookup"><span data-stu-id="35995-182">**LanguageId** - A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="35995-183">**LanguageId** の既定のテンプレート値は **en-us** です。</span><span class="sxs-lookup"><span data-stu-id="35995-183">The default template value for **LanguageId** is **en-us**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="35995-184">データ インテグレーターでテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="35995-184">Template mapping in data integrator</span></span>

<span data-ttu-id="35995-185">次の図は、データ インテグレーターのテンプレート マッピングの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="35995-185">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="35995-186">連絡先から連絡先へ</span><span class="sxs-lookup"><span data-stu-id="35995-186">Contact to Contact</span></span>

![データ インテグレーターでテンプレートのマッピング](./media/contacts-template-mapping-data-integrator-1.png)

![データ インテグレーターの連絡先のテンプレート マッピング](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a><span data-ttu-id="35995-189">連絡先から顧客へ</span><span class="sxs-lookup"><span data-stu-id="35995-189">Contact to Customer</span></span>

![データ インテグレーターでテンプレートのマッピング](./media/contacts-template-mapping-data-integrator-3.png)

![データ インテグレーターの連絡先のテンプレート マッピング](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="35995-192">関連トピック</span><span class="sxs-lookup"><span data-stu-id="35995-192">Related topics</span></span>

[<span data-ttu-id="35995-193">Finance and Operations の製品を売上の製品に同期する</span><span class="sxs-lookup"><span data-stu-id="35995-193">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="35995-194">Finance and Operations で売上勘定を顧客に同期する</span><span class="sxs-lookup"><span data-stu-id="35995-194">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="35995-195">販売見積ヘッダーおよび明細行の Sales から Finance and Operations への同期</span><span class="sxs-lookup"><span data-stu-id="35995-195">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="35995-196">販売注文ヘッダーおよび明細行の Finance and Operations から Sales への同期</span><span class="sxs-lookup"><span data-stu-id="35995-196">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="35995-197">売上請求書ヘッダーおよび明細行の Finance and Operations から Sales への同期</span><span class="sxs-lookup"><span data-stu-id="35995-197">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)

