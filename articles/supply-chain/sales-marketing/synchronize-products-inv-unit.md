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
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>Finance and Operations から Field Service への製品在庫単位の同期

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に製品と在庫単位を同期させるために使用されるテンプレートと基本的なタスクについて説明します。

[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSProductsOW.png)](./media/FSProductsOW.png)

使用されている **Field Service 製品 (Finance and Operations から Field Service)** テンプレートは、見込顧客を現金化の**製品 (Finance and Operations から Sales) – 直接**テンプレートに基づいています。 詳細については、[製品 (Finance and Operations から Sales) - 直接](products-template-mapping-direct.md) を参照してください。

このトピックでは、**Field Service 製品 (Finance and Operations から Field Service)** および **Field Service 製品 (Finance and Operations から Field Service)** テンプレートの間の違いのみを説明します。

## <a name="templates-and-tasks"></a>テンプレートおよびタスク

**データ統合でのテンプレートの名前:**

- 在庫単位のある Field Service 製品 (Finance and Operations から 販売)

**データ統合プロジェクトのタスク名:**

- 製品

**Field Service 製品と在庫単位 (Finance and Operations から Field Service)** テンプレートには、**Field Service 製品 (Finance and Operations から Field Service)** テンプレートに含まれていないマッピングが 1 つ含まれます。 このマッピングにより、在庫レベルの同期に必要な在庫単位が含まれていることが保証されます。

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ統合のテンプレート マッピングを示しています。

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a>Field Service 製品と在庫単位 (Finance and Operations から Field Service): 製品

[![データ統合のテンプレートのマッピング](./media/FSProduct1.png)](./media/FSProduct1.png)
