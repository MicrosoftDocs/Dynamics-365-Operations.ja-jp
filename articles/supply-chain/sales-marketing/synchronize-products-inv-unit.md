---
title: Supply Chain Management から Field Service へ在庫単位のある製品の同期
description: この記事では、Dynamics 365 Supply Chain Management から Dynamics 365 Field Service に製品と在庫単位を同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: Henrikan
ms.date: 03/13/2019
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
ms.author: henrikan
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5f7658eacd20aa69a64d6288e9d29e53b6ccb002
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887257"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a>Supply Chain Management から Field Service へ在庫単位のある製品の同期

[!include[banner](../includes/banner.md)]

この記事では、Dynamics 365 Supply Chain Management から Dynamics 365 Field Service に製品と在庫単位を同期させるために使用されるテンプレートと基本的なタスクについて説明します。

[![Supply Chain Management および Field Service 間の業務プロセスの同期。](./media/FSProductsOW.png)](./media/FSProductsOW.png)

使用された **Field Service 製品と在庫単位 (Supply Chain Management から Field Service)** テンプレートは、**Field Service 製品 (Supply Chain Management から Field Service)** テンプレートに基づきます。 詳細については、[Supply Chain Management の製品と Field Service の製品との同期](field-service-product.md) を参照してください。

この記事では、2 つのテンプレートの相違のみについて説明します: 
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

[![データ統合のテンプレートのマッピング。](./media/FSProduct1.png)](./media/FSProduct1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]