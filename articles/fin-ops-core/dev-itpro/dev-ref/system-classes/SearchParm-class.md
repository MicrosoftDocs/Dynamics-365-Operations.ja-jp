---
title: SearchParm クラス
description: このトピックでは、SearchParm クラスについて説明します。
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
ms.openlocfilehash: c06c6cb4c8391d1e5ddefb54a20296985b4c87ed
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502816"
---
# <a name="class-searchparm"></a><span data-ttu-id="a0b87-103">クラス SearchParm</span><span class="sxs-lookup"><span data-stu-id="a0b87-103">Class SearchParm</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class SearchParm extends Object
```

<span data-ttu-id="a0b87-104">SearchParm クラスは、カーネルと sysTreeSearch クラス間のインターフェイスとして機能し、アプリケーション オブジェクト ツリー (AOT) で検索できるようにします。</span><span class="sxs-lookup"><span data-stu-id="a0b87-104">The SearchParm class serves as an interface between the kernel and the sysTreeSearch class, and enables searches in the  Application Object Tree (AOT).</span></span>

## <a name="remarks"></a><span data-ttu-id="a0b87-105">備考</span><span class="sxs-lookup"><span data-stu-id="a0b87-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="a0b87-106">例</span><span class="sxs-lookup"><span data-stu-id="a0b87-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="a0b87-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="a0b87-107">Methods</span></span>

| <span data-ttu-id="a0b87-108">方法</span><span class="sxs-lookup"><span data-stu-id="a0b87-108">Method</span></span>                                          | <span data-ttu-id="a0b87-109">説明</span><span class="sxs-lookup"><span data-stu-id="a0b87-109">Description</span></span> |
|-------------------------------------------------|-------------|
| <span data-ttu-id="a0b87-110">public str nodeName(\[str name\])</span><span class="sxs-lookup"><span data-stu-id="a0b87-110">public str nodeName(\[str name\])</span></span>               |             |
| <span data-ttu-id="a0b87-111">public int nodeType(\[int type\])</span><span class="sxs-lookup"><span data-stu-id="a0b87-111">public int nodeType(\[int type\])</span></span>               |             |
| <span data-ttu-id="a0b87-112">public str nodeTypeArray()</span><span class="sxs-lookup"><span data-stu-id="a0b87-112">public str nodeTypeArray()</span></span>                      |             |
| <span data-ttu-id="a0b87-113">public str propertyName(\[str name\])</span><span class="sxs-lookup"><span data-stu-id="a0b87-113">public str propertyName(\[str name\])</span></span>           |             |
| <span data-ttu-id="a0b87-114">public str propertyValue(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a0b87-114">public str propertyValue(\[str value\])</span></span>         |             |
| <span data-ttu-id="a0b87-115">public str replaceString(\[str replaceString\])</span><span class="sxs-lookup"><span data-stu-id="a0b87-115">public str replaceString(\[str replaceString\])</span></span> |             |
| <span data-ttu-id="a0b87-116">public int searchFlag(\[int flag\])</span><span class="sxs-lookup"><span data-stu-id="a0b87-116">public int searchFlag(\[int flag\])</span></span>             |             |
| <span data-ttu-id="a0b87-117">public str searchString(\[str searchString\])</span><span class="sxs-lookup"><span data-stu-id="a0b87-117">public str searchString(\[str searchString\])</span></span>   |             |
| <span data-ttu-id="a0b87-118">public int searchType(\[int type\])</span><span class="sxs-lookup"><span data-stu-id="a0b87-118">public int searchType(\[int type\])</span></span>             |             |
| <span data-ttu-id="a0b87-119">public boolean startSearch()</span><span class="sxs-lookup"><span data-stu-id="a0b87-119">public boolean startSearch()</span></span>                    |             |
| <span data-ttu-id="a0b87-120">public TreeNode topNode(\[TreeNode node\])</span><span class="sxs-lookup"><span data-stu-id="a0b87-120">public TreeNode topNode(\[TreeNode node\])</span></span>      |             |
| <span data-ttu-id="a0b87-121">public str topNodeName(\[str name\])</span><span class="sxs-lookup"><span data-stu-id="a0b87-121">public str topNodeName(\[str name\])</span></span>            |             |
| <span data-ttu-id="a0b87-122">public int topNodeType(\[int type\])</span><span class="sxs-lookup"><span data-stu-id="a0b87-122">public int topNodeType(\[int type\])</span></span>            |             |
| <span data-ttu-id="a0b87-123">public void preSearch()</span><span class="sxs-lookup"><span data-stu-id="a0b87-123">public void preSearch()</span></span>                         |             |
| <span data-ttu-id="a0b87-124">public void killSearch()</span><span class="sxs-lookup"><span data-stu-id="a0b87-124">public void killSearch()</span></span>                        |             |

## <a name="method-nodename"></a><span data-ttu-id="a0b87-125">メソッド nodeName</span><span class="sxs-lookup"><span data-stu-id="a0b87-125">Method nodeName</span></span>

```xpp
public str nodeName([str name])
```

### <a name="parameters---nodename"></a><span data-ttu-id="a0b87-126">パラメーター - nodeName</span><span class="sxs-lookup"><span data-stu-id="a0b87-126">Parameters - nodeName</span></span>

<span data-ttu-id="a0b87-127">名前</span><span class="sxs-lookup"><span data-stu-id="a0b87-127">name</span></span>  

### <a name="return-value---nodename"></a><span data-ttu-id="a0b87-128">戻り値 - nodeName</span><span class="sxs-lookup"><span data-stu-id="a0b87-128">Return Value - nodeName</span></span>

## <a name="method-nodetype"></a><span data-ttu-id="a0b87-129">メソッド nodeType</span><span class="sxs-lookup"><span data-stu-id="a0b87-129">Method nodeType</span></span>

```xpp
public int nodeType([int type])
```

### <a name="parameters---nodetype"></a><span data-ttu-id="a0b87-130">パラメーター - nodeType</span><span class="sxs-lookup"><span data-stu-id="a0b87-130">Parameters - nodeType</span></span>

<span data-ttu-id="a0b87-131">タイプ</span><span class="sxs-lookup"><span data-stu-id="a0b87-131">type</span></span>  

### <a name="return-value---nodetype"></a><span data-ttu-id="a0b87-132">戻り値 - nodeType</span><span class="sxs-lookup"><span data-stu-id="a0b87-132">Return Value - nodeType</span></span>

## <a name="method-nodetypearray"></a><span data-ttu-id="a0b87-133">メソッド nodeTypeArray</span><span class="sxs-lookup"><span data-stu-id="a0b87-133">Method nodeTypeArray</span></span>

```xpp
public str nodeTypeArray()
```

### <a name="return-value---nodetypearray"></a><span data-ttu-id="a0b87-134">戻り値 - nodeTypeArray</span><span class="sxs-lookup"><span data-stu-id="a0b87-134">Return Value - nodeTypeArray</span></span>

## <a name="method-propertyname"></a><span data-ttu-id="a0b87-135">メソッド propertyName</span><span class="sxs-lookup"><span data-stu-id="a0b87-135">Method propertyName</span></span>

```xpp
public str propertyName([str name])
```

### <a name="parameters---propertyname"></a><span data-ttu-id="a0b87-136">パラメーター - propertyName</span><span class="sxs-lookup"><span data-stu-id="a0b87-136">Parameters - propertyName</span></span>

<span data-ttu-id="a0b87-137">名前</span><span class="sxs-lookup"><span data-stu-id="a0b87-137">name</span></span>  

### <a name="return-value---propertyname"></a><span data-ttu-id="a0b87-138">戻り値 - propertyName</span><span class="sxs-lookup"><span data-stu-id="a0b87-138">Return Value - propertyName</span></span>

## <a name="method-propertyvalue"></a><span data-ttu-id="a0b87-139">メソッド propertyValue</span><span class="sxs-lookup"><span data-stu-id="a0b87-139">Method propertyValue</span></span>

```xpp
public str propertyValue([str value])
```

### <a name="parameters---propertyvalue"></a><span data-ttu-id="a0b87-140">パラメーター - propertyValue</span><span class="sxs-lookup"><span data-stu-id="a0b87-140">Parameters - propertyValue</span></span>

<span data-ttu-id="a0b87-141">値</span><span class="sxs-lookup"><span data-stu-id="a0b87-141">value</span></span>  

### <a name="return-value---propertyvalue"></a><span data-ttu-id="a0b87-142">戻り値 - propertyValue</span><span class="sxs-lookup"><span data-stu-id="a0b87-142">Return Value - propertyValue</span></span>

## <a name="method-replacestring"></a><span data-ttu-id="a0b87-143">メソッド replaceString</span><span class="sxs-lookup"><span data-stu-id="a0b87-143">Method replaceString</span></span>

```xpp
public str replaceString([str replaceString])
```

### <a name="parameters---replacestring"></a><span data-ttu-id="a0b87-144">パラメーター - replaceString</span><span class="sxs-lookup"><span data-stu-id="a0b87-144">Parameters - replaceString</span></span>

<span data-ttu-id="a0b87-145">replaceString</span><span class="sxs-lookup"><span data-stu-id="a0b87-145">replaceString</span></span>  

### <a name="return-value---replacestring"></a><span data-ttu-id="a0b87-146">戻り値 - replaceString</span><span class="sxs-lookup"><span data-stu-id="a0b87-146">Return Value - replaceString</span></span>

## <a name="method-searchflag"></a><span data-ttu-id="a0b87-147">メソッド searchFlag</span><span class="sxs-lookup"><span data-stu-id="a0b87-147">Method searchFlag</span></span>

```xpp
public int searchFlag([int flag])
```

### <a name="parameters---searchflag"></a><span data-ttu-id="a0b87-148">パラメーター - searchFlag</span><span class="sxs-lookup"><span data-stu-id="a0b87-148">Parameters - searchFlag</span></span>

<span data-ttu-id="a0b87-149">flag</span><span class="sxs-lookup"><span data-stu-id="a0b87-149">flag</span></span>  

### <a name="return-value---searchflag"></a><span data-ttu-id="a0b87-150">戻り値 - searchFlag</span><span class="sxs-lookup"><span data-stu-id="a0b87-150">Return Value - searchFlag</span></span>

## <a name="method-searchstring"></a><span data-ttu-id="a0b87-151">メソッド searchString</span><span class="sxs-lookup"><span data-stu-id="a0b87-151">Method searchString</span></span>

```xpp
public str searchString([str searchString])
```

### <a name="parameters---searchstring"></a><span data-ttu-id="a0b87-152">パラメーター - searchString</span><span class="sxs-lookup"><span data-stu-id="a0b87-152">Parameters - searchString</span></span>

<span data-ttu-id="a0b87-153">searchString</span><span class="sxs-lookup"><span data-stu-id="a0b87-153">searchString</span></span>  

### <a name="return-value---searchstring"></a><span data-ttu-id="a0b87-154">戻り値 - searchString</span><span class="sxs-lookup"><span data-stu-id="a0b87-154">Return Value - searchString</span></span>

## <a name="method-searchtype"></a><span data-ttu-id="a0b87-155">メソッド searchType</span><span class="sxs-lookup"><span data-stu-id="a0b87-155">Method searchType</span></span>

```xpp
public int searchType([int type])
```

### <a name="parameters---searchtype"></a><span data-ttu-id="a0b87-156">パラメーター - searchType</span><span class="sxs-lookup"><span data-stu-id="a0b87-156">Parameters - searchType</span></span>

<span data-ttu-id="a0b87-157">タイプ</span><span class="sxs-lookup"><span data-stu-id="a0b87-157">type</span></span>  

### <a name="return-value---searchtype"></a><span data-ttu-id="a0b87-158">戻り値 - searchType</span><span class="sxs-lookup"><span data-stu-id="a0b87-158">Return Value - searchType</span></span>

## <a name="method-startsearch"></a><span data-ttu-id="a0b87-159">メソッド startSearch</span><span class="sxs-lookup"><span data-stu-id="a0b87-159">Method startSearch</span></span>

```xpp
public boolean startSearch()
```

### <a name="return-value---startsearch"></a><span data-ttu-id="a0b87-160">戻り値 - startSearch</span><span class="sxs-lookup"><span data-stu-id="a0b87-160">Return Value - startSearch</span></span>

## <a name="method-topnode"></a><span data-ttu-id="a0b87-161">メソッド topNode</span><span class="sxs-lookup"><span data-stu-id="a0b87-161">Method topNode</span></span>

```xpp
public TreeNode topNode([TreeNode node])
```

### <a name="parameters---topnode"></a><span data-ttu-id="a0b87-162">パラメーター - topNode</span><span class="sxs-lookup"><span data-stu-id="a0b87-162">Parameters - topNode</span></span>

<span data-ttu-id="a0b87-163">node</span><span class="sxs-lookup"><span data-stu-id="a0b87-163">node</span></span>  

### <a name="return-value---topnode"></a><span data-ttu-id="a0b87-164">戻り値 - topNode</span><span class="sxs-lookup"><span data-stu-id="a0b87-164">Return Value - topNode</span></span>

## <a name="method-topnodename"></a><span data-ttu-id="a0b87-165">メソッド topNodeName</span><span class="sxs-lookup"><span data-stu-id="a0b87-165">Method topNodeName</span></span>

```xpp
public str topNodeName([str name])
```

### <a name="parameters---topnodename"></a><span data-ttu-id="a0b87-166">パラメーター - topNodeName</span><span class="sxs-lookup"><span data-stu-id="a0b87-166">Parameters - topNodeName</span></span>

<span data-ttu-id="a0b87-167">名前</span><span class="sxs-lookup"><span data-stu-id="a0b87-167">name</span></span>  

### <a name="return-value---topnodename"></a><span data-ttu-id="a0b87-168">戻り値 - topNodeName</span><span class="sxs-lookup"><span data-stu-id="a0b87-168">Return Value - topNodeName</span></span>

## <a name="method-topnodetype"></a><span data-ttu-id="a0b87-169">メソッド topNodeType</span><span class="sxs-lookup"><span data-stu-id="a0b87-169">Method topNodeType</span></span>

```xpp
public int topNodeType([int type])
```

### <a name="parameters---topnodetype"></a><span data-ttu-id="a0b87-170">パラメーター - topNodeType</span><span class="sxs-lookup"><span data-stu-id="a0b87-170">Parameters - topNodeType</span></span>

<span data-ttu-id="a0b87-171">タイプ</span><span class="sxs-lookup"><span data-stu-id="a0b87-171">type</span></span>  

### <a name="return-value---topnodetype"></a><span data-ttu-id="a0b87-172">戻り値 - topNodeType</span><span class="sxs-lookup"><span data-stu-id="a0b87-172">Return Value - topNodeType</span></span>

## <a name="method-presearch"></a><span data-ttu-id="a0b87-173">メソッド preSearch</span><span class="sxs-lookup"><span data-stu-id="a0b87-173">Method preSearch</span></span>

```xpp
public void preSearch()
```

## <a name="method-killsearch"></a><span data-ttu-id="a0b87-174">メソッド killSearch</span><span class="sxs-lookup"><span data-stu-id="a0b87-174">Method killSearch</span></span>

```xpp
public void killSearch()
```

