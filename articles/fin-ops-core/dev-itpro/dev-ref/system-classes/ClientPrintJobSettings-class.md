---
title: ClientPrintJobSettings クラス
description: このトピックでは、ClientPrintJobSettings クラスについて説明します。
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
ms.openlocfilehash: 362be465f969b9d6e608e024cec8147293e4056b
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502711"
---
# <a name="class-clientprintjobsettings"></a><span data-ttu-id="5eab4-103">クラス ClientPrintJobSettings</span><span class="sxs-lookup"><span data-stu-id="5eab4-103">Class ClientPrintJobSettings</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ClientPrintJobSettings extends PrintJobSettings
```

## <a name="remarks"></a><span data-ttu-id="5eab4-104">備考</span><span class="sxs-lookup"><span data-stu-id="5eab4-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="5eab4-105">例</span><span class="sxs-lookup"><span data-stu-id="5eab4-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="5eab4-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="5eab4-106">Methods</span></span>

| <span data-ttu-id="5eab4-107">方法</span><span class="sxs-lookup"><span data-stu-id="5eab4-107">Method</span></span>                                                                                                                  | <span data-ttu-id="5eab4-108">説明</span><span class="sxs-lookup"><span data-stu-id="5eab4-108">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="5eab4-109">public container getFontDimension(container container)</span><span class="sxs-lookup"><span data-stu-id="5eab4-109">public container getFontDimension(container container)</span></span>                                                                  |                                                 |
| <span data-ttu-id="5eab4-110">public container getInfoStrings()</span><span class="sxs-lookup"><span data-stu-id="5eab4-110">public container getInfoStrings()</span></span>                                                                                       |                                                 |
| <span data-ttu-id="5eab4-111">public int getNextLineOffset(container container)</span><span class="sxs-lookup"><span data-stu-id="5eab4-111">public int getNextLineOffset(container container)</span></span>                                                                       |                                                 |
| <span data-ttu-id="5eab4-112">public container getPageInfo()</span><span class="sxs-lookup"><span data-stu-id="5eab4-112">public container getPageInfo()</span></span>                                                                                          |                                                 |
| <span data-ttu-id="5eab4-113">public container getPrinterNames()</span><span class="sxs-lookup"><span data-stu-id="5eab4-113">public container getPrinterNames()</span></span>                                                                                      |                                                 |
| <span data-ttu-id="5eab4-114">public int getTextWidth(str text, str fontName, int charSet, int fontHeight, int style, int weight)</span><span class="sxs-lookup"><span data-stu-id="5eab4-114">public int getTextWidth(str text, str fontName, int charSet, int fontHeight, int style, int weight)</span></span>                     |                                                 |
| <span data-ttu-id="5eab4-115">public container getTextWidthExt(container container)</span><span class="sxs-lookup"><span data-stu-id="5eab4-115">public container getTextWidthExt(container container)</span></span>                                                                   |                                                 |
| <span data-ttu-id="5eab4-116">public container getWordWrapInfo(str text, int width, str fontName, int charSet, int fontHeight, int style, int weight)</span><span class="sxs-lookup"><span data-stu-id="5eab4-116">public container getWordWrapInfo(str text, int width, str fontName, int charSet, int fontHeight, int style, int weight)</span></span> |                                                 |
| <span data-ttu-id="5eab4-117">public container getWordWrapInfoExt(container container)</span><span class="sxs-lookup"><span data-stu-id="5eab4-117">public container getWordWrapInfoExt(container container)</span></span>                                                                |                                                 |
| <span data-ttu-id="5eab4-118">public container printerSettingsExt(str formName, \[xArgs args\], \[ReportRun reportRun\], \[int showWhat\])</span><span class="sxs-lookup"><span data-stu-id="5eab4-118">public container printerSettingsExt(str formName, \[xArgs args\], \[ReportRun reportRun\], \[int showWhat\])</span></span>            |                                                 |
| <span data-ttu-id="5eab4-119">public container setOrientationGetPageInfo(PrinterOrientation orientation)</span><span class="sxs-lookup"><span data-stu-id="5eab4-119">public container setOrientationGetPageInfo(PrinterOrientation orientation)</span></span>                                              |                                                 |
| <span data-ttu-id="5eab4-120">public void new(\[container Settings\], \[boolean infoOnly\])</span><span class="sxs-lookup"><span data-stu-id="5eab4-120">public void new(\[container Settings\], \[boolean infoOnly\])</span></span>                                                           | <span data-ttu-id="5eab4-121">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="5eab4-121">Initializes a new instance of the Object class.</span></span> |

## <a name="method-getfontdimension"></a><span data-ttu-id="5eab4-122">メソッド getFontDimension</span><span class="sxs-lookup"><span data-stu-id="5eab4-122">Method getFontDimension</span></span>

```xpp
public container getFontDimension(container container)
```

### <a name="parameters---getfontdimension"></a><span data-ttu-id="5eab4-123">パラメーター - getFontDimension</span><span class="sxs-lookup"><span data-stu-id="5eab4-123">Parameters - getFontDimension</span></span>

<span data-ttu-id="5eab4-124">コンテナー</span><span class="sxs-lookup"><span data-stu-id="5eab4-124">container</span></span>  

### <a name="return-value---getfontdimension"></a><span data-ttu-id="5eab4-125">戻り値 - getFontDimension</span><span class="sxs-lookup"><span data-stu-id="5eab4-125">Return Value - getFontDimension</span></span>

## <a name="method-getinfostrings"></a><span data-ttu-id="5eab4-126">メソッド getInfoStrings</span><span class="sxs-lookup"><span data-stu-id="5eab4-126">Method getInfoStrings</span></span>

```xpp
public container getInfoStrings()
```

### <a name="return-value---getinfostrings"></a><span data-ttu-id="5eab4-127">戻り値 - getInfoStrings</span><span class="sxs-lookup"><span data-stu-id="5eab4-127">Return Value - getInfoStrings</span></span>

## <a name="method-getnextlineoffset"></a><span data-ttu-id="5eab4-128">メソッド getNextLineOffset</span><span class="sxs-lookup"><span data-stu-id="5eab4-128">Method getNextLineOffset</span></span>

```xpp
public int getNextLineOffset(container container)
```

### <a name="parameters---getnextlineoffset"></a><span data-ttu-id="5eab4-129">パラメーター - getNextLineOffset</span><span class="sxs-lookup"><span data-stu-id="5eab4-129">Parameters - getNextLineOffset</span></span>

<span data-ttu-id="5eab4-130">コンテナー</span><span class="sxs-lookup"><span data-stu-id="5eab4-130">container</span></span>  

### <a name="return-value---getnextlineoffset"></a><span data-ttu-id="5eab4-131">戻り値 - getNextLineOffset</span><span class="sxs-lookup"><span data-stu-id="5eab4-131">Return Value - getNextLineOffset</span></span>

## <a name="method-getpageinfo"></a><span data-ttu-id="5eab4-132">メソッド getPageInfo</span><span class="sxs-lookup"><span data-stu-id="5eab4-132">Method getPageInfo</span></span>

```xpp
public container getPageInfo()
```

### <a name="return-value---getpageinfo"></a><span data-ttu-id="5eab4-133">戻り値 - getPageInfo</span><span class="sxs-lookup"><span data-stu-id="5eab4-133">Return Value - getPageInfo</span></span>

## <a name="method-getprinternames"></a><span data-ttu-id="5eab4-134">メソッド getPrinterNames</span><span class="sxs-lookup"><span data-stu-id="5eab4-134">Method getPrinterNames</span></span>

```xpp
public container getPrinterNames()
```

### <a name="return-value---getprinternames"></a><span data-ttu-id="5eab4-135">戻り値 - getPrinterNames</span><span class="sxs-lookup"><span data-stu-id="5eab4-135">Return Value - getPrinterNames</span></span>

## <a name="method-gettextwidth"></a><span data-ttu-id="5eab4-136">メソッド getTextWidth</span><span class="sxs-lookup"><span data-stu-id="5eab4-136">Method getTextWidth</span></span>

```xpp
public int getTextWidth(str text, str fontName, int charSet, int fontHeight, int style, int weight)
```

### <a name="parameters---gettextwidth"></a><span data-ttu-id="5eab4-137">パラメーター - getTextWidth</span><span class="sxs-lookup"><span data-stu-id="5eab4-137">Parameters - getTextWidth</span></span>

<span data-ttu-id="5eab4-138">テキスト</span><span class="sxs-lookup"><span data-stu-id="5eab4-138">text</span></span>  

<!-- -->

<span data-ttu-id="5eab4-139">fontName</span><span class="sxs-lookup"><span data-stu-id="5eab4-139">fontName</span></span>  

<!-- -->

<span data-ttu-id="5eab4-140">charSet</span><span class="sxs-lookup"><span data-stu-id="5eab4-140">charSet</span></span>  

<!-- -->

<span data-ttu-id="5eab4-141">fontHeight</span><span class="sxs-lookup"><span data-stu-id="5eab4-141">fontHeight</span></span>  

<!-- -->

<span data-ttu-id="5eab4-142">スタイル</span><span class="sxs-lookup"><span data-stu-id="5eab4-142">style</span></span>  

<!-- -->

<span data-ttu-id="5eab4-143">重量</span><span class="sxs-lookup"><span data-stu-id="5eab4-143">weight</span></span>  

### <a name="return-value---gettextwidth"></a><span data-ttu-id="5eab4-144">戻り値 - getTextWidth</span><span class="sxs-lookup"><span data-stu-id="5eab4-144">Return Value - getTextWidth</span></span>

## <a name="method-gettextwidthext"></a><span data-ttu-id="5eab4-145">メソッド getTextWidthExt</span><span class="sxs-lookup"><span data-stu-id="5eab4-145">Method getTextWidthExt</span></span>

```xpp
public container getTextWidthExt(container container)
```

### <a name="parameters---gettextwidthext"></a><span data-ttu-id="5eab4-146">パラメーター - getTextWidthExt</span><span class="sxs-lookup"><span data-stu-id="5eab4-146">Parameters - getTextWidthExt</span></span>

<span data-ttu-id="5eab4-147">コンテナー</span><span class="sxs-lookup"><span data-stu-id="5eab4-147">container</span></span>  

### <a name="return-value---gettextwidthext"></a><span data-ttu-id="5eab4-148">戻り値 - getTextWidthExt</span><span class="sxs-lookup"><span data-stu-id="5eab4-148">Return Value - getTextWidthExt</span></span>

## <a name="method-getwordwrapinfo"></a><span data-ttu-id="5eab4-149">メソッド getWordWrapInfo</span><span class="sxs-lookup"><span data-stu-id="5eab4-149">Method getWordWrapInfo</span></span>

```xpp
public container getWordWrapInfo(str text, int width, str fontName, int charSet, int fontHeight, int style, int weight)
```

### <a name="parameters---getwordwrapinfo"></a><span data-ttu-id="5eab4-150">パラメーター - getWordWrapInfo</span><span class="sxs-lookup"><span data-stu-id="5eab4-150">Parameters - getWordWrapInfo</span></span>

<span data-ttu-id="5eab4-151">テキスト</span><span class="sxs-lookup"><span data-stu-id="5eab4-151">text</span></span>  

<!-- -->

<span data-ttu-id="5eab4-152">width</span><span class="sxs-lookup"><span data-stu-id="5eab4-152">width</span></span>  

<!-- -->

<span data-ttu-id="5eab4-153">fontName</span><span class="sxs-lookup"><span data-stu-id="5eab4-153">fontName</span></span>  

<!-- -->

<span data-ttu-id="5eab4-154">charSet</span><span class="sxs-lookup"><span data-stu-id="5eab4-154">charSet</span></span>  

<!-- -->

<span data-ttu-id="5eab4-155">fontHeight</span><span class="sxs-lookup"><span data-stu-id="5eab4-155">fontHeight</span></span>  

<!-- -->

<span data-ttu-id="5eab4-156">スタイル</span><span class="sxs-lookup"><span data-stu-id="5eab4-156">style</span></span>  

<!-- -->

<span data-ttu-id="5eab4-157">重量</span><span class="sxs-lookup"><span data-stu-id="5eab4-157">weight</span></span>  

### <a name="return-value---getwordwrapinfo"></a><span data-ttu-id="5eab4-158">戻り値 - getWordWrapInfo</span><span class="sxs-lookup"><span data-stu-id="5eab4-158">Return Value - getWordWrapInfo</span></span>

## <a name="method-getwordwrapinfoext"></a><span data-ttu-id="5eab4-159">メソッド getWordWrapInfoExt</span><span class="sxs-lookup"><span data-stu-id="5eab4-159">Method getWordWrapInfoExt</span></span>

```xpp
public container getWordWrapInfoExt(container container)
```

### <a name="parameters---getwordwrapinfoext"></a><span data-ttu-id="5eab4-160">パラメーター - getWordWrapInfoExt</span><span class="sxs-lookup"><span data-stu-id="5eab4-160">Parameters - getWordWrapInfoExt</span></span>

<span data-ttu-id="5eab4-161">コンテナー</span><span class="sxs-lookup"><span data-stu-id="5eab4-161">container</span></span>  

### <a name="return-value---getwordwrapinfoext"></a><span data-ttu-id="5eab4-162">戻り値 - getWordWrapInfoExt</span><span class="sxs-lookup"><span data-stu-id="5eab4-162">Return Value - getWordWrapInfoExt</span></span>

## <a name="method-printersettingsext"></a><span data-ttu-id="5eab4-163">メソッド printerSettingsExt</span><span class="sxs-lookup"><span data-stu-id="5eab4-163">Method printerSettingsExt</span></span>

```xpp
public container printerSettingsExt(str formName, [xArgs args], [ReportRun reportRun], [int showWhat])
```

### <a name="parameters---printersettingsext"></a><span data-ttu-id="5eab4-164">パラメーター - printerSettingsExt</span><span class="sxs-lookup"><span data-stu-id="5eab4-164">Parameters - printerSettingsExt</span></span>

<span data-ttu-id="5eab4-165">formName</span><span class="sxs-lookup"><span data-stu-id="5eab4-165">formName</span></span>  

<!-- -->

<span data-ttu-id="5eab4-166">args</span><span class="sxs-lookup"><span data-stu-id="5eab4-166">args</span></span>  

<!-- -->

<span data-ttu-id="5eab4-167">reportRun</span><span class="sxs-lookup"><span data-stu-id="5eab4-167">reportRun</span></span>  

<!-- -->

<span data-ttu-id="5eab4-168">showWhat</span><span class="sxs-lookup"><span data-stu-id="5eab4-168">showWhat</span></span>  

### <a name="return-value---printersettingsext"></a><span data-ttu-id="5eab4-169">戻り値 - printerSettingsExt</span><span class="sxs-lookup"><span data-stu-id="5eab4-169">Return Value - printerSettingsExt</span></span>

## <a name="method-setorientationgetpageinfo"></a><span data-ttu-id="5eab4-170">メソッド setOrientationGetPageInfo</span><span class="sxs-lookup"><span data-stu-id="5eab4-170">Method setOrientationGetPageInfo</span></span>

```xpp
public container setOrientationGetPageInfo(PrinterOrientation orientation)
```

### <a name="parameters---setorientationgetpageinfo"></a><span data-ttu-id="5eab4-171">パラメーター - setOrientationGetPageInfo</span><span class="sxs-lookup"><span data-stu-id="5eab4-171">Parameters - setOrientationGetPageInfo</span></span>

<span data-ttu-id="5eab4-172">orientation</span><span class="sxs-lookup"><span data-stu-id="5eab4-172">orientation</span></span>  

### <a name="return-value---setorientationgetpageinfo"></a><span data-ttu-id="5eab4-173">戻り値 - setOrientationGetPageInfo</span><span class="sxs-lookup"><span data-stu-id="5eab4-173">Return Value - setOrientationGetPageInfo</span></span>

## <a name="method-new"></a><span data-ttu-id="5eab4-174">メソッド new</span><span class="sxs-lookup"><span data-stu-id="5eab4-174">Method new</span></span>

<span data-ttu-id="5eab4-175">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="5eab4-175">Initializes a new instance of the Object class.</span></span>

```xpp
public void new([container Settings], [boolean infoOnly])
```

### <a name="parameters---new"></a><span data-ttu-id="5eab4-176">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="5eab4-176">Parameters - new</span></span>

<span data-ttu-id="5eab4-177">設定</span><span class="sxs-lookup"><span data-stu-id="5eab4-177">Settings</span></span>  

<!-- -->

<span data-ttu-id="5eab4-178">infoOnly</span><span class="sxs-lookup"><span data-stu-id="5eab4-178">infoOnly</span></span>  

