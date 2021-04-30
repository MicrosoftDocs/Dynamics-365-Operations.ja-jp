---
title: Supply Chain Management から Field Service への在庫レベル情報の同期
description: このトピックでは、Dynamics 365 Supply Chain Management から Dynamics 365 Field Service に在庫レベル情報を同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
ms.date: 05/07/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 15466699b94c284208330d50b840c874534b879c
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910283"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a><span data-ttu-id="bc37f-103">Supply Chain Management から Field Service への在庫レベル情報の同期</span><span class="sxs-lookup"><span data-stu-id="bc37f-103">Synchronize inventory level information from Supply Chain Management to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="bc37f-104">このトピックでは、Dynamics 365 Supply Chain Management から Dynamics 365 Field Service に在庫レベル情報を同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="bc37f-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="bc37f-105">[![Supply Chain Management および Field Service 間の業務プロセスの同期](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="bc37f-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="bc37f-106">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="bc37f-106">Templates and tasks</span></span>
<span data-ttu-id="bc37f-107">次のテンプレートと基本的なタスクは、Supply Chain Management から Field Service に手持在庫レベルの同期を実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="bc37f-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="bc37f-108">**データ統合でのテンプレート**</span><span class="sxs-lookup"><span data-stu-id="bc37f-108">**Template in Data integration**</span></span>
- <span data-ttu-id="bc37f-109">製品在庫 (Supply Chain Management から Field Service)</span><span class="sxs-lookup"><span data-stu-id="bc37f-109">Product Inventory (Supply Chain Management to Field Service)</span></span>
  
<span data-ttu-id="bc37f-110">**データ統合プロジェクトのタスク**</span><span class="sxs-lookup"><span data-stu-id="bc37f-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="bc37f-111">製品在庫</span><span class="sxs-lookup"><span data-stu-id="bc37f-111">Product inventory</span></span>

<span data-ttu-id="bc37f-112">在庫レベルの同期が処理される前に、次の同期タスクが必要です。</span><span class="sxs-lookup"><span data-stu-id="bc37f-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="bc37f-113">倉庫 (Supply Chain Management から Field Service)</span><span class="sxs-lookup"><span data-stu-id="bc37f-113">Warehouses (Supply Chain Management to Field Service)</span></span> 
- <span data-ttu-id="bc37f-114">在庫単位のある Field Service 製品 (Supply Chain Management から Sales)</span><span class="sxs-lookup"><span data-stu-id="bc37f-114">Field Service products with Inventory unit (Supply Chain Management to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="bc37f-115">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="bc37f-115">Entity set</span></span>

| <span data-ttu-id="bc37f-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="bc37f-116">Field Service</span></span>                      | <span data-ttu-id="bc37f-117">サプライ チェーン マネジメント</span><span class="sxs-lookup"><span data-stu-id="bc37f-117">Supply Chain Management</span></span>                |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="bc37f-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="bc37f-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="bc37f-119">倉庫別 Dataverse手持在庫</span><span class="sxs-lookup"><span data-stu-id="bc37f-119">Dataverse inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="bc37f-120">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="bc37f-120">Entity flow</span></span>
<span data-ttu-id="bc37f-121">Finance and Operations からの在庫レベル情報は、選択した製品の Field Service に送信されます。</span><span class="sxs-lookup"><span data-stu-id="bc37f-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="bc37f-122">在庫レベル情報は次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="bc37f-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="bc37f-123">手持在庫数量 (倉庫にある現在記録されている現物数量)</span><span class="sxs-lookup"><span data-stu-id="bc37f-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="bc37f-124">注文数量 (販売注文などの記録された合計注文数量)</span><span class="sxs-lookup"><span data-stu-id="bc37f-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="bc37f-125">注文済数量 (発注書記録された合計注文済数量)</span><span class="sxs-lookup"><span data-stu-id="bc37f-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="bc37f-126">この情報は、各倉庫にリリースされた製品ごとにキャプチャされ、在庫レベルが変更されると、変更追跡に基づいて同期されます。</span><span class="sxs-lookup"><span data-stu-id="bc37f-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="bc37f-127">Field Service では、統合ソリューションがデルタ用の在庫仕訳帳を作成し、Field Service のレベルを Supply Chain Management のレベルと一致するようにします。</span><span class="sxs-lookup"><span data-stu-id="bc37f-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Supply Chain Management.</span></span>

<span data-ttu-id="bc37f-128">Supply Chain Management は、在庫レベルのマスターとして機能します。</span><span class="sxs-lookup"><span data-stu-id="bc37f-128">Supply Chain Management will act as the master for inventory levels.</span></span> <span data-ttu-id="bc37f-129">したがって、この機能を Supply Chain Management からの在庫レベルの同期と共に Field Service で使用する場合は、ワーク オーダー、振替および調整を Field Service から Supply Chain Management に統合設定することが重要です。</span><span class="sxs-lookup"><span data-stu-id="bc37f-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Supply Chain Management if this functionality is used in Field Service, together with synchronization of inventory levels from Supply Chain Management.</span></span>

<span data-ttu-id="bc37f-130">在庫レベルが Supply Chain Management から習得されている製品および倉庫は、高度なクエリおよびフィルタリング (Power Query) で制御できます。</span><span class="sxs-lookup"><span data-stu-id="bc37f-130">The products and warehouses where inventory levels are mastered from Supply Chain Management can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="bc37f-131">Field Services で複数の倉庫を作成し (**外部で管理 = いいえ**)、Supply Chain Management で高度なクエリおよびフィルター処理を使用して 1 つの倉庫にマッピングすることができます。</span><span class="sxs-lookup"><span data-stu-id="bc37f-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Supply Chain Management, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="bc37f-132">これは、Field service に詳細な在庫レベルを習得させ、Supply Chain Management に更新を送信するだけの場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="bc37f-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Supply Chain Management.</span></span> <span data-ttu-id="bc37f-133">この場合、Field service では、Supply Chain Management からの在庫レベルの更新は受信しません。</span><span class="sxs-lookup"><span data-stu-id="bc37f-133">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="bc37f-134">追加情報については、「[Field Service から Supply Chain Management への在庫調整の同期](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments)」および「[Field Service でのワーク オーダーを Supply Chain Management のプロジェクトにリンクされている販売注文に同期](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bc37f-134">For additional information, see [Synchronize inventory adjustments from Field Service to Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="bc37f-135">Field Service CRM ソリューション</span><span class="sxs-lookup"><span data-stu-id="bc37f-135">Field Service CRM solution</span></span>
<span data-ttu-id="bc37f-136">**外部の製品在庫** エンティティは、統合へのバックエンドのみに使用されます。</span><span class="sxs-lookup"><span data-stu-id="bc37f-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="bc37f-137">このエンティティは統合内の Supply Chain Management から在庫レベルの値を受け取り、次のそれらの値を Manuel 在庫仕訳帳に変換します。これにより、倉庫の在庫製品が変更されます。</span><span class="sxs-lookup"><span data-stu-id="bc37f-137">This entity receives the inventory level values from Supply Chain Management in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="bc37f-138">前提条件およびマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="bc37f-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration"></a><span data-ttu-id="bc37f-139">データ統合</span><span class="sxs-lookup"><span data-stu-id="bc37f-139">Data integration</span></span>
<span data-ttu-id="bc37f-140">プロジェクトを機能させるには、統合キーが msdynce_externalproductinventories 用に更新されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc37f-140">For the project to work, you need to ensure that the Integration key is updated for msdynce_externalproductinventories.</span></span>
1.  <span data-ttu-id="bc37f-141">**データ統合 > 接続セット** に移動します。</span><span class="sxs-lookup"><span data-stu-id="bc37f-141">Go to **Data integration > Connection sets**.</span></span>
2.  <span data-ttu-id="bc37f-142">使用する接続設定を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc37f-142">Select the used Connection set.</span></span>
3.  <span data-ttu-id="bc37f-143">**統合キー** タブで、次のキーが msdynce_externalproductinventories に追加されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bc37f-143">On the **Integration key** tab, ensure that the following keys are added to msdynce_externalproductinventories:</span></span>
      - <span data-ttu-id="bc37f-144">msdynce_productnumber (製品番号)</span><span class="sxs-lookup"><span data-stu-id="bc37f-144">msdynce_productnumber (Product Number)</span></span>
      - <span data-ttu-id="bc37f-145">msdynce_warehouseid (倉庫 ID)</span><span class="sxs-lookup"><span data-stu-id="bc37f-145">msdynce_warehouseid (Warehouse ID)</span></span>
      
### <a name="data-integration-project"></a><span data-ttu-id="bc37f-146">データ統合プロジェクト</span><span class="sxs-lookup"><span data-stu-id="bc37f-146">Data integration project</span></span>
<span data-ttu-id="bc37f-147">フィルターを高度なクエリおよびフィルタリングに適用し、特定の製品および倉庫のみが在庫レベル情報を Supply Chain Management から Field Service に送信するようにします。</span><span class="sxs-lookup"><span data-stu-id="bc37f-147">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Supply Chain Management to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="bc37f-148">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="bc37f-148">Template mapping in Data integration</span></span>

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a><span data-ttu-id="bc37f-149">製品在庫 (Supply Chain Management から Field Service): 製品在庫</span><span class="sxs-lookup"><span data-stu-id="bc37f-149">Product inventory (Supply Chain Management to Field Service): Product inventory</span></span>

<span data-ttu-id="bc37f-150">[![データ統合のテンプレートのマッピング](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="bc37f-150">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]