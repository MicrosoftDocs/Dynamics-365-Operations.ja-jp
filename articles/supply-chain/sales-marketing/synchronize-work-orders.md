---
title: "Finance and Operations から Field Service へのワーク オーダーの同期"
description: "このトピックでは、Microsoft Dynamics 365 for Field Service から Microsoft Dynamics 365 for Finance and Operations にワーク オーダーとプロジェクト番号を同期させるために使用するテンプレートと基本的なタスクについて説明します。"
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
ms.openlocfilehash: f5bd6b8c554688d0d1b2bfd93a34a60a95412bf3
ms.contentlocale: ja-jp
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="81560-103">Field Service から Finance and Operations へのワーク オーダーとプロジェクトの同期</span><span class="sxs-lookup"><span data-stu-id="81560-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="81560-104">このトピックでは、Microsoft Dynamics 365 for Field Service から Microsoft Dynamics 365 for Finance and Operations にワーク オーダーとプロジェクト番号を同期させるために使用するテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="81560-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="81560-105">[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="81560-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="81560-106">使用されている **Field Service 製品 (Finance and Operations から Field Service)** テンプレートは、見込顧客を現金化の**製品 (Finance and Operations から Sales) – 直接**テンプレートに基づいています。</span><span class="sxs-lookup"><span data-stu-id="81560-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="81560-107">詳細については、[製品 (Finance and Operations から Sales) - 直接](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="81560-107">For more information, see [Products (Finance and Operations to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="81560-108">このトピックでは、**Field Service 製品 (Finance and Operations から Field Service)** および **Field Service 製品 (Finance and Operations から Field Service)** テンプレートの間の違いのみを説明します。</span><span class="sxs-lookup"><span data-stu-id="81560-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

<span data-ttu-id="81560-109">主な違いは、このテンプレートには Field Service のワーク オーダーに割り当てられたプロジェクト番号のマッピングが含まれており、Finance and Operations で作成された販売注文にプロジェクト番号が含まれ、関連付けられているプロジェクトの請求が確実に行われるようにしていることです。</span><span class="sxs-lookup"><span data-stu-id="81560-109">The main difference is that this template include mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="81560-110">これに加え、テンプレートは高度なクエリおよびフィルター処理を使用します。</span><span class="sxs-lookup"><span data-stu-id="81560-110">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="81560-111">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="81560-111">Templates and tasks</span></span>

<span data-ttu-id="81560-112">**データ統合でのテンプレートの名前:**</span><span class="sxs-lookup"><span data-stu-id="81560-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="81560-113">ワーク オーダーとプロジェクト (Field Service から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="81560-113">Work Orders with Project (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="81560-114">**データ統合プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="81560-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="81560-115">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="81560-115">WorkOrderHeader</span></span>
- <span data-ttu-id="81560-116">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="81560-116">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="81560-117">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="81560-117">WorkOrderProduct</span></span>
- <span data-ttu-id="81560-118">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="81560-118">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="81560-119">Field Service CRM ソリューション</span><span class="sxs-lookup"><span data-stu-id="81560-119">Field Service CRM solution</span></span>
<span data-ttu-id="81560-120">**外部プロジェクト** フィールドが、ワーク オーダー エンティティに追加されました。</span><span class="sxs-lookup"><span data-stu-id="81560-120">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="81560-121">このフィールドはルックアップで、ワーク オーダーとプロジェクトのタグ付けを購入し、それから販売注文は Finance and Operations によりプロジェクトに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="81560-121">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="81560-122">**システム ステータス**がオープンから変わった場合 - 上位のステータスへの Progress(690,970,000) で、**外部プロジェクト** フィールドはロックされ、値の追加、削除、また変更はできなくなります。</span><span class="sxs-lookup"><span data-stu-id="81560-122">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="81560-123">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="81560-123">Template mapping in Data integration</span></span>

<span data-ttu-id="81560-124">次の図は、データ統合のテンプレート マッピングを示しています。</span><span class="sxs-lookup"><span data-stu-id="81560-124">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a><span data-ttu-id="81560-125">ワーク オーダーとプロジェクト (Field Service から Finance and Operations): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="81560-125">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeader</span></span>

<span data-ttu-id="81560-126">[![データ統合のテンプレートのマッピング](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="81560-126">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a><span data-ttu-id="81560-127">ワーク オーダーとプロジェクト (Field Service から Finance and Operations): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="81560-127">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeaderProject</span></span>

<span data-ttu-id="81560-128">[![データ統合のテンプレートのマッピング](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="81560-128">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a><span data-ttu-id="81560-129">ワーク オーダーとプロジェクト (Field Service から Finance and Operations): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="81560-129">Work Orders with Project (Field Service to Finance and Operations): WorkOrderProduct</span></span>

<span data-ttu-id="81560-130">[![データ統合のテンプレートのマッピング](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="81560-130">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a><span data-ttu-id="81560-131">ワーク オーダーとプロジェクト (Field Service から Finance and Operations): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="81560-131">Work Orders with Project (Field Service to Finance and Operations): WorkOrderService</span></span>

<span data-ttu-id="81560-132">[![データ統合のテンプレートのマッピング](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="81560-132">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>

