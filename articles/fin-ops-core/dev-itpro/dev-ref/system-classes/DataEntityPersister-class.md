---
title: DataEntityPersister クラス
description: このトピックでは、DataEntityPersister クラスについて説明します。
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
ms.openlocfilehash: 41f78007d70e0f0adb36c343d7344619dc158416
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502742"
---
# <a name="class-dataentitypersister"></a>クラス DataEntityPersister

[!include [banner](../../includes/banner.md)]

```xpp
class DataEntityPersister extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                                                                                                            | 説明 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| public boolean doSaveDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)                                                                                             |             |
| public Common doFindDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)                                                                                              |             |
| public boolean hasDataSourceRecordChanged(int dataSourceId, Common originalRecord, Common updatedRecord)                                                                                                          |             |
| public str getCompanyForDataSource(DataEntityRuntimeContext entityCtx, int dataSourceId)                                                                                                                          |             |
| public int getValidTimeStateUpdateModeForDataSource(DataEntityRuntimeContext entityCtx, int dataSourceId)                                                                                                         |             |
| public Common findDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)                                                                                                |             |
| public boolean saveDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)                                                                                               |             |
| public void doMapEntityToDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)                                                                                         |             |
| public void mapEntityToDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)                                                                                           |             |
| public void doMapDataSourceToEntity(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)                                                                                         |             |
| public void selectDataSourceBufferByRecId(Common dataSourceBuffer, Int64 dataSourceRecId, Boolean explicitlyForUpdate, Boolean fetchActiveRecordOnly)                                                             |             |
| public void doPersistEntity(DataEntityRuntimeContext entityCtx)                                                                                                                                                   |             |
| public void doInitializeDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)                                                                                          |             |
| public void initializeDataSource(DataEntityRuntimeContext entityCtx, str dataSourceName, Common dataSourceBuffer, int dataSourceId, Boolean optional, Boolean readonly, Boolean oneToMany, Boolean dateEffective) |             |

## <a name="method-dosavedatasource"></a>メソッド doSaveDataSource

```xpp
public boolean doSaveDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)
```

### <a name="parameters---dosavedatasource"></a>パラメーター - doSaveDataSource

entityCtx  

<!-- -->

dataSourceCtx  

### <a name="return-value---dosavedatasource"></a>戻り値 - doSaveDataSource

## <a name="method-dofinddatasource"></a>メソッド doFindDataSource

```xpp
public Common doFindDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)
```

### <a name="parameters---dofinddatasource"></a>パラメーター - doFindDataSource

entityCtx  

<!-- -->

dataSourceCtx  

### <a name="return-value---dofinddatasource"></a>戻り値 - doFindDataSource

## <a name="method-hasdatasourcerecordchanged"></a>メソッド hasDataSourceRecordChanged

```xpp
public boolean hasDataSourceRecordChanged(int dataSourceId, Common originalRecord, Common updatedRecord)
```

### <a name="parameters---hasdatasourcerecordchanged"></a>パラメーター - hasDataSourceRecordChanged

dataSourceId  

<!-- -->

originalRecord  

<!-- -->

updatedRecord  

### <a name="return-value---hasdatasourcerecordchanged"></a>戻り値 - hasDataSourceRecordChanged

## <a name="method-getcompanyfordatasource"></a>メソッド getCompanyForDataSource

```xpp
public str getCompanyForDataSource(DataEntityRuntimeContext entityCtx, int dataSourceId)
```

### <a name="parameters---getcompanyfordatasource"></a>パラメーター - getCompanyForDataSource

entityCtx  

<!-- -->

dataSourceId  

### <a name="return-value---getcompanyfordatasource"></a>戻り値 - getCompanyForDataSource

## <a name="method-getvalidtimestateupdatemodefordatasource"></a>メソッド getValidTimeStateUpdateModeForDataSource

```xpp
public int getValidTimeStateUpdateModeForDataSource(DataEntityRuntimeContext entityCtx, int dataSourceId)
```

### <a name="parameters---getvalidtimestateupdatemodefordatasource"></a>パラメーター - getValidTimeStateUpdateModeForDataSource

entityCtx  

<!-- -->

dataSourceId  

### <a name="return-value---getvalidtimestateupdatemodefordatasource"></a>戻り値 - getValidTimeStateUpdateModeForDataSource

## <a name="method-finddatasource"></a>メソッド findDataSource

```xpp
public Common findDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)
```

### <a name="parameters---finddatasource"></a>パラメーター - findDataSource

entityCtx  

<!-- -->

dataSourceCtx  

### <a name="return-value---finddatasource"></a>戻り値 - findDataSource

## <a name="method-savedatasource"></a>メソッド saveDataSource

```xpp
public boolean saveDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)
```

### <a name="parameters---savedatasource"></a>パラメーター - saveDataSource

entityCtx  

<!-- -->

dataSourceCtx  

### <a name="return-value---savedatasource"></a>戻り値 - saveDataSource

## <a name="method-domapentitytodatasource"></a>メソッド doMapEntityToDataSource

```xpp
public void doMapEntityToDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)
```

### <a name="parameters---domapentitytodatasource"></a>パラメーター - doMapEntityToDataSource

entityCtx  

<!-- -->

dataSourceCtx  

## <a name="method-mapentitytodatasource"></a>メソッド mapEntityToDataSource

```xpp
public void mapEntityToDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)
```

### <a name="parameters---mapentitytodatasource"></a>パラメーター - mapEntityToDataSource

entityCtx  

<!-- -->

dataSourceCtx  

## <a name="method-domapdatasourcetoentity"></a>メソッド doMapDataSourceToEntity

```xpp
public void doMapDataSourceToEntity(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)
```

### <a name="parameters---domapdatasourcetoentity"></a>パラメーター - doMapDataSourceToEntity

entityCtx  

<!-- -->

dataSourceCtx  

## <a name="method-selectdatasourcebufferbyrecid"></a>メソッド selectDataSourceBufferByRecId

```xpp
public void selectDataSourceBufferByRecId(Common dataSourceBuffer, Int64 dataSourceRecId, Boolean explicitlyForUpdate, Boolean fetchActiveRecordOnly)
```

### <a name="parameters---selectdatasourcebufferbyrecid"></a>パラメーター - selectDataSourceBufferByRecId

dataSourceBuffer  

<!-- -->

dataSourceRecId  

<!-- -->

explicitlyForUpdate  

<!-- -->

fetchActiveRecordOnly  

## <a name="method-dopersistentity"></a>メソッド doPersistEntity

```xpp
public void doPersistEntity(DataEntityRuntimeContext entityCtx)
```

### <a name="parameters---dopersistentity"></a>パラメーター - doPersistEntity

entityCtx  

## <a name="method-doinitializedatasource"></a>メソッド doInitializeDataSource

```xpp
public void doInitializeDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)
```

### <a name="parameters---doinitializedatasource"></a>パラメーター - doInitializeDataSource

entityCtx  

<!-- -->

dataSourceCtx  

## <a name="method-initializedatasource"></a>メソッド initializeDataSource

```xpp
public void initializeDataSource(DataEntityRuntimeContext entityCtx, str dataSourceName, Common dataSourceBuffer, int dataSourceId, Boolean optional, Boolean readonly, Boolean oneToMany, Boolean dateEffective)
```

### <a name="parameters---initializedatasource"></a>パラメーター - initializeDataSource

entityCtx  

<!-- -->

dataSourceName  

<!-- -->

dataSourceBuffer  

<!-- -->

dataSourceId  

<!-- -->

省略可  

<!-- -->

readonly  

<!-- -->

oneToMany  

<!-- -->

dateEffective  

