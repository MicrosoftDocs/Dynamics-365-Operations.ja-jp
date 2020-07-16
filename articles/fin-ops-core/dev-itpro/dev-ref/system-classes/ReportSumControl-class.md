---
title: ReportSumControl クラス
description: このトピックでは、ReportSumControl クラスについて説明します。
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
ms.openlocfilehash: 1143aed7b26a1615e6e989ebef3930ce888ae7f5
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502827"
---
# <a name="class-reportsumcontrol"></a><span data-ttu-id="32aa5-103">クラス ReportSumControl</span><span class="sxs-lookup"><span data-stu-id="32aa5-103">Class ReportSumControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ReportSumControl extends ReportControl
```

<span data-ttu-id="32aa5-104">ReportSumcontrol クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="32aa5-104">The ReportSumcontrol class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="32aa5-105">備考</span><span class="sxs-lookup"><span data-stu-id="32aa5-105">Remarks</span></span>

<span data-ttu-id="32aa5-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="32aa5-107">例</span><span class="sxs-lookup"><span data-stu-id="32aa5-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="32aa5-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="32aa5-108">Methods</span></span>

| <span data-ttu-id="32aa5-109">方法</span><span class="sxs-lookup"><span data-stu-id="32aa5-109">Method</span></span>                                                                   | <span data-ttu-id="32aa5-110">説明</span><span class="sxs-lookup"><span data-stu-id="32aa5-110">Description</span></span>                                                                                                                       |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32aa5-111">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-111">public int alignment(\[int value\])</span></span>                                      |                                                                                                                                   |
| <span data-ttu-id="32aa5-112">public int allowNegative(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-112">public int allowNegative(\[int value\])</span></span>                                  |                                                                                                                                   |
| <span data-ttu-id="32aa5-113">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-113">public int arrayIndex(\[int value\])</span></span>                                     |                                                                                                                                   |
| <span data-ttu-id="32aa5-114">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-114">public boolean autoDeclaration(\[boolean value\])</span></span>                        | <span data-ttu-id="32aa5-115">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-115">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                |
| <span data-ttu-id="32aa5-116">public int autoInsSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-116">public int autoInsSeparator(\[int value\])</span></span>                               |                                                                                                                                   |
| <span data-ttu-id="32aa5-117">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-117">public int backgroundColor(\[int value\])</span></span>                                | <span data-ttu-id="32aa5-118">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-118">Gets or sets the background color of the control.</span></span>                                                                                 |
| <span data-ttu-id="32aa5-119">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-119">public int backStyle(\[int value\])</span></span>                                      | <span data-ttu-id="32aa5-120">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-120">Determines whether the control background can be transparent.</span></span>                                                                    |
| <span data-ttu-id="32aa5-121">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-121">public int bold(\[int value\])</span></span>                                           | <span data-ttu-id="32aa5-122">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-122">Gets or sets the weight of font used to output text in the control.</span></span>                                                               |
| <span data-ttu-id="32aa5-123">public int bottomMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="32aa5-123">public int bottomMarginAndFrame()</span></span>                                        |                                                                                                                                   |
| <span data-ttu-id="32aa5-124">public int bottomMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-124">public int bottomMarginMode(\[int value\])</span></span>                               |                                                                                                                                   |
| <span data-ttu-id="32aa5-125">public str bottomMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-125">public str bottomMarginStr(\[str value\])</span></span>                                |                                                                                                                                   |
| <span data-ttu-id="32aa5-126">public Units bottomMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-126">public Units bottomMarginUnit(\[Units value\])</span></span>                           |                                                                                                                                   |
| <span data-ttu-id="32aa5-127">public Real bottomMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-127">public Real bottomMarginValue(\[Real value\])</span></span>                            |                                                                                                                                   |
| <span data-ttu-id="32aa5-128">public int changeLabelCase(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-128">public int changeLabelCase(\[int value\])</span></span>                                |                                                                                                                                   |
| <span data-ttu-id="32aa5-129">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-129">public int characterSet(\[int value\])</span></span>                                   | <span data-ttu-id="32aa5-130">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-130">Gets or sets the character set of the font.</span></span>                                                                                       |
| <span data-ttu-id="32aa5-131">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-131">public int colorScheme(\[int value\])</span></span>                                    | <span data-ttu-id="32aa5-132">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-132">Gets or sets the color scheme of the control.</span></span>                                                                                     |
| <span data-ttu-id="32aa5-133">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-133">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="32aa5-134">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-134">Gets or sets the configuration key that is assigned to the control.</span></span>                                                               |
| <span data-ttu-id="32aa5-135">public ReportFieldType controlType()</span><span class="sxs-lookup"><span data-stu-id="32aa5-135">public ReportFieldType controlType()</span></span>                                     |                                                                                                                                   |
| <span data-ttu-id="32aa5-136">public str cssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-136">public str cssClass(\[str value\])</span></span>                                       |                                                                                                                                   |
| <span data-ttu-id="32aa5-137">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-137">public FieldId dataField(\[FieldId value\])</span></span>                              |                                                                                                                                   |
| <span data-ttu-id="32aa5-138">public str dataFieldName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-138">public str dataFieldName(\[str value\])</span></span>                                  |                                                                                                                                   |
| <span data-ttu-id="32aa5-139">public int decimalSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-139">public int decimalSeparator(\[int value\])</span></span>                               |                                                                                                                                   |
| <span data-ttu-id="32aa5-140">public int delete()</span><span class="sxs-lookup"><span data-stu-id="32aa5-140">public int delete()</span></span>                                                      |                                                                                                                                   |
| <span data-ttu-id="32aa5-141">public int displaceNegative(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-141">public int displaceNegative(\[int value\], \[AutoMode mode\])</span></span>            |                                                                                                                                   |
| <span data-ttu-id="32aa5-142">public AutoMode displaceNegativeMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-142">public AutoMode displaceNegativeMode(\[AutoMode mode\])</span></span>                  |                                                                                                                                   |
| <span data-ttu-id="32aa5-143">public int displaceNegativeValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-143">public int displaceNegativeValue(\[int value\])</span></span>                          |                                                                                                                                   |
| <span data-ttu-id="32aa5-144">public str effectiveFont()</span><span class="sxs-lookup"><span data-stu-id="32aa5-144">public str effectiveFont()</span></span>                                               |                                                                                                                                   |
| <span data-ttu-id="32aa5-145">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-145">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>         |                                                                                                                                   |
| <span data-ttu-id="32aa5-146">public int extraSumWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-146">public int extraSumWidthMode(\[int value\])</span></span>                              |                                                                                                                                   |
| <span data-ttu-id="32aa5-147">public str extraSumWidthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-147">public str extraSumWidthStr(\[str value\])</span></span>                               |                                                                                                                                   |
| <span data-ttu-id="32aa5-148">public Units extraSumWidthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-148">public Units extraSumWidthUnit(\[Units value\])</span></span>                          |                                                                                                                                   |
| <span data-ttu-id="32aa5-149">public Real extraSumWidthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-149">public Real extraSumWidthValue(\[Real value\])</span></span>                           |                                                                                                                                   |
| <span data-ttu-id="32aa5-150">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-150">public str font(\[str value\])</span></span>                                           | <span data-ttu-id="32aa5-151">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-151">Gets or sets the name of the font for the control to use.</span></span>                                                                         |
| <span data-ttu-id="32aa5-152">public str fontInfoPrinter()</span><span class="sxs-lookup"><span data-stu-id="32aa5-152">public str fontInfoPrinter()</span></span>                                             |                                                                                                                                   |
| <span data-ttu-id="32aa5-153">public int fontInfoPrinterAscent()</span><span class="sxs-lookup"><span data-stu-id="32aa5-153">public int fontInfoPrinterAscent()</span></span>                                       |                                                                                                                                   |
| <span data-ttu-id="32aa5-154">public int fontInfoPrinterDescent()</span><span class="sxs-lookup"><span data-stu-id="32aa5-154">public int fontInfoPrinterDescent()</span></span>                                      |                                                                                                                                   |
| <span data-ttu-id="32aa5-155">public int fontInfoPrinterExtLead()</span><span class="sxs-lookup"><span data-stu-id="32aa5-155">public int fontInfoPrinterExtLead()</span></span>                                      |                                                                                                                                   |
| <span data-ttu-id="32aa5-156">public int fontInfoPrinterHeight()</span><span class="sxs-lookup"><span data-stu-id="32aa5-156">public int fontInfoPrinterHeight()</span></span>                                       |                                                                                                                                   |
| <span data-ttu-id="32aa5-157">public int fontInfoPrinterIntLead()</span><span class="sxs-lookup"><span data-stu-id="32aa5-157">public int fontInfoPrinterIntLead()</span></span>                                      |                                                                                                                                   |
| <span data-ttu-id="32aa5-158">public str fontInfoScreen()</span><span class="sxs-lookup"><span data-stu-id="32aa5-158">public str fontInfoScreen()</span></span>                                              |                                                                                                                                   |
| <span data-ttu-id="32aa5-159">public int fontInfoScreenAscent()</span><span class="sxs-lookup"><span data-stu-id="32aa5-159">public int fontInfoScreenAscent()</span></span>                                        |                                                                                                                                   |
| <span data-ttu-id="32aa5-160">public int fontInfoScreenDescent()</span><span class="sxs-lookup"><span data-stu-id="32aa5-160">public int fontInfoScreenDescent()</span></span>                                       |                                                                                                                                   |
| <span data-ttu-id="32aa5-161">public int fontInfoScreenExtLead()</span><span class="sxs-lookup"><span data-stu-id="32aa5-161">public int fontInfoScreenExtLead()</span></span>                                       |                                                                                                                                   |
| <span data-ttu-id="32aa5-162">public int fontInfoScreenHeight()</span><span class="sxs-lookup"><span data-stu-id="32aa5-162">public int fontInfoScreenHeight()</span></span>                                        |                                                                                                                                   |
| <span data-ttu-id="32aa5-163">public int fontInfoScreenIntLead()</span><span class="sxs-lookup"><span data-stu-id="32aa5-163">public int fontInfoScreenIntLead()</span></span>                                       |                                                                                                                                   |
| <span data-ttu-id="32aa5-164">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-164">public int fontSize(\[int value\])</span></span>                                       | <span data-ttu-id="32aa5-165">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-165">Gets or sets the size of the font for the control to use.</span></span>                                                                         |
| <span data-ttu-id="32aa5-166">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-166">public int foregroundColor(\[int value\])</span></span>                                | <span data-ttu-id="32aa5-167">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-167">Gets or sets the text color for the control to use.</span></span>                                                                               |
| <span data-ttu-id="32aa5-168">public int formatMST(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-168">public int formatMST(\[int value\])</span></span>                                      |                                                                                                                                   |
| <span data-ttu-id="32aa5-169">public int height100mm(\[int heightExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-169">public int height100mm(\[int heightExclBorder\])</span></span>                         |                                                                                                                                   |
| <span data-ttu-id="32aa5-170">public int height100mmInclBorder(\[int heightInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-170">public int height100mmInclBorder(\[int heightInclBorder\])</span></span>               |                                                                                                                                   |
| <span data-ttu-id="32aa5-171">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-171">public int heightMode(\[int value\])</span></span>                                     | <span data-ttu-id="32aa5-172">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-172">Gets or sets a calculation mode for the height of the control.</span></span>                                                                    |
| <span data-ttu-id="32aa5-173">public int heightOfWordWrappedString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="32aa5-173">public int heightOfWordWrappedString100mm(str string)</span></span>                    |                                                                                                                                   |
| <span data-ttu-id="32aa5-174">public str heightStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-174">public str heightStr(\[str value\])</span></span>                                      |                                                                                                                                   |
| <span data-ttu-id="32aa5-175">public Units heightUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-175">public Units heightUnit(\[Units value\])</span></span>                                 |                                                                                                                                   |
| <span data-ttu-id="32aa5-176">public Real heightValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-176">public Real heightValue(\[Real value\])</span></span>                                  | <span data-ttu-id="32aa5-177">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-177">Gets or sets the height of the control.</span></span>                                                                                           |
| <span data-ttu-id="32aa5-178">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-178">public boolean italic(\[boolean value\])</span></span>                                 |                                                                                                                                   |
| <span data-ttu-id="32aa5-179">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-179">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="32aa5-180">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-180">Gets or sets the label for a control.</span></span>                                                                                             |
| <span data-ttu-id="32aa5-181">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-181">public int labelBold(\[int value\])</span></span>                                      |                                                                                                                                   |
| <span data-ttu-id="32aa5-182">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-182">public int labelCharacterSet(\[int value\])</span></span>                              |                                                                                                                                   |
| <span data-ttu-id="32aa5-183">public str labelCssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-183">public str labelCssClass(\[str value\])</span></span>                                  |                                                                                                                                   |
| <span data-ttu-id="32aa5-184">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-184">public str labelFont(\[str value\])</span></span>                                      |                                                                                                                                   |
| <span data-ttu-id="32aa5-185">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-185">public int labelFontSize(\[int value\])</span></span>                                  |                                                                                                                                   |
| <span data-ttu-id="32aa5-186">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-186">public boolean labelItalic(\[boolean value\])</span></span>                            |                                                                                                                                   |
| <span data-ttu-id="32aa5-187">public LineType labelLineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-187">public LineType labelLineBelow(\[LineType value\])</span></span>                       |                                                                                                                                   |
| <span data-ttu-id="32aa5-188">public LineThickness labelLineThickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-188">public LineThickness labelLineThickness(\[LineThickness value\])</span></span>         |                                                                                                                                   |
| <span data-ttu-id="32aa5-189">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-189">public int labelPosition(\[int value\])</span></span>                                  |                                                                                                                                   |
| <span data-ttu-id="32aa5-190">public int labelTabLeader(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-190">public int labelTabLeader(\[int value\])</span></span>                                 |                                                                                                                                   |
| <span data-ttu-id="32aa5-191">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-191">public boolean labelUnderline(\[boolean value\])</span></span>                         |                                                                                                                                   |
| <span data-ttu-id="32aa5-192">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-192">public int labelWidthMode(\[int value\])</span></span>                                 |                                                                                                                                   |
| <span data-ttu-id="32aa5-193">public str labelWidthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-193">public str labelWidthStr(\[str value\])</span></span>                                  |                                                                                                                                   |
| <span data-ttu-id="32aa5-194">public Units labelWidthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-194">public Units labelWidthUnit(\[Units value\])</span></span>                             |                                                                                                                                   |
| <span data-ttu-id="32aa5-195">public Real labelWidthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-195">public Real labelWidthValue(\[Real value\])</span></span>                              |                                                                                                                                   |
| <span data-ttu-id="32aa5-196">public int left100mm(\[int leftExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-196">public int left100mm(\[int leftExclBorder\])</span></span>                             |                                                                                                                                   |
| <span data-ttu-id="32aa5-197">public int left100mmInclBorder(\[int leftInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-197">public int left100mmInclBorder(\[int leftInclBorder\])</span></span>                   |                                                                                                                                   |
| <span data-ttu-id="32aa5-198">public int leftMarginAnFrame()</span><span class="sxs-lookup"><span data-stu-id="32aa5-198">public int leftMarginAnFrame()</span></span>                                           |                                                                                                                                   |
| <span data-ttu-id="32aa5-199">public int leftMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-199">public int leftMarginMode(\[int value\])</span></span>                                 |                                                                                                                                   |
| <span data-ttu-id="32aa5-200">public str leftMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-200">public str leftMarginStr(\[str value\])</span></span>                                  |                                                                                                                                   |
| <span data-ttu-id="32aa5-201">public Units leftMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-201">public Units leftMarginUnit(\[Units value\])</span></span>                             |                                                                                                                                   |
| <span data-ttu-id="32aa5-202">public Real leftMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-202">public Real leftMarginValue(\[Real value\])</span></span>                              |                                                                                                                                   |
| <span data-ttu-id="32aa5-203">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-203">public int leftMode(\[int value\])</span></span>                                       |                                                                                                                                   |
| <span data-ttu-id="32aa5-204">public str leftStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-204">public str leftStr(\[str value\])</span></span>                                        |                                                                                                                                   |
| <span data-ttu-id="32aa5-205">public Units leftUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-205">public Units leftUnit(\[Units value\])</span></span>                                   |                                                                                                                                   |
| <span data-ttu-id="32aa5-206">public Real leftValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-206">public Real leftValue(\[Real value\])</span></span>                                    |                                                                                                                                   |
| <span data-ttu-id="32aa5-207">public LineType lineAbove(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-207">public LineType lineAbove(\[LineType value\])</span></span>                            |                                                                                                                                   |
| <span data-ttu-id="32aa5-208">public LineType lineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-208">public LineType lineBelow(\[LineType value\])</span></span>                            |                                                                                                                                   |
| <span data-ttu-id="32aa5-209">public LineType lineLeft(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-209">public LineType lineLeft(\[LineType value\])</span></span>                             | <span data-ttu-id="32aa5-210">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-210">Gets or sets the type of line that is used as the left border of a section.</span></span>                                                       |
| <span data-ttu-id="32aa5-211">public LineType lineRight(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-211">public LineType lineRight(\[LineType value\])</span></span>                            |                                                                                                                                   |
| <span data-ttu-id="32aa5-212">public str menuItemLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-212">public str menuItemLabel(\[str value\])</span></span>                                  |                                                                                                                                   |
| <span data-ttu-id="32aa5-213">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-213">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                                   |
| <span data-ttu-id="32aa5-214">public MenuItemType menuItemType(\[MenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-214">public MenuItemType menuItemType(\[MenuItemType value\])</span></span>                 |                                                                                                                                   |
| <span data-ttu-id="32aa5-215">public int minNoOfDecimals(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-215">public int minNoOfDecimals(\[int value\], \[AutoMode mode\])</span></span>             |                                                                                                                                   |
| <span data-ttu-id="32aa5-216">public AutoMode minNoOfDecimalsMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-216">public AutoMode minNoOfDecimalsMode(\[AutoMode mode\])</span></span>                   |                                                                                                                                   |
| <span data-ttu-id="32aa5-217">public int minNoOfDecimalsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-217">public int minNoOfDecimalsValue(\[int value\])</span></span>                           |                                                                                                                                   |
| <span data-ttu-id="32aa5-218">public str modelFieldName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-218">public str modelFieldName(\[str value\])</span></span>                                 |                                                                                                                                   |
| <span data-ttu-id="32aa5-219">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-219">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="32aa5-220">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-220">Gets or sets the name used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="32aa5-221">public int noOfDecimals(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-221">public int noOfDecimals(\[int value\], \[AutoMode mode\])</span></span>                |                                                                                                                                   |
| <span data-ttu-id="32aa5-222">public AutoMode noOfDecimalsMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-222">public AutoMode noOfDecimalsMode(\[AutoMode mode\])</span></span>                      |                                                                                                                                   |
| <span data-ttu-id="32aa5-223">public int noOfDecimalsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-223">public int noOfDecimalsValue(\[int value\])</span></span>                              |                                                                                                                                   |
| <span data-ttu-id="32aa5-224">public int numberOfLines(int height100mm)</span><span class="sxs-lookup"><span data-stu-id="32aa5-224">public int numberOfLines(int height100mm)</span></span>                                |                                                                                                                                   |
| <span data-ttu-id="32aa5-225">public int position(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-225">public int position(\[int value\])</span></span>                                       |                                                                                                                                   |
| <span data-ttu-id="32aa5-226">public str previewInfo(str string)</span><span class="sxs-lookup"><span data-stu-id="32aa5-226">public str previewInfo(str string)</span></span>                                       |                                                                                                                                   |
| <span data-ttu-id="32aa5-227">public int previewXCompensation100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="32aa5-227">public int previewXCompensation100mm(str string)</span></span>                         |                                                                                                                                   |
| <span data-ttu-id="32aa5-228">public int right100mm()</span><span class="sxs-lookup"><span data-stu-id="32aa5-228">public int right100mm()</span></span>                                                  |                                                                                                                                   |
| <span data-ttu-id="32aa5-229">public int right100mmInclBorder()</span><span class="sxs-lookup"><span data-stu-id="32aa5-229">public int right100mmInclBorder()</span></span>                                        |                                                                                                                                   |
| <span data-ttu-id="32aa5-230">public int rightMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="32aa5-230">public int rightMarginAndFrame()</span></span>                                         |                                                                                                                                   |
| <span data-ttu-id="32aa5-231">public int rightMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-231">public int rightMarginMode(\[int value\])</span></span>                                |                                                                                                                                   |
| <span data-ttu-id="32aa5-232">public str rightMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-232">public str rightMarginStr(\[str value\])</span></span>                                 |                                                                                                                                   |
| <span data-ttu-id="32aa5-233">public Units rightMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-233">public Units rightMarginUnit(\[Units value\])</span></span>                            |                                                                                                                                   |
| <span data-ttu-id="32aa5-234">public Real rightMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-234">public Real rightMarginValue(\[Real value\])</span></span>                             |                                                                                                                                   |
| <span data-ttu-id="32aa5-235">public int rotateSign(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-235">public int rotateSign(\[int value\])</span></span>                                     |                                                                                                                                   |
| <span data-ttu-id="32aa5-236">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-236">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                                   |
| <span data-ttu-id="32aa5-237">public str setHeightGetText(int lines, str string)</span><span class="sxs-lookup"><span data-stu-id="32aa5-237">public str setHeightGetText(int lines, str string)</span></span>                       |                                                                                                                                   |
| <span data-ttu-id="32aa5-238">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-238">public boolean showLabel(\[boolean value\])</span></span>                              |                                                                                                                                   |
| <span data-ttu-id="32aa5-239">public int showZero(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-239">public int showZero(\[int value\])</span></span>                                       |                                                                                                                                   |
| <span data-ttu-id="32aa5-240">public int signDisplay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-240">public int signDisplay(\[int value\])</span></span>                                    |                                                                                                                                   |
| <span data-ttu-id="32aa5-241">public int sumType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-241">public int sumType(\[int value\])</span></span>                                        |                                                                                                                                   |
| <span data-ttu-id="32aa5-242">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-242">public TableId table(\[TableId value\])</span></span>                                  | <span data-ttu-id="32aa5-243">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-243">Gets or sets the table ID associated with the object.</span></span>                                                                             |
| <span data-ttu-id="32aa5-244">public LineThickness thickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-244">public LineThickness thickness(\[LineThickness value\])</span></span>                  |                                                                                                                                   |
| <span data-ttu-id="32aa5-245">public int thousandSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-245">public int thousandSeparator(\[int value\])</span></span>                              |                                                                                                                                   |
| <span data-ttu-id="32aa5-246">public int top100mm(\[int topExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-246">public int top100mm(\[int topExclBorder\])</span></span>                               |                                                                                                                                   |
| <span data-ttu-id="32aa5-247">public int top100mmInclBorder(\[int topInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-247">public int top100mmInclBorder(\[int topInclBorder\])</span></span>                     |                                                                                                                                   |
| <span data-ttu-id="32aa5-248">public int topMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="32aa5-248">public int topMarginAndFrame()</span></span>                                           |                                                                                                                                   |
| <span data-ttu-id="32aa5-249">public int topMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-249">public int topMarginMode(\[int value\])</span></span>                                  |                                                                                                                                   |
| <span data-ttu-id="32aa5-250">public str topMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-250">public str topMarginStr(\[str value\])</span></span>                                   |                                                                                                                                   |
| <span data-ttu-id="32aa5-251">public Units topMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-251">public Units topMarginUnit(\[Units value\])</span></span>                              |                                                                                                                                   |
| <span data-ttu-id="32aa5-252">public Real topMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-252">public Real topMarginValue(\[Real value\])</span></span>                               |                                                                                                                                   |
| <span data-ttu-id="32aa5-253">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-253">public int topMode(\[int value\])</span></span>                                        |                                                                                                                                   |
| <span data-ttu-id="32aa5-254">public str topStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-254">public str topStr(\[str value\])</span></span>                                         |                                                                                                                                   |
| <span data-ttu-id="32aa5-255">public Units topUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-255">public Units topUnit(\[Units value\])</span></span>                                    |                                                                                                                                   |
| <span data-ttu-id="32aa5-256">public Real topValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-256">public Real topValue(\[Real value\])</span></span>                                     |                                                                                                                                   |
| <span data-ttu-id="32aa5-257">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-257">public boolean underline(\[boolean value\])</span></span>                              |                                                                                                                                   |
| <span data-ttu-id="32aa5-258">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-258">public boolean visible(\[boolean value\])</span></span>                                |                                                                                                                                   |
| <span data-ttu-id="32aa5-259">public str webMenuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-259">public str webMenuItemName(\[str value\])</span></span>                                |                                                                                                                                   |
| <span data-ttu-id="32aa5-260">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-260">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span></span>        |                                                                                                                                   |
| <span data-ttu-id="32aa5-261">public str webTarget(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-261">public str webTarget(\[str value\])</span></span>                                      |                                                                                                                                   |
| <span data-ttu-id="32aa5-262">public int width100mm(\[int widthExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-262">public int width100mm(\[int widthExclBorder\])</span></span>                           |                                                                                                                                   |
| <span data-ttu-id="32aa5-263">public int width100mmInclBorder(\[int widthInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-263">public int width100mmInclBorder(\[int widthInclBorder\])</span></span>                 |                                                                                                                                   |
| <span data-ttu-id="32aa5-264">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-264">public int widthMode(\[int value\])</span></span>                                      | <span data-ttu-id="32aa5-265">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-265">Gets or sets the calculation mode of the width of the control.</span></span>                                                                    |
| <span data-ttu-id="32aa5-266">public int widthOfString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="32aa5-266">public int widthOfString100mm(str string)</span></span>                                |                                                                                                                                   |
| <span data-ttu-id="32aa5-267">public str widthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-267">public str widthStr(\[str value\])</span></span>                                       |                                                                                                                                   |
| <span data-ttu-id="32aa5-268">public Units widthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-268">public Units widthUnit(\[Units value\])</span></span>                                  |                                                                                                                                   |
| <span data-ttu-id="32aa5-269">public Real widthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="32aa5-269">public Real widthValue(\[Real value\])</span></span>                                   | <span data-ttu-id="32aa5-270">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-270">Gets or sets the width of the control.</span></span>                                                                                            |
| <span data-ttu-id="32aa5-271">public void top(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="32aa5-271">public void top(Real value, Units unit)</span></span>                                  |                                                                                                                                   |
| <span data-ttu-id="32aa5-272">public void topMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="32aa5-272">public void topMargin(Real value, Units unit)</span></span>                            |                                                                                                                                   |
| <span data-ttu-id="32aa5-273">public void bottomMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="32aa5-273">public void bottomMargin(Real value, Units unit)</span></span>                         |                                                                                                                                   |
| <span data-ttu-id="32aa5-274">public void rightMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="32aa5-274">public void rightMargin(Real value, Units unit)</span></span>                          |                                                                                                                                   |
| <span data-ttu-id="32aa5-275">public void leftMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="32aa5-275">public void leftMargin(Real value, Units unit)</span></span>                           |                                                                                                                                   |
| <span data-ttu-id="32aa5-276">public void show()</span><span class="sxs-lookup"><span data-stu-id="32aa5-276">public void show()</span></span>                                                       |                                                                                                                                   |
| <span data-ttu-id="32aa5-277">public void left(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="32aa5-277">public void left(Real value, Units unit)</span></span>                                 |                                                                                                                                   |
| <span data-ttu-id="32aa5-278">public void width(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="32aa5-278">public void width(Real value, Units unit)</span></span>                                | <span data-ttu-id="32aa5-279">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-279">Gets or sets the width of the control.</span></span>                                                                                            |
| <span data-ttu-id="32aa5-280">public void extraSumWidth(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="32aa5-280">public void extraSumWidth(Real value, Units unit)</span></span>                        |                                                                                                                                   |
| <span data-ttu-id="32aa5-281">public void labelWidth(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="32aa5-281">public void labelWidth(Real value, Units unit)</span></span>                           |                                                                                                                                   |
| <span data-ttu-id="32aa5-282">public void hide()</span><span class="sxs-lookup"><span data-stu-id="32aa5-282">public void hide()</span></span>                                                       |                                                                                                                                   |
| <span data-ttu-id="32aa5-283">public void height(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="32aa5-283">public void height(Real value, Units unit)</span></span>                               | <span data-ttu-id="32aa5-284">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-284">Gets or sets the height of the control.</span></span>                                                                                           |

## <a name="method-alignment"></a><span data-ttu-id="32aa5-285">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="32aa5-285">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="32aa5-286">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="32aa5-286">Parameters - alignment</span></span>

<span data-ttu-id="32aa5-287">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-287">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="32aa5-288">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="32aa5-288">Return Value - alignment</span></span>

## <a name="method-allownegative"></a><span data-ttu-id="32aa5-289">メソッド allowNegative</span><span class="sxs-lookup"><span data-stu-id="32aa5-289">Method allowNegative</span></span>

```xpp
public int allowNegative([int value])
```

### <a name="parameters---allownegative"></a><span data-ttu-id="32aa5-290">パラメーター - allowNegative</span><span class="sxs-lookup"><span data-stu-id="32aa5-290">Parameters - allowNegative</span></span>

<span data-ttu-id="32aa5-291">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-291">value</span></span>  

### <a name="return-value---allownegative"></a><span data-ttu-id="32aa5-292">戻り値 - allowNegative</span><span class="sxs-lookup"><span data-stu-id="32aa5-292">Return Value - allowNegative</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="32aa5-293">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="32aa5-293">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="32aa5-294">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="32aa5-294">Parameters - arrayIndex</span></span>

<span data-ttu-id="32aa5-295">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-295">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="32aa5-296">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="32aa5-296">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="32aa5-297">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="32aa5-297">Method autoDeclaration</span></span>

<span data-ttu-id="32aa5-298">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-298">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="32aa5-299">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="32aa5-299">Parameters - autoDeclaration</span></span>

<span data-ttu-id="32aa5-300">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-300">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="32aa5-301">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="32aa5-301">Return Value - autoDeclaration</span></span>

<span data-ttu-id="32aa5-302">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="32aa5-302">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="32aa5-303">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="32aa5-303">Remarks - autoDeclaration</span></span>

<span data-ttu-id="32aa5-304">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="32aa5-304">Controls cannot have identical names.</span></span>

## <a name="method-autoinsseparator"></a><span data-ttu-id="32aa5-305">メソッド autoInsSeparator</span><span class="sxs-lookup"><span data-stu-id="32aa5-305">Method autoInsSeparator</span></span>

```xpp
public int autoInsSeparator([int value])
```

### <a name="parameters---autoinsseparator"></a><span data-ttu-id="32aa5-306">パラメーター - autoInsSeparator</span><span class="sxs-lookup"><span data-stu-id="32aa5-306">Parameters - autoInsSeparator</span></span>

<span data-ttu-id="32aa5-307">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-307">value</span></span>  

### <a name="return-value---autoinsseparator"></a><span data-ttu-id="32aa5-308">戻り値 - autoInsSeparator</span><span class="sxs-lookup"><span data-stu-id="32aa5-308">Return Value - autoInsSeparator</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="32aa5-309">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="32aa5-309">Method backgroundColor</span></span>

<span data-ttu-id="32aa5-310">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-310">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="32aa5-311">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="32aa5-311">Parameters - backgroundColor</span></span>

<span data-ttu-id="32aa5-312">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-312">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="32aa5-313">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="32aa5-313">Return Value - backgroundColor</span></span>

<span data-ttu-id="32aa5-314">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="32aa5-314">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="32aa5-315">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="32aa5-315">Remarks - backgroundColor</span></span>

<span data-ttu-id="32aa5-316">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="32aa5-316">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="32aa5-317">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="32aa5-317">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="32aa5-318">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="32aa5-318">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="32aa5-319">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="32aa5-319">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="32aa5-320">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="32aa5-320">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="32aa5-321">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="32aa5-321">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="32aa5-322">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="32aa5-322">Method backStyle</span></span>

<span data-ttu-id="32aa5-323">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-323">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="32aa5-324">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="32aa5-324">Parameters - backStyle</span></span>

<span data-ttu-id="32aa5-325">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-325">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="32aa5-326">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="32aa5-326">Return Value - backStyle</span></span>

<span data-ttu-id="32aa5-327">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="32aa5-327">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="32aa5-328">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="32aa5-328">Method bold</span></span>

<span data-ttu-id="32aa5-329">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-329">Gets or sets the weight of font used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="32aa5-330">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="32aa5-330">Parameters - bold</span></span>

<span data-ttu-id="32aa5-331">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-331">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="32aa5-332">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="32aa5-332">Return Value - bold</span></span>

<span data-ttu-id="32aa5-333">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="32aa5-333">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="32aa5-334">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="32aa5-334">Remarks - bold</span></span>

<span data-ttu-id="32aa5-335">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="32aa5-335">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="32aa5-336">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-336">0 Use the default font weight.</span></span>
-   <span data-ttu-id="32aa5-337">1 シン。</span><span class="sxs-lookup"><span data-stu-id="32aa5-337">1 Thin.</span></span>
-   <span data-ttu-id="32aa5-338">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="32aa5-338">2 Extra-light.</span></span>
-   <span data-ttu-id="32aa5-339">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="32aa5-339">3 Light.</span></span>
-   <span data-ttu-id="32aa5-340">4 標準。</span><span class="sxs-lookup"><span data-stu-id="32aa5-340">4 Normal.</span></span>
-   <span data-ttu-id="32aa5-341">5 中。</span><span class="sxs-lookup"><span data-stu-id="32aa5-341">5 Medium.</span></span>
-   <span data-ttu-id="32aa5-342">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="32aa5-342">6 Semibold.</span></span>
-   <span data-ttu-id="32aa5-343">7 太字。</span><span class="sxs-lookup"><span data-stu-id="32aa5-343">7 Bold.</span></span>
-   <span data-ttu-id="32aa5-344">8 極太。</span><span class="sxs-lookup"><span data-stu-id="32aa5-344">8 Extra-bold.</span></span>
-   <span data-ttu-id="32aa5-345">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="32aa5-345">9 Heavy.</span></span>

## <a name="method-bottommarginandframe"></a><span data-ttu-id="32aa5-346">メソッド bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="32aa5-346">Method bottomMarginAndFrame</span></span>

```xpp
public int bottomMarginAndFrame()
```

### <a name="return-value---bottommarginandframe"></a><span data-ttu-id="32aa5-347">戻り値 - bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="32aa5-347">Return Value - bottomMarginAndFrame</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="32aa5-348">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-348">Method bottomMarginMode</span></span>

```xpp
public int bottomMarginMode([int value])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="32aa5-349">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-349">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="32aa5-350">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-350">value</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="32aa5-351">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-351">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginstr"></a><span data-ttu-id="32aa5-352">メソッド bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-352">Method bottomMarginStr</span></span>

```xpp
public str bottomMarginStr([str value])
```

### <a name="parameters---bottommarginstr"></a><span data-ttu-id="32aa5-353">パラメーター - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-353">Parameters - bottomMarginStr</span></span>

<span data-ttu-id="32aa5-354">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-354">value</span></span>  

### <a name="return-value---bottommarginstr"></a><span data-ttu-id="32aa5-355">戻り値 - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-355">Return Value - bottomMarginStr</span></span>

## <a name="method-bottommarginunit"></a><span data-ttu-id="32aa5-356">メソッド bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-356">Method bottomMarginUnit</span></span>

```xpp
public Units bottomMarginUnit([Units value])
```

### <a name="parameters---bottommarginunit"></a><span data-ttu-id="32aa5-357">パラメーター - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-357">Parameters - bottomMarginUnit</span></span>

<span data-ttu-id="32aa5-358">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-358">value</span></span>  

### <a name="return-value---bottommarginunit"></a><span data-ttu-id="32aa5-359">戻り値 - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-359">Return Value - bottomMarginUnit</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="32aa5-360">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-360">Method bottomMarginValue</span></span>

```xpp
public Real bottomMarginValue([Real value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="32aa5-361">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-361">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="32aa5-362">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-362">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="32aa5-363">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-363">Return Value - bottomMarginValue</span></span>

## <a name="method-changelabelcase"></a><span data-ttu-id="32aa5-364">メソッド changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="32aa5-364">Method changeLabelCase</span></span>

```xpp
public int changeLabelCase([int value])
```

### <a name="parameters---changelabelcase"></a><span data-ttu-id="32aa5-365">パラメーター - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="32aa5-365">Parameters - changeLabelCase</span></span>

<span data-ttu-id="32aa5-366">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-366">value</span></span>  

### <a name="return-value---changelabelcase"></a><span data-ttu-id="32aa5-367">戻り値 - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="32aa5-367">Return Value - changeLabelCase</span></span>

## <a name="method-characterset"></a><span data-ttu-id="32aa5-368">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="32aa5-368">Method characterSet</span></span>

<span data-ttu-id="32aa5-369">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-369">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="32aa5-370">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="32aa5-370">Parameters - characterSet</span></span>

<span data-ttu-id="32aa5-371">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-371">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="32aa5-372">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="32aa5-372">Return Value - characterSet</span></span>

<span data-ttu-id="32aa5-373">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="32aa5-373">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="32aa5-374">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="32aa5-374">Remarks - characterSet</span></span>

<span data-ttu-id="32aa5-375">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-375">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="32aa5-376">値です。</span><span class="sxs-lookup"><span data-stu-id="32aa5-376">Value.</span></span> | <span data-ttu-id="32aa5-377">説明。</span><span class="sxs-lookup"><span data-stu-id="32aa5-377">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="32aa5-378">0</span><span class="sxs-lookup"><span data-stu-id="32aa5-378">0</span></span>      | <span data-ttu-id="32aa5-379">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="32aa5-379">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="32aa5-380">1</span><span class="sxs-lookup"><span data-stu-id="32aa5-380">1</span></span>      | <span data-ttu-id="32aa5-381">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="32aa5-381">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="32aa5-382">2</span><span class="sxs-lookup"><span data-stu-id="32aa5-382">2</span></span>      | <span data-ttu-id="32aa5-383">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="32aa5-383">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="32aa5-384">77</span><span class="sxs-lookup"><span data-stu-id="32aa5-384">77</span></span>     | <span data-ttu-id="32aa5-385">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="32aa5-385">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="32aa5-386">128</span><span class="sxs-lookup"><span data-stu-id="32aa5-386">128</span></span>    | <span data-ttu-id="32aa5-387">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="32aa5-387">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="32aa5-388">129</span><span class="sxs-lookup"><span data-stu-id="32aa5-388">129</span></span>    | <span data-ttu-id="32aa5-389">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="32aa5-389">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="32aa5-390">134</span><span class="sxs-lookup"><span data-stu-id="32aa5-390">134</span></span>    | <span data-ttu-id="32aa5-391">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="32aa5-391">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="32aa5-392">136</span><span class="sxs-lookup"><span data-stu-id="32aa5-392">136</span></span>    | <span data-ttu-id="32aa5-393">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="32aa5-393">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="32aa5-394">161</span><span class="sxs-lookup"><span data-stu-id="32aa5-394">161</span></span>    | <span data-ttu-id="32aa5-395">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="32aa5-395">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="32aa5-396">162</span><span class="sxs-lookup"><span data-stu-id="32aa5-396">162</span></span>    | <span data-ttu-id="32aa5-397">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="32aa5-397">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="32aa5-398">163</span><span class="sxs-lookup"><span data-stu-id="32aa5-398">163</span></span>    | <span data-ttu-id="32aa5-399">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="32aa5-399">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="32aa5-400">186</span><span class="sxs-lookup"><span data-stu-id="32aa5-400">186</span></span>    | <span data-ttu-id="32aa5-401">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="32aa5-401">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="32aa5-402">204</span><span class="sxs-lookup"><span data-stu-id="32aa5-402">204</span></span>    | <span data-ttu-id="32aa5-403">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="32aa5-403">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="32aa5-404">238</span><span class="sxs-lookup"><span data-stu-id="32aa5-404">238</span></span>    | <span data-ttu-id="32aa5-405">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="32aa5-405">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="32aa5-406">255</span><span class="sxs-lookup"><span data-stu-id="32aa5-406">255</span></span>    | <span data-ttu-id="32aa5-407">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="32aa5-407">OEM\_CHARSET</span></span>         |

<span data-ttu-id="32aa5-408">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="32aa5-408">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="32aa5-409">値です。</span><span class="sxs-lookup"><span data-stu-id="32aa5-409">Value.</span></span> | <span data-ttu-id="32aa5-410">説明。</span><span class="sxs-lookup"><span data-stu-id="32aa5-410">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="32aa5-411">130</span><span class="sxs-lookup"><span data-stu-id="32aa5-411">130</span></span>    | <span data-ttu-id="32aa5-412">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="32aa5-412">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="32aa5-413">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="32aa5-413">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="32aa5-414">値です。</span><span class="sxs-lookup"><span data-stu-id="32aa5-414">Value.</span></span> | <span data-ttu-id="32aa5-415">説明。</span><span class="sxs-lookup"><span data-stu-id="32aa5-415">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="32aa5-416">177</span><span class="sxs-lookup"><span data-stu-id="32aa5-416">177</span></span>    | <span data-ttu-id="32aa5-417">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="32aa5-417">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="32aa5-418">178</span><span class="sxs-lookup"><span data-stu-id="32aa5-418">178</span></span>    | <span data-ttu-id="32aa5-419">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="32aa5-419">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="32aa5-420">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="32aa5-420">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="32aa5-421">値です。</span><span class="sxs-lookup"><span data-stu-id="32aa5-421">Value.</span></span> | <span data-ttu-id="32aa5-422">説明。</span><span class="sxs-lookup"><span data-stu-id="32aa5-422">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="32aa5-423">222</span><span class="sxs-lookup"><span data-stu-id="32aa5-423">222</span></span>    | <span data-ttu-id="32aa5-424">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="32aa5-424">THAI\_CHARSET</span></span> |

<span data-ttu-id="32aa5-425">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="32aa5-425">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="32aa5-426">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="32aa5-426">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="32aa5-427">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="32aa5-427">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="32aa5-428">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="32aa5-428">Method colorScheme</span></span>

<span data-ttu-id="32aa5-429">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-429">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="32aa5-430">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="32aa5-430">Parameters - colorScheme</span></span>

<span data-ttu-id="32aa5-431">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-431">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="32aa5-432">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="32aa5-432">Return Value - colorScheme</span></span>

<span data-ttu-id="32aa5-433">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="32aa5-433">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="32aa5-434">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="32aa5-434">Remarks - colorScheme</span></span>

<span data-ttu-id="32aa5-435">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="32aa5-435">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="32aa5-436">値です。</span><span class="sxs-lookup"><span data-stu-id="32aa5-436">Value.</span></span> | <span data-ttu-id="32aa5-437">スタイル。</span><span class="sxs-lookup"><span data-stu-id="32aa5-437">Style.</span></span>                 |
|--------|------------------------|
| <span data-ttu-id="32aa5-438">0</span><span class="sxs-lookup"><span data-stu-id="32aa5-438">0</span></span>      | <span data-ttu-id="32aa5-439">既定。</span><span class="sxs-lookup"><span data-stu-id="32aa5-439">Default.</span></span>               |
| <span data-ttu-id="32aa5-440">1</span><span class="sxs-lookup"><span data-stu-id="32aa5-440">1</span></span>      | <span data-ttu-id="32aa5-441">Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="32aa5-441">The Windows palette.</span></span>   |
| <span data-ttu-id="32aa5-442">2</span><span class="sxs-lookup"><span data-stu-id="32aa5-442">2</span></span>      | <span data-ttu-id="32aa5-443">真の配色。</span><span class="sxs-lookup"><span data-stu-id="32aa5-443">The true-color scheme.</span></span> |

## <a name="method-configurationkey"></a><span data-ttu-id="32aa5-444">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="32aa5-444">Method configurationKey</span></span>

<span data-ttu-id="32aa5-445">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-445">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="32aa5-446">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="32aa5-446">Parameters - configurationKey</span></span>

<span data-ttu-id="32aa5-447">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-447">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="32aa5-448">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="32aa5-448">Return Value - configurationKey</span></span>

<span data-ttu-id="32aa5-449">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="32aa5-449">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="32aa5-450">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="32aa5-450">Remarks - configurationKey</span></span>

<span data-ttu-id="32aa5-451">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="32aa5-451">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="32aa5-452">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="32aa5-452">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-controltype"></a><span data-ttu-id="32aa5-453">メソッド controlType</span><span class="sxs-lookup"><span data-stu-id="32aa5-453">Method controlType</span></span>

```xpp
public ReportFieldType controlType()
```

### <a name="return-value---controltype"></a><span data-ttu-id="32aa5-454">戻り値 - controlType</span><span class="sxs-lookup"><span data-stu-id="32aa5-454">Return Value - controlType</span></span>

## <a name="method-cssclass"></a><span data-ttu-id="32aa5-455">メソッド cssClass</span><span class="sxs-lookup"><span data-stu-id="32aa5-455">Method cssClass</span></span>

```xpp
public str cssClass([str value])
```

### <a name="parameters---cssclass"></a><span data-ttu-id="32aa5-456">パラメーター - cssClass</span><span class="sxs-lookup"><span data-stu-id="32aa5-456">Parameters - cssClass</span></span>

<span data-ttu-id="32aa5-457">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-457">value</span></span>  

### <a name="return-value---cssclass"></a><span data-ttu-id="32aa5-458">戻り値 - cssClass</span><span class="sxs-lookup"><span data-stu-id="32aa5-458">Return Value - cssClass</span></span>

## <a name="method-datafield"></a><span data-ttu-id="32aa5-459">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="32aa5-459">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="32aa5-460">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="32aa5-460">Parameters - dataField</span></span>

<span data-ttu-id="32aa5-461">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-461">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="32aa5-462">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="32aa5-462">Return Value - dataField</span></span>

## <a name="method-datafieldname"></a><span data-ttu-id="32aa5-463">メソッド dataFieldName</span><span class="sxs-lookup"><span data-stu-id="32aa5-463">Method dataFieldName</span></span>

```xpp
public str dataFieldName([str value])
```

### <a name="parameters---datafieldname"></a><span data-ttu-id="32aa5-464">パラメーター - dataFieldName</span><span class="sxs-lookup"><span data-stu-id="32aa5-464">Parameters - dataFieldName</span></span>

<span data-ttu-id="32aa5-465">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-465">value</span></span>  

### <a name="return-value---datafieldname"></a><span data-ttu-id="32aa5-466">戻り値 - dataFieldName</span><span class="sxs-lookup"><span data-stu-id="32aa5-466">Return Value - dataFieldName</span></span>

## <a name="method-decimalseparator"></a><span data-ttu-id="32aa5-467">メソッド decimalSeparator</span><span class="sxs-lookup"><span data-stu-id="32aa5-467">Method decimalSeparator</span></span>

```xpp
public int decimalSeparator([int value])
```

### <a name="parameters---decimalseparator"></a><span data-ttu-id="32aa5-468">パラメーター - decimalSeparator</span><span class="sxs-lookup"><span data-stu-id="32aa5-468">Parameters - decimalSeparator</span></span>

<span data-ttu-id="32aa5-469">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-469">value</span></span>  

### <a name="return-value---decimalseparator"></a><span data-ttu-id="32aa5-470">戻り値 - decimalSeparator</span><span class="sxs-lookup"><span data-stu-id="32aa5-470">Return Value - decimalSeparator</span></span>

## <a name="method-delete"></a><span data-ttu-id="32aa5-471">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="32aa5-471">Method delete</span></span>

```xpp
public int delete()
```

### <a name="return-value---delete"></a><span data-ttu-id="32aa5-472">戻り値 - delete</span><span class="sxs-lookup"><span data-stu-id="32aa5-472">Return Value - delete</span></span>

## <a name="method-displacenegative"></a><span data-ttu-id="32aa5-473">メソッド displaceNegative</span><span class="sxs-lookup"><span data-stu-id="32aa5-473">Method displaceNegative</span></span>

```xpp
public int displaceNegative([int value], [AutoMode mode])
```

### <a name="parameters---displacenegative"></a><span data-ttu-id="32aa5-474">パラメーター - displaceNegative</span><span class="sxs-lookup"><span data-stu-id="32aa5-474">Parameters - displaceNegative</span></span>

<span data-ttu-id="32aa5-475">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-475">value</span></span>  

<!-- -->

<span data-ttu-id="32aa5-476">モード</span><span class="sxs-lookup"><span data-stu-id="32aa5-476">mode</span></span>  

### <a name="return-value---displacenegative"></a><span data-ttu-id="32aa5-477">戻り値 - displaceNegative</span><span class="sxs-lookup"><span data-stu-id="32aa5-477">Return Value - displaceNegative</span></span>

## <a name="method-displacenegativemode"></a><span data-ttu-id="32aa5-478">メソッド displaceNegativeMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-478">Method displaceNegativeMode</span></span>

```xpp
public AutoMode displaceNegativeMode([AutoMode mode])
```

### <a name="parameters---displacenegativemode"></a><span data-ttu-id="32aa5-479">パラメーター - displaceNegativeMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-479">Parameters - displaceNegativeMode</span></span>

<span data-ttu-id="32aa5-480">モード</span><span class="sxs-lookup"><span data-stu-id="32aa5-480">mode</span></span>  

### <a name="return-value---displacenegativemode"></a><span data-ttu-id="32aa5-481">戻り値 - displaceNegativeMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-481">Return Value - displaceNegativeMode</span></span>

## <a name="method-displacenegativevalue"></a><span data-ttu-id="32aa5-482">メソッド displaceNegativeValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-482">Method displaceNegativeValue</span></span>

```xpp
public int displaceNegativeValue([int value])
```

### <a name="parameters---displacenegativevalue"></a><span data-ttu-id="32aa5-483">パラメーター - displaceNegativeValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-483">Parameters - displaceNegativeValue</span></span>

<span data-ttu-id="32aa5-484">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-484">value</span></span>  

### <a name="return-value---displacenegativevalue"></a><span data-ttu-id="32aa5-485">戻り値 - displaceNegativeValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-485">Return Value - displaceNegativeValue</span></span>

## <a name="method-effectivefont"></a><span data-ttu-id="32aa5-486">メソッド effectiveFont</span><span class="sxs-lookup"><span data-stu-id="32aa5-486">Method effectiveFont</span></span>

```xpp
public str effectiveFont()
```

### <a name="return-value---effectivefont"></a><span data-ttu-id="32aa5-487">戻り値 - effectiveFont</span><span class="sxs-lookup"><span data-stu-id="32aa5-487">Return Value - effectiveFont</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="32aa5-488">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="32aa5-488">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="32aa5-489">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="32aa5-489">Parameters - extendedDataType</span></span>

<span data-ttu-id="32aa5-490">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-490">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="32aa5-491">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="32aa5-491">Return Value - extendedDataType</span></span>

## <a name="method-extrasumwidthmode"></a><span data-ttu-id="32aa5-492">メソッド extraSumWidthMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-492">Method extraSumWidthMode</span></span>

```xpp
public int extraSumWidthMode([int value])
```

### <a name="parameters---extrasumwidthmode"></a><span data-ttu-id="32aa5-493">パラメーター - extraSumWidthMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-493">Parameters - extraSumWidthMode</span></span>

<span data-ttu-id="32aa5-494">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-494">value</span></span>  

### <a name="return-value---extrasumwidthmode"></a><span data-ttu-id="32aa5-495">戻り値 - extraSumWidthMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-495">Return Value - extraSumWidthMode</span></span>

## <a name="method-extrasumwidthstr"></a><span data-ttu-id="32aa5-496">メソッド extraSumWidthStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-496">Method extraSumWidthStr</span></span>

```xpp
public str extraSumWidthStr([str value])
```

### <a name="parameters---extrasumwidthstr"></a><span data-ttu-id="32aa5-497">パラメーター - extraSumWidthStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-497">Parameters - extraSumWidthStr</span></span>

<span data-ttu-id="32aa5-498">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-498">value</span></span>  

### <a name="return-value---extrasumwidthstr"></a><span data-ttu-id="32aa5-499">戻り値 - extraSumWidthStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-499">Return Value - extraSumWidthStr</span></span>

## <a name="method-extrasumwidthunit"></a><span data-ttu-id="32aa5-500">メソッド extraSumWidthUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-500">Method extraSumWidthUnit</span></span>

```xpp
public Units extraSumWidthUnit([Units value])
```

### <a name="parameters---extrasumwidthunit"></a><span data-ttu-id="32aa5-501">パラメーター - extraSumWidthUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-501">Parameters - extraSumWidthUnit</span></span>

<span data-ttu-id="32aa5-502">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-502">value</span></span>  

### <a name="return-value---extrasumwidthunit"></a><span data-ttu-id="32aa5-503">戻り値 - extraSumWidthUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-503">Return Value - extraSumWidthUnit</span></span>

## <a name="method-extrasumwidthvalue"></a><span data-ttu-id="32aa5-504">メソッド extraSumWidthValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-504">Method extraSumWidthValue</span></span>

```xpp
public Real extraSumWidthValue([Real value])
```

### <a name="parameters---extrasumwidthvalue"></a><span data-ttu-id="32aa5-505">パラメーター - extraSumWidthValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-505">Parameters - extraSumWidthValue</span></span>

<span data-ttu-id="32aa5-506">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-506">value</span></span>  

### <a name="return-value---extrasumwidthvalue"></a><span data-ttu-id="32aa5-507">戻り値 - extraSumWidthValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-507">Return Value - extraSumWidthValue</span></span>

## <a name="method-font"></a><span data-ttu-id="32aa5-508">メソッド font</span><span class="sxs-lookup"><span data-stu-id="32aa5-508">Method font</span></span>

<span data-ttu-id="32aa5-509">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-509">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="32aa5-510">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="32aa5-510">Parameters - font</span></span>

<span data-ttu-id="32aa5-511">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-511">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="32aa5-512">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="32aa5-512">Return Value - font</span></span>

<span data-ttu-id="32aa5-513">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="32aa5-513">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontinfoprinter"></a><span data-ttu-id="32aa5-514">メソッド fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="32aa5-514">Method fontInfoPrinter</span></span>

```xpp
public str fontInfoPrinter()
```

### <a name="return-value---fontinfoprinter"></a><span data-ttu-id="32aa5-515">戻り値 - fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="32aa5-515">Return Value - fontInfoPrinter</span></span>

## <a name="method-fontinfoprinterascent"></a><span data-ttu-id="32aa5-516">メソッド fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="32aa5-516">Method fontInfoPrinterAscent</span></span>

```xpp
public int fontInfoPrinterAscent()
```

### <a name="return-value---fontinfoprinterascent"></a><span data-ttu-id="32aa5-517">戻り値 - fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="32aa5-517">Return Value - fontInfoPrinterAscent</span></span>

## <a name="method-fontinfoprinterdescent"></a><span data-ttu-id="32aa5-518">メソッド fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="32aa5-518">Method fontInfoPrinterDescent</span></span>

```xpp
public int fontInfoPrinterDescent()
```

### <a name="return-value---fontinfoprinterdescent"></a><span data-ttu-id="32aa5-519">戻り値 - fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="32aa5-519">Return Value - fontInfoPrinterDescent</span></span>

## <a name="method-fontinfoprinterextlead"></a><span data-ttu-id="32aa5-520">メソッド fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="32aa5-520">Method fontInfoPrinterExtLead</span></span>

```xpp
public int fontInfoPrinterExtLead()
```

### <a name="return-value---fontinfoprinterextlead"></a><span data-ttu-id="32aa5-521">戻り値 - fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="32aa5-521">Return Value - fontInfoPrinterExtLead</span></span>

## <a name="method-fontinfoprinterheight"></a><span data-ttu-id="32aa5-522">メソッド fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="32aa5-522">Method fontInfoPrinterHeight</span></span>

```xpp
public int fontInfoPrinterHeight()
```

### <a name="return-value---fontinfoprinterheight"></a><span data-ttu-id="32aa5-523">戻り値 - fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="32aa5-523">Return Value - fontInfoPrinterHeight</span></span>

## <a name="method-fontinfoprinterintlead"></a><span data-ttu-id="32aa5-524">メソッド fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="32aa5-524">Method fontInfoPrinterIntLead</span></span>

```xpp
public int fontInfoPrinterIntLead()
```

### <a name="return-value---fontinfoprinterintlead"></a><span data-ttu-id="32aa5-525">戻り値 - fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="32aa5-525">Return Value - fontInfoPrinterIntLead</span></span>

## <a name="method-fontinfoscreen"></a><span data-ttu-id="32aa5-526">メソッド fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="32aa5-526">Method fontInfoScreen</span></span>

```xpp
public str fontInfoScreen()
```

### <a name="return-value---fontinfoscreen"></a><span data-ttu-id="32aa5-527">戻り値 - fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="32aa5-527">Return Value - fontInfoScreen</span></span>

## <a name="method-fontinfoscreenascent"></a><span data-ttu-id="32aa5-528">メソッド fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="32aa5-528">Method fontInfoScreenAscent</span></span>

```xpp
public int fontInfoScreenAscent()
```

### <a name="return-value---fontinfoscreenascent"></a><span data-ttu-id="32aa5-529">戻り値 - fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="32aa5-529">Return Value - fontInfoScreenAscent</span></span>

## <a name="method-fontinfoscreendescent"></a><span data-ttu-id="32aa5-530">メソッド fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="32aa5-530">Method fontInfoScreenDescent</span></span>

```xpp
public int fontInfoScreenDescent()
```

### <a name="return-value---fontinfoscreendescent"></a><span data-ttu-id="32aa5-531">戻り値 - fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="32aa5-531">Return Value - fontInfoScreenDescent</span></span>

## <a name="method-fontinfoscreenextlead"></a><span data-ttu-id="32aa5-532">メソッド fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="32aa5-532">Method fontInfoScreenExtLead</span></span>

```xpp
public int fontInfoScreenExtLead()
```

### <a name="return-value---fontinfoscreenextlead"></a><span data-ttu-id="32aa5-533">戻り値 - fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="32aa5-533">Return Value - fontInfoScreenExtLead</span></span>

## <a name="method-fontinfoscreenheight"></a><span data-ttu-id="32aa5-534">メソッド fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="32aa5-534">Method fontInfoScreenHeight</span></span>

```xpp
public int fontInfoScreenHeight()
```

### <a name="return-value---fontinfoscreenheight"></a><span data-ttu-id="32aa5-535">戻り値 - fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="32aa5-535">Return Value - fontInfoScreenHeight</span></span>

## <a name="method-fontinfoscreenintlead"></a><span data-ttu-id="32aa5-536">メソッド fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="32aa5-536">Method fontInfoScreenIntLead</span></span>

```xpp
public int fontInfoScreenIntLead()
```

### <a name="return-value---fontinfoscreenintlead"></a><span data-ttu-id="32aa5-537">戻り値 - fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="32aa5-537">Return Value - fontInfoScreenIntLead</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="32aa5-538">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="32aa5-538">Method fontSize</span></span>

<span data-ttu-id="32aa5-539">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-539">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="32aa5-540">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="32aa5-540">Parameters - fontSize</span></span>

<span data-ttu-id="32aa5-541">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-541">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="32aa5-542">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="32aa5-542">Return Value - fontSize</span></span>

<span data-ttu-id="32aa5-543">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="32aa5-543">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="32aa5-544">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="32aa5-544">Method foregroundColor</span></span>

<span data-ttu-id="32aa5-545">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-545">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="32aa5-546">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="32aa5-546">Parameters - foregroundColor</span></span>

<span data-ttu-id="32aa5-547">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-547">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="32aa5-548">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="32aa5-548">Return Value - foregroundColor</span></span>

<span data-ttu-id="32aa5-549">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="32aa5-549">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="32aa5-550">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="32aa5-550">Remarks - foregroundColor</span></span>

<span data-ttu-id="32aa5-551">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="32aa5-551">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="32aa5-552">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="32aa5-552">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="32aa5-553">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="32aa5-553">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="32aa5-554">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="32aa5-554">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="32aa5-555">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="32aa5-555">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="32aa5-556">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="32aa5-556">The maximum value for a single byte is 255.</span></span>

## <a name="method-formatmst"></a><span data-ttu-id="32aa5-557">メソッド formatMST</span><span class="sxs-lookup"><span data-stu-id="32aa5-557">Method formatMST</span></span>

```xpp
public int formatMST([int value])
```

### <a name="parameters---formatmst"></a><span data-ttu-id="32aa5-558">パラメーター - formatMST</span><span class="sxs-lookup"><span data-stu-id="32aa5-558">Parameters - formatMST</span></span>

<span data-ttu-id="32aa5-559">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-559">value</span></span>  

### <a name="return-value---formatmst"></a><span data-ttu-id="32aa5-560">戻り値 - formatMST</span><span class="sxs-lookup"><span data-stu-id="32aa5-560">Return Value - formatMST</span></span>

## <a name="method-height100mm"></a><span data-ttu-id="32aa5-561">メソッド height100mm</span><span class="sxs-lookup"><span data-stu-id="32aa5-561">Method height100mm</span></span>

```xpp
public int height100mm([int heightExclBorder])
```

### <a name="parameters---height100mm"></a><span data-ttu-id="32aa5-562">パラメーター - height100mm</span><span class="sxs-lookup"><span data-stu-id="32aa5-562">Parameters - height100mm</span></span>

<span data-ttu-id="32aa5-563">heightExclBorder</span><span class="sxs-lookup"><span data-stu-id="32aa5-563">heightExclBorder</span></span>  

### <a name="return-value---height100mm"></a><span data-ttu-id="32aa5-564">戻り値 - height100mm</span><span class="sxs-lookup"><span data-stu-id="32aa5-564">Return Value - height100mm</span></span>

## <a name="method-height100mminclborder"></a><span data-ttu-id="32aa5-565">メソッド height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="32aa5-565">Method height100mmInclBorder</span></span>

```xpp
public int height100mmInclBorder([int heightInclBorder])
```

### <a name="parameters---height100mminclborder"></a><span data-ttu-id="32aa5-566">パラメーター - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="32aa5-566">Parameters - height100mmInclBorder</span></span>

<span data-ttu-id="32aa5-567">heightInclBorder</span><span class="sxs-lookup"><span data-stu-id="32aa5-567">heightInclBorder</span></span>  

### <a name="return-value---height100mminclborder"></a><span data-ttu-id="32aa5-568">戻り値 - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="32aa5-568">Return Value - height100mmInclBorder</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="32aa5-569">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-569">Method heightMode</span></span>

<span data-ttu-id="32aa5-570">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-570">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="32aa5-571">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-571">Parameters - heightMode</span></span>

<span data-ttu-id="32aa5-572">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-572">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="32aa5-573">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-573">Return Value - heightMode</span></span>

<span data-ttu-id="32aa5-574">計算モード。</span><span class="sxs-lookup"><span data-stu-id="32aa5-574">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="32aa5-575">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-575">Remarks - heightMode</span></span>

<span data-ttu-id="32aa5-576">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="32aa5-576">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="32aa5-577">モード。</span><span class="sxs-lookup"><span data-stu-id="32aa5-577">Mode.</span></span>          | <span data-ttu-id="32aa5-578">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="32aa5-578">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="32aa5-579">正確。</span><span class="sxs-lookup"><span data-stu-id="32aa5-579">Exact.</span></span>         | <span data-ttu-id="32aa5-580">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="32aa5-580">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="32aa5-581">自動。</span><span class="sxs-lookup"><span data-stu-id="32aa5-581">Auto.</span></span>          | <span data-ttu-id="32aa5-582">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="32aa5-582">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="32aa5-583">列の高さ</span><span class="sxs-lookup"><span data-stu-id="32aa5-583">Column height.</span></span> | <span data-ttu-id="32aa5-584">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="32aa5-584">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="32aa5-585">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="32aa5-585">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightofwordwrappedstring100mm"></a><span data-ttu-id="32aa5-586">メソッド heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="32aa5-586">Method heightOfWordWrappedString100mm</span></span>

```xpp
public int heightOfWordWrappedString100mm(str string)
```

### <a name="parameters---heightofwordwrappedstring100mm"></a><span data-ttu-id="32aa5-587">パラメーター - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="32aa5-587">Parameters - heightOfWordWrappedString100mm</span></span>

<span data-ttu-id="32aa5-588">文字列</span><span class="sxs-lookup"><span data-stu-id="32aa5-588">string</span></span>  

### <a name="return-value---heightofwordwrappedstring100mm"></a><span data-ttu-id="32aa5-589">戻り値 - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="32aa5-589">Return Value - heightOfWordWrappedString100mm</span></span>

## <a name="method-heightstr"></a><span data-ttu-id="32aa5-590">メソッド heightStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-590">Method heightStr</span></span>

```xpp
public str heightStr([str value])
```

### <a name="parameters---heightstr"></a><span data-ttu-id="32aa5-591">パラメーター - heightStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-591">Parameters - heightStr</span></span>

<span data-ttu-id="32aa5-592">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-592">value</span></span>  

### <a name="return-value---heightstr"></a><span data-ttu-id="32aa5-593">戻り値 - heightStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-593">Return Value - heightStr</span></span>

## <a name="method-heightunit"></a><span data-ttu-id="32aa5-594">メソッド heightUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-594">Method heightUnit</span></span>

```xpp
public Units heightUnit([Units value])
```

### <a name="parameters---heightunit"></a><span data-ttu-id="32aa5-595">パラメーター - heightUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-595">Parameters - heightUnit</span></span>

<span data-ttu-id="32aa5-596">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-596">value</span></span>  

### <a name="return-value---heightunit"></a><span data-ttu-id="32aa5-597">戻り値 - heightUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-597">Return Value - heightUnit</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="32aa5-598">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-598">Method heightValue</span></span>

<span data-ttu-id="32aa5-599">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-599">Gets or sets the height of the control.</span></span>

```xpp
public Real heightValue([Real value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="32aa5-600">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-600">Parameters - heightValue</span></span>

<span data-ttu-id="32aa5-601">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-601">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="32aa5-602">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-602">Return Value - heightValue</span></span>

<span data-ttu-id="32aa5-603">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="32aa5-603">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="32aa5-604">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-604">Remarks - heightValue</span></span>

<span data-ttu-id="32aa5-605">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="32aa5-605">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-italic"></a><span data-ttu-id="32aa5-606">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="32aa5-606">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="32aa5-607">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="32aa5-607">Parameters - italic</span></span>

<span data-ttu-id="32aa5-608">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-608">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="32aa5-609">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="32aa5-609">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="32aa5-610">メソッド label</span><span class="sxs-lookup"><span data-stu-id="32aa5-610">Method label</span></span>

<span data-ttu-id="32aa5-611">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-611">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="32aa5-612">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="32aa5-612">Parameters - label</span></span>

<span data-ttu-id="32aa5-613">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-613">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="32aa5-614">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="32aa5-614">Return Value - label</span></span>

<span data-ttu-id="32aa5-615">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="32aa5-615">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="32aa5-616">備考 - label</span><span class="sxs-lookup"><span data-stu-id="32aa5-616">Remarks - label</span></span>

<span data-ttu-id="32aa5-617">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-617">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="32aa5-618">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="32aa5-618">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="32aa5-619">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="32aa5-619">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="32aa5-620">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="32aa5-620">Parameters - labelBold</span></span>

<span data-ttu-id="32aa5-621">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-621">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="32aa5-622">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="32aa5-622">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="32aa5-623">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="32aa5-623">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="32aa5-624">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="32aa5-624">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="32aa5-625">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-625">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="32aa5-626">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="32aa5-626">Return Value - labelCharacterSet</span></span>

## <a name="method-labelcssclass"></a><span data-ttu-id="32aa5-627">メソッド labelCssClass</span><span class="sxs-lookup"><span data-stu-id="32aa5-627">Method labelCssClass</span></span>

```xpp
public str labelCssClass([str value])
```

### <a name="parameters---labelcssclass"></a><span data-ttu-id="32aa5-628">パラメーター - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="32aa5-628">Parameters - labelCssClass</span></span>

<span data-ttu-id="32aa5-629">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-629">value</span></span>  

### <a name="return-value---labelcssclass"></a><span data-ttu-id="32aa5-630">戻り値 - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="32aa5-630">Return Value - labelCssClass</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="32aa5-631">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="32aa5-631">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="32aa5-632">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="32aa5-632">Parameters - labelFont</span></span>

<span data-ttu-id="32aa5-633">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-633">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="32aa5-634">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="32aa5-634">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="32aa5-635">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="32aa5-635">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="32aa5-636">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="32aa5-636">Parameters - labelFontSize</span></span>

<span data-ttu-id="32aa5-637">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-637">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="32aa5-638">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="32aa5-638">Return Value - labelFontSize</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="32aa5-639">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="32aa5-639">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="32aa5-640">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="32aa5-640">Parameters - labelItalic</span></span>

<span data-ttu-id="32aa5-641">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-641">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="32aa5-642">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="32aa5-642">Return Value - labelItalic</span></span>

## <a name="method-labellinebelow"></a><span data-ttu-id="32aa5-643">メソッド labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="32aa5-643">Method labelLineBelow</span></span>

```xpp
public LineType labelLineBelow([LineType value])
```

### <a name="parameters---labellinebelow"></a><span data-ttu-id="32aa5-644">パラメーター - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="32aa5-644">Parameters - labelLineBelow</span></span>

<span data-ttu-id="32aa5-645">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-645">value</span></span>  

### <a name="return-value---labellinebelow"></a><span data-ttu-id="32aa5-646">戻り値 - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="32aa5-646">Return Value - labelLineBelow</span></span>

## <a name="method-labellinethickness"></a><span data-ttu-id="32aa5-647">メソッド labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="32aa5-647">Method labelLineThickness</span></span>

```xpp
public LineThickness labelLineThickness([LineThickness value])
```

### <a name="parameters---labellinethickness"></a><span data-ttu-id="32aa5-648">パラメーター - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="32aa5-648">Parameters - labelLineThickness</span></span>

<span data-ttu-id="32aa5-649">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-649">value</span></span>  

### <a name="return-value---labellinethickness"></a><span data-ttu-id="32aa5-650">戻り値 - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="32aa5-650">Return Value - labelLineThickness</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="32aa5-651">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="32aa5-651">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="32aa5-652">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="32aa5-652">Parameters - labelPosition</span></span>

<span data-ttu-id="32aa5-653">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-653">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="32aa5-654">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="32aa5-654">Return Value - labelPosition</span></span>

## <a name="method-labeltableader"></a><span data-ttu-id="32aa5-655">メソッド labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="32aa5-655">Method labelTabLeader</span></span>

```xpp
public int labelTabLeader([int value])
```

### <a name="parameters---labeltableader"></a><span data-ttu-id="32aa5-656">パラメーター - labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="32aa5-656">Parameters - labelTabLeader</span></span>

<span data-ttu-id="32aa5-657">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-657">value</span></span>  

### <a name="return-value---labeltableader"></a><span data-ttu-id="32aa5-658">戻り値 - labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="32aa5-658">Return Value - labelTabLeader</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="32aa5-659">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="32aa5-659">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="32aa5-660">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="32aa5-660">Parameters - labelUnderline</span></span>

<span data-ttu-id="32aa5-661">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-661">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="32aa5-662">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="32aa5-662">Return Value - labelUnderline</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="32aa5-663">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-663">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="32aa5-664">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-664">Parameters - labelWidthMode</span></span>

<span data-ttu-id="32aa5-665">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-665">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="32aa5-666">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-666">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthstr"></a><span data-ttu-id="32aa5-667">メソッド labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-667">Method labelWidthStr</span></span>

```xpp
public str labelWidthStr([str value])
```

### <a name="parameters---labelwidthstr"></a><span data-ttu-id="32aa5-668">パラメーター - labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-668">Parameters - labelWidthStr</span></span>

<span data-ttu-id="32aa5-669">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-669">value</span></span>  

### <a name="return-value---labelwidthstr"></a><span data-ttu-id="32aa5-670">戻り値 - labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-670">Return Value - labelWidthStr</span></span>

## <a name="method-labelwidthunit"></a><span data-ttu-id="32aa5-671">メソッド labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-671">Method labelWidthUnit</span></span>

```xpp
public Units labelWidthUnit([Units value])
```

### <a name="parameters---labelwidthunit"></a><span data-ttu-id="32aa5-672">パラメーター - labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-672">Parameters - labelWidthUnit</span></span>

<span data-ttu-id="32aa5-673">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-673">value</span></span>  

### <a name="return-value---labelwidthunit"></a><span data-ttu-id="32aa5-674">戻り値 - labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-674">Return Value - labelWidthUnit</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="32aa5-675">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-675">Method labelWidthValue</span></span>

```xpp
public Real labelWidthValue([Real value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="32aa5-676">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-676">Parameters - labelWidthValue</span></span>

<span data-ttu-id="32aa5-677">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-677">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="32aa5-678">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-678">Return Value - labelWidthValue</span></span>

## <a name="method-left100mm"></a><span data-ttu-id="32aa5-679">メソッド left100mm</span><span class="sxs-lookup"><span data-stu-id="32aa5-679">Method left100mm</span></span>

```xpp
public int left100mm([int leftExclBorder])
```

### <a name="parameters---left100mm"></a><span data-ttu-id="32aa5-680">パラメーター - left100mm</span><span class="sxs-lookup"><span data-stu-id="32aa5-680">Parameters - left100mm</span></span>

<span data-ttu-id="32aa5-681">leftExclBorder</span><span class="sxs-lookup"><span data-stu-id="32aa5-681">leftExclBorder</span></span>  

### <a name="return-value---left100mm"></a><span data-ttu-id="32aa5-682">戻り値 - left100mm</span><span class="sxs-lookup"><span data-stu-id="32aa5-682">Return Value - left100mm</span></span>

## <a name="method-left100mminclborder"></a><span data-ttu-id="32aa5-683">メソッド left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="32aa5-683">Method left100mmInclBorder</span></span>

```xpp
public int left100mmInclBorder([int leftInclBorder])
```

### <a name="parameters---left100mminclborder"></a><span data-ttu-id="32aa5-684">パラメーター - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="32aa5-684">Parameters - left100mmInclBorder</span></span>

<span data-ttu-id="32aa5-685">leftInclBorder</span><span class="sxs-lookup"><span data-stu-id="32aa5-685">leftInclBorder</span></span>  

### <a name="return-value---left100mminclborder"></a><span data-ttu-id="32aa5-686">戻り値 - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="32aa5-686">Return Value - left100mmInclBorder</span></span>

## <a name="method-leftmarginanframe"></a><span data-ttu-id="32aa5-687">メソッド leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="32aa5-687">Method leftMarginAnFrame</span></span>

```xpp
public int leftMarginAnFrame()
```

### <a name="return-value---leftmarginanframe"></a><span data-ttu-id="32aa5-688">戻り値 - leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="32aa5-688">Return Value - leftMarginAnFrame</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="32aa5-689">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-689">Method leftMarginMode</span></span>

```xpp
public int leftMarginMode([int value])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="32aa5-690">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-690">Parameters - leftMarginMode</span></span>

<span data-ttu-id="32aa5-691">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-691">value</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="32aa5-692">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-692">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginstr"></a><span data-ttu-id="32aa5-693">メソッド leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-693">Method leftMarginStr</span></span>

```xpp
public str leftMarginStr([str value])
```

### <a name="parameters---leftmarginstr"></a><span data-ttu-id="32aa5-694">パラメーター - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-694">Parameters - leftMarginStr</span></span>

<span data-ttu-id="32aa5-695">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-695">value</span></span>  

### <a name="return-value---leftmarginstr"></a><span data-ttu-id="32aa5-696">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-696">Return Value - leftMarginStr</span></span>

## <a name="method-leftmarginunit"></a><span data-ttu-id="32aa5-697">メソッド leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-697">Method leftMarginUnit</span></span>

```xpp
public Units leftMarginUnit([Units value])
```

### <a name="parameters---leftmarginunit"></a><span data-ttu-id="32aa5-698">パラメーター - leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-698">Parameters - leftMarginUnit</span></span>

<span data-ttu-id="32aa5-699">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-699">value</span></span>  

### <a name="return-value---leftmarginunit"></a><span data-ttu-id="32aa5-700">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-700">Return Value - leftMarginUnit</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="32aa5-701">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-701">Method leftMarginValue</span></span>

```xpp
public Real leftMarginValue([Real value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="32aa5-702">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-702">Parameters - leftMarginValue</span></span>

<span data-ttu-id="32aa5-703">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-703">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="32aa5-704">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-704">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="32aa5-705">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-705">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="32aa5-706">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-706">Parameters - leftMode</span></span>

<span data-ttu-id="32aa5-707">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-707">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="32aa5-708">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-708">Return Value - leftMode</span></span>

## <a name="method-leftstr"></a><span data-ttu-id="32aa5-709">メソッド leftStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-709">Method leftStr</span></span>

```xpp
public str leftStr([str value])
```

### <a name="parameters---leftstr"></a><span data-ttu-id="32aa5-710">パラメーター - leftStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-710">Parameters - leftStr</span></span>

<span data-ttu-id="32aa5-711">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-711">value</span></span>  

### <a name="return-value---leftstr"></a><span data-ttu-id="32aa5-712">戻り値 - leftStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-712">Return Value - leftStr</span></span>

## <a name="method-leftunit"></a><span data-ttu-id="32aa5-713">メソッド leftUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-713">Method leftUnit</span></span>

```xpp
public Units leftUnit([Units value])
```

### <a name="parameters---leftunit"></a><span data-ttu-id="32aa5-714">パラメーター - leftUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-714">Parameters - leftUnit</span></span>

<span data-ttu-id="32aa5-715">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-715">value</span></span>  

### <a name="return-value---leftunit"></a><span data-ttu-id="32aa5-716">戻り値 - leftUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-716">Return Value - leftUnit</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="32aa5-717">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-717">Method leftValue</span></span>

```xpp
public Real leftValue([Real value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="32aa5-718">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-718">Parameters - leftValue</span></span>

<span data-ttu-id="32aa5-719">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-719">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="32aa5-720">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-720">Return Value - leftValue</span></span>

## <a name="method-lineabove"></a><span data-ttu-id="32aa5-721">メソッド lineAbove</span><span class="sxs-lookup"><span data-stu-id="32aa5-721">Method lineAbove</span></span>

```xpp
public LineType lineAbove([LineType value])
```

### <a name="parameters---lineabove"></a><span data-ttu-id="32aa5-722">パラメーター - lineAbove</span><span class="sxs-lookup"><span data-stu-id="32aa5-722">Parameters - lineAbove</span></span>

<span data-ttu-id="32aa5-723">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-723">value</span></span>  

### <a name="return-value---lineabove"></a><span data-ttu-id="32aa5-724">戻り値 - lineAbove</span><span class="sxs-lookup"><span data-stu-id="32aa5-724">Return Value - lineAbove</span></span>

## <a name="method-linebelow"></a><span data-ttu-id="32aa5-725">メソッド lineBelow</span><span class="sxs-lookup"><span data-stu-id="32aa5-725">Method lineBelow</span></span>

```xpp
public LineType lineBelow([LineType value])
```

### <a name="parameters---linebelow"></a><span data-ttu-id="32aa5-726">パラメーター - lineBelow</span><span class="sxs-lookup"><span data-stu-id="32aa5-726">Parameters - lineBelow</span></span>

<span data-ttu-id="32aa5-727">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-727">value</span></span>  

### <a name="return-value---linebelow"></a><span data-ttu-id="32aa5-728">戻り値 - lineBelow</span><span class="sxs-lookup"><span data-stu-id="32aa5-728">Return Value - lineBelow</span></span>

## <a name="method-lineleft"></a><span data-ttu-id="32aa5-729">メソッド lineLeft</span><span class="sxs-lookup"><span data-stu-id="32aa5-729">Method lineLeft</span></span>

<span data-ttu-id="32aa5-730">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-730">Gets or sets the type of line that is used as the left border of a section.</span></span>

```xpp
public LineType lineLeft([LineType value])
```

### <a name="parameters---lineleft"></a><span data-ttu-id="32aa5-731">パラメーター - lineLeft</span><span class="sxs-lookup"><span data-stu-id="32aa5-731">Parameters - lineLeft</span></span>

<span data-ttu-id="32aa5-732">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-732">value</span></span>  

### <a name="return-value---lineleft"></a><span data-ttu-id="32aa5-733">戻り値 - lineLeft</span><span class="sxs-lookup"><span data-stu-id="32aa5-733">Return Value - lineLeft</span></span>

<span data-ttu-id="32aa5-734">左境界線として使用される線のタイプ。</span><span class="sxs-lookup"><span data-stu-id="32aa5-734">The type of line that is used as the left border.</span></span>

## <a name="method-lineright"></a><span data-ttu-id="32aa5-735">メソッド lineRight</span><span class="sxs-lookup"><span data-stu-id="32aa5-735">Method lineRight</span></span>

```xpp
public LineType lineRight([LineType value])
```

### <a name="parameters---lineright"></a><span data-ttu-id="32aa5-736">パラメーター - lineRight</span><span class="sxs-lookup"><span data-stu-id="32aa5-736">Parameters - lineRight</span></span>

<span data-ttu-id="32aa5-737">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-737">value</span></span>  

### <a name="return-value---lineright"></a><span data-ttu-id="32aa5-738">戻り値 - lineRight</span><span class="sxs-lookup"><span data-stu-id="32aa5-738">Return Value - lineRight</span></span>

## <a name="method-menuitemlabel"></a><span data-ttu-id="32aa5-739">メソッド menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="32aa5-739">Method menuItemLabel</span></span>

```xpp
public str menuItemLabel([str value])
```

### <a name="parameters---menuitemlabel"></a><span data-ttu-id="32aa5-740">パラメーター - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="32aa5-740">Parameters - menuItemLabel</span></span>

<span data-ttu-id="32aa5-741">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-741">value</span></span>  

### <a name="return-value---menuitemlabel"></a><span data-ttu-id="32aa5-742">戻り値 - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="32aa5-742">Return Value - menuItemLabel</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="32aa5-743">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="32aa5-743">Method menuItemName</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="32aa5-744">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="32aa5-744">Parameters - menuItemName</span></span>

<span data-ttu-id="32aa5-745">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-745">value</span></span>  

### <a name="return-value---menuitemname"></a><span data-ttu-id="32aa5-746">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="32aa5-746">Return Value - menuItemName</span></span>

## <a name="method-menuitemtype"></a><span data-ttu-id="32aa5-747">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="32aa5-747">Method menuItemType</span></span>

```xpp
public MenuItemType menuItemType([MenuItemType value])
```

### <a name="parameters---menuitemtype"></a><span data-ttu-id="32aa5-748">パラメーター - menuItemType</span><span class="sxs-lookup"><span data-stu-id="32aa5-748">Parameters - menuItemType</span></span>

<span data-ttu-id="32aa5-749">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-749">value</span></span>  

### <a name="return-value---menuitemtype"></a><span data-ttu-id="32aa5-750">戻り値 - menuItemType</span><span class="sxs-lookup"><span data-stu-id="32aa5-750">Return Value - menuItemType</span></span>

## <a name="method-minnoofdecimals"></a><span data-ttu-id="32aa5-751">メソッド minNoOfDecimals</span><span class="sxs-lookup"><span data-stu-id="32aa5-751">Method minNoOfDecimals</span></span>

```xpp
public int minNoOfDecimals([int value], [AutoMode mode])
```

### <a name="parameters---minnoofdecimals"></a><span data-ttu-id="32aa5-752">パラメーター - minNoOfDecimals</span><span class="sxs-lookup"><span data-stu-id="32aa5-752">Parameters - minNoOfDecimals</span></span>

<span data-ttu-id="32aa5-753">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-753">value</span></span>  

<!-- -->

<span data-ttu-id="32aa5-754">モード</span><span class="sxs-lookup"><span data-stu-id="32aa5-754">mode</span></span>  

### <a name="return-value---minnoofdecimals"></a><span data-ttu-id="32aa5-755">戻り値 - minNoOfDecimals</span><span class="sxs-lookup"><span data-stu-id="32aa5-755">Return Value - minNoOfDecimals</span></span>

## <a name="method-minnoofdecimalsmode"></a><span data-ttu-id="32aa5-756">メソッド minNoOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-756">Method minNoOfDecimalsMode</span></span>

```xpp
public AutoMode minNoOfDecimalsMode([AutoMode mode])
```

### <a name="parameters---minnoofdecimalsmode"></a><span data-ttu-id="32aa5-757">パラメーター - minNoOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-757">Parameters - minNoOfDecimalsMode</span></span>

<span data-ttu-id="32aa5-758">モード</span><span class="sxs-lookup"><span data-stu-id="32aa5-758">mode</span></span>  

### <a name="return-value---minnoofdecimalsmode"></a><span data-ttu-id="32aa5-759">戻り値 - minNoOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-759">Return Value - minNoOfDecimalsMode</span></span>

## <a name="method-minnoofdecimalsvalue"></a><span data-ttu-id="32aa5-760">メソッド minNoOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-760">Method minNoOfDecimalsValue</span></span>

```xpp
public int minNoOfDecimalsValue([int value])
```

### <a name="parameters---minnoofdecimalsvalue"></a><span data-ttu-id="32aa5-761">パラメーター - minNoOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-761">Parameters - minNoOfDecimalsValue</span></span>

<span data-ttu-id="32aa5-762">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-762">value</span></span>  

### <a name="return-value---minnoofdecimalsvalue"></a><span data-ttu-id="32aa5-763">戻り値 - minNoOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-763">Return Value - minNoOfDecimalsValue</span></span>

## <a name="method-modelfieldname"></a><span data-ttu-id="32aa5-764">メソッド modelFieldName</span><span class="sxs-lookup"><span data-stu-id="32aa5-764">Method modelFieldName</span></span>

```xpp
public str modelFieldName([str value])
```

### <a name="parameters---modelfieldname"></a><span data-ttu-id="32aa5-765">パラメーター - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="32aa5-765">Parameters - modelFieldName</span></span>

<span data-ttu-id="32aa5-766">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-766">value</span></span>  

### <a name="return-value---modelfieldname"></a><span data-ttu-id="32aa5-767">戻り値 - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="32aa5-767">Return Value - modelFieldName</span></span>

## <a name="method-name"></a><span data-ttu-id="32aa5-768">メソッド名</span><span class="sxs-lookup"><span data-stu-id="32aa5-768">Method name</span></span>

<span data-ttu-id="32aa5-769">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-769">Gets or sets the name used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="32aa5-770">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="32aa5-770">Parameters - name</span></span>

<span data-ttu-id="32aa5-771">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-771">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="32aa5-772">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="32aa5-772">Return Value - name</span></span>

<span data-ttu-id="32aa5-773">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="32aa5-773">The name used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="32aa5-774">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="32aa5-774">Remarks - name</span></span>

<span data-ttu-id="32aa5-775">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="32aa5-775">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="32aa5-776">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="32aa5-776">Begins with a letter.</span></span>
-   <span data-ttu-id="32aa5-777">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="32aa5-777">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="32aa5-778">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="32aa5-778">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="32aa5-779">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="32aa5-779">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="32aa5-780">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="32aa5-780">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-noofdecimals"></a><span data-ttu-id="32aa5-781">メソッド noOfDecimals</span><span class="sxs-lookup"><span data-stu-id="32aa5-781">Method noOfDecimals</span></span>

```xpp
public int noOfDecimals([int value], [AutoMode mode])
```

### <a name="parameters---noofdecimals"></a><span data-ttu-id="32aa5-782">パラメーター - noOfDecimals</span><span class="sxs-lookup"><span data-stu-id="32aa5-782">Parameters - noOfDecimals</span></span>

<span data-ttu-id="32aa5-783">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-783">value</span></span>  

<!-- -->

<span data-ttu-id="32aa5-784">モード</span><span class="sxs-lookup"><span data-stu-id="32aa5-784">mode</span></span>  

### <a name="return-value---noofdecimals"></a><span data-ttu-id="32aa5-785">戻り値 - noOfDecimals</span><span class="sxs-lookup"><span data-stu-id="32aa5-785">Return Value - noOfDecimals</span></span>

## <a name="method-noofdecimalsmode"></a><span data-ttu-id="32aa5-786">メソッド noOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-786">Method noOfDecimalsMode</span></span>

```xpp
public AutoMode noOfDecimalsMode([AutoMode mode])
```

### <a name="parameters---noofdecimalsmode"></a><span data-ttu-id="32aa5-787">パラメーター - noOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-787">Parameters - noOfDecimalsMode</span></span>

<span data-ttu-id="32aa5-788">モード</span><span class="sxs-lookup"><span data-stu-id="32aa5-788">mode</span></span>  

### <a name="return-value---noofdecimalsmode"></a><span data-ttu-id="32aa5-789">戻り値 - noOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-789">Return Value - noOfDecimalsMode</span></span>

## <a name="method-noofdecimalsvalue"></a><span data-ttu-id="32aa5-790">メソッド noOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-790">Method noOfDecimalsValue</span></span>

```xpp
public int noOfDecimalsValue([int value])
```

### <a name="parameters---noofdecimalsvalue"></a><span data-ttu-id="32aa5-791">パラメーター - noOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-791">Parameters - noOfDecimalsValue</span></span>

<span data-ttu-id="32aa5-792">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-792">value</span></span>  

### <a name="return-value---noofdecimalsvalue"></a><span data-ttu-id="32aa5-793">戻り値 - noOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-793">Return Value - noOfDecimalsValue</span></span>

## <a name="method-numberoflines"></a><span data-ttu-id="32aa5-794">メソッド numberOfLines</span><span class="sxs-lookup"><span data-stu-id="32aa5-794">Method numberOfLines</span></span>

```xpp
public int numberOfLines(int height100mm)
```

### <a name="parameters---numberoflines"></a><span data-ttu-id="32aa5-795">パラメーター - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="32aa5-795">Parameters - numberOfLines</span></span>

<span data-ttu-id="32aa5-796">height100mm</span><span class="sxs-lookup"><span data-stu-id="32aa5-796">height100mm</span></span>  

### <a name="return-value---numberoflines"></a><span data-ttu-id="32aa5-797">戻り値 - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="32aa5-797">Return Value - numberOfLines</span></span>

## <a name="method-position"></a><span data-ttu-id="32aa5-798">メソッドの位置</span><span class="sxs-lookup"><span data-stu-id="32aa5-798">Method position</span></span>

```xpp
public int position([int value])
```

### <a name="parameters---position"></a><span data-ttu-id="32aa5-799">パラメーター - position</span><span class="sxs-lookup"><span data-stu-id="32aa5-799">Parameters - position</span></span>

<span data-ttu-id="32aa5-800">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-800">value</span></span>  

### <a name="return-value---position"></a><span data-ttu-id="32aa5-801">戻り値 - position</span><span class="sxs-lookup"><span data-stu-id="32aa5-801">Return Value - position</span></span>

## <a name="method-previewinfo"></a><span data-ttu-id="32aa5-802">メソッド previewInfo</span><span class="sxs-lookup"><span data-stu-id="32aa5-802">Method previewInfo</span></span>

```xpp
public str previewInfo(str string)
```

### <a name="parameters---previewinfo"></a><span data-ttu-id="32aa5-803">パラメーター - previewInfo</span><span class="sxs-lookup"><span data-stu-id="32aa5-803">Parameters - previewInfo</span></span>

<span data-ttu-id="32aa5-804">文字列</span><span class="sxs-lookup"><span data-stu-id="32aa5-804">string</span></span>  

### <a name="return-value---previewinfo"></a><span data-ttu-id="32aa5-805">戻り値 - previewInfo</span><span class="sxs-lookup"><span data-stu-id="32aa5-805">Return Value - previewInfo</span></span>

## <a name="method-previewxcompensation100mm"></a><span data-ttu-id="32aa5-806">メソッド previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="32aa5-806">Method previewXCompensation100mm</span></span>

```xpp
public int previewXCompensation100mm(str string)
```

### <a name="parameters---previewxcompensation100mm"></a><span data-ttu-id="32aa5-807">パラメーター - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="32aa5-807">Parameters - previewXCompensation100mm</span></span>

<span data-ttu-id="32aa5-808">文字列</span><span class="sxs-lookup"><span data-stu-id="32aa5-808">string</span></span>  

### <a name="return-value---previewxcompensation100mm"></a><span data-ttu-id="32aa5-809">戻り値 - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="32aa5-809">Return Value - previewXCompensation100mm</span></span>

## <a name="method-right100mm"></a><span data-ttu-id="32aa5-810">メソッド right100mm</span><span class="sxs-lookup"><span data-stu-id="32aa5-810">Method right100mm</span></span>

```xpp
public int right100mm()
```

### <a name="return-value---right100mm"></a><span data-ttu-id="32aa5-811">戻り値 - right100mm</span><span class="sxs-lookup"><span data-stu-id="32aa5-811">Return Value - right100mm</span></span>

## <a name="method-right100mminclborder"></a><span data-ttu-id="32aa5-812">メソッド right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="32aa5-812">Method right100mmInclBorder</span></span>

```xpp
public int right100mmInclBorder()
```

### <a name="return-value---right100mminclborder"></a><span data-ttu-id="32aa5-813">戻り値 - right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="32aa5-813">Return Value - right100mmInclBorder</span></span>

## <a name="method-rightmarginandframe"></a><span data-ttu-id="32aa5-814">メソッド rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="32aa5-814">Method rightMarginAndFrame</span></span>

```xpp
public int rightMarginAndFrame()
```

### <a name="return-value---rightmarginandframe"></a><span data-ttu-id="32aa5-815">戻り値 - rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="32aa5-815">Return Value - rightMarginAndFrame</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="32aa5-816">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-816">Method rightMarginMode</span></span>

```xpp
public int rightMarginMode([int value])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="32aa5-817">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-817">Parameters - rightMarginMode</span></span>

<span data-ttu-id="32aa5-818">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-818">value</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="32aa5-819">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-819">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginstr"></a><span data-ttu-id="32aa5-820">メソッド rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-820">Method rightMarginStr</span></span>

```xpp
public str rightMarginStr([str value])
```

### <a name="parameters---rightmarginstr"></a><span data-ttu-id="32aa5-821">パラメーター - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-821">Parameters - rightMarginStr</span></span>

<span data-ttu-id="32aa5-822">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-822">value</span></span>  

### <a name="return-value---rightmarginstr"></a><span data-ttu-id="32aa5-823">戻り値 - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-823">Return Value - rightMarginStr</span></span>

## <a name="method-rightmarginunit"></a><span data-ttu-id="32aa5-824">メソッド rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-824">Method rightMarginUnit</span></span>

```xpp
public Units rightMarginUnit([Units value])
```

### <a name="parameters---rightmarginunit"></a><span data-ttu-id="32aa5-825">パラメーター - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-825">Parameters - rightMarginUnit</span></span>

<span data-ttu-id="32aa5-826">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-826">value</span></span>  

### <a name="return-value---rightmarginunit"></a><span data-ttu-id="32aa5-827">戻り値 - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-827">Return Value - rightMarginUnit</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="32aa5-828">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-828">Method rightMarginValue</span></span>

```xpp
public Real rightMarginValue([Real value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="32aa5-829">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-829">Parameters - rightMarginValue</span></span>

<span data-ttu-id="32aa5-830">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-830">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="32aa5-831">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-831">Return Value - rightMarginValue</span></span>

## <a name="method-rotatesign"></a><span data-ttu-id="32aa5-832">メソッド rotateSign</span><span class="sxs-lookup"><span data-stu-id="32aa5-832">Method rotateSign</span></span>

```xpp
public int rotateSign([int value])
```

### <a name="parameters---rotatesign"></a><span data-ttu-id="32aa5-833">パラメーター - rotateSign</span><span class="sxs-lookup"><span data-stu-id="32aa5-833">Parameters - rotateSign</span></span>

<span data-ttu-id="32aa5-834">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-834">value</span></span>  

### <a name="return-value---rotatesign"></a><span data-ttu-id="32aa5-835">戻り値 - rotateSign</span><span class="sxs-lookup"><span data-stu-id="32aa5-835">Return Value - rotateSign</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="32aa5-836">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="32aa5-836">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="32aa5-837">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="32aa5-837">Parameters - securityKey</span></span>

<span data-ttu-id="32aa5-838">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-838">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="32aa5-839">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="32aa5-839">Return Value - securityKey</span></span>

## <a name="method-setheightgettext"></a><span data-ttu-id="32aa5-840">メソッド setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="32aa5-840">Method setHeightGetText</span></span>

```xpp
public str setHeightGetText(int lines, str string)
```

### <a name="parameters---setheightgettext"></a><span data-ttu-id="32aa5-841">パラメーター - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="32aa5-841">Parameters - setHeightGetText</span></span>

<span data-ttu-id="32aa5-842">明細行</span><span class="sxs-lookup"><span data-stu-id="32aa5-842">lines</span></span>  

<!-- -->

<span data-ttu-id="32aa5-843">文字列</span><span class="sxs-lookup"><span data-stu-id="32aa5-843">string</span></span>  

### <a name="return-value---setheightgettext"></a><span data-ttu-id="32aa5-844">戻り値 - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="32aa5-844">Return Value - setHeightGetText</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="32aa5-845">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="32aa5-845">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="32aa5-846">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="32aa5-846">Parameters - showLabel</span></span>

<span data-ttu-id="32aa5-847">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-847">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="32aa5-848">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="32aa5-848">Return Value - showLabel</span></span>

## <a name="method-showzero"></a><span data-ttu-id="32aa5-849">メソッド showZero</span><span class="sxs-lookup"><span data-stu-id="32aa5-849">Method showZero</span></span>

```xpp
public int showZero([int value])
```

### <a name="parameters---showzero"></a><span data-ttu-id="32aa5-850">パラメーター - showZero</span><span class="sxs-lookup"><span data-stu-id="32aa5-850">Parameters - showZero</span></span>

<span data-ttu-id="32aa5-851">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-851">value</span></span>  

### <a name="return-value---showzero"></a><span data-ttu-id="32aa5-852">戻り値 - showZero</span><span class="sxs-lookup"><span data-stu-id="32aa5-852">Return Value - showZero</span></span>

## <a name="method-signdisplay"></a><span data-ttu-id="32aa5-853">メソッド signDisplay</span><span class="sxs-lookup"><span data-stu-id="32aa5-853">Method signDisplay</span></span>

```xpp
public int signDisplay([int value])
```

### <a name="parameters---signdisplay"></a><span data-ttu-id="32aa5-854">パラメーター - signDisplay</span><span class="sxs-lookup"><span data-stu-id="32aa5-854">Parameters - signDisplay</span></span>

<span data-ttu-id="32aa5-855">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-855">value</span></span>  

### <a name="return-value---signdisplay"></a><span data-ttu-id="32aa5-856">戻り値 - signDisplay</span><span class="sxs-lookup"><span data-stu-id="32aa5-856">Return Value - signDisplay</span></span>

## <a name="method-sumtype"></a><span data-ttu-id="32aa5-857">メソッド sumType</span><span class="sxs-lookup"><span data-stu-id="32aa5-857">Method sumType</span></span>

```xpp
public int sumType([int value])
```

### <a name="parameters---sumtype"></a><span data-ttu-id="32aa5-858">パラメーター - sumType</span><span class="sxs-lookup"><span data-stu-id="32aa5-858">Parameters - sumType</span></span>

<span data-ttu-id="32aa5-859">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-859">value</span></span>  

### <a name="return-value---sumtype"></a><span data-ttu-id="32aa5-860">戻り値 - sumType</span><span class="sxs-lookup"><span data-stu-id="32aa5-860">Return Value - sumType</span></span>

## <a name="method-table"></a><span data-ttu-id="32aa5-861">メソッド table</span><span class="sxs-lookup"><span data-stu-id="32aa5-861">Method table</span></span>

<span data-ttu-id="32aa5-862">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-862">Gets or sets the table ID associated with the object.</span></span>

```xpp
public TableId table([TableId value])
```

### <a name="parameters---table"></a><span data-ttu-id="32aa5-863">パラメーター - table</span><span class="sxs-lookup"><span data-stu-id="32aa5-863">Parameters - table</span></span>

<span data-ttu-id="32aa5-864">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-864">value</span></span>  

### <a name="return-value---table"></a><span data-ttu-id="32aa5-865">戻り値 - toBlob</span><span class="sxs-lookup"><span data-stu-id="32aa5-865">Return Value - table</span></span>

<span data-ttu-id="32aa5-866">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="32aa5-866">The current value of the table ID associated with the object.</span></span>

## <a name="method-thickness"></a><span data-ttu-id="32aa5-867">メソッド thickness</span><span class="sxs-lookup"><span data-stu-id="32aa5-867">Method thickness</span></span>

```xpp
public LineThickness thickness([LineThickness value])
```

### <a name="parameters---thickness"></a><span data-ttu-id="32aa5-868">パラメーター - thickness</span><span class="sxs-lookup"><span data-stu-id="32aa5-868">Parameters - thickness</span></span>

<span data-ttu-id="32aa5-869">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-869">value</span></span>  

### <a name="return-value---thickness"></a><span data-ttu-id="32aa5-870">戻り値 - thickness</span><span class="sxs-lookup"><span data-stu-id="32aa5-870">Return Value - thickness</span></span>

## <a name="method-thousandseparator"></a><span data-ttu-id="32aa5-871">メソッド thousandSeparator</span><span class="sxs-lookup"><span data-stu-id="32aa5-871">Method thousandSeparator</span></span>

```xpp
public int thousandSeparator([int value])
```

### <a name="parameters---thousandseparator"></a><span data-ttu-id="32aa5-872">パラメーター - thousandSeparator</span><span class="sxs-lookup"><span data-stu-id="32aa5-872">Parameters - thousandSeparator</span></span>

<span data-ttu-id="32aa5-873">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-873">value</span></span>  

### <a name="return-value---thousandseparator"></a><span data-ttu-id="32aa5-874">戻り値 - thousandSeparator</span><span class="sxs-lookup"><span data-stu-id="32aa5-874">Return Value - thousandSeparator</span></span>

## <a name="method-top100mm"></a><span data-ttu-id="32aa5-875">メソッド top100mm</span><span class="sxs-lookup"><span data-stu-id="32aa5-875">Method top100mm</span></span>

```xpp
public int top100mm([int topExclBorder])
```

### <a name="parameters---top100mm"></a><span data-ttu-id="32aa5-876">パラメーター - top100mm</span><span class="sxs-lookup"><span data-stu-id="32aa5-876">Parameters - top100mm</span></span>

<span data-ttu-id="32aa5-877">topExclBorder</span><span class="sxs-lookup"><span data-stu-id="32aa5-877">topExclBorder</span></span>  

### <a name="return-value---top100mm"></a><span data-ttu-id="32aa5-878">戻り値 - top100mm</span><span class="sxs-lookup"><span data-stu-id="32aa5-878">Return Value - top100mm</span></span>

## <a name="method-top100mminclborder"></a><span data-ttu-id="32aa5-879">メソッド top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="32aa5-879">Method top100mmInclBorder</span></span>

```xpp
public int top100mmInclBorder([int topInclBorder])
```

### <a name="parameters---top100mminclborder"></a><span data-ttu-id="32aa5-880">パラメーター - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="32aa5-880">Parameters - top100mmInclBorder</span></span>

<span data-ttu-id="32aa5-881">topInclBorder</span><span class="sxs-lookup"><span data-stu-id="32aa5-881">topInclBorder</span></span>  

### <a name="return-value---top100mminclborder"></a><span data-ttu-id="32aa5-882">戻り値 - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="32aa5-882">Return Value - top100mmInclBorder</span></span>

## <a name="method-topmarginandframe"></a><span data-ttu-id="32aa5-883">メソッド topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="32aa5-883">Method topMarginAndFrame</span></span>

```xpp
public int topMarginAndFrame()
```

### <a name="return-value---topmarginandframe"></a><span data-ttu-id="32aa5-884">戻り値 - topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="32aa5-884">Return Value - topMarginAndFrame</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="32aa5-885">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-885">Method topMarginMode</span></span>

```xpp
public int topMarginMode([int value])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="32aa5-886">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-886">Parameters - topMarginMode</span></span>

<span data-ttu-id="32aa5-887">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-887">value</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="32aa5-888">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-888">Return Value - topMarginMode</span></span>

## <a name="method-topmarginstr"></a><span data-ttu-id="32aa5-889">メソッド topMarginStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-889">Method topMarginStr</span></span>

```xpp
public str topMarginStr([str value])
```

### <a name="parameters---topmarginstr"></a><span data-ttu-id="32aa5-890">パラメーター - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-890">Parameters - topMarginStr</span></span>

<span data-ttu-id="32aa5-891">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-891">value</span></span>  

### <a name="return-value---topmarginstr"></a><span data-ttu-id="32aa5-892">戻り値 - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-892">Return Value - topMarginStr</span></span>

## <a name="method-topmarginunit"></a><span data-ttu-id="32aa5-893">メソッド topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-893">Method topMarginUnit</span></span>

```xpp
public Units topMarginUnit([Units value])
```

### <a name="parameters---topmarginunit"></a><span data-ttu-id="32aa5-894">パラメーター - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-894">Parameters - topMarginUnit</span></span>

<span data-ttu-id="32aa5-895">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-895">value</span></span>  

### <a name="return-value---topmarginunit"></a><span data-ttu-id="32aa5-896">戻り値 - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-896">Return Value - topMarginUnit</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="32aa5-897">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-897">Method topMarginValue</span></span>

```xpp
public Real topMarginValue([Real value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="32aa5-898">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-898">Parameters - topMarginValue</span></span>

<span data-ttu-id="32aa5-899">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-899">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="32aa5-900">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-900">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="32aa5-901">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-901">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="32aa5-902">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-902">Parameters - topMode</span></span>

<span data-ttu-id="32aa5-903">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-903">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="32aa5-904">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-904">Return Value - topMode</span></span>

## <a name="method-topstr"></a><span data-ttu-id="32aa5-905">メソッド topStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-905">Method topStr</span></span>

```xpp
public str topStr([str value])
```

### <a name="parameters---topstr"></a><span data-ttu-id="32aa5-906">パラメーター - topStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-906">Parameters - topStr</span></span>

<span data-ttu-id="32aa5-907">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-907">value</span></span>  

### <a name="return-value---topstr"></a><span data-ttu-id="32aa5-908">戻り値 - topStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-908">Return Value - topStr</span></span>

## <a name="method-topunit"></a><span data-ttu-id="32aa5-909">メソッド topUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-909">Method topUnit</span></span>

```xpp
public Units topUnit([Units value])
```

### <a name="parameters---topunit"></a><span data-ttu-id="32aa5-910">パラメーター - topUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-910">Parameters - topUnit</span></span>

<span data-ttu-id="32aa5-911">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-911">value</span></span>  

### <a name="return-value---topunit"></a><span data-ttu-id="32aa5-912">戻り値 - topUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-912">Return Value - topUnit</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="32aa5-913">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-913">Method topValue</span></span>

```xpp
public Real topValue([Real value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="32aa5-914">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-914">Parameters - topValue</span></span>

<span data-ttu-id="32aa5-915">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-915">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="32aa5-916">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-916">Return Value - topValue</span></span>

## <a name="method-underline"></a><span data-ttu-id="32aa5-917">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="32aa5-917">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="32aa5-918">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="32aa5-918">Parameters - underline</span></span>

<span data-ttu-id="32aa5-919">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-919">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="32aa5-920">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="32aa5-920">Return Value - underline</span></span>

## <a name="method-visible"></a><span data-ttu-id="32aa5-921">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="32aa5-921">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="32aa5-922">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="32aa5-922">Parameters - visible</span></span>

<span data-ttu-id="32aa5-923">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-923">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="32aa5-924">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="32aa5-924">Return Value - visible</span></span>

## <a name="method-webmenuitemname"></a><span data-ttu-id="32aa5-925">メソッド webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="32aa5-925">Method webMenuItemName</span></span>

```xpp
public str webMenuItemName([str value])
```

### <a name="parameters---webmenuitemname"></a><span data-ttu-id="32aa5-926">パラメーター - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="32aa5-926">Parameters - webMenuItemName</span></span>

<span data-ttu-id="32aa5-927">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-927">value</span></span>  

### <a name="return-value---webmenuitemname"></a><span data-ttu-id="32aa5-928">戻り値 - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="32aa5-928">Return Value - webMenuItemName</span></span>

## <a name="method-webmenuitemtype"></a><span data-ttu-id="32aa5-929">メソッド webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="32aa5-929">Method webMenuItemType</span></span>

```xpp
public WebMenuItemType webMenuItemType([WebMenuItemType value])
```

### <a name="parameters---webmenuitemtype"></a><span data-ttu-id="32aa5-930">パラメーター - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="32aa5-930">Parameters - webMenuItemType</span></span>

<span data-ttu-id="32aa5-931">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-931">value</span></span>  

### <a name="return-value---webmenuitemtype"></a><span data-ttu-id="32aa5-932">戻り値 - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="32aa5-932">Return Value - webMenuItemType</span></span>

## <a name="method-webtarget"></a><span data-ttu-id="32aa5-933">メソッド webTarget</span><span class="sxs-lookup"><span data-stu-id="32aa5-933">Method webTarget</span></span>

```xpp
public str webTarget([str value])
```

### <a name="parameters---webtarget"></a><span data-ttu-id="32aa5-934">パラメーター - webTarget</span><span class="sxs-lookup"><span data-stu-id="32aa5-934">Parameters - webTarget</span></span>

<span data-ttu-id="32aa5-935">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-935">value</span></span>  

### <a name="return-value---webtarget"></a><span data-ttu-id="32aa5-936">戻り値 - webTarget</span><span class="sxs-lookup"><span data-stu-id="32aa5-936">Return Value - webTarget</span></span>

## <a name="method-width100mm"></a><span data-ttu-id="32aa5-937">メソッド width100mm</span><span class="sxs-lookup"><span data-stu-id="32aa5-937">Method width100mm</span></span>

```xpp
public int width100mm([int widthExclBorder])
```

### <a name="parameters---width100mm"></a><span data-ttu-id="32aa5-938">パラメーター - width100mm</span><span class="sxs-lookup"><span data-stu-id="32aa5-938">Parameters - width100mm</span></span>

<span data-ttu-id="32aa5-939">widthExclBorder</span><span class="sxs-lookup"><span data-stu-id="32aa5-939">widthExclBorder</span></span>  

### <a name="return-value---width100mm"></a><span data-ttu-id="32aa5-940">戻り値 - width100mm</span><span class="sxs-lookup"><span data-stu-id="32aa5-940">Return Value - width100mm</span></span>

## <a name="method-width100mminclborder"></a><span data-ttu-id="32aa5-941">メソッド width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="32aa5-941">Method width100mmInclBorder</span></span>

```xpp
public int width100mmInclBorder([int widthInclBorder])
```

### <a name="parameters---width100mminclborder"></a><span data-ttu-id="32aa5-942">パラメーター - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="32aa5-942">Parameters - width100mmInclBorder</span></span>

<span data-ttu-id="32aa5-943">widthInclBorder</span><span class="sxs-lookup"><span data-stu-id="32aa5-943">widthInclBorder</span></span>  

### <a name="return-value---width100mminclborder"></a><span data-ttu-id="32aa5-944">戻り値 - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="32aa5-944">Return Value - width100mmInclBorder</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="32aa5-945">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-945">Method widthMode</span></span>

<span data-ttu-id="32aa5-946">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-946">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="32aa5-947">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-947">Parameters - widthMode</span></span>

<span data-ttu-id="32aa5-948">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-948">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="32aa5-949">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-949">Return Value - widthMode</span></span>

<span data-ttu-id="32aa5-950">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="32aa5-950">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="32aa5-951">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="32aa5-951">Remarks - widthMode</span></span>

<span data-ttu-id="32aa5-952">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="32aa5-952">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="32aa5-953">モード。</span><span class="sxs-lookup"><span data-stu-id="32aa5-953">Mode.</span></span>         | <span data-ttu-id="32aa5-954">幅計算。</span><span class="sxs-lookup"><span data-stu-id="32aa5-954">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="32aa5-955">正確。</span><span class="sxs-lookup"><span data-stu-id="32aa5-955">Exact.</span></span>        | <span data-ttu-id="32aa5-956">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="32aa5-956">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="32aa5-957">自動。</span><span class="sxs-lookup"><span data-stu-id="32aa5-957">Auto.</span></span>         | <span data-ttu-id="32aa5-958">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="32aa5-958">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="32aa5-959">列の幅。</span><span class="sxs-lookup"><span data-stu-id="32aa5-959">Column width.</span></span> | <span data-ttu-id="32aa5-960">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="32aa5-960">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="32aa5-961">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="32aa5-961">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthofstring100mm"></a><span data-ttu-id="32aa5-962">メソッド widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="32aa5-962">Method widthOfString100mm</span></span>

```xpp
public int widthOfString100mm(str string)
```

### <a name="parameters---widthofstring100mm"></a><span data-ttu-id="32aa5-963">パラメーター - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="32aa5-963">Parameters - widthOfString100mm</span></span>

<span data-ttu-id="32aa5-964">文字列</span><span class="sxs-lookup"><span data-stu-id="32aa5-964">string</span></span>  

### <a name="return-value---widthofstring100mm"></a><span data-ttu-id="32aa5-965">戻り値 - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="32aa5-965">Return Value - widthOfString100mm</span></span>

## <a name="method-widthstr"></a><span data-ttu-id="32aa5-966">メソッド widthStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-966">Method widthStr</span></span>

```xpp
public str widthStr([str value])
```

### <a name="parameters---widthstr"></a><span data-ttu-id="32aa5-967">パラメーター - widthStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-967">Parameters - widthStr</span></span>

<span data-ttu-id="32aa5-968">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-968">value</span></span>  

### <a name="return-value---widthstr"></a><span data-ttu-id="32aa5-969">戻り値 - widthStr</span><span class="sxs-lookup"><span data-stu-id="32aa5-969">Return Value - widthStr</span></span>

## <a name="method-widthunit"></a><span data-ttu-id="32aa5-970">メソッド widthUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-970">Method widthUnit</span></span>

```xpp
public Units widthUnit([Units value])
```

### <a name="parameters---widthunit"></a><span data-ttu-id="32aa5-971">パラメーター - widthUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-971">Parameters - widthUnit</span></span>

<span data-ttu-id="32aa5-972">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-972">value</span></span>  

### <a name="return-value---widthunit"></a><span data-ttu-id="32aa5-973">戻り値 - widthUnit</span><span class="sxs-lookup"><span data-stu-id="32aa5-973">Return Value - widthUnit</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="32aa5-974">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-974">Method widthValue</span></span>

<span data-ttu-id="32aa5-975">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-975">Gets or sets the width of the control.</span></span>

```xpp
public Real widthValue([Real value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="32aa5-976">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-976">Parameters - widthValue</span></span>

<span data-ttu-id="32aa5-977">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-977">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="32aa5-978">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-978">Return Value - widthValue</span></span>

<span data-ttu-id="32aa5-979">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="32aa5-979">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="32aa5-980">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="32aa5-980">Remarks - widthValue</span></span>

<span data-ttu-id="32aa5-981">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-981">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-top"></a><span data-ttu-id="32aa5-982">メソッド top</span><span class="sxs-lookup"><span data-stu-id="32aa5-982">Method top</span></span>

```xpp
public void top(Real value, Units unit)
```

### <a name="parameters---top"></a><span data-ttu-id="32aa5-983">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="32aa5-983">Parameters - top</span></span>

<span data-ttu-id="32aa5-984">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-984">value</span></span>  

<!-- -->

<span data-ttu-id="32aa5-985">単位</span><span class="sxs-lookup"><span data-stu-id="32aa5-985">unit</span></span>  

## <a name="method-topmargin"></a><span data-ttu-id="32aa5-986">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="32aa5-986">Method topMargin</span></span>

```xpp
public void topMargin(Real value, Units unit)
```

### <a name="parameters---topmargin"></a><span data-ttu-id="32aa5-987">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="32aa5-987">Parameters - topMargin</span></span>

<span data-ttu-id="32aa5-988">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-988">value</span></span>  

<!-- -->

<span data-ttu-id="32aa5-989">単位</span><span class="sxs-lookup"><span data-stu-id="32aa5-989">unit</span></span>  

## <a name="method-bottommargin"></a><span data-ttu-id="32aa5-990">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="32aa5-990">Method bottomMargin</span></span>

```xpp
public void bottomMargin(Real value, Units unit)
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="32aa5-991">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="32aa5-991">Parameters - bottomMargin</span></span>

<span data-ttu-id="32aa5-992">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-992">value</span></span>  

<!-- -->

<span data-ttu-id="32aa5-993">単位</span><span class="sxs-lookup"><span data-stu-id="32aa5-993">unit</span></span>  

## <a name="method-rightmargin"></a><span data-ttu-id="32aa5-994">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="32aa5-994">Method rightMargin</span></span>

```xpp
public void rightMargin(Real value, Units unit)
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="32aa5-995">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="32aa5-995">Parameters - rightMargin</span></span>

<span data-ttu-id="32aa5-996">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-996">value</span></span>  

<!-- -->

<span data-ttu-id="32aa5-997">単位</span><span class="sxs-lookup"><span data-stu-id="32aa5-997">unit</span></span>  

## <a name="method-leftmargin"></a><span data-ttu-id="32aa5-998">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="32aa5-998">Method leftMargin</span></span>

```xpp
public void leftMargin(Real value, Units unit)
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="32aa5-999">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="32aa5-999">Parameters - leftMargin</span></span>

<span data-ttu-id="32aa5-1000">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-1000">value</span></span>  

<!-- -->

<span data-ttu-id="32aa5-1001">単位</span><span class="sxs-lookup"><span data-stu-id="32aa5-1001">unit</span></span>  

## <a name="method-show"></a><span data-ttu-id="32aa5-1002">メソッド show</span><span class="sxs-lookup"><span data-stu-id="32aa5-1002">Method show</span></span>

```xpp
public void show()
```

## <a name="method-left"></a><span data-ttu-id="32aa5-1003">メソッド left</span><span class="sxs-lookup"><span data-stu-id="32aa5-1003">Method left</span></span>

```xpp
public void left(Real value, Units unit)
```

### <a name="parameters---left"></a><span data-ttu-id="32aa5-1004">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="32aa5-1004">Parameters - left</span></span>

<span data-ttu-id="32aa5-1005">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-1005">value</span></span>  

<!-- -->

<span data-ttu-id="32aa5-1006">単位</span><span class="sxs-lookup"><span data-stu-id="32aa5-1006">unit</span></span>  

## <a name="method-width"></a><span data-ttu-id="32aa5-1007">メソッド width</span><span class="sxs-lookup"><span data-stu-id="32aa5-1007">Method width</span></span>

<span data-ttu-id="32aa5-1008">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-1008">Gets or sets the width of the control.</span></span>

```xpp
public void width(Real value, Units unit)
```

### <a name="parameters---width"></a><span data-ttu-id="32aa5-1009">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="32aa5-1009">Parameters - width</span></span>

<span data-ttu-id="32aa5-1010">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-1010">value</span></span>  

<!-- -->

<span data-ttu-id="32aa5-1011">単位</span><span class="sxs-lookup"><span data-stu-id="32aa5-1011">unit</span></span>  

### <a name="remarks---width"></a><span data-ttu-id="32aa5-1012">備考 - width</span><span class="sxs-lookup"><span data-stu-id="32aa5-1012">Remarks - width</span></span>

<span data-ttu-id="32aa5-1013">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="32aa5-1013">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="32aa5-1014">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="32aa5-1014">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="32aa5-1015">モード。</span><span class="sxs-lookup"><span data-stu-id="32aa5-1015">Mode.</span></span>           | <span data-ttu-id="32aa5-1016">幅計算。</span><span class="sxs-lookup"><span data-stu-id="32aa5-1016">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="32aa5-1017">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="32aa5-1017">-1 Exact.</span></span>       | <span data-ttu-id="32aa5-1018">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="32aa5-1018">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="32aa5-1019">0 自動。</span><span class="sxs-lookup"><span data-stu-id="32aa5-1019">0 Auto.</span></span>         | <span data-ttu-id="32aa5-1020">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="32aa5-1020">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="32aa5-1021">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="32aa5-1021">1 Column width.</span></span> | <span data-ttu-id="32aa5-1022">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="32aa5-1022">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="32aa5-1023">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="32aa5-1023">The width and width calculation mode can be set separately.</span></span>

## <a name="method-extrasumwidth"></a><span data-ttu-id="32aa5-1024">メソッド extraSumWidth</span><span class="sxs-lookup"><span data-stu-id="32aa5-1024">Method extraSumWidth</span></span>

```xpp
public void extraSumWidth(Real value, Units unit)
```

### <a name="parameters---extrasumwidth"></a><span data-ttu-id="32aa5-1025">パラメーター - extraSumWidth</span><span class="sxs-lookup"><span data-stu-id="32aa5-1025">Parameters - extraSumWidth</span></span>

<span data-ttu-id="32aa5-1026">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-1026">value</span></span>  

<!-- -->

<span data-ttu-id="32aa5-1027">単位</span><span class="sxs-lookup"><span data-stu-id="32aa5-1027">unit</span></span>  

## <a name="method-labelwidth"></a><span data-ttu-id="32aa5-1028">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="32aa5-1028">Method labelWidth</span></span>

```xpp
public void labelWidth(Real value, Units unit)
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="32aa5-1029">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="32aa5-1029">Parameters - labelWidth</span></span>

<span data-ttu-id="32aa5-1030">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-1030">value</span></span>  

<!-- -->

<span data-ttu-id="32aa5-1031">単位</span><span class="sxs-lookup"><span data-stu-id="32aa5-1031">unit</span></span>  

## <a name="method-hide"></a><span data-ttu-id="32aa5-1032">メソッド hide</span><span class="sxs-lookup"><span data-stu-id="32aa5-1032">Method hide</span></span>

```xpp
public void hide()
```

## <a name="method-height"></a><span data-ttu-id="32aa5-1033">メソッド height</span><span class="sxs-lookup"><span data-stu-id="32aa5-1033">Method height</span></span>

<span data-ttu-id="32aa5-1034">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="32aa5-1034">Gets or sets the height of the control.</span></span>

```xpp
public void height(Real value, Units unit)
```

### <a name="parameters---height"></a><span data-ttu-id="32aa5-1035">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="32aa5-1035">Parameters - height</span></span>

<span data-ttu-id="32aa5-1036">値</span><span class="sxs-lookup"><span data-stu-id="32aa5-1036">value</span></span>  

<!-- -->

<span data-ttu-id="32aa5-1037">単位</span><span class="sxs-lookup"><span data-stu-id="32aa5-1037">unit</span></span>  

### <a name="remarks---height"></a><span data-ttu-id="32aa5-1038">備考 - height</span><span class="sxs-lookup"><span data-stu-id="32aa5-1038">Remarks - height</span></span>

<span data-ttu-id="32aa5-1039">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="32aa5-1039">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="32aa5-1040">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="32aa5-1040">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="32aa5-1041">モード。</span><span class="sxs-lookup"><span data-stu-id="32aa5-1041">Mode.</span></span>            | <span data-ttu-id="32aa5-1042">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="32aa5-1042">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="32aa5-1043">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="32aa5-1043">-1 Exact.</span></span>        | <span data-ttu-id="32aa5-1044">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="32aa5-1044">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="32aa5-1045">0 自動。</span><span class="sxs-lookup"><span data-stu-id="32aa5-1045">0 Auto.</span></span>          | <span data-ttu-id="32aa5-1046">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="32aa5-1046">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="32aa5-1047">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="32aa5-1047">1 Column height.</span></span> | <span data-ttu-id="32aa5-1048">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="32aa5-1048">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="32aa5-1049">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="32aa5-1049">The height and height calculation mode can be set separately.</span></span>

