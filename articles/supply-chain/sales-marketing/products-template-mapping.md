---
title: "Finance and Operations の製品を売上の製品に同期"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations, Enterprise edition の製品を Microsoft Dynamics 365 for Sales の製品に同期するときに使用されるテンプレートと基本的なタスクについて説明します。"
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
ms.openlocfilehash: 405a6cf9f3e6cc52925ff7d9f10836196343c36b
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="2adf0-103">Finance and Operations の製品を売上の製品に同期</span><span class="sxs-lookup"><span data-stu-id="2adf0-103">Synchronize products from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="2adf0-104">見込顧客を現金化するソリューションを使用する前に、[Dynamics 365 データ統合](/common-data-service/entity-reference/dynamics-365-integration) をよく理解しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="2adf0-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="2adf0-105">このトピックでは、Microsoft Dynamics 365 for Finance and Operations, Enterprise edition の製品を Microsoft Dynamics 365 for Sales の製品に同期するときに使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2adf0-105">This topic discusses the templates and underlying tasks that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="template-and-task"></a><span data-ttu-id="2adf0-106">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="2adf0-106">Template and task</span></span>

<span data-ttu-id="2adf0-107">次のトピックでは、Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (Finance and Operations) から Microsoft Dynamics 365 for Sales (Sales) に製品を同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2adf0-107">The following templates and underlying tasks are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) to Microsoft Dynamics 365 for Sales (Sales).</span></span>

-   <span data-ttu-id="2adf0-108">テンプレートの名前: 製品 (Finance and Operations から売上)</span><span class="sxs-lookup"><span data-stu-id="2adf0-108">Name of template: Products (Fin and Ops to Sales)</span></span>

-   <span data-ttu-id="2adf0-109">プロジェクトのタスク名: 製品</span><span class="sxs-lookup"><span data-stu-id="2adf0-109">Name of task in project: Products</span></span>

<span data-ttu-id="2adf0-110">製品を同期する前に必要なタスクの同期: なし</span><span class="sxs-lookup"><span data-stu-id="2adf0-110">Sync tasks required prior to Product sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="2adf0-111">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="2adf0-111">Entity set</span></span>

| <span data-ttu-id="2adf0-112">**Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="2adf0-112">**Finance and Operations**</span></span> | <span data-ttu-id="2adf0-113">**CDS**</span><span class="sxs-lookup"><span data-stu-id="2adf0-113">**CDS**</span></span> | <span data-ttu-id="2adf0-114">**販売**</span><span class="sxs-lookup"><span data-stu-id="2adf0-114">**Sales**</span></span>  |
|----------------------------|---------|------------|
| <span data-ttu-id="2adf0-115">販売可能なリリース済製品</span><span class="sxs-lookup"><span data-stu-id="2adf0-115">Sellable released products</span></span> | <span data-ttu-id="2adf0-116">品目</span><span class="sxs-lookup"><span data-stu-id="2adf0-116">Product</span></span> | <span data-ttu-id="2adf0-117">製品</span><span class="sxs-lookup"><span data-stu-id="2adf0-117">Products</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="2adf0-118">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="2adf0-118">Entity flow</span></span>

<span data-ttu-id="2adf0-119">製品は Finance and Operations で管理され、売上に同期されます。</span><span class="sxs-lookup"><span data-stu-id="2adf0-119">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="2adf0-120">Finance and Operations のデータ エンティティ、**販売可能な製品**のみを輸出します。つまり、製品には、販売注文で使用する必要のある情報があります。</span><span class="sxs-lookup"><span data-stu-id="2adf0-120">The data entity **Sellable released products** in Finance and Operations only exports products that are sellable, which means that products have the information required to be used on a sales order.</span></span> <span data-ttu-id="2adf0-121">[**リリースされた製品**] ページで [**検証**] 機能を使用して製品を検証する場合も、同じルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="2adf0-121">The same rules apply when a product is validated with the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="2adf0-122">[**製品番号**] がキーとして使用されます。これは、製品バリアントが [**製品バリアント**] ごとの個別の [**Product IDs**] で CDS と売上に同期されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="2adf0-122">The **Product number** is used as key, meaning that product variants are synchronized to CDS and Sales with individual **Product IDs** per **Product variant**.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="2adf0-123">売上の見込顧客を現金化するソリューション</span><span class="sxs-lookup"><span data-stu-id="2adf0-123">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="2adf0-124">売上では、製品の新しいフィールド、[**外部管理**] が追加され、特定の製品が外部で維持されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="2adf0-124">In Sales, a new field on the products **Is Externally Maintained** is added to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="2adf0-125">値は、デフォルトでは、売上へのインポート時に [**はい**] に設定されます。</span><span class="sxs-lookup"><span data-stu-id="2adf0-125">The value is set to **Yes** by default during import to Sales.</span></span>

-   <span data-ttu-id="2adf0-126">**外部管理が = はい**: 製品が Finance and Operations に由来し、売上では編集できません。</span><span class="sxs-lookup"><span data-stu-id="2adf0-126">**Is Externally Maintained = Yes**: Product originates from Finance and Operations and will not be editable in Sales.</span></span>

-   <span data-ttu-id="2adf0-127">**外部で管理 = いいえ**: 製品は売上に直接入力します。</span><span class="sxs-lookup"><span data-stu-id="2adf0-127">**Is Externally Maintained = No**: Product is entered directly in Sales.</span></span>

-   <span data-ttu-id="2adf0-128">**外部で管理を = 空白**: 見込顧客を現金化するソリューションを有効にする前に、製品が販売に存在します。</span><span class="sxs-lookup"><span data-stu-id="2adf0-128">**Is Externally Maintained = Blank**: Product exists in Sales prior to enabling the Prospect to cash solution.</span></span>

<span data-ttu-id="2adf0-129">**外部管理**情報を使用して、[**外部で管理された製品**] で [**見積**] と [**販売注文**] のみが Finance and Operations に確実に同期するようにします。</span><span class="sxs-lookup"><span data-stu-id="2adf0-129">The **Is Externally Maintained** information is used to ensure that only **Quotes** and **Sales orders** with **Externally maintained products** will sync to Finance and Operations.</span></span>

<span data-ttu-id="2adf0-130">**外部管理の製品**が、同じ通貨で最初に有効な**価格リスト**に自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="2adf0-130">**Externally maintained products** are automatically added to the first valid **Price list** with the same currency.</span></span> <span data-ttu-id="2adf0-131">このリストでは、**名前**がアルファベット順で構成されています。</span><span class="sxs-lookup"><span data-stu-id="2adf0-131">Note that the list is organized alphabetically by **Name**.</span></span> <span data-ttu-id="2adf0-132">Finance and Operations の製品販売価格は**価格リスト**の価格として使用されています。</span><span class="sxs-lookup"><span data-stu-id="2adf0-132">The product sales price from Finance and Operations is used as price on the **Price list**.</span></span> <span data-ttu-id="2adf0-133">これは、Finance and Operations の**製品の販売通貨**ごとに、売上の**価格リスト**を必要とすることを意味します。</span><span class="sxs-lookup"><span data-stu-id="2adf0-133">This means that it is required to have a **Price list** in Sales for each **Product sales currency** in Finance and Operations.</span></span> <span data-ttu-id="2adf0-134">リリースされた販売可能商品の通貨は、製品が輸出される法人の会計通貨に設定されます。</span><span class="sxs-lookup"><span data-stu-id="2adf0-134">Currency on the released sellable products is set to the accounting currency in the legal entity, from which the product is exported.</span></span>

> [!NOTE]
> <span data-ttu-id="2adf0-135">製品の同期は、一致する通貨を含む**価格リスト**なしでは成功しません。</span><span class="sxs-lookup"><span data-stu-id="2adf0-135">Product sync will not succeed without a **Price list** with the matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="2adf0-136">前提条件とマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="2adf0-136">Preconditions and mapping setup</span></span>

-   <span data-ttu-id="2adf0-137">一番最初の同期を実行する前に、Finance and Operation の既存製品に対して [**特徴的製品テーブル**] を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2adf0-137">Before you run the very first sync, you must populate the **Distinct product table** for existing products in Finance and Operations.</span></span> <span data-ttu-id="2adf0-138">このジョブが完了するまで、既存の製品は同期されません。</span><span class="sxs-lookup"><span data-stu-id="2adf0-138">Existing products will not be synchronized until this job is completed.</span></span>

    -   <span data-ttu-id="2adf0-139">Finance and Operations の場合は、[検索] を使用し、[**特徴的製品テーブルの設定**] を検索します。</span><span class="sxs-lookup"><span data-stu-id="2adf0-139">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>

    -   <span data-ttu-id="2adf0-140">[**特徴的製品テーブルの設定**] をクリックし、ジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="2adf0-140">Click the **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="2adf0-141">このジョブは、1 回のみ実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2adf0-141">This job only needs to be run once.</span></span>

-   <span data-ttu-id="2adf0-142">**Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure** の順に検索できる Finance and Operations で **Unit of measure** (UOM) を販売する上で必要となる **ValueMap** を確認します。</span><span class="sxs-lookup"><span data-stu-id="2adf0-142">Ensure that the needed **ValueMap** for selling **Unit of measure** (UOM) in Finance and Operations exists in the **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span></span>

-   <span data-ttu-id="2adf0-143">**ソース \> CD** の順に移動し、[**CDS の組織 ID (Organization_OrganizationId)**] を更新します。</span><span class="sxs-lookup"><span data-stu-id="2adf0-143">Update the **CDS Organization ID Organization_OrganizationId** in **Source -\> CDS**.</span></span>

    -   <span data-ttu-id="2adf0-144">テンプレート値のデフォルトは ORG001 です。</span><span class="sxs-lookup"><span data-stu-id="2adf0-144">Template value is defaulted to ORG001.</span></span>

-   <span data-ttu-id="2adf0-145">**CD -\>出力先**の順に移動し、**単位グループ** (**defaultuomscheduleid.name**) の **ValueMap** を更新し、売上の**単位グループ**に一致させます。</span><span class="sxs-lookup"><span data-stu-id="2adf0-145">Update **ValueMap** for **Unit group** (**defaultuomscheduleid.name**) in **CDS -\> Destination** to match the **Unit groups** in Sales.</span></span>

    -   <span data-ttu-id="2adf0-146">テンプレート値のデフォルトは**既定単位**です。</span><span class="sxs-lookup"><span data-stu-id="2adf0-146">Template value is defaulted to **Default unit**.</span></span>

-   <span data-ttu-id="2adf0-147">**CDS 候補リスト**値を使用し、Finance and Operations の UOM を販売するすべての製品が売上に存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="2adf0-147">Ensure that all products selling UOMs from Finance and Operations exist in Sales with the **CDS picklists** value.</span></span>

-   <span data-ttu-id="2adf0-148">**価格表** が、Finance and Operations の製品販売通貨ごとに売上に存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="2adf0-148">Ensure that **Price lists** exist in Sales for each product sales currency in Finance and Operations.</span></span>

-   <span data-ttu-id="2adf0-149">製品は、ステータスが**ドラフト**または**有効**である売上で作成することができます。</span><span class="sxs-lookup"><span data-stu-id="2adf0-149">Products can be created in Sales with status **Draft** or **Active**.</span></span> <span data-ttu-id="2adf0-150">これは、売上にある**売上**の**システム設定**で管理できます。</span><span class="sxs-lookup"><span data-stu-id="2adf0-150">This is controlled in **System settings** under **Sales** in Sales.</span></span>

    -   <span data-ttu-id="2adf0-151">ドラフト ステータスで作成された製品は、**見積**または**販売注文**に追加する前にアクティブ化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2adf0-151">Products created with draft status need to be activated before they can be added to **Quote** or **Sales order**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="2adf0-152">データ インテグレーターでテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="2adf0-152">Template mapping in data integrator</span></span>

<span data-ttu-id="2adf0-153">次の図は、データ インテグレーターのテンプレート マッピングの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="2adf0-153">The following illustrations show an example of a template mapping in data integrator.</span></span>

![データ インテグレーターのテンプレートのマッピング](./media/products-template-mapping-data-integrator-1.png)

![データ インテグレーターの製品のテンプレート マッピング](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="2adf0-156">関連トピック</span><span class="sxs-lookup"><span data-stu-id="2adf0-156">Related topics</span></span>

[<span data-ttu-id="2adf0-157">Finance and Operations で売上勘定を顧客に同期する</span><span class="sxs-lookup"><span data-stu-id="2adf0-157">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="2adf0-158">Finance and Operations の連絡先または顧客への Sales の連絡先の同期</span><span class="sxs-lookup"><span data-stu-id="2adf0-158">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="2adf0-159">販売見積ヘッダーおよび明細行の Sales から Finance and Operations への同期</span><span class="sxs-lookup"><span data-stu-id="2adf0-159">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="2adf0-160">販売注文ヘッダーおよび明細行の Finance and Operations から Sales への同期</span><span class="sxs-lookup"><span data-stu-id="2adf0-160">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="2adf0-161">売上請求書ヘッダーおよび明細行の Finance and Operations から Sales への同期</span><span class="sxs-lookup"><span data-stu-id="2adf0-161">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


