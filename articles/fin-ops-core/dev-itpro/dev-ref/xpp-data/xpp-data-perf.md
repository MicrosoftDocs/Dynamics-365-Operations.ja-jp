---
title: セットベースからレコード単位への操作の変換
description: この記事では、X++ 言語での SQL 操作を高速化する方法について説明します。
author: josaw1
ms.date: 06/16/2020
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e04e079e198e0b8a3cbb3e3b1eab308ea887b66
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271363"
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
