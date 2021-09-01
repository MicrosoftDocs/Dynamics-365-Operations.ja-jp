---
title: X++ リフレクション ランタイム関数
description: このトピックでは、リフレクション ランタイム関数について説明します。
author: RobinARH
ms.date: 06/20/2017
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cff054661928442d3f68ae581a344304d1af016d4a69db0f80089bfdbb2ff5e9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747231"
---
# <a name="x-reflection-runtime-functions"></a>X++ リフレクション ランタイム関数

[!include [banner](../includes/banner.md)]

このトピックでは、リフレクション ランタイム関数について説明します。

## <a name="classidget"></a>classIdGet

初期化されるオブジェクトが属しているクラスの数値識別子 (クラス ID) を取得します。

```xpp
int classIdGet(class object)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                         |
|-----------|-------------------------------------|
| オブジェクト    | クラス ID を取得するオブジェクト。 |

### <a name="return-value"></a>戻り値

指定されたオブジェクトのクラス ID。

### <a name="example"></a>例

```xpp
static void classIdGetExample(Args _args)
{
    int i;
    WorkTimeCheck w;

    i = classIdGet(w);
    print "Class ID for object is " + int2Str(i);
}
```

## <a name="dimof"></a>dimOf
X++ 配列内で領域が割り当てられているインデックス要素の番号を取得します。

```xpp
int dimOf(anytype object)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                   |
|-----------|-----------------------------------------------|
| オブジェクト    | 分析コード サイズを決定するための配列。 |

### <a name="return-value"></a>戻り値

*オブジェクト* パラメーターの値が配列である場合、値は配列の要素の数になります。それ以外の場合は **0** (ゼロ) になります。

### <a name="remarks"></a>備考

**dimOf** 関数は、次の X++ プリミティブ型として宣言されている X++ 配列に使用されます。

-   ブール値
-   日付
-   int
-   int64
-   real
-   utcDateTime

たとえば **int iAmounts\[6\];** です。 列挙値および拡張データ型の配列も、前述のプリミティブ データ型のいずれかに最終的に基づいている場合はサポートされています (**int** など) 。 **dimOf** 機能は、すべての X++ プリミティブ型の配列を受け入れるわけではありません。 **dimOf** 関数が受け入れない配列タイプを次に示します。

-   **str**
-   **コンテナー**
-   **anytype**
-   クラス オブジェクトの配列
-   **配列** クラスのインスタンス

### <a name="example"></a>例

```xpp
static void JobDimOfArrays(Args _args)
{
    int iAmounts[20], iCounts[];
    ABCModel enumAbcModel[22]; // Enum
    ABCModelType exdtAbcModelType[24]; // Extended data type
    anytype anyThings[26];
    str sNames[28];
    Array myArrayObj; // Class

    info("Start of job.");
    info("--(Next, normal int array, dimOf() accepts it.)");
    info(int2Str(dimOf(iAmounts)));
    info("--(Next, normal enum array, dimOf() accepts it.)");
    info(int2Str(dimOf(enumAbcModel)));
    info("--(Next, normal extended data type array (based on enum), dimOf() accepts it.)");
    info(int2Str(dimOf(exdtAbcModelType)));
    info("--(Next, dynamic int array, dimension not yet set.)");
    info(int2Str(dimOf(iCounts)));
    info("--(Next, dynamic int array, after dimension established.)");

    iCounts[13] = 13;
    info(int2Str(dimOf(iCounts)));
    info(" == == == == == (Next, array types that dimOf() does not support.)");
    info("--(Next, normal anytype array, dimOf() always returns 0.)");
    info(int2Str(dimOf(anyThings)));
    info("--(Next, an instance of class X++ Array, dimOf() always returns 0.)");

    myArrayObj = new Array(Types::Integer);
    myArrayObj.value(1,501);
    info(int2Str(dimOf(myArrayObj)));
    info("--(Next, the lastIndex method provides size information about Array instances.)");
    info(int2Str(myArrayObj.lastIndex()));
    info("--(Next, normal str array, dimOf() does not accept it, job is halted.)");
    info(int2Str(dimOf(sNames)));
    info("End of job.");

}
/************  Actual Infolog output
Message (11:10:06 am)
Start of job.
--(Next, normal int array, dimOf() accepts it.)
20
--(Next, normal enum array, dimOf() accepts it.)
22
--(Next, normal extended data type array (based on enum), dimOf() accepts it.)
24
--(Next, dynamic int array, dimension not yet set.)
0
--(Next, dynamic int array, after dimension established.)
16
== == == == == (Next, array types that dimOf() does not support.)
--(Next, normal anytype array, dimOf() always returns 0.)
0
--(Next, an instance of class X++ Array, dimOf() always returns 0.)
0
--(Next, the lastIndex method provides size information about Array instances.)
1
--(Next, normal str array, dimOf() does not accept it, job is halted.)
Error executing code: Illegal operation on this type of array. (C)JobsJobDimOfArrays - line 41
************/
/***********  Pop-up error dialog box
"Internal error number 25 in script."
This error is caused by the code line...
info(int2Str(dimOf(iCounts)));
...before iCounts was assigned at any index.
***********/
```

## <a name="fieldid2name"></a>fieldId2Name
テーブルの ID 番号とフィールドの ID 番号で指定されているフィールドの名前を表す文字列を取得します。

```xpp
str fieldId2Name(int tableid, int fieldid)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------|
| tableid   | テーブルの ID 番号。 **注記:** テーブルの ID を指定するには、**tableName2Id** 関数を使用します。 |
| fieldid   | フィールドの ID 番号。                                                                           |

### <a name="return-value"></a>戻り値

フィールドの名前。

### <a name="remarks"></a>備考

フィールド名の印刷可能なバージョンを返すには、**fieldId2PName** 関数を使用します。

### <a name="example"></a>例

次の例では、フィールド ID が 7 の Customer (CustGroup) テーブルのフィールド名に **fn** を設定しています。

```xpp
static void fieldId2NameExample(Args _arg)
{
    str fn;
    fn = fieldId2Name(tableName2Id("Customer"),7);
}
```

## <a name="fieldid2pname"></a>fieldId2PName
テーブルの ID 番号とフィールドの ID 番号で指定されているフィールドの出力可能な名前を取得します。

```xpp
str fieldId2PName(int tableid, int fieldid)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------|
| tableid   | テーブルの ID 番号。 **注記:** テーブルの ID を指定するには、**tableName2Id** 関数を使用します。 |
| fieldid   | フィールドの ID 番号。 **注記:** フィールドの ID を指定するには、**fieldName2Id** 関数を使用します。 |

### <a name="return-value"></a>戻り値

フィールドの名前。

### <a name="example"></a>例

```xpp
static void fieldId2PNameExample(Args _arg)
{
    str name;
    tableid _tableId;
    fieldid _fieldid;

    _tableId = tableName2Id("Address");
    _fieldId = fieldName2Id(_tableId, "Name");
    name = fieldId2PName(_tableId, _fieldid);
    print name;
}
```

## <a name="fieldname2id"></a>fieldName2Id
テーブルの ID 番号とフィールドの ID 番号で指定されているテーブル フィールドのフィールド ID を取得します。

```xpp
int fieldName2Id(int tableid, str fieldname)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------|
| tableid   | テーブルの ID 番号。 **注記:** テーブルの ID を指定するには、**tableName2Id** 関数を使用します。 |
| fieldname | フィールドの名前。                                                                                |

### <a name="return-value"></a>戻り値

*tableid* および *fieldname* パラメーターにより指定されているフィールドの ID。

### <a name="example"></a>例

```xpp
static void fieldName2IdExample(Args _arg)
{
    int id;

    id = fieldName2Id(tableName2Id("Address"), "Name");
    // Returns 6. Name is the 6th field in the Address table.
    print id;
}
```

## <a name="indexid2name"></a>indexId2Name
インデックスの名前を取得します。

```xpp
str indexId2Name(int tableid, int indexid)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                    |
|-----------|------------------------------------------------|
| tableid   | インデックスが属するテーブルの ID。 |
| indexid   | インデックスの ID です。                           |

### <a name="return-value"></a>戻り値

インデックスの名前。

### <a name="example"></a>例

```xpp
static void indexId2NameExample(Args _arg)
{
    str s;
    tableid id;
    indexid idx;

    id  = tableName2Id("Address");
    idx = indexName2Id(id, "AddrIdx");
    s = indexId2Name(id, idx);
    print "The result of calling indexId2Name is " + s;
}
```

## <a name="indexname2id"></a>indexName2Id
インデックスの ID を取得します。

```xpp
int indexName2Id(int tableid, str indexname)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                                    |
|-----------|------------------------------------------------|
| tableid   | インデックスが属するテーブルの ID。 |
| indexname | インデックスの名前。                         |

### <a name="return-value"></a>戻り値

インデックスの ID です。

### <a name="example"></a>例

```xpp
static void indexName2IdExample(Args _arg)
{
    indexid idx;
    tableid id;

    id  = tableName2Id("Address");
    idx = indexName2Id(id, "AddrIdx");
    print "Index ID for index name AddrIdx of table Address is " + int2Str(idx);
}
```

## <a name="tableid2name"></a>tableId2Name
テーブルの名前を含む文字列を取得します。

```xpp
str tableId2Name(int _tableid)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明          |
|-----------|----------------------|
| \_tableid | テーブルの ID。 |

### <a name="return-value"></a>戻り値

テーブルの名前。

### <a name="example"></a>例

```xpp
static void tableId2NameExample(Args _arg)
{
    str s;
    tableid id;

    // Get the ID for table name Address.
    id = tableName2Id("Address");
    print "ID for table name Address is " + int2Str(id);

    // Get the name from the table ID.
    s = tableId2Name(id);
    print "Name for table ID " + int2Str(id) + " is " + s;

    // Get the printable name from the table ID.
    s = tableId2PName(id);
    print "Printable name for table ID " + int2Str(id) + " is " + s;
}
```

## <a name="tableid2pname"></a>tableId2PName
テーブルの出力可能な名前 (ラベル) を含む文字列を取得します。

```xpp
str tableId2PName(int _fieldid)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明          |
|-----------|----------------------|
| \_fieldid | テーブルの ID。 |

### <a name="return-value"></a>戻り値

テーブルのラベル。

### <a name="example"></a>例

```xpp
static void tableId2NameExample(Args _arg)
{
    str s;
    tableid id;

    // Get the ID for table name Address.
    id = tableName2Id("Address");
    print "ID for table name Address is " + int2Str(id);

    // Get the name from the table ID.
    s = tableId2Name(id);
    print "Name for table ID " + int2Str(id) + " is " + s;

    // Get the printable name from the table ID.
    s = tableId2PName(id);
    print "Printable name for table ID " + int2Str(id) + " is " + s;
}
```

## <a name="tablename2id"></a>tableName2Id
テーブルの ID を取得します。

```xpp
int tableName2Id(str _name)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明            |
|-----------|------------------------|
| \_名前    | テーブルの名前。 |

### <a name="return-value"></a>戻り値

テーブルの ID。

### <a name="example"></a>例

```xpp
static void tableName2IdExample(Args _arg)
{
    str s;
    tableid id;

    // Get the ID for the Address table name.
    id = tableName2Id("Address");
    print "ID for the Address table name is " + int2Str(id);

    // Get the name from the table ID.
    s = tableId2Name(id);
    print "Name for table ID " + int2Str(id) + " is " + s;

    // Get the printable name from the table ID.
    s = tableId2PName(id);
    print "Printable name for table ID " + int2Str(id) + " is " + s;
}
```

## <a name="typeof"></a>typeOf
要素のタイプを取得します。

```xpp
enum typeOf(anytype _object)
```

### <a name="parameters"></a>パラメーター

| パラメーター | 説明                         |
|-----------|-------------------------------------|
| \_オブジェクト  | タイプを返す対象の要素。 |

### <a name="return-value"></a>戻り値

**タイプ** システム列挙値。

### <a name="example"></a>例

次の例では、コンテナ内の最初の要素、**c** が単一の整数を含む別のコンテナーであるかどうかをテストします。

```xpp
if(typeof(conpeek(c, 1)) != Types::Container ||
conlen(conpeek(c, 1)) != 1 ||
typeof(conpeek(conpeek(c, 1), 1)) != Types::Integer)
{
    // More code.
}
```




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]