---
title: ReportShapeControl クラス
description: このトピックでは、ReportShapeControl クラスについて説明します。
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
ms.openlocfilehash: 74aec881287a0a36d8cbac9fda8ba35c92a3acff
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502830"
---
# <a name="class-reportshapecontrol"></a><span data-ttu-id="09829-103">クラス ReportShapeControl</span><span class="sxs-lookup"><span data-stu-id="09829-103">Class ReportShapeControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ReportShapeControl extends ReportControl
```

<span data-ttu-id="09829-104">ReportShapeControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="09829-104">The ReportShapeControl class enables you to create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="09829-105">備考</span><span class="sxs-lookup"><span data-stu-id="09829-105">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="09829-106">例</span><span class="sxs-lookup"><span data-stu-id="09829-106">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="09829-107">メソッド</span><span class="sxs-lookup"><span data-stu-id="09829-107">Methods</span></span>

| <span data-ttu-id="09829-108">方法</span><span class="sxs-lookup"><span data-stu-id="09829-108">Method</span></span>                                                                   | <span data-ttu-id="09829-109">説明</span><span class="sxs-lookup"><span data-stu-id="09829-109">Description</span></span>                                                                                                       |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09829-110">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="09829-110">public boolean autoDeclaration(\[boolean value\])</span></span>                        | <span data-ttu-id="09829-111">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="09829-111">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                |
| <span data-ttu-id="09829-112">public int bottomMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="09829-112">public int bottomMarginAndFrame()</span></span>                                        |                                                                                                                   |
| <span data-ttu-id="09829-113">public int bottomMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09829-113">public int bottomMarginMode(\[int value\])</span></span>                               |                                                                                                                   |
| <span data-ttu-id="09829-114">public str bottomMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09829-114">public str bottomMarginStr(\[str value\])</span></span>                                |                                                                                                                   |
| <span data-ttu-id="09829-115">public Units bottomMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="09829-115">public Units bottomMarginUnit(\[Units value\])</span></span>                           |                                                                                                                   |
| <span data-ttu-id="09829-116">public Real bottomMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="09829-116">public Real bottomMarginValue(\[Real value\])</span></span>                            |                                                                                                                   |
| <span data-ttu-id="09829-117">public int changeLabelCase(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09829-117">public int changeLabelCase(\[int value\])</span></span>                                |                                                                                                                   |
| <span data-ttu-id="09829-118">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09829-118">public int colorScheme(\[int value\])</span></span>                                    | <span data-ttu-id="09829-119">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09829-119">Gets or sets the color scheme of the control.</span></span>                                                                     |
| <span data-ttu-id="09829-120">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="09829-120">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="09829-121">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09829-121">Gets or sets the configuration key that is assigned to the control.</span></span>                                               |
| <span data-ttu-id="09829-122">public ReportFieldType controlType()</span><span class="sxs-lookup"><span data-stu-id="09829-122">public ReportFieldType controlType()</span></span>                                     |                                                                                                                   |
| <span data-ttu-id="09829-123">public str cssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09829-123">public str cssClass(\[str value\])</span></span>                                       |                                                                                                                   |
| <span data-ttu-id="09829-124">public int delete()</span><span class="sxs-lookup"><span data-stu-id="09829-124">public int delete()</span></span>                                                      |                                                                                                                   |
| <span data-ttu-id="09829-125">public str effectiveFont()</span><span class="sxs-lookup"><span data-stu-id="09829-125">public str effectiveFont()</span></span>                                               |                                                                                                                   |
| <span data-ttu-id="09829-126">public str fontInfoPrinter()</span><span class="sxs-lookup"><span data-stu-id="09829-126">public str fontInfoPrinter()</span></span>                                             |                                                                                                                   |
| <span data-ttu-id="09829-127">public int fontInfoPrinterAscent()</span><span class="sxs-lookup"><span data-stu-id="09829-127">public int fontInfoPrinterAscent()</span></span>                                       |                                                                                                                   |
| <span data-ttu-id="09829-128">public int fontInfoPrinterDescent()</span><span class="sxs-lookup"><span data-stu-id="09829-128">public int fontInfoPrinterDescent()</span></span>                                      |                                                                                                                   |
| <span data-ttu-id="09829-129">public int fontInfoPrinterExtLead()</span><span class="sxs-lookup"><span data-stu-id="09829-129">public int fontInfoPrinterExtLead()</span></span>                                      |                                                                                                                   |
| <span data-ttu-id="09829-130">public int fontInfoPrinterHeight()</span><span class="sxs-lookup"><span data-stu-id="09829-130">public int fontInfoPrinterHeight()</span></span>                                       |                                                                                                                   |
| <span data-ttu-id="09829-131">public int fontInfoPrinterIntLead()</span><span class="sxs-lookup"><span data-stu-id="09829-131">public int fontInfoPrinterIntLead()</span></span>                                      |                                                                                                                   |
| <span data-ttu-id="09829-132">public str fontInfoScreen()</span><span class="sxs-lookup"><span data-stu-id="09829-132">public str fontInfoScreen()</span></span>                                              |                                                                                                                   |
| <span data-ttu-id="09829-133">public int fontInfoScreenAscent()</span><span class="sxs-lookup"><span data-stu-id="09829-133">public int fontInfoScreenAscent()</span></span>                                        |                                                                                                                   |
| <span data-ttu-id="09829-134">public int fontInfoScreenDescent()</span><span class="sxs-lookup"><span data-stu-id="09829-134">public int fontInfoScreenDescent()</span></span>                                       |                                                                                                                   |
| <span data-ttu-id="09829-135">public int fontInfoScreenExtLead()</span><span class="sxs-lookup"><span data-stu-id="09829-135">public int fontInfoScreenExtLead()</span></span>                                       |                                                                                                                   |
| <span data-ttu-id="09829-136">public int fontInfoScreenHeight()</span><span class="sxs-lookup"><span data-stu-id="09829-136">public int fontInfoScreenHeight()</span></span>                                        |                                                                                                                   |
| <span data-ttu-id="09829-137">public int fontInfoScreenIntLead()</span><span class="sxs-lookup"><span data-stu-id="09829-137">public int fontInfoScreenIntLead()</span></span>                                       |                                                                                                                   |
| <span data-ttu-id="09829-138">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09829-138">public int foregroundColor(\[int value\])</span></span>                                | <span data-ttu-id="09829-139">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09829-139">Gets or sets the text color for the control to use.</span></span>                                                               |
| <span data-ttu-id="09829-140">public int height100mm(\[int heightExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="09829-140">public int height100mm(\[int heightExclBorder\])</span></span>                         |                                                                                                                   |
| <span data-ttu-id="09829-141">public int height100mmInclBorder(\[int heightInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="09829-141">public int height100mmInclBorder(\[int heightInclBorder\])</span></span>               |                                                                                                                   |
| <span data-ttu-id="09829-142">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09829-142">public int heightMode(\[int value\])</span></span>                                     | <span data-ttu-id="09829-143">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09829-143">Gets or sets a calculation mode for the height of the control.</span></span>                                                    |
| <span data-ttu-id="09829-144">public int heightOfWordWrappedString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="09829-144">public int heightOfWordWrappedString100mm(str string)</span></span>                    |                                                                                                                   |
| <span data-ttu-id="09829-145">public str heightStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09829-145">public str heightStr(\[str value\])</span></span>                                      |                                                                                                                   |
| <span data-ttu-id="09829-146">public Units heightUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="09829-146">public Units heightUnit(\[Units value\])</span></span>                                 |                                                                                                                   |
| <span data-ttu-id="09829-147">public Real heightValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="09829-147">public Real heightValue(\[Real value\])</span></span>                                  | <span data-ttu-id="09829-148">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09829-148">Gets or sets the height of the control.</span></span>                                                                           |
| <span data-ttu-id="09829-149">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09829-149">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="09829-150">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09829-150">Gets or sets the label for a control.</span></span>                                                                             |
| <span data-ttu-id="09829-151">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09829-151">public int labelBold(\[int value\])</span></span>                                      |                                                                                                                   |
| <span data-ttu-id="09829-152">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09829-152">public int labelCharacterSet(\[int value\])</span></span>                              |                                                                                                                   |
| <span data-ttu-id="09829-153">public str labelCssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09829-153">public str labelCssClass(\[str value\])</span></span>                                  |                                                                                                                   |
| <span data-ttu-id="09829-154">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09829-154">public str labelFont(\[str value\])</span></span>                                      |                                                                                                                   |
| <span data-ttu-id="09829-155">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09829-155">public int labelFontSize(\[int value\])</span></span>                                  |                                                                                                                   |
| <span data-ttu-id="09829-156">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="09829-156">public boolean labelItalic(\[boolean value\])</span></span>                            |                                                                                                                   |
| <span data-ttu-id="09829-157">public LineType labelLineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="09829-157">public LineType labelLineBelow(\[LineType value\])</span></span>                       |                                                                                                                   |
| <span data-ttu-id="09829-158">public LineThickness labelLineThickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="09829-158">public LineThickness labelLineThickness(\[LineThickness value\])</span></span>         |                                                                                                                   |
| <span data-ttu-id="09829-159">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09829-159">public int labelPosition(\[int value\])</span></span>                                  |                                                                                                                   |
| <span data-ttu-id="09829-160">public int labelTabLeader(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09829-160">public int labelTabLeader(\[int value\])</span></span>                                 |                                                                                                                   |
| <span data-ttu-id="09829-161">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="09829-161">public boolean labelUnderline(\[boolean value\])</span></span>                         |                                                                                                                   |
| <span data-ttu-id="09829-162">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09829-162">public int labelWidthMode(\[int value\])</span></span>                                 |                                                                                                                   |
| <span data-ttu-id="09829-163">public str labelWidthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09829-163">public str labelWidthStr(\[str value\])</span></span>                                  |                                                                                                                   |
| <span data-ttu-id="09829-164">public Units labelWidthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="09829-164">public Units labelWidthUnit(\[Units value\])</span></span>                             |                                                                                                                   |
| <span data-ttu-id="09829-165">public Real labelWidthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="09829-165">public Real labelWidthValue(\[Real value\])</span></span>                              |                                                                                                                   |
| <span data-ttu-id="09829-166">public int left100mm(\[int leftExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="09829-166">public int left100mm(\[int leftExclBorder\])</span></span>                             |                                                                                                                   |
| <span data-ttu-id="09829-167">public int left100mmInclBorder(\[int leftInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="09829-167">public int left100mmInclBorder(\[int leftInclBorder\])</span></span>                   |                                                                                                                   |
| <span data-ttu-id="09829-168">public int leftMarginAnFrame()</span><span class="sxs-lookup"><span data-stu-id="09829-168">public int leftMarginAnFrame()</span></span>                                           |                                                                                                                   |
| <span data-ttu-id="09829-169">public int leftMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09829-169">public int leftMarginMode(\[int value\])</span></span>                                 |                                                                                                                   |
| <span data-ttu-id="09829-170">public str leftMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09829-170">public str leftMarginStr(\[str value\])</span></span>                                  |                                                                                                                   |
| <span data-ttu-id="09829-171">public Units leftMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="09829-171">public Units leftMarginUnit(\[Units value\])</span></span>                             |                                                                                                                   |
| <span data-ttu-id="09829-172">public Real leftMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="09829-172">public Real leftMarginValue(\[Real value\])</span></span>                              |                                                                                                                   |
| <span data-ttu-id="09829-173">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09829-173">public int leftMode(\[int value\])</span></span>                                       |                                                                                                                   |
| <span data-ttu-id="09829-174">public str leftStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09829-174">public str leftStr(\[str value\])</span></span>                                        |                                                                                                                   |
| <span data-ttu-id="09829-175">public Units leftUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="09829-175">public Units leftUnit(\[Units value\])</span></span>                                   |                                                                                                                   |
| <span data-ttu-id="09829-176">public Real leftValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="09829-176">public Real leftValue(\[Real value\])</span></span>                                    |                                                                                                                   |
| <span data-ttu-id="09829-177">public LineType line(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="09829-177">public LineType line(\[LineType value\])</span></span>                                 |                                                                                                                   |
| <span data-ttu-id="09829-178">public LineType lineAbove(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="09829-178">public LineType lineAbove(\[LineType value\])</span></span>                            |                                                                                                                   |
| <span data-ttu-id="09829-179">public LineType lineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="09829-179">public LineType lineBelow(\[LineType value\])</span></span>                            |                                                                                                                   |
| <span data-ttu-id="09829-180">public LineType lineLeft(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="09829-180">public LineType lineLeft(\[LineType value\])</span></span>                             | <span data-ttu-id="09829-181">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09829-181">Gets or sets the type of line that is used as the left border of a section.</span></span>                                       |
| <span data-ttu-id="09829-182">public LineType lineRight(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="09829-182">public LineType lineRight(\[LineType value\])</span></span>                            |                                                                                                                   |
| <span data-ttu-id="09829-183">public str menuItemLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09829-183">public str menuItemLabel(\[str value\])</span></span>                                  |                                                                                                                   |
| <span data-ttu-id="09829-184">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09829-184">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                   |
| <span data-ttu-id="09829-185">public MenuItemType menuItemType(\[MenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="09829-185">public MenuItemType menuItemType(\[MenuItemType value\])</span></span>                 |                                                                                                                   |
| <span data-ttu-id="09829-186">public str modelFieldName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09829-186">public str modelFieldName(\[str value\])</span></span>                                 |                                                                                                                   |
| <span data-ttu-id="09829-187">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09829-187">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="09829-188">フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09829-188">Gets or sets the name used in code to identify a form, report, table, query, or another MSDAX application object.</span></span> |
| <span data-ttu-id="09829-189">public int numberOfLines(int height100mm)</span><span class="sxs-lookup"><span data-stu-id="09829-189">public int numberOfLines(int height100mm)</span></span>                                |                                                                                                                   |
| <span data-ttu-id="09829-190">public int position(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09829-190">public int position(\[int value\])</span></span>                                       |                                                                                                                   |
| <span data-ttu-id="09829-191">public str previewInfo(str string)</span><span class="sxs-lookup"><span data-stu-id="09829-191">public str previewInfo(str string)</span></span>                                       |                                                                                                                   |
| <span data-ttu-id="09829-192">public int previewXCompensation100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="09829-192">public int previewXCompensation100mm(str string)</span></span>                         |                                                                                                                   |
| <span data-ttu-id="09829-193">public int right100mm()</span><span class="sxs-lookup"><span data-stu-id="09829-193">public int right100mm()</span></span>                                                  |                                                                                                                   |
| <span data-ttu-id="09829-194">public int right100mmInclBorder()</span><span class="sxs-lookup"><span data-stu-id="09829-194">public int right100mmInclBorder()</span></span>                                        |                                                                                                                   |
| <span data-ttu-id="09829-195">public int rightMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="09829-195">public int rightMarginAndFrame()</span></span>                                         |                                                                                                                   |
| <span data-ttu-id="09829-196">public int rightMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09829-196">public int rightMarginMode(\[int value\])</span></span>                                |                                                                                                                   |
| <span data-ttu-id="09829-197">public str rightMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09829-197">public str rightMarginStr(\[str value\])</span></span>                                 |                                                                                                                   |
| <span data-ttu-id="09829-198">public Units rightMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="09829-198">public Units rightMarginUnit(\[Units value\])</span></span>                            |                                                                                                                   |
| <span data-ttu-id="09829-199">public Real rightMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="09829-199">public Real rightMarginValue(\[Real value\])</span></span>                             |                                                                                                                   |
| <span data-ttu-id="09829-200">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="09829-200">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                   |
| <span data-ttu-id="09829-201">public str setHeightGetText(int lines, str string)</span><span class="sxs-lookup"><span data-stu-id="09829-201">public str setHeightGetText(int lines, str string)</span></span>                       |                                                                                                                   |
| <span data-ttu-id="09829-202">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="09829-202">public boolean showLabel(\[boolean value\])</span></span>                              |                                                                                                                   |
| <span data-ttu-id="09829-203">public LineThickness thickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="09829-203">public LineThickness thickness(\[LineThickness value\])</span></span>                  |                                                                                                                   |
| <span data-ttu-id="09829-204">public int top100mm(\[int topExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="09829-204">public int top100mm(\[int topExclBorder\])</span></span>                               |                                                                                                                   |
| <span data-ttu-id="09829-205">public int top100mmInclBorder(\[int topInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="09829-205">public int top100mmInclBorder(\[int topInclBorder\])</span></span>                     |                                                                                                                   |
| <span data-ttu-id="09829-206">public int topMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="09829-206">public int topMarginAndFrame()</span></span>                                           |                                                                                                                   |
| <span data-ttu-id="09829-207">public int topMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09829-207">public int topMarginMode(\[int value\])</span></span>                                  |                                                                                                                   |
| <span data-ttu-id="09829-208">public str topMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09829-208">public str topMarginStr(\[str value\])</span></span>                                   |                                                                                                                   |
| <span data-ttu-id="09829-209">public Units topMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="09829-209">public Units topMarginUnit(\[Units value\])</span></span>                              |                                                                                                                   |
| <span data-ttu-id="09829-210">public Real topMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="09829-210">public Real topMarginValue(\[Real value\])</span></span>                               |                                                                                                                   |
| <span data-ttu-id="09829-211">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09829-211">public int topMode(\[int value\])</span></span>                                        |                                                                                                                   |
| <span data-ttu-id="09829-212">public str topStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09829-212">public str topStr(\[str value\])</span></span>                                         |                                                                                                                   |
| <span data-ttu-id="09829-213">public Units topUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="09829-213">public Units topUnit(\[Units value\])</span></span>                                    |                                                                                                                   |
| <span data-ttu-id="09829-214">public Real topValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="09829-214">public Real topValue(\[Real value\])</span></span>                                     |                                                                                                                   |
| <span data-ttu-id="09829-215">public ShapeType type(\[ShapeType value\])</span><span class="sxs-lookup"><span data-stu-id="09829-215">public ShapeType type(\[ShapeType value\])</span></span>                               |                                                                                                                   |
| <span data-ttu-id="09829-216">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="09829-216">public boolean visible(\[boolean value\])</span></span>                                |                                                                                                                   |
| <span data-ttu-id="09829-217">public str webMenuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09829-217">public str webMenuItemName(\[str value\])</span></span>                                |                                                                                                                   |
| <span data-ttu-id="09829-218">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="09829-218">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span></span>        |                                                                                                                   |
| <span data-ttu-id="09829-219">public str webTarget(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09829-219">public str webTarget(\[str value\])</span></span>                                      |                                                                                                                   |
| <span data-ttu-id="09829-220">public int width100mm(\[int widthExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="09829-220">public int width100mm(\[int widthExclBorder\])</span></span>                           |                                                                                                                   |
| <span data-ttu-id="09829-221">public int width100mmInclBorder(\[int widthInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="09829-221">public int width100mmInclBorder(\[int widthInclBorder\])</span></span>                 |                                                                                                                   |
| <span data-ttu-id="09829-222">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="09829-222">public int widthMode(\[int value\])</span></span>                                      | <span data-ttu-id="09829-223">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09829-223">Gets or sets the calculation mode of the width of the control.</span></span>                                                    |
| <span data-ttu-id="09829-224">public int widthOfString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="09829-224">public int widthOfString100mm(str string)</span></span>                                |                                                                                                                   |
| <span data-ttu-id="09829-225">public str widthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="09829-225">public str widthStr(\[str value\])</span></span>                                       |                                                                                                                   |
| <span data-ttu-id="09829-226">public Units widthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="09829-226">public Units widthUnit(\[Units value\])</span></span>                                  |                                                                                                                   |
| <span data-ttu-id="09829-227">public Real widthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="09829-227">public Real widthValue(\[Real value\])</span></span>                                   | <span data-ttu-id="09829-228">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09829-228">Gets or sets the width of the control.</span></span>                                                                            |
| <span data-ttu-id="09829-229">public void bottomMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="09829-229">public void bottomMargin(Real value, Units unit)</span></span>                         |                                                                                                                   |
| <span data-ttu-id="09829-230">public void left(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="09829-230">public void left(Real value, Units unit)</span></span>                                 |                                                                                                                   |
| <span data-ttu-id="09829-231">public void top(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="09829-231">public void top(Real value, Units unit)</span></span>                                  |                                                                                                                   |
| <span data-ttu-id="09829-232">public void labelWidth(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="09829-232">public void labelWidth(Real value, Units unit)</span></span>                           |                                                                                                                   |
| <span data-ttu-id="09829-233">public void height(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="09829-233">public void height(Real value, Units unit)</span></span>                               | <span data-ttu-id="09829-234">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09829-234">Gets or sets the height of the control.</span></span>                                                                           |
| <span data-ttu-id="09829-235">public void leftMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="09829-235">public void leftMargin(Real value, Units unit)</span></span>                           |                                                                                                                   |
| <span data-ttu-id="09829-236">public void rightMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="09829-236">public void rightMargin(Real value, Units unit)</span></span>                          |                                                                                                                   |
| <span data-ttu-id="09829-237">public void hide()</span><span class="sxs-lookup"><span data-stu-id="09829-237">public void hide()</span></span>                                                       |                                                                                                                   |
| <span data-ttu-id="09829-238">public void topMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="09829-238">public void topMargin(Real value, Units unit)</span></span>                            |                                                                                                                   |
| <span data-ttu-id="09829-239">public void show()</span><span class="sxs-lookup"><span data-stu-id="09829-239">public void show()</span></span>                                                       |                                                                                                                   |
| <span data-ttu-id="09829-240">public void width(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="09829-240">public void width(Real value, Units unit)</span></span>                                | <span data-ttu-id="09829-241">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09829-241">Gets or sets the width of the control.</span></span>                                                                            |

## <a name="method-autodeclaration"></a><span data-ttu-id="09829-242">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="09829-242">Method autoDeclaration</span></span>

<span data-ttu-id="09829-243">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="09829-243">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="09829-244">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="09829-244">Parameters - autoDeclaration</span></span>

<span data-ttu-id="09829-245">値</span><span class="sxs-lookup"><span data-stu-id="09829-245">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="09829-246">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="09829-246">Return Value - autoDeclaration</span></span>

<span data-ttu-id="09829-247">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="09829-247">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="09829-248">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="09829-248">Remarks - autoDeclaration</span></span>

<span data-ttu-id="09829-249">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="09829-249">Controls cannot have identical names.</span></span>

## <a name="method-bottommarginandframe"></a><span data-ttu-id="09829-250">メソッド bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="09829-250">Method bottomMarginAndFrame</span></span>

```xpp
public int bottomMarginAndFrame()
```

### <a name="return-value---bottommarginandframe"></a><span data-ttu-id="09829-251">戻り値 - bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="09829-251">Return Value - bottomMarginAndFrame</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="09829-252">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="09829-252">Method bottomMarginMode</span></span>

```xpp
public int bottomMarginMode([int value])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="09829-253">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="09829-253">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="09829-254">値</span><span class="sxs-lookup"><span data-stu-id="09829-254">value</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="09829-255">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="09829-255">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginstr"></a><span data-ttu-id="09829-256">メソッド bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="09829-256">Method bottomMarginStr</span></span>

```xpp
public str bottomMarginStr([str value])
```

### <a name="parameters---bottommarginstr"></a><span data-ttu-id="09829-257">パラメーター - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="09829-257">Parameters - bottomMarginStr</span></span>

<span data-ttu-id="09829-258">値</span><span class="sxs-lookup"><span data-stu-id="09829-258">value</span></span>  

### <a name="return-value---bottommarginstr"></a><span data-ttu-id="09829-259">戻り値 - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="09829-259">Return Value - bottomMarginStr</span></span>

## <a name="method-bottommarginunit"></a><span data-ttu-id="09829-260">メソッド bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="09829-260">Method bottomMarginUnit</span></span>

```xpp
public Units bottomMarginUnit([Units value])
```

### <a name="parameters---bottommarginunit"></a><span data-ttu-id="09829-261">パラメーター - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="09829-261">Parameters - bottomMarginUnit</span></span>

<span data-ttu-id="09829-262">値</span><span class="sxs-lookup"><span data-stu-id="09829-262">value</span></span>  

### <a name="return-value---bottommarginunit"></a><span data-ttu-id="09829-263">戻り値 - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="09829-263">Return Value - bottomMarginUnit</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="09829-264">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="09829-264">Method bottomMarginValue</span></span>

```xpp
public Real bottomMarginValue([Real value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="09829-265">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="09829-265">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="09829-266">値</span><span class="sxs-lookup"><span data-stu-id="09829-266">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="09829-267">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="09829-267">Return Value - bottomMarginValue</span></span>

## <a name="method-changelabelcase"></a><span data-ttu-id="09829-268">メソッド changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="09829-268">Method changeLabelCase</span></span>

```xpp
public int changeLabelCase([int value])
```

### <a name="parameters---changelabelcase"></a><span data-ttu-id="09829-269">パラメーター - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="09829-269">Parameters - changeLabelCase</span></span>

<span data-ttu-id="09829-270">値</span><span class="sxs-lookup"><span data-stu-id="09829-270">value</span></span>  

### <a name="return-value---changelabelcase"></a><span data-ttu-id="09829-271">戻り値 - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="09829-271">Return Value - changeLabelCase</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="09829-272">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="09829-272">Method colorScheme</span></span>

<span data-ttu-id="09829-273">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09829-273">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="09829-274">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="09829-274">Parameters - colorScheme</span></span>

<span data-ttu-id="09829-275">値</span><span class="sxs-lookup"><span data-stu-id="09829-275">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="09829-276">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="09829-276">Return Value - colorScheme</span></span>

<span data-ttu-id="09829-277">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="09829-277">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="09829-278">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="09829-278">Remarks - colorScheme</span></span>

<span data-ttu-id="09829-279">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="09829-279">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="09829-280">値です。</span><span class="sxs-lookup"><span data-stu-id="09829-280">Value.</span></span> | <span data-ttu-id="09829-281">スタイル。</span><span class="sxs-lookup"><span data-stu-id="09829-281">Style.</span></span>                         |
|--------|--------------------------------|
| <span data-ttu-id="09829-282">0</span><span class="sxs-lookup"><span data-stu-id="09829-282">0</span></span>      | <span data-ttu-id="09829-283">既定。</span><span class="sxs-lookup"><span data-stu-id="09829-283">Default.</span></span>                       |
| <span data-ttu-id="09829-284">1</span><span class="sxs-lookup"><span data-stu-id="09829-284">1</span></span>      | <span data-ttu-id="09829-285">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="09829-285">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="09829-286">2</span><span class="sxs-lookup"><span data-stu-id="09829-286">2</span></span>      | <span data-ttu-id="09829-287">真の配色。</span><span class="sxs-lookup"><span data-stu-id="09829-287">The true-color scheme.</span></span>         |

## <a name="method-configurationkey"></a><span data-ttu-id="09829-288">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="09829-288">Method configurationKey</span></span>

<span data-ttu-id="09829-289">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09829-289">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="09829-290">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="09829-290">Parameters - configurationKey</span></span>

<span data-ttu-id="09829-291">値</span><span class="sxs-lookup"><span data-stu-id="09829-291">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="09829-292">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="09829-292">Return Value - configurationKey</span></span>

<span data-ttu-id="09829-293">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="09829-293">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="09829-294">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="09829-294">Remarks - configurationKey</span></span>

<span data-ttu-id="09829-295">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="09829-295">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="09829-296">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="09829-296">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-controltype"></a><span data-ttu-id="09829-297">メソッド controlType</span><span class="sxs-lookup"><span data-stu-id="09829-297">Method controlType</span></span>

```xpp
public ReportFieldType controlType()
```

### <a name="return-value---controltype"></a><span data-ttu-id="09829-298">戻り値 - controlType</span><span class="sxs-lookup"><span data-stu-id="09829-298">Return Value - controlType</span></span>

## <a name="method-cssclass"></a><span data-ttu-id="09829-299">メソッド cssClass</span><span class="sxs-lookup"><span data-stu-id="09829-299">Method cssClass</span></span>

```xpp
public str cssClass([str value])
```

### <a name="parameters---cssclass"></a><span data-ttu-id="09829-300">パラメーター - cssClass</span><span class="sxs-lookup"><span data-stu-id="09829-300">Parameters - cssClass</span></span>

<span data-ttu-id="09829-301">値</span><span class="sxs-lookup"><span data-stu-id="09829-301">value</span></span>  

### <a name="return-value---cssclass"></a><span data-ttu-id="09829-302">戻り値 - cssClass</span><span class="sxs-lookup"><span data-stu-id="09829-302">Return Value - cssClass</span></span>

## <a name="method-delete"></a><span data-ttu-id="09829-303">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="09829-303">Method delete</span></span>

```xpp
public int delete()
```

### <a name="return-value---delete"></a><span data-ttu-id="09829-304">戻り値 - delete</span><span class="sxs-lookup"><span data-stu-id="09829-304">Return Value - delete</span></span>

## <a name="method-effectivefont"></a><span data-ttu-id="09829-305">メソッド effectiveFont</span><span class="sxs-lookup"><span data-stu-id="09829-305">Method effectiveFont</span></span>

```xpp
public str effectiveFont()
```

### <a name="return-value---effectivefont"></a><span data-ttu-id="09829-306">戻り値 - effectiveFont</span><span class="sxs-lookup"><span data-stu-id="09829-306">Return Value - effectiveFont</span></span>

## <a name="method-fontinfoprinter"></a><span data-ttu-id="09829-307">メソッド fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="09829-307">Method fontInfoPrinter</span></span>

```xpp
public str fontInfoPrinter()
```

### <a name="return-value---fontinfoprinter"></a><span data-ttu-id="09829-308">戻り値 - fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="09829-308">Return Value - fontInfoPrinter</span></span>

## <a name="method-fontinfoprinterascent"></a><span data-ttu-id="09829-309">メソッド fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="09829-309">Method fontInfoPrinterAscent</span></span>

```xpp
public int fontInfoPrinterAscent()
```

### <a name="return-value---fontinfoprinterascent"></a><span data-ttu-id="09829-310">戻り値 - fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="09829-310">Return Value - fontInfoPrinterAscent</span></span>

## <a name="method-fontinfoprinterdescent"></a><span data-ttu-id="09829-311">メソッド fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="09829-311">Method fontInfoPrinterDescent</span></span>

```xpp
public int fontInfoPrinterDescent()
```

### <a name="return-value---fontinfoprinterdescent"></a><span data-ttu-id="09829-312">戻り値 - fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="09829-312">Return Value - fontInfoPrinterDescent</span></span>

## <a name="method-fontinfoprinterextlead"></a><span data-ttu-id="09829-313">メソッド fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="09829-313">Method fontInfoPrinterExtLead</span></span>

```xpp
public int fontInfoPrinterExtLead()
```

### <a name="return-value---fontinfoprinterextlead"></a><span data-ttu-id="09829-314">戻り値 - fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="09829-314">Return Value - fontInfoPrinterExtLead</span></span>

## <a name="method-fontinfoprinterheight"></a><span data-ttu-id="09829-315">メソッド fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="09829-315">Method fontInfoPrinterHeight</span></span>

```xpp
public int fontInfoPrinterHeight()
```

### <a name="return-value---fontinfoprinterheight"></a><span data-ttu-id="09829-316">戻り値 - fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="09829-316">Return Value - fontInfoPrinterHeight</span></span>

## <a name="method-fontinfoprinterintlead"></a><span data-ttu-id="09829-317">メソッド fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="09829-317">Method fontInfoPrinterIntLead</span></span>

```xpp
public int fontInfoPrinterIntLead()
```

### <a name="return-value---fontinfoprinterintlead"></a><span data-ttu-id="09829-318">戻り値 - fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="09829-318">Return Value - fontInfoPrinterIntLead</span></span>

## <a name="method-fontinfoscreen"></a><span data-ttu-id="09829-319">メソッド fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="09829-319">Method fontInfoScreen</span></span>

```xpp
public str fontInfoScreen()
```

### <a name="return-value---fontinfoscreen"></a><span data-ttu-id="09829-320">戻り値 - fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="09829-320">Return Value - fontInfoScreen</span></span>

## <a name="method-fontinfoscreenascent"></a><span data-ttu-id="09829-321">メソッド fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="09829-321">Method fontInfoScreenAscent</span></span>

```xpp
public int fontInfoScreenAscent()
```

### <a name="return-value---fontinfoscreenascent"></a><span data-ttu-id="09829-322">戻り値 - fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="09829-322">Return Value - fontInfoScreenAscent</span></span>

## <a name="method-fontinfoscreendescent"></a><span data-ttu-id="09829-323">メソッド fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="09829-323">Method fontInfoScreenDescent</span></span>

```xpp
public int fontInfoScreenDescent()
```

### <a name="return-value---fontinfoscreendescent"></a><span data-ttu-id="09829-324">戻り値 - fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="09829-324">Return Value - fontInfoScreenDescent</span></span>

## <a name="method-fontinfoscreenextlead"></a><span data-ttu-id="09829-325">メソッド fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="09829-325">Method fontInfoScreenExtLead</span></span>

```xpp
public int fontInfoScreenExtLead()
```

### <a name="return-value---fontinfoscreenextlead"></a><span data-ttu-id="09829-326">戻り値 - fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="09829-326">Return Value - fontInfoScreenExtLead</span></span>

## <a name="method-fontinfoscreenheight"></a><span data-ttu-id="09829-327">メソッド fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="09829-327">Method fontInfoScreenHeight</span></span>

```xpp
public int fontInfoScreenHeight()
```

### <a name="return-value---fontinfoscreenheight"></a><span data-ttu-id="09829-328">戻り値 - fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="09829-328">Return Value - fontInfoScreenHeight</span></span>

## <a name="method-fontinfoscreenintlead"></a><span data-ttu-id="09829-329">メソッド fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="09829-329">Method fontInfoScreenIntLead</span></span>

```xpp
public int fontInfoScreenIntLead()
```

### <a name="return-value---fontinfoscreenintlead"></a><span data-ttu-id="09829-330">戻り値 - fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="09829-330">Return Value - fontInfoScreenIntLead</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="09829-331">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="09829-331">Method foregroundColor</span></span>

<span data-ttu-id="09829-332">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09829-332">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="09829-333">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="09829-333">Parameters - foregroundColor</span></span>

<span data-ttu-id="09829-334">値</span><span class="sxs-lookup"><span data-stu-id="09829-334">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="09829-335">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="09829-335">Return Value - foregroundColor</span></span>

<span data-ttu-id="09829-336">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="09829-336">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="09829-337">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="09829-337">Remarks - foregroundColor</span></span>

<span data-ttu-id="09829-338">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="09829-338">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="09829-339">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="09829-339">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="09829-340">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="09829-340">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="09829-341">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="09829-341">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="09829-342">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="09829-342">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="09829-343">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="09829-343">The maximum value for a single byte is 255.</span></span>

## <a name="method-height100mm"></a><span data-ttu-id="09829-344">メソッド height100mm</span><span class="sxs-lookup"><span data-stu-id="09829-344">Method height100mm</span></span>

```xpp
public int height100mm([int heightExclBorder])
```

### <a name="parameters---height100mm"></a><span data-ttu-id="09829-345">パラメーター - height100mm</span><span class="sxs-lookup"><span data-stu-id="09829-345">Parameters - height100mm</span></span>

<span data-ttu-id="09829-346">heightExclBorder</span><span class="sxs-lookup"><span data-stu-id="09829-346">heightExclBorder</span></span>  

### <a name="return-value---height100mm"></a><span data-ttu-id="09829-347">戻り値 - height100mm</span><span class="sxs-lookup"><span data-stu-id="09829-347">Return Value - height100mm</span></span>

## <a name="method-height100mminclborder"></a><span data-ttu-id="09829-348">メソッド height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="09829-348">Method height100mmInclBorder</span></span>

```xpp
public int height100mmInclBorder([int heightInclBorder])
```

### <a name="parameters---height100mminclborder"></a><span data-ttu-id="09829-349">パラメーター - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="09829-349">Parameters - height100mmInclBorder</span></span>

<span data-ttu-id="09829-350">heightInclBorder</span><span class="sxs-lookup"><span data-stu-id="09829-350">heightInclBorder</span></span>  

### <a name="return-value---height100mminclborder"></a><span data-ttu-id="09829-351">戻り値 - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="09829-351">Return Value - height100mmInclBorder</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="09829-352">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="09829-352">Method heightMode</span></span>

<span data-ttu-id="09829-353">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09829-353">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="09829-354">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="09829-354">Parameters - heightMode</span></span>

<span data-ttu-id="09829-355">値</span><span class="sxs-lookup"><span data-stu-id="09829-355">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="09829-356">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="09829-356">Return Value - heightMode</span></span>

<span data-ttu-id="09829-357">計算モード。</span><span class="sxs-lookup"><span data-stu-id="09829-357">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="09829-358">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="09829-358">Remarks - heightMode</span></span>

<span data-ttu-id="09829-359">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="09829-359">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="09829-360">モード。</span><span class="sxs-lookup"><span data-stu-id="09829-360">Mode.</span></span>          | <span data-ttu-id="09829-361">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="09829-361">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="09829-362">正確。</span><span class="sxs-lookup"><span data-stu-id="09829-362">Exact.</span></span>         | <span data-ttu-id="09829-363">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="09829-363">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="09829-364">自動。</span><span class="sxs-lookup"><span data-stu-id="09829-364">Auto.</span></span>          | <span data-ttu-id="09829-365">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="09829-365">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="09829-366">列の高さ</span><span class="sxs-lookup"><span data-stu-id="09829-366">Column height.</span></span> | <span data-ttu-id="09829-367">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="09829-367">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="09829-368">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="09829-368">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightofwordwrappedstring100mm"></a><span data-ttu-id="09829-369">メソッド heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="09829-369">Method heightOfWordWrappedString100mm</span></span>

```xpp
public int heightOfWordWrappedString100mm(str string)
```

### <a name="parameters---heightofwordwrappedstring100mm"></a><span data-ttu-id="09829-370">パラメーター - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="09829-370">Parameters - heightOfWordWrappedString100mm</span></span>

<span data-ttu-id="09829-371">文字列</span><span class="sxs-lookup"><span data-stu-id="09829-371">string</span></span>  

### <a name="return-value---heightofwordwrappedstring100mm"></a><span data-ttu-id="09829-372">戻り値 - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="09829-372">Return Value - heightOfWordWrappedString100mm</span></span>

## <a name="method-heightstr"></a><span data-ttu-id="09829-373">メソッド heightStr</span><span class="sxs-lookup"><span data-stu-id="09829-373">Method heightStr</span></span>

```xpp
public str heightStr([str value])
```

### <a name="parameters---heightstr"></a><span data-ttu-id="09829-374">パラメーター - heightStr</span><span class="sxs-lookup"><span data-stu-id="09829-374">Parameters - heightStr</span></span>

<span data-ttu-id="09829-375">値</span><span class="sxs-lookup"><span data-stu-id="09829-375">value</span></span>  

### <a name="return-value---heightstr"></a><span data-ttu-id="09829-376">戻り値 - heightStr</span><span class="sxs-lookup"><span data-stu-id="09829-376">Return Value - heightStr</span></span>

## <a name="method-heightunit"></a><span data-ttu-id="09829-377">メソッド heightUnit</span><span class="sxs-lookup"><span data-stu-id="09829-377">Method heightUnit</span></span>

```xpp
public Units heightUnit([Units value])
```

### <a name="parameters---heightunit"></a><span data-ttu-id="09829-378">パラメーター - heightUnit</span><span class="sxs-lookup"><span data-stu-id="09829-378">Parameters - heightUnit</span></span>

<span data-ttu-id="09829-379">値</span><span class="sxs-lookup"><span data-stu-id="09829-379">value</span></span>  

### <a name="return-value---heightunit"></a><span data-ttu-id="09829-380">戻り値 - heightUnit</span><span class="sxs-lookup"><span data-stu-id="09829-380">Return Value - heightUnit</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="09829-381">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="09829-381">Method heightValue</span></span>

<span data-ttu-id="09829-382">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09829-382">Gets or sets the height of the control.</span></span>

```xpp
public Real heightValue([Real value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="09829-383">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="09829-383">Parameters - heightValue</span></span>

<span data-ttu-id="09829-384">値</span><span class="sxs-lookup"><span data-stu-id="09829-384">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="09829-385">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="09829-385">Return Value - heightValue</span></span>

<span data-ttu-id="09829-386">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="09829-386">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="09829-387">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="09829-387">Remarks - heightValue</span></span>

<span data-ttu-id="09829-388">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="09829-388">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-label"></a><span data-ttu-id="09829-389">メソッド label</span><span class="sxs-lookup"><span data-stu-id="09829-389">Method label</span></span>

<span data-ttu-id="09829-390">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09829-390">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="09829-391">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="09829-391">Parameters - label</span></span>

<span data-ttu-id="09829-392">値</span><span class="sxs-lookup"><span data-stu-id="09829-392">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="09829-393">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="09829-393">Return Value - label</span></span>

<span data-ttu-id="09829-394">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="09829-394">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="09829-395">備考 - label</span><span class="sxs-lookup"><span data-stu-id="09829-395">Remarks - label</span></span>

<span data-ttu-id="09829-396">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="09829-396">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="09829-397">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="09829-397">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="09829-398">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="09829-398">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="09829-399">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="09829-399">Parameters - labelBold</span></span>

<span data-ttu-id="09829-400">値</span><span class="sxs-lookup"><span data-stu-id="09829-400">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="09829-401">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="09829-401">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="09829-402">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="09829-402">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="09829-403">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="09829-403">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="09829-404">値</span><span class="sxs-lookup"><span data-stu-id="09829-404">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="09829-405">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="09829-405">Return Value - labelCharacterSet</span></span>

## <a name="method-labelcssclass"></a><span data-ttu-id="09829-406">メソッド labelCssClass</span><span class="sxs-lookup"><span data-stu-id="09829-406">Method labelCssClass</span></span>

```xpp
public str labelCssClass([str value])
```

### <a name="parameters---labelcssclass"></a><span data-ttu-id="09829-407">パラメーター - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="09829-407">Parameters - labelCssClass</span></span>

<span data-ttu-id="09829-408">値</span><span class="sxs-lookup"><span data-stu-id="09829-408">value</span></span>  

### <a name="return-value---labelcssclass"></a><span data-ttu-id="09829-409">戻り値 - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="09829-409">Return Value - labelCssClass</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="09829-410">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="09829-410">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="09829-411">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="09829-411">Parameters - labelFont</span></span>

<span data-ttu-id="09829-412">値</span><span class="sxs-lookup"><span data-stu-id="09829-412">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="09829-413">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="09829-413">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="09829-414">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="09829-414">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="09829-415">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="09829-415">Parameters - labelFontSize</span></span>

<span data-ttu-id="09829-416">値</span><span class="sxs-lookup"><span data-stu-id="09829-416">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="09829-417">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="09829-417">Return Value - labelFontSize</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="09829-418">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="09829-418">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="09829-419">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="09829-419">Parameters - labelItalic</span></span>

<span data-ttu-id="09829-420">値</span><span class="sxs-lookup"><span data-stu-id="09829-420">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="09829-421">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="09829-421">Return Value - labelItalic</span></span>

## <a name="method-labellinebelow"></a><span data-ttu-id="09829-422">メソッド labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="09829-422">Method labelLineBelow</span></span>

```xpp
public LineType labelLineBelow([LineType value])
```

### <a name="parameters---labellinebelow"></a><span data-ttu-id="09829-423">パラメーター - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="09829-423">Parameters - labelLineBelow</span></span>

<span data-ttu-id="09829-424">値</span><span class="sxs-lookup"><span data-stu-id="09829-424">value</span></span>  

### <a name="return-value---labellinebelow"></a><span data-ttu-id="09829-425">戻り値 - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="09829-425">Return Value - labelLineBelow</span></span>

## <a name="method-labellinethickness"></a><span data-ttu-id="09829-426">メソッド labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="09829-426">Method labelLineThickness</span></span>

```xpp
public LineThickness labelLineThickness([LineThickness value])
```

### <a name="parameters---labellinethickness"></a><span data-ttu-id="09829-427">パラメーター - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="09829-427">Parameters - labelLineThickness</span></span>

<span data-ttu-id="09829-428">値</span><span class="sxs-lookup"><span data-stu-id="09829-428">value</span></span>  

### <a name="return-value---labellinethickness"></a><span data-ttu-id="09829-429">戻り値 - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="09829-429">Return Value - labelLineThickness</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="09829-430">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="09829-430">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="09829-431">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="09829-431">Parameters - labelPosition</span></span>

<span data-ttu-id="09829-432">値</span><span class="sxs-lookup"><span data-stu-id="09829-432">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="09829-433">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="09829-433">Return Value - labelPosition</span></span>

## <a name="method-labeltableader"></a><span data-ttu-id="09829-434">メソッド labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="09829-434">Method labelTabLeader</span></span>

```xpp
public int labelTabLeader([int value])
```

### <a name="parameters---labeltableader"></a><span data-ttu-id="09829-435">パラメーター - labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="09829-435">Parameters - labelTabLeader</span></span>

<span data-ttu-id="09829-436">値</span><span class="sxs-lookup"><span data-stu-id="09829-436">value</span></span>  

### <a name="return-value---labeltableader"></a><span data-ttu-id="09829-437">戻り値 - labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="09829-437">Return Value - labelTabLeader</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="09829-438">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="09829-438">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="09829-439">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="09829-439">Parameters - labelUnderline</span></span>

<span data-ttu-id="09829-440">値</span><span class="sxs-lookup"><span data-stu-id="09829-440">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="09829-441">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="09829-441">Return Value - labelUnderline</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="09829-442">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="09829-442">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="09829-443">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="09829-443">Parameters - labelWidthMode</span></span>

<span data-ttu-id="09829-444">値</span><span class="sxs-lookup"><span data-stu-id="09829-444">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="09829-445">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="09829-445">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthstr"></a><span data-ttu-id="09829-446">メソッド labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="09829-446">Method labelWidthStr</span></span>

```xpp
public str labelWidthStr([str value])
```

### <a name="parameters---labelwidthstr"></a><span data-ttu-id="09829-447">パラメーター - labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="09829-447">Parameters - labelWidthStr</span></span>

<span data-ttu-id="09829-448">値</span><span class="sxs-lookup"><span data-stu-id="09829-448">value</span></span>  

### <a name="return-value---labelwidthstr"></a><span data-ttu-id="09829-449">戻り値 - labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="09829-449">Return Value - labelWidthStr</span></span>

## <a name="method-labelwidthunit"></a><span data-ttu-id="09829-450">メソッド labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="09829-450">Method labelWidthUnit</span></span>

```xpp
public Units labelWidthUnit([Units value])
```

### <a name="parameters---labelwidthunit"></a><span data-ttu-id="09829-451">パラメーター - labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="09829-451">Parameters - labelWidthUnit</span></span>

<span data-ttu-id="09829-452">値</span><span class="sxs-lookup"><span data-stu-id="09829-452">value</span></span>  

### <a name="return-value---labelwidthunit"></a><span data-ttu-id="09829-453">戻り値 - labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="09829-453">Return Value - labelWidthUnit</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="09829-454">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="09829-454">Method labelWidthValue</span></span>

```xpp
public Real labelWidthValue([Real value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="09829-455">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="09829-455">Parameters - labelWidthValue</span></span>

<span data-ttu-id="09829-456">値</span><span class="sxs-lookup"><span data-stu-id="09829-456">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="09829-457">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="09829-457">Return Value - labelWidthValue</span></span>

## <a name="method-left100mm"></a><span data-ttu-id="09829-458">メソッド left100mm</span><span class="sxs-lookup"><span data-stu-id="09829-458">Method left100mm</span></span>

```xpp
public int left100mm([int leftExclBorder])
```

### <a name="parameters---left100mm"></a><span data-ttu-id="09829-459">パラメーター - left100mm</span><span class="sxs-lookup"><span data-stu-id="09829-459">Parameters - left100mm</span></span>

<span data-ttu-id="09829-460">leftExclBorder</span><span class="sxs-lookup"><span data-stu-id="09829-460">leftExclBorder</span></span>  

### <a name="return-value---left100mm"></a><span data-ttu-id="09829-461">戻り値 - left100mm</span><span class="sxs-lookup"><span data-stu-id="09829-461">Return Value - left100mm</span></span>

## <a name="method-left100mminclborder"></a><span data-ttu-id="09829-462">メソッド left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="09829-462">Method left100mmInclBorder</span></span>

```xpp
public int left100mmInclBorder([int leftInclBorder])
```

### <a name="parameters---left100mminclborder"></a><span data-ttu-id="09829-463">パラメーター - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="09829-463">Parameters - left100mmInclBorder</span></span>

<span data-ttu-id="09829-464">leftInclBorder</span><span class="sxs-lookup"><span data-stu-id="09829-464">leftInclBorder</span></span>  

### <a name="return-value---left100mminclborder"></a><span data-ttu-id="09829-465">戻り値 - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="09829-465">Return Value - left100mmInclBorder</span></span>

## <a name="method-leftmarginanframe"></a><span data-ttu-id="09829-466">メソッド leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="09829-466">Method leftMarginAnFrame</span></span>

```xpp
public int leftMarginAnFrame()
```

### <a name="return-value---leftmarginanframe"></a><span data-ttu-id="09829-467">戻り値 - leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="09829-467">Return Value - leftMarginAnFrame</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="09829-468">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="09829-468">Method leftMarginMode</span></span>

```xpp
public int leftMarginMode([int value])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="09829-469">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="09829-469">Parameters - leftMarginMode</span></span>

<span data-ttu-id="09829-470">値</span><span class="sxs-lookup"><span data-stu-id="09829-470">value</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="09829-471">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="09829-471">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginstr"></a><span data-ttu-id="09829-472">メソッド leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="09829-472">Method leftMarginStr</span></span>

```xpp
public str leftMarginStr([str value])
```

### <a name="parameters---leftmarginstr"></a><span data-ttu-id="09829-473">パラメーター - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="09829-473">Parameters - leftMarginStr</span></span>

<span data-ttu-id="09829-474">値</span><span class="sxs-lookup"><span data-stu-id="09829-474">value</span></span>  

### <a name="return-value---leftmarginstr"></a><span data-ttu-id="09829-475">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="09829-475">Return Value - leftMarginStr</span></span>

## <a name="method-leftmarginunit"></a><span data-ttu-id="09829-476">メソッド leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="09829-476">Method leftMarginUnit</span></span>

```xpp
public Units leftMarginUnit([Units value])
```

### <a name="parameters---leftmarginunit"></a><span data-ttu-id="09829-477">パラメーター - leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="09829-477">Parameters - leftMarginUnit</span></span>

<span data-ttu-id="09829-478">値</span><span class="sxs-lookup"><span data-stu-id="09829-478">value</span></span>  

### <a name="return-value---leftmarginunit"></a><span data-ttu-id="09829-479">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="09829-479">Return Value - leftMarginUnit</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="09829-480">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="09829-480">Method leftMarginValue</span></span>

```xpp
public Real leftMarginValue([Real value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="09829-481">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="09829-481">Parameters - leftMarginValue</span></span>

<span data-ttu-id="09829-482">値</span><span class="sxs-lookup"><span data-stu-id="09829-482">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="09829-483">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="09829-483">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="09829-484">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="09829-484">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="09829-485">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="09829-485">Parameters - leftMode</span></span>

<span data-ttu-id="09829-486">値</span><span class="sxs-lookup"><span data-stu-id="09829-486">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="09829-487">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="09829-487">Return Value - leftMode</span></span>

## <a name="method-leftstr"></a><span data-ttu-id="09829-488">メソッド leftStr</span><span class="sxs-lookup"><span data-stu-id="09829-488">Method leftStr</span></span>

```xpp
public str leftStr([str value])
```

### <a name="parameters---leftstr"></a><span data-ttu-id="09829-489">パラメーター - leftStr</span><span class="sxs-lookup"><span data-stu-id="09829-489">Parameters - leftStr</span></span>

<span data-ttu-id="09829-490">値</span><span class="sxs-lookup"><span data-stu-id="09829-490">value</span></span>  

### <a name="return-value---leftstr"></a><span data-ttu-id="09829-491">戻り値 - leftStr</span><span class="sxs-lookup"><span data-stu-id="09829-491">Return Value - leftStr</span></span>

## <a name="method-leftunit"></a><span data-ttu-id="09829-492">メソッド leftUnit</span><span class="sxs-lookup"><span data-stu-id="09829-492">Method leftUnit</span></span>

```xpp
public Units leftUnit([Units value])
```

### <a name="parameters---leftunit"></a><span data-ttu-id="09829-493">パラメーター - leftUnit</span><span class="sxs-lookup"><span data-stu-id="09829-493">Parameters - leftUnit</span></span>

<span data-ttu-id="09829-494">値</span><span class="sxs-lookup"><span data-stu-id="09829-494">value</span></span>  

### <a name="return-value---leftunit"></a><span data-ttu-id="09829-495">戻り値 - leftUnit</span><span class="sxs-lookup"><span data-stu-id="09829-495">Return Value - leftUnit</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="09829-496">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="09829-496">Method leftValue</span></span>

```xpp
public Real leftValue([Real value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="09829-497">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="09829-497">Parameters - leftValue</span></span>

<span data-ttu-id="09829-498">値</span><span class="sxs-lookup"><span data-stu-id="09829-498">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="09829-499">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="09829-499">Return Value - leftValue</span></span>

## <a name="method-line"></a><span data-ttu-id="09829-500">メソッド line</span><span class="sxs-lookup"><span data-stu-id="09829-500">Method line</span></span>

```xpp
public LineType line([LineType value])
```

### <a name="parameters---line"></a><span data-ttu-id="09829-501">パラメーター - line</span><span class="sxs-lookup"><span data-stu-id="09829-501">Parameters - line</span></span>

<span data-ttu-id="09829-502">値</span><span class="sxs-lookup"><span data-stu-id="09829-502">value</span></span>  

### <a name="return-value---line"></a><span data-ttu-id="09829-503">戻り値 - line</span><span class="sxs-lookup"><span data-stu-id="09829-503">Return Value - line</span></span>

## <a name="method-lineabove"></a><span data-ttu-id="09829-504">メソッド lineAbove</span><span class="sxs-lookup"><span data-stu-id="09829-504">Method lineAbove</span></span>

```xpp
public LineType lineAbove([LineType value])
```

### <a name="parameters---lineabove"></a><span data-ttu-id="09829-505">パラメーター - lineAbove</span><span class="sxs-lookup"><span data-stu-id="09829-505">Parameters - lineAbove</span></span>

<span data-ttu-id="09829-506">値</span><span class="sxs-lookup"><span data-stu-id="09829-506">value</span></span>  

### <a name="return-value---lineabove"></a><span data-ttu-id="09829-507">戻り値 - lineAbove</span><span class="sxs-lookup"><span data-stu-id="09829-507">Return Value - lineAbove</span></span>

## <a name="method-linebelow"></a><span data-ttu-id="09829-508">メソッド lineBelow</span><span class="sxs-lookup"><span data-stu-id="09829-508">Method lineBelow</span></span>

```xpp
public LineType lineBelow([LineType value])
```

### <a name="parameters---linebelow"></a><span data-ttu-id="09829-509">パラメーター - lineBelow</span><span class="sxs-lookup"><span data-stu-id="09829-509">Parameters - lineBelow</span></span>

<span data-ttu-id="09829-510">値</span><span class="sxs-lookup"><span data-stu-id="09829-510">value</span></span>  

### <a name="return-value---linebelow"></a><span data-ttu-id="09829-511">戻り値 - lineBelow</span><span class="sxs-lookup"><span data-stu-id="09829-511">Return Value - lineBelow</span></span>

## <a name="method-lineleft"></a><span data-ttu-id="09829-512">メソッド lineLeft</span><span class="sxs-lookup"><span data-stu-id="09829-512">Method lineLeft</span></span>

<span data-ttu-id="09829-513">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09829-513">Gets or sets the type of line that is used as the left border of a section.</span></span>

```xpp
public LineType lineLeft([LineType value])
```

### <a name="parameters---lineleft"></a><span data-ttu-id="09829-514">パラメーター - lineLeft</span><span class="sxs-lookup"><span data-stu-id="09829-514">Parameters - lineLeft</span></span>

<span data-ttu-id="09829-515">値</span><span class="sxs-lookup"><span data-stu-id="09829-515">value</span></span>  

### <a name="return-value---lineleft"></a><span data-ttu-id="09829-516">戻り値 - lineLeft</span><span class="sxs-lookup"><span data-stu-id="09829-516">Return Value - lineLeft</span></span>

<span data-ttu-id="09829-517">左境界線として使用される線のタイプ。</span><span class="sxs-lookup"><span data-stu-id="09829-517">The type of line that is used as the left border.</span></span>

## <a name="method-lineright"></a><span data-ttu-id="09829-518">メソッド lineRight</span><span class="sxs-lookup"><span data-stu-id="09829-518">Method lineRight</span></span>

```xpp
public LineType lineRight([LineType value])
```

### <a name="parameters---lineright"></a><span data-ttu-id="09829-519">パラメーター - lineRight</span><span class="sxs-lookup"><span data-stu-id="09829-519">Parameters - lineRight</span></span>

<span data-ttu-id="09829-520">値</span><span class="sxs-lookup"><span data-stu-id="09829-520">value</span></span>  

### <a name="return-value---lineright"></a><span data-ttu-id="09829-521">戻り値 - lineRight</span><span class="sxs-lookup"><span data-stu-id="09829-521">Return Value - lineRight</span></span>

## <a name="method-menuitemlabel"></a><span data-ttu-id="09829-522">メソッド menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="09829-522">Method menuItemLabel</span></span>

```xpp
public str menuItemLabel([str value])
```

### <a name="parameters---menuitemlabel"></a><span data-ttu-id="09829-523">パラメーター - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="09829-523">Parameters - menuItemLabel</span></span>

<span data-ttu-id="09829-524">値</span><span class="sxs-lookup"><span data-stu-id="09829-524">value</span></span>  

### <a name="return-value---menuitemlabel"></a><span data-ttu-id="09829-525">戻り値 - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="09829-525">Return Value - menuItemLabel</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="09829-526">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="09829-526">Method menuItemName</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="09829-527">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="09829-527">Parameters - menuItemName</span></span>

<span data-ttu-id="09829-528">値</span><span class="sxs-lookup"><span data-stu-id="09829-528">value</span></span>  

### <a name="return-value---menuitemname"></a><span data-ttu-id="09829-529">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="09829-529">Return Value - menuItemName</span></span>

## <a name="method-menuitemtype"></a><span data-ttu-id="09829-530">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="09829-530">Method menuItemType</span></span>

```xpp
public MenuItemType menuItemType([MenuItemType value])
```

### <a name="parameters---menuitemtype"></a><span data-ttu-id="09829-531">パラメーター - menuItemType</span><span class="sxs-lookup"><span data-stu-id="09829-531">Parameters - menuItemType</span></span>

<span data-ttu-id="09829-532">値</span><span class="sxs-lookup"><span data-stu-id="09829-532">value</span></span>  

### <a name="return-value---menuitemtype"></a><span data-ttu-id="09829-533">戻り値 - menuItemType</span><span class="sxs-lookup"><span data-stu-id="09829-533">Return Value - menuItemType</span></span>

## <a name="method-modelfieldname"></a><span data-ttu-id="09829-534">メソッド modelFieldName</span><span class="sxs-lookup"><span data-stu-id="09829-534">Method modelFieldName</span></span>

```xpp
public str modelFieldName([str value])
```

### <a name="parameters---modelfieldname"></a><span data-ttu-id="09829-535">パラメーター - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="09829-535">Parameters - modelFieldName</span></span>

<span data-ttu-id="09829-536">値</span><span class="sxs-lookup"><span data-stu-id="09829-536">value</span></span>  

### <a name="return-value---modelfieldname"></a><span data-ttu-id="09829-537">戻り値 - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="09829-537">Return Value - modelFieldName</span></span>

## <a name="method-name"></a><span data-ttu-id="09829-538">メソッド名</span><span class="sxs-lookup"><span data-stu-id="09829-538">Method name</span></span>

<span data-ttu-id="09829-539">フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09829-539">Gets or sets the name used in code to identify a form, report, table, query, or another MSDAX application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="09829-540">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="09829-540">Parameters - name</span></span>

<span data-ttu-id="09829-541">値</span><span class="sxs-lookup"><span data-stu-id="09829-541">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="09829-542">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="09829-542">Return Value - name</span></span>

<span data-ttu-id="09829-543">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="09829-543">The name used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="09829-544">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="09829-544">Remarks - name</span></span>

<span data-ttu-id="09829-545">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="09829-545">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="09829-546">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="09829-546">Begins with a letter.</span></span>
-   <span data-ttu-id="09829-547">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="09829-547">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="09829-548">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="09829-548">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="09829-549">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="09829-549">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="09829-550">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="09829-550">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-numberoflines"></a><span data-ttu-id="09829-551">メソッド numberOfLines</span><span class="sxs-lookup"><span data-stu-id="09829-551">Method numberOfLines</span></span>

```xpp
public int numberOfLines(int height100mm)
```

### <a name="parameters---numberoflines"></a><span data-ttu-id="09829-552">パラメーター - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="09829-552">Parameters - numberOfLines</span></span>

<span data-ttu-id="09829-553">height100mm</span><span class="sxs-lookup"><span data-stu-id="09829-553">height100mm</span></span>  

### <a name="return-value---numberoflines"></a><span data-ttu-id="09829-554">戻り値 - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="09829-554">Return Value - numberOfLines</span></span>

## <a name="method-position"></a><span data-ttu-id="09829-555">メソッドの位置</span><span class="sxs-lookup"><span data-stu-id="09829-555">Method position</span></span>

```xpp
public int position([int value])
```

### <a name="parameters---position"></a><span data-ttu-id="09829-556">パラメーター - position</span><span class="sxs-lookup"><span data-stu-id="09829-556">Parameters - position</span></span>

<span data-ttu-id="09829-557">値</span><span class="sxs-lookup"><span data-stu-id="09829-557">value</span></span>  

### <a name="return-value---position"></a><span data-ttu-id="09829-558">戻り値 - position</span><span class="sxs-lookup"><span data-stu-id="09829-558">Return Value - position</span></span>

## <a name="method-previewinfo"></a><span data-ttu-id="09829-559">メソッド previewInfo</span><span class="sxs-lookup"><span data-stu-id="09829-559">Method previewInfo</span></span>

```xpp
public str previewInfo(str string)
```

### <a name="parameters---previewinfo"></a><span data-ttu-id="09829-560">パラメーター - previewInfo</span><span class="sxs-lookup"><span data-stu-id="09829-560">Parameters - previewInfo</span></span>

<span data-ttu-id="09829-561">文字列</span><span class="sxs-lookup"><span data-stu-id="09829-561">string</span></span>  

### <a name="return-value---previewinfo"></a><span data-ttu-id="09829-562">戻り値 - previewInfo</span><span class="sxs-lookup"><span data-stu-id="09829-562">Return Value - previewInfo</span></span>

## <a name="method-previewxcompensation100mm"></a><span data-ttu-id="09829-563">メソッド previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="09829-563">Method previewXCompensation100mm</span></span>

```xpp
public int previewXCompensation100mm(str string)
```

### <a name="parameters---previewxcompensation100mm"></a><span data-ttu-id="09829-564">パラメーター - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="09829-564">Parameters - previewXCompensation100mm</span></span>

<span data-ttu-id="09829-565">文字列</span><span class="sxs-lookup"><span data-stu-id="09829-565">string</span></span>  

### <a name="return-value---previewxcompensation100mm"></a><span data-ttu-id="09829-566">戻り値 - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="09829-566">Return Value - previewXCompensation100mm</span></span>

## <a name="method-right100mm"></a><span data-ttu-id="09829-567">メソッド right100mm</span><span class="sxs-lookup"><span data-stu-id="09829-567">Method right100mm</span></span>

```xpp
public int right100mm()
```

### <a name="return-value---right100mm"></a><span data-ttu-id="09829-568">戻り値 - right100mm</span><span class="sxs-lookup"><span data-stu-id="09829-568">Return Value - right100mm</span></span>

## <a name="method-right100mminclborder"></a><span data-ttu-id="09829-569">メソッド right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="09829-569">Method right100mmInclBorder</span></span>

```xpp
public int right100mmInclBorder()
```

### <a name="return-value---right100mminclborder"></a><span data-ttu-id="09829-570">戻り値 - right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="09829-570">Return Value - right100mmInclBorder</span></span>

## <a name="method-rightmarginandframe"></a><span data-ttu-id="09829-571">メソッド rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="09829-571">Method rightMarginAndFrame</span></span>

```xpp
public int rightMarginAndFrame()
```

### <a name="return-value---rightmarginandframe"></a><span data-ttu-id="09829-572">戻り値 - rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="09829-572">Return Value - rightMarginAndFrame</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="09829-573">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="09829-573">Method rightMarginMode</span></span>

```xpp
public int rightMarginMode([int value])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="09829-574">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="09829-574">Parameters - rightMarginMode</span></span>

<span data-ttu-id="09829-575">値</span><span class="sxs-lookup"><span data-stu-id="09829-575">value</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="09829-576">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="09829-576">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginstr"></a><span data-ttu-id="09829-577">メソッド rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="09829-577">Method rightMarginStr</span></span>

```xpp
public str rightMarginStr([str value])
```

### <a name="parameters---rightmarginstr"></a><span data-ttu-id="09829-578">パラメーター - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="09829-578">Parameters - rightMarginStr</span></span>

<span data-ttu-id="09829-579">値</span><span class="sxs-lookup"><span data-stu-id="09829-579">value</span></span>  

### <a name="return-value---rightmarginstr"></a><span data-ttu-id="09829-580">戻り値 - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="09829-580">Return Value - rightMarginStr</span></span>

## <a name="method-rightmarginunit"></a><span data-ttu-id="09829-581">メソッド rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="09829-581">Method rightMarginUnit</span></span>

```xpp
public Units rightMarginUnit([Units value])
```

### <a name="parameters---rightmarginunit"></a><span data-ttu-id="09829-582">パラメーター - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="09829-582">Parameters - rightMarginUnit</span></span>

<span data-ttu-id="09829-583">値</span><span class="sxs-lookup"><span data-stu-id="09829-583">value</span></span>  

### <a name="return-value---rightmarginunit"></a><span data-ttu-id="09829-584">戻り値 - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="09829-584">Return Value - rightMarginUnit</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="09829-585">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="09829-585">Method rightMarginValue</span></span>

```xpp
public Real rightMarginValue([Real value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="09829-586">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="09829-586">Parameters - rightMarginValue</span></span>

<span data-ttu-id="09829-587">値</span><span class="sxs-lookup"><span data-stu-id="09829-587">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="09829-588">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="09829-588">Return Value - rightMarginValue</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="09829-589">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="09829-589">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="09829-590">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="09829-590">Parameters - securityKey</span></span>

<span data-ttu-id="09829-591">値</span><span class="sxs-lookup"><span data-stu-id="09829-591">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="09829-592">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="09829-592">Return Value - securityKey</span></span>

## <a name="method-setheightgettext"></a><span data-ttu-id="09829-593">メソッド setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="09829-593">Method setHeightGetText</span></span>

```xpp
public str setHeightGetText(int lines, str string)
```

### <a name="parameters---setheightgettext"></a><span data-ttu-id="09829-594">パラメーター - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="09829-594">Parameters - setHeightGetText</span></span>

<span data-ttu-id="09829-595">明細行</span><span class="sxs-lookup"><span data-stu-id="09829-595">lines</span></span>  

<!-- -->

<span data-ttu-id="09829-596">文字列</span><span class="sxs-lookup"><span data-stu-id="09829-596">string</span></span>  

### <a name="return-value---setheightgettext"></a><span data-ttu-id="09829-597">戻り値 - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="09829-597">Return Value - setHeightGetText</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="09829-598">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="09829-598">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="09829-599">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="09829-599">Parameters - showLabel</span></span>

<span data-ttu-id="09829-600">値</span><span class="sxs-lookup"><span data-stu-id="09829-600">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="09829-601">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="09829-601">Return Value - showLabel</span></span>

## <a name="method-thickness"></a><span data-ttu-id="09829-602">メソッド thickness</span><span class="sxs-lookup"><span data-stu-id="09829-602">Method thickness</span></span>

```xpp
public LineThickness thickness([LineThickness value])
```

### <a name="parameters---thickness"></a><span data-ttu-id="09829-603">パラメーター - thickness</span><span class="sxs-lookup"><span data-stu-id="09829-603">Parameters - thickness</span></span>

<span data-ttu-id="09829-604">値</span><span class="sxs-lookup"><span data-stu-id="09829-604">value</span></span>  

### <a name="return-value---thickness"></a><span data-ttu-id="09829-605">戻り値 - thickness</span><span class="sxs-lookup"><span data-stu-id="09829-605">Return Value - thickness</span></span>

## <a name="method-top100mm"></a><span data-ttu-id="09829-606">メソッド top100mm</span><span class="sxs-lookup"><span data-stu-id="09829-606">Method top100mm</span></span>

```xpp
public int top100mm([int topExclBorder])
```

### <a name="parameters---top100mm"></a><span data-ttu-id="09829-607">パラメーター - top100mm</span><span class="sxs-lookup"><span data-stu-id="09829-607">Parameters - top100mm</span></span>

<span data-ttu-id="09829-608">topExclBorder</span><span class="sxs-lookup"><span data-stu-id="09829-608">topExclBorder</span></span>  

### <a name="return-value---top100mm"></a><span data-ttu-id="09829-609">戻り値 - top100mm</span><span class="sxs-lookup"><span data-stu-id="09829-609">Return Value - top100mm</span></span>

## <a name="method-top100mminclborder"></a><span data-ttu-id="09829-610">メソッド top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="09829-610">Method top100mmInclBorder</span></span>

```xpp
public int top100mmInclBorder([int topInclBorder])
```

### <a name="parameters---top100mminclborder"></a><span data-ttu-id="09829-611">パラメーター - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="09829-611">Parameters - top100mmInclBorder</span></span>

<span data-ttu-id="09829-612">topInclBorder</span><span class="sxs-lookup"><span data-stu-id="09829-612">topInclBorder</span></span>  

### <a name="return-value---top100mminclborder"></a><span data-ttu-id="09829-613">戻り値 - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="09829-613">Return Value - top100mmInclBorder</span></span>

## <a name="method-topmarginandframe"></a><span data-ttu-id="09829-614">メソッド topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="09829-614">Method topMarginAndFrame</span></span>

```xpp
public int topMarginAndFrame()
```

### <a name="return-value---topmarginandframe"></a><span data-ttu-id="09829-615">戻り値 - topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="09829-615">Return Value - topMarginAndFrame</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="09829-616">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="09829-616">Method topMarginMode</span></span>

```xpp
public int topMarginMode([int value])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="09829-617">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="09829-617">Parameters - topMarginMode</span></span>

<span data-ttu-id="09829-618">値</span><span class="sxs-lookup"><span data-stu-id="09829-618">value</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="09829-619">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="09829-619">Return Value - topMarginMode</span></span>

## <a name="method-topmarginstr"></a><span data-ttu-id="09829-620">メソッド topMarginStr</span><span class="sxs-lookup"><span data-stu-id="09829-620">Method topMarginStr</span></span>

```xpp
public str topMarginStr([str value])
```

### <a name="parameters---topmarginstr"></a><span data-ttu-id="09829-621">パラメーター - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="09829-621">Parameters - topMarginStr</span></span>

<span data-ttu-id="09829-622">値</span><span class="sxs-lookup"><span data-stu-id="09829-622">value</span></span>  

### <a name="return-value---topmarginstr"></a><span data-ttu-id="09829-623">戻り値 - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="09829-623">Return Value - topMarginStr</span></span>

## <a name="method-topmarginunit"></a><span data-ttu-id="09829-624">メソッド topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="09829-624">Method topMarginUnit</span></span>

```xpp
public Units topMarginUnit([Units value])
```

### <a name="parameters---topmarginunit"></a><span data-ttu-id="09829-625">パラメーター - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="09829-625">Parameters - topMarginUnit</span></span>

<span data-ttu-id="09829-626">値</span><span class="sxs-lookup"><span data-stu-id="09829-626">value</span></span>  

### <a name="return-value---topmarginunit"></a><span data-ttu-id="09829-627">戻り値 - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="09829-627">Return Value - topMarginUnit</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="09829-628">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="09829-628">Method topMarginValue</span></span>

```xpp
public Real topMarginValue([Real value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="09829-629">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="09829-629">Parameters - topMarginValue</span></span>

<span data-ttu-id="09829-630">値</span><span class="sxs-lookup"><span data-stu-id="09829-630">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="09829-631">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="09829-631">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="09829-632">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="09829-632">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="09829-633">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="09829-633">Parameters - topMode</span></span>

<span data-ttu-id="09829-634">値</span><span class="sxs-lookup"><span data-stu-id="09829-634">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="09829-635">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="09829-635">Return Value - topMode</span></span>

## <a name="method-topstr"></a><span data-ttu-id="09829-636">メソッド topStr</span><span class="sxs-lookup"><span data-stu-id="09829-636">Method topStr</span></span>

```xpp
public str topStr([str value])
```

### <a name="parameters---topstr"></a><span data-ttu-id="09829-637">パラメーター - topStr</span><span class="sxs-lookup"><span data-stu-id="09829-637">Parameters - topStr</span></span>

<span data-ttu-id="09829-638">値</span><span class="sxs-lookup"><span data-stu-id="09829-638">value</span></span>  

### <a name="return-value---topstr"></a><span data-ttu-id="09829-639">戻り値 - topStr</span><span class="sxs-lookup"><span data-stu-id="09829-639">Return Value - topStr</span></span>

## <a name="method-topunit"></a><span data-ttu-id="09829-640">メソッド topUnit</span><span class="sxs-lookup"><span data-stu-id="09829-640">Method topUnit</span></span>

```xpp
public Units topUnit([Units value])
```

### <a name="parameters---topunit"></a><span data-ttu-id="09829-641">パラメーター - topUnit</span><span class="sxs-lookup"><span data-stu-id="09829-641">Parameters - topUnit</span></span>

<span data-ttu-id="09829-642">値</span><span class="sxs-lookup"><span data-stu-id="09829-642">value</span></span>  

### <a name="return-value---topunit"></a><span data-ttu-id="09829-643">戻り値 - topUnit</span><span class="sxs-lookup"><span data-stu-id="09829-643">Return Value - topUnit</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="09829-644">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="09829-644">Method topValue</span></span>

```xpp
public Real topValue([Real value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="09829-645">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="09829-645">Parameters - topValue</span></span>

<span data-ttu-id="09829-646">値</span><span class="sxs-lookup"><span data-stu-id="09829-646">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="09829-647">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="09829-647">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="09829-648">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="09829-648">Method type</span></span>

```xpp
public ShapeType type([ShapeType value])
```

### <a name="parameters---type"></a><span data-ttu-id="09829-649">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="09829-649">Parameters - type</span></span>

<span data-ttu-id="09829-650">値</span><span class="sxs-lookup"><span data-stu-id="09829-650">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="09829-651">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="09829-651">Return Value - type</span></span>

## <a name="method-visible"></a><span data-ttu-id="09829-652">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="09829-652">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="09829-653">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="09829-653">Parameters - visible</span></span>

<span data-ttu-id="09829-654">値</span><span class="sxs-lookup"><span data-stu-id="09829-654">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="09829-655">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="09829-655">Return Value - visible</span></span>

## <a name="method-webmenuitemname"></a><span data-ttu-id="09829-656">メソッド webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="09829-656">Method webMenuItemName</span></span>

```xpp
public str webMenuItemName([str value])
```

### <a name="parameters---webmenuitemname"></a><span data-ttu-id="09829-657">パラメーター - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="09829-657">Parameters - webMenuItemName</span></span>

<span data-ttu-id="09829-658">値</span><span class="sxs-lookup"><span data-stu-id="09829-658">value</span></span>  

### <a name="return-value---webmenuitemname"></a><span data-ttu-id="09829-659">戻り値 - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="09829-659">Return Value - webMenuItemName</span></span>

## <a name="method-webmenuitemtype"></a><span data-ttu-id="09829-660">メソッド webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="09829-660">Method webMenuItemType</span></span>

```xpp
public WebMenuItemType webMenuItemType([WebMenuItemType value])
```

### <a name="parameters---webmenuitemtype"></a><span data-ttu-id="09829-661">パラメーター - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="09829-661">Parameters - webMenuItemType</span></span>

<span data-ttu-id="09829-662">値</span><span class="sxs-lookup"><span data-stu-id="09829-662">value</span></span>  

### <a name="return-value---webmenuitemtype"></a><span data-ttu-id="09829-663">戻り値 - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="09829-663">Return Value - webMenuItemType</span></span>

## <a name="method-webtarget"></a><span data-ttu-id="09829-664">メソッド webTarget</span><span class="sxs-lookup"><span data-stu-id="09829-664">Method webTarget</span></span>

```xpp
public str webTarget([str value])
```

### <a name="parameters---webtarget"></a><span data-ttu-id="09829-665">パラメーター - webTarget</span><span class="sxs-lookup"><span data-stu-id="09829-665">Parameters - webTarget</span></span>

<span data-ttu-id="09829-666">値</span><span class="sxs-lookup"><span data-stu-id="09829-666">value</span></span>  

### <a name="return-value---webtarget"></a><span data-ttu-id="09829-667">戻り値 - webTarget</span><span class="sxs-lookup"><span data-stu-id="09829-667">Return Value - webTarget</span></span>

## <a name="method-width100mm"></a><span data-ttu-id="09829-668">メソッド width100mm</span><span class="sxs-lookup"><span data-stu-id="09829-668">Method width100mm</span></span>

```xpp
public int width100mm([int widthExclBorder])
```

### <a name="parameters---width100mm"></a><span data-ttu-id="09829-669">パラメーター - width100mm</span><span class="sxs-lookup"><span data-stu-id="09829-669">Parameters - width100mm</span></span>

<span data-ttu-id="09829-670">widthExclBorder</span><span class="sxs-lookup"><span data-stu-id="09829-670">widthExclBorder</span></span>  

### <a name="return-value---width100mm"></a><span data-ttu-id="09829-671">戻り値 - width100mm</span><span class="sxs-lookup"><span data-stu-id="09829-671">Return Value - width100mm</span></span>

## <a name="method-width100mminclborder"></a><span data-ttu-id="09829-672">メソッド width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="09829-672">Method width100mmInclBorder</span></span>

```xpp
public int width100mmInclBorder([int widthInclBorder])
```

### <a name="parameters---width100mminclborder"></a><span data-ttu-id="09829-673">パラメーター - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="09829-673">Parameters - width100mmInclBorder</span></span>

<span data-ttu-id="09829-674">widthInclBorder</span><span class="sxs-lookup"><span data-stu-id="09829-674">widthInclBorder</span></span>  

### <a name="return-value---width100mminclborder"></a><span data-ttu-id="09829-675">戻り値 - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="09829-675">Return Value - width100mmInclBorder</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="09829-676">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="09829-676">Method widthMode</span></span>

<span data-ttu-id="09829-677">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09829-677">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="09829-678">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="09829-678">Parameters - widthMode</span></span>

<span data-ttu-id="09829-679">値</span><span class="sxs-lookup"><span data-stu-id="09829-679">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="09829-680">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="09829-680">Return Value - widthMode</span></span>

<span data-ttu-id="09829-681">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="09829-681">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="09829-682">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="09829-682">Remarks - widthMode</span></span>

<span data-ttu-id="09829-683">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="09829-683">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="09829-684">モード。</span><span class="sxs-lookup"><span data-stu-id="09829-684">Mode.</span></span>         | <span data-ttu-id="09829-685">幅計算。</span><span class="sxs-lookup"><span data-stu-id="09829-685">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="09829-686">正確。</span><span class="sxs-lookup"><span data-stu-id="09829-686">Exact.</span></span>        | <span data-ttu-id="09829-687">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="09829-687">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="09829-688">自動。</span><span class="sxs-lookup"><span data-stu-id="09829-688">Auto.</span></span>         | <span data-ttu-id="09829-689">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="09829-689">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="09829-690">列の幅。</span><span class="sxs-lookup"><span data-stu-id="09829-690">Column width.</span></span> | <span data-ttu-id="09829-691">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="09829-691">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="09829-692">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="09829-692">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthofstring100mm"></a><span data-ttu-id="09829-693">メソッド widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="09829-693">Method widthOfString100mm</span></span>

```xpp
public int widthOfString100mm(str string)
```

### <a name="parameters---widthofstring100mm"></a><span data-ttu-id="09829-694">パラメーター - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="09829-694">Parameters - widthOfString100mm</span></span>

<span data-ttu-id="09829-695">文字列</span><span class="sxs-lookup"><span data-stu-id="09829-695">string</span></span>  

### <a name="return-value---widthofstring100mm"></a><span data-ttu-id="09829-696">戻り値 - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="09829-696">Return Value - widthOfString100mm</span></span>

## <a name="method-widthstr"></a><span data-ttu-id="09829-697">メソッド widthStr</span><span class="sxs-lookup"><span data-stu-id="09829-697">Method widthStr</span></span>

```xpp
public str widthStr([str value])
```

### <a name="parameters---widthstr"></a><span data-ttu-id="09829-698">パラメーター - widthStr</span><span class="sxs-lookup"><span data-stu-id="09829-698">Parameters - widthStr</span></span>

<span data-ttu-id="09829-699">値</span><span class="sxs-lookup"><span data-stu-id="09829-699">value</span></span>  

### <a name="return-value---widthstr"></a><span data-ttu-id="09829-700">戻り値 - widthStr</span><span class="sxs-lookup"><span data-stu-id="09829-700">Return Value - widthStr</span></span>

## <a name="method-widthunit"></a><span data-ttu-id="09829-701">メソッド widthUnit</span><span class="sxs-lookup"><span data-stu-id="09829-701">Method widthUnit</span></span>

```xpp
public Units widthUnit([Units value])
```

### <a name="parameters---widthunit"></a><span data-ttu-id="09829-702">パラメーター - widthUnit</span><span class="sxs-lookup"><span data-stu-id="09829-702">Parameters - widthUnit</span></span>

<span data-ttu-id="09829-703">値</span><span class="sxs-lookup"><span data-stu-id="09829-703">value</span></span>  

### <a name="return-value---widthunit"></a><span data-ttu-id="09829-704">戻り値 - widthUnit</span><span class="sxs-lookup"><span data-stu-id="09829-704">Return Value - widthUnit</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="09829-705">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="09829-705">Method widthValue</span></span>

<span data-ttu-id="09829-706">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09829-706">Gets or sets the width of the control.</span></span>

```xpp
public Real widthValue([Real value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="09829-707">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="09829-707">Parameters - widthValue</span></span>

<span data-ttu-id="09829-708">値</span><span class="sxs-lookup"><span data-stu-id="09829-708">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="09829-709">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="09829-709">Return Value - widthValue</span></span>

<span data-ttu-id="09829-710">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="09829-710">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="09829-711">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="09829-711">Remarks - widthValue</span></span>

<span data-ttu-id="09829-712">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="09829-712">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="09829-713">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="09829-713">Method bottomMargin</span></span>

```xpp
public void bottomMargin(Real value, Units unit)
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="09829-714">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="09829-714">Parameters - bottomMargin</span></span>

<span data-ttu-id="09829-715">値</span><span class="sxs-lookup"><span data-stu-id="09829-715">value</span></span>  

<!-- -->

<span data-ttu-id="09829-716">単位</span><span class="sxs-lookup"><span data-stu-id="09829-716">unit</span></span>  

## <a name="method-left"></a><span data-ttu-id="09829-717">メソッド left</span><span class="sxs-lookup"><span data-stu-id="09829-717">Method left</span></span>

```xpp
public void left(Real value, Units unit)
```

### <a name="parameters---left"></a><span data-ttu-id="09829-718">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="09829-718">Parameters - left</span></span>

<span data-ttu-id="09829-719">値</span><span class="sxs-lookup"><span data-stu-id="09829-719">value</span></span>  

<!-- -->

<span data-ttu-id="09829-720">単位</span><span class="sxs-lookup"><span data-stu-id="09829-720">unit</span></span>  

## <a name="method-top"></a><span data-ttu-id="09829-721">メソッド top</span><span class="sxs-lookup"><span data-stu-id="09829-721">Method top</span></span>

```xpp
public void top(Real value, Units unit)
```

### <a name="parameters---top"></a><span data-ttu-id="09829-722">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="09829-722">Parameters - top</span></span>

<span data-ttu-id="09829-723">値</span><span class="sxs-lookup"><span data-stu-id="09829-723">value</span></span>  

<!-- -->

<span data-ttu-id="09829-724">単位</span><span class="sxs-lookup"><span data-stu-id="09829-724">unit</span></span>  

## <a name="method-labelwidth"></a><span data-ttu-id="09829-725">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="09829-725">Method labelWidth</span></span>

```xpp
public void labelWidth(Real value, Units unit)
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="09829-726">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="09829-726">Parameters - labelWidth</span></span>

<span data-ttu-id="09829-727">値</span><span class="sxs-lookup"><span data-stu-id="09829-727">value</span></span>  

<!-- -->

<span data-ttu-id="09829-728">単位</span><span class="sxs-lookup"><span data-stu-id="09829-728">unit</span></span>  

## <a name="method-height"></a><span data-ttu-id="09829-729">メソッド height</span><span class="sxs-lookup"><span data-stu-id="09829-729">Method height</span></span>

<span data-ttu-id="09829-730">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09829-730">Gets or sets the height of the control.</span></span>

```xpp
public void height(Real value, Units unit)
```

### <a name="parameters---height"></a><span data-ttu-id="09829-731">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="09829-731">Parameters - height</span></span>

<span data-ttu-id="09829-732">値</span><span class="sxs-lookup"><span data-stu-id="09829-732">value</span></span>  

<!-- -->

<span data-ttu-id="09829-733">単位</span><span class="sxs-lookup"><span data-stu-id="09829-733">unit</span></span>  

### <a name="remarks---height"></a><span data-ttu-id="09829-734">備考 - height</span><span class="sxs-lookup"><span data-stu-id="09829-734">Remarks - height</span></span>

<span data-ttu-id="09829-735">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="09829-735">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="09829-736">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="09829-736">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="09829-737">モード。</span><span class="sxs-lookup"><span data-stu-id="09829-737">Mode.</span></span>            | <span data-ttu-id="09829-738">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="09829-738">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="09829-739">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="09829-739">-1 Exact.</span></span>        | <span data-ttu-id="09829-740">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="09829-740">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="09829-741">0 自動。</span><span class="sxs-lookup"><span data-stu-id="09829-741">0 Auto.</span></span>          | <span data-ttu-id="09829-742">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="09829-742">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="09829-743">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="09829-743">1 Column height.</span></span> | <span data-ttu-id="09829-744">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="09829-744">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="09829-745">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="09829-745">The height and height calculation mode can be set separately.</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="09829-746">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="09829-746">Method leftMargin</span></span>

```xpp
public void leftMargin(Real value, Units unit)
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="09829-747">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="09829-747">Parameters - leftMargin</span></span>

<span data-ttu-id="09829-748">値</span><span class="sxs-lookup"><span data-stu-id="09829-748">value</span></span>  

<!-- -->

<span data-ttu-id="09829-749">単位</span><span class="sxs-lookup"><span data-stu-id="09829-749">unit</span></span>  

## <a name="method-rightmargin"></a><span data-ttu-id="09829-750">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="09829-750">Method rightMargin</span></span>

```xpp
public void rightMargin(Real value, Units unit)
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="09829-751">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="09829-751">Parameters - rightMargin</span></span>

<span data-ttu-id="09829-752">値</span><span class="sxs-lookup"><span data-stu-id="09829-752">value</span></span>  

<!-- -->

<span data-ttu-id="09829-753">単位</span><span class="sxs-lookup"><span data-stu-id="09829-753">unit</span></span>  

## <a name="method-hide"></a><span data-ttu-id="09829-754">メソッド hide</span><span class="sxs-lookup"><span data-stu-id="09829-754">Method hide</span></span>

```xpp
public void hide()
```

## <a name="method-topmargin"></a><span data-ttu-id="09829-755">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="09829-755">Method topMargin</span></span>

```xpp
public void topMargin(Real value, Units unit)
```

### <a name="parameters---topmargin"></a><span data-ttu-id="09829-756">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="09829-756">Parameters - topMargin</span></span>

<span data-ttu-id="09829-757">値</span><span class="sxs-lookup"><span data-stu-id="09829-757">value</span></span>  

<!-- -->

<span data-ttu-id="09829-758">単位</span><span class="sxs-lookup"><span data-stu-id="09829-758">unit</span></span>  

## <a name="method-show"></a><span data-ttu-id="09829-759">メソッド show</span><span class="sxs-lookup"><span data-stu-id="09829-759">Method show</span></span>

```xpp
public void show()
```

## <a name="method-width"></a><span data-ttu-id="09829-760">メソッド width</span><span class="sxs-lookup"><span data-stu-id="09829-760">Method width</span></span>

<span data-ttu-id="09829-761">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="09829-761">Gets or sets the width of the control.</span></span>

```xpp
public void width(Real value, Units unit)
```

### <a name="parameters---width"></a><span data-ttu-id="09829-762">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="09829-762">Parameters - width</span></span>

<span data-ttu-id="09829-763">値</span><span class="sxs-lookup"><span data-stu-id="09829-763">value</span></span>  

<!-- -->

<span data-ttu-id="09829-764">単位</span><span class="sxs-lookup"><span data-stu-id="09829-764">unit</span></span>  

### <a name="remarks---width"></a><span data-ttu-id="09829-765">備考 - width</span><span class="sxs-lookup"><span data-stu-id="09829-765">Remarks - width</span></span>

<span data-ttu-id="09829-766">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="09829-766">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="09829-767">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="09829-767">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="09829-768">モード。</span><span class="sxs-lookup"><span data-stu-id="09829-768">Mode.</span></span>           | <span data-ttu-id="09829-769">幅計算。</span><span class="sxs-lookup"><span data-stu-id="09829-769">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="09829-770">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="09829-770">-1 Exact.</span></span>       | <span data-ttu-id="09829-771">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="09829-771">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="09829-772">0 自動。</span><span class="sxs-lookup"><span data-stu-id="09829-772">0 Auto.</span></span>         | <span data-ttu-id="09829-773">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="09829-773">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="09829-774">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="09829-774">1 Column width.</span></span> | <span data-ttu-id="09829-775">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="09829-775">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="09829-776">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="09829-776">The width and width calculation mode can be set separately.</span></span>

