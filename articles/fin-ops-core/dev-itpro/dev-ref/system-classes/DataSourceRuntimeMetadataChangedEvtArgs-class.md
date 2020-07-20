---
title: DataSourceRuntimeMetadataChangedEvtArgs クラス
description: このトピックでは、DataSourceRuntimeMetadataChangedEvtArgs クラスについて説明します。
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
ms.openlocfilehash: e26a3b799530d73eb6b958a56116c4fe3efa6a1e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502731"
---
# <a name="class-datasourceruntimemetadatachangedevtargs"></a>クラス DataSourceRuntimeMetadataChangedEvtArgs

[!include [banner](../../includes/banner.md)]

```xpp
class DataSourceRuntimeMetadataChangedEvtArgs extends ManagedEventArgs
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                                    | 説明                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| public str changedDataSourceName()                                                                                                        |                                                           |
| public FieldId changedFieldId()                                                                                                           |                                                           |
| public DataSourceMetadataChangeType changeType()                                                                                          |                                                           |
| public str referencedDataSourceName()                                                                                                     |                                                           |
| public void new(str changedDatasourceName, str referencedDatasourceName, FieldId changedFieldId, DataSourceMetadataChangeType changeType) | ManagedEventArgs クラスの新しいインスタンスを初期化します。 |
| public void finalize()                                                                                                                    |                                                           |

## <a name="method-changeddatasourcename"></a>メソッド changedDataSourceName

```xpp
public str changedDataSourceName()
```

### <a name="return-value---changeddatasourcename"></a>戻り値 - changedDataSourceName

## <a name="method-changedfieldid"></a>メソッド changedFieldId

```xpp
public FieldId changedFieldId()
```

### <a name="return-value---changedfieldid"></a>戻り値 - changedFieldId

## <a name="method-changetype"></a>メソッド changeType

```xpp
public DataSourceMetadataChangeType changeType()
```

### <a name="return-value---changetype"></a>戻り値 - changeType

## <a name="method-referenceddatasourcename"></a>メソッド referencedDataSourceName

```xpp
public str referencedDataSourceName()
```

### <a name="return-value---referenceddatasourcename"></a>戻り値 - referencedDataSourceName

## <a name="method-new"></a>メソッド new

ManagedEventArgs クラスの新しいインスタンスを初期化します。

```xpp
public void new(str changedDatasourceName, str referencedDatasourceName, FieldId changedFieldId, DataSourceMetadataChangeType changeType)
```

### <a name="parameters---new"></a>パラメーター - new

changedDatasourceName  

<!-- -->

referencedDatasourceName  

<!-- -->

changedFieldId  

<!-- -->

changeType  

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

