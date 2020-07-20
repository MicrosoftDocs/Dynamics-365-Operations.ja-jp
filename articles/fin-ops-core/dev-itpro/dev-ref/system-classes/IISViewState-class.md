---
title: IISViewState クラス
description: このトピックでは、IISViewState クラスについて説明します。
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
ms.openlocfilehash: df5acdeb301ed7881515d8f5a4d8da9f2667acc1
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502903"
---
# <a name="class-iisviewstate"></a>クラス IISViewState

[!include [banner](../../includes/banner.md)]

```xpp
class IISViewState extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                         | 説明                                           |
|------------------------------------------------|-------------------------------------------------------|
| public boolean viewStateContains(str key)      |                                                       |
| public str viewStateItem(str key, \[str val\]) |                                                       |
| public void finalize()                         |                                                       |
| public void viewStateDelete(str key)           |                                                       |
| public void new()                              | IISViewState クラスの新しいインスタンスを初期化します。 |

## <a name="method-viewstatecontains"></a>メソッド viewStateContains

```xpp
public boolean viewStateContains(str key)
```

### <a name="parameters---viewstatecontains"></a>パラメーター - viewStateContains

キー  

### <a name="return-value---viewstatecontains"></a>戻り値 - viewStateContains

## <a name="method-viewstateitem"></a>メソッド viewStateItem

```xpp
public str viewStateItem(str key, [str val])
```

### <a name="parameters---viewstateitem"></a>パラメーター - viewStateItem

キー  

<!-- -->

val  

### <a name="return-value---viewstateitem"></a>戻り値 - viewStateItem

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-viewstatedelete"></a>メソッド viewStateDelete

```xpp
public void viewStateDelete(str key)
```

### <a name="parameters---viewstatedelete"></a>パラメーター - viewStateDelete

キー  

## <a name="method-new"></a>メソッド new

IISViewState クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

