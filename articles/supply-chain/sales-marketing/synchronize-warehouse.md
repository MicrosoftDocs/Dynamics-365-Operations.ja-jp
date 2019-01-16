---
title: "Finance and Operations から Field Service への倉庫の同期"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に倉庫を同期させるために使用されるテンプレートと基本的なタスクについて説明します。"
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
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
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: ja-jp
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="be552-103">Finance and Operations から Field Service への倉庫の同期</span><span class="sxs-lookup"><span data-stu-id="be552-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="be552-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に倉庫を同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="be552-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="be552-105">[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="be552-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="be552-106">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="be552-106">Templates and tasks</span></span>
<span data-ttu-id="be552-107">次のテンプレートおよび基本的なタスクは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に倉庫の同期を実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="be552-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="be552-108">**データ統合でのテンプレートの名前:**</span><span class="sxs-lookup"><span data-stu-id="be552-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="be552-109">倉庫 (Finance and Operations から Field Service)</span><span class="sxs-lookup"><span data-stu-id="be552-109">Warehouses (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="be552-110">**データ統合プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="be552-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="be552-111">倉庫</span><span class="sxs-lookup"><span data-stu-id="be552-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="be552-112">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="be552-112">Entity set</span></span>
| <span data-ttu-id="be552-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="be552-113">Field Service</span></span>    | <span data-ttu-id="be552-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="be552-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="be552-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="be552-115">msdyn_warehouses</span></span> | <span data-ttu-id="be552-116">倉庫</span><span class="sxs-lookup"><span data-stu-id="be552-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="be552-117">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="be552-117">Entity flow</span></span>
<span data-ttu-id="be552-118">Finance and Operations で作成および管理されている倉庫は、Common Data Service (CDS) データの統合プロジェクトを通して Field Service に同期することができます。</span><span class="sxs-lookup"><span data-stu-id="be552-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="be552-119">Field Service に同期することが必要な倉庫は、プロジェクトの高度なクエリおよびフィルター処理で制御することができます。</span><span class="sxs-lookup"><span data-stu-id="be552-119">The desired warehouses that synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="be552-120">Finance and Operations から同期する倉庫は Field Service で作成され、外部で管理フィールドをはいに設定することにより、レコードは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="be552-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the field Is maintained externally set to Yes and the record is made read only.</span></span>
<span data-ttu-id="be552-121">Field Service CRM ソリューション Field Service および Finance and Operations の統合をサポートするために、Field Service CRM からの追加機能が必要です。</span><span class="sxs-lookup"><span data-stu-id="be552-121">Field Service CRM solution To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="be552-122">ソリューションには、次の変更が含まれます。</span><span class="sxs-lookup"><span data-stu-id="be552-122">The solution includes the following changes.</span></span>
<span data-ttu-id="be552-123">**外部で管理**フィールドが、**倉庫 (msdyn_warehouses)** エンティティに追加されました。</span><span class="sxs-lookup"><span data-stu-id="be552-123">The field **Is Maintained Externally** has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="be552-124">このフィールドは、倉庫が Operations から処理されているのか、または Field Service にのみ存在するのかを識別するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="be552-124">This field helps to identify If the Warehouse is handled from Operations or if It only exists in Field Service.</span></span>
- <span data-ttu-id="be552-125">はい – 倉庫は Finance and Operations に由来し、Sales では編集できません。</span><span class="sxs-lookup"><span data-stu-id="be552-125">Yes – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="be552-126">いいえ – 倉庫は Field Service で直接入力されており、ここで管理されます。</span><span class="sxs-lookup"><span data-stu-id="be552-126">No – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="be552-127">**外部で管理**フィールドは、在庫レベル、調整、移動およびワーク オーダーの使用状況の同期を制御します。</span><span class="sxs-lookup"><span data-stu-id="be552-127">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers and usage on work orders.</span></span> <span data-ttu-id="be552-128">**外部で管理** = はいの倉庫のみ、その他のシステムの同じ倉庫に直接同期するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="be552-128">Only warehouses with **Is Externally Maintained** = Yes can be used to synchronize directly to the same warehouse in the other system.</span></span> 

<span data-ttu-id="be552-129">注記: Field Services で複数の倉庫を作成し (**外部で管理** = いいえの場合)、Finance and Operations で高度なクエリおよびフィルター処理を使用して 1 つの倉庫にマッピングすることができます。</span><span class="sxs-lookup"><span data-stu-id="be552-129">Note: It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="be552-130">これは、Field service に詳細な在庫レベルを習得させ、Finance and Operations に更新を送信するだけの場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="be552-130">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="be552-131">この場合、Field service は、Finance and Operations からの在庫レベルの更新は受信しません。</span><span class="sxs-lookup"><span data-stu-id="be552-131">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="be552-132">追加情報については、Field Service から Finance and Operations への在庫調整の同期、および Field Service でのワーク オーダーを Finance and Operations のプロジェクトにリンクされている販売注文に同期、を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be552-132">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="be552-133">前提条件およびマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="be552-133">Prerequisites and mapping setup</span></span>
### <a name="in-the-data-integration-project"></a><span data-ttu-id="be552-134">データ統合プロジェクト内</span><span class="sxs-lookup"><span data-stu-id="be552-134">In the Data Integration project</span></span>
<span data-ttu-id="be552-135">倉庫の同期の前に、プロジェクト上で高度なクエリおよびフィルタリング処理を更新し、Finance and Operations から Field Service へ移動させる倉庫のみが含まれていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="be552-135">Before synchronization of the warehouses make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="be552-136">Field Service の倉庫をワーク オーダー、調整、および移動に適用する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="be552-136">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments and transfers.</span></span>  

<span data-ttu-id="be552-137">**統合キー**が **msdyn_warehouses** に存在することを確認</span><span class="sxs-lookup"><span data-stu-id="be552-137">Ensure the **Integration key** exist for **msdyn_warehouses**</span></span>
1. <span data-ttu-id="be552-138">データ統合に移動</span><span class="sxs-lookup"><span data-stu-id="be552-138">Go to Data Integration</span></span>
2. <span data-ttu-id="be552-139">**接続設定**タブを選択</span><span class="sxs-lookup"><span data-stu-id="be552-139">Select **Connection Set** tab</span></span>
3. <span data-ttu-id="be552-140">ワーク オーダー同期に使用される接続設定を選択します。</span><span class="sxs-lookup"><span data-stu-id="be552-140">Select the Connection set used for Work order synchronization</span></span>
4. <span data-ttu-id="be552-141">**統合キー**タブを選択</span><span class="sxs-lookup"><span data-stu-id="be552-141">Select **Integration key** tab</span></span>
5. <span data-ttu-id="be552-142">Msdyn_warehouses を検索し、キーの **msdyn_name (名前)** が追加されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="be552-142">Find msdyn_warehouses and check that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="be552-143">表示されていない場合は、**キーの追加**をクリックして追加し、ページの上部にある**保存**をクリックします</span><span class="sxs-lookup"><span data-stu-id="be552-143">If it is not shown, add it by click **Add key** and click **Save** in the top of the page</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="be552-144">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="be552-144">Template mapping in Data integration</span></span>

<span data-ttu-id="be552-145">次の図は、データ統合のテンプレート マッピングを示しています。</span><span class="sxs-lookup"><span data-stu-id="be552-145">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a><span data-ttu-id="be552-146">倉庫 (Finance and Operations から Field Service): 倉庫</span><span class="sxs-lookup"><span data-stu-id="be552-146">Warehouses (Finance and Operations to Field Service): Warehouse</span></span>

<span data-ttu-id="be552-147">[![データ統合のテンプレートのマッピング](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="be552-147">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>

