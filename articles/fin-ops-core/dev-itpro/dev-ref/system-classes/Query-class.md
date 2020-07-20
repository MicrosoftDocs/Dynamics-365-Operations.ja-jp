---
title: Query クラス
description: このトピックでは、Query クラスについて説明します。
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
ms.openlocfilehash: a8b5daa9f26ad98fc8e2135c62d2813d99c1cca4
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502871"
---
# <a name="class-query"></a>クラス クエリ

[!include [banner](../../includes/banner.md)]


```xpp
class Query extends TreeNode
```

クエリ クラスには、クエリの構造が含まれます。

## <a name="remarks"></a>備考

このタイプのオブジェクトは、データベースからレコードをフェッチするために使用されません。 代わりに、クエリ オブジェクトを割り当てることができる QueryRun オブジェクトを使用します。 クエリの動的な動作は、QueryRun クラスによって定義されます。 静的なビヘイビアーは、Query クラスによって定義されます。 クエリには、データベース内のテーブルに対応する 1 つまたは複数のデータ ソースが含まれます。 データ ソースを指定するには、QueryBuildDataSource オブジェクトを使用します。 このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。 クエリは、ユーザーが、たとえばフォームなどによりフェッチされるレコードを変更する場合に使用されます。 多くの場合、1 つ以上の範囲は既存のデータ ソースに追加されます。 範囲を指定するには、queryBuildRange オブジェクトを使用します。

## <a name="examples"></a>例

次の例では、QueryRun オブジェクトを作成するために使用されるクエリ オブジェクトを作成します。

```xpp
{ 
    Query q = new Query (QueryStr(Cust)); 
    // Use the query to build a queryRun object. 
    QueryRun qr = new QueryRun (q); 
    // Traverse some records. 
    while (qr.next()) 
    { 
        // ... 
    } 
}
```

## <a name="methods"></a>メソッド

| 方法                                                                                                                                                                 | 説明                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public Query addBaseQuery(str queryName)                                                                                                                               |                                                                                                                                           |
| public QueryBuildDataSource addDataSource(TableId table, \[str name\], \[UnionType unionType\], \[boolean emptyFieldList\])                                            | クエリのトップ レベルにデータ ソースを追加します。                                                                                         |
| public QueryHavingFilter addHavingFilter(QueryBuildDataSource dataSource, str fieldName, AggregateFunction aggregateFunction, \[int arrayIndex\])                      |                                                                                                                                           |
| public QueryFilter addQueryFilter(QueryBuildDataSource dataSource, str fieldName, \[int arrayIndex\])                                                                  |                                                                                                                                           |
| public boolean allowCheck(\[boolean value\])                                                                                                                           |                                                                                                                                           |
| public boolean allowCrossCompany(\[boolean value\])                                                                                                                    |                                                                                                                                           |
| public boolean allowHavingFilters(QueryBuildDataSource dataSource, FieldName fieldName, AggregateFunction aggregateFunction)                                           |                                                                                                                                           |
| public boolean allowQueryFilters(QueryBuildDataSource dataSource)                                                                                                      |                                                                                                                                           |
| public str changedBy(\[str value\])                                                                                                                                    | クエリ オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                                      |
| public Date changedDate(\[Date value\])                                                                                                                                | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                             |
| public str changedTime(\[str value\])                                                                                                                                  | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                             |
| public int childDataSourceCount()                                                                                                                                      | クエリに関連するデータ ソースの数をカウントします。                                                                          |
| public QueryBuildDataSource childDataSourceNo(int dataSourceNo)                                                                                                        | 指定された番号に対応するデータ ソースを返します。                                                                   |
| public boolean containsAggregateFields()                                                                                                                               |                                                                                                                                           |
| public str createdBy(\[str value\])                                                                                                                                    | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                     |
| public Date creationDate(\[Date value\])                                                                                                                               | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                                  |
| public str creationTime(\[str value\])                                                                                                                                 |                                                                                                                                           |
| public int dataSourceCount()                                                                                                                                           | 埋め込みデータ ソースを含む、クエリのデータ ソースの合計数を返します。                                              |
| public QueryBuildDataSource dataSourceName(str name)                                                                                                                   | 指定された名前を持つデータ ソースを返します。                                                                                      |
| public QueryBuildDataSource dataSourceNo(int dataSourceNo)                                                                                                             | データ ソース番号により指定されたデータ ソースを返します。                                                                      |
| public QueryBuildDataSource dataSourceTable(TableId table, \[int occurrence\])                                                                                         | 指定されたテーブルが割り当てられているデータ ソースを返します。                                                                          |
| public QueryBuildDataSource dataSourceUniqueId(int uniqueId)                                                                                                           |                                                                                                                                           |
| public str description(\[str value\])                                                                                                                                  |                                                                                                                                           |
| public boolean equal(Object record)                                                                                                                                    | あるクエリが別のクエリと等しいかどうかを評価します。                                                                                          |
| public str exportXML()                                                                                                                                                 |                                                                                                                                           |
| public QueryHavingFilter findHavingFilterByField(QueryBuildDataSource dataSource, FieldName fieldName, \[int occurrence\], \[int arrayIndex\])                         |                                                                                                                                           |
| public QueryFilter findQueryFilter(QueryBuildDataSource dataSource, FieldName fieldName, \[int occurrence\], \[int arrayIndex\])                                       |                                                                                                                                           |
| public QueryBuildDataSource firstTopLevelDataSource()                                                                                                                  |                                                                                                                                           |
| public boolean forceNestedLoop(boolean arg)                                                                                                                            |                                                                                                                                           |
| public boolean forceSelectOrder(boolean arg)                                                                                                                           |                                                                                                                                           |
| public str form(\[str value\])                                                                                                                                         |                                                                                                                                           |
| public container getCompanyRange()                                                                                                                                     |                                                                                                                                           |
| public int getMostRestrictedQueryFilterStatus(QueryBuildDataSource dataSource, FieldName fieldName, \[int fieldId\])                                                   |                                                                                                                                           |
| public int getNextUniqueId()                                                                                                                                           |                                                                                                                                           |
| public str getSQLStatement(\[boolean noRuntimeOptimization\])                                                                                                          |                                                                                                                                           |
| public container getValidTimeStateDateRange()                                                                                                                          |                                                                                                                                           |
| public container getValidTimeStateDateTimeRange()                                                                                                                      |                                                                                                                                           |
| public ValidTimeStateQueryType getValidTimeStateQueryType()                                                                                                            |                                                                                                                                           |
| public QueryGroupByField groupByField(int index, \[QueryBuildDataSource dataSource\])                                                                                  |                                                                                                                                           |
| public int groupByFieldCount(\[QueryBuildDataSource dataSource\])                                                                                                      |                                                                                                                                           |
| public boolean hasMultipleTopLevelDataSource()                                                                                                                         |                                                                                                                                           |
| public boolean hasRangeOrFilter(QueryBuildDataSource dataSource)                                                                                                       |                                                                                                                                           |
| public QueryHavingFilter havingFilter(int count, \[QueryBuildDataSource dataSource\])                                                                                  |                                                                                                                                           |
| public int havingFilterCount(\[QueryBuildDataSource dataSource\])                                                                                                      |                                                                                                                                           |
| public boolean inReport()                                                                                                                                              | クエリがレポートの一部であるかどうかを決定します。                                                                                         |
| public boolean interactive(\[boolean value\])                                                                                                                          | クエリが対話的かどうかを指定します。                                                                                               |
| public boolean isCompositeQuery()                                                                                                                                      |                                                                                                                                           |
| public boolean isExplicitlyOrdered()                                                                                                                                   |                                                                                                                                           |
| public boolean isExplicitlyGrouped()                                                                                                                                   |                                                                                                                                           |
| public boolean isPureUnionAll()                                                                                                                                        |                                                                                                                                           |
| public boolean isUnionType()                                                                                                                                           |                                                                                                                                           |
| public int levelNo(int dataSourceNo)                                                                                                                                   | 指定されたデータ ソースのインデントのレベルを決定します。                                                                         |
| public int levelTable(TableId table, \[int occurrence\])                                                                                                               | 指定したテーブルに割り当てられているデータ ソースのツリー レベルを、データ ソースの階層内で決定します。                  |
| public int literals(\[int value\])                                                                                                                                     |                                                                                                                                           |
| public str name(\[str value\])                                                                                                                                         | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public Query newObject(AnyType source)                                                                                                                                 | ソース クエリとして同じクライアント側、またはサーバー側で存在するクエリを作成します。                                                   |
| public int nextUniqueId(\[int value\])                                                                                                                                 |                                                                                                                                           |
| public QueryOrderByField orderByField(int index, \[QueryBuildDataSource dataSource\])                                                                                  |                                                                                                                                           |
| public int orderByFieldCount(\[QueryBuildDataSource dataSource\])                                                                                                      |                                                                                                                                           |
| public Guid origin(\[Guid value\])                                                                                                                                     |                                                                                                                                           |
| public container pack(\[boolean doCheck\])                                                                                                                             | コンテナーにクエリをパックし、クエリを作成するときに使用できるようにそのコンテナーを返します。                              |
| public container packInternals()                                                                                                                                       |                                                                                                                                           |
| public QueryFilter queryFilter(int count, \[QueryBuildDataSource rootDataSource\])                                                                                     |                                                                                                                                           |
| public int queryFilterCount(\[QueryBuildDataSource rootDataSource\])                                                                                                   |                                                                                                                                           |
| public int queryType(\[int value\])                                                                                                                                    |                                                                                                                                           |
| public str quickFilterValue()                                                                                                                                          |                                                                                                                                           |
| public int quickFilterControlId()                                                                                                                                      |                                                                                                                                           |
| public boolean recordLevelSecurity(\[boolean value\])                                                                                                                  |                                                                                                                                           |
| public Report report()                                                                                                                                                 | レポートが存在する場合、クエリが定義されているレポートを返します。                                                                   |
| public boolean saved()                                                                                                                                                 | クエリがディスクに保存されたかどうかを示します。                                                                                       |
| public boolean searchable(\[boolean value\])                                                                                                                           |                                                                                                                                           |
| public Guid importSession(\[Guid value\])                                                                                                                              |                                                                                                                                           |
| public str title(\[str value\])                                                                                                                                        |                                                                                                                                           |
| public int topRows(\[int value\])                                                                                                                                      |                                                                                                                                           |
| public str toString()                                                                                                                                                  | 現在のオブジェクトを表す文字列を返します。                                                                                      |
| public boolean userUpdate(\[boolean value\])                                                                                                                           | フェッチされたレコードをクエリが更新できるかどうかを示す値を取得または設定します。                                             |
| public Date validTimeStateAsOfDate(\[Date asOfDate\])                                                                                                                  |                                                                                                                                           |
| public DateTime validTimeStateAsOfDateTime(\[DateTime asOfDateTime\])                                                                                                  |                                                                                                                                           |
| public int validTimeStateFlags(\[int value\])                                                                                                                          |                                                                                                                                           |
| public int version(\[int value\])                                                                                                                                      |                                                                                                                                           |
| public str xml(\[int indent\])                                                                                                                                         | 現在のオブジェクトを表す XML 文字列を返します。                                                                                 |
| public void clearBaseQueries()                                                                                                                                         |                                                                                                                                           |
| public void addCompanyRange(str companyName)                                                                                                                           |                                                                                                                                           |
| public void checkRangeParsingErrors(boolean setCheckRangeParsingErrors)                                                                                                |                                                                                                                                           |
| public void clearCompanyRange()                                                                                                                                        |                                                                                                                                           |
| public void unpackInternals(container internalData)                                                                                                                    |                                                                                                                                           |
| public void new(\[AnyType source\])                                                                                                                                    | クエリ オブジェクトを作成します。                                                                                                                   |
| public void checkFieldAccess(boolean setCheckFieldAccess)                                                                                                              |                                                                                                                                           |
| public void useDbCacheOnGeneratedCursors(\[int fetchsize\])                                                                                                            |                                                                                                                                           |
| public void setValidTimeStateQueryType(\[ValidTimeStateQueryType type\])                                                                                               |                                                                                                                                           |
| public void validTimeStateDateRange(\[Date fromDate\], \[Date toDate\])                                                                                                |                                                                                                                                           |
| public void clearHavingFilters(\[QueryBuildDataSource dataSource\], \[str fieldName\], \[int occurence\], \[int arrayIndex\])                                          |                                                                                                                                           |
| public void quickFilter(\[str dataSourceName\], \[int tableId\], \[int fieldId\], \[str filterValue\], \[int controlId\], \[boolean useEqualityComparisonForStrings\]) |                                                                                                                                           |
| public void finalize()                                                                                                                                                 |                                                                                                                                           |
| public void clearQueryFilters(\[QueryBuildDataSource dataSource\], \[str fieldName\], \[int occurence\], \[int arrayIndex\])                                           |                                                                                                                                           |
| public void clearOrderBy()                                                                                                                                             |                                                                                                                                           |
| public void clearAllFields()                                                                                                                                           |                                                                                                                                           |
| public void clearGroupBy()                                                                                                                                             |                                                                                                                                           |
| public void autoAuthzMode(AutoAuthzMode mode)                                                                                                                          |                                                                                                                                           |
| ::public static void insert\_recordset(Common targetCursor, Map targetToSourceMap, Query sourceQuery)                                                                  |                                                                                                                                           |
| public void generateCursors()                                                                                                                                          |                                                                                                                                           |
| public void checkAuthorizationOnOpenRanges(boolean setCheckAuthorizationOnOpenRanges)                                                                                  |                                                                                                                                           |
| public void addContains(str containsValue, \[boolean prefixSearch\])                                                                                                   |                                                                                                                                           |
| public void resetValidTimeStateQueryType()                                                                                                                             |                                                                                                                                           |
| public void validTimeStateDateTimeRange(\[DateTime fromDateTime\], \[DateTime toDateTime\])                                                                            |                                                                                                                                           |
| public boolean skipAutoOrderBy(\[boolean value\])                                                                                                                           | Order By フィールドが明示的に指定されていない場合、Order By 句の自動生成をスキップすることができます。                                             |

## <a name="method-addbasequery"></a>メソッド addBaseQuery

```xpp
public Query addBaseQuery(str queryName)
```

### <a name="parameters---addbasequery"></a>パラメーター - addBaseQuery

queryName  

### <a name="return-value---addbasequery"></a>戻り値 - addBaseQuery

## <a name="method-adddatasource"></a>メソッド addDataSource

クエリのトップ レベルにデータ ソースを追加します。

```xpp
public QueryBuildDataSource addDataSource(TableId table, [str name], [UnionType unionType], [boolean emptyFieldList])
```

### <a name="parameters---adddatasource"></a>パラメーター - addDataSource

テーブル  

<!-- -->

名前  

<!-- -->

unionType  

<!-- -->

emptyFieldList  

### <a name="return-value---adddatasource"></a>戻り値 - addDataSource

作成されたデータ ソース オブジェクト。

### <a name="remarks---adddatasource"></a>備考 - addDataSource

文書作成のために名前の値を指定できます。 dataSourceName メソッドを使用してデータ ソースをフェッチする名前を使用することができます。

## <a name="method-addhavingfilter"></a>メソッド addHavingFilter

```xpp
public QueryHavingFilter addHavingFilter(QueryBuildDataSource dataSource, str fieldName, AggregateFunction aggregateFunction, [int arrayIndex])
```

### <a name="parameters---addhavingfilter"></a>パラメーター - addHavingFilter

dataSource  

<!-- -->

fieldName  

<!-- -->

aggregateFunction  

<!-- -->

arrayIndex  

### <a name="return-value---addhavingfilter"></a>戻り値 - addHavingFilter

## <a name="method-addqueryfilter"></a>メソッド addQueryFilter

```xpp
public QueryFilter addQueryFilter(QueryBuildDataSource dataSource, str fieldName, [int arrayIndex])
```

### <a name="parameters---addqueryfilter"></a>パラメーター - addQueryFilter

dataSource  

<!-- -->

fieldName  

<!-- -->

arrayIndex  

### <a name="return-value---addqueryfilter"></a>戻り値 - addQueryFilter

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

## <a name="method-allowhavingfilters"></a>メソッド allowHavingFilters

```xpp
public boolean allowHavingFilters(QueryBuildDataSource dataSource, FieldName fieldName, AggregateFunction aggregateFunction)
```

### <a name="parameters---allowhavingfilters"></a>パラメーター - allowHavingFilters

dataSource  

<!-- -->

fieldName  

<!-- -->

aggregateFunction  

### <a name="return-value---allowhavingfilters"></a>戻り値 - allowHavingFilters

## <a name="method-allowqueryfilters"></a>メソッド allowQueryFilters

```xpp
public boolean allowQueryFilters(QueryBuildDataSource dataSource)
```

### <a name="parameters---allowqueryfilters"></a>パラメーター - allowQueryFilters

dataSource  

### <a name="return-value---allowqueryfilters"></a>戻り値 - allowQueryFilters

## <a name="method-changedby"></a>メソッド changedBy

クエリ オブジェクトを最後に変更したユーザーの名前を取得または設定します。

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a>パラメーター - changedBy

値  
クエリ オブジェクトを最後に変更したユーザーの名前 (オプション)。

### <a name="return-value---changedby"></a>戻り値 - changedBy

クエリ オブジェクトを最後に変更したユーザーの名前。

## <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a>パラメーター - changedDate

値  

### <a name="return-value---changeddate"></a>戻り値 - changedDate

アプリケーション オブジェクトが最後に変更された日付。

## <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a>パラメーター - changedTime

値  

### <a name="return-value---changedtime"></a>戻り値 - changedTime

アプリケーション オブジェクトが最後に変更された時間。

## <a name="method-childdatasourcecount"></a>メソッド childDataSourceCount

クエリに関連するデータ ソースの数をカウントします。

```xpp
public int childDataSourceCount()
```

### <a name="return-value---childdatasourcecount"></a>戻り値 - childDataSourceCount

このクエリに関連するデータ ソースの数。

### <a name="remarks---childdatasourcecount"></a>備考 - childDataSourceCount

このメソッドは、トップレベルのクエリに使用されます。 別のデータ ソースに埋め込まれているデータ ソースの数を確認するには、childDataSourceCount メソッドを使用します。

## <a name="method-childdatasourceno"></a>メソッド childDataSourceNo

指定された番号に対応するデータ ソースを返します。

```xpp
public QueryBuildDataSource childDataSourceNo(int dataSourceNo)
```

### <a name="parameters---childdatasourceno"></a>パラメーター - childDataSourceNo

dataSourceNo  
子データ ソースの番号。

### <a name="return-value---childdatasourceno"></a>戻り値 - childDataSourceNo

指定された番号を持つ子データ ソース。

### <a name="remarks---childdatasourceno"></a>備考 - childDataSourceNo

指定された数値は、クエリのすぐ下にあるデータ ソースを表す必要があります。 通常、このようなデータ ソースは 1 つだけです。

## <a name="method-containsaggregatefields"></a>メソッド containsAggregateFields

```xpp
public boolean containsAggregateFields()
```

### <a name="return-value---containsaggregatefields"></a>戻り値 - containsAggregateFields

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

## <a name="method-datasourcecount"></a>メソッド dataSourceCount

埋め込みデータ ソースを含む、クエリのデータ ソースの合計数を返します。

```xpp
public int dataSourceCount()
```

### <a name="return-value---datasourcecount"></a>戻り値 - dataSourceCount

このクエリのデータ ソースの数。

### <a name="remarks---datasourcecount"></a>備考 - dataSourceCount

この番号は、データ ソースの推移的な番号であり、任意の埋め込みデータ ソースが含まれています。

## <a name="method-datasourcename"></a>メソッド dataSourceName

指定された名前を持つデータ ソースを返します。

```xpp
public QueryBuildDataSource dataSourceName(str name)
```

### <a name="parameters---datasourcename"></a>パラメーター - dataSourceName

名前  
返すデータソースの名前を含む文字列。

### <a name="return-value---datasourcename"></a>戻り値 - dataSourceName

指定した名前を持つデータ ソース。指定されたデータ ソースが存在しない場合は、初期化されていないオブジェクト。

## <a name="method-datasourceno"></a>メソッド dataSourceNo

データ ソース番号により指定されたデータ ソースを返します。

```xpp
public QueryBuildDataSource dataSourceNo(int dataSourceNo)
```

### <a name="parameters---datasourceno"></a>パラメーター - dataSdataSourceNo

dataSourceNo  
データ ソースの番号。

### <a name="return-value---datasourceno"></a>戻り値 - dataSourceNo

指定した番号を持つデータ ソース。指定されたデータ ソースが存在しない場合は、初期化されていないオブジェクト。

## <a name="method-datasourcetable"></a>メソッド dataSourceTable

指定されたテーブルが割り当てられているデータ ソースを返します。

```xpp
public QueryBuildDataSource dataSourceTable(TableId table, [int occurrence])
```

### <a name="parameters---datasourcetable"></a>パラメーター - dataSourceTable

テーブル  
複数のデータ ソースが指定されたテーブル ID を使用する場合に使用される整数。オプション。 既定値は 1で、最初の (通常は唯一の) インスタンスを指定します。

<!-- -->

occurrence  
複数のデータ ソースが指定されたテーブル ID を使用する場合に使用される整数。オプション。 既定値は 1で、最初の (通常は唯一の) インスタンスを指定します。

### <a name="return-value---datasourcetable"></a>戻り値 - dataSourceTable

指定されたテーブルが割り当てられているデータ ソース。

### <a name="remarks---datasourcetable"></a>備考 - dataSourceTable

データ ソースは、dataSourceNo メソッドまたは dataSourceName メソッドを呼び出すことによって取得することもできます。

## <a name="method-datasourceuniqueid"></a>メソッド dataSourceUniqueId

```xpp
public QueryBuildDataSource dataSourceUniqueId(int uniqueId)
```

### <a name="parameters---datasourceuniqueid"></a>パラメーター - dataSourceUniqueId

uniqueId  

### <a name="return-value---datasourceuniqueid"></a>戻り値 - dataSourceUniqueId

## <a name="method-description"></a>メソッドの説明

```xpp
public str description([str value])
```

### <a name="parameters---description"></a>パラメーター - description

値  

### <a name="return-value---description"></a>戻り値 - description

## <a name="method-equal"></a>メソッド equal

あるクエリが別のクエリと等しいかどうかを評価します。

```xpp
public boolean equal(Object record)
```

### <a name="parameters---equal"></a>パラメーター - equal

記録  
比較として使用するクエリです。

### <a name="return-value---equal"></a>戻り値 - equal

クエリが等しい場合は true。それ以外の場合は、false。

### <a name="remarks---equal"></a>備考 - equal

この場合、「等しい」は、クエリが比較されるクエリと構造的に同一であることを意味します。 クエリには、同じファイルに割り当てられたデータ ソースと同じ数のデータ ソースがあり、同じ数の範囲があります。

## <a name="method-exportxml"></a>メソッド exportXML

```xpp
public str exportXML()
```

### <a name="return-value---exportxml"></a>戻り値 - exportXML

## <a name="method-findhavingfilterbyfield"></a>メソッド findHavingFilterByField

```xpp
public QueryHavingFilter findHavingFilterByField(QueryBuildDataSource dataSource, FieldName fieldName, [int occurrence], [int arrayIndex])
```

### <a name="parameters---findhavingfilterbyfield"></a>パラメーター - findHavingFilterByField

dataSource  

<!-- -->

fieldName  

<!-- -->

occurrence  

<!-- -->

arrayIndex  

### <a name="return-value---findhavingfilterbyfield"></a>戻り値 - findHavingFilterByField

## <a name="method-findqueryfilter"></a>メソッド findQueryFilter

```xpp
public QueryFilter findQueryFilter(QueryBuildDataSource dataSource, FieldName fieldName, [int occurrence], [int arrayIndex])
```

### <a name="parameters---findqueryfilter"></a>パラメーター - findQueryFilter

dataSource  

<!-- -->

fieldName  

<!-- -->

occurrence  

<!-- -->

arrayIndex  

### <a name="return-value---findqueryfilter"></a>戻り値 - findQueryFilter

## <a name="method-firsttopleveldatasource"></a>メソッド firstTopLevelDataSource

```xpp
public QueryBuildDataSource firstTopLevelDataSource()
```

### <a name="return-value---firsttopleveldatasource"></a>戻り値 - firstTopLevelDataSource

## <a name="method-forcenestedloop"></a>メソッド forceNestedLoop

```xpp
public boolean forceNestedLoop(boolean arg)
```

### <a name="parameters---forcenestedloop"></a>パラメーター - forceNestedLoop

arg  

### <a name="return-value---forcenestedloop"></a>戻り値 - forceNestedLoop

## <a name="method-forceselectorder"></a>メソッド forceSelectOrder

```xpp
public boolean forceSelectOrder(boolean arg)
```

### <a name="parameters---forceselectorder"></a>パラメーター - forceSelectOrder

arg  

### <a name="return-value---forceselectorder"></a>戻り値 - forceSelectOrder

## <a name="method-form"></a>メソッド form

```xpp
public str form([str value])
```

### <a name="parameters---form"></a>パラメーター - form

値  

### <a name="return-value---form"></a>戻り値 - form

## <a name="method-getcompanyrange"></a>メソッド getCompanyRange

```xpp
public container getCompanyRange()
```

### <a name="return-value---getcompanyrange"></a>戻り値 - getCompanyRange

## <a name="method-getmostrestrictedqueryfilterstatus"></a>メソッド getMostRestrictedQueryFilterStatus

```xpp
public int getMostRestrictedQueryFilterStatus(QueryBuildDataSource dataSource, FieldName fieldName, [int fieldId])
```

### <a name="parameters---getmostrestrictedqueryfilterstatus"></a>パラメーター - getMostRestrictedQueryFilterStatus

dataSource  

<!-- -->

fieldName  

<!-- -->

fieldId  

### <a name="return-value---getmostrestrictedqueryfilterstatus"></a>戻り値 - getMostRestrictedQueryFilterStatus

## <a name="method-getnextuniqueid"></a>メソッド getNextUniqueId

```xpp
public int getNextUniqueId()
```

### <a name="return-value---getnextuniqueid"></a>戻り値 - getNextUniqueId

## <a name="method-getsqlstatement"></a>メソッド getSQLStatement

```xpp
public str getSQLStatement([boolean noRuntimeOptimization])
```

### <a name="parameters---getsqlstatement"></a>パラメーター - getSQLStatement

noRuntimeOptimization  

### <a name="return-value---getsqlstatement"></a>戻り値 - getSQLStatement

## <a name="method-getvalidtimestatedaterange"></a>メソッド getValidTimeStateDateRange

```xpp
public container getValidTimeStateDateRange()
```

### <a name="return-value---getvalidtimestatedaterange"></a>戻り値 - getValidTimeStateDateRange

## <a name="method-getvalidtimestatedatetimerange"></a>メソッド getValidTimeStateDateTimeRange

```xpp
public container getValidTimeStateDateTimeRange()
```

### <a name="return-value---getvalidtimestatedatetimerange"></a>戻り値 - getValidTimeStateDateTimeRange

## <a name="method-getvalidtimestatequerytype"></a>メソッド getValidTimeStateQueryType

```xpp
public ValidTimeStateQueryType getValidTimeStateQueryType()
```

### <a name="return-value---getvalidtimestatequerytype"></a>戻り値 - getValidTimeStateQueryType

## <a name="method-groupbyfield"></a>メソッド groupByField

```xpp
public QueryGroupByField groupByField(int index, [QueryBuildDataSource dataSource])
```

### <a name="parameters---groupbyfield"></a>パラメーター - groupByField

指数  

<!-- -->

dataSource  

### <a name="return-value---groupbyfield"></a>戻り値 - groupByField

## <a name="method-groupbyfieldcount"></a>メソッド groupByFieldCount

```xpp
public int groupByFieldCount([QueryBuildDataSource dataSource])
```

### <a name="parameters---groupbyfieldcount"></a>パラメーター - groupByFieldCount

dataSource  

### <a name="return-value---groupbyfieldcount"></a>戻り値 - groupByFieldCount

## <a name="method-hasmultipletopleveldatasource"></a>メソッド hasMultipleTopLevelDataSource

```xpp
public boolean hasMultipleTopLevelDataSource()
```

### <a name="return-value---hasmultipletopleveldatasource"></a>戻り値 - hasMultipleTopLevelDataSource

## <a name="method-hasrangeorfilter"></a>メソッド hasRangeOrFilter

```xpp
public boolean hasRangeOrFilter(QueryBuildDataSource dataSource)
```

### <a name="parameters---hasrangeorfilter"></a>パラメーター - hasRangeOrFilter

dataSource  

### <a name="return-value---hasrangeorfilter"></a>戻り値 - hasRangeOrFilter

## <a name="method-havingfilter"></a>メソッド havingFilter

```xpp
public QueryHavingFilter havingFilter(int count, [QueryBuildDataSource dataSource])
```

### <a name="parameters---havingfilter"></a>パラメーター - havingFilter

カウント  

<!-- -->

dataSource  

### <a name="return-value---havingfilter"></a>戻り値 - havingFilter

## <a name="method-havingfiltercount"></a>メソッド havingFilterCount

```xpp
public int havingFilterCount([QueryBuildDataSource dataSource])
```

### <a name="parameters---havingfiltercount"></a>パラメーター - havingFilterCount

dataSource  

### <a name="return-value---havingfiltercount"></a>戻り値 - havingFilterCount

## <a name="method-inreport"></a>メソッド inReport

クエリがレポートの一部であるかどうかを決定します。

```xpp
public boolean inReport()
```

### <a name="return-value---inreport"></a>戻り値 - inReport

クエリがレポートの一部である場合は (レポートのデータ ソース ノードの下にある場合は) true。それ以外の場合は、false。

### <a name="remarks---inreport"></a>備考 - inReport

この関数は、通常アプリケーション コードでは使用されません。 メソッドが true を返す場合は、レポート メソッドはクエリが定義されているレポートにアクセスするために使用することができます。

## <a name="method-interactive"></a>メソッド interactive

クエリが対話的かどうかを指定します。

```xpp
public boolean interactive([boolean value])
```

### <a name="parameters---interactive"></a>パラメーター - interactive

値  
クエリがインタラクティブかどうかを示す値、オプション。

### <a name="return-value---interactive"></a>戻り値 - interactive

クエリが対話形式である場合は true。それ以外の場合は、false。

### <a name="remarks---interactive"></a>備考 - interactive

対話型クエリでは、たとえば prompt メソッドが呼び出されたときに、クエリはユーザーにダイアログ ボックスを提示できます。 この機能は、コードをバッチに送信する場合や、コードを無人で実行する必要がある場合に使用されます。

## <a name="method-iscompositequery"></a>メソッド isCompositeQuery

```xpp
public boolean isCompositeQuery()
```

### <a name="return-value---iscompositequery"></a>備考 - isCompositeQuery

## <a name="method-isexplicitlyordered"></a>メソッド isExplicitlyOrdered

```xpp
public boolean isExplicitlyOrdered()
```

### <a name="return-value---isexplicitlyordered"></a>戻り値 - isExplicitlyOrdered

## <a name="method-isexplicitlygrouped"></a>メソッド isExplicitlyGrouped

```xpp
public boolean isExplicitlyGrouped()
```

### <a name="return-value---isexplicitlygrouped"></a>戻り値 - isExplicitlyGrouped

## <a name="method-ispureunionall"></a>メソッド isPureUnionAll

```xpp
public boolean isPureUnionAll()
```

### <a name="return-value---ispureunionall"></a>戻り値 - isPureUnionAll

## <a name="method-isuniontype"></a>メソッド isUnionType

```xpp
public boolean isUnionType()
```

### <a name="return-value---isuniontype"></a>戻り値 - isUnionType

## <a name="method-levelno"></a>メソッド levelNo

指定されたデータ ソースのインデントのレベルを決定します。

```xpp
public int levelNo(int dataSourceNo)
```

### <a name="parameters---levelno"></a>パラメーター - levelNo

dataSourceNo  
データ ソースのレベルを決定する番号。

### <a name="return-value---levelno"></a>戻り値 - levelNo

指定されたデータ ソースのレベル番号。

### <a name="remarks---levelno"></a>備考 - levelNo

データソースは、1 から順に番号付けされます。

## <a name="method-leveltable"></a>メソッド levelTable

指定したテーブルに割り当てられているデータ ソースのツリー レベルを、データ ソースの階層内で決定します。

```xpp
public int levelTable(TableId table, [int occurrence])
```

### <a name="parameters---leveltable"></a>パラメーター - levelTable

テーブル  
複数のデータ ソースが同じテーブルに割り当てられる場合に使用される整数。オプション。

<!-- -->

occurrence  
複数のデータ ソースが同じテーブルに割り当てられる場合に使用される整数。オプション。

### <a name="return-value---leveltable"></a>戻り値 - levelTable

クエリの指定されたデータ ソースのレベル番号。

## <a name="method-literals"></a>メソッド literals

```xpp
public int literals([int value])
```

### <a name="parameters---literals"></a>パラメーター - literals

値  

### <a name="return-value---literals"></a>戻り値 - literals

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

ソース クエリとして同じクライアント側、またはサーバー側で存在するクエリを作成します。

```xpp
public Query newObject(AnyType source)
```

### <a name="parameters---newobject"></a>パラメーター - newObject

ソース  
ソース クエリ。

### <a name="return-value---newobject"></a>戻り値 - newObject

新しいクエリ。

## <a name="method-nextuniqueid"></a>メソッド nextUniqueId

```xpp
public int nextUniqueId([int value])
```

### <a name="parameters---nextuniqueid"></a>パラメーター - nextUniqueId

値  

### <a name="return-value---nextuniqueid"></a>戻り値 - nextUniqueId

## <a name="method-orderbyfield"></a>メソッド orderByField

```xpp
public QueryOrderByField orderByField(int index, [QueryBuildDataSource dataSource])
```

### <a name="parameters---orderbyfield"></a>パラメーター - orderByField

指数  

<!-- -->

dataSource  

### <a name="return-value---orderbyfield"></a>戻り値 - orderByField

## <a name="method-orderbyfieldcount"></a>メソッド orderByFieldCount

```xpp
public int orderByFieldCount([QueryBuildDataSource dataSource])
```

### <a name="parameters---orderbyfieldcount"></a>パラメーター - orderByFieldCount

dataSource  

### <a name="return-value---orderbyfieldcount"></a>戻り値 - orderByFieldCount

## <a name="method-origin"></a>メソッド origin

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a>パラメーター - origin

値  

### <a name="return-value---origin"></a>戻り値 - origin

## <a name="method-pack"></a>メソッド pack

コンテナーにクエリをパックし、クエリを作成するときに使用できるようにそのコンテナーを返します。

```xpp
public container pack([boolean doCheck])
```

### <a name="parameters---pack"></a>パラメーター - pack

doCheck  
クエリのデーターソースが外部のカーソルを参照する (クエリのデータソースを外部のカーソルへリンクするなど) ときに、エラーフラグを設定するかどうかを示すブール値; オプション。 既定値は、true で、制約が適用されます。

### <a name="return-value---pack"></a>戻り値 - pack

クエリを保持するコンテナー。

### <a name="remarks---pack"></a>備考 - pack

このメソッドで作成されたコンテナーは、新しいメソッドまたは newObject メソッドのいずれかを使用して query オブジェクトまたは queryRun オブジェクトをインスタンス化するときに入力として機能します。 クエリのデータ ソースとは異なるカーソルへのリンクは、コンテナーにパックされません。 この種類のリンクをパックする必要がある場合は、カーソルのデータのスナップショットを取得し、各フィールドの範囲を作成します。

## <a name="method-packinternals"></a>メソッド packInternals

```xpp
public container packInternals()
```

### <a name="return-value---packinternals"></a>戻り値 - packInternals

## <a name="method-queryfilter"></a>メソッド queryFilter

```xpp
public QueryFilter queryFilter(int count, [QueryBuildDataSource rootDataSource])
```

### <a name="parameters---queryfilter"></a>パラメーター - queryFilter

カウント  

<!-- -->

rootDataSource  

### <a name="return-value---queryfilter"></a>戻り値 - queryFilter

## <a name="method-queryfiltercount"></a>メソッド queryFilterCount

```xpp
public int queryFilterCount([QueryBuildDataSource rootDataSource])
```

### <a name="parameters---queryfiltercount"></a>パラメーター - queryFilterCount

rootDataSource  

### <a name="return-value---queryfiltercount"></a>戻り値 - queryFilterCount

## <a name="method-querytype"></a>メソッド queryType

```xpp
public int queryType([int value])
```

### <a name="parameters---querytype"></a>パラメーター - queryType

値  

### <a name="return-value---querytype"></a>戻り値 - queryType

## <a name="method-quickfiltervalue"></a>メソッド quickFilterValue

```xpp
public str quickFilterValue()
```

### <a name="return-value---quickfiltervalue"></a>戻り値 - quickFilterValue

## <a name="method-quickfiltercontrolid"></a>メソッド quickFilterControlId

```xpp
public int quickFilterControlId()
```

### <a name="return-value---quickfiltercontrolid"></a>戻り値 - quickFilterControlId

## <a name="method-recordlevelsecurity"></a>メソッド recordLevelSecurity

```xpp
public boolean recordLevelSecurity([boolean value])
```

### <a name="parameters---recordlevelsecurity"></a>パラメーター - recordLevelSecurity

値  

### <a name="return-value---recordlevelsecurity"></a>戻り値 - recordLevelSecurity

## <a name="method-report"></a>メソッド report

レポートが存在する場合、クエリが定義されているレポートを返します。

```xpp
public Report report()
```

### <a name="return-value---report"></a>戻り値 - report

クエリがデータ ソース ノードの下で定義されているレポート。

### <a name="remarks---report"></a>備考 - report

クエリは、必ずしもレポートのコンテキストで定義されているとは限りません。 レポートのコンテキストでクエリが定義されているかどうかを確認するには、inReport メソッドを使用します。

## <a name="method-saved"></a>メソッド saved

クエリがディスクに保存されたかどうかを示します。

```xpp
public boolean saved()
```

### <a name="return-value---saved"></a>戻り値 - saved

クエリがディスクに保存されている場合は true。それ以外の場合は、false。

## <a name="method-searchable"></a>メソッド searchable

```xpp
public boolean searchable([boolean value])
```

### <a name="parameters---searchable"></a>パラメーター - searchable

値  

### <a name="return-value---searchable"></a>戻り値 - searchable

## <a name="method-importsession"></a>メソッド importSession

```xpp
public Guid importSession([Guid value])
```

### <a name="parameters---importsession"></a>パラメーター - importSession

値  

### <a name="return-value---importsession"></a>戻り値 - importSession

## <a name="method-title"></a>メソッド title

```xpp
public str title([str value])
```

### <a name="parameters---title"></a>パラメーター - title

値  

### <a name="return-value---title"></a>戻り値 - title

## <a name="method-toprows"></a>メソッド topRows

```xpp
public int topRows([int value])
```

### <a name="parameters---toprows"></a>パラメーター - topRows

値  

### <a name="return-value---toprows"></a>戻り値 - topRows

## <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

現在のオブジェクトを表す文字列。

### <a name="remarks---tostring"></a>備考 - toString

既定の実装は、オブジェクトのクラス名を返します。 ただし、メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、メソッド名、およびインスタンスまたは静的などのメソッドのタイプを返します。

## <a name="method-userupdate"></a>メソッド userUpdate

フェッチされたレコードをクエリが更新できるかどうかを示す値を取得または設定します。

```xpp
public boolean userUpdate([boolean value])
```

### <a name="parameters---userupdate"></a>パラメーター - userUpdate

値  
フェッチされたレコードをクエリが更新できるかどうかを示すブール値; オプション。

### <a name="return-value---userupdate"></a>戻り値 - userUpdate

クエリがフェッチ対象のレコードを現在更新することができる場合は true。それ以外の場合は false。

## <a name="method-validtimestateasofdate"></a>メソッド validTimeStateAsOfDate

```xpp
public Date validTimeStateAsOfDate([Date asOfDate])
```

### <a name="parameters---validtimestateasofdate"></a>パラメーター - validTimeStateAsOfDate

asOfDate  

### <a name="return-value---validtimestateasofdate"></a>戻り値 - validTimeStateAsOfDate

## <a name="method-validtimestateasofdatetime"></a>メソッド validTimeStateAsOfDateTime

```xpp
public DateTime validTimeStateAsOfDateTime([DateTime asOfDateTime])
```

### <a name="parameters---validtimestateasofdatetime"></a>パラメーター - validTimeStateAsOfDateTime

asOfDateTime  

### <a name="return-value---validtimestateasofdatetime"></a>戻り値 - validTimeStateAsOfDateTime

## <a name="method-validtimestateflags"></a>メソッド validTimeStateFlags

```xpp
public int validTimeStateFlags([int value])
```

### <a name="parameters---validtimestateflags"></a>パラメーター - validTimeStateFlags

値  

### <a name="return-value---validtimestateflags"></a>戻り値 - validTimeStateFlags

## <a name="method-version"></a>メソッド version

```xpp
public int version([int value])
```

### <a name="parameters---version"></a>パラメーター - version

値  

### <a name="return-value---version"></a>戻り値 - version

## <a name="method-xml"></a>メソッド xml

現在のオブジェクトを表す XML 文字列を返します。

```xpp
public str xml([int indent])
```

### <a name="parameters---xml"></a>パラメーター - xml

インデント  
返された XML 文字列のインデントの量 (省略可能)。

### <a name="return-value---xml"></a>戻り値 - xml

現在のオブジェクトを表す XML 文字列です。

### <a name="remarks---xml"></a>備考 - xml

このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。

## <a name="method-clearbasequeries"></a>メソッド clearBaseQueries

```xpp
public void clearBaseQueries()
```

## <a name="method-addcompanyrange"></a>メソッド addCompanyRange

```xpp
public void addCompanyRange(str companyName)
```

### <a name="parameters---addcompanyrange"></a>パラメーター - addCompanyRange

companyName  

## <a name="method-checkrangeparsingerrors"></a>メソッド checkRangeParsingErrors

```xpp
public void checkRangeParsingErrors(boolean setCheckRangeParsingErrors)
```

### <a name="parameters---checkrangeparsingerrors"></a>パラメーター - checkRangeParsingErrors

setCheckRangeParsingErrors  

## <a name="method-clearcompanyrange"></a>メソッド clearCompanyRange

```xpp
public void clearCompanyRange()
```

## <a name="method-unpackinternals"></a>メソッド unpackInternals

```xpp
public void unpackInternals(container internalData)
```

### <a name="parameters---unpackinternals"></a>パラメーター - unpackInternals

internalData  

## <a name="method-new"></a>メソッド new

クエリ オブジェクトを作成します。

```xpp
public void new([AnyType source])
```

### <a name="parameters---new"></a>パラメーター - new

ソース  
クエリ オブジェクトを基にするソース (オプション)。

### <a name="remarks---new"></a>備考 - new

このメソッドが呼び出されときに引数が指定されていない場合、将来使用するために、アプリケーション オブジェクト ツリー (AOT) で保存されていない一時的なクエリが作成されます。

## <a name="method-checkfieldaccess"></a>メソッド checkFieldAccess

```xpp
public void checkFieldAccess(boolean setCheckFieldAccess)
```

### <a name="parameters---checkfieldaccess"></a>パラメーター - checkFieldAccess

setCheckFieldAccess  

## <a name="method-usedbcacheongeneratedcursors"></a>メソッド useDbCacheOnGeneratedCursors

```xpp
public void useDbCacheOnGeneratedCursors([int fetchsize])
```

### <a name="parameters---usedbcacheongeneratedcursors"></a>パラメーター - useDbCacheOnGeneratedCursors

fetchsize  

## <a name="method-setvalidtimestatequerytype"></a>メソッド setValidTimeStateQueryType

```xpp
public void setValidTimeStateQueryType([ValidTimeStateQueryType type])
```

### <a name="parameters---setvalidtimestatequerytype"></a>パラメーター - setValidTimeStateQueryType

タイプ  

## <a name="method-validtimestatedaterange"></a>メソッド validTimeStateDateRange

```xpp
public void validTimeStateDateRange([Date fromDate], [Date toDate])
```

### <a name="parameters---validtimestatedaterange"></a>パラメーター - validTimeStateDateRange

fromDate  

<!-- -->

toDate  

## <a name="method-clearhavingfilters"></a>メソッド clearHavingFilters

```xpp
public void clearHavingFilters([QueryBuildDataSource dataSource], [str fieldName], [int occurence], [int arrayIndex])
```

### <a name="parameters---clearhavingfilters"></a>パラメーター - clearHavingFilters

dataSource  

<!-- -->

fieldName  

<!-- -->

occurence  

<!-- -->

arrayIndex  

## <a name="method-quickfilter"></a>メソッド quickFilter

```xpp
public void quickFilter([str dataSourceName], [int tableId], [int fieldId], [str filterValue], [int controlId], [boolean useEqualityComparisonForStrings])
```

### <a name="parameters---quickfilter"></a>パラメーター - quickFilter

dataSourceName  

<!-- -->

tableId  

<!-- -->

fieldId  

<!-- -->

filterValue  

<!-- -->

controlId  

<!-- -->

useEqualityComparisonForStrings  

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-clearqueryfilters"></a>メソッド clearQueryFilters

```xpp
public void clearQueryFilters([QueryBuildDataSource dataSource], [str fieldName], [int occurence], [int arrayIndex])
```

### <a name="parameters---clearqueryfilters"></a>パラメーター - clearQueryFilters

dataSource  

<!-- -->

fieldName  

<!-- -->

occurence  

<!-- -->

arrayIndex  

## <a name="method-clearorderby"></a>メソッド clearOrderBy

```xpp
public void clearOrderBy()
```

## <a name="method-clearallfields"></a>メソッド clearAllFields

```xpp
public void clearAllFields()
```

## <a name="method-cleargroupby"></a>メソッド clearGroupBy

```xpp
public void clearGroupBy()
```

## <a name="method-autoauthzmode"></a>メソッド autoAuthzMode

```xpp
public void autoAuthzMode(AutoAuthzMode mode)
```

### <a name="parameters---autoauthzmode"></a>パラメーター - autoAuthzMode

モード  

## <a name="method-insert_recordset"></a>メソッド insert\_recordset

```xpp
public static void insert_recordset(Common targetCursor, Map targetToSourceMap, Query sourceQuery)
```

### <a name="parameters---insert_recordset"></a>パラメーター - insert\_recordset

targetCursor  

<!-- -->

targetToSourceMap  

<!-- -->

sourceQuery  

## <a name="method-generatecursors"></a>メソッド generateCursors

```xpp
public void generateCursors()
```

## <a name="method-checkauthorizationonopenranges"></a>メソッド checkAuthorizationOnOpenRanges

```xpp
public void checkAuthorizationOnOpenRanges(boolean setCheckAuthorizationOnOpenRanges)
```

### <a name="parameters---checkauthorizationonopenranges"></a>パラメーター - checkAuthorizationOnOpenRanges

setCheckAuthorizationOnOpenRanges  

## <a name="method-addcontains"></a>メソッド addContains

```xpp
public void addContains(str containsValue, [boolean prefixSearch])
```

### <a name="parameters---addcontains"></a>パラメーター -addContains

containsValue  

<!-- -->

prefixSearch  

## <a name="method-resetvalidtimestatequerytype"></a>メソッド resetValidTimeStateQueryType

```xpp
public void resetValidTimeStateQueryType()
```

## <a name="method-validtimestatedatetimerange"></a>メソッド validTimeStateDateTimeRange

```xpp
public void validTimeStateDateTimeRange([DateTime fromDateTime], [DateTime toDateTime])
```

### <a name="parameters---validtimestatedatetimerange"></a>パラメーター - validTimeStateDateTimeRange

fromDateTime  

<!-- -->

toDateTime  

