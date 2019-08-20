---
title: Finance and Operations から Field Service への倉庫の同期
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に倉庫を同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: ae99624076eecda2969961d0361d1adf42c6c5f3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835673"
---
# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="ff70c-103">Finance and Operations から Field Service への倉庫の同期</span><span class="sxs-lookup"><span data-stu-id="ff70c-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ff70c-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に倉庫を同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ff70c-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="ff70c-105">[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="ff70c-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="ff70c-106">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="ff70c-106">Templates and tasks</span></span>
<span data-ttu-id="ff70c-107">次のテンプレートと基本的なタスクは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に倉庫の同期を実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ff70c-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="ff70c-108">**データ統合でのテンプレート**</span><span class="sxs-lookup"><span data-stu-id="ff70c-108">**Template in Data integration**</span></span>
- <span data-ttu-id="ff70c-109">倉庫 (Finance and Operations から Field Service)</span><span class="sxs-lookup"><span data-stu-id="ff70c-109">Warehouses (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="ff70c-110">**データ統合プロジェクトのタスク**</span><span class="sxs-lookup"><span data-stu-id="ff70c-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="ff70c-111">倉庫</span><span class="sxs-lookup"><span data-stu-id="ff70c-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="ff70c-112">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="ff70c-112">Entity set</span></span>
| <span data-ttu-id="ff70c-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="ff70c-113">Field Service</span></span>    | <span data-ttu-id="ff70c-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ff70c-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="ff70c-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="ff70c-115">msdyn_warehouses</span></span> | <span data-ttu-id="ff70c-116">倉庫</span><span class="sxs-lookup"><span data-stu-id="ff70c-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="ff70c-117">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="ff70c-117">Entity flow</span></span>
<span data-ttu-id="ff70c-118">Finance and Operations で作成および管理されている倉庫は、Common Data Service (CDS) データの統合プロジェクトを通して Field Service に同期することができます。</span><span class="sxs-lookup"><span data-stu-id="ff70c-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="ff70c-119">Field Service に同期する倉庫は、プロジェクトの高度なクエリおよびフィルター処理で制御することができます。</span><span class="sxs-lookup"><span data-stu-id="ff70c-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="ff70c-120">Finance and Operations から同期する倉庫は Field Service で作成され、**外部で管理**フィールドを**はい**に設定することにより、レコードは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="ff70c-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the **Is maintained externally** field set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="ff70c-121">Field Service CRM ソリューション</span><span class="sxs-lookup"><span data-stu-id="ff70c-121">Field Service CRM solution</span></span>
<span data-ttu-id="ff70c-122">Field Service および Finance and Operations の統合をサポートするために、Field Service CRM からの追加機能が必要です。</span><span class="sxs-lookup"><span data-stu-id="ff70c-122">To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="ff70c-123">ソリューションとして、**外部で管理**フィールドが、**倉庫 (msdyn_warehouses)** エンティティに追加されました。</span><span class="sxs-lookup"><span data-stu-id="ff70c-123">In the solution, the **Is Maintained Externally** field has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="ff70c-124">このフィールドは、倉庫が Finance and Operations から処理されているのか、または Field Service にのみ存在するのかを識別するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="ff70c-124">This field helps to identify if the warehouse is handled from Finance and Operations or if it only exists in Field Service.</span></span> <span data-ttu-id="ff70c-125">このフィールドの設定は以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ff70c-125">The settings for this field include:</span></span>
- <span data-ttu-id="ff70c-126">**はい** – 倉庫は Finance and Operations に由来し、Sales では編集できません。</span><span class="sxs-lookup"><span data-stu-id="ff70c-126">**Yes** – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="ff70c-127">**いいえ** – 倉庫は Field Service で直接入力されており、ここで管理されます。</span><span class="sxs-lookup"><span data-stu-id="ff70c-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="ff70c-128">**外部で管理**フィールドは、在庫レベル、調整、移動およびワーク オーダーの使用状況の同期を制御します。</span><span class="sxs-lookup"><span data-stu-id="ff70c-128">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="ff70c-129">**外部で管理**が**はい**に設定された倉庫のみ、その他のシステムの同じ倉庫に直接同期するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="ff70c-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="ff70c-130">Field Service で複数の倉庫を作成し (**外部で管理** = いいえ)、Finance and Operations で高度なクエリおよびフィルター処理を使用して 1 つの倉庫にマッピングすることができます。</span><span class="sxs-lookup"><span data-stu-id="ff70c-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="ff70c-131">これは、Field service に詳細な在庫レベルを習得させ、Finance and Operations に更新を送信するだけの場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="ff70c-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="ff70c-132">この場合、Field service は、Finance and Operations からの在庫レベルの更新は受信しません。</span><span class="sxs-lookup"><span data-stu-id="ff70c-132">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="ff70c-133">追加情報については、「[Field Service から Finance and Operations への在庫調整の同期](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments)」および「[Field Service でのワーク オーダーを Finance and Operations のプロジェクトにリンクされている販売注文に同期](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ff70c-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="ff70c-134">前提条件およびマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="ff70c-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="ff70c-135">データ統合プロジェクト</span><span class="sxs-lookup"><span data-stu-id="ff70c-135">Data Integration project</span></span>
<span data-ttu-id="ff70c-136">倉庫を同期する前に、プロジェクト上で高度なクエリおよびフィルタリング処理を更新し、Finance and Operations から Field Service へ移動させる倉庫のみが含まれていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ff70c-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="ff70c-137">Field Service の倉庫をワーク オーダー、調整、および移動に適用する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ff70c-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="ff70c-138">**統合キー**が **msdyn_warehouses** に存在することを確認するには:</span><span class="sxs-lookup"><span data-stu-id="ff70c-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="ff70c-139">データ統合に移動します。</span><span class="sxs-lookup"><span data-stu-id="ff70c-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="ff70c-140">**接続設定**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="ff70c-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="ff70c-141">ワーク オーダー同期に使用される接続設定を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff70c-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="ff70c-142">**統合キー** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="ff70c-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="ff70c-143">Msdyn_warehouses を検索し、キーの **msdyn_name (名前)** が追加されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ff70c-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="ff70c-144">表示されていない場合は、**キーの追加**をクリックして追加してから、ページの上部にある**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ff70c-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ff70c-145">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="ff70c-145">Template mapping in Data integration</span></span>

<span data-ttu-id="ff70c-146">次の図は、データ統合のテンプレート マッピングを示します。</span><span class="sxs-lookup"><span data-stu-id="ff70c-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-fin-and-ops-to-field-service-warehouse"></a><span data-ttu-id="ff70c-147">倉庫 (Finance and Operations から Field Service): 倉庫</span><span class="sxs-lookup"><span data-stu-id="ff70c-147">Warehouses (Fin and Ops to Field Service): Warehouse</span></span>

<span data-ttu-id="ff70c-148">[![データ統合のテンプレートのマッピング](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="ff70c-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>
