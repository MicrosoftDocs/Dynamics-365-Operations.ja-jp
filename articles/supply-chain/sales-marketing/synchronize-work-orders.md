---
title: Field Service から Supply Chain Management へのプロジェクトの作業指示書の同期
description: このトピックでは、Dynamics 365 Field Service から Dynamics 365 Supply Chain Management にワーク オーダーとプロジェクト番号を同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
ms.date: 03/12/2019
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
ms.openlocfilehash: d733bf3256fa1f6c572bd0aa35c228490d409bbc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836497"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a><span data-ttu-id="10a1f-103">Field Service から Supply Chain Management へのプロジェクトの作業指示書の同期</span><span class="sxs-lookup"><span data-stu-id="10a1f-103">Synchronize work orders with project from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="10a1f-104">このトピックでは、Dynamics 365 Field Service から Dynamics 365 Supply Chain Management にワーク オーダーとプロジェクト番号を同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="10a1f-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Dynamics 365 Field Service to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="10a1f-105">[![Supply Chain Management および Field Service 間の業務プロセスの同期](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="10a1f-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="10a1f-106">使用されている **ワーク オーダーとプロジェクト (Field Service から Supply Chain Management)** テンプレートは、**ワーク オーダー (Field Service から Supply Chain Management)** テンプレートに基づきます。</span><span class="sxs-lookup"><span data-stu-id="10a1f-106">The used **Work Orders with Project (Field Service to Supply Chain Management)** template is based on the **Work Orders (Field Service to Supply Chain Management)** template.</span></span> <span data-ttu-id="10a1f-107">詳細については、[Field Service のワーク オーダーと Supply Chain Management の販売注文との同期](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="10a1f-107">For more information, see [Synchronize work orders in Field Service to sales orders in Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="10a1f-108">このトピックでは、2 つのテンプレートの相違のみについて説明します:</span><span class="sxs-lookup"><span data-stu-id="10a1f-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="10a1f-109">**ワーク オーダーとプロジェクト (Field Service から Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="10a1f-109">**Work Orders with Project (Field Service to Supply Chain Management)**</span></span>
- <span data-ttu-id="10a1f-110">**ワーク オーダー (Field Service から Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="10a1f-110">**Work Orders (Field Service to Supply Chain Management)**</span></span>

<span data-ttu-id="10a1f-111">主な違いは、このテンプレートには Field Service のワーク オーダーに割り当てられたプロジェクト番号のマッピングが含まれており、Supply Chain Management で作成された販売注文にはプロジェクト番号が含まれ、関連付けられているプロジェクトの請求が確実に行われるようにしていることです。</span><span class="sxs-lookup"><span data-stu-id="10a1f-111">The main difference is that this template includes mapping of the project number assigned to the Work order in Field Service, ensuring that the Sales order created in Supply Chain Management include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="10a1f-112">これに加え、テンプレートは高度なクエリおよびフィルター処理を使用します。</span><span class="sxs-lookup"><span data-stu-id="10a1f-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="10a1f-113">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="10a1f-113">Templates and tasks</span></span>

<span data-ttu-id="10a1f-114">**データ統合でのテンプレートの名前:**</span><span class="sxs-lookup"><span data-stu-id="10a1f-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="10a1f-115">ワーク オーダーとプロジェクト (Field Service から Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="10a1f-115">Work Orders with Project (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="10a1f-116">**データ統合プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="10a1f-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="10a1f-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="10a1f-117">WorkOrderHeader</span></span>
- <span data-ttu-id="10a1f-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="10a1f-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="10a1f-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="10a1f-119">WorkOrderProduct</span></span>
- <span data-ttu-id="10a1f-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="10a1f-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="10a1f-121">Field Service CRM ソリューション</span><span class="sxs-lookup"><span data-stu-id="10a1f-121">Field Service CRM solution</span></span>
<span data-ttu-id="10a1f-122">**外部プロジェクト** フィールドが、ワーク オーダー エンティティに追加されました。</span><span class="sxs-lookup"><span data-stu-id="10a1f-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="10a1f-123">このフィールドはルックアップで、ワーク オーダーがプロジェクトにタグ付けられ、販売注文は Supply Chain Management 内のプロジェクトに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="10a1f-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Supply Chain Management.</span></span> <span data-ttu-id="10a1f-124">**システム ステータス** がオープン – 処理中 (690,970,000) から上位のステータスへ変わった場合、**外部プロジェクト** フィールドはロックされ、値の追加、削除、また変更はできなくなります。</span><span class="sxs-lookup"><span data-stu-id="10a1f-124">When the **System Status** changes from Open – In Progress(690,970,000) to a higher status, the **External Project** field will be locked and you can't add, remove, or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="10a1f-125">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="10a1f-125">Template mapping in Data integration</span></span>

<span data-ttu-id="10a1f-126">次の図は、データ統合のテンプレート マッピングを示しています。</span><span class="sxs-lookup"><span data-stu-id="10a1f-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a><span data-ttu-id="10a1f-127">ワーク オーダーとプロジェクト (Field Service から Supply Chain Management): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="10a1f-127">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeader</span></span>

<span data-ttu-id="10a1f-128">[![データ統合のテンプレートのマッピング](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="10a1f-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a><span data-ttu-id="10a1f-129">ワーク オーダーとプロジェクト (Field Service から Supply Chain Management): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="10a1f-129">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeaderProject</span></span>

<span data-ttu-id="10a1f-130">[![データ統合のテンプレートのマッピング](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="10a1f-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a><span data-ttu-id="10a1f-131">ワーク オーダーとプロジェクト (Field Service から Supply Chain Management): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="10a1f-131">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderProduct</span></span>

<span data-ttu-id="10a1f-132">[![データ統合のテンプレートのマッピング](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="10a1f-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a><span data-ttu-id="10a1f-133">ワーク オーダーとプロジェクト (Field Service から Supply Chain Management): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="10a1f-133">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderService</span></span>

<span data-ttu-id="10a1f-134">[![データ統合のテンプレートのマッピング](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="10a1f-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]