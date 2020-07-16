---
title: ReportTimeControl クラス
description: このトピックでは、ReportTimeControl クラスについて説明します。
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
ms.openlocfilehash: bb292505992c5857783d9297f59ecba62e719648
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502825"
---
# <a name="class-reporttimecontrol"></a><span data-ttu-id="fa306-103">クラス ReportTimeControl</span><span class="sxs-lookup"><span data-stu-id="fa306-103">Class ReportTimeControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ReportTimeControl extends ReportControl
```

<span data-ttu-id="fa306-104">ReportTimeControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="fa306-104">The ReportTimeControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa306-105">備考</span><span class="sxs-lookup"><span data-stu-id="fa306-105">Remarks</span></span>

<span data-ttu-id="fa306-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fa306-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="fa306-107">例</span><span class="sxs-lookup"><span data-stu-id="fa306-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="fa306-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="fa306-108">Methods</span></span>

| <span data-ttu-id="fa306-109">方法</span><span class="sxs-lookup"><span data-stu-id="fa306-109">Method</span></span>                                                                   | <span data-ttu-id="fa306-110">説明</span><span class="sxs-lookup"><span data-stu-id="fa306-110">Description</span></span>                                                                                                                               |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa306-111">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-111">public int alignment(\[int value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="fa306-112">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-112">public int arrayIndex(\[int value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="fa306-113">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-113">public boolean autoDeclaration(\[boolean value\])</span></span>                        | <span data-ttu-id="fa306-114">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-114">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                        |
| <span data-ttu-id="fa306-115">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-115">public int backgroundColor(\[int value\])</span></span>                                | <span data-ttu-id="fa306-116">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-116">Gets or sets the background color of the control.</span></span>                                                                                         |
| <span data-ttu-id="fa306-117">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-117">public int backStyle(\[int value\])</span></span>                                      | <span data-ttu-id="fa306-118">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-118">Determines whether the control background can be transparent.</span></span>                                                                            |
| <span data-ttu-id="fa306-119">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-119">public int bold(\[int value\])</span></span>                                           | <span data-ttu-id="fa306-120">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-120">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                               |
| <span data-ttu-id="fa306-121">public int bottomMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="fa306-121">public int bottomMarginAndFrame()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="fa306-122">public int bottomMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-122">public int bottomMarginMode(\[int value\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="fa306-123">public str bottomMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-123">public str bottomMarginStr(\[str value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="fa306-124">public Units bottomMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-124">public Units bottomMarginUnit(\[Units value\])</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="fa306-125">public Real bottomMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-125">public Real bottomMarginValue(\[Real value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="fa306-126">public int changeLabelCase(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-126">public int changeLabelCase(\[int value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="fa306-127">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-127">public int characterSet(\[int value\])</span></span>                                   | <span data-ttu-id="fa306-128">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-128">Gets or sets the character set of the font.</span></span>                                                                                               |
| <span data-ttu-id="fa306-129">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-129">public int colorScheme(\[int value\])</span></span>                                    | <span data-ttu-id="fa306-130">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-130">Gets or sets the color scheme of the control.</span></span>                                                                                             |
| <span data-ttu-id="fa306-131">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-131">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="fa306-132">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-132">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                       |
| <span data-ttu-id="fa306-133">public ReportFieldType controlType()</span><span class="sxs-lookup"><span data-stu-id="fa306-133">public ReportFieldType controlType()</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="fa306-134">public str cssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-134">public str cssClass(\[str value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="fa306-135">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-135">public FieldId dataField(\[FieldId value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="fa306-136">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-136">public str dataMethod(\[str value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="fa306-137">public int delete()</span><span class="sxs-lookup"><span data-stu-id="fa306-137">public int delete()</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="fa306-138">public str effectiveFont()</span><span class="sxs-lookup"><span data-stu-id="fa306-138">public str effectiveFont()</span></span>                                               |                                                                                                                                           |
| <span data-ttu-id="fa306-139">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-139">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>         |                                                                                                                                           |
| <span data-ttu-id="fa306-140">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-140">public str font(\[str value\])</span></span>                                           | <span data-ttu-id="fa306-141">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-141">Gets or sets the name of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="fa306-142">public str fontInfoPrinter()</span><span class="sxs-lookup"><span data-stu-id="fa306-142">public str fontInfoPrinter()</span></span>                                             |                                                                                                                                           |
| <span data-ttu-id="fa306-143">public int fontInfoPrinterAscent()</span><span class="sxs-lookup"><span data-stu-id="fa306-143">public int fontInfoPrinterAscent()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="fa306-144">public int fontInfoPrinterDescent()</span><span class="sxs-lookup"><span data-stu-id="fa306-144">public int fontInfoPrinterDescent()</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="fa306-145">public int fontInfoPrinterExtLead()</span><span class="sxs-lookup"><span data-stu-id="fa306-145">public int fontInfoPrinterExtLead()</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="fa306-146">public int fontInfoPrinterHeight()</span><span class="sxs-lookup"><span data-stu-id="fa306-146">public int fontInfoPrinterHeight()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="fa306-147">public int fontInfoPrinterIntLead()</span><span class="sxs-lookup"><span data-stu-id="fa306-147">public int fontInfoPrinterIntLead()</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="fa306-148">public str fontInfoScreen()</span><span class="sxs-lookup"><span data-stu-id="fa306-148">public str fontInfoScreen()</span></span>                                              |                                                                                                                                           |
| <span data-ttu-id="fa306-149">public int fontInfoScreenAscent()</span><span class="sxs-lookup"><span data-stu-id="fa306-149">public int fontInfoScreenAscent()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="fa306-150">public int fontInfoScreenDescent()</span><span class="sxs-lookup"><span data-stu-id="fa306-150">public int fontInfoScreenDescent()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="fa306-151">public int fontInfoScreenExtLead()</span><span class="sxs-lookup"><span data-stu-id="fa306-151">public int fontInfoScreenExtLead()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="fa306-152">public int fontInfoScreenHeight()</span><span class="sxs-lookup"><span data-stu-id="fa306-152">public int fontInfoScreenHeight()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="fa306-153">public int fontInfoScreenIntLead()</span><span class="sxs-lookup"><span data-stu-id="fa306-153">public int fontInfoScreenIntLead()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="fa306-154">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-154">public int fontSize(\[int value\])</span></span>                                       | <span data-ttu-id="fa306-155">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-155">Gets or sets the size of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="fa306-156">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-156">public int foregroundColor(\[int value\])</span></span>                                | <span data-ttu-id="fa306-157">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-157">Gets or sets the text color for the control to use.</span></span>                                                                                       |
| <span data-ttu-id="fa306-158">public int height100mm(\[int heightExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="fa306-158">public int height100mm(\[int heightExclBorder\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="fa306-159">public int height100mmInclBorder(\[int heightInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="fa306-159">public int height100mmInclBorder(\[int heightInclBorder\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="fa306-160">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-160">public int heightMode(\[int value\])</span></span>                                     | <span data-ttu-id="fa306-161">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-161">Gets or sets a calculation mode for the height of the control.</span></span>                                                                            |
| <span data-ttu-id="fa306-162">public int heightOfWordWrappedString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="fa306-162">public int heightOfWordWrappedString100mm(str string)</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="fa306-163">public str heightStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-163">public str heightStr(\[str value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="fa306-164">public Units heightUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-164">public Units heightUnit(\[Units value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="fa306-165">public Real heightValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-165">public Real heightValue(\[Real value\])</span></span>                                  | <span data-ttu-id="fa306-166">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-166">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="fa306-167">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-167">public boolean italic(\[boolean value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="fa306-168">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-168">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="fa306-169">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-169">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="fa306-170">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-170">public int labelBold(\[int value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="fa306-171">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-171">public int labelCharacterSet(\[int value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="fa306-172">public str labelCssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-172">public str labelCssClass(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="fa306-173">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-173">public str labelFont(\[str value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="fa306-174">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-174">public int labelFontSize(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="fa306-175">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-175">public boolean labelItalic(\[boolean value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="fa306-176">public LineType labelLineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-176">public LineType labelLineBelow(\[LineType value\])</span></span>                       |                                                                                                                                           |
| <span data-ttu-id="fa306-177">public LineThickness labelLineThickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-177">public LineThickness labelLineThickness(\[LineThickness value\])</span></span>         |                                                                                                                                           |
| <span data-ttu-id="fa306-178">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-178">public int labelPosition(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="fa306-179">public int labelTabLeader(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-179">public int labelTabLeader(\[int value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="fa306-180">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-180">public boolean labelUnderline(\[boolean value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="fa306-181">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-181">public int labelWidthMode(\[int value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="fa306-182">public str labelWidthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-182">public str labelWidthStr(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="fa306-183">public Units labelWidthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-183">public Units labelWidthUnit(\[Units value\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="fa306-184">public Real labelWidthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-184">public Real labelWidthValue(\[Real value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="fa306-185">public int left100mm(\[int leftExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="fa306-185">public int left100mm(\[int leftExclBorder\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="fa306-186">public int left100mmInclBorder(\[int leftInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="fa306-186">public int left100mmInclBorder(\[int leftInclBorder\])</span></span>                   |                                                                                                                                           |
| <span data-ttu-id="fa306-187">public int leftMarginAnFrame()</span><span class="sxs-lookup"><span data-stu-id="fa306-187">public int leftMarginAnFrame()</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="fa306-188">public int leftMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-188">public int leftMarginMode(\[int value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="fa306-189">public str leftMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-189">public str leftMarginStr(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="fa306-190">public Units leftMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-190">public Units leftMarginUnit(\[Units value\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="fa306-191">public Real leftMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-191">public Real leftMarginValue(\[Real value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="fa306-192">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-192">public int leftMode(\[int value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="fa306-193">public str leftStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-193">public str leftStr(\[str value\])</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="fa306-194">public Units leftUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-194">public Units leftUnit(\[Units value\])</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="fa306-195">public Real leftValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-195">public Real leftValue(\[Real value\])</span></span>                                    |                                                                                                                                           |
| <span data-ttu-id="fa306-196">public LineType lineAbove(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-196">public LineType lineAbove(\[LineType value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="fa306-197">public LineType lineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-197">public LineType lineBelow(\[LineType value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="fa306-198">public LineType lineLeft(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-198">public LineType lineLeft(\[LineType value\])</span></span>                             | <span data-ttu-id="fa306-199">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-199">Gets or sets the type of line that is used as the left border of a section.</span></span>                                                               |
| <span data-ttu-id="fa306-200">public LineType lineRight(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-200">public LineType lineRight(\[LineType value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="fa306-201">public str menuItemLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-201">public str menuItemLabel(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="fa306-202">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-202">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="fa306-203">public MenuItemType menuItemType(\[MenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-203">public MenuItemType menuItemType(\[MenuItemType value\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="fa306-204">public str modelFieldName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-204">public str modelFieldName(\[str value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="fa306-205">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-205">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="fa306-206">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-206">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="fa306-207">public int numberOfLines(int height100mm)</span><span class="sxs-lookup"><span data-stu-id="fa306-207">public int numberOfLines(int height100mm)</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="fa306-208">public int position(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-208">public int position(\[int value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="fa306-209">public str previewInfo(str string)</span><span class="sxs-lookup"><span data-stu-id="fa306-209">public str previewInfo(str string)</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="fa306-210">public int previewXCompensation100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="fa306-210">public int previewXCompensation100mm(str string)</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="fa306-211">public int right100mm()</span><span class="sxs-lookup"><span data-stu-id="fa306-211">public int right100mm()</span></span>                                                  |                                                                                                                                           |
| <span data-ttu-id="fa306-212">public int right100mmInclBorder()</span><span class="sxs-lookup"><span data-stu-id="fa306-212">public int right100mmInclBorder()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="fa306-213">public int rightMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="fa306-213">public int rightMarginAndFrame()</span></span>                                         |                                                                                                                                           |
| <span data-ttu-id="fa306-214">public int rightMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-214">public int rightMarginMode(\[int value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="fa306-215">public str rightMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-215">public str rightMarginStr(\[str value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="fa306-216">public Units rightMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-216">public Units rightMarginUnit(\[Units value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="fa306-217">public Real rightMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-217">public Real rightMarginValue(\[Real value\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="fa306-218">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-218">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                                           |
| <span data-ttu-id="fa306-219">public str setHeightGetText(int lines, str string)</span><span class="sxs-lookup"><span data-stu-id="fa306-219">public str setHeightGetText(int lines, str string)</span></span>                       |                                                                                                                                           |
| <span data-ttu-id="fa306-220">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-220">public boolean showLabel(\[boolean value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="fa306-221">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-221">public TableId table(\[TableId value\])</span></span>                                  | <span data-ttu-id="fa306-222">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-222">Gets or sets the table ID associated with the object.</span></span>                                                                                     |
| <span data-ttu-id="fa306-223">public LineThickness thickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-223">public LineThickness thickness(\[LineThickness value\])</span></span>                  |                                                                                                                                           |
| <span data-ttu-id="fa306-224">public int timeFormat(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-224">public int timeFormat(\[int value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="fa306-225">public int timeHours(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-225">public int timeHours(\[int value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="fa306-226">public int timeMinute(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-226">public int timeMinute(\[int value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="fa306-227">public int timeSeconds(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-227">public int timeSeconds(\[int value\])</span></span>                                    |                                                                                                                                           |
| <span data-ttu-id="fa306-228">public int timeSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-228">public int timeSeparator(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="fa306-229">public int top100mm(\[int topExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="fa306-229">public int top100mm(\[int topExclBorder\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="fa306-230">public int top100mmInclBorder(\[int topInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="fa306-230">public int top100mmInclBorder(\[int topInclBorder\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="fa306-231">public int topMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="fa306-231">public int topMarginAndFrame()</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="fa306-232">public int topMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-232">public int topMarginMode(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="fa306-233">public str topMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-233">public str topMarginStr(\[str value\])</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="fa306-234">public Units topMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-234">public Units topMarginUnit(\[Units value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="fa306-235">public Real topMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-235">public Real topMarginValue(\[Real value\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="fa306-236">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-236">public int topMode(\[int value\])</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="fa306-237">public str topStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-237">public str topStr(\[str value\])</span></span>                                         |                                                                                                                                           |
| <span data-ttu-id="fa306-238">public Units topUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-238">public Units topUnit(\[Units value\])</span></span>                                    |                                                                                                                                           |
| <span data-ttu-id="fa306-239">public Real topValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-239">public Real topValue(\[Real value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="fa306-240">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-240">public boolean underline(\[boolean value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="fa306-241">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-241">public boolean visible(\[boolean value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="fa306-242">public str webMenuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-242">public str webMenuItemName(\[str value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="fa306-243">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-243">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span></span>        |                                                                                                                                           |
| <span data-ttu-id="fa306-244">public str webTarget(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-244">public str webTarget(\[str value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="fa306-245">public int width100mm(\[int widthExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="fa306-245">public int width100mm(\[int widthExclBorder\])</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="fa306-246">public int width100mmInclBorder(\[int widthInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="fa306-246">public int width100mmInclBorder(\[int widthInclBorder\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="fa306-247">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-247">public int widthMode(\[int value\])</span></span>                                      | <span data-ttu-id="fa306-248">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-248">Gets or sets the calculation mode of the width of the control.</span></span>                                                                            |
| <span data-ttu-id="fa306-249">public int widthOfString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="fa306-249">public int widthOfString100mm(str string)</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="fa306-250">public str widthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-250">public str widthStr(\[str value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="fa306-251">public Units widthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-251">public Units widthUnit(\[Units value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="fa306-252">public Real widthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="fa306-252">public Real widthValue(\[Real value\])</span></span>                                   | <span data-ttu-id="fa306-253">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-253">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="fa306-254">public void leftMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="fa306-254">public void leftMargin(Real value, Units unit)</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="fa306-255">public void rightMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="fa306-255">public void rightMargin(Real value, Units unit)</span></span>                          |                                                                                                                                           |
| <span data-ttu-id="fa306-256">public void bottomMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="fa306-256">public void bottomMargin(Real value, Units unit)</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="fa306-257">public void width(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="fa306-257">public void width(Real value, Units unit)</span></span>                                | <span data-ttu-id="fa306-258">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-258">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="fa306-259">public void top(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="fa306-259">public void top(Real value, Units unit)</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="fa306-260">public void height(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="fa306-260">public void height(Real value, Units unit)</span></span>                               | <span data-ttu-id="fa306-261">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-261">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="fa306-262">public void labelWidth(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="fa306-262">public void labelWidth(Real value, Units unit)</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="fa306-263">public void topMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="fa306-263">public void topMargin(Real value, Units unit)</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="fa306-264">public void left(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="fa306-264">public void left(Real value, Units unit)</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="fa306-265">public void hide()</span><span class="sxs-lookup"><span data-stu-id="fa306-265">public void hide()</span></span>                                                       |                                                                                                                                           |
| <span data-ttu-id="fa306-266">public void show()</span><span class="sxs-lookup"><span data-stu-id="fa306-266">public void show()</span></span>                                                       |                                                                                                                                           |

## <a name="method-alignment"></a><span data-ttu-id="fa306-267">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="fa306-267">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="fa306-268">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="fa306-268">Parameters - alignment</span></span>

<span data-ttu-id="fa306-269">値</span><span class="sxs-lookup"><span data-stu-id="fa306-269">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="fa306-270">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="fa306-270">Return Value - alignment</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="fa306-271">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="fa306-271">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="fa306-272">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="fa306-272">Parameters - arrayIndex</span></span>

<span data-ttu-id="fa306-273">値</span><span class="sxs-lookup"><span data-stu-id="fa306-273">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="fa306-274">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="fa306-274">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="fa306-275">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="fa306-275">Method autoDeclaration</span></span>

<span data-ttu-id="fa306-276">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-276">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="fa306-277">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="fa306-277">Parameters - autoDeclaration</span></span>

<span data-ttu-id="fa306-278">値</span><span class="sxs-lookup"><span data-stu-id="fa306-278">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="fa306-279">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="fa306-279">Return Value - autoDeclaration</span></span>

<span data-ttu-id="fa306-280">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fa306-280">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="fa306-281">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="fa306-281">Remarks - autoDeclaration</span></span>

<span data-ttu-id="fa306-282">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="fa306-282">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="fa306-283">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="fa306-283">Method backgroundColor</span></span>

<span data-ttu-id="fa306-284">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-284">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="fa306-285">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="fa306-285">Parameters - backgroundColor</span></span>

<span data-ttu-id="fa306-286">値</span><span class="sxs-lookup"><span data-stu-id="fa306-286">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="fa306-287">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="fa306-287">Return Value - backgroundColor</span></span>

<span data-ttu-id="fa306-288">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="fa306-288">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="fa306-289">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="fa306-289">Remarks - backgroundColor</span></span>

<span data-ttu-id="fa306-290">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fa306-290">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="fa306-291">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fa306-291">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="fa306-292">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="fa306-292">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="fa306-293">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="fa306-293">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="fa306-294">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="fa306-294">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="fa306-295">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="fa306-295">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="fa306-296">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="fa306-296">Method backStyle</span></span>

<span data-ttu-id="fa306-297">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-297">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="fa306-298">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="fa306-298">Parameters - backStyle</span></span>

<span data-ttu-id="fa306-299">値</span><span class="sxs-lookup"><span data-stu-id="fa306-299">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="fa306-300">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="fa306-300">Return Value - backStyle</span></span>

<span data-ttu-id="fa306-301">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="fa306-301">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="fa306-302">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="fa306-302">Method bold</span></span>

<span data-ttu-id="fa306-303">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-303">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="fa306-304">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="fa306-304">Parameters - bold</span></span>

<span data-ttu-id="fa306-305">値</span><span class="sxs-lookup"><span data-stu-id="fa306-305">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="fa306-306">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="fa306-306">Return Value - bold</span></span>

<span data-ttu-id="fa306-307">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="fa306-307">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="fa306-308">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="fa306-308">Remarks - bold</span></span>

<span data-ttu-id="fa306-309">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="fa306-309">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="fa306-310">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="fa306-310">0 Use the default font weight.</span></span>
-   <span data-ttu-id="fa306-311">1 シン。</span><span class="sxs-lookup"><span data-stu-id="fa306-311">1 Thin.</span></span>
-   <span data-ttu-id="fa306-312">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="fa306-312">2 Extra-light.</span></span>
-   <span data-ttu-id="fa306-313">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="fa306-313">3 Light.</span></span>
-   <span data-ttu-id="fa306-314">4 標準。</span><span class="sxs-lookup"><span data-stu-id="fa306-314">4 Normal.</span></span>
-   <span data-ttu-id="fa306-315">5 中。</span><span class="sxs-lookup"><span data-stu-id="fa306-315">5 Medium.</span></span>
-   <span data-ttu-id="fa306-316">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="fa306-316">6 Semibold.</span></span>
-   <span data-ttu-id="fa306-317">7 太字。</span><span class="sxs-lookup"><span data-stu-id="fa306-317">7 Bold.</span></span>
-   <span data-ttu-id="fa306-318">8 極太。</span><span class="sxs-lookup"><span data-stu-id="fa306-318">8 Extra-bold.</span></span>
-   <span data-ttu-id="fa306-319">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="fa306-319">9 Heavy.</span></span>

## <a name="method-bottommarginandframe"></a><span data-ttu-id="fa306-320">メソッド bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="fa306-320">Method bottomMarginAndFrame</span></span>

```xpp
public int bottomMarginAndFrame()
```

### <a name="return-value---bottommarginandframe"></a><span data-ttu-id="fa306-321">戻り値 - bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="fa306-321">Return Value - bottomMarginAndFrame</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="fa306-322">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="fa306-322">Method bottomMarginMode</span></span>

```xpp
public int bottomMarginMode([int value])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="fa306-323">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="fa306-323">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="fa306-324">値</span><span class="sxs-lookup"><span data-stu-id="fa306-324">value</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="fa306-325">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="fa306-325">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginstr"></a><span data-ttu-id="fa306-326">メソッド bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="fa306-326">Method bottomMarginStr</span></span>

```xpp
public str bottomMarginStr([str value])
```

### <a name="parameters---bottommarginstr"></a><span data-ttu-id="fa306-327">パラメーター - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="fa306-327">Parameters - bottomMarginStr</span></span>

<span data-ttu-id="fa306-328">値</span><span class="sxs-lookup"><span data-stu-id="fa306-328">value</span></span>  

### <a name="return-value---bottommarginstr"></a><span data-ttu-id="fa306-329">戻り値 - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="fa306-329">Return Value - bottomMarginStr</span></span>

## <a name="method-bottommarginunit"></a><span data-ttu-id="fa306-330">メソッド bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-330">Method bottomMarginUnit</span></span>

```xpp
public Units bottomMarginUnit([Units value])
```

### <a name="parameters---bottommarginunit"></a><span data-ttu-id="fa306-331">パラメーター - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-331">Parameters - bottomMarginUnit</span></span>

<span data-ttu-id="fa306-332">値</span><span class="sxs-lookup"><span data-stu-id="fa306-332">value</span></span>  

### <a name="return-value---bottommarginunit"></a><span data-ttu-id="fa306-333">戻り値 - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-333">Return Value - bottomMarginUnit</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="fa306-334">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="fa306-334">Method bottomMarginValue</span></span>

```xpp
public Real bottomMarginValue([Real value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="fa306-335">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="fa306-335">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="fa306-336">値</span><span class="sxs-lookup"><span data-stu-id="fa306-336">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="fa306-337">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="fa306-337">Return Value - bottomMarginValue</span></span>

## <a name="method-changelabelcase"></a><span data-ttu-id="fa306-338">メソッド changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="fa306-338">Method changeLabelCase</span></span>

```xpp
public int changeLabelCase([int value])
```

### <a name="parameters---changelabelcase"></a><span data-ttu-id="fa306-339">パラメーター - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="fa306-339">Parameters - changeLabelCase</span></span>

<span data-ttu-id="fa306-340">値</span><span class="sxs-lookup"><span data-stu-id="fa306-340">value</span></span>  

### <a name="return-value---changelabelcase"></a><span data-ttu-id="fa306-341">戻り値 - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="fa306-341">Return Value - changeLabelCase</span></span>

## <a name="method-characterset"></a><span data-ttu-id="fa306-342">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="fa306-342">Method characterSet</span></span>

<span data-ttu-id="fa306-343">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-343">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="fa306-344">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="fa306-344">Parameters - characterSet</span></span>

<span data-ttu-id="fa306-345">値</span><span class="sxs-lookup"><span data-stu-id="fa306-345">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="fa306-346">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="fa306-346">Return Value - characterSet</span></span>

<span data-ttu-id="fa306-347">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="fa306-347">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="fa306-348">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="fa306-348">Remarks - characterSet</span></span>

<span data-ttu-id="fa306-349">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="fa306-349">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="fa306-350">値です。</span><span class="sxs-lookup"><span data-stu-id="fa306-350">Value.</span></span> | <span data-ttu-id="fa306-351">説明。</span><span class="sxs-lookup"><span data-stu-id="fa306-351">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="fa306-352">0</span><span class="sxs-lookup"><span data-stu-id="fa306-352">0</span></span>      | <span data-ttu-id="fa306-353">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fa306-353">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="fa306-354">1</span><span class="sxs-lookup"><span data-stu-id="fa306-354">1</span></span>      | <span data-ttu-id="fa306-355">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fa306-355">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="fa306-356">2</span><span class="sxs-lookup"><span data-stu-id="fa306-356">2</span></span>      | <span data-ttu-id="fa306-357">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fa306-357">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="fa306-358">77</span><span class="sxs-lookup"><span data-stu-id="fa306-358">77</span></span>     | <span data-ttu-id="fa306-359">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fa306-359">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="fa306-360">128</span><span class="sxs-lookup"><span data-stu-id="fa306-360">128</span></span>    | <span data-ttu-id="fa306-361">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fa306-361">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="fa306-362">129</span><span class="sxs-lookup"><span data-stu-id="fa306-362">129</span></span>    | <span data-ttu-id="fa306-363">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fa306-363">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="fa306-364">134</span><span class="sxs-lookup"><span data-stu-id="fa306-364">134</span></span>    | <span data-ttu-id="fa306-365">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fa306-365">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="fa306-366">136</span><span class="sxs-lookup"><span data-stu-id="fa306-366">136</span></span>    | <span data-ttu-id="fa306-367">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fa306-367">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="fa306-368">161</span><span class="sxs-lookup"><span data-stu-id="fa306-368">161</span></span>    | <span data-ttu-id="fa306-369">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fa306-369">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="fa306-370">162</span><span class="sxs-lookup"><span data-stu-id="fa306-370">162</span></span>    | <span data-ttu-id="fa306-371">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fa306-371">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="fa306-372">163</span><span class="sxs-lookup"><span data-stu-id="fa306-372">163</span></span>    | <span data-ttu-id="fa306-373">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fa306-373">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="fa306-374">186</span><span class="sxs-lookup"><span data-stu-id="fa306-374">186</span></span>    | <span data-ttu-id="fa306-375">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fa306-375">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="fa306-376">204</span><span class="sxs-lookup"><span data-stu-id="fa306-376">204</span></span>    | <span data-ttu-id="fa306-377">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fa306-377">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="fa306-378">238</span><span class="sxs-lookup"><span data-stu-id="fa306-378">238</span></span>    | <span data-ttu-id="fa306-379">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fa306-379">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="fa306-380">255</span><span class="sxs-lookup"><span data-stu-id="fa306-380">255</span></span>    | <span data-ttu-id="fa306-381">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fa306-381">OEM\_CHARSET</span></span>         |

<span data-ttu-id="fa306-382">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="fa306-382">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="fa306-383">値です。</span><span class="sxs-lookup"><span data-stu-id="fa306-383">Value.</span></span> | <span data-ttu-id="fa306-384">説明。</span><span class="sxs-lookup"><span data-stu-id="fa306-384">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="fa306-385">130</span><span class="sxs-lookup"><span data-stu-id="fa306-385">130</span></span>    | <span data-ttu-id="fa306-386">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fa306-386">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="fa306-387">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="fa306-387">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="fa306-388">値です。</span><span class="sxs-lookup"><span data-stu-id="fa306-388">Value.</span></span> | <span data-ttu-id="fa306-389">説明。</span><span class="sxs-lookup"><span data-stu-id="fa306-389">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="fa306-390">177</span><span class="sxs-lookup"><span data-stu-id="fa306-390">177</span></span>    | <span data-ttu-id="fa306-391">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fa306-391">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="fa306-392">178</span><span class="sxs-lookup"><span data-stu-id="fa306-392">178</span></span>    | <span data-ttu-id="fa306-393">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fa306-393">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="fa306-394">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="fa306-394">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="fa306-395">値です。</span><span class="sxs-lookup"><span data-stu-id="fa306-395">Value.</span></span> | <span data-ttu-id="fa306-396">説明。</span><span class="sxs-lookup"><span data-stu-id="fa306-396">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="fa306-397">222</span><span class="sxs-lookup"><span data-stu-id="fa306-397">222</span></span>    | <span data-ttu-id="fa306-398">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fa306-398">THAI\_CHARSET</span></span> |

<span data-ttu-id="fa306-399">既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="fa306-399">The default character set is set to a value, depending on the current system locale.</span></span> <span data-ttu-id="fa306-400">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="fa306-400">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="fa306-401">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fa306-401">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="fa306-402">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="fa306-402">Method colorScheme</span></span>

<span data-ttu-id="fa306-403">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-403">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="fa306-404">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="fa306-404">Parameters - colorScheme</span></span>

<span data-ttu-id="fa306-405">値</span><span class="sxs-lookup"><span data-stu-id="fa306-405">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="fa306-406">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="fa306-406">Return Value - colorScheme</span></span>

<span data-ttu-id="fa306-407">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="fa306-407">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="fa306-408">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="fa306-408">Remarks - colorScheme</span></span>

<span data-ttu-id="fa306-409">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="fa306-409">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="fa306-410">値です。</span><span class="sxs-lookup"><span data-stu-id="fa306-410">Value.</span></span> | <span data-ttu-id="fa306-411">スタイル。</span><span class="sxs-lookup"><span data-stu-id="fa306-411">Style.</span></span>                 |
|--------|------------------------|
| <span data-ttu-id="fa306-412">0</span><span class="sxs-lookup"><span data-stu-id="fa306-412">0</span></span>      | <span data-ttu-id="fa306-413">既定。</span><span class="sxs-lookup"><span data-stu-id="fa306-413">Default.</span></span>               |
| <span data-ttu-id="fa306-414">1</span><span class="sxs-lookup"><span data-stu-id="fa306-414">1</span></span>      | <span data-ttu-id="fa306-415">Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="fa306-415">The Windows palette.</span></span>   |
| <span data-ttu-id="fa306-416">2</span><span class="sxs-lookup"><span data-stu-id="fa306-416">2</span></span>      | <span data-ttu-id="fa306-417">真の配色。</span><span class="sxs-lookup"><span data-stu-id="fa306-417">The true-color scheme.</span></span> |

## <a name="method-configurationkey"></a><span data-ttu-id="fa306-418">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="fa306-418">Method configurationKey</span></span>

<span data-ttu-id="fa306-419">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-419">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="fa306-420">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="fa306-420">Parameters - configurationKey</span></span>

<span data-ttu-id="fa306-421">値</span><span class="sxs-lookup"><span data-stu-id="fa306-421">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="fa306-422">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="fa306-422">Return Value - configurationKey</span></span>

<span data-ttu-id="fa306-423">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="fa306-423">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="fa306-424">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="fa306-424">Remarks - configurationKey</span></span>

<span data-ttu-id="fa306-425">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa306-425">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="fa306-426">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="fa306-426">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-controltype"></a><span data-ttu-id="fa306-427">メソッド controlType</span><span class="sxs-lookup"><span data-stu-id="fa306-427">Method controlType</span></span>

```xpp
public ReportFieldType controlType()
```

### <a name="return-value---controltype"></a><span data-ttu-id="fa306-428">戻り値 - controlType</span><span class="sxs-lookup"><span data-stu-id="fa306-428">Return Value - controlType</span></span>

## <a name="method-cssclass"></a><span data-ttu-id="fa306-429">メソッド cssClass</span><span class="sxs-lookup"><span data-stu-id="fa306-429">Method cssClass</span></span>

```xpp
public str cssClass([str value])
```

### <a name="parameters---cssclass"></a><span data-ttu-id="fa306-430">パラメーター - cssClass</span><span class="sxs-lookup"><span data-stu-id="fa306-430">Parameters - cssClass</span></span>

<span data-ttu-id="fa306-431">値</span><span class="sxs-lookup"><span data-stu-id="fa306-431">value</span></span>  

### <a name="return-value---cssclass"></a><span data-ttu-id="fa306-432">戻り値 - cssClass</span><span class="sxs-lookup"><span data-stu-id="fa306-432">Return Value - cssClass</span></span>

## <a name="method-datafield"></a><span data-ttu-id="fa306-433">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="fa306-433">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="fa306-434">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="fa306-434">Parameters - dataField</span></span>

<span data-ttu-id="fa306-435">値</span><span class="sxs-lookup"><span data-stu-id="fa306-435">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="fa306-436">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="fa306-436">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="fa306-437">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="fa306-437">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="fa306-438">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="fa306-438">Parameters - dataMethod</span></span>

<span data-ttu-id="fa306-439">値</span><span class="sxs-lookup"><span data-stu-id="fa306-439">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="fa306-440">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="fa306-440">Return Value - dataMethod</span></span>

## <a name="method-delete"></a><span data-ttu-id="fa306-441">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="fa306-441">Method delete</span></span>

```xpp
public int delete()
```

### <a name="return-value---delete"></a><span data-ttu-id="fa306-442">戻り値 - delete</span><span class="sxs-lookup"><span data-stu-id="fa306-442">Return Value - delete</span></span>

## <a name="method-effectivefont"></a><span data-ttu-id="fa306-443">メソッド effectiveFont</span><span class="sxs-lookup"><span data-stu-id="fa306-443">Method effectiveFont</span></span>

```xpp
public str effectiveFont()
```

### <a name="return-value---effectivefont"></a><span data-ttu-id="fa306-444">戻り値 - effectiveFont</span><span class="sxs-lookup"><span data-stu-id="fa306-444">Return Value - effectiveFont</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="fa306-445">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="fa306-445">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="fa306-446">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="fa306-446">Parameters - extendedDataType</span></span>

<span data-ttu-id="fa306-447">値</span><span class="sxs-lookup"><span data-stu-id="fa306-447">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="fa306-448">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="fa306-448">Return Value - extendedDataType</span></span>

## <a name="method-font"></a><span data-ttu-id="fa306-449">メソッド font</span><span class="sxs-lookup"><span data-stu-id="fa306-449">Method font</span></span>

<span data-ttu-id="fa306-450">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-450">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="fa306-451">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="fa306-451">Parameters - font</span></span>

<span data-ttu-id="fa306-452">値</span><span class="sxs-lookup"><span data-stu-id="fa306-452">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="fa306-453">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="fa306-453">Return Value - font</span></span>

<span data-ttu-id="fa306-454">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="fa306-454">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontinfoprinter"></a><span data-ttu-id="fa306-455">メソッド fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="fa306-455">Method fontInfoPrinter</span></span>

```xpp
public str fontInfoPrinter()
```

### <a name="return-value---fontinfoprinter"></a><span data-ttu-id="fa306-456">戻り値 - fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="fa306-456">Return Value - fontInfoPrinter</span></span>

## <a name="method-fontinfoprinterascent"></a><span data-ttu-id="fa306-457">メソッド fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="fa306-457">Method fontInfoPrinterAscent</span></span>

```xpp
public int fontInfoPrinterAscent()
```

### <a name="return-value---fontinfoprinterascent"></a><span data-ttu-id="fa306-458">戻り値 - fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="fa306-458">Return Value - fontInfoPrinterAscent</span></span>

## <a name="method-fontinfoprinterdescent"></a><span data-ttu-id="fa306-459">メソッド fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="fa306-459">Method fontInfoPrinterDescent</span></span>

```xpp
public int fontInfoPrinterDescent()
```

### <a name="return-value---fontinfoprinterdescent"></a><span data-ttu-id="fa306-460">戻り値 - fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="fa306-460">Return Value - fontInfoPrinterDescent</span></span>

## <a name="method-fontinfoprinterextlead"></a><span data-ttu-id="fa306-461">メソッド fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="fa306-461">Method fontInfoPrinterExtLead</span></span>

```xpp
public int fontInfoPrinterExtLead()
```

### <a name="return-value---fontinfoprinterextlead"></a><span data-ttu-id="fa306-462">戻り値 - fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="fa306-462">Return Value - fontInfoPrinterExtLead</span></span>

## <a name="method-fontinfoprinterheight"></a><span data-ttu-id="fa306-463">メソッド fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="fa306-463">Method fontInfoPrinterHeight</span></span>

```xpp
public int fontInfoPrinterHeight()
```

### <a name="return-value---fontinfoprinterheight"></a><span data-ttu-id="fa306-464">戻り値 - fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="fa306-464">Return Value - fontInfoPrinterHeight</span></span>

## <a name="method-fontinfoprinterintlead"></a><span data-ttu-id="fa306-465">メソッド fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="fa306-465">Method fontInfoPrinterIntLead</span></span>

```xpp
public int fontInfoPrinterIntLead()
```

### <a name="return-value---fontinfoprinterintlead"></a><span data-ttu-id="fa306-466">戻り値 - fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="fa306-466">Return Value - fontInfoPrinterIntLead</span></span>

## <a name="method-fontinfoscreen"></a><span data-ttu-id="fa306-467">メソッド fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="fa306-467">Method fontInfoScreen</span></span>

```xpp
public str fontInfoScreen()
```

### <a name="return-value---fontinfoscreen"></a><span data-ttu-id="fa306-468">戻り値 - fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="fa306-468">Return Value - fontInfoScreen</span></span>

## <a name="method-fontinfoscreenascent"></a><span data-ttu-id="fa306-469">メソッド fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="fa306-469">Method fontInfoScreenAscent</span></span>

```xpp
public int fontInfoScreenAscent()
```

### <a name="return-value---fontinfoscreenascent"></a><span data-ttu-id="fa306-470">戻り値 - fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="fa306-470">Return Value - fontInfoScreenAscent</span></span>

## <a name="method-fontinfoscreendescent"></a><span data-ttu-id="fa306-471">メソッド fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="fa306-471">Method fontInfoScreenDescent</span></span>

```xpp
public int fontInfoScreenDescent()
```

### <a name="return-value---fontinfoscreendescent"></a><span data-ttu-id="fa306-472">戻り値 - fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="fa306-472">Return Value - fontInfoScreenDescent</span></span>

## <a name="method-fontinfoscreenextlead"></a><span data-ttu-id="fa306-473">メソッド fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="fa306-473">Method fontInfoScreenExtLead</span></span>

```xpp
public int fontInfoScreenExtLead()
```

### <a name="return-value---fontinfoscreenextlead"></a><span data-ttu-id="fa306-474">戻り値 - fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="fa306-474">Return Value - fontInfoScreenExtLead</span></span>

## <a name="method-fontinfoscreenheight"></a><span data-ttu-id="fa306-475">メソッド fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="fa306-475">Method fontInfoScreenHeight</span></span>

```xpp
public int fontInfoScreenHeight()
```

### <a name="return-value---fontinfoscreenheight"></a><span data-ttu-id="fa306-476">戻り値 - fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="fa306-476">Return Value - fontInfoScreenHeight</span></span>

## <a name="method-fontinfoscreenintlead"></a><span data-ttu-id="fa306-477">メソッド fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="fa306-477">Method fontInfoScreenIntLead</span></span>

```xpp
public int fontInfoScreenIntLead()
```

### <a name="return-value---fontinfoscreenintlead"></a><span data-ttu-id="fa306-478">戻り値 - fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="fa306-478">Return Value - fontInfoScreenIntLead</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="fa306-479">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="fa306-479">Method fontSize</span></span>

<span data-ttu-id="fa306-480">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-480">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="fa306-481">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="fa306-481">Parameters - fontSize</span></span>

<span data-ttu-id="fa306-482">値</span><span class="sxs-lookup"><span data-stu-id="fa306-482">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="fa306-483">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="fa306-483">Return Value - fontSize</span></span>

<span data-ttu-id="fa306-484">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="fa306-484">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="fa306-485">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="fa306-485">Method foregroundColor</span></span>

<span data-ttu-id="fa306-486">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-486">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="fa306-487">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="fa306-487">Parameters - foregroundColor</span></span>

<span data-ttu-id="fa306-488">値</span><span class="sxs-lookup"><span data-stu-id="fa306-488">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="fa306-489">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="fa306-489">Return Value - foregroundColor</span></span>

<span data-ttu-id="fa306-490">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="fa306-490">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="fa306-491">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="fa306-491">Remarks - foregroundColor</span></span>

<span data-ttu-id="fa306-492">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fa306-492">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="fa306-493">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fa306-493">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="fa306-494">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="fa306-494">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="fa306-495">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="fa306-495">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="fa306-496">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="fa306-496">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="fa306-497">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="fa306-497">The maximum value for a single byte is 255.</span></span>

## <a name="method-height100mm"></a><span data-ttu-id="fa306-498">メソッド height100mm</span><span class="sxs-lookup"><span data-stu-id="fa306-498">Method height100mm</span></span>

```xpp
public int height100mm([int heightExclBorder])
```

### <a name="parameters---height100mm"></a><span data-ttu-id="fa306-499">パラメーター - height100mm</span><span class="sxs-lookup"><span data-stu-id="fa306-499">Parameters - height100mm</span></span>

<span data-ttu-id="fa306-500">heightExclBorder</span><span class="sxs-lookup"><span data-stu-id="fa306-500">heightExclBorder</span></span>  

### <a name="return-value---height100mm"></a><span data-ttu-id="fa306-501">戻り値 - height100mm</span><span class="sxs-lookup"><span data-stu-id="fa306-501">Return Value - height100mm</span></span>

## <a name="method-height100mminclborder"></a><span data-ttu-id="fa306-502">メソッド height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fa306-502">Method height100mmInclBorder</span></span>

```xpp
public int height100mmInclBorder([int heightInclBorder])
```

### <a name="parameters---height100mminclborder"></a><span data-ttu-id="fa306-503">パラメーター - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fa306-503">Parameters - height100mmInclBorder</span></span>

<span data-ttu-id="fa306-504">heightInclBorder</span><span class="sxs-lookup"><span data-stu-id="fa306-504">heightInclBorder</span></span>  

### <a name="return-value---height100mminclborder"></a><span data-ttu-id="fa306-505">戻り値 - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fa306-505">Return Value - height100mmInclBorder</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="fa306-506">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="fa306-506">Method heightMode</span></span>

<span data-ttu-id="fa306-507">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-507">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="fa306-508">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="fa306-508">Parameters - heightMode</span></span>

<span data-ttu-id="fa306-509">値</span><span class="sxs-lookup"><span data-stu-id="fa306-509">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="fa306-510">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="fa306-510">Return Value - heightMode</span></span>

<span data-ttu-id="fa306-511">計算モード。</span><span class="sxs-lookup"><span data-stu-id="fa306-511">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="fa306-512">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="fa306-512">Remarks - heightMode</span></span>

<span data-ttu-id="fa306-513">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="fa306-513">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="fa306-514">モード。</span><span class="sxs-lookup"><span data-stu-id="fa306-514">Mode.</span></span>          | <span data-ttu-id="fa306-515">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="fa306-515">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa306-516">正確。</span><span class="sxs-lookup"><span data-stu-id="fa306-516">Exact.</span></span>         | <span data-ttu-id="fa306-517">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa306-517">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="fa306-518">自動。</span><span class="sxs-lookup"><span data-stu-id="fa306-518">Auto.</span></span>          | <span data-ttu-id="fa306-519">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="fa306-519">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="fa306-520">列の高さ</span><span class="sxs-lookup"><span data-stu-id="fa306-520">Column height.</span></span> | <span data-ttu-id="fa306-521">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="fa306-521">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="fa306-522">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="fa306-522">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightofwordwrappedstring100mm"></a><span data-ttu-id="fa306-523">メソッド heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="fa306-523">Method heightOfWordWrappedString100mm</span></span>

```xpp
public int heightOfWordWrappedString100mm(str string)
```

### <a name="parameters---heightofwordwrappedstring100mm"></a><span data-ttu-id="fa306-524">パラメーター - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="fa306-524">Parameters - heightOfWordWrappedString100mm</span></span>

<span data-ttu-id="fa306-525">文字列</span><span class="sxs-lookup"><span data-stu-id="fa306-525">string</span></span>  

### <a name="return-value---heightofwordwrappedstring100mm"></a><span data-ttu-id="fa306-526">戻り値 - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="fa306-526">Return Value - heightOfWordWrappedString100mm</span></span>

## <a name="method-heightstr"></a><span data-ttu-id="fa306-527">メソッド heightStr</span><span class="sxs-lookup"><span data-stu-id="fa306-527">Method heightStr</span></span>

```xpp
public str heightStr([str value])
```

### <a name="parameters---heightstr"></a><span data-ttu-id="fa306-528">パラメーター - heightStr</span><span class="sxs-lookup"><span data-stu-id="fa306-528">Parameters - heightStr</span></span>

<span data-ttu-id="fa306-529">値</span><span class="sxs-lookup"><span data-stu-id="fa306-529">value</span></span>  

### <a name="return-value---heightstr"></a><span data-ttu-id="fa306-530">戻り値 - heightStr</span><span class="sxs-lookup"><span data-stu-id="fa306-530">Return Value - heightStr</span></span>

## <a name="method-heightunit"></a><span data-ttu-id="fa306-531">メソッド heightUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-531">Method heightUnit</span></span>

```xpp
public Units heightUnit([Units value])
```

### <a name="parameters---heightunit"></a><span data-ttu-id="fa306-532">パラメーター - heightUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-532">Parameters - heightUnit</span></span>

<span data-ttu-id="fa306-533">値</span><span class="sxs-lookup"><span data-stu-id="fa306-533">value</span></span>  

### <a name="return-value---heightunit"></a><span data-ttu-id="fa306-534">戻り値 - heightUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-534">Return Value - heightUnit</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="fa306-535">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="fa306-535">Method heightValue</span></span>

<span data-ttu-id="fa306-536">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-536">Gets or sets the height of the control.</span></span>

```xpp
public Real heightValue([Real value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="fa306-537">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="fa306-537">Parameters - heightValue</span></span>

<span data-ttu-id="fa306-538">値</span><span class="sxs-lookup"><span data-stu-id="fa306-538">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="fa306-539">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="fa306-539">Return Value - heightValue</span></span>

<span data-ttu-id="fa306-540">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="fa306-540">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="fa306-541">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="fa306-541">Remarks - heightValue</span></span>

<span data-ttu-id="fa306-542">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="fa306-542">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-italic"></a><span data-ttu-id="fa306-543">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="fa306-543">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="fa306-544">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="fa306-544">Parameters - italic</span></span>

<span data-ttu-id="fa306-545">値</span><span class="sxs-lookup"><span data-stu-id="fa306-545">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="fa306-546">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="fa306-546">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="fa306-547">メソッド label</span><span class="sxs-lookup"><span data-stu-id="fa306-547">Method label</span></span>

<span data-ttu-id="fa306-548">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-548">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="fa306-549">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="fa306-549">Parameters - label</span></span>

<span data-ttu-id="fa306-550">値</span><span class="sxs-lookup"><span data-stu-id="fa306-550">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="fa306-551">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="fa306-551">Return Value - label</span></span>

<span data-ttu-id="fa306-552">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="fa306-552">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="fa306-553">備考 - label</span><span class="sxs-lookup"><span data-stu-id="fa306-553">Remarks - label</span></span>

<span data-ttu-id="fa306-554">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-554">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="fa306-555">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="fa306-555">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="fa306-556">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="fa306-556">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="fa306-557">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="fa306-557">Parameters - labelBold</span></span>

<span data-ttu-id="fa306-558">値</span><span class="sxs-lookup"><span data-stu-id="fa306-558">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="fa306-559">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="fa306-559">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="fa306-560">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="fa306-560">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="fa306-561">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="fa306-561">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="fa306-562">値</span><span class="sxs-lookup"><span data-stu-id="fa306-562">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="fa306-563">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="fa306-563">Return Value - labelCharacterSet</span></span>

## <a name="method-labelcssclass"></a><span data-ttu-id="fa306-564">メソッド labelCssClass</span><span class="sxs-lookup"><span data-stu-id="fa306-564">Method labelCssClass</span></span>

```xpp
public str labelCssClass([str value])
```

### <a name="parameters---labelcssclass"></a><span data-ttu-id="fa306-565">パラメーター - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="fa306-565">Parameters - labelCssClass</span></span>

<span data-ttu-id="fa306-566">値</span><span class="sxs-lookup"><span data-stu-id="fa306-566">value</span></span>  

### <a name="return-value---labelcssclass"></a><span data-ttu-id="fa306-567">戻り値 - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="fa306-567">Return Value - labelCssClass</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="fa306-568">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="fa306-568">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="fa306-569">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="fa306-569">Parameters - labelFont</span></span>

<span data-ttu-id="fa306-570">値</span><span class="sxs-lookup"><span data-stu-id="fa306-570">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="fa306-571">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="fa306-571">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="fa306-572">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="fa306-572">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="fa306-573">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="fa306-573">Parameters - labelFontSize</span></span>

<span data-ttu-id="fa306-574">値</span><span class="sxs-lookup"><span data-stu-id="fa306-574">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="fa306-575">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="fa306-575">Return Value - labelFontSize</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="fa306-576">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="fa306-576">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="fa306-577">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="fa306-577">Parameters - labelItalic</span></span>

<span data-ttu-id="fa306-578">値</span><span class="sxs-lookup"><span data-stu-id="fa306-578">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="fa306-579">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="fa306-579">Return Value - labelItalic</span></span>

## <a name="method-labellinebelow"></a><span data-ttu-id="fa306-580">メソッド labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="fa306-580">Method labelLineBelow</span></span>

```xpp
public LineType labelLineBelow([LineType value])
```

### <a name="parameters---labellinebelow"></a><span data-ttu-id="fa306-581">パラメーター - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="fa306-581">Parameters - labelLineBelow</span></span>

<span data-ttu-id="fa306-582">値</span><span class="sxs-lookup"><span data-stu-id="fa306-582">value</span></span>  

### <a name="return-value---labellinebelow"></a><span data-ttu-id="fa306-583">戻り値 - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="fa306-583">Return Value - labelLineBelow</span></span>

## <a name="method-labellinethickness"></a><span data-ttu-id="fa306-584">メソッド labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="fa306-584">Method labelLineThickness</span></span>

```xpp
public LineThickness labelLineThickness([LineThickness value])
```

### <a name="parameters---labellinethickness"></a><span data-ttu-id="fa306-585">パラメーター - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="fa306-585">Parameters - labelLineThickness</span></span>

<span data-ttu-id="fa306-586">値</span><span class="sxs-lookup"><span data-stu-id="fa306-586">value</span></span>  

### <a name="return-value---labellinethickness"></a><span data-ttu-id="fa306-587">戻り値 - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="fa306-587">Return Value - labelLineThickness</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="fa306-588">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="fa306-588">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="fa306-589">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="fa306-589">Parameters - labelPosition</span></span>

<span data-ttu-id="fa306-590">値</span><span class="sxs-lookup"><span data-stu-id="fa306-590">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="fa306-591">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="fa306-591">Return Value - labelPosition</span></span>

## <a name="method-labeltableader"></a><span data-ttu-id="fa306-592">メソッド labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="fa306-592">Method labelTabLeader</span></span>

```xpp
public int labelTabLeader([int value])
```

### <a name="parameters---labeltableader"></a><span data-ttu-id="fa306-593">パラメーター - labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="fa306-593">Parameters - labelTabLeader</span></span>

<span data-ttu-id="fa306-594">値</span><span class="sxs-lookup"><span data-stu-id="fa306-594">value</span></span>  

### <a name="return-value---labeltableader"></a><span data-ttu-id="fa306-595">戻り値 - labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="fa306-595">Return Value - labelTabLeader</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="fa306-596">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="fa306-596">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="fa306-597">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="fa306-597">Parameters - labelUnderline</span></span>

<span data-ttu-id="fa306-598">値</span><span class="sxs-lookup"><span data-stu-id="fa306-598">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="fa306-599">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="fa306-599">Return Value - labelUnderline</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="fa306-600">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="fa306-600">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="fa306-601">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="fa306-601">Parameters - labelWidthMode</span></span>

<span data-ttu-id="fa306-602">値</span><span class="sxs-lookup"><span data-stu-id="fa306-602">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="fa306-603">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="fa306-603">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthstr"></a><span data-ttu-id="fa306-604">メソッド labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="fa306-604">Method labelWidthStr</span></span>

```xpp
public str labelWidthStr([str value])
```

### <a name="parameters---labelwidthstr"></a><span data-ttu-id="fa306-605">パラメーター - labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="fa306-605">Parameters - labelWidthStr</span></span>

<span data-ttu-id="fa306-606">値</span><span class="sxs-lookup"><span data-stu-id="fa306-606">value</span></span>  

### <a name="return-value---labelwidthstr"></a><span data-ttu-id="fa306-607">戻り値 - labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="fa306-607">Return Value - labelWidthStr</span></span>

## <a name="method-labelwidthunit"></a><span data-ttu-id="fa306-608">メソッド labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-608">Method labelWidthUnit</span></span>

```xpp
public Units labelWidthUnit([Units value])
```

### <a name="parameters---labelwidthunit"></a><span data-ttu-id="fa306-609">パラメーター - labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-609">Parameters - labelWidthUnit</span></span>

<span data-ttu-id="fa306-610">値</span><span class="sxs-lookup"><span data-stu-id="fa306-610">value</span></span>  

### <a name="return-value---labelwidthunit"></a><span data-ttu-id="fa306-611">戻り値 - labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-611">Return Value - labelWidthUnit</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="fa306-612">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="fa306-612">Method labelWidthValue</span></span>

```xpp
public Real labelWidthValue([Real value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="fa306-613">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="fa306-613">Parameters - labelWidthValue</span></span>

<span data-ttu-id="fa306-614">値</span><span class="sxs-lookup"><span data-stu-id="fa306-614">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="fa306-615">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="fa306-615">Return Value - labelWidthValue</span></span>

## <a name="method-left100mm"></a><span data-ttu-id="fa306-616">メソッド left100mm</span><span class="sxs-lookup"><span data-stu-id="fa306-616">Method left100mm</span></span>

```xpp
public int left100mm([int leftExclBorder])
```

### <a name="parameters---left100mm"></a><span data-ttu-id="fa306-617">パラメーター - left100mm</span><span class="sxs-lookup"><span data-stu-id="fa306-617">Parameters - left100mm</span></span>

<span data-ttu-id="fa306-618">leftExclBorder</span><span class="sxs-lookup"><span data-stu-id="fa306-618">leftExclBorder</span></span>  

### <a name="return-value---left100mm"></a><span data-ttu-id="fa306-619">戻り値 - left100mm</span><span class="sxs-lookup"><span data-stu-id="fa306-619">Return Value - left100mm</span></span>

## <a name="method-left100mminclborder"></a><span data-ttu-id="fa306-620">メソッド left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fa306-620">Method left100mmInclBorder</span></span>

```xpp
public int left100mmInclBorder([int leftInclBorder])
```

### <a name="parameters---left100mminclborder"></a><span data-ttu-id="fa306-621">パラメーター - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fa306-621">Parameters - left100mmInclBorder</span></span>

<span data-ttu-id="fa306-622">leftInclBorder</span><span class="sxs-lookup"><span data-stu-id="fa306-622">leftInclBorder</span></span>  

### <a name="return-value---left100mminclborder"></a><span data-ttu-id="fa306-623">戻り値 - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fa306-623">Return Value - left100mmInclBorder</span></span>

## <a name="method-leftmarginanframe"></a><span data-ttu-id="fa306-624">メソッド leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="fa306-624">Method leftMarginAnFrame</span></span>

```xpp
public int leftMarginAnFrame()
```

### <a name="return-value---leftmarginanframe"></a><span data-ttu-id="fa306-625">戻り値 - leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="fa306-625">Return Value - leftMarginAnFrame</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="fa306-626">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="fa306-626">Method leftMarginMode</span></span>

```xpp
public int leftMarginMode([int value])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="fa306-627">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="fa306-627">Parameters - leftMarginMode</span></span>

<span data-ttu-id="fa306-628">値</span><span class="sxs-lookup"><span data-stu-id="fa306-628">value</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="fa306-629">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="fa306-629">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginstr"></a><span data-ttu-id="fa306-630">メソッド leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="fa306-630">Method leftMarginStr</span></span>

```xpp
public str leftMarginStr([str value])
```

### <a name="parameters---leftmarginstr"></a><span data-ttu-id="fa306-631">パラメーター - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="fa306-631">Parameters - leftMarginStr</span></span>

<span data-ttu-id="fa306-632">値</span><span class="sxs-lookup"><span data-stu-id="fa306-632">value</span></span>  

### <a name="return-value---leftmarginstr"></a><span data-ttu-id="fa306-633">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="fa306-633">Return Value - leftMarginStr</span></span>

## <a name="method-leftmarginunit"></a><span data-ttu-id="fa306-634">メソッド leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-634">Method leftMarginUnit</span></span>

```xpp
public Units leftMarginUnit([Units value])
```

### <a name="parameters---leftmarginunit"></a><span data-ttu-id="fa306-635">パラメーター - leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-635">Parameters - leftMarginUnit</span></span>

<span data-ttu-id="fa306-636">値</span><span class="sxs-lookup"><span data-stu-id="fa306-636">value</span></span>  

### <a name="return-value---leftmarginunit"></a><span data-ttu-id="fa306-637">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="fa306-637">Return Value - leftMarginUnit</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="fa306-638">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="fa306-638">Method leftMarginValue</span></span>

```xpp
public Real leftMarginValue([Real value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="fa306-639">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="fa306-639">Parameters - leftMarginValue</span></span>

<span data-ttu-id="fa306-640">値</span><span class="sxs-lookup"><span data-stu-id="fa306-640">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="fa306-641">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="fa306-641">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="fa306-642">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="fa306-642">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="fa306-643">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="fa306-643">Parameters - leftMode</span></span>

<span data-ttu-id="fa306-644">値</span><span class="sxs-lookup"><span data-stu-id="fa306-644">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="fa306-645">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="fa306-645">Return Value - leftMode</span></span>

## <a name="method-leftstr"></a><span data-ttu-id="fa306-646">メソッド leftStr</span><span class="sxs-lookup"><span data-stu-id="fa306-646">Method leftStr</span></span>

```xpp
public str leftStr([str value])
```

### <a name="parameters---leftstr"></a><span data-ttu-id="fa306-647">パラメーター - leftStr</span><span class="sxs-lookup"><span data-stu-id="fa306-647">Parameters - leftStr</span></span>

<span data-ttu-id="fa306-648">値</span><span class="sxs-lookup"><span data-stu-id="fa306-648">value</span></span>  

### <a name="return-value---leftstr"></a><span data-ttu-id="fa306-649">戻り値 - leftStr</span><span class="sxs-lookup"><span data-stu-id="fa306-649">Return Value - leftStr</span></span>

## <a name="method-leftunit"></a><span data-ttu-id="fa306-650">メソッド leftUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-650">Method leftUnit</span></span>

```xpp
public Units leftUnit([Units value])
```

### <a name="parameters---leftunit"></a><span data-ttu-id="fa306-651">パラメーター - leftUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-651">Parameters - leftUnit</span></span>

<span data-ttu-id="fa306-652">値</span><span class="sxs-lookup"><span data-stu-id="fa306-652">value</span></span>  

### <a name="return-value---leftunit"></a><span data-ttu-id="fa306-653">戻り値 - leftUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-653">Return Value - leftUnit</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="fa306-654">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="fa306-654">Method leftValue</span></span>

```xpp
public Real leftValue([Real value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="fa306-655">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="fa306-655">Parameters - leftValue</span></span>

<span data-ttu-id="fa306-656">値</span><span class="sxs-lookup"><span data-stu-id="fa306-656">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="fa306-657">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="fa306-657">Return Value - leftValue</span></span>

## <a name="method-lineabove"></a><span data-ttu-id="fa306-658">メソッド lineAbove</span><span class="sxs-lookup"><span data-stu-id="fa306-658">Method lineAbove</span></span>

```xpp
public LineType lineAbove([LineType value])
```

### <a name="parameters---lineabove"></a><span data-ttu-id="fa306-659">パラメーター - lineAbove</span><span class="sxs-lookup"><span data-stu-id="fa306-659">Parameters - lineAbove</span></span>

<span data-ttu-id="fa306-660">値</span><span class="sxs-lookup"><span data-stu-id="fa306-660">value</span></span>  

### <a name="return-value---lineabove"></a><span data-ttu-id="fa306-661">戻り値 - lineAbove</span><span class="sxs-lookup"><span data-stu-id="fa306-661">Return Value - lineAbove</span></span>

## <a name="method-linebelow"></a><span data-ttu-id="fa306-662">メソッド lineBelow</span><span class="sxs-lookup"><span data-stu-id="fa306-662">Method lineBelow</span></span>

```xpp
public LineType lineBelow([LineType value])
```

### <a name="parameters---linebelow"></a><span data-ttu-id="fa306-663">パラメーター - lineBelow</span><span class="sxs-lookup"><span data-stu-id="fa306-663">Parameters - lineBelow</span></span>

<span data-ttu-id="fa306-664">値</span><span class="sxs-lookup"><span data-stu-id="fa306-664">value</span></span>  

### <a name="return-value---linebelow"></a><span data-ttu-id="fa306-665">戻り値 - lineBelow</span><span class="sxs-lookup"><span data-stu-id="fa306-665">Return Value - lineBelow</span></span>

## <a name="method-lineleft"></a><span data-ttu-id="fa306-666">メソッド lineLeft</span><span class="sxs-lookup"><span data-stu-id="fa306-666">Method lineLeft</span></span>

<span data-ttu-id="fa306-667">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-667">Gets or sets the type of line that is used as the left border of a section.</span></span>

```xpp
public LineType lineLeft([LineType value])
```

### <a name="parameters---lineleft"></a><span data-ttu-id="fa306-668">パラメーター - lineLeft</span><span class="sxs-lookup"><span data-stu-id="fa306-668">Parameters - lineLeft</span></span>

<span data-ttu-id="fa306-669">値</span><span class="sxs-lookup"><span data-stu-id="fa306-669">value</span></span>  

### <a name="return-value---lineleft"></a><span data-ttu-id="fa306-670">戻り値 - lineLeft</span><span class="sxs-lookup"><span data-stu-id="fa306-670">Return Value - lineLeft</span></span>

<span data-ttu-id="fa306-671">左境界線として使用される線のタイプ。</span><span class="sxs-lookup"><span data-stu-id="fa306-671">The type of line that is used as the left border.</span></span>

## <a name="method-lineright"></a><span data-ttu-id="fa306-672">メソッド lineRight</span><span class="sxs-lookup"><span data-stu-id="fa306-672">Method lineRight</span></span>

```xpp
public LineType lineRight([LineType value])
```

### <a name="parameters---lineright"></a><span data-ttu-id="fa306-673">パラメーター - lineRight</span><span class="sxs-lookup"><span data-stu-id="fa306-673">Parameters - lineRight</span></span>

<span data-ttu-id="fa306-674">値</span><span class="sxs-lookup"><span data-stu-id="fa306-674">value</span></span>  

### <a name="return-value---lineright"></a><span data-ttu-id="fa306-675">戻り値 - lineRight</span><span class="sxs-lookup"><span data-stu-id="fa306-675">Return Value - lineRight</span></span>

## <a name="method-menuitemlabel"></a><span data-ttu-id="fa306-676">メソッド menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="fa306-676">Method menuItemLabel</span></span>

```xpp
public str menuItemLabel([str value])
```

### <a name="parameters---menuitemlabel"></a><span data-ttu-id="fa306-677">パラメーター - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="fa306-677">Parameters - menuItemLabel</span></span>

<span data-ttu-id="fa306-678">値</span><span class="sxs-lookup"><span data-stu-id="fa306-678">value</span></span>  

### <a name="return-value---menuitemlabel"></a><span data-ttu-id="fa306-679">戻り値 - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="fa306-679">Return Value - menuItemLabel</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="fa306-680">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="fa306-680">Method menuItemName</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="fa306-681">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="fa306-681">Parameters - menuItemName</span></span>

<span data-ttu-id="fa306-682">値</span><span class="sxs-lookup"><span data-stu-id="fa306-682">value</span></span>  

### <a name="return-value---menuitemname"></a><span data-ttu-id="fa306-683">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="fa306-683">Return Value - menuItemName</span></span>

## <a name="method-menuitemtype"></a><span data-ttu-id="fa306-684">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="fa306-684">Method menuItemType</span></span>

```xpp
public MenuItemType menuItemType([MenuItemType value])
```

### <a name="parameters---menuitemtype"></a><span data-ttu-id="fa306-685">パラメーター - menuItemType</span><span class="sxs-lookup"><span data-stu-id="fa306-685">Parameters - menuItemType</span></span>

<span data-ttu-id="fa306-686">値</span><span class="sxs-lookup"><span data-stu-id="fa306-686">value</span></span>  

### <a name="return-value---menuitemtype"></a><span data-ttu-id="fa306-687">戻り値 - menuItemType</span><span class="sxs-lookup"><span data-stu-id="fa306-687">Return Value - menuItemType</span></span>

## <a name="method-modelfieldname"></a><span data-ttu-id="fa306-688">メソッド modelFieldName</span><span class="sxs-lookup"><span data-stu-id="fa306-688">Method modelFieldName</span></span>

```xpp
public str modelFieldName([str value])
```

### <a name="parameters---modelfieldname"></a><span data-ttu-id="fa306-689">パラメーター - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="fa306-689">Parameters - modelFieldName</span></span>

<span data-ttu-id="fa306-690">値</span><span class="sxs-lookup"><span data-stu-id="fa306-690">value</span></span>  

### <a name="return-value---modelfieldname"></a><span data-ttu-id="fa306-691">戻り値 - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="fa306-691">Return Value - modelFieldName</span></span>

## <a name="method-name"></a><span data-ttu-id="fa306-692">メソッド名</span><span class="sxs-lookup"><span data-stu-id="fa306-692">Method name</span></span>

<span data-ttu-id="fa306-693">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-693">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="fa306-694">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="fa306-694">Parameters - name</span></span>

<span data-ttu-id="fa306-695">値</span><span class="sxs-lookup"><span data-stu-id="fa306-695">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="fa306-696">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="fa306-696">Return Value - name</span></span>

<span data-ttu-id="fa306-697">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="fa306-697">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="fa306-698">備考 - name</span><span class="sxs-lookup"><span data-stu-id="fa306-698">Remarks - name</span></span>

<span data-ttu-id="fa306-699">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa306-699">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="fa306-700">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="fa306-700">Begins with a letter.</span></span>
-   <span data-ttu-id="fa306-701">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="fa306-701">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="fa306-702">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="fa306-702">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="fa306-703">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="fa306-703">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="fa306-704">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="fa306-704">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-numberoflines"></a><span data-ttu-id="fa306-705">メソッド numberOfLines</span><span class="sxs-lookup"><span data-stu-id="fa306-705">Method numberOfLines</span></span>

```xpp
public int numberOfLines(int height100mm)
```

### <a name="parameters---numberoflines"></a><span data-ttu-id="fa306-706">パラメーター - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="fa306-706">Parameters - numberOfLines</span></span>

<span data-ttu-id="fa306-707">height100mm</span><span class="sxs-lookup"><span data-stu-id="fa306-707">height100mm</span></span>  

### <a name="return-value---numberoflines"></a><span data-ttu-id="fa306-708">戻り値 - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="fa306-708">Return Value - numberOfLines</span></span>

## <a name="method-position"></a><span data-ttu-id="fa306-709">メソッドの位置</span><span class="sxs-lookup"><span data-stu-id="fa306-709">Method position</span></span>

```xpp
public int position([int value])
```

### <a name="parameters---position"></a><span data-ttu-id="fa306-710">パラメーター - position</span><span class="sxs-lookup"><span data-stu-id="fa306-710">Parameters - position</span></span>

<span data-ttu-id="fa306-711">値</span><span class="sxs-lookup"><span data-stu-id="fa306-711">value</span></span>  

### <a name="return-value---position"></a><span data-ttu-id="fa306-712">戻り値 - position</span><span class="sxs-lookup"><span data-stu-id="fa306-712">Return Value - position</span></span>

## <a name="method-previewinfo"></a><span data-ttu-id="fa306-713">メソッド previewInfo</span><span class="sxs-lookup"><span data-stu-id="fa306-713">Method previewInfo</span></span>

```xpp
public str previewInfo(str string)
```

### <a name="parameters---previewinfo"></a><span data-ttu-id="fa306-714">パラメーター - previewInfo</span><span class="sxs-lookup"><span data-stu-id="fa306-714">Parameters - previewInfo</span></span>

<span data-ttu-id="fa306-715">文字列</span><span class="sxs-lookup"><span data-stu-id="fa306-715">string</span></span>  

### <a name="return-value---previewinfo"></a><span data-ttu-id="fa306-716">戻り値 - previewInfo</span><span class="sxs-lookup"><span data-stu-id="fa306-716">Return Value - previewInfo</span></span>

## <a name="method-previewxcompensation100mm"></a><span data-ttu-id="fa306-717">メソッド previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="fa306-717">Method previewXCompensation100mm</span></span>

```xpp
public int previewXCompensation100mm(str string)
```

### <a name="parameters---previewxcompensation100mm"></a><span data-ttu-id="fa306-718">パラメーター - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="fa306-718">Parameters - previewXCompensation100mm</span></span>

<span data-ttu-id="fa306-719">文字列</span><span class="sxs-lookup"><span data-stu-id="fa306-719">string</span></span>  

### <a name="return-value---previewxcompensation100mm"></a><span data-ttu-id="fa306-720">戻り値 - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="fa306-720">Return Value - previewXCompensation100mm</span></span>

## <a name="method-right100mm"></a><span data-ttu-id="fa306-721">メソッド right100mm</span><span class="sxs-lookup"><span data-stu-id="fa306-721">Method right100mm</span></span>

```xpp
public int right100mm()
```

### <a name="return-value---right100mm"></a><span data-ttu-id="fa306-722">戻り値 - right100mm</span><span class="sxs-lookup"><span data-stu-id="fa306-722">Return Value - right100mm</span></span>

## <a name="method-right100mminclborder"></a><span data-ttu-id="fa306-723">メソッド right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fa306-723">Method right100mmInclBorder</span></span>

```xpp
public int right100mmInclBorder()
```

### <a name="return-value---right100mminclborder"></a><span data-ttu-id="fa306-724">戻り値 - right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fa306-724">Return Value - right100mmInclBorder</span></span>

## <a name="method-rightmarginandframe"></a><span data-ttu-id="fa306-725">メソッド rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="fa306-725">Method rightMarginAndFrame</span></span>

```xpp
public int rightMarginAndFrame()
```

### <a name="return-value---rightmarginandframe"></a><span data-ttu-id="fa306-726">戻り値 - rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="fa306-726">Return Value - rightMarginAndFrame</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="fa306-727">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="fa306-727">Method rightMarginMode</span></span>

```xpp
public int rightMarginMode([int value])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="fa306-728">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="fa306-728">Parameters - rightMarginMode</span></span>

<span data-ttu-id="fa306-729">値</span><span class="sxs-lookup"><span data-stu-id="fa306-729">value</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="fa306-730">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="fa306-730">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginstr"></a><span data-ttu-id="fa306-731">メソッド rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="fa306-731">Method rightMarginStr</span></span>

```xpp
public str rightMarginStr([str value])
```

### <a name="parameters---rightmarginstr"></a><span data-ttu-id="fa306-732">パラメーター - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="fa306-732">Parameters - rightMarginStr</span></span>

<span data-ttu-id="fa306-733">値</span><span class="sxs-lookup"><span data-stu-id="fa306-733">value</span></span>  

### <a name="return-value---rightmarginstr"></a><span data-ttu-id="fa306-734">戻り値 - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="fa306-734">Return Value - rightMarginStr</span></span>

## <a name="method-rightmarginunit"></a><span data-ttu-id="fa306-735">メソッド rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-735">Method rightMarginUnit</span></span>

```xpp
public Units rightMarginUnit([Units value])
```

### <a name="parameters---rightmarginunit"></a><span data-ttu-id="fa306-736">パラメーター - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-736">Parameters - rightMarginUnit</span></span>

<span data-ttu-id="fa306-737">値</span><span class="sxs-lookup"><span data-stu-id="fa306-737">value</span></span>  

### <a name="return-value---rightmarginunit"></a><span data-ttu-id="fa306-738">戻り値 - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-738">Return Value - rightMarginUnit</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="fa306-739">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="fa306-739">Method rightMarginValue</span></span>

```xpp
public Real rightMarginValue([Real value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="fa306-740">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="fa306-740">Parameters - rightMarginValue</span></span>

<span data-ttu-id="fa306-741">値</span><span class="sxs-lookup"><span data-stu-id="fa306-741">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="fa306-742">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="fa306-742">Return Value - rightMarginValue</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="fa306-743">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="fa306-743">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="fa306-744">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="fa306-744">Parameters - securityKey</span></span>

<span data-ttu-id="fa306-745">値</span><span class="sxs-lookup"><span data-stu-id="fa306-745">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="fa306-746">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="fa306-746">Return Value - securityKey</span></span>

## <a name="method-setheightgettext"></a><span data-ttu-id="fa306-747">メソッド setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="fa306-747">Method setHeightGetText</span></span>

```xpp
public str setHeightGetText(int lines, str string)
```

### <a name="parameters---setheightgettext"></a><span data-ttu-id="fa306-748">パラメーター - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="fa306-748">Parameters - setHeightGetText</span></span>

<span data-ttu-id="fa306-749">明細行</span><span class="sxs-lookup"><span data-stu-id="fa306-749">lines</span></span>  

<!-- -->

<span data-ttu-id="fa306-750">文字列</span><span class="sxs-lookup"><span data-stu-id="fa306-750">string</span></span>  

### <a name="return-value---setheightgettext"></a><span data-ttu-id="fa306-751">戻り値 - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="fa306-751">Return Value - setHeightGetText</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="fa306-752">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="fa306-752">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="fa306-753">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="fa306-753">Parameters - showLabel</span></span>

<span data-ttu-id="fa306-754">値</span><span class="sxs-lookup"><span data-stu-id="fa306-754">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="fa306-755">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="fa306-755">Return Value - showLabel</span></span>

## <a name="method-table"></a><span data-ttu-id="fa306-756">メソッド table</span><span class="sxs-lookup"><span data-stu-id="fa306-756">Method table</span></span>

<span data-ttu-id="fa306-757">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-757">Gets or sets the table ID associated with the object.</span></span>

```xpp
public TableId table([TableId value])
```

### <a name="parameters---table"></a><span data-ttu-id="fa306-758">パラメーター - table</span><span class="sxs-lookup"><span data-stu-id="fa306-758">Parameters - table</span></span>

<span data-ttu-id="fa306-759">値</span><span class="sxs-lookup"><span data-stu-id="fa306-759">value</span></span>  

### <a name="return-value---table"></a><span data-ttu-id="fa306-760">戻り値 - toBlob</span><span class="sxs-lookup"><span data-stu-id="fa306-760">Return Value - table</span></span>

<span data-ttu-id="fa306-761">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="fa306-761">The current value of the table ID associated with the object.</span></span>

## <a name="method-thickness"></a><span data-ttu-id="fa306-762">メソッド thickness</span><span class="sxs-lookup"><span data-stu-id="fa306-762">Method thickness</span></span>

```xpp
public LineThickness thickness([LineThickness value])
```

### <a name="parameters---thickness"></a><span data-ttu-id="fa306-763">パラメーター - thickness</span><span class="sxs-lookup"><span data-stu-id="fa306-763">Parameters - thickness</span></span>

<span data-ttu-id="fa306-764">値</span><span class="sxs-lookup"><span data-stu-id="fa306-764">value</span></span>  

### <a name="return-value---thickness"></a><span data-ttu-id="fa306-765">戻り値 - thickness</span><span class="sxs-lookup"><span data-stu-id="fa306-765">Return Value - thickness</span></span>

## <a name="method-timeformat"></a><span data-ttu-id="fa306-766">メソッド timeFormat</span><span class="sxs-lookup"><span data-stu-id="fa306-766">Method timeFormat</span></span>

```xpp
public int timeFormat([int value])
```

### <a name="parameters---timeformat"></a><span data-ttu-id="fa306-767">パラメーター - timeFormat</span><span class="sxs-lookup"><span data-stu-id="fa306-767">Parameters - timeFormat</span></span>

<span data-ttu-id="fa306-768">値</span><span class="sxs-lookup"><span data-stu-id="fa306-768">value</span></span>  

### <a name="return-value---timeformat"></a><span data-ttu-id="fa306-769">戻り値 - timeFormat</span><span class="sxs-lookup"><span data-stu-id="fa306-769">Return Value - timeFormat</span></span>

## <a name="method-timehours"></a><span data-ttu-id="fa306-770">メソッド timeHours</span><span class="sxs-lookup"><span data-stu-id="fa306-770">Method timeHours</span></span>

```xpp
public int timeHours([int value])
```

### <a name="parameters---timehours"></a><span data-ttu-id="fa306-771">パラメーター - timeHours</span><span class="sxs-lookup"><span data-stu-id="fa306-771">Parameters - timeHours</span></span>

<span data-ttu-id="fa306-772">値</span><span class="sxs-lookup"><span data-stu-id="fa306-772">value</span></span>  

### <a name="return-value---timehours"></a><span data-ttu-id="fa306-773">戻り値 - timeHours</span><span class="sxs-lookup"><span data-stu-id="fa306-773">Return Value - timeHours</span></span>

## <a name="method-timeminute"></a><span data-ttu-id="fa306-774">メソッド timeMinute</span><span class="sxs-lookup"><span data-stu-id="fa306-774">Method timeMinute</span></span>

```xpp
public int timeMinute([int value])
```

### <a name="parameters---timeminute"></a><span data-ttu-id="fa306-775">パラメーター - timeMinute</span><span class="sxs-lookup"><span data-stu-id="fa306-775">Parameters - timeMinute</span></span>

<span data-ttu-id="fa306-776">値</span><span class="sxs-lookup"><span data-stu-id="fa306-776">value</span></span>  

### <a name="return-value---timeminute"></a><span data-ttu-id="fa306-777">戻り値 - timeMinute</span><span class="sxs-lookup"><span data-stu-id="fa306-777">Return Value - timeMinute</span></span>

## <a name="method-timeseconds"></a><span data-ttu-id="fa306-778">メソッド timeSeconds</span><span class="sxs-lookup"><span data-stu-id="fa306-778">Method timeSeconds</span></span>

```xpp
public int timeSeconds([int value])
```

### <a name="parameters---timeseconds"></a><span data-ttu-id="fa306-779">パラメーター - timeSeconds</span><span class="sxs-lookup"><span data-stu-id="fa306-779">Parameters - timeSeconds</span></span>

<span data-ttu-id="fa306-780">値</span><span class="sxs-lookup"><span data-stu-id="fa306-780">value</span></span>  

### <a name="return-value---timeseconds"></a><span data-ttu-id="fa306-781">戻り値 - timeSeconds</span><span class="sxs-lookup"><span data-stu-id="fa306-781">Return Value - timeSeconds</span></span>

## <a name="method-timeseparator"></a><span data-ttu-id="fa306-782">メソッド timeSeparator</span><span class="sxs-lookup"><span data-stu-id="fa306-782">Method timeSeparator</span></span>

```xpp
public int timeSeparator([int value])
```

### <a name="parameters---timeseparator"></a><span data-ttu-id="fa306-783">パラメーター - timeSeparator</span><span class="sxs-lookup"><span data-stu-id="fa306-783">Parameters - timeSeparator</span></span>

<span data-ttu-id="fa306-784">値</span><span class="sxs-lookup"><span data-stu-id="fa306-784">value</span></span>  

### <a name="return-value---timeseparator"></a><span data-ttu-id="fa306-785">戻り値 - timeSeparator</span><span class="sxs-lookup"><span data-stu-id="fa306-785">Return Value - timeSeparator</span></span>

## <a name="method-top100mm"></a><span data-ttu-id="fa306-786">メソッド top100mm</span><span class="sxs-lookup"><span data-stu-id="fa306-786">Method top100mm</span></span>

```xpp
public int top100mm([int topExclBorder])
```

### <a name="parameters---top100mm"></a><span data-ttu-id="fa306-787">パラメーター - top100mm</span><span class="sxs-lookup"><span data-stu-id="fa306-787">Parameters - top100mm</span></span>

<span data-ttu-id="fa306-788">topExclBorder</span><span class="sxs-lookup"><span data-stu-id="fa306-788">topExclBorder</span></span>  

### <a name="return-value---top100mm"></a><span data-ttu-id="fa306-789">戻り値 - top100mm</span><span class="sxs-lookup"><span data-stu-id="fa306-789">Return Value - top100mm</span></span>

## <a name="method-top100mminclborder"></a><span data-ttu-id="fa306-790">メソッド top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fa306-790">Method top100mmInclBorder</span></span>

```xpp
public int top100mmInclBorder([int topInclBorder])
```

### <a name="parameters---top100mminclborder"></a><span data-ttu-id="fa306-791">パラメーター - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fa306-791">Parameters - top100mmInclBorder</span></span>

<span data-ttu-id="fa306-792">topInclBorder</span><span class="sxs-lookup"><span data-stu-id="fa306-792">topInclBorder</span></span>  

### <a name="return-value---top100mminclborder"></a><span data-ttu-id="fa306-793">戻り値 - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fa306-793">Return Value - top100mmInclBorder</span></span>

## <a name="method-topmarginandframe"></a><span data-ttu-id="fa306-794">メソッド topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="fa306-794">Method topMarginAndFrame</span></span>

```xpp
public int topMarginAndFrame()
```

### <a name="return-value---topmarginandframe"></a><span data-ttu-id="fa306-795">戻り値 - topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="fa306-795">Return Value - topMarginAndFrame</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="fa306-796">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="fa306-796">Method topMarginMode</span></span>

```xpp
public int topMarginMode([int value])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="fa306-797">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="fa306-797">Parameters - topMarginMode</span></span>

<span data-ttu-id="fa306-798">値</span><span class="sxs-lookup"><span data-stu-id="fa306-798">value</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="fa306-799">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="fa306-799">Return Value - topMarginMode</span></span>

## <a name="method-topmarginstr"></a><span data-ttu-id="fa306-800">メソッド topMarginStr</span><span class="sxs-lookup"><span data-stu-id="fa306-800">Method topMarginStr</span></span>

```xpp
public str topMarginStr([str value])
```

### <a name="parameters---topmarginstr"></a><span data-ttu-id="fa306-801">パラメーター - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="fa306-801">Parameters - topMarginStr</span></span>

<span data-ttu-id="fa306-802">値</span><span class="sxs-lookup"><span data-stu-id="fa306-802">value</span></span>  

### <a name="return-value---topmarginstr"></a><span data-ttu-id="fa306-803">戻り値 - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="fa306-803">Return Value - topMarginStr</span></span>

## <a name="method-topmarginunit"></a><span data-ttu-id="fa306-804">メソッド topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-804">Method topMarginUnit</span></span>

```xpp
public Units topMarginUnit([Units value])
```

### <a name="parameters---topmarginunit"></a><span data-ttu-id="fa306-805">パラメーター - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-805">Parameters - topMarginUnit</span></span>

<span data-ttu-id="fa306-806">値</span><span class="sxs-lookup"><span data-stu-id="fa306-806">value</span></span>  

### <a name="return-value---topmarginunit"></a><span data-ttu-id="fa306-807">戻り値 - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-807">Return Value - topMarginUnit</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="fa306-808">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="fa306-808">Method topMarginValue</span></span>

```xpp
public Real topMarginValue([Real value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="fa306-809">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="fa306-809">Parameters - topMarginValue</span></span>

<span data-ttu-id="fa306-810">値</span><span class="sxs-lookup"><span data-stu-id="fa306-810">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="fa306-811">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="fa306-811">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="fa306-812">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="fa306-812">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="fa306-813">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="fa306-813">Parameters - topMode</span></span>

<span data-ttu-id="fa306-814">値</span><span class="sxs-lookup"><span data-stu-id="fa306-814">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="fa306-815">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="fa306-815">Return Value - topMode</span></span>

## <a name="method-topstr"></a><span data-ttu-id="fa306-816">メソッド topStr</span><span class="sxs-lookup"><span data-stu-id="fa306-816">Method topStr</span></span>

```xpp
public str topStr([str value])
```

### <a name="parameters---topstr"></a><span data-ttu-id="fa306-817">パラメーター - topStr</span><span class="sxs-lookup"><span data-stu-id="fa306-817">Parameters - topStr</span></span>

<span data-ttu-id="fa306-818">値</span><span class="sxs-lookup"><span data-stu-id="fa306-818">value</span></span>  

### <a name="return-value---topstr"></a><span data-ttu-id="fa306-819">戻り値 - topStr</span><span class="sxs-lookup"><span data-stu-id="fa306-819">Return Value - topStr</span></span>

## <a name="method-topunit"></a><span data-ttu-id="fa306-820">メソッド topUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-820">Method topUnit</span></span>

```xpp
public Units topUnit([Units value])
```

### <a name="parameters---topunit"></a><span data-ttu-id="fa306-821">パラメーター - topUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-821">Parameters - topUnit</span></span>

<span data-ttu-id="fa306-822">値</span><span class="sxs-lookup"><span data-stu-id="fa306-822">value</span></span>  

### <a name="return-value---topunit"></a><span data-ttu-id="fa306-823">戻り値 - topUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-823">Return Value - topUnit</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="fa306-824">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="fa306-824">Method topValue</span></span>

```xpp
public Real topValue([Real value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="fa306-825">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="fa306-825">Parameters - topValue</span></span>

<span data-ttu-id="fa306-826">値</span><span class="sxs-lookup"><span data-stu-id="fa306-826">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="fa306-827">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="fa306-827">Return Value - topValue</span></span>

## <a name="method-underline"></a><span data-ttu-id="fa306-828">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="fa306-828">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="fa306-829">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="fa306-829">Parameters - underline</span></span>

<span data-ttu-id="fa306-830">値</span><span class="sxs-lookup"><span data-stu-id="fa306-830">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="fa306-831">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="fa306-831">Return Value - underline</span></span>

## <a name="method-visible"></a><span data-ttu-id="fa306-832">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="fa306-832">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="fa306-833">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="fa306-833">Parameters - visible</span></span>

<span data-ttu-id="fa306-834">値</span><span class="sxs-lookup"><span data-stu-id="fa306-834">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="fa306-835">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="fa306-835">Return Value - visible</span></span>

## <a name="method-webmenuitemname"></a><span data-ttu-id="fa306-836">メソッド webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="fa306-836">Method webMenuItemName</span></span>

```xpp
public str webMenuItemName([str value])
```

### <a name="parameters---webmenuitemname"></a><span data-ttu-id="fa306-837">パラメーター - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="fa306-837">Parameters - webMenuItemName</span></span>

<span data-ttu-id="fa306-838">値</span><span class="sxs-lookup"><span data-stu-id="fa306-838">value</span></span>  

### <a name="return-value---webmenuitemname"></a><span data-ttu-id="fa306-839">戻り値 - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="fa306-839">Return Value - webMenuItemName</span></span>

## <a name="method-webmenuitemtype"></a><span data-ttu-id="fa306-840">メソッド webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="fa306-840">Method webMenuItemType</span></span>

```xpp
public WebMenuItemType webMenuItemType([WebMenuItemType value])
```

### <a name="parameters---webmenuitemtype"></a><span data-ttu-id="fa306-841">パラメーター - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="fa306-841">Parameters - webMenuItemType</span></span>

<span data-ttu-id="fa306-842">値</span><span class="sxs-lookup"><span data-stu-id="fa306-842">value</span></span>  

### <a name="return-value---webmenuitemtype"></a><span data-ttu-id="fa306-843">戻り値 - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="fa306-843">Return Value - webMenuItemType</span></span>

## <a name="method-webtarget"></a><span data-ttu-id="fa306-844">メソッド webTarget</span><span class="sxs-lookup"><span data-stu-id="fa306-844">Method webTarget</span></span>

```xpp
public str webTarget([str value])
```

### <a name="parameters---webtarget"></a><span data-ttu-id="fa306-845">パラメーター - webTarget</span><span class="sxs-lookup"><span data-stu-id="fa306-845">Parameters - webTarget</span></span>

<span data-ttu-id="fa306-846">値</span><span class="sxs-lookup"><span data-stu-id="fa306-846">value</span></span>  

### <a name="return-value---webtarget"></a><span data-ttu-id="fa306-847">戻り値 - webTarget</span><span class="sxs-lookup"><span data-stu-id="fa306-847">Return Value - webTarget</span></span>

## <a name="method-width100mm"></a><span data-ttu-id="fa306-848">メソッド width100mm</span><span class="sxs-lookup"><span data-stu-id="fa306-848">Method width100mm</span></span>

```xpp
public int width100mm([int widthExclBorder])
```

### <a name="parameters---width100mm"></a><span data-ttu-id="fa306-849">パラメーター - width100mm</span><span class="sxs-lookup"><span data-stu-id="fa306-849">Parameters - width100mm</span></span>

<span data-ttu-id="fa306-850">widthExclBorder</span><span class="sxs-lookup"><span data-stu-id="fa306-850">widthExclBorder</span></span>  

### <a name="return-value---width100mm"></a><span data-ttu-id="fa306-851">戻り値 - width100mm</span><span class="sxs-lookup"><span data-stu-id="fa306-851">Return Value - width100mm</span></span>

## <a name="method-width100mminclborder"></a><span data-ttu-id="fa306-852">メソッド width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fa306-852">Method width100mmInclBorder</span></span>

```xpp
public int width100mmInclBorder([int widthInclBorder])
```

### <a name="parameters---width100mminclborder"></a><span data-ttu-id="fa306-853">パラメーター - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fa306-853">Parameters - width100mmInclBorder</span></span>

<span data-ttu-id="fa306-854">widthInclBorder</span><span class="sxs-lookup"><span data-stu-id="fa306-854">widthInclBorder</span></span>  

### <a name="return-value---width100mminclborder"></a><span data-ttu-id="fa306-855">戻り値 - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fa306-855">Return Value - width100mmInclBorder</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="fa306-856">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="fa306-856">Method widthMode</span></span>

<span data-ttu-id="fa306-857">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-857">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="fa306-858">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="fa306-858">Parameters - widthMode</span></span>

<span data-ttu-id="fa306-859">値</span><span class="sxs-lookup"><span data-stu-id="fa306-859">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="fa306-860">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="fa306-860">Return Value - widthMode</span></span>

<span data-ttu-id="fa306-861">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="fa306-861">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="fa306-862">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="fa306-862">Remarks - widthMode</span></span>

<span data-ttu-id="fa306-863">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="fa306-863">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="fa306-864">モード。</span><span class="sxs-lookup"><span data-stu-id="fa306-864">Mode.</span></span>         | <span data-ttu-id="fa306-865">幅計算。</span><span class="sxs-lookup"><span data-stu-id="fa306-865">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa306-866">正確。</span><span class="sxs-lookup"><span data-stu-id="fa306-866">Exact.</span></span>        | <span data-ttu-id="fa306-867">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa306-867">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="fa306-868">自動。</span><span class="sxs-lookup"><span data-stu-id="fa306-868">Auto.</span></span>         | <span data-ttu-id="fa306-869">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="fa306-869">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="fa306-870">列の幅。</span><span class="sxs-lookup"><span data-stu-id="fa306-870">Column width.</span></span> | <span data-ttu-id="fa306-871">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="fa306-871">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="fa306-872">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="fa306-872">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthofstring100mm"></a><span data-ttu-id="fa306-873">メソッド widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="fa306-873">Method widthOfString100mm</span></span>

```xpp
public int widthOfString100mm(str string)
```

### <a name="parameters---widthofstring100mm"></a><span data-ttu-id="fa306-874">パラメーター - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="fa306-874">Parameters - widthOfString100mm</span></span>

<span data-ttu-id="fa306-875">文字列</span><span class="sxs-lookup"><span data-stu-id="fa306-875">string</span></span>  

### <a name="return-value---widthofstring100mm"></a><span data-ttu-id="fa306-876">戻り値 - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="fa306-876">Return Value - widthOfString100mm</span></span>

## <a name="method-widthstr"></a><span data-ttu-id="fa306-877">メソッド widthStr</span><span class="sxs-lookup"><span data-stu-id="fa306-877">Method widthStr</span></span>

```xpp
public str widthStr([str value])
```

### <a name="parameters---widthstr"></a><span data-ttu-id="fa306-878">パラメーター - widthStr</span><span class="sxs-lookup"><span data-stu-id="fa306-878">Parameters - widthStr</span></span>

<span data-ttu-id="fa306-879">値</span><span class="sxs-lookup"><span data-stu-id="fa306-879">value</span></span>  

### <a name="return-value---widthstr"></a><span data-ttu-id="fa306-880">戻り値 - widthStr</span><span class="sxs-lookup"><span data-stu-id="fa306-880">Return Value - widthStr</span></span>

## <a name="method-widthunit"></a><span data-ttu-id="fa306-881">メソッド widthUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-881">Method widthUnit</span></span>

```xpp
public Units widthUnit([Units value])
```

### <a name="parameters---widthunit"></a><span data-ttu-id="fa306-882">パラメーター - widthUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-882">Parameters - widthUnit</span></span>

<span data-ttu-id="fa306-883">値</span><span class="sxs-lookup"><span data-stu-id="fa306-883">value</span></span>  

### <a name="return-value---widthunit"></a><span data-ttu-id="fa306-884">戻り値 - widthUnit</span><span class="sxs-lookup"><span data-stu-id="fa306-884">Return Value - widthUnit</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="fa306-885">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="fa306-885">Method widthValue</span></span>

<span data-ttu-id="fa306-886">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-886">Gets or sets the width of the control.</span></span>

```xpp
public Real widthValue([Real value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="fa306-887">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="fa306-887">Parameters - widthValue</span></span>

<span data-ttu-id="fa306-888">値</span><span class="sxs-lookup"><span data-stu-id="fa306-888">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="fa306-889">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="fa306-889">Return Value - widthValue</span></span>

<span data-ttu-id="fa306-890">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="fa306-890">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="fa306-891">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="fa306-891">Remarks - widthValue</span></span>

<span data-ttu-id="fa306-892">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="fa306-892">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="fa306-893">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="fa306-893">Method leftMargin</span></span>

```xpp
public void leftMargin(Real value, Units unit)
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="fa306-894">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="fa306-894">Parameters - leftMargin</span></span>

<span data-ttu-id="fa306-895">値</span><span class="sxs-lookup"><span data-stu-id="fa306-895">value</span></span>  

<!-- -->

<span data-ttu-id="fa306-896">単位</span><span class="sxs-lookup"><span data-stu-id="fa306-896">unit</span></span>  

## <a name="method-rightmargin"></a><span data-ttu-id="fa306-897">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="fa306-897">Method rightMargin</span></span>

```xpp
public void rightMargin(Real value, Units unit)
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="fa306-898">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="fa306-898">Parameters - rightMargin</span></span>

<span data-ttu-id="fa306-899">値</span><span class="sxs-lookup"><span data-stu-id="fa306-899">value</span></span>  

<!-- -->

<span data-ttu-id="fa306-900">単位</span><span class="sxs-lookup"><span data-stu-id="fa306-900">unit</span></span>  

## <a name="method-bottommargin"></a><span data-ttu-id="fa306-901">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="fa306-901">Method bottomMargin</span></span>

```xpp
public void bottomMargin(Real value, Units unit)
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="fa306-902">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="fa306-902">Parameters - bottomMargin</span></span>

<span data-ttu-id="fa306-903">値</span><span class="sxs-lookup"><span data-stu-id="fa306-903">value</span></span>  

<!-- -->

<span data-ttu-id="fa306-904">単位</span><span class="sxs-lookup"><span data-stu-id="fa306-904">unit</span></span>  

## <a name="method-width"></a><span data-ttu-id="fa306-905">メソッド width</span><span class="sxs-lookup"><span data-stu-id="fa306-905">Method width</span></span>

<span data-ttu-id="fa306-906">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-906">Gets or sets the width of the control.</span></span>

```xpp
public void width(Real value, Units unit)
```

### <a name="parameters---width"></a><span data-ttu-id="fa306-907">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="fa306-907">Parameters - width</span></span>

<span data-ttu-id="fa306-908">値</span><span class="sxs-lookup"><span data-stu-id="fa306-908">value</span></span>  

<!-- -->

<span data-ttu-id="fa306-909">単位</span><span class="sxs-lookup"><span data-stu-id="fa306-909">unit</span></span>  

### <a name="remarks---width"></a><span data-ttu-id="fa306-910">備考 - width</span><span class="sxs-lookup"><span data-stu-id="fa306-910">Remarks - width</span></span>

<span data-ttu-id="fa306-911">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa306-911">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="fa306-912">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="fa306-912">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="fa306-913">モード。</span><span class="sxs-lookup"><span data-stu-id="fa306-913">Mode.</span></span>           | <span data-ttu-id="fa306-914">幅計算。</span><span class="sxs-lookup"><span data-stu-id="fa306-914">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa306-915">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="fa306-915">-1 Exact.</span></span>       | <span data-ttu-id="fa306-916">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa306-916">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="fa306-917">0 自動。</span><span class="sxs-lookup"><span data-stu-id="fa306-917">0 Auto.</span></span>         | <span data-ttu-id="fa306-918">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="fa306-918">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="fa306-919">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="fa306-919">1 Column width.</span></span> | <span data-ttu-id="fa306-920">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="fa306-920">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="fa306-921">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="fa306-921">The width and width calculation mode can be set separately.</span></span>

## <a name="method-top"></a><span data-ttu-id="fa306-922">メソッド top</span><span class="sxs-lookup"><span data-stu-id="fa306-922">Method top</span></span>

```xpp
public void top(Real value, Units unit)
```

### <a name="parameters---top"></a><span data-ttu-id="fa306-923">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="fa306-923">Parameters - top</span></span>

<span data-ttu-id="fa306-924">値</span><span class="sxs-lookup"><span data-stu-id="fa306-924">value</span></span>  

<!-- -->

<span data-ttu-id="fa306-925">単位</span><span class="sxs-lookup"><span data-stu-id="fa306-925">unit</span></span>  

## <a name="method-height"></a><span data-ttu-id="fa306-926">メソッド height</span><span class="sxs-lookup"><span data-stu-id="fa306-926">Method height</span></span>

<span data-ttu-id="fa306-927">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fa306-927">Gets or sets the height of the control.</span></span>

```xpp
public void height(Real value, Units unit)
```

### <a name="parameters---height"></a><span data-ttu-id="fa306-928">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="fa306-928">Parameters - height</span></span>

<span data-ttu-id="fa306-929">値</span><span class="sxs-lookup"><span data-stu-id="fa306-929">value</span></span>  

<!-- -->

<span data-ttu-id="fa306-930">単位</span><span class="sxs-lookup"><span data-stu-id="fa306-930">unit</span></span>  

### <a name="remarks---height"></a><span data-ttu-id="fa306-931">備考 - height</span><span class="sxs-lookup"><span data-stu-id="fa306-931">Remarks - height</span></span>

<span data-ttu-id="fa306-932">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa306-932">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="fa306-933">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="fa306-933">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="fa306-934">モード。</span><span class="sxs-lookup"><span data-stu-id="fa306-934">Mode.</span></span>            | <span data-ttu-id="fa306-935">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="fa306-935">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa306-936">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="fa306-936">-1 Exact.</span></span>        | <span data-ttu-id="fa306-937">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa306-937">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="fa306-938">0 自動。</span><span class="sxs-lookup"><span data-stu-id="fa306-938">0 Auto.</span></span>          | <span data-ttu-id="fa306-939">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="fa306-939">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="fa306-940">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="fa306-940">1 Column height.</span></span> | <span data-ttu-id="fa306-941">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="fa306-941">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="fa306-942">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="fa306-942">The height and height calculation mode can be set separately.</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="fa306-943">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="fa306-943">Method labelWidth</span></span>

```xpp
public void labelWidth(Real value, Units unit)
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="fa306-944">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="fa306-944">Parameters - labelWidth</span></span>

<span data-ttu-id="fa306-945">値</span><span class="sxs-lookup"><span data-stu-id="fa306-945">value</span></span>  

<!-- -->

<span data-ttu-id="fa306-946">単位</span><span class="sxs-lookup"><span data-stu-id="fa306-946">unit</span></span>  

## <a name="method-topmargin"></a><span data-ttu-id="fa306-947">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="fa306-947">Method topMargin</span></span>

```xpp
public void topMargin(Real value, Units unit)
```

### <a name="parameters---topmargin"></a><span data-ttu-id="fa306-948">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="fa306-948">Parameters - topMargin</span></span>

<span data-ttu-id="fa306-949">値</span><span class="sxs-lookup"><span data-stu-id="fa306-949">value</span></span>  

<!-- -->

<span data-ttu-id="fa306-950">単位</span><span class="sxs-lookup"><span data-stu-id="fa306-950">unit</span></span>  

## <a name="method-left"></a><span data-ttu-id="fa306-951">メソッド left</span><span class="sxs-lookup"><span data-stu-id="fa306-951">Method left</span></span>

```xpp
public void left(Real value, Units unit)
```

### <a name="parameters---left"></a><span data-ttu-id="fa306-952">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="fa306-952">Parameters - left</span></span>

<span data-ttu-id="fa306-953">値</span><span class="sxs-lookup"><span data-stu-id="fa306-953">value</span></span>  

<!-- -->

<span data-ttu-id="fa306-954">単位</span><span class="sxs-lookup"><span data-stu-id="fa306-954">unit</span></span>  

## <a name="method-hide"></a><span data-ttu-id="fa306-955">メソッド hide</span><span class="sxs-lookup"><span data-stu-id="fa306-955">Method hide</span></span>

```xpp
public void hide()
```

## <a name="method-show"></a><span data-ttu-id="fa306-956">メソッド show</span><span class="sxs-lookup"><span data-stu-id="fa306-956">Method show</span></span>

```xpp
public void show()
```

