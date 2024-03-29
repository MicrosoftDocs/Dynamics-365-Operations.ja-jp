---
title: テーブル マップ拡張
description: テーブル マップを拡張するために、テーブル マップをモデルにリファクタリングしました。追加のフィールドとメソッドを使用してソリューションを拡張できます。
author: MichaelFruergaardPontoppidan
ms.date: 12/20/2017
ms.topic: article
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 11
ms.openlocfilehash: 715a0d3f0adae306d3d1c71237cf272d7e1c6cc5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270823"
---
# <a name="table-map-extension"></a>テーブル マップ拡張

[!include [banner](../includes/banner.md)]

テーブル マップを拡張するために、テーブル マップをモデルにリファクタリングしました。追加のフィールドとメソッドを使用してソリューションを拡張できます。 この記事では、テーブルのマップを拡張するためのモデルが必要な理由を説明します。

拡張機能を使用して既存のテーブル マップにフィールドを追加すると、いくつかの問題が発生する可能性があります。 実装時にこれらの問題に対処しない場合は、ランタイム エラーになる可能性があります。 エラーは、開発者がテーブル マップの実装に関連するすべてのテーブルを変更できないために発生します。 メソッドがテーブル マップ上でインスタンス メソッドとして直接呼び出された場合、メソッドをテーブル マップに追加する場合も同じです。 テーブル マップのフィールドがどのようにテーブル マップを実装するすべてのテーブルのフィールドにマップされる必要があるかを、強制する方法はありません。 同様に、テーブル マップのメソッドがどのようにテーブル マップを実装するすべてのテーブルのメソッドにマップされる必要があるかを、強制する方法はありません。

次の図は、**SalesPurchTable** テーブル マップを示しています。これは、**ApplicationSuite** モデルの **SalesTable**、**PurchTable**、および **SalesBasket** テーブルによって実装されています。 さらに、**ISV1Header** テーブルは **SalesPurchTable** テーブル マップを実装しますが、**ISV1Header** は **ISVModule1** モデルの一部です。

![拡張なしのマップ。](media/MapExtensions1.png)

たとえば、**AccountingGroupId** という名前の新しいフィールドおよび **validateAccountingGroup** という名前の新しいメソッドが **ApplicationSuite** モデルでテーブル マップに追加されます。それから、そのテーブル マップを実装するテーブルは、フィールドおよび追加されるメソッドも含むよう更新できます。 ただし、**ISVModule1** モデルの **ISV1Header** テーブルは、開発者が **ApplicationSuite** モデルに変更を加えるコントロールの外にあります。

![新しいフィールドを使用するマップ拡張。](media/MapExtensions2.png)

ビジネス ロジックを **ApplicationSuite** モデルに追加する場合、そのロジックは新しい **AccountingGroupId** フィールドをクエリし、テーブル マップ レコードのタイプが **ISV1Header** である場合、ランタイム エラーが発生します。

```xpp
SalesPurchTable      headerTable;
...
...
if (headerTable.AccountingGroupId)
```

同様に、ビジネス ロジックを **ApplicationSuite** モデルに追加する場合、およびそのロジックが **validateAccountingGroup** を照会する場合、ランタイム エラーが発生します。

```xpp
SalesPurchTable      headerTable;
...
...
if (headerTable.validateAccountingGroup())
```

結果として、新しいフィールドにマッピングを追加して新しいメソッドを **ISV1Header** テーブルに追加しない限り、ソリューションは破損します。 

フィールドまたはメソッドを追加する機能が拡張機能を介してテーブル マップに追加された場合は、競合は解決されません。 これは、**ISVModule2** に **ApplicationSuite** モデルのテーブル マップと実装テーブルの拡張が含まれている次の図に示されています。 **ISVModule2** を実装する開発者は、**ISVModule1** モデルの **ISV1Header** テーブルを制御できません。**ISV1Header** テーブルには、**AccountingGroupId** フィールドのマッピングと **validateAccountingGroup** メソッドの実装がありません。

![新しいフィールドおよび新しいメソッドを使用する拡張。](media/MapExtensions3.png)

コンパイラがテーブル マップのすべてのフィールドとメソッドを、テーブル マップを実装するすべてのテーブルにマップする必要がある場合でも、競合は解決されません。 マップされた新しいフィールドまたは実装された新しいメソッドがないテーブルは、追加されたフィールド/メソッドを含むモデルが適用されるときにコンパイルするため、ランタイム エラーを受け取る代わりに、フィールドまたはメソッドを追加することで重大な変更をクリアします。 テーブル マップを拡張するために、テーブル マップをモデルにリファクタリングしました。追加のフィールドとメソッドを使用してソリューションを拡張できます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
