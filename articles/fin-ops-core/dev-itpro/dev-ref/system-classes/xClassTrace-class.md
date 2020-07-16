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
# <a name="class-xclasstrace"></a><span data-ttu-id="56535-103">クラス xClassTrace</span><span class="sxs-lookup"><span data-stu-id="56535-103">Class xClassTrace</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class xClassTrace extends Object
```

## <a name="remarks"></a><span data-ttu-id="56535-104">備考</span><span class="sxs-lookup"><span data-stu-id="56535-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="56535-105">例</span><span class="sxs-lookup"><span data-stu-id="56535-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="56535-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="56535-106">Methods</span></span>

| <span data-ttu-id="56535-107">方法</span><span class="sxs-lookup"><span data-stu-id="56535-107">Method</span></span>                                                                                                                                                                             | <span data-ttu-id="56535-108">説明</span><span class="sxs-lookup"><span data-stu-id="56535-108">Description</span></span>                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="56535-109">::public static boolean isTracingEnabled(\[Int64 keyword\], \[int level\])</span><span class="sxs-lookup"><span data-stu-id="56535-109">::public static boolean isTracingEnabled(\[Int64 keyword\], \[int level\])</span></span>                                                                                                         |                                                      |
| <span data-ttu-id="56535-110">::public static boolean isTracingStarted()</span><span class="sxs-lookup"><span data-stu-id="56535-110">::public static boolean isTracingStarted()</span></span>                                                                                                                                         |                                                      |
| <span data-ttu-id="56535-111">::public static str kernelCustomerId()</span><span class="sxs-lookup"><span data-stu-id="56535-111">::public static str kernelCustomerId()</span></span>                                                                                                                                             |                                                      |
| <span data-ttu-id="56535-112">::public static Guid kernelRequestId()</span><span class="sxs-lookup"><span data-stu-id="56535-112">::public static Guid kernelRequestId()</span></span>                                                                                                                                             |                                                      |
| <span data-ttu-id="56535-113">::public static str kernelSessionId()</span><span class="sxs-lookup"><span data-stu-id="56535-113">::public static str kernelSessionId()</span></span>                                                                                                                                              |                                                      |
| <span data-ttu-id="56535-114">::public static str kernelUserId()</span><span class="sxs-lookup"><span data-stu-id="56535-114">::public static str kernelUserId()</span></span>                                                                                                                                                 |                                                      |
| <span data-ttu-id="56535-115">::public static int start(str logFileName, \[int logBufferSize\], \[int minBuffers\], \[int maxBuffers\], \[Int64 keywords\], \[int maxFileSize\], \[boolean useCircularLogging\])</span><span class="sxs-lookup"><span data-stu-id="56535-115">::public static int start(str logFileName, \[int logBufferSize\], \[int minBuffers\], \[int maxBuffers\], \[Int64 keywords\], \[int maxFileSize\], \[boolean useCircularLogging\])</span></span> |                                                      |
| <span data-ttu-id="56535-116">::public static int stop()</span><span class="sxs-lookup"><span data-stu-id="56535-116">::public static int stop()</span></span>                                                                                                                                                         |                                                      |
| <span data-ttu-id="56535-117">::public static void logMessage(str message)</span><span class="sxs-lookup"><span data-stu-id="56535-117">::public static void logMessage(str message)</span></span>                                                                                                                                       |                                                      |
| <span data-ttu-id="56535-118">public void endMarker(str transactionName)</span><span class="sxs-lookup"><span data-stu-id="56535-118">public void endMarker(str transactionName)</span></span>                                                                                                                                         |                                                      |
| <span data-ttu-id="56535-119">public void beginMarker(str transactionName)</span><span class="sxs-lookup"><span data-stu-id="56535-119">public void beginMarker(str transactionName)</span></span>                                                                                                                                       |                                                      |
| <span data-ttu-id="56535-120">::public static void logComponentMessage(str component, str message)</span><span class="sxs-lookup"><span data-stu-id="56535-120">::public static void logComponentMessage(str component, str message)</span></span>                                                                                                               |                                                      |
| <span data-ttu-id="56535-121">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="56535-121">public void finalize()</span></span>                                                                                                                                                             |                                                      |
| <span data-ttu-id="56535-122">public void new()</span><span class="sxs-lookup"><span data-stu-id="56535-122">public void new()</span></span>                                                                                                                                                                  | <span data-ttu-id="56535-123">xClassTrace クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="56535-123">Initializes a new instance of the xClassTrace class.</span></span> |

## <a name="method-istracingenabled"></a><span data-ttu-id="56535-124">メソッド isTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="56535-124">Method isTracingEnabled</span></span>

```xpp
public static boolean isTracingEnabled([Int64 keyword], [int level])
```

### <a name="parameters---istracingenabled"></a><span data-ttu-id="56535-125">パラメーター - isTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="56535-125">Parameters - isTracingEnabled</span></span>

<span data-ttu-id="56535-126">キーワード</span><span class="sxs-lookup"><span data-stu-id="56535-126">keyword</span></span>  

<!-- -->

<span data-ttu-id="56535-127">level</span><span class="sxs-lookup"><span data-stu-id="56535-127">level</span></span>  

### <a name="return-value---istracingenabled"></a><span data-ttu-id="56535-128">戻り値 - isTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="56535-128">Return Value - isTracingEnabled</span></span>

## <a name="method-istracingstarted"></a><span data-ttu-id="56535-129">メソッド isTracingStarted</span><span class="sxs-lookup"><span data-stu-id="56535-129">Method isTracingStarted</span></span>

```xpp
public static boolean isTracingStarted()
```

### <a name="return-value---istracingstarted"></a><span data-ttu-id="56535-130">戻り値 - isTracingStarted</span><span class="sxs-lookup"><span data-stu-id="56535-130">Return Value - isTracingStarted</span></span>

## <a name="method-kernelcustomerid"></a><span data-ttu-id="56535-131">メソッド kernelCustomerId</span><span class="sxs-lookup"><span data-stu-id="56535-131">Method kernelCustomerId</span></span>

```xpp
public static str kernelCustomerId()
```

### <a name="return-value---kernelcustomerid"></a><span data-ttu-id="56535-132">戻り値 - kernelCustomerId</span><span class="sxs-lookup"><span data-stu-id="56535-132">Return Value - kernelCustomerId</span></span>

## <a name="method-kernelrequestid"></a><span data-ttu-id="56535-133">メソッド kernelRequestId</span><span class="sxs-lookup"><span data-stu-id="56535-133">Method kernelRequestId</span></span>

```xpp
public static Guid kernelRequestId()
```

### <a name="return-value---kernelrequestid"></a><span data-ttu-id="56535-134">戻り値 - kernelRequestId</span><span class="sxs-lookup"><span data-stu-id="56535-134">Return Value - kernelRequestId</span></span>

## <a name="method-kernelsessionid"></a><span data-ttu-id="56535-135">メソッド kernelSessionId</span><span class="sxs-lookup"><span data-stu-id="56535-135">Method kernelSessionId</span></span>

```xpp
public static str kernelSessionId()
```

### <a name="return-value---kernelsessionid"></a><span data-ttu-id="56535-136">戻り値 - kernelSessionId</span><span class="sxs-lookup"><span data-stu-id="56535-136">Return Value - kernelSessionId</span></span>

## <a name="method-kerneluserid"></a><span data-ttu-id="56535-137">メソッド kernelUserId</span><span class="sxs-lookup"><span data-stu-id="56535-137">Method kernelUserId</span></span>

```xpp
public static str kernelUserId()
```

### <a name="return-value---kerneluserid"></a><span data-ttu-id="56535-138">戻り値 - kernelUserId</span><span class="sxs-lookup"><span data-stu-id="56535-138">Return Value - kernelUserId</span></span>

## <a name="method-start"></a><span data-ttu-id="56535-139">メソッド start</span><span class="sxs-lookup"><span data-stu-id="56535-139">Method start</span></span>

```xpp
public static int start(str logFileName, [int logBufferSize], [int minBuffers], [int maxBuffers], [Int64 keywords], [int maxFileSize], [boolean useCircularLogging])
```

### <a name="parameters---start"></a><span data-ttu-id="56535-140">パラメーター - start</span><span class="sxs-lookup"><span data-stu-id="56535-140">Parameters - start</span></span>

<span data-ttu-id="56535-141">logFileName</span><span class="sxs-lookup"><span data-stu-id="56535-141">logFileName</span></span>  

<!-- -->

<span data-ttu-id="56535-142">logBufferSize</span><span class="sxs-lookup"><span data-stu-id="56535-142">logBufferSize</span></span>  

<!-- -->

<span data-ttu-id="56535-143">minBuffers</span><span class="sxs-lookup"><span data-stu-id="56535-143">minBuffers</span></span>  

<!-- -->

<span data-ttu-id="56535-144">maxBuffers</span><span class="sxs-lookup"><span data-stu-id="56535-144">maxBuffers</span></span>  

<!-- -->

<span data-ttu-id="56535-145">キーワード</span><span class="sxs-lookup"><span data-stu-id="56535-145">keywords</span></span>  

<!-- -->

<span data-ttu-id="56535-146">maxFileSize</span><span class="sxs-lookup"><span data-stu-id="56535-146">maxFileSize</span></span>  

<!-- -->

<span data-ttu-id="56535-147">useCircularLogging</span><span class="sxs-lookup"><span data-stu-id="56535-147">useCircularLogging</span></span>  

### <a name="return-value---start"></a><span data-ttu-id="56535-148">戻り値 - start</span><span class="sxs-lookup"><span data-stu-id="56535-148">Return Value - start</span></span>

## <a name="method-stop"></a><span data-ttu-id="56535-149">メソッド stop</span><span class="sxs-lookup"><span data-stu-id="56535-149">Method stop</span></span>

```xpp
public static int stop()
```

### <a name="return-value---stop"></a><span data-ttu-id="56535-150">戻り値 - stop</span><span class="sxs-lookup"><span data-stu-id="56535-150">Return Value - stop</span></span>

## <a name="method-logmessage"></a><span data-ttu-id="56535-151">メソッド logMessage</span><span class="sxs-lookup"><span data-stu-id="56535-151">Method logMessage</span></span>

```xpp
public static void logMessage(str message)
```

### <a name="parameters---logmessage"></a><span data-ttu-id="56535-152">パラメーター - logMessage</span><span class="sxs-lookup"><span data-stu-id="56535-152">Parameters - logMessage</span></span>

<span data-ttu-id="56535-153">メッセージ</span><span class="sxs-lookup"><span data-stu-id="56535-153">message</span></span>  

## <a name="method-endmarker"></a><span data-ttu-id="56535-154">メソッド endMarker</span><span class="sxs-lookup"><span data-stu-id="56535-154">Method endMarker</span></span>

```xpp
public void endMarker(str transactionName)
```

### <a name="parameters---endmarker"></a><span data-ttu-id="56535-155">パラメーター - endMarker</span><span class="sxs-lookup"><span data-stu-id="56535-155">Parameters - endMarker</span></span>

<span data-ttu-id="56535-156">transactionName</span><span class="sxs-lookup"><span data-stu-id="56535-156">transactionName</span></span>  

## <a name="method-beginmarker"></a><span data-ttu-id="56535-157">メソッド beginMarker</span><span class="sxs-lookup"><span data-stu-id="56535-157">Method beginMarker</span></span>

```xpp
public void beginMarker(str transactionName)
```

### <a name="parameters---beginmarker"></a><span data-ttu-id="56535-158">パラメーター - beginMarker</span><span class="sxs-lookup"><span data-stu-id="56535-158">Parameters - beginMarker</span></span>

<span data-ttu-id="56535-159">transactionName</span><span class="sxs-lookup"><span data-stu-id="56535-159">transactionName</span></span>  

## <a name="method-logcomponentmessage"></a><span data-ttu-id="56535-160">メソッド logComponentMessage</span><span class="sxs-lookup"><span data-stu-id="56535-160">Method logComponentMessage</span></span>

```xpp
public static void logComponentMessage(str component, str message)
```

### <a name="parameters---logcomponentmessage"></a><span data-ttu-id="56535-161">パラメーター - logComponentMessage</span><span class="sxs-lookup"><span data-stu-id="56535-161">Parameters - logComponentMessage</span></span>

<span data-ttu-id="56535-162">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="56535-162">component</span></span>  

<!-- -->

<span data-ttu-id="56535-163">メッセージ</span><span class="sxs-lookup"><span data-stu-id="56535-163">message</span></span>  

## <a name="method-finalize"></a><span data-ttu-id="56535-164">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="56535-164">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-new"></a><span data-ttu-id="56535-165">メソッド new</span><span class="sxs-lookup"><span data-stu-id="56535-165">Method new</span></span>

<span data-ttu-id="56535-166">xClassTrace クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="56535-166">Initializes a new instance of the xClassTrace class.</span></span>

```xpp
public void new()
```

