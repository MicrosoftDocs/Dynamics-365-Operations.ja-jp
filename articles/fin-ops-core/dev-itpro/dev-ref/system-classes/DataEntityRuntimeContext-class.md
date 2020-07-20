---
title: DataEntityRuntimeContext クラス
description: このトピックでは、DataEntityRuntimeContext クラスについて説明します。
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
ms.openlocfilehash: 856249f9c477c8600859bb89b3c41b02d47d3678
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502741"
---
# <a name="class-dataentityruntimecontext"></a>クラス DataEntityRuntimeContext

[!include [banner](../../includes/banner.md)]

```xpp
class DataEntityRuntimeContext extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                               | 説明 |
|------------------------------------------------------------------------------------------------------|-------------|
| public DataEntityDatabaseOperation getDatabaseOperation()                                            |             |
| public AnyType getCustomProperty(str name)                                                           |             |
| public Common getEntityRecord()                                                                      |             |
| public DataEntityDataSourceRuntimeContext getRuntimeContextByName(str datasourceName)                |             |
| public void new(DataEntityDatabaseOperation operation, Common record, DataEntityPersister persister) |             |
| public void setCustomProperty(str name, AnyType obj)                                                 |             |

## <a name="method-getdatabaseoperation"></a>メソッド getDatabaseOperation

```xpp
public DataEntityDatabaseOperation getDatabaseOperation()
```

### <a name="return-value---getdatabaseoperation"></a>戻り値 - getDatabaseOperation

## <a name="method-getcustomproperty"></a>メソッド getCustomProperty

```xpp
public AnyType getCustomProperty(str name)
```

### <a name="parameters---getcustomproperty"></a>パラメーター - getCustomProperty

名前  

### <a name="return-value---getcustomproperty"></a>戻り値 - getCustomProperty

## <a name="method-getentityrecord"></a>メソッド getEntityRecord

```xpp
public Common getEntityRecord()
```

### <a name="return-value---getentityrecord"></a>戻り値 - getEntityRecord

## <a name="method-getruntimecontextbyname"></a>メソッド getRuntimeContextByName

```xpp
public DataEntityDataSourceRuntimeContext getRuntimeContextByName(str datasourceName)
```

### <a name="parameters---getruntimecontextbyname"></a>パラメーター - getRuntimeContextByName

datasourceName  

### <a name="return-value---getruntimecontextbyname"></a>戻り値 - getRuntimeContextByName

## <a name="method-new"></a>メソッド new

```xpp
public void new(DataEntityDatabaseOperation operation, Common record, DataEntityPersister persister)
```

### <a name="parameters---new"></a>パラメーター - new

工程  

<!-- -->

記録  

<!-- -->

persister  

## <a name="method-setcustomproperty"></a>メソッド setCustomProperty

```xpp
public void setCustomProperty(str name, AnyType obj)
```

### <a name="parameters---setcustomproperty"></a>パラメーター - setCustomProperty

名前  

<!-- -->

obj  

