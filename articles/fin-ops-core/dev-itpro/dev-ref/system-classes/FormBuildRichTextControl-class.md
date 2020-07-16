---
title: FormBuildRichTextControl クラス
description: このトピックでは、FormBuildRichTextControl クラスについて説明します。
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
ms.openlocfilehash: 8cae5be81007fc1a70b5fcbcc21fa5861a814ee3
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502644"
---
# <a name="class-formbuildrichtextcontrol"></a><span data-ttu-id="044da-103">クラス FormBuildRichTextControl</span><span class="sxs-lookup"><span data-stu-id="044da-103">Class FormBuildRichTextControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildRichTextControl extends FormBuildControl
```

## <a name="remarks"></a><span data-ttu-id="044da-104">備考</span><span class="sxs-lookup"><span data-stu-id="044da-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="044da-105">例</span><span class="sxs-lookup"><span data-stu-id="044da-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="044da-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="044da-106">Methods</span></span>

| <span data-ttu-id="044da-107">方法</span><span class="sxs-lookup"><span data-stu-id="044da-107">Method</span></span>                                                                                                      | <span data-ttu-id="044da-108">説明</span><span class="sxs-lookup"><span data-stu-id="044da-108">Description</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="044da-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="044da-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="044da-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="044da-110">Determines whether to align the control.</span></span>                                                                                                  |
| <span data-ttu-id="044da-111">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="044da-111">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="044da-112">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="044da-112">Determines whether the user can change the contents of the control.</span></span>                                                                       |
| <span data-ttu-id="044da-113">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-113">public int arrayIndex(\[int value\])</span></span>                                                                        |                                                                                                                                           |
| <span data-ttu-id="044da-114">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="044da-114">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="044da-115">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="044da-115">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                        |
| <span data-ttu-id="044da-116">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-116">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="044da-117">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-117">Gets or sets the background color of the control.</span></span>                                                                                         |
| <span data-ttu-id="044da-118">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-118">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="044da-119">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="044da-119">Determines whether the control background can be transparent.</span></span>                                                                            |
| <span data-ttu-id="044da-120">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-120">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="044da-121">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-121">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                               |
| <span data-ttu-id="044da-122">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-122">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="044da-123">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-123">Gets or sets the style of the borderline of the control.</span></span>                                                                                  |
| <span data-ttu-id="044da-124">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-124">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="044da-125">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-125">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="044da-126">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-126">Gets or sets the character set of the font.</span></span>                                                                                               |
| <span data-ttu-id="044da-127">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-127">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="044da-128">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-128">Gets or sets the color scheme of the control.</span></span>                                                                                             |
| <span data-ttu-id="044da-129">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="044da-129">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="044da-130">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-130">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                       |
| <span data-ttu-id="044da-131">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="044da-131">public int containerId()</span></span>                                                                                    | <span data-ttu-id="044da-132">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="044da-132">Retrieves the ID of the parent container for the control.</span></span>                                                                                 |
| <span data-ttu-id="044da-133">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="044da-133">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                           |
| <span data-ttu-id="044da-134">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="044da-134">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                           |
| <span data-ttu-id="044da-135">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="044da-135">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="044da-136">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="044da-136">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                           |
| <span data-ttu-id="044da-137">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="044da-137">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="044da-138">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="044da-138">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="044da-139">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-139">Gets or sets a data source that is used by the control or the form.</span></span>                                                                       |
| <span data-ttu-id="044da-140">public int direction(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-140">public int direction(\[int value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="044da-141">public int displayHeight(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="044da-141">public int displayHeight(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                           |
| <span data-ttu-id="044da-142">public AutoMode displayHeightMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="044da-142">public AutoMode displayHeightMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                           |
| <span data-ttu-id="044da-143">public int displayHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-143">public int displayHeightValue(\[int value\])</span></span>                                                                |                                                                                                                                           |
| <span data-ttu-id="044da-144">public int displayLength(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="044da-144">public int displayLength(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                           |
| <span data-ttu-id="044da-145">public AutoMode displayLengthMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="044da-145">public AutoMode displayLengthMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                           |
| <span data-ttu-id="044da-146">public int displayLengthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-146">public int displayLengthValue(\[int value\])</span></span>                                                                |                                                                                                                                           |
| <span data-ttu-id="044da-147">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-147">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="044da-148">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-148">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="044da-149">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="044da-149">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                         |
| <span data-ttu-id="044da-150">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="044da-150">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="044da-151">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="044da-151">Determines whether to enable or disable the object.</span></span>                                                                                       |
| <span data-ttu-id="044da-152">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="044da-152">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                           |
| <span data-ttu-id="044da-153">public int fastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-153">public int fastTabSummary(\[int value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="044da-154">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="044da-154">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="044da-155">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-155">Gets or sets the name of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="044da-156">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-156">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="044da-157">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-157">Gets or sets the size of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="044da-158">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-158">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="044da-159">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-159">Gets or sets the text color for the control to use.</span></span>                                                                                       |
| <span data-ttu-id="044da-160">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="044da-160">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="044da-161">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-161">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="044da-162">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-162">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="044da-163">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-163">Gets or sets a calculation mode for the height of the control.</span></span>                                                                            |
| <span data-ttu-id="044da-164">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-164">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="044da-165">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-165">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="044da-166">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="044da-166">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="044da-167">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-167">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="044da-168">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="044da-168">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="044da-169">public int id()</span><span class="sxs-lookup"><span data-stu-id="044da-169">public int id()</span></span>                                                                                             | <span data-ttu-id="044da-170">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="044da-170">Retrieves the ID of the control.</span></span>                                                                                                          |
| <span data-ttu-id="044da-171">public int iMEMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-171">public int iMEMode(\[int value\])</span></span>                                                                           |                                                                                                                                           |
| <span data-ttu-id="044da-172">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="044da-172">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="044da-173">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="044da-173">Retrieves a value that indicates whether the control is a container control.</span></span>                                                              |
| <span data-ttu-id="044da-174">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="044da-174">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="044da-175">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="044da-175">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="044da-176">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-176">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="044da-177">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-177">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="044da-178">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-178">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="044da-179">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-179">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="044da-180">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="044da-180">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="044da-181">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-181">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="044da-182">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-182">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="044da-183">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-183">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                           |
| <span data-ttu-id="044da-184">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="044da-184">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                           |
| <span data-ttu-id="044da-185">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-185">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="044da-186">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-186">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="044da-187">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="044da-187">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                           |
| <span data-ttu-id="044da-188">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-188">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="044da-189">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="044da-189">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                           |
| <span data-ttu-id="044da-190">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="044da-190">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="044da-191">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-191">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="044da-192">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-192">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="044da-193">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="044da-193">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="044da-194">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-194">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="044da-195">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-195">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="044da-196">public int limitText(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="044da-196">public int limitText(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="044da-197">public AutoMode limitTextMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="044da-197">public AutoMode limitTextMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                           |
| <span data-ttu-id="044da-198">public int limitTextValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-198">public int limitTextValue(\[int value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="044da-199">public int lookupButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-199">public int lookupButton(\[int value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="044da-200">public boolean mandatory(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="044da-200">public boolean mandatory(\[boolean value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="044da-201">public boolean multiLine(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="044da-201">public boolean multiLine(\[boolean value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="044da-202">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="044da-202">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="044da-203">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-203">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="044da-204">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-204">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="044da-205">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-205">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                           |
| <span data-ttu-id="044da-206">public boolean replaceOnLookup(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="044da-206">public boolean replaceOnLookup(\[boolean value\])</span></span>                                                           |                                                                                                                                           |
| <span data-ttu-id="044da-207">public int searchAfterInput(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-207">public int searchAfterInput(\[int value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="044da-208">public int searchMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-208">public int searchMode(\[int value\])</span></span>                                                                        |                                                                                                                                           |
| <span data-ttu-id="044da-209">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="044da-209">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                           |
| <span data-ttu-id="044da-210">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="044da-210">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="044da-211">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="044da-211">public boolean skip(\[boolean value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="044da-212">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-212">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                           |
| <span data-ttu-id="044da-213">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="044da-213">public str text(\[str value\])</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="044da-214">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="044da-214">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="044da-215">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-215">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                           |
| <span data-ttu-id="044da-216">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-216">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="044da-217">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-217">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="044da-218">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="044da-218">public boolean underline(\[boolean value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="044da-219">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-219">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="044da-220">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-220">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="044da-221">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-221">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="044da-222">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="044da-222">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                           |
| <span data-ttu-id="044da-223">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="044da-223">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="044da-224">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-224">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="044da-225">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-225">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="044da-226">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="044da-226">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="044da-227">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="044da-227">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="044da-228">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-228">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="044da-229">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-229">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="044da-230">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-230">Gets or sets the calculation mode of the width of the control.</span></span>                                                                            |
| <span data-ttu-id="044da-231">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="044da-231">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="044da-232">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-232">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="044da-233">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="044da-233">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                           |

## <a name="method-aligncontrol"></a><span data-ttu-id="044da-234">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="044da-234">Method alignControl</span></span>

<span data-ttu-id="044da-235">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="044da-235">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="044da-236">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="044da-236">Parameters - alignControl</span></span>

<span data-ttu-id="044da-237">値</span><span class="sxs-lookup"><span data-stu-id="044da-237">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="044da-238">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="044da-238">Return Value - alignControl</span></span>

<span data-ttu-id="044da-239">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="044da-239">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="044da-240">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="044da-240">Remarks - alignControl</span></span>

<span data-ttu-id="044da-241">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="044da-241">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="044da-242">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="044da-242">Method allowEdit</span></span>

<span data-ttu-id="044da-243">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="044da-243">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="044da-244">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="044da-244">Parameters - allowEdit</span></span>

<span data-ttu-id="044da-245">値</span><span class="sxs-lookup"><span data-stu-id="044da-245">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="044da-246">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="044da-246">Return Value - allowEdit</span></span>

<span data-ttu-id="044da-247">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="044da-247">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="044da-248">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="044da-248">Remarks - allowEdit</span></span>

<span data-ttu-id="044da-249">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="044da-249">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="044da-250">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="044da-250">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="044da-251">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="044da-251">Parameters - arrayIndex</span></span>

<span data-ttu-id="044da-252">値</span><span class="sxs-lookup"><span data-stu-id="044da-252">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="044da-253">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="044da-253">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="044da-254">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="044da-254">Method autoDeclaration</span></span>

<span data-ttu-id="044da-255">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="044da-255">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="044da-256">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="044da-256">Parameters - autoDeclaration</span></span>

<span data-ttu-id="044da-257">値</span><span class="sxs-lookup"><span data-stu-id="044da-257">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="044da-258">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="044da-258">Return Value - autoDeclaration</span></span>

<span data-ttu-id="044da-259">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="044da-259">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="044da-260">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="044da-260">Remarks - autoDeclaration</span></span>

<span data-ttu-id="044da-261">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="044da-261">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="044da-262">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="044da-262">Method backgroundColor</span></span>

<span data-ttu-id="044da-263">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-263">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="044da-264">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="044da-264">Parameters - backgroundColor</span></span>

<span data-ttu-id="044da-265">値</span><span class="sxs-lookup"><span data-stu-id="044da-265">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="044da-266">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="044da-266">Return Value - backgroundColor</span></span>

<span data-ttu-id="044da-267">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="044da-267">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="044da-268">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="044da-268">Remarks - backgroundColor</span></span>

<span data-ttu-id="044da-269">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="044da-269">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="044da-270">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="044da-270">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="044da-271">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="044da-271">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="044da-272">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="044da-272">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="044da-273">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="044da-273">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="044da-274">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="044da-274">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="044da-275">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="044da-275">Method backStyle</span></span>

<span data-ttu-id="044da-276">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="044da-276">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="044da-277">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="044da-277">Parameters - backStyle</span></span>

<span data-ttu-id="044da-278">値</span><span class="sxs-lookup"><span data-stu-id="044da-278">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="044da-279">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="044da-279">Return Value - backStyle</span></span>

<span data-ttu-id="044da-280">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="044da-280">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="044da-281">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="044da-281">Method bold</span></span>

<span data-ttu-id="044da-282">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-282">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="044da-283">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="044da-283">Parameters - bold</span></span>

<span data-ttu-id="044da-284">値</span><span class="sxs-lookup"><span data-stu-id="044da-284">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="044da-285">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="044da-285">Return Value - bold</span></span>

<span data-ttu-id="044da-286">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="044da-286">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="044da-287">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="044da-287">Remarks - bold</span></span>

<span data-ttu-id="044da-288">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="044da-288">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="044da-289">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="044da-289">0 Use the default font weight.</span></span>
-   <span data-ttu-id="044da-290">1 シン。</span><span class="sxs-lookup"><span data-stu-id="044da-290">1 Thin.</span></span>
-   <span data-ttu-id="044da-291">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="044da-291">2 Extra-light.</span></span>
-   <span data-ttu-id="044da-292">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="044da-292">3 Light.</span></span>
-   <span data-ttu-id="044da-293">4 標準。</span><span class="sxs-lookup"><span data-stu-id="044da-293">4 Normal.</span></span>
-   <span data-ttu-id="044da-294">5 中。</span><span class="sxs-lookup"><span data-stu-id="044da-294">5 Medium.</span></span>
-   <span data-ttu-id="044da-295">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="044da-295">6 Semibold.</span></span>
-   <span data-ttu-id="044da-296">7 太字。</span><span class="sxs-lookup"><span data-stu-id="044da-296">7 Bold.</span></span>
-   <span data-ttu-id="044da-297">8 極太。</span><span class="sxs-lookup"><span data-stu-id="044da-297">8 Extra-bold.</span></span>
-   <span data-ttu-id="044da-298">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="044da-298">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="044da-299">メソッド border</span><span class="sxs-lookup"><span data-stu-id="044da-299">Method border</span></span>

<span data-ttu-id="044da-300">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-300">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="044da-301">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="044da-301">Parameters - border</span></span>

<span data-ttu-id="044da-302">値</span><span class="sxs-lookup"><span data-stu-id="044da-302">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="044da-303">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="044da-303">Return Value - border</span></span>

<span data-ttu-id="044da-304">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="044da-304">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="044da-305">備考 - border</span><span class="sxs-lookup"><span data-stu-id="044da-305">Remarks - border</span></span>

<span data-ttu-id="044da-306">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="044da-306">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="044da-307">値です。</span><span class="sxs-lookup"><span data-stu-id="044da-307">Value.</span></span> | <span data-ttu-id="044da-308">説明。</span><span class="sxs-lookup"><span data-stu-id="044da-308">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="044da-309">0</span><span class="sxs-lookup"><span data-stu-id="044da-309">0</span></span>      | <span data-ttu-id="044da-310">自動。</span><span class="sxs-lookup"><span data-stu-id="044da-310">Auto.</span></span>        |
| <span data-ttu-id="044da-311">1</span><span class="sxs-lookup"><span data-stu-id="044da-311">1</span></span>      | <span data-ttu-id="044da-312">3D。</span><span class="sxs-lookup"><span data-stu-id="044da-312">3D.</span></span>          |
| <span data-ttu-id="044da-313">2</span><span class="sxs-lookup"><span data-stu-id="044da-313">2</span></span>      | <span data-ttu-id="044da-314">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="044da-314">Single line.</span></span> |
| <span data-ttu-id="044da-315">3</span><span class="sxs-lookup"><span data-stu-id="044da-315">3</span></span>      | <span data-ttu-id="044da-316">均一。</span><span class="sxs-lookup"><span data-stu-id="044da-316">Flat.</span></span>        |
| <span data-ttu-id="044da-317">4</span><span class="sxs-lookup"><span data-stu-id="044da-317">4</span></span>      | <span data-ttu-id="044da-318">なし。</span><span class="sxs-lookup"><span data-stu-id="044da-318">None.</span></span>        |

## <a name="method-cachedatamethod"></a><span data-ttu-id="044da-319">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="044da-319">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="044da-320">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="044da-320">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="044da-321">値</span><span class="sxs-lookup"><span data-stu-id="044da-321">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="044da-322">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="044da-322">Return Value - cacheDataMethod</span></span>

## <a name="method-characterset"></a><span data-ttu-id="044da-323">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="044da-323">Method characterSet</span></span>

<span data-ttu-id="044da-324">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-324">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="044da-325">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="044da-325">Parameters - characterSet</span></span>

<span data-ttu-id="044da-326">値</span><span class="sxs-lookup"><span data-stu-id="044da-326">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="044da-327">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="044da-327">Return Value - characterSet</span></span>

<span data-ttu-id="044da-328">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="044da-328">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="044da-329">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="044da-329">Remarks - characterSet</span></span>

<span data-ttu-id="044da-330">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="044da-330">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="044da-331">値です。</span><span class="sxs-lookup"><span data-stu-id="044da-331">Value.</span></span> | <span data-ttu-id="044da-332">説明。</span><span class="sxs-lookup"><span data-stu-id="044da-332">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="044da-333">0</span><span class="sxs-lookup"><span data-stu-id="044da-333">0</span></span>      | <span data-ttu-id="044da-334">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="044da-334">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="044da-335">1</span><span class="sxs-lookup"><span data-stu-id="044da-335">1</span></span>      | <span data-ttu-id="044da-336">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="044da-336">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="044da-337">2</span><span class="sxs-lookup"><span data-stu-id="044da-337">2</span></span>      | <span data-ttu-id="044da-338">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="044da-338">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="044da-339">77</span><span class="sxs-lookup"><span data-stu-id="044da-339">77</span></span>     | <span data-ttu-id="044da-340">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="044da-340">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="044da-341">128</span><span class="sxs-lookup"><span data-stu-id="044da-341">128</span></span>    | <span data-ttu-id="044da-342">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="044da-342">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="044da-343">129</span><span class="sxs-lookup"><span data-stu-id="044da-343">129</span></span>    | <span data-ttu-id="044da-344">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="044da-344">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="044da-345">134</span><span class="sxs-lookup"><span data-stu-id="044da-345">134</span></span>    | <span data-ttu-id="044da-346">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="044da-346">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="044da-347">136</span><span class="sxs-lookup"><span data-stu-id="044da-347">136</span></span>    | <span data-ttu-id="044da-348">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="044da-348">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="044da-349">161</span><span class="sxs-lookup"><span data-stu-id="044da-349">161</span></span>    | <span data-ttu-id="044da-350">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="044da-350">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="044da-351">162</span><span class="sxs-lookup"><span data-stu-id="044da-351">162</span></span>    | <span data-ttu-id="044da-352">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="044da-352">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="044da-353">163</span><span class="sxs-lookup"><span data-stu-id="044da-353">163</span></span>    | <span data-ttu-id="044da-354">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="044da-354">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="044da-355">186</span><span class="sxs-lookup"><span data-stu-id="044da-355">186</span></span>    | <span data-ttu-id="044da-356">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="044da-356">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="044da-357">204</span><span class="sxs-lookup"><span data-stu-id="044da-357">204</span></span>    | <span data-ttu-id="044da-358">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="044da-358">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="044da-359">238</span><span class="sxs-lookup"><span data-stu-id="044da-359">238</span></span>    | <span data-ttu-id="044da-360">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="044da-360">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="044da-361">255</span><span class="sxs-lookup"><span data-stu-id="044da-361">255</span></span>    | <span data-ttu-id="044da-362">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="044da-362">OEM\_CHARSET</span></span>         |

<span data-ttu-id="044da-363">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="044da-363">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="044da-364">値です。</span><span class="sxs-lookup"><span data-stu-id="044da-364">Value.</span></span> | <span data-ttu-id="044da-365">説明。</span><span class="sxs-lookup"><span data-stu-id="044da-365">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="044da-366">130</span><span class="sxs-lookup"><span data-stu-id="044da-366">130</span></span>    | <span data-ttu-id="044da-367">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="044da-367">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="044da-368">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="044da-368">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="044da-369">値です。</span><span class="sxs-lookup"><span data-stu-id="044da-369">Value.</span></span> | <span data-ttu-id="044da-370">説明。</span><span class="sxs-lookup"><span data-stu-id="044da-370">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="044da-371">177</span><span class="sxs-lookup"><span data-stu-id="044da-371">177</span></span>    | <span data-ttu-id="044da-372">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="044da-372">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="044da-373">178</span><span class="sxs-lookup"><span data-stu-id="044da-373">178</span></span>    | <span data-ttu-id="044da-374">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="044da-374">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="044da-375">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="044da-375">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="044da-376">値です。</span><span class="sxs-lookup"><span data-stu-id="044da-376">Value.</span></span> | <span data-ttu-id="044da-377">説明。</span><span class="sxs-lookup"><span data-stu-id="044da-377">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="044da-378">222</span><span class="sxs-lookup"><span data-stu-id="044da-378">222</span></span>    | <span data-ttu-id="044da-379">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="044da-379">THAI\_CHARSET</span></span> |

<span data-ttu-id="044da-380">既定の文字セットは、現在のシステム ロケールに基づく値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="044da-380">The default character set is set to a value that is based on the current system locale.</span></span> <span data-ttu-id="044da-381">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="044da-381">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="044da-382">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="044da-382">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="044da-383">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="044da-383">Method colorScheme</span></span>

<span data-ttu-id="044da-384">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-384">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="044da-385">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="044da-385">Parameters - colorScheme</span></span>

<span data-ttu-id="044da-386">値</span><span class="sxs-lookup"><span data-stu-id="044da-386">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="044da-387">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="044da-387">Return Value - colorScheme</span></span>

<span data-ttu-id="044da-388">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="044da-388">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="044da-389">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="044da-389">Remarks - colorScheme</span></span>

<span data-ttu-id="044da-390">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="044da-390">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="044da-391">値です。</span><span class="sxs-lookup"><span data-stu-id="044da-391">Value.</span></span> | <span data-ttu-id="044da-392">スタイル。</span><span class="sxs-lookup"><span data-stu-id="044da-392">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="044da-393">0</span><span class="sxs-lookup"><span data-stu-id="044da-393">0</span></span>      | <span data-ttu-id="044da-394">既定。</span><span class="sxs-lookup"><span data-stu-id="044da-394">Default.</span></span>                      |
| <span data-ttu-id="044da-395">1</span><span class="sxs-lookup"><span data-stu-id="044da-395">1</span></span>      | <span data-ttu-id="044da-396">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="044da-396">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="044da-397">2</span><span class="sxs-lookup"><span data-stu-id="044da-397">2</span></span>      | <span data-ttu-id="044da-398">真の配色。</span><span class="sxs-lookup"><span data-stu-id="044da-398">The true-color scheme.</span></span>        |

## <a name="method-configurationkey"></a><span data-ttu-id="044da-399">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="044da-399">Method configurationKey</span></span>

<span data-ttu-id="044da-400">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-400">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="044da-401">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="044da-401">Parameters - configurationKey</span></span>

<span data-ttu-id="044da-402">値</span><span class="sxs-lookup"><span data-stu-id="044da-402">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="044da-403">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="044da-403">Return Value - configurationKey</span></span>

<span data-ttu-id="044da-404">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="044da-404">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="044da-405">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="044da-405">Remarks - configurationKey</span></span>

<span data-ttu-id="044da-406">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="044da-406">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="044da-407">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="044da-407">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="044da-408">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="044da-408">Method containerId</span></span>

<span data-ttu-id="044da-409">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="044da-409">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="044da-410">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="044da-410">Return Value - containerId</span></span>

<span data-ttu-id="044da-411">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="044da-411">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="044da-412">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="044da-412">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="044da-413">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="044da-413">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="044da-414">値</span><span class="sxs-lookup"><span data-stu-id="044da-414">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="044da-415">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="044da-415">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="044da-416">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="044da-416">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="044da-417">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="044da-417">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="044da-418">値</span><span class="sxs-lookup"><span data-stu-id="044da-418">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="044da-419">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="044da-419">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="044da-420">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="044da-420">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="044da-421">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="044da-421">Parameters - dataField</span></span>

<span data-ttu-id="044da-422">値</span><span class="sxs-lookup"><span data-stu-id="044da-422">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="044da-423">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="044da-423">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="044da-424">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="044da-424">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="044da-425">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="044da-425">Parameters - dataMethod</span></span>

<span data-ttu-id="044da-426">値</span><span class="sxs-lookup"><span data-stu-id="044da-426">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="044da-427">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="044da-427">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="044da-428">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="044da-428">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="044da-429">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="044da-429">Parameters - dataRelationPath</span></span>

<span data-ttu-id="044da-430">値</span><span class="sxs-lookup"><span data-stu-id="044da-430">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="044da-431">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="044da-431">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="044da-432">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="044da-432">Method dataSource</span></span>

<span data-ttu-id="044da-433">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-433">Gets or sets a data source that is used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="044da-434">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="044da-434">Parameters - dataSource</span></span>

<span data-ttu-id="044da-435">値</span><span class="sxs-lookup"><span data-stu-id="044da-435">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="044da-436">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="044da-436">Return Value - dataSource</span></span>

<span data-ttu-id="044da-437">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="044da-437">The identifier of the data source that is used.</span></span>

## <a name="method-direction"></a><span data-ttu-id="044da-438">メソッド direction</span><span class="sxs-lookup"><span data-stu-id="044da-438">Method direction</span></span>

```xpp
public int direction([int value])
```

### <a name="parameters---direction"></a><span data-ttu-id="044da-439">パラメーター - direction</span><span class="sxs-lookup"><span data-stu-id="044da-439">Parameters - direction</span></span>

<span data-ttu-id="044da-440">値</span><span class="sxs-lookup"><span data-stu-id="044da-440">value</span></span>  

### <a name="return-value---direction"></a><span data-ttu-id="044da-441">戻り値 - direction</span><span class="sxs-lookup"><span data-stu-id="044da-441">Return Value - direction</span></span>

## <a name="method-displayheight"></a><span data-ttu-id="044da-442">メソッド displayHeight</span><span class="sxs-lookup"><span data-stu-id="044da-442">Method displayHeight</span></span>

```xpp
public int displayHeight([int value], [AutoMode mode])
```

### <a name="parameters---displayheight"></a><span data-ttu-id="044da-443">パラメーター - displayHeight</span><span class="sxs-lookup"><span data-stu-id="044da-443">Parameters - displayHeight</span></span>

<span data-ttu-id="044da-444">値</span><span class="sxs-lookup"><span data-stu-id="044da-444">value</span></span>  

<!-- -->

<span data-ttu-id="044da-445">モード</span><span class="sxs-lookup"><span data-stu-id="044da-445">mode</span></span>  

### <a name="return-value---displayheight"></a><span data-ttu-id="044da-446">戻り値 - displayHeight</span><span class="sxs-lookup"><span data-stu-id="044da-446">Return Value - displayHeight</span></span>

## <a name="method-displayheightmode"></a><span data-ttu-id="044da-447">メソッド displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="044da-447">Method displayHeightMode</span></span>

```xpp
public AutoMode displayHeightMode([AutoMode mode])
```

### <a name="parameters---displayheightmode"></a><span data-ttu-id="044da-448">パラメーター - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="044da-448">Parameters - displayHeightMode</span></span>

<span data-ttu-id="044da-449">モード</span><span class="sxs-lookup"><span data-stu-id="044da-449">mode</span></span>  

### <a name="return-value---displayheightmode"></a><span data-ttu-id="044da-450">戻り値 - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="044da-450">Return Value - displayHeightMode</span></span>

## <a name="method-displayheightvalue"></a><span data-ttu-id="044da-451">メソッド displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="044da-451">Method displayHeightValue</span></span>

```xpp
public int displayHeightValue([int value])
```

### <a name="parameters---displayheightvalue"></a><span data-ttu-id="044da-452">パラメーター - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="044da-452">Parameters - displayHeightValue</span></span>

<span data-ttu-id="044da-453">値</span><span class="sxs-lookup"><span data-stu-id="044da-453">value</span></span>  

### <a name="return-value---displayheightvalue"></a><span data-ttu-id="044da-454">戻り値 - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="044da-454">Return Value - displayHeightValue</span></span>

## <a name="method-displaylength"></a><span data-ttu-id="044da-455">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="044da-455">Method displayLength</span></span>

```xpp
public int displayLength([int value], [AutoMode mode])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="044da-456">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="044da-456">Parameters - displayLength</span></span>

<span data-ttu-id="044da-457">値</span><span class="sxs-lookup"><span data-stu-id="044da-457">value</span></span>  

<!-- -->

<span data-ttu-id="044da-458">モード</span><span class="sxs-lookup"><span data-stu-id="044da-458">mode</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="044da-459">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="044da-459">Return Value - displayLength</span></span>

## <a name="method-displaylengthmode"></a><span data-ttu-id="044da-460">メソッド displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="044da-460">Method displayLengthMode</span></span>

```xpp
public AutoMode displayLengthMode([AutoMode mode])
```

### <a name="parameters---displaylengthmode"></a><span data-ttu-id="044da-461">パラメーター - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="044da-461">Parameters - displayLengthMode</span></span>

<span data-ttu-id="044da-462">モード</span><span class="sxs-lookup"><span data-stu-id="044da-462">mode</span></span>  

### <a name="return-value---displaylengthmode"></a><span data-ttu-id="044da-463">戻り値 - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="044da-463">Return Value - displayLengthMode</span></span>

## <a name="method-displaylengthvalue"></a><span data-ttu-id="044da-464">メソッド displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="044da-464">Method displayLengthValue</span></span>

```xpp
public int displayLengthValue([int value])
```

### <a name="parameters---displaylengthvalue"></a><span data-ttu-id="044da-465">パラメーター - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="044da-465">Parameters - displayLengthValue</span></span>

<span data-ttu-id="044da-466">値</span><span class="sxs-lookup"><span data-stu-id="044da-466">value</span></span>  

### <a name="return-value---displaylengthvalue"></a><span data-ttu-id="044da-467">戻り値 - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="044da-467">Return Value - displayLengthValue</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="044da-468">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="044da-468">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="044da-469">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="044da-469">Parameters - displayTarget</span></span>

<span data-ttu-id="044da-470">値</span><span class="sxs-lookup"><span data-stu-id="044da-470">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="044da-471">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="044da-471">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="044da-472">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="044da-472">Method dragDrop</span></span>

<span data-ttu-id="044da-473">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="044da-473">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="044da-474">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="044da-474">Parameters - dragDrop</span></span>

<span data-ttu-id="044da-475">値</span><span class="sxs-lookup"><span data-stu-id="044da-475">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="044da-476">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="044da-476">Return Value - dragDrop</span></span>

<span data-ttu-id="044da-477">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="044da-477">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="044da-478">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="044da-478">Method enabled</span></span>

<span data-ttu-id="044da-479">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="044da-479">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="044da-480">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="044da-480">Parameters - enabled</span></span>

<span data-ttu-id="044da-481">値</span><span class="sxs-lookup"><span data-stu-id="044da-481">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="044da-482">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="044da-482">Return Value - enabled</span></span>

<span data-ttu-id="044da-483">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="044da-483">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="044da-484">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="044da-484">Remarks - enabled</span></span>

<span data-ttu-id="044da-485">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="044da-485">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="044da-486">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="044da-486">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="044da-487">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="044da-487">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="044da-488">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="044da-488">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="044da-489">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="044da-489">Parameters - extendedDataType</span></span>

<span data-ttu-id="044da-490">値</span><span class="sxs-lookup"><span data-stu-id="044da-490">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="044da-491">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="044da-491">Return Value - extendedDataType</span></span>

## <a name="method-fasttabsummary"></a><span data-ttu-id="044da-492">メソッド fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="044da-492">Method fastTabSummary</span></span>

```xpp
public int fastTabSummary([int value])
```

### <a name="parameters---fasttabsummary"></a><span data-ttu-id="044da-493">パラメーター - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="044da-493">Parameters - fastTabSummary</span></span>

<span data-ttu-id="044da-494">値</span><span class="sxs-lookup"><span data-stu-id="044da-494">value</span></span>  

### <a name="return-value---fasttabsummary"></a><span data-ttu-id="044da-495">戻り値 - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="044da-495">Return Value - fastTabSummary</span></span>

## <a name="method-font"></a><span data-ttu-id="044da-496">メソッド font</span><span class="sxs-lookup"><span data-stu-id="044da-496">Method font</span></span>

<span data-ttu-id="044da-497">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-497">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="044da-498">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="044da-498">Parameters - font</span></span>

<span data-ttu-id="044da-499">値</span><span class="sxs-lookup"><span data-stu-id="044da-499">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="044da-500">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="044da-500">Return Value - font</span></span>

<span data-ttu-id="044da-501">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="044da-501">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="044da-502">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="044da-502">Method fontSize</span></span>

<span data-ttu-id="044da-503">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-503">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="044da-504">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="044da-504">Parameters - fontSize</span></span>

<span data-ttu-id="044da-505">値</span><span class="sxs-lookup"><span data-stu-id="044da-505">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="044da-506">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="044da-506">Return Value - fontSize</span></span>

<span data-ttu-id="044da-507">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="044da-507">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="044da-508">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="044da-508">Method foregroundColor</span></span>

<span data-ttu-id="044da-509">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-509">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="044da-510">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="044da-510">Parameters - foregroundColor</span></span>

<span data-ttu-id="044da-511">値</span><span class="sxs-lookup"><span data-stu-id="044da-511">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="044da-512">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="044da-512">Return Value - foregroundColor</span></span>

<span data-ttu-id="044da-513">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="044da-513">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="044da-514">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="044da-514">Remarks - foregroundColor</span></span>

<span data-ttu-id="044da-515">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="044da-515">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="044da-516">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="044da-516">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="044da-517">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="044da-517">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="044da-518">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="044da-518">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="044da-519">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="044da-519">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="044da-520">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="044da-520">The maximum value for a single byte is 255.</span></span>

## <a name="method-height"></a><span data-ttu-id="044da-521">メソッド height</span><span class="sxs-lookup"><span data-stu-id="044da-521">Method height</span></span>

<span data-ttu-id="044da-522">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-522">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="044da-523">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="044da-523">Parameters - height</span></span>

<span data-ttu-id="044da-524">値</span><span class="sxs-lookup"><span data-stu-id="044da-524">value</span></span>  

<!-- -->

<span data-ttu-id="044da-525">モード</span><span class="sxs-lookup"><span data-stu-id="044da-525">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="044da-526">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="044da-526">Return Value - height</span></span>

<span data-ttu-id="044da-527">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="044da-527">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="044da-528">備考 - height</span><span class="sxs-lookup"><span data-stu-id="044da-528">Remarks - height</span></span>

<span data-ttu-id="044da-529">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="044da-529">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="044da-530">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="044da-530">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="044da-531">モード。</span><span class="sxs-lookup"><span data-stu-id="044da-531">Mode.</span></span>            | <span data-ttu-id="044da-532">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="044da-532">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="044da-533">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="044da-533">-1 Exact.</span></span>        | <span data-ttu-id="044da-534">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="044da-534">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="044da-535">0 自動。</span><span class="sxs-lookup"><span data-stu-id="044da-535">0 Auto.</span></span>          | <span data-ttu-id="044da-536">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="044da-536">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="044da-537">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="044da-537">1 Column height.</span></span> | <span data-ttu-id="044da-538">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="044da-538">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="044da-539">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="044da-539">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="044da-540">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="044da-540">Method heightMode</span></span>

<span data-ttu-id="044da-541">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-541">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="044da-542">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="044da-542">Parameters - heightMode</span></span>

<span data-ttu-id="044da-543">値</span><span class="sxs-lookup"><span data-stu-id="044da-543">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="044da-544">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="044da-544">Return Value - heightMode</span></span>

<span data-ttu-id="044da-545">計算モード。</span><span class="sxs-lookup"><span data-stu-id="044da-545">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="044da-546">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="044da-546">Remarks - heightMode</span></span>

<span data-ttu-id="044da-547">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="044da-547">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="044da-548">モード。</span><span class="sxs-lookup"><span data-stu-id="044da-548">Mode.</span></span>          | <span data-ttu-id="044da-549">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="044da-549">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="044da-550">正確。</span><span class="sxs-lookup"><span data-stu-id="044da-550">Exact.</span></span>         | <span data-ttu-id="044da-551">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="044da-551">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="044da-552">自動。</span><span class="sxs-lookup"><span data-stu-id="044da-552">Auto.</span></span>          | <span data-ttu-id="044da-553">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="044da-553">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="044da-554">列の高さ</span><span class="sxs-lookup"><span data-stu-id="044da-554">Column height.</span></span> | <span data-ttu-id="044da-555">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="044da-555">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="044da-556">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="044da-556">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="044da-557">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="044da-557">Method heightValue</span></span>

<span data-ttu-id="044da-558">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-558">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="044da-559">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="044da-559">Parameters - heightValue</span></span>

<span data-ttu-id="044da-560">値</span><span class="sxs-lookup"><span data-stu-id="044da-560">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="044da-561">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="044da-561">Return Value - heightValue</span></span>

<span data-ttu-id="044da-562">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="044da-562">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="044da-563">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="044da-563">Remarks - heightValue</span></span>

<span data-ttu-id="044da-564">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="044da-564">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="044da-565">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="044da-565">Method helpText</span></span>

<span data-ttu-id="044da-566">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-566">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="044da-567">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="044da-567">Parameters - helpText</span></span>

<span data-ttu-id="044da-568">値</span><span class="sxs-lookup"><span data-stu-id="044da-568">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="044da-569">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="044da-569">Return Value - helpText</span></span>

<span data-ttu-id="044da-570">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="044da-570">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="044da-571">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="044da-571">Remarks - helpText</span></span>

<span data-ttu-id="044da-572">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-572">Set the HelpText property for an object by using the property dialogue box.</span></span> <span data-ttu-id="044da-573">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="044da-573">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="044da-574">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="044da-574">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="044da-575">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="044da-575">Parameters - hierarchyParent</span></span>

<span data-ttu-id="044da-576">値</span><span class="sxs-lookup"><span data-stu-id="044da-576">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="044da-577">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="044da-577">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="044da-578">メソッド id</span><span class="sxs-lookup"><span data-stu-id="044da-578">Method id</span></span>

<span data-ttu-id="044da-579">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="044da-579">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="044da-580">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="044da-580">Return Value - id</span></span>

<span data-ttu-id="044da-581">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="044da-581">The ID of the control.</span></span>

## <a name="method-imemode"></a><span data-ttu-id="044da-582">メソッド iMEMode</span><span class="sxs-lookup"><span data-stu-id="044da-582">Method iMEMode</span></span>

```xpp
public int iMEMode([int value])
```

### <a name="parameters---imemode"></a><span data-ttu-id="044da-583">パラメーター - iMEMode</span><span class="sxs-lookup"><span data-stu-id="044da-583">Parameters - iMEMode</span></span>

<span data-ttu-id="044da-584">値</span><span class="sxs-lookup"><span data-stu-id="044da-584">value</span></span>  

### <a name="return-value---imemode"></a><span data-ttu-id="044da-585">戻り値 - iMEMode</span><span class="sxs-lookup"><span data-stu-id="044da-585">Return Value - iMEMode</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="044da-586">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="044da-586">Method isContainer</span></span>

<span data-ttu-id="044da-587">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="044da-587">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="044da-588">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="044da-588">Return Value - isContainer</span></span>

<span data-ttu-id="044da-589">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="044da-589">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-italic"></a><span data-ttu-id="044da-590">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="044da-590">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="044da-591">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="044da-591">Parameters - italic</span></span>

<span data-ttu-id="044da-592">値</span><span class="sxs-lookup"><span data-stu-id="044da-592">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="044da-593">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="044da-593">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="044da-594">メソッド label</span><span class="sxs-lookup"><span data-stu-id="044da-594">Method label</span></span>

<span data-ttu-id="044da-595">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-595">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="044da-596">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="044da-596">Parameters - label</span></span>

<span data-ttu-id="044da-597">値</span><span class="sxs-lookup"><span data-stu-id="044da-597">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="044da-598">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="044da-598">Return Value - label</span></span>

<span data-ttu-id="044da-599">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="044da-599">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="044da-600">備考 - label</span><span class="sxs-lookup"><span data-stu-id="044da-600">Remarks - label</span></span>

<span data-ttu-id="044da-601">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="044da-601">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="044da-602">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="044da-602">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="044da-603">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="044da-603">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="044da-604">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="044da-604">Parameters - labelAlignment</span></span>

<span data-ttu-id="044da-605">値</span><span class="sxs-lookup"><span data-stu-id="044da-605">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="044da-606">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="044da-606">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="044da-607">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="044da-607">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="044da-608">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="044da-608">Parameters - labelBold</span></span>

<span data-ttu-id="044da-609">値</span><span class="sxs-lookup"><span data-stu-id="044da-609">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="044da-610">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="044da-610">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="044da-611">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="044da-611">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="044da-612">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="044da-612">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="044da-613">値</span><span class="sxs-lookup"><span data-stu-id="044da-613">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="044da-614">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="044da-614">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="044da-615">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="044da-615">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="044da-616">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="044da-616">Parameters - labelFont</span></span>

<span data-ttu-id="044da-617">値</span><span class="sxs-lookup"><span data-stu-id="044da-617">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="044da-618">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="044da-618">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="044da-619">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="044da-619">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="044da-620">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="044da-620">Parameters - labelFontSize</span></span>

<span data-ttu-id="044da-621">値</span><span class="sxs-lookup"><span data-stu-id="044da-621">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="044da-622">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="044da-622">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="044da-623">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="044da-623">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="044da-624">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="044da-624">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="044da-625">値</span><span class="sxs-lookup"><span data-stu-id="044da-625">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="044da-626">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="044da-626">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="044da-627">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="044da-627">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="044da-628">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="044da-628">Parameters - labelGuide</span></span>

<span data-ttu-id="044da-629">値</span><span class="sxs-lookup"><span data-stu-id="044da-629">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="044da-630">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="044da-630">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="044da-631">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="044da-631">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="044da-632">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="044da-632">Parameters - labelHeight</span></span>

<span data-ttu-id="044da-633">値</span><span class="sxs-lookup"><span data-stu-id="044da-633">value</span></span>  

<!-- -->

<span data-ttu-id="044da-634">モード</span><span class="sxs-lookup"><span data-stu-id="044da-634">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="044da-635">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="044da-635">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="044da-636">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="044da-636">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="044da-637">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="044da-637">Parameters - labelHeightMode</span></span>

<span data-ttu-id="044da-638">値</span><span class="sxs-lookup"><span data-stu-id="044da-638">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="044da-639">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="044da-639">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="044da-640">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="044da-640">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="044da-641">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="044da-641">Parameters - labelHeightValue</span></span>

<span data-ttu-id="044da-642">値</span><span class="sxs-lookup"><span data-stu-id="044da-642">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="044da-643">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="044da-643">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="044da-644">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="044da-644">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="044da-645">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="044da-645">Parameters - labelItalic</span></span>

<span data-ttu-id="044da-646">値</span><span class="sxs-lookup"><span data-stu-id="044da-646">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="044da-647">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="044da-647">Return Value - labelItalic</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="044da-648">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="044da-648">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="044da-649">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="044da-649">Parameters - labelPosition</span></span>

<span data-ttu-id="044da-650">値</span><span class="sxs-lookup"><span data-stu-id="044da-650">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="044da-651">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="044da-651">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="044da-652">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="044da-652">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="044da-653">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="044da-653">Parameters - labelUnderline</span></span>

<span data-ttu-id="044da-654">値</span><span class="sxs-lookup"><span data-stu-id="044da-654">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="044da-655">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="044da-655">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="044da-656">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="044da-656">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="044da-657">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="044da-657">Parameters - labelWidth</span></span>

<span data-ttu-id="044da-658">値</span><span class="sxs-lookup"><span data-stu-id="044da-658">value</span></span>  

<!-- -->

<span data-ttu-id="044da-659">モード</span><span class="sxs-lookup"><span data-stu-id="044da-659">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="044da-660">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="044da-660">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="044da-661">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="044da-661">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="044da-662">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="044da-662">Parameters - labelWidthMode</span></span>

<span data-ttu-id="044da-663">値</span><span class="sxs-lookup"><span data-stu-id="044da-663">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="044da-664">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="044da-664">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="044da-665">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="044da-665">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="044da-666">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="044da-666">Parameters - labelWidthValue</span></span>

<span data-ttu-id="044da-667">値</span><span class="sxs-lookup"><span data-stu-id="044da-667">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="044da-668">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="044da-668">Return Value - labelWidthValue</span></span>

## <a name="method-left"></a><span data-ttu-id="044da-669">メソッド left</span><span class="sxs-lookup"><span data-stu-id="044da-669">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="044da-670">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="044da-670">Parameters - left</span></span>

<span data-ttu-id="044da-671">値</span><span class="sxs-lookup"><span data-stu-id="044da-671">value</span></span>  

<!-- -->

<span data-ttu-id="044da-672">モード</span><span class="sxs-lookup"><span data-stu-id="044da-672">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="044da-673">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="044da-673">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="044da-674">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="044da-674">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="044da-675">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="044da-675">Parameters - leftMode</span></span>

<span data-ttu-id="044da-676">値</span><span class="sxs-lookup"><span data-stu-id="044da-676">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="044da-677">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="044da-677">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="044da-678">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="044da-678">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="044da-679">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="044da-679">Parameters - leftValue</span></span>

<span data-ttu-id="044da-680">値</span><span class="sxs-lookup"><span data-stu-id="044da-680">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="044da-681">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="044da-681">Return Value - leftValue</span></span>

## <a name="method-limittext"></a><span data-ttu-id="044da-682">メソッド limitText</span><span class="sxs-lookup"><span data-stu-id="044da-682">Method limitText</span></span>

```xpp
public int limitText([int value], [AutoMode mode])
```

### <a name="parameters---limittext"></a><span data-ttu-id="044da-683">パラメーター - limitText</span><span class="sxs-lookup"><span data-stu-id="044da-683">Parameters - limitText</span></span>

<span data-ttu-id="044da-684">値</span><span class="sxs-lookup"><span data-stu-id="044da-684">value</span></span>  

<!-- -->

<span data-ttu-id="044da-685">モード</span><span class="sxs-lookup"><span data-stu-id="044da-685">mode</span></span>  

### <a name="return-value---limittext"></a><span data-ttu-id="044da-686">戻り値 - limitText</span><span class="sxs-lookup"><span data-stu-id="044da-686">Return Value - limitText</span></span>

## <a name="method-limittextmode"></a><span data-ttu-id="044da-687">メソッド limitTextMode</span><span class="sxs-lookup"><span data-stu-id="044da-687">Method limitTextMode</span></span>

```xpp
public AutoMode limitTextMode([AutoMode mode])
```

### <a name="parameters---limittextmode"></a><span data-ttu-id="044da-688">パラメーター - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="044da-688">Parameters - limitTextMode</span></span>

<span data-ttu-id="044da-689">モード</span><span class="sxs-lookup"><span data-stu-id="044da-689">mode</span></span>  

### <a name="return-value---limittextmode"></a><span data-ttu-id="044da-690">戻り値 - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="044da-690">Return Value - limitTextMode</span></span>

## <a name="method-limittextvalue"></a><span data-ttu-id="044da-691">メソッド limitTextValue</span><span class="sxs-lookup"><span data-stu-id="044da-691">Method limitTextValue</span></span>

```xpp
public int limitTextValue([int value])
```

### <a name="parameters---limittextvalue"></a><span data-ttu-id="044da-692">パラメーター - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="044da-692">Parameters - limitTextValue</span></span>

<span data-ttu-id="044da-693">値</span><span class="sxs-lookup"><span data-stu-id="044da-693">value</span></span>  

### <a name="return-value---limittextvalue"></a><span data-ttu-id="044da-694">戻り値 - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="044da-694">Return Value - limitTextValue</span></span>

## <a name="method-lookupbutton"></a><span data-ttu-id="044da-695">メソッド lookupButton</span><span class="sxs-lookup"><span data-stu-id="044da-695">Method lookupButton</span></span>

```xpp
public int lookupButton([int value])
```

### <a name="parameters---lookupbutton"></a><span data-ttu-id="044da-696">パラメーター - lookupButton</span><span class="sxs-lookup"><span data-stu-id="044da-696">Parameters - lookupButton</span></span>

<span data-ttu-id="044da-697">値</span><span class="sxs-lookup"><span data-stu-id="044da-697">value</span></span>  

### <a name="return-value---lookupbutton"></a><span data-ttu-id="044da-698">戻り値 - lookupButton</span><span class="sxs-lookup"><span data-stu-id="044da-698">Return Value - lookupButton</span></span>

## <a name="method-mandatory"></a><span data-ttu-id="044da-699">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="044da-699">Method mandatory</span></span>

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a><span data-ttu-id="044da-700">パラメーター - mandatory</span><span class="sxs-lookup"><span data-stu-id="044da-700">Parameters - mandatory</span></span>

<span data-ttu-id="044da-701">値</span><span class="sxs-lookup"><span data-stu-id="044da-701">value</span></span>  

### <a name="return-value---mandatory"></a><span data-ttu-id="044da-702">戻り値 - mandatory</span><span class="sxs-lookup"><span data-stu-id="044da-702">Return Value - mandatory</span></span>

## <a name="method-multiline"></a><span data-ttu-id="044da-703">メソッド multiLine</span><span class="sxs-lookup"><span data-stu-id="044da-703">Method multiLine</span></span>

```xpp
public boolean multiLine([boolean value])
```

### <a name="parameters---multiline"></a><span data-ttu-id="044da-704">パラメーター - multiLine</span><span class="sxs-lookup"><span data-stu-id="044da-704">Parameters - multiLine</span></span>

<span data-ttu-id="044da-705">値</span><span class="sxs-lookup"><span data-stu-id="044da-705">value</span></span>  

### <a name="return-value---multiline"></a><span data-ttu-id="044da-706">戻り値 - multiLine</span><span class="sxs-lookup"><span data-stu-id="044da-706">Return Value - multiLine</span></span>

## <a name="method-name"></a><span data-ttu-id="044da-707">メソッド名</span><span class="sxs-lookup"><span data-stu-id="044da-707">Method name</span></span>

<span data-ttu-id="044da-708">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-708">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="044da-709">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="044da-709">Parameters - name</span></span>

<span data-ttu-id="044da-710">値</span><span class="sxs-lookup"><span data-stu-id="044da-710">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="044da-711">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="044da-711">Return Value - name</span></span>

<span data-ttu-id="044da-712">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="044da-712">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="044da-713">備考 - name</span><span class="sxs-lookup"><span data-stu-id="044da-713">Remarks - name</span></span>

<span data-ttu-id="044da-714">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="044da-714">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="044da-715">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="044da-715">Begins with a letter.</span></span>
-   <span data-ttu-id="044da-716">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="044da-716">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="044da-717">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="044da-717">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="044da-718">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="044da-718">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="044da-719">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="044da-719">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="044da-720">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="044da-720">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="044da-721">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="044da-721">Parameters - neededPermission</span></span>

<span data-ttu-id="044da-722">値</span><span class="sxs-lookup"><span data-stu-id="044da-722">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="044da-723">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="044da-723">Return Value - neededPermission</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="044da-724">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="044da-724">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="044da-725">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="044da-725">Parameters - promptrect</span></span>

<span data-ttu-id="044da-726">値</span><span class="sxs-lookup"><span data-stu-id="044da-726">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="044da-727">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="044da-727">Return Value - promptrect</span></span>

## <a name="method-replaceonlookup"></a><span data-ttu-id="044da-728">メソッド replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="044da-728">Method replaceOnLookup</span></span>

```xpp
public boolean replaceOnLookup([boolean value])
```

### <a name="parameters---replaceonlookup"></a><span data-ttu-id="044da-729">パラメーター - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="044da-729">Parameters - replaceOnLookup</span></span>

<span data-ttu-id="044da-730">値</span><span class="sxs-lookup"><span data-stu-id="044da-730">value</span></span>  

### <a name="return-value---replaceonlookup"></a><span data-ttu-id="044da-731">戻り値 - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="044da-731">Return Value - replaceOnLookup</span></span>

## <a name="method-searchafterinput"></a><span data-ttu-id="044da-732">メソッド searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="044da-732">Method searchAfterInput</span></span>

```xpp
public int searchAfterInput([int value])
```

### <a name="parameters---searchafterinput"></a><span data-ttu-id="044da-733">パラメーター - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="044da-733">Parameters - searchAfterInput</span></span>

<span data-ttu-id="044da-734">値</span><span class="sxs-lookup"><span data-stu-id="044da-734">value</span></span>  

### <a name="return-value---searchafterinput"></a><span data-ttu-id="044da-735">戻り値 - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="044da-735">Return Value - searchAfterInput</span></span>

## <a name="method-searchmode"></a><span data-ttu-id="044da-736">メソッド searchMode</span><span class="sxs-lookup"><span data-stu-id="044da-736">Method searchMode</span></span>

```xpp
public int searchMode([int value])
```

### <a name="parameters---searchmode"></a><span data-ttu-id="044da-737">パラメーター - searchMode</span><span class="sxs-lookup"><span data-stu-id="044da-737">Parameters - searchMode</span></span>

<span data-ttu-id="044da-738">値</span><span class="sxs-lookup"><span data-stu-id="044da-738">value</span></span>  

### <a name="return-value---searchmode"></a><span data-ttu-id="044da-739">戻り値 - searchMode</span><span class="sxs-lookup"><span data-stu-id="044da-739">Return Value - searchMode</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="044da-740">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="044da-740">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="044da-741">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="044da-741">Parameters - securityKey</span></span>

<span data-ttu-id="044da-742">値</span><span class="sxs-lookup"><span data-stu-id="044da-742">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="044da-743">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="044da-743">Return Value - securityKey</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="044da-744">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="044da-744">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="044da-745">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="044da-745">Parameters - showLabel</span></span>

<span data-ttu-id="044da-746">値</span><span class="sxs-lookup"><span data-stu-id="044da-746">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="044da-747">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="044da-747">Return Value - showLabel</span></span>

## <a name="method-skip"></a><span data-ttu-id="044da-748">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="044da-748">Method skip</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="044da-749">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="044da-749">Parameters - skip</span></span>

<span data-ttu-id="044da-750">値</span><span class="sxs-lookup"><span data-stu-id="044da-750">value</span></span>  

### <a name="return-value---skip"></a><span data-ttu-id="044da-751">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="044da-751">Return Value - skip</span></span>

## <a name="method-style"></a><span data-ttu-id="044da-752">メソッド style</span><span class="sxs-lookup"><span data-stu-id="044da-752">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="044da-753">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="044da-753">Parameters - style</span></span>

<span data-ttu-id="044da-754">値</span><span class="sxs-lookup"><span data-stu-id="044da-754">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="044da-755">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="044da-755">Return Value - style</span></span>

## <a name="method-text"></a><span data-ttu-id="044da-756">メソッド text</span><span class="sxs-lookup"><span data-stu-id="044da-756">Method text</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="044da-757">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="044da-757">Parameters - text</span></span>

<span data-ttu-id="044da-758">値</span><span class="sxs-lookup"><span data-stu-id="044da-758">value</span></span>  

### <a name="return-value---text"></a><span data-ttu-id="044da-759">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="044da-759">Return Value - text</span></span>

## <a name="method-top"></a><span data-ttu-id="044da-760">メソッド top</span><span class="sxs-lookup"><span data-stu-id="044da-760">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="044da-761">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="044da-761">Parameters - top</span></span>

<span data-ttu-id="044da-762">値</span><span class="sxs-lookup"><span data-stu-id="044da-762">value</span></span>  

<!-- -->

<span data-ttu-id="044da-763">モード</span><span class="sxs-lookup"><span data-stu-id="044da-763">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="044da-764">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="044da-764">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="044da-765">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="044da-765">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="044da-766">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="044da-766">Parameters - topMode</span></span>

<span data-ttu-id="044da-767">値</span><span class="sxs-lookup"><span data-stu-id="044da-767">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="044da-768">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="044da-768">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="044da-769">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="044da-769">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="044da-770">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="044da-770">Parameters - topValue</span></span>

<span data-ttu-id="044da-771">値</span><span class="sxs-lookup"><span data-stu-id="044da-771">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="044da-772">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="044da-772">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="044da-773">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="044da-773">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="044da-774">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="044da-774">Parameters - type</span></span>

<span data-ttu-id="044da-775">値</span><span class="sxs-lookup"><span data-stu-id="044da-775">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="044da-776">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="044da-776">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="044da-777">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="044da-777">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="044da-778">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="044da-778">Parameters - underline</span></span>

<span data-ttu-id="044da-779">値</span><span class="sxs-lookup"><span data-stu-id="044da-779">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="044da-780">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="044da-780">Return Value - underline</span></span>

## <a name="method-userdata"></a><span data-ttu-id="044da-781">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="044da-781">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="044da-782">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="044da-782">Parameters - userData</span></span>

<span data-ttu-id="044da-783">値</span><span class="sxs-lookup"><span data-stu-id="044da-783">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="044da-784">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="044da-784">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="044da-785">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="044da-785">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="044da-786">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="044da-786">Parameters - userDataItem</span></span>

<span data-ttu-id="044da-787">値</span><span class="sxs-lookup"><span data-stu-id="044da-787">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="044da-788">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="044da-788">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="044da-789">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="044da-789">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="044da-790">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="044da-790">Parameters - userDataItems</span></span>

<span data-ttu-id="044da-791">値</span><span class="sxs-lookup"><span data-stu-id="044da-791">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="044da-792">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="044da-792">Return Value - userDataItems</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="044da-793">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="044da-793">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="044da-794">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="044da-794">Parameters - verticalSpacing</span></span>

<span data-ttu-id="044da-795">値</span><span class="sxs-lookup"><span data-stu-id="044da-795">value</span></span>  

<!-- -->

<span data-ttu-id="044da-796">モード</span><span class="sxs-lookup"><span data-stu-id="044da-796">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="044da-797">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="044da-797">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="044da-798">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="044da-798">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="044da-799">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="044da-799">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="044da-800">モード</span><span class="sxs-lookup"><span data-stu-id="044da-800">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="044da-801">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="044da-801">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="044da-802">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="044da-802">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="044da-803">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="044da-803">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="044da-804">値</span><span class="sxs-lookup"><span data-stu-id="044da-804">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="044da-805">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="044da-805">Return Value - verticalSpacingValue</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="044da-806">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="044da-806">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="044da-807">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="044da-807">Parameters - viewEditMode</span></span>

<span data-ttu-id="044da-808">値</span><span class="sxs-lookup"><span data-stu-id="044da-808">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="044da-809">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="044da-809">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="044da-810">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="044da-810">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="044da-811">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="044da-811">Parameters - visible</span></span>

<span data-ttu-id="044da-812">値</span><span class="sxs-lookup"><span data-stu-id="044da-812">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="044da-813">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="044da-813">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="044da-814">メソッド width</span><span class="sxs-lookup"><span data-stu-id="044da-814">Method width</span></span>

<span data-ttu-id="044da-815">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-815">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="044da-816">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="044da-816">Parameters - width</span></span>

<span data-ttu-id="044da-817">値</span><span class="sxs-lookup"><span data-stu-id="044da-817">value</span></span>  

<!-- -->

<span data-ttu-id="044da-818">モード</span><span class="sxs-lookup"><span data-stu-id="044da-818">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="044da-819">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="044da-819">Return Value - width</span></span>

<span data-ttu-id="044da-820">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="044da-820">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="044da-821">備考 - width</span><span class="sxs-lookup"><span data-stu-id="044da-821">Remarks - width</span></span>

<span data-ttu-id="044da-822">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="044da-822">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="044da-823">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="044da-823">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="044da-824">モード。</span><span class="sxs-lookup"><span data-stu-id="044da-824">Mode.</span></span>           | <span data-ttu-id="044da-825">幅計算。</span><span class="sxs-lookup"><span data-stu-id="044da-825">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="044da-826">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="044da-826">-1 Exact.</span></span>       | <span data-ttu-id="044da-827">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="044da-827">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="044da-828">0 自動。</span><span class="sxs-lookup"><span data-stu-id="044da-828">0 Auto.</span></span>         | <span data-ttu-id="044da-829">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="044da-829">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="044da-830">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="044da-830">1 Column width.</span></span> | <span data-ttu-id="044da-831">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="044da-831">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="044da-832">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="044da-832">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="044da-833">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="044da-833">Method widthMode</span></span>

<span data-ttu-id="044da-834">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-834">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="044da-835">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="044da-835">Parameters - widthMode</span></span>

<span data-ttu-id="044da-836">値</span><span class="sxs-lookup"><span data-stu-id="044da-836">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="044da-837">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="044da-837">Return Value - widthMode</span></span>

<span data-ttu-id="044da-838">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="044da-838">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="044da-839">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="044da-839">Remarks - widthMode</span></span>

<span data-ttu-id="044da-840">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="044da-840">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="044da-841">モード。</span><span class="sxs-lookup"><span data-stu-id="044da-841">Mode.</span></span>         | <span data-ttu-id="044da-842">幅計算。</span><span class="sxs-lookup"><span data-stu-id="044da-842">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="044da-843">正確。</span><span class="sxs-lookup"><span data-stu-id="044da-843">Exact.</span></span>        | <span data-ttu-id="044da-844">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="044da-844">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="044da-845">自動。</span><span class="sxs-lookup"><span data-stu-id="044da-845">Auto.</span></span>         | <span data-ttu-id="044da-846">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="044da-846">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="044da-847">列の幅。</span><span class="sxs-lookup"><span data-stu-id="044da-847">Column width.</span></span> | <span data-ttu-id="044da-848">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="044da-848">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="044da-849">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="044da-849">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="044da-850">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="044da-850">Method widthValue</span></span>

<span data-ttu-id="044da-851">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="044da-851">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="044da-852">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="044da-852">Parameters - widthValue</span></span>

<span data-ttu-id="044da-853">値</span><span class="sxs-lookup"><span data-stu-id="044da-853">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="044da-854">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="044da-854">Return Value - widthValue</span></span>

<span data-ttu-id="044da-855">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="044da-855">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="044da-856">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="044da-856">Remarks - widthValue</span></span>

<span data-ttu-id="044da-857">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="044da-857">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="044da-858">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="044da-858">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="044da-859">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="044da-859">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="044da-860">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="044da-860">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="044da-861">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="044da-861">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="044da-862">overrideObject</span><span class="sxs-lookup"><span data-stu-id="044da-862">overrideObject</span></span>  

