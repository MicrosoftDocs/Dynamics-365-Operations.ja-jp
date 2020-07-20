---
title: SystemMonitor クラス
description: このトピックでは、SystemMonitor クラスについて説明します。
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
ms.openlocfilehash: 8bc5e99693640e9f9f3e4a263e096baa2618abfd
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502792"
---
# <a name="class-systemmonitor"></a>クラス SystemMonitor

[!include [banner](../../includes/banner.md)]

```xpp
class SystemMonitor extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                | 説明                                            |
|-----------------------------------------------------------------------|--------------------------------------------------------|
| ::public static container allClientCounters()                         |                                                        |
| ::public static container allServerCounters()                         |                                                        |
| ::public static int getClientCounter(SystemMonitorCounter counter)    |                                                        |
| ::public static container getClientInternals()                        |                                                        |
| ::public static int getCounter(SystemMonitorCounter counter)          |                                                        |
| ::public static int getServerCounter(SystemMonitorCounter counter)    |                                                        |
| ::public static container getServerInternals()                        |                                                        |
| ::public static boolean isRunning()                                   |                                                        |
| ::public static boolean isServerCounter(SystemMonitorCounter counter) |                                                        |
| ::public static container sqlDump()                                   |                                                        |
| ::public static void systemDump(boolean includeSQL)                   |                                                        |
| ::public static void start()                                          |                                                        |
| ::public static void resetServer()                                    |                                                        |
| ::public static void stop()                                           |                                                        |
| public void new()                                                     | SystemMonitor クラスの新しいインスタンスを初期化します。 |
| public void finalize()                                                |                                                        |
| ::public static void reset()                                          |                                                        |
| ::public static void resetClient()                                    |                                                        |

## <a name="method-allclientcounters"></a>メソッド allClientCounters

```xpp
public static container allClientCounters()
```

### <a name="return-value---allclientcounters"></a>戻り値 - allClientCounters

## <a name="method-allservercounters"></a>メソッド allServerCounters

```xpp
public static container allServerCounters()
```

### <a name="return-value---allservercounters"></a>戻り値 - allServerCounters

## <a name="method-getclientcounter"></a>メソッド getClientCounter

```xpp
public static int getClientCounter(SystemMonitorCounter counter)
```

### <a name="parameters---getclientcounter"></a>パラメーター - getClientCounter

counter  

### <a name="return-value---getclientcounter"></a>戻り値 - getClientCounter

## <a name="method-getclientinternals"></a>メソッド getClientInternals

```xpp
public static container getClientInternals()
```

### <a name="return-value---getclientinternals"></a>戻り値 - getClientInternals

## <a name="method-getcounter"></a>メソッド getCounter

```xpp
public static int getCounter(SystemMonitorCounter counter)
```

### <a name="parameters---getcounter"></a>パラメーター - getCounter

counter  

### <a name="return-value---getcounter"></a>戻り値 - getCounter

## <a name="method-getservercounter"></a>メソッド getServerCounter

```xpp
public static int getServerCounter(SystemMonitorCounter counter)
```

### <a name="parameters---getservercounter"></a>パラメーター - getServerCounter

counter  

### <a name="return-value---getservercounter"></a>戻り値 - getServerCounter

## <a name="method-getserverinternals"></a>メソッド getServerInternals

```xpp
public static container getServerInternals()
```

### <a name="return-value---getserverinternals"></a>戻り値 - getServerInternals

## <a name="method-isrunning"></a>メソッド isRunning

```xpp
public static boolean isRunning()
```

### <a name="return-value---isrunning"></a>戻り値 - isRunning

## <a name="method-isservercounter"></a>メソッド isServerCounter

```xpp
public static boolean isServerCounter(SystemMonitorCounter counter)
```

### <a name="parameters---isservercounter"></a>パラメーター - isServerCounter

counter  

### <a name="return-value---isservercounter"></a>戻り値 - isServerCounter

## <a name="method-sqldump"></a>メソッド sqlDump

```xpp
public static container sqlDump()
```

### <a name="return-value---sqldump"></a>戻り値 - sqlDump

## <a name="method-systemdump"></a>メソッド systemDump

```xpp
public static void systemDump(boolean includeSQL)
```

### <a name="parameters---systemdump"></a>パラメーター - systemDump

includeSQL  

## <a name="method-start"></a>メソッド start

```xpp
public static void start()
```

## <a name="method-resetserver"></a>メソッド resetServer

```xpp
public static void resetServer()
```

## <a name="method-stop"></a>メソッド stop

```xpp
public static void stop()
```

## <a name="method-new"></a>メソッド new

SystemMonitor クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-reset"></a>メソッド reset

```xpp
public static void reset()
```

## <a name="method-resetclient"></a>メソッド resetClient

```xpp
public static void resetClient()
```

