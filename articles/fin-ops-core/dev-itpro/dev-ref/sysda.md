---
title: SysDa クラスを使用したデータへのアクセス
description: このトピックでは、SysDa アプリケーションプログラミングインターフェイス (API) を使用して拡張可能なクエリおよびデータアクセスステートメントを作成する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 72211
ms.assetid: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06a8f41eec22779a5e5148c6f3e1114be45f3215
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408753"
---
# <a name="access-data-by-using-the-sysda-classes"></a>SysDa クラスを使用したデータへのアクセス

[!include [banner](../includes/banner.md)]

このトピックでは、SysDa アプリケーションプログラミングインターフェイス (API) を使用して拡張可能なクエリおよびデータアクセスステートメントを作成する方法について説明します。

拡張可能な SysDa API では、X++ で使用できるほとんどすべてのデータアクセス可能性が提供されます。 実際、API は、X++ コンパイラが生成するコードのラッパーです。 したがって、SysDa クラスを使用しても、たとえば **QueryRun** オブジェクトなどを使用してもオーバーヘッドは発生しません。 さらに、X++ コンパイラがデータアクセス明細書に対して行うチェックは、ユーザーの責任です。 たとえば、グローバルな一意識別子 ( GUID) を整数と比較する **where** 句を作成します。 X++ コンパイラは、この句をエラーとして診断します。

SysDa API には、カスタムクエリを作成するための広範な API セットが含まれています。 ただし、主なクエリ活動を駆動するもっと小さなタイプには以下のものがあります。

+ 次を選択します: **SysDaQueryObject**、**SysDaSearchObject**、および **SysDaSearchStatement**
+ 次を更新します: **SysDaUpdateObject** および **SysDaUpdateStatement**
+ 次を挿入します: **SysDaInsertObject** および **SysDaInsertStatement**
+ 次を削除します: **SysDaQueryObject**、**SysDaDeleteObject**、および **SysDaDeleteStatement**

次のセクションでは、クエリのタイプの例と、それがサポートするカスタマイズについて説明します。 この例では、TestTable という名前のテーブルを使用します。 このテーブルには、**stringField** という名前の文字列フィールドと、**intField** という名前の整数フィールドの2つのフィールドがあります。

## <a name="select-query"></a>クエリの選択

**選択** クエリを実行するには、次の手順を実行します。

1. 指定されたレコードを含むテーブルインスタンスを指定する、**SysDaQueryObject** オブジェクトを作成および構成します。
2. **Sysdasearchobject** オブジェクトを作成し、**SysDaQueryObject** オブジェクトをコンストラクターに渡します。
3. **Sysdasearchobject** オブジェクトを **SysDaSearchStatement.next()** メソッドに渡すことで、クエリの結果を繰り返します。

次の例では **intField**\<= **5** のTestTableのすべての行を検索します。

```xpp
// t is the table buffer that will hold the result.
TestTable t;

// Create the query.
var qe = new SysDaQueryObject(t);

// Add clauses to the query. First the projection.
var s = qe.projection()
    .add(fieldStr(TestTable, intField))
    .add(fieldStr(TestTable, stringField));

// At this point the query is:
// intField, stringField FROM TestTable

// Add a where clause to include rows where intField is <= 5.
qe.WhereClause(new SysDaLessThanOrEqualsExpression(
    new SysDaFieldExpression(t, fieldStr(TestTable, intField)),
    new SysDaValueExpression(5)));

// Now the query is:
// intField, stringField FROM TestTable WHERE (TestTable.intField<= 5)

// Order the results by intField.
qe.OrderByClause().addDescending(fieldStr(TestTable, intField));

// Now the query is:
// intField, stringField FROM TestTable ORDER BY intField DESC WHERE (TestTable.intField<= 5)

var so = new SysDaSearchObject(qe);
var ss = new SysDaSearchStatement();

// Enumerate the designated values by using ss.
while (ss.next(so))
{
    info(t.stringField);
}
```

## <a name="update-statement"></a>明細書の更新

**Update** 明細書を実行するには、次の手順を実行します。

1. **SysDaUpdateObject** オブジェクトを作成および構成します。
2. **SysDaUpdateObject** オブジェクトを **SysDaUpdateStatement.execute()** オブジェクトに渡すことでデータを更新します。 更新ではデータベースのデータが変更されるため、**ttsbegin** および **ttscommit** ステートメントで **実行** するための呼び出しをラップする必要があります。

次の例では、**intField** = **50** のすべての行について、**stringField** を **"fifty"** に更新します。

```xpp
TestTable t;

// Create an update query to find rows where intField = 50.
var uo = new SysDaUpdateObject(t);

// Set stringField to "fifty".
uo.settingClause()
    .add(fieldStr(TestTable, stringField), new SysDaValueExpression("fifty"));

// At this point the update statement is:
// UPDATE_RECORDSET TestTable SETTING stringField=fifty

uo.whereClause(new SysDaEqualsExpression(
    new SysDaFieldExpression(t, fieldStr(TestTable, intField)),
    new SysDaValueExpression(50)));

// Now the update statement is:
// UPDATE_RECORDSET TestTable SETTING stringField=fifty WHERE (TestTable.intField == 50)

// Update the rows.
ttsbegin;
    new SysDaUpdateStatement().execute(uo);
ttscommit;

// Verify the results of the update query.
TestTable t1;
select intField, stringField from t1 where t1.intField == 50;
info("Updated value is: " + t1.stringField);
// Output is: "Updated value is: fifty".
```

## <a name="insert-statement"></a>明細書の挿入

**挿入** 明細書を実行するには、次の手順を実行します。

1. **SysDaInsertObject** オブジェクトを作成および構成して、挿入中に更新されるフィールドを指定します。
2. 挿入する行のソースを指定する **SysDaQueryObject** オブジェクトを作成および構成します。 **SysDaQueryObject.予測()** のフィールドの順序は、**SysDaInsertObject.fields()** のフィールドの順序と一致している必要があります。
3. **SysDaQueryObject** オブジェクトを、**SysDaInsertObject** オブジェクトに割り当てます。
4. 新しい行を挿入するには **SysDaInsertObject** オブジェクトを **SysDaInsertStatement.executeQuery()** メソッドに渡します。

次の例では、行を **intField** = **40** と **stringField** = **"en-us"** を TestTable に挿入します。

```xpp
TestTable t;

// Specify the fields in the new row.
var insertObject = new SysDaInsertObject(t);
insertObject.fields()
    .add(fieldStr(TestTable, stringField))
    .add(fieldStr(TestTable, intField));

// At this point the insert statement is:
// INSERT_RECORDSET TestTable(stringField, intField) SELECT

// Retrieve the data to insert from the LanguageTable by using a query.
LanguageTable source;
var qe = new SysDaQueryObject(source);

var s1 = qe.projection()
    .Add(fieldStr(LanguageTable, LanguageId))
    .AddValue(40);

// The query statement is:
// LanguageId, 40 FROM LanguageTable

qe.WhereClause(new SysDaEqualsExpression(
        new SysDaFieldExpression(source, fieldStr(LanguageTable, LanguageId)),
        new SysDaValueExpression("en-us")));

// Now the query is:
// LanguageId, 40 FROM LanguageTable WHERE (LanguageTable.LanguageId == en-us)

// Assign the query to the insert statement.
insertObject.query(qe); 

// The insert statement is now:
// INSERT_RECORDSET TestTable(stringField, intField) SELECT LanguageId, 40 FROM LanguageTable WHERE (LanguageTable.LanguageId == en-us)

var insertStmt = new SysDaInsertStatement();
ttsbegin;
    insertStmt.executeQuery(insertObject);
ttscommit;

// Verify the results of the insert query.
TestTable t1;
select * from t1 where t1.stringField == "en-us";
info(any2Str(t1.intField) + ":" + t1.stringField); 
// The output is "40:en-us".
```

## <a name="delete-statement"></a>明細書の削除

明細書の **削除** を実行するには、次の手順を実行します。

1. **Sysdaqueryobject** オブジェクトを作成および構成して、削除する行を指定します。
2. **SysDaDeleteObject** オブジェクトを作成し、**SysDaQueryObject** オブジェクトをコンストラクターに渡します。
3. 行を削除するには **SysDaDeleteObject** オブジェクトを **SysDaDeleteStatement.executeQuery()** メソッドに渡します。

次の例では、**intField** が偶数である行を削除します。

```xpp
TestTable t;

// Build the query that specifies which rows to delete.
var qe = new SysDaQueryObject(t);

var s = qe.projection()
    .add(fieldStr(TestTable, intField));

// At this point the query is:
// intField FROM TestTable

// Delete rows where intField is even.
qe.WhereClause(new SysDaEqualsExpression(
    new SysDaModExpression(
    new SysDaFieldExpression(t, fieldStr(TestTable, intField)),
    new SysDaValueExpression(2)),
    new SysDaValueExpression(0)));

// Now the query is:
// intField FROM TestTable WHERE ((TestTable.intField MOD 2) == 0)

var ds = new SysDaDeleteStatement();
var delobj = new SysDaDeleteObject(qe);

// The deletion statement, from the SysDaDeleteObject, is:
// DELETE_FROM intField FROM TestTable WHERE ((TestTable.intField MOD 2) == 0)

ttsbegin;
    ds.executeQuery(delobj);
ttscommit;

info("Number of rows after deletion: " + any2Str(t.RowCount()));
```

## <a name="clauses"></a>句

SysDa クエリは複数の句をサポートします。

+ **whereClause** – **where** 句は、**SysDaQueryExpression** から継承したオブジェクトから構築されます。 例は **SysDaEqualsExpression**、**SysDaNotEqualsExpression**、**SysDaLessThanExpression** があります。 完全な一覧は、アプリケーションエクスプローラーでフィルタ処理することによって確認できます。
+ **orderByClause**
+ **groupByClause**
+ **joinClauseKind** 付き **joinClause**
+ **joinedQuery**
+ **settingClause**

## <a name="troubleshooting"></a>トラブルシューティング

**toString()** メソッドを、**SysDaQueryObject**、**SysDaUpdateObject**、**SysDaInsertObject**、および **SysDaQueryObject** オブジェクトに対して使用して、構築している明細書を表示できます。
