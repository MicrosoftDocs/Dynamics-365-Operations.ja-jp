---
title: Supply Chain Management の製品と Field Service の製品との同期
description: このトピックでは、Dynamics 365 Supply Chain Management から Dynamics 365 Field Service に製品を同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
ms.date: 04/09/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 45a989604d829db715756b6cd206a5675a18acf2
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909994"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a><span data-ttu-id="0e6f9-103">Supply Chain Management の製品と Field Service の製品との同期</span><span class="sxs-lookup"><span data-stu-id="0e6f9-103">Synchronize products in Supply Chain Management to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0e6f9-104">このトピックでは、Dynamics 365 Supply Chain Management から Dynamics 365 Field Service に製品を同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="0e6f9-104">This topic discusses the templates and underlying task that are used to synchronize products from Dynamics 365 Supply Chain Management to Dynamics 365  Field Service.</span></span>

<span data-ttu-id="0e6f9-105">使用されている **Field Service 製品 (Supply Chain Management から Field Service)** テンプレートは、見込顧客を現金化の **製品 (Supply Chain Management から Sales) – 直接** テンプレートに基づきます。</span><span class="sxs-lookup"><span data-stu-id="0e6f9-105">The used **Field Service Products (Supply Chain Management to Field Service)** template is based on the **Products (Supply Chain Management to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="0e6f9-106">詳細については、[製品 (Supply Chain Management から Sales) - 直接](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e6f9-106">For more information, see [Products (Supply Chain Management to Sales) – Direct](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="0e6f9-107">このトピックでは、**Field Service 製品 (Supply Chain Management から Field Service)** および **製品 (Supply Chain Management から Sales) – 直接** テンプレートの間の違いのみを説明します。</span><span class="sxs-lookup"><span data-stu-id="0e6f9-107">This topic only describes the differences between the **Field Service Products (Supply Chain Management to Field Service)** and **Products (Supply Chain Management to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="0e6f9-108">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="0e6f9-108">Templates and tasks</span></span>

<span data-ttu-id="0e6f9-109">**データ統合でのテンプレートの名前**</span><span class="sxs-lookup"><span data-stu-id="0e6f9-109">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="0e6f9-110">Field Service 製品 (Supply Chain Management から Field Service)</span><span class="sxs-lookup"><span data-stu-id="0e6f9-110">Field Service Products (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="0e6f9-111">**データ統合プロジェクトのタスク名**</span><span class="sxs-lookup"><span data-stu-id="0e6f9-111">**Name of the task in the Data integration project**</span></span>

- <span data-ttu-id="0e6f9-112">製品 - 製品</span><span class="sxs-lookup"><span data-stu-id="0e6f9-112">Products - Products</span></span>

<span data-ttu-id="0e6f9-113">**Field Service 製品 (Supply Chain Management から Field Service)** テンプレートは、**製品 (Supply Chain Management から Sales) – 直接** テンプレートに含まれていないマッピングに基づきます。</span><span class="sxs-lookup"><span data-stu-id="0e6f9-113">The **Field Service Products (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Products (Supply Chain Management to Sales) – Direct** template.</span></span> <span data-ttu-id="0e6f9-114">このマッピングは、必要な Field Service 固有のフィールド **サービス製品タイプ** が正しく設定されるようにします。</span><span class="sxs-lookup"><span data-stu-id="0e6f9-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="0e6f9-115">次の値マッピングが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0e6f9-115">The following value mapping is used.</span></span>

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="0e6f9-116">Supply Chain Management で、**販売可能なリリース済製品** データ エンティティ上の **Field Service 製品タイプ** の値は次のように計算されます。</span><span class="sxs-lookup"><span data-stu-id="0e6f9-116">In Supply Chain Management, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="0e6f9-117">**在庫:** 製品タイプ = 製品および品目モデル グループ、在庫製品 = True</span><span class="sxs-lookup"><span data-stu-id="0e6f9-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="0e6f9-118">**在庫なし:** 製品タイプ = 製品および品目モデル グループ、在庫製品 = False</span><span class="sxs-lookup"><span data-stu-id="0e6f9-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="0e6f9-119">**サービス:** 製品タイプ = サービス</span><span class="sxs-lookup"><span data-stu-id="0e6f9-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="0e6f9-120">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="0e6f9-120">Template mapping in Data integration</span></span>

<span data-ttu-id="0e6f9-121">次の図は、データ統合のテンプレート マッピングを示しています。</span><span class="sxs-lookup"><span data-stu-id="0e6f9-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a><span data-ttu-id="0e6f9-122">Field Service 製品 (Supply Chain Management から Field Service) : 製品 - 製品</span><span class="sxs-lookup"><span data-stu-id="0e6f9-122">Field Service Products (Supply Chain Management to Field Service): Products - Products</span></span>

<span data-ttu-id="0e6f9-123">[![データ統合のテンプレートのマッピング](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="0e6f9-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]