---
title: DictRelation クラス
description: このトピックでは、DictRelation クラスについて説明します。
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
ms.openlocfilehash: 2d79651b7998c203d088cd8da5964d2e8ef5b3f1
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502983"
---
# <a name="class-dictrelation"></a>クラス DictRelation

[!include [banner](../../includes/banner.md)]

```xpp
class DictRelation extends Object
```

DictRelation クラスは、テーブルのディクショナリ関係の管理に使用できます。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                | 説明                                                          |
|-----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| public Cardinality Cardinality()                                                                                      | 基数値を取得します。                                     |
| public boolean createNavigationPropertyMethods()                                                                      |                                                                      |
| public boolean EDTRelation()                                                                                          | 拡張データ型 (EDT) の関係の状態を取得します。               |
| public str entityRelationshipRole()                                                                                   | エンティティ リレーションシップ ロールの名前を取得します。                  |
| public str entityRelationshipRoleLabelId()                                                                            | エンティティ関係ロールの名前のラベル ID を取得します。 |
| public TableId externTable()                                                                                          | 関係のために使用する外部テーブルの ID を返します。  |
| public boolean isSelfLink()                                                                                           | リレーションが自己リンクされているかどうかを検証します。                        |
| public int lineExternTableValue(int lineNumber)                                                                       | 特定の行の外部テーブル値を取得します。               |
| public int lines()                                                                                                    | リレーションの明細行の数を取得します。                   |
| public int lineSourceEDT(int lineNumber)                                                                              | 特定のテーブル行のソース EDT 値を取得します。             |
| public RelationshipSubType lineSubType(int lineNumber)                                                                | 指定されたテーブル行のサブタイプを取得します。                     |
| public int lineTableValue(int lineNumber)                                                                             | 特定のテーブル行の値を取得します。                        |
| public TableRelation lineType(int lineNumber)                                                                         | 指定されたテーブル行のリレーション タイプを取得します。                |
| public TableId loadFieldRelation(FieldId fieldId, \[TableScope tableScope\], \[Common record\], \[boolean isLookup\]) | フィールド ID で指定されている関係を読み込みます。                    |
| public TableId loadNameRelation(str name)                                                                             | 指定された名前の関係を読み込みます。                               |
| public TableId loadTableRelation(TableId tableId, \[TableScope tableScope\], \[Common record\])                       | テーブル リレーションを読み込みます。                                              |
| public str navigationPropertyNameOverride()                                                                           |                                                                      |
| public RelatedTableCardinality RelatedTableCardinality()                                                              | 関連テーブルの基数を取得します。                     |
| public str RelatedTableRole()                                                                                         | 関連テーブルのロール名を取得します。                       |
| public RelationshipType relationshipType()                                                                            | 関係タイプを取得します。                                     |
| public str Role()                                                                                                     | ロール名を取得します。                                             |
| public TableId table()                                                                                                | リレーションのテーブル ID を返します。                                |
| public boolean useDefaultRoleNames()                                                                                  |                                                                      |
| public boolean validate()                                                                                             | リレーションを検証します。                                                |
| ::public static boolean isSurrogateForeignKeyRelation(TableId tableId, str relationName)                              | 代理外部キーのリレーションがあるかどうかを検証します。            |
| public void new(int id, \[UtilElementType Util\_Element\_Type\], \[int index\])                                       | Object クラスの新しいインスタンスを初期化します。                      |

## <a name="method-cardinality"></a>メソッド Cardinality

基数値を取得します。

```xpp
public Cardinality Cardinality()
```

### <a name="return-value---cardinality"></a>戻り値 - Cardinality

基数値。

## <a name="method-createnavigationpropertymethods"></a>メソッド createNavigationPropertyMethods

```xpp
public boolean createNavigationPropertyMethods()
```

### <a name="return-value---createnavigationpropertymethods"></a>戻り値 - createNavigationPropertyMethods

## <a name="method-edtrelation"></a>メソッド EDTRelation

拡張データ型 (EDT) の関係の状態を取得します。

```xpp
public boolean EDTRelation()
```

### <a name="return-value---edtrelation"></a>戻り値 - EDTRelation

EDT 関係が使用可能かどうかを示すブール値。

## <a name="method-entityrelationshiprole"></a>メソッド entityRelationshipRole

エンティティ リレーションシップ ロールの名前を取得します。

```xpp
public str entityRelationshipRole()
```

### <a name="return-value---entityrelationshiprole"></a>戻り値 - entityRelationshipRole

エンティティ リレーションシップ ロールの名前。

## <a name="method-entityrelationshiprolelabelid"></a>メソッド entityRelationshipRoleLabelId

エンティティ関係ロールの名前のラベル ID を取得します。

```xpp
public str entityRelationshipRoleLabelId()
```

### <a name="return-value---entityrelationshiprolelabelid"></a>戻り値 - entityRelationshipRoleLabelId

エンティティ リレーションシップ ロールのラベル ID。

## <a name="method-externtable"></a>メソッド externTable

関係のために使用する外部テーブルの ID を返します。

```xpp
public TableId externTable()
```

### <a name="return-value---externtable"></a>戻り値 - externTable

関係に使用される外部テーブルの ID。関係がまだ読み込まれていない場合は 0 (ゼロ)。

### <a name="examples---externtable"></a>例 - externTable

次の例は、外部テーブルの ID の取得を示しています。

```xpp
Dictionary dict; 
DictRelation dr; 
int i;  
dict = new Dictionary(); 
dr = new DictRelation(dict.tableName2Id("CustTable")); 
// Load a relation by name 
dr.loadNameRelation("CompanyData");  // Also returns the external table ID. 
print "The external table ID is: " + int2str(dr.externTable());
```

## <a name="method-isselflink"></a>メソッド isSelfLink

リレーションが自己リンクされているかどうかを検証します。

```xpp
public boolean isSelfLink()
```

### <a name="return-value---isselflink"></a>戻り値 - isSelfLink

リレーションが自己リンクである場合は true。それ以外の場合は、false。

## <a name="method-lineexterntablevalue"></a>メソッド lineExternTableValue

特定の行の外部テーブル値を取得します。

```xpp
public int lineExternTableValue(int lineNumber)
```

### <a name="parameters---lineexterntablevalue"></a>パラメーター - lineExternTableValue

lineNumber  

### <a name="return-value---lineexterntablevalue"></a>戻り値 - lineExternTableValue

外部テーブル値。

## <a name="method-lines"></a>メソッド lines

リレーションの明細行の数を取得します。

```xpp
public int lines()
```

### <a name="return-value---lines"></a>戻り値 - lines

ラインの数。

## <a name="method-linesourceedt"></a>メソッド lineSourceEDT

特定のテーブル行のソース EDT 値を取得します。

```xpp
public int lineSourceEDT(int lineNumber)
```

### <a name="parameters---linesourceedt"></a>パラメーター - lineSourceEDT

lineNumber  

### <a name="return-value---linesourceedt"></a>戻り値 - lineSourceEDT

ソース EDT 値。

## <a name="method-linesubtype"></a>メソッド lineSubType

指定されたテーブル行のサブタイプを取得します。

```xpp
public RelationshipSubType lineSubType(int lineNumber)
```

### <a name="parameters---linesubtype"></a>パラメーター - lineSubType

lineNumber  

### <a name="return-value---linesubtype"></a>戻り値 - lineSubType

指定されたテーブル行のサブタイプ。

## <a name="method-linetablevalue"></a>メソッド lineTableValue

特定のテーブル行の値を取得します。

```xpp
public int lineTableValue(int lineNumber)
```

### <a name="parameters---linetablevalue"></a>パラメーター - lineTableValue

lineNumber  

### <a name="return-value---linetablevalue"></a>戻り値 - lineTableValue

テーブル行の値。

## <a name="method-linetype"></a>メソッド lineType

指定されたテーブル行のリレーション タイプを取得します。

```xpp
public TableRelation lineType(int lineNumber)
```

### <a name="parameters---linetype"></a>パラメーター - lineType

lineNumber  

### <a name="return-value---linetype"></a>戻り値 - lineType

指定された行のテーブルのリレーション タイプ。

## <a name="method-loadfieldrelation"></a>メソッド loadFieldRelation

フィールド ID で指定されている関係を読み込みます。

```xpp
public TableId loadFieldRelation(FieldId fieldId, [TableScope tableScope], [Common record], [boolean isLookup])
```

### <a name="parameters---loadfieldrelation"></a>パラメーター - loadFieldRelation

fieldId  

<!-- -->

tableScope  

<!-- -->

記録  

<!-- -->

isLookup  

### <a name="return-value---loadfieldrelation"></a>戻り値 - loadFieldRelation

関係のテーブルの ID。メソッドが失敗した場合は null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。

## <a name="method-loadnamerelation"></a>メソッド loadNameRelation

指定された名前の関係を読み込みます。

```xpp
public TableId loadNameRelation(str name)
```

### <a name="parameters---loadnamerelation"></a>パラメーター - loadNameRelation

名前  

### <a name="return-value---loadnamerelation"></a>戻り値 - loadNameRelation

テーブル リレーションのテーブル ID。

## <a name="method-loadtablerelation"></a>メソッド loadTableRelation

テーブル リレーションを読み込みます。

```xpp
public TableId loadTableRelation(TableId tableId, [TableScope tableScope], [Common record])
```

### <a name="parameters---loadtablerelation"></a>パラメーター - loadTableRelation

tableId  

<!-- -->

tableScope  

<!-- -->

記録  

### <a name="return-value---loadtablerelation"></a>戻り値 - loadTableRelation

テーブル リレーションのテーブル ID。

## <a name="method-navigationpropertynameoverride"></a>メソッド navigationPropertyNameOverride

```xpp
public str navigationPropertyNameOverride()
```

### <a name="return-value---navigationpropertynameoverride"></a>戻り値 - navigationPropertyNameOverride

## <a name="method-relatedtablecardinality"></a>メソッド RelatedTableCardinality

関連テーブルの基数を取得します。

```xpp
public RelatedTableCardinality RelatedTableCardinality()
```

### <a name="return-value---relatedtablecardinality"></a>戻り値 - RelatedTableCardinality

関連テーブルの基数。

## <a name="method-relatedtablerole"></a>メソッド RelatedTableRole

関連テーブルのロール名を取得します。

```xpp
public str RelatedTableRole()
```

### <a name="return-value---relatedtablerole"></a>戻り値 - RelatedTableRole

関連テーブルのロール名。

## <a name="method-relationshiptype"></a>メソッド relationshipType

関係タイプを取得します。

```xpp
public RelationshipType relationshipType()
```

### <a name="return-value---relationshiptype"></a>戻り値 - relationshipType

リレーションシップ タイプ。

## <a name="method-role"></a>メソッド Role

ロール名を取得します。

```xpp
public str Role()
```

### <a name="return-value---role"></a>戻り値 - Role

ロール名。

## <a name="method-table"></a>メソッド table

リレーションのテーブル ID を返します。

```xpp
public TableId table()
```

### <a name="return-value---table"></a>戻り値 - toBlob

リレーションのテーブル ID

### <a name="examples---table"></a>例 - table

次の例は、リレーションのテーブル ID の取得を示しています。

```xpp
Dictionary dict; 
DictRelation dr; 
dict = new Dictionary(); 
dr = new DictRelation(dict.tableName2Id("CustTable")); 
print dr.table();
```

## <a name="method-usedefaultrolenames"></a>メソッド useDefaultRoleNames

```xpp
public boolean useDefaultRoleNames()
```

### <a name="return-value---usedefaultrolenames"></a>戻り値 - useDefaultRoleNames

## <a name="method-validate"></a>メソッド validate

リレーションを検証します。

```xpp
public boolean validate()
```

### <a name="return-value---validate"></a>戻り値 - validate

リレーションが有効である場合は true。それ以外の場合は、false。

## <a name="method-issurrogateforeignkeyrelation"></a>メソッド isSurrogateForeignKeyRelation

代理外部キーのリレーションがあるかどうかを検証します。

```xpp
public static boolean isSurrogateForeignKeyRelation(TableId tableId, str relationName)
```

### <a name="parameters---issurrogateforeignkeyrelation"></a>パラメーター - isSurrogateForeignKeyRelation

tableId  

<!-- -->

relationName  

### <a name="return-value---issurrogateforeignkeyrelation"></a>戻り値 - isSurrogateForeignKeyRelation

代理外部キー リレーションがある場合は true。それ以外の場合は、false。

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(int id, [UtilElementType Util_Element_Type], [int index])
```

### <a name="parameters---new"></a>パラメーター - new

id  
リレーション インデックス (オプション)。 既定値は 1 です。

<!-- -->

Util\_Element\_Type  
リレーション インデックス (オプション)。 既定値は 1 です。

<!-- -->

指数  
リレーション インデックス (オプション)。 既定値は 1 です。

