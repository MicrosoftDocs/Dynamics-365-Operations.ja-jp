---
title: DataEntityDataSourceRuntimeContext クラス
description: このトピックでは、DataEntityDataSourceRuntimeContext クラスについて説明します。
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
ms.openlocfilehash: 3c16464e20c3245a1a75f4ad82103238ed4e6f46
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502744"
---
# <a name="class-dataentitydatasourceruntimecontext"></a>クラス DataEntityDataSourceRuntimeContext

[!include [banner](../../includes/banner.md)]


```xpp
class DataEntityDataSourceRuntimeContext extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

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

## <a name="method-name"></a>メソッド名

```xpp
public str name()
```

### <a name="return-value---name"></a>戻り値 - name

## <a name="method-id"></a>メソッド id

```xpp
public int id()
```

### <a name="return-value---id"></a>戻り値 - id

## <a name="method-getbuffer"></a>メソッド getBuffer

```xpp
public Common getBuffer()
```

### <a name="return-value---getbuffer"></a>戻り値 - getBuffer

## <a name="method-getdatabaseoperation"></a>メソッド getDatabaseOperation

```xpp
public DataEntityDatabaseOperation getDatabaseOperation()
```

### <a name="return-value---getdatabaseoperation"></a>戻り値 - getDatabaseOperation

## <a name="method-getcompany"></a>メソッド getCompany

```xpp
public str getCompany()
```

### <a name="return-value---getcompany"></a>戻り値 - getCompany

## <a name="method-getdatasaved"></a>メソッド getDataSaved

```xpp
public boolean getDataSaved()
```

### <a name="return-value---getdatasaved"></a>戻り値 - getDataSaved

## <a name="method-skipdatamethods"></a>メソッド skipDataMethods

```xpp
public boolean skipDataMethods([boolean skip])
```

### <a name="parameters---skipdatamethods"></a>パラメーター - skipDataMethods

skip  

### <a name="return-value---skipdatamethods"></a>戻り値 - skipDataMethods

## <a name="method-skipdeletemethod"></a>メソッド skipDeleteMethod

```xpp
public boolean skipDeleteMethod([boolean b])
```

### <a name="parameters---skipdeletemethod"></a>パラメーター - skipDeleteMethod

b  

### <a name="return-value---skipdeletemethod"></a>戻り値 - skipDeleteMethod

## <a name="method-skipvalidatewrite"></a>メソッド skipValidateWrite

```xpp
public boolean skipValidateWrite([boolean skip])
```

### <a name="parameters---skipvalidatewrite"></a>パラメーター - skipValidateWrite

skip  

### <a name="return-value---skipvalidatewrite"></a>戻り値 - skipValidateWrite

## <a name="method-skipvalidatedelete"></a>メソッド skipValidateDelete

```xpp
public boolean skipValidateDelete([boolean skip])
```

### <a name="parameters---skipvalidatedelete"></a>パラメーター - skipValidateDelete

skip  

### <a name="return-value---skipvalidatedelete"></a>戻り値 - skipValidateDelete

## <a name="method-skipinitvalue"></a>メソッド skipInitValue

```xpp
public boolean skipInitValue([boolean skip])
```

### <a name="parameters---skipinitvalue"></a>パラメーター - skipInitValue

skip  

### <a name="return-value---skipinitvalue"></a>戻り値 - skipInitValue

## <a name="method-skipdefaultrow"></a>メソッド skipDefaultRow

```xpp
public boolean skipDefaultRow([boolean skip])
```

### <a name="parameters---skipdefaultrow"></a>パラメーター - skipDefaultRow

skip  

### <a name="return-value---skipdefaultrow"></a>戻り値 - skipDefaultRow

## <a name="method-readonly"></a>メソッド readOnly

```xpp
public boolean readOnly()
```

### <a name="return-value---readonly"></a>戻り値 - readOnly

## <a name="method-onetomany"></a>メソッド oneToMany

```xpp
public boolean oneToMany()
```

### <a name="return-value---onetomany"></a>戻り値 - oneToMany

## <a name="method-optional"></a>メソッド optional

```xpp
public boolean optional()
```

### <a name="return-value---optional"></a>戻り値 - optional

## <a name="method-dateeffective"></a>メソッド dateEffective

```xpp
public boolean dateEffective()
```

### <a name="return-value---dateeffective"></a>戻り値 - dateEffective

## <a name="method-conflictdetectioninvoked"></a>メソッド conflictDetectionInvoked

```xpp
public boolean conflictDetectionInvoked([boolean found])
```

### <a name="parameters---conflictdetectioninvoked"></a>パラメーター - conflictDetectionInvoked

found  

### <a name="return-value---conflictdetectioninvoked"></a>戻り値 - conflictDetectionInvoked

## <a name="method-new"></a>メソッド new

```xpp
public void new(Common dataSourceBuffer, str dataSourceName, int dataSourceId)
```

### <a name="parameters---new"></a>パラメーター - new

dataSourceBuffer  

<!-- -->

dataSourceName  

<!-- -->

dataSourceId  

## <a name="method-setcompany"></a>メソッド setCompany

```xpp
public void setCompany(str company)
```

### <a name="parameters---setcompany"></a>パラメーター - setCompany

会社  

## <a name="method-setbuffer"></a>メソッド setBuffer

```xpp
public void setBuffer(Common buffer)
```

### <a name="parameters---setbuffer"></a>パラメーター - setBuffer

バッファ  

## <a name="method-setdatabaseoperation"></a>メソッド setDatabaseOperation

```xpp
public void setDatabaseOperation(DataEntityDatabaseOperation dbOperation)
```

### <a name="parameters---setdatabaseoperation"></a>パラメーター - setDatabaseOperation

dbOperation  

## <a name="method-setdatasaved"></a>メソッド setDataSaved

```xpp
public void setDataSaved(boolean saved)
```

### <a name="parameters---setdatasaved"></a>パラメーター - setDataSaved

 が保存されました  

