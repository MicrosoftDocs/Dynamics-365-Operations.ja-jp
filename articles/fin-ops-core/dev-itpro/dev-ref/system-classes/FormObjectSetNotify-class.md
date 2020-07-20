---
title: FormObjectSetNotify クラス
description: このトピックでは、FormObjectSetNotify クラスについて説明します。
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
ms.openlocfilehash: 221c3a33bf7eb41c82497a2cdd28267e3f63df1e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502921"
---
# <a name="class-formobjectsetnotify"></a>クラス FormObjectSetNotify

[!include [banner](../../includes/banner.md)]

```xpp
class FormObjectSetNotify extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                                                                               | 説明                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| public boolean onLeave(FormObjectSet sender)                                                                                                                                         |                                                              |
| public int onRequestCacheSize(FormObjectSet sender)                                                                                                                                  |                                                              |
| public void onCacheChanged(FormObjectSet sender, NotifyCacheChangeType cacheChangeType)                                                                                              |                                                              |
| public void new()                                                                                                                                                                    | FormObjectSetNotify クラスの新しいインスタンスを初期化します。 |
| public void onCurrentChanged(FormObjectSet sender, int position)                                                                                                                     |                                                              |
| public void onActive(FormObjectSet sender)                                                                                                                                           |                                                              |
| public void onPagingParametersChanged(FormObjectSet sender, boolean pagingEnabled, int startRowIndex, int pageSize)                                                                  |                                                              |
| public void finalize()                                                                                                                                                               |                                                              |
| public void onRuntimeMetadataChanged(FormObjectSet sender, str changedDatasourceName, str referencedDatasourceName, FieldId changedFieldId, DataSourceMetadataChangeType changeType) |                                                              |
| public void onRefresh(FormObjectSet sender)                                                                                                                                          |                                                              |
| public void onMarkingChanged(FormObjectSet sender, Array ids)                                                                                                                        |                                                              |

## <a name="method-onleave"></a>メソッド onLeave

```xpp
public boolean onLeave(FormObjectSet sender)
```

### <a name="parameters---onleave"></a>パラメーター - onLeave

sender  

### <a name="return-value---onleave"></a>戻り値 - onLeave

## <a name="method-onrequestcachesize"></a>メソッド onRequestCacheSize

```xpp
public int onRequestCacheSize(FormObjectSet sender)
```

### <a name="parameters---onrequestcachesize"></a>パラメーター - onRequestCacheSize

sender  

### <a name="return-value---onrequestcachesize"></a>戻り値 - onRequestCacheSize

## <a name="method-oncachechanged"></a>メソッド onCacheChanged

```xpp
public void onCacheChanged(FormObjectSet sender, NotifyCacheChangeType cacheChangeType)
```

### <a name="parameters---oncachechanged"></a>パラメーター - onCacheChanged

sender  

<!-- -->

cacheChangeType  

## <a name="method-new"></a>メソッド new

FormObjectSetNotify クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-oncurrentchanged"></a>メソッド onCurrentChanged

```xpp
public void onCurrentChanged(FormObjectSet sender, int position)
```

### <a name="parameters---oncurrentchanged"></a>パラメーター - onCurrentChanged

sender  

<!-- -->

職位  

## <a name="method-onactive"></a>メソッド onActive

```xpp
public void onActive(FormObjectSet sender)
```

### <a name="parameters---onactive"></a>パラメーター - onActive

sender  

## <a name="method-onpagingparameterschanged"></a>メソッド onPagingParametersChanged

```xpp
public void onPagingParametersChanged(FormObjectSet sender, boolean pagingEnabled, int startRowIndex, int pageSize)
```

### <a name="parameters---onpagingparameterschanged"></a>パラメーター - onPagingParametersChanged

sender  

<!-- -->

pagingEnabled  

<!-- -->

startRowIndex  

<!-- -->

pageSize  

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-onruntimemetadatachanged"></a>メソッド onRuntimeMetadataChanged

```xpp
public void onRuntimeMetadataChanged(FormObjectSet sender, str changedDatasourceName, str referencedDatasourceName, FieldId changedFieldId, DataSourceMetadataChangeType changeType)
```

### <a name="parameters---onruntimemetadatachanged"></a>パラメーター - onRuntimeMetadataChanged

sender  

<!-- -->

changedDatasourceName  

<!-- -->

referencedDatasourceName  

<!-- -->

changedFieldId  

<!-- -->

changeType  

## <a name="method-onrefresh"></a>メソッド onRefresh

```xpp
public void onRefresh(FormObjectSet sender)
```

### <a name="parameters---onrefresh"></a>パラメーター - onRefresh

sender  

## <a name="method-onmarkingchanged"></a>メソッド onMarkingChanged

```xpp
public void onMarkingChanged(FormObjectSet sender, Array ids)
```

### <a name="parameters---onmarkingchanged"></a>パラメーター - onMarkingChanged

sender  

<!-- -->

ids  

