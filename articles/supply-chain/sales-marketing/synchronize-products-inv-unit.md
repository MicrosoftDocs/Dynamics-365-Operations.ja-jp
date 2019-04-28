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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 080672b9a6acd9fd6137580b5b7e14d12cfccf19
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/14/2019
ms.locfileid: "842465"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>Finance and Operations から Field Service への製品在庫単位の同期

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に製品と在庫単位を同期させるために使用されるテンプレートと基本的なタスクについて説明します。

[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSProductsOW.png)](./media/FSProductsOW.png)

使用された **Field Service 製品と在庫単位 (Finance and Operations から Field Service)** テンプレートは、**Field Service 製品 (Finance and Operations から Field Service)** テンプレートに基づきます。 詳細については、[Field Service 製品 (Finance and Operations から Field Service)](field-service-product.md) を参照してください。

このトピックでは、2 つのテンプレートの相違のみについて説明します: 
- **在庫単位のある Field Service 製品 (Finance and Operations から Sales)**
- **Field Service 製品 (Finance and Operations から Field Service)** 

## <a name="templates-and-tasks"></a>テンプレートおよびタスク

**データ統合でのテンプレートの名前:**

- 在庫単位のある Field Service 製品 (Finance and Operations から Sales)

**データ統合プロジェクトのタスク名:**

- 製品

**Field Service 製品と在庫単位 (Finance and Operations から Field Service)** テンプレートには、**Field Service 製品 (Finance and Operations から Field Service)** テンプレートに含まれていないマッピングが 1 つ含まれます。 このマッピングにより、在庫レベルの同期に必要な在庫単位が含まれていることが保証されます。

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ統合のテンプレート マッピングを示しています。

### <a name="field-service-products-with-inventory-unit-fin-and-ops-to-field-service-products"></a>Field Service 製品と在庫単位 (Finance and Operations から Field Service): 製品

[![データ統合のテンプレートのマッピング](./media/FSProduct1.png)](./media/FSProduct1.png)
