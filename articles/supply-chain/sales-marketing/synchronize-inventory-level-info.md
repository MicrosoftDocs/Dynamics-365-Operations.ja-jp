---
title: Finance and Operations から Field Service への在庫レベル情報の同期
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に在庫レベル情報を同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
manager: AnnBe
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: c7dce4427810b93e0ee4f1a27881c2b1b04fb125
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1535701"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="da8bd-103">Finance and Operations から Field Service への在庫レベル情報の同期</span><span class="sxs-lookup"><span data-stu-id="da8bd-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="da8bd-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に在庫レベル情報を同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="da8bd-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="da8bd-105">[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="da8bd-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="da8bd-106">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="da8bd-106">Templates and tasks</span></span>
<span data-ttu-id="da8bd-107">次のテンプレートと基本的なタスクは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service への手持在庫レベルの同期を実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="da8bd-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="da8bd-108">**データ統合でのテンプレート**</span><span class="sxs-lookup"><span data-stu-id="da8bd-108">**Template in Data integration**</span></span>
- <span data-ttu-id="da8bd-109">製品在庫 (Fin and Ops から Field Service)</span><span class="sxs-lookup"><span data-stu-id="da8bd-109">Product Inventory (Fin and Ops to Field Service)</span></span>
  
<span data-ttu-id="da8bd-110">**データ統合プロジェクトのタスク**</span><span class="sxs-lookup"><span data-stu-id="da8bd-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="da8bd-111">製品在庫</span><span class="sxs-lookup"><span data-stu-id="da8bd-111">Product inventory</span></span>

<span data-ttu-id="da8bd-112">在庫レベルの同期が処理される前に、次の同期タスクが必要です。</span><span class="sxs-lookup"><span data-stu-id="da8bd-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="da8bd-113">倉庫 (Finance and Operations から Field Service)</span><span class="sxs-lookup"><span data-stu-id="da8bd-113">Warehouses (Fin and Ops to Field Service)</span></span> 
- <span data-ttu-id="da8bd-114">在庫単位のある Field Service 製品 (Fin and Ops から Sales)</span><span class="sxs-lookup"><span data-stu-id="da8bd-114">Field Service products with Inventory unit (Fin and Ops to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="da8bd-115">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="da8bd-115">Entity set</span></span>

| <span data-ttu-id="da8bd-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="da8bd-116">Field Service</span></span>                      | <span data-ttu-id="da8bd-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="da8bd-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="da8bd-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="da8bd-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="da8bd-119">CDS 倉庫別手持在庫</span><span class="sxs-lookup"><span data-stu-id="da8bd-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="da8bd-120">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="da8bd-120">Entity flow</span></span>
<span data-ttu-id="da8bd-121">Finance and Operations からの在庫レベル情報は、選択した製品の Field Service に送信されます。</span><span class="sxs-lookup"><span data-stu-id="da8bd-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="da8bd-122">在庫レベル情報は次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="da8bd-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="da8bd-123">手持在庫数量 (倉庫にある現在記録されている現物数量)</span><span class="sxs-lookup"><span data-stu-id="da8bd-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="da8bd-124">注文数量 (販売注文などの記録された合計注文数量)</span><span class="sxs-lookup"><span data-stu-id="da8bd-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="da8bd-125">注文済数量 (発注書記録された合計注文済数量)</span><span class="sxs-lookup"><span data-stu-id="da8bd-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="da8bd-126">この情報は、各倉庫にリリースされた製品ごとにキャプチャされ、在庫レベルが変更されると、変更追跡に基づいて同期されます。</span><span class="sxs-lookup"><span data-stu-id="da8bd-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="da8bd-127">Field Service では、統合ソリューションがデルタ用の在庫仕訳帳を作成し、Field Service のレベルを Finance and Operations のレベルと一致するようにします。</span><span class="sxs-lookup"><span data-stu-id="da8bd-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Finance and Operations.</span></span>

<span data-ttu-id="da8bd-128">Finance and Operations は、在庫レベルのマスターとして機能します。</span><span class="sxs-lookup"><span data-stu-id="da8bd-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="da8bd-129">したがって、この機能を Finance and Operations からの在庫レベルの同期と共に Field Service で使用する場合は、ワーク オーダー、振替および調整を、Field Service から Finance and Operations に統合設定することが重要です。</span><span class="sxs-lookup"><span data-stu-id="da8bd-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Finance and Operations if this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="da8bd-130">在庫レベルが Finance and Operations から習得されている製品および倉庫は、高度なクエリおよびフィルタリング (Power Query) で制御できます。</span><span class="sxs-lookup"><span data-stu-id="da8bd-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="da8bd-131">Field Services で複数の倉庫を作成し (**外部で管理 = いいえ**)、Finance and Operations で高度なクエリおよびフィルター処理を使用して 1 つの倉庫にマッピングすることができます。</span><span class="sxs-lookup"><span data-stu-id="da8bd-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="da8bd-132">これは、Field service に詳細な在庫レベルを習得させ、Finance and Operations に更新を送信するだけの場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="da8bd-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Finance and Operations.</span></span> <span data-ttu-id="da8bd-133">この場合、Field service は、Finance and Operations からの在庫レベルの更新は受信しません。</span><span class="sxs-lookup"><span data-stu-id="da8bd-133">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="da8bd-134">追加情報については、「[Field Service から Finance and Operations への在庫調整の同期](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments)」および「[Field Service でのワーク オーダーを Finance and Operations のプロジェクトにリンクされている販売注文に同期](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="da8bd-134">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="da8bd-135">Field Service CRM ソリューション</span><span class="sxs-lookup"><span data-stu-id="da8bd-135">Field Service CRM solution</span></span>
<span data-ttu-id="da8bd-136">**外部の製品在庫**エンティティは、統合へのバックエンドのみに使用されます。</span><span class="sxs-lookup"><span data-stu-id="da8bd-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="da8bd-137">このエンティティは統合内の Finance and Operations から在庫レベルの値を受け取り、次のそれらの値を Manuel 在庫仕訳帳に変換します。これにより、倉庫の在庫製品が変更されます。</span><span class="sxs-lookup"><span data-stu-id="da8bd-137">This entity receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="da8bd-138">前提条件およびマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="da8bd-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration"></a><span data-ttu-id="da8bd-139">データ統合</span><span class="sxs-lookup"><span data-stu-id="da8bd-139">Data integration</span></span>
<span data-ttu-id="da8bd-140">プロジェクトを機能させるには、統合キーが msdynce_externalproductinventories 用に更新されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="da8bd-140">For the project to work, you need to ensure that the Integration key is updated for msdynce_externalproductinventories.</span></span>
1.  <span data-ttu-id="da8bd-141">**データ統合 > 接続セット**に移動します。</span><span class="sxs-lookup"><span data-stu-id="da8bd-141">Go to **Data integration > Connection sets**.</span></span>
2.  <span data-ttu-id="da8bd-142">使用する接続設定を選択します。</span><span class="sxs-lookup"><span data-stu-id="da8bd-142">Select the used Connection set.</span></span>
3.  <span data-ttu-id="da8bd-143">**統合キー**タブで、次のキーが msdynce_externalproductinventories に追加されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="da8bd-143">On the **Integration key** tab, ensure that the following keys are added to msdynce_externalproductinventories:</span></span>
      - <span data-ttu-id="da8bd-144">msdynce_productnumber (製品番号)</span><span class="sxs-lookup"><span data-stu-id="da8bd-144">msdynce_productnumber (Product Number)</span></span>
      - <span data-ttu-id="da8bd-145">msdynce_warehouseid (倉庫 ID)</span><span class="sxs-lookup"><span data-stu-id="da8bd-145">msdynce_warehouseid (Warehouse ID)</span></span>
      
### <a name="data-integration-project"></a><span data-ttu-id="da8bd-146">データ統合プロジェクト</span><span class="sxs-lookup"><span data-stu-id="da8bd-146">Data integration project</span></span>
<span data-ttu-id="da8bd-147">フィルターを高度なクエリおよびフィルタリングに適用し、特定の製品および倉庫のみが在庫レベル情報を Finance and Operations から Field Service に送信するようにします。</span><span class="sxs-lookup"><span data-stu-id="da8bd-147">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="da8bd-148">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="da8bd-148">Template mapping in Data integration</span></span>

### <a name="product-inventory-fin-and-ops-to-field-service-product-inventory"></a><span data-ttu-id="da8bd-149">製品在庫 (Fin and Ops から Field Service): 製品在庫</span><span class="sxs-lookup"><span data-stu-id="da8bd-149">Product inventory (Fin and Ops to Field Service): Product inventory</span></span>

<span data-ttu-id="da8bd-150">[![データ統合のテンプレートのマッピング](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="da8bd-150">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>
