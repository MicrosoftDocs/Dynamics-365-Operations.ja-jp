---
title: Field Service から Finance and Operations へのワーク オーダーとプロジェクトの同期
description: このトピックでは、Microsoft Dynamics 365 for Field Service から Microsoft Dynamics 365 for Finance and Operations にワーク オーダーとプロジェクト番号を同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 6b61411a5a235e2d0aad8bb25ae4a3bfcf1248d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "329853"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="460c2-103">Field Service から Finance and Operations へのワーク オーダーとプロジェクトの同期</span><span class="sxs-lookup"><span data-stu-id="460c2-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="460c2-104">このトピックでは、Microsoft Dynamics 365 for Field Service から Microsoft Dynamics 365 for Finance and Operations にワーク オーダーとプロジェクト番号を同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="460c2-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="460c2-105">[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="460c2-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="460c2-106">使用されている **Field Service 製品 (Finance and Operations から Field Service)** テンプレートは、見込顧客を現金化の**製品 (Finance and Operations から Sales) – 直接**テンプレートに基づいています。</span><span class="sxs-lookup"><span data-stu-id="460c2-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="460c2-107">詳細については、[製品 (Finance and Operations から Sales) - 直接](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="460c2-107">For more information, see [Products (Finance and Operations to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="460c2-108">このトピックでは、**Field Service 製品 (Finance and Operations から Field Service)** および **Field Service 製品 (Finance and Operations から Field Service)** テンプレートの間の違いのみを説明します。</span><span class="sxs-lookup"><span data-stu-id="460c2-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

<span data-ttu-id="460c2-109">主な違いは、このテンプレートには Field Service のワーク オーダーに割り当てられたプロジェクト番号のマッピングが含まれており、Finance and Operations で作成された販売注文にプロジェクト番号が含まれ、関連付けられているプロジェクトの請求が確実に行われるようにしていることです。</span><span class="sxs-lookup"><span data-stu-id="460c2-109">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="460c2-110">これに加え、テンプレートは高度なクエリおよびフィルター処理を使用します。</span><span class="sxs-lookup"><span data-stu-id="460c2-110">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="460c2-111">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="460c2-111">Templates and tasks</span></span>

<span data-ttu-id="460c2-112">**データ統合でのテンプレートの名前:**</span><span class="sxs-lookup"><span data-stu-id="460c2-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="460c2-113">ワーク オーダーとプロジェクト (Field Service から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="460c2-113">Work Orders with Project (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="460c2-114">**データ統合プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="460c2-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="460c2-115">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="460c2-115">WorkOrderHeader</span></span>
- <span data-ttu-id="460c2-116">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="460c2-116">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="460c2-117">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="460c2-117">WorkOrderProduct</span></span>
- <span data-ttu-id="460c2-118">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="460c2-118">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="460c2-119">Field Service CRM ソリューション</span><span class="sxs-lookup"><span data-stu-id="460c2-119">Field Service CRM solution</span></span>
<span data-ttu-id="460c2-120">**外部プロジェクト** フィールドが、ワーク オーダー エンティティに追加されました。</span><span class="sxs-lookup"><span data-stu-id="460c2-120">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="460c2-121">このフィールドはルックアップで、ワーク オーダーとプロジェクトのタグ付けを購入し、それから販売注文は Finance and Operations によりプロジェクトに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="460c2-121">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="460c2-122">**システム ステータス**がオープンから変わった場合 - 上位のステータスへの Progress(690,970,000) で、**外部プロジェクト** フィールドはロックされ、値の追加、削除、また変更はできなくなります。</span><span class="sxs-lookup"><span data-stu-id="460c2-122">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="460c2-123">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="460c2-123">Template mapping in Data integration</span></span>

<span data-ttu-id="460c2-124">次の図は、データ統合のテンプレート マッピングを示しています。</span><span class="sxs-lookup"><span data-stu-id="460c2-124">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a><span data-ttu-id="460c2-125">ワーク オーダーとプロジェクト (Field Service から Finance and Operations): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="460c2-125">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeader</span></span>

<span data-ttu-id="460c2-126">[![データ統合のテンプレートのマッピング](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="460c2-126">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a><span data-ttu-id="460c2-127">ワーク オーダーとプロジェクト (Field Service から Finance and Operations): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="460c2-127">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeaderProject</span></span>

<span data-ttu-id="460c2-128">[![データ統合のテンプレートのマッピング](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="460c2-128">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a><span data-ttu-id="460c2-129">ワーク オーダーとプロジェクト (Field Service から Finance and Operations): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="460c2-129">Work Orders with Project (Field Service to Finance and Operations): WorkOrderProduct</span></span>

<span data-ttu-id="460c2-130">[![データ統合のテンプレートのマッピング](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="460c2-130">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a><span data-ttu-id="460c2-131">ワーク オーダーとプロジェクト (Field Service から Finance and Operations): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="460c2-131">Work Orders with Project (Field Service to Finance and Operations): WorkOrderService</span></span>

<span data-ttu-id="460c2-132">[![データ統合のテンプレートのマッピング](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="460c2-132">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
