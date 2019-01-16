---
title: "Field Service から Finance and Operations への在庫振替と調整の同期"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に在庫調整と振替を同期させるために使用されるテンプレートと基本的なタスクについて説明します。"
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: ja-jp
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>Field Service から Finance and Operations への在庫調整の同期

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に在庫調整と振替を同期させるために使用されるテンプレートと基本的なタスクについて説明します。

[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>テンプレートおよびタスク
次のテンプレートと基本的なタスクは、Microsoft Dynamics 365 for Field Service から Microsoft Dynamics 365 for Finance and Operations への在庫調整と振替の同期を実行するために使用されます。

**データ統合におけるテンプレートの名前:**
- 在庫調整 (Field Service から Finance and Operations)
- 在庫振替 (Field Service から Finance and Operations)

**データ統合プロジェクトのタスク名:**
- 在庫調整
- 在庫振替

## <a name="entity-set"></a>エンティティ セット
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   CDS 在庫調整仕訳帳のヘッダーおよび明細行 |
| msdyn_inventoryadjustmentproducts | CDS 在庫移動仕訳帳のヘッダーおよび明細行   |

## <a name="entity-flow"></a>エンティティのフロー
**ステータスを転記**が作成済から転記済に変更されると、Field Service で行われた在庫調整と振替は Finance and Operations と同期します。 これが発生すると、調整および振替は Finance and Operations に転記される可能性があり、調整および振替のオーダーがロックされ読み取り専用になるため、変更することができません。
Finance and Operations では、調整を自動的に転記し、統合によって生成された在庫仕訳帳を振り替えるようにバッチ ジョブを設定できます。 バッチ ジョブを有効にする方法の詳細については、以下の前提条件を参照してください。

## <a name="field-service-crm-solution"></a>Field Service CRM ソリューション 
在庫単位のフィールドは、製品のエンティティに追加されました。 販売および在庫単位は工程で常に同じであるとは限らないため、このフィールドは必要です。また倉庫在庫の工程では、在庫単位が必要です。
在庫調整と在庫振替の両方の在庫調整製品に製品を設定すると、製品在庫製品の値から単位がフェッチされます。 値が見つかると、在庫調整製品の単位フィールドがロックされます。

在庫調整のエンティティと、在庫振替のエンティティの両方に、転記ステータス フィールドが追加されました。 このフィールドは、調整または振替が工程に送信されるときにフィルターとして使用されます。 このフィールドは、既定で作成 (1) に設定されており、工程には送信されません。 変更したものは転記済 (2) になり工程に送信されますが、以降調整または振替で何かを変更したり、新しい明細行を追加することはできなくなります。
番号順序のフィールドは、在庫調整製品のエンティティに追加されました。 このフィールドは、統合が一意の番号を持つのに役立ちます。そのため、統合がいつ作成を行い、いつ更新を行うかを認識します。 最初の在庫調整製品を作成すると、P2C 自動採番エンティティに新しいレコードが作成され、番号シリーズと使用される接頭語が維持されます。

## <a name="prerequisites-and-mapping-setup"></a>前提条件およびマッピングの設定

### <a name="in-finance-and-operations"></a>Finance and Operations
統合によって生成される統合在庫仕訳帳は、バッチ ジョブに自動的に転記されます。 これは、次で有効になります: 在庫管理 > 定期処理タスク > CDS 統合 > 統合在庫仕訳帳の転記

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ統合のテンプレート マッピングを示しています。

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a>在庫調整 (Field Service から Finance and Operations): 在庫調整

[![データ統合のテンプレートのマッピング](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a>在庫振替 (Field Service から Finance and Operations): 在庫振替

[![データ統合のテンプレートのマッピング](./media/FSTrans1.png)](./media/FSTrans1.png)

