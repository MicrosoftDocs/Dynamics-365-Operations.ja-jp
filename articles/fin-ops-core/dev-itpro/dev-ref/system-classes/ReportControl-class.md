---
title: ReportControl クラス
description: このトピックでは、ReportControl クラスについて説明します。
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
ms.openlocfilehash: 1e3a72b41283df067be9d5913abf446f3770b62a
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502846"
---
# <a name="class-reportcontrol"></a><span data-ttu-id="f8801-103">クラス ReportControl</span><span class="sxs-lookup"><span data-stu-id="f8801-103">Class ReportControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ReportControl extends TreeNode
```

<span data-ttu-id="f8801-104">ReportControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f8801-104">The ReportControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8801-105">備考</span><span class="sxs-lookup"><span data-stu-id="f8801-105">Remarks</span></span>

<span data-ttu-id="f8801-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f8801-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="f8801-107">例</span><span class="sxs-lookup"><span data-stu-id="f8801-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="f8801-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="f8801-108">Methods</span></span>

| <span data-ttu-id="f8801-109">方法</span><span class="sxs-lookup"><span data-stu-id="f8801-109">Method</span></span>                                                     | <span data-ttu-id="f8801-110">説明</span><span class="sxs-lookup"><span data-stu-id="f8801-110">Description</span></span> |
|------------------------------------------------------------|-------------|
| <span data-ttu-id="f8801-111">public int bottomMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="f8801-111">public int bottomMarginAndFrame()</span></span>                          |             |
| <span data-ttu-id="f8801-112">public ReportFieldType controlType()</span><span class="sxs-lookup"><span data-stu-id="f8801-112">public ReportFieldType controlType()</span></span>                       |             |
| <span data-ttu-id="f8801-113">public int delete()</span><span class="sxs-lookup"><span data-stu-id="f8801-113">public int delete()</span></span>                                        |             |
| <span data-ttu-id="f8801-114">public str effectiveFont()</span><span class="sxs-lookup"><span data-stu-id="f8801-114">public str effectiveFont()</span></span>                                 |             |
| <span data-ttu-id="f8801-115">public str fontInfoPrinter()</span><span class="sxs-lookup"><span data-stu-id="f8801-115">public str fontInfoPrinter()</span></span>                               |             |
| <span data-ttu-id="f8801-116">public int fontInfoPrinterAscent()</span><span class="sxs-lookup"><span data-stu-id="f8801-116">public int fontInfoPrinterAscent()</span></span>                         |             |
| <span data-ttu-id="f8801-117">public int fontInfoPrinterDescent()</span><span class="sxs-lookup"><span data-stu-id="f8801-117">public int fontInfoPrinterDescent()</span></span>                        |             |
| <span data-ttu-id="f8801-118">public int fontInfoPrinterExtLead()</span><span class="sxs-lookup"><span data-stu-id="f8801-118">public int fontInfoPrinterExtLead()</span></span>                        |             |
| <span data-ttu-id="f8801-119">public int fontInfoPrinterHeight()</span><span class="sxs-lookup"><span data-stu-id="f8801-119">public int fontInfoPrinterHeight()</span></span>                         |             |
| <span data-ttu-id="f8801-120">public int fontInfoPrinterIntLead()</span><span class="sxs-lookup"><span data-stu-id="f8801-120">public int fontInfoPrinterIntLead()</span></span>                        |             |
| <span data-ttu-id="f8801-121">public str fontInfoScreen()</span><span class="sxs-lookup"><span data-stu-id="f8801-121">public str fontInfoScreen()</span></span>                                |             |
| <span data-ttu-id="f8801-122">public int fontInfoScreenAscent()</span><span class="sxs-lookup"><span data-stu-id="f8801-122">public int fontInfoScreenAscent()</span></span>                          |             |
| <span data-ttu-id="f8801-123">public int fontInfoScreenDescent()</span><span class="sxs-lookup"><span data-stu-id="f8801-123">public int fontInfoScreenDescent()</span></span>                         |             |
| <span data-ttu-id="f8801-124">public int fontInfoScreenExtLead()</span><span class="sxs-lookup"><span data-stu-id="f8801-124">public int fontInfoScreenExtLead()</span></span>                         |             |
| <span data-ttu-id="f8801-125">public int fontInfoScreenHeight()</span><span class="sxs-lookup"><span data-stu-id="f8801-125">public int fontInfoScreenHeight()</span></span>                          |             |
| <span data-ttu-id="f8801-126">public int fontInfoScreenIntLead()</span><span class="sxs-lookup"><span data-stu-id="f8801-126">public int fontInfoScreenIntLead()</span></span>                         |             |
| <span data-ttu-id="f8801-127">public int height100mm(\[int heightExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="f8801-127">public int height100mm(\[int heightExclBorder\])</span></span>           |             |
| <span data-ttu-id="f8801-128">public int height100mmInclBorder(\[int heightInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="f8801-128">public int height100mmInclBorder(\[int heightInclBorder\])</span></span> |             |
| <span data-ttu-id="f8801-129">public int heightOfWordWrappedString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="f8801-129">public int heightOfWordWrappedString100mm(str string)</span></span>      |             |
| <span data-ttu-id="f8801-130">public int left100mm(\[int leftExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="f8801-130">public int left100mm(\[int leftExclBorder\])</span></span>               |             |
| <span data-ttu-id="f8801-131">public int left100mmInclBorder(\[int leftInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="f8801-131">public int left100mmInclBorder(\[int leftInclBorder\])</span></span>     |             |
| <span data-ttu-id="f8801-132">public int leftMarginAnFrame()</span><span class="sxs-lookup"><span data-stu-id="f8801-132">public int leftMarginAnFrame()</span></span>                             |             |
| <span data-ttu-id="f8801-133">public int numberOfLines(int height100mm)</span><span class="sxs-lookup"><span data-stu-id="f8801-133">public int numberOfLines(int height100mm)</span></span>                  |             |
| <span data-ttu-id="f8801-134">public int position(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f8801-134">public int position(\[int value\])</span></span>                         |             |
| <span data-ttu-id="f8801-135">public str previewInfo(str string)</span><span class="sxs-lookup"><span data-stu-id="f8801-135">public str previewInfo(str string)</span></span>                         |             |
| <span data-ttu-id="f8801-136">public int previewXCompensation100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="f8801-136">public int previewXCompensation100mm(str string)</span></span>           |             |
| <span data-ttu-id="f8801-137">public int right100mm()</span><span class="sxs-lookup"><span data-stu-id="f8801-137">public int right100mm()</span></span>                                    |             |
| <span data-ttu-id="f8801-138">public int right100mmInclBorder()</span><span class="sxs-lookup"><span data-stu-id="f8801-138">public int right100mmInclBorder()</span></span>                          |             |
| <span data-ttu-id="f8801-139">public int rightMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="f8801-139">public int rightMarginAndFrame()</span></span>                           |             |
| <span data-ttu-id="f8801-140">public str setHeightGetText(int lines, str string)</span><span class="sxs-lookup"><span data-stu-id="f8801-140">public str setHeightGetText(int lines, str string)</span></span>         |             |
| <span data-ttu-id="f8801-141">public int top100mm(\[int topExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="f8801-141">public int top100mm(\[int topExclBorder\])</span></span>                 |             |
| <span data-ttu-id="f8801-142">public int top100mmInclBorder(\[int topInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="f8801-142">public int top100mmInclBorder(\[int topInclBorder\])</span></span>       |             |
| <span data-ttu-id="f8801-143">public int topMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="f8801-143">public int topMarginAndFrame()</span></span>                             |             |
| <span data-ttu-id="f8801-144">public int width100mm(\[int widthExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="f8801-144">public int width100mm(\[int widthExclBorder\])</span></span>             |             |
| <span data-ttu-id="f8801-145">public int width100mmInclBorder(\[int widthInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="f8801-145">public int width100mmInclBorder(\[int widthInclBorder\])</span></span>   |             |
| <span data-ttu-id="f8801-146">public int widthOfString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="f8801-146">public int widthOfString100mm(str string)</span></span>                  |             |
| <span data-ttu-id="f8801-147">public void show()</span><span class="sxs-lookup"><span data-stu-id="f8801-147">public void show()</span></span>                                         |             |
| <span data-ttu-id="f8801-148">public void hide()</span><span class="sxs-lookup"><span data-stu-id="f8801-148">public void hide()</span></span>                                         |             |

## <a name="method-bottommarginandframe"></a><span data-ttu-id="f8801-149">メソッド bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="f8801-149">Method bottomMarginAndFrame</span></span>

```xpp
public int bottomMarginAndFrame()
```

### <a name="return-value---bottommarginandframe"></a><span data-ttu-id="f8801-150">戻り値 - bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="f8801-150">Return Value - bottomMarginAndFrame</span></span>

## <a name="method-controltype"></a><span data-ttu-id="f8801-151">メソッド controlType</span><span class="sxs-lookup"><span data-stu-id="f8801-151">Method controlType</span></span>

```xpp
public ReportFieldType controlType()
```

### <a name="return-value---controltype"></a><span data-ttu-id="f8801-152">戻り値 - controlType</span><span class="sxs-lookup"><span data-stu-id="f8801-152">Return Value - controlType</span></span>

## <a name="method-delete"></a><span data-ttu-id="f8801-153">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="f8801-153">Method delete</span></span>

```xpp
public int delete()
```

### <a name="return-value---delete"></a><span data-ttu-id="f8801-154">戻り値 - delete</span><span class="sxs-lookup"><span data-stu-id="f8801-154">Return Value - delete</span></span>

## <a name="method-effectivefont"></a><span data-ttu-id="f8801-155">メソッド effectiveFont</span><span class="sxs-lookup"><span data-stu-id="f8801-155">Method effectiveFont</span></span>

```xpp
public str effectiveFont()
```

### <a name="return-value---effectivefont"></a><span data-ttu-id="f8801-156">戻り値 - effectiveFont</span><span class="sxs-lookup"><span data-stu-id="f8801-156">Return Value - effectiveFont</span></span>

## <a name="method-fontinfoprinter"></a><span data-ttu-id="f8801-157">メソッド fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="f8801-157">Method fontInfoPrinter</span></span>

```xpp
public str fontInfoPrinter()
```

### <a name="return-value---fontinfoprinter"></a><span data-ttu-id="f8801-158">戻り値 - fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="f8801-158">Return Value - fontInfoPrinter</span></span>

## <a name="method-fontinfoprinterascent"></a><span data-ttu-id="f8801-159">メソッド fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="f8801-159">Method fontInfoPrinterAscent</span></span>

```xpp
public int fontInfoPrinterAscent()
```

### <a name="return-value---fontinfoprinterascent"></a><span data-ttu-id="f8801-160">戻り値 - fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="f8801-160">Return Value - fontInfoPrinterAscent</span></span>

## <a name="method-fontinfoprinterdescent"></a><span data-ttu-id="f8801-161">メソッド fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="f8801-161">Method fontInfoPrinterDescent</span></span>

```xpp
public int fontInfoPrinterDescent()
```

### <a name="return-value---fontinfoprinterdescent"></a><span data-ttu-id="f8801-162">戻り値 - fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="f8801-162">Return Value - fontInfoPrinterDescent</span></span>

## <a name="method-fontinfoprinterextlead"></a><span data-ttu-id="f8801-163">メソッド fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="f8801-163">Method fontInfoPrinterExtLead</span></span>

```xpp
public int fontInfoPrinterExtLead()
```

### <a name="return-value---fontinfoprinterextlead"></a><span data-ttu-id="f8801-164">戻り値 - fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="f8801-164">Return Value - fontInfoPrinterExtLead</span></span>

## <a name="method-fontinfoprinterheight"></a><span data-ttu-id="f8801-165">メソッド fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="f8801-165">Method fontInfoPrinterHeight</span></span>

```xpp
public int fontInfoPrinterHeight()
```

### <a name="return-value---fontinfoprinterheight"></a><span data-ttu-id="f8801-166">戻り値 - fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="f8801-166">Return Value - fontInfoPrinterHeight</span></span>

## <a name="method-fontinfoprinterintlead"></a><span data-ttu-id="f8801-167">メソッド fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="f8801-167">Method fontInfoPrinterIntLead</span></span>

```xpp
public int fontInfoPrinterIntLead()
```

### <a name="return-value---fontinfoprinterintlead"></a><span data-ttu-id="f8801-168">戻り値 - fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="f8801-168">Return Value - fontInfoPrinterIntLead</span></span>

## <a name="method-fontinfoscreen"></a><span data-ttu-id="f8801-169">メソッド fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="f8801-169">Method fontInfoScreen</span></span>

```xpp
public str fontInfoScreen()
```

### <a name="return-value---fontinfoscreen"></a><span data-ttu-id="f8801-170">戻り値 - fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="f8801-170">Return Value - fontInfoScreen</span></span>

## <a name="method-fontinfoscreenascent"></a><span data-ttu-id="f8801-171">メソッド fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="f8801-171">Method fontInfoScreenAscent</span></span>

```xpp
public int fontInfoScreenAscent()
```

### <a name="return-value---fontinfoscreenascent"></a><span data-ttu-id="f8801-172">戻り値 - fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="f8801-172">Return Value - fontInfoScreenAscent</span></span>

## <a name="method-fontinfoscreendescent"></a><span data-ttu-id="f8801-173">メソッド fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="f8801-173">Method fontInfoScreenDescent</span></span>

```xpp
public int fontInfoScreenDescent()
```

### <a name="return-value---fontinfoscreendescent"></a><span data-ttu-id="f8801-174">戻り値 - fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="f8801-174">Return Value - fontInfoScreenDescent</span></span>

## <a name="method-fontinfoscreenextlead"></a><span data-ttu-id="f8801-175">メソッド fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="f8801-175">Method fontInfoScreenExtLead</span></span>

```xpp
public int fontInfoScreenExtLead()
```

### <a name="return-value---fontinfoscreenextlead"></a><span data-ttu-id="f8801-176">戻り値 - fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="f8801-176">Return Value - fontInfoScreenExtLead</span></span>

## <a name="method-fontinfoscreenheight"></a><span data-ttu-id="f8801-177">メソッド fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="f8801-177">Method fontInfoScreenHeight</span></span>

```xpp
public int fontInfoScreenHeight()
```

### <a name="return-value---fontinfoscreenheight"></a><span data-ttu-id="f8801-178">戻り値 - fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="f8801-178">Return Value - fontInfoScreenHeight</span></span>

## <a name="method-fontinfoscreenintlead"></a><span data-ttu-id="f8801-179">メソッド fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="f8801-179">Method fontInfoScreenIntLead</span></span>

```xpp
public int fontInfoScreenIntLead()
```

### <a name="return-value---fontinfoscreenintlead"></a><span data-ttu-id="f8801-180">戻り値 - fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="f8801-180">Return Value - fontInfoScreenIntLead</span></span>

## <a name="method-height100mm"></a><span data-ttu-id="f8801-181">メソッド height100mm</span><span class="sxs-lookup"><span data-stu-id="f8801-181">Method height100mm</span></span>

```xpp
public int height100mm([int heightExclBorder])
```

### <a name="parameters---height100mm"></a><span data-ttu-id="f8801-182">パラメーター - height100mm</span><span class="sxs-lookup"><span data-stu-id="f8801-182">Parameters - height100mm</span></span>

<span data-ttu-id="f8801-183">heightExclBorder</span><span class="sxs-lookup"><span data-stu-id="f8801-183">heightExclBorder</span></span>  

### <a name="return-value---height100mm"></a><span data-ttu-id="f8801-184">戻り値 - height100mm</span><span class="sxs-lookup"><span data-stu-id="f8801-184">Return Value - height100mm</span></span>

## <a name="method-height100mminclborder"></a><span data-ttu-id="f8801-185">メソッド height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f8801-185">Method height100mmInclBorder</span></span>

```xpp
public int height100mmInclBorder([int heightInclBorder])
```

### <a name="parameters---height100mminclborder"></a><span data-ttu-id="f8801-186">パラメーター - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f8801-186">Parameters - height100mmInclBorder</span></span>

<span data-ttu-id="f8801-187">heightInclBorder</span><span class="sxs-lookup"><span data-stu-id="f8801-187">heightInclBorder</span></span>  

### <a name="return-value---height100mminclborder"></a><span data-ttu-id="f8801-188">戻り値 - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f8801-188">Return Value - height100mmInclBorder</span></span>

## <a name="method-heightofwordwrappedstring100mm"></a><span data-ttu-id="f8801-189">メソッド heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="f8801-189">Method heightOfWordWrappedString100mm</span></span>

```xpp
public int heightOfWordWrappedString100mm(str string)
```

### <a name="parameters---heightofwordwrappedstring100mm"></a><span data-ttu-id="f8801-190">パラメーター - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="f8801-190">Parameters - heightOfWordWrappedString100mm</span></span>

<span data-ttu-id="f8801-191">文字列</span><span class="sxs-lookup"><span data-stu-id="f8801-191">string</span></span>  

### <a name="return-value---heightofwordwrappedstring100mm"></a><span data-ttu-id="f8801-192">戻り値 - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="f8801-192">Return Value - heightOfWordWrappedString100mm</span></span>

## <a name="method-left100mm"></a><span data-ttu-id="f8801-193">メソッド left100mm</span><span class="sxs-lookup"><span data-stu-id="f8801-193">Method left100mm</span></span>

```xpp
public int left100mm([int leftExclBorder])
```

### <a name="parameters---left100mm"></a><span data-ttu-id="f8801-194">パラメーター - left100mm</span><span class="sxs-lookup"><span data-stu-id="f8801-194">Parameters - left100mm</span></span>

<span data-ttu-id="f8801-195">leftExclBorder</span><span class="sxs-lookup"><span data-stu-id="f8801-195">leftExclBorder</span></span>  

### <a name="return-value---left100mm"></a><span data-ttu-id="f8801-196">戻り値 - left100mm</span><span class="sxs-lookup"><span data-stu-id="f8801-196">Return Value - left100mm</span></span>

## <a name="method-left100mminclborder"></a><span data-ttu-id="f8801-197">メソッド left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f8801-197">Method left100mmInclBorder</span></span>

```xpp
public int left100mmInclBorder([int leftInclBorder])
```

### <a name="parameters---left100mminclborder"></a><span data-ttu-id="f8801-198">パラメーター - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f8801-198">Parameters - left100mmInclBorder</span></span>

<span data-ttu-id="f8801-199">leftInclBorder</span><span class="sxs-lookup"><span data-stu-id="f8801-199">leftInclBorder</span></span>  

### <a name="return-value---left100mminclborder"></a><span data-ttu-id="f8801-200">戻り値 - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f8801-200">Return Value - left100mmInclBorder</span></span>

## <a name="method-leftmarginanframe"></a><span data-ttu-id="f8801-201">メソッド leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="f8801-201">Method leftMarginAnFrame</span></span>

```xpp
public int leftMarginAnFrame()
```

### <a name="return-value---leftmarginanframe"></a><span data-ttu-id="f8801-202">戻り値 - leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="f8801-202">Return Value - leftMarginAnFrame</span></span>

## <a name="method-numberoflines"></a><span data-ttu-id="f8801-203">メソッド numberOfLines</span><span class="sxs-lookup"><span data-stu-id="f8801-203">Method numberOfLines</span></span>

```xpp
public int numberOfLines(int height100mm)
```

### <a name="parameters---numberoflines"></a><span data-ttu-id="f8801-204">パラメーター - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="f8801-204">Parameters - numberOfLines</span></span>

<span data-ttu-id="f8801-205">height100mm</span><span class="sxs-lookup"><span data-stu-id="f8801-205">height100mm</span></span>  

### <a name="return-value---numberoflines"></a><span data-ttu-id="f8801-206">戻り値 - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="f8801-206">Return Value - numberOfLines</span></span>

## <a name="method-position"></a><span data-ttu-id="f8801-207">メソッドの位置</span><span class="sxs-lookup"><span data-stu-id="f8801-207">Method position</span></span>

```xpp
public int position([int value])
```

### <a name="parameters---position"></a><span data-ttu-id="f8801-208">パラメーター - position</span><span class="sxs-lookup"><span data-stu-id="f8801-208">Parameters - position</span></span>

<span data-ttu-id="f8801-209">値</span><span class="sxs-lookup"><span data-stu-id="f8801-209">value</span></span>  

### <a name="return-value---position"></a><span data-ttu-id="f8801-210">戻り値 - position</span><span class="sxs-lookup"><span data-stu-id="f8801-210">Return Value - position</span></span>

## <a name="method-previewinfo"></a><span data-ttu-id="f8801-211">メソッド previewInfo</span><span class="sxs-lookup"><span data-stu-id="f8801-211">Method previewInfo</span></span>

```xpp
public str previewInfo(str string)
```

### <a name="parameters---previewinfo"></a><span data-ttu-id="f8801-212">パラメーター - previewInfo</span><span class="sxs-lookup"><span data-stu-id="f8801-212">Parameters - previewInfo</span></span>

<span data-ttu-id="f8801-213">文字列</span><span class="sxs-lookup"><span data-stu-id="f8801-213">string</span></span>  

### <a name="return-value---previewinfo"></a><span data-ttu-id="f8801-214">戻り値 - previewInfo</span><span class="sxs-lookup"><span data-stu-id="f8801-214">Return Value - previewInfo</span></span>

## <a name="method-previewxcompensation100mm"></a><span data-ttu-id="f8801-215">メソッド previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="f8801-215">Method previewXCompensation100mm</span></span>

```xpp
public int previewXCompensation100mm(str string)
```

### <a name="parameters---previewxcompensation100mm"></a><span data-ttu-id="f8801-216">パラメーター - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="f8801-216">Parameters - previewXCompensation100mm</span></span>

<span data-ttu-id="f8801-217">文字列</span><span class="sxs-lookup"><span data-stu-id="f8801-217">string</span></span>  

### <a name="return-value---previewxcompensation100mm"></a><span data-ttu-id="f8801-218">戻り値 - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="f8801-218">Return Value - previewXCompensation100mm</span></span>

## <a name="method-right100mm"></a><span data-ttu-id="f8801-219">メソッド right100mm</span><span class="sxs-lookup"><span data-stu-id="f8801-219">Method right100mm</span></span>

```xpp
public int right100mm()
```

### <a name="return-value---right100mm"></a><span data-ttu-id="f8801-220">戻り値 - right100mm</span><span class="sxs-lookup"><span data-stu-id="f8801-220">Return Value - right100mm</span></span>

## <a name="method-right100mminclborder"></a><span data-ttu-id="f8801-221">メソッド right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f8801-221">Method right100mmInclBorder</span></span>

```xpp
public int right100mmInclBorder()
```

### <a name="return-value---right100mminclborder"></a><span data-ttu-id="f8801-222">戻り値 - right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f8801-222">Return Value - right100mmInclBorder</span></span>

## <a name="method-rightmarginandframe"></a><span data-ttu-id="f8801-223">メソッド rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="f8801-223">Method rightMarginAndFrame</span></span>

```xpp
public int rightMarginAndFrame()
```

### <a name="return-value---rightmarginandframe"></a><span data-ttu-id="f8801-224">戻り値 - rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="f8801-224">Return Value - rightMarginAndFrame</span></span>

## <a name="method-setheightgettext"></a><span data-ttu-id="f8801-225">メソッド setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="f8801-225">Method setHeightGetText</span></span>

```xpp
public str setHeightGetText(int lines, str string)
```

### <a name="parameters---setheightgettext"></a><span data-ttu-id="f8801-226">パラメーター - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="f8801-226">Parameters - setHeightGetText</span></span>

<span data-ttu-id="f8801-227">明細行</span><span class="sxs-lookup"><span data-stu-id="f8801-227">lines</span></span>  

<!-- -->

<span data-ttu-id="f8801-228">文字列</span><span class="sxs-lookup"><span data-stu-id="f8801-228">string</span></span>  

### <a name="return-value---setheightgettext"></a><span data-ttu-id="f8801-229">戻り値 - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="f8801-229">Return Value - setHeightGetText</span></span>

## <a name="method-top100mm"></a><span data-ttu-id="f8801-230">メソッド top100mm</span><span class="sxs-lookup"><span data-stu-id="f8801-230">Method top100mm</span></span>

```xpp
public int top100mm([int topExclBorder])
```

### <a name="parameters---top100mm"></a><span data-ttu-id="f8801-231">パラメーター - top100mm</span><span class="sxs-lookup"><span data-stu-id="f8801-231">Parameters - top100mm</span></span>

<span data-ttu-id="f8801-232">topExclBorder</span><span class="sxs-lookup"><span data-stu-id="f8801-232">topExclBorder</span></span>  

### <a name="return-value---top100mm"></a><span data-ttu-id="f8801-233">戻り値 - top100mm</span><span class="sxs-lookup"><span data-stu-id="f8801-233">Return Value - top100mm</span></span>

## <a name="method-top100mminclborder"></a><span data-ttu-id="f8801-234">メソッド top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f8801-234">Method top100mmInclBorder</span></span>

```xpp
public int top100mmInclBorder([int topInclBorder])
```

### <a name="parameters---top100mminclborder"></a><span data-ttu-id="f8801-235">パラメーター - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f8801-235">Parameters - top100mmInclBorder</span></span>

<span data-ttu-id="f8801-236">topInclBorder</span><span class="sxs-lookup"><span data-stu-id="f8801-236">topInclBorder</span></span>  

### <a name="return-value---top100mminclborder"></a><span data-ttu-id="f8801-237">戻り値 - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f8801-237">Return Value - top100mmInclBorder</span></span>

## <a name="method-topmarginandframe"></a><span data-ttu-id="f8801-238">メソッド topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="f8801-238">Method topMarginAndFrame</span></span>

```xpp
public int topMarginAndFrame()
```

### <a name="return-value---topmarginandframe"></a><span data-ttu-id="f8801-239">戻り値 - topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="f8801-239">Return Value - topMarginAndFrame</span></span>

## <a name="method-width100mm"></a><span data-ttu-id="f8801-240">メソッド width100mm</span><span class="sxs-lookup"><span data-stu-id="f8801-240">Method width100mm</span></span>

```xpp
public int width100mm([int widthExclBorder])
```

### <a name="parameters---width100mm"></a><span data-ttu-id="f8801-241">パラメーター - width100mm</span><span class="sxs-lookup"><span data-stu-id="f8801-241">Parameters - width100mm</span></span>

<span data-ttu-id="f8801-242">widthExclBorder</span><span class="sxs-lookup"><span data-stu-id="f8801-242">widthExclBorder</span></span>  

### <a name="return-value---width100mm"></a><span data-ttu-id="f8801-243">戻り値 - width100mm</span><span class="sxs-lookup"><span data-stu-id="f8801-243">Return Value - width100mm</span></span>

## <a name="method-width100mminclborder"></a><span data-ttu-id="f8801-244">メソッド width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f8801-244">Method width100mmInclBorder</span></span>

```xpp
public int width100mmInclBorder([int widthInclBorder])
```

### <a name="parameters---width100mminclborder"></a><span data-ttu-id="f8801-245">パラメーター - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f8801-245">Parameters - width100mmInclBorder</span></span>

<span data-ttu-id="f8801-246">widthInclBorder</span><span class="sxs-lookup"><span data-stu-id="f8801-246">widthInclBorder</span></span>  

### <a name="return-value---width100mminclborder"></a><span data-ttu-id="f8801-247">戻り値 - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f8801-247">Return Value - width100mmInclBorder</span></span>

## <a name="method-widthofstring100mm"></a><span data-ttu-id="f8801-248">メソッド widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="f8801-248">Method widthOfString100mm</span></span>

```xpp
public int widthOfString100mm(str string)
```

### <a name="parameters---widthofstring100mm"></a><span data-ttu-id="f8801-249">パラメーター - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="f8801-249">Parameters - widthOfString100mm</span></span>

<span data-ttu-id="f8801-250">文字列</span><span class="sxs-lookup"><span data-stu-id="f8801-250">string</span></span>  

### <a name="return-value---widthofstring100mm"></a><span data-ttu-id="f8801-251">戻り値 - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="f8801-251">Return Value - widthOfString100mm</span></span>

## <a name="method-show"></a><span data-ttu-id="f8801-252">メソッド show</span><span class="sxs-lookup"><span data-stu-id="f8801-252">Method show</span></span>

```xpp
public void show()
```

## <a name="method-hide"></a><span data-ttu-id="f8801-253">メソッド hide</span><span class="sxs-lookup"><span data-stu-id="f8801-253">Method hide</span></span>

```xpp
public void hide()
```

