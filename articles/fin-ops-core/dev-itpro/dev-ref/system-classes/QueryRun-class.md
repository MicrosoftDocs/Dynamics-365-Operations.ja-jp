---
title: QueryRun クラス
description: このトピックでは、QueryRun クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0cab450ce829f2ca697e1d3762da5b837ebd616
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502858"
---
# <a name="class-queryrun"></a>クラス QueryRun

[!include [banner](../../includes/banner.md)]

```xpp
class QueryRun extends ObjectRun
```

QueryRun クラスは、データベース内のテーブルをスキャンし、ユーザーによって与えられている制約を満たすレコードをフェッチして、ユーザー入力からこのような制約を収集するのに役立ちます。

## <a name="remarks"></a>備考

QueryRun オブジェクトは、データベース内のテーブルをスキャンし、ユーザーが指定した制約を満たすレコードをフェッチするために使用されます。 QueryRun オブジェクトは、ユーザーがそのような制限を入力できるように、ユーザーと通信することができます。 クエリは、レポートに表示するデータを記述してフェッチするためにレポートにより内部的に使用されます。 QueryRun オブジェクトは、クエリ オブジェクト を使用してクエリの構造を定義します (たとえば、どのテーブルを検索するか、レコードをどのように並び替えるかなど)。 QueryRun オブジェクトは、クエリの動的動作を定義しますが、クエリ オブジェクトはクエリの静的特性を定義します。

## <a name="examples"></a>例

次の例では、アプリケーション オブジェクト ツリー (AOT) での顧客という名前のクエリがあり、そこに 1 つのデータ ソース CustTable テーブルがあると見なされます。

```xpp
static void example() 
{ 
    // Create a QueryRun object from a query stored in the AOT. 
    QueryRun qr = new QueryRun ("Customer"); 
    CustTable customerRecord; 
    // Display a window enabling the user to choose which records to print. 
    if (qr.prompt()) 
    { 
        // The user clicked OK. 
        while (qr.next()) 
        { 
            // Get the fetched record. 
            CustomerRecord = qr.GetNo(1); 
            // Do something with it 
            print CustomerRecord.AccountNum; 
        } 
    } 
    else 
    { 
        // The user pressed Cancel, so do nothing. 
    } 
}
```

## <a name="methods"></a>メソッド

| 方法                                                                                                         | 説明                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean allowCheck(\[boolean value\])                                                                   |                                                                                                                                           |
| public boolean allowCrossCompany(\[boolean value\])                                                            |                                                                                                                                           |
| public boolean canPage(\[boolean skipOrderByCheck\], \[boolean throwIfNotPagable\], \[boolean isValuePaging\]) |                                                                                                                                           |
| public boolean changed(TableId table, \[int occurrence\])                                                      | QueryRun.next メソッドの最後の呼び出し以降に、指定されたデータ ソースが新しい値をフェッチしたかどうかを判断します。                     |
| public str changedBy(\[str value\])                                                                            | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                |
| public Date changedDate(\[Date value\])                                                                        | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                             |
| public boolean changedNo(int dataSourceNo)                                                                     |                                                                                                                                           |
| public str changedTime(\[str value\])                                                                          | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                             |
| public str createdBy(\[str value\])                                                                            | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                     |
| public Date creationDate(\[Date value\])                                                                       | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                  |
| public str creationTime(\[str value\])                                                                         |                                                                                                                                           |
| public str description(\[str value\])                                                                          |                                                                                                                                           |
| public boolean equal(Object obj)                                                                               | 指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。                                                                   |
| public str form(\[str value\])                                                                                 |                                                                                                                                           |
| public Common get(TableId table, \[int occurrence\])                                                           | 次のメソッドの前の呼び出しによってフェッチされたレコードを取得します。                                                                         |
| public System.Type getImpExpDataContractType()                                                                 |                                                                                                                                           |
| public Common getNo(int dataSourceNo)                                                                          | QueryRun.next メソッドの前の呼び出しによってフェッチされたレコードを取得します。                                                                |
| public boolean importable()                                                                                    |                                                                                                                                           |
| public boolean interactive(\[boolean value\])                                                                  |                                                                                                                                           |
| public boolean isPositionPagingEnabled()                                                                       |                                                                                                                                           |
| public boolean isQueryTimedout()                                                                               |                                                                                                                                           |
| public boolean isValueBasedPagingEnabled()                                                                     |                                                                                                                                           |
| public int literals(\[int value\])                                                                             |                                                                                                                                           |
| public Guid loadCsv(str fileName)                                                                              |                                                                                                                                           |
| public Guid loadXml(str fileName)                                                                              |                                                                                                                                           |
| public str name(\[str value\])                                                                                 | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public QueryRun newObject(AnyType source)                                                                      |                                                                                                                                           |
| public boolean next()                                                                                          | クエリから次のレコードを取得します。                                                                                                 |
| public int nextUniqueId(\[int value\])                                                                         |                                                                                                                                           |
| public Guid origin(\[Guid value\])                                                                             |                                                                                                                                           |
| public container pack(\[boolean doCheck\])                                                                     |                                                                                                                                           |
| public boolean prompt()                                                                                        | クエリによってフェッチするレコードを定義するためのオプションをユーザーに表示します。                                                   |
| public Query query(\[Query query\])                                                                            |                                                                                                                                           |
| public int queryType(\[int value\])                                                                            |                                                                                                                                           |
| public boolean recordLevelSecurity(\[boolean value\])                                                          |                                                                                                                                           |
| public ReportRun report()                                                                                      |                                                                                                                                           |
| public ReportRun reportRun()                                                                                   |                                                                                                                                           |
| public boolean saved()                                                                                         |                                                                                                                                           |
| public boolean saveUserSetup(\[boolean saveIt\])                                                               | ユーザー設定を保存します。                                                                                                                     |
| public boolean searchable(\[boolean value\])                                                                   |                                                                                                                                           |
| public boolean setCursor(Common record, \[int occurrence\])                                                    |                                                                                                                                           |
| public boolean setRecord(Common record, \[int occurrence\])                                                    |                                                                                                                                           |
| public str title(\[str value\])                                                                                |                                                                                                                                           |
| public str toString()                                                                                          | 現在のオブジェクトを表す文字列を返します。                                                                                      |
| public boolean userUpdate(\[boolean value\])                                                                   |                                                                                                                                           |
| public int version(\[int value\])                                                                              |                                                                                                                                           |
| ::public static int getQueryRowCount(Query query, int maxRows)                                                 |                                                                                                                                           |
| ::public static int runAndPopulate(Query sourceRuery, Common targetTable, Map queryAliasesAndTargetColumnsMap) |                                                                                                                                           |
| public void run()                                                                                              | ユーザーからクエリに関する情報を取得するために使用されるフォームを開いて、一致するレコードをフェッチします。                                  |
| public void new(AnyType source)                                                                                | Object クラスの新しいインスタンスを初期化します。                                                                                           |
| public void addPageRange(\[Int64 startingPosition\], \[Int64 numberOfRecordsToFetch\])                         |                                                                                                                                           |
| public void reset()                                                                                            |                                                                                                                                           |
| public void setImportSession(Guid importSession)                                                               |                                                                                                                                           |
| public void setQuerytimeout(int seconds, \[boolean raiseException\])                                           |                                                                                                                                           |
| public void init()                                                                                             |                                                                                                                                           |
| public void enablePositionPaging(\[boolean enabled\])                                                          |                                                                                                                                           |
| public void shred(Guid importSession)                                                                          |                                                                                                                                           |
| public void enableValueBasedPaging(\[boolean enable\])                                                         |                                                                                                                                           |
| public void bulkNext(\[boolean fetchAllData\])                                                                 |                                                                                                                                           |
| public void applyValueBasedPaging(\[Common sourceCursor\], \[boolean isForward\])                              |                                                                                                                                           |

## <a name="method-allowcheck"></a>メソッド allowCheck

```xpp
public boolean allowCheck([boolean value])
```

### <a name="parameters---allowcheck"></a>パラメーター - allowCheck

値  

### <a name="return-value---allowcheck"></a>戻り値 - allowCheck

## <a name="method-allowcrosscompany"></a>メソッド allowCrossCompany

```xpp
public boolean allowCrossCompany([boolean value])
```

### <a name="parameters---allowcrosscompany"></a>パラメーター - allowCrossCompany

値  

### <a name="return-value---allowcrosscompany"></a>戻り値 - allowCrossCompany

## <a name="method-canpage"></a>メソッド canPage

```xpp
public boolean canPage([boolean skipOrderByCheck], [boolean throwIfNotPagable], [boolean isValuePaging])
```

### <a name="parameters---canpage"></a>パラメーター - canPage

skipOrderByCheck  

<!-- -->

throwIfNotPagable  

<!-- -->

isValuePaging  

### <a name="return-value---canpage"></a>戻り値 - canPage

## <a name="method-changed"></a>メソッド changed

QueryRun.next メソッドの最後の呼び出し以降に、指定されたデータ ソースが新しい値をフェッチしたかどうかを判断します。

```xpp
public boolean changed(TableId table, [int occurrence])
```

### <a name="parameters---changed"></a>パラメーター - changed

テーブル  
確認するデータソース (オプション)。 1 つ以上のデータ ソースが指定されたテーブルに割り当てられている場合、この引数が確認するデータ ソースを決定するために使用できます。

<!-- -->

occurrence  
確認するデータソース (オプション)。 1 つ以上のデータ ソースが指定されたテーブルに割り当てられている場合、この引数が確認するデータ ソースを決定するために使用できます。

### <a name="return-value---changed"></a>戻り値 - changed

QueryRun.next に対する最後の呼び出し後に指定データ ソースが変更された場合は true。それ以外の場合は、false。

### <a name="remarks---changed"></a>備考 - changed

このメソッドは、データ ソースが階層構造になっている場合に便利です。 埋め込みデータ ソースは、何回でも変更できます (顧客トランザクションなど)。 これは、埋め込まれていないデータソース (顧客テーブルなど) が新しいレコード (別の顧客) をフェッチするたびに発生します。 この関数の代わりに changedNo メソッドを使用できます。

## <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a>パラメーター - changedBy

値  

### <a name="return-value---changedby"></a>戻り値 - changedBy

ユーザーの名前。

## <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a>パラメーター - changedDate

値  

### <a name="return-value---changeddate"></a>戻り値 - changedDate

アプリケーション オブジェクトが最後に変更された日付。

## <a name="method-changedno"></a>メソッド changedNo

```xpp
public boolean changedNo(int dataSourceNo)
```

### <a name="parameters---changedno"></a>パラメーター - changedNo

dataSourceNo  

### <a name="return-value---changedno"></a>戻り値 - changedNo

## <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a>パラメーター - changedTime

値  

### <a name="return-value---changedtime"></a>戻り値 - changedTime

アプリケーション オブジェクトが最後に変更された時間。

## <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a>パラメーター - createdBy

値  

### <a name="return-value---createdby"></a>戻り値 - createdBy

ユーザーの名前。

## <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a>パラメーター - creationDate

値  

### <a name="return-value---creationdate"></a>戻り値 - creationDate

アプリケーション オブジェクトが作成された日付。

## <a name="method-creationtime"></a>メソッド creationTime

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a>パラメーター - creationTime

値  

### <a name="return-value---creationtime"></a>戻り値 - creationTime

## <a name="method-description"></a>メソッドの説明

```xpp
public str description([str value])
```

### <a name="parameters---description"></a>パラメーター - description

値  

### <a name="return-value---description"></a>戻り値 - description

## <a name="method-equal"></a>メソッド equal

指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。

```xpp
public boolean equal(Object obj)
```

### <a name="parameters---equal"></a>パラメーター - equal

obj  

### <a name="return-value---equal"></a>戻り値 - equal

指定したオブジェクトが現在のオブジェクトと等しい場合は true。それ以外の場合は、false。

### <a name="remarks---equal"></a>備考 - equal

Object::equal メソッドの既定の実装では、照会の等価性のみをサポートします。 ただし、派生クラスは、値の等価性をサポートするために Object::equal メソッドをオーバーライドできます。

## <a name="method-form"></a>メソッド form

```xpp
public str form([str value])
```

### <a name="parameters---form"></a>パラメーター - form

値  

### <a name="return-value---form"></a>戻り値 - form

## <a name="method-get"></a>メソッド get

次のメソッドの前の呼び出しによってフェッチされたレコードを取得します。

```xpp
public Common get(TableId table, [int occurrence])
```

### <a name="parameters---get"></a>パラメーター - get

テーブル  
アドレス指定されるデータソース (オプション)。 指定されたテーブルを持つデータ ソースの番号。1 ベース。 同じテーブルに割り当てられたデータ ソースが 1 つ以上ある場合は、この (オプションの) パラメーターを使用して、どのパラメーターを指定するかを指定できます。 指定されたテーブルを持つデータ ソースの数を指定します。 したがって、CustTable テーブルが 2 つのデータ ソースに割り当てられ、2 番目のデータ ソースが必要な場合、この引数は 2 の値である必要があります。

<!-- -->

occurrence  
アドレス指定されるデータソース (オプション)。 指定されたテーブルを持つデータ ソースの番号。1 ベース。 同じテーブルに割り当てられたデータ ソースが 1 つ以上ある場合は、この (オプションの) パラメーターを使用して、どのパラメーターを指定するかを指定できます。 指定されたテーブルを持つデータ ソースの数を指定します。 したがって、CustTable テーブルが 2 つのデータ ソースに割り当てられ、2 番目のデータ ソースが必要な場合、この引数は 2 の値である必要があります。

### <a name="return-value---get"></a>戻り値 - get

引数で識別されるデータ ソースからフェッチされたレコードを返します。

### <a name="remarks---get"></a>備考 - get

レコードを取得するデータ ソースは、データ ソースに割り当てられたテーブルとオプションのパラメーターによって指定されます。 テーブル (およびオプションのパラメーター) を指定するのではなく、getNo メソッドを使用して、データ ソースの数を引数として取得できます。

## <a name="method-getimpexpdatacontracttype"></a>メソッド getImpExpDataContractType

```xpp
public System.Type getImpExpDataContractType()
```

### <a name="return-value---getimpexpdatacontracttype"></a>戻り値 - getImpExpDataContractType

## <a name="method-getno"></a>メソッド getNo

QueryRun.next メソッドの前の呼び出しによってフェッチされたレコードを取得します。

```xpp
public Common getNo(int dataSourceNo)
```

### <a name="parameters---getno"></a>パラメーター - getNo

dataSourceNo  
現在選択されているレコードを取得する元のデータ ソースの番号。

### <a name="return-value---getno"></a>戻り値 - getNo

引数で識別されるデータ ソースのフェッチされたレコードを返します。

### <a name="remarks---getno"></a>備考 - getNo

レコードを取り出すデータ ソースは、データ ソースの番号で指定します。 データソースは、1 から順にカウントされます。 代わりに QueryRun.get メソッドを使用できます。このメソッドは、データ ソースを定義するテーブル (およびオプション パラメーター) を使用して指定されます。

### <a name="examples---getno"></a>例 - getNo

```xpp
{ 
    QueryRun qr; 
    // Consider a query with CustTable/CustTrans datasources. 
    // Traverse all records found in CustTable/CustTrans: 
    while (qr.next()) 
    { 
        if (qr.Changed(TableNum(CustTable)))
        { 
            // A new CustTable record 
            CustTableRecord = qr.GetNo(1); 
        } 
        if (qr.Changed(TableNum(CustTrans))) 
        { 
            // A new CustTrans record 
            CustTransRecord = qr.GetNo(1); 
        } 
    } 
}
```

## <a name="method-importable"></a>メソッド importable

```xpp
public boolean importable()
```

### <a name="return-value---importable"></a>戻り値 - importable

## <a name="method-interactive"></a>メソッド interactive

```xpp
public boolean interactive([boolean value])
```

### <a name="parameters---interactive"></a>パラメーター - interactive

値  

### <a name="return-value---interactive"></a>戻り値 - interactive

## <a name="method-ispositionpagingenabled"></a>メソッド isPositionPagingEnabled

```xpp
public boolean isPositionPagingEnabled()
```

### <a name="return-value---ispositionpagingenabled"></a>戻り値 - isPositionPagingEnabled

## <a name="method-isquerytimedout"></a>メソッド isQueryTimedout

```xpp
public boolean isQueryTimedout()
```

### <a name="return-value---isquerytimedout"></a>戻り値 - isQueryTimedout

## <a name="method-isvaluebasedpagingenabled"></a>メソッド isValueBasedPagingEnabled

```xpp
public boolean isValueBasedPagingEnabled()
```

### <a name="return-value---isvaluebasedpagingenabled"></a>戻り値 - isValueBasedPagingEnabled

## <a name="method-literals"></a>メソッド literals

```xpp
public int literals([int value])
```

### <a name="parameters---literals"></a>パラメーター - literals

値  

### <a name="return-value---literals"></a>戻り値 - literals

## <a name="method-loadcsv"></a>メソッド loadCsv

```xpp
public Guid loadCsv(str fileName)
```

### <a name="parameters---loadcsv"></a>パラメーター - loadCsv

fileName  

### <a name="return-value---loadcsv"></a>戻り値 - loadCsv

## <a name="method-loadxml"></a>メソッド loadXml

```xpp
public Guid loadXml(str fileName)
```

### <a name="parameters---loadxml"></a>パラメーター - loadXml

fileName  

### <a name="return-value---loadxml"></a>戻り値 - loadXml

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - name

値  

### <a name="return-value---name"></a>戻り値 - name

アプリケーション オブジェクトを識別するためにコードで使用される名前。

### <a name="remarks---name"></a>備考 - name

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

## <a name="method-newobject"></a>メソッド newObject

```xpp
public QueryRun newObject(AnyType source)
```

### <a name="parameters---newobject"></a>パラメーター - newObject

ソース  

### <a name="return-value---newobject"></a>戻り値 - newObject

## <a name="method-next"></a>メソッド next

クエリから次のレコードを取得します。

```xpp
public boolean next()
```

### <a name="return-value---next"></a>戻り値 - next

次のレコードが利用可能で getNo メソッドまたは get メソッドで取得することができる場合は true。クエリ内に設定された制約を満たすレコードがそれ以上存在しない場合は false。

### <a name="remarks---next"></a>備考 - next

変更されたメソッドまたは changedNo メソッドを使用して、指定されたデータ ソースのレコードが前回の次のメソッド呼び出しから変更されたかどうかを確認できます。

### <a name="examples---next"></a>例 - next

```xpp
{ 
    queryRun qr; 
    CustTable ct; 
    // ... 
    if (qr.prompt()) 
    { 
        while (qr.next()) 
        { 
            if (qr.Changed(tableNum(CustTable))) 
            { 
                ct = qr.Get (tableNum(CustTable)); 
                print ct.AccountNum; 
            } 
        } 
    } 
}
```

## <a name="method-nextuniqueid"></a>メソッド nextUniqueId

```xpp
public int nextUniqueId([int value])
```

### <a name="parameters---nextuniqueid"></a>パラメーター - nextUniqueId

値  

### <a name="return-value---nextuniqueid"></a>戻り値 - nextUniqueId

## <a name="method-origin"></a>メソッド origin

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a>パラメーター - origin

値  

### <a name="return-value---origin"></a>戻り値 - origin

## <a name="method-pack"></a>メソッド pack

```xpp
public container pack([boolean doCheck])
```

### <a name="parameters---pack"></a>パラメーター - pack

doCheck  

### <a name="return-value---pack"></a>戻り値 - pack

## <a name="method-prompt"></a>メソッド prompt

クエリによってフェッチするレコードを定義するためのオプションをユーザーに表示します。

```xpp
public boolean prompt()
```

### <a name="return-value---prompt"></a>戻り値 - prompt

ユーザーが OK をクリックして検索が続行される場合は true。ユーザーがキャンセルをクリックして検索を停止した場合は false。

### <a name="remarks---prompt"></a>備考 - prompt

ユーザーには、フェッチされたレコードによって実行される制約を定義する範囲を与えるためのフォームが提示される。 または、ユーザーは新しいフィールドを追加し、区切ったり、変更したり、並べ替えたりすることができます。 このメソッドをオーバーロードすると、事前定義されたクエリ フォームではなく、アプリケーション定義の方法でユーザーにプロンプトを表示できます。 または、この方法は、フェッチされるレコードをユーザーがコントロールできないように、オーバーロードされることがあります。 これらの結果を生成するには、継承したメソッドを呼び出さないでください。 いずれの場合でも、関数はクエリが続行する場合は true、それ以外の場合は false を返す必要があります。

### <a name="examples---prompt"></a>例 - prompt

```xpp
{ 
    QueryRun qr; 
    // ... 
    if (qr.prompt()) 
    { 
        // The user pressed OK. Go ahead and do whatever is required. 
    } 
    else 
    { 
        // The user pressed Cancel. 
    } 
}
```

## <a name="method-query"></a>メソッド query

```xpp
public Query query([Query query])
```

### <a name="parameters---query"></a>パラメーター - query

クエリ  

### <a name="return-value---query"></a>戻り値 - query

## <a name="method-querytype"></a>メソッド queryType

```xpp
public int queryType([int value])
```

### <a name="parameters---querytype"></a>パラメーター - queryType

値  

### <a name="return-value---querytype"></a>戻り値 - queryType

## <a name="method-recordlevelsecurity"></a>メソッド recordLevelSecurity

```xpp
public boolean recordLevelSecurity([boolean value])
```

### <a name="parameters---recordlevelsecurity"></a>パラメーター - recordLevelSecurity

値  

### <a name="return-value---recordlevelsecurity"></a>戻り値 - recordLevelSecurity

## <a name="method-report"></a>メソッド report

```xpp
public ReportRun report()
```

### <a name="return-value---report"></a>戻り値 - report

## <a name="method-reportrun"></a>メソッド reportRun

```xpp
public ReportRun reportRun()
```

### <a name="return-value---reportrun"></a>戻り値 - reportRun

## <a name="method-saved"></a>メソッド saved

```xpp
public boolean saved()
```

### <a name="return-value---saved"></a>戻り値 - saved

## <a name="method-saveusersetup"></a>メソッド saveUserSetup

ユーザー設定を保存します。

```xpp
public boolean saveUserSetup([boolean saveIt])
```

### <a name="parameters---saveusersetup"></a>パラメーター - saveUserSetup

saveIt  

### <a name="return-value---saveusersetup"></a>戻り値 - saveUserSetup

設定が正常に保存された場合は true。それ以外の場合は false。

## <a name="method-searchable"></a>メソッド searchable

```xpp
public boolean searchable([boolean value])
```

### <a name="parameters---searchable"></a>パラメーター - searchable

値  

### <a name="return-value---searchable"></a>戻り値 - searchable

## <a name="method-setcursor"></a>メソッド setCursor

```xpp
public boolean setCursor(Common record, [int occurrence])
```

### <a name="parameters---setcursor"></a>パラメーター - setCursor

記録  

<!-- -->

occurrence  

### <a name="return-value---setcursor"></a>戻り値 - setCursor

## <a name="method-setrecord"></a>メソッド setRecord

```xpp
public boolean setRecord(Common record, [int occurrence])
```

### <a name="parameters---setrecord"></a>パラメーター - setRecord

記録  

<!-- -->

occurrence  

### <a name="return-value---setrecord"></a>戻り値 - setRecord

## <a name="method-title"></a>メソッド title

```xpp
public str title([str value])
```

### <a name="parameters---title"></a>パラメーター - title

値  

### <a name="return-value---title"></a>戻り値 - title

## <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

現在のオブジェクトを表す文字列。

### <a name="remarks---tostring"></a>備考 - toString

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

## <a name="method-userupdate"></a>メソッド userUpdate

```xpp
public boolean userUpdate([boolean value])
```

### <a name="parameters---userupdate"></a>パラメーター - userUpdate

値  

### <a name="return-value---userupdate"></a>戻り値 - userUpdate

## <a name="method-version"></a>メソッド version

```xpp
public int version([int value])
```

### <a name="parameters---version"></a>パラメーター - version

値  

### <a name="return-value---version"></a>戻り値 - version

## <a name="method-getqueryrowcount"></a>メソッド getQueryRowCount

```xpp
public static int getQueryRowCount(Query query, int maxRows)
```

### <a name="parameters---getqueryrowcount"></a>パラメーター - getQueryRowCount

クエリ  

<!-- -->

maxRows  

### <a name="return-value---getqueryrowcount"></a>戻り値 - getQueryRowCount

## <a name="method-runandpopulate"></a>メソッド runAndPopulate

```xpp
public static int runAndPopulate(Query sourceRuery, Common targetTable, Map queryAliasesAndTargetColumnsMap)
```

### <a name="parameters---runandpopulate"></a>パラメーター - runAndPopulate

sourceRuery  

<!-- -->

targetTable  

<!-- -->

queryAliasesAndTargetColumnsMap  

### <a name="return-value---runandpopulate"></a>戻り値 - runAndPopulate

## <a name="method-run"></a>メソッド run

ユーザーからクエリに関する情報を取得するために使用されるフォームを開いて、一致するレコードをフェッチします。

```xpp
public void run()
```

### <a name="remarks---run"></a>備考 - run

クエリを実行すると、ユーザーによって入力された制約を満たすレコードが検索されます。 ただし、この方法でのクエリの実行には副作用がありません。 扱いやすくするために、1 つ以上の継承されたメソッドをオーバーロードする必要があります。

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(AnyType source)
```

### <a name="parameters---new"></a>パラメーター - new

ソース  

### <a name="remarks---new"></a>備考 - new

クエリ クラスのインスタンスを QueryRun クラスのコンストラクターに渡すと、クエリ オブジェクトのコピーが作成されます。 このクエリ オブジェクト のコピーに加えられた変更は、元のクエリ オブジェクトには影響しません。

## <a name="method-addpagerange"></a>メソッド addPageRange

```xpp
public void addPageRange([Int64 startingPosition], [Int64 numberOfRecordsToFetch])
```

### <a name="parameters---addpagerange"></a>パラメーター - addPageRange

startingPosition  

<!-- -->

numberOfRecordsToFetch  

## <a name="method-reset"></a>メソッド reset

```xpp
public void reset()
```

## <a name="method-setimportsession"></a>メソッド setImportSession

```xpp
public void setImportSession(Guid importSession)
```

### <a name="parameters---setimportsession"></a>パラメーター - setImportSession

importSession  

## <a name="method-setquerytimeout"></a>メソッド setQuerytimeout

```xpp
public void setQuerytimeout(int seconds, [boolean raiseException])
```

### <a name="parameters---setquerytimeout"></a>パラメーター - setQuerytimeout

秒  

<!-- -->

raiseException  

## <a name="method-init"></a>メソッド init

```xpp
public void init()
```

## <a name="method-enablepositionpaging"></a>メソッド enablePositionPaging

```xpp
public void enablePositionPaging([boolean enabled])
```

### <a name="parameters---enablepositionpaging"></a>パラメーター - enablePositionPaging

有効  

## <a name="method-shred"></a>メソッド shred

```xpp
public void shred(Guid importSession)
```

### <a name="parameters---shred"></a>パラメーター - shred

importSession  

## <a name="method-enablevaluebasedpaging"></a>メソッド enableValueBasedPaging

```xpp
public void enableValueBasedPaging([boolean enable])
```

### <a name="parameters---enablevaluebasedpaging"></a>パラメーター - enableValueBasedPaging

enable  

## <a name="method-bulknext"></a>メソッド bulkNext

```xpp
public void bulkNext([boolean fetchAllData])
```

### <a name="parameters---bulknext"></a>パラメーター - bulkNext

fetchAllData  

## <a name="method-applyvaluebasedpaging"></a>メソッド applyValueBasedPaging

```xpp
public void applyValueBasedPaging([Common sourceCursor], [boolean isForward])
```

### <a name="parameters---applyvaluebasedpaging"></a>パラメーター - applyValueBasedPaging

sourceCursor  

<!-- -->

isForward  

## <a name="method-skipautoorderby"></a>メソッド skipAutoOrderBy

```xpp
Specifies whether an Order By clause will be generated, in case no Order By field was specified.
public boolean skipAutoOrderBy([boolean value])

```

先頭値
### <a name="return-value---skipautoorderby"></a>戻り値 - skipAutoOrderBy
パラメーターが指定されていない場合は現在の値、パラメーターが指定されている場合は新しい値です。
### <a name="remarks---skipautoorderby"></a>備考 - skipAutoOrderBy
既定では SkipAutoOrderBy は false で、プラットフォーム更新プログラム 31 以降で使用可能です。
