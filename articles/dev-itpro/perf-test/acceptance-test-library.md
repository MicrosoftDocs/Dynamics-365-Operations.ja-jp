---
title: 承認テスト ライブラリ
description: このトピックでは承認テスト ライブラリに関する情報を提供します。
author: MichaelFruergaardPontoppidan
manager: AnnBe
ms.date: 03/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: RobinARH
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: MichaelFruergaardPontoppidan
ms.search.validFrom: 2018-XX-XX
ms.dyn365.ops.version: App Update 10.0.2
ms.openlocfilehash: dcc7ecd5099402bc0f5e84b778f2486f009011bf
ms.sourcegitcommit: 185d13bc3e2b2a51569471368671d5cc3023ab14
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/12/2019
ms.locfileid: "992912"
---
# <a name="acceptance-test-library"></a>承認テスト ライブラリ

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

承認テスト ライブラリ (ATL) は、X++ テスト ライブラリであり、以下の利点を提供します:

- 一貫したテスト データを作成できます。
- テスト コードが読みやすくなります。
- テスト データの作成に使用されているメソッドの発見可能性が向上します。
- 前提条件の設定の複雑さを隠します。
- パフォーマンスの高いテスト ケースをサポートします。

## <a name="example-of-a-test-that-is-written-in-atl"></a>ATL で記述されたテストの例

```
// Get a reference to a well-known warehouse 
var warehouse = data.invent().warehouses().default();
 
// Create a new item with the "default" setup using the item creator class. Adjust the default warehouse before saving the item.
var item = items.defaultBuilder().setDefaultWarehouse(warehouse).create();

// Add on-hand (information about availability of the item in the warehouse) by using the on-hand adjustment command.
onHand.adjust().forItem(item).forInventDims([warehouse]).setQty(100).execute();

// Create a sales order with one line using the sales order entity
var salesOrder = data.sales().salesOrders().createDefault();
var salesLine = salesOrder.addLine().setItem(item).setQuantity(10).save();

// Reserve 3 units of the item using the reserve() command that is exposed directly on the sales line entity
salesLine.reserve().setQty(3).execute();

// Verify inventory transactions that are associated with the sales line using the inventoryTransactions query and specifications
salesLine.inventoryTransactions().assertExpectedLines(
    invent.trans().spec().withStatusIssue(StatusIssue::OnOrder).withInventDims([warehouse]).withQty(-3),
    invent.trans().spec().withStatusIssue(StatusIssue::ReservPhysical).withInventDims([warehouse]).withQty(-7)); 
```

## <a name="concepts"></a>概念

ATL のクラスとメソッドの構造と命名は非常に厳格です。 この厳格さにより、発見性が向上し、慣れないドメインでさえもテストを簡単に作成できるようになります。

クラスは次の概念に分類されます:

- [ナビゲーション](concepts-navigation.md) – 慣れている階層でエンティティを検出し、データ メソッドをテストします。
- [テスト データ メソッド](test-data-methods.md) – これらのメソッドはテスト データの設定に使用されます。
- [エンティティ](concepts-entities.md) – エンティティは、ひとつの単位として認識されるデータと、それに関連する動作を表します。
- [作成者](concepts-creators.md) – 作成者により特定のテスト データを作成できます。
- [コマンド](concepts-commands.md) – コマンドは事業運営を実行します。
- [クエリ](concepts-queries.md) – クエリはエンティティを検索します。
- [仕様](concepts-specifications.md) – 仕様はテストの終わりで期待されるエンティティを説明します。

## <a name="code-generation"></a>コード生成

クエリと仕様は、エンティティの作成プロセスを簡素化するのに役立ちます。 詳細は [承認テスト ライブラリ コード生成ウィザード](code-generation-wizard.md) を参照してください。 **コード生成** ウィザードを使用してシナリオを作成し、またそれらを更新することができます。

## <a name="further-reading"></a>参考文献

何千ものテスト基盤として、Microsoft は ATL を社内で何年も使用してきました。 詳細については [承認テスト ライブラリのベスト プラクティス](atl-best-practices.md) および [承認テスト ライブラリについてよく寄せられる質問](atl-faq.md) を参照してください。
