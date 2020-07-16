---
title: WinAPINative クラス
description: このトピックでは、WinAPINative クラスについて説明します。
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
ms.openlocfilehash: b1866cc870e8f5913412b0f8ee2bf79478a05353
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502683"
---
# <a name="class-winapinative"></a><span data-ttu-id="e0c0e-103">クラス WinAPINative</span><span class="sxs-lookup"><span data-stu-id="e0c0e-103">Class WinAPINative</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class WinAPINative extends Object
```

## <a name="remarks"></a><span data-ttu-id="e0c0e-104">備考</span><span class="sxs-lookup"><span data-stu-id="e0c0e-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="e0c0e-105">例</span><span class="sxs-lookup"><span data-stu-id="e0c0e-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="e0c0e-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="e0c0e-106">Methods</span></span>

| <span data-ttu-id="e0c0e-107">方法</span><span class="sxs-lookup"><span data-stu-id="e0c0e-107">Method</span></span>                                                                                                                  | <span data-ttu-id="e0c0e-108">説明</span><span class="sxs-lookup"><span data-stu-id="e0c0e-108">Description</span></span>                                           |
|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="e0c0e-109">::public static Int64 createFontIndirect(Binary logfont)</span><span class="sxs-lookup"><span data-stu-id="e0c0e-109">::public static Int64 createFontIndirect(Binary logfont)</span></span>                                                                |                                                       |
| <span data-ttu-id="e0c0e-110">::public static boolean deleteObject(Int64 hGDIObject)</span><span class="sxs-lookup"><span data-stu-id="e0c0e-110">::public static boolean deleteObject(Int64 hGDIObject)</span></span>                                                                  |                                                       |
| <span data-ttu-id="e0c0e-111">::public static boolean getCharABCWidthsI(Int64 hDC, Int64 firstGlyphIndex, Int64 glyphIndicesCount, Binary charWidths)</span><span class="sxs-lookup"><span data-stu-id="e0c0e-111">::public static boolean getCharABCWidthsI(Int64 hDC, Int64 firstGlyphIndex, Int64 glyphIndicesCount, Binary charWidths)</span></span> |                                                       |
| <span data-ttu-id="e0c0e-112">::public static int getDeviceCaps(Int64 hDC, int index)</span><span class="sxs-lookup"><span data-stu-id="e0c0e-112">::public static int getDeviceCaps(Int64 hDC, int index)</span></span>                                                                 |                                                       |
| <span data-ttu-id="e0c0e-113">::public static int getFontData(Int64 hDC, int dwTable, int dwOffset, \[Binary pvBuffer\])</span><span class="sxs-lookup"><span data-stu-id="e0c0e-113">::public static int getFontData(Int64 hDC, int dwTable, int dwOffset, \[Binary pvBuffer\])</span></span>                              |                                                       |
| <span data-ttu-id="e0c0e-114">::public static int getFontUnicodeRanges(Int64 hDC, \[Binary lpgs\])</span><span class="sxs-lookup"><span data-stu-id="e0c0e-114">::public static int getFontUnicodeRanges(Int64 hDC, \[Binary lpgs\])</span></span>                                                    |                                                       |
| <span data-ttu-id="e0c0e-115">::public static int getGlyphIndices(Int64 hDC, str lpstr, Binary pgi, int fl)</span><span class="sxs-lookup"><span data-stu-id="e0c0e-115">::public static int getGlyphIndices(Int64 hDC, str lpstr, Binary pgi, int fl)</span></span>                                           |                                                       |
| <span data-ttu-id="e0c0e-116">::public static Int64 getTextMetrics(Int64 hDC, Binary lpMetrics)</span><span class="sxs-lookup"><span data-stu-id="e0c0e-116">::public static Int64 getTextMetrics(Int64 hDC, Binary lpMetrics)</span></span>                                                       |                                                       |
| <span data-ttu-id="e0c0e-117">::public static int getUniscribeGlyphIndices(Int64 hDC, Int64 hGDIObject, str lpstr, Binary pgi)</span><span class="sxs-lookup"><span data-stu-id="e0c0e-117">::public static int getUniscribeGlyphIndices(Int64 hDC, Int64 hGDIObject, str lpstr, Binary pgi)</span></span>                        |                                                       |
| <span data-ttu-id="e0c0e-118">::public static Int64 selectObject(Int64 hDC, Int64 hGDIObject)</span><span class="sxs-lookup"><span data-stu-id="e0c0e-118">::public static Int64 selectObject(Int64 hDC, Int64 hGDIObject)</span></span>                                                         |                                                       |
| <span data-ttu-id="e0c0e-119">private void new()</span><span class="sxs-lookup"><span data-stu-id="e0c0e-119">private void new()</span></span>                                                                                                      | <span data-ttu-id="e0c0e-120">WinAPINative クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e0c0e-120">Initializes a new instance of the WinAPINative class.</span></span> |

## <a name="method-createfontindirect"></a><span data-ttu-id="e0c0e-121">メソッド createFontIndirect</span><span class="sxs-lookup"><span data-stu-id="e0c0e-121">Method createFontIndirect</span></span>

```xpp
public static Int64 createFontIndirect(Binary logfont)
```

### <a name="parameters---createfontindirect"></a><span data-ttu-id="e0c0e-122">パラメーター - createFontIndirect</span><span class="sxs-lookup"><span data-stu-id="e0c0e-122">Parameters - createFontIndirect</span></span>

<span data-ttu-id="e0c0e-123">logfont</span><span class="sxs-lookup"><span data-stu-id="e0c0e-123">logfont</span></span>  

### <a name="return-value---createfontindirect"></a><span data-ttu-id="e0c0e-124">戻り値 - createFontIndirect</span><span class="sxs-lookup"><span data-stu-id="e0c0e-124">Return Value - createFontIndirect</span></span>

## <a name="method-deleteobject"></a><span data-ttu-id="e0c0e-125">メソッド deleteObject</span><span class="sxs-lookup"><span data-stu-id="e0c0e-125">Method deleteObject</span></span>

```xpp
public static boolean deleteObject(Int64 hGDIObject)
```

### <a name="parameters---deleteobject"></a><span data-ttu-id="e0c0e-126">パラメーター - deleteObject</span><span class="sxs-lookup"><span data-stu-id="e0c0e-126">Parameters - deleteObject</span></span>

<span data-ttu-id="e0c0e-127">hGDIObject</span><span class="sxs-lookup"><span data-stu-id="e0c0e-127">hGDIObject</span></span>  

### <a name="return-value---deleteobject"></a><span data-ttu-id="e0c0e-128">戻り値 - deleteObject</span><span class="sxs-lookup"><span data-stu-id="e0c0e-128">Return Value - deleteObject</span></span>

## <a name="method-getcharabcwidthsi"></a><span data-ttu-id="e0c0e-129">メソッド getCharABCWidthsI</span><span class="sxs-lookup"><span data-stu-id="e0c0e-129">Method getCharABCWidthsI</span></span>

```xpp
public static boolean getCharABCWidthsI(Int64 hDC, Int64 firstGlyphIndex, Int64 glyphIndicesCount, Binary charWidths)
```

### <a name="parameters---getcharabcwidthsi"></a><span data-ttu-id="e0c0e-130">パラメーター - getCharABCWidthsI</span><span class="sxs-lookup"><span data-stu-id="e0c0e-130">Parameters - getCharABCWidthsI</span></span>

<span data-ttu-id="e0c0e-131">hDC</span><span class="sxs-lookup"><span data-stu-id="e0c0e-131">hDC</span></span>  

<!-- -->

<span data-ttu-id="e0c0e-132">firstGlyphIndex</span><span class="sxs-lookup"><span data-stu-id="e0c0e-132">firstGlyphIndex</span></span>  

<!-- -->

<span data-ttu-id="e0c0e-133">glyphIndicesCount</span><span class="sxs-lookup"><span data-stu-id="e0c0e-133">glyphIndicesCount</span></span>  

<!-- -->

<span data-ttu-id="e0c0e-134">charWidths</span><span class="sxs-lookup"><span data-stu-id="e0c0e-134">charWidths</span></span>  

### <a name="return-value---getcharabcwidthsi"></a><span data-ttu-id="e0c0e-135">戻り値 - getCharABCWidthsI</span><span class="sxs-lookup"><span data-stu-id="e0c0e-135">Return Value - getCharABCWidthsI</span></span>

## <a name="method-getdevicecaps"></a><span data-ttu-id="e0c0e-136">メソッド getDeviceCaps</span><span class="sxs-lookup"><span data-stu-id="e0c0e-136">Method getDeviceCaps</span></span>

```xpp
public static int getDeviceCaps(Int64 hDC, int index)
```

### <a name="parameters---getdevicecaps"></a><span data-ttu-id="e0c0e-137">パラメーター - getDeviceCaps</span><span class="sxs-lookup"><span data-stu-id="e0c0e-137">Parameters - getDeviceCaps</span></span>

<span data-ttu-id="e0c0e-138">hDC</span><span class="sxs-lookup"><span data-stu-id="e0c0e-138">hDC</span></span>  

<!-- -->

<span data-ttu-id="e0c0e-139">指数</span><span class="sxs-lookup"><span data-stu-id="e0c0e-139">index</span></span>  

### <a name="return-value---getdevicecaps"></a><span data-ttu-id="e0c0e-140">戻り値 - getDeviceCaps</span><span class="sxs-lookup"><span data-stu-id="e0c0e-140">Return Value - getDeviceCaps</span></span>

## <a name="method-getfontdata"></a><span data-ttu-id="e0c0e-141">メソッド getFontData</span><span class="sxs-lookup"><span data-stu-id="e0c0e-141">Method getFontData</span></span>

```xpp
public static int getFontData(Int64 hDC, int dwTable, int dwOffset, [Binary pvBuffer])
```

### <a name="parameters---getfontdata"></a><span data-ttu-id="e0c0e-142">パラメーター - getFontData</span><span class="sxs-lookup"><span data-stu-id="e0c0e-142">Parameters - getFontData</span></span>

<span data-ttu-id="e0c0e-143">hDC</span><span class="sxs-lookup"><span data-stu-id="e0c0e-143">hDC</span></span>  

<!-- -->

<span data-ttu-id="e0c0e-144">dwTable</span><span class="sxs-lookup"><span data-stu-id="e0c0e-144">dwTable</span></span>  

<!-- -->

<span data-ttu-id="e0c0e-145">dwOffset</span><span class="sxs-lookup"><span data-stu-id="e0c0e-145">dwOffset</span></span>  

<!-- -->

<span data-ttu-id="e0c0e-146">pvBuffer</span><span class="sxs-lookup"><span data-stu-id="e0c0e-146">pvBuffer</span></span>  

### <a name="return-value---getfontdata"></a><span data-ttu-id="e0c0e-147">戻り値 - getFontData</span><span class="sxs-lookup"><span data-stu-id="e0c0e-147">Return Value - getFontData</span></span>

## <a name="method-getfontunicoderanges"></a><span data-ttu-id="e0c0e-148">メソッド getFontUnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="e0c0e-148">Method getFontUnicodeRanges</span></span>

```xpp
public static int getFontUnicodeRanges(Int64 hDC, [Binary lpgs])
```

### <a name="parameters---getfontunicoderanges"></a><span data-ttu-id="e0c0e-149">パラメーター - getFontUnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="e0c0e-149">Parameters - getFontUnicodeRanges</span></span>

<span data-ttu-id="e0c0e-150">hDC</span><span class="sxs-lookup"><span data-stu-id="e0c0e-150">hDC</span></span>  

<!-- -->

<span data-ttu-id="e0c0e-151">lpgs</span><span class="sxs-lookup"><span data-stu-id="e0c0e-151">lpgs</span></span>  

### <a name="return-value---getfontunicoderanges"></a><span data-ttu-id="e0c0e-152">戻り値 - getFontUnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="e0c0e-152">Return Value - getFontUnicodeRanges</span></span>

## <a name="method-getglyphindices"></a><span data-ttu-id="e0c0e-153">メソッド getGlyphIndices</span><span class="sxs-lookup"><span data-stu-id="e0c0e-153">Method getGlyphIndices</span></span>

```xpp
public static int getGlyphIndices(Int64 hDC, str lpstr, Binary pgi, int fl)
```

### <a name="parameters---getglyphindices"></a><span data-ttu-id="e0c0e-154">パラメーター - getGlyphIndices</span><span class="sxs-lookup"><span data-stu-id="e0c0e-154">Parameters - getGlyphIndices</span></span>

<span data-ttu-id="e0c0e-155">hDC</span><span class="sxs-lookup"><span data-stu-id="e0c0e-155">hDC</span></span>  

<!-- -->

<span data-ttu-id="e0c0e-156">lpstr</span><span class="sxs-lookup"><span data-stu-id="e0c0e-156">lpstr</span></span>  

<!-- -->

<span data-ttu-id="e0c0e-157">pgi</span><span class="sxs-lookup"><span data-stu-id="e0c0e-157">pgi</span></span>  

<!-- -->

<span data-ttu-id="e0c0e-158">fl</span><span class="sxs-lookup"><span data-stu-id="e0c0e-158">fl</span></span>  

### <a name="return-value---getglyphindices"></a><span data-ttu-id="e0c0e-159">戻り値 - getGlyphIndices</span><span class="sxs-lookup"><span data-stu-id="e0c0e-159">Return Value - getGlyphIndices</span></span>

## <a name="method-gettextmetrics"></a><span data-ttu-id="e0c0e-160">メソッド getTextMetrics</span><span class="sxs-lookup"><span data-stu-id="e0c0e-160">Method getTextMetrics</span></span>

```xpp
public static Int64 getTextMetrics(Int64 hDC, Binary lpMetrics)
```

### <a name="parameters---gettextmetrics"></a><span data-ttu-id="e0c0e-161">パラメーター - getTextMetrics</span><span class="sxs-lookup"><span data-stu-id="e0c0e-161">Parameters - getTextMetrics</span></span>

<span data-ttu-id="e0c0e-162">hDC</span><span class="sxs-lookup"><span data-stu-id="e0c0e-162">hDC</span></span>  

<!-- -->

<span data-ttu-id="e0c0e-163">lpMetrics</span><span class="sxs-lookup"><span data-stu-id="e0c0e-163">lpMetrics</span></span>  

### <a name="return-value---gettextmetrics"></a><span data-ttu-id="e0c0e-164">戻り値 - getTextMetrics</span><span class="sxs-lookup"><span data-stu-id="e0c0e-164">Return Value - getTextMetrics</span></span>

## <a name="method-getuniscribeglyphindices"></a><span data-ttu-id="e0c0e-165">メソッド getUniscribeGlyphIndices</span><span class="sxs-lookup"><span data-stu-id="e0c0e-165">Method getUniscribeGlyphIndices</span></span>

```xpp
public static int getUniscribeGlyphIndices(Int64 hDC, Int64 hGDIObject, str lpstr, Binary pgi)
```

### <a name="parameters---getuniscribeglyphindices"></a><span data-ttu-id="e0c0e-166">パラメーター - getUniscribeGlyphIndices</span><span class="sxs-lookup"><span data-stu-id="e0c0e-166">Parameters - getUniscribeGlyphIndices</span></span>

<span data-ttu-id="e0c0e-167">hDC</span><span class="sxs-lookup"><span data-stu-id="e0c0e-167">hDC</span></span>  

<!-- -->

<span data-ttu-id="e0c0e-168">hGDIObject</span><span class="sxs-lookup"><span data-stu-id="e0c0e-168">hGDIObject</span></span>  

<!-- -->

<span data-ttu-id="e0c0e-169">lpstr</span><span class="sxs-lookup"><span data-stu-id="e0c0e-169">lpstr</span></span>  

<!-- -->

<span data-ttu-id="e0c0e-170">pgi</span><span class="sxs-lookup"><span data-stu-id="e0c0e-170">pgi</span></span>  

### <a name="return-value---getuniscribeglyphindices"></a><span data-ttu-id="e0c0e-171">戻り値 - getUniscribeGlyphIndices</span><span class="sxs-lookup"><span data-stu-id="e0c0e-171">Return Value - getUniscribeGlyphIndices</span></span>

## <a name="method-selectobject"></a><span data-ttu-id="e0c0e-172">メソッド selectObject</span><span class="sxs-lookup"><span data-stu-id="e0c0e-172">Method selectObject</span></span>

```xpp
public static Int64 selectObject(Int64 hDC, Int64 hGDIObject)
```

### <a name="parameters---selectobject"></a><span data-ttu-id="e0c0e-173">パラメーター - selectObject</span><span class="sxs-lookup"><span data-stu-id="e0c0e-173">Parameters - selectObject</span></span>

<span data-ttu-id="e0c0e-174">hDC</span><span class="sxs-lookup"><span data-stu-id="e0c0e-174">hDC</span></span>  

<!-- -->

<span data-ttu-id="e0c0e-175">hGDIObject</span><span class="sxs-lookup"><span data-stu-id="e0c0e-175">hGDIObject</span></span>  

### <a name="return-value---selectobject"></a><span data-ttu-id="e0c0e-176">戻り値 - selectObject</span><span class="sxs-lookup"><span data-stu-id="e0c0e-176">Return Value - selectObject</span></span>

## <a name="method-new"></a><span data-ttu-id="e0c0e-177">メソッド new</span><span class="sxs-lookup"><span data-stu-id="e0c0e-177">Method new</span></span>

<span data-ttu-id="e0c0e-178">WinAPINative クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e0c0e-178">Initializes a new instance of the WinAPINative class.</span></span>

```xpp
private void new()
```


