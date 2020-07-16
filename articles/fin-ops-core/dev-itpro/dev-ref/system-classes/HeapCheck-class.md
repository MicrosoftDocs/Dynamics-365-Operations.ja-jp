---
title: HeapCheck クラス
description: このトピックでは、HeapCheck クラスについて説明します。
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
ms.openlocfilehash: a5afbaf81b574959b19e4f48a527fe5b75d0be53
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502611"
---
# <a name="class-heapcheck"></a><span data-ttu-id="e9cf3-103">クラス HeapCheck</span><span class="sxs-lookup"><span data-stu-id="e9cf3-103">Class HeapCheck</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class HeapCheck extends Object
```

## <a name="remarks"></a><span data-ttu-id="e9cf3-104">備考</span><span class="sxs-lookup"><span data-stu-id="e9cf3-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="e9cf3-105">例</span><span class="sxs-lookup"><span data-stu-id="e9cf3-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="e9cf3-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="e9cf3-106">Methods</span></span>

| <span data-ttu-id="e9cf3-107">方法</span><span class="sxs-lookup"><span data-stu-id="e9cf3-107">Method</span></span>                                                                                      | <span data-ttu-id="e9cf3-108">説明</span><span class="sxs-lookup"><span data-stu-id="e9cf3-108">Description</span></span>                                     |
|---------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="e9cf3-109">public int accessCnt()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-109">public int accessCnt()</span></span>                                                                      |                                                 |
| <span data-ttu-id="e9cf3-110">public int addRefCnt()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-110">public int addRefCnt()</span></span>                                                                      |                                                 |
| <span data-ttu-id="e9cf3-111">public Int64 blocksAllocated(\[int pool\])</span><span class="sxs-lookup"><span data-stu-id="e9cf3-111">public Int64 blocksAllocated(\[int pool\])</span></span>                                                  |                                                 |
| <span data-ttu-id="e9cf3-112">public int breakCount(\[int count\])</span><span class="sxs-lookup"><span data-stu-id="e9cf3-112">public int breakCount(\[int count\])</span></span>                                                        |                                                 |
| <span data-ttu-id="e9cf3-113">public Int64 bytesAllocated(\[int pool\])</span><span class="sxs-lookup"><span data-stu-id="e9cf3-113">public Int64 bytesAllocated(\[int pool\])</span></span>                                                   |                                                 |
| <span data-ttu-id="e9cf3-114">public Int64 ceiling(int pool, \[int ceiling\])</span><span class="sxs-lookup"><span data-stu-id="e9cf3-114">public Int64 ceiling(int pool, \[int ceiling\])</span></span>                                             |                                                 |
| <span data-ttu-id="e9cf3-115">public int context(\[int context\])</span><span class="sxs-lookup"><span data-stu-id="e9cf3-115">public int context(\[int context\])</span></span>                                                         |                                                 |
| <span data-ttu-id="e9cf3-116">public int count(\[int count\])</span><span class="sxs-lookup"><span data-stu-id="e9cf3-116">public int count(\[int count\])</span></span>                                                             |                                                 |
| <span data-ttu-id="e9cf3-117">public int countObjects(int classId)</span><span class="sxs-lookup"><span data-stu-id="e9cf3-117">public int countObjects(int classId)</span></span>                                                        |                                                 |
| <span data-ttu-id="e9cf3-118">public container createAContainer()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-118">public container createAContainer()</span></span>                                                         |                                                 |
| <span data-ttu-id="e9cf3-119">public int csCallCnt()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-119">public int csCallCnt()</span></span>                                                                      |                                                 |
| <span data-ttu-id="e9cf3-120">public int csSweepCnt()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-120">public int csSweepCnt()</span></span>                                                                     |                                                 |
| <span data-ttu-id="e9cf3-121">public container dataByContext(\[int poolNo\], \[int context\])</span><span class="sxs-lookup"><span data-stu-id="e9cf3-121">public container dataByContext(\[int poolNo\], \[int context\])</span></span>                             |                                                 |
| <span data-ttu-id="e9cf3-122">public int dumpCursors()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-122">public int dumpCursors()</span></span>                                                                    |                                                 |
| <span data-ttu-id="e9cf3-123">public int dumpObjects()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-123">public int dumpObjects()</span></span>                                                                    |                                                 |
| <span data-ttu-id="e9cf3-124">public int filename(\[str filename\])</span><span class="sxs-lookup"><span data-stu-id="e9cf3-124">public int filename(\[str filename\])</span></span>                                                       |                                                 |
| <span data-ttu-id="e9cf3-125">public int fixedBlockSize(int pool, \[int blockSize\])</span><span class="sxs-lookup"><span data-stu-id="e9cf3-125">public int fixedBlockSize(int pool, \[int blockSize\])</span></span>                                      |                                                 |
| <span data-ttu-id="e9cf3-126">public int floor(int pool, \[int floor\])</span><span class="sxs-lookup"><span data-stu-id="e9cf3-126">public int floor(int pool, \[int floor\])</span></span>                                                   |                                                 |
| <span data-ttu-id="e9cf3-127">public int freeRefCnt()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-127">public int freeRefCnt()</span></span>                                                                     |                                                 |
| <span data-ttu-id="e9cf3-128">public int getRuntimeBugcheckFlags()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-128">public int getRuntimeBugcheckFlags()</span></span>                                                        |                                                 |
| <span data-ttu-id="e9cf3-129">public Common getUnfreedCursor()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-129">public Common getUnfreedCursor()</span></span>                                                            |                                                 |
| <span data-ttu-id="e9cf3-130">public Common getUnfreedObject()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-130">public Common getUnfreedObject()</span></span>                                                            |                                                 |
| <span data-ttu-id="e9cf3-131">public boolean include(int objectNo, \[boolean include\])</span><span class="sxs-lookup"><span data-stu-id="e9cf3-131">public boolean include(int objectNo, \[boolean include\])</span></span>                                   |                                                 |
| <span data-ttu-id="e9cf3-132">public boolean moreUnfreedCursors()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-132">public boolean moreUnfreedCursors()</span></span>                                                         |                                                 |
| <span data-ttu-id="e9cf3-133">public boolean moreUnfreedObjects()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-133">public boolean moreUnfreedObjects()</span></span>                                                         |                                                 |
| <span data-ttu-id="e9cf3-134">public int objectContext(int objNo, \[int context\])</span><span class="sxs-lookup"><span data-stu-id="e9cf3-134">public int objectContext(int objNo, \[int context\])</span></span>                                        |                                                 |
| <span data-ttu-id="e9cf3-135">public int pageSize(int pool, \[int pageSize\])</span><span class="sxs-lookup"><span data-stu-id="e9cf3-135">public int pageSize(int pool, \[int pageSize\])</span></span>                                             |                                                 |
| <span data-ttu-id="e9cf3-136">public int poolCount()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-136">public int poolCount()</span></span>                                                                      |                                                 |
| <span data-ttu-id="e9cf3-137">public str poolName(int poolNo)</span><span class="sxs-lookup"><span data-stu-id="e9cf3-137">public str poolName(int poolNo)</span></span>                                                             |                                                 |
| <span data-ttu-id="e9cf3-138">public int smallBlockSize(int pool, \[int blockSize\])</span><span class="sxs-lookup"><span data-stu-id="e9cf3-138">public int smallBlockSize(int pool, \[int blockSize\])</span></span>                                      |                                                 |
| <span data-ttu-id="e9cf3-139">public int sweepCnt()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-139">public int sweepCnt()</span></span>                                                                       |                                                 |
| <span data-ttu-id="e9cf3-140">public int testBlocks(\[int arg1\])</span><span class="sxs-lookup"><span data-stu-id="e9cf3-140">public int testBlocks(\[int arg1\])</span></span>                                                         |                                                 |
| <span data-ttu-id="e9cf3-141">public str unfreedObjectClass()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-141">public str unfreedObjectClass()</span></span>                                                             |                                                 |
| <span data-ttu-id="e9cf3-142">public boolean unfreedObjectClient()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-142">public boolean unfreedObjectClient()</span></span>                                                        |                                                 |
| <span data-ttu-id="e9cf3-143">public boolean unfreedObjectFinalized()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-143">public boolean unfreedObjectFinalized()</span></span>                                                     |                                                 |
| <span data-ttu-id="e9cf3-144">public int unfreedObjectHandle()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-144">public int unfreedObjectHandle()</span></span>                                                            |                                                 |
| <span data-ttu-id="e9cf3-145">public int unfreedObjectIdent()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-145">public int unfreedObjectIdent()</span></span>                                                             |                                                 |
| <span data-ttu-id="e9cf3-146">public int unfreedObjectUseCount()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-146">public int unfreedObjectUseCount()</span></span>                                                          |                                                 |
| <span data-ttu-id="e9cf3-147">public str version()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-147">public str version()</span></span>                                                                        |                                                 |
| <span data-ttu-id="e9cf3-148">public void checkHeap(str Description, \[int context\], \[int pool\], \[boolean detailed\])</span><span class="sxs-lookup"><span data-stu-id="e9cf3-148">public void checkHeap(str Description, \[int context\], \[int pool\], \[boolean detailed\])</span></span> |                                                 |
| <span data-ttu-id="e9cf3-149">public void shrinkPool(\[int poolNo\])</span><span class="sxs-lookup"><span data-stu-id="e9cf3-149">public void shrinkPool(\[int poolNo\])</span></span>                                                      |                                                 |
| <span data-ttu-id="e9cf3-150">public void postCompactingMessage()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-150">public void postCompactingMessage()</span></span>                                                         |                                                 |
| <span data-ttu-id="e9cf3-151">public void checkHeapDif(str Description, \[int context\], \[int pool\])</span><span class="sxs-lookup"><span data-stu-id="e9cf3-151">public void checkHeapDif(str Description, \[int context\], \[int pool\])</span></span>                    |                                                 |
| <span data-ttu-id="e9cf3-152">public void clearHeapContext()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-152">public void clearHeapContext()</span></span>                                                              |                                                 |
| <span data-ttu-id="e9cf3-153">public void writeString(str text)</span><span class="sxs-lookup"><span data-stu-id="e9cf3-153">public void writeString(str text)</span></span>                                                           |                                                 |
| <span data-ttu-id="e9cf3-154">public void firstUnfreedCursor()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-154">public void firstUnfreedCursor()</span></span>                                                            |                                                 |
| <span data-ttu-id="e9cf3-155">public void dumpDGMLGraph()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-155">public void dumpDGMLGraph()</span></span>                                                                 |                                                 |
| <span data-ttu-id="e9cf3-156">public void firstUnfreedObject()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-156">public void firstUnfreedObject()</span></span>                                                            |                                                 |
| <span data-ttu-id="e9cf3-157">public void setHeapContext(str description)</span><span class="sxs-lookup"><span data-stu-id="e9cf3-157">public void setHeapContext(str description)</span></span>                                                 |                                                 |
| <span data-ttu-id="e9cf3-158">public void new(\[str Filename\])</span><span class="sxs-lookup"><span data-stu-id="e9cf3-158">public void new(\[str Filename\])</span></span>                                                           | <span data-ttu-id="e9cf3-159">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e9cf3-159">Initializes a new instance of the Object class.</span></span> |
| <span data-ttu-id="e9cf3-160">public void nextUnfreedObject()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-160">public void nextUnfreedObject()</span></span>                                                             |                                                 |
| <span data-ttu-id="e9cf3-161">public void checkHeapStop()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-161">public void checkHeapStop()</span></span>                                                                 |                                                 |
| <span data-ttu-id="e9cf3-162">public void nextUnfreedCursor()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-162">public void nextUnfreedCursor()</span></span>                                                             |                                                 |
| <span data-ttu-id="e9cf3-163">public void setRuntimeBugcheckFlags(int flags)</span><span class="sxs-lookup"><span data-stu-id="e9cf3-163">public void setRuntimeBugcheckFlags(int flags)</span></span>                                              |                                                 |
| <span data-ttu-id="e9cf3-164">public void checkHeapStart()</span><span class="sxs-lookup"><span data-stu-id="e9cf3-164">public void checkHeapStart()</span></span>                                                                |                                                 |

## <a name="method-accesscnt"></a><span data-ttu-id="e9cf3-165">メソッド accessCnt</span><span class="sxs-lookup"><span data-stu-id="e9cf3-165">Method accessCnt</span></span>

```xpp
public int accessCnt()
```

### <a name="return-value---accesscnt"></a><span data-ttu-id="e9cf3-166">戻り値 - accessCnt</span><span class="sxs-lookup"><span data-stu-id="e9cf3-166">Return Value - accessCnt</span></span>

## <a name="method-addrefcnt"></a><span data-ttu-id="e9cf3-167">メソッド addRefCnt</span><span class="sxs-lookup"><span data-stu-id="e9cf3-167">Method addRefCnt</span></span>

```xpp
public int addRefCnt()
```

### <a name="return-value---addrefcnt"></a><span data-ttu-id="e9cf3-168">戻り値 - addRefCnt</span><span class="sxs-lookup"><span data-stu-id="e9cf3-168">Return Value - addRefCnt</span></span>

## <a name="method-blocksallocated"></a><span data-ttu-id="e9cf3-169">メソッド blocksAllocated</span><span class="sxs-lookup"><span data-stu-id="e9cf3-169">Method blocksAllocated</span></span>

```xpp
public Int64 blocksAllocated([int pool])
```

### <a name="parameters---blocksallocated"></a><span data-ttu-id="e9cf3-170">パラメーター - blocksAllocated</span><span class="sxs-lookup"><span data-stu-id="e9cf3-170">Parameters - blocksAllocated</span></span>

<span data-ttu-id="e9cf3-171">管理グループ</span><span class="sxs-lookup"><span data-stu-id="e9cf3-171">pool</span></span>  

### <a name="return-value---blocksallocated"></a><span data-ttu-id="e9cf3-172">戻り値 - blocksAllocated</span><span class="sxs-lookup"><span data-stu-id="e9cf3-172">Return Value - blocksAllocated</span></span>

## <a name="method-breakcount"></a><span data-ttu-id="e9cf3-173">メソッド breakCount</span><span class="sxs-lookup"><span data-stu-id="e9cf3-173">Method breakCount</span></span>

```xpp
public int breakCount([int count])
```

### <a name="parameters---breakcount"></a><span data-ttu-id="e9cf3-174">パラメーター - breakCount</span><span class="sxs-lookup"><span data-stu-id="e9cf3-174">Parameters - breakCount</span></span>

<span data-ttu-id="e9cf3-175">カウント</span><span class="sxs-lookup"><span data-stu-id="e9cf3-175">count</span></span>  

### <a name="return-value---breakcount"></a><span data-ttu-id="e9cf3-176">戻り値 - breakCount</span><span class="sxs-lookup"><span data-stu-id="e9cf3-176">Return Value - breakCount</span></span>

## <a name="method-bytesallocated"></a><span data-ttu-id="e9cf3-177">メソッド bytesAllocated</span><span class="sxs-lookup"><span data-stu-id="e9cf3-177">Method bytesAllocated</span></span>

```xpp
public Int64 bytesAllocated([int pool])
```

### <a name="parameters---bytesallocated"></a><span data-ttu-id="e9cf3-178">パラメーター - bytesAllocated</span><span class="sxs-lookup"><span data-stu-id="e9cf3-178">Parameters - bytesAllocated</span></span>

<span data-ttu-id="e9cf3-179">管理グループ</span><span class="sxs-lookup"><span data-stu-id="e9cf3-179">pool</span></span>  

### <a name="return-value---bytesallocated"></a><span data-ttu-id="e9cf3-180">戻り値 - bytesAllocated</span><span class="sxs-lookup"><span data-stu-id="e9cf3-180">Return Value - bytesAllocated</span></span>

## <a name="method-ceiling"></a><span data-ttu-id="e9cf3-181">メソッド ceiling</span><span class="sxs-lookup"><span data-stu-id="e9cf3-181">Method ceiling</span></span>

```xpp
public Int64 ceiling(int pool, [int ceiling])
```

### <a name="parameters---ceiling"></a><span data-ttu-id="e9cf3-182">パラメーター - ceiling</span><span class="sxs-lookup"><span data-stu-id="e9cf3-182">Parameters - ceiling</span></span>

<span data-ttu-id="e9cf3-183">管理グループ</span><span class="sxs-lookup"><span data-stu-id="e9cf3-183">pool</span></span>  

<!-- -->

<span data-ttu-id="e9cf3-184">ceiling</span><span class="sxs-lookup"><span data-stu-id="e9cf3-184">ceiling</span></span>  

### <a name="return-value---ceiling"></a><span data-ttu-id="e9cf3-185">戻り値 - ceiling</span><span class="sxs-lookup"><span data-stu-id="e9cf3-185">Return Value - ceiling</span></span>

## <a name="method-context"></a><span data-ttu-id="e9cf3-186">メソッド context</span><span class="sxs-lookup"><span data-stu-id="e9cf3-186">Method context</span></span>

```xpp
public int context([int context])
```

### <a name="parameters---context"></a><span data-ttu-id="e9cf3-187">パラメーター - context</span><span class="sxs-lookup"><span data-stu-id="e9cf3-187">Parameters - context</span></span>

<span data-ttu-id="e9cf3-188">context</span><span class="sxs-lookup"><span data-stu-id="e9cf3-188">context</span></span>  

### <a name="return-value---context"></a><span data-ttu-id="e9cf3-189">戻り値 - context</span><span class="sxs-lookup"><span data-stu-id="e9cf3-189">Return Value - context</span></span>

## <a name="method-count"></a><span data-ttu-id="e9cf3-190">メソッド count</span><span class="sxs-lookup"><span data-stu-id="e9cf3-190">Method count</span></span>

```xpp
public int count([int count])
```

### <a name="parameters---count"></a><span data-ttu-id="e9cf3-191">パラメーター - count</span><span class="sxs-lookup"><span data-stu-id="e9cf3-191">Parameters - count</span></span>

<span data-ttu-id="e9cf3-192">カウント</span><span class="sxs-lookup"><span data-stu-id="e9cf3-192">count</span></span>  

### <a name="return-value---count"></a><span data-ttu-id="e9cf3-193">戻り値 - count</span><span class="sxs-lookup"><span data-stu-id="e9cf3-193">Return Value - count</span></span>

## <a name="method-countobjects"></a><span data-ttu-id="e9cf3-194">メソッド countObjects</span><span class="sxs-lookup"><span data-stu-id="e9cf3-194">Method countObjects</span></span>

```xpp
public int countObjects(int classId)
```

### <a name="parameters---countobjects"></a><span data-ttu-id="e9cf3-195">パラメーター - countObjects</span><span class="sxs-lookup"><span data-stu-id="e9cf3-195">Parameters - countObjects</span></span>

<span data-ttu-id="e9cf3-196">classId</span><span class="sxs-lookup"><span data-stu-id="e9cf3-196">classId</span></span>  

### <a name="return-value---countobjects"></a><span data-ttu-id="e9cf3-197">戻り値 - countObjects</span><span class="sxs-lookup"><span data-stu-id="e9cf3-197">Return Value - countObjects</span></span>

## <a name="method-createacontainer"></a><span data-ttu-id="e9cf3-198">メソッド createAContainer</span><span class="sxs-lookup"><span data-stu-id="e9cf3-198">Method createAContainer</span></span>

```xpp
public container createAContainer()
```

### <a name="return-value---createacontainer"></a><span data-ttu-id="e9cf3-199">戻り値 - createAContainer</span><span class="sxs-lookup"><span data-stu-id="e9cf3-199">Return Value - createAContainer</span></span>

## <a name="method-cscallcnt"></a><span data-ttu-id="e9cf3-200">メソッド csCallCnt</span><span class="sxs-lookup"><span data-stu-id="e9cf3-200">Method csCallCnt</span></span>

```xpp
public int csCallCnt()
```

### <a name="return-value---cscallcnt"></a><span data-ttu-id="e9cf3-201">戻り値 - csCallCnt</span><span class="sxs-lookup"><span data-stu-id="e9cf3-201">Return Value - csCallCnt</span></span>

## <a name="method-cssweepcnt"></a><span data-ttu-id="e9cf3-202">メソッド csSweepCnt</span><span class="sxs-lookup"><span data-stu-id="e9cf3-202">Method csSweepCnt</span></span>

```xpp
public int csSweepCnt()
```

### <a name="return-value---cssweepcnt"></a><span data-ttu-id="e9cf3-203">戻り値 - csSweepCnt</span><span class="sxs-lookup"><span data-stu-id="e9cf3-203">Return Value - csSweepCnt</span></span>

## <a name="method-databycontext"></a><span data-ttu-id="e9cf3-204">メソッド dataByContext</span><span class="sxs-lookup"><span data-stu-id="e9cf3-204">Method dataByContext</span></span>

```xpp
public container dataByContext([int poolNo], [int context])
```

### <a name="parameters---databycontext"></a><span data-ttu-id="e9cf3-205">パラメーター - dataByContext</span><span class="sxs-lookup"><span data-stu-id="e9cf3-205">Parameters - dataByContext</span></span>

<span data-ttu-id="e9cf3-206">poolNo</span><span class="sxs-lookup"><span data-stu-id="e9cf3-206">poolNo</span></span>  

<!-- -->

<span data-ttu-id="e9cf3-207">context</span><span class="sxs-lookup"><span data-stu-id="e9cf3-207">context</span></span>  

### <a name="return-value---databycontext"></a><span data-ttu-id="e9cf3-208">戻り値 - dataByContext</span><span class="sxs-lookup"><span data-stu-id="e9cf3-208">Return Value - dataByContext</span></span>

## <a name="method-dumpcursors"></a><span data-ttu-id="e9cf3-209">メソッド dumpCursors</span><span class="sxs-lookup"><span data-stu-id="e9cf3-209">Method dumpCursors</span></span>

```xpp
public int dumpCursors()
```

### <a name="return-value---dumpcursors"></a><span data-ttu-id="e9cf3-210">戻り値 - dumpCursors</span><span class="sxs-lookup"><span data-stu-id="e9cf3-210">Return Value - dumpCursors</span></span>

## <a name="method-dumpobjects"></a><span data-ttu-id="e9cf3-211">メソッド dumpObjects</span><span class="sxs-lookup"><span data-stu-id="e9cf3-211">Method dumpObjects</span></span>

```xpp
public int dumpObjects()
```

### <a name="return-value---dumpobjects"></a><span data-ttu-id="e9cf3-212">戻り値 - dumpObjects</span><span class="sxs-lookup"><span data-stu-id="e9cf3-212">Return Value - dumpObjects</span></span>

## <a name="method-filename"></a><span data-ttu-id="e9cf3-213">メソッド filename</span><span class="sxs-lookup"><span data-stu-id="e9cf3-213">Method filename</span></span>

```xpp
public int filename([str filename])
```

### <a name="parameters---filename"></a><span data-ttu-id="e9cf3-214">パラメーター - filename</span><span class="sxs-lookup"><span data-stu-id="e9cf3-214">Parameters - filename</span></span>

<span data-ttu-id="e9cf3-215">filename</span><span class="sxs-lookup"><span data-stu-id="e9cf3-215">filename</span></span>  

### <a name="return-value---filename"></a><span data-ttu-id="e9cf3-216">戻り値 - filename</span><span class="sxs-lookup"><span data-stu-id="e9cf3-216">Return Value - filename</span></span>

## <a name="method-fixedblocksize"></a><span data-ttu-id="e9cf3-217">メソッド fixedBlockSize</span><span class="sxs-lookup"><span data-stu-id="e9cf3-217">Method fixedBlockSize</span></span>

```xpp
public int fixedBlockSize(int pool, [int blockSize])
```

### <a name="parameters---fixedblocksize"></a><span data-ttu-id="e9cf3-218">パラメーター - fixedBlockSize</span><span class="sxs-lookup"><span data-stu-id="e9cf3-218">Parameters - fixedBlockSize</span></span>

<span data-ttu-id="e9cf3-219">管理グループ</span><span class="sxs-lookup"><span data-stu-id="e9cf3-219">pool</span></span>  

<!-- -->

<span data-ttu-id="e9cf3-220">blockSize</span><span class="sxs-lookup"><span data-stu-id="e9cf3-220">blockSize</span></span>  

### <a name="return-value---fixedblocksize"></a><span data-ttu-id="e9cf3-221">戻り値 - fixedBlockSize</span><span class="sxs-lookup"><span data-stu-id="e9cf3-221">Return Value - fixedBlockSize</span></span>

## <a name="method-floor"></a><span data-ttu-id="e9cf3-222">メソッド floor</span><span class="sxs-lookup"><span data-stu-id="e9cf3-222">Method floor</span></span>

```xpp
public int floor(int pool, [int floor])
```

### <a name="parameters---floor"></a><span data-ttu-id="e9cf3-223">パラメーター - floor</span><span class="sxs-lookup"><span data-stu-id="e9cf3-223">Parameters - floor</span></span>

<span data-ttu-id="e9cf3-224">管理グループ</span><span class="sxs-lookup"><span data-stu-id="e9cf3-224">pool</span></span>  

<!-- -->

<span data-ttu-id="e9cf3-225">floor</span><span class="sxs-lookup"><span data-stu-id="e9cf3-225">floor</span></span>  

### <a name="return-value---floor"></a><span data-ttu-id="e9cf3-226">戻り値 - floor</span><span class="sxs-lookup"><span data-stu-id="e9cf3-226">Return Value - floor</span></span>

## <a name="method-freerefcnt"></a><span data-ttu-id="e9cf3-227">メソッド freeRefCnt</span><span class="sxs-lookup"><span data-stu-id="e9cf3-227">Method freeRefCnt</span></span>

```xpp
public int freeRefCnt()
```

### <a name="return-value---freerefcnt"></a><span data-ttu-id="e9cf3-228">戻り値 - freeRefCnt</span><span class="sxs-lookup"><span data-stu-id="e9cf3-228">Return Value - freeRefCnt</span></span>

## <a name="method-getruntimebugcheckflags"></a><span data-ttu-id="e9cf3-229">メソッド getRuntimeBugcheckFlags</span><span class="sxs-lookup"><span data-stu-id="e9cf3-229">Method getRuntimeBugcheckFlags</span></span>

```xpp
public int getRuntimeBugcheckFlags()
```

### <a name="return-value---getruntimebugcheckflags"></a><span data-ttu-id="e9cf3-230">戻り値 - getRuntimeBugcheckFlags</span><span class="sxs-lookup"><span data-stu-id="e9cf3-230">Return Value - getRuntimeBugcheckFlags</span></span>

## <a name="method-getunfreedcursor"></a><span data-ttu-id="e9cf3-231">メソッド getUnfreedCursor</span><span class="sxs-lookup"><span data-stu-id="e9cf3-231">Method getUnfreedCursor</span></span>

```xpp
public Common getUnfreedCursor()
```

### <a name="return-value---getunfreedcursor"></a><span data-ttu-id="e9cf3-232">戻り値 - getUnfreedCursor</span><span class="sxs-lookup"><span data-stu-id="e9cf3-232">Return Value - getUnfreedCursor</span></span>

## <a name="method-getunfreedobject"></a><span data-ttu-id="e9cf3-233">メソッド getUnfreedObject</span><span class="sxs-lookup"><span data-stu-id="e9cf3-233">Method getUnfreedObject</span></span>

```xpp
public Common getUnfreedObject()
```

### <a name="return-value---getunfreedobject"></a><span data-ttu-id="e9cf3-234">戻り値 - getUnfreedObject</span><span class="sxs-lookup"><span data-stu-id="e9cf3-234">Return Value - getUnfreedObject</span></span>

## <a name="method-include"></a><span data-ttu-id="e9cf3-235">メソッド include</span><span class="sxs-lookup"><span data-stu-id="e9cf3-235">Method include</span></span>

```xpp
public boolean include(int objectNo, [boolean include])
```

### <a name="parameters---include"></a><span data-ttu-id="e9cf3-236">パラメーター - include</span><span class="sxs-lookup"><span data-stu-id="e9cf3-236">Parameters - include</span></span>

<span data-ttu-id="e9cf3-237">objectNo</span><span class="sxs-lookup"><span data-stu-id="e9cf3-237">objectNo</span></span>  

<!-- -->

<span data-ttu-id="e9cf3-238">include</span><span class="sxs-lookup"><span data-stu-id="e9cf3-238">include</span></span>  

### <a name="return-value---include"></a><span data-ttu-id="e9cf3-239">戻り値 - include</span><span class="sxs-lookup"><span data-stu-id="e9cf3-239">Return Value - include</span></span>

## <a name="method-moreunfreedcursors"></a><span data-ttu-id="e9cf3-240">メソッド moreUnfreedCursors</span><span class="sxs-lookup"><span data-stu-id="e9cf3-240">Method moreUnfreedCursors</span></span>

```xpp
public boolean moreUnfreedCursors()
```

### <a name="return-value---moreunfreedcursors"></a><span data-ttu-id="e9cf3-241">戻り値 - moreUnfreedCursors</span><span class="sxs-lookup"><span data-stu-id="e9cf3-241">Return Value - moreUnfreedCursors</span></span>

## <a name="method-moreunfreedobjects"></a><span data-ttu-id="e9cf3-242">メソッド moreUnfreedObjects</span><span class="sxs-lookup"><span data-stu-id="e9cf3-242">Method moreUnfreedObjects</span></span>

```xpp
public boolean moreUnfreedObjects()
```

### <a name="return-value---moreunfreedobjects"></a><span data-ttu-id="e9cf3-243">戻り値 - moreUnfreedObjects</span><span class="sxs-lookup"><span data-stu-id="e9cf3-243">Return Value - moreUnfreedObjects</span></span>

## <a name="method-objectcontext"></a><span data-ttu-id="e9cf3-244">メソッド objectContext</span><span class="sxs-lookup"><span data-stu-id="e9cf3-244">Method objectContext</span></span>

```xpp
public int objectContext(int objNo, [int context])
```

### <a name="parameters---objectcontext"></a><span data-ttu-id="e9cf3-245">パラメーター - objectContext</span><span class="sxs-lookup"><span data-stu-id="e9cf3-245">Parameters - objectContext</span></span>

<span data-ttu-id="e9cf3-246">objNo</span><span class="sxs-lookup"><span data-stu-id="e9cf3-246">objNo</span></span>  

<!-- -->

<span data-ttu-id="e9cf3-247">context</span><span class="sxs-lookup"><span data-stu-id="e9cf3-247">context</span></span>  

### <a name="return-value---objectcontext"></a><span data-ttu-id="e9cf3-248">戻り値 - objectContext</span><span class="sxs-lookup"><span data-stu-id="e9cf3-248">Return Value - objectContext</span></span>

## <a name="method-pagesize"></a><span data-ttu-id="e9cf3-249">メソッド pageSize</span><span class="sxs-lookup"><span data-stu-id="e9cf3-249">Method pageSize</span></span>

```xpp
public int pageSize(int pool, [int pageSize])
```

### <a name="parameters---pagesize"></a><span data-ttu-id="e9cf3-250">パラメーター - pageSize</span><span class="sxs-lookup"><span data-stu-id="e9cf3-250">Parameters - pageSize</span></span>

<span data-ttu-id="e9cf3-251">管理グループ</span><span class="sxs-lookup"><span data-stu-id="e9cf3-251">pool</span></span>  

<!-- -->

<span data-ttu-id="e9cf3-252">pageSize</span><span class="sxs-lookup"><span data-stu-id="e9cf3-252">pageSize</span></span>  

### <a name="return-value---pagesize"></a><span data-ttu-id="e9cf3-253">戻り値 - pageSize</span><span class="sxs-lookup"><span data-stu-id="e9cf3-253">Return Value - pageSize</span></span>

## <a name="method-poolcount"></a><span data-ttu-id="e9cf3-254">メソッド poolCount</span><span class="sxs-lookup"><span data-stu-id="e9cf3-254">Method poolCount</span></span>

```xpp
public int poolCount()
```

### <a name="return-value---poolcount"></a><span data-ttu-id="e9cf3-255">戻り値 - poolCount</span><span class="sxs-lookup"><span data-stu-id="e9cf3-255">Return Value - poolCount</span></span>

## <a name="method-poolname"></a><span data-ttu-id="e9cf3-256">メソッド poolName</span><span class="sxs-lookup"><span data-stu-id="e9cf3-256">Method poolName</span></span>

```xpp
public str poolName(int poolNo)
```

### <a name="parameters---poolname"></a><span data-ttu-id="e9cf3-257">パラメーター - poolName</span><span class="sxs-lookup"><span data-stu-id="e9cf3-257">Parameters - poolName</span></span>

<span data-ttu-id="e9cf3-258">poolNo</span><span class="sxs-lookup"><span data-stu-id="e9cf3-258">poolNo</span></span>  

### <a name="return-value---poolname"></a><span data-ttu-id="e9cf3-259">戻り値 - poolName</span><span class="sxs-lookup"><span data-stu-id="e9cf3-259">Return Value - poolName</span></span>

## <a name="method-smallblocksize"></a><span data-ttu-id="e9cf3-260">メソッド smallBlockSize</span><span class="sxs-lookup"><span data-stu-id="e9cf3-260">Method smallBlockSize</span></span>

```xpp
public int smallBlockSize(int pool, [int blockSize])
```

### <a name="parameters---smallblocksize"></a><span data-ttu-id="e9cf3-261">パラメーター - smallBlockSize</span><span class="sxs-lookup"><span data-stu-id="e9cf3-261">Parameters - smallBlockSize</span></span>

<span data-ttu-id="e9cf3-262">管理グループ</span><span class="sxs-lookup"><span data-stu-id="e9cf3-262">pool</span></span>  

<!-- -->

<span data-ttu-id="e9cf3-263">blockSize</span><span class="sxs-lookup"><span data-stu-id="e9cf3-263">blockSize</span></span>  

### <a name="return-value---smallblocksize"></a><span data-ttu-id="e9cf3-264">戻り値 - smallBlockSize</span><span class="sxs-lookup"><span data-stu-id="e9cf3-264">Return Value - smallBlockSize</span></span>

## <a name="method-sweepcnt"></a><span data-ttu-id="e9cf3-265">メソッド sweepCnt</span><span class="sxs-lookup"><span data-stu-id="e9cf3-265">Method sweepCnt</span></span>

```xpp
public int sweepCnt()
```

### <a name="return-value---sweepcnt"></a><span data-ttu-id="e9cf3-266">戻り値 - sweepCnt</span><span class="sxs-lookup"><span data-stu-id="e9cf3-266">Return Value - sweepCnt</span></span>

## <a name="method-testblocks"></a><span data-ttu-id="e9cf3-267">メソッド testBlocks</span><span class="sxs-lookup"><span data-stu-id="e9cf3-267">Method testBlocks</span></span>

```xpp
public int testBlocks([int arg1])
```

### <a name="parameters---testblocks"></a><span data-ttu-id="e9cf3-268">パラメーター - testBlocks</span><span class="sxs-lookup"><span data-stu-id="e9cf3-268">Parameters - testBlocks</span></span>

<span data-ttu-id="e9cf3-269">arg1</span><span class="sxs-lookup"><span data-stu-id="e9cf3-269">arg1</span></span>  

### <a name="return-value---testblocks"></a><span data-ttu-id="e9cf3-270">戻り値 - testBlocks</span><span class="sxs-lookup"><span data-stu-id="e9cf3-270">Return Value - testBlocks</span></span>

## <a name="method-unfreedobjectclass"></a><span data-ttu-id="e9cf3-271">メソッド unfreedObjectClass</span><span class="sxs-lookup"><span data-stu-id="e9cf3-271">Method unfreedObjectClass</span></span>

```xpp
public str unfreedObjectClass()
```

### <a name="return-value---unfreedobjectclass"></a><span data-ttu-id="e9cf3-272">戻り値 - unfreedObjectClass</span><span class="sxs-lookup"><span data-stu-id="e9cf3-272">Return Value - unfreedObjectClass</span></span>

## <a name="method-unfreedobjectclient"></a><span data-ttu-id="e9cf3-273">メソッド unfreedObjectClient</span><span class="sxs-lookup"><span data-stu-id="e9cf3-273">Method unfreedObjectClient</span></span>

```xpp
public boolean unfreedObjectClient()
```

### <a name="return-value---unfreedobjectclient"></a><span data-ttu-id="e9cf3-274">戻り値 - unfreedObjectClient</span><span class="sxs-lookup"><span data-stu-id="e9cf3-274">Return Value - unfreedObjectClient</span></span>

## <a name="method-unfreedobjectfinalized"></a><span data-ttu-id="e9cf3-275">メソッド unfreedObjectFinalized</span><span class="sxs-lookup"><span data-stu-id="e9cf3-275">Method unfreedObjectFinalized</span></span>

```xpp
public boolean unfreedObjectFinalized()
```

### <a name="return-value---unfreedobjectfinalized"></a><span data-ttu-id="e9cf3-276">戻り値 - unfreedObjectFinalized</span><span class="sxs-lookup"><span data-stu-id="e9cf3-276">Return Value - unfreedObjectFinalized</span></span>

## <a name="method-unfreedobjecthandle"></a><span data-ttu-id="e9cf3-277">メソッド unfreedObjectHandle</span><span class="sxs-lookup"><span data-stu-id="e9cf3-277">Method unfreedObjectHandle</span></span>

```xpp
public int unfreedObjectHandle()
```

### <a name="return-value---unfreedobjecthandle"></a><span data-ttu-id="e9cf3-278">戻り値 - unfreedObjectHandle</span><span class="sxs-lookup"><span data-stu-id="e9cf3-278">Return Value - unfreedObjectHandle</span></span>

## <a name="method-unfreedobjectident"></a><span data-ttu-id="e9cf3-279">メソッド unfreedObjectIdent</span><span class="sxs-lookup"><span data-stu-id="e9cf3-279">Method unfreedObjectIdent</span></span>

```xpp
public int unfreedObjectIdent()
```

### <a name="return-value---unfreedobjectident"></a><span data-ttu-id="e9cf3-280">戻り値 - unfreedObjectIdent</span><span class="sxs-lookup"><span data-stu-id="e9cf3-280">Return Value - unfreedObjectIdent</span></span>

## <a name="method-unfreedobjectusecount"></a><span data-ttu-id="e9cf3-281">メソッド unfreedObjectUseCount</span><span class="sxs-lookup"><span data-stu-id="e9cf3-281">Method unfreedObjectUseCount</span></span>

```xpp
public int unfreedObjectUseCount()
```

### <a name="return-value---unfreedobjectusecount"></a><span data-ttu-id="e9cf3-282">戻り値 - unfreedObjectUseCount</span><span class="sxs-lookup"><span data-stu-id="e9cf3-282">Return Value - unfreedObjectUseCount</span></span>

## <a name="method-version"></a><span data-ttu-id="e9cf3-283">メソッド version</span><span class="sxs-lookup"><span data-stu-id="e9cf3-283">Method version</span></span>

```xpp
public str version()
```

### <a name="return-value---version"></a><span data-ttu-id="e9cf3-284">戻り値 - version</span><span class="sxs-lookup"><span data-stu-id="e9cf3-284">Return Value - version</span></span>

## <a name="method-checkheap"></a><span data-ttu-id="e9cf3-285">メソッド checkHeap</span><span class="sxs-lookup"><span data-stu-id="e9cf3-285">Method checkHeap</span></span>

```xpp
public void checkHeap(str Description, [int context], [int pool], [boolean detailed])
```

### <a name="parameters---checkheap"></a><span data-ttu-id="e9cf3-286">パラメーター - checkHeap</span><span class="sxs-lookup"><span data-stu-id="e9cf3-286">Parameters - checkHeap</span></span>

<span data-ttu-id="e9cf3-287">説明</span><span class="sxs-lookup"><span data-stu-id="e9cf3-287">Description</span></span>  

<!-- -->

<span data-ttu-id="e9cf3-288">context</span><span class="sxs-lookup"><span data-stu-id="e9cf3-288">context</span></span>  

<!-- -->

<span data-ttu-id="e9cf3-289">管理グループ</span><span class="sxs-lookup"><span data-stu-id="e9cf3-289">pool</span></span>  

<!-- -->

<span data-ttu-id="e9cf3-290">detailed</span><span class="sxs-lookup"><span data-stu-id="e9cf3-290">detailed</span></span>  

## <a name="method-shrinkpool"></a><span data-ttu-id="e9cf3-291">メソッド shrinkPool</span><span class="sxs-lookup"><span data-stu-id="e9cf3-291">Method shrinkPool</span></span>

```xpp
public void shrinkPool([int poolNo])
```

### <a name="parameters---shrinkpool"></a><span data-ttu-id="e9cf3-292">パラメーター - shrinkPool</span><span class="sxs-lookup"><span data-stu-id="e9cf3-292">Parameters - shrinkPool</span></span>

<span data-ttu-id="e9cf3-293">poolNo</span><span class="sxs-lookup"><span data-stu-id="e9cf3-293">poolNo</span></span>  

## <a name="method-postcompactingmessage"></a><span data-ttu-id="e9cf3-294">メソッド postCompactingMessage</span><span class="sxs-lookup"><span data-stu-id="e9cf3-294">Method postCompactingMessage</span></span>

```xpp
public void postCompactingMessage()
```

## <a name="method-checkheapdif"></a><span data-ttu-id="e9cf3-295">メソッド checkHeapDif</span><span class="sxs-lookup"><span data-stu-id="e9cf3-295">Method checkHeapDif</span></span>

```xpp
public void checkHeapDif(str Description, [int context], [int pool])
```

### <a name="parameters---checkheapdif"></a><span data-ttu-id="e9cf3-296">パラメーター - checkHeapDif</span><span class="sxs-lookup"><span data-stu-id="e9cf3-296">Parameters - checkHeapDif</span></span>

<span data-ttu-id="e9cf3-297">説明</span><span class="sxs-lookup"><span data-stu-id="e9cf3-297">Description</span></span>  

<!-- -->

<span data-ttu-id="e9cf3-298">context</span><span class="sxs-lookup"><span data-stu-id="e9cf3-298">context</span></span>  

<!-- -->

<span data-ttu-id="e9cf3-299">管理グループ</span><span class="sxs-lookup"><span data-stu-id="e9cf3-299">pool</span></span>  

## <a name="method-clearheapcontext"></a><span data-ttu-id="e9cf3-300">メソッド clearHeapContext</span><span class="sxs-lookup"><span data-stu-id="e9cf3-300">Method clearHeapContext</span></span>

```xpp
public void clearHeapContext()
```

## <a name="method-writestring"></a><span data-ttu-id="e9cf3-301">メソッド writeString</span><span class="sxs-lookup"><span data-stu-id="e9cf3-301">Method writeString</span></span>

```xpp
public void writeString(str text)
```

### <a name="parameters---writestring"></a><span data-ttu-id="e9cf3-302">パラメーター - writeString</span><span class="sxs-lookup"><span data-stu-id="e9cf3-302">Parameters - writeString</span></span>

<span data-ttu-id="e9cf3-303">テキスト</span><span class="sxs-lookup"><span data-stu-id="e9cf3-303">text</span></span>  

## <a name="method-firstunfreedcursor"></a><span data-ttu-id="e9cf3-304">メソッド firstUnfreedCursor</span><span class="sxs-lookup"><span data-stu-id="e9cf3-304">Method firstUnfreedCursor</span></span>

```xpp
public void firstUnfreedCursor()
```

## <a name="method-dumpdgmlgraph"></a><span data-ttu-id="e9cf3-305">メソッド dumpDGMLGraph</span><span class="sxs-lookup"><span data-stu-id="e9cf3-305">Method dumpDGMLGraph</span></span>

```xpp
public void dumpDGMLGraph()
```

## <a name="method-firstunfreedobject"></a><span data-ttu-id="e9cf3-306">メソッド firstUnfreedObject</span><span class="sxs-lookup"><span data-stu-id="e9cf3-306">Method firstUnfreedObject</span></span>

```xpp
public void firstUnfreedObject()
```

## <a name="method-setheapcontext"></a><span data-ttu-id="e9cf3-307">メソッド setHeapContext</span><span class="sxs-lookup"><span data-stu-id="e9cf3-307">Method setHeapContext</span></span>

```xpp
public void setHeapContext(str description)
```

### <a name="parameters---setheapcontext"></a><span data-ttu-id="e9cf3-308">パラメーター - setHeapContext</span><span class="sxs-lookup"><span data-stu-id="e9cf3-308">Parameters - setHeapContext</span></span>

<span data-ttu-id="e9cf3-309">説明</span><span class="sxs-lookup"><span data-stu-id="e9cf3-309">description</span></span>  

## <a name="method-new"></a><span data-ttu-id="e9cf3-310">メソッド new</span><span class="sxs-lookup"><span data-stu-id="e9cf3-310">Method new</span></span>

<span data-ttu-id="e9cf3-311">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e9cf3-311">Initializes a new instance of the Object class.</span></span>

```xpp
public void new([str Filename])
```

### <a name="parameters---new"></a><span data-ttu-id="e9cf3-312">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="e9cf3-312">Parameters - new</span></span>

<span data-ttu-id="e9cf3-313">ファイル名</span><span class="sxs-lookup"><span data-stu-id="e9cf3-313">Filename</span></span>  

## <a name="method-nextunfreedobject"></a><span data-ttu-id="e9cf3-314">メソッド nextUnfreedObject</span><span class="sxs-lookup"><span data-stu-id="e9cf3-314">Method nextUnfreedObject</span></span>

```xpp
public void nextUnfreedObject()
```

## <a name="method-checkheapstop"></a><span data-ttu-id="e9cf3-315">メソッド checkHeapStop</span><span class="sxs-lookup"><span data-stu-id="e9cf3-315">Method checkHeapStop</span></span>

```xpp
public void checkHeapStop()
```

## <a name="method-nextunfreedcursor"></a><span data-ttu-id="e9cf3-316">メソッド nextUnfreedCursor</span><span class="sxs-lookup"><span data-stu-id="e9cf3-316">Method nextUnfreedCursor</span></span>

```xpp
public void nextUnfreedCursor()
```

## <a name="method-setruntimebugcheckflags"></a><span data-ttu-id="e9cf3-317">メソッド setRuntimeBugcheckFlags</span><span class="sxs-lookup"><span data-stu-id="e9cf3-317">Method setRuntimeBugcheckFlags</span></span>

```xpp
public void setRuntimeBugcheckFlags(int flags)
```

### <a name="parameters---setruntimebugcheckflags"></a><span data-ttu-id="e9cf3-318">パラメーター - setRuntimeBugcheckFlags</span><span class="sxs-lookup"><span data-stu-id="e9cf3-318">Parameters - setRuntimeBugcheckFlags</span></span>

<span data-ttu-id="e9cf3-319">flags</span><span class="sxs-lookup"><span data-stu-id="e9cf3-319">flags</span></span>  

## <a name="method-checkheapstart"></a><span data-ttu-id="e9cf3-320">メソッド checkHeapStart</span><span class="sxs-lookup"><span data-stu-id="e9cf3-320">Method checkHeapStart</span></span>

```xpp
public void checkHeapStart()
```

