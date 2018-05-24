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

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a>Field Service 製品への Finance and Operations の製品の同期

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に製品を同期させるために使用されるテンプレートと基本的なタスクについて説明します。

使用されている **Field Service 製品 (Finance and Operations から Field Service)** テンプレートは、見込顧客を現金化の**製品 (Finance and Operations から Sales) – 直接**テンプレートに基づきます。 詳細については、次を参照してください [製品 (Finance and Operations から Sales) - 直接](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct)。

このトピックでは、**Field Service 製品 (Finance and Operations から Field Service)** および**製品 (Finance and Operations から Sales) – 直接**テンプレートの間の違いのみを説明します。

## <a name="templates-and-tasks"></a>テンプレートおよびタスク

**データ統合でのテンプレートの名前:**

- Field Service 製品 (Finance and Operations から Field Service)

**データ統合プロジェクトのタスク名:**

- 製品 - 製品

**Field Service 製品 (Finance and Operations から Field Service)** テンプレートは、**製品 (Finance and Operations から Sales) – 直接**テンプレートに含まれていないマッピングを含んでいます。 このマッピングは、必要な Field Service 固有のフィールド **サービス製品タイプ** が正しく設定されるようにします。

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

次の値マッピングが使用されます。

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

Finance and Operations で、**販売可能なリリース済製品**データ エンティティ上の **Field Service 製品タイプ**の値は次のように計算されます。

- **在庫:** 製品タイプ = 製品および品目モデル グループ、在庫製品 = True
- **在庫なし:** 製品タイプ = 製品および品目モデル グループ、在庫製品 = False
- **サービス:** 製品タイプ = サービス

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ統合のテンプレート マッピングを示しています。

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a>Field Service 製品 (Finance and Operations から Field Service): 製品 - 製品

[![データ統合のテンプレートのマッピング](./media/FSProduct.png)](./media/FSProduct.png)

