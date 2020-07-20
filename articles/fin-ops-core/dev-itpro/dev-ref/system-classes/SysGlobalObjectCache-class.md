---
title: SysGlobalObjectCache クラス
description: このトピックでは、SysGlobalObjectCache クラスについて説明します。
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
ms.openlocfilehash: efb8fdcc1323738717ee95407931a8ce75395845
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502793"
---
# <a name="class-sysglobalobjectcache"></a>クラス SysGlobalObjectCache

[!include [banner](../../includes/banner.md)]

```xpp
class SysGlobalObjectCache extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                           | 説明                                                   |
|----------------------------------------------------------------------------------|---------------------------------------------------------------|
| public container find(GlobalObjectCacheScope scope, container key)               |                                                               |
| public void finalize()                                                           |                                                               |
| public void remove(GlobalObjectCacheScope scope, container key)                  |                                                               |
| public void print(GlobalObjectCacheScope scope)                                  |                                                               |
| public void clear(GlobalObjectCacheScope scope)                                  |                                                               |
| ::public static void clearAllCaches()                                            |                                                               |
| public void new()                                                                | SysGlobalObjectCache クラスの新しいインスタンスを初期化します。 |
| public void insert(GlobalObjectCacheScope scope, container key, container value) |                                                               |

## <a name="method-find"></a>メソッド find

```xpp
public container find(GlobalObjectCacheScope scope, container key)
```

### <a name="parameters---find"></a>パラメーター - find

scope  

<!-- -->

キー  

### <a name="return-value---find"></a>戻り値 - find

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-remove"></a>メソッド remove

```xpp
public void remove(GlobalObjectCacheScope scope, container key)
```

### <a name="parameters---remove"></a>パラメーター - remove

scope  

<!-- -->

キー  

## <a name="method-print"></a>メソッド print

```xpp
public void print(GlobalObjectCacheScope scope)
```

### <a name="parameters---print"></a>パラメーター - print

scope  

## <a name="method-clear"></a>メソッド clear

```xpp
public void clear(GlobalObjectCacheScope scope)
```

### <a name="parameters---clear"></a>パラメーター - clear

scope  

## <a name="method-clearallcaches"></a>メソッド clearAllCaches

```xpp
public static void clearAllCaches()
```

## <a name="method-new"></a>メソッド new

SysGlobalObjectCache クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-insert"></a>メソッド insert

```xpp
public void insert(GlobalObjectCacheScope scope, container key, container value)
```

### <a name="parameters---insert"></a>パラメーター - insert

scope  

<!-- -->

キー  

<!-- -->

値  

