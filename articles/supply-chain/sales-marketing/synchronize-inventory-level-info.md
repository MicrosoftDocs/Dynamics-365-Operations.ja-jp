---
title: "Finance and Operations から Field Service への在庫レベル情報の同期"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に在庫レベル情報を同期させるために使用されるテンプレートと基本的なタスクについて説明します。"
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: ja-jp
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="f09de-103">Finance and Operations から Field Service への在庫レベル情報の同期</span><span class="sxs-lookup"><span data-stu-id="f09de-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f09de-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に在庫レベル情報を同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f09de-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="f09de-105">[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="f09de-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="f09de-106">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="f09de-106">Templates and tasks</span></span>
<span data-ttu-id="f09de-107">次のテンプレートと基本的なタスクは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service への手持在庫レベルの同期を実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f09de-107">The following template and underlying tasks are used to run synchronization of inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="f09de-108">**データ統合でのテンプレートの名前:**</span><span class="sxs-lookup"><span data-stu-id="f09de-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="f09de-109">製品在庫 (Finance and Operations から Field Service)</span><span class="sxs-lookup"><span data-stu-id="f09de-109">Product Inventory (Finance and Operations to Field Service)</span></span>
  
<span data-ttu-id="f09de-110">**データ統合プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="f09de-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="f09de-111">製品在庫</span><span class="sxs-lookup"><span data-stu-id="f09de-111">Product inventory</span></span>

<span data-ttu-id="f09de-112">在庫レベルの同期が処理される前に、次の同期タスクが必要です。</span><span class="sxs-lookup"><span data-stu-id="f09de-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="f09de-113">倉庫 (Finance and Operations から Field Service)</span><span class="sxs-lookup"><span data-stu-id="f09de-113">Warehouses (Finance and Operations to Field Service)</span></span> 
- <span data-ttu-id="f09de-114">在庫単位のある Field Service 製品 (Finance and Operations から 販売)</span><span class="sxs-lookup"><span data-stu-id="f09de-114">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="f09de-115">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="f09de-115">Entity set</span></span>

| <span data-ttu-id="f09de-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="f09de-116">Field Service</span></span>                      | <span data-ttu-id="f09de-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f09de-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="f09de-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="f09de-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="f09de-119">CDS 倉庫別手持在庫</span><span class="sxs-lookup"><span data-stu-id="f09de-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="f09de-120">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="f09de-120">Entity flow</span></span>
<span data-ttu-id="f09de-121">Finance and Operations からの在庫レベル情報は、選択した製品の Field Service に送信されます。</span><span class="sxs-lookup"><span data-stu-id="f09de-121">Inventory level information from Finance and Operation is send to Field Service for selected products.</span></span> <span data-ttu-id="f09de-122">在庫レベル情報は次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="f09de-122">The inventory level information include:</span></span> 
- <span data-ttu-id="f09de-123">手持在庫数量 (倉庫にある現在記録されている現物数量)</span><span class="sxs-lookup"><span data-stu-id="f09de-123">On hand quantity (current recorded physically quantity located in the warehouse)</span></span>
- <span data-ttu-id="f09de-124">注文数量 (記録された合計注文数量 - 販売注文)</span><span class="sxs-lookup"><span data-stu-id="f09de-124">On order quantity (total recorded quantity on order - i.e. sales orders)</span></span>
- <span data-ttu-id="f09de-125">注文済数量 (記録された合計注文済数量 - 発注書)</span><span class="sxs-lookup"><span data-stu-id="f09de-125">Ordered quantity (total recorded ordered quantity - i.e. purchase orders)</span></span>

<span data-ttu-id="f09de-126">この情報は、各倉庫にリリースされた製品ごとにキャプチャされ、在庫レベルが変更されると、変更追跡に基づいて同期されます。</span><span class="sxs-lookup"><span data-stu-id="f09de-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="f09de-127">Field Service では、統合ソリューションがデルタ用の在庫仕訳帳を作成し、Field Service のレベルを Finance and Operations のレベルと一致させます。</span><span class="sxs-lookup"><span data-stu-id="f09de-127">In Field Service the integration solution create inventory journals for the delta, to get the levels in Field Service to match the levels in Finance and Operations.</span></span>

<span data-ttu-id="f09de-128">Finance and Operations は、在庫レベルのマスターとして機能します。</span><span class="sxs-lookup"><span data-stu-id="f09de-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="f09de-129">したがって、この機能を Finance and Operations からの在庫レベルの同期と共に Field Service で使用する場合は、ワークオーダー、振替および調整を、Field Service から Finance and Operations に統合設定することが重要です。</span><span class="sxs-lookup"><span data-stu-id="f09de-129">So it is important to setup integration for workorders, transfers and adjustments from Field Service to Finance and Operations if the this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="f09de-130">在庫レベルが Finance and Operations から習得されている製品および倉庫は、高度なクエリおよびフィルタリング (Power Query) で制御できます。</span><span class="sxs-lookup"><span data-stu-id="f09de-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

<span data-ttu-id="f09de-131">Field Services で複数の倉庫を作成し (外部で管理 = いいえの場合)、Finance and Operations で高度なクエリおよびフィルター処理を使用して 1 つの倉庫にマッピングすることができます。</span><span class="sxs-lookup"><span data-stu-id="f09de-131">Note: It is possible to create multiple warehouses in Field Services (with Is Externally Maintained = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="f09de-132">これは、Field service に詳細な在庫レベルを習得させ、Finance and Operations に更新を送信するだけの場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="f09de-132">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="f09de-133">この場合、Field service は、Finance and Operations からの在庫レベルの更新は受信しません。</span><span class="sxs-lookup"><span data-stu-id="f09de-133">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="f09de-134">追加情報については、Field Service から Finance and Operations への在庫調整の同期、および Field Service でのワーク オーダーを Finance and Operations のプロジェクトにリンクされている販売注文に同期、を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f09de-134">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="f09de-135">Field Service CRM ソリューション</span><span class="sxs-lookup"><span data-stu-id="f09de-135">Field Service CRM solution</span></span>
<span data-ttu-id="f09de-136">外部の製品在庫エンティティは、統合のバックエンドのみに使用される新しいエンティティです。</span><span class="sxs-lookup"><span data-stu-id="f09de-136">The External Product Inventory entity is a new entity that’s only used for backend in the integration.</span></span> <span data-ttu-id="f09de-137">統合内の Finance and Operations から在庫レベルの値を受け取り、次のそれらの値を Manuel 在庫仕訳帳に変換します。これにより、倉庫の在庫製品が変更されます。</span><span class="sxs-lookup"><span data-stu-id="f09de-137">It receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manuel Inventory journals, that then changes the Inventory Products on the Warehouse.</span></span> 

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="f09de-138">前提条件およびマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="f09de-138">Prerequisites and mapping setup</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="f09de-139">データ統合プロジェクト内</span><span class="sxs-lookup"><span data-stu-id="f09de-139">In the Data Integration project</span></span>
<span data-ttu-id="f09de-140">高度なクエリおよびフィルタリングを使用してフィルターを適用し、必要な製品および倉庫のみが在庫レベル情報を Finance and Operations から Field Service に送信するように制御します。</span><span class="sxs-lookup"><span data-stu-id="f09de-140">Apply filters with the Advanced  Query and Filtering to control that only desired products and warehouses send inventory level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f09de-141">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="f09de-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a><span data-ttu-id="f09de-142">製品在庫 (Finance and Operations から Field Service): 製品在庫</span><span class="sxs-lookup"><span data-stu-id="f09de-142">Product Inventory (Finance and Operations to Field Service): Product inventory</span></span>

<span data-ttu-id="f09de-143">[![データ統合のテンプレートのマッピング](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="f09de-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>

