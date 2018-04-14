---
title: "Sales から Finance and Operations への販売見積ヘッダーおよび明細行の直接同期"
description: "このトピックでは、Microsoft Dynamics 365 for Sales から Microsoft Dynamics 365 for Finance and Operations に対して、販売見積ヘッダーと明細行を直接同期するために使用されるテンプレートと基本的なタスクについて説明します。"
author: ChristianRytt
manager: AnnBe
ms.date: 11/14/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d61e85a80cda06570e17276b9aa35255540626d0
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a><span data-ttu-id="03daf-103">Sales から Finance and Operations への販売見積ヘッダーおよび明細行の直接同期</span><span class="sxs-lookup"><span data-stu-id="03daf-103">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="03daf-104">このトピックでは、Microsoft Dynamics 365 for Sales から Microsoft Dynamics 365 for Finance and Operations に対して、販売見積ヘッダーと明細行を直接同期するために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="03daf-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="03daf-105">見込顧客を現金化するソリューションを使用する前に、[Dynamics 365 データ統合](/common-data-service/entity-reference/dynamics-365-integration) をよく理解しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="03daf-105">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="03daf-106">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="03daf-106">Template and tasks</span></span>

<span data-ttu-id="03daf-107">Sales から Finance and Operations への販売見積ヘッダーと明細行の直接同期には、以下のテンプレートと基本的なタスクが使用されます。</span><span class="sxs-lookup"><span data-stu-id="03daf-107">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="03daf-108">**データ統合における テンプレートの名前** 販売見積 (Finance and Operations から Sales)- 直接</span><span class="sxs-lookup"><span data-stu-id="03daf-108">**Name of the template in Data integration:** Sales Quotes (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="03daf-109">**データ統合プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="03daf-109">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="03daf-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="03daf-110">QuoteHeader</span></span>
    - <span data-ttu-id="03daf-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="03daf-111">QuoteLine</span></span>

<span data-ttu-id="03daf-112">販売見積ヘッダーと明細行を同期させるには、次の同期タスクが必要です。</span><span class="sxs-lookup"><span data-stu-id="03daf-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="03daf-113">製品 (Finance and Operations から Sales) - 直接</span><span class="sxs-lookup"><span data-stu-id="03daf-113">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="03daf-114">勘定 (Sales から Finance and Operations) - 直接(使用されている場合)</span><span class="sxs-lookup"><span data-stu-id="03daf-114">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="03daf-115">顧客への連絡先 (Sales から Finance and Operations) - ダイレクト (使用されている場合)</span><span class="sxs-lookup"><span data-stu-id="03daf-115">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="03daf-116">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="03daf-116">Entity set</span></span>

| <span data-ttu-id="03daf-117">売上</span><span class="sxs-lookup"><span data-stu-id="03daf-117">Sales</span></span>        | <span data-ttu-id="03daf-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="03daf-118">Finance and Operations</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="03daf-119">引用</span><span class="sxs-lookup"><span data-stu-id="03daf-119">Quotes</span></span>       | <span data-ttu-id="03daf-120">CDS 販売見積ヘッダー</span><span class="sxs-lookup"><span data-stu-id="03daf-120">CDS sales quotation header</span></span> |
| <span data-ttu-id="03daf-121">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="03daf-121">QuoteDetails</span></span> | <span data-ttu-id="03daf-122">CDS 販売見積明細行</span><span class="sxs-lookup"><span data-stu-id="03daf-122">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="03daf-123">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="03daf-123">Entity flow</span></span>

<span data-ttu-id="03daf-124">販売見積が Sales で作成され Finance and Operations に同期されます。</span><span class="sxs-lookup"><span data-stu-id="03daf-124">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="03daf-125">Sales からの販売見積は、次の条件が満たされた場合にのみに同期されます。</span><span class="sxs-lookup"><span data-stu-id="03daf-125">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="03daf-126">販売見積のすべての見積は、外部から管理されます。</span><span class="sxs-lookup"><span data-stu-id="03daf-126">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="03daf-127">**有効化見積**をクリックした後、販売見積は有効です。</span><span class="sxs-lookup"><span data-stu-id="03daf-127">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="03daf-128">売上の見込顧客を現金化するソリューション</span><span class="sxs-lookup"><span data-stu-id="03daf-128">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="03daf-129">[外部で管理された製品のみ] フィールドが**見積**エンティティに追加され、販売見積が完全に外部管理製品から構成されているかどうか一貫して追跡されます。</span><span class="sxs-lookup"><span data-stu-id="03daf-129">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="03daf-130">販売見積に外部で管理された製品のみがある場合、製品は Finance and Operations で管理されます。</span><span class="sxs-lookup"><span data-stu-id="03daf-130">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="03daf-131">この動作は、Finance and Operations で不明な製品を含む販売見積明細行を同期させないことを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="03daf-131">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="03daf-132">販売見積書のすべての見積製品は、販売見積書ヘッダーからの [外部で管理される製品のみ] 情報で更新されます。</span><span class="sxs-lookup"><span data-stu-id="03daf-132">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="03daf-133">この情報は、**QuoteDetails**エンティティの [外部で管理される製品のみの見積] フィールドに記載されています。</span><span class="sxs-lookup"><span data-stu-id="03daf-133">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="03daf-134">割引は、見積製品に追加することができ、Finance and Operations と同期されます。</span><span class="sxs-lookup"><span data-stu-id="03daf-134">A discount can be added to the quote product and will be synchronized to Finance and Operations.</span></span> <span data-ttu-id="03daf-135">[割引]、[請求]、および [税] フィールドは、ヘッダーで Finance and Operations の設定によって制御されます。</span><span class="sxs-lookup"><span data-stu-id="03daf-135">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Finance and Operations.</span></span> <span data-ttu-id="03daf-136">今現在、この設定では、統合マッピングはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="03daf-136">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="03daf-137">現在の設計では、[価格]、[割引]、[請求金額]、および [税] の各フィールドは、Finance and Operations によって維持され、処理されます。</span><span class="sxs-lookup"><span data-stu-id="03daf-137">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Finance and Operations.</span></span>

<span data-ttu-id="03daf-138">Sales では、値が Finance and Operations に同期されていないため、このソリューションでは次のフィールドを読み取り専用にします。</span><span class="sxs-lookup"><span data-stu-id="03daf-138">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="03daf-139">販売見積ヘッダーの読み取り専用フィールド: **割引率**、**割引**、**貨物量**</span><span class="sxs-lookup"><span data-stu-id="03daf-139">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="03daf-140">見積製品の読み取り専用フィールド: **税**</span><span class="sxs-lookup"><span data-stu-id="03daf-140">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="03daf-141">前提条件とマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="03daf-141">Preconditions and mapping setup</span></span>

<span data-ttu-id="03daf-142">販売見積が同期される前に、以下の設定を更新することが重要です。</span><span class="sxs-lookup"><span data-stu-id="03daf-142">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="03daf-143">Sales での設定</span><span class="sxs-lookup"><span data-stu-id="03daf-143">Setup in Sales</span></span>

- <span data-ttu-id="03daf-144">Sales で設定された接続のユーザーが割り当てられているチームのアクセス許可が設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="03daf-144">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="03daf-145">デモデータを使用している場合、通常、ユーザーは管理者権限を持っていますが、チームには管理者権限がありません。</span><span class="sxs-lookup"><span data-stu-id="03daf-145">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="03daf-146">チームがデータ統合からプロジェクトを実行するときにチームに管理者権限がない場合、主要なチームがないというエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="03daf-146">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="03daf-147">チームのアクセス許可を設定するには、[**設定**] &gt; [**セキュリティ**] &gt; [**チーム**] の順に進み、該当するチームを選択します。</span><span class="sxs-lookup"><span data-stu-id="03daf-147">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="03daf-148">[**ロールの管理**] を選択して、[**システム管理者**] などの必要なアクセス許可を持つロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="03daf-148">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="03daf-149">[**設定**] &gt; [**管理**] &gt; [**システム設定**] &gt; [**Sales**] へと順に進み、次の設定が使用されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="03daf-149">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="03daf-150">[**システム プライジング計算システムの使用**] オプションが、[**はい**] に設定されている。</span><span class="sxs-lookup"><span data-stu-id="03daf-150">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="03daf-151">[**割引の計算方法**] フィールドが、[**明細行品目**] に設定されている。</span><span class="sxs-lookup"><span data-stu-id="03daf-151">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="03daf-152">データ統合プロジェクトでの設定</span><span class="sxs-lookup"><span data-stu-id="03daf-152">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="03daf-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="03daf-153">QuoteHeader</span></span>

- <span data-ttu-id="03daf-154">必要なマッピングが [**Shipto\_country**] から [**DeliveryAddressCountryRegionISOCode**] に存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="03daf-154">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="03daf-155">値マップでは、値が空白の場合に使用される既定値を定義できます。</span><span class="sxs-lookup"><span data-stu-id="03daf-155">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="03daf-156">左側を空白のままにして、右側を希望する国または地域に設定します。</span><span class="sxs-lookup"><span data-stu-id="03daf-156">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="03daf-157">これにより、国または地域国内の注文を入力する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="03daf-157">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="03daf-158">テンプレートの値は、複数の国または地域がマップされている値マップで、空白値は [**米国**] の値と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="03daf-158">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="03daf-159">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="03daf-159">QuoteLine</span></span>

- <span data-ttu-id="03daf-160">Finance and Operations の**SalesUnitSymbol**に必要な値マップが存在することを確認して下さい。</span><span class="sxs-lookup"><span data-stu-id="03daf-160">Make sure that the required value map exists for **SalesUnitSymbol** in Finance and Operations.</span></span>
- <span data-ttu-id="03daf-161">Sales に必要な単位が定義されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="03daf-161">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="03daf-162">値マップを持つテンプレート値が**oumid.name**から**SalesUnitSymbol**まで定義されています。</span><span class="sxs-lookup"><span data-stu-id="03daf-162">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="03daf-163">オプション： 次のマッピングを追加して、顧客または製品からの既定の情報がない場合、販売見積明細行を Finance and Operations にインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="03daf-163">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="03daf-164">**SiteId** – Finance and Operations で見積書および販売注文を生成するにはサイトが必要です。</span><span class="sxs-lookup"><span data-stu-id="03daf-164">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="03daf-165">[**SiteId**] に対する既定のテンプレート値はありません。</span><span class="sxs-lookup"><span data-stu-id="03daf-165">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="03daf-166">**WarehouseId** – Finance and Operations で見積書および販売注文を処理するには倉庫が必要です。</span><span class="sxs-lookup"><span data-stu-id="03daf-166">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="03daf-167">[**WarehouseId**] に対する既定のテンプレート値はありません。</span><span class="sxs-lookup"><span data-stu-id="03daf-167">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="03daf-168">データ インテグレーターでテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="03daf-168">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="03daf-169">[**割引**]、[**請求**]、および [**税**] フィールドは、Finance and Operations の複雑な設定によって制御されます。</span><span class="sxs-lookup"><span data-stu-id="03daf-169">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="03daf-170">今現在、この設定では、統合マッピングはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="03daf-170">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="03daf-171">現在の設計では、[**価格**]、[**割引**]、[**請求金額**]、および [**税**] の各フィールドは、Finance and Operations によって処理されます。</span><span class="sxs-lookup"><span data-stu-id="03daf-171">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="03daf-172">[**支払条件**]、[**運賃条件**]、[**配送条件**]、[**送付方法**]、および [**配送モード**] フィールドは、既定のマッピングの一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="03daf-172">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="03daf-173">これらのフィールドをマップするには、エンティティ間で同期される組織内のデータに固有の値マッピングを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03daf-173">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="03daf-174">次の図は、データ インテグレーターのテンプレート マッピングの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="03daf-174">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="03daf-175">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="03daf-175">QuoteHeader</span></span>

![データ インテグレーターでテンプレートのマッピング](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="03daf-177">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="03daf-177">QuoteLine</span></span>

![データ インテグレーターでテンプレートのマッピング](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="03daf-179">関連トピック</span><span class="sxs-lookup"><span data-stu-id="03daf-179">Related topics</span></span>

[<span data-ttu-id="03daf-180">見込顧客を現金化</span><span class="sxs-lookup"><span data-stu-id="03daf-180">Prospect to cash</span></span>](prospect-to-cash.md)


