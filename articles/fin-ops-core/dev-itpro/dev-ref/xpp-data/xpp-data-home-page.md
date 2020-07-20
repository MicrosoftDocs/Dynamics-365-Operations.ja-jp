---
title: X++ データの選択と操作の概要
description: このトピックでは、X++ 言語での select ステートメントについて説明します。
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
ms.author: robinr
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 0788129db2ebb809601be770b3233b88aeff4bab
ms.sourcegitcommit: 4ba6817b7aa7735a291a021022b4c12c2de5f2eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/26/2020
ms.locfileid: "3505952"
---
# <a name="x-data-selection-and-manipulation-overview"></a>X++ データの選択と操作の概要

[!include [banner](../../includes/banner.md)]

データベースに格納されているデータを取得し変更するため、SQL ステートメントを対話的またはソース コード内で使用することができます。 これらのタスクには、**select** ステートメントおよび API メソッドを使用できます。

- [データの選択](xpp-select.md): 表示または変更するデータを選択します。

    - [select ステートメント](xpp-select-statement.md): レコードをフェッチします。

- [データの挿入](xpp-insert.md): 1 つ以上の新しいレコードをテーブルに追加します。

    - [insert](xpp-insert.md#insert-method) および [doinsert](xpp-insert.md#do-insert-method) メソッド: 一度に 1 つのレコードを挿入します。
    - [insert\_recordset](xpp-insert.md#insert-recordset-statement)、[RecordInsertList.insertDatabase](../system-classes/recordinsertlist-class.md#method-insertdatabase)、および [RecordSortedList.insertDatabase](../system-classes/recordsortedlist-class.md#method-insertdatabase) メソッド: 複数のレコードを同時に挿入します。

- [データの更新](xpp-update.md): 既存のテーブル レコードでデータを変更します。

    - [update](xpp-update.md#update-method) および [doUpdate](xpp-update.md#do-update-method) メソッド: 一度に 1 つのレコードを更新します。
    - [update\_recordset](xpp-update.md#update-recordset-statement) ステートメント: 複数のレコードを同時に更新します。

- [データの削除](xpp-delete.md): 既存のレコードをテーブルから削除します。

    - [delete](xpp-delete.md#delete-method) および [doDelete](xpp-delete.md#do-delete-method) メソッド: 一度に 1 つのレコードを削除します。
    - [delete\_from](xpp-delete.md#delete-from-statement) ステートメント: 複数のレコードを同時に削除します。

データ アクセスに使用するその他のステートメントを次に示します。

- [while select](xpp-while-select.md) ステートメント。
- [select 式](xpp-select-expression.md)。
- [next](xpp-select.md) ステートメント。

[トランザクションの整合性](xpp-transaction.md)により、データの破損を防ぎ、スケーラビリティを向上させることができます。

[セット ベースからレコードごとへの操作の変換](xpp-data-perf.md)では、レコードセット ベースのステートメントおよびメソッドを効率的に使用するための追加情報を提供します。

[SysDa クラス](../sysda.md)を使用してデータを取得および変更することもできます。 拡張可能な SysDa API では、X++ で使用できるほとんどすべてのデータアクセス可能性が提供されます。
