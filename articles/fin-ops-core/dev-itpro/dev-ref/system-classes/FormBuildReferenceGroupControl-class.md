---
title: FormBuildReferenceGroupControl クラス
description: このトピックでは、FormBuildReferenceGroupControl クラスについて説明します。
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
ms.openlocfilehash: 996146febe99c8ce7ffce17feaaa142217a5fa8b
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502957"
---
# <a name="class-formbuildreferencegroupcontrol"></a><span data-ttu-id="62b99-103">クラス FormBuildReferenceGroupControl</span><span class="sxs-lookup"><span data-stu-id="62b99-103">Class FormBuildReferenceGroupControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildReferenceGroupControl extends FormBuildControl
```

## <a name="remarks"></a><span data-ttu-id="62b99-104">備考</span><span class="sxs-lookup"><span data-stu-id="62b99-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="62b99-105">例</span><span class="sxs-lookup"><span data-stu-id="62b99-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="62b99-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="62b99-106">Methods</span></span>

| <span data-ttu-id="62b99-107">方法</span><span class="sxs-lookup"><span data-stu-id="62b99-107">Method</span></span>                                                                                                      | <span data-ttu-id="62b99-108">説明</span><span class="sxs-lookup"><span data-stu-id="62b99-108">Description</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62b99-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="62b99-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-110">Determines whether to align the control.</span></span>                                                                                                  |
| <span data-ttu-id="62b99-111">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-111">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="62b99-112">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-112">Determines whether the user can change the contents of the control.</span></span>                                                                       |
| <span data-ttu-id="62b99-113">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-113">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="62b99-114">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-114">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                        |
| <span data-ttu-id="62b99-115">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-115">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="62b99-116">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-116">Gets or sets the background color of the control.</span></span>                                                                                         |
| <span data-ttu-id="62b99-117">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-117">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="62b99-118">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-118">Determines whether the control background can be transparent.</span></span>                                                                             |
| <span data-ttu-id="62b99-119">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-119">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="62b99-120">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-120">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                               |
| <span data-ttu-id="62b99-121">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-121">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="62b99-122">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-122">Gets or sets the style of the borderline of the control.</span></span>                                                                                  |
| <span data-ttu-id="62b99-123">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-123">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="62b99-124">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-124">Gets or sets the character set of the font.</span></span>                                                                                               |
| <span data-ttu-id="62b99-125">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-125">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="62b99-126">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-126">Gets or sets the color scheme of the control.</span></span>                                                                                             |
| <span data-ttu-id="62b99-127">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-127">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="62b99-128">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-128">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                       |
| <span data-ttu-id="62b99-129">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="62b99-129">public int containerId()</span></span>                                                                                    | <span data-ttu-id="62b99-130">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="62b99-130">Retrieves the ID of the parent container for the control.</span></span>                                                                                 |
| <span data-ttu-id="62b99-131">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-131">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                           |
| <span data-ttu-id="62b99-132">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-132">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                           |
| <span data-ttu-id="62b99-133">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-133">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="62b99-134">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-134">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="62b99-135">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-135">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                  |
| <span data-ttu-id="62b99-136">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-136">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="62b99-137">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-137">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="62b99-138">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-138">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                         |
| <span data-ttu-id="62b99-139">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-139">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="62b99-140">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-140">Determines whether to enable or disable the object.</span></span>                                                                                       |
| <span data-ttu-id="62b99-141">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-141">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                           |
| <span data-ttu-id="62b99-142">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-142">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="62b99-143">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-143">Gets or sets the name of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="62b99-144">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-144">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="62b99-145">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-145">Gets or sets the size of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="62b99-146">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-146">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="62b99-147">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-147">Gets or sets the text color for the control to use.</span></span>                                                                                       |
| <span data-ttu-id="62b99-148">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="62b99-148">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="62b99-149">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-149">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="62b99-150">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-150">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="62b99-151">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-151">Gets or sets a calculation mode for the height of the control.</span></span>                                                                            |
| <span data-ttu-id="62b99-152">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-152">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="62b99-153">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-153">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="62b99-154">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-154">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="62b99-155">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-155">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="62b99-156">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-156">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                               |                                                                                                                                           |
| <span data-ttu-id="62b99-157">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-157">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="62b99-158">public int id()</span><span class="sxs-lookup"><span data-stu-id="62b99-158">public int id()</span></span>                                                                                             | <span data-ttu-id="62b99-159">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="62b99-159">Retrieves the ID of the control.</span></span>                                                                                                          |
| <span data-ttu-id="62b99-160">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="62b99-160">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="62b99-161">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="62b99-161">Retrieves a value that indicates whether the control is a container control.</span></span>                                                              |
| <span data-ttu-id="62b99-162">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-162">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="62b99-163">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-163">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="62b99-164">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-164">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="62b99-165">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-165">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="62b99-166">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-166">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="62b99-167">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-167">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="62b99-168">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-168">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="62b99-169">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-169">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="62b99-170">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-170">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="62b99-171">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-171">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                           |
| <span data-ttu-id="62b99-172">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="62b99-172">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                           |
| <span data-ttu-id="62b99-173">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-173">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="62b99-174">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-174">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="62b99-175">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-175">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                           |
| <span data-ttu-id="62b99-176">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-176">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="62b99-177">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-177">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                           |
| <span data-ttu-id="62b99-178">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="62b99-178">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="62b99-179">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-179">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="62b99-180">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-180">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="62b99-181">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="62b99-181">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="62b99-182">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-182">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="62b99-183">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-183">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="62b99-184">public boolean mandatory(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-184">public boolean mandatory(\[boolean value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="62b99-185">public int moveControl(int controlId, \[int insertAfterControlId\])</span><span class="sxs-lookup"><span data-stu-id="62b99-185">public int moveControl(int controlId, \[int insertAfterControlId\])</span></span>                                         | <span data-ttu-id="62b99-186">コントロールに指定されたコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="62b99-186">Moves a specified control to the control.</span></span>                                                                                                 |
| <span data-ttu-id="62b99-187">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-187">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="62b99-188">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-188">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="62b99-189">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-189">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="62b99-190">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-190">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                           |
| <span data-ttu-id="62b99-191">public FieldId referenceField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-191">public FieldId referenceField(\[FieldId value\])</span></span>                                                            |                                                                                                                                           |
| <span data-ttu-id="62b99-192">public str replacementFieldGroup(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-192">public str replacementFieldGroup(\[str value\])</span></span>                                                             |                                                                                                                                           |
| <span data-ttu-id="62b99-193">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-193">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                           |
| <span data-ttu-id="62b99-194">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-194">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="62b99-195">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-195">public boolean skip(\[boolean value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="62b99-196">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-196">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                           |
| <span data-ttu-id="62b99-197">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="62b99-197">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="62b99-198">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-198">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                           |
| <span data-ttu-id="62b99-199">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-199">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="62b99-200">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-200">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="62b99-201">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-201">public boolean underline(\[boolean value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="62b99-202">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-202">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="62b99-203">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-203">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="62b99-204">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-204">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="62b99-205">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-205">public boolean useUserLayout(\[boolean value\])</span></span>                                                             |                                                                                                                                           |
| <span data-ttu-id="62b99-206">public Int64 value(\[Int64 value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-206">public Int64 value(\[Int64 value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="62b99-207">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="62b99-207">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                           |
| <span data-ttu-id="62b99-208">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="62b99-208">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="62b99-209">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-209">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="62b99-210">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-210">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="62b99-211">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-211">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="62b99-212">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="62b99-212">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="62b99-213">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-213">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="62b99-214">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-214">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="62b99-215">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-215">Gets or sets the calculation mode of the width of the control.</span></span>                                                                            |
| <span data-ttu-id="62b99-216">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="62b99-216">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="62b99-217">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-217">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="62b99-218">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="62b99-218">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                           |

## <a name="method-aligncontrol"></a><span data-ttu-id="62b99-219">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="62b99-219">Method alignControl</span></span>

<span data-ttu-id="62b99-220">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-220">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="62b99-221">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="62b99-221">Parameters - alignControl</span></span>

<span data-ttu-id="62b99-222">値</span><span class="sxs-lookup"><span data-stu-id="62b99-222">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="62b99-223">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="62b99-223">Return Value - alignControl</span></span>

<span data-ttu-id="62b99-224">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="62b99-224">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="62b99-225">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="62b99-225">Remarks - alignControl</span></span>

<span data-ttu-id="62b99-226">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="62b99-226">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="62b99-227">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="62b99-227">Method allowEdit</span></span>

<span data-ttu-id="62b99-228">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-228">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="62b99-229">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="62b99-229">Parameters - allowEdit</span></span>

<span data-ttu-id="62b99-230">値</span><span class="sxs-lookup"><span data-stu-id="62b99-230">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="62b99-231">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="62b99-231">Return Value - allowEdit</span></span>

<span data-ttu-id="62b99-232">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="62b99-232">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="62b99-233">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="62b99-233">Remarks - allowEdit</span></span>

<span data-ttu-id="62b99-234">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="62b99-234">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="62b99-235">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="62b99-235">Method autoDeclaration</span></span>

<span data-ttu-id="62b99-236">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-236">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="62b99-237">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="62b99-237">Parameters - autoDeclaration</span></span>

<span data-ttu-id="62b99-238">値</span><span class="sxs-lookup"><span data-stu-id="62b99-238">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="62b99-239">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="62b99-239">Return Value - autoDeclaration</span></span>

<span data-ttu-id="62b99-240">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="62b99-240">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="62b99-241">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="62b99-241">Remarks - autoDeclaration</span></span>

<span data-ttu-id="62b99-242">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="62b99-242">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="62b99-243">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="62b99-243">Method backgroundColor</span></span>

<span data-ttu-id="62b99-244">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-244">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="62b99-245">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="62b99-245">Parameters - backgroundColor</span></span>

<span data-ttu-id="62b99-246">値</span><span class="sxs-lookup"><span data-stu-id="62b99-246">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="62b99-247">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="62b99-247">Return Value - backgroundColor</span></span>

<span data-ttu-id="62b99-248">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="62b99-248">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="62b99-249">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="62b99-249">Remarks - backgroundColor</span></span>

<span data-ttu-id="62b99-250">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="62b99-250">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="62b99-251">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="62b99-251">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="62b99-252">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="62b99-252">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="62b99-253">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="62b99-253">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="62b99-254">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="62b99-254">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="62b99-255">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="62b99-255">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="62b99-256">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="62b99-256">Method backStyle</span></span>

<span data-ttu-id="62b99-257">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-257">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="62b99-258">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="62b99-258">Parameters - backStyle</span></span>

<span data-ttu-id="62b99-259">値</span><span class="sxs-lookup"><span data-stu-id="62b99-259">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="62b99-260">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="62b99-260">Return Value - backStyle</span></span>

<span data-ttu-id="62b99-261">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="62b99-261">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="62b99-262">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="62b99-262">Method bold</span></span>

<span data-ttu-id="62b99-263">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-263">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="62b99-264">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="62b99-264">Parameters - bold</span></span>

<span data-ttu-id="62b99-265">値</span><span class="sxs-lookup"><span data-stu-id="62b99-265">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="62b99-266">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="62b99-266">Return Value - bold</span></span>

<span data-ttu-id="62b99-267">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="62b99-267">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="62b99-268">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="62b99-268">Remarks - bold</span></span>

<span data-ttu-id="62b99-269">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="62b99-269">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="62b99-270">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="62b99-270">0 Use the default font weight.</span></span>
-   <span data-ttu-id="62b99-271">1 シン。</span><span class="sxs-lookup"><span data-stu-id="62b99-271">1 Thin.</span></span>
-   <span data-ttu-id="62b99-272">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="62b99-272">2 Extra-light.</span></span>
-   <span data-ttu-id="62b99-273">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="62b99-273">3 Light.</span></span>
-   <span data-ttu-id="62b99-274">4 標準。</span><span class="sxs-lookup"><span data-stu-id="62b99-274">4 Normal.</span></span>
-   <span data-ttu-id="62b99-275">5 中。</span><span class="sxs-lookup"><span data-stu-id="62b99-275">5 Medium.</span></span>
-   <span data-ttu-id="62b99-276">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="62b99-276">6 Semibold.</span></span>
-   <span data-ttu-id="62b99-277">7 太字。</span><span class="sxs-lookup"><span data-stu-id="62b99-277">7 Bold.</span></span>
-   <span data-ttu-id="62b99-278">8 極太。</span><span class="sxs-lookup"><span data-stu-id="62b99-278">8 Extra-bold.</span></span>
-   <span data-ttu-id="62b99-279">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="62b99-279">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="62b99-280">メソッド border</span><span class="sxs-lookup"><span data-stu-id="62b99-280">Method border</span></span>

<span data-ttu-id="62b99-281">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-281">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="62b99-282">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="62b99-282">Parameters - border</span></span>

<span data-ttu-id="62b99-283">値</span><span class="sxs-lookup"><span data-stu-id="62b99-283">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="62b99-284">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="62b99-284">Return Value - border</span></span>

<span data-ttu-id="62b99-285">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="62b99-285">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="62b99-286">備考 - border</span><span class="sxs-lookup"><span data-stu-id="62b99-286">Remarks - border</span></span>

<span data-ttu-id="62b99-287">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="62b99-287">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="62b99-288">値です。</span><span class="sxs-lookup"><span data-stu-id="62b99-288">Value.</span></span> | <span data-ttu-id="62b99-289">説明。</span><span class="sxs-lookup"><span data-stu-id="62b99-289">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="62b99-290">0</span><span class="sxs-lookup"><span data-stu-id="62b99-290">0</span></span>      | <span data-ttu-id="62b99-291">自動。</span><span class="sxs-lookup"><span data-stu-id="62b99-291">Auto.</span></span>        |
| <span data-ttu-id="62b99-292">1</span><span class="sxs-lookup"><span data-stu-id="62b99-292">1</span></span>      | <span data-ttu-id="62b99-293">3D。</span><span class="sxs-lookup"><span data-stu-id="62b99-293">3D.</span></span>          |
| <span data-ttu-id="62b99-294">2</span><span class="sxs-lookup"><span data-stu-id="62b99-294">2</span></span>      | <span data-ttu-id="62b99-295">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="62b99-295">Single line.</span></span> |
| <span data-ttu-id="62b99-296">3</span><span class="sxs-lookup"><span data-stu-id="62b99-296">3</span></span>      | <span data-ttu-id="62b99-297">均一。</span><span class="sxs-lookup"><span data-stu-id="62b99-297">Flat.</span></span>        |
| <span data-ttu-id="62b99-298">4</span><span class="sxs-lookup"><span data-stu-id="62b99-298">4</span></span>      | <span data-ttu-id="62b99-299">なし。</span><span class="sxs-lookup"><span data-stu-id="62b99-299">None.</span></span>        |

## <a name="method-characterset"></a><span data-ttu-id="62b99-300">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="62b99-300">Method characterSet</span></span>

<span data-ttu-id="62b99-301">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-301">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="62b99-302">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="62b99-302">Parameters - characterSet</span></span>

<span data-ttu-id="62b99-303">値</span><span class="sxs-lookup"><span data-stu-id="62b99-303">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="62b99-304">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="62b99-304">Return Value - characterSet</span></span>

<span data-ttu-id="62b99-305">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="62b99-305">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="62b99-306">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="62b99-306">Remarks - characterSet</span></span>

<span data-ttu-id="62b99-307">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="62b99-307">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="62b99-308">値です。</span><span class="sxs-lookup"><span data-stu-id="62b99-308">Value.</span></span> | <span data-ttu-id="62b99-309">説明。</span><span class="sxs-lookup"><span data-stu-id="62b99-309">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="62b99-310">0</span><span class="sxs-lookup"><span data-stu-id="62b99-310">0</span></span>      | <span data-ttu-id="62b99-311">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="62b99-311">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="62b99-312">1</span><span class="sxs-lookup"><span data-stu-id="62b99-312">1</span></span>      | <span data-ttu-id="62b99-313">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="62b99-313">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="62b99-314">2</span><span class="sxs-lookup"><span data-stu-id="62b99-314">2</span></span>      | <span data-ttu-id="62b99-315">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="62b99-315">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="62b99-316">77</span><span class="sxs-lookup"><span data-stu-id="62b99-316">77</span></span>     | <span data-ttu-id="62b99-317">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="62b99-317">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="62b99-318">128</span><span class="sxs-lookup"><span data-stu-id="62b99-318">128</span></span>    | <span data-ttu-id="62b99-319">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="62b99-319">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="62b99-320">129</span><span class="sxs-lookup"><span data-stu-id="62b99-320">129</span></span>    | <span data-ttu-id="62b99-321">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="62b99-321">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="62b99-322">134</span><span class="sxs-lookup"><span data-stu-id="62b99-322">134</span></span>    | <span data-ttu-id="62b99-323">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="62b99-323">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="62b99-324">136</span><span class="sxs-lookup"><span data-stu-id="62b99-324">136</span></span>    | <span data-ttu-id="62b99-325">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="62b99-325">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="62b99-326">161</span><span class="sxs-lookup"><span data-stu-id="62b99-326">161</span></span>    | <span data-ttu-id="62b99-327">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="62b99-327">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="62b99-328">162</span><span class="sxs-lookup"><span data-stu-id="62b99-328">162</span></span>    | <span data-ttu-id="62b99-329">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="62b99-329">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="62b99-330">163</span><span class="sxs-lookup"><span data-stu-id="62b99-330">163</span></span>    | <span data-ttu-id="62b99-331">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="62b99-331">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="62b99-332">186</span><span class="sxs-lookup"><span data-stu-id="62b99-332">186</span></span>    | <span data-ttu-id="62b99-333">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="62b99-333">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="62b99-334">204</span><span class="sxs-lookup"><span data-stu-id="62b99-334">204</span></span>    | <span data-ttu-id="62b99-335">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="62b99-335">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="62b99-336">238</span><span class="sxs-lookup"><span data-stu-id="62b99-336">238</span></span>    | <span data-ttu-id="62b99-337">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="62b99-337">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="62b99-338">255</span><span class="sxs-lookup"><span data-stu-id="62b99-338">255</span></span>    | <span data-ttu-id="62b99-339">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="62b99-339">OEM\_CHARSET</span></span>         |

<span data-ttu-id="62b99-340">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="62b99-340">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="62b99-341">値です。</span><span class="sxs-lookup"><span data-stu-id="62b99-341">Value.</span></span> | <span data-ttu-id="62b99-342">説明。</span><span class="sxs-lookup"><span data-stu-id="62b99-342">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="62b99-343">130</span><span class="sxs-lookup"><span data-stu-id="62b99-343">130</span></span>    | <span data-ttu-id="62b99-344">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="62b99-344">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="62b99-345">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="62b99-345">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="62b99-346">値です。</span><span class="sxs-lookup"><span data-stu-id="62b99-346">Value.</span></span> | <span data-ttu-id="62b99-347">説明。</span><span class="sxs-lookup"><span data-stu-id="62b99-347">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="62b99-348">177</span><span class="sxs-lookup"><span data-stu-id="62b99-348">177</span></span>    | <span data-ttu-id="62b99-349">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="62b99-349">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="62b99-350">178</span><span class="sxs-lookup"><span data-stu-id="62b99-350">178</span></span>    | <span data-ttu-id="62b99-351">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="62b99-351">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="62b99-352">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="62b99-352">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="62b99-353">値です。</span><span class="sxs-lookup"><span data-stu-id="62b99-353">Value.</span></span> | <span data-ttu-id="62b99-354">説明。</span><span class="sxs-lookup"><span data-stu-id="62b99-354">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="62b99-355">222</span><span class="sxs-lookup"><span data-stu-id="62b99-355">222</span></span>    | <span data-ttu-id="62b99-356">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="62b99-356">THAI\_CHARSET</span></span> |

<span data-ttu-id="62b99-357">既定の文字セットは、現在のシステム ロケールに基づく値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="62b99-357">The default character set is set to a value that is based on the current system locale.</span></span> <span data-ttu-id="62b99-358">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="62b99-358">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="62b99-359">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="62b99-359">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="62b99-360">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="62b99-360">Method colorScheme</span></span>

<span data-ttu-id="62b99-361">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-361">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="62b99-362">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="62b99-362">Parameters - colorScheme</span></span>

<span data-ttu-id="62b99-363">値</span><span class="sxs-lookup"><span data-stu-id="62b99-363">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="62b99-364">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="62b99-364">Return Value - colorScheme</span></span>

<span data-ttu-id="62b99-365">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="62b99-365">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="62b99-366">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="62b99-366">Remarks - colorScheme</span></span>

<span data-ttu-id="62b99-367">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="62b99-367">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="62b99-368">値です。</span><span class="sxs-lookup"><span data-stu-id="62b99-368">Value.</span></span> | <span data-ttu-id="62b99-369">スタイル。</span><span class="sxs-lookup"><span data-stu-id="62b99-369">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="62b99-370">0</span><span class="sxs-lookup"><span data-stu-id="62b99-370">0</span></span>      | <span data-ttu-id="62b99-371">既定。</span><span class="sxs-lookup"><span data-stu-id="62b99-371">Default.</span></span>                      |
| <span data-ttu-id="62b99-372">1</span><span class="sxs-lookup"><span data-stu-id="62b99-372">1</span></span>      | <span data-ttu-id="62b99-373">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="62b99-373">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="62b99-374">2</span><span class="sxs-lookup"><span data-stu-id="62b99-374">2</span></span>      | <span data-ttu-id="62b99-375">真の配色。</span><span class="sxs-lookup"><span data-stu-id="62b99-375">The true-color scheme.</span></span>        |

## <a name="method-configurationkey"></a><span data-ttu-id="62b99-376">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="62b99-376">Method configurationKey</span></span>

<span data-ttu-id="62b99-377">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-377">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="62b99-378">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="62b99-378">Parameters - configurationKey</span></span>

<span data-ttu-id="62b99-379">値</span><span class="sxs-lookup"><span data-stu-id="62b99-379">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="62b99-380">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="62b99-380">Return Value - configurationKey</span></span>

<span data-ttu-id="62b99-381">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="62b99-381">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="62b99-382">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="62b99-382">Remarks - configurationKey</span></span>

<span data-ttu-id="62b99-383">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="62b99-383">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="62b99-384">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="62b99-384">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="62b99-385">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="62b99-385">Method containerId</span></span>

<span data-ttu-id="62b99-386">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="62b99-386">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="62b99-387">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="62b99-387">Return Value - containerId</span></span>

<span data-ttu-id="62b99-388">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="62b99-388">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="62b99-389">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="62b99-389">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="62b99-390">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="62b99-390">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="62b99-391">値</span><span class="sxs-lookup"><span data-stu-id="62b99-391">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="62b99-392">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="62b99-392">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="62b99-393">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="62b99-393">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="62b99-394">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="62b99-394">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="62b99-395">値</span><span class="sxs-lookup"><span data-stu-id="62b99-395">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="62b99-396">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="62b99-396">Return Value - countryRegionContextField</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="62b99-397">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="62b99-397">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="62b99-398">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="62b99-398">Parameters - dataRelationPath</span></span>

<span data-ttu-id="62b99-399">値</span><span class="sxs-lookup"><span data-stu-id="62b99-399">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="62b99-400">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="62b99-400">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="62b99-401">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="62b99-401">Method dataSource</span></span>

<span data-ttu-id="62b99-402">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-402">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="62b99-403">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="62b99-403">Parameters - dataSource</span></span>

<span data-ttu-id="62b99-404">値</span><span class="sxs-lookup"><span data-stu-id="62b99-404">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="62b99-405">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="62b99-405">Return Value - dataSource</span></span>

<span data-ttu-id="62b99-406">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="62b99-406">The identifier of the data source that will be used.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="62b99-407">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="62b99-407">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="62b99-408">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="62b99-408">Parameters - displayTarget</span></span>

<span data-ttu-id="62b99-409">値</span><span class="sxs-lookup"><span data-stu-id="62b99-409">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="62b99-410">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="62b99-410">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="62b99-411">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="62b99-411">Method dragDrop</span></span>

<span data-ttu-id="62b99-412">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-412">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="62b99-413">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="62b99-413">Parameters - dragDrop</span></span>

<span data-ttu-id="62b99-414">値</span><span class="sxs-lookup"><span data-stu-id="62b99-414">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="62b99-415">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="62b99-415">Return Value - dragDrop</span></span>

<span data-ttu-id="62b99-416">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="62b99-416">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="62b99-417">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="62b99-417">Method enabled</span></span>

<span data-ttu-id="62b99-418">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-418">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="62b99-419">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="62b99-419">Parameters - enabled</span></span>

<span data-ttu-id="62b99-420">値</span><span class="sxs-lookup"><span data-stu-id="62b99-420">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="62b99-421">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="62b99-421">Return Value - enabled</span></span>

<span data-ttu-id="62b99-422">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="62b99-422">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="62b99-423">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="62b99-423">Remarks - enabled</span></span>

<span data-ttu-id="62b99-424">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="62b99-424">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="62b99-425">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="62b99-425">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="62b99-426">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="62b99-426">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="62b99-427">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="62b99-427">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="62b99-428">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="62b99-428">Parameters - extendedDataType</span></span>

<span data-ttu-id="62b99-429">値</span><span class="sxs-lookup"><span data-stu-id="62b99-429">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="62b99-430">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="62b99-430">Return Value - extendedDataType</span></span>

## <a name="method-font"></a><span data-ttu-id="62b99-431">メソッド font</span><span class="sxs-lookup"><span data-stu-id="62b99-431">Method font</span></span>

<span data-ttu-id="62b99-432">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-432">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="62b99-433">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="62b99-433">Parameters - font</span></span>

<span data-ttu-id="62b99-434">値</span><span class="sxs-lookup"><span data-stu-id="62b99-434">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="62b99-435">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="62b99-435">Return Value - font</span></span>

<span data-ttu-id="62b99-436">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="62b99-436">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="62b99-437">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="62b99-437">Method fontSize</span></span>

<span data-ttu-id="62b99-438">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-438">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="62b99-439">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="62b99-439">Parameters - fontSize</span></span>

<span data-ttu-id="62b99-440">値</span><span class="sxs-lookup"><span data-stu-id="62b99-440">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="62b99-441">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="62b99-441">Return Value - fontSize</span></span>

<span data-ttu-id="62b99-442">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="62b99-442">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="62b99-443">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="62b99-443">Method foregroundColor</span></span>

<span data-ttu-id="62b99-444">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-444">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="62b99-445">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="62b99-445">Parameters - foregroundColor</span></span>

<span data-ttu-id="62b99-446">値</span><span class="sxs-lookup"><span data-stu-id="62b99-446">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="62b99-447">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="62b99-447">Return Value - foregroundColor</span></span>

<span data-ttu-id="62b99-448">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="62b99-448">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="62b99-449">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="62b99-449">Remarks - foregroundColor</span></span>

<span data-ttu-id="62b99-450">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="62b99-450">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="62b99-451">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="62b99-451">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="62b99-452">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="62b99-452">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="62b99-453">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="62b99-453">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="62b99-454">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="62b99-454">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="62b99-455">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="62b99-455">The maximum value for a single byte is 255.</span></span>

## <a name="method-height"></a><span data-ttu-id="62b99-456">メソッド height</span><span class="sxs-lookup"><span data-stu-id="62b99-456">Method height</span></span>

<span data-ttu-id="62b99-457">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-457">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="62b99-458">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="62b99-458">Parameters - height</span></span>

<span data-ttu-id="62b99-459">値</span><span class="sxs-lookup"><span data-stu-id="62b99-459">value</span></span>  

<!-- -->

<span data-ttu-id="62b99-460">モード</span><span class="sxs-lookup"><span data-stu-id="62b99-460">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="62b99-461">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="62b99-461">Return Value - height</span></span>

<span data-ttu-id="62b99-462">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="62b99-462">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="62b99-463">備考 - height</span><span class="sxs-lookup"><span data-stu-id="62b99-463">Remarks - height</span></span>

<span data-ttu-id="62b99-464">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="62b99-464">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="62b99-465">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="62b99-465">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="62b99-466">モード。</span><span class="sxs-lookup"><span data-stu-id="62b99-466">Mode.</span></span>            | <span data-ttu-id="62b99-467">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="62b99-467">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="62b99-468">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="62b99-468">-1 Exact.</span></span>        | <span data-ttu-id="62b99-469">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="62b99-469">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="62b99-470">0 自動。</span><span class="sxs-lookup"><span data-stu-id="62b99-470">0 Auto.</span></span>          | <span data-ttu-id="62b99-471">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="62b99-471">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="62b99-472">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="62b99-472">1 Column height.</span></span> | <span data-ttu-id="62b99-473">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="62b99-473">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="62b99-474">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="62b99-474">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="62b99-475">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="62b99-475">Method heightMode</span></span>

<span data-ttu-id="62b99-476">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-476">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="62b99-477">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="62b99-477">Parameters - heightMode</span></span>

<span data-ttu-id="62b99-478">値</span><span class="sxs-lookup"><span data-stu-id="62b99-478">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="62b99-479">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="62b99-479">Return Value - heightMode</span></span>

<span data-ttu-id="62b99-480">計算モード。</span><span class="sxs-lookup"><span data-stu-id="62b99-480">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="62b99-481">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="62b99-481">Remarks - heightMode</span></span>

<span data-ttu-id="62b99-482">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="62b99-482">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="62b99-483">モード。</span><span class="sxs-lookup"><span data-stu-id="62b99-483">Mode.</span></span>          | <span data-ttu-id="62b99-484">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="62b99-484">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="62b99-485">正確。</span><span class="sxs-lookup"><span data-stu-id="62b99-485">Exact.</span></span>         | <span data-ttu-id="62b99-486">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="62b99-486">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="62b99-487">自動。</span><span class="sxs-lookup"><span data-stu-id="62b99-487">Auto.</span></span>          | <span data-ttu-id="62b99-488">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="62b99-488">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="62b99-489">列の高さ</span><span class="sxs-lookup"><span data-stu-id="62b99-489">Column height.</span></span> | <span data-ttu-id="62b99-490">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="62b99-490">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="62b99-491">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="62b99-491">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="62b99-492">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="62b99-492">Method heightValue</span></span>

<span data-ttu-id="62b99-493">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-493">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="62b99-494">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="62b99-494">Parameters - heightValue</span></span>

<span data-ttu-id="62b99-495">値</span><span class="sxs-lookup"><span data-stu-id="62b99-495">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="62b99-496">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="62b99-496">Return Value - heightValue</span></span>

<span data-ttu-id="62b99-497">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="62b99-497">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="62b99-498">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="62b99-498">Remarks - heightValue</span></span>

<span data-ttu-id="62b99-499">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="62b99-499">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="62b99-500">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="62b99-500">Method helpText</span></span>

<span data-ttu-id="62b99-501">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-501">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="62b99-502">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="62b99-502">Parameters - helpText</span></span>

<span data-ttu-id="62b99-503">値</span><span class="sxs-lookup"><span data-stu-id="62b99-503">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="62b99-504">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="62b99-504">Return Value - helpText</span></span>

<span data-ttu-id="62b99-505">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="62b99-505">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="62b99-506">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="62b99-506">Remarks - helpText</span></span>

<span data-ttu-id="62b99-507">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-507">Set the HelpText property for an object by using the property dialogue box.</span></span> <span data-ttu-id="62b99-508">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="62b99-508">The help text must not exceed 250 characters.</span></span>

## <a name="method-hideifempty"></a><span data-ttu-id="62b99-509">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="62b99-509">Method hideIfEmpty</span></span>

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a><span data-ttu-id="62b99-510">パラメーター - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="62b99-510">Parameters - hideIfEmpty</span></span>

<span data-ttu-id="62b99-511">値</span><span class="sxs-lookup"><span data-stu-id="62b99-511">value</span></span>  

### <a name="return-value---hideifempty"></a><span data-ttu-id="62b99-512">戻り値 - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="62b99-512">Return Value - hideIfEmpty</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="62b99-513">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="62b99-513">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="62b99-514">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="62b99-514">Parameters - hierarchyParent</span></span>

<span data-ttu-id="62b99-515">値</span><span class="sxs-lookup"><span data-stu-id="62b99-515">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="62b99-516">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="62b99-516">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="62b99-517">メソッド id</span><span class="sxs-lookup"><span data-stu-id="62b99-517">Method id</span></span>

<span data-ttu-id="62b99-518">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="62b99-518">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="62b99-519">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="62b99-519">Return Value - id</span></span>

<span data-ttu-id="62b99-520">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="62b99-520">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="62b99-521">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="62b99-521">Method isContainer</span></span>

<span data-ttu-id="62b99-522">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="62b99-522">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="62b99-523">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="62b99-523">Return Value - isContainer</span></span>

<span data-ttu-id="62b99-524">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="62b99-524">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-italic"></a><span data-ttu-id="62b99-525">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="62b99-525">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="62b99-526">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="62b99-526">Parameters - italic</span></span>

<span data-ttu-id="62b99-527">値</span><span class="sxs-lookup"><span data-stu-id="62b99-527">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="62b99-528">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="62b99-528">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="62b99-529">メソッド label</span><span class="sxs-lookup"><span data-stu-id="62b99-529">Method label</span></span>

<span data-ttu-id="62b99-530">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-530">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="62b99-531">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="62b99-531">Parameters - label</span></span>

<span data-ttu-id="62b99-532">値</span><span class="sxs-lookup"><span data-stu-id="62b99-532">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="62b99-533">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="62b99-533">Return Value - label</span></span>

<span data-ttu-id="62b99-534">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="62b99-534">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="62b99-535">備考 - label</span><span class="sxs-lookup"><span data-stu-id="62b99-535">Remarks - label</span></span>

<span data-ttu-id="62b99-536">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-536">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="62b99-537">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="62b99-537">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="62b99-538">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="62b99-538">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="62b99-539">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="62b99-539">Parameters - labelAlignment</span></span>

<span data-ttu-id="62b99-540">値</span><span class="sxs-lookup"><span data-stu-id="62b99-540">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="62b99-541">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="62b99-541">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="62b99-542">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="62b99-542">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="62b99-543">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="62b99-543">Parameters - labelBold</span></span>

<span data-ttu-id="62b99-544">値</span><span class="sxs-lookup"><span data-stu-id="62b99-544">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="62b99-545">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="62b99-545">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="62b99-546">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="62b99-546">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="62b99-547">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="62b99-547">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="62b99-548">値</span><span class="sxs-lookup"><span data-stu-id="62b99-548">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="62b99-549">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="62b99-549">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="62b99-550">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="62b99-550">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="62b99-551">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="62b99-551">Parameters - labelFont</span></span>

<span data-ttu-id="62b99-552">値</span><span class="sxs-lookup"><span data-stu-id="62b99-552">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="62b99-553">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="62b99-553">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="62b99-554">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="62b99-554">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="62b99-555">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="62b99-555">Parameters - labelFontSize</span></span>

<span data-ttu-id="62b99-556">値</span><span class="sxs-lookup"><span data-stu-id="62b99-556">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="62b99-557">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="62b99-557">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="62b99-558">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="62b99-558">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="62b99-559">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="62b99-559">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="62b99-560">値</span><span class="sxs-lookup"><span data-stu-id="62b99-560">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="62b99-561">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="62b99-561">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="62b99-562">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="62b99-562">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="62b99-563">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="62b99-563">Parameters - labelGuide</span></span>

<span data-ttu-id="62b99-564">値</span><span class="sxs-lookup"><span data-stu-id="62b99-564">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="62b99-565">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="62b99-565">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="62b99-566">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="62b99-566">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="62b99-567">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="62b99-567">Parameters - labelHeight</span></span>

<span data-ttu-id="62b99-568">値</span><span class="sxs-lookup"><span data-stu-id="62b99-568">value</span></span>  

<!-- -->

<span data-ttu-id="62b99-569">モード</span><span class="sxs-lookup"><span data-stu-id="62b99-569">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="62b99-570">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="62b99-570">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="62b99-571">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="62b99-571">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="62b99-572">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="62b99-572">Parameters - labelHeightMode</span></span>

<span data-ttu-id="62b99-573">値</span><span class="sxs-lookup"><span data-stu-id="62b99-573">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="62b99-574">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="62b99-574">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="62b99-575">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="62b99-575">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="62b99-576">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="62b99-576">Parameters - labelHeightValue</span></span>

<span data-ttu-id="62b99-577">値</span><span class="sxs-lookup"><span data-stu-id="62b99-577">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="62b99-578">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="62b99-578">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="62b99-579">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="62b99-579">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="62b99-580">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="62b99-580">Parameters - labelItalic</span></span>

<span data-ttu-id="62b99-581">値</span><span class="sxs-lookup"><span data-stu-id="62b99-581">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="62b99-582">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="62b99-582">Return Value - labelItalic</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="62b99-583">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="62b99-583">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="62b99-584">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="62b99-584">Parameters - labelPosition</span></span>

<span data-ttu-id="62b99-585">値</span><span class="sxs-lookup"><span data-stu-id="62b99-585">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="62b99-586">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="62b99-586">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="62b99-587">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="62b99-587">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="62b99-588">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="62b99-588">Parameters - labelUnderline</span></span>

<span data-ttu-id="62b99-589">値</span><span class="sxs-lookup"><span data-stu-id="62b99-589">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="62b99-590">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="62b99-590">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="62b99-591">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="62b99-591">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="62b99-592">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="62b99-592">Parameters - labelWidth</span></span>

<span data-ttu-id="62b99-593">値</span><span class="sxs-lookup"><span data-stu-id="62b99-593">value</span></span>  

<!-- -->

<span data-ttu-id="62b99-594">モード</span><span class="sxs-lookup"><span data-stu-id="62b99-594">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="62b99-595">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="62b99-595">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="62b99-596">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="62b99-596">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="62b99-597">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="62b99-597">Parameters - labelWidthMode</span></span>

<span data-ttu-id="62b99-598">値</span><span class="sxs-lookup"><span data-stu-id="62b99-598">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="62b99-599">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="62b99-599">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="62b99-600">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="62b99-600">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="62b99-601">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="62b99-601">Parameters - labelWidthValue</span></span>

<span data-ttu-id="62b99-602">値</span><span class="sxs-lookup"><span data-stu-id="62b99-602">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="62b99-603">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="62b99-603">Return Value - labelWidthValue</span></span>

## <a name="method-left"></a><span data-ttu-id="62b99-604">メソッド left</span><span class="sxs-lookup"><span data-stu-id="62b99-604">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="62b99-605">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="62b99-605">Parameters - left</span></span>

<span data-ttu-id="62b99-606">値</span><span class="sxs-lookup"><span data-stu-id="62b99-606">value</span></span>  

<!-- -->

<span data-ttu-id="62b99-607">モード</span><span class="sxs-lookup"><span data-stu-id="62b99-607">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="62b99-608">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="62b99-608">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="62b99-609">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="62b99-609">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="62b99-610">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="62b99-610">Parameters - leftMode</span></span>

<span data-ttu-id="62b99-611">値</span><span class="sxs-lookup"><span data-stu-id="62b99-611">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="62b99-612">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="62b99-612">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="62b99-613">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="62b99-613">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="62b99-614">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="62b99-614">Parameters - leftValue</span></span>

<span data-ttu-id="62b99-615">値</span><span class="sxs-lookup"><span data-stu-id="62b99-615">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="62b99-616">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="62b99-616">Return Value - leftValue</span></span>

## <a name="method-mandatory"></a><span data-ttu-id="62b99-617">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="62b99-617">Method mandatory</span></span>

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a><span data-ttu-id="62b99-618">パラメーター - mandatory</span><span class="sxs-lookup"><span data-stu-id="62b99-618">Parameters - mandatory</span></span>

<span data-ttu-id="62b99-619">値</span><span class="sxs-lookup"><span data-stu-id="62b99-619">value</span></span>  

### <a name="return-value---mandatory"></a><span data-ttu-id="62b99-620">戻り値 - mandatory</span><span class="sxs-lookup"><span data-stu-id="62b99-620">Return Value - mandatory</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="62b99-621">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="62b99-621">Method moveControl</span></span>

<span data-ttu-id="62b99-622">コントロールに指定されたコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="62b99-622">Moves a specified control to the control.</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterControlId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="62b99-623">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="62b99-623">Parameters - moveControl</span></span>

<span data-ttu-id="62b99-624">controlId</span><span class="sxs-lookup"><span data-stu-id="62b99-624">controlId</span></span>  

<!-- -->

<span data-ttu-id="62b99-625">insertAfterControlId</span><span class="sxs-lookup"><span data-stu-id="62b99-625">insertAfterControlId</span></span>  

### <a name="return-value---movecontrol"></a><span data-ttu-id="62b99-626">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="62b99-626">Return Value - moveControl</span></span>

<span data-ttu-id="62b99-627">コントロールが正常に移動した場合は 1、それ以外の場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="62b99-627">1 if the control was moved successfully; otherwise, 0.</span></span>

### <a name="remarks---movecontrol"></a><span data-ttu-id="62b99-628">備考 - moveControl</span><span class="sxs-lookup"><span data-stu-id="62b99-628">Remarks - moveControl</span></span>

<span data-ttu-id="62b99-629">一般に、指定したコントロールをコントロールに含めることができ、現在のコンテナーから移動できる場合、このメソッドは成功します。</span><span class="sxs-lookup"><span data-stu-id="62b99-629">In general, if the specified control can be contained in the control and can be moved from the container that it is currently in, this method should succeed.</span></span> <span data-ttu-id="62b99-630">ただし、場合によっては、参照グループ コントロールのインスタンス コントロールなど、コントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="62b99-630">However, in some cases, such as for the reference group control instance, controls cannot be moved.</span></span>

## <a name="method-name"></a><span data-ttu-id="62b99-631">メソッド名</span><span class="sxs-lookup"><span data-stu-id="62b99-631">Method name</span></span>

<span data-ttu-id="62b99-632">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-632">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="62b99-633">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="62b99-633">Parameters - name</span></span>

<span data-ttu-id="62b99-634">値</span><span class="sxs-lookup"><span data-stu-id="62b99-634">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="62b99-635">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="62b99-635">Return Value - name</span></span>

<span data-ttu-id="62b99-636">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="62b99-636">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="62b99-637">備考 - name</span><span class="sxs-lookup"><span data-stu-id="62b99-637">Remarks - name</span></span>

<span data-ttu-id="62b99-638">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="62b99-638">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="62b99-639">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="62b99-639">Begins with a letter.</span></span>
-   <span data-ttu-id="62b99-640">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="62b99-640">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="62b99-641">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="62b99-641">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="62b99-642">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="62b99-642">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="62b99-643">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="62b99-643">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="62b99-644">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="62b99-644">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="62b99-645">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="62b99-645">Parameters - neededPermission</span></span>

<span data-ttu-id="62b99-646">値</span><span class="sxs-lookup"><span data-stu-id="62b99-646">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="62b99-647">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="62b99-647">Return Value - neededPermission</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="62b99-648">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="62b99-648">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="62b99-649">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="62b99-649">Parameters - promptrect</span></span>

<span data-ttu-id="62b99-650">値</span><span class="sxs-lookup"><span data-stu-id="62b99-650">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="62b99-651">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="62b99-651">Return Value - promptrect</span></span>

## <a name="method-referencefield"></a><span data-ttu-id="62b99-652">メソッド referenceField</span><span class="sxs-lookup"><span data-stu-id="62b99-652">Method referenceField</span></span>

```xpp
public FieldId referenceField([FieldId value])
```

### <a name="parameters---referencefield"></a><span data-ttu-id="62b99-653">パラメーター - referenceField</span><span class="sxs-lookup"><span data-stu-id="62b99-653">Parameters - referenceField</span></span>

<span data-ttu-id="62b99-654">値</span><span class="sxs-lookup"><span data-stu-id="62b99-654">value</span></span>  

### <a name="return-value---referencefield"></a><span data-ttu-id="62b99-655">戻り値 - referenceField</span><span class="sxs-lookup"><span data-stu-id="62b99-655">Return Value - referenceField</span></span>

## <a name="method-replacementfieldgroup"></a><span data-ttu-id="62b99-656">メソッド replacementFieldGroup</span><span class="sxs-lookup"><span data-stu-id="62b99-656">Method replacementFieldGroup</span></span>

```xpp
public str replacementFieldGroup([str value])
```

### <a name="parameters---replacementfieldgroup"></a><span data-ttu-id="62b99-657">パラメーター - replacementFieldGroup</span><span class="sxs-lookup"><span data-stu-id="62b99-657">Parameters - replacementFieldGroup</span></span>

<span data-ttu-id="62b99-658">値</span><span class="sxs-lookup"><span data-stu-id="62b99-658">value</span></span>  

### <a name="return-value---replacementfieldgroup"></a><span data-ttu-id="62b99-659">戻り値 - replacementFieldGroup</span><span class="sxs-lookup"><span data-stu-id="62b99-659">Return Value - replacementFieldGroup</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="62b99-660">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="62b99-660">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="62b99-661">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="62b99-661">Parameters - securityKey</span></span>

<span data-ttu-id="62b99-662">値</span><span class="sxs-lookup"><span data-stu-id="62b99-662">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="62b99-663">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="62b99-663">Return Value - securityKey</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="62b99-664">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="62b99-664">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="62b99-665">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="62b99-665">Parameters - showLabel</span></span>

<span data-ttu-id="62b99-666">値</span><span class="sxs-lookup"><span data-stu-id="62b99-666">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="62b99-667">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="62b99-667">Return Value - showLabel</span></span>

## <a name="method-skip"></a><span data-ttu-id="62b99-668">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="62b99-668">Method skip</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="62b99-669">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="62b99-669">Parameters - skip</span></span>

<span data-ttu-id="62b99-670">値</span><span class="sxs-lookup"><span data-stu-id="62b99-670">value</span></span>  

### <a name="return-value---skip"></a><span data-ttu-id="62b99-671">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="62b99-671">Return Value - skip</span></span>

## <a name="method-style"></a><span data-ttu-id="62b99-672">メソッド style</span><span class="sxs-lookup"><span data-stu-id="62b99-672">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="62b99-673">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="62b99-673">Parameters - style</span></span>

<span data-ttu-id="62b99-674">値</span><span class="sxs-lookup"><span data-stu-id="62b99-674">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="62b99-675">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="62b99-675">Return Value - style</span></span>

## <a name="method-top"></a><span data-ttu-id="62b99-676">メソッド top</span><span class="sxs-lookup"><span data-stu-id="62b99-676">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="62b99-677">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="62b99-677">Parameters - top</span></span>

<span data-ttu-id="62b99-678">値</span><span class="sxs-lookup"><span data-stu-id="62b99-678">value</span></span>  

<!-- -->

<span data-ttu-id="62b99-679">モード</span><span class="sxs-lookup"><span data-stu-id="62b99-679">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="62b99-680">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="62b99-680">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="62b99-681">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="62b99-681">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="62b99-682">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="62b99-682">Parameters - topMode</span></span>

<span data-ttu-id="62b99-683">値</span><span class="sxs-lookup"><span data-stu-id="62b99-683">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="62b99-684">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="62b99-684">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="62b99-685">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="62b99-685">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="62b99-686">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="62b99-686">Parameters - topValue</span></span>

<span data-ttu-id="62b99-687">値</span><span class="sxs-lookup"><span data-stu-id="62b99-687">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="62b99-688">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="62b99-688">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="62b99-689">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="62b99-689">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="62b99-690">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="62b99-690">Parameters - type</span></span>

<span data-ttu-id="62b99-691">値</span><span class="sxs-lookup"><span data-stu-id="62b99-691">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="62b99-692">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="62b99-692">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="62b99-693">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="62b99-693">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="62b99-694">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="62b99-694">Parameters - underline</span></span>

<span data-ttu-id="62b99-695">値</span><span class="sxs-lookup"><span data-stu-id="62b99-695">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="62b99-696">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="62b99-696">Return Value - underline</span></span>

## <a name="method-userdata"></a><span data-ttu-id="62b99-697">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="62b99-697">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="62b99-698">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="62b99-698">Parameters - userData</span></span>

<span data-ttu-id="62b99-699">値</span><span class="sxs-lookup"><span data-stu-id="62b99-699">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="62b99-700">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="62b99-700">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="62b99-701">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="62b99-701">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="62b99-702">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="62b99-702">Parameters - userDataItem</span></span>

<span data-ttu-id="62b99-703">値</span><span class="sxs-lookup"><span data-stu-id="62b99-703">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="62b99-704">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="62b99-704">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="62b99-705">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="62b99-705">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="62b99-706">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="62b99-706">Parameters - userDataItems</span></span>

<span data-ttu-id="62b99-707">値</span><span class="sxs-lookup"><span data-stu-id="62b99-707">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="62b99-708">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="62b99-708">Return Value - userDataItems</span></span>

## <a name="method-useuserlayout"></a><span data-ttu-id="62b99-709">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="62b99-709">Method useUserLayout</span></span>

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a><span data-ttu-id="62b99-710">パラメーター - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="62b99-710">Parameters - useUserLayout</span></span>

<span data-ttu-id="62b99-711">値</span><span class="sxs-lookup"><span data-stu-id="62b99-711">value</span></span>  

### <a name="return-value---useuserlayout"></a><span data-ttu-id="62b99-712">戻り値 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="62b99-712">Return Value - useUserLayout</span></span>

## <a name="method-value"></a><span data-ttu-id="62b99-713">メソッド value</span><span class="sxs-lookup"><span data-stu-id="62b99-713">Method value</span></span>

```xpp
public Int64 value([Int64 value])
```

### <a name="parameters---value"></a><span data-ttu-id="62b99-714">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="62b99-714">Parameters - value</span></span>

<span data-ttu-id="62b99-715">値</span><span class="sxs-lookup"><span data-stu-id="62b99-715">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="62b99-716">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="62b99-716">Return Value - value</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="62b99-717">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="62b99-717">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="62b99-718">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="62b99-718">Parameters - verticalSpacing</span></span>

<span data-ttu-id="62b99-719">値</span><span class="sxs-lookup"><span data-stu-id="62b99-719">value</span></span>  

<!-- -->

<span data-ttu-id="62b99-720">モード</span><span class="sxs-lookup"><span data-stu-id="62b99-720">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="62b99-721">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="62b99-721">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="62b99-722">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="62b99-722">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="62b99-723">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="62b99-723">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="62b99-724">モード</span><span class="sxs-lookup"><span data-stu-id="62b99-724">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="62b99-725">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="62b99-725">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="62b99-726">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="62b99-726">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="62b99-727">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="62b99-727">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="62b99-728">値</span><span class="sxs-lookup"><span data-stu-id="62b99-728">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="62b99-729">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="62b99-729">Return Value - verticalSpacingValue</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="62b99-730">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="62b99-730">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="62b99-731">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="62b99-731">Parameters - viewEditMode</span></span>

<span data-ttu-id="62b99-732">値</span><span class="sxs-lookup"><span data-stu-id="62b99-732">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="62b99-733">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="62b99-733">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="62b99-734">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="62b99-734">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="62b99-735">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="62b99-735">Parameters - visible</span></span>

<span data-ttu-id="62b99-736">値</span><span class="sxs-lookup"><span data-stu-id="62b99-736">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="62b99-737">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="62b99-737">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="62b99-738">メソッド width</span><span class="sxs-lookup"><span data-stu-id="62b99-738">Method width</span></span>

<span data-ttu-id="62b99-739">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-739">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="62b99-740">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="62b99-740">Parameters - width</span></span>

<span data-ttu-id="62b99-741">値</span><span class="sxs-lookup"><span data-stu-id="62b99-741">value</span></span>  

<!-- -->

<span data-ttu-id="62b99-742">モード</span><span class="sxs-lookup"><span data-stu-id="62b99-742">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="62b99-743">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="62b99-743">Return Value - width</span></span>

<span data-ttu-id="62b99-744">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="62b99-744">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="62b99-745">備考 - width</span><span class="sxs-lookup"><span data-stu-id="62b99-745">Remarks - width</span></span>

<span data-ttu-id="62b99-746">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="62b99-746">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="62b99-747">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="62b99-747">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="62b99-748">モード。</span><span class="sxs-lookup"><span data-stu-id="62b99-748">Mode.</span></span>           | <span data-ttu-id="62b99-749">幅計算。</span><span class="sxs-lookup"><span data-stu-id="62b99-749">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="62b99-750">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="62b99-750">-1 Exact.</span></span>       | <span data-ttu-id="62b99-751">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="62b99-751">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="62b99-752">0 自動。</span><span class="sxs-lookup"><span data-stu-id="62b99-752">0 Auto.</span></span>         | <span data-ttu-id="62b99-753">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="62b99-753">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="62b99-754">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="62b99-754">1 Column width.</span></span> | <span data-ttu-id="62b99-755">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="62b99-755">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="62b99-756">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="62b99-756">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="62b99-757">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="62b99-757">Method widthMode</span></span>

<span data-ttu-id="62b99-758">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-758">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="62b99-759">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="62b99-759">Parameters - widthMode</span></span>

<span data-ttu-id="62b99-760">値</span><span class="sxs-lookup"><span data-stu-id="62b99-760">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="62b99-761">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="62b99-761">Return Value - widthMode</span></span>

<span data-ttu-id="62b99-762">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="62b99-762">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="62b99-763">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="62b99-763">Remarks - widthMode</span></span>

<span data-ttu-id="62b99-764">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="62b99-764">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="62b99-765">モード。</span><span class="sxs-lookup"><span data-stu-id="62b99-765">Mode.</span></span>         | <span data-ttu-id="62b99-766">幅計算。</span><span class="sxs-lookup"><span data-stu-id="62b99-766">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="62b99-767">正確。</span><span class="sxs-lookup"><span data-stu-id="62b99-767">Exact.</span></span>        | <span data-ttu-id="62b99-768">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="62b99-768">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="62b99-769">自動。</span><span class="sxs-lookup"><span data-stu-id="62b99-769">Auto.</span></span>         | <span data-ttu-id="62b99-770">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="62b99-770">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="62b99-771">列の幅。</span><span class="sxs-lookup"><span data-stu-id="62b99-771">Column width.</span></span> | <span data-ttu-id="62b99-772">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="62b99-772">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="62b99-773">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="62b99-773">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="62b99-774">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="62b99-774">Method widthValue</span></span>

<span data-ttu-id="62b99-775">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="62b99-775">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="62b99-776">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="62b99-776">Parameters - widthValue</span></span>

<span data-ttu-id="62b99-777">値</span><span class="sxs-lookup"><span data-stu-id="62b99-777">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="62b99-778">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="62b99-778">Return Value - widthValue</span></span>

<span data-ttu-id="62b99-779">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="62b99-779">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="62b99-780">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="62b99-780">Remarks - widthValue</span></span>

<span data-ttu-id="62b99-781">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="62b99-781">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="62b99-782">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="62b99-782">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="62b99-783">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="62b99-783">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="62b99-784">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="62b99-784">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="62b99-785">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="62b99-785">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="62b99-786">overrideObject</span><span class="sxs-lookup"><span data-stu-id="62b99-786">overrideObject</span></span>  

