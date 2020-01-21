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
ms.search.scope: Operations
ms.custom: 72211
ms.assetid: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37da0a13176e73b09e4b62c4e4fce9d37e7ca2d3
ms.sourcegitcommit: 7eae20185944ff7394531173490a286a61092323
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/03/2019
ms.locfileid: "2872655"
---
# <a name="access-data-by-using-the-sysda-classes"></a><span data-ttu-id="2e4b5-103">SysDa クラスを使用したデータへのアクセス</span><span class="sxs-lookup"><span data-stu-id="2e4b5-103">Access data by using the SysDa classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e4b5-104">このトピックでは、SysDa アプリケーションプログラミングインターフェイス (API) を使用して拡張可能なクエリおよびデータアクセスステートメントを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-104">This topic explains how to create extensible queries by using the SysDa application programming interface (API).</span></span>

<span data-ttu-id="2e4b5-105">拡張可能な SysDa API では、X++ で使用できるほとんどすべてのデータアクセス可能性が提供されます。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-105">The extensible SysDa API provides almost all the data access possibilities that are available in X++.</span></span> <span data-ttu-id="2e4b5-106">実際、API は、X++ コンパイラが生成するコードのラッパーです。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-106">In fact, the APIs are wrappers around the code that the X++ compiler would generate.</span></span> <span data-ttu-id="2e4b5-107">したがって、SysDa クラスを使用しても、たとえば**QueryRun**オブジェクトなどを使用してもオーバーヘッドは発生しません。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-107">Therefore, use of the SysDa classes carries no overhead, unlike use of the **QueryRun** object, for example.</span></span> <span data-ttu-id="2e4b5-108">さらに、X++ コンパイラがデータアクセス明細書に対して行うチェックは、ユーザーの責任です。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-108">Additionally, the check that the X++ compiler does on data access statements is your responsibility.</span></span> <span data-ttu-id="2e4b5-109">たとえば、グローバルな一意識別子 ( GUID) を整数と比較する **where** 句を作成します。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-109">For example, you create a **where** clause that compares a globally unique identifier (GUID) to an integer.</span></span> <span data-ttu-id="2e4b5-110">X++ コンパイラは、この句をエラーとして診断します。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-110">The X++ compiler would diagnose this clause as an error.</span></span>

<span data-ttu-id="2e4b5-111">SysDa API には、カスタムクエリを作成するための広範な API セットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-111">The SysDa APIs include an extensive set of APIs for creating custom queries.</span></span> <span data-ttu-id="2e4b5-112">ただし、主なクエリ活動を駆動するもっと小さなタイプには以下のものがあります。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-112">However, there is a smaller set of types that drives the primary query activities:</span></span>

+ <span data-ttu-id="2e4b5-113">次を選択します: **SysDaQueryObject**、**SysDaSearchObject**、および **SysDaSearchStatement**</span><span class="sxs-lookup"><span data-stu-id="2e4b5-113">Select: **SysDaQueryObject**, **SysDaSearchObject**, and **SysDaSearchStatement**</span></span>
+ <span data-ttu-id="2e4b5-114">次を更新します: **SysDaUpdateObject** および **SysDaUpdateStatement**</span><span class="sxs-lookup"><span data-stu-id="2e4b5-114">Update: **SysDaUpdateObject** and **SysDaUpdateStatement**</span></span>
+ <span data-ttu-id="2e4b5-115">次を挿入します: **SysDaInsertObject** および **SysDaInsertStatement**</span><span class="sxs-lookup"><span data-stu-id="2e4b5-115">Insert: **SysDaInsertObject** and **SysDaInsertStatement**</span></span>
+ <span data-ttu-id="2e4b5-116">次を削除します: **SysDaQueryObject**、**SysDaDeleteObject**、および **SysDaDeleteStatement**</span><span class="sxs-lookup"><span data-stu-id="2e4b5-116">Delete: **SysDaQueryObject**, **SysDaDeleteObject**, and **SysDaDeleteStatement**</span></span>

<span data-ttu-id="2e4b5-117">次のセクションでは、クエリのタイプの例と、それがサポートするカスタマイズについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-117">The following sections provide examples of each type of query and the customizations that it supports.</span></span> <span data-ttu-id="2e4b5-118">この例では、TestTable という名前のテーブルを使用します。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-118">The examples use a table that is named TestTable.</span></span> <span data-ttu-id="2e4b5-119">このテーブルには、**stringField** という名前の文字列フィールドと、**intField** という名前の整数フィールドの2つのフィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-119">This table has two fields: a string field that is named **stringField** and an integer field that is named **intField**.</span></span>

## <a name="select-query"></a><span data-ttu-id="2e4b5-120">クエリの選択</span><span class="sxs-lookup"><span data-stu-id="2e4b5-120">Select query</span></span>

<span data-ttu-id="2e4b5-121">**選択** クエリを実行するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-121">To run a **select** query, follow these steps.</span></span>

1. <span data-ttu-id="2e4b5-122">指定されたレコードを含むテーブルインスタンスを指定する、**SysDaQueryObject** オブジェクトを作成および構成します。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-122">Create and configure a **SysDaQueryObject** object that specifies the table instance that will contain the designated records.</span></span>
2. <span data-ttu-id="2e4b5-123">**Sysdasearchobject** オブジェクトを作成し、**SysDaQueryObject** オブジェクトをコンストラクターに渡します。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-123">Create a **SysDaSearchObject** object, and pass the **SysDaQueryObject** object to the constructor.</span></span>
3. <span data-ttu-id="2e4b5-124">**Sysdasearchobject** オブジェクトを**SysDaSearchStatement.next()** メソッドに渡すことで、クエリの結果を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-124">Iterate over the results of the query by passing the **SysDaSearchObject** object to the **SysDaSearchStatement.next()** method.</span></span>

<span data-ttu-id="2e4b5-125">次の例では**intField**\<= **5** のTestTableのすべての行を検索します。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-125">The following example finds all rows in TestTable where **intField** \<= **5**.</span></span>

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

## <a name="update-statement"></a><span data-ttu-id="2e4b5-126">明細書の更新</span><span class="sxs-lookup"><span data-stu-id="2e4b5-126">Update statement</span></span>

<span data-ttu-id="2e4b5-127">**Update** 明細書を実行するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-127">To run an **update** statement, follow these steps.</span></span>

1. <span data-ttu-id="2e4b5-128">**SysDaUpdateObject**オブジェクトを作成および構成します。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-128">Create and configure a **SysDaUpdateObject** object.</span></span>
2. <span data-ttu-id="2e4b5-129">**SysDaUpdateObject** オブジェクトを **SysDaUpdateStatement.execute()** オブジェクトに渡すことでデータを更新します。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-129">Update data by passing the **SysDaUpdateObject** object to the **SysDaUpdateStatement.execute()** object.</span></span> <span data-ttu-id="2e4b5-130">更新ではデータベースのデータが変更されるため、**ttsbegin** および **ttscommit** ステートメントで **実行** するための呼び出しをラップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-130">Because updates modify the data in the database, you must wrap the call to **execute** in **ttsbegin** and **ttscommit** statements.</span></span>

<span data-ttu-id="2e4b5-131">次の例では、**intField** = **50** のすべての行について、**stringField** を **"fifty"** に更新します。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-131">The following example updates **stringField** to **"fifty"** for all rows where **intField** = **50**.</span></span>

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

## <a name="insert-statement"></a><span data-ttu-id="2e4b5-132">明細書の挿入</span><span class="sxs-lookup"><span data-stu-id="2e4b5-132">Insert statement</span></span>

<span data-ttu-id="2e4b5-133">**挿入**明細書を実行するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-133">To run an **insert** statement, follow these steps.</span></span>

1. <span data-ttu-id="2e4b5-134">**SysDaInsertObject** オブジェクトを作成および構成して、挿入中に更新されるフィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-134">Create and configure a **SysDaInsertObject** object to specify which fields are updated during the insertion.</span></span>
2. <span data-ttu-id="2e4b5-135">挿入する行のソースを指定する **SysDaQueryObject** オブジェクトを作成および構成します。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-135">Create and configure a **SysDaQueryObject** object that specifies the source of the rows to insert.</span></span> <span data-ttu-id="2e4b5-136">**SysDaQueryObject.予測()** のフィールドの順序は、**SysDaInsertObject.fields()** のフィールドの順序と一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-136">The order of the fields in **SysDaQueryObject.projection()** must match the order of the fields in **SysDaInsertObject.fields()**.</span></span>
3. <span data-ttu-id="2e4b5-137">**SysDaQueryObject** オブジェクトを、**SysDaInsertObject** オブジェクトに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-137">Assign the **SysDaQueryObject** object to the **SysDaInsertObject** object.</span></span>
4. <span data-ttu-id="2e4b5-138">新しい行を挿入するには**SysDaInsertObject** オブジェクトを **SysDaInsertStatement.executeQuery()** メソッドに渡します。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-138">Insert the new row by passing the **SysDaInsertObject** object to the **SysDaInsertStatement.executeQuery()** method.</span></span>

<span data-ttu-id="2e4b5-139">次の例では、行を **intField** = **40** と**stringField** = **"en-us"** を TestTable に挿入します。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-139">The following example inserts rows where **intField** = **40** and **stringField** = **"en-us"** into TestTable.</span></span>

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

## <a name="delete-statement"></a><span data-ttu-id="2e4b5-140">明細書の削除</span><span class="sxs-lookup"><span data-stu-id="2e4b5-140">Delete statement</span></span>

<span data-ttu-id="2e4b5-141">明細書の **削除** を実行するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-141">To run a **delete** statement, follow these steps.</span></span>

1. <span data-ttu-id="2e4b5-142">**Sysdaqueryobject** オブジェクトを作成および構成して、削除する行を指定します。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-142">Create and configure a **SysDaQueryObject** object to specify which rows to delete.</span></span>
2. <span data-ttu-id="2e4b5-143">**SysDaDeleteObject** オブジェクトを作成し、**SysDaQueryObject** オブジェクトをコンストラクターに渡します。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-143">Create a **SysDaDeleteObject** object, and pass the **SysDaQueryObject** object to the constructor.</span></span>
3. <span data-ttu-id="2e4b5-144">行を削除するには **SysDaDeleteObject** オブジェクトを **SysDaDeleteStatement.executeQuery()** メソッドに渡します。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-144">Delete the rows by passing the **SysDaDeleteObject** object to the **SysDaDeleteStatement.executeQuery()** method.</span></span>

<span data-ttu-id="2e4b5-145">次の例では、**intField** が偶数である行を削除します。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-145">The following example deletes rows where **intField** is an even number.</span></span>

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

## <a name="clauses"></a><span data-ttu-id="2e4b5-146">句</span><span class="sxs-lookup"><span data-stu-id="2e4b5-146">Clauses</span></span>

<span data-ttu-id="2e4b5-147">SysDa クエリは複数の句をサポートします。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-147">SysDa queries support several clauses:</span></span>

+ <span data-ttu-id="2e4b5-148">**whereClause** – **where** 句は、**SysDaQueryExpression** から継承したオブジェクトから構築されます。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-148">**whereClause** – The **where** clause is constructed from objects that inherit from **SysDaQueryExpression**.</span></span> <span data-ttu-id="2e4b5-149">例は**SysDaEqualsExpression**、**SysDaNotEqualsExpression**、**SysDaLessThanExpression**があります。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-149">Examples are **SysDaEqualsExpression**, **SysDaNotEqualsExpression**, and **SysDaLessThanExpression**.</span></span> <span data-ttu-id="2e4b5-150">完全な一覧は、アプリケーションエクスプローラーでフィルタ処理することによって確認できます。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-150">You can find the full list by filtering in Application Explorer.</span></span>
+ <span data-ttu-id="2e4b5-151">**orderByClause**</span><span class="sxs-lookup"><span data-stu-id="2e4b5-151">**orderByClause**</span></span>
+ <span data-ttu-id="2e4b5-152">**groupByClause**</span><span class="sxs-lookup"><span data-stu-id="2e4b5-152">**groupByClause**</span></span>
+ <span data-ttu-id="2e4b5-153">**joinClauseKind** 付き **joinClause**</span><span class="sxs-lookup"><span data-stu-id="2e4b5-153">**joinClause** with **joinClauseKind**</span></span>
+ <span data-ttu-id="2e4b5-154">**joinedQuery**</span><span class="sxs-lookup"><span data-stu-id="2e4b5-154">**joinedQuery**</span></span>
+ <span data-ttu-id="2e4b5-155">**settingClause**</span><span class="sxs-lookup"><span data-stu-id="2e4b5-155">**settingClause**</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="2e4b5-156">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="2e4b5-156">Troubleshooting</span></span>

<span data-ttu-id="2e4b5-157">**toString()** メソッドを、**SysDaQueryObject**、**SysDaUpdateObject**、**SysDaInsertObject**、および**SysDaQueryObject**オブジェクトに対して使用して、構築している明細書を表示できます。</span><span class="sxs-lookup"><span data-stu-id="2e4b5-157">You can use the **toString()** method on **SysDaQueryObject**, **SysDaUpdateObject**, **SysDaInsertObject**, and **SysDaQueryObject** objects to view the statement that you're building.</span></span>
