---
title: "Finance and Operations から Field Service への倉庫の同期"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に倉庫を同期させるために使用されるテンプレートと基本的なタスクについて説明します。"
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
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
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: ja-jp
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a>Finance and Operations から Field Service への倉庫の同期

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に倉庫を同期させるために使用されるテンプレートと基本的なタスクについて説明します。

[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>テンプレートおよびタスク
次のテンプレートおよび基本的なタスクは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に倉庫の同期を実行するために使用されます。

**データ統合でのテンプレートの名前:**
- 倉庫 (Finance and Operations から Field Service)

**データ統合プロジェクトのタスク名:**
- 倉庫

## <a name="entity-set"></a>エンティティ セット
| Field Service    | Finance and Operations                 |
|------------------|----------------------------------------|
| msdyn_warehouses | 倉庫                             |

## <a name="entity-flow"></a>エンティティのフロー
Finance and Operations で作成および管理されている倉庫は、Common Data Service (CDS) データの統合プロジェクトを通して Field Service に同期することができます。 Field Service に同期することが必要な倉庫は、プロジェクトの高度なクエリおよびフィルター処理で制御することができます。 Finance and Operations から同期する倉庫は Field Service で作成され、外部で管理フィールドをはいに設定することにより、レコードは読み取り専用になります。
Field Service CRM ソリューション Field Service および Finance and Operations の統合をサポートするために、Field Service CRM からの追加機能が必要です。 ソリューションには、次の変更が含まれます。
**外部で管理**フィールドが、**倉庫 (msdyn_warehouses)** エンティティに追加されました。 このフィールドは、倉庫が Operations から処理されているのか、または Field Service にのみ存在するのかを識別するのに役立ちます。
- はい – 倉庫は Finance and Operations に由来し、Sales では編集できません。
- いいえ – 倉庫は Field Service で直接入力されており、ここで管理されます。

**外部で管理**フィールドは、在庫レベル、調整、移動およびワーク オーダーの使用状況の同期を制御します。 **外部で管理** = はいの倉庫のみ、その他のシステムの同じ倉庫に直接同期するのに使用されます。 

注記: Field Services で複数の倉庫を作成し (**外部で管理** = いいえの場合)、Finance and Operations で高度なクエリおよびフィルター処理を使用して 1 つの倉庫にマッピングすることができます。 これは、Field service に詳細な在庫レベルを習得させ、Finance and Operations に更新を送信するだけの場合に使用されます。 この場合、Field service は、Finance and Operations からの在庫レベルの更新は受信しません。 追加情報については、Field Service から Finance and Operations への在庫調整の同期、および Field Service でのワーク オーダーを Finance and Operations のプロジェクトにリンクされている販売注文に同期、を参照してください。

## <a name="prerequisites-and-mapping-setup"></a>前提条件およびマッピングの設定
### <a name="in-the-data-integration-project"></a>データ統合プロジェクト内
倉庫の同期の前に、プロジェクト上で高度なクエリおよびフィルタリング処理を更新し、Finance and Operations から Field Service へ移動させる倉庫のみが含まれていることを確認してください。 Field Service の倉庫をワーク オーダー、調整、および移動に適用する必要があることに注意してください。  

**統合キー**が **msdyn_warehouses** に存在することを確認
1. データ統合に移動
2. **接続設定**タブを選択
3. ワーク オーダー同期に使用される接続設定を選択します。
4. **統合キー**タブを選択
5. Msdyn_warehouses を検索し、キーの **msdyn_name (名前)** が追加されていることを確認します。 表示されていない場合は、**キーの追加**をクリックして追加し、ページの上部にある**保存**をクリックします

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ統合のテンプレート マッピングを示しています。

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a>倉庫 (Finance and Operations から Field Service): 倉庫

[![データ統合のテンプレートのマッピング](./media/Warehouse1.png)](./media/Warehouse1.png)

