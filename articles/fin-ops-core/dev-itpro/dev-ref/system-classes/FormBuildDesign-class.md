---
title: FormBuildDesign クラス
description: このトピックでは、FormBuildDesign クラスについて説明します。
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
ms.openlocfilehash: 355e0be156dedcc9549b275ca84abe8c4d1ce4b6
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502652"
---
# <a name="class-formbuilddesign"></a><span data-ttu-id="4f8c7-103">クラス FormBuildDesign</span><span class="sxs-lookup"><span data-stu-id="4f8c7-103">Class FormBuildDesign</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildDesign extends Object
```

<span data-ttu-id="4f8c7-104">FormBuildDesign クラスは、フォーム デザインを変更します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-104">The FormBuildDesign class modifies a form design.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f8c7-105">備考</span><span class="sxs-lookup"><span data-stu-id="4f8c7-105">Remarks</span></span>

<span data-ttu-id="4f8c7-106">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-106">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="4f8c7-107">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-107">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="4f8c7-108">例</span><span class="sxs-lookup"><span data-stu-id="4f8c7-108">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="4f8c7-109">メソッド</span><span class="sxs-lookup"><span data-stu-id="4f8c7-109">Methods</span></span>

| <span data-ttu-id="4f8c7-110">方法</span><span class="sxs-lookup"><span data-stu-id="4f8c7-110">Method</span></span>                                                                                                                          | <span data-ttu-id="4f8c7-111">説明</span><span class="sxs-lookup"><span data-stu-id="4f8c7-111">Description</span></span>                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="4f8c7-112">public Object addControl(FormControlType controlType, str controlName, \[FormBuildControl insertAfter\], \[boolean pushFront\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-112">public Object addControl(FormControlType controlType, str controlName, \[FormBuildControl insertAfter\], \[boolean pushFront\])</span></span> |                                                                             |
| <span data-ttu-id="4f8c7-113">public Object addControlEx(str controlClass, str controlName, \[FormBuildControl insertAfter\], \[boolean pushFront\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-113">public Object addControlEx(str controlClass, str controlName, \[FormBuildControl insertAfter\], \[boolean pushFront\])</span></span>          |                                                                             |
| <span data-ttu-id="4f8c7-114">public boolean alignChild(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-114">public boolean alignChild(\[boolean value\])</span></span>                                                                                    |                                                                             |
| <span data-ttu-id="4f8c7-115">public boolean alignChildren(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-115">public boolean alignChildren(\[boolean value\])</span></span>                                                                                 |                                                                             |
| <span data-ttu-id="4f8c7-116">public boolean allowDocking(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-116">public boolean allowDocking(\[boolean value\])</span></span>                                                                                  |                                                                             |
| <span data-ttu-id="4f8c7-117">public boolean allowFormCompanyChange(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-117">public boolean allowFormCompanyChange(\[boolean value\])</span></span>                                                                        |                                                                             |
| <span data-ttu-id="4f8c7-118">public boolean allowImplicitParent(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-118">public boolean allowImplicitParent(\[boolean value\])</span></span>                                                                           |                                                                             |
| <span data-ttu-id="4f8c7-119">public int allowUserSetup(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-119">public int allowUserSetup(\[int value\])</span></span>                                                                                        |                                                                             |
| <span data-ttu-id="4f8c7-120">public boolean alwaysOnTop(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-120">public boolean alwaysOnTop(\[boolean value\])</span></span>                                                                                   |                                                                             |
| <span data-ttu-id="4f8c7-121">public int arrangeGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-121">public int arrangeGuide(\[int value\])</span></span>                                                                                          |                                                                             |
| <span data-ttu-id="4f8c7-122">public int arrangeMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-122">public int arrangeMethod(\[int value\])</span></span>                                                                                         |                                                                             |
| <span data-ttu-id="4f8c7-123">public int arrangeWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-123">public int arrangeWhen(\[int value\])</span></span>                                                                                           |                                                                             |
| <span data-ttu-id="4f8c7-124">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-124">public int backgroundColor(\[int value\])</span></span>                                                                                       | <span data-ttu-id="4f8c7-125">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-125">Gets or sets the background color of the control.</span></span>                           |
| <span data-ttu-id="4f8c7-126">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-126">public int bold(\[int value\])</span></span>                                                                                                  | <span data-ttu-id="4f8c7-127">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-127">Gets or sets the weight of font that is used to output text in the control.</span></span> |
| <span data-ttu-id="4f8c7-128">public int bottomMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-128">public int bottomMargin(\[int value\], \[AutoMode mode\])</span></span>                                                                       |                                                                             |
| <span data-ttu-id="4f8c7-129">public AutoMode bottomMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-129">public AutoMode bottomMarginMode(\[AutoMode mode\])</span></span>                                                                             |                                                                             |
| <span data-ttu-id="4f8c7-130">public int bottomMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-130">public int bottomMarginValue(\[int value\])</span></span>                                                                                     |                                                                             |
| <span data-ttu-id="4f8c7-131">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-131">public str caption(\[str value\])</span></span>                                                                                               | <span data-ttu-id="4f8c7-132">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-132">Gets or set the caption of the control.</span></span>                                     |
| <span data-ttu-id="4f8c7-133">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-133">public int characterSet(\[int value\])</span></span>                                                                                          | <span data-ttu-id="4f8c7-134">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-134">Gets or sets the character set of the font.</span></span>                                 |
| <span data-ttu-id="4f8c7-135">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-135">public int colorScheme(\[int value\])</span></span>                                                                                           | <span data-ttu-id="4f8c7-136">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-136">Gets or sets the color scheme of the control.</span></span>                               |
| <span data-ttu-id="4f8c7-137">public int columns(\[int value\], \[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-137">public int columns(\[int value\], \[ColumnsMode mode\])</span></span>                                                                         |                                                                             |
| <span data-ttu-id="4f8c7-138">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-138">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span></span>                                                                            |                                                                             |
| <span data-ttu-id="4f8c7-139">public int columnspace(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-139">public int columnspace(\[int value\], \[AutoMode mode\])</span></span>                                                                        |                                                                             |
| <span data-ttu-id="4f8c7-140">public AutoMode columnspaceMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-140">public AutoMode columnspaceMode(\[AutoMode mode\])</span></span>                                                                              |                                                                             |
| <span data-ttu-id="4f8c7-141">public int columnspaceValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-141">public int columnspaceValue(\[int value\])</span></span>                                                                                      |                                                                             |
| <span data-ttu-id="4f8c7-142">public int columnsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-142">public int columnsValue(\[int value\])</span></span>                                                                                          |                                                                             |
| <span data-ttu-id="4f8c7-143">public Object control(AnyType control)</span><span class="sxs-lookup"><span data-stu-id="4f8c7-143">public Object control(AnyType control)</span></span>                                                                                          |                                                                             |
| <span data-ttu-id="4f8c7-144">public int controlCount()</span><span class="sxs-lookup"><span data-stu-id="4f8c7-144">public int controlCount()</span></span>                                                                                                       |                                                                             |
| <span data-ttu-id="4f8c7-145">public FormBuildControl controlNum(int controlNo)</span><span class="sxs-lookup"><span data-stu-id="4f8c7-145">public FormBuildControl controlNum(int controlNo)</span></span>                                                                               |                                                                             |
| <span data-ttu-id="4f8c7-146">public str cssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-146">public str cssClass(\[str value\])</span></span>                                                                                              |                                                                             |
| <span data-ttu-id="4f8c7-147">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-147">public int dataSource(\[AnyType value\])</span></span>                                                                                        | <span data-ttu-id="4f8c7-148">コントロールまたはフォームで使用される必要があるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-148">Gets or sets a data source that should be used by the control or the form.</span></span>  |
| <span data-ttu-id="4f8c7-149">public str defaultAction(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-149">public str defaultAction(\[str value\])</span></span>                                                                                         |                                                                             |
| <span data-ttu-id="4f8c7-150">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-150">public str font(\[str value\])</span></span>                                                                                                  | <span data-ttu-id="4f8c7-151">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-151">Gets or sets the name of the font for the control to use.</span></span>                   |
| <span data-ttu-id="4f8c7-152">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-152">public int fontSize(\[int value\])</span></span>                                                                                              | <span data-ttu-id="4f8c7-153">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-153">Gets or sets the size of the font for the control to use.</span></span>                   |
| <span data-ttu-id="4f8c7-154">public int frame(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-154">public int frame(\[int value\])</span></span>                                                                                                 |                                                                             |
| <span data-ttu-id="4f8c7-155">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-155">public int height(int value, \[int mode\])</span></span>                                                                                      | <span data-ttu-id="4f8c7-156">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-156">Gets or sets the height of the control.</span></span>                                     |
| <span data-ttu-id="4f8c7-157">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-157">public int heightMode(\[int value\])</span></span>                                                                                            | <span data-ttu-id="4f8c7-158">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-158">Gets or sets a calculation mode for the height of the control.</span></span>              |
| <span data-ttu-id="4f8c7-159">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-159">public int heightValue(\[int value\])</span></span>                                                                                           | <span data-ttu-id="4f8c7-160">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-160">Gets or sets the height of the control.</span></span>                                     |
| <span data-ttu-id="4f8c7-161">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-161">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                                                   |                                                                             |
| <span data-ttu-id="4f8c7-162">public boolean hideToolbar(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-162">public boolean hideToolbar(\[boolean value\])</span></span>                                                                                   |                                                                             |
| <span data-ttu-id="4f8c7-163">public int imagemode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-163">public int imagemode(\[int value\])</span></span>                                                                                             |                                                                             |
| <span data-ttu-id="4f8c7-164">public str imageName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-164">public str imageName(\[str value\])</span></span>                                                                                             |                                                                             |
| <span data-ttu-id="4f8c7-165">public int imageResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-165">public int imageResource(\[int value\])</span></span>                                                                                         |                                                                             |
| <span data-ttu-id="4f8c7-166">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-166">public boolean italic(\[boolean value\])</span></span>                                                                                        |                                                                             |
| <span data-ttu-id="4f8c7-167">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-167">public int labelBold(\[int value\])</span></span>                                                                                             |                                                                             |
| <span data-ttu-id="4f8c7-168">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-168">public int labelCharacterSet(\[int value\])</span></span>                                                                                     |                                                                             |
| <span data-ttu-id="4f8c7-169">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-169">public str labelFont(\[str value\])</span></span>                                                                                             |                                                                             |
| <span data-ttu-id="4f8c7-170">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-170">public int labelFontSize(\[int value\])</span></span>                                                                                         |                                                                             |
| <span data-ttu-id="4f8c7-171">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-171">public boolean labelItalic(\[boolean value\])</span></span>                                                                                   |                                                                             |
| <span data-ttu-id="4f8c7-172">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-172">public boolean labelUnderline(\[boolean value\])</span></span>                                                                                |                                                                             |
| <span data-ttu-id="4f8c7-173">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-173">public int left(int value, \[int mode\])</span></span>                                                                                        |                                                                             |
| <span data-ttu-id="4f8c7-174">public int leftMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-174">public int leftMargin(\[int value\], \[AutoMode mode\])</span></span>                                                                         |                                                                             |
| <span data-ttu-id="4f8c7-175">public AutoMode leftMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-175">public AutoMode leftMarginMode(\[AutoMode mode\])</span></span>                                                                               |                                                                             |
| <span data-ttu-id="4f8c7-176">public int leftMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-176">public int leftMarginValue(\[int value\])</span></span>                                                                                       |                                                                             |
| <span data-ttu-id="4f8c7-177">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-177">public int leftMode(\[int value\])</span></span>                                                                                              |                                                                             |
| <span data-ttu-id="4f8c7-178">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-178">public int leftValue(\[int value\])</span></span>                                                                                             |                                                                             |
| <span data-ttu-id="4f8c7-179">public str localWebMenu(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-179">public str localWebMenu(\[str value\])</span></span>                                                                                          |                                                                             |
| <span data-ttu-id="4f8c7-180">public boolean maximizeBox(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-180">public boolean maximizeBox(\[boolean value\])</span></span>                                                                                   |                                                                             |
| <span data-ttu-id="4f8c7-181">public boolean minimizeBox(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-181">public boolean minimizeBox(\[boolean value\])</span></span>                                                                                   |                                                                             |
| <span data-ttu-id="4f8c7-182">public int mode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-182">public int mode(\[int value\])</span></span>                                                                                                  |                                                                             |
| <span data-ttu-id="4f8c7-183">public int moveControl(int controlId, \[int insertAfterControlId\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-183">public int moveControl(int controlId, \[int insertAfterControlId\])</span></span>                                                             |                                                                             |
| <span data-ttu-id="4f8c7-184">public str newRecordAction(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-184">public str newRecordAction(\[str value\])</span></span>                                                                                       |                                                                             |
| <span data-ttu-id="4f8c7-185">public int rightMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-185">public int rightMargin(\[int value\], \[AutoMode mode\])</span></span>                                                                        |                                                                             |
| <span data-ttu-id="4f8c7-186">public AutoMode rightMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-186">public AutoMode rightMarginMode(\[AutoMode mode\])</span></span>                                                                              |                                                                             |
| <span data-ttu-id="4f8c7-187">public int rightMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-187">public int rightMarginValue(\[int value\])</span></span>                                                                                      |                                                                             |
| <span data-ttu-id="4f8c7-188">public boolean saveSize(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-188">public boolean saveSize(\[boolean value\])</span></span>                                                                                      |                                                                             |
| <span data-ttu-id="4f8c7-189">public int scrollbars(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-189">public int scrollbars(\[int value\])</span></span>                                                                                            |                                                                             |
| <span data-ttu-id="4f8c7-190">public boolean setCompany(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-190">public boolean setCompany(\[boolean value\])</span></span>                                                                                    |                                                                             |
| <span data-ttu-id="4f8c7-191">public int showDeleteButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-191">public int showDeleteButton(\[int value\])</span></span>                                                                                      |                                                                             |
| <span data-ttu-id="4f8c7-192">public int showNewButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-192">public int showNewButton(\[int value\])</span></span>                                                                                         |                                                                             |
| <span data-ttu-id="4f8c7-193">public int showWebHelp(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-193">public int showWebHelp(\[int value\])</span></span>                                                                                           |                                                                             |
| <span data-ttu-id="4f8c7-194">public int statusBarStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-194">public int statusBarStyle(\[int value\])</span></span>                                                                                        |                                                                             |
| <span data-ttu-id="4f8c7-195">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-195">public int style(\[int value\])</span></span>                                                                                                 |                                                                             |
| <span data-ttu-id="4f8c7-196">public int submitMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-196">public int submitMethod(\[int value\])</span></span>                                                                                          |                                                                             |
| <span data-ttu-id="4f8c7-197">public boolean supportReload(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-197">public boolean supportReload(\[boolean value\])</span></span>                                                                                 |                                                                             |
| <span data-ttu-id="4f8c7-198">public int titleDatasource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-198">public int titleDatasource(\[AnyType value\])</span></span>                                                                                   |                                                                             |
| <span data-ttu-id="4f8c7-199">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-199">public int top(int value, \[int mode\])</span></span>                                                                                         |                                                                             |
| <span data-ttu-id="4f8c7-200">public int topMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-200">public int topMargin(\[int value\], \[AutoMode mode\])</span></span>                                                                          |                                                                             |
| <span data-ttu-id="4f8c7-201">public AutoMode topMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-201">public AutoMode topMarginMode(\[AutoMode mode\])</span></span>                                                                                |                                                                             |
| <span data-ttu-id="4f8c7-202">public int topMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-202">public int topMarginValue(\[int value\])</span></span>                                                                                        |                                                                             |
| <span data-ttu-id="4f8c7-203">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-203">public int topMode(\[int value\])</span></span>                                                                                               |                                                                             |
| <span data-ttu-id="4f8c7-204">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-204">public int topValue(\[int value\])</span></span>                                                                                              |                                                                             |
| <span data-ttu-id="4f8c7-205">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-205">public boolean underline(\[boolean value\])</span></span>                                                                                     |                                                                             |
| <span data-ttu-id="4f8c7-206">public int useCaptionFromMenuItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-206">public int useCaptionFromMenuItem(\[int value\])</span></span>                                                                                |                                                                             |
| <span data-ttu-id="4f8c7-207">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-207">public int viewEditMode(\[int value\])</span></span>                                                                                          |                                                                             |
| <span data-ttu-id="4f8c7-208">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-208">public boolean visible(\[boolean value\])</span></span>                                                                                       |                                                                             |
| <span data-ttu-id="4f8c7-209">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-209">public int width(int value, \[int mode\])</span></span>                                                                                       | <span data-ttu-id="4f8c7-210">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-210">Gets or sets the width of the control.</span></span>                                      |
| <span data-ttu-id="4f8c7-211">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-211">public int widthMode(\[int value\])</span></span>                                                                                             | <span data-ttu-id="4f8c7-212">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-212">Gets or sets the calculation mode of the width of the control.</span></span>              |
| <span data-ttu-id="4f8c7-213">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-213">public int widthValue(\[int value\])</span></span>                                                                                            | <span data-ttu-id="4f8c7-214">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-214">Gets or sets the width of the control.</span></span>                                      |
| <span data-ttu-id="4f8c7-215">public int windowResize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-215">public int windowResize(\[int value\])</span></span>                                                                                          |                                                                             |
| <span data-ttu-id="4f8c7-216">public int windowType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-216">public int windowType(\[int value\])</span></span>                                                                                            |                                                                             |
| <span data-ttu-id="4f8c7-217">public int workflowDatasource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-217">public int workflowDatasource(\[AnyType value\])</span></span>                                                                                |                                                                             |
| <span data-ttu-id="4f8c7-218">public boolean workflowEnabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-218">public boolean workflowEnabled(\[boolean value\])</span></span>                                                                               |                                                                             |
| <span data-ttu-id="4f8c7-219">public str workflowType(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-219">public str workflowType(\[str value\])</span></span>                                                                                          |                                                                             |
| <span data-ttu-id="4f8c7-220">public int dialogSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4f8c7-220">public int dialogSize(\[int value\])</span></span>                                                                                            |                                                                             |

## <a name="method-addcontrol"></a><span data-ttu-id="4f8c7-221">メソッド addControl</span><span class="sxs-lookup"><span data-stu-id="4f8c7-221">Method addControl</span></span>

```xpp
public Object addControl(FormControlType controlType, str controlName, [FormBuildControl insertAfter], [boolean pushFront])
```

### <a name="parameters---addcontrol"></a><span data-ttu-id="4f8c7-222">パラメーター - addControl</span><span class="sxs-lookup"><span data-stu-id="4f8c7-222">Parameters - addControl</span></span>

<span data-ttu-id="4f8c7-223">controlType</span><span class="sxs-lookup"><span data-stu-id="4f8c7-223">controlType</span></span>  

<!-- -->

<span data-ttu-id="4f8c7-224">controlName</span><span class="sxs-lookup"><span data-stu-id="4f8c7-224">controlName</span></span>  

<!-- -->

<span data-ttu-id="4f8c7-225">insertAfter</span><span class="sxs-lookup"><span data-stu-id="4f8c7-225">insertAfter</span></span>  

<!-- -->

<span data-ttu-id="4f8c7-226">pushFront</span><span class="sxs-lookup"><span data-stu-id="4f8c7-226">pushFront</span></span>  

### <a name="return-value---addcontrol"></a><span data-ttu-id="4f8c7-227">戻り値 - addControl</span><span class="sxs-lookup"><span data-stu-id="4f8c7-227">Return Value - addControl</span></span>

## <a name="method-addcontrolex"></a><span data-ttu-id="4f8c7-228">メソッド addControlEx</span><span class="sxs-lookup"><span data-stu-id="4f8c7-228">Method addControlEx</span></span>

```xpp
public Object addControlEx(str controlClass, str controlName, [FormBuildControl insertAfter], [boolean pushFront])
```

### <a name="parameters---addcontrolex"></a><span data-ttu-id="4f8c7-229">パラメーター - addControlEx</span><span class="sxs-lookup"><span data-stu-id="4f8c7-229">Parameters - addControlEx</span></span>

<span data-ttu-id="4f8c7-230">controlClass</span><span class="sxs-lookup"><span data-stu-id="4f8c7-230">controlClass</span></span>  

<!-- -->

<span data-ttu-id="4f8c7-231">controlName</span><span class="sxs-lookup"><span data-stu-id="4f8c7-231">controlName</span></span>  

<!-- -->

<span data-ttu-id="4f8c7-232">insertAfter</span><span class="sxs-lookup"><span data-stu-id="4f8c7-232">insertAfter</span></span>  

<!-- -->

<span data-ttu-id="4f8c7-233">pushFront</span><span class="sxs-lookup"><span data-stu-id="4f8c7-233">pushFront</span></span>  

### <a name="return-value---addcontrolex"></a><span data-ttu-id="4f8c7-234">戻り値 - addControlEx</span><span class="sxs-lookup"><span data-stu-id="4f8c7-234">Return Value - addControlEx</span></span>

## <a name="method-alignchild"></a><span data-ttu-id="4f8c7-235">メソッド alignChild</span><span class="sxs-lookup"><span data-stu-id="4f8c7-235">Method alignChild</span></span>

```xpp
public boolean alignChild([boolean value])
```

### <a name="parameters---alignchild"></a><span data-ttu-id="4f8c7-236">パラメーター - alignChild</span><span class="sxs-lookup"><span data-stu-id="4f8c7-236">Parameters - alignChild</span></span>

<span data-ttu-id="4f8c7-237">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-237">value</span></span>  

### <a name="return-value---alignchild"></a><span data-ttu-id="4f8c7-238">戻り値 - alignChild</span><span class="sxs-lookup"><span data-stu-id="4f8c7-238">Return Value - alignChild</span></span>

## <a name="method-alignchildren"></a><span data-ttu-id="4f8c7-239">メソッド alignChildren</span><span class="sxs-lookup"><span data-stu-id="4f8c7-239">Method alignChildren</span></span>

```xpp
public boolean alignChildren([boolean value])
```

### <a name="parameters---alignchildren"></a><span data-ttu-id="4f8c7-240">パラメーター - alignChildren</span><span class="sxs-lookup"><span data-stu-id="4f8c7-240">Parameters - alignChildren</span></span>

<span data-ttu-id="4f8c7-241">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-241">value</span></span>  

### <a name="return-value---alignchildren"></a><span data-ttu-id="4f8c7-242">戻り値 - alignChildren</span><span class="sxs-lookup"><span data-stu-id="4f8c7-242">Return Value - alignChildren</span></span>

## <a name="method-allowdocking"></a><span data-ttu-id="4f8c7-243">メソッド allowDocking</span><span class="sxs-lookup"><span data-stu-id="4f8c7-243">Method allowDocking</span></span>

```xpp
public boolean allowDocking([boolean value])
```

### <a name="parameters---allowdocking"></a><span data-ttu-id="4f8c7-244">パラメーター - allowDocking</span><span class="sxs-lookup"><span data-stu-id="4f8c7-244">Parameters - allowDocking</span></span>

<span data-ttu-id="4f8c7-245">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-245">value</span></span>  

### <a name="return-value---allowdocking"></a><span data-ttu-id="4f8c7-246">戻り値 - allowDocking</span><span class="sxs-lookup"><span data-stu-id="4f8c7-246">Return Value - allowDocking</span></span>

## <a name="method-allowformcompanychange"></a><span data-ttu-id="4f8c7-247">メソッド allowFormCompanyChange</span><span class="sxs-lookup"><span data-stu-id="4f8c7-247">Method allowFormCompanyChange</span></span>

```xpp
public boolean allowFormCompanyChange([boolean value])
```

### <a name="parameters---allowformcompanychange"></a><span data-ttu-id="4f8c7-248">パラメーター - allowFormCompanyChange</span><span class="sxs-lookup"><span data-stu-id="4f8c7-248">Parameters - allowFormCompanyChange</span></span>

<span data-ttu-id="4f8c7-249">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-249">value</span></span>  

### <a name="return-value---allowformcompanychange"></a><span data-ttu-id="4f8c7-250">戻り値 - allowFormCompanyChange</span><span class="sxs-lookup"><span data-stu-id="4f8c7-250">Return Value - allowFormCompanyChange</span></span>

## <a name="method-allowimplicitparent"></a><span data-ttu-id="4f8c7-251">メソッド allowImplicitParent</span><span class="sxs-lookup"><span data-stu-id="4f8c7-251">Method allowImplicitParent</span></span>

```xpp
public boolean allowImplicitParent([boolean value])
```

### <a name="parameters---allowimplicitparent"></a><span data-ttu-id="4f8c7-252">パラメーター - allowImplicitParent</span><span class="sxs-lookup"><span data-stu-id="4f8c7-252">Parameters - allowImplicitParent</span></span>

<span data-ttu-id="4f8c7-253">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-253">value</span></span>  

### <a name="return-value---allowimplicitparent"></a><span data-ttu-id="4f8c7-254">戻り値 - allowImplicitParent</span><span class="sxs-lookup"><span data-stu-id="4f8c7-254">Return Value - allowImplicitParent</span></span>

## <a name="method-allowusersetup"></a><span data-ttu-id="4f8c7-255">メソッド allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="4f8c7-255">Method allowUserSetup</span></span>

```xpp
public int allowUserSetup([int value])
```

### <a name="parameters---allowusersetup"></a><span data-ttu-id="4f8c7-256">パラメーター - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="4f8c7-256">Parameters - allowUserSetup</span></span>

<span data-ttu-id="4f8c7-257">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-257">value</span></span>  

### <a name="return-value---allowusersetup"></a><span data-ttu-id="4f8c7-258">戻り値 - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="4f8c7-258">Return Value - allowUserSetup</span></span>

## <a name="method-alwaysontop"></a><span data-ttu-id="4f8c7-259">メソッド alwaysOnTop</span><span class="sxs-lookup"><span data-stu-id="4f8c7-259">Method alwaysOnTop</span></span>

```xpp
public boolean alwaysOnTop([boolean value])
```

### <a name="parameters---alwaysontop"></a><span data-ttu-id="4f8c7-260">パラメーター - alwaysOnTop</span><span class="sxs-lookup"><span data-stu-id="4f8c7-260">Parameters - alwaysOnTop</span></span>

<span data-ttu-id="4f8c7-261">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-261">value</span></span>  

### <a name="return-value---alwaysontop"></a><span data-ttu-id="4f8c7-262">戻り値 - alwaysOnTop</span><span class="sxs-lookup"><span data-stu-id="4f8c7-262">Return Value - alwaysOnTop</span></span>

## <a name="method-arrangeguide"></a><span data-ttu-id="4f8c7-263">メソッド arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="4f8c7-263">Method arrangeGuide</span></span>

```xpp
public int arrangeGuide([int value])
```

### <a name="parameters---arrangeguide"></a><span data-ttu-id="4f8c7-264">パラメーター - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="4f8c7-264">Parameters - arrangeGuide</span></span>

<span data-ttu-id="4f8c7-265">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-265">value</span></span>  

### <a name="return-value---arrangeguide"></a><span data-ttu-id="4f8c7-266">戻り値 - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="4f8c7-266">Return Value - arrangeGuide</span></span>

## <a name="method-arrangemethod"></a><span data-ttu-id="4f8c7-267">メソッド arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="4f8c7-267">Method arrangeMethod</span></span>

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a><span data-ttu-id="4f8c7-268">パラメーター - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="4f8c7-268">Parameters - arrangeMethod</span></span>

<span data-ttu-id="4f8c7-269">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-269">value</span></span>  

### <a name="return-value---arrangemethod"></a><span data-ttu-id="4f8c7-270">戻り値 - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="4f8c7-270">Return Value - arrangeMethod</span></span>

## <a name="method-arrangewhen"></a><span data-ttu-id="4f8c7-271">メソッド arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="4f8c7-271">Method arrangeWhen</span></span>

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a><span data-ttu-id="4f8c7-272">パラメーター - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="4f8c7-272">Parameters - arrangeWhen</span></span>

<span data-ttu-id="4f8c7-273">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-273">value</span></span>  

### <a name="return-value---arrangewhen"></a><span data-ttu-id="4f8c7-274">戻り値 - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="4f8c7-274">Return Value - arrangeWhen</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="4f8c7-275">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="4f8c7-275">Method backgroundColor</span></span>

<span data-ttu-id="4f8c7-276">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-276">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="4f8c7-277">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="4f8c7-277">Parameters - backgroundColor</span></span>

<span data-ttu-id="4f8c7-278">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-278">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="4f8c7-279">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="4f8c7-279">Return Value - backgroundColor</span></span>

<span data-ttu-id="4f8c7-280">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-280">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="4f8c7-281">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="4f8c7-281">Remarks - backgroundColor</span></span>

<span data-ttu-id="4f8c7-282">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-282">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="4f8c7-283">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-283">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="4f8c7-284">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-284">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="4f8c7-285">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-285">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="4f8c7-286">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-286">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="4f8c7-287">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-287">The maximum value for a single byte is 255.</span></span>

## <a name="method-bold"></a><span data-ttu-id="4f8c7-288">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="4f8c7-288">Method bold</span></span>

<span data-ttu-id="4f8c7-289">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-289">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="4f8c7-290">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="4f8c7-290">Parameters - bold</span></span>

<span data-ttu-id="4f8c7-291">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-291">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="4f8c7-292">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="4f8c7-292">Return Value - bold</span></span>

<span data-ttu-id="4f8c7-293">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-293">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="4f8c7-294">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="4f8c7-294">Remarks - bold</span></span>

<span data-ttu-id="4f8c7-295">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-295">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="4f8c7-296">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-296">0 Use the default font weight.</span></span>
-   <span data-ttu-id="4f8c7-297">1 シン。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-297">1 Thin.</span></span>
-   <span data-ttu-id="4f8c7-298">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-298">2 Extra-light.</span></span>
-   <span data-ttu-id="4f8c7-299">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-299">3 Light.</span></span>
-   <span data-ttu-id="4f8c7-300">4 標準。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-300">4 Normal.</span></span>
-   <span data-ttu-id="4f8c7-301">5 中。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-301">5 Medium.</span></span>
-   <span data-ttu-id="4f8c7-302">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-302">6 Semibold.</span></span>
-   <span data-ttu-id="4f8c7-303">7 太字。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-303">7 Bold.</span></span>
-   <span data-ttu-id="4f8c7-304">8 極太。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-304">8 Extra-bold.</span></span>
-   <span data-ttu-id="4f8c7-305">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-305">9 Heavy.</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="4f8c7-306">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="4f8c7-306">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="4f8c7-307">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="4f8c7-307">Parameters - bottomMargin</span></span>

<span data-ttu-id="4f8c7-308">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-308">value</span></span>  

<!-- -->

<span data-ttu-id="4f8c7-309">モード</span><span class="sxs-lookup"><span data-stu-id="4f8c7-309">mode</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="4f8c7-310">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="4f8c7-310">Return Value - bottomMargin</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="4f8c7-311">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-311">Method bottomMarginMode</span></span>

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="4f8c7-312">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-312">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="4f8c7-313">モード</span><span class="sxs-lookup"><span data-stu-id="4f8c7-313">mode</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="4f8c7-314">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-314">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="4f8c7-315">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-315">Method bottomMarginValue</span></span>

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="4f8c7-316">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-316">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="4f8c7-317">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-317">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="4f8c7-318">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-318">Return Value - bottomMarginValue</span></span>

## <a name="method-caption"></a><span data-ttu-id="4f8c7-319">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="4f8c7-319">Method caption</span></span>

<span data-ttu-id="4f8c7-320">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-320">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="4f8c7-321">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="4f8c7-321">Parameters - caption</span></span>

<span data-ttu-id="4f8c7-322">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-322">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="4f8c7-323">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="4f8c7-323">Return Value - caption</span></span>

<span data-ttu-id="4f8c7-324">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-324">The string that is used as the caption of the control.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="4f8c7-325">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="4f8c7-325">Method characterSet</span></span>

<span data-ttu-id="4f8c7-326">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-326">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="4f8c7-327">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="4f8c7-327">Parameters - characterSet</span></span>

<span data-ttu-id="4f8c7-328">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-328">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="4f8c7-329">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="4f8c7-329">Return Value - characterSet</span></span>

<span data-ttu-id="4f8c7-330">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-330">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="4f8c7-331">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="4f8c7-331">Remarks - characterSet</span></span>

<span data-ttu-id="4f8c7-332">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-332">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="4f8c7-333">値です。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-333">Value.</span></span> | <span data-ttu-id="4f8c7-334">説明。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-334">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="4f8c7-335">0</span><span class="sxs-lookup"><span data-stu-id="4f8c7-335">0</span></span>      | <span data-ttu-id="4f8c7-336">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4f8c7-336">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="4f8c7-337">1</span><span class="sxs-lookup"><span data-stu-id="4f8c7-337">1</span></span>      | <span data-ttu-id="4f8c7-338">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4f8c7-338">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="4f8c7-339">2</span><span class="sxs-lookup"><span data-stu-id="4f8c7-339">2</span></span>      | <span data-ttu-id="4f8c7-340">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4f8c7-340">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="4f8c7-341">77</span><span class="sxs-lookup"><span data-stu-id="4f8c7-341">77</span></span>     | <span data-ttu-id="4f8c7-342">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4f8c7-342">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="4f8c7-343">128</span><span class="sxs-lookup"><span data-stu-id="4f8c7-343">128</span></span>    | <span data-ttu-id="4f8c7-344">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4f8c7-344">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="4f8c7-345">129</span><span class="sxs-lookup"><span data-stu-id="4f8c7-345">129</span></span>    | <span data-ttu-id="4f8c7-346">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4f8c7-346">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="4f8c7-347">134</span><span class="sxs-lookup"><span data-stu-id="4f8c7-347">134</span></span>    | <span data-ttu-id="4f8c7-348">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4f8c7-348">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="4f8c7-349">136</span><span class="sxs-lookup"><span data-stu-id="4f8c7-349">136</span></span>    | <span data-ttu-id="4f8c7-350">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4f8c7-350">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="4f8c7-351">161</span><span class="sxs-lookup"><span data-stu-id="4f8c7-351">161</span></span>    | <span data-ttu-id="4f8c7-352">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4f8c7-352">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="4f8c7-353">162</span><span class="sxs-lookup"><span data-stu-id="4f8c7-353">162</span></span>    | <span data-ttu-id="4f8c7-354">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4f8c7-354">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="4f8c7-355">163</span><span class="sxs-lookup"><span data-stu-id="4f8c7-355">163</span></span>    | <span data-ttu-id="4f8c7-356">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4f8c7-356">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="4f8c7-357">186</span><span class="sxs-lookup"><span data-stu-id="4f8c7-357">186</span></span>    | <span data-ttu-id="4f8c7-358">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4f8c7-358">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="4f8c7-359">204</span><span class="sxs-lookup"><span data-stu-id="4f8c7-359">204</span></span>    | <span data-ttu-id="4f8c7-360">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4f8c7-360">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="4f8c7-361">238</span><span class="sxs-lookup"><span data-stu-id="4f8c7-361">238</span></span>    | <span data-ttu-id="4f8c7-362">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4f8c7-362">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="4f8c7-363">255</span><span class="sxs-lookup"><span data-stu-id="4f8c7-363">255</span></span>    | <span data-ttu-id="4f8c7-364">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4f8c7-364">OEM\_CHARSET</span></span>         |

<span data-ttu-id="4f8c7-365">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-365">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="4f8c7-366">値です。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-366">Value.</span></span> | <span data-ttu-id="4f8c7-367">説明。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-367">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="4f8c7-368">130</span><span class="sxs-lookup"><span data-stu-id="4f8c7-368">130</span></span>    | <span data-ttu-id="4f8c7-369">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4f8c7-369">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="4f8c7-370">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-370">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="4f8c7-371">値です。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-371">Value.</span></span> | <span data-ttu-id="4f8c7-372">説明。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-372">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="4f8c7-373">177</span><span class="sxs-lookup"><span data-stu-id="4f8c7-373">177</span></span>    | <span data-ttu-id="4f8c7-374">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4f8c7-374">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="4f8c7-375">178</span><span class="sxs-lookup"><span data-stu-id="4f8c7-375">178</span></span>    | <span data-ttu-id="4f8c7-376">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4f8c7-376">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="4f8c7-377">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-377">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="4f8c7-378">値です。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-378">Value.</span></span> | <span data-ttu-id="4f8c7-379">説明。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-379">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="4f8c7-380">222</span><span class="sxs-lookup"><span data-stu-id="4f8c7-380">222</span></span>    | <span data-ttu-id="4f8c7-381">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="4f8c7-381">THAI\_CHARSET</span></span> |

<span data-ttu-id="4f8c7-382">既定の文字セットは、現在のシステム ロケールに基づく値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-382">The default character set is set to a value that is based on the current system locale.</span></span> <span data-ttu-id="4f8c7-383">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-383">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="4f8c7-384">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-384">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="4f8c7-385">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="4f8c7-385">Method colorScheme</span></span>

<span data-ttu-id="4f8c7-386">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-386">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="4f8c7-387">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="4f8c7-387">Parameters - colorScheme</span></span>

<span data-ttu-id="4f8c7-388">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-388">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="4f8c7-389">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="4f8c7-389">Return Value - colorScheme</span></span>

<span data-ttu-id="4f8c7-390">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-390">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="4f8c7-391">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="4f8c7-391">Remarks - colorScheme</span></span>

<span data-ttu-id="4f8c7-392">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-392">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="4f8c7-393">値です。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-393">Value.</span></span> | <span data-ttu-id="4f8c7-394">スタイル。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-394">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="4f8c7-395">0</span><span class="sxs-lookup"><span data-stu-id="4f8c7-395">0</span></span>      | <span data-ttu-id="4f8c7-396">既定。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-396">Default.</span></span>                      |
| <span data-ttu-id="4f8c7-397">1</span><span class="sxs-lookup"><span data-stu-id="4f8c7-397">1</span></span>      | <span data-ttu-id="4f8c7-398">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-398">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="4f8c7-399">2</span><span class="sxs-lookup"><span data-stu-id="4f8c7-399">2</span></span>      | <span data-ttu-id="4f8c7-400">真の配色。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-400">The true-color scheme.</span></span>        |

## <a name="method-columns"></a><span data-ttu-id="4f8c7-401">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="4f8c7-401">Method columns</span></span>

```xpp
public int columns([int value], [ColumnsMode mode])
```

### <a name="parameters---columns"></a><span data-ttu-id="4f8c7-402">パラメーター - columns</span><span class="sxs-lookup"><span data-stu-id="4f8c7-402">Parameters - columns</span></span>

<span data-ttu-id="4f8c7-403">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-403">value</span></span>  

<!-- -->

<span data-ttu-id="4f8c7-404">モード</span><span class="sxs-lookup"><span data-stu-id="4f8c7-404">mode</span></span>  

### <a name="return-value---columns"></a><span data-ttu-id="4f8c7-405">戻り値 - columns</span><span class="sxs-lookup"><span data-stu-id="4f8c7-405">Return Value - columns</span></span>

## <a name="method-columnsmode"></a><span data-ttu-id="4f8c7-406">メソッド columnsMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-406">Method columnsMode</span></span>

```xpp
public ColumnsMode columnsMode([ColumnsMode mode])
```

### <a name="parameters---columnsmode"></a><span data-ttu-id="4f8c7-407">パラメーター - columnsMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-407">Parameters - columnsMode</span></span>

<span data-ttu-id="4f8c7-408">モード</span><span class="sxs-lookup"><span data-stu-id="4f8c7-408">mode</span></span>  

### <a name="return-value---columnsmode"></a><span data-ttu-id="4f8c7-409">戻り値 - columnsMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-409">Return Value - columnsMode</span></span>

## <a name="method-columnspace"></a><span data-ttu-id="4f8c7-410">メソッド columnspace</span><span class="sxs-lookup"><span data-stu-id="4f8c7-410">Method columnspace</span></span>

```xpp
public int columnspace([int value], [AutoMode mode])
```

### <a name="parameters---columnspace"></a><span data-ttu-id="4f8c7-411">パラメーター - columnspace</span><span class="sxs-lookup"><span data-stu-id="4f8c7-411">Parameters - columnspace</span></span>

<span data-ttu-id="4f8c7-412">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-412">value</span></span>  

<!-- -->

<span data-ttu-id="4f8c7-413">モード</span><span class="sxs-lookup"><span data-stu-id="4f8c7-413">mode</span></span>  

### <a name="return-value---columnspace"></a><span data-ttu-id="4f8c7-414">戻り値 - columnspace</span><span class="sxs-lookup"><span data-stu-id="4f8c7-414">Return Value - columnspace</span></span>

## <a name="method-columnspacemode"></a><span data-ttu-id="4f8c7-415">メソッド columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-415">Method columnspaceMode</span></span>

```xpp
public AutoMode columnspaceMode([AutoMode mode])
```

### <a name="parameters---columnspacemode"></a><span data-ttu-id="4f8c7-416">パラメーター - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-416">Parameters - columnspaceMode</span></span>

<span data-ttu-id="4f8c7-417">モード</span><span class="sxs-lookup"><span data-stu-id="4f8c7-417">mode</span></span>  

### <a name="return-value---columnspacemode"></a><span data-ttu-id="4f8c7-418">戻り値 - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-418">Return Value - columnspaceMode</span></span>

## <a name="method-columnspacevalue"></a><span data-ttu-id="4f8c7-419">メソッド columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-419">Method columnspaceValue</span></span>

```xpp
public int columnspaceValue([int value])
```

### <a name="parameters---columnspacevalue"></a><span data-ttu-id="4f8c7-420">パラメーター - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-420">Parameters - columnspaceValue</span></span>

<span data-ttu-id="4f8c7-421">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-421">value</span></span>  

### <a name="return-value---columnspacevalue"></a><span data-ttu-id="4f8c7-422">戻り値 - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-422">Return Value - columnspaceValue</span></span>

## <a name="method-columnsvalue"></a><span data-ttu-id="4f8c7-423">メソッド columnsValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-423">Method columnsValue</span></span>

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a><span data-ttu-id="4f8c7-424">パラメーター - columnsValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-424">Parameters - columnsValue</span></span>

<span data-ttu-id="4f8c7-425">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-425">value</span></span>  

### <a name="return-value---columnsvalue"></a><span data-ttu-id="4f8c7-426">戻り値 - columnsValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-426">Return Value - columnsValue</span></span>

## <a name="method-control"></a><span data-ttu-id="4f8c7-427">メソッド control</span><span class="sxs-lookup"><span data-stu-id="4f8c7-427">Method control</span></span>

```xpp
public Object control(AnyType control)
```

### <a name="parameters---control"></a><span data-ttu-id="4f8c7-428">パラメーター - control</span><span class="sxs-lookup"><span data-stu-id="4f8c7-428">Parameters - control</span></span>

<span data-ttu-id="4f8c7-429">control</span><span class="sxs-lookup"><span data-stu-id="4f8c7-429">control</span></span>  

### <a name="return-value---control"></a><span data-ttu-id="4f8c7-430">戻り値 - control</span><span class="sxs-lookup"><span data-stu-id="4f8c7-430">Return Value - control</span></span>

## <a name="method-controlcount"></a><span data-ttu-id="4f8c7-431">メソッド controlCount</span><span class="sxs-lookup"><span data-stu-id="4f8c7-431">Method controlCount</span></span>

```xpp
public int controlCount()
```

### <a name="return-value---controlcount"></a><span data-ttu-id="4f8c7-432">戻り値 - controlCount</span><span class="sxs-lookup"><span data-stu-id="4f8c7-432">Return Value - controlCount</span></span>

## <a name="method-controlnum"></a><span data-ttu-id="4f8c7-433">メソッド controlNum</span><span class="sxs-lookup"><span data-stu-id="4f8c7-433">Method controlNum</span></span>

```xpp
public FormBuildControl controlNum(int controlNo)
```

### <a name="parameters---controlnum"></a><span data-ttu-id="4f8c7-434">パラメーター - controlNum</span><span class="sxs-lookup"><span data-stu-id="4f8c7-434">Parameters - controlNum</span></span>

<span data-ttu-id="4f8c7-435">controlNo</span><span class="sxs-lookup"><span data-stu-id="4f8c7-435">controlNo</span></span>  

### <a name="return-value---controlnum"></a><span data-ttu-id="4f8c7-436">戻り値 - controlNum</span><span class="sxs-lookup"><span data-stu-id="4f8c7-436">Return Value - controlNum</span></span>

## <a name="method-cssclass"></a><span data-ttu-id="4f8c7-437">メソッド cssClass</span><span class="sxs-lookup"><span data-stu-id="4f8c7-437">Method cssClass</span></span>

```xpp
public str cssClass([str value])
```

### <a name="parameters---cssclass"></a><span data-ttu-id="4f8c7-438">パラメーター - cssClass</span><span class="sxs-lookup"><span data-stu-id="4f8c7-438">Parameters - cssClass</span></span>

<span data-ttu-id="4f8c7-439">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-439">value</span></span>  

### <a name="return-value---cssclass"></a><span data-ttu-id="4f8c7-440">戻り値 - cssClass</span><span class="sxs-lookup"><span data-stu-id="4f8c7-440">Return Value - cssClass</span></span>

## <a name="method-datasource"></a><span data-ttu-id="4f8c7-441">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="4f8c7-441">Method dataSource</span></span>

<span data-ttu-id="4f8c7-442">コントロールまたはフォームで使用される必要があるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-442">Gets or sets a data source that should be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="4f8c7-443">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="4f8c7-443">Parameters - dataSource</span></span>

<span data-ttu-id="4f8c7-444">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-444">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="4f8c7-445">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="4f8c7-445">Return Value - dataSource</span></span>

<span data-ttu-id="4f8c7-446">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-446">The identifier of the data source that will be used.</span></span>

## <a name="method-defaultaction"></a><span data-ttu-id="4f8c7-447">メソッド defaultAction</span><span class="sxs-lookup"><span data-stu-id="4f8c7-447">Method defaultAction</span></span>

```xpp
public str defaultAction([str value])
```

### <a name="parameters---defaultaction"></a><span data-ttu-id="4f8c7-448">パラメーター - defaultAction</span><span class="sxs-lookup"><span data-stu-id="4f8c7-448">Parameters - defaultAction</span></span>

<span data-ttu-id="4f8c7-449">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-449">value</span></span>  

### <a name="return-value---defaultaction"></a><span data-ttu-id="4f8c7-450">戻り値 - defaultAction</span><span class="sxs-lookup"><span data-stu-id="4f8c7-450">Return Value - defaultAction</span></span>

## <a name="method-font"></a><span data-ttu-id="4f8c7-451">メソッド font</span><span class="sxs-lookup"><span data-stu-id="4f8c7-451">Method font</span></span>

<span data-ttu-id="4f8c7-452">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-452">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="4f8c7-453">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="4f8c7-453">Parameters - font</span></span>

<span data-ttu-id="4f8c7-454">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-454">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="4f8c7-455">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="4f8c7-455">Return Value - font</span></span>

<span data-ttu-id="4f8c7-456">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-456">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="4f8c7-457">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="4f8c7-457">Method fontSize</span></span>

<span data-ttu-id="4f8c7-458">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-458">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="4f8c7-459">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="4f8c7-459">Parameters - fontSize</span></span>

<span data-ttu-id="4f8c7-460">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-460">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="4f8c7-461">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="4f8c7-461">Return Value - fontSize</span></span>

<span data-ttu-id="4f8c7-462">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-462">The height of the font in points.</span></span>

## <a name="method-frame"></a><span data-ttu-id="4f8c7-463">メソッド frame</span><span class="sxs-lookup"><span data-stu-id="4f8c7-463">Method frame</span></span>

```xpp
public int frame([int value])
```

### <a name="parameters---frame"></a><span data-ttu-id="4f8c7-464">パラメーター - frame</span><span class="sxs-lookup"><span data-stu-id="4f8c7-464">Parameters - frame</span></span>

<span data-ttu-id="4f8c7-465">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-465">value</span></span>  

### <a name="return-value---frame"></a><span data-ttu-id="4f8c7-466">戻り値 - frame</span><span class="sxs-lookup"><span data-stu-id="4f8c7-466">Return Value - frame</span></span>

## <a name="method-height"></a><span data-ttu-id="4f8c7-467">メソッド height</span><span class="sxs-lookup"><span data-stu-id="4f8c7-467">Method height</span></span>

<span data-ttu-id="4f8c7-468">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-468">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="4f8c7-469">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="4f8c7-469">Parameters - height</span></span>

<span data-ttu-id="4f8c7-470">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-470">value</span></span>  

<!-- -->

<span data-ttu-id="4f8c7-471">モード</span><span class="sxs-lookup"><span data-stu-id="4f8c7-471">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="4f8c7-472">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="4f8c7-472">Return Value - height</span></span>

<span data-ttu-id="4f8c7-473">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-473">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="4f8c7-474">備考 - height</span><span class="sxs-lookup"><span data-stu-id="4f8c7-474">Remarks - height</span></span>

<span data-ttu-id="4f8c7-475">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-475">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="4f8c7-476">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="4f8c7-476">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="4f8c7-477">モード。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-477">Mode.</span></span>            | <span data-ttu-id="4f8c7-478">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-478">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f8c7-479">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-479">-1 Exact.</span></span>        | <span data-ttu-id="4f8c7-480">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-480">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="4f8c7-481">0 自動。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-481">0 Auto.</span></span>          | <span data-ttu-id="4f8c7-482">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-482">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="4f8c7-483">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-483">1 Column height.</span></span> | <span data-ttu-id="4f8c7-484">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-484">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="4f8c7-485">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-485">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="4f8c7-486">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-486">Method heightMode</span></span>

<span data-ttu-id="4f8c7-487">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-487">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="4f8c7-488">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-488">Parameters - heightMode</span></span>

<span data-ttu-id="4f8c7-489">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-489">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="4f8c7-490">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-490">Return Value - heightMode</span></span>

<span data-ttu-id="4f8c7-491">計算モード。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-491">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="4f8c7-492">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-492">Remarks - heightMode</span></span>

<span data-ttu-id="4f8c7-493">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="4f8c7-493">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="4f8c7-494">モード。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-494">Mode.</span></span>          | <span data-ttu-id="4f8c7-495">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-495">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f8c7-496">正確。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-496">Exact.</span></span>         | <span data-ttu-id="4f8c7-497">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-497">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="4f8c7-498">自動。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-498">Auto.</span></span>          | <span data-ttu-id="4f8c7-499">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-499">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="4f8c7-500">列の高さ</span><span class="sxs-lookup"><span data-stu-id="4f8c7-500">Column height.</span></span> | <span data-ttu-id="4f8c7-501">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-501">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="4f8c7-502">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-502">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="4f8c7-503">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-503">Method heightValue</span></span>

<span data-ttu-id="4f8c7-504">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-504">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="4f8c7-505">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-505">Parameters - heightValue</span></span>

<span data-ttu-id="4f8c7-506">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-506">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="4f8c7-507">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-507">Return Value - heightValue</span></span>

<span data-ttu-id="4f8c7-508">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-508">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="4f8c7-509">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-509">Remarks - heightValue</span></span>

<span data-ttu-id="4f8c7-510">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-510">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-hideifempty"></a><span data-ttu-id="4f8c7-511">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="4f8c7-511">Method hideIfEmpty</span></span>

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a><span data-ttu-id="4f8c7-512">パラメーター - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="4f8c7-512">Parameters - hideIfEmpty</span></span>

<span data-ttu-id="4f8c7-513">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-513">value</span></span>  

### <a name="return-value---hideifempty"></a><span data-ttu-id="4f8c7-514">戻り値 - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="4f8c7-514">Return Value - hideIfEmpty</span></span>

## <a name="method-hidetoolbar"></a><span data-ttu-id="4f8c7-515">メソッド hideToolbar</span><span class="sxs-lookup"><span data-stu-id="4f8c7-515">Method hideToolbar</span></span>

```xpp
public boolean hideToolbar([boolean value])
```

### <a name="parameters---hidetoolbar"></a><span data-ttu-id="4f8c7-516">パラメーター - hideToolbar</span><span class="sxs-lookup"><span data-stu-id="4f8c7-516">Parameters - hideToolbar</span></span>

<span data-ttu-id="4f8c7-517">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-517">value</span></span>  

### <a name="return-value---hidetoolbar"></a><span data-ttu-id="4f8c7-518">戻り値 - hideToolbar</span><span class="sxs-lookup"><span data-stu-id="4f8c7-518">Return Value - hideToolbar</span></span>

## <a name="method-imagemode"></a><span data-ttu-id="4f8c7-519">メソッド imagemode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-519">Method imagemode</span></span>

```xpp
public int imagemode([int value])
```

### <a name="parameters---imagemode"></a><span data-ttu-id="4f8c7-520">パラメーター - imagemode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-520">Parameters - imagemode</span></span>

<span data-ttu-id="4f8c7-521">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-521">value</span></span>  

### <a name="return-value---imagemode"></a><span data-ttu-id="4f8c7-522">戻り値 - imagemode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-522">Return Value - imagemode</span></span>

## <a name="method-imagename"></a><span data-ttu-id="4f8c7-523">メソッド imageName</span><span class="sxs-lookup"><span data-stu-id="4f8c7-523">Method imageName</span></span>

```xpp
public str imageName([str value])
```

### <a name="parameters---imagename"></a><span data-ttu-id="4f8c7-524">パラメーター - imageName</span><span class="sxs-lookup"><span data-stu-id="4f8c7-524">Parameters - imageName</span></span>

<span data-ttu-id="4f8c7-525">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-525">value</span></span>  

### <a name="return-value---imagename"></a><span data-ttu-id="4f8c7-526">戻り値 - imageName</span><span class="sxs-lookup"><span data-stu-id="4f8c7-526">Return Value - imageName</span></span>

## <a name="method-imageresource"></a><span data-ttu-id="4f8c7-527">メソッド imageResource</span><span class="sxs-lookup"><span data-stu-id="4f8c7-527">Method imageResource</span></span>

```xpp
public int imageResource([int value])
```

### <a name="parameters---imageresource"></a><span data-ttu-id="4f8c7-528">パラメーター - imageResource</span><span class="sxs-lookup"><span data-stu-id="4f8c7-528">Parameters - imageResource</span></span>

<span data-ttu-id="4f8c7-529">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-529">value</span></span>  

### <a name="return-value---imageresource"></a><span data-ttu-id="4f8c7-530">戻り値 - imageResource</span><span class="sxs-lookup"><span data-stu-id="4f8c7-530">Return Value - imageResource</span></span>

## <a name="method-italic"></a><span data-ttu-id="4f8c7-531">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="4f8c7-531">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="4f8c7-532">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="4f8c7-532">Parameters - italic</span></span>

<span data-ttu-id="4f8c7-533">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-533">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="4f8c7-534">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="4f8c7-534">Return Value - italic</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="4f8c7-535">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="4f8c7-535">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="4f8c7-536">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="4f8c7-536">Parameters - labelBold</span></span>

<span data-ttu-id="4f8c7-537">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-537">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="4f8c7-538">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="4f8c7-538">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="4f8c7-539">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="4f8c7-539">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="4f8c7-540">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="4f8c7-540">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="4f8c7-541">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-541">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="4f8c7-542">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="4f8c7-542">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="4f8c7-543">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="4f8c7-543">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="4f8c7-544">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="4f8c7-544">Parameters - labelFont</span></span>

<span data-ttu-id="4f8c7-545">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-545">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="4f8c7-546">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="4f8c7-546">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="4f8c7-547">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="4f8c7-547">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="4f8c7-548">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="4f8c7-548">Parameters - labelFontSize</span></span>

<span data-ttu-id="4f8c7-549">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-549">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="4f8c7-550">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="4f8c7-550">Return Value - labelFontSize</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="4f8c7-551">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="4f8c7-551">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="4f8c7-552">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="4f8c7-552">Parameters - labelItalic</span></span>

<span data-ttu-id="4f8c7-553">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-553">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="4f8c7-554">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="4f8c7-554">Return Value - labelItalic</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="4f8c7-555">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="4f8c7-555">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="4f8c7-556">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="4f8c7-556">Parameters - labelUnderline</span></span>

<span data-ttu-id="4f8c7-557">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-557">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="4f8c7-558">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="4f8c7-558">Return Value - labelUnderline</span></span>

## <a name="method-left"></a><span data-ttu-id="4f8c7-559">メソッド left</span><span class="sxs-lookup"><span data-stu-id="4f8c7-559">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="4f8c7-560">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="4f8c7-560">Parameters - left</span></span>

<span data-ttu-id="4f8c7-561">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-561">value</span></span>  

<!-- -->

<span data-ttu-id="4f8c7-562">モード</span><span class="sxs-lookup"><span data-stu-id="4f8c7-562">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="4f8c7-563">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="4f8c7-563">Return Value - left</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="4f8c7-564">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="4f8c7-564">Method leftMargin</span></span>

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="4f8c7-565">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="4f8c7-565">Parameters - leftMargin</span></span>

<span data-ttu-id="4f8c7-566">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-566">value</span></span>  

<!-- -->

<span data-ttu-id="4f8c7-567">モード</span><span class="sxs-lookup"><span data-stu-id="4f8c7-567">mode</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="4f8c7-568">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="4f8c7-568">Return Value - leftMargin</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="4f8c7-569">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-569">Method leftMarginMode</span></span>

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="4f8c7-570">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-570">Parameters - leftMarginMode</span></span>

<span data-ttu-id="4f8c7-571">モード</span><span class="sxs-lookup"><span data-stu-id="4f8c7-571">mode</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="4f8c7-572">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-572">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="4f8c7-573">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-573">Method leftMarginValue</span></span>

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="4f8c7-574">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-574">Parameters - leftMarginValue</span></span>

<span data-ttu-id="4f8c7-575">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-575">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="4f8c7-576">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-576">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="4f8c7-577">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-577">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="4f8c7-578">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-578">Parameters - leftMode</span></span>

<span data-ttu-id="4f8c7-579">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-579">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="4f8c7-580">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-580">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="4f8c7-581">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-581">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="4f8c7-582">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-582">Parameters - leftValue</span></span>

<span data-ttu-id="4f8c7-583">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-583">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="4f8c7-584">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-584">Return Value - leftValue</span></span>

## <a name="method-localwebmenu"></a><span data-ttu-id="4f8c7-585">メソッド localWebMenu</span><span class="sxs-lookup"><span data-stu-id="4f8c7-585">Method localWebMenu</span></span>

```xpp
public str localWebMenu([str value])
```

### <a name="parameters---localwebmenu"></a><span data-ttu-id="4f8c7-586">パラメーター - localWebMenu</span><span class="sxs-lookup"><span data-stu-id="4f8c7-586">Parameters - localWebMenu</span></span>

<span data-ttu-id="4f8c7-587">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-587">value</span></span>  

### <a name="return-value---localwebmenu"></a><span data-ttu-id="4f8c7-588">戻り値 - localWebMenu</span><span class="sxs-lookup"><span data-stu-id="4f8c7-588">Return Value - localWebMenu</span></span>

## <a name="method-maximizebox"></a><span data-ttu-id="4f8c7-589">メソッド maximizeBox</span><span class="sxs-lookup"><span data-stu-id="4f8c7-589">Method maximizeBox</span></span>

```xpp
public boolean maximizeBox([boolean value])
```

### <a name="parameters---maximizebox"></a><span data-ttu-id="4f8c7-590">パラメーター - maximizeBox</span><span class="sxs-lookup"><span data-stu-id="4f8c7-590">Parameters - maximizeBox</span></span>

<span data-ttu-id="4f8c7-591">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-591">value</span></span>  

### <a name="return-value---maximizebox"></a><span data-ttu-id="4f8c7-592">戻り値 - maximizeBox</span><span class="sxs-lookup"><span data-stu-id="4f8c7-592">Return Value - maximizeBox</span></span>

## <a name="method-minimizebox"></a><span data-ttu-id="4f8c7-593">メソッド minimizeBox</span><span class="sxs-lookup"><span data-stu-id="4f8c7-593">Method minimizeBox</span></span>

```xpp
public boolean minimizeBox([boolean value])
```

### <a name="parameters---minimizebox"></a><span data-ttu-id="4f8c7-594">パラメーター - minimizeBox</span><span class="sxs-lookup"><span data-stu-id="4f8c7-594">Parameters - minimizeBox</span></span>

<span data-ttu-id="4f8c7-595">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-595">value</span></span>  

### <a name="return-value---minimizebox"></a><span data-ttu-id="4f8c7-596">戻り値 - minimizeBox</span><span class="sxs-lookup"><span data-stu-id="4f8c7-596">Return Value - minimizeBox</span></span>

## <a name="method-mode"></a><span data-ttu-id="4f8c7-597">メソッド mode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-597">Method mode</span></span>

```xpp
public int mode([int value])
```

### <a name="parameters---mode"></a><span data-ttu-id="4f8c7-598">パラメーター - mode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-598">Parameters - mode</span></span>

<span data-ttu-id="4f8c7-599">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-599">value</span></span>  

### <a name="return-value---mode"></a><span data-ttu-id="4f8c7-600">戻り値 - mode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-600">Return Value - mode</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="4f8c7-601">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="4f8c7-601">Method moveControl</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterControlId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="4f8c7-602">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="4f8c7-602">Parameters - moveControl</span></span>

<span data-ttu-id="4f8c7-603">controlId</span><span class="sxs-lookup"><span data-stu-id="4f8c7-603">controlId</span></span>  

<!-- -->

<span data-ttu-id="4f8c7-604">insertAfterControlId</span><span class="sxs-lookup"><span data-stu-id="4f8c7-604">insertAfterControlId</span></span>  

### <a name="return-value---movecontrol"></a><span data-ttu-id="4f8c7-605">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="4f8c7-605">Return Value - moveControl</span></span>

## <a name="method-newrecordaction"></a><span data-ttu-id="4f8c7-606">メソッド newRecordAction</span><span class="sxs-lookup"><span data-stu-id="4f8c7-606">Method newRecordAction</span></span>

```xpp
public str newRecordAction([str value])
```

### <a name="parameters---newrecordaction"></a><span data-ttu-id="4f8c7-607">パラメーター - newRecordAction</span><span class="sxs-lookup"><span data-stu-id="4f8c7-607">Parameters - newRecordAction</span></span>

<span data-ttu-id="4f8c7-608">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-608">value</span></span>  

### <a name="return-value---newrecordaction"></a><span data-ttu-id="4f8c7-609">戻り値 - newRecordAction</span><span class="sxs-lookup"><span data-stu-id="4f8c7-609">Return Value - newRecordAction</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="4f8c7-610">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="4f8c7-610">Method rightMargin</span></span>

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="4f8c7-611">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="4f8c7-611">Parameters - rightMargin</span></span>

<span data-ttu-id="4f8c7-612">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-612">value</span></span>  

<!-- -->

<span data-ttu-id="4f8c7-613">モード</span><span class="sxs-lookup"><span data-stu-id="4f8c7-613">mode</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="4f8c7-614">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="4f8c7-614">Return Value - rightMargin</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="4f8c7-615">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-615">Method rightMarginMode</span></span>

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="4f8c7-616">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-616">Parameters - rightMarginMode</span></span>

<span data-ttu-id="4f8c7-617">モード</span><span class="sxs-lookup"><span data-stu-id="4f8c7-617">mode</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="4f8c7-618">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-618">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="4f8c7-619">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-619">Method rightMarginValue</span></span>

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="4f8c7-620">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-620">Parameters - rightMarginValue</span></span>

<span data-ttu-id="4f8c7-621">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-621">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="4f8c7-622">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-622">Return Value - rightMarginValue</span></span>

## <a name="method-savesize"></a><span data-ttu-id="4f8c7-623">メソッド saveSize</span><span class="sxs-lookup"><span data-stu-id="4f8c7-623">Method saveSize</span></span>

```xpp
public boolean saveSize([boolean value])
```

### <a name="parameters---savesize"></a><span data-ttu-id="4f8c7-624">パラメーター - saveSize</span><span class="sxs-lookup"><span data-stu-id="4f8c7-624">Parameters - saveSize</span></span>

<span data-ttu-id="4f8c7-625">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-625">value</span></span>  

### <a name="return-value---savesize"></a><span data-ttu-id="4f8c7-626">戻り値 - saveSize</span><span class="sxs-lookup"><span data-stu-id="4f8c7-626">Return Value - saveSize</span></span>

## <a name="method-scrollbars"></a><span data-ttu-id="4f8c7-627">メソッド scrollbars</span><span class="sxs-lookup"><span data-stu-id="4f8c7-627">Method scrollbars</span></span>

```xpp
public int scrollbars([int value])
```

### <a name="parameters---scrollbars"></a><span data-ttu-id="4f8c7-628">パラメーター - scrollbars</span><span class="sxs-lookup"><span data-stu-id="4f8c7-628">Parameters - scrollbars</span></span>

<span data-ttu-id="4f8c7-629">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-629">value</span></span>  

### <a name="return-value---scrollbars"></a><span data-ttu-id="4f8c7-630">戻り値 - scrollbars</span><span class="sxs-lookup"><span data-stu-id="4f8c7-630">Return Value - scrollbars</span></span>

## <a name="method-setcompany"></a><span data-ttu-id="4f8c7-631">メソッド setCompany</span><span class="sxs-lookup"><span data-stu-id="4f8c7-631">Method setCompany</span></span>

```xpp
public boolean setCompany([boolean value])
```

### <a name="parameters---setcompany"></a><span data-ttu-id="4f8c7-632">パラメーター - setCompany</span><span class="sxs-lookup"><span data-stu-id="4f8c7-632">Parameters - setCompany</span></span>

<span data-ttu-id="4f8c7-633">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-633">value</span></span>  

### <a name="return-value---setcompany"></a><span data-ttu-id="4f8c7-634">戻り値 - setCompany</span><span class="sxs-lookup"><span data-stu-id="4f8c7-634">Return Value - setCompany</span></span>

## <a name="method-showdeletebutton"></a><span data-ttu-id="4f8c7-635">メソッド showDeleteButton</span><span class="sxs-lookup"><span data-stu-id="4f8c7-635">Method showDeleteButton</span></span>

```xpp
public int showDeleteButton([int value])
```

### <a name="parameters---showdeletebutton"></a><span data-ttu-id="4f8c7-636">パラメーター - showDeleteButton</span><span class="sxs-lookup"><span data-stu-id="4f8c7-636">Parameters - showDeleteButton</span></span>

<span data-ttu-id="4f8c7-637">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-637">value</span></span>  

### <a name="return-value---showdeletebutton"></a><span data-ttu-id="4f8c7-638">戻り値 - showDeleteButton</span><span class="sxs-lookup"><span data-stu-id="4f8c7-638">Return Value - showDeleteButton</span></span>

## <a name="method-shownewbutton"></a><span data-ttu-id="4f8c7-639">メソッド showNewButton</span><span class="sxs-lookup"><span data-stu-id="4f8c7-639">Method showNewButton</span></span>

```xpp
public int showNewButton([int value])
```

### <a name="parameters---shownewbutton"></a><span data-ttu-id="4f8c7-640">パラメーター - showNewButton</span><span class="sxs-lookup"><span data-stu-id="4f8c7-640">Parameters - showNewButton</span></span>

<span data-ttu-id="4f8c7-641">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-641">value</span></span>  

### <a name="return-value---shownewbutton"></a><span data-ttu-id="4f8c7-642">戻り値 - showNewButton</span><span class="sxs-lookup"><span data-stu-id="4f8c7-642">Return Value - showNewButton</span></span>

## <a name="method-showwebhelp"></a><span data-ttu-id="4f8c7-643">メソッド showWebHelp</span><span class="sxs-lookup"><span data-stu-id="4f8c7-643">Method showWebHelp</span></span>

```xpp
public int showWebHelp([int value])
```

### <a name="parameters---showwebhelp"></a><span data-ttu-id="4f8c7-644">パラメーター - showWebHelp</span><span class="sxs-lookup"><span data-stu-id="4f8c7-644">Parameters - showWebHelp</span></span>

<span data-ttu-id="4f8c7-645">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-645">value</span></span>  

### <a name="return-value---showwebhelp"></a><span data-ttu-id="4f8c7-646">戻り値 - showWebHelp</span><span class="sxs-lookup"><span data-stu-id="4f8c7-646">Return Value - showWebHelp</span></span>

## <a name="method-statusbarstyle"></a><span data-ttu-id="4f8c7-647">メソッド statusBarStyle</span><span class="sxs-lookup"><span data-stu-id="4f8c7-647">Method statusBarStyle</span></span>

```xpp
public int statusBarStyle([int value])
```

### <a name="parameters---statusbarstyle"></a><span data-ttu-id="4f8c7-648">パラメーター - statusBarStyle</span><span class="sxs-lookup"><span data-stu-id="4f8c7-648">Parameters - statusBarStyle</span></span>

<span data-ttu-id="4f8c7-649">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-649">value</span></span>  

### <a name="return-value---statusbarstyle"></a><span data-ttu-id="4f8c7-650">戻り値 - statusBarStyle</span><span class="sxs-lookup"><span data-stu-id="4f8c7-650">Return Value - statusBarStyle</span></span>

## <a name="method-style"></a><span data-ttu-id="4f8c7-651">メソッド style</span><span class="sxs-lookup"><span data-stu-id="4f8c7-651">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="4f8c7-652">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="4f8c7-652">Parameters - style</span></span>

<span data-ttu-id="4f8c7-653">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-653">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="4f8c7-654">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="4f8c7-654">Return Value - style</span></span>

## <a name="method-submitmethod"></a><span data-ttu-id="4f8c7-655">メソッド submitMethod</span><span class="sxs-lookup"><span data-stu-id="4f8c7-655">Method submitMethod</span></span>

```xpp
public int submitMethod([int value])
```

### <a name="parameters---submitmethod"></a><span data-ttu-id="4f8c7-656">パラメーター - submitMethod</span><span class="sxs-lookup"><span data-stu-id="4f8c7-656">Parameters - submitMethod</span></span>

<span data-ttu-id="4f8c7-657">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-657">value</span></span>  

### <a name="return-value---submitmethod"></a><span data-ttu-id="4f8c7-658">戻り値 - submitMethod</span><span class="sxs-lookup"><span data-stu-id="4f8c7-658">Return Value - submitMethod</span></span>

## <a name="method-supportreload"></a><span data-ttu-id="4f8c7-659">メソッド supportReload</span><span class="sxs-lookup"><span data-stu-id="4f8c7-659">Method supportReload</span></span>

```xpp
public boolean supportReload([boolean value])
```

### <a name="parameters---supportreload"></a><span data-ttu-id="4f8c7-660">パラメーター - supportReload</span><span class="sxs-lookup"><span data-stu-id="4f8c7-660">Parameters - supportReload</span></span>

<span data-ttu-id="4f8c7-661">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-661">value</span></span>  

### <a name="return-value---supportreload"></a><span data-ttu-id="4f8c7-662">戻り値 - supportReload</span><span class="sxs-lookup"><span data-stu-id="4f8c7-662">Return Value - supportReload</span></span>

## <a name="method-titledatasource"></a><span data-ttu-id="4f8c7-663">メソッド titleDatasource</span><span class="sxs-lookup"><span data-stu-id="4f8c7-663">Method titleDatasource</span></span>

```xpp
public int titleDatasource([AnyType value])
```

### <a name="parameters---titledatasource"></a><span data-ttu-id="4f8c7-664">パラメーター - titleDatasource</span><span class="sxs-lookup"><span data-stu-id="4f8c7-664">Parameters - titleDatasource</span></span>

<span data-ttu-id="4f8c7-665">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-665">value</span></span>  

### <a name="return-value---titledatasource"></a><span data-ttu-id="4f8c7-666">戻り値 - titleDatasource</span><span class="sxs-lookup"><span data-stu-id="4f8c7-666">Return Value - titleDatasource</span></span>

## <a name="method-top"></a><span data-ttu-id="4f8c7-667">メソッド top</span><span class="sxs-lookup"><span data-stu-id="4f8c7-667">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="4f8c7-668">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="4f8c7-668">Parameters - top</span></span>

<span data-ttu-id="4f8c7-669">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-669">value</span></span>  

<!-- -->

<span data-ttu-id="4f8c7-670">モード</span><span class="sxs-lookup"><span data-stu-id="4f8c7-670">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="4f8c7-671">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="4f8c7-671">Return Value - top</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="4f8c7-672">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="4f8c7-672">Method topMargin</span></span>

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="4f8c7-673">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="4f8c7-673">Parameters - topMargin</span></span>

<span data-ttu-id="4f8c7-674">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-674">value</span></span>  

<!-- -->

<span data-ttu-id="4f8c7-675">モード</span><span class="sxs-lookup"><span data-stu-id="4f8c7-675">mode</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="4f8c7-676">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="4f8c7-676">Return Value - topMargin</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="4f8c7-677">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-677">Method topMarginMode</span></span>

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="4f8c7-678">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-678">Parameters - topMarginMode</span></span>

<span data-ttu-id="4f8c7-679">モード</span><span class="sxs-lookup"><span data-stu-id="4f8c7-679">mode</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="4f8c7-680">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-680">Return Value - topMarginMode</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="4f8c7-681">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-681">Method topMarginValue</span></span>

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="4f8c7-682">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-682">Parameters - topMarginValue</span></span>

<span data-ttu-id="4f8c7-683">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-683">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="4f8c7-684">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-684">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="4f8c7-685">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-685">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="4f8c7-686">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-686">Parameters - topMode</span></span>

<span data-ttu-id="4f8c7-687">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-687">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="4f8c7-688">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-688">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="4f8c7-689">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-689">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="4f8c7-690">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-690">Parameters - topValue</span></span>

<span data-ttu-id="4f8c7-691">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-691">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="4f8c7-692">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-692">Return Value - topValue</span></span>

## <a name="method-underline"></a><span data-ttu-id="4f8c7-693">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="4f8c7-693">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="4f8c7-694">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="4f8c7-694">Parameters - underline</span></span>

<span data-ttu-id="4f8c7-695">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-695">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="4f8c7-696">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="4f8c7-696">Return Value - underline</span></span>

## <a name="method-usecaptionfrommenuitem"></a><span data-ttu-id="4f8c7-697">メソッド useCaptionFromMenuItem</span><span class="sxs-lookup"><span data-stu-id="4f8c7-697">Method useCaptionFromMenuItem</span></span>

```xpp
public int useCaptionFromMenuItem([int value])
```

### <a name="parameters---usecaptionfrommenuitem"></a><span data-ttu-id="4f8c7-698">パラメーター - useCaptionFromMenuItem</span><span class="sxs-lookup"><span data-stu-id="4f8c7-698">Parameters - useCaptionFromMenuItem</span></span>

<span data-ttu-id="4f8c7-699">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-699">value</span></span>  

### <a name="return-value---usecaptionfrommenuitem"></a><span data-ttu-id="4f8c7-700">戻り値 - useCaptionFromMenuItem</span><span class="sxs-lookup"><span data-stu-id="4f8c7-700">Return Value - useCaptionFromMenuItem</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="4f8c7-701">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-701">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="4f8c7-702">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-702">Parameters - viewEditMode</span></span>

<span data-ttu-id="4f8c7-703">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-703">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="4f8c7-704">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-704">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="4f8c7-705">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="4f8c7-705">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="4f8c7-706">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="4f8c7-706">Parameters - visible</span></span>

<span data-ttu-id="4f8c7-707">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-707">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="4f8c7-708">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="4f8c7-708">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="4f8c7-709">メソッド width</span><span class="sxs-lookup"><span data-stu-id="4f8c7-709">Method width</span></span>

<span data-ttu-id="4f8c7-710">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-710">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="4f8c7-711">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="4f8c7-711">Parameters - width</span></span>

<span data-ttu-id="4f8c7-712">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-712">value</span></span>  

<!-- -->

<span data-ttu-id="4f8c7-713">モード</span><span class="sxs-lookup"><span data-stu-id="4f8c7-713">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="4f8c7-714">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="4f8c7-714">Return Value - width</span></span>

<span data-ttu-id="4f8c7-715">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-715">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="4f8c7-716">備考 - width</span><span class="sxs-lookup"><span data-stu-id="4f8c7-716">Remarks - width</span></span>

<span data-ttu-id="4f8c7-717">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-717">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="4f8c7-718">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="4f8c7-718">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="4f8c7-719">モード。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-719">Mode.</span></span>           | <span data-ttu-id="4f8c7-720">幅計算。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-720">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f8c7-721">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-721">-1 Exact.</span></span>       | <span data-ttu-id="4f8c7-722">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-722">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="4f8c7-723">0 自動。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-723">0 Auto.</span></span>         | <span data-ttu-id="4f8c7-724">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-724">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="4f8c7-725">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-725">1 Column width.</span></span> | <span data-ttu-id="4f8c7-726">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-726">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="4f8c7-727">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-727">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="4f8c7-728">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-728">Method widthMode</span></span>

<span data-ttu-id="4f8c7-729">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-729">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="4f8c7-730">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-730">Parameters - widthMode</span></span>

<span data-ttu-id="4f8c7-731">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-731">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="4f8c7-732">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-732">Return Value - widthMode</span></span>

<span data-ttu-id="4f8c7-733">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-733">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="4f8c7-734">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="4f8c7-734">Remarks - widthMode</span></span>

<span data-ttu-id="4f8c7-735">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="4f8c7-735">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="4f8c7-736">モード。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-736">Mode.</span></span>         | <span data-ttu-id="4f8c7-737">幅計算。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-737">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f8c7-738">正確。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-738">Exact.</span></span>        | <span data-ttu-id="4f8c7-739">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-739">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="4f8c7-740">自動。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-740">Auto.</span></span>         | <span data-ttu-id="4f8c7-741">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-741">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="4f8c7-742">列の幅。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-742">Column width.</span></span> | <span data-ttu-id="4f8c7-743">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-743">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="4f8c7-744">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-744">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="4f8c7-745">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-745">Method widthValue</span></span>

<span data-ttu-id="4f8c7-746">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-746">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="4f8c7-747">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-747">Parameters - widthValue</span></span>

<span data-ttu-id="4f8c7-748">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-748">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="4f8c7-749">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-749">Return Value - widthValue</span></span>

<span data-ttu-id="4f8c7-750">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-750">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="4f8c7-751">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="4f8c7-751">Remarks - widthValue</span></span>

<span data-ttu-id="4f8c7-752">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="4f8c7-752">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-windowresize"></a><span data-ttu-id="4f8c7-753">メソッド windowResize</span><span class="sxs-lookup"><span data-stu-id="4f8c7-753">Method windowResize</span></span>

```xpp
public int windowResize([int value])
```

### <a name="parameters---windowresize"></a><span data-ttu-id="4f8c7-754">パラメーター - windowResize</span><span class="sxs-lookup"><span data-stu-id="4f8c7-754">Parameters - windowResize</span></span>

<span data-ttu-id="4f8c7-755">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-755">value</span></span>  

### <a name="return-value---windowresize"></a><span data-ttu-id="4f8c7-756">戻り値 - windowResize</span><span class="sxs-lookup"><span data-stu-id="4f8c7-756">Return Value - windowResize</span></span>

## <a name="method-windowtype"></a><span data-ttu-id="4f8c7-757">メソッド windowType</span><span class="sxs-lookup"><span data-stu-id="4f8c7-757">Method windowType</span></span>

```xpp
public int windowType([int value])
```

### <a name="parameters---windowtype"></a><span data-ttu-id="4f8c7-758">パラメーター - windowType</span><span class="sxs-lookup"><span data-stu-id="4f8c7-758">Parameters - windowType</span></span>

<span data-ttu-id="4f8c7-759">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-759">value</span></span>  

### <a name="return-value---windowtype"></a><span data-ttu-id="4f8c7-760">戻り値 - windowType</span><span class="sxs-lookup"><span data-stu-id="4f8c7-760">Return Value - windowType</span></span>

## <a name="method-workflowdatasource"></a><span data-ttu-id="4f8c7-761">メソッド workflowDatasource</span><span class="sxs-lookup"><span data-stu-id="4f8c7-761">Method workflowDatasource</span></span>

```xpp
public int workflowDatasource([AnyType value])
```

### <a name="parameters---workflowdatasource"></a><span data-ttu-id="4f8c7-762">パラメーター - workflowDatasource</span><span class="sxs-lookup"><span data-stu-id="4f8c7-762">Parameters - workflowDatasource</span></span>

<span data-ttu-id="4f8c7-763">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-763">value</span></span>  

### <a name="return-value---workflowdatasource"></a><span data-ttu-id="4f8c7-764">戻り値 - workflowDatasource</span><span class="sxs-lookup"><span data-stu-id="4f8c7-764">Return Value - workflowDatasource</span></span>

## <a name="method-workflowenabled"></a><span data-ttu-id="4f8c7-765">メソッド workflowEnabled</span><span class="sxs-lookup"><span data-stu-id="4f8c7-765">Method workflowEnabled</span></span>

```xpp
public boolean workflowEnabled([boolean value])
```

### <a name="parameters---workflowenabled"></a><span data-ttu-id="4f8c7-766">パラメーター - workflowEnabled</span><span class="sxs-lookup"><span data-stu-id="4f8c7-766">Parameters - workflowEnabled</span></span>

<span data-ttu-id="4f8c7-767">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-767">value</span></span>  

### <a name="return-value---workflowenabled"></a><span data-ttu-id="4f8c7-768">戻り値 - workflowEnabled</span><span class="sxs-lookup"><span data-stu-id="4f8c7-768">Return Value - workflowEnabled</span></span>

## <a name="method-workflowtype"></a><span data-ttu-id="4f8c7-769">メソッド workflowType</span><span class="sxs-lookup"><span data-stu-id="4f8c7-769">Method workflowType</span></span>

```xpp
public str workflowType([str value])
```

### <a name="parameters---workflowtype"></a><span data-ttu-id="4f8c7-770">パラメーター - workflowType</span><span class="sxs-lookup"><span data-stu-id="4f8c7-770">Parameters - workflowType</span></span>

<span data-ttu-id="4f8c7-771">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-771">value</span></span>  

### <a name="return-value---workflowtype"></a><span data-ttu-id="4f8c7-772">戻り値 - workflowType</span><span class="sxs-lookup"><span data-stu-id="4f8c7-772">Return Value - workflowType</span></span>

## <a name="method-dialogsize"></a><span data-ttu-id="4f8c7-773">メソッド dialogSize</span><span class="sxs-lookup"><span data-stu-id="4f8c7-773">Method dialogSize</span></span>

```xpp
public int dialogSize([int value])
```

### <a name="parameters---dialogsize"></a><span data-ttu-id="4f8c7-774">パラメーター - dialogSize</span><span class="sxs-lookup"><span data-stu-id="4f8c7-774">Parameters - dialogSize</span></span>

<span data-ttu-id="4f8c7-775">値</span><span class="sxs-lookup"><span data-stu-id="4f8c7-775">value</span></span>  

### <a name="return-value---dialogsize"></a><span data-ttu-id="4f8c7-776">戻り値 - dialogSize</span><span class="sxs-lookup"><span data-stu-id="4f8c7-776">Return Value - dialogSize</span></span>

