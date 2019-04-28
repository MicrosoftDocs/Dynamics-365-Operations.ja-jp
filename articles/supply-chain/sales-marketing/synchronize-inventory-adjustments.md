---
title: Field Service から Finance and Operations への在庫振替と調整の同期
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に在庫調整と振替を同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.openlocfilehash: 75181661c41d238cdc06ffbb6969a2efd7d88d46
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/14/2019
ms.locfileid: "842418"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="4baa8-103">Field Service から Finance and Operations への在庫調整の同期</span><span class="sxs-lookup"><span data-stu-id="4baa8-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4baa8-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に在庫調整と振替を同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4baa8-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="4baa8-105">[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="4baa8-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="4baa8-106">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="4baa8-106">Templates and tasks</span></span>
<span data-ttu-id="4baa8-107">次のテンプレートと基本的なタスクは、Microsoft Dynamics 365 for Field Service から Microsoft Dynamics 365 for Finance and Operations への在庫調整と振替の同期を実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4baa8-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="4baa8-108">**データ統合でのテンプレート**</span><span class="sxs-lookup"><span data-stu-id="4baa8-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="4baa8-109">在庫調整 (Field Service から Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="4baa8-109">Inventory Adjustment (Field Service to Fin and Ops)</span></span>
- <span data-ttu-id="4baa8-110">在庫振替 (Field Service から Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="4baa8-110">Inventory Transfers (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="4baa8-111">**データ統合プロジェクトのタスク:**</span><span class="sxs-lookup"><span data-stu-id="4baa8-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="4baa8-112">在庫調整</span><span class="sxs-lookup"><span data-stu-id="4baa8-112">Inventory Adjustments</span></span>
- <span data-ttu-id="4baa8-113">在庫振替</span><span class="sxs-lookup"><span data-stu-id="4baa8-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="4baa8-114">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="4baa8-114">Entity set</span></span>
| <span data-ttu-id="4baa8-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="4baa8-115">Field Service</span></span>                     | <span data-ttu-id="4baa8-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4baa8-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="4baa8-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="4baa8-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="4baa8-118">CDS 在庫調整仕訳帳のヘッダーおよび明細行</span><span class="sxs-lookup"><span data-stu-id="4baa8-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="4baa8-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="4baa8-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="4baa8-120">CDS 在庫移動仕訳帳のヘッダーおよび明細行</span><span class="sxs-lookup"><span data-stu-id="4baa8-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="4baa8-121">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="4baa8-121">Entity flow</span></span>
<span data-ttu-id="4baa8-122">**ステータスを転記**が**作成済**から**転記済**に変更された後、Field Service で行われた在庫調整と振替は Finance and Operations と同期します。</span><span class="sxs-lookup"><span data-stu-id="4baa8-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="4baa8-123">このような場合は、調整または移動オーダーがロックされ、読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="4baa8-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="4baa8-124">つまり、調整および転送は Finance and Operations に転記されますが、変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="4baa8-124">This means that adjustments and transfers can be posted in Finance and Operations, but cannot be modified.</span></span> <span data-ttu-id="4baa8-125">Finance and Operations では、調整を自動的に転記し、統合中に生成された在庫仕訳帳を振り替えるようにバッチ ジョブを設定できます。</span><span class="sxs-lookup"><span data-stu-id="4baa8-125">In Finance and Operations, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="4baa8-126">バッチ ジョブを有効にする方法の詳細については、以下の前提条件を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4baa8-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="4baa8-127">Field Service CRM ソリューション</span><span class="sxs-lookup"><span data-stu-id="4baa8-127">Field Service CRM solution</span></span> 
<span data-ttu-id="4baa8-128">**在庫単位**フィールドは、**製品**エンティティに追加されました。</span><span class="sxs-lookup"><span data-stu-id="4baa8-128">The **Inventory unit** field has been added to the **Product** entity.</span></span> <span data-ttu-id="4baa8-129">販売および在庫単位は Finance and Operations で常に同じであるとは限らないため、このフィールドは必要です。また倉庫在庫の Finance and Operations では、在庫単位が必要です。</span><span class="sxs-lookup"><span data-stu-id="4baa8-129">This field is needed because the Sales and Inventory unit is not always the same in Finance and Operations, and the Inventory Unit is needed for the Warehouse Inventory in Finance and Operations.</span></span>
<span data-ttu-id="4baa8-130">在庫調整と在庫振替の両方の在庫調整製品に製品を設定すると、在庫製品の値から単位がフェッチされます。</span><span class="sxs-lookup"><span data-stu-id="4baa8-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="4baa8-131">値が見つかると、在庫調整製品の**単位**フィールドがロックされます。</span><span class="sxs-lookup"><span data-stu-id="4baa8-131">If a value is found, the **Unit** field will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="4baa8-132">**在庫調整**のエンティティと**在庫振替**のエンティティの両方に、**転記ステータス** フィールドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="4baa8-132">The **Post status** field has been added to both the **Inventory adjustment** entity and the **Inventory transfer** entity.</span></span> <span data-ttu-id="4baa8-133">このフィールドは、調整または振替が Finance and Operations に送信されるときにフィルターとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="4baa8-133">This field is used as a filter when an adjustment or transfer is sent to Finance and Operations.</span></span> <span data-ttu-id="4baa8-134">このフィールドの既定値は作成 (1) ですが、Finance and Operations には送信されません。</span><span class="sxs-lookup"><span data-stu-id="4baa8-134">The default for this field is Created (1), however it is not sent to Finance and Operations.</span></span> <span data-ttu-id="4baa8-135">転記済 (2) の値を更新する場合、Finance and Operations に送信されますが、以降調整または振替を変更したり、新しい明細行を追加することはできなくなります。</span><span class="sxs-lookup"><span data-stu-id="4baa8-135">When you update the value to Posted (2), it is sent to Finance and Operations, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="4baa8-136">**番号順序**のフィールドは、**在庫調整製品**のエンティティに追加されました。</span><span class="sxs-lookup"><span data-stu-id="4baa8-136">The **Number sequence** field has been added to the **Inventory adjustment product** entity.</span></span> <span data-ttu-id="4baa8-137">このフィールドは、統合に固有の番号があり、統合が調整を作成および更新できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4baa8-137">This field ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="4baa8-138">最初の在庫調整製品を作成すると、**P2C 自動採番**エンティティに新しいレコードが作成され、番号シリーズと使用される接頭語が維持されます。</span><span class="sxs-lookup"><span data-stu-id="4baa8-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="4baa8-139">前提条件およびマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="4baa8-139">Prerequisites and mapping setup</span></span>

### <a name="finance-and-operations"></a><span data-ttu-id="4baa8-140">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4baa8-140">Finance and Operations</span></span>
<span data-ttu-id="4baa8-141">統合によって生成される統合在庫仕訳帳は、バッチ ジョブを使用して自動的に転記されます。</span><span class="sxs-lookup"><span data-stu-id="4baa8-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="4baa8-142">これは、**在庫管理 > 定期処理タスク > CDS 統合 > 統合在庫仕訳帳の転記**から有効になります。</span><span class="sxs-lookup"><span data-stu-id="4baa8-142">This is enabled from **Inventory management > Periodic tasks > CDS integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="4baa8-143">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="4baa8-143">Template mapping in Data integration</span></span>

<span data-ttu-id="4baa8-144">次の図は、データ統合のテンプレート マッピングを示しています。</span><span class="sxs-lookup"><span data-stu-id="4baa8-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-fin-and-ops-inventory-adjustment"></a><span data-ttu-id="4baa8-145">在庫調整 (Field Service から Fin and Ops): 在庫調整</span><span class="sxs-lookup"><span data-stu-id="4baa8-145">Inventory adjustment (Field Service to Fin and Ops): Inventory adjustment</span></span>

<span data-ttu-id="4baa8-146">[![データ統合のテンプレートのマッピング](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="4baa8-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-fin-and-ops-inventory-transfer"></a><span data-ttu-id="4baa8-147">在庫振替 (Field Service から Fin and Ops): 在庫振替</span><span class="sxs-lookup"><span data-stu-id="4baa8-147">Inventory transfer (Field Service to Fin and Ops): Inventory transfer</span></span>

<span data-ttu-id="4baa8-148">[![データ統合のテンプレートのマッピング](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="4baa8-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>
