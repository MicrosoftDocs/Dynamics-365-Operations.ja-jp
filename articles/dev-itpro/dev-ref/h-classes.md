---
title: H クラス
description: 文字 H で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 52591
ms.assetid: c27e2044-28c2-432a-b15f-a41d26a83a52
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 40e4ccefb7389571b6ea84d37b54d8fbf5822867
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537026"
---
# <a name="h-classes"></a><span data-ttu-id="a688d-103">H クラス</span><span class="sxs-lookup"><span data-stu-id="a688d-103">H classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a688d-104">文字 H で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="a688d-104">System API classes that start with the letter H.</span></span>

<a name="class-heapcheck"></a><span data-ttu-id="a688d-105">クラス HeapCheck</span><span class="sxs-lookup"><span data-stu-id="a688d-105">Class HeapCheck</span></span>
---------------

    class HeapCheck extends Object

### <a name="remarks"></a><span data-ttu-id="a688d-106">備考</span><span class="sxs-lookup"><span data-stu-id="a688d-106">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="a688d-107">例</span><span class="sxs-lookup"><span data-stu-id="a688d-107">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="a688d-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="a688d-108">Methods</span></span>

| <span data-ttu-id="a688d-109">方法</span><span class="sxs-lookup"><span data-stu-id="a688d-109">Method</span></span>                                                                                      | <span data-ttu-id="a688d-110">説明</span><span class="sxs-lookup"><span data-stu-id="a688d-110">Description</span></span>                                     |
|---------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="a688d-111">public int accessCnt()</span><span class="sxs-lookup"><span data-stu-id="a688d-111">public int accessCnt()</span></span>                                                                      |                                                 |
| <span data-ttu-id="a688d-112">public int addRefCnt()</span><span class="sxs-lookup"><span data-stu-id="a688d-112">public int addRefCnt()</span></span>                                                                      |                                                 |
| <span data-ttu-id="a688d-113">public Int64 blocksAllocated(\[int pool\])</span><span class="sxs-lookup"><span data-stu-id="a688d-113">public Int64 blocksAllocated(\[int pool\])</span></span>                                                  |                                                 |
| <span data-ttu-id="a688d-114">public int breakCount(\[int count\])</span><span class="sxs-lookup"><span data-stu-id="a688d-114">public int breakCount(\[int count\])</span></span>                                                        |                                                 |
| <span data-ttu-id="a688d-115">public Int64 bytesAllocated(\[int pool\])</span><span class="sxs-lookup"><span data-stu-id="a688d-115">public Int64 bytesAllocated(\[int pool\])</span></span>                                                   |                                                 |
| <span data-ttu-id="a688d-116">public Int64 ceiling(int pool, \[int ceiling\])</span><span class="sxs-lookup"><span data-stu-id="a688d-116">public Int64 ceiling(int pool, \[int ceiling\])</span></span>                                             |                                                 |
| <span data-ttu-id="a688d-117">public int context(\[int context\])</span><span class="sxs-lookup"><span data-stu-id="a688d-117">public int context(\[int context\])</span></span>                                                         |                                                 |
| <span data-ttu-id="a688d-118">public int count(\[int count\])</span><span class="sxs-lookup"><span data-stu-id="a688d-118">public int count(\[int count\])</span></span>                                                             |                                                 |
| <span data-ttu-id="a688d-119">public int countObjects(int classId)</span><span class="sxs-lookup"><span data-stu-id="a688d-119">public int countObjects(int classId)</span></span>                                                        |                                                 |
| <span data-ttu-id="a688d-120">public container createAContainer()</span><span class="sxs-lookup"><span data-stu-id="a688d-120">public container createAContainer()</span></span>                                                         |                                                 |
| <span data-ttu-id="a688d-121">public int csCallCnt()</span><span class="sxs-lookup"><span data-stu-id="a688d-121">public int csCallCnt()</span></span>                                                                      |                                                 |
| <span data-ttu-id="a688d-122">public int csSweepCnt()</span><span class="sxs-lookup"><span data-stu-id="a688d-122">public int csSweepCnt()</span></span>                                                                     |                                                 |
| <span data-ttu-id="a688d-123">public container dataByContext(\[int poolNo\], \[int context\])</span><span class="sxs-lookup"><span data-stu-id="a688d-123">public container dataByContext(\[int poolNo\], \[int context\])</span></span>                             |                                                 |
| <span data-ttu-id="a688d-124">public int dumpCursors()</span><span class="sxs-lookup"><span data-stu-id="a688d-124">public int dumpCursors()</span></span>                                                                    |                                                 |
| <span data-ttu-id="a688d-125">public int dumpObjects()</span><span class="sxs-lookup"><span data-stu-id="a688d-125">public int dumpObjects()</span></span>                                                                    |                                                 |
| <span data-ttu-id="a688d-126">public int filename(\[str filename\])</span><span class="sxs-lookup"><span data-stu-id="a688d-126">public int filename(\[str filename\])</span></span>                                                       |                                                 |
| <span data-ttu-id="a688d-127">public int fixedBlockSize(int pool, \[int blockSize\])</span><span class="sxs-lookup"><span data-stu-id="a688d-127">public int fixedBlockSize(int pool, \[int blockSize\])</span></span>                                      |                                                 |
| <span data-ttu-id="a688d-128">public int floor(int pool, \[int floor\])</span><span class="sxs-lookup"><span data-stu-id="a688d-128">public int floor(int pool, \[int floor\])</span></span>                                                   |                                                 |
| <span data-ttu-id="a688d-129">public int freeRefCnt()</span><span class="sxs-lookup"><span data-stu-id="a688d-129">public int freeRefCnt()</span></span>                                                                     |                                                 |
| <span data-ttu-id="a688d-130">public int getRuntimeBugcheckFlags()</span><span class="sxs-lookup"><span data-stu-id="a688d-130">public int getRuntimeBugcheckFlags()</span></span>                                                        |                                                 |
| <span data-ttu-id="a688d-131">public Common getUnfreedCursor()</span><span class="sxs-lookup"><span data-stu-id="a688d-131">public Common getUnfreedCursor()</span></span>                                                            |                                                 |
| <span data-ttu-id="a688d-132">public Common getUnfreedObject()</span><span class="sxs-lookup"><span data-stu-id="a688d-132">public Common getUnfreedObject()</span></span>                                                            |                                                 |
| <span data-ttu-id="a688d-133">public boolean include(int objectNo, \[boolean include\])</span><span class="sxs-lookup"><span data-stu-id="a688d-133">public boolean include(int objectNo, \[boolean include\])</span></span>                                   |                                                 |
| <span data-ttu-id="a688d-134">public boolean moreUnfreedCursors()</span><span class="sxs-lookup"><span data-stu-id="a688d-134">public boolean moreUnfreedCursors()</span></span>                                                         |                                                 |
| <span data-ttu-id="a688d-135">public boolean moreUnfreedObjects()</span><span class="sxs-lookup"><span data-stu-id="a688d-135">public boolean moreUnfreedObjects()</span></span>                                                         |                                                 |
| <span data-ttu-id="a688d-136">public int objectContext(int objNo, \[int context\])</span><span class="sxs-lookup"><span data-stu-id="a688d-136">public int objectContext(int objNo, \[int context\])</span></span>                                        |                                                 |
| <span data-ttu-id="a688d-137">public int pageSize(int pool, \[int pageSize\])</span><span class="sxs-lookup"><span data-stu-id="a688d-137">public int pageSize(int pool, \[int pageSize\])</span></span>                                             |                                                 |
| <span data-ttu-id="a688d-138">public int poolCount()</span><span class="sxs-lookup"><span data-stu-id="a688d-138">public int poolCount()</span></span>                                                                      |                                                 |
| <span data-ttu-id="a688d-139">public str poolName(int poolNo)</span><span class="sxs-lookup"><span data-stu-id="a688d-139">public str poolName(int poolNo)</span></span>                                                             |                                                 |
| <span data-ttu-id="a688d-140">public int smallBlockSize(int pool, \[int blockSize\])</span><span class="sxs-lookup"><span data-stu-id="a688d-140">public int smallBlockSize(int pool, \[int blockSize\])</span></span>                                      |                                                 |
| <span data-ttu-id="a688d-141">public int sweepCnt()</span><span class="sxs-lookup"><span data-stu-id="a688d-141">public int sweepCnt()</span></span>                                                                       |                                                 |
| <span data-ttu-id="a688d-142">public int testBlocks(\[int arg1\])</span><span class="sxs-lookup"><span data-stu-id="a688d-142">public int testBlocks(\[int arg1\])</span></span>                                                         |                                                 |
| <span data-ttu-id="a688d-143">public str unfreedObjectClass()</span><span class="sxs-lookup"><span data-stu-id="a688d-143">public str unfreedObjectClass()</span></span>                                                             |                                                 |
| <span data-ttu-id="a688d-144">public boolean unfreedObjectClient()</span><span class="sxs-lookup"><span data-stu-id="a688d-144">public boolean unfreedObjectClient()</span></span>                                                        |                                                 |
| <span data-ttu-id="a688d-145">public boolean unfreedObjectFinalized()</span><span class="sxs-lookup"><span data-stu-id="a688d-145">public boolean unfreedObjectFinalized()</span></span>                                                     |                                                 |
| <span data-ttu-id="a688d-146">public int unfreedObjectHandle()</span><span class="sxs-lookup"><span data-stu-id="a688d-146">public int unfreedObjectHandle()</span></span>                                                            |                                                 |
| <span data-ttu-id="a688d-147">public int unfreedObjectIdent()</span><span class="sxs-lookup"><span data-stu-id="a688d-147">public int unfreedObjectIdent()</span></span>                                                             |                                                 |
| <span data-ttu-id="a688d-148">public int unfreedObjectUseCount()</span><span class="sxs-lookup"><span data-stu-id="a688d-148">public int unfreedObjectUseCount()</span></span>                                                          |                                                 |
| <span data-ttu-id="a688d-149">public str version()</span><span class="sxs-lookup"><span data-stu-id="a688d-149">public str version()</span></span>                                                                        |                                                 |
| <span data-ttu-id="a688d-150">public void checkHeap(str Description, \[int context\], \[int pool\], \[boolean detailed\])</span><span class="sxs-lookup"><span data-stu-id="a688d-150">public void checkHeap(str Description, \[int context\], \[int pool\], \[boolean detailed\])</span></span> |                                                 |
| <span data-ttu-id="a688d-151">public void shrinkPool(\[int poolNo\])</span><span class="sxs-lookup"><span data-stu-id="a688d-151">public void shrinkPool(\[int poolNo\])</span></span>                                                      |                                                 |
| <span data-ttu-id="a688d-152">public void postCompactingMessage()</span><span class="sxs-lookup"><span data-stu-id="a688d-152">public void postCompactingMessage()</span></span>                                                         |                                                 |
| <span data-ttu-id="a688d-153">public void checkHeapDif(str Description, \[int context\], \[int pool\])</span><span class="sxs-lookup"><span data-stu-id="a688d-153">public void checkHeapDif(str Description, \[int context\], \[int pool\])</span></span>                    |                                                 |
| <span data-ttu-id="a688d-154">public void clearHeapContext()</span><span class="sxs-lookup"><span data-stu-id="a688d-154">public void clearHeapContext()</span></span>                                                              |                                                 |
| <span data-ttu-id="a688d-155">public void writeString(str text)</span><span class="sxs-lookup"><span data-stu-id="a688d-155">public void writeString(str text)</span></span>                                                           |                                                 |
| <span data-ttu-id="a688d-156">public void firstUnfreedCursor()</span><span class="sxs-lookup"><span data-stu-id="a688d-156">public void firstUnfreedCursor()</span></span>                                                            |                                                 |
| <span data-ttu-id="a688d-157">public void dumpDGMLGraph()</span><span class="sxs-lookup"><span data-stu-id="a688d-157">public void dumpDGMLGraph()</span></span>                                                                 |                                                 |
| <span data-ttu-id="a688d-158">public void firstUnfreedObject()</span><span class="sxs-lookup"><span data-stu-id="a688d-158">public void firstUnfreedObject()</span></span>                                                            |                                                 |
| <span data-ttu-id="a688d-159">public void setHeapContext(str description)</span><span class="sxs-lookup"><span data-stu-id="a688d-159">public void setHeapContext(str description)</span></span>                                                 |                                                 |
| <span data-ttu-id="a688d-160">public void new(\[str Filename\])</span><span class="sxs-lookup"><span data-stu-id="a688d-160">public void new(\[str Filename\])</span></span>                                                           | <span data-ttu-id="a688d-161">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a688d-161">Initializes a new instance of the Object class.</span></span> |
| <span data-ttu-id="a688d-162">public void nextUnfreedObject()</span><span class="sxs-lookup"><span data-stu-id="a688d-162">public void nextUnfreedObject()</span></span>                                                             |                                                 |
| <span data-ttu-id="a688d-163">public void checkHeapStop()</span><span class="sxs-lookup"><span data-stu-id="a688d-163">public void checkHeapStop()</span></span>                                                                 |                                                 |
| <span data-ttu-id="a688d-164">public void nextUnfreedCursor()</span><span class="sxs-lookup"><span data-stu-id="a688d-164">public void nextUnfreedCursor()</span></span>                                                             |                                                 |
| <span data-ttu-id="a688d-165">public void setRuntimeBugcheckFlags(int flags)</span><span class="sxs-lookup"><span data-stu-id="a688d-165">public void setRuntimeBugcheckFlags(int flags)</span></span>                                              |                                                 |
| <span data-ttu-id="a688d-166">public void checkHeapStart()</span><span class="sxs-lookup"><span data-stu-id="a688d-166">public void checkHeapStart()</span></span>                                                                |                                                 |

### <a name="method-accesscnt"></a><span data-ttu-id="a688d-167">メソッド accessCnt</span><span class="sxs-lookup"><span data-stu-id="a688d-167">Method accessCnt</span></span>

    public int accessCnt()

#### <a name="return-value"></a><span data-ttu-id="a688d-168">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-168">Return Value</span></span>

### <a name="method-addrefcnt"></a><span data-ttu-id="a688d-169">メソッド addRefCnt</span><span class="sxs-lookup"><span data-stu-id="a688d-169">Method addRefCnt</span></span>

    public int addRefCnt()

#### <a name="return-value"></a><span data-ttu-id="a688d-170">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-170">Return Value</span></span>

### <a name="method-blocksallocated"></a><span data-ttu-id="a688d-171">メソッド blocksAllocated</span><span class="sxs-lookup"><span data-stu-id="a688d-171">Method blocksAllocated</span></span>

    public Int64 blocksAllocated([int pool])

#### <a name="parameters"></a><span data-ttu-id="a688d-172">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-172">Parameters</span></span>

<span data-ttu-id="a688d-173">管理グループ</span><span class="sxs-lookup"><span data-stu-id="a688d-173">pool</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-174">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-174">Return Value</span></span>

### <a name="method-breakcount"></a><span data-ttu-id="a688d-175">メソッド breakCount</span><span class="sxs-lookup"><span data-stu-id="a688d-175">Method breakCount</span></span>

    public int breakCount([int count])

#### <a name="parameters"></a><span data-ttu-id="a688d-176">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-176">Parameters</span></span>

<span data-ttu-id="a688d-177">カウント</span><span class="sxs-lookup"><span data-stu-id="a688d-177">count</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-178">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-178">Return Value</span></span>

### <a name="method-bytesallocated"></a><span data-ttu-id="a688d-179">メソッド bytesAllocated</span><span class="sxs-lookup"><span data-stu-id="a688d-179">Method bytesAllocated</span></span>

    public Int64 bytesAllocated([int pool])

#### <a name="parameters"></a><span data-ttu-id="a688d-180">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-180">Parameters</span></span>

<span data-ttu-id="a688d-181">管理グループ</span><span class="sxs-lookup"><span data-stu-id="a688d-181">pool</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-182">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-182">Return Value</span></span>

### <a name="method-ceiling"></a><span data-ttu-id="a688d-183">メソッド ceiling</span><span class="sxs-lookup"><span data-stu-id="a688d-183">Method ceiling</span></span>

    public Int64 ceiling(int pool, [int ceiling])

#### <a name="parameters"></a><span data-ttu-id="a688d-184">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-184">Parameters</span></span>

<span data-ttu-id="a688d-185">管理グループ</span><span class="sxs-lookup"><span data-stu-id="a688d-185">pool</span></span>  

<!-- -->

<span data-ttu-id="a688d-186">ceiling</span><span class="sxs-lookup"><span data-stu-id="a688d-186">ceiling</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-187">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-187">Return Value</span></span>

### <a name="method-context"></a><span data-ttu-id="a688d-188">メソッド context</span><span class="sxs-lookup"><span data-stu-id="a688d-188">Method context</span></span>

    public int context([int context])

#### <a name="parameters"></a><span data-ttu-id="a688d-189">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-189">Parameters</span></span>

<span data-ttu-id="a688d-190">context</span><span class="sxs-lookup"><span data-stu-id="a688d-190">context</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-191">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-191">Return Value</span></span>

### <a name="method-count"></a><span data-ttu-id="a688d-192">メソッド count</span><span class="sxs-lookup"><span data-stu-id="a688d-192">Method count</span></span>

    public int count([int count])

#### <a name="parameters"></a><span data-ttu-id="a688d-193">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-193">Parameters</span></span>

<span data-ttu-id="a688d-194">カウント</span><span class="sxs-lookup"><span data-stu-id="a688d-194">count</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-195">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-195">Return Value</span></span>

### <a name="method-countobjects"></a><span data-ttu-id="a688d-196">メソッド countObjects</span><span class="sxs-lookup"><span data-stu-id="a688d-196">Method countObjects</span></span>

    public int countObjects(int classId)

#### <a name="parameters"></a><span data-ttu-id="a688d-197">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-197">Parameters</span></span>

<span data-ttu-id="a688d-198">classId</span><span class="sxs-lookup"><span data-stu-id="a688d-198">classId</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-199">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-199">Return Value</span></span>

### <a name="method-createacontainer"></a><span data-ttu-id="a688d-200">メソッド createAContainer</span><span class="sxs-lookup"><span data-stu-id="a688d-200">Method createAContainer</span></span>

    public container createAContainer()

#### <a name="return-value"></a><span data-ttu-id="a688d-201">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-201">Return Value</span></span>

### <a name="method-cscallcnt"></a><span data-ttu-id="a688d-202">メソッド csCallCnt</span><span class="sxs-lookup"><span data-stu-id="a688d-202">Method csCallCnt</span></span>

    public int csCallCnt()

#### <a name="return-value"></a><span data-ttu-id="a688d-203">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-203">Return Value</span></span>

### <a name="method-cssweepcnt"></a><span data-ttu-id="a688d-204">メソッド csSweepCnt</span><span class="sxs-lookup"><span data-stu-id="a688d-204">Method csSweepCnt</span></span>

    public int csSweepCnt()

#### <a name="return-value"></a><span data-ttu-id="a688d-205">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-205">Return Value</span></span>

### <a name="method-databycontext"></a><span data-ttu-id="a688d-206">メソッド dataByContext</span><span class="sxs-lookup"><span data-stu-id="a688d-206">Method dataByContext</span></span>

    public container dataByContext([int poolNo], [int context])

#### <a name="parameters"></a><span data-ttu-id="a688d-207">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-207">Parameters</span></span>

<span data-ttu-id="a688d-208">poolNo</span><span class="sxs-lookup"><span data-stu-id="a688d-208">poolNo</span></span>  

<!-- -->

<span data-ttu-id="a688d-209">context</span><span class="sxs-lookup"><span data-stu-id="a688d-209">context</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-210">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-210">Return Value</span></span>

### <a name="method-dumpcursors"></a><span data-ttu-id="a688d-211">メソッド dumpCursors</span><span class="sxs-lookup"><span data-stu-id="a688d-211">Method dumpCursors</span></span>

    public int dumpCursors()

#### <a name="return-value"></a><span data-ttu-id="a688d-212">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-212">Return Value</span></span>

### <a name="method-dumpobjects"></a><span data-ttu-id="a688d-213">メソッド dumpObjects</span><span class="sxs-lookup"><span data-stu-id="a688d-213">Method dumpObjects</span></span>

    public int dumpObjects()

#### <a name="return-value"></a><span data-ttu-id="a688d-214">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-214">Return Value</span></span>

### <a name="method-filename"></a><span data-ttu-id="a688d-215">メソッド filename</span><span class="sxs-lookup"><span data-stu-id="a688d-215">Method filename</span></span>

    public int filename([str filename])

#### <a name="parameters"></a><span data-ttu-id="a688d-216">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-216">Parameters</span></span>

<span data-ttu-id="a688d-217">filename</span><span class="sxs-lookup"><span data-stu-id="a688d-217">filename</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-218">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-218">Return Value</span></span>

### <a name="method-fixedblocksize"></a><span data-ttu-id="a688d-219">メソッド fixedBlockSize</span><span class="sxs-lookup"><span data-stu-id="a688d-219">Method fixedBlockSize</span></span>

    public int fixedBlockSize(int pool, [int blockSize])

#### <a name="parameters"></a><span data-ttu-id="a688d-220">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-220">Parameters</span></span>

<span data-ttu-id="a688d-221">管理グループ</span><span class="sxs-lookup"><span data-stu-id="a688d-221">pool</span></span>  

<!-- -->

<span data-ttu-id="a688d-222">blockSize</span><span class="sxs-lookup"><span data-stu-id="a688d-222">blockSize</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-223">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-223">Return Value</span></span>

### <a name="method-floor"></a><span data-ttu-id="a688d-224">メソッド floor</span><span class="sxs-lookup"><span data-stu-id="a688d-224">Method floor</span></span>

    public int floor(int pool, [int floor])

#### <a name="parameters"></a><span data-ttu-id="a688d-225">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-225">Parameters</span></span>

<span data-ttu-id="a688d-226">管理グループ</span><span class="sxs-lookup"><span data-stu-id="a688d-226">pool</span></span>  

<!-- -->

<span data-ttu-id="a688d-227">floor</span><span class="sxs-lookup"><span data-stu-id="a688d-227">floor</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-228">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-228">Return Value</span></span>

### <a name="method-freerefcnt"></a><span data-ttu-id="a688d-229">メソッド freeRefCnt</span><span class="sxs-lookup"><span data-stu-id="a688d-229">Method freeRefCnt</span></span>

    public int freeRefCnt()

#### <a name="return-value"></a><span data-ttu-id="a688d-230">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-230">Return Value</span></span>

### <a name="method-getruntimebugcheckflags"></a><span data-ttu-id="a688d-231">メソッド getRuntimeBugcheckFlags</span><span class="sxs-lookup"><span data-stu-id="a688d-231">Method getRuntimeBugcheckFlags</span></span>

    public int getRuntimeBugcheckFlags()

#### <a name="return-value"></a><span data-ttu-id="a688d-232">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-232">Return Value</span></span>

### <a name="method-getunfreedcursor"></a><span data-ttu-id="a688d-233">メソッド getUnfreedCursor</span><span class="sxs-lookup"><span data-stu-id="a688d-233">Method getUnfreedCursor</span></span>

    public Common getUnfreedCursor()

#### <a name="return-value"></a><span data-ttu-id="a688d-234">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-234">Return Value</span></span>

### <a name="method-getunfreedobject"></a><span data-ttu-id="a688d-235">メソッド getUnfreedObject</span><span class="sxs-lookup"><span data-stu-id="a688d-235">Method getUnfreedObject</span></span>

    public Common getUnfreedObject()

#### <a name="return-value"></a><span data-ttu-id="a688d-236">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-236">Return Value</span></span>

### <a name="method-include"></a><span data-ttu-id="a688d-237">メソッド include</span><span class="sxs-lookup"><span data-stu-id="a688d-237">Method include</span></span>

    public boolean include(int objectNo, [boolean include])

#### <a name="parameters"></a><span data-ttu-id="a688d-238">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-238">Parameters</span></span>

<span data-ttu-id="a688d-239">objectNo</span><span class="sxs-lookup"><span data-stu-id="a688d-239">objectNo</span></span>  

<!-- -->

<span data-ttu-id="a688d-240">include</span><span class="sxs-lookup"><span data-stu-id="a688d-240">include</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-241">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-241">Return Value</span></span>

### <a name="method-moreunfreedcursors"></a><span data-ttu-id="a688d-242">メソッド moreUnfreedCursors</span><span class="sxs-lookup"><span data-stu-id="a688d-242">Method moreUnfreedCursors</span></span>

    public boolean moreUnfreedCursors()

#### <a name="return-value"></a><span data-ttu-id="a688d-243">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-243">Return Value</span></span>

### <a name="method-moreunfreedobjects"></a><span data-ttu-id="a688d-244">メソッド moreUnfreedObjects</span><span class="sxs-lookup"><span data-stu-id="a688d-244">Method moreUnfreedObjects</span></span>

    public boolean moreUnfreedObjects()

#### <a name="return-value"></a><span data-ttu-id="a688d-245">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-245">Return Value</span></span>

### <a name="method-objectcontext"></a><span data-ttu-id="a688d-246">メソッド objectContext</span><span class="sxs-lookup"><span data-stu-id="a688d-246">Method objectContext</span></span>

    public int objectContext(int objNo, [int context])

#### <a name="parameters"></a><span data-ttu-id="a688d-247">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-247">Parameters</span></span>

<span data-ttu-id="a688d-248">objNo</span><span class="sxs-lookup"><span data-stu-id="a688d-248">objNo</span></span>  

<!-- -->

<span data-ttu-id="a688d-249">context</span><span class="sxs-lookup"><span data-stu-id="a688d-249">context</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-250">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-250">Return Value</span></span>

### <a name="method-pagesize"></a><span data-ttu-id="a688d-251">メソッド pageSize</span><span class="sxs-lookup"><span data-stu-id="a688d-251">Method pageSize</span></span>

    public int pageSize(int pool, [int pageSize])

#### <a name="parameters"></a><span data-ttu-id="a688d-252">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-252">Parameters</span></span>

<span data-ttu-id="a688d-253">管理グループ</span><span class="sxs-lookup"><span data-stu-id="a688d-253">pool</span></span>  

<!-- -->

<span data-ttu-id="a688d-254">pageSize</span><span class="sxs-lookup"><span data-stu-id="a688d-254">pageSize</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-255">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-255">Return Value</span></span>

### <a name="method-poolcount"></a><span data-ttu-id="a688d-256">メソッド poolCount</span><span class="sxs-lookup"><span data-stu-id="a688d-256">Method poolCount</span></span>

    public int poolCount()

#### <a name="return-value"></a><span data-ttu-id="a688d-257">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-257">Return Value</span></span>

### <a name="method-poolname"></a><span data-ttu-id="a688d-258">メソッド poolName</span><span class="sxs-lookup"><span data-stu-id="a688d-258">Method poolName</span></span>

    public str poolName(int poolNo)

#### <a name="parameters"></a><span data-ttu-id="a688d-259">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-259">Parameters</span></span>

<span data-ttu-id="a688d-260">poolNo</span><span class="sxs-lookup"><span data-stu-id="a688d-260">poolNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-261">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-261">Return Value</span></span>

### <a name="method-smallblocksize"></a><span data-ttu-id="a688d-262">メソッド smallBlockSize</span><span class="sxs-lookup"><span data-stu-id="a688d-262">Method smallBlockSize</span></span>

    public int smallBlockSize(int pool, [int blockSize])

#### <a name="parameters"></a><span data-ttu-id="a688d-263">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-263">Parameters</span></span>

<span data-ttu-id="a688d-264">管理グループ</span><span class="sxs-lookup"><span data-stu-id="a688d-264">pool</span></span>  

<!-- -->

<span data-ttu-id="a688d-265">blockSize</span><span class="sxs-lookup"><span data-stu-id="a688d-265">blockSize</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-266">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-266">Return Value</span></span>

### <a name="method-sweepcnt"></a><span data-ttu-id="a688d-267">メソッド sweepCnt</span><span class="sxs-lookup"><span data-stu-id="a688d-267">Method sweepCnt</span></span>

    public int sweepCnt()

#### <a name="return-value"></a><span data-ttu-id="a688d-268">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-268">Return Value</span></span>

### <a name="method-testblocks"></a><span data-ttu-id="a688d-269">メソッド testBlocks</span><span class="sxs-lookup"><span data-stu-id="a688d-269">Method testBlocks</span></span>

    public int testBlocks([int arg1])

#### <a name="parameters"></a><span data-ttu-id="a688d-270">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-270">Parameters</span></span>

<span data-ttu-id="a688d-271">arg1</span><span class="sxs-lookup"><span data-stu-id="a688d-271">arg1</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-272">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-272">Return Value</span></span>

### <a name="method-unfreedobjectclass"></a><span data-ttu-id="a688d-273">メソッド unfreedObjectClass</span><span class="sxs-lookup"><span data-stu-id="a688d-273">Method unfreedObjectClass</span></span>

    public str unfreedObjectClass()

#### <a name="return-value"></a><span data-ttu-id="a688d-274">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-274">Return Value</span></span>

### <a name="method-unfreedobjectclient"></a><span data-ttu-id="a688d-275">メソッド unfreedObjectClient</span><span class="sxs-lookup"><span data-stu-id="a688d-275">Method unfreedObjectClient</span></span>

    public boolean unfreedObjectClient()

#### <a name="return-value"></a><span data-ttu-id="a688d-276">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-276">Return Value</span></span>

### <a name="method-unfreedobjectfinalized"></a><span data-ttu-id="a688d-277">メソッド unfreedObjectFinalized</span><span class="sxs-lookup"><span data-stu-id="a688d-277">Method unfreedObjectFinalized</span></span>

    public boolean unfreedObjectFinalized()

#### <a name="return-value"></a><span data-ttu-id="a688d-278">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-278">Return Value</span></span>

### <a name="method-unfreedobjecthandle"></a><span data-ttu-id="a688d-279">メソッド unfreedObjectHandle</span><span class="sxs-lookup"><span data-stu-id="a688d-279">Method unfreedObjectHandle</span></span>

    public int unfreedObjectHandle()

#### <a name="return-value"></a><span data-ttu-id="a688d-280">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-280">Return Value</span></span>

### <a name="method-unfreedobjectident"></a><span data-ttu-id="a688d-281">メソッド unfreedObjectIdent</span><span class="sxs-lookup"><span data-stu-id="a688d-281">Method unfreedObjectIdent</span></span>

    public int unfreedObjectIdent()

#### <a name="return-value"></a><span data-ttu-id="a688d-282">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-282">Return Value</span></span>

### <a name="method-unfreedobjectusecount"></a><span data-ttu-id="a688d-283">メソッド unfreedObjectUseCount</span><span class="sxs-lookup"><span data-stu-id="a688d-283">Method unfreedObjectUseCount</span></span>

    public int unfreedObjectUseCount()

#### <a name="return-value"></a><span data-ttu-id="a688d-284">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-284">Return Value</span></span>

### <a name="method-version"></a><span data-ttu-id="a688d-285">メソッド version</span><span class="sxs-lookup"><span data-stu-id="a688d-285">Method version</span></span>

    public str version()

#### <a name="return-value"></a><span data-ttu-id="a688d-286">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-286">Return Value</span></span>

### <a name="method-checkheap"></a><span data-ttu-id="a688d-287">メソッド checkHeap</span><span class="sxs-lookup"><span data-stu-id="a688d-287">Method checkHeap</span></span>

    public void checkHeap(str Description, [int context], [int pool], [boolean detailed])

#### <a name="parameters"></a><span data-ttu-id="a688d-288">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-288">Parameters</span></span>

<span data-ttu-id="a688d-289">説明</span><span class="sxs-lookup"><span data-stu-id="a688d-289">Description</span></span>  

<!-- -->

<span data-ttu-id="a688d-290">context</span><span class="sxs-lookup"><span data-stu-id="a688d-290">context</span></span>  

<!-- -->

<span data-ttu-id="a688d-291">管理グループ</span><span class="sxs-lookup"><span data-stu-id="a688d-291">pool</span></span>  

<!-- -->

<span data-ttu-id="a688d-292">detailed</span><span class="sxs-lookup"><span data-stu-id="a688d-292">detailed</span></span>  

### <a name="method-shrinkpool"></a><span data-ttu-id="a688d-293">メソッド shrinkPool</span><span class="sxs-lookup"><span data-stu-id="a688d-293">Method shrinkPool</span></span>

    public void shrinkPool([int poolNo])

#### <a name="parameters"></a><span data-ttu-id="a688d-294">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-294">Parameters</span></span>

<span data-ttu-id="a688d-295">poolNo</span><span class="sxs-lookup"><span data-stu-id="a688d-295">poolNo</span></span>  

### <a name="method-postcompactingmessage"></a><span data-ttu-id="a688d-296">メソッド postCompactingMessage</span><span class="sxs-lookup"><span data-stu-id="a688d-296">Method postCompactingMessage</span></span>

    public void postCompactingMessage()

### <a name="method-checkheapdif"></a><span data-ttu-id="a688d-297">メソッド checkHeapDif</span><span class="sxs-lookup"><span data-stu-id="a688d-297">Method checkHeapDif</span></span>

    public void checkHeapDif(str Description, [int context], [int pool])

#### <a name="parameters"></a><span data-ttu-id="a688d-298">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-298">Parameters</span></span>

<span data-ttu-id="a688d-299">説明</span><span class="sxs-lookup"><span data-stu-id="a688d-299">Description</span></span>  

<!-- -->

<span data-ttu-id="a688d-300">context</span><span class="sxs-lookup"><span data-stu-id="a688d-300">context</span></span>  

<!-- -->

<span data-ttu-id="a688d-301">管理グループ</span><span class="sxs-lookup"><span data-stu-id="a688d-301">pool</span></span>  

### <a name="method-clearheapcontext"></a><span data-ttu-id="a688d-302">メソッド clearHeapContext</span><span class="sxs-lookup"><span data-stu-id="a688d-302">Method clearHeapContext</span></span>

    public void clearHeapContext()

### <a name="method-writestring"></a><span data-ttu-id="a688d-303">メソッド writeString</span><span class="sxs-lookup"><span data-stu-id="a688d-303">Method writeString</span></span>

    public void writeString(str text)

#### <a name="parameters"></a><span data-ttu-id="a688d-304">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-304">Parameters</span></span>

<span data-ttu-id="a688d-305">テキスト</span><span class="sxs-lookup"><span data-stu-id="a688d-305">text</span></span>  

### <a name="method-firstunfreedcursor"></a><span data-ttu-id="a688d-306">メソッド firstUnfreedCursor</span><span class="sxs-lookup"><span data-stu-id="a688d-306">Method firstUnfreedCursor</span></span>

    public void firstUnfreedCursor()

### <a name="method-dumpdgmlgraph"></a><span data-ttu-id="a688d-307">メソッド dumpDGMLGraph</span><span class="sxs-lookup"><span data-stu-id="a688d-307">Method dumpDGMLGraph</span></span>

    public void dumpDGMLGraph()

### <a name="method-firstunfreedobject"></a><span data-ttu-id="a688d-308">メソッド firstUnfreedObject</span><span class="sxs-lookup"><span data-stu-id="a688d-308">Method firstUnfreedObject</span></span>

    public void firstUnfreedObject()

### <a name="method-setheapcontext"></a><span data-ttu-id="a688d-309">メソッド setHeapContext</span><span class="sxs-lookup"><span data-stu-id="a688d-309">Method setHeapContext</span></span>

    public void setHeapContext(str description)

#### <a name="parameters"></a><span data-ttu-id="a688d-310">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-310">Parameters</span></span>

<span data-ttu-id="a688d-311">description</span><span class="sxs-lookup"><span data-stu-id="a688d-311">description</span></span>  

### <a name="method-new"></a><span data-ttu-id="a688d-312">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a688d-312">Method new</span></span>

<span data-ttu-id="a688d-313">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a688d-313">Initializes a new instance of the Object class.</span></span>

    public void new([str Filename])

#### <a name="parameters"></a><span data-ttu-id="a688d-314">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-314">Parameters</span></span>

<span data-ttu-id="a688d-315">ファイル名</span><span class="sxs-lookup"><span data-stu-id="a688d-315">Filename</span></span>  

### <a name="method-nextunfreedobject"></a><span data-ttu-id="a688d-316">メソッド nextUnfreedObject</span><span class="sxs-lookup"><span data-stu-id="a688d-316">Method nextUnfreedObject</span></span>

    public void nextUnfreedObject()

### <a name="method-checkheapstop"></a><span data-ttu-id="a688d-317">メソッド checkHeapStop</span><span class="sxs-lookup"><span data-stu-id="a688d-317">Method checkHeapStop</span></span>

    public void checkHeapStop()

### <a name="method-nextunfreedcursor"></a><span data-ttu-id="a688d-318">メソッド nextUnfreedCursor</span><span class="sxs-lookup"><span data-stu-id="a688d-318">Method nextUnfreedCursor</span></span>

    public void nextUnfreedCursor()

### <a name="method-setruntimebugcheckflags"></a><span data-ttu-id="a688d-319">メソッド setRuntimeBugcheckFlags</span><span class="sxs-lookup"><span data-stu-id="a688d-319">Method setRuntimeBugcheckFlags</span></span>

    public void setRuntimeBugcheckFlags(int flags)

#### <a name="parameters"></a><span data-ttu-id="a688d-320">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-320">Parameters</span></span>

<span data-ttu-id="a688d-321">flags</span><span class="sxs-lookup"><span data-stu-id="a688d-321">flags</span></span>  

### <a name="method-checkheapstart"></a><span data-ttu-id="a688d-322">メソッド checkHeapStart</span><span class="sxs-lookup"><span data-stu-id="a688d-322">Method checkHeapStart</span></span>

    public void checkHeapStart()

## <a name="class-helpdocsetnode"></a><span data-ttu-id="a688d-323">クラス HelpDocSetNode</span><span class="sxs-lookup"><span data-stu-id="a688d-323">Class HelpDocSetNode</span></span>
    class HelpDocSetNode extends TreeNode

### <a name="remarks"></a><span data-ttu-id="a688d-324">備考</span><span class="sxs-lookup"><span data-stu-id="a688d-324">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="a688d-325">例</span><span class="sxs-lookup"><span data-stu-id="a688d-325">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="a688d-326">メソッド</span><span class="sxs-lookup"><span data-stu-id="a688d-326">Methods</span></span>

| <span data-ttu-id="a688d-327">方法</span><span class="sxs-lookup"><span data-stu-id="a688d-327">Method</span></span>                                                     | <span data-ttu-id="a688d-328">説明</span><span class="sxs-lookup"><span data-stu-id="a688d-328">Description</span></span>                                                                |
|------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="a688d-329">public boolean addToApplicationHelpMenu(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a688d-329">public boolean addToApplicationHelpMenu(\[boolean value\])</span></span> |                                                                            |
| <span data-ttu-id="a688d-330">public boolean addToDeveloperHelpMenu(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a688d-330">public boolean addToDeveloperHelpMenu(\[boolean value\])</span></span>   |                                                                            |
| <span data-ttu-id="a688d-331">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a688d-331">public str changedBy(\[str value\])</span></span>                        | <span data-ttu-id="a688d-332">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a688d-332">Gets or sets the name of the user who last changed the application object.</span></span> |
| <span data-ttu-id="a688d-333">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="a688d-333">public Date changedDate(\[Date value\])</span></span>                    | <span data-ttu-id="a688d-334">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a688d-334">Gets or sets the date an application object was last changed.</span></span>              |
| <span data-ttu-id="a688d-335">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a688d-335">public str changedTime(\[str value\])</span></span>                      | <span data-ttu-id="a688d-336">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a688d-336">Gets or sets the time an application object was last changed.</span></span>              |
| <span data-ttu-id="a688d-337">public int contentLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a688d-337">public int contentLocation(\[int value\])</span></span>                  |                                                                            |
| <span data-ttu-id="a688d-338">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a688d-338">public str createdBy(\[str value\])</span></span>                        | <span data-ttu-id="a688d-339">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a688d-339">Gets or sets the name of the user who created the application object.</span></span>      |
| <span data-ttu-id="a688d-340">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="a688d-340">public Date creationDate(\[Date value\])</span></span>                   | <span data-ttu-id="a688d-341">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a688d-341">Gets or sets the date an application object was created.</span></span>                   |
| <span data-ttu-id="a688d-342">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a688d-342">public str creationTime(\[str value\])</span></span>                     |                                                                            |
| <span data-ttu-id="a688d-343">public boolean developerDocumentSet(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a688d-343">public boolean developerDocumentSet(\[boolean value\])</span></span>     |                                                                            |
| <span data-ttu-id="a688d-344">public str documentSetDescription(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a688d-344">public str documentSetDescription(\[str value\])</span></span>           |                                                                            |
| <span data-ttu-id="a688d-345">public str documentSetName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a688d-345">public str documentSetName(\[str value\])</span></span>                  |                                                                            |
| <span data-ttu-id="a688d-346">public str helpProviderClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a688d-346">public str helpProviderClass(\[str value\])</span></span>                |                                                                            |
| <span data-ttu-id="a688d-347">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="a688d-347">public Guid origin(\[Guid value\])</span></span>                         |                                                                            |
| <span data-ttu-id="a688d-348">public boolean userDocumentSet(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a688d-348">public boolean userDocumentSet(\[boolean value\])</span></span>          |                                                                            |
| <span data-ttu-id="a688d-349">public void new(str DocSetName)</span><span class="sxs-lookup"><span data-stu-id="a688d-349">public void new(str DocSetName)</span></span>                            | <span data-ttu-id="a688d-350">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a688d-350">Initializes a new instance of the TreeNode class.</span></span>                          |

### <a name="method-addtoapplicationhelpmenu"></a><span data-ttu-id="a688d-351">メソッド addToApplicationHelpMenu</span><span class="sxs-lookup"><span data-stu-id="a688d-351">Method addToApplicationHelpMenu</span></span>

    public boolean addToApplicationHelpMenu([boolean value])

#### <a name="parameters"></a><span data-ttu-id="a688d-352">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-352">Parameters</span></span>

<span data-ttu-id="a688d-353">値</span><span class="sxs-lookup"><span data-stu-id="a688d-353">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-354">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-354">Return Value</span></span>

### <a name="method-addtodeveloperhelpmenu"></a><span data-ttu-id="a688d-355">メソッド addToDeveloperHelpMenu</span><span class="sxs-lookup"><span data-stu-id="a688d-355">Method addToDeveloperHelpMenu</span></span>

    public boolean addToDeveloperHelpMenu([boolean value])

#### <a name="parameters"></a><span data-ttu-id="a688d-356">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-356">Parameters</span></span>

<span data-ttu-id="a688d-357">値</span><span class="sxs-lookup"><span data-stu-id="a688d-357">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-358">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-358">Return Value</span></span>

### <a name="method-changedby"></a><span data-ttu-id="a688d-359">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="a688d-359">Method changedBy</span></span>

<span data-ttu-id="a688d-360">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a688d-360">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="a688d-361">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-361">Parameters</span></span>

<span data-ttu-id="a688d-362">値</span><span class="sxs-lookup"><span data-stu-id="a688d-362">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-363">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-363">Return Value</span></span>

<span data-ttu-id="a688d-364">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="a688d-364">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="a688d-365">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="a688d-365">Method changedDate</span></span>

<span data-ttu-id="a688d-366">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a688d-366">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="a688d-367">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-367">Parameters</span></span>

<span data-ttu-id="a688d-368">値</span><span class="sxs-lookup"><span data-stu-id="a688d-368">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-369">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-369">Return Value</span></span>

<span data-ttu-id="a688d-370">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="a688d-370">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="a688d-371">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="a688d-371">Method changedTime</span></span>

<span data-ttu-id="a688d-372">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a688d-372">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="a688d-373">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-373">Parameters</span></span>

<span data-ttu-id="a688d-374">値</span><span class="sxs-lookup"><span data-stu-id="a688d-374">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-375">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-375">Return Value</span></span>

<span data-ttu-id="a688d-376">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="a688d-376">The time an application object was last changed.</span></span>

### <a name="method-contentlocation"></a><span data-ttu-id="a688d-377">メソッド contentLocation</span><span class="sxs-lookup"><span data-stu-id="a688d-377">Method contentLocation</span></span>

    public int contentLocation([int value])

#### <a name="parameters"></a><span data-ttu-id="a688d-378">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-378">Parameters</span></span>

<span data-ttu-id="a688d-379">値</span><span class="sxs-lookup"><span data-stu-id="a688d-379">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-380">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-380">Return Value</span></span>

### <a name="method-createdby"></a><span data-ttu-id="a688d-381">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="a688d-381">Method createdBy</span></span>

<span data-ttu-id="a688d-382">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a688d-382">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="a688d-383">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-383">Parameters</span></span>

<span data-ttu-id="a688d-384">値</span><span class="sxs-lookup"><span data-stu-id="a688d-384">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-385">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-385">Return Value</span></span>

<span data-ttu-id="a688d-386">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="a688d-386">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="a688d-387">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="a688d-387">Method creationDate</span></span>

<span data-ttu-id="a688d-388">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a688d-388">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="a688d-389">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-389">Parameters</span></span>

<span data-ttu-id="a688d-390">値</span><span class="sxs-lookup"><span data-stu-id="a688d-390">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-391">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-391">Return Value</span></span>

<span data-ttu-id="a688d-392">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="a688d-392">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="a688d-393">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="a688d-393">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="a688d-394">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-394">Parameters</span></span>

<span data-ttu-id="a688d-395">値</span><span class="sxs-lookup"><span data-stu-id="a688d-395">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-396">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-396">Return Value</span></span>

### <a name="method-developerdocumentset"></a><span data-ttu-id="a688d-397">メソッド developerDocumentSet</span><span class="sxs-lookup"><span data-stu-id="a688d-397">Method developerDocumentSet</span></span>

    public boolean developerDocumentSet([boolean value])

#### <a name="parameters"></a><span data-ttu-id="a688d-398">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-398">Parameters</span></span>

<span data-ttu-id="a688d-399">値</span><span class="sxs-lookup"><span data-stu-id="a688d-399">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-400">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-400">Return Value</span></span>

### <a name="method-documentsetdescription"></a><span data-ttu-id="a688d-401">メソッド documentSetDescription</span><span class="sxs-lookup"><span data-stu-id="a688d-401">Method documentSetDescription</span></span>

    public str documentSetDescription([str value])

#### <a name="parameters"></a><span data-ttu-id="a688d-402">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-402">Parameters</span></span>

<span data-ttu-id="a688d-403">値</span><span class="sxs-lookup"><span data-stu-id="a688d-403">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-404">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-404">Return Value</span></span>

### <a name="method-documentsetname"></a><span data-ttu-id="a688d-405">メソッド documentSetName</span><span class="sxs-lookup"><span data-stu-id="a688d-405">Method documentSetName</span></span>

    public str documentSetName([str value])

#### <a name="parameters"></a><span data-ttu-id="a688d-406">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-406">Parameters</span></span>

<span data-ttu-id="a688d-407">値</span><span class="sxs-lookup"><span data-stu-id="a688d-407">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-408">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-408">Return Value</span></span>

### <a name="method-helpproviderclass"></a><span data-ttu-id="a688d-409">メソッド helpProviderClass</span><span class="sxs-lookup"><span data-stu-id="a688d-409">Method helpProviderClass</span></span>

    public str helpProviderClass([str value])

#### <a name="parameters"></a><span data-ttu-id="a688d-410">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-410">Parameters</span></span>

<span data-ttu-id="a688d-411">値</span><span class="sxs-lookup"><span data-stu-id="a688d-411">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-412">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-412">Return Value</span></span>

### <a name="method-origin"></a><span data-ttu-id="a688d-413">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="a688d-413">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="a688d-414">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-414">Parameters</span></span>

<span data-ttu-id="a688d-415">値</span><span class="sxs-lookup"><span data-stu-id="a688d-415">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-416">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-416">Return Value</span></span>

### <a name="method-userdocumentset"></a><span data-ttu-id="a688d-417">メソッド userDocumentSet</span><span class="sxs-lookup"><span data-stu-id="a688d-417">Method userDocumentSet</span></span>

    public boolean userDocumentSet([boolean value])

#### <a name="parameters"></a><span data-ttu-id="a688d-418">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-418">Parameters</span></span>

<span data-ttu-id="a688d-419">値</span><span class="sxs-lookup"><span data-stu-id="a688d-419">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-420">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-420">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="a688d-421">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a688d-421">Method new</span></span>

<span data-ttu-id="a688d-422">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a688d-422">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str DocSetName)

#### <a name="parameters"></a><span data-ttu-id="a688d-423">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-423">Parameters</span></span>

<span data-ttu-id="a688d-424">DocSetName</span><span class="sxs-lookup"><span data-stu-id="a688d-424">DocSetName</span></span>  

## <a name="class-helpdocumentmanager"></a><span data-ttu-id="a688d-425">クラス HelpDocumentManager</span><span class="sxs-lookup"><span data-stu-id="a688d-425">Class HelpDocumentManager</span></span>
    class HelpDocumentManager extends Object

### <a name="remarks"></a><span data-ttu-id="a688d-426">備考</span><span class="sxs-lookup"><span data-stu-id="a688d-426">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="a688d-427">例</span><span class="sxs-lookup"><span data-stu-id="a688d-427">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="a688d-428">メソッド</span><span class="sxs-lookup"><span data-stu-id="a688d-428">Methods</span></span>

| <span data-ttu-id="a688d-429">方法</span><span class="sxs-lookup"><span data-stu-id="a688d-429">Method</span></span>                                                                                                              | <span data-ttu-id="a688d-430">説明</span><span class="sxs-lookup"><span data-stu-id="a688d-430">Description</span></span>                                                  |
|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="a688d-431">public void new()</span><span class="sxs-lookup"><span data-stu-id="a688d-431">public void new()</span></span>                                                                                                   | <span data-ttu-id="a688d-432">HelpDocumentManager クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a688d-432">Initializes a new instance of the HelpDocumentManager class.</span></span> |
| <span data-ttu-id="a688d-433">::public static void showHelpTopic(\[str topic\], \[str documentSet\], \[str contentLanguage\], \[str uiLanguage\])</span><span class="sxs-lookup"><span data-stu-id="a688d-433">::public static void showHelpTopic(\[str topic\], \[str documentSet\], \[str contentLanguage\], \[str uiLanguage\])</span></span> |                                                              |
| <span data-ttu-id="a688d-434">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="a688d-434">public void finalize()</span></span>                                                                                              |                                                              |

### <a name="method-new"></a><span data-ttu-id="a688d-435">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a688d-435">Method new</span></span>

<span data-ttu-id="a688d-436">HelpDocumentManager クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a688d-436">Initializes a new instance of the HelpDocumentManager class.</span></span>

    public void new()

### <a name="method-showhelptopic"></a><span data-ttu-id="a688d-437">メソッド showHelpTopic</span><span class="sxs-lookup"><span data-stu-id="a688d-437">Method showHelpTopic</span></span>

    public static void showHelpTopic([str topic], [str documentSet], [str contentLanguage], [str uiLanguage])

#### <a name="parameters"></a><span data-ttu-id="a688d-438">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-438">Parameters</span></span>

<span data-ttu-id="a688d-439">トピック</span><span class="sxs-lookup"><span data-stu-id="a688d-439">topic</span></span>  

<!-- -->

<span data-ttu-id="a688d-440">documentSet</span><span class="sxs-lookup"><span data-stu-id="a688d-440">documentSet</span></span>  

<!-- -->

<span data-ttu-id="a688d-441">contentLanguage</span><span class="sxs-lookup"><span data-stu-id="a688d-441">contentLanguage</span></span>  

<!-- -->

<span data-ttu-id="a688d-442">uiLanguage</span><span class="sxs-lookup"><span data-stu-id="a688d-442">uiLanguage</span></span>  

### <a name="method-finalize"></a><span data-ttu-id="a688d-443">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="a688d-443">Method finalize</span></span>

    public void finalize()

## <a name="class-htmlfont"></a><span data-ttu-id="a688d-444">クラス HtmlFont</span><span class="sxs-lookup"><span data-stu-id="a688d-444">Class HtmlFont</span></span>
    class HtmlFont extends Object

### <a name="remarks"></a><span data-ttu-id="a688d-445">備考</span><span class="sxs-lookup"><span data-stu-id="a688d-445">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="a688d-446">例</span><span class="sxs-lookup"><span data-stu-id="a688d-446">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="a688d-447">メソッド</span><span class="sxs-lookup"><span data-stu-id="a688d-447">Methods</span></span>

| <span data-ttu-id="a688d-448">方法</span><span class="sxs-lookup"><span data-stu-id="a688d-448">Method</span></span>                                                                                                    | <span data-ttu-id="a688d-449">説明</span><span class="sxs-lookup"><span data-stu-id="a688d-449">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="a688d-450">public int backColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a688d-450">public int backColor(\[int value\])</span></span>                                                                       |                                                 |
| <span data-ttu-id="a688d-451">public str fontName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a688d-451">public str fontName(\[str value\])</span></span>                                                                        |                                                 |
| <span data-ttu-id="a688d-452">public int pointSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a688d-452">public int pointSize(\[int value\])</span></span>                                                                       |                                                 |
| <span data-ttu-id="a688d-453">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a688d-453">public int style(\[int value\])</span></span>                                                                           |                                                 |
| <span data-ttu-id="a688d-454">public int textColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a688d-454">public int textColor(\[int value\])</span></span>                                                                       |                                                 |
| <span data-ttu-id="a688d-455">public void new(\[str TypeFace\], \[int PointSize\], \[int Style\], \[int TextColor\], \[int BackColor\])</span><span class="sxs-lookup"><span data-stu-id="a688d-455">public void new(\[str TypeFace\], \[int PointSize\], \[int Style\], \[int TextColor\], \[int BackColor\])</span></span> | <span data-ttu-id="a688d-456">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a688d-456">Initializes a new instance of the Object class.</span></span> |
| <span data-ttu-id="a688d-457">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="a688d-457">public void finalize()</span></span>                                                                                    |                                                 |

### <a name="method-backcolor"></a><span data-ttu-id="a688d-458">メソッド backColor</span><span class="sxs-lookup"><span data-stu-id="a688d-458">Method backColor</span></span>

    public int backColor([int value])

#### <a name="parameters"></a><span data-ttu-id="a688d-459">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-459">Parameters</span></span>

<span data-ttu-id="a688d-460">値</span><span class="sxs-lookup"><span data-stu-id="a688d-460">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-461">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-461">Return Value</span></span>

### <a name="method-fontname"></a><span data-ttu-id="a688d-462">メソッド fontName</span><span class="sxs-lookup"><span data-stu-id="a688d-462">Method fontName</span></span>

    public str fontName([str value])

#### <a name="parameters"></a><span data-ttu-id="a688d-463">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-463">Parameters</span></span>

<span data-ttu-id="a688d-464">値</span><span class="sxs-lookup"><span data-stu-id="a688d-464">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-465">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-465">Return Value</span></span>

### <a name="method-pointsize"></a><span data-ttu-id="a688d-466">メソッド pointSize</span><span class="sxs-lookup"><span data-stu-id="a688d-466">Method pointSize</span></span>

    public int pointSize([int value])

#### <a name="parameters"></a><span data-ttu-id="a688d-467">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-467">Parameters</span></span>

<span data-ttu-id="a688d-468">値</span><span class="sxs-lookup"><span data-stu-id="a688d-468">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-469">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-469">Return Value</span></span>

### <a name="method-style"></a><span data-ttu-id="a688d-470">メソッド style</span><span class="sxs-lookup"><span data-stu-id="a688d-470">Method style</span></span>

    public int style([int value])

#### <a name="parameters"></a><span data-ttu-id="a688d-471">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-471">Parameters</span></span>

<span data-ttu-id="a688d-472">値</span><span class="sxs-lookup"><span data-stu-id="a688d-472">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-473">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-473">Return Value</span></span>

### <a name="method-textcolor"></a><span data-ttu-id="a688d-474">メソッド textColor</span><span class="sxs-lookup"><span data-stu-id="a688d-474">Method textColor</span></span>

    public int textColor([int value])

#### <a name="parameters"></a><span data-ttu-id="a688d-475">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-475">Parameters</span></span>

<span data-ttu-id="a688d-476">値</span><span class="sxs-lookup"><span data-stu-id="a688d-476">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="a688d-477">戻り値</span><span class="sxs-lookup"><span data-stu-id="a688d-477">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="a688d-478">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a688d-478">Method new</span></span>

<span data-ttu-id="a688d-479">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a688d-479">Initializes a new instance of the Object class.</span></span>

    public void new([str TypeFace], [int PointSize], [int Style], [int TextColor], [int BackColor])

#### <a name="parameters"></a><span data-ttu-id="a688d-480">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a688d-480">Parameters</span></span>

<span data-ttu-id="a688d-481">TypeFace</span><span class="sxs-lookup"><span data-stu-id="a688d-481">TypeFace</span></span>  

<!-- -->

<span data-ttu-id="a688d-482">PointSize</span><span class="sxs-lookup"><span data-stu-id="a688d-482">PointSize</span></span>  

<!-- -->

<span data-ttu-id="a688d-483">スタイル</span><span class="sxs-lookup"><span data-stu-id="a688d-483">Style</span></span>  

<!-- -->

<span data-ttu-id="a688d-484">TextColor</span><span class="sxs-lookup"><span data-stu-id="a688d-484">TextColor</span></span>  

<!-- -->

<span data-ttu-id="a688d-485">BackColor</span><span class="sxs-lookup"><span data-stu-id="a688d-485">BackColor</span></span>  

### <a name="method-finalize"></a><span data-ttu-id="a688d-486">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="a688d-486">Method finalize</span></span>

    public void finalize()



