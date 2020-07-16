---
title: バイナリ クラス
description: このトピックでは、バイナリ クラスについて説明します。
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
ms.openlocfilehash: 90669ef6c0d171ca8ea8a28c88f5137f11698e4b
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502720"
---
# <a name="class-binary"></a><span data-ttu-id="e5335-103">クラス バイナリ</span><span class="sxs-lookup"><span data-stu-id="e5335-103">Class Binary</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class Binary extends Object
```

## <a name="remarks"></a><span data-ttu-id="e5335-104">備考</span><span class="sxs-lookup"><span data-stu-id="e5335-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="e5335-105">例</span><span class="sxs-lookup"><span data-stu-id="e5335-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="e5335-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="e5335-106">Methods</span></span>

| <span data-ttu-id="e5335-107">方法</span><span class="sxs-lookup"><span data-stu-id="e5335-107">Method</span></span>                                                                   | <span data-ttu-id="e5335-108">説明</span><span class="sxs-lookup"><span data-stu-id="e5335-108">Description</span></span>                                     |
|--------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="e5335-109">public int byte(int offset, \[int value\])</span><span class="sxs-lookup"><span data-stu-id="e5335-109">public int byte(int offset, \[int value\])</span></span>                               |                                                 |
| <span data-ttu-id="e5335-110">public Real double(int offset, \[Real value\])</span><span class="sxs-lookup"><span data-stu-id="e5335-110">public Real double(int offset, \[Real value\])</span></span>                           |                                                 |
| <span data-ttu-id="e5335-111">public int dWord(int offset, \[int value\])</span><span class="sxs-lookup"><span data-stu-id="e5335-111">public int dWord(int offset, \[int value\])</span></span>                              |                                                 |
| <span data-ttu-id="e5335-112">public container getContainer()</span><span class="sxs-lookup"><span data-stu-id="e5335-112">public container getContainer()</span></span>                                          |                                                 |
| <span data-ttu-id="e5335-113">public CLRObject getMemoryStream()</span><span class="sxs-lookup"><span data-stu-id="e5335-113">public CLRObject getMemoryStream()</span></span>                                       |                                                 |
| <span data-ttu-id="e5335-114">public Int64 qWord(int offset, \[Int64 value\])</span><span class="sxs-lookup"><span data-stu-id="e5335-114">public Int64 qWord(int offset, \[Int64 value\])</span></span>                          |                                                 |
| <span data-ttu-id="e5335-115">public str string(int offset, \[str value\])</span><span class="sxs-lookup"><span data-stu-id="e5335-115">public str string(int offset, \[str value\])</span></span>                             |                                                 |
| <span data-ttu-id="e5335-116">public int strLenBytes(int offset)</span><span class="sxs-lookup"><span data-stu-id="e5335-116">public int strLenBytes(int offset)</span></span>                                       |                                                 |
| <span data-ttu-id="e5335-117">public int word(int offset, \[int value\])</span><span class="sxs-lookup"><span data-stu-id="e5335-117">public int word(int offset, \[int value\])</span></span>                               |                                                 |
| <span data-ttu-id="e5335-118">public str wString(int offset, \[str value\])</span><span class="sxs-lookup"><span data-stu-id="e5335-118">public str wString(int offset, \[str value\])</span></span>                            |                                                 |
| <span data-ttu-id="e5335-119">::public static Binary constructFromContainer(container data)</span><span class="sxs-lookup"><span data-stu-id="e5335-119">::public static Binary constructFromContainer(container data)</span></span>            |                                                 |
| <span data-ttu-id="e5335-120">::public static Binary constructFromMemoryStream(CLRObject memoryStream)</span><span class="sxs-lookup"><span data-stu-id="e5335-120">::public static Binary constructFromMemoryStream(CLRObject memoryStream)</span></span> |                                                 |
| <span data-ttu-id="e5335-121">public void attach(Int64 bufPtr, int bufSize)</span><span class="sxs-lookup"><span data-stu-id="e5335-121">public void attach(Int64 bufPtr, int bufSize)</span></span>                            |                                                 |
| <span data-ttu-id="e5335-122">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="e5335-122">public void finalize()</span></span>                                                   |                                                 |
| <span data-ttu-id="e5335-123">public void appendSubString(\[str string\])</span><span class="sxs-lookup"><span data-stu-id="e5335-123">public void appendSubString(\[str string\])</span></span>                              |                                                 |
| <span data-ttu-id="e5335-124">public void setBinaryValue(int offset, Binary value)</span><span class="sxs-lookup"><span data-stu-id="e5335-124">public void setBinaryValue(int offset, Binary value)</span></span>                     |                                                 |
| <span data-ttu-id="e5335-125">public void new(AnyType buffersizeOrString, \[boolean wideString\])</span><span class="sxs-lookup"><span data-stu-id="e5335-125">public void new(AnyType buffersizeOrString, \[boolean wideString\])</span></span>      | <span data-ttu-id="e5335-126">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e5335-126">Initializes a new instance of the Object class.</span></span> |

## <a name="method-byte"></a><span data-ttu-id="e5335-127">メソッド byte</span><span class="sxs-lookup"><span data-stu-id="e5335-127">Method byte</span></span>

```xpp
public int byte(int offset, [int value])
```

### <a name="parameters---byte"></a><span data-ttu-id="e5335-128">パラメーター - byte</span><span class="sxs-lookup"><span data-stu-id="e5335-128">Parameters - byte</span></span>

<span data-ttu-id="e5335-129">相殺</span><span class="sxs-lookup"><span data-stu-id="e5335-129">offset</span></span>  

<!-- -->

<span data-ttu-id="e5335-130">値</span><span class="sxs-lookup"><span data-stu-id="e5335-130">value</span></span>  

### <a name="return-value---byte"></a><span data-ttu-id="e5335-131">戻り値 - byte</span><span class="sxs-lookup"><span data-stu-id="e5335-131">Return Value - byte</span></span>

## <a name="method-double"></a><span data-ttu-id="e5335-132">メソッド double</span><span class="sxs-lookup"><span data-stu-id="e5335-132">Method double</span></span>

```xpp
public Real double(int offset, [Real value])
```

### <a name="parameters---double"></a><span data-ttu-id="e5335-133">パラメーター - double</span><span class="sxs-lookup"><span data-stu-id="e5335-133">Parameters - double</span></span>

<span data-ttu-id="e5335-134">相殺</span><span class="sxs-lookup"><span data-stu-id="e5335-134">offset</span></span>  

<!-- -->

<span data-ttu-id="e5335-135">値</span><span class="sxs-lookup"><span data-stu-id="e5335-135">value</span></span>  

### <a name="return-value---double"></a><span data-ttu-id="e5335-136">戻り値 - double</span><span class="sxs-lookup"><span data-stu-id="e5335-136">Return Value - double</span></span>

## <a name="method-dword"></a><span data-ttu-id="e5335-137">メソッド dWord</span><span class="sxs-lookup"><span data-stu-id="e5335-137">Method dWord</span></span>

```xpp
public int dWord(int offset, [int value])
```

### <a name="parameters---dword"></a><span data-ttu-id="e5335-138">パラメーター - dWord</span><span class="sxs-lookup"><span data-stu-id="e5335-138">Parameters - dWord</span></span>

<span data-ttu-id="e5335-139">相殺</span><span class="sxs-lookup"><span data-stu-id="e5335-139">offset</span></span>  

<!-- -->

<span data-ttu-id="e5335-140">値</span><span class="sxs-lookup"><span data-stu-id="e5335-140">value</span></span>  

### <a name="return-value---dword"></a><span data-ttu-id="e5335-141">戻り値 - dWord</span><span class="sxs-lookup"><span data-stu-id="e5335-141">Return Value - dWord</span></span>

## <a name="method-getcontainer"></a><span data-ttu-id="e5335-142">メソッド getContainer</span><span class="sxs-lookup"><span data-stu-id="e5335-142">Method getContainer</span></span>

```xpp
public container getContainer()
```

### <a name="return-value---getcontainer"></a><span data-ttu-id="e5335-143">戻り値 - getContainer</span><span class="sxs-lookup"><span data-stu-id="e5335-143">Return Value - getContainer</span></span>

## <a name="method-getmemorystream"></a><span data-ttu-id="e5335-144">メソッド getMemoryStream</span><span class="sxs-lookup"><span data-stu-id="e5335-144">Method getMemoryStream</span></span>

```xpp
public CLRObject getMemoryStream()
```

### <a name="return-value---getmemorystream"></a><span data-ttu-id="e5335-145">戻り値 - getMemoryStream</span><span class="sxs-lookup"><span data-stu-id="e5335-145">Return Value - getMemoryStream</span></span>

## <a name="method-qword"></a><span data-ttu-id="e5335-146">メソッド qWord</span><span class="sxs-lookup"><span data-stu-id="e5335-146">Method qWord</span></span>

```xpp
public Int64 qWord(int offset, [Int64 value])
```

### <a name="parameters---qword"></a><span data-ttu-id="e5335-147">パラメーター - qWord</span><span class="sxs-lookup"><span data-stu-id="e5335-147">Parameters - qWord</span></span>

<span data-ttu-id="e5335-148">相殺</span><span class="sxs-lookup"><span data-stu-id="e5335-148">offset</span></span>  

<!-- -->

<span data-ttu-id="e5335-149">値</span><span class="sxs-lookup"><span data-stu-id="e5335-149">value</span></span>  

### <a name="return-value---qword"></a><span data-ttu-id="e5335-150">戻り値 - qWord</span><span class="sxs-lookup"><span data-stu-id="e5335-150">Return Value - qWord</span></span>

## <a name="method-string"></a><span data-ttu-id="e5335-151">メソッド string</span><span class="sxs-lookup"><span data-stu-id="e5335-151">Method string</span></span>

```xpp
public str string(int offset, [str value])
```

### <a name="parameters---string"></a><span data-ttu-id="e5335-152">パラメーター - string</span><span class="sxs-lookup"><span data-stu-id="e5335-152">Parameters - string</span></span>

<span data-ttu-id="e5335-153">相殺</span><span class="sxs-lookup"><span data-stu-id="e5335-153">offset</span></span>  

<!-- -->

<span data-ttu-id="e5335-154">値</span><span class="sxs-lookup"><span data-stu-id="e5335-154">value</span></span>  

### <a name="return-value---string"></a><span data-ttu-id="e5335-155">戻り値 - string</span><span class="sxs-lookup"><span data-stu-id="e5335-155">Return Value - string</span></span>

## <a name="method-strlenbytes"></a><span data-ttu-id="e5335-156">メソッド strLenBytes</span><span class="sxs-lookup"><span data-stu-id="e5335-156">Method strLenBytes</span></span>

```xpp
public int strLenBytes(int offset)
```

### <a name="parameters---strlenbytes"></a><span data-ttu-id="e5335-157">パラメーター - strLenBytes</span><span class="sxs-lookup"><span data-stu-id="e5335-157">Parameters - strLenBytes</span></span>

<span data-ttu-id="e5335-158">相殺</span><span class="sxs-lookup"><span data-stu-id="e5335-158">offset</span></span>  

### <a name="return-value---strlenbytes"></a><span data-ttu-id="e5335-159">戻り値 - strLenBytes</span><span class="sxs-lookup"><span data-stu-id="e5335-159">Return Value - strLenBytes</span></span>

## <a name="method-word"></a><span data-ttu-id="e5335-160">メソッド word</span><span class="sxs-lookup"><span data-stu-id="e5335-160">Method word</span></span>

```xpp
public int word(int offset, [int value])
```

### <a name="parameters---word"></a><span data-ttu-id="e5335-161">パラメーター - word</span><span class="sxs-lookup"><span data-stu-id="e5335-161">Parameters - word</span></span>

<span data-ttu-id="e5335-162">相殺</span><span class="sxs-lookup"><span data-stu-id="e5335-162">offset</span></span>  

<!-- -->

<span data-ttu-id="e5335-163">値</span><span class="sxs-lookup"><span data-stu-id="e5335-163">value</span></span>  

### <a name="return-value---word"></a><span data-ttu-id="e5335-164">戻り値 - word</span><span class="sxs-lookup"><span data-stu-id="e5335-164">Return Value - word</span></span>

## <a name="method-wstring"></a><span data-ttu-id="e5335-165">メソッド wString</span><span class="sxs-lookup"><span data-stu-id="e5335-165">Method wString</span></span>

```xpp
public str wString(int offset, [str value])
```

### <a name="parameters---wstring"></a><span data-ttu-id="e5335-166">パラメーター - wString</span><span class="sxs-lookup"><span data-stu-id="e5335-166">Parameters - wString</span></span>

<span data-ttu-id="e5335-167">相殺</span><span class="sxs-lookup"><span data-stu-id="e5335-167">offset</span></span>  

<!-- -->

<span data-ttu-id="e5335-168">値</span><span class="sxs-lookup"><span data-stu-id="e5335-168">value</span></span>  

### <a name="return-value---wstring"></a><span data-ttu-id="e5335-169">戻り値 - wString</span><span class="sxs-lookup"><span data-stu-id="e5335-169">Return Value - wString</span></span>

## <a name="method-constructfromcontainer"></a><span data-ttu-id="e5335-170">メソッド constructFromContainer</span><span class="sxs-lookup"><span data-stu-id="e5335-170">Method constructFromContainer</span></span>

```xpp
public static Binary constructFromContainer(container data)
```

### <a name="parameters---constructfromcontainer"></a><span data-ttu-id="e5335-171">パラメーター   constructFromContainer</span><span class="sxs-lookup"><span data-stu-id="e5335-171">Parameters - constructFromContainer</span></span>

<span data-ttu-id="e5335-172">データ</span><span class="sxs-lookup"><span data-stu-id="e5335-172">data</span></span>  

### <a name="return-value---constructfromcontainer"></a><span data-ttu-id="e5335-173">戻り値 - constructFromContainer</span><span class="sxs-lookup"><span data-stu-id="e5335-173">Return Value - constructFromContainer</span></span>

## <a name="method-constructfrommemorystream"></a><span data-ttu-id="e5335-174">メソッド constructFromMemoryStream</span><span class="sxs-lookup"><span data-stu-id="e5335-174">Method constructFromMemoryStream</span></span>

```xpp
public static Binary constructFromMemoryStream(CLRObject memoryStream)
```

### <a name="parameters---constructfrommemorystream"></a><span data-ttu-id="e5335-175">パラメーター - constructFromMemoryStream</span><span class="sxs-lookup"><span data-stu-id="e5335-175">Parameters - constructFromMemoryStream</span></span>

<span data-ttu-id="e5335-176">memoryStream</span><span class="sxs-lookup"><span data-stu-id="e5335-176">memoryStream</span></span>  

### <a name="return-value---constructfrommemorystream"></a><span data-ttu-id="e5335-177">戻り値 - constructFromMemoryStream</span><span class="sxs-lookup"><span data-stu-id="e5335-177">Return Value - constructFromMemoryStream</span></span>

## <a name="method-attach"></a><span data-ttu-id="e5335-178">メソッド attach</span><span class="sxs-lookup"><span data-stu-id="e5335-178">Method attach</span></span>

```xpp
public void attach(Int64 bufPtr, int bufSize)
```

### <a name="parameters---attach"></a><span data-ttu-id="e5335-179">パラメーター - attach</span><span class="sxs-lookup"><span data-stu-id="e5335-179">Parameters - attach</span></span>

<span data-ttu-id="e5335-180">bufPtr</span><span class="sxs-lookup"><span data-stu-id="e5335-180">bufPtr</span></span>  

<!-- -->

<span data-ttu-id="e5335-181">bufSize</span><span class="sxs-lookup"><span data-stu-id="e5335-181">bufSize</span></span>  

## <a name="method-finalize"></a><span data-ttu-id="e5335-182">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="e5335-182">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-appendsubstring"></a><span data-ttu-id="e5335-183">メソッド appendSubString</span><span class="sxs-lookup"><span data-stu-id="e5335-183">Method appendSubString</span></span>

```xpp
public void appendSubString([str string])
```

### <a name="parameters---appendsubstring"></a><span data-ttu-id="e5335-184">パラメーター - appendSubString</span><span class="sxs-lookup"><span data-stu-id="e5335-184">Parameters - appendSubString</span></span>

<span data-ttu-id="e5335-185">文字列</span><span class="sxs-lookup"><span data-stu-id="e5335-185">string</span></span>  

## <a name="method-setbinaryvalue"></a><span data-ttu-id="e5335-186">メソッド setBinaryValue</span><span class="sxs-lookup"><span data-stu-id="e5335-186">Method setBinaryValue</span></span>

```xpp
public void setBinaryValue(int offset, Binary value)
```

### <a name="parameters---setbinaryvalue"></a><span data-ttu-id="e5335-187">パラメーター - setBinaryValue</span><span class="sxs-lookup"><span data-stu-id="e5335-187">Parameters - setBinaryValue</span></span>

<span data-ttu-id="e5335-188">相殺</span><span class="sxs-lookup"><span data-stu-id="e5335-188">offset</span></span>  

<!-- -->

<span data-ttu-id="e5335-189">値</span><span class="sxs-lookup"><span data-stu-id="e5335-189">value</span></span>  

## <a name="method-new"></a><span data-ttu-id="e5335-190">メソッド new</span><span class="sxs-lookup"><span data-stu-id="e5335-190">Method new</span></span>

<span data-ttu-id="e5335-191">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e5335-191">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(AnyType buffersizeOrString, [boolean wideString])
```

### <a name="parameters---new"></a><span data-ttu-id="e5335-192">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="e5335-192">Parameters - new</span></span>

<span data-ttu-id="e5335-193">buffersizeOrString</span><span class="sxs-lookup"><span data-stu-id="e5335-193">buffersizeOrString</span></span>  

<!-- -->

<span data-ttu-id="e5335-194">wideString</span><span class="sxs-lookup"><span data-stu-id="e5335-194">wideString</span></span>  

