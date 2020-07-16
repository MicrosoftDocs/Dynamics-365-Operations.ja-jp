---
title: xClassTrace クラス
description: このトピックでは、xClassTrace クラスについて説明します。
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
ms.openlocfilehash: 63a0982157dc58b907ccde57b7cd33b9d7f3fdd5
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502767"
---
# <a name="class-xclasstrace"></a>クラス xClassTrace

[!include [banner](../../includes/banner.md)]

```xpp
class xClassTrace extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                                                                             | 説明                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| ::public static boolean isTracingEnabled(\[Int64 keyword\], \[int level\])                                                                                                         |                                                      |
| ::public static boolean isTracingStarted()                                                                                                                                         |                                                      |
| ::public static str kernelCustomerId()                                                                                                                                             |                                                      |
| ::public static Guid kernelRequestId()                                                                                                                                             |                                                      |
| ::public static str kernelSessionId()                                                                                                                                              |                                                      |
| ::public static str kernelUserId()                                                                                                                                                 |                                                      |
| ::public static int start(str logFileName, \[int logBufferSize\], \[int minBuffers\], \[int maxBuffers\], \[Int64 keywords\], \[int maxFileSize\], \[boolean useCircularLogging\]) |                                                      |
| ::public static int stop()                                                                                                                                                         |                                                      |
| ::public static void logMessage(str message)                                                                                                                                       |                                                      |
| public void endMarker(str transactionName)                                                                                                                                         |                                                      |
| public void beginMarker(str transactionName)                                                                                                                                       |                                                      |
| ::public static void logComponentMessage(str component, str message)                                                                                                               |                                                      |
| public void finalize()                                                                                                                                                             |                                                      |
| public void new()                                                                                                                                                                  | xClassTrace クラスの新しいインスタンスを初期化します。 |

## <a name="method-istracingenabled"></a>メソッド isTracingEnabled

```xpp
public static boolean isTracingEnabled([Int64 keyword], [int level])
```

### <a name="parameters---istracingenabled"></a>パラメーター - isTracingEnabled

キーワード  

<!-- -->

level  

### <a name="return-value---istracingenabled"></a>戻り値 - isTracingEnabled

## <a name="method-istracingstarted"></a>メソッド isTracingStarted

```xpp
public static boolean isTracingStarted()
```

### <a name="return-value---istracingstarted"></a>戻り値 - isTracingStarted

## <a name="method-kernelcustomerid"></a>メソッド kernelCustomerId

```xpp
public static str kernelCustomerId()
```

### <a name="return-value---kernelcustomerid"></a>戻り値 - kernelCustomerId

## <a name="method-kernelrequestid"></a>メソッド kernelRequestId

```xpp
public static Guid kernelRequestId()
```

### <a name="return-value---kernelrequestid"></a>戻り値 - kernelRequestId

## <a name="method-kernelsessionid"></a>メソッド kernelSessionId

```xpp
public static str kernelSessionId()
```

### <a name="return-value---kernelsessionid"></a>戻り値 - kernelSessionId

## <a name="method-kerneluserid"></a>メソッド kernelUserId

```xpp
public static str kernelUserId()
```

### <a name="return-value---kerneluserid"></a>戻り値 - kernelUserId

## <a name="method-start"></a>メソッド start

```xpp
public static int start(str logFileName, [int logBufferSize], [int minBuffers], [int maxBuffers], [Int64 keywords], [int maxFileSize], [boolean useCircularLogging])
```

### <a name="parameters---start"></a>パラメーター - start

logFileName  

<!-- -->

logBufferSize  

<!-- -->

minBuffers  

<!-- -->

maxBuffers  

<!-- -->

キーワード  

<!-- -->

maxFileSize  

<!-- -->

useCircularLogging  

### <a name="return-value---start"></a>戻り値 - start

## <a name="method-stop"></a>メソッド stop

```xpp
public static int stop()
```

### <a name="return-value---stop"></a>戻り値 - stop

## <a name="method-logmessage"></a>メソッド logMessage

```xpp
public static void logMessage(str message)
```

### <a name="parameters---logmessage"></a>パラメーター - logMessage

メッセージ  

## <a name="method-endmarker"></a>メソッド endMarker

```xpp
public void endMarker(str transactionName)
```

### <a name="parameters---endmarker"></a>パラメーター - endMarker

transactionName  

## <a name="method-beginmarker"></a>メソッド beginMarker

```xpp
public void beginMarker(str transactionName)
```

### <a name="parameters---beginmarker"></a>パラメーター - beginMarker

transactionName  

## <a name="method-logcomponentmessage"></a>メソッド logComponentMessage

```xpp
public static void logComponentMessage(str component, str message)
```

### <a name="parameters---logcomponentmessage"></a>パラメーター - logComponentMessage

コンポーネント  

<!-- -->

メッセージ  

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-new"></a>メソッド new

xClassTrace クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

