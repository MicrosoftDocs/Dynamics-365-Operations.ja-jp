---
title: ReportDateControl クラス
description: このトピックでは、ReportDateControl クラスについて説明します。
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
ms.openlocfilehash: 13ba41602114ee8fa8fbce3475ddb8419f9e6d28
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502848"
---
# <a name="class-reportdatecontrol"></a><span data-ttu-id="b32c3-103">クラス ReportDateControl</span><span class="sxs-lookup"><span data-stu-id="b32c3-103">Class ReportDateControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ReportDateControl extends ReportControl
```

<span data-ttu-id="b32c3-104">ReportDateControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="b32c3-104">The ReportDateControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="b32c3-105">備考</span><span class="sxs-lookup"><span data-stu-id="b32c3-105">Remarks</span></span>

<span data-ttu-id="b32c3-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="b32c3-107">例</span><span class="sxs-lookup"><span data-stu-id="b32c3-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="b32c3-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="b32c3-108">Methods</span></span>

| <span data-ttu-id="b32c3-109">方法</span><span class="sxs-lookup"><span data-stu-id="b32c3-109">Method</span></span>                                                                   | <span data-ttu-id="b32c3-110">説明</span><span class="sxs-lookup"><span data-stu-id="b32c3-110">Description</span></span>                                                                                                                               |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b32c3-111">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-111">public int alignment(\[int value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="b32c3-112">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-112">public int arrayIndex(\[int value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="b32c3-113">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-113">public boolean autoDeclaration(\[boolean value\])</span></span>                        | <span data-ttu-id="b32c3-114">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-114">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                        |
| <span data-ttu-id="b32c3-115">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-115">public int backgroundColor(\[int value\])</span></span>                                | <span data-ttu-id="b32c3-116">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-116">Gets or sets the background color of the control.</span></span>                                                                                         |
| <span data-ttu-id="b32c3-117">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-117">public int backStyle(\[int value\])</span></span>                                      | <span data-ttu-id="b32c3-118">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-118">Determines whether the control background can be transparent.</span></span>                                                                            |
| <span data-ttu-id="b32c3-119">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-119">public int bold(\[int value\])</span></span>                                           | <span data-ttu-id="b32c3-120">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-120">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                               |
| <span data-ttu-id="b32c3-121">public int bottomMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="b32c3-121">public int bottomMarginAndFrame()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="b32c3-122">public int bottomMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-122">public int bottomMarginMode(\[int value\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="b32c3-123">public str bottomMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-123">public str bottomMarginStr(\[str value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="b32c3-124">public Units bottomMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-124">public Units bottomMarginUnit(\[Units value\])</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="b32c3-125">public Real bottomMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-125">public Real bottomMarginValue(\[Real value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="b32c3-126">public int changeLabelCase(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-126">public int changeLabelCase(\[int value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="b32c3-127">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-127">public int characterSet(\[int value\])</span></span>                                   | <span data-ttu-id="b32c3-128">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-128">Gets or sets the character set of the font.</span></span>                                                                                               |
| <span data-ttu-id="b32c3-129">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-129">public int colorScheme(\[int value\])</span></span>                                    | <span data-ttu-id="b32c3-130">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-130">Gets or sets the color scheme of the control.</span></span>                                                                                             |
| <span data-ttu-id="b32c3-131">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-131">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="b32c3-132">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-132">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                       |
| <span data-ttu-id="b32c3-133">public ReportFieldType controlType()</span><span class="sxs-lookup"><span data-stu-id="b32c3-133">public ReportFieldType controlType()</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="b32c3-134">public str cssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-134">public str cssClass(\[str value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="b32c3-135">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-135">public FieldId dataField(\[FieldId value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="b32c3-136">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-136">public str dataMethod(\[str value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="b32c3-137">public int dateDay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-137">public int dateDay(\[int value\])</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="b32c3-138">public int dateFormat(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-138">public int dateFormat(\[int value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="b32c3-139">public int dateMonth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-139">public int dateMonth(\[int value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="b32c3-140">public int dateSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-140">public int dateSeparator(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="b32c3-141">public int dateYear(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-141">public int dateYear(\[int value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="b32c3-142">public int delete()</span><span class="sxs-lookup"><span data-stu-id="b32c3-142">public int delete()</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="b32c3-143">public str effectiveFont()</span><span class="sxs-lookup"><span data-stu-id="b32c3-143">public str effectiveFont()</span></span>                                               |                                                                                                                                           |
| <span data-ttu-id="b32c3-144">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-144">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>         |                                                                                                                                           |
| <span data-ttu-id="b32c3-145">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-145">public str font(\[str value\])</span></span>                                           | <span data-ttu-id="b32c3-146">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-146">Gets or sets the name of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="b32c3-147">public str fontInfoPrinter()</span><span class="sxs-lookup"><span data-stu-id="b32c3-147">public str fontInfoPrinter()</span></span>                                             |                                                                                                                                           |
| <span data-ttu-id="b32c3-148">public int fontInfoPrinterAscent()</span><span class="sxs-lookup"><span data-stu-id="b32c3-148">public int fontInfoPrinterAscent()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="b32c3-149">public int fontInfoPrinterDescent()</span><span class="sxs-lookup"><span data-stu-id="b32c3-149">public int fontInfoPrinterDescent()</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="b32c3-150">public int fontInfoPrinterExtLead()</span><span class="sxs-lookup"><span data-stu-id="b32c3-150">public int fontInfoPrinterExtLead()</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="b32c3-151">public int fontInfoPrinterHeight()</span><span class="sxs-lookup"><span data-stu-id="b32c3-151">public int fontInfoPrinterHeight()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="b32c3-152">public int fontInfoPrinterIntLead()</span><span class="sxs-lookup"><span data-stu-id="b32c3-152">public int fontInfoPrinterIntLead()</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="b32c3-153">public str fontInfoScreen()</span><span class="sxs-lookup"><span data-stu-id="b32c3-153">public str fontInfoScreen()</span></span>                                              |                                                                                                                                           |
| <span data-ttu-id="b32c3-154">public int fontInfoScreenAscent()</span><span class="sxs-lookup"><span data-stu-id="b32c3-154">public int fontInfoScreenAscent()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="b32c3-155">public int fontInfoScreenDescent()</span><span class="sxs-lookup"><span data-stu-id="b32c3-155">public int fontInfoScreenDescent()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="b32c3-156">public int fontInfoScreenExtLead()</span><span class="sxs-lookup"><span data-stu-id="b32c3-156">public int fontInfoScreenExtLead()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="b32c3-157">public int fontInfoScreenHeight()</span><span class="sxs-lookup"><span data-stu-id="b32c3-157">public int fontInfoScreenHeight()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="b32c3-158">public int fontInfoScreenIntLead()</span><span class="sxs-lookup"><span data-stu-id="b32c3-158">public int fontInfoScreenIntLead()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="b32c3-159">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-159">public int fontSize(\[int value\])</span></span>                                       | <span data-ttu-id="b32c3-160">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-160">Gets or sets the size of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="b32c3-161">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-161">public int foregroundColor(\[int value\])</span></span>                                | <span data-ttu-id="b32c3-162">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-162">Gets or sets the text color for the control to use.</span></span>                                                                                       |
| <span data-ttu-id="b32c3-163">public int height100mm(\[int heightExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-163">public int height100mm(\[int heightExclBorder\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="b32c3-164">public int height100mmInclBorder(\[int heightInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-164">public int height100mmInclBorder(\[int heightInclBorder\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="b32c3-165">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-165">public int heightMode(\[int value\])</span></span>                                     | <span data-ttu-id="b32c3-166">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-166">Gets or sets a calculation mode for the height of the control.</span></span>                                                                            |
| <span data-ttu-id="b32c3-167">public int heightOfWordWrappedString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="b32c3-167">public int heightOfWordWrappedString100mm(str string)</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="b32c3-168">public str heightStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-168">public str heightStr(\[str value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="b32c3-169">public Units heightUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-169">public Units heightUnit(\[Units value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="b32c3-170">public Real heightValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-170">public Real heightValue(\[Real value\])</span></span>                                  | <span data-ttu-id="b32c3-171">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-171">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="b32c3-172">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-172">public boolean italic(\[boolean value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="b32c3-173">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-173">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="b32c3-174">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-174">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="b32c3-175">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-175">public int labelBold(\[int value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="b32c3-176">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-176">public int labelCharacterSet(\[int value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="b32c3-177">public str labelCssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-177">public str labelCssClass(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="b32c3-178">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-178">public str labelFont(\[str value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="b32c3-179">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-179">public int labelFontSize(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="b32c3-180">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-180">public boolean labelItalic(\[boolean value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="b32c3-181">public LineType labelLineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-181">public LineType labelLineBelow(\[LineType value\])</span></span>                       |                                                                                                                                           |
| <span data-ttu-id="b32c3-182">public LineThickness labelLineThickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-182">public LineThickness labelLineThickness(\[LineThickness value\])</span></span>         |                                                                                                                                           |
| <span data-ttu-id="b32c3-183">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-183">public int labelPosition(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="b32c3-184">public int labelTabLeader(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-184">public int labelTabLeader(\[int value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="b32c3-185">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-185">public boolean labelUnderline(\[boolean value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="b32c3-186">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-186">public int labelWidthMode(\[int value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="b32c3-187">public str labelWidthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-187">public str labelWidthStr(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="b32c3-188">public Units labelWidthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-188">public Units labelWidthUnit(\[Units value\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="b32c3-189">public Real labelWidthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-189">public Real labelWidthValue(\[Real value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="b32c3-190">public int left100mm(\[int leftExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-190">public int left100mm(\[int leftExclBorder\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="b32c3-191">public int left100mmInclBorder(\[int leftInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-191">public int left100mmInclBorder(\[int leftInclBorder\])</span></span>                   |                                                                                                                                           |
| <span data-ttu-id="b32c3-192">public int leftMarginAnFrame()</span><span class="sxs-lookup"><span data-stu-id="b32c3-192">public int leftMarginAnFrame()</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="b32c3-193">public int leftMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-193">public int leftMarginMode(\[int value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="b32c3-194">public str leftMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-194">public str leftMarginStr(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="b32c3-195">public Units leftMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-195">public Units leftMarginUnit(\[Units value\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="b32c3-196">public Real leftMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-196">public Real leftMarginValue(\[Real value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="b32c3-197">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-197">public int leftMode(\[int value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="b32c3-198">public str leftStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-198">public str leftStr(\[str value\])</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="b32c3-199">public Units leftUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-199">public Units leftUnit(\[Units value\])</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="b32c3-200">public Real leftValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-200">public Real leftValue(\[Real value\])</span></span>                                    |                                                                                                                                           |
| <span data-ttu-id="b32c3-201">public LineType lineAbove(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-201">public LineType lineAbove(\[LineType value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="b32c3-202">public LineType lineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-202">public LineType lineBelow(\[LineType value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="b32c3-203">public LineType lineLeft(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-203">public LineType lineLeft(\[LineType value\])</span></span>                             | <span data-ttu-id="b32c3-204">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-204">Gets or sets the type of line that is used as the left border of a section.</span></span>                                                               |
| <span data-ttu-id="b32c3-205">public LineType lineRight(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-205">public LineType lineRight(\[LineType value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="b32c3-206">public str menuItemLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-206">public str menuItemLabel(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="b32c3-207">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-207">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="b32c3-208">public MenuItemType menuItemType(\[MenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-208">public MenuItemType menuItemType(\[MenuItemType value\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="b32c3-209">public str modelFieldName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-209">public str modelFieldName(\[str value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="b32c3-210">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-210">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="b32c3-211">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-211">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="b32c3-212">public int numberOfLines(int height100mm)</span><span class="sxs-lookup"><span data-stu-id="b32c3-212">public int numberOfLines(int height100mm)</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="b32c3-213">public int position(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-213">public int position(\[int value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="b32c3-214">public str previewInfo(str string)</span><span class="sxs-lookup"><span data-stu-id="b32c3-214">public str previewInfo(str string)</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="b32c3-215">public int previewXCompensation100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="b32c3-215">public int previewXCompensation100mm(str string)</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="b32c3-216">public int right100mm()</span><span class="sxs-lookup"><span data-stu-id="b32c3-216">public int right100mm()</span></span>                                                  |                                                                                                                                           |
| <span data-ttu-id="b32c3-217">public int right100mmInclBorder()</span><span class="sxs-lookup"><span data-stu-id="b32c3-217">public int right100mmInclBorder()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="b32c3-218">public int rightMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="b32c3-218">public int rightMarginAndFrame()</span></span>                                         |                                                                                                                                           |
| <span data-ttu-id="b32c3-219">public int rightMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-219">public int rightMarginMode(\[int value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="b32c3-220">public str rightMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-220">public str rightMarginStr(\[str value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="b32c3-221">public Units rightMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-221">public Units rightMarginUnit(\[Units value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="b32c3-222">public Real rightMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-222">public Real rightMarginValue(\[Real value\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="b32c3-223">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-223">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                                           |
| <span data-ttu-id="b32c3-224">public str setHeightGetText(int lines, str string)</span><span class="sxs-lookup"><span data-stu-id="b32c3-224">public str setHeightGetText(int lines, str string)</span></span>                       |                                                                                                                                           |
| <span data-ttu-id="b32c3-225">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-225">public boolean showLabel(\[boolean value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="b32c3-226">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-226">public TableId table(\[TableId value\])</span></span>                                  | <span data-ttu-id="b32c3-227">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-227">Gets or sets the table ID associated with the object.</span></span>                                                                                     |
| <span data-ttu-id="b32c3-228">public LineThickness thickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-228">public LineThickness thickness(\[LineThickness value\])</span></span>                  |                                                                                                                                           |
| <span data-ttu-id="b32c3-229">public int top100mm(\[int topExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-229">public int top100mm(\[int topExclBorder\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="b32c3-230">public int top100mmInclBorder(\[int topInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-230">public int top100mmInclBorder(\[int topInclBorder\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="b32c3-231">public int topMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="b32c3-231">public int topMarginAndFrame()</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="b32c3-232">public int topMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-232">public int topMarginMode(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="b32c3-233">public str topMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-233">public str topMarginStr(\[str value\])</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="b32c3-234">public Units topMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-234">public Units topMarginUnit(\[Units value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="b32c3-235">public Real topMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-235">public Real topMarginValue(\[Real value\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="b32c3-236">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-236">public int topMode(\[int value\])</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="b32c3-237">public str topStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-237">public str topStr(\[str value\])</span></span>                                         |                                                                                                                                           |
| <span data-ttu-id="b32c3-238">public Units topUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-238">public Units topUnit(\[Units value\])</span></span>                                    |                                                                                                                                           |
| <span data-ttu-id="b32c3-239">public Real topValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-239">public Real topValue(\[Real value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="b32c3-240">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-240">public boolean underline(\[boolean value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="b32c3-241">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-241">public boolean visible(\[boolean value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="b32c3-242">public str webMenuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-242">public str webMenuItemName(\[str value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="b32c3-243">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-243">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span></span>        |                                                                                                                                           |
| <span data-ttu-id="b32c3-244">public str webTarget(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-244">public str webTarget(\[str value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="b32c3-245">public int width100mm(\[int widthExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-245">public int width100mm(\[int widthExclBorder\])</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="b32c3-246">public int width100mmInclBorder(\[int widthInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-246">public int width100mmInclBorder(\[int widthInclBorder\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="b32c3-247">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-247">public int widthMode(\[int value\])</span></span>                                      | <span data-ttu-id="b32c3-248">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-248">Gets or sets the calculation mode of the width of the control.</span></span>                                                                            |
| <span data-ttu-id="b32c3-249">public int widthOfString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="b32c3-249">public int widthOfString100mm(str string)</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="b32c3-250">public str widthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-250">public str widthStr(\[str value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="b32c3-251">public Units widthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-251">public Units widthUnit(\[Units value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="b32c3-252">public Real widthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="b32c3-252">public Real widthValue(\[Real value\])</span></span>                                   | <span data-ttu-id="b32c3-253">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-253">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="b32c3-254">public void left(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="b32c3-254">public void left(Real value, Units unit)</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="b32c3-255">public void top(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="b32c3-255">public void top(Real value, Units unit)</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="b32c3-256">public void topMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="b32c3-256">public void topMargin(Real value, Units unit)</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="b32c3-257">public void leftMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="b32c3-257">public void leftMargin(Real value, Units unit)</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="b32c3-258">public void labelWidth(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="b32c3-258">public void labelWidth(Real value, Units unit)</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="b32c3-259">public void width(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="b32c3-259">public void width(Real value, Units unit)</span></span>                                | <span data-ttu-id="b32c3-260">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-260">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="b32c3-261">public void hide()</span><span class="sxs-lookup"><span data-stu-id="b32c3-261">public void hide()</span></span>                                                       |                                                                                                                                           |
| <span data-ttu-id="b32c3-262">public void height(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="b32c3-262">public void height(Real value, Units unit)</span></span>                               | <span data-ttu-id="b32c3-263">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-263">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="b32c3-264">public void show()</span><span class="sxs-lookup"><span data-stu-id="b32c3-264">public void show()</span></span>                                                       |                                                                                                                                           |
| <span data-ttu-id="b32c3-265">public void bottomMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="b32c3-265">public void bottomMargin(Real value, Units unit)</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="b32c3-266">public void rightMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="b32c3-266">public void rightMargin(Real value, Units unit)</span></span>                          |                                                                                                                                           |

## <a name="method-alignment"></a><span data-ttu-id="b32c3-267">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="b32c3-267">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="b32c3-268">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="b32c3-268">Parameters - alignment</span></span>

<span data-ttu-id="b32c3-269">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-269">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="b32c3-270">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="b32c3-270">Return Value - alignment</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="b32c3-271">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="b32c3-271">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="b32c3-272">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="b32c3-272">Parameters - arrayIndex</span></span>

<span data-ttu-id="b32c3-273">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-273">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="b32c3-274">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="b32c3-274">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="b32c3-275">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="b32c3-275">Method autoDeclaration</span></span>

<span data-ttu-id="b32c3-276">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-276">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="b32c3-277">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="b32c3-277">Parameters - autoDeclaration</span></span>

<span data-ttu-id="b32c3-278">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-278">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="b32c3-279">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="b32c3-279">Return Value - autoDeclaration</span></span>

<span data-ttu-id="b32c3-280">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="b32c3-280">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="b32c3-281">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="b32c3-281">Remarks - autoDeclaration</span></span>

<span data-ttu-id="b32c3-282">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="b32c3-282">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="b32c3-283">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="b32c3-283">Method backgroundColor</span></span>

<span data-ttu-id="b32c3-284">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-284">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="b32c3-285">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="b32c3-285">Parameters - backgroundColor</span></span>

<span data-ttu-id="b32c3-286">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-286">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="b32c3-287">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="b32c3-287">Return Value - backgroundColor</span></span>

<span data-ttu-id="b32c3-288">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="b32c3-288">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="b32c3-289">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="b32c3-289">Remarks - backgroundColor</span></span>

<span data-ttu-id="b32c3-290">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b32c3-290">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="b32c3-291">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b32c3-291">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="b32c3-292">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="b32c3-292">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="b32c3-293">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="b32c3-293">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="b32c3-294">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b32c3-294">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="b32c3-295">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="b32c3-295">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="b32c3-296">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="b32c3-296">Method backStyle</span></span>

<span data-ttu-id="b32c3-297">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-297">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="b32c3-298">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="b32c3-298">Parameters - backStyle</span></span>

<span data-ttu-id="b32c3-299">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-299">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="b32c3-300">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="b32c3-300">Return Value - backStyle</span></span>

<span data-ttu-id="b32c3-301">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="b32c3-301">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="b32c3-302">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="b32c3-302">Method bold</span></span>

<span data-ttu-id="b32c3-303">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-303">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="b32c3-304">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="b32c3-304">Parameters - bold</span></span>

<span data-ttu-id="b32c3-305">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-305">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="b32c3-306">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="b32c3-306">Return Value - bold</span></span>

<span data-ttu-id="b32c3-307">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="b32c3-307">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="b32c3-308">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="b32c3-308">Remarks - bold</span></span>

<span data-ttu-id="b32c3-309">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b32c3-309">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="b32c3-310">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-310">0 Use the default font weight.</span></span>
-   <span data-ttu-id="b32c3-311">1 シン。</span><span class="sxs-lookup"><span data-stu-id="b32c3-311">1 Thin.</span></span>
-   <span data-ttu-id="b32c3-312">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="b32c3-312">2 Extra-light.</span></span>
-   <span data-ttu-id="b32c3-313">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="b32c3-313">3 Light.</span></span>
-   <span data-ttu-id="b32c3-314">4 標準。</span><span class="sxs-lookup"><span data-stu-id="b32c3-314">4 Normal.</span></span>
-   <span data-ttu-id="b32c3-315">5 中。</span><span class="sxs-lookup"><span data-stu-id="b32c3-315">5 Medium.</span></span>
-   <span data-ttu-id="b32c3-316">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="b32c3-316">6 Semibold.</span></span>
-   <span data-ttu-id="b32c3-317">7 太字。</span><span class="sxs-lookup"><span data-stu-id="b32c3-317">7 Bold.</span></span>
-   <span data-ttu-id="b32c3-318">8 極太。</span><span class="sxs-lookup"><span data-stu-id="b32c3-318">8 Extra-bold.</span></span>
-   <span data-ttu-id="b32c3-319">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="b32c3-319">9 Heavy.</span></span>

## <a name="method-bottommarginandframe"></a><span data-ttu-id="b32c3-320">メソッド bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="b32c3-320">Method bottomMarginAndFrame</span></span>

```xpp
public int bottomMarginAndFrame()
```

### <a name="return-value---bottommarginandframe"></a><span data-ttu-id="b32c3-321">戻り値 - bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="b32c3-321">Return Value - bottomMarginAndFrame</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="b32c3-322">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-322">Method bottomMarginMode</span></span>

```xpp
public int bottomMarginMode([int value])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="b32c3-323">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-323">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="b32c3-324">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-324">value</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="b32c3-325">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-325">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginstr"></a><span data-ttu-id="b32c3-326">メソッド bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-326">Method bottomMarginStr</span></span>

```xpp
public str bottomMarginStr([str value])
```

### <a name="parameters---bottommarginstr"></a><span data-ttu-id="b32c3-327">パラメーター - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-327">Parameters - bottomMarginStr</span></span>

<span data-ttu-id="b32c3-328">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-328">value</span></span>  

### <a name="return-value---bottommarginstr"></a><span data-ttu-id="b32c3-329">戻り値 - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-329">Return Value - bottomMarginStr</span></span>

## <a name="method-bottommarginunit"></a><span data-ttu-id="b32c3-330">メソッド bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-330">Method bottomMarginUnit</span></span>

```xpp
public Units bottomMarginUnit([Units value])
```

### <a name="parameters---bottommarginunit"></a><span data-ttu-id="b32c3-331">パラメーター - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-331">Parameters - bottomMarginUnit</span></span>

<span data-ttu-id="b32c3-332">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-332">value</span></span>  

### <a name="return-value---bottommarginunit"></a><span data-ttu-id="b32c3-333">戻り値 - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-333">Return Value - bottomMarginUnit</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="b32c3-334">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-334">Method bottomMarginValue</span></span>

```xpp
public Real bottomMarginValue([Real value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="b32c3-335">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-335">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="b32c3-336">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-336">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="b32c3-337">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-337">Return Value - bottomMarginValue</span></span>

## <a name="method-changelabelcase"></a><span data-ttu-id="b32c3-338">メソッド changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="b32c3-338">Method changeLabelCase</span></span>

```xpp
public int changeLabelCase([int value])
```

### <a name="parameters---changelabelcase"></a><span data-ttu-id="b32c3-339">パラメーター - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="b32c3-339">Parameters - changeLabelCase</span></span>

<span data-ttu-id="b32c3-340">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-340">value</span></span>  

### <a name="return-value---changelabelcase"></a><span data-ttu-id="b32c3-341">戻り値 - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="b32c3-341">Return Value - changeLabelCase</span></span>

## <a name="method-characterset"></a><span data-ttu-id="b32c3-342">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="b32c3-342">Method characterSet</span></span>

<span data-ttu-id="b32c3-343">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-343">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="b32c3-344">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="b32c3-344">Parameters - characterSet</span></span>

<span data-ttu-id="b32c3-345">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-345">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="b32c3-346">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="b32c3-346">Return Value - characterSet</span></span>

<span data-ttu-id="b32c3-347">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b32c3-347">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="b32c3-348">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="b32c3-348">Remarks - characterSet</span></span>

<span data-ttu-id="b32c3-349">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-349">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="b32c3-350">値です。</span><span class="sxs-lookup"><span data-stu-id="b32c3-350">Value.</span></span> | <span data-ttu-id="b32c3-351">説明。</span><span class="sxs-lookup"><span data-stu-id="b32c3-351">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="b32c3-352">0</span><span class="sxs-lookup"><span data-stu-id="b32c3-352">0</span></span>      | <span data-ttu-id="b32c3-353">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b32c3-353">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="b32c3-354">1</span><span class="sxs-lookup"><span data-stu-id="b32c3-354">1</span></span>      | <span data-ttu-id="b32c3-355">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b32c3-355">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="b32c3-356">2</span><span class="sxs-lookup"><span data-stu-id="b32c3-356">2</span></span>      | <span data-ttu-id="b32c3-357">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b32c3-357">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="b32c3-358">77</span><span class="sxs-lookup"><span data-stu-id="b32c3-358">77</span></span>     | <span data-ttu-id="b32c3-359">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b32c3-359">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="b32c3-360">128</span><span class="sxs-lookup"><span data-stu-id="b32c3-360">128</span></span>    | <span data-ttu-id="b32c3-361">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b32c3-361">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="b32c3-362">129</span><span class="sxs-lookup"><span data-stu-id="b32c3-362">129</span></span>    | <span data-ttu-id="b32c3-363">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b32c3-363">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="b32c3-364">134</span><span class="sxs-lookup"><span data-stu-id="b32c3-364">134</span></span>    | <span data-ttu-id="b32c3-365">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b32c3-365">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="b32c3-366">136</span><span class="sxs-lookup"><span data-stu-id="b32c3-366">136</span></span>    | <span data-ttu-id="b32c3-367">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b32c3-367">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="b32c3-368">161</span><span class="sxs-lookup"><span data-stu-id="b32c3-368">161</span></span>    | <span data-ttu-id="b32c3-369">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b32c3-369">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="b32c3-370">162</span><span class="sxs-lookup"><span data-stu-id="b32c3-370">162</span></span>    | <span data-ttu-id="b32c3-371">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b32c3-371">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="b32c3-372">163</span><span class="sxs-lookup"><span data-stu-id="b32c3-372">163</span></span>    | <span data-ttu-id="b32c3-373">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b32c3-373">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="b32c3-374">186</span><span class="sxs-lookup"><span data-stu-id="b32c3-374">186</span></span>    | <span data-ttu-id="b32c3-375">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b32c3-375">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="b32c3-376">204</span><span class="sxs-lookup"><span data-stu-id="b32c3-376">204</span></span>    | <span data-ttu-id="b32c3-377">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b32c3-377">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="b32c3-378">238</span><span class="sxs-lookup"><span data-stu-id="b32c3-378">238</span></span>    | <span data-ttu-id="b32c3-379">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b32c3-379">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="b32c3-380">255</span><span class="sxs-lookup"><span data-stu-id="b32c3-380">255</span></span>    | <span data-ttu-id="b32c3-381">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b32c3-381">OEM\_CHARSET</span></span>         |

<span data-ttu-id="b32c3-382">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="b32c3-382">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="b32c3-383">値です。</span><span class="sxs-lookup"><span data-stu-id="b32c3-383">Value.</span></span> | <span data-ttu-id="b32c3-384">説明。</span><span class="sxs-lookup"><span data-stu-id="b32c3-384">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="b32c3-385">130</span><span class="sxs-lookup"><span data-stu-id="b32c3-385">130</span></span>    | <span data-ttu-id="b32c3-386">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b32c3-386">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="b32c3-387">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="b32c3-387">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="b32c3-388">値です。</span><span class="sxs-lookup"><span data-stu-id="b32c3-388">Value.</span></span> | <span data-ttu-id="b32c3-389">説明。</span><span class="sxs-lookup"><span data-stu-id="b32c3-389">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="b32c3-390">177</span><span class="sxs-lookup"><span data-stu-id="b32c3-390">177</span></span>    | <span data-ttu-id="b32c3-391">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b32c3-391">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="b32c3-392">178</span><span class="sxs-lookup"><span data-stu-id="b32c3-392">178</span></span>    | <span data-ttu-id="b32c3-393">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b32c3-393">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="b32c3-394">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="b32c3-394">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="b32c3-395">値です。</span><span class="sxs-lookup"><span data-stu-id="b32c3-395">Value.</span></span> | <span data-ttu-id="b32c3-396">説明。</span><span class="sxs-lookup"><span data-stu-id="b32c3-396">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="b32c3-397">222</span><span class="sxs-lookup"><span data-stu-id="b32c3-397">222</span></span>    | <span data-ttu-id="b32c3-398">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b32c3-398">THAI\_CHARSET</span></span> |

<span data-ttu-id="b32c3-399">既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="b32c3-399">The default character set is set to a value, depending on the current system locale.</span></span> <span data-ttu-id="b32c3-400">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="b32c3-400">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="b32c3-401">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b32c3-401">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="b32c3-402">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="b32c3-402">Method colorScheme</span></span>

<span data-ttu-id="b32c3-403">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-403">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="b32c3-404">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="b32c3-404">Parameters - colorScheme</span></span>

<span data-ttu-id="b32c3-405">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-405">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="b32c3-406">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="b32c3-406">Return Value - colorScheme</span></span>

<span data-ttu-id="b32c3-407">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="b32c3-407">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="b32c3-408">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="b32c3-408">Remarks - colorScheme</span></span>

<span data-ttu-id="b32c3-409">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="b32c3-409">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="b32c3-410">値です。</span><span class="sxs-lookup"><span data-stu-id="b32c3-410">Value.</span></span> | <span data-ttu-id="b32c3-411">スタイル。</span><span class="sxs-lookup"><span data-stu-id="b32c3-411">Style.</span></span>                 |
|--------|------------------------|
| <span data-ttu-id="b32c3-412">0</span><span class="sxs-lookup"><span data-stu-id="b32c3-412">0</span></span>      | <span data-ttu-id="b32c3-413">既定。</span><span class="sxs-lookup"><span data-stu-id="b32c3-413">Default.</span></span>               |
| <span data-ttu-id="b32c3-414">1</span><span class="sxs-lookup"><span data-stu-id="b32c3-414">1</span></span>      | <span data-ttu-id="b32c3-415">Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="b32c3-415">The Windows palette.</span></span>   |
| <span data-ttu-id="b32c3-416">2</span><span class="sxs-lookup"><span data-stu-id="b32c3-416">2</span></span>      | <span data-ttu-id="b32c3-417">真の配色。</span><span class="sxs-lookup"><span data-stu-id="b32c3-417">The true-color scheme.</span></span> |

## <a name="method-configurationkey"></a><span data-ttu-id="b32c3-418">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="b32c3-418">Method configurationKey</span></span>

<span data-ttu-id="b32c3-419">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-419">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="b32c3-420">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="b32c3-420">Parameters - configurationKey</span></span>

<span data-ttu-id="b32c3-421">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-421">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="b32c3-422">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="b32c3-422">Return Value - configurationKey</span></span>

<span data-ttu-id="b32c3-423">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="b32c3-423">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="b32c3-424">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="b32c3-424">Remarks - configurationKey</span></span>

<span data-ttu-id="b32c3-425">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b32c3-425">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="b32c3-426">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="b32c3-426">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-controltype"></a><span data-ttu-id="b32c3-427">メソッド controlType</span><span class="sxs-lookup"><span data-stu-id="b32c3-427">Method controlType</span></span>

```xpp
public ReportFieldType controlType()
```

### <a name="return-value---controltype"></a><span data-ttu-id="b32c3-428">戻り値 - controlType</span><span class="sxs-lookup"><span data-stu-id="b32c3-428">Return Value - controlType</span></span>

## <a name="method-cssclass"></a><span data-ttu-id="b32c3-429">メソッド cssClass</span><span class="sxs-lookup"><span data-stu-id="b32c3-429">Method cssClass</span></span>

```xpp
public str cssClass([str value])
```

### <a name="parameters---cssclass"></a><span data-ttu-id="b32c3-430">パラメーター - cssClass</span><span class="sxs-lookup"><span data-stu-id="b32c3-430">Parameters - cssClass</span></span>

<span data-ttu-id="b32c3-431">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-431">value</span></span>  

### <a name="return-value---cssclass"></a><span data-ttu-id="b32c3-432">戻り値 - cssClass</span><span class="sxs-lookup"><span data-stu-id="b32c3-432">Return Value - cssClass</span></span>

## <a name="method-datafield"></a><span data-ttu-id="b32c3-433">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="b32c3-433">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="b32c3-434">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="b32c3-434">Parameters - dataField</span></span>

<span data-ttu-id="b32c3-435">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-435">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="b32c3-436">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="b32c3-436">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="b32c3-437">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="b32c3-437">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="b32c3-438">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="b32c3-438">Parameters - dataMethod</span></span>

<span data-ttu-id="b32c3-439">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-439">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="b32c3-440">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="b32c3-440">Return Value - dataMethod</span></span>

## <a name="method-dateday"></a><span data-ttu-id="b32c3-441">メソッド dateDay</span><span class="sxs-lookup"><span data-stu-id="b32c3-441">Method dateDay</span></span>

```xpp
public int dateDay([int value])
```

### <a name="parameters---dateday"></a><span data-ttu-id="b32c3-442">パラメーター - dateDay</span><span class="sxs-lookup"><span data-stu-id="b32c3-442">Parameters - dateDay</span></span>

<span data-ttu-id="b32c3-443">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-443">value</span></span>  

### <a name="return-value---dateday"></a><span data-ttu-id="b32c3-444">戻り値 - dateDay</span><span class="sxs-lookup"><span data-stu-id="b32c3-444">Return Value - dateDay</span></span>

## <a name="method-dateformat"></a><span data-ttu-id="b32c3-445">メソッド dateFormat</span><span class="sxs-lookup"><span data-stu-id="b32c3-445">Method dateFormat</span></span>

```xpp
public int dateFormat([int value])
```

### <a name="parameters---dateformat"></a><span data-ttu-id="b32c3-446">パラメーター - dateFormat</span><span class="sxs-lookup"><span data-stu-id="b32c3-446">Parameters - dateFormat</span></span>

<span data-ttu-id="b32c3-447">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-447">value</span></span>  

### <a name="return-value---dateformat"></a><span data-ttu-id="b32c3-448">戻り値 - dateFormat</span><span class="sxs-lookup"><span data-stu-id="b32c3-448">Return Value - dateFormat</span></span>

## <a name="method-datemonth"></a><span data-ttu-id="b32c3-449">メソッド dateMonth</span><span class="sxs-lookup"><span data-stu-id="b32c3-449">Method dateMonth</span></span>

```xpp
public int dateMonth([int value])
```

### <a name="parameters---datemonth"></a><span data-ttu-id="b32c3-450">パラメーター - dateMonth</span><span class="sxs-lookup"><span data-stu-id="b32c3-450">Parameters - dateMonth</span></span>

<span data-ttu-id="b32c3-451">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-451">value</span></span>  

### <a name="return-value---datemonth"></a><span data-ttu-id="b32c3-452">戻り値 - dateMonth</span><span class="sxs-lookup"><span data-stu-id="b32c3-452">Return Value - dateMonth</span></span>

## <a name="method-dateseparator"></a><span data-ttu-id="b32c3-453">メソッド dateSeparator</span><span class="sxs-lookup"><span data-stu-id="b32c3-453">Method dateSeparator</span></span>

```xpp
public int dateSeparator([int value])
```

### <a name="parameters---dateseparator"></a><span data-ttu-id="b32c3-454">パラメーター - dateSeparator</span><span class="sxs-lookup"><span data-stu-id="b32c3-454">Parameters - dateSeparator</span></span>

<span data-ttu-id="b32c3-455">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-455">value</span></span>  

### <a name="return-value---dateseparator"></a><span data-ttu-id="b32c3-456">戻り値 - dateSeparator</span><span class="sxs-lookup"><span data-stu-id="b32c3-456">Return Value - dateSeparator</span></span>

## <a name="method-dateyear"></a><span data-ttu-id="b32c3-457">メソッド dateYear</span><span class="sxs-lookup"><span data-stu-id="b32c3-457">Method dateYear</span></span>

```xpp
public int dateYear([int value])
```

### <a name="parameters---dateyear"></a><span data-ttu-id="b32c3-458">パラメーター - dateYear</span><span class="sxs-lookup"><span data-stu-id="b32c3-458">Parameters - dateYear</span></span>

<span data-ttu-id="b32c3-459">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-459">value</span></span>  

### <a name="return-value---dateyear"></a><span data-ttu-id="b32c3-460">戻り値 - dateYear</span><span class="sxs-lookup"><span data-stu-id="b32c3-460">Return Value - dateYear</span></span>

## <a name="method-delete"></a><span data-ttu-id="b32c3-461">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="b32c3-461">Method delete</span></span>

```xpp
public int delete()
```

### <a name="return-value---delete"></a><span data-ttu-id="b32c3-462">戻り値 - delete</span><span class="sxs-lookup"><span data-stu-id="b32c3-462">Return Value - delete</span></span>

## <a name="method-effectivefont"></a><span data-ttu-id="b32c3-463">メソッド effectiveFont</span><span class="sxs-lookup"><span data-stu-id="b32c3-463">Method effectiveFont</span></span>

```xpp
public str effectiveFont()
```

### <a name="return-value---effectivefont"></a><span data-ttu-id="b32c3-464">戻り値 - effectiveFont</span><span class="sxs-lookup"><span data-stu-id="b32c3-464">Return Value - effectiveFont</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="b32c3-465">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="b32c3-465">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="b32c3-466">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="b32c3-466">Parameters - extendedDataType</span></span>

<span data-ttu-id="b32c3-467">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-467">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="b32c3-468">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="b32c3-468">Return Value - extendedDataType</span></span>

## <a name="method-font"></a><span data-ttu-id="b32c3-469">メソッド font</span><span class="sxs-lookup"><span data-stu-id="b32c3-469">Method font</span></span>

<span data-ttu-id="b32c3-470">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-470">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="b32c3-471">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="b32c3-471">Parameters - font</span></span>

<span data-ttu-id="b32c3-472">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-472">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="b32c3-473">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="b32c3-473">Return Value - font</span></span>

<span data-ttu-id="b32c3-474">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="b32c3-474">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontinfoprinter"></a><span data-ttu-id="b32c3-475">メソッド fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="b32c3-475">Method fontInfoPrinter</span></span>

```xpp
public str fontInfoPrinter()
```

### <a name="return-value---fontinfoprinter"></a><span data-ttu-id="b32c3-476">戻り値 - fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="b32c3-476">Return Value - fontInfoPrinter</span></span>

## <a name="method-fontinfoprinterascent"></a><span data-ttu-id="b32c3-477">メソッド fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="b32c3-477">Method fontInfoPrinterAscent</span></span>

```xpp
public int fontInfoPrinterAscent()
```

### <a name="return-value---fontinfoprinterascent"></a><span data-ttu-id="b32c3-478">戻り値 - fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="b32c3-478">Return Value - fontInfoPrinterAscent</span></span>

## <a name="method-fontinfoprinterdescent"></a><span data-ttu-id="b32c3-479">メソッド fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="b32c3-479">Method fontInfoPrinterDescent</span></span>

```xpp
public int fontInfoPrinterDescent()
```

### <a name="return-value---fontinfoprinterdescent"></a><span data-ttu-id="b32c3-480">戻り値 - fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="b32c3-480">Return Value - fontInfoPrinterDescent</span></span>

## <a name="method-fontinfoprinterextlead"></a><span data-ttu-id="b32c3-481">メソッド fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="b32c3-481">Method fontInfoPrinterExtLead</span></span>

```xpp
public int fontInfoPrinterExtLead()
```

### <a name="return-value---fontinfoprinterextlead"></a><span data-ttu-id="b32c3-482">戻り値 - fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="b32c3-482">Return Value - fontInfoPrinterExtLead</span></span>

## <a name="method-fontinfoprinterheight"></a><span data-ttu-id="b32c3-483">メソッド fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="b32c3-483">Method fontInfoPrinterHeight</span></span>

```xpp
public int fontInfoPrinterHeight()
```

### <a name="return-value---fontinfoprinterheight"></a><span data-ttu-id="b32c3-484">戻り値 - fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="b32c3-484">Return Value - fontInfoPrinterHeight</span></span>

## <a name="method-fontinfoprinterintlead"></a><span data-ttu-id="b32c3-485">メソッド fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="b32c3-485">Method fontInfoPrinterIntLead</span></span>

```xpp
public int fontInfoPrinterIntLead()
```

### <a name="return-value---fontinfoprinterintlead"></a><span data-ttu-id="b32c3-486">戻り値 - fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="b32c3-486">Return Value - fontInfoPrinterIntLead</span></span>

## <a name="method-fontinfoscreen"></a><span data-ttu-id="b32c3-487">メソッド fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="b32c3-487">Method fontInfoScreen</span></span>

```xpp
public str fontInfoScreen()
```

### <a name="return-value---fontinfoscreen"></a><span data-ttu-id="b32c3-488">戻り値 - fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="b32c3-488">Return Value - fontInfoScreen</span></span>

## <a name="method-fontinfoscreenascent"></a><span data-ttu-id="b32c3-489">メソッド fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="b32c3-489">Method fontInfoScreenAscent</span></span>

```xpp
public int fontInfoScreenAscent()
```

### <a name="return-value---fontinfoscreenascent"></a><span data-ttu-id="b32c3-490">戻り値 - fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="b32c3-490">Return Value - fontInfoScreenAscent</span></span>

## <a name="method-fontinfoscreendescent"></a><span data-ttu-id="b32c3-491">メソッド fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="b32c3-491">Method fontInfoScreenDescent</span></span>

```xpp
public int fontInfoScreenDescent()
```

### <a name="return-value---fontinfoscreendescent"></a><span data-ttu-id="b32c3-492">戻り値 - fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="b32c3-492">Return Value - fontInfoScreenDescent</span></span>

## <a name="method-fontinfoscreenextlead"></a><span data-ttu-id="b32c3-493">メソッド fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="b32c3-493">Method fontInfoScreenExtLead</span></span>

```xpp
public int fontInfoScreenExtLead()
```

### <a name="return-value---fontinfoscreenextlead"></a><span data-ttu-id="b32c3-494">戻り値 - fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="b32c3-494">Return Value - fontInfoScreenExtLead</span></span>

## <a name="method-fontinfoscreenheight"></a><span data-ttu-id="b32c3-495">メソッド fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="b32c3-495">Method fontInfoScreenHeight</span></span>

```xpp
public int fontInfoScreenHeight()
```

### <a name="return-value---fontinfoscreenheight"></a><span data-ttu-id="b32c3-496">戻り値 - fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="b32c3-496">Return Value - fontInfoScreenHeight</span></span>

## <a name="method-fontinfoscreenintlead"></a><span data-ttu-id="b32c3-497">メソッド fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="b32c3-497">Method fontInfoScreenIntLead</span></span>

```xpp
public int fontInfoScreenIntLead()
```

### <a name="return-value---fontinfoscreenintlead"></a><span data-ttu-id="b32c3-498">戻り値 - fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="b32c3-498">Return Value - fontInfoScreenIntLead</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="b32c3-499">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="b32c3-499">Method fontSize</span></span>

<span data-ttu-id="b32c3-500">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-500">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="b32c3-501">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="b32c3-501">Parameters - fontSize</span></span>

<span data-ttu-id="b32c3-502">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-502">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="b32c3-503">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="b32c3-503">Return Value - fontSize</span></span>

<span data-ttu-id="b32c3-504">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="b32c3-504">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="b32c3-505">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="b32c3-505">Method foregroundColor</span></span>

<span data-ttu-id="b32c3-506">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-506">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="b32c3-507">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="b32c3-507">Parameters - foregroundColor</span></span>

<span data-ttu-id="b32c3-508">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-508">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="b32c3-509">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="b32c3-509">Return Value - foregroundColor</span></span>

<span data-ttu-id="b32c3-510">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="b32c3-510">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="b32c3-511">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="b32c3-511">Remarks - foregroundColor</span></span>

<span data-ttu-id="b32c3-512">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b32c3-512">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="b32c3-513">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b32c3-513">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="b32c3-514">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="b32c3-514">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="b32c3-515">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="b32c3-515">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="b32c3-516">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b32c3-516">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="b32c3-517">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="b32c3-517">The maximum value for a single byte is 255.</span></span>

## <a name="method-height100mm"></a><span data-ttu-id="b32c3-518">メソッド height100mm</span><span class="sxs-lookup"><span data-stu-id="b32c3-518">Method height100mm</span></span>

```xpp
public int height100mm([int heightExclBorder])
```

### <a name="parameters---height100mm"></a><span data-ttu-id="b32c3-519">パラメーター - height100mm</span><span class="sxs-lookup"><span data-stu-id="b32c3-519">Parameters - height100mm</span></span>

<span data-ttu-id="b32c3-520">heightExclBorder</span><span class="sxs-lookup"><span data-stu-id="b32c3-520">heightExclBorder</span></span>  

### <a name="return-value---height100mm"></a><span data-ttu-id="b32c3-521">戻り値 - height100mm</span><span class="sxs-lookup"><span data-stu-id="b32c3-521">Return Value - height100mm</span></span>

## <a name="method-height100mminclborder"></a><span data-ttu-id="b32c3-522">メソッド height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b32c3-522">Method height100mmInclBorder</span></span>

```xpp
public int height100mmInclBorder([int heightInclBorder])
```

### <a name="parameters---height100mminclborder"></a><span data-ttu-id="b32c3-523">パラメーター - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b32c3-523">Parameters - height100mmInclBorder</span></span>

<span data-ttu-id="b32c3-524">heightInclBorder</span><span class="sxs-lookup"><span data-stu-id="b32c3-524">heightInclBorder</span></span>  

### <a name="return-value---height100mminclborder"></a><span data-ttu-id="b32c3-525">戻り値 - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b32c3-525">Return Value - height100mmInclBorder</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="b32c3-526">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-526">Method heightMode</span></span>

<span data-ttu-id="b32c3-527">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-527">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="b32c3-528">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-528">Parameters - heightMode</span></span>

<span data-ttu-id="b32c3-529">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-529">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="b32c3-530">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-530">Return Value - heightMode</span></span>

<span data-ttu-id="b32c3-531">計算モード。</span><span class="sxs-lookup"><span data-stu-id="b32c3-531">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="b32c3-532">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-532">Remarks - heightMode</span></span>

<span data-ttu-id="b32c3-533">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="b32c3-533">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="b32c3-534">モード。</span><span class="sxs-lookup"><span data-stu-id="b32c3-534">Mode.</span></span>          | <span data-ttu-id="b32c3-535">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="b32c3-535">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b32c3-536">正確。</span><span class="sxs-lookup"><span data-stu-id="b32c3-536">Exact.</span></span>         | <span data-ttu-id="b32c3-537">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b32c3-537">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b32c3-538">自動。</span><span class="sxs-lookup"><span data-stu-id="b32c3-538">Auto.</span></span>          | <span data-ttu-id="b32c3-539">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b32c3-539">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b32c3-540">列の高さ</span><span class="sxs-lookup"><span data-stu-id="b32c3-540">Column height.</span></span> | <span data-ttu-id="b32c3-541">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="b32c3-541">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="b32c3-542">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="b32c3-542">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightofwordwrappedstring100mm"></a><span data-ttu-id="b32c3-543">メソッド heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="b32c3-543">Method heightOfWordWrappedString100mm</span></span>

```xpp
public int heightOfWordWrappedString100mm(str string)
```

### <a name="parameters---heightofwordwrappedstring100mm"></a><span data-ttu-id="b32c3-544">パラメーター - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="b32c3-544">Parameters - heightOfWordWrappedString100mm</span></span>

<span data-ttu-id="b32c3-545">文字列</span><span class="sxs-lookup"><span data-stu-id="b32c3-545">string</span></span>  

### <a name="return-value---heightofwordwrappedstring100mm"></a><span data-ttu-id="b32c3-546">戻り値 - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="b32c3-546">Return Value - heightOfWordWrappedString100mm</span></span>

## <a name="method-heightstr"></a><span data-ttu-id="b32c3-547">メソッド heightStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-547">Method heightStr</span></span>

```xpp
public str heightStr([str value])
```

### <a name="parameters---heightstr"></a><span data-ttu-id="b32c3-548">パラメーター - heightStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-548">Parameters - heightStr</span></span>

<span data-ttu-id="b32c3-549">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-549">value</span></span>  

### <a name="return-value---heightstr"></a><span data-ttu-id="b32c3-550">戻り値 - heightStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-550">Return Value - heightStr</span></span>

## <a name="method-heightunit"></a><span data-ttu-id="b32c3-551">メソッド heightUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-551">Method heightUnit</span></span>

```xpp
public Units heightUnit([Units value])
```

### <a name="parameters---heightunit"></a><span data-ttu-id="b32c3-552">パラメーター - heightUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-552">Parameters - heightUnit</span></span>

<span data-ttu-id="b32c3-553">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-553">value</span></span>  

### <a name="return-value---heightunit"></a><span data-ttu-id="b32c3-554">戻り値 - heightUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-554">Return Value - heightUnit</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="b32c3-555">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-555">Method heightValue</span></span>

<span data-ttu-id="b32c3-556">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-556">Gets or sets the height of the control.</span></span>

```xpp
public Real heightValue([Real value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="b32c3-557">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-557">Parameters - heightValue</span></span>

<span data-ttu-id="b32c3-558">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-558">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="b32c3-559">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-559">Return Value - heightValue</span></span>

<span data-ttu-id="b32c3-560">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="b32c3-560">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="b32c3-561">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-561">Remarks - heightValue</span></span>

<span data-ttu-id="b32c3-562">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="b32c3-562">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-italic"></a><span data-ttu-id="b32c3-563">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="b32c3-563">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="b32c3-564">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="b32c3-564">Parameters - italic</span></span>

<span data-ttu-id="b32c3-565">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-565">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="b32c3-566">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="b32c3-566">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="b32c3-567">メソッド label</span><span class="sxs-lookup"><span data-stu-id="b32c3-567">Method label</span></span>

<span data-ttu-id="b32c3-568">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-568">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="b32c3-569">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="b32c3-569">Parameters - label</span></span>

<span data-ttu-id="b32c3-570">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-570">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="b32c3-571">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="b32c3-571">Return Value - label</span></span>

<span data-ttu-id="b32c3-572">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="b32c3-572">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="b32c3-573">備考 - label</span><span class="sxs-lookup"><span data-stu-id="b32c3-573">Remarks - label</span></span>

<span data-ttu-id="b32c3-574">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-574">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="b32c3-575">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="b32c3-575">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="b32c3-576">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="b32c3-576">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="b32c3-577">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="b32c3-577">Parameters - labelBold</span></span>

<span data-ttu-id="b32c3-578">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-578">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="b32c3-579">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="b32c3-579">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="b32c3-580">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="b32c3-580">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="b32c3-581">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="b32c3-581">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="b32c3-582">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-582">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="b32c3-583">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="b32c3-583">Return Value - labelCharacterSet</span></span>

## <a name="method-labelcssclass"></a><span data-ttu-id="b32c3-584">メソッド labelCssClass</span><span class="sxs-lookup"><span data-stu-id="b32c3-584">Method labelCssClass</span></span>

```xpp
public str labelCssClass([str value])
```

### <a name="parameters---labelcssclass"></a><span data-ttu-id="b32c3-585">パラメーター - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="b32c3-585">Parameters - labelCssClass</span></span>

<span data-ttu-id="b32c3-586">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-586">value</span></span>  

### <a name="return-value---labelcssclass"></a><span data-ttu-id="b32c3-587">戻り値 - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="b32c3-587">Return Value - labelCssClass</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="b32c3-588">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="b32c3-588">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="b32c3-589">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="b32c3-589">Parameters - labelFont</span></span>

<span data-ttu-id="b32c3-590">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-590">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="b32c3-591">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="b32c3-591">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="b32c3-592">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="b32c3-592">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="b32c3-593">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="b32c3-593">Parameters - labelFontSize</span></span>

<span data-ttu-id="b32c3-594">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-594">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="b32c3-595">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="b32c3-595">Return Value - labelFontSize</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="b32c3-596">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="b32c3-596">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="b32c3-597">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="b32c3-597">Parameters - labelItalic</span></span>

<span data-ttu-id="b32c3-598">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-598">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="b32c3-599">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="b32c3-599">Return Value - labelItalic</span></span>

## <a name="method-labellinebelow"></a><span data-ttu-id="b32c3-600">メソッド labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="b32c3-600">Method labelLineBelow</span></span>

```xpp
public LineType labelLineBelow([LineType value])
```

### <a name="parameters---labellinebelow"></a><span data-ttu-id="b32c3-601">パラメーター - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="b32c3-601">Parameters - labelLineBelow</span></span>

<span data-ttu-id="b32c3-602">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-602">value</span></span>  

### <a name="return-value---labellinebelow"></a><span data-ttu-id="b32c3-603">戻り値 - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="b32c3-603">Return Value - labelLineBelow</span></span>

## <a name="method-labellinethickness"></a><span data-ttu-id="b32c3-604">メソッド labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="b32c3-604">Method labelLineThickness</span></span>

```xpp
public LineThickness labelLineThickness([LineThickness value])
```

### <a name="parameters---labellinethickness"></a><span data-ttu-id="b32c3-605">パラメーター - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="b32c3-605">Parameters - labelLineThickness</span></span>

<span data-ttu-id="b32c3-606">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-606">value</span></span>  

### <a name="return-value---labellinethickness"></a><span data-ttu-id="b32c3-607">戻り値 - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="b32c3-607">Return Value - labelLineThickness</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="b32c3-608">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="b32c3-608">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="b32c3-609">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="b32c3-609">Parameters - labelPosition</span></span>

<span data-ttu-id="b32c3-610">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-610">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="b32c3-611">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="b32c3-611">Return Value - labelPosition</span></span>

## <a name="method-labeltableader"></a><span data-ttu-id="b32c3-612">メソッド labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="b32c3-612">Method labelTabLeader</span></span>

```xpp
public int labelTabLeader([int value])
```

### <a name="parameters---labeltableader"></a><span data-ttu-id="b32c3-613">パラメーター - labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="b32c3-613">Parameters - labelTabLeader</span></span>

<span data-ttu-id="b32c3-614">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-614">value</span></span>  

### <a name="return-value---labeltableader"></a><span data-ttu-id="b32c3-615">戻り値 - labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="b32c3-615">Return Value - labelTabLeader</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="b32c3-616">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="b32c3-616">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="b32c3-617">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="b32c3-617">Parameters - labelUnderline</span></span>

<span data-ttu-id="b32c3-618">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-618">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="b32c3-619">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="b32c3-619">Return Value - labelUnderline</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="b32c3-620">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-620">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="b32c3-621">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-621">Parameters - labelWidthMode</span></span>

<span data-ttu-id="b32c3-622">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-622">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="b32c3-623">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-623">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthstr"></a><span data-ttu-id="b32c3-624">メソッド labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-624">Method labelWidthStr</span></span>

```xpp
public str labelWidthStr([str value])
```

### <a name="parameters---labelwidthstr"></a><span data-ttu-id="b32c3-625">パラメーター - labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-625">Parameters - labelWidthStr</span></span>

<span data-ttu-id="b32c3-626">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-626">value</span></span>  

### <a name="return-value---labelwidthstr"></a><span data-ttu-id="b32c3-627">戻り値 - labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-627">Return Value - labelWidthStr</span></span>

## <a name="method-labelwidthunit"></a><span data-ttu-id="b32c3-628">メソッド labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-628">Method labelWidthUnit</span></span>

```xpp
public Units labelWidthUnit([Units value])
```

### <a name="parameters---labelwidthunit"></a><span data-ttu-id="b32c3-629">パラメーター - labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-629">Parameters - labelWidthUnit</span></span>

<span data-ttu-id="b32c3-630">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-630">value</span></span>  

### <a name="return-value---labelwidthunit"></a><span data-ttu-id="b32c3-631">戻り値 - labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-631">Return Value - labelWidthUnit</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="b32c3-632">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-632">Method labelWidthValue</span></span>

```xpp
public Real labelWidthValue([Real value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="b32c3-633">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-633">Parameters - labelWidthValue</span></span>

<span data-ttu-id="b32c3-634">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-634">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="b32c3-635">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-635">Return Value - labelWidthValue</span></span>

## <a name="method-left100mm"></a><span data-ttu-id="b32c3-636">メソッド left100mm</span><span class="sxs-lookup"><span data-stu-id="b32c3-636">Method left100mm</span></span>

```xpp
public int left100mm([int leftExclBorder])
```

### <a name="parameters---left100mm"></a><span data-ttu-id="b32c3-637">パラメーター - left100mm</span><span class="sxs-lookup"><span data-stu-id="b32c3-637">Parameters - left100mm</span></span>

<span data-ttu-id="b32c3-638">leftExclBorder</span><span class="sxs-lookup"><span data-stu-id="b32c3-638">leftExclBorder</span></span>  

### <a name="return-value---left100mm"></a><span data-ttu-id="b32c3-639">戻り値 - left100mm</span><span class="sxs-lookup"><span data-stu-id="b32c3-639">Return Value - left100mm</span></span>

## <a name="method-left100mminclborder"></a><span data-ttu-id="b32c3-640">メソッド left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b32c3-640">Method left100mmInclBorder</span></span>

```xpp
public int left100mmInclBorder([int leftInclBorder])
```

### <a name="parameters---left100mminclborder"></a><span data-ttu-id="b32c3-641">パラメーター - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b32c3-641">Parameters - left100mmInclBorder</span></span>

<span data-ttu-id="b32c3-642">leftInclBorder</span><span class="sxs-lookup"><span data-stu-id="b32c3-642">leftInclBorder</span></span>  

### <a name="return-value---left100mminclborder"></a><span data-ttu-id="b32c3-643">戻り値 - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b32c3-643">Return Value - left100mmInclBorder</span></span>

## <a name="method-leftmarginanframe"></a><span data-ttu-id="b32c3-644">メソッド leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="b32c3-644">Method leftMarginAnFrame</span></span>

```xpp
public int leftMarginAnFrame()
```

### <a name="return-value---leftmarginanframe"></a><span data-ttu-id="b32c3-645">戻り値 - leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="b32c3-645">Return Value - leftMarginAnFrame</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="b32c3-646">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-646">Method leftMarginMode</span></span>

```xpp
public int leftMarginMode([int value])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="b32c3-647">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-647">Parameters - leftMarginMode</span></span>

<span data-ttu-id="b32c3-648">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-648">value</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="b32c3-649">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-649">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginstr"></a><span data-ttu-id="b32c3-650">メソッド leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-650">Method leftMarginStr</span></span>

```xpp
public str leftMarginStr([str value])
```

### <a name="parameters---leftmarginstr"></a><span data-ttu-id="b32c3-651">パラメーター - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-651">Parameters - leftMarginStr</span></span>

<span data-ttu-id="b32c3-652">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-652">value</span></span>  

### <a name="return-value---leftmarginstr"></a><span data-ttu-id="b32c3-653">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-653">Return Value - leftMarginStr</span></span>

## <a name="method-leftmarginunit"></a><span data-ttu-id="b32c3-654">メソッド leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-654">Method leftMarginUnit</span></span>

```xpp
public Units leftMarginUnit([Units value])
```

### <a name="parameters---leftmarginunit"></a><span data-ttu-id="b32c3-655">パラメーター - leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-655">Parameters - leftMarginUnit</span></span>

<span data-ttu-id="b32c3-656">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-656">value</span></span>  

### <a name="return-value---leftmarginunit"></a><span data-ttu-id="b32c3-657">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-657">Return Value - leftMarginUnit</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="b32c3-658">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-658">Method leftMarginValue</span></span>

```xpp
public Real leftMarginValue([Real value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="b32c3-659">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-659">Parameters - leftMarginValue</span></span>

<span data-ttu-id="b32c3-660">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-660">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="b32c3-661">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-661">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="b32c3-662">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-662">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="b32c3-663">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-663">Parameters - leftMode</span></span>

<span data-ttu-id="b32c3-664">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-664">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="b32c3-665">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-665">Return Value - leftMode</span></span>

## <a name="method-leftstr"></a><span data-ttu-id="b32c3-666">メソッド leftStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-666">Method leftStr</span></span>

```xpp
public str leftStr([str value])
```

### <a name="parameters---leftstr"></a><span data-ttu-id="b32c3-667">パラメーター - leftStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-667">Parameters - leftStr</span></span>

<span data-ttu-id="b32c3-668">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-668">value</span></span>  

### <a name="return-value---leftstr"></a><span data-ttu-id="b32c3-669">戻り値 - leftStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-669">Return Value - leftStr</span></span>

## <a name="method-leftunit"></a><span data-ttu-id="b32c3-670">メソッド leftUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-670">Method leftUnit</span></span>

```xpp
public Units leftUnit([Units value])
```

### <a name="parameters---leftunit"></a><span data-ttu-id="b32c3-671">パラメーター - leftUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-671">Parameters - leftUnit</span></span>

<span data-ttu-id="b32c3-672">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-672">value</span></span>  

### <a name="return-value---leftunit"></a><span data-ttu-id="b32c3-673">戻り値 - leftUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-673">Return Value - leftUnit</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="b32c3-674">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-674">Method leftValue</span></span>

```xpp
public Real leftValue([Real value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="b32c3-675">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-675">Parameters - leftValue</span></span>

<span data-ttu-id="b32c3-676">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-676">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="b32c3-677">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-677">Return Value - leftValue</span></span>

## <a name="method-lineabove"></a><span data-ttu-id="b32c3-678">メソッド lineAbove</span><span class="sxs-lookup"><span data-stu-id="b32c3-678">Method lineAbove</span></span>

```xpp
public LineType lineAbove([LineType value])
```

### <a name="parameters---lineabove"></a><span data-ttu-id="b32c3-679">パラメーター - lineAbove</span><span class="sxs-lookup"><span data-stu-id="b32c3-679">Parameters - lineAbove</span></span>

<span data-ttu-id="b32c3-680">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-680">value</span></span>  

### <a name="return-value---lineabove"></a><span data-ttu-id="b32c3-681">戻り値 - lineAbove</span><span class="sxs-lookup"><span data-stu-id="b32c3-681">Return Value - lineAbove</span></span>

## <a name="method-linebelow"></a><span data-ttu-id="b32c3-682">メソッド lineBelow</span><span class="sxs-lookup"><span data-stu-id="b32c3-682">Method lineBelow</span></span>

```xpp
public LineType lineBelow([LineType value])
```

### <a name="parameters---linebelow"></a><span data-ttu-id="b32c3-683">パラメーター - lineBelow</span><span class="sxs-lookup"><span data-stu-id="b32c3-683">Parameters - lineBelow</span></span>

<span data-ttu-id="b32c3-684">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-684">value</span></span>  

### <a name="return-value---linebelow"></a><span data-ttu-id="b32c3-685">戻り値 - lineBelow</span><span class="sxs-lookup"><span data-stu-id="b32c3-685">Return Value - lineBelow</span></span>

## <a name="method-lineleft"></a><span data-ttu-id="b32c3-686">メソッド lineLeft</span><span class="sxs-lookup"><span data-stu-id="b32c3-686">Method lineLeft</span></span>

<span data-ttu-id="b32c3-687">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-687">Gets or sets the type of line that is used as the left border of a section.</span></span>

```xpp
public LineType lineLeft([LineType value])
```

### <a name="parameters---lineleft"></a><span data-ttu-id="b32c3-688">パラメーター - lineLeft</span><span class="sxs-lookup"><span data-stu-id="b32c3-688">Parameters - lineLeft</span></span>

<span data-ttu-id="b32c3-689">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-689">value</span></span>  

### <a name="return-value---lineleft"></a><span data-ttu-id="b32c3-690">戻り値 - lineLeft</span><span class="sxs-lookup"><span data-stu-id="b32c3-690">Return Value - lineLeft</span></span>

<span data-ttu-id="b32c3-691">左境界線として使用される線のタイプ。</span><span class="sxs-lookup"><span data-stu-id="b32c3-691">The type of line that is used as the left border.</span></span>

## <a name="method-lineright"></a><span data-ttu-id="b32c3-692">メソッド lineRight</span><span class="sxs-lookup"><span data-stu-id="b32c3-692">Method lineRight</span></span>

```xpp
public LineType lineRight([LineType value])
```

### <a name="parameters---lineright"></a><span data-ttu-id="b32c3-693">パラメーター - lineRight</span><span class="sxs-lookup"><span data-stu-id="b32c3-693">Parameters - lineRight</span></span>

<span data-ttu-id="b32c3-694">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-694">value</span></span>  

### <a name="return-value---lineright"></a><span data-ttu-id="b32c3-695">戻り値 - lineRight</span><span class="sxs-lookup"><span data-stu-id="b32c3-695">Return Value - lineRight</span></span>

## <a name="method-menuitemlabel"></a><span data-ttu-id="b32c3-696">メソッド menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="b32c3-696">Method menuItemLabel</span></span>

```xpp
public str menuItemLabel([str value])
```

### <a name="parameters---menuitemlabel"></a><span data-ttu-id="b32c3-697">パラメーター - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="b32c3-697">Parameters - menuItemLabel</span></span>

<span data-ttu-id="b32c3-698">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-698">value</span></span>  

### <a name="return-value---menuitemlabel"></a><span data-ttu-id="b32c3-699">戻り値 - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="b32c3-699">Return Value - menuItemLabel</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="b32c3-700">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="b32c3-700">Method menuItemName</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="b32c3-701">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="b32c3-701">Parameters - menuItemName</span></span>

<span data-ttu-id="b32c3-702">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-702">value</span></span>  

### <a name="return-value---menuitemname"></a><span data-ttu-id="b32c3-703">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="b32c3-703">Return Value - menuItemName</span></span>

## <a name="method-menuitemtype"></a><span data-ttu-id="b32c3-704">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="b32c3-704">Method menuItemType</span></span>

```xpp
public MenuItemType menuItemType([MenuItemType value])
```

### <a name="parameters---menuitemtype"></a><span data-ttu-id="b32c3-705">パラメーター - menuItemType</span><span class="sxs-lookup"><span data-stu-id="b32c3-705">Parameters - menuItemType</span></span>

<span data-ttu-id="b32c3-706">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-706">value</span></span>  

### <a name="return-value---menuitemtype"></a><span data-ttu-id="b32c3-707">戻り値 - menuItemType</span><span class="sxs-lookup"><span data-stu-id="b32c3-707">Return Value - menuItemType</span></span>

## <a name="method-modelfieldname"></a><span data-ttu-id="b32c3-708">メソッド modelFieldName</span><span class="sxs-lookup"><span data-stu-id="b32c3-708">Method modelFieldName</span></span>

```xpp
public str modelFieldName([str value])
```

### <a name="parameters---modelfieldname"></a><span data-ttu-id="b32c3-709">パラメーター - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="b32c3-709">Parameters - modelFieldName</span></span>

<span data-ttu-id="b32c3-710">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-710">value</span></span>  

### <a name="return-value---modelfieldname"></a><span data-ttu-id="b32c3-711">戻り値 - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="b32c3-711">Return Value - modelFieldName</span></span>

## <a name="method-name"></a><span data-ttu-id="b32c3-712">メソッド名</span><span class="sxs-lookup"><span data-stu-id="b32c3-712">Method name</span></span>

<span data-ttu-id="b32c3-713">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-713">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="b32c3-714">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="b32c3-714">Parameters - name</span></span>

<span data-ttu-id="b32c3-715">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-715">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="b32c3-716">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="b32c3-716">Return Value - name</span></span>

<span data-ttu-id="b32c3-717">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="b32c3-717">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="b32c3-718">備考 - name</span><span class="sxs-lookup"><span data-stu-id="b32c3-718">Remarks - name</span></span>

<span data-ttu-id="b32c3-719">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b32c3-719">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="b32c3-720">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="b32c3-720">Begins with a letter.</span></span>
-   <span data-ttu-id="b32c3-721">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="b32c3-721">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="b32c3-722">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="b32c3-722">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="b32c3-723">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="b32c3-723">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="b32c3-724">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="b32c3-724">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-numberoflines"></a><span data-ttu-id="b32c3-725">メソッド numberOfLines</span><span class="sxs-lookup"><span data-stu-id="b32c3-725">Method numberOfLines</span></span>

```xpp
public int numberOfLines(int height100mm)
```

### <a name="parameters---numberoflines"></a><span data-ttu-id="b32c3-726">パラメーター - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="b32c3-726">Parameters - numberOfLines</span></span>

<span data-ttu-id="b32c3-727">height100mm</span><span class="sxs-lookup"><span data-stu-id="b32c3-727">height100mm</span></span>  

### <a name="return-value---numberoflines"></a><span data-ttu-id="b32c3-728">戻り値 - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="b32c3-728">Return Value - numberOfLines</span></span>

## <a name="method-position"></a><span data-ttu-id="b32c3-729">メソッドの位置</span><span class="sxs-lookup"><span data-stu-id="b32c3-729">Method position</span></span>

```xpp
public int position([int value])
```

### <a name="parameters---position"></a><span data-ttu-id="b32c3-730">パラメーター - position</span><span class="sxs-lookup"><span data-stu-id="b32c3-730">Parameters - position</span></span>

<span data-ttu-id="b32c3-731">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-731">value</span></span>  

### <a name="return-value---position"></a><span data-ttu-id="b32c3-732">戻り値 - position</span><span class="sxs-lookup"><span data-stu-id="b32c3-732">Return Value - position</span></span>

## <a name="method-previewinfo"></a><span data-ttu-id="b32c3-733">メソッド previewInfo</span><span class="sxs-lookup"><span data-stu-id="b32c3-733">Method previewInfo</span></span>

```xpp
public str previewInfo(str string)
```

### <a name="parameters---previewinfo"></a><span data-ttu-id="b32c3-734">パラメーター - previewInfo</span><span class="sxs-lookup"><span data-stu-id="b32c3-734">Parameters - previewInfo</span></span>

<span data-ttu-id="b32c3-735">文字列</span><span class="sxs-lookup"><span data-stu-id="b32c3-735">string</span></span>  

### <a name="return-value---previewinfo"></a><span data-ttu-id="b32c3-736">戻り値 - previewInfo</span><span class="sxs-lookup"><span data-stu-id="b32c3-736">Return Value - previewInfo</span></span>

## <a name="method-previewxcompensation100mm"></a><span data-ttu-id="b32c3-737">メソッド previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="b32c3-737">Method previewXCompensation100mm</span></span>

```xpp
public int previewXCompensation100mm(str string)
```

### <a name="parameters---previewxcompensation100mm"></a><span data-ttu-id="b32c3-738">パラメーター - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="b32c3-738">Parameters - previewXCompensation100mm</span></span>

<span data-ttu-id="b32c3-739">文字列</span><span class="sxs-lookup"><span data-stu-id="b32c3-739">string</span></span>  

### <a name="return-value---previewxcompensation100mm"></a><span data-ttu-id="b32c3-740">戻り値 - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="b32c3-740">Return Value - previewXCompensation100mm</span></span>

## <a name="method-right100mm"></a><span data-ttu-id="b32c3-741">メソッド right100mm</span><span class="sxs-lookup"><span data-stu-id="b32c3-741">Method right100mm</span></span>

```xpp
public int right100mm()
```

### <a name="return-value---right100mm"></a><span data-ttu-id="b32c3-742">戻り値 - right100mm</span><span class="sxs-lookup"><span data-stu-id="b32c3-742">Return Value - right100mm</span></span>

## <a name="method-right100mminclborder"></a><span data-ttu-id="b32c3-743">メソッド right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b32c3-743">Method right100mmInclBorder</span></span>

```xpp
public int right100mmInclBorder()
```

### <a name="return-value---right100mminclborder"></a><span data-ttu-id="b32c3-744">戻り値 - right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b32c3-744">Return Value - right100mmInclBorder</span></span>

## <a name="method-rightmarginandframe"></a><span data-ttu-id="b32c3-745">メソッド rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="b32c3-745">Method rightMarginAndFrame</span></span>

```xpp
public int rightMarginAndFrame()
```

### <a name="return-value---rightmarginandframe"></a><span data-ttu-id="b32c3-746">戻り値 - rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="b32c3-746">Return Value - rightMarginAndFrame</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="b32c3-747">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-747">Method rightMarginMode</span></span>

```xpp
public int rightMarginMode([int value])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="b32c3-748">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-748">Parameters - rightMarginMode</span></span>

<span data-ttu-id="b32c3-749">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-749">value</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="b32c3-750">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-750">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginstr"></a><span data-ttu-id="b32c3-751">メソッド rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-751">Method rightMarginStr</span></span>

```xpp
public str rightMarginStr([str value])
```

### <a name="parameters---rightmarginstr"></a><span data-ttu-id="b32c3-752">パラメーター - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-752">Parameters - rightMarginStr</span></span>

<span data-ttu-id="b32c3-753">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-753">value</span></span>  

### <a name="return-value---rightmarginstr"></a><span data-ttu-id="b32c3-754">戻り値 - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-754">Return Value - rightMarginStr</span></span>

## <a name="method-rightmarginunit"></a><span data-ttu-id="b32c3-755">メソッド rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-755">Method rightMarginUnit</span></span>

```xpp
public Units rightMarginUnit([Units value])
```

### <a name="parameters---rightmarginunit"></a><span data-ttu-id="b32c3-756">パラメーター - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-756">Parameters - rightMarginUnit</span></span>

<span data-ttu-id="b32c3-757">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-757">value</span></span>  

### <a name="return-value---rightmarginunit"></a><span data-ttu-id="b32c3-758">戻り値 - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-758">Return Value - rightMarginUnit</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="b32c3-759">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-759">Method rightMarginValue</span></span>

```xpp
public Real rightMarginValue([Real value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="b32c3-760">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-760">Parameters - rightMarginValue</span></span>

<span data-ttu-id="b32c3-761">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-761">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="b32c3-762">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-762">Return Value - rightMarginValue</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="b32c3-763">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="b32c3-763">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="b32c3-764">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="b32c3-764">Parameters - securityKey</span></span>

<span data-ttu-id="b32c3-765">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-765">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="b32c3-766">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="b32c3-766">Return Value - securityKey</span></span>

## <a name="method-setheightgettext"></a><span data-ttu-id="b32c3-767">メソッド setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="b32c3-767">Method setHeightGetText</span></span>

```xpp
public str setHeightGetText(int lines, str string)
```

### <a name="parameters---setheightgettext"></a><span data-ttu-id="b32c3-768">パラメーター - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="b32c3-768">Parameters - setHeightGetText</span></span>

<span data-ttu-id="b32c3-769">明細行</span><span class="sxs-lookup"><span data-stu-id="b32c3-769">lines</span></span>  

<!-- -->

<span data-ttu-id="b32c3-770">文字列</span><span class="sxs-lookup"><span data-stu-id="b32c3-770">string</span></span>  

### <a name="return-value---setheightgettext"></a><span data-ttu-id="b32c3-771">戻り値 - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="b32c3-771">Return Value - setHeightGetText</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="b32c3-772">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="b32c3-772">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="b32c3-773">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="b32c3-773">Parameters - showLabel</span></span>

<span data-ttu-id="b32c3-774">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-774">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="b32c3-775">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="b32c3-775">Return Value - showLabel</span></span>

## <a name="method-table"></a><span data-ttu-id="b32c3-776">メソッド table</span><span class="sxs-lookup"><span data-stu-id="b32c3-776">Method table</span></span>

<span data-ttu-id="b32c3-777">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-777">Gets or sets the table ID associated with the object.</span></span>

```xpp
public TableId table([TableId value])
```

### <a name="parameters---table"></a><span data-ttu-id="b32c3-778">パラメーター - table</span><span class="sxs-lookup"><span data-stu-id="b32c3-778">Parameters - table</span></span>

<span data-ttu-id="b32c3-779">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-779">value</span></span>  

### <a name="return-value---table"></a><span data-ttu-id="b32c3-780">戻り値 - toBlob</span><span class="sxs-lookup"><span data-stu-id="b32c3-780">Return Value - table</span></span>

<span data-ttu-id="b32c3-781">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="b32c3-781">The current value of the table ID associated with the object.</span></span>

## <a name="method-thickness"></a><span data-ttu-id="b32c3-782">メソッド thickness</span><span class="sxs-lookup"><span data-stu-id="b32c3-782">Method thickness</span></span>

```xpp
public LineThickness thickness([LineThickness value])
```

### <a name="parameters---thickness"></a><span data-ttu-id="b32c3-783">パラメーター - thickness</span><span class="sxs-lookup"><span data-stu-id="b32c3-783">Parameters - thickness</span></span>

<span data-ttu-id="b32c3-784">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-784">value</span></span>  

### <a name="return-value---thickness"></a><span data-ttu-id="b32c3-785">戻り値 - thickness</span><span class="sxs-lookup"><span data-stu-id="b32c3-785">Return Value - thickness</span></span>

## <a name="method-top100mm"></a><span data-ttu-id="b32c3-786">メソッド top100mm</span><span class="sxs-lookup"><span data-stu-id="b32c3-786">Method top100mm</span></span>

```xpp
public int top100mm([int topExclBorder])
```

### <a name="parameters---top100mm"></a><span data-ttu-id="b32c3-787">パラメーター - top100mm</span><span class="sxs-lookup"><span data-stu-id="b32c3-787">Parameters - top100mm</span></span>

<span data-ttu-id="b32c3-788">topExclBorder</span><span class="sxs-lookup"><span data-stu-id="b32c3-788">topExclBorder</span></span>  

### <a name="return-value---top100mm"></a><span data-ttu-id="b32c3-789">戻り値 - top100mm</span><span class="sxs-lookup"><span data-stu-id="b32c3-789">Return Value - top100mm</span></span>

## <a name="method-top100mminclborder"></a><span data-ttu-id="b32c3-790">メソッド top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b32c3-790">Method top100mmInclBorder</span></span>

```xpp
public int top100mmInclBorder([int topInclBorder])
```

### <a name="parameters---top100mminclborder"></a><span data-ttu-id="b32c3-791">パラメーター - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b32c3-791">Parameters - top100mmInclBorder</span></span>

<span data-ttu-id="b32c3-792">topInclBorder</span><span class="sxs-lookup"><span data-stu-id="b32c3-792">topInclBorder</span></span>  

### <a name="return-value---top100mminclborder"></a><span data-ttu-id="b32c3-793">戻り値 - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b32c3-793">Return Value - top100mmInclBorder</span></span>

## <a name="method-topmarginandframe"></a><span data-ttu-id="b32c3-794">メソッド topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="b32c3-794">Method topMarginAndFrame</span></span>

```xpp
public int topMarginAndFrame()
```

### <a name="return-value---topmarginandframe"></a><span data-ttu-id="b32c3-795">戻り値 - topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="b32c3-795">Return Value - topMarginAndFrame</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="b32c3-796">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-796">Method topMarginMode</span></span>

```xpp
public int topMarginMode([int value])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="b32c3-797">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-797">Parameters - topMarginMode</span></span>

<span data-ttu-id="b32c3-798">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-798">value</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="b32c3-799">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-799">Return Value - topMarginMode</span></span>

## <a name="method-topmarginstr"></a><span data-ttu-id="b32c3-800">メソッド topMarginStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-800">Method topMarginStr</span></span>

```xpp
public str topMarginStr([str value])
```

### <a name="parameters---topmarginstr"></a><span data-ttu-id="b32c3-801">パラメーター - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-801">Parameters - topMarginStr</span></span>

<span data-ttu-id="b32c3-802">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-802">value</span></span>  

### <a name="return-value---topmarginstr"></a><span data-ttu-id="b32c3-803">戻り値 - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-803">Return Value - topMarginStr</span></span>

## <a name="method-topmarginunit"></a><span data-ttu-id="b32c3-804">メソッド topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-804">Method topMarginUnit</span></span>

```xpp
public Units topMarginUnit([Units value])
```

### <a name="parameters---topmarginunit"></a><span data-ttu-id="b32c3-805">パラメーター - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-805">Parameters - topMarginUnit</span></span>

<span data-ttu-id="b32c3-806">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-806">value</span></span>  

### <a name="return-value---topmarginunit"></a><span data-ttu-id="b32c3-807">戻り値 - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-807">Return Value - topMarginUnit</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="b32c3-808">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-808">Method topMarginValue</span></span>

```xpp
public Real topMarginValue([Real value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="b32c3-809">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-809">Parameters - topMarginValue</span></span>

<span data-ttu-id="b32c3-810">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-810">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="b32c3-811">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-811">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="b32c3-812">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-812">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="b32c3-813">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-813">Parameters - topMode</span></span>

<span data-ttu-id="b32c3-814">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-814">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="b32c3-815">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-815">Return Value - topMode</span></span>

## <a name="method-topstr"></a><span data-ttu-id="b32c3-816">メソッド topStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-816">Method topStr</span></span>

```xpp
public str topStr([str value])
```

### <a name="parameters---topstr"></a><span data-ttu-id="b32c3-817">パラメーター - topStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-817">Parameters - topStr</span></span>

<span data-ttu-id="b32c3-818">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-818">value</span></span>  

### <a name="return-value---topstr"></a><span data-ttu-id="b32c3-819">戻り値 - topStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-819">Return Value - topStr</span></span>

## <a name="method-topunit"></a><span data-ttu-id="b32c3-820">メソッド topUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-820">Method topUnit</span></span>

```xpp
public Units topUnit([Units value])
```

### <a name="parameters---topunit"></a><span data-ttu-id="b32c3-821">パラメーター - topUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-821">Parameters - topUnit</span></span>

<span data-ttu-id="b32c3-822">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-822">value</span></span>  

### <a name="return-value---topunit"></a><span data-ttu-id="b32c3-823">戻り値 - topUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-823">Return Value - topUnit</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="b32c3-824">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-824">Method topValue</span></span>

```xpp
public Real topValue([Real value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="b32c3-825">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-825">Parameters - topValue</span></span>

<span data-ttu-id="b32c3-826">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-826">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="b32c3-827">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-827">Return Value - topValue</span></span>

## <a name="method-underline"></a><span data-ttu-id="b32c3-828">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="b32c3-828">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="b32c3-829">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="b32c3-829">Parameters - underline</span></span>

<span data-ttu-id="b32c3-830">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-830">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="b32c3-831">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="b32c3-831">Return Value - underline</span></span>

## <a name="method-visible"></a><span data-ttu-id="b32c3-832">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="b32c3-832">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="b32c3-833">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="b32c3-833">Parameters - visible</span></span>

<span data-ttu-id="b32c3-834">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-834">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="b32c3-835">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="b32c3-835">Return Value - visible</span></span>

## <a name="method-webmenuitemname"></a><span data-ttu-id="b32c3-836">メソッド webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="b32c3-836">Method webMenuItemName</span></span>

```xpp
public str webMenuItemName([str value])
```

### <a name="parameters---webmenuitemname"></a><span data-ttu-id="b32c3-837">パラメーター - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="b32c3-837">Parameters - webMenuItemName</span></span>

<span data-ttu-id="b32c3-838">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-838">value</span></span>  

### <a name="return-value---webmenuitemname"></a><span data-ttu-id="b32c3-839">戻り値 - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="b32c3-839">Return Value - webMenuItemName</span></span>

## <a name="method-webmenuitemtype"></a><span data-ttu-id="b32c3-840">メソッド webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="b32c3-840">Method webMenuItemType</span></span>

```xpp
public WebMenuItemType webMenuItemType([WebMenuItemType value])
```

### <a name="parameters---webmenuitemtype"></a><span data-ttu-id="b32c3-841">パラメーター - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="b32c3-841">Parameters - webMenuItemType</span></span>

<span data-ttu-id="b32c3-842">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-842">value</span></span>  

### <a name="return-value---webmenuitemtype"></a><span data-ttu-id="b32c3-843">戻り値 - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="b32c3-843">Return Value - webMenuItemType</span></span>

## <a name="method-webtarget"></a><span data-ttu-id="b32c3-844">メソッド webTarget</span><span class="sxs-lookup"><span data-stu-id="b32c3-844">Method webTarget</span></span>

```xpp
public str webTarget([str value])
```

### <a name="parameters---webtarget"></a><span data-ttu-id="b32c3-845">パラメーター - webTarget</span><span class="sxs-lookup"><span data-stu-id="b32c3-845">Parameters - webTarget</span></span>

<span data-ttu-id="b32c3-846">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-846">value</span></span>  

### <a name="return-value---webtarget"></a><span data-ttu-id="b32c3-847">戻り値 - webTarget</span><span class="sxs-lookup"><span data-stu-id="b32c3-847">Return Value - webTarget</span></span>

## <a name="method-width100mm"></a><span data-ttu-id="b32c3-848">メソッド width100mm</span><span class="sxs-lookup"><span data-stu-id="b32c3-848">Method width100mm</span></span>

```xpp
public int width100mm([int widthExclBorder])
```

### <a name="parameters---width100mm"></a><span data-ttu-id="b32c3-849">パラメーター - width100mm</span><span class="sxs-lookup"><span data-stu-id="b32c3-849">Parameters - width100mm</span></span>

<span data-ttu-id="b32c3-850">widthExclBorder</span><span class="sxs-lookup"><span data-stu-id="b32c3-850">widthExclBorder</span></span>  

### <a name="return-value---width100mm"></a><span data-ttu-id="b32c3-851">戻り値 - width100mm</span><span class="sxs-lookup"><span data-stu-id="b32c3-851">Return Value - width100mm</span></span>

## <a name="method-width100mminclborder"></a><span data-ttu-id="b32c3-852">メソッド width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b32c3-852">Method width100mmInclBorder</span></span>

```xpp
public int width100mmInclBorder([int widthInclBorder])
```

### <a name="parameters---width100mminclborder"></a><span data-ttu-id="b32c3-853">パラメーター - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b32c3-853">Parameters - width100mmInclBorder</span></span>

<span data-ttu-id="b32c3-854">widthInclBorder</span><span class="sxs-lookup"><span data-stu-id="b32c3-854">widthInclBorder</span></span>  

### <a name="return-value---width100mminclborder"></a><span data-ttu-id="b32c3-855">戻り値 - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="b32c3-855">Return Value - width100mmInclBorder</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="b32c3-856">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-856">Method widthMode</span></span>

<span data-ttu-id="b32c3-857">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-857">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="b32c3-858">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-858">Parameters - widthMode</span></span>

<span data-ttu-id="b32c3-859">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-859">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="b32c3-860">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-860">Return Value - widthMode</span></span>

<span data-ttu-id="b32c3-861">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b32c3-861">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="b32c3-862">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="b32c3-862">Remarks - widthMode</span></span>

<span data-ttu-id="b32c3-863">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="b32c3-863">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="b32c3-864">モード。</span><span class="sxs-lookup"><span data-stu-id="b32c3-864">Mode.</span></span>         | <span data-ttu-id="b32c3-865">幅計算。</span><span class="sxs-lookup"><span data-stu-id="b32c3-865">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b32c3-866">正確。</span><span class="sxs-lookup"><span data-stu-id="b32c3-866">Exact.</span></span>        | <span data-ttu-id="b32c3-867">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b32c3-867">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b32c3-868">自動。</span><span class="sxs-lookup"><span data-stu-id="b32c3-868">Auto.</span></span>         | <span data-ttu-id="b32c3-869">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b32c3-869">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b32c3-870">列の幅。</span><span class="sxs-lookup"><span data-stu-id="b32c3-870">Column width.</span></span> | <span data-ttu-id="b32c3-871">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="b32c3-871">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="b32c3-872">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="b32c3-872">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthofstring100mm"></a><span data-ttu-id="b32c3-873">メソッド widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="b32c3-873">Method widthOfString100mm</span></span>

```xpp
public int widthOfString100mm(str string)
```

### <a name="parameters---widthofstring100mm"></a><span data-ttu-id="b32c3-874">パラメーター - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="b32c3-874">Parameters - widthOfString100mm</span></span>

<span data-ttu-id="b32c3-875">文字列</span><span class="sxs-lookup"><span data-stu-id="b32c3-875">string</span></span>  

### <a name="return-value---widthofstring100mm"></a><span data-ttu-id="b32c3-876">戻り値 - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="b32c3-876">Return Value - widthOfString100mm</span></span>

## <a name="method-widthstr"></a><span data-ttu-id="b32c3-877">メソッド widthStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-877">Method widthStr</span></span>

```xpp
public str widthStr([str value])
```

### <a name="parameters---widthstr"></a><span data-ttu-id="b32c3-878">パラメーター - widthStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-878">Parameters - widthStr</span></span>

<span data-ttu-id="b32c3-879">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-879">value</span></span>  

### <a name="return-value---widthstr"></a><span data-ttu-id="b32c3-880">戻り値 - widthStr</span><span class="sxs-lookup"><span data-stu-id="b32c3-880">Return Value - widthStr</span></span>

## <a name="method-widthunit"></a><span data-ttu-id="b32c3-881">メソッド widthUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-881">Method widthUnit</span></span>

```xpp
public Units widthUnit([Units value])
```

### <a name="parameters---widthunit"></a><span data-ttu-id="b32c3-882">パラメーター - widthUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-882">Parameters - widthUnit</span></span>

<span data-ttu-id="b32c3-883">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-883">value</span></span>  

### <a name="return-value---widthunit"></a><span data-ttu-id="b32c3-884">戻り値 - widthUnit</span><span class="sxs-lookup"><span data-stu-id="b32c3-884">Return Value - widthUnit</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="b32c3-885">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-885">Method widthValue</span></span>

<span data-ttu-id="b32c3-886">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-886">Gets or sets the width of the control.</span></span>

```xpp
public Real widthValue([Real value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="b32c3-887">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-887">Parameters - widthValue</span></span>

<span data-ttu-id="b32c3-888">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-888">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="b32c3-889">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-889">Return Value - widthValue</span></span>

<span data-ttu-id="b32c3-890">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="b32c3-890">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="b32c3-891">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="b32c3-891">Remarks - widthValue</span></span>

<span data-ttu-id="b32c3-892">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-892">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-left"></a><span data-ttu-id="b32c3-893">メソッド left</span><span class="sxs-lookup"><span data-stu-id="b32c3-893">Method left</span></span>

```xpp
public void left(Real value, Units unit)
```

### <a name="parameters---left"></a><span data-ttu-id="b32c3-894">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="b32c3-894">Parameters - left</span></span>

<span data-ttu-id="b32c3-895">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-895">value</span></span>  

<!-- -->

<span data-ttu-id="b32c3-896">単位</span><span class="sxs-lookup"><span data-stu-id="b32c3-896">unit</span></span>  

## <a name="method-top"></a><span data-ttu-id="b32c3-897">メソッド top</span><span class="sxs-lookup"><span data-stu-id="b32c3-897">Method top</span></span>

```xpp
public void top(Real value, Units unit)
```

### <a name="parameters---top"></a><span data-ttu-id="b32c3-898">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="b32c3-898">Parameters - top</span></span>

<span data-ttu-id="b32c3-899">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-899">value</span></span>  

<!-- -->

<span data-ttu-id="b32c3-900">単位</span><span class="sxs-lookup"><span data-stu-id="b32c3-900">unit</span></span>  

## <a name="method-topmargin"></a><span data-ttu-id="b32c3-901">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="b32c3-901">Method topMargin</span></span>

```xpp
public void topMargin(Real value, Units unit)
```

### <a name="parameters---topmargin"></a><span data-ttu-id="b32c3-902">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="b32c3-902">Parameters - topMargin</span></span>

<span data-ttu-id="b32c3-903">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-903">value</span></span>  

<!-- -->

<span data-ttu-id="b32c3-904">単位</span><span class="sxs-lookup"><span data-stu-id="b32c3-904">unit</span></span>  

## <a name="method-leftmargin"></a><span data-ttu-id="b32c3-905">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="b32c3-905">Method leftMargin</span></span>

```xpp
public void leftMargin(Real value, Units unit)
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="b32c3-906">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="b32c3-906">Parameters - leftMargin</span></span>

<span data-ttu-id="b32c3-907">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-907">value</span></span>  

<!-- -->

<span data-ttu-id="b32c3-908">単位</span><span class="sxs-lookup"><span data-stu-id="b32c3-908">unit</span></span>  

## <a name="method-labelwidth"></a><span data-ttu-id="b32c3-909">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="b32c3-909">Method labelWidth</span></span>

```xpp
public void labelWidth(Real value, Units unit)
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="b32c3-910">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="b32c3-910">Parameters - labelWidth</span></span>

<span data-ttu-id="b32c3-911">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-911">value</span></span>  

<!-- -->

<span data-ttu-id="b32c3-912">単位</span><span class="sxs-lookup"><span data-stu-id="b32c3-912">unit</span></span>  

## <a name="method-width"></a><span data-ttu-id="b32c3-913">メソッド width</span><span class="sxs-lookup"><span data-stu-id="b32c3-913">Method width</span></span>

<span data-ttu-id="b32c3-914">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-914">Gets or sets the width of the control.</span></span>

```xpp
public void width(Real value, Units unit)
```

### <a name="parameters---width"></a><span data-ttu-id="b32c3-915">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="b32c3-915">Parameters - width</span></span>

<span data-ttu-id="b32c3-916">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-916">value</span></span>  

<!-- -->

<span data-ttu-id="b32c3-917">単位</span><span class="sxs-lookup"><span data-stu-id="b32c3-917">unit</span></span>  

### <a name="remarks---width"></a><span data-ttu-id="b32c3-918">備考 - width</span><span class="sxs-lookup"><span data-stu-id="b32c3-918">Remarks - width</span></span>

<span data-ttu-id="b32c3-919">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b32c3-919">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="b32c3-920">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="b32c3-920">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="b32c3-921">モード。</span><span class="sxs-lookup"><span data-stu-id="b32c3-921">Mode.</span></span>           | <span data-ttu-id="b32c3-922">幅計算。</span><span class="sxs-lookup"><span data-stu-id="b32c3-922">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b32c3-923">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="b32c3-923">-1 Exact.</span></span>       | <span data-ttu-id="b32c3-924">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b32c3-924">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b32c3-925">0 自動。</span><span class="sxs-lookup"><span data-stu-id="b32c3-925">0 Auto.</span></span>         | <span data-ttu-id="b32c3-926">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b32c3-926">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b32c3-927">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="b32c3-927">1 Column width.</span></span> | <span data-ttu-id="b32c3-928">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="b32c3-928">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="b32c3-929">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="b32c3-929">The width and width calculation mode can be set separately.</span></span>

## <a name="method-hide"></a><span data-ttu-id="b32c3-930">メソッド hide</span><span class="sxs-lookup"><span data-stu-id="b32c3-930">Method hide</span></span>

```xpp
public void hide()
```

## <a name="method-height"></a><span data-ttu-id="b32c3-931">メソッド height</span><span class="sxs-lookup"><span data-stu-id="b32c3-931">Method height</span></span>

<span data-ttu-id="b32c3-932">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b32c3-932">Gets or sets the height of the control.</span></span>

```xpp
public void height(Real value, Units unit)
```

### <a name="parameters---height"></a><span data-ttu-id="b32c3-933">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="b32c3-933">Parameters - height</span></span>

<span data-ttu-id="b32c3-934">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-934">value</span></span>  

<!-- -->

<span data-ttu-id="b32c3-935">単位</span><span class="sxs-lookup"><span data-stu-id="b32c3-935">unit</span></span>  

### <a name="remarks---height"></a><span data-ttu-id="b32c3-936">備考 - height</span><span class="sxs-lookup"><span data-stu-id="b32c3-936">Remarks - height</span></span>

<span data-ttu-id="b32c3-937">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b32c3-937">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="b32c3-938">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="b32c3-938">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="b32c3-939">モード。</span><span class="sxs-lookup"><span data-stu-id="b32c3-939">Mode.</span></span>            | <span data-ttu-id="b32c3-940">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="b32c3-940">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b32c3-941">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="b32c3-941">-1 Exact.</span></span>        | <span data-ttu-id="b32c3-942">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b32c3-942">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b32c3-943">0 自動。</span><span class="sxs-lookup"><span data-stu-id="b32c3-943">0 Auto.</span></span>          | <span data-ttu-id="b32c3-944">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b32c3-944">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b32c3-945">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="b32c3-945">1 Column height.</span></span> | <span data-ttu-id="b32c3-946">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="b32c3-946">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="b32c3-947">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="b32c3-947">The height and height calculation mode can be set separately.</span></span>

## <a name="method-show"></a><span data-ttu-id="b32c3-948">メソッド show</span><span class="sxs-lookup"><span data-stu-id="b32c3-948">Method show</span></span>

```xpp
public void show()
```

## <a name="method-bottommargin"></a><span data-ttu-id="b32c3-949">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="b32c3-949">Method bottomMargin</span></span>

```xpp
public void bottomMargin(Real value, Units unit)
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="b32c3-950">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="b32c3-950">Parameters - bottomMargin</span></span>

<span data-ttu-id="b32c3-951">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-951">value</span></span>  

<!-- -->

<span data-ttu-id="b32c3-952">単位</span><span class="sxs-lookup"><span data-stu-id="b32c3-952">unit</span></span>  

## <a name="method-rightmargin"></a><span data-ttu-id="b32c3-953">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="b32c3-953">Method rightMargin</span></span>

```xpp
public void rightMargin(Real value, Units unit)
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="b32c3-954">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="b32c3-954">Parameters - rightMargin</span></span>

<span data-ttu-id="b32c3-955">値</span><span class="sxs-lookup"><span data-stu-id="b32c3-955">value</span></span>  

<!-- -->

<span data-ttu-id="b32c3-956">単位</span><span class="sxs-lookup"><span data-stu-id="b32c3-956">unit</span></span>  

