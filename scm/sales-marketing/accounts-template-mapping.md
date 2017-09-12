---
title: "Finance and Operations で売上勘定を顧客に同期する"
description: "このトピックでは、Microsoft Dynamics 365 for Sales から Microsoft Dynamics 365 for Finance and Operations, Enterprise edition に勘定を同期させるために使用されるテンプレートと基本的なタスクについて説明します。"
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
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
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: b497f078d9786a5c7630e924da6bb04cad37f5e9
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="3585f-103">Finance and Operations で売上勘定を顧客に同期する</span><span class="sxs-lookup"><span data-stu-id="3585f-103">Synchronize accounts from Sales to customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="3585f-104">見込顧客を現金化するソリューションを使用する前に、[Dynamics 365 データ統合](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration) をよく理解しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="3585f-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="3585f-105">このトピックでは、Microsoft Dynamics 365 for Sales (Sales) から Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Finance and Operations) に勘定を同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="3585f-105">The topic discusses the templates and underlying tasks that are used to synchronize accounts from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="template-and-task"></a><span data-ttu-id="3585f-106">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="3585f-106">Template and task</span></span>

<span data-ttu-id="3585f-107">売上から Finance and Operations への勘定同期には、以下のテンプレートと基本的なタスクが使用されます。</span><span class="sxs-lookup"><span data-stu-id="3585f-107">The following templates and underlying tasks are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="3585f-108">**テンプレートの名前:** 勘定 (売上から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="3585f-108">**Name of the template:** Accounts (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="3585f-109">**プロジェクトのタスクの名前:** - 勘定 - 勘定 - 顧客</span><span class="sxs-lookup"><span data-stu-id="3585f-109">**Name of the task in the project:** Accounts - Account - Customers</span></span>

<span data-ttu-id="3585f-110">勘定/顧客を同期する前に必要なタスクの同期: なし</span><span class="sxs-lookup"><span data-stu-id="3585f-110">Sync tasks required prior to Account / Customer sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="3585f-111">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="3585f-111">Entity set</span></span>

| <span data-ttu-id="3585f-112">売上</span><span class="sxs-lookup"><span data-stu-id="3585f-112">Sales</span></span>    | <span data-ttu-id="3585f-113">CDS</span><span class="sxs-lookup"><span data-stu-id="3585f-113">CDS</span></span>     | <span data-ttu-id="3585f-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3585f-114">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="3585f-115">アカウント</span><span class="sxs-lookup"><span data-stu-id="3585f-115">Accounts</span></span> | <span data-ttu-id="3585f-116">アカウント</span><span class="sxs-lookup"><span data-stu-id="3585f-116">Account</span></span> | <span data-ttu-id="3585f-117">顧客</span><span class="sxs-lookup"><span data-stu-id="3585f-117">Customers</span></span>              |

## <a name="entity-flow"></a><span data-ttu-id="3585f-118">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="3585f-118">Entity flow</span></span>

<span data-ttu-id="3585f-119">勘定は売上で管理され、Finance and Operations に顧客として同期されます。</span><span class="sxs-lookup"><span data-stu-id="3585f-119">Accounts are managed in Sales and synchronized to Finance and Operations as Customers.</span></span> <span data-ttu-id="3585f-120">この顧客の**外部管理**プロパティを**はい**に設定し、売上から生成される顧客を追跡します。</span><span class="sxs-lookup"><span data-stu-id="3585f-120">The **Is Externally Maintained** property on these Customers is set to **Yes** to track Customers that originate from Sales.</span></span> <span data-ttu-id="3585f-121">請求時に、この情報は、売上に同期される請求書のフィルター処理に使用されます。</span><span class="sxs-lookup"><span data-stu-id="3585f-121">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="3585f-122">売上の見込顧客を現金化するソリューション</span><span class="sxs-lookup"><span data-stu-id="3585f-122">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="3585f-123">**勘定番号**フィールドは、**勘定**ページで利用できます。</span><span class="sxs-lookup"><span data-stu-id="3585f-123">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="3585f-124">統合をサポートするための自然で固有のキーとなっています。</span><span class="sxs-lookup"><span data-stu-id="3585f-124">It has been made a natural and unique key to support the integration.</span></span> <span data-ttu-id="3585f-125">顧客関係管理 (CRM) ソリューションのナチュラル キー機能は、すでに **勘定番号** フィールドを使用しているが、勘定ごとに一意の **勘定番号** 値を使用していない顧客に影響する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3585f-125">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="3585f-126">現時点では、統合ソリューションは、このケースをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="3585f-126">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="3585f-127">新しいアカウントが作成され、**勘定番号**値が存在しない場合、番号順序を使用して自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="3585f-127">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="3585f-128">その値は**勘定**で構成され、続いて番号順序が増加し、6 文字の接尾辞が続きます。</span><span class="sxs-lookup"><span data-stu-id="3585f-128">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="3585f-129">次に例を示します: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="3585f-129">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="3585f-130">売上の統合ソリューションが適用されている場合、アップグレード スクリプトにより、売上の既存のアカウントの、**勘定番号**フィールドが設定されます。</span><span class="sxs-lookup"><span data-stu-id="3585f-130">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="3585f-131">**勘定番号**値がない場合は、前述した番号順序を使用します。</span><span class="sxs-lookup"><span data-stu-id="3585f-131">If there are no **Account Number** values, the number sequence that was described earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="3585f-132">前提条件とマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="3585f-132">Preconditions and mapping setup</span></span>

- <span data-ttu-id="3585f-133">**CustomerGroupId** は Finance and Operation で有効な値に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3585f-133">**CustomerGroupId** must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="3585f-134">既定値を指定するか、値マップを使用して値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="3585f-134">You can specify a default value, or you can set the value by using a value map.</span></span> <span data-ttu-id="3585f-135">既定のテンプレートの値は **10** です。</span><span class="sxs-lookup"><span data-stu-id="3585f-135">The default template value is **10**.</span></span>
- <span data-ttu-id="3585f-136">**住所/国の地域コード** フィールドが Finance and Operations では必要です。</span><span class="sxs-lookup"><span data-stu-id="3585f-136">**Address country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="3585f-137">同期エラーを避けるためには、既定値を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="3585f-137">To avoid synchronization errors, you can specify a default value.</span></span> <span data-ttu-id="3585f-138">販売でこのフィールドが空白の場合、既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="3585f-138">That default value is then used if the field is left blank in Sales.</span></span>

    - <span data-ttu-id="3585f-139">[**AddressCountryRegionISOCode**] の既定のテンプレート値は **USA** です。</span><span class="sxs-lookup"><span data-stu-id="3585f-139">The default template value for **AddressCountryRegionISOCode** is **USA**.</span></span>
    - <span data-ttu-id="3585f-140">**DeliveryAddressCountryRegionISOCode** の既定のテンプレート値は **USA** です。</span><span class="sxs-lookup"><span data-stu-id="3585f-140">The default template value for **DeliveryAddressCountryRegionISOCode** is **USA**.</span></span>

- <span data-ttu-id="3585f-141">次のマッピングを **CD&gt;出力先** から追加することによって、Finance and Operations で必要な手動更新の数を減らすことができます。</span><span class="sxs-lookup"><span data-stu-id="3585f-141">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="3585f-142">たとえば、**国/地域**または**市町村**のデフォルト値または値マップを使用できます。</span><span class="sxs-lookup"><span data-stu-id="3585f-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="3585f-143">**SiteId** – Finance and Operations で見積書および販売注文を生成するにはサイトが必要です。</span><span class="sxs-lookup"><span data-stu-id="3585f-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="3585f-144">デフォルトのサイトは、製品から、または注文ヘッダーの顧客から取得できます。</span><span class="sxs-lookup"><span data-stu-id="3585f-144">A default site can be taken either from the product, or from the customer from the order header.</span></span> <span data-ttu-id="3585f-145">**SiteId** の既定のテンプレート値は **1** です。</span><span class="sxs-lookup"><span data-stu-id="3585f-145">The default template value for **SiteId** is **1**.</span></span>
    - <span data-ttu-id="3585f-146">**WarehouseId** – Finance and Operations で見積書および販売注文を処理するには倉庫が必要です。</span><span class="sxs-lookup"><span data-stu-id="3585f-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="3585f-147">デフォルト倉庫は、製品から、または Finance and Operations の受注ヘッダーの顧客から取得できます。</span><span class="sxs-lookup"><span data-stu-id="3585f-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span> <span data-ttu-id="3585f-148">**WarehouseId** の既定のテンプレート値は **13** です。</span><span class="sxs-lookup"><span data-stu-id="3585f-148">The default template value for **WarehouseId** is **13**.</span></span>
    - <span data-ttu-id="3585f-149">**LanguageId** – Finance and Operations で見積書および販売注文を生成するには言語が必要です。</span><span class="sxs-lookup"><span data-stu-id="3585f-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="3585f-150">既定では、顧客からの注文ヘッダの言語が使用されます。</span><span class="sxs-lookup"><span data-stu-id="3585f-150">By default, the language from the order header from the customer is used.</span></span> <span data-ttu-id="3585f-151">**LanguageId** の既定のテンプレート値は **en-us** です。</span><span class="sxs-lookup"><span data-stu-id="3585f-151">The default template value for **LanguageId** is **en-us**.</span></span>

- <span data-ttu-id="3585f-152">**ソース &gt; CD** マッピングの順に移動し、CD の組織 ID (**Organization_OrganizationId**) を更新します。</span><span class="sxs-lookup"><span data-stu-id="3585f-152">Update the CDS organization ID (**Organization_OrganizationId**) in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="3585f-153">既定のテンプレートの値は **ORG001** です。</span><span class="sxs-lookup"><span data-stu-id="3585f-153">The default template value is **ORG001**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="3585f-154">データ インテグレーターでテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="3585f-154">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="3585f-155">[**支払条件**]、[**運賃条件**]、[**配送条件**]、[**送付方法**]、および [**配送モード**] フィールドは、既定のマッピングには含まれていません。</span><span class="sxs-lookup"><span data-stu-id="3585f-155">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="3585f-156">これらのフィールドをマップするには、値マッピングを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3585f-156">To map these fields, you must set up a value mapping.</span></span> <span data-ttu-id="3585f-157">値マッピングは、エンティティ間で同期される組織内のデータ固有です。</span><span class="sxs-lookup"><span data-stu-id="3585f-157">Value mappings are specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="3585f-158">次の図は、データ インテグレーターのテンプレート マッピングの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="3585f-158">The following illustrations show an example of a template mapping in data integrator.</span></span>

![データ インテグレーターでテンプレートのマッピング](./media/accounts-template-mapping-data-integrator-1.png)

![データ インテグレーターの勘定のテンプレート マッピング](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="3585f-161">関連トピック</span><span class="sxs-lookup"><span data-stu-id="3585f-161">Related topics</span></span>

[<span data-ttu-id="3585f-162">Finance and Operations の製品を売上の製品に同期する</span><span class="sxs-lookup"><span data-stu-id="3585f-162">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="3585f-163">売上の連絡先を Finance and Operations の連絡先または顧客に同期させる</span><span class="sxs-lookup"><span data-stu-id="3585f-163">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="3585f-164">販売見積のヘッダーおよび明細行を売上から Finance and Operations に同期する</span><span class="sxs-lookup"><span data-stu-id="3585f-164">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)




