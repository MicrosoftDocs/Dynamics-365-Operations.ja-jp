---
title: Q クラス
description: 文字 Q で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 11/07/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 51831
ms.assetid: 279efb4c-e228-4ab5-be7d-c96d91064787
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85bab7b4a98e351e45157e1168939d30e08b0505
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537032"
---
# <a name="q-classes"></a>Q クラス

[!include [banner](../includes/banner.md)]

文字 Q で始まるシステム API クラス。

<a name="class-query"></a>クラス クエリ
-----------

    class Query extends TreeNode

クエリ クラスには、クエリの構造が含まれます。

### <a name="remarks"></a>備考

このタイプのオブジェクトは、データベースからレコードをフェッチするために使用されません。 代わりに、クエリ オブジェクトを割り当てることができる QueryRun オブジェクトを使用します。 クエリの動的な動作は、QueryRun クラスによって定義されます。 静的なビヘイビアーは、Query クラスによって定義されます。 クエリには、データベース内のテーブルに対応する 1 つまたは複数のデータ ソースが含まれます。 データ ソースを指定するには、QueryBuildDataSource オブジェクトを使用します。 このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。 クエリは、ユーザーが、たとえばフォームなどによりフェッチされるレコードを変更する場合に使用されます。 多くの場合、1 つ以上の範囲は既存のデータ ソースに追加されます。 範囲を指定するには、queryBuildRange オブジェクトを使用します。

### <a name="examples"></a>例

次の例では、QueryRun オブジェクトを作成するために使用されるクエリ オブジェクトを作成します。

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

### <a name="methods"></a>メソッド

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
| public str name(\[str value\])                                                                                                                                         | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
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

### <a name="method-addbasequery"></a>メソッド addBaseQuery

    public Query addBaseQuery(str queryName)

#### <a name="parameters"></a>パラメーター

queryName  

#### <a name="return-value"></a>戻り値

### <a name="method-adddatasource"></a>メソッド addDataSource

クエリのトップ レベルにデータ ソースを追加します。

    public QueryBuildDataSource addDataSource(TableId table, [str name], [UnionType unionType], [boolean emptyFieldList])

#### <a name="parameters"></a>パラメーター

テーブル  

<!-- -->

名前  

<!-- -->

unionType  

<!-- -->

emptyFieldList  

#### <a name="return-value"></a>戻り値

作成されたデータ ソース オブジェクト。

#### <a name="remarks"></a>備考

文書作成のために名前の値を指定できます。 dataSourceName メソッドを使用してデータ ソースをフェッチする名前を使用することができます。

### <a name="method-addhavingfilter"></a>メソッド addHavingFilter

    public QueryHavingFilter addHavingFilter(QueryBuildDataSource dataSource, str fieldName, AggregateFunction aggregateFunction, [int arrayIndex])

#### <a name="parameters"></a>パラメーター

dataSource  

<!-- -->

fieldName  

<!-- -->

aggregateFunction  

<!-- -->

arrayIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-addqueryfilter"></a>メソッド addQueryFilter

    public QueryFilter addQueryFilter(QueryBuildDataSource dataSource, str fieldName, [int arrayIndex])

#### <a name="parameters"></a>パラメーター

dataSource  

<!-- -->

fieldName  

<!-- -->

arrayIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-allowcheck"></a>メソッド allowCheck

    public boolean allowCheck([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-allowcrosscompany"></a>メソッド allowCrossCompany

    public boolean allowCrossCompany([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-allowhavingfilters"></a>メソッド allowHavingFilters

    public boolean allowHavingFilters(QueryBuildDataSource dataSource, FieldName fieldName, AggregateFunction aggregateFunction)

#### <a name="parameters"></a>パラメーター

dataSource  

<!-- -->

fieldName  

<!-- -->

aggregateFunction  

#### <a name="return-value"></a>戻り値

### <a name="method-allowqueryfilters"></a>メソッド allowQueryFilters

    public boolean allowQueryFilters(QueryBuildDataSource dataSource)

#### <a name="parameters"></a>パラメーター

dataSource  

#### <a name="return-value"></a>戻り値

### <a name="method-changedby"></a>メソッド changedBy

クエリ オブジェクトを最後に変更したユーザーの名前を取得または設定します。

    public str changedBy([str value])

#### <a name="parameters"></a>パラメーター

値  
クエリ オブジェクトを最後に変更したユーザーの名前 (オプション)。

#### <a name="return-value"></a>戻り値

クエリ オブジェクトを最後に変更したユーザーの名前。

### <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

    public Date changedDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された日付。

### <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

    public str changedTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された時間。

### <a name="method-childdatasourcecount"></a>メソッド childDataSourceCount

クエリに関連するデータ ソースの数をカウントします。

    public int childDataSourceCount()

#### <a name="return-value"></a>戻り値

このクエリに関連するデータ ソースの数。

#### <a name="remarks"></a>備考

このメソッドは、トップレベルのクエリに使用されます。 別のデータ ソースに埋め込まれているデータ ソースの数を確認するには、childDataSourceCount メソッドを使用します。

### <a name="method-childdatasourceno"></a>メソッド childDataSourceNo

指定された番号に対応するデータ ソースを返します。

    public QueryBuildDataSource childDataSourceNo(int dataSourceNo)

#### <a name="parameters"></a>パラメーター

dataSourceNo  
子データ ソースの番号。

#### <a name="return-value"></a>戻り値

指定された番号を持つ子データ ソース。

#### <a name="remarks"></a>備考

指定された数値は、クエリのすぐ下にあるデータ ソースを表す必要があります。 通常、このようなデータ ソースは 1 つだけです。

### <a name="method-containsaggregatefields"></a>メソッド containsAggregateFields

    public boolean containsAggregateFields()

#### <a name="return-value"></a>戻り値

### <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

    public str createdBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

    public Date creationDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが作成された日付。

### <a name="method-creationtime"></a>メソッド creationTime

    public str creationTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datasourcecount"></a>メソッド dataSourceCount

埋め込みデータ ソースを含む、クエリのデータ ソースの合計数を返します。

    public int dataSourceCount()

#### <a name="return-value"></a>戻り値

このクエリのデータ ソースの数。

#### <a name="remarks"></a>備考

この番号は、データ ソースの推移的な番号であり、任意の埋め込みデータ ソースが含まれています。

### <a name="method-datasourcename"></a>メソッド dataSourceName

指定された名前を持つデータ ソースを返します。

    public QueryBuildDataSource dataSourceName(str name)

#### <a name="parameters"></a>パラメーター

名前  
返すデータソースの名前を含む文字列。

#### <a name="return-value"></a>戻り値

指定した名前を持つデータ ソース。指定されたデータ ソースが存在しない場合は、初期化されていないオブジェクト。

### <a name="method-datasourceno"></a>メソッド dataSourceNo

データ ソース番号により指定されたデータ ソースを返します。

    public QueryBuildDataSource dataSourceNo(int dataSourceNo)

#### <a name="parameters"></a>パラメーター

dataSourceNo  
データ ソースの番号。

#### <a name="return-value"></a>戻り値

指定した番号を持つデータ ソース。指定されたデータ ソースが存在しない場合は、初期化されていないオブジェクト。

### <a name="method-datasourcetable"></a>メソッド dataSourceTable

指定されたテーブルが割り当てられているデータ ソースを返します。

    public QueryBuildDataSource dataSourceTable(TableId table, [int occurrence])

#### <a name="parameters"></a>パラメーター

テーブル  
複数のデータ ソースが指定されたテーブル ID を使用する場合に使用される整数。オプション。 既定値は 1で、最初の (通常は唯一の) インスタンスを指定します。

<!-- -->

occurrence  
複数のデータ ソースが指定されたテーブル ID を使用する場合に使用される整数。オプション。 既定値は 1で、最初の (通常は唯一の) インスタンスを指定します。

#### <a name="return-value"></a>戻り値

指定されたテーブルが割り当てられているデータ ソース。

#### <a name="remarks"></a>備考

データ ソースは、dataSourceNo メソッドまたは dataSourceName メソッドを呼び出すことによって取得することもできます。

### <a name="method-datasourceuniqueid"></a>メソッド dataSourceUniqueId

    public QueryBuildDataSource dataSourceUniqueId(int uniqueId)

#### <a name="parameters"></a>パラメーター

uniqueId  

#### <a name="return-value"></a>戻り値

### <a name="method-description"></a>メソッドの説明

    public str description([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-equal"></a>メソッド equal

あるクエリが別のクエリと等しいかどうかを評価します。

    public boolean equal(Object record)

#### <a name="parameters"></a>パラメーター

記録  
比較として使用するクエリです。

#### <a name="return-value"></a>戻り値

クエリが等しい場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

この場合、「等しい」は、クエリが比較されるクエリと構造的に同一であることを意味します。 クエリには、同じファイルに割り当てられたデータ ソースと同じ数のデータ ソースがあり、同じ数の範囲があります。

### <a name="method-exportxml"></a>メソッド exportXML

    public str exportXML()

#### <a name="return-value"></a>戻り値

### <a name="method-findhavingfilterbyfield"></a>メソッド findHavingFilterByField

    public QueryHavingFilter findHavingFilterByField(QueryBuildDataSource dataSource, FieldName fieldName, [int occurrence], [int arrayIndex])

#### <a name="parameters"></a>パラメーター

dataSource  

<!-- -->

fieldName  

<!-- -->

occurrence  

<!-- -->

arrayIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-findqueryfilter"></a>メソッド findQueryFilter

    public QueryFilter findQueryFilter(QueryBuildDataSource dataSource, FieldName fieldName, [int occurrence], [int arrayIndex])

#### <a name="parameters"></a>パラメーター

dataSource  

<!-- -->

fieldName  

<!-- -->

occurrence  

<!-- -->

arrayIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-firsttopleveldatasource"></a>メソッド firstTopLevelDataSource

    public QueryBuildDataSource firstTopLevelDataSource()

#### <a name="return-value"></a>戻り値

### <a name="method-forcenestedloop"></a>メソッド forceNestedLoop

    public boolean forceNestedLoop(boolean arg)

#### <a name="parameters"></a>パラメーター

arg  

#### <a name="return-value"></a>戻り値

### <a name="method-forceselectorder"></a>メソッド forceSelectOrder

    public boolean forceSelectOrder(boolean arg)

#### <a name="parameters"></a>パラメーター

arg  

#### <a name="return-value"></a>戻り値

### <a name="method-form"></a>メソッド form

    public str form([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-getcompanyrange"></a>メソッド getCompanyRange

    public container getCompanyRange()

#### <a name="return-value"></a>戻り値

### <a name="method-getmostrestrictedqueryfilterstatus"></a>メソッド getMostRestrictedQueryFilterStatus

    public int getMostRestrictedQueryFilterStatus(QueryBuildDataSource dataSource, FieldName fieldName, [int fieldId])

#### <a name="parameters"></a>パラメーター

dataSource  

<!-- -->

fieldName  

<!-- -->

fieldId  

#### <a name="return-value"></a>戻り値

### <a name="method-getnextuniqueid"></a>メソッド getNextUniqueId

    public int getNextUniqueId()

#### <a name="return-value"></a>戻り値

### <a name="method-getsqlstatement"></a>メソッド getSQLStatement

    public str getSQLStatement([boolean noRuntimeOptimization])

#### <a name="parameters"></a>パラメーター

noRuntimeOptimization  

#### <a name="return-value"></a>戻り値

### <a name="method-getvalidtimestatedaterange"></a>メソッド getValidTimeStateDateRange

    public container getValidTimeStateDateRange()

#### <a name="return-value"></a>戻り値

### <a name="method-getvalidtimestatedatetimerange"></a>メソッド getValidTimeStateDateTimeRange

    public container getValidTimeStateDateTimeRange()

#### <a name="return-value"></a>戻り値

### <a name="method-getvalidtimestatequerytype"></a>メソッド getValidTimeStateQueryType

    public ValidTimeStateQueryType getValidTimeStateQueryType()

#### <a name="return-value"></a>戻り値

### <a name="method-groupbyfield"></a>メソッド groupByField

    public QueryGroupByField groupByField(int index, [QueryBuildDataSource dataSource])

#### <a name="parameters"></a>パラメーター

指数  

<!-- -->

dataSource  

#### <a name="return-value"></a>戻り値

### <a name="method-groupbyfieldcount"></a>メソッド groupByFieldCount

    public int groupByFieldCount([QueryBuildDataSource dataSource])

#### <a name="parameters"></a>パラメーター

dataSource  

#### <a name="return-value"></a>戻り値

### <a name="method-hasmultipletopleveldatasource"></a>メソッド hasMultipleTopLevelDataSource

    public boolean hasMultipleTopLevelDataSource()

#### <a name="return-value"></a>戻り値

### <a name="method-hasrangeorfilter"></a>メソッド hasRangeOrFilter

    public boolean hasRangeOrFilter(QueryBuildDataSource dataSource)

#### <a name="parameters"></a>パラメーター

dataSource  

#### <a name="return-value"></a>戻り値

### <a name="method-havingfilter"></a>メソッド havingFilter

    public QueryHavingFilter havingFilter(int count, [QueryBuildDataSource dataSource])

#### <a name="parameters"></a>パラメーター

カウント  

<!-- -->

dataSource  

#### <a name="return-value"></a>戻り値

### <a name="method-havingfiltercount"></a>メソッド havingFilterCount

    public int havingFilterCount([QueryBuildDataSource dataSource])

#### <a name="parameters"></a>パラメーター

dataSource  

#### <a name="return-value"></a>戻り値

### <a name="method-inreport"></a>メソッド inReport

クエリがレポートの一部であるかどうかを決定します。

    public boolean inReport()

#### <a name="return-value"></a>戻り値

クエリがレポートの一部である場合は (レポートのデータ ソース ノードの下にある場合は) true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

この関数は、通常アプリケーション コードでは使用されません。 メソッドが true を返す場合は、レポート メソッドはクエリが定義されているレポートにアクセスするために使用することができます。

### <a name="method-interactive"></a>メソッド interactive

クエリが対話的かどうかを指定します。

    public boolean interactive([boolean value])

#### <a name="parameters"></a>パラメーター

値  
クエリがインタラクティブかどうかを示す値、オプション。

#### <a name="return-value"></a>戻り値

クエリが対話形式である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

対話型クエリでは、たとえば prompt メソッドが呼び出されたときに、クエリはユーザーにダイアログ ボックスを提示できます。 この機能は、コードをバッチに送信する場合や、コードを無人で実行する必要がある場合に使用されます。

### <a name="method-iscompositequery"></a>メソッド isCompositeQuery

    public boolean isCompositeQuery()

#### <a name="return-value"></a>戻り値

### <a name="method-isexplicitlyordered"></a>メソッド isExplicitlyOrdered

    public boolean isExplicitlyOrdered()

#### <a name="return-value"></a>戻り値

### <a name="method-isexplicitlygrouped"></a>メソッド isExplicitlyGrouped

    public boolean isExplicitlyGrouped()

#### <a name="return-value"></a>戻り値

### <a name="method-ispureunionall"></a>メソッド isPureUnionAll

    public boolean isPureUnionAll()

#### <a name="return-value"></a>戻り値

### <a name="method-isuniontype"></a>メソッド isUnionType

    public boolean isUnionType()

#### <a name="return-value"></a>戻り値

### <a name="method-levelno"></a>メソッド levelNo

指定されたデータ ソースのインデントのレベルを決定します。

    public int levelNo(int dataSourceNo)

#### <a name="parameters"></a>パラメーター

dataSourceNo  
データ ソースのレベルを決定する番号。

#### <a name="return-value"></a>戻り値

指定されたデータ ソースのレベル番号。

#### <a name="remarks"></a>備考

データソースは、1 から順に番号付けされます。

### <a name="method-leveltable"></a>メソッド levelTable

指定したテーブルに割り当てられているデータ ソースのツリー レベルを、データ ソースの階層内で決定します。

    public int levelTable(TableId table, [int occurrence])

#### <a name="parameters"></a>パラメーター

テーブル  
複数のデータ ソースが同じテーブルに割り当てられる場合に使用される整数。オプション。

<!-- -->

occurrence  
複数のデータ ソースが同じテーブルに割り当てられる場合に使用される整数。オプション。

#### <a name="return-value"></a>戻り値

クエリの指定されたデータ ソースのレベル番号。

### <a name="method-literals"></a>メソッド literals

    public int literals([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-newobject"></a>メソッド newObject

ソース クエリとして同じクライアント側、またはサーバー側で存在するクエリを作成します。

    public Query newObject(AnyType source)

#### <a name="parameters"></a>パラメーター

ソース  
ソース クエリ。

#### <a name="return-value"></a>戻り値

新しいクエリ。

### <a name="method-nextuniqueid"></a>メソッド nextUniqueId

    public int nextUniqueId([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-orderbyfield"></a>メソッド orderByField

    public QueryOrderByField orderByField(int index, [QueryBuildDataSource dataSource])

#### <a name="parameters"></a>パラメーター

指数  

<!-- -->

dataSource  

#### <a name="return-value"></a>戻り値

### <a name="method-orderbyfieldcount"></a>メソッド orderByFieldCount

    public int orderByFieldCount([QueryBuildDataSource dataSource])

#### <a name="parameters"></a>パラメーター

dataSource  

#### <a name="return-value"></a>戻り値

### <a name="method-origin"></a>メソッド origin

    public Guid origin([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-pack"></a>メソッド pack

コンテナーにクエリをパックし、クエリを作成するときに使用できるようにそのコンテナーを返します。

    public container pack([boolean doCheck])

#### <a name="parameters"></a>パラメーター

doCheck  
クエリのデーターソースが外部のカーソルを参照する (クエリのデータソースを外部のカーソルへリンクするなど) ときに、エラーフラグを設定するかどうかを示すブール値; オプション。 既定値は、true で、制約が適用されます。

#### <a name="return-value"></a>戻り値

クエリを保持するコンテナー。

#### <a name="remarks"></a>備考

このメソッドで作成されたコンテナーは、新しいメソッドまたは newObject メソッドのいずれかを使用して query オブジェクトまたは queryRun オブジェクトをインスタンス化するときに入力として機能します。 クエリのデータ ソースとは異なるカーソルへのリンクは、コンテナーにパックされません。 この種類のリンクをパックする必要がある場合は、カーソルのデータのスナップショットを取得し、各フィールドの範囲を作成します。

### <a name="method-packinternals"></a>メソッド packInternals

    public container packInternals()

#### <a name="return-value"></a>戻り値

### <a name="method-queryfilter"></a>メソッド queryFilter

    public QueryFilter queryFilter(int count, [QueryBuildDataSource rootDataSource])

#### <a name="parameters"></a>パラメーター

カウント  

<!-- -->

rootDataSource  

#### <a name="return-value"></a>戻り値

### <a name="method-queryfiltercount"></a>メソッド queryFilterCount

    public int queryFilterCount([QueryBuildDataSource rootDataSource])

#### <a name="parameters"></a>パラメーター

rootDataSource  

#### <a name="return-value"></a>戻り値

### <a name="method-querytype"></a>メソッド queryType

    public int queryType([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-quickfiltervalue"></a>メソッド quickFilterValue

    public str quickFilterValue()

#### <a name="return-value"></a>戻り値

### <a name="method-quickfiltercontrolid"></a>メソッド quickFilterControlId

    public int quickFilterControlId()

#### <a name="return-value"></a>戻り値

### <a name="method-recordlevelsecurity"></a>メソッド recordLevelSecurity

    public boolean recordLevelSecurity([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-report"></a>メソッド report

レポートが存在する場合、クエリが定義されているレポートを返します。

    public Report report()

#### <a name="return-value"></a>戻り値

クエリがデータ ソース ノードの下で定義されているレポート。

#### <a name="remarks"></a>備考

クエリは、必ずしもレポートのコンテキストで定義されているとは限りません。 レポートのコンテキストでクエリが定義されているかどうかを確認するには、inReport メソッドを使用します。

### <a name="method-saved"></a>メソッド saved

クエリがディスクに保存されたかどうかを示します。

    public boolean saved()

#### <a name="return-value"></a>戻り値

クエリがディスクに保存されている場合は true。それ以外の場合は、false。

### <a name="method-searchable"></a>メソッド searchable

    public boolean searchable([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-importsession"></a>メソッド importSession

    public Guid importSession([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-title"></a>メソッド title

    public str title([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-toprows"></a>メソッド topRows

    public int topRows([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 ただし、メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、メソッド名、およびインスタンスまたは静的などのメソッドのタイプを返します。

### <a name="method-userupdate"></a>メソッド userUpdate

フェッチされたレコードをクエリが更新できるかどうかを示す値を取得または設定します。

    public boolean userUpdate([boolean value])

#### <a name="parameters"></a>パラメーター

値  
フェッチされたレコードをクエリが更新できるかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

クエリがフェッチ対象のレコードを現在更新することができる場合は true。それ以外の場合は false。

### <a name="method-validtimestateasofdate"></a>メソッド validTimeStateAsOfDate

    public Date validTimeStateAsOfDate([Date asOfDate])

#### <a name="parameters"></a>パラメーター

asOfDate  

#### <a name="return-value"></a>戻り値

### <a name="method-validtimestateasofdatetime"></a>メソッド validTimeStateAsOfDateTime

    public DateTime validTimeStateAsOfDateTime([DateTime asOfDateTime])

#### <a name="parameters"></a>パラメーター

asOfDateTime  

#### <a name="return-value"></a>戻り値

### <a name="method-validtimestateflags"></a>メソッド validTimeStateFlags

    public int validTimeStateFlags([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-version"></a>メソッド version

    public int version([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-xml"></a>メソッド xml

現在のオブジェクトを表す XML 文字列を返します。

    public str xml([int indent])

#### <a name="parameters"></a>パラメーター

インデント  
返された XML 文字列のインデントの量 (省略可能)。

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す XML 文字列です。

#### <a name="remarks"></a>備考

このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。

### <a name="method-clearbasequeries"></a>メソッド clearBaseQueries

    public void clearBaseQueries()

### <a name="method-addcompanyrange"></a>メソッド addCompanyRange

    public void addCompanyRange(str companyName)

#### <a name="parameters"></a>パラメーター

companyName  

### <a name="method-checkrangeparsingerrors"></a>メソッド checkRangeParsingErrors

    public void checkRangeParsingErrors(boolean setCheckRangeParsingErrors)

#### <a name="parameters"></a>パラメーター

setCheckRangeParsingErrors  

### <a name="method-clearcompanyrange"></a>メソッド clearCompanyRange

    public void clearCompanyRange()

### <a name="method-unpackinternals"></a>メソッド unpackInternals

    public void unpackInternals(container internalData)

#### <a name="parameters"></a>パラメーター

internalData  

### <a name="method-new"></a>メソッド new

クエリ オブジェクトを作成します。

    public void new([AnyType source])

#### <a name="parameters"></a>パラメーター

ソース  
クエリ オブジェクトを基にするソース (オプション)。

#### <a name="remarks"></a>備考

このメソッドが呼び出されときに引数を指定すると、将来使用するために、Finance and Operations アプリケーション オブジェクト ツリー (AOT) で保存されていない一時的なクエリが作成されます。

### <a name="method-checkfieldaccess"></a>メソッド checkFieldAccess

    public void checkFieldAccess(boolean setCheckFieldAccess)

#### <a name="parameters"></a>パラメーター

setCheckFieldAccess  

### <a name="method-usedbcacheongeneratedcursors"></a>メソッド useDbCacheOnGeneratedCursors

    public void useDbCacheOnGeneratedCursors([int fetchsize])

#### <a name="parameters"></a>パラメーター

fetchsize  

### <a name="method-setvalidtimestatequerytype"></a>メソッド setValidTimeStateQueryType

    public void setValidTimeStateQueryType([ValidTimeStateQueryType type])

#### <a name="parameters"></a>パラメーター

タイプ  

### <a name="method-validtimestatedaterange"></a>メソッド validTimeStateDateRange

    public void validTimeStateDateRange([Date fromDate], [Date toDate])

#### <a name="parameters"></a>パラメーター

fromDate  

<!-- -->

toDate  

### <a name="method-clearhavingfilters"></a>メソッド clearHavingFilters

    public void clearHavingFilters([QueryBuildDataSource dataSource], [str fieldName], [int occurence], [int arrayIndex])

#### <a name="parameters"></a>パラメーター

dataSource  

<!-- -->

fieldName  

<!-- -->

occurence  

<!-- -->

arrayIndex  

### <a name="method-quickfilter"></a>メソッド quickFilter

    public void quickFilter([str dataSourceName], [int tableId], [int fieldId], [str filterValue], [int controlId], [boolean useEqualityComparisonForStrings])

#### <a name="parameters"></a>パラメーター

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

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-clearqueryfilters"></a>メソッド clearQueryFilters

    public void clearQueryFilters([QueryBuildDataSource dataSource], [str fieldName], [int occurence], [int arrayIndex])

#### <a name="parameters"></a>パラメーター

dataSource  

<!-- -->

fieldName  

<!-- -->

occurence  

<!-- -->

arrayIndex  

### <a name="method-clearorderby"></a>メソッド clearOrderBy

    public void clearOrderBy()

### <a name="method-clearallfields"></a>メソッド clearAllFields

    public void clearAllFields()

### <a name="method-cleargroupby"></a>メソッド clearGroupBy

    public void clearGroupBy()

### <a name="method-autoauthzmode"></a>メソッド autoAuthzMode

    public void autoAuthzMode(AutoAuthzMode mode)

#### <a name="parameters"></a>パラメーター

モード  

### <a name="method-insertrecordset"></a>メソッド insert\_recordset

    public static void insert_recordset(Common targetCursor, Map targetToSourceMap, Query sourceQuery)

#### <a name="parameters"></a>パラメーター

targetCursor  

<!-- -->

targetToSourceMap  

<!-- -->

sourceQuery  

### <a name="method-generatecursors"></a>メソッド generateCursors

    public void generateCursors()

### <a name="method-checkauthorizationonopenranges"></a>メソッド checkAuthorizationOnOpenRanges

    public void checkAuthorizationOnOpenRanges(boolean setCheckAuthorizationOnOpenRanges)

#### <a name="parameters"></a>パラメーター

setCheckAuthorizationOnOpenRanges  

### <a name="method-addcontains"></a>メソッド addContains

    public void addContains(str containsValue, [boolean prefixSearch])

#### <a name="parameters"></a>パラメーター

containsValue  

<!-- -->

prefixSearch  

### <a name="method-resetvalidtimestatequerytype"></a>メソッド resetValidTimeStateQueryType

    public void resetValidTimeStateQueryType()

### <a name="method-validtimestatedatetimerange"></a>メソッド validTimeStateDateTimeRange

    public void validTimeStateDateTimeRange([DateTime fromDateTime], [DateTime toDateTime])

#### <a name="parameters"></a>パラメーター

fromDateTime  

<!-- -->

toDateTime  

## <a name="class-querybuilddatasource"></a>クラス QueryBuildDataSource
    class QueryBuildDataSource extends TreeNode

QueryBuildDataSource クラスは、クエリが構成されているレポート パーツを提供します。

### <a name="remarks"></a>備考

データ ソースは、データ ソースに割り当てられたテーブルからレコードがフェッチされる順序を定義する階層内で配置されます。 各データ ソースでは、レコードがフェッチされる順序および選択されたレコードによって満たされなければならない基準を定義します。 このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

    {    QueryBuildDataSource ds;    Query q = new Query();        ds = q.addDataSource(        TableNum(CustTable));}

### <a name="methods"></a>メソッド

| 方法                                                                                                                                                       | 説明                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public int addAllFields(TableName tableName)                                                                                                                 |                                                                                                                                           |
| public QueryBuildDataSource addDataSource(AnyType arg, \[str name\], \[boolean emptyFieldList\])                                                             | このデータ ソースに埋め込まれているデータ ソースを追加します。                                                                                  |
| public QueryBuildDynalink addDynalink(FieldId field, Common dynamicFile, FieldId dynamicField, \[int fieldArrayIndex\], \[int dynamicFieldArrayIndex\])      |                                                                                                                                           |
| public QueryBuildLink addForeignkeyRelation(str relatedTableRole, \[str parentDatasourceName\])                                                              |                                                                                                                                           |
| public QueryGroupByField addGroupByField(FieldId fieldID, \[int arrayIndex\])                                                                                |                                                                                                                                           |
| public QueryBuildLink addLink(FieldId parentField, FieldId thisField, \[str parentDatasourceName\])                                                          |                                                                                                                                           |
| public QueryOrderByField addOrderByAggregateField(SelectionField fieldType, FieldId fieldID, \[SortOrder direction\], \[int arrayIndex\])                    |                                                                                                                                           |
| public QueryOrderByField addOrderByCalculationField(Microsoft.Dynamics.AX.Analytics.CalculationModel.NumericExpression calculation, \[SortOrder direction\]) |                                                                                                                                           |
| public QueryOrderByField addOrderByField(FieldId fieldID, \[SortOrder direction\], \[int arrayIndex\])                                                       |                                                                                                                                           |
| public QueryBuildRange addRange(FieldId field, \[int arrayIndex\], \[QueryRangeType rangeType\])                                                             | データ ソースに範囲を追加します。                                                                                                          |
| public int addSortField(FieldId sortField, \[SortOrder direction\], \[int arrayIndex\])                                                                      |                                                                                                                                           |
| public int addSortIndex(IndexId index)                                                                                                                       |                                                                                                                                           |
| public int allowAdd(\[int value\])                                                                                                                           |                                                                                                                                           |
| public boolean applyFilter(FilterValue filterValue)                                                                                                          |                                                                                                                                           |
| public boolean autoHeader(FieldId field, \[boolean orderNo\])                                                                                                |                                                                                                                                           |
| public int autoHeaderDetailLevel(FieldId field, \[int orderNo\])                                                                                             |                                                                                                                                           |
| public boolean autoSum(FieldId field, \[boolean orderNo\])                                                                                                   |                                                                                                                                           |
| public int autoSumDetailLevel(FieldId field, \[int orderNo\])                                                                                                |                                                                                                                                           |
| public boolean changedNo()                                                                                                                                   |                                                                                                                                           |
| public int childDataSourceCount()                                                                                                                            |                                                                                                                                           |
| public QueryBuildDataSource childDataSourceNo(int dataSourceNo)                                                                                              |                                                                                                                                           |
| public str company(\[str value\])                                                                                                                            |                                                                                                                                           |
| public int concurrencyModel(\[int value\])                                                                                                                   |                                                                                                                                           |
| public QueryBuildDynalink dynalink(int dynalinkNo)                                                                                                           |                                                                                                                                           |
| public int dynalinkCount()                                                                                                                                   |                                                                                                                                           |
| public boolean embedded()                                                                                                                                    |                                                                                                                                           |
| public boolean enabled(\[boolean value\])                                                                                                                    | オブジェクトを有効または無効にするかどうかを決定します。                                                                                       |
| public boolean existsMeanOrExists(\[boolean value\])                                                                                                         |                                                                                                                                           |
| public int fetchMode(\[int value\])                                                                                                                          |                                                                                                                                           |
| public QueryBuildFieldList fields()                                                                                                                          |                                                                                                                                           |
| public TableId file()                                                                                                                                        |                                                                                                                                           |
| public QueryBuildRange findRange(FieldId field, \[int occurrence\], \[int arrayIndex\])                                                                      |                                                                                                                                           |
| public boolean firstFast(\[boolean value\])                                                                                                                  | 他のレコードの前にクエリから最初のレコードを取得するかどうかを決定します。                                                  |
| public boolean firstOnly(\[boolean value\])                                                                                                                  |                                                                                                                                           |
| public int getMostRestrictedQueryBuildRangeStatus(FieldId field, \[int occurrence\], \[int arrayIndex\])                                                     |                                                                                                                                           |
| public Common getNo()                                                                                                                                        |                                                                                                                                           |
| public int id()                                                                                                                                              |                                                                                                                                           |
| public boolean indexIsHint(boolean arg)                                                                                                                      |                                                                                                                                           |
| public boolean isPartOfSubQueryInBaseQuery()                                                                                                                 |                                                                                                                                           |
| public boolean joined()                                                                                                                                      |                                                                                                                                           |
| public container joinedDataSources()                                                                                                                         |                                                                                                                                           |
| public int joinMode(\[int value\])                                                                                                                           |                                                                                                                                           |
| public str label(\[str value\])                                                                                                                              | コントロールのラベルを取得または設定します。                                                                                                     |
| public int level()                                                                                                                                           |                                                                                                                                           |
| public QueryBuildLink link(int associationNo)                                                                                                                |                                                                                                                                           |
| public int linkCount()                                                                                                                                       |                                                                                                                                           |
| public str name(\[str value\])                                                                                                                               | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public container oneToOneDataSources()                                                                                                                       |                                                                                                                                           |
| public int orderMode(\[int value\])                                                                                                                          |                                                                                                                                           |
| public QueryBuildDataSource parentDataSource()                                                                                                               |                                                                                                                                           |
| public str policyContext(\[str value\])                                                                                                                      |                                                                                                                                           |
| public QueryBuildRange range(int rangeNo)                                                                                                                    |                                                                                                                                           |
| public int rangeCount()                                                                                                                                      |                                                                                                                                           |
| public QueryBuildRange rangeField(FieldId field, \[int occurrence\])                                                                                         |                                                                                                                                           |
| public boolean relations(\[boolean value\])                                                                                                                  |                                                                                                                                           |
| public int selectionCount()                                                                                                                                  |                                                                                                                                           |
| public boolean selectWithRepeatableRead(\[boolean value\])                                                                                                   |                                                                                                                                           |
| public SortOrder sortDirection(FieldId field, \[SortOrder direction\])                                                                                       |                                                                                                                                           |
| public FieldId sortField(FieldId field)                                                                                                                      |                                                                                                                                           |
| public int sortFieldCount()                                                                                                                                  |                                                                                                                                           |
| public IndexId sortIndex(int indexNo)                                                                                                                        |                                                                                                                                           |
| public int sortIndexCount()                                                                                                                                  |                                                                                                                                           |
| public QueryBuildStaticlink staticlink(int staticlinkNo)                                                                                                     | クエリのデータ ソースで静的リンク オブジェクトを返します。                                                                                  |
| public int staticlinkCount()                                                                                                                                 | QueryBuildDataSource オブジェクトに対して定義されている静的リンクの数が与えられます。                                                     |
| public TableId table(\[TableId value\])                                                                                                                      | オブジェクトに関連付けられているテーブル ID を取得または設定します。                                                                             |
| public str toString()                                                                                                                                        | 現在のオブジェクトを表す文字列を返します。                                                                                      |
| public int unionType(\[int value\])                                                                                                                          |                                                                                                                                           |
| public int uniqueId()                                                                                                                                        |                                                                                                                                           |
| public boolean update(\[boolean value\])                                                                                                                     | このデータ ソースによってフェッチされたレコードを更新できるかどうかを決定します。                                                                |
| public void clearLinks()                                                                                                                                     |                                                                                                                                           |
| public void clearDynalinks()                                                                                                                                 |                                                                                                                                           |
| public void clearRange(FieldId field, \[int occurrence\])                                                                                                    |                                                                                                                                           |
| public void sortClear()                                                                                                                                      |                                                                                                                                           |
| public void finalize()                                                                                                                                       |                                                                                                                                           |
| public void addSelectionFieldWithAlias(str alias, FieldId field, \[SelectionField fieldType\])                                                               |                                                                                                                                           |
| public void addCalculationField(Microsoft.Dynamics.AX.Analytics.CalculationModel.NumericExpression calculation, str alias)                                   |                                                                                                                                           |
| public void addForeignKeyDynalink(Common dynamicFile, str relatedRole)                                                                                       |                                                                                                                                           |
| public void addRelation(DictRelation relation, \[TableScope tableScope\])                                                                                    |                                                                                                                                           |
| public void clearSortIndex()                                                                                                                                 |                                                                                                                                           |
| public void clearRanges()                                                                                                                                    | データ ソースに関連付けられているすべての範囲を削除します。                                                                              |
| public void linkFields(str parentField, str thisField, \[str parentDatasourceName\])                                                                         |                                                                                                                                           |
| public void addSelectionField(FieldId field, \[SelectionField fieldType\], \[int arrayIndex\])                                                               |                                                                                                                                           |

### <a name="method-addallfields"></a>メソッド addAllFields

    public int addAllFields(TableName tableName)

#### <a name="parameters"></a>パラメーター

tableName  

#### <a name="return-value"></a>戻り値

### <a name="method-adddatasource"></a>メソッド addDataSource

このデータ ソースに埋め込まれているデータ ソースを追加します。

    public QueryBuildDataSource addDataSource(AnyType arg, [str name], [boolean emptyFieldList])

#### <a name="parameters"></a>パラメーター

arg  

<!-- -->

名前  

<!-- -->

emptyFieldList  

#### <a name="return-value"></a>戻り値

新しいデータ ソースを選択します。

#### <a name="remarks"></a>備考

最上位レベルのデータ ソースは、addDataSource メソッドを使用して作成されます。

### <a name="method-adddynalink"></a>メソッド addDynalink

    public QueryBuildDynalink addDynalink(FieldId field, Common dynamicFile, FieldId dynamicField, [int fieldArrayIndex], [int dynamicFieldArrayIndex])

#### <a name="parameters"></a>パラメーター

フィールド  

<!-- -->

dynamicFile  

<!-- -->

dynamicField  

<!-- -->

fieldArrayIndex  

<!-- -->

dynamicFieldArrayIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-addforeignkeyrelation"></a>メソッド addForeignkeyRelation

    public QueryBuildLink addForeignkeyRelation(str relatedTableRole, [str parentDatasourceName])

#### <a name="parameters"></a>パラメーター

relatedTableRole  

<!-- -->

parentDatasourceName  

#### <a name="return-value"></a>戻り値

### <a name="method-addgroupbyfield"></a>メソッド addGroupByField

    public QueryGroupByField addGroupByField(FieldId fieldID, [int arrayIndex])

#### <a name="parameters"></a>パラメーター

fieldID  

<!-- -->

arrayIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-addlink"></a>メソッド addLink

    public QueryBuildLink addLink(FieldId parentField, FieldId thisField, [str parentDatasourceName])

#### <a name="parameters"></a>パラメーター

parentField  

<!-- -->

thisField  

<!-- -->

parentDatasourceName  

#### <a name="return-value"></a>戻り値

### <a name="method-addorderbyaggregatefield"></a>メソッド addOrderByAggregateField

    public QueryOrderByField addOrderByAggregateField(SelectionField fieldType, FieldId fieldID, [SortOrder direction], [int arrayIndex])

#### <a name="parameters"></a>パラメーター

fieldType  

<!-- -->

fieldID  

<!-- -->

direction  

<!-- -->

arrayIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-addorderbycalculationfield"></a>メソッド addOrderByCalculationField

    public QueryOrderByField addOrderByCalculationField(Microsoft.Dynamics.AX.Analytics.CalculationModel.NumericExpression calculation, [SortOrder direction])

#### <a name="parameters"></a>パラメーター

計算  

<!-- -->

direction  

#### <a name="return-value"></a>戻り値

### <a name="method-addorderbyfield"></a>メソッド addOrderByField

    public QueryOrderByField addOrderByField(FieldId fieldID, [SortOrder direction], [int arrayIndex])

#### <a name="parameters"></a>パラメーター

fieldID  

<!-- -->

direction  

<!-- -->

arrayIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-addrange"></a>メソッド addRange

データ ソースに範囲を追加します。

    public QueryBuildRange addRange(FieldId field, [int arrayIndex], [QueryRangeType rangeType])

#### <a name="parameters"></a>パラメーター

フィールド  

<!-- -->

arrayIndex  

<!-- -->

rangeType  

#### <a name="return-value"></a>戻り値

データ ソースの新しい範囲。

#### <a name="remarks"></a>備考

範囲は、データ ソースのテーブルのレコードが満たす必要がある値を定義します。 いくつかの値の範囲は、特定のデータ ソース内の同じフィールドに存在することができます。 この場合、レコードが提供される値のいずれかにが適用される場合、値はクエリに含まれます。 複数のフィールドの範囲が含まれているときは、両方の条件によって提供される制約を満たすレコードだけが含まれます。 制約は値のメソッドで指定されます。

### <a name="method-addsortfield"></a>メソッド addSortField

    public int addSortField(FieldId sortField, [SortOrder direction], [int arrayIndex])

#### <a name="parameters"></a>パラメーター

sortField  

<!-- -->

direction  

<!-- -->

arrayIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-addsortindex"></a>メソッド addSortIndex

    public int addSortIndex(IndexId index)

#### <a name="parameters"></a>パラメーター

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-allowadd"></a>メソッド allowAdd

    public int allowAdd([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-applyfilter"></a>メソッド applyFilter

    public boolean applyFilter(FilterValue filterValue)

#### <a name="parameters"></a>パラメーター

filterValue  

#### <a name="return-value"></a>戻り値

### <a name="method-autoheader"></a>メソッド autoHeader

    public boolean autoHeader(FieldId field, [boolean orderNo])

#### <a name="parameters"></a>パラメーター

フィールド  

<!-- -->

orderNo  

#### <a name="return-value"></a>戻り値

### <a name="method-autoheaderdetaillevel"></a>メソッド autoHeaderDetailLevel

    public int autoHeaderDetailLevel(FieldId field, [int orderNo])

#### <a name="parameters"></a>パラメーター

フィールド  

<!-- -->

orderNo  

#### <a name="return-value"></a>戻り値

### <a name="method-autosum"></a>メソッド autoSum

    public boolean autoSum(FieldId field, [boolean orderNo])

#### <a name="parameters"></a>パラメーター

フィールド  

<!-- -->

orderNo  

#### <a name="return-value"></a>戻り値

### <a name="method-autosumdetaillevel"></a>メソッド autoSumDetailLevel

    public int autoSumDetailLevel(FieldId field, [int orderNo])

#### <a name="parameters"></a>パラメーター

フィールド  

<!-- -->

orderNo  

#### <a name="return-value"></a>戻り値

### <a name="method-changedno"></a>メソッド changedNo

    public boolean changedNo()

#### <a name="return-value"></a>戻り値

### <a name="method-childdatasourcecount"></a>メソッド childDataSourceCount

    public int childDataSourceCount()

#### <a name="return-value"></a>戻り値

### <a name="method-childdatasourceno"></a>メソッド childDataSourceNo

    public QueryBuildDataSource childDataSourceNo(int dataSourceNo)

#### <a name="parameters"></a>パラメーター

dataSourceNo  

#### <a name="return-value"></a>戻り値

### <a name="method-company"></a>メソッド company

    public str company([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-concurrencymodel"></a>メソッド concurrencyModel

    public int concurrencyModel([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dynalink"></a>メソッド dynalink

    public QueryBuildDynalink dynalink(int dynalinkNo)

#### <a name="parameters"></a>パラメーター

dynalinkNo  

#### <a name="return-value"></a>戻り値

### <a name="method-dynalinkcount"></a>メソッド dynalinkCount

    public int dynalinkCount()

#### <a name="return-value"></a>戻り値

### <a name="method-embedded"></a>メソッド embedded

    public boolean embedded()

#### <a name="return-value"></a>戻り値

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-existsmeanorexists"></a>メソッド existsMeanOrExists

    public boolean existsMeanOrExists([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-fetchmode"></a>メソッド fetchMode

    public int fetchMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-fields"></a>メソッド fields

    public QueryBuildFieldList fields()

#### <a name="return-value"></a>戻り値

### <a name="method-file"></a>メソッド file

    public TableId file()

#### <a name="return-value"></a>戻り値

### <a name="method-findrange"></a>メソッド findRange

    public QueryBuildRange findRange(FieldId field, [int occurrence], [int arrayIndex])

#### <a name="parameters"></a>パラメーター

フィールド  

<!-- -->

occurrence  

<!-- -->

arrayIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-firstfast"></a>メソッド firstFast

他のレコードの前にクエリから最初のレコードを取得するかどうかを決定します。

    public boolean firstFast([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

最初のレコードが最初に取得される場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

firstFast プロパティは、一部のデータベース システムでレコードの取得を最適化できるため、パフォーマンスが向上します。 データベースはこのプロパティをサポートしていない場合は無視されます。

### <a name="method-firstonly"></a>メソッド firstOnly

    public boolean firstOnly([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-getmostrestrictedquerybuildrangestatus"></a>メソッド getMostRestrictedQueryBuildRangeStatus

    public int getMostRestrictedQueryBuildRangeStatus(FieldId field, [int occurrence], [int arrayIndex])

#### <a name="parameters"></a>パラメーター

フィールド  

<!-- -->

occurrence  

<!-- -->

arrayIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-getno"></a>メソッド getNo

    public Common getNo()

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

    public int id()

#### <a name="return-value"></a>戻り値

### <a name="method-indexishint"></a>メソッド indexIsHint

    public boolean indexIsHint(boolean arg)

#### <a name="parameters"></a>パラメーター

arg  

#### <a name="return-value"></a>戻り値

### <a name="method-ispartofsubqueryinbasequery"></a>メソッド isPartOfSubQueryInBaseQuery

    public boolean isPartOfSubQueryInBaseQuery()

#### <a name="return-value"></a>戻り値

### <a name="method-joined"></a>メソッド joined

    public boolean joined()

#### <a name="return-value"></a>戻り値

### <a name="method-joineddatasources"></a>メソッド joinedDataSources

    public container joinedDataSources()

#### <a name="return-value"></a>戻り値

### <a name="method-joinmode"></a>メソッド joinMode

    public int joinMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

    public str label([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ラベル文字列の現在の値。

#### <a name="remarks"></a>備考

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

### <a name="method-level"></a>メソッド level

    public int level()

#### <a name="return-value"></a>戻り値

### <a name="method-link"></a>メソッド link

    public QueryBuildLink link(int associationNo)

#### <a name="parameters"></a>パラメーター

associationNo  

#### <a name="return-value"></a>戻り値

### <a name="method-linkcount"></a>メソッド linkCount

    public int linkCount()

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-onetoonedatasources"></a>メソッド oneToOneDataSources

    public container oneToOneDataSources()

#### <a name="return-value"></a>戻り値

### <a name="method-ordermode"></a>メソッド orderMode

    public int orderMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-parentdatasource"></a>メソッド parentDataSource

    public QueryBuildDataSource parentDataSource()

#### <a name="return-value"></a>戻り値

### <a name="method-policycontext"></a>メソッド policyContext

    public str policyContext([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-range"></a>メソッド range

    public QueryBuildRange range(int rangeNo)

#### <a name="parameters"></a>パラメーター

rangeNo  

#### <a name="return-value"></a>戻り値

### <a name="method-rangecount"></a>メソッド rangeCount

    public int rangeCount()

#### <a name="return-value"></a>戻り値

### <a name="method-rangefield"></a>メソッド rangeField

    public QueryBuildRange rangeField(FieldId field, [int occurrence])

#### <a name="parameters"></a>パラメーター

フィールド  

<!-- -->

occurrence  

#### <a name="return-value"></a>戻り値

### <a name="method-relations"></a>メソッド relations

    public boolean relations([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-selectioncount"></a>メソッド selectionCount

    public int selectionCount()

#### <a name="return-value"></a>戻り値

### <a name="method-selectwithrepeatableread"></a>メソッド selectWithRepeatableRead

    public boolean selectWithRepeatableRead([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-sortdirection"></a>メソッド sortDirection

    public SortOrder sortDirection(FieldId field, [SortOrder direction])

#### <a name="parameters"></a>パラメーター

フィールド  

<!-- -->

direction  

#### <a name="return-value"></a>戻り値

### <a name="method-sortfield"></a>メソッド sortField

    public FieldId sortField(FieldId field)

#### <a name="parameters"></a>パラメーター

フィールド  

#### <a name="return-value"></a>戻り値

### <a name="method-sortfieldcount"></a>メソッド sortFieldCount

    public int sortFieldCount()

#### <a name="return-value"></a>戻り値

### <a name="method-sortindex"></a>メソッド sortIndex

    public IndexId sortIndex(int indexNo)

#### <a name="parameters"></a>パラメーター

indexNo  

#### <a name="return-value"></a>戻り値

### <a name="method-sortindexcount"></a>メソッド sortIndexCount

    public int sortIndexCount()

#### <a name="return-value"></a>戻り値

### <a name="method-staticlink"></a>メソッド staticlink

クエリのデータ ソースで静的リンク オブジェクトを返します。

    public QueryBuildStaticlink staticlink(int staticlinkNo)

#### <a name="parameters"></a>パラメーター

staticlinkNo  

#### <a name="return-value"></a>戻り値

\_staticLinkNo インデックスの静的リンク オブジェクト。

### <a name="method-staticlinkcount"></a>メソッド staticlinkCount

QueryBuildDataSource オブジェクトに対して定義されている静的リンクの数が与えられます。

    public int staticlinkCount()

#### <a name="return-value"></a>戻り値

QueryBuildDataSource オブジェクトに対して定義されている静的リンクの数。

### <a name="method-table"></a>メソッド table

オブジェクトに関連付けられているテーブル ID を取得または設定します。

    public TableId table([TableId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトに関連付けられたテーブル ID の現在の値。

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

### <a name="method-uniontype"></a>メソッド unionType

    public int unionType([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-uniqueid"></a>メソッド uniqueId

    public int uniqueId()

#### <a name="return-value"></a>戻り値

### <a name="method-update"></a>メソッド update

このデータ ソースによってフェッチされたレコードを更新できるかどうかを決定します。

    public boolean update([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

レコードを更新することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

レコードを更新するには、ttsBegin および ttsCommit メソッドを使用して別のトランザクションを開始します。

### <a name="method-clearlinks"></a>メソッド clearLinks

    public void clearLinks()

### <a name="method-cleardynalinks"></a>メソッド clearDynalinks

    public void clearDynalinks()

### <a name="method-clearrange"></a>メソッド clearRange

    public void clearRange(FieldId field, [int occurrence])

#### <a name="parameters"></a>パラメーター

フィールド  

<!-- -->

occurrence  

### <a name="method-sortclear"></a>メソッド sortClear

    public void sortClear()

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-addselectionfieldwithalias"></a>メソッド addSelectionFieldWithAlias

    public void addSelectionFieldWithAlias(str alias, FieldId field, [SelectionField fieldType])

#### <a name="parameters"></a>パラメーター

エイリアス  

<!-- -->

フィールド  

<!-- -->

fieldType  

### <a name="method-addcalculationfield"></a>メソッド addCalculationField

    public void addCalculationField(Microsoft.Dynamics.AX.Analytics.CalculationModel.NumericExpression calculation, str alias)

#### <a name="parameters"></a>パラメーター

計算  

<!-- -->

エイリアス  

### <a name="method-addforeignkeydynalink"></a>メソッド addForeignKeyDynalink

    public void addForeignKeyDynalink(Common dynamicFile, str relatedRole)

#### <a name="parameters"></a>パラメーター

dynamicFile  

<!-- -->

relatedRole  

### <a name="method-addrelation"></a>メソッド addRelation

    public void addRelation(DictRelation relation, [TableScope tableScope])

#### <a name="parameters"></a>パラメーター

関係  

<!-- -->

tableScope  

### <a name="method-clearsortindex"></a>メソッド clearSortIndex

    public void clearSortIndex()

### <a name="method-clearranges"></a>メソッド clearRanges

データ ソースに関連付けられているすべての範囲を削除します。

    public void clearRanges()

#### <a name="examples"></a>例

次の例では、範囲を追加し、データソースから範囲を削除します。

    Query Q = new Query(); 
    QueryBuildDataSource ds = q.addDataSource(TableNum(CustTable)); 
    QueryBuildRange r = ds.addRange(FieldNum(CustTable, recId)); 
    print ds.rangeCount(); 
    ds.clearRanges(); 
    print ds.rangeCount(); 
    pause;

### <a name="method-linkfields"></a>メソッド linkFields

    public void linkFields(str parentField, str thisField, [str parentDatasourceName])

#### <a name="parameters"></a>パラメーター

parentField  

<!-- -->

thisField  

<!-- -->

parentDatasourceName  

### <a name="method-addselectionfield"></a>メソッド addSelectionField

    public void addSelectionField(FieldId field, [SelectionField fieldType], [int arrayIndex])

#### <a name="parameters"></a>パラメーター

フィールド  

<!-- -->

fieldType  

<!-- -->

arrayIndex  

## <a name="class-querybuilddynalink"></a>クラス QueryBuildDynalink
    class QueryBuildDynalink extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                | 説明 |
|-------------------------------------------------------|-------------|
| public Common cursor(\[Common cursor\])               |             |
| public QueryBuildDataSource dataSource()              |             |
| public FieldId dynamicField(\[FieldId dynamicField\]) |             |
| public FieldId field(\[FieldId fieldId\])             |             |
| public int fieldArrayIndex()                          |             |
| public FieldName fieldName()                          |             |
| public void finalize()                                |             |

### <a name="method-cursor"></a>メソッド cursor

    public Common cursor([Common cursor])

#### <a name="parameters"></a>パラメーター

cursor  

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

    public QueryBuildDataSource dataSource()

#### <a name="return-value"></a>戻り値

### <a name="method-dynamicfield"></a>メソッド dynamicField

    public FieldId dynamicField([FieldId dynamicField])

#### <a name="parameters"></a>パラメーター

dynamicField  

#### <a name="return-value"></a>戻り値

### <a name="method-field"></a>メソッド field

    public FieldId field([FieldId fieldId])

#### <a name="parameters"></a>パラメーター

fieldId  

#### <a name="return-value"></a>戻り値

### <a name="method-fieldarrayindex"></a>メソッド fieldArrayIndex

    public int fieldArrayIndex()

#### <a name="return-value"></a>戻り値

### <a name="method-fieldname"></a>メソッド fieldName

    public FieldName fieldName()

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-querybuildfieldlist"></a>クラス QueryBuildFieldList
    class QueryBuildFieldList extends TreeNode

QueryBuildFieldList クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                 | 説明 |
|--------------------------------------------------------------------------------------------------------|-------------|
| public int addAllFields(TableName tableName)                                                           |             |
| public QueryBuildFieldList addField(FieldId fieldId, \[SelectionField fieldType\], \[int arrayIndex\]) |             |
| public int dynamic(\[int value\])                                                                      |             |
| public FieldId field(int index)                                                                        |             |
| public int fieldCount()                                                                                |             |
| public SelectionField fieldKind(int index)                                                             |             |
| public TableId tableSelector(int index)                                                                |             |
| public void clearFieldList()                                                                           |             |

### <a name="method-addallfields"></a>メソッド addAllFields

    public int addAllFields(TableName tableName)

#### <a name="parameters"></a>パラメーター

tableName  

#### <a name="return-value"></a>戻り値

### <a name="method-addfield"></a>メソッド addField

    public QueryBuildFieldList addField(FieldId fieldId, [SelectionField fieldType], [int arrayIndex])

#### <a name="parameters"></a>パラメーター

fieldId  

<!-- -->

fieldType  

<!-- -->

arrayIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-dynamic"></a>メソッド dynamic

    public int dynamic([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-field"></a>メソッド field

    public FieldId field(int index)

#### <a name="parameters"></a>パラメーター

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-fieldcount"></a>メソッド fieldCount

    public int fieldCount()

#### <a name="return-value"></a>戻り値

### <a name="method-fieldkind"></a>メソッド fieldKind

    public SelectionField fieldKind(int index)

#### <a name="parameters"></a>パラメーター

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-tableselector"></a>メソッド tableSelector

    public TableId tableSelector(int index)

#### <a name="parameters"></a>パラメーター

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-clearfieldlist"></a>メソッド clearFieldList

    public void clearFieldList()

## <a name="class-querybuildlink"></a>クラス QueryBuildLink
    class QueryBuildLink extends TreeNode

QueryBuildLink クラスは、X++ コードおよびメタデータの作成、読み取り、更新、および削除を可能にします。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                      | 説明 |
|-----------------------------|-------------|
| public int delete()         |             |
| public int field()          |             |
| public boolean incomplete() |             |
| public str joinRelation()   |             |
| public int relatedField()   |             |
| public int relatedTable()   |             |
| public int table()          |             |
| public void finalize()      |             |

### <a name="method-delete"></a>メソッド delete

    public int delete()

#### <a name="return-value"></a>戻り値

### <a name="method-field"></a>メソッド field

    public int field()

#### <a name="return-value"></a>戻り値

### <a name="method-incomplete"></a>メソッド incomplete

    public boolean incomplete()

#### <a name="return-value"></a>戻り値

### <a name="method-joinrelation"></a>メソッド joinRelation

    public str joinRelation()

#### <a name="return-value"></a>戻り値

### <a name="method-relatedfield"></a>メソッド relatedField

    public int relatedField()

#### <a name="return-value"></a>戻り値

### <a name="method-relatedtable"></a>メソッド relatedTable

    public int relatedTable()

#### <a name="return-value"></a>戻り値

### <a name="method-table"></a>メソッド table

    public int table()

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-querybuildrange"></a>クラス QueryBuildRange
    class QueryBuildRange extends TreeNode

QueryBuildRange クラスは、QueryBuildRange クラスが関連付けられているデータ ソースからフェッチするレコードを定義する範囲を表します。

### <a name="remarks"></a>備考

value プロパティを使用して、範囲を定義する文字列を設定できます。 このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。 特定のデータ ソースは、任意の数の範囲を持つことができます。 複数の範囲は、同じデータ ソース フィールドに対して有効です。

### <a name="examples"></a>例

次の基本的な例は、QueryBuildRange クラスを使用して特定のデータ フィールドの対象範囲を指定する方法を示しています。

    Query                   query; 
    QueryRun                queryRun; 
    QueryBuildDataSource    queryBuildDataSource; 
    QueryBuildRange         queryBuildRange; 
    CustTable               custTable; 
    query = new Query(); 
    queryBuildDataSource = query.addDataSource( 
       TableNum(CustTable)); 
    queryBuildRange = queryBuildDataSource.addRange( 
        FieldNum(CustTable,AccountNum)); 
    queryBuildRange.value("4000..5000"); 
    queryRun = new queryRun(query); 
    if (queryRun.prompt()) 
    { 
        while (queryRun.next()) 
        { 
            custTable = queryRun.get(TableNum(CustTable)); 
            print custTable.AccountNum; 
        } 
    }

### <a name="methods"></a>メソッド

| 方法                                                        | 説明                                                                                                                               |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public QueryBuildDataSource dataSource()                      | QueryBuildRange オブジェクトのインスタンスを作成するために使用されたデータソースを返します。                                                          |
| public boolean doesRangeNodeBelongToCompositeQuery()          |                                                                                                                                           |
| public boolean enabled(\[boolean value\])                     | オブジェクトを有効または無効にするかどうかを決定します。                                                                                       |
| public FieldId field(\[FieldId value\])                       | オブジェクトに関連付けられているフィールド ID を取得または設定します。                                                                                     |
| public int fieldArrayIndex()                                  |                                                                                                                                           |
| public FieldName fieldName()                                  |                                                                                                                                           |
| public str label(\[str value\])                               | コントロールのラベルを取得または設定します。                                                                                                     |
| public str name(\[str value\])                                | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public str prompt()                                           |                                                                                                                                           |
| public QueryRangeType rangeType(\[QueryRangeType rangeType\]) |                                                                                                                                           |
| public int status(\[int value\])                              | オブジェクトの状態を取得または設定します。                                                                                                     |
| public TableId table(\[TableId value\])                       | オブジェクトに関連付けられているテーブル ID を取得または設定します。                                                                             |
| public TableId tableSelector(\[TableId value\])               |                                                                                                                                           |
| public str toString()                                         | 現在のオブジェクトを表す文字列を返します。                                                                                      |
| public int typeof()                                           |                                                                                                                                           |
| public boolean valid()                                        |                                                                                                                                           |
| public str value(\[str value\])                               | 取得するために一致する必要がある照会されたレコードの値を取得または設定します。                                                                   |
| public void associateRangeNodeToCompositeQuery()              |                                                                                                                                           |
| public void finalize()                                        |                                                                                                                                           |

### <a name="method-datasource"></a>メソッド dataSource

QueryBuildRange オブジェクトのインスタンスを作成するために使用されたデータソースを返します。

    public QueryBuildDataSource dataSource()

#### <a name="return-value"></a>戻り値

QueryBuildRange クラスオブジェクトのインスタンスを作成するために使用されたデータソース。

### <a name="method-doesrangenodebelongtocompositequery"></a>メソッド doesRangeNodeBelongToCompositeQuery

    public boolean doesRangeNodeBelongToCompositeQuery()

#### <a name="return-value"></a>戻り値

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-field"></a>メソッド field

オブジェクトに関連付けられているフィールド ID を取得または設定します。

    public FieldId field([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトに関連付けられたフィールド ID の現在の値。

### <a name="method-fieldarrayindex"></a>メソッド fieldArrayIndex

    public int fieldArrayIndex()

#### <a name="return-value"></a>戻り値

### <a name="method-fieldname"></a>メソッド fieldName

    public FieldName fieldName()

#### <a name="return-value"></a>戻り値

### <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

    public str label([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ラベル文字列の現在の値。

#### <a name="remarks"></a>備考

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-prompt"></a>メソッド prompt

    public str prompt()

#### <a name="return-value"></a>戻り値

### <a name="method-rangetype"></a>メソッド rangeType

    public QueryRangeType rangeType([QueryRangeType rangeType])

#### <a name="parameters"></a>パラメーター

rangeType  

#### <a name="return-value"></a>戻り値

### <a name="method-status"></a>メソッド status

オブジェクトの状態を取得または設定します。

    public int status([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトの現在の状態

#### <a name="remarks"></a>備考

ステータスには次の値があります。

-   0 - ステータス オープン。
-   1 - ステータス ロック。
-   2 - ステータスが非表示です。

### <a name="method-table"></a>メソッド table

オブジェクトに関連付けられているテーブル ID を取得または設定します。

    public TableId table([TableId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトに関連付けられたテーブル ID の現在の値。

### <a name="method-tableselector"></a>メソッド tableSelector

    public TableId tableSelector([TableId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

### <a name="method-typeof"></a>メソッド typeof

    public int typeof()

#### <a name="return-value"></a>戻り値

### <a name="method-valid"></a>メソッド valid

    public boolean valid()

#### <a name="return-value"></a>戻り値

### <a name="method-value"></a>メソッド value

取得するために一致する必要がある照会されたレコードの値を取得または設定します。

    public str value([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

範囲の文字列値

### <a name="method-associaterangenodetocompositequery"></a>メソッド associateRangeNodeToCompositeQuery

    public void associateRangeNodeToCompositeQuery()

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-querybuildstaticlink"></a>クラス QueryBuildStaticlink
    class QueryBuildStaticlink extends Object

QueryBuildStaticLink クラスは、QueryBuildDataSource クラスで定義されている静的リンクに関する情報を提供します。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                 | 説明                                                         |
|------------------------|---------------------------------------------------------------------|
| public FieldId field() | 静的リンクが定義されているフィールド情報を提供します/ |
| public AnyType value() | 静的リンクが定義されているフィールドの値を取得します。    |
| public void finalize() |                                                                     |

### <a name="method-field"></a>メソッド field

静的リンクが定義されているフィールド情報を提供します/

    public FieldId field()

#### <a name="return-value"></a>戻り値

静的リンクが定義されているフィールドの FieldId 値。

### <a name="method-value"></a>メソッド value

静的リンクが定義されているフィールドの値を取得します。

    public AnyType value()

#### <a name="return-value"></a>戻り値

静的リンクの値。

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-queryfilter"></a>クラス QueryFilter
    class QueryFilter extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                        | 説明                                          |
|---------------------------------------------------------------|------------------------------------------------------|
| public QueryBuildDataSource dataSource()                      |                                                      |
| public FieldName field()                                      |                                                      |
| public QueryRangeType rangeType(\[QueryRangeType rangeType\]) |                                                      |
| public int status(\[int status\])                             |                                                      |
| public str toString()                                         | 現在のオブジェクトを表す文字列を返します。 |
| public str value(\[str value\])                               |                                                      |
| public void finalize()                                        |                                                      |

### <a name="method-datasource"></a>メソッド dataSource

    public QueryBuildDataSource dataSource()

#### <a name="return-value"></a>戻り値

### <a name="method-field"></a>メソッド field

    public FieldName field()

#### <a name="return-value"></a>戻り値

### <a name="method-rangetype"></a>メソッド rangeType

    public QueryRangeType rangeType([QueryRangeType rangeType])

#### <a name="parameters"></a>パラメーター

rangeType  

#### <a name="return-value"></a>戻り値

### <a name="method-status"></a>メソッド status

    public int status([int status])

#### <a name="parameters"></a>パラメーター

ステータス  

#### <a name="return-value"></a>戻り値

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

### <a name="method-value"></a>メソッド value

    public str value([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-querygroupbyfield"></a>クラス QueryGroupByField
    class QueryGroupByField extends TreeNode

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                  | 説明 |
|---------------------------------------------------------|-------------|
| public boolean autoHeader(\[boolean value\])            |             |
| public int autoHeaderDetailLevel(\[int value\])         |             |
| public boolean autoSum(\[boolean value\])               |             |
| public int autoSumDetailLevel(\[int value\])            |             |
| public QueryBuildDataSource dataSource()                |             |
| public int fieldID()                                    |             |
| public TableId tableSelector(\[TableId tableSelector\]) |             |
| public void finalize()                                  |             |

### <a name="method-autoheader"></a>メソッド autoHeader

    public boolean autoHeader([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autoheaderdetaillevel"></a>メソッド autoHeaderDetailLevel

    public int autoHeaderDetailLevel([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autosum"></a>メソッド autoSum

    public boolean autoSum([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autosumdetaillevel"></a>メソッド autoSumDetailLevel

    public int autoSumDetailLevel([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

    public QueryBuildDataSource dataSource()

#### <a name="return-value"></a>戻り値

### <a name="method-fieldid"></a>メソッド fieldID

    public int fieldID()

#### <a name="return-value"></a>戻り値

### <a name="method-tableselector"></a>メソッド tableSelector

    public TableId tableSelector([TableId tableSelector])

#### <a name="parameters"></a>パラメーター

tableSelector  

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-queryhavingfilter"></a>クラス QueryHavingFilter
    class QueryHavingFilter extends TreeNode

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                          | 説明                                                                                                                               |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public AggregateFunction aggregateFunction()    |                                                                                                                                           |
| public QueryBuildDataSource dataSource()        |                                                                                                                                           |
| public boolean enabled(\[boolean value\])       | オブジェクトを有効または無効にするかどうかを決定します。                                                                                       |
| public FieldId field(\[FieldId value\])         | オブジェクトに関連付けられているフィールド ID を取得または設定します。                                                                                     |
| public int fieldArrayIndex()                    |                                                                                                                                           |
| public FieldName fieldName()                    |                                                                                                                                           |
| public str label(\[str value\])                 | コントロールのラベルを取得または設定します。                                                                                                     |
| public str name(\[str value\])                  | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public str prompt()                             |                                                                                                                                           |
| public int status(\[int value\])                | オブジェクトの状態を取得または設定します。                                                                                                     |
| public TableId table(\[TableId value\])         | オブジェクトに関連付けられているテーブル ID を取得または設定します。                                                                             |
| public TableId tableSelector(\[TableId value\]) |                                                                                                                                           |
| public str toString()                           | 現在のオブジェクトを表す文字列を返します。                                                                                      |
| public int typeof()                             |                                                                                                                                           |
| public boolean valid()                          |                                                                                                                                           |
| public str value(\[str value\])                 |                                                                                                                                           |
| public void finalize()                          |                                                                                                                                           |

### <a name="method-aggregatefunction"></a>メソッド aggregateFunction

    public AggregateFunction aggregateFunction()

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

    public QueryBuildDataSource dataSource()

#### <a name="return-value"></a>戻り値

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-field"></a>メソッド field

オブジェクトに関連付けられているフィールド ID を取得または設定します。

    public FieldId field([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトに関連付けられたフィールド ID の現在の値。

### <a name="method-fieldarrayindex"></a>メソッド fieldArrayIndex

    public int fieldArrayIndex()

#### <a name="return-value"></a>戻り値

### <a name="method-fieldname"></a>メソッド fieldName

    public FieldName fieldName()

#### <a name="return-value"></a>戻り値

### <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

    public str label([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ラベル文字列の現在の値。

#### <a name="remarks"></a>備考

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-prompt"></a>メソッド prompt

    public str prompt()

#### <a name="return-value"></a>戻り値

### <a name="method-status"></a>メソッド status

オブジェクトの状態を取得または設定します。

    public int status([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトのステータスの現在の値。

### <a name="method-table"></a>メソッド table

オブジェクトに関連付けられているテーブル ID を取得または設定します。

    public TableId table([TableId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトに関連付けられたテーブル ID の現在の値。

### <a name="method-tableselector"></a>メソッド tableSelector

    public TableId tableSelector([TableId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

### <a name="method-typeof"></a>メソッド typeof

    public int typeof()

#### <a name="return-value"></a>戻り値

### <a name="method-valid"></a>メソッド valid

    public boolean valid()

#### <a name="return-value"></a>戻り値

### <a name="method-value"></a>メソッド value

    public str value([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-queryorderbyfield"></a>クラス QueryOrderByField
    class QueryOrderByField extends TreeNode

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                  | 説明 |
|---------------------------------------------------------|-------------|
| public boolean autoHeader(\[boolean value\])            |             |
| public int autoHeaderDetailLevel(\[int value\])         |             |
| public boolean autoSum(\[boolean value\])               |             |
| public int autoSumDetailLevel(\[int value\])            |             |
| public QueryBuildDataSource dataSource()                |             |
| public SortOrder direction()                            |             |
| public int fieldID()                                    |             |
| public TableId tableSelector(\[TableId tableSelector\]) |             |
| public void finalize()                                  |             |

### <a name="method-autoheader"></a>メソッド autoHeader

    public boolean autoHeader([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autoheaderdetaillevel"></a>メソッド autoHeaderDetailLevel

    public int autoHeaderDetailLevel([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autosum"></a>メソッド autoSum

    public boolean autoSum([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autosumdetaillevel"></a>メソッド autoSumDetailLevel

    public int autoSumDetailLevel([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

    public QueryBuildDataSource dataSource()

#### <a name="return-value"></a>戻り値

### <a name="method-direction"></a>メソッド direction

    public SortOrder direction()

#### <a name="return-value"></a>戻り値

### <a name="method-fieldid"></a>メソッド fieldID

    public int fieldID()

#### <a name="return-value"></a>戻り値

### <a name="method-tableselector"></a>メソッド tableSelector

    public TableId tableSelector([TableId tableSelector])

#### <a name="parameters"></a>パラメーター

tableSelector  

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-queryrun"></a>クラス QueryRun
    class QueryRun extends ObjectRun

QueryRun クラスは、データベース内のテーブルをスキャンし、ユーザーによって与えられている制約を満たすレコードをフェッチして、ユーザー入力からこのような制約を収集するのに役立ちます。

### <a name="remarks"></a>備考

QueryRun オブジェクトは、データベース内のテーブルをスキャンし、ユーザーが指定した制約を満たすレコードをフェッチするために使用されます。 QueryRun オブジェクトは、ユーザーがそのような制限を入力できるように、ユーザーと通信することができます。 クエリは、レポートに表示するデータを記述してフェッチするためにレポートにより内部的に使用されます。 QueryRun オブジェクトは、クエリ オブジェクト を使用してクエリの構造を定義します (たとえば、どのテーブルを検索するか、レコードをどのように並び替えるかなど)。 QueryRun オブジェクトは、クエリの動的動作を定義しますが、クエリ オブジェクトはクエリの静的特性を定義します。

### <a name="examples"></a>例

次の例では、Finance and Operations のアプリケーション オブジェクト ツリー (AOT) での顧客という名前のクエリがあり、そこに 1 つのデータ ソース CustTable テーブルがあると見なされます。

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

### <a name="methods"></a>メソッド

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
| public str name(\[str value\])                                                                                 | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
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

### <a name="method-allowcheck"></a>メソッド allowCheck

    public boolean allowCheck([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-allowcrosscompany"></a>メソッド allowCrossCompany

    public boolean allowCrossCompany([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-canpage"></a>メソッド canPage

    public boolean canPage([boolean skipOrderByCheck], [boolean throwIfNotPagable], [boolean isValuePaging])

#### <a name="parameters"></a>パラメーター

skipOrderByCheck  

<!-- -->

throwIfNotPagable  

<!-- -->

isValuePaging  

#### <a name="return-value"></a>戻り値

### <a name="method-changed"></a>メソッド changed

QueryRun.next メソッドの最後の呼び出し以降に、指定されたデータ ソースが新しい値をフェッチしたかどうかを判断します。

    public boolean changed(TableId table, [int occurrence])

#### <a name="parameters"></a>パラメーター

テーブル  
確認するデータソース (オプション)。 1 つ以上のデータ ソースが指定されたテーブルに割り当てられている場合、この引数が確認するデータ ソースを決定するために使用できます。

<!-- -->

occurrence  
確認するデータソース (オプション)。 1 つ以上のデータ ソースが指定されたテーブルに割り当てられている場合、この引数が確認するデータ ソースを決定するために使用できます。

#### <a name="return-value"></a>戻り値

QueryRun.next に対する最後の呼び出し後に指定データ ソースが変更された場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

このメソッドは、データ ソースが階層構造になっている場合に便利です。 埋め込みデータ ソースは、何回でも変更できます (顧客トランザクションなど)。 これは、埋め込まれていないデータソース (顧客テーブルなど) が新しいレコード (別の顧客) をフェッチするたびに発生します。 この関数の代わりに changedNo メソッドを使用できます。

### <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

    public str changedBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

    public Date changedDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された日付。

### <a name="method-changedno"></a>メソッド changedNo

    public boolean changedNo(int dataSourceNo)

#### <a name="parameters"></a>パラメーター

dataSourceNo  

#### <a name="return-value"></a>戻り値

### <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

    public str changedTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された時間。

### <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

    public str createdBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

    public Date creationDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが作成された日付。

### <a name="method-creationtime"></a>メソッド creationTime

    public str creationTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-description"></a>メソッドの説明

    public str description([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-equal"></a>メソッド equal

指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。

    public boolean equal(Object obj)

#### <a name="parameters"></a>パラメーター

obj  

#### <a name="return-value"></a>戻り値

指定したオブジェクトが現在のオブジェクトと等しい場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

Object::equal メソッドの既定の実装では、照会の等価性のみをサポートします。 ただし、派生クラスは、値の等価性をサポートするために Object::equal メソッドをオーバーライドできます。

### <a name="method-form"></a>メソッド form

    public str form([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-get"></a>メソッド get

次のメソッドの前の呼び出しによってフェッチされたレコードを取得します。

    public Common get(TableId table, [int occurrence])

#### <a name="parameters"></a>パラメーター

テーブル  
アドレス指定されるデータソース (オプション)。 指定されたテーブルを持つデータ ソースの番号。1 ベース。 同じテーブルに割り当てられたデータ ソースが 1 つ以上ある場合は、この (オプションの) パラメーターを使用して、どのパラメーターを指定するかを指定できます。 指定されたテーブルを持つデータ ソースの数を指定します。 したがって、CustTable テーブルが 2 つのデータ ソースに割り当てられ、2 番目のデータ ソースが必要な場合、この引数は 2 の値である必要があります。

<!-- -->

occurrence  
アドレス指定されるデータソース (オプション)。 指定されたテーブルを持つデータ ソースの番号。1 ベース。 同じテーブルに割り当てられたデータ ソースが 1 つ以上ある場合は、この (オプションの) パラメーターを使用して、どのパラメーターを指定するかを指定できます。 指定されたテーブルを持つデータ ソースの数を指定します。 したがって、CustTable テーブルが 2 つのデータ ソースに割り当てられ、2 番目のデータ ソースが必要な場合、この引数は 2 の値である必要があります。

#### <a name="return-value"></a>戻り値

引数で識別されるデータ ソースからフェッチされたレコードを返します。

#### <a name="remarks"></a>備考

レコードを取得するデータ ソースは、データ ソースに割り当てられたテーブルとオプションのパラメーターによって指定されます。 テーブル (およびオプションのパラメーター) を指定するのではなく、getNo メソッドを使用して、データ ソースの数を引数として取得できます。

### <a name="method-getimpexpdatacontracttype"></a>メソッド getImpExpDataContractType

    public System.Type getImpExpDataContractType()

#### <a name="return-value"></a>戻り値

### <a name="method-getno"></a>メソッド getNo

QueryRun.next メソッドの前の呼び出しによってフェッチされたレコードを取得します。

    public Common getNo(int dataSourceNo)

#### <a name="parameters"></a>パラメーター

dataSourceNo  
現在選択されているレコードを取得する元のデータ ソースの番号。

#### <a name="return-value"></a>戻り値

引数で識別されるデータ ソースのフェッチされたレコードを返します。

#### <a name="remarks"></a>備考

レコードを取り出すデータ ソースは、データ ソースの番号で指定します。 データソースは、1 から順にカウントされます。 代わりに QueryRun.get メソッドを使用できます。このメソッドは、データ ソースを定義するテーブル (およびオプション パラメーター) を使用して指定されます。

#### <a name="examples"></a>例

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

### <a name="method-importable"></a>メソッド importable

    public boolean importable()

#### <a name="return-value"></a>戻り値

### <a name="method-interactive"></a>メソッド interactive

    public boolean interactive([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-ispositionpagingenabled"></a>メソッド isPositionPagingEnabled

    public boolean isPositionPagingEnabled()

#### <a name="return-value"></a>戻り値

### <a name="method-isquerytimedout"></a>メソッド isQueryTimedout

    public boolean isQueryTimedout()

#### <a name="return-value"></a>戻り値

### <a name="method-isvaluebasedpagingenabled"></a>メソッド isValueBasedPagingEnabled

    public boolean isValueBasedPagingEnabled()

#### <a name="return-value"></a>戻り値

### <a name="method-literals"></a>メソッド literals

    public int literals([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-loadcsv"></a>メソッド loadCsv

    public Guid loadCsv(str fileName)

#### <a name="parameters"></a>パラメーター

fileName  

#### <a name="return-value"></a>戻り値

### <a name="method-loadxml"></a>メソッド loadXml

    public Guid loadXml(str fileName)

#### <a name="parameters"></a>パラメーター

fileName  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-newobject"></a>メソッド newObject

    public QueryRun newObject(AnyType source)

#### <a name="parameters"></a>パラメーター

ソース  

#### <a name="return-value"></a>戻り値

### <a name="method-next"></a>メソッド next

クエリから次のレコードを取得します。

    public boolean next()

#### <a name="return-value"></a>戻り値

次のレコードが利用可能で getNo メソッドまたは get メソッドで取得することができる場合は true。クエリ内に設定された制約を満たすレコードがそれ以上存在しない場合は false。

#### <a name="remarks"></a>備考

変更されたメソッドまたは changedNo メソッドを使用して、指定されたデータ ソースのレコードが前回の次のメソッド呼び出しから変更されたかどうかを確認できます。

#### <a name="examples"></a>例

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

### <a name="method-nextuniqueid"></a>メソッド nextUniqueId

    public int nextUniqueId([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-origin"></a>メソッド origin

    public Guid origin([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-pack"></a>メソッド pack

    public container pack([boolean doCheck])

#### <a name="parameters"></a>パラメーター

doCheck  

#### <a name="return-value"></a>戻り値

### <a name="method-prompt"></a>メソッド prompt

クエリによってフェッチするレコードを定義するためのオプションをユーザーに表示します。

    public boolean prompt()

#### <a name="return-value"></a>戻り値

ユーザーが OK をクリックして検索が続行される場合は true。ユーザーがキャンセルをクリックして検索を停止した場合は false。

#### <a name="remarks"></a>備考

ユーザーには、フェッチされたレコードによって実行される制約を定義する範囲を与えるためのフォームが提示される。 または、ユーザーは新しいフィールドを追加し、区切ったり、変更したり、並べ替えたりすることができます。 このメソッドをオーバーロードすると、事前定義されたクエリ フォームではなく、アプリケーション定義の方法でユーザーにプロンプトを表示できます。 または、この方法は、フェッチされるレコードをユーザーがコントロールできないように、オーバーロードされることがあります。 これらの結果を生成するには、継承したメソッドを呼び出さないでください。 いずれの場合でも、関数はクエリが続行する場合は true、それ以外の場合は false を返す必要があります。

#### <a name="examples"></a>例

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

### <a name="method-query"></a>メソッド query

    public Query query([Query query])

#### <a name="parameters"></a>パラメーター

クエリ  

#### <a name="return-value"></a>戻り値

### <a name="method-querytype"></a>メソッド queryType

    public int queryType([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-recordlevelsecurity"></a>メソッド recordLevelSecurity

    public boolean recordLevelSecurity([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-report"></a>メソッド report

    public ReportRun report()

#### <a name="return-value"></a>戻り値

### <a name="method-reportrun"></a>メソッド reportRun

    public ReportRun reportRun()

#### <a name="return-value"></a>戻り値

### <a name="method-saved"></a>メソッド saved

    public boolean saved()

#### <a name="return-value"></a>戻り値

### <a name="method-saveusersetup"></a>メソッド saveUserSetup

ユーザー設定を保存します。

    public boolean saveUserSetup([boolean saveIt])

#### <a name="parameters"></a>パラメーター

saveIt  

#### <a name="return-value"></a>戻り値

設定が正常に保存された場合は true。それ以外の場合は false。

### <a name="method-searchable"></a>メソッド searchable

    public boolean searchable([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-setcursor"></a>メソッド setCursor

    public boolean setCursor(Common record, [int occurrence])

#### <a name="parameters"></a>パラメーター

記録  

<!-- -->

occurrence  

#### <a name="return-value"></a>戻り値

### <a name="method-setrecord"></a>メソッド setRecord

    public boolean setRecord(Common record, [int occurrence])

#### <a name="parameters"></a>パラメーター

記録  

<!-- -->

occurrence  

#### <a name="return-value"></a>戻り値

### <a name="method-title"></a>メソッド title

    public str title([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

### <a name="method-userupdate"></a>メソッド userUpdate

    public boolean userUpdate([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-version"></a>メソッド version

    public int version([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-getqueryrowcount"></a>メソッド getQueryRowCount

    public static int getQueryRowCount(Query query, int maxRows)

#### <a name="parameters"></a>パラメーター

クエリ  

<!-- -->

maxRows  

#### <a name="return-value"></a>戻り値

### <a name="method-runandpopulate"></a>メソッド runAndPopulate

    public static int runAndPopulate(Query sourceRuery, Common targetTable, Map queryAliasesAndTargetColumnsMap)

#### <a name="parameters"></a>パラメーター

sourceRuery  

<!-- -->

targetTable  

<!-- -->

queryAliasesAndTargetColumnsMap  

#### <a name="return-value"></a>戻り値

### <a name="method-run"></a>メソッド run

ユーザーからクエリに関する情報を取得するために使用されるフォームを開いて、一致するレコードをフェッチします。

    public void run()

#### <a name="remarks"></a>備考

クエリを実行すると、ユーザーによって入力された制約を満たすレコードが検索されます。 ただし、この方法でのクエリの実行には副作用がありません。 扱いやすくするために、1 つ以上の継承されたメソッドをオーバーロードする必要があります。

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(AnyType source)

#### <a name="parameters"></a>パラメーター

ソース  

#### <a name="remarks"></a>備考

クエリ クラスのインスタンスを QueryRun クラスのコンストラクターに渡すと、クエリ オブジェクトのコピーが作成されます。 このクエリ オブジェクト のコピーに加えられた変更は、元のクエリ オブジェクトには影響しません。

### <a name="method-addpagerange"></a>メソッド addPageRange

    public void addPageRange([Int64 startingPosition], [Int64 numberOfRecordsToFetch])

#### <a name="parameters"></a>パラメーター

startingPosition  

<!-- -->

numberOfRecordsToFetch  

### <a name="method-reset"></a>メソッド reset

    public void reset()

### <a name="method-setimportsession"></a>メソッド setImportSession

    public void setImportSession(Guid importSession)

#### <a name="parameters"></a>パラメーター

importSession  

### <a name="method-setquerytimeout"></a>メソッド setQuerytimeout

    public void setQuerytimeout(int seconds, [boolean raiseException])

#### <a name="parameters"></a>パラメーター

 秒  

<!-- -->

raiseException  

### <a name="method-init"></a>メソッド init

    public void init()

### <a name="method-enablepositionpaging"></a>メソッド enablePositionPaging

    public void enablePositionPaging([boolean enabled])

#### <a name="parameters"></a>パラメーター

有効  

### <a name="method-shred"></a>メソッド shred

    public void shred(Guid importSession)

#### <a name="parameters"></a>パラメーター

importSession  

### <a name="method-enablevaluebasedpaging"></a>メソッド enableValueBasedPaging

    public void enableValueBasedPaging([boolean enable])

#### <a name="parameters"></a>パラメーター

enable  

### <a name="method-bulknext"></a>メソッド bulkNext

    public void bulkNext([boolean fetchAllData])

#### <a name="parameters"></a>パラメーター

fetchAllData  

### <a name="method-applyvaluebasedpaging"></a>メソッド applyValueBasedPaging

    public void applyValueBasedPaging([Common sourceCursor], [boolean isForward])

#### <a name="parameters"></a>パラメーター

sourceCursor  

<!-- -->

isForward  





