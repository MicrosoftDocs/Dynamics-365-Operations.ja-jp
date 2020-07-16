---
title: データの挿入
description: このトピックでは、X++ を使用してテーブルにデータを挿入する方法について説明します。
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
ms.openlocfilehash: 2da19977e00a414cb3d15efaf4874ea910101e89
ms.sourcegitcommit: 4ba6817b7aa7735a291a021022b4c12c2de5f2eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/26/2020
ms.locfileid: "3505950"
---
# <a name="insert-data"></a><span data-ttu-id="f72f8-103">データの挿入</span><span class="sxs-lookup"><span data-stu-id="f72f8-103">Insert data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f72f8-104">データベースに格納されているテーブルに一つまたは複数の行を挿入するため、SQL ステートメントを対話的またはソース コード内で使用することができます。</span><span class="sxs-lookup"><span data-stu-id="f72f8-104">You can use SQL statements, either interactively or within source code, to insert one or more rows into tables stored in the database.</span></span>

+ <span data-ttu-id="f72f8-105">**[insert メソッド](#insert-method)**: 一度に 1 行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="f72f8-105">**[insert method](#insert-method)**: Inserts one row at a time.</span></span>
+ <span data-ttu-id="f72f8-106">**[doInsert メソッド](#do-insert-method)**: 一度に 1 行を挿入します。</span><span class="sxs-lookup"><span data-stu-id="f72f8-106">**[doInsert method](#do-insert-method)**: Inserts one row at a time.</span></span>
+ <span data-ttu-id="f72f8-107">**[insert\_recordset ステートメント](#insert-recordset-statement)**: 複数のレコードを 1 つまたは複数のテーブルから別のテーブルに 1 回のデータベース トリップで直接コピーします。</span><span class="sxs-lookup"><span data-stu-id="f72f8-107">**[insert\_recordset statement](#insert-recordset-statement)**: Copies multiple records directly from one or more tables into another table in one database trip.</span></span>
+ <span data-ttu-id="f72f8-108">**[RecordInsertList: insertDatabase](../system-classes/recordinsertlist-class.md#method-insertdatabase)**: 1 回のデータベース トリップで複数の行を同時に挿入します。</span><span class="sxs-lookup"><span data-stu-id="f72f8-108">**[RecordInsertList.insertDatabase](../system-classes/recordinsertlist-class.md#method-insertdatabase)**: Inserts multiple rows at the same time in one database trip.</span></span> <span data-ttu-id="f72f8-109">データをソートする必要がない場合は、この構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="f72f8-109">Use this construct when you don't have to sort the data.</span></span>
+ <span data-ttu-id="f72f8-110">**[RecordSortedList.insertDatabase](../system-classes/recordsortedlist-class.md#method-insertdatabase)**: 1 回のデータベース トリップで複数の行を同時に挿入します。</span><span class="sxs-lookup"><span data-stu-id="f72f8-110">**[RecordSortedList.insertDatabase](../system-classes/recordsortedlist-class.md#method-insertdatabase)**: Inserts multiple rows at the same time in one database trip.</span></span> <span data-ttu-id="f72f8-111">特定のテーブルのデータのサブセットを必要とし、現在インデックスとして存在しない順序でソートする場合は、このコンストラクトを使用します</span><span class="sxs-lookup"><span data-stu-id="f72f8-111">Use this construct when you want a subset of data from a specific table, and you want that data to be sorted in an order that doesn't currently exist as an index.</span></span>

<span data-ttu-id="f72f8-112">**RecordSortedList**、**RecordInsertList**、および **insert\_recordset** を使用すると、複数のレコードを挿入できます。</span><span class="sxs-lookup"><span data-stu-id="f72f8-112">**RecordSortedList**, **RecordInsertList**, and **insert\_recordset** let you insert multiple records.</span></span> <span data-ttu-id="f72f8-113">これらのメソッドを使用することにより、アプリケーションとデータベース間の通信が減少するためパフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="f72f8-113">By using these methods, you reduce communication between the application and the database, and therefore help increase performance.</span></span> <span data-ttu-id="f72f8-114">場合によっては、レコードのセットに基づく操作をレコードごとの操作に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="f72f8-114">In some situations, record set–based operations can fall back to record-by-record operations.</span></span> <span data-ttu-id="f72f8-115">詳細については、[セット ベースからレコード単位への操作の変換](xpp-data-perf.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f72f8-115">For more information, see [Conversion of operations from set-based to record-by-record](xpp-data-perf.md).</span></span>

## <a name="insert-method"></a><a id="insert-method"></a><span data-ttu-id="f72f8-116">insert メソッド</span><span class="sxs-lookup"><span data-stu-id="f72f8-116">insert method</span></span>

<span data-ttu-id="f72f8-117">**insert** メソッドは、一度に 1 つのレコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="f72f8-117">The **insert** method inserts one record at a time.</span></span> <span data-ttu-id="f72f8-118">メソッドは、**RecId** フィールドおよびシステム フィールドの値を生成した後、データベースにバッファーの内容 (列の値) を挿入します。</span><span class="sxs-lookup"><span data-stu-id="f72f8-118">The method generates values for the **RecId** field and system fields, and then inserts the contents of the buffer (the column values) into the database.</span></span>

+ <span data-ttu-id="f72f8-119">**insert** メソッドを呼び出す前に、テーブル変数で **select** ステートメントを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="f72f8-119">Do not use a **select** statement on the table variable before you call the **insert** method.</span></span>
+ <span data-ttu-id="f72f8-120">**insert** メソッドでは、主要なフィールド要件とテーブルの依存関係がすべて処理されることはありません。</span><span class="sxs-lookup"><span data-stu-id="f72f8-120">The **insert** method does not handle all of the key field requirements and table dependencies.</span></span> <span data-ttu-id="f72f8-121">この処理を行うには、コードを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f72f8-121">You must write code to handle that.</span></span>

<span data-ttu-id="f72f8-122">**挿入**メソッドが作用する方法を次に示します。</span><span class="sxs-lookup"><span data-stu-id="f72f8-122">Here is how the **insert** method works:</span></span>

+ <span data-ttu-id="f72f8-123">クエリによって選択されている行の指定された列のみ、名前付きテーブルに挿入されます。</span><span class="sxs-lookup"><span data-stu-id="f72f8-123">Only the specified columns of the rows that have been selected by the query are inserted into the named table.</span></span>
+ <span data-ttu-id="f72f8-124">コピー元のテーブルの列とコピー先のテーブルの列は、互換性のある型であることが必要です。</span><span class="sxs-lookup"><span data-stu-id="f72f8-124">The columns of the table that is copied from and the columns of the table that is copied to must be type-compatible.</span></span>
+ <span data-ttu-id="f72f8-125">両方のテーブルの列がタイプおよび順序において一致する場合、列リストは**挿入**句から省略されます。</span><span class="sxs-lookup"><span data-stu-id="f72f8-125">If the columns of both tables match in type and order, column list can be omitted from the **insert** clause.</span></span>

<span data-ttu-id="f72f8-126">次の例では、新しいレコードを **CustGroup** テーブルに挿入します。</span><span class="sxs-lookup"><span data-stu-id="f72f8-126">The following example inserts a new record into the **CustGroup** table.</span></span> <span data-ttu-id="f72f8-127">新しいレコードの **CustGroup** 列は **41** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="f72f8-127">The **CustGroup** column of the new record is set to **41**.</span></span> <span data-ttu-id="f72f8-128">レコードの他のフィールドは空白になります。</span><span class="sxs-lookup"><span data-stu-id="f72f8-128">Other fields in the record will be blank.</span></span>

```xpp
CustGroup custGroup;
ttsBegin;
    custGroup.CustGroup = '41';
    custGroup.insert();
ttsCommit;
```

<span data-ttu-id="f72f8-129">**insert** メソッドの動作を上書きするには、[**doInsert**](#do-insert-method) メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f72f8-129">To override the behavior of the **insert** method, use the [**doInsert**](#do-insert-method) method.</span></span>

## <a name="doinsert-method"></a><a id="do-insert-method"></a><span data-ttu-id="f72f8-130">doInsert メソッド</span><span class="sxs-lookup"><span data-stu-id="f72f8-130">doInsert method</span></span>

<span data-ttu-id="f72f8-131">**doInsert** メソッドは、**RecId** フィールドおよびその他のシステム フィールドの値を生成した後、データベースにバッファーの内容を挿入します。</span><span class="sxs-lookup"><span data-stu-id="f72f8-131">The **doInsert** method generates values for the **RecId** field and other system fields, and then inserts the contents of the buffer into the database.</span></span> <span data-ttu-id="f72f8-132">テーブルの **insert** メソッドをバイパスする必要がある場合は、このメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f72f8-132">Use this method when the **insert** method on the table must be bypassed.</span></span> 

> [!WARNING]
> <span data-ttu-id="f72f8-133">**doInsert** の呼び出しは 、データベース イベント ハンドラー (たとえば **oninserting** および **oninserted**)、コマンド チェーン **onInsert()**、および **insert()** の呼び出し自体を含むすべてのロジックをスキップします。</span><span class="sxs-lookup"><span data-stu-id="f72f8-133">Calling **doInsert** skips all logic, including database event handlers (for example **oninserting** and  **oninserted**), chain-of-command  **onInsert()**, and the **insert()** call itself.</span></span> <span data-ttu-id="f72f8-134">一般に、**doInsert** を使用することは不適切なプラクティスと見なされ、お勧めできません。</span><span class="sxs-lookup"><span data-stu-id="f72f8-134">It's generally considered bad practice to use **doInsert** and it's not recommended.</span></span>

## <a name="insert_recordset-statement"></a><a id="insert-recordset-statement"></a><span data-ttu-id="f72f8-135">insert\_recordset ステートメント</span><span class="sxs-lookup"><span data-stu-id="f72f8-135">insert\_recordset statement</span></span>

<span data-ttu-id="f72f8-136">**insert\_recordset** ステートメントは、1 回のサーバー トリップで、1 つ以上のソース テーブルからデータを直接 1 つのターゲット テーブルにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f72f8-136">The **insert\_recordset** statement copies data directly from one or more source tables into one destination table in one server trip.</span></span> <span data-ttu-id="f72f8-137">配列挿入 (**RecordInsertList.insertDatabase** または **RecordSortedList.insertDatabase**) より **insert\_recordset** を使用する方が高速です。</span><span class="sxs-lookup"><span data-stu-id="f72f8-137">It's faster to use **insert\_recordset** than an array insert (**RecordInsertList.insertDatabase** or **RecordSortedList.insertDatabase**).</span></span> <span data-ttu-id="f72f8-138">ただし、配列挿入は、データを挿入する前に処理する場合より柔軟になります。</span><span class="sxs-lookup"><span data-stu-id="f72f8-138">However, array inserts are more flexible if you want to handle the data before you insert it.</span></span> <span data-ttu-id="f72f8-139">**insert\_recordset** は、一度に複数のレコードに対して操作を実行するレコード セット ベースの演算子ですが、多くの場合、レコードごとの操作に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="f72f8-139">Although **insert\_recordset** is a record set–based operator that performs operations on multiple records at a time, it can fall back to record-by-record operations in many situations.</span></span> <span data-ttu-id="f72f8-140">詳細については、[セット ベースからレコード単位への操作の変換](xpp-data-perf.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f72f8-140">For more information, see [Conversion of operations from set-based to record-by-record](xpp-data-perf.md).</span></span>

<span data-ttu-id="f72f8-141">**insert\_recordset** ステートメントの次の構文では、**\[\]** はステートメントのオプション要素を示します。</span><span class="sxs-lookup"><span data-stu-id="f72f8-141">In the following syntax for the **insert\_recordset** statement, **\[\]** indicates optional elements of the statement.</span></span>

<span data-ttu-id="f72f8-142">**insert\_recordset** *DestinationTable* **(** *ListOfFields* **)**</span><span class="sxs-lookup"><span data-stu-id="f72f8-142">**insert\_recordset** *DestinationTable* **(** *ListOfFields* **)**</span></span>

<span data-ttu-id="f72f8-143">**select** *ListOfFields1* **from** *SourceTable* **\[ where** *WhereClause* **\]**</span><span class="sxs-lookup"><span data-stu-id="f72f8-143">**select** *ListOfFields1* **from** *SourceTable* **\[ where** *WhereClause* **\]**</span></span> 

<span data-ttu-id="f72f8-144">**\[ join** *ListOfFields2* **from** *JoinedSourceTable* **\[ where** *JoinedWhereClause* **\]\]**</span><span class="sxs-lookup"><span data-stu-id="f72f8-144">**\[ join** *ListOfFields2* **from** *JoinedSourceTable* **\[ where** *JoinedWhereClause* **\]\]**</span></span>

+ <span data-ttu-id="f72f8-145">*ListOfFields* 出力先テーブルは、ソース テーブル内のフィールドのリストと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f72f8-145">*ListOfFields* in the destination table must match the list of fields in the source tables.</span></span> <span data-ttu-id="f72f8-146">データは、フィールドの一覧に表示されている順に転送されます。</span><span class="sxs-lookup"><span data-stu-id="f72f8-146">Data is transferred in the order in which it appears in the list of fields.</span></span> <span data-ttu-id="f72f8-147">フィールドの一覧に表示されていない出力先テーブルのフィールドは、他の領域と同じように、**0** (ゼロ) の値に割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="f72f8-147">Fields in the destination table that aren't present in the list of fields are assigned **0** (zero) values, as in other areas.</span></span> <span data-ttu-id="f72f8-148">**RecId** などのシステム フィールドは、出力先テーブルのカーネルによって透過的に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="f72f8-148">System fields, such as **RecId**, are assigned transparently by the kernel in the destination table.</span></span>
+ <span data-ttu-id="f72f8-149">*WhereClause* および *JoinedWhereClause* は、[**select** ステートメント](xpp-select-statement.md#where-keyword)の *WhereClause* で記述されます。</span><span class="sxs-lookup"><span data-stu-id="f72f8-149">*WhereClause* and *JoinedWhereClause* are described in the *WhereClause* in the [**select** statement](xpp-select-statement.md#where-keyword).</span></span>

## <a name="insert_recordset-insert-data-from-another-table"></a><span data-ttu-id="f72f8-150">insert\_recordset: 別のテーブルからデータを挿入</span><span class="sxs-lookup"><span data-stu-id="f72f8-150">insert\_recordset: insert data from another table</span></span>

<span data-ttu-id="f72f8-151">この例では、**NameValuePair** テーブルの**値**列は、**名前**値ごとに合計されます。</span><span class="sxs-lookup"><span data-stu-id="f72f8-151">In this example, the **Value** column in the **NameValuePair** table is summed for each **Name** value.</span></span> <span data-ttu-id="f72f8-152">集計の結果は、**ValueSumByName** テーブルに格納されます。</span><span class="sxs-lookup"><span data-stu-id="f72f8-152">The results of the aggregation are stored in the **ValueSumByName** table.</span></span>

```xpp
ValueSumByName valueSumName;
NameValuePair nameValuePair;

insert_recordset valueSumName (Name, ValueSum)
    select Name, sum(Value)
    from nameValuePair
    group by Name;
```

## <a name="insert_recordset-insert-data-from-variables"></a><span data-ttu-id="f72f8-153">insert\_recordset: 変数からデータを挿入</span><span class="sxs-lookup"><span data-stu-id="f72f8-153">insert\_recordset: insert data from variables</span></span>

<span data-ttu-id="f72f8-154">次の例は、**insert\_recordset** ステートメントが変数データを挿入できることを示しています。</span><span class="sxs-lookup"><span data-stu-id="f72f8-154">The following example shows that the **insert\_recordset** statement can insert variable data.</span></span>

- <span data-ttu-id="f72f8-155">1 つの新しいレコードだけを挿入する場合は、**firstonly** キーワードを含めます。</span><span class="sxs-lookup"><span data-stu-id="f72f8-155">Include the **firstonly** keyword to insert only one new record.</span></span> <span data-ttu-id="f72f8-156">**firstonly** を省略すると、**CustTable** の各レコードに対してレコードが挿入されます。</span><span class="sxs-lookup"><span data-stu-id="f72f8-156">If you omit **firstonly**, then a record is inserted for each record in **CustTable**.</span></span>  
- <span data-ttu-id="f72f8-157">**128** または **"このリテラル文字列"** などのリテラルは、挿入されたデータのソースとしてクエリで使用できません。</span><span class="sxs-lookup"><span data-stu-id="f72f8-157">Literals, such as **128** or **"this literal string"**, can't be used in the query as a source of data that is inserted.</span></span>
- <span data-ttu-id="f72f8-158">ソース テーブルの列は、ターゲット テーブルに対応している必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f72f8-158">The columns in the source table do not have to correspond to the target table.</span></span>

<span data-ttu-id="f72f8-159">次の例では、**NameValuePair** テーブルに 1 つの新しいレコードが挿入され、**Id** が **1**、**名前**が **Name1**、**値**が **1** となります。</span><span class="sxs-lookup"><span data-stu-id="f72f8-159">In the following example, one new record is inserted in the **NameValuePair** table, with **Id** of **1**, **Name** of **Name1**, and **Value** of **1**.</span></span>

```X++
NameValuePair nameValuePair;
CustTable custTable;

int id_var = 1;
str name_var = 'Name1';
int value_var = 1;

insert_recordset nameValuePair (Id, Name, Value)
select firstonly id_var, name_var, value_var from custTable;
```

## <a name="insert_recordset-insert-data-by-using-a-join"></a><span data-ttu-id="f72f8-160">insert\_recordset: 結合を使用してデータを挿入</span><span class="sxs-lookup"><span data-stu-id="f72f8-160">insert\_recordset: insert data by using a join</span></span>

<span data-ttu-id="f72f8-161">次の例は、サブセレクトを持つ **insert\_recordset** ステートメント上の 3 つのテーブルの結合を示しています。</span><span class="sxs-lookup"><span data-stu-id="f72f8-161">The following example shows a join of three tables on an **insert\_recordset** statement that has a subselect.</span></span> <span data-ttu-id="f72f8-162">また、同じ結合がある **while select** ステートメントも示しています。</span><span class="sxs-lookup"><span data-stu-id="f72f8-162">It also shows a **while select** statement that has a similar join.</span></span> <span data-ttu-id="f72f8-163">変数は、1 つの列に挿入された値を供給するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f72f8-163">A variable is used to supply the inserted value for one column.</span></span> <span data-ttu-id="f72f8-164">**str** 変数は、宣言する必要があり、長さを対応するデータベース フィールドの最大長さ以下にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f72f8-164">The **str** variable must be declared, and must have a length that is less than or equal to the maximum length of the corresponding database field.</span></span> <span data-ttu-id="f72f8-165">この例では、tabEmplProj5 テーブルに対する **insert\_recordset** ステートメントがあります。</span><span class="sxs-lookup"><span data-stu-id="f72f8-165">In this example, there is an **insert\_recordset** statement for the tabEmplProj5 table.</span></span> <span data-ttu-id="f72f8-166">ターゲット フィールドの 1 つに**説明**という名前が付けられ、フィールドのデータはローカル変数 **sDescriptionVariable** から取得されます。</span><span class="sxs-lookup"><span data-stu-id="f72f8-166">One of the target fields is named **Description**, and the field's data comes from the local variable **sDescriptionVariable**.</span></span> <span data-ttu-id="f72f8-167">**説明** フィールドの構成キーは無効の場合でも **insert\_recordset** ステートメントは成功します。</span><span class="sxs-lookup"><span data-stu-id="f72f8-167">The **insert\_recordset** statement succeeds even when the configuration key for the **Description** field is turned off.</span></span> <span data-ttu-id="f72f8-168">システムでは、**Description** フィールドと **sDescriptionVariable** 変数の両方を無視します。</span><span class="sxs-lookup"><span data-stu-id="f72f8-168">The system ignores both the **Description** field and the **sDescriptionVariable** variable.</span></span> <span data-ttu-id="f72f8-169">したがって、このコードは*コンフィギュレーション キーの自動化*の例を提供します。</span><span class="sxs-lookup"><span data-stu-id="f72f8-169">Therefore, this code provides an example of *configuration key automation*.</span></span> <span data-ttu-id="f72f8-170">コンフィギュレーション キーの自動化は、コンフィギュレーション キーがオフになっているフィールドにデータを挿入する **insert\_ recordset** ステートメントの動作を、システムが自動的に調整できるときに発生します。</span><span class="sxs-lookup"><span data-stu-id="f72f8-170">Configuration key automation occurs when the system can automatically adjust the behavior of an **insert\_recordset** statement that inserts data into fields that the configuration key is turned off for.</span></span>

```X++
static void InsertJoin42Job(Args _args)
{
    GmTabDepartment tabDept2;
    GmTabEmployee tabEmpl3;
    GmTabProject tabProj4;
    GmTabEmployeeProject tabEmplProj5;
    str 64 sDescriptionVariable = "From variable.";
    DELETE_FROM tabEmplProj5;
    INSERT_RECORDSET tabEmplProj5
        (
        Description
        , EmployeeRecId
        , ProjectRecId
        )
    Select
        sDescriptionVariable
        , RecId
    from
        tabEmpl3
        join
            tabDept2
            where tabEmpl3 .DepartmentGuid == tabDept2 .DepartmentGuid
        join RecId
            from tabProj4
            where tabDept2 .DepartmentGuid == tabProj4 .DepartmentGuid
    info(int642str(tabEmplProj5 .rowCount())
        + " ==Number of rows inserted.");
    WHILE SELECT *
        from
            tabEmplProj5
            join tabEmpl3
                where tabEmplProj5 .EmployeeRecId == tabEmpl3 .RecId
            join tabProj4
                where tabEmplProj5 .ProjectRecId == tabProj4 .RecId
    {
        info(
            tabEmpl3 .EmployeeName
            + "  --works on--  "
            + tabProj4 .ProjectName
            + " (" + tabEmplProj5 .Description + ")."
            );
    }

/*****************  Actual Infolog output
Message (01:05:41 pm)
4 ==Number of rows inserted.
Alice  --works on--  Project ZZZ (From variable.).
Alice  --works on--  Project YY (From variable.).
Beth  --works on--  Project ZZZ (From variable.).
Beth  --works on--  Project YY (From variable.).
*****************/
}
```

## <a name="handle-a-duplicatekeyexception"></a><span data-ttu-id="f72f8-171">DuplicateKeyException の処理</span><span class="sxs-lookup"><span data-stu-id="f72f8-171">Handle a DuplicateKeyException</span></span>

<span data-ttu-id="f72f8-172">次の例は、明示的なトランザクションのコンテキストで **DuplicateKeyException** 例外をキャッチする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="f72f8-172">The following example shows how you can catch a **DuplicateKeyException** exception in the context of an explicit transaction.</span></span> <span data-ttu-id="f72f8-173">キー値が既に存在しているため、**xRecord.insert** の呼び出しが失敗した場合に例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="f72f8-173">The exception is thrown when a call to **xRecord.insert** fails because key value already exists.</span></span> <span data-ttu-id="f72f8-174">**catch** ブロックでは、コードで修正アクションを実行するか、後で分析するためにエラーを記録したりできます。</span><span class="sxs-lookup"><span data-stu-id="f72f8-174">In the **catch** block, your code can either take corrective action or log the error for later analysis.</span></span> <span data-ttu-id="f72f8-175">これにより、トランザクションの保留中のすべての作業が失うことなく、コードの実行を続けることできます。</span><span class="sxs-lookup"><span data-stu-id="f72f8-175">Your code can then continue without losing all the pending work of the transaction.</span></span> <span data-ttu-id="f72f8-176">**挿入\_レコードセット** などのセットに基づく操作によって発生する重複キー例外を把握することはできません。</span><span class="sxs-lookup"><span data-stu-id="f72f8-176">You can't catch a duplicate key exception that is caused by a set-based operation such as **insert\_recordset**.</span></span> <span data-ttu-id="f72f8-177">この例は、**SourceTable** および **DestinationTable** という 2 つのテーブルによって異なります。</span><span class="sxs-lookup"><span data-stu-id="f72f8-177">This example depends on two tables: **SourceTable** and **DestinationTable**.</span></span> <span data-ttu-id="f72f8-178">両方のテーブルには 1 つの必須の整数フィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="f72f8-178">Both tables have one mandatory integer field.</span></span> <span data-ttu-id="f72f8-179">これらのフィールドはそれぞれ、**SourceKeyField** および **DestinationKeyField** という名前が付けられます。</span><span class="sxs-lookup"><span data-stu-id="f72f8-179">These fields are named **SourceKeyField** and **DestinationKeyField**, respectively.</span></span> <span data-ttu-id="f72f8-180">固有インデックスは、各キー フィールドで定義されます。</span><span class="sxs-lookup"><span data-stu-id="f72f8-180">A unique index is defined on each key field.</span></span> <span data-ttu-id="f72f8-181">**SourceTable** テーブルには、少なくとも 1 つのレコードが必要です。</span><span class="sxs-lookup"><span data-stu-id="f72f8-181">The **SourceTable** table must have at least one record in it.</span></span>

```xpp
static void JobDuplicKeyException44Job(Args _args)
{
    SourceTable sourceTable; // Must have at least one record.
    DestinationTable destinationTable;
    int countTries = 0;
    int numberAdjust = 0;
    int newKey;
    int inote;
    container notes;

    // Empty the destination table.
    delete_from destinationTable;

    // Copy all the records from SourceTable to DestinationTable
    insert_recordset destinationTable (destinationKeyField)
        select SourceKeyField from sourceTable order by SourceKeyField asc;

    // Copy the records from SourceTable to DestinationTable, one at a time.
    // This immediately throws a DuplicateKeyException.
    ttsBegin;
    try
    {
        countTries++;
        notes += strFmt("Inside the try block, try count is %1.", countTries);
        while select * from sourceTable order by SourceKeyField asc
        {
            destinationTable.clear();
            newKey = sourceTable.SourceKeyField + numberAdjust;
            destinationTable.DestinationKeyField = newKey;
            notes += strFmt("%1 is the key to be tried." , newKey);
            destinationTable.insert();
            notes += "Success: .insert()";
        }
        ttsCommit;
    }
    catch (Exception::DuplicateKeyException, destinationTable) // Table is optional.
    {
        notes += "Inside the catch block.";
        notes += 'Error: ' + infolog.text().strReplace('\n', '');
        if (countTries <= 1)
        {
            notes += "Will issue retry.";
            numberAdjust = 1;
            retry; // Erases Infolog.
        }
        else
        {
            notes += "Aborting the transaction.";
            ttsAbort;
        }
    }

    for (inote = 1; inote <= conLen(notes); inote++)
    {
        info(conPeek(notes, inote));
    }
}

/* Output
    ---- Inside the try block, try count is 1.
    ---- 11 is the key to be tried.
    ---- Inside the catch block.
    Cannot create a record in DestinationTable (DestinationTable).
    The record already exists.
    ---- Will issue retry.
    ---- Inside the try block, try count is 2.
    ---- 12 is the key to be tried.
    ---- .insert() successful.
*/
```
