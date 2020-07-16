---
title: FormSegment クラス
description: このトピックでは、FormSegment クラスについて説明します。
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
ms.openlocfilehash: 883c8b6f28a0e8e1287e27784d6300ec752d8895
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502613"
---
# <a name="class-formsegment"></a><span data-ttu-id="fa72d-103">クラス FormSegment</span><span class="sxs-lookup"><span data-stu-id="fa72d-103">Class FormSegment</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormSegment extends Object
```

<span data-ttu-id="fa72d-104">FormSegment クラスは、SegmentedEntry コントロールでセグメントを表すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa72d-104">The FormSegment class is used to represent a segment in the SegmentedEntry control.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa72d-105">備考</span><span class="sxs-lookup"><span data-stu-id="fa72d-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="fa72d-106">例</span><span class="sxs-lookup"><span data-stu-id="fa72d-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="fa72d-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="fa72d-107">Methods</span></span>

| <span data-ttu-id="fa72d-108">方法</span><span class="sxs-lookup"><span data-stu-id="fa72d-108">Method</span></span>                                                          | <span data-ttu-id="fa72d-109">説明</span><span class="sxs-lookup"><span data-stu-id="fa72d-109">Description</span></span>                            |
|-----------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="fa72d-110">public str text()</span><span class="sxs-lookup"><span data-stu-id="fa72d-110">public str text()</span></span>                                               | <span data-ttu-id="fa72d-111">セグメントの現在のテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="fa72d-111">Gets the current text of the segment.</span></span>  |
| <span data-ttu-id="fa72d-112">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fa72d-112">public boolean allowEdit(\[boolean value\])</span></span>                     |                                        |
| <span data-ttu-id="fa72d-113">public str description(\[str description\])</span><span class="sxs-lookup"><span data-stu-id="fa72d-113">public str description(\[str description\])</span></span>                     |                                        |
| <span data-ttu-id="fa72d-114">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fa72d-114">public boolean enabled(\[boolean value\])</span></span>                       |                                        |
| <span data-ttu-id="fa72d-115">public int getIndex()</span><span class="sxs-lookup"><span data-stu-id="fa72d-115">public int getIndex()</span></span>                                           |                                        |
| <span data-ttu-id="fa72d-116">public str name()</span><span class="sxs-lookup"><span data-stu-id="fa72d-116">public str name()</span></span>                                               |                                        |
| <span data-ttu-id="fa72d-117">public SegmentedEntryState state(\[SegmentedEntryState state\])</span><span class="sxs-lookup"><span data-stu-id="fa72d-117">public SegmentedEntryState state(\[SegmentedEntryState state\])</span></span> |                                        |
| <span data-ttu-id="fa72d-118">public str value(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fa72d-118">public str value(\[str value\])</span></span>                                 | <span data-ttu-id="fa72d-119">セグメントの現在の値を取得します。</span><span class="sxs-lookup"><span data-stu-id="fa72d-119">Gets the current value of the segment.</span></span> |

## <a name="method-text"></a><span data-ttu-id="fa72d-120">メソッド text</span><span class="sxs-lookup"><span data-stu-id="fa72d-120">Method text</span></span>

<span data-ttu-id="fa72d-121">セグメントの現在のテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="fa72d-121">Gets the current text of the segment.</span></span>

```xpp
public str text()
```

### <a name="return-value---text"></a><span data-ttu-id="fa72d-122">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="fa72d-122">Return Value - text</span></span>

<span data-ttu-id="fa72d-123">セグメントの現在のテキスト。</span><span class="sxs-lookup"><span data-stu-id="fa72d-123">The current text of the segment.</span></span>

### <a name="remarks---text"></a><span data-ttu-id="fa72d-124">備考 - text</span><span class="sxs-lookup"><span data-stu-id="fa72d-124">Remarks - text</span></span>

<span data-ttu-id="fa72d-125">このメソッドは、変更中であっても、セグメントのテキストの持続値を常に返します。</span><span class="sxs-lookup"><span data-stu-id="fa72d-125">This method always returns the current text of the segment, even while it is being modified.</span></span> <span data-ttu-id="fa72d-126">セグメントの保存された最後の値を取得するには、value メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="fa72d-126">To retrieve the last value that was persisted for the segment, use the value method.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="fa72d-127">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="fa72d-127">Method allowEdit</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="fa72d-128">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="fa72d-128">Parameters - allowEdit</span></span>

<span data-ttu-id="fa72d-129">値</span><span class="sxs-lookup"><span data-stu-id="fa72d-129">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="fa72d-130">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="fa72d-130">Return Value - allowEdit</span></span>

## <a name="method-description"></a><span data-ttu-id="fa72d-131">メソッドの説明</span><span class="sxs-lookup"><span data-stu-id="fa72d-131">Method description</span></span>

```xpp
public str description([str description])
```

### <a name="parameters---description"></a><span data-ttu-id="fa72d-132">パラメーター - description</span><span class="sxs-lookup"><span data-stu-id="fa72d-132">Parameters - description</span></span>

<span data-ttu-id="fa72d-133">説明</span><span class="sxs-lookup"><span data-stu-id="fa72d-133">description</span></span>  

### <a name="return-value---description"></a><span data-ttu-id="fa72d-134">戻り値 - description</span><span class="sxs-lookup"><span data-stu-id="fa72d-134">Return Value - description</span></span>

## <a name="method-enabled"></a><span data-ttu-id="fa72d-135">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="fa72d-135">Method enabled</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="fa72d-136">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="fa72d-136">Parameters - enabled</span></span>

<span data-ttu-id="fa72d-137">値</span><span class="sxs-lookup"><span data-stu-id="fa72d-137">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="fa72d-138">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="fa72d-138">Return Value - enabled</span></span>

## <a name="method-getindex"></a><span data-ttu-id="fa72d-139">メソッド getIndex</span><span class="sxs-lookup"><span data-stu-id="fa72d-139">Method getIndex</span></span>

```xpp
public int getIndex()
```

### <a name="return-value---getindex"></a><span data-ttu-id="fa72d-140">戻り値 - getIndex</span><span class="sxs-lookup"><span data-stu-id="fa72d-140">Return Value - getIndex</span></span>

## <a name="method-name"></a><span data-ttu-id="fa72d-141">メソッド名</span><span class="sxs-lookup"><span data-stu-id="fa72d-141">Method name</span></span>

```xpp
public str name()
```

### <a name="return-value---name"></a><span data-ttu-id="fa72d-142">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="fa72d-142">Return Value - name</span></span>

## <a name="method-state"></a><span data-ttu-id="fa72d-143">メソッド state</span><span class="sxs-lookup"><span data-stu-id="fa72d-143">Method state</span></span>

```xpp
public SegmentedEntryState state([SegmentedEntryState state])
```

### <a name="parameters---state"></a><span data-ttu-id="fa72d-144">パラメーター - state</span><span class="sxs-lookup"><span data-stu-id="fa72d-144">Parameters - state</span></span>

<span data-ttu-id="fa72d-145">状態</span><span class="sxs-lookup"><span data-stu-id="fa72d-145">state</span></span>  

### <a name="return-value---state"></a><span data-ttu-id="fa72d-146">戻り値 - state</span><span class="sxs-lookup"><span data-stu-id="fa72d-146">Return Value - state</span></span>

## <a name="method-value"></a><span data-ttu-id="fa72d-147">メソッド value</span><span class="sxs-lookup"><span data-stu-id="fa72d-147">Method value</span></span>

<span data-ttu-id="fa72d-148">セグメントの現在の値を取得します。</span><span class="sxs-lookup"><span data-stu-id="fa72d-148">Gets the current value of the segment.</span></span>

```xpp
public str value([str value])
```

### <a name="parameters---value"></a><span data-ttu-id="fa72d-149">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="fa72d-149">Parameters - value</span></span>

<span data-ttu-id="fa72d-150">値</span><span class="sxs-lookup"><span data-stu-id="fa72d-150">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="fa72d-151">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="fa72d-151">Return Value - value</span></span>

<span data-ttu-id="fa72d-152">セグメントの現在の値。</span><span class="sxs-lookup"><span data-stu-id="fa72d-152">The current value of the segment.</span></span>

### <a name="remarks---value"></a><span data-ttu-id="fa72d-153">備考 - value</span><span class="sxs-lookup"><span data-stu-id="fa72d-153">Remarks - value</span></span>

<span data-ttu-id="fa72d-154">このメソッドは、変更中であっても、セグメントの現在の持続値を常に返します。</span><span class="sxs-lookup"><span data-stu-id="fa72d-154">This method always returns the current persisted value of the segment, even while it is being modified.</span></span> <span data-ttu-id="fa72d-155">コントロールの現在のテキストを取得するには、text メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="fa72d-155">To retrieve the current text of the control while it is being modified, use the text method.</span></span>

