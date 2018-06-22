---
title: "H クラス"
description: "文字 H で始まるシステム API クラス。"
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
ms.custom: 52591
ms.assetid: c27e2044-28c2-432a-b15f-a41d26a83a52
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1fc31e89f2f626b79484a802645dc58f07011959
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="h-classes"></a><span data-ttu-id="49c97-103">H クラス</span><span class="sxs-lookup"><span data-stu-id="49c97-103">H Classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49c97-104">文字 H で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="49c97-104">System API classes that start with the letter H.</span></span>

<a name="class-heapcheck"></a><span data-ttu-id="49c97-105">クラス HeapCheck</span><span class="sxs-lookup"><span data-stu-id="49c97-105">Class HeapCheck</span></span>
---------------

    class HeapCheck extends Object

### <a name="remarks"></a><span data-ttu-id="49c97-106">備考</span><span class="sxs-lookup"><span data-stu-id="49c97-106">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="49c97-107">例</span><span class="sxs-lookup"><span data-stu-id="49c97-107">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="49c97-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="49c97-108">Methods</span></span>

| <span data-ttu-id="49c97-109">方法</span><span class="sxs-lookup"><span data-stu-id="49c97-109">Method</span></span>                                                                                      | <span data-ttu-id="49c97-110">説明</span><span class="sxs-lookup"><span data-stu-id="49c97-110">Description</span></span>                                     |
|---------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="49c97-111">public int accessCnt()</span><span class="sxs-lookup"><span data-stu-id="49c97-111">public int accessCnt()</span></span>                                                                      |                                                 |
| <span data-ttu-id="49c97-112">public int addRefCnt()</span><span class="sxs-lookup"><span data-stu-id="49c97-112">public int addRefCnt()</span></span>                                                                      |                                                 |
| <span data-ttu-id="49c97-113">public Int64 blocksAllocated(\[int pool\])</span><span class="sxs-lookup"><span data-stu-id="49c97-113">public Int64 blocksAllocated(\[int pool\])</span></span>                                                  |                                                 |
| <span data-ttu-id="49c97-114">public int breakCount(\[int count\])</span><span class="sxs-lookup"><span data-stu-id="49c97-114">public int breakCount(\[int count\])</span></span>                                                        |                                                 |
| <span data-ttu-id="49c97-115">public Int64 bytesAllocated(\[int pool\])</span><span class="sxs-lookup"><span data-stu-id="49c97-115">public Int64 bytesAllocated(\[int pool\])</span></span>                                                   |                                                 |
| <span data-ttu-id="49c97-116">public Int64 ceiling(int pool, \[int ceiling\])</span><span class="sxs-lookup"><span data-stu-id="49c97-116">public Int64 ceiling(int pool, \[int ceiling\])</span></span>                                             |                                                 |
| <span data-ttu-id="49c97-117">public int context(\[int context\])</span><span class="sxs-lookup"><span data-stu-id="49c97-117">public int context(\[int context\])</span></span>                                                         |                                                 |
| <span data-ttu-id="49c97-118">public int count(\[int count\])</span><span class="sxs-lookup"><span data-stu-id="49c97-118">public int count(\[int count\])</span></span>                                                             |                                                 |
| <span data-ttu-id="49c97-119">public int countObjects(int classId)</span><span class="sxs-lookup"><span data-stu-id="49c97-119">public int countObjects(int classId)</span></span>                                                        |                                                 |
| <span data-ttu-id="49c97-120">public container createAContainer()</span><span class="sxs-lookup"><span data-stu-id="49c97-120">public container createAContainer()</span></span>                                                         |                                                 |
| <span data-ttu-id="49c97-121">public int csCallCnt()</span><span class="sxs-lookup"><span data-stu-id="49c97-121">public int csCallCnt()</span></span>                                                                      |                                                 |
| <span data-ttu-id="49c97-122">public int csSweepCnt()</span><span class="sxs-lookup"><span data-stu-id="49c97-122">public int csSweepCnt()</span></span>                                                                     |                                                 |
| <span data-ttu-id="49c97-123">public container dataByContext(\[int poolNo\], \[int context\])</span><span class="sxs-lookup"><span data-stu-id="49c97-123">public container dataByContext(\[int poolNo\], \[int context\])</span></span>                             |                                                 |
| <span data-ttu-id="49c97-124">public int dumpCursors()</span><span class="sxs-lookup"><span data-stu-id="49c97-124">public int dumpCursors()</span></span>                                                                    |                                                 |
| <span data-ttu-id="49c97-125">public int dumpObjects()</span><span class="sxs-lookup"><span data-stu-id="49c97-125">public int dumpObjects()</span></span>                                                                    |                                                 |
| <span data-ttu-id="49c97-126">public int filename(\[str filename\])</span><span class="sxs-lookup"><span data-stu-id="49c97-126">public int filename(\[str filename\])</span></span>                                                       |                                                 |
| <span data-ttu-id="49c97-127">public int fixedBlockSize(int pool, \[int blockSize\])</span><span class="sxs-lookup"><span data-stu-id="49c97-127">public int fixedBlockSize(int pool, \[int blockSize\])</span></span>                                      |                                                 |
| <span data-ttu-id="49c97-128">public int floor(int pool, \[int floor\])</span><span class="sxs-lookup"><span data-stu-id="49c97-128">public int floor(int pool, \[int floor\])</span></span>                                                   |                                                 |
| <span data-ttu-id="49c97-129">public int freeRefCnt()</span><span class="sxs-lookup"><span data-stu-id="49c97-129">public int freeRefCnt()</span></span>                                                                     |                                                 |
| <span data-ttu-id="49c97-130">public int getRuntimeBugcheckFlags()</span><span class="sxs-lookup"><span data-stu-id="49c97-130">public int getRuntimeBugcheckFlags()</span></span>                                                        |                                                 |
| <span data-ttu-id="49c97-131">public Common getUnfreedCursor()</span><span class="sxs-lookup"><span data-stu-id="49c97-131">public Common getUnfreedCursor()</span></span>                                                            |                                                 |
| <span data-ttu-id="49c97-132">public Common getUnfreedObject()</span><span class="sxs-lookup"><span data-stu-id="49c97-132">public Common getUnfreedObject()</span></span>                                                            |                                                 |
| <span data-ttu-id="49c97-133">public boolean include(int objectNo, \[boolean include\])</span><span class="sxs-lookup"><span data-stu-id="49c97-133">public boolean include(int objectNo, \[boolean include\])</span></span>                                   |                                                 |
| <span data-ttu-id="49c97-134">public boolean moreUnfreedCursors()</span><span class="sxs-lookup"><span data-stu-id="49c97-134">public boolean moreUnfreedCursors()</span></span>                                                         |                                                 |
| <span data-ttu-id="49c97-135">public boolean moreUnfreedObjects()</span><span class="sxs-lookup"><span data-stu-id="49c97-135">public boolean moreUnfreedObjects()</span></span>                                                         |                                                 |
| <span data-ttu-id="49c97-136">public int objectContext(int objNo, \[int context\])</span><span class="sxs-lookup"><span data-stu-id="49c97-136">public int objectContext(int objNo, \[int context\])</span></span>                                        |                                                 |
| <span data-ttu-id="49c97-137">public int pageSize(int pool, \[int pageSize\])</span><span class="sxs-lookup"><span data-stu-id="49c97-137">public int pageSize(int pool, \[int pageSize\])</span></span>                                             |                                                 |
| <span data-ttu-id="49c97-138">public int poolCount()</span><span class="sxs-lookup"><span data-stu-id="49c97-138">public int poolCount()</span></span>                                                                      |                                                 |
| <span data-ttu-id="49c97-139">public str poolName(int poolNo)</span><span class="sxs-lookup"><span data-stu-id="49c97-139">public str poolName(int poolNo)</span></span>                                                             |                                                 |
| <span data-ttu-id="49c97-140">public int smallBlockSize(int pool, \[int blockSize\])</span><span class="sxs-lookup"><span data-stu-id="49c97-140">public int smallBlockSize(int pool, \[int blockSize\])</span></span>                                      |                                                 |
| <span data-ttu-id="49c97-141">public int sweepCnt()</span><span class="sxs-lookup"><span data-stu-id="49c97-141">public int sweepCnt()</span></span>                                                                       |                                                 |
| <span data-ttu-id="49c97-142">public int testBlocks(\[int arg1\])</span><span class="sxs-lookup"><span data-stu-id="49c97-142">public int testBlocks(\[int arg1\])</span></span>                                                         |                                                 |
| <span data-ttu-id="49c97-143">public str unfreedObjectClass()</span><span class="sxs-lookup"><span data-stu-id="49c97-143">public str unfreedObjectClass()</span></span>                                                             |                                                 |
| <span data-ttu-id="49c97-144">public boolean unfreedObjectClient()</span><span class="sxs-lookup"><span data-stu-id="49c97-144">public boolean unfreedObjectClient()</span></span>                                                        |                                                 |
| <span data-ttu-id="49c97-145">public boolean unfreedObjectFinalized()</span><span class="sxs-lookup"><span data-stu-id="49c97-145">public boolean unfreedObjectFinalized()</span></span>                                                     |                                                 |
| <span data-ttu-id="49c97-146">public int unfreedObjectHandle()</span><span class="sxs-lookup"><span data-stu-id="49c97-146">public int unfreedObjectHandle()</span></span>                                                            |                                                 |
| <span data-ttu-id="49c97-147">public int unfreedObjectIdent()</span><span class="sxs-lookup"><span data-stu-id="49c97-147">public int unfreedObjectIdent()</span></span>                                                             |                                                 |
| <span data-ttu-id="49c97-148">public int unfreedObjectUseCount()</span><span class="sxs-lookup"><span data-stu-id="49c97-148">public int unfreedObjectUseCount()</span></span>                                                          |                                                 |
| <span data-ttu-id="49c97-149">public str version()</span><span class="sxs-lookup"><span data-stu-id="49c97-149">public str version()</span></span>                                                                        |                                                 |
| <span data-ttu-id="49c97-150">public void checkHeap(str Description, \[int context\], \[int pool\], \[boolean detailed\])</span><span class="sxs-lookup"><span data-stu-id="49c97-150">public void checkHeap(str Description, \[int context\], \[int pool\], \[boolean detailed\])</span></span> |                                                 |
| <span data-ttu-id="49c97-151">public void shrinkPool(\[int poolNo\])</span><span class="sxs-lookup"><span data-stu-id="49c97-151">public void shrinkPool(\[int poolNo\])</span></span>                                                      |                                                 |
| <span data-ttu-id="49c97-152">public void postCompactingMessage()</span><span class="sxs-lookup"><span data-stu-id="49c97-152">public void postCompactingMessage()</span></span>                                                         |                                                 |
| <span data-ttu-id="49c97-153">public void checkHeapDif(str Description, \[int context\], \[int pool\])</span><span class="sxs-lookup"><span data-stu-id="49c97-153">public void checkHeapDif(str Description, \[int context\], \[int pool\])</span></span>                    |                                                 |
| <span data-ttu-id="49c97-154">public void clearHeapContext()</span><span class="sxs-lookup"><span data-stu-id="49c97-154">public void clearHeapContext()</span></span>                                                              |                                                 |
| <span data-ttu-id="49c97-155">public void writeString(str text)</span><span class="sxs-lookup"><span data-stu-id="49c97-155">public void writeString(str text)</span></span>                                                           |                                                 |
| <span data-ttu-id="49c97-156">public void firstUnfreedCursor()</span><span class="sxs-lookup"><span data-stu-id="49c97-156">public void firstUnfreedCursor()</span></span>                                                            |                                                 |
| <span data-ttu-id="49c97-157">public void dumpDGMLGraph()</span><span class="sxs-lookup"><span data-stu-id="49c97-157">public void dumpDGMLGraph()</span></span>                                                                 |                                                 |
| <span data-ttu-id="49c97-158">public void firstUnfreedObject()</span><span class="sxs-lookup"><span data-stu-id="49c97-158">public void firstUnfreedObject()</span></span>                                                            |                                                 |
| <span data-ttu-id="49c97-159">public void setHeapContext(str description)</span><span class="sxs-lookup"><span data-stu-id="49c97-159">public void setHeapContext(str description)</span></span>                                                 |                                                 |
| <span data-ttu-id="49c97-160">public void new(\[str Filename\])</span><span class="sxs-lookup"><span data-stu-id="49c97-160">public void new(\[str Filename\])</span></span>                                                           | <span data-ttu-id="49c97-161">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="49c97-161">Initializes a new instance of the Object class.</span></span> |
| <span data-ttu-id="49c97-162">public void nextUnfreedObject()</span><span class="sxs-lookup"><span data-stu-id="49c97-162">public void nextUnfreedObject()</span></span>                                                             |                                                 |
| <span data-ttu-id="49c97-163">public void checkHeapStop()</span><span class="sxs-lookup"><span data-stu-id="49c97-163">public void checkHeapStop()</span></span>                                                                 |                                                 |
| <span data-ttu-id="49c97-164">public void nextUnfreedCursor()</span><span class="sxs-lookup"><span data-stu-id="49c97-164">public void nextUnfreedCursor()</span></span>                                                             |                                                 |
| <span data-ttu-id="49c97-165">public void setRuntimeBugcheckFlags(int flags)</span><span class="sxs-lookup"><span data-stu-id="49c97-165">public void setRuntimeBugcheckFlags(int flags)</span></span>                                              |                                                 |
| <span data-ttu-id="49c97-166">public void checkHeapStart()</span><span class="sxs-lookup"><span data-stu-id="49c97-166">public void checkHeapStart()</span></span>                                                                |                                                 |

### <a name="method-accesscnt"></a><span data-ttu-id="49c97-167">メソッド accessCnt</span><span class="sxs-lookup"><span data-stu-id="49c97-167">Method accessCnt</span></span>

    public int accessCnt()

#### <a name="return-value"></a><span data-ttu-id="49c97-168">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-168">Return Value</span></span>

### <a name="method-addrefcnt"></a><span data-ttu-id="49c97-169">メソッド addRefCnt</span><span class="sxs-lookup"><span data-stu-id="49c97-169">Method addRefCnt</span></span>

    public int addRefCnt()

#### <a name="return-value"></a><span data-ttu-id="49c97-170">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-170">Return Value</span></span>

### <a name="method-blocksallocated"></a><span data-ttu-id="49c97-171">メソッド blocksAllocated</span><span class="sxs-lookup"><span data-stu-id="49c97-171">Method blocksAllocated</span></span>

    public Int64 blocksAllocated([int pool])

#### <a name="parameters"></a><span data-ttu-id="49c97-172">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-172">Parameters</span></span>

<span data-ttu-id="49c97-173">管理グループ</span><span class="sxs-lookup"><span data-stu-id="49c97-173">pool</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-174">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-174">Return Value</span></span>

### <a name="method-breakcount"></a><span data-ttu-id="49c97-175">メソッド breakCount</span><span class="sxs-lookup"><span data-stu-id="49c97-175">Method breakCount</span></span>

    public int breakCount([int count])

#### <a name="parameters"></a><span data-ttu-id="49c97-176">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-176">Parameters</span></span>

<span data-ttu-id="49c97-177">カウント</span><span class="sxs-lookup"><span data-stu-id="49c97-177">count</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-178">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-178">Return Value</span></span>

### <a name="method-bytesallocated"></a><span data-ttu-id="49c97-179">メソッド bytesAllocated</span><span class="sxs-lookup"><span data-stu-id="49c97-179">Method bytesAllocated</span></span>

    public Int64 bytesAllocated([int pool])

#### <a name="parameters"></a><span data-ttu-id="49c97-180">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-180">Parameters</span></span>

<span data-ttu-id="49c97-181">管理グループ</span><span class="sxs-lookup"><span data-stu-id="49c97-181">pool</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-182">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-182">Return Value</span></span>

### <a name="method-ceiling"></a><span data-ttu-id="49c97-183">メソッド ceiling</span><span class="sxs-lookup"><span data-stu-id="49c97-183">Method ceiling</span></span>

    public Int64 ceiling(int pool, [int ceiling])

#### <a name="parameters"></a><span data-ttu-id="49c97-184">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-184">Parameters</span></span>

<span data-ttu-id="49c97-185">管理グループ</span><span class="sxs-lookup"><span data-stu-id="49c97-185">pool</span></span>  

<!-- -->

<span data-ttu-id="49c97-186">ceiling</span><span class="sxs-lookup"><span data-stu-id="49c97-186">ceiling</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-187">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-187">Return Value</span></span>

### <a name="method-context"></a><span data-ttu-id="49c97-188">メソッド context</span><span class="sxs-lookup"><span data-stu-id="49c97-188">Method context</span></span>

    public int context([int context])

#### <a name="parameters"></a><span data-ttu-id="49c97-189">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-189">Parameters</span></span>

<span data-ttu-id="49c97-190">context</span><span class="sxs-lookup"><span data-stu-id="49c97-190">context</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-191">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-191">Return Value</span></span>

### <a name="method-count"></a><span data-ttu-id="49c97-192">メソッド count</span><span class="sxs-lookup"><span data-stu-id="49c97-192">Method count</span></span>

    public int count([int count])

#### <a name="parameters"></a><span data-ttu-id="49c97-193">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-193">Parameters</span></span>

<span data-ttu-id="49c97-194">カウント</span><span class="sxs-lookup"><span data-stu-id="49c97-194">count</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-195">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-195">Return Value</span></span>

### <a name="method-countobjects"></a><span data-ttu-id="49c97-196">メソッド countObjects</span><span class="sxs-lookup"><span data-stu-id="49c97-196">Method countObjects</span></span>

    public int countObjects(int classId)

#### <a name="parameters"></a><span data-ttu-id="49c97-197">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-197">Parameters</span></span>

<span data-ttu-id="49c97-198">classId</span><span class="sxs-lookup"><span data-stu-id="49c97-198">classId</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-199">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-199">Return Value</span></span>

### <a name="method-createacontainer"></a><span data-ttu-id="49c97-200">メソッド createAContainer</span><span class="sxs-lookup"><span data-stu-id="49c97-200">Method createAContainer</span></span>

    public container createAContainer()

#### <a name="return-value"></a><span data-ttu-id="49c97-201">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-201">Return Value</span></span>

### <a name="method-cscallcnt"></a><span data-ttu-id="49c97-202">メソッド csCallCnt</span><span class="sxs-lookup"><span data-stu-id="49c97-202">Method csCallCnt</span></span>

    public int csCallCnt()

#### <a name="return-value"></a><span data-ttu-id="49c97-203">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-203">Return Value</span></span>

### <a name="method-cssweepcnt"></a><span data-ttu-id="49c97-204">メソッド csSweepCnt</span><span class="sxs-lookup"><span data-stu-id="49c97-204">Method csSweepCnt</span></span>

    public int csSweepCnt()

#### <a name="return-value"></a><span data-ttu-id="49c97-205">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-205">Return Value</span></span>

### <a name="method-databycontext"></a><span data-ttu-id="49c97-206">メソッド dataByContext</span><span class="sxs-lookup"><span data-stu-id="49c97-206">Method dataByContext</span></span>

    public container dataByContext([int poolNo], [int context])

#### <a name="parameters"></a><span data-ttu-id="49c97-207">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-207">Parameters</span></span>

<span data-ttu-id="49c97-208">poolNo</span><span class="sxs-lookup"><span data-stu-id="49c97-208">poolNo</span></span>  

<!-- -->

<span data-ttu-id="49c97-209">context</span><span class="sxs-lookup"><span data-stu-id="49c97-209">context</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-210">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-210">Return Value</span></span>

### <a name="method-dumpcursors"></a><span data-ttu-id="49c97-211">メソッド dumpCursors</span><span class="sxs-lookup"><span data-stu-id="49c97-211">Method dumpCursors</span></span>

    public int dumpCursors()

#### <a name="return-value"></a><span data-ttu-id="49c97-212">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-212">Return Value</span></span>

### <a name="method-dumpobjects"></a><span data-ttu-id="49c97-213">メソッド dumpObjects</span><span class="sxs-lookup"><span data-stu-id="49c97-213">Method dumpObjects</span></span>

    public int dumpObjects()

#### <a name="return-value"></a><span data-ttu-id="49c97-214">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-214">Return Value</span></span>

### <a name="method-filename"></a><span data-ttu-id="49c97-215">メソッド filename</span><span class="sxs-lookup"><span data-stu-id="49c97-215">Method filename</span></span>

    public int filename([str filename])

#### <a name="parameters"></a><span data-ttu-id="49c97-216">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-216">Parameters</span></span>

<span data-ttu-id="49c97-217">filename</span><span class="sxs-lookup"><span data-stu-id="49c97-217">filename</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-218">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-218">Return Value</span></span>

### <a name="method-fixedblocksize"></a><span data-ttu-id="49c97-219">メソッド fixedBlockSize</span><span class="sxs-lookup"><span data-stu-id="49c97-219">Method fixedBlockSize</span></span>

    public int fixedBlockSize(int pool, [int blockSize])

#### <a name="parameters"></a><span data-ttu-id="49c97-220">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-220">Parameters</span></span>

<span data-ttu-id="49c97-221">管理グループ</span><span class="sxs-lookup"><span data-stu-id="49c97-221">pool</span></span>  

<!-- -->

<span data-ttu-id="49c97-222">blockSize</span><span class="sxs-lookup"><span data-stu-id="49c97-222">blockSize</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-223">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-223">Return Value</span></span>

### <a name="method-floor"></a><span data-ttu-id="49c97-224">メソッド floor</span><span class="sxs-lookup"><span data-stu-id="49c97-224">Method floor</span></span>

    public int floor(int pool, [int floor])

#### <a name="parameters"></a><span data-ttu-id="49c97-225">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-225">Parameters</span></span>

<span data-ttu-id="49c97-226">管理グループ</span><span class="sxs-lookup"><span data-stu-id="49c97-226">pool</span></span>  

<!-- -->

<span data-ttu-id="49c97-227">floor</span><span class="sxs-lookup"><span data-stu-id="49c97-227">floor</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-228">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-228">Return Value</span></span>

### <a name="method-freerefcnt"></a><span data-ttu-id="49c97-229">メソッド freeRefCnt</span><span class="sxs-lookup"><span data-stu-id="49c97-229">Method freeRefCnt</span></span>

    public int freeRefCnt()

#### <a name="return-value"></a><span data-ttu-id="49c97-230">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-230">Return Value</span></span>

### <a name="method-getruntimebugcheckflags"></a><span data-ttu-id="49c97-231">メソッド getRuntimeBugcheckFlags</span><span class="sxs-lookup"><span data-stu-id="49c97-231">Method getRuntimeBugcheckFlags</span></span>

    public int getRuntimeBugcheckFlags()

#### <a name="return-value"></a><span data-ttu-id="49c97-232">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-232">Return Value</span></span>

### <a name="method-getunfreedcursor"></a><span data-ttu-id="49c97-233">メソッド getUnfreedCursor</span><span class="sxs-lookup"><span data-stu-id="49c97-233">Method getUnfreedCursor</span></span>

    public Common getUnfreedCursor()

#### <a name="return-value"></a><span data-ttu-id="49c97-234">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-234">Return Value</span></span>

### <a name="method-getunfreedobject"></a><span data-ttu-id="49c97-235">メソッド getUnfreedObject</span><span class="sxs-lookup"><span data-stu-id="49c97-235">Method getUnfreedObject</span></span>

    public Common getUnfreedObject()

#### <a name="return-value"></a><span data-ttu-id="49c97-236">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-236">Return Value</span></span>

### <a name="method-include"></a><span data-ttu-id="49c97-237">メソッド include</span><span class="sxs-lookup"><span data-stu-id="49c97-237">Method include</span></span>

    public boolean include(int objectNo, [boolean include])

#### <a name="parameters"></a><span data-ttu-id="49c97-238">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-238">Parameters</span></span>

<span data-ttu-id="49c97-239">objectNo</span><span class="sxs-lookup"><span data-stu-id="49c97-239">objectNo</span></span>  

<!-- -->

<span data-ttu-id="49c97-240">include</span><span class="sxs-lookup"><span data-stu-id="49c97-240">include</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-241">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-241">Return Value</span></span>

### <a name="method-moreunfreedcursors"></a><span data-ttu-id="49c97-242">メソッド moreUnfreedCursors</span><span class="sxs-lookup"><span data-stu-id="49c97-242">Method moreUnfreedCursors</span></span>

    public boolean moreUnfreedCursors()

#### <a name="return-value"></a><span data-ttu-id="49c97-243">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-243">Return Value</span></span>

### <a name="method-moreunfreedobjects"></a><span data-ttu-id="49c97-244">メソッド moreUnfreedObjects</span><span class="sxs-lookup"><span data-stu-id="49c97-244">Method moreUnfreedObjects</span></span>

    public boolean moreUnfreedObjects()

#### <a name="return-value"></a><span data-ttu-id="49c97-245">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-245">Return Value</span></span>

### <a name="method-objectcontext"></a><span data-ttu-id="49c97-246">メソッド objectContext</span><span class="sxs-lookup"><span data-stu-id="49c97-246">Method objectContext</span></span>

    public int objectContext(int objNo, [int context])

#### <a name="parameters"></a><span data-ttu-id="49c97-247">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-247">Parameters</span></span>

<span data-ttu-id="49c97-248">objNo</span><span class="sxs-lookup"><span data-stu-id="49c97-248">objNo</span></span>  

<!-- -->

<span data-ttu-id="49c97-249">context</span><span class="sxs-lookup"><span data-stu-id="49c97-249">context</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-250">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-250">Return Value</span></span>

### <a name="method-pagesize"></a><span data-ttu-id="49c97-251">メソッド pageSize</span><span class="sxs-lookup"><span data-stu-id="49c97-251">Method pageSize</span></span>

    public int pageSize(int pool, [int pageSize])

#### <a name="parameters"></a><span data-ttu-id="49c97-252">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-252">Parameters</span></span>

<span data-ttu-id="49c97-253">管理グループ</span><span class="sxs-lookup"><span data-stu-id="49c97-253">pool</span></span>  

<!-- -->

<span data-ttu-id="49c97-254">pageSize</span><span class="sxs-lookup"><span data-stu-id="49c97-254">pageSize</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-255">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-255">Return Value</span></span>

### <a name="method-poolcount"></a><span data-ttu-id="49c97-256">メソッド poolCount</span><span class="sxs-lookup"><span data-stu-id="49c97-256">Method poolCount</span></span>

    public int poolCount()

#### <a name="return-value"></a><span data-ttu-id="49c97-257">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-257">Return Value</span></span>

### <a name="method-poolname"></a><span data-ttu-id="49c97-258">メソッド poolName</span><span class="sxs-lookup"><span data-stu-id="49c97-258">Method poolName</span></span>

    public str poolName(int poolNo)

#### <a name="parameters"></a><span data-ttu-id="49c97-259">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-259">Parameters</span></span>

<span data-ttu-id="49c97-260">poolNo</span><span class="sxs-lookup"><span data-stu-id="49c97-260">poolNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-261">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-261">Return Value</span></span>

### <a name="method-smallblocksize"></a><span data-ttu-id="49c97-262">メソッド smallBlockSize</span><span class="sxs-lookup"><span data-stu-id="49c97-262">Method smallBlockSize</span></span>

    public int smallBlockSize(int pool, [int blockSize])

#### <a name="parameters"></a><span data-ttu-id="49c97-263">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-263">Parameters</span></span>

<span data-ttu-id="49c97-264">管理グループ</span><span class="sxs-lookup"><span data-stu-id="49c97-264">pool</span></span>  

<!-- -->

<span data-ttu-id="49c97-265">blockSize</span><span class="sxs-lookup"><span data-stu-id="49c97-265">blockSize</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-266">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-266">Return Value</span></span>

### <a name="method-sweepcnt"></a><span data-ttu-id="49c97-267">メソッド sweepCnt</span><span class="sxs-lookup"><span data-stu-id="49c97-267">Method sweepCnt</span></span>

    public int sweepCnt()

#### <a name="return-value"></a><span data-ttu-id="49c97-268">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-268">Return Value</span></span>

### <a name="method-testblocks"></a><span data-ttu-id="49c97-269">メソッド testBlocks</span><span class="sxs-lookup"><span data-stu-id="49c97-269">Method testBlocks</span></span>

    public int testBlocks([int arg1])

#### <a name="parameters"></a><span data-ttu-id="49c97-270">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-270">Parameters</span></span>

<span data-ttu-id="49c97-271">arg1</span><span class="sxs-lookup"><span data-stu-id="49c97-271">arg1</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-272">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-272">Return Value</span></span>

### <a name="method-unfreedobjectclass"></a><span data-ttu-id="49c97-273">メソッド unfreedObjectClass</span><span class="sxs-lookup"><span data-stu-id="49c97-273">Method unfreedObjectClass</span></span>

    public str unfreedObjectClass()

#### <a name="return-value"></a><span data-ttu-id="49c97-274">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-274">Return Value</span></span>

### <a name="method-unfreedobjectclient"></a><span data-ttu-id="49c97-275">メソッド unfreedObjectClient</span><span class="sxs-lookup"><span data-stu-id="49c97-275">Method unfreedObjectClient</span></span>

    public boolean unfreedObjectClient()

#### <a name="return-value"></a><span data-ttu-id="49c97-276">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-276">Return Value</span></span>

### <a name="method-unfreedobjectfinalized"></a><span data-ttu-id="49c97-277">メソッド unfreedObjectFinalized</span><span class="sxs-lookup"><span data-stu-id="49c97-277">Method unfreedObjectFinalized</span></span>

    public boolean unfreedObjectFinalized()

#### <a name="return-value"></a><span data-ttu-id="49c97-278">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-278">Return Value</span></span>

### <a name="method-unfreedobjecthandle"></a><span data-ttu-id="49c97-279">メソッド unfreedObjectHandle</span><span class="sxs-lookup"><span data-stu-id="49c97-279">Method unfreedObjectHandle</span></span>

    public int unfreedObjectHandle()

#### <a name="return-value"></a><span data-ttu-id="49c97-280">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-280">Return Value</span></span>

### <a name="method-unfreedobjectident"></a><span data-ttu-id="49c97-281">メソッド unfreedObjectIdent</span><span class="sxs-lookup"><span data-stu-id="49c97-281">Method unfreedObjectIdent</span></span>

    public int unfreedObjectIdent()

#### <a name="return-value"></a><span data-ttu-id="49c97-282">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-282">Return Value</span></span>

### <a name="method-unfreedobjectusecount"></a><span data-ttu-id="49c97-283">メソッド unfreedObjectUseCount</span><span class="sxs-lookup"><span data-stu-id="49c97-283">Method unfreedObjectUseCount</span></span>

    public int unfreedObjectUseCount()

#### <a name="return-value"></a><span data-ttu-id="49c97-284">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-284">Return Value</span></span>

### <a name="method-version"></a><span data-ttu-id="49c97-285">メソッド version</span><span class="sxs-lookup"><span data-stu-id="49c97-285">Method version</span></span>

    public str version()

#### <a name="return-value"></a><span data-ttu-id="49c97-286">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-286">Return Value</span></span>

### <a name="method-checkheap"></a><span data-ttu-id="49c97-287">メソッド checkHeap</span><span class="sxs-lookup"><span data-stu-id="49c97-287">Method checkHeap</span></span>

    public void checkHeap(str Description, [int context], [int pool], [boolean detailed])

#### <a name="parameters"></a><span data-ttu-id="49c97-288">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-288">Parameters</span></span>

<span data-ttu-id="49c97-289">説明</span><span class="sxs-lookup"><span data-stu-id="49c97-289">Description</span></span>  

<!-- -->

<span data-ttu-id="49c97-290">context</span><span class="sxs-lookup"><span data-stu-id="49c97-290">context</span></span>  

<!-- -->

<span data-ttu-id="49c97-291">管理グループ</span><span class="sxs-lookup"><span data-stu-id="49c97-291">pool</span></span>  

<!-- -->

<span data-ttu-id="49c97-292">detailed</span><span class="sxs-lookup"><span data-stu-id="49c97-292">detailed</span></span>  

### <a name="method-shrinkpool"></a><span data-ttu-id="49c97-293">メソッド shrinkPool</span><span class="sxs-lookup"><span data-stu-id="49c97-293">Method shrinkPool</span></span>

    public void shrinkPool([int poolNo])

#### <a name="parameters"></a><span data-ttu-id="49c97-294">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-294">Parameters</span></span>

<span data-ttu-id="49c97-295">poolNo</span><span class="sxs-lookup"><span data-stu-id="49c97-295">poolNo</span></span>  

### <a name="method-postcompactingmessage"></a><span data-ttu-id="49c97-296">メソッド postCompactingMessage</span><span class="sxs-lookup"><span data-stu-id="49c97-296">Method postCompactingMessage</span></span>

    public void postCompactingMessage()

### <a name="method-checkheapdif"></a><span data-ttu-id="49c97-297">メソッド checkHeapDif</span><span class="sxs-lookup"><span data-stu-id="49c97-297">Method checkHeapDif</span></span>

    public void checkHeapDif(str Description, [int context], [int pool])

#### <a name="parameters"></a><span data-ttu-id="49c97-298">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-298">Parameters</span></span>

<span data-ttu-id="49c97-299">説明</span><span class="sxs-lookup"><span data-stu-id="49c97-299">Description</span></span>  

<!-- -->

<span data-ttu-id="49c97-300">context</span><span class="sxs-lookup"><span data-stu-id="49c97-300">context</span></span>  

<!-- -->

<span data-ttu-id="49c97-301">管理グループ</span><span class="sxs-lookup"><span data-stu-id="49c97-301">pool</span></span>  

### <a name="method-clearheapcontext"></a><span data-ttu-id="49c97-302">メソッド clearHeapContext</span><span class="sxs-lookup"><span data-stu-id="49c97-302">Method clearHeapContext</span></span>

    public void clearHeapContext()

### <a name="method-writestring"></a><span data-ttu-id="49c97-303">メソッド writeString</span><span class="sxs-lookup"><span data-stu-id="49c97-303">Method writeString</span></span>

    public void writeString(str text)

#### <a name="parameters"></a><span data-ttu-id="49c97-304">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-304">Parameters</span></span>

<span data-ttu-id="49c97-305">テキスト</span><span class="sxs-lookup"><span data-stu-id="49c97-305">text</span></span>  

### <a name="method-firstunfreedcursor"></a><span data-ttu-id="49c97-306">メソッド firstUnfreedCursor</span><span class="sxs-lookup"><span data-stu-id="49c97-306">Method firstUnfreedCursor</span></span>

    public void firstUnfreedCursor()

### <a name="method-dumpdgmlgraph"></a><span data-ttu-id="49c97-307">メソッド dumpDGMLGraph</span><span class="sxs-lookup"><span data-stu-id="49c97-307">Method dumpDGMLGraph</span></span>

    public void dumpDGMLGraph()

### <a name="method-firstunfreedobject"></a><span data-ttu-id="49c97-308">メソッド firstUnfreedObject</span><span class="sxs-lookup"><span data-stu-id="49c97-308">Method firstUnfreedObject</span></span>

    public void firstUnfreedObject()

### <a name="method-setheapcontext"></a><span data-ttu-id="49c97-309">メソッド setHeapContext</span><span class="sxs-lookup"><span data-stu-id="49c97-309">Method setHeapContext</span></span>

    public void setHeapContext(str description)

#### <a name="parameters"></a><span data-ttu-id="49c97-310">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-310">Parameters</span></span>

<span data-ttu-id="49c97-311">description</span><span class="sxs-lookup"><span data-stu-id="49c97-311">description</span></span>  

### <a name="method-new"></a><span data-ttu-id="49c97-312">メソッド new</span><span class="sxs-lookup"><span data-stu-id="49c97-312">Method new</span></span>

<span data-ttu-id="49c97-313">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="49c97-313">Initializes a new instance of the Object class.</span></span>

    public void new([str Filename])

#### <a name="parameters"></a><span data-ttu-id="49c97-314">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-314">Parameters</span></span>

<span data-ttu-id="49c97-315">ファイル名</span><span class="sxs-lookup"><span data-stu-id="49c97-315">Filename</span></span>  

### <a name="method-nextunfreedobject"></a><span data-ttu-id="49c97-316">メソッド nextUnfreedObject</span><span class="sxs-lookup"><span data-stu-id="49c97-316">Method nextUnfreedObject</span></span>

    public void nextUnfreedObject()

### <a name="method-checkheapstop"></a><span data-ttu-id="49c97-317">メソッド checkHeapStop</span><span class="sxs-lookup"><span data-stu-id="49c97-317">Method checkHeapStop</span></span>

    public void checkHeapStop()

### <a name="method-nextunfreedcursor"></a><span data-ttu-id="49c97-318">メソッド nextUnfreedCursor</span><span class="sxs-lookup"><span data-stu-id="49c97-318">Method nextUnfreedCursor</span></span>

    public void nextUnfreedCursor()

### <a name="method-setruntimebugcheckflags"></a><span data-ttu-id="49c97-319">メソッド setRuntimeBugcheckFlags</span><span class="sxs-lookup"><span data-stu-id="49c97-319">Method setRuntimeBugcheckFlags</span></span>

    public void setRuntimeBugcheckFlags(int flags)

#### <a name="parameters"></a><span data-ttu-id="49c97-320">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-320">Parameters</span></span>

<span data-ttu-id="49c97-321">flags</span><span class="sxs-lookup"><span data-stu-id="49c97-321">flags</span></span>  

### <a name="method-checkheapstart"></a><span data-ttu-id="49c97-322">メソッド checkHeapStart</span><span class="sxs-lookup"><span data-stu-id="49c97-322">Method checkHeapStart</span></span>

    public void checkHeapStart()

## <a name="class-helpdocsetnode"></a><span data-ttu-id="49c97-323">クラス HelpDocSetNode</span><span class="sxs-lookup"><span data-stu-id="49c97-323">Class HelpDocSetNode</span></span>
    class HelpDocSetNode extends TreeNode

### <a name="remarks"></a><span data-ttu-id="49c97-324">備考</span><span class="sxs-lookup"><span data-stu-id="49c97-324">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="49c97-325">例</span><span class="sxs-lookup"><span data-stu-id="49c97-325">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="49c97-326">メソッド</span><span class="sxs-lookup"><span data-stu-id="49c97-326">Methods</span></span>

| <span data-ttu-id="49c97-327">方法</span><span class="sxs-lookup"><span data-stu-id="49c97-327">Method</span></span>                                                     | <span data-ttu-id="49c97-328">説明</span><span class="sxs-lookup"><span data-stu-id="49c97-328">Description</span></span>                                                                |
|------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="49c97-329">public boolean addToApplicationHelpMenu(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49c97-329">public boolean addToApplicationHelpMenu(\[boolean value\])</span></span> |                                                                            |
| <span data-ttu-id="49c97-330">public boolean addToDeveloperHelpMenu(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49c97-330">public boolean addToDeveloperHelpMenu(\[boolean value\])</span></span>   |                                                                            |
| <span data-ttu-id="49c97-331">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49c97-331">public str changedBy(\[str value\])</span></span>                        | <span data-ttu-id="49c97-332">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49c97-332">Gets or sets the name of the user who last changed the application object.</span></span> |
| <span data-ttu-id="49c97-333">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="49c97-333">public Date changedDate(\[Date value\])</span></span>                    | <span data-ttu-id="49c97-334">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49c97-334">Gets or sets the date an application object was last changed.</span></span>              |
| <span data-ttu-id="49c97-335">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49c97-335">public str changedTime(\[str value\])</span></span>                      | <span data-ttu-id="49c97-336">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49c97-336">Gets or sets the time an application object was last changed.</span></span>              |
| <span data-ttu-id="49c97-337">public int contentLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49c97-337">public int contentLocation(\[int value\])</span></span>                  |                                                                            |
| <span data-ttu-id="49c97-338">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49c97-338">public str createdBy(\[str value\])</span></span>                        | <span data-ttu-id="49c97-339">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49c97-339">Gets or sets the name of the user who created the application object.</span></span>      |
| <span data-ttu-id="49c97-340">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="49c97-340">public Date creationDate(\[Date value\])</span></span>                   | <span data-ttu-id="49c97-341">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49c97-341">Gets or sets the date an application object was created.</span></span>                   |
| <span data-ttu-id="49c97-342">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49c97-342">public str creationTime(\[str value\])</span></span>                     |                                                                            |
| <span data-ttu-id="49c97-343">public boolean developerDocumentSet(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49c97-343">public boolean developerDocumentSet(\[boolean value\])</span></span>     |                                                                            |
| <span data-ttu-id="49c97-344">public str documentSetDescription(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49c97-344">public str documentSetDescription(\[str value\])</span></span>           |                                                                            |
| <span data-ttu-id="49c97-345">public str documentSetName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49c97-345">public str documentSetName(\[str value\])</span></span>                  |                                                                            |
| <span data-ttu-id="49c97-346">public str helpProviderClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49c97-346">public str helpProviderClass(\[str value\])</span></span>                |                                                                            |
| <span data-ttu-id="49c97-347">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="49c97-347">public Guid origin(\[Guid value\])</span></span>                         |                                                                            |
| <span data-ttu-id="49c97-348">public boolean userDocumentSet(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="49c97-348">public boolean userDocumentSet(\[boolean value\])</span></span>          |                                                                            |
| <span data-ttu-id="49c97-349">public void new(str DocSetName)</span><span class="sxs-lookup"><span data-stu-id="49c97-349">public void new(str DocSetName)</span></span>                            | <span data-ttu-id="49c97-350">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="49c97-350">Initializes a new instance of the TreeNode class.</span></span>                          |

### <a name="method-addtoapplicationhelpmenu"></a><span data-ttu-id="49c97-351">メソッド addToApplicationHelpMenu</span><span class="sxs-lookup"><span data-stu-id="49c97-351">Method addToApplicationHelpMenu</span></span>

    public boolean addToApplicationHelpMenu([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49c97-352">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-352">Parameters</span></span>

<span data-ttu-id="49c97-353">値</span><span class="sxs-lookup"><span data-stu-id="49c97-353">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-354">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-354">Return Value</span></span>

### <a name="method-addtodeveloperhelpmenu"></a><span data-ttu-id="49c97-355">メソッド addToDeveloperHelpMenu</span><span class="sxs-lookup"><span data-stu-id="49c97-355">Method addToDeveloperHelpMenu</span></span>

    public boolean addToDeveloperHelpMenu([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49c97-356">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-356">Parameters</span></span>

<span data-ttu-id="49c97-357">値</span><span class="sxs-lookup"><span data-stu-id="49c97-357">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-358">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-358">Return Value</span></span>

### <a name="method-changedby"></a><span data-ttu-id="49c97-359">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="49c97-359">Method changedBy</span></span>

<span data-ttu-id="49c97-360">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49c97-360">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="49c97-361">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-361">Parameters</span></span>

<span data-ttu-id="49c97-362">値</span><span class="sxs-lookup"><span data-stu-id="49c97-362">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-363">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-363">Return Value</span></span>

<span data-ttu-id="49c97-364">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="49c97-364">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="49c97-365">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="49c97-365">Method changedDate</span></span>

<span data-ttu-id="49c97-366">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49c97-366">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="49c97-367">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-367">Parameters</span></span>

<span data-ttu-id="49c97-368">値</span><span class="sxs-lookup"><span data-stu-id="49c97-368">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-369">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-369">Return Value</span></span>

<span data-ttu-id="49c97-370">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="49c97-370">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="49c97-371">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="49c97-371">Method changedTime</span></span>

<span data-ttu-id="49c97-372">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49c97-372">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="49c97-373">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-373">Parameters</span></span>

<span data-ttu-id="49c97-374">値</span><span class="sxs-lookup"><span data-stu-id="49c97-374">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-375">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-375">Return Value</span></span>

<span data-ttu-id="49c97-376">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="49c97-376">The time an application object was last changed.</span></span>

### <a name="method-contentlocation"></a><span data-ttu-id="49c97-377">メソッド contentLocation</span><span class="sxs-lookup"><span data-stu-id="49c97-377">Method contentLocation</span></span>

    public int contentLocation([int value])

#### <a name="parameters"></a><span data-ttu-id="49c97-378">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-378">Parameters</span></span>

<span data-ttu-id="49c97-379">値</span><span class="sxs-lookup"><span data-stu-id="49c97-379">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-380">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-380">Return Value</span></span>

### <a name="method-createdby"></a><span data-ttu-id="49c97-381">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="49c97-381">Method createdBy</span></span>

<span data-ttu-id="49c97-382">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49c97-382">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="49c97-383">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-383">Parameters</span></span>

<span data-ttu-id="49c97-384">値</span><span class="sxs-lookup"><span data-stu-id="49c97-384">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-385">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-385">Return Value</span></span>

<span data-ttu-id="49c97-386">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="49c97-386">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="49c97-387">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="49c97-387">Method creationDate</span></span>

<span data-ttu-id="49c97-388">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="49c97-388">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="49c97-389">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-389">Parameters</span></span>

<span data-ttu-id="49c97-390">値</span><span class="sxs-lookup"><span data-stu-id="49c97-390">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-391">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-391">Return Value</span></span>

<span data-ttu-id="49c97-392">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="49c97-392">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="49c97-393">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="49c97-393">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="49c97-394">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-394">Parameters</span></span>

<span data-ttu-id="49c97-395">値</span><span class="sxs-lookup"><span data-stu-id="49c97-395">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-396">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-396">Return Value</span></span>

### <a name="method-developerdocumentset"></a><span data-ttu-id="49c97-397">メソッド developerDocumentSet</span><span class="sxs-lookup"><span data-stu-id="49c97-397">Method developerDocumentSet</span></span>

    public boolean developerDocumentSet([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49c97-398">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-398">Parameters</span></span>

<span data-ttu-id="49c97-399">値</span><span class="sxs-lookup"><span data-stu-id="49c97-399">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-400">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-400">Return Value</span></span>

### <a name="method-documentsetdescription"></a><span data-ttu-id="49c97-401">メソッド documentSetDescription</span><span class="sxs-lookup"><span data-stu-id="49c97-401">Method documentSetDescription</span></span>

    public str documentSetDescription([str value])

#### <a name="parameters"></a><span data-ttu-id="49c97-402">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-402">Parameters</span></span>

<span data-ttu-id="49c97-403">値</span><span class="sxs-lookup"><span data-stu-id="49c97-403">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-404">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-404">Return Value</span></span>

### <a name="method-documentsetname"></a><span data-ttu-id="49c97-405">メソッド documentSetName</span><span class="sxs-lookup"><span data-stu-id="49c97-405">Method documentSetName</span></span>

    public str documentSetName([str value])

#### <a name="parameters"></a><span data-ttu-id="49c97-406">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-406">Parameters</span></span>

<span data-ttu-id="49c97-407">値</span><span class="sxs-lookup"><span data-stu-id="49c97-407">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-408">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-408">Return Value</span></span>

### <a name="method-helpproviderclass"></a><span data-ttu-id="49c97-409">メソッド helpProviderClass</span><span class="sxs-lookup"><span data-stu-id="49c97-409">Method helpProviderClass</span></span>

    public str helpProviderClass([str value])

#### <a name="parameters"></a><span data-ttu-id="49c97-410">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-410">Parameters</span></span>

<span data-ttu-id="49c97-411">値</span><span class="sxs-lookup"><span data-stu-id="49c97-411">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-412">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-412">Return Value</span></span>

### <a name="method-origin"></a><span data-ttu-id="49c97-413">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="49c97-413">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="49c97-414">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-414">Parameters</span></span>

<span data-ttu-id="49c97-415">値</span><span class="sxs-lookup"><span data-stu-id="49c97-415">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-416">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-416">Return Value</span></span>

### <a name="method-userdocumentset"></a><span data-ttu-id="49c97-417">メソッド userDocumentSet</span><span class="sxs-lookup"><span data-stu-id="49c97-417">Method userDocumentSet</span></span>

    public boolean userDocumentSet([boolean value])

#### <a name="parameters"></a><span data-ttu-id="49c97-418">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-418">Parameters</span></span>

<span data-ttu-id="49c97-419">値</span><span class="sxs-lookup"><span data-stu-id="49c97-419">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-420">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-420">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="49c97-421">メソッド new</span><span class="sxs-lookup"><span data-stu-id="49c97-421">Method new</span></span>

<span data-ttu-id="49c97-422">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="49c97-422">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str DocSetName)

#### <a name="parameters"></a><span data-ttu-id="49c97-423">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-423">Parameters</span></span>

<span data-ttu-id="49c97-424">DocSetName</span><span class="sxs-lookup"><span data-stu-id="49c97-424">DocSetName</span></span>  

## <a name="class-helpdocumentmanager"></a><span data-ttu-id="49c97-425">クラス HelpDocumentManager</span><span class="sxs-lookup"><span data-stu-id="49c97-425">Class HelpDocumentManager</span></span>
    class HelpDocumentManager extends Object

### <a name="remarks"></a><span data-ttu-id="49c97-426">備考</span><span class="sxs-lookup"><span data-stu-id="49c97-426">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="49c97-427">例</span><span class="sxs-lookup"><span data-stu-id="49c97-427">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="49c97-428">メソッド</span><span class="sxs-lookup"><span data-stu-id="49c97-428">Methods</span></span>

| <span data-ttu-id="49c97-429">方法</span><span class="sxs-lookup"><span data-stu-id="49c97-429">Method</span></span>                                                                                                              | <span data-ttu-id="49c97-430">説明</span><span class="sxs-lookup"><span data-stu-id="49c97-430">Description</span></span>                                                  |
|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="49c97-431">public void new()</span><span class="sxs-lookup"><span data-stu-id="49c97-431">public void new()</span></span>                                                                                                   | <span data-ttu-id="49c97-432">HelpDocumentManager クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="49c97-432">Initializes a new instance of the HelpDocumentManager class.</span></span> |
| <span data-ttu-id="49c97-433">::public static void showHelpTopic(\[str topic\], \[str documentSet\], \[str contentLanguage\], \[str uiLanguage\])</span><span class="sxs-lookup"><span data-stu-id="49c97-433">::public static void showHelpTopic(\[str topic\], \[str documentSet\], \[str contentLanguage\], \[str uiLanguage\])</span></span> |                                                              |
| <span data-ttu-id="49c97-434">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="49c97-434">public void finalize()</span></span>                                                                                              |                                                              |

### <a name="method-new"></a><span data-ttu-id="49c97-435">メソッド new</span><span class="sxs-lookup"><span data-stu-id="49c97-435">Method new</span></span>

<span data-ttu-id="49c97-436">HelpDocumentManager クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="49c97-436">Initializes a new instance of the HelpDocumentManager class.</span></span>

    public void new()

### <a name="method-showhelptopic"></a><span data-ttu-id="49c97-437">メソッド showHelpTopic</span><span class="sxs-lookup"><span data-stu-id="49c97-437">Method showHelpTopic</span></span>

    public static void showHelpTopic([str topic], [str documentSet], [str contentLanguage], [str uiLanguage])

#### <a name="parameters"></a><span data-ttu-id="49c97-438">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-438">Parameters</span></span>

<span data-ttu-id="49c97-439">トピック</span><span class="sxs-lookup"><span data-stu-id="49c97-439">topic</span></span>  

<!-- -->

<span data-ttu-id="49c97-440">documentSet</span><span class="sxs-lookup"><span data-stu-id="49c97-440">documentSet</span></span>  

<!-- -->

<span data-ttu-id="49c97-441">contentLanguage</span><span class="sxs-lookup"><span data-stu-id="49c97-441">contentLanguage</span></span>  

<!-- -->

<span data-ttu-id="49c97-442">uiLanguage</span><span class="sxs-lookup"><span data-stu-id="49c97-442">uiLanguage</span></span>  

### <a name="method-finalize"></a><span data-ttu-id="49c97-443">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="49c97-443">Method finalize</span></span>

    public void finalize()

## <a name="class-htmlfont"></a><span data-ttu-id="49c97-444">クラス HtmlFont</span><span class="sxs-lookup"><span data-stu-id="49c97-444">Class HtmlFont</span></span>
    class HtmlFont extends Object

### <a name="remarks"></a><span data-ttu-id="49c97-445">備考</span><span class="sxs-lookup"><span data-stu-id="49c97-445">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="49c97-446">例</span><span class="sxs-lookup"><span data-stu-id="49c97-446">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="49c97-447">メソッド</span><span class="sxs-lookup"><span data-stu-id="49c97-447">Methods</span></span>

| <span data-ttu-id="49c97-448">方法</span><span class="sxs-lookup"><span data-stu-id="49c97-448">Method</span></span>                                                                                                    | <span data-ttu-id="49c97-449">説明</span><span class="sxs-lookup"><span data-stu-id="49c97-449">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="49c97-450">public int backColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49c97-450">public int backColor(\[int value\])</span></span>                                                                       |                                                 |
| <span data-ttu-id="49c97-451">public str fontName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="49c97-451">public str fontName(\[str value\])</span></span>                                                                        |                                                 |
| <span data-ttu-id="49c97-452">public int pointSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49c97-452">public int pointSize(\[int value\])</span></span>                                                                       |                                                 |
| <span data-ttu-id="49c97-453">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49c97-453">public int style(\[int value\])</span></span>                                                                           |                                                 |
| <span data-ttu-id="49c97-454">public int textColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="49c97-454">public int textColor(\[int value\])</span></span>                                                                       |                                                 |
| <span data-ttu-id="49c97-455">public void new(\[str TypeFace\], \[int PointSize\], \[int Style\], \[int TextColor\], \[int BackColor\])</span><span class="sxs-lookup"><span data-stu-id="49c97-455">public void new(\[str TypeFace\], \[int PointSize\], \[int Style\], \[int TextColor\], \[int BackColor\])</span></span> | <span data-ttu-id="49c97-456">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="49c97-456">Initializes a new instance of the Object class.</span></span> |
| <span data-ttu-id="49c97-457">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="49c97-457">public void finalize()</span></span>                                                                                    |                                                 |

### <a name="method-backcolor"></a><span data-ttu-id="49c97-458">メソッド backColor</span><span class="sxs-lookup"><span data-stu-id="49c97-458">Method backColor</span></span>

    public int backColor([int value])

#### <a name="parameters"></a><span data-ttu-id="49c97-459">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-459">Parameters</span></span>

<span data-ttu-id="49c97-460">値</span><span class="sxs-lookup"><span data-stu-id="49c97-460">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-461">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-461">Return Value</span></span>

### <a name="method-fontname"></a><span data-ttu-id="49c97-462">メソッド fontName</span><span class="sxs-lookup"><span data-stu-id="49c97-462">Method fontName</span></span>

    public str fontName([str value])

#### <a name="parameters"></a><span data-ttu-id="49c97-463">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-463">Parameters</span></span>

<span data-ttu-id="49c97-464">値</span><span class="sxs-lookup"><span data-stu-id="49c97-464">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-465">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-465">Return Value</span></span>

### <a name="method-pointsize"></a><span data-ttu-id="49c97-466">メソッド pointSize</span><span class="sxs-lookup"><span data-stu-id="49c97-466">Method pointSize</span></span>

    public int pointSize([int value])

#### <a name="parameters"></a><span data-ttu-id="49c97-467">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-467">Parameters</span></span>

<span data-ttu-id="49c97-468">値</span><span class="sxs-lookup"><span data-stu-id="49c97-468">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-469">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-469">Return Value</span></span>

### <a name="method-style"></a><span data-ttu-id="49c97-470">メソッド style</span><span class="sxs-lookup"><span data-stu-id="49c97-470">Method style</span></span>

    public int style([int value])

#### <a name="parameters"></a><span data-ttu-id="49c97-471">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-471">Parameters</span></span>

<span data-ttu-id="49c97-472">値</span><span class="sxs-lookup"><span data-stu-id="49c97-472">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-473">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-473">Return Value</span></span>

### <a name="method-textcolor"></a><span data-ttu-id="49c97-474">メソッド textColor</span><span class="sxs-lookup"><span data-stu-id="49c97-474">Method textColor</span></span>

    public int textColor([int value])

#### <a name="parameters"></a><span data-ttu-id="49c97-475">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-475">Parameters</span></span>

<span data-ttu-id="49c97-476">値</span><span class="sxs-lookup"><span data-stu-id="49c97-476">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="49c97-477">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c97-477">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="49c97-478">メソッド new</span><span class="sxs-lookup"><span data-stu-id="49c97-478">Method new</span></span>

<span data-ttu-id="49c97-479">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="49c97-479">Initializes a new instance of the Object class.</span></span>

    public void new([str TypeFace], [int PointSize], [int Style], [int TextColor], [int BackColor])

#### <a name="parameters"></a><span data-ttu-id="49c97-480">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c97-480">Parameters</span></span>

<span data-ttu-id="49c97-481">TypeFace</span><span class="sxs-lookup"><span data-stu-id="49c97-481">TypeFace</span></span>  

<!-- -->

<span data-ttu-id="49c97-482">PointSize</span><span class="sxs-lookup"><span data-stu-id="49c97-482">PointSize</span></span>  

<!-- -->

<span data-ttu-id="49c97-483">スタイル</span><span class="sxs-lookup"><span data-stu-id="49c97-483">Style</span></span>  

<!-- -->

<span data-ttu-id="49c97-484">TextColor</span><span class="sxs-lookup"><span data-stu-id="49c97-484">TextColor</span></span>  

<!-- -->

<span data-ttu-id="49c97-485">BackColor</span><span class="sxs-lookup"><span data-stu-id="49c97-485">BackColor</span></span>  

### <a name="method-finalize"></a><span data-ttu-id="49c97-486">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="49c97-486">Method finalize</span></span>

    public void finalize()




