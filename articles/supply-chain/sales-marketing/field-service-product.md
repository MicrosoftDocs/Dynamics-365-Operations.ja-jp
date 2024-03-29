---
title: Supply Chain Management の製品と Field Service の製品との同期
description: この記事では、Dynamics 365 Supply Chain Management から Dynamics 365 Field Service に製品を同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: Henrikan
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
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 114550f01f3aed197480fb6830fe913dbfa7b570
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860554"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a>Supply Chain Management の製品と Field Service の製品との同期

[!include[banner](../includes/banner.md)]

この記事では、Dynamics 365 Supply Chain Management から Dynamics 365 Field Service に製品を同期させるために使用されるテンプレートと基本的なタスクについて説明します。

使用されている **Field Service 製品 (Supply Chain Management から Field Service)** テンプレートは、見込顧客を現金化の **製品 (Supply Chain Management から Sales) – 直接** テンプレートに基づきます。 詳細については、[製品 (Supply Chain Management から Sales) - 直接](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct) を参照してください。

この記事では、**Field Service 製品 (Supply Chain Management から Field Service)** および **製品 (Supply Chain Management から Sales) – 直接** のテンプレート間の違いのみを説明します。

## <a name="templates-and-tasks"></a>テンプレートおよびタスク

**データ統合でのテンプレートの名前**

- Field Service 製品 (Supply Chain Management から Field Service)

**データ統合プロジェクトのタスク名**

- 製品 - 製品

**Field Service 製品 (Supply Chain Management から Field Service)** テンプレートは、**製品 (Supply Chain Management から Sales) – 直接** テンプレートに含まれていないマッピングに基づきます。 このマッピングは、必要な Field Service 固有のフィールド **サービス製品タイプ** が正しく設定されるようにします。

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

次の値マッピングが使用されます。

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

Supply Chain Management で、**販売可能なリリース済製品** データ エンティティ上の **Field Service 製品タイプ** の値は次のように計算されます。

- **在庫:** 製品タイプ = 製品および品目モデル グループ、在庫製品 = True
- **在庫なし:** 製品タイプ = 製品および品目モデル グループ、在庫製品 = False
- **サービス:** 製品タイプ = サービス

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ統合のテンプレート マッピングを示しています。

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a>Field Service 製品 (Supply Chain Management から Field Service) : 製品 - 製品

[![データ統合のテンプレートのマッピング。](./media/FSProduct.png)](./media/FSProduct.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]