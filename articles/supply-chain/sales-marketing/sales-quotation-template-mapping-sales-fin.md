---
title: 販売見積のヘッダーおよび明細行の Sales から Supply Chain Management への直接同期
description: このトピックでは、Dynamics 365 Sales から Dynamics 365 Supply Chain Management に販売見積ヘッダーおよび明細行を直接同期するために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: bdca4d63fbe04a01cf1bbf2ccd7b095d4718a115
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910308"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a><span data-ttu-id="ab2de-103">販売見積のヘッダーおよび明細行の Sales から Supply Chain Management への直接同期</span><span class="sxs-lookup"><span data-stu-id="ab2de-103">Synchronize sales quotation headers and lines directly from Sales to Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ab2de-104">このトピックでは、Dynamics 365 Sales から Dynamics 365 Supply Chain Management に販売見積ヘッダーおよび明細行を直接同期するために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ab2de-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

> [!NOTE]
> <span data-ttu-id="ab2de-105">見込顧客を現金化するソリューションを使用する前に、[Microsoft Dataverse for Apps へデータを統合](/powerapps/administrator/data-integrator) をよく理解しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab2de-105">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](/powerapps/administrator/data-integrator).</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="ab2de-106">見込み客の現金化へのデータフロー</span><span class="sxs-lookup"><span data-stu-id="ab2de-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="ab2de-107">見込み客の現金化ソリューションは、Supply Chain Management と Sales のインスタンス間でデータを同期するため、データの統合機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="ab2de-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="ab2de-108">データ統合機能で利用可能な見込み顧客を現金化するテンプレートにより、Supply Chain Management と Sales 間での勘定、連絡先、製品および販売見積、販売注文、および売上請求書のデータの流れが可能になります。</span><span class="sxs-lookup"><span data-stu-id="ab2de-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="ab2de-109">次の図は、Supply Chain Management と Sales の間でデータを同期させる方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="ab2de-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="ab2de-110">[![見込み客の現金化へのデータフロー](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="ab2de-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="ab2de-111">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="ab2de-111">Template and tasks</span></span>

<span data-ttu-id="ab2de-112">Sales から Supply Chain Management への販売見積ヘッダーと明細行の直接同期には、以下のテンプレートと基本的なタスクが使用されます。</span><span class="sxs-lookup"><span data-stu-id="ab2de-112">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="ab2de-113">**データ統合における テンプレートの名前:** 販売見積 (Sales から Supply Chain Management)- 直接</span><span class="sxs-lookup"><span data-stu-id="ab2de-113">**Name of the template in Data integration:** Sales Quotes (Sales to Supply Chain Management) - Direct</span></span>
- <span data-ttu-id="ab2de-114">**データ統合プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="ab2de-114">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="ab2de-115">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="ab2de-115">QuoteHeader</span></span>
    - <span data-ttu-id="ab2de-116">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="ab2de-116">QuoteLine</span></span>

<span data-ttu-id="ab2de-117">販売見積ヘッダーと明細行を同期させるには、次の同期タスクが必要です。</span><span class="sxs-lookup"><span data-stu-id="ab2de-117">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="ab2de-118">製品 (Supply Chain Management から Sales) - 直接</span><span class="sxs-lookup"><span data-stu-id="ab2de-118">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="ab2de-119">勘定 (Sales から Supply Chain Management) - ダイレクト (使用する場合)</span><span class="sxs-lookup"><span data-stu-id="ab2de-119">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="ab2de-120">顧客への連絡先 (Sales から Supply Chain Management) - ダイレクト (使用する場合)</span><span class="sxs-lookup"><span data-stu-id="ab2de-120">Contacts to Customers (Sales to Supply Chain Management) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="ab2de-121">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="ab2de-121">Entity set</span></span>

| <span data-ttu-id="ab2de-122">販売注文</span><span class="sxs-lookup"><span data-stu-id="ab2de-122">Sales</span></span>        | <span data-ttu-id="ab2de-123">サプライ チェーン マネジメント</span><span class="sxs-lookup"><span data-stu-id="ab2de-123">Supply Chain Management</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="ab2de-124">引用</span><span class="sxs-lookup"><span data-stu-id="ab2de-124">Quotes</span></span>       | <span data-ttu-id="ab2de-125">Dataverse 販売見積もりのヘッダー</span><span class="sxs-lookup"><span data-stu-id="ab2de-125">Dataverse sales quotation header</span></span> |
| <span data-ttu-id="ab2de-126">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="ab2de-126">QuoteDetails</span></span> | <span data-ttu-id="ab2de-127">Dataverse 販売見積明細行</span><span class="sxs-lookup"><span data-stu-id="ab2de-127">Dataverse sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="ab2de-128">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="ab2de-128">Entity flow</span></span>

<span data-ttu-id="ab2de-129">販売見積が Sales で作成され、Supply Chain Management に同期されます。</span><span class="sxs-lookup"><span data-stu-id="ab2de-129">Sales quotations are created in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="ab2de-130">Sales からの販売見積は、次の条件が満たされた場合にのみに同期されます。</span><span class="sxs-lookup"><span data-stu-id="ab2de-130">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="ab2de-131">販売見積のすべての見積は、外部から管理されます。</span><span class="sxs-lookup"><span data-stu-id="ab2de-131">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="ab2de-132">**有効化見積** をクリックした後、販売見積は有効です。</span><span class="sxs-lookup"><span data-stu-id="ab2de-132">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="ab2de-133">売上の見込顧客を現金化するソリューション</span><span class="sxs-lookup"><span data-stu-id="ab2de-133">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="ab2de-134">**外部で管理された製品のみ** フィールドが **見積** エンティティに追加され、販売見積が完全に外部管理製品から構成されているかどうか一貫して追跡されます。</span><span class="sxs-lookup"><span data-stu-id="ab2de-134">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="ab2de-135">販売見積に外部で管理された製品のみがある場合、製品は Supply Chain Management で管理されます。</span><span class="sxs-lookup"><span data-stu-id="ab2de-135">If a sales quotation has only externally maintained products, the products are maintained in Supply Chain Management.</span></span> <span data-ttu-id="ab2de-136">この動作は、Supply Chain Management で不明な製品を含む販売見積明細行を同期させないことを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="ab2de-136">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Supply Chain Management.</span></span>

<span data-ttu-id="ab2de-137">販売見積書のすべての見積製品は、販売見積書ヘッダーからの **外部で管理される製品のみ** 情報で更新されます。</span><span class="sxs-lookup"><span data-stu-id="ab2de-137">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="ab2de-138">この情報は、**QuoteDetails** エンティティの **外部で管理される製品のみの見積** フィールドに記載されています。</span><span class="sxs-lookup"><span data-stu-id="ab2de-138">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="ab2de-139">割引は、見積製品に追加することができ、Supply Chain Management と同期されます。</span><span class="sxs-lookup"><span data-stu-id="ab2de-139">A discount can be added to the quote product and will be synchronized to Supply Chain Management.</span></span> <span data-ttu-id="ab2de-140">**割引**、**請求**、および **税** フィールドは、ヘッダーで Supply Chain Management の設定によって制御されます。</span><span class="sxs-lookup"><span data-stu-id="ab2de-140">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Supply Chain Management.</span></span> <span data-ttu-id="ab2de-141">今現在、この設定では、統合マッピングはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="ab2de-141">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="ab2de-142">現在の設計では、**価格**、**割引**、**請求金額**、および **税** の各フィールドは、FSupply Chain Management によって維持され、処理されます。</span><span class="sxs-lookup"><span data-stu-id="ab2de-142">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in FSupply Chain Management.</span></span>

<span data-ttu-id="ab2de-143">Sales では、値が Supply Chain Management に同期されていないため、このソリューションでは次のフィールドを読み取り専用にします。</span><span class="sxs-lookup"><span data-stu-id="ab2de-143">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Supply Chain Management:</span></span>

- <span data-ttu-id="ab2de-144">販売見積ヘッダーの読み取り専用フィールド: **割引率**、**割引**、**貨物量**</span><span class="sxs-lookup"><span data-stu-id="ab2de-144">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="ab2de-145">見積製品の読み取り専用フィールド: **税**</span><span class="sxs-lookup"><span data-stu-id="ab2de-145">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="ab2de-146">前提条件とマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="ab2de-146">Preconditions and mapping setup</span></span>

<span data-ttu-id="ab2de-147">販売見積が同期される前に、以下の設定を更新することが重要です。</span><span class="sxs-lookup"><span data-stu-id="ab2de-147">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="ab2de-148">Sales での設定</span><span class="sxs-lookup"><span data-stu-id="ab2de-148">Setup in Sales</span></span>

- <span data-ttu-id="ab2de-149">Sales で設定された接続のユーザーが割り当てられているチームのアクセス許可が設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ab2de-149">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="ab2de-150">デモデータを使用している場合、通常、ユーザーは管理者権限を持っていますが、チームには管理者権限がありません。</span><span class="sxs-lookup"><span data-stu-id="ab2de-150">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="ab2de-151">チームがデータ統合からプロジェクトを実行するときにチームに管理者権限がない場合、主要なチームがないというエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ab2de-151">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="ab2de-152">チームのアクセス許可を設定するには、**設定** &gt; **セキュリティ** &gt; **チーム** の順に進み、該当するチームを選択します。</span><span class="sxs-lookup"><span data-stu-id="ab2de-152">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="ab2de-153">**ロールの管理** を選択して、**システム管理者** などの必要なアクセス許可を持つロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="ab2de-153">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="ab2de-154">**設定** &gt; **管理** &gt; **システム設定** &gt; **Sales** へと順に進み、次の設定が使用されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ab2de-154">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="ab2de-155">**システム プライジング計算システムの使用** オプションが、**はい** に設定されている。</span><span class="sxs-lookup"><span data-stu-id="ab2de-155">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="ab2de-156">**割引の計算方法** フィールドが、**明細行品目** に設定されている。</span><span class="sxs-lookup"><span data-stu-id="ab2de-156">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="ab2de-157">データ統合プロジェクトでの設定</span><span class="sxs-lookup"><span data-stu-id="ab2de-157">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="ab2de-158">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="ab2de-158">QuoteHeader</span></span>

- <span data-ttu-id="ab2de-159">必要なマッピングが **Shipto\_country** から **DeliveryAddressCountryRegionISOCode** に存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="ab2de-159">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="ab2de-160">値マップでは、値が空白の場合に使用される既定値を定義できます。</span><span class="sxs-lookup"><span data-stu-id="ab2de-160">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="ab2de-161">左側を空白のままにして、右側を希望する国または地域に設定します。</span><span class="sxs-lookup"><span data-stu-id="ab2de-161">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="ab2de-162">これにより、国または地域国内の注文を入力する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ab2de-162">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="ab2de-163">テンプレートの値は、複数の国または地域がマップされている値マップで、空白値は **米国** の値と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="ab2de-163">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="ab2de-164">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="ab2de-164">QuoteLine</span></span>

- <span data-ttu-id="ab2de-165">Supply Chain Management の **SalesUnitSymbol** に必要な値マップが存在することを確認して下さい。</span><span class="sxs-lookup"><span data-stu-id="ab2de-165">Make sure that the required value map exists for **SalesUnitSymbol** in Supply Chain Management.</span></span>
- <span data-ttu-id="ab2de-166">Sales に必要な単位が定義されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ab2de-166">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="ab2de-167">値マップを持つテンプレート値が **oumid.name** から **SalesUnitSymbol** まで定義されています。</span><span class="sxs-lookup"><span data-stu-id="ab2de-167">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="ab2de-168">オプション： 次のマッピングを追加して、顧客または製品からの既定の情報がない場合、販売見積明細行を Supply Chain Management にインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="ab2de-168">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Supply Chain Management if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="ab2de-169">**SiteId** – Supply Chain Management で見積書および販売注文を生成するにはサイトが必要です。</span><span class="sxs-lookup"><span data-stu-id="ab2de-169">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="ab2de-170">**SiteId** に対する既定のテンプレート値はありません。</span><span class="sxs-lookup"><span data-stu-id="ab2de-170">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="ab2de-171">**WarehouseId** – Supply Chain Management で見積書および販売注文を処理するには倉庫が必要です。</span><span class="sxs-lookup"><span data-stu-id="ab2de-171">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="ab2de-172">**WarehouseId** に対する既定のテンプレート値はありません。</span><span class="sxs-lookup"><span data-stu-id="ab2de-172">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="ab2de-173">データ インテグレーターでテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="ab2de-173">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="ab2de-174">**割引**、**請求**、および **税** フィールドは、Supply Chain Management 内の複雑な設定によって制御されています。</span><span class="sxs-lookup"><span data-stu-id="ab2de-174">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Supply Chain Management.</span></span> <span data-ttu-id="ab2de-175">今現在、この設定では、統合マッピングはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="ab2de-175">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="ab2de-176">現在の設計では、**価格**、**割引**、**請求金額**、および **税** の各フィールドは、Supply Chain Management によって処理されます。</span><span class="sxs-lookup"><span data-stu-id="ab2de-176">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Supply Chain Management.</span></span>
> - <span data-ttu-id="ab2de-177">**支払条件**、**運賃条件**、**配送条件**、**送付方法**、および **配送モード** フィールドは、既定のマッピングの一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="ab2de-177">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="ab2de-178">これらのフィールドをマップするには、エンティティ間で同期される組織内のデータに固有の値マッピングを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab2de-178">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="ab2de-179">次の図は、データ インテグレーターのテンプレート マッピングの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="ab2de-179">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="ab2de-180">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="ab2de-180">QuoteHeader</span></span>

![データ インテグレーターでテンプレートのマッピング](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="ab2de-182">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="ab2de-182">QuoteLine</span></span>

![データ インテグレーターでテンプレートのマッピング](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="ab2de-184">関連トピック</span><span class="sxs-lookup"><span data-stu-id="ab2de-184">Related topics</span></span>

[<span data-ttu-id="ab2de-185">見込顧客を現金化</span><span class="sxs-lookup"><span data-stu-id="ab2de-185">Prospect to cash</span></span>](prospect-to-cash.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]