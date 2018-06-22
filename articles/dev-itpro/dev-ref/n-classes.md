---
title: "N クラス"
description: "文字 N で始まるシステム API クラス。"
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
ms.custom: 52351
ms.assetid: 4816db3a-defc-4057-ba08-50d85f597eeb
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d2a5fde451d5457781e02609eb600cf616ea0e49
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="n-classes"></a><span data-ttu-id="bffae-103">N クラス</span><span class="sxs-lookup"><span data-stu-id="bffae-103">N Classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bffae-104">文字 N で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="bffae-104">System API classes that start with the letter N.</span></span>

<a name="class-numbersequence"></a><span data-ttu-id="bffae-105">クラス NumberSequence</span><span class="sxs-lookup"><span data-stu-id="bffae-105">Class NumberSequence</span></span>
--------------------

    class NumberSequence extends Object

### <a name="remarks"></a><span data-ttu-id="bffae-106">備考</span><span class="sxs-lookup"><span data-stu-id="bffae-106">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="bffae-107">例</span><span class="sxs-lookup"><span data-stu-id="bffae-107">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="bffae-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="bffae-108">Methods</span></span>

| <span data-ttu-id="bffae-109">方法</span><span class="sxs-lookup"><span data-stu-id="bffae-109">Method</span></span>                                                                                                                                                                | <span data-ttu-id="bffae-110">説明</span><span class="sxs-lookup"><span data-stu-id="bffae-110">Description</span></span>                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="bffae-111">::public static int getNextNumber(Connection connection, Int64 numbersequencerecordid, Int64 globaltransid, str userid, int sessionid, DateTime sessionLoginDateTime)</span><span class="sxs-lookup"><span data-stu-id="bffae-111">::public static int getNextNumber(Connection connection, Int64 numbersequencerecordid, Int64 globaltransid, str userid, int sessionid, DateTime sessionLoginDateTime)</span></span> |                                                         |
| <span data-ttu-id="bffae-112">public void new()</span><span class="sxs-lookup"><span data-stu-id="bffae-112">public void new()</span></span>                                                                                                                                                     | <span data-ttu-id="bffae-113">NumberSequence クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="bffae-113">Initializes a new instance of the NumberSequence class.</span></span> |

### <a name="method-getnextnumber"></a><span data-ttu-id="bffae-114">メソッド getNextNumber</span><span class="sxs-lookup"><span data-stu-id="bffae-114">Method getNextNumber</span></span>

    public static int getNextNumber(Connection connection, Int64 numbersequencerecordid, Int64 globaltransid, str userid, int sessionid, DateTime sessionLoginDateTime)

#### <a name="parameters"></a><span data-ttu-id="bffae-115">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bffae-115">Parameters</span></span>

<span data-ttu-id="bffae-116">connection</span><span class="sxs-lookup"><span data-stu-id="bffae-116">connection</span></span>  

<!-- -->

<span data-ttu-id="bffae-117">numbersequencerecordid</span><span class="sxs-lookup"><span data-stu-id="bffae-117">numbersequencerecordid</span></span>  

<!-- -->

<span data-ttu-id="bffae-118">globaltransid</span><span class="sxs-lookup"><span data-stu-id="bffae-118">globaltransid</span></span>  

<!-- -->

<span data-ttu-id="bffae-119">userid</span><span class="sxs-lookup"><span data-stu-id="bffae-119">userid</span></span>  

<!-- -->

<span data-ttu-id="bffae-120">sessionid</span><span class="sxs-lookup"><span data-stu-id="bffae-120">sessionid</span></span>  

<!-- -->

<span data-ttu-id="bffae-121">sessionLoginDateTime</span><span class="sxs-lookup"><span data-stu-id="bffae-121">sessionLoginDateTime</span></span>  

#### <a name="return-value"></a><span data-ttu-id="bffae-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="bffae-122">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="bffae-123">メソッド new</span><span class="sxs-lookup"><span data-stu-id="bffae-123">Method new</span></span>

<span data-ttu-id="bffae-124">NumberSequence クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="bffae-124">Initializes a new instance of the NumberSequence class.</span></span>

    public void new()

## <a name="class-numbersequencesessionlesscache"></a><span data-ttu-id="bffae-125">クラス NumberSequenceSessionLessCache</span><span class="sxs-lookup"><span data-stu-id="bffae-125">Class NumberSequenceSessionLessCache</span></span>
    class NumberSequenceSessionLessCache extends Object

### <a name="remarks"></a><span data-ttu-id="bffae-126">備考</span><span class="sxs-lookup"><span data-stu-id="bffae-126">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="bffae-127">例</span><span class="sxs-lookup"><span data-stu-id="bffae-127">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="bffae-128">メソッド</span><span class="sxs-lookup"><span data-stu-id="bffae-128">Methods</span></span>

| <span data-ttu-id="bffae-129">方法</span><span class="sxs-lookup"><span data-stu-id="bffae-129">Method</span></span>                                                                         | <span data-ttu-id="bffae-130">説明</span><span class="sxs-lookup"><span data-stu-id="bffae-130">Description</span></span>                                                             |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="bffae-131">public int getNumFromCache(Common numbersequencetable)</span><span class="sxs-lookup"><span data-stu-id="bffae-131">public int getNumFromCache(Common numbersequencetable)</span></span>                         |                                                                         |
| <span data-ttu-id="bffae-132">public int valueLastNumFromCache(Int64 numbersequecerecordid)</span><span class="sxs-lookup"><span data-stu-id="bffae-132">public int valueLastNumFromCache(Int64 numbersequecerecordid)</span></span>                  |                                                                         |
| <span data-ttu-id="bffae-133">public int valueNextNumFromCache(Int64 numbersequecerecordid)</span><span class="sxs-lookup"><span data-stu-id="bffae-133">public int valueNextNumFromCache(Int64 numbersequecerecordid)</span></span>                  |                                                                         |
| <span data-ttu-id="bffae-134">public void flushCache(Int64 numbersequecerecordid)</span><span class="sxs-lookup"><span data-stu-id="bffae-134">public void flushCache(Int64 numbersequecerecordid)</span></span>                            |                                                                         |
| <span data-ttu-id="bffae-135">public void fillCache(Int64 numbersequecerecordid, int nextRec, int blockSize)</span><span class="sxs-lookup"><span data-stu-id="bffae-135">public void fillCache(Int64 numbersequecerecordid, int nextRec, int blockSize)</span></span> |                                                                         |
| <span data-ttu-id="bffae-136">public void new()</span><span class="sxs-lookup"><span data-stu-id="bffae-136">public void new()</span></span>                                                              | <span data-ttu-id="bffae-137">NumberSequenceSessionLessCache クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="bffae-137">Initializes a new instance of the NumberSequenceSessionLessCache class.</span></span> |

### <a name="method-getnumfromcache"></a><span data-ttu-id="bffae-138">メソッド getNumFromCache</span><span class="sxs-lookup"><span data-stu-id="bffae-138">Method getNumFromCache</span></span>

    public int getNumFromCache(Common numbersequencetable)

#### <a name="parameters"></a><span data-ttu-id="bffae-139">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bffae-139">Parameters</span></span>

<span data-ttu-id="bffae-140">numbersequencetable</span><span class="sxs-lookup"><span data-stu-id="bffae-140">numbersequencetable</span></span>  

#### <a name="return-value"></a><span data-ttu-id="bffae-141">戻り値</span><span class="sxs-lookup"><span data-stu-id="bffae-141">Return Value</span></span>

### <a name="method-valuelastnumfromcache"></a><span data-ttu-id="bffae-142">メソッド valueLastNumFromCache</span><span class="sxs-lookup"><span data-stu-id="bffae-142">Method valueLastNumFromCache</span></span>

    public int valueLastNumFromCache(Int64 numbersequecerecordid)

#### <a name="parameters"></a><span data-ttu-id="bffae-143">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bffae-143">Parameters</span></span>

<span data-ttu-id="bffae-144">numbersequecerecordid</span><span class="sxs-lookup"><span data-stu-id="bffae-144">numbersequecerecordid</span></span>  

#### <a name="return-value"></a><span data-ttu-id="bffae-145">戻り値</span><span class="sxs-lookup"><span data-stu-id="bffae-145">Return Value</span></span>

### <a name="method-valuenextnumfromcache"></a><span data-ttu-id="bffae-146">メソッド valueNextNumFromCache</span><span class="sxs-lookup"><span data-stu-id="bffae-146">Method valueNextNumFromCache</span></span>

    public int valueNextNumFromCache(Int64 numbersequecerecordid)

#### <a name="parameters"></a><span data-ttu-id="bffae-147">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bffae-147">Parameters</span></span>

<span data-ttu-id="bffae-148">numbersequecerecordid</span><span class="sxs-lookup"><span data-stu-id="bffae-148">numbersequecerecordid</span></span>  

#### <a name="return-value"></a><span data-ttu-id="bffae-149">戻り値</span><span class="sxs-lookup"><span data-stu-id="bffae-149">Return Value</span></span>

### <a name="method-flushcache"></a><span data-ttu-id="bffae-150">メソッド flushCache</span><span class="sxs-lookup"><span data-stu-id="bffae-150">Method flushCache</span></span>

    public void flushCache(Int64 numbersequecerecordid)

#### <a name="parameters"></a><span data-ttu-id="bffae-151">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bffae-151">Parameters</span></span>

<span data-ttu-id="bffae-152">numbersequecerecordid</span><span class="sxs-lookup"><span data-stu-id="bffae-152">numbersequecerecordid</span></span>  

### <a name="method-fillcache"></a><span data-ttu-id="bffae-153">メソッド fillCache</span><span class="sxs-lookup"><span data-stu-id="bffae-153">Method fillCache</span></span>

    public void fillCache(Int64 numbersequecerecordid, int nextRec, int blockSize)

#### <a name="parameters"></a><span data-ttu-id="bffae-154">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bffae-154">Parameters</span></span>

<span data-ttu-id="bffae-155">numbersequecerecordid</span><span class="sxs-lookup"><span data-stu-id="bffae-155">numbersequecerecordid</span></span>  

<!-- -->

<span data-ttu-id="bffae-156">nextRec</span><span class="sxs-lookup"><span data-stu-id="bffae-156">nextRec</span></span>  

<!-- -->

<span data-ttu-id="bffae-157">blockSize</span><span class="sxs-lookup"><span data-stu-id="bffae-157">blockSize</span></span>  

### <a name="method-new"></a><span data-ttu-id="bffae-158">メソッド new</span><span class="sxs-lookup"><span data-stu-id="bffae-158">Method new</span></span>

<span data-ttu-id="bffae-159">NumberSequenceSessionLessCache クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="bffae-159">Initializes a new instance of the NumberSequenceSessionLessCache class.</span></span>

    public void new()




