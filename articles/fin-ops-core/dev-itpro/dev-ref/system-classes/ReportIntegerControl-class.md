---
title: ReportIntegerControl クラス
description: このトピックでは、ReportIntegerControl クラスについて説明します。
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
ms.openlocfilehash: 4486c9b6b7825929156c41636ac4e0d3a3ea9b49
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502839"
---
# <a name="class-reportintegercontrol"></a><span data-ttu-id="fb266-103">クラス ReportIntegerControl</span><span class="sxs-lookup"><span data-stu-id="fb266-103">Class ReportIntegerControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ReportIntegerControl extends ReportControl
```

<span data-ttu-id="fb266-104">ReportIntegerControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="fb266-104">The ReportIntegerControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb266-105">備考</span><span class="sxs-lookup"><span data-stu-id="fb266-105">Remarks</span></span>

<span data-ttu-id="fb266-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fb266-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="fb266-107">例</span><span class="sxs-lookup"><span data-stu-id="fb266-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="fb266-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="fb266-108">Methods</span></span>

| <span data-ttu-id="fb266-109">方法</span><span class="sxs-lookup"><span data-stu-id="fb266-109">Method</span></span>                                                                   | <span data-ttu-id="fb266-110">説明</span><span class="sxs-lookup"><span data-stu-id="fb266-110">Description</span></span>                                                                                                                               |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb266-111">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-111">public int alignment(\[int value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="fb266-112">public int allowNegative(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-112">public int allowNegative(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="fb266-113">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-113">public int arrayIndex(\[int value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="fb266-114">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-114">public boolean autoDeclaration(\[boolean value\])</span></span>                        | <span data-ttu-id="fb266-115">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-115">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                        |
| <span data-ttu-id="fb266-116">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-116">public int backgroundColor(\[int value\])</span></span>                                | <span data-ttu-id="fb266-117">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-117">Gets or sets the background color of the control.</span></span>                                                                                         |
| <span data-ttu-id="fb266-118">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-118">public int backStyle(\[int value\])</span></span>                                      | <span data-ttu-id="fb266-119">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-119">Determines whether the control background can be transparent.</span></span>                                                                            |
| <span data-ttu-id="fb266-120">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-120">public int bold(\[int value\])</span></span>                                           | <span data-ttu-id="fb266-121">コントロール内のテキストを出力するのに使用されたフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-121">Gets or sets the weight of font that was used to output text in the control.</span></span>                                                              |
| <span data-ttu-id="fb266-122">public int bottomMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="fb266-122">public int bottomMarginAndFrame()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="fb266-123">public int bottomMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-123">public int bottomMarginMode(\[int value\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="fb266-124">public str bottomMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-124">public str bottomMarginStr(\[str value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="fb266-125">public Units bottomMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-125">public Units bottomMarginUnit(\[Units value\])</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="fb266-126">public Real bottomMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-126">public Real bottomMarginValue(\[Real value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="fb266-127">public int changeLabelCase(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-127">public int changeLabelCase(\[int value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="fb266-128">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-128">public int characterSet(\[int value\])</span></span>                                   | <span data-ttu-id="fb266-129">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-129">Gets or sets the character set of the font.</span></span>                                                                                               |
| <span data-ttu-id="fb266-130">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-130">public int colorScheme(\[int value\])</span></span>                                    | <span data-ttu-id="fb266-131">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-131">Gets or sets the color scheme of the control.</span></span>                                                                                             |
| <span data-ttu-id="fb266-132">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-132">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="fb266-133">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-133">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                       |
| <span data-ttu-id="fb266-134">public ReportFieldType controlType()</span><span class="sxs-lookup"><span data-stu-id="fb266-134">public ReportFieldType controlType()</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="fb266-135">public str cssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-135">public str cssClass(\[str value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="fb266-136">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-136">public FieldId dataField(\[FieldId value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="fb266-137">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-137">public str dataMethod(\[str value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="fb266-138">public int delete()</span><span class="sxs-lookup"><span data-stu-id="fb266-138">public int delete()</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="fb266-139">public int displaceNegative(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="fb266-139">public int displaceNegative(\[int value\], \[AutoMode mode\])</span></span>            |                                                                                                                                           |
| <span data-ttu-id="fb266-140">public AutoMode displaceNegativeMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="fb266-140">public AutoMode displaceNegativeMode(\[AutoMode mode\])</span></span>                  |                                                                                                                                           |
| <span data-ttu-id="fb266-141">public int displaceNegativeValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-141">public int displaceNegativeValue(\[int value\])</span></span>                          |                                                                                                                                           |
| <span data-ttu-id="fb266-142">public str effectiveFont()</span><span class="sxs-lookup"><span data-stu-id="fb266-142">public str effectiveFont()</span></span>                                               |                                                                                                                                           |
| <span data-ttu-id="fb266-143">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-143">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>         |                                                                                                                                           |
| <span data-ttu-id="fb266-144">public int extraSumWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-144">public int extraSumWidthMode(\[int value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="fb266-145">public str extraSumWidthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-145">public str extraSumWidthStr(\[str value\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="fb266-146">public Units extraSumWidthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-146">public Units extraSumWidthUnit(\[Units value\])</span></span>                          |                                                                                                                                           |
| <span data-ttu-id="fb266-147">public Real extraSumWidthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-147">public Real extraSumWidthValue(\[Real value\])</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="fb266-148">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-148">public str font(\[str value\])</span></span>                                           | <span data-ttu-id="fb266-149">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-149">Gets or sets the name of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="fb266-150">public str fontInfoPrinter()</span><span class="sxs-lookup"><span data-stu-id="fb266-150">public str fontInfoPrinter()</span></span>                                             |                                                                                                                                           |
| <span data-ttu-id="fb266-151">public int fontInfoPrinterAscent()</span><span class="sxs-lookup"><span data-stu-id="fb266-151">public int fontInfoPrinterAscent()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="fb266-152">public int fontInfoPrinterDescent()</span><span class="sxs-lookup"><span data-stu-id="fb266-152">public int fontInfoPrinterDescent()</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="fb266-153">public int fontInfoPrinterExtLead()</span><span class="sxs-lookup"><span data-stu-id="fb266-153">public int fontInfoPrinterExtLead()</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="fb266-154">public int fontInfoPrinterHeight()</span><span class="sxs-lookup"><span data-stu-id="fb266-154">public int fontInfoPrinterHeight()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="fb266-155">public int fontInfoPrinterIntLead()</span><span class="sxs-lookup"><span data-stu-id="fb266-155">public int fontInfoPrinterIntLead()</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="fb266-156">public str fontInfoScreen()</span><span class="sxs-lookup"><span data-stu-id="fb266-156">public str fontInfoScreen()</span></span>                                              |                                                                                                                                           |
| <span data-ttu-id="fb266-157">public int fontInfoScreenAscent()</span><span class="sxs-lookup"><span data-stu-id="fb266-157">public int fontInfoScreenAscent()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="fb266-158">public int fontInfoScreenDescent()</span><span class="sxs-lookup"><span data-stu-id="fb266-158">public int fontInfoScreenDescent()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="fb266-159">public int fontInfoScreenExtLead()</span><span class="sxs-lookup"><span data-stu-id="fb266-159">public int fontInfoScreenExtLead()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="fb266-160">public int fontInfoScreenHeight()</span><span class="sxs-lookup"><span data-stu-id="fb266-160">public int fontInfoScreenHeight()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="fb266-161">public int fontInfoScreenIntLead()</span><span class="sxs-lookup"><span data-stu-id="fb266-161">public int fontInfoScreenIntLead()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="fb266-162">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-162">public int fontSize(\[int value\])</span></span>                                       | <span data-ttu-id="fb266-163">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-163">Gets or sets the size of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="fb266-164">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-164">public int foregroundColor(\[int value\])</span></span>                                | <span data-ttu-id="fb266-165">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-165">Gets or sets the text color for the control to use.</span></span>                                                                                       |
| <span data-ttu-id="fb266-166">public int height100mm(\[int heightExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="fb266-166">public int height100mm(\[int heightExclBorder\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="fb266-167">public int height100mmInclBorder(\[int heightInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="fb266-167">public int height100mmInclBorder(\[int heightInclBorder\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="fb266-168">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-168">public int heightMode(\[int value\])</span></span>                                     | <span data-ttu-id="fb266-169">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-169">Gets or sets a calculation mode for the height of the control.</span></span>                                                                            |
| <span data-ttu-id="fb266-170">public int heightOfWordWrappedString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="fb266-170">public int heightOfWordWrappedString100mm(str string)</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="fb266-171">public str heightStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-171">public str heightStr(\[str value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="fb266-172">public Units heightUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-172">public Units heightUnit(\[Units value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="fb266-173">public Real heightValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-173">public Real heightValue(\[Real value\])</span></span>                                  | <span data-ttu-id="fb266-174">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-174">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="fb266-175">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-175">public boolean italic(\[boolean value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="fb266-176">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-176">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="fb266-177">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-177">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="fb266-178">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-178">public int labelBold(\[int value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="fb266-179">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-179">public int labelCharacterSet(\[int value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="fb266-180">public str labelCssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-180">public str labelCssClass(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="fb266-181">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-181">public str labelFont(\[str value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="fb266-182">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-182">public int labelFontSize(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="fb266-183">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-183">public boolean labelItalic(\[boolean value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="fb266-184">public LineType labelLineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-184">public LineType labelLineBelow(\[LineType value\])</span></span>                       |                                                                                                                                           |
| <span data-ttu-id="fb266-185">public LineThickness labelLineThickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-185">public LineThickness labelLineThickness(\[LineThickness value\])</span></span>         |                                                                                                                                           |
| <span data-ttu-id="fb266-186">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-186">public int labelPosition(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="fb266-187">public int labelTabLeader(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-187">public int labelTabLeader(\[int value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="fb266-188">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-188">public boolean labelUnderline(\[boolean value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="fb266-189">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-189">public int labelWidthMode(\[int value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="fb266-190">public str labelWidthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-190">public str labelWidthStr(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="fb266-191">public Units labelWidthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-191">public Units labelWidthUnit(\[Units value\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="fb266-192">public Real labelWidthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-192">public Real labelWidthValue(\[Real value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="fb266-193">public int left100mm(\[int leftExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="fb266-193">public int left100mm(\[int leftExclBorder\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="fb266-194">public int left100mmInclBorder(\[int leftInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="fb266-194">public int left100mmInclBorder(\[int leftInclBorder\])</span></span>                   |                                                                                                                                           |
| <span data-ttu-id="fb266-195">public int leftMarginAnFrame()</span><span class="sxs-lookup"><span data-stu-id="fb266-195">public int leftMarginAnFrame()</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="fb266-196">public int leftMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-196">public int leftMarginMode(\[int value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="fb266-197">public str leftMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-197">public str leftMarginStr(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="fb266-198">public Units leftMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-198">public Units leftMarginUnit(\[Units value\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="fb266-199">public Real leftMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-199">public Real leftMarginValue(\[Real value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="fb266-200">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-200">public int leftMode(\[int value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="fb266-201">public str leftStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-201">public str leftStr(\[str value\])</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="fb266-202">public Units leftUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-202">public Units leftUnit(\[Units value\])</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="fb266-203">public Real leftValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-203">public Real leftValue(\[Real value\])</span></span>                                    |                                                                                                                                           |
| <span data-ttu-id="fb266-204">public LineType lineAbove(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-204">public LineType lineAbove(\[LineType value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="fb266-205">public LineType lineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-205">public LineType lineBelow(\[LineType value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="fb266-206">public LineType lineLeft(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-206">public LineType lineLeft(\[LineType value\])</span></span>                             | <span data-ttu-id="fb266-207">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-207">Gets or sets the type of line that is used as the left border of a section.</span></span>                                                               |
| <span data-ttu-id="fb266-208">public LineType lineRight(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-208">public LineType lineRight(\[LineType value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="fb266-209">public str menuItemLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-209">public str menuItemLabel(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="fb266-210">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-210">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="fb266-211">public MenuItemType menuItemType(\[MenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-211">public MenuItemType menuItemType(\[MenuItemType value\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="fb266-212">public str modelFieldName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-212">public str modelFieldName(\[str value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="fb266-213">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-213">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="fb266-214">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-214">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="fb266-215">public int numberOfLines(int height100mm)</span><span class="sxs-lookup"><span data-stu-id="fb266-215">public int numberOfLines(int height100mm)</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="fb266-216">public int position(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-216">public int position(\[int value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="fb266-217">public str previewInfo(str string)</span><span class="sxs-lookup"><span data-stu-id="fb266-217">public str previewInfo(str string)</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="fb266-218">public int previewXCompensation100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="fb266-218">public int previewXCompensation100mm(str string)</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="fb266-219">public int right100mm()</span><span class="sxs-lookup"><span data-stu-id="fb266-219">public int right100mm()</span></span>                                                  |                                                                                                                                           |
| <span data-ttu-id="fb266-220">public int right100mmInclBorder()</span><span class="sxs-lookup"><span data-stu-id="fb266-220">public int right100mmInclBorder()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="fb266-221">public int rightMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="fb266-221">public int rightMarginAndFrame()</span></span>                                         |                                                                                                                                           |
| <span data-ttu-id="fb266-222">public int rightMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-222">public int rightMarginMode(\[int value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="fb266-223">public str rightMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-223">public str rightMarginStr(\[str value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="fb266-224">public Units rightMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-224">public Units rightMarginUnit(\[Units value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="fb266-225">public Real rightMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-225">public Real rightMarginValue(\[Real value\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="fb266-226">public int rotateSign(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-226">public int rotateSign(\[int value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="fb266-227">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-227">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                                           |
| <span data-ttu-id="fb266-228">public str setHeightGetText(int lines, str string)</span><span class="sxs-lookup"><span data-stu-id="fb266-228">public str setHeightGetText(int lines, str string)</span></span>                       |                                                                                                                                           |
| <span data-ttu-id="fb266-229">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-229">public boolean showLabel(\[boolean value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="fb266-230">public int showZero(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-230">public int showZero(\[int value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="fb266-231">public int signDisplay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-231">public int signDisplay(\[int value\])</span></span>                                    |                                                                                                                                           |
| <span data-ttu-id="fb266-232">public boolean sumAll(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-232">public boolean sumAll(\[boolean value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="fb266-233">public boolean sumNeg(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-233">public boolean sumNeg(\[boolean value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="fb266-234">public boolean sumPos(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-234">public boolean sumPos(\[boolean value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="fb266-235">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-235">public TableId table(\[TableId value\])</span></span>                                  | <span data-ttu-id="fb266-236">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-236">Gets or sets the table ID associated with the object.</span></span>                                                                                     |
| <span data-ttu-id="fb266-237">public LineThickness thickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-237">public LineThickness thickness(\[LineThickness value\])</span></span>                  |                                                                                                                                           |
| <span data-ttu-id="fb266-238">public int top100mm(\[int topExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="fb266-238">public int top100mm(\[int topExclBorder\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="fb266-239">public int top100mmInclBorder(\[int topInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="fb266-239">public int top100mmInclBorder(\[int topInclBorder\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="fb266-240">public int topMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="fb266-240">public int topMarginAndFrame()</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="fb266-241">public int topMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-241">public int topMarginMode(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="fb266-242">public str topMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-242">public str topMarginStr(\[str value\])</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="fb266-243">public Units topMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-243">public Units topMarginUnit(\[Units value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="fb266-244">public Real topMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-244">public Real topMarginValue(\[Real value\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="fb266-245">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-245">public int topMode(\[int value\])</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="fb266-246">public str topStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-246">public str topStr(\[str value\])</span></span>                                         |                                                                                                                                           |
| <span data-ttu-id="fb266-247">public Units topUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-247">public Units topUnit(\[Units value\])</span></span>                                    |                                                                                                                                           |
| <span data-ttu-id="fb266-248">public Real topValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-248">public Real topValue(\[Real value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="fb266-249">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-249">public boolean underline(\[boolean value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="fb266-250">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-250">public boolean visible(\[boolean value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="fb266-251">public str webMenuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-251">public str webMenuItemName(\[str value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="fb266-252">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-252">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span></span>        |                                                                                                                                           |
| <span data-ttu-id="fb266-253">public str webTarget(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-253">public str webTarget(\[str value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="fb266-254">public int width100mm(\[int widthExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="fb266-254">public int width100mm(\[int widthExclBorder\])</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="fb266-255">public int width100mmInclBorder(\[int widthInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="fb266-255">public int width100mmInclBorder(\[int widthInclBorder\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="fb266-256">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-256">public int widthMode(\[int value\])</span></span>                                      | <span data-ttu-id="fb266-257">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-257">Gets or sets the calculation mode of the width of the control.</span></span>                                                                            |
| <span data-ttu-id="fb266-258">public int widthOfString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="fb266-258">public int widthOfString100mm(str string)</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="fb266-259">public str widthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-259">public str widthStr(\[str value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="fb266-260">public Units widthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-260">public Units widthUnit(\[Units value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="fb266-261">public Real widthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="fb266-261">public Real widthValue(\[Real value\])</span></span>                                   | <span data-ttu-id="fb266-262">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-262">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="fb266-263">public void show()</span><span class="sxs-lookup"><span data-stu-id="fb266-263">public void show()</span></span>                                                       |                                                                                                                                           |
| <span data-ttu-id="fb266-264">public void left(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="fb266-264">public void left(Real value, Units unit)</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="fb266-265">public void width(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="fb266-265">public void width(Real value, Units unit)</span></span>                                | <span data-ttu-id="fb266-266">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-266">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="fb266-267">public void extraSumWidth(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="fb266-267">public void extraSumWidth(Real value, Units unit)</span></span>                        |                                                                                                                                           |
| <span data-ttu-id="fb266-268">public void leftMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="fb266-268">public void leftMargin(Real value, Units unit)</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="fb266-269">public void topMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="fb266-269">public void topMargin(Real value, Units unit)</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="fb266-270">public void hide()</span><span class="sxs-lookup"><span data-stu-id="fb266-270">public void hide()</span></span>                                                       |                                                                                                                                           |
| <span data-ttu-id="fb266-271">public void bottomMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="fb266-271">public void bottomMargin(Real value, Units unit)</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="fb266-272">public void top(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="fb266-272">public void top(Real value, Units unit)</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="fb266-273">public void labelWidth(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="fb266-273">public void labelWidth(Real value, Units unit)</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="fb266-274">public void rightMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="fb266-274">public void rightMargin(Real value, Units unit)</span></span>                          |                                                                                                                                           |
| <span data-ttu-id="fb266-275">public void height(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="fb266-275">public void height(Real value, Units unit)</span></span>                               | <span data-ttu-id="fb266-276">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-276">Gets or sets the height of the control.</span></span>                                                                                                   |

## <a name="method-alignment"></a><span data-ttu-id="fb266-277">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="fb266-277">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="fb266-278">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="fb266-278">Parameters - alignment</span></span>

<span data-ttu-id="fb266-279">値</span><span class="sxs-lookup"><span data-stu-id="fb266-279">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="fb266-280">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="fb266-280">Return Value - alignment</span></span>

## <a name="method-allownegative"></a><span data-ttu-id="fb266-281">メソッド allowNegative</span><span class="sxs-lookup"><span data-stu-id="fb266-281">Method allowNegative</span></span>

```xpp
public int allowNegative([int value])
```

### <a name="parameters---allownegative"></a><span data-ttu-id="fb266-282">パラメーター - allowNegative</span><span class="sxs-lookup"><span data-stu-id="fb266-282">Parameters - allowNegative</span></span>

<span data-ttu-id="fb266-283">値</span><span class="sxs-lookup"><span data-stu-id="fb266-283">value</span></span>  

### <a name="return-value---allownegative"></a><span data-ttu-id="fb266-284">戻り値 - allowNegative</span><span class="sxs-lookup"><span data-stu-id="fb266-284">Return Value - allowNegative</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="fb266-285">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="fb266-285">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="fb266-286">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="fb266-286">Parameters - arrayIndex</span></span>

<span data-ttu-id="fb266-287">値</span><span class="sxs-lookup"><span data-stu-id="fb266-287">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="fb266-288">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="fb266-288">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="fb266-289">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="fb266-289">Method autoDeclaration</span></span>

<span data-ttu-id="fb266-290">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-290">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="fb266-291">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="fb266-291">Parameters - autoDeclaration</span></span>

<span data-ttu-id="fb266-292">値</span><span class="sxs-lookup"><span data-stu-id="fb266-292">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="fb266-293">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="fb266-293">Return Value - autoDeclaration</span></span>

<span data-ttu-id="fb266-294">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fb266-294">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="fb266-295">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="fb266-295">Remarks - autoDeclaration</span></span>

<span data-ttu-id="fb266-296">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="fb266-296">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="fb266-297">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="fb266-297">Method backgroundColor</span></span>

<span data-ttu-id="fb266-298">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-298">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="fb266-299">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="fb266-299">Parameters - backgroundColor</span></span>

<span data-ttu-id="fb266-300">値</span><span class="sxs-lookup"><span data-stu-id="fb266-300">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="fb266-301">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="fb266-301">Return Value - backgroundColor</span></span>

<span data-ttu-id="fb266-302">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="fb266-302">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="fb266-303">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="fb266-303">Remarks - backgroundColor</span></span>

<span data-ttu-id="fb266-304">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fb266-304">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="fb266-305">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fb266-305">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="fb266-306">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="fb266-306">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="fb266-307">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="fb266-307">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="fb266-308">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="fb266-308">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="fb266-309">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="fb266-309">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="fb266-310">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="fb266-310">Method backStyle</span></span>

<span data-ttu-id="fb266-311">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-311">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="fb266-312">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="fb266-312">Parameters - backStyle</span></span>

<span data-ttu-id="fb266-313">値</span><span class="sxs-lookup"><span data-stu-id="fb266-313">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="fb266-314">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="fb266-314">Return Value - backStyle</span></span>

<span data-ttu-id="fb266-315">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="fb266-315">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="fb266-316">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="fb266-316">Method bold</span></span>

<span data-ttu-id="fb266-317">コントロール内のテキストを出力するのに使用されたフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-317">Gets or sets the weight of font that was used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="fb266-318">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="fb266-318">Parameters - bold</span></span>

<span data-ttu-id="fb266-319">値</span><span class="sxs-lookup"><span data-stu-id="fb266-319">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="fb266-320">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="fb266-320">Return Value - bold</span></span>

<span data-ttu-id="fb266-321">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="fb266-321">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="fb266-322">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="fb266-322">Remarks - bold</span></span>

<span data-ttu-id="fb266-323">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="fb266-323">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="fb266-324">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="fb266-324">0 Use the default font weight.</span></span>
-   <span data-ttu-id="fb266-325">1 シン。</span><span class="sxs-lookup"><span data-stu-id="fb266-325">1 Thin.</span></span>
-   <span data-ttu-id="fb266-326">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="fb266-326">2 Extra-light.</span></span>
-   <span data-ttu-id="fb266-327">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="fb266-327">3 Light.</span></span>
-   <span data-ttu-id="fb266-328">4 標準。</span><span class="sxs-lookup"><span data-stu-id="fb266-328">4 Normal.</span></span>
-   <span data-ttu-id="fb266-329">5 中。</span><span class="sxs-lookup"><span data-stu-id="fb266-329">5 Medium.</span></span>
-   <span data-ttu-id="fb266-330">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="fb266-330">6 Semibold.</span></span>
-   <span data-ttu-id="fb266-331">7 太字。</span><span class="sxs-lookup"><span data-stu-id="fb266-331">7 Bold.</span></span>
-   <span data-ttu-id="fb266-332">8 極太。</span><span class="sxs-lookup"><span data-stu-id="fb266-332">8 Extra-bold.</span></span>
-   <span data-ttu-id="fb266-333">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="fb266-333">9 Heavy.</span></span>

## <a name="method-bottommarginandframe"></a><span data-ttu-id="fb266-334">メソッド bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="fb266-334">Method bottomMarginAndFrame</span></span>

```xpp
public int bottomMarginAndFrame()
```

### <a name="return-value---bottommarginandframe"></a><span data-ttu-id="fb266-335">戻り値 - bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="fb266-335">Return Value - bottomMarginAndFrame</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="fb266-336">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="fb266-336">Method bottomMarginMode</span></span>

```xpp
public int bottomMarginMode([int value])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="fb266-337">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="fb266-337">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="fb266-338">値</span><span class="sxs-lookup"><span data-stu-id="fb266-338">value</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="fb266-339">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="fb266-339">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginstr"></a><span data-ttu-id="fb266-340">メソッド bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="fb266-340">Method bottomMarginStr</span></span>

```xpp
public str bottomMarginStr([str value])
```

### <a name="parameters---bottommarginstr"></a><span data-ttu-id="fb266-341">パラメーター - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="fb266-341">Parameters - bottomMarginStr</span></span>

<span data-ttu-id="fb266-342">値</span><span class="sxs-lookup"><span data-stu-id="fb266-342">value</span></span>  

### <a name="return-value---bottommarginstr"></a><span data-ttu-id="fb266-343">戻り値 - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="fb266-343">Return Value - bottomMarginStr</span></span>

## <a name="method-bottommarginunit"></a><span data-ttu-id="fb266-344">メソッド bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-344">Method bottomMarginUnit</span></span>

```xpp
public Units bottomMarginUnit([Units value])
```

### <a name="parameters---bottommarginunit"></a><span data-ttu-id="fb266-345">パラメーター - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-345">Parameters - bottomMarginUnit</span></span>

<span data-ttu-id="fb266-346">値</span><span class="sxs-lookup"><span data-stu-id="fb266-346">value</span></span>  

### <a name="return-value---bottommarginunit"></a><span data-ttu-id="fb266-347">戻り値 - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-347">Return Value - bottomMarginUnit</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="fb266-348">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="fb266-348">Method bottomMarginValue</span></span>

```xpp
public Real bottomMarginValue([Real value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="fb266-349">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="fb266-349">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="fb266-350">値</span><span class="sxs-lookup"><span data-stu-id="fb266-350">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="fb266-351">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="fb266-351">Return Value - bottomMarginValue</span></span>

## <a name="method-changelabelcase"></a><span data-ttu-id="fb266-352">メソッド changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="fb266-352">Method changeLabelCase</span></span>

```xpp
public int changeLabelCase([int value])
```

### <a name="parameters---changelabelcase"></a><span data-ttu-id="fb266-353">パラメーター - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="fb266-353">Parameters - changeLabelCase</span></span>

<span data-ttu-id="fb266-354">値</span><span class="sxs-lookup"><span data-stu-id="fb266-354">value</span></span>  

### <a name="return-value---changelabelcase"></a><span data-ttu-id="fb266-355">戻り値 - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="fb266-355">Return Value - changeLabelCase</span></span>

## <a name="method-characterset"></a><span data-ttu-id="fb266-356">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="fb266-356">Method characterSet</span></span>

<span data-ttu-id="fb266-357">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-357">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="fb266-358">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="fb266-358">Parameters - characterSet</span></span>

<span data-ttu-id="fb266-359">値</span><span class="sxs-lookup"><span data-stu-id="fb266-359">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="fb266-360">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="fb266-360">Return Value - characterSet</span></span>

<span data-ttu-id="fb266-361">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="fb266-361">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="fb266-362">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="fb266-362">Remarks - characterSet</span></span>

<span data-ttu-id="fb266-363">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="fb266-363">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="fb266-364">値です。</span><span class="sxs-lookup"><span data-stu-id="fb266-364">Value.</span></span> | <span data-ttu-id="fb266-365">説明。</span><span class="sxs-lookup"><span data-stu-id="fb266-365">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="fb266-366">0</span><span class="sxs-lookup"><span data-stu-id="fb266-366">0</span></span>      | <span data-ttu-id="fb266-367">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fb266-367">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="fb266-368">1</span><span class="sxs-lookup"><span data-stu-id="fb266-368">1</span></span>      | <span data-ttu-id="fb266-369">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fb266-369">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="fb266-370">2</span><span class="sxs-lookup"><span data-stu-id="fb266-370">2</span></span>      | <span data-ttu-id="fb266-371">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fb266-371">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="fb266-372">77</span><span class="sxs-lookup"><span data-stu-id="fb266-372">77</span></span>     | <span data-ttu-id="fb266-373">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fb266-373">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="fb266-374">128</span><span class="sxs-lookup"><span data-stu-id="fb266-374">128</span></span>    | <span data-ttu-id="fb266-375">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fb266-375">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="fb266-376">129</span><span class="sxs-lookup"><span data-stu-id="fb266-376">129</span></span>    | <span data-ttu-id="fb266-377">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fb266-377">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="fb266-378">134</span><span class="sxs-lookup"><span data-stu-id="fb266-378">134</span></span>    | <span data-ttu-id="fb266-379">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fb266-379">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="fb266-380">136</span><span class="sxs-lookup"><span data-stu-id="fb266-380">136</span></span>    | <span data-ttu-id="fb266-381">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fb266-381">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="fb266-382">161</span><span class="sxs-lookup"><span data-stu-id="fb266-382">161</span></span>    | <span data-ttu-id="fb266-383">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fb266-383">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="fb266-384">162</span><span class="sxs-lookup"><span data-stu-id="fb266-384">162</span></span>    | <span data-ttu-id="fb266-385">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fb266-385">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="fb266-386">163</span><span class="sxs-lookup"><span data-stu-id="fb266-386">163</span></span>    | <span data-ttu-id="fb266-387">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fb266-387">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="fb266-388">186</span><span class="sxs-lookup"><span data-stu-id="fb266-388">186</span></span>    | <span data-ttu-id="fb266-389">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fb266-389">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="fb266-390">204</span><span class="sxs-lookup"><span data-stu-id="fb266-390">204</span></span>    | <span data-ttu-id="fb266-391">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fb266-391">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="fb266-392">238</span><span class="sxs-lookup"><span data-stu-id="fb266-392">238</span></span>    | <span data-ttu-id="fb266-393">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fb266-393">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="fb266-394">255</span><span class="sxs-lookup"><span data-stu-id="fb266-394">255</span></span>    | <span data-ttu-id="fb266-395">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fb266-395">OEM\_CHARSET</span></span>         |

<span data-ttu-id="fb266-396">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="fb266-396">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="fb266-397">値です。</span><span class="sxs-lookup"><span data-stu-id="fb266-397">Value.</span></span> | <span data-ttu-id="fb266-398">説明。</span><span class="sxs-lookup"><span data-stu-id="fb266-398">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="fb266-399">130</span><span class="sxs-lookup"><span data-stu-id="fb266-399">130</span></span>    | <span data-ttu-id="fb266-400">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fb266-400">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="fb266-401">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="fb266-401">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="fb266-402">値です。</span><span class="sxs-lookup"><span data-stu-id="fb266-402">Value.</span></span> | <span data-ttu-id="fb266-403">説明。</span><span class="sxs-lookup"><span data-stu-id="fb266-403">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="fb266-404">177</span><span class="sxs-lookup"><span data-stu-id="fb266-404">177</span></span>    | <span data-ttu-id="fb266-405">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fb266-405">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="fb266-406">178</span><span class="sxs-lookup"><span data-stu-id="fb266-406">178</span></span>    | <span data-ttu-id="fb266-407">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fb266-407">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="fb266-408">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="fb266-408">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="fb266-409">値です。</span><span class="sxs-lookup"><span data-stu-id="fb266-409">Value.</span></span> | <span data-ttu-id="fb266-410">説明。</span><span class="sxs-lookup"><span data-stu-id="fb266-410">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="fb266-411">222</span><span class="sxs-lookup"><span data-stu-id="fb266-411">222</span></span>    | <span data-ttu-id="fb266-412">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="fb266-412">THAI\_CHARSET</span></span> |

<span data-ttu-id="fb266-413">既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="fb266-413">The default character set is set to a value, depending on the current system locale.</span></span> <span data-ttu-id="fb266-414">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="fb266-414">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="fb266-415">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fb266-415">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="fb266-416">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="fb266-416">Method colorScheme</span></span>

<span data-ttu-id="fb266-417">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-417">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="fb266-418">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="fb266-418">Parameters - colorScheme</span></span>

<span data-ttu-id="fb266-419">値</span><span class="sxs-lookup"><span data-stu-id="fb266-419">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="fb266-420">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="fb266-420">Return Value - colorScheme</span></span>

<span data-ttu-id="fb266-421">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="fb266-421">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="fb266-422">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="fb266-422">Remarks - colorScheme</span></span>

<span data-ttu-id="fb266-423">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="fb266-423">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="fb266-424">値です。</span><span class="sxs-lookup"><span data-stu-id="fb266-424">Value.</span></span> | <span data-ttu-id="fb266-425">スタイル。</span><span class="sxs-lookup"><span data-stu-id="fb266-425">Style.</span></span>                 |
|--------|------------------------|
| <span data-ttu-id="fb266-426">0</span><span class="sxs-lookup"><span data-stu-id="fb266-426">0</span></span>      | <span data-ttu-id="fb266-427">既定。</span><span class="sxs-lookup"><span data-stu-id="fb266-427">Default.</span></span>               |
| <span data-ttu-id="fb266-428">1</span><span class="sxs-lookup"><span data-stu-id="fb266-428">1</span></span>      | <span data-ttu-id="fb266-429">Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="fb266-429">The Windows palette.</span></span>   |
| <span data-ttu-id="fb266-430">2</span><span class="sxs-lookup"><span data-stu-id="fb266-430">2</span></span>      | <span data-ttu-id="fb266-431">真の配色。</span><span class="sxs-lookup"><span data-stu-id="fb266-431">The true-color scheme.</span></span> |

## <a name="method-configurationkey"></a><span data-ttu-id="fb266-432">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="fb266-432">Method configurationKey</span></span>

<span data-ttu-id="fb266-433">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-433">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="fb266-434">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="fb266-434">Parameters - configurationKey</span></span>

<span data-ttu-id="fb266-435">値</span><span class="sxs-lookup"><span data-stu-id="fb266-435">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="fb266-436">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="fb266-436">Return Value - configurationKey</span></span>

<span data-ttu-id="fb266-437">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="fb266-437">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="fb266-438">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="fb266-438">Remarks - configurationKey</span></span>

<span data-ttu-id="fb266-439">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fb266-439">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="fb266-440">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="fb266-440">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-controltype"></a><span data-ttu-id="fb266-441">メソッド controlType</span><span class="sxs-lookup"><span data-stu-id="fb266-441">Method controlType</span></span>

```xpp
public ReportFieldType controlType()
```

### <a name="return-value---controltype"></a><span data-ttu-id="fb266-442">戻り値 - controlType</span><span class="sxs-lookup"><span data-stu-id="fb266-442">Return Value - controlType</span></span>

## <a name="method-cssclass"></a><span data-ttu-id="fb266-443">メソッド cssClass</span><span class="sxs-lookup"><span data-stu-id="fb266-443">Method cssClass</span></span>

```xpp
public str cssClass([str value])
```

### <a name="parameters---cssclass"></a><span data-ttu-id="fb266-444">パラメーター - cssClass</span><span class="sxs-lookup"><span data-stu-id="fb266-444">Parameters - cssClass</span></span>

<span data-ttu-id="fb266-445">値</span><span class="sxs-lookup"><span data-stu-id="fb266-445">value</span></span>  

### <a name="return-value---cssclass"></a><span data-ttu-id="fb266-446">戻り値 - cssClass</span><span class="sxs-lookup"><span data-stu-id="fb266-446">Return Value - cssClass</span></span>

## <a name="method-datafield"></a><span data-ttu-id="fb266-447">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="fb266-447">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="fb266-448">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="fb266-448">Parameters - dataField</span></span>

<span data-ttu-id="fb266-449">値</span><span class="sxs-lookup"><span data-stu-id="fb266-449">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="fb266-450">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="fb266-450">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="fb266-451">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="fb266-451">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="fb266-452">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="fb266-452">Parameters - dataMethod</span></span>

<span data-ttu-id="fb266-453">値</span><span class="sxs-lookup"><span data-stu-id="fb266-453">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="fb266-454">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="fb266-454">Return Value - dataMethod</span></span>

## <a name="method-delete"></a><span data-ttu-id="fb266-455">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="fb266-455">Method delete</span></span>

```xpp
public int delete()
```

### <a name="return-value---delete"></a><span data-ttu-id="fb266-456">戻り値 - delete</span><span class="sxs-lookup"><span data-stu-id="fb266-456">Return Value - delete</span></span>

## <a name="method-displacenegative"></a><span data-ttu-id="fb266-457">メソッド displaceNegative</span><span class="sxs-lookup"><span data-stu-id="fb266-457">Method displaceNegative</span></span>

```xpp
public int displaceNegative([int value], [AutoMode mode])
```

### <a name="parameters---displacenegative"></a><span data-ttu-id="fb266-458">パラメーター - displaceNegative</span><span class="sxs-lookup"><span data-stu-id="fb266-458">Parameters - displaceNegative</span></span>

<span data-ttu-id="fb266-459">値</span><span class="sxs-lookup"><span data-stu-id="fb266-459">value</span></span>  

<!-- -->

<span data-ttu-id="fb266-460">モード</span><span class="sxs-lookup"><span data-stu-id="fb266-460">mode</span></span>  

### <a name="return-value---displacenegative"></a><span data-ttu-id="fb266-461">戻り値 - displaceNegative</span><span class="sxs-lookup"><span data-stu-id="fb266-461">Return Value - displaceNegative</span></span>

## <a name="method-displacenegativemode"></a><span data-ttu-id="fb266-462">メソッド displaceNegativeMode</span><span class="sxs-lookup"><span data-stu-id="fb266-462">Method displaceNegativeMode</span></span>

```xpp
public AutoMode displaceNegativeMode([AutoMode mode])
```

### <a name="parameters---displacenegativemode"></a><span data-ttu-id="fb266-463">パラメーター - displaceNegativeMode</span><span class="sxs-lookup"><span data-stu-id="fb266-463">Parameters - displaceNegativeMode</span></span>

<span data-ttu-id="fb266-464">モード</span><span class="sxs-lookup"><span data-stu-id="fb266-464">mode</span></span>  

### <a name="return-value---displacenegativemode"></a><span data-ttu-id="fb266-465">戻り値 - displaceNegativeMode</span><span class="sxs-lookup"><span data-stu-id="fb266-465">Return Value - displaceNegativeMode</span></span>

## <a name="method-displacenegativevalue"></a><span data-ttu-id="fb266-466">メソッド displaceNegativeValue</span><span class="sxs-lookup"><span data-stu-id="fb266-466">Method displaceNegativeValue</span></span>

```xpp
public int displaceNegativeValue([int value])
```

### <a name="parameters---displacenegativevalue"></a><span data-ttu-id="fb266-467">パラメーター - displaceNegativeValue</span><span class="sxs-lookup"><span data-stu-id="fb266-467">Parameters - displaceNegativeValue</span></span>

<span data-ttu-id="fb266-468">値</span><span class="sxs-lookup"><span data-stu-id="fb266-468">value</span></span>  

### <a name="return-value---displacenegativevalue"></a><span data-ttu-id="fb266-469">戻り値 - displaceNegativeValue</span><span class="sxs-lookup"><span data-stu-id="fb266-469">Return Value - displaceNegativeValue</span></span>

## <a name="method-effectivefont"></a><span data-ttu-id="fb266-470">メソッド effectiveFont</span><span class="sxs-lookup"><span data-stu-id="fb266-470">Method effectiveFont</span></span>

```xpp
public str effectiveFont()
```

### <a name="return-value---effectivefont"></a><span data-ttu-id="fb266-471">戻り値 - effectiveFont</span><span class="sxs-lookup"><span data-stu-id="fb266-471">Return Value - effectiveFont</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="fb266-472">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="fb266-472">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="fb266-473">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="fb266-473">Parameters - extendedDataType</span></span>

<span data-ttu-id="fb266-474">値</span><span class="sxs-lookup"><span data-stu-id="fb266-474">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="fb266-475">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="fb266-475">Return Value - extendedDataType</span></span>

## <a name="method-extrasumwidthmode"></a><span data-ttu-id="fb266-476">メソッド extraSumWidthMode</span><span class="sxs-lookup"><span data-stu-id="fb266-476">Method extraSumWidthMode</span></span>

```xpp
public int extraSumWidthMode([int value])
```

### <a name="parameters---extrasumwidthmode"></a><span data-ttu-id="fb266-477">パラメーター - extraSumWidthMode</span><span class="sxs-lookup"><span data-stu-id="fb266-477">Parameters - extraSumWidthMode</span></span>

<span data-ttu-id="fb266-478">値</span><span class="sxs-lookup"><span data-stu-id="fb266-478">value</span></span>  

### <a name="return-value---extrasumwidthmode"></a><span data-ttu-id="fb266-479">戻り値 - extraSumWidthMode</span><span class="sxs-lookup"><span data-stu-id="fb266-479">Return Value - extraSumWidthMode</span></span>

## <a name="method-extrasumwidthstr"></a><span data-ttu-id="fb266-480">メソッド extraSumWidthStr</span><span class="sxs-lookup"><span data-stu-id="fb266-480">Method extraSumWidthStr</span></span>

```xpp
public str extraSumWidthStr([str value])
```

### <a name="parameters---extrasumwidthstr"></a><span data-ttu-id="fb266-481">パラメーター - extraSumWidthStr</span><span class="sxs-lookup"><span data-stu-id="fb266-481">Parameters - extraSumWidthStr</span></span>

<span data-ttu-id="fb266-482">値</span><span class="sxs-lookup"><span data-stu-id="fb266-482">value</span></span>  

### <a name="return-value---extrasumwidthstr"></a><span data-ttu-id="fb266-483">戻り値 - extraSumWidthStr</span><span class="sxs-lookup"><span data-stu-id="fb266-483">Return Value - extraSumWidthStr</span></span>

## <a name="method-extrasumwidthunit"></a><span data-ttu-id="fb266-484">メソッド extraSumWidthUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-484">Method extraSumWidthUnit</span></span>

```xpp
public Units extraSumWidthUnit([Units value])
```

### <a name="parameters---extrasumwidthunit"></a><span data-ttu-id="fb266-485">パラメーター - extraSumWidthUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-485">Parameters - extraSumWidthUnit</span></span>

<span data-ttu-id="fb266-486">値</span><span class="sxs-lookup"><span data-stu-id="fb266-486">value</span></span>  

### <a name="return-value---extrasumwidthunit"></a><span data-ttu-id="fb266-487">戻り値 - extraSumWidthUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-487">Return Value - extraSumWidthUnit</span></span>

## <a name="method-extrasumwidthvalue"></a><span data-ttu-id="fb266-488">メソッド extraSumWidthValue</span><span class="sxs-lookup"><span data-stu-id="fb266-488">Method extraSumWidthValue</span></span>

```xpp
public Real extraSumWidthValue([Real value])
```

### <a name="parameters---extrasumwidthvalue"></a><span data-ttu-id="fb266-489">パラメーター - extraSumWidthValue</span><span class="sxs-lookup"><span data-stu-id="fb266-489">Parameters - extraSumWidthValue</span></span>

<span data-ttu-id="fb266-490">値</span><span class="sxs-lookup"><span data-stu-id="fb266-490">value</span></span>  

### <a name="return-value---extrasumwidthvalue"></a><span data-ttu-id="fb266-491">戻り値 - extraSumWidthValue</span><span class="sxs-lookup"><span data-stu-id="fb266-491">Return Value - extraSumWidthValue</span></span>

## <a name="method-font"></a><span data-ttu-id="fb266-492">メソッド font</span><span class="sxs-lookup"><span data-stu-id="fb266-492">Method font</span></span>

<span data-ttu-id="fb266-493">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-493">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="fb266-494">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="fb266-494">Parameters - font</span></span>

<span data-ttu-id="fb266-495">値</span><span class="sxs-lookup"><span data-stu-id="fb266-495">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="fb266-496">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="fb266-496">Return Value - font</span></span>

<span data-ttu-id="fb266-497">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="fb266-497">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontinfoprinter"></a><span data-ttu-id="fb266-498">メソッド fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="fb266-498">Method fontInfoPrinter</span></span>

```xpp
public str fontInfoPrinter()
```

### <a name="return-value---fontinfoprinter"></a><span data-ttu-id="fb266-499">戻り値 - fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="fb266-499">Return Value - fontInfoPrinter</span></span>

## <a name="method-fontinfoprinterascent"></a><span data-ttu-id="fb266-500">メソッド fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="fb266-500">Method fontInfoPrinterAscent</span></span>

```xpp
public int fontInfoPrinterAscent()
```

### <a name="return-value---fontinfoprinterascent"></a><span data-ttu-id="fb266-501">戻り値 - fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="fb266-501">Return Value - fontInfoPrinterAscent</span></span>

## <a name="method-fontinfoprinterdescent"></a><span data-ttu-id="fb266-502">メソッド fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="fb266-502">Method fontInfoPrinterDescent</span></span>

```xpp
public int fontInfoPrinterDescent()
```

### <a name="return-value---fontinfoprinterdescent"></a><span data-ttu-id="fb266-503">戻り値 - fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="fb266-503">Return Value - fontInfoPrinterDescent</span></span>

## <a name="method-fontinfoprinterextlead"></a><span data-ttu-id="fb266-504">メソッド fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="fb266-504">Method fontInfoPrinterExtLead</span></span>

```xpp
public int fontInfoPrinterExtLead()
```

### <a name="return-value---fontinfoprinterextlead"></a><span data-ttu-id="fb266-505">戻り値 - fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="fb266-505">Return Value - fontInfoPrinterExtLead</span></span>

## <a name="method-fontinfoprinterheight"></a><span data-ttu-id="fb266-506">メソッド fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="fb266-506">Method fontInfoPrinterHeight</span></span>

```xpp
public int fontInfoPrinterHeight()
```

### <a name="return-value---fontinfoprinterheight"></a><span data-ttu-id="fb266-507">戻り値 - fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="fb266-507">Return Value - fontInfoPrinterHeight</span></span>

## <a name="method-fontinfoprinterintlead"></a><span data-ttu-id="fb266-508">メソッド fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="fb266-508">Method fontInfoPrinterIntLead</span></span>

```xpp
public int fontInfoPrinterIntLead()
```

### <a name="return-value---fontinfoprinterintlead"></a><span data-ttu-id="fb266-509">戻り値 - fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="fb266-509">Return Value - fontInfoPrinterIntLead</span></span>

## <a name="method-fontinfoscreen"></a><span data-ttu-id="fb266-510">メソッド fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="fb266-510">Method fontInfoScreen</span></span>

```xpp
public str fontInfoScreen()
```

### <a name="return-value---fontinfoscreen"></a><span data-ttu-id="fb266-511">戻り値 - fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="fb266-511">Return Value - fontInfoScreen</span></span>

## <a name="method-fontinfoscreenascent"></a><span data-ttu-id="fb266-512">メソッド fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="fb266-512">Method fontInfoScreenAscent</span></span>

```xpp
public int fontInfoScreenAscent()
```

### <a name="return-value---fontinfoscreenascent"></a><span data-ttu-id="fb266-513">戻り値 - fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="fb266-513">Return Value - fontInfoScreenAscent</span></span>

## <a name="method-fontinfoscreendescent"></a><span data-ttu-id="fb266-514">メソッド fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="fb266-514">Method fontInfoScreenDescent</span></span>

```xpp
public int fontInfoScreenDescent()
```

### <a name="return-value---fontinfoscreendescent"></a><span data-ttu-id="fb266-515">戻り値 - fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="fb266-515">Return Value - fontInfoScreenDescent</span></span>

## <a name="method-fontinfoscreenextlead"></a><span data-ttu-id="fb266-516">メソッド fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="fb266-516">Method fontInfoScreenExtLead</span></span>

```xpp
public int fontInfoScreenExtLead()
```

### <a name="return-value---fontinfoscreenextlead"></a><span data-ttu-id="fb266-517">戻り値 - fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="fb266-517">Return Value - fontInfoScreenExtLead</span></span>

## <a name="method-fontinfoscreenheight"></a><span data-ttu-id="fb266-518">メソッド fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="fb266-518">Method fontInfoScreenHeight</span></span>

```xpp
public int fontInfoScreenHeight()
```

### <a name="return-value---fontinfoscreenheight"></a><span data-ttu-id="fb266-519">戻り値 - fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="fb266-519">Return Value - fontInfoScreenHeight</span></span>

## <a name="method-fontinfoscreenintlead"></a><span data-ttu-id="fb266-520">メソッド fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="fb266-520">Method fontInfoScreenIntLead</span></span>

```xpp
public int fontInfoScreenIntLead()
```

### <a name="return-value---fontinfoscreenintlead"></a><span data-ttu-id="fb266-521">戻り値 - fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="fb266-521">Return Value - fontInfoScreenIntLead</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="fb266-522">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="fb266-522">Method fontSize</span></span>

<span data-ttu-id="fb266-523">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-523">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="fb266-524">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="fb266-524">Parameters - fontSize</span></span>

<span data-ttu-id="fb266-525">値</span><span class="sxs-lookup"><span data-stu-id="fb266-525">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="fb266-526">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="fb266-526">Return Value - fontSize</span></span>

<span data-ttu-id="fb266-527">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="fb266-527">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="fb266-528">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="fb266-528">Method foregroundColor</span></span>

<span data-ttu-id="fb266-529">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-529">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="fb266-530">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="fb266-530">Parameters - foregroundColor</span></span>

<span data-ttu-id="fb266-531">値</span><span class="sxs-lookup"><span data-stu-id="fb266-531">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="fb266-532">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="fb266-532">Return Value - foregroundColor</span></span>

<span data-ttu-id="fb266-533">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="fb266-533">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="fb266-534">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="fb266-534">Remarks - foregroundColor</span></span>

<span data-ttu-id="fb266-535">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fb266-535">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="fb266-536">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fb266-536">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="fb266-537">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="fb266-537">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="fb266-538">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="fb266-538">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="fb266-539">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="fb266-539">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="fb266-540">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="fb266-540">The maximum value for a single byte is 255.</span></span>

## <a name="method-height100mm"></a><span data-ttu-id="fb266-541">メソッド height100mm</span><span class="sxs-lookup"><span data-stu-id="fb266-541">Method height100mm</span></span>

```xpp
public int height100mm([int heightExclBorder])
```

### <a name="parameters---height100mm"></a><span data-ttu-id="fb266-542">パラメーター - height100mm</span><span class="sxs-lookup"><span data-stu-id="fb266-542">Parameters - height100mm</span></span>

<span data-ttu-id="fb266-543">heightExclBorder</span><span class="sxs-lookup"><span data-stu-id="fb266-543">heightExclBorder</span></span>  

### <a name="return-value---height100mm"></a><span data-ttu-id="fb266-544">戻り値 - height100mm</span><span class="sxs-lookup"><span data-stu-id="fb266-544">Return Value - height100mm</span></span>

## <a name="method-height100mminclborder"></a><span data-ttu-id="fb266-545">メソッド height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fb266-545">Method height100mmInclBorder</span></span>

```xpp
public int height100mmInclBorder([int heightInclBorder])
```

### <a name="parameters---height100mminclborder"></a><span data-ttu-id="fb266-546">パラメーター - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fb266-546">Parameters - height100mmInclBorder</span></span>

<span data-ttu-id="fb266-547">heightInclBorder</span><span class="sxs-lookup"><span data-stu-id="fb266-547">heightInclBorder</span></span>  

### <a name="return-value---height100mminclborder"></a><span data-ttu-id="fb266-548">戻り値 - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fb266-548">Return Value - height100mmInclBorder</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="fb266-549">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="fb266-549">Method heightMode</span></span>

<span data-ttu-id="fb266-550">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-550">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="fb266-551">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="fb266-551">Parameters - heightMode</span></span>

<span data-ttu-id="fb266-552">値</span><span class="sxs-lookup"><span data-stu-id="fb266-552">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="fb266-553">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="fb266-553">Return Value - heightMode</span></span>

<span data-ttu-id="fb266-554">計算モード。</span><span class="sxs-lookup"><span data-stu-id="fb266-554">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="fb266-555">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="fb266-555">Remarks - heightMode</span></span>

<span data-ttu-id="fb266-556">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="fb266-556">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="fb266-557">モード。</span><span class="sxs-lookup"><span data-stu-id="fb266-557">Mode.</span></span>          | <span data-ttu-id="fb266-558">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="fb266-558">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb266-559">正確。</span><span class="sxs-lookup"><span data-stu-id="fb266-559">Exact.</span></span>         | <span data-ttu-id="fb266-560">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="fb266-560">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="fb266-561">自動。</span><span class="sxs-lookup"><span data-stu-id="fb266-561">Auto.</span></span>          | <span data-ttu-id="fb266-562">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="fb266-562">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="fb266-563">列の高さ</span><span class="sxs-lookup"><span data-stu-id="fb266-563">Column height.</span></span> | <span data-ttu-id="fb266-564">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="fb266-564">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="fb266-565">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="fb266-565">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightofwordwrappedstring100mm"></a><span data-ttu-id="fb266-566">メソッド heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="fb266-566">Method heightOfWordWrappedString100mm</span></span>

```xpp
public int heightOfWordWrappedString100mm(str string)
```

### <a name="parameters---heightofwordwrappedstring100mm"></a><span data-ttu-id="fb266-567">パラメーター - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="fb266-567">Parameters - heightOfWordWrappedString100mm</span></span>

<span data-ttu-id="fb266-568">文字列</span><span class="sxs-lookup"><span data-stu-id="fb266-568">string</span></span>  

### <a name="return-value---heightofwordwrappedstring100mm"></a><span data-ttu-id="fb266-569">戻り値 - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="fb266-569">Return Value - heightOfWordWrappedString100mm</span></span>

## <a name="method-heightstr"></a><span data-ttu-id="fb266-570">メソッド heightStr</span><span class="sxs-lookup"><span data-stu-id="fb266-570">Method heightStr</span></span>

```xpp
public str heightStr([str value])
```

### <a name="parameters---heightstr"></a><span data-ttu-id="fb266-571">パラメーター - heightStr</span><span class="sxs-lookup"><span data-stu-id="fb266-571">Parameters - heightStr</span></span>

<span data-ttu-id="fb266-572">値</span><span class="sxs-lookup"><span data-stu-id="fb266-572">value</span></span>  

### <a name="return-value---heightstr"></a><span data-ttu-id="fb266-573">戻り値 - heightStr</span><span class="sxs-lookup"><span data-stu-id="fb266-573">Return Value - heightStr</span></span>

## <a name="method-heightunit"></a><span data-ttu-id="fb266-574">メソッド heightUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-574">Method heightUnit</span></span>

```xpp
public Units heightUnit([Units value])
```

### <a name="parameters---heightunit"></a><span data-ttu-id="fb266-575">パラメーター - heightUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-575">Parameters - heightUnit</span></span>

<span data-ttu-id="fb266-576">値</span><span class="sxs-lookup"><span data-stu-id="fb266-576">value</span></span>  

### <a name="return-value---heightunit"></a><span data-ttu-id="fb266-577">戻り値 - heightUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-577">Return Value - heightUnit</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="fb266-578">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="fb266-578">Method heightValue</span></span>

<span data-ttu-id="fb266-579">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-579">Gets or sets the height of the control.</span></span>

```xpp
public Real heightValue([Real value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="fb266-580">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="fb266-580">Parameters - heightValue</span></span>

<span data-ttu-id="fb266-581">値</span><span class="sxs-lookup"><span data-stu-id="fb266-581">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="fb266-582">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="fb266-582">Return Value - heightValue</span></span>

<span data-ttu-id="fb266-583">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="fb266-583">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="fb266-584">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="fb266-584">Remarks - heightValue</span></span>

<span data-ttu-id="fb266-585">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="fb266-585">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-italic"></a><span data-ttu-id="fb266-586">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="fb266-586">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="fb266-587">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="fb266-587">Parameters - italic</span></span>

<span data-ttu-id="fb266-588">値</span><span class="sxs-lookup"><span data-stu-id="fb266-588">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="fb266-589">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="fb266-589">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="fb266-590">メソッド label</span><span class="sxs-lookup"><span data-stu-id="fb266-590">Method label</span></span>

<span data-ttu-id="fb266-591">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-591">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="fb266-592">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="fb266-592">Parameters - label</span></span>

<span data-ttu-id="fb266-593">値</span><span class="sxs-lookup"><span data-stu-id="fb266-593">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="fb266-594">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="fb266-594">Return Value - label</span></span>

<span data-ttu-id="fb266-595">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="fb266-595">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="fb266-596">備考 - label</span><span class="sxs-lookup"><span data-stu-id="fb266-596">Remarks - label</span></span>

<span data-ttu-id="fb266-597">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-597">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="fb266-598">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="fb266-598">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="fb266-599">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="fb266-599">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="fb266-600">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="fb266-600">Parameters - labelBold</span></span>

<span data-ttu-id="fb266-601">値</span><span class="sxs-lookup"><span data-stu-id="fb266-601">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="fb266-602">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="fb266-602">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="fb266-603">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="fb266-603">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="fb266-604">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="fb266-604">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="fb266-605">値</span><span class="sxs-lookup"><span data-stu-id="fb266-605">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="fb266-606">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="fb266-606">Return Value - labelCharacterSet</span></span>

## <a name="method-labelcssclass"></a><span data-ttu-id="fb266-607">メソッド labelCssClass</span><span class="sxs-lookup"><span data-stu-id="fb266-607">Method labelCssClass</span></span>

```xpp
public str labelCssClass([str value])
```

### <a name="parameters---labelcssclass"></a><span data-ttu-id="fb266-608">パラメーター - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="fb266-608">Parameters - labelCssClass</span></span>

<span data-ttu-id="fb266-609">値</span><span class="sxs-lookup"><span data-stu-id="fb266-609">value</span></span>  

### <a name="return-value---labelcssclass"></a><span data-ttu-id="fb266-610">戻り値 - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="fb266-610">Return Value - labelCssClass</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="fb266-611">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="fb266-611">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="fb266-612">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="fb266-612">Parameters - labelFont</span></span>

<span data-ttu-id="fb266-613">値</span><span class="sxs-lookup"><span data-stu-id="fb266-613">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="fb266-614">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="fb266-614">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="fb266-615">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="fb266-615">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="fb266-616">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="fb266-616">Parameters - labelFontSize</span></span>

<span data-ttu-id="fb266-617">値</span><span class="sxs-lookup"><span data-stu-id="fb266-617">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="fb266-618">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="fb266-618">Return Value - labelFontSize</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="fb266-619">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="fb266-619">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="fb266-620">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="fb266-620">Parameters - labelItalic</span></span>

<span data-ttu-id="fb266-621">値</span><span class="sxs-lookup"><span data-stu-id="fb266-621">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="fb266-622">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="fb266-622">Return Value - labelItalic</span></span>

## <a name="method-labellinebelow"></a><span data-ttu-id="fb266-623">メソッド labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="fb266-623">Method labelLineBelow</span></span>

```xpp
public LineType labelLineBelow([LineType value])
```

### <a name="parameters---labellinebelow"></a><span data-ttu-id="fb266-624">パラメーター - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="fb266-624">Parameters - labelLineBelow</span></span>

<span data-ttu-id="fb266-625">値</span><span class="sxs-lookup"><span data-stu-id="fb266-625">value</span></span>  

### <a name="return-value---labellinebelow"></a><span data-ttu-id="fb266-626">戻り値 - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="fb266-626">Return Value - labelLineBelow</span></span>

## <a name="method-labellinethickness"></a><span data-ttu-id="fb266-627">メソッド labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="fb266-627">Method labelLineThickness</span></span>

```xpp
public LineThickness labelLineThickness([LineThickness value])
```

### <a name="parameters---labellinethickness"></a><span data-ttu-id="fb266-628">パラメーター - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="fb266-628">Parameters - labelLineThickness</span></span>

<span data-ttu-id="fb266-629">値</span><span class="sxs-lookup"><span data-stu-id="fb266-629">value</span></span>  

### <a name="return-value---labellinethickness"></a><span data-ttu-id="fb266-630">戻り値 - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="fb266-630">Return Value - labelLineThickness</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="fb266-631">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="fb266-631">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="fb266-632">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="fb266-632">Parameters - labelPosition</span></span>

<span data-ttu-id="fb266-633">値</span><span class="sxs-lookup"><span data-stu-id="fb266-633">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="fb266-634">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="fb266-634">Return Value - labelPosition</span></span>

## <a name="method-labeltableader"></a><span data-ttu-id="fb266-635">メソッド labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="fb266-635">Method labelTabLeader</span></span>

```xpp
public int labelTabLeader([int value])
```

### <a name="parameters---labeltableader"></a><span data-ttu-id="fb266-636">パラメーター - labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="fb266-636">Parameters - labelTabLeader</span></span>

<span data-ttu-id="fb266-637">値</span><span class="sxs-lookup"><span data-stu-id="fb266-637">value</span></span>  

### <a name="return-value---labeltableader"></a><span data-ttu-id="fb266-638">戻り値 - labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="fb266-638">Return Value - labelTabLeader</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="fb266-639">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="fb266-639">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="fb266-640">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="fb266-640">Parameters - labelUnderline</span></span>

<span data-ttu-id="fb266-641">値</span><span class="sxs-lookup"><span data-stu-id="fb266-641">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="fb266-642">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="fb266-642">Return Value - labelUnderline</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="fb266-643">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="fb266-643">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="fb266-644">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="fb266-644">Parameters - labelWidthMode</span></span>

<span data-ttu-id="fb266-645">値</span><span class="sxs-lookup"><span data-stu-id="fb266-645">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="fb266-646">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="fb266-646">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthstr"></a><span data-ttu-id="fb266-647">メソッド labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="fb266-647">Method labelWidthStr</span></span>

```xpp
public str labelWidthStr([str value])
```

### <a name="parameters---labelwidthstr"></a><span data-ttu-id="fb266-648">パラメーター - labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="fb266-648">Parameters - labelWidthStr</span></span>

<span data-ttu-id="fb266-649">値</span><span class="sxs-lookup"><span data-stu-id="fb266-649">value</span></span>  

### <a name="return-value---labelwidthstr"></a><span data-ttu-id="fb266-650">戻り値 - labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="fb266-650">Return Value - labelWidthStr</span></span>

## <a name="method-labelwidthunit"></a><span data-ttu-id="fb266-651">メソッド labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-651">Method labelWidthUnit</span></span>

```xpp
public Units labelWidthUnit([Units value])
```

### <a name="parameters---labelwidthunit"></a><span data-ttu-id="fb266-652">パラメーター - labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-652">Parameters - labelWidthUnit</span></span>

<span data-ttu-id="fb266-653">値</span><span class="sxs-lookup"><span data-stu-id="fb266-653">value</span></span>  

### <a name="return-value---labelwidthunit"></a><span data-ttu-id="fb266-654">戻り値 - labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-654">Return Value - labelWidthUnit</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="fb266-655">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="fb266-655">Method labelWidthValue</span></span>

```xpp
public Real labelWidthValue([Real value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="fb266-656">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="fb266-656">Parameters - labelWidthValue</span></span>

<span data-ttu-id="fb266-657">値</span><span class="sxs-lookup"><span data-stu-id="fb266-657">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="fb266-658">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="fb266-658">Return Value - labelWidthValue</span></span>

## <a name="method-left100mm"></a><span data-ttu-id="fb266-659">メソッド left100mm</span><span class="sxs-lookup"><span data-stu-id="fb266-659">Method left100mm</span></span>

```xpp
public int left100mm([int leftExclBorder])
```

### <a name="parameters---left100mm"></a><span data-ttu-id="fb266-660">パラメーター - left100mm</span><span class="sxs-lookup"><span data-stu-id="fb266-660">Parameters - left100mm</span></span>

<span data-ttu-id="fb266-661">leftExclBorder</span><span class="sxs-lookup"><span data-stu-id="fb266-661">leftExclBorder</span></span>  

### <a name="return-value---left100mm"></a><span data-ttu-id="fb266-662">戻り値 - left100mm</span><span class="sxs-lookup"><span data-stu-id="fb266-662">Return Value - left100mm</span></span>

## <a name="method-left100mminclborder"></a><span data-ttu-id="fb266-663">メソッド left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fb266-663">Method left100mmInclBorder</span></span>

```xpp
public int left100mmInclBorder([int leftInclBorder])
```

### <a name="parameters---left100mminclborder"></a><span data-ttu-id="fb266-664">パラメーター - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fb266-664">Parameters - left100mmInclBorder</span></span>

<span data-ttu-id="fb266-665">leftInclBorder</span><span class="sxs-lookup"><span data-stu-id="fb266-665">leftInclBorder</span></span>  

### <a name="return-value---left100mminclborder"></a><span data-ttu-id="fb266-666">戻り値 - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fb266-666">Return Value - left100mmInclBorder</span></span>

## <a name="method-leftmarginanframe"></a><span data-ttu-id="fb266-667">メソッド leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="fb266-667">Method leftMarginAnFrame</span></span>

```xpp
public int leftMarginAnFrame()
```

### <a name="return-value---leftmarginanframe"></a><span data-ttu-id="fb266-668">戻り値 - leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="fb266-668">Return Value - leftMarginAnFrame</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="fb266-669">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="fb266-669">Method leftMarginMode</span></span>

```xpp
public int leftMarginMode([int value])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="fb266-670">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="fb266-670">Parameters - leftMarginMode</span></span>

<span data-ttu-id="fb266-671">値</span><span class="sxs-lookup"><span data-stu-id="fb266-671">value</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="fb266-672">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="fb266-672">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginstr"></a><span data-ttu-id="fb266-673">メソッド leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="fb266-673">Method leftMarginStr</span></span>

```xpp
public str leftMarginStr([str value])
```

### <a name="parameters---leftmarginstr"></a><span data-ttu-id="fb266-674">パラメーター - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="fb266-674">Parameters - leftMarginStr</span></span>

<span data-ttu-id="fb266-675">値</span><span class="sxs-lookup"><span data-stu-id="fb266-675">value</span></span>  

### <a name="return-value---leftmarginstr"></a><span data-ttu-id="fb266-676">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="fb266-676">Return Value - leftMarginStr</span></span>

## <a name="method-leftmarginunit"></a><span data-ttu-id="fb266-677">メソッド leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-677">Method leftMarginUnit</span></span>

```xpp
public Units leftMarginUnit([Units value])
```

### <a name="parameters---leftmarginunit"></a><span data-ttu-id="fb266-678">パラメーター - leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-678">Parameters - leftMarginUnit</span></span>

<span data-ttu-id="fb266-679">値</span><span class="sxs-lookup"><span data-stu-id="fb266-679">value</span></span>  

### <a name="return-value---leftmarginunit"></a><span data-ttu-id="fb266-680">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="fb266-680">Return Value - leftMarginUnit</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="fb266-681">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="fb266-681">Method leftMarginValue</span></span>

```xpp
public Real leftMarginValue([Real value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="fb266-682">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="fb266-682">Parameters - leftMarginValue</span></span>

<span data-ttu-id="fb266-683">値</span><span class="sxs-lookup"><span data-stu-id="fb266-683">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="fb266-684">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="fb266-684">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="fb266-685">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="fb266-685">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="fb266-686">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="fb266-686">Parameters - leftMode</span></span>

<span data-ttu-id="fb266-687">値</span><span class="sxs-lookup"><span data-stu-id="fb266-687">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="fb266-688">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="fb266-688">Return Value - leftMode</span></span>

## <a name="method-leftstr"></a><span data-ttu-id="fb266-689">メソッド leftStr</span><span class="sxs-lookup"><span data-stu-id="fb266-689">Method leftStr</span></span>

```xpp
public str leftStr([str value])
```

### <a name="parameters---leftstr"></a><span data-ttu-id="fb266-690">パラメーター - leftStr</span><span class="sxs-lookup"><span data-stu-id="fb266-690">Parameters - leftStr</span></span>

<span data-ttu-id="fb266-691">値</span><span class="sxs-lookup"><span data-stu-id="fb266-691">value</span></span>  

### <a name="return-value---leftstr"></a><span data-ttu-id="fb266-692">戻り値 - leftStr</span><span class="sxs-lookup"><span data-stu-id="fb266-692">Return Value - leftStr</span></span>

## <a name="method-leftunit"></a><span data-ttu-id="fb266-693">メソッド leftUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-693">Method leftUnit</span></span>

```xpp
public Units leftUnit([Units value])
```

### <a name="parameters---leftunit"></a><span data-ttu-id="fb266-694">パラメーター - leftUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-694">Parameters - leftUnit</span></span>

<span data-ttu-id="fb266-695">値</span><span class="sxs-lookup"><span data-stu-id="fb266-695">value</span></span>  

### <a name="return-value---leftunit"></a><span data-ttu-id="fb266-696">戻り値 - leftUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-696">Return Value - leftUnit</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="fb266-697">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="fb266-697">Method leftValue</span></span>

```xpp
public Real leftValue([Real value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="fb266-698">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="fb266-698">Parameters - leftValue</span></span>

<span data-ttu-id="fb266-699">値</span><span class="sxs-lookup"><span data-stu-id="fb266-699">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="fb266-700">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="fb266-700">Return Value - leftValue</span></span>

## <a name="method-lineabove"></a><span data-ttu-id="fb266-701">メソッド lineAbove</span><span class="sxs-lookup"><span data-stu-id="fb266-701">Method lineAbove</span></span>

```xpp
public LineType lineAbove([LineType value])
```

### <a name="parameters---lineabove"></a><span data-ttu-id="fb266-702">パラメーター - lineAbove</span><span class="sxs-lookup"><span data-stu-id="fb266-702">Parameters - lineAbove</span></span>

<span data-ttu-id="fb266-703">値</span><span class="sxs-lookup"><span data-stu-id="fb266-703">value</span></span>  

### <a name="return-value---lineabove"></a><span data-ttu-id="fb266-704">戻り値 - lineAbove</span><span class="sxs-lookup"><span data-stu-id="fb266-704">Return Value - lineAbove</span></span>

## <a name="method-linebelow"></a><span data-ttu-id="fb266-705">メソッド lineBelow</span><span class="sxs-lookup"><span data-stu-id="fb266-705">Method lineBelow</span></span>

```xpp
public LineType lineBelow([LineType value])
```

### <a name="parameters---linebelow"></a><span data-ttu-id="fb266-706">パラメーター - lineBelow</span><span class="sxs-lookup"><span data-stu-id="fb266-706">Parameters - lineBelow</span></span>

<span data-ttu-id="fb266-707">値</span><span class="sxs-lookup"><span data-stu-id="fb266-707">value</span></span>  

### <a name="return-value---linebelow"></a><span data-ttu-id="fb266-708">戻り値 - lineBelow</span><span class="sxs-lookup"><span data-stu-id="fb266-708">Return Value - lineBelow</span></span>

## <a name="method-lineleft"></a><span data-ttu-id="fb266-709">メソッド lineLeft</span><span class="sxs-lookup"><span data-stu-id="fb266-709">Method lineLeft</span></span>

<span data-ttu-id="fb266-710">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-710">Gets or sets the type of line that is used as the left border of a section.</span></span>

```xpp
public LineType lineLeft([LineType value])
```

### <a name="parameters---lineleft"></a><span data-ttu-id="fb266-711">パラメーター - lineLeft</span><span class="sxs-lookup"><span data-stu-id="fb266-711">Parameters - lineLeft</span></span>

<span data-ttu-id="fb266-712">値</span><span class="sxs-lookup"><span data-stu-id="fb266-712">value</span></span>  

### <a name="return-value---lineleft"></a><span data-ttu-id="fb266-713">戻り値 - lineLeft</span><span class="sxs-lookup"><span data-stu-id="fb266-713">Return Value - lineLeft</span></span>

<span data-ttu-id="fb266-714">左境界線として使用される線のタイプ。</span><span class="sxs-lookup"><span data-stu-id="fb266-714">The type of line that is used as the left border.</span></span>

## <a name="method-lineright"></a><span data-ttu-id="fb266-715">メソッド lineRight</span><span class="sxs-lookup"><span data-stu-id="fb266-715">Method lineRight</span></span>

```xpp
public LineType lineRight([LineType value])
```

### <a name="parameters---lineright"></a><span data-ttu-id="fb266-716">パラメーター - lineRight</span><span class="sxs-lookup"><span data-stu-id="fb266-716">Parameters - lineRight</span></span>

<span data-ttu-id="fb266-717">値</span><span class="sxs-lookup"><span data-stu-id="fb266-717">value</span></span>  

### <a name="return-value---lineright"></a><span data-ttu-id="fb266-718">戻り値 - lineRight</span><span class="sxs-lookup"><span data-stu-id="fb266-718">Return Value - lineRight</span></span>

## <a name="method-menuitemlabel"></a><span data-ttu-id="fb266-719">メソッド menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="fb266-719">Method menuItemLabel</span></span>

```xpp
public str menuItemLabel([str value])
```

### <a name="parameters---menuitemlabel"></a><span data-ttu-id="fb266-720">パラメーター - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="fb266-720">Parameters - menuItemLabel</span></span>

<span data-ttu-id="fb266-721">値</span><span class="sxs-lookup"><span data-stu-id="fb266-721">value</span></span>  

### <a name="return-value---menuitemlabel"></a><span data-ttu-id="fb266-722">戻り値 - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="fb266-722">Return Value - menuItemLabel</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="fb266-723">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="fb266-723">Method menuItemName</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="fb266-724">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="fb266-724">Parameters - menuItemName</span></span>

<span data-ttu-id="fb266-725">値</span><span class="sxs-lookup"><span data-stu-id="fb266-725">value</span></span>  

### <a name="return-value---menuitemname"></a><span data-ttu-id="fb266-726">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="fb266-726">Return Value - menuItemName</span></span>

## <a name="method-menuitemtype"></a><span data-ttu-id="fb266-727">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="fb266-727">Method menuItemType</span></span>

```xpp
public MenuItemType menuItemType([MenuItemType value])
```

### <a name="parameters---menuitemtype"></a><span data-ttu-id="fb266-728">パラメーター - menuItemType</span><span class="sxs-lookup"><span data-stu-id="fb266-728">Parameters - menuItemType</span></span>

<span data-ttu-id="fb266-729">値</span><span class="sxs-lookup"><span data-stu-id="fb266-729">value</span></span>  

### <a name="return-value---menuitemtype"></a><span data-ttu-id="fb266-730">戻り値 - menuItemType</span><span class="sxs-lookup"><span data-stu-id="fb266-730">Return Value - menuItemType</span></span>

## <a name="method-modelfieldname"></a><span data-ttu-id="fb266-731">メソッド modelFieldName</span><span class="sxs-lookup"><span data-stu-id="fb266-731">Method modelFieldName</span></span>

```xpp
public str modelFieldName([str value])
```

### <a name="parameters---modelfieldname"></a><span data-ttu-id="fb266-732">パラメーター - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="fb266-732">Parameters - modelFieldName</span></span>

<span data-ttu-id="fb266-733">値</span><span class="sxs-lookup"><span data-stu-id="fb266-733">value</span></span>  

### <a name="return-value---modelfieldname"></a><span data-ttu-id="fb266-734">戻り値 - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="fb266-734">Return Value - modelFieldName</span></span>

## <a name="method-name"></a><span data-ttu-id="fb266-735">メソッド名</span><span class="sxs-lookup"><span data-stu-id="fb266-735">Method name</span></span>

<span data-ttu-id="fb266-736">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-736">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="fb266-737">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="fb266-737">Parameters - name</span></span>

<span data-ttu-id="fb266-738">値</span><span class="sxs-lookup"><span data-stu-id="fb266-738">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="fb266-739">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="fb266-739">Return Value - name</span></span>

<span data-ttu-id="fb266-740">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="fb266-740">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="fb266-741">備考 - name</span><span class="sxs-lookup"><span data-stu-id="fb266-741">Remarks - name</span></span>

<span data-ttu-id="fb266-742">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb266-742">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="fb266-743">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="fb266-743">Begins with a letter.</span></span>
-   <span data-ttu-id="fb266-744">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="fb266-744">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="fb266-745">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="fb266-745">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="fb266-746">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="fb266-746">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="fb266-747">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="fb266-747">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-numberoflines"></a><span data-ttu-id="fb266-748">メソッド numberOfLines</span><span class="sxs-lookup"><span data-stu-id="fb266-748">Method numberOfLines</span></span>

```xpp
public int numberOfLines(int height100mm)
```

### <a name="parameters---numberoflines"></a><span data-ttu-id="fb266-749">パラメーター - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="fb266-749">Parameters - numberOfLines</span></span>

<span data-ttu-id="fb266-750">height100mm</span><span class="sxs-lookup"><span data-stu-id="fb266-750">height100mm</span></span>  

### <a name="return-value---numberoflines"></a><span data-ttu-id="fb266-751">戻り値 - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="fb266-751">Return Value - numberOfLines</span></span>

## <a name="method-position"></a><span data-ttu-id="fb266-752">メソッドの位置</span><span class="sxs-lookup"><span data-stu-id="fb266-752">Method position</span></span>

```xpp
public int position([int value])
```

### <a name="parameters---position"></a><span data-ttu-id="fb266-753">パラメーター - position</span><span class="sxs-lookup"><span data-stu-id="fb266-753">Parameters - position</span></span>

<span data-ttu-id="fb266-754">値</span><span class="sxs-lookup"><span data-stu-id="fb266-754">value</span></span>  

### <a name="return-value---position"></a><span data-ttu-id="fb266-755">戻り値 - position</span><span class="sxs-lookup"><span data-stu-id="fb266-755">Return Value - position</span></span>

## <a name="method-previewinfo"></a><span data-ttu-id="fb266-756">メソッド previewInfo</span><span class="sxs-lookup"><span data-stu-id="fb266-756">Method previewInfo</span></span>

```xpp
public str previewInfo(str string)
```

### <a name="parameters---previewinfo"></a><span data-ttu-id="fb266-757">パラメーター - previewInfo</span><span class="sxs-lookup"><span data-stu-id="fb266-757">Parameters - previewInfo</span></span>

<span data-ttu-id="fb266-758">文字列</span><span class="sxs-lookup"><span data-stu-id="fb266-758">string</span></span>  

### <a name="return-value---previewinfo"></a><span data-ttu-id="fb266-759">戻り値 - previewInfo</span><span class="sxs-lookup"><span data-stu-id="fb266-759">Return Value - previewInfo</span></span>

## <a name="method-previewxcompensation100mm"></a><span data-ttu-id="fb266-760">メソッド previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="fb266-760">Method previewXCompensation100mm</span></span>

```xpp
public int previewXCompensation100mm(str string)
```

### <a name="parameters---previewxcompensation100mm"></a><span data-ttu-id="fb266-761">パラメーター - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="fb266-761">Parameters - previewXCompensation100mm</span></span>

<span data-ttu-id="fb266-762">文字列</span><span class="sxs-lookup"><span data-stu-id="fb266-762">string</span></span>  

### <a name="return-value---previewxcompensation100mm"></a><span data-ttu-id="fb266-763">戻り値 - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="fb266-763">Return Value - previewXCompensation100mm</span></span>

## <a name="method-right100mm"></a><span data-ttu-id="fb266-764">メソッド right100mm</span><span class="sxs-lookup"><span data-stu-id="fb266-764">Method right100mm</span></span>

```xpp
public int right100mm()
```

### <a name="return-value---right100mm"></a><span data-ttu-id="fb266-765">戻り値 - right100mm</span><span class="sxs-lookup"><span data-stu-id="fb266-765">Return Value - right100mm</span></span>

## <a name="method-right100mminclborder"></a><span data-ttu-id="fb266-766">メソッド right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fb266-766">Method right100mmInclBorder</span></span>

```xpp
public int right100mmInclBorder()
```

### <a name="return-value---right100mminclborder"></a><span data-ttu-id="fb266-767">戻り値 - right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fb266-767">Return Value - right100mmInclBorder</span></span>

## <a name="method-rightmarginandframe"></a><span data-ttu-id="fb266-768">メソッド rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="fb266-768">Method rightMarginAndFrame</span></span>

```xpp
public int rightMarginAndFrame()
```

### <a name="return-value---rightmarginandframe"></a><span data-ttu-id="fb266-769">戻り値 - rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="fb266-769">Return Value - rightMarginAndFrame</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="fb266-770">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="fb266-770">Method rightMarginMode</span></span>

```xpp
public int rightMarginMode([int value])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="fb266-771">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="fb266-771">Parameters - rightMarginMode</span></span>

<span data-ttu-id="fb266-772">値</span><span class="sxs-lookup"><span data-stu-id="fb266-772">value</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="fb266-773">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="fb266-773">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginstr"></a><span data-ttu-id="fb266-774">メソッド rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="fb266-774">Method rightMarginStr</span></span>

```xpp
public str rightMarginStr([str value])
```

### <a name="parameters---rightmarginstr"></a><span data-ttu-id="fb266-775">パラメーター - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="fb266-775">Parameters - rightMarginStr</span></span>

<span data-ttu-id="fb266-776">値</span><span class="sxs-lookup"><span data-stu-id="fb266-776">value</span></span>  

### <a name="return-value---rightmarginstr"></a><span data-ttu-id="fb266-777">戻り値 - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="fb266-777">Return Value - rightMarginStr</span></span>

## <a name="method-rightmarginunit"></a><span data-ttu-id="fb266-778">メソッド rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-778">Method rightMarginUnit</span></span>

```xpp
public Units rightMarginUnit([Units value])
```

### <a name="parameters---rightmarginunit"></a><span data-ttu-id="fb266-779">パラメーター - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-779">Parameters - rightMarginUnit</span></span>

<span data-ttu-id="fb266-780">値</span><span class="sxs-lookup"><span data-stu-id="fb266-780">value</span></span>  

### <a name="return-value---rightmarginunit"></a><span data-ttu-id="fb266-781">戻り値 - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-781">Return Value - rightMarginUnit</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="fb266-782">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="fb266-782">Method rightMarginValue</span></span>

```xpp
public Real rightMarginValue([Real value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="fb266-783">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="fb266-783">Parameters - rightMarginValue</span></span>

<span data-ttu-id="fb266-784">値</span><span class="sxs-lookup"><span data-stu-id="fb266-784">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="fb266-785">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="fb266-785">Return Value - rightMarginValue</span></span>

## <a name="method-rotatesign"></a><span data-ttu-id="fb266-786">メソッド rotateSign</span><span class="sxs-lookup"><span data-stu-id="fb266-786">Method rotateSign</span></span>

```xpp
public int rotateSign([int value])
```

### <a name="parameters---rotatesign"></a><span data-ttu-id="fb266-787">パラメーター - rotateSign</span><span class="sxs-lookup"><span data-stu-id="fb266-787">Parameters - rotateSign</span></span>

<span data-ttu-id="fb266-788">値</span><span class="sxs-lookup"><span data-stu-id="fb266-788">value</span></span>  

### <a name="return-value---rotatesign"></a><span data-ttu-id="fb266-789">戻り値 - rotateSign</span><span class="sxs-lookup"><span data-stu-id="fb266-789">Return Value - rotateSign</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="fb266-790">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="fb266-790">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="fb266-791">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="fb266-791">Parameters - securityKey</span></span>

<span data-ttu-id="fb266-792">値</span><span class="sxs-lookup"><span data-stu-id="fb266-792">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="fb266-793">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="fb266-793">Return Value - securityKey</span></span>

## <a name="method-setheightgettext"></a><span data-ttu-id="fb266-794">メソッド setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="fb266-794">Method setHeightGetText</span></span>

```xpp
public str setHeightGetText(int lines, str string)
```

### <a name="parameters---setheightgettext"></a><span data-ttu-id="fb266-795">パラメーター - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="fb266-795">Parameters - setHeightGetText</span></span>

<span data-ttu-id="fb266-796">明細行</span><span class="sxs-lookup"><span data-stu-id="fb266-796">lines</span></span>  

<!-- -->

<span data-ttu-id="fb266-797">文字列</span><span class="sxs-lookup"><span data-stu-id="fb266-797">string</span></span>  

### <a name="return-value---setheightgettext"></a><span data-ttu-id="fb266-798">戻り値 - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="fb266-798">Return Value - setHeightGetText</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="fb266-799">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="fb266-799">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="fb266-800">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="fb266-800">Parameters - showLabel</span></span>

<span data-ttu-id="fb266-801">値</span><span class="sxs-lookup"><span data-stu-id="fb266-801">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="fb266-802">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="fb266-802">Return Value - showLabel</span></span>

## <a name="method-showzero"></a><span data-ttu-id="fb266-803">メソッド showZero</span><span class="sxs-lookup"><span data-stu-id="fb266-803">Method showZero</span></span>

```xpp
public int showZero([int value])
```

### <a name="parameters---showzero"></a><span data-ttu-id="fb266-804">パラメーター - showZero</span><span class="sxs-lookup"><span data-stu-id="fb266-804">Parameters - showZero</span></span>

<span data-ttu-id="fb266-805">値</span><span class="sxs-lookup"><span data-stu-id="fb266-805">value</span></span>  

### <a name="return-value---showzero"></a><span data-ttu-id="fb266-806">戻り値 - showZero</span><span class="sxs-lookup"><span data-stu-id="fb266-806">Return Value - showZero</span></span>

## <a name="method-signdisplay"></a><span data-ttu-id="fb266-807">メソッド signDisplay</span><span class="sxs-lookup"><span data-stu-id="fb266-807">Method signDisplay</span></span>

```xpp
public int signDisplay([int value])
```

### <a name="parameters---signdisplay"></a><span data-ttu-id="fb266-808">パラメーター - signDisplay</span><span class="sxs-lookup"><span data-stu-id="fb266-808">Parameters - signDisplay</span></span>

<span data-ttu-id="fb266-809">値</span><span class="sxs-lookup"><span data-stu-id="fb266-809">value</span></span>  

### <a name="return-value---signdisplay"></a><span data-ttu-id="fb266-810">戻り値 - signDisplay</span><span class="sxs-lookup"><span data-stu-id="fb266-810">Return Value - signDisplay</span></span>

## <a name="method-sumall"></a><span data-ttu-id="fb266-811">メソッド sumAll</span><span class="sxs-lookup"><span data-stu-id="fb266-811">Method sumAll</span></span>

```xpp
public boolean sumAll([boolean value])
```

### <a name="parameters---sumall"></a><span data-ttu-id="fb266-812">パラメーター - sumAll</span><span class="sxs-lookup"><span data-stu-id="fb266-812">Parameters - sumAll</span></span>

<span data-ttu-id="fb266-813">値</span><span class="sxs-lookup"><span data-stu-id="fb266-813">value</span></span>  

### <a name="return-value---sumall"></a><span data-ttu-id="fb266-814">戻り値 - sumAll</span><span class="sxs-lookup"><span data-stu-id="fb266-814">Return Value - sumAll</span></span>

## <a name="method-sumneg"></a><span data-ttu-id="fb266-815">メソッド sumNeg</span><span class="sxs-lookup"><span data-stu-id="fb266-815">Method sumNeg</span></span>

```xpp
public boolean sumNeg([boolean value])
```

### <a name="parameters---sumneg"></a><span data-ttu-id="fb266-816">パラメーター - sumNeg</span><span class="sxs-lookup"><span data-stu-id="fb266-816">Parameters - sumNeg</span></span>

<span data-ttu-id="fb266-817">値</span><span class="sxs-lookup"><span data-stu-id="fb266-817">value</span></span>  

### <a name="return-value---sumneg"></a><span data-ttu-id="fb266-818">戻り値 - sumNeg</span><span class="sxs-lookup"><span data-stu-id="fb266-818">Return Value - sumNeg</span></span>

## <a name="method-sumpos"></a><span data-ttu-id="fb266-819">メソッド sumPos</span><span class="sxs-lookup"><span data-stu-id="fb266-819">Method sumPos</span></span>

```xpp
public boolean sumPos([boolean value])
```

### <a name="parameters---sumpos"></a><span data-ttu-id="fb266-820">パラメーター - sumPos</span><span class="sxs-lookup"><span data-stu-id="fb266-820">Parameters - sumPos</span></span>

<span data-ttu-id="fb266-821">値</span><span class="sxs-lookup"><span data-stu-id="fb266-821">value</span></span>  

### <a name="return-value---sumpos"></a><span data-ttu-id="fb266-822">戻り値 - sumPos</span><span class="sxs-lookup"><span data-stu-id="fb266-822">Return Value - sumPos</span></span>

## <a name="method-table"></a><span data-ttu-id="fb266-823">メソッド table</span><span class="sxs-lookup"><span data-stu-id="fb266-823">Method table</span></span>

<span data-ttu-id="fb266-824">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-824">Gets or sets the table ID associated with the object.</span></span>

```xpp
public TableId table([TableId value])
```

### <a name="parameters---table"></a><span data-ttu-id="fb266-825">パラメーター - table</span><span class="sxs-lookup"><span data-stu-id="fb266-825">Parameters - table</span></span>

<span data-ttu-id="fb266-826">値</span><span class="sxs-lookup"><span data-stu-id="fb266-826">value</span></span>  

### <a name="return-value---table"></a><span data-ttu-id="fb266-827">戻り値 - toBlob</span><span class="sxs-lookup"><span data-stu-id="fb266-827">Return Value - table</span></span>

<span data-ttu-id="fb266-828">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="fb266-828">The current value of the table ID associated with the object.</span></span>

## <a name="method-thickness"></a><span data-ttu-id="fb266-829">メソッド thickness</span><span class="sxs-lookup"><span data-stu-id="fb266-829">Method thickness</span></span>

```xpp
public LineThickness thickness([LineThickness value])
```

### <a name="parameters---thickness"></a><span data-ttu-id="fb266-830">パラメーター - thickness</span><span class="sxs-lookup"><span data-stu-id="fb266-830">Parameters - thickness</span></span>

<span data-ttu-id="fb266-831">値</span><span class="sxs-lookup"><span data-stu-id="fb266-831">value</span></span>  

### <a name="return-value---thickness"></a><span data-ttu-id="fb266-832">戻り値 - thickness</span><span class="sxs-lookup"><span data-stu-id="fb266-832">Return Value - thickness</span></span>

## <a name="method-top100mm"></a><span data-ttu-id="fb266-833">メソッド top100mm</span><span class="sxs-lookup"><span data-stu-id="fb266-833">Method top100mm</span></span>

```xpp
public int top100mm([int topExclBorder])
```

### <a name="parameters---top100mm"></a><span data-ttu-id="fb266-834">パラメーター - top100mm</span><span class="sxs-lookup"><span data-stu-id="fb266-834">Parameters - top100mm</span></span>

<span data-ttu-id="fb266-835">topExclBorder</span><span class="sxs-lookup"><span data-stu-id="fb266-835">topExclBorder</span></span>  

### <a name="return-value---top100mm"></a><span data-ttu-id="fb266-836">戻り値 - top100mm</span><span class="sxs-lookup"><span data-stu-id="fb266-836">Return Value - top100mm</span></span>

## <a name="method-top100mminclborder"></a><span data-ttu-id="fb266-837">メソッド top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fb266-837">Method top100mmInclBorder</span></span>

```xpp
public int top100mmInclBorder([int topInclBorder])
```

### <a name="parameters---top100mminclborder"></a><span data-ttu-id="fb266-838">パラメーター - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fb266-838">Parameters - top100mmInclBorder</span></span>

<span data-ttu-id="fb266-839">topInclBorder</span><span class="sxs-lookup"><span data-stu-id="fb266-839">topInclBorder</span></span>  

### <a name="return-value---top100mminclborder"></a><span data-ttu-id="fb266-840">戻り値 - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fb266-840">Return Value - top100mmInclBorder</span></span>

## <a name="method-topmarginandframe"></a><span data-ttu-id="fb266-841">メソッド topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="fb266-841">Method topMarginAndFrame</span></span>

```xpp
public int topMarginAndFrame()
```

### <a name="return-value---topmarginandframe"></a><span data-ttu-id="fb266-842">戻り値 - topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="fb266-842">Return Value - topMarginAndFrame</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="fb266-843">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="fb266-843">Method topMarginMode</span></span>

```xpp
public int topMarginMode([int value])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="fb266-844">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="fb266-844">Parameters - topMarginMode</span></span>

<span data-ttu-id="fb266-845">値</span><span class="sxs-lookup"><span data-stu-id="fb266-845">value</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="fb266-846">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="fb266-846">Return Value - topMarginMode</span></span>

## <a name="method-topmarginstr"></a><span data-ttu-id="fb266-847">メソッド topMarginStr</span><span class="sxs-lookup"><span data-stu-id="fb266-847">Method topMarginStr</span></span>

```xpp
public str topMarginStr([str value])
```

### <a name="parameters---topmarginstr"></a><span data-ttu-id="fb266-848">パラメーター - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="fb266-848">Parameters - topMarginStr</span></span>

<span data-ttu-id="fb266-849">値</span><span class="sxs-lookup"><span data-stu-id="fb266-849">value</span></span>  

### <a name="return-value---topmarginstr"></a><span data-ttu-id="fb266-850">戻り値 - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="fb266-850">Return Value - topMarginStr</span></span>

## <a name="method-topmarginunit"></a><span data-ttu-id="fb266-851">メソッド topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-851">Method topMarginUnit</span></span>

```xpp
public Units topMarginUnit([Units value])
```

### <a name="parameters---topmarginunit"></a><span data-ttu-id="fb266-852">パラメーター - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-852">Parameters - topMarginUnit</span></span>

<span data-ttu-id="fb266-853">値</span><span class="sxs-lookup"><span data-stu-id="fb266-853">value</span></span>  

### <a name="return-value---topmarginunit"></a><span data-ttu-id="fb266-854">戻り値 - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-854">Return Value - topMarginUnit</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="fb266-855">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="fb266-855">Method topMarginValue</span></span>

```xpp
public Real topMarginValue([Real value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="fb266-856">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="fb266-856">Parameters - topMarginValue</span></span>

<span data-ttu-id="fb266-857">値</span><span class="sxs-lookup"><span data-stu-id="fb266-857">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="fb266-858">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="fb266-858">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="fb266-859">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="fb266-859">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="fb266-860">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="fb266-860">Parameters - topMode</span></span>

<span data-ttu-id="fb266-861">値</span><span class="sxs-lookup"><span data-stu-id="fb266-861">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="fb266-862">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="fb266-862">Return Value - topMode</span></span>

## <a name="method-topstr"></a><span data-ttu-id="fb266-863">メソッド topStr</span><span class="sxs-lookup"><span data-stu-id="fb266-863">Method topStr</span></span>

```xpp
public str topStr([str value])
```

### <a name="parameters---topstr"></a><span data-ttu-id="fb266-864">パラメーター - topStr</span><span class="sxs-lookup"><span data-stu-id="fb266-864">Parameters - topStr</span></span>

<span data-ttu-id="fb266-865">値</span><span class="sxs-lookup"><span data-stu-id="fb266-865">value</span></span>  

### <a name="return-value---topstr"></a><span data-ttu-id="fb266-866">戻り値 - topStr</span><span class="sxs-lookup"><span data-stu-id="fb266-866">Return Value - topStr</span></span>

## <a name="method-topunit"></a><span data-ttu-id="fb266-867">メソッド topUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-867">Method topUnit</span></span>

```xpp
public Units topUnit([Units value])
```

### <a name="parameters---topunit"></a><span data-ttu-id="fb266-868">パラメーター - topUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-868">Parameters - topUnit</span></span>

<span data-ttu-id="fb266-869">値</span><span class="sxs-lookup"><span data-stu-id="fb266-869">value</span></span>  

### <a name="return-value---topunit"></a><span data-ttu-id="fb266-870">戻り値 - topUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-870">Return Value - topUnit</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="fb266-871">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="fb266-871">Method topValue</span></span>

```xpp
public Real topValue([Real value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="fb266-872">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="fb266-872">Parameters - topValue</span></span>

<span data-ttu-id="fb266-873">値</span><span class="sxs-lookup"><span data-stu-id="fb266-873">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="fb266-874">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="fb266-874">Return Value - topValue</span></span>

## <a name="method-underline"></a><span data-ttu-id="fb266-875">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="fb266-875">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="fb266-876">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="fb266-876">Parameters - underline</span></span>

<span data-ttu-id="fb266-877">値</span><span class="sxs-lookup"><span data-stu-id="fb266-877">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="fb266-878">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="fb266-878">Return Value - underline</span></span>

## <a name="method-visible"></a><span data-ttu-id="fb266-879">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="fb266-879">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="fb266-880">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="fb266-880">Parameters - visible</span></span>

<span data-ttu-id="fb266-881">値</span><span class="sxs-lookup"><span data-stu-id="fb266-881">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="fb266-882">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="fb266-882">Return Value - visible</span></span>

## <a name="method-webmenuitemname"></a><span data-ttu-id="fb266-883">メソッド webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="fb266-883">Method webMenuItemName</span></span>

```xpp
public str webMenuItemName([str value])
```

### <a name="parameters---webmenuitemname"></a><span data-ttu-id="fb266-884">パラメーター - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="fb266-884">Parameters - webMenuItemName</span></span>

<span data-ttu-id="fb266-885">値</span><span class="sxs-lookup"><span data-stu-id="fb266-885">value</span></span>  

### <a name="return-value---webmenuitemname"></a><span data-ttu-id="fb266-886">戻り値 - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="fb266-886">Return Value - webMenuItemName</span></span>

## <a name="method-webmenuitemtype"></a><span data-ttu-id="fb266-887">メソッド webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="fb266-887">Method webMenuItemType</span></span>

```xpp
public WebMenuItemType webMenuItemType([WebMenuItemType value])
```

### <a name="parameters---webmenuitemtype"></a><span data-ttu-id="fb266-888">パラメーター - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="fb266-888">Parameters - webMenuItemType</span></span>

<span data-ttu-id="fb266-889">値</span><span class="sxs-lookup"><span data-stu-id="fb266-889">value</span></span>  

### <a name="return-value---webmenuitemtype"></a><span data-ttu-id="fb266-890">戻り値 - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="fb266-890">Return Value - webMenuItemType</span></span>

## <a name="method-webtarget"></a><span data-ttu-id="fb266-891">メソッド webTarget</span><span class="sxs-lookup"><span data-stu-id="fb266-891">Method webTarget</span></span>

```xpp
public str webTarget([str value])
```

### <a name="parameters---webtarget"></a><span data-ttu-id="fb266-892">パラメーター - webTarget</span><span class="sxs-lookup"><span data-stu-id="fb266-892">Parameters - webTarget</span></span>

<span data-ttu-id="fb266-893">値</span><span class="sxs-lookup"><span data-stu-id="fb266-893">value</span></span>  

### <a name="return-value---webtarget"></a><span data-ttu-id="fb266-894">戻り値 - webTarget</span><span class="sxs-lookup"><span data-stu-id="fb266-894">Return Value - webTarget</span></span>

## <a name="method-width100mm"></a><span data-ttu-id="fb266-895">メソッド width100mm</span><span class="sxs-lookup"><span data-stu-id="fb266-895">Method width100mm</span></span>

```xpp
public int width100mm([int widthExclBorder])
```

### <a name="parameters---width100mm"></a><span data-ttu-id="fb266-896">パラメーター - width100mm</span><span class="sxs-lookup"><span data-stu-id="fb266-896">Parameters - width100mm</span></span>

<span data-ttu-id="fb266-897">widthExclBorder</span><span class="sxs-lookup"><span data-stu-id="fb266-897">widthExclBorder</span></span>  

### <a name="return-value---width100mm"></a><span data-ttu-id="fb266-898">戻り値 - width100mm</span><span class="sxs-lookup"><span data-stu-id="fb266-898">Return Value - width100mm</span></span>

## <a name="method-width100mminclborder"></a><span data-ttu-id="fb266-899">メソッド width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fb266-899">Method width100mmInclBorder</span></span>

```xpp
public int width100mmInclBorder([int widthInclBorder])
```

### <a name="parameters---width100mminclborder"></a><span data-ttu-id="fb266-900">パラメーター - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fb266-900">Parameters - width100mmInclBorder</span></span>

<span data-ttu-id="fb266-901">widthInclBorder</span><span class="sxs-lookup"><span data-stu-id="fb266-901">widthInclBorder</span></span>  

### <a name="return-value---width100mminclborder"></a><span data-ttu-id="fb266-902">戻り値 - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="fb266-902">Return Value - width100mmInclBorder</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="fb266-903">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="fb266-903">Method widthMode</span></span>

<span data-ttu-id="fb266-904">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-904">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="fb266-905">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="fb266-905">Parameters - widthMode</span></span>

<span data-ttu-id="fb266-906">値</span><span class="sxs-lookup"><span data-stu-id="fb266-906">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="fb266-907">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="fb266-907">Return Value - widthMode</span></span>

<span data-ttu-id="fb266-908">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="fb266-908">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="fb266-909">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="fb266-909">Remarks - widthMode</span></span>

<span data-ttu-id="fb266-910">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="fb266-910">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="fb266-911">モード。</span><span class="sxs-lookup"><span data-stu-id="fb266-911">Mode.</span></span>         | <span data-ttu-id="fb266-912">幅計算。</span><span class="sxs-lookup"><span data-stu-id="fb266-912">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb266-913">正確。</span><span class="sxs-lookup"><span data-stu-id="fb266-913">Exact.</span></span>        | <span data-ttu-id="fb266-914">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="fb266-914">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="fb266-915">自動。</span><span class="sxs-lookup"><span data-stu-id="fb266-915">Auto.</span></span>         | <span data-ttu-id="fb266-916">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="fb266-916">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="fb266-917">列の幅。</span><span class="sxs-lookup"><span data-stu-id="fb266-917">Column width.</span></span> | <span data-ttu-id="fb266-918">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="fb266-918">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="fb266-919">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="fb266-919">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthofstring100mm"></a><span data-ttu-id="fb266-920">メソッド widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="fb266-920">Method widthOfString100mm</span></span>

```xpp
public int widthOfString100mm(str string)
```

### <a name="parameters---widthofstring100mm"></a><span data-ttu-id="fb266-921">パラメーター - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="fb266-921">Parameters - widthOfString100mm</span></span>

<span data-ttu-id="fb266-922">文字列</span><span class="sxs-lookup"><span data-stu-id="fb266-922">string</span></span>  

### <a name="return-value---widthofstring100mm"></a><span data-ttu-id="fb266-923">戻り値 - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="fb266-923">Return Value - widthOfString100mm</span></span>

## <a name="method-widthstr"></a><span data-ttu-id="fb266-924">メソッド widthStr</span><span class="sxs-lookup"><span data-stu-id="fb266-924">Method widthStr</span></span>

```xpp
public str widthStr([str value])
```

### <a name="parameters---widthstr"></a><span data-ttu-id="fb266-925">パラメーター - widthStr</span><span class="sxs-lookup"><span data-stu-id="fb266-925">Parameters - widthStr</span></span>

<span data-ttu-id="fb266-926">値</span><span class="sxs-lookup"><span data-stu-id="fb266-926">value</span></span>  

### <a name="return-value---widthstr"></a><span data-ttu-id="fb266-927">戻り値 - widthStr</span><span class="sxs-lookup"><span data-stu-id="fb266-927">Return Value - widthStr</span></span>

## <a name="method-widthunit"></a><span data-ttu-id="fb266-928">メソッド widthUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-928">Method widthUnit</span></span>

```xpp
public Units widthUnit([Units value])
```

### <a name="parameters---widthunit"></a><span data-ttu-id="fb266-929">パラメーター - widthUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-929">Parameters - widthUnit</span></span>

<span data-ttu-id="fb266-930">値</span><span class="sxs-lookup"><span data-stu-id="fb266-930">value</span></span>  

### <a name="return-value---widthunit"></a><span data-ttu-id="fb266-931">戻り値 - widthUnit</span><span class="sxs-lookup"><span data-stu-id="fb266-931">Return Value - widthUnit</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="fb266-932">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="fb266-932">Method widthValue</span></span>

<span data-ttu-id="fb266-933">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-933">Gets or sets the width of the control.</span></span>

```xpp
public Real widthValue([Real value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="fb266-934">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="fb266-934">Parameters - widthValue</span></span>

<span data-ttu-id="fb266-935">値</span><span class="sxs-lookup"><span data-stu-id="fb266-935">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="fb266-936">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="fb266-936">Return Value - widthValue</span></span>

<span data-ttu-id="fb266-937">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="fb266-937">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="fb266-938">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="fb266-938">Remarks - widthValue</span></span>

<span data-ttu-id="fb266-939">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="fb266-939">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-show"></a><span data-ttu-id="fb266-940">メソッド show</span><span class="sxs-lookup"><span data-stu-id="fb266-940">Method show</span></span>

```xpp
public void show()
```

## <a name="method-left"></a><span data-ttu-id="fb266-941">メソッド left</span><span class="sxs-lookup"><span data-stu-id="fb266-941">Method left</span></span>

```xpp
public void left(Real value, Units unit)
```

### <a name="parameters---left"></a><span data-ttu-id="fb266-942">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="fb266-942">Parameters - left</span></span>

<span data-ttu-id="fb266-943">値</span><span class="sxs-lookup"><span data-stu-id="fb266-943">value</span></span>  

<!-- -->

<span data-ttu-id="fb266-944">単位</span><span class="sxs-lookup"><span data-stu-id="fb266-944">unit</span></span>  

## <a name="method-width"></a><span data-ttu-id="fb266-945">メソッド width</span><span class="sxs-lookup"><span data-stu-id="fb266-945">Method width</span></span>

<span data-ttu-id="fb266-946">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-946">Gets or sets the width of the control.</span></span>

```xpp
public void width(Real value, Units unit)
```

### <a name="parameters---width"></a><span data-ttu-id="fb266-947">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="fb266-947">Parameters - width</span></span>

<span data-ttu-id="fb266-948">値</span><span class="sxs-lookup"><span data-stu-id="fb266-948">value</span></span>  

<!-- -->

<span data-ttu-id="fb266-949">単位</span><span class="sxs-lookup"><span data-stu-id="fb266-949">unit</span></span>  

### <a name="remarks---width"></a><span data-ttu-id="fb266-950">備考 - width</span><span class="sxs-lookup"><span data-stu-id="fb266-950">Remarks - width</span></span>

<span data-ttu-id="fb266-951">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="fb266-951">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="fb266-952">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="fb266-952">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="fb266-953">モード。</span><span class="sxs-lookup"><span data-stu-id="fb266-953">Mode.</span></span>           | <span data-ttu-id="fb266-954">幅計算。</span><span class="sxs-lookup"><span data-stu-id="fb266-954">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb266-955">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="fb266-955">-1 Exact.</span></span>       | <span data-ttu-id="fb266-956">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="fb266-956">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="fb266-957">0 自動。</span><span class="sxs-lookup"><span data-stu-id="fb266-957">0 Auto.</span></span>         | <span data-ttu-id="fb266-958">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="fb266-958">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="fb266-959">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="fb266-959">1 Column width.</span></span> | <span data-ttu-id="fb266-960">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="fb266-960">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="fb266-961">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="fb266-961">The width and width calculation mode can be set separately.</span></span>

## <a name="method-extrasumwidth"></a><span data-ttu-id="fb266-962">メソッド extraSumWidth</span><span class="sxs-lookup"><span data-stu-id="fb266-962">Method extraSumWidth</span></span>

```xpp
public void extraSumWidth(Real value, Units unit)
```

### <a name="parameters---extrasumwidth"></a><span data-ttu-id="fb266-963">パラメーター - extraSumWidth</span><span class="sxs-lookup"><span data-stu-id="fb266-963">Parameters - extraSumWidth</span></span>

<span data-ttu-id="fb266-964">値</span><span class="sxs-lookup"><span data-stu-id="fb266-964">value</span></span>  

<!-- -->

<span data-ttu-id="fb266-965">単位</span><span class="sxs-lookup"><span data-stu-id="fb266-965">unit</span></span>  

## <a name="method-leftmargin"></a><span data-ttu-id="fb266-966">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="fb266-966">Method leftMargin</span></span>

```xpp
public void leftMargin(Real value, Units unit)
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="fb266-967">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="fb266-967">Parameters - leftMargin</span></span>

<span data-ttu-id="fb266-968">値</span><span class="sxs-lookup"><span data-stu-id="fb266-968">value</span></span>  

<!-- -->

<span data-ttu-id="fb266-969">単位</span><span class="sxs-lookup"><span data-stu-id="fb266-969">unit</span></span>  

## <a name="method-topmargin"></a><span data-ttu-id="fb266-970">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="fb266-970">Method topMargin</span></span>

```xpp
public void topMargin(Real value, Units unit)
```

### <a name="parameters---topmargin"></a><span data-ttu-id="fb266-971">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="fb266-971">Parameters - topMargin</span></span>

<span data-ttu-id="fb266-972">値</span><span class="sxs-lookup"><span data-stu-id="fb266-972">value</span></span>  

<!-- -->

<span data-ttu-id="fb266-973">単位</span><span class="sxs-lookup"><span data-stu-id="fb266-973">unit</span></span>  

## <a name="method-hide"></a><span data-ttu-id="fb266-974">メソッド hide</span><span class="sxs-lookup"><span data-stu-id="fb266-974">Method hide</span></span>

```xpp
public void hide()
```

## <a name="method-bottommargin"></a><span data-ttu-id="fb266-975">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="fb266-975">Method bottomMargin</span></span>

```xpp
public void bottomMargin(Real value, Units unit)
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="fb266-976">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="fb266-976">Parameters - bottomMargin</span></span>

<span data-ttu-id="fb266-977">値</span><span class="sxs-lookup"><span data-stu-id="fb266-977">value</span></span>  

<!-- -->

<span data-ttu-id="fb266-978">単位</span><span class="sxs-lookup"><span data-stu-id="fb266-978">unit</span></span>  

## <a name="method-top"></a><span data-ttu-id="fb266-979">メソッド top</span><span class="sxs-lookup"><span data-stu-id="fb266-979">Method top</span></span>

```xpp
public void top(Real value, Units unit)
```

### <a name="parameters---top"></a><span data-ttu-id="fb266-980">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="fb266-980">Parameters - top</span></span>

<span data-ttu-id="fb266-981">値</span><span class="sxs-lookup"><span data-stu-id="fb266-981">value</span></span>  

<!-- -->

<span data-ttu-id="fb266-982">単位</span><span class="sxs-lookup"><span data-stu-id="fb266-982">unit</span></span>  

## <a name="method-labelwidth"></a><span data-ttu-id="fb266-983">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="fb266-983">Method labelWidth</span></span>

```xpp
public void labelWidth(Real value, Units unit)
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="fb266-984">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="fb266-984">Parameters - labelWidth</span></span>

<span data-ttu-id="fb266-985">値</span><span class="sxs-lookup"><span data-stu-id="fb266-985">value</span></span>  

<!-- -->

<span data-ttu-id="fb266-986">単位</span><span class="sxs-lookup"><span data-stu-id="fb266-986">unit</span></span>  

## <a name="method-rightmargin"></a><span data-ttu-id="fb266-987">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="fb266-987">Method rightMargin</span></span>

```xpp
public void rightMargin(Real value, Units unit)
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="fb266-988">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="fb266-988">Parameters - rightMargin</span></span>

<span data-ttu-id="fb266-989">値</span><span class="sxs-lookup"><span data-stu-id="fb266-989">value</span></span>  

<!-- -->

<span data-ttu-id="fb266-990">単位</span><span class="sxs-lookup"><span data-stu-id="fb266-990">unit</span></span>  

## <a name="method-height"></a><span data-ttu-id="fb266-991">メソッド height</span><span class="sxs-lookup"><span data-stu-id="fb266-991">Method height</span></span>

<span data-ttu-id="fb266-992">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fb266-992">Gets or sets the height of the control.</span></span>

```xpp
public void height(Real value, Units unit)
```

### <a name="parameters---height"></a><span data-ttu-id="fb266-993">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="fb266-993">Parameters - height</span></span>

<span data-ttu-id="fb266-994">値</span><span class="sxs-lookup"><span data-stu-id="fb266-994">value</span></span>  

<!-- -->

<span data-ttu-id="fb266-995">単位</span><span class="sxs-lookup"><span data-stu-id="fb266-995">unit</span></span>  

### <a name="remarks---height"></a><span data-ttu-id="fb266-996">備考 - height</span><span class="sxs-lookup"><span data-stu-id="fb266-996">Remarks - height</span></span>

<span data-ttu-id="fb266-997">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="fb266-997">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="fb266-998">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="fb266-998">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="fb266-999">モード。</span><span class="sxs-lookup"><span data-stu-id="fb266-999">Mode.</span></span>            | <span data-ttu-id="fb266-1000">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="fb266-1000">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb266-1001">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="fb266-1001">-1 Exact.</span></span>        | <span data-ttu-id="fb266-1002">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="fb266-1002">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="fb266-1003">0 自動。</span><span class="sxs-lookup"><span data-stu-id="fb266-1003">0 Auto.</span></span>          | <span data-ttu-id="fb266-1004">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="fb266-1004">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="fb266-1005">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="fb266-1005">1 Column height.</span></span> | <span data-ttu-id="fb266-1006">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="fb266-1006">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="fb266-1007">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="fb266-1007">The height and height calculation mode can be set separately.</span></span>

