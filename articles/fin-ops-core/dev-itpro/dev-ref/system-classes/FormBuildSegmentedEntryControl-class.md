---
title: FormBuildSegmentedEntryControl クラス
description: このトピックでは、FormBuildSegmentedEntryControl クラスについて説明します。
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
ms.openlocfilehash: ba4c2bdedd02c8dfa2ce97d8d3b02073d4ef5b1f
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502643"
---
# <a name="class-formbuildsegmentedentrycontrol"></a><span data-ttu-id="76417-103">クラス FormBuildSegmentedEntryControl</span><span class="sxs-lookup"><span data-stu-id="76417-103">Class FormBuildSegmentedEntryControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildSegmentedEntryControl extends FormBuildControl
```

## <a name="remarks"></a><span data-ttu-id="76417-104">備考</span><span class="sxs-lookup"><span data-stu-id="76417-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="76417-105">例</span><span class="sxs-lookup"><span data-stu-id="76417-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="76417-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="76417-106">Methods</span></span>

| <span data-ttu-id="76417-107">方法</span><span class="sxs-lookup"><span data-stu-id="76417-107">Method</span></span>                                                                                                      | <span data-ttu-id="76417-108">説明</span><span class="sxs-lookup"><span data-stu-id="76417-108">Description</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76417-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="76417-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="76417-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="76417-110">Determines whether to align the control.</span></span>                                                                                                  |
| <span data-ttu-id="76417-111">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="76417-111">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="76417-112">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="76417-112">Determines whether the user can change the contents of the control.</span></span>                                                                       |
| <span data-ttu-id="76417-113">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="76417-113">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="76417-114">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="76417-114">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                        |
| <span data-ttu-id="76417-115">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-115">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="76417-116">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-116">Gets or sets the background color of the control.</span></span>                                                                                         |
| <span data-ttu-id="76417-117">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-117">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="76417-118">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="76417-118">Determines whether the control background can be transparent.</span></span>                                                                             |
| <span data-ttu-id="76417-119">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-119">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="76417-120">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-120">Gets or sets the style of the borderline of the control.</span></span>                                                                                  |
| <span data-ttu-id="76417-121">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-121">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="76417-122">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-122">Gets or sets the color scheme of the control.</span></span>                                                                                             |
| <span data-ttu-id="76417-123">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="76417-123">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="76417-124">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-124">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                       |
| <span data-ttu-id="76417-125">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="76417-125">public int containerId()</span></span>                                                                                    | <span data-ttu-id="76417-126">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="76417-126">Retrieves the ID of the parent container for the control.</span></span>                                                                                 |
| <span data-ttu-id="76417-127">public boolean contextFlyout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="76417-127">public boolean contextFlyout(\[boolean value\])</span></span>                                                             |                                                                                                                                           |
| <span data-ttu-id="76417-128">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="76417-128">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                           |
| <span data-ttu-id="76417-129">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="76417-129">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                           |
| <span data-ttu-id="76417-130">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="76417-130">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="76417-131">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="76417-131">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="76417-132">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-132">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                  |
| <span data-ttu-id="76417-133">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-133">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="76417-134">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-134">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="76417-135">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="76417-135">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                         |
| <span data-ttu-id="76417-136">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="76417-136">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="76417-137">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="76417-137">Determines whether to enable or disable the object.</span></span>                                                                                       |
| <span data-ttu-id="76417-138">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="76417-138">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                           |
| <span data-ttu-id="76417-139">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-139">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="76417-140">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-140">Gets or sets the text color for the control to use.</span></span>                                                                                       |
| <span data-ttu-id="76417-141">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="76417-141">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="76417-142">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-142">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="76417-143">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-143">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="76417-144">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-144">Gets or sets a calculation mode for the height of the control.</span></span>                                                                            |
| <span data-ttu-id="76417-145">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-145">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="76417-146">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-146">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="76417-147">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="76417-147">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="76417-148">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-148">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="76417-149">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="76417-149">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="76417-150">public int id()</span><span class="sxs-lookup"><span data-stu-id="76417-150">public int id()</span></span>                                                                                             | <span data-ttu-id="76417-151">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="76417-151">Retrieves the ID of the control.</span></span>                                                                                                          |
| <span data-ttu-id="76417-152">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="76417-152">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="76417-153">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="76417-153">Retrieves a value that indicates whether the control is a container control.</span></span>                                                              |
| <span data-ttu-id="76417-154">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="76417-154">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="76417-155">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-155">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="76417-156">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-156">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="76417-157">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-157">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="76417-158">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-158">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="76417-159">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="76417-159">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="76417-160">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-160">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="76417-161">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-161">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="76417-162">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-162">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                           |
| <span data-ttu-id="76417-163">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="76417-163">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                           |
| <span data-ttu-id="76417-164">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-164">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="76417-165">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-165">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="76417-166">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="76417-166">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                           |
| <span data-ttu-id="76417-167">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-167">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="76417-168">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="76417-168">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                           |
| <span data-ttu-id="76417-169">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="76417-169">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="76417-170">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-170">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="76417-171">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-171">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="76417-172">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="76417-172">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="76417-173">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-173">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="76417-174">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-174">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="76417-175">public boolean mandatory(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="76417-175">public boolean mandatory(\[boolean value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="76417-176">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="76417-176">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="76417-177">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-177">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="76417-178">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-178">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="76417-179">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-179">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                           |
| <span data-ttu-id="76417-180">public FieldId referenceField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="76417-180">public FieldId referenceField(\[FieldId value\])</span></span>                                                            |                                                                                                                                           |
| <span data-ttu-id="76417-181">public str replacementFieldGroup(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="76417-181">public str replacementFieldGroup(\[str value\])</span></span>                                                             |                                                                                                                                           |
| <span data-ttu-id="76417-182">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="76417-182">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                           |
| <span data-ttu-id="76417-183">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="76417-183">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="76417-184">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="76417-184">public boolean skip(\[boolean value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="76417-185">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="76417-185">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="76417-186">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-186">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                           |
| <span data-ttu-id="76417-187">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-187">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="76417-188">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-188">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="76417-189">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-189">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="76417-190">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-190">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="76417-191">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-191">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="76417-192">public Int64 value(\[Int64 value\])</span><span class="sxs-lookup"><span data-stu-id="76417-192">public Int64 value(\[Int64 value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="76417-193">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="76417-193">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                           |
| <span data-ttu-id="76417-194">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="76417-194">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="76417-195">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-195">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="76417-196">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-196">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="76417-197">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="76417-197">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="76417-198">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="76417-198">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="76417-199">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-199">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="76417-200">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-200">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="76417-201">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-201">Gets or sets the calculation mode of the width of the control.</span></span>                                                                            |
| <span data-ttu-id="76417-202">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="76417-202">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="76417-203">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-203">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="76417-204">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="76417-204">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                           |

## <a name="method-aligncontrol"></a><span data-ttu-id="76417-205">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="76417-205">Method alignControl</span></span>

<span data-ttu-id="76417-206">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="76417-206">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="76417-207">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="76417-207">Parameters - alignControl</span></span>

<span data-ttu-id="76417-208">値</span><span class="sxs-lookup"><span data-stu-id="76417-208">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="76417-209">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="76417-209">Return Value - alignControl</span></span>

<span data-ttu-id="76417-210">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="76417-210">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="76417-211">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="76417-211">Remarks - alignControl</span></span>

<span data-ttu-id="76417-212">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="76417-212">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="76417-213">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="76417-213">Method allowEdit</span></span>

<span data-ttu-id="76417-214">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="76417-214">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="76417-215">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="76417-215">Parameters - allowEdit</span></span>

<span data-ttu-id="76417-216">値</span><span class="sxs-lookup"><span data-stu-id="76417-216">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="76417-217">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="76417-217">Return Value - allowEdit</span></span>

<span data-ttu-id="76417-218">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="76417-218">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="76417-219">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="76417-219">Remarks - allowEdit</span></span>

<span data-ttu-id="76417-220">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="76417-220">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="76417-221">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="76417-221">Method autoDeclaration</span></span>

<span data-ttu-id="76417-222">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="76417-222">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="76417-223">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="76417-223">Parameters - autoDeclaration</span></span>

<span data-ttu-id="76417-224">値</span><span class="sxs-lookup"><span data-stu-id="76417-224">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="76417-225">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="76417-225">Return Value - autoDeclaration</span></span>

<span data-ttu-id="76417-226">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="76417-226">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="76417-227">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="76417-227">Remarks - autoDeclaration</span></span>

<span data-ttu-id="76417-228">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="76417-228">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="76417-229">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="76417-229">Method backgroundColor</span></span>

<span data-ttu-id="76417-230">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-230">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="76417-231">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="76417-231">Parameters - backgroundColor</span></span>

<span data-ttu-id="76417-232">値</span><span class="sxs-lookup"><span data-stu-id="76417-232">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="76417-233">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="76417-233">Return Value - backgroundColor</span></span>

<span data-ttu-id="76417-234">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="76417-234">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="76417-235">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="76417-235">Remarks - backgroundColor</span></span>

<span data-ttu-id="76417-236">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="76417-236">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="76417-237">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="76417-237">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="76417-238">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="76417-238">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="76417-239">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="76417-239">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="76417-240">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="76417-240">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="76417-241">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="76417-241">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="76417-242">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="76417-242">Method backStyle</span></span>

<span data-ttu-id="76417-243">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="76417-243">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="76417-244">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="76417-244">Parameters - backStyle</span></span>

<span data-ttu-id="76417-245">値</span><span class="sxs-lookup"><span data-stu-id="76417-245">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="76417-246">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="76417-246">Return Value - backStyle</span></span>

<span data-ttu-id="76417-247">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="76417-247">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-border"></a><span data-ttu-id="76417-248">メソッド border</span><span class="sxs-lookup"><span data-stu-id="76417-248">Method border</span></span>

<span data-ttu-id="76417-249">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-249">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="76417-250">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="76417-250">Parameters - border</span></span>

<span data-ttu-id="76417-251">値</span><span class="sxs-lookup"><span data-stu-id="76417-251">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="76417-252">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="76417-252">Return Value - border</span></span>

<span data-ttu-id="76417-253">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="76417-253">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="76417-254">備考 - border</span><span class="sxs-lookup"><span data-stu-id="76417-254">Remarks - border</span></span>

<span data-ttu-id="76417-255">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="76417-255">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="76417-256">値です。</span><span class="sxs-lookup"><span data-stu-id="76417-256">Value.</span></span> | <span data-ttu-id="76417-257">説明。</span><span class="sxs-lookup"><span data-stu-id="76417-257">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="76417-258">0</span><span class="sxs-lookup"><span data-stu-id="76417-258">0</span></span>      | <span data-ttu-id="76417-259">自動。</span><span class="sxs-lookup"><span data-stu-id="76417-259">Auto.</span></span>        |
| <span data-ttu-id="76417-260">1</span><span class="sxs-lookup"><span data-stu-id="76417-260">1</span></span>      | <span data-ttu-id="76417-261">3D。</span><span class="sxs-lookup"><span data-stu-id="76417-261">3D.</span></span>          |
| <span data-ttu-id="76417-262">2</span><span class="sxs-lookup"><span data-stu-id="76417-262">2</span></span>      | <span data-ttu-id="76417-263">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="76417-263">Single line.</span></span> |
| <span data-ttu-id="76417-264">3</span><span class="sxs-lookup"><span data-stu-id="76417-264">3</span></span>      | <span data-ttu-id="76417-265">均一。</span><span class="sxs-lookup"><span data-stu-id="76417-265">Flat.</span></span>        |
| <span data-ttu-id="76417-266">4</span><span class="sxs-lookup"><span data-stu-id="76417-266">4</span></span>      | <span data-ttu-id="76417-267">なし。</span><span class="sxs-lookup"><span data-stu-id="76417-267">None.</span></span>        |

## <a name="method-colorscheme"></a><span data-ttu-id="76417-268">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="76417-268">Method colorScheme</span></span>

<span data-ttu-id="76417-269">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-269">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="76417-270">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="76417-270">Parameters - colorScheme</span></span>

<span data-ttu-id="76417-271">値</span><span class="sxs-lookup"><span data-stu-id="76417-271">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="76417-272">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="76417-272">Return Value - colorScheme</span></span>

<span data-ttu-id="76417-273">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="76417-273">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="76417-274">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="76417-274">Remarks - colorScheme</span></span>

<span data-ttu-id="76417-275">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="76417-275">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="76417-276">値です。</span><span class="sxs-lookup"><span data-stu-id="76417-276">Value.</span></span> | <span data-ttu-id="76417-277">スタイル。</span><span class="sxs-lookup"><span data-stu-id="76417-277">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="76417-278">0</span><span class="sxs-lookup"><span data-stu-id="76417-278">0</span></span>      | <span data-ttu-id="76417-279">既定。</span><span class="sxs-lookup"><span data-stu-id="76417-279">Default.</span></span>                      |
| <span data-ttu-id="76417-280">1</span><span class="sxs-lookup"><span data-stu-id="76417-280">1</span></span>      | <span data-ttu-id="76417-281">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="76417-281">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="76417-282">2</span><span class="sxs-lookup"><span data-stu-id="76417-282">2</span></span>      | <span data-ttu-id="76417-283">真の配色。</span><span class="sxs-lookup"><span data-stu-id="76417-283">The true-color scheme.</span></span>        |

## <a name="method-configurationkey"></a><span data-ttu-id="76417-284">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="76417-284">Method configurationKey</span></span>

<span data-ttu-id="76417-285">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-285">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="76417-286">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="76417-286">Parameters - configurationKey</span></span>

<span data-ttu-id="76417-287">値</span><span class="sxs-lookup"><span data-stu-id="76417-287">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="76417-288">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="76417-288">Return Value - configurationKey</span></span>

<span data-ttu-id="76417-289">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="76417-289">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="76417-290">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="76417-290">Remarks - configurationKey</span></span>

<span data-ttu-id="76417-291">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="76417-291">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="76417-292">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="76417-292">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="76417-293">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="76417-293">Method containerId</span></span>

<span data-ttu-id="76417-294">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="76417-294">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="76417-295">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="76417-295">Return Value - containerId</span></span>

<span data-ttu-id="76417-296">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="76417-296">The ID of the parent container.</span></span>

## <a name="method-contextflyout"></a><span data-ttu-id="76417-297">メソッド contextFlyout</span><span class="sxs-lookup"><span data-stu-id="76417-297">Method contextFlyout</span></span>

```xpp
public boolean contextFlyout([boolean value])
```

### <a name="parameters---contextflyout"></a><span data-ttu-id="76417-298">パラメーター - contextFlyout</span><span class="sxs-lookup"><span data-stu-id="76417-298">Parameters - contextFlyout</span></span>

<span data-ttu-id="76417-299">値</span><span class="sxs-lookup"><span data-stu-id="76417-299">value</span></span>  

### <a name="return-value---contextflyout"></a><span data-ttu-id="76417-300">戻り値 - contextFlyout</span><span class="sxs-lookup"><span data-stu-id="76417-300">Return Value - contextFlyout</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="76417-301">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="76417-301">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="76417-302">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="76417-302">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="76417-303">値</span><span class="sxs-lookup"><span data-stu-id="76417-303">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="76417-304">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="76417-304">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="76417-305">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="76417-305">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="76417-306">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="76417-306">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="76417-307">値</span><span class="sxs-lookup"><span data-stu-id="76417-307">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="76417-308">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="76417-308">Return Value - countryRegionContextField</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="76417-309">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="76417-309">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="76417-310">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="76417-310">Parameters - dataRelationPath</span></span>

<span data-ttu-id="76417-311">値</span><span class="sxs-lookup"><span data-stu-id="76417-311">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="76417-312">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="76417-312">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="76417-313">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="76417-313">Method dataSource</span></span>

<span data-ttu-id="76417-314">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-314">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="76417-315">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="76417-315">Parameters - dataSource</span></span>

<span data-ttu-id="76417-316">値</span><span class="sxs-lookup"><span data-stu-id="76417-316">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="76417-317">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="76417-317">Return Value - dataSource</span></span>

<span data-ttu-id="76417-318">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="76417-318">The identifier of the data source that will be used.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="76417-319">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="76417-319">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="76417-320">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="76417-320">Parameters - displayTarget</span></span>

<span data-ttu-id="76417-321">値</span><span class="sxs-lookup"><span data-stu-id="76417-321">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="76417-322">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="76417-322">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="76417-323">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="76417-323">Method dragDrop</span></span>

<span data-ttu-id="76417-324">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="76417-324">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="76417-325">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="76417-325">Parameters - dragDrop</span></span>

<span data-ttu-id="76417-326">値</span><span class="sxs-lookup"><span data-stu-id="76417-326">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="76417-327">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="76417-327">Return Value - dragDrop</span></span>

<span data-ttu-id="76417-328">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="76417-328">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="76417-329">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="76417-329">Method enabled</span></span>

<span data-ttu-id="76417-330">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="76417-330">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="76417-331">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="76417-331">Parameters - enabled</span></span>

<span data-ttu-id="76417-332">値</span><span class="sxs-lookup"><span data-stu-id="76417-332">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="76417-333">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="76417-333">Return Value - enabled</span></span>

<span data-ttu-id="76417-334">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="76417-334">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="76417-335">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="76417-335">Remarks - enabled</span></span>

<span data-ttu-id="76417-336">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="76417-336">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="76417-337">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="76417-337">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="76417-338">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="76417-338">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="76417-339">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="76417-339">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="76417-340">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="76417-340">Parameters - extendedDataType</span></span>

<span data-ttu-id="76417-341">値</span><span class="sxs-lookup"><span data-stu-id="76417-341">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="76417-342">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="76417-342">Return Value - extendedDataType</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="76417-343">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="76417-343">Method foregroundColor</span></span>

<span data-ttu-id="76417-344">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-344">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="76417-345">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="76417-345">Parameters - foregroundColor</span></span>

<span data-ttu-id="76417-346">値</span><span class="sxs-lookup"><span data-stu-id="76417-346">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="76417-347">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="76417-347">Return Value - foregroundColor</span></span>

<span data-ttu-id="76417-348">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="76417-348">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="76417-349">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="76417-349">Remarks - foregroundColor</span></span>

<span data-ttu-id="76417-350">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="76417-350">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="76417-351">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="76417-351">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="76417-352">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="76417-352">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="76417-353">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="76417-353">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="76417-354">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="76417-354">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="76417-355">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="76417-355">The maximum value for a single byte is 255.</span></span>

## <a name="method-height"></a><span data-ttu-id="76417-356">メソッド height</span><span class="sxs-lookup"><span data-stu-id="76417-356">Method height</span></span>

<span data-ttu-id="76417-357">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-357">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="76417-358">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="76417-358">Parameters - height</span></span>

<span data-ttu-id="76417-359">値</span><span class="sxs-lookup"><span data-stu-id="76417-359">value</span></span>  

<!-- -->

<span data-ttu-id="76417-360">モード</span><span class="sxs-lookup"><span data-stu-id="76417-360">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="76417-361">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="76417-361">Return Value - height</span></span>

<span data-ttu-id="76417-362">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="76417-362">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="76417-363">備考 - height</span><span class="sxs-lookup"><span data-stu-id="76417-363">Remarks - height</span></span>

<span data-ttu-id="76417-364">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="76417-364">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="76417-365">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="76417-365">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="76417-366">モード。</span><span class="sxs-lookup"><span data-stu-id="76417-366">Mode.</span></span>            | <span data-ttu-id="76417-367">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="76417-367">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="76417-368">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="76417-368">-1 Exact.</span></span>        | <span data-ttu-id="76417-369">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="76417-369">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="76417-370">0 自動。</span><span class="sxs-lookup"><span data-stu-id="76417-370">0 Auto.</span></span>          | <span data-ttu-id="76417-371">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="76417-371">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="76417-372">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="76417-372">1 Column height.</span></span> | <span data-ttu-id="76417-373">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="76417-373">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="76417-374">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="76417-374">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="76417-375">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="76417-375">Method heightMode</span></span>

<span data-ttu-id="76417-376">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-376">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="76417-377">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="76417-377">Parameters - heightMode</span></span>

<span data-ttu-id="76417-378">値</span><span class="sxs-lookup"><span data-stu-id="76417-378">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="76417-379">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="76417-379">Return Value - heightMode</span></span>

<span data-ttu-id="76417-380">計算モード。</span><span class="sxs-lookup"><span data-stu-id="76417-380">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="76417-381">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="76417-381">Remarks - heightMode</span></span>

<span data-ttu-id="76417-382">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="76417-382">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="76417-383">モード。</span><span class="sxs-lookup"><span data-stu-id="76417-383">Mode.</span></span>          | <span data-ttu-id="76417-384">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="76417-384">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="76417-385">正確。</span><span class="sxs-lookup"><span data-stu-id="76417-385">Exact.</span></span>         | <span data-ttu-id="76417-386">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="76417-386">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="76417-387">自動。</span><span class="sxs-lookup"><span data-stu-id="76417-387">Auto.</span></span>          | <span data-ttu-id="76417-388">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="76417-388">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="76417-389">列の高さ</span><span class="sxs-lookup"><span data-stu-id="76417-389">Column height.</span></span> | <span data-ttu-id="76417-390">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="76417-390">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="76417-391">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="76417-391">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="76417-392">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="76417-392">Method heightValue</span></span>

<span data-ttu-id="76417-393">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-393">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="76417-394">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="76417-394">Parameters - heightValue</span></span>

<span data-ttu-id="76417-395">値</span><span class="sxs-lookup"><span data-stu-id="76417-395">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="76417-396">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="76417-396">Return Value - heightValue</span></span>

<span data-ttu-id="76417-397">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="76417-397">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="76417-398">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="76417-398">Remarks - heightValue</span></span>

<span data-ttu-id="76417-399">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="76417-399">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="76417-400">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="76417-400">Method helpText</span></span>

<span data-ttu-id="76417-401">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-401">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="76417-402">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="76417-402">Parameters - helpText</span></span>

<span data-ttu-id="76417-403">値</span><span class="sxs-lookup"><span data-stu-id="76417-403">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="76417-404">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="76417-404">Return Value - helpText</span></span>

<span data-ttu-id="76417-405">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="76417-405">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="76417-406">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="76417-406">Remarks - helpText</span></span>

<span data-ttu-id="76417-407">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-407">Set the HelpText property for an object by using the property dialogue box.</span></span> <span data-ttu-id="76417-408">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="76417-408">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="76417-409">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="76417-409">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="76417-410">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="76417-410">Parameters - hierarchyParent</span></span>

<span data-ttu-id="76417-411">値</span><span class="sxs-lookup"><span data-stu-id="76417-411">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="76417-412">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="76417-412">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="76417-413">メソッド id</span><span class="sxs-lookup"><span data-stu-id="76417-413">Method id</span></span>

<span data-ttu-id="76417-414">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="76417-414">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="76417-415">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="76417-415">Return Value - id</span></span>

<span data-ttu-id="76417-416">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="76417-416">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="76417-417">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="76417-417">Method isContainer</span></span>

<span data-ttu-id="76417-418">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="76417-418">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="76417-419">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="76417-419">Return Value - isContainer</span></span>

<span data-ttu-id="76417-420">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="76417-420">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-label"></a><span data-ttu-id="76417-421">メソッド label</span><span class="sxs-lookup"><span data-stu-id="76417-421">Method label</span></span>

<span data-ttu-id="76417-422">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-422">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="76417-423">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="76417-423">Parameters - label</span></span>

<span data-ttu-id="76417-424">値</span><span class="sxs-lookup"><span data-stu-id="76417-424">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="76417-425">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="76417-425">Return Value - label</span></span>

<span data-ttu-id="76417-426">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="76417-426">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="76417-427">備考 - label</span><span class="sxs-lookup"><span data-stu-id="76417-427">Remarks - label</span></span>

<span data-ttu-id="76417-428">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="76417-428">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="76417-429">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="76417-429">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="76417-430">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="76417-430">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="76417-431">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="76417-431">Parameters - labelAlignment</span></span>

<span data-ttu-id="76417-432">値</span><span class="sxs-lookup"><span data-stu-id="76417-432">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="76417-433">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="76417-433">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="76417-434">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="76417-434">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="76417-435">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="76417-435">Parameters - labelBold</span></span>

<span data-ttu-id="76417-436">値</span><span class="sxs-lookup"><span data-stu-id="76417-436">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="76417-437">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="76417-437">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="76417-438">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="76417-438">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="76417-439">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="76417-439">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="76417-440">値</span><span class="sxs-lookup"><span data-stu-id="76417-440">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="76417-441">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="76417-441">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="76417-442">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="76417-442">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="76417-443">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="76417-443">Parameters - labelFont</span></span>

<span data-ttu-id="76417-444">値</span><span class="sxs-lookup"><span data-stu-id="76417-444">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="76417-445">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="76417-445">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="76417-446">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="76417-446">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="76417-447">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="76417-447">Parameters - labelFontSize</span></span>

<span data-ttu-id="76417-448">値</span><span class="sxs-lookup"><span data-stu-id="76417-448">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="76417-449">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="76417-449">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="76417-450">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="76417-450">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="76417-451">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="76417-451">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="76417-452">値</span><span class="sxs-lookup"><span data-stu-id="76417-452">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="76417-453">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="76417-453">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="76417-454">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="76417-454">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="76417-455">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="76417-455">Parameters - labelGuide</span></span>

<span data-ttu-id="76417-456">値</span><span class="sxs-lookup"><span data-stu-id="76417-456">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="76417-457">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="76417-457">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="76417-458">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="76417-458">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="76417-459">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="76417-459">Parameters - labelHeight</span></span>

<span data-ttu-id="76417-460">値</span><span class="sxs-lookup"><span data-stu-id="76417-460">value</span></span>  

<!-- -->

<span data-ttu-id="76417-461">モード</span><span class="sxs-lookup"><span data-stu-id="76417-461">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="76417-462">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="76417-462">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="76417-463">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="76417-463">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="76417-464">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="76417-464">Parameters - labelHeightMode</span></span>

<span data-ttu-id="76417-465">値</span><span class="sxs-lookup"><span data-stu-id="76417-465">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="76417-466">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="76417-466">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="76417-467">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="76417-467">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="76417-468">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="76417-468">Parameters - labelHeightValue</span></span>

<span data-ttu-id="76417-469">値</span><span class="sxs-lookup"><span data-stu-id="76417-469">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="76417-470">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="76417-470">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="76417-471">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="76417-471">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="76417-472">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="76417-472">Parameters - labelItalic</span></span>

<span data-ttu-id="76417-473">値</span><span class="sxs-lookup"><span data-stu-id="76417-473">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="76417-474">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="76417-474">Return Value - labelItalic</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="76417-475">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="76417-475">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="76417-476">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="76417-476">Parameters - labelPosition</span></span>

<span data-ttu-id="76417-477">値</span><span class="sxs-lookup"><span data-stu-id="76417-477">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="76417-478">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="76417-478">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="76417-479">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="76417-479">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="76417-480">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="76417-480">Parameters - labelUnderline</span></span>

<span data-ttu-id="76417-481">値</span><span class="sxs-lookup"><span data-stu-id="76417-481">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="76417-482">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="76417-482">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="76417-483">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="76417-483">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="76417-484">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="76417-484">Parameters - labelWidth</span></span>

<span data-ttu-id="76417-485">値</span><span class="sxs-lookup"><span data-stu-id="76417-485">value</span></span>  

<!-- -->

<span data-ttu-id="76417-486">モード</span><span class="sxs-lookup"><span data-stu-id="76417-486">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="76417-487">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="76417-487">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="76417-488">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="76417-488">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="76417-489">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="76417-489">Parameters - labelWidthMode</span></span>

<span data-ttu-id="76417-490">値</span><span class="sxs-lookup"><span data-stu-id="76417-490">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="76417-491">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="76417-491">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="76417-492">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="76417-492">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="76417-493">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="76417-493">Parameters - labelWidthValue</span></span>

<span data-ttu-id="76417-494">値</span><span class="sxs-lookup"><span data-stu-id="76417-494">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="76417-495">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="76417-495">Return Value - labelWidthValue</span></span>

## <a name="method-left"></a><span data-ttu-id="76417-496">メソッド left</span><span class="sxs-lookup"><span data-stu-id="76417-496">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="76417-497">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="76417-497">Parameters - left</span></span>

<span data-ttu-id="76417-498">値</span><span class="sxs-lookup"><span data-stu-id="76417-498">value</span></span>  

<!-- -->

<span data-ttu-id="76417-499">モード</span><span class="sxs-lookup"><span data-stu-id="76417-499">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="76417-500">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="76417-500">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="76417-501">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="76417-501">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="76417-502">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="76417-502">Parameters - leftMode</span></span>

<span data-ttu-id="76417-503">値</span><span class="sxs-lookup"><span data-stu-id="76417-503">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="76417-504">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="76417-504">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="76417-505">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="76417-505">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="76417-506">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="76417-506">Parameters - leftValue</span></span>

<span data-ttu-id="76417-507">値</span><span class="sxs-lookup"><span data-stu-id="76417-507">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="76417-508">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="76417-508">Return Value - leftValue</span></span>

## <a name="method-mandatory"></a><span data-ttu-id="76417-509">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="76417-509">Method mandatory</span></span>

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a><span data-ttu-id="76417-510">パラメーター - mandatory</span><span class="sxs-lookup"><span data-stu-id="76417-510">Parameters - mandatory</span></span>

<span data-ttu-id="76417-511">値</span><span class="sxs-lookup"><span data-stu-id="76417-511">value</span></span>  

### <a name="return-value---mandatory"></a><span data-ttu-id="76417-512">戻り値 - mandatory</span><span class="sxs-lookup"><span data-stu-id="76417-512">Return Value - mandatory</span></span>

## <a name="method-name"></a><span data-ttu-id="76417-513">メソッド名</span><span class="sxs-lookup"><span data-stu-id="76417-513">Method name</span></span>

<span data-ttu-id="76417-514">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-514">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="76417-515">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="76417-515">Parameters - name</span></span>

<span data-ttu-id="76417-516">値</span><span class="sxs-lookup"><span data-stu-id="76417-516">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="76417-517">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="76417-517">Return Value - name</span></span>

<span data-ttu-id="76417-518">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="76417-518">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="76417-519">備考 - name</span><span class="sxs-lookup"><span data-stu-id="76417-519">Remarks - name</span></span>

<span data-ttu-id="76417-520">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="76417-520">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="76417-521">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="76417-521">Begins with a letter.</span></span>
-   <span data-ttu-id="76417-522">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="76417-522">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="76417-523">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="76417-523">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="76417-524">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="76417-524">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="76417-525">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="76417-525">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, classes, and so on.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="76417-526">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="76417-526">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="76417-527">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="76417-527">Parameters - neededPermission</span></span>

<span data-ttu-id="76417-528">値</span><span class="sxs-lookup"><span data-stu-id="76417-528">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="76417-529">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="76417-529">Return Value - neededPermission</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="76417-530">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="76417-530">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="76417-531">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="76417-531">Parameters - promptrect</span></span>

<span data-ttu-id="76417-532">値</span><span class="sxs-lookup"><span data-stu-id="76417-532">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="76417-533">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="76417-533">Return Value - promptrect</span></span>

## <a name="method-referencefield"></a><span data-ttu-id="76417-534">メソッド referenceField</span><span class="sxs-lookup"><span data-stu-id="76417-534">Method referenceField</span></span>

```xpp
public FieldId referenceField([FieldId value])
```

### <a name="parameters---referencefield"></a><span data-ttu-id="76417-535">パラメーター - referenceField</span><span class="sxs-lookup"><span data-stu-id="76417-535">Parameters - referenceField</span></span>

<span data-ttu-id="76417-536">値</span><span class="sxs-lookup"><span data-stu-id="76417-536">value</span></span>  

### <a name="return-value---referencefield"></a><span data-ttu-id="76417-537">戻り値 - referenceField</span><span class="sxs-lookup"><span data-stu-id="76417-537">Return Value - referenceField</span></span>

## <a name="method-replacementfieldgroup"></a><span data-ttu-id="76417-538">メソッド replacementFieldGroup</span><span class="sxs-lookup"><span data-stu-id="76417-538">Method replacementFieldGroup</span></span>

```xpp
public str replacementFieldGroup([str value])
```

### <a name="parameters---replacementfieldgroup"></a><span data-ttu-id="76417-539">パラメーター - replacementFieldGroup</span><span class="sxs-lookup"><span data-stu-id="76417-539">Parameters - replacementFieldGroup</span></span>

<span data-ttu-id="76417-540">値</span><span class="sxs-lookup"><span data-stu-id="76417-540">value</span></span>  

### <a name="return-value---replacementfieldgroup"></a><span data-ttu-id="76417-541">戻り値 - replacementFieldGroup</span><span class="sxs-lookup"><span data-stu-id="76417-541">Return Value - replacementFieldGroup</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="76417-542">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="76417-542">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="76417-543">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="76417-543">Parameters - securityKey</span></span>

<span data-ttu-id="76417-544">値</span><span class="sxs-lookup"><span data-stu-id="76417-544">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="76417-545">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="76417-545">Return Value - securityKey</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="76417-546">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="76417-546">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="76417-547">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="76417-547">Parameters - showLabel</span></span>

<span data-ttu-id="76417-548">値</span><span class="sxs-lookup"><span data-stu-id="76417-548">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="76417-549">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="76417-549">Return Value - showLabel</span></span>

## <a name="method-skip"></a><span data-ttu-id="76417-550">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="76417-550">Method skip</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="76417-551">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="76417-551">Parameters - skip</span></span>

<span data-ttu-id="76417-552">値</span><span class="sxs-lookup"><span data-stu-id="76417-552">value</span></span>  

### <a name="return-value---skip"></a><span data-ttu-id="76417-553">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="76417-553">Return Value - skip</span></span>

## <a name="method-top"></a><span data-ttu-id="76417-554">メソッド top</span><span class="sxs-lookup"><span data-stu-id="76417-554">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="76417-555">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="76417-555">Parameters - top</span></span>

<span data-ttu-id="76417-556">値</span><span class="sxs-lookup"><span data-stu-id="76417-556">value</span></span>  

<!-- -->

<span data-ttu-id="76417-557">モード</span><span class="sxs-lookup"><span data-stu-id="76417-557">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="76417-558">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="76417-558">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="76417-559">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="76417-559">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="76417-560">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="76417-560">Parameters - topMode</span></span>

<span data-ttu-id="76417-561">値</span><span class="sxs-lookup"><span data-stu-id="76417-561">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="76417-562">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="76417-562">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="76417-563">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="76417-563">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="76417-564">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="76417-564">Parameters - topValue</span></span>

<span data-ttu-id="76417-565">値</span><span class="sxs-lookup"><span data-stu-id="76417-565">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="76417-566">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="76417-566">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="76417-567">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="76417-567">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="76417-568">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="76417-568">Parameters - type</span></span>

<span data-ttu-id="76417-569">値</span><span class="sxs-lookup"><span data-stu-id="76417-569">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="76417-570">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="76417-570">Return Value - type</span></span>

## <a name="method-userdata"></a><span data-ttu-id="76417-571">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="76417-571">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="76417-572">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="76417-572">Parameters - userData</span></span>

<span data-ttu-id="76417-573">値</span><span class="sxs-lookup"><span data-stu-id="76417-573">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="76417-574">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="76417-574">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="76417-575">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="76417-575">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="76417-576">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="76417-576">Parameters - userDataItem</span></span>

<span data-ttu-id="76417-577">値</span><span class="sxs-lookup"><span data-stu-id="76417-577">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="76417-578">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="76417-578">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="76417-579">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="76417-579">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="76417-580">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="76417-580">Parameters - userDataItems</span></span>

<span data-ttu-id="76417-581">値</span><span class="sxs-lookup"><span data-stu-id="76417-581">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="76417-582">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="76417-582">Return Value - userDataItems</span></span>

## <a name="method-value"></a><span data-ttu-id="76417-583">メソッド value</span><span class="sxs-lookup"><span data-stu-id="76417-583">Method value</span></span>

```xpp
public Int64 value([Int64 value])
```

### <a name="parameters---value"></a><span data-ttu-id="76417-584">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="76417-584">Parameters - value</span></span>

<span data-ttu-id="76417-585">値</span><span class="sxs-lookup"><span data-stu-id="76417-585">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="76417-586">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="76417-586">Return Value - value</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="76417-587">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="76417-587">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="76417-588">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="76417-588">Parameters - verticalSpacing</span></span>

<span data-ttu-id="76417-589">値</span><span class="sxs-lookup"><span data-stu-id="76417-589">value</span></span>  

<!-- -->

<span data-ttu-id="76417-590">モード</span><span class="sxs-lookup"><span data-stu-id="76417-590">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="76417-591">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="76417-591">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="76417-592">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="76417-592">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="76417-593">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="76417-593">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="76417-594">モード</span><span class="sxs-lookup"><span data-stu-id="76417-594">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="76417-595">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="76417-595">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="76417-596">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="76417-596">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="76417-597">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="76417-597">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="76417-598">値</span><span class="sxs-lookup"><span data-stu-id="76417-598">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="76417-599">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="76417-599">Return Value - verticalSpacingValue</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="76417-600">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="76417-600">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="76417-601">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="76417-601">Parameters - viewEditMode</span></span>

<span data-ttu-id="76417-602">値</span><span class="sxs-lookup"><span data-stu-id="76417-602">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="76417-603">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="76417-603">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="76417-604">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="76417-604">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="76417-605">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="76417-605">Parameters - visible</span></span>

<span data-ttu-id="76417-606">値</span><span class="sxs-lookup"><span data-stu-id="76417-606">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="76417-607">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="76417-607">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="76417-608">メソッド width</span><span class="sxs-lookup"><span data-stu-id="76417-608">Method width</span></span>

<span data-ttu-id="76417-609">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-609">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="76417-610">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="76417-610">Parameters - width</span></span>

<span data-ttu-id="76417-611">値</span><span class="sxs-lookup"><span data-stu-id="76417-611">value</span></span>  

<!-- -->

<span data-ttu-id="76417-612">モード</span><span class="sxs-lookup"><span data-stu-id="76417-612">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="76417-613">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="76417-613">Return Value - width</span></span>

<span data-ttu-id="76417-614">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="76417-614">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="76417-615">備考 - width</span><span class="sxs-lookup"><span data-stu-id="76417-615">Remarks - width</span></span>

<span data-ttu-id="76417-616">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="76417-616">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="76417-617">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="76417-617">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="76417-618">モード。</span><span class="sxs-lookup"><span data-stu-id="76417-618">Mode.</span></span>           | <span data-ttu-id="76417-619">幅計算。</span><span class="sxs-lookup"><span data-stu-id="76417-619">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="76417-620">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="76417-620">-1 Exact.</span></span>       | <span data-ttu-id="76417-621">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="76417-621">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="76417-622">0 自動。</span><span class="sxs-lookup"><span data-stu-id="76417-622">0 Auto.</span></span>         | <span data-ttu-id="76417-623">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="76417-623">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="76417-624">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="76417-624">1 Column width.</span></span> | <span data-ttu-id="76417-625">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="76417-625">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="76417-626">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="76417-626">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="76417-627">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="76417-627">Method widthMode</span></span>

<span data-ttu-id="76417-628">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-628">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="76417-629">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="76417-629">Parameters - widthMode</span></span>

<span data-ttu-id="76417-630">値</span><span class="sxs-lookup"><span data-stu-id="76417-630">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="76417-631">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="76417-631">Return Value - widthMode</span></span>

<span data-ttu-id="76417-632">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="76417-632">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="76417-633">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="76417-633">Remarks - widthMode</span></span>

<span data-ttu-id="76417-634">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="76417-634">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="76417-635">モード。</span><span class="sxs-lookup"><span data-stu-id="76417-635">Mode.</span></span>         | <span data-ttu-id="76417-636">幅計算。</span><span class="sxs-lookup"><span data-stu-id="76417-636">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="76417-637">正確。</span><span class="sxs-lookup"><span data-stu-id="76417-637">Exact.</span></span>        | <span data-ttu-id="76417-638">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="76417-638">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="76417-639">自動。</span><span class="sxs-lookup"><span data-stu-id="76417-639">Auto.</span></span>         | <span data-ttu-id="76417-640">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="76417-640">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="76417-641">列の幅。</span><span class="sxs-lookup"><span data-stu-id="76417-641">Column width.</span></span> | <span data-ttu-id="76417-642">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="76417-642">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="76417-643">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="76417-643">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="76417-644">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="76417-644">Method widthValue</span></span>

<span data-ttu-id="76417-645">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="76417-645">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="76417-646">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="76417-646">Parameters - widthValue</span></span>

<span data-ttu-id="76417-647">値</span><span class="sxs-lookup"><span data-stu-id="76417-647">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="76417-648">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="76417-648">Return Value - widthValue</span></span>

<span data-ttu-id="76417-649">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="76417-649">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="76417-650">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="76417-650">Remarks - widthValue</span></span>

<span data-ttu-id="76417-651">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="76417-651">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="76417-652">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="76417-652">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="76417-653">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="76417-653">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="76417-654">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="76417-654">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="76417-655">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="76417-655">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="76417-656">overrideObject</span><span class="sxs-lookup"><span data-stu-id="76417-656">overrideObject</span></span>  

