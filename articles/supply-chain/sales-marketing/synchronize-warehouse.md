---
title: Supply Chain Management から Field Service への倉庫の同期
description: このトピックでは、Dynamics 365 Supply Chain Management から Dynamics 365 Field Service に倉庫を同期させるために使用されるテンプレートと基本的なタスクについて説明します。
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
ms.openlocfilehash: bb365d1aae2ee6d6417f9a76f3a1716eb61c1f5b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572556"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a>Supply Chain Management から Field Service への倉庫の同期

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Dynamics 365 Supply Chain Management から Dynamics 365 Field Service に倉庫を同期させるために使用されるテンプレートと基本的なタスクについて説明します。

[![Supply Chain Management および Field Service 間の業務プロセスの同期。](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>テンプレートおよびタスク
次のテンプレートと基本的なタスクは、Supply Chain Management から Field Service への倉庫の同期を実行するために使用されます。

**データ統合でのテンプレート**
- 倉庫 (Supply Chain Management から Field Service)

**データ統合プロジェクトのタスク**
- 倉庫

## <a name="table-set"></a>テーブル セット
| Field Service    | サプライ チェーン マネジメント                 |
|------------------|----------------------------------------|
| msdyn_warehouses | 倉庫                             |

## <a name="table-flow"></a>テーブル フロー
Supply Chain Management で作成および管理されている倉庫は、Microsoft Dataverse データ統合プロジェクトを通して Field Service に同期することができます。 Field Service に同期する倉庫は、プロジェクトの高度なクエリおよびフィルター処理で制御することができます。 Supply Chain Management から同期する倉庫は Field Service で作成され、**外部で管理** 列を **はい** に設定することにより、レコードは読み取り専用になります。

## <a name="field-service-crm-solution"></a>Field Service CRM ソリューション
Field Service および Supply Chain Management の統合をサポートするために、Field Service CRM からの追加機能が必要です。 ソリューションとして、**外部で管理** 列が、**倉庫 (msdyn_warehouses)** テーブルに追加されました。 この列は、倉庫が Supply Chain Management から処理されているのか、または Field Service にのみ存在するのかを識別するのに役立ちます。 この列の設定は以下のとおりです。
- **はい** – 倉庫は Supply Chain Management に由来し、Sales では編集できません。
- **いいえ** – 倉庫は Field Service で直接入力されており、ここで管理されます。

**外部で管理** 列は、在庫レベル、調整、移動、ワーク オーダーの使用状況の同期を制御します。 **外部で管理** が **はい** に設定された倉庫のみ、その他のシステムの同じ倉庫に直接同期するのに使用されます。 

> [!NOTE]
> Field Service で複数の倉庫を作成し (**外部で管理** = いいえ)、高度なクエリおよびフィルター処理を使用して 1 つの倉庫にマッピングすることができます。 これは、Field service に詳細な在庫レベルを習得させ、Supply Chain Management に更新を送信するだけの場合に使用されます。 この場合、Field service では、Supply Chain Management からの在庫レベルの更新は受信しません。 追加情報については、[Field Service から Finance and Operations への在庫調整の同期](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) および [Field Service でのワーク オーダーを Finance and Operations のプロジェクトにリンクされている販売注文に同期](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order) を参照してください。

## <a name="prerequisites-and-mapping-setup"></a>前提条件およびマッピングの設定
### <a name="data-integration-project"></a>データ統合プロジェクト
倉庫を同期する前に、プロジェクト上で高度なクエリおよびフィルタリング処理を更新し、Supply Chain Management から Field Service へ移動させる倉庫のみが含まれていることを確認してください。 Field Service の倉庫をワーク オーダー、調整、および移動に適用する必要があることに注意してください。  

**統合キー** が **msdyn_warehouses** に存在することを確認するには:
1. データ統合に移動します。
2. **接続設定** タブを選択します。
3. ワーク オーダー同期に使用される接続設定を選択します。
4. **統合キー** タブを選択します。
5. Msdyn_warehouses を検索し、キーの **msdyn_name (名前)** が追加されていることを確認します。 表示されていない場合は、**キーの追加** をクリックして追加してから、ページの上部にある **保存** をクリックします。

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ統合のテンプレート マッピングを示します。

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a>倉庫 (Supply Chain Management から Field Service): 倉庫

[![データ統合のテンプレートのマッピング。](./media/Warehouse1.png)](./media/Warehouse1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]