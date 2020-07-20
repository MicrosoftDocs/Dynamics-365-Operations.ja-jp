---
title: QueryBuildDataSource クラス
description: このトピックでは、QueryBuildDataSource クラスについて説明します。
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
ms.openlocfilehash: 95f9d1cfdd34a20ed595ad6009ef8491d753a05b
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502869"
---
# <a name="class-querybuilddatasource"></a>クラス QueryBuildDataSource

[!include [banner](../../includes/banner.md)]

```xpp
class QueryBuildDataSource extends TreeNode
```

QueryBuildDataSource クラスは、クエリが構成されているレポート パーツを提供します。

## <a name="remarks"></a>備考

データ ソースは、データ ソースに割り当てられたテーブルからレコードがフェッチされる順序を定義する階層内で配置されます。 各データ ソースでは、レコードがフェッチされる順序および選択されたレコードによって満たされなければならない基準を定義します。 このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

```xpp
{    QueryBuildDataSource ds;    Query q = new Query();        ds = q.addDataSource(        TableNum(CustTable));}
```

## <a name="methods"></a>メソッド

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
| public str name(\[str value\])                                                                                                                               | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
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

## <a name="method-addallfields"></a>メソッド addAllFields

```xpp
public int addAllFields(TableName tableName)
```

### <a name="parameters---addallfields"></a>パラメーター - addAllFields

tableName  

### <a name="return-value---addallfields"></a>戻り値 - addAllFields

## <a name="method-adddatasource"></a>メソッド addDataSource

このデータ ソースに埋め込まれているデータ ソースを追加します。

```xpp
public QueryBuildDataSource addDataSource(AnyType arg, [str name], [boolean emptyFieldList])
```

### <a name="parameters---adddatasource"></a>パラメーター - addDataSource

arg  

<!-- -->

名前  

<!-- -->

emptyFieldList  

### <a name="return-value---adddatasource"></a>戻り値 - addDataSource

新しいデータ ソースを選択します。

### <a name="remarks---adddatasource"></a>備考 - addDataSource

最上位レベルのデータ ソースは、addDataSource メソッドを使用して作成されます。

## <a name="method-adddynalink"></a>メソッド addDynalink

```xpp
public QueryBuildDynalink addDynalink(FieldId field, Common dynamicFile, FieldId dynamicField, [int fieldArrayIndex], [int dynamicFieldArrayIndex])
```

### <a name="parameters---adddynalink"></a>パラメーター - addDynalink

 フィールド  

<!-- -->

dynamicFile  

<!-- -->

dynamicField  

<!-- -->

fieldArrayIndex  

<!-- -->

dynamicFieldArrayIndex  

### <a name="return-value---adddynalink"></a>戻り値 - addDynalink

## <a name="method-addforeignkeyrelation"></a>メソッド addForeignkeyRelation

```xpp
public QueryBuildLink addForeignkeyRelation(str relatedTableRole, [str parentDatasourceName])
```

### <a name="parameters---addforeignkeyrelation"></a>パラメーター - addForeignkeyRelation

relatedTableRole  

<!-- -->

parentDatasourceName  

### <a name="return-value---addforeignkeyrelation"></a>戻り値 - addForeignkeyRelation

## <a name="method-addgroupbyfield"></a>メソッド addGroupByField

```xpp
public QueryGroupByField addGroupByField(FieldId fieldID, [int arrayIndex])
```

### <a name="parameters---addgroupbyfield"></a>パラメーター - addGroupByField

fieldID  

<!-- -->

arrayIndex  

### <a name="return-value---addgroupbyfield"></a>戻り値 - addGroupByField

## <a name="method-addlink"></a>メソッド addLink

```xpp
public QueryBuildLink addLink(FieldId parentField, FieldId thisField, [str parentDatasourceName])
```

### <a name="parameters---addlink"></a>パラメーター - addLink

parentField  

<!-- -->

thisField  

<!-- -->

parentDatasourceName  

### <a name="return-value---addlink"></a>戻り値 - addLink

## <a name="method-addorderbyaggregatefield"></a>メソッド addOrderByAggregateField

```xpp
public QueryOrderByField addOrderByAggregateField(SelectionField fieldType, FieldId fieldID, [SortOrder direction], [int arrayIndex])
```

### <a name="parameters---addorderbyaggregatefield"></a>パラメーター - addOrderByAggregateField

fieldType  

<!-- -->

fieldID  

<!-- -->

direction  

<!-- -->

arrayIndex  

### <a name="return-value---addorderbyaggregatefield"></a>戻り値 - addOrderByAggregateField

## <a name="method-addorderbycalculationfield"></a>メソッド addOrderByCalculationField

```xpp
public QueryOrderByField addOrderByCalculationField(Microsoft.Dynamics.AX.Analytics.CalculationModel.NumericExpression calculation, [SortOrder direction])
```

### <a name="parameters---addorderbycalculationfield"></a>パラメーター - addOrderByCalculationField

計算  

<!-- -->

direction  

### <a name="return-value---addorderbycalculationfield"></a>戻り値 - addOrderByCalculationField

## <a name="method-addorderbyfield"></a>メソッド addOrderByField

```xpp
public QueryOrderByField addOrderByField(FieldId fieldID, [SortOrder direction], [int arrayIndex])
```

### <a name="parameters---addorderbyfield"></a>パラメーター - addOrderByField

fieldID  

<!-- -->

direction  

<!-- -->

arrayIndex  

### <a name="return-value---addorderbyfield"></a>戻り値 - addOrderByField

## <a name="method-addrange"></a>メソッド addRange

データ ソースに範囲を追加します。

```xpp
public QueryBuildRange addRange(FieldId field, [int arrayIndex], [QueryRangeType rangeType])
```

### <a name="parameters---addrange"></a>パラメーター - addRange

 フィールド  

<!-- -->

arrayIndex  

<!-- -->

rangeType  

### <a name="return-value---addrange"></a>戻り値 - addRange

データ ソースの新しい範囲。

### <a name="remarks---addrange"></a>備考 - addRange

範囲は、データ ソースのテーブルのレコードが満たす必要がある値を定義します。 いくつかの値の範囲は、特定のデータ ソース内の同じフィールドに存在することができます。 この場合、レコードが提供される値のいずれかにが適用される場合、値はクエリに含まれます。 複数のフィールドの範囲が含まれているときは、両方の条件によって提供される制約を満たすレコードだけが含まれます。 制約は値のメソッドで指定されます。

## <a name="method-addsortfield"></a>メソッド addSortField

```xpp
public int addSortField(FieldId sortField, [SortOrder direction], [int arrayIndex])
```

### <a name="parameters---addsortfield"></a>パラメーター - addSortField

sortField  

<!-- -->

direction  

<!-- -->

arrayIndex  

### <a name="return-value---addsortfield"></a>戻り値 - addSortField

## <a name="method-addsortindex"></a>メソッド addSortIndex

```xpp
public int addSortIndex(IndexId index)
```

### <a name="parameters---addsortindex"></a>パラメーター - addSortIndex

指数  

### <a name="return-value---addsortindex"></a>戻り値 - addSortIndex

## <a name="method-allowadd"></a>メソッド allowAdd

```xpp
public int allowAdd([int value])
```

### <a name="parameters---allowadd"></a>パラメーター - allowAdd

値  

### <a name="return-value---allowadd"></a>戻り値 - allowAdd

## <a name="method-applyfilter"></a>メソッド applyFilter

```xpp
public boolean applyFilter(FilterValue filterValue)
```

### <a name="parameters---applyfilter"></a>パラメーター - applyFilter

filterValue  

### <a name="return-value---applyfilter"></a>戻り値 - applyFilter

## <a name="method-autoheader"></a>メソッド autoHeader

```xpp
public boolean autoHeader(FieldId field, [boolean orderNo])
```

### <a name="parameters---autoheader"></a>パラメーター - autoHeader

 フィールド  

<!-- -->

orderNo  

### <a name="return-value---autoheader"></a>戻り値 - autoHeader

## <a name="method-autoheaderdetaillevel"></a>メソッド autoHeaderDetailLevel

```xpp
public int autoHeaderDetailLevel(FieldId field, [int orderNo])
```

### <a name="parameters---autoheaderdetaillevel"></a>パラメーター - autoHeaderDetailLevel

 フィールド  

<!-- -->

orderNo  

### <a name="return-value---autoheaderdetaillevel"></a>戻り値 - autoHeaderDetailLevel

## <a name="method-autosum"></a>メソッド autoSum

```xpp
public boolean autoSum(FieldId field, [boolean orderNo])
```

### <a name="parameters---autosum"></a>パラメーター - autoSum

 フィールド  

<!-- -->

orderNo  

### <a name="return-value---autosum"></a>戻り値 - autoSum

## <a name="method-autosumdetaillevel"></a>メソッド autoSumDetailLevel

```xpp
public int autoSumDetailLevel(FieldId field, [int orderNo])
```

### <a name="parameters---autosumdetaillevel"></a>パラメーター - autoSumDetailLevel

 フィールド  

<!-- -->

orderNo  

### <a name="return-value---autosumdetaillevel"></a>戻り値 - autoSumDetailLevel

## <a name="method-changedno"></a>メソッド changedNo

```xpp
public boolean changedNo()
```

### <a name="return-value---changedno"></a>戻り値 - changedNo

## <a name="method-childdatasourcecount"></a>メソッド childDataSourceCount

```xpp
public int childDataSourceCount()
```

### <a name="return-value---childdatasourcecount"></a>戻り値 - childDataSourceCount

## <a name="method-childdatasourceno"></a>メソッド childDataSourceNo

```xpp
public QueryBuildDataSource childDataSourceNo(int dataSourceNo)
```

### <a name="parameters---childdatasourceno"></a>パラメーター - childDataSourceNo

dataSourceNo  

### <a name="return-value---childdatasourceno"></a>戻り値 - childDataSourceNo

## <a name="method-company"></a>メソッド company

```xpp
public str company([str value])
```

### <a name="parameters---company"></a>パラメーター - company

値  

### <a name="return-value---company"></a>戻り値 - company

## <a name="method-concurrencymodel"></a>メソッド concurrencyModel

```xpp
public int concurrencyModel([int value])
```

### <a name="parameters---concurrencymodel"></a>パラメーター - concurrencyModel

値  

### <a name="return-value---concurrencymodel"></a>戻り値 - concurrencyModel

## <a name="method-dynalink"></a>メソッド dynalink

```xpp
public QueryBuildDynalink dynalink(int dynalinkNo)
```

### <a name="parameters---dynalink"></a>パラメーター - dynalink

dynalinkNo  

### <a name="return-value---dynalink"></a>戻り値 - dynalink

## <a name="method-dynalinkcount"></a>メソッド dynalinkCount

```xpp
public int dynalinkCount()
```

### <a name="return-value---dynalinkcount"></a>戻り値 - dynalinkCount

## <a name="method-embedded"></a>メソッド embedded

```xpp
public boolean embedded()
```

### <a name="return-value---embedded"></a>戻り値 - embedded

## <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a>パラメーター - enabled

値  

### <a name="return-value---enabled"></a>戻り値 - enabled

オブジェクトが有効である場合は true。それ以外の場合は、false。

### <a name="remarks---enabled"></a>備考 - enabled

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

## <a name="method-existsmeanorexists"></a>メソッド existsMeanOrExists

```xpp
public boolean existsMeanOrExists([boolean value])
```

### <a name="parameters---existsmeanorexists"></a>パラメーター - existsMeanOrExists

値  

### <a name="return-value---existsmeanorexists"></a>戻り値 - existsMeanOrExists

## <a name="method-fetchmode"></a>メソッド fetchMode

```xpp
public int fetchMode([int value])
```

### <a name="parameters---fetchmode"></a>パラメーター - fetchMode

値  

### <a name="return-value---fetchmode"></a>戻り値 - fetchMode

## <a name="method-fields"></a>メソッド fields

```xpp
public QueryBuildFieldList fields()
```

### <a name="return-value---fields"></a>戻り値 - fields

## <a name="method-file"></a>メソッド file

```xpp
public TableId file()
```

### <a name="return-value---file"></a>戻り値 - file

## <a name="method-findrange"></a>メソッド findRange

```xpp
public QueryBuildRange findRange(FieldId field, [int occurrence], [int arrayIndex])
```

### <a name="parameters---findrange"></a>パラメーター - findRange

 フィールド  

<!-- -->

occurrence  

<!-- -->

arrayIndex  

### <a name="return-value---findrange"></a>戻り値 - findRange

## <a name="method-firstfast"></a>メソッド firstFast

他のレコードの前にクエリから最初のレコードを取得するかどうかを決定します。

```xpp
public boolean firstFast([boolean value])
```

### <a name="parameters---firstfast"></a>パラメーター - firstFast

値  

### <a name="return-value---firstfast"></a>戻り値 - firstFast

最初のレコードが最初に取得される場合は true。それ以外の場合は、false。

### <a name="remarks---firstfast"></a>備考 - firstFast

firstFast プロパティは、一部のデータベース システムでレコードの取得を最適化できるため、パフォーマンスが向上します。 データベースはこのプロパティをサポートしていない場合は無視されます。

## <a name="method-firstonly"></a>メソッド firstOnly

```xpp
public boolean firstOnly([boolean value])
```

### <a name="parameters---firstonly"></a>パラメーター - firstOnly

値  

### <a name="return-value---firstonly"></a>戻り値 - firstOnly

## <a name="method-getmostrestrictedquerybuildrangestatus"></a>メソッド getMostRestrictedQueryBuildRangeStatus

```xpp
public int getMostRestrictedQueryBuildRangeStatus(FieldId field, [int occurrence], [int arrayIndex])
```

### <a name="parameters---getmostrestrictedquerybuildrangestatus"></a>パラメーター - getMostRestrictedQueryBuildRangeStatus

 フィールド  

<!-- -->

occurrence  

<!-- -->

arrayIndex  

### <a name="return-value---getmostrestrictedquerybuildrangestatus"></a>戻り値 - getMostRestrictedQueryBuildRangeStatus

## <a name="method-getno"></a>メソッド getNo

```xpp
public Common getNo()
```

### <a name="return-value---getno"></a>戻り値 - getNo

## <a name="method-id"></a>メソッド id

```xpp
public int id()
```

### <a name="return-value---id"></a>戻り値 - id

## <a name="method-indexishint"></a>メソッド indexIsHint

```xpp
public boolean indexIsHint(boolean arg)
```

### <a name="parameters---indexishint"></a>パラメーター - indexIsHint

arg  

### <a name="return-value---indexishint"></a>戻り値 - indexIsHint

## <a name="method-ispartofsubqueryinbasequery"></a>メソッド isPartOfSubQueryInBaseQuery

```xpp
public boolean isPartOfSubQueryInBaseQuery()
```

### <a name="return-value---ispartofsubqueryinbasequery"></a>戻り値 - isPartOfSubQueryInBaseQuery

## <a name="method-joined"></a>メソッド joined

```xpp
public boolean joined()
```

### <a name="return-value---joined"></a>戻り値 - joined

## <a name="method-joineddatasources"></a>メソッド joinedDataSources

```xpp
public container joinedDataSources()
```

### <a name="return-value---joineddatasources"></a>戻り値 - joinedDataSources

## <a name="method-joinmode"></a>メソッド joinMode

```xpp
public int joinMode([int value])
```

### <a name="parameters---joinmode"></a>パラメーター - joinMode

値  

### <a name="return-value---joinmode"></a>戻り値 - joinMode

## <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

```xpp
public str label([str value])
```

### <a name="parameters---label"></a>パラメーター - label

値  

### <a name="return-value---label"></a>戻り値 - label

ラベル文字列の現在の値。

### <a name="remarks---label"></a>備考 - label

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

## <a name="method-level"></a>メソッド level

```xpp
public int level()
```

### <a name="return-value---level"></a>戻り値 - level

## <a name="method-link"></a>メソッド link

```xpp
public QueryBuildLink link(int associationNo)
```

### <a name="parameters---link"></a>パラメーター - link

associationNo  

### <a name="return-value---link"></a>戻り値 - link

## <a name="method-linkcount"></a>メソッド linkCount

```xpp
public int linkCount()
```

### <a name="return-value---linkcount"></a>戻り値 - linkCount

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

## <a name="method-onetoonedatasources"></a>メソッド oneToOneDataSources

```xpp
public container oneToOneDataSources()
```

### <a name="return-value---onetoonedatasources"></a>戻り値 - oneToOneDataSources

## <a name="method-ordermode"></a>メソッド orderMode

```xpp
public int orderMode([int value])
```

### <a name="parameters---ordermode"></a>パラメーター - orderMode

値  

### <a name="return-value---ordermode"></a>戻り値 - orderMode

## <a name="method-parentdatasource"></a>メソッド parentDataSource

```xpp
public QueryBuildDataSource parentDataSource()
```

### <a name="return-value---parentdatasource"></a>戻り値 - parentDataSource

## <a name="method-policycontext"></a>メソッド policyContext

```xpp
public str policyContext([str value])
```

### <a name="parameters---policycontext"></a>パラメーター - policyContext

値  

### <a name="return-value---policycontext"></a>戻り値 - policyContext

## <a name="method-range"></a>メソッド range

```xpp
public QueryBuildRange range(int rangeNo)
```

### <a name="parameters---range"></a>パラメーター - range

rangeNo  

### <a name="return-value---range"></a>戻り値 - range

## <a name="method-rangecount"></a>メソッド rangeCount

```xpp
public int rangeCount()
```

### <a name="return-value---rangecount"></a>戻り値 - rangeCount

## <a name="method-rangefield"></a>メソッド rangeField

```xpp
public QueryBuildRange rangeField(FieldId field, [int occurrence])
```

### <a name="parameters---rangefield"></a>パラメーター - rangeField

 フィールド  

<!-- -->

occurrence  

### <a name="return-value---rangefield"></a>戻り値 - rangeField

## <a name="method-relations"></a>メソッド relations

```xpp
public boolean relations([boolean value])
```

### <a name="parameters---relations"></a>パラメーター - relations

値  

### <a name="return-value---relations"></a>戻り値 - relations

## <a name="method-selectioncount"></a>メソッド selectionCount

```xpp
public int selectionCount()
```

### <a name="return-value---selectioncount"></a>戻り値 - selectionCount

## <a name="method-selectwithrepeatableread"></a>メソッド selectWithRepeatableRead

```xpp
public boolean selectWithRepeatableRead([boolean value])
```

### <a name="parameters---selectwithrepeatableread"></a>パラメーター - selectWithRepeatableRead

値  

### <a name="return-value---selectwithrepeatableread"></a>戻り値 - selectWithRepeatableRead

## <a name="method-sortdirection"></a>メソッド sortDirection

```xpp
public SortOrder sortDirection(FieldId field, [SortOrder direction])
```

### <a name="parameters---sortdirection"></a>パラメーター - sortDirection

 フィールド  

<!-- -->

direction  

### <a name="return-value---sortdirection"></a>戻り値 - sortDirection

## <a name="method-sortfield"></a>メソッド sortField

```xpp
public FieldId sortField(FieldId field)
```

### <a name="parameters---sortfield"></a>パラメーター - sortField

 フィールド  

### <a name="return-value---sortfield"></a>戻り値 - sortField

## <a name="method-sortfieldcount"></a>メソッド sortFieldCount

```xpp
public int sortFieldCount()
```

### <a name="return-value---sortfieldcount"></a>戻り値 - sortFieldCount

## <a name="method-sortindex"></a>メソッド sortIndex

```xpp
public IndexId sortIndex(int indexNo)
```

### <a name="parameters---sortindex"></a>パラメーター - sortIndex

indexNo  

### <a name="return-value---sortindex"></a>戻り値 - sortIndex

## <a name="method-sortindexcount"></a>メソッド sortIndexCount

```xpp
public int sortIndexCount()
```

### <a name="return-value---sortindexcount"></a>戻り値 - sortIndexCount

## <a name="method-staticlink"></a>メソッド staticlink

クエリのデータ ソースで静的リンク オブジェクトを返します。

```xpp
public QueryBuildStaticlink staticlink(int staticlinkNo)
```

### <a name="parameters---staticlink"></a>パラメーター - staticlink

staticlinkNo  

### <a name="return-value---staticlink"></a>戻り値 - staticlink

\_staticLinkNo インデックスの静的リンク オブジェクト。

## <a name="method-staticlinkcount"></a>メソッド staticlinkCount

QueryBuildDataSource オブジェクトに対して定義されている静的リンクの数が与えられます。

```xpp
public int staticlinkCount()
```

### <a name="return-value---staticlinkcount"></a>戻り値 - staticlinkCount

QueryBuildDataSource オブジェクトに対して定義されている静的リンクの数。

## <a name="method-table"></a>メソッド table

オブジェクトに関連付けられているテーブル ID を取得または設定します。

```xpp
public TableId table([TableId value])
```

### <a name="parameters---table"></a>パラメーター - table

値  

### <a name="return-value---table"></a>戻り値 - toBlob

オブジェクトに関連付けられたテーブル ID の現在の値。

## <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

現在のオブジェクトを表す文字列。

### <a name="remarks---tostring"></a>備考 - toString

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

## <a name="method-uniontype"></a>メソッド unionType

```xpp
public int unionType([int value])
```

### <a name="parameters---uniontype"></a>パラメーター - unionType

値  

### <a name="return-value---uniontype"></a>戻り値 - unionType

## <a name="method-uniqueid"></a>メソッド uniqueId

```xpp
public int uniqueId()
```

### <a name="return-value---uniqueid"></a>戻り値 - uniqueId

## <a name="method-update"></a>メソッド update

このデータ ソースによってフェッチされたレコードを更新できるかどうかを決定します。

```xpp
public boolean update([boolean value])
```

### <a name="parameters---update"></a>パラメーター - update

値  

### <a name="return-value---update"></a>戻り値 - update

レコードを更新することができる場合は true。それ以外の場合は、false。

### <a name="remarks---update"></a>備考 - update

レコードを更新するには、ttsBegin および ttsCommit メソッドを使用して別のトランザクションを開始します。

## <a name="method-clearlinks"></a>メソッド clearLinks

```xpp
public void clearLinks()
```

## <a name="method-cleardynalinks"></a>メソッド clearDynalinks

```xpp
public void clearDynalinks()
```

## <a name="method-clearrange"></a>メソッド clearRange

```xpp
public void clearRange(FieldId field, [int occurrence])
```

### <a name="parameters---clearrange"></a>パラメーター - clearRange

 フィールド  

<!-- -->

occurrence  

## <a name="method-sortclear"></a>メソッド sortClear

```xpp
public void sortClear()
```

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-addselectionfieldwithalias"></a>メソッド addSelectionFieldWithAlias

```xpp
public void addSelectionFieldWithAlias(str alias, FieldId field, [SelectionField fieldType])
```

### <a name="parameters---addselectionfieldwithalias"></a>パラメーター - addSelectionFieldWithAlias

エイリアス  

<!-- -->

 フィールド  

<!-- -->

fieldType  

## <a name="method-addcalculationfield"></a>メソッド addCalculationField

```xpp
public void addCalculationField(Microsoft.Dynamics.AX.Analytics.CalculationModel.NumericExpression calculation, str alias)
```

### <a name="parameters---addcalculationfield"></a>パラメーター - addCalculationField

計算  

<!-- -->

エイリアス  

## <a name="method-addforeignkeydynalink"></a>メソッド addForeignKeyDynalink

```xpp
public void addForeignKeyDynalink(Common dynamicFile, str relatedRole)
```

### <a name="parameters---addforeignkeydynalink"></a>パラメーター - addForeignKeyDynalink

dynamicFile  

<!-- -->

relatedRole  

## <a name="method-addrelation"></a>メソッド addRelation

```xpp
public void addRelation(DictRelation relation, [TableScope tableScope])
```

### <a name="parameters---addrelation"></a>パラメーター - addRelation

関係  

<!-- -->

tableScope  

## <a name="method-clearsortindex"></a>メソッド clearSortIndex

```xpp
public void clearSortIndex()
```

## <a name="method-clearranges"></a>メソッド clearRanges

データ ソースに関連付けられているすべての範囲を削除します。

```xpp
public void clearRanges()
```

### <a name="examples---clearranges"></a>例 - clearRanges

次の例では、範囲を追加し、データソースから範囲を削除します。

```xpp
Query Q = new Query(); 
QueryBuildDataSource ds = q.addDataSource(TableNum(CustTable)); 
QueryBuildRange r = ds.addRange(FieldNum(CustTable, recId)); 
print ds.rangeCount(); 
ds.clearRanges(); 
print ds.rangeCount(); 
pause;
```

## <a name="method-linkfields"></a>メソッド linkFields

```xpp
public void linkFields(str parentField, str thisField, [str parentDatasourceName])
```

### <a name="parameters---linkfields"></a>パラメーター - linkFields

parentField  

<!-- -->

thisField  

<!-- -->

parentDatasourceName  

## <a name="method-addselectionfield"></a>メソッド addSelectionField

```xpp
public void addSelectionField(FieldId field, [SelectionField fieldType], [int arrayIndex])
```

### <a name="parameters---addselectionfield"></a>パラメーター - addSelectionField

 フィールド  

<!-- -->

fieldType  

<!-- -->

arrayIndex  

