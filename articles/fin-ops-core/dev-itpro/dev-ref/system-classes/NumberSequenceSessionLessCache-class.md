---
title: NumberSequenceSessionLessCache クラス
description: このトピックでは、NumberSequenceSessionLessCache クラスについて説明します。
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
ms.openlocfilehash: 9e93d0ae641a0c8edf49c4bce1c98717a369aec1
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502567"
---
# <a name="class-numbersequencesessionlesscache"></a><span data-ttu-id="9f352-103">クラス NumberSequenceSessionLessCache</span><span class="sxs-lookup"><span data-stu-id="9f352-103">Class NumberSequenceSessionLessCache</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class NumberSequenceSessionLessCache extends Object
```

## <a name="remarks"></a><span data-ttu-id="9f352-104">備考</span><span class="sxs-lookup"><span data-stu-id="9f352-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="9f352-105">例</span><span class="sxs-lookup"><span data-stu-id="9f352-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="9f352-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="9f352-106">Methods</span></span>

| <span data-ttu-id="9f352-107">方法</span><span class="sxs-lookup"><span data-stu-id="9f352-107">Method</span></span>                                                                         | <span data-ttu-id="9f352-108">説明</span><span class="sxs-lookup"><span data-stu-id="9f352-108">Description</span></span>                                                             |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="9f352-109">public int getNumFromCache(Common numbersequencetable)</span><span class="sxs-lookup"><span data-stu-id="9f352-109">public int getNumFromCache(Common numbersequencetable)</span></span>                         |                                                                         |
| <span data-ttu-id="9f352-110">public int valueLastNumFromCache(Int64 numbersequecerecordid)</span><span class="sxs-lookup"><span data-stu-id="9f352-110">public int valueLastNumFromCache(Int64 numbersequecerecordid)</span></span>                  |                                                                         |
| <span data-ttu-id="9f352-111">public int valueNextNumFromCache(Int64 numbersequecerecordid)</span><span class="sxs-lookup"><span data-stu-id="9f352-111">public int valueNextNumFromCache(Int64 numbersequecerecordid)</span></span>                  |                                                                         |
| <span data-ttu-id="9f352-112">public void flushCache(Int64 numbersequecerecordid)</span><span class="sxs-lookup"><span data-stu-id="9f352-112">public void flushCache(Int64 numbersequecerecordid)</span></span>                            |                                                                         |
| <span data-ttu-id="9f352-113">public void fillCache(Int64 numbersequecerecordid, int nextRec, int blockSize)</span><span class="sxs-lookup"><span data-stu-id="9f352-113">public void fillCache(Int64 numbersequecerecordid, int nextRec, int blockSize)</span></span> |                                                                         |
| <span data-ttu-id="9f352-114">public void new()</span><span class="sxs-lookup"><span data-stu-id="9f352-114">public void new()</span></span>                                                              | <span data-ttu-id="9f352-115">NumberSequenceSessionLessCache クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="9f352-115">Initializes a new instance of the NumberSequenceSessionLessCache class.</span></span> |

## <a name="method-getnumfromcache"></a><span data-ttu-id="9f352-116">メソッド getNumFromCache</span><span class="sxs-lookup"><span data-stu-id="9f352-116">Method getNumFromCache</span></span>

```xpp
public int getNumFromCache(Common numbersequencetable)
```

### <a name="parameters---getnumfromcache"></a><span data-ttu-id="9f352-117">パラメーター - getNumFromCache</span><span class="sxs-lookup"><span data-stu-id="9f352-117">Parameters - getNumFromCache</span></span>

<span data-ttu-id="9f352-118">numbersequencetable</span><span class="sxs-lookup"><span data-stu-id="9f352-118">numbersequencetable</span></span>  

### <a name="return-value---getnumfromcache"></a><span data-ttu-id="9f352-119">戻り値 - getNumFromCache</span><span class="sxs-lookup"><span data-stu-id="9f352-119">Return Value - getNumFromCache</span></span>

## <a name="method-valuelastnumfromcache"></a><span data-ttu-id="9f352-120">メソッド valueLastNumFromCache</span><span class="sxs-lookup"><span data-stu-id="9f352-120">Method valueLastNumFromCache</span></span>

```xpp
public int valueLastNumFromCache(Int64 numbersequecerecordid)
```

### <a name="parameters---valuelastnumfromcache"></a><span data-ttu-id="9f352-121">パラメーター - valueNextNumFromCache</span><span class="sxs-lookup"><span data-stu-id="9f352-121">Parameters - valueLastNumFromCache</span></span>

<span data-ttu-id="9f352-122">numbersequecerecordid</span><span class="sxs-lookup"><span data-stu-id="9f352-122">numbersequecerecordid</span></span>  

### <a name="return-value---valuelastnumfromcache"></a><span data-ttu-id="9f352-123">戻り値 - valueNextNumFromCache</span><span class="sxs-lookup"><span data-stu-id="9f352-123">Return Value - valueLastNumFromCache</span></span>

## <a name="method-valuenextnumfromcache"></a><span data-ttu-id="9f352-124">メソッド valueNextNumFromCache</span><span class="sxs-lookup"><span data-stu-id="9f352-124">Method valueNextNumFromCache</span></span>

```xpp
public int valueNextNumFromCache(Int64 numbersequecerecordid)
```

### <a name="parameters---valuenextnumfromcache"></a><span data-ttu-id="9f352-125">パラメーター - valueNextNumFromCache</span><span class="sxs-lookup"><span data-stu-id="9f352-125">Parameters - valueNextNumFromCache</span></span>

<span data-ttu-id="9f352-126">numbersequecerecordid</span><span class="sxs-lookup"><span data-stu-id="9f352-126">numbersequecerecordid</span></span>  

### <a name="return-value---valuenextnumfromcache"></a><span data-ttu-id="9f352-127">戻り値 - valueNextNumFromCache</span><span class="sxs-lookup"><span data-stu-id="9f352-127">Return Value - valueNextNumFromCache</span></span>

## <a name="method-flushcache"></a><span data-ttu-id="9f352-128">メソッド flushCache</span><span class="sxs-lookup"><span data-stu-id="9f352-128">Method flushCache</span></span>

```xpp
public void flushCache(Int64 numbersequecerecordid)
```

### <a name="parameters---flushcache"></a><span data-ttu-id="9f352-129">パラメーター - flushCache</span><span class="sxs-lookup"><span data-stu-id="9f352-129">Parameters - flushCache</span></span>

<span data-ttu-id="9f352-130">numbersequecerecordid</span><span class="sxs-lookup"><span data-stu-id="9f352-130">numbersequecerecordid</span></span>  

## <a name="method-fillcache"></a><span data-ttu-id="9f352-131">メソッド fillCache</span><span class="sxs-lookup"><span data-stu-id="9f352-131">Method fillCache</span></span>

```xpp
public void fillCache(Int64 numbersequecerecordid, int nextRec, int blockSize)
```

### <a name="parameters---fillcache"></a><span data-ttu-id="9f352-132">パラメーター - fillCache</span><span class="sxs-lookup"><span data-stu-id="9f352-132">Parameters - fillCache</span></span>

<span data-ttu-id="9f352-133">numbersequecerecordid</span><span class="sxs-lookup"><span data-stu-id="9f352-133">numbersequecerecordid</span></span>  

<!-- -->

<span data-ttu-id="9f352-134">nextRec</span><span class="sxs-lookup"><span data-stu-id="9f352-134">nextRec</span></span>  

<!-- -->

<span data-ttu-id="9f352-135">blockSize</span><span class="sxs-lookup"><span data-stu-id="9f352-135">blockSize</span></span>  

## <a name="method-new"></a><span data-ttu-id="9f352-136">メソッド new</span><span class="sxs-lookup"><span data-stu-id="9f352-136">Method new</span></span>

<span data-ttu-id="9f352-137">NumberSequenceSessionLessCache クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="9f352-137">Initializes a new instance of the NumberSequenceSessionLessCache class.</span></span>

```xpp
public void new()
```


