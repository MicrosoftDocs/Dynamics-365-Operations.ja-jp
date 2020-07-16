---
title: PartList クラス
description: このトピックでは、PartList クラスについて説明します。
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
ms.openlocfilehash: d95ebc00a2b19d63e4b34cce95b580ed33de657e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502537"
---
# <a name="class-partlist"></a>クラス PartList

[!include [banner](../../includes/banner.md)]

```xpp
class PartList extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                        | 説明                                     |
|-----------------------------------------------|-------------------------------------------------|
| public xFormRun getPartById(int id)           |                                                 |
| public FormControl getPartControlById(int id) |                                                 |
| public int partCount()                        |                                                 |
| public void new(xFormRun form)                | Object クラスの新しいインスタンスを初期化します。 |
| public void finalize()                        |                                                 |

## <a name="method-getpartbyid"></a>メソッド getPartById

```xpp
public xFormRun getPartById(int id)
```

### <a name="parameters---getpartbyid"></a>パラメーター - getPartById

id  

### <a name="return-value---getpartbyid"></a>戻り値 - getPartById

## <a name="method-getpartcontrolbyid"></a>メソッド getPartControlById

```xpp
public FormControl getPartControlById(int id)
```

### <a name="parameters---getpartcontrolbyid"></a>パラメーター - getPartControlById

id  

### <a name="return-value---getpartcontrolbyid"></a>戻り値 - getPartControlById

## <a name="method-partcount"></a>メソッド partCount

```xpp
public int partCount()
```

### <a name="return-value---partcount"></a>戻り値 - partCount

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(xFormRun form)
```

### <a name="parameters---new"></a>パラメーター - new

フォーム  

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

