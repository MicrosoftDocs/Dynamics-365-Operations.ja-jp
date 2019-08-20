---
title: Field Service から Finance and Operations への在庫振替と調整の同期
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に在庫調整と振替を同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 145c9c06635aa6518fd1f76324a8bd6e4cc07d16
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835721"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>Field Service から Finance and Operations への在庫調整の同期

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に在庫調整と振替を同期させるために使用されるテンプレートと基本的なタスクについて説明します。

[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>テンプレートおよびタスク
次のテンプレートと基本的なタスクは、Microsoft Dynamics 365 for Field Service から Microsoft Dynamics 365 for Finance and Operations への在庫調整と振替の同期を実行するために使用されます。

**データ統合でのテンプレート**
- 在庫調整 (Field Service から Fin and Ops)
- 在庫振替 (Field Service から Fin and Ops)

**データ統合プロジェクトのタスク:**
- 在庫調整
- 在庫振替

## <a name="entity-set"></a>エンティティ セット
| Field Service                     | Finance and Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   CDS 在庫調整仕訳帳のヘッダーおよび明細行 |
| msdyn_inventoryadjustmentproducts | CDS 在庫移動仕訳帳のヘッダーおよび明細行   |

## <a name="entity-flow"></a>エンティティのフロー
**ステータスを転記**が**作成済**から**転記済**に変更された後、Field Service で行われた在庫調整と振替は Finance and Operations と同期します。 このような場合は、調整または移動オーダーがロックされ、読み取り専用になります。 つまり、調整および転送は Finance and Operations に転記されますが、変更することはできません。 Finance and Operations では、調整を自動的に転記し、統合中に生成された在庫仕訳帳を振り替えるようにバッチ ジョブを設定できます。 バッチ ジョブを有効にする方法の詳細については、以下の前提条件を参照してください。

## <a name="field-service-crm-solution"></a>Field Service CRM ソリューション 
**在庫単位**フィールドは、**製品**エンティティに追加されました。 販売および在庫単位は Finance and Operations で常に同じであるとは限らないため、このフィールドは必要です。また倉庫在庫の Finance and Operations では、在庫単位が必要です。
在庫調整と在庫振替の両方の在庫調整製品に製品を設定すると、在庫製品の値から単位がフェッチされます。 値が見つかると、在庫調整製品の**単位**フィールドがロックされます。

**在庫調整**のエンティティと**在庫振替**のエンティティの両方に、**転記ステータス** フィールドが追加されました。 このフィールドは、調整または振替が Finance and Operations に送信されるときにフィルターとして使用されます。 このフィールドの既定値は作成 (1) ですが、Finance and Operations には送信されません。 転記済 (2) の値を更新する場合、Finance and Operations に送信されますが、以降調整または振替を変更したり、新しい明細行を追加することはできなくなります。

**番号順序**のフィールドは、**在庫調整製品**のエンティティに追加されました。 このフィールドは、統合に固有の番号があり、統合が調整を作成および更新できることを確認します。 最初の在庫調整製品を作成すると、**P2C 自動採番**エンティティに新しいレコードが作成され、番号シリーズと使用される接頭語が維持されます。

## <a name="prerequisites-and-mapping-setup"></a>前提条件およびマッピングの設定

### <a name="finance-and-operations"></a>Finance and Operations
統合によって生成される統合在庫仕訳帳は、バッチ ジョブを使用して自動的に転記されます。 これは、**在庫管理 > 定期処理タスク > CDS 統合 > 統合在庫仕訳帳の転記**から有効になります。

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ統合のテンプレート マッピングを示しています。

### <a name="inventory-adjustment-field-service-to-fin-and-ops-inventory-adjustment"></a>在庫調整 (Field Service から Fin and Ops): 在庫調整

[![データ統合のテンプレートのマッピング](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-fin-and-ops-inventory-transfer"></a>在庫振替 (Field Service から Fin and Ops): 在庫振替

[![データ統合のテンプレートのマッピング](./media/FSTrans1.png)](./media/FSTrans1.png)
