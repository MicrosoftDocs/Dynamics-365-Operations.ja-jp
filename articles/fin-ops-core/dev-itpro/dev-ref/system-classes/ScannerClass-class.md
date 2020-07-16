---
title: ScannerClass クラス
description: このトピックでは、ScannerClass クラスについて説明します。
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
ms.openlocfilehash: 30cbff5dd2982379b2b385fecbc48022704c1324
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502817"
---
# <a name="class-scannerclass"></a><span data-ttu-id="0f56f-103">クラス ScannerClass</span><span class="sxs-lookup"><span data-stu-id="0f56f-103">Class ScannerClass</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class ScannerClass extends Object
```

## <a name="remarks"></a><span data-ttu-id="0f56f-104">備考</span><span class="sxs-lookup"><span data-stu-id="0f56f-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="0f56f-105">例</span><span class="sxs-lookup"><span data-stu-id="0f56f-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="0f56f-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="0f56f-106">Methods</span></span>

| <span data-ttu-id="0f56f-107">方法</span><span class="sxs-lookup"><span data-stu-id="0f56f-107">Method</span></span>                                                                                       | <span data-ttu-id="0f56f-108">説明</span><span class="sxs-lookup"><span data-stu-id="0f56f-108">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="0f56f-109">public int col()</span><span class="sxs-lookup"><span data-stu-id="0f56f-109">public int col()</span></span>                                                                             |                                                 |
| <span data-ttu-id="0f56f-110">public Date dateValue()</span><span class="sxs-lookup"><span data-stu-id="0f56f-110">public Date dateValue()</span></span>                                                                      |                                                 |
| <span data-ttu-id="0f56f-111">public int firstSymbol()</span><span class="sxs-lookup"><span data-stu-id="0f56f-111">public int firstSymbol()</span></span>                                                                     |                                                 |
| <span data-ttu-id="0f56f-112">public Int64 int64Value()</span><span class="sxs-lookup"><span data-stu-id="0f56f-112">public Int64 int64Value()</span></span>                                                                    |                                                 |
| <span data-ttu-id="0f56f-113">public int intValue()</span><span class="sxs-lookup"><span data-stu-id="0f56f-113">public int intValue()</span></span>                                                                        |                                                 |
| <span data-ttu-id="0f56f-114">public int line()</span><span class="sxs-lookup"><span data-stu-id="0f56f-114">public int line()</span></span>                                                                            |                                                 |
| <span data-ttu-id="0f56f-115">public int nextSymbol()</span><span class="sxs-lookup"><span data-stu-id="0f56f-115">public int nextSymbol()</span></span>                                                                      |                                                 |
| <span data-ttu-id="0f56f-116">public Real realValue()</span><span class="sxs-lookup"><span data-stu-id="0f56f-116">public Real realValue()</span></span>                                                                      |                                                 |
| <span data-ttu-id="0f56f-117">public int startColumn()</span><span class="sxs-lookup"><span data-stu-id="0f56f-117">public int startColumn()</span></span>                                                                     |                                                 |
| <span data-ttu-id="0f56f-118">public str string()</span><span class="sxs-lookup"><span data-stu-id="0f56f-118">public str string()</span></span>                                                                          |                                                 |
| <span data-ttu-id="0f56f-119">public str strValue()</span><span class="sxs-lookup"><span data-stu-id="0f56f-119">public str strValue()</span></span>                                                                        |                                                 |
| <span data-ttu-id="0f56f-120">public void localMacroDefine(str text, int startLine, int startPos, int endLine, int endPos)</span><span class="sxs-lookup"><span data-stu-id="0f56f-120">public void localMacroDefine(str text, int startLine, int startPos, int endLine, int endPos)</span></span> |                                                 |
| <span data-ttu-id="0f56f-121">public void lineComment(str text, int startLine, int startPos, int endLine, int endPos)</span><span class="sxs-lookup"><span data-stu-id="0f56f-121">public void lineComment(str text, int startLine, int startPos, int endLine, int endPos)</span></span>      |                                                 |
| <span data-ttu-id="0f56f-122">public void macroDefine(str text, int startLine, int startPos, int endLine, int endPos)</span><span class="sxs-lookup"><span data-stu-id="0f56f-122">public void macroDefine(str text, int startLine, int startPos, int endLine, int endPos)</span></span>      |                                                 |
| <span data-ttu-id="0f56f-123">public void new(str source)</span><span class="sxs-lookup"><span data-stu-id="0f56f-123">public void new(str source)</span></span>                                                                  | <span data-ttu-id="0f56f-124">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="0f56f-124">Initializes a new instance of the Object class.</span></span> |
| <span data-ttu-id="0f56f-125">public void comment(str text, int startLine, int startPos, int endLine, int endPos)</span><span class="sxs-lookup"><span data-stu-id="0f56f-125">public void comment(str text, int startLine, int startPos, int endLine, int endPos)</span></span>          |                                                 |

## <a name="method-col"></a><span data-ttu-id="0f56f-126">メソッド col</span><span class="sxs-lookup"><span data-stu-id="0f56f-126">Method col</span></span>

```xpp
public int col()
```

### <a name="return-value---col"></a><span data-ttu-id="0f56f-127">戻り値 - col</span><span class="sxs-lookup"><span data-stu-id="0f56f-127">Return Value - col</span></span>

## <a name="method-datevalue"></a><span data-ttu-id="0f56f-128">メソッド dateValue</span><span class="sxs-lookup"><span data-stu-id="0f56f-128">Method dateValue</span></span>

```xpp
public Date dateValue()
```

### <a name="return-value---datevalue"></a><span data-ttu-id="0f56f-129">戻り値 - dateValue</span><span class="sxs-lookup"><span data-stu-id="0f56f-129">Return Value - dateValue</span></span>

## <a name="method-firstsymbol"></a><span data-ttu-id="0f56f-130">メソッド firstSymbol</span><span class="sxs-lookup"><span data-stu-id="0f56f-130">Method firstSymbol</span></span>

```xpp
public int firstSymbol()
```

### <a name="return-value---firstsymbol"></a><span data-ttu-id="0f56f-131">戻り値 - firstSymbol</span><span class="sxs-lookup"><span data-stu-id="0f56f-131">Return Value - firstSymbol</span></span>

## <a name="method-int64value"></a><span data-ttu-id="0f56f-132">メソッド int64Value</span><span class="sxs-lookup"><span data-stu-id="0f56f-132">Method int64Value</span></span>

```xpp
public Int64 int64Value()
```

### <a name="return-value---int64value"></a><span data-ttu-id="0f56f-133">戻り値 - int64Value</span><span class="sxs-lookup"><span data-stu-id="0f56f-133">Return Value - int64Value</span></span>

## <a name="method-intvalue"></a><span data-ttu-id="0f56f-134">メソッド intValue</span><span class="sxs-lookup"><span data-stu-id="0f56f-134">Method intValue</span></span>

```xpp
public int intValue()
```

### <a name="return-value---intvalue"></a><span data-ttu-id="0f56f-135">戻り値 - intValue</span><span class="sxs-lookup"><span data-stu-id="0f56f-135">Return Value - intValue</span></span>

## <a name="method-line"></a><span data-ttu-id="0f56f-136">メソッド line</span><span class="sxs-lookup"><span data-stu-id="0f56f-136">Method line</span></span>

```xpp
public int line()
```

### <a name="return-value---line"></a><span data-ttu-id="0f56f-137">戻り値 - line</span><span class="sxs-lookup"><span data-stu-id="0f56f-137">Return Value - line</span></span>

## <a name="method-nextsymbol"></a><span data-ttu-id="0f56f-138">メソッド nextSymbol</span><span class="sxs-lookup"><span data-stu-id="0f56f-138">Method nextSymbol</span></span>

```xpp
public int nextSymbol()
```

### <a name="return-value---nextsymbol"></a><span data-ttu-id="0f56f-139">戻り値 - nextSymbol</span><span class="sxs-lookup"><span data-stu-id="0f56f-139">Return Value - nextSymbol</span></span>

## <a name="method-realvalue"></a><span data-ttu-id="0f56f-140">メソッド realValue</span><span class="sxs-lookup"><span data-stu-id="0f56f-140">Method realValue</span></span>

```xpp
public Real realValue()
```

### <a name="return-value---realvalue"></a><span data-ttu-id="0f56f-141">戻り値 - realValue</span><span class="sxs-lookup"><span data-stu-id="0f56f-141">Return Value - realValue</span></span>

## <a name="method-startcolumn"></a><span data-ttu-id="0f56f-142">メソッド startColumn</span><span class="sxs-lookup"><span data-stu-id="0f56f-142">Method startColumn</span></span>

```xpp
public int startColumn()
```

### <a name="return-value---startcolumn"></a><span data-ttu-id="0f56f-143">戻り値 - startColumn</span><span class="sxs-lookup"><span data-stu-id="0f56f-143">Return Value - startColumn</span></span>

## <a name="method-string"></a><span data-ttu-id="0f56f-144">メソッド string</span><span class="sxs-lookup"><span data-stu-id="0f56f-144">Method string</span></span>

```xpp
public str string()
```

### <a name="return-value---string"></a><span data-ttu-id="0f56f-145">戻り値 - string</span><span class="sxs-lookup"><span data-stu-id="0f56f-145">Return Value - string</span></span>

## <a name="method-strvalue"></a><span data-ttu-id="0f56f-146">メソッド strValue</span><span class="sxs-lookup"><span data-stu-id="0f56f-146">Method strValue</span></span>

```xpp
public str strValue()
```

### <a name="return-value---strvalue"></a><span data-ttu-id="0f56f-147">戻り値 - strValue</span><span class="sxs-lookup"><span data-stu-id="0f56f-147">Return Value - strValue</span></span>

## <a name="method-localmacrodefine"></a><span data-ttu-id="0f56f-148">メソッド localMacroDefine</span><span class="sxs-lookup"><span data-stu-id="0f56f-148">Method localMacroDefine</span></span>

```xpp
public void localMacroDefine(str text, int startLine, int startPos, int endLine, int endPos)
```

### <a name="parameters---localmacrodefine"></a><span data-ttu-id="0f56f-149">パラメーター - localMacroDefine</span><span class="sxs-lookup"><span data-stu-id="0f56f-149">Parameters - localMacroDefine</span></span>

<span data-ttu-id="0f56f-150">テキスト</span><span class="sxs-lookup"><span data-stu-id="0f56f-150">text</span></span>  

<!-- -->

<span data-ttu-id="0f56f-151">startLine</span><span class="sxs-lookup"><span data-stu-id="0f56f-151">startLine</span></span>  

<!-- -->

<span data-ttu-id="0f56f-152">startPos</span><span class="sxs-lookup"><span data-stu-id="0f56f-152">startPos</span></span>  

<!-- -->

<span data-ttu-id="0f56f-153">endLine</span><span class="sxs-lookup"><span data-stu-id="0f56f-153">endLine</span></span>  

<!-- -->

<span data-ttu-id="0f56f-154">endPos</span><span class="sxs-lookup"><span data-stu-id="0f56f-154">endPos</span></span>  

## <a name="method-linecomment"></a><span data-ttu-id="0f56f-155">メソッド lineComment</span><span class="sxs-lookup"><span data-stu-id="0f56f-155">Method lineComment</span></span>

```xpp
public void lineComment(str text, int startLine, int startPos, int endLine, int endPos)
```

### <a name="parameters---linecomment"></a><span data-ttu-id="0f56f-156">パラメーター - lineComment</span><span class="sxs-lookup"><span data-stu-id="0f56f-156">Parameters - lineComment</span></span>

<span data-ttu-id="0f56f-157">テキスト</span><span class="sxs-lookup"><span data-stu-id="0f56f-157">text</span></span>  

<!-- -->

<span data-ttu-id="0f56f-158">startLine</span><span class="sxs-lookup"><span data-stu-id="0f56f-158">startLine</span></span>  

<!-- -->

<span data-ttu-id="0f56f-159">startPos</span><span class="sxs-lookup"><span data-stu-id="0f56f-159">startPos</span></span>  

<!-- -->

<span data-ttu-id="0f56f-160">endLine</span><span class="sxs-lookup"><span data-stu-id="0f56f-160">endLine</span></span>  

<!-- -->

<span data-ttu-id="0f56f-161">endPos</span><span class="sxs-lookup"><span data-stu-id="0f56f-161">endPos</span></span>  

## <a name="method-macrodefine"></a><span data-ttu-id="0f56f-162">メソッド macroDefine</span><span class="sxs-lookup"><span data-stu-id="0f56f-162">Method macroDefine</span></span>

```xpp
public void macroDefine(str text, int startLine, int startPos, int endLine, int endPos)
```

### <a name="parameters---macrodefine"></a><span data-ttu-id="0f56f-163">パラメーター - macroDefine</span><span class="sxs-lookup"><span data-stu-id="0f56f-163">Parameters - macroDefine</span></span>

<span data-ttu-id="0f56f-164">テキスト</span><span class="sxs-lookup"><span data-stu-id="0f56f-164">text</span></span>  

<!-- -->

<span data-ttu-id="0f56f-165">startLine</span><span class="sxs-lookup"><span data-stu-id="0f56f-165">startLine</span></span>  

<!-- -->

<span data-ttu-id="0f56f-166">startPos</span><span class="sxs-lookup"><span data-stu-id="0f56f-166">startPos</span></span>  

<!-- -->

<span data-ttu-id="0f56f-167">endLine</span><span class="sxs-lookup"><span data-stu-id="0f56f-167">endLine</span></span>  

<!-- -->

<span data-ttu-id="0f56f-168">endPos</span><span class="sxs-lookup"><span data-stu-id="0f56f-168">endPos</span></span>  

## <a name="method-new"></a><span data-ttu-id="0f56f-169">メソッド new</span><span class="sxs-lookup"><span data-stu-id="0f56f-169">Method new</span></span>

<span data-ttu-id="0f56f-170">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="0f56f-170">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(str source)
```

### <a name="parameters---new"></a><span data-ttu-id="0f56f-171">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="0f56f-171">Parameters - new</span></span>

<span data-ttu-id="0f56f-172">ソース</span><span class="sxs-lookup"><span data-stu-id="0f56f-172">source</span></span>  

## <a name="method-comment"></a><span data-ttu-id="0f56f-173">メソッド comment</span><span class="sxs-lookup"><span data-stu-id="0f56f-173">Method comment</span></span>

```xpp
public void comment(str text, int startLine, int startPos, int endLine, int endPos)
```

### <a name="parameters---comment"></a><span data-ttu-id="0f56f-174">パラメーター - comment</span><span class="sxs-lookup"><span data-stu-id="0f56f-174">Parameters - comment</span></span>

<span data-ttu-id="0f56f-175">テキスト</span><span class="sxs-lookup"><span data-stu-id="0f56f-175">text</span></span>  

<!-- -->

<span data-ttu-id="0f56f-176">startLine</span><span class="sxs-lookup"><span data-stu-id="0f56f-176">startLine</span></span>  

<!-- -->

<span data-ttu-id="0f56f-177">startPos</span><span class="sxs-lookup"><span data-stu-id="0f56f-177">startPos</span></span>  

<!-- -->

<span data-ttu-id="0f56f-178">endLine</span><span class="sxs-lookup"><span data-stu-id="0f56f-178">endLine</span></span>  

<!-- -->

<span data-ttu-id="0f56f-179">endPos</span><span class="sxs-lookup"><span data-stu-id="0f56f-179">endPos</span></span>  

