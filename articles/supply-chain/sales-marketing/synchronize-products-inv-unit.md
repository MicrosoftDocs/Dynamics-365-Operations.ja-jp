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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: c5be622d6f62d54bcec053b93700ce0c234b8308
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010900"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a>Supply Chain Management から Field Service へ在庫単位のある製品の同期

[!include[banner](../includes/banner.md)]

このトピックでは、Dynamics 365 Supply Chain Management から Dynamics 365 Field Service に製品と在庫単位を同期させるために使用されるテンプレートと基本的なタスクについて説明します。

[![Supply Chain Management および Field Service 間の業務プロセスの同期](./media/FSProductsOW.png)](./media/FSProductsOW.png)

使用された **Field Service 製品と在庫単位 (Supply Chain Management から Field Service)** テンプレートは、**Field Service 製品 (Supply Chain Management から Field Service)** テンプレートに基づきます。 詳細については、[Supply Chain Management の製品と Field Service の製品との同期](field-service-product.md) を参照してください。

このトピックでは、2 つのテンプレートの相違のみについて説明します: 
- **在庫単位のある Field Service 製品 (Supply Chain Management から Sales)**
- **Field Service 製品 (Supply Chain Management から Field Service)** 

## <a name="templates-and-tasks"></a>テンプレートおよびタスク

**データ統合でのテンプレートの名前:**

- 在庫単位のある Field Service 製品 (Supply Chain Management から Sales)

**データ統合プロジェクトのタスク名:**

- 製品

**在庫単位のある Field Service 製品 (Supply Chain Management から Field Service)** テンプレートには、**Field Service 製品 (Supply Chain Management から Field Service)** テンプレートに含まれていないマッピングが 1 つ含まれます。 このマッピングにより、在庫レベルの同期に必要な在庫単位が含まれていることが保証されます。

```plaintext
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ統合のテンプレート マッピングを示しています。

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a>在庫単位のある Field Service 製品 (Supply Chain Management から Field Service): 製品

[![データ統合のテンプレートのマッピング](./media/FSProduct1.png)](./media/FSProduct1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]