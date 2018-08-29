---
title: "D クラス"
description: "文字 D で始まるシステム API クラス。"
author: RobinARH
manager: AnnBe
ms.date: 11/06/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 52531
ms.assetid: 97f18d4d-1704-40fd-a0a2-2624a5798d66
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 0cb7a4d7a5d6795a855fcc1af72df6dbd528ee92
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="d-classes"></a>D クラス

[!include [banner](../includes/banner.md)]

文字 D で始まるシステム API クラス。

<a name="class-dataentitydatasourceruntimecontext"></a>クラス DataEntityDataSourceRuntimeContext
----------------------------------------

    class DataEntityDataSourceRuntimeContext extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                         | 説明 |
|--------------------------------------------------------------------------------|-------------|
| public str name()                                                              |             |
| public int id()                                                                |             |
| public Common getBuffer()                                                      |             |
| public DataEntityDatabaseOperation getDatabaseOperation()                      |             |
| public str getCompany()                                                        |             |
| public boolean getDataSaved()                                                  |             |
| public boolean skipDataMethods(\[boolean skip\])                               |             |
| public boolean skipDeleteMethod(\[boolean b\])                                 |             |
| public boolean skipValidateWrite(\[boolean skip\])                             |             |
| public boolean skipValidateDelete(\[boolean skip\])                            |             |
| public boolean skipInitValue(\[boolean skip\])                                 |             |
| public boolean skipDefaultRow(\[boolean skip\])                                |             |
| public boolean readOnly()                                                      |             |
| public boolean oneToMany()                                                     |             |
| public boolean optional()                                                      |             |
| public boolean dateEffective()                                                 |             |
| public boolean conflictDetectionInvoked(\[boolean found\])                     |             |
| public void new(Common dataSourceBuffer, str dataSourceName, int dataSourceId) |             |
| public void setCompany(str company)                                            |             |
| public void setBuffer(Common buffer)                                           |             |
| public void setDatabaseOperation(DataEntityDatabaseOperation dbOperation)      |             |
| public void setDataSaved(boolean saved)                                        |             |

### <a name="method-name"></a>メソッド名

    public str name()

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

    public int id()

#### <a name="return-value"></a>戻り値

### <a name="method-getbuffer"></a>メソッド getBuffer

    public Common getBuffer()

#### <a name="return-value"></a>戻り値

### <a name="method-getdatabaseoperation"></a>メソッド getDatabaseOperation

    public DataEntityDatabaseOperation getDatabaseOperation()

#### <a name="return-value"></a>戻り値

### <a name="method-getcompany"></a>メソッド getCompany

    public str getCompany()

#### <a name="return-value"></a>戻り値

### <a name="method-getdatasaved"></a>メソッド getDataSaved

    public boolean getDataSaved()

#### <a name="return-value"></a>戻り値

### <a name="method-skipdatamethods"></a>メソッド skipDataMethods

    public boolean skipDataMethods([boolean skip])

#### <a name="parameters"></a>パラメーター

skip  

#### <a name="return-value"></a>戻り値

### <a name="method-skipdeletemethod"></a>メソッド skipDeleteMethod

    public boolean skipDeleteMethod([boolean b])

#### <a name="parameters"></a>パラメーター

b  

#### <a name="return-value"></a>戻り値

### <a name="method-skipvalidatewrite"></a>メソッド skipValidateWrite

    public boolean skipValidateWrite([boolean skip])

#### <a name="parameters"></a>パラメーター

skip  

#### <a name="return-value"></a>戻り値

### <a name="method-skipvalidatedelete"></a>メソッド skipValidateDelete

    public boolean skipValidateDelete([boolean skip])

#### <a name="parameters"></a>パラメーター

skip  

#### <a name="return-value"></a>戻り値

### <a name="method-skipinitvalue"></a>メソッド skipInitValue

    public boolean skipInitValue([boolean skip])

#### <a name="parameters"></a>パラメーター

skip  

#### <a name="return-value"></a>戻り値

### <a name="method-skipdefaultrow"></a>メソッド skipDefaultRow

    public boolean skipDefaultRow([boolean skip])

#### <a name="parameters"></a>パラメーター

skip  

#### <a name="return-value"></a>戻り値

### <a name="method-readonly"></a>メソッド readOnly

    public boolean readOnly()

#### <a name="return-value"></a>戻り値

### <a name="method-onetomany"></a>メソッド oneToMany

    public boolean oneToMany()

#### <a name="return-value"></a>戻り値

### <a name="method-optional"></a>メソッド optional

    public boolean optional()

#### <a name="return-value"></a>戻り値

### <a name="method-dateeffective"></a>メソッド dateEffective

    public boolean dateEffective()

#### <a name="return-value"></a>戻り値

### <a name="method-conflictdetectioninvoked"></a>メソッド conflictDetectionInvoked

    public boolean conflictDetectionInvoked([boolean found])

#### <a name="parameters"></a>パラメーター

found  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

    public void new(Common dataSourceBuffer, str dataSourceName, int dataSourceId)

#### <a name="parameters"></a>パラメーター

dataSourceBuffer  

<!-- -->

dataSourceName  

<!-- -->

dataSourceId  

### <a name="method-setcompany"></a>メソッド setCompany

    public void setCompany(str company)

#### <a name="parameters"></a>パラメーター

会社  

### <a name="method-setbuffer"></a>メソッド setBuffer

    public void setBuffer(Common buffer)

#### <a name="parameters"></a>パラメーター

バッファ  

### <a name="method-setdatabaseoperation"></a>メソッド setDatabaseOperation

    public void setDatabaseOperation(DataEntityDatabaseOperation dbOperation)

#### <a name="parameters"></a>パラメーター

dbOperation  

### <a name="method-setdatasaved"></a>メソッド setDataSaved

    public void setDataSaved(boolean saved)

#### <a name="parameters"></a>パラメーター

 が保存されました  

## <a name="class-dataentitypersister"></a>クラス DataEntityPersister
    class DataEntityPersister extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

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

### <a name="method-dosavedatasource"></a>メソッド doSaveDataSource

    public boolean doSaveDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)

#### <a name="parameters"></a>パラメーター

entityCtx  

<!-- -->

dataSourceCtx  

#### <a name="return-value"></a>戻り値

### <a name="method-dofinddatasource"></a>メソッド doFindDataSource

    public Common doFindDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)

#### <a name="parameters"></a>パラメーター

entityCtx  

<!-- -->

dataSourceCtx  

#### <a name="return-value"></a>戻り値

### <a name="method-hasdatasourcerecordchanged"></a>メソッド hasDataSourceRecordChanged

    public boolean hasDataSourceRecordChanged(int dataSourceId, Common originalRecord, Common updatedRecord)

#### <a name="parameters"></a>パラメーター

dataSourceId  

<!-- -->

originalRecord  

<!-- -->

updatedRecord  

#### <a name="return-value"></a>戻り値

### <a name="method-getcompanyfordatasource"></a>メソッド getCompanyForDataSource

    public str getCompanyForDataSource(DataEntityRuntimeContext entityCtx, int dataSourceId)

#### <a name="parameters"></a>パラメーター

entityCtx  

<!-- -->

dataSourceId  

#### <a name="return-value"></a>戻り値

### <a name="method-getvalidtimestateupdatemodefordatasource"></a>メソッド getValidTimeStateUpdateModeForDataSource

    public int getValidTimeStateUpdateModeForDataSource(DataEntityRuntimeContext entityCtx, int dataSourceId)

#### <a name="parameters"></a>パラメーター

entityCtx  

<!-- -->

dataSourceId  

#### <a name="return-value"></a>戻り値

### <a name="method-finddatasource"></a>メソッド findDataSource

    public Common findDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)

#### <a name="parameters"></a>パラメーター

entityCtx  

<!-- -->

dataSourceCtx  

#### <a name="return-value"></a>戻り値

### <a name="method-savedatasource"></a>メソッド saveDataSource

    public boolean saveDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)

#### <a name="parameters"></a>パラメーター

entityCtx  

<!-- -->

dataSourceCtx  

#### <a name="return-value"></a>戻り値

### <a name="method-domapentitytodatasource"></a>メソッド doMapEntityToDataSource

    public void doMapEntityToDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)

#### <a name="parameters"></a>パラメーター

entityCtx  

<!-- -->

dataSourceCtx  

### <a name="method-mapentitytodatasource"></a>メソッド mapEntityToDataSource

    public void mapEntityToDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)

#### <a name="parameters"></a>パラメーター

entityCtx  

<!-- -->

dataSourceCtx  

### <a name="method-domapdatasourcetoentity"></a>メソッド doMapDataSourceToEntity

    public void doMapDataSourceToEntity(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)

#### <a name="parameters"></a>パラメーター

entityCtx  

<!-- -->

dataSourceCtx  

### <a name="method-selectdatasourcebufferbyrecid"></a>メソッド selectDataSourceBufferByRecId

    public void selectDataSourceBufferByRecId(Common dataSourceBuffer, Int64 dataSourceRecId, Boolean explicitlyForUpdate, Boolean fetchActiveRecordOnly)

#### <a name="parameters"></a>パラメーター

dataSourceBuffer  

<!-- -->

dataSourceRecId  

<!-- -->

explicitlyForUpdate  

<!-- -->

fetchActiveRecordOnly  

### <a name="method-dopersistentity"></a>メソッド doPersistEntity

    public void doPersistEntity(DataEntityRuntimeContext entityCtx)

#### <a name="parameters"></a>パラメーター

entityCtx  

### <a name="method-doinitializedatasource"></a>メソッド doInitializeDataSource

    public void doInitializeDataSource(DataEntityRuntimeContext entityCtx, DataEntityDataSourceRuntimeContext dataSourceCtx)

#### <a name="parameters"></a>パラメーター

entityCtx  

<!-- -->

dataSourceCtx  

### <a name="method-initializedatasource"></a>メソッド initializeDataSource

    public void initializeDataSource(DataEntityRuntimeContext entityCtx, str dataSourceName, Common dataSourceBuffer, int dataSourceId, Boolean optional, Boolean readonly, Boolean oneToMany, Boolean dateEffective)

#### <a name="parameters"></a>パラメーター

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

## <a name="class-dataentityruntimecontext"></a>クラス DataEntityRuntimeContext
    class DataEntityRuntimeContext extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                               | 説明 |
|------------------------------------------------------------------------------------------------------|-------------|
| public DataEntityDatabaseOperation getDatabaseOperation()                                            |             |
| public AnyType getCustomProperty(str name)                                                           |             |
| public Common getEntityRecord()                                                                      |             |
| public DataEntityDataSourceRuntimeContext getRuntimeContextByName(str datasourceName)                |             |
| public void new(DataEntityDatabaseOperation operation, Common record, DataEntityPersister persister) |             |
| public void setCustomProperty(str name, AnyType obj)                                                 |             |

### <a name="method-getdatabaseoperation"></a>メソッド getDatabaseOperation

    public DataEntityDatabaseOperation getDatabaseOperation()

#### <a name="return-value"></a>戻り値

### <a name="method-getcustomproperty"></a>メソッド getCustomProperty

    public AnyType getCustomProperty(str name)

#### <a name="parameters"></a>パラメーター

名前  

#### <a name="return-value"></a>戻り値

### <a name="method-getentityrecord"></a>メソッド getEntityRecord

    public Common getEntityRecord()

#### <a name="return-value"></a>戻り値

### <a name="method-getruntimecontextbyname"></a>メソッド getRuntimeContextByName

    public DataEntityDataSourceRuntimeContext getRuntimeContextByName(str datasourceName)

#### <a name="parameters"></a>パラメーター

datasourceName  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

    public void new(DataEntityDatabaseOperation operation, Common record, DataEntityPersister persister)

#### <a name="parameters"></a>パラメーター

工程  

<!-- -->

記録  

<!-- -->

persister  

### <a name="method-setcustomproperty"></a>メソッド setCustomProperty

    public void setCustomProperty(str name, AnyType obj)

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

obj  

## <a name="class-dataeventargs"></a>クラス DataEventArgs
    class DataEventArgs

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法 | 説明 |
|--------|-------------|
|        |             |

## <a name="class-dataimportexportmanager"></a>クラス DataImportExportManager
    class DataImportExportManager extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                               | 説明 |
|--------------------------------------|-------------|
| public void finalize()               |             |
| public void new()                    |             |
| public void importDataFile(str name) |             |

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-new"></a>メソッド new

    public void new()

### <a name="method-importdatafile"></a>メソッド importDataFile

    public void importDataFile(str name)

#### <a name="parameters"></a>パラメーター

名前  

## <a name="class-dataimportmanager"></a>クラス DataImportManager
    class DataImportManager extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                        | 説明                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| ::public static int commitImportSessionInfo(DataImportSessionInfo impInfo)                    |                                                            |
| ::public static int endTableDataCopy(ImportTableDataInfo dataInfo)                            |                                                            |
| ::public static int endTableSchemaCopy(ImportTableSchemaInfo schInfo)                         |                                                            |
| ::public static int finishMergeTableData()                                                    |                                                            |
| ::public static int getImportSessionProgress(DataImportSessionInfo impInfo)                   |                                                            |
| ::public static int mergeAllData()                                                            |                                                            |
| ::public static int mergeTableData(int mergeStep, TableId tableId, boolean updateHeartbeat)   |                                                            |
| ::public static int recoverImportSession(DataImportSessionInfo impInfo, boolean fTryToResume) |                                                            |
| public void new()                                                                             | DataImportManager クラスの新しいインスタンスを初期化します。 |

### <a name="method-commitimportsessioninfo"></a>メソッド commitImportSessionInfo

    public static int commitImportSessionInfo(DataImportSessionInfo impInfo)

#### <a name="parameters"></a>パラメーター

impInfo  

#### <a name="return-value"></a>戻り値

### <a name="method-endtabledatacopy"></a>メソッド endTableDataCopy

    public static int endTableDataCopy(ImportTableDataInfo dataInfo)

#### <a name="parameters"></a>パラメーター

dataInfo  

#### <a name="return-value"></a>戻り値

### <a name="method-endtableschemacopy"></a>メソッド endTableSchemaCopy

    public static int endTableSchemaCopy(ImportTableSchemaInfo schInfo)

#### <a name="parameters"></a>パラメーター

schInfo  

#### <a name="return-value"></a>戻り値

### <a name="method-finishmergetabledata"></a>メソッド finishMergeTableData

    public static int finishMergeTableData()

#### <a name="return-value"></a>戻り値

### <a name="method-getimportsessionprogress"></a>メソッド getImportSessionProgress

    public static int getImportSessionProgress(DataImportSessionInfo impInfo)

#### <a name="parameters"></a>パラメーター

impInfo  

#### <a name="return-value"></a>戻り値

### <a name="method-mergealldata"></a>メソッド mergeAllData

    public static int mergeAllData()

#### <a name="return-value"></a>戻り値

### <a name="method-mergetabledata"></a>メソッド mergeTableData

    public static int mergeTableData(int mergeStep, TableId tableId, boolean updateHeartbeat)

#### <a name="parameters"></a>パラメーター

mergeStep  

<!-- -->

tableId  

<!-- -->

updateHeartbeat  

#### <a name="return-value"></a>戻り値

### <a name="method-recoverimportsession"></a>メソッド recoverImportSession

    public static int recoverImportSession(DataImportSessionInfo impInfo, boolean fTryToResume)

#### <a name="parameters"></a>パラメーター

impInfo  

<!-- -->

fTryToResume  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

DataImportManager クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-dataimportsessioninfo"></a>クラス DataImportSessionInfo
    class DataImportSessionInfo extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                         | 説明                                     |
|--------------------------------------------------------------------------------|-------------------------------------------------|
| public int addImportTable(str szTabName, int ulTableId, boolean fAlwaysUpdate) |                                                 |
| public int getCurrentProgress()                                                |                                                 |
| public str getCurrentTable()                                                   |                                                 |
| public int setSourceGUID(Guid szSourceGUID)                                    |                                                 |
| public int setSysDataImpLogId(int sysDataImpLogId)                             |                                                 |
| public void new(str szInpFileName, boolean fUpdateExistingData)                | Object クラスの新しいインスタンスを初期化します。 |

### <a name="method-addimporttable"></a>メソッド addImportTable

    public int addImportTable(str szTabName, int ulTableId, boolean fAlwaysUpdate)

#### <a name="parameters"></a>パラメーター

szTabName  

<!-- -->

ulTableId  

<!-- -->

fAlwaysUpdate  

#### <a name="return-value"></a>戻り値

### <a name="method-getcurrentprogress"></a>メソッド getCurrentProgress

    public int getCurrentProgress()

#### <a name="return-value"></a>戻り値

### <a name="method-getcurrenttable"></a>メソッド getCurrentTable

    public str getCurrentTable()

#### <a name="return-value"></a>戻り値

### <a name="method-setsourceguid"></a>メソッド setSourceGUID

    public int setSourceGUID(Guid szSourceGUID)

#### <a name="parameters"></a>パラメーター

szSourceGUID  

#### <a name="return-value"></a>戻り値

### <a name="method-setsysdataimplogid"></a>メソッド setSysDataImpLogId

    public int setSysDataImpLogId(int sysDataImpLogId)

#### <a name="parameters"></a>パラメーター

sysDataImpLogId  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(str szInpFileName, boolean fUpdateExistingData)

#### <a name="parameters"></a>パラメーター

szInpFileName  

<!-- -->

fUpdateExistingData  

## <a name="class-dataset"></a>クラス データセット
    class DataSet extends TreeNode

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                  | 説明                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| public FormBuildDataSource addDataSource(str name)      |                                                                                                                                   |
| public str changedBy(\[str value\])                     | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                        |
| public Date changedDate(\[Date value\])                 | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                     |
| public str changedTime(\[str value\])                   | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                     |
| public str createdBy(\[str value\])                     | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                             |
| public Date creationDate(\[Date value\])                | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                          |
| public str creationTime(\[str value\])                  |                                                                                                                                   |
| public FormBuildDataSource dataSource(int dataSourceNo) |                                                                                                                                   |
| public int dataSourceCount()                            |                                                                                                                                   |
| public str name(\[str value\])                          | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public Guid origin(\[Guid value\])                      |                                                                                                                                   |
| public void load(str name, \[boolean buildMode\])       |                                                                                                                                   |
| public void finalize()                                  |                                                                                                                                   |
| public void new(\[str name\], \[boolean buildMode\])    | TreeNode クラスの新しいインスタンスを初期化します。                                                                                 |
| public void save()                                      |                                                                                                                                   |

### <a name="method-adddatasource"></a>メソッド addDataSource

    public FormBuildDataSource addDataSource(str name)

#### <a name="parameters"></a>パラメーター

名前  

#### <a name="return-value"></a>戻り値

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

### <a name="method-datasource"></a>メソッド dataSource

    public FormBuildDataSource dataSource(int dataSourceNo)

#### <a name="parameters"></a>パラメーター

dataSourceNo  

#### <a name="return-value"></a>戻り値

### <a name="method-datasourcecount"></a>メソッド dataSourceCount

    public int dataSourceCount()

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

### <a name="method-origin"></a>メソッド origin

    public Guid origin([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-load"></a>メソッド load

    public void load(str name, [boolean buildMode])

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

buildMode  

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-new"></a>メソッド new

TreeNode クラスの新しいインスタンスを初期化します。

    public void new([str name], [boolean buildMode])

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

buildMode  

### <a name="method-save"></a>メソッド save

    public void save()

## <a name="class-datasetrun"></a>クラス DataSetRun
    class DataSetRun extends ObjectRun

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

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

### <a name="method-adddatasource"></a>メソッド addDataSource

dataSetRun クラスに新しいデータ ソースを追加します。

    public FormDataSource addDataSource(TableId tableId, [str joinDataSourceName], [DataSourceLinkTypePropertyValues linkType], [FieldId joinFieldId], [str newDataSourceName])

#### <a name="parameters"></a>パラメーター

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

#### <a name="return-value"></a>戻り値

新しいデータ ソースを選択します。

### <a name="method-dataset"></a>メソッド dataSet

    public DataSet dataSet()

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

    public FormObjectSet dataSource([AnyType objectSet])

#### <a name="parameters"></a>パラメーター

objectSet  

#### <a name="return-value"></a>戻り値

### <a name="method-datasourcebyid"></a>メソッド dataSourceById

    public FormObjectSet dataSourceById(int id)

#### <a name="parameters"></a>パラメーター

id  

#### <a name="return-value"></a>戻り値

### <a name="method-datasourcecount"></a>メソッド dataSourceCount

    public int dataSourceCount()

#### <a name="return-value"></a>戻り値

### <a name="method-getactivefields"></a>メソッド getActiveFields

    public Array getActiveFields(int dataSourceId)

#### <a name="parameters"></a>パラメーター

dataSourceId  

#### <a name="return-value"></a>戻り値

### <a name="method-getchildrenbyid"></a>メソッド getChildrenById

親 ID を使用してデータ ソースの子を取得します。

    public container getChildrenById(str dataSourceName, [AnyType parentId])

#### <a name="parameters"></a>パラメーター

dataSourceName  
親 ID。

<!-- -->

parentId  
親 ID。

#### <a name="return-value"></a>戻り値

子のためのコンテナーです。

### <a name="method-getchildrenbyindex"></a>メソッド getChildrenByIndex

親インデックスを使用してデータ ソースの子を取得します。

    public container getChildrenByIndex(str dataSourceName, [int parentIndex])

#### <a name="parameters"></a>パラメーター

dataSourceName  
親インデックス。

<!-- -->

parentIndex  
親インデックス。

#### <a name="return-value"></a>戻り値

子のためのコンテナーです。

### <a name="method-getlasterror"></a>メソッド getLastError

    public DataSetError getLastError()

#### <a name="return-value"></a>戻り値

### <a name="method-getparentbyid"></a>メソッド getParentById

子 ID を使用してデータ ソースの親を取得します。

    public AnyType getParentById(str dataSourceName, AnyType childId)

#### <a name="parameters"></a>パラメーター

dataSourceName  
子 ID。

<!-- -->

childId  
子 ID。

#### <a name="return-value"></a>戻り値

親 ID。

### <a name="method-getparentbyindex"></a>メソッド getParentByIndex

子インデックスを使用してデータ ソースの親を取得します。

    public int getParentByIndex(str dataSourceName, int childIndex)

#### <a name="parameters"></a>パラメーター

dataSourceName  
子インデックス。

<!-- -->

childIndex  
子インデックス。

#### <a name="return-value"></a>戻り値

親 ID。

### <a name="method-getrowindexfromrowhierarchyid"></a>メソッド getRowIndexFromRowHierarchyId

行階層 ID を使用してデータ ソース内の行インデックスを取得します。

    public int getRowIndexFromRowHierarchyId(str dataSourceName, AnyType id)

#### <a name="parameters"></a>パラメーター

dataSourceName  
行の階層 ID。

<!-- -->

id  
行の階層 ID。

#### <a name="return-value"></a>戻り値

行インデックス。

### <a name="method-initcomplete"></a>メソッド initComplete

    public boolean initComplete()

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

    public str name()

#### <a name="return-value"></a>戻り値

### <a name="method-objectset"></a>メソッド objectSet

    public FormObjectSet objectSet([AnyType objectSet])

#### <a name="parameters"></a>パラメーター

objectSet  

#### <a name="return-value"></a>戻り値

### <a name="method-pack"></a>メソッド pack

DataSetRun クラスの現在のインスタンスをシリアル化します。

    public container pack()

#### <a name="return-value"></a>戻り値

DataSetRun クラスの現在のインスタンスを含むコンテナーです。

### <a name="method-runcalled"></a>メソッド runCalled

    public boolean runCalled()

#### <a name="return-value"></a>戻り値

### <a name="method-unpack"></a>メソッド unpack

pack パラメーター値を DataSetRun クラスのインスタンスに逆シリアル化します。

    public boolean unpack(container pack)

#### <a name="parameters"></a>パラメーター

梱包  
インスタンスを逆シリアル化するコンテナー。

#### <a name="return-value"></a>戻り値

逆シリアル化が成功した場合は true。それ以外の場合は、false。

### <a name="method-create"></a>メソッド create

    public static DataSetRun create(str name, container pack)

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

梱包  

#### <a name="return-value"></a>戻り値

### <a name="method-createruntime"></a>メソッド createRunTime

    public static DataSetRun createRunTime(container pack)

#### <a name="parameters"></a>パラメーター

梱包  

#### <a name="return-value"></a>戻り値

### <a name="method-setlasterror"></a>メソッド setLastError

    public void setLastError(DataSetError error)

#### <a name="parameters"></a>パラメーター

エラー  

### <a name="method-run"></a>メソッド run

    public void run()

### <a name="method-setlookupmode"></a>メソッド setLookupMode

データセットをルックアップ モードにします。

    public void setLookupMode()

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(xArgs args)

#### <a name="parameters"></a>パラメーター

args  

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-createrecord"></a>メソッド createRecord

新しいレコードを作成します。

    public void createRecord(str formDataSourceName, [boolean append])

#### <a name="parameters"></a>パラメーター

formDataSourceName  
追加するレコード。

<!-- -->

append  
追加するレコード。

### <a name="method-setactivefields"></a>メソッド setActiveFields

    public void setActiveFields(int dataSourceId, Array fieldIds)

#### <a name="parameters"></a>パラメーター

dataSourceId  

<!-- -->

fieldIds  

### <a name="method-setexternalcontext"></a>メソッド setExternalContext

dataSetRun オブジェクトの外部コンテキストを設定します。

    public void setExternalContext([Common externalContext])

#### <a name="parameters"></a>パラメーター

externalContext  
外部コンテキスト。

### <a name="method-init"></a>メソッド init

    public void init()

### <a name="method-enablehierarchicaldatabrowsing"></a>メソッド enableHierarchicalDataBrowsing

階層データの参照を有効にします。

    public void enableHierarchicalDataBrowsing(str hierarchyPKDataSourceName, FieldId hierarchyPKfieldId, str hierarchyFKDataSourceName, FieldId hierarchyFKfieldId)

#### <a name="parameters"></a>パラメーター

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

### <a name="method-disablehierarchicaldatabrowsing"></a>メソッド disableHierarchicalDataBrowsing

階層データの参照を無効にします。

    public void disableHierarchicalDataBrowsing(str dataSourceName)

#### <a name="parameters"></a>パラメーター

dataSourceName  
階層データの参照を無効にするデータ ソースの名前。

## <a name="class-datasourcemethodinfo"></a>クラス DataSourceMethodInfo
    class DataSourceMethodInfo extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                           | 説明                                     |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| public DisplayFunctionType displayType()                                                                         |                                                 |
| public boolean isStatic()                                                                                        |                                                 |
| public str name()                                                                                                |                                                 |
| public Types returnType()                                                                                        |                                                 |
| public int returnTypeId()                                                                                        |                                                 |
| public void new(str name, DisplayFunctionType displayType, Types returnType, int returnTypeId, boolean isStatic) | Object クラスの新しいインスタンスを初期化します。 |
| public void finalize()                                                                                           |                                                 |

### <a name="method-displaytype"></a>メソッド displayType

    public DisplayFunctionType displayType()

#### <a name="return-value"></a>戻り値

### <a name="method-isstatic"></a>メソッド isStatic

    public boolean isStatic()

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

    public str name()

#### <a name="return-value"></a>戻り値

### <a name="method-returntype"></a>メソッド returnType

    public Types returnType()

#### <a name="return-value"></a>戻り値

### <a name="method-returntypeid"></a>メソッド returnTypeId

    public int returnTypeId()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(str name, DisplayFunctionType displayType, Types returnType, int returnTypeId, boolean isStatic)

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

displayType  

<!-- -->

returnType  

<!-- -->

returnTypeId  

<!-- -->

isStatic  

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-datasourcemethodinfolist"></a>クラス DataSourceMethodInfoList
    class DataSourceMethodInfoList extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                  | 説明                                                       |
|---------------------------------------------------------|-------------------------------------------------------------------|
| public int count()                                      |                                                                   |
| public DataSourceMethodInfo getMethod(int methodNumber) |                                                                   |
| public void addMethod(DataSourceMethodInfo method)      |                                                                   |
| public void new()                                       | DataSourceMethodInfoList クラスの新しいインスタンスを初期化します。 |
| public void finalize()                                  |                                                                   |

### <a name="method-count"></a>メソッド count

    public int count()

#### <a name="return-value"></a>戻り値

### <a name="method-getmethod"></a>メソッド getMethod

    public DataSourceMethodInfo getMethod(int methodNumber)

#### <a name="parameters"></a>パラメーター

methodNumber  

#### <a name="return-value"></a>戻り値

### <a name="method-addmethod"></a>メソッド addMethod

    public void addMethod(DataSourceMethodInfo method)

#### <a name="parameters"></a>パラメーター

メソッド  

### <a name="method-new"></a>メソッド new

DataSourceMethodInfoList クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-datasourcenode"></a>クラス DataSourceNode
    class DataSourceNode extends TreeNode

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                            | 説明                                             |
|---------------------------------------------------|---------------------------------------------------------|
| public DataSourceMethodInfoList memberFunctions() |                                                         |
| public void finalize()                            |                                                         |
| private void new()                                | DataSourceNode クラスの新しいインスタンスを初期化します。 |

### <a name="method-memberfunctions"></a>メソッド memberFunctions

    public DataSourceMethodInfoList memberFunctions()

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-new"></a>メソッド new

DataSourceNode クラスの新しいインスタンスを初期化します。

    private void new()

## <a name="class-datasourceruntimemetadatachangedevtargs"></a>クラス DataSourceRuntimeMetadataChangedEvtArgs
    class DataSourceRuntimeMetadataChangedEvtArgs extends ManagedEventArgs

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                                                    | 説明                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| public str changedDataSourceName()                                                                                                        |                                                           |
| public FieldId changedFieldId()                                                                                                           |                                                           |
| public DataSourceMetadataChangeType changeType()                                                                                          |                                                           |
| public str referencedDataSourceName()                                                                                                     |                                                           |
| public void new(str changedDatasourceName, str referencedDatasourceName, FieldId changedFieldId, DataSourceMetadataChangeType changeType) | ManagedEventArgs クラスの新しいインスタンスを初期化します。 |
| public void finalize()                                                                                                                    |                                                           |

### <a name="method-changeddatasourcename"></a>メソッド changedDataSourceName

    public str changedDataSourceName()

#### <a name="return-value"></a>戻り値

### <a name="method-changedfieldid"></a>メソッド changedFieldId

    public FieldId changedFieldId()

#### <a name="return-value"></a>戻り値

### <a name="method-changetype"></a>メソッド changeType

    public DataSourceMetadataChangeType changeType()

#### <a name="return-value"></a>戻り値

### <a name="method-referenceddatasourcename"></a>メソッド referencedDataSourceName

    public str referencedDataSourceName()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

ManagedEventArgs クラスの新しいインスタンスを初期化します。

    public void new(str changedDatasourceName, str referencedDatasourceName, FieldId changedFieldId, DataSourceMetadataChangeType changeType)

#### <a name="parameters"></a>パラメーター

changedDatasourceName  

<!-- -->

referencedDatasourceName  

<!-- -->

changedFieldId  

<!-- -->

changeType  

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-datetimeutil"></a>クラス DateTimeUtil
    class DateTimeUtil extends Object

DateTimeUtil クラスは、utcdatetime および Timezone 値を変換または変更するために使用できます。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                                                                                            | 説明                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ::public static DateTime addDays(DateTime t, int value)                                                                                                                           | utcdatetime 値に指定された日数を追加します。                                                                                                      |
| ::public static DateTime addHours(DateTime t, int value)                                                                                                                          | utcdatetime 値に指定された時間数を追加します。                                                                                                     |
| ::public static DateTime addMinutes(DateTime t, int value)                                                                                                                        | utcdatetime 値に指定された分数を追加します。                                                                                                   |
| ::public static DateTime addMonths(DateTime t, int value)                                                                                                                         | utcdatetime 値に指定された月数を追加します。                                                                                                    |
| ::public static DateTime addSeconds(DateTime t, Int64 value)                                                                                                                      | utcdatetime 値に指定された秒数を追加します。                                                                                                   |
| ::public static DateTime addYears(DateTime t, int value)                                                                                                                          | utcdatetime 値に指定された年数を追加します。                                                                                                     |
| ::public static DateTime anyToDateTime(AnyType value)                                                                                                                             | 任意のオブジェクトを utcdatetime 値に変換します。                                                                                                             |
| ::public static DateTime applyTimeZoneOffset(DateTime t, Timezone tz)                                                                                                             | 指定された utcdatetime 値から、指定された Timezone 列挙値により示された量オフセットされる utcdatetime 値を取得します。 |
| ::public static str applyTimeZoneOffsetFilter(QueryFilter filter)                                                                                                                 | フィルターにタイム ゾーン オフセットを適用します。                                                                                                                    |
| ::public static str applyTimeZoneOffsetRange(QueryBuildRange range)                                                                                                               | 範囲にタイム ゾーン オフセットを適用します。                                                                                                                     |
| ::public static Date date(DateTime t)                                                                                                                                             | 指定された utcdatetime 値をデータ タイプに変換します。                                                                                                       |
| ::public static int day(DateTime t)                                                                                                                                               | utcdatetime 値によって指定されている月の日を取得します。                                                                                       |
| ::public static Timezone getClientMachineTimeZone()                                                                                                                               | クライアント コンピューターのタイム ゾーン列挙値を取得します。                                                                                                    |
| ::public static Timezone getCompanyTimeZone()                                                                                                                                     | 現在の法人に設定されているタイム ゾーンを取得します。                                                                                              |
| ::public static Int64 getDifference(DateTime t1, DateTime t2)                                                                                                                     | 2 つの指定された utcdatetime 値間の秒数を取得します。                                                                                           |
| ::public static Timezone getOriginatingTimeZone(DateTime t)                                                                                                                       | 指定した utcdatetime 値の元のタイム ゾーン列挙値を取得します。                                                                            |
| ::public static Date getSystemDate(Timezone tz)                                                                                                                                   |                                                                                                                                                                |
| ::public static DateTime getSystemDateTime()                                                                                                                                      | utcdatetime 値としての現在のシステム時刻を取得します。                                                                                                           |
| ::public static TimeOfDay getTimeNow(Timezone tz)                                                                                                                                 |                                                                                                                                                                |
| ::public static TimeZoneId getTimeZoneId(Timezone tz)                                                                                                                             |                                                                                                                                                                |
| ::public static int getTimeZoneOffset(DateTime t, Timezone tz)                                                                                                                    | タイム ゾーン列挙値の情報を使用して UTC に指定された utcdatetime 値のオフセットを取得します。                                            |
| ::public static int getTimeZoneRule(DateTime t)                                                                                                                                   | 指定した日に影響を与えるタイム ゾーン ルールを返します。                                                                                                |
| ::public static Date getToday(Timezone tz)                                                                                                                                        |                                                                                                                                                                |
| ::public static PreferredCalendar getUserPreferredCalendar()                                                                                                                      | 現在のユーザーの PreferredCalendar 列挙値を取得します。                                                                                             |
| ::public static Timezone getUserPreferredTimeZone()                                                                                                                               | 現在のユーザーの PreferredTimezone 列挙値を取得します。                                                                                             |
| ::public static int hour(DateTime t)                                                                                                                                              | utcdatetime 値によって指定されている日の時間を取得します。                                                                                        |
| ::public static DateTime maxValue()                                                                                                                                               | utcdatetime タイプの変数に許可される最大値を取得します。                                                                            |
| ::public static int minute(DateTime t)                                                                                                                                            | utcdatetime 値によって指定されている時間の分を取得します。                                                                                     |
| ::public static DateTime minValue()                                                                                                                                               | utcdatetime タイプの変数に許可される最小値を取得します。                                                                            |
| ::public static int month(DateTime t)                                                                                                                                             | utcdatetime 値によって指定されている年の月を取得します。                                                                                      |
| ::public static DateTime newDateTime(Date date, TimeOfDay time, \[Timezone tzOffsetToRemove\])                                                                                    | 指定されたデータおよび timeOfDay 値を使用して、新しい utcdatetime 値を作成します。                                                                              |
| ::public static DateTime parse(str s)                                                                                                                                             | 指定された文字列から新しい utcdatetime 値を作成します。                                                                                                     |
| ::public static container populateTimeZoneInfo(int year, Timezone tz)                                                                                                             | 開始日と終了日と時間バイアスを取得します。                                                                                                                   |
| ::public static DateTime removeTimeZoneOffset(DateTime t, Timezone tz)                                                                                                            | 指定した utcdatetime 値からタイムゾーンの列挙値によって示されるオフセットを削除します。                                                     |
| ::public static str removeTimeZoneOffsetFilter(QueryFilter filter)                                                                                                                | フィルターからタイム ゾーン オフセットを削除します。                                                                                                                  |
| ::public static str removeTimeZoneOffsetRange(QueryBuildRange range)                                                                                                              | 範囲からタイム ゾーン オフセットを削除します。                                                                                                                   |
| ::public static int second(DateTime t)                                                                                                                                            | utcdatetime 値によって指定されている分の秒を取得します。                                                                                    |
| ::public static TimeOfDay time(DateTime t)                                                                                                                                        | 指定した utcdatetime 値から timeOfDay 値として午前 0 時からの経過秒数を取得します。                                    |
| ::public static str toFormattedStr(DateTime t, int sequence, int day, int separator1, int month, int separator2, int year, int timeSeparator1, int timeSeparator2, \[int flags\]) |                                                                                                                                                                |
| ::public static str toStr(DateTime t)                                                                                                                                             | utcdatetime 値を次の形式の文字列に変換します。YYYY-MM-DDThh:mm:ss。T は文字リテラルです。                                         |
| ::public static DateTime utcNow()                                                                                                                                                 | 現在のシステム時刻を示す utcdatetime 値を取得します。                                                                                          |
| ::public static int year(DateTime t)                                                                                                                                              | utcdatetime 値によって指定されている年を取得します。                                                                                                   |
| ::public static void setSystemDateTime(DateTime t)                                                                                                                                | 指定した utcdatetime 値に、システムの日時を設定します。                                                                                       |
| ::public static void setCompanyTimeZone(Timezone tz, \[boolean persist\])                                                                                                         | 現在の会社によって使用されているタイムゾーン列挙値を設定します。                                                                                       |
| ::public static void setUserPreferredCalendar(PreferredCalendar calendar)                                                                                                         | 現在のセッションの現在のユーザーの PreferredCalendar 列挙型の値を設定します。                                                          |
| ::public static void setUserPreferredTimeZone(Timezone tz, \[boolean persist\])                                                                                                   | 指定したタイムゾーンの列挙値に、ユーザーの優先タイム ゾーンを設定します。                                                                          |
| private void new()                                                                                                                                                                | DateTimeUtil クラスの新しいインスタンスを初期化します。                                                                                                          |

### <a name="method-adddays"></a>メソッド addDays

utcdatetime 値に指定された日数を追加します。

    public static DateTime addDays(DateTime t, int value)

#### <a name="parameters"></a>パラメーター

t  
追加する日数。

<!-- -->

値  
追加する日数。

#### <a name="return-value"></a>戻り値

新しい utcdatetime 値。

#### <a name="remarks"></a>備考

値パラメーターの値が負の場合は、日数が差し引かれます。

### <a name="method-addhours"></a>メソッド addHours

utcdatetime 値に指定された時間数を追加します。

    public static DateTime addHours(DateTime t, int value)

#### <a name="parameters"></a>パラメーター

t  
追加する時間数。

<!-- -->

値  
追加する時間数。

#### <a name="return-value"></a>戻り値

新しい utcdatetime 値。

#### <a name="remarks"></a>備考

値パラメーターの値が負の場合は、時間数が差し引かれます。

### <a name="method-addminutes"></a>メソッド addMinutes

utcdatetime 値に指定された分数を追加します。

    public static DateTime addMinutes(DateTime t, int value)

#### <a name="parameters"></a>パラメーター

t  
追加する分数。

<!-- -->

値  
追加する分数。

#### <a name="return-value"></a>戻り値

新しい utcdatetime 値。

#### <a name="remarks"></a>備考

値パラメーターの値が負の場合は、分数が差し引かれます。

### <a name="method-addmonths"></a>メソッド addMonths

utcdatetime 値に指定された月数を追加します。

    public static DateTime addMonths(DateTime t, int value)

#### <a name="parameters"></a>パラメーター

t  
追加する月数。

<!-- -->

値  
追加する月数。

#### <a name="return-value"></a>戻り値

新しい utcdatetime 値。

#### <a name="remarks"></a>備考

値パラメーターの値が負の場合は、月数が差し引かれます。

### <a name="method-addseconds"></a>メソッド addSeconds

utcdatetime 値に指定された秒数を追加します。

    public static DateTime addSeconds(DateTime t, Int64 value)

#### <a name="parameters"></a>パラメーター

t  
追加する秒数。

<!-- -->

値  
追加する秒数。

#### <a name="return-value"></a>戻り値

新しい utcdatetime 値。

#### <a name="remarks"></a>備考

値パラメーターの値が負の場合は、秒数が差し引かれます。

### <a name="method-addyears"></a>メソッド addYears

utcdatetime 値に指定された年数を追加します。

    public static DateTime addYears(DateTime t, int value)

#### <a name="parameters"></a>パラメーター

t  
追加する年数。

<!-- -->

値  
追加する年数。

#### <a name="return-value"></a>戻り値

新しい utcdatetime 値。

#### <a name="remarks"></a>備考

値パラメーターの値が負の場合は、年数が差し引かれます。

### <a name="method-anytodatetime"></a>メソッド anyToDateTime

任意のオブジェクトを utcdatetime 値に変換します。

    public static DateTime anyToDateTime(AnyType value)

#### <a name="parameters"></a>パラメーター

値  
変換するオブジェクト。

#### <a name="return-value"></a>戻り値

新しい utcdatetime 値。

#### <a name="remarks"></a>備考

次の例の文字列は、この anyToDateTime メソッドが正しく変換できる日付/時刻文字列の形式を示しています ("2009-01-28T13：44：55")。 DateTimeUtil::utcNow メソッドの出力は、anyToDateTime メソッドへの有効な入力です。

### <a name="method-applytimezoneoffset"></a>メソッド applyTimeZoneOffset

指定された utcdatetime 値から、指定された Timezone 列挙値により示された量オフセットされる utcdatetime 値を取得します。

    public static DateTime applyTimeZoneOffset(DateTime t, Timezone tz)

#### <a name="parameters"></a>パラメーター

t  
使用する新しいオフセットを示すタイム ゾーン列挙値。

<!-- -->

tz  
使用する新しいオフセットを示すタイム ゾーン列挙値。

#### <a name="return-value"></a>戻り値

新しい utcdatetime 値。

### <a name="method-applytimezoneoffsetfilter"></a>メソッド applyTimeZoneOffsetFilter

フィルターにタイム ゾーン オフセットを適用します。

    public static str applyTimeZoneOffsetFilter(QueryFilter filter)

#### <a name="parameters"></a>パラメーター

フィルタ  

#### <a name="return-value"></a>戻り値

新しい日付/時間範囲の値。

### <a name="method-applytimezoneoffsetrange"></a>メソッド applyTimeZoneOffsetRange

範囲にタイム ゾーン オフセットを適用します。

    public static str applyTimeZoneOffsetRange(QueryBuildRange range)

#### <a name="parameters"></a>パラメーター

range  

#### <a name="return-value"></a>戻り値

新しい日付/時間範囲の値。

### <a name="method-date"></a>メソッド date

指定された utcdatetime 値をデータ タイプに変換します。

    public static Date date(DateTime t)

#### <a name="parameters"></a>パラメーター

t  
変換する utcdatetime 値。

#### <a name="return-value"></a>戻り値

日付の値です。

### <a name="method-day"></a>メソッド day

utcdatetime 値によって指定されている月の日を取得します。

    public static int day(DateTime t)

#### <a name="parameters"></a>パラメーター

t  
日付のコンポーネントの値を取得するための utcdatetime 値。

#### <a name="return-value"></a>戻り値

指定した utcdatetime 値の月の日。

### <a name="method-getclientmachinetimezone"></a>メソッド getClientMachineTimeZone

クライアント コンピューターのタイム ゾーン列挙値を取得します。

    public static Timezone getClientMachineTimeZone()

#### <a name="return-value"></a>戻り値

クライアント コンピューターのタイム ゾーン列挙値。

### <a name="method-getcompanytimezone"></a>メソッド getCompanyTimeZone

現在の法人に設定されているタイム ゾーンを取得します。

    public static Timezone getCompanyTimeZone()

#### <a name="return-value"></a>戻り値

現在の法人に設定されているタイム ゾーン

### <a name="method-getdifference"></a>メソッド getDifference

2 つの指定された utcdatetime 値間の秒数を取得します。

    public static Int64 getDifference(DateTime t1, DateTime t2)

#### <a name="parameters"></a>パラメーター

t1  
2 番目の utcdatetime 値。

<!-- -->

t2  
2 番目の utcdatetime 値。

#### <a name="return-value"></a>戻り値

2 つの指定された utcdatetime 値間の秒数。

### <a name="method-getoriginatingtimezone"></a>メソッド getOriginatingTimeZone

指定した utcdatetime 値の元のタイム ゾーン列挙値を取得します。

    public static Timezone getOriginatingTimeZone(DateTime t)

#### <a name="parameters"></a>パラメーター

t  
タイム ゾーンを取得するための utcdatetime 値。

#### <a name="return-value"></a>戻り値

指定した utcdatetime 値のタイム ゾーン列挙値。

### <a name="method-getsystemdate"></a>メソッド getSystemDate

    public static Date getSystemDate(Timezone tz)

#### <a name="parameters"></a>パラメーター

tz  

#### <a name="return-value"></a>戻り値

### <a name="method-getsystemdatetime"></a>メソッド getSystemDateTime

utcdatetime 値としての現在のシステム時刻を取得します。

    public static DateTime getSystemDateTime()

#### <a name="return-value"></a>戻り値

utcdatetime 値としての現在のシステム時刻。

#### <a name="remarks"></a>備考

システム時刻に固定値がない場合は、それが返されます。 それ以外の場合、現在の日付と時刻がローカル コンピューターから返されます。

### <a name="method-gettimenow"></a>メソッド getTimeNow

    public static TimeOfDay getTimeNow(Timezone tz)

#### <a name="parameters"></a>パラメーター

tz  

#### <a name="return-value"></a>戻り値

### <a name="method-gettimezoneid"></a>メソッド getTimeZoneId

    public static TimeZoneId getTimeZoneId(Timezone tz)

#### <a name="parameters"></a>パラメーター

tz  

#### <a name="return-value"></a>戻り値

### <a name="method-gettimezoneoffset"></a>メソッド getTimeZoneOffset

タイム ゾーン列挙値の情報を使用して UTC に指定された utcdatetime 値のオフセットを取得します。

    public static int getTimeZoneOffset(DateTime t, Timezone tz)

#### <a name="parameters"></a>パラメーター

t  
T パラメーターのタイム ゾーンを示すタイム ゾーン列挙値。

<!-- -->

tz  
T パラメーターのタイム ゾーンを示すタイム ゾーン列挙値。

#### <a name="return-value"></a>戻り値

UTC に指定された utcdatetime 値のオフセットを示す整数。

### <a name="method-gettimezonerule"></a>メソッド getTimeZoneRule

指定した日に影響を与えるタイム ゾーン ルールを返します。

    public static int getTimeZoneRule(DateTime t)

#### <a name="parameters"></a>パラメーター

t  

#### <a name="return-value"></a>戻り値

指定された日付のタイム ゾーン ルール。

### <a name="method-gettoday"></a>メソッド getToday

    public static Date getToday(Timezone tz)

#### <a name="parameters"></a>パラメーター

tz  

#### <a name="return-value"></a>戻り値

### <a name="method-getuserpreferredcalendar"></a>メソッド getUserPreferredCalendar

現在のユーザーの PreferredCalendar 列挙値を取得します。

    public static PreferredCalendar getUserPreferredCalendar()

#### <a name="return-value"></a>戻り値

現在のユーザーの PreferredCalendar 列挙値。

### <a name="method-getuserpreferredtimezone"></a>メソッド getUserPreferredTimeZone

現在のユーザーの PreferredTimezone 列挙値を取得します。

    public static Timezone getUserPreferredTimeZone()

#### <a name="return-value"></a>戻り値

現在のユーザーの PreferredTimezone 列挙値。

### <a name="method-hour"></a>メソッド hour

utcdatetime 値によって指定されている日の時間を取得します。

    public static int hour(DateTime t)

#### <a name="parameters"></a>パラメーター

t  
時間のコンポーネントの値を取得するための utcdatetime 値。

#### <a name="return-value"></a>戻り値

指定した utcdatetime 値の日の時間。

### <a name="method-maxvalue"></a>メソッド maxValue

utcdatetime タイプの変数に許可される最大値を取得します。

    public static DateTime maxValue()

#### <a name="return-value"></a>戻り値

utcdatetime タイプの変数に許可される最大値。

### <a name="method-minute"></a>メソッド minute

utcdatetime 値によって指定されている時間の分を取得します。

    public static int minute(DateTime t)

#### <a name="parameters"></a>パラメーター

t  
分のコンポーネントの値を取得するための utcdatetime 値。

#### <a name="return-value"></a>戻り値

指定した utcdatetime 値の時間の分。

### <a name="method-minvalue"></a>メソッド minValue

utcdatetime タイプの変数に許可される最小値を取得します。

    public static DateTime minValue()

#### <a name="return-value"></a>戻り値

utcdatetime タイプの変数に許可される最小値。

### <a name="method-month"></a>メソッド month

utcdatetime 値によって指定されている年の月を取得します。

    public static int month(DateTime t)

#### <a name="parameters"></a>パラメーター

t  
月のコンポーネントの値を取得するための utcdatetime 値。

#### <a name="return-value"></a>戻り値

指定された utcdatetime 値の年の月。

### <a name="method-newdatetime"></a>メソッド newDateTime

指定されたデータおよび timeOfDay 値を使用して、新しい utcdatetime 値を作成します。

    public static DateTime newDateTime(Date date, TimeOfDay time, [Timezone tzOffsetToRemove])

#### <a name="parameters"></a>パラメーター

日付  
新しい utcdatetime 値を作成するタイム ゾーン (オプション)。

<!-- -->

タイム  
新しい utcdatetime 値を作成するタイム ゾーン (オプション)。

<!-- -->

tzOffsetToRemove  
新しい utcdatetime 値を作成するタイム ゾーン (オプション)。

#### <a name="return-value"></a>戻り値

新しい utcdatetime 値。

#### <a name="remarks"></a>備考

TzOffsetToRemove パラメーターの値が指定されていない場合は、UTC タイム ゾーンで utcdatetime 値が作成されます。

### <a name="method-parse"></a>メソッド parse

指定された文字列から新しい utcdatetime 値を作成します。

    public static DateTime parse(str s)

#### <a name="parameters"></a>パラメーター

秒  
次の形式の文字列: yyyy-mm-ddThh:mm:ss。

#### <a name="return-value"></a>戻り値

指定した文字列からの新しい utcdatetime 値。

### <a name="method-populatetimezoneinfo"></a>メソッド populateTimeZoneInfo

開始日と終了日と時間バイアスを取得します。

    public static container populateTimeZoneInfo(int year, Timezone tz)

#### <a name="parameters"></a>パラメーター

年  
タイム ゾーン。

<!-- -->

tz  
タイム ゾーン。

#### <a name="return-value"></a>戻り値

開始日と終了日と時間バイアス。

### <a name="method-removetimezoneoffset"></a>メソッド removeTimeZoneOffset

指定した utcdatetime 値からタイムゾーンの列挙値によって示されるオフセットを削除します。

    public static DateTime removeTimeZoneOffset(DateTime t, Timezone tz)

#### <a name="parameters"></a>パラメーター

t  
削除するタイム ゾーン列挙値。

<!-- -->

tz  
削除するタイム ゾーン列挙値。

#### <a name="return-value"></a>戻り値

タイム ゾーン オフセットなしの utcdatetime 値。

### <a name="method-removetimezoneoffsetfilter"></a>メソッド removeTimeZoneOffsetFilter

フィルターからタイム ゾーン オフセットを削除します。

    public static str removeTimeZoneOffsetFilter(QueryFilter filter)

#### <a name="parameters"></a>パラメーター

フィルタ  

#### <a name="return-value"></a>戻り値

新しい日付/時間範囲の値。

### <a name="method-removetimezoneoffsetrange"></a>メソッド removeTimeZoneOffsetRange

範囲からタイム ゾーン オフセットを削除します。

    public static str removeTimeZoneOffsetRange(QueryBuildRange range)

#### <a name="parameters"></a>パラメーター

range  

#### <a name="return-value"></a>戻り値

新しい日付/時間範囲の値。

### <a name="method-second"></a>メソッド second

utcdatetime 値によって指定されている分の秒を取得します。

    public static int second(DateTime t)

#### <a name="parameters"></a>パラメーター

t  
秒のコンポーネントの値を取得するための utcdatetime 値。

#### <a name="return-value"></a>戻り値

指定された utcdatetime 値の分の秒です。

### <a name="method-time"></a>メソッド time

指定した utcdatetime 値から timeOfDay 値として午前 0 時からの経過秒数を取得します。

    public static TimeOfDay time(DateTime t)

#### <a name="parameters"></a>パラメーター

t  
時刻を取得するための utcdatetime 値。

#### <a name="return-value"></a>戻り値

午前 0 時から経過した秒数を示す timeOfDay 値。

### <a name="method-toformattedstr"></a>メソッド toFormattedStr

    public static str toFormattedStr(DateTime t, int sequence, int day, int separator1, int month, int separator2, int year, int timeSeparator1, int timeSeparator2, [int flags])

#### <a name="parameters"></a>パラメーター

t  

<!-- -->

順序  

<!-- -->

日  

<!-- -->

separator1  

<!-- -->

月  

<!-- -->

separator2  

<!-- -->

年  

<!-- -->

timeSeparator1  

<!-- -->

timeSeparator2  

<!-- -->

flags  

#### <a name="return-value"></a>戻り値

### <a name="method-tostr"></a>メソッド toStr

utcdatetime 値を次の形式の文字列に変換します。YYYY-MM-DDThh:mm:ss。T は文字リテラルです。

    public static str toStr(DateTime t)

#### <a name="parameters"></a>パラメーター

t  
変換する utcdatetime 値。

#### <a name="return-value"></a>戻り値

指定された utcdatetime 値の文字列表現。

### <a name="method-utcnow"></a>メソッド utcNow

現在のシステム時刻を示す utcdatetime 値を取得します。

    public static DateTime utcNow()

#### <a name="return-value"></a>戻り値

utcdatetime 値としての現在のシステム時刻。

#### <a name="remarks"></a>備考

このメソッドはサーバー上で実行されるため、返される時刻はサーバーのシステム時刻です。

### <a name="method-year"></a>メソッド year

utcdatetime 値によって指定されている年を取得します。

    public static int year(DateTime t)

#### <a name="parameters"></a>パラメーター

t  
年のコンポーネントの値を取得するための utcdatetime 値。

#### <a name="return-value"></a>戻り値

指定された utcdatetime 値の年。

### <a name="method-setsystemdatetime"></a>メソッド setSystemDateTime

指定した utcdatetime 値に、システムの日時を設定します。

    public static void setSystemDateTime(DateTime t)

#### <a name="parameters"></a>パラメーター

t  
システム日時を設定する utcdatetime 値。

### <a name="method-setcompanytimezone"></a>メソッド setCompanyTimeZone

現在の会社によって使用されているタイムゾーン列挙値を設定します。

    public static void setCompanyTimeZone(Timezone tz, [boolean persist])

#### <a name="parameters"></a>パラメーター

tz  
新しい値を保持する必要があるかどうかを示すブール値。

<!-- -->

persist  
新しい値を保持する必要があるかどうかを示すブール値。

### <a name="method-setuserpreferredcalendar"></a>メソッド setUserPreferredCalendar

現在のセッションの現在のユーザーの PreferredCalendar 列挙型の値を設定します。

    public static void setUserPreferredCalendar(PreferredCalendar calendar)

#### <a name="parameters"></a>パラメーター

カレンダー  
設定する PreferredCalendar 列挙値。

### <a name="method-setuserpreferredtimezone"></a>メソッド setUserPreferredTimeZone

指定したタイムゾーンの列挙値に、ユーザーの優先タイム ゾーンを設定します。

    public static void setUserPreferredTimeZone(Timezone tz, [boolean persist])

#### <a name="parameters"></a>パラメーター

tz  
新しい値を保持する必要があるかどうかを示すブール値。

<!-- -->

persist  
新しい値を保持する必要があるかどうかを示すブール値。

### <a name="method-new"></a>メソッド new

DateTimeUtil クラスの新しいインスタンスを初期化します。

    private void new()

## <a name="class-dialogbox"></a>クラス ダイアログ ボックス
    class DialogBox extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                               | 説明                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| public DialogButton retval()                                                                         |                                                 |
| public void new(DialogBoxType type, str text, str title, str bottomtext, DialogButton defaultButton) | Object クラスの新しいインスタンスを初期化します。 |
| public void finalize()                                                                               |                                                 |

### <a name="method-retval"></a>メソッド retval

    public DialogButton retval()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(DialogBoxType type, str text, str title, str bottomtext, DialogButton defaultButton)

#### <a name="parameters"></a>パラメーター

タイプ  

<!-- -->

テキスト  

<!-- -->

title  

<!-- -->

bottomtext  

<!-- -->

defaultButton  

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-dictclass"></a>クラス DictClass
    class DictClass extends Object

DictClass クラスは、クラスに関する情報を提供します。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                            | 説明                                                                                                                                   |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public AnyType callObject(str methodName, Object Called, VarArg ) | オブジェクトのメソッドを呼び出します。                                                                                                                  |
| public AnyType callStatic(str methodName, VarArg )                | 静的メソッドを呼び出します。                                                                                                                        |
| public ClassId extend()                                           | 指定されたクラスが拡張されるクラスの ID を提供します。                                                                                 |
| public List extendedBy(\[boolean allLevels\])                     | 指定されたクラスを拡張するクラスのリスト オブジェクトを提供します。                                                                         |
| public Array getAllAttributes()                                   | クラスの属性の完全なセットを取得します。                                                                                           |
| public Object getAttribute(str attribute)                         | クラス ヘッダー メタデータから最初に一致する属性を取得し、その属性を表すオブジェクト クラスのインスタンスを作成し、返します。 |
| public Array getAttributes(str attribute)                         |                                                                                                                                               |
| public ClassId id()                                               | 指定されたクラスの ID を提供します。                                                                                                        |
| public ClassId implements(int no)                                 | クラスが実装する指定されたインターフェイスの ID を示します。                                                                            |
| public int implementsCnt()                                        | クラスが実装するインターフェイスの数を示します。                                                                                   |
| public boolean isAbstract()                                       | クラスが抽象であるかどうかを示します。                                                                                                        |
| public boolean isFinal()                                          | クラスが最終であるかどうかを示します。                                                                                                           |
| public boolean isInterface()                                      | オブジェクトがインターフェイスであるかどうかを示します。                                                                                                  |
| public boolean isKernel()                                         | クラスがカーネル クラスであるかどうかを示します。                                                                                                  |
| public boolean isRunable()                                        | クラスを実行できるかどうかを示します。                                                                                                         |
| public Object makeObject(VarArg )                                 | オブジェクトを作成します。                                                                                                                            |
| public str name()                                                 | クラスの名前を提供します。                                                                                                                 |
| public str objectMethod(int methodNumber)                         | クラスの指定されたインスタンス メソッドの名前を提供します。                                                                                  |
| public int objectMethodCnt()                                      | クラスのインスタンス メソッドの数を示します。                                                                                          |
| public DictMethod objectMethodObject(int methodNumber)            | DictMethod オブジェクトを返すことで、クラス内の指定されたインスタンス メソッドに関する情報を提供します。                                           |
| public ClassRunMode RunMode()                                     | クラスが実行される場所を指定します。                                                                                                          |
| public str staticMethod(int methodNumber)                         | クラスの指定された静的メソッドの名前を提供します。                                                                                    |
| public int staticMethodCnt()                                      | クラスの静的メソッドの数を示します。                                                                                            |
| public DictMethod staticMethodObject(int methodNumber)            | DictMethod オブジェクトを返すことで、クラス内の指定された静的メソッドに関する情報を提供します。                                             |
| ::public static Array getAttributedClasses(str attribute)         |                                                                                                                                               |
| ::public static Object createObject(str className, VarArg )       |                                                                                                                                               |
| public void new(ClassId classId)                                  | Object クラスの新しいインスタンスを初期化します。                                                                                               |

### <a name="method-callobject"></a>メソッド callObject

オブジェクトのメソッドを呼び出します。

    public AnyType callObject(str methodName, Object Called, VarArg )

#### <a name="parameters"></a>パラメーター

methodName  

<!-- -->

呼び出された  

<!-- -->



#### <a name="return-value"></a>戻り値

指定されたメソッドによって返される anytype データ型値です。

#### <a name="remarks"></a>備考

callObject メソッドに渡すメソッドを含むクラスを使用して、DictClass オブジェクトのインスタンスを作成する必要があります。 攻撃者が callObject メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権を持っていることを確認します。

#### <a name="examples"></a>例

この例では、このクラスのグローバル インスタンスの名前が infolog である Info クラスの toString インスタンス メソッドを呼び出し、呼び出しから返された値を出力します。

    static void Job_Example_DictClass_CallObject(Args _args) 
    { 
        DictClass dictClass; 
        anytype   retVal; 
        str      resultOutput; 
        ExecutePermission perm; 
        perm = new ExecutePermission(); 
        // Grants permission to execute the DictClass.callObject method. 
        // DictClass.callObject runs under code access security. 
        perm.assert(); 
        dictClass = new DictClass(classidget(infolog)); 
        if (dictClass != null) 
        { 
            retVal       = dictClass.callObject("toString", infolog); 
            resultOutput = strfmt("Return value is %1", retVal); 
            print resultOutput; 
            pause; 
        } 
        // Closes the code access permission scope. 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-callstatic"></a>メソッド callStatic

静的メソッドを呼び出します。

    public AnyType callStatic(str methodName, VarArg )

#### <a name="parameters"></a>パラメーター

methodName  

<!-- -->



#### <a name="return-value"></a>戻り値

指定されたメソッドによって返される anytype データ型値です。

#### <a name="remarks"></a>備考

callStatic メソッドに渡されるメソッドを含むクラスを使用して、DictClass クラスのオブジェクトのインスタンスを作成する必要があります。 攻撃者が callStatic メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権を持っていることを確認します。

#### <a name="examples"></a>例

この例では、Session クラスの AOSClientMode メソッドを呼び出し、呼び出しから返された値を出力します。

    static void Job_Example_DictClass_CallStatic(Args _args) 
    { 
        DictClass dictClass; 
        anytype   retVal; 
        str       resultOutput; 
        ExecutePermission perm; 
        perm = new ExecutePermission(); 
        // Grants permission to execute the DictClass.callStatic method. 
        // DictClass.callStatic runs under code access security. 
        perm.assert(); 
        dictClass = new DictClass(classnum(Session)); 
        if (dictClass != null) 
        { 
            retVal       = dictClass.callStatic("AOSClientMode"); 
            resultOutput = strfmt( 
                "Return value of AOSClientMode is %1",  
                retVal); 
            print resultOutput; 
            pause; 
        } 
        // Closes the code access permission scope. 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-extend"></a>メソッド extend

指定されたクラスが拡張されるクラスの ID を提供します。

    public ClassId extend()

#### <a name="return-value"></a>戻り値

クラス ID を示す classID システムデータ型の値、クラスが別のクラスを拡張していない場合は 0。

### <a name="method-extendedby"></a>メソッド extendedBy

指定されたクラスを拡張するクラスのリスト オブジェクトを提供します。

    public List extendedBy([boolean allLevels])

#### <a name="parameters"></a>パラメーター

allLevels  

#### <a name="return-value"></a>戻り値

クラスを拡張するクラスのリスト オブジェクト。

### <a name="method-getallattributes"></a>メソッド getAllAttributes

クラスの属性の完全なセットを取得します。

    public Array getAllAttributes()

#### <a name="return-value"></a>戻り値

クラスの SysAttribute オブジェクトの配列。

### <a name="method-getattribute"></a>メソッド getAttribute

クラス ヘッダー メタデータから最初に一致する属性を取得し、その属性を表すオブジェクト クラスのインスタンスを作成し、返します。

    public Object getAttribute(str attribute)

#### <a name="parameters"></a>パラメーター

属性  
検索の対象である属性。

#### <a name="return-value"></a>戻り値

オブジェクト クラスのインスタンスとしての属性。

### <a name="method-getattributes"></a>メソッド getAttributes

    public Array getAttributes(str attribute)

#### <a name="parameters"></a>パラメーター

属性  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

指定されたクラスの ID を提供します。

    public ClassId id()

#### <a name="return-value"></a>戻り値

クラス ID を示す classId システムデータ型の値。

### <a name="method-implements"></a>メソッド implements

クラスが実装する指定されたインターフェイスの ID を示します。

    public ClassId implements(int no)

#### <a name="parameters"></a>パラメーター

no  
クラス宣言内のインターフェイスの順序に基づいて、インターフェイスを指定する整数データ型。

#### <a name="return-value"></a>戻り値

クラス ID を示す classID システムデータ型の値。

### <a name="method-implementscnt"></a>メソッド implementsCnt

クラスが実装するインターフェイスの数を示します。

    public int implementsCnt()

#### <a name="return-value"></a>戻り値

クラスが実装するインターフェイスの数の整数データ型値。

### <a name="method-isabstract"></a>メソッド isAbstract

クラスが抽象であるかどうかを示します。

    public boolean isAbstract()

#### <a name="return-value"></a>戻り値

クラスが抽象である場合は true。それ以外の場合は、false。

### <a name="method-isfinal"></a>メソッド isFinal

クラスが最終であるかどうかを示します。

    public boolean isFinal()

#### <a name="return-value"></a>戻り値

クラスが最終である場合は true。それ以外の場合は、false。

### <a name="method-isinterface"></a>メソッド isInterface

オブジェクトがインターフェイスであるかどうかを示します。

    public boolean isInterface()

#### <a name="return-value"></a>戻り値

オブジェクトがインターフェイスである場合は true。それ以外の場合は、false。

### <a name="method-iskernel"></a>メソッド isKernel

クラスがカーネル クラスであるかどうかを示します。

    public boolean isKernel()

#### <a name="return-value"></a>戻り値

クラスがカーネル クラスの場合は true。それ以外の場合は、false。

### <a name="method-isrunable"></a>メソッド isRunable

クラスを実行できるかどうかを示します。

    public boolean isRunable()

#### <a name="return-value"></a>戻り値

クラスを実行することができる場合は true。それ以外の場合は、false。

### <a name="method-makeobject"></a>メソッド makeObject

オブジェクトを作成します。

    public Object makeObject(VarArg )

#### <a name="parameters"></a>パラメーター



#### <a name="return-value"></a>戻り値

オブジェクト クラスのインスタンス。

#### <a name="remarks"></a>備考

オブジェクト クラスのインスタンスを DictClass::callObject メソッドに渡すことができます。

### <a name="method-name"></a>メソッド名

クラスの名前を提供します。

    public str name()

#### <a name="return-value"></a>戻り値

クラス名の文字列データ型の値。

### <a name="method-objectmethod"></a>メソッド objectMethod

クラスの指定されたインスタンス メソッドの名前を提供します。

    public str objectMethod(int methodNumber)

#### <a name="parameters"></a>パラメーター

methodNumber  
メソッドの順序に基づいて、クラス内のメソッドを指定する整数データ型。

#### <a name="return-value"></a>戻り値

メソッド名の文字列データ型の値。

#### <a name="remarks"></a>備考

\_methodNumber パラメーターは 1 から始まります。

### <a name="method-objectmethodcnt"></a>メソッド objectMethodCnt

クラスのインスタンス メソッドの数を示します。

    public int objectMethodCnt()

#### <a name="return-value"></a>戻り値

クラス内のインスタンス メソッドの数を示す整数値。

### <a name="method-objectmethodobject"></a>メソッド objectMethodObject

DictMethod オブジェクトを返すことで、クラス内の指定されたインスタンス メソッドに関する情報を提供します。

    public DictMethod objectMethodObject(int methodNumber)

#### <a name="parameters"></a>パラメーター

methodNumber  
メソッドの順序に基づいて、クラス内のメソッドを指定する整数データ型。 番号付けは 1 から開始します。

#### <a name="return-value"></a>戻り値

クラス内の指定されたメソッドに関する情報を含む DictMethod オブジェクト。

#### <a name="remarks"></a>備考

\_methodNumber パラメーターは 1 から始まります。

### <a name="method-runmode"></a>メソッド RunMode

クラスが実行される場所を指定します。

    public ClassRunMode RunMode()

#### <a name="return-value"></a>戻り値

クラスが実行される場所を示す ClassRunMode システム列挙値。

#### <a name="remarks"></a>備考

可能な戻り値は次のとおりです。

-   呼び出された値。
-   Client 値。
-   ClientorServer 値。
-   サーバーの値。

### <a name="method-staticmethod"></a>メソッド staticMethod

クラスの指定された静的メソッドの名前を提供します。

    public str staticMethod(int methodNumber)

#### <a name="parameters"></a>パラメーター

methodNumber  
メソッドの順序に基づいて、クラス内のメソッドを指定する整数データ型。

#### <a name="return-value"></a>戻り値

メソッド名の文字列データ型の値。

#### <a name="remarks"></a>備考

\_methodNumber パラメーターは 1 から始まります。

### <a name="method-staticmethodcnt"></a>メソッド staticMethodCnt

クラスの静的メソッドの数を示します。

    public int staticMethodCnt()

#### <a name="return-value"></a>戻り値

クラスの静的メソッドの数を示す整数。

### <a name="method-staticmethodobject"></a>メソッド staticMethodObject

DictMethod オブジェクトを返すことで、クラス内の指定された静的メソッドに関する情報を提供します。

    public DictMethod staticMethodObject(int methodNumber)

#### <a name="parameters"></a>パラメーター

methodNumber  
メソッドの順序に基づいて、クラス内のメソッドを指定する整数データ型。

#### <a name="return-value"></a>戻り値

クラス内の指定されたメソッドに関する情報を含む DictMethod オブジェクト。

#### <a name="remarks"></a>備考

\_methodNumber パラメーターは 1 から始まります。

### <a name="method-getattributedclasses"></a>メソッド getAttributedClasses

    public static Array getAttributedClasses(str attribute)

#### <a name="parameters"></a>パラメーター

属性  

#### <a name="return-value"></a>戻り値

### <a name="method-createobject"></a>メソッド createObject

    public static Object createObject(str className, VarArg )

#### <a name="parameters"></a>パラメーター

className  

<!-- -->



#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(ClassId classId)

#### <a name="parameters"></a>パラメーター

classId  
クラスのシステム ID を示す classId システムデータ型の値。

#### <a name="remarks"></a>備考

クラス ID は符号なし整数なので、常に 0 から 65535 の範囲です。 無効なクラス ID が渡された場合は、このメソッドは失敗しません。 ClassNum 組み込み関数を使用して、クラス ID の代わりにクラス名をメソッドに渡すことができます。 この機能の詳細については、「組み込み関数」を参照してください。

## <a name="class-dictcompositechilddataentity"></a>クラス DictCompositeChildDataEntity
    class DictCompositeChildDataEntity extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                           | 説明 |
|------------------------------------------------------------------|-------------|
| public int level()                                               |             |
| public str name()                                                |             |
| public str dataEntity()                                          |             |
| public str relation()                                            |             |
| public str tags()                                                |             |
| public DictCompositeChildDataEntity parent()                     |             |
| public void new(str compositeDataEntityName, str dataEntityName) |             |

### <a name="method-level"></a>メソッド level

    public int level()

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

    public str name()

#### <a name="return-value"></a>戻り値

### <a name="method-dataentity"></a>メソッド dataEntity

    public str dataEntity()

#### <a name="return-value"></a>戻り値

### <a name="method-relation"></a>メソッド relation

    public str relation()

#### <a name="return-value"></a>戻り値

### <a name="method-tags"></a>メソッド tags

    public str tags()

#### <a name="return-value"></a>戻り値

### <a name="method-parent"></a>メソッド parent

    public DictCompositeChildDataEntity parent()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

    public void new(str compositeDataEntityName, str dataEntityName)

#### <a name="parameters"></a>パラメーター

compositeDataEntityName  

<!-- -->

dataEntityName  

## <a name="class-dictcompositedataentity"></a>クラス DictCompositeDataEntity
    class DictCompositeDataEntity extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                       | 説明 |
|--------------------------------------------------------------|-------------|
| ::public static List listOfCompositeDataEntities()           |             |
| public str label()                                           |             |
| public boolean isReadOnly()                                  |             |
| public str modules()                                         |             |
| public str configurationKey()                                |             |
| public str countryRegionCodes()                              |             |
| public str countryRegionContextField()                       |             |
| public str developerDocumentation()                          |             |
| public EntityCategory entityCategory()                       |             |
| public str formRef()                                         |             |
| public str singularLabel()                                   |             |
| public str tags()                                            |             |
| public str publicCollectionName()                            |             |
| public str publicEntityName()                                |             |
| public int dataEntityCount()                                 |             |
| public DictCompositeChildDataEntity childDataEntityNo(int n) |             |
| public void new(str compositeDataEntityName)                 |             |

### <a name="method-listofcompositedataentities"></a>メソッド listOfCompositeDataEntities

    public static List listOfCompositeDataEntities()

#### <a name="return-value"></a>戻り値

### <a name="method-label"></a>メソッド label

    public str label()

#### <a name="return-value"></a>戻り値

### <a name="method-isreadonly"></a>メソッド isReadOnly

    public boolean isReadOnly()

#### <a name="return-value"></a>戻り値

### <a name="method-modules"></a>メソッド modules

    public str modules()

#### <a name="return-value"></a>戻り値

### <a name="method-configurationkey"></a>メソッド configurationKey

    public str configurationKey()

#### <a name="return-value"></a>戻り値

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes()

#### <a name="return-value"></a>戻り値

### <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

    public str countryRegionContextField()

#### <a name="return-value"></a>戻り値

### <a name="method-developerdocumentation"></a>メソッド developerDocumentation

    public str developerDocumentation()

#### <a name="return-value"></a>戻り値

### <a name="method-entitycategory"></a>メソッド entityCategory

    public EntityCategory entityCategory()

#### <a name="return-value"></a>戻り値

### <a name="method-formref"></a>メソッド formRef

    public str formRef()

#### <a name="return-value"></a>戻り値

### <a name="method-singularlabel"></a>メソッド singularLabel

    public str singularLabel()

#### <a name="return-value"></a>戻り値

### <a name="method-tags"></a>メソッド tags

    public str tags()

#### <a name="return-value"></a>戻り値

### <a name="method-publiccollectionname"></a>メソッド publicCollectionName

    public str publicCollectionName()

#### <a name="return-value"></a>戻り値

### <a name="method-publicentityname"></a>メソッド publicEntityName

    public str publicEntityName()

#### <a name="return-value"></a>戻り値

### <a name="method-dataentitycount"></a>メソッド dataEntityCount

    public int dataEntityCount()

#### <a name="return-value"></a>戻り値

### <a name="method-childdataentityno"></a>メソッド childDataEntityNo

    public DictCompositeChildDataEntity childDataEntityNo(int n)

#### <a name="parameters"></a>パラメーター

n  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

    public void new(str compositeDataEntityName)

#### <a name="parameters"></a>パラメーター

compositeDataEntityName  

## <a name="class-dictconfigurationkey"></a>クラス DictConfigurationKey
    class DictConfigurationKey extends Object

DictConfigurationKey クラスは、コンフィギュレーション キーの情報を提供します。

### <a name="remarks"></a>備考

DictConfigurationKey クラスを使用する例については、新しいメソッドを参照してください。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                     | 説明                                                               |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------|
| public boolean enabled()                                                   | 構成キーが有効かどうかを示す値を返します。  |
| public ConfigurationKeyId id()                                             | コンフィギュレーション キーの ID を返します。                                  |
| public str label()                                                         | コンフィギュレーション キーのラベルを返します。                                |
| public str labelId()                                                       |                                                                           |
| public LicenseCodeId licenseCode()                                         | コンフィギュレーション キーのライセンス コード ID を返します。                    |
| public str name()                                                          | コンフィギュレーション キーの名前を返します。                                |
| public ConfigurationKeyId parentConfigurationKeyId()                       | コンフィギュレーション キーの親コンフィギュレーション キーの ID を返します。 |
| ::public static boolean enabledById(ConfigurationKeyId configurationKeyId) |                                                                           |
| public boolean permanentlyDisabled()                                       |                                                                           |
| public void new(ConfigurationKeyId configurationKeyId)                     | Object クラスの新しいインスタンスを初期化します。                           |

### <a name="method-enabled"></a>メソッド enabled

構成キーが有効かどうかを示す値を返します。

    public boolean enabled()

#### <a name="return-value"></a>戻り値

コンフィギュレーション キーが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

このメソッドを使用する例については、新しいメソッドを参照してください。

### <a name="method-id"></a>メソッド id

コンフィギュレーション キーの ID を返します。

    public ConfigurationKeyId id()

#### <a name="return-value"></a>戻り値

コンフィギュレーション キーの ID。

### <a name="method-label"></a>メソッド label

コンフィギュレーション キーのラベルを返します。

    public str label()

#### <a name="return-value"></a>戻り値

コンフィギュレーション キーのラベル。コンフィギュレーション キーにラベル値がない場合は空の文字列。

### <a name="method-labelid"></a>メソッド labelId

    public str labelId()

#### <a name="return-value"></a>戻り値

### <a name="method-licensecode"></a>メソッド licenseCode

コンフィギュレーション キーのライセンス コード ID を返します。

    public LicenseCodeId licenseCode()

#### <a name="return-value"></a>戻り値

コンフィギュレーション キーのライセンス コード ID。コンフィギュレーション キーにライセンス コードがない場合は 0 (ゼロ)。

### <a name="method-name"></a>メソッド名

コンフィギュレーション キーの名前を返します。

    public str name()

#### <a name="return-value"></a>戻り値

コンフィギュレーション キーの名前。

#### <a name="remarks"></a>備考

このメソッドを使用する例については、新しいメソッドを参照してください。

### <a name="method-parentconfigurationkeyid"></a>メソッド parentConfigurationKeyId

コンフィギュレーション キーの親コンフィギュレーション キーの ID を返します。

    public ConfigurationKeyId parentConfigurationKeyId()

#### <a name="return-value"></a>戻り値

親コンフィギュレーション キーの ID。コンフィギュレーション キーに親コンフィギュレーション キーがない場合は 0 (ゼロ)。

### <a name="method-enabledbyid"></a>メソッド enabledById

    public static boolean enabledById(ConfigurationKeyId configurationKeyId)

#### <a name="parameters"></a>パラメーター

configurationKeyId  

#### <a name="return-value"></a>戻り値

### <a name="method-permanentlydisabled"></a>メソッド permanentlyDisabled

    public boolean permanentlyDisabled()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(ConfigurationKeyId configurationKeyId)

#### <a name="parameters"></a>パラメーター

configurationKeyId  
DictConfigurationKey クラスのインスタンスを作成するために使用されるコンフィギュレーション キーの ID。

#### <a name="examples"></a>例

次の例は、コンフィギュレーション キーの列挙中に DictConfigurationKey クラスの新しいインスタンスを作成する方法を示しています。

    ConfigurationKeySet configKeySet; 
    DictConfigurationKey dictConfigKey; 
    str strOutput; 
    int i; 
    configKeySet = new ConfigurationKeySet(); 
    configKeySet.loadSystemSetup(); 
    // Output the configuration key names and their enable state. 
    for (i=1; i <= configKeySet.cnt(); i++) 
    { 
        dictConfigKey = new DictConfigurationKey(configKeySet.cnt2Id(i)); 
        strOutput = dictConfigKey.enabled() ? "enabled" : "disabled"; 
        strOutput += " " + dictConfigKey.name(); 
        print strOutput; 
    }

## <a name="class-dictdataentity"></a>クラス DictDataEntity
    class DictDataEntity extends DictView

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

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

### <a name="method-isaggregatedataentity"></a>メソッド isAggregateDataEntity

    public boolean isAggregateDataEntity()

#### <a name="return-value"></a>戻り値

### <a name="method-isreadonly"></a>メソッド isReadOnly

    public boolean isReadOnly()

#### <a name="return-value"></a>戻り値

### <a name="method-primarycompanycontext"></a>メソッド primaryCompanyContext

    public str primaryCompanyContext()

#### <a name="return-value"></a>戻り値

### <a name="method-primarykey"></a>メソッド primaryKey

    public str primaryKey()

#### <a name="return-value"></a>戻り値

### <a name="method-supportssetbasedsqloperations"></a>メソッド supportsSetBasedSqlOperations

    public boolean supportsSetBasedSqlOperations()

#### <a name="return-value"></a>戻り値

### <a name="method-enablesetbasedsqloperations"></a>メソッド enableSetBasedSqlOperations

    public AutoNo enableSetBasedSqlOperations()

#### <a name="return-value"></a>戻り値

### <a name="method-modules"></a>メソッド modules

    public str modules()

#### <a name="return-value"></a>戻り値

### <a name="method-entitycategory"></a>メソッド entityCategory

    public EntityCategory entityCategory()

#### <a name="return-value"></a>戻り値

### <a name="method-datamanagementenabled"></a>メソッド dataManagementEnabled

    public boolean dataManagementEnabled()

#### <a name="return-value"></a>戻り値

### <a name="method-datamanagementstagingtable"></a>メソッド dataManagementStagingTable

    public str dataManagementStagingTable()

#### <a name="return-value"></a>戻り値

### <a name="method-publiccollectionname"></a>メソッド publicCollectionName

    public str publicCollectionName()

#### <a name="return-value"></a>戻り値

### <a name="method-publicentityname"></a>メソッド publicEntityName

    public str publicEntityName()

#### <a name="return-value"></a>戻り値

### <a name="method-datasourceisreadonly"></a>メソッド dataSourceIsReadOnly

    public boolean dataSourceIsReadOnly(str dataSourceName)

#### <a name="parameters"></a>パラメーター

dataSourceName  

#### <a name="return-value"></a>戻り値

### <a name="method-datasourceid2name"></a>メソッド dataSourceID2Name

    public str dataSourceID2Name(int dataSourceId)

#### <a name="parameters"></a>パラメーター

dataSourceId  

#### <a name="return-value"></a>戻り値

### <a name="method-hasextensionfields"></a>メソッド hasExtensionFields

    public boolean hasExtensionFields()

#### <a name="return-value"></a>戻り値

### <a name="method-getextensionfieldnames"></a>メソッド getExtensionFieldNames

    public List getExtensionFieldNames()

#### <a name="return-value"></a>戻り値

### <a name="method-listofdataentities"></a>メソッド listOfDataEntities

    public static List listOfDataEntities()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

    public void new(TableId tableId)

#### <a name="parameters"></a>パラメーター

tableId  

## <a name="class-dictdataentityfield"></a>クラス DictDataEntityField
    class DictDataEntityField extends DictField

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                | 説明 |
|-----------------------------------------------------------------------|-------------|
| public FieldAccessModifier accessModifier()                           |             |
| public str dataEntityViewMethod()                                     |             |
| public str dataField()                                                |             |
| public str dataSource()                                               |             |
| public str dimensionLegalEntityContextField()                         |             |
| public str dynamicDimensionEnumerationField()                         |             |
| public boolean IsComputedField()                                      |             |
| public void new(TableId tableId, FieldId fieldId, \[int arrayIndex\]) |             |

### <a name="method-accessmodifier"></a>メソッド accessModifier

    public FieldAccessModifier accessModifier()

#### <a name="return-value"></a>戻り値

### <a name="method-dataentityviewmethod"></a>メソッド dataEntityViewMethod

    public str dataEntityViewMethod()

#### <a name="return-value"></a>戻り値

### <a name="method-datafield"></a>メソッド dataField

    public str dataField()

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

    public str dataSource()

#### <a name="return-value"></a>戻り値

### <a name="method-dimensionlegalentitycontextfield"></a>メソッド dimensionLegalEntityContextField

    public str dimensionLegalEntityContextField()

#### <a name="return-value"></a>戻り値

### <a name="method-dynamicdimensionenumerationfield"></a>メソッド dynamicDimensionEnumerationField

    public str dynamicDimensionEnumerationField()

#### <a name="return-value"></a>戻り値

### <a name="method-iscomputedfield"></a>メソッド IsComputedField

    public boolean IsComputedField()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

    public void new(TableId tableId, FieldId fieldId, [int arrayIndex])

#### <a name="parameters"></a>パラメーター

tableId  

<!-- -->

fieldId  

<!-- -->

arrayIndex  

## <a name="class-dictenum"></a>クラス DictEnum
    class DictEnum extends Object

DictEnum クラスは、Finance and Operations アプリケーション オブジェクト ツリー (AOT) で基本列挙の列挙値に関するメタ情報を取得します。

### <a name="remarks"></a>備考

下位互換性については、プロパティに変換される、またはプロパティから変換されるメソッドの特別な名前付け規則が使用されます。


|                 |                                |                          |
|-----------------|--------------------------------|--------------------------|
|      氏名       |            ReqDate             | 記号 (文字列として型設定) |
|      ラベル      | @SYS18075 (「要求日」) |      名前またはラベル       |
|   FeatureKey    |         ReqSchedAction         |        FeatureKey        |
|    EnumValue    |               0                |          先頭値           |
| AOT の位置 |       最初 (インデックス = 0)        |          指数           |

この例では、ActionBasicDateType 基本列挙から取得されます。 列挙に関する一般情報については、開発者ガイドを参照してください。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                            | 説明                                                                                                               |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| public ConfigurationKeyId configurationKeyId()                    | 列挙値のコンフィギュレーション キー ID を返します。                                                                     |
| public int displayLength(\[boolean useLongestLabel\])             |                                                                                                                           |
| public container getCountryRegionCodes()                          |                                                                                                                           |
| public str help(\[boolean useInterfaceLanguage\])                 | この列挙型のヘルプ テキストを取得します。                                                                             |
| public str helpDefined()                                          | この列挙型に対する help プロパティの値を返します。                                                              |
| public EnumId id()                                                | 列挙値の列挙 ID を返します。                                                                            |
| public ConfigurationKeyId index2ConfigurationKey(int index)       |                                                                                                                           |
| public container index2CountryRegionCodes(int index)              |                                                                                                                           |
| public str index2Label(int index)                                 | インデックスにより指定される列挙項目のラベルを返します。                                                  |
| public str index2LabelId(int index)                               |                                                                                                                           |
| public str index2Name(int index)                                  | インデックスにより指定される列挙項目のラベルを返します。                                                  |
| public str index2Symbol(int index)                                | インデックスにより指定される列挙項目のシンボルまたは名前を返します。                                         |
| public int index2Value(int index)                                 | インデックスにより指定される列挙項目の値を返します。                                                  |
| public str label()                                                | 列挙値のラベル テキストを返します。                                                                                |
| public str labelDefined()                                         | この列挙型に対する label プロパティの値を返します。                                                             |
| public str name()                                                 | 列挙型の名前を返します。                                                                                      |
| public int name2Value(str name)                                   | ラベルにより参照される項目の列挙値を返します。                                                |
| public boolean showAsRadio()                                      | 列挙をコンボ ボックスではなくラジオ ボタンを使用して表示するかどうかを示す値を返します。 |
| public int symbol2Value(str name)                                 | シンボルまたは名前により参照される項目の列挙値を返します。                                              |
| public ConfigurationKeyId value2ConfigurationKey(int value)       | 指定した列挙値のコンフィギュレーション キー ID を返します。                                                        |
| public container value2CountryRegionCodes(int value)              |                                                                                                                           |
| public str value2Label(int value)                                 | 指定された列挙値のラベルを返します。                                                                       |
| public str value2Name(int value)                                  | 指定された列挙値の名前を返します。                                                                        |
| public str value2Symbol(int value)                                | 記号、または指定した列挙値の Name プロパティの値を返します。                                  |
| public int values()                                               | 列挙型内の項目の数を返します。                                                                           |
| ::public static str queryFilterNames2Values(QueryFilter filter)   |                                                                                                                           |
| ::public static str queryFilterValues2Names(QueryFilter filter)   |                                                                                                                           |
| ::public static str queryRangeNames2Values(QueryBuildRange range) |                                                                                                                           |
| ::public static str queryRangeValues2Names(QueryBuildRange range) |                                                                                                                           |
| ::public static int value2id(AnyType value)                       | 指定された値の列挙 ID を返します。                                                                          |
| public void new(EnumId typeId)                                    | Object クラスの新しいインスタンスを初期化します。                                                                           |

### <a name="method-configurationkeyid"></a>メソッド configurationKeyId

列挙値のコンフィギュレーション キー ID を返します。

    public ConfigurationKeyId configurationKeyId()

#### <a name="return-value"></a>戻り値

列挙のコンフィギュレーション キー ID がない場合の列挙のコンフィギュレーション キー ID は 0 (ゼロ)。

#### <a name="examples"></a>例

次の例は、列挙型のコンフィギュレーション キー ID の取得を示しています。

    DictEnum de; 
    int      i; 
    de = new DictEnum(enumName2Id("ActionType")); 
    print int2str(de.configurationKeyId());

### <a name="method-displaylength"></a>メソッド displayLength

    public int displayLength([boolean useLongestLabel])

#### <a name="parameters"></a>パラメーター

useLongestLabel  

#### <a name="return-value"></a>戻り値

### <a name="method-getcountryregioncodes"></a>メソッド getCountryRegionCodes

    public container getCountryRegionCodes()

#### <a name="return-value"></a>戻り値

### <a name="method-help"></a>メソッド help

この列挙型のヘルプ テキストを取得します。

    public str help([boolean useInterfaceLanguage])

#### <a name="parameters"></a>パラメーター

useInterfaceLanguage  

#### <a name="return-value"></a>戻り値

ヘルプ テキストを含む文字列、ヘルプ テキストが定義されていない場合、空の文字列。

#### <a name="remarks"></a>備考

ヘルプ テキストは、基本列挙のヘルプ プロパティで定義されます。

### <a name="method-helpdefined"></a>メソッド helpDefined

この列挙型に対する help プロパティの値を返します。

    public str helpDefined()

#### <a name="return-value"></a>戻り値

この列挙型に対する help プロパティの値。

### <a name="method-id"></a>メソッド id

列挙値の列挙 ID を返します。

    public EnumId id()

#### <a name="return-value"></a>戻り値

この列挙の列挙 ID。

### <a name="method-index2configurationkey"></a>メソッド index2ConfigurationKey

    public ConfigurationKeyId index2ConfigurationKey(int index)

#### <a name="parameters"></a>パラメーター

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-index2countryregioncodes"></a>メソッド index2CountryRegionCodes

    public container index2CountryRegionCodes(int index)

#### <a name="parameters"></a>パラメーター

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-index2label"></a>メソッド index2Label

インデックスにより指定される列挙項目のラベルを返します。

    public str index2Label(int index)

#### <a name="parameters"></a>パラメーター

指数  
AOT の列挙体の 0 から始まるインデックス。

#### <a name="return-value"></a>戻り値

インデックスで指定された列挙項目のラベル。インデックスが有効な列挙項目を参照しない場合は空の文字列。

#### <a name="examples"></a>例

次の例は、列挙型内の項目のラベルの取得を示しています。

    DictEnum de; 
    int      i; 
    de = new DictEnum(enumName2Id("ActionType")); 
    for (i=0; i < de.values(); i++) 
    { 
        print int2str(i) + ", " + de.index2Label(i); 
    }

### <a name="method-index2labelid"></a>メソッド index2LabelId

    public str index2LabelId(int index)

#### <a name="parameters"></a>パラメーター

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-index2name"></a>メソッド index2Name

インデックスにより指定される列挙項目のラベルを返します。

    public str index2Name(int index)

#### <a name="parameters"></a>パラメーター

指数  
AOT の列挙体の 0 から始まるインデックス。

#### <a name="return-value"></a>戻り値

インデックスで指定された列挙項目のラベル。インデックスが有効な列挙項目を参照しない場合は空の文字列。

#### <a name="remarks"></a>備考

Finance and Operations の以前のバージョンとの下位互換性については、DictEnum::value2Name での「名前」は、列挙項目のラベル プロパティを表します。 コードを読みやすくするには、DictEnum :: value2Name メソッドの代わりに DictEnum :: value2Label メソッドを使用します。 AOT に示すように、列挙型項目の name プロパティの値を取得するには、DictEnum :: value2Symbol メソッドを使用します。

#### <a name="examples"></a>例

次の例は、列挙型内の項目のラベルの取得を示しています。

    DictEnum de; 
    int      i; 
    de = new DictEnum(enumName2Id("ActionType")); 
    for (i=0; i < de.values(); i++) 
    { 
        print int2str(i) + ", " + de.index2Name(i); 
    }

### <a name="method-index2symbol"></a>メソッド index2Symbol

インデックスにより指定される列挙項目のシンボルまたは名前を返します。

    public str index2Symbol(int index)

#### <a name="parameters"></a>パラメーター

指数  
AOT の列挙体の 0 から始まるインデックス。

#### <a name="return-value"></a>戻り値

インデックスで指定される列挙型項目のシンボル。インデックスが有効な列挙型項目を参照しない場合は空の文字列。

#### <a name="remarks"></a>備考

シンボルは、AOT の列挙型項目の Name プロパティに対応します。

#### <a name="examples"></a>例

次の例は、列挙型内の項目の記号の取得を示しています。

    DictEnum de; 
    int      i; 
    de = new DictEnum(enumName2Id("ActionType")); 
    for (i=0; i < de.values(); i++) 
    { 
        print int2str(i) + ", " + de.index2Symbol(i); 
    }

### <a name="method-index2value"></a>メソッド index2Value

インデックスにより指定される列挙項目の値を返します。

    public int index2Value(int index)

#### <a name="parameters"></a>パラメーター

指数  
AOT の列挙体の 0 から始まるインデックス。

#### <a name="return-value"></a>戻り値

インデックスで指定される列挙項目の値。

#### <a name="examples"></a>例

次の例は、列挙型内の項目の値の取得を示しています。

    DictEnum de; 
    int      i; 
    de = new DictEnum(enumName2Id("ActionType")); 
    for (i=0; i < de.values(); i++) 
    { 
        print int2str(i) + ", " + int2str(de.index2Value(i)); 
    }

### <a name="method-label"></a>メソッド label

列挙値のラベル テキストを返します。

    public str label()

#### <a name="return-value"></a>戻り値

列挙型の名前。列挙の型ラベルがない場合は、空の文字列。

### <a name="method-labeldefined"></a>メソッド labelDefined

この列挙型に対する label プロパティの値を返します。

    public str labelDefined()

#### <a name="return-value"></a>戻り値

この列挙型に対する label プロパティの値。

### <a name="method-name"></a>メソッド名

列挙型の名前を返します。

    public str name()

#### <a name="return-value"></a>戻り値

列挙型の名前。

### <a name="method-name2value"></a>メソッド name2Value

ラベルにより参照される項目の列挙値を返します。

    public int name2Value(str name)

#### <a name="parameters"></a>パラメーター

名前  
列挙値が取得されている列挙型のラベル。

#### <a name="return-value"></a>戻り値

名前の列挙値。名前が有効な列挙ラベルでない場合は 255 です。

#### <a name="remarks"></a>備考

Finance and Operations の以前のバージョンとの下位互換性については、名前はラベルを表します。 ラべルが無い列挙型の品目は、DictEnum::name2Value メソッドを使用して見つけることができません。

### <a name="method-showasradio"></a>メソッド showAsRadio

列挙をコンボ ボックスではなくラジオ ボタンを使用して表示するかどうかを示す値を返します。

    public boolean showAsRadio()

#### <a name="return-value"></a>戻り値

列挙スタイルがオプション ボタンである場合は true。それ以外の場合は、false。

### <a name="method-symbol2value"></a>メソッド symbol2Value

シンボルまたは名前により参照される項目の列挙値を返します。

    public int symbol2Value(str name)

#### <a name="parameters"></a>パラメーター

名前  
列挙値が取得されている列挙体のシンボルまたは名前。

#### <a name="return-value"></a>戻り値

名前の列挙値。名前が有効な列挙でない場合は 255 です。

### <a name="method-value2configurationkey"></a>メソッド value2ConfigurationKey

指定した列挙値のコンフィギュレーション キー ID を返します。

    public ConfigurationKeyId value2ConfigurationKey(int value)

#### <a name="parameters"></a>パラメーター

値  
コンフィギュレーション キーが取得されている列挙型の整数値。

#### <a name="return-value"></a>戻り値

値のコンフィギュレーション キーがない場合または値が有効な列挙出ない場合の値のコンフィギュレーション キー ID は 0 (ゼロ)。

### <a name="method-value2countryregioncodes"></a>メソッド value2CountryRegionCodes

    public container value2CountryRegionCodes(int value)

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-value2label"></a>メソッド value2Label

指定された列挙値のラベルを返します。

    public str value2Label(int value)

#### <a name="parameters"></a>パラメーター

値  
ラベルが取得されている列挙型の整数値。

#### <a name="return-value"></a>戻り値

値のラベル。値または値のラベルがない場合は空の文字列は有効な列挙型ではありません。

#### <a name="remarks"></a>備考

列挙型の品目は、ラベルを挿入する必要がありません。 このメソッドを使用して、値が列挙に存在するかどうかを判断はできません。 列挙型に値が存在するかどうかを確認するには、DictEnum::value2Symbol メソッドを使用します。

### <a name="method-value2name"></a>メソッド value2Name

指定された列挙値の名前を返します。

    public str value2Name(int value)

#### <a name="parameters"></a>パラメーター

値  
ラベルが取得されている列挙型の整数値。

#### <a name="return-value"></a>戻り値

値の名前。値または値の名前がない場合は空の文字列は有効な列挙型ではありません。

#### <a name="remarks"></a>備考

列挙型に値が存在するかどうかを確認するには、代わりに value2Symbol メソッドを使用します。 列挙項目にラベルを付ける必要はないため、value2Name メソッドを使用して値が列挙型にあるかどうかを判断することはできません。

### <a name="method-value2symbol"></a>メソッド value2Symbol

記号、または指定した列挙値の Name プロパティの値を返します。

    public str value2Symbol(int value)

#### <a name="parameters"></a>パラメーター

値  
記号が取得されている列挙型の整数値。

#### <a name="return-value"></a>戻り値

値のシンボルまたは名前。値が有効な列挙体でない場合は空の文字列。

#### <a name="remarks"></a>備考

列挙型の値には、記号が必要です。 このメソッドを使用すると、戻り値が空の文字列かどうかを調べることによって、列挙値が存在するかどうかを判断できます。

### <a name="method-values"></a>メソッド values

列挙型内の項目の数を返します。

    public int values()

#### <a name="return-value"></a>戻り値

列挙型内の項目の数。

#### <a name="remarks"></a>備考

値は一意でなければならないので、値の数は品目の数と同じです。

#### <a name="examples"></a>例

次の例は、列挙内の項目の数を取得し、その値をループ内で使用する方法を示しています。

    DictEnum de; 
    int      i; 
    de = new DictEnum(enumName2Id("ActionType")); 
    for (i=0; i < de.values(); i++) 
    { 
        print int2str(i) + ", " + de.index2Name(i); 
    }

### <a name="method-queryfilternames2values"></a>メソッド queryFilterNames2Values

    public static str queryFilterNames2Values(QueryFilter filter)

#### <a name="parameters"></a>パラメーター

フィルタ  

#### <a name="return-value"></a>戻り値

### <a name="method-queryfiltervalues2names"></a>メソッド queryFilterValues2Names

    public static str queryFilterValues2Names(QueryFilter filter)

#### <a name="parameters"></a>パラメーター

フィルタ  

#### <a name="return-value"></a>戻り値

### <a name="method-queryrangenames2values"></a>メソッド queryRangeNames2Values

    public static str queryRangeNames2Values(QueryBuildRange range)

#### <a name="parameters"></a>パラメーター

range  

#### <a name="return-value"></a>戻り値

### <a name="method-queryrangevalues2names"></a>メソッド queryRangeValues2Names

    public static str queryRangeValues2Names(QueryBuildRange range)

#### <a name="parameters"></a>パラメーター

range  

#### <a name="return-value"></a>戻り値

### <a name="method-value2id"></a>メソッド value2id

指定された値の列挙 ID を返します。

    public static int value2id(AnyType value)

#### <a name="parameters"></a>パラメーター

値  
列挙 ID が照会されている値。 value パラメーターは、任意のタイプを指定できます。

#### <a name="return-value"></a>戻り値

値が列挙の場合は値の列挙型 ID。それ以外の場合は 0 (ゼロ) です。

#### <a name="remarks"></a>備考

value パラメーターは、任意のタイプを指定できます。

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(EnumId typeId)

#### <a name="parameters"></a>パラメーター

typeId  
列挙の ID。

#### <a name="remarks"></a>備考

無効な enum ID を指定した場合は、コンストラクターは失敗しません。 ただし、DictEnum インスタンスを使用すると、実行時エラーが発生します。 EnumID 値は符号なし整数なので、常に 0 ～ 65535 の範囲であることに注意してください。

#### <a name="examples"></a>例

次の例では、DictEnum クラスのインスタンスを作成します。

    DictEnum de; 
    de = new DictEnum(enumName2Id("ActionType"));

## <a name="class-dictfield"></a>クラス DictField
    class DictField extends Object

DictField クラスは、指定されたテーブルで指定したフィールドに関する情報を提供します。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

次の例は、フィールドが必須かどうかを判断するために DictField クラスのインスタンスを作成する方法を示しています。

    #macrolib.dictfield 
    DictField df; 
    int       nFlags; 
    df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
    if (df) 
    { 
        nFlags = df.flags(); 
        if (bitTest(nFlags,#DBF_MANDATORY)) 
        { 
            print ("The field is mandatory."); 
        } 
        else 
        { 
            print ("The field is not mandatory."); 
        } 
    }

### <a name="methods"></a>メソッド

| 方法                                                                                                                | 説明                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public FieldId aliasFor()                                                                                             | フィールドが別のフィールドのエイリアスの場合は、エイリアス フィールドの ID を返します。                                                            |
| public Alignment alignment()                                                                                          |                                                                                                                                           |
| public boolean allowEdit()                                                                                            |                                                                                                                                           |
| public boolean allowEditOnCreate()                                                                                    |                                                                                                                                           |
| public boolean aosAuthorization()                                                                                     |                                                                                                                                           |
| public int arrayIndex()                                                                                               |                                                                                                                                           |
| public int arraySize()                                                                                                | フィールドの配列サイズを返します (つまり、基になる拡張データ型の配列サイズ)。                               |
| public Types baseType()                                                                                               | 文字列、実数、整数、日付、時刻、列挙、またはコンテナーなど、フィールドの基本型を返します。                                        |
| public ConfigurationKeyId configurationKeyId()                                                                        | フィールドのコンフィギュレーション キーの ID を返します。                                                                                    |
| public str dateTimeTimeZoneRuleFieldName(\[int arrayindex\])                                                          |                                                                                                                                           |
| public int displayHeight(\[boolean useDefaults\])                                                                     |                                                                                                                                           |
| public int displayLength(\[boolean useDefaults\])                                                                     |                                                                                                                                           |
| public EnumId enumId()                                                                                                | フィールドが列挙型に基づいている場合は列挙型の ID を返します。                                                                |
| public int flags(\[str ext\], \[Common record\])                                                                      | フィールドのプロパティを定義する整数を返します。 DBF\_MANDATORY、などのフラグ値は、DictField マクロで定義されています。 |
| public container getCountryRegionCodes()                                                                              |                                                                                                                                           |
| public FieldId getCountryRegionContextField()                                                                         |                                                                                                                                           |
| public str getPrimaryTableForSurrogateField()                                                                         |                                                                                                                                           |
| public str groupPrompt()                                                                                              | フィールドの groupPrompt 値を返します。                                                                                              |
| public str groupPromptDefined()                                                                                       | フィールドの groupPrompt プロパティの値を返します。                                                                              |
| public str help(\[int arrayIndex\], \[boolean useInterfaceLanguage\])                                                 | フィールドについて表示されるヘルプ テキストを返します。                                                                                    |
| public str helpDefined()                                                                                              | フィールドの help プロパティの値を返します。                                                                                     |
| public FieldId id()                                                                                                   | フィールドの ID を返します。                                                                                                              |
| public boolean isIgnoreEDTRelation()                                                                                  |                                                                                                                                           |
| public boolean isMonocased()                                                                                          | フィールドが monocase であるデータベースが必要とするかどうかを示す値を返します。                                                  |
| public boolean isSql()                                                                                                | フィールドが SQL データベースにあるかどうかを示す値を返します。                                                                  |
| public boolean isSurrogateForeignKey()                                                                                |                                                                                                                                           |
| public boolean isSystem()                                                                                             | フィールドがシステム フィールドかどうかを示す値を返します。                                                                       |
| public str label(\[int arrayIndex\])                                                                                  | フィールドのラベルを返します。                                                                                                          |
| public str labelDefined()                                                                                             | フィールドの label プロパティの値を返します。                                                                                    |
| public boolean mandatory()                                                                                            |                                                                                                                                           |
| public str name(\[DbBackend db\], \[int arrayindex\], \[FieldNameGenerationMode generationMode\], \[str tableAlias\]) | フィールドの名前を返します。                                                                                                            |
| public Guid origin()                                                                                                  |                                                                                                                                           |
| public str qualifiedLabel(\[int arrayIndex\])                                                                         |                                                                                                                                           |
| public str relatedTableName()                                                                                         |                                                                                                                                           |
| public str relationContext()                                                                                          |                                                                                                                                           |
| public DictRelation relationObject(\[int arrayIndex\])                                                                | フィールドが関係のある拡張データ型に基づいている場合、フィールドの DictRelation オブジェクトを返します。                           |
| public AccessType rights(\[boolean ignoreContext\])                                                                   | このフィールドに指定されている、現在のユーザーのアクセス権を返します。                                                          |
| public int stringLen()                                                                                                | フィールドの基本型が文字列の場合、フィールドの文字列サイズを返します。                                                           |
| public TableId tableid()                                                                                              | フィールドを含むテーブルの ID を返します。                                                                                      |
| public Types type()                                                                                                   | フィールドのデータ型を返します。                                                                                                       |
| public ExtendedTypeId typeId()                                                                                        | このフィールドが拡張データ型に基づいている場合は、拡張データ型の ID を返します。                                                  |
| public boolean visible()                                                                                              |                                                                                                                                           |
| public void setLookupMode(boolean lookupMode)                                                                         |                                                                                                                                           |
| public void setSFKAutoAuthorizationMode(boolean sfkMode)                                                              |                                                                                                                                           |
| public void new(TableId tableId, FieldId fieldId, \[int arrayIndex\])                                                 | Object クラスの新しいインスタンスを初期化します。                                                                                           |

### <a name="method-aliasfor"></a>メソッド aliasFor

フィールドが別のフィールドのエイリアスの場合は、エイリアス フィールドの ID を返します。

    public FieldId aliasFor()

#### <a name="return-value"></a>戻り値

フィールドのエイリアス フィールドの ID。フィールドが別のフィールドのエイリアスでない場合は 0 (ゼロ)。

#### <a name="remarks"></a>備考

ユーザーがデータをフィールドに入力すると、そのテーブルの validateField メソッドが呼び出されます。 validateField メソッドが値に対する参照を実行することができない場合、エイリアスが存在するかどうかを確認します。 エイリアス フィールドが存在する場合、validateField メソッドでは、エイリアス フィールドで検索を実行します。

#### <a name="examples"></a>例

次の例は、フィールドのエイリアス フィールドの取得を示しています。

    DictField df; 
    fieldId   fId; 
    df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum));
    if (df) 
    { 
        fId = df.aliasFor(); 
        if (0 != fId) 
        { 
            print (strfmt("Field alias: %1", fieldid2name(tablenum(CustTable), fId))); 
        } 
    }

### <a name="method-alignment"></a>メソッド alignment

    public Alignment alignment()

#### <a name="return-value"></a>戻り値

### <a name="method-allowedit"></a>メソッド allowEdit

    public boolean allowEdit()

#### <a name="return-value"></a>戻り値

### <a name="method-alloweditoncreate"></a>メソッド allowEditOnCreate

    public boolean allowEditOnCreate()

#### <a name="return-value"></a>戻り値

### <a name="method-aosauthorization"></a>メソッド aosAuthorization

    public boolean aosAuthorization()

#### <a name="return-value"></a>戻り値

### <a name="method-arrayindex"></a>メソッド arrayIndex

    public int arrayIndex()

#### <a name="return-value"></a>戻り値

### <a name="method-arraysize"></a>メソッド arraySize

フィールドの配列サイズを返します (つまり、基になる拡張データ型の配列サイズ)。

    public int arraySize()

#### <a name="return-value"></a>戻り値

フィールドの配列サイズ。このフィールドが配列ではない場合は 1 です。

#### <a name="examples"></a>例

次の例は、フィールドの配列サイズの取得を示しています。

    DictField df; 
    Types     t; 
    df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum));  
    if (df) 
    { 
        print strfmt("The arraySize is %1.", df.arraySize()); 
    }

### <a name="method-basetype"></a>メソッド baseType

文字列、実数、整数、日付、時刻、列挙、またはコンテナーなど、フィールドの基本型を返します。

    public Types baseType()

#### <a name="return-value"></a>戻り値

フィールドのタイプを指定するタイプ値。

#### <a name="examples"></a>例

次の例は、フィールドの基準タイプの取得を示しています。

    DictField df;
    df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
    if (df)
    {
        print strfmt("The field type is %1.", df.baseType());
    }

### <a name="method-configurationkeyid"></a>メソッド configurationKeyId

フィールドのコンフィギュレーション キーの ID を返します。

    public ConfigurationKeyId configurationKeyId()

#### <a name="return-value"></a>戻り値

フィールドのコンフィギュレーション キーの ID。フィールドのコンフィギュレーション キーがない場合は 0 (ゼロ)。

#### <a name="examples"></a>例

次の例は、フィールドのコンフィギュレーション キー ID とコンフィギュレーション キー名の取得を示しています。

    DictField df; 
    configurationKeyId cki; 
    DictConfigurationKey dck; 
    df = new DictField(tablenum(BankAccountTable), fieldnum(BankAccountTable, CustPaymFeePost)); 
    if (df) 
    { 
        cki = df.configurationKeyId(); 
        //    print df.helpDefined(); 
        if (0 != cki) 
        { 
            dck = new DictConfigurationKey(cki); 
            if (dck) 
            print strfmt("The configuration key is %1.", dck.name()); 
        } 
        else 
        { 
            print "No configuration key"; 
        } 
    }

### <a name="method-datetimetimezonerulefieldname"></a>メソッド dateTimeTimeZoneRuleFieldName

    public str dateTimeTimeZoneRuleFieldName([int arrayindex])

#### <a name="parameters"></a>パラメーター

arrayindex  

#### <a name="return-value"></a>戻り値

### <a name="method-displayheight"></a>メソッド displayHeight

    public int displayHeight([boolean useDefaults])

#### <a name="parameters"></a>パラメーター

useDefaults  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylength"></a>メソッド displayLength

    public int displayLength([boolean useDefaults])

#### <a name="parameters"></a>パラメーター

useDefaults  

#### <a name="return-value"></a>戻り値

### <a name="method-enumid"></a>メソッド enumId

フィールドが列挙型に基づいている場合は列挙型の ID を返します。

    public EnumId enumId()

#### <a name="return-value"></a>戻り値

フィールドが列挙型に基づいている場合は列挙型 ID。それ以外の場合は 0 (ゼロ) です。

#### <a name="examples"></a>例

次の例は、列挙型 ID と列挙型に基づくフィールドの列挙型名の取得を示しています。

    DictField df; 
    DictEnum  de; 
    enumId    id; 
    df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
    if (df) 
    { 
        id = df.enumId(); 
        if (0 != id) 
        { 
            de = new DictEnum(id); 
            if (de) 
            { 
                print de.name(); 
            } 
        } 
    }

### <a name="method-flags"></a>メソッド flags

フィールドのプロパティを定義する整数を返します。 DBF\_MANDATORY、などのフラグ値は、DictField マクロで定義されています。

    public int flags([str ext], [Common record])

#### <a name="parameters"></a>パラメーター

ext  

<!-- -->

記録  

#### <a name="return-value"></a>戻り値

各ビットが、フィールド フラグに対応している整数値。

#### <a name="remarks"></a>備考

Global::bitTest メソッドまたは & 演算子を使用して、個々のフラグ値を確認します。

#### <a name="examples"></a>例

次の例は、フィールドが必須かどうかを判断するためにフィールドのフラグを取得する方法を示しています。

    #macrolib.dictfield 
    DictField df; 
    int       nFlags; 
    df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
    if (df) 
    { 
        nFlags = df.flags(); 
        if (bitTest(nFlags,#DBF_MANDATORY)) 
        { 
            print ("The field is mandatory."); 
        } 
        else 
        { 
            print ("The field is not mandatory."); 
        } 
    }

### <a name="method-getcountryregioncodes"></a>メソッド getCountryRegionCodes

    public container getCountryRegionCodes()

#### <a name="return-value"></a>戻り値

### <a name="method-getcountryregioncontextfield"></a>メソッド getCountryRegionContextField

    public FieldId getCountryRegionContextField()

#### <a name="return-value"></a>戻り値

### <a name="method-getprimarytableforsurrogatefield"></a>メソッド getPrimaryTableForSurrogateField

    public str getPrimaryTableForSurrogateField()

#### <a name="return-value"></a>戻り値

### <a name="method-groupprompt"></a>メソッド groupPrompt

フィールドの groupPrompt 値を返します。

    public str groupPrompt()

#### <a name="return-value"></a>戻り値

フィールドの groupPrompt 値。

### <a name="method-grouppromptdefined"></a>メソッド groupPromptDefined

フィールドの groupPrompt プロパティの値を返します。

    public str groupPromptDefined()

#### <a name="return-value"></a>戻り値

テーブルに対する groupPrompt プロパティの値。

### <a name="method-help"></a>メソッド help

フィールドについて表示されるヘルプ テキストを返します。

    public str help([int arrayIndex], [boolean useInterfaceLanguage])

#### <a name="parameters"></a>パラメーター

arrayIndex  
ヘルプ テキストにユーザー インターフェイス言語を使用するかどうかを示すブール値; オプション。

<!-- -->

useInterfaceLanguage  
ヘルプ テキストにユーザー インターフェイス言語を使用するかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

ヘルプ テキストまたはフィールドの継承されたヘルプ テキスト。

#### <a name="remarks"></a>備考

フィールドのヘルプ テキストが定義されていない場合、該当する場合に、このメソッドはフィールドに使用される、拡張データ型のヘルプ テキストを返します。 配列のエントリが指定されている場合、このメソッドは、配列要素のヘルプ テキストを返します。

#### <a name="examples"></a>例

次の例は、フィールドのヘルプ テキストの取得を示しています。

    DictField df; 
    df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
    if (df) 
    { 
        print df.help(); 
    }

### <a name="method-helpdefined"></a>メソッド helpDefined

フィールドの help プロパティの値を返します。

    public str helpDefined()

#### <a name="return-value"></a>戻り値

フィールドに対する help プロパティの値。

#### <a name="remarks"></a>備考

ヘルプ メソッドとは異なり、フィールドが拡張データ型に基づいていて、ヘルプ テキストが定義されていない場合、helpDefined メソッドは拡張データ型のヘルプ テキストを返しません。

#### <a name="examples"></a>例

次の例は、フィールドの定義済ヘルプ テキストの取得を示しています。

    DictField df; 
    df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
    if (df) 
    { 
        print df.helpDefined(); 
    }

### <a name="method-id"></a>メソッド id

フィールドの ID を返します。

    public FieldId id()

#### <a name="return-value"></a>戻り値

フィールドの ID。

#### <a name="examples"></a>例

次の例では、フィールドの ID を取得します。

    DictField df; 
    df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
    if (df) 
    { 
        print df.id(); 
    }

### <a name="method-isignoreedtrelation"></a>メソッド isIgnoreEDTRelation

    public boolean isIgnoreEDTRelation()

#### <a name="return-value"></a>戻り値

### <a name="method-ismonocased"></a>メソッド isMonocased

フィールドが monocase であるデータベースが必要とするかどうかを示す値を返します。

    public boolean isMonocased()

#### <a name="return-value"></a>戻り値

フィールドが monocase である場合は true。それ以外の場合は、false。

### <a name="method-issql"></a>メソッド isSql

フィールドが SQL データベースにあるかどうかを示す値を返します。

    public boolean isSql()

#### <a name="return-value"></a>戻り値

フィールドが SQL データベースである場合は true。それ以外の場合は、false。

#### <a name="examples"></a>例

次の例では、フィールドが SQL データベースにあるかどうかを判断します。

        DictField df; 
        df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
        if (df) 
        { 
        if (df.isSql()) 
        { 
            print ("Field is in SQL database"); 
        } 
        else 
        { 
            print ("Field is not in SQL database"); 
        } 
        }

### <a name="method-issurrogateforeignkey"></a>メソッド isSurrogateForeignKey

    public boolean isSurrogateForeignKey()

#### <a name="return-value"></a>戻り値

### <a name="method-issystem"></a>メソッド isSystem

フィールドがシステム フィールドかどうかを示す値を返します。

    public boolean isSystem()

#### <a name="return-value"></a>戻り値

フィールドがシステム フィールドである場合は true。それ以外の場合は、false。

### <a name="method-label"></a>メソッド label

フィールドのラベルを返します。

    public str label([int arrayIndex])

#### <a name="parameters"></a>パラメーター

arrayIndex  

#### <a name="return-value"></a>戻り値

フィールドのラベルまたは継承されたラベル値。

#### <a name="remarks"></a>備考

フィールドのラベルが指定されていない場合、該当する場合に、このメソッドはフィールドに使用される、拡張データ型のラベルを返します。 配列のエントリが指定されている場合、このメソッドは、配列要素のラベルを返します。

### <a name="method-labeldefined"></a>メソッド labelDefined

フィールドの label プロパティの値を返します。

    public str labelDefined()

#### <a name="return-value"></a>戻り値

テーブルの label プロパティの値。テーブルのラベル テキストがない場合は空の文字列。

#### <a name="remarks"></a>備考

label メソッドとは異なり、フィールドが拡張データ型に基づいていて、ラベルが定義されていない場合、labelDefined メソッドは拡張データ型のラベルを返しません。

#### <a name="examples"></a>例

次の例は、フィールドの定義済ラベルの取得を示しています。

    DictField df; 
    df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
    if (df) 
    { 
        print df.labelDefined(); 
    }

### <a name="method-mandatory"></a>メソッド mandatory

    public boolean mandatory()

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フィールドの名前を返します。

    public str name([DbBackend db], [int arrayindex], [FieldNameGenerationMode generationMode], [str tableAlias])

#### <a name="parameters"></a>パラメーター

db  
テーブルのエイリアス (省略可能)。

<!-- -->

arrayindex  
テーブルのエイリアス (省略可能)。

<!-- -->

generationMode  
テーブルのエイリアス (省略可能)。

<!-- -->

tableAlias  
テーブルのエイリアス (省略可能)。

#### <a name="return-value"></a>戻り値

フィールドの名前。

#### <a name="examples"></a>例

次の例は、フィールドの名前の取得を示しています。

    DictField df; 
    df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
    if (df) 
    { 
        print df.name(); 
    }

### <a name="method-origin"></a>メソッド origin

    public Guid origin()

#### <a name="return-value"></a>戻り値

### <a name="method-qualifiedlabel"></a>メソッド qualifiedLabel

    public str qualifiedLabel([int arrayIndex])

#### <a name="parameters"></a>パラメーター

arrayIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-relatedtablename"></a>メソッド relatedTableName

    public str relatedTableName()

#### <a name="return-value"></a>戻り値

### <a name="method-relationcontext"></a>メソッド relationContext

    public str relationContext()

#### <a name="return-value"></a>戻り値

### <a name="method-relationobject"></a>メソッド relationObject

フィールドが関係のある拡張データ型に基づいている場合、フィールドの DictRelation オブジェクトを返します。

    public DictRelation relationObject([int arrayIndex])

#### <a name="parameters"></a>パラメーター

arrayIndex  

#### <a name="return-value"></a>戻り値

フィールドの関係を表す DictRelation オブジェクト; null、Nothing、nullptr、unit、フィールドに関係が定義されていない場合、またはフィールドが拡張データ型に基づいていない場合は null 参照 (Visual Basic にはなし)。

### <a name="method-rights"></a>メソッド rights

このフィールドに指定されている、現在のユーザーのアクセス権を返します。

    public AccessType rights([boolean ignoreContext])

#### <a name="parameters"></a>パラメーター

ignoreContext  

#### <a name="return-value"></a>戻り値

このフィールドに指定されている、現在のユーザーのアクセス権。

#### <a name="remarks"></a>備考

これは、AccessType 列挙型の値の 1 つです。

### <a name="method-stringlen"></a>メソッド stringLen

フィールドの基本型が文字列の場合、フィールドの文字列サイズを返します。

    public int stringLen()

#### <a name="return-value"></a>戻り値

フィールドの基本型が文字列の場合、フィールドの文字列サイズ。それ以外の場合は 0 (ゼロ) です。

#### <a name="examples"></a>例

次の例は、フィールドの文字列の長さを取得する方法を示しています。

    DictField df; 
    df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
    if (df) 
    { 
        print strfmt("The string length is %1.", df.stringLen()); 
    }

### <a name="method-tableid"></a>メソッド tableid

フィールドを含むテーブルの ID を返します。

    public TableId tableid()

#### <a name="return-value"></a>戻り値

フィールドを含むテーブルの ID。

#### <a name="examples"></a>例

次の例は、フィールドのテーブル ID の取得を示しています。

    DictField df; 
    df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
    if (df) 
    { 
        print df.tableid(); 
    }

### <a name="method-type"></a>メソッドのタイプ

フィールドのデータ型を返します。

    public Types type()

#### <a name="return-value"></a>戻り値

フィールドのタイプを指定するタイプ値。

#### <a name="remarks"></a>備考

このフィールドが拡張データ型に基づいている場合は、このメソッドの戻り値として Types::UserType が返されます。

#### <a name="examples"></a>例

次の例は、フィールドのタイプの取得を示しています。

    DictField df; 
    df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
    if (df) 
    { 
        print df.type(); 
    }

### <a name="method-typeid"></a>メソッド typeId

このフィールドが拡張データ型に基づいている場合は、拡張データ型の ID を返します。

    public ExtendedTypeId typeId()

#### <a name="return-value"></a>戻り値

フィールドが拡張データ型に基づいている場合は、拡張データ型の ID。それ以外の場合は 0 (ゼロ)。

#### <a name="examples"></a>例

次の例は、フィールドの拡張データ型 ID の取得を示しています。

    DictField df; 
    extendedTypeId eti; 
    DictType  dt; 
    df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
    if (df) 
    { 
       eti = df.typeId(); 
       if (0 != eti) 
       { 
            dt = new DictType(eti); 
            if (dt) 
            { 
                print strfmt("The field is based on %1.", dt.name()); 
            } 
       } 
       else 
       { 
            print "The field is not based on an extended data type."; 
       } 
    }

### <a name="method-visible"></a>メソッド visible

    public boolean visible()

#### <a name="return-value"></a>戻り値

### <a name="method-setlookupmode"></a>メソッド setLookupMode

    public void setLookupMode(boolean lookupMode)

#### <a name="parameters"></a>パラメーター

lookupMode  

### <a name="method-setsfkautoauthorizationmode"></a>メソッド setSFKAutoAuthorizationMode

    public void setSFKAutoAuthorizationMode(boolean sfkMode)

#### <a name="parameters"></a>パラメーター

sfkMode  

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(TableId tableId, FieldId fieldId, [int arrayIndex])

#### <a name="parameters"></a>パラメーター

tableId  

<!-- -->

fieldId  

<!-- -->

arrayIndex  

#### <a name="examples"></a>例

次の例は、DictField クラスのインスタンスを作成する方法を示しています。

    DictField df; 
    df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
    // Check df for successful creation before proceeding. 
    if (!df) 
    { 
    // Take error action. 
    }

## <a name="class-dictfieldgroup"></a>クラス DictFieldGroup
    class DictFieldGroup extends Object

DictFieldGroup クラスは、テーブル内の固有のフィールド グループに関する情報を提供します。

### <a name="remarks"></a>備考

このクラスを使用するコード例では、DictFieldGroup.numberOfFields Method メソッドを参照してください。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                             | 説明                                                                         |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| public FieldId field(int fieldNumber)                                              | フィールド グループから指定したフィールドを返します。                                   |
| public str label()                                                                 | フィールド グループのラベル テキストを返します。                                          |
| public str labelId()                                                               | フィールド グループのラベル ID を返します。                                            |
| public str methodName(FieldId fieldId)                                             | フィールド グループから指定したメソッドの名前を返します。                      |
| public str name()                                                                  | フィールド グループの名前を返します。                                                |
| public int numberOfFields()                                                        | フィールド グループのテーブル フィールドの数と編集メソッドと表示メソッドを返します。 |
| public TableId tableid()                                                           | フィールド グループに関連付けられたテーブル ID を返します。                |
| public void new(TableId tableId, str FieldGroupName, \[TableId includeBaseTable\]) | Object クラスの新しいインスタンスを初期化します。                                     |

### <a name="method-field"></a>メソッド field

フィールド グループから指定したフィールドを返します。

    public FieldId field(int fieldNumber)

#### <a name="parameters"></a>パラメーター

fieldNumber  
フィールド グループのフィールド内のフィールドへの 1 から始まるインデックス。 インデックスは、Finance and Operations アプリケーション オブジェクト ツリー (AOT) と同じ順序です。

#### <a name="return-value"></a>戻り値

フィールドのフィールド ID。 品目が表示メソッドの場合は、ID は、フォーム 65280 + 0 から始まるメソッドのインデックスになります。

#### <a name="remarks"></a>備考

フィールド メソッドを使用するコード例では、DictFieldGroup.numberOfFields Method メソッドを参照してください。

### <a name="method-label"></a>メソッド label

フィールド グループのラベル テキストを返します。

    public str label()

#### <a name="return-value"></a>戻り値

フィールド グループのラベル テキスト。

### <a name="method-labelid"></a>メソッド labelId

フィールド グループのラベル ID を返します。

    public str labelId()

#### <a name="return-value"></a>戻り値

フィールド グループのラベル ID。

### <a name="method-methodname"></a>メソッド methodName

フィールド グループから指定したメソッドの名前を返します。

    public str methodName(FieldId fieldId)

#### <a name="parameters"></a>パラメーター

fieldId  
返されるメソッド名のフィールド メソッドへの呼び出しから返されるフィールド ID。 有効なフィールド ID が使用されていることを確認するのは開発者の責任です。

#### <a name="return-value"></a>戻り値

フィールド グループから指定されたメソッドの名前。fieldId の値が 65280 より小さい場合は空の文字列。

#### <a name="remarks"></a>備考

メソッドは、メソッド インデックス + 65280 によって指定されます。 このメソッドを使用するコード例では、DictFieldGroup.numberOfFields Method メソッドを参照してください。

### <a name="method-name"></a>メソッド名

フィールド グループの名前を返します。

    public str name()

#### <a name="return-value"></a>戻り値

フィールド グループの名前。

### <a name="method-numberoffields"></a>メソッド numberOfFields

フィールド グループのテーブル フィールドの数と編集メソッドと表示メソッドを返します。

    public int numberOfFields()

#### <a name="return-value"></a>戻り値

フィールド グループのテーブル フィールドの数と編集メソッドと表示メソッド。

#### <a name="examples"></a>例

次の例は、フィールド グループのテーブル フィールド数と編集メソッドおよび表示メソッドの数の取得を示しています。

        DictFieldGroup  fldGrp; 
        DictField       fld; 
        fieldId         fldId; 
        tableId         tblId; 
        int             i; 
        tblId = tablenum("CustTable"); 
        fldGrp = new DictFieldGroup(tblId,"AutoReport"); 
        if (fldGrp) 
        {     for (i=1; i <= fldGrp.numberOfFields(); i++) 
             { 
                 fldId = fldGrp.field(i); 
                 fld  = new DictField(tblId, fldId); 
                 if (fld) 
                 { 
                    print 'Field: ' + fld.name() 
           + ' (' + int2str(fldId) + ')'; 
                 } 
                 else 
                 { 
                    print 'MethodName: ' + fldGrp.methodName(fldId)  
                    + ' (' + int2str(fldId) + ')'; 
                 } 
             } 
        }

### <a name="method-tableid"></a>メソッド tableid

フィールド グループに関連付けられたテーブル ID を返します。

    public TableId tableid()

#### <a name="return-value"></a>戻り値

フィールド グループに関連付けられたテーブル ID。

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(TableId tableId, str FieldGroupName, [TableId includeBaseTable])

#### <a name="parameters"></a>パラメーター

tableId  

<!-- -->

FieldGroupName  

<!-- -->

includeBaseTable  

#### <a name="remarks"></a>備考

このメソッドを使用するコード例では、DictFieldGroup.numberOfFields Method メソッドを参照してください。

## <a name="class-dictfulltextindex"></a>クラス DictFullTextIndex
    class DictFullTextIndex extends Object

DictFullTextIndex クラスは、フル テキスト インデックスに関するメタデータを返します。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                  | 説明                                            |
|---------------------------------------------------------|--------------------------------------------------------|
| public FullTextIndexChangeTracking changeTrackingMode() | フル テキスト インデックスの変更追跡モードを取得します。  |
| public ConfigurationKeyId configurationKeyId()          | インデックスのコンフィギュレーション キーの ID を返します。 |
| public IndexId id()                                     | フル テキスト インデックスの ID を取得します。                    |
| public str name()                                       | フル テキスト インデックスの名前を取得します。                  |
| public TableId tableid()                                | インデックスを含むテーブルの ID を返します。   |
| public void new(TableId tableId, IndexId indexId)       | Object クラスの新しいインスタンスを初期化します。        |

### <a name="method-changetrackingmode"></a>メソッド changeTrackingMode

フル テキスト インデックスの変更追跡モードを取得します。

    public FullTextIndexChangeTracking changeTrackingMode()

#### <a name="return-value"></a>戻り値

### <a name="method-configurationkeyid"></a>メソッド configurationKeyId

インデックスのコンフィギュレーション キーの ID を返します。

    public ConfigurationKeyId configurationKeyId()

#### <a name="return-value"></a>戻り値

インデックスのコンフィギュレーション キーの ID。インデックスにコンフィギュレーション キーがない場合は 0 (ゼロ)。

### <a name="method-id"></a>メソッド id

フル テキスト インデックスの ID を取得します。

    public IndexId id()

#### <a name="return-value"></a>戻り値

インデックスの ID です。

### <a name="method-name"></a>メソッド名

フル テキスト インデックスの名前を取得します。

    public str name()

#### <a name="return-value"></a>戻り値

インデックスの名前。

### <a name="method-tableid"></a>メソッド tableid

インデックスを含むテーブルの ID を返します。

    public TableId tableid()

#### <a name="return-value"></a>戻り値

インデックスを含むテーブルの ID。

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(TableId tableId, IndexId indexId)

#### <a name="parameters"></a>パラメーター

tableId  

<!-- -->

indexId  

## <a name="class-dictindex"></a>クラス DictIndex
    class DictIndex extends Object

DictIndex クラスは、テーブル インデックスに関するメタデータを返します。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

次の例では、DictIndex クラスのインスタンスを作成します。

    Dictionary dict; 
    DictTable  table; 
    DictIndex  idx; 
    dict = new Dictionary(); 
    table = new DictTable(dict.tableName2Id("Address")); 
    idx = new DictIndex(table.id(), table.indexName2Id("AddrIdx"));

### <a name="methods"></a>メソッド

| 方法                                                                                                                          | 説明                                                           |
|---------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| public boolean allowDuplicates()                                                                                                | インデックスの allowDuplicates プロパティの値を返します。      |
| public ConfigurationKeyId configurationKeyId()                                                                                  | インデックスのコンフィギュレーション キーの ID を返します。                |
| public boolean enabled()                                                                                                        | インデックスが有効かどうかを示す値を返します。          |
| public FieldId field(int fieldNumber)                                                                                           | インデックス内の指定したフィールドの ID を返します。                   |
| public ValidTimeStateMode getValidTimeStateMode()                                                                               |                                                                       |
| public IndexId id()                                                                                                             | インデックスの ID を返します。                                          |
| public FieldId includedColumn(int fieldNumber)                                                                                  |                                                                       |
| public boolean isAlternateKey()                                                                                                 |                                                                       |
| public boolean isSql()                                                                                                          | インデックスが SQL データベースにあるかどうかを示す値を取得します。 |
| public boolean isValidTimeStateKey()                                                                                            |                                                                       |
| public boolean modify(boolean enabled, boolean allowDuplicates, boolean saveInLoadedLayer)                                      | インデックスを変更します。                                                   |
| public str name(\[DbBackend db\])                                                                                               | インデックスの名前を返します。                                        |
| public int numberOfFields()                                                                                                     | インデックス定義のフィールドの数を返します。                 |
| public int numberOfIncludedColumns()                                                                                            |                                                                       |
| public boolean setAlternateKey(boolean alternateKey, boolean saveInLoadedLayer)                                                 |                                                                       |
| public boolean setValidTimeStateKey(boolean setValidTimeStateKey, ValidTimeStateMode validTimeState, boolean saveInLoadedLayer) |                                                                       |
| public TableId tableid()                                                                                                        | インデックスを含むテーブルの ID を返します。                  |
| public void new(TableId tableId, IndexId indexId)                                                                               | Object クラスの新しいインスタンスを初期化します。                       |

### <a name="method-allowduplicates"></a>メソッド allowDuplicates

インデックスの allowDuplicates プロパティの値を返します。

    public boolean allowDuplicates()

#### <a name="return-value"></a>戻り値

インデックスが重複を許容する場合は true。それ以外の場合は、false。

### <a name="method-configurationkeyid"></a>メソッド configurationKeyId

インデックスのコンフィギュレーション キーの ID を返します。

    public ConfigurationKeyId configurationKeyId()

#### <a name="return-value"></a>戻り値

インデックスのコンフィギュレーション キーの ID。インデックスにコンフィギュレーション キーがない場合は 0 (ゼロ)。

### <a name="method-enabled"></a>メソッド enabled

インデックスが有効かどうかを示す値を返します。

    public boolean enabled()

#### <a name="return-value"></a>戻り値

インデックスが有効である場合は true。それ以外の場合は、false。

### <a name="method-field"></a>メソッド field

インデックス内の指定したフィールドの ID を返します。

    public FieldId field(int fieldNumber)

#### <a name="parameters"></a>パラメーター

fieldNumber  
インデックス内のフィールドの 1 から始まるインデックス。

#### <a name="return-value"></a>戻り値

fieldNumber により指定されているフィールドの ID。fieldNumber が有効なフィールドを表していない場合は 0 (ゼロ)。

#### <a name="examples"></a>例

次の例は、インデックス内の各フィールドの取得を示しています。 各フィールドの名前は、ループを使用して表示されます。

    Dictionary dict; 
    DictTable  table; 
    DictIndex  idx; 
    DictField  field; 
    int i; 
    dict = new Dictionary(); 
    table = new DictTable(dict.tableName2Id("Address")); 
    idx = new DictIndex(table.id(), table.indexName2Id("AddrIdx")); 
    for (i=1; i <= idx.numberOfFields(); i++) 
    { 
        field = new DictField(table.id(), idx.field(i)); 
        print field.name(); 
    }

### <a name="method-getvalidtimestatemode"></a>メソッド getValidTimeStateMode

    public ValidTimeStateMode getValidTimeStateMode()

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

インデックスの ID を返します。

    public IndexId id()

#### <a name="return-value"></a>戻り値

インデックスの ID です。

### <a name="method-includedcolumn"></a>メソッド includedColumn

    public FieldId includedColumn(int fieldNumber)

#### <a name="parameters"></a>パラメーター

fieldNumber  

#### <a name="return-value"></a>戻り値

### <a name="method-isalternatekey"></a>メソッド isAlternateKey

    public boolean isAlternateKey()

#### <a name="return-value"></a>戻り値

### <a name="method-issql"></a>メソッド isSql

インデックスが SQL データベースにあるかどうかを示す値を取得します。

    public boolean isSql()

#### <a name="return-value"></a>戻り値

インデックスが SQL データベースである場合は true。それ以外の場合は、false。

### <a name="method-isvalidtimestatekey"></a>メソッド isValidTimeStateKey

    public boolean isValidTimeStateKey()

#### <a name="return-value"></a>戻り値

### <a name="method-modify"></a>メソッド modify

インデックスを変更します。

    public boolean modify(boolean enabled, boolean allowDuplicates, boolean saveInLoadedLayer)

#### <a name="parameters"></a>パラメーター

有効  
読み込まれたレイヤーに変更が保存されるかどうかを示すブール値。

<!-- -->

allowDuplicates  
読み込まれたレイヤーに変更が保存されるかどうかを示すブール値。

<!-- -->

saveInLoadedLayer  
読み込まれたレイヤーに変更が保存されるかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

インデックスが正常に修正された場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

このメソッドを使用すると、X++ コードとメタデータを作成、読み込み、更新、および削除ができます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="method-name"></a>メソッド名

インデックスの名前を返します。

    public str name([DbBackend db])

#### <a name="parameters"></a>パラメーター

db  
返される名前のタイプを指定する DbBackend 値。 これは、インデックスのネイティブ名の場合は DbBackend :: Native、インデックスの SQL 名の場合は DbBackend :: Sql になります。 Db が指定されていない場合は、DbBackend::Native が使用されます。

#### <a name="return-value"></a>戻り値

データベースで指定された形式のインデックスの名前。

### <a name="method-numberoffields"></a>メソッド numberOfFields

インデックス定義のフィールドの数を返します。

    public int numberOfFields()

#### <a name="return-value"></a>戻り値

インデックス内のフィールドの数。

#### <a name="examples"></a>例

次の例は、インデックス内のフィールド数の取得を示し、インデックス内のフィールドの名前をリストしています。

    Dictionary dict; 
    DictTable  table; 
    DictIndex  idx; 
    DictField  field; 
    int i; 
    dict = new Dictionary(); 
    table = new DictTable(dict.tableName2Id("Address")); 
    idx = new DictIndex(table.id(), table.indexName2Id("AddrIdx")); 
    for (i=1; i <= idx.numberOfFields(); i++) 
    { 
        field = new DictField(table.id(), idx.field(i)); 
        print field.name(); 
    }

### <a name="method-numberofincludedcolumns"></a>メソッド numberOfIncludedColumns

    public int numberOfIncludedColumns()

#### <a name="return-value"></a>戻り値

### <a name="method-setalternatekey"></a>メソッド setAlternateKey

    public boolean setAlternateKey(boolean alternateKey, boolean saveInLoadedLayer)

#### <a name="parameters"></a>パラメーター

alternateKey  

<!-- -->

saveInLoadedLayer  

#### <a name="return-value"></a>戻り値

### <a name="method-setvalidtimestatekey"></a>メソッド setValidTimeStateKey

    public boolean setValidTimeStateKey(boolean setValidTimeStateKey, ValidTimeStateMode validTimeState, boolean saveInLoadedLayer)

#### <a name="parameters"></a>パラメーター

setValidTimeStateKey  

<!-- -->

validTimeState  

<!-- -->

saveInLoadedLayer  

#### <a name="return-value"></a>戻り値

### <a name="method-tableid"></a>メソッド tableid

インデックスを含むテーブルの ID を返します。

    public TableId tableid()

#### <a name="return-value"></a>戻り値

インデックスを含むテーブルの ID。

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(TableId tableId, IndexId indexId)

#### <a name="parameters"></a>パラメーター

tableId  
DictIndex クラスのこのインスタンスを作成するために使用されるインデックスの ID。

<!-- -->

indexId  
DictIndex クラスのこのインスタンスを作成するために使用されるインデックスの ID。

## <a name="class-dictionary"></a>クラス ディクショナリ
    class Dictionary extends Object

ディクショナリ クラスは、テーブル、拡張データ型、クラス、および Finance and Operations アプリケーション オブジェクト ツリー (AOT) の他の品目に関する情報を提供します。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                                                       | 説明                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| public int classCnt()                                                                                                                        | Finance and Operations のクラスの数を示します。                                                        |
| public ClassId classCnt2Id(int cnt)                                                                                                          | 指定されたクラスの ID を提供します。                                                                            |
| public str className(ClassId classId)                                                                                                        | 指定されたクラスの名前を提供します。                                                                          |
| public ClassId className2Id(str name)                                                                                                        | クラスの名前に基づいて、指定されたクラスの ID を提供します。                                                  |
| public ClassId classNext(ClassId classId)                                                                                                    | クラス ID に基づいて、指定されたクラスの後に続くクラスを示します。                                     |
| public DictClass classObject(ClassId classId)                                                                                                | DictClass オブジェクトを返すことで、指定されたクラスに関する情報を提供します。                                    |
| public int configurationKeyCnt()                                                                                                             | Finance and Operations のコンフィギュレーション キーの数を示します。                                             |
| public ConfigurationKeyId configurationKeyCnt2Id(int cnt)                                                                                    | 指定された構成キーの ID を提供します。                                                                |
| public str configurationKeyName(ConfigurationKeyId configurationKey)                                                                         | 指定された構成キーの名前を提供します。                                                              |
| public ConfigurationKeyId configurationKeyName2Id(str name)                                                                                  | 構成キー名に基づいて、指定された構成キーの ID を提供します。                          |
| public ConfigurationKeyId configurationKeyNext(ConfigurationKeyId configurationKey)                                                          | コンフィギュレーション キー ID に基づいて、指定されたコンフィギュレーション キーの後に続くコンフィギュレーション キーを示します。 |
| public DictConfigurationKey configurationKeyObject(ConfigurationKeyId configurationKey)                                                      | DictConfigurationKey オブジェクトを返すことで、指定された構成キーに関する情報を提供します。             |
| public SelectableDataArea currentCompany()                                                                                                   | データベースでデータを使用できる現在の会社を示します。                                       |
| public int enumCnt()                                                                                                                         | Finance and Operations の列挙型の数を示します。                                              |
| public EnumId enumCnt2Id(int cnt)                                                                                                            | 指定された列挙型タイプの ID を提供します。                                                                 |
| public str enumName(EnumId typeId)                                                                                                           | 指定された列挙型の名前を指定します。                                                                   |
| public EnumId enumName2Id(str name)                                                                                                          | 名前に基づく、指定された列挙型の ID を提供します。                                                   |
| public EnumId enumNext(EnumId typeId)                                                                                                        | 列挙型 ID に基づいて、指定した列挙型の後に続く列挙型を示します。    |
| public DictEnum enumObject(EnumId typeId)                                                                                                    | DictEnum オブジェクトを返すことで、指定された列挙型に関する情報を提供します。                               |
| public int licenseCodeCnt()                                                                                                                  | Finance and Operations のライセンス コードの数を示します。                                                  |
| public LicenseCodeId licenseCodeCnt2Id(int cnt)                                                                                              | 指定されたライセンス コードの ID を提供します。                                                                     |
| public str licenseCodeName(LicenseCodeId licenseCode)                                                                                        | 指定されたライセンス コードの名前を提供します。                                                                   |
| public LicenseCodeId licenseCodeName2Id(str name)                                                                                            | ライセンス コード名に基づいて、指定されたライセンス コードの ID を提供します。                                    |
| public LicenseCodeId licenseCodeNext(LicenseCodeId licenseCode)                                                                              | ライセンス コード ID に基づいて、指定したライセンス コードの後に続くライセンス コードを示します。                |
| public DictLicenseCode licenseCodeObject(LicenseCodeId licenseCode)                                                                          | DictLicenseCode オブジェクトを返すことで、指定されたライセンス コードに関する情報を提供します。                       |
| public int tableCnt()                                                                                                                        | Finance and Operations のテーブルの数を示します。                                                         |
| public TableId tableCnt2Id(int cnt)                                                                                                          | 指定されたテーブルの ID を提供します。                                                                            |
| public str tableName(TableId tableId)                                                                                                        | 指定されたテーブルの名前を提供します。                                                                          |
| public TableId tableName2Id(str name)                                                                                                        | テーブルの名前に基づいて、指定されたテーブルの ID を提供します。                                                  |
| public TableId tableNext(TableId tableId)                                                                                                    | テーブル ID に基づいて、指定されたテーブルの後に続くテーブルを示します。                                     |
| public DictTable tableObject(TableId tableId)                                                                                                | DictTable オブジェクトを返すことで、指定されたテーブルに関する情報を提供します。                                    |
| public boolean tableSql(TableId tableId)                                                                                                     | テーブルが SQL テーブルであるかどうかを示します。                                                                        |
| public boolean tableSystem(TableId tableId)                                                                                                  | テーブルがシステム テーブルであるかどうかを示します。                                                                     |
| public int testCode(int id, str value, str name, str serialno, str expiryDate, \[int userCount\], \[boolean verifyCert\], \[str timestamp\]) |                                                                                                                  |
| public int typeCnt()                                                                                                                         | Finance and Operations の拡張データ型の数を示します。                                            |
| public ExtendedTypeId typeCnt2Id(int cnt)                                                                                                    | 指定された拡張データ型の ID を提供します。                                                               |
| public str typeName(ExtendedTypeId typeId)                                                                                                   | 指定された拡張データ型の名前を提供します。                                                             |
| public ExtendedTypeId typeName2Id(str name)                                                                                                  | 拡張データ型名に基づいて、指定された拡張データ型の ID を提供します。                        |
| public ExtendedTypeId typeNext(ExtendedTypeId typeId)                                                                                        | ID に基づいて、指定された拡張データ型の後に続く拡張データ型を示します。                 |
| public DictType typeObject(ExtendedTypeId typeId)                                                                                            | DictType オブジェクトを返すことで、指定された拡張データ型に関する情報を提供します。                        |
| ::public static boolean safeMode()                                                                                                           |                                                                                                                  |
| ::public static void loginSettingsFlush()                                                                                                    | Finance and Operations のログオン設定を更新します。                                                          |
| ::public static void dataFlush(\[TableId tableId\])                                                                                          | Finance and Operations でテーブル データを更新します。                                                               |
| public void tableFlush()                                                                                                                     | Finance and Operations でテーブルを更新します。                                                                   |
| public void enumFlush()                                                                                                                      | Finance and Operations で列挙型を更新します。                                                        |
| public void new()                                                                                                                            | Dictionary クラスの新しいインスタンスを初期化します。                                                              |
| public void classFlush()                                                                                                                     | Finance and Operations でクラスを更新します。                                                                  |
| public void reloadSecurity(\[boolean reloadCodes\], \[boolean setSynchronizeRequired\], \[boolean flushTable\])                              | 機能キー システムを再読み込みします。                                                                                  |
| public void typeFlush()                                                                                                                      | Finance and Operations で拡張データ型を更新します。                                                      |
| public void configurationKeyFlush()                                                                                                          | Finance and Operations で更新キーを更新します。                                                       |
| public void licenseCodeFlush()                                                                                                               | Finance and Operations でライセンス コードを更新します。                                                            |
| ::public static void aodFlush()                                                                                                              | .aod ファイルを更新します。                                                                                         |

### <a name="method-classcnt"></a>メソッド classCnt

Finance and Operations のクラスの数を示します。

    public int classCnt()

#### <a name="return-value"></a>戻り値

クラスの数を示す整数値。

### <a name="method-classcnt2id"></a>メソッド classCnt2Id

指定されたクラスの ID を提供します。

    public ClassId classCnt2Id(int cnt)

#### <a name="parameters"></a>パラメーター

cnt  
Finance and Operations のクラスの順序に基づいてクラスを指定する整数値。

#### <a name="return-value"></a>戻り値

クラス ID を示す classId システム データ型値; Dictionary::classCnt メソッドによって返されるクラスの数より大きな cnt 値を渡すと 0 (ゼロ)。

### <a name="method-classname"></a>メソッド className

指定されたクラスの名前を提供します。

    public str className(ClassId classId)

#### <a name="parameters"></a>パラメーター

classId  
クラス ID を示す classId システム データ型。

#### <a name="return-value"></a>戻り値

クラス名を示す文字列。

#### <a name="remarks"></a>備考

クラス ID は、符号なし整数です。

### <a name="method-classname2id"></a>メソッド className2Id

クラスの名前に基づいて、指定されたクラスの ID を提供します。

    public ClassId className2Id(str name)

#### <a name="parameters"></a>パラメーター

名前  
クラス名を示す文字列。

#### <a name="return-value"></a>戻り値

クラス ID を示す classId システム データ型値; 存在しないクラスの名前値を渡すと 0 (ゼロ)。

### <a name="method-classnext"></a>メソッド classNext

クラス ID に基づいて、指定されたクラスの後に続くクラスを示します。

    public ClassId classNext(ClassId classId)

#### <a name="parameters"></a>パラメーター

classId  
クラス ID を示す classId システム データ型。

#### <a name="return-value"></a>戻り値

指定されたクラスを継承するクラスを示す classId システム データ型値。

### <a name="method-classobject"></a>メソッド classObject

DictClass オブジェクトを返すことで、指定されたクラスに関する情報を提供します。

    public DictClass classObject(ClassId classId)

#### <a name="parameters"></a>パラメーター

classId  
クラス ID を示す classId システム データ型。

#### <a name="return-value"></a>戻り値

指定されたクラスに関する情報を含む DictClass オブジェクト。

### <a name="method-configurationkeycnt"></a>メソッド configurationKeyCnt

Finance and Operations のコンフィギュレーション キーの数を示します。

    public int configurationKeyCnt()

#### <a name="return-value"></a>戻り値

コンフィギュレーション キーの数を示す整数値。

### <a name="method-configurationkeycnt2id"></a>メソッド configurationKeyCnt2Id

指定された構成キーの ID を提供します。

    public ConfigurationKeyId configurationKeyCnt2Id(int cnt)

#### <a name="parameters"></a>パラメーター

cnt  
Finance and Operations のコンフィギュレーション キーの順序に基づいてコンフィギュレーション キーを指定する整数。

#### <a name="return-value"></a>戻り値

コンフィギュレーション キー ID を示す configurationKeyId システム データ型値; Dictionary::configurationKeyCnt メソッドから返されるコンフィギュレーション キーの数よりも大きい cnt 値を渡すと、0 (ゼロ) になります。

### <a name="method-configurationkeyname"></a>メソッド configurationKeyName

指定された構成キーの名前を提供します。

    public str configurationKeyName(ConfigurationKeyId configurationKey)

#### <a name="parameters"></a>パラメーター

configurationKey  
コンフィギュレーション キーの ID を示す configurationKeyId システム データ型。

#### <a name="return-value"></a>戻り値

コンフィギュレーション キーの名前を示す文字列。

### <a name="method-configurationkeyname2id"></a>メソッド configurationKeyName2Id

構成キー名に基づいて、指定された構成キーの ID を提供します。

    public ConfigurationKeyId configurationKeyName2Id(str name)

#### <a name="parameters"></a>パラメーター

名前  
コンフィギュレーション キーの名前を示す文字列。

#### <a name="return-value"></a>戻り値

コンフィギュレーション キー ID を示す configurationKeyId システム データ型値; 存在しないコンフィギュレーション キー の名前の値を渡すと、0 (ゼロ) になります。

### <a name="method-configurationkeynext"></a>メソッド configurationKeyNext

コンフィギュレーション キー ID に基づいて、指定されたコンフィギュレーション キーの後に続くコンフィギュレーション キーを示します。

    public ConfigurationKeyId configurationKeyNext(ConfigurationKeyId configurationKey)

#### <a name="parameters"></a>パラメーター

configurationKey  
コンフィギュレーション キーの ID を示す configurationKeyId システム データ型。

#### <a name="return-value"></a>戻り値

指定されたコンフィギュレーション キー の後に続くコンフィギュレーション キーの configurationKeyId システム データ型値。

### <a name="method-configurationkeyobject"></a>メソッド configurationKeyObject

DictConfigurationKey オブジェクトを返すことで、指定された構成キーに関する情報を提供します。

    public DictConfigurationKey configurationKeyObject(ConfigurationKeyId configurationKey)

#### <a name="parameters"></a>パラメーター

configurationKey  
コンフィギュレーション キーの ID を示す configurationKeyId システム データ型。

#### <a name="return-value"></a>戻り値

指定されたコンフィギュレーション キーに関する情報を含む DictConfigurationKey オブジェクト。

### <a name="method-currentcompany"></a>メソッド currentCompany

データベースでデータを使用できる現在の会社を示します。

    public SelectableDataArea currentCompany()

#### <a name="return-value"></a>戻り値

現在の会社を示す SelectableDataArea システムのデータ型の値。

### <a name="method-enumcnt"></a>メソッド enumCnt

Finance and Operations の列挙型の数を示します。

    public int enumCnt()

#### <a name="return-value"></a>戻り値

列挙型の数を示す整数。

### <a name="method-enumcnt2id"></a>メソッド enumCnt2Id

指定された列挙型タイプの ID を提供します。

    public EnumId enumCnt2Id(int cnt)

#### <a name="parameters"></a>パラメーター

cnt  
Finance and Operations の列挙型の順序に基づいて列挙型を指定する整数。

#### <a name="return-value"></a>戻り値

列挙型 ID を示す enumId システム データ型値です。Dictionary::enumCnt メソッドによって返されるクラスの数より大きな cnt 値を渡すと 0 (ゼロ) になります。

### <a name="method-enumname"></a>メソッド enumName

指定された列挙型の名前を指定します。

    public str enumName(EnumId typeId)

#### <a name="parameters"></a>パラメーター

typeId  
列挙の enumId システム データ型です。

#### <a name="return-value"></a>戻り値

列挙の名前を示す文字列。

### <a name="method-enumname2id"></a>メソッド enumName2Id

名前に基づく、指定された列挙型の ID を提供します。

    public EnumId enumName2Id(str name)

#### <a name="parameters"></a>パラメーター

名前  
列挙の名前を示す文字列。

#### <a name="return-value"></a>戻り値

列挙の ID を示す enumId システム データ型値です。

### <a name="method-enumnext"></a>メソッド enumNext

列挙型 ID に基づいて、指定した列挙型の後に続く列挙型を示します。

    public EnumId enumNext(EnumId typeId)

#### <a name="parameters"></a>パラメーター

typeId  
列挙 ID を示す enumId システム データ型です。

#### <a name="return-value"></a>戻り値

指定された列挙を継承する列挙の enumId システム データ型値です。

### <a name="method-enumobject"></a>メソッド enumObject

DictEnum オブジェクトを返すことで、指定された列挙型に関する情報を提供します。

    public DictEnum enumObject(EnumId typeId)

#### <a name="parameters"></a>パラメーター

typeId  
列挙 ID を示す enumId システム データ型です。

#### <a name="return-value"></a>戻り値

指定された列挙に関する情報を含む DictEnum オブジェクト。

### <a name="method-licensecodecnt"></a>メソッド licenseCodeCnt

Finance and Operations のライセンス コードの数を示します。

    public int licenseCodeCnt()

#### <a name="return-value"></a>戻り値

ライセンス コードの数を示す整数。

### <a name="method-licensecodecnt2id"></a>メソッド licenseCodeCnt2Id

指定されたライセンス コードの ID を提供します。

    public LicenseCodeId licenseCodeCnt2Id(int cnt)

#### <a name="parameters"></a>パラメーター

cnt  
Finance and Operations のライセンス コードの順序に基づいてライセンス コードを指定する整数。

#### <a name="return-value"></a>戻り値

ライセンス コード ID を示す licenseCodeId システムのデータ型の値、Dictionary::licenseCodeCnt メソッドによって返されるライセンス コードの数より大きな cnt 値を渡すと 0 (ゼロ)。

### <a name="method-licensecodename"></a>メソッド licenseCodeName

指定されたライセンス コードの名前を提供します。

    public str licenseCodeName(LicenseCodeId licenseCode)

#### <a name="parameters"></a>パラメーター

licenseCode  
ライセンス コード ID を示す licenseCodeId システム データ型。

#### <a name="return-value"></a>戻り値

ライセンス コード名を示す文字列。

### <a name="method-licensecodename2id"></a>メソッド licenseCodeName2Id

ライセンス コード名に基づいて、指定されたライセンス コードの ID を提供します。

    public LicenseCodeId licenseCodeName2Id(str name)

#### <a name="parameters"></a>パラメーター

名前  
ライセンス コード名を示す文字列。

#### <a name="return-value"></a>戻り値

ライセンス コード ID を示す licenseCodeId システム データ型の値、存在しないライセンス コード名の値を渡すと 0 (ゼロ)。

### <a name="method-licensecodenext"></a>メソッド licenseCodeNext

ライセンス コード ID に基づいて、指定したライセンス コードの後に続くライセンス コードを示します。

    public LicenseCodeId licenseCodeNext(LicenseCodeId licenseCode)

#### <a name="parameters"></a>パラメーター

licenseCode  
ライセンス コード ID を示す licenseCodeId システム データ型。

#### <a name="return-value"></a>戻り値

指定したライセンス コードの後に続くライセンス コードの licenseCodeId システム データ型の値。

### <a name="method-licensecodeobject"></a>メソッド licenseCodeObject

DictLicenseCode オブジェクトを返すことで、指定されたライセンス コードに関する情報を提供します。

    public DictLicenseCode licenseCodeObject(LicenseCodeId licenseCode)

#### <a name="parameters"></a>パラメーター

licenseCode  
ライセンス コード ID を示す licenseCodeId システム データ。

#### <a name="return-value"></a>戻り値

指定されたライセンス コードに関する情報を含む DictLicenseCode オブジェクト。

### <a name="method-tablecnt"></a>メソッド tableCnt

Finance and Operations のテーブルの数を示します。

    public int tableCnt()

#### <a name="return-value"></a>戻り値

テーブルの数を示す整数。

### <a name="method-tablecnt2id"></a>メソッド tableCnt2Id

指定されたテーブルの ID を提供します。

    public TableId tableCnt2Id(int cnt)

#### <a name="parameters"></a>パラメーター

cnt  
テーブルの順序に基づく、テーブルを指定する整数。

#### <a name="return-value"></a>戻り値

テーブル ID を示す TableId システムのデータ型値、Dictionary::tableCnt メソッドによって返されるテーブル数より大きな cnt 値を渡すと 0 (ゼロ)。

### <a name="method-tablename"></a>メソッド tableName

指定されたテーブルの名前を提供します。

    public str tableName(TableId tableId)

#### <a name="parameters"></a>パラメーター

tableId  
テーブル ID を示す tableId システムのデータ型。

#### <a name="return-value"></a>戻り値

テーブル名を示す文字列、存在しない tableId 値を渡すと UNKNOWN。

#### <a name="remarks"></a>備考

存在しない tableId 値を渡すと、不明が返されます。

### <a name="method-tablename2id"></a>メソッド tableName2Id

テーブルの名前に基づいて、指定されたテーブルの ID を提供します。

    public TableId tableName2Id(str name)

#### <a name="parameters"></a>パラメーター

名前  
テーブル名を示す文字列。

#### <a name="return-value"></a>戻り値

テーブル ID を示す TableId システムのデータ型値、存在しないテーブルの名前の値を渡すと 0 (ゼロ)。

### <a name="method-tablenext"></a>メソッド tableNext

テーブル ID に基づいて、指定されたテーブルの後に続くテーブルを示します。

    public TableId tableNext(TableId tableId)

#### <a name="parameters"></a>パラメーター

tableId  
テーブル ID を示す tableId システムのデータ型。

#### <a name="return-value"></a>戻り値

指定されたテーブルの後に続くテーブルの TableId システムのデータ型値。

### <a name="method-tableobject"></a>メソッド tableObject

DictTable オブジェクトを返すことで、指定されたテーブルに関する情報を提供します。

    public DictTable tableObject(TableId tableId)

#### <a name="parameters"></a>パラメーター

tableId  
テーブル ID を示す tableId システムのデータ型。

#### <a name="return-value"></a>戻り値

指定されたテーブルに関する情報を含む DictTable オブジェクト。

### <a name="method-tablesql"></a>メソッド tableSql

テーブルが SQL テーブルであるかどうかを示します。

    public boolean tableSql(TableId tableId)

#### <a name="parameters"></a>パラメーター

tableId  
テーブル ID を示す tableId システムのデータ型。

#### <a name="return-value"></a>戻り値

テーブルが SQL テーブルである場合は true。それ以外の場合は false。

### <a name="method-tablesystem"></a>メソッド tableSystem

テーブルがシステム テーブルであるかどうかを示します。

    public boolean tableSystem(TableId tableId)

#### <a name="parameters"></a>パラメーター

tableId  
テーブル ID を示す tableId システムのデータ型。

#### <a name="return-value"></a>戻り値

テーブルがシステム テーブルである場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

tableNum 組み込み関数を使用して、テーブル ID の代わりにテーブル名をこのメソッドに渡すことができます。 この機能の詳細については、「組み込み関数」を参照してください。

### <a name="method-testcode"></a>メソッド testCode

    public int testCode(int id, str value, str name, str serialno, str expiryDate, [int userCount], [boolean verifyCert], [str timestamp])

#### <a name="parameters"></a>パラメーター

id  

<!-- -->

値  

<!-- -->

名前  

<!-- -->

serialno  

<!-- -->

expiryDate  

<!-- -->

userCount  

<!-- -->

verifyCert  

<!-- -->

timestamp  

#### <a name="return-value"></a>戻り値

### <a name="method-typecnt"></a>メソッド typeCnt

Finance and Operations の拡張データ型の数を示します。

    public int typeCnt()

#### <a name="return-value"></a>戻り値

拡張データ型の数を示す整数。

### <a name="method-typecnt2id"></a>メソッド typeCnt2Id

指定された拡張データ型の ID を提供します。

    public ExtendedTypeId typeCnt2Id(int cnt)

#### <a name="parameters"></a>パラメーター

cnt  
Finance and Operations の拡張データ型の順序に基づいて拡張データ型を指定する整数。

#### <a name="return-value"></a>戻り値

拡張データ型の ID を示す extendedTypeId システム データ型値です。Dictionary::typeCnt メソッドによって返される拡張データ型の数より大きな cnt 値を渡すと 0 (ゼロ) になります。

### <a name="method-typename"></a>メソッド typeName

指定された拡張データ型の名前を提供します。

    public str typeName(ExtendedTypeId typeId)

#### <a name="parameters"></a>パラメーター

typeId  
拡張データ型の ID を示す extendedTypeId システム データ型です。

#### <a name="return-value"></a>戻り値

拡張データ型の名前を示す文字列。

### <a name="method-typename2id"></a>メソッド typeName2Id

拡張データ型名に基づいて、指定された拡張データ型の ID を提供します。

    public ExtendedTypeId typeName2Id(str name)

#### <a name="parameters"></a>パラメーター

名前  
拡張データ型の名前を示す文字列。

#### <a name="return-value"></a>戻り値

拡張データ型の ID を示す extendedTypeId システム データ型値です。存在しない拡張データ型の名前の値を渡した場合は 0 (ゼロ) になります。

### <a name="method-typenext"></a>メソッド typeNext

ID に基づいて、指定された拡張データ型の後に続く拡張データ型を示します。

    public ExtendedTypeId typeNext(ExtendedTypeId typeId)

#### <a name="parameters"></a>パラメーター

typeId  
拡張データ型の ID を示す extendedTypeId システム データ型です。

#### <a name="return-value"></a>戻り値

指定された拡張データ型を継承する拡張データ型の extendedTypeId システム データ型値です。

### <a name="method-typeobject"></a>メソッド typeObject

DictType オブジェクトを返すことで、指定された拡張データ型に関する情報を提供します。

    public DictType typeObject(ExtendedTypeId typeId)

#### <a name="parameters"></a>パラメーター

typeId  
拡張データ型の ID を示す extendedTypeId システム データ型です。

#### <a name="return-value"></a>戻り値

指定されてた拡張データ型に関する情報を含む DictType オブジェクト。

### <a name="method-safemode"></a>メソッド safeMode

    public static boolean safeMode()

#### <a name="return-value"></a>戻り値

### <a name="method-loginsettingsflush"></a>メソッド loginSettingsFlush

Finance and Operations のログオン設定を更新します。

    public static void loginSettingsFlush()

### <a name="method-dataflush"></a>メソッド dataFlush

Finance and Operations でテーブル データを更新します。

    public static void dataFlush([TableId tableId])

#### <a name="parameters"></a>パラメーター

tableId  
単一のテーブルまたはすべてのテーブルを示す tableId システムのデータ型。 既定値はすべてです。

#### <a name="remarks"></a>備考

既定では、このメソッドはすべてのテーブルのデータを更新します。

### <a name="method-tableflush"></a>メソッド tableFlush

Finance and Operations でテーブルを更新します。

    public void tableFlush()

### <a name="method-enumflush"></a>メソッド enumFlush

Finance and Operations で列挙型を更新します。

    public void enumFlush()

### <a name="method-new"></a>メソッド new

Dictionary クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-classflush"></a>メソッド classFlush

Finance and Operations でクラスを更新します。

    public void classFlush()

### <a name="method-reloadsecurity"></a>メソッド reloadSecurity

機能キー システムを再読み込みします。

    public void reloadSecurity([boolean reloadCodes], [boolean setSynchronizeRequired], [boolean flushTable])

#### <a name="parameters"></a>パラメーター

reloadCodes  

<!-- -->

setSynchronizeRequired  

<!-- -->

flushTable  

#### <a name="remarks"></a>備考

\_reloadCodes パラメーターの既定値は false です。 \_setSynchronizeRequired パラメーターの既定値は true です。

### <a name="method-typeflush"></a>メソッド typeFlush

Finance and Operations で拡張データ型を更新します。

    public void typeFlush()

### <a name="method-configurationkeyflush"></a>メソッド configurationKeyFlush

Finance and Operations で更新キーを更新します。

    public void configurationKeyFlush()

### <a name="method-licensecodeflush"></a>メソッド licenseCodeFlush

Finance and Operations でライセンス コードを更新します。

    public void licenseCodeFlush()

### <a name="method-aodflush"></a>メソッド aodFlush

.aod ファイルを更新します。

    public static void aodFlush()

## <a name="class-dictlicensecode"></a>クラス DictLicenseCode
    class DictLicenseCode extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                       | 説明                                     |
|----------------------------------------------|-------------------------------------------------|
| public LicenseCodeGroup group()              |                                                 |
| public LicenseCodeId id()                    |                                                 |
| public str label()                           |                                                 |
| public str name()                            |                                                 |
| public SysLicensePackageType package()       |                                                 |
| public int publicKey()                       |                                                 |
| public LicenseCodeType type()                |                                                 |
| public void new(LicenseCodeId licenseCodeId) | Object クラスの新しいインスタンスを初期化します。 |

### <a name="method-group"></a>メソッド group

    public LicenseCodeGroup group()

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

    public LicenseCodeId id()

#### <a name="return-value"></a>戻り値

### <a name="method-label"></a>メソッド label

    public str label()

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

    public str name()

#### <a name="return-value"></a>戻り値

### <a name="method-package"></a>メソッド package

    public SysLicensePackageType package()

#### <a name="return-value"></a>戻り値

### <a name="method-publickey"></a>メソッド publicKey

    public int publicKey()

#### <a name="return-value"></a>戻り値

### <a name="method-type"></a>メソッドのタイプ

    public LicenseCodeType type()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(LicenseCodeId licenseCodeId)

#### <a name="parameters"></a>パラメーター

licenseCodeId  

## <a name="class-dictmethod"></a>クラス DictMethod
    class DictMethod extends MethodInfo

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                      | 説明                                                                                                                                                  |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public AccessSpecifier accessSpecifier()                    | メソッドがパブリック、保護、またはプライベートかどうかを指定します。                                                                                               |
| public str clrParameterType(int variableNumber)             |                                                                                                                                                              |
| public str clrReturnType()                                  |                                                                                                                                                              |
| public str clrVarType(int variableNumber)                   |                                                                                                                                                              |
| public boolean compiledOk()                                 | メソッドが正常にコンパイルしたかどうかを示します。                                                                                                          |
| public TableId displayId()                                  |                                                                                                                                                              |
| public DisplayFunctionType displayType()                    | メソッドの表示機能のタイプを示します。                                                                                                          |
| public boolean hasImplementation()                          | 実際のメソッドの実装がクラスにあるのか、基本クラスから派生したのかを判断します。                                                          |
| public boolean isAbstract()                                 | メソッドが抽象かどうかを示します。                                                                                                                    |
| public boolean isDelegate()                                 | メソッドがデリゲートかどうかを示します。                                                                                                                  |
| public boolean isStatic()                                   | メソッドが静的かどうかを示します。                                                                                                                      |
| public str name()                                           | メソッドの名前を取得します。                                                                                                                                 |
| public int parameterCnt()                                   | メソッドのパラメーター数を取得します。                                                                                                                |
| public int parameterId(int variableNumber)                  | 指定されたパラメータの ID を取得します。                                                                                                                      |
| public str parameterName(int variableNumber)                | 指定されたパラメータの名前を取得します。                                                                                                                    |
| public boolean parameterOptional(int variableNumber)        | メソッドの指定されたパラメーターが省略可能かどうかを示します。                                                                                         |
| public Types parameterType(int variableNumber)              |                                                                                                                                                              |
| public int parentId()                                       | メソッドを所有する親の ID を取得します。                                                                                                              |
| public str propertyHelp()                                   | メソッドに関連付けられているプロパティのヘルプ文字列を取得します。                                                                                    |
| public NoYes propertyMethod()                               | メソッドがプロパティ メソッドかどうかを示します。                                                                                                           |
| public int returnId()                                       | 値を返すメソッドについて、拡張データ型やクラスなどの特定の戻り値のデータ型の ID を指定します。                                  |
| public Types returnType()                                   | メソッドの戻り値の型を指定します。                                                                                                                              |
| public ClassRunMode runMode()                               | メソッドが実行される場所を指定します。                                                                                                                             |
| public int varCnt()                                         | メソッドの変数の数を取得します。                                                                                                                 |
| public str varName(int variableNumber)                      | 指定された変数の名前を取得します。                                                                                                                     |
| public void setMethod(MemberFunction method)                | MemberFunction クラスのインスタンスを使用して Finance and Operations アプリケーション オブジェクト ツリー (AOT) 内のノードのアプリケーション オブジェクト タイプを指定します。 |
| public void new(UtilElementType utilType, int id, str name) | Object クラスの新しいインスタンスを初期化します。                                                                                                              |

### <a name="method-accessspecifier"></a>メソッド accessSpecifier

メソッドがパブリック、保護、またはプライベートかどうかを指定します。

    public AccessSpecifier accessSpecifier()

#### <a name="return-value"></a>戻り値

メソッドがパブリック、保護、またはプライベートのいずれかを指定する AccessSpecifier 列挙値です。

### <a name="method-clrparametertype"></a>メソッド clrParameterType

    public str clrParameterType(int variableNumber)

#### <a name="parameters"></a>パラメーター

variableNumber  

#### <a name="return-value"></a>戻り値

### <a name="method-clrreturntype"></a>メソッド clrReturnType

    public str clrReturnType()

#### <a name="return-value"></a>戻り値

### <a name="method-clrvartype"></a>メソッド clrVarType

    public str clrVarType(int variableNumber)

#### <a name="parameters"></a>パラメーター

variableNumber  

#### <a name="return-value"></a>戻り値

### <a name="method-compiledok"></a>メソッド compiledOk

メソッドが正常にコンパイルしたかどうかを示します。

    public boolean compiledOk()

#### <a name="return-value"></a>戻り値

メソッドが正常にコンパイルされる場合は true。それ以外の場合は、false。

### <a name="method-displayid"></a>メソッド displayId

    public TableId displayId()

#### <a name="return-value"></a>戻り値

### <a name="method-displaytype"></a>メソッド displayType

メソッドの表示機能のタイプを示します。

    public DisplayFunctionType displayType()

#### <a name="return-value"></a>戻り値

メソッドの表示機能のタイプを示す DisplayFunctionType 列挙値。

#### <a name="remarks"></a>備考

次のテーブルに、displayType メソッドによって返される可能な値を示します。

|           |                                             |
|-----------|---------------------------------------------|
| 取得       | このメソッドは表示メソッドです。             |
| None      | このメソッドは、表示メソッドまたは編集メソッドではありません。 |
| RecordGet | このメソッドは、レコードを取得します。              |
| RecordSet | このメソッドは、レコードを設定します。                   |
| セット       | このメソッドは、編集メソッドです。               |

### <a name="method-hasimplementation"></a>メソッド hasImplementation

実際のメソッドの実装がクラスにあるのか、基本クラスから派生したのかを判断します。

    public boolean hasImplementation()

#### <a name="return-value"></a>戻り値

メソッドがクラス上に実装される場合は true。それ以外の場合は、false。

### <a name="method-isabstract"></a>メソッド isAbstract

メソッドが抽象かどうかを示します。

    public boolean isAbstract()

#### <a name="return-value"></a>戻り値

メソッドが抽象である場合は true。それ以外の場合は、false。

### <a name="method-isdelegate"></a>メソッド isDelegate

メソッドがデリゲートかどうかを示します。

    public boolean isDelegate()

#### <a name="return-value"></a>戻り値

メソッドがデリゲートされる場合は true。それ以外の場合は、false。

### <a name="method-isstatic"></a>メソッド isStatic

メソッドが静的かどうかを示します。

    public boolean isStatic()

#### <a name="return-value"></a>戻り値

メソッドが静的である場合は true。それ以外の場合は、false。

### <a name="method-name"></a>メソッド名

メソッドの名前を取得します。

    public str name()

#### <a name="return-value"></a>戻り値

メソッドの名前。

### <a name="method-parametercnt"></a>メソッド parameterCnt

メソッドのパラメーター数を取得します。

    public int parameterCnt()

#### <a name="return-value"></a>戻り値

メソッドのパラメーター数を取得。

### <a name="method-parameterid"></a>メソッド parameterId

指定されたパラメータの ID を取得します。

    public int parameterId(int variableNumber)

#### <a name="parameters"></a>パラメーター

variableNumber  
メソッドのパラメーター リストへの 1 から始まるインデックス。

#### <a name="return-value"></a>戻り値

指定されたパラメーターの ID。

### <a name="method-parametername"></a>メソッド parameterName

指定されたパラメータの名前を取得します。

    public str parameterName(int variableNumber)

#### <a name="parameters"></a>パラメーター

variableNumber  
メソッドのパラメーター リストへの 1 から始まるインデックス。

#### <a name="return-value"></a>戻り値

指定されたパラメーターの名前。

### <a name="method-parameteroptional"></a>メソッド parameterOptional

メソッドの指定されたパラメーターが省略可能かどうかを示します。

    public boolean parameterOptional(int variableNumber)

#### <a name="parameters"></a>パラメーター

variableNumber  
メソッドのパラメーター リストへの 1 から始まるインデックス。

#### <a name="return-value"></a>戻り値

パラメーターがオプションである場合は true。それ以外の場合は false。

### <a name="method-parametertype"></a>メソッド parameterType

    public Types parameterType(int variableNumber)

#### <a name="parameters"></a>パラメーター

variableNumber  

#### <a name="return-value"></a>戻り値

### <a name="method-parentid"></a>メソッド parentId

メソッドを所有する親の ID を取得します。

    public int parentId()

#### <a name="return-value"></a>戻り値

メソッドを所有する親の ID。

### <a name="method-propertyhelp"></a>メソッド propertyHelp

メソッドに関連付けられているプロパティのヘルプ文字列を取得します。

    public str propertyHelp()

#### <a name="return-value"></a>戻り値

メソッドに関連付けられているプロパティのヘルプ文字列。ヘルプ文字列がない場合は、空の文字列。

#### <a name="remarks"></a>備考

このメソッドは、DictMethod :: propertyMethod メソッドを呼び出して、メソッドがプロパティ メソッドかどうかを判定します。

### <a name="method-propertymethod"></a>メソッド propertyMethod

メソッドがプロパティ メソッドかどうかを示します。

    public NoYes propertyMethod()

#### <a name="return-value"></a>戻り値

メソッドがプロパティ メソッドである場合は NoYes::No 列挙値、それ以外の場合は NoYes::Yes 列挙値。

### <a name="method-returnid"></a>メソッド returnId

値を返すメソッドについて、拡張データ型やクラスなどの特定の戻り値のデータ型の ID を指定します。

    public int returnId()

#### <a name="return-value"></a>戻り値

戻り値のデータ型の ID。データ型に ID がない場合またはメソッドが値を返さない場合は 0 (ゼロ) です。

### <a name="method-returntype"></a>メソッド returnType

メソッドの戻り値の型を指定します。

    public Types returnType()

#### <a name="return-value"></a>戻り値

メソッドの戻り値を示すタイプ列挙値。

#### <a name="remarks"></a>備考

表示される値は次のとおりです。

-   AnyType
-   BLOB
-   クラス
-   コンテナー
-   日
-   日時
-   列挙
-   グリッド
-   Int64
-   整数
-   実数
-   レコード
-   RString
-   文字列
-   UserType
-   VarString
-   無効

### <a name="method-runmode"></a>メソッド runMode

メソッドが実行される場所を指定します。

    public ClassRunMode runMode()

#### <a name="return-value"></a>戻り値

メソッドが実行される場所を示す ClassRunMode 列挙値。

#### <a name="remarks"></a>備考

表示される値は次のとおりです。

-   呼び出された
-   クライアント
-   ClientorServer
-   サーバー

### <a name="method-varcnt"></a>メソッド varCnt

メソッドの変数の数を取得します。

    public int varCnt()

#### <a name="return-value"></a>戻り値

メソッドのローカル変数と継承変数の数。

### <a name="method-varname"></a>メソッド varName

指定された変数の名前を取得します。

    public str varName(int variableNumber)

#### <a name="parameters"></a>パラメーター

variableNumber  
メソッドの変数リストへの 1 から始まるインデックス。

#### <a name="return-value"></a>戻り値

指定された変数の名前。

### <a name="method-setmethod"></a>メソッド setMethod

MemberFunction クラスのインスタンスを使用して Finance and Operations アプリケーション オブジェクト ツリー (AOT) 内のノードのアプリケーション オブジェクト タイプを指定します。

    public void setMethod(MemberFunction method)

#### <a name="parameters"></a>パラメーター

メソッド  
AOT 内のノードを表す MemberFunction クラスのインスタンス。

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(UtilElementType utilType, int id, str name)

#### <a name="parameters"></a>パラメーター

utilType  

<!-- -->

id  

<!-- -->

名前  

## <a name="class-dictrelation"></a>クラス DictRelation
    class DictRelation extends Object

DictRelation クラスは、テーブルのディクショナリ関係の管理に使用できます。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

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

### <a name="method-cardinality"></a>メソッド Cardinality

基数値を取得します。

    public Cardinality Cardinality()

#### <a name="return-value"></a>戻り値

基数値。

### <a name="method-createnavigationpropertymethods"></a>メソッド createNavigationPropertyMethods

    public boolean createNavigationPropertyMethods()

#### <a name="return-value"></a>戻り値

### <a name="method-edtrelation"></a>メソッド EDTRelation

拡張データ型 (EDT) の関係の状態を取得します。

    public boolean EDTRelation()

#### <a name="return-value"></a>戻り値

EDT 関係が使用可能かどうかを示すブール値。

### <a name="method-entityrelationshiprole"></a>メソッド entityRelationshipRole

エンティティ リレーションシップ ロールの名前を取得します。

    public str entityRelationshipRole()

#### <a name="return-value"></a>戻り値

エンティティ リレーションシップ ロールの名前。

### <a name="method-entityrelationshiprolelabelid"></a>メソッド entityRelationshipRoleLabelId

エンティティ関係ロールの名前のラベル ID を取得します。

    public str entityRelationshipRoleLabelId()

#### <a name="return-value"></a>戻り値

エンティティ リレーションシップ ロールのラベル ID。

### <a name="method-externtable"></a>メソッド externTable

関係のために使用する外部テーブルの ID を返します。

    public TableId externTable()

#### <a name="return-value"></a>戻り値

関係に使用される外部テーブルの ID。関係がまだ読み込まれていない場合は 0 (ゼロ)。

#### <a name="examples"></a>例

次の例は、外部テーブルの ID の取得を示しています。

    Dictionary dict; 
    DictRelation dr; 
    int i;  
    dict = new Dictionary(); 
    dr = new DictRelation(dict.tableName2Id("CustTable")); 
    // Load a relation by name 
    dr.loadNameRelation("CompanyData");  // Also returns the external table ID. 
    print "The external table ID is: " + int2str(dr.externTable());

### <a name="method-isselflink"></a>メソッド isSelfLink

リレーションが自己リンクされているかどうかを検証します。

    public boolean isSelfLink()

#### <a name="return-value"></a>戻り値

リレーションが自己リンクである場合は true。それ以外の場合は、false。

### <a name="method-lineexterntablevalue"></a>メソッド lineExternTableValue

特定の行の外部テーブル値を取得します。

    public int lineExternTableValue(int lineNumber)

#### <a name="parameters"></a>パラメーター

lineNumber  

#### <a name="return-value"></a>戻り値

外部テーブル値。

### <a name="method-lines"></a>メソッド lines

リレーションの明細行の数を取得します。

    public int lines()

#### <a name="return-value"></a>戻り値

ラインの数。

### <a name="method-linesourceedt"></a>メソッド lineSourceEDT

特定のテーブル行のソース EDT 値を取得します。

    public int lineSourceEDT(int lineNumber)

#### <a name="parameters"></a>パラメーター

lineNumber  

#### <a name="return-value"></a>戻り値

ソース EDT 値。

### <a name="method-linesubtype"></a>メソッド lineSubType

指定されたテーブル行のサブタイプを取得します。

    public RelationshipSubType lineSubType(int lineNumber)

#### <a name="parameters"></a>パラメーター

lineNumber  

#### <a name="return-value"></a>戻り値

指定されたテーブル行のサブタイプ。

### <a name="method-linetablevalue"></a>メソッド lineTableValue

特定のテーブル行の値を取得します。

    public int lineTableValue(int lineNumber)

#### <a name="parameters"></a>パラメーター

lineNumber  

#### <a name="return-value"></a>戻り値

テーブル行の値。

### <a name="method-linetype"></a>メソッド lineType

指定されたテーブル行のリレーション タイプを取得します。

    public TableRelation lineType(int lineNumber)

#### <a name="parameters"></a>パラメーター

lineNumber  

#### <a name="return-value"></a>戻り値

指定された行のテーブルのリレーション タイプ。

### <a name="method-loadfieldrelation"></a>メソッド loadFieldRelation

フィールド ID で指定されている関係を読み込みます。

    public TableId loadFieldRelation(FieldId fieldId, [TableScope tableScope], [Common record], [boolean isLookup])

#### <a name="parameters"></a>パラメーター

fieldId  

<!-- -->

tableScope  

<!-- -->

記録  

<!-- -->

isLookup  

#### <a name="return-value"></a>戻り値

関係のテーブルの ID。メソッドが失敗した場合は null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。

### <a name="method-loadnamerelation"></a>メソッド loadNameRelation

指定された名前の関係を読み込みます。

    public TableId loadNameRelation(str name)

#### <a name="parameters"></a>パラメーター

名前  

#### <a name="return-value"></a>戻り値

テーブル リレーションのテーブル ID。

### <a name="method-loadtablerelation"></a>メソッド loadTableRelation

テーブル リレーションを読み込みます。

    public TableId loadTableRelation(TableId tableId, [TableScope tableScope], [Common record])

#### <a name="parameters"></a>パラメーター

tableId  

<!-- -->

tableScope  

<!-- -->

記録  

#### <a name="return-value"></a>戻り値

テーブル リレーションのテーブル ID。

### <a name="method-navigationpropertynameoverride"></a>メソッド navigationPropertyNameOverride

    public str navigationPropertyNameOverride()

#### <a name="return-value"></a>戻り値

### <a name="method-relatedtablecardinality"></a>メソッド RelatedTableCardinality

関連テーブルの基数を取得します。

    public RelatedTableCardinality RelatedTableCardinality()

#### <a name="return-value"></a>戻り値

関連テーブルの基数。

### <a name="method-relatedtablerole"></a>メソッド RelatedTableRole

関連テーブルのロール名を取得します。

    public str RelatedTableRole()

#### <a name="return-value"></a>戻り値

関連テーブルのロール名。

### <a name="method-relationshiptype"></a>メソッド relationshipType

関係タイプを取得します。

    public RelationshipType relationshipType()

#### <a name="return-value"></a>戻り値

リレーションシップ タイプ。

### <a name="method-role"></a>メソッド Role

ロール名を取得します。

    public str Role()

#### <a name="return-value"></a>戻り値

ロール名。

### <a name="method-table"></a>メソッド table

リレーションのテーブル ID を返します。

    public TableId table()

#### <a name="return-value"></a>戻り値

リレーションのテーブル ID

#### <a name="examples"></a>例

次の例は、リレーションのテーブル ID の取得を示しています。

    Dictionary dict; 
    DictRelation dr; 
    dict = new Dictionary(); 
    dr = new DictRelation(dict.tableName2Id("CustTable")); 
    print dr.table();

### <a name="method-usedefaultrolenames"></a>メソッド useDefaultRoleNames

    public boolean useDefaultRoleNames()

#### <a name="return-value"></a>戻り値

### <a name="method-validate"></a>メソッド validate

リレーションを検証します。

    public boolean validate()

#### <a name="return-value"></a>戻り値

リレーションが有効である場合は true。それ以外の場合は、false。

### <a name="method-issurrogateforeignkeyrelation"></a>メソッド isSurrogateForeignKeyRelation

代理外部キーのリレーションがあるかどうかを検証します。

    public static boolean isSurrogateForeignKeyRelation(TableId tableId, str relationName)

#### <a name="parameters"></a>パラメーター

tableId  

<!-- -->

relationName  

#### <a name="return-value"></a>戻り値

代理外部キー リレーションがある場合は true。それ以外の場合は、false。

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(int id, [UtilElementType Util_Element_Type], [int index])

#### <a name="parameters"></a>パラメーター

id  
リレーション インデックス (オプション)。 既定値は 1 です。

<!-- -->

Util\_Element\_Type  
リレーション インデックス (オプション)。 既定値は 1 です。

<!-- -->

指数  
リレーション インデックス (オプション)。 既定値は 1 です。

## <a name="class-dicttable"></a>クラス DictTable
    class DictTable extends Object

DictTable クラスは、テーブルに関する情報を提供します。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

次の例は、DictTable クラスのインスタンスを作成して、テーブル内のデータが会社ごとに格納されているかどうかを判断する方法を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        print (strfmt("The table is saved on a %1 basis.", dt.dataPrCompany() ? 
                          "per company" : "global")); 
    }

### <a name="methods"></a>メソッド

| 方法                                                                                                                                      | 説明                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean doesMethodExist(str name)                                                                                                    | 指定されたメソッドがテーブルに存在するかどうかをチェックします。                                                                                                                        |
| public AOSAuthorization AOSAuthSetting()                                                                                                    | ユーザーのアクセス許可に応じて、ユーザーがテーブルで実行できる操作の種類を指定する AOSAuthorization システム列挙値を取得します。 |
| public RecordCacheLevel cacheLookup()                                                                                                       | テーブルのレコード キャッシュ レベルを返します。                                                                                                                             |
| public int cacheSize()                                                                                                                      | テーブルのキャッシュ サイズをレコードの数で返します。                                                                                                           |
| public AnyType callObject(str methodName, Common Called, VarArg )                                                                           | テーブルの指定されたオブジェクトのメソッドを呼び出します。                                                                                                                            |
| public AnyType callStatic(str methodName, VarArg )                                                                                          | テーブルの指定された静的メソッドを呼び出します。                                                                                                                            |
| public IndexId clusterIndex(\[boolean asDefinedInAOT\])                                                                                     | テーブルのクラスター化されたインデックスの ID を返します。                                                                                                                      |
| public ConfigurationKeyId configurationKeyId()                                                                                              | テーブルのコンフィギュレーション キーの ID を返します。                                                                                                                    |
| public boolean dataPerPartition()                                                                                                           | テーブルのデータがパーティション単位で保存されるかどうかと、テーブルの SaveDataPerPartition プロパティに対応するかどうかを示す値を返します。        |
| public boolean dataPrCompany()                                                                                                              | テーブルのデータが会社単位で保存されるかどうかと、テーブルの SaveDataPerCompany プロパティに対応するかどうかを示す値を返します。            |
| public int deleteActionCnt()                                                                                                                | テーブルの削除アクションの数を取得します。                                                                                                                     |
| public str deleteActionRelation(int cnt)                                                                                                    |                                                                                                                                                                           |
| public TableId deleteActionTableId(int cnt)                                                                                                 | インデックスで指定されているテーブルの削除アクションのテーブル ID を返します。                                                                                            |
| public int deleteActionType(int cnt)                                                                                                        | テーブルの削除アクションの種類を取得します。                                                                                                                        |
| public str developerDocumentation()                                                                                                         |                                                                                                                                                                           |
| public str developerDocumentationLabelId()                                                                                                  |                                                                                                                                                                           |
| public boolean enabled()                                                                                                                    | テーブルが有効かどうかを示す値を返します。                                                                                                              |
| public boolean enforceRelationRules()                                                                                                       |                                                                                                                                                                           |
| public EntityRelationshipType entityRelationshipType()                                                                                      |                                                                                                                                                                           |
| public List extendedBy(\[boolean allLevels\])                                                                                               |                                                                                                                                                                           |
| public TableId extends()                                                                                                                    | 基本テーブルのテーブル ID を返します。                                                                                                                                     |
| public int fieldCnt(\[TableScope tableScope\])                                                                                              | テーブルのフィールドの数を返します。                                                                                                                                 |
| public FieldId fieldCnt2Id(int cnt, \[TableScope tableScope\])                                                                              | インデックスで指定されるフィールドのフィールド ID を返します。                                                                                                          |
| public str fieldGroup(int FieldGroupNumber, \[TableScope tableScope\])                                                                      | インデックスで指定されるフィールド グループの名前を返します。                                                                                                             |
| public int fieldGroupCnt(\[TableScope tableScope\])                                                                                         | テーブルのフィールド グループの数を返します。                                                                                                                         |
| public str fieldName(FieldId fieldId, \[DbBackend db\], \[int arrayindex\], \[FieldNameGenerationMode generationMode\], \[str tableAlias\]) | フィールド ID で指定されるフィールドの名前を返します。                                                                                                              |
| public FieldId fieldName2Id(str name)                                                                                                       | 名前で指定されるフィールドのフィールド ID を返します。                                                                                                                |
| public FieldId fieldNext(FieldId fieldId, \[TableScope tableScope\])                                                                        | テーブルのフィールド反復処理中に、次のフィールド ID の値を返します。                                                                                             |
| public DictField fieldObject(FieldId fieldId)                                                                                               | フィールド ID で指定されているフィールドの DictField クラスのインスタンスを作成します。                                                                                   |
| public IndexId fieldOrigin2Id(Guid fieldOrigin, \[TableScope tableScope\])                                                                  |                                                                                                                                                                           |
| public str fieldSqlDefault(FieldId fieldId)                                                                                                 | フィールド ID で指定されているフィールドの SQL 既定値を返します。                                                                                                |
| public str formRef(\[boolean searchBaseTables\])                                                                                            | テーブルの既定のフォームの名前を返します。                                                                                                                       |
| public container getCountryRegionCodes()                                                                                                    |                                                                                                                                                                           |
| public FieldId getCountryRegionContextField()                                                                                               |                                                                                                                                                                           |
| public FieldId getValidTimeStateValidFromFieldId()                                                                                          |                                                                                                                                                                           |
| public FieldId getValidTimeStateValidToFieldId()                                                                                            |                                                                                                                                                                           |
| public boolean hasRecidIdx()                                                                                                                | テーブルのレコード ID インデックスが有効かどうかを示す値を返します。                                                                                      |
| public boolean hasSurrogateKey()                                                                                                            |                                                                                                                                                                           |
| public TableId id()                                                                                                                         | テーブルの ID を返します。                                                                                                                                              |
| public int indexCnt()                                                                                                                       | テーブルのインデックスの数を返します。                                                                                                                              |
| public IndexId indexCnt2Id(int cnt)                                                                                                         |                                                                                                                                                                           |
| public str indexName(IndexId indexId, \[DbBackend db\])                                                                                     | indexId パラメーターで指定された形式のインデックスの名前を返します。                                                                                                  |
| public IndexId indexName2Id(str name)                                                                                                       | 名前で指定されているインデックスの ID を返します。                                                                                                                     |
| public IndexId indexNext(IndexId id)                                                                                                        | テーブルのインデックス反復処理中に、次のインデックス ID の値を返します。                                                                                            |
| public DictIndex indexObject(IndexId indexId)                                                                                               | ID で指定されているインデックスの DictTable クラスのインスタンスを作成します。                                                                                         |
| public IndexId indexUnique()                                                                                                                | テーブルの一意のインデックスの ID を返します。                                                                                                                         |
| public FieldId instanceRelationType()                                                                                                       |                                                                                                                                                                           |
| public boolean isAbstract()                                                                                                                 | このテーブルが抽象かどうかを示します。                                                                                                                                 |
| public boolean isBaseData()                                                                                                                 | テーブル コンテンツが基本データであるかどうかを示します。                                                                                                                         |
| public boolean isDefaultData()                                                                                                              | テーブルが既定のデータを含むかどうかを示します。                                                                                                                        |
| public boolean isDerivedFrom(TableName baseTableName)                                                                                       | 1 つのテーブル タイプが別から派生しているかどうかを示します。                                                                                                                    |
| public boolean isMap()                                                                                                                      | テーブルがマップであるかどうかを示します。                                                                                                                                     |
| public boolean isSql()                                                                                                                      | テーブルが SQL テーブルであるかどうかを示します。                                                                                                                              |
| public boolean isSystemTable()                                                                                                              | テーブルがシステム テーブルであるかどうかを示します。                                                                                                                            |
| public boolean isTempDb()                                                                                                                   |                                                                                                                                                                           |
| public boolean isTmp()                                                                                                                      | テーブルが一時テーブルであるかどうかを示します。                                                                                                                         |
| public boolean isUnionAllView()                                                                                                             |                                                                                                                                                                           |
| public boolean isValidTimeStateTable()                                                                                                      |                                                                                                                                                                           |
| public boolean isView()                                                                                                                     | テーブルがビューであるかどうかを示します。                                                                                                                                    |
| public str label()                                                                                                                          | テーブルのラベル テキストを返します。                                                                                                                                     |
| public str labelDefined()                                                                                                                   | テーブルの label プロパティの値を返します。                                                                                                                    |
| public str listPageRef(\[boolean searchBaseTables\])                                                                                        |                                                                                                                                                                           |
| public Common makeRecord()                                                                                                                  | テーブルの空白のレコードを作成します。                                                                                                                                     |
| public AccessType maxAccessMode()                                                                                                           | AOT 内で設定されているとおり、テーブルの MaxAccessMode プロパティの値を返します。                                                                                           |
| public str name(\[DbBackend db\], \[boolean pseudoname\])                                                                                   | テーブル名を取得します。                                                                                                                                          |
| public str objectMethod(int methodNumber, \[TableScope tableScope\])                                                                        | インデックスで指定されるインスタンス メソッドの名前を返します。                                                                                                        |
| public int objectMethodCnt(\[TableScope tableScope\])                                                                                       | テーブルのインスタンス メソッドの数を返します。                                                                                                                     |
| public DictMethod objectMethodObject(int methodNumber, \[TableScope tableScope\])                                                           | インデックスにより指定されているオブジェクト メソッドの MethodInfo クラスのインスタンスを返します。                                                                              |
| public DictTableMap mapObject(int methodNumber)                                                                                             | インデックスで指定されているマッピングに対する \[t: DictTableMap\] クラスのインスタンスを作成します。                                                                            |
| public int mapCnt()                                                                                                                         | この DictTable インスタンスにより指定されているマップの使用可能なテーブル マッピングの数を返します。                                                                   |
| public boolean occEnabled()                                                                                                                 | テーブルに対してオプティミスティック同時実行モードが有効になっているかどうかを示します。                                                                                           |
| public IndexId primaryIndex(\[boolean asDefinedInAOT\])                                                                                     | テーブルのプライマリ インデックスの ID を返します。                                                                                                                        |
| public FieldId primaryKeyField()                                                                                                            | テーブルの主キーに使用されているフィールドの ID を返します。                                                                                                |
| public str relation(int RelationNumber, \[TableScope tableScope\])                                                                          | インデックスで指定される関係の名前を返します。                                                                                                                |
| public int relationCnt(\[TableScope tableScope\])                                                                                           | テーブルの関係の数を返します。                                                                                                                            |
| public IndexId replacementKey()                                                                                                             |                                                                                                                                                                           |
| public str reportRef()                                                                                                                      | テーブルの既定のレポートの名前を返します。                                                                                                                     |
| public AccessType rights(\[boolean ignoreContext\])                                                                                         | テーブルに指定されている、現在のユーザーのアクセス権を返します。                                                                                            |
| public SecurityKeyId securityKeyId()                                                                                                        | テーブルのセキュリティ キーの ID を返します。                                                                                                                         |
| public str singularLabel(\[boolean labelTranslation\])                                                                                      |                                                                                                                                                                           |
| public str staticMethod(int methodNumber)                                                                                                   | インデックスで指定される静的メソッドの名前を返します。                                                                                                           |
| public int staticMethodCnt()                                                                                                                | テーブルの静的メソッドの数を返します。                                                                                                                       |
| public DictMethod staticMethodObject(int methodNumber)                                                                                      | インデックスにより指定されている静的メソッドの MethodInfo クラスのインスタンスを返します。                                                                               |
| public boolean supportInheritance()                                                                                                         |                                                                                                                                                                           |
| public TableGroup tableGroup()                                                                                                              | テーブルのテーブル グループを返します。                                                                                                                                      |
| public TableType tableType()                                                                                                                | テーブルのタイプを示します。                                                                                                                                          |
| public FieldId titleField1(\[boolean includeBaseTables\], \[boolean extendedFieldId\])                                                      | テーブルの titleField1 プロパティを表すフィールドの ID を返します。                                                                                        |
| public FieldId titleField2(\[boolean includeBaseTables\], \[boolean extendedFieldId\])                                                      | テーブルの titleField2 プロパティを表すフィールドの ID を返します。                                                                                        |
| public boolean validRelationship()                                                                                                          |                                                                                                                                                                           |
| public boolean visible()                                                                                                                    | テーブルが表示できるかどうかを判定します。                                                                                                                                  |
| ::public static DictTable construct(str tableName)                                                                                          |                                                                                                                                                                           |
| ::public static RecId getRelationTypeFromTableName(TableName tableName)                                                                     |                                                                                                                                                                           |
| ::public static TableName getTableNameFromRelationType(RecId relationType)                                                                  |                                                                                                                                                                           |
| ::public static Common createRecord(str tableName)                                                                                          |                                                                                                                                                                           |
| public void reloadSecurity()                                                                                                                | テーブルの機能キー システムを再読み込みします。                                                                                                                             |
| public void new(TableId tableId)                                                                                                            | Object クラスの新しいインスタンスを初期化します。                                                                                                                           |
| public void reindex()                                                                                                                       | テーブルのインデックスの再作成を実行します。                                                                                                                                          |

### <a name="method-doesmethodexist"></a>メソッド doesMethodExist

指定されたメソッドがテーブルに存在するかどうかをチェックします。

    public boolean doesMethodExist(str name)

#### <a name="parameters"></a>パラメーター

名前  

#### <a name="return-value"></a>戻り値

指定メソッドがテーブル上に存在する場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

この API は、メソッドが正常にコンパイルされているかどうかを確認せずに、メソッドがテーブルに存在するかどうかを確認するために推奨される方法です。

### <a name="method-aosauthsetting"></a>メソッド AOSAuthSetting

ユーザーのアクセス許可に応じて、ユーザーがテーブルで実行できる操作の種類を指定する AOSAuthorization システム列挙値を取得します。

    public AOSAuthorization AOSAuthSetting()

#### <a name="return-value"></a>戻り値

AOSAuthorization システム列挙値です。

#### <a name="remarks"></a>備考

AOSAuthorization::None 値は、承認チェックが実行されないことを示します。 テーブルの AOSAuthorization プロパティを設定するには、テーブルのプロパティを使用します。 Finance and Operations のアプリケーション オブジェクト ツリー (AOT) で、テーブルを右クリックしてからプロパティをクリックしてテーブルのプロパティにアクセスします。

#### <a name="examples"></a>例

次の例は、AOSAuthSetting メソッドの呼び出しを示しています。

    static public void Main(Args _args) 
    { 
        DictTable dt; 
        AOSAuthorization a; 
        dt = new DictTable(tablenum(CustTable)); 
        a = dt.AOSAuthSetting(); 
    }

### <a name="method-cachelookup"></a>メソッド cacheLookup

テーブルのレコード キャッシュ レベルを返します。

    public RecordCacheLevel cacheLookup()

#### <a name="return-value"></a>戻り値

テーブルのレコード キャッシュ レベルを示す RecordCacheLevel 値。

#### <a name="examples"></a>例

次の例は、テーブルのキャッシュ レベルの取得を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        print dt.cacheLookup(); 
    }

### <a name="method-cachesize"></a>メソッド cacheSize

テーブルのキャッシュ サイズをレコードの数で返します。

    public int cacheSize()

#### <a name="return-value"></a>戻り値

テーブルのキャッシュ サイズです。

#### <a name="examples"></a>例

次の例では、テーブルのキャッシュ サイズを取得します。

    DictTable dt; 
    dt = new DictTable(tablenum(SysUserInfo)); 
    if (dt) 
    { 
         print strfmt("Cache size: %1", dt.cacheSize()); 
    }

### <a name="method-callobject"></a>メソッド callObject

テーブルの指定されたオブジェクトのメソッドを呼び出します。

    public AnyType callObject(str methodName, Common Called, VarArg )

#### <a name="parameters"></a>パラメーター

methodName  

<!-- -->

呼び出された  

<!-- -->



#### <a name="return-value"></a>戻り値

methodName パラメーターへの呼び出しの結果。

#### <a name="remarks"></a>備考

攻撃者が callObject メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

#### <a name="examples"></a>例

この例では、SysUserLog テーブルの SysUserLog.onlineTime 静的メソッドを呼び出し、呼び出しから返された値を出力します。

    { 
        Dicttable         dictTable; 
        int               onlineTime; 
        Common            common; 
        str               resultOutput; 
        ExecutePermission perm; 
        perm = new ExecutePermission(); 
        dictTable= new DictTable(tablenum(SysUserLog)); 
        if (dictTable != null) 
        { 
            common = dictTable.makeRecord(); 
            // Grants permission to execute the 
            // DictTable.callObject method. DictTable.callObject runs 
            // under code access security. 
            perm.assert(); 
            onlineTime   = dictTable.callObject("onlineTime", common); 
            resultOutput = strfmt("User online time is %1", onlineTime); 
            print resultOutput; 
            pause; 
        } 
        // Close the code access permission scope. 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-callstatic"></a>メソッド callStatic

テーブルの指定された静的メソッドを呼び出します。

    public AnyType callStatic(str methodName, VarArg )

#### <a name="parameters"></a>パラメーター

methodName  

<!-- -->



#### <a name="return-value"></a>戻り値

methodName パラメーターへの呼び出しの結果。

#### <a name="remarks"></a>備考

攻撃者がこの機能への入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、callStatic メソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

#### <a name="examples"></a>例

この例では、SysUserInfo テーブル内の SysUserInfo:find static method メソッドを呼び出し、呼び出しから返された値を callStatic メソッドに出力します。

     { 
        Dicttable   dictTable; 
        SysUserInfo userInfo; 
        str         resultOutput; 
        ExecutePermission perm; 
        perm = new ExecutePermission(); 
        // Grants permission to execute the DictTable.callStatic method. 
        // DictTable.callStatic runs under code access security. 
        perm.assert(); 
        dictTable= new DictTable(tablenum(SysUserInfo)); 
        if (dictTable != null) 
        { 
            userInfo     = dictTable.callStatic("find"); 
            resultOutput = strfmt("Current user ID is %1", userInfo.Id); 
            print resultOutput; 
            pause; 
        } 
        // Close the code access permission scope. 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-clusterindex"></a>メソッド clusterIndex

テーブルのクラスター化されたインデックスの ID を返します。

    public IndexId clusterIndex([boolean asDefinedInAOT])

#### <a name="parameters"></a>パラメーター

asDefinedInAOT  
取得するクラスター インデックスが AOT で定義されているかどうかを示す値。 true の値は、AOT で定義されたクラスター インデックスを返します。 false の値は、SQL テーブルで定義されたクラスター インデックスを返します、オプション。

#### <a name="return-value"></a>戻り値

テーブルのクラスター化されたインデックスの ID。テーブルのクラスター化されたインデックスがない場合は 0 (ゼロ)。

#### <a name="examples"></a>例

次の例は、テーブルのクラスター インデックスの取得を示しています。

    DictTable dt; 
    DictIndex di; 
    int       i; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        i = dt.clusterIndex(); 
        if (0 != i) 
        { 
            di = new DictIndex(tablenum(CustTable), i); 
            print di.name(); 
        } 
    }

### <a name="method-configurationkeyid"></a>メソッド configurationKeyId

テーブルのコンフィギュレーション キーの ID を返します。

    public ConfigurationKeyId configurationKeyId()

#### <a name="return-value"></a>戻り値

テーブルのコンフィギュレーション キーの ID。テーブルのコンフィギュレーション キーがない場合は 0 (ゼロ)。

#### <a name="examples"></a>例

次の例は、テーブルのコンフィギュレーション キー ID の取得を示しています。

    DictTable dt; 
    DictConfigurationKey dck; 
    dt = new DictTable(tablenum(AddressCountryRegionBLWI)); 
    if (dt) 
    { 
        if (0 != dt.configurationKeyId()) 
        dck = new DictConfigurationKey(dt.configurationKeyId()); 
        if (dck) 
        { 
            print (strfmt("The table's configuration key is %1.", dck.name())); 
        } 
    }

### <a name="method-dataperpartition"></a>メソッド dataPerPartition

テーブルのデータがパーティション単位で保存されるかどうかと、テーブルの SaveDataPerPartition プロパティに対応するかどうかを示す値を返します。

    public boolean dataPerPartition()

#### <a name="return-value"></a>戻り値

データがパーティション単位で保存される場合は true。それ以外の場合は false で、データはすべてのパーティションに対してグローバルに保存されます。

### <a name="method-dataprcompany"></a>メソッド dataPrCompany

テーブルのデータが会社単位で保存されるかどうかと、テーブルの SaveDataPerCompany プロパティに対応するかどうかを示す値を返します。

    public boolean dataPrCompany()

#### <a name="return-value"></a>戻り値

データが会社単位で保存される場合は true。それ以外の場合は false で、データはすべての会社に対してグローバルに保存されます。

#### <a name="examples"></a>例

次の例は、データが会社ごとに保存されるかどうかを示す値の取得を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        print (strfmt("The table is saved on a %1 basis.", dt.dataPrCompany() ? "per company" : "global")); 
    }

### <a name="method-deleteactioncnt"></a>メソッド deleteActionCnt

テーブルの削除アクションの数を取得します。

    public int deleteActionCnt()

#### <a name="return-value"></a>戻り値

テーブルの削除アクションの数。

#### <a name="examples"></a>例

次の例は、テーブルの削除アクション数の取得を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        print (strfmt("The table has %1 delete actions.", dt.deleteActionCnt())); 
    }

### <a name="method-deleteactionrelation"></a>メソッド deleteActionRelation

    public str deleteActionRelation(int cnt)

#### <a name="parameters"></a>パラメーター

cnt  

#### <a name="return-value"></a>戻り値

### <a name="method-deleteactiontableid"></a>メソッド deleteActionTableId

インデックスで指定されているテーブルの削除アクションのテーブル ID を返します。

    public TableId deleteActionTableId(int cnt)

#### <a name="parameters"></a>パラメーター

cnt  
テーブルの削除アクションのリストへの 1 から始まるインデックス。 リストは AOT の順です。

#### <a name="return-value"></a>戻り値

cnt によって指定されたテーブルの削除アクションのテーブル ID。cnt 値が有効な削除アクション索引を表していない場合は 0 (ゼロ)。

#### <a name="examples"></a>例

次の例は、deleteActionTableId メソッドを使用して CustTable テーブルの削除アクションを持つテーブルの名前を取得する方法を示しています。

    DictTable dt, dt2; 
    int       i; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        for (i=1; i <= dt.deleteActionCnt(); i++) 
        { 
            dt2 = new DictTable(dt.deleteActionTableId(i)); 
            if (dt2) 
            { 
                print dt2.name(); 
            } 
        } 
    }

### <a name="method-deleteactiontype"></a>メソッド deleteActionType

テーブルの削除アクションの種類を取得します。

    public int deleteActionType(int cnt)

#### <a name="parameters"></a>パラメーター

cnt  
テーブルの削除アクションのリストへの 1 から始まるインデックス。 リストは AOT の順です。

#### <a name="return-value"></a>戻り値

cnt パラメーターで指定されているテーブルの削除アクションのタイプを表す整数。 これは、次のテーブルの値の 1 つになります。

|     |                      |
|-----|----------------------|
| 0   | None                 |
| 1   | 重ねて表示              |
| 2   | 制限           |
| 3   | 重ねて表示 + 制限 |

#### <a name="examples"></a>例

次の例は、テーブルの削除アクションのタイプの取得を示しています。

    DictTable dt, dt2; 
    str       strDelActType; 
    int       i, nDelActType; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        for (i=1; i <= dt.deleteActionCnt(); i++) 
        { 
            dt2 = new DictTable(dt.deleteActionTableId(i)); 
            if (dt2) 
            { 
                nDelActType = dt.deleteActionType(i); 
                switch (nDelActType) 
                { 
                   case 0: 
                    strDelActType = "None"; 
                    break; 
                   case 1: 
                    strDelActType = "Cascade"; 
                    break; 
                   case 2: 
                    strDelActType = "Restricted"; 
                    break; 
                   case 3: 
                    strDelActType = "Cascade + Restricted"; 
                    break; 
                } 
                print strfmt("Delete action table: %1 Type: %2", 
                             dt2.name(), 
                             strDelActType); 
            } 
        } 
    }

### <a name="method-developerdocumentation"></a>メソッド developerDocumentation

    public str developerDocumentation()

#### <a name="return-value"></a>戻り値

### <a name="method-developerdocumentationlabelid"></a>メソッド developerDocumentationLabelId

    public str developerDocumentationLabelId()

#### <a name="return-value"></a>戻り値

### <a name="method-enabled"></a>メソッド enabled

テーブルが有効かどうかを示す値を返します。

    public boolean enabled()

#### <a name="return-value"></a>戻り値

テーブルが有効である場合は true。それ以外の場合は、false。

#### <a name="examples"></a>例

次の例は、テーブルが有効化されているかどうかを示す値の取得を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        print (strfmt("The table is %1.", dt.enabled() ? "enabled" : "not enabled")); 
    }

### <a name="method-enforcerelationrules"></a>メソッド enforceRelationRules

    public boolean enforceRelationRules()

#### <a name="return-value"></a>戻り値

### <a name="method-entityrelationshiptype"></a>メソッド entityRelationshipType

    public EntityRelationshipType entityRelationshipType()

#### <a name="return-value"></a>戻り値

### <a name="method-extendedby"></a>メソッド extendedBy

    public List extendedBy([boolean allLevels])

#### <a name="parameters"></a>パラメーター

allLevels  

#### <a name="return-value"></a>戻り値

### <a name="method-extends"></a>メソッド extends

基本テーブルのテーブル ID を返します。

    public TableId extends()

#### <a name="return-value"></a>戻り値

ベース テーブルのテーブル ID

### <a name="method-fieldcnt"></a>メソッド fieldCnt

テーブルのフィールドの数を返します。

    public int fieldCnt([TableScope tableScope])

#### <a name="parameters"></a>パラメーター

tableScope  

#### <a name="return-value"></a>戻り値

テーブルのフィールドの数。

#### <a name="examples"></a>例

次の例は、テーブルのフィールド数の取得を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        print (strfmt("The table has %1 fields.", dt.fieldCnt())); 
    }

### <a name="method-fieldcnt2id"></a>メソッド fieldCnt2Id

インデックスで指定されるフィールドのフィールド ID を返します。

    public FieldId fieldCnt2Id(int cnt, [TableScope tableScope])

#### <a name="parameters"></a>パラメーター

cnt  

<!-- -->

tableScope  

#### <a name="return-value"></a>戻り値

インデックスで指定されたフィールドのフィールド ID。

#### <a name="examples"></a>例

次の例は、インデックスによるテーブルのフィールドの取得を示しています。

    DictTable dt; 
    int       i, fId, tId; 
    DictField df; 
    str       strFieldName; 
    tId = tablenum(CustTable); 
    dt = new DictTable(tId); 
    if (dt) 
    { 
        for (i=1; i <= dt.fieldCnt(); i++) 
        { 
            fId = dt.fieldCnt2Id(i); 
            df = new DictField(tId, fId); 
            strFieldName = (df ? df.name() : ""); 
            print(strfmt("%1) %2 %3", i, fId, strFieldName)); 
        } 
    }

### <a name="method-fieldgroup"></a>メソッド fieldGroup

インデックスで指定されるフィールド グループの名前を返します。

    public str fieldGroup(int FieldGroupNumber, [TableScope tableScope])

#### <a name="parameters"></a>パラメーター

FieldGroupNumber  

<!-- -->

tableScope  

#### <a name="return-value"></a>戻り値

FieldGroupNumber パラメーターで指定されるフィールド グループの名前。

#### <a name="examples"></a>例

次の例は、テーブルのフィールド グループの名前の取得を示しています。

    DictTable dt; 
    int       i; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        for (i =1; i <= dt.fieldGroupCnt(); i++) 
        { 
            print (dt.fieldGroup(i)); 
        } 
    }

### <a name="method-fieldgroupcnt"></a>メソッド fieldGroupCnt

テーブルのフィールド グループの数を返します。

    public int fieldGroupCnt([TableScope tableScope])

#### <a name="parameters"></a>パラメーター

tableScope  

#### <a name="return-value"></a>戻り値

テーブルのフィールド グループの数。

#### <a name="examples"></a>例

次の例は、テーブルのフィールド グループ数の取得を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        print (strfmt("The table has %1 field groups.", dt.fieldGroupCnt())); 
    }

### <a name="method-fieldname"></a>メソッド fieldName

フィールド ID で指定されるフィールドの名前を返します。

    public str fieldName(FieldId fieldId, [DbBackend db], [int arrayindex], [FieldNameGenerationMode generationMode], [str tableAlias])

#### <a name="parameters"></a>パラメーター

fieldId  
テーブルのエイリアスの名前 (省略可能)。

<!-- -->

db  
テーブルのエイリアスの名前 (省略可能)。

<!-- -->

arrayindex  
テーブルのエイリアスの名前 (省略可能)。

<!-- -->

generationMode  
テーブルのエイリアスの名前 (省略可能)。

<!-- -->

tableAlias  
テーブルのエイリアスの名前 (省略可能)。

#### <a name="return-value"></a>戻り値

フィールド ID で指定されるフィールド グループの名前。

#### <a name="remarks"></a>備考

Db が指定されていない場合は、DbBackend::Native オブジェクトが使用されます。

#### <a name="examples"></a>例

次の例は、フィールド ID で指定されたテーブルのフィールド名の取得を示しています。

    DictTable dt; 
    int       i, tId, fId; 
    tId = tablenum(CustTable); 
    dt = new DictTable(tId); 
    if (dt) 
    { 
        for (i=1; i <= dt.fieldCnt(); i++) 
        { 
            fId = dt.fieldCnt2Id(i); 
            print(strfmt("%1) %2 %3", i, fId, dt.fieldName(fId))); 
        } 
    }

### <a name="method-fieldname2id"></a>メソッド fieldName2Id

名前で指定されるフィールドのフィールド ID を返します。

    public FieldId fieldName2Id(str name)

#### <a name="parameters"></a>パラメーター

名前  
フィールド ID が取得されているフィールドの名前。

#### <a name="return-value"></a>戻り値

name パラメーターで指定されたフィールドのフィールド ID。name がテーブルの有効なフィールド名を表していない場合は 0 (ゼロ) です。

#### <a name="examples"></a>例

次の例は、フィールド名によるフィールド ID の取得を示しています。

    DictTable dt; 
    fieldId   fId; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        fId = dt.fieldName2Id("Pager"); 
        // Use the field ID as needed. 
        // This example merely prints out the field ID. 
        print (strfmt("fId: %1", fId)); 
    }

### <a name="method-fieldnext"></a>メソッド fieldNext

テーブルのフィールド反復処理中に、次のフィールド ID の値を返します。

    public FieldId fieldNext(FieldId fieldId, [TableScope tableScope])

#### <a name="parameters"></a>パラメーター

fieldId  

<!-- -->

tableScope  

#### <a name="return-value"></a>戻り値

テーブルのフィールド反復における次のフィールドの ID。反復処理するフィールドがない場合は 0 (ゼロ)。

#### <a name="remarks"></a>備考

フィールドの反復を開始するには、fieldId パラメーターの値を 0 (ゼロ) に評価し、その反復の後続の呼び出しには戻り値を使用する必要があります。

#### <a name="examples"></a>例

次の例では、テーブルのフィールドを反復処理します。

    DictTable   dt; 
    DictField   df; 
    int         counter; 
    counter = 0; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        counter = dt.fieldNext(counter); 
        while (counter) 
        { 
            df = dt.fieldObject(counter); 
            if (df) 
            { 
                print strfmt("ID: %1 Name: %2", 
                             df.id(), 
                             df.name() ); 
            } 
            counter = dt.fieldNext(counter); 
        } 
    }

### <a name="method-fieldobject"></a>メソッド fieldObject

フィールド ID で指定されているフィールドの DictField クラスのインスタンスを作成します。

    public DictField fieldObject(FieldId fieldId)

#### <a name="parameters"></a>パラメーター

fieldId  
作成するフィールドの ID。

#### <a name="return-value"></a>戻り値

fieldId パラメーターで指定されたフィールドの DictField オブジェクト; null、Nothing、nullptr、unit、オブジェクトを作成できない場合は null 参照 (Visual Basic にはなし)。

#### <a name="examples"></a>例

次の例は、テーブル内のフィールドの DictField オブジェクトを作成する方法を示しています。

    DictTable dt; 
    DictField df; 
    int       i; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        for (i=1; i <= dt.fieldCnt(); i++) 
        { 
          df = dt.fieldObject(dt.fieldCnt2Id(i)); 
          if (df) 
          { 
              print df.name(); 
          } 
        } 
    }

### <a name="method-fieldorigin2id"></a>メソッド fieldOrigin2Id

    public IndexId fieldOrigin2Id(Guid fieldOrigin, [TableScope tableScope])

#### <a name="parameters"></a>パラメーター

fieldOrigin  

<!-- -->

tableScope  

#### <a name="return-value"></a>戻り値

### <a name="method-fieldsqldefault"></a>メソッド fieldSqlDefault

フィールド ID で指定されているフィールドの SQL 既定値を返します。

    public str fieldSqlDefault(FieldId fieldId)

#### <a name="parameters"></a>パラメーター

fieldId  
SQL の既定のデータが取得されるフィールドの ID。

#### <a name="return-value"></a>戻り値

fieldId パラメーターで指定されたフィールドの SQL 既定値を表す文字列、フィールドに SQL のデフォルト値がない場合、またはテーブルが SQL テーブルではない場合は空の文字列。

### <a name="method-formref"></a>メソッド formRef

テーブルの既定のフォームの名前を返します。

    public str formRef([boolean searchBaseTables])

#### <a name="parameters"></a>パラメーター

searchBaseTables  

#### <a name="return-value"></a>戻り値

テーブルの既定のフォームの名前。

#### <a name="remarks"></a>備考

AOT に、テーブルの FormRef プロパティの値が表示されない場合、テーブルの既定のフォームの名前は、テーブルの名前と同じであると見なされます。 この場合、このメソッドは空の文字列を返しません。

#### <a name="examples"></a>例

次の例は、テーブルの既定のフォームの取得を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        print strfmt("Default form: %1", dt.formRef()); 
    }

### <a name="method-getcountryregioncodes"></a>メソッド getCountryRegionCodes

    public container getCountryRegionCodes()

#### <a name="return-value"></a>戻り値

### <a name="method-getcountryregioncontextfield"></a>メソッド getCountryRegionContextField

    public FieldId getCountryRegionContextField()

#### <a name="return-value"></a>戻り値

### <a name="method-getvalidtimestatevalidfromfieldid"></a>メソッド getValidTimeStateValidFromFieldId

    public FieldId getValidTimeStateValidFromFieldId()

#### <a name="return-value"></a>戻り値

### <a name="method-getvalidtimestatevalidtofieldid"></a>メソッド getValidTimeStateValidToFieldId

    public FieldId getValidTimeStateValidToFieldId()

#### <a name="return-value"></a>戻り値

### <a name="method-hasrecididx"></a>メソッド hasRecidIdx

テーブルのレコード ID インデックスが有効かどうかを示す値を返します。

    public boolean hasRecidIdx()

#### <a name="return-value"></a>戻り値

レコード ID インデックスがテーブルで有効な場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

戻り値は、テーブルの CreateRecIdIndex プロパティが Yes に設定されているかどうかに対応します。

#### <a name="examples"></a>例

次の例は、テーブルのレコード ID インデックスが有効かどうかを示す値の取得を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        print (strfmt("A record ID index for the table %1 in effect.", 
               dt.hasRecidIdx() ? "is" : "is not") ); 
    }

### <a name="method-hassurrogatekey"></a>メソッド hasSurrogateKey

    public boolean hasSurrogateKey()

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

テーブルの ID を返します。

    public TableId id()

#### <a name="return-value"></a>戻り値

テーブルの ID。

#### <a name="examples"></a>例

次の例は、テーブルの ID の取得を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        print (strfmt("The table ID is: %1", dt.id())); 
    }

### <a name="method-indexcnt"></a>メソッド indexCnt

テーブルのインデックスの数を返します。

    public int indexCnt()

#### <a name="return-value"></a>戻り値

テーブルのインデックスの数。

#### <a name="examples"></a>例

次の例は、テーブルのインデックス数の取得を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        print (strfmt("The table has %1 indexes.", dt.indexCnt())); 
    }

### <a name="method-indexcnt2id"></a>メソッド indexCnt2Id

    public IndexId indexCnt2Id(int cnt)

#### <a name="parameters"></a>パラメーター

cnt  

#### <a name="return-value"></a>戻り値

### <a name="method-indexname"></a>メソッド indexName

indexId パラメーターで指定された形式のインデックスの名前を返します。

    public str indexName(IndexId indexId, [DbBackend db])

#### <a name="parameters"></a>パラメーター

indexId  
データベース バックエンドのタイプを指定する DbBackend 値; オプション。

<!-- -->

db  
データベース バックエンドのタイプを指定する DbBackend 値; オプション。

#### <a name="return-value"></a>戻り値

indexId パラメーターで指定された形式のインデックスの名前。

#### <a name="examples"></a>例

次の例は、テーブルのインデックスの名前の取得を示しています。

    DictTable dt; 
    int       i; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        for (i=1; i <= dt.indexCnt(); i++) 
        { 
            print (dt.indexName(i)); 
        } 
    }

### <a name="method-indexname2id"></a>メソッド indexName2Id

名前で指定されているインデックスの ID を返します。

    public IndexId indexName2Id(str name)

#### <a name="parameters"></a>パラメーター

名前  
インデックスの名前。

#### <a name="return-value"></a>戻り値

名前パラメーターで指定されているインデックスの ID。名前値と同じ名前が付けられたインデックスがない場合は 0 (ゼロ)。

#### <a name="examples"></a>例

次の例は、名前で指定されたインデックスの ID の取得を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        print(strfmt("Index ID: %1", dt.indexName2Id("TypeIdx"))); 
    }

### <a name="method-indexnext"></a>メソッド indexNext

テーブルのインデックス反復処理中に、次のインデックス ID の値を返します。

    public IndexId indexNext(IndexId id)

#### <a name="parameters"></a>パラメーター

id  
次のインデックス ID が照会されるインデックスの ID。

#### <a name="return-value"></a>戻り値

テーブルのインデックス反復における次のインデックスの ID。反復処理するインデックスがない場合は 0 (ゼロ)。

#### <a name="remarks"></a>備考

インデックスの反復を開始するには、id パラメーターの値を 0 (ゼロ) に評価し、その反復の後続の呼び出しには戻り値を使用する必要があります。

#### <a name="examples"></a>例

次の例では、テーブルのインデックスを反復処理します。

    DictTable   dt; 
    DictIndex   di; 
    int         counter; 
    counter = 0; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        counter = dt.indexNext(counter); 
        while (counter) 
        { 
            di = dt.indexObject(counter); 
            if (di) 
            { 
                print strfmt("ID: %1 Name: %2", 
                             di.id(), 
                             di.name() ); 
            } 
            counter = dt.indexNext(counter); 
        } 
    }

### <a name="method-indexobject"></a>メソッド indexObject

ID で指定されているインデックスの DictTable クラスのインスタンスを作成します。

    public DictIndex indexObject(IndexId indexId)

#### <a name="parameters"></a>パラメーター

indexId  
作成するインデックスの ID。

#### <a name="return-value"></a>戻り値

indexId パラメーターで指定されたインデックスの DictIndex オブジェクト; null、Nothing、nullptr、unit、オブジェクトを作成できない場合は null 参照 (Visual Basic にはなし)。

#### <a name="examples"></a>例

次の例は、テーブルの固有インデックスの DictIndex オブジェクトを作成する方法を示しています。

    DictTable dt; 
    DictIndex di; 
    dt = new DictTable(tablenum(SysUserInfo)); 
    if (dt) 
    { 
         di = dt.indexObject(dt.indexUnique()); 
         if (di) 
         { 
            print di.name(); 
         } 
    }

### <a name="method-indexunique"></a>メソッド indexUnique

テーブルの一意のインデックスの ID を返します。

    public IndexId indexUnique()

#### <a name="return-value"></a>戻り値

テーブルの一意のインデックスの ID。

#### <a name="remarks"></a>備考

テーブルに複数の一意のインデックスが存在するとき、戻り値は次のいずれかです。

-   RecID 列を持つインデックス。
-   インデックスにレコードの ID がない場合、最短サイズを持つインデックスは、列のサイズの合計に基づきます。
-   最短サイズに関して複数のインデックスが一致する場合、インデックスが最初に追加されました。

#### <a name="examples"></a>例

次の例は、テーブルの固有インデックスの取得を示しています。

    DictTable dt; 
    DictIndex di; 
    dt = new DictTable(tablenum(SysUserInfo)); 
    if (dt) 
    { 
         di = dt.indexObject(dt.indexUnique()); 
         if (di) 
         { 
            print di.name(); 
         } 
    }

### <a name="method-instancerelationtype"></a>メソッド instanceRelationType

    public FieldId instanceRelationType()

#### <a name="return-value"></a>戻り値

### <a name="method-isabstract"></a>メソッド isAbstract

このテーブルが抽象かどうかを示します。

    public boolean isAbstract()

#### <a name="return-value"></a>戻り値

このテーブルが抽象である場合は true。それ以外の場合は、false。

### <a name="method-isbasedata"></a>メソッド isBaseData

テーブル コンテンツが基本データであるかどうかを示します。

    public boolean isBaseData()

#### <a name="return-value"></a>戻り値

テーブル コンテンツがベース データであることを AOT 内の TableContents プロパティが示す場合は true。それ以外の場合は、false。

#### <a name="examples"></a>例

次の例は、テーブルの内容が基本データかどうかを示す値の取得を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        print strfmt("isBaseData: %1", dt.isBaseData()); 
        print strfmt("isDefaultData: %1", dt.isDefaultData()); 
    }

### <a name="method-isdefaultdata"></a>メソッド isDefaultData

テーブルが既定のデータを含むかどうかを示します。

    public boolean isDefaultData()

#### <a name="return-value"></a>戻り値

テーブルに既定のデータが含まれている場合は true。それ以外の場合は、false。

#### <a name="examples"></a>例

次の例は、テーブルに既定のデータが含まれているかどうかを示す値の取得を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        print strfmt("isDefaultData: %1", dt.isDefaultData()); 
    }

### <a name="method-isderivedfrom"></a>メソッド isDerivedFrom

1 つのテーブル タイプが別から派生しているかどうかを示します。

    public boolean isDerivedFrom(TableName baseTableName)

#### <a name="parameters"></a>パラメーター

baseTableName  

#### <a name="return-value"></a>戻り値

このテーブルが baseTableName パラメーターで指定されたテーブルに由来する場合は true。

### <a name="method-ismap"></a>メソッド isMap

テーブルがマップであるかどうかを示します。

    public boolean isMap()

#### <a name="return-value"></a>戻り値

テーブルがマップである場合は true。それ以外の場合は false。

#### <a name="examples"></a>例

次の例は、テーブルがマップかどうかを示す値の取得を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(AddressMap)); 
    if (dt) 
    { 
        print(strfmt("Map: %1", dt.isMap())); 
    }

### <a name="method-issql"></a>メソッド isSql

テーブルが SQL テーブルであるかどうかを示します。

    public boolean isSql()

#### <a name="return-value"></a>戻り値

テーブルが SQL テーブルである場合は true。それ以外の場合は false。

#### <a name="examples"></a>例

次の例は、テーブルが SQL テーブルかどうかを示す値の取得を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        print(strfmt("SQL table: %1", dt.isSql())); 
    }

### <a name="method-issystemtable"></a>メソッド isSystemTable

テーブルがシステム テーブルであるかどうかを示します。

    public boolean isSystemTable()

#### <a name="return-value"></a>戻り値

テーブルがシステム テーブルである場合は true。それ以外の場合は false。

#### <a name="examples"></a>例

次の例は、テーブルがシステム テーブルかどうかを示す値の取得を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        print(strfmt("System table: %1", dt.isSystemTable())); 
    }

### <a name="method-istempdb"></a>メソッド isTempDb

    public boolean isTempDb()

#### <a name="return-value"></a>戻り値

### <a name="method-istmp"></a>メソッド isTmp

テーブルが一時テーブルであるかどうかを示します。

    public boolean isTmp()

#### <a name="return-value"></a>戻り値

テーブルが一時テーブルである場合は true。それ以外の場合は false。

#### <a name="examples"></a>例

次の例は、テーブルが一時テーブルかどうかを示す値の取得を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(TmpWMSOrder)); 
    if (dt) 
    { 
        print(strfmt("Temporary table: %1", dt.isTmp())); 
    }

### <a name="method-isunionallview"></a>メソッド isUnionAllView

    public boolean isUnionAllView()

#### <a name="return-value"></a>戻り値

### <a name="method-isvalidtimestatetable"></a>メソッド isValidTimeStateTable

    public boolean isValidTimeStateTable()

#### <a name="return-value"></a>戻り値

### <a name="method-isview"></a>メソッド isView

テーブルがビューであるかどうかを示します。

    public boolean isView()

#### <a name="return-value"></a>戻り値

テーブルがビューである場合は true。それ以外の場合は false。

#### <a name="examples"></a>例

次の例は、テーブルがビューかどうかを示す値の取得を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        print(strfmt("View: %1", dt.isView())); 
    }

### <a name="method-label"></a>メソッド label

テーブルのラベル テキストを返します。

    public str label()

#### <a name="return-value"></a>戻り値

テーブルのラベル テキスト。テーブルにラベル テキストがない場合は空の文字列。

#### <a name="examples"></a>例

次の例は、テーブルのラベル テキストの取得を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
         print(strfmt("Label: %1", dt.label())); 
    }

### <a name="method-labeldefined"></a>メソッド labelDefined

テーブルの label プロパティの値を返します。

    public str labelDefined()

#### <a name="return-value"></a>戻り値

テーブルの label プロパティの値。テーブルのラベル テキストがない場合は空の文字列。

### <a name="method-listpageref"></a>メソッド listPageRef

    public str listPageRef([boolean searchBaseTables])

#### <a name="parameters"></a>パラメーター

searchBaseTables  

#### <a name="return-value"></a>戻り値

### <a name="method-makerecord"></a>メソッド makeRecord

テーブルの空白のレコードを作成します。

    public Common makeRecord()

#### <a name="return-value"></a>戻り値

レコードが正常に作成された場合の共通の値; null、Nothing、nullptr、unit、レコードを作成できなかった場合は null 参照 (Visual Basic にはなし)。

#### <a name="remarks"></a>備考

返される共通値は、DictTable.callObject メソッドの呼び出しで使用できます。

### <a name="method-maxaccessmode"></a>メソッド maxAccessMode

AOT 内で設定されているとおり、テーブルの MaxAccessMode プロパティの値を返します。

    public AccessType maxAccessMode()

#### <a name="return-value"></a>戻り値

テーブルの最大アクセス モードを表す AccessType 値。

#### <a name="examples"></a>例

次の例は、テーブルの最大アクセス モードの取得を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        print strfmt("Maximum Access Mode: %1",dt.maxAccessMode()); 
    }

### <a name="method-name"></a>メソッド名

テーブル名を取得します。

    public str name([DbBackend db], [boolean pseudoname])

#### <a name="parameters"></a>パラメーター

db  
疑似名が返されるかどうかを示すブール値; オプション。

<!-- -->

pseudoname  
疑似名が返されるかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

テーブルの名前。

#### <a name="remarks"></a>備考

テーブル名が 30 文字よりも長い場合は、ネイティブ名およびテーブルの SQL 名は一致しません。

#### <a name="examples"></a>例

次の例は、テーブルの名前の取得を示しています。

    DictTable dt; 
    dt = new DictTable(1);  // 1 == tablenum(CustTable) 
    if (dt) 
    { 
        print(strfmt("The table name is %1.", dt.name())); 
    }

### <a name="method-objectmethod"></a>メソッド objectMethod

インデックスで指定されるインスタンス メソッドの名前を返します。

    public str objectMethod(int methodNumber, [TableScope tableScope])

#### <a name="parameters"></a>パラメーター

methodNumber  

<!-- -->

tableScope  

#### <a name="return-value"></a>戻り値

methodNumber パラメーターで指定されているインスタンス メソッドの名前。methodNumber 値が有効なインスタンス メソッド インデックスでない場合は空の文字列。

#### <a name="examples"></a>例

次の例は、テーブル内の各インスタンス メソッドの名前の取得を示しています。

    DictTable dt; 
    int       i; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        for (i=1; i <= dt.objectMethodCnt() ; i++) 
        { 
            print dt.objectMethod(i); 
        } 
    }

### <a name="method-objectmethodcnt"></a>メソッド objectMethodCnt

テーブルのインスタンス メソッドの数を返します。

    public int objectMethodCnt([TableScope tableScope])

#### <a name="parameters"></a>パラメーター

tableScope  

#### <a name="return-value"></a>戻り値

テーブルのインスタンス メソッドの数。

#### <a name="examples"></a>例

次の例は、テーブルのインスタンス メソッド数の取得を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        print (strfmt("The table has %1 instance methods.", dt.objectMethodCnt())); 
    }

### <a name="method-objectmethodobject"></a>メソッド objectMethodObject

インデックスにより指定されているオブジェクト メソッドの MethodInfo クラスのインスタンスを返します。

    public DictMethod objectMethodObject(int methodNumber, [TableScope tableScope])

#### <a name="parameters"></a>パラメーター

methodNumber  

<!-- -->

tableScope  

#### <a name="return-value"></a>戻り値

methodNumber パラメーターで指定されているオブジェクト メソッドの MethodInfo クラスのインスタンス。インスタンスを作成できない場合は null、Nothing、nullptr、unit、null 参照 (Visual Basic にはなし) 。

#### <a name="examples"></a>例

次の例は、テーブルのオブジェクト メソッドの取得を示しています。

    DictTable dt; 
    int       i; 
    MethodInfo mi; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        for (i=1; i <= dt.objectMethodCnt(); i++) 
        { 
            mi = dt.objectMethodObject(i); 
            if (mi) 
            { 
                print mi.name(); 
            } 
        } 
    }

### <a name="method-mapobject"></a>メソッド mapObject

インデックスで指定されているマッピングに対する \[t: DictTableMap\] クラスのインスタンスを作成します。

    public DictTableMap mapObject(int methodNumber)

#### <a name="parameters"></a>パラメーター

methodNumber  

#### <a name="return-value"></a>戻り値

\_cnt パラメーターで指定されたフィールドの DictTableMap オブジェクト; null、Nothing、nullptr、unit、オブジェクトを作成できない場合は null 参照 (Visual Basic にはなし)。

### <a name="method-mapcnt"></a>メソッド mapCnt

この DictTable インスタンスにより指定されているマップの使用可能なテーブル マッピングの数を返します。

    public int mapCnt()

#### <a name="return-value"></a>戻り値

カウント。

### <a name="method-occenabled"></a>メソッド occEnabled

テーブルに対してオプティミスティック同時実行モードが有効になっているかどうかを示します。

    public boolean occEnabled()

#### <a name="return-value"></a>戻り値

オプティミスティック同時モードが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

このモードを有効にすると、データがデータベースからフェッチされるときに、データは今後の変更からロックされません。 データは、実際の更新の実行時にのみロックされます。

#### <a name="examples"></a>例

次の例は、occEnabled メソッドの呼び出しを示しています。

    static public void Main(Args _args) 
    { 
        DictTable dt; 
        boolean enabled; 
        dt = new DictTable(tablenum(CustTable)); 
        enabled = dt.occEnabled(); 
    }

### <a name="method-primaryindex"></a>メソッド primaryIndex

テーブルのプライマリ インデックスの ID を返します。

    public IndexId primaryIndex([boolean asDefinedInAOT])

#### <a name="parameters"></a>パラメーター

asDefinedInAOT  
取得するプライマリ インデックスが、AOT で定義されているかどうかを示すブール値。 true の値は、AOT で定義されたプライマリ インデックスを返します。 false の値は、SQL テーブルで定義されたプライマリ インデックスを返します、オプション。

#### <a name="return-value"></a>戻り値

テーブルの主インデックスの ID。テーブルの主インデックスがない場合は 0 (ゼロ)。

#### <a name="examples"></a>例

次の例は、テーブルのプライマリ インデックスの取得を示しています。

    DictTable dt; 
    DictIndex di; 
    int       i; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        i = dt.primaryIndex(); 
        if (0 != i) 
        { 
            di = new DictIndex(tablenum(CustTable), i); 
            print di.name(); 
        } 
    }

### <a name="method-primarykeyfield"></a>メソッド primaryKeyField

テーブルの主キーに使用されているフィールドの ID を返します。

    public FieldId primaryKeyField()

#### <a name="return-value"></a>戻り値

テーブルの主キーで使用されるフィールドの ID。テーブルの主キーとして機能する単一のフィールドがない場合は 0 (ゼロ)。

#### <a name="examples"></a>例

次の例は、テーブルの主キーのフィールド ID の取得を示しています。

    DictTable dt; 
    DictField df; 
    tableId   tID; 
    fieldId   fID; 
    tID = tablenum(CustTable); 
    dt = new DictTable(tID); 
    if (dt) 
    { 
       fID = dt.primaryKeyField(); 
       if (0 != fID) 
       { 
           df = new DictField(tID, fID); 
           if (df) 
           { 
                print strfmt("Primary key field name: %1", df.name()); 
           } 
       } 
    }

### <a name="method-relation"></a>メソッド relation

インデックスで指定される関係の名前を返します。

    public str relation(int RelationNumber, [TableScope tableScope])

#### <a name="parameters"></a>パラメーター

RelationNumber  

<!-- -->

tableScope  

#### <a name="return-value"></a>戻り値

RelationNumber パラメーターで指定されているリレーションの名前。RelationNumber 値が有効なリレーション インデックスでない場合は空の文字列。

#### <a name="examples"></a>例

次の例は、テーブル内の各リレーションの名前の取得を示しています。

    DictTable dt; 
    int       i; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        for (i=1; i <= dt.relationCnt() ; i++) 
        { 
            print dt.relation(i); 
        } 
    }

### <a name="method-relationcnt"></a>メソッド relationCnt

テーブルの関係の数を返します。

    public int relationCnt([TableScope tableScope])

#### <a name="parameters"></a>パラメーター

tableScope  

#### <a name="return-value"></a>戻り値

テーブルのリレーションの番号。

#### <a name="examples"></a>例

次の例は、テーブルのリレーション数の取得を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        print (strfmt("The table has %1 relations.", dt.relationCnt())); 
    }

### <a name="method-replacementkey"></a>メソッド replacementKey

    public IndexId replacementKey()

#### <a name="return-value"></a>戻り値

### <a name="method-reportref"></a>メソッド reportRef

テーブルの既定のレポートの名前を返します。

    public str reportRef()

#### <a name="return-value"></a>戻り値

テーブルの既定のレポートの名前。テーブルの既定のレポートがない場合は空の文字列。

#### <a name="examples"></a>例

以下は、テーブルの既定のレポートの名前の取得を示しています。

    DictTable dt; 
    str       strReport; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        strReport = dt.reportRef(); 
        print strfmt("Default report: %1", strReport != "" ? strReport : "None specified"); 
    }

### <a name="method-rights"></a>メソッド rights

テーブルに指定されている、現在のユーザーのアクセス権を返します。

    public AccessType rights([boolean ignoreContext])

#### <a name="parameters"></a>パラメーター

ignoreContext  

#### <a name="return-value"></a>戻り値

テーブルに指定されている、現在のユーザーのアクセス権。 戻り値は、AccessType システム列挙値の 1 つです。

### <a name="method-securitykeyid"></a>メソッド securityKeyId

テーブルのセキュリティ キーの ID を返します。

    public SecurityKeyId securityKeyId()

#### <a name="return-value"></a>戻り値

テーブルのセキュリティ キーの ID。テーブルのセキュリティ キーがない場合は 0 (ゼロ)。

#### <a name="examples"></a>例

次の例は、テーブルのセキュリティ キー ID の取得を示しています。

    DictTable dt; 
    DictSecurityKey dsk; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        if (0 != dt.securityKeyId()) 
        dsk = new DictSecurityKey(dt.securityKeyId()); 
        if (dsk) 
        { 
            print (strfmt("The table's security key is %1.", dsk.name())); 
        } 
    }

### <a name="method-singularlabel"></a>メソッド singularLabel

    public str singularLabel([boolean labelTranslation])

#### <a name="parameters"></a>パラメーター

labelTranslation  

#### <a name="return-value"></a>戻り値

### <a name="method-staticmethod"></a>メソッド staticMethod

インデックスで指定される静的メソッドの名前を返します。

    public str staticMethod(int methodNumber)

#### <a name="parameters"></a>パラメーター

methodNumber  
テーブルの静的メソッドのリストへの AOT の順で、1 から始まるインデックス。

#### <a name="return-value"></a>戻り値

methodNumber パラメーターで指定されている静的メソッドの名前。methodNumber 値が有効な静的メソッド インデックスでない場合は空の文字列。

#### <a name="examples"></a>例

次の例は、テーブル内の各静的メソッドの名前の取得を示しています。

    DictTable dt; 
    int       i; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        for (i=1; i <= dt.staticMethodCnt() ; i++) 
        { 
            print dt.staticMethod(i); 
        } 
    }

### <a name="method-staticmethodcnt"></a>メソッド staticMethodCnt

テーブルの静的メソッドの数を返します。

    public int staticMethodCnt()

#### <a name="return-value"></a>戻り値

テーブルの静的メソッドの数。

#### <a name="examples"></a>例

次の例は、テーブルの静的メソッド数の取得を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        print (strfmt("The table has %1 static methods.", dt. staticMethodCnt())); 
    }

### <a name="method-staticmethodobject"></a>メソッド staticMethodObject

インデックスにより指定されている静的メソッドの MethodInfo クラスのインスタンスを返します。

    public DictMethod staticMethodObject(int methodNumber)

#### <a name="parameters"></a>パラメーター

methodNumber  
テーブルの静的メソッドへの AOT の順で、1 から始まるインデックス。

#### <a name="return-value"></a>戻り値

methodNumber パラメーターで指定されている静的メソッドの MethodInfo クラスのインスタンス。null、Nothing、nullptr、unit、null 参照 (Visual Basic にはなし) 。

#### <a name="examples"></a>例

次の例は、テーブルの静的メソッドの取得を示しています。

    DictTable dt; 
    int       i; 
    MethodInfo mi; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        for (i=1; i <= dt.staticMethodCnt(); i++) 
        { 
            mi = dt.staticMethodObject(i); 
            if (mi) 
            { 
                print mi.name(); 
            } 
        } 
    }

### <a name="method-supportinheritance"></a>メソッド supportInheritance

    public boolean supportInheritance()

#### <a name="return-value"></a>戻り値

### <a name="method-tablegroup"></a>メソッド tableGroup

テーブルのテーブル グループを返します。

    public TableGroup tableGroup()

#### <a name="return-value"></a>戻り値

テーブルのテーブル グループを表す TableGroup 値。

#### <a name="remarks"></a>備考

戻り値は、AOT テーブルの TableGroup プロパティに対応します。

#### <a name="examples"></a>例

次の例は、テーブルのテーブル グループの取得を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
       print strfmt("Table Group: %1", dt.tableGroup()); 
    }

### <a name="method-tabletype"></a>メソッド tableType

テーブルのタイプを示します。

    public TableType tableType()

#### <a name="return-value"></a>戻り値

エラー状態がある場合は、エラー状態です。

### <a name="method-titlefield1"></a>メソッド titleField1

テーブルの titleField1 プロパティを表すフィールドの ID を返します。

    public FieldId titleField1([boolean includeBaseTables], [boolean extendedFieldId])

#### <a name="parameters"></a>パラメーター

includeBaseTables  

<!-- -->

extendedFieldId  

#### <a name="return-value"></a>戻り値

テーブルの titleField1 プロパティを表すフィールドの ID。

#### <a name="remarks"></a>備考

ベスト プラクティスのガイドラインに従うと、titleField1 プロパティは、テーブルのレコードのキー フィールドを表します。

#### <a name="examples"></a>例

次の例は、テーブルの titleField1 プロパティに使用されるフィールドの ID の取得を示しています。

    DictTable dt; 
    DictField df; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        df = new DictField(tablenum(CustTable),dt.titleField1()); 
        if (df) 
        { 
            print df.name(); 
        } 
    } 
    pause;

### <a name="method-titlefield2"></a>メソッド titleField2

テーブルの titleField2 プロパティを表すフィールドの ID を返します。

    public FieldId titleField2([boolean includeBaseTables], [boolean extendedFieldId])

#### <a name="parameters"></a>パラメーター

includeBaseTables  

<!-- -->

extendedFieldId  

#### <a name="return-value"></a>戻り値

テーブルの titleField2 プロパティを表すフィールドの ID。

#### <a name="remarks"></a>備考

ベスト プラクティスのガイドラインに従うと、titleField2 プロパティは、テーブルのレコードの説明を表します。

#### <a name="examples"></a>例

次の例は、テーブルの titleField2 プロパティに使用されるフィールドの ID の取得を示しています。

    DictTable dt; 
    DictField df; 
    dt = new DictTable(tablenum(CustTable)); 
    if (dt) 
    { 
        df = new DictField(tablenum(CustTable),dt.titleField2()); 
        if (df) 
        { 
            print df.name(); 
        } 
    }

### <a name="method-validrelationship"></a>メソッド validRelationship

    public boolean validRelationship()

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

テーブルが表示できるかどうかを判定します。

    public boolean visible()

#### <a name="return-value"></a>戻り値

テーブルが可視である場合は true。それ以外の場合は false。

### <a name="method-construct"></a>メソッド construct

    public static DictTable construct(str tableName)

#### <a name="parameters"></a>パラメーター

tableName  

#### <a name="return-value"></a>戻り値

### <a name="method-getrelationtypefromtablename"></a>メソッド getRelationTypeFromTableName

    public static RecId getRelationTypeFromTableName(TableName tableName)

#### <a name="parameters"></a>パラメーター

tableName  

#### <a name="return-value"></a>戻り値

### <a name="method-gettablenamefromrelationtype"></a>メソッド getTableNameFromRelationType

    public static TableName getTableNameFromRelationType(RecId relationType)

#### <a name="parameters"></a>パラメーター

relationType  

#### <a name="return-value"></a>戻り値

### <a name="method-createrecord"></a>メソッド createRecord

    public static Common createRecord(str tableName)

#### <a name="parameters"></a>パラメーター

tableName  

#### <a name="return-value"></a>戻り値

### <a name="method-reloadsecurity"></a>メソッド reloadSecurity

テーブルの機能キー システムを再読み込みします。

    public void reloadSecurity()

#### <a name="examples"></a>例

次の例では、テーブルの機能キー システムを再読み込みします。

    dt.reloadSecurity()

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(TableId tableId)

#### <a name="parameters"></a>パラメーター

tableId  
DictTable クラスのインスタンスを作成するために使用されるテーブルの ID。

#### <a name="examples"></a>例

次の例は、DictTable クラスのインスタンスを作成する方法を示しています。

    DictTable dt; 
    dt = new DictTable(tablenum(CustTable)); 
    if (!dt) 
    { 
        // Take error action. 
    }

### <a name="method-reindex"></a>メソッド reindex

テーブルのインデックスの再作成を実行します。

    public void reindex()

#### <a name="remarks"></a>備考

SQL テーブルを再作成するメソッドを使用しないでください。代わりに、SqlDataDictionary::tableReindex メソッドを使用してください。 また、クライアントで実行時に DictTable::reindex メソッドはサポートされません。

## <a name="class-dicttablemap"></a>クラス DictTableMap
    class DictTableMap extends Object

DictTableMap クラスは、テーブル マッピングに関する情報を提供します。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                 | 説明                                                    |
|----------------------------------------|----------------------------------------------------------------|
| public int table()                     | マッピングが参照するテーブルを取得します。               |
| public int fieldCnt()                  | テーブル マッピングのフィールドの数を取得します。            |
| public int fieldCnt2FieldTo(int cnt)   | マップ フィールドにより参照されているテーブル フィールドを取得します。 |
| public int fieldCnt2FieldFrom(int cnt) | テーブル フィールドを参照しているマップ フィールドを取得します。     |

### <a name="method-table"></a>メソッド table

マッピングが参照するテーブルを取得します。

    public int table()

#### <a name="return-value"></a>戻り値

テーブル ID。

#### <a name="remarks"></a>備考

ツリー ノードをトラバースするのではなく、テーブルのマッピングにアクセスするには、このメソッドを使用します。

### <a name="method-fieldcnt"></a>メソッド fieldCnt

テーブル マッピングのフィールドの数を取得します。

    public int fieldCnt()

#### <a name="return-value"></a>戻り値

カウント。

#### <a name="remarks"></a>備考

ツリー ノードをトラバースするのではなく、テーブルのマッピングにアクセスするには、このメソッドを使用します。

### <a name="method-fieldcnt2fieldto"></a>メソッド fieldCnt2FieldTo

マップ フィールドにより参照されているテーブル フィールドを取得します。

    public int fieldCnt2FieldTo(int cnt)

#### <a name="parameters"></a>パラメーター

cnt  

#### <a name="return-value"></a>戻り値

テーブル フィールド ID。

#### <a name="remarks"></a>備考

ツリー ノードをトラバースするのではなく、テーブルのマッピングにアクセスするには、このメソッドを使用します。

### <a name="method-fieldcnt2fieldfrom"></a>メソッド fieldCnt2FieldFrom

テーブル フィールドを参照しているマップ フィールドを取得します。

    public int fieldCnt2FieldFrom(int cnt)

#### <a name="parameters"></a>パラメーター

cnt  

#### <a name="return-value"></a>戻り値

マップ フィールド ID。

#### <a name="remarks"></a>備考

ツリー ノードをトラバースするのではなく、テーブルのマッピングにアクセスするには、このメソッドを使用します。

## <a name="class-dicttype"></a>クラス DictType
    class DictType extends Object

DictType クラスは、拡張データ型を管理します。

### <a name="remarks"></a>備考

SysDictType クラスは DictType を拡張します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                | 説明                                                                                                                                                              |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public Alignment alignment()                                          | 拡張データ型の配置を取得します。                                                                                                                      |
| public int arraySize()                                                | 拡張データ型の配列サイズを提供します。                                                                                                                       |
| public Types baseType()                                               | タイプ列挙値を使うことで、拡張データ型の基になるデータ型を提供します。                                                                          |
| public ConfigurationKeyId configurationKeyId()                        | 拡張データ型のコンフィギュレーション キーの ID を返します。                                                                                                      |
| public int displayHeight(\[boolean useDefaults\])                     | タイプの表示の高さを取得します。                                                                                                                               |
| public int displayLength(\[boolean useDefaults\])                     |                                                                                                                                                                          |
| public EnumId enumId()                                                | 拡張データ型の基になる列挙型の ID を提供します。                                                                                        |
| public ExtendedTypeId extend()                                        | 拡張データ型が拡張される拡張データ型の ID を提供します。                                                                                           |
| public List extendedBy(\[boolean allLevels\])                         | 現在の EDT により拡張された拡張データ型 (EDT) のタイプ ID の一覧を取得します。                                                                        |
| public str formHelp()                                                 |                                                                                                                                                                          |
| public str getControlClass()                                          |                                                                                                                                                                          |
| public container getCountryRegionCodes()                              | 定義されている国/地域コードを保持するコンテナーを取得します。                                                                                              |
| public DictRelation getLookupRelation(\[int arrayIndex\])             |                                                                                                                                                                          |
| public AnyType getValue(\[int arrayIndex\])                           |                                                                                                                                                                          |
| public str help(\[int arrayIndex\], \[boolean useInterfaceLanguage\]) | 拡張データ型または指定した配列要素、または拡張データ型を拡張する拡張データ型に表示されるヘルプ テキストを提供します。       |
| public str helpDefined(\[int arrayIndex\])                            | 拡張データ型の help プロパティの値を返します。                                                                                                       |
| public ExtendedTypeId id()                                            | 拡張データ型の ID を提供します。                                                                                                                               |
| public boolean isExtendedFrom(str baseEDTName)                        | 拡張データ型が、提供される基本拡張データ型から拡張するかどうかを決定します。                                                                     |
| public int isRadioStyle()                                             | 列挙データ型に基づいている拡張データ型のスタイルがオプション ボタンまたはコンボ ボックスであるかどうかを示します。                                                |
| public str label(\[int arrayIndex\])                                  | 拡張データ型または指定した配列要素、または拡張データ型を拡張する拡張データ型のラベルに表示されるラベル テキストを提供します。 |
| public str labelDefined(\[int arrayIndex\])                           | 拡張データ型の label プロパティの値を返します。                                                                                                      |
| public str lookupTable(\[boolean useInheritedMetaData\])              |                                                                                                                                                                          |
| public str name()                                                     | 拡張データ型の名前を提供します。                                                                                                                              |
| public DictRelation relationObject(\[int arrayIndex\])                | DictRelation オブジェクトを返すことで、拡張データ型または指定された配列要素に対して定義されている関係に関する情報を提供します。                         |
| public int stringLen()                                                | 文字列データ型に基づいている拡張データ型の文字列の長さを提供します。                                                                              |
| public boolean stringRight()                                          | 文字列が文字列データ型に基づいている拡張データ型で右揃えかどうかを示します。                                                         |
| ::public static Alignment getTypeAlignment(Types type)                |                                                                                                                                                                          |
| ::public static int getTypeDisplayHeight(Types type)                  |                                                                                                                                                                          |
| ::public static int getTypeDisplayLength(Types type)                  | 組み込み型の表示の長さを取得します。                                                                                                                         |
| public void setValue(AnyType Value, \[int arrayEntry\])               |                                                                                                                                                                          |
| public void new(ExtendedTypeId typeId)                                | Object クラスの新しいインスタンスを初期化します。                                                                                                                          |
| public void setStringLen(int stringLen)                               | 文字列データ型に基づいている拡張データ型の文字列の長さを設定します。                                                                                  |
| public void setStringRight(boolean right)                             | 文字列データ型に基づいている拡張データ型の文字列の妥当性を示します。                                                                        |

### <a name="method-alignment"></a>メソッド alignment

拡張データ型の配置を取得します。

    public Alignment alignment()

#### <a name="return-value"></a>戻り値

拡張データ型の配置。

### <a name="method-arraysize"></a>メソッド arraySize

拡張データ型の配列サイズを提供します。

    public int arraySize()

#### <a name="return-value"></a>戻り値

配列サイズの整数値。拡張データ型に配列要素がない場合は 1 。

#### <a name="examples"></a>例

次の例では、arraySize メソッドは XMLMapDimension 拡張データ型の配列のサイズを返します。

        DictType dicttype; 
        int i; 
        dicttype = new DictType(extendedTypeNum(XMLMapDimension)); 
        for (i = 1;  i < dicttype.arraySize(); i++) 
        { 
            print dicttype.label(i); 
            pause; 
        }

### <a name="method-basetype"></a>メソッド baseType

タイプ列挙値を使うことで、拡張データ型の基になるデータ型を提供します。

    public Types baseType()

#### <a name="return-value"></a>戻り値

データ型を示すタイプ列挙値。

#### <a name="remarks"></a>備考

Global::Enum2Value メソッドを使用することにより、戻り値を文字列に変換することができます。

### <a name="method-configurationkeyid"></a>メソッド configurationKeyId

拡張データ型のコンフィギュレーション キーの ID を返します。

    public ConfigurationKeyId configurationKeyId()

#### <a name="return-value"></a>戻り値

拡張データ型のコンフィギュレーション キーの ID。

### <a name="method-displayheight"></a>メソッド displayHeight

タイプの表示の高さを取得します。

    public int displayHeight([boolean useDefaults])

#### <a name="parameters"></a>パラメーター

useDefaults  
タイプに長さがない場合に既定値を使用するかどうかを示すブール値。

#### <a name="return-value"></a>戻り値

タイプの表示の高さ。

### <a name="method-displaylength"></a>メソッド displayLength

    public int displayLength([boolean useDefaults])

#### <a name="parameters"></a>パラメーター

useDefaults  

#### <a name="return-value"></a>戻り値

### <a name="method-enumid"></a>メソッド enumId

拡張データ型の基になる列挙型の ID を提供します。

    public EnumId enumId()

#### <a name="return-value"></a>戻り値

拡張データ型の基になる列挙タイプのID。拡張データ型が列挙値に基づかない場合は 0 (ゼロ)。

#### <a name="remarks"></a>備考

baseType メソッドを使用すると、拡張データ タイプのデータ タイプを判断することができます。

### <a name="method-extend"></a>メソッド extend

拡張データ型が拡張される拡張データ型の ID を提供します。

    public ExtendedTypeId extend()

#### <a name="return-value"></a>戻り値

拡張データ型を超えた拡張データ型の ID。拡張データ型が拡張データ型を超えていない場合は 0 (ゼロ)。

#### <a name="examples"></a>例

次の例では、拡張メソッドは ABCPercentA 拡張データ型が拡張する拡張データ型の ID を返します。

        DictType dicttype; 
        dicttype = new DictType(extendedTypeNum(ABCPercentA)); 
        print dicttype.name() + " extends: " + extendedTypeId2Name(dicttype.extend());

### <a name="method-extendedby"></a>メソッド extendedBy

現在の EDT により拡張された拡張データ型 (EDT) のタイプ ID の一覧を取得します。

    public List extendedBy([boolean allLevels])

#### <a name="parameters"></a>パラメーター

allLevels  

#### <a name="return-value"></a>戻り値

現在の EDT により拡張された EDT のタイプ ID の一覧。

### <a name="method-formhelp"></a>メソッド formHelp

    public str formHelp()

#### <a name="return-value"></a>戻り値

### <a name="method-getcontrolclass"></a>メソッド getControlClass

    public str getControlClass()

#### <a name="return-value"></a>戻り値

### <a name="method-getcountryregioncodes"></a>メソッド getCountryRegionCodes

定義されている国/地域コードを保持するコンテナーを取得します。

    public container getCountryRegionCodes()

#### <a name="return-value"></a>戻り値

国/地域コードを保持するコンテナーです。

### <a name="method-getlookuprelation"></a>メソッド getLookupRelation

    public DictRelation getLookupRelation([int arrayIndex])

#### <a name="parameters"></a>パラメーター

arrayIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-getvalue"></a>メソッド getValue

    public AnyType getValue([int arrayIndex])

#### <a name="parameters"></a>パラメーター

arrayIndex  

#### <a name="return-value"></a>戻り値

### <a name="method-help"></a>メソッド help

拡張データ型または指定した配列要素、または拡張データ型を拡張する拡張データ型に表示されるヘルプ テキストを提供します。

    public str help([int arrayIndex], [boolean useInterfaceLanguage])

#### <a name="parameters"></a>パラメーター

arrayIndex  
ユーザー インターフェイス言語がヘルプ テキストに使用されているかどうかを示すブール値; オプション。

<!-- -->

useInterfaceLanguage  
ユーザー インターフェイス言語がヘルプ テキストに使用されているかどうかを示すブール値; オプション。

#### <a name="return-value"></a>戻り値

拡張データ型に表示されるヘルプ テキストの文字列値、または arrayEntry 値が提供される場合の配列要素。 ヘルプ テキストは、AOT 内の拡張データ型のヘルプ テキスト プロパティ、または Finance and Operations アプリケーション オブジェクト ツリー (AOT) 内の array 要素に対応します。 拡張データ型にヘルプ テキストがないとき、このメソッドは、拡張データ型が拡張する拡張データ型に対して定義されているヘルプ テキストを返します。

### <a name="method-helpdefined"></a>メソッド helpDefined

拡張データ型の help プロパティの値を返します。

    public str helpDefined([int arrayIndex])

#### <a name="parameters"></a>パラメーター

arrayIndex  

#### <a name="return-value"></a>戻り値

拡張データ型の場合は help プロパティの値、arrayEntry 値が指定されている場合は配列要素の値。 ヘルプ テキストは、AOT 内の拡張データ型のヘルプ テキスト プロパティ、または AOT 内の array 要素に対応します。

### <a name="method-id"></a>メソッド id

拡張データ型の ID を提供します。

    public ExtendedTypeId id()

#### <a name="return-value"></a>戻り値

拡張データ型の ID を示すデータ型の値です。

### <a name="method-isextendedfrom"></a>メソッド isExtendedFrom

拡張データ型が、提供される基本拡張データ型から拡張するかどうかを決定します。

    public boolean isExtendedFrom(str baseEDTName)

#### <a name="parameters"></a>パラメーター

baseEDTName  
拡張データ型の名前。

#### <a name="return-value"></a>戻り値

用意された基本拡張データ型から拡張データ型が拡張される場合は true。それ以外の場合は、false。

### <a name="method-isradiostyle"></a>メソッド isRadioStyle

列挙データ型に基づいている拡張データ型のスタイルがオプション ボタンまたはコンボ ボックスであるかどうかを示します。

    public int isRadioStyle()

#### <a name="return-value"></a>戻り値

スタイルがオプション ボタンである場合は 1、それ以外の場合は 0 (ゼロ) です。

### <a name="method-label"></a>メソッド label

拡張データ型または指定した配列要素、または拡張データ型を拡張する拡張データ型のラベルに表示されるラベル テキストを提供します。

    public str label([int arrayIndex])

#### <a name="parameters"></a>パラメーター

arrayIndex  

#### <a name="return-value"></a>戻り値

拡張データ タイプの場合に表示されるラベル、または arrayEntry 値が指定されている場合は配列要素のラベル。 拡張データ型にラベルがないとき、このメソッドは、拡張データ型が拡張する拡張データ型に対して定義されているラベルを返します。

#### <a name="remarks"></a>備考

返されるラベルは、AOT の拡張データ型または配列要素のラベル プロパティに対応します。

### <a name="method-labeldefined"></a>メソッド labelDefined

拡張データ型の label プロパティの値を返します。

    public str labelDefined([int arrayIndex])

#### <a name="parameters"></a>パラメーター

arrayIndex  

#### <a name="return-value"></a>戻り値

拡張データ型の場合は label プロパティの値、arrayEntry 値が指定されている場合は配列要素の値。

#### <a name="remarks"></a>備考

戻り値は、AOT 内の拡張データ型のラベルプロパティ、またはAOT 内の array 要素に対応します。

### <a name="method-lookuptable"></a>メソッド lookupTable

    public str lookupTable([boolean useInheritedMetaData])

#### <a name="parameters"></a>パラメーター

useInheritedMetaData  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

拡張データ型の名前を提供します。

    public str name()

#### <a name="return-value"></a>戻り値

名前の文字列値。 名前は、AOT 内の拡張データ型の名前プロパティに対応します。

### <a name="method-relationobject"></a>メソッド relationObject

DictRelation オブジェクトを返すことで、拡張データ型または指定された配列要素に対して定義されている関係に関する情報を提供します。

    public DictRelation relationObject([int arrayIndex])

#### <a name="parameters"></a>パラメーター

arrayIndex  

#### <a name="return-value"></a>戻り値

関係に関する情報を提供する DictRelation オブジェクト。

#### <a name="remarks"></a>備考

拡張データ型および配列要素に対して関係が定義されていない場合、DictRelation インスタンスを後続使用すると、実行時にエラーが発生します。

#### <a name="examples"></a>例

次の例では、relationObject メソッドは XMLMapDimension 拡張データ型の DictRelation オブジェクトを返します。

        DictType dicttype; 
        DictRelation dictrelation; 
        dicttype = new DictType(extendedTypeNum(XMLMapDimension)); 
        dictrelation = dicttype.relationObject(); 
        if(dictrelation) 
        { 
            print "Relation lines: " + int2str(dictrelation.lines()); 
        } 
        else 
        { 
            print "No relations defined."; 
         }

### <a name="method-stringlen"></a>メソッド stringLen

文字列データ型に基づいている拡張データ型の文字列の長さを提供します。

    public int stringLen()

#### <a name="return-value"></a>戻り値

文字列の長さを示す整数。拡張データ型が文字列データ型に基づいていない場合は 0 (ゼロ) 。

### <a name="method-stringright"></a>メソッド stringRight

文字列が文字列データ型に基づいている拡張データ型で右揃えかどうかを示します。

    public boolean stringRight()

#### <a name="return-value"></a>戻り値

文字列が右揃えの場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

戻り値は、AOT 内の拡張データ型の調整プロパティに対応します。

### <a name="method-gettypealignment"></a>メソッド getTypeAlignment

    public static Alignment getTypeAlignment(Types type)

#### <a name="parameters"></a>パラメーター

タイプ  

#### <a name="return-value"></a>戻り値

### <a name="method-gettypedisplayheight"></a>メソッド getTypeDisplayHeight

    public static int getTypeDisplayHeight(Types type)

#### <a name="parameters"></a>パラメーター

タイプ  

#### <a name="return-value"></a>戻り値

### <a name="method-gettypedisplaylength"></a>メソッド getTypeDisplayLength

組み込み型の表示の長さを取得します。

    public static int getTypeDisplayLength(Types type)

#### <a name="parameters"></a>パラメーター

タイプ  
タイプ。

#### <a name="return-value"></a>戻り値

組み込み型の表示の長さ。

### <a name="method-setvalue"></a>メソッド setValue

    public void setValue(AnyType Value, [int arrayEntry])

#### <a name="parameters"></a>パラメーター

先頭値  

<!-- -->

arrayEntry  

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(ExtendedTypeId typeId)

#### <a name="parameters"></a>パラメーター

typeId  
拡張データ型の ID を示すデータ型です。

#### <a name="remarks"></a>備考

TypeId 値が無効な拡張データ型 ID である場合にこのコンストラクターは失敗しません。ただし、DictType インスタンスを使用すると、実行時にエラーが発生します。 extendedTypeNum 関数を使用して、ID の代わりに拡張データ タイプの名前を渡すことができます。

#### <a name="examples"></a>例

次の例は、DictType クラスのインスタンスを作成する方法を示しています。

        DictType dicttype; 
        dicttype = new DictType(extendedTypeNum(ABCModelType));

### <a name="method-setstringlen"></a>メソッド setStringLen

文字列データ型に基づいている拡張データ型の文字列の長さを設定します。

    public void setStringLen(int stringLen)

#### <a name="parameters"></a>パラメーター

stringLen  
文字列の長さを示す整数。

#### <a name="remarks"></a>備考

このメソッドを使用すると、X++ コードとメタデータを作成、読み込み、更新、および削除ができます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。 文字列の長さは、AOT 内の拡張データ型 StringSize プロパティに対応します。

#### <a name="examples"></a>例

次の例では、AccountName 拡張データ型の StringSize プロパティを 10 に設定します。

    server static public void Main(Args _args) 
    { 
        DictType  dt; 
        dt = new DictType(ExtendedTypeNum(AccountName)); 
        if (dt) 
        { 
            dt.setStringLen(10); 
        } 
    }

### <a name="method-setstringright"></a>メソッド setStringRight

文字列データ型に基づいている拡張データ型の文字列の妥当性を示します。

    public void setStringRight(boolean right)

#### <a name="parameters"></a>パラメーター

権限  
ブール値: 右揃え文字列の場合は true、左揃え文字列の場合は false。

#### <a name="remarks"></a>備考

このメソッドを使用すると、X++ コードとメタデータを作成、読み込み、更新、および削除ができます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

#### <a name="examples"></a>例

次の例では、AccountName 拡張データ型の正当性を設定します。

    server static public void Main(Args _args) 
    { 
        DictType dt; 
        dt = new DictType(ExtendedTypeNum(AccountName)); 
        if (dt) 
        { 
            dt.setStringRight(true); 
        } 
    }

## <a name="class-dictview"></a>クラス DictView
    class DictView extends DictTable

DictView クラスでは、特定のビューに関する情報へのアクセスを提供します。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

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

### <a name="method-computedcolumnstring"></a>メソッド computedColumnString

テーブル エイリアスを取得します。

    public str computedColumnString(str dataSourceName, str fieldName, [FieldNameGenerationMode generationMode], [boolean needTrim])

#### <a name="parameters"></a>パラメーター

dataSourceName  

<!-- -->

fieldName  

<!-- -->

generationMode  

<!-- -->

needTrim  

#### <a name="return-value"></a>戻り値

書式設定されたフィールド名文字列。

#### <a name="remarks"></a>備考

テーブルのエイリアスは、計算列定義と一緒に使用できるデータベース形式の SQL フィールド名です。

### <a name="method-datasourcecnt"></a>メソッド datasourceCnt

ビュー内のデータ ソースをカウントします。

    public int datasourceCnt()

#### <a name="return-value"></a>戻り値

ビュー内のデータ ソースの数。

### <a name="method-datasourcedataareaidname"></a>メソッド datasourceDataareaIdName

データ ソースの法人を識別するためにビュー定義で使用される SQL 名を取得します。

    public str datasourceDataareaIdName(int cnt)

#### <a name="parameters"></a>パラメーター

cnt  

#### <a name="return-value"></a>戻り値

データ ソースの法人を識別するためにビュー定義で使用される SQL 名。エラーが発生した場合は空の文字列。

### <a name="method-datasourceid2tableid"></a>メソッド datasourceID2TableId

特定のデータ ソースのテーブル ID を取得します。

    public TableId datasourceID2TableId(TableId dataSourceId)

#### <a name="parameters"></a>パラメーター

dataSourceId  

#### <a name="return-value"></a>戻り値

特定のデータ ソースのテーブル ID。

### <a name="method-datasourcetableid"></a>メソッド datasourceTableId

インデックス化されたデータ ソースのテーブル ID を取得します。

    public TableId datasourceTableId(int cnt)

#### <a name="parameters"></a>パラメーター

cnt  

#### <a name="return-value"></a>戻り値

指定されたデータ ソースのテーブル ID。エラーが発生した場合は 0 (ゼロ)。

### <a name="method-fieldaggregation"></a>メソッド fieldAggregation

特定のフィールドが実行する集計の種類を取得します。

    public SelectionField fieldAggregation(FieldId fieldId)

#### <a name="parameters"></a>パラメーター

fieldId  

#### <a name="return-value"></a>戻り値

集約のタイプ。

### <a name="method-fielddatasource"></a>メソッド fieldDatasource

特定のフィールドの発生元データ ソースの ID を取得します。

    public int fieldDatasource(FieldId fieldId)

#### <a name="parameters"></a>パラメーター

fieldId  

#### <a name="return-value"></a>戻り値

データ ソース ID。

### <a name="method-fielddatasourceid"></a>メソッド fieldDatasourceID

特定のフィールドがマッピングされるビューでデータ ソースの ID を取得します。

    public TableId fieldDatasourceID(FieldId fieldId)

#### <a name="parameters"></a>パラメーター

fieldId  

#### <a name="return-value"></a>戻り値

データ ソース ID。

### <a name="method-fieldid"></a>メソッド fieldId

元のテーブルのフィールド ID を取得します。

    public FieldId fieldId(FieldId fieldId)

#### <a name="parameters"></a>パラメーター

fieldId  

#### <a name="return-value"></a>戻り値

基になるテーブルのフィールド ID。

### <a name="method-isaggregatedview"></a>メソッド isAggregatedView

ビューが集約されているかどうかをチェックします。

    public boolean isAggregatedView()

#### <a name="return-value"></a>戻り値

ビューが集計される場合は true。それ以外の場合は false。

### <a name="method-query"></a>メソッド query

    public Query query()

#### <a name="return-value"></a>戻り値

### <a name="method-isdataentity"></a>メソッド isDataEntity

    public boolean isDataEntity()

#### <a name="return-value"></a>戻り値

### <a name="method-isupdatable"></a>メソッド isUpdatable

    public boolean isUpdatable()

#### <a name="return-value"></a>戻り値

### <a name="method-ispublic"></a>メソッド isPublic

    public boolean isPublic()

#### <a name="return-value"></a>戻り値

### <a name="method-collectionname"></a>メソッド collectionName

    public str collectionName()

#### <a name="return-value"></a>戻り値

### <a name="method-isvirtualfield"></a>メソッド isVirtualField

    public boolean isVirtualField(str fieldName)

#### <a name="parameters"></a>パラメーター

fieldName  

#### <a name="return-value"></a>戻り値

### <a name="method-getfieldaccessmodifier"></a>メソッド getFieldAccessModifier

    public FieldAccessModifier getFieldAccessModifier(str fieldName)

#### <a name="parameters"></a>パラメーター

fieldName  

#### <a name="return-value"></a>戻り値

### <a name="method-isstaged"></a>メソッド isStaged

    public boolean isStaged()

#### <a name="return-value"></a>戻り値

### <a name="method-version"></a>メソッド version

    public str version()

#### <a name="return-value"></a>戻り値

### <a name="method-messagingrole"></a>メソッド messagingRole

    public MessagingRole messagingRole()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(TableId tableId)

#### <a name="parameters"></a>パラメーター

tableId  
クラス インスタンスの作成に使用するテーブル ID。

## <a name="class-dll"></a>クラス DLL
    class DLL extends Object

DLL クラスでは、Microsoft Windows 動的リンク ライブラリ (DLL) との通信を有効にします。

### <a name="remarks"></a>備考

Unicode DLL を使用している場合は、次の操作を行います。

-   ExtTypes :: String の代わりに ExtTypes :: WString を使用して、文字列型を指定します。
-   文字データがバイナリ構造に埋め込まれている場合は、Binary :: String ではなく Binary :: WString を使用します。
-   バイナリオ オブジェクトから文字列を読み取る必要がある場合は、Binary.string メソッドの代わりに Binary.wstring メソッドを使用します。

### <a name="examples"></a>例

次の例では、DLL および DLLFunction クラスを使用して Kernel32.dll の GetVersion API と相互運用します。 この例では、コードがサーバー上で実行されている場合にのみ必要な InteropPermission クラスの使用をアサートします。 DLL を読み込み、成功した場合は DLLFunction クラスの呼び出しから戻り値の型を設定します。

    void DLLExample() 
    { 
        Dll               dll; 
        DllFunction       dllFunc; 
        anytype           retVal; 
        InteropPermission perm; 
        perm = new InteropPermission(InteropKind::DllInterop); 
        // Grants permission to execute the DLL.new method.  
        // DLL.new runs under code access security. 
        perm.assert(); 
        dll = new Dll("Kernel32.dll"); 
        // Closes the code access permission scope. 
           CodeAccessPermission::revertAssert(); 
        if (dll != null) 
        { 
            perm = new InteropPermission(InteropKind::DllInterop); 
        // Grants permission to execute the DLLFunction.new method.  
        // DLLFunction.new runs under code access security. 
            perm.assert(); 
            dllFunc = new DllFunction(dll, "GetVersion"); 
            if (dllFunc != null) 
            { 
                 dllFunc.returns(ExtTypes::DWord); 
                retVal = dllFunc.call(); 
            } 
            // Closes the code access permission scope. 
           CodeAccessPermission::revertAssert(); 
        } 
    }

### <a name="methods"></a>メソッド

| 方法                             | 説明                                                                               |
|------------------------------------|-------------------------------------------------------------------------------------------|
| ::public static int lastDLLError() | DLL によって報告された最後のエラーを設定または取得します。                            |
| public void new(str filename)      | DLL クラスのインスタンスを作成します。                                                     |
| public void finalize()             | リソースを解放し、DLL クラスのインスタンスがリリースされる前にクリーンアップを実行します。 |

### <a name="method-lastdllerror"></a>メソッド lastDLLError

DLL によって報告された最後のエラーを設定または取得します。

    public static int lastDLLError()

#### <a name="return-value"></a>戻り値

DLL によって報告された最後のエラー。

### <a name="method-new"></a>メソッド new

DLL クラスのインスタンスを作成します。

    public void new(str filename)

#### <a name="parameters"></a>パラメーター

filename  
DLL クラスのインスタンスを作成するために使用する DLL のファイル名。

#### <a name="remarks"></a>備考

DLL 関数にアクセスするには、DLLFunction :: new メソッドの呼び出しで作成された DLL クラスのインスタンスを使用します。 攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

#### <a name="examples"></a>例

次の例では、DLL および DLLFunction クラスを使用して Kernel32.dll の GetVersion API と相互運用します。 この例では、InteropPermission クラスの使用をアサートします。 DLL を読み込み、成功した場合は DLLFunction クラスでの呼び出しから戻り値の型を設定します。

    void DLLExample() 
    { 
        Dll               dll; 
        DllFunction       dllFunc; 
        anytype           retVal; 
        InteropPermission perm; 
        perm = new InteropPermission(InteropKind::DllInterop); 
        // Grants permission to execute the DLL.new method. 
        // DLL.new runs under code access security. 
        perm.assert(); 
        dll = new Dll("Kernel32.dll"); 
        // Closes the code access permission scope. 
           CodeAccessPermission::revertAssert(); 
        if (dll != null) 
        { 
            perm = new InteropPermission(InteropKind::DllInterop); 
           // Grants permission to execute the DLLFunction.new method. 
           // DLLFunction.new runs under code access security. 
            perm.assert(); 
            dllFunc = new DllFunction(dll, "GetVersion"); 
            if (dllFunc != null) 
            { 
                 dllFunc.returns(ExtTypes::DWord); 
                retVal = dllFunc.call(); 
            } 
            // Close the code access permission scope. 
           CodeAccessPermission::revertAssert(); 
        } 
    }

### <a name="method-finalize"></a>メソッド finalize

リソースを解放し、DLL クラスのインスタンスがリリースされる前にクリーンアップを実行します。

    public void finalize()

## <a name="class-dllfunction"></a>クラス DLLFunction
    class DLLFunction extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                           | 説明                                     |
|--------------------------------------------------|-------------------------------------------------|
| public AnyType call(VarArg )                     |                                                 |
| public ExtTypes returns(\[ExtTypes returnType\]) |                                                 |
| public void new(DLL dll, str functionname)       | Object クラスの新しいインスタンスを初期化します。 |
| public void finalize()                           |                                                 |
| public void arg(VarArg )                         |                                                 |

### <a name="method-call"></a>メソッド call

    public AnyType call(VarArg )

#### <a name="parameters"></a>パラメーター



#### <a name="return-value"></a>戻り値

#### <a name="remarks"></a>備考

攻撃者が呼び出しメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

#### <a name="examples"></a>例

次の例では、DLL および DLLFunction クラスを使用して Kernel32.dll の GetVersion API と相互運用します。 コードのアクセス保護を提供する InteropPermission クラスの使用をアサートして、DLL をロードします。 これが成功した場合は、戻り値の型は DLLFunction クラスの呼び出しからを設定されます。

    { 
        Dll               dll; 
        DllFunction       dllFunc; 
        anytype           retVal; 
        InteropPermission perm; 
        perm = new InteropPermission(InteropKind::DllInterop); 
        // Grants permission to execute the DLL.new method. 
        // DLL.new is protected by code access security. 
        perm.assert(); 
        dll = new Dll("Kernel32.dll"); 
        // Closes the code access permission scope. 
        CodeAccessPermission::revertAssert(); 
        if (dll != null) 
        { 
            // Grants permission to execute the DLLFunction.new method. 
            // DLLFunction.new is protected by code access security. 
            perm = new InteropPermission(InteropKind::DllInterop); 
            perm.assert(); 
            dllFunc = new DllFunction(dll, "GetVersion"); 
            if (dllFunc != null) 
             { 
                dllFunc.returns(ExtTypes::DWord); 
                 retVal = dllFunc.call(); 
             } 
           // Closes the code access permission scope. 
           CodeAccessPermission::revertAssert(); 
        } 
    }

### <a name="method-returns"></a>メソッド returns

    public ExtTypes returns([ExtTypes returnType])

#### <a name="parameters"></a>パラメーター

returnType  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(DLL dll, str functionname)

#### <a name="parameters"></a>パラメーター

dll  

<!-- -->

functionname  

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-arg"></a>メソッド arg

    public void arg(VarArg )

#### <a name="parameters"></a>パラメーター



## <a name="class-docnode"></a>クラス DocNode
    class DocNode extends TreeNode

DocNode クラスは、ドキュメント ノードの情報や機能を提供します。

### <a name="remarks"></a>備考

このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                                                                                                            | 説明                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| public str AOTgetSource()                                                                                                                                                                         | ノードのソース コードを返します。                                                                                                   |
| public str changedBy(\[str value\])                                                                                                                                                               | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                              |
| public Date changedDate(\[Date value\])                                                                                                                                                           | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                                      |
| public str changedTime(\[str value\])                                                                                                                                                             | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                                      |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                                                                                                          | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                     |
| public str createdBy(\[str value\])                                                                                                                                                               | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                                   |
| public Date creationDate(\[Date value\])                                                                                                                                                          | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                           |
| public str creationTime(\[str value\])                                                                                                                                                            |                                                                                                                                         |
| public str description(\[str value\])                                                                                                                                                             | ドキュメント ノードの説明を設定するか返します。                                                                              |
| public str name(\[str value\])                                                                                                                                                                    | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededAccessLevel(\[int value\])                                                                                                                                                       | MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。                                                                 |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                                                                                                         | ドキュメント ノードのセキュリティ キーを設定するか返します。                                                                            |
| public str title(\[str value\])                                                                                                                                                                   | ドキュメント ノードのタイトルを設定するか返します。                                                                                    |
| ::public static DocNode findAOTElementDocNode(ApplCodeDocType HelpType, str Name, \[str ParentName\], \[int Mode\])                                                                               | Finance and Operations アプリケーション オブジェクト ツリー (AOT) で要素ドキュメント ノードの検索を実行します。                         |
| ::public static DocNode findApplicationDocNode(ApplHelpType HelpType, str Name, \[str ParentName\], \[int Mode\])                                                                                 | アプリケーション要素ドキュメント ノードの検索を実行します。                                                                        |
| ::public static DocNode findKernelDocNode(KernelHelpType HelpType, str Name, \[str ParentName\], \[int Mode\])                                                                                    | カーネル要素ドキュメント ノードの検索を実行します。                                                                              |
| ::public static DocNode getNodeDetached(UtilFileType helpType, int UtilType, str Name, \[int ParentId\], \[int Type\], \[UtilEntryLevel Utillevel\], \[boolean Forcelevel\], \[boolean OldUtil\]) | 指定したドキュメントのノードを返します。                                                                                               |
| public void AOTsetSource(str source, \[boolean isStatic\])                                                                                                                                        | ノードのソース コードを設定します。                                                                                                      |
| public void AOTedit(\[int Line\], \[int Column\])                                                                                                                                                 | このノードの適切なエディタを開きます。                                                                                             |

### <a name="method-aotgetsource"></a>メソッド AOTgetSource

ノードのソース コードを返します。

    public str AOTgetSource()

#### <a name="return-value"></a>戻り値

文字列としてのノードのソースコード。null、Nothing、nullptr、unit、ノードのソース コードがない場合は null 参照 (Visual Basic ではなし) です。

### <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

    public str changedBy([str value])

#### <a name="parameters"></a>パラメーター

値  
ドキュメント ノードを変更したユーザーとして割り当てられている値。

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

    public Date changedDate([Date value])

#### <a name="parameters"></a>パラメーター

値  
ドキュメント ノードの変更日として割り当てられている値。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された日付。

### <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

    public str changedTime([str value])

#### <a name="parameters"></a>パラメーター

値  
ドキュメント ノードの変更時刻として割り当てられている値。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された時間。

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  
構成キー ID に割り当てられている値。

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

    public str createdBy([str value])

#### <a name="parameters"></a>パラメーター

値  
ドキュメント ノードを作成したユーザーとして割り当てられている値。

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

    public Date creationDate([Date value])

#### <a name="parameters"></a>パラメーター

値  
ドキュメント ノードの作成日として割り当てられている値。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが作成された日付。

### <a name="method-creationtime"></a>メソッド creationTime

    public str creationTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-description"></a>メソッドの説明

ドキュメント ノードの説明を設定するか返します。

    public str description([str value])

#### <a name="parameters"></a>パラメーター

値  
ドキュメント ノードの説明として割り当てられている値。

#### <a name="return-value"></a>戻り値

ドキュメント ノードの説明の入力

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  
ドキュメント ノードに割り当てられている名前。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、およびクラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededaccesslevel"></a>メソッド neededAccessLevel

MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。

    public int neededAccessLevel([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

neededAccessLevel プロパティの現在の値。

#### <a name="remarks"></a>備考

AccessType システム列挙値の使用可能な値は次のとおりです。

-   AccessType::NoAccess.
-   AccessType::View.
-   AccessType::Edit.
-   AccessType::Add.
-   AccessType::Delete.

### <a name="method-securitykey"></a>メソッド securityKey

ドキュメント ノードのセキュリティ キーを設定するか返します。

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  
セキュリティ キー ID に割り当てられている値。

#### <a name="return-value"></a>戻り値

ドキュメント ノードのセキュリティ キー ID。ドキュメント ノードにセキュリティ キーが関連付けられていない場合は 0 (ゼロ)。

### <a name="method-title"></a>メソッド title

ドキュメント ノードのタイトルを設定するか返します。

    public str title([str value])

#### <a name="parameters"></a>パラメーター

値  
ドキュメント ノードに割り当てられているタイトル。

#### <a name="return-value"></a>戻り値

ドキュメント ノードのタイトル。

### <a name="method-findaotelementdocnode"></a>メソッド findAOTElementDocNode

Finance and Operations アプリケーション オブジェクト ツリー (AOT) で要素ドキュメント ノードの検索を実行します。

    public static DocNode findAOTElementDocNode(ApplCodeDocType HelpType, str Name, [str ParentName], [int Mode])

#### <a name="parameters"></a>パラメーター

HelpType  
検索に使用するモード (オプション)。

<!-- -->

氏名  
検索に使用するモード (オプション)。

<!-- -->

ParentName  
検索に使用するモード (オプション)。

<!-- -->

モード  
検索に使用するモード (オプション)。

#### <a name="return-value"></a>戻り値

検出されるノードは otherwise、null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing) です。

### <a name="method-findapplicationdocnode"></a>メソッド findApplicationDocNode

アプリケーション要素ドキュメント ノードの検索を実行します。

    public static DocNode findApplicationDocNode(ApplHelpType HelpType, str Name, [str ParentName], [int Mode])

#### <a name="parameters"></a>パラメーター

HelpType  
検索に使用するモード (オプション)。

<!-- -->

氏名  
検索に使用するモード (オプション)。

<!-- -->

ParentName  
検索に使用するモード (オプション)。

<!-- -->

モード  
検索に使用するモード (オプション)。

#### <a name="return-value"></a>戻り値

検出されるノードは null、Nothing、nullptr、unit です。ノードが検出されなかった場合は null 参照 (Visual Basic では Nothing) です。

### <a name="method-findkerneldocnode"></a>メソッド findKernelDocNode

カーネル要素ドキュメント ノードの検索を実行します。

    public static DocNode findKernelDocNode(KernelHelpType HelpType, str Name, [str ParentName], [int Mode])

#### <a name="parameters"></a>パラメーター

HelpType  
検索に使用するモード (オプション)。

<!-- -->

氏名  
検索に使用するモード (オプション)。

<!-- -->

ParentName  
検索に使用するモード (オプション)。

<!-- -->

モード  
検索に使用するモード (オプション)。

#### <a name="return-value"></a>戻り値

検出されるノードは otherwise、null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing) です。

### <a name="method-getnodedetached"></a>メソッド getNodeDetached

指定したドキュメントのノードを返します。

    public static DocNode getNodeDetached(UtilFileType helpType, int UtilType, str Name, [int ParentId], [int Type], [UtilEntryLevel Utillevel], [boolean Forcelevel], [boolean OldUtil])

#### <a name="parameters"></a>パラメーター

helpType  
引当済。省略可能です。

<!-- -->

UtilType  
引当済。省略可能です。

<!-- -->

氏名  
引当済。省略可能です。

<!-- -->

ParentId  
引当済。省略可能です。

<!-- -->

種類  
引当済。省略可能です。

<!-- -->

Utillevel  
引当済。省略可能です。

<!-- -->

Forcelevel  
引当済。省略可能です。

<!-- -->

OldUtil  
引当済。省略可能です。

#### <a name="return-value"></a>戻り値

指定したドキュメントのノードです。

### <a name="method-aotsetsource"></a>メソッド AOTsetSource

ノードのソース コードを設定します。

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a>パラメーター

ソース  
メソッドが静的かどうかを示すブール値。

<!-- -->

isStatic  
メソッドが静的かどうかを示すブール値。

### <a name="method-aotedit"></a>メソッド AOTedit

このノードの適切なエディタを開きます。

    public void AOTedit([int Line], [int Column])

#### <a name="parameters"></a>パラメーター

明細行  
カーソル位置の列 (オプション)。

<!-- -->

円柱  
カーソル位置の列 (オプション)。

#### <a name="remarks"></a>備考

ノードがメソッドである場合は、コード エディタが開きます。 ノードがドキュメンテーションの対象である場合は、ヘルプ エディタが開きます。

## <a name="class-dynamicpropertycallback"></a>クラス DynamicPropertyCallback
    class DynamicPropertyCallback

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                              | 説明 |
|---------------------------------------------------------------------|-------------|
| public boolean propChanged(str propertyName, AnyType propertyValue) |             |

### <a name="method-propchanged"></a>メソッド propChanged

    public boolean propChanged(str propertyName, AnyType propertyValue)

#### <a name="parameters"></a>パラメーター

propertyName  

<!-- -->

propertyValue  

#### <a name="return-value"></a>戻り値

## <a name="class-dynamicpropertymanager"></a>クラス DynamicPropertyManager
    class DynamicPropertyManager extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                                                                                                      | 説明                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| public DynamicPropertyCallback callbackObject()                                                                                                                                             |                                                                 |
| public str getConfigString()                                                                                                                                                                | Microsoft 社内のみで使用。                                    |
| public int hasSheetChanged()                                                                                                                                                                | Microsoft 社内のみで使用。                                    |
| public Struct propertyValues()                                                                                                                                                              |                                                                 |
| public void allowEdit(str name, boolean allow)                                                                                                                                              |                                                                 |
| public void updateValue(str propertyname, str value)                                                                                                                                        |                                                                 |
| public void new()                                                                                                                                                                           | DynamicPropertyManager クラスの新しいインスタンスを初期化します。 |
| public void getPropertySheet(str configString, boolean canWebletTypeChange)                                                                                                                 | Microsoft 社内のみで使用。                                    |
| public void noProperties()                                                                                                                                                                  |                                                                 |
| public void allowDisplay(str name, boolean allow)                                                                                                                                           |                                                                 |
| public void refresh()                                                                                                                                                                       |                                                                 |
| public void setProperties(int propertySetId, str caption, Struct values, \[Struct defaultValues\], \[Struct categories\], \[DynamicPropertyCallback callbackObject\], \[boolean setFocus\]) |                                                                 |

### <a name="method-callbackobject"></a>メソッド callbackObject

    public DynamicPropertyCallback callbackObject()

#### <a name="return-value"></a>戻り値

### <a name="method-getconfigstring"></a>メソッド getConfigString

Microsoft 社内のみで使用。

    public str getConfigString()

#### <a name="return-value"></a>戻り値

コンフィギュレーションの文字列。

### <a name="method-hassheetchanged"></a>メソッド hasSheetChanged

Microsoft 社内のみで使用。

    public int hasSheetChanged()

#### <a name="return-value"></a>戻り値

シートが変更されたかどうかを示す値。

### <a name="method-propertyvalues"></a>メソッド propertyValues

    public Struct propertyValues()

#### <a name="return-value"></a>戻り値

### <a name="method-allowedit"></a>メソッド allowEdit

    public void allowEdit(str name, boolean allow)

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

allow  

### <a name="method-updatevalue"></a>メソッド updateValue

    public void updateValue(str propertyname, str value)

#### <a name="parameters"></a>パラメーター

propertyname  

<!-- -->

値  

### <a name="method-new"></a>メソッド new

DynamicPropertyManager クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-getpropertysheet"></a>メソッド getPropertySheet

Microsoft 社内のみで使用。

    public void getPropertySheet(str configString, boolean canWebletTypeChange)

#### <a name="parameters"></a>パラメーター

configString  
Weblet タイプが変更されたかどうかを示す値。

<!-- -->

canWebletTypeChange  
Weblet タイプが変更されたかどうかを示す値。

### <a name="method-noproperties"></a>メソッド noProperties

    public void noProperties()

### <a name="method-allowdisplay"></a>メソッド allowDisplay

    public void allowDisplay(str name, boolean allow)

#### <a name="parameters"></a>パラメーター

名前  

<!-- -->

allow  

### <a name="method-refresh"></a>メソッド refresh

    public void refresh()

### <a name="method-setproperties"></a>メソッド setProperties

    public void setProperties(int propertySetId, str caption, Struct values, [Struct defaultValues], [Struct categories], [DynamicPropertyCallback callbackObject], [boolean setFocus])

#### <a name="parameters"></a>パラメーター

propertySetId  

<!-- -->

caption  

<!-- -->

値  

<!-- -->

defaultValues  

<!-- -->

カテゴリ  

<!-- -->

callbackObject  

<!-- -->

setFocus  






