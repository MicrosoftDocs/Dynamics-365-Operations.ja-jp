---
title: ReportPromptControl クラス
description: このトピックでは、ReportPromptControl クラスについて説明します。
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
ms.openlocfilehash: bba26d20906b1b32df0ceebf2dd89dfe3b0cc421
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502834"
---
# <a name="class-reportpromptcontrol"></a><span data-ttu-id="81fb5-103">クラス ReportPromptControl</span><span class="sxs-lookup"><span data-stu-id="81fb5-103">Class ReportPromptControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ReportPromptControl extends ReportControl
```

<span data-ttu-id="81fb5-104">ReportPromptControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="81fb5-104">The ReportPromptControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="81fb5-105">備考</span><span class="sxs-lookup"><span data-stu-id="81fb5-105">Remarks</span></span>

<span data-ttu-id="81fb5-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="81fb5-107">例</span><span class="sxs-lookup"><span data-stu-id="81fb5-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="81fb5-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="81fb5-108">Methods</span></span>

| <span data-ttu-id="81fb5-109">方法</span><span class="sxs-lookup"><span data-stu-id="81fb5-109">Method</span></span>                                                                   | <span data-ttu-id="81fb5-110">説明</span><span class="sxs-lookup"><span data-stu-id="81fb5-110">Description</span></span>                                                                                                                               |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81fb5-111">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-111">public int alignment(\[int value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="81fb5-112">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-112">public int arrayIndex(\[int value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="81fb5-113">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-113">public boolean autoDeclaration(\[boolean value\])</span></span>                        | <span data-ttu-id="81fb5-114">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-114">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                        |
| <span data-ttu-id="81fb5-115">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-115">public int backgroundColor(\[int value\])</span></span>                                | <span data-ttu-id="81fb5-116">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-116">Gets or sets the background color of the control.</span></span>                                                                                         |
| <span data-ttu-id="81fb5-117">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-117">public int backStyle(\[int value\])</span></span>                                      | <span data-ttu-id="81fb5-118">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-118">Determines whether the control background can be transparent.</span></span>                                                                            |
| <span data-ttu-id="81fb5-119">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-119">public int bold(\[int value\])</span></span>                                           | <span data-ttu-id="81fb5-120">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-120">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                               |
| <span data-ttu-id="81fb5-121">public int bottomMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="81fb5-121">public int bottomMarginAndFrame()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="81fb5-122">public int bottomMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-122">public int bottomMarginMode(\[int value\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="81fb5-123">public str bottomMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-123">public str bottomMarginStr(\[str value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="81fb5-124">public Units bottomMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-124">public Units bottomMarginUnit(\[Units value\])</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="81fb5-125">public Real bottomMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-125">public Real bottomMarginValue(\[Real value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="81fb5-126">public int changeCase(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-126">public int changeCase(\[int value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="81fb5-127">public int changeLabelCase(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-127">public int changeLabelCase(\[int value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="81fb5-128">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-128">public int characterSet(\[int value\])</span></span>                                   | <span data-ttu-id="81fb5-129">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-129">Gets or sets the character set of the font.</span></span>                                                                                               |
| <span data-ttu-id="81fb5-130">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-130">public int colorScheme(\[int value\])</span></span>                                    | <span data-ttu-id="81fb5-131">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-131">Gets or sets the color scheme of the control.</span></span>                                                                                             |
| <span data-ttu-id="81fb5-132">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-132">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="81fb5-133">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-133">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                       |
| <span data-ttu-id="81fb5-134">public ReportFieldType controlType()</span><span class="sxs-lookup"><span data-stu-id="81fb5-134">public ReportFieldType controlType()</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="81fb5-135">public str cssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-135">public str cssClass(\[str value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="81fb5-136">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-136">public FieldId dataField(\[FieldId value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="81fb5-137">public int delete()</span><span class="sxs-lookup"><span data-stu-id="81fb5-137">public int delete()</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="81fb5-138">public str effectiveFont()</span><span class="sxs-lookup"><span data-stu-id="81fb5-138">public str effectiveFont()</span></span>                                               |                                                                                                                                           |
| <span data-ttu-id="81fb5-139">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-139">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>         |                                                                                                                                           |
| <span data-ttu-id="81fb5-140">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-140">public str font(\[str value\])</span></span>                                           | <span data-ttu-id="81fb5-141">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-141">Gets or sets the name of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="81fb5-142">public str fontInfoPrinter()</span><span class="sxs-lookup"><span data-stu-id="81fb5-142">public str fontInfoPrinter()</span></span>                                             |                                                                                                                                           |
| <span data-ttu-id="81fb5-143">public int fontInfoPrinterAscent()</span><span class="sxs-lookup"><span data-stu-id="81fb5-143">public int fontInfoPrinterAscent()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="81fb5-144">public int fontInfoPrinterDescent()</span><span class="sxs-lookup"><span data-stu-id="81fb5-144">public int fontInfoPrinterDescent()</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="81fb5-145">public int fontInfoPrinterExtLead()</span><span class="sxs-lookup"><span data-stu-id="81fb5-145">public int fontInfoPrinterExtLead()</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="81fb5-146">public int fontInfoPrinterHeight()</span><span class="sxs-lookup"><span data-stu-id="81fb5-146">public int fontInfoPrinterHeight()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="81fb5-147">public int fontInfoPrinterIntLead()</span><span class="sxs-lookup"><span data-stu-id="81fb5-147">public int fontInfoPrinterIntLead()</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="81fb5-148">public str fontInfoScreen()</span><span class="sxs-lookup"><span data-stu-id="81fb5-148">public str fontInfoScreen()</span></span>                                              |                                                                                                                                           |
| <span data-ttu-id="81fb5-149">public int fontInfoScreenAscent()</span><span class="sxs-lookup"><span data-stu-id="81fb5-149">public int fontInfoScreenAscent()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="81fb5-150">public int fontInfoScreenDescent()</span><span class="sxs-lookup"><span data-stu-id="81fb5-150">public int fontInfoScreenDescent()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="81fb5-151">public int fontInfoScreenExtLead()</span><span class="sxs-lookup"><span data-stu-id="81fb5-151">public int fontInfoScreenExtLead()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="81fb5-152">public int fontInfoScreenHeight()</span><span class="sxs-lookup"><span data-stu-id="81fb5-152">public int fontInfoScreenHeight()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="81fb5-153">public int fontInfoScreenIntLead()</span><span class="sxs-lookup"><span data-stu-id="81fb5-153">public int fontInfoScreenIntLead()</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="81fb5-154">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-154">public int fontSize(\[int value\])</span></span>                                       | <span data-ttu-id="81fb5-155">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-155">Gets or sets the size of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="81fb5-156">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-156">public int foregroundColor(\[int value\])</span></span>                                | <span data-ttu-id="81fb5-157">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-157">Gets or sets the text color for the control to use.</span></span>                                                                                       |
| <span data-ttu-id="81fb5-158">public int height100mm(\[int heightExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-158">public int height100mm(\[int heightExclBorder\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="81fb5-159">public int height100mmInclBorder(\[int heightInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-159">public int height100mmInclBorder(\[int heightInclBorder\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="81fb5-160">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-160">public int heightMode(\[int value\])</span></span>                                     | <span data-ttu-id="81fb5-161">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-161">Gets or sets a calculation mode for the height of the control.</span></span>                                                                            |
| <span data-ttu-id="81fb5-162">public int heightOfWordWrappedString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="81fb5-162">public int heightOfWordWrappedString100mm(str string)</span></span>                    |                                                                                                                                           |
| <span data-ttu-id="81fb5-163">public str heightStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-163">public str heightStr(\[str value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="81fb5-164">public Units heightUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-164">public Units heightUnit(\[Units value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="81fb5-165">public Real heightValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-165">public Real heightValue(\[Real value\])</span></span>                                  | <span data-ttu-id="81fb5-166">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-166">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="81fb5-167">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-167">public boolean italic(\[boolean value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="81fb5-168">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-168">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="81fb5-169">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-169">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="81fb5-170">public str labelCssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-170">public str labelCssClass(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="81fb5-171">public LineType labelLineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-171">public LineType labelLineBelow(\[LineType value\])</span></span>                       |                                                                                                                                           |
| <span data-ttu-id="81fb5-172">public LineThickness labelLineThickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-172">public LineThickness labelLineThickness(\[LineThickness value\])</span></span>         |                                                                                                                                           |
| <span data-ttu-id="81fb5-173">public int left100mm(\[int leftExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-173">public int left100mm(\[int leftExclBorder\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="81fb5-174">public int left100mmInclBorder(\[int leftInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-174">public int left100mmInclBorder(\[int leftInclBorder\])</span></span>                   |                                                                                                                                           |
| <span data-ttu-id="81fb5-175">public int leftMarginAnFrame()</span><span class="sxs-lookup"><span data-stu-id="81fb5-175">public int leftMarginAnFrame()</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="81fb5-176">public int leftMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-176">public int leftMarginMode(\[int value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="81fb5-177">public str leftMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-177">public str leftMarginStr(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="81fb5-178">public Units leftMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-178">public Units leftMarginUnit(\[Units value\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="81fb5-179">public Real leftMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-179">public Real leftMarginValue(\[Real value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="81fb5-180">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-180">public int leftMode(\[int value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="81fb5-181">public str leftStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-181">public str leftStr(\[str value\])</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="81fb5-182">public Units leftUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-182">public Units leftUnit(\[Units value\])</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="81fb5-183">public Real leftValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-183">public Real leftValue(\[Real value\])</span></span>                                    |                                                                                                                                           |
| <span data-ttu-id="81fb5-184">public LineType lineAbove(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-184">public LineType lineAbove(\[LineType value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="81fb5-185">public LineType lineBelow(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-185">public LineType lineBelow(\[LineType value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="81fb5-186">public LineType lineLeft(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-186">public LineType lineLeft(\[LineType value\])</span></span>                             | <span data-ttu-id="81fb5-187">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-187">Gets or sets the type of line that is used as the left border of a section.</span></span>                                                               |
| <span data-ttu-id="81fb5-188">public LineType lineRight(\[LineType value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-188">public LineType lineRight(\[LineType value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="81fb5-189">public str menuItemLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-189">public str menuItemLabel(\[str value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="81fb5-190">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-190">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="81fb5-191">public MenuItemType menuItemType(\[MenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-191">public MenuItemType menuItemType(\[MenuItemType value\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="81fb5-192">public str modelFieldName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-192">public str modelFieldName(\[str value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="81fb5-193">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-193">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="81fb5-194">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-194">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="81fb5-195">public int numberOfLines(int height100mm)</span><span class="sxs-lookup"><span data-stu-id="81fb5-195">public int numberOfLines(int height100mm)</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="81fb5-196">public int position(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-196">public int position(\[int value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="81fb5-197">public str previewInfo(str string)</span><span class="sxs-lookup"><span data-stu-id="81fb5-197">public str previewInfo(str string)</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="81fb5-198">public int previewXCompensation100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="81fb5-198">public int previewXCompensation100mm(str string)</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="81fb5-199">public int right100mm()</span><span class="sxs-lookup"><span data-stu-id="81fb5-199">public int right100mm()</span></span>                                                  |                                                                                                                                           |
| <span data-ttu-id="81fb5-200">public int right100mmInclBorder()</span><span class="sxs-lookup"><span data-stu-id="81fb5-200">public int right100mmInclBorder()</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="81fb5-201">public int rightMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="81fb5-201">public int rightMarginAndFrame()</span></span>                                         |                                                                                                                                           |
| <span data-ttu-id="81fb5-202">public int rightMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-202">public int rightMarginMode(\[int value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="81fb5-203">public str rightMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-203">public str rightMarginStr(\[str value\])</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="81fb5-204">public Units rightMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-204">public Units rightMarginUnit(\[Units value\])</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="81fb5-205">public Real rightMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-205">public Real rightMarginValue(\[Real value\])</span></span>                             |                                                                                                                                           |
| <span data-ttu-id="81fb5-206">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-206">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                                           |
| <span data-ttu-id="81fb5-207">public str setHeightGetText(int lines, str string)</span><span class="sxs-lookup"><span data-stu-id="81fb5-207">public str setHeightGetText(int lines, str string)</span></span>                       |                                                                                                                                           |
| <span data-ttu-id="81fb5-208">public TableId table(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-208">public TableId table(\[TableId value\])</span></span>                                  | <span data-ttu-id="81fb5-209">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-209">Gets or sets the table ID associated with the object.</span></span>                                                                                     |
| <span data-ttu-id="81fb5-210">public LineThickness thickness(\[LineThickness value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-210">public LineThickness thickness(\[LineThickness value\])</span></span>                  |                                                                                                                                           |
| <span data-ttu-id="81fb5-211">public int top100mm(\[int topExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-211">public int top100mm(\[int topExclBorder\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="81fb5-212">public int top100mmInclBorder(\[int topInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-212">public int top100mmInclBorder(\[int topInclBorder\])</span></span>                     |                                                                                                                                           |
| <span data-ttu-id="81fb5-213">public int topMarginAndFrame()</span><span class="sxs-lookup"><span data-stu-id="81fb5-213">public int topMarginAndFrame()</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="81fb5-214">public int topMarginMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-214">public int topMarginMode(\[int value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="81fb5-215">public str topMarginStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-215">public str topMarginStr(\[str value\])</span></span>                                   |                                                                                                                                           |
| <span data-ttu-id="81fb5-216">public Units topMarginUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-216">public Units topMarginUnit(\[Units value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="81fb5-217">public Real topMarginValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-217">public Real topMarginValue(\[Real value\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="81fb5-218">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-218">public int topMode(\[int value\])</span></span>                                        |                                                                                                                                           |
| <span data-ttu-id="81fb5-219">public str topStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-219">public str topStr(\[str value\])</span></span>                                         |                                                                                                                                           |
| <span data-ttu-id="81fb5-220">public Units topUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-220">public Units topUnit(\[Units value\])</span></span>                                    |                                                                                                                                           |
| <span data-ttu-id="81fb5-221">public Real topValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-221">public Real topValue(\[Real value\])</span></span>                                     |                                                                                                                                           |
| <span data-ttu-id="81fb5-222">public int typeHeaderPrompt(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-222">public int typeHeaderPrompt(\[int value\])</span></span>                               |                                                                                                                                           |
| <span data-ttu-id="81fb5-223">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-223">public boolean underline(\[boolean value\])</span></span>                              |                                                                                                                                           |
| <span data-ttu-id="81fb5-224">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-224">public boolean visible(\[boolean value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="81fb5-225">public str webMenuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-225">public str webMenuItemName(\[str value\])</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="81fb5-226">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-226">public WebMenuItemType webMenuItemType(\[WebMenuItemType value\])</span></span>        |                                                                                                                                           |
| <span data-ttu-id="81fb5-227">public str webTarget(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-227">public str webTarget(\[str value\])</span></span>                                      |                                                                                                                                           |
| <span data-ttu-id="81fb5-228">public int width100mm(\[int widthExclBorder\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-228">public int width100mm(\[int widthExclBorder\])</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="81fb5-229">public int width100mmInclBorder(\[int widthInclBorder\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-229">public int width100mmInclBorder(\[int widthInclBorder\])</span></span>                 |                                                                                                                                           |
| <span data-ttu-id="81fb5-230">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-230">public int widthMode(\[int value\])</span></span>                                      | <span data-ttu-id="81fb5-231">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-231">Gets or sets the calculation mode of the width of the control.</span></span>                                                                            |
| <span data-ttu-id="81fb5-232">public int widthOfString100mm(str string)</span><span class="sxs-lookup"><span data-stu-id="81fb5-232">public int widthOfString100mm(str string)</span></span>                                |                                                                                                                                           |
| <span data-ttu-id="81fb5-233">public str widthStr(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-233">public str widthStr(\[str value\])</span></span>                                       |                                                                                                                                           |
| <span data-ttu-id="81fb5-234">public Units widthUnit(\[Units value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-234">public Units widthUnit(\[Units value\])</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="81fb5-235">public Real widthValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="81fb5-235">public Real widthValue(\[Real value\])</span></span>                                   | <span data-ttu-id="81fb5-236">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-236">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="81fb5-237">public void width(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="81fb5-237">public void width(Real value, Units unit)</span></span>                                | <span data-ttu-id="81fb5-238">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-238">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="81fb5-239">public void bottomMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="81fb5-239">public void bottomMargin(Real value, Units unit)</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="81fb5-240">public void rightMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="81fb5-240">public void rightMargin(Real value, Units unit)</span></span>                          |                                                                                                                                           |
| <span data-ttu-id="81fb5-241">public void leftMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="81fb5-241">public void leftMargin(Real value, Units unit)</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="81fb5-242">public void topMargin(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="81fb5-242">public void topMargin(Real value, Units unit)</span></span>                            |                                                                                                                                           |
| <span data-ttu-id="81fb5-243">public void top(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="81fb5-243">public void top(Real value, Units unit)</span></span>                                  |                                                                                                                                           |
| <span data-ttu-id="81fb5-244">public void left(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="81fb5-244">public void left(Real value, Units unit)</span></span>                                 |                                                                                                                                           |
| <span data-ttu-id="81fb5-245">public void show()</span><span class="sxs-lookup"><span data-stu-id="81fb5-245">public void show()</span></span>                                                       |                                                                                                                                           |
| <span data-ttu-id="81fb5-246">public void height(Real value, Units unit)</span><span class="sxs-lookup"><span data-stu-id="81fb5-246">public void height(Real value, Units unit)</span></span>                               | <span data-ttu-id="81fb5-247">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-247">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="81fb5-248">public void hide()</span><span class="sxs-lookup"><span data-stu-id="81fb5-248">public void hide()</span></span>                                                       |                                                                                                                                           |

## <a name="method-alignment"></a><span data-ttu-id="81fb5-249">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="81fb5-249">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="81fb5-250">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="81fb5-250">Parameters - alignment</span></span>

<span data-ttu-id="81fb5-251">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-251">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="81fb5-252">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="81fb5-252">Return Value - alignment</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="81fb5-253">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="81fb5-253">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="81fb5-254">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="81fb5-254">Parameters - arrayIndex</span></span>

<span data-ttu-id="81fb5-255">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-255">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="81fb5-256">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="81fb5-256">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="81fb5-257">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="81fb5-257">Method autoDeclaration</span></span>

<span data-ttu-id="81fb5-258">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-258">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="81fb5-259">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="81fb5-259">Parameters - autoDeclaration</span></span>

<span data-ttu-id="81fb5-260">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-260">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="81fb5-261">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="81fb5-261">Return Value - autoDeclaration</span></span>

<span data-ttu-id="81fb5-262">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="81fb5-262">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="81fb5-263">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="81fb5-263">Remarks - autoDeclaration</span></span>

<span data-ttu-id="81fb5-264">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="81fb5-264">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="81fb5-265">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="81fb5-265">Method backgroundColor</span></span>

<span data-ttu-id="81fb5-266">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-266">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="81fb5-267">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="81fb5-267">Parameters - backgroundColor</span></span>

<span data-ttu-id="81fb5-268">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-268">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="81fb5-269">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="81fb5-269">Return Value - backgroundColor</span></span>

<span data-ttu-id="81fb5-270">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="81fb5-270">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="81fb5-271">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="81fb5-271">Remarks - backgroundColor</span></span>

<span data-ttu-id="81fb5-272">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="81fb5-272">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="81fb5-273">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="81fb5-273">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="81fb5-274">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="81fb5-274">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="81fb5-275">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="81fb5-275">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="81fb5-276">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="81fb5-276">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="81fb5-277">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="81fb5-277">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="81fb5-278">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="81fb5-278">Method backStyle</span></span>

<span data-ttu-id="81fb5-279">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-279">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="81fb5-280">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="81fb5-280">Parameters - backStyle</span></span>

<span data-ttu-id="81fb5-281">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-281">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="81fb5-282">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="81fb5-282">Return Value - backStyle</span></span>

<span data-ttu-id="81fb5-283">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="81fb5-283">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="81fb5-284">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="81fb5-284">Method bold</span></span>

<span data-ttu-id="81fb5-285">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-285">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="81fb5-286">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="81fb5-286">Parameters - bold</span></span>

<span data-ttu-id="81fb5-287">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-287">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="81fb5-288">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="81fb5-288">Return Value - bold</span></span>

<span data-ttu-id="81fb5-289">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="81fb5-289">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="81fb5-290">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="81fb5-290">Remarks - bold</span></span>

<span data-ttu-id="81fb5-291">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="81fb5-291">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="81fb5-292">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-292">0 Use the default font weight.</span></span>
-   <span data-ttu-id="81fb5-293">1 シン。</span><span class="sxs-lookup"><span data-stu-id="81fb5-293">1 Thin.</span></span>
-   <span data-ttu-id="81fb5-294">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="81fb5-294">2 Extra-light.</span></span>
-   <span data-ttu-id="81fb5-295">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="81fb5-295">3 Light.</span></span>
-   <span data-ttu-id="81fb5-296">4 標準。</span><span class="sxs-lookup"><span data-stu-id="81fb5-296">4 Normal.</span></span>
-   <span data-ttu-id="81fb5-297">5 中。</span><span class="sxs-lookup"><span data-stu-id="81fb5-297">5 Medium.</span></span>
-   <span data-ttu-id="81fb5-298">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="81fb5-298">6 Semibold.</span></span>
-   <span data-ttu-id="81fb5-299">7 太字。</span><span class="sxs-lookup"><span data-stu-id="81fb5-299">7 Bold.</span></span>
-   <span data-ttu-id="81fb5-300">8 極太。</span><span class="sxs-lookup"><span data-stu-id="81fb5-300">8 Extra-bold.</span></span>
-   <span data-ttu-id="81fb5-301">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="81fb5-301">9 Heavy.</span></span>

## <a name="method-bottommarginandframe"></a><span data-ttu-id="81fb5-302">メソッド bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="81fb5-302">Method bottomMarginAndFrame</span></span>

```xpp
public int bottomMarginAndFrame()
```

### <a name="return-value---bottommarginandframe"></a><span data-ttu-id="81fb5-303">戻り値 - bottomMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="81fb5-303">Return Value - bottomMarginAndFrame</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="81fb5-304">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-304">Method bottomMarginMode</span></span>

```xpp
public int bottomMarginMode([int value])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="81fb5-305">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-305">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="81fb5-306">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-306">value</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="81fb5-307">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-307">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginstr"></a><span data-ttu-id="81fb5-308">メソッド bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-308">Method bottomMarginStr</span></span>

```xpp
public str bottomMarginStr([str value])
```

### <a name="parameters---bottommarginstr"></a><span data-ttu-id="81fb5-309">パラメーター - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-309">Parameters - bottomMarginStr</span></span>

<span data-ttu-id="81fb5-310">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-310">value</span></span>  

### <a name="return-value---bottommarginstr"></a><span data-ttu-id="81fb5-311">戻り値 - bottomMarginStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-311">Return Value - bottomMarginStr</span></span>

## <a name="method-bottommarginunit"></a><span data-ttu-id="81fb5-312">メソッド bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="81fb5-312">Method bottomMarginUnit</span></span>

```xpp
public Units bottomMarginUnit([Units value])
```

### <a name="parameters---bottommarginunit"></a><span data-ttu-id="81fb5-313">パラメーター - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="81fb5-313">Parameters - bottomMarginUnit</span></span>

<span data-ttu-id="81fb5-314">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-314">value</span></span>  

### <a name="return-value---bottommarginunit"></a><span data-ttu-id="81fb5-315">戻り値 - bottomMarginUnit</span><span class="sxs-lookup"><span data-stu-id="81fb5-315">Return Value - bottomMarginUnit</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="81fb5-316">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-316">Method bottomMarginValue</span></span>

```xpp
public Real bottomMarginValue([Real value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="81fb5-317">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-317">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="81fb5-318">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-318">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="81fb5-319">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-319">Return Value - bottomMarginValue</span></span>

## <a name="method-changecase"></a><span data-ttu-id="81fb5-320">メソッド changeCase</span><span class="sxs-lookup"><span data-stu-id="81fb5-320">Method changeCase</span></span>

```xpp
public int changeCase([int value])
```

### <a name="parameters---changecase"></a><span data-ttu-id="81fb5-321">パラメーター - changeCase</span><span class="sxs-lookup"><span data-stu-id="81fb5-321">Parameters - changeCase</span></span>

<span data-ttu-id="81fb5-322">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-322">value</span></span>  

### <a name="return-value---changecase"></a><span data-ttu-id="81fb5-323">戻り値 - changeCase</span><span class="sxs-lookup"><span data-stu-id="81fb5-323">Return Value - changeCase</span></span>

## <a name="method-changelabelcase"></a><span data-ttu-id="81fb5-324">メソッド changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="81fb5-324">Method changeLabelCase</span></span>

```xpp
public int changeLabelCase([int value])
```

### <a name="parameters---changelabelcase"></a><span data-ttu-id="81fb5-325">パラメーター - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="81fb5-325">Parameters - changeLabelCase</span></span>

<span data-ttu-id="81fb5-326">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-326">value</span></span>  

### <a name="return-value---changelabelcase"></a><span data-ttu-id="81fb5-327">戻り値 - changeLabelCase</span><span class="sxs-lookup"><span data-stu-id="81fb5-327">Return Value - changeLabelCase</span></span>

## <a name="method-characterset"></a><span data-ttu-id="81fb5-328">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="81fb5-328">Method characterSet</span></span>

<span data-ttu-id="81fb5-329">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-329">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="81fb5-330">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="81fb5-330">Parameters - characterSet</span></span>

<span data-ttu-id="81fb5-331">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-331">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="81fb5-332">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="81fb5-332">Return Value - characterSet</span></span>

<span data-ttu-id="81fb5-333">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="81fb5-333">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="81fb5-334">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="81fb5-334">Remarks - characterSet</span></span>

<span data-ttu-id="81fb5-335">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-335">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="81fb5-336">値です。</span><span class="sxs-lookup"><span data-stu-id="81fb5-336">Value.</span></span> | <span data-ttu-id="81fb5-337">説明。</span><span class="sxs-lookup"><span data-stu-id="81fb5-337">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="81fb5-338">0</span><span class="sxs-lookup"><span data-stu-id="81fb5-338">0</span></span>      | <span data-ttu-id="81fb5-339">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="81fb5-339">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="81fb5-340">1</span><span class="sxs-lookup"><span data-stu-id="81fb5-340">1</span></span>      | <span data-ttu-id="81fb5-341">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="81fb5-341">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="81fb5-342">2</span><span class="sxs-lookup"><span data-stu-id="81fb5-342">2</span></span>      | <span data-ttu-id="81fb5-343">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="81fb5-343">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="81fb5-344">77</span><span class="sxs-lookup"><span data-stu-id="81fb5-344">77</span></span>     | <span data-ttu-id="81fb5-345">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="81fb5-345">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="81fb5-346">128</span><span class="sxs-lookup"><span data-stu-id="81fb5-346">128</span></span>    | <span data-ttu-id="81fb5-347">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="81fb5-347">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="81fb5-348">129</span><span class="sxs-lookup"><span data-stu-id="81fb5-348">129</span></span>    | <span data-ttu-id="81fb5-349">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="81fb5-349">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="81fb5-350">134</span><span class="sxs-lookup"><span data-stu-id="81fb5-350">134</span></span>    | <span data-ttu-id="81fb5-351">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="81fb5-351">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="81fb5-352">136</span><span class="sxs-lookup"><span data-stu-id="81fb5-352">136</span></span>    | <span data-ttu-id="81fb5-353">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="81fb5-353">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="81fb5-354">161</span><span class="sxs-lookup"><span data-stu-id="81fb5-354">161</span></span>    | <span data-ttu-id="81fb5-355">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="81fb5-355">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="81fb5-356">162</span><span class="sxs-lookup"><span data-stu-id="81fb5-356">162</span></span>    | <span data-ttu-id="81fb5-357">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="81fb5-357">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="81fb5-358">163</span><span class="sxs-lookup"><span data-stu-id="81fb5-358">163</span></span>    | <span data-ttu-id="81fb5-359">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="81fb5-359">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="81fb5-360">186</span><span class="sxs-lookup"><span data-stu-id="81fb5-360">186</span></span>    | <span data-ttu-id="81fb5-361">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="81fb5-361">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="81fb5-362">204</span><span class="sxs-lookup"><span data-stu-id="81fb5-362">204</span></span>    | <span data-ttu-id="81fb5-363">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="81fb5-363">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="81fb5-364">238</span><span class="sxs-lookup"><span data-stu-id="81fb5-364">238</span></span>    | <span data-ttu-id="81fb5-365">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="81fb5-365">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="81fb5-366">255</span><span class="sxs-lookup"><span data-stu-id="81fb5-366">255</span></span>    | <span data-ttu-id="81fb5-367">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="81fb5-367">OEM\_CHARSET</span></span>         |

<span data-ttu-id="81fb5-368">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="81fb5-368">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="81fb5-369">値です。</span><span class="sxs-lookup"><span data-stu-id="81fb5-369">Value.</span></span> | <span data-ttu-id="81fb5-370">説明。</span><span class="sxs-lookup"><span data-stu-id="81fb5-370">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="81fb5-371">130</span><span class="sxs-lookup"><span data-stu-id="81fb5-371">130</span></span>    | <span data-ttu-id="81fb5-372">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="81fb5-372">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="81fb5-373">次のテーブルの値は、中東言語語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="81fb5-373">The values in the following table are for the Middle East language edition of Windows.</span></span>

| <span data-ttu-id="81fb5-374">値です。</span><span class="sxs-lookup"><span data-stu-id="81fb5-374">Value.</span></span> | <span data-ttu-id="81fb5-375">説明。</span><span class="sxs-lookup"><span data-stu-id="81fb5-375">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="81fb5-376">177</span><span class="sxs-lookup"><span data-stu-id="81fb5-376">177</span></span>    | <span data-ttu-id="81fb5-377">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="81fb5-377">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="81fb5-378">178</span><span class="sxs-lookup"><span data-stu-id="81fb5-378">178</span></span>    | <span data-ttu-id="81fb5-379">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="81fb5-379">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="81fb5-380">次のテーブルの値は、タイ語版 Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="81fb5-380">The value in the following table is for the Thai language edition of Windows.</span></span>

| <span data-ttu-id="81fb5-381">値です。</span><span class="sxs-lookup"><span data-stu-id="81fb5-381">Value.</span></span> | <span data-ttu-id="81fb5-382">説明。</span><span class="sxs-lookup"><span data-stu-id="81fb5-382">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="81fb5-383">222</span><span class="sxs-lookup"><span data-stu-id="81fb5-383">222</span></span>    | <span data-ttu-id="81fb5-384">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="81fb5-384">THAI\_CHARSET</span></span> |

<span data-ttu-id="81fb5-385">既定の文字セットは、現在のシステム ロケールに基づく値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="81fb5-385">The default character set is set to a value that is based on the current system locale.</span></span> <span data-ttu-id="81fb5-386">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="81fb5-386">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="81fb5-387">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="81fb5-387">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="81fb5-388">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="81fb5-388">Method colorScheme</span></span>

<span data-ttu-id="81fb5-389">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-389">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="81fb5-390">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="81fb5-390">Parameters - colorScheme</span></span>

<span data-ttu-id="81fb5-391">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-391">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="81fb5-392">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="81fb5-392">Return Value - colorScheme</span></span>

<span data-ttu-id="81fb5-393">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="81fb5-393">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="81fb5-394">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="81fb5-394">Remarks - colorScheme</span></span>

<span data-ttu-id="81fb5-395">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="81fb5-395">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="81fb5-396">値です。</span><span class="sxs-lookup"><span data-stu-id="81fb5-396">Value.</span></span> | <span data-ttu-id="81fb5-397">スタイル。</span><span class="sxs-lookup"><span data-stu-id="81fb5-397">Style.</span></span>                 |
|--------|------------------------|
| <span data-ttu-id="81fb5-398">0</span><span class="sxs-lookup"><span data-stu-id="81fb5-398">0</span></span>      | <span data-ttu-id="81fb5-399">既定。</span><span class="sxs-lookup"><span data-stu-id="81fb5-399">Default.</span></span>               |
| <span data-ttu-id="81fb5-400">1</span><span class="sxs-lookup"><span data-stu-id="81fb5-400">1</span></span>      | <span data-ttu-id="81fb5-401">Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="81fb5-401">The Windows palette.</span></span>   |
| <span data-ttu-id="81fb5-402">2</span><span class="sxs-lookup"><span data-stu-id="81fb5-402">2</span></span>      | <span data-ttu-id="81fb5-403">真の配色。</span><span class="sxs-lookup"><span data-stu-id="81fb5-403">The true-color scheme.</span></span> |

## <a name="method-configurationkey"></a><span data-ttu-id="81fb5-404">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="81fb5-404">Method configurationKey</span></span>

<span data-ttu-id="81fb5-405">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-405">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="81fb5-406">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="81fb5-406">Parameters - configurationKey</span></span>

<span data-ttu-id="81fb5-407">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-407">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="81fb5-408">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="81fb5-408">Return Value - configurationKey</span></span>

<span data-ttu-id="81fb5-409">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="81fb5-409">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="81fb5-410">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="81fb5-410">Remarks - configurationKey</span></span>

<span data-ttu-id="81fb5-411">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="81fb5-411">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="81fb5-412">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="81fb5-412">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-controltype"></a><span data-ttu-id="81fb5-413">メソッド controlType</span><span class="sxs-lookup"><span data-stu-id="81fb5-413">Method controlType</span></span>

```xpp
public ReportFieldType controlType()
```

### <a name="return-value---controltype"></a><span data-ttu-id="81fb5-414">戻り値 - controlType</span><span class="sxs-lookup"><span data-stu-id="81fb5-414">Return Value - controlType</span></span>

## <a name="method-cssclass"></a><span data-ttu-id="81fb5-415">メソッド cssClass</span><span class="sxs-lookup"><span data-stu-id="81fb5-415">Method cssClass</span></span>

```xpp
public str cssClass([str value])
```

### <a name="parameters---cssclass"></a><span data-ttu-id="81fb5-416">パラメーター - cssClass</span><span class="sxs-lookup"><span data-stu-id="81fb5-416">Parameters - cssClass</span></span>

<span data-ttu-id="81fb5-417">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-417">value</span></span>  

### <a name="return-value---cssclass"></a><span data-ttu-id="81fb5-418">戻り値 - cssClass</span><span class="sxs-lookup"><span data-stu-id="81fb5-418">Return Value - cssClass</span></span>

## <a name="method-datafield"></a><span data-ttu-id="81fb5-419">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="81fb5-419">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="81fb5-420">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="81fb5-420">Parameters - dataField</span></span>

<span data-ttu-id="81fb5-421">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-421">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="81fb5-422">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="81fb5-422">Return Value - dataField</span></span>

## <a name="method-delete"></a><span data-ttu-id="81fb5-423">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="81fb5-423">Method delete</span></span>

```xpp
public int delete()
```

### <a name="return-value---delete"></a><span data-ttu-id="81fb5-424">戻り値 - delete</span><span class="sxs-lookup"><span data-stu-id="81fb5-424">Return Value - delete</span></span>

## <a name="method-effectivefont"></a><span data-ttu-id="81fb5-425">メソッド effectiveFont</span><span class="sxs-lookup"><span data-stu-id="81fb5-425">Method effectiveFont</span></span>

```xpp
public str effectiveFont()
```

### <a name="return-value---effectivefont"></a><span data-ttu-id="81fb5-426">戻り値 - effectiveFont</span><span class="sxs-lookup"><span data-stu-id="81fb5-426">Return Value - effectiveFont</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="81fb5-427">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="81fb5-427">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="81fb5-428">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="81fb5-428">Parameters - extendedDataType</span></span>

<span data-ttu-id="81fb5-429">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-429">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="81fb5-430">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="81fb5-430">Return Value - extendedDataType</span></span>

## <a name="method-font"></a><span data-ttu-id="81fb5-431">メソッド font</span><span class="sxs-lookup"><span data-stu-id="81fb5-431">Method font</span></span>

<span data-ttu-id="81fb5-432">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-432">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="81fb5-433">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="81fb5-433">Parameters - font</span></span>

<span data-ttu-id="81fb5-434">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-434">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="81fb5-435">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="81fb5-435">Return Value - font</span></span>

<span data-ttu-id="81fb5-436">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="81fb5-436">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontinfoprinter"></a><span data-ttu-id="81fb5-437">メソッド fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="81fb5-437">Method fontInfoPrinter</span></span>

```xpp
public str fontInfoPrinter()
```

### <a name="return-value---fontinfoprinter"></a><span data-ttu-id="81fb5-438">戻り値 - fontInfoPrinter</span><span class="sxs-lookup"><span data-stu-id="81fb5-438">Return Value - fontInfoPrinter</span></span>

## <a name="method-fontinfoprinterascent"></a><span data-ttu-id="81fb5-439">メソッド fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="81fb5-439">Method fontInfoPrinterAscent</span></span>

```xpp
public int fontInfoPrinterAscent()
```

### <a name="return-value---fontinfoprinterascent"></a><span data-ttu-id="81fb5-440">戻り値 - fontInfoPrinterAscent</span><span class="sxs-lookup"><span data-stu-id="81fb5-440">Return Value - fontInfoPrinterAscent</span></span>

## <a name="method-fontinfoprinterdescent"></a><span data-ttu-id="81fb5-441">メソッド fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="81fb5-441">Method fontInfoPrinterDescent</span></span>

```xpp
public int fontInfoPrinterDescent()
```

### <a name="return-value---fontinfoprinterdescent"></a><span data-ttu-id="81fb5-442">戻り値 - fontInfoPrinterDescent</span><span class="sxs-lookup"><span data-stu-id="81fb5-442">Return Value - fontInfoPrinterDescent</span></span>

## <a name="method-fontinfoprinterextlead"></a><span data-ttu-id="81fb5-443">メソッド fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="81fb5-443">Method fontInfoPrinterExtLead</span></span>

```xpp
public int fontInfoPrinterExtLead()
```

### <a name="return-value---fontinfoprinterextlead"></a><span data-ttu-id="81fb5-444">戻り値 - fontInfoPrinterExtLead</span><span class="sxs-lookup"><span data-stu-id="81fb5-444">Return Value - fontInfoPrinterExtLead</span></span>

## <a name="method-fontinfoprinterheight"></a><span data-ttu-id="81fb5-445">メソッド fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="81fb5-445">Method fontInfoPrinterHeight</span></span>

```xpp
public int fontInfoPrinterHeight()
```

### <a name="return-value---fontinfoprinterheight"></a><span data-ttu-id="81fb5-446">戻り値 - fontInfoPrinterHeight</span><span class="sxs-lookup"><span data-stu-id="81fb5-446">Return Value - fontInfoPrinterHeight</span></span>

## <a name="method-fontinfoprinterintlead"></a><span data-ttu-id="81fb5-447">メソッド fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="81fb5-447">Method fontInfoPrinterIntLead</span></span>

```xpp
public int fontInfoPrinterIntLead()
```

### <a name="return-value---fontinfoprinterintlead"></a><span data-ttu-id="81fb5-448">戻り値 - fontInfoPrinterIntLead</span><span class="sxs-lookup"><span data-stu-id="81fb5-448">Return Value - fontInfoPrinterIntLead</span></span>

## <a name="method-fontinfoscreen"></a><span data-ttu-id="81fb5-449">メソッド fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="81fb5-449">Method fontInfoScreen</span></span>

```xpp
public str fontInfoScreen()
```

### <a name="return-value---fontinfoscreen"></a><span data-ttu-id="81fb5-450">戻り値 - fontInfoScreen</span><span class="sxs-lookup"><span data-stu-id="81fb5-450">Return Value - fontInfoScreen</span></span>

## <a name="method-fontinfoscreenascent"></a><span data-ttu-id="81fb5-451">メソッド fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="81fb5-451">Method fontInfoScreenAscent</span></span>

```xpp
public int fontInfoScreenAscent()
```

### <a name="return-value---fontinfoscreenascent"></a><span data-ttu-id="81fb5-452">戻り値 - fontInfoScreenAscent</span><span class="sxs-lookup"><span data-stu-id="81fb5-452">Return Value - fontInfoScreenAscent</span></span>

## <a name="method-fontinfoscreendescent"></a><span data-ttu-id="81fb5-453">メソッド fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="81fb5-453">Method fontInfoScreenDescent</span></span>

```xpp
public int fontInfoScreenDescent()
```

### <a name="return-value---fontinfoscreendescent"></a><span data-ttu-id="81fb5-454">戻り値 - fontInfoScreenDescent</span><span class="sxs-lookup"><span data-stu-id="81fb5-454">Return Value - fontInfoScreenDescent</span></span>

## <a name="method-fontinfoscreenextlead"></a><span data-ttu-id="81fb5-455">メソッド fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="81fb5-455">Method fontInfoScreenExtLead</span></span>

```xpp
public int fontInfoScreenExtLead()
```

### <a name="return-value---fontinfoscreenextlead"></a><span data-ttu-id="81fb5-456">戻り値 - fontInfoScreenExtLead</span><span class="sxs-lookup"><span data-stu-id="81fb5-456">Return Value - fontInfoScreenExtLead</span></span>

## <a name="method-fontinfoscreenheight"></a><span data-ttu-id="81fb5-457">メソッド fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="81fb5-457">Method fontInfoScreenHeight</span></span>

```xpp
public int fontInfoScreenHeight()
```

### <a name="return-value---fontinfoscreenheight"></a><span data-ttu-id="81fb5-458">戻り値 - fontInfoScreenHeight</span><span class="sxs-lookup"><span data-stu-id="81fb5-458">Return Value - fontInfoScreenHeight</span></span>

## <a name="method-fontinfoscreenintlead"></a><span data-ttu-id="81fb5-459">メソッド fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="81fb5-459">Method fontInfoScreenIntLead</span></span>

```xpp
public int fontInfoScreenIntLead()
```

### <a name="return-value---fontinfoscreenintlead"></a><span data-ttu-id="81fb5-460">戻り値 - fontInfoScreenIntLead</span><span class="sxs-lookup"><span data-stu-id="81fb5-460">Return Value - fontInfoScreenIntLead</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="81fb5-461">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="81fb5-461">Method fontSize</span></span>

<span data-ttu-id="81fb5-462">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-462">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="81fb5-463">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="81fb5-463">Parameters - fontSize</span></span>

<span data-ttu-id="81fb5-464">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-464">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="81fb5-465">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="81fb5-465">Return Value - fontSize</span></span>

<span data-ttu-id="81fb5-466">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="81fb5-466">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="81fb5-467">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="81fb5-467">Method foregroundColor</span></span>

<span data-ttu-id="81fb5-468">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-468">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="81fb5-469">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="81fb5-469">Parameters - foregroundColor</span></span>

<span data-ttu-id="81fb5-470">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-470">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="81fb5-471">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="81fb5-471">Return Value - foregroundColor</span></span>

<span data-ttu-id="81fb5-472">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="81fb5-472">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="81fb5-473">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="81fb5-473">Remarks - foregroundColor</span></span>

<span data-ttu-id="81fb5-474">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="81fb5-474">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="81fb5-475">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="81fb5-475">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="81fb5-476">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="81fb5-476">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="81fb5-477">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="81fb5-477">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="81fb5-478">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="81fb5-478">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="81fb5-479">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="81fb5-479">The maximum value for a single byte is 255.</span></span>

## <a name="method-height100mm"></a><span data-ttu-id="81fb5-480">メソッド height100mm</span><span class="sxs-lookup"><span data-stu-id="81fb5-480">Method height100mm</span></span>

```xpp
public int height100mm([int heightExclBorder])
```

### <a name="parameters---height100mm"></a><span data-ttu-id="81fb5-481">パラメーター - height100mm</span><span class="sxs-lookup"><span data-stu-id="81fb5-481">Parameters - height100mm</span></span>

<span data-ttu-id="81fb5-482">heightExclBorder</span><span class="sxs-lookup"><span data-stu-id="81fb5-482">heightExclBorder</span></span>  

### <a name="return-value---height100mm"></a><span data-ttu-id="81fb5-483">戻り値 - height100mm</span><span class="sxs-lookup"><span data-stu-id="81fb5-483">Return Value - height100mm</span></span>

## <a name="method-height100mminclborder"></a><span data-ttu-id="81fb5-484">メソッド height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="81fb5-484">Method height100mmInclBorder</span></span>

```xpp
public int height100mmInclBorder([int heightInclBorder])
```

### <a name="parameters---height100mminclborder"></a><span data-ttu-id="81fb5-485">パラメーター - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="81fb5-485">Parameters - height100mmInclBorder</span></span>

<span data-ttu-id="81fb5-486">heightInclBorder</span><span class="sxs-lookup"><span data-stu-id="81fb5-486">heightInclBorder</span></span>  

### <a name="return-value---height100mminclborder"></a><span data-ttu-id="81fb5-487">戻り値 - height100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="81fb5-487">Return Value - height100mmInclBorder</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="81fb5-488">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-488">Method heightMode</span></span>

<span data-ttu-id="81fb5-489">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-489">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="81fb5-490">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-490">Parameters - heightMode</span></span>

<span data-ttu-id="81fb5-491">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-491">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="81fb5-492">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-492">Return Value - heightMode</span></span>

<span data-ttu-id="81fb5-493">計算モード。</span><span class="sxs-lookup"><span data-stu-id="81fb5-493">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="81fb5-494">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-494">Remarks - heightMode</span></span>

<span data-ttu-id="81fb5-495">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="81fb5-495">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="81fb5-496">モード。</span><span class="sxs-lookup"><span data-stu-id="81fb5-496">Mode.</span></span>          | <span data-ttu-id="81fb5-497">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="81fb5-497">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="81fb5-498">正確。</span><span class="sxs-lookup"><span data-stu-id="81fb5-498">Exact.</span></span>         | <span data-ttu-id="81fb5-499">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="81fb5-499">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="81fb5-500">自動。</span><span class="sxs-lookup"><span data-stu-id="81fb5-500">Auto.</span></span>          | <span data-ttu-id="81fb5-501">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="81fb5-501">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="81fb5-502">列の高さ</span><span class="sxs-lookup"><span data-stu-id="81fb5-502">Column height.</span></span> | <span data-ttu-id="81fb5-503">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="81fb5-503">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="81fb5-504">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="81fb5-504">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightofwordwrappedstring100mm"></a><span data-ttu-id="81fb5-505">メソッド heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="81fb5-505">Method heightOfWordWrappedString100mm</span></span>

```xpp
public int heightOfWordWrappedString100mm(str string)
```

### <a name="parameters---heightofwordwrappedstring100mm"></a><span data-ttu-id="81fb5-506">パラメーター - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="81fb5-506">Parameters - heightOfWordWrappedString100mm</span></span>

<span data-ttu-id="81fb5-507">文字列</span><span class="sxs-lookup"><span data-stu-id="81fb5-507">string</span></span>  

### <a name="return-value---heightofwordwrappedstring100mm"></a><span data-ttu-id="81fb5-508">戻り値 - heightOfWordWrappedString100mm</span><span class="sxs-lookup"><span data-stu-id="81fb5-508">Return Value - heightOfWordWrappedString100mm</span></span>

## <a name="method-heightstr"></a><span data-ttu-id="81fb5-509">メソッド heightStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-509">Method heightStr</span></span>

```xpp
public str heightStr([str value])
```

### <a name="parameters---heightstr"></a><span data-ttu-id="81fb5-510">パラメーター - heightStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-510">Parameters - heightStr</span></span>

<span data-ttu-id="81fb5-511">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-511">value</span></span>  

### <a name="return-value---heightstr"></a><span data-ttu-id="81fb5-512">戻り値 - heightStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-512">Return Value - heightStr</span></span>

## <a name="method-heightunit"></a><span data-ttu-id="81fb5-513">メソッド heightUnit</span><span class="sxs-lookup"><span data-stu-id="81fb5-513">Method heightUnit</span></span>

```xpp
public Units heightUnit([Units value])
```

### <a name="parameters---heightunit"></a><span data-ttu-id="81fb5-514">パラメーター - heightUnit</span><span class="sxs-lookup"><span data-stu-id="81fb5-514">Parameters - heightUnit</span></span>

<span data-ttu-id="81fb5-515">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-515">value</span></span>  

### <a name="return-value---heightunit"></a><span data-ttu-id="81fb5-516">戻り値 - heightUnit</span><span class="sxs-lookup"><span data-stu-id="81fb5-516">Return Value - heightUnit</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="81fb5-517">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-517">Method heightValue</span></span>

<span data-ttu-id="81fb5-518">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-518">Gets or sets the height of the control.</span></span>

```xpp
public Real heightValue([Real value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="81fb5-519">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-519">Parameters - heightValue</span></span>

<span data-ttu-id="81fb5-520">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-520">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="81fb5-521">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-521">Return Value - heightValue</span></span>

<span data-ttu-id="81fb5-522">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="81fb5-522">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="81fb5-523">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-523">Remarks - heightValue</span></span>

<span data-ttu-id="81fb5-524">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="81fb5-524">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-italic"></a><span data-ttu-id="81fb5-525">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="81fb5-525">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="81fb5-526">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="81fb5-526">Parameters - italic</span></span>

<span data-ttu-id="81fb5-527">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-527">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="81fb5-528">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="81fb5-528">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="81fb5-529">メソッド label</span><span class="sxs-lookup"><span data-stu-id="81fb5-529">Method label</span></span>

<span data-ttu-id="81fb5-530">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-530">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="81fb5-531">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="81fb5-531">Parameters - label</span></span>

<span data-ttu-id="81fb5-532">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-532">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="81fb5-533">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="81fb5-533">Return Value - label</span></span>

<span data-ttu-id="81fb5-534">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="81fb5-534">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="81fb5-535">備考 - label</span><span class="sxs-lookup"><span data-stu-id="81fb5-535">Remarks - label</span></span>

<span data-ttu-id="81fb5-536">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-536">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="81fb5-537">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="81fb5-537">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelcssclass"></a><span data-ttu-id="81fb5-538">メソッド labelCssClass</span><span class="sxs-lookup"><span data-stu-id="81fb5-538">Method labelCssClass</span></span>

```xpp
public str labelCssClass([str value])
```

### <a name="parameters---labelcssclass"></a><span data-ttu-id="81fb5-539">パラメーター - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="81fb5-539">Parameters - labelCssClass</span></span>

<span data-ttu-id="81fb5-540">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-540">value</span></span>  

### <a name="return-value---labelcssclass"></a><span data-ttu-id="81fb5-541">戻り値 - labelCssClass</span><span class="sxs-lookup"><span data-stu-id="81fb5-541">Return Value - labelCssClass</span></span>

## <a name="method-labellinebelow"></a><span data-ttu-id="81fb5-542">メソッド labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="81fb5-542">Method labelLineBelow</span></span>

```xpp
public LineType labelLineBelow([LineType value])
```

### <a name="parameters---labellinebelow"></a><span data-ttu-id="81fb5-543">パラメーター - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="81fb5-543">Parameters - labelLineBelow</span></span>

<span data-ttu-id="81fb5-544">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-544">value</span></span>  

### <a name="return-value---labellinebelow"></a><span data-ttu-id="81fb5-545">戻り値 - labelLineBelow</span><span class="sxs-lookup"><span data-stu-id="81fb5-545">Return Value - labelLineBelow</span></span>

## <a name="method-labellinethickness"></a><span data-ttu-id="81fb5-546">メソッド labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="81fb5-546">Method labelLineThickness</span></span>

```xpp
public LineThickness labelLineThickness([LineThickness value])
```

### <a name="parameters---labellinethickness"></a><span data-ttu-id="81fb5-547">パラメーター - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="81fb5-547">Parameters - labelLineThickness</span></span>

<span data-ttu-id="81fb5-548">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-548">value</span></span>  

### <a name="return-value---labellinethickness"></a><span data-ttu-id="81fb5-549">戻り値 - labelLineThickness</span><span class="sxs-lookup"><span data-stu-id="81fb5-549">Return Value - labelLineThickness</span></span>

## <a name="method-left100mm"></a><span data-ttu-id="81fb5-550">メソッド left100mm</span><span class="sxs-lookup"><span data-stu-id="81fb5-550">Method left100mm</span></span>

```xpp
public int left100mm([int leftExclBorder])
```

### <a name="parameters---left100mm"></a><span data-ttu-id="81fb5-551">パラメーター - left100mm</span><span class="sxs-lookup"><span data-stu-id="81fb5-551">Parameters - left100mm</span></span>

<span data-ttu-id="81fb5-552">leftExclBorder</span><span class="sxs-lookup"><span data-stu-id="81fb5-552">leftExclBorder</span></span>  

### <a name="return-value---left100mm"></a><span data-ttu-id="81fb5-553">戻り値 - left100mm</span><span class="sxs-lookup"><span data-stu-id="81fb5-553">Return Value - left100mm</span></span>

## <a name="method-left100mminclborder"></a><span data-ttu-id="81fb5-554">メソッド left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="81fb5-554">Method left100mmInclBorder</span></span>

```xpp
public int left100mmInclBorder([int leftInclBorder])
```

### <a name="parameters---left100mminclborder"></a><span data-ttu-id="81fb5-555">パラメーター - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="81fb5-555">Parameters - left100mmInclBorder</span></span>

<span data-ttu-id="81fb5-556">leftInclBorder</span><span class="sxs-lookup"><span data-stu-id="81fb5-556">leftInclBorder</span></span>  

### <a name="return-value---left100mminclborder"></a><span data-ttu-id="81fb5-557">戻り値 - left100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="81fb5-557">Return Value - left100mmInclBorder</span></span>

## <a name="method-leftmarginanframe"></a><span data-ttu-id="81fb5-558">メソッド leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="81fb5-558">Method leftMarginAnFrame</span></span>

```xpp
public int leftMarginAnFrame()
```

### <a name="return-value---leftmarginanframe"></a><span data-ttu-id="81fb5-559">戻り値 - leftMarginAnFrame</span><span class="sxs-lookup"><span data-stu-id="81fb5-559">Return Value - leftMarginAnFrame</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="81fb5-560">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-560">Method leftMarginMode</span></span>

```xpp
public int leftMarginMode([int value])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="81fb5-561">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-561">Parameters - leftMarginMode</span></span>

<span data-ttu-id="81fb5-562">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-562">value</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="81fb5-563">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-563">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginstr"></a><span data-ttu-id="81fb5-564">メソッド leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-564">Method leftMarginStr</span></span>

```xpp
public str leftMarginStr([str value])
```

### <a name="parameters---leftmarginstr"></a><span data-ttu-id="81fb5-565">パラメーター - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-565">Parameters - leftMarginStr</span></span>

<span data-ttu-id="81fb5-566">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-566">value</span></span>  

### <a name="return-value---leftmarginstr"></a><span data-ttu-id="81fb5-567">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-567">Return Value - leftMarginStr</span></span>

## <a name="method-leftmarginunit"></a><span data-ttu-id="81fb5-568">メソッド leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="81fb5-568">Method leftMarginUnit</span></span>

```xpp
public Units leftMarginUnit([Units value])
```

### <a name="parameters---leftmarginunit"></a><span data-ttu-id="81fb5-569">パラメーター - leftMarginUnit</span><span class="sxs-lookup"><span data-stu-id="81fb5-569">Parameters - leftMarginUnit</span></span>

<span data-ttu-id="81fb5-570">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-570">value</span></span>  

### <a name="return-value---leftmarginunit"></a><span data-ttu-id="81fb5-571">戻り値 - leftMarginStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-571">Return Value - leftMarginUnit</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="81fb5-572">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-572">Method leftMarginValue</span></span>

```xpp
public Real leftMarginValue([Real value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="81fb5-573">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-573">Parameters - leftMarginValue</span></span>

<span data-ttu-id="81fb5-574">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-574">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="81fb5-575">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-575">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="81fb5-576">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-576">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="81fb5-577">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-577">Parameters - leftMode</span></span>

<span data-ttu-id="81fb5-578">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-578">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="81fb5-579">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-579">Return Value - leftMode</span></span>

## <a name="method-leftstr"></a><span data-ttu-id="81fb5-580">メソッド leftStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-580">Method leftStr</span></span>

```xpp
public str leftStr([str value])
```

### <a name="parameters---leftstr"></a><span data-ttu-id="81fb5-581">パラメーター - leftStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-581">Parameters - leftStr</span></span>

<span data-ttu-id="81fb5-582">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-582">value</span></span>  

### <a name="return-value---leftstr"></a><span data-ttu-id="81fb5-583">戻り値 - leftStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-583">Return Value - leftStr</span></span>

## <a name="method-leftunit"></a><span data-ttu-id="81fb5-584">メソッド leftUnit</span><span class="sxs-lookup"><span data-stu-id="81fb5-584">Method leftUnit</span></span>

```xpp
public Units leftUnit([Units value])
```

### <a name="parameters---leftunit"></a><span data-ttu-id="81fb5-585">パラメーター - leftUnit</span><span class="sxs-lookup"><span data-stu-id="81fb5-585">Parameters - leftUnit</span></span>

<span data-ttu-id="81fb5-586">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-586">value</span></span>  

### <a name="return-value---leftunit"></a><span data-ttu-id="81fb5-587">戻り値 - leftUnit</span><span class="sxs-lookup"><span data-stu-id="81fb5-587">Return Value - leftUnit</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="81fb5-588">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-588">Method leftValue</span></span>

```xpp
public Real leftValue([Real value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="81fb5-589">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-589">Parameters - leftValue</span></span>

<span data-ttu-id="81fb5-590">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-590">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="81fb5-591">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-591">Return Value - leftValue</span></span>

## <a name="method-lineabove"></a><span data-ttu-id="81fb5-592">メソッド lineAbove</span><span class="sxs-lookup"><span data-stu-id="81fb5-592">Method lineAbove</span></span>

```xpp
public LineType lineAbove([LineType value])
```

### <a name="parameters---lineabove"></a><span data-ttu-id="81fb5-593">パラメーター - lineAbove</span><span class="sxs-lookup"><span data-stu-id="81fb5-593">Parameters - lineAbove</span></span>

<span data-ttu-id="81fb5-594">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-594">value</span></span>  

### <a name="return-value---lineabove"></a><span data-ttu-id="81fb5-595">戻り値 - lineAbove</span><span class="sxs-lookup"><span data-stu-id="81fb5-595">Return Value - lineAbove</span></span>

## <a name="method-linebelow"></a><span data-ttu-id="81fb5-596">メソッド lineBelow</span><span class="sxs-lookup"><span data-stu-id="81fb5-596">Method lineBelow</span></span>

```xpp
public LineType lineBelow([LineType value])
```

### <a name="parameters---linebelow"></a><span data-ttu-id="81fb5-597">パラメーター - lineBelow</span><span class="sxs-lookup"><span data-stu-id="81fb5-597">Parameters - lineBelow</span></span>

<span data-ttu-id="81fb5-598">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-598">value</span></span>  

### <a name="return-value---linebelow"></a><span data-ttu-id="81fb5-599">戻り値 - lineBelow</span><span class="sxs-lookup"><span data-stu-id="81fb5-599">Return Value - lineBelow</span></span>

## <a name="method-lineleft"></a><span data-ttu-id="81fb5-600">メソッド lineLeft</span><span class="sxs-lookup"><span data-stu-id="81fb5-600">Method lineLeft</span></span>

<span data-ttu-id="81fb5-601">セクションの左枠として使用される明細行のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-601">Gets or sets the type of line that is used as the left border of a section.</span></span>

```xpp
public LineType lineLeft([LineType value])
```

### <a name="parameters---lineleft"></a><span data-ttu-id="81fb5-602">パラメーター - lineLeft</span><span class="sxs-lookup"><span data-stu-id="81fb5-602">Parameters - lineLeft</span></span>

<span data-ttu-id="81fb5-603">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-603">value</span></span>  

### <a name="return-value---lineleft"></a><span data-ttu-id="81fb5-604">戻り値 - lineLeft</span><span class="sxs-lookup"><span data-stu-id="81fb5-604">Return Value - lineLeft</span></span>

<span data-ttu-id="81fb5-605">左境界線として使用される線のタイプ。</span><span class="sxs-lookup"><span data-stu-id="81fb5-605">The type of line that is used as the left border.</span></span>

## <a name="method-lineright"></a><span data-ttu-id="81fb5-606">メソッド lineRight</span><span class="sxs-lookup"><span data-stu-id="81fb5-606">Method lineRight</span></span>

```xpp
public LineType lineRight([LineType value])
```

### <a name="parameters---lineright"></a><span data-ttu-id="81fb5-607">パラメーター - lineRight</span><span class="sxs-lookup"><span data-stu-id="81fb5-607">Parameters - lineRight</span></span>

<span data-ttu-id="81fb5-608">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-608">value</span></span>  

### <a name="return-value---lineright"></a><span data-ttu-id="81fb5-609">戻り値 - lineRight</span><span class="sxs-lookup"><span data-stu-id="81fb5-609">Return Value - lineRight</span></span>

## <a name="method-menuitemlabel"></a><span data-ttu-id="81fb5-610">メソッド menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="81fb5-610">Method menuItemLabel</span></span>

```xpp
public str menuItemLabel([str value])
```

### <a name="parameters---menuitemlabel"></a><span data-ttu-id="81fb5-611">パラメーター - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="81fb5-611">Parameters - menuItemLabel</span></span>

<span data-ttu-id="81fb5-612">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-612">value</span></span>  

### <a name="return-value---menuitemlabel"></a><span data-ttu-id="81fb5-613">戻り値 - menuItemLabel</span><span class="sxs-lookup"><span data-stu-id="81fb5-613">Return Value - menuItemLabel</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="81fb5-614">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="81fb5-614">Method menuItemName</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="81fb5-615">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="81fb5-615">Parameters - menuItemName</span></span>

<span data-ttu-id="81fb5-616">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-616">value</span></span>  

### <a name="return-value---menuitemname"></a><span data-ttu-id="81fb5-617">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="81fb5-617">Return Value - menuItemName</span></span>

## <a name="method-menuitemtype"></a><span data-ttu-id="81fb5-618">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="81fb5-618">Method menuItemType</span></span>

```xpp
public MenuItemType menuItemType([MenuItemType value])
```

### <a name="parameters---menuitemtype"></a><span data-ttu-id="81fb5-619">パラメーター - menuItemType</span><span class="sxs-lookup"><span data-stu-id="81fb5-619">Parameters - menuItemType</span></span>

<span data-ttu-id="81fb5-620">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-620">value</span></span>  

### <a name="return-value---menuitemtype"></a><span data-ttu-id="81fb5-621">戻り値 - menuItemType</span><span class="sxs-lookup"><span data-stu-id="81fb5-621">Return Value - menuItemType</span></span>

## <a name="method-modelfieldname"></a><span data-ttu-id="81fb5-622">メソッド modelFieldName</span><span class="sxs-lookup"><span data-stu-id="81fb5-622">Method modelFieldName</span></span>

```xpp
public str modelFieldName([str value])
```

### <a name="parameters---modelfieldname"></a><span data-ttu-id="81fb5-623">パラメーター - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="81fb5-623">Parameters - modelFieldName</span></span>

<span data-ttu-id="81fb5-624">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-624">value</span></span>  

### <a name="return-value---modelfieldname"></a><span data-ttu-id="81fb5-625">戻り値 - modelFieldName</span><span class="sxs-lookup"><span data-stu-id="81fb5-625">Return Value - modelFieldName</span></span>

## <a name="method-name"></a><span data-ttu-id="81fb5-626">メソッド名</span><span class="sxs-lookup"><span data-stu-id="81fb5-626">Method name</span></span>

<span data-ttu-id="81fb5-627">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-627">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="81fb5-628">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="81fb5-628">Parameters - name</span></span>

<span data-ttu-id="81fb5-629">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-629">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="81fb5-630">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="81fb5-630">Return Value - name</span></span>

<span data-ttu-id="81fb5-631">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="81fb5-631">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="81fb5-632">備考 - name</span><span class="sxs-lookup"><span data-stu-id="81fb5-632">Remarks - name</span></span>

<span data-ttu-id="81fb5-633">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="81fb5-633">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="81fb5-634">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="81fb5-634">Begins with a letter.</span></span>
-   <span data-ttu-id="81fb5-635">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="81fb5-635">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="81fb5-636">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="81fb5-636">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="81fb5-637">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="81fb5-637">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="81fb5-638">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="81fb5-638">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-numberoflines"></a><span data-ttu-id="81fb5-639">メソッド numberOfLines</span><span class="sxs-lookup"><span data-stu-id="81fb5-639">Method numberOfLines</span></span>

```xpp
public int numberOfLines(int height100mm)
```

### <a name="parameters---numberoflines"></a><span data-ttu-id="81fb5-640">パラメーター - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="81fb5-640">Parameters - numberOfLines</span></span>

<span data-ttu-id="81fb5-641">height100mm</span><span class="sxs-lookup"><span data-stu-id="81fb5-641">height100mm</span></span>  

### <a name="return-value---numberoflines"></a><span data-ttu-id="81fb5-642">戻り値 - numberOfLines</span><span class="sxs-lookup"><span data-stu-id="81fb5-642">Return Value - numberOfLines</span></span>

## <a name="method-position"></a><span data-ttu-id="81fb5-643">メソッドの位置</span><span class="sxs-lookup"><span data-stu-id="81fb5-643">Method position</span></span>

```xpp
public int position([int value])
```

### <a name="parameters---position"></a><span data-ttu-id="81fb5-644">パラメーター - position</span><span class="sxs-lookup"><span data-stu-id="81fb5-644">Parameters - position</span></span>

<span data-ttu-id="81fb5-645">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-645">value</span></span>  

### <a name="return-value---position"></a><span data-ttu-id="81fb5-646">戻り値 - position</span><span class="sxs-lookup"><span data-stu-id="81fb5-646">Return Value - position</span></span>

## <a name="method-previewinfo"></a><span data-ttu-id="81fb5-647">メソッド previewInfo</span><span class="sxs-lookup"><span data-stu-id="81fb5-647">Method previewInfo</span></span>

```xpp
public str previewInfo(str string)
```

### <a name="parameters---previewinfo"></a><span data-ttu-id="81fb5-648">パラメーター - previewInfo</span><span class="sxs-lookup"><span data-stu-id="81fb5-648">Parameters - previewInfo</span></span>

<span data-ttu-id="81fb5-649">文字列</span><span class="sxs-lookup"><span data-stu-id="81fb5-649">string</span></span>  

### <a name="return-value---previewinfo"></a><span data-ttu-id="81fb5-650">戻り値 - previewInfo</span><span class="sxs-lookup"><span data-stu-id="81fb5-650">Return Value - previewInfo</span></span>

## <a name="method-previewxcompensation100mm"></a><span data-ttu-id="81fb5-651">メソッド previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="81fb5-651">Method previewXCompensation100mm</span></span>

```xpp
public int previewXCompensation100mm(str string)
```

### <a name="parameters---previewxcompensation100mm"></a><span data-ttu-id="81fb5-652">パラメーター - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="81fb5-652">Parameters - previewXCompensation100mm</span></span>

<span data-ttu-id="81fb5-653">文字列</span><span class="sxs-lookup"><span data-stu-id="81fb5-653">string</span></span>  

### <a name="return-value---previewxcompensation100mm"></a><span data-ttu-id="81fb5-654">戻り値 - previewXCompensation100mm</span><span class="sxs-lookup"><span data-stu-id="81fb5-654">Return Value - previewXCompensation100mm</span></span>

## <a name="method-right100mm"></a><span data-ttu-id="81fb5-655">メソッド right100mm</span><span class="sxs-lookup"><span data-stu-id="81fb5-655">Method right100mm</span></span>

```xpp
public int right100mm()
```

### <a name="return-value---right100mm"></a><span data-ttu-id="81fb5-656">戻り値 - right100mm</span><span class="sxs-lookup"><span data-stu-id="81fb5-656">Return Value - right100mm</span></span>

## <a name="method-right100mminclborder"></a><span data-ttu-id="81fb5-657">メソッド right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="81fb5-657">Method right100mmInclBorder</span></span>

```xpp
public int right100mmInclBorder()
```

### <a name="return-value---right100mminclborder"></a><span data-ttu-id="81fb5-658">戻り値 - right100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="81fb5-658">Return Value - right100mmInclBorder</span></span>

## <a name="method-rightmarginandframe"></a><span data-ttu-id="81fb5-659">メソッド rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="81fb5-659">Method rightMarginAndFrame</span></span>

```xpp
public int rightMarginAndFrame()
```

### <a name="return-value---rightmarginandframe"></a><span data-ttu-id="81fb5-660">戻り値 - rightMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="81fb5-660">Return Value - rightMarginAndFrame</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="81fb5-661">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-661">Method rightMarginMode</span></span>

```xpp
public int rightMarginMode([int value])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="81fb5-662">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-662">Parameters - rightMarginMode</span></span>

<span data-ttu-id="81fb5-663">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-663">value</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="81fb5-664">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-664">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginstr"></a><span data-ttu-id="81fb5-665">メソッド rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-665">Method rightMarginStr</span></span>

```xpp
public str rightMarginStr([str value])
```

### <a name="parameters---rightmarginstr"></a><span data-ttu-id="81fb5-666">パラメーター - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-666">Parameters - rightMarginStr</span></span>

<span data-ttu-id="81fb5-667">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-667">value</span></span>  

### <a name="return-value---rightmarginstr"></a><span data-ttu-id="81fb5-668">戻り値 - rightMarginStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-668">Return Value - rightMarginStr</span></span>

## <a name="method-rightmarginunit"></a><span data-ttu-id="81fb5-669">メソッド rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="81fb5-669">Method rightMarginUnit</span></span>

```xpp
public Units rightMarginUnit([Units value])
```

### <a name="parameters---rightmarginunit"></a><span data-ttu-id="81fb5-670">パラメーター - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="81fb5-670">Parameters - rightMarginUnit</span></span>

<span data-ttu-id="81fb5-671">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-671">value</span></span>  

### <a name="return-value---rightmarginunit"></a><span data-ttu-id="81fb5-672">戻り値 - rightMarginUnit</span><span class="sxs-lookup"><span data-stu-id="81fb5-672">Return Value - rightMarginUnit</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="81fb5-673">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-673">Method rightMarginValue</span></span>

```xpp
public Real rightMarginValue([Real value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="81fb5-674">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-674">Parameters - rightMarginValue</span></span>

<span data-ttu-id="81fb5-675">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-675">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="81fb5-676">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-676">Return Value - rightMarginValue</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="81fb5-677">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="81fb5-677">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="81fb5-678">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="81fb5-678">Parameters - securityKey</span></span>

<span data-ttu-id="81fb5-679">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-679">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="81fb5-680">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="81fb5-680">Return Value - securityKey</span></span>

## <a name="method-setheightgettext"></a><span data-ttu-id="81fb5-681">メソッド setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="81fb5-681">Method setHeightGetText</span></span>

```xpp
public str setHeightGetText(int lines, str string)
```

### <a name="parameters---setheightgettext"></a><span data-ttu-id="81fb5-682">パラメーター - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="81fb5-682">Parameters - setHeightGetText</span></span>

<span data-ttu-id="81fb5-683">明細行</span><span class="sxs-lookup"><span data-stu-id="81fb5-683">lines</span></span>  

<!-- -->

<span data-ttu-id="81fb5-684">文字列</span><span class="sxs-lookup"><span data-stu-id="81fb5-684">string</span></span>  

### <a name="return-value---setheightgettext"></a><span data-ttu-id="81fb5-685">戻り値 - setHeightGetText</span><span class="sxs-lookup"><span data-stu-id="81fb5-685">Return Value - setHeightGetText</span></span>

## <a name="method-table"></a><span data-ttu-id="81fb5-686">メソッド table</span><span class="sxs-lookup"><span data-stu-id="81fb5-686">Method table</span></span>

<span data-ttu-id="81fb5-687">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-687">Gets or sets the table ID associated with the object.</span></span>

```xpp
public TableId table([TableId value])
```

### <a name="parameters---table"></a><span data-ttu-id="81fb5-688">パラメーター - table</span><span class="sxs-lookup"><span data-stu-id="81fb5-688">Parameters - table</span></span>

<span data-ttu-id="81fb5-689">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-689">value</span></span>  

### <a name="return-value---table"></a><span data-ttu-id="81fb5-690">戻り値 - toBlob</span><span class="sxs-lookup"><span data-stu-id="81fb5-690">Return Value - table</span></span>

<span data-ttu-id="81fb5-691">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="81fb5-691">The current value of the table ID associated with the object.</span></span>

## <a name="method-thickness"></a><span data-ttu-id="81fb5-692">メソッド thickness</span><span class="sxs-lookup"><span data-stu-id="81fb5-692">Method thickness</span></span>

```xpp
public LineThickness thickness([LineThickness value])
```

### <a name="parameters---thickness"></a><span data-ttu-id="81fb5-693">パラメーター - thickness</span><span class="sxs-lookup"><span data-stu-id="81fb5-693">Parameters - thickness</span></span>

<span data-ttu-id="81fb5-694">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-694">value</span></span>  

### <a name="return-value---thickness"></a><span data-ttu-id="81fb5-695">戻り値 - thickness</span><span class="sxs-lookup"><span data-stu-id="81fb5-695">Return Value - thickness</span></span>

## <a name="method-top100mm"></a><span data-ttu-id="81fb5-696">メソッド top100mm</span><span class="sxs-lookup"><span data-stu-id="81fb5-696">Method top100mm</span></span>

```xpp
public int top100mm([int topExclBorder])
```

### <a name="parameters---top100mm"></a><span data-ttu-id="81fb5-697">パラメーター - top100mm</span><span class="sxs-lookup"><span data-stu-id="81fb5-697">Parameters - top100mm</span></span>

<span data-ttu-id="81fb5-698">topExclBorder</span><span class="sxs-lookup"><span data-stu-id="81fb5-698">topExclBorder</span></span>  

### <a name="return-value---top100mm"></a><span data-ttu-id="81fb5-699">戻り値 - top100mm</span><span class="sxs-lookup"><span data-stu-id="81fb5-699">Return Value - top100mm</span></span>

## <a name="method-top100mminclborder"></a><span data-ttu-id="81fb5-700">メソッド top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="81fb5-700">Method top100mmInclBorder</span></span>

```xpp
public int top100mmInclBorder([int topInclBorder])
```

### <a name="parameters---top100mminclborder"></a><span data-ttu-id="81fb5-701">パラメーター - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="81fb5-701">Parameters - top100mmInclBorder</span></span>

<span data-ttu-id="81fb5-702">topInclBorder</span><span class="sxs-lookup"><span data-stu-id="81fb5-702">topInclBorder</span></span>  

### <a name="return-value---top100mminclborder"></a><span data-ttu-id="81fb5-703">戻り値 - top100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="81fb5-703">Return Value - top100mmInclBorder</span></span>

## <a name="method-topmarginandframe"></a><span data-ttu-id="81fb5-704">メソッド topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="81fb5-704">Method topMarginAndFrame</span></span>

```xpp
public int topMarginAndFrame()
```

### <a name="return-value---topmarginandframe"></a><span data-ttu-id="81fb5-705">戻り値 - topMarginAndFrame</span><span class="sxs-lookup"><span data-stu-id="81fb5-705">Return Value - topMarginAndFrame</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="81fb5-706">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-706">Method topMarginMode</span></span>

```xpp
public int topMarginMode([int value])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="81fb5-707">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-707">Parameters - topMarginMode</span></span>

<span data-ttu-id="81fb5-708">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-708">value</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="81fb5-709">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-709">Return Value - topMarginMode</span></span>

## <a name="method-topmarginstr"></a><span data-ttu-id="81fb5-710">メソッド topMarginStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-710">Method topMarginStr</span></span>

```xpp
public str topMarginStr([str value])
```

### <a name="parameters---topmarginstr"></a><span data-ttu-id="81fb5-711">パラメーター - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-711">Parameters - topMarginStr</span></span>

<span data-ttu-id="81fb5-712">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-712">value</span></span>  

### <a name="return-value---topmarginstr"></a><span data-ttu-id="81fb5-713">戻り値 - topMarginStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-713">Return Value - topMarginStr</span></span>

## <a name="method-topmarginunit"></a><span data-ttu-id="81fb5-714">メソッド topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="81fb5-714">Method topMarginUnit</span></span>

```xpp
public Units topMarginUnit([Units value])
```

### <a name="parameters---topmarginunit"></a><span data-ttu-id="81fb5-715">パラメーター - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="81fb5-715">Parameters - topMarginUnit</span></span>

<span data-ttu-id="81fb5-716">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-716">value</span></span>  

### <a name="return-value---topmarginunit"></a><span data-ttu-id="81fb5-717">戻り値 - topMarginUnit</span><span class="sxs-lookup"><span data-stu-id="81fb5-717">Return Value - topMarginUnit</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="81fb5-718">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-718">Method topMarginValue</span></span>

```xpp
public Real topMarginValue([Real value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="81fb5-719">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-719">Parameters - topMarginValue</span></span>

<span data-ttu-id="81fb5-720">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-720">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="81fb5-721">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-721">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="81fb5-722">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-722">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="81fb5-723">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-723">Parameters - topMode</span></span>

<span data-ttu-id="81fb5-724">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-724">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="81fb5-725">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-725">Return Value - topMode</span></span>

## <a name="method-topstr"></a><span data-ttu-id="81fb5-726">メソッド topStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-726">Method topStr</span></span>

```xpp
public str topStr([str value])
```

### <a name="parameters---topstr"></a><span data-ttu-id="81fb5-727">パラメーター - topStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-727">Parameters - topStr</span></span>

<span data-ttu-id="81fb5-728">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-728">value</span></span>  

### <a name="return-value---topstr"></a><span data-ttu-id="81fb5-729">戻り値 - topStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-729">Return Value - topStr</span></span>

## <a name="method-topunit"></a><span data-ttu-id="81fb5-730">メソッド topUnit</span><span class="sxs-lookup"><span data-stu-id="81fb5-730">Method topUnit</span></span>

```xpp
public Units topUnit([Units value])
```

### <a name="parameters---topunit"></a><span data-ttu-id="81fb5-731">パラメーター - topUnit</span><span class="sxs-lookup"><span data-stu-id="81fb5-731">Parameters - topUnit</span></span>

<span data-ttu-id="81fb5-732">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-732">value</span></span>  

### <a name="return-value---topunit"></a><span data-ttu-id="81fb5-733">戻り値 - topUnit</span><span class="sxs-lookup"><span data-stu-id="81fb5-733">Return Value - topUnit</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="81fb5-734">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-734">Method topValue</span></span>

```xpp
public Real topValue([Real value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="81fb5-735">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-735">Parameters - topValue</span></span>

<span data-ttu-id="81fb5-736">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-736">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="81fb5-737">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-737">Return Value - topValue</span></span>

## <a name="method-typeheaderprompt"></a><span data-ttu-id="81fb5-738">メソッド typeHeaderPrompt</span><span class="sxs-lookup"><span data-stu-id="81fb5-738">Method typeHeaderPrompt</span></span>

```xpp
public int typeHeaderPrompt([int value])
```

### <a name="parameters---typeheaderprompt"></a><span data-ttu-id="81fb5-739">パラメーター - typeHeaderPrompt</span><span class="sxs-lookup"><span data-stu-id="81fb5-739">Parameters - typeHeaderPrompt</span></span>

<span data-ttu-id="81fb5-740">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-740">value</span></span>  

### <a name="return-value---typeheaderprompt"></a><span data-ttu-id="81fb5-741">戻り値 - typeHeaderPrompt</span><span class="sxs-lookup"><span data-stu-id="81fb5-741">Return Value - typeHeaderPrompt</span></span>

## <a name="method-underline"></a><span data-ttu-id="81fb5-742">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="81fb5-742">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="81fb5-743">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="81fb5-743">Parameters - underline</span></span>

<span data-ttu-id="81fb5-744">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-744">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="81fb5-745">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="81fb5-745">Return Value - underline</span></span>

## <a name="method-visible"></a><span data-ttu-id="81fb5-746">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="81fb5-746">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="81fb5-747">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="81fb5-747">Parameters - visible</span></span>

<span data-ttu-id="81fb5-748">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-748">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="81fb5-749">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="81fb5-749">Return Value - visible</span></span>

## <a name="method-webmenuitemname"></a><span data-ttu-id="81fb5-750">メソッド webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="81fb5-750">Method webMenuItemName</span></span>

```xpp
public str webMenuItemName([str value])
```

### <a name="parameters---webmenuitemname"></a><span data-ttu-id="81fb5-751">パラメーター - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="81fb5-751">Parameters - webMenuItemName</span></span>

<span data-ttu-id="81fb5-752">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-752">value</span></span>  

### <a name="return-value---webmenuitemname"></a><span data-ttu-id="81fb5-753">戻り値 - webMenuItemName</span><span class="sxs-lookup"><span data-stu-id="81fb5-753">Return Value - webMenuItemName</span></span>

## <a name="method-webmenuitemtype"></a><span data-ttu-id="81fb5-754">メソッド webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="81fb5-754">Method webMenuItemType</span></span>

```xpp
public WebMenuItemType webMenuItemType([WebMenuItemType value])
```

### <a name="parameters---webmenuitemtype"></a><span data-ttu-id="81fb5-755">パラメーター - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="81fb5-755">Parameters - webMenuItemType</span></span>

<span data-ttu-id="81fb5-756">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-756">value</span></span>  

### <a name="return-value---webmenuitemtype"></a><span data-ttu-id="81fb5-757">戻り値 - webMenuItemType</span><span class="sxs-lookup"><span data-stu-id="81fb5-757">Return Value - webMenuItemType</span></span>

## <a name="method-webtarget"></a><span data-ttu-id="81fb5-758">メソッド webTarget</span><span class="sxs-lookup"><span data-stu-id="81fb5-758">Method webTarget</span></span>

```xpp
public str webTarget([str value])
```

### <a name="parameters---webtarget"></a><span data-ttu-id="81fb5-759">パラメーター - webTarget</span><span class="sxs-lookup"><span data-stu-id="81fb5-759">Parameters - webTarget</span></span>

<span data-ttu-id="81fb5-760">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-760">value</span></span>  

### <a name="return-value---webtarget"></a><span data-ttu-id="81fb5-761">戻り値 - webTarget</span><span class="sxs-lookup"><span data-stu-id="81fb5-761">Return Value - webTarget</span></span>

## <a name="method-width100mm"></a><span data-ttu-id="81fb5-762">メソッド width100mm</span><span class="sxs-lookup"><span data-stu-id="81fb5-762">Method width100mm</span></span>

```xpp
public int width100mm([int widthExclBorder])
```

### <a name="parameters---width100mm"></a><span data-ttu-id="81fb5-763">パラメーター - width100mm</span><span class="sxs-lookup"><span data-stu-id="81fb5-763">Parameters - width100mm</span></span>

<span data-ttu-id="81fb5-764">widthExclBorder</span><span class="sxs-lookup"><span data-stu-id="81fb5-764">widthExclBorder</span></span>  

### <a name="return-value---width100mm"></a><span data-ttu-id="81fb5-765">戻り値 - width100mm</span><span class="sxs-lookup"><span data-stu-id="81fb5-765">Return Value - width100mm</span></span>

## <a name="method-width100mminclborder"></a><span data-ttu-id="81fb5-766">メソッド width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="81fb5-766">Method width100mmInclBorder</span></span>

```xpp
public int width100mmInclBorder([int widthInclBorder])
```

### <a name="parameters---width100mminclborder"></a><span data-ttu-id="81fb5-767">パラメーター - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="81fb5-767">Parameters - width100mmInclBorder</span></span>

<span data-ttu-id="81fb5-768">widthInclBorder</span><span class="sxs-lookup"><span data-stu-id="81fb5-768">widthInclBorder</span></span>  

### <a name="return-value---width100mminclborder"></a><span data-ttu-id="81fb5-769">戻り値 - width100mmInclBorder</span><span class="sxs-lookup"><span data-stu-id="81fb5-769">Return Value - width100mmInclBorder</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="81fb5-770">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-770">Method widthMode</span></span>

<span data-ttu-id="81fb5-771">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-771">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="81fb5-772">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-772">Parameters - widthMode</span></span>

<span data-ttu-id="81fb5-773">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-773">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="81fb5-774">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-774">Return Value - widthMode</span></span>

<span data-ttu-id="81fb5-775">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="81fb5-775">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="81fb5-776">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="81fb5-776">Remarks - widthMode</span></span>

<span data-ttu-id="81fb5-777">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="81fb5-777">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="81fb5-778">モード。</span><span class="sxs-lookup"><span data-stu-id="81fb5-778">Mode.</span></span>         | <span data-ttu-id="81fb5-779">幅計算。</span><span class="sxs-lookup"><span data-stu-id="81fb5-779">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="81fb5-780">正確。</span><span class="sxs-lookup"><span data-stu-id="81fb5-780">Exact.</span></span>        | <span data-ttu-id="81fb5-781">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="81fb5-781">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="81fb5-782">自動。</span><span class="sxs-lookup"><span data-stu-id="81fb5-782">Auto.</span></span>         | <span data-ttu-id="81fb5-783">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="81fb5-783">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="81fb5-784">列の幅。</span><span class="sxs-lookup"><span data-stu-id="81fb5-784">Column width.</span></span> | <span data-ttu-id="81fb5-785">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="81fb5-785">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="81fb5-786">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="81fb5-786">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthofstring100mm"></a><span data-ttu-id="81fb5-787">メソッド widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="81fb5-787">Method widthOfString100mm</span></span>

```xpp
public int widthOfString100mm(str string)
```

### <a name="parameters---widthofstring100mm"></a><span data-ttu-id="81fb5-788">パラメーター - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="81fb5-788">Parameters - widthOfString100mm</span></span>

<span data-ttu-id="81fb5-789">文字列</span><span class="sxs-lookup"><span data-stu-id="81fb5-789">string</span></span>  

### <a name="return-value---widthofstring100mm"></a><span data-ttu-id="81fb5-790">戻り値 - widthOfString100mm</span><span class="sxs-lookup"><span data-stu-id="81fb5-790">Return Value - widthOfString100mm</span></span>

## <a name="method-widthstr"></a><span data-ttu-id="81fb5-791">メソッド widthStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-791">Method widthStr</span></span>

```xpp
public str widthStr([str value])
```

### <a name="parameters---widthstr"></a><span data-ttu-id="81fb5-792">パラメーター - widthStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-792">Parameters - widthStr</span></span>

<span data-ttu-id="81fb5-793">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-793">value</span></span>  

### <a name="return-value---widthstr"></a><span data-ttu-id="81fb5-794">戻り値 - widthStr</span><span class="sxs-lookup"><span data-stu-id="81fb5-794">Return Value - widthStr</span></span>

## <a name="method-widthunit"></a><span data-ttu-id="81fb5-795">メソッド widthUnit</span><span class="sxs-lookup"><span data-stu-id="81fb5-795">Method widthUnit</span></span>

```xpp
public Units widthUnit([Units value])
```

### <a name="parameters---widthunit"></a><span data-ttu-id="81fb5-796">パラメーター - widthUnit</span><span class="sxs-lookup"><span data-stu-id="81fb5-796">Parameters - widthUnit</span></span>

<span data-ttu-id="81fb5-797">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-797">value</span></span>  

### <a name="return-value---widthunit"></a><span data-ttu-id="81fb5-798">戻り値 - widthUnit</span><span class="sxs-lookup"><span data-stu-id="81fb5-798">Return Value - widthUnit</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="81fb5-799">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-799">Method widthValue</span></span>

<span data-ttu-id="81fb5-800">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-800">Gets or sets the width of the control.</span></span>

```xpp
public Real widthValue([Real value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="81fb5-801">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-801">Parameters - widthValue</span></span>

<span data-ttu-id="81fb5-802">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-802">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="81fb5-803">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-803">Return Value - widthValue</span></span>

<span data-ttu-id="81fb5-804">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="81fb5-804">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="81fb5-805">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="81fb5-805">Remarks - widthValue</span></span>

<span data-ttu-id="81fb5-806">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-806">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-width"></a><span data-ttu-id="81fb5-807">メソッド width</span><span class="sxs-lookup"><span data-stu-id="81fb5-807">Method width</span></span>

<span data-ttu-id="81fb5-808">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-808">Gets or sets the width of the control.</span></span>

```xpp
public void width(Real value, Units unit)
```

### <a name="parameters---width"></a><span data-ttu-id="81fb5-809">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="81fb5-809">Parameters - width</span></span>

<span data-ttu-id="81fb5-810">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-810">value</span></span>  

<!-- -->

<span data-ttu-id="81fb5-811">単位</span><span class="sxs-lookup"><span data-stu-id="81fb5-811">unit</span></span>  

### <a name="remarks---width"></a><span data-ttu-id="81fb5-812">備考 - width</span><span class="sxs-lookup"><span data-stu-id="81fb5-812">Remarks - width</span></span>

<span data-ttu-id="81fb5-813">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="81fb5-813">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="81fb5-814">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="81fb5-814">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="81fb5-815">モード。</span><span class="sxs-lookup"><span data-stu-id="81fb5-815">Mode.</span></span>           | <span data-ttu-id="81fb5-816">幅計算。</span><span class="sxs-lookup"><span data-stu-id="81fb5-816">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="81fb5-817">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="81fb5-817">-1 Exact.</span></span>       | <span data-ttu-id="81fb5-818">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="81fb5-818">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="81fb5-819">0 自動。</span><span class="sxs-lookup"><span data-stu-id="81fb5-819">0 Auto.</span></span>         | <span data-ttu-id="81fb5-820">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="81fb5-820">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="81fb5-821">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="81fb5-821">1 Column width.</span></span> | <span data-ttu-id="81fb5-822">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="81fb5-822">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="81fb5-823">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="81fb5-823">The width and width calculation mode can be set separately.</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="81fb5-824">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="81fb5-824">Method bottomMargin</span></span>

```xpp
public void bottomMargin(Real value, Units unit)
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="81fb5-825">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="81fb5-825">Parameters - bottomMargin</span></span>

<span data-ttu-id="81fb5-826">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-826">value</span></span>  

<!-- -->

<span data-ttu-id="81fb5-827">単位</span><span class="sxs-lookup"><span data-stu-id="81fb5-827">unit</span></span>  

## <a name="method-rightmargin"></a><span data-ttu-id="81fb5-828">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="81fb5-828">Method rightMargin</span></span>

```xpp
public void rightMargin(Real value, Units unit)
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="81fb5-829">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="81fb5-829">Parameters - rightMargin</span></span>

<span data-ttu-id="81fb5-830">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-830">value</span></span>  

<!-- -->

<span data-ttu-id="81fb5-831">単位</span><span class="sxs-lookup"><span data-stu-id="81fb5-831">unit</span></span>  

## <a name="method-leftmargin"></a><span data-ttu-id="81fb5-832">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="81fb5-832">Method leftMargin</span></span>

```xpp
public void leftMargin(Real value, Units unit)
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="81fb5-833">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="81fb5-833">Parameters - leftMargin</span></span>

<span data-ttu-id="81fb5-834">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-834">value</span></span>  

<!-- -->

<span data-ttu-id="81fb5-835">単位</span><span class="sxs-lookup"><span data-stu-id="81fb5-835">unit</span></span>  

## <a name="method-topmargin"></a><span data-ttu-id="81fb5-836">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="81fb5-836">Method topMargin</span></span>

```xpp
public void topMargin(Real value, Units unit)
```

### <a name="parameters---topmargin"></a><span data-ttu-id="81fb5-837">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="81fb5-837">Parameters - topMargin</span></span>

<span data-ttu-id="81fb5-838">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-838">value</span></span>  

<!-- -->

<span data-ttu-id="81fb5-839">単位</span><span class="sxs-lookup"><span data-stu-id="81fb5-839">unit</span></span>  

## <a name="method-top"></a><span data-ttu-id="81fb5-840">メソッド top</span><span class="sxs-lookup"><span data-stu-id="81fb5-840">Method top</span></span>

```xpp
public void top(Real value, Units unit)
```

### <a name="parameters---top"></a><span data-ttu-id="81fb5-841">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="81fb5-841">Parameters - top</span></span>

<span data-ttu-id="81fb5-842">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-842">value</span></span>  

<!-- -->

<span data-ttu-id="81fb5-843">単位</span><span class="sxs-lookup"><span data-stu-id="81fb5-843">unit</span></span>  

## <a name="method-left"></a><span data-ttu-id="81fb5-844">メソッド left</span><span class="sxs-lookup"><span data-stu-id="81fb5-844">Method left</span></span>

```xpp
public void left(Real value, Units unit)
```

### <a name="parameters---left"></a><span data-ttu-id="81fb5-845">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="81fb5-845">Parameters - left</span></span>

<span data-ttu-id="81fb5-846">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-846">value</span></span>  

<!-- -->

<span data-ttu-id="81fb5-847">単位</span><span class="sxs-lookup"><span data-stu-id="81fb5-847">unit</span></span>  

## <a name="method-show"></a><span data-ttu-id="81fb5-848">メソッド show</span><span class="sxs-lookup"><span data-stu-id="81fb5-848">Method show</span></span>

```xpp
public void show()
```

## <a name="method-height"></a><span data-ttu-id="81fb5-849">メソッド height</span><span class="sxs-lookup"><span data-stu-id="81fb5-849">Method height</span></span>

<span data-ttu-id="81fb5-850">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="81fb5-850">Gets or sets the height of the control.</span></span>

```xpp
public void height(Real value, Units unit)
```

### <a name="parameters---height"></a><span data-ttu-id="81fb5-851">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="81fb5-851">Parameters - height</span></span>

<span data-ttu-id="81fb5-852">値</span><span class="sxs-lookup"><span data-stu-id="81fb5-852">value</span></span>  

<!-- -->

<span data-ttu-id="81fb5-853">単位</span><span class="sxs-lookup"><span data-stu-id="81fb5-853">unit</span></span>  

### <a name="remarks---height"></a><span data-ttu-id="81fb5-854">備考 - height</span><span class="sxs-lookup"><span data-stu-id="81fb5-854">Remarks - height</span></span>

<span data-ttu-id="81fb5-855">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="81fb5-855">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="81fb5-856">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="81fb5-856">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="81fb5-857">モード。</span><span class="sxs-lookup"><span data-stu-id="81fb5-857">Mode.</span></span>            | <span data-ttu-id="81fb5-858">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="81fb5-858">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="81fb5-859">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="81fb5-859">-1 Exact.</span></span>        | <span data-ttu-id="81fb5-860">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="81fb5-860">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="81fb5-861">0 自動。</span><span class="sxs-lookup"><span data-stu-id="81fb5-861">0 Auto.</span></span>          | <span data-ttu-id="81fb5-862">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="81fb5-862">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="81fb5-863">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="81fb5-863">1 Column height.</span></span> | <span data-ttu-id="81fb5-864">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="81fb5-864">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="81fb5-865">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="81fb5-865">The height and height calculation mode can be set separately.</span></span>

## <a name="method-hide"></a><span data-ttu-id="81fb5-866">メソッド hide</span><span class="sxs-lookup"><span data-stu-id="81fb5-866">Method hide</span></span>

```xpp
public void hide()
```

