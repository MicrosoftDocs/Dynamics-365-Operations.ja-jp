---
title: "販売見積のヘッダーおよび明細行を Sales から Finance and Operations に同期する"
description: "このトピックでは、Microsoft Dynamics 365 for Sales から Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition に対して、販売見積ヘッダーと明細行を同期するために使用されるテンプレートと基本的なタスクについて説明します。"
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
ms.openlocfilehash: 172a3da1b6d90a25ea9ebd14265e70e4a6f9bd70
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a><span data-ttu-id="6adf3-103">販売見積のヘッダーおよび明細行を Sales から Finance and Operations に同期する</span><span class="sxs-lookup"><span data-stu-id="6adf3-103">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="6adf3-104">見込顧客を現金化するソリューションを使用する前に、[Dynamics 365 データ統合](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration) をよく理解しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="6adf3-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="6adf3-105">このトピックでは、Microsoft Dynamics 365 for Sales (Sales) から Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Finance and Operations) に対して、販売見積ヘッダーと明細行を同期するために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6adf3-105">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="6adf3-106">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="6adf3-106">Template and tasks</span></span>

<span data-ttu-id="6adf3-107">Sales から Finance and Operations への販売見積ヘッダーと明細行の同期には、以下のテンプレートと基本的なタスクが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6adf3-107">The following templates and underlying tasks are used to synchronize sales quotation headers and lines from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="6adf3-108">[**テンプレートの名前:**] 販売見積もり (Sales から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="6adf3-108">**Name of the template:** Sales Quotes (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="6adf3-109">**プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="6adf3-109">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="6adf3-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="6adf3-110">QuoteHeader</span></span>
    - <span data-ttu-id="6adf3-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="6adf3-111">QuoteLine</span></span>

<span data-ttu-id="6adf3-112">販売見積ヘッダーと明細行を同期させるには、次の同期タスクが必要です。</span><span class="sxs-lookup"><span data-stu-id="6adf3-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="6adf3-113">製品</span><span class="sxs-lookup"><span data-stu-id="6adf3-113">Products</span></span>
- <span data-ttu-id="6adf3-114">アカウント (使用されている場合)</span><span class="sxs-lookup"><span data-stu-id="6adf3-114">Accounts (if used)</span></span>
- <span data-ttu-id="6adf3-115">連絡先 (使用されている場合)</span><span class="sxs-lookup"><span data-stu-id="6adf3-115">Contacts (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="6adf3-116">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="6adf3-116">Entity set</span></span>

| <span data-ttu-id="6adf3-117">売上</span><span class="sxs-lookup"><span data-stu-id="6adf3-117">Sales</span></span>        | <span data-ttu-id="6adf3-118">CDS</span><span class="sxs-lookup"><span data-stu-id="6adf3-118">CDS</span></span>           | <span data-ttu-id="6adf3-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="6adf3-119">Finance and Operations</span></span>    |
|--------------|---------------|---------------------------|
| <span data-ttu-id="6adf3-120">引用</span><span class="sxs-lookup"><span data-stu-id="6adf3-120">Quotes</span></span>       | <span data-ttu-id="6adf3-121">見積書</span><span class="sxs-lookup"><span data-stu-id="6adf3-121">Quotation</span></span>     | <span data-ttu-id="6adf3-122">販売見積ヘッダー</span><span class="sxs-lookup"><span data-stu-id="6adf3-122">Sales quotation headers</span></span>   |
| <span data-ttu-id="6adf3-123">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="6adf3-123">QuoteDetails</span></span> | <span data-ttu-id="6adf3-124">QuotationLine</span><span class="sxs-lookup"><span data-stu-id="6adf3-124">QuotationLine</span></span> | <span data-ttu-id="6adf3-125">CDS 販売見積明細行</span><span class="sxs-lookup"><span data-stu-id="6adf3-125">CDS sales quotation lines</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="6adf3-126">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="6adf3-126">Entity flow</span></span>

<span data-ttu-id="6adf3-127">販売見積が Sales で作成され Finance and Operations に同期されます。</span><span class="sxs-lookup"><span data-stu-id="6adf3-127">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="6adf3-128">Sales からの販売見積は、次の条件が満たされた場合にのみに同期されます。</span><span class="sxs-lookup"><span data-stu-id="6adf3-128">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="6adf3-129">販売見積明細行のすべての製品は、外部から管理されます。</span><span class="sxs-lookup"><span data-stu-id="6adf3-129">All products on the sales quotation lines are externally maintained.</span></span>
- <span data-ttu-id="6adf3-130">販売見積は、有効または有効化されています。</span><span class="sxs-lookup"><span data-stu-id="6adf3-130">The sales quotation is active or activated.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="6adf3-131">売上の見込顧客を現金化するソリューション</span><span class="sxs-lookup"><span data-stu-id="6adf3-131">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="6adf3-132">[**外部で管理される製品のみあり**] フィールドが見積エンティティに追加され、販売見積が外部管理製品から完全に構成されているかどうかが一貫して追跡されます。</span><span class="sxs-lookup"><span data-stu-id="6adf3-132">The **Has Externally Maintained Products Only** field has been added to the Quote entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="6adf3-133">販売見積に外部で管理された製品のみがある場合、製品は Finance and Operations で管理されます。</span><span class="sxs-lookup"><span data-stu-id="6adf3-133">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="6adf3-134">この動作は、Finance and Operations で不明な製品と販売見積明細行を同期させないことを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="6adf3-134">This behavior helps guarantee that you don't try to synchronize sales quotation lines with products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="6adf3-135">見積書のすべての製品と明細行は、見積書ヘッダーからの [**外部で管理される製品のみあり**] 情報で更新されます。</span><span class="sxs-lookup"><span data-stu-id="6adf3-135">All products and lines on the quotation are updated with the **Has Externally Maintained Products Only** information from the quotation header.</span></span> <span data-ttu-id="6adf3-136">この情報は、見積明細行エンティティの [**外部で管理される製品のみの見積**] フィールドに記載されています。</span><span class="sxs-lookup"><span data-stu-id="6adf3-136">This information can be found in the **Quote Has Externally Maintained Products Only** field on the Quote line entity.</span></span>

<span data-ttu-id="6adf3-137">[**割引**]、[**請求**]、および [**税**] フィールドは、Finance and Operations の複雑な設定によって制御されます。</span><span class="sxs-lookup"><span data-stu-id="6adf3-137">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="6adf3-138">この設定では現在、統合マッピングはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6adf3-138">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="6adf3-139">現在の設計では、[**価格**]、[**割引**]、[**請求金額**]、および [**税**] の各フィールドは、Finance and Operations によって習得され、処理されます。</span><span class="sxs-lookup"><span data-stu-id="6adf3-139">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are mastered and handled by Finance and Operations.</span></span>

<span data-ttu-id="6adf3-140">Sales では、値が Finance and Operations に同期されていないため、このソリューションでは次のフィールドを読み取り専用にします。</span><span class="sxs-lookup"><span data-stu-id="6adf3-140">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="6adf3-141">[**販売見積ヘッダーの読み取り専用フィールド:**] 割引率、割引、貨物量</span><span class="sxs-lookup"><span data-stu-id="6adf3-141">**Read-only fields on the sales quotation header:** Discount %, Discount, Freight Amount</span></span>
- <span data-ttu-id="6adf3-142">[**販売見積明細行の読み取り専用のフィールド:**] 税</span><span class="sxs-lookup"><span data-stu-id="6adf3-142">**Read-only fields on sales quotation lines:** Tax</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="6adf3-143">前提条件とマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="6adf3-143">Preconditions and mapping setup</span></span>

- <span data-ttu-id="6adf3-144">販売見積を同期する前に、Sales で [**設定**] &gt; [**管理**] &gt; [**システム設定**] &gt; [**販売**] に移動し、[**割引の計算方法**] フィールドが [**単位あたり**] に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6adf3-144">Before you synchronize sales quotations, in Sales, go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the **Discount calculation method** field is set to **Per unit**.</span></span> <span data-ttu-id="6adf3-145">この設定を使用すると、Sales からの明細行品目割引が Finance and Operations の設定と一致することが保証されます。</span><span class="sxs-lookup"><span data-stu-id="6adf3-145">This setting helps guarantee that the line item discount from Sales matches the setting in Finance and Operations.</span></span> <span data-ttu-id="6adf3-146">それ以外の場合、Finance and Operations では、売上高の 1 ラインあたりの割引であっても、割引を単価単位で読み取るため、割引は Finance and Operations では正しく行われません</span><span class="sxs-lookup"><span data-stu-id="6adf3-146">Otherwise, the discount won't be correct in Finance and Operations, because Finance and Operations will read the discount as a per-unit discount even if it was a per-line discount in Sales.</span></span>
- <span data-ttu-id="6adf3-147">Finance and Operations で、[**売掛金**] &gt; [**設定**] &gt; [**売掛金勘定パラメーター"**] に移動します。</span><span class="sxs-lookup"><span data-stu-id="6adf3-147">In Finance and Operations, go to **Accounts receivable** &gt; **Setup** &gt; **Account receivable parameters**.</span></span> <span data-ttu-id="6adf3-148">[**番号順序**] タブで、販売見積の番号順序を選択し、[**詳細を表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6adf3-148">On the **Number sequence** tab, select the number sequence for sales quotations, and then click **View details**.</span></span> <span data-ttu-id="6adf3-149">その後 [**全般設定**] で、[**手動**] フィールドを [**はい**] に設定します。</span><span class="sxs-lookup"><span data-stu-id="6adf3-149">Then, under **General Setup**, set the **Manual** field to **Yes**.</span></span>
- <span data-ttu-id="6adf3-150">Finance and Operations で、[**売掛金**] &gt; [**設定**] &gt; [**売掛金勘定パラメーター**] に移動します。</span><span class="sxs-lookup"><span data-stu-id="6adf3-150">In Finance and Operations, go to **Accounts receivable** &gt; **Setup** &gt; **Accounts receivable parameters**.</span></span> <span data-ttu-id="6adf3-151">その後、[**出荷**] タブで、[**配送日管理**] フィールドを [**なし**] に設定します。</span><span class="sxs-lookup"><span data-stu-id="6adf3-151">Then, on the **Shipments** tab, set the **Delivery date control** field to **None**.</span></span> <span data-ttu-id="6adf3-152">この設定は、販売見積の同期が失敗するのを防ぐのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="6adf3-152">This setting helps prevent synchronization from failing for sales quotations.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="6adf3-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="6adf3-153">QuoteHeader</span></span>

- <span data-ttu-id="6adf3-154">[**要求された納期日**] フィールドは Finance and Operations で必要です。このフィールドが空白の場合、同期は失敗します。</span><span class="sxs-lookup"><span data-stu-id="6adf3-154">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="6adf3-155">この問題を防ぐために、このフィールドが空白の場合、既定の日付が [**ソース &gt; CDS**] から取得されます。</span><span class="sxs-lookup"><span data-stu-id="6adf3-155">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="6adf3-156">日付は優先値に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6adf3-156">The date should be updated to a preferred value.</span></span> <span data-ttu-id="6adf3-157">現在、今日の日付を表す [**今日**] などの値を入力することはできません。</span><span class="sxs-lookup"><span data-stu-id="6adf3-157">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="6adf3-158">固有の期日を入力してください。</span><span class="sxs-lookup"><span data-stu-id="6adf3-158">You must enter a specific date.</span></span> <span data-ttu-id="6adf3-159">[**配送指定日**] の既定のテンプレート値は [**1/1/2020**] です。</span><span class="sxs-lookup"><span data-stu-id="6adf3-159">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="6adf3-160">[**住所/国の地域コード**] フィールドが Finance and Operations では必要です。</span><span class="sxs-lookup"><span data-stu-id="6adf3-160">The **Address Country region code** field is required in Finance and Operations.</span></span> <span data-ttu-id="6adf3-161">同期エラーを防ぐために、Sales でフィールドが空白のままである場合に使用されるデフォルト値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6adf3-161">To help prevent synchronization errors, you can specify a default value that is used if the field is left blank in Sales.</span></span> <span data-ttu-id="6adf3-162">この既定値は、ローカル アドレスの場合は [**国地域**] フィールドに値を手動で入力する必要がないため便利です。</span><span class="sxs-lookup"><span data-stu-id="6adf3-162">This default value is also useful, because you don't have to manually enter a value in the **Country region** field for local addresses.</span></span> <span data-ttu-id="6adf3-163">[**DeliveryAddressCountryRegionISOCode**] には既定のテンプレート値はありません。</span><span class="sxs-lookup"><span data-stu-id="6adf3-163">There is no default template value for **DeliveryAddressCountryRegionISOCode**.</span></span>
- <span data-ttu-id="6adf3-164">[**ソース &gt; CDS**] の [**CDS 組織 ID**] のマッピングを更新して、組織エンティティの [**CDS 組織**] に一致させます。</span><span class="sxs-lookup"><span data-stu-id="6adf3-164">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="6adf3-165">[**Organization_OrganizationId**] の既定のテンプレート値は [**ORG001**] です。</span><span class="sxs-lookup"><span data-stu-id="6adf3-165">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="6adf3-166">[**Account_Organization_OrganizationId**] の既定のテンプレート値は [**ORG001**] です。</span><span class="sxs-lookup"><span data-stu-id="6adf3-166">The default template value for **Account_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="6adf3-167">[**InvoiceAccount_OrganizationId**] の既定のテンプレート値は [**ORG001**] です。</span><span class="sxs-lookup"><span data-stu-id="6adf3-167">The default template value for **InvoiceAccount_OrganizationId** is **ORG001**.</span></span>

### <a name="quoteline"></a><span data-ttu-id="6adf3-168">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="6adf3-168">QuoteLine</span></span>

- <span data-ttu-id="6adf3-169">[**ソース &gt; CDS**] の [**CDS 組織 ID**] のマッピングを更新して、組織エンティティの [**CDS 組織**] に一致させます。</span><span class="sxs-lookup"><span data-stu-id="6adf3-169">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="6adf3-170">[**Organization_OrganizationId**] の既定のテンプレート値は [**ORG001**] です。</span><span class="sxs-lookup"><span data-stu-id="6adf3-170">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="6adf3-171">[**Product_Organization_Organization_OrganizationId**] の既定のテンプレート値は [**ORG001**] です。</span><span class="sxs-lookup"><span data-stu-id="6adf3-171">The default template value for **Product_Organization_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="6adf3-172">[**Quotation_Organization_Organization_OrganizationId**] の既定のテンプレート値は [**ORG001**] です。</span><span class="sxs-lookup"><span data-stu-id="6adf3-172">The default template value for **Quotation_Organization_Organization_OrganizationId** is **ORG001**.</span></span>

- <span data-ttu-id="6adf3-173">[**要求された納期日**] フィールドは Finance and Operations で必要です。このフィールドが空白の場合、同期は失敗します。</span><span class="sxs-lookup"><span data-stu-id="6adf3-173">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="6adf3-174">この問題を防ぐために、このフィールドが空白の場合、既定の日付が [**ソース &gt; CDS**] から取得されます。</span><span class="sxs-lookup"><span data-stu-id="6adf3-174">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="6adf3-175">日付は優先値に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6adf3-175">The date should be updated to a preferred value.</span></span> <span data-ttu-id="6adf3-176">現在、今日の日付を表す [**今日**] などの値を入力することはできません。</span><span class="sxs-lookup"><span data-stu-id="6adf3-176">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="6adf3-177">固有の期日を入力してください。</span><span class="sxs-lookup"><span data-stu-id="6adf3-177">You must enter a specific date.</span></span> <span data-ttu-id="6adf3-178">[**配送指定日**] の既定のテンプレート値は [**1/1/2020**] です。</span><span class="sxs-lookup"><span data-stu-id="6adf3-178">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="6adf3-179">[**CDS &gt; 出力先**] から次のマッピングを追加して、顧客または製品からの既定の情報がない場合、見積書明細行を Finance and Operations にインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="6adf3-179">You can add the following mappings from **CDS &gt; Destination** to help guarantee that quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="6adf3-180">**SiteId** – Finance and Operations で見積書および販売注文を生成するにはサイトが必要です。</span><span class="sxs-lookup"><span data-stu-id="6adf3-180">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="6adf3-181">[**SiteId**] に対する既定のテンプレート値はありません。</span><span class="sxs-lookup"><span data-stu-id="6adf3-181">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="6adf3-182">**WarehouseId** – Finance and Operations で見積書および販売注文を処理するには倉庫が必要です。</span><span class="sxs-lookup"><span data-stu-id="6adf3-182">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="6adf3-183">[**WarehouseId**] に対する既定のテンプレート値はありません。</span><span class="sxs-lookup"><span data-stu-id="6adf3-183">There is no default template value for **WarehouseId**.</span></span>

- <span data-ttu-id="6adf3-184">[**Quantity_UOM**] から [**SALESUNITSYMBOL**] の [**CDS &gt; Destination**] マッピングに、Finance and Operations における販売量測定単位 (UOM) の必要な値マップが存在することを確認してください。</span><span class="sxs-lookup"><span data-stu-id="6adf3-184">Make sure that the required value map for the selling unit of measure (UOM) in Finance and Operations exists in the **CDS &gt; Destination** mapping for **Quantity_UOM** to **SALESUNITSYMBOL**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="6adf3-185">データ インテグレーターでテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="6adf3-185">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="6adf3-186">[**割引**]、[**請求**]、および [**税**] フィールドは、Finance and Operations の複雑な設定によって制御されます。</span><span class="sxs-lookup"><span data-stu-id="6adf3-186">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="6adf3-187">この設定では現在、統合マッピングはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6adf3-187">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="6adf3-188">現在の設計では、[**価格**]、[**割引**]、[**請求金額**]、および [**税**] の各フィールドは、Finance and Operations によって処理されます。</span><span class="sxs-lookup"><span data-stu-id="6adf3-188">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="6adf3-189">[**支払条件**]、[**運賃条件**]、[**配送条件**]、[**送付方法**]、および [**配送モード**] フィールドは、既定のマッピングの一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="6adf3-189">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="6adf3-190">これらのフィールドをマップするには、エンティティ間で同期される組織内のデータに固有の値マッピングを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6adf3-190">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="6adf3-191">次の図は、データ インテグレーターのテンプレート マッピングの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="6adf3-191">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="6adf3-192">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="6adf3-192">QuoteHeader</span></span>

![データ インテグレーターでテンプレートのマッピング](./media/sales-quotation-template-mapping-data-integrator-1.png)

![データ インテグレーターでテンプレートのマッピング](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a><span data-ttu-id="6adf3-195">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="6adf3-195">QuoteLine</span></span>

![データ インテグレーターでテンプレートのマッピング](./media/sales-quotation-template-mapping-data-integrator-3.png)

![データ インテグレーターでテンプレートのマッピング](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a><span data-ttu-id="6adf3-198">関連トピック</span><span class="sxs-lookup"><span data-stu-id="6adf3-198">Related topics</span></span>

[<span data-ttu-id="6adf3-199">Finance and Operations の製品を売上の製品に同期する</span><span class="sxs-lookup"><span data-stu-id="6adf3-199">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="6adf3-200">Finance and Operations で売上勘定を顧客に同期する</span><span class="sxs-lookup"><span data-stu-id="6adf3-200">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="6adf3-201">売上の連絡先を Finance and Operations の連絡先または顧客に同期させる</span><span class="sxs-lookup"><span data-stu-id="6adf3-201">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)



