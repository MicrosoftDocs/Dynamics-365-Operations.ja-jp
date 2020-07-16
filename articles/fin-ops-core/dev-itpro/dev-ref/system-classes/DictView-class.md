---
title: DictView クラス
description: このトピックでは、DictView クラスについて説明します。
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
ms.openlocfilehash: 8d00c99afe8e9e29b94b463af0caebbfee57b1a6
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502674"
---
# <a name="class-dictview"></a>クラス DictView

[!include [banner](../../includes/banner.md)]

```xpp
class DictView extends DictTable
```

DictView クラスでは、特定のビューに関する情報へのアクセスを提供します。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                               | 説明                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| public str computedColumnString(str dataSourceName, str fieldName, \[FieldNameGenerationMode generationMode\], \[boolean needTrim\]) | テーブル エイリアスを取得します。                                                                                  |
| public int datasourceCnt()                                                                                                           | ビュー内のデータ ソースをカウントします。                                                                            |
| public str datasourceDataareaIdName(int cnt)                                                                                         | データ ソースの法人を識別するためにビュー定義で使用される SQL 名を取得します。 |
| public TableId datasourceID2TableId(TableId dataSourceId)                                                                            | 特定のデータ ソースのテーブル ID を取得します。                                                                 |
| public TableId datasourceTableId(int cnt)                                                                                            | インデックス化されたデータ ソースのテーブル ID を取得します。                                                          |
| public SelectionField fieldAggregation(FieldId fieldId)                                                                              | 特定のフィールドが実行する集計の種類を取得します。                                              |
| public int fieldDatasource(FieldId fieldId)                                                                                          | 特定のフィールドの発生元データ ソースの ID を取得します。                                   |
| public TableId fieldDatasourceID(FieldId fieldId)                                                                                    | 特定のフィールドがマッピングされるビューでデータ ソースの ID を取得します。                               |
| public FieldId fieldId(FieldId fieldId)                                                                                              | 元のテーブルのフィールド ID を取得します。                                                           |
| public boolean isAggregatedView()                                                                                                    | ビューが集約されているかどうかをチェックします。                                                                      |
| public Query query()                                                                                                                 |                                                                                                             |
| public boolean isDataEntity()                                                                                                        |                                                                                                             |
| public boolean isUpdatable()                                                                                                         |                                                                                                             |
| public boolean isPublic()                                                                                                            |                                                                                                             |
| public str collectionName()                                                                                                          |                                                                                                             |
| public boolean isVirtualField(str fieldName)                                                                                         |                                                                                                             |
| public FieldAccessModifier getFieldAccessModifier(str fieldName)                                                                     |                                                                                                             |
| public boolean isStaged()                                                                                                            |                                                                                                             |
| public str version()                                                                                                                 |                                                                                                             |
| public MessagingRole messagingRole()                                                                                                 |                                                                                                             |
| public void new(TableId tableId)                                                                                                     | Object クラスの新しいインスタンスを初期化します。                                                             |

## <a name="method-computedcolumnstring"></a>メソッド computedColumnString

テーブル エイリアスを取得します。

```xpp
public str computedColumnString(str dataSourceName, str fieldName, [FieldNameGenerationMode generationMode], [boolean needTrim])
```

### <a name="parameters---computedcolumnstring"></a>パラメーター - computedColumnString

dataSourceName  

<!-- -->

fieldName  

<!-- -->

generationMode  

<!-- -->

needTrim  

### <a name="return-value---computedcolumnstring"></a>戻り値 - computedColumnString

書式設定されたフィールド名文字列。

### <a name="remarks---computedcolumnstring"></a>備考 - computedColumnString

テーブルのエイリアスは、計算列定義と一緒に使用できるデータベース形式の SQL フィールド名です。

## <a name="method-datasourcecnt"></a>メソッド datasourceCnt

ビュー内のデータ ソースをカウントします。

```xpp
public int datasourceCnt()
```

### <a name="return-value---datasourcecnt"></a>戻り値 - datasourceCnt

ビュー内のデータ ソースの数。

## <a name="method-datasourcedataareaidname"></a>メソッド datasourceDataareaIdName

データ ソースの法人を識別するためにビュー定義で使用される SQL 名を取得します。

```xpp
public str datasourceDataareaIdName(int cnt)
```

### <a name="parameters---datasourcedataareaidname"></a>パラメーター - datasourceDataareaIdName

cnt  

### <a name="return-value---datasourcedataareaidname"></a>戻り値 - datasourceDataareaIdName

データ ソースの法人を識別するためにビュー定義で使用される SQL 名。エラーが発生した場合は空の文字列。

## <a name="method-datasourceid2tableid"></a>メソッド datasourceID2TableId

特定のデータ ソースのテーブル ID を取得します。

```xpp
public TableId datasourceID2TableId(TableId dataSourceId)
```

### <a name="parameters---datasourceid2tableid"></a>パラメーター - datasourceID2TableId

dataSourceId  

### <a name="return-value---datasourceid2tableid"></a>戻り値 - datasourceID2TableId

特定のデータ ソースのテーブル ID。

## <a name="method-datasourcetableid"></a>メソッド datasourceTableId

インデックス化されたデータ ソースのテーブル ID を取得します。

```xpp
public TableId datasourceTableId(int cnt)
```

### <a name="parameters---datasourcetableid"></a>パラメーター - datasourceTableId

cnt  

### <a name="return-value---datasourcetableid"></a>戻り値 - datasourceTableId

指定されたデータ ソースのテーブル ID。エラーが発生した場合は 0 (ゼロ)。

## <a name="method-fieldaggregation"></a>メソッド fieldAggregation

特定のフィールドが実行する集計の種類を取得します。

```xpp
public SelectionField fieldAggregation(FieldId fieldId)
```

### <a name="parameters---fieldaggregation"></a>パラメーター - fieldAggregation

fieldId  

### <a name="return-value---fieldaggregation"></a>戻り値 - fieldAggregation

集約のタイプ。

## <a name="method-fielddatasource"></a>メソッド fieldDatasource

特定のフィールドの発生元データ ソースの ID を取得します。

```xpp
public int fieldDatasource(FieldId fieldId)
```

### <a name="parameters---fielddatasource"></a>パラメーター - fieldDatasource

fieldId  

### <a name="return-value---fielddatasource"></a>戻り値 - fieldDatasource

データ ソース ID。

## <a name="method-fielddatasourceid"></a>メソッド fieldDatasourceID

特定のフィールドがマッピングされるビューでデータ ソースの ID を取得します。

```xpp
public TableId fieldDatasourceID(FieldId fieldId)
```

### <a name="parameters---fielddatasourceid"></a>パラメーター - fieldDatasourceID

fieldId  

### <a name="return-value---fielddatasourceid"></a>戻り値 - fieldDatasourceID

データ ソース ID。

## <a name="method-fieldid"></a>メソッド fieldId

元のテーブルのフィールド ID を取得します。

```xpp
public FieldId fieldId(FieldId fieldId)
```

### <a name="parameters---fieldid"></a>パラメーター - fieldId

fieldId  

### <a name="return-value---fieldid"></a>戻り値 - fieldId

基になるテーブルのフィールド ID。

## <a name="method-isaggregatedview"></a>メソッド isAggregatedView

ビューが集約されているかどうかをチェックします。

```xpp
public boolean isAggregatedView()
```

### <a name="return-value---isaggregatedview"></a>戻り値 - isAggregatedView

ビューが集計される場合は true。それ以外の場合は false。

## <a name="method-query"></a>メソッド query

```xpp
public Query query()
```

### <a name="return-value---query"></a>戻り値 - query

## <a name="method-isdataentity"></a>メソッド isDataEntity

```xpp
public boolean isDataEntity()
```

### <a name="return-value---isdataentity"></a>戻り値 - isDataEntity

## <a name="method-isupdatable"></a>メソッド isUpdatable

```xpp
public boolean isUpdatable()
```

### <a name="return-value---isupdatable"></a>戻り値 - isUpdatable

## <a name="method-ispublic"></a>メソッド isPublic

```xpp
public boolean isPublic()
```

### <a name="return-value---ispublic"></a>戻り値 - isPublic

## <a name="method-collectionname"></a>メソッド collectionName

```xpp
public str collectionName()
```

### <a name="return-value---collectionname"></a>戻り値 - collectionName

## <a name="method-isvirtualfield"></a>メソッド isVirtualField

```xpp
public boolean isVirtualField(str fieldName)
```

### <a name="parameters---isvirtualfield"></a>パラメーター - isVirtualField

fieldName  

### <a name="return-value---isvirtualfield"></a>戻り値 - isVirtualField

## <a name="method-getfieldaccessmodifier"></a>メソッド getFieldAccessModifier

```xpp
public FieldAccessModifier getFieldAccessModifier(str fieldName)
```

### <a name="parameters---getfieldaccessmodifier"></a>パラメーター - getFieldAccessModifier

fieldName  

### <a name="return-value---getfieldaccessmodifier"></a>戻り値 - getFieldAccessModifier

## <a name="method-isstaged"></a>メソッド isStaged

```xpp
public boolean isStaged()
```

### <a name="return-value---isstaged"></a>戻り値 - isStaged

## <a name="method-version"></a>メソッド version

```xpp
public str version()
```

### <a name="return-value---version"></a>戻り値 - version

## <a name="method-messagingrole"></a>メソッド messagingRole

```xpp
public MessagingRole messagingRole()
```

### <a name="return-value---messagingrole"></a>戻り値 - messagingRole

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(TableId tableId)
```

### <a name="parameters---new"></a>パラメーター - new

tableId  
クラス インスタンスの作成に使用するテーブル ID。

