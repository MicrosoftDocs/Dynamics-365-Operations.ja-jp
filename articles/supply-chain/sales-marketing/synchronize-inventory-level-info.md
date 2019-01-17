---
title: "Finance and Operations から Field Service への在庫レベル情報の同期"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に在庫レベル情報を同期させるために使用されるテンプレートと基本的なタスクについて説明します。"
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
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: ja-jp
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>Finance and Operations から Field Service への在庫レベル情報の同期 

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service に在庫レベル情報を同期させるために使用されるテンプレートと基本的なタスクについて説明します。

[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>テンプレートおよびタスク
次のテンプレートと基本的なタスクは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service への手持在庫レベルの同期を実行するために使用されます。

**データ統合でのテンプレートの名前:**
- 製品在庫 (Finance and Operations から Field Service)
  
**データ統合プロジェクトのタスク名:**
- 製品在庫

在庫レベルの同期が処理される前に、次の同期タスクが必要です。
- 倉庫 (Finance and Operations から Field Service) 
- 在庫単位のある Field Service 製品 (Finance and Operations から 販売) 

## <a name="entity-set"></a>エンティティ セット

| Field Service                      | Finance and Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | CDS 倉庫別手持在庫     |

## <a name="entity-flow"></a>エンティティのフロー
Finance and Operations からの在庫レベル情報は、選択した製品の Field Service に送信されます。 在庫レベル情報は次のとおりです: 
- 手持在庫数量 (倉庫にある現在記録されている現物数量)
- 注文数量 (記録された合計注文数量 - 販売注文)
- 注文済数量 (記録された合計注文済数量 - 発注書)

この情報は、各倉庫にリリースされた製品ごとにキャプチャされ、在庫レベルが変更されると、変更追跡に基づいて同期されます。

Field Service では、統合ソリューションがデルタ用の在庫仕訳帳を作成し、Field Service のレベルを Finance and Operations のレベルと一致させます。

Finance and Operations は、在庫レベルのマスターとして機能します。 したがって、この機能を Finance and Operations からの在庫レベルの同期と共に Field Service で使用する場合は、ワークオーダー、振替および調整を、Field Service から Finance and Operations に統合設定することが重要です。

在庫レベルが Finance and Operations から習得されている製品および倉庫は、高度なクエリおよびフィルタリング (Power Query) で制御できます。

Field Services で複数の倉庫を作成し (外部で管理 = いいえの場合)、Finance and Operations で高度なクエリおよびフィルター処理を使用して 1 つの倉庫にマッピングすることができます。 これは、Field service に詳細な在庫レベルを習得させ、Finance and Operations に更新を送信するだけの場合に使用されます。 この場合、Field service は、Finance and Operations からの在庫レベルの更新は受信しません。 追加情報については、Field Service から Finance and Operations への在庫調整の同期、および Field Service でのワーク オーダーを Finance and Operations のプロジェクトにリンクされている販売注文に同期、を参照してください。

## <a name="field-service-crm-solution"></a>Field Service CRM ソリューション
外部の製品在庫エンティティは、統合のバックエンドのみに使用される新しいエンティティです。 統合内の Finance and Operations から在庫レベルの値を受け取り、次のそれらの値を Manuel 在庫仕訳帳に変換します。これにより、倉庫の在庫製品が変更されます。 

## <a name="prerequisites-and-mapping-setup"></a>前提条件およびマッピングの設定

### <a name="in-the-data-integration-project"></a>データ統合プロジェクト内
高度なクエリおよびフィルタリングを使用してフィルターを適用し、必要な製品および倉庫のみが在庫レベル情報を Finance and Operations から Field Service に送信するように制御します。

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a>製品在庫 (Finance and Operations から Field Service): 製品在庫

[![データ統合のテンプレートのマッピング](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)

