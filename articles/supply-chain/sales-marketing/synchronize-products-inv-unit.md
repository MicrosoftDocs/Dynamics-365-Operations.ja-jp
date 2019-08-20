---
title: Finance and Operations から Field Service への製品と在庫単位の同期
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に製品と在庫単位を同期させるために使用されるテンプレートと基本的なタスクについて説明します。
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
ms.openlocfilehash: 78e8d8fa609b015cf2fceaf498279fe091325dbb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835697"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="af7ba-103">Finance and Operations から Field Service への製品在庫単位の同期</span><span class="sxs-lookup"><span data-stu-id="af7ba-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="af7ba-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に製品と在庫単位を同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="af7ba-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="af7ba-105">[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="af7ba-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="af7ba-106">使用された **Field Service 製品と在庫単位 (Finance and Operations から Field Service)** テンプレートは、**Field Service 製品 (Finance and Operations から Field Service)** テンプレートに基づきます。</span><span class="sxs-lookup"><span data-stu-id="af7ba-106">The used **Field Service Products with Inventory unit (Fin and Ops to Field Service)** template is based on the **Field Service Products (Fin and Ops to Field Service)** template.</span></span> <span data-ttu-id="af7ba-107">詳細については、[Field Service 製品 (Finance and Operations から Field Service)](field-service-product.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="af7ba-107">For more information, see [Field Service Products (Finance and Operations to Field Service)](field-service-product.md).</span></span>

<span data-ttu-id="af7ba-108">このトピックでは、2 つのテンプレートの相違のみについて説明します:</span><span class="sxs-lookup"><span data-stu-id="af7ba-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="af7ba-109">**在庫単位のある Field Service 製品 (Finance and Operations から Sales)**</span><span class="sxs-lookup"><span data-stu-id="af7ba-109">**Field Service Products with Inventory unit (Fin and Ops to Sales)**</span></span>
- <span data-ttu-id="af7ba-110">**Field Service 製品 (Finance and Operations から Field Service)**</span><span class="sxs-lookup"><span data-stu-id="af7ba-110">**Field Service Products (Fin and Ops to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="af7ba-111">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="af7ba-111">Templates and tasks</span></span>

<span data-ttu-id="af7ba-112">**データ統合でのテンプレートの名前:**</span><span class="sxs-lookup"><span data-stu-id="af7ba-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="af7ba-113">在庫単位のある Field Service 製品 (Finance and Operations から Sales)</span><span class="sxs-lookup"><span data-stu-id="af7ba-113">Field Service Products with Inventory unit (Fin and Ops to Sales)</span></span>

<span data-ttu-id="af7ba-114">**データ統合プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="af7ba-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="af7ba-115">製品</span><span class="sxs-lookup"><span data-stu-id="af7ba-115">Products</span></span>

<span data-ttu-id="af7ba-116">**Field Service 製品と在庫単位 (Finance and Operations から Field Service)** テンプレートには、**Field Service 製品 (Finance and Operations から Field Service)** テンプレートに含まれていないマッピングが 1 つ含まれます。</span><span class="sxs-lookup"><span data-stu-id="af7ba-116">The **Field Service Products with Inventory unit (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Fin and Ops to Field Service)** template.</span></span> <span data-ttu-id="af7ba-117">このマッピングにより、在庫レベルの同期に必要な在庫単位が含まれていることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="af7ba-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="af7ba-118">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="af7ba-118">Template mapping in Data integration</span></span>

<span data-ttu-id="af7ba-119">次の図は、データ統合のテンプレート マッピングを示しています。</span><span class="sxs-lookup"><span data-stu-id="af7ba-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-fin-and-ops-to-field-service-products"></a><span data-ttu-id="af7ba-120">Field Service 製品と在庫単位 (Finance and Operations から Field Service): 製品</span><span class="sxs-lookup"><span data-stu-id="af7ba-120">Field Service Products with Inventory unit (Fin and Ops to Field Service): Products</span></span>

<span data-ttu-id="af7ba-121">[![データ統合のテンプレートのマッピング](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="af7ba-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
