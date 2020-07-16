---
title: ReportTextControl クラス
description: このトピックでは、ReportTextControl クラスについて説明します。
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
ms.openlocfilehash: e93d55df921ef4f34074e4ece9e06e11a972019b
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502826"
---
# <a name="class-reporttextcontrol"></a><span data-ttu-id="a0a5a-103">クラス ReportTextControl</span><span class="sxs-lookup"><span data-stu-id="a0a5a-103">Class ReportTextControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ReportTextControl extends ReportControl
```

<span data-ttu-id="a0a5a-104">ReportTextControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-104">The ReportTextControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0a5a-105">備考</span><span class="sxs-lookup"><span data-stu-id="a0a5a-105">Remarks</span></span>

<span data-ttu-id="a0a5a-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="a0a5a-107">例</span><span class="sxs-lookup"><span data-stu-id="a0a5a-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="a0a5a-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="a0a5a-108">Methods</span></span>

| <span data-ttu-id="a0a5a-109">方法</span><span class="sxs-lookup"><span data-stu-id="a0a5a-109">Method</span></span>                                                                   | <span data-ttu-id="a0a5a-110">説明</span><span class="sxs-lookup"><span data-stu-id="a0a5a-110">Description</span></span>                                                                                                                               |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0a5a-111">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-111">public int alignment(\[int value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="a0a5a-112">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-112">public boolean autoDeclaration(\[boolean value\])</span></span>                        | <span data-ttu-id="a0a5a-113">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-113">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                        |
| <span data-ttu-id="a0a5a-114">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-114">public int backgroundColor(\[int value\])</span></span>                                | <span data-ttu-id="a0a5a-115">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-115">Gets or sets the background color of the control.</span></span>                                                                                         |
| <span data-ttu-id="a0a5a-116">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-116">public int backStyle(\[int value\])</span></span>                                      | <span data-ttu-id="a0a5a-117">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-117">Determines whether the control background can be transparent.</span></span>                                                                             |
| <span data-ttu-id="a0a5a-118">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-118">public int bold(\[int value\])</span></span>                                           | <span data-ttu-id="a0a5a-119">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-119">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                               |
| <span data-ttu-id="a0a5a-120">public int bottomMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-120">public int bottomMarginAndFrame()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="a0a5a-121">public int bottomMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-121">public int bottomMarginMode(\[int value\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="a0a5a-122">public str bottomMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-122">public str bottomMarginStr(\[str value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="a0a5a-123">public Units bottomMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-123">public Units bottomMarginUnit(\[Units value\])</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="a0a5a-124">public Real bottomMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-124">public Real bottomMarginValue(\[Real value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="a0a5a-125">public int changeCase(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-125">public int changeCase(\[int value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="a0a5a-126">public int changeLabelCase(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-126">public int changeLabelCase(\[int value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="a0a5a-127">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-127">public int characterSet(\[int value\])</span></span>                                   | <span data-ttu-id="a0a5a-128">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-128">Gets or sets the character set of the font.</span></span>                                                                                               |
| <span data-ttu-id="a0a5a-129">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-129">public int colorScheme(\[int value\])</span></span>                                    | <span data-ttu-id="a0a5a-130">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-130">Gets or sets the color scheme of the control.</span></span>                                                                                             |
| <span data-ttu-id="a0a5a-131">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-131">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="a0a5a-132">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-132">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                       |
| <span data-ttu-id="a0a5a-133">public ReportFieldType controlType()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-133">public ReportFieldType controlType()</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="a0a5a-134">public str cssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-134">public str cssClass(\[str value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="a0a5a-135">public int delete()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-135">public int delete()</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="a0a5a-136">public str effectiveFont()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-136">public str effectiveFont()</span></span>                                               |                                                                                                                                           |
| <span data-ttu-id="a0a5a-137">public str eval()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-137">public str eval()</span></span>                                                        |                                                                                                                                           |
| <span data-ttu-id="a0a5a-138">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-138">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>         |                                                                                                                                           |
| <span data-ttu-id="a0a5a-139">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-139">public str font(\[str value\])</span></span>                                           | <span data-ttu-id="a0a5a-140">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-140">Gets or sets the name of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="a0a5a-141">public str fontInfoPrinter()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-141">public str fontInfoPrinter()</span></span>                                             |                                                                                                                                           |
| <span data-ttu-id="a0a5a-142">public int fontInfoPrinterAscent()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-142">public int fontInfoPrinterAscent()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="a0a5a-143">public int fontInfoPrinterDescent()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-143">public int fontInfoPrinterDescent()</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="a0a5a-144">public int fontInfoPrinterExtLead()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-144">public int fontInfoPrinterExtLead()</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="a0a5a-145">public int fontInfoPrinterHeight()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-145">public int fontInfoPrinterHeight()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="a0a5a-146">public int fontInfoPrinterIntLead()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-146">public int fontInfoPrinterIntLead()</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="a0a5a-147">public str fontInfoScreen()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-147">public str fontInfoScreen()</span></span>                                              |                                                                                                                                           |
| <span data-ttu-id="a0a5a-148">public int fontInfoScreenAscent()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-148">public int fontInfoScreenAscent()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="a0a5a-149">public int fontInfoScreenDescent()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-149">public int fontInfoScreenDescent()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="a0a5a-150">public int fontInfoScreenExtLead()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-150">public int fontInfoScreenExtLead()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="a0a5a-151">public int fontInfoScreenHeight()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-151">public int fontInfoScreenHeight()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="a0a5a-152">public int fontInfoScreenIntLead()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-152">public int fontInfoScreenIntLead()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="a0a5a-153">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-153">public int fontSize(\[int value\])</span></span>                                       | <span data-ttu-id="a0a5a-154">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-154">Gets or sets the size of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="a0a5a-155">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-155">public int foregroundColor(\[int value\])</span></span>                                | <span data-ttu-id="a0a5a-156">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-156">Gets or sets the text color for the control to use.</span></span>                                                                                       |
| <span data-ttu-id="a0a5a-157">public int height100mm(\[int heightExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-157">public int height100mm(\[int heightExclBorder\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="a0a5a-158">public int height100mmInclBorder(\[int heightInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-158">public int height100mmInclBorder(\[int heightInclBorder\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="a0a5a-159">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-159">public int heightMode(\[int value\])</span></span>                                     | <span data-ttu-id="a0a5a-160">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-160">Gets or sets a calculation mode for the height of the control.</span></span>                                                                            |
| <span data-ttu-id="a0a5a-161">public int heightOfWordWrappedString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="a0a5a-161">public int heightOfWordWrappedString100mm(str string)</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="a0a5a-162">public str heightStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-162">public str heightStr(\[str value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="a0a5a-163">public Units heightUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-163">public Units heightUnit(\[Units value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="a0a5a-164">public Real heightValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-164">public Real heightValue(\[Real value\])</span></span>                                  | <span data-ttu-id="a0a5a-165">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-165">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="a0a5a-166">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-166">public boolean italic(\[boolean value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="a0a5a-167">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-167">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="a0a5a-168">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-168">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="a0a5a-169">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-169">public int labelBold(\[int value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="a0a5a-170">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-170">public int labelCharacterSet(\[int value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="a0a5a-171">public str labelCssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-171">public str labelCssClass(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="a0a5a-172">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-172">public str labelFont(\[str value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="a0a5a-173">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-173">public int labelFontSize(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="a0a5a-174">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-174">public boolean labelItalic(\[boolean value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="a0a5a-175">public LineType labelLineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-175">public LineType labelLineBelow(\[LineType value\])</span></span>                       |                                                                                                                                           |
| <span data-ttu-id="a0a5a-176">public LineThickness labelLineThickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-176">public LineThickness labelLineThickness(\[LineThickness value\])</span></span>         |                                                                                                                                           |
| <span data-ttu-id="a0a5a-177">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-177">public int labelPosition(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="a0a5a-178">public int labelTabLeader(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-178">public int labelTabLeader(\[int value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="a0a5a-179">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-179">public boolean labelUnderline(\[boolean value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="a0a5a-180">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-180">public int labelWidthMode(\[int value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="a0a5a-181">public str labelWidthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-181">public str labelWidthStr(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="a0a5a-182">public Units labelWidthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-182">public Units labelWidthUnit(\[Units value\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="a0a5a-183">public Real labelWidthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-183">public Real labelWidthValue(\[Real value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="a0a5a-184">public int left100mm(\[int leftExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-184">public int left100mm(\[int leftExclBorder\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="a0a5a-185">public int left100mmInclBorder(\[int leftInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-185">public int left100mmInclBorder(\[int leftInclBorder\])</span></span>                   |                                                                                                                                           |
| <span data-ttu-id="a0a5a-186">public int leftMarginAnFrame()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-186">public int leftMarginAnFrame()</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="a0a5a-187">public int leftMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-187">public int leftMarginMode(\[int value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="a0a5a-188">public str leftMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-188">public str leftMarginStr(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="a0a5a-189">public Units leftMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-189">public Units leftMarginUnit(\[Units value\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="a0a5a-190">public Real leftMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-190">public Real leftMarginValue(\[Real value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="a0a5a-191">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-191">public int leftMode(\[int value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="a0a5a-192">public str leftStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-192">public str leftStr(\[str value\])</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="a0a5a-193">public Units leftUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-193">public Units leftUnit(\[Units value\])</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="a0a5a-194">public Real leftValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-194">public Real leftValue(\[Real value\])</span></span>                                    |                                                                                                                                           |
| <span data-ttu-id="a0a5a-195">public LineType lineAbove(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-195">public LineType lineAbove(\[LineType value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="a0a5a-196">public LineType lineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-196">public LineType lineBelow(\[LineType value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="a0a5a-197">public LineType lineLeft(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-197">public LineType lineLeft(\[LineType value\])</span></span>                             | <span data-ttu-id="a0a5a-198">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-198">Gets or sets the type of line that is used as the left border of a section.</span></span>                                                               |
| <span data-ttu-id="a0a5a-199">public LineType lineRight(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-199">public LineType lineRight(\[LineType value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="a0a5a-200">public str menuItemLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-200">public str menuItemLabel(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="a0a5a-201">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-201">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="a0a5a-202">public MenuItemType menuItemType(\[MenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-202">public MenuItemType menuItemType(\[MenuItemType value\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="a0a5a-203">public str modelFieldName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-203">public str modelFieldName(\[str value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="a0a5a-204">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-204">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="a0a5a-205">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-205">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="a0a5a-206">public int numberOfLines(int height100mm)</span><span class="sxs-lookup"><span data-stu-id="a0a5a-206">public int numberOfLines(int height100mm)</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="a0a5a-207">public int position(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-207">public int position(\[int value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="a0a5a-208">public str previewInfo(str string)</span><span class="sxs-lookup"><span data-stu-id="a0a5a-208">public str previewInfo(str string)</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="a0a5a-209">public int previewXCompensation100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="a0a5a-209">public int previewXCompensation100mm(str string)</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="a0a5a-210">public int right100mm()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-210">public int right100mm()</span></span>                                                  |                                                                                                                                           |
| <span data-ttu-id="a0a5a-211">public int right100mmInclBorder()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-211">public int right100mmInclBorder()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="a0a5a-212">public int rightMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-212">public int rightMarginAndFrame()</span></span>                                         |                                                                                                                                           |
| <span data-ttu-id="a0a5a-213">public int rightMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-213">public int rightMarginMode(\[int value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="a0a5a-214">public str rightMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-214">public str rightMarginStr(\[str value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="a0a5a-215">public Units rightMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-215">public Units rightMarginUnit(\[Units value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="a0a5a-216">public Real rightMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-216">public Real rightMarginValue(\[Real value\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="a0a5a-217">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-217">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                                           |
| <span data-ttu-id="a0a5a-218">public str setHeightGetText(int lines, str string)</span><span class="sxs-lookup"><span data-stu-id="a0a5a-218">public str setHeightGetText(int lines, str string)</span></span>                       |                                                                                                                                           |
| <span data-ttu-id="a0a5a-219">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-219">public boolean showLabel(\[boolean value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="a0a5a-220">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-220">public str text(\[str value\])</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="a0a5a-221">public int textExtentX100mm()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-221">public int textExtentX100mm()</span></span>                                            |                                                                                                                                           |
| <span data-ttu-id="a0a5a-222">public int textExtentY100mm()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-222">public int textExtentY100mm()</span></span>                                            |                                                                                                                                           |
| <span data-ttu-id="a0a5a-223">public LineThickness thickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-223">public LineThickness thickness(\[LineThickness value\])</span></span>                  |                                                                                                                                           |
| <span data-ttu-id="a0a5a-224">public int top100mm(\[int topExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-224">public int top100mm(\[int topExclBorder\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="a0a5a-225">public int top100mmInclBorder(\[int topInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-225">public int top100mmInclBorder(\[int topInclBorder\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="a0a5a-226">public int topMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-226">public int topMarginAndFrame()</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="a0a5a-227">public int topMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-227">public int topMarginMode(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="a0a5a-228">public str topMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-228">public str topMarginStr(\[str value\])</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="a0a5a-229">public Units topMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-229">public Units topMarginUnit(\[Units value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="a0a5a-230">public Real topMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-230">public Real topMarginValue(\[Real value\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="a0a5a-231">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-231">public int topMode(\[int value\])</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="a0a5a-232">public str topStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-232">public str topStr(\[str value\])</span></span>                                         |                                                                                                                                           |
| <span data-ttu-id="a0a5a-233">public Units topUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-233">public Units topUnit(\[Units value\])</span></span>                                    |                                                                                                                                           |
| <span data-ttu-id="a0a5a-234">public Real topValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-234">public Real topValue(\[Real value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="a0a5a-235">public int typeHeaderPrompt(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-235">public int typeHeaderPrompt(\[int value\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="a0a5a-236">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-236">public boolean underline(\[boolean value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="a0a5a-237">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-237">public boolean visible(\[boolean value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="a0a5a-238">public str webMenuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-238">public str webMenuItemName(\[str value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="a0a5a-239">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-239">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span></span>        |                                                                                                                                           |
| <span data-ttu-id="a0a5a-240">public str webTarget(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-240">public str webTarget(\[str value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="a0a5a-241">public int width100mm(\[int widthExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-241">public int width100mm(\[int widthExclBorder\])</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="a0a5a-242">public int width100mmInclBorder(\[int widthInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-242">public int width100mmInclBorder(\[int widthInclBorder\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="a0a5a-243">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-243">public int widthMode(\[int value\])</span></span>                                      | <span data-ttu-id="a0a5a-244">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-244">Gets or sets the calculation mode of the width of the control.</span></span>                                                                            |
| <span data-ttu-id="a0a5a-245">public int widthOfString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="a0a5a-245">public int widthOfString100mm(str string)</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="a0a5a-246">public str widthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-246">public str widthStr(\[str value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="a0a5a-247">public Units widthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-247">public Units widthUnit(\[Units value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="a0a5a-248">public Real widthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="a0a5a-248">public Real widthValue(\[Real value\])</span></span>                                   | <span data-ttu-id="a0a5a-249">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-249">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="a0a5a-250">public void show()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-250">public void show()</span></span>                                                       |                                                                                                                                           |
| <span data-ttu-id="a0a5a-251">public void topMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="a0a5a-251">public void topMargin(Real value, Units unit)</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="a0a5a-252">public void bottomMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="a0a5a-252">public void bottomMargin(Real value, Units unit)</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="a0a5a-253">public void labelWidth(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="a0a5a-253">public void labelWidth(Real value, Units unit)</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="a0a5a-254">public void top(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="a0a5a-254">public void top(Real value, Units unit)</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="a0a5a-255">public void width(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="a0a5a-255">public void width(Real value, Units unit)</span></span>                                | <span data-ttu-id="a0a5a-256">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-256">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="a0a5a-257">public void leftMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="a0a5a-257">public void leftMargin(Real value, Units unit)</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="a0a5a-258">public void height(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="a0a5a-258">public void height(Real value, Units unit)</span></span>                               | <span data-ttu-id="a0a5a-259">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-259">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="a0a5a-260">public void rightMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="a0a5a-260">public void rightMargin(Real value, Units unit)</span></span>                          |                                                                                                                                           |
| <span data-ttu-id="a0a5a-261">public void left(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="a0a5a-261">public void left(Real value, Units unit)</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="a0a5a-262">public void hide()</span><span class="sxs-lookup"><span data-stu-id="a0a5a-262">public void hide()</span></span>                                                       |                                                                                                                                           |

## <a name="method-alignment"></a><span data-ttu-id="a0a5a-263">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="a0a5a-263">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="a0a5a-264">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="a0a5a-264">Parameters - alignment</span></span>

<span data-ttu-id="a0a5a-265">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-265">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="a0a5a-266">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="a0a5a-266">Return Value - alignment</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="a0a5a-267">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="a0a5a-267">Method autoDeclaration</span></span>

<span data-ttu-id="a0a5a-268">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-268">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="a0a5a-269">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="a0a5a-269">Parameters - autoDeclaration</span></span>

<span data-ttu-id="a0a5a-270">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-270">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="a0a5a-271">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="a0a5a-271">Return Value - autoDeclaration</span></span>

<span data-ttu-id="a0a5a-272">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-272">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="a0a5a-273">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="a0a5a-273">Remarks - autoDeclaration</span></span>

<span data-ttu-id="a0a5a-274">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-274">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="a0a5a-275">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="a0a5a-275">Method backgroundColor</span></span>

<span data-ttu-id="a0a5a-276">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-276">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="a0a5a-277">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="a0a5a-277">Parameters - backgroundColor</span></span>

<span data-ttu-id="a0a5a-278">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-278">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="a0a5a-279">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="a0a5a-279">Return Value - backgroundColor</span></span>

<span data-ttu-id="a0a5a-280">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-280">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="a0a5a-281">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="a0a5a-281">Remarks - backgroundColor</span></span>

<span data-ttu-id="a0a5a-282">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-282">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="a0a5a-283">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-283">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="a0a5a-284">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-284">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="a0a5a-285">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-285">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="a0a5a-286">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-286">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="a0a5a-287">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-287">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="a0a5a-288">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="a0a5a-288">Method backStyle</span></span>

<span data-ttu-id="a0a5a-289">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-289">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="a0a5a-290">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="a0a5a-290">Parameters - backStyle</span></span>

<span data-ttu-id="a0a5a-291">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-291">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="a0a5a-292">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="a0a5a-292">Return Value - backStyle</span></span>

<span data-ttu-id="a0a5a-293">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-293">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="a0a5a-294">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="a0a5a-294">Method bold</span></span>

<span data-ttu-id="a0a5a-295">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-295">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="a0a5a-296">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="a0a5a-296">Parameters - bold</span></span>

<span data-ttu-id="a0a5a-297">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-297">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="a0a5a-298">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="a0a5a-298">Return Value - bold</span></span>

<span data-ttu-id="a0a5a-299">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-299">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="a0a5a-300">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="a0a5a-300">Remarks - bold</span></span>

<span data-ttu-id="a0a5a-301">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-301">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="a0a5a-302">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-302">0 Use the default font weight.</span></span>
-   <span data-ttu-id="a0a5a-303">1 シン。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-303">1 Thin.</span></span>
-   <span data-ttu-id="a0a5a-304">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-304">2 Extra-light.</span></span>
-   <span data-ttu-id="a0a5a-305">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-305">3 Light.</span></span>
-   <span data-ttu-id="a0a5a-306">4 標準。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-306">4 Normal.</span></span>
-   <span data-ttu-id="a0a5a-307">5 中。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-307">5 Medium.</span></span>
-   <span data-ttu-id="a0a5a-308">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-308">6 Semibold.</span></span>
-   <span data-ttu-id="a0a5a-309">7 太字。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-309">7 Bold.</span></span>
-   <span data-ttu-id="a0a5a-310">8 極太。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-310">8 Extra-bold.</span></span>
-   <span data-ttu-id="a0a5a-311">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-311">9 Heavy.</span></span>

## <a name="method-bottommarginandframe"></a><span data-ttu-id="a0a5a-312">メソッド bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="a0a5a-312">Method bottomMarginAndFrame</span></span>

```xpp
public int bottomMarginAndFrame()
```

### <a name="return-value---bottommarginandframe"></a><span data-ttu-id="a0a5a-313">戻り値 - bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="a0a5a-313">Return Value - bottomMarginAndFrame</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="a0a5a-314">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-314">Method bottomMarginMode</span></span>

```xpp
public int bottomMarginMode([int value])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="a0a5a-315">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-315">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="a0a5a-316">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-316">value</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="a0a5a-317">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-317">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginstr"></a><span data-ttu-id="a0a5a-318">メソッド bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-318">Method bottomMarginStr</span></span>

```xpp
public str bottomMarginStr([str value])
```

### <a name="parameters---bottommarginstr"></a><span data-ttu-id="a0a5a-319">パラメーター - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-319">Parameters - bottomMarginStr</span></span>

<span data-ttu-id="a0a5a-320">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-320">value</span></span>  

### <a name="return-value---bottommarginstr"></a><span data-ttu-id="a0a5a-321">戻り値 - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-321">Return Value - bottomMarginStr</span></span>

## <a name="method-bottommarginunit"></a><span data-ttu-id="a0a5a-322">メソッド bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-322">Method bottomMarginUnit</span></span>

```xpp
public Units bottomMarginUnit([Units value])
```

### <a name="parameters---bottommarginunit"></a><span data-ttu-id="a0a5a-323">パラメーター - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-323">Parameters - bottomMarginUnit</span></span>

<span data-ttu-id="a0a5a-324">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-324">value</span></span>  

### <a name="return-value---bottommarginunit"></a><span data-ttu-id="a0a5a-325">戻り値 - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-325">Return Value - bottomMarginUnit</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="a0a5a-326">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-326">Method bottomMarginValue</span></span>

```xpp
public Real bottomMarginValue([Real value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="a0a5a-327">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-327">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="a0a5a-328">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-328">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="a0a5a-329">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-329">Return Value - bottomMarginValue</span></span>

## <a name="method-changecase"></a><span data-ttu-id="a0a5a-330">メソッド changeCase</span><span class="sxs-lookup"><span data-stu-id="a0a5a-330">Method changeCase</span></span>

```xpp
public int changeCase([int value])
```

### <a name="parameters---changecase"></a><span data-ttu-id="a0a5a-331">パラメーター - changeCase</span><span class="sxs-lookup"><span data-stu-id="a0a5a-331">Parameters - changeCase</span></span>

<span data-ttu-id="a0a5a-332">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-332">value</span></span>  

### <a name="return-value---changecase"></a><span data-ttu-id="a0a5a-333">戻り値 - changeCase</span><span class="sxs-lookup"><span data-stu-id="a0a5a-333">Return Value - changeCase</span></span>

## <a name="method-changelabelcase"></a><span data-ttu-id="a0a5a-334">メソッド changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="a0a5a-334">Method changeLabelCase</span></span>

```xpp
public int changeLabelCase([int value])
```

### <a name="parameters---changelabelcase"></a><span data-ttu-id="a0a5a-335">パラメーター - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="a0a5a-335">Parameters - changeLabelCase</span></span>

<span data-ttu-id="a0a5a-336">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-336">value</span></span>  

### <a name="return-value---changelabelcase"></a><span data-ttu-id="a0a5a-337">戻り値 - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="a0a5a-337">Return Value - changeLabelCase</span></span>

## <a name="method-characterset"></a><span data-ttu-id="a0a5a-338">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="a0a5a-338">Method characterSet</span></span>

<span data-ttu-id="a0a5a-339">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-339">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="a0a5a-340">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="a0a5a-340">Parameters - characterSet</span></span>

<span data-ttu-id="a0a5a-341">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-341">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="a0a5a-342">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="a0a5a-342">Return Value - characterSet</span></span>

<span data-ttu-id="a0a5a-343">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-343">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="a0a5a-344">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="a0a5a-344">Remarks - characterSet</span></span>

<span data-ttu-id="a0a5a-345">取得される整数値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-345">The Integer values that are retrieved indicate the character set according to the following table:</span></span>

| <span data-ttu-id="a0a5a-346">値です。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-346">Value.</span></span> | <span data-ttu-id="a0a5a-347">説明。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-347">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="a0a5a-348">0</span><span class="sxs-lookup"><span data-stu-id="a0a5a-348">0</span></span>      | <span data-ttu-id="a0a5a-349">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a0a5a-349">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="a0a5a-350">1</span><span class="sxs-lookup"><span data-stu-id="a0a5a-350">1</span></span>      | <span data-ttu-id="a0a5a-351">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a0a5a-351">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="a0a5a-352">2</span><span class="sxs-lookup"><span data-stu-id="a0a5a-352">2</span></span>      | <span data-ttu-id="a0a5a-353">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a0a5a-353">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="a0a5a-354">77</span><span class="sxs-lookup"><span data-stu-id="a0a5a-354">77</span></span>     | <span data-ttu-id="a0a5a-355">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a0a5a-355">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="a0a5a-356">128</span><span class="sxs-lookup"><span data-stu-id="a0a5a-356">128</span></span>    | <span data-ttu-id="a0a5a-357">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a0a5a-357">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="a0a5a-358">129</span><span class="sxs-lookup"><span data-stu-id="a0a5a-358">129</span></span>    | <span data-ttu-id="a0a5a-359">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a0a5a-359">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="a0a5a-360">134</span><span class="sxs-lookup"><span data-stu-id="a0a5a-360">134</span></span>    | <span data-ttu-id="a0a5a-361">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a0a5a-361">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="a0a5a-362">136</span><span class="sxs-lookup"><span data-stu-id="a0a5a-362">136</span></span>    | <span data-ttu-id="a0a5a-363">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a0a5a-363">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="a0a5a-364">161</span><span class="sxs-lookup"><span data-stu-id="a0a5a-364">161</span></span>    | <span data-ttu-id="a0a5a-365">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a0a5a-365">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="a0a5a-366">162</span><span class="sxs-lookup"><span data-stu-id="a0a5a-366">162</span></span>    | <span data-ttu-id="a0a5a-367">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a0a5a-367">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="a0a5a-368">163</span><span class="sxs-lookup"><span data-stu-id="a0a5a-368">163</span></span>    | <span data-ttu-id="a0a5a-369">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a0a5a-369">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="a0a5a-370">186</span><span class="sxs-lookup"><span data-stu-id="a0a5a-370">186</span></span>    | <span data-ttu-id="a0a5a-371">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a0a5a-371">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="a0a5a-372">204</span><span class="sxs-lookup"><span data-stu-id="a0a5a-372">204</span></span>    | <span data-ttu-id="a0a5a-373">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a0a5a-373">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="a0a5a-374">238</span><span class="sxs-lookup"><span data-stu-id="a0a5a-374">238</span></span>    | <span data-ttu-id="a0a5a-375">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a0a5a-375">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="a0a5a-376">255</span><span class="sxs-lookup"><span data-stu-id="a0a5a-376">255</span></span>    | <span data-ttu-id="a0a5a-377">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a0a5a-377">OEM\_CHARSET</span></span>         |

<span data-ttu-id="a0a5a-378">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-378">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="a0a5a-379">値です。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-379">Value.</span></span> | <span data-ttu-id="a0a5a-380">説明。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-380">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="a0a5a-381">130</span><span class="sxs-lookup"><span data-stu-id="a0a5a-381">130</span></span>    | <span data-ttu-id="a0a5a-382">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a0a5a-382">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="a0a5a-383">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-383">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="a0a5a-384">値です。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-384">Value.</span></span> | <span data-ttu-id="a0a5a-385">説明。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-385">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="a0a5a-386">177</span><span class="sxs-lookup"><span data-stu-id="a0a5a-386">177</span></span>    | <span data-ttu-id="a0a5a-387">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a0a5a-387">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="a0a5a-388">178</span><span class="sxs-lookup"><span data-stu-id="a0a5a-388">178</span></span>    | <span data-ttu-id="a0a5a-389">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a0a5a-389">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="a0a5a-390">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-390">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="a0a5a-391">値です。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-391">Value.</span></span> | <span data-ttu-id="a0a5a-392">説明。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-392">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="a0a5a-393">222</span><span class="sxs-lookup"><span data-stu-id="a0a5a-393">222</span></span>    | <span data-ttu-id="a0a5a-394">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a0a5a-394">THAI\_CHARSET</span></span> |

<span data-ttu-id="a0a5a-395">既定の文字セットは、現在のシステム ロケールに基づく値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-395">The default character set is set to a value that is based on the current system locale.</span></span> <span data-ttu-id="a0a5a-396">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-396">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="a0a5a-397">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-397">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="a0a5a-398">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="a0a5a-398">Method colorScheme</span></span>

<span data-ttu-id="a0a5a-399">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-399">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="a0a5a-400">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="a0a5a-400">Parameters - colorScheme</span></span>

<span data-ttu-id="a0a5a-401">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-401">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="a0a5a-402">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="a0a5a-402">Return Value - colorScheme</span></span>

<span data-ttu-id="a0a5a-403">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-403">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="a0a5a-404">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="a0a5a-404">Remarks - colorScheme</span></span>

<span data-ttu-id="a0a5a-405">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-405">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="a0a5a-406">値です。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-406">Value.</span></span> | <span data-ttu-id="a0a5a-407">スタイル。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-407">Style.</span></span>                 |
|--------|------------------------|
| <span data-ttu-id="a0a5a-408">0</span><span class="sxs-lookup"><span data-stu-id="a0a5a-408">0</span></span>      | <span data-ttu-id="a0a5a-409">既定。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-409">Default.</span></span>               |
| <span data-ttu-id="a0a5a-410">1</span><span class="sxs-lookup"><span data-stu-id="a0a5a-410">1</span></span>      | <span data-ttu-id="a0a5a-411">Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-411">The Windows palette.</span></span>   |
| <span data-ttu-id="a0a5a-412">2</span><span class="sxs-lookup"><span data-stu-id="a0a5a-412">2</span></span>      | <span data-ttu-id="a0a5a-413">真の配色。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-413">The true-color scheme.</span></span> |

## <a name="method-configurationkey"></a><span data-ttu-id="a0a5a-414">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="a0a5a-414">Method configurationKey</span></span>

<span data-ttu-id="a0a5a-415">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-415">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="a0a5a-416">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="a0a5a-416">Parameters - configurationKey</span></span>

<span data-ttu-id="a0a5a-417">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-417">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="a0a5a-418">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="a0a5a-418">Return Value - configurationKey</span></span>

<span data-ttu-id="a0a5a-419">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-419">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="a0a5a-420">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="a0a5a-420">Remarks - configurationKey</span></span>

<span data-ttu-id="a0a5a-421">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-421">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="a0a5a-422">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-422">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-controltype"></a><span data-ttu-id="a0a5a-423">メソッド controlType</span><span class="sxs-lookup"><span data-stu-id="a0a5a-423">Method controlType</span></span>

```xpp
public ReportFieldType controlType()
```

### <a name="return-value---controltype"></a><span data-ttu-id="a0a5a-424">戻り値 - controlType</span><span class="sxs-lookup"><span data-stu-id="a0a5a-424">Return Value - controlType</span></span>

## <a name="method-cssclass"></a><span data-ttu-id="a0a5a-425">メソッド cssClass</span><span class="sxs-lookup"><span data-stu-id="a0a5a-425">Method cssClass</span></span>

```xpp
public str cssClass([str value])
```

### <a name="parameters---cssclass"></a><span data-ttu-id="a0a5a-426">パラメーター - cssClass</span><span class="sxs-lookup"><span data-stu-id="a0a5a-426">Parameters - cssClass</span></span>

<span data-ttu-id="a0a5a-427">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-427">value</span></span>  

### <a name="return-value---cssclass"></a><span data-ttu-id="a0a5a-428">戻り値 - cssClass</span><span class="sxs-lookup"><span data-stu-id="a0a5a-428">Return Value - cssClass</span></span>

## <a name="method-delete"></a><span data-ttu-id="a0a5a-429">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="a0a5a-429">Method delete</span></span>

```xpp
public int delete()
```

### <a name="return-value---delete"></a><span data-ttu-id="a0a5a-430">戻り値 - delete</span><span class="sxs-lookup"><span data-stu-id="a0a5a-430">Return Value - delete</span></span>

## <a name="method-effectivefont"></a><span data-ttu-id="a0a5a-431">メソッド effectiveFont</span><span class="sxs-lookup"><span data-stu-id="a0a5a-431">Method effectiveFont</span></span>

```xpp
public str effectiveFont()
```

### <a name="return-value---effectivefont"></a><span data-ttu-id="a0a5a-432">戻り値 - effectiveFont</span><span class="sxs-lookup"><span data-stu-id="a0a5a-432">Return Value - effectiveFont</span></span>

## <a name="method-eval"></a><span data-ttu-id="a0a5a-433">メソッド eval</span><span class="sxs-lookup"><span data-stu-id="a0a5a-433">Method eval</span></span>

```xpp
public str eval()
```

### <a name="return-value---eval"></a><span data-ttu-id="a0a5a-434">戻り値 - eval</span><span class="sxs-lookup"><span data-stu-id="a0a5a-434">Return Value - eval</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="a0a5a-435">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="a0a5a-435">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="a0a5a-436">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="a0a5a-436">Parameters - extendedDataType</span></span>

<span data-ttu-id="a0a5a-437">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-437">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="a0a5a-438">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="a0a5a-438">Return Value - extendedDataType</span></span>

## <a name="method-font"></a><span data-ttu-id="a0a5a-439">メソッド font</span><span class="sxs-lookup"><span data-stu-id="a0a5a-439">Method font</span></span>

<span data-ttu-id="a0a5a-440">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-440">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="a0a5a-441">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="a0a5a-441">Parameters - font</span></span>

<span data-ttu-id="a0a5a-442">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-442">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="a0a5a-443">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="a0a5a-443">Return Value - font</span></span>

<span data-ttu-id="a0a5a-444">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-444">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontinfoprinter"></a><span data-ttu-id="a0a5a-445">メソッド fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="a0a5a-445">Method fontInfoPrinter</span></span>

```xpp
public str fontInfoPrinter()
```

### <a name="return-value---fontinfoprinter"></a><span data-ttu-id="a0a5a-446">戻り値 - fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="a0a5a-446">Return Value - fontInfoPrinter</span></span>

## <a name="method-fontinfoprinterascent"></a><span data-ttu-id="a0a5a-447">メソッド fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="a0a5a-447">Method fontInfoPrinterAscent</span></span>

```xpp
public int fontInfoPrinterAscent()
```

### <a name="return-value---fontinfoprinterascent"></a><span data-ttu-id="a0a5a-448">戻り値 - fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="a0a5a-448">Return Value - fontInfoPrinterAscent</span></span>

## <a name="method-fontinfoprinterdescent"></a><span data-ttu-id="a0a5a-449">メソッド fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="a0a5a-449">Method fontInfoPrinterDescent</span></span>

```xpp
public int fontInfoPrinterDescent()
```

### <a name="return-value---fontinfoprinterdescent"></a><span data-ttu-id="a0a5a-450">戻り値 - fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="a0a5a-450">Return Value - fontInfoPrinterDescent</span></span>

## <a name="method-fontinfoprinterextlead"></a><span data-ttu-id="a0a5a-451">メソッド fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="a0a5a-451">Method fontInfoPrinterExtLead</span></span>

```xpp
public int fontInfoPrinterExtLead()
```

### <a name="return-value---fontinfoprinterextlead"></a><span data-ttu-id="a0a5a-452">戻り値 - fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="a0a5a-452">Return Value - fontInfoPrinterExtLead</span></span>

## <a name="method-fontinfoprinterheight"></a><span data-ttu-id="a0a5a-453">メソッド fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="a0a5a-453">Method fontInfoPrinterHeight</span></span>

```xpp
public int fontInfoPrinterHeight()
```

### <a name="return-value---fontinfoprinterheight"></a><span data-ttu-id="a0a5a-454">戻り値 - fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="a0a5a-454">Return Value - fontInfoPrinterHeight</span></span>

## <a name="method-fontinfoprinterintlead"></a><span data-ttu-id="a0a5a-455">メソッド fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="a0a5a-455">Method fontInfoPrinterIntLead</span></span>

```xpp
public int fontInfoPrinterIntLead()
```

### <a name="return-value---fontinfoprinterintlead"></a><span data-ttu-id="a0a5a-456">戻り値 - fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="a0a5a-456">Return Value - fontInfoPrinterIntLead</span></span>

## <a name="method-fontinfoscreen"></a><span data-ttu-id="a0a5a-457">メソッド fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="a0a5a-457">Method fontInfoScreen</span></span>

```xpp
public str fontInfoScreen()
```

### <a name="return-value---fontinfoscreen"></a><span data-ttu-id="a0a5a-458">戻り値 - fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="a0a5a-458">Return Value - fontInfoScreen</span></span>

## <a name="method-fontinfoscreenascent"></a><span data-ttu-id="a0a5a-459">メソッド fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="a0a5a-459">Method fontInfoScreenAscent</span></span>

```xpp
public int fontInfoScreenAscent()
```

### <a name="return-value---fontinfoscreenascent"></a><span data-ttu-id="a0a5a-460">戻り値 - fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="a0a5a-460">Return Value - fontInfoScreenAscent</span></span>

## <a name="method-fontinfoscreendescent"></a><span data-ttu-id="a0a5a-461">メソッド fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="a0a5a-461">Method fontInfoScreenDescent</span></span>

```xpp
public int fontInfoScreenDescent()
```

### <a name="return-value---fontinfoscreendescent"></a><span data-ttu-id="a0a5a-462">戻り値 - fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="a0a5a-462">Return Value - fontInfoScreenDescent</span></span>

## <a name="method-fontinfoscreenextlead"></a><span data-ttu-id="a0a5a-463">メソッド fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="a0a5a-463">Method fontInfoScreenExtLead</span></span>

```xpp
public int fontInfoScreenExtLead()
```

### <a name="return-value---fontinfoscreenextlead"></a><span data-ttu-id="a0a5a-464">戻り値 - fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="a0a5a-464">Return Value - fontInfoScreenExtLead</span></span>

## <a name="method-fontinfoscreenheight"></a><span data-ttu-id="a0a5a-465">メソッド fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="a0a5a-465">Method fontInfoScreenHeight</span></span>

```xpp
public int fontInfoScreenHeight()
```

### <a name="return-value---fontinfoscreenheight"></a><span data-ttu-id="a0a5a-466">戻り値 - fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="a0a5a-466">Return Value - fontInfoScreenHeight</span></span>

## <a name="method-fontinfoscreenintlead"></a><span data-ttu-id="a0a5a-467">メソッド fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="a0a5a-467">Method fontInfoScreenIntLead</span></span>

```xpp
public int fontInfoScreenIntLead()
```

### <a name="return-value---fontinfoscreenintlead"></a><span data-ttu-id="a0a5a-468">戻り値 - fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="a0a5a-468">Return Value - fontInfoScreenIntLead</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="a0a5a-469">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="a0a5a-469">Method fontSize</span></span>

<span data-ttu-id="a0a5a-470">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-470">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="a0a5a-471">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="a0a5a-471">Parameters - fontSize</span></span>

<span data-ttu-id="a0a5a-472">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-472">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="a0a5a-473">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="a0a5a-473">Return Value - fontSize</span></span>

<span data-ttu-id="a0a5a-474">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-474">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="a0a5a-475">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="a0a5a-475">Method foregroundColor</span></span>

<span data-ttu-id="a0a5a-476">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-476">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="a0a5a-477">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="a0a5a-477">Parameters - foregroundColor</span></span>

<span data-ttu-id="a0a5a-478">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-478">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="a0a5a-479">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="a0a5a-479">Return Value - foregroundColor</span></span>

<span data-ttu-id="a0a5a-480">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-480">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="a0a5a-481">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="a0a5a-481">Remarks - foregroundColor</span></span>

<span data-ttu-id="a0a5a-482">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-482">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="a0a5a-483">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-483">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="a0a5a-484">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-484">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="a0a5a-485">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-485">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="a0a5a-486">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-486">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="a0a5a-487">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-487">The maximum value for a single byte is 255.</span></span>

## <a name="method-height100mm"></a><span data-ttu-id="a0a5a-488">メソッド height100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-488">Method height100mm</span></span>

```xpp
public int height100mm([int heightExclBorder])
```

### <a name="parameters---height100mm"></a><span data-ttu-id="a0a5a-489">パラメーター - height100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-489">Parameters - height100mm</span></span>

<span data-ttu-id="a0a5a-490">heightExclBorder</span><span class="sxs-lookup"><span data-stu-id="a0a5a-490">heightExclBorder</span></span>  

### <a name="return-value---height100mm"></a><span data-ttu-id="a0a5a-491">戻り値 - height100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-491">Return Value - height100mm</span></span>

## <a name="method-height100mminclborder"></a><span data-ttu-id="a0a5a-492">メソッド height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="a0a5a-492">Method height100mmInclBorder</span></span>

```xpp
public int height100mmInclBorder([int heightInclBorder])
```

### <a name="parameters---height100mminclborder"></a><span data-ttu-id="a0a5a-493">パラメーター - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="a0a5a-493">Parameters - height100mmInclBorder</span></span>

<span data-ttu-id="a0a5a-494">heightInclBorder</span><span class="sxs-lookup"><span data-stu-id="a0a5a-494">heightInclBorder</span></span>  

### <a name="return-value---height100mminclborder"></a><span data-ttu-id="a0a5a-495">戻り値 - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="a0a5a-495">Return Value - height100mmInclBorder</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="a0a5a-496">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-496">Method heightMode</span></span>

<span data-ttu-id="a0a5a-497">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-497">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="a0a5a-498">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-498">Parameters - heightMode</span></span>

<span data-ttu-id="a0a5a-499">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-499">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="a0a5a-500">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-500">Return Value - heightMode</span></span>

<span data-ttu-id="a0a5a-501">計算モード。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-501">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="a0a5a-502">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-502">Remarks - heightMode</span></span>

<span data-ttu-id="a0a5a-503">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="a0a5a-503">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="a0a5a-504">モード。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-504">Mode.</span></span>          | <span data-ttu-id="a0a5a-505">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-505">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0a5a-506">正確。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-506">Exact.</span></span>         | <span data-ttu-id="a0a5a-507">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-507">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="a0a5a-508">自動。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-508">Auto.</span></span>          | <span data-ttu-id="a0a5a-509">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-509">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="a0a5a-510">列の高さ</span><span class="sxs-lookup"><span data-stu-id="a0a5a-510">Column height.</span></span> | <span data-ttu-id="a0a5a-511">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-511">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="a0a5a-512">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-512">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightofwordwrappedstring100mm"></a><span data-ttu-id="a0a5a-513">メソッド heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-513">Method heightOfWordWrappedString100mm</span></span>

```xpp
public int heightOfWordWrappedString100mm(str string)
```

### <a name="parameters---heightofwordwrappedstring100mm"></a><span data-ttu-id="a0a5a-514">パラメーター - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-514">Parameters - heightOfWordWrappedString100mm</span></span>

<span data-ttu-id="a0a5a-515">文字列</span><span class="sxs-lookup"><span data-stu-id="a0a5a-515">string</span></span>  

### <a name="return-value---heightofwordwrappedstring100mm"></a><span data-ttu-id="a0a5a-516">戻り値 - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-516">Return Value - heightOfWordWrappedString100mm</span></span>

## <a name="method-heightstr"></a><span data-ttu-id="a0a5a-517">メソッド heightStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-517">Method heightStr</span></span>

```xpp
public str heightStr([str value])
```

### <a name="parameters---heightstr"></a><span data-ttu-id="a0a5a-518">パラメーター - heightStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-518">Parameters - heightStr</span></span>

<span data-ttu-id="a0a5a-519">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-519">value</span></span>  

### <a name="return-value---heightstr"></a><span data-ttu-id="a0a5a-520">戻り値 - heightStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-520">Return Value - heightStr</span></span>

## <a name="method-heightunit"></a><span data-ttu-id="a0a5a-521">メソッド heightUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-521">Method heightUnit</span></span>

```xpp
public Units heightUnit([Units value])
```

### <a name="parameters---heightunit"></a><span data-ttu-id="a0a5a-522">パラメーター - heightUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-522">Parameters - heightUnit</span></span>

<span data-ttu-id="a0a5a-523">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-523">value</span></span>  

### <a name="return-value---heightunit"></a><span data-ttu-id="a0a5a-524">戻り値 - heightUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-524">Return Value - heightUnit</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="a0a5a-525">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-525">Method heightValue</span></span>

<span data-ttu-id="a0a5a-526">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-526">Gets or sets the height of the control.</span></span>

```xpp
public Real heightValue([Real value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="a0a5a-527">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-527">Parameters - heightValue</span></span>

<span data-ttu-id="a0a5a-528">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-528">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="a0a5a-529">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-529">Return Value - heightValue</span></span>

<span data-ttu-id="a0a5a-530">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-530">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="a0a5a-531">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-531">Remarks - heightValue</span></span>

<span data-ttu-id="a0a5a-532">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-532">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-italic"></a><span data-ttu-id="a0a5a-533">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="a0a5a-533">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="a0a5a-534">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="a0a5a-534">Parameters - italic</span></span>

<span data-ttu-id="a0a5a-535">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-535">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="a0a5a-536">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="a0a5a-536">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="a0a5a-537">メソッド label</span><span class="sxs-lookup"><span data-stu-id="a0a5a-537">Method label</span></span>

<span data-ttu-id="a0a5a-538">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-538">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="a0a5a-539">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="a0a5a-539">Parameters - label</span></span>

<span data-ttu-id="a0a5a-540">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-540">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="a0a5a-541">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="a0a5a-541">Return Value - label</span></span>

<span data-ttu-id="a0a5a-542">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-542">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="a0a5a-543">備考 - label</span><span class="sxs-lookup"><span data-stu-id="a0a5a-543">Remarks - label</span></span>

<span data-ttu-id="a0a5a-544">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-544">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="a0a5a-545">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-545">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="a0a5a-546">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="a0a5a-546">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="a0a5a-547">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="a0a5a-547">Parameters - labelBold</span></span>

<span data-ttu-id="a0a5a-548">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-548">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="a0a5a-549">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="a0a5a-549">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="a0a5a-550">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="a0a5a-550">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="a0a5a-551">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="a0a5a-551">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="a0a5a-552">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-552">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="a0a5a-553">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="a0a5a-553">Return Value - labelCharacterSet</span></span>

## <a name="method-labelcssclass"></a><span data-ttu-id="a0a5a-554">メソッド labelCssClass</span><span class="sxs-lookup"><span data-stu-id="a0a5a-554">Method labelCssClass</span></span>

```xpp
public str labelCssClass([str value])
```

### <a name="parameters---labelcssclass"></a><span data-ttu-id="a0a5a-555">パラメーター - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="a0a5a-555">Parameters - labelCssClass</span></span>

<span data-ttu-id="a0a5a-556">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-556">value</span></span>  

### <a name="return-value---labelcssclass"></a><span data-ttu-id="a0a5a-557">戻り値 - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="a0a5a-557">Return Value - labelCssClass</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="a0a5a-558">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="a0a5a-558">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="a0a5a-559">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="a0a5a-559">Parameters - labelFont</span></span>

<span data-ttu-id="a0a5a-560">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-560">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="a0a5a-561">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="a0a5a-561">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="a0a5a-562">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="a0a5a-562">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="a0a5a-563">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="a0a5a-563">Parameters - labelFontSize</span></span>

<span data-ttu-id="a0a5a-564">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-564">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="a0a5a-565">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="a0a5a-565">Return Value - labelFontSize</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="a0a5a-566">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="a0a5a-566">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="a0a5a-567">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="a0a5a-567">Parameters - labelItalic</span></span>

<span data-ttu-id="a0a5a-568">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-568">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="a0a5a-569">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="a0a5a-569">Return Value - labelItalic</span></span>

## <a name="method-labellinebelow"></a><span data-ttu-id="a0a5a-570">メソッド labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="a0a5a-570">Method labelLineBelow</span></span>

```xpp
public LineType labelLineBelow([LineType value])
```

### <a name="parameters---labellinebelow"></a><span data-ttu-id="a0a5a-571">パラメーター - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="a0a5a-571">Parameters - labelLineBelow</span></span>

<span data-ttu-id="a0a5a-572">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-572">value</span></span>  

### <a name="return-value---labellinebelow"></a><span data-ttu-id="a0a5a-573">戻り値 - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="a0a5a-573">Return Value - labelLineBelow</span></span>

## <a name="method-labellinethickness"></a><span data-ttu-id="a0a5a-574">メソッド labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="a0a5a-574">Method labelLineThickness</span></span>

```xpp
public LineThickness labelLineThickness([LineThickness value])
```

### <a name="parameters---labellinethickness"></a><span data-ttu-id="a0a5a-575">パラメーター - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="a0a5a-575">Parameters - labelLineThickness</span></span>

<span data-ttu-id="a0a5a-576">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-576">value</span></span>  

### <a name="return-value---labellinethickness"></a><span data-ttu-id="a0a5a-577">戻り値 - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="a0a5a-577">Return Value - labelLineThickness</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="a0a5a-578">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="a0a5a-578">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="a0a5a-579">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="a0a5a-579">Parameters - labelPosition</span></span>

<span data-ttu-id="a0a5a-580">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-580">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="a0a5a-581">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="a0a5a-581">Return Value - labelPosition</span></span>

## <a name="method-labeltableader"></a><span data-ttu-id="a0a5a-582">メソッド labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="a0a5a-582">Method labelTabLeader</span></span>

```xpp
public int labelTabLeader([int value])
```

### <a name="parameters---labeltableader"></a><span data-ttu-id="a0a5a-583">パラメーター - labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="a0a5a-583">Parameters - labelTabLeader</span></span>

<span data-ttu-id="a0a5a-584">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-584">value</span></span>  

### <a name="return-value---labeltableader"></a><span data-ttu-id="a0a5a-585">戻り値 - labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="a0a5a-585">Return Value - labelTabLeader</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="a0a5a-586">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="a0a5a-586">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="a0a5a-587">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="a0a5a-587">Parameters - labelUnderline</span></span>

<span data-ttu-id="a0a5a-588">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-588">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="a0a5a-589">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="a0a5a-589">Return Value - labelUnderline</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="a0a5a-590">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-590">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="a0a5a-591">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-591">Parameters - labelWidthMode</span></span>

<span data-ttu-id="a0a5a-592">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-592">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="a0a5a-593">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-593">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthstr"></a><span data-ttu-id="a0a5a-594">メソッド labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-594">Method labelWidthStr</span></span>

```xpp
public str labelWidthStr([str value])
```

### <a name="parameters---labelwidthstr"></a><span data-ttu-id="a0a5a-595">パラメーター - labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-595">Parameters - labelWidthStr</span></span>

<span data-ttu-id="a0a5a-596">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-596">value</span></span>  

### <a name="return-value---labelwidthstr"></a><span data-ttu-id="a0a5a-597">戻り値 - labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-597">Return Value - labelWidthStr</span></span>

## <a name="method-labelwidthunit"></a><span data-ttu-id="a0a5a-598">メソッド labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-598">Method labelWidthUnit</span></span>

```xpp
public Units labelWidthUnit([Units value])
```

### <a name="parameters---labelwidthunit"></a><span data-ttu-id="a0a5a-599">パラメーター - labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-599">Parameters - labelWidthUnit</span></span>

<span data-ttu-id="a0a5a-600">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-600">value</span></span>  

### <a name="return-value---labelwidthunit"></a><span data-ttu-id="a0a5a-601">戻り値 - labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-601">Return Value - labelWidthUnit</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="a0a5a-602">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-602">Method labelWidthValue</span></span>

```xpp
public Real labelWidthValue([Real value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="a0a5a-603">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-603">Parameters - labelWidthValue</span></span>

<span data-ttu-id="a0a5a-604">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-604">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="a0a5a-605">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-605">Return Value - labelWidthValue</span></span>

## <a name="method-left100mm"></a><span data-ttu-id="a0a5a-606">メソッド left100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-606">Method left100mm</span></span>

```xpp
public int left100mm([int leftExclBorder])
```

### <a name="parameters---left100mm"></a><span data-ttu-id="a0a5a-607">パラメーター - left100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-607">Parameters - left100mm</span></span>

<span data-ttu-id="a0a5a-608">leftExclBorder</span><span class="sxs-lookup"><span data-stu-id="a0a5a-608">leftExclBorder</span></span>  

### <a name="return-value---left100mm"></a><span data-ttu-id="a0a5a-609">戻り値 - left100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-609">Return Value - left100mm</span></span>

## <a name="method-left100mminclborder"></a><span data-ttu-id="a0a5a-610">メソッド left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="a0a5a-610">Method left100mmInclBorder</span></span>

```xpp
public int left100mmInclBorder([int leftInclBorder])
```

### <a name="parameters---left100mminclborder"></a><span data-ttu-id="a0a5a-611">パラメーター - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="a0a5a-611">Parameters - left100mmInclBorder</span></span>

<span data-ttu-id="a0a5a-612">leftInclBorder</span><span class="sxs-lookup"><span data-stu-id="a0a5a-612">leftInclBorder</span></span>  

### <a name="return-value---left100mminclborder"></a><span data-ttu-id="a0a5a-613">戻り値 - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="a0a5a-613">Return Value - left100mmInclBorder</span></span>

## <a name="method-leftmarginanframe"></a><span data-ttu-id="a0a5a-614">メソッド leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="a0a5a-614">Method leftMarginAnFrame</span></span>

```xpp
public int leftMarginAnFrame()
```

### <a name="return-value---leftmarginanframe"></a><span data-ttu-id="a0a5a-615">戻り値 - leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="a0a5a-615">Return Value - leftMarginAnFrame</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="a0a5a-616">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-616">Method leftMarginMode</span></span>

```xpp
public int leftMarginMode([int value])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="a0a5a-617">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-617">Parameters - leftMarginMode</span></span>

<span data-ttu-id="a0a5a-618">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-618">value</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="a0a5a-619">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-619">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginstr"></a><span data-ttu-id="a0a5a-620">メソッド leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-620">Method leftMarginStr</span></span>

```xpp
public str leftMarginStr([str value])
```

### <a name="parameters---leftmarginstr"></a><span data-ttu-id="a0a5a-621">パラメーター - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-621">Parameters - leftMarginStr</span></span>

<span data-ttu-id="a0a5a-622">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-622">value</span></span>  

### <a name="return-value---leftmarginstr"></a><span data-ttu-id="a0a5a-623">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-623">Return Value - leftMarginStr</span></span>

## <a name="method-leftmarginunit"></a><span data-ttu-id="a0a5a-624">メソッド leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-624">Method leftMarginUnit</span></span>

```xpp
public Units leftMarginUnit([Units value])
```

### <a name="parameters---leftmarginunit"></a><span data-ttu-id="a0a5a-625">パラメーター - leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-625">Parameters - leftMarginUnit</span></span>

<span data-ttu-id="a0a5a-626">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-626">value</span></span>  

### <a name="return-value---leftmarginunit"></a><span data-ttu-id="a0a5a-627">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-627">Return Value - leftMarginUnit</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="a0a5a-628">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-628">Method leftMarginValue</span></span>

```xpp
public Real leftMarginValue([Real value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="a0a5a-629">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-629">Parameters - leftMarginValue</span></span>

<span data-ttu-id="a0a5a-630">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-630">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="a0a5a-631">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-631">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="a0a5a-632">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-632">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="a0a5a-633">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-633">Parameters - leftMode</span></span>

<span data-ttu-id="a0a5a-634">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-634">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="a0a5a-635">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-635">Return Value - leftMode</span></span>

## <a name="method-leftstr"></a><span data-ttu-id="a0a5a-636">メソッド leftStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-636">Method leftStr</span></span>

```xpp
public str leftStr([str value])
```

### <a name="parameters---leftstr"></a><span data-ttu-id="a0a5a-637">パラメーター - leftStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-637">Parameters - leftStr</span></span>

<span data-ttu-id="a0a5a-638">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-638">value</span></span>  

### <a name="return-value---leftstr"></a><span data-ttu-id="a0a5a-639">戻り値 - leftStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-639">Return Value - leftStr</span></span>

## <a name="method-leftunit"></a><span data-ttu-id="a0a5a-640">メソッド leftUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-640">Method leftUnit</span></span>

```xpp
public Units leftUnit([Units value])
```

### <a name="parameters---leftunit"></a><span data-ttu-id="a0a5a-641">パラメーター - leftUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-641">Parameters - leftUnit</span></span>

<span data-ttu-id="a0a5a-642">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-642">value</span></span>  

### <a name="return-value---leftunit"></a><span data-ttu-id="a0a5a-643">戻り値 - leftUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-643">Return Value - leftUnit</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="a0a5a-644">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-644">Method leftValue</span></span>

```xpp
public Real leftValue([Real value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="a0a5a-645">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-645">Parameters - leftValue</span></span>

<span data-ttu-id="a0a5a-646">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-646">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="a0a5a-647">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-647">Return Value - leftValue</span></span>

## <a name="method-lineabove"></a><span data-ttu-id="a0a5a-648">メソッド lineAbove</span><span class="sxs-lookup"><span data-stu-id="a0a5a-648">Method lineAbove</span></span>

```xpp
public LineType lineAbove([LineType value])
```

### <a name="parameters---lineabove"></a><span data-ttu-id="a0a5a-649">パラメーター - lineAbove</span><span class="sxs-lookup"><span data-stu-id="a0a5a-649">Parameters - lineAbove</span></span>

<span data-ttu-id="a0a5a-650">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-650">value</span></span>  

### <a name="return-value---lineabove"></a><span data-ttu-id="a0a5a-651">戻り値 - lineAbove</span><span class="sxs-lookup"><span data-stu-id="a0a5a-651">Return Value - lineAbove</span></span>

## <a name="method-linebelow"></a><span data-ttu-id="a0a5a-652">メソッド lineBelow</span><span class="sxs-lookup"><span data-stu-id="a0a5a-652">Method lineBelow</span></span>

```xpp
public LineType lineBelow([LineType value])
```

### <a name="parameters---linebelow"></a><span data-ttu-id="a0a5a-653">パラメーター - lineBelow</span><span class="sxs-lookup"><span data-stu-id="a0a5a-653">Parameters - lineBelow</span></span>

<span data-ttu-id="a0a5a-654">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-654">value</span></span>  

### <a name="return-value---linebelow"></a><span data-ttu-id="a0a5a-655">戻り値 - lineBelow</span><span class="sxs-lookup"><span data-stu-id="a0a5a-655">Return Value - lineBelow</span></span>

## <a name="method-lineleft"></a><span data-ttu-id="a0a5a-656">メソッド lineLeft</span><span class="sxs-lookup"><span data-stu-id="a0a5a-656">Method lineLeft</span></span>

<span data-ttu-id="a0a5a-657">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-657">Gets or sets the type of line that is used as the left border of a section.</span></span>

```xpp
public LineType lineLeft([LineType value])
```

### <a name="parameters---lineleft"></a><span data-ttu-id="a0a5a-658">パラメーター - lineLeft</span><span class="sxs-lookup"><span data-stu-id="a0a5a-658">Parameters - lineLeft</span></span>

<span data-ttu-id="a0a5a-659">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-659">value</span></span>  

### <a name="return-value---lineleft"></a><span data-ttu-id="a0a5a-660">戻り値 - lineLeft</span><span class="sxs-lookup"><span data-stu-id="a0a5a-660">Return Value - lineLeft</span></span>

<span data-ttu-id="a0a5a-661">左境界線として使用される線のタイプ。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-661">The type of line that is used as the left border.</span></span>

## <a name="method-lineright"></a><span data-ttu-id="a0a5a-662">メソッド lineRight</span><span class="sxs-lookup"><span data-stu-id="a0a5a-662">Method lineRight</span></span>

```xpp
public LineType lineRight([LineType value])
```

### <a name="parameters---lineright"></a><span data-ttu-id="a0a5a-663">パラメーター - lineRight</span><span class="sxs-lookup"><span data-stu-id="a0a5a-663">Parameters - lineRight</span></span>

<span data-ttu-id="a0a5a-664">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-664">value</span></span>  

### <a name="return-value---lineright"></a><span data-ttu-id="a0a5a-665">戻り値 - lineRight</span><span class="sxs-lookup"><span data-stu-id="a0a5a-665">Return Value - lineRight</span></span>

## <a name="method-menuitemlabel"></a><span data-ttu-id="a0a5a-666">メソッド menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="a0a5a-666">Method menuItemLabel</span></span>

```xpp
public str menuItemLabel([str value])
```

### <a name="parameters---menuitemlabel"></a><span data-ttu-id="a0a5a-667">パラメーター - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="a0a5a-667">Parameters - menuItemLabel</span></span>

<span data-ttu-id="a0a5a-668">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-668">value</span></span>  

### <a name="return-value---menuitemlabel"></a><span data-ttu-id="a0a5a-669">戻り値 - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="a0a5a-669">Return Value - menuItemLabel</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="a0a5a-670">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="a0a5a-670">Method menuItemName</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="a0a5a-671">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="a0a5a-671">Parameters - menuItemName</span></span>

<span data-ttu-id="a0a5a-672">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-672">value</span></span>  

### <a name="return-value---menuitemname"></a><span data-ttu-id="a0a5a-673">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="a0a5a-673">Return Value - menuItemName</span></span>

## <a name="method-menuitemtype"></a><span data-ttu-id="a0a5a-674">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="a0a5a-674">Method menuItemType</span></span>

```xpp
public MenuItemType menuItemType([MenuItemType value])
```

### <a name="parameters---menuitemtype"></a><span data-ttu-id="a0a5a-675">パラメーター - menuItemType</span><span class="sxs-lookup"><span data-stu-id="a0a5a-675">Parameters - menuItemType</span></span>

<span data-ttu-id="a0a5a-676">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-676">value</span></span>  

### <a name="return-value---menuitemtype"></a><span data-ttu-id="a0a5a-677">戻り値 - menuItemType</span><span class="sxs-lookup"><span data-stu-id="a0a5a-677">Return Value - menuItemType</span></span>

## <a name="method-modelfieldname"></a><span data-ttu-id="a0a5a-678">メソッド modelFieldName</span><span class="sxs-lookup"><span data-stu-id="a0a5a-678">Method modelFieldName</span></span>

```xpp
public str modelFieldName([str value])
```

### <a name="parameters---modelfieldname"></a><span data-ttu-id="a0a5a-679">パラメーター - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="a0a5a-679">Parameters - modelFieldName</span></span>

<span data-ttu-id="a0a5a-680">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-680">value</span></span>  

### <a name="return-value---modelfieldname"></a><span data-ttu-id="a0a5a-681">戻り値 - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="a0a5a-681">Return Value - modelFieldName</span></span>

## <a name="method-name"></a><span data-ttu-id="a0a5a-682">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a0a5a-682">Method name</span></span>

<span data-ttu-id="a0a5a-683">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-683">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="a0a5a-684">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="a0a5a-684">Parameters - name</span></span>

<span data-ttu-id="a0a5a-685">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-685">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="a0a5a-686">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="a0a5a-686">Return Value - name</span></span>

<span data-ttu-id="a0a5a-687">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-687">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="a0a5a-688">備考 - name</span><span class="sxs-lookup"><span data-stu-id="a0a5a-688">Remarks - name</span></span>

<span data-ttu-id="a0a5a-689">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-689">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="a0a5a-690">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-690">Begins with a letter.</span></span>
-   <span data-ttu-id="a0a5a-691">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-691">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="a0a5a-692">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-692">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="a0a5a-693">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-693">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="a0a5a-694">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-694">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-numberoflines"></a><span data-ttu-id="a0a5a-695">メソッド numberOfLines</span><span class="sxs-lookup"><span data-stu-id="a0a5a-695">Method numberOfLines</span></span>

```xpp
public int numberOfLines(int height100mm)
```

### <a name="parameters---numberoflines"></a><span data-ttu-id="a0a5a-696">パラメーター - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="a0a5a-696">Parameters - numberOfLines</span></span>

<span data-ttu-id="a0a5a-697">height100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-697">height100mm</span></span>  

### <a name="return-value---numberoflines"></a><span data-ttu-id="a0a5a-698">戻り値 - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="a0a5a-698">Return Value - numberOfLines</span></span>

## <a name="method-position"></a><span data-ttu-id="a0a5a-699">メソッドの位置</span><span class="sxs-lookup"><span data-stu-id="a0a5a-699">Method position</span></span>

```xpp
public int position([int value])
```

### <a name="parameters---position"></a><span data-ttu-id="a0a5a-700">パラメーター - position</span><span class="sxs-lookup"><span data-stu-id="a0a5a-700">Parameters - position</span></span>

<span data-ttu-id="a0a5a-701">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-701">value</span></span>  

### <a name="return-value---position"></a><span data-ttu-id="a0a5a-702">戻り値 - position</span><span class="sxs-lookup"><span data-stu-id="a0a5a-702">Return Value - position</span></span>

## <a name="method-previewinfo"></a><span data-ttu-id="a0a5a-703">メソッド previewInfo</span><span class="sxs-lookup"><span data-stu-id="a0a5a-703">Method previewInfo</span></span>

```xpp
public str previewInfo(str string)
```

### <a name="parameters---previewinfo"></a><span data-ttu-id="a0a5a-704">パラメーター - previewInfo</span><span class="sxs-lookup"><span data-stu-id="a0a5a-704">Parameters - previewInfo</span></span>

<span data-ttu-id="a0a5a-705">文字列</span><span class="sxs-lookup"><span data-stu-id="a0a5a-705">string</span></span>  

### <a name="return-value---previewinfo"></a><span data-ttu-id="a0a5a-706">戻り値 - previewInfo</span><span class="sxs-lookup"><span data-stu-id="a0a5a-706">Return Value - previewInfo</span></span>

## <a name="method-previewxcompensation100mm"></a><span data-ttu-id="a0a5a-707">メソッド previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-707">Method previewXCompensation100mm</span></span>

```xpp
public int previewXCompensation100mm(str string)
```

### <a name="parameters---previewxcompensation100mm"></a><span data-ttu-id="a0a5a-708">パラメーター - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-708">Parameters - previewXCompensation100mm</span></span>

<span data-ttu-id="a0a5a-709">文字列</span><span class="sxs-lookup"><span data-stu-id="a0a5a-709">string</span></span>  

### <a name="return-value---previewxcompensation100mm"></a><span data-ttu-id="a0a5a-710">戻り値 - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-710">Return Value - previewXCompensation100mm</span></span>

## <a name="method-right100mm"></a><span data-ttu-id="a0a5a-711">メソッド right100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-711">Method right100mm</span></span>

```xpp
public int right100mm()
```

### <a name="return-value---right100mm"></a><span data-ttu-id="a0a5a-712">戻り値 - right100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-712">Return Value - right100mm</span></span>

## <a name="method-right100mminclborder"></a><span data-ttu-id="a0a5a-713">メソッド right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="a0a5a-713">Method right100mmInclBorder</span></span>

```xpp
public int right100mmInclBorder()
```

### <a name="return-value---right100mminclborder"></a><span data-ttu-id="a0a5a-714">戻り値 - right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="a0a5a-714">Return Value - right100mmInclBorder</span></span>

## <a name="method-rightmarginandframe"></a><span data-ttu-id="a0a5a-715">メソッド rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="a0a5a-715">Method rightMarginAndFrame</span></span>

```xpp
public int rightMarginAndFrame()
```

### <a name="return-value---rightmarginandframe"></a><span data-ttu-id="a0a5a-716">戻り値 - rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="a0a5a-716">Return Value - rightMarginAndFrame</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="a0a5a-717">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-717">Method rightMarginMode</span></span>

```xpp
public int rightMarginMode([int value])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="a0a5a-718">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-718">Parameters - rightMarginMode</span></span>

<span data-ttu-id="a0a5a-719">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-719">value</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="a0a5a-720">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-720">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginstr"></a><span data-ttu-id="a0a5a-721">メソッド rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-721">Method rightMarginStr</span></span>

```xpp
public str rightMarginStr([str value])
```

### <a name="parameters---rightmarginstr"></a><span data-ttu-id="a0a5a-722">パラメーター - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-722">Parameters - rightMarginStr</span></span>

<span data-ttu-id="a0a5a-723">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-723">value</span></span>  

### <a name="return-value---rightmarginstr"></a><span data-ttu-id="a0a5a-724">戻り値 - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-724">Return Value - rightMarginStr</span></span>

## <a name="method-rightmarginunit"></a><span data-ttu-id="a0a5a-725">メソッド rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-725">Method rightMarginUnit</span></span>

```xpp
public Units rightMarginUnit([Units value])
```

### <a name="parameters---rightmarginunit"></a><span data-ttu-id="a0a5a-726">パラメーター - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-726">Parameters - rightMarginUnit</span></span>

<span data-ttu-id="a0a5a-727">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-727">value</span></span>  

### <a name="return-value---rightmarginunit"></a><span data-ttu-id="a0a5a-728">戻り値 - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-728">Return Value - rightMarginUnit</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="a0a5a-729">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-729">Method rightMarginValue</span></span>

```xpp
public Real rightMarginValue([Real value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="a0a5a-730">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-730">Parameters - rightMarginValue</span></span>

<span data-ttu-id="a0a5a-731">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-731">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="a0a5a-732">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-732">Return Value - rightMarginValue</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="a0a5a-733">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="a0a5a-733">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="a0a5a-734">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="a0a5a-734">Parameters - securityKey</span></span>

<span data-ttu-id="a0a5a-735">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-735">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="a0a5a-736">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="a0a5a-736">Return Value - securityKey</span></span>

## <a name="method-setheightgettext"></a><span data-ttu-id="a0a5a-737">メソッド setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="a0a5a-737">Method setHeightGetText</span></span>

```xpp
public str setHeightGetText(int lines, str string)
```

### <a name="parameters---setheightgettext"></a><span data-ttu-id="a0a5a-738">パラメーター - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="a0a5a-738">Parameters - setHeightGetText</span></span>

<span data-ttu-id="a0a5a-739">明細行</span><span class="sxs-lookup"><span data-stu-id="a0a5a-739">lines</span></span>  

<!-- -->

<span data-ttu-id="a0a5a-740">文字列</span><span class="sxs-lookup"><span data-stu-id="a0a5a-740">string</span></span>  

### <a name="return-value---setheightgettext"></a><span data-ttu-id="a0a5a-741">戻り値 - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="a0a5a-741">Return Value - setHeightGetText</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="a0a5a-742">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="a0a5a-742">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="a0a5a-743">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="a0a5a-743">Parameters - showLabel</span></span>

<span data-ttu-id="a0a5a-744">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-744">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="a0a5a-745">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="a0a5a-745">Return Value - showLabel</span></span>

## <a name="method-text"></a><span data-ttu-id="a0a5a-746">メソッド text</span><span class="sxs-lookup"><span data-stu-id="a0a5a-746">Method text</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="a0a5a-747">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="a0a5a-747">Parameters - text</span></span>

<span data-ttu-id="a0a5a-748">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-748">value</span></span>  

### <a name="return-value---text"></a><span data-ttu-id="a0a5a-749">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="a0a5a-749">Return Value - text</span></span>

## <a name="method-textextentx100mm"></a><span data-ttu-id="a0a5a-750">メソッド textExtentX100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-750">Method textExtentX100mm</span></span>

```xpp
public int textExtentX100mm()
```

### <a name="return-value---textextentx100mm"></a><span data-ttu-id="a0a5a-751">戻り値 - textExtentX100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-751">Return Value - textExtentX100mm</span></span>

## <a name="method-textextenty100mm"></a><span data-ttu-id="a0a5a-752">メソッド textExtentY100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-752">Method textExtentY100mm</span></span>

```xpp
public int textExtentY100mm()
```

### <a name="return-value---textextenty100mm"></a><span data-ttu-id="a0a5a-753">戻り値 - textExtentY100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-753">Return Value - textExtentY100mm</span></span>

## <a name="method-thickness"></a><span data-ttu-id="a0a5a-754">メソッド thickness</span><span class="sxs-lookup"><span data-stu-id="a0a5a-754">Method thickness</span></span>

```xpp
public LineThickness thickness([LineThickness value])
```

### <a name="parameters---thickness"></a><span data-ttu-id="a0a5a-755">パラメーター - thickness</span><span class="sxs-lookup"><span data-stu-id="a0a5a-755">Parameters - thickness</span></span>

<span data-ttu-id="a0a5a-756">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-756">value</span></span>  

### <a name="return-value---thickness"></a><span data-ttu-id="a0a5a-757">戻り値 - thickness</span><span class="sxs-lookup"><span data-stu-id="a0a5a-757">Return Value - thickness</span></span>

## <a name="method-top100mm"></a><span data-ttu-id="a0a5a-758">メソッド top100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-758">Method top100mm</span></span>

```xpp
public int top100mm([int topExclBorder])
```

### <a name="parameters---top100mm"></a><span data-ttu-id="a0a5a-759">パラメーター - top100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-759">Parameters - top100mm</span></span>

<span data-ttu-id="a0a5a-760">topExclBorder</span><span class="sxs-lookup"><span data-stu-id="a0a5a-760">topExclBorder</span></span>  

### <a name="return-value---top100mm"></a><span data-ttu-id="a0a5a-761">戻り値 - top100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-761">Return Value - top100mm</span></span>

## <a name="method-top100mminclborder"></a><span data-ttu-id="a0a5a-762">メソッド top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="a0a5a-762">Method top100mmInclBorder</span></span>

```xpp
public int top100mmInclBorder([int topInclBorder])
```

### <a name="parameters---top100mminclborder"></a><span data-ttu-id="a0a5a-763">パラメーター - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="a0a5a-763">Parameters - top100mmInclBorder</span></span>

<span data-ttu-id="a0a5a-764">topInclBorder</span><span class="sxs-lookup"><span data-stu-id="a0a5a-764">topInclBorder</span></span>  

### <a name="return-value---top100mminclborder"></a><span data-ttu-id="a0a5a-765">戻り値 - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="a0a5a-765">Return Value - top100mmInclBorder</span></span>

## <a name="method-topmarginandframe"></a><span data-ttu-id="a0a5a-766">メソッド topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="a0a5a-766">Method topMarginAndFrame</span></span>

```xpp
public int topMarginAndFrame()
```

### <a name="return-value---topmarginandframe"></a><span data-ttu-id="a0a5a-767">戻り値 - topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="a0a5a-767">Return Value - topMarginAndFrame</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="a0a5a-768">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-768">Method topMarginMode</span></span>

```xpp
public int topMarginMode([int value])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="a0a5a-769">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-769">Parameters - topMarginMode</span></span>

<span data-ttu-id="a0a5a-770">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-770">value</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="a0a5a-771">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-771">Return Value - topMarginMode</span></span>

## <a name="method-topmarginstr"></a><span data-ttu-id="a0a5a-772">メソッド topMarginStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-772">Method topMarginStr</span></span>

```xpp
public str topMarginStr([str value])
```

### <a name="parameters---topmarginstr"></a><span data-ttu-id="a0a5a-773">パラメーター - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-773">Parameters - topMarginStr</span></span>

<span data-ttu-id="a0a5a-774">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-774">value</span></span>  

### <a name="return-value---topmarginstr"></a><span data-ttu-id="a0a5a-775">戻り値 - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-775">Return Value - topMarginStr</span></span>

## <a name="method-topmarginunit"></a><span data-ttu-id="a0a5a-776">メソッド topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-776">Method topMarginUnit</span></span>

```xpp
public Units topMarginUnit([Units value])
```

### <a name="parameters---topmarginunit"></a><span data-ttu-id="a0a5a-777">パラメーター - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-777">Parameters - topMarginUnit</span></span>

<span data-ttu-id="a0a5a-778">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-778">value</span></span>  

### <a name="return-value---topmarginunit"></a><span data-ttu-id="a0a5a-779">戻り値 - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-779">Return Value - topMarginUnit</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="a0a5a-780">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-780">Method topMarginValue</span></span>

```xpp
public Real topMarginValue([Real value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="a0a5a-781">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-781">Parameters - topMarginValue</span></span>

<span data-ttu-id="a0a5a-782">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-782">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="a0a5a-783">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-783">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="a0a5a-784">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-784">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="a0a5a-785">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-785">Parameters - topMode</span></span>

<span data-ttu-id="a0a5a-786">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-786">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="a0a5a-787">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-787">Return Value - topMode</span></span>

## <a name="method-topstr"></a><span data-ttu-id="a0a5a-788">メソッド topStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-788">Method topStr</span></span>

```xpp
public str topStr([str value])
```

### <a name="parameters---topstr"></a><span data-ttu-id="a0a5a-789">パラメーター - topStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-789">Parameters - topStr</span></span>

<span data-ttu-id="a0a5a-790">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-790">value</span></span>  

### <a name="return-value---topstr"></a><span data-ttu-id="a0a5a-791">戻り値 - topStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-791">Return Value - topStr</span></span>

## <a name="method-topunit"></a><span data-ttu-id="a0a5a-792">メソッド topUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-792">Method topUnit</span></span>

```xpp
public Units topUnit([Units value])
```

### <a name="parameters---topunit"></a><span data-ttu-id="a0a5a-793">パラメーター - topUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-793">Parameters - topUnit</span></span>

<span data-ttu-id="a0a5a-794">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-794">value</span></span>  

### <a name="return-value---topunit"></a><span data-ttu-id="a0a5a-795">戻り値 - topUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-795">Return Value - topUnit</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="a0a5a-796">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-796">Method topValue</span></span>

```xpp
public Real topValue([Real value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="a0a5a-797">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-797">Parameters - topValue</span></span>

<span data-ttu-id="a0a5a-798">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-798">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="a0a5a-799">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-799">Return Value - topValue</span></span>

## <a name="method-typeheaderprompt"></a><span data-ttu-id="a0a5a-800">メソッド typeHeaderPrompt</span><span class="sxs-lookup"><span data-stu-id="a0a5a-800">Method typeHeaderPrompt</span></span>

```xpp
public int typeHeaderPrompt([int value])
```

### <a name="parameters---typeheaderprompt"></a><span data-ttu-id="a0a5a-801">パラメーター - typeHeaderPrompt</span><span class="sxs-lookup"><span data-stu-id="a0a5a-801">Parameters - typeHeaderPrompt</span></span>

<span data-ttu-id="a0a5a-802">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-802">value</span></span>  

### <a name="return-value---typeheaderprompt"></a><span data-ttu-id="a0a5a-803">戻り値 - typeHeaderPrompt</span><span class="sxs-lookup"><span data-stu-id="a0a5a-803">Return Value - typeHeaderPrompt</span></span>

## <a name="method-underline"></a><span data-ttu-id="a0a5a-804">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="a0a5a-804">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="a0a5a-805">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="a0a5a-805">Parameters - underline</span></span>

<span data-ttu-id="a0a5a-806">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-806">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="a0a5a-807">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="a0a5a-807">Return Value - underline</span></span>

## <a name="method-visible"></a><span data-ttu-id="a0a5a-808">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="a0a5a-808">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="a0a5a-809">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="a0a5a-809">Parameters - visible</span></span>

<span data-ttu-id="a0a5a-810">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-810">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="a0a5a-811">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="a0a5a-811">Return Value - visible</span></span>

## <a name="method-webmenuitemname"></a><span data-ttu-id="a0a5a-812">メソッド webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="a0a5a-812">Method webMenuItemName</span></span>

```xpp
public str webMenuItemName([str value])
```

### <a name="parameters---webmenuitemname"></a><span data-ttu-id="a0a5a-813">パラメーター - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="a0a5a-813">Parameters - webMenuItemName</span></span>

<span data-ttu-id="a0a5a-814">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-814">value</span></span>  

### <a name="return-value---webmenuitemname"></a><span data-ttu-id="a0a5a-815">戻り値 - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="a0a5a-815">Return Value - webMenuItemName</span></span>

## <a name="method-webmenuitemtype"></a><span data-ttu-id="a0a5a-816">メソッド webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="a0a5a-816">Method webMenuItemType</span></span>

```xpp
public WebMenuItemType webMenuItemType([WebMenuItemType value])
```

### <a name="parameters---webmenuitemtype"></a><span data-ttu-id="a0a5a-817">パラメーター - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="a0a5a-817">Parameters - webMenuItemType</span></span>

<span data-ttu-id="a0a5a-818">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-818">value</span></span>  

### <a name="return-value---webmenuitemtype"></a><span data-ttu-id="a0a5a-819">戻り値 - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="a0a5a-819">Return Value - webMenuItemType</span></span>

## <a name="method-webtarget"></a><span data-ttu-id="a0a5a-820">メソッド webTarget</span><span class="sxs-lookup"><span data-stu-id="a0a5a-820">Method webTarget</span></span>

```xpp
public str webTarget([str value])
```

### <a name="parameters---webtarget"></a><span data-ttu-id="a0a5a-821">パラメーター - webTarget</span><span class="sxs-lookup"><span data-stu-id="a0a5a-821">Parameters - webTarget</span></span>

<span data-ttu-id="a0a5a-822">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-822">value</span></span>  

### <a name="return-value---webtarget"></a><span data-ttu-id="a0a5a-823">戻り値 - webTarget</span><span class="sxs-lookup"><span data-stu-id="a0a5a-823">Return Value - webTarget</span></span>

## <a name="method-width100mm"></a><span data-ttu-id="a0a5a-824">メソッド width100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-824">Method width100mm</span></span>

```xpp
public int width100mm([int widthExclBorder])
```

### <a name="parameters---width100mm"></a><span data-ttu-id="a0a5a-825">パラメーター - width100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-825">Parameters - width100mm</span></span>

<span data-ttu-id="a0a5a-826">widthExclBorder</span><span class="sxs-lookup"><span data-stu-id="a0a5a-826">widthExclBorder</span></span>  

### <a name="return-value---width100mm"></a><span data-ttu-id="a0a5a-827">戻り値 - width100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-827">Return Value - width100mm</span></span>

## <a name="method-width100mminclborder"></a><span data-ttu-id="a0a5a-828">メソッド width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="a0a5a-828">Method width100mmInclBorder</span></span>

```xpp
public int width100mmInclBorder([int widthInclBorder])
```

### <a name="parameters---width100mminclborder"></a><span data-ttu-id="a0a5a-829">パラメーター - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="a0a5a-829">Parameters - width100mmInclBorder</span></span>

<span data-ttu-id="a0a5a-830">widthInclBorder</span><span class="sxs-lookup"><span data-stu-id="a0a5a-830">widthInclBorder</span></span>  

### <a name="return-value---width100mminclborder"></a><span data-ttu-id="a0a5a-831">戻り値 - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="a0a5a-831">Return Value - width100mmInclBorder</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="a0a5a-832">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-832">Method widthMode</span></span>

<span data-ttu-id="a0a5a-833">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-833">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="a0a5a-834">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-834">Parameters - widthMode</span></span>

<span data-ttu-id="a0a5a-835">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-835">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="a0a5a-836">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-836">Return Value - widthMode</span></span>

<span data-ttu-id="a0a5a-837">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-837">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="a0a5a-838">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="a0a5a-838">Remarks - widthMode</span></span>

<span data-ttu-id="a0a5a-839">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="a0a5a-839">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="a0a5a-840">モード。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-840">Mode.</span></span>         | <span data-ttu-id="a0a5a-841">幅計算。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-841">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0a5a-842">正確。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-842">Exact.</span></span>        | <span data-ttu-id="a0a5a-843">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-843">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="a0a5a-844">自動。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-844">Auto.</span></span>         | <span data-ttu-id="a0a5a-845">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-845">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="a0a5a-846">列の幅。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-846">Column width.</span></span> | <span data-ttu-id="a0a5a-847">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-847">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="a0a5a-848">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-848">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthofstring100mm"></a><span data-ttu-id="a0a5a-849">メソッド widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-849">Method widthOfString100mm</span></span>

```xpp
public int widthOfString100mm(str string)
```

### <a name="parameters---widthofstring100mm"></a><span data-ttu-id="a0a5a-850">パラメーター - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-850">Parameters - widthOfString100mm</span></span>

<span data-ttu-id="a0a5a-851">文字列</span><span class="sxs-lookup"><span data-stu-id="a0a5a-851">string</span></span>  

### <a name="return-value---widthofstring100mm"></a><span data-ttu-id="a0a5a-852">戻り値 - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="a0a5a-852">Return Value - widthOfString100mm</span></span>

## <a name="method-widthstr"></a><span data-ttu-id="a0a5a-853">メソッド widthStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-853">Method widthStr</span></span>

```xpp
public str widthStr([str value])
```

### <a name="parameters---widthstr"></a><span data-ttu-id="a0a5a-854">パラメーター - widthStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-854">Parameters - widthStr</span></span>

<span data-ttu-id="a0a5a-855">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-855">value</span></span>  

### <a name="return-value---widthstr"></a><span data-ttu-id="a0a5a-856">戻り値 - widthStr</span><span class="sxs-lookup"><span data-stu-id="a0a5a-856">Return Value - widthStr</span></span>

## <a name="method-widthunit"></a><span data-ttu-id="a0a5a-857">メソッド widthUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-857">Method widthUnit</span></span>

```xpp
public Units widthUnit([Units value])
```

### <a name="parameters---widthunit"></a><span data-ttu-id="a0a5a-858">パラメーター - widthUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-858">Parameters - widthUnit</span></span>

<span data-ttu-id="a0a5a-859">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-859">value</span></span>  

### <a name="return-value---widthunit"></a><span data-ttu-id="a0a5a-860">戻り値 - widthUnit</span><span class="sxs-lookup"><span data-stu-id="a0a5a-860">Return Value - widthUnit</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="a0a5a-861">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-861">Method widthValue</span></span>

<span data-ttu-id="a0a5a-862">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-862">Gets or sets the width of the control.</span></span>

```xpp
public Real widthValue([Real value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="a0a5a-863">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-863">Parameters - widthValue</span></span>

<span data-ttu-id="a0a5a-864">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-864">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="a0a5a-865">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-865">Return Value - widthValue</span></span>

<span data-ttu-id="a0a5a-866">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-866">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="a0a5a-867">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="a0a5a-867">Remarks - widthValue</span></span>

<span data-ttu-id="a0a5a-868">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-868">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-show"></a><span data-ttu-id="a0a5a-869">メソッド show</span><span class="sxs-lookup"><span data-stu-id="a0a5a-869">Method show</span></span>

```xpp
public void show()
```

## <a name="method-topmargin"></a><span data-ttu-id="a0a5a-870">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="a0a5a-870">Method topMargin</span></span>

```xpp
public void topMargin(Real value, Units unit)
```

### <a name="parameters---topmargin"></a><span data-ttu-id="a0a5a-871">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="a0a5a-871">Parameters - topMargin</span></span>

<span data-ttu-id="a0a5a-872">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-872">value</span></span>  

<!-- -->

<span data-ttu-id="a0a5a-873">単位</span><span class="sxs-lookup"><span data-stu-id="a0a5a-873">unit</span></span>  

## <a name="method-bottommargin"></a><span data-ttu-id="a0a5a-874">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="a0a5a-874">Method bottomMargin</span></span>

```xpp
public void bottomMargin(Real value, Units unit)
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="a0a5a-875">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="a0a5a-875">Parameters - bottomMargin</span></span>

<span data-ttu-id="a0a5a-876">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-876">value</span></span>  

<!-- -->

<span data-ttu-id="a0a5a-877">単位</span><span class="sxs-lookup"><span data-stu-id="a0a5a-877">unit</span></span>  

## <a name="method-labelwidth"></a><span data-ttu-id="a0a5a-878">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="a0a5a-878">Method labelWidth</span></span>

```xpp
public void labelWidth(Real value, Units unit)
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="a0a5a-879">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="a0a5a-879">Parameters - labelWidth</span></span>

<span data-ttu-id="a0a5a-880">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-880">value</span></span>  

<!-- -->

<span data-ttu-id="a0a5a-881">単位</span><span class="sxs-lookup"><span data-stu-id="a0a5a-881">unit</span></span>  

## <a name="method-top"></a><span data-ttu-id="a0a5a-882">メソッド top</span><span class="sxs-lookup"><span data-stu-id="a0a5a-882">Method top</span></span>

```xpp
public void top(Real value, Units unit)
```

### <a name="parameters---top"></a><span data-ttu-id="a0a5a-883">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="a0a5a-883">Parameters - top</span></span>

<span data-ttu-id="a0a5a-884">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-884">value</span></span>  

<!-- -->

<span data-ttu-id="a0a5a-885">単位</span><span class="sxs-lookup"><span data-stu-id="a0a5a-885">unit</span></span>  

## <a name="method-width"></a><span data-ttu-id="a0a5a-886">メソッド width</span><span class="sxs-lookup"><span data-stu-id="a0a5a-886">Method width</span></span>

<span data-ttu-id="a0a5a-887">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-887">Gets or sets the width of the control.</span></span>

```xpp
public void width(Real value, Units unit)
```

### <a name="parameters---width"></a><span data-ttu-id="a0a5a-888">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="a0a5a-888">Parameters - width</span></span>

<span data-ttu-id="a0a5a-889">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-889">value</span></span>  

<!-- -->

<span data-ttu-id="a0a5a-890">単位</span><span class="sxs-lookup"><span data-stu-id="a0a5a-890">unit</span></span>  

### <a name="remarks---width"></a><span data-ttu-id="a0a5a-891">備考 - width</span><span class="sxs-lookup"><span data-stu-id="a0a5a-891">Remarks - width</span></span>

<span data-ttu-id="a0a5a-892">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-892">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="a0a5a-893">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="a0a5a-893">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="a0a5a-894">モード。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-894">Mode.</span></span>           | <span data-ttu-id="a0a5a-895">幅計算。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-895">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0a5a-896">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-896">-1 Exact.</span></span>       | <span data-ttu-id="a0a5a-897">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-897">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="a0a5a-898">0 自動。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-898">0 Auto.</span></span>         | <span data-ttu-id="a0a5a-899">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-899">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="a0a5a-900">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-900">1 Column width.</span></span> | <span data-ttu-id="a0a5a-901">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-901">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="a0a5a-902">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-902">The width and width calculation mode can be set separately.</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="a0a5a-903">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="a0a5a-903">Method leftMargin</span></span>

```xpp
public void leftMargin(Real value, Units unit)
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="a0a5a-904">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="a0a5a-904">Parameters - leftMargin</span></span>

<span data-ttu-id="a0a5a-905">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-905">value</span></span>  

<!-- -->

<span data-ttu-id="a0a5a-906">単位</span><span class="sxs-lookup"><span data-stu-id="a0a5a-906">unit</span></span>  

## <a name="method-height"></a><span data-ttu-id="a0a5a-907">メソッド height</span><span class="sxs-lookup"><span data-stu-id="a0a5a-907">Method height</span></span>

<span data-ttu-id="a0a5a-908">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-908">Gets or sets the height of the control.</span></span>

```xpp
public void height(Real value, Units unit)
```

### <a name="parameters---height"></a><span data-ttu-id="a0a5a-909">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="a0a5a-909">Parameters - height</span></span>

<span data-ttu-id="a0a5a-910">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-910">value</span></span>  

<!-- -->

<span data-ttu-id="a0a5a-911">単位</span><span class="sxs-lookup"><span data-stu-id="a0a5a-911">unit</span></span>  

### <a name="remarks---height"></a><span data-ttu-id="a0a5a-912">備考 - height</span><span class="sxs-lookup"><span data-stu-id="a0a5a-912">Remarks - height</span></span>

<span data-ttu-id="a0a5a-913">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-913">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="a0a5a-914">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="a0a5a-914">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="a0a5a-915">モード。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-915">Mode.</span></span>            | <span data-ttu-id="a0a5a-916">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-916">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0a5a-917">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-917">-1 Exact.</span></span>        | <span data-ttu-id="a0a5a-918">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-918">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="a0a5a-919">0 自動。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-919">0 Auto.</span></span>          | <span data-ttu-id="a0a5a-920">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-920">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="a0a5a-921">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-921">1 Column height.</span></span> | <span data-ttu-id="a0a5a-922">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-922">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="a0a5a-923">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="a0a5a-923">The height and height calculation mode can be set separately.</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="a0a5a-924">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="a0a5a-924">Method rightMargin</span></span>

```xpp
public void rightMargin(Real value, Units unit)
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="a0a5a-925">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="a0a5a-925">Parameters - rightMargin</span></span>

<span data-ttu-id="a0a5a-926">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-926">value</span></span>  

<!-- -->

<span data-ttu-id="a0a5a-927">単位</span><span class="sxs-lookup"><span data-stu-id="a0a5a-927">unit</span></span>  

## <a name="method-left"></a><span data-ttu-id="a0a5a-928">メソッド left</span><span class="sxs-lookup"><span data-stu-id="a0a5a-928">Method left</span></span>

```xpp
public void left(Real value, Units unit)
```

### <a name="parameters---left"></a><span data-ttu-id="a0a5a-929">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="a0a5a-929">Parameters - left</span></span>

<span data-ttu-id="a0a5a-930">値</span><span class="sxs-lookup"><span data-stu-id="a0a5a-930">value</span></span>  

<!-- -->

<span data-ttu-id="a0a5a-931">単位</span><span class="sxs-lookup"><span data-stu-id="a0a5a-931">unit</span></span>  

## <a name="method-hide"></a><span data-ttu-id="a0a5a-932">メソッド hide</span><span class="sxs-lookup"><span data-stu-id="a0a5a-932">Method hide</span></span>

```xpp
public void hide()
```

