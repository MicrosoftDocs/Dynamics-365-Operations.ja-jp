---
title: Supply Chain Management から Field Service への在庫レベル情報の同期
description: この記事では、Dynamics 365 Supply Chain Management から Dynamics 365 Field Service に在庫レベル情報を同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: Henrikan
ms.date: 05/07/2019
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
ms.openlocfilehash: fc14fc63bc1a69a57b10f39b2cb9fb8014e6f70b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844796"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a>Supply Chain Management から Field Service への在庫レベル情報の同期 

[!include[banner](../includes/banner.md)]



この記事では、Dynamics 365 Supply Chain Management から Dynamics 365 Field Service に在庫レベル情報を同期させるために使用されるテンプレートと基本的なタスクについて説明します。

[![Supply Chain Management および Field Service 間の業務プロセスの同期。](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>テンプレートおよびタスク
次のテンプレートと基本的なタスクは、Supply Chain Management から Field Service に手持在庫レベルの同期を実行するために使用されます。

**データ統合でのテンプレート**
- 製品在庫 (Supply Chain Management から Field Service)
  
**データ統合プロジェクトのタスク**
- 製品在庫

在庫レベルの同期が処理される前に、次の同期タスクが必要です。
- 倉庫 (Supply Chain Management から Field Service) 
- 在庫単位のある Field Service 製品 (Supply Chain Management から Sales) 

## <a name="entity-set"></a>エンティティ セット

| Field Service                      | サプライ チェーン マネジメント                |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | 倉庫別 Dataverse手持在庫     |

## <a name="entity-flow"></a>エンティティのフロー
Finance and Operations からの在庫レベル情報は、選択した製品の Field Service に送信されます。 在庫レベル情報は次のとおりです: 
- 手持在庫数量 (倉庫にある現在記録されている現物数量)
- 注文数量 (販売注文などの記録された合計注文数量)
- 注文済数量 (発注書記録された合計注文済数量)

この情報は、各倉庫にリリースされた製品ごとにキャプチャされ、在庫レベルが変更されると、変更追跡に基づいて同期されます。

Field Service では、統合ソリューションがデルタ用の在庫仕訳帳を作成し、Field Service のレベルを Supply Chain Management のレベルと一致するようにします。

Supply Chain Management は、在庫レベルのマスターとして機能します。 したがって、この機能を Supply Chain Management からの在庫レベルの同期と共に Field Service で使用する場合は、ワーク オーダー、振替および調整を Field Service から Supply Chain Management に統合設定することが重要です。

在庫レベルが Supply Chain Management から習得されている製品および倉庫は、高度なクエリおよびフィルタリング (Power Query) で制御できます。

> [!NOTE]
> Field Services で複数の倉庫を作成し (**外部で管理 = いいえ**)、Supply Chain Management で高度なクエリおよびフィルター処理を使用して 1 つの倉庫にマッピングすることができます。 これは、Field service に詳細な在庫レベルを習得させ、Supply Chain Management に更新を送信するだけの場合に使用されます。 この場合、Field service では、Supply Chain Management からの在庫レベルの更新は受信しません。 追加情報については、「[Field Service から Supply Chain Management への在庫調整の同期](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments)」および「[Field Service でのワーク オーダーを Supply Chain Management のプロジェクトにリンクされている販売注文に同期](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order)」を参照してください。

## <a name="field-service-crm-solution"></a>Field Service CRM ソリューション
**外部の製品在庫** エンティティは、統合へのバックエンドのみに使用されます。 このエンティティは統合内の Supply Chain Management から在庫レベルの値を受け取り、次のそれらの値を Manuel 在庫仕訳帳に変換します。これにより、倉庫の在庫製品が変更されます。

## <a name="prerequisites-and-mapping-setup"></a>前提条件およびマッピングの設定

### <a name="data-integration"></a>データ統合
プロジェクトを機能させるには、統合キーが msdynce_externalproductinventories 用に更新されていることを確認する必要があります。
1.  **データ統合 > 接続セット** に移動します。
2.  使用する接続設定を選択します。
3.  **統合キー** タブで、次のキーが msdynce_externalproductinventories に追加されていることを確認します。
      - msdynce_productnumber (製品番号)
      - msdynce_warehouseid (倉庫 ID)
      
### <a name="data-integration-project"></a>データ統合プロジェクト
フィルターを高度なクエリおよびフィルタリングに適用し、特定の製品および倉庫のみが在庫レベル情報を Supply Chain Management から Field Service に送信するようにします。

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a>製品在庫 (Supply Chain Management から Field Service): 製品在庫

[![データ統合のテンプレートのマッピング。](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]