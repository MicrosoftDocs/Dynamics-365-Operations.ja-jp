---
title: DataSetRun クラス
description: このトピックでは、DataSetRun クラスについて説明します。
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
ms.openlocfilehash: d28bb8fb5b3264abfc9a7e37fc6c718d7d291de3
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502735"
---
# <a name="class-datasetrun"></a>クラス DataSetRun

[!include [banner](../../includes/banner.md)]

```xpp
class DataSetRun extends ObjectRun
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                                                                              | 説明                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| public FormDataSource addDataSource(TableId tableId, \[str joinDataSourceName\], \[DataSourceLinkTypePropertyValues linkType\], \[FieldId joinFieldId\], \[str newDataSourceName\]) | dataSetRun クラスに新しいデータ ソースを追加します。                               |
| public DataSet dataSet()                                                                                                                                                            |                                                                               |
| public FormObjectSet dataSource(\[AnyType objectSet\])                                                                                                                              |                                                                               |
| public FormObjectSet dataSourceById(int id)                                                                                                                                         |                                                                               |
| public int dataSourceCount()                                                                                                                                                        |                                                                               |
| public Array getActiveFields(int dataSourceId)                                                                                                                                      |                                                                               |
| public container getChildrenById(str dataSourceName, \[AnyType parentId\])                                                                                                          | 親 ID を使用してデータ ソースの子を取得します。                    |
| public container getChildrenByIndex(str dataSourceName, \[int parentIndex\])                                                                                                        | 親インデックスを使用してデータ ソースの子を取得します。                 |
| public DataSetError getLastError()                                                                                                                                                  |                                                                               |
| public AnyType getParentById(str dataSourceName, AnyType childId)                                                                                                                   | 子 ID を使用してデータ ソースの親を取得します。                       |
| public int getParentByIndex(str dataSourceName, int childIndex)                                                                                                                     | 子インデックスを使用してデータ ソースの親を取得します。                    |
| public int getRowIndexFromRowHierarchyId(str dataSourceName, AnyType id)                                                                                                            | 行階層 ID を使用してデータ ソース内の行インデックスを取得します。              |
| public boolean initComplete()                                                                                                                                                       |                                                                               |
| public str name()                                                                                                                                                                   |                                                                               |
| public FormObjectSet objectSet(\[AnyType objectSet\])                                                                                                                               |                                                                               |
| public container pack()                                                                                                                                                             | DataSetRun クラスの現在のインスタンスをシリアル化します。                      |
| public boolean runCalled()                                                                                                                                                          |                                                                               |
| public boolean unpack(container pack)                                                                                                                                               | pack パラメーター値を DataSetRun クラスのインスタンスに逆シリアル化します。 |
| ::public static DataSetRun create(str name, container pack)                                                                                                                         |                                                                               |
| ::public static DataSetRun createRunTime(container pack)                                                                                                                            |                                                                               |
| public void setLastError(DataSetError error)                                                                                                                                        |                                                                               |
| public void run()                                                                                                                                                                   |                                                                               |
| public void setLookupMode()                                                                                                                                                         | データセットをルックアップ モードにします。                                            |
| public void new(xArgs args)                                                                                                                                                         | Object クラスの新しいインスタンスを初期化します。                               |
| public void finalize()                                                                                                                                                              |                                                                               |
| public void createRecord(str formDataSourceName, \[boolean append\])                                                                                                                | 新しいレコードを作成します。                                                         |
| public void setActiveFields(int dataSourceId, Array fieldIds)                                                                                                                       |                                                                               |
| public void setExternalContext(\[Common externalContext\])                                                                                                                          | dataSetRun オブジェクトの外部コンテキストを設定します。                           |
| public void init()                                                                                                                                                                  |                                                                               |
| public void enableHierarchicalDataBrowsing(str hierarchyPKDataSourceName, FieldId hierarchyPKfieldId, str hierarchyFKDataSourceName, FieldId hierarchyFKfieldId)                    | 階層データの参照を有効にします。                                           |
| public void disableHierarchicalDataBrowsing(str dataSourceName)                                                                                                                     | 階層データの参照を無効にします。                                          |

## <a name="method-adddatasource"></a>メソッド addDataSource

dataSetRun クラスに新しいデータ ソースを追加します。

```xpp
public FormDataSource addDataSource(TableId tableId, [str joinDataSourceName], [DataSourceLinkTypePropertyValues linkType], [FieldId joinFieldId], [str newDataSourceName])
```

### <a name="parameters---adddatasource"></a>パラメーター - addDataSource

tableId  
新しいデータ ソースの名前。

<!-- -->

joinDataSourceName  
新しいデータ ソースの名前。

<!-- -->

linkType  
新しいデータ ソースの名前。

<!-- -->

joinFieldId  
新しいデータ ソースの名前。

<!-- -->

newDataSourceName  
新しいデータ ソースの名前。

### <a name="return-value---adddatasource"></a>戻り値 - addDataSource

新しいデータ ソースを選択します。

## <a name="method-dataset"></a>メソッド dataSet

```xpp
public DataSet dataSet()
```

### <a name="return-value---dataset"></a>戻り値 - dataSet

## <a name="method-datasource"></a>メソッド dataSource

```xpp
public FormObjectSet dataSource([AnyType objectSet])
```

### <a name="parameters---datasource"></a>パラメーター - dataSource

objectSet  

### <a name="return-value---datasource"></a>戻り値 - dataSource

## <a name="method-datasourcebyid"></a>メソッド dataSourceById

```xpp
public FormObjectSet dataSourceById(int id)
```

### <a name="parameters---datasourcebyid"></a>パラメーター - dataSourceById

id  

### <a name="return-value---datasourcebyid"></a>戻り値 - dataSourceById

## <a name="method-datasourcecount"></a>メソッド dataSourceCount

```xpp
public int dataSourceCount()
```

### <a name="return-value---datasourcecount"></a>戻り値 - dataSourceCount

## <a name="method-getactivefields"></a>メソッド getActiveFields

```xpp
public Array getActiveFields(int dataSourceId)
```

### <a name="parameters---getactivefields"></a>パラメーター - getActiveFields

dataSourceId  

### <a name="return-value---getactivefields"></a>戻り値 - getActiveFields

## <a name="method-getchildrenbyid"></a>メソッド getChildrenById

親 ID を使用してデータ ソースの子を取得します。

```xpp
public container getChildrenById(str dataSourceName, [AnyType parentId])
```

### <a name="parameters---getchildrenbyid"></a>パラメーター - getChildrenById

dataSourceName  
親 ID。

<!-- -->

parentId  
親 ID。

### <a name="return-value---getchildrenbyid"></a>戻り値 - getChildrenById

子のためのコンテナーです。

## <a name="method-getchildrenbyindex"></a>メソッド getChildrenByIndex

親インデックスを使用してデータ ソースの子を取得します。

```xpp
public container getChildrenByIndex(str dataSourceName, [int parentIndex])
```

### <a name="parameters---getchildrenbyindex"></a>パラメーター - getChildrenByIndex

dataSourceName  
親インデックス。

<!-- -->

parentIndex  
親インデックス。

### <a name="return-value---getchildrenbyindex"></a>戻り値 - getChildrenByIndex

子のためのコンテナーです。

## <a name="method-getlasterror"></a>メソッド getLastError

```xpp
public DataSetError getLastError()
```

### <a name="return-value---getlasterror"></a>戻り値 - getLastError

## <a name="method-getparentbyid"></a>メソッド getParentById

子 ID を使用してデータ ソースの親を取得します。

```xpp
public AnyType getParentById(str dataSourceName, AnyType childId)
```

### <a name="parameters---getparentbyid"></a>パラメーター - getParentById

dataSourceName  
子 ID。

<!-- -->

childId  
子 ID。

### <a name="return-value---getparentbyid"></a>戻り値 - getParentById

親 ID。

## <a name="method-getparentbyindex"></a>メソッド getParentByIndex

子インデックスを使用してデータ ソースの親を取得します。

```xpp
public int getParentByIndex(str dataSourceName, int childIndex)
```

### <a name="parameters---getparentbyindex"></a>パラメーター - getParentByIndex

dataSourceName  
子インデックス。

<!-- -->

childIndex  
子インデックス。

### <a name="return-value---getparentbyindex"></a>戻り値 - getParentByIndex

親 ID。

## <a name="method-getrowindexfromrowhierarchyid"></a>メソッド getRowIndexFromRowHierarchyId

行階層 ID を使用してデータ ソース内の行インデックスを取得します。

```xpp
public int getRowIndexFromRowHierarchyId(str dataSourceName, AnyType id)
```

### <a name="parameters---getrowindexfromrowhierarchyid"></a>パラメーター - getRowIndexFromRowHierarchyId

dataSourceName  
行の階層 ID。

<!-- -->

id  
行の階層 ID。

### <a name="return-value---getrowindexfromrowhierarchyid"></a>戻り値 - getRowIndexFromRowHierarchyId

行インデックス。

## <a name="method-initcomplete"></a>メソッド initComplete

```xpp
public boolean initComplete()
```

### <a name="return-value---initcomplete"></a>戻り値 - initComplete

## <a name="method-name"></a>メソッド名

```xpp
public str name()
```

### <a name="return-value---name"></a>戻り値 - name

## <a name="method-objectset"></a>メソッド objectSet

```xpp
public FormObjectSet objectSet([AnyType objectSet])
```

### <a name="parameters---objectset"></a>パラメーター - objectSet

objectSet  

### <a name="return-value---objectset"></a>戻り値 - objectSet

## <a name="method-pack"></a>メソッド pack

DataSetRun クラスの現在のインスタンスをシリアル化します。

```xpp
public container pack()
```

### <a name="return-value---pack"></a>戻り値 - pack

DataSetRun クラスの現在のインスタンスを含むコンテナーです。

## <a name="method-runcalled"></a>メソッド runCalled

```xpp
public boolean runCalled()
```

### <a name="return-value---runcalled"></a>戻り値 - runCalled

## <a name="method-unpack"></a>メソッド unpack

pack パラメーター値を DataSetRun クラスのインスタンスに逆シリアル化します。

```xpp
public boolean unpack(container pack)
```

### <a name="parameters---unpack"></a>パラメーター - unpack

梱包  
インスタンスを逆シリアル化するコンテナー。

### <a name="return-value---unpack"></a>戻り値 - unpack

逆シリアル化が成功した場合は true。それ以外の場合は、false。

## <a name="method-create"></a>メソッド create

```xpp
public static DataSetRun create(str name, container pack)
```

### <a name="parameters---create"></a>パラメーター - create

名前  

<!-- -->

梱包  

### <a name="return-value---create"></a>戻り値 - create

## <a name="method-createruntime"></a>メソッド createRunTime

```xpp
public static DataSetRun createRunTime(container pack)
```

### <a name="parameters---createruntime"></a>パラメーター - createRunTime

梱包  

### <a name="return-value---createruntime"></a>戻り値 - createRunTime

## <a name="method-setlasterror"></a>メソッド setLastError

```xpp
public void setLastError(DataSetError error)
```

### <a name="parameters---setlasterror"></a>パラメーター - setLastError

エラー  

## <a name="method-run"></a>メソッド run

```xpp
public void run()
```

## <a name="method-setlookupmode"></a>メソッド setLookupMode

データセットをルックアップ モードにします。

```xpp
public void setLookupMode()
```

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(xArgs args)
```

### <a name="parameters---new"></a>パラメーター - new

args  

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-createrecord"></a>メソッド createRecord

新しいレコードを作成します。

```xpp
public void createRecord(str formDataSourceName, [boolean append])
```

### <a name="parameters---createrecord"></a>パラメーター - createRecord

formDataSourceName  
追加するレコード。

<!-- -->

append  
追加するレコード。

## <a name="method-setactivefields"></a>メソッド setActiveFields

```xpp
public void setActiveFields(int dataSourceId, Array fieldIds)
```

### <a name="parameters---setactivefields"></a>パラメーター - setActiveFields

dataSourceId  

<!-- -->

fieldIds  

## <a name="method-setexternalcontext"></a>メソッド setExternalContext

dataSetRun オブジェクトの外部コンテキストを設定します。

```xpp
public void setExternalContext([Common externalContext])
```

### <a name="parameters---setexternalcontext"></a>パラメーター - setExternalContext

externalContext  
外部コンテキスト。

## <a name="method-init"></a>メソッド init

```xpp
public void init()
```

## <a name="method-enablehierarchicaldatabrowsing"></a>メソッド enableHierarchicalDataBrowsing

階層データの参照を有効にします。

```xpp
public void enableHierarchicalDataBrowsing(str hierarchyPKDataSourceName, FieldId hierarchyPKfieldId, str hierarchyFKDataSourceName, FieldId hierarchyFKfieldId)
```

### <a name="parameters---enablehierarchicaldatabrowsing"></a>パラメーター - enableHierarchicalDataBrowsing

hierarchyPKDataSourceName  
階層内の外部キー フィールドの ID。

<!-- -->

hierarchyPKfieldId  
階層内の外部キー フィールドの ID。

<!-- -->

hierarchyFKDataSourceName  
階層内の外部キー フィールドの ID。

<!-- -->

hierarchyFKfieldId  
階層内の外部キー フィールドの ID。

## <a name="method-disablehierarchicaldatabrowsing"></a>メソッド disableHierarchicalDataBrowsing

階層データの参照を無効にします。

```xpp
public void disableHierarchicalDataBrowsing(str dataSourceName)
```

### <a name="parameters---disablehierarchicaldatabrowsing"></a>パラメーター - disableHierarchicalDataBrowsing

dataSourceName  
階層データの参照を無効にするデータ ソースの名前。

