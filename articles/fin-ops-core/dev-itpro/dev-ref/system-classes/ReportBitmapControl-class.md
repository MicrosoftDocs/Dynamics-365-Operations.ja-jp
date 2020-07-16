---
title: ReportBitmapControl クラス
description: このトピックでは、ReportBitmapControl クラスについて説明します。
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
ms.openlocfilehash: f7d98eaf0a20152aa538abf1b94a7a7a6bbee3a0
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502845"
---
# <a name="class-reportbitmapcontrol"></a><span data-ttu-id="8974d-103">クラス ReportBitmapControl</span><span class="sxs-lookup"><span data-stu-id="8974d-103">Class ReportBitmapControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ReportBitmapControl extends ReportControl
```

<span data-ttu-id="8974d-104">ReportBitmapControl クラスは、X++ コードおよびメタデータの作成、読み取り、更新、および削除を行います。</span><span class="sxs-lookup"><span data-stu-id="8974d-104">The ReportBitmapControl class creates, reads, updates, and deletes X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="8974d-105">備考</span><span class="sxs-lookup"><span data-stu-id="8974d-105">Remarks</span></span>

<span data-ttu-id="8974d-106">この API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8974d-106">You must have access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="8974d-107">例</span><span class="sxs-lookup"><span data-stu-id="8974d-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="8974d-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="8974d-108">Methods</span></span>

| <span data-ttu-id="8974d-109">方法</span><span class="sxs-lookup"><span data-stu-id="8974d-109">Method</span></span>                                                                   | <span data-ttu-id="8974d-110">説明</span><span class="sxs-lookup"><span data-stu-id="8974d-110">Description</span></span>                                                                                                                               |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8974d-111">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-111">public int alignment(\[int value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="8974d-112">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-112">public int arrayIndex(\[int value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="8974d-113">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-113">public boolean autoDeclaration(\[boolean value\])</span></span>                        | <span data-ttu-id="8974d-114">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-114">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                        |
| <span data-ttu-id="8974d-115">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-115">public int backStyle(\[int value\])</span></span>                                      | <span data-ttu-id="8974d-116">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-116">Determines whether the control background can be transparent.</span></span>                                                                            |
| <span data-ttu-id="8974d-117">public int bottomMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="8974d-117">public int bottomMarginAndFrame()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="8974d-118">public int bottomMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-118">public int bottomMarginMode(\[int value\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="8974d-119">public str bottomMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-119">public str bottomMarginStr(\[str value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="8974d-120">public Units bottomMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-120">public Units bottomMarginUnit(\[Units value\])</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="8974d-121">public Real bottomMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-121">public Real bottomMarginValue(\[Real value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="8974d-122">public int changeLabelCase(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-122">public int changeLabelCase(\[int value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="8974d-123">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-123">public int colorScheme(\[int value\])</span></span>                                    | <span data-ttu-id="8974d-124">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-124">Gets or sets the color scheme of the control.</span></span>                                                                                             |
| <span data-ttu-id="8974d-125">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-125">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="8974d-126">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-126">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                       |
| <span data-ttu-id="8974d-127">public ReportFieldType controlType()</span><span class="sxs-lookup"><span data-stu-id="8974d-127">public ReportFieldType controlType()</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="8974d-128">public str cssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-128">public str cssClass(\[str value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="8974d-129">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-129">public FieldId dataField(\[FieldId value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="8974d-130">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-130">public str dataMethod(\[str value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="8974d-131">public int delete()</span><span class="sxs-lookup"><span data-stu-id="8974d-131">public int delete()</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="8974d-132">public str effectiveFont()</span><span class="sxs-lookup"><span data-stu-id="8974d-132">public str effectiveFont()</span></span>                                               |                                                                                                                                           |
| <span data-ttu-id="8974d-133">public str fontInfoPrinter()</span><span class="sxs-lookup"><span data-stu-id="8974d-133">public str fontInfoPrinter()</span></span>                                             |                                                                                                                                           |
| <span data-ttu-id="8974d-134">public int fontInfoPrinterAscent()</span><span class="sxs-lookup"><span data-stu-id="8974d-134">public int fontInfoPrinterAscent()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="8974d-135">public int fontInfoPrinterDescent()</span><span class="sxs-lookup"><span data-stu-id="8974d-135">public int fontInfoPrinterDescent()</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="8974d-136">public int fontInfoPrinterExtLead()</span><span class="sxs-lookup"><span data-stu-id="8974d-136">public int fontInfoPrinterExtLead()</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="8974d-137">public int fontInfoPrinterHeight()</span><span class="sxs-lookup"><span data-stu-id="8974d-137">public int fontInfoPrinterHeight()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="8974d-138">public int fontInfoPrinterIntLead()</span><span class="sxs-lookup"><span data-stu-id="8974d-138">public int fontInfoPrinterIntLead()</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="8974d-139">public str fontInfoScreen()</span><span class="sxs-lookup"><span data-stu-id="8974d-139">public str fontInfoScreen()</span></span>                                              |                                                                                                                                           |
| <span data-ttu-id="8974d-140">public int fontInfoScreenAscent()</span><span class="sxs-lookup"><span data-stu-id="8974d-140">public int fontInfoScreenAscent()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="8974d-141">public int fontInfoScreenDescent()</span><span class="sxs-lookup"><span data-stu-id="8974d-141">public int fontInfoScreenDescent()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="8974d-142">public int fontInfoScreenExtLead()</span><span class="sxs-lookup"><span data-stu-id="8974d-142">public int fontInfoScreenExtLead()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="8974d-143">public int fontInfoScreenHeight()</span><span class="sxs-lookup"><span data-stu-id="8974d-143">public int fontInfoScreenHeight()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="8974d-144">public int fontInfoScreenIntLead()</span><span class="sxs-lookup"><span data-stu-id="8974d-144">public int fontInfoScreenIntLead()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="8974d-145">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-145">public int foregroundColor(\[int value\])</span></span>                                | <span data-ttu-id="8974d-146">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-146">Gets or sets the text color for the control to use.</span></span>                                                                                       |
| <span data-ttu-id="8974d-147">public int height100mm(\[int heightExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="8974d-147">public int height100mm(\[int heightExclBorder\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="8974d-148">public int height100mmInclBorder(\[int heightInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="8974d-148">public int height100mmInclBorder(\[int heightInclBorder\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="8974d-149">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-149">public int heightMode(\[int value\])</span></span>                                     | <span data-ttu-id="8974d-150">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-150">Gets or sets a calculation mode for the height of the control.</span></span>                                                                            |
| <span data-ttu-id="8974d-151">public int heightOfWordWrappedString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="8974d-151">public int heightOfWordWrappedString100mm(str string)</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="8974d-152">public str heightStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-152">public str heightStr(\[str value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="8974d-153">public Units heightUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-153">public Units heightUnit(\[Units value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="8974d-154">public Real heightValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-154">public Real heightValue(\[Real value\])</span></span>                                  | <span data-ttu-id="8974d-155">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-155">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="8974d-156">public str imageName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-156">public str imageName(\[str value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="8974d-157">public int imageResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-157">public int imageResource(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="8974d-158">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-158">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="8974d-159">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-159">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="8974d-160">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-160">public int labelBold(\[int value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="8974d-161">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-161">public int labelCharacterSet(\[int value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="8974d-162">public str labelCssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-162">public str labelCssClass(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="8974d-163">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-163">public str labelFont(\[str value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="8974d-164">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-164">public int labelFontSize(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="8974d-165">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-165">public boolean labelItalic(\[boolean value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="8974d-166">public LineType labelLineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-166">public LineType labelLineBelow(\[LineType value\])</span></span>                       |                                                                                                                                           |
| <span data-ttu-id="8974d-167">public LineThickness labelLineThickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-167">public LineThickness labelLineThickness(\[LineThickness value\])</span></span>         |                                                                                                                                           |
| <span data-ttu-id="8974d-168">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-168">public int labelPosition(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="8974d-169">public int labelTabLeader(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-169">public int labelTabLeader(\[int value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="8974d-170">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-170">public boolean labelUnderline(\[boolean value\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="8974d-171">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-171">public int labelWidthMode(\[int value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="8974d-172">public str labelWidthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-172">public str labelWidthStr(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="8974d-173">public Units labelWidthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-173">public Units labelWidthUnit(\[Units value\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="8974d-174">public Real labelWidthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-174">public Real labelWidthValue(\[Real value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="8974d-175">public int left100mm(\[int leftExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="8974d-175">public int left100mm(\[int leftExclBorder\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="8974d-176">public int left100mmInclBorder(\[int leftInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="8974d-176">public int left100mmInclBorder(\[int leftInclBorder\])</span></span>                   |                                                                                                                                           |
| <span data-ttu-id="8974d-177">public int leftMarginAnFrame()</span><span class="sxs-lookup"><span data-stu-id="8974d-177">public int leftMarginAnFrame()</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="8974d-178">public int leftMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-178">public int leftMarginMode(\[int value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="8974d-179">public str leftMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-179">public str leftMarginStr(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="8974d-180">public Units leftMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-180">public Units leftMarginUnit(\[Units value\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="8974d-181">public Real leftMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-181">public Real leftMarginValue(\[Real value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="8974d-182">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-182">public int leftMode(\[int value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="8974d-183">public str leftStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-183">public str leftStr(\[str value\])</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="8974d-184">public Units leftUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-184">public Units leftUnit(\[Units value\])</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="8974d-185">public Real leftValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-185">public Real leftValue(\[Real value\])</span></span>                                    |                                                                                                                                           |
| <span data-ttu-id="8974d-186">public LineType lineAbove(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-186">public LineType lineAbove(\[LineType value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="8974d-187">public LineType lineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-187">public LineType lineBelow(\[LineType value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="8974d-188">public LineType lineLeft(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-188">public LineType lineLeft(\[LineType value\])</span></span>                             | <span data-ttu-id="8974d-189">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-189">Gets or sets the type of line that is used as the left border of a section.</span></span>                                                               |
| <span data-ttu-id="8974d-190">public LineType lineRight(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-190">public LineType lineRight(\[LineType value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="8974d-191">public str menuItemLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-191">public str menuItemLabel(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="8974d-192">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-192">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="8974d-193">public MenuItemType menuItemType(\[MenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-193">public MenuItemType menuItemType(\[MenuItemType value\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="8974d-194">public str modelFieldName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-194">public str modelFieldName(\[str value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="8974d-195">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-195">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="8974d-196">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-196">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="8974d-197">public int numberOfLines(int height100mm)</span><span class="sxs-lookup"><span data-stu-id="8974d-197">public int numberOfLines(int height100mm)</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="8974d-198">public int position(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-198">public int position(\[int value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="8974d-199">public str previewInfo(str string)</span><span class="sxs-lookup"><span data-stu-id="8974d-199">public str previewInfo(str string)</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="8974d-200">public int previewXCompensation100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="8974d-200">public int previewXCompensation100mm(str string)</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="8974d-201">public boolean resizeBitmap(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-201">public boolean resizeBitmap(\[boolean value\])</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="8974d-202">public int right100mm()</span><span class="sxs-lookup"><span data-stu-id="8974d-202">public int right100mm()</span></span>                                                  |                                                                                                                                           |
| <span data-ttu-id="8974d-203">public int right100mmInclBorder()</span><span class="sxs-lookup"><span data-stu-id="8974d-203">public int right100mmInclBorder()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="8974d-204">public int rightMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="8974d-204">public int rightMarginAndFrame()</span></span>                                         |                                                                                                                                           |
| <span data-ttu-id="8974d-205">public int rightMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-205">public int rightMarginMode(\[int value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="8974d-206">public str rightMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-206">public str rightMarginStr(\[str value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="8974d-207">public Units rightMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-207">public Units rightMarginUnit(\[Units value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="8974d-208">public Real rightMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-208">public Real rightMarginValue(\[Real value\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="8974d-209">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-209">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                                           |
| <span data-ttu-id="8974d-210">public str setHeightGetText(int lines, str string)</span><span class="sxs-lookup"><span data-stu-id="8974d-210">public str setHeightGetText(int lines, str string)</span></span>                       |                                                                                                                                           |
| <span data-ttu-id="8974d-211">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-211">public boolean showLabel(\[boolean value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="8974d-212">public boolean showPicAsText(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-212">public boolean showPicAsText(\[boolean value\])</span></span>                          |                                                                                                                                           |
| <span data-ttu-id="8974d-213">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-213">public TableId table(\[TableId value\])</span></span>                                  | <span data-ttu-id="8974d-214">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-214">Gets or sets the table ID associated with the object.</span></span>                                                                                     |
| <span data-ttu-id="8974d-215">public LineThickness thickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-215">public LineThickness thickness(\[LineThickness value\])</span></span>                  |                                                                                                                                           |
| <span data-ttu-id="8974d-216">public int top100mm(\[int topExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="8974d-216">public int top100mm(\[int topExclBorder\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="8974d-217">public int top100mmInclBorder(\[int topInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="8974d-217">public int top100mmInclBorder(\[int topInclBorder\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="8974d-218">public int topMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="8974d-218">public int topMarginAndFrame()</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="8974d-219">public int topMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-219">public int topMarginMode(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="8974d-220">public str topMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-220">public str topMarginStr(\[str value\])</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="8974d-221">public Units topMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-221">public Units topMarginUnit(\[Units value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="8974d-222">public Real topMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-222">public Real topMarginValue(\[Real value\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="8974d-223">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-223">public int topMode(\[int value\])</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="8974d-224">public str topStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-224">public str topStr(\[str value\])</span></span>                                         |                                                                                                                                           |
| <span data-ttu-id="8974d-225">public Units topUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-225">public Units topUnit(\[Units value\])</span></span>                                    |                                                                                                                                           |
| <span data-ttu-id="8974d-226">public Real topValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-226">public Real topValue(\[Real value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="8974d-227">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-227">public boolean visible(\[boolean value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="8974d-228">public boolean warnIfMissing(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-228">public boolean warnIfMissing(\[boolean value\])</span></span>                          |                                                                                                                                           |
| <span data-ttu-id="8974d-229">public str webMenuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-229">public str webMenuItemName(\[str value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="8974d-230">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-230">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span></span>        |                                                                                                                                           |
| <span data-ttu-id="8974d-231">public str webTarget(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-231">public str webTarget(\[str value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="8974d-232">public int width100mm(\[int widthExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="8974d-232">public int width100mm(\[int widthExclBorder\])</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="8974d-233">public int width100mmInclBorder(\[int widthInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="8974d-233">public int width100mmInclBorder(\[int widthInclBorder\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="8974d-234">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-234">public int widthMode(\[int value\])</span></span>                                      | <span data-ttu-id="8974d-235">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-235">Gets or sets the calculation mode of the width of the control.</span></span>                                                                            |
| <span data-ttu-id="8974d-236">public int widthOfString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="8974d-236">public int widthOfString100mm(str string)</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="8974d-237">public str widthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-237">public str widthStr(\[str value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="8974d-238">public Units widthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-238">public Units widthUnit(\[Units value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="8974d-239">public Real widthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="8974d-239">public Real widthValue(\[Real value\])</span></span>                                   | <span data-ttu-id="8974d-240">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-240">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="8974d-241">public void labelWidth(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="8974d-241">public void labelWidth(Real value, Units unit)</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="8974d-242">public void top(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="8974d-242">public void top(Real value, Units unit)</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="8974d-243">public void show()</span><span class="sxs-lookup"><span data-stu-id="8974d-243">public void show()</span></span>                                                       |                                                                                                                                           |
| <span data-ttu-id="8974d-244">public void rightMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="8974d-244">public void rightMargin(Real value, Units unit)</span></span>                          |                                                                                                                                           |
| <span data-ttu-id="8974d-245">public void left(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="8974d-245">public void left(Real value, Units unit)</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="8974d-246">public void bottomMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="8974d-246">public void bottomMargin(Real value, Units unit)</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="8974d-247">public void height(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="8974d-247">public void height(Real value, Units unit)</span></span>                               | <span data-ttu-id="8974d-248">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-248">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="8974d-249">public void hide()</span><span class="sxs-lookup"><span data-stu-id="8974d-249">public void hide()</span></span>                                                       |                                                                                                                                           |
| <span data-ttu-id="8974d-250">public void topMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="8974d-250">public void topMargin(Real value, Units unit)</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="8974d-251">public void leftMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="8974d-251">public void leftMargin(Real value, Units unit)</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="8974d-252">public void width(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="8974d-252">public void width(Real value, Units unit)</span></span>                                | <span data-ttu-id="8974d-253">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-253">Gets or sets the width of the control.</span></span>                                                                                                    |

## <a name="method-alignment"></a><span data-ttu-id="8974d-254">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="8974d-254">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="8974d-255">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="8974d-255">Parameters - alignment</span></span>

<span data-ttu-id="8974d-256">値</span><span class="sxs-lookup"><span data-stu-id="8974d-256">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="8974d-257">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="8974d-257">Return Value - alignment</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="8974d-258">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="8974d-258">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="8974d-259">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="8974d-259">Parameters - arrayIndex</span></span>

<span data-ttu-id="8974d-260">値</span><span class="sxs-lookup"><span data-stu-id="8974d-260">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="8974d-261">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="8974d-261">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="8974d-262">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="8974d-262">Method autoDeclaration</span></span>

<span data-ttu-id="8974d-263">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-263">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="8974d-264">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="8974d-264">Parameters - autoDeclaration</span></span>

<span data-ttu-id="8974d-265">値</span><span class="sxs-lookup"><span data-stu-id="8974d-265">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="8974d-266">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="8974d-266">Return Value - autoDeclaration</span></span>

<span data-ttu-id="8974d-267">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="8974d-267">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="8974d-268">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="8974d-268">Remarks - autoDeclaration</span></span>

<span data-ttu-id="8974d-269">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="8974d-269">Controls cannot have identical names.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="8974d-270">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="8974d-270">Method backStyle</span></span>

<span data-ttu-id="8974d-271">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-271">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="8974d-272">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="8974d-272">Parameters - backStyle</span></span>

<span data-ttu-id="8974d-273">値</span><span class="sxs-lookup"><span data-stu-id="8974d-273">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="8974d-274">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="8974d-274">Return Value - backStyle</span></span>

<span data-ttu-id="8974d-275">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="8974d-275">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bottommarginandframe"></a><span data-ttu-id="8974d-276">メソッド bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="8974d-276">Method bottomMarginAndFrame</span></span>

```xpp
public int bottomMarginAndFrame()
```

### <a name="return-value---bottommarginandframe"></a><span data-ttu-id="8974d-277">戻り値 - bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="8974d-277">Return Value - bottomMarginAndFrame</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="8974d-278">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="8974d-278">Method bottomMarginMode</span></span>

```xpp
public int bottomMarginMode([int value])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="8974d-279">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="8974d-279">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="8974d-280">値</span><span class="sxs-lookup"><span data-stu-id="8974d-280">value</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="8974d-281">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="8974d-281">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginstr"></a><span data-ttu-id="8974d-282">メソッド bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="8974d-282">Method bottomMarginStr</span></span>

```xpp
public str bottomMarginStr([str value])
```

### <a name="parameters---bottommarginstr"></a><span data-ttu-id="8974d-283">パラメーター - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="8974d-283">Parameters - bottomMarginStr</span></span>

<span data-ttu-id="8974d-284">値</span><span class="sxs-lookup"><span data-stu-id="8974d-284">value</span></span>  

### <a name="return-value---bottommarginstr"></a><span data-ttu-id="8974d-285">戻り値 - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="8974d-285">Return Value - bottomMarginStr</span></span>

## <a name="method-bottommarginunit"></a><span data-ttu-id="8974d-286">メソッド bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-286">Method bottomMarginUnit</span></span>

```xpp
public Units bottomMarginUnit([Units value])
```

### <a name="parameters---bottommarginunit"></a><span data-ttu-id="8974d-287">パラメーター - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-287">Parameters - bottomMarginUnit</span></span>

<span data-ttu-id="8974d-288">値</span><span class="sxs-lookup"><span data-stu-id="8974d-288">value</span></span>  

### <a name="return-value---bottommarginunit"></a><span data-ttu-id="8974d-289">戻り値 - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-289">Return Value - bottomMarginUnit</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="8974d-290">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="8974d-290">Method bottomMarginValue</span></span>

```xpp
public Real bottomMarginValue([Real value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="8974d-291">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="8974d-291">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="8974d-292">値</span><span class="sxs-lookup"><span data-stu-id="8974d-292">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="8974d-293">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="8974d-293">Return Value - bottomMarginValue</span></span>

## <a name="method-changelabelcase"></a><span data-ttu-id="8974d-294">メソッド changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="8974d-294">Method changeLabelCase</span></span>

```xpp
public int changeLabelCase([int value])
```

### <a name="parameters---changelabelcase"></a><span data-ttu-id="8974d-295">パラメーター - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="8974d-295">Parameters - changeLabelCase</span></span>

<span data-ttu-id="8974d-296">値</span><span class="sxs-lookup"><span data-stu-id="8974d-296">value</span></span>  

### <a name="return-value---changelabelcase"></a><span data-ttu-id="8974d-297">戻り値 - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="8974d-297">Return Value - changeLabelCase</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="8974d-298">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="8974d-298">Method colorScheme</span></span>

<span data-ttu-id="8974d-299">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-299">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="8974d-300">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="8974d-300">Parameters - colorScheme</span></span>

<span data-ttu-id="8974d-301">値</span><span class="sxs-lookup"><span data-stu-id="8974d-301">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="8974d-302">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="8974d-302">Return Value - colorScheme</span></span>

<span data-ttu-id="8974d-303">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="8974d-303">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="8974d-304">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="8974d-304">Remarks - colorScheme</span></span>

<span data-ttu-id="8974d-305">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="8974d-305">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="8974d-306">値です。</span><span class="sxs-lookup"><span data-stu-id="8974d-306">Value.</span></span> | <span data-ttu-id="8974d-307">スタイル。</span><span class="sxs-lookup"><span data-stu-id="8974d-307">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="8974d-308">0</span><span class="sxs-lookup"><span data-stu-id="8974d-308">0</span></span>      | <span data-ttu-id="8974d-309">既定。</span><span class="sxs-lookup"><span data-stu-id="8974d-309">Default.</span></span>                      |
| <span data-ttu-id="8974d-310">1</span><span class="sxs-lookup"><span data-stu-id="8974d-310">1</span></span>      | <span data-ttu-id="8974d-311">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="8974d-311">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="8974d-312">2</span><span class="sxs-lookup"><span data-stu-id="8974d-312">2</span></span>      | <span data-ttu-id="8974d-313">真の配色。</span><span class="sxs-lookup"><span data-stu-id="8974d-313">The true-color scheme.</span></span>        |

## <a name="method-configurationkey"></a><span data-ttu-id="8974d-314">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="8974d-314">Method configurationKey</span></span>

<span data-ttu-id="8974d-315">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-315">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="8974d-316">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="8974d-316">Parameters - configurationKey</span></span>

<span data-ttu-id="8974d-317">値</span><span class="sxs-lookup"><span data-stu-id="8974d-317">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="8974d-318">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="8974d-318">Return Value - configurationKey</span></span>

<span data-ttu-id="8974d-319">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="8974d-319">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="8974d-320">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="8974d-320">Remarks - configurationKey</span></span>

<span data-ttu-id="8974d-321">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8974d-321">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="8974d-322">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="8974d-322">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-controltype"></a><span data-ttu-id="8974d-323">メソッド controlType</span><span class="sxs-lookup"><span data-stu-id="8974d-323">Method controlType</span></span>

```xpp
public ReportFieldType controlType()
```

### <a name="return-value---controltype"></a><span data-ttu-id="8974d-324">戻り値 - controlType</span><span class="sxs-lookup"><span data-stu-id="8974d-324">Return Value - controlType</span></span>

## <a name="method-cssclass"></a><span data-ttu-id="8974d-325">メソッド cssClass</span><span class="sxs-lookup"><span data-stu-id="8974d-325">Method cssClass</span></span>

```xpp
public str cssClass([str value])
```

### <a name="parameters---cssclass"></a><span data-ttu-id="8974d-326">パラメーター - cssClass</span><span class="sxs-lookup"><span data-stu-id="8974d-326">Parameters - cssClass</span></span>

<span data-ttu-id="8974d-327">値</span><span class="sxs-lookup"><span data-stu-id="8974d-327">value</span></span>  

### <a name="return-value---cssclass"></a><span data-ttu-id="8974d-328">戻り値 - cssClass</span><span class="sxs-lookup"><span data-stu-id="8974d-328">Return Value - cssClass</span></span>

## <a name="method-datafield"></a><span data-ttu-id="8974d-329">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="8974d-329">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="8974d-330">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="8974d-330">Parameters - dataField</span></span>

<span data-ttu-id="8974d-331">値</span><span class="sxs-lookup"><span data-stu-id="8974d-331">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="8974d-332">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="8974d-332">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="8974d-333">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="8974d-333">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="8974d-334">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="8974d-334">Parameters - dataMethod</span></span>

<span data-ttu-id="8974d-335">値</span><span class="sxs-lookup"><span data-stu-id="8974d-335">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="8974d-336">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="8974d-336">Return Value - dataMethod</span></span>

## <a name="method-delete"></a><span data-ttu-id="8974d-337">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="8974d-337">Method delete</span></span>

```xpp
public int delete()
```

### <a name="return-value---delete"></a><span data-ttu-id="8974d-338">戻り値 - delete</span><span class="sxs-lookup"><span data-stu-id="8974d-338">Return Value - delete</span></span>

## <a name="method-effectivefont"></a><span data-ttu-id="8974d-339">メソッド effectiveFont</span><span class="sxs-lookup"><span data-stu-id="8974d-339">Method effectiveFont</span></span>

```xpp
public str effectiveFont()
```

### <a name="return-value---effectivefont"></a><span data-ttu-id="8974d-340">戻り値 - effectiveFont</span><span class="sxs-lookup"><span data-stu-id="8974d-340">Return Value - effectiveFont</span></span>

## <a name="method-fontinfoprinter"></a><span data-ttu-id="8974d-341">メソッド fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="8974d-341">Method fontInfoPrinter</span></span>

```xpp
public str fontInfoPrinter()
```

### <a name="return-value---fontinfoprinter"></a><span data-ttu-id="8974d-342">戻り値 - fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="8974d-342">Return Value - fontInfoPrinter</span></span>

## <a name="method-fontinfoprinterascent"></a><span data-ttu-id="8974d-343">メソッド fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="8974d-343">Method fontInfoPrinterAscent</span></span>

```xpp
public int fontInfoPrinterAscent()
```

### <a name="return-value---fontinfoprinterascent"></a><span data-ttu-id="8974d-344">戻り値 - fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="8974d-344">Return Value - fontInfoPrinterAscent</span></span>

## <a name="method-fontinfoprinterdescent"></a><span data-ttu-id="8974d-345">メソッド fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="8974d-345">Method fontInfoPrinterDescent</span></span>

```xpp
public int fontInfoPrinterDescent()
```

### <a name="return-value---fontinfoprinterdescent"></a><span data-ttu-id="8974d-346">戻り値 - fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="8974d-346">Return Value - fontInfoPrinterDescent</span></span>

## <a name="method-fontinfoprinterextlead"></a><span data-ttu-id="8974d-347">メソッド fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="8974d-347">Method fontInfoPrinterExtLead</span></span>

```xpp
public int fontInfoPrinterExtLead()
```

### <a name="return-value---fontinfoprinterextlead"></a><span data-ttu-id="8974d-348">戻り値 - fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="8974d-348">Return Value - fontInfoPrinterExtLead</span></span>

## <a name="method-fontinfoprinterheight"></a><span data-ttu-id="8974d-349">メソッド fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="8974d-349">Method fontInfoPrinterHeight</span></span>

```xpp
public int fontInfoPrinterHeight()
```

### <a name="return-value---fontinfoprinterheight"></a><span data-ttu-id="8974d-350">戻り値 - fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="8974d-350">Return Value - fontInfoPrinterHeight</span></span>

## <a name="method-fontinfoprinterintlead"></a><span data-ttu-id="8974d-351">メソッド fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="8974d-351">Method fontInfoPrinterIntLead</span></span>

```xpp
public int fontInfoPrinterIntLead()
```

### <a name="return-value---fontinfoprinterintlead"></a><span data-ttu-id="8974d-352">戻り値 - fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="8974d-352">Return Value - fontInfoPrinterIntLead</span></span>

## <a name="method-fontinfoscreen"></a><span data-ttu-id="8974d-353">メソッド fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="8974d-353">Method fontInfoScreen</span></span>

```xpp
public str fontInfoScreen()
```

### <a name="return-value---fontinfoscreen"></a><span data-ttu-id="8974d-354">戻り値 - fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="8974d-354">Return Value - fontInfoScreen</span></span>

## <a name="method-fontinfoscreenascent"></a><span data-ttu-id="8974d-355">メソッド fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="8974d-355">Method fontInfoScreenAscent</span></span>

```xpp
public int fontInfoScreenAscent()
```

### <a name="return-value---fontinfoscreenascent"></a><span data-ttu-id="8974d-356">戻り値 - fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="8974d-356">Return Value - fontInfoScreenAscent</span></span>

## <a name="method-fontinfoscreendescent"></a><span data-ttu-id="8974d-357">メソッド fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="8974d-357">Method fontInfoScreenDescent</span></span>

```xpp
public int fontInfoScreenDescent()
```

### <a name="return-value---fontinfoscreendescent"></a><span data-ttu-id="8974d-358">戻り値 - fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="8974d-358">Return Value - fontInfoScreenDescent</span></span>

## <a name="method-fontinfoscreenextlead"></a><span data-ttu-id="8974d-359">メソッド fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="8974d-359">Method fontInfoScreenExtLead</span></span>

```xpp
public int fontInfoScreenExtLead()
```

### <a name="return-value---fontinfoscreenextlead"></a><span data-ttu-id="8974d-360">戻り値 - fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="8974d-360">Return Value - fontInfoScreenExtLead</span></span>

## <a name="method-fontinfoscreenheight"></a><span data-ttu-id="8974d-361">メソッド fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="8974d-361">Method fontInfoScreenHeight</span></span>

```xpp
public int fontInfoScreenHeight()
```

### <a name="return-value---fontinfoscreenheight"></a><span data-ttu-id="8974d-362">戻り値 - fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="8974d-362">Return Value - fontInfoScreenHeight</span></span>

## <a name="method-fontinfoscreenintlead"></a><span data-ttu-id="8974d-363">メソッド fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="8974d-363">Method fontInfoScreenIntLead</span></span>

```xpp
public int fontInfoScreenIntLead()
```

### <a name="return-value---fontinfoscreenintlead"></a><span data-ttu-id="8974d-364">戻り値 - fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="8974d-364">Return Value - fontInfoScreenIntLead</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="8974d-365">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="8974d-365">Method foregroundColor</span></span>

<span data-ttu-id="8974d-366">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-366">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="8974d-367">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="8974d-367">Parameters - foregroundColor</span></span>

<span data-ttu-id="8974d-368">値</span><span class="sxs-lookup"><span data-stu-id="8974d-368">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="8974d-369">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="8974d-369">Return Value - foregroundColor</span></span>

<span data-ttu-id="8974d-370">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="8974d-370">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="8974d-371">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="8974d-371">Remarks - foregroundColor</span></span>

<span data-ttu-id="8974d-372">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8974d-372">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="8974d-373">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8974d-373">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="8974d-374">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="8974d-374">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="8974d-375">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="8974d-375">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="8974d-376">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="8974d-376">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="8974d-377">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="8974d-377">The maximum value for a single byte is 255.</span></span>

## <a name="method-height100mm"></a><span data-ttu-id="8974d-378">メソッド height100mm</span><span class="sxs-lookup"><span data-stu-id="8974d-378">Method height100mm</span></span>

```xpp
public int height100mm([int heightExclBorder])
```

### <a name="parameters---height100mm"></a><span data-ttu-id="8974d-379">パラメーター - height100mm</span><span class="sxs-lookup"><span data-stu-id="8974d-379">Parameters - height100mm</span></span>

<span data-ttu-id="8974d-380">heightExclBorder</span><span class="sxs-lookup"><span data-stu-id="8974d-380">heightExclBorder</span></span>  

### <a name="return-value---height100mm"></a><span data-ttu-id="8974d-381">戻り値 - height100mm</span><span class="sxs-lookup"><span data-stu-id="8974d-381">Return Value - height100mm</span></span>

## <a name="method-height100mminclborder"></a><span data-ttu-id="8974d-382">メソッド height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="8974d-382">Method height100mmInclBorder</span></span>

```xpp
public int height100mmInclBorder([int heightInclBorder])
```

### <a name="parameters---height100mminclborder"></a><span data-ttu-id="8974d-383">パラメーター - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="8974d-383">Parameters - height100mmInclBorder</span></span>

<span data-ttu-id="8974d-384">heightInclBorder</span><span class="sxs-lookup"><span data-stu-id="8974d-384">heightInclBorder</span></span>  

### <a name="return-value---height100mminclborder"></a><span data-ttu-id="8974d-385">戻り値 - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="8974d-385">Return Value - height100mmInclBorder</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="8974d-386">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="8974d-386">Method heightMode</span></span>

<span data-ttu-id="8974d-387">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-387">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="8974d-388">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="8974d-388">Parameters - heightMode</span></span>

<span data-ttu-id="8974d-389">値</span><span class="sxs-lookup"><span data-stu-id="8974d-389">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="8974d-390">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="8974d-390">Return Value - heightMode</span></span>

<span data-ttu-id="8974d-391">計算モード。</span><span class="sxs-lookup"><span data-stu-id="8974d-391">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="8974d-392">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="8974d-392">Remarks - heightMode</span></span>

<span data-ttu-id="8974d-393">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="8974d-393">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="8974d-394">モード。</span><span class="sxs-lookup"><span data-stu-id="8974d-394">Mode.</span></span>          | <span data-ttu-id="8974d-395">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="8974d-395">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8974d-396">正確。</span><span class="sxs-lookup"><span data-stu-id="8974d-396">Exact.</span></span>         | <span data-ttu-id="8974d-397">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="8974d-397">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="8974d-398">自動。</span><span class="sxs-lookup"><span data-stu-id="8974d-398">Auto.</span></span>          | <span data-ttu-id="8974d-399">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="8974d-399">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="8974d-400">列の高さ</span><span class="sxs-lookup"><span data-stu-id="8974d-400">Column height.</span></span> | <span data-ttu-id="8974d-401">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="8974d-401">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="8974d-402">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="8974d-402">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightofwordwrappedstring100mm"></a><span data-ttu-id="8974d-403">メソッド heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="8974d-403">Method heightOfWordWrappedString100mm</span></span>

```xpp
public int heightOfWordWrappedString100mm(str string)
```

### <a name="parameters---heightofwordwrappedstring100mm"></a><span data-ttu-id="8974d-404">パラメーター - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="8974d-404">Parameters - heightOfWordWrappedString100mm</span></span>

<span data-ttu-id="8974d-405">文字列</span><span class="sxs-lookup"><span data-stu-id="8974d-405">string</span></span>  

### <a name="return-value---heightofwordwrappedstring100mm"></a><span data-ttu-id="8974d-406">戻り値 - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="8974d-406">Return Value - heightOfWordWrappedString100mm</span></span>

## <a name="method-heightstr"></a><span data-ttu-id="8974d-407">メソッド heightStr</span><span class="sxs-lookup"><span data-stu-id="8974d-407">Method heightStr</span></span>

```xpp
public str heightStr([str value])
```

### <a name="parameters---heightstr"></a><span data-ttu-id="8974d-408">パラメーター - heightStr</span><span class="sxs-lookup"><span data-stu-id="8974d-408">Parameters - heightStr</span></span>

<span data-ttu-id="8974d-409">値</span><span class="sxs-lookup"><span data-stu-id="8974d-409">value</span></span>  

### <a name="return-value---heightstr"></a><span data-ttu-id="8974d-410">戻り値 - heightStr</span><span class="sxs-lookup"><span data-stu-id="8974d-410">Return Value - heightStr</span></span>

## <a name="method-heightunit"></a><span data-ttu-id="8974d-411">メソッド heightUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-411">Method heightUnit</span></span>

```xpp
public Units heightUnit([Units value])
```

### <a name="parameters---heightunit"></a><span data-ttu-id="8974d-412">パラメーター - heightUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-412">Parameters - heightUnit</span></span>

<span data-ttu-id="8974d-413">値</span><span class="sxs-lookup"><span data-stu-id="8974d-413">value</span></span>  

### <a name="return-value---heightunit"></a><span data-ttu-id="8974d-414">戻り値 - heightUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-414">Return Value - heightUnit</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="8974d-415">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="8974d-415">Method heightValue</span></span>

<span data-ttu-id="8974d-416">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-416">Gets or sets the height of the control.</span></span>

```xpp
public Real heightValue([Real value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="8974d-417">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="8974d-417">Parameters - heightValue</span></span>

<span data-ttu-id="8974d-418">値</span><span class="sxs-lookup"><span data-stu-id="8974d-418">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="8974d-419">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="8974d-419">Return Value - heightValue</span></span>

<span data-ttu-id="8974d-420">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="8974d-420">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="8974d-421">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="8974d-421">Remarks - heightValue</span></span>

<span data-ttu-id="8974d-422">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="8974d-422">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-imagename"></a><span data-ttu-id="8974d-423">メソッド imageName</span><span class="sxs-lookup"><span data-stu-id="8974d-423">Method imageName</span></span>

```xpp
public str imageName([str value])
```

### <a name="parameters---imagename"></a><span data-ttu-id="8974d-424">パラメーター - imageName</span><span class="sxs-lookup"><span data-stu-id="8974d-424">Parameters - imageName</span></span>

<span data-ttu-id="8974d-425">値</span><span class="sxs-lookup"><span data-stu-id="8974d-425">value</span></span>  

### <a name="return-value---imagename"></a><span data-ttu-id="8974d-426">戻り値 - imageName</span><span class="sxs-lookup"><span data-stu-id="8974d-426">Return Value - imageName</span></span>

## <a name="method-imageresource"></a><span data-ttu-id="8974d-427">メソッド imageResource</span><span class="sxs-lookup"><span data-stu-id="8974d-427">Method imageResource</span></span>

```xpp
public int imageResource([int value])
```

### <a name="parameters---imageresource"></a><span data-ttu-id="8974d-428">パラメーター - imageResource</span><span class="sxs-lookup"><span data-stu-id="8974d-428">Parameters - imageResource</span></span>

<span data-ttu-id="8974d-429">値</span><span class="sxs-lookup"><span data-stu-id="8974d-429">value</span></span>  

### <a name="return-value---imageresource"></a><span data-ttu-id="8974d-430">戻り値 - imageResource</span><span class="sxs-lookup"><span data-stu-id="8974d-430">Return Value - imageResource</span></span>

## <a name="method-label"></a><span data-ttu-id="8974d-431">メソッド label</span><span class="sxs-lookup"><span data-stu-id="8974d-431">Method label</span></span>

<span data-ttu-id="8974d-432">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-432">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="8974d-433">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="8974d-433">Parameters - label</span></span>

<span data-ttu-id="8974d-434">値</span><span class="sxs-lookup"><span data-stu-id="8974d-434">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="8974d-435">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="8974d-435">Return Value - label</span></span>

<span data-ttu-id="8974d-436">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="8974d-436">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="8974d-437">備考 - label</span><span class="sxs-lookup"><span data-stu-id="8974d-437">Remarks - label</span></span>

<span data-ttu-id="8974d-438">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-438">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="8974d-439">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="8974d-439">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="8974d-440">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="8974d-440">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="8974d-441">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="8974d-441">Parameters - labelBold</span></span>

<span data-ttu-id="8974d-442">値</span><span class="sxs-lookup"><span data-stu-id="8974d-442">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="8974d-443">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="8974d-443">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="8974d-444">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="8974d-444">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="8974d-445">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="8974d-445">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="8974d-446">値</span><span class="sxs-lookup"><span data-stu-id="8974d-446">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="8974d-447">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="8974d-447">Return Value - labelCharacterSet</span></span>

## <a name="method-labelcssclass"></a><span data-ttu-id="8974d-448">メソッド labelCssClass</span><span class="sxs-lookup"><span data-stu-id="8974d-448">Method labelCssClass</span></span>

```xpp
public str labelCssClass([str value])
```

### <a name="parameters---labelcssclass"></a><span data-ttu-id="8974d-449">パラメーター - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="8974d-449">Parameters - labelCssClass</span></span>

<span data-ttu-id="8974d-450">値</span><span class="sxs-lookup"><span data-stu-id="8974d-450">value</span></span>  

### <a name="return-value---labelcssclass"></a><span data-ttu-id="8974d-451">戻り値 - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="8974d-451">Return Value - labelCssClass</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="8974d-452">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="8974d-452">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="8974d-453">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="8974d-453">Parameters - labelFont</span></span>

<span data-ttu-id="8974d-454">値</span><span class="sxs-lookup"><span data-stu-id="8974d-454">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="8974d-455">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="8974d-455">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="8974d-456">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="8974d-456">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="8974d-457">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="8974d-457">Parameters - labelFontSize</span></span>

<span data-ttu-id="8974d-458">値</span><span class="sxs-lookup"><span data-stu-id="8974d-458">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="8974d-459">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="8974d-459">Return Value - labelFontSize</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="8974d-460">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="8974d-460">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="8974d-461">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="8974d-461">Parameters - labelItalic</span></span>

<span data-ttu-id="8974d-462">値</span><span class="sxs-lookup"><span data-stu-id="8974d-462">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="8974d-463">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="8974d-463">Return Value - labelItalic</span></span>

## <a name="method-labellinebelow"></a><span data-ttu-id="8974d-464">メソッド labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="8974d-464">Method labelLineBelow</span></span>

```xpp
public LineType labelLineBelow([LineType value])
```

### <a name="parameters---labellinebelow"></a><span data-ttu-id="8974d-465">パラメーター - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="8974d-465">Parameters - labelLineBelow</span></span>

<span data-ttu-id="8974d-466">値</span><span class="sxs-lookup"><span data-stu-id="8974d-466">value</span></span>  

### <a name="return-value---labellinebelow"></a><span data-ttu-id="8974d-467">戻り値 - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="8974d-467">Return Value - labelLineBelow</span></span>

## <a name="method-labellinethickness"></a><span data-ttu-id="8974d-468">メソッド labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="8974d-468">Method labelLineThickness</span></span>

```xpp
public LineThickness labelLineThickness([LineThickness value])
```

### <a name="parameters---labellinethickness"></a><span data-ttu-id="8974d-469">パラメーター - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="8974d-469">Parameters - labelLineThickness</span></span>

<span data-ttu-id="8974d-470">値</span><span class="sxs-lookup"><span data-stu-id="8974d-470">value</span></span>  

### <a name="return-value---labellinethickness"></a><span data-ttu-id="8974d-471">戻り値 - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="8974d-471">Return Value - labelLineThickness</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="8974d-472">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="8974d-472">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="8974d-473">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="8974d-473">Parameters - labelPosition</span></span>

<span data-ttu-id="8974d-474">値</span><span class="sxs-lookup"><span data-stu-id="8974d-474">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="8974d-475">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="8974d-475">Return Value - labelPosition</span></span>

## <a name="method-labeltableader"></a><span data-ttu-id="8974d-476">メソッド labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="8974d-476">Method labelTabLeader</span></span>

```xpp
public int labelTabLeader([int value])
```

### <a name="parameters---labeltableader"></a><span data-ttu-id="8974d-477">パラメーター - labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="8974d-477">Parameters - labelTabLeader</span></span>

<span data-ttu-id="8974d-478">値</span><span class="sxs-lookup"><span data-stu-id="8974d-478">value</span></span>  

### <a name="return-value---labeltableader"></a><span data-ttu-id="8974d-479">戻り値 - labelTabLeader</span><span class="sxs-lookup"><span data-stu-id="8974d-479">Return Value - labelTabLeader</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="8974d-480">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="8974d-480">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="8974d-481">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="8974d-481">Parameters - labelUnderline</span></span>

<span data-ttu-id="8974d-482">値</span><span class="sxs-lookup"><span data-stu-id="8974d-482">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="8974d-483">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="8974d-483">Return Value - labelUnderline</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="8974d-484">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="8974d-484">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="8974d-485">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="8974d-485">Parameters - labelWidthMode</span></span>

<span data-ttu-id="8974d-486">値</span><span class="sxs-lookup"><span data-stu-id="8974d-486">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="8974d-487">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="8974d-487">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthstr"></a><span data-ttu-id="8974d-488">メソッド labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="8974d-488">Method labelWidthStr</span></span>

```xpp
public str labelWidthStr([str value])
```

### <a name="parameters---labelwidthstr"></a><span data-ttu-id="8974d-489">パラメーター - labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="8974d-489">Parameters - labelWidthStr</span></span>

<span data-ttu-id="8974d-490">値</span><span class="sxs-lookup"><span data-stu-id="8974d-490">value</span></span>  

### <a name="return-value---labelwidthstr"></a><span data-ttu-id="8974d-491">戻り値 - labelWidthStr</span><span class="sxs-lookup"><span data-stu-id="8974d-491">Return Value - labelWidthStr</span></span>

## <a name="method-labelwidthunit"></a><span data-ttu-id="8974d-492">メソッド labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-492">Method labelWidthUnit</span></span>

```xpp
public Units labelWidthUnit([Units value])
```

### <a name="parameters---labelwidthunit"></a><span data-ttu-id="8974d-493">パラメーター - labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-493">Parameters - labelWidthUnit</span></span>

<span data-ttu-id="8974d-494">値</span><span class="sxs-lookup"><span data-stu-id="8974d-494">value</span></span>  

### <a name="return-value---labelwidthunit"></a><span data-ttu-id="8974d-495">戻り値 - labelWidthUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-495">Return Value - labelWidthUnit</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="8974d-496">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="8974d-496">Method labelWidthValue</span></span>

```xpp
public Real labelWidthValue([Real value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="8974d-497">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="8974d-497">Parameters - labelWidthValue</span></span>

<span data-ttu-id="8974d-498">値</span><span class="sxs-lookup"><span data-stu-id="8974d-498">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="8974d-499">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="8974d-499">Return Value - labelWidthValue</span></span>

## <a name="method-left100mm"></a><span data-ttu-id="8974d-500">メソッド left100mm</span><span class="sxs-lookup"><span data-stu-id="8974d-500">Method left100mm</span></span>

```xpp
public int left100mm([int leftExclBorder])
```

### <a name="parameters---left100mm"></a><span data-ttu-id="8974d-501">パラメーター - left100mm</span><span class="sxs-lookup"><span data-stu-id="8974d-501">Parameters - left100mm</span></span>

<span data-ttu-id="8974d-502">leftExclBorder</span><span class="sxs-lookup"><span data-stu-id="8974d-502">leftExclBorder</span></span>  

### <a name="return-value---left100mm"></a><span data-ttu-id="8974d-503">戻り値 - left100mm</span><span class="sxs-lookup"><span data-stu-id="8974d-503">Return Value - left100mm</span></span>

## <a name="method-left100mminclborder"></a><span data-ttu-id="8974d-504">メソッド left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="8974d-504">Method left100mmInclBorder</span></span>

```xpp
public int left100mmInclBorder([int leftInclBorder])
```

### <a name="parameters---left100mminclborder"></a><span data-ttu-id="8974d-505">パラメーター - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="8974d-505">Parameters - left100mmInclBorder</span></span>

<span data-ttu-id="8974d-506">leftInclBorder</span><span class="sxs-lookup"><span data-stu-id="8974d-506">leftInclBorder</span></span>  

### <a name="return-value---left100mminclborder"></a><span data-ttu-id="8974d-507">戻り値 - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="8974d-507">Return Value - left100mmInclBorder</span></span>

## <a name="method-leftmarginanframe"></a><span data-ttu-id="8974d-508">メソッド leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="8974d-508">Method leftMarginAnFrame</span></span>

```xpp
public int leftMarginAnFrame()
```

### <a name="return-value---leftmarginanframe"></a><span data-ttu-id="8974d-509">戻り値 - leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="8974d-509">Return Value - leftMarginAnFrame</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="8974d-510">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="8974d-510">Method leftMarginMode</span></span>

```xpp
public int leftMarginMode([int value])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="8974d-511">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="8974d-511">Parameters - leftMarginMode</span></span>

<span data-ttu-id="8974d-512">値</span><span class="sxs-lookup"><span data-stu-id="8974d-512">value</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="8974d-513">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="8974d-513">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginstr"></a><span data-ttu-id="8974d-514">メソッド leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="8974d-514">Method leftMarginStr</span></span>

```xpp
public str leftMarginStr([str value])
```

### <a name="parameters---leftmarginstr"></a><span data-ttu-id="8974d-515">パラメーター - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="8974d-515">Parameters - leftMarginStr</span></span>

<span data-ttu-id="8974d-516">値</span><span class="sxs-lookup"><span data-stu-id="8974d-516">value</span></span>  

### <a name="return-value---leftmarginstr"></a><span data-ttu-id="8974d-517">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="8974d-517">Return Value - leftMarginStr</span></span>

## <a name="method-leftmarginunit"></a><span data-ttu-id="8974d-518">メソッド leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-518">Method leftMarginUnit</span></span>

```xpp
public Units leftMarginUnit([Units value])
```

### <a name="parameters---leftmarginunit"></a><span data-ttu-id="8974d-519">パラメーター - leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-519">Parameters - leftMarginUnit</span></span>

<span data-ttu-id="8974d-520">値</span><span class="sxs-lookup"><span data-stu-id="8974d-520">value</span></span>  

### <a name="return-value---leftmarginunit"></a><span data-ttu-id="8974d-521">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="8974d-521">Return Value - leftMarginUnit</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="8974d-522">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="8974d-522">Method leftMarginValue</span></span>

```xpp
public Real leftMarginValue([Real value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="8974d-523">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="8974d-523">Parameters - leftMarginValue</span></span>

<span data-ttu-id="8974d-524">値</span><span class="sxs-lookup"><span data-stu-id="8974d-524">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="8974d-525">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="8974d-525">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="8974d-526">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="8974d-526">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="8974d-527">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="8974d-527">Parameters - leftMode</span></span>

<span data-ttu-id="8974d-528">値</span><span class="sxs-lookup"><span data-stu-id="8974d-528">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="8974d-529">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="8974d-529">Return Value - leftMode</span></span>

## <a name="method-leftstr"></a><span data-ttu-id="8974d-530">メソッド leftStr</span><span class="sxs-lookup"><span data-stu-id="8974d-530">Method leftStr</span></span>

```xpp
public str leftStr([str value])
```

### <a name="parameters---leftstr"></a><span data-ttu-id="8974d-531">パラメーター - leftStr</span><span class="sxs-lookup"><span data-stu-id="8974d-531">Parameters - leftStr</span></span>

<span data-ttu-id="8974d-532">値</span><span class="sxs-lookup"><span data-stu-id="8974d-532">value</span></span>  

### <a name="return-value---leftstr"></a><span data-ttu-id="8974d-533">戻り値 - leftStr</span><span class="sxs-lookup"><span data-stu-id="8974d-533">Return Value - leftStr</span></span>

## <a name="method-leftunit"></a><span data-ttu-id="8974d-534">メソッド leftUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-534">Method leftUnit</span></span>

```xpp
public Units leftUnit([Units value])
```

### <a name="parameters---leftunit"></a><span data-ttu-id="8974d-535">パラメーター - leftUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-535">Parameters - leftUnit</span></span>

<span data-ttu-id="8974d-536">値</span><span class="sxs-lookup"><span data-stu-id="8974d-536">value</span></span>  

### <a name="return-value---leftunit"></a><span data-ttu-id="8974d-537">戻り値 - leftUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-537">Return Value - leftUnit</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="8974d-538">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="8974d-538">Method leftValue</span></span>

```xpp
public Real leftValue([Real value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="8974d-539">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="8974d-539">Parameters - leftValue</span></span>

<span data-ttu-id="8974d-540">値</span><span class="sxs-lookup"><span data-stu-id="8974d-540">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="8974d-541">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="8974d-541">Return Value - leftValue</span></span>

## <a name="method-lineabove"></a><span data-ttu-id="8974d-542">メソッド lineAbove</span><span class="sxs-lookup"><span data-stu-id="8974d-542">Method lineAbove</span></span>

```xpp
public LineType lineAbove([LineType value])
```

### <a name="parameters---lineabove"></a><span data-ttu-id="8974d-543">パラメーター - lineAbove</span><span class="sxs-lookup"><span data-stu-id="8974d-543">Parameters - lineAbove</span></span>

<span data-ttu-id="8974d-544">値</span><span class="sxs-lookup"><span data-stu-id="8974d-544">value</span></span>  

### <a name="return-value---lineabove"></a><span data-ttu-id="8974d-545">戻り値 - lineAbove</span><span class="sxs-lookup"><span data-stu-id="8974d-545">Return Value - lineAbove</span></span>

## <a name="method-linebelow"></a><span data-ttu-id="8974d-546">メソッド lineBelow</span><span class="sxs-lookup"><span data-stu-id="8974d-546">Method lineBelow</span></span>

```xpp
public LineType lineBelow([LineType value])
```

### <a name="parameters---linebelow"></a><span data-ttu-id="8974d-547">パラメーター - lineBelow</span><span class="sxs-lookup"><span data-stu-id="8974d-547">Parameters - lineBelow</span></span>

<span data-ttu-id="8974d-548">値</span><span class="sxs-lookup"><span data-stu-id="8974d-548">value</span></span>  

### <a name="return-value---linebelow"></a><span data-ttu-id="8974d-549">戻り値 - lineBelow</span><span class="sxs-lookup"><span data-stu-id="8974d-549">Return Value - lineBelow</span></span>

## <a name="method-lineleft"></a><span data-ttu-id="8974d-550">メソッド lineLeft</span><span class="sxs-lookup"><span data-stu-id="8974d-550">Method lineLeft</span></span>

<span data-ttu-id="8974d-551">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-551">Gets or sets the type of line that is used as the left border of a section.</span></span>

```xpp
public LineType lineLeft([LineType value])
```

### <a name="parameters---lineleft"></a><span data-ttu-id="8974d-552">パラメーター - lineLeft</span><span class="sxs-lookup"><span data-stu-id="8974d-552">Parameters - lineLeft</span></span>

<span data-ttu-id="8974d-553">値</span><span class="sxs-lookup"><span data-stu-id="8974d-553">value</span></span>  

### <a name="return-value---lineleft"></a><span data-ttu-id="8974d-554">戻り値 - lineLeft</span><span class="sxs-lookup"><span data-stu-id="8974d-554">Return Value - lineLeft</span></span>

<span data-ttu-id="8974d-555">左境界線として使用される線のタイプ。</span><span class="sxs-lookup"><span data-stu-id="8974d-555">The type of line that is used as the left border.</span></span>

## <a name="method-lineright"></a><span data-ttu-id="8974d-556">メソッド lineRight</span><span class="sxs-lookup"><span data-stu-id="8974d-556">Method lineRight</span></span>

```xpp
public LineType lineRight([LineType value])
```

### <a name="parameters---lineright"></a><span data-ttu-id="8974d-557">パラメーター - lineRight</span><span class="sxs-lookup"><span data-stu-id="8974d-557">Parameters - lineRight</span></span>

<span data-ttu-id="8974d-558">値</span><span class="sxs-lookup"><span data-stu-id="8974d-558">value</span></span>  

### <a name="return-value---lineright"></a><span data-ttu-id="8974d-559">戻り値 - lineRight</span><span class="sxs-lookup"><span data-stu-id="8974d-559">Return Value - lineRight</span></span>

## <a name="method-menuitemlabel"></a><span data-ttu-id="8974d-560">メソッド menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="8974d-560">Method menuItemLabel</span></span>

```xpp
public str menuItemLabel([str value])
```

### <a name="parameters---menuitemlabel"></a><span data-ttu-id="8974d-561">パラメーター - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="8974d-561">Parameters - menuItemLabel</span></span>

<span data-ttu-id="8974d-562">値</span><span class="sxs-lookup"><span data-stu-id="8974d-562">value</span></span>  

### <a name="return-value---menuitemlabel"></a><span data-ttu-id="8974d-563">戻り値 - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="8974d-563">Return Value - menuItemLabel</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="8974d-564">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="8974d-564">Method menuItemName</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="8974d-565">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="8974d-565">Parameters - menuItemName</span></span>

<span data-ttu-id="8974d-566">値</span><span class="sxs-lookup"><span data-stu-id="8974d-566">value</span></span>  

### <a name="return-value---menuitemname"></a><span data-ttu-id="8974d-567">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="8974d-567">Return Value - menuItemName</span></span>

## <a name="method-menuitemtype"></a><span data-ttu-id="8974d-568">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="8974d-568">Method menuItemType</span></span>

```xpp
public MenuItemType menuItemType([MenuItemType value])
```

### <a name="parameters---menuitemtype"></a><span data-ttu-id="8974d-569">パラメーター - menuItemType</span><span class="sxs-lookup"><span data-stu-id="8974d-569">Parameters - menuItemType</span></span>

<span data-ttu-id="8974d-570">値</span><span class="sxs-lookup"><span data-stu-id="8974d-570">value</span></span>  

### <a name="return-value---menuitemtype"></a><span data-ttu-id="8974d-571">戻り値 - menuItemType</span><span class="sxs-lookup"><span data-stu-id="8974d-571">Return Value - menuItemType</span></span>

## <a name="method-modelfieldname"></a><span data-ttu-id="8974d-572">メソッド modelFieldName</span><span class="sxs-lookup"><span data-stu-id="8974d-572">Method modelFieldName</span></span>

```xpp
public str modelFieldName([str value])
```

### <a name="parameters---modelfieldname"></a><span data-ttu-id="8974d-573">パラメーター - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="8974d-573">Parameters - modelFieldName</span></span>

<span data-ttu-id="8974d-574">値</span><span class="sxs-lookup"><span data-stu-id="8974d-574">value</span></span>  

### <a name="return-value---modelfieldname"></a><span data-ttu-id="8974d-575">戻り値 - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="8974d-575">Return Value - modelFieldName</span></span>

## <a name="method-name"></a><span data-ttu-id="8974d-576">メソッド名</span><span class="sxs-lookup"><span data-stu-id="8974d-576">Method name</span></span>

<span data-ttu-id="8974d-577">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-577">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="8974d-578">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="8974d-578">Parameters - name</span></span>

<span data-ttu-id="8974d-579">値</span><span class="sxs-lookup"><span data-stu-id="8974d-579">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="8974d-580">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="8974d-580">Return Value - name</span></span>

<span data-ttu-id="8974d-581">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="8974d-581">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="8974d-582">備考 - name</span><span class="sxs-lookup"><span data-stu-id="8974d-582">Remarks - name</span></span>

<span data-ttu-id="8974d-583">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8974d-583">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="8974d-584">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="8974d-584">Begins with a letter.</span></span>
-   <span data-ttu-id="8974d-585">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="8974d-585">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="8974d-586">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="8974d-586">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="8974d-587">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="8974d-587">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="8974d-588">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="8974d-588">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-numberoflines"></a><span data-ttu-id="8974d-589">メソッド numberOfLines</span><span class="sxs-lookup"><span data-stu-id="8974d-589">Method numberOfLines</span></span>

```xpp
public int numberOfLines(int height100mm)
```

### <a name="parameters---numberoflines"></a><span data-ttu-id="8974d-590">パラメーター - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="8974d-590">Parameters - numberOfLines</span></span>

<span data-ttu-id="8974d-591">height100mm</span><span class="sxs-lookup"><span data-stu-id="8974d-591">height100mm</span></span>  

### <a name="return-value---numberoflines"></a><span data-ttu-id="8974d-592">戻り値 - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="8974d-592">Return Value - numberOfLines</span></span>

## <a name="method-position"></a><span data-ttu-id="8974d-593">メソッドの位置</span><span class="sxs-lookup"><span data-stu-id="8974d-593">Method position</span></span>

```xpp
public int position([int value])
```

### <a name="parameters---position"></a><span data-ttu-id="8974d-594">パラメーター - position</span><span class="sxs-lookup"><span data-stu-id="8974d-594">Parameters - position</span></span>

<span data-ttu-id="8974d-595">値</span><span class="sxs-lookup"><span data-stu-id="8974d-595">value</span></span>  

### <a name="return-value---position"></a><span data-ttu-id="8974d-596">戻り値 - position</span><span class="sxs-lookup"><span data-stu-id="8974d-596">Return Value - position</span></span>

## <a name="method-previewinfo"></a><span data-ttu-id="8974d-597">メソッド previewInfo</span><span class="sxs-lookup"><span data-stu-id="8974d-597">Method previewInfo</span></span>

```xpp
public str previewInfo(str string)
```

### <a name="parameters---previewinfo"></a><span data-ttu-id="8974d-598">パラメーター - previewInfo</span><span class="sxs-lookup"><span data-stu-id="8974d-598">Parameters - previewInfo</span></span>

<span data-ttu-id="8974d-599">文字列</span><span class="sxs-lookup"><span data-stu-id="8974d-599">string</span></span>  

### <a name="return-value---previewinfo"></a><span data-ttu-id="8974d-600">戻り値 - previewInfo</span><span class="sxs-lookup"><span data-stu-id="8974d-600">Return Value - previewInfo</span></span>

## <a name="method-previewxcompensation100mm"></a><span data-ttu-id="8974d-601">メソッド previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="8974d-601">Method previewXCompensation100mm</span></span>

```xpp
public int previewXCompensation100mm(str string)
```

### <a name="parameters---previewxcompensation100mm"></a><span data-ttu-id="8974d-602">パラメーター - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="8974d-602">Parameters - previewXCompensation100mm</span></span>

<span data-ttu-id="8974d-603">文字列</span><span class="sxs-lookup"><span data-stu-id="8974d-603">string</span></span>  

### <a name="return-value---previewxcompensation100mm"></a><span data-ttu-id="8974d-604">戻り値 - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="8974d-604">Return Value - previewXCompensation100mm</span></span>

## <a name="method-resizebitmap"></a><span data-ttu-id="8974d-605">メソッド resizeBitmap</span><span class="sxs-lookup"><span data-stu-id="8974d-605">Method resizeBitmap</span></span>

```xpp
public boolean resizeBitmap([boolean value])
```

### <a name="parameters---resizebitmap"></a><span data-ttu-id="8974d-606">パラメーター - resizeBitmap</span><span class="sxs-lookup"><span data-stu-id="8974d-606">Parameters - resizeBitmap</span></span>

<span data-ttu-id="8974d-607">値</span><span class="sxs-lookup"><span data-stu-id="8974d-607">value</span></span>  

### <a name="return-value---resizebitmap"></a><span data-ttu-id="8974d-608">戻り値 - resizeBitmap</span><span class="sxs-lookup"><span data-stu-id="8974d-608">Return Value - resizeBitmap</span></span>

## <a name="method-right100mm"></a><span data-ttu-id="8974d-609">メソッド right100mm</span><span class="sxs-lookup"><span data-stu-id="8974d-609">Method right100mm</span></span>

```xpp
public int right100mm()
```

### <a name="return-value---right100mm"></a><span data-ttu-id="8974d-610">戻り値 - right100mm</span><span class="sxs-lookup"><span data-stu-id="8974d-610">Return Value - right100mm</span></span>

## <a name="method-right100mminclborder"></a><span data-ttu-id="8974d-611">メソッド right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="8974d-611">Method right100mmInclBorder</span></span>

```xpp
public int right100mmInclBorder()
```

### <a name="return-value---right100mminclborder"></a><span data-ttu-id="8974d-612">戻り値 - right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="8974d-612">Return Value - right100mmInclBorder</span></span>

## <a name="method-rightmarginandframe"></a><span data-ttu-id="8974d-613">メソッド rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="8974d-613">Method rightMarginAndFrame</span></span>

```xpp
public int rightMarginAndFrame()
```

### <a name="return-value---rightmarginandframe"></a><span data-ttu-id="8974d-614">戻り値 - rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="8974d-614">Return Value - rightMarginAndFrame</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="8974d-615">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="8974d-615">Method rightMarginMode</span></span>

```xpp
public int rightMarginMode([int value])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="8974d-616">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="8974d-616">Parameters - rightMarginMode</span></span>

<span data-ttu-id="8974d-617">値</span><span class="sxs-lookup"><span data-stu-id="8974d-617">value</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="8974d-618">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="8974d-618">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginstr"></a><span data-ttu-id="8974d-619">メソッド rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="8974d-619">Method rightMarginStr</span></span>

```xpp
public str rightMarginStr([str value])
```

### <a name="parameters---rightmarginstr"></a><span data-ttu-id="8974d-620">パラメーター - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="8974d-620">Parameters - rightMarginStr</span></span>

<span data-ttu-id="8974d-621">値</span><span class="sxs-lookup"><span data-stu-id="8974d-621">value</span></span>  

### <a name="return-value---rightmarginstr"></a><span data-ttu-id="8974d-622">戻り値 - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="8974d-622">Return Value - rightMarginStr</span></span>

## <a name="method-rightmarginunit"></a><span data-ttu-id="8974d-623">メソッド rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-623">Method rightMarginUnit</span></span>

```xpp
public Units rightMarginUnit([Units value])
```

### <a name="parameters---rightmarginunit"></a><span data-ttu-id="8974d-624">パラメーター - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-624">Parameters - rightMarginUnit</span></span>

<span data-ttu-id="8974d-625">値</span><span class="sxs-lookup"><span data-stu-id="8974d-625">value</span></span>  

### <a name="return-value---rightmarginunit"></a><span data-ttu-id="8974d-626">戻り値 - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-626">Return Value - rightMarginUnit</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="8974d-627">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="8974d-627">Method rightMarginValue</span></span>

```xpp
public Real rightMarginValue([Real value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="8974d-628">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="8974d-628">Parameters - rightMarginValue</span></span>

<span data-ttu-id="8974d-629">値</span><span class="sxs-lookup"><span data-stu-id="8974d-629">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="8974d-630">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="8974d-630">Return Value - rightMarginValue</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="8974d-631">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="8974d-631">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="8974d-632">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="8974d-632">Parameters - securityKey</span></span>

<span data-ttu-id="8974d-633">値</span><span class="sxs-lookup"><span data-stu-id="8974d-633">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="8974d-634">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="8974d-634">Return Value - securityKey</span></span>

## <a name="method-setheightgettext"></a><span data-ttu-id="8974d-635">メソッド setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="8974d-635">Method setHeightGetText</span></span>

```xpp
public str setHeightGetText(int lines, str string)
```

### <a name="parameters---setheightgettext"></a><span data-ttu-id="8974d-636">パラメーター - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="8974d-636">Parameters - setHeightGetText</span></span>

<span data-ttu-id="8974d-637">明細行</span><span class="sxs-lookup"><span data-stu-id="8974d-637">lines</span></span>  

<!-- -->

<span data-ttu-id="8974d-638">文字列</span><span class="sxs-lookup"><span data-stu-id="8974d-638">string</span></span>  

### <a name="return-value---setheightgettext"></a><span data-ttu-id="8974d-639">戻り値 - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="8974d-639">Return Value - setHeightGetText</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="8974d-640">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="8974d-640">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="8974d-641">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="8974d-641">Parameters - showLabel</span></span>

<span data-ttu-id="8974d-642">値</span><span class="sxs-lookup"><span data-stu-id="8974d-642">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="8974d-643">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="8974d-643">Return Value - showLabel</span></span>

## <a name="method-showpicastext"></a><span data-ttu-id="8974d-644">メソッド showPicAsText</span><span class="sxs-lookup"><span data-stu-id="8974d-644">Method showPicAsText</span></span>

```xpp
public boolean showPicAsText([boolean value])
```

### <a name="parameters---showpicastext"></a><span data-ttu-id="8974d-645">パラメーター - showPicAsText</span><span class="sxs-lookup"><span data-stu-id="8974d-645">Parameters - showPicAsText</span></span>

<span data-ttu-id="8974d-646">値</span><span class="sxs-lookup"><span data-stu-id="8974d-646">value</span></span>  

### <a name="return-value---showpicastext"></a><span data-ttu-id="8974d-647">戻り値 - showPicAsText</span><span class="sxs-lookup"><span data-stu-id="8974d-647">Return Value - showPicAsText</span></span>

## <a name="method-table"></a><span data-ttu-id="8974d-648">メソッド table</span><span class="sxs-lookup"><span data-stu-id="8974d-648">Method table</span></span>

<span data-ttu-id="8974d-649">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-649">Gets or sets the table ID associated with the object.</span></span>

```xpp
public TableId table([TableId value])
```

### <a name="parameters---table"></a><span data-ttu-id="8974d-650">パラメーター - table</span><span class="sxs-lookup"><span data-stu-id="8974d-650">Parameters - table</span></span>

<span data-ttu-id="8974d-651">値</span><span class="sxs-lookup"><span data-stu-id="8974d-651">value</span></span>  

### <a name="return-value---table"></a><span data-ttu-id="8974d-652">戻り値 - toBlob</span><span class="sxs-lookup"><span data-stu-id="8974d-652">Return Value - table</span></span>

<span data-ttu-id="8974d-653">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="8974d-653">The current value of the table ID associated with the object.</span></span>

## <a name="method-thickness"></a><span data-ttu-id="8974d-654">メソッド thickness</span><span class="sxs-lookup"><span data-stu-id="8974d-654">Method thickness</span></span>

```xpp
public LineThickness thickness([LineThickness value])
```

### <a name="parameters---thickness"></a><span data-ttu-id="8974d-655">パラメーター - thickness</span><span class="sxs-lookup"><span data-stu-id="8974d-655">Parameters - thickness</span></span>

<span data-ttu-id="8974d-656">値</span><span class="sxs-lookup"><span data-stu-id="8974d-656">value</span></span>  

### <a name="return-value---thickness"></a><span data-ttu-id="8974d-657">戻り値 - thickness</span><span class="sxs-lookup"><span data-stu-id="8974d-657">Return Value - thickness</span></span>

## <a name="method-top100mm"></a><span data-ttu-id="8974d-658">メソッド top100mm</span><span class="sxs-lookup"><span data-stu-id="8974d-658">Method top100mm</span></span>

```xpp
public int top100mm([int topExclBorder])
```

### <a name="parameters---top100mm"></a><span data-ttu-id="8974d-659">パラメーター - top100mm</span><span class="sxs-lookup"><span data-stu-id="8974d-659">Parameters - top100mm</span></span>

<span data-ttu-id="8974d-660">topExclBorder</span><span class="sxs-lookup"><span data-stu-id="8974d-660">topExclBorder</span></span>  

### <a name="return-value---top100mm"></a><span data-ttu-id="8974d-661">戻り値 - top100mm</span><span class="sxs-lookup"><span data-stu-id="8974d-661">Return Value - top100mm</span></span>

## <a name="method-top100mminclborder"></a><span data-ttu-id="8974d-662">メソッド top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="8974d-662">Method top100mmInclBorder</span></span>

```xpp
public int top100mmInclBorder([int topInclBorder])
```

### <a name="parameters---top100mminclborder"></a><span data-ttu-id="8974d-663">パラメーター - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="8974d-663">Parameters - top100mmInclBorder</span></span>

<span data-ttu-id="8974d-664">topInclBorder</span><span class="sxs-lookup"><span data-stu-id="8974d-664">topInclBorder</span></span>  

### <a name="return-value---top100mminclborder"></a><span data-ttu-id="8974d-665">戻り値 - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="8974d-665">Return Value - top100mmInclBorder</span></span>

## <a name="method-topmarginandframe"></a><span data-ttu-id="8974d-666">メソッド topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="8974d-666">Method topMarginAndFrame</span></span>

```xpp
public int topMarginAndFrame()
```

### <a name="return-value---topmarginandframe"></a><span data-ttu-id="8974d-667">戻り値 - topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="8974d-667">Return Value - topMarginAndFrame</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="8974d-668">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="8974d-668">Method topMarginMode</span></span>

```xpp
public int topMarginMode([int value])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="8974d-669">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="8974d-669">Parameters - topMarginMode</span></span>

<span data-ttu-id="8974d-670">値</span><span class="sxs-lookup"><span data-stu-id="8974d-670">value</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="8974d-671">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="8974d-671">Return Value - topMarginMode</span></span>

## <a name="method-topmarginstr"></a><span data-ttu-id="8974d-672">メソッド topMarginStr</span><span class="sxs-lookup"><span data-stu-id="8974d-672">Method topMarginStr</span></span>

```xpp
public str topMarginStr([str value])
```

### <a name="parameters---topmarginstr"></a><span data-ttu-id="8974d-673">パラメーター - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="8974d-673">Parameters - topMarginStr</span></span>

<span data-ttu-id="8974d-674">値</span><span class="sxs-lookup"><span data-stu-id="8974d-674">value</span></span>  

### <a name="return-value---topmarginstr"></a><span data-ttu-id="8974d-675">戻り値 - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="8974d-675">Return Value - topMarginStr</span></span>

## <a name="method-topmarginunit"></a><span data-ttu-id="8974d-676">メソッド topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-676">Method topMarginUnit</span></span>

```xpp
public Units topMarginUnit([Units value])
```

### <a name="parameters---topmarginunit"></a><span data-ttu-id="8974d-677">パラメーター - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-677">Parameters - topMarginUnit</span></span>

<span data-ttu-id="8974d-678">値</span><span class="sxs-lookup"><span data-stu-id="8974d-678">value</span></span>  

### <a name="return-value---topmarginunit"></a><span data-ttu-id="8974d-679">戻り値 - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-679">Return Value - topMarginUnit</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="8974d-680">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="8974d-680">Method topMarginValue</span></span>

```xpp
public Real topMarginValue([Real value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="8974d-681">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="8974d-681">Parameters - topMarginValue</span></span>

<span data-ttu-id="8974d-682">値</span><span class="sxs-lookup"><span data-stu-id="8974d-682">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="8974d-683">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="8974d-683">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="8974d-684">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="8974d-684">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="8974d-685">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="8974d-685">Parameters - topMode</span></span>

<span data-ttu-id="8974d-686">値</span><span class="sxs-lookup"><span data-stu-id="8974d-686">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="8974d-687">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="8974d-687">Return Value - topMode</span></span>

## <a name="method-topstr"></a><span data-ttu-id="8974d-688">メソッド topStr</span><span class="sxs-lookup"><span data-stu-id="8974d-688">Method topStr</span></span>

```xpp
public str topStr([str value])
```

### <a name="parameters---topstr"></a><span data-ttu-id="8974d-689">パラメーター - topStr</span><span class="sxs-lookup"><span data-stu-id="8974d-689">Parameters - topStr</span></span>

<span data-ttu-id="8974d-690">値</span><span class="sxs-lookup"><span data-stu-id="8974d-690">value</span></span>  

### <a name="return-value---topstr"></a><span data-ttu-id="8974d-691">戻り値 - topStr</span><span class="sxs-lookup"><span data-stu-id="8974d-691">Return Value - topStr</span></span>

## <a name="method-topunit"></a><span data-ttu-id="8974d-692">メソッド topUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-692">Method topUnit</span></span>

```xpp
public Units topUnit([Units value])
```

### <a name="parameters---topunit"></a><span data-ttu-id="8974d-693">パラメーター - topUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-693">Parameters - topUnit</span></span>

<span data-ttu-id="8974d-694">値</span><span class="sxs-lookup"><span data-stu-id="8974d-694">value</span></span>  

### <a name="return-value---topunit"></a><span data-ttu-id="8974d-695">戻り値 - topUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-695">Return Value - topUnit</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="8974d-696">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="8974d-696">Method topValue</span></span>

```xpp
public Real topValue([Real value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="8974d-697">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="8974d-697">Parameters - topValue</span></span>

<span data-ttu-id="8974d-698">値</span><span class="sxs-lookup"><span data-stu-id="8974d-698">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="8974d-699">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="8974d-699">Return Value - topValue</span></span>

## <a name="method-visible"></a><span data-ttu-id="8974d-700">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="8974d-700">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="8974d-701">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="8974d-701">Parameters - visible</span></span>

<span data-ttu-id="8974d-702">値</span><span class="sxs-lookup"><span data-stu-id="8974d-702">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="8974d-703">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="8974d-703">Return Value - visible</span></span>

## <a name="method-warnifmissing"></a><span data-ttu-id="8974d-704">メソッド warnIfMissing</span><span class="sxs-lookup"><span data-stu-id="8974d-704">Method warnIfMissing</span></span>

```xpp
public boolean warnIfMissing([boolean value])
```

### <a name="parameters---warnifmissing"></a><span data-ttu-id="8974d-705">パラメーター - warnIfMissing</span><span class="sxs-lookup"><span data-stu-id="8974d-705">Parameters - warnIfMissing</span></span>

<span data-ttu-id="8974d-706">値</span><span class="sxs-lookup"><span data-stu-id="8974d-706">value</span></span>  

### <a name="return-value---warnifmissing"></a><span data-ttu-id="8974d-707">戻り値 - warnIfMissing</span><span class="sxs-lookup"><span data-stu-id="8974d-707">Return Value - warnIfMissing</span></span>

## <a name="method-webmenuitemname"></a><span data-ttu-id="8974d-708">メソッド webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="8974d-708">Method webMenuItemName</span></span>

```xpp
public str webMenuItemName([str value])
```

### <a name="parameters---webmenuitemname"></a><span data-ttu-id="8974d-709">パラメーター - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="8974d-709">Parameters - webMenuItemName</span></span>

<span data-ttu-id="8974d-710">値</span><span class="sxs-lookup"><span data-stu-id="8974d-710">value</span></span>  

### <a name="return-value---webmenuitemname"></a><span data-ttu-id="8974d-711">戻り値 - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="8974d-711">Return Value - webMenuItemName</span></span>

## <a name="method-webmenuitemtype"></a><span data-ttu-id="8974d-712">メソッド webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="8974d-712">Method webMenuItemType</span></span>

```xpp
public WebMenuItemType webMenuItemType([WebMenuItemType value])
```

### <a name="parameters---webmenuitemtype"></a><span data-ttu-id="8974d-713">パラメーター - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="8974d-713">Parameters - webMenuItemType</span></span>

<span data-ttu-id="8974d-714">値</span><span class="sxs-lookup"><span data-stu-id="8974d-714">value</span></span>  

### <a name="return-value---webmenuitemtype"></a><span data-ttu-id="8974d-715">戻り値 - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="8974d-715">Return Value - webMenuItemType</span></span>

## <a name="method-webtarget"></a><span data-ttu-id="8974d-716">メソッド webTarget</span><span class="sxs-lookup"><span data-stu-id="8974d-716">Method webTarget</span></span>

```xpp
public str webTarget([str value])
```

### <a name="parameters---webtarget"></a><span data-ttu-id="8974d-717">パラメーター - webTarget</span><span class="sxs-lookup"><span data-stu-id="8974d-717">Parameters - webTarget</span></span>

<span data-ttu-id="8974d-718">値</span><span class="sxs-lookup"><span data-stu-id="8974d-718">value</span></span>  

### <a name="return-value---webtarget"></a><span data-ttu-id="8974d-719">戻り値 - webTarget</span><span class="sxs-lookup"><span data-stu-id="8974d-719">Return Value - webTarget</span></span>

## <a name="method-width100mm"></a><span data-ttu-id="8974d-720">メソッド width100mm</span><span class="sxs-lookup"><span data-stu-id="8974d-720">Method width100mm</span></span>

```xpp
public int width100mm([int widthExclBorder])
```

### <a name="parameters---width100mm"></a><span data-ttu-id="8974d-721">パラメーター - width100mm</span><span class="sxs-lookup"><span data-stu-id="8974d-721">Parameters - width100mm</span></span>

<span data-ttu-id="8974d-722">widthExclBorder</span><span class="sxs-lookup"><span data-stu-id="8974d-722">widthExclBorder</span></span>  

### <a name="return-value---width100mm"></a><span data-ttu-id="8974d-723">戻り値 - width100mm</span><span class="sxs-lookup"><span data-stu-id="8974d-723">Return Value - width100mm</span></span>

## <a name="method-width100mminclborder"></a><span data-ttu-id="8974d-724">メソッド width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="8974d-724">Method width100mmInclBorder</span></span>

```xpp
public int width100mmInclBorder([int widthInclBorder])
```

### <a name="parameters---width100mminclborder"></a><span data-ttu-id="8974d-725">パラメーター - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="8974d-725">Parameters - width100mmInclBorder</span></span>

<span data-ttu-id="8974d-726">widthInclBorder</span><span class="sxs-lookup"><span data-stu-id="8974d-726">widthInclBorder</span></span>  

### <a name="return-value---width100mminclborder"></a><span data-ttu-id="8974d-727">戻り値 - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="8974d-727">Return Value - width100mmInclBorder</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="8974d-728">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="8974d-728">Method widthMode</span></span>

<span data-ttu-id="8974d-729">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-729">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="8974d-730">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="8974d-730">Parameters - widthMode</span></span>

<span data-ttu-id="8974d-731">値</span><span class="sxs-lookup"><span data-stu-id="8974d-731">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="8974d-732">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="8974d-732">Return Value - widthMode</span></span>

<span data-ttu-id="8974d-733">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="8974d-733">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="8974d-734">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="8974d-734">Remarks - widthMode</span></span>

<span data-ttu-id="8974d-735">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="8974d-735">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="8974d-736">モード。</span><span class="sxs-lookup"><span data-stu-id="8974d-736">Mode.</span></span>         | <span data-ttu-id="8974d-737">幅計算。</span><span class="sxs-lookup"><span data-stu-id="8974d-737">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8974d-738">正確。</span><span class="sxs-lookup"><span data-stu-id="8974d-738">Exact.</span></span>        | <span data-ttu-id="8974d-739">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="8974d-739">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="8974d-740">自動。</span><span class="sxs-lookup"><span data-stu-id="8974d-740">Auto.</span></span>         | <span data-ttu-id="8974d-741">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="8974d-741">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="8974d-742">列の幅。</span><span class="sxs-lookup"><span data-stu-id="8974d-742">Column width.</span></span> | <span data-ttu-id="8974d-743">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="8974d-743">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="8974d-744">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="8974d-744">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthofstring100mm"></a><span data-ttu-id="8974d-745">メソッド widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="8974d-745">Method widthOfString100mm</span></span>

```xpp
public int widthOfString100mm(str string)
```

### <a name="parameters---widthofstring100mm"></a><span data-ttu-id="8974d-746">パラメーター - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="8974d-746">Parameters - widthOfString100mm</span></span>

<span data-ttu-id="8974d-747">文字列</span><span class="sxs-lookup"><span data-stu-id="8974d-747">string</span></span>  

### <a name="return-value---widthofstring100mm"></a><span data-ttu-id="8974d-748">戻り値 - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="8974d-748">Return Value - widthOfString100mm</span></span>

## <a name="method-widthstr"></a><span data-ttu-id="8974d-749">メソッド widthStr</span><span class="sxs-lookup"><span data-stu-id="8974d-749">Method widthStr</span></span>

```xpp
public str widthStr([str value])
```

### <a name="parameters---widthstr"></a><span data-ttu-id="8974d-750">パラメーター - widthStr</span><span class="sxs-lookup"><span data-stu-id="8974d-750">Parameters - widthStr</span></span>

<span data-ttu-id="8974d-751">値</span><span class="sxs-lookup"><span data-stu-id="8974d-751">value</span></span>  

### <a name="return-value---widthstr"></a><span data-ttu-id="8974d-752">戻り値 - widthStr</span><span class="sxs-lookup"><span data-stu-id="8974d-752">Return Value - widthStr</span></span>

## <a name="method-widthunit"></a><span data-ttu-id="8974d-753">メソッド widthUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-753">Method widthUnit</span></span>

```xpp
public Units widthUnit([Units value])
```

### <a name="parameters---widthunit"></a><span data-ttu-id="8974d-754">パラメーター - widthUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-754">Parameters - widthUnit</span></span>

<span data-ttu-id="8974d-755">値</span><span class="sxs-lookup"><span data-stu-id="8974d-755">value</span></span>  

### <a name="return-value---widthunit"></a><span data-ttu-id="8974d-756">戻り値 - widthUnit</span><span class="sxs-lookup"><span data-stu-id="8974d-756">Return Value - widthUnit</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="8974d-757">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="8974d-757">Method widthValue</span></span>

<span data-ttu-id="8974d-758">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-758">Gets or sets the width of the control.</span></span>

```xpp
public Real widthValue([Real value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="8974d-759">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="8974d-759">Parameters - widthValue</span></span>

<span data-ttu-id="8974d-760">値</span><span class="sxs-lookup"><span data-stu-id="8974d-760">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="8974d-761">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="8974d-761">Return Value - widthValue</span></span>

<span data-ttu-id="8974d-762">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="8974d-762">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="8974d-763">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="8974d-763">Remarks - widthValue</span></span>

<span data-ttu-id="8974d-764">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="8974d-764">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="8974d-765">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="8974d-765">Method labelWidth</span></span>

```xpp
public void labelWidth(Real value, Units unit)
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="8974d-766">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="8974d-766">Parameters - labelWidth</span></span>

<span data-ttu-id="8974d-767">値</span><span class="sxs-lookup"><span data-stu-id="8974d-767">value</span></span>  

<!-- -->

<span data-ttu-id="8974d-768">単位</span><span class="sxs-lookup"><span data-stu-id="8974d-768">unit</span></span>  

## <a name="method-top"></a><span data-ttu-id="8974d-769">メソッド top</span><span class="sxs-lookup"><span data-stu-id="8974d-769">Method top</span></span>

```xpp
public void top(Real value, Units unit)
```

### <a name="parameters---top"></a><span data-ttu-id="8974d-770">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="8974d-770">Parameters - top</span></span>

<span data-ttu-id="8974d-771">値</span><span class="sxs-lookup"><span data-stu-id="8974d-771">value</span></span>  

<!-- -->

<span data-ttu-id="8974d-772">単位</span><span class="sxs-lookup"><span data-stu-id="8974d-772">unit</span></span>  

## <a name="method-show"></a><span data-ttu-id="8974d-773">メソッド show</span><span class="sxs-lookup"><span data-stu-id="8974d-773">Method show</span></span>

```xpp
public void show()
```

## <a name="method-rightmargin"></a><span data-ttu-id="8974d-774">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="8974d-774">Method rightMargin</span></span>

```xpp
public void rightMargin(Real value, Units unit)
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="8974d-775">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="8974d-775">Parameters - rightMargin</span></span>

<span data-ttu-id="8974d-776">値</span><span class="sxs-lookup"><span data-stu-id="8974d-776">value</span></span>  

<!-- -->

<span data-ttu-id="8974d-777">単位</span><span class="sxs-lookup"><span data-stu-id="8974d-777">unit</span></span>  

## <a name="method-left"></a><span data-ttu-id="8974d-778">メソッド left</span><span class="sxs-lookup"><span data-stu-id="8974d-778">Method left</span></span>

```xpp
public void left(Real value, Units unit)
```

### <a name="parameters---left"></a><span data-ttu-id="8974d-779">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="8974d-779">Parameters - left</span></span>

<span data-ttu-id="8974d-780">値</span><span class="sxs-lookup"><span data-stu-id="8974d-780">value</span></span>  

<!-- -->

<span data-ttu-id="8974d-781">単位</span><span class="sxs-lookup"><span data-stu-id="8974d-781">unit</span></span>  

## <a name="method-bottommargin"></a><span data-ttu-id="8974d-782">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="8974d-782">Method bottomMargin</span></span>

```xpp
public void bottomMargin(Real value, Units unit)
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="8974d-783">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="8974d-783">Parameters - bottomMargin</span></span>

<span data-ttu-id="8974d-784">値</span><span class="sxs-lookup"><span data-stu-id="8974d-784">value</span></span>  

<!-- -->

<span data-ttu-id="8974d-785">単位</span><span class="sxs-lookup"><span data-stu-id="8974d-785">unit</span></span>  

## <a name="method-height"></a><span data-ttu-id="8974d-786">メソッド height</span><span class="sxs-lookup"><span data-stu-id="8974d-786">Method height</span></span>

<span data-ttu-id="8974d-787">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-787">Gets or sets the height of the control.</span></span>

```xpp
public void height(Real value, Units unit)
```

### <a name="parameters---height"></a><span data-ttu-id="8974d-788">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="8974d-788">Parameters - height</span></span>

<span data-ttu-id="8974d-789">値</span><span class="sxs-lookup"><span data-stu-id="8974d-789">value</span></span>  

<!-- -->

<span data-ttu-id="8974d-790">単位</span><span class="sxs-lookup"><span data-stu-id="8974d-790">unit</span></span>  

### <a name="remarks---height"></a><span data-ttu-id="8974d-791">備考 - height</span><span class="sxs-lookup"><span data-stu-id="8974d-791">Remarks - height</span></span>

<span data-ttu-id="8974d-792">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="8974d-792">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="8974d-793">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="8974d-793">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="8974d-794">モード。</span><span class="sxs-lookup"><span data-stu-id="8974d-794">Mode.</span></span>            | <span data-ttu-id="8974d-795">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="8974d-795">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8974d-796">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="8974d-796">-1 Exact.</span></span>        | <span data-ttu-id="8974d-797">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="8974d-797">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="8974d-798">0 自動。</span><span class="sxs-lookup"><span data-stu-id="8974d-798">0 Auto.</span></span>          | <span data-ttu-id="8974d-799">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="8974d-799">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="8974d-800">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="8974d-800">1 Column height.</span></span> | <span data-ttu-id="8974d-801">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="8974d-801">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="8974d-802">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="8974d-802">The height and height calculation mode can be set separately.</span></span>

## <a name="method-hide"></a><span data-ttu-id="8974d-803">メソッド hide</span><span class="sxs-lookup"><span data-stu-id="8974d-803">Method hide</span></span>

```xpp
public void hide()
```

## <a name="method-topmargin"></a><span data-ttu-id="8974d-804">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="8974d-804">Method topMargin</span></span>

```xpp
public void topMargin(Real value, Units unit)
```

### <a name="parameters---topmargin"></a><span data-ttu-id="8974d-805">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="8974d-805">Parameters - topMargin</span></span>

<span data-ttu-id="8974d-806">値</span><span class="sxs-lookup"><span data-stu-id="8974d-806">value</span></span>  

<!-- -->

<span data-ttu-id="8974d-807">単位</span><span class="sxs-lookup"><span data-stu-id="8974d-807">unit</span></span>  

## <a name="method-leftmargin"></a><span data-ttu-id="8974d-808">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="8974d-808">Method leftMargin</span></span>

```xpp
public void leftMargin(Real value, Units unit)
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="8974d-809">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="8974d-809">Parameters - leftMargin</span></span>

<span data-ttu-id="8974d-810">値</span><span class="sxs-lookup"><span data-stu-id="8974d-810">value</span></span>  

<!-- -->

<span data-ttu-id="8974d-811">単位</span><span class="sxs-lookup"><span data-stu-id="8974d-811">unit</span></span>  

## <a name="method-width"></a><span data-ttu-id="8974d-812">メソッド width</span><span class="sxs-lookup"><span data-stu-id="8974d-812">Method width</span></span>

<span data-ttu-id="8974d-813">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="8974d-813">Gets or sets the width of the control.</span></span>

```xpp
public void width(Real value, Units unit)
```

### <a name="parameters---width"></a><span data-ttu-id="8974d-814">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="8974d-814">Parameters - width</span></span>

<span data-ttu-id="8974d-815">値</span><span class="sxs-lookup"><span data-stu-id="8974d-815">value</span></span>  

<!-- -->

<span data-ttu-id="8974d-816">単位</span><span class="sxs-lookup"><span data-stu-id="8974d-816">unit</span></span>  

### <a name="remarks---width"></a><span data-ttu-id="8974d-817">備考 - width</span><span class="sxs-lookup"><span data-stu-id="8974d-817">Remarks - width</span></span>

<span data-ttu-id="8974d-818">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="8974d-818">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="8974d-819">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="8974d-819">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="8974d-820">モード。</span><span class="sxs-lookup"><span data-stu-id="8974d-820">Mode.</span></span>           | <span data-ttu-id="8974d-821">幅計算。</span><span class="sxs-lookup"><span data-stu-id="8974d-821">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8974d-822">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="8974d-822">-1 Exact.</span></span>       | <span data-ttu-id="8974d-823">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="8974d-823">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="8974d-824">0 自動。</span><span class="sxs-lookup"><span data-stu-id="8974d-824">0 Auto.</span></span>         | <span data-ttu-id="8974d-825">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="8974d-825">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="8974d-826">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="8974d-826">1 Column width.</span></span> | <span data-ttu-id="8974d-827">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="8974d-827">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="8974d-828">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="8974d-828">The width and width calculation mode can be set separately.</span></span>

