---
title: "B クラス"
description: "文字 B で始まるシステム API クラス。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 50951
ms.assetid: 23a67a79-4f80-4f48-802a-08aba7824259
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7578acce04846b7e3f249f42688fcc6e9c345411
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="b-classes"></a><span data-ttu-id="0d46f-103">B クラス</span><span class="sxs-lookup"><span data-stu-id="0d46f-103">B Classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d46f-104">文字 B で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="0d46f-104">System API classes that start with the letter B.</span></span>

<a name="class-binary"></a><span data-ttu-id="0d46f-105">クラス バイナリ</span><span class="sxs-lookup"><span data-stu-id="0d46f-105">Class Binary</span></span>
------------

    class Binary extends Object

### <a name="remarks"></a><span data-ttu-id="0d46f-106">備考</span><span class="sxs-lookup"><span data-stu-id="0d46f-106">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="0d46f-107">例</span><span class="sxs-lookup"><span data-stu-id="0d46f-107">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="0d46f-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="0d46f-108">Methods</span></span>

| <span data-ttu-id="0d46f-109">方法</span><span class="sxs-lookup"><span data-stu-id="0d46f-109">Method</span></span>                                                                   | <span data-ttu-id="0d46f-110">説明</span><span class="sxs-lookup"><span data-stu-id="0d46f-110">Description</span></span>                                     |
|--------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="0d46f-111">public int byte(int offset, \[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d46f-111">public int byte(int offset, \[int value\])</span></span>                               |                                                 |
| <span data-ttu-id="0d46f-112">public Real double(int offset, \[Real value\])</span><span class="sxs-lookup"><span data-stu-id="0d46f-112">public Real double(int offset, \[Real value\])</span></span>                           |                                                 |
| <span data-ttu-id="0d46f-113">public int dWord(int offset, \[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d46f-113">public int dWord(int offset, \[int value\])</span></span>                              |                                                 |
| <span data-ttu-id="0d46f-114">public container getContainer()</span><span class="sxs-lookup"><span data-stu-id="0d46f-114">public container getContainer()</span></span>                                          |                                                 |
| <span data-ttu-id="0d46f-115">public CLRObject getMemoryStream()</span><span class="sxs-lookup"><span data-stu-id="0d46f-115">public CLRObject getMemoryStream()</span></span>                                       |                                                 |
| <span data-ttu-id="0d46f-116">public Int64 qWord(int offset, \[Int64 value\])</span><span class="sxs-lookup"><span data-stu-id="0d46f-116">public Int64 qWord(int offset, \[Int64 value\])</span></span>                          |                                                 |
| <span data-ttu-id="0d46f-117">public str string(int offset, \[str value\])</span><span class="sxs-lookup"><span data-stu-id="0d46f-117">public str string(int offset, \[str value\])</span></span>                             |                                                 |
| <span data-ttu-id="0d46f-118">public int strLenBytes(int offset)</span><span class="sxs-lookup"><span data-stu-id="0d46f-118">public int strLenBytes(int offset)</span></span>                                       |                                                 |
| <span data-ttu-id="0d46f-119">public int word(int offset, \[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d46f-119">public int word(int offset, \[int value\])</span></span>                               |                                                 |
| <span data-ttu-id="0d46f-120">public str wString(int offset, \[str value\])</span><span class="sxs-lookup"><span data-stu-id="0d46f-120">public str wString(int offset, \[str value\])</span></span>                            |                                                 |
| <span data-ttu-id="0d46f-121">::public static Binary constructFromContainer(container data)</span><span class="sxs-lookup"><span data-stu-id="0d46f-121">::public static Binary constructFromContainer(container data)</span></span>            |                                                 |
| <span data-ttu-id="0d46f-122">::public static Binary constructFromMemoryStream(CLRObject memoryStream)</span><span class="sxs-lookup"><span data-stu-id="0d46f-122">::public static Binary constructFromMemoryStream(CLRObject memoryStream)</span></span> |                                                 |
| <span data-ttu-id="0d46f-123">public void attach(Int64 bufPtr, int bufSize)</span><span class="sxs-lookup"><span data-stu-id="0d46f-123">public void attach(Int64 bufPtr, int bufSize)</span></span>                            |                                                 |
| <span data-ttu-id="0d46f-124">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="0d46f-124">public void finalize()</span></span>                                                   |                                                 |
| <span data-ttu-id="0d46f-125">public void appendSubString(\[str string\])</span><span class="sxs-lookup"><span data-stu-id="0d46f-125">public void appendSubString(\[str string\])</span></span>                              |                                                 |
| <span data-ttu-id="0d46f-126">public void setBinaryValue(int offset, Binary value)</span><span class="sxs-lookup"><span data-stu-id="0d46f-126">public void setBinaryValue(int offset, Binary value)</span></span>                     |                                                 |
| <span data-ttu-id="0d46f-127">public void new(AnyType buffersizeOrString, \[boolean wideString\])</span><span class="sxs-lookup"><span data-stu-id="0d46f-127">public void new(AnyType buffersizeOrString, \[boolean wideString\])</span></span>      | <span data-ttu-id="0d46f-128">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="0d46f-128">Initializes a new instance of the Object class.</span></span> |

### <a name="method-byte"></a><span data-ttu-id="0d46f-129">メソッド byte</span><span class="sxs-lookup"><span data-stu-id="0d46f-129">Method byte</span></span>

    public int byte(int offset, [int value])

#### <a name="parameters"></a><span data-ttu-id="0d46f-130">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-130">Parameters</span></span>

<span data-ttu-id="0d46f-131">相殺</span><span class="sxs-lookup"><span data-stu-id="0d46f-131">offset</span></span>  

<!-- -->

<span data-ttu-id="0d46f-132">値</span><span class="sxs-lookup"><span data-stu-id="0d46f-132">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="0d46f-133">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-133">Return Value</span></span>

### <a name="method-double"></a><span data-ttu-id="0d46f-134">メソッド double</span><span class="sxs-lookup"><span data-stu-id="0d46f-134">Method double</span></span>

    public Real double(int offset, [Real value])

#### <a name="parameters"></a><span data-ttu-id="0d46f-135">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-135">Parameters</span></span>

<span data-ttu-id="0d46f-136">相殺</span><span class="sxs-lookup"><span data-stu-id="0d46f-136">offset</span></span>  

<!-- -->

<span data-ttu-id="0d46f-137">値</span><span class="sxs-lookup"><span data-stu-id="0d46f-137">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="0d46f-138">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-138">Return Value</span></span>

### <a name="method-dword"></a><span data-ttu-id="0d46f-139">メソッド dWord</span><span class="sxs-lookup"><span data-stu-id="0d46f-139">Method dWord</span></span>

    public int dWord(int offset, [int value])

#### <a name="parameters"></a><span data-ttu-id="0d46f-140">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-140">Parameters</span></span>

<span data-ttu-id="0d46f-141">相殺</span><span class="sxs-lookup"><span data-stu-id="0d46f-141">offset</span></span>  

<!-- -->

<span data-ttu-id="0d46f-142">値</span><span class="sxs-lookup"><span data-stu-id="0d46f-142">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="0d46f-143">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-143">Return Value</span></span>

### <a name="method-getcontainer"></a><span data-ttu-id="0d46f-144">メソッド getContainer</span><span class="sxs-lookup"><span data-stu-id="0d46f-144">Method getContainer</span></span>

    public container getContainer()

#### <a name="return-value"></a><span data-ttu-id="0d46f-145">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-145">Return Value</span></span>

### <a name="method-getmemorystream"></a><span data-ttu-id="0d46f-146">メソッド getMemoryStream</span><span class="sxs-lookup"><span data-stu-id="0d46f-146">Method getMemoryStream</span></span>

    public CLRObject getMemoryStream()

#### <a name="return-value"></a><span data-ttu-id="0d46f-147">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-147">Return Value</span></span>

### <a name="method-qword"></a><span data-ttu-id="0d46f-148">メソッド qWord</span><span class="sxs-lookup"><span data-stu-id="0d46f-148">Method qWord</span></span>

    public Int64 qWord(int offset, [Int64 value])

#### <a name="parameters"></a><span data-ttu-id="0d46f-149">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-149">Parameters</span></span>

<span data-ttu-id="0d46f-150">相殺</span><span class="sxs-lookup"><span data-stu-id="0d46f-150">offset</span></span>  

<!-- -->

<span data-ttu-id="0d46f-151">値</span><span class="sxs-lookup"><span data-stu-id="0d46f-151">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="0d46f-152">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-152">Return Value</span></span>

### <a name="method-string"></a><span data-ttu-id="0d46f-153">メソッド string</span><span class="sxs-lookup"><span data-stu-id="0d46f-153">Method string</span></span>

    public str string(int offset, [str value])

#### <a name="parameters"></a><span data-ttu-id="0d46f-154">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-154">Parameters</span></span>

<span data-ttu-id="0d46f-155">相殺</span><span class="sxs-lookup"><span data-stu-id="0d46f-155">offset</span></span>  

<!-- -->

<span data-ttu-id="0d46f-156">値</span><span class="sxs-lookup"><span data-stu-id="0d46f-156">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="0d46f-157">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-157">Return Value</span></span>

### <a name="method-strlenbytes"></a><span data-ttu-id="0d46f-158">メソッド strLenBytes</span><span class="sxs-lookup"><span data-stu-id="0d46f-158">Method strLenBytes</span></span>

    public int strLenBytes(int offset)

#### <a name="parameters"></a><span data-ttu-id="0d46f-159">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-159">Parameters</span></span>

<span data-ttu-id="0d46f-160">相殺</span><span class="sxs-lookup"><span data-stu-id="0d46f-160">offset</span></span>  

#### <a name="return-value"></a><span data-ttu-id="0d46f-161">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-161">Return Value</span></span>

### <a name="method-word"></a><span data-ttu-id="0d46f-162">メソッド word</span><span class="sxs-lookup"><span data-stu-id="0d46f-162">Method word</span></span>

    public int word(int offset, [int value])

#### <a name="parameters"></a><span data-ttu-id="0d46f-163">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-163">Parameters</span></span>

<span data-ttu-id="0d46f-164">相殺</span><span class="sxs-lookup"><span data-stu-id="0d46f-164">offset</span></span>  

<!-- -->

<span data-ttu-id="0d46f-165">値</span><span class="sxs-lookup"><span data-stu-id="0d46f-165">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="0d46f-166">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-166">Return Value</span></span>

### <a name="method-wstring"></a><span data-ttu-id="0d46f-167">メソッド wString</span><span class="sxs-lookup"><span data-stu-id="0d46f-167">Method wString</span></span>

    public str wString(int offset, [str value])

#### <a name="parameters"></a><span data-ttu-id="0d46f-168">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-168">Parameters</span></span>

<span data-ttu-id="0d46f-169">相殺</span><span class="sxs-lookup"><span data-stu-id="0d46f-169">offset</span></span>  

<!-- -->

<span data-ttu-id="0d46f-170">値</span><span class="sxs-lookup"><span data-stu-id="0d46f-170">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="0d46f-171">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-171">Return Value</span></span>

### <a name="method-constructfromcontainer"></a><span data-ttu-id="0d46f-172">メソッド constructFromContainer</span><span class="sxs-lookup"><span data-stu-id="0d46f-172">Method constructFromContainer</span></span>

    public static Binary constructFromContainer(container data)

#### <a name="parameters"></a><span data-ttu-id="0d46f-173">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-173">Parameters</span></span>

<span data-ttu-id="0d46f-174">データ</span><span class="sxs-lookup"><span data-stu-id="0d46f-174">data</span></span>  

#### <a name="return-value"></a><span data-ttu-id="0d46f-175">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-175">Return Value</span></span>

### <a name="method-constructfrommemorystream"></a><span data-ttu-id="0d46f-176">メソッド constructFromMemoryStream</span><span class="sxs-lookup"><span data-stu-id="0d46f-176">Method constructFromMemoryStream</span></span>

    public static Binary constructFromMemoryStream(CLRObject memoryStream)

#### <a name="parameters"></a><span data-ttu-id="0d46f-177">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-177">Parameters</span></span>

<span data-ttu-id="0d46f-178">memoryStream</span><span class="sxs-lookup"><span data-stu-id="0d46f-178">memoryStream</span></span>  

#### <a name="return-value"></a><span data-ttu-id="0d46f-179">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-179">Return Value</span></span>

### <a name="method-attach"></a><span data-ttu-id="0d46f-180">メソッド attach</span><span class="sxs-lookup"><span data-stu-id="0d46f-180">Method attach</span></span>

    public void attach(Int64 bufPtr, int bufSize)

#### <a name="parameters"></a><span data-ttu-id="0d46f-181">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-181">Parameters</span></span>

<span data-ttu-id="0d46f-182">bufPtr</span><span class="sxs-lookup"><span data-stu-id="0d46f-182">bufPtr</span></span>  

<!-- -->

<span data-ttu-id="0d46f-183">bufSize</span><span class="sxs-lookup"><span data-stu-id="0d46f-183">bufSize</span></span>  

### <a name="method-finalize"></a><span data-ttu-id="0d46f-184">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="0d46f-184">Method finalize</span></span>

    public void finalize()

### <a name="method-appendsubstring"></a><span data-ttu-id="0d46f-185">メソッド appendSubString</span><span class="sxs-lookup"><span data-stu-id="0d46f-185">Method appendSubString</span></span>

    public void appendSubString([str string])

#### <a name="parameters"></a><span data-ttu-id="0d46f-186">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-186">Parameters</span></span>

<span data-ttu-id="0d46f-187">string</span><span class="sxs-lookup"><span data-stu-id="0d46f-187">string</span></span>  

### <a name="method-setbinaryvalue"></a><span data-ttu-id="0d46f-188">メソッド setBinaryValue</span><span class="sxs-lookup"><span data-stu-id="0d46f-188">Method setBinaryValue</span></span>

    public void setBinaryValue(int offset, Binary value)

#### <a name="parameters"></a><span data-ttu-id="0d46f-189">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-189">Parameters</span></span>

<span data-ttu-id="0d46f-190">相殺</span><span class="sxs-lookup"><span data-stu-id="0d46f-190">offset</span></span>  

<!-- -->

<span data-ttu-id="0d46f-191">値</span><span class="sxs-lookup"><span data-stu-id="0d46f-191">value</span></span>  

### <a name="method-new"></a><span data-ttu-id="0d46f-192">メソッド new</span><span class="sxs-lookup"><span data-stu-id="0d46f-192">Method new</span></span>

<span data-ttu-id="0d46f-193">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="0d46f-193">Initializes a new instance of the Object class.</span></span>

    public void new(AnyType buffersizeOrString, [boolean wideString])

#### <a name="parameters"></a><span data-ttu-id="0d46f-194">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-194">Parameters</span></span>

<span data-ttu-id="0d46f-195">buffersizeOrString</span><span class="sxs-lookup"><span data-stu-id="0d46f-195">buffersizeOrString</span></span>  

<!-- -->

<span data-ttu-id="0d46f-196">wideString</span><span class="sxs-lookup"><span data-stu-id="0d46f-196">wideString</span></span>  

## <a name="class-binaryio"></a><span data-ttu-id="0d46f-197">クラス BinaryIo</span><span class="sxs-lookup"><span data-stu-id="0d46f-197">Class BinaryIo</span></span>
    class BinaryIo extends Io

### <a name="remarks"></a><span data-ttu-id="0d46f-198">備考</span><span class="sxs-lookup"><span data-stu-id="0d46f-198">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="0d46f-199">例</span><span class="sxs-lookup"><span data-stu-id="0d46f-199">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="0d46f-200">メソッド</span><span class="sxs-lookup"><span data-stu-id="0d46f-200">Methods</span></span>

| <span data-ttu-id="0d46f-201">方法</span><span class="sxs-lookup"><span data-stu-id="0d46f-201">Method</span></span>                                  | <span data-ttu-id="0d46f-202">説明</span><span class="sxs-lookup"><span data-stu-id="0d46f-202">Description</span></span>                                                                     |
|-----------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="0d46f-203">public container read()</span><span class="sxs-lookup"><span data-stu-id="0d46f-203">public container read()</span></span>                 | <span data-ttu-id="0d46f-204">Io オブジェクトから次の完全なレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="0d46f-204">Reads the next full record from the Io object.</span></span>                                  |
| <span data-ttu-id="0d46f-205">public IO\_Status status()</span><span class="sxs-lookup"><span data-stu-id="0d46f-205">public IO\_Status status()</span></span>              | <span data-ttu-id="0d46f-206">Io オブジェクトで実行された最後の操作のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="0d46f-206">Retrieves the status of the last operation that was performed on the Io object.</span></span> |
| <span data-ttu-id="0d46f-207">public boolean write(VarArg values)</span><span class="sxs-lookup"><span data-stu-id="0d46f-207">public boolean write(VarArg values)</span></span>     | <span data-ttu-id="0d46f-208">単純型の値を記述します。</span><span class="sxs-lookup"><span data-stu-id="0d46f-208">Writes values of a simple type.</span></span>                                                 |
| <span data-ttu-id="0d46f-209">public boolean writeExp(container data)</span><span class="sxs-lookup"><span data-stu-id="0d46f-209">public boolean writeExp(container data)</span></span> | <span data-ttu-id="0d46f-210">コンテナのコンテンツをファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="0d46f-210">Writes the content of a container to a file.</span></span>                                    |
| <span data-ttu-id="0d46f-211">public void new(str filename, str mode)</span><span class="sxs-lookup"><span data-stu-id="0d46f-211">public void new(str filename, str mode)</span></span> | <span data-ttu-id="0d46f-212">BinaryIo クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="0d46f-212">Creates an instance of the BinaryIo class.</span></span>                                      |
| <span data-ttu-id="0d46f-213">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="0d46f-213">public void finalize()</span></span>                  | <span data-ttu-id="0d46f-214">ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="0d46f-214">Closes the file and, if data was written, flushes the file buffers to disk.</span></span>     |

### <a name="method-read"></a><span data-ttu-id="0d46f-215">メソッド read</span><span class="sxs-lookup"><span data-stu-id="0d46f-215">Method read</span></span>

<span data-ttu-id="0d46f-216">Io オブジェクトから次の完全なレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="0d46f-216">Reads the next full record from the Io object.</span></span>

    public container read()

#### <a name="return-value"></a><span data-ttu-id="0d46f-217">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-217">Return Value</span></span>

<span data-ttu-id="0d46f-218">入出力オブジェクトから次の完全なレコードを保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="0d46f-218">A container that holds the next full record from the Io object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="0d46f-219">備考</span><span class="sxs-lookup"><span data-stu-id="0d46f-219">Remarks</span></span>

<span data-ttu-id="0d46f-220">次の完全なレコードの定義は、次のプロパティ、inFieldDelimiter、inRecordDelimiter、および inRecordLength メソッド プロパティによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="0d46f-220">The definition of the next full record is controlled by the inFieldDelimiter, inRecordDelimiter, and inRecordLength method properties.</span></span> <span data-ttu-id="0d46f-221">レコードはコンテナーとして返されます。</span><span class="sxs-lookup"><span data-stu-id="0d46f-221">The record is returned as a container.</span></span> <span data-ttu-id="0d46f-222">コンテナー内の各エントリは、レコードの 1 つのフィールドと同じです。</span><span class="sxs-lookup"><span data-stu-id="0d46f-222">Each entry in the container equals one field in the record.</span></span> <span data-ttu-id="0d46f-223">そべての特殊な Io クラスには、inFieldDelimiter、inRecordDelimiter、および inRecordLength のプロパティのデフォルト設定があります。</span><span class="sxs-lookup"><span data-stu-id="0d46f-223">Every specialized Io class has default settings for the inFieldDelimiter, inRecordDelimiter, and inRecordLength properties.</span></span> <span data-ttu-id="0d46f-224">これらの既定の設定では、最も一般的な形式の入力と出力が可能です。</span><span class="sxs-lookup"><span data-stu-id="0d46f-224">These default settings enable input and output of the most common formats.</span></span> <span data-ttu-id="0d46f-225">使用する形式をサポートするために、これらの設定の調整が生じる場合があります。</span><span class="sxs-lookup"><span data-stu-id="0d46f-225">You might have to adjust these settings to support the format that you want to use.</span></span>

### <a name="method-status"></a><span data-ttu-id="0d46f-226">メソッド status</span><span class="sxs-lookup"><span data-stu-id="0d46f-226">Method status</span></span>

<span data-ttu-id="0d46f-227">Io オブジェクトで実行された最後の操作のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="0d46f-227">Retrieves the status of the last operation that was performed on the Io object.</span></span>

    public IO_Status status()

#### <a name="return-value"></a><span data-ttu-id="0d46f-228">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-228">Return Value</span></span>

<span data-ttu-id="0d46f-229">IO\_Status システム列挙値としての最後の操作の状態。</span><span class="sxs-lookup"><span data-stu-id="0d46f-229">The status of the last operation as an IO\_Status system enumeration value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="0d46f-230">備考</span><span class="sxs-lookup"><span data-stu-id="0d46f-230">Remarks</span></span>

<span data-ttu-id="0d46f-231">返される可能性のある IO\_Status の値の範囲は、Io クラスによって異なります。</span><span class="sxs-lookup"><span data-stu-id="0d46f-231">The range of possible IO\_Status values that are returned varies, depending on the Io class.</span></span>

### <a name="method-write"></a><span data-ttu-id="0d46f-232">メソッド write</span><span class="sxs-lookup"><span data-stu-id="0d46f-232">Method write</span></span>

<span data-ttu-id="0d46f-233">単純型の値を記述します。</span><span class="sxs-lookup"><span data-stu-id="0d46f-233">Writes values of a simple type.</span></span>

    public boolean write(VarArg values)

#### <a name="parameters"></a><span data-ttu-id="0d46f-234">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-234">Parameters</span></span>

<span data-ttu-id="0d46f-235">値</span><span class="sxs-lookup"><span data-stu-id="0d46f-235">values</span></span>  
<span data-ttu-id="0d46f-236">単純型。</span><span class="sxs-lookup"><span data-stu-id="0d46f-236">The simple type.</span></span> <span data-ttu-id="0d46f-237">単純型は、文字列、整数、実数、列挙型、日付です。</span><span class="sxs-lookup"><span data-stu-id="0d46f-237">The simple types are string, integer, real, enum, and date.</span></span>

#### <a name="return-value"></a><span data-ttu-id="0d46f-238">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-238">Return Value</span></span>

<span data-ttu-id="0d46f-239">書き込み操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0d46f-239">true if the write operation succeeds; otherwise, false.</span></span> <span data-ttu-id="0d46f-240">書き込み操作が失敗すると、ステータス メソッドで原因について確認できます。</span><span class="sxs-lookup"><span data-stu-id="0d46f-240">If the write operation is unsuccessful, you can check the status method for the cause.</span></span>

#### <a name="remarks"></a><span data-ttu-id="0d46f-241">備考</span><span class="sxs-lookup"><span data-stu-id="0d46f-241">Remarks</span></span>

<span data-ttu-id="0d46f-242">このメソッドは、可変数の引数を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="0d46f-242">This method accepts a variable number of arguments.</span></span> <span data-ttu-id="0d46f-243">指定された各値は、フィールドとして出力レコードに配置されます。</span><span class="sxs-lookup"><span data-stu-id="0d46f-243">Each value that is specified is put into the output record as a field.</span></span> <span data-ttu-id="0d46f-244">最初の引数は最初のフィールドであり、2 番目の引数は 2 番目のフィールドなどになります。</span><span class="sxs-lookup"><span data-stu-id="0d46f-244">The first argument is the first field, the second argument is the second field, and so on.</span></span> <span data-ttu-id="0d46f-245">フィールドは、outFieldDelimiter メソッドで指定されたフィールド区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="0d46f-245">The fields are separated by the field delimiter that is specified in the outFieldDelimiter method.</span></span> <span data-ttu-id="0d46f-246">各レコードは、outRecordDelimiter メソッドで指定されるレコード 区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="0d46f-246">Each record is separated by the record delimiter that is specified in the outRecordDelimiter method.</span></span> <span data-ttu-id="0d46f-247">完全なコンテナーを書き込むには、writeExp メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="0d46f-247">To write complete containers, use the writeExp method.</span></span>

### <a name="method-writeexp"></a><span data-ttu-id="0d46f-248">メソッド writeExp</span><span class="sxs-lookup"><span data-stu-id="0d46f-248">Method writeExp</span></span>

<span data-ttu-id="0d46f-249">コンテナのコンテンツをファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="0d46f-249">Writes the content of a container to a file.</span></span>

    public boolean writeExp(container data)

#### <a name="parameters"></a><span data-ttu-id="0d46f-250">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-250">Parameters</span></span>

<span data-ttu-id="0d46f-251">データ</span><span class="sxs-lookup"><span data-stu-id="0d46f-251">data</span></span>  
<span data-ttu-id="0d46f-252">レコードのデータを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="0d46f-252">The container that holds data for the record.</span></span>

#### <a name="return-value"></a><span data-ttu-id="0d46f-253">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-253">Return Value</span></span>

<span data-ttu-id="0d46f-254">操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0d46f-254">true if the operation is successful; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="0d46f-255">備考</span><span class="sxs-lookup"><span data-stu-id="0d46f-255">Remarks</span></span>

<span data-ttu-id="0d46f-256">このメソッドが false を返す場合、ステータス メソッドで原因を確認します。</span><span class="sxs-lookup"><span data-stu-id="0d46f-256">If this method returns false, check the status method for the cause.</span></span> <span data-ttu-id="0d46f-257">コンテナー内のエントリはフィールドとして扱われ、コンテナーは完全なレコードとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="0d46f-257">The entries in the container are treated as fields, and the container is treated as a full record.</span></span> <span data-ttu-id="0d46f-258">フィールド区切り記号は、outFieldDelimiter メソッドで定義されています。</span><span class="sxs-lookup"><span data-stu-id="0d46f-258">The field separator is defined in the outFieldDelimiter method.</span></span> <span data-ttu-id="0d46f-259">レコード区切りは outRecordDelimiter メソッドで定義されます。</span><span class="sxs-lookup"><span data-stu-id="0d46f-259">The record separator is defined in the outRecordDelimiter method.</span></span>

### <a name="method-new"></a><span data-ttu-id="0d46f-260">メソッド new</span><span class="sxs-lookup"><span data-stu-id="0d46f-260">Method new</span></span>

<span data-ttu-id="0d46f-261">BinaryIo クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="0d46f-261">Creates an instance of the BinaryIo class.</span></span>

    public void new(str filename, str mode)

#### <a name="parameters"></a><span data-ttu-id="0d46f-262">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-262">Parameters</span></span>

<span data-ttu-id="0d46f-263">filename</span><span class="sxs-lookup"><span data-stu-id="0d46f-263">filename</span></span>  
<span data-ttu-id="0d46f-264">BinaryIo クラスのインスタンスを作成するために使用するモード。</span><span class="sxs-lookup"><span data-stu-id="0d46f-264">The mode to use to create the instance of the BinaryIo class.</span></span>

<!-- -->

<span data-ttu-id="0d46f-265">モード</span><span class="sxs-lookup"><span data-stu-id="0d46f-265">mode</span></span>  
<span data-ttu-id="0d46f-266">BinaryIo クラスのインスタンスを作成するために使用するモード。</span><span class="sxs-lookup"><span data-stu-id="0d46f-266">The mode to use to create the instance of the BinaryIo class.</span></span>

#### <a name="remarks"></a><span data-ttu-id="0d46f-267">備考</span><span class="sxs-lookup"><span data-stu-id="0d46f-267">Remarks</span></span>

<span data-ttu-id="0d46f-268">攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="0d46f-268">If an attacker can control input to the new method, a security risk exists.</span></span> <span data-ttu-id="0d46f-269">したがって、このメソッドはクラス下で実行されます。</span><span class="sxs-lookup"><span data-stu-id="0d46f-269">Therefore, this method runs under class.</span></span> <span data-ttu-id="0d46f-270">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0d46f-270">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

#### <a name="examples"></a><span data-ttu-id="0d46f-271">例</span><span class="sxs-lookup"><span data-stu-id="0d46f-271">Examples</span></span>

<span data-ttu-id="0d46f-272">この例では、BinaryIo クラスを使用して、ExampleFile のテキスト ファイルからデータを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="0d46f-272">This example uses the BinaryIo class to read data from the ExampleFile text file.</span></span>

    static void BinaryIoExampleW2(Args _args)
    {     
        #define.ExampleFile(@"D:\Writers\GeneMi\_Junk\TestW.BinaryIo")
        #define.ExampleOpenModeW("w")
        #define.ExampleOpenModeR("r")
        BinaryIo binaryIoObject;
        container con1;
        str sConRecs;
        FileIoPermission perm;

        // Set the code access permission to help protect the use of
        // the BinaryIo.new method.
        perm = new FileIoPermission(#ExampleFile, #ExampleOpenModeW);
        if (perm == null)
        {
            return;
        }
        perm.assert();

        // Overwrites the file if it already exists; restarts it as empty.
        binaryIoObject = new BinaryIo(#ExampleFile, #ExampleOpenModeW);
        if (binaryIoObject != null)
        {
            info("w binaryIoObject is NOT null, Good.");
            binaryIoObject.write("hello world");
            binaryIoObject.write("goodbye solar system");
        }
        else
        {
            warning("w binaryIoObject is NULL, Bad.");
        }

        binaryIoObject.finalize();
        binaryIoObject = null;
        // Close the file, w?
        // BinaryIo instance can only read files in that
        // are in the exact same esoteric format that BinaryIo
        // writes files to.
        // binaryIoObject = new BinaryIo(#ExampleFile, #ExampleOpenModeR);
        if (binaryIoObject != null)
        {
             info("r binaryIoObject is NOT null, Good.");
             while (true)
            {
                con1 = binaryIoObject.read();
                if (con1 == conNull())
                {
                    info("r, no more records.");
                    break;
                }
                sConRecs = con2Str(con1);
                info(sConRecs);
            }
        }
        else
        {
             warning("r binaryIoObject is NULL, Bad.");
        }
        binaryIoObject.finalize();
        binaryIoObject = null;
        WINAPI::deleteFile(#ExampleFile);
         // Clean up after the job.
        CodeAccessPermission::revertAssert();
     }
    /*** Output copied from Infolog:Message (11:22:16 am)w binaryIoObject is NOT null, Good.r binaryIoObject is NOT null, Good.hello worldgoodbye solar systemr, no more records.***/

### <a name="method-finalize"></a><span data-ttu-id="0d46f-273">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="0d46f-273">Method finalize</span></span>

<span data-ttu-id="0d46f-274">ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="0d46f-274">Closes the file and, if data was written, flushes the file buffers to disk.</span></span>

    public void finalize()

#### <a name="remarks"></a><span data-ttu-id="0d46f-275">備考</span><span class="sxs-lookup"><span data-stu-id="0d46f-275">Remarks</span></span>

<span data-ttu-id="0d46f-276">通常、スコープを離れることでオブジェクトを確定します。</span><span class="sxs-lookup"><span data-stu-id="0d46f-276">Typically, you finalize the object by leaving the scope.</span></span> <span data-ttu-id="0d46f-277">したがって、確定メソッドは、通常は直接呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="0d46f-277">Therefore, the finalize method is not usually called directly.</span></span> <span data-ttu-id="0d46f-278">記述された出力はオブジェクトが終了するまで無効です。</span><span class="sxs-lookup"><span data-stu-id="0d46f-278">Written output is not valid until the object is finalized.</span></span>

## <a name="class-bindata"></a><span data-ttu-id="0d46f-279">クラス BinData</span><span class="sxs-lookup"><span data-stu-id="0d46f-279">Class BinData</span></span>
    class BinData extends Object

### <a name="remarks"></a><span data-ttu-id="0d46f-280">備考</span><span class="sxs-lookup"><span data-stu-id="0d46f-280">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="0d46f-281">例</span><span class="sxs-lookup"><span data-stu-id="0d46f-281">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="0d46f-282">メソッド</span><span class="sxs-lookup"><span data-stu-id="0d46f-282">Methods</span></span>

| <span data-ttu-id="0d46f-283">方法</span><span class="sxs-lookup"><span data-stu-id="0d46f-283">Method</span></span>                                                                | <span data-ttu-id="0d46f-284">説明</span><span class="sxs-lookup"><span data-stu-id="0d46f-284">Description</span></span>                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="0d46f-285">public boolean appendToFile(str filename)</span><span class="sxs-lookup"><span data-stu-id="0d46f-285">public boolean appendToFile(str filename)</span></span>                             |                                               |
| <span data-ttu-id="0d46f-286">public str ascii85Encode()</span><span class="sxs-lookup"><span data-stu-id="0d46f-286">public str ascii85Encode()</span></span>                                            |                                               |
| <span data-ttu-id="0d46f-287">public str base64Encode()</span><span class="sxs-lookup"><span data-stu-id="0d46f-287">public str base64Encode()</span></span>                                             |                                               |
| <span data-ttu-id="0d46f-288">public int compressLZ77(int windowBits)</span><span class="sxs-lookup"><span data-stu-id="0d46f-288">public int compressLZ77(int windowBits)</span></span>                               |                                               |
| <span data-ttu-id="0d46f-289">public boolean copyData(BinData data, \[int offset\], \[int length\])</span><span class="sxs-lookup"><span data-stu-id="0d46f-289">public boolean copyData(BinData data, \[int offset\], \[int length\])</span></span> |                                               |
| <span data-ttu-id="0d46f-290">public int decompressLZ77()</span><span class="sxs-lookup"><span data-stu-id="0d46f-290">public int decompressLZ77()</span></span>                                           |                                               |
| <span data-ttu-id="0d46f-291">public str getAsciiData()</span><span class="sxs-lookup"><span data-stu-id="0d46f-291">public str getAsciiData()</span></span>                                             |                                               |
| <span data-ttu-id="0d46f-292">public container getData()</span><span class="sxs-lookup"><span data-stu-id="0d46f-292">public container getData()</span></span>                                            |                                               |
| <span data-ttu-id="0d46f-293">public str getStrData()</span><span class="sxs-lookup"><span data-stu-id="0d46f-293">public str getStrData()</span></span>                                               |                                               |
| <span data-ttu-id="0d46f-294">public COMVariant getVariant()</span><span class="sxs-lookup"><span data-stu-id="0d46f-294">public COMVariant getVariant()</span></span>                                        |                                               |
| <span data-ttu-id="0d46f-295">public boolean loadFile(str filename, \[int offset\], \[int length\])</span><span class="sxs-lookup"><span data-stu-id="0d46f-295">public boolean loadFile(str filename, \[int offset\], \[int length\])</span></span> |                                               |
| <span data-ttu-id="0d46f-296">public boolean saveFile(str filename)</span><span class="sxs-lookup"><span data-stu-id="0d46f-296">public boolean saveFile(str filename)</span></span>                                 |                                               |
| <span data-ttu-id="0d46f-297">public int size()</span><span class="sxs-lookup"><span data-stu-id="0d46f-297">public int size()</span></span>                                                     |                                               |
| <span data-ttu-id="0d46f-298">::public static str dataToString(container data)</span><span class="sxs-lookup"><span data-stu-id="0d46f-298">::public static str dataToString(container data)</span></span>                      |                                               |
| <span data-ttu-id="0d46f-299">::public static container loadFromAscii85(str ascii85EncodedString)</span><span class="sxs-lookup"><span data-stu-id="0d46f-299">::public static container loadFromAscii85(str ascii85EncodedString)</span></span>   |                                               |
| <span data-ttu-id="0d46f-300">::public static container loadFromBase64(str base64EncodedString)</span><span class="sxs-lookup"><span data-stu-id="0d46f-300">::public static container loadFromBase64(str base64EncodedString)</span></span>     |                                               |
| <span data-ttu-id="0d46f-301">::public static container stringToData(str string)</span><span class="sxs-lookup"><span data-stu-id="0d46f-301">::public static container stringToData(str string)</span></span>                    |                                               |
| <span data-ttu-id="0d46f-302">public void setStrData(str data)</span><span class="sxs-lookup"><span data-stu-id="0d46f-302">public void setStrData(str data)</span></span>                                      |                                               |
| <span data-ttu-id="0d46f-303">public void setVariant(COMVariant data)</span><span class="sxs-lookup"><span data-stu-id="0d46f-303">public void setVariant(COMVariant data)</span></span>                               |                                               |
| <span data-ttu-id="0d46f-304">public void appendData(BinData binData)</span><span class="sxs-lookup"><span data-stu-id="0d46f-304">public void appendData(BinData binData)</span></span>                               |                                               |
| <span data-ttu-id="0d46f-305">public void new()</span><span class="sxs-lookup"><span data-stu-id="0d46f-305">public void new()</span></span>                                                     | <span data-ttu-id="0d46f-306">BinData クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="0d46f-306">Initializes an instance of the BinData class.</span></span> |
| <span data-ttu-id="0d46f-307">public void setBinaryData(Binary binary)</span><span class="sxs-lookup"><span data-stu-id="0d46f-307">public void setBinaryData(Binary binary)</span></span>                              |                                               |
| <span data-ttu-id="0d46f-308">public void setAsciiData(str data, \[int codePage\])</span><span class="sxs-lookup"><span data-stu-id="0d46f-308">public void setAsciiData(str data, \[int codePage\])</span></span>                  |                                               |
| <span data-ttu-id="0d46f-309">public void setData(container data)</span><span class="sxs-lookup"><span data-stu-id="0d46f-309">public void setData(container data)</span></span>                                   |                                               |
| <span data-ttu-id="0d46f-310">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="0d46f-310">public void finalize()</span></span>                                                |                                               |

### <a name="method-appendtofile"></a><span data-ttu-id="0d46f-311">メソッド appendToFile</span><span class="sxs-lookup"><span data-stu-id="0d46f-311">Method appendToFile</span></span>

    public boolean appendToFile(str filename)

#### <a name="parameters"></a><span data-ttu-id="0d46f-312">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-312">Parameters</span></span>

<span data-ttu-id="0d46f-313">filename</span><span class="sxs-lookup"><span data-stu-id="0d46f-313">filename</span></span>  

#### <a name="return-value"></a><span data-ttu-id="0d46f-314">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-314">Return Value</span></span>

### <a name="method-ascii85encode"></a><span data-ttu-id="0d46f-315">メソッド ascii85Encode</span><span class="sxs-lookup"><span data-stu-id="0d46f-315">Method ascii85Encode</span></span>

    public str ascii85Encode()

#### <a name="return-value"></a><span data-ttu-id="0d46f-316">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-316">Return Value</span></span>

### <a name="method-base64encode"></a><span data-ttu-id="0d46f-317">メソッド base64Encode</span><span class="sxs-lookup"><span data-stu-id="0d46f-317">Method base64Encode</span></span>

    public str base64Encode()

#### <a name="return-value"></a><span data-ttu-id="0d46f-318">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-318">Return Value</span></span>

### <a name="method-compresslz77"></a><span data-ttu-id="0d46f-319">メソッド compressLZ77</span><span class="sxs-lookup"><span data-stu-id="0d46f-319">Method compressLZ77</span></span>

    public int compressLZ77(int windowBits)

#### <a name="parameters"></a><span data-ttu-id="0d46f-320">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-320">Parameters</span></span>

<span data-ttu-id="0d46f-321">windowBits</span><span class="sxs-lookup"><span data-stu-id="0d46f-321">windowBits</span></span>  

#### <a name="return-value"></a><span data-ttu-id="0d46f-322">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-322">Return Value</span></span>

### <a name="method-copydata"></a><span data-ttu-id="0d46f-323">メソッド copyData</span><span class="sxs-lookup"><span data-stu-id="0d46f-323">Method copyData</span></span>

    public boolean copyData(BinData data, [int offset], [int length])

#### <a name="parameters"></a><span data-ttu-id="0d46f-324">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-324">Parameters</span></span>

<span data-ttu-id="0d46f-325">データ</span><span class="sxs-lookup"><span data-stu-id="0d46f-325">data</span></span>  

<!-- -->

<span data-ttu-id="0d46f-326">相殺</span><span class="sxs-lookup"><span data-stu-id="0d46f-326">offset</span></span>  

<!-- -->

<span data-ttu-id="0d46f-327">length</span><span class="sxs-lookup"><span data-stu-id="0d46f-327">length</span></span>  

#### <a name="return-value"></a><span data-ttu-id="0d46f-328">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-328">Return Value</span></span>

### <a name="method-decompresslz77"></a><span data-ttu-id="0d46f-329">メソッド decompressLZ77</span><span class="sxs-lookup"><span data-stu-id="0d46f-329">Method decompressLZ77</span></span>

    public int decompressLZ77()

#### <a name="return-value"></a><span data-ttu-id="0d46f-330">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-330">Return Value</span></span>

### <a name="method-getasciidata"></a><span data-ttu-id="0d46f-331">メソッド getAsciiData</span><span class="sxs-lookup"><span data-stu-id="0d46f-331">Method getAsciiData</span></span>

    public str getAsciiData()

#### <a name="return-value"></a><span data-ttu-id="0d46f-332">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-332">Return Value</span></span>

### <a name="method-getdata"></a><span data-ttu-id="0d46f-333">メソッド getData</span><span class="sxs-lookup"><span data-stu-id="0d46f-333">Method getData</span></span>

    public container getData()

#### <a name="return-value"></a><span data-ttu-id="0d46f-334">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-334">Return Value</span></span>

### <a name="method-getstrdata"></a><span data-ttu-id="0d46f-335">メソッド getStrData</span><span class="sxs-lookup"><span data-stu-id="0d46f-335">Method getStrData</span></span>

    public str getStrData()

#### <a name="return-value"></a><span data-ttu-id="0d46f-336">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-336">Return Value</span></span>

### <a name="method-getvariant"></a><span data-ttu-id="0d46f-337">メソッド getVariant</span><span class="sxs-lookup"><span data-stu-id="0d46f-337">Method getVariant</span></span>

    public COMVariant getVariant()

#### <a name="return-value"></a><span data-ttu-id="0d46f-338">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-338">Return Value</span></span>

### <a name="method-loadfile"></a><span data-ttu-id="0d46f-339">メソッド loadFile</span><span class="sxs-lookup"><span data-stu-id="0d46f-339">Method loadFile</span></span>

    public boolean loadFile(str filename, [int offset], [int length])

#### <a name="parameters"></a><span data-ttu-id="0d46f-340">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-340">Parameters</span></span>

<span data-ttu-id="0d46f-341">filename</span><span class="sxs-lookup"><span data-stu-id="0d46f-341">filename</span></span>  

<!-- -->

<span data-ttu-id="0d46f-342">相殺</span><span class="sxs-lookup"><span data-stu-id="0d46f-342">offset</span></span>  

<!-- -->

<span data-ttu-id="0d46f-343">length</span><span class="sxs-lookup"><span data-stu-id="0d46f-343">length</span></span>  

#### <a name="return-value"></a><span data-ttu-id="0d46f-344">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-344">Return Value</span></span>

#### <a name="remarks"></a><span data-ttu-id="0d46f-345">備考</span><span class="sxs-lookup"><span data-stu-id="0d46f-345">Remarks</span></span>

<span data-ttu-id="0d46f-346">攻撃者が loadFile メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="0d46f-346">If an attacker can control input to the loadFile method, a security risk exists.</span></span> <span data-ttu-id="0d46f-347">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="0d46f-347">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="0d46f-348">サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="0d46f-348">Calls to this method on the server require permission.</span></span> <span data-ttu-id="0d46f-349">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0d46f-349">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

### <a name="method-savefile"></a><span data-ttu-id="0d46f-350">メソッド saveFile</span><span class="sxs-lookup"><span data-stu-id="0d46f-350">Method saveFile</span></span>

    public boolean saveFile(str filename)

#### <a name="parameters"></a><span data-ttu-id="0d46f-351">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-351">Parameters</span></span>

<span data-ttu-id="0d46f-352">filename</span><span class="sxs-lookup"><span data-stu-id="0d46f-352">filename</span></span>  

#### <a name="return-value"></a><span data-ttu-id="0d46f-353">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-353">Return Value</span></span>

#### <a name="remarks"></a><span data-ttu-id="0d46f-354">備考</span><span class="sxs-lookup"><span data-stu-id="0d46f-354">Remarks</span></span>

<span data-ttu-id="0d46f-355">攻撃者が saveFile メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="0d46f-355">If an attacker can control input to the saveFile method, a security risk exists.</span></span> <span data-ttu-id="0d46f-356">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="0d46f-356">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="0d46f-357">サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="0d46f-357">Calls to this method on the server require permission.</span></span> <span data-ttu-id="0d46f-358">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0d46f-358">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

### <a name="method-size"></a><span data-ttu-id="0d46f-359">メソッド size</span><span class="sxs-lookup"><span data-stu-id="0d46f-359">Method size</span></span>

    public int size()

#### <a name="return-value"></a><span data-ttu-id="0d46f-360">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-360">Return Value</span></span>

### <a name="method-datatostring"></a><span data-ttu-id="0d46f-361">メソッド dataToString</span><span class="sxs-lookup"><span data-stu-id="0d46f-361">Method dataToString</span></span>

    public static str dataToString(container data)

#### <a name="parameters"></a><span data-ttu-id="0d46f-362">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-362">Parameters</span></span>

<span data-ttu-id="0d46f-363">データ</span><span class="sxs-lookup"><span data-stu-id="0d46f-363">data</span></span>  

#### <a name="return-value"></a><span data-ttu-id="0d46f-364">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-364">Return Value</span></span>

### <a name="method-loadfromascii85"></a><span data-ttu-id="0d46f-365">メソッド loadFromAscii85</span><span class="sxs-lookup"><span data-stu-id="0d46f-365">Method loadFromAscii85</span></span>

    public static container loadFromAscii85(str ascii85EncodedString)

#### <a name="parameters"></a><span data-ttu-id="0d46f-366">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-366">Parameters</span></span>

<span data-ttu-id="0d46f-367">ascii85EncodedString</span><span class="sxs-lookup"><span data-stu-id="0d46f-367">ascii85EncodedString</span></span>  

#### <a name="return-value"></a><span data-ttu-id="0d46f-368">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-368">Return Value</span></span>

### <a name="method-loadfrombase64"></a><span data-ttu-id="0d46f-369">メソッド loadFromBase64</span><span class="sxs-lookup"><span data-stu-id="0d46f-369">Method loadFromBase64</span></span>

    public static container loadFromBase64(str base64EncodedString)

#### <a name="parameters"></a><span data-ttu-id="0d46f-370">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-370">Parameters</span></span>

<span data-ttu-id="0d46f-371">base64EncodedString</span><span class="sxs-lookup"><span data-stu-id="0d46f-371">base64EncodedString</span></span>  

#### <a name="return-value"></a><span data-ttu-id="0d46f-372">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-372">Return Value</span></span>

### <a name="method-stringtodata"></a><span data-ttu-id="0d46f-373">メソッド stringToData</span><span class="sxs-lookup"><span data-stu-id="0d46f-373">Method stringToData</span></span>

    public static container stringToData(str string)

#### <a name="parameters"></a><span data-ttu-id="0d46f-374">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-374">Parameters</span></span>

<span data-ttu-id="0d46f-375">string</span><span class="sxs-lookup"><span data-stu-id="0d46f-375">string</span></span>  

#### <a name="return-value"></a><span data-ttu-id="0d46f-376">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d46f-376">Return Value</span></span>

### <a name="method-setstrdata"></a><span data-ttu-id="0d46f-377">メソッド setStrData</span><span class="sxs-lookup"><span data-stu-id="0d46f-377">Method setStrData</span></span>

    public void setStrData(str data)

#### <a name="parameters"></a><span data-ttu-id="0d46f-378">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-378">Parameters</span></span>

<span data-ttu-id="0d46f-379">データ</span><span class="sxs-lookup"><span data-stu-id="0d46f-379">data</span></span>  

### <a name="method-setvariant"></a><span data-ttu-id="0d46f-380">メソッド setVariant</span><span class="sxs-lookup"><span data-stu-id="0d46f-380">Method setVariant</span></span>

    public void setVariant(COMVariant data)

#### <a name="parameters"></a><span data-ttu-id="0d46f-381">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-381">Parameters</span></span>

<span data-ttu-id="0d46f-382">データ</span><span class="sxs-lookup"><span data-stu-id="0d46f-382">data</span></span>  

### <a name="method-appenddata"></a><span data-ttu-id="0d46f-383">メソッド appendData</span><span class="sxs-lookup"><span data-stu-id="0d46f-383">Method appendData</span></span>

    public void appendData(BinData binData)

#### <a name="parameters"></a><span data-ttu-id="0d46f-384">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-384">Parameters</span></span>

<span data-ttu-id="0d46f-385">binData</span><span class="sxs-lookup"><span data-stu-id="0d46f-385">binData</span></span>  

### <a name="method-new"></a><span data-ttu-id="0d46f-386">メソッド new</span><span class="sxs-lookup"><span data-stu-id="0d46f-386">Method new</span></span>

<span data-ttu-id="0d46f-387">BinData クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="0d46f-387">Initializes an instance of the BinData class.</span></span>

    public void new()

### <a name="method-setbinarydata"></a><span data-ttu-id="0d46f-388">メソッド setBinaryData</span><span class="sxs-lookup"><span data-stu-id="0d46f-388">Method setBinaryData</span></span>

    public void setBinaryData(Binary binary)

#### <a name="parameters"></a><span data-ttu-id="0d46f-389">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-389">Parameters</span></span>

<span data-ttu-id="0d46f-390">binary</span><span class="sxs-lookup"><span data-stu-id="0d46f-390">binary</span></span>  

### <a name="method-setasciidata"></a><span data-ttu-id="0d46f-391">メソッド setAsciiData</span><span class="sxs-lookup"><span data-stu-id="0d46f-391">Method setAsciiData</span></span>

    public void setAsciiData(str data, [int codePage])

#### <a name="parameters"></a><span data-ttu-id="0d46f-392">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-392">Parameters</span></span>

<span data-ttu-id="0d46f-393">データ</span><span class="sxs-lookup"><span data-stu-id="0d46f-393">data</span></span>  

<!-- -->

<span data-ttu-id="0d46f-394">codePage</span><span class="sxs-lookup"><span data-stu-id="0d46f-394">codePage</span></span>  

### <a name="method-setdata"></a><span data-ttu-id="0d46f-395">メソッド setData</span><span class="sxs-lookup"><span data-stu-id="0d46f-395">Method setData</span></span>

    public void setData(container data)

#### <a name="parameters"></a><span data-ttu-id="0d46f-396">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d46f-396">Parameters</span></span>

<span data-ttu-id="0d46f-397">データ</span><span class="sxs-lookup"><span data-stu-id="0d46f-397">data</span></span>  

### <a name="method-finalize"></a><span data-ttu-id="0d46f-398">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="0d46f-398">Method finalize</span></span>

    public void finalize()




