---
title: FormDesign クラス
description: このトピックでは、FormDesign クラスについて説明します。
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
ms.openlocfilehash: c44b5ec0bf54e72042b6fd6d790c16096ca17019
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502628"
---
# <a name="class-formdesign"></a><span data-ttu-id="b0c63-103">クラス FormDesign</span><span class="sxs-lookup"><span data-stu-id="b0c63-103">Class FormDesign</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormDesign extends Object
```

## <a name="remarks"></a><span data-ttu-id="b0c63-104">備考</span><span class="sxs-lookup"><span data-stu-id="b0c63-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="b0c63-105">例</span><span class="sxs-lookup"><span data-stu-id="b0c63-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="b0c63-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="b0c63-106">Methods</span></span>

| <span data-ttu-id="b0c63-107">方法</span><span class="sxs-lookup"><span data-stu-id="b0c63-107">Method</span></span>                                                                                                              | <span data-ttu-id="b0c63-108">説明</span><span class="sxs-lookup"><span data-stu-id="b0c63-108">Description</span></span>                                                         |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="b0c63-109">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-109">public FormControl addControl(FormControlType controlType, str controlName, \[FormControl insertAfter\])</span></span>            |                                                                     |
| <span data-ttu-id="b0c63-110">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-110">public FormControl addControlEx(str controlClass, str controlName, \[FormControl insertAfter\])</span></span>                     |                                                                     |
| <span data-ttu-id="b0c63-111">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-111">public FormControl addDataField(int dataSourceId, FieldId fieldId, \[FormControl insertAfter\], \[int arrayIndex\])</span></span> |                                                                     |
| <span data-ttu-id="b0c63-112">public boolean alignChild(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-112">public boolean alignChild(\[boolean value\])</span></span>                                                                        |                                                                     |
| <span data-ttu-id="b0c63-113">public boolean alignChildren(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-113">public boolean alignChildren(\[boolean value\])</span></span>                                                                     |                                                                     |
| <span data-ttu-id="b0c63-114">public boolean allowDocking(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-114">public boolean allowDocking(\[boolean value\])</span></span>                                                                      |                                                                     |
| <span data-ttu-id="b0c63-115">public boolean allowFormCompanyChange(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-115">public boolean allowFormCompanyChange(\[boolean value\])</span></span>                                                            |                                                                     |
| <span data-ttu-id="b0c63-116">public boolean allowImplicitParent(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-116">public boolean allowImplicitParent(\[boolean value\])</span></span>                                                               |                                                                     |
| <span data-ttu-id="b0c63-117">public int allowUserSetup(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-117">public int allowUserSetup(\[int value\])</span></span>                                                                            |                                                                     |
| <span data-ttu-id="b0c63-118">public boolean alwaysOnTop(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-118">public boolean alwaysOnTop(\[boolean value\])</span></span>                                                                       |                                                                     |
| <span data-ttu-id="b0c63-119">public int arrangeGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-119">public int arrangeGuide(\[int value\])</span></span>                                                                              |                                                                     |
| <span data-ttu-id="b0c63-120">public int arrangeMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-120">public int arrangeMethod(\[int value\])</span></span>                                                                             |                                                                     |
| <span data-ttu-id="b0c63-121">public int arrangeWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-121">public int arrangeWhen(\[int value\])</span></span>                                                                               |                                                                     |
| <span data-ttu-id="b0c63-122">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-122">public int backgroundColor(\[int value\])</span></span>                                                                           | <span data-ttu-id="b0c63-123">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-123">Gets or sets the background color of the control.</span></span>                   |
| <span data-ttu-id="b0c63-124">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-124">public int bold(\[int value\])</span></span>                                                                                      | <span data-ttu-id="b0c63-125">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-125">Gets or sets the weight of font used to output text in the control.</span></span> |
| <span data-ttu-id="b0c63-126">public int bottomMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-126">public int bottomMargin(\[int value\], \[AutoMode mode\])</span></span>                                                           |                                                                     |
| <span data-ttu-id="b0c63-127">public AutoMode bottomMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-127">public AutoMode bottomMarginMode(\[AutoMode mode\])</span></span>                                                                 |                                                                     |
| <span data-ttu-id="b0c63-128">public int bottomMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-128">public int bottomMarginValue(\[int value\])</span></span>                                                                         |                                                                     |
| <span data-ttu-id="b0c63-129">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-129">public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])</span></span>                               |                                                                     |
| <span data-ttu-id="b0c63-130">public boolean canContain(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="b0c63-130">public boolean canContain(FormControl control)</span></span>                                                                      |                                                                     |
| <span data-ttu-id="b0c63-131">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-131">public str caption(\[str value\])</span></span>                                                                                   | <span data-ttu-id="b0c63-132">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-132">Gets or set the caption of the control.</span></span>                             |
| <span data-ttu-id="b0c63-133">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-133">public int characterSet(\[int value\])</span></span>                                                                              | <span data-ttu-id="b0c63-134">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-134">Gets or sets the character set of the font.</span></span>                         |
| <span data-ttu-id="b0c63-135">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-135">public int colorScheme(\[int value\])</span></span>                                                                               | <span data-ttu-id="b0c63-136">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-136">Gets or sets the color scheme of the control.</span></span>                       |
| <span data-ttu-id="b0c63-137">public int columns(\[int value\], \[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-137">public int columns(\[int value\], \[ColumnsMode mode\])</span></span>                                                             |                                                                     |
| <span data-ttu-id="b0c63-138">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-138">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span></span>                                                                |                                                                     |
| <span data-ttu-id="b0c63-139">public int columnspace(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-139">public int columnspace(\[int value\], \[AutoMode mode\])</span></span>                                                            |                                                                     |
| <span data-ttu-id="b0c63-140">public AutoMode columnspaceMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-140">public AutoMode columnspaceMode(\[AutoMode mode\])</span></span>                                                                  |                                                                     |
| <span data-ttu-id="b0c63-141">public int columnspaceValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-141">public int columnspaceValue(\[int value\])</span></span>                                                                          |                                                                     |
| <span data-ttu-id="b0c63-142">public int columnsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-142">public int columnsValue(\[int value\])</span></span>                                                                              |                                                                     |
| <span data-ttu-id="b0c63-143">public boolean contains(FormControl control)</span><span class="sxs-lookup"><span data-stu-id="b0c63-143">public boolean contains(FormControl control)</span></span>                                                                        |                                                                     |
| <span data-ttu-id="b0c63-144">public FormControl control(int controlId)</span><span class="sxs-lookup"><span data-stu-id="b0c63-144">public FormControl control(int controlId)</span></span>                                                                           |                                                                     |
| <span data-ttu-id="b0c63-145">public int controlCount()</span><span class="sxs-lookup"><span data-stu-id="b0c63-145">public int controlCount()</span></span>                                                                                           |                                                                     |
| <span data-ttu-id="b0c63-146">public FormControl controlName(str controlName)</span><span class="sxs-lookup"><span data-stu-id="b0c63-146">public FormControl controlName(str controlName)</span></span>                                                                     |                                                                     |
| <span data-ttu-id="b0c63-147">public FormControl controlNum(int controlNo)</span><span class="sxs-lookup"><span data-stu-id="b0c63-147">public FormControl controlNum(int controlNo)</span></span>                                                                        |                                                                     |
| <span data-ttu-id="b0c63-148">public str cssClass(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-148">public str cssClass(\[str value\])</span></span>                                                                                  |                                                                     |
| <span data-ttu-id="b0c63-149">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-149">public int dataSource(\[AnyType value\])</span></span>                                                                            | <span data-ttu-id="b0c63-150">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-150">Gets or sets a data source to be used by the control or the form.</span></span>   |
| <span data-ttu-id="b0c63-151">public str defaultAction(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-151">public str defaultAction(\[str value\])</span></span>                                                                             |                                                                     |
| <span data-ttu-id="b0c63-152">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-152">public str font(\[str value\])</span></span>                                                                                      | <span data-ttu-id="b0c63-153">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-153">Gets or sets the name of the font for the control to use.</span></span>           |
| <span data-ttu-id="b0c63-154">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-154">public int fontSize(\[int value\])</span></span>                                                                                  | <span data-ttu-id="b0c63-155">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-155">Gets or sets the size of the font for the control to use.</span></span>           |
| <span data-ttu-id="b0c63-156">public int frame(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-156">public int frame(\[int value\])</span></span>                                                                                     |                                                                     |
| <span data-ttu-id="b0c63-157">public boolean hasUserSetting()</span><span class="sxs-lookup"><span data-stu-id="b0c63-157">public boolean hasUserSetting()</span></span>                                                                                     |                                                                     |
| <span data-ttu-id="b0c63-158">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-158">public int height(int value, \[int mode\])</span></span>                                                                          | <span data-ttu-id="b0c63-159">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-159">Gets or sets the height of the control.</span></span>                             |
| <span data-ttu-id="b0c63-160">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-160">public int heightMode(\[int value\])</span></span>                                                                                | <span data-ttu-id="b0c63-161">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-161">Gets or sets a calculation mode for the height of the control.</span></span>      |
| <span data-ttu-id="b0c63-162">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-162">public int heightValue(\[int value\])</span></span>                                                                               | <span data-ttu-id="b0c63-163">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-163">Gets or sets the height of the control.</span></span>                             |
| <span data-ttu-id="b0c63-164">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-164">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                                       |                                                                     |
| <span data-ttu-id="b0c63-165">public boolean hideToolbar(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-165">public boolean hideToolbar(\[boolean value\])</span></span>                                                                       |                                                                     |
| <span data-ttu-id="b0c63-166">public int imagemode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-166">public int imagemode(\[int value\])</span></span>                                                                                 |                                                                     |
| <span data-ttu-id="b0c63-167">public str imageName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-167">public str imageName(\[str value\])</span></span>                                                                                 |                                                                     |
| <span data-ttu-id="b0c63-168">public int imageResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-168">public int imageResource(\[int value\])</span></span>                                                                             |                                                                     |
| <span data-ttu-id="b0c63-169">public boolean isUserSetupEnabled(int neededSetupRights)</span><span class="sxs-lookup"><span data-stu-id="b0c63-169">public boolean isUserSetupEnabled(int neededSetupRights)</span></span>                                                            |                                                                     |
| <span data-ttu-id="b0c63-170">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-170">public boolean italic(\[boolean value\])</span></span>                                                                            |                                                                     |
| <span data-ttu-id="b0c63-171">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-171">public int labelBold(\[int value\])</span></span>                                                                                 |                                                                     |
| <span data-ttu-id="b0c63-172">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-172">public int labelCharacterSet(\[int value\])</span></span>                                                                         |                                                                     |
| <span data-ttu-id="b0c63-173">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-173">public str labelFont(\[str value\])</span></span>                                                                                 |                                                                     |
| <span data-ttu-id="b0c63-174">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-174">public int labelFontSize(\[int value\])</span></span>                                                                             |                                                                     |
| <span data-ttu-id="b0c63-175">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-175">public boolean labelItalic(\[boolean value\])</span></span>                                                                       |                                                                     |
| <span data-ttu-id="b0c63-176">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-176">public boolean labelUnderline(\[boolean value\])</span></span>                                                                    |                                                                     |
| <span data-ttu-id="b0c63-177">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-177">public int left(int value, \[int mode\])</span></span>                                                                            |                                                                     |
| <span data-ttu-id="b0c63-178">public int leftMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-178">public int leftMargin(\[int value\], \[AutoMode mode\])</span></span>                                                             |                                                                     |
| <span data-ttu-id="b0c63-179">public AutoMode leftMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-179">public AutoMode leftMarginMode(\[AutoMode mode\])</span></span>                                                                   |                                                                     |
| <span data-ttu-id="b0c63-180">public int leftMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-180">public int leftMarginValue(\[int value\])</span></span>                                                                           |                                                                     |
| <span data-ttu-id="b0c63-181">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-181">public int leftMode(\[int value\])</span></span>                                                                                  |                                                                     |
| <span data-ttu-id="b0c63-182">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-182">public int leftValue(\[int value\])</span></span>                                                                                 |                                                                     |
| <span data-ttu-id="b0c63-183">public str localWebMenu(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-183">public str localWebMenu(\[str value\])</span></span>                                                                              |                                                                     |
| <span data-ttu-id="b0c63-184">public boolean maximizeBox(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-184">public boolean maximizeBox(\[boolean value\])</span></span>                                                                       |                                                                     |
| <span data-ttu-id="b0c63-185">public boolean minimizeBox(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-185">public boolean minimizeBox(\[boolean value\])</span></span>                                                                       |                                                                     |
| <span data-ttu-id="b0c63-186">public int mode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-186">public int mode(\[int value\])</span></span>                                                                                      |                                                                     |
| <span data-ttu-id="b0c63-187">public int moveControl(int controlId, \[int insertAfterControlId\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-187">public int moveControl(int controlId, \[int insertAfterControlId\])</span></span>                                                 |                                                                     |
| <span data-ttu-id="b0c63-188">public str newRecordAction(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-188">public str newRecordAction(\[str value\])</span></span>                                                                           |                                                                     |
| <span data-ttu-id="b0c63-189">public container SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="b0c63-189">public container SysObsoleteAttribute()</span></span>                                                                             |                                                                     |
| <span data-ttu-id="b0c63-190">public int rightMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-190">public int rightMargin(\[int value\], \[AutoMode mode\])</span></span>                                                            |                                                                     |
| <span data-ttu-id="b0c63-191">public AutoMode rightMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-191">public AutoMode rightMarginMode(\[AutoMode mode\])</span></span>                                                                  |                                                                     |
| <span data-ttu-id="b0c63-192">public int rightMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-192">public int rightMarginValue(\[int value\])</span></span>                                                                          |                                                                     |
| <span data-ttu-id="b0c63-193">public boolean saveSize(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-193">public boolean saveSize(\[boolean value\])</span></span>                                                                          |                                                                     |
| <span data-ttu-id="b0c63-194">public int scrollbars(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-194">public int scrollbars(\[int value\])</span></span>                                                                                |                                                                     |
| <span data-ttu-id="b0c63-195">public boolean setCompany(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-195">public boolean setCompany(\[boolean value\])</span></span>                                                                        |                                                                     |
| <span data-ttu-id="b0c63-196">public int showDeleteButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-196">public int showDeleteButton(\[int value\])</span></span>                                                                          |                                                                     |
| <span data-ttu-id="b0c63-197">public int showNewButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-197">public int showNewButton(\[int value\])</span></span>                                                                             |                                                                     |
| <span data-ttu-id="b0c63-198">public int showWebHelp(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-198">public int showWebHelp(\[int value\])</span></span>                                                                               |                                                                     |
| <span data-ttu-id="b0c63-199">public int statusBarStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-199">public int statusBarStyle(\[int value\])</span></span>                                                                            |                                                                     |
| <span data-ttu-id="b0c63-200">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-200">public int style(\[int value\])</span></span>                                                                                     |                                                                     |
| <span data-ttu-id="b0c63-201">public int submitMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-201">public int submitMethod(\[int value\])</span></span>                                                                              |                                                                     |
| <span data-ttu-id="b0c63-202">public boolean supportReload(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-202">public boolean supportReload(\[boolean value\])</span></span>                                                                     |                                                                     |
| <span data-ttu-id="b0c63-203">public int titleDatasource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-203">public int titleDatasource(\[AnyType value\])</span></span>                                                                       |                                                                     |
| <span data-ttu-id="b0c63-204">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-204">public int top(int value, \[int mode\])</span></span>                                                                             |                                                                     |
| <span data-ttu-id="b0c63-205">public int topMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-205">public int topMargin(\[int value\], \[AutoMode mode\])</span></span>                                                              |                                                                     |
| <span data-ttu-id="b0c63-206">public AutoMode topMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-206">public AutoMode topMarginMode(\[AutoMode mode\])</span></span>                                                                    |                                                                     |
| <span data-ttu-id="b0c63-207">public int topMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-207">public int topMarginValue(\[int value\])</span></span>                                                                            |                                                                     |
| <span data-ttu-id="b0c63-208">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-208">public int topMode(\[int value\])</span></span>                                                                                   |                                                                     |
| <span data-ttu-id="b0c63-209">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-209">public int topValue(\[int value\])</span></span>                                                                                  |                                                                     |
| <span data-ttu-id="b0c63-210">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-210">public boolean underline(\[boolean value\])</span></span>                                                                         |                                                                     |
| <span data-ttu-id="b0c63-211">public boolean SysObsoleteAttribute(container data)</span><span class="sxs-lookup"><span data-stu-id="b0c63-211">public boolean SysObsoleteAttribute(container data)</span></span>                                                                 |                                                                     |
| <span data-ttu-id="b0c63-212">public int useCaptionFromMenuItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-212">public int useCaptionFromMenuItem(\[int value\])</span></span>                                                                    |                                                                     |
| <span data-ttu-id="b0c63-213">public boolean userSettingAllowSave()</span><span class="sxs-lookup"><span data-stu-id="b0c63-213">public boolean userSettingAllowSave()</span></span>                                                                               |                                                                     |
| <span data-ttu-id="b0c63-214">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-214">public boolean useUserLayout(\[boolean value\])</span></span>                                                                     |                                                                     |
| <span data-ttu-id="b0c63-215">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-215">public int viewEditMode(\[int value\])</span></span>                                                                              |                                                                     |
| <span data-ttu-id="b0c63-216">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-216">public boolean visible(\[boolean value\])</span></span>                                                                           |                                                                     |
| <span data-ttu-id="b0c63-217">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-217">public int width(int value, \[int mode\])</span></span>                                                                           | <span data-ttu-id="b0c63-218">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-218">Gets or sets the width of the control.</span></span>                              |
| <span data-ttu-id="b0c63-219">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-219">public int widthMode(\[int value\])</span></span>                                                                                 | <span data-ttu-id="b0c63-220">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-220">Gets or sets the calculation mode of the width of the control.</span></span>      |
| <span data-ttu-id="b0c63-221">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-221">public int widthValue(\[int value\])</span></span>                                                                                | <span data-ttu-id="b0c63-222">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-222">Gets or sets the width of the control.</span></span>                              |
| <span data-ttu-id="b0c63-223">public int windowResize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-223">public int windowResize(\[int value\])</span></span>                                                                              |                                                                     |
| <span data-ttu-id="b0c63-224">public int windowType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-224">public int windowType(\[int value\])</span></span>                                                                                |                                                                     |
| <span data-ttu-id="b0c63-225">public int workflowDatasource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-225">public int workflowDatasource(\[AnyType value\])</span></span>                                                                    |                                                                     |
| <span data-ttu-id="b0c63-226">public boolean workflowEnabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-226">public boolean workflowEnabled(\[boolean value\])</span></span>                                                                   |                                                                     |
| <span data-ttu-id="b0c63-227">public str workflowType(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-227">public str workflowType(\[str value\])</span></span>                                                                              |                                                                     |
| <span data-ttu-id="b0c63-228">public int dialogSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-228">public int dialogSize(\[int value\])</span></span>                                                                                |                                                                     |
| <span data-ttu-id="b0c63-229">public void resetUserSetting()</span><span class="sxs-lookup"><span data-stu-id="b0c63-229">public void resetUserSetting()</span></span>                                                                                      |                                                                     |
| <span data-ttu-id="b0c63-230">public void removeControl(\[int controlId\])</span><span class="sxs-lookup"><span data-stu-id="b0c63-230">public void removeControl(\[int controlId\])</span></span>                                                                        |                                                                     |
| <span data-ttu-id="b0c63-231">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="b0c63-231">public void finalize()</span></span>                                                                                              |                                                                     |

## <a name="method-addcontrol"></a><span data-ttu-id="b0c63-232">メソッド addControl</span><span class="sxs-lookup"><span data-stu-id="b0c63-232">Method addControl</span></span>

```xpp
public FormControl addControl(FormControlType controlType, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrol"></a><span data-ttu-id="b0c63-233">パラメーター - addControl</span><span class="sxs-lookup"><span data-stu-id="b0c63-233">Parameters - addControl</span></span>

<span data-ttu-id="b0c63-234">controlType</span><span class="sxs-lookup"><span data-stu-id="b0c63-234">controlType</span></span>  

<!-- -->

<span data-ttu-id="b0c63-235">controlName</span><span class="sxs-lookup"><span data-stu-id="b0c63-235">controlName</span></span>  

<!-- -->

<span data-ttu-id="b0c63-236">insertAfter</span><span class="sxs-lookup"><span data-stu-id="b0c63-236">insertAfter</span></span>  

### <a name="return-value---addcontrol"></a><span data-ttu-id="b0c63-237">戻り値 - addControl</span><span class="sxs-lookup"><span data-stu-id="b0c63-237">Return Value - addControl</span></span>

## <a name="method-addcontrolex"></a><span data-ttu-id="b0c63-238">メソッド addControlEx</span><span class="sxs-lookup"><span data-stu-id="b0c63-238">Method addControlEx</span></span>

```xpp
public FormControl addControlEx(str controlClass, str controlName, [FormControl insertAfter])
```

### <a name="parameters---addcontrolex"></a><span data-ttu-id="b0c63-239">パラメーター - addControlEx</span><span class="sxs-lookup"><span data-stu-id="b0c63-239">Parameters - addControlEx</span></span>

<span data-ttu-id="b0c63-240">controlClass</span><span class="sxs-lookup"><span data-stu-id="b0c63-240">controlClass</span></span>  

<!-- -->

<span data-ttu-id="b0c63-241">controlName</span><span class="sxs-lookup"><span data-stu-id="b0c63-241">controlName</span></span>  

<!-- -->

<span data-ttu-id="b0c63-242">insertAfter</span><span class="sxs-lookup"><span data-stu-id="b0c63-242">insertAfter</span></span>  

### <a name="return-value---addcontrolex"></a><span data-ttu-id="b0c63-243">戻り値 - addControlEx</span><span class="sxs-lookup"><span data-stu-id="b0c63-243">Return Value - addControlEx</span></span>

## <a name="method-adddatafield"></a><span data-ttu-id="b0c63-244">メソッド addDataField</span><span class="sxs-lookup"><span data-stu-id="b0c63-244">Method addDataField</span></span>

```xpp
public FormControl addDataField(int dataSourceId, FieldId fieldId, [FormControl insertAfter], [int arrayIndex])
```

### <a name="parameters---adddatafield"></a><span data-ttu-id="b0c63-245">パラメーター - addDataField</span><span class="sxs-lookup"><span data-stu-id="b0c63-245">Parameters - addDataField</span></span>

<span data-ttu-id="b0c63-246">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="b0c63-246">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="b0c63-247">fieldId</span><span class="sxs-lookup"><span data-stu-id="b0c63-247">fieldId</span></span>  

<!-- -->

<span data-ttu-id="b0c63-248">insertAfter</span><span class="sxs-lookup"><span data-stu-id="b0c63-248">insertAfter</span></span>  

<!-- -->

<span data-ttu-id="b0c63-249">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="b0c63-249">arrayIndex</span></span>  

### <a name="return-value---adddatafield"></a><span data-ttu-id="b0c63-250">戻り値 - addDataField</span><span class="sxs-lookup"><span data-stu-id="b0c63-250">Return Value - addDataField</span></span>

## <a name="method-alignchild"></a><span data-ttu-id="b0c63-251">メソッド alignChild</span><span class="sxs-lookup"><span data-stu-id="b0c63-251">Method alignChild</span></span>

```xpp
public boolean alignChild([boolean value])
```

### <a name="parameters---alignchild"></a><span data-ttu-id="b0c63-252">パラメーター - alignChild</span><span class="sxs-lookup"><span data-stu-id="b0c63-252">Parameters - alignChild</span></span>

<span data-ttu-id="b0c63-253">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-253">value</span></span>  

### <a name="return-value---alignchild"></a><span data-ttu-id="b0c63-254">戻り値 - alignChild</span><span class="sxs-lookup"><span data-stu-id="b0c63-254">Return Value - alignChild</span></span>

## <a name="method-alignchildren"></a><span data-ttu-id="b0c63-255">メソッド alignChildren</span><span class="sxs-lookup"><span data-stu-id="b0c63-255">Method alignChildren</span></span>

```xpp
public boolean alignChildren([boolean value])
```

### <a name="parameters---alignchildren"></a><span data-ttu-id="b0c63-256">パラメーター - alignChildren</span><span class="sxs-lookup"><span data-stu-id="b0c63-256">Parameters - alignChildren</span></span>

<span data-ttu-id="b0c63-257">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-257">value</span></span>  

### <a name="return-value---alignchildren"></a><span data-ttu-id="b0c63-258">戻り値 - alignChildren</span><span class="sxs-lookup"><span data-stu-id="b0c63-258">Return Value - alignChildren</span></span>

## <a name="method-allowdocking"></a><span data-ttu-id="b0c63-259">メソッド allowDocking</span><span class="sxs-lookup"><span data-stu-id="b0c63-259">Method allowDocking</span></span>

```xpp
public boolean allowDocking([boolean value])
```

### <a name="parameters---allowdocking"></a><span data-ttu-id="b0c63-260">パラメーター - allowDocking</span><span class="sxs-lookup"><span data-stu-id="b0c63-260">Parameters - allowDocking</span></span>

<span data-ttu-id="b0c63-261">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-261">value</span></span>  

### <a name="return-value---allowdocking"></a><span data-ttu-id="b0c63-262">戻り値 - allowDocking</span><span class="sxs-lookup"><span data-stu-id="b0c63-262">Return Value - allowDocking</span></span>

## <a name="method-allowformcompanychange"></a><span data-ttu-id="b0c63-263">メソッド allowFormCompanyChange</span><span class="sxs-lookup"><span data-stu-id="b0c63-263">Method allowFormCompanyChange</span></span>

```xpp
public boolean allowFormCompanyChange([boolean value])
```

### <a name="parameters---allowformcompanychange"></a><span data-ttu-id="b0c63-264">パラメーター - allowFormCompanyChange</span><span class="sxs-lookup"><span data-stu-id="b0c63-264">Parameters - allowFormCompanyChange</span></span>

<span data-ttu-id="b0c63-265">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-265">value</span></span>  

### <a name="return-value---allowformcompanychange"></a><span data-ttu-id="b0c63-266">戻り値 - allowFormCompanyChange</span><span class="sxs-lookup"><span data-stu-id="b0c63-266">Return Value - allowFormCompanyChange</span></span>

## <a name="method-allowimplicitparent"></a><span data-ttu-id="b0c63-267">メソッド allowImplicitParent</span><span class="sxs-lookup"><span data-stu-id="b0c63-267">Method allowImplicitParent</span></span>

```xpp
public boolean allowImplicitParent([boolean value])
```

### <a name="parameters---allowimplicitparent"></a><span data-ttu-id="b0c63-268">パラメーター - allowImplicitParent</span><span class="sxs-lookup"><span data-stu-id="b0c63-268">Parameters - allowImplicitParent</span></span>

<span data-ttu-id="b0c63-269">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-269">value</span></span>  

### <a name="return-value---allowimplicitparent"></a><span data-ttu-id="b0c63-270">戻り値 - allowImplicitParent</span><span class="sxs-lookup"><span data-stu-id="b0c63-270">Return Value - allowImplicitParent</span></span>

## <a name="method-allowusersetup"></a><span data-ttu-id="b0c63-271">メソッド allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="b0c63-271">Method allowUserSetup</span></span>

```xpp
public int allowUserSetup([int value])
```

### <a name="parameters---allowusersetup"></a><span data-ttu-id="b0c63-272">パラメーター - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="b0c63-272">Parameters - allowUserSetup</span></span>

<span data-ttu-id="b0c63-273">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-273">value</span></span>  

### <a name="return-value---allowusersetup"></a><span data-ttu-id="b0c63-274">戻り値 - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="b0c63-274">Return Value - allowUserSetup</span></span>

## <a name="method-alwaysontop"></a><span data-ttu-id="b0c63-275">メソッド alwaysOnTop</span><span class="sxs-lookup"><span data-stu-id="b0c63-275">Method alwaysOnTop</span></span>

```xpp
public boolean alwaysOnTop([boolean value])
```

### <a name="parameters---alwaysontop"></a><span data-ttu-id="b0c63-276">パラメーター - alwaysOnTop</span><span class="sxs-lookup"><span data-stu-id="b0c63-276">Parameters - alwaysOnTop</span></span>

<span data-ttu-id="b0c63-277">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-277">value</span></span>  

### <a name="return-value---alwaysontop"></a><span data-ttu-id="b0c63-278">戻り値 - alwaysOnTop</span><span class="sxs-lookup"><span data-stu-id="b0c63-278">Return Value - alwaysOnTop</span></span>

## <a name="method-arrangeguide"></a><span data-ttu-id="b0c63-279">メソッド arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="b0c63-279">Method arrangeGuide</span></span>

```xpp
public int arrangeGuide([int value])
```

### <a name="parameters---arrangeguide"></a><span data-ttu-id="b0c63-280">パラメーター - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="b0c63-280">Parameters - arrangeGuide</span></span>

<span data-ttu-id="b0c63-281">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-281">value</span></span>  

### <a name="return-value---arrangeguide"></a><span data-ttu-id="b0c63-282">戻り値 - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="b0c63-282">Return Value - arrangeGuide</span></span>

## <a name="method-arrangemethod"></a><span data-ttu-id="b0c63-283">メソッド arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="b0c63-283">Method arrangeMethod</span></span>

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a><span data-ttu-id="b0c63-284">パラメーター - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="b0c63-284">Parameters - arrangeMethod</span></span>

<span data-ttu-id="b0c63-285">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-285">value</span></span>  

### <a name="return-value---arrangemethod"></a><span data-ttu-id="b0c63-286">戻り値 - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="b0c63-286">Return Value - arrangeMethod</span></span>

## <a name="method-arrangewhen"></a><span data-ttu-id="b0c63-287">メソッド arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="b0c63-287">Method arrangeWhen</span></span>

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a><span data-ttu-id="b0c63-288">パラメーター - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="b0c63-288">Parameters - arrangeWhen</span></span>

<span data-ttu-id="b0c63-289">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-289">value</span></span>  

### <a name="return-value---arrangewhen"></a><span data-ttu-id="b0c63-290">戻り値 - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="b0c63-290">Return Value - arrangeWhen</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="b0c63-291">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="b0c63-291">Method backgroundColor</span></span>

<span data-ttu-id="b0c63-292">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-292">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="b0c63-293">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="b0c63-293">Parameters - backgroundColor</span></span>

<span data-ttu-id="b0c63-294">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-294">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="b0c63-295">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="b0c63-295">Return Value - backgroundColor</span></span>

<span data-ttu-id="b0c63-296">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="b0c63-296">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="b0c63-297">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="b0c63-297">Remarks - backgroundColor</span></span>

<span data-ttu-id="b0c63-298">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b0c63-298">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="b0c63-299">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b0c63-299">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="b0c63-300">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="b0c63-300">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="b0c63-301">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="b0c63-301">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="b0c63-302">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="b0c63-302">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="b0c63-303">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="b0c63-303">The maximum value for a single byte is 255.</span></span>

## <a name="method-bold"></a><span data-ttu-id="b0c63-304">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="b0c63-304">Method bold</span></span>

<span data-ttu-id="b0c63-305">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-305">Gets or sets the weight of font used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="b0c63-306">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="b0c63-306">Parameters - bold</span></span>

<span data-ttu-id="b0c63-307">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-307">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="b0c63-308">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="b0c63-308">Return Value - bold</span></span>

<span data-ttu-id="b0c63-309">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="b0c63-309">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="b0c63-310">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="b0c63-310">Remarks - bold</span></span>

<span data-ttu-id="b0c63-311">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b0c63-311">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="b0c63-312">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-312">0 Use the default font weight.</span></span>
-   <span data-ttu-id="b0c63-313">1 シン。</span><span class="sxs-lookup"><span data-stu-id="b0c63-313">1 Thin.</span></span>
-   <span data-ttu-id="b0c63-314">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="b0c63-314">2 Extra-light.</span></span>
-   <span data-ttu-id="b0c63-315">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="b0c63-315">3 Light.</span></span>
-   <span data-ttu-id="b0c63-316">4 標準。</span><span class="sxs-lookup"><span data-stu-id="b0c63-316">4 Normal.</span></span>
-   <span data-ttu-id="b0c63-317">5 中。</span><span class="sxs-lookup"><span data-stu-id="b0c63-317">5 Medium.</span></span>
-   <span data-ttu-id="b0c63-318">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="b0c63-318">6 Semibold.</span></span>
-   <span data-ttu-id="b0c63-319">7 太字。</span><span class="sxs-lookup"><span data-stu-id="b0c63-319">7 Bold.</span></span>
-   <span data-ttu-id="b0c63-320">8 極太。</span><span class="sxs-lookup"><span data-stu-id="b0c63-320">8 Extra-bold.</span></span>
-   <span data-ttu-id="b0c63-321">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="b0c63-321">9 Heavy.</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="b0c63-322">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="b0c63-322">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="b0c63-323">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="b0c63-323">Parameters - bottomMargin</span></span>

<span data-ttu-id="b0c63-324">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-324">value</span></span>  

<!-- -->

<span data-ttu-id="b0c63-325">モード</span><span class="sxs-lookup"><span data-stu-id="b0c63-325">mode</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="b0c63-326">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="b0c63-326">Return Value - bottomMargin</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="b0c63-327">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-327">Method bottomMarginMode</span></span>

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="b0c63-328">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-328">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="b0c63-329">モード</span><span class="sxs-lookup"><span data-stu-id="b0c63-329">mode</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="b0c63-330">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-330">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="b0c63-331">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-331">Method bottomMarginValue</span></span>

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="b0c63-332">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-332">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="b0c63-333">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-333">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="b0c63-334">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-334">Return Value - bottomMarginValue</span></span>

## <a name="method-canadddatafield"></a><span data-ttu-id="b0c63-335">メソッド canAddDataField</span><span class="sxs-lookup"><span data-stu-id="b0c63-335">Method canAddDataField</span></span>

```xpp
public boolean canAddDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---canadddatafield"></a><span data-ttu-id="b0c63-336">パラメーター - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="b0c63-336">Parameters - canAddDataField</span></span>

<span data-ttu-id="b0c63-337">dataSourceId</span><span class="sxs-lookup"><span data-stu-id="b0c63-337">dataSourceId</span></span>  

<!-- -->

<span data-ttu-id="b0c63-338">fieldId</span><span class="sxs-lookup"><span data-stu-id="b0c63-338">fieldId</span></span>  

<!-- -->

<span data-ttu-id="b0c63-339">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="b0c63-339">arrayIndex</span></span>  

### <a name="return-value---canadddatafield"></a><span data-ttu-id="b0c63-340">戻り値 - canAddDataField</span><span class="sxs-lookup"><span data-stu-id="b0c63-340">Return Value - canAddDataField</span></span>

## <a name="method-cancontain"></a><span data-ttu-id="b0c63-341">メソッド canContain</span><span class="sxs-lookup"><span data-stu-id="b0c63-341">Method canContain</span></span>

```xpp
public boolean canContain(FormControl control)
```

### <a name="parameters---cancontain"></a><span data-ttu-id="b0c63-342">パラメーター - canContain</span><span class="sxs-lookup"><span data-stu-id="b0c63-342">Parameters - canContain</span></span>

<span data-ttu-id="b0c63-343">control</span><span class="sxs-lookup"><span data-stu-id="b0c63-343">control</span></span>  

### <a name="return-value---cancontain"></a><span data-ttu-id="b0c63-344">戻り値 - canContain</span><span class="sxs-lookup"><span data-stu-id="b0c63-344">Return Value - canContain</span></span>

## <a name="method-caption"></a><span data-ttu-id="b0c63-345">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="b0c63-345">Method caption</span></span>

<span data-ttu-id="b0c63-346">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-346">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="b0c63-347">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="b0c63-347">Parameters - caption</span></span>

<span data-ttu-id="b0c63-348">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-348">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="b0c63-349">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="b0c63-349">Return Value - caption</span></span>

<span data-ttu-id="b0c63-350">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="b0c63-350">The string that is used as the caption of the control.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="b0c63-351">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="b0c63-351">Method characterSet</span></span>

<span data-ttu-id="b0c63-352">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-352">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="b0c63-353">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="b0c63-353">Parameters - characterSet</span></span>

<span data-ttu-id="b0c63-354">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-354">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="b0c63-355">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="b0c63-355">Return Value - characterSet</span></span>

<span data-ttu-id="b0c63-356">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b0c63-356">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="b0c63-357">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="b0c63-357">Remarks - characterSet</span></span>

<span data-ttu-id="b0c63-358">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-358">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="b0c63-359">値です。</span><span class="sxs-lookup"><span data-stu-id="b0c63-359">Value.</span></span> | <span data-ttu-id="b0c63-360">説明。</span><span class="sxs-lookup"><span data-stu-id="b0c63-360">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="b0c63-361">0</span><span class="sxs-lookup"><span data-stu-id="b0c63-361">0</span></span>      | <span data-ttu-id="b0c63-362">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b0c63-362">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="b0c63-363">1</span><span class="sxs-lookup"><span data-stu-id="b0c63-363">1</span></span>      | <span data-ttu-id="b0c63-364">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b0c63-364">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="b0c63-365">2</span><span class="sxs-lookup"><span data-stu-id="b0c63-365">2</span></span>      | <span data-ttu-id="b0c63-366">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b0c63-366">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="b0c63-367">77</span><span class="sxs-lookup"><span data-stu-id="b0c63-367">77</span></span>     | <span data-ttu-id="b0c63-368">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b0c63-368">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="b0c63-369">128</span><span class="sxs-lookup"><span data-stu-id="b0c63-369">128</span></span>    | <span data-ttu-id="b0c63-370">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b0c63-370">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="b0c63-371">129</span><span class="sxs-lookup"><span data-stu-id="b0c63-371">129</span></span>    | <span data-ttu-id="b0c63-372">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b0c63-372">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="b0c63-373">134</span><span class="sxs-lookup"><span data-stu-id="b0c63-373">134</span></span>    | <span data-ttu-id="b0c63-374">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b0c63-374">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="b0c63-375">136</span><span class="sxs-lookup"><span data-stu-id="b0c63-375">136</span></span>    | <span data-ttu-id="b0c63-376">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b0c63-376">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="b0c63-377">161</span><span class="sxs-lookup"><span data-stu-id="b0c63-377">161</span></span>    | <span data-ttu-id="b0c63-378">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b0c63-378">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="b0c63-379">162</span><span class="sxs-lookup"><span data-stu-id="b0c63-379">162</span></span>    | <span data-ttu-id="b0c63-380">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b0c63-380">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="b0c63-381">163</span><span class="sxs-lookup"><span data-stu-id="b0c63-381">163</span></span>    | <span data-ttu-id="b0c63-382">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b0c63-382">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="b0c63-383">186</span><span class="sxs-lookup"><span data-stu-id="b0c63-383">186</span></span>    | <span data-ttu-id="b0c63-384">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b0c63-384">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="b0c63-385">204</span><span class="sxs-lookup"><span data-stu-id="b0c63-385">204</span></span>    | <span data-ttu-id="b0c63-386">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b0c63-386">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="b0c63-387">238</span><span class="sxs-lookup"><span data-stu-id="b0c63-387">238</span></span>    | <span data-ttu-id="b0c63-388">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b0c63-388">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="b0c63-389">255</span><span class="sxs-lookup"><span data-stu-id="b0c63-389">255</span></span>    | <span data-ttu-id="b0c63-390">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b0c63-390">OEM\_CHARSET</span></span>         |

<span data-ttu-id="b0c63-391">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="b0c63-391">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="b0c63-392">値です。</span><span class="sxs-lookup"><span data-stu-id="b0c63-392">Value.</span></span> | <span data-ttu-id="b0c63-393">説明。</span><span class="sxs-lookup"><span data-stu-id="b0c63-393">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="b0c63-394">130</span><span class="sxs-lookup"><span data-stu-id="b0c63-394">130</span></span>    | <span data-ttu-id="b0c63-395">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b0c63-395">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="b0c63-396">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="b0c63-396">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="b0c63-397">値です。</span><span class="sxs-lookup"><span data-stu-id="b0c63-397">Value.</span></span> | <span data-ttu-id="b0c63-398">説明。</span><span class="sxs-lookup"><span data-stu-id="b0c63-398">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="b0c63-399">177</span><span class="sxs-lookup"><span data-stu-id="b0c63-399">177</span></span>    | <span data-ttu-id="b0c63-400">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b0c63-400">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="b0c63-401">178</span><span class="sxs-lookup"><span data-stu-id="b0c63-401">178</span></span>    | <span data-ttu-id="b0c63-402">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b0c63-402">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="b0c63-403">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="b0c63-403">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="b0c63-404">値です。</span><span class="sxs-lookup"><span data-stu-id="b0c63-404">Value.</span></span> | <span data-ttu-id="b0c63-405">説明。</span><span class="sxs-lookup"><span data-stu-id="b0c63-405">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="b0c63-406">222</span><span class="sxs-lookup"><span data-stu-id="b0c63-406">222</span></span>    | <span data-ttu-id="b0c63-407">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="b0c63-407">THAI\_CHARSET</span></span> |

<span data-ttu-id="b0c63-408">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="b0c63-408">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="b0c63-409">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="b0c63-409">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="b0c63-410">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0c63-410">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="b0c63-411">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="b0c63-411">Method colorScheme</span></span>

<span data-ttu-id="b0c63-412">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-412">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="b0c63-413">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="b0c63-413">Parameters - colorScheme</span></span>

<span data-ttu-id="b0c63-414">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-414">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="b0c63-415">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="b0c63-415">Return Value - colorScheme</span></span>

<span data-ttu-id="b0c63-416">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="b0c63-416">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="b0c63-417">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="b0c63-417">Remarks - colorScheme</span></span>

<span data-ttu-id="b0c63-418">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="b0c63-418">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="b0c63-419">値です。</span><span class="sxs-lookup"><span data-stu-id="b0c63-419">Value.</span></span> | <span data-ttu-id="b0c63-420">スタイル。</span><span class="sxs-lookup"><span data-stu-id="b0c63-420">Style.</span></span>                         |
|--------|--------------------------------|
| <span data-ttu-id="b0c63-421">0</span><span class="sxs-lookup"><span data-stu-id="b0c63-421">0</span></span>      | <span data-ttu-id="b0c63-422">既定。</span><span class="sxs-lookup"><span data-stu-id="b0c63-422">Default.</span></span>                       |
| <span data-ttu-id="b0c63-423">1</span><span class="sxs-lookup"><span data-stu-id="b0c63-423">1</span></span>      | <span data-ttu-id="b0c63-424">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="b0c63-424">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="b0c63-425">2</span><span class="sxs-lookup"><span data-stu-id="b0c63-425">2</span></span>      | <span data-ttu-id="b0c63-426">真の配色。</span><span class="sxs-lookup"><span data-stu-id="b0c63-426">The true-color scheme.</span></span>         |

## <a name="method-columns"></a><span data-ttu-id="b0c63-427">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="b0c63-427">Method columns</span></span>

```xpp
public int columns([int value], [ColumnsMode mode])
```

### <a name="parameters---columns"></a><span data-ttu-id="b0c63-428">パラメーター - columns</span><span class="sxs-lookup"><span data-stu-id="b0c63-428">Parameters - columns</span></span>

<span data-ttu-id="b0c63-429">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-429">value</span></span>  

<!-- -->

<span data-ttu-id="b0c63-430">モード</span><span class="sxs-lookup"><span data-stu-id="b0c63-430">mode</span></span>  

### <a name="return-value---columns"></a><span data-ttu-id="b0c63-431">戻り値 - columns</span><span class="sxs-lookup"><span data-stu-id="b0c63-431">Return Value - columns</span></span>

## <a name="method-columnsmode"></a><span data-ttu-id="b0c63-432">メソッド columnsMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-432">Method columnsMode</span></span>

```xpp
public ColumnsMode columnsMode([ColumnsMode mode])
```

### <a name="parameters---columnsmode"></a><span data-ttu-id="b0c63-433">パラメーター - columnsMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-433">Parameters - columnsMode</span></span>

<span data-ttu-id="b0c63-434">モード</span><span class="sxs-lookup"><span data-stu-id="b0c63-434">mode</span></span>  

### <a name="return-value---columnsmode"></a><span data-ttu-id="b0c63-435">戻り値 - columnsMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-435">Return Value - columnsMode</span></span>

## <a name="method-columnspace"></a><span data-ttu-id="b0c63-436">メソッド columnspace</span><span class="sxs-lookup"><span data-stu-id="b0c63-436">Method columnspace</span></span>

```xpp
public int columnspace([int value], [AutoMode mode])
```

### <a name="parameters---columnspace"></a><span data-ttu-id="b0c63-437">パラメーター - columnspace</span><span class="sxs-lookup"><span data-stu-id="b0c63-437">Parameters - columnspace</span></span>

<span data-ttu-id="b0c63-438">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-438">value</span></span>  

<!-- -->

<span data-ttu-id="b0c63-439">モード</span><span class="sxs-lookup"><span data-stu-id="b0c63-439">mode</span></span>  

### <a name="return-value---columnspace"></a><span data-ttu-id="b0c63-440">戻り値 - columnspace</span><span class="sxs-lookup"><span data-stu-id="b0c63-440">Return Value - columnspace</span></span>

## <a name="method-columnspacemode"></a><span data-ttu-id="b0c63-441">メソッド columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-441">Method columnspaceMode</span></span>

```xpp
public AutoMode columnspaceMode([AutoMode mode])
```

### <a name="parameters---columnspacemode"></a><span data-ttu-id="b0c63-442">パラメーター - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-442">Parameters - columnspaceMode</span></span>

<span data-ttu-id="b0c63-443">モード</span><span class="sxs-lookup"><span data-stu-id="b0c63-443">mode</span></span>  

### <a name="return-value---columnspacemode"></a><span data-ttu-id="b0c63-444">戻り値 - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-444">Return Value - columnspaceMode</span></span>

## <a name="method-columnspacevalue"></a><span data-ttu-id="b0c63-445">メソッド columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-445">Method columnspaceValue</span></span>

```xpp
public int columnspaceValue([int value])
```

### <a name="parameters---columnspacevalue"></a><span data-ttu-id="b0c63-446">パラメーター - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-446">Parameters - columnspaceValue</span></span>

<span data-ttu-id="b0c63-447">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-447">value</span></span>  

### <a name="return-value---columnspacevalue"></a><span data-ttu-id="b0c63-448">戻り値 - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-448">Return Value - columnspaceValue</span></span>

## <a name="method-columnsvalue"></a><span data-ttu-id="b0c63-449">メソッド columnsValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-449">Method columnsValue</span></span>

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a><span data-ttu-id="b0c63-450">パラメーター - columnsValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-450">Parameters - columnsValue</span></span>

<span data-ttu-id="b0c63-451">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-451">value</span></span>  

### <a name="return-value---columnsvalue"></a><span data-ttu-id="b0c63-452">戻り値 - columnsValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-452">Return Value - columnsValue</span></span>

## <a name="method-contains"></a><span data-ttu-id="b0c63-453">メソッド contains</span><span class="sxs-lookup"><span data-stu-id="b0c63-453">Method contains</span></span>

```xpp
public boolean contains(FormControl control)
```

### <a name="parameters---contains"></a><span data-ttu-id="b0c63-454">パラメーター - contains</span><span class="sxs-lookup"><span data-stu-id="b0c63-454">Parameters - contains</span></span>

<span data-ttu-id="b0c63-455">control</span><span class="sxs-lookup"><span data-stu-id="b0c63-455">control</span></span>  

### <a name="return-value---contains"></a><span data-ttu-id="b0c63-456">戻り値 - contains</span><span class="sxs-lookup"><span data-stu-id="b0c63-456">Return Value - contains</span></span>

## <a name="method-control"></a><span data-ttu-id="b0c63-457">メソッド control</span><span class="sxs-lookup"><span data-stu-id="b0c63-457">Method control</span></span>

```xpp
public FormControl control(int controlId)
```

### <a name="parameters---control"></a><span data-ttu-id="b0c63-458">パラメーター - control</span><span class="sxs-lookup"><span data-stu-id="b0c63-458">Parameters - control</span></span>

<span data-ttu-id="b0c63-459">controlId</span><span class="sxs-lookup"><span data-stu-id="b0c63-459">controlId</span></span>  

### <a name="return-value---control"></a><span data-ttu-id="b0c63-460">戻り値 - control</span><span class="sxs-lookup"><span data-stu-id="b0c63-460">Return Value - control</span></span>

## <a name="method-controlcount"></a><span data-ttu-id="b0c63-461">メソッド controlCount</span><span class="sxs-lookup"><span data-stu-id="b0c63-461">Method controlCount</span></span>

```xpp
public int controlCount()
```

### <a name="return-value---controlcount"></a><span data-ttu-id="b0c63-462">戻り値 - controlCount</span><span class="sxs-lookup"><span data-stu-id="b0c63-462">Return Value - controlCount</span></span>

## <a name="method-controlname"></a><span data-ttu-id="b0c63-463">メソッド controlName</span><span class="sxs-lookup"><span data-stu-id="b0c63-463">Method controlName</span></span>

```xpp
public FormControl controlName(str controlName)
```

### <a name="parameters---controlname"></a><span data-ttu-id="b0c63-464">パラメーター - controlName</span><span class="sxs-lookup"><span data-stu-id="b0c63-464">Parameters - controlName</span></span>

<span data-ttu-id="b0c63-465">controlName</span><span class="sxs-lookup"><span data-stu-id="b0c63-465">controlName</span></span>  

### <a name="return-value---controlname"></a><span data-ttu-id="b0c63-466">戻り値 - controlName</span><span class="sxs-lookup"><span data-stu-id="b0c63-466">Return Value - controlName</span></span>

## <a name="method-controlnum"></a><span data-ttu-id="b0c63-467">メソッド controlNum</span><span class="sxs-lookup"><span data-stu-id="b0c63-467">Method controlNum</span></span>

```xpp
public FormControl controlNum(int controlNo)
```

### <a name="parameters---controlnum"></a><span data-ttu-id="b0c63-468">パラメーター - controlNum</span><span class="sxs-lookup"><span data-stu-id="b0c63-468">Parameters - controlNum</span></span>

<span data-ttu-id="b0c63-469">controlNo</span><span class="sxs-lookup"><span data-stu-id="b0c63-469">controlNo</span></span>  

### <a name="return-value---controlnum"></a><span data-ttu-id="b0c63-470">戻り値 - controlNum</span><span class="sxs-lookup"><span data-stu-id="b0c63-470">Return Value - controlNum</span></span>

## <a name="method-cssclass"></a><span data-ttu-id="b0c63-471">メソッド cssClass</span><span class="sxs-lookup"><span data-stu-id="b0c63-471">Method cssClass</span></span>

```xpp
public str cssClass([str value])
```

### <a name="parameters---cssclass"></a><span data-ttu-id="b0c63-472">パラメーター - cssClass</span><span class="sxs-lookup"><span data-stu-id="b0c63-472">Parameters - cssClass</span></span>

<span data-ttu-id="b0c63-473">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-473">value</span></span>  

### <a name="return-value---cssclass"></a><span data-ttu-id="b0c63-474">戻り値 - cssClass</span><span class="sxs-lookup"><span data-stu-id="b0c63-474">Return Value - cssClass</span></span>

## <a name="method-datasource"></a><span data-ttu-id="b0c63-475">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="b0c63-475">Method dataSource</span></span>

<span data-ttu-id="b0c63-476">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-476">Gets or sets a data source to be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="b0c63-477">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="b0c63-477">Parameters - dataSource</span></span>

<span data-ttu-id="b0c63-478">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-478">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="b0c63-479">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="b0c63-479">Return Value - dataSource</span></span>

<span data-ttu-id="b0c63-480">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="b0c63-480">The identifier of the data source to be used.</span></span>

## <a name="method-defaultaction"></a><span data-ttu-id="b0c63-481">メソッド defaultAction</span><span class="sxs-lookup"><span data-stu-id="b0c63-481">Method defaultAction</span></span>

```xpp
public str defaultAction([str value])
```

### <a name="parameters---defaultaction"></a><span data-ttu-id="b0c63-482">パラメーター - defaultAction</span><span class="sxs-lookup"><span data-stu-id="b0c63-482">Parameters - defaultAction</span></span>

<span data-ttu-id="b0c63-483">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-483">value</span></span>  

### <a name="return-value---defaultaction"></a><span data-ttu-id="b0c63-484">戻り値 - defaultAction</span><span class="sxs-lookup"><span data-stu-id="b0c63-484">Return Value - defaultAction</span></span>

## <a name="method-font"></a><span data-ttu-id="b0c63-485">メソッド font</span><span class="sxs-lookup"><span data-stu-id="b0c63-485">Method font</span></span>

<span data-ttu-id="b0c63-486">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-486">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="b0c63-487">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="b0c63-487">Parameters - font</span></span>

<span data-ttu-id="b0c63-488">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-488">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="b0c63-489">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="b0c63-489">Return Value - font</span></span>

<span data-ttu-id="b0c63-490">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="b0c63-490">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="b0c63-491">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="b0c63-491">Method fontSize</span></span>

<span data-ttu-id="b0c63-492">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-492">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="b0c63-493">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="b0c63-493">Parameters - fontSize</span></span>

<span data-ttu-id="b0c63-494">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-494">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="b0c63-495">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="b0c63-495">Return Value - fontSize</span></span>

<span data-ttu-id="b0c63-496">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="b0c63-496">The height of the font in points.</span></span>

## <a name="method-frame"></a><span data-ttu-id="b0c63-497">メソッド frame</span><span class="sxs-lookup"><span data-stu-id="b0c63-497">Method frame</span></span>

```xpp
public int frame([int value])
```

### <a name="parameters---frame"></a><span data-ttu-id="b0c63-498">パラメーター - frame</span><span class="sxs-lookup"><span data-stu-id="b0c63-498">Parameters - frame</span></span>

<span data-ttu-id="b0c63-499">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-499">value</span></span>  

### <a name="return-value---frame"></a><span data-ttu-id="b0c63-500">戻り値 - frame</span><span class="sxs-lookup"><span data-stu-id="b0c63-500">Return Value - frame</span></span>

## <a name="method-hasusersetting"></a><span data-ttu-id="b0c63-501">メソッド hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="b0c63-501">Method hasUserSetting</span></span>

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a><span data-ttu-id="b0c63-502">戻り値 - hasUserSetting</span><span class="sxs-lookup"><span data-stu-id="b0c63-502">Return Value - hasUserSetting</span></span>

## <a name="method-height"></a><span data-ttu-id="b0c63-503">メソッド height</span><span class="sxs-lookup"><span data-stu-id="b0c63-503">Method height</span></span>

<span data-ttu-id="b0c63-504">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-504">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="b0c63-505">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="b0c63-505">Parameters - height</span></span>

<span data-ttu-id="b0c63-506">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-506">value</span></span>  

<!-- -->

<span data-ttu-id="b0c63-507">モード</span><span class="sxs-lookup"><span data-stu-id="b0c63-507">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="b0c63-508">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="b0c63-508">Return Value - height</span></span>

<span data-ttu-id="b0c63-509">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="b0c63-509">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="b0c63-510">備考 - height</span><span class="sxs-lookup"><span data-stu-id="b0c63-510">Remarks - height</span></span>

<span data-ttu-id="b0c63-511">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0c63-511">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="b0c63-512">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="b0c63-512">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="b0c63-513">モード。</span><span class="sxs-lookup"><span data-stu-id="b0c63-513">Mode.</span></span>            | <span data-ttu-id="b0c63-514">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="b0c63-514">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0c63-515">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="b0c63-515">-1 Exact.</span></span>        | <span data-ttu-id="b0c63-516">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0c63-516">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b0c63-517">0 自動。</span><span class="sxs-lookup"><span data-stu-id="b0c63-517">0 Auto.</span></span>          | <span data-ttu-id="b0c63-518">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b0c63-518">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b0c63-519">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="b0c63-519">1 Column height.</span></span> | <span data-ttu-id="b0c63-520">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="b0c63-520">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="b0c63-521">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="b0c63-521">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="b0c63-522">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-522">Method heightMode</span></span>

<span data-ttu-id="b0c63-523">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-523">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="b0c63-524">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-524">Parameters - heightMode</span></span>

<span data-ttu-id="b0c63-525">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-525">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="b0c63-526">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-526">Return Value - heightMode</span></span>

<span data-ttu-id="b0c63-527">計算モード。</span><span class="sxs-lookup"><span data-stu-id="b0c63-527">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="b0c63-528">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-528">Remarks - heightMode</span></span>

<span data-ttu-id="b0c63-529">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="b0c63-529">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="b0c63-530">モード。</span><span class="sxs-lookup"><span data-stu-id="b0c63-530">Mode.</span></span>          | <span data-ttu-id="b0c63-531">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="b0c63-531">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0c63-532">正確。</span><span class="sxs-lookup"><span data-stu-id="b0c63-532">Exact.</span></span>         | <span data-ttu-id="b0c63-533">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0c63-533">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b0c63-534">自動。</span><span class="sxs-lookup"><span data-stu-id="b0c63-534">Auto.</span></span>          | <span data-ttu-id="b0c63-535">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b0c63-535">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b0c63-536">列の高さ</span><span class="sxs-lookup"><span data-stu-id="b0c63-536">Column height.</span></span> | <span data-ttu-id="b0c63-537">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="b0c63-537">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="b0c63-538">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="b0c63-538">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="b0c63-539">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-539">Method heightValue</span></span>

<span data-ttu-id="b0c63-540">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-540">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="b0c63-541">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-541">Parameters - heightValue</span></span>

<span data-ttu-id="b0c63-542">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-542">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="b0c63-543">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-543">Return Value - heightValue</span></span>

<span data-ttu-id="b0c63-544">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="b0c63-544">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="b0c63-545">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-545">Remarks - heightValue</span></span>

<span data-ttu-id="b0c63-546">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="b0c63-546">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-hideifempty"></a><span data-ttu-id="b0c63-547">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="b0c63-547">Method hideIfEmpty</span></span>

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a><span data-ttu-id="b0c63-548">パラメーター - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="b0c63-548">Parameters - hideIfEmpty</span></span>

<span data-ttu-id="b0c63-549">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-549">value</span></span>  

### <a name="return-value---hideifempty"></a><span data-ttu-id="b0c63-550">戻り値 - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="b0c63-550">Return Value - hideIfEmpty</span></span>

## <a name="method-hidetoolbar"></a><span data-ttu-id="b0c63-551">メソッド hideToolbar</span><span class="sxs-lookup"><span data-stu-id="b0c63-551">Method hideToolbar</span></span>

```xpp
public boolean hideToolbar([boolean value])
```

### <a name="parameters---hidetoolbar"></a><span data-ttu-id="b0c63-552">パラメーター - hideToolbar</span><span class="sxs-lookup"><span data-stu-id="b0c63-552">Parameters - hideToolbar</span></span>

<span data-ttu-id="b0c63-553">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-553">value</span></span>  

### <a name="return-value---hidetoolbar"></a><span data-ttu-id="b0c63-554">戻り値 - hideToolbar</span><span class="sxs-lookup"><span data-stu-id="b0c63-554">Return Value - hideToolbar</span></span>

## <a name="method-imagemode"></a><span data-ttu-id="b0c63-555">メソッド imagemode</span><span class="sxs-lookup"><span data-stu-id="b0c63-555">Method imagemode</span></span>

```xpp
public int imagemode([int value])
```

### <a name="parameters---imagemode"></a><span data-ttu-id="b0c63-556">パラメーター - imagemode</span><span class="sxs-lookup"><span data-stu-id="b0c63-556">Parameters - imagemode</span></span>

<span data-ttu-id="b0c63-557">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-557">value</span></span>  

### <a name="return-value---imagemode"></a><span data-ttu-id="b0c63-558">戻り値 - imagemode</span><span class="sxs-lookup"><span data-stu-id="b0c63-558">Return Value - imagemode</span></span>

## <a name="method-imagename"></a><span data-ttu-id="b0c63-559">メソッド imageName</span><span class="sxs-lookup"><span data-stu-id="b0c63-559">Method imageName</span></span>

```xpp
public str imageName([str value])
```

### <a name="parameters---imagename"></a><span data-ttu-id="b0c63-560">パラメーター - imageName</span><span class="sxs-lookup"><span data-stu-id="b0c63-560">Parameters - imageName</span></span>

<span data-ttu-id="b0c63-561">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-561">value</span></span>  

### <a name="return-value---imagename"></a><span data-ttu-id="b0c63-562">戻り値 - imageName</span><span class="sxs-lookup"><span data-stu-id="b0c63-562">Return Value - imageName</span></span>

## <a name="method-imageresource"></a><span data-ttu-id="b0c63-563">メソッド imageResource</span><span class="sxs-lookup"><span data-stu-id="b0c63-563">Method imageResource</span></span>

```xpp
public int imageResource([int value])
```

### <a name="parameters---imageresource"></a><span data-ttu-id="b0c63-564">パラメーター - imageResource</span><span class="sxs-lookup"><span data-stu-id="b0c63-564">Parameters - imageResource</span></span>

<span data-ttu-id="b0c63-565">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-565">value</span></span>  

### <a name="return-value---imageresource"></a><span data-ttu-id="b0c63-566">戻り値 - imageResource</span><span class="sxs-lookup"><span data-stu-id="b0c63-566">Return Value - imageResource</span></span>

## <a name="method-isusersetupenabled"></a><span data-ttu-id="b0c63-567">メソッド isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="b0c63-567">Method isUserSetupEnabled</span></span>

```xpp
public boolean isUserSetupEnabled(int neededSetupRights)
```

### <a name="parameters---isusersetupenabled"></a><span data-ttu-id="b0c63-568">パラメーター - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="b0c63-568">Parameters - isUserSetupEnabled</span></span>

<span data-ttu-id="b0c63-569">neededSetupRights</span><span class="sxs-lookup"><span data-stu-id="b0c63-569">neededSetupRights</span></span>  

### <a name="return-value---isusersetupenabled"></a><span data-ttu-id="b0c63-570">戻り値 - isUserSetupEnabled</span><span class="sxs-lookup"><span data-stu-id="b0c63-570">Return Value - isUserSetupEnabled</span></span>

## <a name="method-italic"></a><span data-ttu-id="b0c63-571">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="b0c63-571">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="b0c63-572">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="b0c63-572">Parameters - italic</span></span>

<span data-ttu-id="b0c63-573">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-573">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="b0c63-574">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="b0c63-574">Return Value - italic</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="b0c63-575">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="b0c63-575">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="b0c63-576">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="b0c63-576">Parameters - labelBold</span></span>

<span data-ttu-id="b0c63-577">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-577">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="b0c63-578">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="b0c63-578">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="b0c63-579">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="b0c63-579">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="b0c63-580">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="b0c63-580">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="b0c63-581">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-581">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="b0c63-582">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="b0c63-582">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="b0c63-583">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="b0c63-583">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="b0c63-584">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="b0c63-584">Parameters - labelFont</span></span>

<span data-ttu-id="b0c63-585">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-585">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="b0c63-586">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="b0c63-586">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="b0c63-587">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="b0c63-587">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="b0c63-588">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="b0c63-588">Parameters - labelFontSize</span></span>

<span data-ttu-id="b0c63-589">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-589">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="b0c63-590">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="b0c63-590">Return Value - labelFontSize</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="b0c63-591">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="b0c63-591">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="b0c63-592">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="b0c63-592">Parameters - labelItalic</span></span>

<span data-ttu-id="b0c63-593">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-593">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="b0c63-594">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="b0c63-594">Return Value - labelItalic</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="b0c63-595">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="b0c63-595">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="b0c63-596">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="b0c63-596">Parameters - labelUnderline</span></span>

<span data-ttu-id="b0c63-597">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-597">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="b0c63-598">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="b0c63-598">Return Value - labelUnderline</span></span>

## <a name="method-left"></a><span data-ttu-id="b0c63-599">メソッド left</span><span class="sxs-lookup"><span data-stu-id="b0c63-599">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="b0c63-600">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="b0c63-600">Parameters - left</span></span>

<span data-ttu-id="b0c63-601">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-601">value</span></span>  

<!-- -->

<span data-ttu-id="b0c63-602">モード</span><span class="sxs-lookup"><span data-stu-id="b0c63-602">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="b0c63-603">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="b0c63-603">Return Value - left</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="b0c63-604">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="b0c63-604">Method leftMargin</span></span>

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="b0c63-605">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="b0c63-605">Parameters - leftMargin</span></span>

<span data-ttu-id="b0c63-606">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-606">value</span></span>  

<!-- -->

<span data-ttu-id="b0c63-607">モード</span><span class="sxs-lookup"><span data-stu-id="b0c63-607">mode</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="b0c63-608">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="b0c63-608">Return Value - leftMargin</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="b0c63-609">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-609">Method leftMarginMode</span></span>

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="b0c63-610">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-610">Parameters - leftMarginMode</span></span>

<span data-ttu-id="b0c63-611">モード</span><span class="sxs-lookup"><span data-stu-id="b0c63-611">mode</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="b0c63-612">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-612">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="b0c63-613">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-613">Method leftMarginValue</span></span>

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="b0c63-614">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-614">Parameters - leftMarginValue</span></span>

<span data-ttu-id="b0c63-615">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-615">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="b0c63-616">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-616">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="b0c63-617">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-617">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="b0c63-618">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-618">Parameters - leftMode</span></span>

<span data-ttu-id="b0c63-619">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-619">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="b0c63-620">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-620">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="b0c63-621">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-621">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="b0c63-622">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-622">Parameters - leftValue</span></span>

<span data-ttu-id="b0c63-623">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-623">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="b0c63-624">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-624">Return Value - leftValue</span></span>

## <a name="method-localwebmenu"></a><span data-ttu-id="b0c63-625">メソッド localWebMenu</span><span class="sxs-lookup"><span data-stu-id="b0c63-625">Method localWebMenu</span></span>

```xpp
public str localWebMenu([str value])
```

### <a name="parameters---localwebmenu"></a><span data-ttu-id="b0c63-626">パラメーター - localWebMenu</span><span class="sxs-lookup"><span data-stu-id="b0c63-626">Parameters - localWebMenu</span></span>

<span data-ttu-id="b0c63-627">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-627">value</span></span>  

### <a name="return-value---localwebmenu"></a><span data-ttu-id="b0c63-628">戻り値 - localWebMenu</span><span class="sxs-lookup"><span data-stu-id="b0c63-628">Return Value - localWebMenu</span></span>

## <a name="method-maximizebox"></a><span data-ttu-id="b0c63-629">メソッド maximizeBox</span><span class="sxs-lookup"><span data-stu-id="b0c63-629">Method maximizeBox</span></span>

```xpp
public boolean maximizeBox([boolean value])
```

### <a name="parameters---maximizebox"></a><span data-ttu-id="b0c63-630">パラメーター - maximizeBox</span><span class="sxs-lookup"><span data-stu-id="b0c63-630">Parameters - maximizeBox</span></span>

<span data-ttu-id="b0c63-631">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-631">value</span></span>  

### <a name="return-value---maximizebox"></a><span data-ttu-id="b0c63-632">戻り値 - maximizeBox</span><span class="sxs-lookup"><span data-stu-id="b0c63-632">Return Value - maximizeBox</span></span>

## <a name="method-minimizebox"></a><span data-ttu-id="b0c63-633">メソッド minimizeBox</span><span class="sxs-lookup"><span data-stu-id="b0c63-633">Method minimizeBox</span></span>

```xpp
public boolean minimizeBox([boolean value])
```

### <a name="parameters---minimizebox"></a><span data-ttu-id="b0c63-634">パラメーター - minimizeBox</span><span class="sxs-lookup"><span data-stu-id="b0c63-634">Parameters - minimizeBox</span></span>

<span data-ttu-id="b0c63-635">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-635">value</span></span>  

### <a name="return-value---minimizebox"></a><span data-ttu-id="b0c63-636">戻り値 - minimizeBox</span><span class="sxs-lookup"><span data-stu-id="b0c63-636">Return Value - minimizeBox</span></span>

## <a name="method-mode"></a><span data-ttu-id="b0c63-637">メソッド mode</span><span class="sxs-lookup"><span data-stu-id="b0c63-637">Method mode</span></span>

```xpp
public int mode([int value])
```

### <a name="parameters---mode"></a><span data-ttu-id="b0c63-638">パラメーター - mode</span><span class="sxs-lookup"><span data-stu-id="b0c63-638">Parameters - mode</span></span>

<span data-ttu-id="b0c63-639">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-639">value</span></span>  

### <a name="return-value---mode"></a><span data-ttu-id="b0c63-640">戻り値 - mode</span><span class="sxs-lookup"><span data-stu-id="b0c63-640">Return Value - mode</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="b0c63-641">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="b0c63-641">Method moveControl</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterControlId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="b0c63-642">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="b0c63-642">Parameters - moveControl</span></span>

<span data-ttu-id="b0c63-643">controlId</span><span class="sxs-lookup"><span data-stu-id="b0c63-643">controlId</span></span>  

<!-- -->

<span data-ttu-id="b0c63-644">insertAfterControlId</span><span class="sxs-lookup"><span data-stu-id="b0c63-644">insertAfterControlId</span></span>  

### <a name="return-value---movecontrol"></a><span data-ttu-id="b0c63-645">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="b0c63-645">Return Value - moveControl</span></span>

## <a name="method-newrecordaction"></a><span data-ttu-id="b0c63-646">メソッド newRecordAction</span><span class="sxs-lookup"><span data-stu-id="b0c63-646">Method newRecordAction</span></span>

```xpp
public str newRecordAction([str value])
```

### <a name="parameters---newrecordaction"></a><span data-ttu-id="b0c63-647">パラメーター - newRecordAction</span><span class="sxs-lookup"><span data-stu-id="b0c63-647">Parameters - newRecordAction</span></span>

<span data-ttu-id="b0c63-648">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-648">value</span></span>  

### <a name="return-value---newrecordaction"></a><span data-ttu-id="b0c63-649">戻り値 - newRecordAction</span><span class="sxs-lookup"><span data-stu-id="b0c63-649">Return Value - newRecordAction</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="b0c63-650">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="b0c63-650">Method SysObsoleteAttribute</span></span>

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="b0c63-651">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="b0c63-651">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="b0c63-652">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="b0c63-652">Method rightMargin</span></span>

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="b0c63-653">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="b0c63-653">Parameters - rightMargin</span></span>

<span data-ttu-id="b0c63-654">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-654">value</span></span>  

<!-- -->

<span data-ttu-id="b0c63-655">モード</span><span class="sxs-lookup"><span data-stu-id="b0c63-655">mode</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="b0c63-656">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="b0c63-656">Return Value - rightMargin</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="b0c63-657">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-657">Method rightMarginMode</span></span>

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="b0c63-658">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-658">Parameters - rightMarginMode</span></span>

<span data-ttu-id="b0c63-659">モード</span><span class="sxs-lookup"><span data-stu-id="b0c63-659">mode</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="b0c63-660">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-660">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="b0c63-661">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-661">Method rightMarginValue</span></span>

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="b0c63-662">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-662">Parameters - rightMarginValue</span></span>

<span data-ttu-id="b0c63-663">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-663">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="b0c63-664">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-664">Return Value - rightMarginValue</span></span>

## <a name="method-savesize"></a><span data-ttu-id="b0c63-665">メソッド saveSize</span><span class="sxs-lookup"><span data-stu-id="b0c63-665">Method saveSize</span></span>

```xpp
public boolean saveSize([boolean value])
```

### <a name="parameters---savesize"></a><span data-ttu-id="b0c63-666">パラメーター - saveSize</span><span class="sxs-lookup"><span data-stu-id="b0c63-666">Parameters - saveSize</span></span>

<span data-ttu-id="b0c63-667">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-667">value</span></span>  

### <a name="return-value---savesize"></a><span data-ttu-id="b0c63-668">戻り値 - saveSize</span><span class="sxs-lookup"><span data-stu-id="b0c63-668">Return Value - saveSize</span></span>

## <a name="method-scrollbars"></a><span data-ttu-id="b0c63-669">メソッド scrollbars</span><span class="sxs-lookup"><span data-stu-id="b0c63-669">Method scrollbars</span></span>

```xpp
public int scrollbars([int value])
```

### <a name="parameters---scrollbars"></a><span data-ttu-id="b0c63-670">パラメーター - scrollbars</span><span class="sxs-lookup"><span data-stu-id="b0c63-670">Parameters - scrollbars</span></span>

<span data-ttu-id="b0c63-671">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-671">value</span></span>  

### <a name="return-value---scrollbars"></a><span data-ttu-id="b0c63-672">戻り値 - scrollbars</span><span class="sxs-lookup"><span data-stu-id="b0c63-672">Return Value - scrollbars</span></span>

## <a name="method-setcompany"></a><span data-ttu-id="b0c63-673">メソッド setCompany</span><span class="sxs-lookup"><span data-stu-id="b0c63-673">Method setCompany</span></span>

```xpp
public boolean setCompany([boolean value])
```

### <a name="parameters---setcompany"></a><span data-ttu-id="b0c63-674">パラメーター - setCompany</span><span class="sxs-lookup"><span data-stu-id="b0c63-674">Parameters - setCompany</span></span>

<span data-ttu-id="b0c63-675">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-675">value</span></span>  

### <a name="return-value---setcompany"></a><span data-ttu-id="b0c63-676">戻り値 - setCompany</span><span class="sxs-lookup"><span data-stu-id="b0c63-676">Return Value - setCompany</span></span>

## <a name="method-showdeletebutton"></a><span data-ttu-id="b0c63-677">メソッド showDeleteButton</span><span class="sxs-lookup"><span data-stu-id="b0c63-677">Method showDeleteButton</span></span>

```xpp
public int showDeleteButton([int value])
```

### <a name="parameters---showdeletebutton"></a><span data-ttu-id="b0c63-678">パラメーター - showDeleteButton</span><span class="sxs-lookup"><span data-stu-id="b0c63-678">Parameters - showDeleteButton</span></span>

<span data-ttu-id="b0c63-679">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-679">value</span></span>  

### <a name="return-value---showdeletebutton"></a><span data-ttu-id="b0c63-680">戻り値 - showDeleteButton</span><span class="sxs-lookup"><span data-stu-id="b0c63-680">Return Value - showDeleteButton</span></span>

## <a name="method-shownewbutton"></a><span data-ttu-id="b0c63-681">メソッド showNewButton</span><span class="sxs-lookup"><span data-stu-id="b0c63-681">Method showNewButton</span></span>

```xpp
public int showNewButton([int value])
```

### <a name="parameters---shownewbutton"></a><span data-ttu-id="b0c63-682">パラメーター - showNewButton</span><span class="sxs-lookup"><span data-stu-id="b0c63-682">Parameters - showNewButton</span></span>

<span data-ttu-id="b0c63-683">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-683">value</span></span>  

### <a name="return-value---shownewbutton"></a><span data-ttu-id="b0c63-684">戻り値 - showNewButton</span><span class="sxs-lookup"><span data-stu-id="b0c63-684">Return Value - showNewButton</span></span>

## <a name="method-showwebhelp"></a><span data-ttu-id="b0c63-685">メソッド showWebHelp</span><span class="sxs-lookup"><span data-stu-id="b0c63-685">Method showWebHelp</span></span>

```xpp
public int showWebHelp([int value])
```

### <a name="parameters---showwebhelp"></a><span data-ttu-id="b0c63-686">パラメーター - showWebHelp</span><span class="sxs-lookup"><span data-stu-id="b0c63-686">Parameters - showWebHelp</span></span>

<span data-ttu-id="b0c63-687">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-687">value</span></span>  

### <a name="return-value---showwebhelp"></a><span data-ttu-id="b0c63-688">戻り値 - showWebHelp</span><span class="sxs-lookup"><span data-stu-id="b0c63-688">Return Value - showWebHelp</span></span>

## <a name="method-statusbarstyle"></a><span data-ttu-id="b0c63-689">メソッド statusBarStyle</span><span class="sxs-lookup"><span data-stu-id="b0c63-689">Method statusBarStyle</span></span>

```xpp
public int statusBarStyle([int value])
```

### <a name="parameters---statusbarstyle"></a><span data-ttu-id="b0c63-690">パラメーター - statusBarStyle</span><span class="sxs-lookup"><span data-stu-id="b0c63-690">Parameters - statusBarStyle</span></span>

<span data-ttu-id="b0c63-691">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-691">value</span></span>  

### <a name="return-value---statusbarstyle"></a><span data-ttu-id="b0c63-692">戻り値 - statusBarStyle</span><span class="sxs-lookup"><span data-stu-id="b0c63-692">Return Value - statusBarStyle</span></span>

## <a name="method-style"></a><span data-ttu-id="b0c63-693">メソッド style</span><span class="sxs-lookup"><span data-stu-id="b0c63-693">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="b0c63-694">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="b0c63-694">Parameters - style</span></span>

<span data-ttu-id="b0c63-695">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-695">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="b0c63-696">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="b0c63-696">Return Value - style</span></span>

## <a name="method-submitmethod"></a><span data-ttu-id="b0c63-697">メソッド submitMethod</span><span class="sxs-lookup"><span data-stu-id="b0c63-697">Method submitMethod</span></span>

```xpp
public int submitMethod([int value])
```

### <a name="parameters---submitmethod"></a><span data-ttu-id="b0c63-698">パラメーター - submitMethod</span><span class="sxs-lookup"><span data-stu-id="b0c63-698">Parameters - submitMethod</span></span>

<span data-ttu-id="b0c63-699">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-699">value</span></span>  

### <a name="return-value---submitmethod"></a><span data-ttu-id="b0c63-700">戻り値 - submitMethod</span><span class="sxs-lookup"><span data-stu-id="b0c63-700">Return Value - submitMethod</span></span>

## <a name="method-supportreload"></a><span data-ttu-id="b0c63-701">メソッド supportReload</span><span class="sxs-lookup"><span data-stu-id="b0c63-701">Method supportReload</span></span>

```xpp
public boolean supportReload([boolean value])
```

### <a name="parameters---supportreload"></a><span data-ttu-id="b0c63-702">パラメーター - supportReload</span><span class="sxs-lookup"><span data-stu-id="b0c63-702">Parameters - supportReload</span></span>

<span data-ttu-id="b0c63-703">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-703">value</span></span>  

### <a name="return-value---supportreload"></a><span data-ttu-id="b0c63-704">戻り値 - supportReload</span><span class="sxs-lookup"><span data-stu-id="b0c63-704">Return Value - supportReload</span></span>

## <a name="method-titledatasource"></a><span data-ttu-id="b0c63-705">メソッド titleDatasource</span><span class="sxs-lookup"><span data-stu-id="b0c63-705">Method titleDatasource</span></span>

```xpp
public int titleDatasource([AnyType value])
```

### <a name="parameters---titledatasource"></a><span data-ttu-id="b0c63-706">パラメーター - titleDatasource</span><span class="sxs-lookup"><span data-stu-id="b0c63-706">Parameters - titleDatasource</span></span>

<span data-ttu-id="b0c63-707">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-707">value</span></span>  

### <a name="return-value---titledatasource"></a><span data-ttu-id="b0c63-708">戻り値 - titleDatasource</span><span class="sxs-lookup"><span data-stu-id="b0c63-708">Return Value - titleDatasource</span></span>

## <a name="method-top"></a><span data-ttu-id="b0c63-709">メソッド top</span><span class="sxs-lookup"><span data-stu-id="b0c63-709">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="b0c63-710">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="b0c63-710">Parameters - top</span></span>

<span data-ttu-id="b0c63-711">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-711">value</span></span>  

<!-- -->

<span data-ttu-id="b0c63-712">モード</span><span class="sxs-lookup"><span data-stu-id="b0c63-712">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="b0c63-713">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="b0c63-713">Return Value - top</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="b0c63-714">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="b0c63-714">Method topMargin</span></span>

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="b0c63-715">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="b0c63-715">Parameters - topMargin</span></span>

<span data-ttu-id="b0c63-716">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-716">value</span></span>  

<!-- -->

<span data-ttu-id="b0c63-717">モード</span><span class="sxs-lookup"><span data-stu-id="b0c63-717">mode</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="b0c63-718">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="b0c63-718">Return Value - topMargin</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="b0c63-719">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-719">Method topMarginMode</span></span>

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="b0c63-720">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-720">Parameters - topMarginMode</span></span>

<span data-ttu-id="b0c63-721">モード</span><span class="sxs-lookup"><span data-stu-id="b0c63-721">mode</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="b0c63-722">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-722">Return Value - topMarginMode</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="b0c63-723">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-723">Method topMarginValue</span></span>

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="b0c63-724">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-724">Parameters - topMarginValue</span></span>

<span data-ttu-id="b0c63-725">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-725">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="b0c63-726">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-726">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="b0c63-727">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-727">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="b0c63-728">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-728">Parameters - topMode</span></span>

<span data-ttu-id="b0c63-729">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-729">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="b0c63-730">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-730">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="b0c63-731">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-731">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="b0c63-732">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-732">Parameters - topValue</span></span>

<span data-ttu-id="b0c63-733">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-733">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="b0c63-734">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-734">Return Value - topValue</span></span>

## <a name="method-underline"></a><span data-ttu-id="b0c63-735">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="b0c63-735">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="b0c63-736">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="b0c63-736">Parameters - underline</span></span>

<span data-ttu-id="b0c63-737">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-737">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="b0c63-738">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="b0c63-738">Return Value - underline</span></span>

## <a name="method-sysobsoleteattribute"></a><span data-ttu-id="b0c63-739">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="b0c63-739">Method SysObsoleteAttribute</span></span>

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a><span data-ttu-id="b0c63-740">パラメーター - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="b0c63-740">Parameters - SysObsoleteAttribute</span></span>

<span data-ttu-id="b0c63-741">データ</span><span class="sxs-lookup"><span data-stu-id="b0c63-741">data</span></span>  

### <a name="return-value---sysobsoleteattribute"></a><span data-ttu-id="b0c63-742">戻り値 - SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="b0c63-742">Return Value - SysObsoleteAttribute</span></span>

## <a name="method-usecaptionfrommenuitem"></a><span data-ttu-id="b0c63-743">メソッド useCaptionFromMenuItem</span><span class="sxs-lookup"><span data-stu-id="b0c63-743">Method useCaptionFromMenuItem</span></span>

```xpp
public int useCaptionFromMenuItem([int value])
```

### <a name="parameters---usecaptionfrommenuitem"></a><span data-ttu-id="b0c63-744">パラメーター - useCaptionFromMenuItem</span><span class="sxs-lookup"><span data-stu-id="b0c63-744">Parameters - useCaptionFromMenuItem</span></span>

<span data-ttu-id="b0c63-745">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-745">value</span></span>  

### <a name="return-value---usecaptionfrommenuitem"></a><span data-ttu-id="b0c63-746">戻り値 - useCaptionFromMenuItem</span><span class="sxs-lookup"><span data-stu-id="b0c63-746">Return Value - useCaptionFromMenuItem</span></span>

## <a name="method-usersettingallowsave"></a><span data-ttu-id="b0c63-747">メソッド userSettingAllowSave</span><span class="sxs-lookup"><span data-stu-id="b0c63-747">Method userSettingAllowSave</span></span>

```xpp
public boolean userSettingAllowSave()
```

### <a name="return-value---usersettingallowsave"></a><span data-ttu-id="b0c63-748">戻り値 - userSettingAllowSave</span><span class="sxs-lookup"><span data-stu-id="b0c63-748">Return Value - userSettingAllowSave</span></span>

## <a name="method-useuserlayout"></a><span data-ttu-id="b0c63-749">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="b0c63-749">Method useUserLayout</span></span>

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a><span data-ttu-id="b0c63-750">パラメーター - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="b0c63-750">Parameters - useUserLayout</span></span>

<span data-ttu-id="b0c63-751">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-751">value</span></span>  

### <a name="return-value---useuserlayout"></a><span data-ttu-id="b0c63-752">戻り値 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="b0c63-752">Return Value - useUserLayout</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="b0c63-753">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-753">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="b0c63-754">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-754">Parameters - viewEditMode</span></span>

<span data-ttu-id="b0c63-755">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-755">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="b0c63-756">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-756">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="b0c63-757">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="b0c63-757">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="b0c63-758">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="b0c63-758">Parameters - visible</span></span>

<span data-ttu-id="b0c63-759">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-759">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="b0c63-760">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="b0c63-760">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="b0c63-761">メソッド width</span><span class="sxs-lookup"><span data-stu-id="b0c63-761">Method width</span></span>

<span data-ttu-id="b0c63-762">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-762">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="b0c63-763">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="b0c63-763">Parameters - width</span></span>

<span data-ttu-id="b0c63-764">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-764">value</span></span>  

<!-- -->

<span data-ttu-id="b0c63-765">モード</span><span class="sxs-lookup"><span data-stu-id="b0c63-765">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="b0c63-766">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="b0c63-766">Return Value - width</span></span>

<span data-ttu-id="b0c63-767">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="b0c63-767">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="b0c63-768">備考 - width</span><span class="sxs-lookup"><span data-stu-id="b0c63-768">Remarks - width</span></span>

<span data-ttu-id="b0c63-769">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0c63-769">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="b0c63-770">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="b0c63-770">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="b0c63-771">モード。</span><span class="sxs-lookup"><span data-stu-id="b0c63-771">Mode.</span></span>           | <span data-ttu-id="b0c63-772">幅計算。</span><span class="sxs-lookup"><span data-stu-id="b0c63-772">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0c63-773">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="b0c63-773">-1 Exact.</span></span>       | <span data-ttu-id="b0c63-774">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0c63-774">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b0c63-775">0 自動。</span><span class="sxs-lookup"><span data-stu-id="b0c63-775">0 Auto.</span></span>         | <span data-ttu-id="b0c63-776">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b0c63-776">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b0c63-777">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="b0c63-777">1 Column width.</span></span> | <span data-ttu-id="b0c63-778">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="b0c63-778">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="b0c63-779">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="b0c63-779">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="b0c63-780">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-780">Method widthMode</span></span>

<span data-ttu-id="b0c63-781">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-781">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="b0c63-782">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-782">Parameters - widthMode</span></span>

<span data-ttu-id="b0c63-783">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-783">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="b0c63-784">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-784">Return Value - widthMode</span></span>

<span data-ttu-id="b0c63-785">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="b0c63-785">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="b0c63-786">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="b0c63-786">Remarks - widthMode</span></span>

<span data-ttu-id="b0c63-787">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="b0c63-787">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="b0c63-788">モード。</span><span class="sxs-lookup"><span data-stu-id="b0c63-788">Mode.</span></span>         | <span data-ttu-id="b0c63-789">幅計算。</span><span class="sxs-lookup"><span data-stu-id="b0c63-789">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0c63-790">正確。</span><span class="sxs-lookup"><span data-stu-id="b0c63-790">Exact.</span></span>        | <span data-ttu-id="b0c63-791">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b0c63-791">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="b0c63-792">自動。</span><span class="sxs-lookup"><span data-stu-id="b0c63-792">Auto.</span></span>         | <span data-ttu-id="b0c63-793">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="b0c63-793">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="b0c63-794">列の幅。</span><span class="sxs-lookup"><span data-stu-id="b0c63-794">Column width.</span></span> | <span data-ttu-id="b0c63-795">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="b0c63-795">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="b0c63-796">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="b0c63-796">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="b0c63-797">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-797">Method widthValue</span></span>

<span data-ttu-id="b0c63-798">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-798">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="b0c63-799">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-799">Parameters - widthValue</span></span>

<span data-ttu-id="b0c63-800">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-800">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="b0c63-801">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-801">Return Value - widthValue</span></span>

<span data-ttu-id="b0c63-802">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="b0c63-802">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="b0c63-803">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="b0c63-803">Remarks - widthValue</span></span>

<span data-ttu-id="b0c63-804">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="b0c63-804">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-windowresize"></a><span data-ttu-id="b0c63-805">メソッド windowResize</span><span class="sxs-lookup"><span data-stu-id="b0c63-805">Method windowResize</span></span>

```xpp
public int windowResize([int value])
```

### <a name="parameters---windowresize"></a><span data-ttu-id="b0c63-806">パラメーター - windowResize</span><span class="sxs-lookup"><span data-stu-id="b0c63-806">Parameters - windowResize</span></span>

<span data-ttu-id="b0c63-807">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-807">value</span></span>  

### <a name="return-value---windowresize"></a><span data-ttu-id="b0c63-808">戻り値 - windowResize</span><span class="sxs-lookup"><span data-stu-id="b0c63-808">Return Value - windowResize</span></span>

## <a name="method-windowtype"></a><span data-ttu-id="b0c63-809">メソッド windowType</span><span class="sxs-lookup"><span data-stu-id="b0c63-809">Method windowType</span></span>

```xpp
public int windowType([int value])
```

### <a name="parameters---windowtype"></a><span data-ttu-id="b0c63-810">パラメーター - windowType</span><span class="sxs-lookup"><span data-stu-id="b0c63-810">Parameters - windowType</span></span>

<span data-ttu-id="b0c63-811">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-811">value</span></span>  

### <a name="return-value---windowtype"></a><span data-ttu-id="b0c63-812">戻り値 - windowType</span><span class="sxs-lookup"><span data-stu-id="b0c63-812">Return Value - windowType</span></span>

## <a name="method-workflowdatasource"></a><span data-ttu-id="b0c63-813">メソッド workflowDatasource</span><span class="sxs-lookup"><span data-stu-id="b0c63-813">Method workflowDatasource</span></span>

```xpp
public int workflowDatasource([AnyType value])
```

### <a name="parameters---workflowdatasource"></a><span data-ttu-id="b0c63-814">パラメーター - workflowDatasource</span><span class="sxs-lookup"><span data-stu-id="b0c63-814">Parameters - workflowDatasource</span></span>

<span data-ttu-id="b0c63-815">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-815">value</span></span>  

### <a name="return-value---workflowdatasource"></a><span data-ttu-id="b0c63-816">戻り値 - workflowDatasource</span><span class="sxs-lookup"><span data-stu-id="b0c63-816">Return Value - workflowDatasource</span></span>

## <a name="method-workflowenabled"></a><span data-ttu-id="b0c63-817">メソッド workflowEnabled</span><span class="sxs-lookup"><span data-stu-id="b0c63-817">Method workflowEnabled</span></span>

```xpp
public boolean workflowEnabled([boolean value])
```

### <a name="parameters---workflowenabled"></a><span data-ttu-id="b0c63-818">パラメーター - workflowEnabled</span><span class="sxs-lookup"><span data-stu-id="b0c63-818">Parameters - workflowEnabled</span></span>

<span data-ttu-id="b0c63-819">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-819">value</span></span>  

### <a name="return-value---workflowenabled"></a><span data-ttu-id="b0c63-820">戻り値 - workflowEnabled</span><span class="sxs-lookup"><span data-stu-id="b0c63-820">Return Value - workflowEnabled</span></span>

## <a name="method-workflowtype"></a><span data-ttu-id="b0c63-821">メソッド workflowType</span><span class="sxs-lookup"><span data-stu-id="b0c63-821">Method workflowType</span></span>

```xpp
public str workflowType([str value])
```

### <a name="parameters---workflowtype"></a><span data-ttu-id="b0c63-822">パラメーター - workflowType</span><span class="sxs-lookup"><span data-stu-id="b0c63-822">Parameters - workflowType</span></span>

<span data-ttu-id="b0c63-823">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-823">value</span></span>  

### <a name="return-value---workflowtype"></a><span data-ttu-id="b0c63-824">戻り値 - workflowType</span><span class="sxs-lookup"><span data-stu-id="b0c63-824">Return Value - workflowType</span></span>

## <a name="method-dialogsize"></a><span data-ttu-id="b0c63-825">メソッド dialogSize</span><span class="sxs-lookup"><span data-stu-id="b0c63-825">Method dialogSize</span></span>

```xpp
public int dialogSize([int value])
```

### <a name="parameters---dialogsize"></a><span data-ttu-id="b0c63-826">パラメーター - dialogSize</span><span class="sxs-lookup"><span data-stu-id="b0c63-826">Parameters - dialogSize</span></span>

<span data-ttu-id="b0c63-827">値</span><span class="sxs-lookup"><span data-stu-id="b0c63-827">value</span></span>  

### <a name="return-value---dialogsize"></a><span data-ttu-id="b0c63-828">戻り値 - dialogSize</span><span class="sxs-lookup"><span data-stu-id="b0c63-828">Return Value - dialogSize</span></span>

## <a name="method-resetusersetting"></a><span data-ttu-id="b0c63-829">メソッド resetUserSetting</span><span class="sxs-lookup"><span data-stu-id="b0c63-829">Method resetUserSetting</span></span>

```xpp
public void resetUserSetting()
```

## <a name="method-removecontrol"></a><span data-ttu-id="b0c63-830">メソッド removeControl</span><span class="sxs-lookup"><span data-stu-id="b0c63-830">Method removeControl</span></span>

```xpp
public void removeControl([int controlId])
```

### <a name="parameters---removecontrol"></a><span data-ttu-id="b0c63-831">パラメーター - removeControl</span><span class="sxs-lookup"><span data-stu-id="b0c63-831">Parameters - removeControl</span></span>

<span data-ttu-id="b0c63-832">controlId</span><span class="sxs-lookup"><span data-stu-id="b0c63-832">controlId</span></span>  

## <a name="method-finalize"></a><span data-ttu-id="b0c63-833">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="b0c63-833">Method finalize</span></span>

```xpp
public void finalize()
```

