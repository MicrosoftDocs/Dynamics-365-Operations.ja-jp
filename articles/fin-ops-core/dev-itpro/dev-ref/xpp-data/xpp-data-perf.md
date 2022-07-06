---
title: セットベースからレコード単位への操作の変換
description: この記事では、X++ 言語での SQL 操作を高速化する方法について説明します。
author: RobinARH
ms.date: 06/16/2020
audience: Developer
ms.reviewer: robinr
ms.search.region: Global
ms.author: tfehr
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 1c667791e8d3ffec95fe5461cd265b4e0086ae58
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867201"
---
# <a name="conversion-of-operations-from-set-based-to-record-by-record"></a>セットベースからレコード単位への操作の変換

次のステートメントとメソッドを使用して、アプリケーションとデータベース間の通信を減らすことにより、パフォーマンスを向上させることができます。

- [delete_from](xpp-delete.md#delete-from-statement)
- [update_recordset](xpp-update.md#update-recordset-statement)
- [insert_recordset](xpp-insert.md#insert-recordset-statement)
- [RecordSortedList.insertDatabase](/dotnet/api/dynamics.ax.application#method-insertdatabase)
- [RecordInsertList.insertDatabase](/dotnet/api/dynamics.ax.application#method-insertdatabase)

状況によっては、これらのレコード セット ベースの操作をより低速のレコードごとの操作に変換できます。 次のテーブルは、これらの状況を識別します。

| 状況 | delete\_from | update\_recordset | insert\_recordset | RecordSortedList, RecordInsertList | 上書きに使用 |
|---|--------------|-------------------|-------------------|--------------------------------------|------------------|
| 非 SQL テーブル | 有 | 有 | 有 | 有 | 該当なし |
| アクションの削除 | 有 | 無 | 無 | 無 | **skipDeleteActions** |
| データベース ログが有効になっています。 | 有 | 有 | 有 | 無 | **skipDatabaseLog** |
| オーバーライドされたメソッド | 有 | 有 | 有 | 有 | **skipDataMethods** |
| 警告はテーブルの設定をします。 | 有 | 有 | 有 | 無 | **skipEvents** |
| テーブルの **ValidTimeStateFieldType** プロパティが **なし** 以外の値に設定されています。 | あり | あり | あり | あり | 適用できません |

「上書きに使用」列で表示される **スキップ\**設定を使用して、パフォーマンスに悪影響を与える 1 つまた複数の要因を明示的にスキップまたは無視できます。何らかの理由で、前述の SQL 操作のいずれかがレコードごとの操作にダウングレードされた場合、すべての* スキップ\**設定は無視されます。たとえば、次のコードでは、コンテナーまたはメモ フィールドが myTable で定義されている場合はこの方法をスキップする必要があると明確に示されていても、myTable テーブルで* 挿入** メソッドが実行されます。

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]