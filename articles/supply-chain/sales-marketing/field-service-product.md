---
title: "Field Service 製品への Finance and Operations の製品の同期"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に製品を同期させるために使用されるテンプレートと基本的なタスクについて説明します。"
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: ace66c037953f4b1b2e8b93a315faefdb090b1eb
ms.openlocfilehash: bf5de13fee6db1b467c1cf4d5cc65b46c67b29fe
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a><span data-ttu-id="64c94-103">Field Service 製品への Finance and Operations の製品の同期</span><span class="sxs-lookup"><span data-stu-id="64c94-103">Synchronize products in Finance and Operations to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="64c94-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に製品を同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="64c94-104">This topic discusses the templates and underlying task that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="64c94-105">使用されている **Field Service 製品 (Finance and Operations から Field Service)** テンプレートは、見込顧客を現金化の**製品 (Finance and Operations から Sales) – 直接**テンプレートに基づきます。</span><span class="sxs-lookup"><span data-stu-id="64c94-105">The used **Field Service Products (Fin and Ops to Field Service)** template is based on the **Products (Fin and Ops to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="64c94-106">詳細については、次を参照してください [製品 (Finance and Operations から Sales) - 直接](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct)。</span><span class="sxs-lookup"><span data-stu-id="64c94-106">For more information, see [Products (Fin and Ops to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="64c94-107">このトピックでは、**Field Service 製品 (Finance and Operations から Field Service)** および**製品 (Finance and Operations から Sales) – 直接**テンプレートの間の違いのみを説明します。</span><span class="sxs-lookup"><span data-stu-id="64c94-107">This topic only describes the differences between the **Field Service Products (Fin and Ops to Field Service)** and **Products (Fin and Ops to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="64c94-108">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="64c94-108">Templates and tasks</span></span>

<span data-ttu-id="64c94-109">**データ統合でのテンプレートの名前:**</span><span class="sxs-lookup"><span data-stu-id="64c94-109">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="64c94-110">Field Service 製品 (Finance and Operations から Field Service)</span><span class="sxs-lookup"><span data-stu-id="64c94-110">Field Service Products (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="64c94-111">**データ統合プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="64c94-111">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="64c94-112">製品 - 製品</span><span class="sxs-lookup"><span data-stu-id="64c94-112">Products - Products</span></span>

<span data-ttu-id="64c94-113">**Field Service 製品 (Finance and Operations から Field Service)** テンプレートは、**製品 (Finance and Operations から Sales) – 直接**テンプレートに含まれていないマッピングを含んでいます。</span><span class="sxs-lookup"><span data-stu-id="64c94-113">The **Field Service Products (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Products (Fin and Ops to Sales) – Direct** template.</span></span> <span data-ttu-id="64c94-114">このマッピングは、必要な Field Service 固有のフィールド **サービス製品タイプ** が正しく設定されるようにします。</span><span class="sxs-lookup"><span data-stu-id="64c94-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="64c94-115">次の値マッピングが使用されます。</span><span class="sxs-lookup"><span data-stu-id="64c94-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="64c94-116">Finance and Operations で、**販売可能なリリース済製品**データ エンティティ上の **Field Service 製品タイプ**の値は次のように計算されます。</span><span class="sxs-lookup"><span data-stu-id="64c94-116">In Finance and Operations, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="64c94-117">**在庫:** 製品タイプ = 製品および品目モデル グループ、在庫製品 = True</span><span class="sxs-lookup"><span data-stu-id="64c94-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="64c94-118">**在庫なし:** 製品タイプ = 製品および品目モデル グループ、在庫製品 = False</span><span class="sxs-lookup"><span data-stu-id="64c94-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="64c94-119">**サービス:** 製品タイプ = サービス</span><span class="sxs-lookup"><span data-stu-id="64c94-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="64c94-120">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="64c94-120">Template mapping in Data integration</span></span>

<span data-ttu-id="64c94-121">次の図は、データ統合のテンプレート マッピングを示しています。</span><span class="sxs-lookup"><span data-stu-id="64c94-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a><span data-ttu-id="64c94-122">Field Service 製品 (Finance and Operations から Field Service): 製品 - 製品</span><span class="sxs-lookup"><span data-stu-id="64c94-122">Field Service Products (Fin and Ops to Field Service): Products - Products</span></span>

<span data-ttu-id="64c94-123">[![データ統合のテンプレートのマッピング](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="64c94-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>

