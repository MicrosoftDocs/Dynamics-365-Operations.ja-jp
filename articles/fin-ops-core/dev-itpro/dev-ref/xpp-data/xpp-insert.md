---
title: データの挿入
description: このトピックでは、X++ を使用してテーブルにデータを挿入する方法について説明します。
author: robinarh
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 150273
ms.search.region: Global
ms.author: rhaertle
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 6f454e842695de81828ab5894f0bc751d351cb09
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749962"
---
# <a name="insert-data"></a>データの挿入

[!include [banner](../../includes/banner.md)]

データベースに格納されているテーブルに 1 つまたは複数の行を挿入するため、SQL ステートメントを対話的またはソース コード内で使用することができます。

+ **[insert メソッド](#insert-method)** – 一度に 1 行を挿入します。
+ **[doInsert メソッド](#do-insert-method)** – 一度に 1 行を挿入します。
+ **[insert\_recordset ステートメント](#insert-recordset-statement)** – 複数のレコードを 1 つまたは複数のテーブルから別のテーブルに 1 回のデータベース トリップで直接コピーします。
+ **[RecordInsertList.insertDatabase](../system-classes/recordinsertlist-class.md#method-insertdatabase)** – 1 回のデータベース トリップで複数の行を同時に挿入します。 データをソートする必要がない場合は、この構文を使用します。
+ **[RecordSortedList.insertDatabase](../system-classes/recordsortedlist-class.md#method-insertdatabase)** – 1 回のデータベース トリップで複数の行を同時に挿入します。 特定のテーブルのデータのサブセットを必要とし、現在インデックスとして存在しない順序でソートする場合は、このコンストラクトを使用します

**RecordSortedList**、**RecordInsertList**、および **insert\_recordset** を使用すると、複数のレコードを挿入できます。 これらのメソッドを使用することにより、アプリケーションとデータベース間の通信が減少します。 したがって、パフォーマンスの向上に役立ちます。 場合によっては、レコードのセットに基づく操作をレコードごとの操作に戻すことができます。 詳細については、[セット ベースからレコード単位への操作の変換](xpp-data-perf.md)を参照してください。

## <a name="insert-method"></a><a id="insert-method"></a>insert メソッド

**insert** メソッドは、一度に 1 つのレコードを挿入します。 **RecId** フィールドおよびシステム フィールドの値を生成し、バッファーの内容 (つまり、列の値) をデータベースに挿入します。

+ **insert** メソッドを呼び出す前に、テーブル変数で **select** ステートメントを使用しないでください。
+ **insert** メソッドでは、すべての主要なフィールド要件とテーブルの依存関係を処理するわけではありません。 それらの処理を行うには、コードを記述する必要があります。

**挿入** メソッドが作用する方法を次に示します。

+ クエリによって選択されている行の指定された列のみ、名前付きテーブルに挿入されます。
+ コピー元のテーブルの列とコピー先のテーブルの列は、互換性のある型であることが必要です。
+ 両方のテーブルの列がタイプおよび順序において一致する場合、列リストは **挿入** 句から省略されます。

次の例では、新しいレコードを CustGroup テーブルに挿入します。 新しいレコードの **CustGroup** 列は **41** に設定されています。 レコードの他のフィールドは空白になります。

```xpp
CustGroup custGroup;
ttsBegin;
    custGroup.CustGroup = '41';
    custGroup.insert();
ttsCommit;
```

**insert** メソッドの動作を上書きするには、**[doInsert](#do-insert-method)** メソッドを使用します。

## <a name="doinsert-method"></a><a id="do-insert-method"></a>doInsert メソッド

**doInsert** メソッドは、**RecId** フィールドおよびその他のシステム フィールドの値を生成した後、データベースにバッファーの内容を挿入します。 テーブルの **insert** メソッドをバイパスする必要がある場合は、このメソッドを使用します。

> [!WARNING]
> **doInsert** の呼び出しは、データベース イベント ハンドラー (たとえば **oninserting** および **oninserted**)、コマンド チェーン **onInsert()**、および **insert()** の呼び出し自体を含むすべてのロジックをスキップします。 一般に、**doInsert** を使用することは不適切なプラクティスと見なされており、使用することはお勧めしません。

## <a name="insert_recordset-statement"></a><a id="insert-recordset-statement"></a>insert\_recordset ステートメント

**insert\_recordset** ステートメントは、1 回のサーバー トリップで、1 つ以上のソース テーブルからデータを直接 1 つのターゲット テーブルにコピーします。 配列挿入 (**RecordInsertList.insertDatabase** または **RecordSortedList.insertDatabase**) より **insert\_recordset** を使用する方が高速です。 ただし、配列挿入は、データを挿入する前に処理する場合より柔軟になります。 **insert\_recordset** は、一度に複数のレコードに対して操作を実行するレコード セット ベースの演算子ですが、多くの場合、レコードごとの操作に戻すことができます。 詳細については、[セット ベースからレコード単位への操作の変換](xpp-data-perf.md)を参照してください。

次の **insert\_recordset** ステートメントの構文では、かっこ (\[\]) はステートメントのオプションの要素を示します。

**insert\_recordset** *DestinationTable* **(** *ListOfFields* **)**

**select** *ListOfFields1* **from** *SourceTable* **\[ where** *WhereClause* **\]** 

**\[ join** *ListOfFields2* **from** *JoinedSourceTable* **\[ where** *JoinedWhereClause* **\]\]**

+ *ListOfFields* 出力先テーブルは、ソース テーブル内のフィールドのリストと一致する必要があります。 データは、フィールドの一覧に表示されている順に転送されます。 フィールドの一覧に表示されていない出力先テーブルのフィールドは、他の領域と同じように、**0** (ゼロ) の値に割り当てられています。 **RecId** などのシステム フィールドは、出力先テーブルのカーネルによって透過的に割り当てられます。
+ *WhereClause* および *JoinedWhereClause* は、**[select](xpp-select-statement.md#where-keyword)** ステートメントの *WhereClause* 句で説明されています。

### <a name="insert_recordset-inserting-data-from-another-table"></a>insert\_recordset: 別のテーブルからのデータの挿入

この例では、NameValuePair テーブルの **値** 列は **名前** 値ごとに合計されます。 集計の結果は、ValueSumByName テーブルに格納されます。

```xpp
ValueSumByName valueSumName;
NameValuePair nameValuePair;

insert_recordset valueSumName (Name, ValueSum)
    select Name, sum(Value)
    from nameValuePair
    group by Name;
```

### <a name="insert_recordset-inserting-data-from-variables"></a>insert\_recordset: 変数からのデータの挿入

次の例は、**insert\_recordset** ステートメントが変数データを挿入できることを示しています。

- 1 つの新しいレコードだけを挿入する場合は、**firstonly** キーワードを含めます。 **firstonly** を省略すると CustTable テーブルの各レコードに対してレコードが挿入されます。
- **128** または **"このリテラル文字列"** などのリテラルは、挿入されたデータのソースとしてクエリで使用できません。
- ソース テーブルの列は、ターゲット テーブルに対応している必要はありません。

この例では、NameValuePair テーブルに 1 つの新しいレコードが挿入されます。 このレコードの **ID** 値は **1**、**名前** の値は **Name1**、**値** の値は **1** です。

```X++
NameValuePair nameValuePair;
CustTable custTable;

int id_var = 1;
str name_var = 'Name1';
int value_var = 1;

insert_recordset nameValuePair (Id, Name, Value)
select firstonly id_var, name_var, value_var from custTable;
```

### <a name="insert_recordset-inserting-data-by-using-a-join"></a>insert\_recordset: 結合を使用してデータを挿入する

次の例は、サブセレクトを持つ **insert\_recordset** ステートメント上の 3 つのテーブルの結合を示しています。 また、同じ結合がある **while select** ステートメントも示しています。 変数は、1 つの列に挿入された値を供給するために使用されます。 **str** 変数は、宣言する必要があり、対応するデータベース フィールドの最大長さ以下の長さである必要があります。

この例では、tabEmplProj5 テーブルに対する **insert\_recordset** ステートメントがあります。 ターゲット フィールドの 1 つに **説明** という名前が付けられ、そのデータはローカル **sDescriptionVariable** 変数から取得されます。 **説明** フィールドの構成キーは無効の場合でも **insert\_recordset** ステートメントは成功します。 システムでは、**Description** フィールドと **sDescriptionVariable** 変数の両方を無視します。 したがって、このコードは *コンフィギュレーション キーの自動化* の例を提供します。 コンフィギュレーション キーの自動化は、コンフィギュレーション キーがオフになっているフィールドにデータを挿入する **insert\_ recordset** ステートメントの動作を、システムが自動的に調整できるときに発生します。

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

## <a name="handling-duplicatekeyexception-exceptions"></a>DuplicateKeyException 例外の処理

次の例は、明示的なトランザクションのコンテキストで **DuplicateKeyException** 例外をキャッチする方法を示しています。 キー値が既に存在しているため、**xRecord.insert** の呼び出しが失敗した場合に例外がスローされます。 **catch** ブロックでは、コードで修正アクションを実行するか、後で分析するためにエラーを記録したりできます。 これにより、トランザクションの保留中のすべての作業が失うことなく、コードの実行を続けることできます。 **insert\_recordset** などのセット ベース操作によって発生する **DuplicateKeyException** 例外を把握することはできません。

この例は、SourceTable および DestinationTable という 2 つのテーブルによって異なります。 各テーブルには 1 つの必須の整数フィールドがあります。 フィールドの名前はそれぞれ、**SourceKeyField** および **DestinationKeyField** です。 固有インデックスは、各キー フィールドで定義されます。 SourceTable テーブルには、少なくとも 1 つのレコードが必要です。

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]