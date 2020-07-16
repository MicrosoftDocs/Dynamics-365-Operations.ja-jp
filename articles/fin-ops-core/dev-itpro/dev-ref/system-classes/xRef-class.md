---
title: xRef クラス
description: このトピックでは、xRef クラスについて説明します。
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
ms.openlocfilehash: c790f8540773f3039301fcc91ba75b14a5a677d0
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502677"
---
# <a name="class-xref"></a><span data-ttu-id="8e227-103">クラス xRef</span><span class="sxs-lookup"><span data-stu-id="8e227-103">Class xRef</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class xRef extends Object
```

## <a name="remarks"></a><span data-ttu-id="8e227-104">備考</span><span class="sxs-lookup"><span data-stu-id="8e227-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="8e227-105">例</span><span class="sxs-lookup"><span data-stu-id="8e227-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="8e227-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="8e227-106">Methods</span></span>

| <span data-ttu-id="8e227-107">方法</span><span class="sxs-lookup"><span data-stu-id="8e227-107">Method</span></span>                                         | <span data-ttu-id="8e227-108">説明</span><span class="sxs-lookup"><span data-stu-id="8e227-108">Description</span></span>                                     |
|------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="8e227-109">public AccessLevel accessLevel()</span><span class="sxs-lookup"><span data-stu-id="8e227-109">public AccessLevel accessLevel()</span></span>               |                                                 |
| <span data-ttu-id="8e227-110">public int column()</span><span class="sxs-lookup"><span data-stu-id="8e227-110">public int column()</span></span>                            |                                                 |
| <span data-ttu-id="8e227-111">public container contents()</span><span class="sxs-lookup"><span data-stu-id="8e227-111">public container contents()</span></span>                    |                                                 |
| <span data-ttu-id="8e227-112">public xRefKind kind()</span><span class="sxs-lookup"><span data-stu-id="8e227-112">public xRefKind kind()</span></span>                         |                                                 |
| <span data-ttu-id="8e227-113">public int line()</span><span class="sxs-lookup"><span data-stu-id="8e227-113">public int line()</span></span>                              |                                                 |
| <span data-ttu-id="8e227-114">public XRefMode mode()</span><span class="sxs-lookup"><span data-stu-id="8e227-114">public XRefMode mode()</span></span>                         |                                                 |
| <span data-ttu-id="8e227-115">public str name()</span><span class="sxs-lookup"><span data-stu-id="8e227-115">public str name()</span></span>                              |                                                 |
| <span data-ttu-id="8e227-116">public str path()</span><span class="sxs-lookup"><span data-stu-id="8e227-116">public str path()</span></span>                              |                                                 |
| <span data-ttu-id="8e227-117">public XRefReference reference()</span><span class="sxs-lookup"><span data-stu-id="8e227-117">public XRefReference reference()</span></span>               |                                                 |
| <span data-ttu-id="8e227-118">public int typeHandle()</span><span class="sxs-lookup"><span data-stu-id="8e227-118">public int typeHandle()</span></span>                        |                                                 |
| <span data-ttu-id="8e227-119">public str typeName(xRefKind kind, int handle)</span><span class="sxs-lookup"><span data-stu-id="8e227-119">public str typeName(xRefKind kind, int handle)</span></span> |                                                 |
| <span data-ttu-id="8e227-120">public void new(container data)</span><span class="sxs-lookup"><span data-stu-id="8e227-120">public void new(container data)</span></span>                | <span data-ttu-id="8e227-121">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="8e227-121">Initializes a new instance of the Object class.</span></span> |
| <span data-ttu-id="8e227-122">public void init()</span><span class="sxs-lookup"><span data-stu-id="8e227-122">public void init()</span></span>                             |                                                 |
| <span data-ttu-id="8e227-123">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="8e227-123">public void finalize()</span></span>                         |                                                 |
| <span data-ttu-id="8e227-124">public void next()</span><span class="sxs-lookup"><span data-stu-id="8e227-124">public void next()</span></span>                             |                                                 |

## <a name="method-accesslevel"></a><span data-ttu-id="8e227-125">メソッド accessLevel</span><span class="sxs-lookup"><span data-stu-id="8e227-125">Method accessLevel</span></span>

```xpp
public AccessLevel accessLevel()
```

### <a name="return-value---accesslevel"></a><span data-ttu-id="8e227-126">戻り値 - accessLevel</span><span class="sxs-lookup"><span data-stu-id="8e227-126">Return Value - accessLevel</span></span>

## <a name="method-column"></a><span data-ttu-id="8e227-127">メソッド column</span><span class="sxs-lookup"><span data-stu-id="8e227-127">Method column</span></span>

```xpp
public int column()
```

### <a name="return-value---column"></a><span data-ttu-id="8e227-128">戻り値 - column</span><span class="sxs-lookup"><span data-stu-id="8e227-128">Return Value - column</span></span>

## <a name="method-contents"></a><span data-ttu-id="8e227-129">メソッド contents</span><span class="sxs-lookup"><span data-stu-id="8e227-129">Method contents</span></span>

```xpp
public container contents()
```

### <a name="return-value---contents"></a><span data-ttu-id="8e227-130">戻り値 - contents</span><span class="sxs-lookup"><span data-stu-id="8e227-130">Return Value - contents</span></span>

## <a name="method-kind"></a><span data-ttu-id="8e227-131">メソッド kind</span><span class="sxs-lookup"><span data-stu-id="8e227-131">Method kind</span></span>

```xpp
public xRefKind kind()
```

### <a name="return-value---kind"></a><span data-ttu-id="8e227-132">戻り値 - kind</span><span class="sxs-lookup"><span data-stu-id="8e227-132">Return Value - kind</span></span>

## <a name="method-line"></a><span data-ttu-id="8e227-133">メソッド line</span><span class="sxs-lookup"><span data-stu-id="8e227-133">Method line</span></span>

```xpp
public int line()
```

### <a name="return-value---line"></a><span data-ttu-id="8e227-134">戻り値 - line</span><span class="sxs-lookup"><span data-stu-id="8e227-134">Return Value - line</span></span>

## <a name="method-mode"></a><span data-ttu-id="8e227-135">メソッド mode</span><span class="sxs-lookup"><span data-stu-id="8e227-135">Method mode</span></span>

```xpp
public XRefMode mode()
```

### <a name="return-value---mode"></a><span data-ttu-id="8e227-136">戻り値 - mode</span><span class="sxs-lookup"><span data-stu-id="8e227-136">Return Value - mode</span></span>

## <a name="method-name"></a><span data-ttu-id="8e227-137">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8e227-137">Method name</span></span>

```xpp
public str name()
```

### <a name="return-value---name"></a><span data-ttu-id="8e227-138">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="8e227-138">Return Value - name</span></span>

## <a name="method-path"></a><span data-ttu-id="8e227-139">メソッド path</span><span class="sxs-lookup"><span data-stu-id="8e227-139">Method path</span></span>

```xpp
public str path()
```

### <a name="return-value---path"></a><span data-ttu-id="8e227-140">戻り値 - path</span><span class="sxs-lookup"><span data-stu-id="8e227-140">Return Value - path</span></span>

## <a name="method-reference"></a><span data-ttu-id="8e227-141">メソッド reference</span><span class="sxs-lookup"><span data-stu-id="8e227-141">Method reference</span></span>

```xpp
public XRefReference reference()
```

### <a name="return-value---reference"></a><span data-ttu-id="8e227-142">戻り値 - reference</span><span class="sxs-lookup"><span data-stu-id="8e227-142">Return Value - reference</span></span>

## <a name="method-typehandle"></a><span data-ttu-id="8e227-143">メソッド typeHandle</span><span class="sxs-lookup"><span data-stu-id="8e227-143">Method typeHandle</span></span>

```xpp
public int typeHandle()
```

### <a name="return-value---typehandle"></a><span data-ttu-id="8e227-144">戻り値 - typeHandle</span><span class="sxs-lookup"><span data-stu-id="8e227-144">Return Value - typeHandle</span></span>

## <a name="method-typename"></a><span data-ttu-id="8e227-145">メソッド typeName</span><span class="sxs-lookup"><span data-stu-id="8e227-145">Method typeName</span></span>

```xpp
public str typeName(xRefKind kind, int handle)
```

### <a name="parameters---typename"></a><span data-ttu-id="8e227-146">パラメーター - typeName</span><span class="sxs-lookup"><span data-stu-id="8e227-146">Parameters - typeName</span></span>

<span data-ttu-id="8e227-147">kind</span><span class="sxs-lookup"><span data-stu-id="8e227-147">kind</span></span>  

<!-- -->

<span data-ttu-id="8e227-148">handle</span><span class="sxs-lookup"><span data-stu-id="8e227-148">handle</span></span>  

### <a name="return-value---typename"></a><span data-ttu-id="8e227-149">戻り値 - typeName</span><span class="sxs-lookup"><span data-stu-id="8e227-149">Return Value - typeName</span></span>

## <a name="method-new"></a><span data-ttu-id="8e227-150">メソッド new</span><span class="sxs-lookup"><span data-stu-id="8e227-150">Method new</span></span>

<span data-ttu-id="8e227-151">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="8e227-151">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(container data)
```

### <a name="parameters---new"></a><span data-ttu-id="8e227-152">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="8e227-152">Parameters - new</span></span>

<span data-ttu-id="8e227-153">データ</span><span class="sxs-lookup"><span data-stu-id="8e227-153">data</span></span>  

## <a name="method-init"></a><span data-ttu-id="8e227-154">メソッド init</span><span class="sxs-lookup"><span data-stu-id="8e227-154">Method init</span></span>

```xpp
public void init()
```

## <a name="method-finalize"></a><span data-ttu-id="8e227-155">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="8e227-155">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-next"></a><span data-ttu-id="8e227-156">メソッド next</span><span class="sxs-lookup"><span data-stu-id="8e227-156">Method next</span></span>

```xpp
public void next()
```

