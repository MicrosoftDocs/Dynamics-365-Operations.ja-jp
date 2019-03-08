---
title: Finance and Operations から Field Service への製品と在庫単位の同期
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に製品と在庫単位を同期させるために使用されるテンプレートと基本的なタスクについて説明します。
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
ms.openlocfilehash: 5d3767c1a499f3d888d8fc2ce06c2837442e39f0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "359247"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="be917-103">Finance and Operations から Field Service への製品在庫単位の同期</span><span class="sxs-lookup"><span data-stu-id="be917-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="be917-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に製品と在庫単位を同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="be917-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="be917-105">[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="be917-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="be917-106">使用されている **Field Service 製品 (Finance and Operations から Field Service)** テンプレートは、見込顧客を現金化の**製品 (Finance and Operations から Sales) – 直接**テンプレートに基づいています。</span><span class="sxs-lookup"><span data-stu-id="be917-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="be917-107">詳細については、[製品 (Finance and Operations から Sales) - 直接](products-template-mapping-direct.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be917-107">For more information, see [Products (Finance and Operations to Sales) – Direct](products-template-mapping-direct.md).</span></span>

<span data-ttu-id="be917-108">このトピックでは、**Field Service 製品 (Finance and Operations から Field Service)** および **Field Service 製品 (Finance and Operations から Field Service)** テンプレートの間の違いのみを説明します。</span><span class="sxs-lookup"><span data-stu-id="be917-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="be917-109">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="be917-109">Templates and tasks</span></span>

<span data-ttu-id="be917-110">**データ統合でのテンプレートの名前:**</span><span class="sxs-lookup"><span data-stu-id="be917-110">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="be917-111">在庫単位のある Field Service 製品 (Finance and Operations から 販売)</span><span class="sxs-lookup"><span data-stu-id="be917-111">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span>

<span data-ttu-id="be917-112">**データ統合プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="be917-112">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="be917-113">製品</span><span class="sxs-lookup"><span data-stu-id="be917-113">Products</span></span>

<span data-ttu-id="be917-114">**Field Service 製品と在庫単位 (Finance and Operations から Field Service)** テンプレートには、**Field Service 製品 (Finance and Operations から Field Service)** テンプレートに含まれていないマッピングが 1 つ含まれます。</span><span class="sxs-lookup"><span data-stu-id="be917-114">The **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="be917-115">このマッピングにより、在庫レベルの同期に必要な在庫単位が含まれていることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="be917-115">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="be917-116">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="be917-116">Template mapping in Data integration</span></span>

<span data-ttu-id="be917-117">次の図は、データ統合のテンプレート マッピングを示しています。</span><span class="sxs-lookup"><span data-stu-id="be917-117">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a><span data-ttu-id="be917-118">Field Service 製品と在庫単位 (Finance and Operations から Field Service): 製品</span><span class="sxs-lookup"><span data-stu-id="be917-118">Field Service Products with Inventory unit (Finance and Operations to Field Service): Products</span></span>

<span data-ttu-id="be917-119">[![データ統合のテンプレートのマッピング](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="be917-119">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
