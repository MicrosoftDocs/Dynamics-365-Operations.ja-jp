---
title: Field Service から Finance and Operations へのワーク オーダーとプロジェクトの同期
description: このトピックでは、Microsoft Dynamics 365 for Field Service から Microsoft Dynamics 365 for Finance and Operations にワーク オーダーとプロジェクト番号を同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 5ca01b085315d916a18c512af28fc7534ce76ee8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1536736"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="d2856-103">Field Service から Finance and Operations へのワーク オーダーとプロジェクトの同期</span><span class="sxs-lookup"><span data-stu-id="d2856-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d2856-104">このトピックでは、Microsoft Dynamics 365 for Field Service から Microsoft Dynamics 365 for Finance and Operations にワーク オーダーとプロジェクト番号を同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d2856-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="d2856-105">[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="d2856-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="d2856-106">使用されている**ワーク オーダーとプロジェクト (Field Service から Finance and Operations)** テンプレートは、**ワーク オーダー (Field Service から Finance and Operations)** テンプレートに基づきます。</span><span class="sxs-lookup"><span data-stu-id="d2856-106">The used **Work Orders with Project (Field Service to Fin and Ops)** template is based on the **Work Orders (Field Service to Fin and Ops)** template.</span></span> <span data-ttu-id="d2856-107">詳細については、[Field Service のワーク オーダーと Finance and Operations の販売注文との同期](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2856-107">For more information, see [Synchronize work orders in Field Service to sales orders in Finance and Operations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="d2856-108">このトピックでは、2 つのテンプレートの相違のみについて説明します:</span><span class="sxs-lookup"><span data-stu-id="d2856-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="d2856-109">**ワーク オーダーとプロジェクト (Field Service から Finance and Operations)**</span><span class="sxs-lookup"><span data-stu-id="d2856-109">**Work Orders with Project (Field Service to Fin and Ops)**</span></span>
- <span data-ttu-id="d2856-110">**ワーク オーダー (Field Service から Finance and Operations)**</span><span class="sxs-lookup"><span data-stu-id="d2856-110">**Work Orders (Field Service to Fin and Ops)**</span></span>

<span data-ttu-id="d2856-111">主な違いは、このテンプレートには Field Service のワーク オーダーに割り当てられたプロジェクト番号のマッピングが含まれており、Finance and Operations で作成された販売注文にプロジェクト番号が含まれ、関連付けられているプロジェクトの請求が確実に行われるようにしていることです。</span><span class="sxs-lookup"><span data-stu-id="d2856-111">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="d2856-112">これに加え、テンプレートは高度なクエリおよびフィルター処理を使用します。</span><span class="sxs-lookup"><span data-stu-id="d2856-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="d2856-113">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="d2856-113">Templates and tasks</span></span>

<span data-ttu-id="d2856-114">**データ統合でのテンプレートの名前:**</span><span class="sxs-lookup"><span data-stu-id="d2856-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="d2856-115">ワーク オーダーとプロジェクト (Field Service から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="d2856-115">Work Orders with Project (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="d2856-116">**データ統合プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="d2856-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="d2856-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="d2856-117">WorkOrderHeader</span></span>
- <span data-ttu-id="d2856-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="d2856-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="d2856-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="d2856-119">WorkOrderProduct</span></span>
- <span data-ttu-id="d2856-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="d2856-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="d2856-121">Field Service CRM ソリューション</span><span class="sxs-lookup"><span data-stu-id="d2856-121">Field Service CRM solution</span></span>
<span data-ttu-id="d2856-122">**外部プロジェクト** フィールドが、ワーク オーダー エンティティに追加されました。</span><span class="sxs-lookup"><span data-stu-id="d2856-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="d2856-123">このフィールドはルックアップで、ワーク オーダーとプロジェクトのタグ付けを購入し、それから販売注文は Finance and Operations によりプロジェクトに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="d2856-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="d2856-124">**システム ステータス**がオープンから変わった場合 - 上位のステータスへの Progress(690,970,000) で、**外部プロジェクト** フィールドはロックされ、値の追加、削除、また変更はできなくなります。</span><span class="sxs-lookup"><span data-stu-id="d2856-124">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="d2856-125">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="d2856-125">Template mapping in Data integration</span></span>

<span data-ttu-id="d2856-126">次の図は、データ統合のテンプレート マッピングを示しています。</span><span class="sxs-lookup"><span data-stu-id="d2856-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a><span data-ttu-id="d2856-127">ワーク オーダーとプロジェクト (Field Service から Finance and Operations): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="d2856-127">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeader</span></span>

<span data-ttu-id="d2856-128">[![データ統合のテンプレートのマッピング](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="d2856-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a><span data-ttu-id="d2856-129">ワーク オーダーとプロジェクト (Field Service から Finance and Operations): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="d2856-129">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeaderProject</span></span>

<span data-ttu-id="d2856-130">[![データ統合のテンプレートのマッピング](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="d2856-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a><span data-ttu-id="d2856-131">ワーク オーダーとプロジェクト (Field Service から Finance and Operations): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="d2856-131">Work Orders with Project (Field Service to Fin and Ops): WorkOrderProduct</span></span>

<span data-ttu-id="d2856-132">[![データ統合のテンプレートのマッピング](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="d2856-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a><span data-ttu-id="d2856-133">ワーク オーダーとプロジェクト (Field Service から Finance and Operations): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="d2856-133">Work Orders with Project (Field Service to Fin and Ops): WorkOrderService</span></span>

<span data-ttu-id="d2856-134">[![データ統合のテンプレートのマッピング](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="d2856-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
