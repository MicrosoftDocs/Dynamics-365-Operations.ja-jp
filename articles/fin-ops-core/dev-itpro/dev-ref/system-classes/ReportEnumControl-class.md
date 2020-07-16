---
title: ReportEnumControl クラス
description: このトピックでは、ReportEnumControl クラスについて説明します。
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
ms.openlocfilehash: 74b84f5171a93b548691f0580f0b5a37b1c8b684
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502844"
---
# <a name="class-reportenumcontrol"></a><span data-ttu-id="f9f72-103">クラス ReportEnumControl</span><span class="sxs-lookup"><span data-stu-id="f9f72-103">Class ReportEnumControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ReportEnumControl extends ReportControl
```

<span data-ttu-id="f9f72-104">ReportEnumControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f9f72-104">The ReportEnumControl class lets you to create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9f72-105">備考</span><span class="sxs-lookup"><span data-stu-id="f9f72-105">Remarks</span></span>

<span data-ttu-id="f9f72-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="f9f72-107">例</span><span class="sxs-lookup"><span data-stu-id="f9f72-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="f9f72-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="f9f72-108">Methods</span></span>

| <span data-ttu-id="f9f72-109">方法</span><span class="sxs-lookup"><span data-stu-id="f9f72-109">Method</span></span>                                                                   | <span data-ttu-id="f9f72-110">説明</span><span class="sxs-lookup"><span data-stu-id="f9f72-110">Description</span></span>                                                                                                                               |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9f72-111">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-111">public int alignment(\[int value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="f9f72-112">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-112">public int arrayIndex(\[int value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="f9f72-113">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-113">public boolean autoDeclaration(\[boolean value\])</span></span>                        | <span data-ttu-id="f9f72-114">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-114">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                        |
| <span data-ttu-id="f9f72-115">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-115">public int backgroundColor(\[int value\])</span></span>                                | <span data-ttu-id="f9f72-116">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-116">Gets or sets the background color of the control.</span></span>                                                                                         |
| <span data-ttu-id="f9f72-117">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-117">public int backStyle(\[int value\])</span></span>                                      | <span data-ttu-id="f9f72-118">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-118">Determines whether the control background can be transparent.</span></span>                                                                            |
| <span data-ttu-id="f9f72-119">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-119">public int bold(\[int value\])</span></span>                                           | <span data-ttu-id="f9f72-120">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-120">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                               |
| <span data-ttu-id="f9f72-121">public int bottomMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="f9f72-121">public int bottomMarginAndFrame()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="f9f72-122">public int bottomMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-122">public int bottomMarginMode(\[int value\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="f9f72-123">public str bottomMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-123">public str bottomMarginStr(\[str value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="f9f72-124">public Units bottomMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-124">public Units bottomMarginUnit(\[Units value\])</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="f9f72-125">public Real bottomMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-125">public Real bottomMarginValue(\[Real value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="f9f72-126">public int changeCase(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-126">public int changeCase(\[int value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="f9f72-127">public int changeLabelCase(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-127">public int changeLabelCase(\[int value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="f9f72-128">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-128">public int characterSet(\[int value\])</span></span>                                   | <span data-ttu-id="f9f72-129">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-129">Gets or sets the character set of the font.</span></span>                                                                                               |
| <span data-ttu-id="f9f72-130">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-130">public int colorScheme(\[int value\])</span></span>                                    | <span data-ttu-id="f9f72-131">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-131">Gets or sets the color scheme of the control.</span></span>                                                                                             |
| <span data-ttu-id="f9f72-132">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-132">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="f9f72-133">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-133">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                       |
| <span data-ttu-id="f9f72-134">public ReportFieldType controlType()</span><span class="sxs-lookup"><span data-stu-id="f9f72-134">public ReportFieldType controlType()</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="f9f72-135">public str cssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-135">public str cssClass(\[str value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="f9f72-136">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-136">public FieldId dataField(\[FieldId value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="f9f72-137">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-137">public str dataMethod(\[str value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="f9f72-138">public int delete()</span><span class="sxs-lookup"><span data-stu-id="f9f72-138">public int delete()</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="f9f72-139">public str effectiveFont()</span><span class="sxs-lookup"><span data-stu-id="f9f72-139">public str effectiveFont()</span></span>                                               |                                                                                                                                           |
| <span data-ttu-id="f9f72-140">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-140">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>         |                                                                                                                                           |
| <span data-ttu-id="f9f72-141">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-141">public str font(\[str value\])</span></span>                                           | <span data-ttu-id="f9f72-142">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-142">Gets or sets the name of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="f9f72-143">public str fontInfoPrinter()</span><span class="sxs-lookup"><span data-stu-id="f9f72-143">public str fontInfoPrinter()</span></span>                                             |                                                                                                                                           |
| <span data-ttu-id="f9f72-144">public int fontInfoPrinterAscent()</span><span class="sxs-lookup"><span data-stu-id="f9f72-144">public int fontInfoPrinterAscent()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="f9f72-145">public int fontInfoPrinterDescent()</span><span class="sxs-lookup"><span data-stu-id="f9f72-145">public int fontInfoPrinterDescent()</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="f9f72-146">public int fontInfoPrinterExtLead()</span><span class="sxs-lookup"><span data-stu-id="f9f72-146">public int fontInfoPrinterExtLead()</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="f9f72-147">public int fontInfoPrinterHeight()</span><span class="sxs-lookup"><span data-stu-id="f9f72-147">public int fontInfoPrinterHeight()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="f9f72-148">public int fontInfoPrinterIntLead()</span><span class="sxs-lookup"><span data-stu-id="f9f72-148">public int fontInfoPrinterIntLead()</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="f9f72-149">public str fontInfoScreen()</span><span class="sxs-lookup"><span data-stu-id="f9f72-149">public str fontInfoScreen()</span></span>                                              |                                                                                                                                           |
| <span data-ttu-id="f9f72-150">public int fontInfoScreenAscent()</span><span class="sxs-lookup"><span data-stu-id="f9f72-150">public int fontInfoScreenAscent()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="f9f72-151">public int fontInfoScreenDescent()</span><span class="sxs-lookup"><span data-stu-id="f9f72-151">public int fontInfoScreenDescent()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="f9f72-152">public int fontInfoScreenExtLead()</span><span class="sxs-lookup"><span data-stu-id="f9f72-152">public int fontInfoScreenExtLead()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="f9f72-153">public int fontInfoScreenHeight()</span><span class="sxs-lookup"><span data-stu-id="f9f72-153">public int fontInfoScreenHeight()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="f9f72-154">public int fontInfoScreenIntLead()</span><span class="sxs-lookup"><span data-stu-id="f9f72-154">public int fontInfoScreenIntLead()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="f9f72-155">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-155">public int fontSize(\[int value\])</span></span>                                       | <span data-ttu-id="f9f72-156">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-156">Gets or sets the size of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="f9f72-157">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-157">public int foregroundColor(\[int value\])</span></span>                                | <span data-ttu-id="f9f72-158">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-158">Gets or sets the text color for the control to use.</span></span>                                                                                       |
| <span data-ttu-id="f9f72-159">public int height100mm(\[int heightExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-159">public int height100mm(\[int heightExclBorder\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="f9f72-160">public int height100mmInclBorder(\[int heightInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-160">public int height100mmInclBorder(\[int heightInclBorder\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="f9f72-161">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-161">public int heightMode(\[int value\])</span></span>                                     | <span data-ttu-id="f9f72-162">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-162">Gets or sets a calculation mode for the height of the control.</span></span>                                                                            |
| <span data-ttu-id="f9f72-163">public int heightOfWordWrappedString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="f9f72-163">public int heightOfWordWrappedString100mm(str string)</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="f9f72-164">public str heightStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-164">public str heightStr(\[str value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="f9f72-165">public Units heightUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-165">public Units heightUnit(\[Units value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="f9f72-166">public Real heightValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-166">public Real heightValue(\[Real value\])</span></span>                                  | <span data-ttu-id="f9f72-167">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-167">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="f9f72-168">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-168">public boolean italic(\[boolean value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="f9f72-169">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-169">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="f9f72-170">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-170">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="f9f72-171">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-171">public int labelBold(\[int value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="f9f72-172">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-172">public int labelCharacterSet(\[int value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="f9f72-173">public str labelCssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-173">public str labelCssClass(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="f9f72-174">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-174">public str labelFont(\[str value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="f9f72-175">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-175">public int labelFontSize(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="f9f72-176">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-176">public boolean labelItalic(\[boolean value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="f9f72-177">public LineType labelLineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-177">public LineType labelLineBelow(\[LineType value\])</span></span>                       |                                                                                                                                           |
| <span data-ttu-id="f9f72-178">public LineThickness labelLineThickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-178">public LineThickness labelLineThickness(\[LineThickness value\])</span></span>         |                                                                                                                                           |
| <span data-ttu-id="f9f72-179">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-179">public int labelPosition(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="f9f72-180">public int labelTabLeader(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-180">public int labelTabLeader(\[int value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="f9f72-181">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-181">public boolean labelUnderline(\[boolean value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="f9f72-182">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-182">public int labelWidthMode(\[int value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="f9f72-183">public str labelWidthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-183">public str labelWidthStr(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="f9f72-184">public Units labelWidthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-184">public Units labelWidthUnit(\[Units value\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="f9f72-185">public Real labelWidthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-185">public Real labelWidthValue(\[Real value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="f9f72-186">public int left100mm(\[int leftExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-186">public int left100mm(\[int leftExclBorder\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="f9f72-187">public int left100mmInclBorder(\[int leftInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-187">public int left100mmInclBorder(\[int leftInclBorder\])</span></span>                   |                                                                                                                                           |
| <span data-ttu-id="f9f72-188">public int leftMarginAnFrame()</span><span class="sxs-lookup"><span data-stu-id="f9f72-188">public int leftMarginAnFrame()</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="f9f72-189">public int leftMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-189">public int leftMarginMode(\[int value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="f9f72-190">public str leftMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-190">public str leftMarginStr(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="f9f72-191">public Units leftMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-191">public Units leftMarginUnit(\[Units value\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="f9f72-192">public Real leftMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-192">public Real leftMarginValue(\[Real value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="f9f72-193">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-193">public int leftMode(\[int value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="f9f72-194">public str leftStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-194">public str leftStr(\[str value\])</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="f9f72-195">public Units leftUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-195">public Units leftUnit(\[Units value\])</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="f9f72-196">public Real leftValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-196">public Real leftValue(\[Real value\])</span></span>                                    |                                                                                                                                           |
| <span data-ttu-id="f9f72-197">public LineType lineAbove(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-197">public LineType lineAbove(\[LineType value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="f9f72-198">public LineType lineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-198">public LineType lineBelow(\[LineType value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="f9f72-199">public LineType lineLeft(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-199">public LineType lineLeft(\[LineType value\])</span></span>                             | <span data-ttu-id="f9f72-200">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-200">Gets or sets the type of line that is used as the left border of a section.</span></span>                                                               |
| <span data-ttu-id="f9f72-201">public LineType lineRight(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-201">public LineType lineRight(\[LineType value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="f9f72-202">public str menuItemLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-202">public str menuItemLabel(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="f9f72-203">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-203">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="f9f72-204">public MenuItemType menuItemType(\[MenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-204">public MenuItemType menuItemType(\[MenuItemType value\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="f9f72-205">public str modelFieldName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-205">public str modelFieldName(\[str value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="f9f72-206">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-206">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="f9f72-207">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-207">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="f9f72-208">public int numberOfLines(int height100mm)</span><span class="sxs-lookup"><span data-stu-id="f9f72-208">public int numberOfLines(int height100mm)</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="f9f72-209">public int position(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-209">public int position(\[int value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="f9f72-210">public str previewInfo(str string)</span><span class="sxs-lookup"><span data-stu-id="f9f72-210">public str previewInfo(str string)</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="f9f72-211">public int previewXCompensation100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="f9f72-211">public int previewXCompensation100mm(str string)</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="f9f72-212">public int right100mm()</span><span class="sxs-lookup"><span data-stu-id="f9f72-212">public int right100mm()</span></span>                                                  |                                                                                                                                           |
| <span data-ttu-id="f9f72-213">public int right100mmInclBorder()</span><span class="sxs-lookup"><span data-stu-id="f9f72-213">public int right100mmInclBorder()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="f9f72-214">public int rightMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="f9f72-214">public int rightMarginAndFrame()</span></span>                                         |                                                                                                                                           |
| <span data-ttu-id="f9f72-215">public int rightMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-215">public int rightMarginMode(\[int value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="f9f72-216">public str rightMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-216">public str rightMarginStr(\[str value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="f9f72-217">public Units rightMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-217">public Units rightMarginUnit(\[Units value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="f9f72-218">public Real rightMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-218">public Real rightMarginValue(\[Real value\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="f9f72-219">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-219">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                                           |
| <span data-ttu-id="f9f72-220">public str setHeightGetText(int lines, str string)</span><span class="sxs-lookup"><span data-stu-id="f9f72-220">public str setHeightGetText(int lines, str string)</span></span>                       |                                                                                                                                           |
| <span data-ttu-id="f9f72-221">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-221">public boolean showLabel(\[boolean value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="f9f72-222">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-222">public TableId table(\[TableId value\])</span></span>                                  | <span data-ttu-id="f9f72-223">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-223">Gets or sets the table ID associated with the object.</span></span>                                                                                     |
| <span data-ttu-id="f9f72-224">public LineThickness thickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-224">public LineThickness thickness(\[LineThickness value\])</span></span>                  |                                                                                                                                           |
| <span data-ttu-id="f9f72-225">public int top100mm(\[int topExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-225">public int top100mm(\[int topExclBorder\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="f9f72-226">public int top100mmInclBorder(\[int topInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-226">public int top100mmInclBorder(\[int topInclBorder\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="f9f72-227">public int topMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="f9f72-227">public int topMarginAndFrame()</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="f9f72-228">public int topMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-228">public int topMarginMode(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="f9f72-229">public str topMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-229">public str topMarginStr(\[str value\])</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="f9f72-230">public Units topMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-230">public Units topMarginUnit(\[Units value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="f9f72-231">public Real topMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-231">public Real topMarginValue(\[Real value\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="f9f72-232">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-232">public int topMode(\[int value\])</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="f9f72-233">public str topStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-233">public str topStr(\[str value\])</span></span>                                         |                                                                                                                                           |
| <span data-ttu-id="f9f72-234">public Units topUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-234">public Units topUnit(\[Units value\])</span></span>                                    |                                                                                                                                           |
| <span data-ttu-id="f9f72-235">public Real topValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-235">public Real topValue(\[Real value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="f9f72-236">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-236">public boolean underline(\[boolean value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="f9f72-237">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-237">public boolean visible(\[boolean value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="f9f72-238">public str webMenuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-238">public str webMenuItemName(\[str value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="f9f72-239">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-239">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span></span>        |                                                                                                                                           |
| <span data-ttu-id="f9f72-240">public str webTarget(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-240">public str webTarget(\[str value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="f9f72-241">public int width100mm(\[int widthExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-241">public int width100mm(\[int widthExclBorder\])</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="f9f72-242">public int width100mmInclBorder(\[int widthInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-242">public int width100mmInclBorder(\[int widthInclBorder\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="f9f72-243">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-243">public int widthMode(\[int value\])</span></span>                                      | <span data-ttu-id="f9f72-244">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-244">Gets or sets the calculation mode of the width of the control.</span></span>                                                                            |
| <span data-ttu-id="f9f72-245">public int widthOfString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="f9f72-245">public int widthOfString100mm(str string)</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="f9f72-246">public str widthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-246">public str widthStr(\[str value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="f9f72-247">public Units widthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-247">public Units widthUnit(\[Units value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="f9f72-248">public Real widthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="f9f72-248">public Real widthValue(\[Real value\])</span></span>                                   | <span data-ttu-id="f9f72-249">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-249">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="f9f72-250">public void top(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="f9f72-250">public void top(Real value, Units unit)</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="f9f72-251">public void bottomMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="f9f72-251">public void bottomMargin(Real value, Units unit)</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="f9f72-252">public void height(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="f9f72-252">public void height(Real value, Units unit)</span></span>                               | <span data-ttu-id="f9f72-253">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-253">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="f9f72-254">public void show()</span><span class="sxs-lookup"><span data-stu-id="f9f72-254">public void show()</span></span>                                                       |                                                                                                                                           |
| <span data-ttu-id="f9f72-255">public void labelWidth(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="f9f72-255">public void labelWidth(Real value, Units unit)</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="f9f72-256">public void leftMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="f9f72-256">public void leftMargin(Real value, Units unit)</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="f9f72-257">public void topMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="f9f72-257">public void topMargin(Real value, Units unit)</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="f9f72-258">public void width(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="f9f72-258">public void width(Real value, Units unit)</span></span>                                | <span data-ttu-id="f9f72-259">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-259">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="f9f72-260">public void rightMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="f9f72-260">public void rightMargin(Real value, Units unit)</span></span>                          |                                                                                                                                           |
| <span data-ttu-id="f9f72-261">public void left(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="f9f72-261">public void left(Real value, Units unit)</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="f9f72-262">public void hide()</span><span class="sxs-lookup"><span data-stu-id="f9f72-262">public void hide()</span></span>                                                       |                                                                                                                                           |

## <a name="method-alignment"></a><span data-ttu-id="f9f72-263">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="f9f72-263">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="f9f72-264">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="f9f72-264">Parameters - alignment</span></span>

<span data-ttu-id="f9f72-265">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-265">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="f9f72-266">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="f9f72-266">Return Value - alignment</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="f9f72-267">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="f9f72-267">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="f9f72-268">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="f9f72-268">Parameters - arrayIndex</span></span>

<span data-ttu-id="f9f72-269">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-269">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="f9f72-270">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="f9f72-270">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="f9f72-271">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="f9f72-271">Method autoDeclaration</span></span>

<span data-ttu-id="f9f72-272">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-272">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="f9f72-273">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="f9f72-273">Parameters - autoDeclaration</span></span>

<span data-ttu-id="f9f72-274">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-274">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="f9f72-275">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="f9f72-275">Return Value - autoDeclaration</span></span>

<span data-ttu-id="f9f72-276">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f9f72-276">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="f9f72-277">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="f9f72-277">Remarks - autoDeclaration</span></span>

<span data-ttu-id="f9f72-278">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="f9f72-278">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="f9f72-279">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="f9f72-279">Method backgroundColor</span></span>

<span data-ttu-id="f9f72-280">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-280">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="f9f72-281">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="f9f72-281">Parameters - backgroundColor</span></span>

<span data-ttu-id="f9f72-282">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-282">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="f9f72-283">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="f9f72-283">Return Value - backgroundColor</span></span>

<span data-ttu-id="f9f72-284">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="f9f72-284">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="f9f72-285">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="f9f72-285">Remarks - backgroundColor</span></span>

<span data-ttu-id="f9f72-286">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f9f72-286">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="f9f72-287">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f9f72-287">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="f9f72-288">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="f9f72-288">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="f9f72-289">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="f9f72-289">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="f9f72-290">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="f9f72-290">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="f9f72-291">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="f9f72-291">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="f9f72-292">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="f9f72-292">Method backStyle</span></span>

<span data-ttu-id="f9f72-293">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-293">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="f9f72-294">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="f9f72-294">Parameters - backStyle</span></span>

<span data-ttu-id="f9f72-295">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-295">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="f9f72-296">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="f9f72-296">Return Value - backStyle</span></span>

<span data-ttu-id="f9f72-297">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="f9f72-297">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="f9f72-298">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="f9f72-298">Method bold</span></span>

<span data-ttu-id="f9f72-299">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-299">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="f9f72-300">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="f9f72-300">Parameters - bold</span></span>

<span data-ttu-id="f9f72-301">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-301">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="f9f72-302">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="f9f72-302">Return Value - bold</span></span>

<span data-ttu-id="f9f72-303">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="f9f72-303">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="f9f72-304">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="f9f72-304">Remarks - bold</span></span>

<span data-ttu-id="f9f72-305">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f9f72-305">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="f9f72-306">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-306">0 Use the default font weight.</span></span>
-   <span data-ttu-id="f9f72-307">1 シン。</span><span class="sxs-lookup"><span data-stu-id="f9f72-307">1 Thin.</span></span>
-   <span data-ttu-id="f9f72-308">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="f9f72-308">2 Extra-light.</span></span>
-   <span data-ttu-id="f9f72-309">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="f9f72-309">3 Light.</span></span>
-   <span data-ttu-id="f9f72-310">4 標準。</span><span class="sxs-lookup"><span data-stu-id="f9f72-310">4 Normal.</span></span>
-   <span data-ttu-id="f9f72-311">5 中。</span><span class="sxs-lookup"><span data-stu-id="f9f72-311">5 Medium.</span></span>
-   <span data-ttu-id="f9f72-312">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="f9f72-312">6 Semibold.</span></span>
-   <span data-ttu-id="f9f72-313">7 太字。</span><span class="sxs-lookup"><span data-stu-id="f9f72-313">7 Bold.</span></span>
-   <span data-ttu-id="f9f72-314">8 極太。</span><span class="sxs-lookup"><span data-stu-id="f9f72-314">8 Extra-bold.</span></span>
-   <span data-ttu-id="f9f72-315">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="f9f72-315">9 Heavy.</span></span>

## <a name="method-bottommarginandframe"></a><span data-ttu-id="f9f72-316">メソッド bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="f9f72-316">Method bottomMarginAndFrame</span></span>

```xpp
public int bottomMarginAndFrame()
```

### <a name="return-value---bottommarginandframe"></a><span data-ttu-id="f9f72-317">戻り値 - bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="f9f72-317">Return Value - bottomMarginAndFrame</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="f9f72-318">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-318">Method bottomMarginMode</span></span>

```xpp
public int bottomMarginMode([int value])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="f9f72-319">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-319">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="f9f72-320">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-320">value</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="f9f72-321">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-321">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginstr"></a><span data-ttu-id="f9f72-322">メソッド bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-322">Method bottomMarginStr</span></span>

```xpp
public str bottomMarginStr([str value])
```

### <a name="parameters---bottommarginstr"></a><span data-ttu-id="f9f72-323">パラメーター - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-323">Parameters - bottomMarginStr</span></span>

<span data-ttu-id="f9f72-324">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-324">value</span></span>  

### <a name="return-value---bottommarginstr"></a><span data-ttu-id="f9f72-325">戻り値 - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-325">Return Value - bottomMarginStr</span></span>

## <a name="method-bottommarginunit"></a><span data-ttu-id="f9f72-326">メソッド bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-326">Method bottomMarginUnit</span></span>

```xpp
public Units bottomMarginUnit([Units value])
```

### <a name="parameters---bottommarginunit"></a><span data-ttu-id="f9f72-327">パラメーター - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-327">Parameters - bottomMarginUnit</span></span>

<span data-ttu-id="f9f72-328">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-328">value</span></span>  

### <a name="return-value---bottommarginunit"></a><span data-ttu-id="f9f72-329">戻り値 - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-329">Return Value - bottomMarginUnit</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="f9f72-330">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-330">Method bottomMarginValue</span></span>

```xpp
public Real bottomMarginValue([Real value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="f9f72-331">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-331">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="f9f72-332">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-332">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="f9f72-333">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-333">Return Value - bottomMarginValue</span></span>

## <a name="method-changecase"></a><span data-ttu-id="f9f72-334">メソッド changeCase</span><span class="sxs-lookup"><span data-stu-id="f9f72-334">Method changeCase</span></span>

```xpp
public int changeCase([int value])
```

### <a name="parameters---changecase"></a><span data-ttu-id="f9f72-335">パラメーター - changeCase</span><span class="sxs-lookup"><span data-stu-id="f9f72-335">Parameters - changeCase</span></span>

<span data-ttu-id="f9f72-336">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-336">value</span></span>  

### <a name="return-value---changecase"></a><span data-ttu-id="f9f72-337">戻り値 - changeCase</span><span class="sxs-lookup"><span data-stu-id="f9f72-337">Return Value - changeCase</span></span>

## <a name="method-changelabelcase"></a><span data-ttu-id="f9f72-338">メソッド changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="f9f72-338">Method changeLabelCase</span></span>

```xpp
public int changeLabelCase([int value])
```

### <a name="parameters---changelabelcase"></a><span data-ttu-id="f9f72-339">パラメーター - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="f9f72-339">Parameters - changeLabelCase</span></span>

<span data-ttu-id="f9f72-340">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-340">value</span></span>  

### <a name="return-value---changelabelcase"></a><span data-ttu-id="f9f72-341">戻り値 - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="f9f72-341">Return Value - changeLabelCase</span></span>

## <a name="method-characterset"></a><span data-ttu-id="f9f72-342">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="f9f72-342">Method characterSet</span></span>

<span data-ttu-id="f9f72-343">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-343">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="f9f72-344">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="f9f72-344">Parameters - characterSet</span></span>

<span data-ttu-id="f9f72-345">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-345">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="f9f72-346">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="f9f72-346">Return Value - characterSet</span></span>

<span data-ttu-id="f9f72-347">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f9f72-347">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="f9f72-348">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="f9f72-348">Remarks - characterSet</span></span>

<span data-ttu-id="f9f72-349">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-349">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="f9f72-350">値です。</span><span class="sxs-lookup"><span data-stu-id="f9f72-350">Value.</span></span> | <span data-ttu-id="f9f72-351">説明。</span><span class="sxs-lookup"><span data-stu-id="f9f72-351">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="f9f72-352">0</span><span class="sxs-lookup"><span data-stu-id="f9f72-352">0</span></span>      | <span data-ttu-id="f9f72-353">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f9f72-353">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="f9f72-354">1</span><span class="sxs-lookup"><span data-stu-id="f9f72-354">1</span></span>      | <span data-ttu-id="f9f72-355">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f9f72-355">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="f9f72-356">2</span><span class="sxs-lookup"><span data-stu-id="f9f72-356">2</span></span>      | <span data-ttu-id="f9f72-357">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f9f72-357">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="f9f72-358">77</span><span class="sxs-lookup"><span data-stu-id="f9f72-358">77</span></span>     | <span data-ttu-id="f9f72-359">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f9f72-359">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="f9f72-360">128</span><span class="sxs-lookup"><span data-stu-id="f9f72-360">128</span></span>    | <span data-ttu-id="f9f72-361">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f9f72-361">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="f9f72-362">129</span><span class="sxs-lookup"><span data-stu-id="f9f72-362">129</span></span>    | <span data-ttu-id="f9f72-363">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f9f72-363">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="f9f72-364">134</span><span class="sxs-lookup"><span data-stu-id="f9f72-364">134</span></span>    | <span data-ttu-id="f9f72-365">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f9f72-365">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="f9f72-366">136</span><span class="sxs-lookup"><span data-stu-id="f9f72-366">136</span></span>    | <span data-ttu-id="f9f72-367">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f9f72-367">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="f9f72-368">161</span><span class="sxs-lookup"><span data-stu-id="f9f72-368">161</span></span>    | <span data-ttu-id="f9f72-369">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f9f72-369">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="f9f72-370">162</span><span class="sxs-lookup"><span data-stu-id="f9f72-370">162</span></span>    | <span data-ttu-id="f9f72-371">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f9f72-371">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="f9f72-372">163</span><span class="sxs-lookup"><span data-stu-id="f9f72-372">163</span></span>    | <span data-ttu-id="f9f72-373">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f9f72-373">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="f9f72-374">186</span><span class="sxs-lookup"><span data-stu-id="f9f72-374">186</span></span>    | <span data-ttu-id="f9f72-375">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f9f72-375">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="f9f72-376">204</span><span class="sxs-lookup"><span data-stu-id="f9f72-376">204</span></span>    | <span data-ttu-id="f9f72-377">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f9f72-377">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="f9f72-378">238</span><span class="sxs-lookup"><span data-stu-id="f9f72-378">238</span></span>    | <span data-ttu-id="f9f72-379">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f9f72-379">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="f9f72-380">255</span><span class="sxs-lookup"><span data-stu-id="f9f72-380">255</span></span>    | <span data-ttu-id="f9f72-381">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f9f72-381">OEM\_CHARSET</span></span>         |

<span data-ttu-id="f9f72-382">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="f9f72-382">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="f9f72-383">値です。</span><span class="sxs-lookup"><span data-stu-id="f9f72-383">Value.</span></span> | <span data-ttu-id="f9f72-384">説明。</span><span class="sxs-lookup"><span data-stu-id="f9f72-384">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="f9f72-385">130</span><span class="sxs-lookup"><span data-stu-id="f9f72-385">130</span></span>    | <span data-ttu-id="f9f72-386">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f9f72-386">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="f9f72-387">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="f9f72-387">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="f9f72-388">値です。</span><span class="sxs-lookup"><span data-stu-id="f9f72-388">Value.</span></span> | <span data-ttu-id="f9f72-389">説明。</span><span class="sxs-lookup"><span data-stu-id="f9f72-389">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="f9f72-390">177</span><span class="sxs-lookup"><span data-stu-id="f9f72-390">177</span></span>    | <span data-ttu-id="f9f72-391">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f9f72-391">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="f9f72-392">178</span><span class="sxs-lookup"><span data-stu-id="f9f72-392">178</span></span>    | <span data-ttu-id="f9f72-393">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f9f72-393">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="f9f72-394">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="f9f72-394">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="f9f72-395">値です。</span><span class="sxs-lookup"><span data-stu-id="f9f72-395">Value.</span></span> | <span data-ttu-id="f9f72-396">説明。</span><span class="sxs-lookup"><span data-stu-id="f9f72-396">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="f9f72-397">222</span><span class="sxs-lookup"><span data-stu-id="f9f72-397">222</span></span>    | <span data-ttu-id="f9f72-398">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="f9f72-398">THAI\_CHARSET</span></span> |

<span data-ttu-id="f9f72-399">既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="f9f72-399">The default character set is set to a value, depending on the current system locale.</span></span> <span data-ttu-id="f9f72-400">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="f9f72-400">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="f9f72-401">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9f72-401">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="f9f72-402">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="f9f72-402">Method colorScheme</span></span>

<span data-ttu-id="f9f72-403">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-403">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="f9f72-404">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="f9f72-404">Parameters - colorScheme</span></span>

<span data-ttu-id="f9f72-405">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-405">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="f9f72-406">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="f9f72-406">Return Value - colorScheme</span></span>

<span data-ttu-id="f9f72-407">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="f9f72-407">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="f9f72-408">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="f9f72-408">Remarks - colorScheme</span></span>

<span data-ttu-id="f9f72-409">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="f9f72-409">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="f9f72-410">値です。</span><span class="sxs-lookup"><span data-stu-id="f9f72-410">Value.</span></span> | <span data-ttu-id="f9f72-411">スタイル。</span><span class="sxs-lookup"><span data-stu-id="f9f72-411">Style.</span></span>                 |
|--------|------------------------|
| <span data-ttu-id="f9f72-412">0</span><span class="sxs-lookup"><span data-stu-id="f9f72-412">0</span></span>      | <span data-ttu-id="f9f72-413">既定。</span><span class="sxs-lookup"><span data-stu-id="f9f72-413">Default.</span></span>               |
| <span data-ttu-id="f9f72-414">1</span><span class="sxs-lookup"><span data-stu-id="f9f72-414">1</span></span>      | <span data-ttu-id="f9f72-415">Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="f9f72-415">The Windows palette.</span></span>   |
| <span data-ttu-id="f9f72-416">2</span><span class="sxs-lookup"><span data-stu-id="f9f72-416">2</span></span>      | <span data-ttu-id="f9f72-417">真の配色。</span><span class="sxs-lookup"><span data-stu-id="f9f72-417">The true-color scheme.</span></span> |

## <a name="method-configurationkey"></a><span data-ttu-id="f9f72-418">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="f9f72-418">Method configurationKey</span></span>

<span data-ttu-id="f9f72-419">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-419">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="f9f72-420">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="f9f72-420">Parameters - configurationKey</span></span>

<span data-ttu-id="f9f72-421">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-421">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="f9f72-422">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="f9f72-422">Return Value - configurationKey</span></span>

<span data-ttu-id="f9f72-423">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="f9f72-423">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="f9f72-424">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="f9f72-424">Remarks - configurationKey</span></span>

<span data-ttu-id="f9f72-425">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f9f72-425">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="f9f72-426">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="f9f72-426">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-controltype"></a><span data-ttu-id="f9f72-427">メソッド controlType</span><span class="sxs-lookup"><span data-stu-id="f9f72-427">Method controlType</span></span>

```xpp
public ReportFieldType controlType()
```

### <a name="return-value---controltype"></a><span data-ttu-id="f9f72-428">戻り値 - controlType</span><span class="sxs-lookup"><span data-stu-id="f9f72-428">Return Value - controlType</span></span>

## <a name="method-cssclass"></a><span data-ttu-id="f9f72-429">メソッド cssClass</span><span class="sxs-lookup"><span data-stu-id="f9f72-429">Method cssClass</span></span>

```xpp
public str cssClass([str value])
```

### <a name="parameters---cssclass"></a><span data-ttu-id="f9f72-430">パラメーター - cssClass</span><span class="sxs-lookup"><span data-stu-id="f9f72-430">Parameters - cssClass</span></span>

<span data-ttu-id="f9f72-431">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-431">value</span></span>  

### <a name="return-value---cssclass"></a><span data-ttu-id="f9f72-432">戻り値 - cssClass</span><span class="sxs-lookup"><span data-stu-id="f9f72-432">Return Value - cssClass</span></span>

## <a name="method-datafield"></a><span data-ttu-id="f9f72-433">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="f9f72-433">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="f9f72-434">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="f9f72-434">Parameters - dataField</span></span>

<span data-ttu-id="f9f72-435">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-435">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="f9f72-436">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="f9f72-436">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="f9f72-437">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="f9f72-437">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="f9f72-438">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="f9f72-438">Parameters - dataMethod</span></span>

<span data-ttu-id="f9f72-439">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-439">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="f9f72-440">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="f9f72-440">Return Value - dataMethod</span></span>

## <a name="method-delete"></a><span data-ttu-id="f9f72-441">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="f9f72-441">Method delete</span></span>

```xpp
public int delete()
```

### <a name="return-value---delete"></a><span data-ttu-id="f9f72-442">戻り値 - delete</span><span class="sxs-lookup"><span data-stu-id="f9f72-442">Return Value - delete</span></span>

## <a name="method-effectivefont"></a><span data-ttu-id="f9f72-443">メソッド effectiveFont</span><span class="sxs-lookup"><span data-stu-id="f9f72-443">Method effectiveFont</span></span>

```xpp
public str effectiveFont()
```

### <a name="return-value---effectivefont"></a><span data-ttu-id="f9f72-444">戻り値 - effectiveFont</span><span class="sxs-lookup"><span data-stu-id="f9f72-444">Return Value - effectiveFont</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="f9f72-445">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="f9f72-445">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="f9f72-446">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="f9f72-446">Parameters - extendedDataType</span></span>

<span data-ttu-id="f9f72-447">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-447">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="f9f72-448">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="f9f72-448">Return Value - extendedDataType</span></span>

## <a name="method-font"></a><span data-ttu-id="f9f72-449">メソッド font</span><span class="sxs-lookup"><span data-stu-id="f9f72-449">Method font</span></span>

<span data-ttu-id="f9f72-450">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-450">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="f9f72-451">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="f9f72-451">Parameters - font</span></span>

<span data-ttu-id="f9f72-452">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-452">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="f9f72-453">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="f9f72-453">Return Value - font</span></span>

<span data-ttu-id="f9f72-454">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="f9f72-454">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontinfoprinter"></a><span data-ttu-id="f9f72-455">メソッド fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="f9f72-455">Method fontInfoPrinter</span></span>

```xpp
public str fontInfoPrinter()
```

### <a name="return-value---fontinfoprinter"></a><span data-ttu-id="f9f72-456">戻り値 - fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="f9f72-456">Return Value - fontInfoPrinter</span></span>

## <a name="method-fontinfoprinterascent"></a><span data-ttu-id="f9f72-457">メソッド fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="f9f72-457">Method fontInfoPrinterAscent</span></span>

```xpp
public int fontInfoPrinterAscent()
```

### <a name="return-value---fontinfoprinterascent"></a><span data-ttu-id="f9f72-458">戻り値 - fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="f9f72-458">Return Value - fontInfoPrinterAscent</span></span>

## <a name="method-fontinfoprinterdescent"></a><span data-ttu-id="f9f72-459">メソッド fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="f9f72-459">Method fontInfoPrinterDescent</span></span>

```xpp
public int fontInfoPrinterDescent()
```

### <a name="return-value---fontinfoprinterdescent"></a><span data-ttu-id="f9f72-460">戻り値 - fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="f9f72-460">Return Value - fontInfoPrinterDescent</span></span>

## <a name="method-fontinfoprinterextlead"></a><span data-ttu-id="f9f72-461">メソッド fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="f9f72-461">Method fontInfoPrinterExtLead</span></span>

```xpp
public int fontInfoPrinterExtLead()
```

### <a name="return-value---fontinfoprinterextlead"></a><span data-ttu-id="f9f72-462">戻り値 - fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="f9f72-462">Return Value - fontInfoPrinterExtLead</span></span>

## <a name="method-fontinfoprinterheight"></a><span data-ttu-id="f9f72-463">メソッド fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="f9f72-463">Method fontInfoPrinterHeight</span></span>

```xpp
public int fontInfoPrinterHeight()
```

### <a name="return-value---fontinfoprinterheight"></a><span data-ttu-id="f9f72-464">戻り値 - fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="f9f72-464">Return Value - fontInfoPrinterHeight</span></span>

## <a name="method-fontinfoprinterintlead"></a><span data-ttu-id="f9f72-465">メソッド fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="f9f72-465">Method fontInfoPrinterIntLead</span></span>

```xpp
public int fontInfoPrinterIntLead()
```

### <a name="return-value---fontinfoprinterintlead"></a><span data-ttu-id="f9f72-466">戻り値 - fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="f9f72-466">Return Value - fontInfoPrinterIntLead</span></span>

## <a name="method-fontinfoscreen"></a><span data-ttu-id="f9f72-467">メソッド fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="f9f72-467">Method fontInfoScreen</span></span>

```xpp
public str fontInfoScreen()
```

### <a name="return-value---fontinfoscreen"></a><span data-ttu-id="f9f72-468">戻り値 - fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="f9f72-468">Return Value - fontInfoScreen</span></span>

## <a name="method-fontinfoscreenascent"></a><span data-ttu-id="f9f72-469">メソッド fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="f9f72-469">Method fontInfoScreenAscent</span></span>

```xpp
public int fontInfoScreenAscent()
```

### <a name="return-value---fontinfoscreenascent"></a><span data-ttu-id="f9f72-470">戻り値 - fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="f9f72-470">Return Value - fontInfoScreenAscent</span></span>

## <a name="method-fontinfoscreendescent"></a><span data-ttu-id="f9f72-471">メソッド fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="f9f72-471">Method fontInfoScreenDescent</span></span>

```xpp
public int fontInfoScreenDescent()
```

### <a name="return-value---fontinfoscreendescent"></a><span data-ttu-id="f9f72-472">戻り値 - fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="f9f72-472">Return Value - fontInfoScreenDescent</span></span>

## <a name="method-fontinfoscreenextlead"></a><span data-ttu-id="f9f72-473">メソッド fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="f9f72-473">Method fontInfoScreenExtLead</span></span>

```xpp
public int fontInfoScreenExtLead()
```

### <a name="return-value---fontinfoscreenextlead"></a><span data-ttu-id="f9f72-474">戻り値 - fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="f9f72-474">Return Value - fontInfoScreenExtLead</span></span>

## <a name="method-fontinfoscreenheight"></a><span data-ttu-id="f9f72-475">メソッド fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="f9f72-475">Method fontInfoScreenHeight</span></span>

```xpp
public int fontInfoScreenHeight()
```

### <a name="return-value---fontinfoscreenheight"></a><span data-ttu-id="f9f72-476">戻り値 - fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="f9f72-476">Return Value - fontInfoScreenHeight</span></span>

## <a name="method-fontinfoscreenintlead"></a><span data-ttu-id="f9f72-477">メソッド fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="f9f72-477">Method fontInfoScreenIntLead</span></span>

```xpp
public int fontInfoScreenIntLead()
```

### <a name="return-value---fontinfoscreenintlead"></a><span data-ttu-id="f9f72-478">戻り値 - fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="f9f72-478">Return Value - fontInfoScreenIntLead</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="f9f72-479">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="f9f72-479">Method fontSize</span></span>

<span data-ttu-id="f9f72-480">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-480">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="f9f72-481">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="f9f72-481">Parameters - fontSize</span></span>

<span data-ttu-id="f9f72-482">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-482">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="f9f72-483">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="f9f72-483">Return Value - fontSize</span></span>

<span data-ttu-id="f9f72-484">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="f9f72-484">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="f9f72-485">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="f9f72-485">Method foregroundColor</span></span>

<span data-ttu-id="f9f72-486">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-486">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="f9f72-487">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="f9f72-487">Parameters - foregroundColor</span></span>

<span data-ttu-id="f9f72-488">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-488">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="f9f72-489">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="f9f72-489">Return Value - foregroundColor</span></span>

<span data-ttu-id="f9f72-490">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="f9f72-490">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="f9f72-491">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="f9f72-491">Remarks - foregroundColor</span></span>

<span data-ttu-id="f9f72-492">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f9f72-492">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="f9f72-493">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f9f72-493">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="f9f72-494">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="f9f72-494">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="f9f72-495">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="f9f72-495">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="f9f72-496">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="f9f72-496">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="f9f72-497">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="f9f72-497">The maximum value for a single byte is 255.</span></span>

## <a name="method-height100mm"></a><span data-ttu-id="f9f72-498">メソッド height100mm</span><span class="sxs-lookup"><span data-stu-id="f9f72-498">Method height100mm</span></span>

```xpp
public int height100mm([int heightExclBorder])
```

### <a name="parameters---height100mm"></a><span data-ttu-id="f9f72-499">パラメーター - height100mm</span><span class="sxs-lookup"><span data-stu-id="f9f72-499">Parameters - height100mm</span></span>

<span data-ttu-id="f9f72-500">heightExclBorder</span><span class="sxs-lookup"><span data-stu-id="f9f72-500">heightExclBorder</span></span>  

### <a name="return-value---height100mm"></a><span data-ttu-id="f9f72-501">戻り値 - height100mm</span><span class="sxs-lookup"><span data-stu-id="f9f72-501">Return Value - height100mm</span></span>

## <a name="method-height100mminclborder"></a><span data-ttu-id="f9f72-502">メソッド height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f9f72-502">Method height100mmInclBorder</span></span>

```xpp
public int height100mmInclBorder([int heightInclBorder])
```

### <a name="parameters---height100mminclborder"></a><span data-ttu-id="f9f72-503">パラメーター - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f9f72-503">Parameters - height100mmInclBorder</span></span>

<span data-ttu-id="f9f72-504">heightInclBorder</span><span class="sxs-lookup"><span data-stu-id="f9f72-504">heightInclBorder</span></span>  

### <a name="return-value---height100mminclborder"></a><span data-ttu-id="f9f72-505">戻り値 - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f9f72-505">Return Value - height100mmInclBorder</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="f9f72-506">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-506">Method heightMode</span></span>

<span data-ttu-id="f9f72-507">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-507">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="f9f72-508">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-508">Parameters - heightMode</span></span>

<span data-ttu-id="f9f72-509">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-509">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="f9f72-510">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-510">Return Value - heightMode</span></span>

<span data-ttu-id="f9f72-511">計算モード。</span><span class="sxs-lookup"><span data-stu-id="f9f72-511">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="f9f72-512">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-512">Remarks - heightMode</span></span>

<span data-ttu-id="f9f72-513">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="f9f72-513">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="f9f72-514">モード。</span><span class="sxs-lookup"><span data-stu-id="f9f72-514">Mode.</span></span>          | <span data-ttu-id="f9f72-515">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="f9f72-515">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9f72-516">正確。</span><span class="sxs-lookup"><span data-stu-id="f9f72-516">Exact.</span></span>         | <span data-ttu-id="f9f72-517">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f9f72-517">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="f9f72-518">自動。</span><span class="sxs-lookup"><span data-stu-id="f9f72-518">Auto.</span></span>          | <span data-ttu-id="f9f72-519">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="f9f72-519">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="f9f72-520">列の高さ</span><span class="sxs-lookup"><span data-stu-id="f9f72-520">Column height.</span></span> | <span data-ttu-id="f9f72-521">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="f9f72-521">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="f9f72-522">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="f9f72-522">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightofwordwrappedstring100mm"></a><span data-ttu-id="f9f72-523">メソッド heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="f9f72-523">Method heightOfWordWrappedString100mm</span></span>

```xpp
public int heightOfWordWrappedString100mm(str string)
```

### <a name="parameters---heightofwordwrappedstring100mm"></a><span data-ttu-id="f9f72-524">パラメーター - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="f9f72-524">Parameters - heightOfWordWrappedString100mm</span></span>

<span data-ttu-id="f9f72-525">文字列</span><span class="sxs-lookup"><span data-stu-id="f9f72-525">string</span></span>  

### <a name="return-value---heightofwordwrappedstring100mm"></a><span data-ttu-id="f9f72-526">戻り値 - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="f9f72-526">Return Value - heightOfWordWrappedString100mm</span></span>

## <a name="method-heightstr"></a><span data-ttu-id="f9f72-527">メソッド heightStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-527">Method heightStr</span></span>

```xpp
public str heightStr([str value])
```

### <a name="parameters---heightstr"></a><span data-ttu-id="f9f72-528">パラメーター - heightStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-528">Parameters - heightStr</span></span>

<span data-ttu-id="f9f72-529">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-529">value</span></span>  

### <a name="return-value---heightstr"></a><span data-ttu-id="f9f72-530">戻り値 - heightStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-530">Return Value - heightStr</span></span>

## <a name="method-heightunit"></a><span data-ttu-id="f9f72-531">メソッド heightUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-531">Method heightUnit</span></span>

```xpp
public Units heightUnit([Units value])
```

### <a name="parameters---heightunit"></a><span data-ttu-id="f9f72-532">パラメーター - heightUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-532">Parameters - heightUnit</span></span>

<span data-ttu-id="f9f72-533">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-533">value</span></span>  

### <a name="return-value---heightunit"></a><span data-ttu-id="f9f72-534">戻り値 - heightUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-534">Return Value - heightUnit</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="f9f72-535">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-535">Method heightValue</span></span>

<span data-ttu-id="f9f72-536">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-536">Gets or sets the height of the control.</span></span>

```xpp
public Real heightValue([Real value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="f9f72-537">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-537">Parameters - heightValue</span></span>

<span data-ttu-id="f9f72-538">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-538">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="f9f72-539">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-539">Return Value - heightValue</span></span>

<span data-ttu-id="f9f72-540">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="f9f72-540">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="f9f72-541">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-541">Remarks - heightValue</span></span>

<span data-ttu-id="f9f72-542">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="f9f72-542">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-italic"></a><span data-ttu-id="f9f72-543">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="f9f72-543">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="f9f72-544">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="f9f72-544">Parameters - italic</span></span>

<span data-ttu-id="f9f72-545">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-545">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="f9f72-546">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="f9f72-546">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="f9f72-547">メソッド label</span><span class="sxs-lookup"><span data-stu-id="f9f72-547">Method label</span></span>

<span data-ttu-id="f9f72-548">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-548">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="f9f72-549">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="f9f72-549">Parameters - label</span></span>

<span data-ttu-id="f9f72-550">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-550">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="f9f72-551">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="f9f72-551">Return Value - label</span></span>

<span data-ttu-id="f9f72-552">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="f9f72-552">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="f9f72-553">備考 - label</span><span class="sxs-lookup"><span data-stu-id="f9f72-553">Remarks - label</span></span>

<span data-ttu-id="f9f72-554">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-554">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="f9f72-555">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="f9f72-555">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="f9f72-556">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="f9f72-556">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="f9f72-557">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="f9f72-557">Parameters - labelBold</span></span>

<span data-ttu-id="f9f72-558">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-558">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="f9f72-559">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="f9f72-559">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="f9f72-560">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="f9f72-560">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="f9f72-561">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="f9f72-561">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="f9f72-562">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-562">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="f9f72-563">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="f9f72-563">Return Value - labelCharacterSet</span></span>

## <a name="method-labelcssclass"></a><span data-ttu-id="f9f72-564">メソッド labelCssClass</span><span class="sxs-lookup"><span data-stu-id="f9f72-564">Method labelCssClass</span></span>

```xpp
public str labelCssClass([str value])
```

### <a name="parameters---labelcssclass"></a><span data-ttu-id="f9f72-565">パラメーター - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="f9f72-565">Parameters - labelCssClass</span></span>

<span data-ttu-id="f9f72-566">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-566">value</span></span>  

### <a name="return-value---labelcssclass"></a><span data-ttu-id="f9f72-567">戻り値 - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="f9f72-567">Return Value - labelCssClass</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="f9f72-568">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="f9f72-568">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="f9f72-569">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="f9f72-569">Parameters - labelFont</span></span>

<span data-ttu-id="f9f72-570">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-570">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="f9f72-571">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="f9f72-571">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="f9f72-572">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="f9f72-572">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="f9f72-573">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="f9f72-573">Parameters - labelFontSize</span></span>

<span data-ttu-id="f9f72-574">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-574">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="f9f72-575">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="f9f72-575">Return Value - labelFontSize</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="f9f72-576">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="f9f72-576">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="f9f72-577">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="f9f72-577">Parameters - labelItalic</span></span>

<span data-ttu-id="f9f72-578">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-578">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="f9f72-579">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="f9f72-579">Return Value - labelItalic</span></span>

## <a name="method-labellinebelow"></a><span data-ttu-id="f9f72-580">メソッド labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="f9f72-580">Method labelLineBelow</span></span>

```xpp
public LineType labelLineBelow([LineType value])
```

### <a name="parameters---labellinebelow"></a><span data-ttu-id="f9f72-581">パラメーター - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="f9f72-581">Parameters - labelLineBelow</span></span>

<span data-ttu-id="f9f72-582">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-582">value</span></span>  

### <a name="return-value---labellinebelow"></a><span data-ttu-id="f9f72-583">戻り値 - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="f9f72-583">Return Value - labelLineBelow</span></span>

## <a name="method-labellinethickness"></a><span data-ttu-id="f9f72-584">メソッド labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="f9f72-584">Method labelLineThickness</span></span>

```xpp
public LineThickness labelLineThickness([LineThickness value])
```

### <a name="parameters---labellinethickness"></a><span data-ttu-id="f9f72-585">パラメーター - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="f9f72-585">Parameters - labelLineThickness</span></span>

<span data-ttu-id="f9f72-586">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-586">value</span></span>  

### <a name="return-value---labellinethickness"></a><span data-ttu-id="f9f72-587">戻り値 - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="f9f72-587">Return Value - labelLineThickness</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="f9f72-588">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="f9f72-588">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="f9f72-589">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="f9f72-589">Parameters - labelPosition</span></span>

<span data-ttu-id="f9f72-590">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-590">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="f9f72-591">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="f9f72-591">Return Value - labelPosition</span></span>

## <a name="method-labeltableader"></a><span data-ttu-id="f9f72-592">メソッド labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="f9f72-592">Method labelTabLeader</span></span>

```xpp
public int labelTabLeader([int value])
```

### <a name="parameters---labeltableader"></a><span data-ttu-id="f9f72-593">パラメーター - labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="f9f72-593">Parameters - labelTabLeader</span></span>

<span data-ttu-id="f9f72-594">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-594">value</span></span>  

### <a name="return-value---labeltableader"></a><span data-ttu-id="f9f72-595">戻り値 - labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="f9f72-595">Return Value - labelTabLeader</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="f9f72-596">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="f9f72-596">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="f9f72-597">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="f9f72-597">Parameters - labelUnderline</span></span>

<span data-ttu-id="f9f72-598">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-598">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="f9f72-599">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="f9f72-599">Return Value - labelUnderline</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="f9f72-600">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-600">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="f9f72-601">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-601">Parameters - labelWidthMode</span></span>

<span data-ttu-id="f9f72-602">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-602">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="f9f72-603">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-603">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthstr"></a><span data-ttu-id="f9f72-604">メソッド labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-604">Method labelWidthStr</span></span>

```xpp
public str labelWidthStr([str value])
```

### <a name="parameters---labelwidthstr"></a><span data-ttu-id="f9f72-605">パラメーター - labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-605">Parameters - labelWidthStr</span></span>

<span data-ttu-id="f9f72-606">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-606">value</span></span>  

### <a name="return-value---labelwidthstr"></a><span data-ttu-id="f9f72-607">戻り値 - labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-607">Return Value - labelWidthStr</span></span>

## <a name="method-labelwidthunit"></a><span data-ttu-id="f9f72-608">メソッド labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-608">Method labelWidthUnit</span></span>

```xpp
public Units labelWidthUnit([Units value])
```

### <a name="parameters---labelwidthunit"></a><span data-ttu-id="f9f72-609">パラメーター - labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-609">Parameters - labelWidthUnit</span></span>

<span data-ttu-id="f9f72-610">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-610">value</span></span>  

### <a name="return-value---labelwidthunit"></a><span data-ttu-id="f9f72-611">戻り値 - labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-611">Return Value - labelWidthUnit</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="f9f72-612">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-612">Method labelWidthValue</span></span>

```xpp
public Real labelWidthValue([Real value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="f9f72-613">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-613">Parameters - labelWidthValue</span></span>

<span data-ttu-id="f9f72-614">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-614">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="f9f72-615">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-615">Return Value - labelWidthValue</span></span>

## <a name="method-left100mm"></a><span data-ttu-id="f9f72-616">メソッド left100mm</span><span class="sxs-lookup"><span data-stu-id="f9f72-616">Method left100mm</span></span>

```xpp
public int left100mm([int leftExclBorder])
```

### <a name="parameters---left100mm"></a><span data-ttu-id="f9f72-617">パラメーター - left100mm</span><span class="sxs-lookup"><span data-stu-id="f9f72-617">Parameters - left100mm</span></span>

<span data-ttu-id="f9f72-618">leftExclBorder</span><span class="sxs-lookup"><span data-stu-id="f9f72-618">leftExclBorder</span></span>  

### <a name="return-value---left100mm"></a><span data-ttu-id="f9f72-619">戻り値 - left100mm</span><span class="sxs-lookup"><span data-stu-id="f9f72-619">Return Value - left100mm</span></span>

## <a name="method-left100mminclborder"></a><span data-ttu-id="f9f72-620">メソッド left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f9f72-620">Method left100mmInclBorder</span></span>

```xpp
public int left100mmInclBorder([int leftInclBorder])
```

### <a name="parameters---left100mminclborder"></a><span data-ttu-id="f9f72-621">パラメーター - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f9f72-621">Parameters - left100mmInclBorder</span></span>

<span data-ttu-id="f9f72-622">leftInclBorder</span><span class="sxs-lookup"><span data-stu-id="f9f72-622">leftInclBorder</span></span>  

### <a name="return-value---left100mminclborder"></a><span data-ttu-id="f9f72-623">戻り値 - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f9f72-623">Return Value - left100mmInclBorder</span></span>

## <a name="method-leftmarginanframe"></a><span data-ttu-id="f9f72-624">メソッド leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="f9f72-624">Method leftMarginAnFrame</span></span>

```xpp
public int leftMarginAnFrame()
```

### <a name="return-value---leftmarginanframe"></a><span data-ttu-id="f9f72-625">戻り値 - leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="f9f72-625">Return Value - leftMarginAnFrame</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="f9f72-626">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-626">Method leftMarginMode</span></span>

```xpp
public int leftMarginMode([int value])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="f9f72-627">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-627">Parameters - leftMarginMode</span></span>

<span data-ttu-id="f9f72-628">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-628">value</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="f9f72-629">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-629">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginstr"></a><span data-ttu-id="f9f72-630">メソッド leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-630">Method leftMarginStr</span></span>

```xpp
public str leftMarginStr([str value])
```

### <a name="parameters---leftmarginstr"></a><span data-ttu-id="f9f72-631">パラメーター - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-631">Parameters - leftMarginStr</span></span>

<span data-ttu-id="f9f72-632">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-632">value</span></span>  

### <a name="return-value---leftmarginstr"></a><span data-ttu-id="f9f72-633">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-633">Return Value - leftMarginStr</span></span>

## <a name="method-leftmarginunit"></a><span data-ttu-id="f9f72-634">メソッド leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-634">Method leftMarginUnit</span></span>

```xpp
public Units leftMarginUnit([Units value])
```

### <a name="parameters---leftmarginunit"></a><span data-ttu-id="f9f72-635">パラメーター - leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-635">Parameters - leftMarginUnit</span></span>

<span data-ttu-id="f9f72-636">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-636">value</span></span>  

### <a name="return-value---leftmarginunit"></a><span data-ttu-id="f9f72-637">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-637">Return Value - leftMarginUnit</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="f9f72-638">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-638">Method leftMarginValue</span></span>

```xpp
public Real leftMarginValue([Real value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="f9f72-639">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-639">Parameters - leftMarginValue</span></span>

<span data-ttu-id="f9f72-640">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-640">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="f9f72-641">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-641">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="f9f72-642">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-642">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="f9f72-643">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-643">Parameters - leftMode</span></span>

<span data-ttu-id="f9f72-644">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-644">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="f9f72-645">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-645">Return Value - leftMode</span></span>

## <a name="method-leftstr"></a><span data-ttu-id="f9f72-646">メソッド leftStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-646">Method leftStr</span></span>

```xpp
public str leftStr([str value])
```

### <a name="parameters---leftstr"></a><span data-ttu-id="f9f72-647">パラメーター - leftStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-647">Parameters - leftStr</span></span>

<span data-ttu-id="f9f72-648">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-648">value</span></span>  

### <a name="return-value---leftstr"></a><span data-ttu-id="f9f72-649">戻り値 - leftStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-649">Return Value - leftStr</span></span>

## <a name="method-leftunit"></a><span data-ttu-id="f9f72-650">メソッド leftUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-650">Method leftUnit</span></span>

```xpp
public Units leftUnit([Units value])
```

### <a name="parameters---leftunit"></a><span data-ttu-id="f9f72-651">パラメーター - leftUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-651">Parameters - leftUnit</span></span>

<span data-ttu-id="f9f72-652">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-652">value</span></span>  

### <a name="return-value---leftunit"></a><span data-ttu-id="f9f72-653">戻り値 - leftUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-653">Return Value - leftUnit</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="f9f72-654">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-654">Method leftValue</span></span>

```xpp
public Real leftValue([Real value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="f9f72-655">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-655">Parameters - leftValue</span></span>

<span data-ttu-id="f9f72-656">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-656">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="f9f72-657">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-657">Return Value - leftValue</span></span>

## <a name="method-lineabove"></a><span data-ttu-id="f9f72-658">メソッド lineAbove</span><span class="sxs-lookup"><span data-stu-id="f9f72-658">Method lineAbove</span></span>

```xpp
public LineType lineAbove([LineType value])
```

### <a name="parameters---lineabove"></a><span data-ttu-id="f9f72-659">パラメーター - lineAbove</span><span class="sxs-lookup"><span data-stu-id="f9f72-659">Parameters - lineAbove</span></span>

<span data-ttu-id="f9f72-660">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-660">value</span></span>  

### <a name="return-value---lineabove"></a><span data-ttu-id="f9f72-661">戻り値 - lineAbove</span><span class="sxs-lookup"><span data-stu-id="f9f72-661">Return Value - lineAbove</span></span>

## <a name="method-linebelow"></a><span data-ttu-id="f9f72-662">メソッド lineBelow</span><span class="sxs-lookup"><span data-stu-id="f9f72-662">Method lineBelow</span></span>

```xpp
public LineType lineBelow([LineType value])
```

### <a name="parameters---linebelow"></a><span data-ttu-id="f9f72-663">パラメーター - lineBelow</span><span class="sxs-lookup"><span data-stu-id="f9f72-663">Parameters - lineBelow</span></span>

<span data-ttu-id="f9f72-664">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-664">value</span></span>  

### <a name="return-value---linebelow"></a><span data-ttu-id="f9f72-665">戻り値 - lineBelow</span><span class="sxs-lookup"><span data-stu-id="f9f72-665">Return Value - lineBelow</span></span>

## <a name="method-lineleft"></a><span data-ttu-id="f9f72-666">メソッド lineLeft</span><span class="sxs-lookup"><span data-stu-id="f9f72-666">Method lineLeft</span></span>

<span data-ttu-id="f9f72-667">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-667">Gets or sets the type of line that is used as the left border of a section.</span></span>

```xpp
public LineType lineLeft([LineType value])
```

### <a name="parameters---lineleft"></a><span data-ttu-id="f9f72-668">パラメーター - lineLeft</span><span class="sxs-lookup"><span data-stu-id="f9f72-668">Parameters - lineLeft</span></span>

<span data-ttu-id="f9f72-669">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-669">value</span></span>  

### <a name="return-value---lineleft"></a><span data-ttu-id="f9f72-670">戻り値 - lineLeft</span><span class="sxs-lookup"><span data-stu-id="f9f72-670">Return Value - lineLeft</span></span>

<span data-ttu-id="f9f72-671">左境界線として使用される線のタイプ。</span><span class="sxs-lookup"><span data-stu-id="f9f72-671">The type of line that is used as the left border.</span></span>

## <a name="method-lineright"></a><span data-ttu-id="f9f72-672">メソッド lineRight</span><span class="sxs-lookup"><span data-stu-id="f9f72-672">Method lineRight</span></span>

```xpp
public LineType lineRight([LineType value])
```

### <a name="parameters---lineright"></a><span data-ttu-id="f9f72-673">パラメーター - lineRight</span><span class="sxs-lookup"><span data-stu-id="f9f72-673">Parameters - lineRight</span></span>

<span data-ttu-id="f9f72-674">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-674">value</span></span>  

### <a name="return-value---lineright"></a><span data-ttu-id="f9f72-675">戻り値 - lineRight</span><span class="sxs-lookup"><span data-stu-id="f9f72-675">Return Value - lineRight</span></span>

## <a name="method-menuitemlabel"></a><span data-ttu-id="f9f72-676">メソッド menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="f9f72-676">Method menuItemLabel</span></span>

```xpp
public str menuItemLabel([str value])
```

### <a name="parameters---menuitemlabel"></a><span data-ttu-id="f9f72-677">パラメーター - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="f9f72-677">Parameters - menuItemLabel</span></span>

<span data-ttu-id="f9f72-678">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-678">value</span></span>  

### <a name="return-value---menuitemlabel"></a><span data-ttu-id="f9f72-679">戻り値 - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="f9f72-679">Return Value - menuItemLabel</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="f9f72-680">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="f9f72-680">Method menuItemName</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="f9f72-681">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="f9f72-681">Parameters - menuItemName</span></span>

<span data-ttu-id="f9f72-682">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-682">value</span></span>  

### <a name="return-value---menuitemname"></a><span data-ttu-id="f9f72-683">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="f9f72-683">Return Value - menuItemName</span></span>

## <a name="method-menuitemtype"></a><span data-ttu-id="f9f72-684">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="f9f72-684">Method menuItemType</span></span>

```xpp
public MenuItemType menuItemType([MenuItemType value])
```

### <a name="parameters---menuitemtype"></a><span data-ttu-id="f9f72-685">パラメーター - menuItemType</span><span class="sxs-lookup"><span data-stu-id="f9f72-685">Parameters - menuItemType</span></span>

<span data-ttu-id="f9f72-686">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-686">value</span></span>  

### <a name="return-value---menuitemtype"></a><span data-ttu-id="f9f72-687">戻り値 - menuItemType</span><span class="sxs-lookup"><span data-stu-id="f9f72-687">Return Value - menuItemType</span></span>

## <a name="method-modelfieldname"></a><span data-ttu-id="f9f72-688">メソッド modelFieldName</span><span class="sxs-lookup"><span data-stu-id="f9f72-688">Method modelFieldName</span></span>

```xpp
public str modelFieldName([str value])
```

### <a name="parameters---modelfieldname"></a><span data-ttu-id="f9f72-689">パラメーター - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="f9f72-689">Parameters - modelFieldName</span></span>

<span data-ttu-id="f9f72-690">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-690">value</span></span>  

### <a name="return-value---modelfieldname"></a><span data-ttu-id="f9f72-691">戻り値 - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="f9f72-691">Return Value - modelFieldName</span></span>

## <a name="method-name"></a><span data-ttu-id="f9f72-692">メソッド名</span><span class="sxs-lookup"><span data-stu-id="f9f72-692">Method name</span></span>

<span data-ttu-id="f9f72-693">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-693">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="f9f72-694">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="f9f72-694">Parameters - name</span></span>

<span data-ttu-id="f9f72-695">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-695">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="f9f72-696">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="f9f72-696">Return Value - name</span></span>

<span data-ttu-id="f9f72-697">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="f9f72-697">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="f9f72-698">備考 - name</span><span class="sxs-lookup"><span data-stu-id="f9f72-698">Remarks - name</span></span>

<span data-ttu-id="f9f72-699">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9f72-699">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="f9f72-700">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="f9f72-700">Begins with a letter.</span></span>
-   <span data-ttu-id="f9f72-701">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="f9f72-701">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="f9f72-702">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="f9f72-702">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="f9f72-703">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="f9f72-703">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="f9f72-704">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="f9f72-704">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-numberoflines"></a><span data-ttu-id="f9f72-705">メソッド numberOfLines</span><span class="sxs-lookup"><span data-stu-id="f9f72-705">Method numberOfLines</span></span>

```xpp
public int numberOfLines(int height100mm)
```

### <a name="parameters---numberoflines"></a><span data-ttu-id="f9f72-706">パラメーター - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="f9f72-706">Parameters - numberOfLines</span></span>

<span data-ttu-id="f9f72-707">height100mm</span><span class="sxs-lookup"><span data-stu-id="f9f72-707">height100mm</span></span>  

### <a name="return-value---numberoflines"></a><span data-ttu-id="f9f72-708">戻り値 - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="f9f72-708">Return Value - numberOfLines</span></span>

## <a name="method-position"></a><span data-ttu-id="f9f72-709">メソッドの位置</span><span class="sxs-lookup"><span data-stu-id="f9f72-709">Method position</span></span>

```xpp
public int position([int value])
```

### <a name="parameters---position"></a><span data-ttu-id="f9f72-710">パラメーター - position</span><span class="sxs-lookup"><span data-stu-id="f9f72-710">Parameters - position</span></span>

<span data-ttu-id="f9f72-711">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-711">value</span></span>  

### <a name="return-value---position"></a><span data-ttu-id="f9f72-712">戻り値 - position</span><span class="sxs-lookup"><span data-stu-id="f9f72-712">Return Value - position</span></span>

## <a name="method-previewinfo"></a><span data-ttu-id="f9f72-713">メソッド previewInfo</span><span class="sxs-lookup"><span data-stu-id="f9f72-713">Method previewInfo</span></span>

```xpp
public str previewInfo(str string)
```

### <a name="parameters---previewinfo"></a><span data-ttu-id="f9f72-714">パラメーター - previewInfo</span><span class="sxs-lookup"><span data-stu-id="f9f72-714">Parameters - previewInfo</span></span>

<span data-ttu-id="f9f72-715">文字列</span><span class="sxs-lookup"><span data-stu-id="f9f72-715">string</span></span>  

### <a name="return-value---previewinfo"></a><span data-ttu-id="f9f72-716">戻り値 - previewInfo</span><span class="sxs-lookup"><span data-stu-id="f9f72-716">Return Value - previewInfo</span></span>

## <a name="method-previewxcompensation100mm"></a><span data-ttu-id="f9f72-717">メソッド previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="f9f72-717">Method previewXCompensation100mm</span></span>

```xpp
public int previewXCompensation100mm(str string)
```

### <a name="parameters---previewxcompensation100mm"></a><span data-ttu-id="f9f72-718">パラメーター - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="f9f72-718">Parameters - previewXCompensation100mm</span></span>

<span data-ttu-id="f9f72-719">文字列</span><span class="sxs-lookup"><span data-stu-id="f9f72-719">string</span></span>  

### <a name="return-value---previewxcompensation100mm"></a><span data-ttu-id="f9f72-720">戻り値 - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="f9f72-720">Return Value - previewXCompensation100mm</span></span>

## <a name="method-right100mm"></a><span data-ttu-id="f9f72-721">メソッド right100mm</span><span class="sxs-lookup"><span data-stu-id="f9f72-721">Method right100mm</span></span>

```xpp
public int right100mm()
```

### <a name="return-value---right100mm"></a><span data-ttu-id="f9f72-722">戻り値 - right100mm</span><span class="sxs-lookup"><span data-stu-id="f9f72-722">Return Value - right100mm</span></span>

## <a name="method-right100mminclborder"></a><span data-ttu-id="f9f72-723">メソッド right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f9f72-723">Method right100mmInclBorder</span></span>

```xpp
public int right100mmInclBorder()
```

### <a name="return-value---right100mminclborder"></a><span data-ttu-id="f9f72-724">戻り値 - right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f9f72-724">Return Value - right100mmInclBorder</span></span>

## <a name="method-rightmarginandframe"></a><span data-ttu-id="f9f72-725">メソッド rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="f9f72-725">Method rightMarginAndFrame</span></span>

```xpp
public int rightMarginAndFrame()
```

### <a name="return-value---rightmarginandframe"></a><span data-ttu-id="f9f72-726">戻り値 - rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="f9f72-726">Return Value - rightMarginAndFrame</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="f9f72-727">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-727">Method rightMarginMode</span></span>

```xpp
public int rightMarginMode([int value])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="f9f72-728">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-728">Parameters - rightMarginMode</span></span>

<span data-ttu-id="f9f72-729">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-729">value</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="f9f72-730">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-730">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginstr"></a><span data-ttu-id="f9f72-731">メソッド rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-731">Method rightMarginStr</span></span>

```xpp
public str rightMarginStr([str value])
```

### <a name="parameters---rightmarginstr"></a><span data-ttu-id="f9f72-732">パラメーター - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-732">Parameters - rightMarginStr</span></span>

<span data-ttu-id="f9f72-733">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-733">value</span></span>  

### <a name="return-value---rightmarginstr"></a><span data-ttu-id="f9f72-734">戻り値 - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-734">Return Value - rightMarginStr</span></span>

## <a name="method-rightmarginunit"></a><span data-ttu-id="f9f72-735">メソッド rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-735">Method rightMarginUnit</span></span>

```xpp
public Units rightMarginUnit([Units value])
```

### <a name="parameters---rightmarginunit"></a><span data-ttu-id="f9f72-736">パラメーター - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-736">Parameters - rightMarginUnit</span></span>

<span data-ttu-id="f9f72-737">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-737">value</span></span>  

### <a name="return-value---rightmarginunit"></a><span data-ttu-id="f9f72-738">戻り値 - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-738">Return Value - rightMarginUnit</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="f9f72-739">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-739">Method rightMarginValue</span></span>

```xpp
public Real rightMarginValue([Real value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="f9f72-740">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-740">Parameters - rightMarginValue</span></span>

<span data-ttu-id="f9f72-741">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-741">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="f9f72-742">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-742">Return Value - rightMarginValue</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="f9f72-743">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="f9f72-743">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="f9f72-744">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="f9f72-744">Parameters - securityKey</span></span>

<span data-ttu-id="f9f72-745">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-745">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="f9f72-746">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="f9f72-746">Return Value - securityKey</span></span>

## <a name="method-setheightgettext"></a><span data-ttu-id="f9f72-747">メソッド setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="f9f72-747">Method setHeightGetText</span></span>

```xpp
public str setHeightGetText(int lines, str string)
```

### <a name="parameters---setheightgettext"></a><span data-ttu-id="f9f72-748">パラメーター - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="f9f72-748">Parameters - setHeightGetText</span></span>

<span data-ttu-id="f9f72-749">明細行</span><span class="sxs-lookup"><span data-stu-id="f9f72-749">lines</span></span>  

<!-- -->

<span data-ttu-id="f9f72-750">文字列</span><span class="sxs-lookup"><span data-stu-id="f9f72-750">string</span></span>  

### <a name="return-value---setheightgettext"></a><span data-ttu-id="f9f72-751">戻り値 - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="f9f72-751">Return Value - setHeightGetText</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="f9f72-752">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="f9f72-752">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="f9f72-753">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="f9f72-753">Parameters - showLabel</span></span>

<span data-ttu-id="f9f72-754">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-754">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="f9f72-755">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="f9f72-755">Return Value - showLabel</span></span>

## <a name="method-table"></a><span data-ttu-id="f9f72-756">メソッド table</span><span class="sxs-lookup"><span data-stu-id="f9f72-756">Method table</span></span>

<span data-ttu-id="f9f72-757">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-757">Gets or sets the table ID associated with the object.</span></span>

```xpp
public TableId table([TableId value])
```

### <a name="parameters---table"></a><span data-ttu-id="f9f72-758">パラメーター - table</span><span class="sxs-lookup"><span data-stu-id="f9f72-758">Parameters - table</span></span>

<span data-ttu-id="f9f72-759">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-759">value</span></span>  

### <a name="return-value---table"></a><span data-ttu-id="f9f72-760">戻り値 - toBlob</span><span class="sxs-lookup"><span data-stu-id="f9f72-760">Return Value - table</span></span>

<span data-ttu-id="f9f72-761">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="f9f72-761">The current value of the table ID associated with the object.</span></span>

## <a name="method-thickness"></a><span data-ttu-id="f9f72-762">メソッド thickness</span><span class="sxs-lookup"><span data-stu-id="f9f72-762">Method thickness</span></span>

```xpp
public LineThickness thickness([LineThickness value])
```

### <a name="parameters---thickness"></a><span data-ttu-id="f9f72-763">パラメーター - thickness</span><span class="sxs-lookup"><span data-stu-id="f9f72-763">Parameters - thickness</span></span>

<span data-ttu-id="f9f72-764">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-764">value</span></span>  

### <a name="return-value---thickness"></a><span data-ttu-id="f9f72-765">戻り値 - thickness</span><span class="sxs-lookup"><span data-stu-id="f9f72-765">Return Value - thickness</span></span>

## <a name="method-top100mm"></a><span data-ttu-id="f9f72-766">メソッド top100mm</span><span class="sxs-lookup"><span data-stu-id="f9f72-766">Method top100mm</span></span>

```xpp
public int top100mm([int topExclBorder])
```

### <a name="parameters---top100mm"></a><span data-ttu-id="f9f72-767">パラメーター - top100mm</span><span class="sxs-lookup"><span data-stu-id="f9f72-767">Parameters - top100mm</span></span>

<span data-ttu-id="f9f72-768">topExclBorder</span><span class="sxs-lookup"><span data-stu-id="f9f72-768">topExclBorder</span></span>  

### <a name="return-value---top100mm"></a><span data-ttu-id="f9f72-769">戻り値 - top100mm</span><span class="sxs-lookup"><span data-stu-id="f9f72-769">Return Value - top100mm</span></span>

## <a name="method-top100mminclborder"></a><span data-ttu-id="f9f72-770">メソッド top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f9f72-770">Method top100mmInclBorder</span></span>

```xpp
public int top100mmInclBorder([int topInclBorder])
```

### <a name="parameters---top100mminclborder"></a><span data-ttu-id="f9f72-771">パラメーター - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f9f72-771">Parameters - top100mmInclBorder</span></span>

<span data-ttu-id="f9f72-772">topInclBorder</span><span class="sxs-lookup"><span data-stu-id="f9f72-772">topInclBorder</span></span>  

### <a name="return-value---top100mminclborder"></a><span data-ttu-id="f9f72-773">戻り値 - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f9f72-773">Return Value - top100mmInclBorder</span></span>

## <a name="method-topmarginandframe"></a><span data-ttu-id="f9f72-774">メソッド topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="f9f72-774">Method topMarginAndFrame</span></span>

```xpp
public int topMarginAndFrame()
```

### <a name="return-value---topmarginandframe"></a><span data-ttu-id="f9f72-775">戻り値 - topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="f9f72-775">Return Value - topMarginAndFrame</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="f9f72-776">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-776">Method topMarginMode</span></span>

```xpp
public int topMarginMode([int value])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="f9f72-777">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-777">Parameters - topMarginMode</span></span>

<span data-ttu-id="f9f72-778">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-778">value</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="f9f72-779">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-779">Return Value - topMarginMode</span></span>

## <a name="method-topmarginstr"></a><span data-ttu-id="f9f72-780">メソッド topMarginStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-780">Method topMarginStr</span></span>

```xpp
public str topMarginStr([str value])
```

### <a name="parameters---topmarginstr"></a><span data-ttu-id="f9f72-781">パラメーター - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-781">Parameters - topMarginStr</span></span>

<span data-ttu-id="f9f72-782">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-782">value</span></span>  

### <a name="return-value---topmarginstr"></a><span data-ttu-id="f9f72-783">戻り値 - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-783">Return Value - topMarginStr</span></span>

## <a name="method-topmarginunit"></a><span data-ttu-id="f9f72-784">メソッド topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-784">Method topMarginUnit</span></span>

```xpp
public Units topMarginUnit([Units value])
```

### <a name="parameters---topmarginunit"></a><span data-ttu-id="f9f72-785">パラメーター - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-785">Parameters - topMarginUnit</span></span>

<span data-ttu-id="f9f72-786">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-786">value</span></span>  

### <a name="return-value---topmarginunit"></a><span data-ttu-id="f9f72-787">戻り値 - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-787">Return Value - topMarginUnit</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="f9f72-788">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-788">Method topMarginValue</span></span>

```xpp
public Real topMarginValue([Real value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="f9f72-789">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-789">Parameters - topMarginValue</span></span>

<span data-ttu-id="f9f72-790">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-790">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="f9f72-791">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-791">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="f9f72-792">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-792">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="f9f72-793">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-793">Parameters - topMode</span></span>

<span data-ttu-id="f9f72-794">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-794">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="f9f72-795">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-795">Return Value - topMode</span></span>

## <a name="method-topstr"></a><span data-ttu-id="f9f72-796">メソッド topStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-796">Method topStr</span></span>

```xpp
public str topStr([str value])
```

### <a name="parameters---topstr"></a><span data-ttu-id="f9f72-797">パラメーター - topStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-797">Parameters - topStr</span></span>

<span data-ttu-id="f9f72-798">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-798">value</span></span>  

### <a name="return-value---topstr"></a><span data-ttu-id="f9f72-799">戻り値 - topStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-799">Return Value - topStr</span></span>

## <a name="method-topunit"></a><span data-ttu-id="f9f72-800">メソッド topUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-800">Method topUnit</span></span>

```xpp
public Units topUnit([Units value])
```

### <a name="parameters---topunit"></a><span data-ttu-id="f9f72-801">パラメーター - topUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-801">Parameters - topUnit</span></span>

<span data-ttu-id="f9f72-802">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-802">value</span></span>  

### <a name="return-value---topunit"></a><span data-ttu-id="f9f72-803">戻り値 - topUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-803">Return Value - topUnit</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="f9f72-804">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-804">Method topValue</span></span>

```xpp
public Real topValue([Real value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="f9f72-805">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-805">Parameters - topValue</span></span>

<span data-ttu-id="f9f72-806">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-806">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="f9f72-807">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-807">Return Value - topValue</span></span>

## <a name="method-underline"></a><span data-ttu-id="f9f72-808">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="f9f72-808">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="f9f72-809">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="f9f72-809">Parameters - underline</span></span>

<span data-ttu-id="f9f72-810">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-810">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="f9f72-811">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="f9f72-811">Return Value - underline</span></span>

## <a name="method-visible"></a><span data-ttu-id="f9f72-812">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="f9f72-812">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="f9f72-813">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="f9f72-813">Parameters - visible</span></span>

<span data-ttu-id="f9f72-814">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-814">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="f9f72-815">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="f9f72-815">Return Value - visible</span></span>

## <a name="method-webmenuitemname"></a><span data-ttu-id="f9f72-816">メソッド webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="f9f72-816">Method webMenuItemName</span></span>

```xpp
public str webMenuItemName([str value])
```

### <a name="parameters---webmenuitemname"></a><span data-ttu-id="f9f72-817">パラメーター - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="f9f72-817">Parameters - webMenuItemName</span></span>

<span data-ttu-id="f9f72-818">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-818">value</span></span>  

### <a name="return-value---webmenuitemname"></a><span data-ttu-id="f9f72-819">戻り値 - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="f9f72-819">Return Value - webMenuItemName</span></span>

## <a name="method-webmenuitemtype"></a><span data-ttu-id="f9f72-820">メソッド webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="f9f72-820">Method webMenuItemType</span></span>

```xpp
public WebMenuItemType webMenuItemType([WebMenuItemType value])
```

### <a name="parameters---webmenuitemtype"></a><span data-ttu-id="f9f72-821">パラメーター - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="f9f72-821">Parameters - webMenuItemType</span></span>

<span data-ttu-id="f9f72-822">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-822">value</span></span>  

### <a name="return-value---webmenuitemtype"></a><span data-ttu-id="f9f72-823">戻り値 - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="f9f72-823">Return Value - webMenuItemType</span></span>

## <a name="method-webtarget"></a><span data-ttu-id="f9f72-824">メソッド webTarget</span><span class="sxs-lookup"><span data-stu-id="f9f72-824">Method webTarget</span></span>

```xpp
public str webTarget([str value])
```

### <a name="parameters---webtarget"></a><span data-ttu-id="f9f72-825">パラメーター - webTarget</span><span class="sxs-lookup"><span data-stu-id="f9f72-825">Parameters - webTarget</span></span>

<span data-ttu-id="f9f72-826">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-826">value</span></span>  

### <a name="return-value---webtarget"></a><span data-ttu-id="f9f72-827">戻り値 - webTarget</span><span class="sxs-lookup"><span data-stu-id="f9f72-827">Return Value - webTarget</span></span>

## <a name="method-width100mm"></a><span data-ttu-id="f9f72-828">メソッド width100mm</span><span class="sxs-lookup"><span data-stu-id="f9f72-828">Method width100mm</span></span>

```xpp
public int width100mm([int widthExclBorder])
```

### <a name="parameters---width100mm"></a><span data-ttu-id="f9f72-829">パラメーター - width100mm</span><span class="sxs-lookup"><span data-stu-id="f9f72-829">Parameters - width100mm</span></span>

<span data-ttu-id="f9f72-830">widthExclBorder</span><span class="sxs-lookup"><span data-stu-id="f9f72-830">widthExclBorder</span></span>  

### <a name="return-value---width100mm"></a><span data-ttu-id="f9f72-831">戻り値 - width100mm</span><span class="sxs-lookup"><span data-stu-id="f9f72-831">Return Value - width100mm</span></span>

## <a name="method-width100mminclborder"></a><span data-ttu-id="f9f72-832">メソッド width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f9f72-832">Method width100mmInclBorder</span></span>

```xpp
public int width100mmInclBorder([int widthInclBorder])
```

### <a name="parameters---width100mminclborder"></a><span data-ttu-id="f9f72-833">パラメーター - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f9f72-833">Parameters - width100mmInclBorder</span></span>

<span data-ttu-id="f9f72-834">widthInclBorder</span><span class="sxs-lookup"><span data-stu-id="f9f72-834">widthInclBorder</span></span>  

### <a name="return-value---width100mminclborder"></a><span data-ttu-id="f9f72-835">戻り値 - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="f9f72-835">Return Value - width100mmInclBorder</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="f9f72-836">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-836">Method widthMode</span></span>

<span data-ttu-id="f9f72-837">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-837">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="f9f72-838">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-838">Parameters - widthMode</span></span>

<span data-ttu-id="f9f72-839">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-839">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="f9f72-840">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-840">Return Value - widthMode</span></span>

<span data-ttu-id="f9f72-841">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f9f72-841">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="f9f72-842">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="f9f72-842">Remarks - widthMode</span></span>

<span data-ttu-id="f9f72-843">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="f9f72-843">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="f9f72-844">モード。</span><span class="sxs-lookup"><span data-stu-id="f9f72-844">Mode.</span></span>         | <span data-ttu-id="f9f72-845">幅計算。</span><span class="sxs-lookup"><span data-stu-id="f9f72-845">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9f72-846">正確。</span><span class="sxs-lookup"><span data-stu-id="f9f72-846">Exact.</span></span>        | <span data-ttu-id="f9f72-847">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="f9f72-847">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="f9f72-848">自動。</span><span class="sxs-lookup"><span data-stu-id="f9f72-848">Auto.</span></span>         | <span data-ttu-id="f9f72-849">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="f9f72-849">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="f9f72-850">列の幅。</span><span class="sxs-lookup"><span data-stu-id="f9f72-850">Column width.</span></span> | <span data-ttu-id="f9f72-851">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="f9f72-851">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="f9f72-852">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="f9f72-852">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthofstring100mm"></a><span data-ttu-id="f9f72-853">メソッド widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="f9f72-853">Method widthOfString100mm</span></span>

```xpp
public int widthOfString100mm(str string)
```

### <a name="parameters---widthofstring100mm"></a><span data-ttu-id="f9f72-854">パラメーター - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="f9f72-854">Parameters - widthOfString100mm</span></span>

<span data-ttu-id="f9f72-855">文字列</span><span class="sxs-lookup"><span data-stu-id="f9f72-855">string</span></span>  

### <a name="return-value---widthofstring100mm"></a><span data-ttu-id="f9f72-856">戻り値 - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="f9f72-856">Return Value - widthOfString100mm</span></span>

## <a name="method-widthstr"></a><span data-ttu-id="f9f72-857">メソッド widthStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-857">Method widthStr</span></span>

```xpp
public str widthStr([str value])
```

### <a name="parameters---widthstr"></a><span data-ttu-id="f9f72-858">パラメーター - widthStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-858">Parameters - widthStr</span></span>

<span data-ttu-id="f9f72-859">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-859">value</span></span>  

### <a name="return-value---widthstr"></a><span data-ttu-id="f9f72-860">戻り値 - widthStr</span><span class="sxs-lookup"><span data-stu-id="f9f72-860">Return Value - widthStr</span></span>

## <a name="method-widthunit"></a><span data-ttu-id="f9f72-861">メソッド widthUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-861">Method widthUnit</span></span>

```xpp
public Units widthUnit([Units value])
```

### <a name="parameters---widthunit"></a><span data-ttu-id="f9f72-862">パラメーター - widthUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-862">Parameters - widthUnit</span></span>

<span data-ttu-id="f9f72-863">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-863">value</span></span>  

### <a name="return-value---widthunit"></a><span data-ttu-id="f9f72-864">戻り値 - widthUnit</span><span class="sxs-lookup"><span data-stu-id="f9f72-864">Return Value - widthUnit</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="f9f72-865">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-865">Method widthValue</span></span>

<span data-ttu-id="f9f72-866">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-866">Gets or sets the width of the control.</span></span>

```xpp
public Real widthValue([Real value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="f9f72-867">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-867">Parameters - widthValue</span></span>

<span data-ttu-id="f9f72-868">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-868">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="f9f72-869">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-869">Return Value - widthValue</span></span>

<span data-ttu-id="f9f72-870">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="f9f72-870">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="f9f72-871">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="f9f72-871">Remarks - widthValue</span></span>

<span data-ttu-id="f9f72-872">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-872">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-top"></a><span data-ttu-id="f9f72-873">メソッド top</span><span class="sxs-lookup"><span data-stu-id="f9f72-873">Method top</span></span>

```xpp
public void top(Real value, Units unit)
```

### <a name="parameters---top"></a><span data-ttu-id="f9f72-874">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="f9f72-874">Parameters - top</span></span>

<span data-ttu-id="f9f72-875">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-875">value</span></span>  

<!-- -->

<span data-ttu-id="f9f72-876">単位</span><span class="sxs-lookup"><span data-stu-id="f9f72-876">unit</span></span>  

## <a name="method-bottommargin"></a><span data-ttu-id="f9f72-877">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="f9f72-877">Method bottomMargin</span></span>

```xpp
public void bottomMargin(Real value, Units unit)
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="f9f72-878">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="f9f72-878">Parameters - bottomMargin</span></span>

<span data-ttu-id="f9f72-879">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-879">value</span></span>  

<!-- -->

<span data-ttu-id="f9f72-880">単位</span><span class="sxs-lookup"><span data-stu-id="f9f72-880">unit</span></span>  

## <a name="method-height"></a><span data-ttu-id="f9f72-881">メソッド height</span><span class="sxs-lookup"><span data-stu-id="f9f72-881">Method height</span></span>

<span data-ttu-id="f9f72-882">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-882">Gets or sets the height of the control.</span></span>

```xpp
public void height(Real value, Units unit)
```

### <a name="parameters---height"></a><span data-ttu-id="f9f72-883">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="f9f72-883">Parameters - height</span></span>

<span data-ttu-id="f9f72-884">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-884">value</span></span>  

<!-- -->

<span data-ttu-id="f9f72-885">単位</span><span class="sxs-lookup"><span data-stu-id="f9f72-885">unit</span></span>  

### <a name="remarks---height"></a><span data-ttu-id="f9f72-886">備考 - height</span><span class="sxs-lookup"><span data-stu-id="f9f72-886">Remarks - height</span></span>

<span data-ttu-id="f9f72-887">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f9f72-887">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="f9f72-888">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="f9f72-888">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="f9f72-889">モード。</span><span class="sxs-lookup"><span data-stu-id="f9f72-889">Mode.</span></span>            | <span data-ttu-id="f9f72-890">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="f9f72-890">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9f72-891">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="f9f72-891">-1 Exact.</span></span>        | <span data-ttu-id="f9f72-892">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f9f72-892">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="f9f72-893">0 自動。</span><span class="sxs-lookup"><span data-stu-id="f9f72-893">0 Auto.</span></span>          | <span data-ttu-id="f9f72-894">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="f9f72-894">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="f9f72-895">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="f9f72-895">1 Column height.</span></span> | <span data-ttu-id="f9f72-896">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="f9f72-896">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="f9f72-897">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="f9f72-897">The height and height calculation mode can be set separately.</span></span>

## <a name="method-show"></a><span data-ttu-id="f9f72-898">メソッド show</span><span class="sxs-lookup"><span data-stu-id="f9f72-898">Method show</span></span>

```xpp
public void show()
```

## <a name="method-labelwidth"></a><span data-ttu-id="f9f72-899">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="f9f72-899">Method labelWidth</span></span>

```xpp
public void labelWidth(Real value, Units unit)
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="f9f72-900">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="f9f72-900">Parameters - labelWidth</span></span>

<span data-ttu-id="f9f72-901">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-901">value</span></span>  

<!-- -->

<span data-ttu-id="f9f72-902">単位</span><span class="sxs-lookup"><span data-stu-id="f9f72-902">unit</span></span>  

## <a name="method-leftmargin"></a><span data-ttu-id="f9f72-903">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="f9f72-903">Method leftMargin</span></span>

```xpp
public void leftMargin(Real value, Units unit)
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="f9f72-904">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="f9f72-904">Parameters - leftMargin</span></span>

<span data-ttu-id="f9f72-905">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-905">value</span></span>  

<!-- -->

<span data-ttu-id="f9f72-906">単位</span><span class="sxs-lookup"><span data-stu-id="f9f72-906">unit</span></span>  

## <a name="method-topmargin"></a><span data-ttu-id="f9f72-907">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="f9f72-907">Method topMargin</span></span>

```xpp
public void topMargin(Real value, Units unit)
```

### <a name="parameters---topmargin"></a><span data-ttu-id="f9f72-908">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="f9f72-908">Parameters - topMargin</span></span>

<span data-ttu-id="f9f72-909">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-909">value</span></span>  

<!-- -->

<span data-ttu-id="f9f72-910">単位</span><span class="sxs-lookup"><span data-stu-id="f9f72-910">unit</span></span>  

## <a name="method-width"></a><span data-ttu-id="f9f72-911">メソッド width</span><span class="sxs-lookup"><span data-stu-id="f9f72-911">Method width</span></span>

<span data-ttu-id="f9f72-912">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f9f72-912">Gets or sets the width of the control.</span></span>

```xpp
public void width(Real value, Units unit)
```

### <a name="parameters---width"></a><span data-ttu-id="f9f72-913">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="f9f72-913">Parameters - width</span></span>

<span data-ttu-id="f9f72-914">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-914">value</span></span>  

<!-- -->

<span data-ttu-id="f9f72-915">単位</span><span class="sxs-lookup"><span data-stu-id="f9f72-915">unit</span></span>  

### <a name="remarks---width"></a><span data-ttu-id="f9f72-916">備考 - width</span><span class="sxs-lookup"><span data-stu-id="f9f72-916">Remarks - width</span></span>

<span data-ttu-id="f9f72-917">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f9f72-917">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="f9f72-918">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="f9f72-918">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="f9f72-919">モード。</span><span class="sxs-lookup"><span data-stu-id="f9f72-919">Mode.</span></span>           | <span data-ttu-id="f9f72-920">幅計算。</span><span class="sxs-lookup"><span data-stu-id="f9f72-920">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9f72-921">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="f9f72-921">-1 Exact.</span></span>       | <span data-ttu-id="f9f72-922">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="f9f72-922">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="f9f72-923">0 自動。</span><span class="sxs-lookup"><span data-stu-id="f9f72-923">0 Auto.</span></span>         | <span data-ttu-id="f9f72-924">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="f9f72-924">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="f9f72-925">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="f9f72-925">1 Column width.</span></span> | <span data-ttu-id="f9f72-926">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="f9f72-926">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="f9f72-927">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="f9f72-927">The width and width calculation mode can be set separately.</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="f9f72-928">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="f9f72-928">Method rightMargin</span></span>

```xpp
public void rightMargin(Real value, Units unit)
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="f9f72-929">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="f9f72-929">Parameters - rightMargin</span></span>

<span data-ttu-id="f9f72-930">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-930">value</span></span>  

<!-- -->

<span data-ttu-id="f9f72-931">単位</span><span class="sxs-lookup"><span data-stu-id="f9f72-931">unit</span></span>  

## <a name="method-left"></a><span data-ttu-id="f9f72-932">メソッド left</span><span class="sxs-lookup"><span data-stu-id="f9f72-932">Method left</span></span>

```xpp
public void left(Real value, Units unit)
```

### <a name="parameters---left"></a><span data-ttu-id="f9f72-933">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="f9f72-933">Parameters - left</span></span>

<span data-ttu-id="f9f72-934">値</span><span class="sxs-lookup"><span data-stu-id="f9f72-934">value</span></span>  

<!-- -->

<span data-ttu-id="f9f72-935">単位</span><span class="sxs-lookup"><span data-stu-id="f9f72-935">unit</span></span>  

## <a name="method-hide"></a><span data-ttu-id="f9f72-936">メソッド hide</span><span class="sxs-lookup"><span data-stu-id="f9f72-936">Method hide</span></span>

```xpp
public void hide()
```

