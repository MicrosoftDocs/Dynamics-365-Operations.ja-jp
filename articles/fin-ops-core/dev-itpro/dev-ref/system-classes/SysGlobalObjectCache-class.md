---
title: SysGlobalObjectCache クラス
description: このトピックでは、SysGlobalObjectCache クラスについて説明します。
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
ms.openlocfilehash: efb8fdcc1323738717ee95407931a8ce75395845
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502793"
---
# <a name="class-sysglobalobjectcache"></a><span data-ttu-id="15908-103">クラス SysGlobalObjectCache</span><span class="sxs-lookup"><span data-stu-id="15908-103">Class SysGlobalObjectCache</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class SysGlobalObjectCache extends Object
```

## <a name="remarks"></a><span data-ttu-id="15908-104">備考</span><span class="sxs-lookup"><span data-stu-id="15908-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="15908-105">例</span><span class="sxs-lookup"><span data-stu-id="15908-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="15908-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="15908-106">Methods</span></span>

| <span data-ttu-id="15908-107">方法</span><span class="sxs-lookup"><span data-stu-id="15908-107">Method</span></span>                                                                           | <span data-ttu-id="15908-108">説明</span><span class="sxs-lookup"><span data-stu-id="15908-108">Description</span></span>                                                   |
|----------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="15908-109">public container find(GlobalObjectCacheScope scope, container key)</span><span class="sxs-lookup"><span data-stu-id="15908-109">public container find(GlobalObjectCacheScope scope, container key)</span></span>               |                                                               |
| <span data-ttu-id="15908-110">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="15908-110">public void finalize()</span></span>                                                           |                                                               |
| <span data-ttu-id="15908-111">public void remove(GlobalObjectCacheScope scope, container key)</span><span class="sxs-lookup"><span data-stu-id="15908-111">public void remove(GlobalObjectCacheScope scope, container key)</span></span>                  |                                                               |
| <span data-ttu-id="15908-112">public void print(GlobalObjectCacheScope scope)</span><span class="sxs-lookup"><span data-stu-id="15908-112">public void print(GlobalObjectCacheScope scope)</span></span>                                  |                                                               |
| <span data-ttu-id="15908-113">public void clear(GlobalObjectCacheScope scope)</span><span class="sxs-lookup"><span data-stu-id="15908-113">public void clear(GlobalObjectCacheScope scope)</span></span>                                  |                                                               |
| <span data-ttu-id="15908-114">::public static void clearAllCaches()</span><span class="sxs-lookup"><span data-stu-id="15908-114">::public static void clearAllCaches()</span></span>                                            |                                                               |
| <span data-ttu-id="15908-115">public void new()</span><span class="sxs-lookup"><span data-stu-id="15908-115">public void new()</span></span>                                                                | <span data-ttu-id="15908-116">SysGlobalObjectCache クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="15908-116">Initializes a new instance of the SysGlobalObjectCache class.</span></span> |
| <span data-ttu-id="15908-117">public void insert(GlobalObjectCacheScope scope, container key, container value)</span><span class="sxs-lookup"><span data-stu-id="15908-117">public void insert(GlobalObjectCacheScope scope, container key, container value)</span></span> |                                                               |

## <a name="method-find"></a><span data-ttu-id="15908-118">メソッド find</span><span class="sxs-lookup"><span data-stu-id="15908-118">Method find</span></span>

```xpp
public container find(GlobalObjectCacheScope scope, container key)
```

### <a name="parameters---find"></a><span data-ttu-id="15908-119">パラメーター - find</span><span class="sxs-lookup"><span data-stu-id="15908-119">Parameters - find</span></span>

<span data-ttu-id="15908-120">scope</span><span class="sxs-lookup"><span data-stu-id="15908-120">scope</span></span>  

<!-- -->

<span data-ttu-id="15908-121">キー</span><span class="sxs-lookup"><span data-stu-id="15908-121">key</span></span>  

### <a name="return-value---find"></a><span data-ttu-id="15908-122">戻り値 - find</span><span class="sxs-lookup"><span data-stu-id="15908-122">Return Value - find</span></span>

## <a name="method-finalize"></a><span data-ttu-id="15908-123">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="15908-123">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-remove"></a><span data-ttu-id="15908-124">メソッド remove</span><span class="sxs-lookup"><span data-stu-id="15908-124">Method remove</span></span>

```xpp
public void remove(GlobalObjectCacheScope scope, container key)
```

### <a name="parameters---remove"></a><span data-ttu-id="15908-125">パラメーター - remove</span><span class="sxs-lookup"><span data-stu-id="15908-125">Parameters - remove</span></span>

<span data-ttu-id="15908-126">scope</span><span class="sxs-lookup"><span data-stu-id="15908-126">scope</span></span>  

<!-- -->

<span data-ttu-id="15908-127">キー</span><span class="sxs-lookup"><span data-stu-id="15908-127">key</span></span>  

## <a name="method-print"></a><span data-ttu-id="15908-128">メソッド print</span><span class="sxs-lookup"><span data-stu-id="15908-128">Method print</span></span>

```xpp
public void print(GlobalObjectCacheScope scope)
```

### <a name="parameters---print"></a><span data-ttu-id="15908-129">パラメーター - print</span><span class="sxs-lookup"><span data-stu-id="15908-129">Parameters - print</span></span>

<span data-ttu-id="15908-130">scope</span><span class="sxs-lookup"><span data-stu-id="15908-130">scope</span></span>  

## <a name="method-clear"></a><span data-ttu-id="15908-131">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="15908-131">Method clear</span></span>

```xpp
public void clear(GlobalObjectCacheScope scope)
```

### <a name="parameters---clear"></a><span data-ttu-id="15908-132">パラメーター - clear</span><span class="sxs-lookup"><span data-stu-id="15908-132">Parameters - clear</span></span>

<span data-ttu-id="15908-133">scope</span><span class="sxs-lookup"><span data-stu-id="15908-133">scope</span></span>  

## <a name="method-clearallcaches"></a><span data-ttu-id="15908-134">メソッド clearAllCaches</span><span class="sxs-lookup"><span data-stu-id="15908-134">Method clearAllCaches</span></span>

```xpp
public static void clearAllCaches()
```

## <a name="method-new"></a><span data-ttu-id="15908-135">メソッド new</span><span class="sxs-lookup"><span data-stu-id="15908-135">Method new</span></span>

<span data-ttu-id="15908-136">SysGlobalObjectCache クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="15908-136">Initializes a new instance of the SysGlobalObjectCache class.</span></span>

```xpp
public void new()
```

## <a name="method-insert"></a><span data-ttu-id="15908-137">メソッド insert</span><span class="sxs-lookup"><span data-stu-id="15908-137">Method insert</span></span>

```xpp
public void insert(GlobalObjectCacheScope scope, container key, container value)
```

### <a name="parameters---insert"></a><span data-ttu-id="15908-138">パラメーター - insert</span><span class="sxs-lookup"><span data-stu-id="15908-138">Parameters - insert</span></span>

<span data-ttu-id="15908-139">scope</span><span class="sxs-lookup"><span data-stu-id="15908-139">scope</span></span>  

<!-- -->

<span data-ttu-id="15908-140">キー</span><span class="sxs-lookup"><span data-stu-id="15908-140">key</span></span>  

<!-- -->

<span data-ttu-id="15908-141">値</span><span class="sxs-lookup"><span data-stu-id="15908-141">value</span></span>  

