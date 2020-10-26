---
title: X++ データの選択と操作の概要
description: このトピックでは、X++ データの選択と操作についてのトピックへのリンクを提供します。
author: robinarh
manager: AnnBe
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 150273
ms.search.region: Global
ms.author: rhaertle
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 0c9dc0258aa05e9056b1759cd19cf82ac113378a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983088"
---
# <a name="x-data-selection-and-manipulation-overview"></a>X++ データの選択と操作の概要

[!include [banner](../../includes/banner.md)]

データベースに格納されているデータを取得し変更するため、SQL ステートメントを対話式またはソース コード内で使用することができます。 これらのタスクには、**select** ステートメントおよび API メソッドを使用できます。

- [データの選択](xpp-select.md): 表示または変更するデータを選択します。

    - **[select](xpp-select-statement.md) ステートメント** – レコードをフェッチします。

- [データの挿入](xpp-insert.md): 1 つ以上の新しいレコードをテーブルに追加します。

    - **[insert](xpp-insert.md#insert-method) および [doInsert](xpp-insert.md#do-insert-method) メソッド** – 一度に 1 つのレコードを挿入します。
    - **[insert\_recordset](xpp-insert.md#insert-recordset-statement)、[RecordInsertList.insertDatabase](../system-classes/recordinsertlist-class.md#method-insertdatabase)、および [RecordSortedList.insertDatabase](../system-classes/recordsortedlist-class.md#method-insertdatabase) メソッド** – 複数のレコードを同時に挿入します。

- [データの更新](xpp-update.md): 既存のテーブル レコードでデータを変更します。

    - **[update](xpp-update.md#update-method) および [doUpdate](xpp-update.md#do-update-method) メソッド** – 一度に 1 つのレコードを更新します。
    - **[update\_recordset](xpp-update.md#update-recordset-statement) ステートメント** – 複数のレコードを同時に更新します。

- [データの削除](xpp-delete.md): 既存のレコードをテーブルから削除します。

    - **[delete](xpp-delete.md#delete-method) および [doDelete](xpp-delete.md#do-delete-method) メソッド** – 一度に 1 つのレコードを削除します。
    - **[delete\_from](xpp-delete.md#delete-from-statement) ステートメント** – 複数のレコードを同時に削除します。

データ アクセスに使用するその他のステートメントを次に示します。

- [while select](xpp-while-select.md) ステートメント
- [select](xpp-select-expression.md) 式
- [next](xpp-select.md) ステートメント

[トランザクションの整合性](xpp-transaction.md) により、データの破損を防ぎ、スケーラビリティを向上させることができます。

[セット ベースからレコード単位への操作の変換](xpp-data-perf.md) トピックでは、レコード セット ベースのステートメントおよびメソッドをより効率的に使用するための情報を提供します。

[SysDa クラス](../sysda.md)を使用してデータを取得および変更することもできます。 拡張可能な SysDa API では、X++ で使用できるほとんどすべてのデータアクセス可能性が提供されます。
