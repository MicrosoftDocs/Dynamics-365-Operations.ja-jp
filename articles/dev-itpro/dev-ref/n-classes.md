---
title: N クラス
description: 文字 N で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 52351
ms.assetid: 4816db3a-defc-4057-ba08-50d85f597eeb
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cc3311c6c477f60a98a115eec7ee7221e92909f4
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833666"
---
# <a name="n-classes"></a><span data-ttu-id="35afc-103">N クラス</span><span class="sxs-lookup"><span data-stu-id="35afc-103">N classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35afc-104">文字 N で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="35afc-104">System API classes that start with the letter N.</span></span>

<a name="class-numbersequence"></a><span data-ttu-id="35afc-105">クラス NumberSequence</span><span class="sxs-lookup"><span data-stu-id="35afc-105">Class NumberSequence</span></span>
--------------------

    class NumberSequence extends Object

### <a name="remarks"></a><span data-ttu-id="35afc-106">備考</span><span class="sxs-lookup"><span data-stu-id="35afc-106">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="35afc-107">例</span><span class="sxs-lookup"><span data-stu-id="35afc-107">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="35afc-108">方法</span><span class="sxs-lookup"><span data-stu-id="35afc-108">Methods</span></span>

| <span data-ttu-id="35afc-109">方法</span><span class="sxs-lookup"><span data-stu-id="35afc-109">Method</span></span>                                                                                                                                                                | <span data-ttu-id="35afc-110">説明</span><span class="sxs-lookup"><span data-stu-id="35afc-110">Description</span></span>                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="35afc-111">::public static int getNextNumber(Connection connection, Int64 numbersequencerecordid, Int64 globaltransid, str userid, int sessionid, DateTime sessionLoginDateTime)</span><span class="sxs-lookup"><span data-stu-id="35afc-111">::public static int getNextNumber(Connection connection, Int64 numbersequencerecordid, Int64 globaltransid, str userid, int sessionid, DateTime sessionLoginDateTime)</span></span> |                                                         |
| <span data-ttu-id="35afc-112">public void new()</span><span class="sxs-lookup"><span data-stu-id="35afc-112">public void new()</span></span>                                                                                                                                                     | <span data-ttu-id="35afc-113">NumberSequence クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="35afc-113">Initializes a new instance of the NumberSequence class.</span></span> |

### <a name="method-getnextnumber"></a><span data-ttu-id="35afc-114">メソッド getNextNumber</span><span class="sxs-lookup"><span data-stu-id="35afc-114">Method getNextNumber</span></span>

    public static int getNextNumber(Connection connection, Int64 numbersequencerecordid, Int64 globaltransid, str userid, int sessionid, DateTime sessionLoginDateTime)

#### <a name="parameters"></a><span data-ttu-id="35afc-115">パラメーター</span><span class="sxs-lookup"><span data-stu-id="35afc-115">Parameters</span></span>

<span data-ttu-id="35afc-116">connection</span><span class="sxs-lookup"><span data-stu-id="35afc-116">connection</span></span>  

<!-- -->

<span data-ttu-id="35afc-117">numbersequencerecordid</span><span class="sxs-lookup"><span data-stu-id="35afc-117">numbersequencerecordid</span></span>  

<!-- -->

<span data-ttu-id="35afc-118">globaltransid</span><span class="sxs-lookup"><span data-stu-id="35afc-118">globaltransid</span></span>  

<!-- -->

<span data-ttu-id="35afc-119">userid</span><span class="sxs-lookup"><span data-stu-id="35afc-119">userid</span></span>  

<!-- -->

<span data-ttu-id="35afc-120">sessionid</span><span class="sxs-lookup"><span data-stu-id="35afc-120">sessionid</span></span>  

<!-- -->

<span data-ttu-id="35afc-121">sessionLoginDateTime</span><span class="sxs-lookup"><span data-stu-id="35afc-121">sessionLoginDateTime</span></span>  

#### <a name="return-value"></a><span data-ttu-id="35afc-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="35afc-122">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="35afc-123">メソッド new</span><span class="sxs-lookup"><span data-stu-id="35afc-123">Method new</span></span>

<span data-ttu-id="35afc-124">NumberSequence クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="35afc-124">Initializes a new instance of the NumberSequence class.</span></span>

    public void new()

## <a name="class-numbersequencesessionlesscache"></a><span data-ttu-id="35afc-125">クラス NumberSequenceSessionLessCache</span><span class="sxs-lookup"><span data-stu-id="35afc-125">Class NumberSequenceSessionLessCache</span></span>
    class NumberSequenceSessionLessCache extends Object

### <a name="remarks"></a><span data-ttu-id="35afc-126">備考</span><span class="sxs-lookup"><span data-stu-id="35afc-126">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="35afc-127">例</span><span class="sxs-lookup"><span data-stu-id="35afc-127">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="35afc-128">メソッド</span><span class="sxs-lookup"><span data-stu-id="35afc-128">Methods</span></span>

| <span data-ttu-id="35afc-129">方法</span><span class="sxs-lookup"><span data-stu-id="35afc-129">Method</span></span>                                                                         | <span data-ttu-id="35afc-130">説明</span><span class="sxs-lookup"><span data-stu-id="35afc-130">Description</span></span>                                                             |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="35afc-131">public int getNumFromCache(Common numbersequencetable)</span><span class="sxs-lookup"><span data-stu-id="35afc-131">public int getNumFromCache(Common numbersequencetable)</span></span>                         |                                                                         |
| <span data-ttu-id="35afc-132">public int valueLastNumFromCache(Int64 numbersequecerecordid)</span><span class="sxs-lookup"><span data-stu-id="35afc-132">public int valueLastNumFromCache(Int64 numbersequecerecordid)</span></span>                  |                                                                         |
| <span data-ttu-id="35afc-133">public int valueNextNumFromCache(Int64 numbersequecerecordid)</span><span class="sxs-lookup"><span data-stu-id="35afc-133">public int valueNextNumFromCache(Int64 numbersequecerecordid)</span></span>                  |                                                                         |
| <span data-ttu-id="35afc-134">public void flushCache(Int64 numbersequecerecordid)</span><span class="sxs-lookup"><span data-stu-id="35afc-134">public void flushCache(Int64 numbersequecerecordid)</span></span>                            |                                                                         |
| <span data-ttu-id="35afc-135">public void fillCache(Int64 numbersequecerecordid, int nextRec, int blockSize)</span><span class="sxs-lookup"><span data-stu-id="35afc-135">public void fillCache(Int64 numbersequecerecordid, int nextRec, int blockSize)</span></span> |                                                                         |
| <span data-ttu-id="35afc-136">public void new()</span><span class="sxs-lookup"><span data-stu-id="35afc-136">public void new()</span></span>                                                              | <span data-ttu-id="35afc-137">NumberSequenceSessionLessCache クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="35afc-137">Initializes a new instance of the NumberSequenceSessionLessCache class.</span></span> |

### <a name="method-getnumfromcache"></a><span data-ttu-id="35afc-138">メソッド getNumFromCache</span><span class="sxs-lookup"><span data-stu-id="35afc-138">Method getNumFromCache</span></span>

    public int getNumFromCache(Common numbersequencetable)

#### <a name="parameters"></a><span data-ttu-id="35afc-139">パラメーター</span><span class="sxs-lookup"><span data-stu-id="35afc-139">Parameters</span></span>

<span data-ttu-id="35afc-140">numbersequencetable</span><span class="sxs-lookup"><span data-stu-id="35afc-140">numbersequencetable</span></span>  

#### <a name="return-value"></a><span data-ttu-id="35afc-141">戻り値</span><span class="sxs-lookup"><span data-stu-id="35afc-141">Return Value</span></span>

### <a name="method-valuelastnumfromcache"></a><span data-ttu-id="35afc-142">メソッド valueLastNumFromCache</span><span class="sxs-lookup"><span data-stu-id="35afc-142">Method valueLastNumFromCache</span></span>

    public int valueLastNumFromCache(Int64 numbersequecerecordid)

#### <a name="parameters"></a><span data-ttu-id="35afc-143">パラメーター</span><span class="sxs-lookup"><span data-stu-id="35afc-143">Parameters</span></span>

<span data-ttu-id="35afc-144">numbersequecerecordid</span><span class="sxs-lookup"><span data-stu-id="35afc-144">numbersequecerecordid</span></span>  

#### <a name="return-value"></a><span data-ttu-id="35afc-145">戻り値</span><span class="sxs-lookup"><span data-stu-id="35afc-145">Return Value</span></span>

### <a name="method-valuenextnumfromcache"></a><span data-ttu-id="35afc-146">メソッド valueNextNumFromCache</span><span class="sxs-lookup"><span data-stu-id="35afc-146">Method valueNextNumFromCache</span></span>

    public int valueNextNumFromCache(Int64 numbersequecerecordid)

#### <a name="parameters"></a><span data-ttu-id="35afc-147">パラメーター</span><span class="sxs-lookup"><span data-stu-id="35afc-147">Parameters</span></span>

<span data-ttu-id="35afc-148">numbersequecerecordid</span><span class="sxs-lookup"><span data-stu-id="35afc-148">numbersequecerecordid</span></span>  

#### <a name="return-value"></a><span data-ttu-id="35afc-149">戻り値</span><span class="sxs-lookup"><span data-stu-id="35afc-149">Return Value</span></span>

### <a name="method-flushcache"></a><span data-ttu-id="35afc-150">メソッド flushCache</span><span class="sxs-lookup"><span data-stu-id="35afc-150">Method flushCache</span></span>

    public void flushCache(Int64 numbersequecerecordid)

#### <a name="parameters"></a><span data-ttu-id="35afc-151">パラメーター</span><span class="sxs-lookup"><span data-stu-id="35afc-151">Parameters</span></span>

<span data-ttu-id="35afc-152">numbersequecerecordid</span><span class="sxs-lookup"><span data-stu-id="35afc-152">numbersequecerecordid</span></span>  

### <a name="method-fillcache"></a><span data-ttu-id="35afc-153">メソッド fillCache</span><span class="sxs-lookup"><span data-stu-id="35afc-153">Method fillCache</span></span>

    public void fillCache(Int64 numbersequecerecordid, int nextRec, int blockSize)

#### <a name="parameters"></a><span data-ttu-id="35afc-154">パラメーター</span><span class="sxs-lookup"><span data-stu-id="35afc-154">Parameters</span></span>

<span data-ttu-id="35afc-155">numbersequecerecordid</span><span class="sxs-lookup"><span data-stu-id="35afc-155">numbersequecerecordid</span></span>  

<!-- -->

<span data-ttu-id="35afc-156">nextRec</span><span class="sxs-lookup"><span data-stu-id="35afc-156">nextRec</span></span>  

<!-- -->

<span data-ttu-id="35afc-157">blockSize</span><span class="sxs-lookup"><span data-stu-id="35afc-157">blockSize</span></span>  

### <a name="method-new"></a><span data-ttu-id="35afc-158">メソッド new</span><span class="sxs-lookup"><span data-stu-id="35afc-158">Method new</span></span>

<span data-ttu-id="35afc-159">NumberSequenceSessionLessCache クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="35afc-159">Initializes a new instance of the NumberSequenceSessionLessCache class.</span></span>

    public void new()



