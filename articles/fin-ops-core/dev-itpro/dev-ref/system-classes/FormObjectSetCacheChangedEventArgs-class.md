---
title: FormObjectSetCacheChangedEventArgs クラス
description: このトピックでは、FormObjectSetCacheChangedEventArgs クラスについて説明します。
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
ms.openlocfilehash: 81c1bfb6d97f46f7782e7c8f7484c515d2e9c53b
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502925"
---
# <a name="class-formobjectsetcachechangedeventargs"></a>クラス FormObjectSetCacheChangedEventArgs

[!include [banner](../../includes/banner.md)]

```xpp
class FormObjectSetCacheChangedEventArgs extends ManagedEventArgs
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                 | 説明                                               |
|--------------------------------------------------------|-----------------------------------------------------------|
| public NotifyCacheChangeType cacheChangeType()         |                                                           |
| public void finalize()                                 |                                                           |
| public void new(NotifyCacheChangeType cacheChangeType) | ManagedEventArgs クラスの新しいインスタンスを初期化します。 |

## <a name="method-cachechangetype"></a>メソッド cacheChangeType

```xpp
public NotifyCacheChangeType cacheChangeType()
```

### <a name="return-value---cachechangetype"></a>戻り値 - cacheChangeType

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-new"></a>メソッド new

ManagedEventArgs クラスの新しいインスタンスを初期化します。

```xpp
public void new(NotifyCacheChangeType cacheChangeType)
```

### <a name="parameters---new"></a>パラメーター - new

cacheChangeType  

