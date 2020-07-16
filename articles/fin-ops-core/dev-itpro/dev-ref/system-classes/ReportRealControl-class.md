---
title: ReportRealControl クラス
description: このトピックでは、ReportRealControl クラスについて説明します。
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
ms.openlocfilehash: 234f81a8c4ce373582dd28ee133ccef09bd416f0
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502833"
---
# <a name="class-reportrealcontrol"></a><span data-ttu-id="7b424-103">クラス ReportRealControl</span><span class="sxs-lookup"><span data-stu-id="7b424-103">Class ReportRealControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ReportRealControl extends ReportControl
```

<span data-ttu-id="7b424-104">ReportRealControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7b424-104">The ReportRealControl class enables you to create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b424-105">備考</span><span class="sxs-lookup"><span data-stu-id="7b424-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="7b424-106">例</span><span class="sxs-lookup"><span data-stu-id="7b424-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="7b424-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="7b424-107">Methods</span></span>

| <span data-ttu-id="7b424-108">方法</span><span class="sxs-lookup"><span data-stu-id="7b424-108">Method</span></span>                                                                   | <span data-ttu-id="7b424-109">説明</span><span class="sxs-lookup"><span data-stu-id="7b424-109">Description</span></span>                                                                                                                                   |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b424-110">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-110">public int alignment(\[int value\])</span></span>                                      |                                                                                                                                               |
| <span data-ttu-id="7b424-111">public int allowNegative(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-111">public int allowNegative(\[int value\])</span></span>                                  |                                                                                                                                               |
| <span data-ttu-id="7b424-112">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-112">public int arrayIndex(\[int value\])</span></span>                                     |                                                                                                                                               |
| <span data-ttu-id="7b424-113">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-113">public boolean autoDeclaration(\[boolean value\])</span></span>                        | <span data-ttu-id="7b424-114">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-114">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                            |
| <span data-ttu-id="7b424-115">public int autoInsSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-115">public int autoInsSeparator(\[int value\])</span></span>                               |                                                                                                                                               |
| <span data-ttu-id="7b424-116">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-116">public int backgroundColor(\[int value\])</span></span>                                | <span data-ttu-id="7b424-117">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-117">Gets or sets the background color of the control.</span></span>                                                                                             |
| <span data-ttu-id="7b424-118">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-118">public int backStyle(\[int value\])</span></span>                                      | <span data-ttu-id="7b424-119">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-119">Determines whether the control background can be transparent.</span></span>                                                                                |
| <span data-ttu-id="7b424-120">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-120">public int bold(\[int value\])</span></span>                                           | <span data-ttu-id="7b424-121">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-121">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                                   |
| <span data-ttu-id="7b424-122">public int bottomMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="7b424-122">public int bottomMarginAndFrame()</span></span>                                        |                                                                                                                                               |
| <span data-ttu-id="7b424-123">public int bottomMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-123">public int bottomMarginMode(\[int value\])</span></span>                               |                                                                                                                                               |
| <span data-ttu-id="7b424-124">public str bottomMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-124">public str bottomMarginStr(\[str value\])</span></span>                                |                                                                                                                                               |
| <span data-ttu-id="7b424-125">public Units bottomMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-125">public Units bottomMarginUnit(\[Units value\])</span></span>                           |                                                                                                                                               |
| <span data-ttu-id="7b424-126">public Real bottomMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-126">public Real bottomMarginValue(\[Real value\])</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="7b424-127">public int changeLabelCase(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-127">public int changeLabelCase(\[int value\])</span></span>                                |                                                                                                                                               |
| <span data-ttu-id="7b424-128">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-128">public int characterSet(\[int value\])</span></span>                                   | <span data-ttu-id="7b424-129">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-129">Gets or sets the character set of the font.</span></span>                                                                                                   |
| <span data-ttu-id="7b424-130">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-130">public int colorScheme(\[int value\])</span></span>                                    | <span data-ttu-id="7b424-131">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-131">Gets or sets the color scheme of the control.</span></span>                                                                                                 |
| <span data-ttu-id="7b424-132">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-132">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="7b424-133">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-133">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                           |
| <span data-ttu-id="7b424-134">public ReportFieldType controlType()</span><span class="sxs-lookup"><span data-stu-id="7b424-134">public ReportFieldType controlType()</span></span>                                     |                                                                                                                                               |
| <span data-ttu-id="7b424-135">public str cssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-135">public str cssClass(\[str value\])</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="7b424-136">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-136">public FieldId dataField(\[FieldId value\])</span></span>                              |                                                                                                                                               |
| <span data-ttu-id="7b424-137">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-137">public str dataMethod(\[str value\])</span></span>                                     |                                                                                                                                               |
| <span data-ttu-id="7b424-138">public int decimalSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-138">public int decimalSeparator(\[int value\])</span></span>                               |                                                                                                                                               |
| <span data-ttu-id="7b424-139">public int delete()</span><span class="sxs-lookup"><span data-stu-id="7b424-139">public int delete()</span></span>                                                      |                                                                                                                                               |
| <span data-ttu-id="7b424-140">public int displaceNegative(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7b424-140">public int displaceNegative(\[int value\], \[AutoMode mode\])</span></span>            |                                                                                                                                               |
| <span data-ttu-id="7b424-141">public AutoMode displaceNegativeMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7b424-141">public AutoMode displaceNegativeMode(\[AutoMode mode\])</span></span>                  |                                                                                                                                               |
| <span data-ttu-id="7b424-142">public int displaceNegativeValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-142">public int displaceNegativeValue(\[int value\])</span></span>                          |                                                                                                                                               |
| <span data-ttu-id="7b424-143">public str effectiveFont()</span><span class="sxs-lookup"><span data-stu-id="7b424-143">public str effectiveFont()</span></span>                                               |                                                                                                                                               |
| <span data-ttu-id="7b424-144">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-144">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>         |                                                                                                                                               |
| <span data-ttu-id="7b424-145">public int extraSumWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-145">public int extraSumWidthMode(\[int value\])</span></span>                              |                                                                                                                                               |
| <span data-ttu-id="7b424-146">public str extraSumWidthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-146">public str extraSumWidthStr(\[str value\])</span></span>                               |                                                                                                                                               |
| <span data-ttu-id="7b424-147">public Units extraSumWidthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-147">public Units extraSumWidthUnit(\[Units value\])</span></span>                          |                                                                                                                                               |
| <span data-ttu-id="7b424-148">public Real extraSumWidthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-148">public Real extraSumWidthValue(\[Real value\])</span></span>                           |                                                                                                                                               |
| <span data-ttu-id="7b424-149">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-149">public str font(\[str value\])</span></span>                                           | <span data-ttu-id="7b424-150">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-150">Gets or sets the name of the font for the control to use.</span></span>                                                                                     |
| <span data-ttu-id="7b424-151">public str fontInfoPrinter()</span><span class="sxs-lookup"><span data-stu-id="7b424-151">public str fontInfoPrinter()</span></span>                                             |                                                                                                                                               |
| <span data-ttu-id="7b424-152">public int fontInfoPrinterAscent()</span><span class="sxs-lookup"><span data-stu-id="7b424-152">public int fontInfoPrinterAscent()</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="7b424-153">public int fontInfoPrinterDescent()</span><span class="sxs-lookup"><span data-stu-id="7b424-153">public int fontInfoPrinterDescent()</span></span>                                      |                                                                                                                                               |
| <span data-ttu-id="7b424-154">public int fontInfoPrinterExtLead()</span><span class="sxs-lookup"><span data-stu-id="7b424-154">public int fontInfoPrinterExtLead()</span></span>                                      |                                                                                                                                               |
| <span data-ttu-id="7b424-155">public int fontInfoPrinterHeight()</span><span class="sxs-lookup"><span data-stu-id="7b424-155">public int fontInfoPrinterHeight()</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="7b424-156">public int fontInfoPrinterIntLead()</span><span class="sxs-lookup"><span data-stu-id="7b424-156">public int fontInfoPrinterIntLead()</span></span>                                      |                                                                                                                                               |
| <span data-ttu-id="7b424-157">public str fontInfoScreen()</span><span class="sxs-lookup"><span data-stu-id="7b424-157">public str fontInfoScreen()</span></span>                                              |                                                                                                                                               |
| <span data-ttu-id="7b424-158">public int fontInfoScreenAscent()</span><span class="sxs-lookup"><span data-stu-id="7b424-158">public int fontInfoScreenAscent()</span></span>                                        |                                                                                                                                               |
| <span data-ttu-id="7b424-159">public int fontInfoScreenDescent()</span><span class="sxs-lookup"><span data-stu-id="7b424-159">public int fontInfoScreenDescent()</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="7b424-160">public int fontInfoScreenExtLead()</span><span class="sxs-lookup"><span data-stu-id="7b424-160">public int fontInfoScreenExtLead()</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="7b424-161">public int fontInfoScreenHeight()</span><span class="sxs-lookup"><span data-stu-id="7b424-161">public int fontInfoScreenHeight()</span></span>                                        |                                                                                                                                               |
| <span data-ttu-id="7b424-162">public int fontInfoScreenIntLead()</span><span class="sxs-lookup"><span data-stu-id="7b424-162">public int fontInfoScreenIntLead()</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="7b424-163">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-163">public int fontSize(\[int value\])</span></span>                                       | <span data-ttu-id="7b424-164">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-164">Gets or sets the size of the font for the control to use.</span></span>                                                                                     |
| <span data-ttu-id="7b424-165">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-165">public int foregroundColor(\[int value\])</span></span>                                | <span data-ttu-id="7b424-166">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-166">Gets or sets the text color for the control to use.</span></span>                                                                                           |
| <span data-ttu-id="7b424-167">public int formatMST(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-167">public int formatMST(\[int value\])</span></span>                                      |                                                                                                                                               |
| <span data-ttu-id="7b424-168">public int height100mm(\[int heightExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="7b424-168">public int height100mm(\[int heightExclBorder\])</span></span>                         |                                                                                                                                               |
| <span data-ttu-id="7b424-169">public int height100mmInclBorder(\[int heightInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="7b424-169">public int height100mmInclBorder(\[int heightInclBorder\])</span></span>               |                                                                                                                                               |
| <span data-ttu-id="7b424-170">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-170">public int heightMode(\[int value\])</span></span>                                     | <span data-ttu-id="7b424-171">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-171">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                |
| <span data-ttu-id="7b424-172">public int heightOfWordWrappedString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="7b424-172">public int heightOfWordWrappedString100mm(str string)</span></span>                    |                                                                                                                                               |
| <span data-ttu-id="7b424-173">public str heightStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-173">public str heightStr(\[str value\])</span></span>                                      |                                                                                                                                               |
| <span data-ttu-id="7b424-174">public Units heightUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-174">public Units heightUnit(\[Units value\])</span></span>                                 |                                                                                                                                               |
| <span data-ttu-id="7b424-175">public Real heightValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-175">public Real heightValue(\[Real value\])</span></span>                                  | <span data-ttu-id="7b424-176">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-176">Gets or sets the height of the control.</span></span>                                                                                                       |
| <span data-ttu-id="7b424-177">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-177">public boolean italic(\[boolean value\])</span></span>                                 |                                                                                                                                               |
| <span data-ttu-id="7b424-178">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-178">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="7b424-179">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-179">Gets or sets the label for a control.</span></span>                                                                                                         |
| <span data-ttu-id="7b424-180">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-180">public int labelBold(\[int value\])</span></span>                                      |                                                                                                                                               |
| <span data-ttu-id="7b424-181">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-181">public int labelCharacterSet(\[int value\])</span></span>                              |                                                                                                                                               |
| <span data-ttu-id="7b424-182">public str labelCssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-182">public str labelCssClass(\[str value\])</span></span>                                  |                                                                                                                                               |
| <span data-ttu-id="7b424-183">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-183">public str labelFont(\[str value\])</span></span>                                      |                                                                                                                                               |
| <span data-ttu-id="7b424-184">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-184">public int labelFontSize(\[int value\])</span></span>                                  |                                                                                                                                               |
| <span data-ttu-id="7b424-185">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-185">public boolean labelItalic(\[boolean value\])</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="7b424-186">public LineType labelLineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-186">public LineType labelLineBelow(\[LineType value\])</span></span>                       |                                                                                                                                               |
| <span data-ttu-id="7b424-187">public LineThickness labelLineThickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-187">public LineThickness labelLineThickness(\[LineThickness value\])</span></span>         |                                                                                                                                               |
| <span data-ttu-id="7b424-188">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-188">public int labelPosition(\[int value\])</span></span>                                  |                                                                                                                                               |
| <span data-ttu-id="7b424-189">public int labelTabLeader(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-189">public int labelTabLeader(\[int value\])</span></span>                                 |                                                                                                                                               |
| <span data-ttu-id="7b424-190">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-190">public boolean labelUnderline(\[boolean value\])</span></span>                         |                                                                                                                                               |
| <span data-ttu-id="7b424-191">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-191">public int labelWidthMode(\[int value\])</span></span>                                 |                                                                                                                                               |
| <span data-ttu-id="7b424-192">public str labelWidthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-192">public str labelWidthStr(\[str value\])</span></span>                                  |                                                                                                                                               |
| <span data-ttu-id="7b424-193">public Units labelWidthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-193">public Units labelWidthUnit(\[Units value\])</span></span>                             |                                                                                                                                               |
| <span data-ttu-id="7b424-194">public Real labelWidthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-194">public Real labelWidthValue(\[Real value\])</span></span>                              |                                                                                                                                               |
| <span data-ttu-id="7b424-195">public int left100mm(\[int leftExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="7b424-195">public int left100mm(\[int leftExclBorder\])</span></span>                             |                                                                                                                                               |
| <span data-ttu-id="7b424-196">public int left100mmInclBorder(\[int leftInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="7b424-196">public int left100mmInclBorder(\[int leftInclBorder\])</span></span>                   |                                                                                                                                               |
| <span data-ttu-id="7b424-197">public int leftMarginAnFrame()</span><span class="sxs-lookup"><span data-stu-id="7b424-197">public int leftMarginAnFrame()</span></span>                                           |                                                                                                                                               |
| <span data-ttu-id="7b424-198">public int leftMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-198">public int leftMarginMode(\[int value\])</span></span>                                 |                                                                                                                                               |
| <span data-ttu-id="7b424-199">public str leftMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-199">public str leftMarginStr(\[str value\])</span></span>                                  |                                                                                                                                               |
| <span data-ttu-id="7b424-200">public Units leftMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-200">public Units leftMarginUnit(\[Units value\])</span></span>                             |                                                                                                                                               |
| <span data-ttu-id="7b424-201">public Real leftMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-201">public Real leftMarginValue(\[Real value\])</span></span>                              |                                                                                                                                               |
| <span data-ttu-id="7b424-202">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-202">public int leftMode(\[int value\])</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="7b424-203">public str leftStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-203">public str leftStr(\[str value\])</span></span>                                        |                                                                                                                                               |
| <span data-ttu-id="7b424-204">public Units leftUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-204">public Units leftUnit(\[Units value\])</span></span>                                   |                                                                                                                                               |
| <span data-ttu-id="7b424-205">public Real leftValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-205">public Real leftValue(\[Real value\])</span></span>                                    |                                                                                                                                               |
| <span data-ttu-id="7b424-206">public LineType lineAbove(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-206">public LineType lineAbove(\[LineType value\])</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="7b424-207">public LineType lineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-207">public LineType lineBelow(\[LineType value\])</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="7b424-208">public LineType lineLeft(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-208">public LineType lineLeft(\[LineType value\])</span></span>                             | <span data-ttu-id="7b424-209">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-209">Gets or sets the type of line that is used as the left border of a section.</span></span>                                                                   |
| <span data-ttu-id="7b424-210">public LineType lineRight(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-210">public LineType lineRight(\[LineType value\])</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="7b424-211">public str menuItemLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-211">public str menuItemLabel(\[str value\])</span></span>                                  |                                                                                                                                               |
| <span data-ttu-id="7b424-212">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-212">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                                               |
| <span data-ttu-id="7b424-213">public MenuItemType menuItemType(\[MenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-213">public MenuItemType menuItemType(\[MenuItemType value\])</span></span>                 |                                                                                                                                               |
| <span data-ttu-id="7b424-214">public int minNoOfDecimals(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7b424-214">public int minNoOfDecimals(\[int value\], \[AutoMode mode\])</span></span>             |                                                                                                                                               |
| <span data-ttu-id="7b424-215">public AutoMode minNoOfDecimalsMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7b424-215">public AutoMode minNoOfDecimalsMode(\[AutoMode mode\])</span></span>                   |                                                                                                                                               |
| <span data-ttu-id="7b424-216">public int minNoOfDecimalsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-216">public int minNoOfDecimalsValue(\[int value\])</span></span>                           |                                                                                                                                               |
| <span data-ttu-id="7b424-217">public str modelFieldName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-217">public str modelFieldName(\[str value\])</span></span>                                 |                                                                                                                                               |
| <span data-ttu-id="7b424-218">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-218">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="7b424-219">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-219">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="7b424-220">public int noOfDecimals(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7b424-220">public int noOfDecimals(\[int value\], \[AutoMode mode\])</span></span>                |                                                                                                                                               |
| <span data-ttu-id="7b424-221">public AutoMode noOfDecimalsMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="7b424-221">public AutoMode noOfDecimalsMode(\[AutoMode mode\])</span></span>                      |                                                                                                                                               |
| <span data-ttu-id="7b424-222">public int noOfDecimalsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-222">public int noOfDecimalsValue(\[int value\])</span></span>                              |                                                                                                                                               |
| <span data-ttu-id="7b424-223">public int numberOfLines(int height100mm)</span><span class="sxs-lookup"><span data-stu-id="7b424-223">public int numberOfLines(int height100mm)</span></span>                                |                                                                                                                                               |
| <span data-ttu-id="7b424-224">public int position(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-224">public int position(\[int value\])</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="7b424-225">public str previewInfo(str string)</span><span class="sxs-lookup"><span data-stu-id="7b424-225">public str previewInfo(str string)</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="7b424-226">public int previewXCompensation100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="7b424-226">public int previewXCompensation100mm(str string)</span></span>                         |                                                                                                                                               |
| <span data-ttu-id="7b424-227">public int right100mm()</span><span class="sxs-lookup"><span data-stu-id="7b424-227">public int right100mm()</span></span>                                                  |                                                                                                                                               |
| <span data-ttu-id="7b424-228">public int right100mmInclBorder()</span><span class="sxs-lookup"><span data-stu-id="7b424-228">public int right100mmInclBorder()</span></span>                                        |                                                                                                                                               |
| <span data-ttu-id="7b424-229">public int rightMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="7b424-229">public int rightMarginAndFrame()</span></span>                                         |                                                                                                                                               |
| <span data-ttu-id="7b424-230">public int rightMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-230">public int rightMarginMode(\[int value\])</span></span>                                |                                                                                                                                               |
| <span data-ttu-id="7b424-231">public str rightMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-231">public str rightMarginStr(\[str value\])</span></span>                                 |                                                                                                                                               |
| <span data-ttu-id="7b424-232">public Units rightMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-232">public Units rightMarginUnit(\[Units value\])</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="7b424-233">public Real rightMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-233">public Real rightMarginValue(\[Real value\])</span></span>                             |                                                                                                                                               |
| <span data-ttu-id="7b424-234">public int rotateSign(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-234">public int rotateSign(\[int value\])</span></span>                                     |                                                                                                                                               |
| <span data-ttu-id="7b424-235">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-235">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                                               |
| <span data-ttu-id="7b424-236">public str setHeightGetText(int lines, str string)</span><span class="sxs-lookup"><span data-stu-id="7b424-236">public str setHeightGetText(int lines, str string)</span></span>                       |                                                                                                                                               |
| <span data-ttu-id="7b424-237">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-237">public boolean showLabel(\[boolean value\])</span></span>                              |                                                                                                                                               |
| <span data-ttu-id="7b424-238">public int showZero(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-238">public int showZero(\[int value\])</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="7b424-239">public int signDisplay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-239">public int signDisplay(\[int value\])</span></span>                                    |                                                                                                                                               |
| <span data-ttu-id="7b424-240">public boolean sumAll(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-240">public boolean sumAll(\[boolean value\])</span></span>                                 |                                                                                                                                               |
| <span data-ttu-id="7b424-241">public boolean sumNeg(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-241">public boolean sumNeg(\[boolean value\])</span></span>                                 |                                                                                                                                               |
| <span data-ttu-id="7b424-242">public boolean sumPos(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-242">public boolean sumPos(\[boolean value\])</span></span>                                 |                                                                                                                                               |
| <span data-ttu-id="7b424-243">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-243">public TableId table(\[TableId value\])</span></span>                                  | <span data-ttu-id="7b424-244">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-244">Gets or sets the table ID associated with the object.</span></span>                                                                                         |
| <span data-ttu-id="7b424-245">public LineThickness thickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-245">public LineThickness thickness(\[LineThickness value\])</span></span>                  |                                                                                                                                               |
| <span data-ttu-id="7b424-246">public int thousandSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-246">public int thousandSeparator(\[int value\])</span></span>                              |                                                                                                                                               |
| <span data-ttu-id="7b424-247">public int top100mm(\[int topExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="7b424-247">public int top100mm(\[int topExclBorder\])</span></span>                               |                                                                                                                                               |
| <span data-ttu-id="7b424-248">public int top100mmInclBorder(\[int topInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="7b424-248">public int top100mmInclBorder(\[int topInclBorder\])</span></span>                     |                                                                                                                                               |
| <span data-ttu-id="7b424-249">public int topMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="7b424-249">public int topMarginAndFrame()</span></span>                                           |                                                                                                                                               |
| <span data-ttu-id="7b424-250">public int topMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-250">public int topMarginMode(\[int value\])</span></span>                                  |                                                                                                                                               |
| <span data-ttu-id="7b424-251">public str topMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-251">public str topMarginStr(\[str value\])</span></span>                                   |                                                                                                                                               |
| <span data-ttu-id="7b424-252">public Units topMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-252">public Units topMarginUnit(\[Units value\])</span></span>                              |                                                                                                                                               |
| <span data-ttu-id="7b424-253">public Real topMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-253">public Real topMarginValue(\[Real value\])</span></span>                               |                                                                                                                                               |
| <span data-ttu-id="7b424-254">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-254">public int topMode(\[int value\])</span></span>                                        |                                                                                                                                               |
| <span data-ttu-id="7b424-255">public str topStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-255">public str topStr(\[str value\])</span></span>                                         |                                                                                                                                               |
| <span data-ttu-id="7b424-256">public Units topUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-256">public Units topUnit(\[Units value\])</span></span>                                    |                                                                                                                                               |
| <span data-ttu-id="7b424-257">public Real topValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-257">public Real topValue(\[Real value\])</span></span>                                     |                                                                                                                                               |
| <span data-ttu-id="7b424-258">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-258">public boolean underline(\[boolean value\])</span></span>                              |                                                                                                                                               |
| <span data-ttu-id="7b424-259">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-259">public boolean visible(\[boolean value\])</span></span>                                |                                                                                                                                               |
| <span data-ttu-id="7b424-260">public str webMenuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-260">public str webMenuItemName(\[str value\])</span></span>                                |                                                                                                                                               |
| <span data-ttu-id="7b424-261">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-261">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span></span>        |                                                                                                                                               |
| <span data-ttu-id="7b424-262">public str webTarget(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-262">public str webTarget(\[str value\])</span></span>                                      |                                                                                                                                               |
| <span data-ttu-id="7b424-263">public int width100mm(\[int widthExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="7b424-263">public int width100mm(\[int widthExclBorder\])</span></span>                           |                                                                                                                                               |
| <span data-ttu-id="7b424-264">public int width100mmInclBorder(\[int widthInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="7b424-264">public int width100mmInclBorder(\[int widthInclBorder\])</span></span>                 |                                                                                                                                               |
| <span data-ttu-id="7b424-265">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-265">public int widthMode(\[int value\])</span></span>                                      | <span data-ttu-id="7b424-266">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-266">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                |
| <span data-ttu-id="7b424-267">public int widthOfString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="7b424-267">public int widthOfString100mm(str string)</span></span>                                |                                                                                                                                               |
| <span data-ttu-id="7b424-268">public str widthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-268">public str widthStr(\[str value\])</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="7b424-269">public Units widthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-269">public Units widthUnit(\[Units value\])</span></span>                                  |                                                                                                                                               |
| <span data-ttu-id="7b424-270">public Real widthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="7b424-270">public Real widthValue(\[Real value\])</span></span>                                   | <span data-ttu-id="7b424-271">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-271">Gets or sets the width of the control.</span></span>                                                                                                        |
| <span data-ttu-id="7b424-272">public void show()</span><span class="sxs-lookup"><span data-stu-id="7b424-272">public void show()</span></span>                                                       |                                                                                                                                               |
| <span data-ttu-id="7b424-273">public void hide()</span><span class="sxs-lookup"><span data-stu-id="7b424-273">public void hide()</span></span>                                                       |                                                                                                                                               |
| <span data-ttu-id="7b424-274">public void height(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="7b424-274">public void height(Real value, Units unit)</span></span>                               | <span data-ttu-id="7b424-275">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-275">Gets or sets the height of the control.</span></span>                                                                                                       |
| <span data-ttu-id="7b424-276">public void rightMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="7b424-276">public void rightMargin(Real value, Units unit)</span></span>                          |                                                                                                                                               |
| <span data-ttu-id="7b424-277">public void left(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="7b424-277">public void left(Real value, Units unit)</span></span>                                 |                                                                                                                                               |
| <span data-ttu-id="7b424-278">public void width(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="7b424-278">public void width(Real value, Units unit)</span></span>                                | <span data-ttu-id="7b424-279">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-279">Gets or sets the width of the control.</span></span>                                                                                                        |
| <span data-ttu-id="7b424-280">public void extraSumWidth(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="7b424-280">public void extraSumWidth(Real value, Units unit)</span></span>                        |                                                                                                                                               |
| <span data-ttu-id="7b424-281">public void topMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="7b424-281">public void topMargin(Real value, Units unit)</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="7b424-282">public void leftMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="7b424-282">public void leftMargin(Real value, Units unit)</span></span>                           |                                                                                                                                               |
| <span data-ttu-id="7b424-283">public void labelWidth(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="7b424-283">public void labelWidth(Real value, Units unit)</span></span>                           |                                                                                                                                               |
| <span data-ttu-id="7b424-284">public void top(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="7b424-284">public void top(Real value, Units unit)</span></span>                                  |                                                                                                                                               |
| <span data-ttu-id="7b424-285">public void bottomMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="7b424-285">public void bottomMargin(Real value, Units unit)</span></span>                         |                                                                                                                                               |

## <a name="method-alignment"></a><span data-ttu-id="7b424-286">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="7b424-286">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="7b424-287">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="7b424-287">Parameters - alignment</span></span>

<span data-ttu-id="7b424-288">値</span><span class="sxs-lookup"><span data-stu-id="7b424-288">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="7b424-289">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="7b424-289">Return Value - alignment</span></span>

## <a name="method-allownegative"></a><span data-ttu-id="7b424-290">メソッド allowNegative</span><span class="sxs-lookup"><span data-stu-id="7b424-290">Method allowNegative</span></span>

```xpp
public int allowNegative([int value])
```

### <a name="parameters---allownegative"></a><span data-ttu-id="7b424-291">パラメーター - allowNegative</span><span class="sxs-lookup"><span data-stu-id="7b424-291">Parameters - allowNegative</span></span>

<span data-ttu-id="7b424-292">値</span><span class="sxs-lookup"><span data-stu-id="7b424-292">value</span></span>  

### <a name="return-value---allownegative"></a><span data-ttu-id="7b424-293">戻り値 - allowNegative</span><span class="sxs-lookup"><span data-stu-id="7b424-293">Return Value - allowNegative</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="7b424-294">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="7b424-294">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="7b424-295">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="7b424-295">Parameters - arrayIndex</span></span>

<span data-ttu-id="7b424-296">値</span><span class="sxs-lookup"><span data-stu-id="7b424-296">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="7b424-297">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="7b424-297">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="7b424-298">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="7b424-298">Method autoDeclaration</span></span>

<span data-ttu-id="7b424-299">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-299">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="7b424-300">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="7b424-300">Parameters - autoDeclaration</span></span>

<span data-ttu-id="7b424-301">値</span><span class="sxs-lookup"><span data-stu-id="7b424-301">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="7b424-302">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="7b424-302">Return Value - autoDeclaration</span></span>

<span data-ttu-id="7b424-303">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="7b424-303">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="7b424-304">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="7b424-304">Remarks - autoDeclaration</span></span>

<span data-ttu-id="7b424-305">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="7b424-305">Controls cannot have identical names.</span></span>

## <a name="method-autoinsseparator"></a><span data-ttu-id="7b424-306">メソッド autoInsSeparator</span><span class="sxs-lookup"><span data-stu-id="7b424-306">Method autoInsSeparator</span></span>

```xpp
public int autoInsSeparator([int value])
```

### <a name="parameters---autoinsseparator"></a><span data-ttu-id="7b424-307">パラメーター - autoInsSeparator</span><span class="sxs-lookup"><span data-stu-id="7b424-307">Parameters - autoInsSeparator</span></span>

<span data-ttu-id="7b424-308">値</span><span class="sxs-lookup"><span data-stu-id="7b424-308">value</span></span>  

### <a name="return-value---autoinsseparator"></a><span data-ttu-id="7b424-309">戻り値 - autoInsSeparator</span><span class="sxs-lookup"><span data-stu-id="7b424-309">Return Value - autoInsSeparator</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="7b424-310">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="7b424-310">Method backgroundColor</span></span>

<span data-ttu-id="7b424-311">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-311">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="7b424-312">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="7b424-312">Parameters - backgroundColor</span></span>

<span data-ttu-id="7b424-313">値</span><span class="sxs-lookup"><span data-stu-id="7b424-313">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="7b424-314">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="7b424-314">Return Value - backgroundColor</span></span>

<span data-ttu-id="7b424-315">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="7b424-315">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="7b424-316">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="7b424-316">Remarks - backgroundColor</span></span>

<span data-ttu-id="7b424-317">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7b424-317">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="7b424-318">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7b424-318">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="7b424-319">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="7b424-319">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="7b424-320">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="7b424-320">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="7b424-321">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="7b424-321">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="7b424-322">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="7b424-322">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="7b424-323">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="7b424-323">Method backStyle</span></span>

<span data-ttu-id="7b424-324">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-324">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="7b424-325">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="7b424-325">Parameters - backStyle</span></span>

<span data-ttu-id="7b424-326">値</span><span class="sxs-lookup"><span data-stu-id="7b424-326">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="7b424-327">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="7b424-327">Return Value - backStyle</span></span>

<span data-ttu-id="7b424-328">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="7b424-328">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="7b424-329">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="7b424-329">Method bold</span></span>

<span data-ttu-id="7b424-330">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-330">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="7b424-331">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="7b424-331">Parameters - bold</span></span>

<span data-ttu-id="7b424-332">値</span><span class="sxs-lookup"><span data-stu-id="7b424-332">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="7b424-333">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="7b424-333">Return Value - bold</span></span>

<span data-ttu-id="7b424-334">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="7b424-334">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="7b424-335">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="7b424-335">Remarks - bold</span></span>

<span data-ttu-id="7b424-336">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7b424-336">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="7b424-337">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="7b424-337">0 Use the default font weight.</span></span>
-   <span data-ttu-id="7b424-338">1 シン。</span><span class="sxs-lookup"><span data-stu-id="7b424-338">1 Thin.</span></span>
-   <span data-ttu-id="7b424-339">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="7b424-339">2 Extra-light.</span></span>
-   <span data-ttu-id="7b424-340">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="7b424-340">3 Light.</span></span>
-   <span data-ttu-id="7b424-341">4 標準。</span><span class="sxs-lookup"><span data-stu-id="7b424-341">4 Normal.</span></span>
-   <span data-ttu-id="7b424-342">5 中。</span><span class="sxs-lookup"><span data-stu-id="7b424-342">5 Medium.</span></span>
-   <span data-ttu-id="7b424-343">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="7b424-343">6 Semibold.</span></span>
-   <span data-ttu-id="7b424-344">7 太字。</span><span class="sxs-lookup"><span data-stu-id="7b424-344">7 Bold.</span></span>
-   <span data-ttu-id="7b424-345">8 極太。</span><span class="sxs-lookup"><span data-stu-id="7b424-345">8 Extra-bold.</span></span>
-   <span data-ttu-id="7b424-346">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="7b424-346">9 Heavy.</span></span>

## <a name="method-bottommarginandframe"></a><span data-ttu-id="7b424-347">メソッド bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="7b424-347">Method bottomMarginAndFrame</span></span>

```xpp
public int bottomMarginAndFrame()
```

### <a name="return-value---bottommarginandframe"></a><span data-ttu-id="7b424-348">戻り値 - bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="7b424-348">Return Value - bottomMarginAndFrame</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="7b424-349">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="7b424-349">Method bottomMarginMode</span></span>

```xpp
public int bottomMarginMode([int value])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="7b424-350">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="7b424-350">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="7b424-351">値</span><span class="sxs-lookup"><span data-stu-id="7b424-351">value</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="7b424-352">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="7b424-352">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginstr"></a><span data-ttu-id="7b424-353">メソッド bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="7b424-353">Method bottomMarginStr</span></span>

```xpp
public str bottomMarginStr([str value])
```

### <a name="parameters---bottommarginstr"></a><span data-ttu-id="7b424-354">パラメーター - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="7b424-354">Parameters - bottomMarginStr</span></span>

<span data-ttu-id="7b424-355">値</span><span class="sxs-lookup"><span data-stu-id="7b424-355">value</span></span>  

### <a name="return-value---bottommarginstr"></a><span data-ttu-id="7b424-356">戻り値 - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="7b424-356">Return Value - bottomMarginStr</span></span>

## <a name="method-bottommarginunit"></a><span data-ttu-id="7b424-357">メソッド bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-357">Method bottomMarginUnit</span></span>

```xpp
public Units bottomMarginUnit([Units value])
```

### <a name="parameters---bottommarginunit"></a><span data-ttu-id="7b424-358">パラメーター - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-358">Parameters - bottomMarginUnit</span></span>

<span data-ttu-id="7b424-359">値</span><span class="sxs-lookup"><span data-stu-id="7b424-359">value</span></span>  

### <a name="return-value---bottommarginunit"></a><span data-ttu-id="7b424-360">戻り値 - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-360">Return Value - bottomMarginUnit</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="7b424-361">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="7b424-361">Method bottomMarginValue</span></span>

```xpp
public Real bottomMarginValue([Real value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="7b424-362">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="7b424-362">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="7b424-363">値</span><span class="sxs-lookup"><span data-stu-id="7b424-363">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="7b424-364">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="7b424-364">Return Value - bottomMarginValue</span></span>

## <a name="method-changelabelcase"></a><span data-ttu-id="7b424-365">メソッド changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="7b424-365">Method changeLabelCase</span></span>

```xpp
public int changeLabelCase([int value])
```

### <a name="parameters---changelabelcase"></a><span data-ttu-id="7b424-366">パラメーター - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="7b424-366">Parameters - changeLabelCase</span></span>

<span data-ttu-id="7b424-367">値</span><span class="sxs-lookup"><span data-stu-id="7b424-367">value</span></span>  

### <a name="return-value---changelabelcase"></a><span data-ttu-id="7b424-368">戻り値 - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="7b424-368">Return Value - changeLabelCase</span></span>

## <a name="method-characterset"></a><span data-ttu-id="7b424-369">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="7b424-369">Method characterSet</span></span>

<span data-ttu-id="7b424-370">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-370">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="7b424-371">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="7b424-371">Parameters - characterSet</span></span>

<span data-ttu-id="7b424-372">値</span><span class="sxs-lookup"><span data-stu-id="7b424-372">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="7b424-373">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="7b424-373">Return Value - characterSet</span></span>

<span data-ttu-id="7b424-374">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7b424-374">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="7b424-375">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="7b424-375">Remarks - characterSet</span></span>

<span data-ttu-id="7b424-376">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="7b424-376">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="7b424-377">値です。</span><span class="sxs-lookup"><span data-stu-id="7b424-377">Value.</span></span> | <span data-ttu-id="7b424-378">説明。</span><span class="sxs-lookup"><span data-stu-id="7b424-378">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="7b424-379">0</span><span class="sxs-lookup"><span data-stu-id="7b424-379">0</span></span>      | <span data-ttu-id="7b424-380">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7b424-380">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="7b424-381">1</span><span class="sxs-lookup"><span data-stu-id="7b424-381">1</span></span>      | <span data-ttu-id="7b424-382">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7b424-382">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="7b424-383">2</span><span class="sxs-lookup"><span data-stu-id="7b424-383">2</span></span>      | <span data-ttu-id="7b424-384">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7b424-384">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="7b424-385">77</span><span class="sxs-lookup"><span data-stu-id="7b424-385">77</span></span>     | <span data-ttu-id="7b424-386">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7b424-386">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="7b424-387">128</span><span class="sxs-lookup"><span data-stu-id="7b424-387">128</span></span>    | <span data-ttu-id="7b424-388">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7b424-388">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="7b424-389">129</span><span class="sxs-lookup"><span data-stu-id="7b424-389">129</span></span>    | <span data-ttu-id="7b424-390">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7b424-390">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="7b424-391">134</span><span class="sxs-lookup"><span data-stu-id="7b424-391">134</span></span>    | <span data-ttu-id="7b424-392">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7b424-392">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="7b424-393">136</span><span class="sxs-lookup"><span data-stu-id="7b424-393">136</span></span>    | <span data-ttu-id="7b424-394">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7b424-394">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="7b424-395">161</span><span class="sxs-lookup"><span data-stu-id="7b424-395">161</span></span>    | <span data-ttu-id="7b424-396">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7b424-396">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="7b424-397">162</span><span class="sxs-lookup"><span data-stu-id="7b424-397">162</span></span>    | <span data-ttu-id="7b424-398">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7b424-398">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="7b424-399">163</span><span class="sxs-lookup"><span data-stu-id="7b424-399">163</span></span>    | <span data-ttu-id="7b424-400">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7b424-400">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="7b424-401">186</span><span class="sxs-lookup"><span data-stu-id="7b424-401">186</span></span>    | <span data-ttu-id="7b424-402">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7b424-402">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="7b424-403">204</span><span class="sxs-lookup"><span data-stu-id="7b424-403">204</span></span>    | <span data-ttu-id="7b424-404">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7b424-404">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="7b424-405">238</span><span class="sxs-lookup"><span data-stu-id="7b424-405">238</span></span>    | <span data-ttu-id="7b424-406">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7b424-406">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="7b424-407">255</span><span class="sxs-lookup"><span data-stu-id="7b424-407">255</span></span>    | <span data-ttu-id="7b424-408">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7b424-408">OEM\_CHARSET</span></span>         |

<span data-ttu-id="7b424-409">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="7b424-409">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="7b424-410">値です。</span><span class="sxs-lookup"><span data-stu-id="7b424-410">Value.</span></span> | <span data-ttu-id="7b424-411">説明。</span><span class="sxs-lookup"><span data-stu-id="7b424-411">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="7b424-412">130</span><span class="sxs-lookup"><span data-stu-id="7b424-412">130</span></span>    | <span data-ttu-id="7b424-413">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7b424-413">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="7b424-414">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="7b424-414">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="7b424-415">値です。</span><span class="sxs-lookup"><span data-stu-id="7b424-415">Value.</span></span> | <span data-ttu-id="7b424-416">説明。</span><span class="sxs-lookup"><span data-stu-id="7b424-416">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="7b424-417">177</span><span class="sxs-lookup"><span data-stu-id="7b424-417">177</span></span>    | <span data-ttu-id="7b424-418">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7b424-418">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="7b424-419">178</span><span class="sxs-lookup"><span data-stu-id="7b424-419">178</span></span>    | <span data-ttu-id="7b424-420">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7b424-420">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="7b424-421">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="7b424-421">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="7b424-422">値です。</span><span class="sxs-lookup"><span data-stu-id="7b424-422">Value.</span></span> | <span data-ttu-id="7b424-423">説明。</span><span class="sxs-lookup"><span data-stu-id="7b424-423">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="7b424-424">222</span><span class="sxs-lookup"><span data-stu-id="7b424-424">222</span></span>    | <span data-ttu-id="7b424-425">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="7b424-425">THAI\_CHARSET</span></span> |

<span data-ttu-id="7b424-426">既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="7b424-426">The default character set is set to a value, depending on the current system locale.</span></span> <span data-ttu-id="7b424-427">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="7b424-427">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="7b424-428">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7b424-428">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="7b424-429">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="7b424-429">Method colorScheme</span></span>

<span data-ttu-id="7b424-430">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-430">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="7b424-431">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="7b424-431">Parameters - colorScheme</span></span>

<span data-ttu-id="7b424-432">値</span><span class="sxs-lookup"><span data-stu-id="7b424-432">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="7b424-433">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="7b424-433">Return Value - colorScheme</span></span>

<span data-ttu-id="7b424-434">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="7b424-434">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="7b424-435">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="7b424-435">Remarks - colorScheme</span></span>

<span data-ttu-id="7b424-436">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="7b424-436">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="7b424-437">値です。</span><span class="sxs-lookup"><span data-stu-id="7b424-437">Value.</span></span> | <span data-ttu-id="7b424-438">スタイル。</span><span class="sxs-lookup"><span data-stu-id="7b424-438">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="7b424-439">0</span><span class="sxs-lookup"><span data-stu-id="7b424-439">0</span></span>      | <span data-ttu-id="7b424-440">既定。</span><span class="sxs-lookup"><span data-stu-id="7b424-440">Default.</span></span>                      |
| <span data-ttu-id="7b424-441">1</span><span class="sxs-lookup"><span data-stu-id="7b424-441">1</span></span>      | <span data-ttu-id="7b424-442">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="7b424-442">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="7b424-443">2</span><span class="sxs-lookup"><span data-stu-id="7b424-443">2</span></span>      | <span data-ttu-id="7b424-444">真の配色。</span><span class="sxs-lookup"><span data-stu-id="7b424-444">The true-color scheme.</span></span>        |

## <a name="method-configurationkey"></a><span data-ttu-id="7b424-445">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="7b424-445">Method configurationKey</span></span>

<span data-ttu-id="7b424-446">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-446">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="7b424-447">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="7b424-447">Parameters - configurationKey</span></span>

<span data-ttu-id="7b424-448">値</span><span class="sxs-lookup"><span data-stu-id="7b424-448">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="7b424-449">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="7b424-449">Return Value - configurationKey</span></span>

<span data-ttu-id="7b424-450">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="7b424-450">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="7b424-451">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="7b424-451">Remarks - configurationKey</span></span>

<span data-ttu-id="7b424-452">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7b424-452">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="7b424-453">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="7b424-453">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-controltype"></a><span data-ttu-id="7b424-454">メソッド controlType</span><span class="sxs-lookup"><span data-stu-id="7b424-454">Method controlType</span></span>

```xpp
public ReportFieldType controlType()
```

### <a name="return-value---controltype"></a><span data-ttu-id="7b424-455">戻り値 - controlType</span><span class="sxs-lookup"><span data-stu-id="7b424-455">Return Value - controlType</span></span>

## <a name="method-cssclass"></a><span data-ttu-id="7b424-456">メソッド cssClass</span><span class="sxs-lookup"><span data-stu-id="7b424-456">Method cssClass</span></span>

```xpp
public str cssClass([str value])
```

### <a name="parameters---cssclass"></a><span data-ttu-id="7b424-457">パラメーター - cssClass</span><span class="sxs-lookup"><span data-stu-id="7b424-457">Parameters - cssClass</span></span>

<span data-ttu-id="7b424-458">値</span><span class="sxs-lookup"><span data-stu-id="7b424-458">value</span></span>  

### <a name="return-value---cssclass"></a><span data-ttu-id="7b424-459">戻り値 - cssClass</span><span class="sxs-lookup"><span data-stu-id="7b424-459">Return Value - cssClass</span></span>

## <a name="method-datafield"></a><span data-ttu-id="7b424-460">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="7b424-460">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="7b424-461">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="7b424-461">Parameters - dataField</span></span>

<span data-ttu-id="7b424-462">値</span><span class="sxs-lookup"><span data-stu-id="7b424-462">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="7b424-463">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="7b424-463">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="7b424-464">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="7b424-464">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="7b424-465">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="7b424-465">Parameters - dataMethod</span></span>

<span data-ttu-id="7b424-466">値</span><span class="sxs-lookup"><span data-stu-id="7b424-466">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="7b424-467">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="7b424-467">Return Value - dataMethod</span></span>

## <a name="method-decimalseparator"></a><span data-ttu-id="7b424-468">メソッド decimalSeparator</span><span class="sxs-lookup"><span data-stu-id="7b424-468">Method decimalSeparator</span></span>

```xpp
public int decimalSeparator([int value])
```

### <a name="parameters---decimalseparator"></a><span data-ttu-id="7b424-469">パラメーター - decimalSeparator</span><span class="sxs-lookup"><span data-stu-id="7b424-469">Parameters - decimalSeparator</span></span>

<span data-ttu-id="7b424-470">値</span><span class="sxs-lookup"><span data-stu-id="7b424-470">value</span></span>  

### <a name="return-value---decimalseparator"></a><span data-ttu-id="7b424-471">戻り値 - decimalSeparator</span><span class="sxs-lookup"><span data-stu-id="7b424-471">Return Value - decimalSeparator</span></span>

## <a name="method-delete"></a><span data-ttu-id="7b424-472">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="7b424-472">Method delete</span></span>

```xpp
public int delete()
```

### <a name="return-value---delete"></a><span data-ttu-id="7b424-473">戻り値 - delete</span><span class="sxs-lookup"><span data-stu-id="7b424-473">Return Value - delete</span></span>

## <a name="method-displacenegative"></a><span data-ttu-id="7b424-474">メソッド displaceNegative</span><span class="sxs-lookup"><span data-stu-id="7b424-474">Method displaceNegative</span></span>

```xpp
public int displaceNegative([int value], [AutoMode mode])
```

### <a name="parameters---displacenegative"></a><span data-ttu-id="7b424-475">パラメーター - displaceNegative</span><span class="sxs-lookup"><span data-stu-id="7b424-475">Parameters - displaceNegative</span></span>

<span data-ttu-id="7b424-476">値</span><span class="sxs-lookup"><span data-stu-id="7b424-476">value</span></span>  

<!-- -->

<span data-ttu-id="7b424-477">モード</span><span class="sxs-lookup"><span data-stu-id="7b424-477">mode</span></span>  

### <a name="return-value---displacenegative"></a><span data-ttu-id="7b424-478">戻り値 - displaceNegative</span><span class="sxs-lookup"><span data-stu-id="7b424-478">Return Value - displaceNegative</span></span>

## <a name="method-displacenegativemode"></a><span data-ttu-id="7b424-479">メソッド displaceNegativeMode</span><span class="sxs-lookup"><span data-stu-id="7b424-479">Method displaceNegativeMode</span></span>

```xpp
public AutoMode displaceNegativeMode([AutoMode mode])
```

### <a name="parameters---displacenegativemode"></a><span data-ttu-id="7b424-480">パラメーター - displaceNegativeMode</span><span class="sxs-lookup"><span data-stu-id="7b424-480">Parameters - displaceNegativeMode</span></span>

<span data-ttu-id="7b424-481">モード</span><span class="sxs-lookup"><span data-stu-id="7b424-481">mode</span></span>  

### <a name="return-value---displacenegativemode"></a><span data-ttu-id="7b424-482">戻り値 - displaceNegativeMode</span><span class="sxs-lookup"><span data-stu-id="7b424-482">Return Value - displaceNegativeMode</span></span>

## <a name="method-displacenegativevalue"></a><span data-ttu-id="7b424-483">メソッド displaceNegativeValue</span><span class="sxs-lookup"><span data-stu-id="7b424-483">Method displaceNegativeValue</span></span>

```xpp
public int displaceNegativeValue([int value])
```

### <a name="parameters---displacenegativevalue"></a><span data-ttu-id="7b424-484">パラメーター - displaceNegativeValue</span><span class="sxs-lookup"><span data-stu-id="7b424-484">Parameters - displaceNegativeValue</span></span>

<span data-ttu-id="7b424-485">値</span><span class="sxs-lookup"><span data-stu-id="7b424-485">value</span></span>  

### <a name="return-value---displacenegativevalue"></a><span data-ttu-id="7b424-486">戻り値 - displaceNegativeValue</span><span class="sxs-lookup"><span data-stu-id="7b424-486">Return Value - displaceNegativeValue</span></span>

## <a name="method-effectivefont"></a><span data-ttu-id="7b424-487">メソッド effectiveFont</span><span class="sxs-lookup"><span data-stu-id="7b424-487">Method effectiveFont</span></span>

```xpp
public str effectiveFont()
```

### <a name="return-value---effectivefont"></a><span data-ttu-id="7b424-488">戻り値 - effectiveFont</span><span class="sxs-lookup"><span data-stu-id="7b424-488">Return Value - effectiveFont</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="7b424-489">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="7b424-489">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="7b424-490">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="7b424-490">Parameters - extendedDataType</span></span>

<span data-ttu-id="7b424-491">値</span><span class="sxs-lookup"><span data-stu-id="7b424-491">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="7b424-492">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="7b424-492">Return Value - extendedDataType</span></span>

## <a name="method-extrasumwidthmode"></a><span data-ttu-id="7b424-493">メソッド extraSumWidthMode</span><span class="sxs-lookup"><span data-stu-id="7b424-493">Method extraSumWidthMode</span></span>

```xpp
public int extraSumWidthMode([int value])
```

### <a name="parameters---extrasumwidthmode"></a><span data-ttu-id="7b424-494">パラメーター - extraSumWidthMode</span><span class="sxs-lookup"><span data-stu-id="7b424-494">Parameters - extraSumWidthMode</span></span>

<span data-ttu-id="7b424-495">値</span><span class="sxs-lookup"><span data-stu-id="7b424-495">value</span></span>  

### <a name="return-value---extrasumwidthmode"></a><span data-ttu-id="7b424-496">戻り値 - extraSumWidthMode</span><span class="sxs-lookup"><span data-stu-id="7b424-496">Return Value - extraSumWidthMode</span></span>

## <a name="method-extrasumwidthstr"></a><span data-ttu-id="7b424-497">メソッド extraSumWidthStr</span><span class="sxs-lookup"><span data-stu-id="7b424-497">Method extraSumWidthStr</span></span>

```xpp
public str extraSumWidthStr([str value])
```

### <a name="parameters---extrasumwidthstr"></a><span data-ttu-id="7b424-498">パラメーター - extraSumWidthStr</span><span class="sxs-lookup"><span data-stu-id="7b424-498">Parameters - extraSumWidthStr</span></span>

<span data-ttu-id="7b424-499">値</span><span class="sxs-lookup"><span data-stu-id="7b424-499">value</span></span>  

### <a name="return-value---extrasumwidthstr"></a><span data-ttu-id="7b424-500">戻り値 - extraSumWidthStr</span><span class="sxs-lookup"><span data-stu-id="7b424-500">Return Value - extraSumWidthStr</span></span>

## <a name="method-extrasumwidthunit"></a><span data-ttu-id="7b424-501">メソッド extraSumWidthUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-501">Method extraSumWidthUnit</span></span>

```xpp
public Units extraSumWidthUnit([Units value])
```

### <a name="parameters---extrasumwidthunit"></a><span data-ttu-id="7b424-502">パラメーター - extraSumWidthUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-502">Parameters - extraSumWidthUnit</span></span>

<span data-ttu-id="7b424-503">値</span><span class="sxs-lookup"><span data-stu-id="7b424-503">value</span></span>  

### <a name="return-value---extrasumwidthunit"></a><span data-ttu-id="7b424-504">戻り値 - extraSumWidthUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-504">Return Value - extraSumWidthUnit</span></span>

## <a name="method-extrasumwidthvalue"></a><span data-ttu-id="7b424-505">メソッド extraSumWidthValue</span><span class="sxs-lookup"><span data-stu-id="7b424-505">Method extraSumWidthValue</span></span>

```xpp
public Real extraSumWidthValue([Real value])
```

### <a name="parameters---extrasumwidthvalue"></a><span data-ttu-id="7b424-506">パラメーター - extraSumWidthValue</span><span class="sxs-lookup"><span data-stu-id="7b424-506">Parameters - extraSumWidthValue</span></span>

<span data-ttu-id="7b424-507">値</span><span class="sxs-lookup"><span data-stu-id="7b424-507">value</span></span>  

### <a name="return-value---extrasumwidthvalue"></a><span data-ttu-id="7b424-508">戻り値 - extraSumWidthValue</span><span class="sxs-lookup"><span data-stu-id="7b424-508">Return Value - extraSumWidthValue</span></span>

## <a name="method-font"></a><span data-ttu-id="7b424-509">メソッド font</span><span class="sxs-lookup"><span data-stu-id="7b424-509">Method font</span></span>

<span data-ttu-id="7b424-510">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-510">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="7b424-511">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="7b424-511">Parameters - font</span></span>

<span data-ttu-id="7b424-512">値</span><span class="sxs-lookup"><span data-stu-id="7b424-512">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="7b424-513">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="7b424-513">Return Value - font</span></span>

<span data-ttu-id="7b424-514">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="7b424-514">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontinfoprinter"></a><span data-ttu-id="7b424-515">メソッド fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="7b424-515">Method fontInfoPrinter</span></span>

```xpp
public str fontInfoPrinter()
```

### <a name="return-value---fontinfoprinter"></a><span data-ttu-id="7b424-516">戻り値 - fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="7b424-516">Return Value - fontInfoPrinter</span></span>

## <a name="method-fontinfoprinterascent"></a><span data-ttu-id="7b424-517">メソッド fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="7b424-517">Method fontInfoPrinterAscent</span></span>

```xpp
public int fontInfoPrinterAscent()
```

### <a name="return-value---fontinfoprinterascent"></a><span data-ttu-id="7b424-518">戻り値 - fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="7b424-518">Return Value - fontInfoPrinterAscent</span></span>

## <a name="method-fontinfoprinterdescent"></a><span data-ttu-id="7b424-519">メソッド fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="7b424-519">Method fontInfoPrinterDescent</span></span>

```xpp
public int fontInfoPrinterDescent()
```

### <a name="return-value---fontinfoprinterdescent"></a><span data-ttu-id="7b424-520">戻り値 - fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="7b424-520">Return Value - fontInfoPrinterDescent</span></span>

## <a name="method-fontinfoprinterextlead"></a><span data-ttu-id="7b424-521">メソッド fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="7b424-521">Method fontInfoPrinterExtLead</span></span>

```xpp
public int fontInfoPrinterExtLead()
```

### <a name="return-value---fontinfoprinterextlead"></a><span data-ttu-id="7b424-522">戻り値 - fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="7b424-522">Return Value - fontInfoPrinterExtLead</span></span>

## <a name="method-fontinfoprinterheight"></a><span data-ttu-id="7b424-523">メソッド fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="7b424-523">Method fontInfoPrinterHeight</span></span>

```xpp
public int fontInfoPrinterHeight()
```

### <a name="return-value---fontinfoprinterheight"></a><span data-ttu-id="7b424-524">戻り値 - fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="7b424-524">Return Value - fontInfoPrinterHeight</span></span>

## <a name="method-fontinfoprinterintlead"></a><span data-ttu-id="7b424-525">メソッド fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="7b424-525">Method fontInfoPrinterIntLead</span></span>

```xpp
public int fontInfoPrinterIntLead()
```

### <a name="return-value---fontinfoprinterintlead"></a><span data-ttu-id="7b424-526">戻り値 - fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="7b424-526">Return Value - fontInfoPrinterIntLead</span></span>

## <a name="method-fontinfoscreen"></a><span data-ttu-id="7b424-527">メソッド fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="7b424-527">Method fontInfoScreen</span></span>

```xpp
public str fontInfoScreen()
```

### <a name="return-value---fontinfoscreen"></a><span data-ttu-id="7b424-528">戻り値 - fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="7b424-528">Return Value - fontInfoScreen</span></span>

## <a name="method-fontinfoscreenascent"></a><span data-ttu-id="7b424-529">メソッド fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="7b424-529">Method fontInfoScreenAscent</span></span>

```xpp
public int fontInfoScreenAscent()
```

### <a name="return-value---fontinfoscreenascent"></a><span data-ttu-id="7b424-530">戻り値 - fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="7b424-530">Return Value - fontInfoScreenAscent</span></span>

## <a name="method-fontinfoscreendescent"></a><span data-ttu-id="7b424-531">メソッド fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="7b424-531">Method fontInfoScreenDescent</span></span>

```xpp
public int fontInfoScreenDescent()
```

### <a name="return-value---fontinfoscreendescent"></a><span data-ttu-id="7b424-532">戻り値 - fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="7b424-532">Return Value - fontInfoScreenDescent</span></span>

## <a name="method-fontinfoscreenextlead"></a><span data-ttu-id="7b424-533">メソッド fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="7b424-533">Method fontInfoScreenExtLead</span></span>

```xpp
public int fontInfoScreenExtLead()
```

### <a name="return-value---fontinfoscreenextlead"></a><span data-ttu-id="7b424-534">戻り値 - fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="7b424-534">Return Value - fontInfoScreenExtLead</span></span>

## <a name="method-fontinfoscreenheight"></a><span data-ttu-id="7b424-535">メソッド fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="7b424-535">Method fontInfoScreenHeight</span></span>

```xpp
public int fontInfoScreenHeight()
```

### <a name="return-value---fontinfoscreenheight"></a><span data-ttu-id="7b424-536">戻り値 - fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="7b424-536">Return Value - fontInfoScreenHeight</span></span>

## <a name="method-fontinfoscreenintlead"></a><span data-ttu-id="7b424-537">メソッド fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="7b424-537">Method fontInfoScreenIntLead</span></span>

```xpp
public int fontInfoScreenIntLead()
```

### <a name="return-value---fontinfoscreenintlead"></a><span data-ttu-id="7b424-538">戻り値 - fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="7b424-538">Return Value - fontInfoScreenIntLead</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="7b424-539">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="7b424-539">Method fontSize</span></span>

<span data-ttu-id="7b424-540">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-540">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="7b424-541">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="7b424-541">Parameters - fontSize</span></span>

<span data-ttu-id="7b424-542">値</span><span class="sxs-lookup"><span data-stu-id="7b424-542">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="7b424-543">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="7b424-543">Return Value - fontSize</span></span>

<span data-ttu-id="7b424-544">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="7b424-544">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="7b424-545">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="7b424-545">Method foregroundColor</span></span>

<span data-ttu-id="7b424-546">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-546">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="7b424-547">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="7b424-547">Parameters - foregroundColor</span></span>

<span data-ttu-id="7b424-548">値</span><span class="sxs-lookup"><span data-stu-id="7b424-548">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="7b424-549">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="7b424-549">Return Value - foregroundColor</span></span>

<span data-ttu-id="7b424-550">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="7b424-550">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="7b424-551">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="7b424-551">Remarks - foregroundColor</span></span>

<span data-ttu-id="7b424-552">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7b424-552">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="7b424-553">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7b424-553">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="7b424-554">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="7b424-554">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="7b424-555">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="7b424-555">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="7b424-556">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="7b424-556">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="7b424-557">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="7b424-557">The maximum value for a single byte is 255.</span></span>

## <a name="method-formatmst"></a><span data-ttu-id="7b424-558">メソッド formatMST</span><span class="sxs-lookup"><span data-stu-id="7b424-558">Method formatMST</span></span>

```xpp
public int formatMST([int value])
```

### <a name="parameters---formatmst"></a><span data-ttu-id="7b424-559">パラメーター - formatMST</span><span class="sxs-lookup"><span data-stu-id="7b424-559">Parameters - formatMST</span></span>

<span data-ttu-id="7b424-560">値</span><span class="sxs-lookup"><span data-stu-id="7b424-560">value</span></span>  

### <a name="return-value---formatmst"></a><span data-ttu-id="7b424-561">戻り値 - formatMST</span><span class="sxs-lookup"><span data-stu-id="7b424-561">Return Value - formatMST</span></span>

## <a name="method-height100mm"></a><span data-ttu-id="7b424-562">メソッド height100mm</span><span class="sxs-lookup"><span data-stu-id="7b424-562">Method height100mm</span></span>

```xpp
public int height100mm([int heightExclBorder])
```

### <a name="parameters---height100mm"></a><span data-ttu-id="7b424-563">パラメーター - height100mm</span><span class="sxs-lookup"><span data-stu-id="7b424-563">Parameters - height100mm</span></span>

<span data-ttu-id="7b424-564">heightExclBorder</span><span class="sxs-lookup"><span data-stu-id="7b424-564">heightExclBorder</span></span>  

### <a name="return-value---height100mm"></a><span data-ttu-id="7b424-565">戻り値 - height100mm</span><span class="sxs-lookup"><span data-stu-id="7b424-565">Return Value - height100mm</span></span>

## <a name="method-height100mminclborder"></a><span data-ttu-id="7b424-566">メソッド height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="7b424-566">Method height100mmInclBorder</span></span>

```xpp
public int height100mmInclBorder([int heightInclBorder])
```

### <a name="parameters---height100mminclborder"></a><span data-ttu-id="7b424-567">パラメーター - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="7b424-567">Parameters - height100mmInclBorder</span></span>

<span data-ttu-id="7b424-568">heightInclBorder</span><span class="sxs-lookup"><span data-stu-id="7b424-568">heightInclBorder</span></span>  

### <a name="return-value---height100mminclborder"></a><span data-ttu-id="7b424-569">戻り値 - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="7b424-569">Return Value - height100mmInclBorder</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="7b424-570">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="7b424-570">Method heightMode</span></span>

<span data-ttu-id="7b424-571">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-571">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="7b424-572">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="7b424-572">Parameters - heightMode</span></span>

<span data-ttu-id="7b424-573">値</span><span class="sxs-lookup"><span data-stu-id="7b424-573">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="7b424-574">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="7b424-574">Return Value - heightMode</span></span>

<span data-ttu-id="7b424-575">計算モード。</span><span class="sxs-lookup"><span data-stu-id="7b424-575">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="7b424-576">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="7b424-576">Remarks - heightMode</span></span>

<span data-ttu-id="7b424-577">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="7b424-577">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="7b424-578">モード。</span><span class="sxs-lookup"><span data-stu-id="7b424-578">Mode.</span></span>          | <span data-ttu-id="7b424-579">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="7b424-579">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b424-580">正確。</span><span class="sxs-lookup"><span data-stu-id="7b424-580">Exact.</span></span>         | <span data-ttu-id="7b424-581">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="7b424-581">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="7b424-582">自動。</span><span class="sxs-lookup"><span data-stu-id="7b424-582">Auto.</span></span>          | <span data-ttu-id="7b424-583">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="7b424-583">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="7b424-584">列の高さ</span><span class="sxs-lookup"><span data-stu-id="7b424-584">Column height.</span></span> | <span data-ttu-id="7b424-585">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="7b424-585">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="7b424-586">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="7b424-586">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightofwordwrappedstring100mm"></a><span data-ttu-id="7b424-587">メソッド heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="7b424-587">Method heightOfWordWrappedString100mm</span></span>

```xpp
public int heightOfWordWrappedString100mm(str string)
```

### <a name="parameters---heightofwordwrappedstring100mm"></a><span data-ttu-id="7b424-588">パラメーター - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="7b424-588">Parameters - heightOfWordWrappedString100mm</span></span>

<span data-ttu-id="7b424-589">文字列</span><span class="sxs-lookup"><span data-stu-id="7b424-589">string</span></span>  

### <a name="return-value---heightofwordwrappedstring100mm"></a><span data-ttu-id="7b424-590">戻り値 - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="7b424-590">Return Value - heightOfWordWrappedString100mm</span></span>

## <a name="method-heightstr"></a><span data-ttu-id="7b424-591">メソッド heightStr</span><span class="sxs-lookup"><span data-stu-id="7b424-591">Method heightStr</span></span>

```xpp
public str heightStr([str value])
```

### <a name="parameters---heightstr"></a><span data-ttu-id="7b424-592">パラメーター - heightStr</span><span class="sxs-lookup"><span data-stu-id="7b424-592">Parameters - heightStr</span></span>

<span data-ttu-id="7b424-593">値</span><span class="sxs-lookup"><span data-stu-id="7b424-593">value</span></span>  

### <a name="return-value---heightstr"></a><span data-ttu-id="7b424-594">戻り値 - heightStr</span><span class="sxs-lookup"><span data-stu-id="7b424-594">Return Value - heightStr</span></span>

## <a name="method-heightunit"></a><span data-ttu-id="7b424-595">メソッド heightUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-595">Method heightUnit</span></span>

```xpp
public Units heightUnit([Units value])
```

### <a name="parameters---heightunit"></a><span data-ttu-id="7b424-596">パラメーター - heightUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-596">Parameters - heightUnit</span></span>

<span data-ttu-id="7b424-597">値</span><span class="sxs-lookup"><span data-stu-id="7b424-597">value</span></span>  

### <a name="return-value---heightunit"></a><span data-ttu-id="7b424-598">戻り値 - heightUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-598">Return Value - heightUnit</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="7b424-599">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="7b424-599">Method heightValue</span></span>

<span data-ttu-id="7b424-600">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-600">Gets or sets the height of the control.</span></span>

```xpp
public Real heightValue([Real value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="7b424-601">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="7b424-601">Parameters - heightValue</span></span>

<span data-ttu-id="7b424-602">値</span><span class="sxs-lookup"><span data-stu-id="7b424-602">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="7b424-603">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="7b424-603">Return Value - heightValue</span></span>

<span data-ttu-id="7b424-604">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="7b424-604">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="7b424-605">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="7b424-605">Remarks - heightValue</span></span>

<span data-ttu-id="7b424-606">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="7b424-606">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-italic"></a><span data-ttu-id="7b424-607">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="7b424-607">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="7b424-608">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="7b424-608">Parameters - italic</span></span>

<span data-ttu-id="7b424-609">値</span><span class="sxs-lookup"><span data-stu-id="7b424-609">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="7b424-610">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="7b424-610">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="7b424-611">メソッド label</span><span class="sxs-lookup"><span data-stu-id="7b424-611">Method label</span></span>

<span data-ttu-id="7b424-612">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-612">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="7b424-613">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="7b424-613">Parameters - label</span></span>

<span data-ttu-id="7b424-614">値</span><span class="sxs-lookup"><span data-stu-id="7b424-614">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="7b424-615">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="7b424-615">Return Value - label</span></span>

<span data-ttu-id="7b424-616">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="7b424-616">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="7b424-617">備考 - label</span><span class="sxs-lookup"><span data-stu-id="7b424-617">Remarks - label</span></span>

<span data-ttu-id="7b424-618">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-618">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="7b424-619">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="7b424-619">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="7b424-620">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="7b424-620">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="7b424-621">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="7b424-621">Parameters - labelBold</span></span>

<span data-ttu-id="7b424-622">値</span><span class="sxs-lookup"><span data-stu-id="7b424-622">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="7b424-623">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="7b424-623">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="7b424-624">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="7b424-624">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="7b424-625">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="7b424-625">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="7b424-626">値</span><span class="sxs-lookup"><span data-stu-id="7b424-626">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="7b424-627">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="7b424-627">Return Value - labelCharacterSet</span></span>

## <a name="method-labelcssclass"></a><span data-ttu-id="7b424-628">メソッド labelCssClass</span><span class="sxs-lookup"><span data-stu-id="7b424-628">Method labelCssClass</span></span>

```xpp
public str labelCssClass([str value])
```

### <a name="parameters---labelcssclass"></a><span data-ttu-id="7b424-629">パラメーター - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="7b424-629">Parameters - labelCssClass</span></span>

<span data-ttu-id="7b424-630">値</span><span class="sxs-lookup"><span data-stu-id="7b424-630">value</span></span>  

### <a name="return-value---labelcssclass"></a><span data-ttu-id="7b424-631">戻り値 - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="7b424-631">Return Value - labelCssClass</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="7b424-632">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="7b424-632">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="7b424-633">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="7b424-633">Parameters - labelFont</span></span>

<span data-ttu-id="7b424-634">値</span><span class="sxs-lookup"><span data-stu-id="7b424-634">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="7b424-635">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="7b424-635">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="7b424-636">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="7b424-636">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="7b424-637">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="7b424-637">Parameters - labelFontSize</span></span>

<span data-ttu-id="7b424-638">値</span><span class="sxs-lookup"><span data-stu-id="7b424-638">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="7b424-639">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="7b424-639">Return Value - labelFontSize</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="7b424-640">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="7b424-640">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="7b424-641">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="7b424-641">Parameters - labelItalic</span></span>

<span data-ttu-id="7b424-642">値</span><span class="sxs-lookup"><span data-stu-id="7b424-642">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="7b424-643">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="7b424-643">Return Value - labelItalic</span></span>

## <a name="method-labellinebelow"></a><span data-ttu-id="7b424-644">メソッド labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="7b424-644">Method labelLineBelow</span></span>

```xpp
public LineType labelLineBelow([LineType value])
```

### <a name="parameters---labellinebelow"></a><span data-ttu-id="7b424-645">パラメーター - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="7b424-645">Parameters - labelLineBelow</span></span>

<span data-ttu-id="7b424-646">値</span><span class="sxs-lookup"><span data-stu-id="7b424-646">value</span></span>  

### <a name="return-value---labellinebelow"></a><span data-ttu-id="7b424-647">戻り値 - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="7b424-647">Return Value - labelLineBelow</span></span>

## <a name="method-labellinethickness"></a><span data-ttu-id="7b424-648">メソッド labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="7b424-648">Method labelLineThickness</span></span>

```xpp
public LineThickness labelLineThickness([LineThickness value])
```

### <a name="parameters---labellinethickness"></a><span data-ttu-id="7b424-649">パラメーター - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="7b424-649">Parameters - labelLineThickness</span></span>

<span data-ttu-id="7b424-650">値</span><span class="sxs-lookup"><span data-stu-id="7b424-650">value</span></span>  

### <a name="return-value---labellinethickness"></a><span data-ttu-id="7b424-651">戻り値 - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="7b424-651">Return Value - labelLineThickness</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="7b424-652">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="7b424-652">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="7b424-653">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="7b424-653">Parameters - labelPosition</span></span>

<span data-ttu-id="7b424-654">値</span><span class="sxs-lookup"><span data-stu-id="7b424-654">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="7b424-655">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="7b424-655">Return Value - labelPosition</span></span>

## <a name="method-labeltableader"></a><span data-ttu-id="7b424-656">メソッド labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="7b424-656">Method labelTabLeader</span></span>

```xpp
public int labelTabLeader([int value])
```

### <a name="parameters---labeltableader"></a><span data-ttu-id="7b424-657">パラメーター - labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="7b424-657">Parameters - labelTabLeader</span></span>

<span data-ttu-id="7b424-658">値</span><span class="sxs-lookup"><span data-stu-id="7b424-658">value</span></span>  

### <a name="return-value---labeltableader"></a><span data-ttu-id="7b424-659">戻り値 - labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="7b424-659">Return Value - labelTabLeader</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="7b424-660">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="7b424-660">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="7b424-661">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="7b424-661">Parameters - labelUnderline</span></span>

<span data-ttu-id="7b424-662">値</span><span class="sxs-lookup"><span data-stu-id="7b424-662">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="7b424-663">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="7b424-663">Return Value - labelUnderline</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="7b424-664">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="7b424-664">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="7b424-665">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="7b424-665">Parameters - labelWidthMode</span></span>

<span data-ttu-id="7b424-666">値</span><span class="sxs-lookup"><span data-stu-id="7b424-666">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="7b424-667">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="7b424-667">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthstr"></a><span data-ttu-id="7b424-668">メソッド labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="7b424-668">Method labelWidthStr</span></span>

```xpp
public str labelWidthStr([str value])
```

### <a name="parameters---labelwidthstr"></a><span data-ttu-id="7b424-669">パラメーター - labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="7b424-669">Parameters - labelWidthStr</span></span>

<span data-ttu-id="7b424-670">値</span><span class="sxs-lookup"><span data-stu-id="7b424-670">value</span></span>  

### <a name="return-value---labelwidthstr"></a><span data-ttu-id="7b424-671">戻り値 - labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="7b424-671">Return Value - labelWidthStr</span></span>

## <a name="method-labelwidthunit"></a><span data-ttu-id="7b424-672">メソッド labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-672">Method labelWidthUnit</span></span>

```xpp
public Units labelWidthUnit([Units value])
```

### <a name="parameters---labelwidthunit"></a><span data-ttu-id="7b424-673">パラメーター - labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-673">Parameters - labelWidthUnit</span></span>

<span data-ttu-id="7b424-674">値</span><span class="sxs-lookup"><span data-stu-id="7b424-674">value</span></span>  

### <a name="return-value---labelwidthunit"></a><span data-ttu-id="7b424-675">戻り値 - labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-675">Return Value - labelWidthUnit</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="7b424-676">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="7b424-676">Method labelWidthValue</span></span>

```xpp
public Real labelWidthValue([Real value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="7b424-677">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="7b424-677">Parameters - labelWidthValue</span></span>

<span data-ttu-id="7b424-678">値</span><span class="sxs-lookup"><span data-stu-id="7b424-678">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="7b424-679">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="7b424-679">Return Value - labelWidthValue</span></span>

## <a name="method-left100mm"></a><span data-ttu-id="7b424-680">メソッド left100mm</span><span class="sxs-lookup"><span data-stu-id="7b424-680">Method left100mm</span></span>

```xpp
public int left100mm([int leftExclBorder])
```

### <a name="parameters---left100mm"></a><span data-ttu-id="7b424-681">パラメーター - left100mm</span><span class="sxs-lookup"><span data-stu-id="7b424-681">Parameters - left100mm</span></span>

<span data-ttu-id="7b424-682">leftExclBorder</span><span class="sxs-lookup"><span data-stu-id="7b424-682">leftExclBorder</span></span>  

### <a name="return-value---left100mm"></a><span data-ttu-id="7b424-683">戻り値 - left100mm</span><span class="sxs-lookup"><span data-stu-id="7b424-683">Return Value - left100mm</span></span>

## <a name="method-left100mminclborder"></a><span data-ttu-id="7b424-684">メソッド left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="7b424-684">Method left100mmInclBorder</span></span>

```xpp
public int left100mmInclBorder([int leftInclBorder])
```

### <a name="parameters---left100mminclborder"></a><span data-ttu-id="7b424-685">パラメーター - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="7b424-685">Parameters - left100mmInclBorder</span></span>

<span data-ttu-id="7b424-686">leftInclBorder</span><span class="sxs-lookup"><span data-stu-id="7b424-686">leftInclBorder</span></span>  

### <a name="return-value---left100mminclborder"></a><span data-ttu-id="7b424-687">戻り値 - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="7b424-687">Return Value - left100mmInclBorder</span></span>

## <a name="method-leftmarginanframe"></a><span data-ttu-id="7b424-688">メソッド leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="7b424-688">Method leftMarginAnFrame</span></span>

```xpp
public int leftMarginAnFrame()
```

### <a name="return-value---leftmarginanframe"></a><span data-ttu-id="7b424-689">戻り値 - leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="7b424-689">Return Value - leftMarginAnFrame</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="7b424-690">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="7b424-690">Method leftMarginMode</span></span>

```xpp
public int leftMarginMode([int value])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="7b424-691">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="7b424-691">Parameters - leftMarginMode</span></span>

<span data-ttu-id="7b424-692">値</span><span class="sxs-lookup"><span data-stu-id="7b424-692">value</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="7b424-693">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="7b424-693">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginstr"></a><span data-ttu-id="7b424-694">メソッド leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="7b424-694">Method leftMarginStr</span></span>

```xpp
public str leftMarginStr([str value])
```

### <a name="parameters---leftmarginstr"></a><span data-ttu-id="7b424-695">パラメーター - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="7b424-695">Parameters - leftMarginStr</span></span>

<span data-ttu-id="7b424-696">値</span><span class="sxs-lookup"><span data-stu-id="7b424-696">value</span></span>  

### <a name="return-value---leftmarginstr"></a><span data-ttu-id="7b424-697">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="7b424-697">Return Value - leftMarginStr</span></span>

## <a name="method-leftmarginunit"></a><span data-ttu-id="7b424-698">メソッド leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-698">Method leftMarginUnit</span></span>

```xpp
public Units leftMarginUnit([Units value])
```

### <a name="parameters---leftmarginunit"></a><span data-ttu-id="7b424-699">パラメーター - leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-699">Parameters - leftMarginUnit</span></span>

<span data-ttu-id="7b424-700">値</span><span class="sxs-lookup"><span data-stu-id="7b424-700">value</span></span>  

### <a name="return-value---leftmarginunit"></a><span data-ttu-id="7b424-701">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="7b424-701">Return Value - leftMarginUnit</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="7b424-702">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="7b424-702">Method leftMarginValue</span></span>

```xpp
public Real leftMarginValue([Real value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="7b424-703">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="7b424-703">Parameters - leftMarginValue</span></span>

<span data-ttu-id="7b424-704">値</span><span class="sxs-lookup"><span data-stu-id="7b424-704">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="7b424-705">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="7b424-705">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="7b424-706">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="7b424-706">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="7b424-707">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="7b424-707">Parameters - leftMode</span></span>

<span data-ttu-id="7b424-708">値</span><span class="sxs-lookup"><span data-stu-id="7b424-708">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="7b424-709">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="7b424-709">Return Value - leftMode</span></span>

## <a name="method-leftstr"></a><span data-ttu-id="7b424-710">メソッド leftStr</span><span class="sxs-lookup"><span data-stu-id="7b424-710">Method leftStr</span></span>

```xpp
public str leftStr([str value])
```

### <a name="parameters---leftstr"></a><span data-ttu-id="7b424-711">パラメーター - leftStr</span><span class="sxs-lookup"><span data-stu-id="7b424-711">Parameters - leftStr</span></span>

<span data-ttu-id="7b424-712">値</span><span class="sxs-lookup"><span data-stu-id="7b424-712">value</span></span>  

### <a name="return-value---leftstr"></a><span data-ttu-id="7b424-713">戻り値 - leftStr</span><span class="sxs-lookup"><span data-stu-id="7b424-713">Return Value - leftStr</span></span>

## <a name="method-leftunit"></a><span data-ttu-id="7b424-714">メソッド leftUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-714">Method leftUnit</span></span>

```xpp
public Units leftUnit([Units value])
```

### <a name="parameters---leftunit"></a><span data-ttu-id="7b424-715">パラメーター - leftUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-715">Parameters - leftUnit</span></span>

<span data-ttu-id="7b424-716">値</span><span class="sxs-lookup"><span data-stu-id="7b424-716">value</span></span>  

### <a name="return-value---leftunit"></a><span data-ttu-id="7b424-717">戻り値 - leftUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-717">Return Value - leftUnit</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="7b424-718">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="7b424-718">Method leftValue</span></span>

```xpp
public Real leftValue([Real value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="7b424-719">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="7b424-719">Parameters - leftValue</span></span>

<span data-ttu-id="7b424-720">値</span><span class="sxs-lookup"><span data-stu-id="7b424-720">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="7b424-721">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="7b424-721">Return Value - leftValue</span></span>

## <a name="method-lineabove"></a><span data-ttu-id="7b424-722">メソッド lineAbove</span><span class="sxs-lookup"><span data-stu-id="7b424-722">Method lineAbove</span></span>

```xpp
public LineType lineAbove([LineType value])
```

### <a name="parameters---lineabove"></a><span data-ttu-id="7b424-723">パラメーター - lineAbove</span><span class="sxs-lookup"><span data-stu-id="7b424-723">Parameters - lineAbove</span></span>

<span data-ttu-id="7b424-724">値</span><span class="sxs-lookup"><span data-stu-id="7b424-724">value</span></span>  

### <a name="return-value---lineabove"></a><span data-ttu-id="7b424-725">戻り値 - lineAbove</span><span class="sxs-lookup"><span data-stu-id="7b424-725">Return Value - lineAbove</span></span>

## <a name="method-linebelow"></a><span data-ttu-id="7b424-726">メソッド lineBelow</span><span class="sxs-lookup"><span data-stu-id="7b424-726">Method lineBelow</span></span>

```xpp
public LineType lineBelow([LineType value])
```

### <a name="parameters---linebelow"></a><span data-ttu-id="7b424-727">パラメーター - lineBelow</span><span class="sxs-lookup"><span data-stu-id="7b424-727">Parameters - lineBelow</span></span>

<span data-ttu-id="7b424-728">値</span><span class="sxs-lookup"><span data-stu-id="7b424-728">value</span></span>  

### <a name="return-value---linebelow"></a><span data-ttu-id="7b424-729">戻り値 - lineBelow</span><span class="sxs-lookup"><span data-stu-id="7b424-729">Return Value - lineBelow</span></span>

## <a name="method-lineleft"></a><span data-ttu-id="7b424-730">メソッド lineLeft</span><span class="sxs-lookup"><span data-stu-id="7b424-730">Method lineLeft</span></span>

<span data-ttu-id="7b424-731">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-731">Gets or sets the type of line that is used as the left border of a section.</span></span>

```xpp
public LineType lineLeft([LineType value])
```

### <a name="parameters---lineleft"></a><span data-ttu-id="7b424-732">パラメーター - lineLeft</span><span class="sxs-lookup"><span data-stu-id="7b424-732">Parameters - lineLeft</span></span>

<span data-ttu-id="7b424-733">値</span><span class="sxs-lookup"><span data-stu-id="7b424-733">value</span></span>  

### <a name="return-value---lineleft"></a><span data-ttu-id="7b424-734">戻り値 - lineLeft</span><span class="sxs-lookup"><span data-stu-id="7b424-734">Return Value - lineLeft</span></span>

<span data-ttu-id="7b424-735">左境界線として使用される線のタイプ。</span><span class="sxs-lookup"><span data-stu-id="7b424-735">The type of line that is used as the left border.</span></span>

## <a name="method-lineright"></a><span data-ttu-id="7b424-736">メソッド lineRight</span><span class="sxs-lookup"><span data-stu-id="7b424-736">Method lineRight</span></span>

```xpp
public LineType lineRight([LineType value])
```

### <a name="parameters---lineright"></a><span data-ttu-id="7b424-737">パラメーター - lineRight</span><span class="sxs-lookup"><span data-stu-id="7b424-737">Parameters - lineRight</span></span>

<span data-ttu-id="7b424-738">値</span><span class="sxs-lookup"><span data-stu-id="7b424-738">value</span></span>  

### <a name="return-value---lineright"></a><span data-ttu-id="7b424-739">戻り値 - lineRight</span><span class="sxs-lookup"><span data-stu-id="7b424-739">Return Value - lineRight</span></span>

## <a name="method-menuitemlabel"></a><span data-ttu-id="7b424-740">メソッド menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="7b424-740">Method menuItemLabel</span></span>

```xpp
public str menuItemLabel([str value])
```

### <a name="parameters---menuitemlabel"></a><span data-ttu-id="7b424-741">パラメーター - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="7b424-741">Parameters - menuItemLabel</span></span>

<span data-ttu-id="7b424-742">値</span><span class="sxs-lookup"><span data-stu-id="7b424-742">value</span></span>  

### <a name="return-value---menuitemlabel"></a><span data-ttu-id="7b424-743">戻り値 - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="7b424-743">Return Value - menuItemLabel</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="7b424-744">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="7b424-744">Method menuItemName</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="7b424-745">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="7b424-745">Parameters - menuItemName</span></span>

<span data-ttu-id="7b424-746">値</span><span class="sxs-lookup"><span data-stu-id="7b424-746">value</span></span>  

### <a name="return-value---menuitemname"></a><span data-ttu-id="7b424-747">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="7b424-747">Return Value - menuItemName</span></span>

## <a name="method-menuitemtype"></a><span data-ttu-id="7b424-748">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="7b424-748">Method menuItemType</span></span>

```xpp
public MenuItemType menuItemType([MenuItemType value])
```

### <a name="parameters---menuitemtype"></a><span data-ttu-id="7b424-749">パラメーター - menuItemType</span><span class="sxs-lookup"><span data-stu-id="7b424-749">Parameters - menuItemType</span></span>

<span data-ttu-id="7b424-750">値</span><span class="sxs-lookup"><span data-stu-id="7b424-750">value</span></span>  

### <a name="return-value---menuitemtype"></a><span data-ttu-id="7b424-751">戻り値 - menuItemType</span><span class="sxs-lookup"><span data-stu-id="7b424-751">Return Value - menuItemType</span></span>

## <a name="method-minnoofdecimals"></a><span data-ttu-id="7b424-752">メソッド minNoOfDecimals</span><span class="sxs-lookup"><span data-stu-id="7b424-752">Method minNoOfDecimals</span></span>

```xpp
public int minNoOfDecimals([int value], [AutoMode mode])
```

### <a name="parameters---minnoofdecimals"></a><span data-ttu-id="7b424-753">パラメーター - minNoOfDecimals</span><span class="sxs-lookup"><span data-stu-id="7b424-753">Parameters - minNoOfDecimals</span></span>

<span data-ttu-id="7b424-754">値</span><span class="sxs-lookup"><span data-stu-id="7b424-754">value</span></span>  

<!-- -->

<span data-ttu-id="7b424-755">モード</span><span class="sxs-lookup"><span data-stu-id="7b424-755">mode</span></span>  

### <a name="return-value---minnoofdecimals"></a><span data-ttu-id="7b424-756">戻り値 - minNoOfDecimals</span><span class="sxs-lookup"><span data-stu-id="7b424-756">Return Value - minNoOfDecimals</span></span>

## <a name="method-minnoofdecimalsmode"></a><span data-ttu-id="7b424-757">メソッド minNoOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="7b424-757">Method minNoOfDecimalsMode</span></span>

```xpp
public AutoMode minNoOfDecimalsMode([AutoMode mode])
```

### <a name="parameters---minnoofdecimalsmode"></a><span data-ttu-id="7b424-758">パラメーター - minNoOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="7b424-758">Parameters - minNoOfDecimalsMode</span></span>

<span data-ttu-id="7b424-759">モード</span><span class="sxs-lookup"><span data-stu-id="7b424-759">mode</span></span>  

### <a name="return-value---minnoofdecimalsmode"></a><span data-ttu-id="7b424-760">戻り値 - minNoOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="7b424-760">Return Value - minNoOfDecimalsMode</span></span>

## <a name="method-minnoofdecimalsvalue"></a><span data-ttu-id="7b424-761">メソッド minNoOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="7b424-761">Method minNoOfDecimalsValue</span></span>

```xpp
public int minNoOfDecimalsValue([int value])
```

### <a name="parameters---minnoofdecimalsvalue"></a><span data-ttu-id="7b424-762">パラメーター - minNoOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="7b424-762">Parameters - minNoOfDecimalsValue</span></span>

<span data-ttu-id="7b424-763">値</span><span class="sxs-lookup"><span data-stu-id="7b424-763">value</span></span>  

### <a name="return-value---minnoofdecimalsvalue"></a><span data-ttu-id="7b424-764">戻り値 - minNoOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="7b424-764">Return Value - minNoOfDecimalsValue</span></span>

## <a name="method-modelfieldname"></a><span data-ttu-id="7b424-765">メソッド modelFieldName</span><span class="sxs-lookup"><span data-stu-id="7b424-765">Method modelFieldName</span></span>

```xpp
public str modelFieldName([str value])
```

### <a name="parameters---modelfieldname"></a><span data-ttu-id="7b424-766">パラメーター - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="7b424-766">Parameters - modelFieldName</span></span>

<span data-ttu-id="7b424-767">値</span><span class="sxs-lookup"><span data-stu-id="7b424-767">value</span></span>  

### <a name="return-value---modelfieldname"></a><span data-ttu-id="7b424-768">戻り値 - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="7b424-768">Return Value - modelFieldName</span></span>

## <a name="method-name"></a><span data-ttu-id="7b424-769">メソッド名</span><span class="sxs-lookup"><span data-stu-id="7b424-769">Method name</span></span>

<span data-ttu-id="7b424-770">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-770">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="7b424-771">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="7b424-771">Parameters - name</span></span>

<span data-ttu-id="7b424-772">値</span><span class="sxs-lookup"><span data-stu-id="7b424-772">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="7b424-773">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="7b424-773">Return Value - name</span></span>

<span data-ttu-id="7b424-774">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="7b424-774">The name that is used in the code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="7b424-775">備考 - name</span><span class="sxs-lookup"><span data-stu-id="7b424-775">Remarks - name</span></span>

<span data-ttu-id="7b424-776">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b424-776">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="7b424-777">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="7b424-777">Begins with a letter.</span></span>
-   <span data-ttu-id="7b424-778">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="7b424-778">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="7b424-779">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7b424-779">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="7b424-780">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="7b424-780">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="7b424-781">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="7b424-781">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-noofdecimals"></a><span data-ttu-id="7b424-782">メソッド noOfDecimals</span><span class="sxs-lookup"><span data-stu-id="7b424-782">Method noOfDecimals</span></span>

```xpp
public int noOfDecimals([int value], [AutoMode mode])
```

### <a name="parameters---noofdecimals"></a><span data-ttu-id="7b424-783">パラメーター - noOfDecimals</span><span class="sxs-lookup"><span data-stu-id="7b424-783">Parameters - noOfDecimals</span></span>

<span data-ttu-id="7b424-784">値</span><span class="sxs-lookup"><span data-stu-id="7b424-784">value</span></span>  

<!-- -->

<span data-ttu-id="7b424-785">モード</span><span class="sxs-lookup"><span data-stu-id="7b424-785">mode</span></span>  

### <a name="return-value---noofdecimals"></a><span data-ttu-id="7b424-786">戻り値 - noOfDecimals</span><span class="sxs-lookup"><span data-stu-id="7b424-786">Return Value - noOfDecimals</span></span>

## <a name="method-noofdecimalsmode"></a><span data-ttu-id="7b424-787">メソッド noOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="7b424-787">Method noOfDecimalsMode</span></span>

```xpp
public AutoMode noOfDecimalsMode([AutoMode mode])
```

### <a name="parameters---noofdecimalsmode"></a><span data-ttu-id="7b424-788">パラメーター - noOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="7b424-788">Parameters - noOfDecimalsMode</span></span>

<span data-ttu-id="7b424-789">モード</span><span class="sxs-lookup"><span data-stu-id="7b424-789">mode</span></span>  

### <a name="return-value---noofdecimalsmode"></a><span data-ttu-id="7b424-790">戻り値 - noOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="7b424-790">Return Value - noOfDecimalsMode</span></span>

## <a name="method-noofdecimalsvalue"></a><span data-ttu-id="7b424-791">メソッド noOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="7b424-791">Method noOfDecimalsValue</span></span>

```xpp
public int noOfDecimalsValue([int value])
```

### <a name="parameters---noofdecimalsvalue"></a><span data-ttu-id="7b424-792">パラメーター - noOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="7b424-792">Parameters - noOfDecimalsValue</span></span>

<span data-ttu-id="7b424-793">値</span><span class="sxs-lookup"><span data-stu-id="7b424-793">value</span></span>  

### <a name="return-value---noofdecimalsvalue"></a><span data-ttu-id="7b424-794">戻り値 - noOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="7b424-794">Return Value - noOfDecimalsValue</span></span>

## <a name="method-numberoflines"></a><span data-ttu-id="7b424-795">メソッド numberOfLines</span><span class="sxs-lookup"><span data-stu-id="7b424-795">Method numberOfLines</span></span>

```xpp
public int numberOfLines(int height100mm)
```

### <a name="parameters---numberoflines"></a><span data-ttu-id="7b424-796">パラメーター - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="7b424-796">Parameters - numberOfLines</span></span>

<span data-ttu-id="7b424-797">height100mm</span><span class="sxs-lookup"><span data-stu-id="7b424-797">height100mm</span></span>  

### <a name="return-value---numberoflines"></a><span data-ttu-id="7b424-798">戻り値 - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="7b424-798">Return Value - numberOfLines</span></span>

## <a name="method-position"></a><span data-ttu-id="7b424-799">メソッドの位置</span><span class="sxs-lookup"><span data-stu-id="7b424-799">Method position</span></span>

```xpp
public int position([int value])
```

### <a name="parameters---position"></a><span data-ttu-id="7b424-800">パラメーター - position</span><span class="sxs-lookup"><span data-stu-id="7b424-800">Parameters - position</span></span>

<span data-ttu-id="7b424-801">値</span><span class="sxs-lookup"><span data-stu-id="7b424-801">value</span></span>  

### <a name="return-value---position"></a><span data-ttu-id="7b424-802">戻り値 - position</span><span class="sxs-lookup"><span data-stu-id="7b424-802">Return Value - position</span></span>

## <a name="method-previewinfo"></a><span data-ttu-id="7b424-803">メソッド previewInfo</span><span class="sxs-lookup"><span data-stu-id="7b424-803">Method previewInfo</span></span>

```xpp
public str previewInfo(str string)
```

### <a name="parameters---previewinfo"></a><span data-ttu-id="7b424-804">パラメーター - previewInfo</span><span class="sxs-lookup"><span data-stu-id="7b424-804">Parameters - previewInfo</span></span>

<span data-ttu-id="7b424-805">文字列</span><span class="sxs-lookup"><span data-stu-id="7b424-805">string</span></span>  

### <a name="return-value---previewinfo"></a><span data-ttu-id="7b424-806">戻り値 - previewInfo</span><span class="sxs-lookup"><span data-stu-id="7b424-806">Return Value - previewInfo</span></span>

## <a name="method-previewxcompensation100mm"></a><span data-ttu-id="7b424-807">メソッド previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="7b424-807">Method previewXCompensation100mm</span></span>

```xpp
public int previewXCompensation100mm(str string)
```

### <a name="parameters---previewxcompensation100mm"></a><span data-ttu-id="7b424-808">パラメーター - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="7b424-808">Parameters - previewXCompensation100mm</span></span>

<span data-ttu-id="7b424-809">文字列</span><span class="sxs-lookup"><span data-stu-id="7b424-809">string</span></span>  

### <a name="return-value---previewxcompensation100mm"></a><span data-ttu-id="7b424-810">戻り値 - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="7b424-810">Return Value - previewXCompensation100mm</span></span>

## <a name="method-right100mm"></a><span data-ttu-id="7b424-811">メソッド right100mm</span><span class="sxs-lookup"><span data-stu-id="7b424-811">Method right100mm</span></span>

```xpp
public int right100mm()
```

### <a name="return-value---right100mm"></a><span data-ttu-id="7b424-812">戻り値 - right100mm</span><span class="sxs-lookup"><span data-stu-id="7b424-812">Return Value - right100mm</span></span>

## <a name="method-right100mminclborder"></a><span data-ttu-id="7b424-813">メソッド right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="7b424-813">Method right100mmInclBorder</span></span>

```xpp
public int right100mmInclBorder()
```

### <a name="return-value---right100mminclborder"></a><span data-ttu-id="7b424-814">戻り値 - right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="7b424-814">Return Value - right100mmInclBorder</span></span>

## <a name="method-rightmarginandframe"></a><span data-ttu-id="7b424-815">メソッド rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="7b424-815">Method rightMarginAndFrame</span></span>

```xpp
public int rightMarginAndFrame()
```

### <a name="return-value---rightmarginandframe"></a><span data-ttu-id="7b424-816">戻り値 - rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="7b424-816">Return Value - rightMarginAndFrame</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="7b424-817">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="7b424-817">Method rightMarginMode</span></span>

```xpp
public int rightMarginMode([int value])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="7b424-818">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="7b424-818">Parameters - rightMarginMode</span></span>

<span data-ttu-id="7b424-819">値</span><span class="sxs-lookup"><span data-stu-id="7b424-819">value</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="7b424-820">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="7b424-820">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginstr"></a><span data-ttu-id="7b424-821">メソッド rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="7b424-821">Method rightMarginStr</span></span>

```xpp
public str rightMarginStr([str value])
```

### <a name="parameters---rightmarginstr"></a><span data-ttu-id="7b424-822">パラメーター - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="7b424-822">Parameters - rightMarginStr</span></span>

<span data-ttu-id="7b424-823">値</span><span class="sxs-lookup"><span data-stu-id="7b424-823">value</span></span>  

### <a name="return-value---rightmarginstr"></a><span data-ttu-id="7b424-824">戻り値 - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="7b424-824">Return Value - rightMarginStr</span></span>

## <a name="method-rightmarginunit"></a><span data-ttu-id="7b424-825">メソッド rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-825">Method rightMarginUnit</span></span>

```xpp
public Units rightMarginUnit([Units value])
```

### <a name="parameters---rightmarginunit"></a><span data-ttu-id="7b424-826">パラメーター - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-826">Parameters - rightMarginUnit</span></span>

<span data-ttu-id="7b424-827">値</span><span class="sxs-lookup"><span data-stu-id="7b424-827">value</span></span>  

### <a name="return-value---rightmarginunit"></a><span data-ttu-id="7b424-828">戻り値 - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-828">Return Value - rightMarginUnit</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="7b424-829">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="7b424-829">Method rightMarginValue</span></span>

```xpp
public Real rightMarginValue([Real value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="7b424-830">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="7b424-830">Parameters - rightMarginValue</span></span>

<span data-ttu-id="7b424-831">値</span><span class="sxs-lookup"><span data-stu-id="7b424-831">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="7b424-832">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="7b424-832">Return Value - rightMarginValue</span></span>

## <a name="method-rotatesign"></a><span data-ttu-id="7b424-833">メソッド rotateSign</span><span class="sxs-lookup"><span data-stu-id="7b424-833">Method rotateSign</span></span>

```xpp
public int rotateSign([int value])
```

### <a name="parameters---rotatesign"></a><span data-ttu-id="7b424-834">パラメーター - rotateSign</span><span class="sxs-lookup"><span data-stu-id="7b424-834">Parameters - rotateSign</span></span>

<span data-ttu-id="7b424-835">値</span><span class="sxs-lookup"><span data-stu-id="7b424-835">value</span></span>  

### <a name="return-value---rotatesign"></a><span data-ttu-id="7b424-836">戻り値 - rotateSign</span><span class="sxs-lookup"><span data-stu-id="7b424-836">Return Value - rotateSign</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="7b424-837">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="7b424-837">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="7b424-838">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="7b424-838">Parameters - securityKey</span></span>

<span data-ttu-id="7b424-839">値</span><span class="sxs-lookup"><span data-stu-id="7b424-839">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="7b424-840">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="7b424-840">Return Value - securityKey</span></span>

## <a name="method-setheightgettext"></a><span data-ttu-id="7b424-841">メソッド setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="7b424-841">Method setHeightGetText</span></span>

```xpp
public str setHeightGetText(int lines, str string)
```

### <a name="parameters---setheightgettext"></a><span data-ttu-id="7b424-842">パラメーター - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="7b424-842">Parameters - setHeightGetText</span></span>

<span data-ttu-id="7b424-843">明細行</span><span class="sxs-lookup"><span data-stu-id="7b424-843">lines</span></span>  

<!-- -->

<span data-ttu-id="7b424-844">文字列</span><span class="sxs-lookup"><span data-stu-id="7b424-844">string</span></span>  

### <a name="return-value---setheightgettext"></a><span data-ttu-id="7b424-845">戻り値 - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="7b424-845">Return Value - setHeightGetText</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="7b424-846">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="7b424-846">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="7b424-847">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="7b424-847">Parameters - showLabel</span></span>

<span data-ttu-id="7b424-848">値</span><span class="sxs-lookup"><span data-stu-id="7b424-848">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="7b424-849">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="7b424-849">Return Value - showLabel</span></span>

## <a name="method-showzero"></a><span data-ttu-id="7b424-850">メソッド showZero</span><span class="sxs-lookup"><span data-stu-id="7b424-850">Method showZero</span></span>

```xpp
public int showZero([int value])
```

### <a name="parameters---showzero"></a><span data-ttu-id="7b424-851">パラメーター - showZero</span><span class="sxs-lookup"><span data-stu-id="7b424-851">Parameters - showZero</span></span>

<span data-ttu-id="7b424-852">値</span><span class="sxs-lookup"><span data-stu-id="7b424-852">value</span></span>  

### <a name="return-value---showzero"></a><span data-ttu-id="7b424-853">戻り値 - showZero</span><span class="sxs-lookup"><span data-stu-id="7b424-853">Return Value - showZero</span></span>

## <a name="method-signdisplay"></a><span data-ttu-id="7b424-854">メソッド signDisplay</span><span class="sxs-lookup"><span data-stu-id="7b424-854">Method signDisplay</span></span>

```xpp
public int signDisplay([int value])
```

### <a name="parameters---signdisplay"></a><span data-ttu-id="7b424-855">パラメーター - signDisplay</span><span class="sxs-lookup"><span data-stu-id="7b424-855">Parameters - signDisplay</span></span>

<span data-ttu-id="7b424-856">値</span><span class="sxs-lookup"><span data-stu-id="7b424-856">value</span></span>  

### <a name="return-value---signdisplay"></a><span data-ttu-id="7b424-857">戻り値 - signDisplay</span><span class="sxs-lookup"><span data-stu-id="7b424-857">Return Value - signDisplay</span></span>

## <a name="method-sumall"></a><span data-ttu-id="7b424-858">メソッド sumAll</span><span class="sxs-lookup"><span data-stu-id="7b424-858">Method sumAll</span></span>

```xpp
public boolean sumAll([boolean value])
```

### <a name="parameters---sumall"></a><span data-ttu-id="7b424-859">パラメーター - sumAll</span><span class="sxs-lookup"><span data-stu-id="7b424-859">Parameters - sumAll</span></span>

<span data-ttu-id="7b424-860">値</span><span class="sxs-lookup"><span data-stu-id="7b424-860">value</span></span>  

### <a name="return-value---sumall"></a><span data-ttu-id="7b424-861">戻り値 - sumAll</span><span class="sxs-lookup"><span data-stu-id="7b424-861">Return Value - sumAll</span></span>

## <a name="method-sumneg"></a><span data-ttu-id="7b424-862">メソッド sumNeg</span><span class="sxs-lookup"><span data-stu-id="7b424-862">Method sumNeg</span></span>

```xpp
public boolean sumNeg([boolean value])
```

### <a name="parameters---sumneg"></a><span data-ttu-id="7b424-863">パラメーター - sumNeg</span><span class="sxs-lookup"><span data-stu-id="7b424-863">Parameters - sumNeg</span></span>

<span data-ttu-id="7b424-864">値</span><span class="sxs-lookup"><span data-stu-id="7b424-864">value</span></span>  

### <a name="return-value---sumneg"></a><span data-ttu-id="7b424-865">戻り値 - sumNeg</span><span class="sxs-lookup"><span data-stu-id="7b424-865">Return Value - sumNeg</span></span>

## <a name="method-sumpos"></a><span data-ttu-id="7b424-866">メソッド sumPos</span><span class="sxs-lookup"><span data-stu-id="7b424-866">Method sumPos</span></span>

```xpp
public boolean sumPos([boolean value])
```

### <a name="parameters---sumpos"></a><span data-ttu-id="7b424-867">パラメーター - sumPos</span><span class="sxs-lookup"><span data-stu-id="7b424-867">Parameters - sumPos</span></span>

<span data-ttu-id="7b424-868">値</span><span class="sxs-lookup"><span data-stu-id="7b424-868">value</span></span>  

### <a name="return-value---sumpos"></a><span data-ttu-id="7b424-869">戻り値 - sumPos</span><span class="sxs-lookup"><span data-stu-id="7b424-869">Return Value - sumPos</span></span>

## <a name="method-table"></a><span data-ttu-id="7b424-870">メソッド table</span><span class="sxs-lookup"><span data-stu-id="7b424-870">Method table</span></span>

<span data-ttu-id="7b424-871">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-871">Gets or sets the table ID associated with the object.</span></span>

```xpp
public TableId table([TableId value])
```

### <a name="parameters---table"></a><span data-ttu-id="7b424-872">パラメーター - table</span><span class="sxs-lookup"><span data-stu-id="7b424-872">Parameters - table</span></span>

<span data-ttu-id="7b424-873">値</span><span class="sxs-lookup"><span data-stu-id="7b424-873">value</span></span>  

### <a name="return-value---table"></a><span data-ttu-id="7b424-874">戻り値 - toBlob</span><span class="sxs-lookup"><span data-stu-id="7b424-874">Return Value - table</span></span>

<span data-ttu-id="7b424-875">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="7b424-875">The current value of the table ID associated with the object.</span></span>

## <a name="method-thickness"></a><span data-ttu-id="7b424-876">メソッド thickness</span><span class="sxs-lookup"><span data-stu-id="7b424-876">Method thickness</span></span>

```xpp
public LineThickness thickness([LineThickness value])
```

### <a name="parameters---thickness"></a><span data-ttu-id="7b424-877">パラメーター - thickness</span><span class="sxs-lookup"><span data-stu-id="7b424-877">Parameters - thickness</span></span>

<span data-ttu-id="7b424-878">値</span><span class="sxs-lookup"><span data-stu-id="7b424-878">value</span></span>  

### <a name="return-value---thickness"></a><span data-ttu-id="7b424-879">戻り値 - thickness</span><span class="sxs-lookup"><span data-stu-id="7b424-879">Return Value - thickness</span></span>

## <a name="method-thousandseparator"></a><span data-ttu-id="7b424-880">メソッド thousandSeparator</span><span class="sxs-lookup"><span data-stu-id="7b424-880">Method thousandSeparator</span></span>

```xpp
public int thousandSeparator([int value])
```

### <a name="parameters---thousandseparator"></a><span data-ttu-id="7b424-881">パラメーター - thousandSeparator</span><span class="sxs-lookup"><span data-stu-id="7b424-881">Parameters - thousandSeparator</span></span>

<span data-ttu-id="7b424-882">値</span><span class="sxs-lookup"><span data-stu-id="7b424-882">value</span></span>  

### <a name="return-value---thousandseparator"></a><span data-ttu-id="7b424-883">戻り値 - thousandSeparator</span><span class="sxs-lookup"><span data-stu-id="7b424-883">Return Value - thousandSeparator</span></span>

## <a name="method-top100mm"></a><span data-ttu-id="7b424-884">メソッド top100mm</span><span class="sxs-lookup"><span data-stu-id="7b424-884">Method top100mm</span></span>

```xpp
public int top100mm([int topExclBorder])
```

### <a name="parameters---top100mm"></a><span data-ttu-id="7b424-885">パラメーター - top100mm</span><span class="sxs-lookup"><span data-stu-id="7b424-885">Parameters - top100mm</span></span>

<span data-ttu-id="7b424-886">topExclBorder</span><span class="sxs-lookup"><span data-stu-id="7b424-886">topExclBorder</span></span>  

### <a name="return-value---top100mm"></a><span data-ttu-id="7b424-887">戻り値 - top100mm</span><span class="sxs-lookup"><span data-stu-id="7b424-887">Return Value - top100mm</span></span>

## <a name="method-top100mminclborder"></a><span data-ttu-id="7b424-888">メソッド top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="7b424-888">Method top100mmInclBorder</span></span>

```xpp
public int top100mmInclBorder([int topInclBorder])
```

### <a name="parameters---top100mminclborder"></a><span data-ttu-id="7b424-889">パラメーター - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="7b424-889">Parameters - top100mmInclBorder</span></span>

<span data-ttu-id="7b424-890">topInclBorder</span><span class="sxs-lookup"><span data-stu-id="7b424-890">topInclBorder</span></span>  

### <a name="return-value---top100mminclborder"></a><span data-ttu-id="7b424-891">戻り値 - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="7b424-891">Return Value - top100mmInclBorder</span></span>

## <a name="method-topmarginandframe"></a><span data-ttu-id="7b424-892">メソッド topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="7b424-892">Method topMarginAndFrame</span></span>

```xpp
public int topMarginAndFrame()
```

### <a name="return-value---topmarginandframe"></a><span data-ttu-id="7b424-893">戻り値 - topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="7b424-893">Return Value - topMarginAndFrame</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="7b424-894">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="7b424-894">Method topMarginMode</span></span>

```xpp
public int topMarginMode([int value])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="7b424-895">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="7b424-895">Parameters - topMarginMode</span></span>

<span data-ttu-id="7b424-896">値</span><span class="sxs-lookup"><span data-stu-id="7b424-896">value</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="7b424-897">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="7b424-897">Return Value - topMarginMode</span></span>

## <a name="method-topmarginstr"></a><span data-ttu-id="7b424-898">メソッド topMarginStr</span><span class="sxs-lookup"><span data-stu-id="7b424-898">Method topMarginStr</span></span>

```xpp
public str topMarginStr([str value])
```

### <a name="parameters---topmarginstr"></a><span data-ttu-id="7b424-899">パラメーター - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="7b424-899">Parameters - topMarginStr</span></span>

<span data-ttu-id="7b424-900">値</span><span class="sxs-lookup"><span data-stu-id="7b424-900">value</span></span>  

### <a name="return-value---topmarginstr"></a><span data-ttu-id="7b424-901">戻り値 - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="7b424-901">Return Value - topMarginStr</span></span>

## <a name="method-topmarginunit"></a><span data-ttu-id="7b424-902">メソッド topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-902">Method topMarginUnit</span></span>

```xpp
public Units topMarginUnit([Units value])
```

### <a name="parameters---topmarginunit"></a><span data-ttu-id="7b424-903">パラメーター - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-903">Parameters - topMarginUnit</span></span>

<span data-ttu-id="7b424-904">値</span><span class="sxs-lookup"><span data-stu-id="7b424-904">value</span></span>  

### <a name="return-value---topmarginunit"></a><span data-ttu-id="7b424-905">戻り値 - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-905">Return Value - topMarginUnit</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="7b424-906">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="7b424-906">Method topMarginValue</span></span>

```xpp
public Real topMarginValue([Real value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="7b424-907">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="7b424-907">Parameters - topMarginValue</span></span>

<span data-ttu-id="7b424-908">値</span><span class="sxs-lookup"><span data-stu-id="7b424-908">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="7b424-909">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="7b424-909">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="7b424-910">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="7b424-910">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="7b424-911">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="7b424-911">Parameters - topMode</span></span>

<span data-ttu-id="7b424-912">値</span><span class="sxs-lookup"><span data-stu-id="7b424-912">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="7b424-913">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="7b424-913">Return Value - topMode</span></span>

## <a name="method-topstr"></a><span data-ttu-id="7b424-914">メソッド topStr</span><span class="sxs-lookup"><span data-stu-id="7b424-914">Method topStr</span></span>

```xpp
public str topStr([str value])
```

### <a name="parameters---topstr"></a><span data-ttu-id="7b424-915">パラメーター - topStr</span><span class="sxs-lookup"><span data-stu-id="7b424-915">Parameters - topStr</span></span>

<span data-ttu-id="7b424-916">値</span><span class="sxs-lookup"><span data-stu-id="7b424-916">value</span></span>  

### <a name="return-value---topstr"></a><span data-ttu-id="7b424-917">戻り値 - topStr</span><span class="sxs-lookup"><span data-stu-id="7b424-917">Return Value - topStr</span></span>

## <a name="method-topunit"></a><span data-ttu-id="7b424-918">メソッド topUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-918">Method topUnit</span></span>

```xpp
public Units topUnit([Units value])
```

### <a name="parameters---topunit"></a><span data-ttu-id="7b424-919">パラメーター - topUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-919">Parameters - topUnit</span></span>

<span data-ttu-id="7b424-920">値</span><span class="sxs-lookup"><span data-stu-id="7b424-920">value</span></span>  

### <a name="return-value---topunit"></a><span data-ttu-id="7b424-921">戻り値 - topUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-921">Return Value - topUnit</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="7b424-922">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="7b424-922">Method topValue</span></span>

```xpp
public Real topValue([Real value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="7b424-923">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="7b424-923">Parameters - topValue</span></span>

<span data-ttu-id="7b424-924">値</span><span class="sxs-lookup"><span data-stu-id="7b424-924">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="7b424-925">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="7b424-925">Return Value - topValue</span></span>

## <a name="method-underline"></a><span data-ttu-id="7b424-926">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="7b424-926">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="7b424-927">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="7b424-927">Parameters - underline</span></span>

<span data-ttu-id="7b424-928">値</span><span class="sxs-lookup"><span data-stu-id="7b424-928">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="7b424-929">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="7b424-929">Return Value - underline</span></span>

## <a name="method-visible"></a><span data-ttu-id="7b424-930">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="7b424-930">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="7b424-931">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="7b424-931">Parameters - visible</span></span>

<span data-ttu-id="7b424-932">値</span><span class="sxs-lookup"><span data-stu-id="7b424-932">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="7b424-933">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="7b424-933">Return Value - visible</span></span>

## <a name="method-webmenuitemname"></a><span data-ttu-id="7b424-934">メソッド webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="7b424-934">Method webMenuItemName</span></span>

```xpp
public str webMenuItemName([str value])
```

### <a name="parameters---webmenuitemname"></a><span data-ttu-id="7b424-935">パラメーター - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="7b424-935">Parameters - webMenuItemName</span></span>

<span data-ttu-id="7b424-936">値</span><span class="sxs-lookup"><span data-stu-id="7b424-936">value</span></span>  

### <a name="return-value---webmenuitemname"></a><span data-ttu-id="7b424-937">戻り値 - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="7b424-937">Return Value - webMenuItemName</span></span>

## <a name="method-webmenuitemtype"></a><span data-ttu-id="7b424-938">メソッド webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="7b424-938">Method webMenuItemType</span></span>

```xpp
public WebMenuItemType webMenuItemType([WebMenuItemType value])
```

### <a name="parameters---webmenuitemtype"></a><span data-ttu-id="7b424-939">パラメーター - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="7b424-939">Parameters - webMenuItemType</span></span>

<span data-ttu-id="7b424-940">値</span><span class="sxs-lookup"><span data-stu-id="7b424-940">value</span></span>  

### <a name="return-value---webmenuitemtype"></a><span data-ttu-id="7b424-941">戻り値 - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="7b424-941">Return Value - webMenuItemType</span></span>

## <a name="method-webtarget"></a><span data-ttu-id="7b424-942">メソッド webTarget</span><span class="sxs-lookup"><span data-stu-id="7b424-942">Method webTarget</span></span>

```xpp
public str webTarget([str value])
```

### <a name="parameters---webtarget"></a><span data-ttu-id="7b424-943">パラメーター - webTarget</span><span class="sxs-lookup"><span data-stu-id="7b424-943">Parameters - webTarget</span></span>

<span data-ttu-id="7b424-944">値</span><span class="sxs-lookup"><span data-stu-id="7b424-944">value</span></span>  

### <a name="return-value---webtarget"></a><span data-ttu-id="7b424-945">戻り値 - webTarget</span><span class="sxs-lookup"><span data-stu-id="7b424-945">Return Value - webTarget</span></span>

## <a name="method-width100mm"></a><span data-ttu-id="7b424-946">メソッド width100mm</span><span class="sxs-lookup"><span data-stu-id="7b424-946">Method width100mm</span></span>

```xpp
public int width100mm([int widthExclBorder])
```

### <a name="parameters---width100mm"></a><span data-ttu-id="7b424-947">パラメーター - width100mm</span><span class="sxs-lookup"><span data-stu-id="7b424-947">Parameters - width100mm</span></span>

<span data-ttu-id="7b424-948">widthExclBorder</span><span class="sxs-lookup"><span data-stu-id="7b424-948">widthExclBorder</span></span>  

### <a name="return-value---width100mm"></a><span data-ttu-id="7b424-949">戻り値 - width100mm</span><span class="sxs-lookup"><span data-stu-id="7b424-949">Return Value - width100mm</span></span>

## <a name="method-width100mminclborder"></a><span data-ttu-id="7b424-950">メソッド width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="7b424-950">Method width100mmInclBorder</span></span>

```xpp
public int width100mmInclBorder([int widthInclBorder])
```

### <a name="parameters---width100mminclborder"></a><span data-ttu-id="7b424-951">パラメーター - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="7b424-951">Parameters - width100mmInclBorder</span></span>

<span data-ttu-id="7b424-952">widthInclBorder</span><span class="sxs-lookup"><span data-stu-id="7b424-952">widthInclBorder</span></span>  

### <a name="return-value---width100mminclborder"></a><span data-ttu-id="7b424-953">戻り値 - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="7b424-953">Return Value - width100mmInclBorder</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="7b424-954">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="7b424-954">Method widthMode</span></span>

<span data-ttu-id="7b424-955">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-955">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="7b424-956">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="7b424-956">Parameters - widthMode</span></span>

<span data-ttu-id="7b424-957">値</span><span class="sxs-lookup"><span data-stu-id="7b424-957">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="7b424-958">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="7b424-958">Return Value - widthMode</span></span>

<span data-ttu-id="7b424-959">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="7b424-959">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="7b424-960">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="7b424-960">Remarks - widthMode</span></span>

<span data-ttu-id="7b424-961">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="7b424-961">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="7b424-962">モード。</span><span class="sxs-lookup"><span data-stu-id="7b424-962">Mode.</span></span>         | <span data-ttu-id="7b424-963">幅計算。</span><span class="sxs-lookup"><span data-stu-id="7b424-963">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b424-964">正確。</span><span class="sxs-lookup"><span data-stu-id="7b424-964">Exact.</span></span>        | <span data-ttu-id="7b424-965">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="7b424-965">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="7b424-966">自動。</span><span class="sxs-lookup"><span data-stu-id="7b424-966">Auto.</span></span>         | <span data-ttu-id="7b424-967">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="7b424-967">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="7b424-968">列の幅。</span><span class="sxs-lookup"><span data-stu-id="7b424-968">Column width.</span></span> | <span data-ttu-id="7b424-969">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="7b424-969">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="7b424-970">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="7b424-970">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthofstring100mm"></a><span data-ttu-id="7b424-971">メソッド widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="7b424-971">Method widthOfString100mm</span></span>

```xpp
public int widthOfString100mm(str string)
```

### <a name="parameters---widthofstring100mm"></a><span data-ttu-id="7b424-972">パラメーター - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="7b424-972">Parameters - widthOfString100mm</span></span>

<span data-ttu-id="7b424-973">文字列</span><span class="sxs-lookup"><span data-stu-id="7b424-973">string</span></span>  

### <a name="return-value---widthofstring100mm"></a><span data-ttu-id="7b424-974">戻り値 - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="7b424-974">Return Value - widthOfString100mm</span></span>

## <a name="method-widthstr"></a><span data-ttu-id="7b424-975">メソッド widthStr</span><span class="sxs-lookup"><span data-stu-id="7b424-975">Method widthStr</span></span>

```xpp
public str widthStr([str value])
```

### <a name="parameters---widthstr"></a><span data-ttu-id="7b424-976">パラメーター - widthStr</span><span class="sxs-lookup"><span data-stu-id="7b424-976">Parameters - widthStr</span></span>

<span data-ttu-id="7b424-977">値</span><span class="sxs-lookup"><span data-stu-id="7b424-977">value</span></span>  

### <a name="return-value---widthstr"></a><span data-ttu-id="7b424-978">戻り値 - widthStr</span><span class="sxs-lookup"><span data-stu-id="7b424-978">Return Value - widthStr</span></span>

## <a name="method-widthunit"></a><span data-ttu-id="7b424-979">メソッド widthUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-979">Method widthUnit</span></span>

```xpp
public Units widthUnit([Units value])
```

### <a name="parameters---widthunit"></a><span data-ttu-id="7b424-980">パラメーター - widthUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-980">Parameters - widthUnit</span></span>

<span data-ttu-id="7b424-981">値</span><span class="sxs-lookup"><span data-stu-id="7b424-981">value</span></span>  

### <a name="return-value---widthunit"></a><span data-ttu-id="7b424-982">戻り値 - widthUnit</span><span class="sxs-lookup"><span data-stu-id="7b424-982">Return Value - widthUnit</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="7b424-983">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="7b424-983">Method widthValue</span></span>

<span data-ttu-id="7b424-984">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-984">Gets or sets the width of the control.</span></span>

```xpp
public Real widthValue([Real value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="7b424-985">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="7b424-985">Parameters - widthValue</span></span>

<span data-ttu-id="7b424-986">値</span><span class="sxs-lookup"><span data-stu-id="7b424-986">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="7b424-987">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="7b424-987">Return Value - widthValue</span></span>

<span data-ttu-id="7b424-988">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="7b424-988">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="7b424-989">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="7b424-989">Remarks - widthValue</span></span>

<span data-ttu-id="7b424-990">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="7b424-990">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-show"></a><span data-ttu-id="7b424-991">メソッド show</span><span class="sxs-lookup"><span data-stu-id="7b424-991">Method show</span></span>

```xpp
public void show()
```

## <a name="method-hide"></a><span data-ttu-id="7b424-992">メソッド hide</span><span class="sxs-lookup"><span data-stu-id="7b424-992">Method hide</span></span>

```xpp
public void hide()
```

## <a name="method-height"></a><span data-ttu-id="7b424-993">メソッド height</span><span class="sxs-lookup"><span data-stu-id="7b424-993">Method height</span></span>

<span data-ttu-id="7b424-994">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-994">Gets or sets the height of the control.</span></span>

```xpp
public void height(Real value, Units unit)
```

### <a name="parameters---height"></a><span data-ttu-id="7b424-995">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="7b424-995">Parameters - height</span></span>

<span data-ttu-id="7b424-996">値</span><span class="sxs-lookup"><span data-stu-id="7b424-996">value</span></span>  

<!-- -->

<span data-ttu-id="7b424-997">単位</span><span class="sxs-lookup"><span data-stu-id="7b424-997">unit</span></span>  

### <a name="remarks---height"></a><span data-ttu-id="7b424-998">備考 - height</span><span class="sxs-lookup"><span data-stu-id="7b424-998">Remarks - height</span></span>

<span data-ttu-id="7b424-999">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="7b424-999">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="7b424-1000">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="7b424-1000">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="7b424-1001">モード。</span><span class="sxs-lookup"><span data-stu-id="7b424-1001">Mode.</span></span>            | <span data-ttu-id="7b424-1002">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="7b424-1002">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b424-1003">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="7b424-1003">-1 Exact.</span></span>        | <span data-ttu-id="7b424-1004">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="7b424-1004">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="7b424-1005">0 自動。</span><span class="sxs-lookup"><span data-stu-id="7b424-1005">0 Auto.</span></span>          | <span data-ttu-id="7b424-1006">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="7b424-1006">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="7b424-1007">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="7b424-1007">1 Column height.</span></span> | <span data-ttu-id="7b424-1008">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="7b424-1008">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="7b424-1009">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="7b424-1009">The height and height calculation mode can be set separately.</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="7b424-1010">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="7b424-1010">Method rightMargin</span></span>

```xpp
public void rightMargin(Real value, Units unit)
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="7b424-1011">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="7b424-1011">Parameters - rightMargin</span></span>

<span data-ttu-id="7b424-1012">値</span><span class="sxs-lookup"><span data-stu-id="7b424-1012">value</span></span>  

<!-- -->

<span data-ttu-id="7b424-1013">単位</span><span class="sxs-lookup"><span data-stu-id="7b424-1013">unit</span></span>  

## <a name="method-left"></a><span data-ttu-id="7b424-1014">メソッド left</span><span class="sxs-lookup"><span data-stu-id="7b424-1014">Method left</span></span>

```xpp
public void left(Real value, Units unit)
```

### <a name="parameters---left"></a><span data-ttu-id="7b424-1015">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="7b424-1015">Parameters - left</span></span>

<span data-ttu-id="7b424-1016">値</span><span class="sxs-lookup"><span data-stu-id="7b424-1016">value</span></span>  

<!-- -->

<span data-ttu-id="7b424-1017">単位</span><span class="sxs-lookup"><span data-stu-id="7b424-1017">unit</span></span>  

## <a name="method-width"></a><span data-ttu-id="7b424-1018">メソッド width</span><span class="sxs-lookup"><span data-stu-id="7b424-1018">Method width</span></span>

<span data-ttu-id="7b424-1019">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="7b424-1019">Gets or sets the width of the control.</span></span>

```xpp
public void width(Real value, Units unit)
```

### <a name="parameters---width"></a><span data-ttu-id="7b424-1020">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="7b424-1020">Parameters - width</span></span>

<span data-ttu-id="7b424-1021">値</span><span class="sxs-lookup"><span data-stu-id="7b424-1021">value</span></span>  

<!-- -->

<span data-ttu-id="7b424-1022">単位</span><span class="sxs-lookup"><span data-stu-id="7b424-1022">unit</span></span>  

### <a name="remarks---width"></a><span data-ttu-id="7b424-1023">備考 - width</span><span class="sxs-lookup"><span data-stu-id="7b424-1023">Remarks - width</span></span>

<span data-ttu-id="7b424-1024">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="7b424-1024">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="7b424-1025">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="7b424-1025">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="7b424-1026">モード。</span><span class="sxs-lookup"><span data-stu-id="7b424-1026">Mode.</span></span>           | <span data-ttu-id="7b424-1027">幅計算。</span><span class="sxs-lookup"><span data-stu-id="7b424-1027">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b424-1028">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="7b424-1028">-1 Exact.</span></span>       | <span data-ttu-id="7b424-1029">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="7b424-1029">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="7b424-1030">0 自動。</span><span class="sxs-lookup"><span data-stu-id="7b424-1030">0 Auto.</span></span>         | <span data-ttu-id="7b424-1031">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="7b424-1031">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="7b424-1032">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="7b424-1032">1 Column width.</span></span> | <span data-ttu-id="7b424-1033">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="7b424-1033">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="7b424-1034">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="7b424-1034">The width and width calculation mode can be set separately.</span></span>

## <a name="method-extrasumwidth"></a><span data-ttu-id="7b424-1035">メソッド extraSumWidth</span><span class="sxs-lookup"><span data-stu-id="7b424-1035">Method extraSumWidth</span></span>

```xpp
public void extraSumWidth(Real value, Units unit)
```

### <a name="parameters---extrasumwidth"></a><span data-ttu-id="7b424-1036">パラメーター - extraSumWidth</span><span class="sxs-lookup"><span data-stu-id="7b424-1036">Parameters - extraSumWidth</span></span>

<span data-ttu-id="7b424-1037">値</span><span class="sxs-lookup"><span data-stu-id="7b424-1037">value</span></span>  

<!-- -->

<span data-ttu-id="7b424-1038">単位</span><span class="sxs-lookup"><span data-stu-id="7b424-1038">unit</span></span>  

## <a name="method-topmargin"></a><span data-ttu-id="7b424-1039">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="7b424-1039">Method topMargin</span></span>

```xpp
public void topMargin(Real value, Units unit)
```

### <a name="parameters---topmargin"></a><span data-ttu-id="7b424-1040">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="7b424-1040">Parameters - topMargin</span></span>

<span data-ttu-id="7b424-1041">値</span><span class="sxs-lookup"><span data-stu-id="7b424-1041">value</span></span>  

<!-- -->

<span data-ttu-id="7b424-1042">単位</span><span class="sxs-lookup"><span data-stu-id="7b424-1042">unit</span></span>  

## <a name="method-leftmargin"></a><span data-ttu-id="7b424-1043">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="7b424-1043">Method leftMargin</span></span>

```xpp
public void leftMargin(Real value, Units unit)
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="7b424-1044">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="7b424-1044">Parameters - leftMargin</span></span>

<span data-ttu-id="7b424-1045">値</span><span class="sxs-lookup"><span data-stu-id="7b424-1045">value</span></span>  

<!-- -->

<span data-ttu-id="7b424-1046">単位</span><span class="sxs-lookup"><span data-stu-id="7b424-1046">unit</span></span>  

## <a name="method-labelwidth"></a><span data-ttu-id="7b424-1047">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="7b424-1047">Method labelWidth</span></span>

```xpp
public void labelWidth(Real value, Units unit)
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="7b424-1048">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="7b424-1048">Parameters - labelWidth</span></span>

<span data-ttu-id="7b424-1049">値</span><span class="sxs-lookup"><span data-stu-id="7b424-1049">value</span></span>  

<!-- -->

<span data-ttu-id="7b424-1050">単位</span><span class="sxs-lookup"><span data-stu-id="7b424-1050">unit</span></span>  

## <a name="method-top"></a><span data-ttu-id="7b424-1051">メソッド top</span><span class="sxs-lookup"><span data-stu-id="7b424-1051">Method top</span></span>

```xpp
public void top(Real value, Units unit)
```

### <a name="parameters---top"></a><span data-ttu-id="7b424-1052">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="7b424-1052">Parameters - top</span></span>

<span data-ttu-id="7b424-1053">値</span><span class="sxs-lookup"><span data-stu-id="7b424-1053">value</span></span>  

<!-- -->

<span data-ttu-id="7b424-1054">単位</span><span class="sxs-lookup"><span data-stu-id="7b424-1054">unit</span></span>  

## <a name="method-bottommargin"></a><span data-ttu-id="7b424-1055">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="7b424-1055">Method bottomMargin</span></span>

```xpp
public void bottomMargin(Real value, Units unit)
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="7b424-1056">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="7b424-1056">Parameters - bottomMargin</span></span>

<span data-ttu-id="7b424-1057">値</span><span class="sxs-lookup"><span data-stu-id="7b424-1057">value</span></span>  

<!-- -->

<span data-ttu-id="7b424-1058">単位</span><span class="sxs-lookup"><span data-stu-id="7b424-1058">unit</span></span>  

