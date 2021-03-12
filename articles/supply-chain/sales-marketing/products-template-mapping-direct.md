---
title: 製品を Supply Chain Management から Sales の製品に直接同期する
description: このトピックでは、Dynamics 365 Supply Chain Management から Dynamics 365 Sales に製品を同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
manager: tfehr
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: ecee843b6c09c86b4e40ab34cc113e5a7e7c76f8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977691"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a><span data-ttu-id="cfd68-103">製品を Supply Chain Management から Sales の製品に直接同期する</span><span class="sxs-lookup"><span data-stu-id="cfd68-103">Synchronize products directly from Supply Chain Management to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="cfd68-104">見込顧客を現金化するソリューションを使用する前に、[Microsoft Dataverse for Apps へデータを統合](https://docs.microsoft.com/powerapps/administrator/data-integrator) をよく理解しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="cfd68-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="cfd68-105">このトピックでは、Dynamics 365 Supply Chain Management から Dynamics 365 Sales に製品を直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="cfd68-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="cfd68-106">見込み客の現金化へのデータフロー</span><span class="sxs-lookup"><span data-stu-id="cfd68-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="cfd68-107">見込み客の現金化ソリューションは、Supply Chain Management と Sales のインスタンス間でデータを同期するため、データの統合機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="cfd68-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="cfd68-108">データ統合機能で利用可能な見込み顧客を現金化するテンプレートにより、Supply Chain Management と Sales 間での勘定、連絡先、製品および販売見積、販売注文、および売上請求書のデータの流れが可能になります。</span><span class="sxs-lookup"><span data-stu-id="cfd68-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="cfd68-109">次の図は、Supply Chain Management と Sales の間でデータを同期させる方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="cfd68-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="cfd68-110">[![見込み客の現金化へのデータフロー](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="cfd68-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="cfd68-111">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="cfd68-111">Templates and tasks</span></span>

<span data-ttu-id="cfd68-112">利用可能なテンプレートにアクセスするには、[Power Apps 管理者センター](https://admin.powerapps.com/dataintegration)を開きます。</span><span class="sxs-lookup"><span data-stu-id="cfd68-112">To access the available templates, open [Power Apps Admin Center](https://admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="cfd68-113">**プロジェクト** を選択した後、右上隅にある **新しいプロジェクト** を選択してパブリック テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="cfd68-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="cfd68-114">Supply Chain Management から Sales への製品同期には、以下のテンプレートと基本的なタスクが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cfd68-114">The following template and underlying tasks are used to synchronize products from Supply Chain Management to Sales.</span></span>

- <span data-ttu-id="cfd68-115">**データ統合における テンプレートの名前:** 製品 (Supply Chain Management から Sales)- 直接</span><span class="sxs-lookup"><span data-stu-id="cfd68-115">**Name of the template in Data integration:** Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="cfd68-116">**データ統合プロジェクトのタスク名:** 製品</span><span class="sxs-lookup"><span data-stu-id="cfd68-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="cfd68-117">製品の同期が発生する前に、同期タスクは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="cfd68-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="cfd68-118">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="cfd68-118">Entity set</span></span>

| <span data-ttu-id="cfd68-119">サプライ チェーン マネジメント</span><span class="sxs-lookup"><span data-stu-id="cfd68-119">Supply Chain Management</span></span>    | <span data-ttu-id="cfd68-120">販売注文</span><span class="sxs-lookup"><span data-stu-id="cfd68-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="cfd68-121">販売可能なリリース済製品</span><span class="sxs-lookup"><span data-stu-id="cfd68-121">Sellable released products</span></span> | <span data-ttu-id="cfd68-122">製品</span><span class="sxs-lookup"><span data-stu-id="cfd68-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="cfd68-123">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="cfd68-123">Entity flow</span></span>

<span data-ttu-id="cfd68-124">製品は Supply Chain Management で管理され、Sales に同期されます。</span><span class="sxs-lookup"><span data-stu-id="cfd68-124">Products are managed in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="cfd68-125">Supply Chain Management の **販売可能なリリース済製品** のデータ エンティティは、*販売可能* な製品のみをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="cfd68-125">The **Sellable released products** data entity in Supply Chain Management exports only products that are *sellable*.</span></span> <span data-ttu-id="cfd68-126">販売可能製品には、販売注文で使用する必要のある情報があります。</span><span class="sxs-lookup"><span data-stu-id="cfd68-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="cfd68-127">**リリースされた製品** ページで **検証** 機能を使用して製品を検証する場合も、同じルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="cfd68-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="cfd68-128">[製品番号] がキーとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="cfd68-128">The product number is used as a key.</span></span> <span data-ttu-id="cfd68-129">これは、製品バリアントが [製品バリアント] ごとの個別の [Product ID] で Sales に同期されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="cfd68-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="cfd68-130">売上の見込顧客を現金化するソリューション</span><span class="sxs-lookup"><span data-stu-id="cfd68-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="cfd68-131">Sales では、新しい **外部管理** フィールドが製品に追加され、特定の製品が外部で維持されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="cfd68-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="cfd68-132">デフォルトでは、値は Sales へのインポート時に **はい** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="cfd68-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="cfd68-133">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="cfd68-133">The following values are available:</span></span>

- <span data-ttu-id="cfd68-134">**はい** – 製品は Supply Chain Management に由来し、Sales では編集できません。</span><span class="sxs-lookup"><span data-stu-id="cfd68-134">**Yes** – The product originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="cfd68-135">**いいえ** – 製品は Sales に直接入力します。</span><span class="sxs-lookup"><span data-stu-id="cfd68-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="cfd68-136">**(空白)** – 見込顧客を現金化するソリューションを有効にする前に、製品が Sales に存在します。</span><span class="sxs-lookup"><span data-stu-id="cfd68-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="cfd68-137">**外部管理** フィールドは、外部管理された製品を持つ見積および受注のみが Supply Chain Management に同期されることを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="cfd68-137">The **Is Externally Maintained** field helps ensure that only quotations and sales orders that have externally maintained products will be synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="cfd68-138">外部管理の製品が、同じ通貨で最初に有効な価格リストに自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="cfd68-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="cfd68-139">価格リストは、名前がアルファベット順で構成されています。</span><span class="sxs-lookup"><span data-stu-id="cfd68-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="cfd68-140">Supply Chain Management の製品販売価格は価格リストの価格として使用されています。</span><span class="sxs-lookup"><span data-stu-id="cfd68-140">The product sales price from Supply Chain Management is used as the price on the price list.</span></span> <span data-ttu-id="cfd68-141">したがって、Supply Chain Management の製品販売通貨ごとに、Sales の価格リストが必要です。</span><span class="sxs-lookup"><span data-stu-id="cfd68-141">Therefore, there must be a price list in Sales for every product sales currency in Supply Chain Management.</span></span> <span data-ttu-id="cfd68-142">リリースされた販売可能商品の通貨は、製品が輸出される法人の会計通貨に設定されます。</span><span class="sxs-lookup"><span data-stu-id="cfd68-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> - <span data-ttu-id="cfd68-143">製品の同期は、一致する通貨を含む価格リストなしでは成功しません。</span><span class="sxs-lookup"><span data-stu-id="cfd68-143">Product synchronization will not succeed unless there is a price list that has a matching currency.</span></span>
> - <span data-ttu-id="cfd68-144">データ統合プロジェクトの pricelevelid.name [既定の価格リスト (名前)] をマッピングすることにより、統合に使用される価格リストを制御できます。</span><span class="sxs-lookup"><span data-stu-id="cfd68-144">You can control the used price list with the integration by mapping the pricelevelid.name [Default Price List (Name)] in the Data Integration project.</span></span> <span data-ttu-id="cfd68-145">入力値は、全小文字である必要があります。</span><span class="sxs-lookup"><span data-stu-id="cfd68-145">The input has to be in all lowercase letters.</span></span> <span data-ttu-id="cfd68-146">たとえば、'標準' という名前の販売での価格リストの既定値は、次のようになります。出力先フィールド: pricelevelid.name [既定の価格リスト (名前)]、およびタイプのマッピング: [ { "transformType": "既定", "defaultValue": "標準" } ]。</span><span class="sxs-lookup"><span data-stu-id="cfd68-146">For example, the default for a price list in Sales named ‘Standard’ would be: Destination field: pricelevelid.name [Default Price List (Name)] and Map type: [ { "transformType": "Default", "defaultValue": "standard" } ].</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="cfd68-147">前提条件とマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="cfd68-147">Preconditions and mapping setup</span></span>

- <span data-ttu-id="cfd68-148">一番最初の同期を実行する前に、Supply Chain Management の既存製品に対して特徴的製品テーブルを全て入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cfd68-148">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Supply Chain Management.</span></span> <span data-ttu-id="cfd68-149">このジョブが完了するまで、既存の製品は同期されません。</span><span class="sxs-lookup"><span data-stu-id="cfd68-149">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="cfd68-150">Supply Chain Management の場合は、検索を使用し、**特徴的製品テーブルの設定** を検索します。</span><span class="sxs-lookup"><span data-stu-id="cfd68-150">In Supply Chain Management, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="cfd68-151">**特徴的製品テーブル** を選択し、ジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="cfd68-151">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="cfd68-152">このジョブには、1回のみ実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cfd68-152">This job must be run only one time.</span></span>

- <span data-ttu-id="cfd68-153">**SalesUnitSymbol** から **DefaultUnit (Name)** へのマッピングに、Supply Chain Management と Sales の間における販売量測定単位 (UOM) に必要な値マップが存在することを確認してください。</span><span class="sxs-lookup"><span data-stu-id="cfd68-153">Make sure that the required value map for the selling unit of measure (UOM) between Supply Chain Management and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="cfd68-154">**単位グループ** (**defaultuomscheduleid.name**) の値マップを更新し、Sales の **単位グループ** に一致させます。</span><span class="sxs-lookup"><span data-stu-id="cfd68-154">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="cfd68-155">デフォルトのテンプレート値は、**既定単位** です。</span><span class="sxs-lookup"><span data-stu-id="cfd68-155">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="cfd68-156">Supply Chain Management からのすべての製品の販売 UOM が Sales に存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="cfd68-156">Make sure that the selling UOMs for all products from Supply Chain Management exist in Sales.</span></span>
- <span data-ttu-id="cfd68-157">価格リストが、Supply Chain Management の製品販売通貨ごとに Sales に存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="cfd68-157">Make sure that price lists exist in Sales for every product sales currency in Supply Chain Management.</span></span>
- <span data-ttu-id="cfd68-158">Sales で製品を作成すると、**ドラフト** または **有効** のステータスになります。</span><span class="sxs-lookup"><span data-stu-id="cfd68-158">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="cfd68-159">動作は、Sales の **設定** > **管理** > **システムの設定** > **販売** で制御されます。</span><span class="sxs-lookup"><span data-stu-id="cfd68-159">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="cfd68-160">作成時にステータスが **ドラフト** である製品は、見積書または販売注文に追加する前に有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cfd68-160">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cfd68-161">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="cfd68-161">Template mapping in Data integration</span></span>

<span data-ttu-id="cfd68-162">次の図は、データ インテグレーターのテンプレート マッピングの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="cfd68-162">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="cfd68-163">マッピングは、Sales から Supply Chain Management にどのフィールド情報を同期するかを表示します。</span><span class="sxs-lookup"><span data-stu-id="cfd68-163">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![データ インテグレーターのテンプレートのマッピング](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="cfd68-165">関連トピック</span><span class="sxs-lookup"><span data-stu-id="cfd68-165">Related topics</span></span>

[<span data-ttu-id="cfd68-166">見込顧客を現金化</span><span class="sxs-lookup"><span data-stu-id="cfd68-166">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="cfd68-167">Supply Chain Management の顧客への Sales の勘定の直接同期</span><span class="sxs-lookup"><span data-stu-id="cfd68-167">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="cfd68-168">Supply Chain Management の連絡先または顧客への Sales の連絡先の直接同期</span><span class="sxs-lookup"><span data-stu-id="cfd68-168">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="cfd68-169">販売注文の Sales と Supply Chain Management の間の直接同期</span><span class="sxs-lookup"><span data-stu-id="cfd68-169">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="cfd68-170">売上請求書のヘッダーおよび明細行の Supply Chain Management から Sales への直接同期</span><span class="sxs-lookup"><span data-stu-id="cfd68-170">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)



