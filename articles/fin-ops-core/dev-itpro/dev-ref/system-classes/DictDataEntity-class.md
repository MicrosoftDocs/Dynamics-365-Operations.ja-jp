---
title: DictDataEntity クラス
description: このトピックでは、DictDataEntity クラスについて説明します。
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
ms.openlocfilehash: b69788ad9349ee2ea8d00dfe2e34b9f93fbfab06
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502991"
---
# <a name="class-dictdataentity"></a>クラス DictDataEntity

[!include [banner](../../includes/banner.md)]

```xpp
class DictDataEntity extends DictView
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                  | 説明 |
|---------------------------------------------------------|-------------|
| public boolean isAggregateDataEntity()                  |             |
| public boolean isReadOnly()                             |             |
| public str primaryCompanyContext()                      |             |
| public str primaryKey()                                 |             |
| public boolean supportsSetBasedSqlOperations()          |             |
| public AutoNo enableSetBasedSqlOperations()             |             |
| public str modules()                                    |             |
| public EntityCategory entityCategory()                  |             |
| public boolean dataManagementEnabled()                  |             |
| public str dataManagementStagingTable()                 |             |
| public str publicCollectionName()                       |             |
| public str publicEntityName()                           |             |
| public boolean dataSourceIsReadOnly(str dataSourceName) |             |
| public str dataSourceID2Name(int dataSourceId)          |             |
| public boolean hasExtensionFields()                     |             |
| public List getExtensionFieldNames()                    |             |
| ::public static List listOfDataEntities()               |             |
| public void new(TableId tableId)                        |             |

## <a name="method-isaggregatedataentity"></a>メソッド isAggregateDataEntity

```xpp
public boolean isAggregateDataEntity()
```

### <a name="return-value---isaggregatedataentity"></a>戻り値 - isAggregateDataEntity

## <a name="method-isreadonly"></a>メソッド isReadOnly

```xpp
public boolean isReadOnly()
```

### <a name="return-value---isreadonly"></a>戻り値 - DictDataEntity

## <a name="method-primarycompanycontext"></a>メソッド primaryCompanyContext

```xpp
public str primaryCompanyContext()
```

### <a name="return-value---primarycompanycontext"></a>戻り値 - primaryCompanyContext

## <a name="method-primarykey"></a>メソッド primaryKey

```xpp
public str primaryKey()
```

### <a name="return-value---primarykey"></a>戻り値 - primaryKey

## <a name="method-supportssetbasedsqloperations"></a>メソッド supportsSetBasedSqlOperations

```xpp
public boolean supportsSetBasedSqlOperations()
```

### <a name="return-value---supportssetbasedsqloperations"></a>戻り値 - supportsSetBasedSqlOperations

## <a name="method-enablesetbasedsqloperations"></a>メソッド enableSetBasedSqlOperations

```xpp
public AutoNo enableSetBasedSqlOperations()
```

### <a name="return-value---enablesetbasedsqloperations"></a>戻り値 - enableSetBasedSqlOperations

## <a name="method-modules"></a>メソッド modules

```xpp
public str modules()
```

### <a name="return-value---modules"></a>戻り値 - modules

## <a name="method-entitycategory"></a>メソッド entityCategory

```xpp
public EntityCategory entityCategory()
```

### <a name="return-value---entitycategory"></a>戻り値 - entityCategory

## <a name="method-datamanagementenabled"></a>メソッド dataManagementEnabled

```xpp
public boolean dataManagementEnabled()
```

### <a name="return-value---datamanagementenabled"></a>戻り値 - dataManagementEnabled

## <a name="method-datamanagementstagingtable"></a>メソッド dataManagementStagingTable

```xpp
public str dataManagementStagingTable()
```

### <a name="return-value---datamanagementstagingtable"></a>戻り値 - dataManagementStagingTable

## <a name="method-publiccollectionname"></a>メソッド publicCollectionName

```xpp
public str publicCollectionName()
```

### <a name="return-value---publiccollectionname"></a>戻り値 - publicCollectionName

## <a name="method-publicentityname"></a>メソッド publicEntityName

```xpp
public str publicEntityName()
```

### <a name="return-value---publicentityname"></a>戻り値 - publicEntityName

## <a name="method-datasourceisreadonly"></a>メソッド dataSourceIsReadOnly

```xpp
public boolean dataSourceIsReadOnly(str dataSourceName)
```

### <a name="parameters---datasourceisreadonly"></a>パラメーター - dataSourceIsReadOnly

dataSourceName  

### <a name="return-value---datasourceisreadonly"></a>戻り値 - dataSourceIsReadOnly

## <a name="method-datasourceid2name"></a>メソッド dataSourceID2Name

```xpp
public str dataSourceID2Name(int dataSourceId)
```

### <a name="parameters---datasourceid2name"></a>パラメーター - dataSourceID2Name

dataSourceId  

### <a name="return-value---datasourceid2name"></a>戻り値 - dataSourceID2Name

## <a name="method-hasextensionfields"></a>メソッド hasExtensionFields

```xpp
public boolean hasExtensionFields()
```

### <a name="return-value---hasextensionfields"></a>戻り値 - hasExtensionFields

## <a name="method-getextensionfieldnames"></a>メソッド getExtensionFieldNames

```xpp
public List getExtensionFieldNames()
```

### <a name="return-value---getextensionfieldnames"></a>戻り値 - getExtensionFieldNames

## <a name="method-listofdataentities"></a>メソッド listOfDataEntities

```xpp
public static List listOfDataEntities()
```

### <a name="return-value---listofdataentities"></a>戻り値 - listOfDataEntities

## <a name="method-new"></a>メソッド new

```xpp
public void new(TableId tableId)
```

### <a name="parameters---new"></a>パラメーター - new

tableId  

