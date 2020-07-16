---
title: ReportStringControl クラス
description: このトピックでは、ReportStringControl クラスについて説明します。
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
ms.openlocfilehash: 1a65d515fc4f5311261230f0638e8a25c6b67b9e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502828"
---
# <a name="class-reportstringcontrol"></a><span data-ttu-id="80dfc-103">クラス ReportStringControl</span><span class="sxs-lookup"><span data-stu-id="80dfc-103">Class ReportStringControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ReportStringControl extends ReportControl
```

<span data-ttu-id="80dfc-104">ReportStringControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="80dfc-104">The ReportStringControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="80dfc-105">備考</span><span class="sxs-lookup"><span data-stu-id="80dfc-105">Remarks</span></span>

<span data-ttu-id="80dfc-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="80dfc-107">例</span><span class="sxs-lookup"><span data-stu-id="80dfc-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="80dfc-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="80dfc-108">Methods</span></span>

| <span data-ttu-id="80dfc-109">方法</span><span class="sxs-lookup"><span data-stu-id="80dfc-109">Method</span></span>                                                                   | <span data-ttu-id="80dfc-110">説明</span><span class="sxs-lookup"><span data-stu-id="80dfc-110">Description</span></span>                                                                                                                               |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80dfc-111">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-111">public int alignment(\[int value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="80dfc-112">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-112">public int arrayIndex(\[int value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="80dfc-113">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-113">public boolean autoDeclaration(\[boolean value\])</span></span>                        | <span data-ttu-id="80dfc-114">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-114">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                        |
| <span data-ttu-id="80dfc-115">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-115">public int backgroundColor(\[int value\])</span></span>                                | <span data-ttu-id="80dfc-116">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-116">Gets or sets the background color of the control.</span></span>                                                                                         |
| <span data-ttu-id="80dfc-117">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-117">public int backStyle(\[int value\])</span></span>                                      | <span data-ttu-id="80dfc-118">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-118">Determines whether the control background can be transparent.</span></span>                                                                             |
| <span data-ttu-id="80dfc-119">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-119">public int bold(\[int value\])</span></span>                                           | <span data-ttu-id="80dfc-120">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-120">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                               |
| <span data-ttu-id="80dfc-121">public int bottomMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="80dfc-121">public int bottomMarginAndFrame()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="80dfc-122">public int bottomMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-122">public int bottomMarginMode(\[int value\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="80dfc-123">public str bottomMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-123">public str bottomMarginStr(\[str value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="80dfc-124">public Units bottomMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-124">public Units bottomMarginUnit(\[Units value\])</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="80dfc-125">public Real bottomMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-125">public Real bottomMarginValue(\[Real value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="80dfc-126">public int changeCase(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-126">public int changeCase(\[int value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="80dfc-127">public int changeLabelCase(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-127">public int changeLabelCase(\[int value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="80dfc-128">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-128">public int characterSet(\[int value\])</span></span>                                   | <span data-ttu-id="80dfc-129">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-129">Gets or sets the character set of the font.</span></span>                                                                                               |
| <span data-ttu-id="80dfc-130">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-130">public int colorScheme(\[int value\])</span></span>                                    | <span data-ttu-id="80dfc-131">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-131">Gets or sets the color scheme of the control.</span></span>                                                                                             |
| <span data-ttu-id="80dfc-132">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-132">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="80dfc-133">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-133">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                       |
| <span data-ttu-id="80dfc-134">public ReportFieldType controlType()</span><span class="sxs-lookup"><span data-stu-id="80dfc-134">public ReportFieldType controlType()</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="80dfc-135">public str cssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-135">public str cssClass(\[str value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="80dfc-136">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-136">public FieldId dataField(\[FieldId value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="80dfc-137">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-137">public str dataMethod(\[str value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="80dfc-138">public int delete()</span><span class="sxs-lookup"><span data-stu-id="80dfc-138">public int delete()</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="80dfc-139">public boolean dynamicHeight(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-139">public boolean dynamicHeight(\[boolean value\])</span></span>                          |                                                                                                                                           |
| <span data-ttu-id="80dfc-140">public str effectiveFont()</span><span class="sxs-lookup"><span data-stu-id="80dfc-140">public str effectiveFont()</span></span>                                               |                                                                                                                                           |
| <span data-ttu-id="80dfc-141">public str eval()</span><span class="sxs-lookup"><span data-stu-id="80dfc-141">public str eval()</span></span>                                                        |                                                                                                                                           |
| <span data-ttu-id="80dfc-142">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-142">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>         |                                                                                                                                           |
| <span data-ttu-id="80dfc-143">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-143">public str font(\[str value\])</span></span>                                           | <span data-ttu-id="80dfc-144">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-144">Gets or sets the name of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="80dfc-145">public str fontInfoPrinter()</span><span class="sxs-lookup"><span data-stu-id="80dfc-145">public str fontInfoPrinter()</span></span>                                             |                                                                                                                                           |
| <span data-ttu-id="80dfc-146">public int fontInfoPrinterAscent()</span><span class="sxs-lookup"><span data-stu-id="80dfc-146">public int fontInfoPrinterAscent()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="80dfc-147">public int fontInfoPrinterDescent()</span><span class="sxs-lookup"><span data-stu-id="80dfc-147">public int fontInfoPrinterDescent()</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="80dfc-148">public int fontInfoPrinterExtLead()</span><span class="sxs-lookup"><span data-stu-id="80dfc-148">public int fontInfoPrinterExtLead()</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="80dfc-149">public int fontInfoPrinterHeight()</span><span class="sxs-lookup"><span data-stu-id="80dfc-149">public int fontInfoPrinterHeight()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="80dfc-150">public int fontInfoPrinterIntLead()</span><span class="sxs-lookup"><span data-stu-id="80dfc-150">public int fontInfoPrinterIntLead()</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="80dfc-151">public str fontInfoScreen()</span><span class="sxs-lookup"><span data-stu-id="80dfc-151">public str fontInfoScreen()</span></span>                                              |                                                                                                                                           |
| <span data-ttu-id="80dfc-152">public int fontInfoScreenAscent()</span><span class="sxs-lookup"><span data-stu-id="80dfc-152">public int fontInfoScreenAscent()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="80dfc-153">public int fontInfoScreenDescent()</span><span class="sxs-lookup"><span data-stu-id="80dfc-153">public int fontInfoScreenDescent()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="80dfc-154">public int fontInfoScreenExtLead()</span><span class="sxs-lookup"><span data-stu-id="80dfc-154">public int fontInfoScreenExtLead()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="80dfc-155">public int fontInfoScreenHeight()</span><span class="sxs-lookup"><span data-stu-id="80dfc-155">public int fontInfoScreenHeight()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="80dfc-156">public int fontInfoScreenIntLead()</span><span class="sxs-lookup"><span data-stu-id="80dfc-156">public int fontInfoScreenIntLead()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="80dfc-157">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-157">public int fontSize(\[int value\])</span></span>                                       | <span data-ttu-id="80dfc-158">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-158">Gets or sets the size of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="80dfc-159">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-159">public int foregroundColor(\[int value\])</span></span>                                | <span data-ttu-id="80dfc-160">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-160">Gets or sets the text color for the control to use.</span></span>                                                                                       |
| <span data-ttu-id="80dfc-161">public int height100mm(\[int heightExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-161">public int height100mm(\[int heightExclBorder\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="80dfc-162">public int height100mmInclBorder(\[int heightInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-162">public int height100mmInclBorder(\[int heightInclBorder\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="80dfc-163">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-163">public int heightMode(\[int value\])</span></span>                                     | <span data-ttu-id="80dfc-164">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-164">Gets or sets a calculation mode for the height of the control.</span></span>                                                                            |
| <span data-ttu-id="80dfc-165">public int heightOfWordWrappedString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="80dfc-165">public int heightOfWordWrappedString100mm(str string)</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="80dfc-166">public str heightStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-166">public str heightStr(\[str value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="80dfc-167">public Units heightUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-167">public Units heightUnit(\[Units value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="80dfc-168">public Real heightValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-168">public Real heightValue(\[Real value\])</span></span>                                  | <span data-ttu-id="80dfc-169">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-169">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="80dfc-170">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-170">public boolean italic(\[boolean value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="80dfc-171">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-171">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="80dfc-172">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-172">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="80dfc-173">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-173">public int labelBold(\[int value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="80dfc-174">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-174">public int labelCharacterSet(\[int value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="80dfc-175">public str labelCssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-175">public str labelCssClass(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="80dfc-176">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-176">public str labelFont(\[str value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="80dfc-177">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-177">public int labelFontSize(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="80dfc-178">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-178">public boolean labelItalic(\[boolean value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="80dfc-179">public LineType labelLineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-179">public LineType labelLineBelow(\[LineType value\])</span></span>                       |                                                                                                                                           |
| <span data-ttu-id="80dfc-180">public LineThickness labelLineThickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-180">public LineThickness labelLineThickness(\[LineThickness value\])</span></span>         |                                                                                                                                           |
| <span data-ttu-id="80dfc-181">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-181">public int labelPosition(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="80dfc-182">public int labelTabLeader(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-182">public int labelTabLeader(\[int value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="80dfc-183">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-183">public boolean labelUnderline(\[boolean value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="80dfc-184">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-184">public int labelWidthMode(\[int value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="80dfc-185">public str labelWidthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-185">public str labelWidthStr(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="80dfc-186">public Units labelWidthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-186">public Units labelWidthUnit(\[Units value\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="80dfc-187">public Real labelWidthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-187">public Real labelWidthValue(\[Real value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="80dfc-188">public int left100mm(\[int leftExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-188">public int left100mm(\[int leftExclBorder\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="80dfc-189">public int left100mmInclBorder(\[int leftInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-189">public int left100mmInclBorder(\[int leftInclBorder\])</span></span>                   |                                                                                                                                           |
| <span data-ttu-id="80dfc-190">public int leftMarginAnFrame()</span><span class="sxs-lookup"><span data-stu-id="80dfc-190">public int leftMarginAnFrame()</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="80dfc-191">public int leftMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-191">public int leftMarginMode(\[int value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="80dfc-192">public str leftMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-192">public str leftMarginStr(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="80dfc-193">public Units leftMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-193">public Units leftMarginUnit(\[Units value\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="80dfc-194">public Real leftMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-194">public Real leftMarginValue(\[Real value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="80dfc-195">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-195">public int leftMode(\[int value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="80dfc-196">public str leftStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-196">public str leftStr(\[str value\])</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="80dfc-197">public Units leftUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-197">public Units leftUnit(\[Units value\])</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="80dfc-198">public Real leftValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-198">public Real leftValue(\[Real value\])</span></span>                                    |                                                                                                                                           |
| <span data-ttu-id="80dfc-199">public LineType lineAbove(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-199">public LineType lineAbove(\[LineType value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="80dfc-200">public LineType lineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-200">public LineType lineBelow(\[LineType value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="80dfc-201">public LineType lineLeft(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-201">public LineType lineLeft(\[LineType value\])</span></span>                             | <span data-ttu-id="80dfc-202">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-202">Gets or sets the type of line that is used as the left border of a section.</span></span>                                                               |
| <span data-ttu-id="80dfc-203">public LineType lineRight(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-203">public LineType lineRight(\[LineType value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="80dfc-204">public str menuItemLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-204">public str menuItemLabel(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="80dfc-205">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-205">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="80dfc-206">public MenuItemType menuItemType(\[MenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-206">public MenuItemType menuItemType(\[MenuItemType value\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="80dfc-207">public str modelFieldName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-207">public str modelFieldName(\[str value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="80dfc-208">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-208">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="80dfc-209">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-209">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="80dfc-210">public int numberOfLines(int height100mm)</span><span class="sxs-lookup"><span data-stu-id="80dfc-210">public int numberOfLines(int height100mm)</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="80dfc-211">public int position(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-211">public int position(\[int value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="80dfc-212">public str previewInfo(str string)</span><span class="sxs-lookup"><span data-stu-id="80dfc-212">public str previewInfo(str string)</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="80dfc-213">public int previewXCompensation100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="80dfc-213">public int previewXCompensation100mm(str string)</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="80dfc-214">public int right100mm()</span><span class="sxs-lookup"><span data-stu-id="80dfc-214">public int right100mm()</span></span>                                                  |                                                                                                                                           |
| <span data-ttu-id="80dfc-215">public int right100mmInclBorder()</span><span class="sxs-lookup"><span data-stu-id="80dfc-215">public int right100mmInclBorder()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="80dfc-216">public int rightMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="80dfc-216">public int rightMarginAndFrame()</span></span>                                         |                                                                                                                                           |
| <span data-ttu-id="80dfc-217">public int rightMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-217">public int rightMarginMode(\[int value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="80dfc-218">public str rightMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-218">public str rightMarginStr(\[str value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="80dfc-219">public Units rightMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-219">public Units rightMarginUnit(\[Units value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="80dfc-220">public Real rightMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-220">public Real rightMarginValue(\[Real value\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="80dfc-221">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-221">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                                           |
| <span data-ttu-id="80dfc-222">public str setHeightGetText(int lines, str string)</span><span class="sxs-lookup"><span data-stu-id="80dfc-222">public str setHeightGetText(int lines, str string)</span></span>                       |                                                                                                                                           |
| <span data-ttu-id="80dfc-223">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-223">public boolean showLabel(\[boolean value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="80dfc-224">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-224">public TableId table(\[TableId value\])</span></span>                                  | <span data-ttu-id="80dfc-225">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-225">Gets or sets the table ID associated with the object.</span></span>                                                                                     |
| <span data-ttu-id="80dfc-226">public LineThickness thickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-226">public LineThickness thickness(\[LineThickness value\])</span></span>                  |                                                                                                                                           |
| <span data-ttu-id="80dfc-227">public int top100mm(\[int topExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-227">public int top100mm(\[int topExclBorder\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="80dfc-228">public int top100mmInclBorder(\[int topInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-228">public int top100mmInclBorder(\[int topInclBorder\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="80dfc-229">public int topMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="80dfc-229">public int topMarginAndFrame()</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="80dfc-230">public int topMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-230">public int topMarginMode(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="80dfc-231">public str topMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-231">public str topMarginStr(\[str value\])</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="80dfc-232">public Units topMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-232">public Units topMarginUnit(\[Units value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="80dfc-233">public Real topMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-233">public Real topMarginValue(\[Real value\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="80dfc-234">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-234">public int topMode(\[int value\])</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="80dfc-235">public str topStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-235">public str topStr(\[str value\])</span></span>                                         |                                                                                                                                           |
| <span data-ttu-id="80dfc-236">public Units topUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-236">public Units topUnit(\[Units value\])</span></span>                                    |                                                                                                                                           |
| <span data-ttu-id="80dfc-237">public Real topValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-237">public Real topValue(\[Real value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="80dfc-238">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-238">public boolean underline(\[boolean value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="80dfc-239">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-239">public boolean visible(\[boolean value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="80dfc-240">public str webMenuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-240">public str webMenuItemName(\[str value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="80dfc-241">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-241">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span></span>        |                                                                                                                                           |
| <span data-ttu-id="80dfc-242">public str webTarget(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-242">public str webTarget(\[str value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="80dfc-243">public int width100mm(\[int widthExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-243">public int width100mm(\[int widthExclBorder\])</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="80dfc-244">public int width100mmInclBorder(\[int widthInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-244">public int width100mmInclBorder(\[int widthInclBorder\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="80dfc-245">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-245">public int widthMode(\[int value\])</span></span>                                      | <span data-ttu-id="80dfc-246">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-246">Gets or sets the calculation mode of the width of the control.</span></span>                                                                            |
| <span data-ttu-id="80dfc-247">public int widthOfString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="80dfc-247">public int widthOfString100mm(str string)</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="80dfc-248">public str widthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-248">public str widthStr(\[str value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="80dfc-249">public Units widthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-249">public Units widthUnit(\[Units value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="80dfc-250">public Real widthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="80dfc-250">public Real widthValue(\[Real value\])</span></span>                                   | <span data-ttu-id="80dfc-251">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-251">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="80dfc-252">public void height(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="80dfc-252">public void height(Real value, Units unit)</span></span>                               | <span data-ttu-id="80dfc-253">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-253">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="80dfc-254">public void topMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="80dfc-254">public void topMargin(Real value, Units unit)</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="80dfc-255">public void labelWidth(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="80dfc-255">public void labelWidth(Real value, Units unit)</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="80dfc-256">public void hide()</span><span class="sxs-lookup"><span data-stu-id="80dfc-256">public void hide()</span></span>                                                       |                                                                                                                                           |
| <span data-ttu-id="80dfc-257">public void left(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="80dfc-257">public void left(Real value, Units unit)</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="80dfc-258">public void rightMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="80dfc-258">public void rightMargin(Real value, Units unit)</span></span>                          |                                                                                                                                           |
| <span data-ttu-id="80dfc-259">public void show()</span><span class="sxs-lookup"><span data-stu-id="80dfc-259">public void show()</span></span>                                                       |                                                                                                                                           |
| <span data-ttu-id="80dfc-260">public void width(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="80dfc-260">public void width(Real value, Units unit)</span></span>                                | <span data-ttu-id="80dfc-261">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-261">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="80dfc-262">public void leftMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="80dfc-262">public void leftMargin(Real value, Units unit)</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="80dfc-263">public void bottomMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="80dfc-263">public void bottomMargin(Real value, Units unit)</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="80dfc-264">public void top(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="80dfc-264">public void top(Real value, Units unit)</span></span>                                  |                                                                                                                                           |

## <a name="method-alignment"></a><span data-ttu-id="80dfc-265">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="80dfc-265">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="80dfc-266">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="80dfc-266">Parameters - alignment</span></span>

<span data-ttu-id="80dfc-267">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-267">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="80dfc-268">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="80dfc-268">Return Value - alignment</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="80dfc-269">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="80dfc-269">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="80dfc-270">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="80dfc-270">Parameters - arrayIndex</span></span>

<span data-ttu-id="80dfc-271">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-271">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="80dfc-272">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="80dfc-272">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="80dfc-273">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="80dfc-273">Method autoDeclaration</span></span>

<span data-ttu-id="80dfc-274">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-274">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="80dfc-275">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="80dfc-275">Parameters - autoDeclaration</span></span>

<span data-ttu-id="80dfc-276">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-276">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="80dfc-277">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="80dfc-277">Return Value - autoDeclaration</span></span>

<span data-ttu-id="80dfc-278">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="80dfc-278">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="80dfc-279">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="80dfc-279">Remarks - autoDeclaration</span></span>

<span data-ttu-id="80dfc-280">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="80dfc-280">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="80dfc-281">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="80dfc-281">Method backgroundColor</span></span>

<span data-ttu-id="80dfc-282">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-282">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="80dfc-283">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="80dfc-283">Parameters - backgroundColor</span></span>

<span data-ttu-id="80dfc-284">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-284">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="80dfc-285">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="80dfc-285">Return Value - backgroundColor</span></span>

<span data-ttu-id="80dfc-286">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="80dfc-286">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="80dfc-287">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="80dfc-287">Remarks - backgroundColor</span></span>

<span data-ttu-id="80dfc-288">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="80dfc-288">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="80dfc-289">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="80dfc-289">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="80dfc-290">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="80dfc-290">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="80dfc-291">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="80dfc-291">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="80dfc-292">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="80dfc-292">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="80dfc-293">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="80dfc-293">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="80dfc-294">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="80dfc-294">Method backStyle</span></span>

<span data-ttu-id="80dfc-295">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-295">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="80dfc-296">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="80dfc-296">Parameters - backStyle</span></span>

<span data-ttu-id="80dfc-297">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-297">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="80dfc-298">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="80dfc-298">Return Value - backStyle</span></span>

<span data-ttu-id="80dfc-299">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="80dfc-299">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="80dfc-300">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="80dfc-300">Method bold</span></span>

<span data-ttu-id="80dfc-301">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-301">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="80dfc-302">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="80dfc-302">Parameters - bold</span></span>

<span data-ttu-id="80dfc-303">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-303">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="80dfc-304">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="80dfc-304">Return Value - bold</span></span>

<span data-ttu-id="80dfc-305">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="80dfc-305">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="80dfc-306">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="80dfc-306">Remarks - bold</span></span>

<span data-ttu-id="80dfc-307">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="80dfc-307">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="80dfc-308">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-308">0 Use the default font weight.</span></span>
-   <span data-ttu-id="80dfc-309">1 シン。</span><span class="sxs-lookup"><span data-stu-id="80dfc-309">1 Thin.</span></span>
-   <span data-ttu-id="80dfc-310">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="80dfc-310">2 Extra-light.</span></span>
-   <span data-ttu-id="80dfc-311">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="80dfc-311">3 Light.</span></span>
-   <span data-ttu-id="80dfc-312">4 標準。</span><span class="sxs-lookup"><span data-stu-id="80dfc-312">4 Normal.</span></span>
-   <span data-ttu-id="80dfc-313">5 中。</span><span class="sxs-lookup"><span data-stu-id="80dfc-313">5 Medium.</span></span>
-   <span data-ttu-id="80dfc-314">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="80dfc-314">6 Semibold.</span></span>
-   <span data-ttu-id="80dfc-315">7 太字。</span><span class="sxs-lookup"><span data-stu-id="80dfc-315">7 Bold.</span></span>
-   <span data-ttu-id="80dfc-316">8 極太。</span><span class="sxs-lookup"><span data-stu-id="80dfc-316">8 Extra-bold.</span></span>
-   <span data-ttu-id="80dfc-317">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="80dfc-317">9 Heavy.</span></span>

## <a name="method-bottommarginandframe"></a><span data-ttu-id="80dfc-318">メソッド bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="80dfc-318">Method bottomMarginAndFrame</span></span>

```xpp
public int bottomMarginAndFrame()
```

### <a name="return-value---bottommarginandframe"></a><span data-ttu-id="80dfc-319">戻り値 - bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="80dfc-319">Return Value - bottomMarginAndFrame</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="80dfc-320">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-320">Method bottomMarginMode</span></span>

```xpp
public int bottomMarginMode([int value])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="80dfc-321">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-321">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="80dfc-322">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-322">value</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="80dfc-323">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-323">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginstr"></a><span data-ttu-id="80dfc-324">メソッド bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-324">Method bottomMarginStr</span></span>

```xpp
public str bottomMarginStr([str value])
```

### <a name="parameters---bottommarginstr"></a><span data-ttu-id="80dfc-325">パラメーター - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-325">Parameters - bottomMarginStr</span></span>

<span data-ttu-id="80dfc-326">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-326">value</span></span>  

### <a name="return-value---bottommarginstr"></a><span data-ttu-id="80dfc-327">戻り値 - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-327">Return Value - bottomMarginStr</span></span>

## <a name="method-bottommarginunit"></a><span data-ttu-id="80dfc-328">メソッド bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-328">Method bottomMarginUnit</span></span>

```xpp
public Units bottomMarginUnit([Units value])
```

### <a name="parameters---bottommarginunit"></a><span data-ttu-id="80dfc-329">パラメーター - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-329">Parameters - bottomMarginUnit</span></span>

<span data-ttu-id="80dfc-330">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-330">value</span></span>  

### <a name="return-value---bottommarginunit"></a><span data-ttu-id="80dfc-331">戻り値 - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-331">Return Value - bottomMarginUnit</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="80dfc-332">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-332">Method bottomMarginValue</span></span>

```xpp
public Real bottomMarginValue([Real value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="80dfc-333">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-333">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="80dfc-334">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-334">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="80dfc-335">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-335">Return Value - bottomMarginValue</span></span>

## <a name="method-changecase"></a><span data-ttu-id="80dfc-336">メソッド changeCase</span><span class="sxs-lookup"><span data-stu-id="80dfc-336">Method changeCase</span></span>

```xpp
public int changeCase([int value])
```

### <a name="parameters---changecase"></a><span data-ttu-id="80dfc-337">パラメーター - changeCase</span><span class="sxs-lookup"><span data-stu-id="80dfc-337">Parameters - changeCase</span></span>

<span data-ttu-id="80dfc-338">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-338">value</span></span>  

### <a name="return-value---changecase"></a><span data-ttu-id="80dfc-339">戻り値 - changeCase</span><span class="sxs-lookup"><span data-stu-id="80dfc-339">Return Value - changeCase</span></span>

## <a name="method-changelabelcase"></a><span data-ttu-id="80dfc-340">メソッド changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="80dfc-340">Method changeLabelCase</span></span>

```xpp
public int changeLabelCase([int value])
```

### <a name="parameters---changelabelcase"></a><span data-ttu-id="80dfc-341">パラメーター - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="80dfc-341">Parameters - changeLabelCase</span></span>

<span data-ttu-id="80dfc-342">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-342">value</span></span>  

### <a name="return-value---changelabelcase"></a><span data-ttu-id="80dfc-343">戻り値 - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="80dfc-343">Return Value - changeLabelCase</span></span>

## <a name="method-characterset"></a><span data-ttu-id="80dfc-344">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="80dfc-344">Method characterSet</span></span>

<span data-ttu-id="80dfc-345">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-345">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="80dfc-346">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="80dfc-346">Parameters - characterSet</span></span>

<span data-ttu-id="80dfc-347">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-347">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="80dfc-348">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="80dfc-348">Return Value - characterSet</span></span>

<span data-ttu-id="80dfc-349">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="80dfc-349">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="80dfc-350">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="80dfc-350">Remarks - characterSet</span></span>

<span data-ttu-id="80dfc-351">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-351">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="80dfc-352">値です。</span><span class="sxs-lookup"><span data-stu-id="80dfc-352">Value.</span></span> | <span data-ttu-id="80dfc-353">説明。</span><span class="sxs-lookup"><span data-stu-id="80dfc-353">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="80dfc-354">0</span><span class="sxs-lookup"><span data-stu-id="80dfc-354">0</span></span>      | <span data-ttu-id="80dfc-355">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="80dfc-355">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="80dfc-356">1</span><span class="sxs-lookup"><span data-stu-id="80dfc-356">1</span></span>      | <span data-ttu-id="80dfc-357">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="80dfc-357">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="80dfc-358">2</span><span class="sxs-lookup"><span data-stu-id="80dfc-358">2</span></span>      | <span data-ttu-id="80dfc-359">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="80dfc-359">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="80dfc-360">77</span><span class="sxs-lookup"><span data-stu-id="80dfc-360">77</span></span>     | <span data-ttu-id="80dfc-361">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="80dfc-361">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="80dfc-362">128</span><span class="sxs-lookup"><span data-stu-id="80dfc-362">128</span></span>    | <span data-ttu-id="80dfc-363">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="80dfc-363">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="80dfc-364">129</span><span class="sxs-lookup"><span data-stu-id="80dfc-364">129</span></span>    | <span data-ttu-id="80dfc-365">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="80dfc-365">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="80dfc-366">134</span><span class="sxs-lookup"><span data-stu-id="80dfc-366">134</span></span>    | <span data-ttu-id="80dfc-367">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="80dfc-367">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="80dfc-368">136</span><span class="sxs-lookup"><span data-stu-id="80dfc-368">136</span></span>    | <span data-ttu-id="80dfc-369">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="80dfc-369">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="80dfc-370">161</span><span class="sxs-lookup"><span data-stu-id="80dfc-370">161</span></span>    | <span data-ttu-id="80dfc-371">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="80dfc-371">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="80dfc-372">162</span><span class="sxs-lookup"><span data-stu-id="80dfc-372">162</span></span>    | <span data-ttu-id="80dfc-373">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="80dfc-373">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="80dfc-374">163</span><span class="sxs-lookup"><span data-stu-id="80dfc-374">163</span></span>    | <span data-ttu-id="80dfc-375">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="80dfc-375">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="80dfc-376">186</span><span class="sxs-lookup"><span data-stu-id="80dfc-376">186</span></span>    | <span data-ttu-id="80dfc-377">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="80dfc-377">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="80dfc-378">204</span><span class="sxs-lookup"><span data-stu-id="80dfc-378">204</span></span>    | <span data-ttu-id="80dfc-379">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="80dfc-379">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="80dfc-380">238</span><span class="sxs-lookup"><span data-stu-id="80dfc-380">238</span></span>    | <span data-ttu-id="80dfc-381">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="80dfc-381">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="80dfc-382">255</span><span class="sxs-lookup"><span data-stu-id="80dfc-382">255</span></span>    | <span data-ttu-id="80dfc-383">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="80dfc-383">OEM\_CHARSET</span></span>         |

<span data-ttu-id="80dfc-384">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="80dfc-384">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="80dfc-385">値です。</span><span class="sxs-lookup"><span data-stu-id="80dfc-385">Value.</span></span> | <span data-ttu-id="80dfc-386">説明。</span><span class="sxs-lookup"><span data-stu-id="80dfc-386">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="80dfc-387">130</span><span class="sxs-lookup"><span data-stu-id="80dfc-387">130</span></span>    | <span data-ttu-id="80dfc-388">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="80dfc-388">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="80dfc-389">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="80dfc-389">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="80dfc-390">値です。</span><span class="sxs-lookup"><span data-stu-id="80dfc-390">Value.</span></span> | <span data-ttu-id="80dfc-391">説明。</span><span class="sxs-lookup"><span data-stu-id="80dfc-391">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="80dfc-392">177</span><span class="sxs-lookup"><span data-stu-id="80dfc-392">177</span></span>    | <span data-ttu-id="80dfc-393">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="80dfc-393">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="80dfc-394">178</span><span class="sxs-lookup"><span data-stu-id="80dfc-394">178</span></span>    | <span data-ttu-id="80dfc-395">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="80dfc-395">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="80dfc-396">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="80dfc-396">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="80dfc-397">値です。</span><span class="sxs-lookup"><span data-stu-id="80dfc-397">Value.</span></span> | <span data-ttu-id="80dfc-398">説明。</span><span class="sxs-lookup"><span data-stu-id="80dfc-398">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="80dfc-399">222</span><span class="sxs-lookup"><span data-stu-id="80dfc-399">222</span></span>    | <span data-ttu-id="80dfc-400">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="80dfc-400">THAI\_CHARSET</span></span> |

<span data-ttu-id="80dfc-401">既定の文字セットは、現在のシステム ロケールに基づく値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="80dfc-401">The default character set is set to a value that is based on the current system locale.</span></span> <span data-ttu-id="80dfc-402">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="80dfc-402">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="80dfc-403">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="80dfc-403">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="80dfc-404">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="80dfc-404">Method colorScheme</span></span>

<span data-ttu-id="80dfc-405">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-405">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="80dfc-406">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="80dfc-406">Parameters - colorScheme</span></span>

<span data-ttu-id="80dfc-407">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-407">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="80dfc-408">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="80dfc-408">Return Value - colorScheme</span></span>

<span data-ttu-id="80dfc-409">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="80dfc-409">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="80dfc-410">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="80dfc-410">Remarks - colorScheme</span></span>

<span data-ttu-id="80dfc-411">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="80dfc-411">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="80dfc-412">値です。</span><span class="sxs-lookup"><span data-stu-id="80dfc-412">Value.</span></span> | <span data-ttu-id="80dfc-413">スタイル。</span><span class="sxs-lookup"><span data-stu-id="80dfc-413">Style.</span></span>                 |
|--------|------------------------|
| <span data-ttu-id="80dfc-414">0</span><span class="sxs-lookup"><span data-stu-id="80dfc-414">0</span></span>      | <span data-ttu-id="80dfc-415">既定。</span><span class="sxs-lookup"><span data-stu-id="80dfc-415">Default.</span></span>               |
| <span data-ttu-id="80dfc-416">1</span><span class="sxs-lookup"><span data-stu-id="80dfc-416">1</span></span>      | <span data-ttu-id="80dfc-417">Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="80dfc-417">The Windows palette.</span></span>   |
| <span data-ttu-id="80dfc-418">2</span><span class="sxs-lookup"><span data-stu-id="80dfc-418">2</span></span>      | <span data-ttu-id="80dfc-419">真の配色。</span><span class="sxs-lookup"><span data-stu-id="80dfc-419">The true-color scheme.</span></span> |

## <a name="method-configurationkey"></a><span data-ttu-id="80dfc-420">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="80dfc-420">Method configurationKey</span></span>

<span data-ttu-id="80dfc-421">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-421">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="80dfc-422">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="80dfc-422">Parameters - configurationKey</span></span>

<span data-ttu-id="80dfc-423">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-423">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="80dfc-424">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="80dfc-424">Return Value - configurationKey</span></span>

<span data-ttu-id="80dfc-425">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="80dfc-425">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="80dfc-426">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="80dfc-426">Remarks - configurationKey</span></span>

<span data-ttu-id="80dfc-427">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="80dfc-427">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="80dfc-428">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="80dfc-428">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-controltype"></a><span data-ttu-id="80dfc-429">メソッド controlType</span><span class="sxs-lookup"><span data-stu-id="80dfc-429">Method controlType</span></span>

```xpp
public ReportFieldType controlType()
```

### <a name="return-value---controltype"></a><span data-ttu-id="80dfc-430">戻り値 - controlType</span><span class="sxs-lookup"><span data-stu-id="80dfc-430">Return Value - controlType</span></span>

## <a name="method-cssclass"></a><span data-ttu-id="80dfc-431">メソッド cssClass</span><span class="sxs-lookup"><span data-stu-id="80dfc-431">Method cssClass</span></span>

```xpp
public str cssClass([str value])
```

### <a name="parameters---cssclass"></a><span data-ttu-id="80dfc-432">パラメーター - cssClass</span><span class="sxs-lookup"><span data-stu-id="80dfc-432">Parameters - cssClass</span></span>

<span data-ttu-id="80dfc-433">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-433">value</span></span>  

### <a name="return-value---cssclass"></a><span data-ttu-id="80dfc-434">戻り値 - cssClass</span><span class="sxs-lookup"><span data-stu-id="80dfc-434">Return Value - cssClass</span></span>

## <a name="method-datafield"></a><span data-ttu-id="80dfc-435">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="80dfc-435">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="80dfc-436">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="80dfc-436">Parameters - dataField</span></span>

<span data-ttu-id="80dfc-437">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-437">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="80dfc-438">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="80dfc-438">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="80dfc-439">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="80dfc-439">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="80dfc-440">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="80dfc-440">Parameters - dataMethod</span></span>

<span data-ttu-id="80dfc-441">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-441">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="80dfc-442">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="80dfc-442">Return Value - dataMethod</span></span>

## <a name="method-delete"></a><span data-ttu-id="80dfc-443">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="80dfc-443">Method delete</span></span>

```xpp
public int delete()
```

### <a name="return-value---delete"></a><span data-ttu-id="80dfc-444">戻り値 - delete</span><span class="sxs-lookup"><span data-stu-id="80dfc-444">Return Value - delete</span></span>

## <a name="method-dynamicheight"></a><span data-ttu-id="80dfc-445">メソッド dynamicHeight</span><span class="sxs-lookup"><span data-stu-id="80dfc-445">Method dynamicHeight</span></span>

```xpp
public boolean dynamicHeight([boolean value])
```

### <a name="parameters---dynamicheight"></a><span data-ttu-id="80dfc-446">パラメーター - dynamicHeight</span><span class="sxs-lookup"><span data-stu-id="80dfc-446">Parameters - dynamicHeight</span></span>

<span data-ttu-id="80dfc-447">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-447">value</span></span>  

### <a name="return-value---dynamicheight"></a><span data-ttu-id="80dfc-448">戻り値 - dynamicHeight</span><span class="sxs-lookup"><span data-stu-id="80dfc-448">Return Value - dynamicHeight</span></span>

## <a name="method-effectivefont"></a><span data-ttu-id="80dfc-449">メソッド effectiveFont</span><span class="sxs-lookup"><span data-stu-id="80dfc-449">Method effectiveFont</span></span>

```xpp
public str effectiveFont()
```

### <a name="return-value---effectivefont"></a><span data-ttu-id="80dfc-450">戻り値 - effectiveFont</span><span class="sxs-lookup"><span data-stu-id="80dfc-450">Return Value - effectiveFont</span></span>

## <a name="method-eval"></a><span data-ttu-id="80dfc-451">メソッド eval</span><span class="sxs-lookup"><span data-stu-id="80dfc-451">Method eval</span></span>

```xpp
public str eval()
```

### <a name="return-value---eval"></a><span data-ttu-id="80dfc-452">戻り値 - eval</span><span class="sxs-lookup"><span data-stu-id="80dfc-452">Return Value - eval</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="80dfc-453">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="80dfc-453">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="80dfc-454">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="80dfc-454">Parameters - extendedDataType</span></span>

<span data-ttu-id="80dfc-455">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-455">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="80dfc-456">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="80dfc-456">Return Value - extendedDataType</span></span>

## <a name="method-font"></a><span data-ttu-id="80dfc-457">メソッド font</span><span class="sxs-lookup"><span data-stu-id="80dfc-457">Method font</span></span>

<span data-ttu-id="80dfc-458">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-458">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="80dfc-459">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="80dfc-459">Parameters - font</span></span>

<span data-ttu-id="80dfc-460">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-460">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="80dfc-461">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="80dfc-461">Return Value - font</span></span>

<span data-ttu-id="80dfc-462">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="80dfc-462">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontinfoprinter"></a><span data-ttu-id="80dfc-463">メソッド fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="80dfc-463">Method fontInfoPrinter</span></span>

```xpp
public str fontInfoPrinter()
```

### <a name="return-value---fontinfoprinter"></a><span data-ttu-id="80dfc-464">戻り値 - fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="80dfc-464">Return Value - fontInfoPrinter</span></span>

## <a name="method-fontinfoprinterascent"></a><span data-ttu-id="80dfc-465">メソッド fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="80dfc-465">Method fontInfoPrinterAscent</span></span>

```xpp
public int fontInfoPrinterAscent()
```

### <a name="return-value---fontinfoprinterascent"></a><span data-ttu-id="80dfc-466">戻り値 - fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="80dfc-466">Return Value - fontInfoPrinterAscent</span></span>

## <a name="method-fontinfoprinterdescent"></a><span data-ttu-id="80dfc-467">メソッド fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="80dfc-467">Method fontInfoPrinterDescent</span></span>

```xpp
public int fontInfoPrinterDescent()
```

### <a name="return-value---fontinfoprinterdescent"></a><span data-ttu-id="80dfc-468">戻り値 - fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="80dfc-468">Return Value - fontInfoPrinterDescent</span></span>

## <a name="method-fontinfoprinterextlead"></a><span data-ttu-id="80dfc-469">メソッド fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="80dfc-469">Method fontInfoPrinterExtLead</span></span>

```xpp
public int fontInfoPrinterExtLead()
```

### <a name="return-value---fontinfoprinterextlead"></a><span data-ttu-id="80dfc-470">戻り値 - fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="80dfc-470">Return Value - fontInfoPrinterExtLead</span></span>

## <a name="method-fontinfoprinterheight"></a><span data-ttu-id="80dfc-471">メソッド fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="80dfc-471">Method fontInfoPrinterHeight</span></span>

```xpp
public int fontInfoPrinterHeight()
```

### <a name="return-value---fontinfoprinterheight"></a><span data-ttu-id="80dfc-472">戻り値 - fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="80dfc-472">Return Value - fontInfoPrinterHeight</span></span>

## <a name="method-fontinfoprinterintlead"></a><span data-ttu-id="80dfc-473">メソッド fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="80dfc-473">Method fontInfoPrinterIntLead</span></span>

```xpp
public int fontInfoPrinterIntLead()
```

### <a name="return-value---fontinfoprinterintlead"></a><span data-ttu-id="80dfc-474">戻り値 - fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="80dfc-474">Return Value - fontInfoPrinterIntLead</span></span>

## <a name="method-fontinfoscreen"></a><span data-ttu-id="80dfc-475">メソッド fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="80dfc-475">Method fontInfoScreen</span></span>

```xpp
public str fontInfoScreen()
```

### <a name="return-value---fontinfoscreen"></a><span data-ttu-id="80dfc-476">戻り値 - fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="80dfc-476">Return Value - fontInfoScreen</span></span>

## <a name="method-fontinfoscreenascent"></a><span data-ttu-id="80dfc-477">メソッド fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="80dfc-477">Method fontInfoScreenAscent</span></span>

```xpp
public int fontInfoScreenAscent()
```

### <a name="return-value---fontinfoscreenascent"></a><span data-ttu-id="80dfc-478">戻り値 - fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="80dfc-478">Return Value - fontInfoScreenAscent</span></span>

## <a name="method-fontinfoscreendescent"></a><span data-ttu-id="80dfc-479">メソッド fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="80dfc-479">Method fontInfoScreenDescent</span></span>

```xpp
public int fontInfoScreenDescent()
```

### <a name="return-value---fontinfoscreendescent"></a><span data-ttu-id="80dfc-480">戻り値 - fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="80dfc-480">Return Value - fontInfoScreenDescent</span></span>

## <a name="method-fontinfoscreenextlead"></a><span data-ttu-id="80dfc-481">メソッド fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="80dfc-481">Method fontInfoScreenExtLead</span></span>

```xpp
public int fontInfoScreenExtLead()
```

### <a name="return-value---fontinfoscreenextlead"></a><span data-ttu-id="80dfc-482">戻り値 - fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="80dfc-482">Return Value - fontInfoScreenExtLead</span></span>

## <a name="method-fontinfoscreenheight"></a><span data-ttu-id="80dfc-483">メソッド fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="80dfc-483">Method fontInfoScreenHeight</span></span>

```xpp
public int fontInfoScreenHeight()
```

### <a name="return-value---fontinfoscreenheight"></a><span data-ttu-id="80dfc-484">戻り値 - fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="80dfc-484">Return Value - fontInfoScreenHeight</span></span>

## <a name="method-fontinfoscreenintlead"></a><span data-ttu-id="80dfc-485">メソッド fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="80dfc-485">Method fontInfoScreenIntLead</span></span>

```xpp
public int fontInfoScreenIntLead()
```

### <a name="return-value---fontinfoscreenintlead"></a><span data-ttu-id="80dfc-486">戻り値 - fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="80dfc-486">Return Value - fontInfoScreenIntLead</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="80dfc-487">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="80dfc-487">Method fontSize</span></span>

<span data-ttu-id="80dfc-488">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-488">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="80dfc-489">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="80dfc-489">Parameters - fontSize</span></span>

<span data-ttu-id="80dfc-490">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-490">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="80dfc-491">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="80dfc-491">Return Value - fontSize</span></span>

<span data-ttu-id="80dfc-492">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="80dfc-492">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="80dfc-493">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="80dfc-493">Method foregroundColor</span></span>

<span data-ttu-id="80dfc-494">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-494">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="80dfc-495">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="80dfc-495">Parameters - foregroundColor</span></span>

<span data-ttu-id="80dfc-496">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-496">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="80dfc-497">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="80dfc-497">Return Value - foregroundColor</span></span>

<span data-ttu-id="80dfc-498">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="80dfc-498">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="80dfc-499">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="80dfc-499">Remarks - foregroundColor</span></span>

<span data-ttu-id="80dfc-500">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="80dfc-500">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="80dfc-501">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="80dfc-501">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="80dfc-502">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="80dfc-502">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="80dfc-503">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="80dfc-503">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="80dfc-504">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="80dfc-504">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="80dfc-505">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="80dfc-505">The maximum value for a single byte is 255.</span></span>

## <a name="method-height100mm"></a><span data-ttu-id="80dfc-506">メソッド height100mm</span><span class="sxs-lookup"><span data-stu-id="80dfc-506">Method height100mm</span></span>

```xpp
public int height100mm([int heightExclBorder])
```

### <a name="parameters---height100mm"></a><span data-ttu-id="80dfc-507">パラメーター - height100mm</span><span class="sxs-lookup"><span data-stu-id="80dfc-507">Parameters - height100mm</span></span>

<span data-ttu-id="80dfc-508">heightExclBorder</span><span class="sxs-lookup"><span data-stu-id="80dfc-508">heightExclBorder</span></span>  

### <a name="return-value---height100mm"></a><span data-ttu-id="80dfc-509">戻り値 - height100mm</span><span class="sxs-lookup"><span data-stu-id="80dfc-509">Return Value - height100mm</span></span>

## <a name="method-height100mminclborder"></a><span data-ttu-id="80dfc-510">メソッド height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="80dfc-510">Method height100mmInclBorder</span></span>

```xpp
public int height100mmInclBorder([int heightInclBorder])
```

### <a name="parameters---height100mminclborder"></a><span data-ttu-id="80dfc-511">パラメーター - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="80dfc-511">Parameters - height100mmInclBorder</span></span>

<span data-ttu-id="80dfc-512">heightInclBorder</span><span class="sxs-lookup"><span data-stu-id="80dfc-512">heightInclBorder</span></span>  

### <a name="return-value---height100mminclborder"></a><span data-ttu-id="80dfc-513">戻り値 - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="80dfc-513">Return Value - height100mmInclBorder</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="80dfc-514">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-514">Method heightMode</span></span>

<span data-ttu-id="80dfc-515">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-515">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="80dfc-516">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-516">Parameters - heightMode</span></span>

<span data-ttu-id="80dfc-517">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-517">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="80dfc-518">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-518">Return Value - heightMode</span></span>

<span data-ttu-id="80dfc-519">計算モード。</span><span class="sxs-lookup"><span data-stu-id="80dfc-519">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="80dfc-520">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-520">Remarks - heightMode</span></span>

<span data-ttu-id="80dfc-521">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="80dfc-521">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="80dfc-522">モード。</span><span class="sxs-lookup"><span data-stu-id="80dfc-522">Mode.</span></span>          | <span data-ttu-id="80dfc-523">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="80dfc-523">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="80dfc-524">正確。</span><span class="sxs-lookup"><span data-stu-id="80dfc-524">Exact.</span></span>         | <span data-ttu-id="80dfc-525">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="80dfc-525">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="80dfc-526">自動。</span><span class="sxs-lookup"><span data-stu-id="80dfc-526">Auto.</span></span>          | <span data-ttu-id="80dfc-527">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="80dfc-527">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="80dfc-528">列の高さ</span><span class="sxs-lookup"><span data-stu-id="80dfc-528">Column height.</span></span> | <span data-ttu-id="80dfc-529">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="80dfc-529">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="80dfc-530">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="80dfc-530">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightofwordwrappedstring100mm"></a><span data-ttu-id="80dfc-531">メソッド heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="80dfc-531">Method heightOfWordWrappedString100mm</span></span>

```xpp
public int heightOfWordWrappedString100mm(str string)
```

### <a name="parameters---heightofwordwrappedstring100mm"></a><span data-ttu-id="80dfc-532">パラメーター - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="80dfc-532">Parameters - heightOfWordWrappedString100mm</span></span>

<span data-ttu-id="80dfc-533">文字列</span><span class="sxs-lookup"><span data-stu-id="80dfc-533">string</span></span>  

### <a name="return-value---heightofwordwrappedstring100mm"></a><span data-ttu-id="80dfc-534">戻り値 - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="80dfc-534">Return Value - heightOfWordWrappedString100mm</span></span>

## <a name="method-heightstr"></a><span data-ttu-id="80dfc-535">メソッド heightStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-535">Method heightStr</span></span>

```xpp
public str heightStr([str value])
```

### <a name="parameters---heightstr"></a><span data-ttu-id="80dfc-536">パラメーター - heightStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-536">Parameters - heightStr</span></span>

<span data-ttu-id="80dfc-537">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-537">value</span></span>  

### <a name="return-value---heightstr"></a><span data-ttu-id="80dfc-538">戻り値 - heightStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-538">Return Value - heightStr</span></span>

## <a name="method-heightunit"></a><span data-ttu-id="80dfc-539">メソッド heightUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-539">Method heightUnit</span></span>

```xpp
public Units heightUnit([Units value])
```

### <a name="parameters---heightunit"></a><span data-ttu-id="80dfc-540">パラメーター - heightUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-540">Parameters - heightUnit</span></span>

<span data-ttu-id="80dfc-541">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-541">value</span></span>  

### <a name="return-value---heightunit"></a><span data-ttu-id="80dfc-542">戻り値 - heightUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-542">Return Value - heightUnit</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="80dfc-543">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-543">Method heightValue</span></span>

<span data-ttu-id="80dfc-544">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-544">Gets or sets the height of the control.</span></span>

```xpp
public Real heightValue([Real value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="80dfc-545">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-545">Parameters - heightValue</span></span>

<span data-ttu-id="80dfc-546">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-546">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="80dfc-547">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-547">Return Value - heightValue</span></span>

<span data-ttu-id="80dfc-548">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="80dfc-548">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="80dfc-549">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-549">Remarks - heightValue</span></span>

<span data-ttu-id="80dfc-550">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="80dfc-550">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-italic"></a><span data-ttu-id="80dfc-551">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="80dfc-551">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="80dfc-552">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="80dfc-552">Parameters - italic</span></span>

<span data-ttu-id="80dfc-553">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-553">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="80dfc-554">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="80dfc-554">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="80dfc-555">メソッド label</span><span class="sxs-lookup"><span data-stu-id="80dfc-555">Method label</span></span>

<span data-ttu-id="80dfc-556">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-556">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="80dfc-557">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="80dfc-557">Parameters - label</span></span>

<span data-ttu-id="80dfc-558">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-558">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="80dfc-559">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="80dfc-559">Return Value - label</span></span>

<span data-ttu-id="80dfc-560">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="80dfc-560">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="80dfc-561">備考 - label</span><span class="sxs-lookup"><span data-stu-id="80dfc-561">Remarks - label</span></span>

<span data-ttu-id="80dfc-562">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-562">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="80dfc-563">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="80dfc-563">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="80dfc-564">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="80dfc-564">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="80dfc-565">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="80dfc-565">Parameters - labelBold</span></span>

<span data-ttu-id="80dfc-566">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-566">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="80dfc-567">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="80dfc-567">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="80dfc-568">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="80dfc-568">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="80dfc-569">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="80dfc-569">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="80dfc-570">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-570">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="80dfc-571">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="80dfc-571">Return Value - labelCharacterSet</span></span>

## <a name="method-labelcssclass"></a><span data-ttu-id="80dfc-572">メソッド labelCssClass</span><span class="sxs-lookup"><span data-stu-id="80dfc-572">Method labelCssClass</span></span>

```xpp
public str labelCssClass([str value])
```

### <a name="parameters---labelcssclass"></a><span data-ttu-id="80dfc-573">パラメーター - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="80dfc-573">Parameters - labelCssClass</span></span>

<span data-ttu-id="80dfc-574">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-574">value</span></span>  

### <a name="return-value---labelcssclass"></a><span data-ttu-id="80dfc-575">戻り値 - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="80dfc-575">Return Value - labelCssClass</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="80dfc-576">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="80dfc-576">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="80dfc-577">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="80dfc-577">Parameters - labelFont</span></span>

<span data-ttu-id="80dfc-578">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-578">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="80dfc-579">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="80dfc-579">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="80dfc-580">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="80dfc-580">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="80dfc-581">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="80dfc-581">Parameters - labelFontSize</span></span>

<span data-ttu-id="80dfc-582">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-582">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="80dfc-583">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="80dfc-583">Return Value - labelFontSize</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="80dfc-584">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="80dfc-584">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="80dfc-585">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="80dfc-585">Parameters - labelItalic</span></span>

<span data-ttu-id="80dfc-586">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-586">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="80dfc-587">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="80dfc-587">Return Value - labelItalic</span></span>

## <a name="method-labellinebelow"></a><span data-ttu-id="80dfc-588">メソッド labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="80dfc-588">Method labelLineBelow</span></span>

```xpp
public LineType labelLineBelow([LineType value])
```

### <a name="parameters---labellinebelow"></a><span data-ttu-id="80dfc-589">パラメーター - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="80dfc-589">Parameters - labelLineBelow</span></span>

<span data-ttu-id="80dfc-590">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-590">value</span></span>  

### <a name="return-value---labellinebelow"></a><span data-ttu-id="80dfc-591">戻り値 - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="80dfc-591">Return Value - labelLineBelow</span></span>

## <a name="method-labellinethickness"></a><span data-ttu-id="80dfc-592">メソッド labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="80dfc-592">Method labelLineThickness</span></span>

```xpp
public LineThickness labelLineThickness([LineThickness value])
```

### <a name="parameters---labellinethickness"></a><span data-ttu-id="80dfc-593">パラメーター - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="80dfc-593">Parameters - labelLineThickness</span></span>

<span data-ttu-id="80dfc-594">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-594">value</span></span>  

### <a name="return-value---labellinethickness"></a><span data-ttu-id="80dfc-595">戻り値 - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="80dfc-595">Return Value - labelLineThickness</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="80dfc-596">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="80dfc-596">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="80dfc-597">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="80dfc-597">Parameters - labelPosition</span></span>

<span data-ttu-id="80dfc-598">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-598">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="80dfc-599">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="80dfc-599">Return Value - labelPosition</span></span>

## <a name="method-labeltableader"></a><span data-ttu-id="80dfc-600">メソッド labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="80dfc-600">Method labelTabLeader</span></span>

```xpp
public int labelTabLeader([int value])
```

### <a name="parameters---labeltableader"></a><span data-ttu-id="80dfc-601">パラメーター - labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="80dfc-601">Parameters - labelTabLeader</span></span>

<span data-ttu-id="80dfc-602">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-602">value</span></span>  

### <a name="return-value---labeltableader"></a><span data-ttu-id="80dfc-603">戻り値 - labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="80dfc-603">Return Value - labelTabLeader</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="80dfc-604">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="80dfc-604">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="80dfc-605">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="80dfc-605">Parameters - labelUnderline</span></span>

<span data-ttu-id="80dfc-606">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-606">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="80dfc-607">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="80dfc-607">Return Value - labelUnderline</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="80dfc-608">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-608">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="80dfc-609">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-609">Parameters - labelWidthMode</span></span>

<span data-ttu-id="80dfc-610">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-610">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="80dfc-611">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-611">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthstr"></a><span data-ttu-id="80dfc-612">メソッド labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-612">Method labelWidthStr</span></span>

```xpp
public str labelWidthStr([str value])
```

### <a name="parameters---labelwidthstr"></a><span data-ttu-id="80dfc-613">パラメーター - labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-613">Parameters - labelWidthStr</span></span>

<span data-ttu-id="80dfc-614">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-614">value</span></span>  

### <a name="return-value---labelwidthstr"></a><span data-ttu-id="80dfc-615">戻り値 - labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-615">Return Value - labelWidthStr</span></span>

## <a name="method-labelwidthunit"></a><span data-ttu-id="80dfc-616">メソッド labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-616">Method labelWidthUnit</span></span>

```xpp
public Units labelWidthUnit([Units value])
```

### <a name="parameters---labelwidthunit"></a><span data-ttu-id="80dfc-617">パラメーター - labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-617">Parameters - labelWidthUnit</span></span>

<span data-ttu-id="80dfc-618">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-618">value</span></span>  

### <a name="return-value---labelwidthunit"></a><span data-ttu-id="80dfc-619">戻り値 - labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-619">Return Value - labelWidthUnit</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="80dfc-620">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-620">Method labelWidthValue</span></span>

```xpp
public Real labelWidthValue([Real value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="80dfc-621">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-621">Parameters - labelWidthValue</span></span>

<span data-ttu-id="80dfc-622">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-622">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="80dfc-623">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-623">Return Value - labelWidthValue</span></span>

## <a name="method-left100mm"></a><span data-ttu-id="80dfc-624">メソッド left100mm</span><span class="sxs-lookup"><span data-stu-id="80dfc-624">Method left100mm</span></span>

```xpp
public int left100mm([int leftExclBorder])
```

### <a name="parameters---left100mm"></a><span data-ttu-id="80dfc-625">パラメーター - left100mm</span><span class="sxs-lookup"><span data-stu-id="80dfc-625">Parameters - left100mm</span></span>

<span data-ttu-id="80dfc-626">leftExclBorder</span><span class="sxs-lookup"><span data-stu-id="80dfc-626">leftExclBorder</span></span>  

### <a name="return-value---left100mm"></a><span data-ttu-id="80dfc-627">戻り値 - left100mm</span><span class="sxs-lookup"><span data-stu-id="80dfc-627">Return Value - left100mm</span></span>

## <a name="method-left100mminclborder"></a><span data-ttu-id="80dfc-628">メソッド left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="80dfc-628">Method left100mmInclBorder</span></span>

```xpp
public int left100mmInclBorder([int leftInclBorder])
```

### <a name="parameters---left100mminclborder"></a><span data-ttu-id="80dfc-629">パラメーター - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="80dfc-629">Parameters - left100mmInclBorder</span></span>

<span data-ttu-id="80dfc-630">leftInclBorder</span><span class="sxs-lookup"><span data-stu-id="80dfc-630">leftInclBorder</span></span>  

### <a name="return-value---left100mminclborder"></a><span data-ttu-id="80dfc-631">戻り値 - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="80dfc-631">Return Value - left100mmInclBorder</span></span>

## <a name="method-leftmarginanframe"></a><span data-ttu-id="80dfc-632">メソッド leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="80dfc-632">Method leftMarginAnFrame</span></span>

```xpp
public int leftMarginAnFrame()
```

### <a name="return-value---leftmarginanframe"></a><span data-ttu-id="80dfc-633">戻り値 - leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="80dfc-633">Return Value - leftMarginAnFrame</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="80dfc-634">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-634">Method leftMarginMode</span></span>

```xpp
public int leftMarginMode([int value])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="80dfc-635">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-635">Parameters - leftMarginMode</span></span>

<span data-ttu-id="80dfc-636">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-636">value</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="80dfc-637">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-637">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginstr"></a><span data-ttu-id="80dfc-638">メソッド leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-638">Method leftMarginStr</span></span>

```xpp
public str leftMarginStr([str value])
```

### <a name="parameters---leftmarginstr"></a><span data-ttu-id="80dfc-639">パラメーター - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-639">Parameters - leftMarginStr</span></span>

<span data-ttu-id="80dfc-640">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-640">value</span></span>  

### <a name="return-value---leftmarginstr"></a><span data-ttu-id="80dfc-641">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-641">Return Value - leftMarginStr</span></span>

## <a name="method-leftmarginunit"></a><span data-ttu-id="80dfc-642">メソッド leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-642">Method leftMarginUnit</span></span>

```xpp
public Units leftMarginUnit([Units value])
```

### <a name="parameters---leftmarginunit"></a><span data-ttu-id="80dfc-643">パラメーター - leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-643">Parameters - leftMarginUnit</span></span>

<span data-ttu-id="80dfc-644">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-644">value</span></span>  

### <a name="return-value---leftmarginunit"></a><span data-ttu-id="80dfc-645">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-645">Return Value - leftMarginUnit</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="80dfc-646">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-646">Method leftMarginValue</span></span>

```xpp
public Real leftMarginValue([Real value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="80dfc-647">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-647">Parameters - leftMarginValue</span></span>

<span data-ttu-id="80dfc-648">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-648">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="80dfc-649">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-649">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="80dfc-650">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-650">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="80dfc-651">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-651">Parameters - leftMode</span></span>

<span data-ttu-id="80dfc-652">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-652">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="80dfc-653">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-653">Return Value - leftMode</span></span>

## <a name="method-leftstr"></a><span data-ttu-id="80dfc-654">メソッド leftStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-654">Method leftStr</span></span>

```xpp
public str leftStr([str value])
```

### <a name="parameters---leftstr"></a><span data-ttu-id="80dfc-655">パラメーター - leftStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-655">Parameters - leftStr</span></span>

<span data-ttu-id="80dfc-656">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-656">value</span></span>  

### <a name="return-value---leftstr"></a><span data-ttu-id="80dfc-657">戻り値 - leftStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-657">Return Value - leftStr</span></span>

## <a name="method-leftunit"></a><span data-ttu-id="80dfc-658">メソッド leftUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-658">Method leftUnit</span></span>

```xpp
public Units leftUnit([Units value])
```

### <a name="parameters---leftunit"></a><span data-ttu-id="80dfc-659">パラメーター - leftUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-659">Parameters - leftUnit</span></span>

<span data-ttu-id="80dfc-660">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-660">value</span></span>  

### <a name="return-value---leftunit"></a><span data-ttu-id="80dfc-661">戻り値 - leftUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-661">Return Value - leftUnit</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="80dfc-662">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-662">Method leftValue</span></span>

```xpp
public Real leftValue([Real value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="80dfc-663">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-663">Parameters - leftValue</span></span>

<span data-ttu-id="80dfc-664">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-664">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="80dfc-665">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-665">Return Value - leftValue</span></span>

## <a name="method-lineabove"></a><span data-ttu-id="80dfc-666">メソッド lineAbove</span><span class="sxs-lookup"><span data-stu-id="80dfc-666">Method lineAbove</span></span>

```xpp
public LineType lineAbove([LineType value])
```

### <a name="parameters---lineabove"></a><span data-ttu-id="80dfc-667">パラメーター - lineAbove</span><span class="sxs-lookup"><span data-stu-id="80dfc-667">Parameters - lineAbove</span></span>

<span data-ttu-id="80dfc-668">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-668">value</span></span>  

### <a name="return-value---lineabove"></a><span data-ttu-id="80dfc-669">戻り値 - lineAbove</span><span class="sxs-lookup"><span data-stu-id="80dfc-669">Return Value - lineAbove</span></span>

## <a name="method-linebelow"></a><span data-ttu-id="80dfc-670">メソッド lineBelow</span><span class="sxs-lookup"><span data-stu-id="80dfc-670">Method lineBelow</span></span>

```xpp
public LineType lineBelow([LineType value])
```

### <a name="parameters---linebelow"></a><span data-ttu-id="80dfc-671">パラメーター - lineBelow</span><span class="sxs-lookup"><span data-stu-id="80dfc-671">Parameters - lineBelow</span></span>

<span data-ttu-id="80dfc-672">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-672">value</span></span>  

### <a name="return-value---linebelow"></a><span data-ttu-id="80dfc-673">戻り値 - lineBelow</span><span class="sxs-lookup"><span data-stu-id="80dfc-673">Return Value - lineBelow</span></span>

## <a name="method-lineleft"></a><span data-ttu-id="80dfc-674">メソッド lineLeft</span><span class="sxs-lookup"><span data-stu-id="80dfc-674">Method lineLeft</span></span>

<span data-ttu-id="80dfc-675">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-675">Gets or sets the type of line that is used as the left border of a section.</span></span>

```xpp
public LineType lineLeft([LineType value])
```

### <a name="parameters---lineleft"></a><span data-ttu-id="80dfc-676">パラメーター - lineLeft</span><span class="sxs-lookup"><span data-stu-id="80dfc-676">Parameters - lineLeft</span></span>

<span data-ttu-id="80dfc-677">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-677">value</span></span>  

### <a name="return-value---lineleft"></a><span data-ttu-id="80dfc-678">戻り値 - lineLeft</span><span class="sxs-lookup"><span data-stu-id="80dfc-678">Return Value - lineLeft</span></span>

<span data-ttu-id="80dfc-679">左境界線として使用される線のタイプ。</span><span class="sxs-lookup"><span data-stu-id="80dfc-679">The type of line that is used as the left border.</span></span>

## <a name="method-lineright"></a><span data-ttu-id="80dfc-680">メソッド lineRight</span><span class="sxs-lookup"><span data-stu-id="80dfc-680">Method lineRight</span></span>

```xpp
public LineType lineRight([LineType value])
```

### <a name="parameters---lineright"></a><span data-ttu-id="80dfc-681">パラメーター - lineRight</span><span class="sxs-lookup"><span data-stu-id="80dfc-681">Parameters - lineRight</span></span>

<span data-ttu-id="80dfc-682">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-682">value</span></span>  

### <a name="return-value---lineright"></a><span data-ttu-id="80dfc-683">戻り値 - lineRight</span><span class="sxs-lookup"><span data-stu-id="80dfc-683">Return Value - lineRight</span></span>

## <a name="method-menuitemlabel"></a><span data-ttu-id="80dfc-684">メソッド menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="80dfc-684">Method menuItemLabel</span></span>

```xpp
public str menuItemLabel([str value])
```

### <a name="parameters---menuitemlabel"></a><span data-ttu-id="80dfc-685">パラメーター - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="80dfc-685">Parameters - menuItemLabel</span></span>

<span data-ttu-id="80dfc-686">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-686">value</span></span>  

### <a name="return-value---menuitemlabel"></a><span data-ttu-id="80dfc-687">戻り値 - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="80dfc-687">Return Value - menuItemLabel</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="80dfc-688">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="80dfc-688">Method menuItemName</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="80dfc-689">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="80dfc-689">Parameters - menuItemName</span></span>

<span data-ttu-id="80dfc-690">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-690">value</span></span>  

### <a name="return-value---menuitemname"></a><span data-ttu-id="80dfc-691">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="80dfc-691">Return Value - menuItemName</span></span>

## <a name="method-menuitemtype"></a><span data-ttu-id="80dfc-692">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="80dfc-692">Method menuItemType</span></span>

```xpp
public MenuItemType menuItemType([MenuItemType value])
```

### <a name="parameters---menuitemtype"></a><span data-ttu-id="80dfc-693">パラメーター - menuItemType</span><span class="sxs-lookup"><span data-stu-id="80dfc-693">Parameters - menuItemType</span></span>

<span data-ttu-id="80dfc-694">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-694">value</span></span>  

### <a name="return-value---menuitemtype"></a><span data-ttu-id="80dfc-695">戻り値 - menuItemType</span><span class="sxs-lookup"><span data-stu-id="80dfc-695">Return Value - menuItemType</span></span>

## <a name="method-modelfieldname"></a><span data-ttu-id="80dfc-696">メソッド modelFieldName</span><span class="sxs-lookup"><span data-stu-id="80dfc-696">Method modelFieldName</span></span>

```xpp
public str modelFieldName([str value])
```

### <a name="parameters---modelfieldname"></a><span data-ttu-id="80dfc-697">パラメーター - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="80dfc-697">Parameters - modelFieldName</span></span>

<span data-ttu-id="80dfc-698">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-698">value</span></span>  

### <a name="return-value---modelfieldname"></a><span data-ttu-id="80dfc-699">戻り値 - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="80dfc-699">Return Value - modelFieldName</span></span>

## <a name="method-name"></a><span data-ttu-id="80dfc-700">メソッド名</span><span class="sxs-lookup"><span data-stu-id="80dfc-700">Method name</span></span>

<span data-ttu-id="80dfc-701">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-701">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="80dfc-702">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="80dfc-702">Parameters - name</span></span>

<span data-ttu-id="80dfc-703">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-703">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="80dfc-704">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="80dfc-704">Return Value - name</span></span>

<span data-ttu-id="80dfc-705">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="80dfc-705">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="80dfc-706">備考 - name</span><span class="sxs-lookup"><span data-stu-id="80dfc-706">Remarks - name</span></span>

<span data-ttu-id="80dfc-707">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="80dfc-707">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="80dfc-708">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="80dfc-708">Begins with a letter.</span></span>
-   <span data-ttu-id="80dfc-709">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="80dfc-709">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="80dfc-710">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="80dfc-710">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="80dfc-711">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="80dfc-711">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="80dfc-712">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="80dfc-712">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-numberoflines"></a><span data-ttu-id="80dfc-713">メソッド numberOfLines</span><span class="sxs-lookup"><span data-stu-id="80dfc-713">Method numberOfLines</span></span>

```xpp
public int numberOfLines(int height100mm)
```

### <a name="parameters---numberoflines"></a><span data-ttu-id="80dfc-714">パラメーター - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="80dfc-714">Parameters - numberOfLines</span></span>

<span data-ttu-id="80dfc-715">height100mm</span><span class="sxs-lookup"><span data-stu-id="80dfc-715">height100mm</span></span>  

### <a name="return-value---numberoflines"></a><span data-ttu-id="80dfc-716">戻り値 - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="80dfc-716">Return Value - numberOfLines</span></span>

## <a name="method-position"></a><span data-ttu-id="80dfc-717">メソッドの位置</span><span class="sxs-lookup"><span data-stu-id="80dfc-717">Method position</span></span>

```xpp
public int position([int value])
```

### <a name="parameters---position"></a><span data-ttu-id="80dfc-718">パラメーター - position</span><span class="sxs-lookup"><span data-stu-id="80dfc-718">Parameters - position</span></span>

<span data-ttu-id="80dfc-719">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-719">value</span></span>  

### <a name="return-value---position"></a><span data-ttu-id="80dfc-720">戻り値 - position</span><span class="sxs-lookup"><span data-stu-id="80dfc-720">Return Value - position</span></span>

## <a name="method-previewinfo"></a><span data-ttu-id="80dfc-721">メソッド previewInfo</span><span class="sxs-lookup"><span data-stu-id="80dfc-721">Method previewInfo</span></span>

```xpp
public str previewInfo(str string)
```

### <a name="parameters---previewinfo"></a><span data-ttu-id="80dfc-722">パラメーター - previewInfo</span><span class="sxs-lookup"><span data-stu-id="80dfc-722">Parameters - previewInfo</span></span>

<span data-ttu-id="80dfc-723">文字列</span><span class="sxs-lookup"><span data-stu-id="80dfc-723">string</span></span>  

### <a name="return-value---previewinfo"></a><span data-ttu-id="80dfc-724">戻り値 - previewInfo</span><span class="sxs-lookup"><span data-stu-id="80dfc-724">Return Value - previewInfo</span></span>

## <a name="method-previewxcompensation100mm"></a><span data-ttu-id="80dfc-725">メソッド previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="80dfc-725">Method previewXCompensation100mm</span></span>

```xpp
public int previewXCompensation100mm(str string)
```

### <a name="parameters---previewxcompensation100mm"></a><span data-ttu-id="80dfc-726">パラメーター - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="80dfc-726">Parameters - previewXCompensation100mm</span></span>

<span data-ttu-id="80dfc-727">文字列</span><span class="sxs-lookup"><span data-stu-id="80dfc-727">string</span></span>  

### <a name="return-value---previewxcompensation100mm"></a><span data-ttu-id="80dfc-728">戻り値 - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="80dfc-728">Return Value - previewXCompensation100mm</span></span>

## <a name="method-right100mm"></a><span data-ttu-id="80dfc-729">メソッド right100mm</span><span class="sxs-lookup"><span data-stu-id="80dfc-729">Method right100mm</span></span>

```xpp
public int right100mm()
```

### <a name="return-value---right100mm"></a><span data-ttu-id="80dfc-730">戻り値 - right100mm</span><span class="sxs-lookup"><span data-stu-id="80dfc-730">Return Value - right100mm</span></span>

## <a name="method-right100mminclborder"></a><span data-ttu-id="80dfc-731">メソッド right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="80dfc-731">Method right100mmInclBorder</span></span>

```xpp
public int right100mmInclBorder()
```

### <a name="return-value---right100mminclborder"></a><span data-ttu-id="80dfc-732">戻り値 - right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="80dfc-732">Return Value - right100mmInclBorder</span></span>

## <a name="method-rightmarginandframe"></a><span data-ttu-id="80dfc-733">メソッド rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="80dfc-733">Method rightMarginAndFrame</span></span>

```xpp
public int rightMarginAndFrame()
```

### <a name="return-value---rightmarginandframe"></a><span data-ttu-id="80dfc-734">戻り値 - rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="80dfc-734">Return Value - rightMarginAndFrame</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="80dfc-735">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-735">Method rightMarginMode</span></span>

```xpp
public int rightMarginMode([int value])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="80dfc-736">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-736">Parameters - rightMarginMode</span></span>

<span data-ttu-id="80dfc-737">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-737">value</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="80dfc-738">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-738">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginstr"></a><span data-ttu-id="80dfc-739">メソッド rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-739">Method rightMarginStr</span></span>

```xpp
public str rightMarginStr([str value])
```

### <a name="parameters---rightmarginstr"></a><span data-ttu-id="80dfc-740">パラメーター - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-740">Parameters - rightMarginStr</span></span>

<span data-ttu-id="80dfc-741">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-741">value</span></span>  

### <a name="return-value---rightmarginstr"></a><span data-ttu-id="80dfc-742">戻り値 - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-742">Return Value - rightMarginStr</span></span>

## <a name="method-rightmarginunit"></a><span data-ttu-id="80dfc-743">メソッド rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-743">Method rightMarginUnit</span></span>

```xpp
public Units rightMarginUnit([Units value])
```

### <a name="parameters---rightmarginunit"></a><span data-ttu-id="80dfc-744">パラメーター - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-744">Parameters - rightMarginUnit</span></span>

<span data-ttu-id="80dfc-745">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-745">value</span></span>  

### <a name="return-value---rightmarginunit"></a><span data-ttu-id="80dfc-746">戻り値 - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-746">Return Value - rightMarginUnit</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="80dfc-747">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-747">Method rightMarginValue</span></span>

```xpp
public Real rightMarginValue([Real value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="80dfc-748">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-748">Parameters - rightMarginValue</span></span>

<span data-ttu-id="80dfc-749">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-749">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="80dfc-750">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-750">Return Value - rightMarginValue</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="80dfc-751">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="80dfc-751">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="80dfc-752">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="80dfc-752">Parameters - securityKey</span></span>

<span data-ttu-id="80dfc-753">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-753">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="80dfc-754">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="80dfc-754">Return Value - securityKey</span></span>

## <a name="method-setheightgettext"></a><span data-ttu-id="80dfc-755">メソッド setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="80dfc-755">Method setHeightGetText</span></span>

```xpp
public str setHeightGetText(int lines, str string)
```

### <a name="parameters---setheightgettext"></a><span data-ttu-id="80dfc-756">パラメーター - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="80dfc-756">Parameters - setHeightGetText</span></span>

<span data-ttu-id="80dfc-757">明細行</span><span class="sxs-lookup"><span data-stu-id="80dfc-757">lines</span></span>  

<!-- -->

<span data-ttu-id="80dfc-758">文字列</span><span class="sxs-lookup"><span data-stu-id="80dfc-758">string</span></span>  

### <a name="return-value---setheightgettext"></a><span data-ttu-id="80dfc-759">戻り値 - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="80dfc-759">Return Value - setHeightGetText</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="80dfc-760">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="80dfc-760">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="80dfc-761">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="80dfc-761">Parameters - showLabel</span></span>

<span data-ttu-id="80dfc-762">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-762">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="80dfc-763">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="80dfc-763">Return Value - showLabel</span></span>

## <a name="method-table"></a><span data-ttu-id="80dfc-764">メソッド table</span><span class="sxs-lookup"><span data-stu-id="80dfc-764">Method table</span></span>

<span data-ttu-id="80dfc-765">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-765">Gets or sets the table ID associated with the object.</span></span>

```xpp
public TableId table([TableId value])
```

### <a name="parameters---table"></a><span data-ttu-id="80dfc-766">パラメーター - table</span><span class="sxs-lookup"><span data-stu-id="80dfc-766">Parameters - table</span></span>

<span data-ttu-id="80dfc-767">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-767">value</span></span>  

### <a name="return-value---table"></a><span data-ttu-id="80dfc-768">戻り値 - toBlob</span><span class="sxs-lookup"><span data-stu-id="80dfc-768">Return Value - table</span></span>

<span data-ttu-id="80dfc-769">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="80dfc-769">The current value of the table ID associated with the object.</span></span>

## <a name="method-thickness"></a><span data-ttu-id="80dfc-770">メソッド thickness</span><span class="sxs-lookup"><span data-stu-id="80dfc-770">Method thickness</span></span>

```xpp
public LineThickness thickness([LineThickness value])
```

### <a name="parameters---thickness"></a><span data-ttu-id="80dfc-771">パラメーター - thickness</span><span class="sxs-lookup"><span data-stu-id="80dfc-771">Parameters - thickness</span></span>

<span data-ttu-id="80dfc-772">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-772">value</span></span>  

### <a name="return-value---thickness"></a><span data-ttu-id="80dfc-773">戻り値 - thickness</span><span class="sxs-lookup"><span data-stu-id="80dfc-773">Return Value - thickness</span></span>

## <a name="method-top100mm"></a><span data-ttu-id="80dfc-774">メソッド top100mm</span><span class="sxs-lookup"><span data-stu-id="80dfc-774">Method top100mm</span></span>

```xpp
public int top100mm([int topExclBorder])
```

### <a name="parameters---top100mm"></a><span data-ttu-id="80dfc-775">パラメーター - top100mm</span><span class="sxs-lookup"><span data-stu-id="80dfc-775">Parameters - top100mm</span></span>

<span data-ttu-id="80dfc-776">topExclBorder</span><span class="sxs-lookup"><span data-stu-id="80dfc-776">topExclBorder</span></span>  

### <a name="return-value---top100mm"></a><span data-ttu-id="80dfc-777">戻り値 - top100mm</span><span class="sxs-lookup"><span data-stu-id="80dfc-777">Return Value - top100mm</span></span>

## <a name="method-top100mminclborder"></a><span data-ttu-id="80dfc-778">メソッド top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="80dfc-778">Method top100mmInclBorder</span></span>

```xpp
public int top100mmInclBorder([int topInclBorder])
```

### <a name="parameters---top100mminclborder"></a><span data-ttu-id="80dfc-779">パラメーター - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="80dfc-779">Parameters - top100mmInclBorder</span></span>

<span data-ttu-id="80dfc-780">topInclBorder</span><span class="sxs-lookup"><span data-stu-id="80dfc-780">topInclBorder</span></span>  

### <a name="return-value---top100mminclborder"></a><span data-ttu-id="80dfc-781">戻り値 - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="80dfc-781">Return Value - top100mmInclBorder</span></span>

## <a name="method-topmarginandframe"></a><span data-ttu-id="80dfc-782">メソッド topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="80dfc-782">Method topMarginAndFrame</span></span>

```xpp
public int topMarginAndFrame()
```

### <a name="return-value---topmarginandframe"></a><span data-ttu-id="80dfc-783">戻り値 - topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="80dfc-783">Return Value - topMarginAndFrame</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="80dfc-784">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-784">Method topMarginMode</span></span>

```xpp
public int topMarginMode([int value])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="80dfc-785">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-785">Parameters - topMarginMode</span></span>

<span data-ttu-id="80dfc-786">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-786">value</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="80dfc-787">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-787">Return Value - topMarginMode</span></span>

## <a name="method-topmarginstr"></a><span data-ttu-id="80dfc-788">メソッド topMarginStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-788">Method topMarginStr</span></span>

```xpp
public str topMarginStr([str value])
```

### <a name="parameters---topmarginstr"></a><span data-ttu-id="80dfc-789">パラメーター - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-789">Parameters - topMarginStr</span></span>

<span data-ttu-id="80dfc-790">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-790">value</span></span>  

### <a name="return-value---topmarginstr"></a><span data-ttu-id="80dfc-791">戻り値 - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-791">Return Value - topMarginStr</span></span>

## <a name="method-topmarginunit"></a><span data-ttu-id="80dfc-792">メソッド topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-792">Method topMarginUnit</span></span>

```xpp
public Units topMarginUnit([Units value])
```

### <a name="parameters---topmarginunit"></a><span data-ttu-id="80dfc-793">パラメーター - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-793">Parameters - topMarginUnit</span></span>

<span data-ttu-id="80dfc-794">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-794">value</span></span>  

### <a name="return-value---topmarginunit"></a><span data-ttu-id="80dfc-795">戻り値 - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-795">Return Value - topMarginUnit</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="80dfc-796">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-796">Method topMarginValue</span></span>

```xpp
public Real topMarginValue([Real value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="80dfc-797">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-797">Parameters - topMarginValue</span></span>

<span data-ttu-id="80dfc-798">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-798">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="80dfc-799">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-799">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="80dfc-800">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-800">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="80dfc-801">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-801">Parameters - topMode</span></span>

<span data-ttu-id="80dfc-802">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-802">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="80dfc-803">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-803">Return Value - topMode</span></span>

## <a name="method-topstr"></a><span data-ttu-id="80dfc-804">メソッド topStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-804">Method topStr</span></span>

```xpp
public str topStr([str value])
```

### <a name="parameters---topstr"></a><span data-ttu-id="80dfc-805">パラメーター - topStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-805">Parameters - topStr</span></span>

<span data-ttu-id="80dfc-806">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-806">value</span></span>  

### <a name="return-value---topstr"></a><span data-ttu-id="80dfc-807">戻り値 - topStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-807">Return Value - topStr</span></span>

## <a name="method-topunit"></a><span data-ttu-id="80dfc-808">メソッド topUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-808">Method topUnit</span></span>

```xpp
public Units topUnit([Units value])
```

### <a name="parameters---topunit"></a><span data-ttu-id="80dfc-809">パラメーター - topUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-809">Parameters - topUnit</span></span>

<span data-ttu-id="80dfc-810">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-810">value</span></span>  

### <a name="return-value---topunit"></a><span data-ttu-id="80dfc-811">戻り値 - topUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-811">Return Value - topUnit</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="80dfc-812">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-812">Method topValue</span></span>

```xpp
public Real topValue([Real value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="80dfc-813">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-813">Parameters - topValue</span></span>

<span data-ttu-id="80dfc-814">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-814">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="80dfc-815">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-815">Return Value - topValue</span></span>

## <a name="method-underline"></a><span data-ttu-id="80dfc-816">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="80dfc-816">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="80dfc-817">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="80dfc-817">Parameters - underline</span></span>

<span data-ttu-id="80dfc-818">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-818">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="80dfc-819">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="80dfc-819">Return Value - underline</span></span>

## <a name="method-visible"></a><span data-ttu-id="80dfc-820">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="80dfc-820">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="80dfc-821">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="80dfc-821">Parameters - visible</span></span>

<span data-ttu-id="80dfc-822">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-822">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="80dfc-823">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="80dfc-823">Return Value - visible</span></span>

## <a name="method-webmenuitemname"></a><span data-ttu-id="80dfc-824">メソッド webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="80dfc-824">Method webMenuItemName</span></span>

```xpp
public str webMenuItemName([str value])
```

### <a name="parameters---webmenuitemname"></a><span data-ttu-id="80dfc-825">パラメーター - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="80dfc-825">Parameters - webMenuItemName</span></span>

<span data-ttu-id="80dfc-826">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-826">value</span></span>  

### <a name="return-value---webmenuitemname"></a><span data-ttu-id="80dfc-827">戻り値 - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="80dfc-827">Return Value - webMenuItemName</span></span>

## <a name="method-webmenuitemtype"></a><span data-ttu-id="80dfc-828">メソッド webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="80dfc-828">Method webMenuItemType</span></span>

```xpp
public WebMenuItemType webMenuItemType([WebMenuItemType value])
```

### <a name="parameters---webmenuitemtype"></a><span data-ttu-id="80dfc-829">パラメーター - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="80dfc-829">Parameters - webMenuItemType</span></span>

<span data-ttu-id="80dfc-830">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-830">value</span></span>  

### <a name="return-value---webmenuitemtype"></a><span data-ttu-id="80dfc-831">戻り値 - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="80dfc-831">Return Value - webMenuItemType</span></span>

## <a name="method-webtarget"></a><span data-ttu-id="80dfc-832">メソッド webTarget</span><span class="sxs-lookup"><span data-stu-id="80dfc-832">Method webTarget</span></span>

```xpp
public str webTarget([str value])
```

### <a name="parameters---webtarget"></a><span data-ttu-id="80dfc-833">パラメーター - webTarget</span><span class="sxs-lookup"><span data-stu-id="80dfc-833">Parameters - webTarget</span></span>

<span data-ttu-id="80dfc-834">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-834">value</span></span>  

### <a name="return-value---webtarget"></a><span data-ttu-id="80dfc-835">戻り値 - webTarget</span><span class="sxs-lookup"><span data-stu-id="80dfc-835">Return Value - webTarget</span></span>

## <a name="method-width100mm"></a><span data-ttu-id="80dfc-836">メソッド width100mm</span><span class="sxs-lookup"><span data-stu-id="80dfc-836">Method width100mm</span></span>

```xpp
public int width100mm([int widthExclBorder])
```

### <a name="parameters---width100mm"></a><span data-ttu-id="80dfc-837">パラメーター - width100mm</span><span class="sxs-lookup"><span data-stu-id="80dfc-837">Parameters - width100mm</span></span>

<span data-ttu-id="80dfc-838">widthExclBorder</span><span class="sxs-lookup"><span data-stu-id="80dfc-838">widthExclBorder</span></span>  

### <a name="return-value---width100mm"></a><span data-ttu-id="80dfc-839">戻り値 - width100mm</span><span class="sxs-lookup"><span data-stu-id="80dfc-839">Return Value - width100mm</span></span>

## <a name="method-width100mminclborder"></a><span data-ttu-id="80dfc-840">メソッド width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="80dfc-840">Method width100mmInclBorder</span></span>

```xpp
public int width100mmInclBorder([int widthInclBorder])
```

### <a name="parameters---width100mminclborder"></a><span data-ttu-id="80dfc-841">パラメーター - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="80dfc-841">Parameters - width100mmInclBorder</span></span>

<span data-ttu-id="80dfc-842">widthInclBorder</span><span class="sxs-lookup"><span data-stu-id="80dfc-842">widthInclBorder</span></span>  

### <a name="return-value---width100mminclborder"></a><span data-ttu-id="80dfc-843">戻り値 - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="80dfc-843">Return Value - width100mmInclBorder</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="80dfc-844">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-844">Method widthMode</span></span>

<span data-ttu-id="80dfc-845">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-845">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="80dfc-846">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-846">Parameters - widthMode</span></span>

<span data-ttu-id="80dfc-847">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-847">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="80dfc-848">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-848">Return Value - widthMode</span></span>

<span data-ttu-id="80dfc-849">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="80dfc-849">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="80dfc-850">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="80dfc-850">Remarks - widthMode</span></span>

<span data-ttu-id="80dfc-851">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="80dfc-851">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="80dfc-852">モード。</span><span class="sxs-lookup"><span data-stu-id="80dfc-852">Mode.</span></span>         | <span data-ttu-id="80dfc-853">幅計算。</span><span class="sxs-lookup"><span data-stu-id="80dfc-853">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="80dfc-854">正確。</span><span class="sxs-lookup"><span data-stu-id="80dfc-854">Exact.</span></span>        | <span data-ttu-id="80dfc-855">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="80dfc-855">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="80dfc-856">自動。</span><span class="sxs-lookup"><span data-stu-id="80dfc-856">Auto.</span></span>         | <span data-ttu-id="80dfc-857">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="80dfc-857">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="80dfc-858">列の幅。</span><span class="sxs-lookup"><span data-stu-id="80dfc-858">Column width.</span></span> | <span data-ttu-id="80dfc-859">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="80dfc-859">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="80dfc-860">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="80dfc-860">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthofstring100mm"></a><span data-ttu-id="80dfc-861">メソッド widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="80dfc-861">Method widthOfString100mm</span></span>

```xpp
public int widthOfString100mm(str string)
```

### <a name="parameters---widthofstring100mm"></a><span data-ttu-id="80dfc-862">パラメーター - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="80dfc-862">Parameters - widthOfString100mm</span></span>

<span data-ttu-id="80dfc-863">文字列</span><span class="sxs-lookup"><span data-stu-id="80dfc-863">string</span></span>  

### <a name="return-value---widthofstring100mm"></a><span data-ttu-id="80dfc-864">戻り値 - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="80dfc-864">Return Value - widthOfString100mm</span></span>

## <a name="method-widthstr"></a><span data-ttu-id="80dfc-865">メソッド widthStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-865">Method widthStr</span></span>

```xpp
public str widthStr([str value])
```

### <a name="parameters---widthstr"></a><span data-ttu-id="80dfc-866">パラメーター - widthStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-866">Parameters - widthStr</span></span>

<span data-ttu-id="80dfc-867">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-867">value</span></span>  

### <a name="return-value---widthstr"></a><span data-ttu-id="80dfc-868">戻り値 - widthStr</span><span class="sxs-lookup"><span data-stu-id="80dfc-868">Return Value - widthStr</span></span>

## <a name="method-widthunit"></a><span data-ttu-id="80dfc-869">メソッド widthUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-869">Method widthUnit</span></span>

```xpp
public Units widthUnit([Units value])
```

### <a name="parameters---widthunit"></a><span data-ttu-id="80dfc-870">パラメーター - widthUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-870">Parameters - widthUnit</span></span>

<span data-ttu-id="80dfc-871">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-871">value</span></span>  

### <a name="return-value---widthunit"></a><span data-ttu-id="80dfc-872">戻り値 - widthUnit</span><span class="sxs-lookup"><span data-stu-id="80dfc-872">Return Value - widthUnit</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="80dfc-873">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-873">Method widthValue</span></span>

<span data-ttu-id="80dfc-874">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-874">Gets or sets the width of the control.</span></span>

```xpp
public Real widthValue([Real value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="80dfc-875">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-875">Parameters - widthValue</span></span>

<span data-ttu-id="80dfc-876">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-876">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="80dfc-877">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-877">Return Value - widthValue</span></span>

<span data-ttu-id="80dfc-878">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="80dfc-878">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="80dfc-879">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="80dfc-879">Remarks - widthValue</span></span>

<span data-ttu-id="80dfc-880">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-880">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-height"></a><span data-ttu-id="80dfc-881">メソッド height</span><span class="sxs-lookup"><span data-stu-id="80dfc-881">Method height</span></span>

<span data-ttu-id="80dfc-882">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-882">Gets or sets the height of the control.</span></span>

```xpp
public void height(Real value, Units unit)
```

### <a name="parameters---height"></a><span data-ttu-id="80dfc-883">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="80dfc-883">Parameters - height</span></span>

<span data-ttu-id="80dfc-884">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-884">value</span></span>  

<!-- -->

<span data-ttu-id="80dfc-885">単位</span><span class="sxs-lookup"><span data-stu-id="80dfc-885">unit</span></span>  

### <a name="remarks---height"></a><span data-ttu-id="80dfc-886">備考 - height</span><span class="sxs-lookup"><span data-stu-id="80dfc-886">Remarks - height</span></span>

<span data-ttu-id="80dfc-887">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="80dfc-887">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="80dfc-888">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="80dfc-888">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="80dfc-889">モード。</span><span class="sxs-lookup"><span data-stu-id="80dfc-889">Mode.</span></span>            | <span data-ttu-id="80dfc-890">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="80dfc-890">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="80dfc-891">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="80dfc-891">-1 Exact.</span></span>        | <span data-ttu-id="80dfc-892">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="80dfc-892">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="80dfc-893">0 自動。</span><span class="sxs-lookup"><span data-stu-id="80dfc-893">0 Auto.</span></span>          | <span data-ttu-id="80dfc-894">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="80dfc-894">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="80dfc-895">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="80dfc-895">1 Column height.</span></span> | <span data-ttu-id="80dfc-896">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="80dfc-896">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="80dfc-897">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="80dfc-897">The height and height calculation mode can be set separately.</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="80dfc-898">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="80dfc-898">Method topMargin</span></span>

```xpp
public void topMargin(Real value, Units unit)
```

### <a name="parameters---topmargin"></a><span data-ttu-id="80dfc-899">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="80dfc-899">Parameters - topMargin</span></span>

<span data-ttu-id="80dfc-900">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-900">value</span></span>  

<!-- -->

<span data-ttu-id="80dfc-901">単位</span><span class="sxs-lookup"><span data-stu-id="80dfc-901">unit</span></span>  

## <a name="method-labelwidth"></a><span data-ttu-id="80dfc-902">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="80dfc-902">Method labelWidth</span></span>

```xpp
public void labelWidth(Real value, Units unit)
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="80dfc-903">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="80dfc-903">Parameters - labelWidth</span></span>

<span data-ttu-id="80dfc-904">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-904">value</span></span>  

<!-- -->

<span data-ttu-id="80dfc-905">単位</span><span class="sxs-lookup"><span data-stu-id="80dfc-905">unit</span></span>  

## <a name="method-hide"></a><span data-ttu-id="80dfc-906">メソッド hide</span><span class="sxs-lookup"><span data-stu-id="80dfc-906">Method hide</span></span>

```xpp
public void hide()
```

## <a name="method-left"></a><span data-ttu-id="80dfc-907">メソッド left</span><span class="sxs-lookup"><span data-stu-id="80dfc-907">Method left</span></span>

```xpp
public void left(Real value, Units unit)
```

### <a name="parameters---left"></a><span data-ttu-id="80dfc-908">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="80dfc-908">Parameters - left</span></span>

<span data-ttu-id="80dfc-909">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-909">value</span></span>  

<!-- -->

<span data-ttu-id="80dfc-910">単位</span><span class="sxs-lookup"><span data-stu-id="80dfc-910">unit</span></span>  

## <a name="method-rightmargin"></a><span data-ttu-id="80dfc-911">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="80dfc-911">Method rightMargin</span></span>

```xpp
public void rightMargin(Real value, Units unit)
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="80dfc-912">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="80dfc-912">Parameters - rightMargin</span></span>

<span data-ttu-id="80dfc-913">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-913">value</span></span>  

<!-- -->

<span data-ttu-id="80dfc-914">単位</span><span class="sxs-lookup"><span data-stu-id="80dfc-914">unit</span></span>  

## <a name="method-show"></a><span data-ttu-id="80dfc-915">メソッド show</span><span class="sxs-lookup"><span data-stu-id="80dfc-915">Method show</span></span>

```xpp
public void show()
```

## <a name="method-width"></a><span data-ttu-id="80dfc-916">メソッド width</span><span class="sxs-lookup"><span data-stu-id="80dfc-916">Method width</span></span>

<span data-ttu-id="80dfc-917">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="80dfc-917">Gets or sets the width of the control.</span></span>

```xpp
public void width(Real value, Units unit)
```

### <a name="parameters---width"></a><span data-ttu-id="80dfc-918">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="80dfc-918">Parameters - width</span></span>

<span data-ttu-id="80dfc-919">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-919">value</span></span>  

<!-- -->

<span data-ttu-id="80dfc-920">単位</span><span class="sxs-lookup"><span data-stu-id="80dfc-920">unit</span></span>  

### <a name="remarks---width"></a><span data-ttu-id="80dfc-921">備考 - width</span><span class="sxs-lookup"><span data-stu-id="80dfc-921">Remarks - width</span></span>

<span data-ttu-id="80dfc-922">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="80dfc-922">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="80dfc-923">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="80dfc-923">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="80dfc-924">モード。</span><span class="sxs-lookup"><span data-stu-id="80dfc-924">Mode.</span></span>           | <span data-ttu-id="80dfc-925">幅計算。</span><span class="sxs-lookup"><span data-stu-id="80dfc-925">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="80dfc-926">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="80dfc-926">-1 Exact.</span></span>       | <span data-ttu-id="80dfc-927">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="80dfc-927">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="80dfc-928">0 自動。</span><span class="sxs-lookup"><span data-stu-id="80dfc-928">0 Auto.</span></span>         | <span data-ttu-id="80dfc-929">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="80dfc-929">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="80dfc-930">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="80dfc-930">1 Column width.</span></span> | <span data-ttu-id="80dfc-931">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="80dfc-931">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="80dfc-932">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="80dfc-932">The width and width calculation mode can be set separately.</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="80dfc-933">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="80dfc-933">Method leftMargin</span></span>

```xpp
public void leftMargin(Real value, Units unit)
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="80dfc-934">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="80dfc-934">Parameters - leftMargin</span></span>

<span data-ttu-id="80dfc-935">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-935">value</span></span>  

<!-- -->

<span data-ttu-id="80dfc-936">単位</span><span class="sxs-lookup"><span data-stu-id="80dfc-936">unit</span></span>  

## <a name="method-bottommargin"></a><span data-ttu-id="80dfc-937">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="80dfc-937">Method bottomMargin</span></span>

```xpp
public void bottomMargin(Real value, Units unit)
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="80dfc-938">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="80dfc-938">Parameters - bottomMargin</span></span>

<span data-ttu-id="80dfc-939">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-939">value</span></span>  

<!-- -->

<span data-ttu-id="80dfc-940">単位</span><span class="sxs-lookup"><span data-stu-id="80dfc-940">unit</span></span>  

## <a name="method-top"></a><span data-ttu-id="80dfc-941">メソッド top</span><span class="sxs-lookup"><span data-stu-id="80dfc-941">Method top</span></span>

```xpp
public void top(Real value, Units unit)
```

### <a name="parameters---top"></a><span data-ttu-id="80dfc-942">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="80dfc-942">Parameters - top</span></span>

<span data-ttu-id="80dfc-943">値</span><span class="sxs-lookup"><span data-stu-id="80dfc-943">value</span></span>  

<!-- -->

<span data-ttu-id="80dfc-944">単位</span><span class="sxs-lookup"><span data-stu-id="80dfc-944">unit</span></span>  

