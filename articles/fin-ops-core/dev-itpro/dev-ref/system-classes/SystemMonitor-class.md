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
# <a name="class-systemmonitor"></a><span data-ttu-id="8e613-103">クラス SystemMonitor</span><span class="sxs-lookup"><span data-stu-id="8e613-103">Class SystemMonitor</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class SystemMonitor extends Object
```

## <a name="remarks"></a><span data-ttu-id="8e613-104">備考</span><span class="sxs-lookup"><span data-stu-id="8e613-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="8e613-105">例</span><span class="sxs-lookup"><span data-stu-id="8e613-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="8e613-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="8e613-106">Methods</span></span>

| <span data-ttu-id="8e613-107">方法</span><span class="sxs-lookup"><span data-stu-id="8e613-107">Method</span></span>                                                                | <span data-ttu-id="8e613-108">説明</span><span class="sxs-lookup"><span data-stu-id="8e613-108">Description</span></span>                                            |
|-----------------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="8e613-109">::public static container allClientCounters()</span><span class="sxs-lookup"><span data-stu-id="8e613-109">::public static container allClientCounters()</span></span>                         |                                                        |
| <span data-ttu-id="8e613-110">::public static container allServerCounters()</span><span class="sxs-lookup"><span data-stu-id="8e613-110">::public static container allServerCounters()</span></span>                         |                                                        |
| <span data-ttu-id="8e613-111">::public static int getClientCounter(SystemMonitorCounter counter)</span><span class="sxs-lookup"><span data-stu-id="8e613-111">::public static int getClientCounter(SystemMonitorCounter counter)</span></span>    |                                                        |
| <span data-ttu-id="8e613-112">::public static container getClientInternals()</span><span class="sxs-lookup"><span data-stu-id="8e613-112">::public static container getClientInternals()</span></span>                        |                                                        |
| <span data-ttu-id="8e613-113">::public static int getCounter(SystemMonitorCounter counter)</span><span class="sxs-lookup"><span data-stu-id="8e613-113">::public static int getCounter(SystemMonitorCounter counter)</span></span>          |                                                        |
| <span data-ttu-id="8e613-114">::public static int getServerCounter(SystemMonitorCounter counter)</span><span class="sxs-lookup"><span data-stu-id="8e613-114">::public static int getServerCounter(SystemMonitorCounter counter)</span></span>    |                                                        |
| <span data-ttu-id="8e613-115">::public static container getServerInternals()</span><span class="sxs-lookup"><span data-stu-id="8e613-115">::public static container getServerInternals()</span></span>                        |                                                        |
| <span data-ttu-id="8e613-116">::public static boolean isRunning()</span><span class="sxs-lookup"><span data-stu-id="8e613-116">::public static boolean isRunning()</span></span>                                   |                                                        |
| <span data-ttu-id="8e613-117">::public static boolean isServerCounter(SystemMonitorCounter counter)</span><span class="sxs-lookup"><span data-stu-id="8e613-117">::public static boolean isServerCounter(SystemMonitorCounter counter)</span></span> |                                                        |
| <span data-ttu-id="8e613-118">::public static container sqlDump()</span><span class="sxs-lookup"><span data-stu-id="8e613-118">::public static container sqlDump()</span></span>                                   |                                                        |
| <span data-ttu-id="8e613-119">::public static void systemDump(boolean includeSQL)</span><span class="sxs-lookup"><span data-stu-id="8e613-119">::public static void systemDump(boolean includeSQL)</span></span>                   |                                                        |
| <span data-ttu-id="8e613-120">::public static void start()</span><span class="sxs-lookup"><span data-stu-id="8e613-120">::public static void start()</span></span>                                          |                                                        |
| <span data-ttu-id="8e613-121">::public static void resetServer()</span><span class="sxs-lookup"><span data-stu-id="8e613-121">::public static void resetServer()</span></span>                                    |                                                        |
| <span data-ttu-id="8e613-122">::public static void stop()</span><span class="sxs-lookup"><span data-stu-id="8e613-122">::public static void stop()</span></span>                                           |                                                        |
| <span data-ttu-id="8e613-123">public void new()</span><span class="sxs-lookup"><span data-stu-id="8e613-123">public void new()</span></span>                                                     | <span data-ttu-id="8e613-124">SystemMonitor クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="8e613-124">Initializes a new instance of the SystemMonitor class.</span></span> |
| <span data-ttu-id="8e613-125">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="8e613-125">public void finalize()</span></span>                                                |                                                        |
| <span data-ttu-id="8e613-126">::public static void reset()</span><span class="sxs-lookup"><span data-stu-id="8e613-126">::public static void reset()</span></span>                                          |                                                        |
| <span data-ttu-id="8e613-127">::public static void resetClient()</span><span class="sxs-lookup"><span data-stu-id="8e613-127">::public static void resetClient()</span></span>                                    |                                                        |

## <a name="method-allclientcounters"></a><span data-ttu-id="8e613-128">メソッド allClientCounters</span><span class="sxs-lookup"><span data-stu-id="8e613-128">Method allClientCounters</span></span>

```xpp
public static container allClientCounters()
```

### <a name="return-value---allclientcounters"></a><span data-ttu-id="8e613-129">戻り値 - allClientCounters</span><span class="sxs-lookup"><span data-stu-id="8e613-129">Return Value - allClientCounters</span></span>

## <a name="method-allservercounters"></a><span data-ttu-id="8e613-130">メソッド allServerCounters</span><span class="sxs-lookup"><span data-stu-id="8e613-130">Method allServerCounters</span></span>

```xpp
public static container allServerCounters()
```

### <a name="return-value---allservercounters"></a><span data-ttu-id="8e613-131">戻り値 - allServerCounters</span><span class="sxs-lookup"><span data-stu-id="8e613-131">Return Value - allServerCounters</span></span>

## <a name="method-getclientcounter"></a><span data-ttu-id="8e613-132">メソッド getClientCounter</span><span class="sxs-lookup"><span data-stu-id="8e613-132">Method getClientCounter</span></span>

```xpp
public static int getClientCounter(SystemMonitorCounter counter)
```

### <a name="parameters---getclientcounter"></a><span data-ttu-id="8e613-133">パラメーター - getClientCounter</span><span class="sxs-lookup"><span data-stu-id="8e613-133">Parameters - getClientCounter</span></span>

<span data-ttu-id="8e613-134">counter</span><span class="sxs-lookup"><span data-stu-id="8e613-134">counter</span></span>  

### <a name="return-value---getclientcounter"></a><span data-ttu-id="8e613-135">戻り値 - getClientCounter</span><span class="sxs-lookup"><span data-stu-id="8e613-135">Return Value - getClientCounter</span></span>

## <a name="method-getclientinternals"></a><span data-ttu-id="8e613-136">メソッド getClientInternals</span><span class="sxs-lookup"><span data-stu-id="8e613-136">Method getClientInternals</span></span>

```xpp
public static container getClientInternals()
```

### <a name="return-value---getclientinternals"></a><span data-ttu-id="8e613-137">戻り値 - getClientInternals</span><span class="sxs-lookup"><span data-stu-id="8e613-137">Return Value - getClientInternals</span></span>

## <a name="method-getcounter"></a><span data-ttu-id="8e613-138">メソッド getCounter</span><span class="sxs-lookup"><span data-stu-id="8e613-138">Method getCounter</span></span>

```xpp
public static int getCounter(SystemMonitorCounter counter)
```

### <a name="parameters---getcounter"></a><span data-ttu-id="8e613-139">パラメーター - getCounter</span><span class="sxs-lookup"><span data-stu-id="8e613-139">Parameters - getCounter</span></span>

<span data-ttu-id="8e613-140">counter</span><span class="sxs-lookup"><span data-stu-id="8e613-140">counter</span></span>  

### <a name="return-value---getcounter"></a><span data-ttu-id="8e613-141">戻り値 - getCounter</span><span class="sxs-lookup"><span data-stu-id="8e613-141">Return Value - getCounter</span></span>

## <a name="method-getservercounter"></a><span data-ttu-id="8e613-142">メソッド getServerCounter</span><span class="sxs-lookup"><span data-stu-id="8e613-142">Method getServerCounter</span></span>

```xpp
public static int getServerCounter(SystemMonitorCounter counter)
```

### <a name="parameters---getservercounter"></a><span data-ttu-id="8e613-143">パラメーター - getServerCounter</span><span class="sxs-lookup"><span data-stu-id="8e613-143">Parameters - getServerCounter</span></span>

<span data-ttu-id="8e613-144">counter</span><span class="sxs-lookup"><span data-stu-id="8e613-144">counter</span></span>  

### <a name="return-value---getservercounter"></a><span data-ttu-id="8e613-145">戻り値 - getServerCounter</span><span class="sxs-lookup"><span data-stu-id="8e613-145">Return Value - getServerCounter</span></span>

## <a name="method-getserverinternals"></a><span data-ttu-id="8e613-146">メソッド getServerInternals</span><span class="sxs-lookup"><span data-stu-id="8e613-146">Method getServerInternals</span></span>

```xpp
public static container getServerInternals()
```

### <a name="return-value---getserverinternals"></a><span data-ttu-id="8e613-147">戻り値 - getServerInternals</span><span class="sxs-lookup"><span data-stu-id="8e613-147">Return Value - getServerInternals</span></span>

## <a name="method-isrunning"></a><span data-ttu-id="8e613-148">メソッド isRunning</span><span class="sxs-lookup"><span data-stu-id="8e613-148">Method isRunning</span></span>

```xpp
public static boolean isRunning()
```

### <a name="return-value---isrunning"></a><span data-ttu-id="8e613-149">戻り値 - isRunning</span><span class="sxs-lookup"><span data-stu-id="8e613-149">Return Value - isRunning</span></span>

## <a name="method-isservercounter"></a><span data-ttu-id="8e613-150">メソッド isServerCounter</span><span class="sxs-lookup"><span data-stu-id="8e613-150">Method isServerCounter</span></span>

```xpp
public static boolean isServerCounter(SystemMonitorCounter counter)
```

### <a name="parameters---isservercounter"></a><span data-ttu-id="8e613-151">パラメーター - isServerCounter</span><span class="sxs-lookup"><span data-stu-id="8e613-151">Parameters - isServerCounter</span></span>

<span data-ttu-id="8e613-152">counter</span><span class="sxs-lookup"><span data-stu-id="8e613-152">counter</span></span>  

### <a name="return-value---isservercounter"></a><span data-ttu-id="8e613-153">戻り値 - isServerCounter</span><span class="sxs-lookup"><span data-stu-id="8e613-153">Return Value - isServerCounter</span></span>

## <a name="method-sqldump"></a><span data-ttu-id="8e613-154">メソッド sqlDump</span><span class="sxs-lookup"><span data-stu-id="8e613-154">Method sqlDump</span></span>

```xpp
public static container sqlDump()
```

### <a name="return-value---sqldump"></a><span data-ttu-id="8e613-155">戻り値 - sqlDump</span><span class="sxs-lookup"><span data-stu-id="8e613-155">Return Value - sqlDump</span></span>

## <a name="method-systemdump"></a><span data-ttu-id="8e613-156">メソッド systemDump</span><span class="sxs-lookup"><span data-stu-id="8e613-156">Method systemDump</span></span>

```xpp
public static void systemDump(boolean includeSQL)
```

### <a name="parameters---systemdump"></a><span data-ttu-id="8e613-157">パラメーター - systemDump</span><span class="sxs-lookup"><span data-stu-id="8e613-157">Parameters - systemDump</span></span>

<span data-ttu-id="8e613-158">includeSQL</span><span class="sxs-lookup"><span data-stu-id="8e613-158">includeSQL</span></span>  

## <a name="method-start"></a><span data-ttu-id="8e613-159">メソッド start</span><span class="sxs-lookup"><span data-stu-id="8e613-159">Method start</span></span>

```xpp
public static void start()
```

## <a name="method-resetserver"></a><span data-ttu-id="8e613-160">メソッド resetServer</span><span class="sxs-lookup"><span data-stu-id="8e613-160">Method resetServer</span></span>

```xpp
public static void resetServer()
```

## <a name="method-stop"></a><span data-ttu-id="8e613-161">メソッド stop</span><span class="sxs-lookup"><span data-stu-id="8e613-161">Method stop</span></span>

```xpp
public static void stop()
```

## <a name="method-new"></a><span data-ttu-id="8e613-162">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8e613-162">Method new</span></span>

<span data-ttu-id="8e613-163">SystemMonitor クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="8e613-163">Initializes a new instance of the SystemMonitor class.</span></span>

```xpp
public void new()
```

## <a name="method-finalize"></a><span data-ttu-id="8e613-164">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="8e613-164">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-reset"></a><span data-ttu-id="8e613-165">メソッド reset</span><span class="sxs-lookup"><span data-stu-id="8e613-165">Method reset</span></span>

```xpp
public static void reset()
```

## <a name="method-resetclient"></a><span data-ttu-id="8e613-166">メソッド resetClient</span><span class="sxs-lookup"><span data-stu-id="8e613-166">Method resetClient</span></span>

```xpp
public static void resetClient()
```

