---
title: "Field Service から Finance and Operations への在庫振替と調整の同期"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に在庫調整と振替を同期させるために使用されるテンプレートと基本的なタスクについて説明します。"
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
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: ja-jp
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="67147-103">Field Service から Finance and Operations への在庫調整の同期</span><span class="sxs-lookup"><span data-stu-id="67147-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="67147-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に在庫調整と振替を同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="67147-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="67147-105">[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="67147-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="67147-106">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="67147-106">Templates and tasks</span></span>
<span data-ttu-id="67147-107">次のテンプレートと基本的なタスクは、Microsoft Dynamics 365 for Field Service から Microsoft Dynamics 365 for Finance and Operations への在庫調整と振替の同期を実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="67147-107">The following template and underlying tasks are used to run synchronization of inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="67147-108">**データ統合におけるテンプレートの名前:**</span><span class="sxs-lookup"><span data-stu-id="67147-108">**Name of the templates in Data integration:**</span></span>
- <span data-ttu-id="67147-109">在庫調整 (Field Service から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="67147-109">Inventory Adjustment (Field Service to Finance and Operations)</span></span>
- <span data-ttu-id="67147-110">在庫振替 (Field Service から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="67147-110">Inventory Transfers (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="67147-111">**データ統合プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="67147-111">**Names of the tasks in the Data integration projects:**</span></span>
- <span data-ttu-id="67147-112">在庫調整</span><span class="sxs-lookup"><span data-stu-id="67147-112">Inventory Adjustments</span></span>
- <span data-ttu-id="67147-113">在庫振替</span><span class="sxs-lookup"><span data-stu-id="67147-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="67147-114">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="67147-114">Entity set</span></span>
| <span data-ttu-id="67147-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="67147-115">Field Service</span></span>                     | <span data-ttu-id="67147-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="67147-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="67147-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="67147-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="67147-118">CDS 在庫調整仕訳帳のヘッダーおよび明細行</span><span class="sxs-lookup"><span data-stu-id="67147-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="67147-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="67147-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="67147-120">CDS 在庫移動仕訳帳のヘッダーおよび明細行</span><span class="sxs-lookup"><span data-stu-id="67147-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="67147-121">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="67147-121">Entity flow</span></span>
<span data-ttu-id="67147-122">**ステータスを転記**が作成済から転記済に変更されると、Field Service で行われた在庫調整と振替は Finance and Operations と同期します。</span><span class="sxs-lookup"><span data-stu-id="67147-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations, once the **Post status** is changed from Created to Posted.</span></span> <span data-ttu-id="67147-123">これが発生すると、調整および振替は Finance and Operations に転記される可能性があり、調整および振替のオーダーがロックされ読み取り専用になるため、変更することができません。</span><span class="sxs-lookup"><span data-stu-id="67147-123">When this happen the adjustment or transfer order will be locked and become read-only, as adjustments and transfers might be posted in Finance and Operations and therefor can't be modified.</span></span>
<span data-ttu-id="67147-124">Finance and Operations では、調整を自動的に転記し、統合によって生成された在庫仕訳帳を振り替えるようにバッチ ジョブを設定できます。</span><span class="sxs-lookup"><span data-stu-id="67147-124">In Finance and Operations you can setup a batch job to automatically post the adjustments and transfer inventory journals generated with the integration.</span></span> <span data-ttu-id="67147-125">バッチ ジョブを有効にする方法の詳細については、以下の前提条件を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67147-125">See prerequisite below for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="67147-126">Field Service CRM ソリューション</span><span class="sxs-lookup"><span data-stu-id="67147-126">Field Service CRM solution</span></span> 
<span data-ttu-id="67147-127">在庫単位のフィールドは、製品のエンティティに追加されました。</span><span class="sxs-lookup"><span data-stu-id="67147-127">The Inventory Unit field has been added to the Product entity.</span></span> <span data-ttu-id="67147-128">販売および在庫単位は工程で常に同じであるとは限らないため、このフィールドは必要です。また倉庫在庫の工程では、在庫単位が必要です。</span><span class="sxs-lookup"><span data-stu-id="67147-128">This field is needed since the Sales and Inventory Unit is not always the same in Operations, and for the Warehouse Inventory in operations we need the Inventory Unit.</span></span>
<span data-ttu-id="67147-129">在庫調整と在庫振替の両方の在庫調整製品に製品を設定すると、製品在庫製品の値から単位がフェッチされます。</span><span class="sxs-lookup"><span data-stu-id="67147-129">When you set the Product on an Inventory Adjustment Product for both Inventory Adjustments and Inventory Transfers the Unit will be fetched from the Products Inventory Product value.</span></span> <span data-ttu-id="67147-130">値が見つかると、在庫調整製品の単位フィールドがロックされます。</span><span class="sxs-lookup"><span data-stu-id="67147-130">If a value is found the Unit field will be locked on the Inventory Adjustment Product</span></span>

<span data-ttu-id="67147-131">在庫調整のエンティティと、在庫振替のエンティティの両方に、転記ステータス フィールドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="67147-131">The Post Status field has been added to both the Inventory Adjustment entity and the Inventory Transfer entity.</span></span> <span data-ttu-id="67147-132">このフィールドは、調整または振替が工程に送信されるときにフィルターとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="67147-132">This field is used as a filter for when a adjustment or transfer is sent to Operations.</span></span> <span data-ttu-id="67147-133">このフィールドは、既定で作成 (1) に設定されており、工程には送信されません。</span><span class="sxs-lookup"><span data-stu-id="67147-133">The field is defaulted to Created (1) and its then not sent over to Operations.</span></span> <span data-ttu-id="67147-134">変更したものは転記済 (2) になり工程に送信されますが、以降調整または振替で何かを変更したり、新しい明細行を追加することはできなくなります。</span><span class="sxs-lookup"><span data-stu-id="67147-134">Ones you change is to Posted (2) It is sent over to operations, but you will then no longer be able to change anything in the Adjustment or Transfer or add any new lines to it.</span></span>
<span data-ttu-id="67147-135">番号順序のフィールドは、在庫調整製品のエンティティに追加されました。</span><span class="sxs-lookup"><span data-stu-id="67147-135">The Number Sequence field has been added to the Inventory Adjustment Product entity.</span></span> <span data-ttu-id="67147-136">このフィールドは、統合が一意の番号を持つのに役立ちます。そのため、統合がいつ作成を行い、いつ更新を行うかを認識します。</span><span class="sxs-lookup"><span data-stu-id="67147-136">This field helps the integration to have a Unique number, so the integration knows when to do creates and when to do updates.</span></span> <span data-ttu-id="67147-137">最初の在庫調整製品を作成すると、P2C 自動採番エンティティに新しいレコードが作成され、番号シリーズと使用される接頭語が維持されます。</span><span class="sxs-lookup"><span data-stu-id="67147-137">When you create your first Inventory Adjustment Product it will create a new record in the P2C AutoNumber entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="67147-138">前提条件およびマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="67147-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="67147-139">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="67147-139">In Finance and Operations</span></span>
<span data-ttu-id="67147-140">統合によって生成される統合在庫仕訳帳は、バッチ ジョブに自動的に転記されます。</span><span class="sxs-lookup"><span data-stu-id="67147-140">The integration inventory journals generated by the integration can automatically be posted with a batch job.</span></span> <span data-ttu-id="67147-141">これは、次で有効になります: 在庫管理 > 定期処理タスク > CDS 統合 > 統合在庫仕訳帳の転記</span><span class="sxs-lookup"><span data-stu-id="67147-141">This is enabled from: Inventory management > Periodic tasks > CDS integration > Post integration inventory journals</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="67147-142">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="67147-142">Template mapping in Data integration</span></span>

<span data-ttu-id="67147-143">次の図は、データ統合のテンプレート マッピングを示しています。</span><span class="sxs-lookup"><span data-stu-id="67147-143">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a><span data-ttu-id="67147-144">在庫調整 (Field Service から Finance and Operations): 在庫調整</span><span class="sxs-lookup"><span data-stu-id="67147-144">Inventory Adjustment (Field Service to Finance and Operations): Inventory Adjustment</span></span>

<span data-ttu-id="67147-145">[![データ統合のテンプレートのマッピング](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="67147-145">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a><span data-ttu-id="67147-146">在庫振替 (Field Service から Finance and Operations): 在庫振替</span><span class="sxs-lookup"><span data-stu-id="67147-146">Inventory Transfer (Field Service to Finance and Operations): Inventory Transfer</span></span>

<span data-ttu-id="67147-147">[![データ統合のテンプレートのマッピング](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="67147-147">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>

