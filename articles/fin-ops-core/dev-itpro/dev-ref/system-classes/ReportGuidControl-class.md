---
title: ReportGuidControl クラス
description: このトピックでは、ReportGuidControl クラスについて説明します。
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
ms.openlocfilehash: 82115b0404bfa7975b2fa646d44d97ca276b83a8
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502842"
---
# <a name="class-reportguidcontrol"></a><span data-ttu-id="b5d86-103">クラス ReportGuidControl</span><span class="sxs-lookup"><span data-stu-id="b5d86-103">Class ReportGuidControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ReportGuidControl extends ReportControl
```

<span data-ttu-id="b5d86-104">ReportGuidControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="b5d86-104">The ReportGuidControl class enables you to create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5d86-105">備考</span><span class="sxs-lookup"><span data-stu-id="b5d86-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="b5d86-106">例</span><span class="sxs-lookup"><span data-stu-id="b5d86-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="b5d86-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="b5d86-107">Methods</span></span>

| <span data-ttu-id="b5d86-108">方法</span><span class="sxs-lookup"><span data-stu-id="b5d86-108">Method</span></span>                                                                   | <span data-ttu-id="b5d86-109">説明</span><span class="sxs-lookup"><span data-stu-id="b5d86-109">Description</span></span>                                                                                                                                   |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d86-110">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-110">public int alignment(\[int value\])</span></span>                                      |                                                                                                                                               |
| <span data-ttu-id="b5d86-111">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-111">public int arrayIndex(\[int value\])</span></span>                                     |                                                                                                                                               |
| <span data-ttu-id="b5d86-112">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-112">public boolean autoDeclaration(\[boolean value\])</span></span>                        | <span data-ttu-id="b5d86-113">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-113">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                            |
| <span data-ttu-id="b5d86-114">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-114">public int backgroundColor(\[int value\])</span></span>                                | <span data-ttu-id="b5d86-115">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-115">Gets or sets the background color of the control.</span></span>                                                                                             |
| <span data-ttu-id="b5d86-116">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-116">public int backStyle(\[int value\])</span></span>                                      | <span data-ttu-id="b5d86-117">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-117">Determines whether the control background can be transparent.</span></span>                                                                                |
| <span data-ttu-id="b5d86-118">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-118">public int bold(\[int value\])</span></span>                                           | <span data-ttu-id="b5d86-119">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-119">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                                   |
| <span data-ttu-id="b5d86-120">public int bottomMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="b5d86-120">public int bottomMarginAndFrame()</span></span>                                        |                                                                                                                                               |
| <span data-ttu-id="b5d86-121">public int bottomMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-121">public int bottomMarginMode(\[int value\])</span></span>                               |                                                                                                                                               |
| <span data-ttu-id="b5d86-122">public str bottomMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-122">public str bottomMarginStr(\[str value\])</span></span>                                |                                                                                                                                               |
| <span data-ttu-id="b5d86-123">public Units bottomMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-123">public Units bottomMarginUnit(\[Units value\])</span></span>                           |                                                                                                                                               |
| <span data-ttu-id="b5d86-124">public Real bottomMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-124">public Real bottomMarginValue(\[Real value\])</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="b5d86-125">public int changeLabelCase(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-125">public int changeLabelCase(\[int value\])</span></span>                                |                                                                                                                                               |
| <span data-ttu-id="b5d86-126">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-126">public int characterSet(\[int value\])</span></span>                                   | <span data-ttu-id="b5d86-127">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-127">Gets or sets the character set of the font.</span></span>                                                                                                   |
| <span data-ttu-id="b5d86-128">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-128">public int colorScheme(\[int value\])</span></span>                                    | <span data-ttu-id="b5d86-129">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-129">Gets or sets the color scheme of the control.</span></span>                                                                                                 |
| <span data-ttu-id="b5d86-130">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-130">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="b5d86-131">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-131">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                           |
| <span data-ttu-id="b5d86-132">public ReportFieldType controlType()</span><span class="sxs-lookup"><span data-stu-id="b5d86-132">public ReportFieldType controlType()</span></span>                                     |                                                                                                                                               |
| <span data-ttu-id="b5d86-133">public str cssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-133">public str cssClass(\[str value\])</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="b5d86-134">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-134">public FieldId dataField(\[FieldId value\])</span></span>                              |                                                                                                                                               |
| <span data-ttu-id="b5d86-135">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-135">public str dataMethod(\[str value\])</span></span>                                     |                                                                                                                                               |
| <span data-ttu-id="b5d86-136">public int delete()</span><span class="sxs-lookup"><span data-stu-id="b5d86-136">public int delete()</span></span>                                                      |                                                                                                                                               |
| <span data-ttu-id="b5d86-137">public str effectiveFont()</span><span class="sxs-lookup"><span data-stu-id="b5d86-137">public str effectiveFont()</span></span>                                               |                                                                                                                                               |
| <span data-ttu-id="b5d86-138">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-138">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>         |                                                                                                                                               |
| <span data-ttu-id="b5d86-139">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-139">public str font(\[str value\])</span></span>                                           | <span data-ttu-id="b5d86-140">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-140">Gets or sets the name of the font for the control to use.</span></span>                                                                                     |
| <span data-ttu-id="b5d86-141">public str fontInfoPrinter()</span><span class="sxs-lookup"><span data-stu-id="b5d86-141">public str fontInfoPrinter()</span></span>                                             |                                                                                                                                               |
| <span data-ttu-id="b5d86-142">public int fontInfoPrinterAscent()</span><span class="sxs-lookup"><span data-stu-id="b5d86-142">public int fontInfoPrinterAscent()</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="b5d86-143">public int fontInfoPrinterDescent()</span><span class="sxs-lookup"><span data-stu-id="b5d86-143">public int fontInfoPrinterDescent()</span></span>                                      |                                                                                                                                               |
| <span data-ttu-id="b5d86-144">public int fontInfoPrinterExtLead()</span><span class="sxs-lookup"><span data-stu-id="b5d86-144">public int fontInfoPrinterExtLead()</span></span>                                      |                                                                                                                                               |
| <span data-ttu-id="b5d86-145">public int fontInfoPrinterHeight()</span><span class="sxs-lookup"><span data-stu-id="b5d86-145">public int fontInfoPrinterHeight()</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="b5d86-146">public int fontInfoPrinterIntLead()</span><span class="sxs-lookup"><span data-stu-id="b5d86-146">public int fontInfoPrinterIntLead()</span></span>                                      |                                                                                                                                               |
| <span data-ttu-id="b5d86-147">public str fontInfoScreen()</span><span class="sxs-lookup"><span data-stu-id="b5d86-147">public str fontInfoScreen()</span></span>                                              |                                                                                                                                               |
| <span data-ttu-id="b5d86-148">public int fontInfoScreenAscent()</span><span class="sxs-lookup"><span data-stu-id="b5d86-148">public int fontInfoScreenAscent()</span></span>                                        |                                                                                                                                               |
| <span data-ttu-id="b5d86-149">public int fontInfoScreenDescent()</span><span class="sxs-lookup"><span data-stu-id="b5d86-149">public int fontInfoScreenDescent()</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="b5d86-150">public int fontInfoScreenExtLead()</span><span class="sxs-lookup"><span data-stu-id="b5d86-150">public int fontInfoScreenExtLead()</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="b5d86-151">public int fontInfoScreenHeight()</span><span class="sxs-lookup"><span data-stu-id="b5d86-151">public int fontInfoScreenHeight()</span></span>                                        |                                                                                                                                               |
| <span data-ttu-id="b5d86-152">public int fontInfoScreenIntLead()</span><span class="sxs-lookup"><span data-stu-id="b5d86-152">public int fontInfoScreenIntLead()</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="b5d86-153">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-153">public int fontSize(\[int value\])</span></span>                                       | <span data-ttu-id="b5d86-154">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-154">Gets or sets the size of the font for the control to use.</span></span>                                                                                     |
| <span data-ttu-id="b5d86-155">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-155">public int foregroundColor(\[int value\])</span></span>                                | <span data-ttu-id="b5d86-156">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-156">Gets or sets the text color for the control to use.</span></span>                                                                                           |
| <span data-ttu-id="b5d86-157">public int height100mm(\[int heightExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-157">public int height100mm(\[int heightExclBorder\])</span></span>                         |                                                                                                                                               |
| <span data-ttu-id="b5d86-158">public int height100mmInclBorder(\[int heightInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-158">public int height100mmInclBorder(\[int heightInclBorder\])</span></span>               |                                                                                                                                               |
| <span data-ttu-id="b5d86-159">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-159">public int heightMode(\[int value\])</span></span>                                     | <span data-ttu-id="b5d86-160">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-160">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                |
| <span data-ttu-id="b5d86-161">public int heightOfWordWrappedString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="b5d86-161">public int heightOfWordWrappedString100mm(str string)</span></span>                    |                                                                                                                                               |
| <span data-ttu-id="b5d86-162">public str heightStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-162">public str heightStr(\[str value\])</span></span>                                      |                                                                                                                                               |
| <span data-ttu-id="b5d86-163">public Units heightUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-163">public Units heightUnit(\[Units value\])</span></span>                                 |                                                                                                                                               |
| <span data-ttu-id="b5d86-164">public Real heightValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-164">public Real heightValue(\[Real value\])</span></span>                                  | <span data-ttu-id="b5d86-165">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-165">Gets or sets the height of the control.</span></span>                                                                                                       |
| <span data-ttu-id="b5d86-166">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-166">public boolean italic(\[boolean value\])</span></span>                                 |                                                                                                                                               |
| <span data-ttu-id="b5d86-167">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-167">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="b5d86-168">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-168">Gets or sets the label for a control.</span></span>                                                                                                         |
| <span data-ttu-id="b5d86-169">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-169">public int labelBold(\[int value\])</span></span>                                      |                                                                                                                                               |
| <span data-ttu-id="b5d86-170">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-170">public int labelCharacterSet(\[int value\])</span></span>                              |                                                                                                                                               |
| <span data-ttu-id="b5d86-171">public str labelCssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-171">public str labelCssClass(\[str value\])</span></span>                                  |                                                                                                                                               |
| <span data-ttu-id="b5d86-172">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-172">public str labelFont(\[str value\])</span></span>                                      |                                                                                                                                               |
| <span data-ttu-id="b5d86-173">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-173">public int labelFontSize(\[int value\])</span></span>                                  |                                                                                                                                               |
| <span data-ttu-id="b5d86-174">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-174">public boolean labelItalic(\[boolean value\])</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="b5d86-175">public LineType labelLineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-175">public LineType labelLineBelow(\[LineType value\])</span></span>                       |                                                                                                                                               |
| <span data-ttu-id="b5d86-176">public LineThickness labelLineThickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-176">public LineThickness labelLineThickness(\[LineThickness value\])</span></span>         |                                                                                                                                               |
| <span data-ttu-id="b5d86-177">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-177">public int labelPosition(\[int value\])</span></span>                                  |                                                                                                                                               |
| <span data-ttu-id="b5d86-178">public int labelTabLeader(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-178">public int labelTabLeader(\[int value\])</span></span>                                 |                                                                                                                                               |
| <span data-ttu-id="b5d86-179">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-179">public boolean labelUnderline(\[boolean value\])</span></span>                         |                                                                                                                                               |
| <span data-ttu-id="b5d86-180">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-180">public int labelWidthMode(\[int value\])</span></span>                                 |                                                                                                                                               |
| <span data-ttu-id="b5d86-181">public str labelWidthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-181">public str labelWidthStr(\[str value\])</span></span>                                  |                                                                                                                                               |
| <span data-ttu-id="b5d86-182">public Units labelWidthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-182">public Units labelWidthUnit(\[Units value\])</span></span>                             |                                                                                                                                               |
| <span data-ttu-id="b5d86-183">public Real labelWidthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-183">public Real labelWidthValue(\[Real value\])</span></span>                              |                                                                                                                                               |
| <span data-ttu-id="b5d86-184">public int left100mm(\[int leftExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-184">public int left100mm(\[int leftExclBorder\])</span></span>                             |                                                                                                                                               |
| <span data-ttu-id="b5d86-185">public int left100mmInclBorder(\[int leftInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-185">public int left100mmInclBorder(\[int leftInclBorder\])</span></span>                   |                                                                                                                                               |
| <span data-ttu-id="b5d86-186">public int leftMarginAnFrame()</span><span class="sxs-lookup"><span data-stu-id="b5d86-186">public int leftMarginAnFrame()</span></span>                                           |                                                                                                                                               |
| <span data-ttu-id="b5d86-187">public int leftMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-187">public int leftMarginMode(\[int value\])</span></span>                                 |                                                                                                                                               |
| <span data-ttu-id="b5d86-188">public str leftMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-188">public str leftMarginStr(\[str value\])</span></span>                                  |                                                                                                                                               |
| <span data-ttu-id="b5d86-189">public Units leftMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-189">public Units leftMarginUnit(\[Units value\])</span></span>                             |                                                                                                                                               |
| <span data-ttu-id="b5d86-190">public Real leftMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-190">public Real leftMarginValue(\[Real value\])</span></span>                              |                                                                                                                                               |
| <span data-ttu-id="b5d86-191">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-191">public int leftMode(\[int value\])</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="b5d86-192">public str leftStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-192">public str leftStr(\[str value\])</span></span>                                        |                                                                                                                                               |
| <span data-ttu-id="b5d86-193">public Units leftUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-193">public Units leftUnit(\[Units value\])</span></span>                                   |                                                                                                                                               |
| <span data-ttu-id="b5d86-194">public Real leftValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-194">public Real leftValue(\[Real value\])</span></span>                                    |                                                                                                                                               |
| <span data-ttu-id="b5d86-195">public LineType lineAbove(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-195">public LineType lineAbove(\[LineType value\])</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="b5d86-196">public LineType lineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-196">public LineType lineBelow(\[LineType value\])</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="b5d86-197">public LineType lineLeft(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-197">public LineType lineLeft(\[LineType value\])</span></span>                             | <span data-ttu-id="b5d86-198">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-198">Gets or sets the type of line that is used as the left border of a section.</span></span>                                                                   |
| <span data-ttu-id="b5d86-199">public LineType lineRight(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-199">public LineType lineRight(\[LineType value\])</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="b5d86-200">public str menuItemLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-200">public str menuItemLabel(\[str value\])</span></span>                                  |                                                                                                                                               |
| <span data-ttu-id="b5d86-201">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-201">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                                               |
| <span data-ttu-id="b5d86-202">public MenuItemType menuItemType(\[MenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-202">public MenuItemType menuItemType(\[MenuItemType value\])</span></span>                 |                                                                                                                                               |
| <span data-ttu-id="b5d86-203">public str modelFieldName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-203">public str modelFieldName(\[str value\])</span></span>                                 |                                                                                                                                               |
| <span data-ttu-id="b5d86-204">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-204">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="b5d86-205">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-205">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="b5d86-206">public int numberOfLines(int height100mm)</span><span class="sxs-lookup"><span data-stu-id="b5d86-206">public int numberOfLines(int height100mm)</span></span>                                |                                                                                                                                               |
| <span data-ttu-id="b5d86-207">public int position(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-207">public int position(\[int value\])</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="b5d86-208">public str previewInfo(str string)</span><span class="sxs-lookup"><span data-stu-id="b5d86-208">public str previewInfo(str string)</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="b5d86-209">public int previewXCompensation100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="b5d86-209">public int previewXCompensation100mm(str string)</span></span>                         |                                                                                                                                               |
| <span data-ttu-id="b5d86-210">public int right100mm()</span><span class="sxs-lookup"><span data-stu-id="b5d86-210">public int right100mm()</span></span>                                                  |                                                                                                                                               |
| <span data-ttu-id="b5d86-211">public int right100mmInclBorder()</span><span class="sxs-lookup"><span data-stu-id="b5d86-211">public int right100mmInclBorder()</span></span>                                        |                                                                                                                                               |
| <span data-ttu-id="b5d86-212">public int rightMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="b5d86-212">public int rightMarginAndFrame()</span></span>                                         |                                                                                                                                               |
| <span data-ttu-id="b5d86-213">public int rightMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-213">public int rightMarginMode(\[int value\])</span></span>                                |                                                                                                                                               |
| <span data-ttu-id="b5d86-214">public str rightMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-214">public str rightMarginStr(\[str value\])</span></span>                                 |                                                                                                                                               |
| <span data-ttu-id="b5d86-215">public Units rightMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-215">public Units rightMarginUnit(\[Units value\])</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="b5d86-216">public Real rightMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-216">public Real rightMarginValue(\[Real value\])</span></span>                             |                                                                                                                                               |
| <span data-ttu-id="b5d86-217">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-217">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                                               |
| <span data-ttu-id="b5d86-218">public str setHeightGetText(int lines, str string)</span><span class="sxs-lookup"><span data-stu-id="b5d86-218">public str setHeightGetText(int lines, str string)</span></span>                       |                                                                                                                                               |
| <span data-ttu-id="b5d86-219">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-219">public boolean showLabel(\[boolean value\])</span></span>                              |                                                                                                                                               |
| <span data-ttu-id="b5d86-220">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-220">public TableId table(\[TableId value\])</span></span>                                  | <span data-ttu-id="b5d86-221">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-221">Gets or sets the table ID associated with the object.</span></span>                                                                                         |
| <span data-ttu-id="b5d86-222">public LineThickness thickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-222">public LineThickness thickness(\[LineThickness value\])</span></span>                  |                                                                                                                                               |
| <span data-ttu-id="b5d86-223">public int top100mm(\[int topExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-223">public int top100mm(\[int topExclBorder\])</span></span>                               |                                                                                                                                               |
| <span data-ttu-id="b5d86-224">public int top100mmInclBorder(\[int topInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-224">public int top100mmInclBorder(\[int topInclBorder\])</span></span>                     |                                                                                                                                               |
| <span data-ttu-id="b5d86-225">public int topMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="b5d86-225">public int topMarginAndFrame()</span></span>                                           |                                                                                                                                               |
| <span data-ttu-id="b5d86-226">public int topMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-226">public int topMarginMode(\[int value\])</span></span>                                  |                                                                                                                                               |
| <span data-ttu-id="b5d86-227">public str topMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-227">public str topMarginStr(\[str value\])</span></span>                                   |                                                                                                                                               |
| <span data-ttu-id="b5d86-228">public Units topMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-228">public Units topMarginUnit(\[Units value\])</span></span>                              |                                                                                                                                               |
| <span data-ttu-id="b5d86-229">public Real topMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-229">public Real topMarginValue(\[Real value\])</span></span>                               |                                                                                                                                               |
| <span data-ttu-id="b5d86-230">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-230">public int topMode(\[int value\])</span></span>                                        |                                                                                                                                               |
| <span data-ttu-id="b5d86-231">public str topStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-231">public str topStr(\[str value\])</span></span>                                         |                                                                                                                                               |
| <span data-ttu-id="b5d86-232">public Units topUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-232">public Units topUnit(\[Units value\])</span></span>                                    |                                                                                                                                               |
| <span data-ttu-id="b5d86-233">public Real topValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-233">public Real topValue(\[Real value\])</span></span>                                     |                                                                                                                                               |
| <span data-ttu-id="b5d86-234">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-234">public boolean underline(\[boolean value\])</span></span>                              |                                                                                                                                               |
| <span data-ttu-id="b5d86-235">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-235">public boolean visible(\[boolean value\])</span></span>                                |                                                                                                                                               |
| <span data-ttu-id="b5d86-236">public str webMenuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-236">public str webMenuItemName(\[str value\])</span></span>                                |                                                                                                                                               |
| <span data-ttu-id="b5d86-237">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-237">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span></span>        |                                                                                                                                               |
| <span data-ttu-id="b5d86-238">public str webTarget(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-238">public str webTarget(\[str value\])</span></span>                                      |                                                                                                                                               |
| <span data-ttu-id="b5d86-239">public int width100mm(\[int widthExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-239">public int width100mm(\[int widthExclBorder\])</span></span>                           |                                                                                                                                               |
| <span data-ttu-id="b5d86-240">public int width100mmInclBorder(\[int widthInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-240">public int width100mmInclBorder(\[int widthInclBorder\])</span></span>                 |                                                                                                                                               |
| <span data-ttu-id="b5d86-241">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-241">public int widthMode(\[int value\])</span></span>                                      | <span data-ttu-id="b5d86-242">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-242">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                |
| <span data-ttu-id="b5d86-243">public int widthOfString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="b5d86-243">public int widthOfString100mm(str string)</span></span>                                |                                                                                                                                               |
| <span data-ttu-id="b5d86-244">public str widthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-244">public str widthStr(\[str value\])</span></span>                                       |                                                                                                                                               |
| <span data-ttu-id="b5d86-245">public Units widthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-245">public Units widthUnit(\[Units value\])</span></span>                                  |                                                                                                                                               |
| <span data-ttu-id="b5d86-246">public Real widthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="b5d86-246">public Real widthValue(\[Real value\])</span></span>                                   | <span data-ttu-id="b5d86-247">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-247">Gets or sets the width of the control.</span></span>                                                                                                        |
| <span data-ttu-id="b5d86-248">public void width(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="b5d86-248">public void width(Real value, Units unit)</span></span>                                | <span data-ttu-id="b5d86-249">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-249">Gets or sets the width of the control.</span></span>                                                                                                        |
| <span data-ttu-id="b5d86-250">public void topMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="b5d86-250">public void topMargin(Real value, Units unit)</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="b5d86-251">public void bottomMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="b5d86-251">public void bottomMargin(Real value, Units unit)</span></span>                         |                                                                                                                                               |
| <span data-ttu-id="b5d86-252">public void rightMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="b5d86-252">public void rightMargin(Real value, Units unit)</span></span>                          |                                                                                                                                               |
| <span data-ttu-id="b5d86-253">public void leftMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="b5d86-253">public void leftMargin(Real value, Units unit)</span></span>                           |                                                                                                                                               |
| <span data-ttu-id="b5d86-254">public void show()</span><span class="sxs-lookup"><span data-stu-id="b5d86-254">public void show()</span></span>                                                       |                                                                                                                                               |
| <span data-ttu-id="b5d86-255">public void hide()</span><span class="sxs-lookup"><span data-stu-id="b5d86-255">public void hide()</span></span>                                                       |                                                                                                                                               |
| <span data-ttu-id="b5d86-256">public void top(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="b5d86-256">public void top(Real value, Units unit)</span></span>                                  |                                                                                                                                               |
| <span data-ttu-id="b5d86-257">public void left(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="b5d86-257">public void left(Real value, Units unit)</span></span>                                 |                                                                                                                                               |
| <span data-ttu-id="b5d86-258">public void labelWidth(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="b5d86-258">public void labelWidth(Real value, Units unit)</span></span>                           |                                                                                                                                               |
| <span data-ttu-id="b5d86-259">public void height(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="b5d86-259">public void height(Real value, Units unit)</span></span>                               | <span data-ttu-id="b5d86-260">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-260">Gets or sets the height of the control.</span></span>                                                                                                       |

## <a name="method-alignment"></a><span data-ttu-id="b5d86-261">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="b5d86-261">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="b5d86-262">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="b5d86-262">Parameters - alignment</span></span>

<span data-ttu-id="b5d86-263">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-263">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="b5d86-264">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="b5d86-264">Return Value - alignment</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="b5d86-265">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="b5d86-265">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="b5d86-266">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="b5d86-266">Parameters - arrayIndex</span></span>

<span data-ttu-id="b5d86-267">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-267">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="b5d86-268">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="b5d86-268">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="b5d86-269">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="b5d86-269">Method autoDeclaration</span></span>

<span data-ttu-id="b5d86-270">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-270">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="b5d86-271">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="b5d86-271">Parameters - autoDeclaration</span></span>

<span data-ttu-id="b5d86-272">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-272">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="b5d86-273">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="b5d86-273">Return Value - autoDeclaration</span></span>

<span data-ttu-id="b5d86-274">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b5d86-274">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="b5d86-275">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="b5d86-275">Remarks - autoDeclaration</span></span>

<span data-ttu-id="b5d86-276">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="b5d86-276">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="b5d86-277">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="b5d86-277">Method backgroundColor</span></span>

<span data-ttu-id="b5d86-278">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-278">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="b5d86-279">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="b5d86-279">Parameters - backgroundColor</span></span>

<span data-ttu-id="b5d86-280">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-280">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="b5d86-281">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="b5d86-281">Return Value - backgroundColor</span></span>

<span data-ttu-id="b5d86-282">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="b5d86-282">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="b5d86-283">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="b5d86-283">Remarks - backgroundColor</span></span>

<span data-ttu-id="b5d86-284">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b5d86-284">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="b5d86-285">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b5d86-285">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="b5d86-286">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="b5d86-286">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="b5d86-287">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="b5d86-287">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="b5d86-288">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b5d86-288">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="b5d86-289">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="b5d86-289">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="b5d86-290">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="b5d86-290">Method backStyle</span></span>

<span data-ttu-id="b5d86-291">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-291">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="b5d86-292">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="b5d86-292">Parameters - backStyle</span></span>

<span data-ttu-id="b5d86-293">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-293">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="b5d86-294">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="b5d86-294">Return Value - backStyle</span></span>

<span data-ttu-id="b5d86-295">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="b5d86-295">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="b5d86-296">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="b5d86-296">Method bold</span></span>

<span data-ttu-id="b5d86-297">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-297">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="b5d86-298">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="b5d86-298">Parameters - bold</span></span>

<span data-ttu-id="b5d86-299">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-299">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="b5d86-300">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="b5d86-300">Return Value - bold</span></span>

<span data-ttu-id="b5d86-301">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="b5d86-301">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="b5d86-302">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="b5d86-302">Remarks - bold</span></span>

<span data-ttu-id="b5d86-303">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b5d86-303">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="b5d86-304">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-304">0 Use the default font weight.</span></span>
-   <span data-ttu-id="b5d86-305">1 シン。</span><span class="sxs-lookup"><span data-stu-id="b5d86-305">1 Thin.</span></span>
-   <span data-ttu-id="b5d86-306">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="b5d86-306">2 Extra-light.</span></span>
-   <span data-ttu-id="b5d86-307">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="b5d86-307">3 Light.</span></span>
-   <span data-ttu-id="b5d86-308">4 標準。</span><span class="sxs-lookup"><span data-stu-id="b5d86-308">4 Normal.</span></span>
-   <span data-ttu-id="b5d86-309">5 中。</span><span class="sxs-lookup"><span data-stu-id="b5d86-309">5 Medium.</span></span>
-   <span data-ttu-id="b5d86-310">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="b5d86-310">6 Semibold.</span></span>
-   <span data-ttu-id="b5d86-311">7 太字。</span><span class="sxs-lookup"><span data-stu-id="b5d86-311">7 Bold.</span></span>
-   <span data-ttu-id="b5d86-312">8 極太。</span><span class="sxs-lookup"><span data-stu-id="b5d86-312">8 Extra-bold.</span></span>
-   <span data-ttu-id="b5d86-313">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="b5d86-313">9 Heavy.</span></span>

## <a name="method-bottommarginandframe"></a><span data-ttu-id="b5d86-314">メソッド bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="b5d86-314">Method bottomMarginAndFrame</span></span>

```xpp
public int bottomMarginAndFrame()
```

### <a name="return-value---bottommarginandframe"></a><span data-ttu-id="b5d86-315">戻り値 - bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="b5d86-315">Return Value - bottomMarginAndFrame</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="b5d86-316">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-316">Method bottomMarginMode</span></span>

```xpp
public int bottomMarginMode([int value])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="b5d86-317">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-317">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="b5d86-318">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-318">value</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="b5d86-319">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-319">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginstr"></a><span data-ttu-id="b5d86-320">メソッド bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-320">Method bottomMarginStr</span></span>

```xpp
public str bottomMarginStr([str value])
```

### <a name="parameters---bottommarginstr"></a><span data-ttu-id="b5d86-321">パラメーター - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-321">Parameters - bottomMarginStr</span></span>

<span data-ttu-id="b5d86-322">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-322">value</span></span>  

### <a name="return-value---bottommarginstr"></a><span data-ttu-id="b5d86-323">戻り値 - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-323">Return Value - bottomMarginStr</span></span>

## <a name="method-bottommarginunit"></a><span data-ttu-id="b5d86-324">メソッド bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-324">Method bottomMarginUnit</span></span>

```xpp
public Units bottomMarginUnit([Units value])
```

### <a name="parameters---bottommarginunit"></a><span data-ttu-id="b5d86-325">パラメーター - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-325">Parameters - bottomMarginUnit</span></span>

<span data-ttu-id="b5d86-326">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-326">value</span></span>  

### <a name="return-value---bottommarginunit"></a><span data-ttu-id="b5d86-327">戻り値 - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-327">Return Value - bottomMarginUnit</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="b5d86-328">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-328">Method bottomMarginValue</span></span>

```xpp
public Real bottomMarginValue([Real value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="b5d86-329">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-329">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="b5d86-330">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-330">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="b5d86-331">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-331">Return Value - bottomMarginValue</span></span>

## <a name="method-changelabelcase"></a><span data-ttu-id="b5d86-332">メソッド changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="b5d86-332">Method changeLabelCase</span></span>

```xpp
public int changeLabelCase([int value])
```

### <a name="parameters---changelabelcase"></a><span data-ttu-id="b5d86-333">パラメーター - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="b5d86-333">Parameters - changeLabelCase</span></span>

<span data-ttu-id="b5d86-334">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-334">value</span></span>  

### <a name="return-value---changelabelcase"></a><span data-ttu-id="b5d86-335">戻り値 - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="b5d86-335">Return Value - changeLabelCase</span></span>

## <a name="method-characterset"></a><span data-ttu-id="b5d86-336">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="b5d86-336">Method characterSet</span></span>

<span data-ttu-id="b5d86-337">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-337">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="b5d86-338">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="b5d86-338">Parameters - characterSet</span></span>

<span data-ttu-id="b5d86-339">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-339">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="b5d86-340">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="b5d86-340">Return Value - characterSet</span></span>

<span data-ttu-id="b5d86-341">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b5d86-341">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="b5d86-342">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="b5d86-342">Remarks - characterSet</span></span>

<span data-ttu-id="b5d86-343">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-343">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="b5d86-344">値です。</span><span class="sxs-lookup"><span data-stu-id="b5d86-344">Value.</span></span> | <span data-ttu-id="b5d86-345">説明。</span><span class="sxs-lookup"><span data-stu-id="b5d86-345">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="b5d86-346">0</span><span class="sxs-lookup"><span data-stu-id="b5d86-346">0</span></span>      | <span data-ttu-id="b5d86-347">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b5d86-347">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="b5d86-348">1</span><span class="sxs-lookup"><span data-stu-id="b5d86-348">1</span></span>      | <span data-ttu-id="b5d86-349">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b5d86-349">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="b5d86-350">2</span><span class="sxs-lookup"><span data-stu-id="b5d86-350">2</span></span>      | <span data-ttu-id="b5d86-351">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b5d86-351">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="b5d86-352">77</span><span class="sxs-lookup"><span data-stu-id="b5d86-352">77</span></span>     | <span data-ttu-id="b5d86-353">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b5d86-353">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="b5d86-354">128</span><span class="sxs-lookup"><span data-stu-id="b5d86-354">128</span></span>    | <span data-ttu-id="b5d86-355">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b5d86-355">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="b5d86-356">129</span><span class="sxs-lookup"><span data-stu-id="b5d86-356">129</span></span>    | <span data-ttu-id="b5d86-357">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b5d86-357">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="b5d86-358">134</span><span class="sxs-lookup"><span data-stu-id="b5d86-358">134</span></span>    | <span data-ttu-id="b5d86-359">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b5d86-359">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="b5d86-360">136</span><span class="sxs-lookup"><span data-stu-id="b5d86-360">136</span></span>    | <span data-ttu-id="b5d86-361">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b5d86-361">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="b5d86-362">161</span><span class="sxs-lookup"><span data-stu-id="b5d86-362">161</span></span>    | <span data-ttu-id="b5d86-363">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b5d86-363">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="b5d86-364">162</span><span class="sxs-lookup"><span data-stu-id="b5d86-364">162</span></span>    | <span data-ttu-id="b5d86-365">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b5d86-365">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="b5d86-366">163</span><span class="sxs-lookup"><span data-stu-id="b5d86-366">163</span></span>    | <span data-ttu-id="b5d86-367">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b5d86-367">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="b5d86-368">186</span><span class="sxs-lookup"><span data-stu-id="b5d86-368">186</span></span>    | <span data-ttu-id="b5d86-369">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b5d86-369">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="b5d86-370">204</span><span class="sxs-lookup"><span data-stu-id="b5d86-370">204</span></span>    | <span data-ttu-id="b5d86-371">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b5d86-371">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="b5d86-372">238</span><span class="sxs-lookup"><span data-stu-id="b5d86-372">238</span></span>    | <span data-ttu-id="b5d86-373">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b5d86-373">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="b5d86-374">255</span><span class="sxs-lookup"><span data-stu-id="b5d86-374">255</span></span>    | <span data-ttu-id="b5d86-375">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b5d86-375">OEM\_CHARSET</span></span>         |

<span data-ttu-id="b5d86-376">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="b5d86-376">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="b5d86-377">値です。</span><span class="sxs-lookup"><span data-stu-id="b5d86-377">Value.</span></span> | <span data-ttu-id="b5d86-378">説明。</span><span class="sxs-lookup"><span data-stu-id="b5d86-378">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="b5d86-379">130</span><span class="sxs-lookup"><span data-stu-id="b5d86-379">130</span></span>    | <span data-ttu-id="b5d86-380">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b5d86-380">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="b5d86-381">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="b5d86-381">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="b5d86-382">値です。</span><span class="sxs-lookup"><span data-stu-id="b5d86-382">Value.</span></span> | <span data-ttu-id="b5d86-383">説明。</span><span class="sxs-lookup"><span data-stu-id="b5d86-383">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="b5d86-384">177</span><span class="sxs-lookup"><span data-stu-id="b5d86-384">177</span></span>    | <span data-ttu-id="b5d86-385">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b5d86-385">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="b5d86-386">178</span><span class="sxs-lookup"><span data-stu-id="b5d86-386">178</span></span>    | <span data-ttu-id="b5d86-387">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b5d86-387">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="b5d86-388">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="b5d86-388">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="b5d86-389">値です。</span><span class="sxs-lookup"><span data-stu-id="b5d86-389">Value.</span></span> | <span data-ttu-id="b5d86-390">説明。</span><span class="sxs-lookup"><span data-stu-id="b5d86-390">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="b5d86-391">222</span><span class="sxs-lookup"><span data-stu-id="b5d86-391">222</span></span>    | <span data-ttu-id="b5d86-392">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b5d86-392">THAI\_CHARSET</span></span> |

<span data-ttu-id="b5d86-393">既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="b5d86-393">The default character set is set to a value, depending on the current system locale.</span></span> <span data-ttu-id="b5d86-394">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="b5d86-394">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="b5d86-395">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5d86-395">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="b5d86-396">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="b5d86-396">Method colorScheme</span></span>

<span data-ttu-id="b5d86-397">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-397">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="b5d86-398">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="b5d86-398">Parameters - colorScheme</span></span>

<span data-ttu-id="b5d86-399">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-399">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="b5d86-400">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="b5d86-400">Return Value - colorScheme</span></span>

<span data-ttu-id="b5d86-401">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="b5d86-401">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="b5d86-402">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="b5d86-402">Remarks - colorScheme</span></span>

<span data-ttu-id="b5d86-403">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="b5d86-403">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="b5d86-404">値です。</span><span class="sxs-lookup"><span data-stu-id="b5d86-404">Value.</span></span> | <span data-ttu-id="b5d86-405">スタイル。</span><span class="sxs-lookup"><span data-stu-id="b5d86-405">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="b5d86-406">0</span><span class="sxs-lookup"><span data-stu-id="b5d86-406">0</span></span>      | <span data-ttu-id="b5d86-407">既定。</span><span class="sxs-lookup"><span data-stu-id="b5d86-407">Default.</span></span>                      |
| <span data-ttu-id="b5d86-408">1</span><span class="sxs-lookup"><span data-stu-id="b5d86-408">1</span></span>      | <span data-ttu-id="b5d86-409">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="b5d86-409">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="b5d86-410">2</span><span class="sxs-lookup"><span data-stu-id="b5d86-410">2</span></span>      | <span data-ttu-id="b5d86-411">真の配色。</span><span class="sxs-lookup"><span data-stu-id="b5d86-411">The true-color scheme.</span></span>        |

## <a name="method-configurationkey"></a><span data-ttu-id="b5d86-412">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="b5d86-412">Method configurationKey</span></span>

<span data-ttu-id="b5d86-413">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-413">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="b5d86-414">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="b5d86-414">Parameters - configurationKey</span></span>

<span data-ttu-id="b5d86-415">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-415">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="b5d86-416">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="b5d86-416">Return Value - configurationKey</span></span>

<span data-ttu-id="b5d86-417">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="b5d86-417">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="b5d86-418">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="b5d86-418">Remarks - configurationKey</span></span>

<span data-ttu-id="b5d86-419">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b5d86-419">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="b5d86-420">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="b5d86-420">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-controltype"></a><span data-ttu-id="b5d86-421">メソッド controlType</span><span class="sxs-lookup"><span data-stu-id="b5d86-421">Method controlType</span></span>

```xpp
public ReportFieldType controlType()
```

### <a name="return-value---controltype"></a><span data-ttu-id="b5d86-422">戻り値 - controlType</span><span class="sxs-lookup"><span data-stu-id="b5d86-422">Return Value - controlType</span></span>

## <a name="method-cssclass"></a><span data-ttu-id="b5d86-423">メソッド cssClass</span><span class="sxs-lookup"><span data-stu-id="b5d86-423">Method cssClass</span></span>

```xpp
public str cssClass([str value])
```

### <a name="parameters---cssclass"></a><span data-ttu-id="b5d86-424">パラメーター - cssClass</span><span class="sxs-lookup"><span data-stu-id="b5d86-424">Parameters - cssClass</span></span>

<span data-ttu-id="b5d86-425">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-425">value</span></span>  

### <a name="return-value---cssclass"></a><span data-ttu-id="b5d86-426">戻り値 - cssClass</span><span class="sxs-lookup"><span data-stu-id="b5d86-426">Return Value - cssClass</span></span>

## <a name="method-datafield"></a><span data-ttu-id="b5d86-427">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="b5d86-427">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="b5d86-428">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="b5d86-428">Parameters - dataField</span></span>

<span data-ttu-id="b5d86-429">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-429">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="b5d86-430">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="b5d86-430">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="b5d86-431">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="b5d86-431">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="b5d86-432">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="b5d86-432">Parameters - dataMethod</span></span>

<span data-ttu-id="b5d86-433">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-433">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="b5d86-434">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="b5d86-434">Return Value - dataMethod</span></span>

## <a name="method-delete"></a><span data-ttu-id="b5d86-435">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="b5d86-435">Method delete</span></span>

```xpp
public int delete()
```

### <a name="return-value---delete"></a><span data-ttu-id="b5d86-436">戻り値 - delete</span><span class="sxs-lookup"><span data-stu-id="b5d86-436">Return Value - delete</span></span>

## <a name="method-effectivefont"></a><span data-ttu-id="b5d86-437">メソッド effectiveFont</span><span class="sxs-lookup"><span data-stu-id="b5d86-437">Method effectiveFont</span></span>

```xpp
public str effectiveFont()
```

### <a name="return-value---effectivefont"></a><span data-ttu-id="b5d86-438">戻り値 - effectiveFont</span><span class="sxs-lookup"><span data-stu-id="b5d86-438">Return Value - effectiveFont</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="b5d86-439">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="b5d86-439">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="b5d86-440">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="b5d86-440">Parameters - extendedDataType</span></span>

<span data-ttu-id="b5d86-441">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-441">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="b5d86-442">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="b5d86-442">Return Value - extendedDataType</span></span>

## <a name="method-font"></a><span data-ttu-id="b5d86-443">メソッド font</span><span class="sxs-lookup"><span data-stu-id="b5d86-443">Method font</span></span>

<span data-ttu-id="b5d86-444">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-444">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="b5d86-445">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="b5d86-445">Parameters - font</span></span>

<span data-ttu-id="b5d86-446">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-446">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="b5d86-447">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="b5d86-447">Return Value - font</span></span>

<span data-ttu-id="b5d86-448">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="b5d86-448">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontinfoprinter"></a><span data-ttu-id="b5d86-449">メソッド fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="b5d86-449">Method fontInfoPrinter</span></span>

```xpp
public str fontInfoPrinter()
```

### <a name="return-value---fontinfoprinter"></a><span data-ttu-id="b5d86-450">戻り値 - fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="b5d86-450">Return Value - fontInfoPrinter</span></span>

## <a name="method-fontinfoprinterascent"></a><span data-ttu-id="b5d86-451">メソッド fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="b5d86-451">Method fontInfoPrinterAscent</span></span>

```xpp
public int fontInfoPrinterAscent()
```

### <a name="return-value---fontinfoprinterascent"></a><span data-ttu-id="b5d86-452">戻り値 - fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="b5d86-452">Return Value - fontInfoPrinterAscent</span></span>

## <a name="method-fontinfoprinterdescent"></a><span data-ttu-id="b5d86-453">メソッド fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="b5d86-453">Method fontInfoPrinterDescent</span></span>

```xpp
public int fontInfoPrinterDescent()
```

### <a name="return-value---fontinfoprinterdescent"></a><span data-ttu-id="b5d86-454">戻り値 - fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="b5d86-454">Return Value - fontInfoPrinterDescent</span></span>

## <a name="method-fontinfoprinterextlead"></a><span data-ttu-id="b5d86-455">メソッド fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="b5d86-455">Method fontInfoPrinterExtLead</span></span>

```xpp
public int fontInfoPrinterExtLead()
```

### <a name="return-value---fontinfoprinterextlead"></a><span data-ttu-id="b5d86-456">戻り値 - fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="b5d86-456">Return Value - fontInfoPrinterExtLead</span></span>

## <a name="method-fontinfoprinterheight"></a><span data-ttu-id="b5d86-457">メソッド fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="b5d86-457">Method fontInfoPrinterHeight</span></span>

```xpp
public int fontInfoPrinterHeight()
```

### <a name="return-value---fontinfoprinterheight"></a><span data-ttu-id="b5d86-458">戻り値 - fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="b5d86-458">Return Value - fontInfoPrinterHeight</span></span>

## <a name="method-fontinfoprinterintlead"></a><span data-ttu-id="b5d86-459">メソッド fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="b5d86-459">Method fontInfoPrinterIntLead</span></span>

```xpp
public int fontInfoPrinterIntLead()
```

### <a name="return-value---fontinfoprinterintlead"></a><span data-ttu-id="b5d86-460">戻り値 - fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="b5d86-460">Return Value - fontInfoPrinterIntLead</span></span>

## <a name="method-fontinfoscreen"></a><span data-ttu-id="b5d86-461">メソッド fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="b5d86-461">Method fontInfoScreen</span></span>

```xpp
public str fontInfoScreen()
```

### <a name="return-value---fontinfoscreen"></a><span data-ttu-id="b5d86-462">戻り値 - fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="b5d86-462">Return Value - fontInfoScreen</span></span>

## <a name="method-fontinfoscreenascent"></a><span data-ttu-id="b5d86-463">メソッド fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="b5d86-463">Method fontInfoScreenAscent</span></span>

```xpp
public int fontInfoScreenAscent()
```

### <a name="return-value---fontinfoscreenascent"></a><span data-ttu-id="b5d86-464">戻り値 - fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="b5d86-464">Return Value - fontInfoScreenAscent</span></span>

## <a name="method-fontinfoscreendescent"></a><span data-ttu-id="b5d86-465">メソッド fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="b5d86-465">Method fontInfoScreenDescent</span></span>

```xpp
public int fontInfoScreenDescent()
```

### <a name="return-value---fontinfoscreendescent"></a><span data-ttu-id="b5d86-466">戻り値 - fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="b5d86-466">Return Value - fontInfoScreenDescent</span></span>

## <a name="method-fontinfoscreenextlead"></a><span data-ttu-id="b5d86-467">メソッド fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="b5d86-467">Method fontInfoScreenExtLead</span></span>

```xpp
public int fontInfoScreenExtLead()
```

### <a name="return-value---fontinfoscreenextlead"></a><span data-ttu-id="b5d86-468">戻り値 - fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="b5d86-468">Return Value - fontInfoScreenExtLead</span></span>

## <a name="method-fontinfoscreenheight"></a><span data-ttu-id="b5d86-469">メソッド fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="b5d86-469">Method fontInfoScreenHeight</span></span>

```xpp
public int fontInfoScreenHeight()
```

### <a name="return-value---fontinfoscreenheight"></a><span data-ttu-id="b5d86-470">戻り値 - fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="b5d86-470">Return Value - fontInfoScreenHeight</span></span>

## <a name="method-fontinfoscreenintlead"></a><span data-ttu-id="b5d86-471">メソッド fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="b5d86-471">Method fontInfoScreenIntLead</span></span>

```xpp
public int fontInfoScreenIntLead()
```

### <a name="return-value---fontinfoscreenintlead"></a><span data-ttu-id="b5d86-472">戻り値 - fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="b5d86-472">Return Value - fontInfoScreenIntLead</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="b5d86-473">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="b5d86-473">Method fontSize</span></span>

<span data-ttu-id="b5d86-474">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-474">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="b5d86-475">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="b5d86-475">Parameters - fontSize</span></span>

<span data-ttu-id="b5d86-476">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-476">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="b5d86-477">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="b5d86-477">Return Value - fontSize</span></span>

<span data-ttu-id="b5d86-478">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="b5d86-478">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="b5d86-479">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="b5d86-479">Method foregroundColor</span></span>

<span data-ttu-id="b5d86-480">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-480">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="b5d86-481">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="b5d86-481">Parameters - foregroundColor</span></span>

<span data-ttu-id="b5d86-482">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-482">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="b5d86-483">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="b5d86-483">Return Value - foregroundColor</span></span>

<span data-ttu-id="b5d86-484">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="b5d86-484">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="b5d86-485">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="b5d86-485">Remarks - foregroundColor</span></span>

<span data-ttu-id="b5d86-486">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b5d86-486">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="b5d86-487">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b5d86-487">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="b5d86-488">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="b5d86-488">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="b5d86-489">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="b5d86-489">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="b5d86-490">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b5d86-490">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="b5d86-491">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="b5d86-491">The maximum value for a single byte is 255.</span></span>

## <a name="method-height100mm"></a><span data-ttu-id="b5d86-492">メソッド height100mm</span><span class="sxs-lookup"><span data-stu-id="b5d86-492">Method height100mm</span></span>

```xpp
public int height100mm([int heightExclBorder])
```

### <a name="parameters---height100mm"></a><span data-ttu-id="b5d86-493">パラメーター - height100mm</span><span class="sxs-lookup"><span data-stu-id="b5d86-493">Parameters - height100mm</span></span>

<span data-ttu-id="b5d86-494">heightExclBorder</span><span class="sxs-lookup"><span data-stu-id="b5d86-494">heightExclBorder</span></span>  

### <a name="return-value---height100mm"></a><span data-ttu-id="b5d86-495">戻り値 - height100mm</span><span class="sxs-lookup"><span data-stu-id="b5d86-495">Return Value - height100mm</span></span>

## <a name="method-height100mminclborder"></a><span data-ttu-id="b5d86-496">メソッド height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b5d86-496">Method height100mmInclBorder</span></span>

```xpp
public int height100mmInclBorder([int heightInclBorder])
```

### <a name="parameters---height100mminclborder"></a><span data-ttu-id="b5d86-497">パラメーター - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b5d86-497">Parameters - height100mmInclBorder</span></span>

<span data-ttu-id="b5d86-498">heightInclBorder</span><span class="sxs-lookup"><span data-stu-id="b5d86-498">heightInclBorder</span></span>  

### <a name="return-value---height100mminclborder"></a><span data-ttu-id="b5d86-499">戻り値 - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b5d86-499">Return Value - height100mmInclBorder</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="b5d86-500">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-500">Method heightMode</span></span>

<span data-ttu-id="b5d86-501">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-501">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="b5d86-502">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-502">Parameters - heightMode</span></span>

<span data-ttu-id="b5d86-503">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-503">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="b5d86-504">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-504">Return Value - heightMode</span></span>

<span data-ttu-id="b5d86-505">計算モード。</span><span class="sxs-lookup"><span data-stu-id="b5d86-505">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="b5d86-506">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-506">Remarks - heightMode</span></span>

<span data-ttu-id="b5d86-507">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="b5d86-507">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="b5d86-508">モード。</span><span class="sxs-lookup"><span data-stu-id="b5d86-508">Mode.</span></span>          | <span data-ttu-id="b5d86-509">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="b5d86-509">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d86-510">正確。</span><span class="sxs-lookup"><span data-stu-id="b5d86-510">Exact.</span></span>         | <span data-ttu-id="b5d86-511">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b5d86-511">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b5d86-512">自動。</span><span class="sxs-lookup"><span data-stu-id="b5d86-512">Auto.</span></span>          | <span data-ttu-id="b5d86-513">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b5d86-513">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b5d86-514">列の高さ</span><span class="sxs-lookup"><span data-stu-id="b5d86-514">Column height.</span></span> | <span data-ttu-id="b5d86-515">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="b5d86-515">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="b5d86-516">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="b5d86-516">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightofwordwrappedstring100mm"></a><span data-ttu-id="b5d86-517">メソッド heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="b5d86-517">Method heightOfWordWrappedString100mm</span></span>

```xpp
public int heightOfWordWrappedString100mm(str string)
```

### <a name="parameters---heightofwordwrappedstring100mm"></a><span data-ttu-id="b5d86-518">パラメーター - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="b5d86-518">Parameters - heightOfWordWrappedString100mm</span></span>

<span data-ttu-id="b5d86-519">文字列</span><span class="sxs-lookup"><span data-stu-id="b5d86-519">string</span></span>  

### <a name="return-value---heightofwordwrappedstring100mm"></a><span data-ttu-id="b5d86-520">戻り値 - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="b5d86-520">Return Value - heightOfWordWrappedString100mm</span></span>

## <a name="method-heightstr"></a><span data-ttu-id="b5d86-521">メソッド heightStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-521">Method heightStr</span></span>

```xpp
public str heightStr([str value])
```

### <a name="parameters---heightstr"></a><span data-ttu-id="b5d86-522">パラメーター - heightStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-522">Parameters - heightStr</span></span>

<span data-ttu-id="b5d86-523">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-523">value</span></span>  

### <a name="return-value---heightstr"></a><span data-ttu-id="b5d86-524">戻り値 - heightStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-524">Return Value - heightStr</span></span>

## <a name="method-heightunit"></a><span data-ttu-id="b5d86-525">メソッド heightUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-525">Method heightUnit</span></span>

```xpp
public Units heightUnit([Units value])
```

### <a name="parameters---heightunit"></a><span data-ttu-id="b5d86-526">パラメーター - heightUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-526">Parameters - heightUnit</span></span>

<span data-ttu-id="b5d86-527">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-527">value</span></span>  

### <a name="return-value---heightunit"></a><span data-ttu-id="b5d86-528">戻り値 - heightUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-528">Return Value - heightUnit</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="b5d86-529">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-529">Method heightValue</span></span>

<span data-ttu-id="b5d86-530">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-530">Gets or sets the height of the control.</span></span>

```xpp
public Real heightValue([Real value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="b5d86-531">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-531">Parameters - heightValue</span></span>

<span data-ttu-id="b5d86-532">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-532">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="b5d86-533">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-533">Return Value - heightValue</span></span>

<span data-ttu-id="b5d86-534">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="b5d86-534">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="b5d86-535">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-535">Remarks - heightValue</span></span>

<span data-ttu-id="b5d86-536">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="b5d86-536">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-italic"></a><span data-ttu-id="b5d86-537">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="b5d86-537">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="b5d86-538">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="b5d86-538">Parameters - italic</span></span>

<span data-ttu-id="b5d86-539">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-539">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="b5d86-540">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="b5d86-540">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="b5d86-541">メソッド label</span><span class="sxs-lookup"><span data-stu-id="b5d86-541">Method label</span></span>

<span data-ttu-id="b5d86-542">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-542">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="b5d86-543">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="b5d86-543">Parameters - label</span></span>

<span data-ttu-id="b5d86-544">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-544">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="b5d86-545">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="b5d86-545">Return Value - label</span></span>

<span data-ttu-id="b5d86-546">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="b5d86-546">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="b5d86-547">備考 - label</span><span class="sxs-lookup"><span data-stu-id="b5d86-547">Remarks - label</span></span>

<span data-ttu-id="b5d86-548">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-548">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="b5d86-549">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="b5d86-549">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="b5d86-550">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="b5d86-550">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="b5d86-551">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="b5d86-551">Parameters - labelBold</span></span>

<span data-ttu-id="b5d86-552">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-552">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="b5d86-553">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="b5d86-553">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="b5d86-554">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="b5d86-554">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="b5d86-555">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="b5d86-555">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="b5d86-556">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-556">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="b5d86-557">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="b5d86-557">Return Value - labelCharacterSet</span></span>

## <a name="method-labelcssclass"></a><span data-ttu-id="b5d86-558">メソッド labelCssClass</span><span class="sxs-lookup"><span data-stu-id="b5d86-558">Method labelCssClass</span></span>

```xpp
public str labelCssClass([str value])
```

### <a name="parameters---labelcssclass"></a><span data-ttu-id="b5d86-559">パラメーター - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="b5d86-559">Parameters - labelCssClass</span></span>

<span data-ttu-id="b5d86-560">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-560">value</span></span>  

### <a name="return-value---labelcssclass"></a><span data-ttu-id="b5d86-561">戻り値 - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="b5d86-561">Return Value - labelCssClass</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="b5d86-562">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="b5d86-562">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="b5d86-563">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="b5d86-563">Parameters - labelFont</span></span>

<span data-ttu-id="b5d86-564">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-564">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="b5d86-565">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="b5d86-565">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="b5d86-566">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="b5d86-566">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="b5d86-567">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="b5d86-567">Parameters - labelFontSize</span></span>

<span data-ttu-id="b5d86-568">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-568">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="b5d86-569">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="b5d86-569">Return Value - labelFontSize</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="b5d86-570">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="b5d86-570">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="b5d86-571">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="b5d86-571">Parameters - labelItalic</span></span>

<span data-ttu-id="b5d86-572">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-572">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="b5d86-573">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="b5d86-573">Return Value - labelItalic</span></span>

## <a name="method-labellinebelow"></a><span data-ttu-id="b5d86-574">メソッド labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="b5d86-574">Method labelLineBelow</span></span>

```xpp
public LineType labelLineBelow([LineType value])
```

### <a name="parameters---labellinebelow"></a><span data-ttu-id="b5d86-575">パラメーター - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="b5d86-575">Parameters - labelLineBelow</span></span>

<span data-ttu-id="b5d86-576">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-576">value</span></span>  

### <a name="return-value---labellinebelow"></a><span data-ttu-id="b5d86-577">戻り値 - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="b5d86-577">Return Value - labelLineBelow</span></span>

## <a name="method-labellinethickness"></a><span data-ttu-id="b5d86-578">メソッド labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="b5d86-578">Method labelLineThickness</span></span>

```xpp
public LineThickness labelLineThickness([LineThickness value])
```

### <a name="parameters---labellinethickness"></a><span data-ttu-id="b5d86-579">パラメーター - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="b5d86-579">Parameters - labelLineThickness</span></span>

<span data-ttu-id="b5d86-580">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-580">value</span></span>  

### <a name="return-value---labellinethickness"></a><span data-ttu-id="b5d86-581">戻り値 - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="b5d86-581">Return Value - labelLineThickness</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="b5d86-582">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="b5d86-582">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="b5d86-583">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="b5d86-583">Parameters - labelPosition</span></span>

<span data-ttu-id="b5d86-584">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-584">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="b5d86-585">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="b5d86-585">Return Value - labelPosition</span></span>

## <a name="method-labeltableader"></a><span data-ttu-id="b5d86-586">メソッド labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="b5d86-586">Method labelTabLeader</span></span>

```xpp
public int labelTabLeader([int value])
```

### <a name="parameters---labeltableader"></a><span data-ttu-id="b5d86-587">パラメーター - labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="b5d86-587">Parameters - labelTabLeader</span></span>

<span data-ttu-id="b5d86-588">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-588">value</span></span>  

### <a name="return-value---labeltableader"></a><span data-ttu-id="b5d86-589">戻り値 - labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="b5d86-589">Return Value - labelTabLeader</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="b5d86-590">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="b5d86-590">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="b5d86-591">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="b5d86-591">Parameters - labelUnderline</span></span>

<span data-ttu-id="b5d86-592">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-592">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="b5d86-593">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="b5d86-593">Return Value - labelUnderline</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="b5d86-594">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-594">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="b5d86-595">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-595">Parameters - labelWidthMode</span></span>

<span data-ttu-id="b5d86-596">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-596">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="b5d86-597">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-597">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthstr"></a><span data-ttu-id="b5d86-598">メソッド labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-598">Method labelWidthStr</span></span>

```xpp
public str labelWidthStr([str value])
```

### <a name="parameters---labelwidthstr"></a><span data-ttu-id="b5d86-599">パラメーター - labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-599">Parameters - labelWidthStr</span></span>

<span data-ttu-id="b5d86-600">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-600">value</span></span>  

### <a name="return-value---labelwidthstr"></a><span data-ttu-id="b5d86-601">戻り値 - labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-601">Return Value - labelWidthStr</span></span>

## <a name="method-labelwidthunit"></a><span data-ttu-id="b5d86-602">メソッド labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-602">Method labelWidthUnit</span></span>

```xpp
public Units labelWidthUnit([Units value])
```

### <a name="parameters---labelwidthunit"></a><span data-ttu-id="b5d86-603">パラメーター - labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-603">Parameters - labelWidthUnit</span></span>

<span data-ttu-id="b5d86-604">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-604">value</span></span>  

### <a name="return-value---labelwidthunit"></a><span data-ttu-id="b5d86-605">戻り値 - labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-605">Return Value - labelWidthUnit</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="b5d86-606">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-606">Method labelWidthValue</span></span>

```xpp
public Real labelWidthValue([Real value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="b5d86-607">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-607">Parameters - labelWidthValue</span></span>

<span data-ttu-id="b5d86-608">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-608">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="b5d86-609">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-609">Return Value - labelWidthValue</span></span>

## <a name="method-left100mm"></a><span data-ttu-id="b5d86-610">メソッド left100mm</span><span class="sxs-lookup"><span data-stu-id="b5d86-610">Method left100mm</span></span>

```xpp
public int left100mm([int leftExclBorder])
```

### <a name="parameters---left100mm"></a><span data-ttu-id="b5d86-611">パラメーター - left100mm</span><span class="sxs-lookup"><span data-stu-id="b5d86-611">Parameters - left100mm</span></span>

<span data-ttu-id="b5d86-612">leftExclBorder</span><span class="sxs-lookup"><span data-stu-id="b5d86-612">leftExclBorder</span></span>  

### <a name="return-value---left100mm"></a><span data-ttu-id="b5d86-613">戻り値 - left100mm</span><span class="sxs-lookup"><span data-stu-id="b5d86-613">Return Value - left100mm</span></span>

## <a name="method-left100mminclborder"></a><span data-ttu-id="b5d86-614">メソッド left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b5d86-614">Method left100mmInclBorder</span></span>

```xpp
public int left100mmInclBorder([int leftInclBorder])
```

### <a name="parameters---left100mminclborder"></a><span data-ttu-id="b5d86-615">パラメーター - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b5d86-615">Parameters - left100mmInclBorder</span></span>

<span data-ttu-id="b5d86-616">leftInclBorder</span><span class="sxs-lookup"><span data-stu-id="b5d86-616">leftInclBorder</span></span>  

### <a name="return-value---left100mminclborder"></a><span data-ttu-id="b5d86-617">戻り値 - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b5d86-617">Return Value - left100mmInclBorder</span></span>

## <a name="method-leftmarginanframe"></a><span data-ttu-id="b5d86-618">メソッド leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="b5d86-618">Method leftMarginAnFrame</span></span>

```xpp
public int leftMarginAnFrame()
```

### <a name="return-value---leftmarginanframe"></a><span data-ttu-id="b5d86-619">戻り値 - leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="b5d86-619">Return Value - leftMarginAnFrame</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="b5d86-620">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-620">Method leftMarginMode</span></span>

```xpp
public int leftMarginMode([int value])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="b5d86-621">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-621">Parameters - leftMarginMode</span></span>

<span data-ttu-id="b5d86-622">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-622">value</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="b5d86-623">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-623">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginstr"></a><span data-ttu-id="b5d86-624">メソッド leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-624">Method leftMarginStr</span></span>

```xpp
public str leftMarginStr([str value])
```

### <a name="parameters---leftmarginstr"></a><span data-ttu-id="b5d86-625">パラメーター - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-625">Parameters - leftMarginStr</span></span>

<span data-ttu-id="b5d86-626">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-626">value</span></span>  

### <a name="return-value---leftmarginstr"></a><span data-ttu-id="b5d86-627">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-627">Return Value - leftMarginStr</span></span>

## <a name="method-leftmarginunit"></a><span data-ttu-id="b5d86-628">メソッド leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-628">Method leftMarginUnit</span></span>

```xpp
public Units leftMarginUnit([Units value])
```

### <a name="parameters---leftmarginunit"></a><span data-ttu-id="b5d86-629">パラメーター - leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-629">Parameters - leftMarginUnit</span></span>

<span data-ttu-id="b5d86-630">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-630">value</span></span>  

### <a name="return-value---leftmarginunit"></a><span data-ttu-id="b5d86-631">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-631">Return Value - leftMarginUnit</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="b5d86-632">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-632">Method leftMarginValue</span></span>

```xpp
public Real leftMarginValue([Real value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="b5d86-633">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-633">Parameters - leftMarginValue</span></span>

<span data-ttu-id="b5d86-634">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-634">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="b5d86-635">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-635">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="b5d86-636">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-636">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="b5d86-637">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-637">Parameters - leftMode</span></span>

<span data-ttu-id="b5d86-638">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-638">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="b5d86-639">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-639">Return Value - leftMode</span></span>

## <a name="method-leftstr"></a><span data-ttu-id="b5d86-640">メソッド leftStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-640">Method leftStr</span></span>

```xpp
public str leftStr([str value])
```

### <a name="parameters---leftstr"></a><span data-ttu-id="b5d86-641">パラメーター - leftStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-641">Parameters - leftStr</span></span>

<span data-ttu-id="b5d86-642">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-642">value</span></span>  

### <a name="return-value---leftstr"></a><span data-ttu-id="b5d86-643">戻り値 - leftStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-643">Return Value - leftStr</span></span>

## <a name="method-leftunit"></a><span data-ttu-id="b5d86-644">メソッド leftUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-644">Method leftUnit</span></span>

```xpp
public Units leftUnit([Units value])
```

### <a name="parameters---leftunit"></a><span data-ttu-id="b5d86-645">パラメーター - leftUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-645">Parameters - leftUnit</span></span>

<span data-ttu-id="b5d86-646">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-646">value</span></span>  

### <a name="return-value---leftunit"></a><span data-ttu-id="b5d86-647">戻り値 - leftUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-647">Return Value - leftUnit</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="b5d86-648">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-648">Method leftValue</span></span>

```xpp
public Real leftValue([Real value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="b5d86-649">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-649">Parameters - leftValue</span></span>

<span data-ttu-id="b5d86-650">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-650">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="b5d86-651">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-651">Return Value - leftValue</span></span>

## <a name="method-lineabove"></a><span data-ttu-id="b5d86-652">メソッド lineAbove</span><span class="sxs-lookup"><span data-stu-id="b5d86-652">Method lineAbove</span></span>

```xpp
public LineType lineAbove([LineType value])
```

### <a name="parameters---lineabove"></a><span data-ttu-id="b5d86-653">パラメーター - lineAbove</span><span class="sxs-lookup"><span data-stu-id="b5d86-653">Parameters - lineAbove</span></span>

<span data-ttu-id="b5d86-654">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-654">value</span></span>  

### <a name="return-value---lineabove"></a><span data-ttu-id="b5d86-655">戻り値 - lineAbove</span><span class="sxs-lookup"><span data-stu-id="b5d86-655">Return Value - lineAbove</span></span>

## <a name="method-linebelow"></a><span data-ttu-id="b5d86-656">メソッド lineBelow</span><span class="sxs-lookup"><span data-stu-id="b5d86-656">Method lineBelow</span></span>

```xpp
public LineType lineBelow([LineType value])
```

### <a name="parameters---linebelow"></a><span data-ttu-id="b5d86-657">パラメーター - lineBelow</span><span class="sxs-lookup"><span data-stu-id="b5d86-657">Parameters - lineBelow</span></span>

<span data-ttu-id="b5d86-658">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-658">value</span></span>  

### <a name="return-value---linebelow"></a><span data-ttu-id="b5d86-659">戻り値 - lineBelow</span><span class="sxs-lookup"><span data-stu-id="b5d86-659">Return Value - lineBelow</span></span>

## <a name="method-lineleft"></a><span data-ttu-id="b5d86-660">メソッド lineLeft</span><span class="sxs-lookup"><span data-stu-id="b5d86-660">Method lineLeft</span></span>

<span data-ttu-id="b5d86-661">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-661">Gets or sets the type of line that is used as the left border of a section.</span></span>

```xpp
public LineType lineLeft([LineType value])
```

### <a name="parameters---lineleft"></a><span data-ttu-id="b5d86-662">パラメーター - lineLeft</span><span class="sxs-lookup"><span data-stu-id="b5d86-662">Parameters - lineLeft</span></span>

<span data-ttu-id="b5d86-663">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-663">value</span></span>  

### <a name="return-value---lineleft"></a><span data-ttu-id="b5d86-664">戻り値 - lineLeft</span><span class="sxs-lookup"><span data-stu-id="b5d86-664">Return Value - lineLeft</span></span>

<span data-ttu-id="b5d86-665">左境界線として使用される線のタイプ。</span><span class="sxs-lookup"><span data-stu-id="b5d86-665">The type of line that is used as the left border.</span></span>

## <a name="method-lineright"></a><span data-ttu-id="b5d86-666">メソッド lineRight</span><span class="sxs-lookup"><span data-stu-id="b5d86-666">Method lineRight</span></span>

```xpp
public LineType lineRight([LineType value])
```

### <a name="parameters---lineright"></a><span data-ttu-id="b5d86-667">パラメーター - lineRight</span><span class="sxs-lookup"><span data-stu-id="b5d86-667">Parameters - lineRight</span></span>

<span data-ttu-id="b5d86-668">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-668">value</span></span>  

### <a name="return-value---lineright"></a><span data-ttu-id="b5d86-669">戻り値 - lineRight</span><span class="sxs-lookup"><span data-stu-id="b5d86-669">Return Value - lineRight</span></span>

## <a name="method-menuitemlabel"></a><span data-ttu-id="b5d86-670">メソッド menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="b5d86-670">Method menuItemLabel</span></span>

```xpp
public str menuItemLabel([str value])
```

### <a name="parameters---menuitemlabel"></a><span data-ttu-id="b5d86-671">パラメーター - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="b5d86-671">Parameters - menuItemLabel</span></span>

<span data-ttu-id="b5d86-672">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-672">value</span></span>  

### <a name="return-value---menuitemlabel"></a><span data-ttu-id="b5d86-673">戻り値 - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="b5d86-673">Return Value - menuItemLabel</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="b5d86-674">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="b5d86-674">Method menuItemName</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="b5d86-675">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="b5d86-675">Parameters - menuItemName</span></span>

<span data-ttu-id="b5d86-676">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-676">value</span></span>  

### <a name="return-value---menuitemname"></a><span data-ttu-id="b5d86-677">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="b5d86-677">Return Value - menuItemName</span></span>

## <a name="method-menuitemtype"></a><span data-ttu-id="b5d86-678">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="b5d86-678">Method menuItemType</span></span>

```xpp
public MenuItemType menuItemType([MenuItemType value])
```

### <a name="parameters---menuitemtype"></a><span data-ttu-id="b5d86-679">パラメーター - menuItemType</span><span class="sxs-lookup"><span data-stu-id="b5d86-679">Parameters - menuItemType</span></span>

<span data-ttu-id="b5d86-680">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-680">value</span></span>  

### <a name="return-value---menuitemtype"></a><span data-ttu-id="b5d86-681">戻り値 - menuItemType</span><span class="sxs-lookup"><span data-stu-id="b5d86-681">Return Value - menuItemType</span></span>

## <a name="method-modelfieldname"></a><span data-ttu-id="b5d86-682">メソッド modelFieldName</span><span class="sxs-lookup"><span data-stu-id="b5d86-682">Method modelFieldName</span></span>

```xpp
public str modelFieldName([str value])
```

### <a name="parameters---modelfieldname"></a><span data-ttu-id="b5d86-683">パラメーター - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="b5d86-683">Parameters - modelFieldName</span></span>

<span data-ttu-id="b5d86-684">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-684">value</span></span>  

### <a name="return-value---modelfieldname"></a><span data-ttu-id="b5d86-685">戻り値 - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="b5d86-685">Return Value - modelFieldName</span></span>

## <a name="method-name"></a><span data-ttu-id="b5d86-686">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b5d86-686">Method name</span></span>

<span data-ttu-id="b5d86-687">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-687">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="b5d86-688">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="b5d86-688">Parameters - name</span></span>

<span data-ttu-id="b5d86-689">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-689">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="b5d86-690">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="b5d86-690">Return Value - name</span></span>

<span data-ttu-id="b5d86-691">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="b5d86-691">The name that is used in the code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="b5d86-692">備考 - name</span><span class="sxs-lookup"><span data-stu-id="b5d86-692">Remarks - name</span></span>

<span data-ttu-id="b5d86-693">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5d86-693">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="b5d86-694">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="b5d86-694">Begins with a letter.</span></span>
-   <span data-ttu-id="b5d86-695">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="b5d86-695">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="b5d86-696">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="b5d86-696">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="b5d86-697">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="b5d86-697">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="b5d86-698">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="b5d86-698">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-numberoflines"></a><span data-ttu-id="b5d86-699">メソッド numberOfLines</span><span class="sxs-lookup"><span data-stu-id="b5d86-699">Method numberOfLines</span></span>

```xpp
public int numberOfLines(int height100mm)
```

### <a name="parameters---numberoflines"></a><span data-ttu-id="b5d86-700">パラメーター - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="b5d86-700">Parameters - numberOfLines</span></span>

<span data-ttu-id="b5d86-701">height100mm</span><span class="sxs-lookup"><span data-stu-id="b5d86-701">height100mm</span></span>  

### <a name="return-value---numberoflines"></a><span data-ttu-id="b5d86-702">戻り値 - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="b5d86-702">Return Value - numberOfLines</span></span>

## <a name="method-position"></a><span data-ttu-id="b5d86-703">メソッドの位置</span><span class="sxs-lookup"><span data-stu-id="b5d86-703">Method position</span></span>

```xpp
public int position([int value])
```

### <a name="parameters---position"></a><span data-ttu-id="b5d86-704">パラメーター - position</span><span class="sxs-lookup"><span data-stu-id="b5d86-704">Parameters - position</span></span>

<span data-ttu-id="b5d86-705">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-705">value</span></span>  

### <a name="return-value---position"></a><span data-ttu-id="b5d86-706">戻り値 - position</span><span class="sxs-lookup"><span data-stu-id="b5d86-706">Return Value - position</span></span>

## <a name="method-previewinfo"></a><span data-ttu-id="b5d86-707">メソッド previewInfo</span><span class="sxs-lookup"><span data-stu-id="b5d86-707">Method previewInfo</span></span>

```xpp
public str previewInfo(str string)
```

### <a name="parameters---previewinfo"></a><span data-ttu-id="b5d86-708">パラメーター - previewInfo</span><span class="sxs-lookup"><span data-stu-id="b5d86-708">Parameters - previewInfo</span></span>

<span data-ttu-id="b5d86-709">文字列</span><span class="sxs-lookup"><span data-stu-id="b5d86-709">string</span></span>  

### <a name="return-value---previewinfo"></a><span data-ttu-id="b5d86-710">戻り値 - previewInfo</span><span class="sxs-lookup"><span data-stu-id="b5d86-710">Return Value - previewInfo</span></span>

## <a name="method-previewxcompensation100mm"></a><span data-ttu-id="b5d86-711">メソッド previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="b5d86-711">Method previewXCompensation100mm</span></span>

```xpp
public int previewXCompensation100mm(str string)
```

### <a name="parameters---previewxcompensation100mm"></a><span data-ttu-id="b5d86-712">パラメーター - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="b5d86-712">Parameters - previewXCompensation100mm</span></span>

<span data-ttu-id="b5d86-713">文字列</span><span class="sxs-lookup"><span data-stu-id="b5d86-713">string</span></span>  

### <a name="return-value---previewxcompensation100mm"></a><span data-ttu-id="b5d86-714">戻り値 - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="b5d86-714">Return Value - previewXCompensation100mm</span></span>

## <a name="method-right100mm"></a><span data-ttu-id="b5d86-715">メソッド right100mm</span><span class="sxs-lookup"><span data-stu-id="b5d86-715">Method right100mm</span></span>

```xpp
public int right100mm()
```

### <a name="return-value---right100mm"></a><span data-ttu-id="b5d86-716">戻り値 - right100mm</span><span class="sxs-lookup"><span data-stu-id="b5d86-716">Return Value - right100mm</span></span>

## <a name="method-right100mminclborder"></a><span data-ttu-id="b5d86-717">メソッド right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b5d86-717">Method right100mmInclBorder</span></span>

```xpp
public int right100mmInclBorder()
```

### <a name="return-value---right100mminclborder"></a><span data-ttu-id="b5d86-718">戻り値 - right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b5d86-718">Return Value - right100mmInclBorder</span></span>

## <a name="method-rightmarginandframe"></a><span data-ttu-id="b5d86-719">メソッド rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="b5d86-719">Method rightMarginAndFrame</span></span>

```xpp
public int rightMarginAndFrame()
```

### <a name="return-value---rightmarginandframe"></a><span data-ttu-id="b5d86-720">戻り値 - rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="b5d86-720">Return Value - rightMarginAndFrame</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="b5d86-721">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-721">Method rightMarginMode</span></span>

```xpp
public int rightMarginMode([int value])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="b5d86-722">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-722">Parameters - rightMarginMode</span></span>

<span data-ttu-id="b5d86-723">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-723">value</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="b5d86-724">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-724">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginstr"></a><span data-ttu-id="b5d86-725">メソッド rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-725">Method rightMarginStr</span></span>

```xpp
public str rightMarginStr([str value])
```

### <a name="parameters---rightmarginstr"></a><span data-ttu-id="b5d86-726">パラメーター - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-726">Parameters - rightMarginStr</span></span>

<span data-ttu-id="b5d86-727">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-727">value</span></span>  

### <a name="return-value---rightmarginstr"></a><span data-ttu-id="b5d86-728">戻り値 - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-728">Return Value - rightMarginStr</span></span>

## <a name="method-rightmarginunit"></a><span data-ttu-id="b5d86-729">メソッド rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-729">Method rightMarginUnit</span></span>

```xpp
public Units rightMarginUnit([Units value])
```

### <a name="parameters---rightmarginunit"></a><span data-ttu-id="b5d86-730">パラメーター - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-730">Parameters - rightMarginUnit</span></span>

<span data-ttu-id="b5d86-731">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-731">value</span></span>  

### <a name="return-value---rightmarginunit"></a><span data-ttu-id="b5d86-732">戻り値 - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-732">Return Value - rightMarginUnit</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="b5d86-733">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-733">Method rightMarginValue</span></span>

```xpp
public Real rightMarginValue([Real value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="b5d86-734">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-734">Parameters - rightMarginValue</span></span>

<span data-ttu-id="b5d86-735">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-735">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="b5d86-736">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-736">Return Value - rightMarginValue</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="b5d86-737">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="b5d86-737">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="b5d86-738">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="b5d86-738">Parameters - securityKey</span></span>

<span data-ttu-id="b5d86-739">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-739">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="b5d86-740">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="b5d86-740">Return Value - securityKey</span></span>

## <a name="method-setheightgettext"></a><span data-ttu-id="b5d86-741">メソッド setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="b5d86-741">Method setHeightGetText</span></span>

```xpp
public str setHeightGetText(int lines, str string)
```

### <a name="parameters---setheightgettext"></a><span data-ttu-id="b5d86-742">パラメーター - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="b5d86-742">Parameters - setHeightGetText</span></span>

<span data-ttu-id="b5d86-743">明細行</span><span class="sxs-lookup"><span data-stu-id="b5d86-743">lines</span></span>  

<!-- -->

<span data-ttu-id="b5d86-744">文字列</span><span class="sxs-lookup"><span data-stu-id="b5d86-744">string</span></span>  

### <a name="return-value---setheightgettext"></a><span data-ttu-id="b5d86-745">戻り値 - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="b5d86-745">Return Value - setHeightGetText</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="b5d86-746">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="b5d86-746">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="b5d86-747">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="b5d86-747">Parameters - showLabel</span></span>

<span data-ttu-id="b5d86-748">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-748">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="b5d86-749">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="b5d86-749">Return Value - showLabel</span></span>

## <a name="method-table"></a><span data-ttu-id="b5d86-750">メソッド table</span><span class="sxs-lookup"><span data-stu-id="b5d86-750">Method table</span></span>

<span data-ttu-id="b5d86-751">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-751">Gets or sets the table ID associated with the object.</span></span>

```xpp
public TableId table([TableId value])
```

### <a name="parameters---table"></a><span data-ttu-id="b5d86-752">パラメーター - table</span><span class="sxs-lookup"><span data-stu-id="b5d86-752">Parameters - table</span></span>

<span data-ttu-id="b5d86-753">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-753">value</span></span>  

### <a name="return-value---table"></a><span data-ttu-id="b5d86-754">戻り値 - toBlob</span><span class="sxs-lookup"><span data-stu-id="b5d86-754">Return Value - table</span></span>

<span data-ttu-id="b5d86-755">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="b5d86-755">The current value of the table ID associated with the object.</span></span>

## <a name="method-thickness"></a><span data-ttu-id="b5d86-756">メソッド thickness</span><span class="sxs-lookup"><span data-stu-id="b5d86-756">Method thickness</span></span>

```xpp
public LineThickness thickness([LineThickness value])
```

### <a name="parameters---thickness"></a><span data-ttu-id="b5d86-757">パラメーター - thickness</span><span class="sxs-lookup"><span data-stu-id="b5d86-757">Parameters - thickness</span></span>

<span data-ttu-id="b5d86-758">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-758">value</span></span>  

### <a name="return-value---thickness"></a><span data-ttu-id="b5d86-759">戻り値 - thickness</span><span class="sxs-lookup"><span data-stu-id="b5d86-759">Return Value - thickness</span></span>

## <a name="method-top100mm"></a><span data-ttu-id="b5d86-760">メソッド top100mm</span><span class="sxs-lookup"><span data-stu-id="b5d86-760">Method top100mm</span></span>

```xpp
public int top100mm([int topExclBorder])
```

### <a name="parameters---top100mm"></a><span data-ttu-id="b5d86-761">パラメーター - top100mm</span><span class="sxs-lookup"><span data-stu-id="b5d86-761">Parameters - top100mm</span></span>

<span data-ttu-id="b5d86-762">topExclBorder</span><span class="sxs-lookup"><span data-stu-id="b5d86-762">topExclBorder</span></span>  

### <a name="return-value---top100mm"></a><span data-ttu-id="b5d86-763">戻り値 - top100mm</span><span class="sxs-lookup"><span data-stu-id="b5d86-763">Return Value - top100mm</span></span>

## <a name="method-top100mminclborder"></a><span data-ttu-id="b5d86-764">メソッド top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b5d86-764">Method top100mmInclBorder</span></span>

```xpp
public int top100mmInclBorder([int topInclBorder])
```

### <a name="parameters---top100mminclborder"></a><span data-ttu-id="b5d86-765">パラメーター - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b5d86-765">Parameters - top100mmInclBorder</span></span>

<span data-ttu-id="b5d86-766">topInclBorder</span><span class="sxs-lookup"><span data-stu-id="b5d86-766">topInclBorder</span></span>  

### <a name="return-value---top100mminclborder"></a><span data-ttu-id="b5d86-767">戻り値 - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b5d86-767">Return Value - top100mmInclBorder</span></span>

## <a name="method-topmarginandframe"></a><span data-ttu-id="b5d86-768">メソッド topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="b5d86-768">Method topMarginAndFrame</span></span>

```xpp
public int topMarginAndFrame()
```

### <a name="return-value---topmarginandframe"></a><span data-ttu-id="b5d86-769">戻り値 - topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="b5d86-769">Return Value - topMarginAndFrame</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="b5d86-770">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-770">Method topMarginMode</span></span>

```xpp
public int topMarginMode([int value])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="b5d86-771">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-771">Parameters - topMarginMode</span></span>

<span data-ttu-id="b5d86-772">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-772">value</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="b5d86-773">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-773">Return Value - topMarginMode</span></span>

## <a name="method-topmarginstr"></a><span data-ttu-id="b5d86-774">メソッド topMarginStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-774">Method topMarginStr</span></span>

```xpp
public str topMarginStr([str value])
```

### <a name="parameters---topmarginstr"></a><span data-ttu-id="b5d86-775">パラメーター - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-775">Parameters - topMarginStr</span></span>

<span data-ttu-id="b5d86-776">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-776">value</span></span>  

### <a name="return-value---topmarginstr"></a><span data-ttu-id="b5d86-777">戻り値 - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-777">Return Value - topMarginStr</span></span>

## <a name="method-topmarginunit"></a><span data-ttu-id="b5d86-778">メソッド topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-778">Method topMarginUnit</span></span>

```xpp
public Units topMarginUnit([Units value])
```

### <a name="parameters---topmarginunit"></a><span data-ttu-id="b5d86-779">パラメーター - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-779">Parameters - topMarginUnit</span></span>

<span data-ttu-id="b5d86-780">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-780">value</span></span>  

### <a name="return-value---topmarginunit"></a><span data-ttu-id="b5d86-781">戻り値 - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-781">Return Value - topMarginUnit</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="b5d86-782">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-782">Method topMarginValue</span></span>

```xpp
public Real topMarginValue([Real value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="b5d86-783">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-783">Parameters - topMarginValue</span></span>

<span data-ttu-id="b5d86-784">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-784">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="b5d86-785">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-785">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="b5d86-786">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-786">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="b5d86-787">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-787">Parameters - topMode</span></span>

<span data-ttu-id="b5d86-788">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-788">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="b5d86-789">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-789">Return Value - topMode</span></span>

## <a name="method-topstr"></a><span data-ttu-id="b5d86-790">メソッド topStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-790">Method topStr</span></span>

```xpp
public str topStr([str value])
```

### <a name="parameters---topstr"></a><span data-ttu-id="b5d86-791">パラメーター - topStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-791">Parameters - topStr</span></span>

<span data-ttu-id="b5d86-792">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-792">value</span></span>  

### <a name="return-value---topstr"></a><span data-ttu-id="b5d86-793">戻り値 - topStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-793">Return Value - topStr</span></span>

## <a name="method-topunit"></a><span data-ttu-id="b5d86-794">メソッド topUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-794">Method topUnit</span></span>

```xpp
public Units topUnit([Units value])
```

### <a name="parameters---topunit"></a><span data-ttu-id="b5d86-795">パラメーター - topUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-795">Parameters - topUnit</span></span>

<span data-ttu-id="b5d86-796">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-796">value</span></span>  

### <a name="return-value---topunit"></a><span data-ttu-id="b5d86-797">戻り値 - topUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-797">Return Value - topUnit</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="b5d86-798">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-798">Method topValue</span></span>

```xpp
public Real topValue([Real value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="b5d86-799">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-799">Parameters - topValue</span></span>

<span data-ttu-id="b5d86-800">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-800">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="b5d86-801">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-801">Return Value - topValue</span></span>

## <a name="method-underline"></a><span data-ttu-id="b5d86-802">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="b5d86-802">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="b5d86-803">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="b5d86-803">Parameters - underline</span></span>

<span data-ttu-id="b5d86-804">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-804">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="b5d86-805">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="b5d86-805">Return Value - underline</span></span>

## <a name="method-visible"></a><span data-ttu-id="b5d86-806">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="b5d86-806">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="b5d86-807">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="b5d86-807">Parameters - visible</span></span>

<span data-ttu-id="b5d86-808">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-808">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="b5d86-809">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="b5d86-809">Return Value - visible</span></span>

## <a name="method-webmenuitemname"></a><span data-ttu-id="b5d86-810">メソッド webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="b5d86-810">Method webMenuItemName</span></span>

```xpp
public str webMenuItemName([str value])
```

### <a name="parameters---webmenuitemname"></a><span data-ttu-id="b5d86-811">パラメーター - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="b5d86-811">Parameters - webMenuItemName</span></span>

<span data-ttu-id="b5d86-812">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-812">value</span></span>  

### <a name="return-value---webmenuitemname"></a><span data-ttu-id="b5d86-813">戻り値 - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="b5d86-813">Return Value - webMenuItemName</span></span>

## <a name="method-webmenuitemtype"></a><span data-ttu-id="b5d86-814">メソッド webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="b5d86-814">Method webMenuItemType</span></span>

```xpp
public WebMenuItemType webMenuItemType([WebMenuItemType value])
```

### <a name="parameters---webmenuitemtype"></a><span data-ttu-id="b5d86-815">パラメーター - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="b5d86-815">Parameters - webMenuItemType</span></span>

<span data-ttu-id="b5d86-816">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-816">value</span></span>  

### <a name="return-value---webmenuitemtype"></a><span data-ttu-id="b5d86-817">戻り値 - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="b5d86-817">Return Value - webMenuItemType</span></span>

## <a name="method-webtarget"></a><span data-ttu-id="b5d86-818">メソッド webTarget</span><span class="sxs-lookup"><span data-stu-id="b5d86-818">Method webTarget</span></span>

```xpp
public str webTarget([str value])
```

### <a name="parameters---webtarget"></a><span data-ttu-id="b5d86-819">パラメーター - webTarget</span><span class="sxs-lookup"><span data-stu-id="b5d86-819">Parameters - webTarget</span></span>

<span data-ttu-id="b5d86-820">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-820">value</span></span>  

### <a name="return-value---webtarget"></a><span data-ttu-id="b5d86-821">戻り値 - webTarget</span><span class="sxs-lookup"><span data-stu-id="b5d86-821">Return Value - webTarget</span></span>

## <a name="method-width100mm"></a><span data-ttu-id="b5d86-822">メソッド width100mm</span><span class="sxs-lookup"><span data-stu-id="b5d86-822">Method width100mm</span></span>

```xpp
public int width100mm([int widthExclBorder])
```

### <a name="parameters---width100mm"></a><span data-ttu-id="b5d86-823">パラメーター - width100mm</span><span class="sxs-lookup"><span data-stu-id="b5d86-823">Parameters - width100mm</span></span>

<span data-ttu-id="b5d86-824">widthExclBorder</span><span class="sxs-lookup"><span data-stu-id="b5d86-824">widthExclBorder</span></span>  

### <a name="return-value---width100mm"></a><span data-ttu-id="b5d86-825">戻り値 - width100mm</span><span class="sxs-lookup"><span data-stu-id="b5d86-825">Return Value - width100mm</span></span>

## <a name="method-width100mminclborder"></a><span data-ttu-id="b5d86-826">メソッド width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b5d86-826">Method width100mmInclBorder</span></span>

```xpp
public int width100mmInclBorder([int widthInclBorder])
```

### <a name="parameters---width100mminclborder"></a><span data-ttu-id="b5d86-827">パラメーター - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b5d86-827">Parameters - width100mmInclBorder</span></span>

<span data-ttu-id="b5d86-828">widthInclBorder</span><span class="sxs-lookup"><span data-stu-id="b5d86-828">widthInclBorder</span></span>  

### <a name="return-value---width100mminclborder"></a><span data-ttu-id="b5d86-829">戻り値 - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b5d86-829">Return Value - width100mmInclBorder</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="b5d86-830">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-830">Method widthMode</span></span>

<span data-ttu-id="b5d86-831">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-831">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="b5d86-832">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-832">Parameters - widthMode</span></span>

<span data-ttu-id="b5d86-833">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-833">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="b5d86-834">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-834">Return Value - widthMode</span></span>

<span data-ttu-id="b5d86-835">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b5d86-835">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="b5d86-836">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="b5d86-836">Remarks - widthMode</span></span>

<span data-ttu-id="b5d86-837">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="b5d86-837">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="b5d86-838">モード。</span><span class="sxs-lookup"><span data-stu-id="b5d86-838">Mode.</span></span>         | <span data-ttu-id="b5d86-839">幅計算。</span><span class="sxs-lookup"><span data-stu-id="b5d86-839">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d86-840">正確。</span><span class="sxs-lookup"><span data-stu-id="b5d86-840">Exact.</span></span>        | <span data-ttu-id="b5d86-841">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b5d86-841">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b5d86-842">自動。</span><span class="sxs-lookup"><span data-stu-id="b5d86-842">Auto.</span></span>         | <span data-ttu-id="b5d86-843">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b5d86-843">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b5d86-844">列の幅。</span><span class="sxs-lookup"><span data-stu-id="b5d86-844">Column width.</span></span> | <span data-ttu-id="b5d86-845">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="b5d86-845">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="b5d86-846">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="b5d86-846">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthofstring100mm"></a><span data-ttu-id="b5d86-847">メソッド widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="b5d86-847">Method widthOfString100mm</span></span>

```xpp
public int widthOfString100mm(str string)
```

### <a name="parameters---widthofstring100mm"></a><span data-ttu-id="b5d86-848">パラメーター - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="b5d86-848">Parameters - widthOfString100mm</span></span>

<span data-ttu-id="b5d86-849">文字列</span><span class="sxs-lookup"><span data-stu-id="b5d86-849">string</span></span>  

### <a name="return-value---widthofstring100mm"></a><span data-ttu-id="b5d86-850">戻り値 - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="b5d86-850">Return Value - widthOfString100mm</span></span>

## <a name="method-widthstr"></a><span data-ttu-id="b5d86-851">メソッド widthStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-851">Method widthStr</span></span>

```xpp
public str widthStr([str value])
```

### <a name="parameters---widthstr"></a><span data-ttu-id="b5d86-852">パラメーター - widthStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-852">Parameters - widthStr</span></span>

<span data-ttu-id="b5d86-853">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-853">value</span></span>  

### <a name="return-value---widthstr"></a><span data-ttu-id="b5d86-854">戻り値 - widthStr</span><span class="sxs-lookup"><span data-stu-id="b5d86-854">Return Value - widthStr</span></span>

## <a name="method-widthunit"></a><span data-ttu-id="b5d86-855">メソッド widthUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-855">Method widthUnit</span></span>

```xpp
public Units widthUnit([Units value])
```

### <a name="parameters---widthunit"></a><span data-ttu-id="b5d86-856">パラメーター - widthUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-856">Parameters - widthUnit</span></span>

<span data-ttu-id="b5d86-857">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-857">value</span></span>  

### <a name="return-value---widthunit"></a><span data-ttu-id="b5d86-858">戻り値 - widthUnit</span><span class="sxs-lookup"><span data-stu-id="b5d86-858">Return Value - widthUnit</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="b5d86-859">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-859">Method widthValue</span></span>

<span data-ttu-id="b5d86-860">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-860">Gets or sets the width of the control.</span></span>

```xpp
public Real widthValue([Real value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="b5d86-861">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-861">Parameters - widthValue</span></span>

<span data-ttu-id="b5d86-862">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-862">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="b5d86-863">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-863">Return Value - widthValue</span></span>

<span data-ttu-id="b5d86-864">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="b5d86-864">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="b5d86-865">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="b5d86-865">Remarks - widthValue</span></span>

<span data-ttu-id="b5d86-866">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-866">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-width"></a><span data-ttu-id="b5d86-867">メソッド width</span><span class="sxs-lookup"><span data-stu-id="b5d86-867">Method width</span></span>

<span data-ttu-id="b5d86-868">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-868">Gets or sets the width of the control.</span></span>

```xpp
public void width(Real value, Units unit)
```

### <a name="parameters---width"></a><span data-ttu-id="b5d86-869">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="b5d86-869">Parameters - width</span></span>

<span data-ttu-id="b5d86-870">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-870">value</span></span>  

<!-- -->

<span data-ttu-id="b5d86-871">単位</span><span class="sxs-lookup"><span data-stu-id="b5d86-871">unit</span></span>  

### <a name="remarks---width"></a><span data-ttu-id="b5d86-872">備考 - width</span><span class="sxs-lookup"><span data-stu-id="b5d86-872">Remarks - width</span></span>

<span data-ttu-id="b5d86-873">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b5d86-873">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="b5d86-874">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="b5d86-874">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="b5d86-875">モード。</span><span class="sxs-lookup"><span data-stu-id="b5d86-875">Mode.</span></span>           | <span data-ttu-id="b5d86-876">幅計算。</span><span class="sxs-lookup"><span data-stu-id="b5d86-876">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d86-877">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="b5d86-877">-1 Exact.</span></span>       | <span data-ttu-id="b5d86-878">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b5d86-878">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b5d86-879">0 自動。</span><span class="sxs-lookup"><span data-stu-id="b5d86-879">0 Auto.</span></span>         | <span data-ttu-id="b5d86-880">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b5d86-880">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b5d86-881">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="b5d86-881">1 Column width.</span></span> | <span data-ttu-id="b5d86-882">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="b5d86-882">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="b5d86-883">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="b5d86-883">The width and width calculation mode can be set separately.</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="b5d86-884">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="b5d86-884">Method topMargin</span></span>

```xpp
public void topMargin(Real value, Units unit)
```

### <a name="parameters---topmargin"></a><span data-ttu-id="b5d86-885">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="b5d86-885">Parameters - topMargin</span></span>

<span data-ttu-id="b5d86-886">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-886">value</span></span>  

<!-- -->

<span data-ttu-id="b5d86-887">単位</span><span class="sxs-lookup"><span data-stu-id="b5d86-887">unit</span></span>  

## <a name="method-bottommargin"></a><span data-ttu-id="b5d86-888">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="b5d86-888">Method bottomMargin</span></span>

```xpp
public void bottomMargin(Real value, Units unit)
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="b5d86-889">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="b5d86-889">Parameters - bottomMargin</span></span>

<span data-ttu-id="b5d86-890">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-890">value</span></span>  

<!-- -->

<span data-ttu-id="b5d86-891">単位</span><span class="sxs-lookup"><span data-stu-id="b5d86-891">unit</span></span>  

## <a name="method-rightmargin"></a><span data-ttu-id="b5d86-892">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="b5d86-892">Method rightMargin</span></span>

```xpp
public void rightMargin(Real value, Units unit)
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="b5d86-893">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="b5d86-893">Parameters - rightMargin</span></span>

<span data-ttu-id="b5d86-894">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-894">value</span></span>  

<!-- -->

<span data-ttu-id="b5d86-895">単位</span><span class="sxs-lookup"><span data-stu-id="b5d86-895">unit</span></span>  

## <a name="method-leftmargin"></a><span data-ttu-id="b5d86-896">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="b5d86-896">Method leftMargin</span></span>

```xpp
public void leftMargin(Real value, Units unit)
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="b5d86-897">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="b5d86-897">Parameters - leftMargin</span></span>

<span data-ttu-id="b5d86-898">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-898">value</span></span>  

<!-- -->

<span data-ttu-id="b5d86-899">単位</span><span class="sxs-lookup"><span data-stu-id="b5d86-899">unit</span></span>  

## <a name="method-show"></a><span data-ttu-id="b5d86-900">メソッド show</span><span class="sxs-lookup"><span data-stu-id="b5d86-900">Method show</span></span>

```xpp
public void show()
```

## <a name="method-hide"></a><span data-ttu-id="b5d86-901">メソッド hide</span><span class="sxs-lookup"><span data-stu-id="b5d86-901">Method hide</span></span>

```xpp
public void hide()
```

## <a name="method-top"></a><span data-ttu-id="b5d86-902">メソッド top</span><span class="sxs-lookup"><span data-stu-id="b5d86-902">Method top</span></span>

```xpp
public void top(Real value, Units unit)
```

### <a name="parameters---top"></a><span data-ttu-id="b5d86-903">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="b5d86-903">Parameters - top</span></span>

<span data-ttu-id="b5d86-904">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-904">value</span></span>  

<!-- -->

<span data-ttu-id="b5d86-905">単位</span><span class="sxs-lookup"><span data-stu-id="b5d86-905">unit</span></span>  

## <a name="method-left"></a><span data-ttu-id="b5d86-906">メソッド left</span><span class="sxs-lookup"><span data-stu-id="b5d86-906">Method left</span></span>

```xpp
public void left(Real value, Units unit)
```

### <a name="parameters---left"></a><span data-ttu-id="b5d86-907">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="b5d86-907">Parameters - left</span></span>

<span data-ttu-id="b5d86-908">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-908">value</span></span>  

<!-- -->

<span data-ttu-id="b5d86-909">単位</span><span class="sxs-lookup"><span data-stu-id="b5d86-909">unit</span></span>  

## <a name="method-labelwidth"></a><span data-ttu-id="b5d86-910">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="b5d86-910">Method labelWidth</span></span>

```xpp
public void labelWidth(Real value, Units unit)
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="b5d86-911">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="b5d86-911">Parameters - labelWidth</span></span>

<span data-ttu-id="b5d86-912">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-912">value</span></span>  

<!-- -->

<span data-ttu-id="b5d86-913">単位</span><span class="sxs-lookup"><span data-stu-id="b5d86-913">unit</span></span>  

## <a name="method-height"></a><span data-ttu-id="b5d86-914">メソッド height</span><span class="sxs-lookup"><span data-stu-id="b5d86-914">Method height</span></span>

<span data-ttu-id="b5d86-915">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b5d86-915">Gets or sets the height of the control.</span></span>

```xpp
public void height(Real value, Units unit)
```

### <a name="parameters---height"></a><span data-ttu-id="b5d86-916">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="b5d86-916">Parameters - height</span></span>

<span data-ttu-id="b5d86-917">値</span><span class="sxs-lookup"><span data-stu-id="b5d86-917">value</span></span>  

<!-- -->

<span data-ttu-id="b5d86-918">単位</span><span class="sxs-lookup"><span data-stu-id="b5d86-918">unit</span></span>  

### <a name="remarks---height"></a><span data-ttu-id="b5d86-919">備考 - height</span><span class="sxs-lookup"><span data-stu-id="b5d86-919">Remarks - height</span></span>

<span data-ttu-id="b5d86-920">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b5d86-920">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="b5d86-921">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="b5d86-921">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="b5d86-922">モード。</span><span class="sxs-lookup"><span data-stu-id="b5d86-922">Mode.</span></span>            | <span data-ttu-id="b5d86-923">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="b5d86-923">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d86-924">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="b5d86-924">-1 Exact.</span></span>        | <span data-ttu-id="b5d86-925">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b5d86-925">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b5d86-926">0 自動。</span><span class="sxs-lookup"><span data-stu-id="b5d86-926">0 Auto.</span></span>          | <span data-ttu-id="b5d86-927">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b5d86-927">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b5d86-928">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="b5d86-928">1 Column height.</span></span> | <span data-ttu-id="b5d86-929">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="b5d86-929">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="b5d86-930">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="b5d86-930">The height and height calculation mode can be set separately.</span></span>

