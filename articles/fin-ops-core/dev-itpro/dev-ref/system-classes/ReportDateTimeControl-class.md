---
title: ReportDateTimeControl クラス
description: このトピックでは、ReportDateTimeControl クラスについて説明します。
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
ms.openlocfilehash: 644c0986f39e107e342cc757e9210f0f4103aed2
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502843"
---
# <a name="class-reportdatetimecontrol"></a><span data-ttu-id="da054-103">クラス ReportDateTimeControl</span><span class="sxs-lookup"><span data-stu-id="da054-103">Class ReportDateTimeControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ReportDateTimeControl extends ReportControl
```

## <a name="remarks"></a><span data-ttu-id="da054-104">備考</span><span class="sxs-lookup"><span data-stu-id="da054-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="da054-105">例</span><span class="sxs-lookup"><span data-stu-id="da054-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="da054-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="da054-106">Methods</span></span>

| <span data-ttu-id="da054-107">方法</span><span class="sxs-lookup"><span data-stu-id="da054-107">Method</span></span>                                                                   | <span data-ttu-id="da054-108">説明</span><span class="sxs-lookup"><span data-stu-id="da054-108">Description</span></span>                                                                                                                                |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da054-109">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-109">public int alignment(\[int value\])</span></span>                                      |                                                                                                                                            |
| <span data-ttu-id="da054-110">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-110">public int arrayIndex(\[int value\])</span></span>                                     |                                                                                                                                            |
| <span data-ttu-id="da054-111">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="da054-111">public boolean autoDeclaration(\[boolean value\])</span></span>                        | <span data-ttu-id="da054-112">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="da054-112">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                         |
| <span data-ttu-id="da054-113">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-113">public int backgroundColor(\[int value\])</span></span>                                | <span data-ttu-id="da054-114">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-114">Gets or sets the background color of the control.</span></span>                                                                                          |
| <span data-ttu-id="da054-115">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-115">public int backStyle(\[int value\])</span></span>                                      | <span data-ttu-id="da054-116">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="da054-116">Determines whether the control background can be transparent.</span></span>                                                                             |
| <span data-ttu-id="da054-117">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-117">public int bold(\[int value\])</span></span>                                           | <span data-ttu-id="da054-118">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-118">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                                |
| <span data-ttu-id="da054-119">public int bottomMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="da054-119">public int bottomMarginAndFrame()</span></span>                                        |                                                                                                                                            |
| <span data-ttu-id="da054-120">public int bottomMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-120">public int bottomMarginMode(\[int value\])</span></span>                               |                                                                                                                                            |
| <span data-ttu-id="da054-121">public str bottomMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="da054-121">public str bottomMarginStr(\[str value\])</span></span>                                |                                                                                                                                            |
| <span data-ttu-id="da054-122">public Units bottomMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="da054-122">public Units bottomMarginUnit(\[Units value\])</span></span>                           |                                                                                                                                            |
| <span data-ttu-id="da054-123">public Real bottomMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="da054-123">public Real bottomMarginValue(\[Real value\])</span></span>                            |                                                                                                                                            |
| <span data-ttu-id="da054-124">public int changeLabelCase(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-124">public int changeLabelCase(\[int value\])</span></span>                                |                                                                                                                                            |
| <span data-ttu-id="da054-125">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-125">public int characterSet(\[int value\])</span></span>                                   | <span data-ttu-id="da054-126">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-126">Gets or sets the character set of the font.</span></span>                                                                                                |
| <span data-ttu-id="da054-127">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-127">public int colorScheme(\[int value\])</span></span>                                    | <span data-ttu-id="da054-128">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-128">Gets or sets the color scheme of the control.</span></span>                                                                                              |
| <span data-ttu-id="da054-129">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="da054-129">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="da054-130">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-130">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                        |
| <span data-ttu-id="da054-131">public ReportFieldType controlType()</span><span class="sxs-lookup"><span data-stu-id="da054-131">public ReportFieldType controlType()</span></span>                                     |                                                                                                                                            |
| <span data-ttu-id="da054-132">public str cssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="da054-132">public str cssClass(\[str value\])</span></span>                                       |                                                                                                                                            |
| <span data-ttu-id="da054-133">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="da054-133">public FieldId dataField(\[FieldId value\])</span></span>                              |                                                                                                                                            |
| <span data-ttu-id="da054-134">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="da054-134">public str dataMethod(\[str value\])</span></span>                                     |                                                                                                                                            |
| <span data-ttu-id="da054-135">public int dateDay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-135">public int dateDay(\[int value\])</span></span>                                        |                                                                                                                                            |
| <span data-ttu-id="da054-136">public int dateFormat(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-136">public int dateFormat(\[int value\])</span></span>                                     |                                                                                                                                            |
| <span data-ttu-id="da054-137">public int dateMonth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-137">public int dateMonth(\[int value\])</span></span>                                      |                                                                                                                                            |
| <span data-ttu-id="da054-138">public int dateSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-138">public int dateSeparator(\[int value\])</span></span>                                  |                                                                                                                                            |
| <span data-ttu-id="da054-139">public int dateYear(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-139">public int dateYear(\[int value\])</span></span>                                       |                                                                                                                                            |
| <span data-ttu-id="da054-140">public int delete()</span><span class="sxs-lookup"><span data-stu-id="da054-140">public int delete()</span></span>                                                      |                                                                                                                                            |
| <span data-ttu-id="da054-141">public str effectiveFont()</span><span class="sxs-lookup"><span data-stu-id="da054-141">public str effectiveFont()</span></span>                                               |                                                                                                                                            |
| <span data-ttu-id="da054-142">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="da054-142">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>         |                                                                                                                                            |
| <span data-ttu-id="da054-143">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="da054-143">public str font(\[str value\])</span></span>                                           | <span data-ttu-id="da054-144">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-144">Gets or sets the name of the font for the control to use.</span></span>                                                                                  |
| <span data-ttu-id="da054-145">public str fontInfoPrinter()</span><span class="sxs-lookup"><span data-stu-id="da054-145">public str fontInfoPrinter()</span></span>                                             |                                                                                                                                            |
| <span data-ttu-id="da054-146">public int fontInfoPrinterAscent()</span><span class="sxs-lookup"><span data-stu-id="da054-146">public int fontInfoPrinterAscent()</span></span>                                       |                                                                                                                                            |
| <span data-ttu-id="da054-147">public int fontInfoPrinterDescent()</span><span class="sxs-lookup"><span data-stu-id="da054-147">public int fontInfoPrinterDescent()</span></span>                                      |                                                                                                                                            |
| <span data-ttu-id="da054-148">public int fontInfoPrinterExtLead()</span><span class="sxs-lookup"><span data-stu-id="da054-148">public int fontInfoPrinterExtLead()</span></span>                                      |                                                                                                                                            |
| <span data-ttu-id="da054-149">public int fontInfoPrinterHeight()</span><span class="sxs-lookup"><span data-stu-id="da054-149">public int fontInfoPrinterHeight()</span></span>                                       |                                                                                                                                            |
| <span data-ttu-id="da054-150">public int fontInfoPrinterIntLead()</span><span class="sxs-lookup"><span data-stu-id="da054-150">public int fontInfoPrinterIntLead()</span></span>                                      |                                                                                                                                            |
| <span data-ttu-id="da054-151">public str fontInfoScreen()</span><span class="sxs-lookup"><span data-stu-id="da054-151">public str fontInfoScreen()</span></span>                                              |                                                                                                                                            |
| <span data-ttu-id="da054-152">public int fontInfoScreenAscent()</span><span class="sxs-lookup"><span data-stu-id="da054-152">public int fontInfoScreenAscent()</span></span>                                        |                                                                                                                                            |
| <span data-ttu-id="da054-153">public int fontInfoScreenDescent()</span><span class="sxs-lookup"><span data-stu-id="da054-153">public int fontInfoScreenDescent()</span></span>                                       |                                                                                                                                            |
| <span data-ttu-id="da054-154">public int fontInfoScreenExtLead()</span><span class="sxs-lookup"><span data-stu-id="da054-154">public int fontInfoScreenExtLead()</span></span>                                       |                                                                                                                                            |
| <span data-ttu-id="da054-155">public int fontInfoScreenHeight()</span><span class="sxs-lookup"><span data-stu-id="da054-155">public int fontInfoScreenHeight()</span></span>                                        |                                                                                                                                            |
| <span data-ttu-id="da054-156">public int fontInfoScreenIntLead()</span><span class="sxs-lookup"><span data-stu-id="da054-156">public int fontInfoScreenIntLead()</span></span>                                       |                                                                                                                                            |
| <span data-ttu-id="da054-157">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-157">public int fontSize(\[int value\])</span></span>                                       | <span data-ttu-id="da054-158">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-158">Gets or sets the size of the font for the control to use.</span></span>                                                                                  |
| <span data-ttu-id="da054-159">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-159">public int foregroundColor(\[int value\])</span></span>                                | <span data-ttu-id="da054-160">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-160">Gets or sets the text color for the control to use.</span></span>                                                                                        |
| <span data-ttu-id="da054-161">public int height100mm(\[int heightExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="da054-161">public int height100mm(\[int heightExclBorder\])</span></span>                         |                                                                                                                                            |
| <span data-ttu-id="da054-162">public int height100mmInclBorder(\[int heightInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="da054-162">public int height100mmInclBorder(\[int heightInclBorder\])</span></span>               |                                                                                                                                            |
| <span data-ttu-id="da054-163">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-163">public int heightMode(\[int value\])</span></span>                                     | <span data-ttu-id="da054-164">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-164">Gets or sets a calculation mode for the height of the control.</span></span>                                                                             |
| <span data-ttu-id="da054-165">public int heightOfWordWrappedString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="da054-165">public int heightOfWordWrappedString100mm(str string)</span></span>                    |                                                                                                                                            |
| <span data-ttu-id="da054-166">public str heightStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="da054-166">public str heightStr(\[str value\])</span></span>                                      |                                                                                                                                            |
| <span data-ttu-id="da054-167">public Units heightUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="da054-167">public Units heightUnit(\[Units value\])</span></span>                                 |                                                                                                                                            |
| <span data-ttu-id="da054-168">public Real heightValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="da054-168">public Real heightValue(\[Real value\])</span></span>                                  | <span data-ttu-id="da054-169">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-169">Gets or sets the height of the control.</span></span>                                                                                                    |
| <span data-ttu-id="da054-170">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="da054-170">public boolean italic(\[boolean value\])</span></span>                                 |                                                                                                                                            |
| <span data-ttu-id="da054-171">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="da054-171">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="da054-172">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-172">Gets or sets the label for a control.</span></span>                                                                                                      |
| <span data-ttu-id="da054-173">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-173">public int labelBold(\[int value\])</span></span>                                      |                                                                                                                                            |
| <span data-ttu-id="da054-174">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-174">public int labelCharacterSet(\[int value\])</span></span>                              |                                                                                                                                            |
| <span data-ttu-id="da054-175">public str labelCssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="da054-175">public str labelCssClass(\[str value\])</span></span>                                  |                                                                                                                                            |
| <span data-ttu-id="da054-176">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="da054-176">public str labelFont(\[str value\])</span></span>                                      |                                                                                                                                            |
| <span data-ttu-id="da054-177">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-177">public int labelFontSize(\[int value\])</span></span>                                  |                                                                                                                                            |
| <span data-ttu-id="da054-178">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="da054-178">public boolean labelItalic(\[boolean value\])</span></span>                            |                                                                                                                                            |
| <span data-ttu-id="da054-179">public LineType labelLineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="da054-179">public LineType labelLineBelow(\[LineType value\])</span></span>                       |                                                                                                                                            |
| <span data-ttu-id="da054-180">public LineThickness labelLineThickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="da054-180">public LineThickness labelLineThickness(\[LineThickness value\])</span></span>         |                                                                                                                                            |
| <span data-ttu-id="da054-181">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-181">public int labelPosition(\[int value\])</span></span>                                  |                                                                                                                                            |
| <span data-ttu-id="da054-182">public int labelTabLeader(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-182">public int labelTabLeader(\[int value\])</span></span>                                 |                                                                                                                                            |
| <span data-ttu-id="da054-183">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="da054-183">public boolean labelUnderline(\[boolean value\])</span></span>                         |                                                                                                                                            |
| <span data-ttu-id="da054-184">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-184">public int labelWidthMode(\[int value\])</span></span>                                 |                                                                                                                                            |
| <span data-ttu-id="da054-185">public str labelWidthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="da054-185">public str labelWidthStr(\[str value\])</span></span>                                  |                                                                                                                                            |
| <span data-ttu-id="da054-186">public Units labelWidthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="da054-186">public Units labelWidthUnit(\[Units value\])</span></span>                             |                                                                                                                                            |
| <span data-ttu-id="da054-187">public Real labelWidthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="da054-187">public Real labelWidthValue(\[Real value\])</span></span>                              |                                                                                                                                            |
| <span data-ttu-id="da054-188">public int left100mm(\[int leftExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="da054-188">public int left100mm(\[int leftExclBorder\])</span></span>                             |                                                                                                                                            |
| <span data-ttu-id="da054-189">public int left100mmInclBorder(\[int leftInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="da054-189">public int left100mmInclBorder(\[int leftInclBorder\])</span></span>                   |                                                                                                                                            |
| <span data-ttu-id="da054-190">public int leftMarginAnFrame()</span><span class="sxs-lookup"><span data-stu-id="da054-190">public int leftMarginAnFrame()</span></span>                                           |                                                                                                                                            |
| <span data-ttu-id="da054-191">public int leftMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-191">public int leftMarginMode(\[int value\])</span></span>                                 |                                                                                                                                            |
| <span data-ttu-id="da054-192">public str leftMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="da054-192">public str leftMarginStr(\[str value\])</span></span>                                  |                                                                                                                                            |
| <span data-ttu-id="da054-193">public Units leftMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="da054-193">public Units leftMarginUnit(\[Units value\])</span></span>                             |                                                                                                                                            |
| <span data-ttu-id="da054-194">public Real leftMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="da054-194">public Real leftMarginValue(\[Real value\])</span></span>                              |                                                                                                                                            |
| <span data-ttu-id="da054-195">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-195">public int leftMode(\[int value\])</span></span>                                       |                                                                                                                                            |
| <span data-ttu-id="da054-196">public str leftStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="da054-196">public str leftStr(\[str value\])</span></span>                                        |                                                                                                                                            |
| <span data-ttu-id="da054-197">public Units leftUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="da054-197">public Units leftUnit(\[Units value\])</span></span>                                   |                                                                                                                                            |
| <span data-ttu-id="da054-198">public Real leftValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="da054-198">public Real leftValue(\[Real value\])</span></span>                                    |                                                                                                                                            |
| <span data-ttu-id="da054-199">public LineType lineAbove(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="da054-199">public LineType lineAbove(\[LineType value\])</span></span>                            |                                                                                                                                            |
| <span data-ttu-id="da054-200">public LineType lineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="da054-200">public LineType lineBelow(\[LineType value\])</span></span>                            |                                                                                                                                            |
| <span data-ttu-id="da054-201">public LineType lineLeft(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="da054-201">public LineType lineLeft(\[LineType value\])</span></span>                             | <span data-ttu-id="da054-202">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-202">Gets or sets the type of line that is used as the left border of a section.</span></span>                                                                |
| <span data-ttu-id="da054-203">public LineType lineRight(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="da054-203">public LineType lineRight(\[LineType value\])</span></span>                            |                                                                                                                                            |
| <span data-ttu-id="da054-204">public str menuItemLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="da054-204">public str menuItemLabel(\[str value\])</span></span>                                  |                                                                                                                                            |
| <span data-ttu-id="da054-205">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="da054-205">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                                            |
| <span data-ttu-id="da054-206">public MenuItemType menuItemType(\[MenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="da054-206">public MenuItemType menuItemType(\[MenuItemType value\])</span></span>                 |                                                                                                                                            |
| <span data-ttu-id="da054-207">public str modelFieldName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="da054-207">public str modelFieldName(\[str value\])</span></span>                                 |                                                                                                                                            |
| <span data-ttu-id="da054-208">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="da054-208">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="da054-209">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-209">Gets or sets the name that used in the code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="da054-210">public int numberOfLines(int height100mm)</span><span class="sxs-lookup"><span data-stu-id="da054-210">public int numberOfLines(int height100mm)</span></span>                                |                                                                                                                                            |
| <span data-ttu-id="da054-211">public int position(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-211">public int position(\[int value\])</span></span>                                       |                                                                                                                                            |
| <span data-ttu-id="da054-212">public str previewInfo(str string)</span><span class="sxs-lookup"><span data-stu-id="da054-212">public str previewInfo(str string)</span></span>                                       |                                                                                                                                            |
| <span data-ttu-id="da054-213">public int previewXCompensation100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="da054-213">public int previewXCompensation100mm(str string)</span></span>                         |                                                                                                                                            |
| <span data-ttu-id="da054-214">public int right100mm()</span><span class="sxs-lookup"><span data-stu-id="da054-214">public int right100mm()</span></span>                                                  |                                                                                                                                            |
| <span data-ttu-id="da054-215">public int right100mmInclBorder()</span><span class="sxs-lookup"><span data-stu-id="da054-215">public int right100mmInclBorder()</span></span>                                        |                                                                                                                                            |
| <span data-ttu-id="da054-216">public int rightMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="da054-216">public int rightMarginAndFrame()</span></span>                                         |                                                                                                                                            |
| <span data-ttu-id="da054-217">public int rightMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-217">public int rightMarginMode(\[int value\])</span></span>                                |                                                                                                                                            |
| <span data-ttu-id="da054-218">public str rightMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="da054-218">public str rightMarginStr(\[str value\])</span></span>                                 |                                                                                                                                            |
| <span data-ttu-id="da054-219">public Units rightMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="da054-219">public Units rightMarginUnit(\[Units value\])</span></span>                            |                                                                                                                                            |
| <span data-ttu-id="da054-220">public Real rightMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="da054-220">public Real rightMarginValue(\[Real value\])</span></span>                             |                                                                                                                                            |
| <span data-ttu-id="da054-221">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="da054-221">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                                            |
| <span data-ttu-id="da054-222">public str setHeightGetText(int lines, str string)</span><span class="sxs-lookup"><span data-stu-id="da054-222">public str setHeightGetText(int lines, str string)</span></span>                       |                                                                                                                                            |
| <span data-ttu-id="da054-223">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="da054-223">public boolean showLabel(\[boolean value\])</span></span>                              |                                                                                                                                            |
| <span data-ttu-id="da054-224">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="da054-224">public TableId table(\[TableId value\])</span></span>                                  | <span data-ttu-id="da054-225">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-225">Gets or sets the table ID associated with the object.</span></span>                                                                                      |
| <span data-ttu-id="da054-226">public LineThickness thickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="da054-226">public LineThickness thickness(\[LineThickness value\])</span></span>                  |                                                                                                                                            |
| <span data-ttu-id="da054-227">public int top100mm(\[int topExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="da054-227">public int top100mm(\[int topExclBorder\])</span></span>                               |                                                                                                                                            |
| <span data-ttu-id="da054-228">public int top100mmInclBorder(\[int topInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="da054-228">public int top100mmInclBorder(\[int topInclBorder\])</span></span>                     |                                                                                                                                            |
| <span data-ttu-id="da054-229">public int topMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="da054-229">public int topMarginAndFrame()</span></span>                                           |                                                                                                                                            |
| <span data-ttu-id="da054-230">public int topMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-230">public int topMarginMode(\[int value\])</span></span>                                  |                                                                                                                                            |
| <span data-ttu-id="da054-231">public str topMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="da054-231">public str topMarginStr(\[str value\])</span></span>                                   |                                                                                                                                            |
| <span data-ttu-id="da054-232">public Units topMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="da054-232">public Units topMarginUnit(\[Units value\])</span></span>                              |                                                                                                                                            |
| <span data-ttu-id="da054-233">public Real topMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="da054-233">public Real topMarginValue(\[Real value\])</span></span>                               |                                                                                                                                            |
| <span data-ttu-id="da054-234">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-234">public int topMode(\[int value\])</span></span>                                        |                                                                                                                                            |
| <span data-ttu-id="da054-235">public str topStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="da054-235">public str topStr(\[str value\])</span></span>                                         |                                                                                                                                            |
| <span data-ttu-id="da054-236">public Units topUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="da054-236">public Units topUnit(\[Units value\])</span></span>                                    |                                                                                                                                            |
| <span data-ttu-id="da054-237">public Real topValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="da054-237">public Real topValue(\[Real value\])</span></span>                                     |                                                                                                                                            |
| <span data-ttu-id="da054-238">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="da054-238">public boolean underline(\[boolean value\])</span></span>                              |                                                                                                                                            |
| <span data-ttu-id="da054-239">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="da054-239">public boolean visible(\[boolean value\])</span></span>                                |                                                                                                                                            |
| <span data-ttu-id="da054-240">public str webMenuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="da054-240">public str webMenuItemName(\[str value\])</span></span>                                |                                                                                                                                            |
| <span data-ttu-id="da054-241">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="da054-241">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span></span>        |                                                                                                                                            |
| <span data-ttu-id="da054-242">public str webTarget(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="da054-242">public str webTarget(\[str value\])</span></span>                                      |                                                                                                                                            |
| <span data-ttu-id="da054-243">public int width100mm(\[int widthExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="da054-243">public int width100mm(\[int widthExclBorder\])</span></span>                           |                                                                                                                                            |
| <span data-ttu-id="da054-244">public int width100mmInclBorder(\[int widthInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="da054-244">public int width100mmInclBorder(\[int widthInclBorder\])</span></span>                 |                                                                                                                                            |
| <span data-ttu-id="da054-245">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="da054-245">public int widthMode(\[int value\])</span></span>                                      | <span data-ttu-id="da054-246">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-246">Gets or sets the calculation mode of the width of the control.</span></span>                                                                             |
| <span data-ttu-id="da054-247">public int widthOfString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="da054-247">public int widthOfString100mm(str string)</span></span>                                |                                                                                                                                            |
| <span data-ttu-id="da054-248">public str widthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="da054-248">public str widthStr(\[str value\])</span></span>                                       |                                                                                                                                            |
| <span data-ttu-id="da054-249">public Units widthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="da054-249">public Units widthUnit(\[Units value\])</span></span>                                  |                                                                                                                                            |
| <span data-ttu-id="da054-250">public Real widthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="da054-250">public Real widthValue(\[Real value\])</span></span>                                   | <span data-ttu-id="da054-251">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-251">Gets or sets the width of the control.</span></span>                                                                                                     |
| <span data-ttu-id="da054-252">public void height(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="da054-252">public void height(Real value, Units unit)</span></span>                               | <span data-ttu-id="da054-253">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-253">Gets or sets the height of the control.</span></span>                                                                                                    |
| <span data-ttu-id="da054-254">public void left(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="da054-254">public void left(Real value, Units unit)</span></span>                                 |                                                                                                                                            |
| <span data-ttu-id="da054-255">public void topMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="da054-255">public void topMargin(Real value, Units unit)</span></span>                            |                                                                                                                                            |
| <span data-ttu-id="da054-256">public void hide()</span><span class="sxs-lookup"><span data-stu-id="da054-256">public void hide()</span></span>                                                       |                                                                                                                                            |
| <span data-ttu-id="da054-257">public void top(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="da054-257">public void top(Real value, Units unit)</span></span>                                  |                                                                                                                                            |
| <span data-ttu-id="da054-258">public void bottomMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="da054-258">public void bottomMargin(Real value, Units unit)</span></span>                         |                                                                                                                                            |
| <span data-ttu-id="da054-259">public void labelWidth(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="da054-259">public void labelWidth(Real value, Units unit)</span></span>                           |                                                                                                                                            |
| <span data-ttu-id="da054-260">public void show()</span><span class="sxs-lookup"><span data-stu-id="da054-260">public void show()</span></span>                                                       |                                                                                                                                            |
| <span data-ttu-id="da054-261">public void rightMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="da054-261">public void rightMargin(Real value, Units unit)</span></span>                          |                                                                                                                                            |
| <span data-ttu-id="da054-262">public void width(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="da054-262">public void width(Real value, Units unit)</span></span>                                | <span data-ttu-id="da054-263">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-263">Gets or sets the width of the control.</span></span>                                                                                                     |
| <span data-ttu-id="da054-264">public void leftMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="da054-264">public void leftMargin(Real value, Units unit)</span></span>                           |                                                                                                                                            |

## <a name="method-alignment"></a><span data-ttu-id="da054-265">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="da054-265">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="da054-266">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="da054-266">Parameters - alignment</span></span>

<span data-ttu-id="da054-267">値</span><span class="sxs-lookup"><span data-stu-id="da054-267">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="da054-268">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="da054-268">Return Value - alignment</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="da054-269">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="da054-269">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="da054-270">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="da054-270">Parameters - arrayIndex</span></span>

<span data-ttu-id="da054-271">値</span><span class="sxs-lookup"><span data-stu-id="da054-271">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="da054-272">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="da054-272">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="da054-273">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="da054-273">Method autoDeclaration</span></span>

<span data-ttu-id="da054-274">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="da054-274">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="da054-275">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="da054-275">Parameters - autoDeclaration</span></span>

<span data-ttu-id="da054-276">値</span><span class="sxs-lookup"><span data-stu-id="da054-276">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="da054-277">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="da054-277">Return Value - autoDeclaration</span></span>

<span data-ttu-id="da054-278">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="da054-278">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="da054-279">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="da054-279">Remarks - autoDeclaration</span></span>

<span data-ttu-id="da054-280">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="da054-280">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="da054-281">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="da054-281">Method backgroundColor</span></span>

<span data-ttu-id="da054-282">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-282">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="da054-283">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="da054-283">Parameters - backgroundColor</span></span>

<span data-ttu-id="da054-284">値</span><span class="sxs-lookup"><span data-stu-id="da054-284">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="da054-285">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="da054-285">Return Value - backgroundColor</span></span>

<span data-ttu-id="da054-286">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="da054-286">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="da054-287">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="da054-287">Remarks - backgroundColor</span></span>

<span data-ttu-id="da054-288">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="da054-288">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="da054-289">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="da054-289">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="da054-290">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="da054-290">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="da054-291">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="da054-291">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="da054-292">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="da054-292">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="da054-293">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="da054-293">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="da054-294">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="da054-294">Method backStyle</span></span>

<span data-ttu-id="da054-295">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="da054-295">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="da054-296">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="da054-296">Parameters - backStyle</span></span>

<span data-ttu-id="da054-297">値</span><span class="sxs-lookup"><span data-stu-id="da054-297">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="da054-298">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="da054-298">Return Value - backStyle</span></span>

<span data-ttu-id="da054-299">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="da054-299">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="da054-300">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="da054-300">Method bold</span></span>

<span data-ttu-id="da054-301">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-301">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="da054-302">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="da054-302">Parameters - bold</span></span>

<span data-ttu-id="da054-303">値</span><span class="sxs-lookup"><span data-stu-id="da054-303">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="da054-304">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="da054-304">Return Value - bold</span></span>

<span data-ttu-id="da054-305">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="da054-305">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="da054-306">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="da054-306">Remarks - bold</span></span>

<span data-ttu-id="da054-307">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="da054-307">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="da054-308">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="da054-308">0 Use the default font weight.</span></span>
-   <span data-ttu-id="da054-309">1 シン。</span><span class="sxs-lookup"><span data-stu-id="da054-309">1 Thin.</span></span>
-   <span data-ttu-id="da054-310">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="da054-310">2 Extra-light.</span></span>
-   <span data-ttu-id="da054-311">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="da054-311">3 Light.</span></span>
-   <span data-ttu-id="da054-312">4 標準。</span><span class="sxs-lookup"><span data-stu-id="da054-312">4 Normal.</span></span>
-   <span data-ttu-id="da054-313">5 中。</span><span class="sxs-lookup"><span data-stu-id="da054-313">5 Medium.</span></span>
-   <span data-ttu-id="da054-314">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="da054-314">6 Semibold.</span></span>
-   <span data-ttu-id="da054-315">7 太字。</span><span class="sxs-lookup"><span data-stu-id="da054-315">7 Bold.</span></span>
-   <span data-ttu-id="da054-316">8 極太。</span><span class="sxs-lookup"><span data-stu-id="da054-316">8 Extra-bold.</span></span>
-   <span data-ttu-id="da054-317">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="da054-317">9 Heavy.</span></span>

## <a name="method-bottommarginandframe"></a><span data-ttu-id="da054-318">メソッド bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="da054-318">Method bottomMarginAndFrame</span></span>

```xpp
public int bottomMarginAndFrame()
```

### <a name="return-value---bottommarginandframe"></a><span data-ttu-id="da054-319">戻り値 - bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="da054-319">Return Value - bottomMarginAndFrame</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="da054-320">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="da054-320">Method bottomMarginMode</span></span>

```xpp
public int bottomMarginMode([int value])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="da054-321">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="da054-321">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="da054-322">値</span><span class="sxs-lookup"><span data-stu-id="da054-322">value</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="da054-323">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="da054-323">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginstr"></a><span data-ttu-id="da054-324">メソッド bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="da054-324">Method bottomMarginStr</span></span>

```xpp
public str bottomMarginStr([str value])
```

### <a name="parameters---bottommarginstr"></a><span data-ttu-id="da054-325">パラメーター - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="da054-325">Parameters - bottomMarginStr</span></span>

<span data-ttu-id="da054-326">値</span><span class="sxs-lookup"><span data-stu-id="da054-326">value</span></span>  

### <a name="return-value---bottommarginstr"></a><span data-ttu-id="da054-327">戻り値 - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="da054-327">Return Value - bottomMarginStr</span></span>

## <a name="method-bottommarginunit"></a><span data-ttu-id="da054-328">メソッド bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="da054-328">Method bottomMarginUnit</span></span>

```xpp
public Units bottomMarginUnit([Units value])
```

### <a name="parameters---bottommarginunit"></a><span data-ttu-id="da054-329">パラメーター - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="da054-329">Parameters - bottomMarginUnit</span></span>

<span data-ttu-id="da054-330">値</span><span class="sxs-lookup"><span data-stu-id="da054-330">value</span></span>  

### <a name="return-value---bottommarginunit"></a><span data-ttu-id="da054-331">戻り値 - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="da054-331">Return Value - bottomMarginUnit</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="da054-332">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="da054-332">Method bottomMarginValue</span></span>

```xpp
public Real bottomMarginValue([Real value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="da054-333">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="da054-333">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="da054-334">値</span><span class="sxs-lookup"><span data-stu-id="da054-334">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="da054-335">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="da054-335">Return Value - bottomMarginValue</span></span>

## <a name="method-changelabelcase"></a><span data-ttu-id="da054-336">メソッド changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="da054-336">Method changeLabelCase</span></span>

```xpp
public int changeLabelCase([int value])
```

### <a name="parameters---changelabelcase"></a><span data-ttu-id="da054-337">パラメーター - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="da054-337">Parameters - changeLabelCase</span></span>

<span data-ttu-id="da054-338">値</span><span class="sxs-lookup"><span data-stu-id="da054-338">value</span></span>  

### <a name="return-value---changelabelcase"></a><span data-ttu-id="da054-339">戻り値 - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="da054-339">Return Value - changeLabelCase</span></span>

## <a name="method-characterset"></a><span data-ttu-id="da054-340">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="da054-340">Method characterSet</span></span>

<span data-ttu-id="da054-341">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-341">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="da054-342">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="da054-342">Parameters - characterSet</span></span>

<span data-ttu-id="da054-343">値</span><span class="sxs-lookup"><span data-stu-id="da054-343">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="da054-344">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="da054-344">Return Value - characterSet</span></span>

<span data-ttu-id="da054-345">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="da054-345">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="da054-346">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="da054-346">Remarks - characterSet</span></span>

<span data-ttu-id="da054-347">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="da054-347">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="da054-348">値です。</span><span class="sxs-lookup"><span data-stu-id="da054-348">Value.</span></span> | <span data-ttu-id="da054-349">説明。</span><span class="sxs-lookup"><span data-stu-id="da054-349">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="da054-350">0</span><span class="sxs-lookup"><span data-stu-id="da054-350">0</span></span>      | <span data-ttu-id="da054-351">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="da054-351">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="da054-352">1</span><span class="sxs-lookup"><span data-stu-id="da054-352">1</span></span>      | <span data-ttu-id="da054-353">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="da054-353">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="da054-354">2</span><span class="sxs-lookup"><span data-stu-id="da054-354">2</span></span>      | <span data-ttu-id="da054-355">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="da054-355">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="da054-356">77</span><span class="sxs-lookup"><span data-stu-id="da054-356">77</span></span>     | <span data-ttu-id="da054-357">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="da054-357">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="da054-358">128</span><span class="sxs-lookup"><span data-stu-id="da054-358">128</span></span>    | <span data-ttu-id="da054-359">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="da054-359">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="da054-360">129</span><span class="sxs-lookup"><span data-stu-id="da054-360">129</span></span>    | <span data-ttu-id="da054-361">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="da054-361">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="da054-362">134</span><span class="sxs-lookup"><span data-stu-id="da054-362">134</span></span>    | <span data-ttu-id="da054-363">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="da054-363">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="da054-364">136</span><span class="sxs-lookup"><span data-stu-id="da054-364">136</span></span>    | <span data-ttu-id="da054-365">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="da054-365">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="da054-366">161</span><span class="sxs-lookup"><span data-stu-id="da054-366">161</span></span>    | <span data-ttu-id="da054-367">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="da054-367">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="da054-368">162</span><span class="sxs-lookup"><span data-stu-id="da054-368">162</span></span>    | <span data-ttu-id="da054-369">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="da054-369">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="da054-370">163</span><span class="sxs-lookup"><span data-stu-id="da054-370">163</span></span>    | <span data-ttu-id="da054-371">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="da054-371">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="da054-372">186</span><span class="sxs-lookup"><span data-stu-id="da054-372">186</span></span>    | <span data-ttu-id="da054-373">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="da054-373">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="da054-374">204</span><span class="sxs-lookup"><span data-stu-id="da054-374">204</span></span>    | <span data-ttu-id="da054-375">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="da054-375">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="da054-376">238</span><span class="sxs-lookup"><span data-stu-id="da054-376">238</span></span>    | <span data-ttu-id="da054-377">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="da054-377">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="da054-378">255</span><span class="sxs-lookup"><span data-stu-id="da054-378">255</span></span>    | <span data-ttu-id="da054-379">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="da054-379">OEM\_CHARSET</span></span>         |

<span data-ttu-id="da054-380">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="da054-380">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="da054-381">値です。</span><span class="sxs-lookup"><span data-stu-id="da054-381">Value.</span></span> | <span data-ttu-id="da054-382">説明。</span><span class="sxs-lookup"><span data-stu-id="da054-382">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="da054-383">130</span><span class="sxs-lookup"><span data-stu-id="da054-383">130</span></span>    | <span data-ttu-id="da054-384">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="da054-384">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="da054-385">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="da054-385">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="da054-386">値です。</span><span class="sxs-lookup"><span data-stu-id="da054-386">Value.</span></span> | <span data-ttu-id="da054-387">説明。</span><span class="sxs-lookup"><span data-stu-id="da054-387">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="da054-388">177</span><span class="sxs-lookup"><span data-stu-id="da054-388">177</span></span>    | <span data-ttu-id="da054-389">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="da054-389">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="da054-390">178</span><span class="sxs-lookup"><span data-stu-id="da054-390">178</span></span>    | <span data-ttu-id="da054-391">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="da054-391">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="da054-392">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="da054-392">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="da054-393">値です。</span><span class="sxs-lookup"><span data-stu-id="da054-393">Value.</span></span> | <span data-ttu-id="da054-394">説明。</span><span class="sxs-lookup"><span data-stu-id="da054-394">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="da054-395">222</span><span class="sxs-lookup"><span data-stu-id="da054-395">222</span></span>    | <span data-ttu-id="da054-396">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="da054-396">THAI\_CHARSET</span></span> |

<span data-ttu-id="da054-397">既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="da054-397">The default character set is set to a value, depending on the current system locale.</span></span> <span data-ttu-id="da054-398">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="da054-398">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="da054-399">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="da054-399">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="da054-400">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="da054-400">Method colorScheme</span></span>

<span data-ttu-id="da054-401">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-401">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="da054-402">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="da054-402">Parameters - colorScheme</span></span>

<span data-ttu-id="da054-403">値</span><span class="sxs-lookup"><span data-stu-id="da054-403">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="da054-404">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="da054-404">Return Value - colorScheme</span></span>

<span data-ttu-id="da054-405">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="da054-405">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="da054-406">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="da054-406">Remarks - colorScheme</span></span>

<span data-ttu-id="da054-407">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="da054-407">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="da054-408">値です。</span><span class="sxs-lookup"><span data-stu-id="da054-408">Value.</span></span> | <span data-ttu-id="da054-409">スタイル。</span><span class="sxs-lookup"><span data-stu-id="da054-409">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="da054-410">0</span><span class="sxs-lookup"><span data-stu-id="da054-410">0</span></span>      | <span data-ttu-id="da054-411">既定。</span><span class="sxs-lookup"><span data-stu-id="da054-411">Default.</span></span>                      |
| <span data-ttu-id="da054-412">1</span><span class="sxs-lookup"><span data-stu-id="da054-412">1</span></span>      | <span data-ttu-id="da054-413">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="da054-413">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="da054-414">2</span><span class="sxs-lookup"><span data-stu-id="da054-414">2</span></span>      | <span data-ttu-id="da054-415">真の配色。</span><span class="sxs-lookup"><span data-stu-id="da054-415">The true-color scheme.</span></span>        |

## <a name="method-configurationkey"></a><span data-ttu-id="da054-416">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="da054-416">Method configurationKey</span></span>

<span data-ttu-id="da054-417">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-417">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="da054-418">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="da054-418">Parameters - configurationKey</span></span>

<span data-ttu-id="da054-419">値</span><span class="sxs-lookup"><span data-stu-id="da054-419">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="da054-420">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="da054-420">Return Value - configurationKey</span></span>

<span data-ttu-id="da054-421">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="da054-421">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="da054-422">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="da054-422">Remarks - configurationKey</span></span>

<span data-ttu-id="da054-423">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="da054-423">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="da054-424">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="da054-424">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-controltype"></a><span data-ttu-id="da054-425">メソッド controlType</span><span class="sxs-lookup"><span data-stu-id="da054-425">Method controlType</span></span>

```xpp
public ReportFieldType controlType()
```

### <a name="return-value---controltype"></a><span data-ttu-id="da054-426">戻り値 - controlType</span><span class="sxs-lookup"><span data-stu-id="da054-426">Return Value - controlType</span></span>

## <a name="method-cssclass"></a><span data-ttu-id="da054-427">メソッド cssClass</span><span class="sxs-lookup"><span data-stu-id="da054-427">Method cssClass</span></span>

```xpp
public str cssClass([str value])
```

### <a name="parameters---cssclass"></a><span data-ttu-id="da054-428">パラメーター - cssClass</span><span class="sxs-lookup"><span data-stu-id="da054-428">Parameters - cssClass</span></span>

<span data-ttu-id="da054-429">値</span><span class="sxs-lookup"><span data-stu-id="da054-429">value</span></span>  

### <a name="return-value---cssclass"></a><span data-ttu-id="da054-430">戻り値 - cssClass</span><span class="sxs-lookup"><span data-stu-id="da054-430">Return Value - cssClass</span></span>

## <a name="method-datafield"></a><span data-ttu-id="da054-431">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="da054-431">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="da054-432">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="da054-432">Parameters - dataField</span></span>

<span data-ttu-id="da054-433">値</span><span class="sxs-lookup"><span data-stu-id="da054-433">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="da054-434">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="da054-434">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="da054-435">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="da054-435">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="da054-436">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="da054-436">Parameters - dataMethod</span></span>

<span data-ttu-id="da054-437">値</span><span class="sxs-lookup"><span data-stu-id="da054-437">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="da054-438">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="da054-438">Return Value - dataMethod</span></span>

## <a name="method-dateday"></a><span data-ttu-id="da054-439">メソッド dateDay</span><span class="sxs-lookup"><span data-stu-id="da054-439">Method dateDay</span></span>

```xpp
public int dateDay([int value])
```

### <a name="parameters---dateday"></a><span data-ttu-id="da054-440">パラメーター - dateDay</span><span class="sxs-lookup"><span data-stu-id="da054-440">Parameters - dateDay</span></span>

<span data-ttu-id="da054-441">値</span><span class="sxs-lookup"><span data-stu-id="da054-441">value</span></span>  

### <a name="return-value---dateday"></a><span data-ttu-id="da054-442">戻り値 - dateDay</span><span class="sxs-lookup"><span data-stu-id="da054-442">Return Value - dateDay</span></span>

## <a name="method-dateformat"></a><span data-ttu-id="da054-443">メソッド dateFormat</span><span class="sxs-lookup"><span data-stu-id="da054-443">Method dateFormat</span></span>

```xpp
public int dateFormat([int value])
```

### <a name="parameters---dateformat"></a><span data-ttu-id="da054-444">パラメーター - dateFormat</span><span class="sxs-lookup"><span data-stu-id="da054-444">Parameters - dateFormat</span></span>

<span data-ttu-id="da054-445">値</span><span class="sxs-lookup"><span data-stu-id="da054-445">value</span></span>  

### <a name="return-value---dateformat"></a><span data-ttu-id="da054-446">戻り値 - dateFormat</span><span class="sxs-lookup"><span data-stu-id="da054-446">Return Value - dateFormat</span></span>

## <a name="method-datemonth"></a><span data-ttu-id="da054-447">メソッド dateMonth</span><span class="sxs-lookup"><span data-stu-id="da054-447">Method dateMonth</span></span>

```xpp
public int dateMonth([int value])
```

### <a name="parameters---datemonth"></a><span data-ttu-id="da054-448">パラメーター - dateMonth</span><span class="sxs-lookup"><span data-stu-id="da054-448">Parameters - dateMonth</span></span>

<span data-ttu-id="da054-449">値</span><span class="sxs-lookup"><span data-stu-id="da054-449">value</span></span>  

### <a name="return-value---datemonth"></a><span data-ttu-id="da054-450">戻り値 - dateMonth</span><span class="sxs-lookup"><span data-stu-id="da054-450">Return Value - dateMonth</span></span>

## <a name="method-dateseparator"></a><span data-ttu-id="da054-451">メソッド dateSeparator</span><span class="sxs-lookup"><span data-stu-id="da054-451">Method dateSeparator</span></span>

```xpp
public int dateSeparator([int value])
```

### <a name="parameters---dateseparator"></a><span data-ttu-id="da054-452">パラメーター - dateSeparator</span><span class="sxs-lookup"><span data-stu-id="da054-452">Parameters - dateSeparator</span></span>

<span data-ttu-id="da054-453">値</span><span class="sxs-lookup"><span data-stu-id="da054-453">value</span></span>  

### <a name="return-value---dateseparator"></a><span data-ttu-id="da054-454">戻り値 - dateSeparator</span><span class="sxs-lookup"><span data-stu-id="da054-454">Return Value - dateSeparator</span></span>

## <a name="method-dateyear"></a><span data-ttu-id="da054-455">メソッド dateYear</span><span class="sxs-lookup"><span data-stu-id="da054-455">Method dateYear</span></span>

```xpp
public int dateYear([int value])
```

### <a name="parameters---dateyear"></a><span data-ttu-id="da054-456">パラメーター - dateYear</span><span class="sxs-lookup"><span data-stu-id="da054-456">Parameters - dateYear</span></span>

<span data-ttu-id="da054-457">値</span><span class="sxs-lookup"><span data-stu-id="da054-457">value</span></span>  

### <a name="return-value---dateyear"></a><span data-ttu-id="da054-458">戻り値 - dateYear</span><span class="sxs-lookup"><span data-stu-id="da054-458">Return Value - dateYear</span></span>

## <a name="method-delete"></a><span data-ttu-id="da054-459">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="da054-459">Method delete</span></span>

```xpp
public int delete()
```

### <a name="return-value---delete"></a><span data-ttu-id="da054-460">戻り値 - delete</span><span class="sxs-lookup"><span data-stu-id="da054-460">Return Value - delete</span></span>

## <a name="method-effectivefont"></a><span data-ttu-id="da054-461">メソッド effectiveFont</span><span class="sxs-lookup"><span data-stu-id="da054-461">Method effectiveFont</span></span>

```xpp
public str effectiveFont()
```

### <a name="return-value---effectivefont"></a><span data-ttu-id="da054-462">戻り値 - effectiveFont</span><span class="sxs-lookup"><span data-stu-id="da054-462">Return Value - effectiveFont</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="da054-463">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="da054-463">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="da054-464">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="da054-464">Parameters - extendedDataType</span></span>

<span data-ttu-id="da054-465">値</span><span class="sxs-lookup"><span data-stu-id="da054-465">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="da054-466">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="da054-466">Return Value - extendedDataType</span></span>

## <a name="method-font"></a><span data-ttu-id="da054-467">メソッド font</span><span class="sxs-lookup"><span data-stu-id="da054-467">Method font</span></span>

<span data-ttu-id="da054-468">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-468">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="da054-469">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="da054-469">Parameters - font</span></span>

<span data-ttu-id="da054-470">値</span><span class="sxs-lookup"><span data-stu-id="da054-470">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="da054-471">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="da054-471">Return Value - font</span></span>

<span data-ttu-id="da054-472">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="da054-472">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontinfoprinter"></a><span data-ttu-id="da054-473">メソッド fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="da054-473">Method fontInfoPrinter</span></span>

```xpp
public str fontInfoPrinter()
```

### <a name="return-value---fontinfoprinter"></a><span data-ttu-id="da054-474">戻り値 - fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="da054-474">Return Value - fontInfoPrinter</span></span>

## <a name="method-fontinfoprinterascent"></a><span data-ttu-id="da054-475">メソッド fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="da054-475">Method fontInfoPrinterAscent</span></span>

```xpp
public int fontInfoPrinterAscent()
```

### <a name="return-value---fontinfoprinterascent"></a><span data-ttu-id="da054-476">戻り値 - fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="da054-476">Return Value - fontInfoPrinterAscent</span></span>

## <a name="method-fontinfoprinterdescent"></a><span data-ttu-id="da054-477">メソッド fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="da054-477">Method fontInfoPrinterDescent</span></span>

```xpp
public int fontInfoPrinterDescent()
```

### <a name="return-value---fontinfoprinterdescent"></a><span data-ttu-id="da054-478">戻り値 - fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="da054-478">Return Value - fontInfoPrinterDescent</span></span>

## <a name="method-fontinfoprinterextlead"></a><span data-ttu-id="da054-479">メソッド fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="da054-479">Method fontInfoPrinterExtLead</span></span>

```xpp
public int fontInfoPrinterExtLead()
```

### <a name="return-value---fontinfoprinterextlead"></a><span data-ttu-id="da054-480">戻り値 - fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="da054-480">Return Value - fontInfoPrinterExtLead</span></span>

## <a name="method-fontinfoprinterheight"></a><span data-ttu-id="da054-481">メソッド fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="da054-481">Method fontInfoPrinterHeight</span></span>

```xpp
public int fontInfoPrinterHeight()
```

### <a name="return-value---fontinfoprinterheight"></a><span data-ttu-id="da054-482">戻り値 - fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="da054-482">Return Value - fontInfoPrinterHeight</span></span>

## <a name="method-fontinfoprinterintlead"></a><span data-ttu-id="da054-483">メソッド fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="da054-483">Method fontInfoPrinterIntLead</span></span>

```xpp
public int fontInfoPrinterIntLead()
```

### <a name="return-value---fontinfoprinterintlead"></a><span data-ttu-id="da054-484">戻り値 - fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="da054-484">Return Value - fontInfoPrinterIntLead</span></span>

## <a name="method-fontinfoscreen"></a><span data-ttu-id="da054-485">メソッド fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="da054-485">Method fontInfoScreen</span></span>

```xpp
public str fontInfoScreen()
```

### <a name="return-value---fontinfoscreen"></a><span data-ttu-id="da054-486">戻り値 - fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="da054-486">Return Value - fontInfoScreen</span></span>

## <a name="method-fontinfoscreenascent"></a><span data-ttu-id="da054-487">メソッド fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="da054-487">Method fontInfoScreenAscent</span></span>

```xpp
public int fontInfoScreenAscent()
```

### <a name="return-value---fontinfoscreenascent"></a><span data-ttu-id="da054-488">戻り値 - fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="da054-488">Return Value - fontInfoScreenAscent</span></span>

## <a name="method-fontinfoscreendescent"></a><span data-ttu-id="da054-489">メソッド fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="da054-489">Method fontInfoScreenDescent</span></span>

```xpp
public int fontInfoScreenDescent()
```

### <a name="return-value---fontinfoscreendescent"></a><span data-ttu-id="da054-490">戻り値 - fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="da054-490">Return Value - fontInfoScreenDescent</span></span>

## <a name="method-fontinfoscreenextlead"></a><span data-ttu-id="da054-491">メソッド fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="da054-491">Method fontInfoScreenExtLead</span></span>

```xpp
public int fontInfoScreenExtLead()
```

### <a name="return-value---fontinfoscreenextlead"></a><span data-ttu-id="da054-492">戻り値 - fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="da054-492">Return Value - fontInfoScreenExtLead</span></span>

## <a name="method-fontinfoscreenheight"></a><span data-ttu-id="da054-493">メソッド fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="da054-493">Method fontInfoScreenHeight</span></span>

```xpp
public int fontInfoScreenHeight()
```

### <a name="return-value---fontinfoscreenheight"></a><span data-ttu-id="da054-494">戻り値 - fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="da054-494">Return Value - fontInfoScreenHeight</span></span>

## <a name="method-fontinfoscreenintlead"></a><span data-ttu-id="da054-495">メソッド fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="da054-495">Method fontInfoScreenIntLead</span></span>

```xpp
public int fontInfoScreenIntLead()
```

### <a name="return-value---fontinfoscreenintlead"></a><span data-ttu-id="da054-496">戻り値 - fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="da054-496">Return Value - fontInfoScreenIntLead</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="da054-497">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="da054-497">Method fontSize</span></span>

<span data-ttu-id="da054-498">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-498">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="da054-499">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="da054-499">Parameters - fontSize</span></span>

<span data-ttu-id="da054-500">値</span><span class="sxs-lookup"><span data-stu-id="da054-500">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="da054-501">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="da054-501">Return Value - fontSize</span></span>

<span data-ttu-id="da054-502">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="da054-502">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="da054-503">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="da054-503">Method foregroundColor</span></span>

<span data-ttu-id="da054-504">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-504">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="da054-505">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="da054-505">Parameters - foregroundColor</span></span>

<span data-ttu-id="da054-506">値</span><span class="sxs-lookup"><span data-stu-id="da054-506">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="da054-507">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="da054-507">Return Value - foregroundColor</span></span>

<span data-ttu-id="da054-508">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="da054-508">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="da054-509">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="da054-509">Remarks - foregroundColor</span></span>

<span data-ttu-id="da054-510">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="da054-510">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="da054-511">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="da054-511">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="da054-512">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="da054-512">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="da054-513">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="da054-513">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="da054-514">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="da054-514">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="da054-515">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="da054-515">The maximum value for a single byte is 255.</span></span>

## <a name="method-height100mm"></a><span data-ttu-id="da054-516">メソッド height100mm</span><span class="sxs-lookup"><span data-stu-id="da054-516">Method height100mm</span></span>

```xpp
public int height100mm([int heightExclBorder])
```

### <a name="parameters---height100mm"></a><span data-ttu-id="da054-517">パラメーター - height100mm</span><span class="sxs-lookup"><span data-stu-id="da054-517">Parameters - height100mm</span></span>

<span data-ttu-id="da054-518">heightExclBorder</span><span class="sxs-lookup"><span data-stu-id="da054-518">heightExclBorder</span></span>  

### <a name="return-value---height100mm"></a><span data-ttu-id="da054-519">戻り値 - height100mm</span><span class="sxs-lookup"><span data-stu-id="da054-519">Return Value - height100mm</span></span>

## <a name="method-height100mminclborder"></a><span data-ttu-id="da054-520">メソッド height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="da054-520">Method height100mmInclBorder</span></span>

```xpp
public int height100mmInclBorder([int heightInclBorder])
```

### <a name="parameters---height100mminclborder"></a><span data-ttu-id="da054-521">パラメーター - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="da054-521">Parameters - height100mmInclBorder</span></span>

<span data-ttu-id="da054-522">heightInclBorder</span><span class="sxs-lookup"><span data-stu-id="da054-522">heightInclBorder</span></span>  

### <a name="return-value---height100mminclborder"></a><span data-ttu-id="da054-523">戻り値 - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="da054-523">Return Value - height100mmInclBorder</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="da054-524">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="da054-524">Method heightMode</span></span>

<span data-ttu-id="da054-525">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-525">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="da054-526">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="da054-526">Parameters - heightMode</span></span>

<span data-ttu-id="da054-527">値</span><span class="sxs-lookup"><span data-stu-id="da054-527">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="da054-528">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="da054-528">Return Value - heightMode</span></span>

<span data-ttu-id="da054-529">計算モード。</span><span class="sxs-lookup"><span data-stu-id="da054-529">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="da054-530">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="da054-530">Remarks - heightMode</span></span>

<span data-ttu-id="da054-531">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="da054-531">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="da054-532">モード。</span><span class="sxs-lookup"><span data-stu-id="da054-532">Mode.</span></span>          | <span data-ttu-id="da054-533">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="da054-533">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="da054-534">正確。</span><span class="sxs-lookup"><span data-stu-id="da054-534">Exact.</span></span>         | <span data-ttu-id="da054-535">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="da054-535">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="da054-536">自動。</span><span class="sxs-lookup"><span data-stu-id="da054-536">Auto.</span></span>          | <span data-ttu-id="da054-537">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="da054-537">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="da054-538">列の高さ</span><span class="sxs-lookup"><span data-stu-id="da054-538">Column height.</span></span> | <span data-ttu-id="da054-539">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="da054-539">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="da054-540">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="da054-540">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightofwordwrappedstring100mm"></a><span data-ttu-id="da054-541">メソッド heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="da054-541">Method heightOfWordWrappedString100mm</span></span>

```xpp
public int heightOfWordWrappedString100mm(str string)
```

### <a name="parameters---heightofwordwrappedstring100mm"></a><span data-ttu-id="da054-542">パラメーター - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="da054-542">Parameters - heightOfWordWrappedString100mm</span></span>

<span data-ttu-id="da054-543">文字列</span><span class="sxs-lookup"><span data-stu-id="da054-543">string</span></span>  

### <a name="return-value---heightofwordwrappedstring100mm"></a><span data-ttu-id="da054-544">戻り値 - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="da054-544">Return Value - heightOfWordWrappedString100mm</span></span>

## <a name="method-heightstr"></a><span data-ttu-id="da054-545">メソッド heightStr</span><span class="sxs-lookup"><span data-stu-id="da054-545">Method heightStr</span></span>

```xpp
public str heightStr([str value])
```

### <a name="parameters---heightstr"></a><span data-ttu-id="da054-546">パラメーター - heightStr</span><span class="sxs-lookup"><span data-stu-id="da054-546">Parameters - heightStr</span></span>

<span data-ttu-id="da054-547">値</span><span class="sxs-lookup"><span data-stu-id="da054-547">value</span></span>  

### <a name="return-value---heightstr"></a><span data-ttu-id="da054-548">戻り値 - heightStr</span><span class="sxs-lookup"><span data-stu-id="da054-548">Return Value - heightStr</span></span>

## <a name="method-heightunit"></a><span data-ttu-id="da054-549">メソッド heightUnit</span><span class="sxs-lookup"><span data-stu-id="da054-549">Method heightUnit</span></span>

```xpp
public Units heightUnit([Units value])
```

### <a name="parameters---heightunit"></a><span data-ttu-id="da054-550">パラメーター - heightUnit</span><span class="sxs-lookup"><span data-stu-id="da054-550">Parameters - heightUnit</span></span>

<span data-ttu-id="da054-551">値</span><span class="sxs-lookup"><span data-stu-id="da054-551">value</span></span>  

### <a name="return-value---heightunit"></a><span data-ttu-id="da054-552">戻り値 - heightUnit</span><span class="sxs-lookup"><span data-stu-id="da054-552">Return Value - heightUnit</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="da054-553">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="da054-553">Method heightValue</span></span>

<span data-ttu-id="da054-554">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-554">Gets or sets the height of the control.</span></span>

```xpp
public Real heightValue([Real value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="da054-555">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="da054-555">Parameters - heightValue</span></span>

<span data-ttu-id="da054-556">値</span><span class="sxs-lookup"><span data-stu-id="da054-556">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="da054-557">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="da054-557">Return Value - heightValue</span></span>

<span data-ttu-id="da054-558">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="da054-558">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="da054-559">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="da054-559">Remarks - heightValue</span></span>

<span data-ttu-id="da054-560">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="da054-560">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-italic"></a><span data-ttu-id="da054-561">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="da054-561">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="da054-562">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="da054-562">Parameters - italic</span></span>

<span data-ttu-id="da054-563">値</span><span class="sxs-lookup"><span data-stu-id="da054-563">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="da054-564">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="da054-564">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="da054-565">メソッド label</span><span class="sxs-lookup"><span data-stu-id="da054-565">Method label</span></span>

<span data-ttu-id="da054-566">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-566">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="da054-567">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="da054-567">Parameters - label</span></span>

<span data-ttu-id="da054-568">値</span><span class="sxs-lookup"><span data-stu-id="da054-568">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="da054-569">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="da054-569">Return Value - label</span></span>

<span data-ttu-id="da054-570">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="da054-570">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="da054-571">備考 - label</span><span class="sxs-lookup"><span data-stu-id="da054-571">Remarks - label</span></span>

<span data-ttu-id="da054-572">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="da054-572">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="da054-573">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="da054-573">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="da054-574">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="da054-574">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="da054-575">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="da054-575">Parameters - labelBold</span></span>

<span data-ttu-id="da054-576">値</span><span class="sxs-lookup"><span data-stu-id="da054-576">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="da054-577">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="da054-577">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="da054-578">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="da054-578">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="da054-579">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="da054-579">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="da054-580">値</span><span class="sxs-lookup"><span data-stu-id="da054-580">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="da054-581">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="da054-581">Return Value - labelCharacterSet</span></span>

## <a name="method-labelcssclass"></a><span data-ttu-id="da054-582">メソッド labelCssClass</span><span class="sxs-lookup"><span data-stu-id="da054-582">Method labelCssClass</span></span>

```xpp
public str labelCssClass([str value])
```

### <a name="parameters---labelcssclass"></a><span data-ttu-id="da054-583">パラメーター - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="da054-583">Parameters - labelCssClass</span></span>

<span data-ttu-id="da054-584">値</span><span class="sxs-lookup"><span data-stu-id="da054-584">value</span></span>  

### <a name="return-value---labelcssclass"></a><span data-ttu-id="da054-585">戻り値 - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="da054-585">Return Value - labelCssClass</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="da054-586">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="da054-586">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="da054-587">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="da054-587">Parameters - labelFont</span></span>

<span data-ttu-id="da054-588">値</span><span class="sxs-lookup"><span data-stu-id="da054-588">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="da054-589">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="da054-589">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="da054-590">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="da054-590">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="da054-591">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="da054-591">Parameters - labelFontSize</span></span>

<span data-ttu-id="da054-592">値</span><span class="sxs-lookup"><span data-stu-id="da054-592">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="da054-593">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="da054-593">Return Value - labelFontSize</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="da054-594">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="da054-594">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="da054-595">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="da054-595">Parameters - labelItalic</span></span>

<span data-ttu-id="da054-596">値</span><span class="sxs-lookup"><span data-stu-id="da054-596">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="da054-597">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="da054-597">Return Value - labelItalic</span></span>

## <a name="method-labellinebelow"></a><span data-ttu-id="da054-598">メソッド labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="da054-598">Method labelLineBelow</span></span>

```xpp
public LineType labelLineBelow([LineType value])
```

### <a name="parameters---labellinebelow"></a><span data-ttu-id="da054-599">パラメーター - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="da054-599">Parameters - labelLineBelow</span></span>

<span data-ttu-id="da054-600">値</span><span class="sxs-lookup"><span data-stu-id="da054-600">value</span></span>  

### <a name="return-value---labellinebelow"></a><span data-ttu-id="da054-601">戻り値 - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="da054-601">Return Value - labelLineBelow</span></span>

## <a name="method-labellinethickness"></a><span data-ttu-id="da054-602">メソッド labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="da054-602">Method labelLineThickness</span></span>

```xpp
public LineThickness labelLineThickness([LineThickness value])
```

### <a name="parameters---labellinethickness"></a><span data-ttu-id="da054-603">パラメーター - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="da054-603">Parameters - labelLineThickness</span></span>

<span data-ttu-id="da054-604">値</span><span class="sxs-lookup"><span data-stu-id="da054-604">value</span></span>  

### <a name="return-value---labellinethickness"></a><span data-ttu-id="da054-605">戻り値 - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="da054-605">Return Value - labelLineThickness</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="da054-606">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="da054-606">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="da054-607">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="da054-607">Parameters - labelPosition</span></span>

<span data-ttu-id="da054-608">値</span><span class="sxs-lookup"><span data-stu-id="da054-608">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="da054-609">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="da054-609">Return Value - labelPosition</span></span>

## <a name="method-labeltableader"></a><span data-ttu-id="da054-610">メソッド labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="da054-610">Method labelTabLeader</span></span>

```xpp
public int labelTabLeader([int value])
```

### <a name="parameters---labeltableader"></a><span data-ttu-id="da054-611">パラメーター - labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="da054-611">Parameters - labelTabLeader</span></span>

<span data-ttu-id="da054-612">値</span><span class="sxs-lookup"><span data-stu-id="da054-612">value</span></span>  

### <a name="return-value---labeltableader"></a><span data-ttu-id="da054-613">戻り値 - labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="da054-613">Return Value - labelTabLeader</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="da054-614">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="da054-614">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="da054-615">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="da054-615">Parameters - labelUnderline</span></span>

<span data-ttu-id="da054-616">値</span><span class="sxs-lookup"><span data-stu-id="da054-616">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="da054-617">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="da054-617">Return Value - labelUnderline</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="da054-618">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="da054-618">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="da054-619">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="da054-619">Parameters - labelWidthMode</span></span>

<span data-ttu-id="da054-620">値</span><span class="sxs-lookup"><span data-stu-id="da054-620">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="da054-621">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="da054-621">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthstr"></a><span data-ttu-id="da054-622">メソッド labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="da054-622">Method labelWidthStr</span></span>

```xpp
public str labelWidthStr([str value])
```

### <a name="parameters---labelwidthstr"></a><span data-ttu-id="da054-623">パラメーター - labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="da054-623">Parameters - labelWidthStr</span></span>

<span data-ttu-id="da054-624">値</span><span class="sxs-lookup"><span data-stu-id="da054-624">value</span></span>  

### <a name="return-value---labelwidthstr"></a><span data-ttu-id="da054-625">戻り値 - labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="da054-625">Return Value - labelWidthStr</span></span>

## <a name="method-labelwidthunit"></a><span data-ttu-id="da054-626">メソッド labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="da054-626">Method labelWidthUnit</span></span>

```xpp
public Units labelWidthUnit([Units value])
```

### <a name="parameters---labelwidthunit"></a><span data-ttu-id="da054-627">パラメーター - labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="da054-627">Parameters - labelWidthUnit</span></span>

<span data-ttu-id="da054-628">値</span><span class="sxs-lookup"><span data-stu-id="da054-628">value</span></span>  

### <a name="return-value---labelwidthunit"></a><span data-ttu-id="da054-629">戻り値 - labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="da054-629">Return Value - labelWidthUnit</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="da054-630">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="da054-630">Method labelWidthValue</span></span>

```xpp
public Real labelWidthValue([Real value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="da054-631">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="da054-631">Parameters - labelWidthValue</span></span>

<span data-ttu-id="da054-632">値</span><span class="sxs-lookup"><span data-stu-id="da054-632">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="da054-633">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="da054-633">Return Value - labelWidthValue</span></span>

## <a name="method-left100mm"></a><span data-ttu-id="da054-634">メソッド left100mm</span><span class="sxs-lookup"><span data-stu-id="da054-634">Method left100mm</span></span>

```xpp
public int left100mm([int leftExclBorder])
```

### <a name="parameters---left100mm"></a><span data-ttu-id="da054-635">パラメーター - left100mm</span><span class="sxs-lookup"><span data-stu-id="da054-635">Parameters - left100mm</span></span>

<span data-ttu-id="da054-636">leftExclBorder</span><span class="sxs-lookup"><span data-stu-id="da054-636">leftExclBorder</span></span>  

### <a name="return-value---left100mm"></a><span data-ttu-id="da054-637">戻り値 - left100mm</span><span class="sxs-lookup"><span data-stu-id="da054-637">Return Value - left100mm</span></span>

## <a name="method-left100mminclborder"></a><span data-ttu-id="da054-638">メソッド left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="da054-638">Method left100mmInclBorder</span></span>

```xpp
public int left100mmInclBorder([int leftInclBorder])
```

### <a name="parameters---left100mminclborder"></a><span data-ttu-id="da054-639">パラメーター - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="da054-639">Parameters - left100mmInclBorder</span></span>

<span data-ttu-id="da054-640">leftInclBorder</span><span class="sxs-lookup"><span data-stu-id="da054-640">leftInclBorder</span></span>  

### <a name="return-value---left100mminclborder"></a><span data-ttu-id="da054-641">戻り値 - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="da054-641">Return Value - left100mmInclBorder</span></span>

## <a name="method-leftmarginanframe"></a><span data-ttu-id="da054-642">メソッド leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="da054-642">Method leftMarginAnFrame</span></span>

```xpp
public int leftMarginAnFrame()
```

### <a name="return-value---leftmarginanframe"></a><span data-ttu-id="da054-643">戻り値 - leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="da054-643">Return Value - leftMarginAnFrame</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="da054-644">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="da054-644">Method leftMarginMode</span></span>

```xpp
public int leftMarginMode([int value])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="da054-645">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="da054-645">Parameters - leftMarginMode</span></span>

<span data-ttu-id="da054-646">値</span><span class="sxs-lookup"><span data-stu-id="da054-646">value</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="da054-647">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="da054-647">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginstr"></a><span data-ttu-id="da054-648">メソッド leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="da054-648">Method leftMarginStr</span></span>

```xpp
public str leftMarginStr([str value])
```

### <a name="parameters---leftmarginstr"></a><span data-ttu-id="da054-649">パラメーター - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="da054-649">Parameters - leftMarginStr</span></span>

<span data-ttu-id="da054-650">値</span><span class="sxs-lookup"><span data-stu-id="da054-650">value</span></span>  

### <a name="return-value---leftmarginstr"></a><span data-ttu-id="da054-651">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="da054-651">Return Value - leftMarginStr</span></span>

## <a name="method-leftmarginunit"></a><span data-ttu-id="da054-652">メソッド leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="da054-652">Method leftMarginUnit</span></span>

```xpp
public Units leftMarginUnit([Units value])
```

### <a name="parameters---leftmarginunit"></a><span data-ttu-id="da054-653">パラメーター - leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="da054-653">Parameters - leftMarginUnit</span></span>

<span data-ttu-id="da054-654">値</span><span class="sxs-lookup"><span data-stu-id="da054-654">value</span></span>  

### <a name="return-value---leftmarginunit"></a><span data-ttu-id="da054-655">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="da054-655">Return Value - leftMarginUnit</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="da054-656">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="da054-656">Method leftMarginValue</span></span>

```xpp
public Real leftMarginValue([Real value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="da054-657">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="da054-657">Parameters - leftMarginValue</span></span>

<span data-ttu-id="da054-658">値</span><span class="sxs-lookup"><span data-stu-id="da054-658">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="da054-659">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="da054-659">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="da054-660">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="da054-660">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="da054-661">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="da054-661">Parameters - leftMode</span></span>

<span data-ttu-id="da054-662">値</span><span class="sxs-lookup"><span data-stu-id="da054-662">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="da054-663">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="da054-663">Return Value - leftMode</span></span>

## <a name="method-leftstr"></a><span data-ttu-id="da054-664">メソッド leftStr</span><span class="sxs-lookup"><span data-stu-id="da054-664">Method leftStr</span></span>

```xpp
public str leftStr([str value])
```

### <a name="parameters---leftstr"></a><span data-ttu-id="da054-665">パラメーター - leftStr</span><span class="sxs-lookup"><span data-stu-id="da054-665">Parameters - leftStr</span></span>

<span data-ttu-id="da054-666">値</span><span class="sxs-lookup"><span data-stu-id="da054-666">value</span></span>  

### <a name="return-value---leftstr"></a><span data-ttu-id="da054-667">戻り値 - leftStr</span><span class="sxs-lookup"><span data-stu-id="da054-667">Return Value - leftStr</span></span>

## <a name="method-leftunit"></a><span data-ttu-id="da054-668">メソッド leftUnit</span><span class="sxs-lookup"><span data-stu-id="da054-668">Method leftUnit</span></span>

```xpp
public Units leftUnit([Units value])
```

### <a name="parameters---leftunit"></a><span data-ttu-id="da054-669">パラメーター - leftUnit</span><span class="sxs-lookup"><span data-stu-id="da054-669">Parameters - leftUnit</span></span>

<span data-ttu-id="da054-670">値</span><span class="sxs-lookup"><span data-stu-id="da054-670">value</span></span>  

### <a name="return-value---leftunit"></a><span data-ttu-id="da054-671">戻り値 - leftUnit</span><span class="sxs-lookup"><span data-stu-id="da054-671">Return Value - leftUnit</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="da054-672">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="da054-672">Method leftValue</span></span>

```xpp
public Real leftValue([Real value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="da054-673">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="da054-673">Parameters - leftValue</span></span>

<span data-ttu-id="da054-674">値</span><span class="sxs-lookup"><span data-stu-id="da054-674">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="da054-675">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="da054-675">Return Value - leftValue</span></span>

## <a name="method-lineabove"></a><span data-ttu-id="da054-676">メソッド lineAbove</span><span class="sxs-lookup"><span data-stu-id="da054-676">Method lineAbove</span></span>

```xpp
public LineType lineAbove([LineType value])
```

### <a name="parameters---lineabove"></a><span data-ttu-id="da054-677">パラメーター - lineAbove</span><span class="sxs-lookup"><span data-stu-id="da054-677">Parameters - lineAbove</span></span>

<span data-ttu-id="da054-678">値</span><span class="sxs-lookup"><span data-stu-id="da054-678">value</span></span>  

### <a name="return-value---lineabove"></a><span data-ttu-id="da054-679">戻り値 - lineAbove</span><span class="sxs-lookup"><span data-stu-id="da054-679">Return Value - lineAbove</span></span>

## <a name="method-linebelow"></a><span data-ttu-id="da054-680">メソッド lineBelow</span><span class="sxs-lookup"><span data-stu-id="da054-680">Method lineBelow</span></span>

```xpp
public LineType lineBelow([LineType value])
```

### <a name="parameters---linebelow"></a><span data-ttu-id="da054-681">パラメーター - lineBelow</span><span class="sxs-lookup"><span data-stu-id="da054-681">Parameters - lineBelow</span></span>

<span data-ttu-id="da054-682">値</span><span class="sxs-lookup"><span data-stu-id="da054-682">value</span></span>  

### <a name="return-value---linebelow"></a><span data-ttu-id="da054-683">戻り値 - lineBelow</span><span class="sxs-lookup"><span data-stu-id="da054-683">Return Value - lineBelow</span></span>

## <a name="method-lineleft"></a><span data-ttu-id="da054-684">メソッド lineLeft</span><span class="sxs-lookup"><span data-stu-id="da054-684">Method lineLeft</span></span>

<span data-ttu-id="da054-685">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-685">Gets or sets the type of line that is used as the left border of a section.</span></span>

```xpp
public LineType lineLeft([LineType value])
```

### <a name="parameters---lineleft"></a><span data-ttu-id="da054-686">パラメーター - lineLeft</span><span class="sxs-lookup"><span data-stu-id="da054-686">Parameters - lineLeft</span></span>

<span data-ttu-id="da054-687">値</span><span class="sxs-lookup"><span data-stu-id="da054-687">value</span></span>  

### <a name="return-value---lineleft"></a><span data-ttu-id="da054-688">戻り値 - lineLeft</span><span class="sxs-lookup"><span data-stu-id="da054-688">Return Value - lineLeft</span></span>

<span data-ttu-id="da054-689">左境界線として使用される線のタイプ。</span><span class="sxs-lookup"><span data-stu-id="da054-689">The type of line that is used as the left border.</span></span>

## <a name="method-lineright"></a><span data-ttu-id="da054-690">メソッド lineRight</span><span class="sxs-lookup"><span data-stu-id="da054-690">Method lineRight</span></span>

```xpp
public LineType lineRight([LineType value])
```

### <a name="parameters---lineright"></a><span data-ttu-id="da054-691">パラメーター - lineRight</span><span class="sxs-lookup"><span data-stu-id="da054-691">Parameters - lineRight</span></span>

<span data-ttu-id="da054-692">値</span><span class="sxs-lookup"><span data-stu-id="da054-692">value</span></span>  

### <a name="return-value---lineright"></a><span data-ttu-id="da054-693">戻り値 - lineRight</span><span class="sxs-lookup"><span data-stu-id="da054-693">Return Value - lineRight</span></span>

## <a name="method-menuitemlabel"></a><span data-ttu-id="da054-694">メソッド menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="da054-694">Method menuItemLabel</span></span>

```xpp
public str menuItemLabel([str value])
```

### <a name="parameters---menuitemlabel"></a><span data-ttu-id="da054-695">パラメーター - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="da054-695">Parameters - menuItemLabel</span></span>

<span data-ttu-id="da054-696">値</span><span class="sxs-lookup"><span data-stu-id="da054-696">value</span></span>  

### <a name="return-value---menuitemlabel"></a><span data-ttu-id="da054-697">戻り値 - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="da054-697">Return Value - menuItemLabel</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="da054-698">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="da054-698">Method menuItemName</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="da054-699">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="da054-699">Parameters - menuItemName</span></span>

<span data-ttu-id="da054-700">値</span><span class="sxs-lookup"><span data-stu-id="da054-700">value</span></span>  

### <a name="return-value---menuitemname"></a><span data-ttu-id="da054-701">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="da054-701">Return Value - menuItemName</span></span>

## <a name="method-menuitemtype"></a><span data-ttu-id="da054-702">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="da054-702">Method menuItemType</span></span>

```xpp
public MenuItemType menuItemType([MenuItemType value])
```

### <a name="parameters---menuitemtype"></a><span data-ttu-id="da054-703">パラメーター - menuItemType</span><span class="sxs-lookup"><span data-stu-id="da054-703">Parameters - menuItemType</span></span>

<span data-ttu-id="da054-704">値</span><span class="sxs-lookup"><span data-stu-id="da054-704">value</span></span>  

### <a name="return-value---menuitemtype"></a><span data-ttu-id="da054-705">戻り値 - menuItemType</span><span class="sxs-lookup"><span data-stu-id="da054-705">Return Value - menuItemType</span></span>

## <a name="method-modelfieldname"></a><span data-ttu-id="da054-706">メソッド modelFieldName</span><span class="sxs-lookup"><span data-stu-id="da054-706">Method modelFieldName</span></span>

```xpp
public str modelFieldName([str value])
```

### <a name="parameters---modelfieldname"></a><span data-ttu-id="da054-707">パラメーター - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="da054-707">Parameters - modelFieldName</span></span>

<span data-ttu-id="da054-708">値</span><span class="sxs-lookup"><span data-stu-id="da054-708">value</span></span>  

### <a name="return-value---modelfieldname"></a><span data-ttu-id="da054-709">戻り値 - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="da054-709">Return Value - modelFieldName</span></span>

## <a name="method-name"></a><span data-ttu-id="da054-710">メソッド名</span><span class="sxs-lookup"><span data-stu-id="da054-710">Method name</span></span>

<span data-ttu-id="da054-711">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-711">Gets or sets the name that used in the code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="da054-712">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="da054-712">Parameters - name</span></span>

<span data-ttu-id="da054-713">値</span><span class="sxs-lookup"><span data-stu-id="da054-713">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="da054-714">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="da054-714">Return Value - name</span></span>

<span data-ttu-id="da054-715">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="da054-715">The name that is used in the code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="da054-716">備考 - name</span><span class="sxs-lookup"><span data-stu-id="da054-716">Remarks - name</span></span>

<span data-ttu-id="da054-717">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="da054-717">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="da054-718">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="da054-718">Begins with a letter.</span></span>
-   <span data-ttu-id="da054-719">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="da054-719">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="da054-720">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="da054-720">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="da054-721">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="da054-721">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="da054-722">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="da054-722">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-numberoflines"></a><span data-ttu-id="da054-723">メソッド numberOfLines</span><span class="sxs-lookup"><span data-stu-id="da054-723">Method numberOfLines</span></span>

```xpp
public int numberOfLines(int height100mm)
```

### <a name="parameters---numberoflines"></a><span data-ttu-id="da054-724">パラメーター - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="da054-724">Parameters - numberOfLines</span></span>

<span data-ttu-id="da054-725">height100mm</span><span class="sxs-lookup"><span data-stu-id="da054-725">height100mm</span></span>  

### <a name="return-value---numberoflines"></a><span data-ttu-id="da054-726">戻り値 - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="da054-726">Return Value - numberOfLines</span></span>

## <a name="method-position"></a><span data-ttu-id="da054-727">メソッドの位置</span><span class="sxs-lookup"><span data-stu-id="da054-727">Method position</span></span>

```xpp
public int position([int value])
```

### <a name="parameters---position"></a><span data-ttu-id="da054-728">パラメーター - position</span><span class="sxs-lookup"><span data-stu-id="da054-728">Parameters - position</span></span>

<span data-ttu-id="da054-729">値</span><span class="sxs-lookup"><span data-stu-id="da054-729">value</span></span>  

### <a name="return-value---position"></a><span data-ttu-id="da054-730">戻り値 - position</span><span class="sxs-lookup"><span data-stu-id="da054-730">Return Value - position</span></span>

## <a name="method-previewinfo"></a><span data-ttu-id="da054-731">メソッド previewInfo</span><span class="sxs-lookup"><span data-stu-id="da054-731">Method previewInfo</span></span>

```xpp
public str previewInfo(str string)
```

### <a name="parameters---previewinfo"></a><span data-ttu-id="da054-732">パラメーター - previewInfo</span><span class="sxs-lookup"><span data-stu-id="da054-732">Parameters - previewInfo</span></span>

<span data-ttu-id="da054-733">文字列</span><span class="sxs-lookup"><span data-stu-id="da054-733">string</span></span>  

### <a name="return-value---previewinfo"></a><span data-ttu-id="da054-734">戻り値 - previewInfo</span><span class="sxs-lookup"><span data-stu-id="da054-734">Return Value - previewInfo</span></span>

## <a name="method-previewxcompensation100mm"></a><span data-ttu-id="da054-735">メソッド previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="da054-735">Method previewXCompensation100mm</span></span>

```xpp
public int previewXCompensation100mm(str string)
```

### <a name="parameters---previewxcompensation100mm"></a><span data-ttu-id="da054-736">パラメーター - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="da054-736">Parameters - previewXCompensation100mm</span></span>

<span data-ttu-id="da054-737">文字列</span><span class="sxs-lookup"><span data-stu-id="da054-737">string</span></span>  

### <a name="return-value---previewxcompensation100mm"></a><span data-ttu-id="da054-738">戻り値 - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="da054-738">Return Value - previewXCompensation100mm</span></span>

## <a name="method-right100mm"></a><span data-ttu-id="da054-739">メソッド right100mm</span><span class="sxs-lookup"><span data-stu-id="da054-739">Method right100mm</span></span>

```xpp
public int right100mm()
```

### <a name="return-value---right100mm"></a><span data-ttu-id="da054-740">戻り値 - right100mm</span><span class="sxs-lookup"><span data-stu-id="da054-740">Return Value - right100mm</span></span>

## <a name="method-right100mminclborder"></a><span data-ttu-id="da054-741">メソッド right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="da054-741">Method right100mmInclBorder</span></span>

```xpp
public int right100mmInclBorder()
```

### <a name="return-value---right100mminclborder"></a><span data-ttu-id="da054-742">戻り値 - right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="da054-742">Return Value - right100mmInclBorder</span></span>

## <a name="method-rightmarginandframe"></a><span data-ttu-id="da054-743">メソッド rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="da054-743">Method rightMarginAndFrame</span></span>

```xpp
public int rightMarginAndFrame()
```

### <a name="return-value---rightmarginandframe"></a><span data-ttu-id="da054-744">戻り値 - rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="da054-744">Return Value - rightMarginAndFrame</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="da054-745">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="da054-745">Method rightMarginMode</span></span>

```xpp
public int rightMarginMode([int value])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="da054-746">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="da054-746">Parameters - rightMarginMode</span></span>

<span data-ttu-id="da054-747">値</span><span class="sxs-lookup"><span data-stu-id="da054-747">value</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="da054-748">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="da054-748">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginstr"></a><span data-ttu-id="da054-749">メソッド rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="da054-749">Method rightMarginStr</span></span>

```xpp
public str rightMarginStr([str value])
```

### <a name="parameters---rightmarginstr"></a><span data-ttu-id="da054-750">パラメーター - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="da054-750">Parameters - rightMarginStr</span></span>

<span data-ttu-id="da054-751">値</span><span class="sxs-lookup"><span data-stu-id="da054-751">value</span></span>  

### <a name="return-value---rightmarginstr"></a><span data-ttu-id="da054-752">戻り値 - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="da054-752">Return Value - rightMarginStr</span></span>

## <a name="method-rightmarginunit"></a><span data-ttu-id="da054-753">メソッド rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="da054-753">Method rightMarginUnit</span></span>

```xpp
public Units rightMarginUnit([Units value])
```

### <a name="parameters---rightmarginunit"></a><span data-ttu-id="da054-754">パラメーター - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="da054-754">Parameters - rightMarginUnit</span></span>

<span data-ttu-id="da054-755">値</span><span class="sxs-lookup"><span data-stu-id="da054-755">value</span></span>  

### <a name="return-value---rightmarginunit"></a><span data-ttu-id="da054-756">戻り値 - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="da054-756">Return Value - rightMarginUnit</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="da054-757">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="da054-757">Method rightMarginValue</span></span>

```xpp
public Real rightMarginValue([Real value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="da054-758">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="da054-758">Parameters - rightMarginValue</span></span>

<span data-ttu-id="da054-759">値</span><span class="sxs-lookup"><span data-stu-id="da054-759">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="da054-760">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="da054-760">Return Value - rightMarginValue</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="da054-761">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="da054-761">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="da054-762">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="da054-762">Parameters - securityKey</span></span>

<span data-ttu-id="da054-763">値</span><span class="sxs-lookup"><span data-stu-id="da054-763">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="da054-764">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="da054-764">Return Value - securityKey</span></span>

## <a name="method-setheightgettext"></a><span data-ttu-id="da054-765">メソッド setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="da054-765">Method setHeightGetText</span></span>

```xpp
public str setHeightGetText(int lines, str string)
```

### <a name="parameters---setheightgettext"></a><span data-ttu-id="da054-766">パラメーター - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="da054-766">Parameters - setHeightGetText</span></span>

<span data-ttu-id="da054-767">明細行</span><span class="sxs-lookup"><span data-stu-id="da054-767">lines</span></span>  

<!-- -->

<span data-ttu-id="da054-768">文字列</span><span class="sxs-lookup"><span data-stu-id="da054-768">string</span></span>  

### <a name="return-value---setheightgettext"></a><span data-ttu-id="da054-769">戻り値 - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="da054-769">Return Value - setHeightGetText</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="da054-770">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="da054-770">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="da054-771">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="da054-771">Parameters - showLabel</span></span>

<span data-ttu-id="da054-772">値</span><span class="sxs-lookup"><span data-stu-id="da054-772">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="da054-773">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="da054-773">Return Value - showLabel</span></span>

## <a name="method-table"></a><span data-ttu-id="da054-774">メソッド table</span><span class="sxs-lookup"><span data-stu-id="da054-774">Method table</span></span>

<span data-ttu-id="da054-775">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-775">Gets or sets the table ID associated with the object.</span></span>

```xpp
public TableId table([TableId value])
```

### <a name="parameters---table"></a><span data-ttu-id="da054-776">パラメーター - table</span><span class="sxs-lookup"><span data-stu-id="da054-776">Parameters - table</span></span>

<span data-ttu-id="da054-777">値</span><span class="sxs-lookup"><span data-stu-id="da054-777">value</span></span>  

### <a name="return-value---table"></a><span data-ttu-id="da054-778">戻り値 - toBlob</span><span class="sxs-lookup"><span data-stu-id="da054-778">Return Value - table</span></span>

<span data-ttu-id="da054-779">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="da054-779">The current value of the table ID associated with the object.</span></span>

## <a name="method-thickness"></a><span data-ttu-id="da054-780">メソッド thickness</span><span class="sxs-lookup"><span data-stu-id="da054-780">Method thickness</span></span>

```xpp
public LineThickness thickness([LineThickness value])
```

### <a name="parameters---thickness"></a><span data-ttu-id="da054-781">パラメーター - thickness</span><span class="sxs-lookup"><span data-stu-id="da054-781">Parameters - thickness</span></span>

<span data-ttu-id="da054-782">値</span><span class="sxs-lookup"><span data-stu-id="da054-782">value</span></span>  

### <a name="return-value---thickness"></a><span data-ttu-id="da054-783">戻り値 - thickness</span><span class="sxs-lookup"><span data-stu-id="da054-783">Return Value - thickness</span></span>

## <a name="method-top100mm"></a><span data-ttu-id="da054-784">メソッド top100mm</span><span class="sxs-lookup"><span data-stu-id="da054-784">Method top100mm</span></span>

```xpp
public int top100mm([int topExclBorder])
```

### <a name="parameters---top100mm"></a><span data-ttu-id="da054-785">パラメーター - top100mm</span><span class="sxs-lookup"><span data-stu-id="da054-785">Parameters - top100mm</span></span>

<span data-ttu-id="da054-786">topExclBorder</span><span class="sxs-lookup"><span data-stu-id="da054-786">topExclBorder</span></span>  

### <a name="return-value---top100mm"></a><span data-ttu-id="da054-787">戻り値 - top100mm</span><span class="sxs-lookup"><span data-stu-id="da054-787">Return Value - top100mm</span></span>

## <a name="method-top100mminclborder"></a><span data-ttu-id="da054-788">メソッド top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="da054-788">Method top100mmInclBorder</span></span>

```xpp
public int top100mmInclBorder([int topInclBorder])
```

### <a name="parameters---top100mminclborder"></a><span data-ttu-id="da054-789">パラメーター - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="da054-789">Parameters - top100mmInclBorder</span></span>

<span data-ttu-id="da054-790">topInclBorder</span><span class="sxs-lookup"><span data-stu-id="da054-790">topInclBorder</span></span>  

### <a name="return-value---top100mminclborder"></a><span data-ttu-id="da054-791">戻り値 - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="da054-791">Return Value - top100mmInclBorder</span></span>

## <a name="method-topmarginandframe"></a><span data-ttu-id="da054-792">メソッド topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="da054-792">Method topMarginAndFrame</span></span>

```xpp
public int topMarginAndFrame()
```

### <a name="return-value---topmarginandframe"></a><span data-ttu-id="da054-793">戻り値 - topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="da054-793">Return Value - topMarginAndFrame</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="da054-794">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="da054-794">Method topMarginMode</span></span>

```xpp
public int topMarginMode([int value])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="da054-795">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="da054-795">Parameters - topMarginMode</span></span>

<span data-ttu-id="da054-796">値</span><span class="sxs-lookup"><span data-stu-id="da054-796">value</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="da054-797">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="da054-797">Return Value - topMarginMode</span></span>

## <a name="method-topmarginstr"></a><span data-ttu-id="da054-798">メソッド topMarginStr</span><span class="sxs-lookup"><span data-stu-id="da054-798">Method topMarginStr</span></span>

```xpp
public str topMarginStr([str value])
```

### <a name="parameters---topmarginstr"></a><span data-ttu-id="da054-799">パラメーター - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="da054-799">Parameters - topMarginStr</span></span>

<span data-ttu-id="da054-800">値</span><span class="sxs-lookup"><span data-stu-id="da054-800">value</span></span>  

### <a name="return-value---topmarginstr"></a><span data-ttu-id="da054-801">戻り値 - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="da054-801">Return Value - topMarginStr</span></span>

## <a name="method-topmarginunit"></a><span data-ttu-id="da054-802">メソッド topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="da054-802">Method topMarginUnit</span></span>

```xpp
public Units topMarginUnit([Units value])
```

### <a name="parameters---topmarginunit"></a><span data-ttu-id="da054-803">パラメーター - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="da054-803">Parameters - topMarginUnit</span></span>

<span data-ttu-id="da054-804">値</span><span class="sxs-lookup"><span data-stu-id="da054-804">value</span></span>  

### <a name="return-value---topmarginunit"></a><span data-ttu-id="da054-805">戻り値 - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="da054-805">Return Value - topMarginUnit</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="da054-806">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="da054-806">Method topMarginValue</span></span>

```xpp
public Real topMarginValue([Real value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="da054-807">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="da054-807">Parameters - topMarginValue</span></span>

<span data-ttu-id="da054-808">値</span><span class="sxs-lookup"><span data-stu-id="da054-808">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="da054-809">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="da054-809">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="da054-810">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="da054-810">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="da054-811">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="da054-811">Parameters - topMode</span></span>

<span data-ttu-id="da054-812">値</span><span class="sxs-lookup"><span data-stu-id="da054-812">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="da054-813">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="da054-813">Return Value - topMode</span></span>

## <a name="method-topstr"></a><span data-ttu-id="da054-814">メソッド topStr</span><span class="sxs-lookup"><span data-stu-id="da054-814">Method topStr</span></span>

```xpp
public str topStr([str value])
```

### <a name="parameters---topstr"></a><span data-ttu-id="da054-815">パラメーター - topStr</span><span class="sxs-lookup"><span data-stu-id="da054-815">Parameters - topStr</span></span>

<span data-ttu-id="da054-816">値</span><span class="sxs-lookup"><span data-stu-id="da054-816">value</span></span>  

### <a name="return-value---topstr"></a><span data-ttu-id="da054-817">戻り値 - topStr</span><span class="sxs-lookup"><span data-stu-id="da054-817">Return Value - topStr</span></span>

## <a name="method-topunit"></a><span data-ttu-id="da054-818">メソッド topUnit</span><span class="sxs-lookup"><span data-stu-id="da054-818">Method topUnit</span></span>

```xpp
public Units topUnit([Units value])
```

### <a name="parameters---topunit"></a><span data-ttu-id="da054-819">パラメーター - topUnit</span><span class="sxs-lookup"><span data-stu-id="da054-819">Parameters - topUnit</span></span>

<span data-ttu-id="da054-820">値</span><span class="sxs-lookup"><span data-stu-id="da054-820">value</span></span>  

### <a name="return-value---topunit"></a><span data-ttu-id="da054-821">戻り値 - topUnit</span><span class="sxs-lookup"><span data-stu-id="da054-821">Return Value - topUnit</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="da054-822">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="da054-822">Method topValue</span></span>

```xpp
public Real topValue([Real value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="da054-823">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="da054-823">Parameters - topValue</span></span>

<span data-ttu-id="da054-824">値</span><span class="sxs-lookup"><span data-stu-id="da054-824">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="da054-825">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="da054-825">Return Value - topValue</span></span>

## <a name="method-underline"></a><span data-ttu-id="da054-826">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="da054-826">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="da054-827">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="da054-827">Parameters - underline</span></span>

<span data-ttu-id="da054-828">値</span><span class="sxs-lookup"><span data-stu-id="da054-828">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="da054-829">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="da054-829">Return Value - underline</span></span>

## <a name="method-visible"></a><span data-ttu-id="da054-830">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="da054-830">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="da054-831">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="da054-831">Parameters - visible</span></span>

<span data-ttu-id="da054-832">値</span><span class="sxs-lookup"><span data-stu-id="da054-832">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="da054-833">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="da054-833">Return Value - visible</span></span>

## <a name="method-webmenuitemname"></a><span data-ttu-id="da054-834">メソッド webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="da054-834">Method webMenuItemName</span></span>

```xpp
public str webMenuItemName([str value])
```

### <a name="parameters---webmenuitemname"></a><span data-ttu-id="da054-835">パラメーター - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="da054-835">Parameters - webMenuItemName</span></span>

<span data-ttu-id="da054-836">値</span><span class="sxs-lookup"><span data-stu-id="da054-836">value</span></span>  

### <a name="return-value---webmenuitemname"></a><span data-ttu-id="da054-837">戻り値 - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="da054-837">Return Value - webMenuItemName</span></span>

## <a name="method-webmenuitemtype"></a><span data-ttu-id="da054-838">メソッド webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="da054-838">Method webMenuItemType</span></span>

```xpp
public WebMenuItemType webMenuItemType([WebMenuItemType value])
```

### <a name="parameters---webmenuitemtype"></a><span data-ttu-id="da054-839">パラメーター - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="da054-839">Parameters - webMenuItemType</span></span>

<span data-ttu-id="da054-840">値</span><span class="sxs-lookup"><span data-stu-id="da054-840">value</span></span>  

### <a name="return-value---webmenuitemtype"></a><span data-ttu-id="da054-841">戻り値 - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="da054-841">Return Value - webMenuItemType</span></span>

## <a name="method-webtarget"></a><span data-ttu-id="da054-842">メソッド webTarget</span><span class="sxs-lookup"><span data-stu-id="da054-842">Method webTarget</span></span>

```xpp
public str webTarget([str value])
```

### <a name="parameters---webtarget"></a><span data-ttu-id="da054-843">パラメーター - webTarget</span><span class="sxs-lookup"><span data-stu-id="da054-843">Parameters - webTarget</span></span>

<span data-ttu-id="da054-844">値</span><span class="sxs-lookup"><span data-stu-id="da054-844">value</span></span>  

### <a name="return-value---webtarget"></a><span data-ttu-id="da054-845">戻り値 - webTarget</span><span class="sxs-lookup"><span data-stu-id="da054-845">Return Value - webTarget</span></span>

## <a name="method-width100mm"></a><span data-ttu-id="da054-846">メソッド width100mm</span><span class="sxs-lookup"><span data-stu-id="da054-846">Method width100mm</span></span>

```xpp
public int width100mm([int widthExclBorder])
```

### <a name="parameters---width100mm"></a><span data-ttu-id="da054-847">パラメーター - width100mm</span><span class="sxs-lookup"><span data-stu-id="da054-847">Parameters - width100mm</span></span>

<span data-ttu-id="da054-848">widthExclBorder</span><span class="sxs-lookup"><span data-stu-id="da054-848">widthExclBorder</span></span>  

### <a name="return-value---width100mm"></a><span data-ttu-id="da054-849">戻り値 - width100mm</span><span class="sxs-lookup"><span data-stu-id="da054-849">Return Value - width100mm</span></span>

## <a name="method-width100mminclborder"></a><span data-ttu-id="da054-850">メソッド width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="da054-850">Method width100mmInclBorder</span></span>

```xpp
public int width100mmInclBorder([int widthInclBorder])
```

### <a name="parameters---width100mminclborder"></a><span data-ttu-id="da054-851">パラメーター - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="da054-851">Parameters - width100mmInclBorder</span></span>

<span data-ttu-id="da054-852">widthInclBorder</span><span class="sxs-lookup"><span data-stu-id="da054-852">widthInclBorder</span></span>  

### <a name="return-value---width100mminclborder"></a><span data-ttu-id="da054-853">戻り値 - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="da054-853">Return Value - width100mmInclBorder</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="da054-854">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="da054-854">Method widthMode</span></span>

<span data-ttu-id="da054-855">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-855">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="da054-856">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="da054-856">Parameters - widthMode</span></span>

<span data-ttu-id="da054-857">値</span><span class="sxs-lookup"><span data-stu-id="da054-857">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="da054-858">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="da054-858">Return Value - widthMode</span></span>

<span data-ttu-id="da054-859">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="da054-859">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="da054-860">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="da054-860">Remarks - widthMode</span></span>

<span data-ttu-id="da054-861">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="da054-861">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="da054-862">モード。</span><span class="sxs-lookup"><span data-stu-id="da054-862">Mode.</span></span>         | <span data-ttu-id="da054-863">幅計算。</span><span class="sxs-lookup"><span data-stu-id="da054-863">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="da054-864">正確。</span><span class="sxs-lookup"><span data-stu-id="da054-864">Exact.</span></span>        | <span data-ttu-id="da054-865">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="da054-865">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="da054-866">自動。</span><span class="sxs-lookup"><span data-stu-id="da054-866">Auto.</span></span>         | <span data-ttu-id="da054-867">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="da054-867">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="da054-868">列の幅。</span><span class="sxs-lookup"><span data-stu-id="da054-868">Column width.</span></span> | <span data-ttu-id="da054-869">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="da054-869">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="da054-870">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="da054-870">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthofstring100mm"></a><span data-ttu-id="da054-871">メソッド widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="da054-871">Method widthOfString100mm</span></span>

```xpp
public int widthOfString100mm(str string)
```

### <a name="parameters---widthofstring100mm"></a><span data-ttu-id="da054-872">パラメーター - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="da054-872">Parameters - widthOfString100mm</span></span>

<span data-ttu-id="da054-873">文字列</span><span class="sxs-lookup"><span data-stu-id="da054-873">string</span></span>  

### <a name="return-value---widthofstring100mm"></a><span data-ttu-id="da054-874">戻り値 - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="da054-874">Return Value - widthOfString100mm</span></span>

## <a name="method-widthstr"></a><span data-ttu-id="da054-875">メソッド widthStr</span><span class="sxs-lookup"><span data-stu-id="da054-875">Method widthStr</span></span>

```xpp
public str widthStr([str value])
```

### <a name="parameters---widthstr"></a><span data-ttu-id="da054-876">パラメーター - widthStr</span><span class="sxs-lookup"><span data-stu-id="da054-876">Parameters - widthStr</span></span>

<span data-ttu-id="da054-877">値</span><span class="sxs-lookup"><span data-stu-id="da054-877">value</span></span>  

### <a name="return-value---widthstr"></a><span data-ttu-id="da054-878">戻り値 - widthStr</span><span class="sxs-lookup"><span data-stu-id="da054-878">Return Value - widthStr</span></span>

## <a name="method-widthunit"></a><span data-ttu-id="da054-879">メソッド widthUnit</span><span class="sxs-lookup"><span data-stu-id="da054-879">Method widthUnit</span></span>

```xpp
public Units widthUnit([Units value])
```

### <a name="parameters---widthunit"></a><span data-ttu-id="da054-880">パラメーター - widthUnit</span><span class="sxs-lookup"><span data-stu-id="da054-880">Parameters - widthUnit</span></span>

<span data-ttu-id="da054-881">値</span><span class="sxs-lookup"><span data-stu-id="da054-881">value</span></span>  

### <a name="return-value---widthunit"></a><span data-ttu-id="da054-882">戻り値 - widthUnit</span><span class="sxs-lookup"><span data-stu-id="da054-882">Return Value - widthUnit</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="da054-883">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="da054-883">Method widthValue</span></span>

<span data-ttu-id="da054-884">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-884">Gets or sets the width of the control.</span></span>

```xpp
public Real widthValue([Real value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="da054-885">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="da054-885">Parameters - widthValue</span></span>

<span data-ttu-id="da054-886">値</span><span class="sxs-lookup"><span data-stu-id="da054-886">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="da054-887">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="da054-887">Return Value - widthValue</span></span>

<span data-ttu-id="da054-888">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="da054-888">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="da054-889">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="da054-889">Remarks - widthValue</span></span>

<span data-ttu-id="da054-890">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="da054-890">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-height"></a><span data-ttu-id="da054-891">メソッド height</span><span class="sxs-lookup"><span data-stu-id="da054-891">Method height</span></span>

<span data-ttu-id="da054-892">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-892">Gets or sets the height of the control.</span></span>

```xpp
public void height(Real value, Units unit)
```

### <a name="parameters---height"></a><span data-ttu-id="da054-893">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="da054-893">Parameters - height</span></span>

<span data-ttu-id="da054-894">値</span><span class="sxs-lookup"><span data-stu-id="da054-894">value</span></span>  

<!-- -->

<span data-ttu-id="da054-895">単位</span><span class="sxs-lookup"><span data-stu-id="da054-895">unit</span></span>  

### <a name="remarks---height"></a><span data-ttu-id="da054-896">備考 - height</span><span class="sxs-lookup"><span data-stu-id="da054-896">Remarks - height</span></span>

<span data-ttu-id="da054-897">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="da054-897">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="da054-898">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="da054-898">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="da054-899">モード。</span><span class="sxs-lookup"><span data-stu-id="da054-899">Mode.</span></span>            | <span data-ttu-id="da054-900">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="da054-900">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="da054-901">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="da054-901">-1 Exact.</span></span>        | <span data-ttu-id="da054-902">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="da054-902">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="da054-903">0 自動。</span><span class="sxs-lookup"><span data-stu-id="da054-903">0 Auto.</span></span>          | <span data-ttu-id="da054-904">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="da054-904">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="da054-905">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="da054-905">1 Column height.</span></span> | <span data-ttu-id="da054-906">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="da054-906">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="da054-907">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="da054-907">The height and height calculation mode can be set separately.</span></span>

## <a name="method-left"></a><span data-ttu-id="da054-908">メソッド left</span><span class="sxs-lookup"><span data-stu-id="da054-908">Method left</span></span>

```xpp
public void left(Real value, Units unit)
```

### <a name="parameters---left"></a><span data-ttu-id="da054-909">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="da054-909">Parameters - left</span></span>

<span data-ttu-id="da054-910">値</span><span class="sxs-lookup"><span data-stu-id="da054-910">value</span></span>  

<!-- -->

<span data-ttu-id="da054-911">単位</span><span class="sxs-lookup"><span data-stu-id="da054-911">unit</span></span>  

## <a name="method-topmargin"></a><span data-ttu-id="da054-912">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="da054-912">Method topMargin</span></span>

```xpp
public void topMargin(Real value, Units unit)
```

### <a name="parameters---topmargin"></a><span data-ttu-id="da054-913">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="da054-913">Parameters - topMargin</span></span>

<span data-ttu-id="da054-914">値</span><span class="sxs-lookup"><span data-stu-id="da054-914">value</span></span>  

<!-- -->

<span data-ttu-id="da054-915">単位</span><span class="sxs-lookup"><span data-stu-id="da054-915">unit</span></span>  

## <a name="method-hide"></a><span data-ttu-id="da054-916">メソッド hide</span><span class="sxs-lookup"><span data-stu-id="da054-916">Method hide</span></span>

```xpp
public void hide()
```

## <a name="method-top"></a><span data-ttu-id="da054-917">メソッド top</span><span class="sxs-lookup"><span data-stu-id="da054-917">Method top</span></span>

```xpp
public void top(Real value, Units unit)
```

### <a name="parameters---top"></a><span data-ttu-id="da054-918">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="da054-918">Parameters - top</span></span>

<span data-ttu-id="da054-919">値</span><span class="sxs-lookup"><span data-stu-id="da054-919">value</span></span>  

<!-- -->

<span data-ttu-id="da054-920">単位</span><span class="sxs-lookup"><span data-stu-id="da054-920">unit</span></span>  

## <a name="method-bottommargin"></a><span data-ttu-id="da054-921">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="da054-921">Method bottomMargin</span></span>

```xpp
public void bottomMargin(Real value, Units unit)
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="da054-922">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="da054-922">Parameters - bottomMargin</span></span>

<span data-ttu-id="da054-923">値</span><span class="sxs-lookup"><span data-stu-id="da054-923">value</span></span>  

<!-- -->

<span data-ttu-id="da054-924">単位</span><span class="sxs-lookup"><span data-stu-id="da054-924">unit</span></span>  

## <a name="method-labelwidth"></a><span data-ttu-id="da054-925">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="da054-925">Method labelWidth</span></span>

```xpp
public void labelWidth(Real value, Units unit)
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="da054-926">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="da054-926">Parameters - labelWidth</span></span>

<span data-ttu-id="da054-927">値</span><span class="sxs-lookup"><span data-stu-id="da054-927">value</span></span>  

<!-- -->

<span data-ttu-id="da054-928">単位</span><span class="sxs-lookup"><span data-stu-id="da054-928">unit</span></span>  

## <a name="method-show"></a><span data-ttu-id="da054-929">メソッド show</span><span class="sxs-lookup"><span data-stu-id="da054-929">Method show</span></span>

```xpp
public void show()
```

## <a name="method-rightmargin"></a><span data-ttu-id="da054-930">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="da054-930">Method rightMargin</span></span>

```xpp
public void rightMargin(Real value, Units unit)
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="da054-931">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="da054-931">Parameters - rightMargin</span></span>

<span data-ttu-id="da054-932">値</span><span class="sxs-lookup"><span data-stu-id="da054-932">value</span></span>  

<!-- -->

<span data-ttu-id="da054-933">単位</span><span class="sxs-lookup"><span data-stu-id="da054-933">unit</span></span>  

## <a name="method-width"></a><span data-ttu-id="da054-934">メソッド width</span><span class="sxs-lookup"><span data-stu-id="da054-934">Method width</span></span>

<span data-ttu-id="da054-935">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="da054-935">Gets or sets the width of the control.</span></span>

```xpp
public void width(Real value, Units unit)
```

### <a name="parameters---width"></a><span data-ttu-id="da054-936">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="da054-936">Parameters - width</span></span>

<span data-ttu-id="da054-937">値</span><span class="sxs-lookup"><span data-stu-id="da054-937">value</span></span>  

<!-- -->

<span data-ttu-id="da054-938">単位</span><span class="sxs-lookup"><span data-stu-id="da054-938">unit</span></span>  

### <a name="remarks---width"></a><span data-ttu-id="da054-939">備考 - width</span><span class="sxs-lookup"><span data-stu-id="da054-939">Remarks - width</span></span>

<span data-ttu-id="da054-940">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="da054-940">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="da054-941">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="da054-941">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="da054-942">モード。</span><span class="sxs-lookup"><span data-stu-id="da054-942">Mode.</span></span>           | <span data-ttu-id="da054-943">幅計算。</span><span class="sxs-lookup"><span data-stu-id="da054-943">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="da054-944">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="da054-944">-1 Exact.</span></span>       | <span data-ttu-id="da054-945">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="da054-945">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="da054-946">0 自動。</span><span class="sxs-lookup"><span data-stu-id="da054-946">0 Auto.</span></span>         | <span data-ttu-id="da054-947">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="da054-947">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="da054-948">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="da054-948">1 Column width.</span></span> | <span data-ttu-id="da054-949">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="da054-949">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="da054-950">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="da054-950">The width and width calculation mode can be set separately.</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="da054-951">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="da054-951">Method leftMargin</span></span>

```xpp
public void leftMargin(Real value, Units unit)
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="da054-952">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="da054-952">Parameters - leftMargin</span></span>

<span data-ttu-id="da054-953">値</span><span class="sxs-lookup"><span data-stu-id="da054-953">value</span></span>  

<!-- -->

<span data-ttu-id="da054-954">単位</span><span class="sxs-lookup"><span data-stu-id="da054-954">unit</span></span>  

