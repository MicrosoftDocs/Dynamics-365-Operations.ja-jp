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
# <a name="class-profiler"></a><span data-ttu-id="79943-103">クラス プロファイラー</span><span class="sxs-lookup"><span data-stu-id="79943-103">Class profiler</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class profiler extends Object
```

## <a name="remarks"></a><span data-ttu-id="79943-104">備考</span><span class="sxs-lookup"><span data-stu-id="79943-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="79943-105">例</span><span class="sxs-lookup"><span data-stu-id="79943-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="79943-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="79943-106">Methods</span></span>

| <span data-ttu-id="79943-107">方法</span><span class="sxs-lookup"><span data-stu-id="79943-107">Method</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="79943-108">説明</span><span class="sxs-lookup"><span data-stu-id="79943-108">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="79943-109">public int collected()</span><span class="sxs-lookup"><span data-stu-id="79943-109">public int collected()</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |                                                      |
| <span data-ttu-id="79943-110">public int flushInterval(\[int interval\])</span><span class="sxs-lookup"><span data-stu-id="79943-110">public int flushInterval(\[int interval\])</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                      |                                                      |
| <span data-ttu-id="79943-111">public AnyType profileOff()</span><span class="sxs-lookup"><span data-stu-id="79943-111">public AnyType profileOff()</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |                                                      |
| <span data-ttu-id="79943-112">public AnyType profileOn(str runId, \[int traceDepth\])</span><span class="sxs-lookup"><span data-stu-id="79943-112">public AnyType profileOn(str runId, \[int traceDepth\])</span></span>                                                                                                                                                                                                                                                                                                                                                                                                         |                                                      |
| <span data-ttu-id="79943-113">public str tempPath()</span><span class="sxs-lookup"><span data-stu-id="79943-113">public str tempPath()</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |                                                      |
| <span data-ttu-id="79943-114">public str toString()</span><span class="sxs-lookup"><span data-stu-id="79943-114">public str toString()</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="79943-115">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="79943-115">Returns a string that represents the current object.</span></span> |
| <span data-ttu-id="79943-116">::public static AnyType profilerAlreadyOn()</span><span class="sxs-lookup"><span data-stu-id="79943-116">::public static AnyType profilerAlreadyOn()</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                     |                                                      |
| <span data-ttu-id="79943-117">public void flush()</span><span class="sxs-lookup"><span data-stu-id="79943-117">public void flush()</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |                                                      |
| <span data-ttu-id="79943-118">public void new()</span><span class="sxs-lookup"><span data-stu-id="79943-118">public void new()</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="79943-119">profiler クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="79943-119">Initializes a new instance of the profiler class.</span></span>    |
| <span data-ttu-id="79943-120">public void flushData(int lineNumber, str path, int microSecs, int sequenceNumber, int parentSequenceNumber, int selectCalls, int selectBytes, int selectRows, int sqlWaitTime, int aosWaitTime, int sqlInserts, int sqlUpdates, int sqlDeletes, int aosInCalls, int aosOutCalls, int aosInBytes, int aosOutBytes, \[int sqlInsertBytes\], \[int sqlInsertRows\], \[int sqlUpdateBytes\], \[int sqlUpdateRows\], \[int sqlDeleteBytes\], \[int sqlDeleteRows\])</span><span class="sxs-lookup"><span data-stu-id="79943-120">public void flushData(int lineNumber, str path, int microSecs, int sequenceNumber, int parentSequenceNumber, int selectCalls, int selectBytes, int selectRows, int sqlWaitTime, int aosWaitTime, int sqlInserts, int sqlUpdates, int sqlDeletes, int aosInCalls, int aosOutCalls, int aosInBytes, int aosOutBytes, \[int sqlInsertBytes\], \[int sqlInsertRows\], \[int sqlUpdateBytes\], \[int sqlUpdateRows\], \[int sqlDeleteBytes\], \[int sqlDeleteRows\])</span></span> |                                                      |

## <a name="method-collected"></a><span data-ttu-id="79943-121">メソッド collected</span><span class="sxs-lookup"><span data-stu-id="79943-121">Method collected</span></span>

```xpp
public int collected()
```

### <a name="return-value---collected"></a><span data-ttu-id="79943-122">戻り値 - collected</span><span class="sxs-lookup"><span data-stu-id="79943-122">Return Value - collected</span></span>

## <a name="method-flushinterval"></a><span data-ttu-id="79943-123">メソッド flushInterval</span><span class="sxs-lookup"><span data-stu-id="79943-123">Method flushInterval</span></span>

```xpp
public int flushInterval([int interval])
```

### <a name="parameters---flushinterval"></a><span data-ttu-id="79943-124">パラメーター - flushInterval</span><span class="sxs-lookup"><span data-stu-id="79943-124">Parameters - flushInterval</span></span>

<span data-ttu-id="79943-125">interval</span><span class="sxs-lookup"><span data-stu-id="79943-125">interval</span></span>  

### <a name="return-value---flushinterval"></a><span data-ttu-id="79943-126">戻り値 - flushInterval</span><span class="sxs-lookup"><span data-stu-id="79943-126">Return Value - flushInterval</span></span>

## <a name="method-profileoff"></a><span data-ttu-id="79943-127">メソッド profileOff</span><span class="sxs-lookup"><span data-stu-id="79943-127">Method profileOff</span></span>

```xpp
public AnyType profileOff()
```

### <a name="return-value---profileoff"></a><span data-ttu-id="79943-128">戻り値 - profileOff</span><span class="sxs-lookup"><span data-stu-id="79943-128">Return Value - profileOff</span></span>

## <a name="method-profileon"></a><span data-ttu-id="79943-129">メソッド profileOn</span><span class="sxs-lookup"><span data-stu-id="79943-129">Method profileOn</span></span>

```xpp
public AnyType profileOn(str runId, [int traceDepth])
```

### <a name="parameters---profileon"></a><span data-ttu-id="79943-130">パラメーター - profileOn</span><span class="sxs-lookup"><span data-stu-id="79943-130">Parameters - profileOn</span></span>

<span data-ttu-id="79943-131">runId</span><span class="sxs-lookup"><span data-stu-id="79943-131">runId</span></span>  

<!-- -->

<span data-ttu-id="79943-132">traceDepth</span><span class="sxs-lookup"><span data-stu-id="79943-132">traceDepth</span></span>  

### <a name="return-value---profileon"></a><span data-ttu-id="79943-133">戻り値 - profileOn</span><span class="sxs-lookup"><span data-stu-id="79943-133">Return Value - profileOn</span></span>

## <a name="method-temppath"></a><span data-ttu-id="79943-134">メソッド tempPath</span><span class="sxs-lookup"><span data-stu-id="79943-134">Method tempPath</span></span>

```xpp
public str tempPath()
```

### <a name="return-value---temppath"></a><span data-ttu-id="79943-135">戻り値 - tempPath</span><span class="sxs-lookup"><span data-stu-id="79943-135">Return Value - tempPath</span></span>

## <a name="method-tostring"></a><span data-ttu-id="79943-136">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="79943-136">Method toString</span></span>

<span data-ttu-id="79943-137">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="79943-137">Returns a string that represents the current object.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="79943-138">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="79943-138">Return Value - toString</span></span>

<span data-ttu-id="79943-139">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="79943-139">A string that represents the current object.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="79943-140">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="79943-140">Remarks - toString</span></span>

<span data-ttu-id="79943-141">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="79943-141">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="79943-142">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="79943-142">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="79943-143">たとえば、クラスのインスタンスは、インスタンスまたは静的などの、メソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="79943-143">For example, an instance of the class returns the method name and type of the method, such as instance or static.</span></span>

## <a name="method-profileralreadyon"></a><span data-ttu-id="79943-144">メソッド profilerAlreadyOn</span><span class="sxs-lookup"><span data-stu-id="79943-144">Method profilerAlreadyOn</span></span>

```xpp
public static AnyType profilerAlreadyOn()
```

### <a name="return-value---profileralreadyon"></a><span data-ttu-id="79943-145">戻り値 - profilerAlreadyOn</span><span class="sxs-lookup"><span data-stu-id="79943-145">Return Value - profilerAlreadyOn</span></span>

## <a name="method-flush"></a><span data-ttu-id="79943-146">メソッド flush</span><span class="sxs-lookup"><span data-stu-id="79943-146">Method flush</span></span>

```xpp
public void flush()
```

## <a name="method-new"></a><span data-ttu-id="79943-147">メソッド new</span><span class="sxs-lookup"><span data-stu-id="79943-147">Method new</span></span>

<span data-ttu-id="79943-148">profiler クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="79943-148">Initializes a new instance of the profiler class.</span></span>

```xpp
public void new()
```

## <a name="method-flushdata"></a><span data-ttu-id="79943-149">メソッド flushData</span><span class="sxs-lookup"><span data-stu-id="79943-149">Method flushData</span></span>

```xpp
public void flushData(int lineNumber, str path, int microSecs, int sequenceNumber, int parentSequenceNumber, int selectCalls, int selectBytes, int selectRows, int sqlWaitTime, int aosWaitTime, int sqlInserts, int sqlUpdates, int sqlDeletes, int aosInCalls, int aosOutCalls, int aosInBytes, int aosOutBytes, [int sqlInsertBytes], [int sqlInsertRows], [int sqlUpdateBytes], [int sqlUpdateRows], [int sqlDeleteBytes], [int sqlDeleteRows])
```

### <a name="parameters---flushdata"></a><span data-ttu-id="79943-150">パラメーター - flushData</span><span class="sxs-lookup"><span data-stu-id="79943-150">Parameters - flushData</span></span>

<span data-ttu-id="79943-151">lineNumber</span><span class="sxs-lookup"><span data-stu-id="79943-151">lineNumber</span></span>  

<!-- -->

<span data-ttu-id="79943-152">path</span><span class="sxs-lookup"><span data-stu-id="79943-152">path</span></span>  

<!-- -->

<span data-ttu-id="79943-153">microSecs</span><span class="sxs-lookup"><span data-stu-id="79943-153">microSecs</span></span>  

<!-- -->

<span data-ttu-id="79943-154">sequenceNumber</span><span class="sxs-lookup"><span data-stu-id="79943-154">sequenceNumber</span></span>  

<!-- -->

<span data-ttu-id="79943-155">parentSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="79943-155">parentSequenceNumber</span></span>  

<!-- -->

<span data-ttu-id="79943-156">selectCalls</span><span class="sxs-lookup"><span data-stu-id="79943-156">selectCalls</span></span>  

<!-- -->

<span data-ttu-id="79943-157">selectBytes</span><span class="sxs-lookup"><span data-stu-id="79943-157">selectBytes</span></span>  

<!-- -->

<span data-ttu-id="79943-158">selectRows</span><span class="sxs-lookup"><span data-stu-id="79943-158">selectRows</span></span>  

<!-- -->

<span data-ttu-id="79943-159">sqlWaitTime</span><span class="sxs-lookup"><span data-stu-id="79943-159">sqlWaitTime</span></span>  

<!-- -->

<span data-ttu-id="79943-160">aosWaitTime</span><span class="sxs-lookup"><span data-stu-id="79943-160">aosWaitTime</span></span>  

<!-- -->

<span data-ttu-id="79943-161">sqlInserts</span><span class="sxs-lookup"><span data-stu-id="79943-161">sqlInserts</span></span>  

<!-- -->

<span data-ttu-id="79943-162">sqlUpdates</span><span class="sxs-lookup"><span data-stu-id="79943-162">sqlUpdates</span></span>  

<!-- -->

<span data-ttu-id="79943-163">sqlDeletes</span><span class="sxs-lookup"><span data-stu-id="79943-163">sqlDeletes</span></span>  

<!-- -->

<span data-ttu-id="79943-164">aosInCalls</span><span class="sxs-lookup"><span data-stu-id="79943-164">aosInCalls</span></span>  

<!-- -->

<span data-ttu-id="79943-165">aosOutCalls</span><span class="sxs-lookup"><span data-stu-id="79943-165">aosOutCalls</span></span>  

<!-- -->

<span data-ttu-id="79943-166">aosInBytes</span><span class="sxs-lookup"><span data-stu-id="79943-166">aosInBytes</span></span>  

<!-- -->

<span data-ttu-id="79943-167">aosOutBytes</span><span class="sxs-lookup"><span data-stu-id="79943-167">aosOutBytes</span></span>  

<!-- -->

<span data-ttu-id="79943-168">sqlInsertBytes</span><span class="sxs-lookup"><span data-stu-id="79943-168">sqlInsertBytes</span></span>  

<!-- -->

<span data-ttu-id="79943-169">sqlInsertRows</span><span class="sxs-lookup"><span data-stu-id="79943-169">sqlInsertRows</span></span>  

<!-- -->

<span data-ttu-id="79943-170">sqlUpdateBytes</span><span class="sxs-lookup"><span data-stu-id="79943-170">sqlUpdateBytes</span></span>  

<!-- -->

<span data-ttu-id="79943-171">sqlUpdateRows</span><span class="sxs-lookup"><span data-stu-id="79943-171">sqlUpdateRows</span></span>  

<!-- -->

<span data-ttu-id="79943-172">sqlDeleteBytes</span><span class="sxs-lookup"><span data-stu-id="79943-172">sqlDeleteBytes</span></span>  

<!-- -->

<span data-ttu-id="79943-173">sqlDeleteRows</span><span class="sxs-lookup"><span data-stu-id="79943-173">sqlDeleteRows</span></span>  

