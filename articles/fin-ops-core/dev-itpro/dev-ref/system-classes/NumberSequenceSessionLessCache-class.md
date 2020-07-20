---
title: NumberSequenceSessionLessCache クラス
description: このトピックでは、NumberSequenceSessionLessCache クラスについて説明します。
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
ms.openlocfilehash: 9e93d0ae641a0c8edf49c4bce1c98717a369aec1
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502567"
---
# <a name="class-numbersequencesessionlesscache"></a>クラス NumberSequenceSessionLessCache

[!include [banner](../../includes/banner.md)]

```xpp
class NumberSequenceSessionLessCache extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                         | 説明                                                             |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| public int getNumFromCache(Common numbersequencetable)                         |                                                                         |
| public int valueLastNumFromCache(Int64 numbersequecerecordid)                  |                                                                         |
| public int valueNextNumFromCache(Int64 numbersequecerecordid)                  |                                                                         |
| public void flushCache(Int64 numbersequecerecordid)                            |                                                                         |
| public void fillCache(Int64 numbersequecerecordid, int nextRec, int blockSize) |                                                                         |
| public void new()                                                              | NumberSequenceSessionLessCache クラスの新しいインスタンスを初期化します。 |

## <a name="method-getnumfromcache"></a>メソッド getNumFromCache

```xpp
public int getNumFromCache(Common numbersequencetable)
```

### <a name="parameters---getnumfromcache"></a>パラメーター - getNumFromCache

numbersequencetable  

### <a name="return-value---getnumfromcache"></a>戻り値 - getNumFromCache

## <a name="method-valuelastnumfromcache"></a>メソッド valueLastNumFromCache

```xpp
public int valueLastNumFromCache(Int64 numbersequecerecordid)
```

### <a name="parameters---valuelastnumfromcache"></a>パラメーター - valueNextNumFromCache

numbersequecerecordid  

### <a name="return-value---valuelastnumfromcache"></a>戻り値 - valueNextNumFromCache

## <a name="method-valuenextnumfromcache"></a>メソッド valueNextNumFromCache

```xpp
public int valueNextNumFromCache(Int64 numbersequecerecordid)
```

### <a name="parameters---valuenextnumfromcache"></a>パラメーター - valueNextNumFromCache

numbersequecerecordid  

### <a name="return-value---valuenextnumfromcache"></a>戻り値 - valueNextNumFromCache

## <a name="method-flushcache"></a>メソッド flushCache

```xpp
public void flushCache(Int64 numbersequecerecordid)
```

### <a name="parameters---flushcache"></a>パラメーター - flushCache

numbersequecerecordid  

## <a name="method-fillcache"></a>メソッド fillCache

```xpp
public void fillCache(Int64 numbersequecerecordid, int nextRec, int blockSize)
```

### <a name="parameters---fillcache"></a>パラメーター - fillCache

numbersequecerecordid  

<!-- -->

nextRec  

<!-- -->

blockSize  

## <a name="method-new"></a>メソッド new

NumberSequenceSessionLessCache クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```


