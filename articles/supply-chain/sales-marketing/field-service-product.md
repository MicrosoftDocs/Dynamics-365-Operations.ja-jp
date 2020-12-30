---
title: Supply Chain Management の製品と Field Service の製品との同期
description: このトピックでは、Dynamics 365 Supply Chain Management から Dynamics 365 Field Service に製品を同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
manager: tfehr
ms.date: 04/09/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: d96d1cd91bad4f950868074d9558cb403821d73f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432125"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a><span data-ttu-id="58ff4-103">Supply Chain Management の製品と Field Service の製品との同期</span><span class="sxs-lookup"><span data-stu-id="58ff4-103">Synchronize products in Supply Chain Management to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="58ff4-104">このトピックでは、Dynamics 365 Supply Chain Management から Dynamics 365 Field Service に製品を同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="58ff4-104">This topic discusses the templates and underlying task that are used to synchronize products from Dynamics 365 Supply Chain Management to Dynamics 365  Field Service.</span></span>

<span data-ttu-id="58ff4-105">使用されている **Field Service 製品 (Supply Chain Management から Field Service)** テンプレートは、見込顧客を現金化の **製品 (Supply Chain Management から Sales) – 直接** テンプレートに基づきます。</span><span class="sxs-lookup"><span data-stu-id="58ff4-105">The used **Field Service Products (Supply Chain Management to Field Service)** template is based on the **Products (Supply Chain Management to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="58ff4-106">詳細については、[製品 (Supply Chain Management から Sales) - 直接](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="58ff4-106">For more information, see [Products (Supply Chain Management to Sales) – Direct](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="58ff4-107">このトピックでは、**Field Service 製品 (Supply Chain Management から Field Service)** および **製品 (Supply Chain Management から Sales) – 直接** テンプレートの間の違いのみを説明します。</span><span class="sxs-lookup"><span data-stu-id="58ff4-107">This topic only describes the differences between the **Field Service Products (Supply Chain Management to Field Service)** and **Products (Supply Chain Management to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="58ff4-108">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="58ff4-108">Templates and tasks</span></span>

<span data-ttu-id="58ff4-109">**データ統合でのテンプレートの名前**</span><span class="sxs-lookup"><span data-stu-id="58ff4-109">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="58ff4-110">Field Service 製品 (Supply Chain Management から Field Service)</span><span class="sxs-lookup"><span data-stu-id="58ff4-110">Field Service Products (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="58ff4-111">**データ統合プロジェクトのタスク名**</span><span class="sxs-lookup"><span data-stu-id="58ff4-111">**Name of the task in the Data integration project**</span></span>

- <span data-ttu-id="58ff4-112">製品 - 製品</span><span class="sxs-lookup"><span data-stu-id="58ff4-112">Products - Products</span></span>

<span data-ttu-id="58ff4-113">**Field Service 製品 (Supply Chain Management から Field Service)** テンプレートは、**製品 (Supply Chain Management から Sales) – 直接** テンプレートに含まれていないマッピングに基づきます。</span><span class="sxs-lookup"><span data-stu-id="58ff4-113">The **Field Service Products (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Products (Supply Chain Management to Sales) – Direct** template.</span></span> <span data-ttu-id="58ff4-114">このマッピングは、必要な Field Service 固有のフィールド **サービス製品タイプ** が正しく設定されるようにします。</span><span class="sxs-lookup"><span data-stu-id="58ff4-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="58ff4-115">次の値マッピングが使用されます。</span><span class="sxs-lookup"><span data-stu-id="58ff4-115">The following value mapping is used.</span></span>

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="58ff4-116">Supply Chain Management で、**販売可能なリリース済製品** データ エンティティ上の **Field Service 製品タイプ** の値は次のように計算されます。</span><span class="sxs-lookup"><span data-stu-id="58ff4-116">In Supply Chain Management, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="58ff4-117">**在庫:** 製品タイプ = 製品および品目モデル グループ、在庫製品 = True</span><span class="sxs-lookup"><span data-stu-id="58ff4-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="58ff4-118">**在庫なし:** 製品タイプ = 製品および品目モデル グループ、在庫製品 = False</span><span class="sxs-lookup"><span data-stu-id="58ff4-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="58ff4-119">**サービス:** 製品タイプ = サービス</span><span class="sxs-lookup"><span data-stu-id="58ff4-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="58ff4-120">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="58ff4-120">Template mapping in Data integration</span></span>

<span data-ttu-id="58ff4-121">次の図は、データ統合のテンプレート マッピングを示しています。</span><span class="sxs-lookup"><span data-stu-id="58ff4-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a><span data-ttu-id="58ff4-122">Field Service 製品 (Supply Chain Management から Field Service) : 製品 - 製品</span><span class="sxs-lookup"><span data-stu-id="58ff4-122">Field Service Products (Supply Chain Management to Field Service): Products - Products</span></span>

<span data-ttu-id="58ff4-123">[![データ統合のテンプレートのマッピング](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="58ff4-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>
