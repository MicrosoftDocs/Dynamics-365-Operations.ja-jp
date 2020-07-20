---
title: profiler クラス
description: このトピックでは、profiler クラスについて説明します。
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
ms.openlocfilehash: 807bb7724ded4b43cef08fb8808399d23e3467aa
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502771"
---
# <a name="class-profiler"></a>クラス プロファイラー

[!include [banner](../../includes/banner.md)]

```xpp
class profiler extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                                                                                                                                                                                                                                                                                                                                                          | 説明                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| public int collected()                                                                                                                                                                                                                                                                                                                                                                                                                                          |                                                      |
| public int flushInterval(\[int interval\])                                                                                                                                                                                                                                                                                                                                                                                                                      |                                                      |
| public AnyType profileOff()                                                                                                                                                                                                                                                                                                                                                                                                                                     |                                                      |
| public AnyType profileOn(str runId, \[int traceDepth\])                                                                                                                                                                                                                                                                                                                                                                                                         |                                                      |
| public str tempPath()                                                                                                                                                                                                                                                                                                                                                                                                                                           |                                                      |
| public str toString()                                                                                                                                                                                                                                                                                                                                                                                                                                           | 現在のオブジェクトを表す文字列を返します。 |
| ::public static AnyType profilerAlreadyOn()                                                                                                                                                                                                                                                                                                                                                                                                                     |                                                      |
| public void flush()                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                      |
| public void new()                                                                                                                                                                                                                                                                                                                                                                                                                                               | profiler クラスの新しいインスタンスを初期化します。    |
| public void flushData(int lineNumber, str path, int microSecs, int sequenceNumber, int parentSequenceNumber, int selectCalls, int selectBytes, int selectRows, int sqlWaitTime, int aosWaitTime, int sqlInserts, int sqlUpdates, int sqlDeletes, int aosInCalls, int aosOutCalls, int aosInBytes, int aosOutBytes, \[int sqlInsertBytes\], \[int sqlInsertRows\], \[int sqlUpdateBytes\], \[int sqlUpdateRows\], \[int sqlDeleteBytes\], \[int sqlDeleteRows\]) |                                                      |

## <a name="method-collected"></a>メソッド collected

```xpp
public int collected()
```

### <a name="return-value---collected"></a>戻り値 - collected

## <a name="method-flushinterval"></a>メソッド flushInterval

```xpp
public int flushInterval([int interval])
```

### <a name="parameters---flushinterval"></a>パラメーター - flushInterval

interval  

### <a name="return-value---flushinterval"></a>戻り値 - flushInterval

## <a name="method-profileoff"></a>メソッド profileOff

```xpp
public AnyType profileOff()
```

### <a name="return-value---profileoff"></a>戻り値 - profileOff

## <a name="method-profileon"></a>メソッド profileOn

```xpp
public AnyType profileOn(str runId, [int traceDepth])
```

### <a name="parameters---profileon"></a>パラメーター - profileOn

runId  

<!-- -->

traceDepth  

### <a name="return-value---profileon"></a>戻り値 - profileOn

## <a name="method-temppath"></a>メソッド tempPath

```xpp
public str tempPath()
```

### <a name="return-value---temppath"></a>戻り値 - tempPath

## <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

現在のオブジェクトを表す文字列。

### <a name="remarks---tostring"></a>備考 - toString

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、クラスのインスタンスは、インスタンスまたは静的などの、メソッド名およびメソッドのタイプを返します。

## <a name="method-profileralreadyon"></a>メソッド profilerAlreadyOn

```xpp
public static AnyType profilerAlreadyOn()
```

### <a name="return-value---profileralreadyon"></a>戻り値 - profilerAlreadyOn

## <a name="method-flush"></a>メソッド flush

```xpp
public void flush()
```

## <a name="method-new"></a>メソッド new

profiler クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-flushdata"></a>メソッド flushData

```xpp
public void flushData(int lineNumber, str path, int microSecs, int sequenceNumber, int parentSequenceNumber, int selectCalls, int selectBytes, int selectRows, int sqlWaitTime, int aosWaitTime, int sqlInserts, int sqlUpdates, int sqlDeletes, int aosInCalls, int aosOutCalls, int aosInBytes, int aosOutBytes, [int sqlInsertBytes], [int sqlInsertRows], [int sqlUpdateBytes], [int sqlUpdateRows], [int sqlDeleteBytes], [int sqlDeleteRows])
```

### <a name="parameters---flushdata"></a>パラメーター - flushData

lineNumber  

<!-- -->

path  

<!-- -->

microSecs  

<!-- -->

sequenceNumber  

<!-- -->

parentSequenceNumber  

<!-- -->

selectCalls  

<!-- -->

selectBytes  

<!-- -->

selectRows  

<!-- -->

sqlWaitTime  

<!-- -->

aosWaitTime  

<!-- -->

sqlInserts  

<!-- -->

sqlUpdates  

<!-- -->

sqlDeletes  

<!-- -->

aosInCalls  

<!-- -->

aosOutCalls  

<!-- -->

aosInBytes  

<!-- -->

aosOutBytes  

<!-- -->

sqlInsertBytes  

<!-- -->

sqlInsertRows  

<!-- -->

sqlUpdateBytes  

<!-- -->

sqlUpdateRows  

<!-- -->

sqlDeleteBytes  

<!-- -->

sqlDeleteRows  

