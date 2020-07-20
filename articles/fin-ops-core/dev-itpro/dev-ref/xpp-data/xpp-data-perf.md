---
title: セット ベースからレコード単位への操作の変換
description: このトピックでは、X++ 言語での SQL 操作を高速化する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 150273
ms.assetid: 999a5ecf-559b-4d66-8b05-9a8e477e0518
ms.search.region: Global
ms.author: robinr
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 6740f235f087a88a0379b2c92745f5d396a7a55f
ms.sourcegitcommit: 4ba6817b7aa7735a291a021022b4c12c2de5f2eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/26/2020
ms.locfileid: "3505946"
---
# <a name="conversion-of-operations-from-set-based-to-record-by-record"></a>セット ベースからレコード単位への操作の変換

次のステートメントおよびメソッドを使用して、アプリケーションとデータベース間の通信を減らすことにより、パフォーマンスを向上させることができます。

- [delete_from](xpp-delete.md#delete-from-statement)
- [update_recordset](xpp-update.md#update-recordset-statement)
- [insert_recordset](xpp-insert.md#insert-recordset-statement)
- [RecordSortedList.insertDatabase](../system-classes/recordsortedlist-class.md#method-insertdatabase)
- [RecordInsertList.insertDatabase](../system-classes/recordinsertlist-class.md#method-insertdatabase)

これらのレコード セット ベースの操作をより低速のレコードごとの操作に変換できる状況があります。 次のテーブルは、これらの状況を識別します。

|    | delete\_from | update\_recordset | insert\_recordset | RecordSortedList<br>RecordInsertList | 上書きに使用 |
|----|--------------|-------------------|-------------------|--------------------------------------|------------------|
非 SQL テーブル | 有 | 有 | 有 | 有 | 該当なし
アクションの削除 | 有 | 無 | 無 | 無 | **skipDeleteActions**
データベース ログの有効化 | 有 | 有 | 有 | 無 | **skipDatabaseLog**
オーバーライドされたメソッド | 有 | 有 | 有 | 有 | **skipDataMethods**
テーブルに警告が設定されている | 有 | 有 | 有 | 無 | **skipEvents**
テーブルの **ValidTimeStateFieldType** プロパティが、なしに等しくない | 有 | 有 | 有 | 有 | 該当なし

**上書きに使用**列で表示される設定を使用して、パフォーマンスに悪影響を与える 1 つまたは複数の要因を明示的にスキップまたは無視します。 何らかの理由で前述の SQL 操作のいずれかがレコードごとの操作にダウングレードされた場合、すべての**スキップ\*** 設定も無視されます。 たとえば、次のコードでは、コンテナーまたはメモ フィールドが myTable で定義されている場合はこの方法をスキップする必要があると明確に示されていても、myTable テーブルで**挿入**メソッドが実行されます。

```xpp
public void tutorialRecordInsertList()
{
    MyTable myTable;
    RecordInsertList insertList = new RecordInsertList(
        myTable.TableId,
        True);
    int i;
    for ( i = 1; i <=  100; i++ )
    {
        myTable.value = i;
        insertList.add(myTable);
    }
    insertList.insertDatabase();
}
```
