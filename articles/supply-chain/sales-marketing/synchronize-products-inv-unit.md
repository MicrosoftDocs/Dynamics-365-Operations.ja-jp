---
title: Supply Chain Management から Field Service へ在庫単位のある製品の同期
description: このトピックでは、Dynamics 365 Supply Chain Management から Dynamics 365 Field Service に製品と在庫単位を同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 3485e4f284218924cee01e45d5248f5af1a64010
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215956"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a><span data-ttu-id="31693-103">Supply Chain Management から Field Service へ在庫単位のある製品の同期</span><span class="sxs-lookup"><span data-stu-id="31693-103">Synchronize products with inventory unit from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="31693-104">このトピックでは、Dynamics 365 Supply Chain Management から Dynamics 365 Field Service に製品と在庫単位を同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="31693-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="31693-105">[![Supply Chain Management および Field Service 間の業務プロセスの同期](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="31693-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="31693-106">使用された **Field Service 製品と在庫単位 (Supply Chain Management から Field Service)** テンプレートは、**Field Service 製品 (Supply Chain Management から Field Service)** テンプレートに基づきます。</span><span class="sxs-lookup"><span data-stu-id="31693-106">The used **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template is based on the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="31693-107">詳細については、[Supply Chain Management の製品と Field Service の製品との同期](field-service-product.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="31693-107">For more information, see [Synchronize products in Supply Chain Management to products in Field Service](field-service-product.md).</span></span>

<span data-ttu-id="31693-108">このトピックでは、2 つのテンプレートの相違のみについて説明します:</span><span class="sxs-lookup"><span data-stu-id="31693-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="31693-109">**在庫単位のある Field Service 製品 (Supply Chain Management から Sales)**</span><span class="sxs-lookup"><span data-stu-id="31693-109">**Field Service Products with Inventory unit (Supply Chain Management to Sales)**</span></span>
- <span data-ttu-id="31693-110">**Field Service 製品 (Supply Chain Management から Field Service)**</span><span class="sxs-lookup"><span data-stu-id="31693-110">**Field Service Products (Supply Chain Management to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="31693-111">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="31693-111">Templates and tasks</span></span>

<span data-ttu-id="31693-112">**データ統合でのテンプレートの名前:**</span><span class="sxs-lookup"><span data-stu-id="31693-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="31693-113">在庫単位のある Field Service 製品 (Supply Chain Management から Sales)</span><span class="sxs-lookup"><span data-stu-id="31693-113">Field Service Products with Inventory unit (Supply Chain Management to Sales)</span></span>

<span data-ttu-id="31693-114">**データ統合プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="31693-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="31693-115">製品</span><span class="sxs-lookup"><span data-stu-id="31693-115">Products</span></span>

<span data-ttu-id="31693-116">**在庫単位のある Field Service 製品 (Supply Chain Management から Field Service)** テンプレートには、**Field Service 製品 (Supply Chain Management から Field Service)** テンプレートに含まれていないマッピングが 1 つ含まれます。</span><span class="sxs-lookup"><span data-stu-id="31693-116">The **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Supply Chain Managementto Field Service)** template.</span></span> <span data-ttu-id="31693-117">このマッピングにより、在庫レベルの同期に必要な在庫単位が含まれていることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="31693-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```Text
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="31693-118">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="31693-118">Template mapping in Data integration</span></span>

<span data-ttu-id="31693-119">次の図は、データ統合のテンプレート マッピングを示しています。</span><span class="sxs-lookup"><span data-stu-id="31693-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a><span data-ttu-id="31693-120">在庫単位のある Field Service 製品 (Supply Chain Management から Field Service): 製品</span><span class="sxs-lookup"><span data-stu-id="31693-120">Field Service Products with Inventory unit (Supply Chain Management to Field Service): Products</span></span>

<span data-ttu-id="31693-121">[![データ統合のテンプレートのマッピング](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="31693-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
