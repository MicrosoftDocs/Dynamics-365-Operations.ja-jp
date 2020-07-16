---
title: RelationPath クラス
description: このトピックでは、RelationPath クラスについて説明します。
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
ms.openlocfilehash: e244ee5943113f51635e7a8b47545329d77276d6
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502852"
---
# <a name="class-relationpath"></a><span data-ttu-id="3d75e-103">クラス RelationPath</span><span class="sxs-lookup"><span data-stu-id="3d75e-103">Class RelationPath</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class RelationPath extends Object
```

## <a name="remarks"></a><span data-ttu-id="3d75e-104">備考</span><span class="sxs-lookup"><span data-stu-id="3d75e-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="3d75e-105">例</span><span class="sxs-lookup"><span data-stu-id="3d75e-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="3d75e-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="3d75e-106">Methods</span></span>

| <span data-ttu-id="3d75e-107">方法</span><span class="sxs-lookup"><span data-stu-id="3d75e-107">Method</span></span>                                                                                        | <span data-ttu-id="3d75e-108">説明</span><span class="sxs-lookup"><span data-stu-id="3d75e-108">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="3d75e-109">public boolean isEqualTo(RelationPath otherRelationPath)</span><span class="sxs-lookup"><span data-stu-id="3d75e-109">public boolean isEqualTo(RelationPath otherRelationPath)</span></span>                                      |                                                       |
| <span data-ttu-id="3d75e-110">public boolean isPathCyclical(boolean excludePathRootTable)</span><span class="sxs-lookup"><span data-stu-id="3d75e-110">public boolean isPathCyclical(boolean excludePathRootTable)</span></span>                                   |                                                       |
| <span data-ttu-id="3d75e-111">public boolean isPathValid()</span><span class="sxs-lookup"><span data-stu-id="3d75e-111">public boolean isPathValid()</span></span>                                                                  |                                                       |
| <span data-ttu-id="3d75e-112">public List pathAsList()</span><span class="sxs-lookup"><span data-stu-id="3d75e-112">public List pathAsList()</span></span>                                                                      |                                                       |
| <span data-ttu-id="3d75e-113">public str pathAsString(\[str delimiter\])</span><span class="sxs-lookup"><span data-stu-id="3d75e-113">public str pathAsString(\[str delimiter\])</span></span>                                                    |                                                       |
| <span data-ttu-id="3d75e-114">public str pathRelativeTable()</span><span class="sxs-lookup"><span data-stu-id="3d75e-114">public str pathRelativeTable()</span></span>                                                                |                                                       |
| <span data-ttu-id="3d75e-115">public str pathRootTable()</span><span class="sxs-lookup"><span data-stu-id="3d75e-115">public str pathRootTable()</span></span>                                                                    |                                                       |
| <span data-ttu-id="3d75e-116">::public static RelationPath construct(RelationPath sourceRelationPath)</span><span class="sxs-lookup"><span data-stu-id="3d75e-116">::public static RelationPath construct(RelationPath sourceRelationPath)</span></span>                       |                                                       |
| <span data-ttu-id="3d75e-117">::public static RelationPath constructFromPathList(str pathRootTableName, List relationPath)</span><span class="sxs-lookup"><span data-stu-id="3d75e-117">::public static RelationPath constructFromPathList(str pathRootTableName, List relationPath)</span></span>  |                                                       |
| <span data-ttu-id="3d75e-118">::public static RelationPath constructFromPathString(str pathRootTableName, str relationPath)</span><span class="sxs-lookup"><span data-stu-id="3d75e-118">::public static RelationPath constructFromPathString(str pathRootTableName, str relationPath)</span></span> |                                                       |
| <span data-ttu-id="3d75e-119">private void new()</span><span class="sxs-lookup"><span data-stu-id="3d75e-119">private void new()</span></span>                                                                            | <span data-ttu-id="3d75e-120">RelationPath クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="3d75e-120">Initializes a new instance of the RelationPath class.</span></span> |
| <span data-ttu-id="3d75e-121">public void trimPathAtFront()</span><span class="sxs-lookup"><span data-stu-id="3d75e-121">public void trimPathAtFront()</span></span>                                                                 |                                                       |
| <span data-ttu-id="3d75e-122">public void trimPathAtEnd()</span><span class="sxs-lookup"><span data-stu-id="3d75e-122">public void trimPathAtEnd()</span></span>                                                                   |                                                       |

## <a name="method-isequalto"></a><span data-ttu-id="3d75e-123">メソッド isEqualTo</span><span class="sxs-lookup"><span data-stu-id="3d75e-123">Method isEqualTo</span></span>

```xpp
public boolean isEqualTo(RelationPath otherRelationPath)
```

### <a name="parameters---isequalto"></a><span data-ttu-id="3d75e-124">パラメーター - isEqualTo</span><span class="sxs-lookup"><span data-stu-id="3d75e-124">Parameters - isEqualTo</span></span>

<span data-ttu-id="3d75e-125">otherRelationPath</span><span class="sxs-lookup"><span data-stu-id="3d75e-125">otherRelationPath</span></span>  

### <a name="return-value---isequalto"></a><span data-ttu-id="3d75e-126">戻り値 - isEqualTo</span><span class="sxs-lookup"><span data-stu-id="3d75e-126">Return Value - isEqualTo</span></span>

## <a name="method-ispathcyclical"></a><span data-ttu-id="3d75e-127">メソッド isPathCyclical</span><span class="sxs-lookup"><span data-stu-id="3d75e-127">Method isPathCyclical</span></span>

```xpp
public boolean isPathCyclical(boolean excludePathRootTable)
```

### <a name="parameters---ispathcyclical"></a><span data-ttu-id="3d75e-128">パラメーター - isPathCyclical</span><span class="sxs-lookup"><span data-stu-id="3d75e-128">Parameters - isPathCyclical</span></span>

<span data-ttu-id="3d75e-129">excludePathRootTable</span><span class="sxs-lookup"><span data-stu-id="3d75e-129">excludePathRootTable</span></span>  

### <a name="return-value---ispathcyclical"></a><span data-ttu-id="3d75e-130">戻り値 - isPathCyclical</span><span class="sxs-lookup"><span data-stu-id="3d75e-130">Return Value - isPathCyclical</span></span>

## <a name="method-ispathvalid"></a><span data-ttu-id="3d75e-131">メソッド isPathValid</span><span class="sxs-lookup"><span data-stu-id="3d75e-131">Method isPathValid</span></span>

```xpp
public boolean isPathValid()
```

### <a name="return-value---ispathvalid"></a><span data-ttu-id="3d75e-132">戻り値 - isPathValid</span><span class="sxs-lookup"><span data-stu-id="3d75e-132">Return Value - isPathValid</span></span>

## <a name="method-pathaslist"></a><span data-ttu-id="3d75e-133">メソッド pathAsList</span><span class="sxs-lookup"><span data-stu-id="3d75e-133">Method pathAsList</span></span>

```xpp
public List pathAsList()
```

### <a name="return-value---pathaslist"></a><span data-ttu-id="3d75e-134">戻り値 - pathAsList</span><span class="sxs-lookup"><span data-stu-id="3d75e-134">Return Value - pathAsList</span></span>

## <a name="method-pathasstring"></a><span data-ttu-id="3d75e-135">メソッド pathAsString</span><span class="sxs-lookup"><span data-stu-id="3d75e-135">Method pathAsString</span></span>

```xpp
public str pathAsString([str delimiter])
```

### <a name="parameters---pathasstring"></a><span data-ttu-id="3d75e-136">パラメーター - pathAsString</span><span class="sxs-lookup"><span data-stu-id="3d75e-136">Parameters - pathAsString</span></span>

<span data-ttu-id="3d75e-137">delimiter</span><span class="sxs-lookup"><span data-stu-id="3d75e-137">delimiter</span></span>  

### <a name="return-value---pathasstring"></a><span data-ttu-id="3d75e-138">戻り値 - pathAsString</span><span class="sxs-lookup"><span data-stu-id="3d75e-138">Return Value - pathAsString</span></span>

## <a name="method-pathrelativetable"></a><span data-ttu-id="3d75e-139">メソッド pathRelativeTable</span><span class="sxs-lookup"><span data-stu-id="3d75e-139">Method pathRelativeTable</span></span>

```xpp
public str pathRelativeTable()
```

### <a name="return-value---pathrelativetable"></a><span data-ttu-id="3d75e-140">戻り値 - pathRelativeTable</span><span class="sxs-lookup"><span data-stu-id="3d75e-140">Return Value - pathRelativeTable</span></span>

## <a name="method-pathroottable"></a><span data-ttu-id="3d75e-141">メソッド pathRootTable</span><span class="sxs-lookup"><span data-stu-id="3d75e-141">Method pathRootTable</span></span>

```xpp
public str pathRootTable()
```

### <a name="return-value---pathroottable"></a><span data-ttu-id="3d75e-142">戻り値 - pathRootTable</span><span class="sxs-lookup"><span data-stu-id="3d75e-142">Return Value - pathRootTable</span></span>

## <a name="method-construct"></a><span data-ttu-id="3d75e-143">メソッド construct</span><span class="sxs-lookup"><span data-stu-id="3d75e-143">Method construct</span></span>

```xpp
public static RelationPath construct(RelationPath sourceRelationPath)
```

### <a name="parameters---construct"></a><span data-ttu-id="3d75e-144">パラメーター - construct</span><span class="sxs-lookup"><span data-stu-id="3d75e-144">Parameters - construct</span></span>

<span data-ttu-id="3d75e-145">sourceRelationPath</span><span class="sxs-lookup"><span data-stu-id="3d75e-145">sourceRelationPath</span></span>  

### <a name="return-value---construct"></a><span data-ttu-id="3d75e-146">戻り値 - construct</span><span class="sxs-lookup"><span data-stu-id="3d75e-146">Return Value - construct</span></span>

## <a name="method-constructfrompathlist"></a><span data-ttu-id="3d75e-147">メソッド constructFromPathList</span><span class="sxs-lookup"><span data-stu-id="3d75e-147">Method constructFromPathList</span></span>

```xpp
public static RelationPath constructFromPathList(str pathRootTableName, List relationPath)
```

### <a name="parameters---constructfrompathlist"></a><span data-ttu-id="3d75e-148">パラメーター - constructFromPathList</span><span class="sxs-lookup"><span data-stu-id="3d75e-148">Parameters - constructFromPathList</span></span>

<span data-ttu-id="3d75e-149">pathRootTableName</span><span class="sxs-lookup"><span data-stu-id="3d75e-149">pathRootTableName</span></span>  

<!-- -->

<span data-ttu-id="3d75e-150">relationPath</span><span class="sxs-lookup"><span data-stu-id="3d75e-150">relationPath</span></span>  

### <a name="return-value---constructfrompathlist"></a><span data-ttu-id="3d75e-151">戻り値 - constructFromPathList</span><span class="sxs-lookup"><span data-stu-id="3d75e-151">Return Value - constructFromPathList</span></span>

## <a name="method-constructfrompathstring"></a><span data-ttu-id="3d75e-152">メソッド constructFromPathString</span><span class="sxs-lookup"><span data-stu-id="3d75e-152">Method constructFromPathString</span></span>

```xpp
public static RelationPath constructFromPathString(str pathRootTableName, str relationPath)
```

### <a name="parameters---constructfrompathstring"></a><span data-ttu-id="3d75e-153">パラメーター - constructFromPathString</span><span class="sxs-lookup"><span data-stu-id="3d75e-153">Parameters - constructFromPathString</span></span>

<span data-ttu-id="3d75e-154">pathRootTableName</span><span class="sxs-lookup"><span data-stu-id="3d75e-154">pathRootTableName</span></span>  

<!-- -->

<span data-ttu-id="3d75e-155">relationPath</span><span class="sxs-lookup"><span data-stu-id="3d75e-155">relationPath</span></span>  

### <a name="return-value---constructfrompathstring"></a><span data-ttu-id="3d75e-156">戻り値 - constructFromPathString</span><span class="sxs-lookup"><span data-stu-id="3d75e-156">Return Value - constructFromPathString</span></span>

## <a name="method-new"></a><span data-ttu-id="3d75e-157">メソッド new</span><span class="sxs-lookup"><span data-stu-id="3d75e-157">Method new</span></span>

<span data-ttu-id="3d75e-158">RelationPath クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="3d75e-158">Initializes a new instance of the RelationPath class.</span></span>

```xpp
private void new()
```

## <a name="method-trimpathatfront"></a><span data-ttu-id="3d75e-159">メソッド trimPathAtFront</span><span class="sxs-lookup"><span data-stu-id="3d75e-159">Method trimPathAtFront</span></span>

```xpp
public void trimPathAtFront()
```

## <a name="method-trimpathatend"></a><span data-ttu-id="3d75e-160">メソッド trimPathAtEnd</span><span class="sxs-lookup"><span data-stu-id="3d75e-160">Method trimPathAtEnd</span></span>

```xpp
public void trimPathAtEnd()
```

