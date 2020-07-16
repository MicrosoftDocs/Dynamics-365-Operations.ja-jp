---
title: FormBuildDateTimeControl クラス
description: このトピックでは、FormBuildDateTimeControl クラスについて説明します。
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
ms.openlocfilehash: 475104e2854fe52bb56ae2ba4f644dfaa87c4c3c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502655"
---
# <a name="class-formbuilddatetimecontrol"></a><span data-ttu-id="a450b-103">クラス FormBuildDateTimeControl</span><span class="sxs-lookup"><span data-stu-id="a450b-103">Class FormBuildDateTimeControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildDateTimeControl extends FormBuildControl
```

## <a name="remarks"></a><span data-ttu-id="a450b-104">備考</span><span class="sxs-lookup"><span data-stu-id="a450b-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="a450b-105">例</span><span class="sxs-lookup"><span data-stu-id="a450b-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="a450b-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="a450b-106">Methods</span></span>

| <span data-ttu-id="a450b-107">方法</span><span class="sxs-lookup"><span data-stu-id="a450b-107">Method</span></span>                                                                                                      | <span data-ttu-id="a450b-108">説明</span><span class="sxs-lookup"><span data-stu-id="a450b-108">Description</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a450b-109">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-109">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="a450b-110">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-110">Determines whether to align the control.</span></span>                                                                                                  |
| <span data-ttu-id="a450b-111">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-111">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="a450b-112">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-112">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="a450b-113">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-113">Determines whether the user can change the contents of the control.</span></span>                                                                       |
| <span data-ttu-id="a450b-114">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-114">public int arrayIndex(\[int value\])</span></span>                                                                        |                                                                                                                                           |
| <span data-ttu-id="a450b-115">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-115">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="a450b-116">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-116">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                        |
| <span data-ttu-id="a450b-117">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-117">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="a450b-118">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-118">Gets or sets the background color of the control.</span></span>                                                                                         |
| <span data-ttu-id="a450b-119">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-119">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="a450b-120">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-120">Determines whether the control background can be transparent.</span></span>                                                                             |
| <span data-ttu-id="a450b-121">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-121">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="a450b-122">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-122">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                               |
| <span data-ttu-id="a450b-123">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-123">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="a450b-124">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-124">Gets or sets the style of the borderline of the control.</span></span>                                                                                  |
| <span data-ttu-id="a450b-125">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-125">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="a450b-126">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-126">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="a450b-127">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-127">Gets or sets the character set of the font.</span></span>                                                                                               |
| <span data-ttu-id="a450b-128">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-128">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="a450b-129">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-129">Gets or sets the color scheme of the control.</span></span>                                                                                             |
| <span data-ttu-id="a450b-130">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-130">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="a450b-131">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-131">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                       |
| <span data-ttu-id="a450b-132">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="a450b-132">public int containerId()</span></span>                                                                                    | <span data-ttu-id="a450b-133">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="a450b-133">Retrieves the ID of the parent container for the control.</span></span>                                                                                 |
| <span data-ttu-id="a450b-134">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-134">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                           |
| <span data-ttu-id="a450b-135">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-135">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                           |
| <span data-ttu-id="a450b-136">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-136">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="a450b-137">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-137">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                           |
| <span data-ttu-id="a450b-138">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-138">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="a450b-139">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-139">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="a450b-140">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-140">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                  |
| <span data-ttu-id="a450b-141">public int dateDay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-141">public int dateDay(\[int value\])</span></span>                                                                           |                                                                                                                                           |
| <span data-ttu-id="a450b-142">public int dateFormat(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-142">public int dateFormat(\[int value\])</span></span>                                                                        |                                                                                                                                           |
| <span data-ttu-id="a450b-143">public int dateMonth(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-143">public int dateMonth(\[int value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="a450b-144">public int dateSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-144">public int dateSeparator(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="a450b-145">public DateTime dateTimeValue(\[DateTime value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-145">public DateTime dateTimeValue(\[DateTime value\])</span></span>                                                           |                                                                                                                                           |
| <span data-ttu-id="a450b-146">public int dateYear(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-146">public int dateYear(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="a450b-147">public int displayOption(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-147">public int displayOption(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="a450b-148">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-148">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="a450b-149">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-149">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="a450b-150">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-150">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                         |
| <span data-ttu-id="a450b-151">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-151">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="a450b-152">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-152">Determines whether to enable or disable the object.</span></span>                                                                                       |
| <span data-ttu-id="a450b-153">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-153">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                           |
| <span data-ttu-id="a450b-154">public int fastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-154">public int fastTabSummary(\[int value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="a450b-155">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-155">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="a450b-156">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-156">Gets or sets the name of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="a450b-157">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-157">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="a450b-158">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-158">Gets or sets the size of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="a450b-159">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-159">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="a450b-160">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-160">Gets or sets the text color for the control to use.</span></span>                                                                                       |
| <span data-ttu-id="a450b-161">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="a450b-161">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="a450b-162">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-162">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="a450b-163">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-163">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="a450b-164">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-164">Gets or sets a calculation mode for the height of the control.</span></span>                                                                            |
| <span data-ttu-id="a450b-165">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-165">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="a450b-166">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-166">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="a450b-167">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-167">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="a450b-168">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-168">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="a450b-169">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-169">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="a450b-170">public int id()</span><span class="sxs-lookup"><span data-stu-id="a450b-170">public int id()</span></span>                                                                                             | <span data-ttu-id="a450b-171">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="a450b-171">Retrieves the ID of the control.</span></span>                                                                                                          |
| <span data-ttu-id="a450b-172">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="a450b-172">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="a450b-173">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="a450b-173">Retrieves a value that indicates whether the control is a container control.</span></span>                                                              |
| <span data-ttu-id="a450b-174">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-174">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="a450b-175">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-175">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="a450b-176">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-176">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="a450b-177">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-177">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="a450b-178">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-178">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="a450b-179">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-179">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="a450b-180">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-180">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="a450b-181">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-181">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="a450b-182">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-182">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="a450b-183">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-183">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                           |
| <span data-ttu-id="a450b-184">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="a450b-184">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                           |
| <span data-ttu-id="a450b-185">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-185">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="a450b-186">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-186">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="a450b-187">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-187">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                           |
| <span data-ttu-id="a450b-188">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-188">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="a450b-189">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-189">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                           |
| <span data-ttu-id="a450b-190">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="a450b-190">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="a450b-191">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-191">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="a450b-192">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-192">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="a450b-193">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="a450b-193">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="a450b-194">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-194">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="a450b-195">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-195">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="a450b-196">public int limitText(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="a450b-196">public int limitText(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="a450b-197">public AutoMode limitTextMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="a450b-197">public AutoMode limitTextMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                           |
| <span data-ttu-id="a450b-198">public int limitTextValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-198">public int limitTextValue(\[int value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="a450b-199">public int lookupButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-199">public int lookupButton(\[int value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="a450b-200">public boolean mandatory(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-200">public boolean mandatory(\[boolean value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="a450b-201">public str maxDateLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-201">public str maxDateLabel(\[str value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="a450b-202">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-202">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="a450b-203">フォーム、レポート、テーブル、クエリ、または別のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-203">Gets or sets the name that is used in code to identify a form, report, table, query, or another application object.</span></span> |
| <span data-ttu-id="a450b-204">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-204">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="a450b-205">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-205">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                           |
| <span data-ttu-id="a450b-206">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-206">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                           |
| <span data-ttu-id="a450b-207">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-207">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="a450b-208">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-208">public boolean skip(\[boolean value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="a450b-209">public int timeFormat(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-209">public int timeFormat(\[int value\])</span></span>                                                                        |                                                                                                                                           |
| <span data-ttu-id="a450b-210">public int timeHours(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-210">public int timeHours(\[int value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="a450b-211">public int timeMinute(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-211">public int timeMinute(\[int value\])</span></span>                                                                        |                                                                                                                                           |
| <span data-ttu-id="a450b-212">public int timeSeconds(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-212">public int timeSeconds(\[int value\])</span></span>                                                                       |                                                                                                                                           |
| <span data-ttu-id="a450b-213">public int timeSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-213">public int timeSeparator(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="a450b-214">public int timeZoneIndicator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-214">public int timeZoneIndicator(\[int value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="a450b-215">public int timezonePreference(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-215">public int timezonePreference(\[int value\])</span></span>                                                                |                                                                                                                                           |
| <span data-ttu-id="a450b-216">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="a450b-216">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="a450b-217">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-217">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                           |
| <span data-ttu-id="a450b-218">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-218">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="a450b-219">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-219">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="a450b-220">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-220">public boolean underline(\[boolean value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="a450b-221">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-221">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="a450b-222">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-222">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="a450b-223">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-223">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="a450b-224">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="a450b-224">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                           |
| <span data-ttu-id="a450b-225">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="a450b-225">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="a450b-226">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-226">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="a450b-227">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-227">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="a450b-228">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-228">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="a450b-229">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="a450b-229">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="a450b-230">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-230">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="a450b-231">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-231">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="a450b-232">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-232">Gets or sets the calculation mode of the width of the control.</span></span>                                                                            |
| <span data-ttu-id="a450b-233">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a450b-233">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="a450b-234">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-234">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="a450b-235">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="a450b-235">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                           |

## <a name="method-aligncontrol"></a><span data-ttu-id="a450b-236">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="a450b-236">Method alignControl</span></span>

<span data-ttu-id="a450b-237">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-237">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="a450b-238">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="a450b-238">Parameters - alignControl</span></span>

<span data-ttu-id="a450b-239">値</span><span class="sxs-lookup"><span data-stu-id="a450b-239">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="a450b-240">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="a450b-240">Return Value - alignControl</span></span>

<span data-ttu-id="a450b-241">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="a450b-241">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="a450b-242">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="a450b-242">Remarks - alignControl</span></span>

<span data-ttu-id="a450b-243">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="a450b-243">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="a450b-244">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="a450b-244">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="a450b-245">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="a450b-245">Parameters - alignment</span></span>

<span data-ttu-id="a450b-246">値</span><span class="sxs-lookup"><span data-stu-id="a450b-246">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="a450b-247">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="a450b-247">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="a450b-248">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="a450b-248">Method allowEdit</span></span>

<span data-ttu-id="a450b-249">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-249">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="a450b-250">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="a450b-250">Parameters - allowEdit</span></span>

<span data-ttu-id="a450b-251">値</span><span class="sxs-lookup"><span data-stu-id="a450b-251">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="a450b-252">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="a450b-252">Return Value - allowEdit</span></span>

<span data-ttu-id="a450b-253">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a450b-253">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="a450b-254">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="a450b-254">Remarks - allowEdit</span></span>

<span data-ttu-id="a450b-255">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="a450b-255">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="a450b-256">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="a450b-256">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="a450b-257">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="a450b-257">Parameters - arrayIndex</span></span>

<span data-ttu-id="a450b-258">値</span><span class="sxs-lookup"><span data-stu-id="a450b-258">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="a450b-259">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="a450b-259">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="a450b-260">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="a450b-260">Method autoDeclaration</span></span>

<span data-ttu-id="a450b-261">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-261">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="a450b-262">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="a450b-262">Parameters - autoDeclaration</span></span>

<span data-ttu-id="a450b-263">値</span><span class="sxs-lookup"><span data-stu-id="a450b-263">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="a450b-264">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="a450b-264">Return Value - autoDeclaration</span></span>

<span data-ttu-id="a450b-265">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a450b-265">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="a450b-266">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="a450b-266">Remarks - autoDeclaration</span></span>

<span data-ttu-id="a450b-267">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="a450b-267">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="a450b-268">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="a450b-268">Method backgroundColor</span></span>

<span data-ttu-id="a450b-269">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-269">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="a450b-270">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="a450b-270">Parameters - backgroundColor</span></span>

<span data-ttu-id="a450b-271">値</span><span class="sxs-lookup"><span data-stu-id="a450b-271">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="a450b-272">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="a450b-272">Return Value - backgroundColor</span></span>

<span data-ttu-id="a450b-273">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="a450b-273">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="a450b-274">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="a450b-274">Remarks - backgroundColor</span></span>

<span data-ttu-id="a450b-275">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a450b-275">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="a450b-276">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a450b-276">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="a450b-277">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="a450b-277">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="a450b-278">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="a450b-278">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="a450b-279">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="a450b-279">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="a450b-280">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="a450b-280">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="a450b-281">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="a450b-281">Method backStyle</span></span>

<span data-ttu-id="a450b-282">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-282">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="a450b-283">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="a450b-283">Parameters - backStyle</span></span>

<span data-ttu-id="a450b-284">値</span><span class="sxs-lookup"><span data-stu-id="a450b-284">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="a450b-285">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="a450b-285">Return Value - backStyle</span></span>

<span data-ttu-id="a450b-286">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="a450b-286">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="a450b-287">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="a450b-287">Method bold</span></span>

<span data-ttu-id="a450b-288">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-288">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="a450b-289">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="a450b-289">Parameters - bold</span></span>

<span data-ttu-id="a450b-290">値</span><span class="sxs-lookup"><span data-stu-id="a450b-290">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="a450b-291">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="a450b-291">Return Value - bold</span></span>

<span data-ttu-id="a450b-292">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="a450b-292">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="a450b-293">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="a450b-293">Remarks - bold</span></span>

<span data-ttu-id="a450b-294">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a450b-294">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="a450b-295">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="a450b-295">0 Use the default font weight.</span></span>
-   <span data-ttu-id="a450b-296">1 シン。</span><span class="sxs-lookup"><span data-stu-id="a450b-296">1 Thin.</span></span>
-   <span data-ttu-id="a450b-297">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="a450b-297">2 Extra-light.</span></span>
-   <span data-ttu-id="a450b-298">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="a450b-298">3 Light.</span></span>
-   <span data-ttu-id="a450b-299">4 標準。</span><span class="sxs-lookup"><span data-stu-id="a450b-299">4 Normal.</span></span>
-   <span data-ttu-id="a450b-300">5 中。</span><span class="sxs-lookup"><span data-stu-id="a450b-300">5 Medium.</span></span>
-   <span data-ttu-id="a450b-301">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="a450b-301">6 Semibold.</span></span>
-   <span data-ttu-id="a450b-302">7 太字。</span><span class="sxs-lookup"><span data-stu-id="a450b-302">7 Bold.</span></span>
-   <span data-ttu-id="a450b-303">8 極太。</span><span class="sxs-lookup"><span data-stu-id="a450b-303">8 Extra-bold.</span></span>
-   <span data-ttu-id="a450b-304">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="a450b-304">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="a450b-305">メソッド border</span><span class="sxs-lookup"><span data-stu-id="a450b-305">Method border</span></span>

<span data-ttu-id="a450b-306">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-306">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="a450b-307">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="a450b-307">Parameters - border</span></span>

<span data-ttu-id="a450b-308">値</span><span class="sxs-lookup"><span data-stu-id="a450b-308">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="a450b-309">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="a450b-309">Return Value - border</span></span>

<span data-ttu-id="a450b-310">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="a450b-310">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="a450b-311">備考 - border</span><span class="sxs-lookup"><span data-stu-id="a450b-311">Remarks - border</span></span>

<span data-ttu-id="a450b-312">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a450b-312">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="a450b-313">値です。</span><span class="sxs-lookup"><span data-stu-id="a450b-313">Value.</span></span> | <span data-ttu-id="a450b-314">説明。</span><span class="sxs-lookup"><span data-stu-id="a450b-314">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="a450b-315">0</span><span class="sxs-lookup"><span data-stu-id="a450b-315">0</span></span>      | <span data-ttu-id="a450b-316">自動。</span><span class="sxs-lookup"><span data-stu-id="a450b-316">Auto.</span></span>        |
| <span data-ttu-id="a450b-317">1</span><span class="sxs-lookup"><span data-stu-id="a450b-317">1</span></span>      | <span data-ttu-id="a450b-318">3D。</span><span class="sxs-lookup"><span data-stu-id="a450b-318">3D.</span></span>          |
| <span data-ttu-id="a450b-319">2</span><span class="sxs-lookup"><span data-stu-id="a450b-319">2</span></span>      | <span data-ttu-id="a450b-320">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="a450b-320">Single line.</span></span> |
| <span data-ttu-id="a450b-321">3</span><span class="sxs-lookup"><span data-stu-id="a450b-321">3</span></span>      | <span data-ttu-id="a450b-322">均一。</span><span class="sxs-lookup"><span data-stu-id="a450b-322">Flat.</span></span>        |
| <span data-ttu-id="a450b-323">4</span><span class="sxs-lookup"><span data-stu-id="a450b-323">4</span></span>      | <span data-ttu-id="a450b-324">なし。</span><span class="sxs-lookup"><span data-stu-id="a450b-324">None.</span></span>        |

## <a name="method-cachedatamethod"></a><span data-ttu-id="a450b-325">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="a450b-325">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="a450b-326">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="a450b-326">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="a450b-327">値</span><span class="sxs-lookup"><span data-stu-id="a450b-327">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="a450b-328">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="a450b-328">Return Value - cacheDataMethod</span></span>

## <a name="method-characterset"></a><span data-ttu-id="a450b-329">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="a450b-329">Method characterSet</span></span>

<span data-ttu-id="a450b-330">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-330">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="a450b-331">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="a450b-331">Parameters - characterSet</span></span>

<span data-ttu-id="a450b-332">値</span><span class="sxs-lookup"><span data-stu-id="a450b-332">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="a450b-333">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="a450b-333">Return Value - characterSet</span></span>

<span data-ttu-id="a450b-334">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a450b-334">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="a450b-335">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="a450b-335">Remarks - characterSet</span></span>

<span data-ttu-id="a450b-336">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="a450b-336">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="a450b-337">値です。</span><span class="sxs-lookup"><span data-stu-id="a450b-337">Value.</span></span> | <span data-ttu-id="a450b-338">説明。</span><span class="sxs-lookup"><span data-stu-id="a450b-338">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="a450b-339">0</span><span class="sxs-lookup"><span data-stu-id="a450b-339">0</span></span>      | <span data-ttu-id="a450b-340">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a450b-340">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="a450b-341">1</span><span class="sxs-lookup"><span data-stu-id="a450b-341">1</span></span>      | <span data-ttu-id="a450b-342">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a450b-342">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="a450b-343">2</span><span class="sxs-lookup"><span data-stu-id="a450b-343">2</span></span>      | <span data-ttu-id="a450b-344">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a450b-344">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="a450b-345">77</span><span class="sxs-lookup"><span data-stu-id="a450b-345">77</span></span>     | <span data-ttu-id="a450b-346">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a450b-346">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="a450b-347">128</span><span class="sxs-lookup"><span data-stu-id="a450b-347">128</span></span>    | <span data-ttu-id="a450b-348">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a450b-348">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="a450b-349">129</span><span class="sxs-lookup"><span data-stu-id="a450b-349">129</span></span>    | <span data-ttu-id="a450b-350">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a450b-350">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="a450b-351">134</span><span class="sxs-lookup"><span data-stu-id="a450b-351">134</span></span>    | <span data-ttu-id="a450b-352">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a450b-352">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="a450b-353">136</span><span class="sxs-lookup"><span data-stu-id="a450b-353">136</span></span>    | <span data-ttu-id="a450b-354">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a450b-354">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="a450b-355">161</span><span class="sxs-lookup"><span data-stu-id="a450b-355">161</span></span>    | <span data-ttu-id="a450b-356">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a450b-356">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="a450b-357">162</span><span class="sxs-lookup"><span data-stu-id="a450b-357">162</span></span>    | <span data-ttu-id="a450b-358">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a450b-358">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="a450b-359">163</span><span class="sxs-lookup"><span data-stu-id="a450b-359">163</span></span>    | <span data-ttu-id="a450b-360">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a450b-360">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="a450b-361">186</span><span class="sxs-lookup"><span data-stu-id="a450b-361">186</span></span>    | <span data-ttu-id="a450b-362">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a450b-362">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="a450b-363">204</span><span class="sxs-lookup"><span data-stu-id="a450b-363">204</span></span>    | <span data-ttu-id="a450b-364">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a450b-364">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="a450b-365">238</span><span class="sxs-lookup"><span data-stu-id="a450b-365">238</span></span>    | <span data-ttu-id="a450b-366">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a450b-366">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="a450b-367">255</span><span class="sxs-lookup"><span data-stu-id="a450b-367">255</span></span>    | <span data-ttu-id="a450b-368">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a450b-368">OEM\_CHARSET</span></span>         |

<span data-ttu-id="a450b-369">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="a450b-369">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="a450b-370">値です。</span><span class="sxs-lookup"><span data-stu-id="a450b-370">Value.</span></span> | <span data-ttu-id="a450b-371">説明。</span><span class="sxs-lookup"><span data-stu-id="a450b-371">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="a450b-372">130</span><span class="sxs-lookup"><span data-stu-id="a450b-372">130</span></span>    | <span data-ttu-id="a450b-373">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a450b-373">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="a450b-374">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="a450b-374">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="a450b-375">値です。</span><span class="sxs-lookup"><span data-stu-id="a450b-375">Value.</span></span> | <span data-ttu-id="a450b-376">説明。</span><span class="sxs-lookup"><span data-stu-id="a450b-376">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="a450b-377">177</span><span class="sxs-lookup"><span data-stu-id="a450b-377">177</span></span>    | <span data-ttu-id="a450b-378">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a450b-378">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="a450b-379">178</span><span class="sxs-lookup"><span data-stu-id="a450b-379">178</span></span>    | <span data-ttu-id="a450b-380">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a450b-380">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="a450b-381">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="a450b-381">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="a450b-382">値です。</span><span class="sxs-lookup"><span data-stu-id="a450b-382">Value.</span></span> | <span data-ttu-id="a450b-383">説明。</span><span class="sxs-lookup"><span data-stu-id="a450b-383">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="a450b-384">222</span><span class="sxs-lookup"><span data-stu-id="a450b-384">222</span></span>    | <span data-ttu-id="a450b-385">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a450b-385">THAI\_CHARSET</span></span> |

<span data-ttu-id="a450b-386">既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="a450b-386">The default character set is set to a value, depending on the current system locale.</span></span> <span data-ttu-id="a450b-387">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="a450b-387">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="a450b-388">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a450b-388">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="a450b-389">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="a450b-389">Method colorScheme</span></span>

<span data-ttu-id="a450b-390">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-390">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="a450b-391">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="a450b-391">Parameters - colorScheme</span></span>

<span data-ttu-id="a450b-392">値</span><span class="sxs-lookup"><span data-stu-id="a450b-392">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="a450b-393">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="a450b-393">Return Value - colorScheme</span></span>

<span data-ttu-id="a450b-394">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="a450b-394">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="a450b-395">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="a450b-395">Remarks - colorScheme</span></span>

<span data-ttu-id="a450b-396">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="a450b-396">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="a450b-397">値です。</span><span class="sxs-lookup"><span data-stu-id="a450b-397">Value.</span></span> | <span data-ttu-id="a450b-398">スタイル。</span><span class="sxs-lookup"><span data-stu-id="a450b-398">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="a450b-399">0</span><span class="sxs-lookup"><span data-stu-id="a450b-399">0</span></span>      | <span data-ttu-id="a450b-400">既定。</span><span class="sxs-lookup"><span data-stu-id="a450b-400">Default.</span></span>                      |
| <span data-ttu-id="a450b-401">1</span><span class="sxs-lookup"><span data-stu-id="a450b-401">1</span></span>      | <span data-ttu-id="a450b-402">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="a450b-402">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="a450b-403">2</span><span class="sxs-lookup"><span data-stu-id="a450b-403">2</span></span>      | <span data-ttu-id="a450b-404">真の配色。</span><span class="sxs-lookup"><span data-stu-id="a450b-404">The true-color scheme.</span></span>        |

## <a name="method-configurationkey"></a><span data-ttu-id="a450b-405">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="a450b-405">Method configurationKey</span></span>

<span data-ttu-id="a450b-406">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-406">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="a450b-407">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="a450b-407">Parameters - configurationKey</span></span>

<span data-ttu-id="a450b-408">値</span><span class="sxs-lookup"><span data-stu-id="a450b-408">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="a450b-409">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="a450b-409">Return Value - configurationKey</span></span>

<span data-ttu-id="a450b-410">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="a450b-410">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="a450b-411">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="a450b-411">Remarks - configurationKey</span></span>

<span data-ttu-id="a450b-412">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a450b-412">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="a450b-413">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="a450b-413">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="a450b-414">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="a450b-414">Method containerId</span></span>

<span data-ttu-id="a450b-415">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="a450b-415">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="a450b-416">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="a450b-416">Return Value - containerId</span></span>

<span data-ttu-id="a450b-417">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="a450b-417">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="a450b-418">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="a450b-418">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="a450b-419">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="a450b-419">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="a450b-420">値</span><span class="sxs-lookup"><span data-stu-id="a450b-420">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="a450b-421">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="a450b-421">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="a450b-422">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="a450b-422">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="a450b-423">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="a450b-423">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="a450b-424">値</span><span class="sxs-lookup"><span data-stu-id="a450b-424">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="a450b-425">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="a450b-425">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="a450b-426">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="a450b-426">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="a450b-427">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="a450b-427">Parameters - dataField</span></span>

<span data-ttu-id="a450b-428">値</span><span class="sxs-lookup"><span data-stu-id="a450b-428">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="a450b-429">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="a450b-429">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="a450b-430">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="a450b-430">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="a450b-431">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="a450b-431">Parameters - dataMethod</span></span>

<span data-ttu-id="a450b-432">値</span><span class="sxs-lookup"><span data-stu-id="a450b-432">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="a450b-433">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="a450b-433">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="a450b-434">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="a450b-434">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="a450b-435">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="a450b-435">Parameters - dataRelationPath</span></span>

<span data-ttu-id="a450b-436">値</span><span class="sxs-lookup"><span data-stu-id="a450b-436">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="a450b-437">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="a450b-437">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="a450b-438">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="a450b-438">Method dataSource</span></span>

<span data-ttu-id="a450b-439">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-439">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="a450b-440">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="a450b-440">Parameters - dataSource</span></span>

<span data-ttu-id="a450b-441">値</span><span class="sxs-lookup"><span data-stu-id="a450b-441">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="a450b-442">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="a450b-442">Return Value - dataSource</span></span>

<span data-ttu-id="a450b-443">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="a450b-443">The identifier of the data source that will be used.</span></span>

## <a name="method-dateday"></a><span data-ttu-id="a450b-444">メソッド dateDay</span><span class="sxs-lookup"><span data-stu-id="a450b-444">Method dateDay</span></span>

```xpp
public int dateDay([int value])
```

### <a name="parameters---dateday"></a><span data-ttu-id="a450b-445">パラメーター - dateDay</span><span class="sxs-lookup"><span data-stu-id="a450b-445">Parameters - dateDay</span></span>

<span data-ttu-id="a450b-446">値</span><span class="sxs-lookup"><span data-stu-id="a450b-446">value</span></span>  

### <a name="return-value---dateday"></a><span data-ttu-id="a450b-447">戻り値 - dateDay</span><span class="sxs-lookup"><span data-stu-id="a450b-447">Return Value - dateDay</span></span>

## <a name="method-dateformat"></a><span data-ttu-id="a450b-448">メソッド dateFormat</span><span class="sxs-lookup"><span data-stu-id="a450b-448">Method dateFormat</span></span>

```xpp
public int dateFormat([int value])
```

### <a name="parameters---dateformat"></a><span data-ttu-id="a450b-449">パラメーター - dateFormat</span><span class="sxs-lookup"><span data-stu-id="a450b-449">Parameters - dateFormat</span></span>

<span data-ttu-id="a450b-450">値</span><span class="sxs-lookup"><span data-stu-id="a450b-450">value</span></span>  

### <a name="return-value---dateformat"></a><span data-ttu-id="a450b-451">戻り値 - dateFormat</span><span class="sxs-lookup"><span data-stu-id="a450b-451">Return Value - dateFormat</span></span>

## <a name="method-datemonth"></a><span data-ttu-id="a450b-452">メソッド dateMonth</span><span class="sxs-lookup"><span data-stu-id="a450b-452">Method dateMonth</span></span>

```xpp
public int dateMonth([int value])
```

### <a name="parameters---datemonth"></a><span data-ttu-id="a450b-453">パラメーター - dateMonth</span><span class="sxs-lookup"><span data-stu-id="a450b-453">Parameters - dateMonth</span></span>

<span data-ttu-id="a450b-454">値</span><span class="sxs-lookup"><span data-stu-id="a450b-454">value</span></span>  

### <a name="return-value---datemonth"></a><span data-ttu-id="a450b-455">戻り値 - dateMonth</span><span class="sxs-lookup"><span data-stu-id="a450b-455">Return Value - dateMonth</span></span>

## <a name="method-dateseparator"></a><span data-ttu-id="a450b-456">メソッド dateSeparator</span><span class="sxs-lookup"><span data-stu-id="a450b-456">Method dateSeparator</span></span>

```xpp
public int dateSeparator([int value])
```

### <a name="parameters---dateseparator"></a><span data-ttu-id="a450b-457">パラメーター - dateSeparator</span><span class="sxs-lookup"><span data-stu-id="a450b-457">Parameters - dateSeparator</span></span>

<span data-ttu-id="a450b-458">値</span><span class="sxs-lookup"><span data-stu-id="a450b-458">value</span></span>  

### <a name="return-value---dateseparator"></a><span data-ttu-id="a450b-459">戻り値 - dateSeparator</span><span class="sxs-lookup"><span data-stu-id="a450b-459">Return Value - dateSeparator</span></span>

## <a name="method-datetimevalue"></a><span data-ttu-id="a450b-460">メソッド dateTimeValue</span><span class="sxs-lookup"><span data-stu-id="a450b-460">Method dateTimeValue</span></span>

```xpp
public DateTime dateTimeValue([DateTime value])
```

### <a name="parameters---datetimevalue"></a><span data-ttu-id="a450b-461">パラメーター - dateTimeValue</span><span class="sxs-lookup"><span data-stu-id="a450b-461">Parameters - dateTimeValue</span></span>

<span data-ttu-id="a450b-462">値</span><span class="sxs-lookup"><span data-stu-id="a450b-462">value</span></span>  

### <a name="return-value---datetimevalue"></a><span data-ttu-id="a450b-463">戻り値 - dateTimeValue</span><span class="sxs-lookup"><span data-stu-id="a450b-463">Return Value - dateTimeValue</span></span>

## <a name="method-dateyear"></a><span data-ttu-id="a450b-464">メソッド dateYear</span><span class="sxs-lookup"><span data-stu-id="a450b-464">Method dateYear</span></span>

```xpp
public int dateYear([int value])
```

### <a name="parameters---dateyear"></a><span data-ttu-id="a450b-465">パラメーター - dateYear</span><span class="sxs-lookup"><span data-stu-id="a450b-465">Parameters - dateYear</span></span>

<span data-ttu-id="a450b-466">値</span><span class="sxs-lookup"><span data-stu-id="a450b-466">value</span></span>  

### <a name="return-value---dateyear"></a><span data-ttu-id="a450b-467">戻り値 - dateYear</span><span class="sxs-lookup"><span data-stu-id="a450b-467">Return Value - dateYear</span></span>

## <a name="method-displayoption"></a><span data-ttu-id="a450b-468">メソッド displayOption</span><span class="sxs-lookup"><span data-stu-id="a450b-468">Method displayOption</span></span>

```xpp
public int displayOption([int value])
```

### <a name="parameters---displayoption"></a><span data-ttu-id="a450b-469">パラメーター - displayOption</span><span class="sxs-lookup"><span data-stu-id="a450b-469">Parameters - displayOption</span></span>

<span data-ttu-id="a450b-470">値</span><span class="sxs-lookup"><span data-stu-id="a450b-470">value</span></span>  

### <a name="return-value---displayoption"></a><span data-ttu-id="a450b-471">戻り値 - displayOption</span><span class="sxs-lookup"><span data-stu-id="a450b-471">Return Value - displayOption</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="a450b-472">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="a450b-472">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="a450b-473">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="a450b-473">Parameters - displayTarget</span></span>

<span data-ttu-id="a450b-474">値</span><span class="sxs-lookup"><span data-stu-id="a450b-474">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="a450b-475">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="a450b-475">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="a450b-476">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="a450b-476">Method dragDrop</span></span>

<span data-ttu-id="a450b-477">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-477">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="a450b-478">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="a450b-478">Parameters - dragDrop</span></span>

<span data-ttu-id="a450b-479">値</span><span class="sxs-lookup"><span data-stu-id="a450b-479">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="a450b-480">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="a450b-480">Return Value - dragDrop</span></span>

<span data-ttu-id="a450b-481">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="a450b-481">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="a450b-482">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="a450b-482">Method enabled</span></span>

<span data-ttu-id="a450b-483">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-483">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="a450b-484">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="a450b-484">Parameters - enabled</span></span>

<span data-ttu-id="a450b-485">値</span><span class="sxs-lookup"><span data-stu-id="a450b-485">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="a450b-486">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="a450b-486">Return Value - enabled</span></span>

<span data-ttu-id="a450b-487">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a450b-487">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="a450b-488">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="a450b-488">Remarks - enabled</span></span>

<span data-ttu-id="a450b-489">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="a450b-489">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="a450b-490">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="a450b-490">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="a450b-491">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="a450b-491">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="a450b-492">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="a450b-492">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="a450b-493">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="a450b-493">Parameters - extendedDataType</span></span>

<span data-ttu-id="a450b-494">値</span><span class="sxs-lookup"><span data-stu-id="a450b-494">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="a450b-495">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="a450b-495">Return Value - extendedDataType</span></span>

## <a name="method-fasttabsummary"></a><span data-ttu-id="a450b-496">メソッド fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="a450b-496">Method fastTabSummary</span></span>

```xpp
public int fastTabSummary([int value])
```

### <a name="parameters---fasttabsummary"></a><span data-ttu-id="a450b-497">パラメーター - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="a450b-497">Parameters - fastTabSummary</span></span>

<span data-ttu-id="a450b-498">値</span><span class="sxs-lookup"><span data-stu-id="a450b-498">value</span></span>  

### <a name="return-value---fasttabsummary"></a><span data-ttu-id="a450b-499">戻り値 - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="a450b-499">Return Value - fastTabSummary</span></span>

## <a name="method-font"></a><span data-ttu-id="a450b-500">メソッド font</span><span class="sxs-lookup"><span data-stu-id="a450b-500">Method font</span></span>

<span data-ttu-id="a450b-501">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-501">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="a450b-502">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="a450b-502">Parameters - font</span></span>

<span data-ttu-id="a450b-503">値</span><span class="sxs-lookup"><span data-stu-id="a450b-503">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="a450b-504">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="a450b-504">Return Value - font</span></span>

<span data-ttu-id="a450b-505">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="a450b-505">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="a450b-506">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="a450b-506">Method fontSize</span></span>

<span data-ttu-id="a450b-507">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-507">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="a450b-508">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="a450b-508">Parameters - fontSize</span></span>

<span data-ttu-id="a450b-509">値</span><span class="sxs-lookup"><span data-stu-id="a450b-509">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="a450b-510">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="a450b-510">Return Value - fontSize</span></span>

<span data-ttu-id="a450b-511">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="a450b-511">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="a450b-512">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="a450b-512">Method foregroundColor</span></span>

<span data-ttu-id="a450b-513">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-513">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="a450b-514">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="a450b-514">Parameters - foregroundColor</span></span>

<span data-ttu-id="a450b-515">値</span><span class="sxs-lookup"><span data-stu-id="a450b-515">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="a450b-516">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="a450b-516">Return Value - foregroundColor</span></span>

<span data-ttu-id="a450b-517">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="a450b-517">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="a450b-518">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="a450b-518">Remarks - foregroundColor</span></span>

<span data-ttu-id="a450b-519">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a450b-519">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="a450b-520">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a450b-520">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="a450b-521">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="a450b-521">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="a450b-522">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="a450b-522">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="a450b-523">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="a450b-523">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="a450b-524">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="a450b-524">The maximum value for a single byte is 255.</span></span>

## <a name="method-height"></a><span data-ttu-id="a450b-525">メソッド height</span><span class="sxs-lookup"><span data-stu-id="a450b-525">Method height</span></span>

<span data-ttu-id="a450b-526">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-526">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="a450b-527">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="a450b-527">Parameters - height</span></span>

<span data-ttu-id="a450b-528">値</span><span class="sxs-lookup"><span data-stu-id="a450b-528">value</span></span>  

<!-- -->

<span data-ttu-id="a450b-529">モード</span><span class="sxs-lookup"><span data-stu-id="a450b-529">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="a450b-530">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="a450b-530">Return Value - height</span></span>

<span data-ttu-id="a450b-531">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="a450b-531">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="a450b-532">備考 - height</span><span class="sxs-lookup"><span data-stu-id="a450b-532">Remarks - height</span></span>

<span data-ttu-id="a450b-533">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a450b-533">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="a450b-534">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="a450b-534">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="a450b-535">モード。</span><span class="sxs-lookup"><span data-stu-id="a450b-535">Mode.</span></span>            | <span data-ttu-id="a450b-536">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="a450b-536">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a450b-537">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="a450b-537">-1 Exact.</span></span>        | <span data-ttu-id="a450b-538">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a450b-538">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="a450b-539">0 自動。</span><span class="sxs-lookup"><span data-stu-id="a450b-539">0 Auto.</span></span>          | <span data-ttu-id="a450b-540">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a450b-540">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="a450b-541">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="a450b-541">1 Column height.</span></span> | <span data-ttu-id="a450b-542">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="a450b-542">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="a450b-543">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="a450b-543">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="a450b-544">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="a450b-544">Method heightMode</span></span>

<span data-ttu-id="a450b-545">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-545">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="a450b-546">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="a450b-546">Parameters - heightMode</span></span>

<span data-ttu-id="a450b-547">値</span><span class="sxs-lookup"><span data-stu-id="a450b-547">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="a450b-548">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="a450b-548">Return Value - heightMode</span></span>

<span data-ttu-id="a450b-549">計算モード。</span><span class="sxs-lookup"><span data-stu-id="a450b-549">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="a450b-550">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="a450b-550">Remarks - heightMode</span></span>

<span data-ttu-id="a450b-551">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="a450b-551">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="a450b-552">モード。</span><span class="sxs-lookup"><span data-stu-id="a450b-552">Mode.</span></span>          | <span data-ttu-id="a450b-553">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="a450b-553">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a450b-554">正確。</span><span class="sxs-lookup"><span data-stu-id="a450b-554">Exact.</span></span>         | <span data-ttu-id="a450b-555">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a450b-555">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="a450b-556">自動。</span><span class="sxs-lookup"><span data-stu-id="a450b-556">Auto.</span></span>          | <span data-ttu-id="a450b-557">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a450b-557">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="a450b-558">列の高さ</span><span class="sxs-lookup"><span data-stu-id="a450b-558">Column height.</span></span> | <span data-ttu-id="a450b-559">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="a450b-559">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="a450b-560">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="a450b-560">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="a450b-561">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="a450b-561">Method heightValue</span></span>

<span data-ttu-id="a450b-562">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-562">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="a450b-563">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="a450b-563">Parameters - heightValue</span></span>

<span data-ttu-id="a450b-564">値</span><span class="sxs-lookup"><span data-stu-id="a450b-564">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="a450b-565">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="a450b-565">Return Value - heightValue</span></span>

<span data-ttu-id="a450b-566">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="a450b-566">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="a450b-567">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="a450b-567">Remarks - heightValue</span></span>

<span data-ttu-id="a450b-568">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="a450b-568">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="a450b-569">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="a450b-569">Method helpText</span></span>

<span data-ttu-id="a450b-570">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-570">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="a450b-571">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="a450b-571">Parameters - helpText</span></span>

<span data-ttu-id="a450b-572">値</span><span class="sxs-lookup"><span data-stu-id="a450b-572">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="a450b-573">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="a450b-573">Return Value - helpText</span></span>

<span data-ttu-id="a450b-574">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="a450b-574">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="a450b-575">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="a450b-575">Remarks - helpText</span></span>

<span data-ttu-id="a450b-576">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-576">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="a450b-577">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="a450b-577">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="a450b-578">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="a450b-578">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="a450b-579">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="a450b-579">Parameters - hierarchyParent</span></span>

<span data-ttu-id="a450b-580">値</span><span class="sxs-lookup"><span data-stu-id="a450b-580">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="a450b-581">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="a450b-581">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="a450b-582">メソッド id</span><span class="sxs-lookup"><span data-stu-id="a450b-582">Method id</span></span>

<span data-ttu-id="a450b-583">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="a450b-583">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="a450b-584">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="a450b-584">Return Value - id</span></span>

<span data-ttu-id="a450b-585">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="a450b-585">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="a450b-586">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="a450b-586">Method isContainer</span></span>

<span data-ttu-id="a450b-587">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="a450b-587">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="a450b-588">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="a450b-588">Return Value - isContainer</span></span>

<span data-ttu-id="a450b-589">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a450b-589">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-italic"></a><span data-ttu-id="a450b-590">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="a450b-590">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="a450b-591">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="a450b-591">Parameters - italic</span></span>

<span data-ttu-id="a450b-592">値</span><span class="sxs-lookup"><span data-stu-id="a450b-592">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="a450b-593">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="a450b-593">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="a450b-594">メソッド label</span><span class="sxs-lookup"><span data-stu-id="a450b-594">Method label</span></span>

<span data-ttu-id="a450b-595">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-595">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="a450b-596">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="a450b-596">Parameters - label</span></span>

<span data-ttu-id="a450b-597">値</span><span class="sxs-lookup"><span data-stu-id="a450b-597">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="a450b-598">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="a450b-598">Return Value - label</span></span>

<span data-ttu-id="a450b-599">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="a450b-599">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="a450b-600">備考 - label</span><span class="sxs-lookup"><span data-stu-id="a450b-600">Remarks - label</span></span>

<span data-ttu-id="a450b-601">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-601">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="a450b-602">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="a450b-602">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="a450b-603">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="a450b-603">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="a450b-604">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="a450b-604">Parameters - labelAlignment</span></span>

<span data-ttu-id="a450b-605">値</span><span class="sxs-lookup"><span data-stu-id="a450b-605">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="a450b-606">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="a450b-606">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="a450b-607">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="a450b-607">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="a450b-608">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="a450b-608">Parameters - labelBold</span></span>

<span data-ttu-id="a450b-609">値</span><span class="sxs-lookup"><span data-stu-id="a450b-609">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="a450b-610">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="a450b-610">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="a450b-611">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="a450b-611">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="a450b-612">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="a450b-612">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="a450b-613">値</span><span class="sxs-lookup"><span data-stu-id="a450b-613">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="a450b-614">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="a450b-614">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="a450b-615">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="a450b-615">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="a450b-616">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="a450b-616">Parameters - labelFont</span></span>

<span data-ttu-id="a450b-617">値</span><span class="sxs-lookup"><span data-stu-id="a450b-617">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="a450b-618">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="a450b-618">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="a450b-619">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="a450b-619">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="a450b-620">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="a450b-620">Parameters - labelFontSize</span></span>

<span data-ttu-id="a450b-621">値</span><span class="sxs-lookup"><span data-stu-id="a450b-621">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="a450b-622">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="a450b-622">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="a450b-623">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="a450b-623">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="a450b-624">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="a450b-624">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="a450b-625">値</span><span class="sxs-lookup"><span data-stu-id="a450b-625">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="a450b-626">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="a450b-626">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="a450b-627">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="a450b-627">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="a450b-628">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="a450b-628">Parameters - labelGuide</span></span>

<span data-ttu-id="a450b-629">値</span><span class="sxs-lookup"><span data-stu-id="a450b-629">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="a450b-630">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="a450b-630">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="a450b-631">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="a450b-631">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="a450b-632">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="a450b-632">Parameters - labelHeight</span></span>

<span data-ttu-id="a450b-633">値</span><span class="sxs-lookup"><span data-stu-id="a450b-633">value</span></span>  

<!-- -->

<span data-ttu-id="a450b-634">モード</span><span class="sxs-lookup"><span data-stu-id="a450b-634">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="a450b-635">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="a450b-635">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="a450b-636">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="a450b-636">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="a450b-637">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="a450b-637">Parameters - labelHeightMode</span></span>

<span data-ttu-id="a450b-638">値</span><span class="sxs-lookup"><span data-stu-id="a450b-638">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="a450b-639">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="a450b-639">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="a450b-640">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="a450b-640">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="a450b-641">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="a450b-641">Parameters - labelHeightValue</span></span>

<span data-ttu-id="a450b-642">値</span><span class="sxs-lookup"><span data-stu-id="a450b-642">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="a450b-643">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="a450b-643">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="a450b-644">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="a450b-644">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="a450b-645">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="a450b-645">Parameters - labelItalic</span></span>

<span data-ttu-id="a450b-646">値</span><span class="sxs-lookup"><span data-stu-id="a450b-646">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="a450b-647">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="a450b-647">Return Value - labelItalic</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="a450b-648">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="a450b-648">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="a450b-649">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="a450b-649">Parameters - labelPosition</span></span>

<span data-ttu-id="a450b-650">値</span><span class="sxs-lookup"><span data-stu-id="a450b-650">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="a450b-651">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="a450b-651">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="a450b-652">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="a450b-652">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="a450b-653">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="a450b-653">Parameters - labelUnderline</span></span>

<span data-ttu-id="a450b-654">値</span><span class="sxs-lookup"><span data-stu-id="a450b-654">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="a450b-655">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="a450b-655">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="a450b-656">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="a450b-656">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="a450b-657">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="a450b-657">Parameters - labelWidth</span></span>

<span data-ttu-id="a450b-658">値</span><span class="sxs-lookup"><span data-stu-id="a450b-658">value</span></span>  

<!-- -->

<span data-ttu-id="a450b-659">モード</span><span class="sxs-lookup"><span data-stu-id="a450b-659">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="a450b-660">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="a450b-660">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="a450b-661">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="a450b-661">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="a450b-662">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="a450b-662">Parameters - labelWidthMode</span></span>

<span data-ttu-id="a450b-663">値</span><span class="sxs-lookup"><span data-stu-id="a450b-663">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="a450b-664">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="a450b-664">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="a450b-665">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="a450b-665">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="a450b-666">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="a450b-666">Parameters - labelWidthValue</span></span>

<span data-ttu-id="a450b-667">値</span><span class="sxs-lookup"><span data-stu-id="a450b-667">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="a450b-668">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="a450b-668">Return Value - labelWidthValue</span></span>

## <a name="method-left"></a><span data-ttu-id="a450b-669">メソッド left</span><span class="sxs-lookup"><span data-stu-id="a450b-669">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="a450b-670">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="a450b-670">Parameters - left</span></span>

<span data-ttu-id="a450b-671">値</span><span class="sxs-lookup"><span data-stu-id="a450b-671">value</span></span>  

<!-- -->

<span data-ttu-id="a450b-672">モード</span><span class="sxs-lookup"><span data-stu-id="a450b-672">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="a450b-673">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="a450b-673">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="a450b-674">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="a450b-674">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="a450b-675">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="a450b-675">Parameters - leftMode</span></span>

<span data-ttu-id="a450b-676">値</span><span class="sxs-lookup"><span data-stu-id="a450b-676">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="a450b-677">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="a450b-677">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="a450b-678">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="a450b-678">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="a450b-679">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="a450b-679">Parameters - leftValue</span></span>

<span data-ttu-id="a450b-680">値</span><span class="sxs-lookup"><span data-stu-id="a450b-680">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="a450b-681">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="a450b-681">Return Value - leftValue</span></span>

## <a name="method-limittext"></a><span data-ttu-id="a450b-682">メソッド limitText</span><span class="sxs-lookup"><span data-stu-id="a450b-682">Method limitText</span></span>

```xpp
public int limitText([int value], [AutoMode mode])
```

### <a name="parameters---limittext"></a><span data-ttu-id="a450b-683">パラメーター - limitText</span><span class="sxs-lookup"><span data-stu-id="a450b-683">Parameters - limitText</span></span>

<span data-ttu-id="a450b-684">値</span><span class="sxs-lookup"><span data-stu-id="a450b-684">value</span></span>  

<!-- -->

<span data-ttu-id="a450b-685">モード</span><span class="sxs-lookup"><span data-stu-id="a450b-685">mode</span></span>  

### <a name="return-value---limittext"></a><span data-ttu-id="a450b-686">戻り値 - limitText</span><span class="sxs-lookup"><span data-stu-id="a450b-686">Return Value - limitText</span></span>

## <a name="method-limittextmode"></a><span data-ttu-id="a450b-687">メソッド limitTextMode</span><span class="sxs-lookup"><span data-stu-id="a450b-687">Method limitTextMode</span></span>

```xpp
public AutoMode limitTextMode([AutoMode mode])
```

### <a name="parameters---limittextmode"></a><span data-ttu-id="a450b-688">パラメーター - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="a450b-688">Parameters - limitTextMode</span></span>

<span data-ttu-id="a450b-689">モード</span><span class="sxs-lookup"><span data-stu-id="a450b-689">mode</span></span>  

### <a name="return-value---limittextmode"></a><span data-ttu-id="a450b-690">戻り値 - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="a450b-690">Return Value - limitTextMode</span></span>

## <a name="method-limittextvalue"></a><span data-ttu-id="a450b-691">メソッド limitTextValue</span><span class="sxs-lookup"><span data-stu-id="a450b-691">Method limitTextValue</span></span>

```xpp
public int limitTextValue([int value])
```

### <a name="parameters---limittextvalue"></a><span data-ttu-id="a450b-692">パラメーター - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="a450b-692">Parameters - limitTextValue</span></span>

<span data-ttu-id="a450b-693">値</span><span class="sxs-lookup"><span data-stu-id="a450b-693">value</span></span>  

### <a name="return-value---limittextvalue"></a><span data-ttu-id="a450b-694">戻り値 - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="a450b-694">Return Value - limitTextValue</span></span>

## <a name="method-lookupbutton"></a><span data-ttu-id="a450b-695">メソッド lookupButton</span><span class="sxs-lookup"><span data-stu-id="a450b-695">Method lookupButton</span></span>

```xpp
public int lookupButton([int value])
```

### <a name="parameters---lookupbutton"></a><span data-ttu-id="a450b-696">パラメーター - lookupButton</span><span class="sxs-lookup"><span data-stu-id="a450b-696">Parameters - lookupButton</span></span>

<span data-ttu-id="a450b-697">値</span><span class="sxs-lookup"><span data-stu-id="a450b-697">value</span></span>  

### <a name="return-value---lookupbutton"></a><span data-ttu-id="a450b-698">戻り値 - lookupButton</span><span class="sxs-lookup"><span data-stu-id="a450b-698">Return Value - lookupButton</span></span>

## <a name="method-mandatory"></a><span data-ttu-id="a450b-699">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="a450b-699">Method mandatory</span></span>

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a><span data-ttu-id="a450b-700">パラメーター - mandatory</span><span class="sxs-lookup"><span data-stu-id="a450b-700">Parameters - mandatory</span></span>

<span data-ttu-id="a450b-701">値</span><span class="sxs-lookup"><span data-stu-id="a450b-701">value</span></span>  

### <a name="return-value---mandatory"></a><span data-ttu-id="a450b-702">戻り値 - mandatory</span><span class="sxs-lookup"><span data-stu-id="a450b-702">Return Value - mandatory</span></span>

## <a name="method-maxdatelabel"></a><span data-ttu-id="a450b-703">メソッド maxDateLabel</span><span class="sxs-lookup"><span data-stu-id="a450b-703">Method maxDateLabel</span></span>

```xpp
public str maxDateLabel([str value])
```

### <a name="parameters---maxdatelabel"></a><span data-ttu-id="a450b-704">パラメーター - maxDateLabel</span><span class="sxs-lookup"><span data-stu-id="a450b-704">Parameters - maxDateLabel</span></span>

<span data-ttu-id="a450b-705">値</span><span class="sxs-lookup"><span data-stu-id="a450b-705">value</span></span>  

### <a name="return-value---maxdatelabel"></a><span data-ttu-id="a450b-706">戻り値 - maxDateLabel</span><span class="sxs-lookup"><span data-stu-id="a450b-706">Return Value - maxDateLabel</span></span>

## <a name="method-name"></a><span data-ttu-id="a450b-707">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a450b-707">Method name</span></span>

<span data-ttu-id="a450b-708">フォーム、レポート、テーブル、クエリ、または別のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-708">Gets or sets the name that is used in code to identify a form, report, table, query, or another application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="a450b-709">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="a450b-709">Parameters - name</span></span>

<span data-ttu-id="a450b-710">値</span><span class="sxs-lookup"><span data-stu-id="a450b-710">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="a450b-711">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="a450b-711">Return Value - name</span></span>

<span data-ttu-id="a450b-712">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="a450b-712">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="a450b-713">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="a450b-713">Remarks - name</span></span>

<span data-ttu-id="a450b-714">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a450b-714">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="a450b-715">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="a450b-715">Begins with a letter.</span></span>
-   <span data-ttu-id="a450b-716">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="a450b-716">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="a450b-717">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="a450b-717">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="a450b-718">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="a450b-718">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="a450b-719">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="a450b-719">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, classes, and so on.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="a450b-720">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="a450b-720">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="a450b-721">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="a450b-721">Parameters - neededPermission</span></span>

<span data-ttu-id="a450b-722">値</span><span class="sxs-lookup"><span data-stu-id="a450b-722">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="a450b-723">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="a450b-723">Return Value - neededPermission</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="a450b-724">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="a450b-724">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="a450b-725">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="a450b-725">Parameters - promptrect</span></span>

<span data-ttu-id="a450b-726">値</span><span class="sxs-lookup"><span data-stu-id="a450b-726">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="a450b-727">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="a450b-727">Return Value - promptrect</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="a450b-728">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="a450b-728">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="a450b-729">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="a450b-729">Parameters - securityKey</span></span>

<span data-ttu-id="a450b-730">値</span><span class="sxs-lookup"><span data-stu-id="a450b-730">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="a450b-731">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="a450b-731">Return Value - securityKey</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="a450b-732">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="a450b-732">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="a450b-733">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="a450b-733">Parameters - showLabel</span></span>

<span data-ttu-id="a450b-734">値</span><span class="sxs-lookup"><span data-stu-id="a450b-734">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="a450b-735">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="a450b-735">Return Value - showLabel</span></span>

## <a name="method-skip"></a><span data-ttu-id="a450b-736">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="a450b-736">Method skip</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="a450b-737">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="a450b-737">Parameters - skip</span></span>

<span data-ttu-id="a450b-738">値</span><span class="sxs-lookup"><span data-stu-id="a450b-738">value</span></span>  

### <a name="return-value---skip"></a><span data-ttu-id="a450b-739">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="a450b-739">Return Value - skip</span></span>

## <a name="method-timeformat"></a><span data-ttu-id="a450b-740">メソッド timeFormat</span><span class="sxs-lookup"><span data-stu-id="a450b-740">Method timeFormat</span></span>

```xpp
public int timeFormat([int value])
```

### <a name="parameters---timeformat"></a><span data-ttu-id="a450b-741">パラメーター - timeFormat</span><span class="sxs-lookup"><span data-stu-id="a450b-741">Parameters - timeFormat</span></span>

<span data-ttu-id="a450b-742">値</span><span class="sxs-lookup"><span data-stu-id="a450b-742">value</span></span>  

### <a name="return-value---timeformat"></a><span data-ttu-id="a450b-743">戻り値 - timeFormat</span><span class="sxs-lookup"><span data-stu-id="a450b-743">Return Value - timeFormat</span></span>

## <a name="method-timehours"></a><span data-ttu-id="a450b-744">メソッド timeHours</span><span class="sxs-lookup"><span data-stu-id="a450b-744">Method timeHours</span></span>

```xpp
public int timeHours([int value])
```

### <a name="parameters---timehours"></a><span data-ttu-id="a450b-745">パラメーター - timeHours</span><span class="sxs-lookup"><span data-stu-id="a450b-745">Parameters - timeHours</span></span>

<span data-ttu-id="a450b-746">値</span><span class="sxs-lookup"><span data-stu-id="a450b-746">value</span></span>  

### <a name="return-value---timehours"></a><span data-ttu-id="a450b-747">戻り値 - timeHours</span><span class="sxs-lookup"><span data-stu-id="a450b-747">Return Value - timeHours</span></span>

## <a name="method-timeminute"></a><span data-ttu-id="a450b-748">メソッド timeMinute</span><span class="sxs-lookup"><span data-stu-id="a450b-748">Method timeMinute</span></span>

```xpp
public int timeMinute([int value])
```

### <a name="parameters---timeminute"></a><span data-ttu-id="a450b-749">パラメーター - timeMinute</span><span class="sxs-lookup"><span data-stu-id="a450b-749">Parameters - timeMinute</span></span>

<span data-ttu-id="a450b-750">値</span><span class="sxs-lookup"><span data-stu-id="a450b-750">value</span></span>  

### <a name="return-value---timeminute"></a><span data-ttu-id="a450b-751">戻り値 - timeMinute</span><span class="sxs-lookup"><span data-stu-id="a450b-751">Return Value - timeMinute</span></span>

## <a name="method-timeseconds"></a><span data-ttu-id="a450b-752">メソッド timeSeconds</span><span class="sxs-lookup"><span data-stu-id="a450b-752">Method timeSeconds</span></span>

```xpp
public int timeSeconds([int value])
```

### <a name="parameters---timeseconds"></a><span data-ttu-id="a450b-753">パラメーター - timeSeconds</span><span class="sxs-lookup"><span data-stu-id="a450b-753">Parameters - timeSeconds</span></span>

<span data-ttu-id="a450b-754">値</span><span class="sxs-lookup"><span data-stu-id="a450b-754">value</span></span>  

### <a name="return-value---timeseconds"></a><span data-ttu-id="a450b-755">戻り値 - timeSeconds</span><span class="sxs-lookup"><span data-stu-id="a450b-755">Return Value - timeSeconds</span></span>

## <a name="method-timeseparator"></a><span data-ttu-id="a450b-756">メソッド timeSeparator</span><span class="sxs-lookup"><span data-stu-id="a450b-756">Method timeSeparator</span></span>

```xpp
public int timeSeparator([int value])
```

### <a name="parameters---timeseparator"></a><span data-ttu-id="a450b-757">パラメーター - timeSeparator</span><span class="sxs-lookup"><span data-stu-id="a450b-757">Parameters - timeSeparator</span></span>

<span data-ttu-id="a450b-758">値</span><span class="sxs-lookup"><span data-stu-id="a450b-758">value</span></span>  

### <a name="return-value---timeseparator"></a><span data-ttu-id="a450b-759">戻り値 - timeSeparator</span><span class="sxs-lookup"><span data-stu-id="a450b-759">Return Value - timeSeparator</span></span>

## <a name="method-timezoneindicator"></a><span data-ttu-id="a450b-760">メソッド timeZoneIndicator</span><span class="sxs-lookup"><span data-stu-id="a450b-760">Method timeZoneIndicator</span></span>

```xpp
public int timeZoneIndicator([int value])
```

### <a name="parameters---timezoneindicator"></a><span data-ttu-id="a450b-761">パラメーター - timeZoneIndicator</span><span class="sxs-lookup"><span data-stu-id="a450b-761">Parameters - timeZoneIndicator</span></span>

<span data-ttu-id="a450b-762">値</span><span class="sxs-lookup"><span data-stu-id="a450b-762">value</span></span>  

### <a name="return-value---timezoneindicator"></a><span data-ttu-id="a450b-763">戻り値 - timeZoneIndicator</span><span class="sxs-lookup"><span data-stu-id="a450b-763">Return Value - timeZoneIndicator</span></span>

## <a name="method-timezonepreference"></a><span data-ttu-id="a450b-764">メソッド timezonePreference</span><span class="sxs-lookup"><span data-stu-id="a450b-764">Method timezonePreference</span></span>

```xpp
public int timezonePreference([int value])
```

### <a name="parameters---timezonepreference"></a><span data-ttu-id="a450b-765">パラメーター - timezonePreference</span><span class="sxs-lookup"><span data-stu-id="a450b-765">Parameters - timezonePreference</span></span>

<span data-ttu-id="a450b-766">値</span><span class="sxs-lookup"><span data-stu-id="a450b-766">value</span></span>  

### <a name="return-value---timezonepreference"></a><span data-ttu-id="a450b-767">戻り値 - timezonePreference</span><span class="sxs-lookup"><span data-stu-id="a450b-767">Return Value - timezonePreference</span></span>

## <a name="method-top"></a><span data-ttu-id="a450b-768">メソッド top</span><span class="sxs-lookup"><span data-stu-id="a450b-768">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="a450b-769">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="a450b-769">Parameters - top</span></span>

<span data-ttu-id="a450b-770">値</span><span class="sxs-lookup"><span data-stu-id="a450b-770">value</span></span>  

<!-- -->

<span data-ttu-id="a450b-771">モード</span><span class="sxs-lookup"><span data-stu-id="a450b-771">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="a450b-772">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="a450b-772">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="a450b-773">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="a450b-773">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="a450b-774">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="a450b-774">Parameters - topMode</span></span>

<span data-ttu-id="a450b-775">値</span><span class="sxs-lookup"><span data-stu-id="a450b-775">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="a450b-776">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="a450b-776">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="a450b-777">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="a450b-777">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="a450b-778">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="a450b-778">Parameters - topValue</span></span>

<span data-ttu-id="a450b-779">値</span><span class="sxs-lookup"><span data-stu-id="a450b-779">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="a450b-780">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="a450b-780">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="a450b-781">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="a450b-781">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="a450b-782">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="a450b-782">Parameters - type</span></span>

<span data-ttu-id="a450b-783">値</span><span class="sxs-lookup"><span data-stu-id="a450b-783">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="a450b-784">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="a450b-784">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="a450b-785">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="a450b-785">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="a450b-786">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="a450b-786">Parameters - underline</span></span>

<span data-ttu-id="a450b-787">値</span><span class="sxs-lookup"><span data-stu-id="a450b-787">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="a450b-788">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="a450b-788">Return Value - underline</span></span>

## <a name="method-userdata"></a><span data-ttu-id="a450b-789">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="a450b-789">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="a450b-790">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="a450b-790">Parameters - userData</span></span>

<span data-ttu-id="a450b-791">値</span><span class="sxs-lookup"><span data-stu-id="a450b-791">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="a450b-792">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="a450b-792">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="a450b-793">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="a450b-793">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="a450b-794">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="a450b-794">Parameters - userDataItem</span></span>

<span data-ttu-id="a450b-795">値</span><span class="sxs-lookup"><span data-stu-id="a450b-795">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="a450b-796">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="a450b-796">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="a450b-797">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="a450b-797">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="a450b-798">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="a450b-798">Parameters - userDataItems</span></span>

<span data-ttu-id="a450b-799">値</span><span class="sxs-lookup"><span data-stu-id="a450b-799">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="a450b-800">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="a450b-800">Return Value - userDataItems</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="a450b-801">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="a450b-801">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="a450b-802">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="a450b-802">Parameters - verticalSpacing</span></span>

<span data-ttu-id="a450b-803">値</span><span class="sxs-lookup"><span data-stu-id="a450b-803">value</span></span>  

<!-- -->

<span data-ttu-id="a450b-804">モード</span><span class="sxs-lookup"><span data-stu-id="a450b-804">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="a450b-805">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="a450b-805">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="a450b-806">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="a450b-806">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="a450b-807">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="a450b-807">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="a450b-808">モード</span><span class="sxs-lookup"><span data-stu-id="a450b-808">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="a450b-809">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="a450b-809">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="a450b-810">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="a450b-810">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="a450b-811">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="a450b-811">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="a450b-812">値</span><span class="sxs-lookup"><span data-stu-id="a450b-812">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="a450b-813">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="a450b-813">Return Value - verticalSpacingValue</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="a450b-814">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="a450b-814">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="a450b-815">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="a450b-815">Parameters - viewEditMode</span></span>

<span data-ttu-id="a450b-816">値</span><span class="sxs-lookup"><span data-stu-id="a450b-816">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="a450b-817">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="a450b-817">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="a450b-818">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="a450b-818">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="a450b-819">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="a450b-819">Parameters - visible</span></span>

<span data-ttu-id="a450b-820">値</span><span class="sxs-lookup"><span data-stu-id="a450b-820">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="a450b-821">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="a450b-821">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="a450b-822">メソッド width</span><span class="sxs-lookup"><span data-stu-id="a450b-822">Method width</span></span>

<span data-ttu-id="a450b-823">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-823">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="a450b-824">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="a450b-824">Parameters - width</span></span>

<span data-ttu-id="a450b-825">値</span><span class="sxs-lookup"><span data-stu-id="a450b-825">value</span></span>  

<!-- -->

<span data-ttu-id="a450b-826">モード</span><span class="sxs-lookup"><span data-stu-id="a450b-826">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="a450b-827">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="a450b-827">Return Value - width</span></span>

<span data-ttu-id="a450b-828">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="a450b-828">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="a450b-829">備考 - width</span><span class="sxs-lookup"><span data-stu-id="a450b-829">Remarks - width</span></span>

<span data-ttu-id="a450b-830">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a450b-830">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="a450b-831">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="a450b-831">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="a450b-832">モード。</span><span class="sxs-lookup"><span data-stu-id="a450b-832">Mode.</span></span>           | <span data-ttu-id="a450b-833">幅計算。</span><span class="sxs-lookup"><span data-stu-id="a450b-833">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a450b-834">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="a450b-834">-1 Exact.</span></span>       | <span data-ttu-id="a450b-835">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a450b-835">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="a450b-836">0 自動。</span><span class="sxs-lookup"><span data-stu-id="a450b-836">0 Auto.</span></span>         | <span data-ttu-id="a450b-837">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a450b-837">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="a450b-838">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="a450b-838">1 Column width.</span></span> | <span data-ttu-id="a450b-839">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="a450b-839">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="a450b-840">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="a450b-840">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="a450b-841">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="a450b-841">Method widthMode</span></span>

<span data-ttu-id="a450b-842">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-842">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="a450b-843">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="a450b-843">Parameters - widthMode</span></span>

<span data-ttu-id="a450b-844">値</span><span class="sxs-lookup"><span data-stu-id="a450b-844">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="a450b-845">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="a450b-845">Return Value - widthMode</span></span>

<span data-ttu-id="a450b-846">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a450b-846">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="a450b-847">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="a450b-847">Remarks - widthMode</span></span>

<span data-ttu-id="a450b-848">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="a450b-848">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="a450b-849">モード。</span><span class="sxs-lookup"><span data-stu-id="a450b-849">Mode.</span></span>         | <span data-ttu-id="a450b-850">幅計算。</span><span class="sxs-lookup"><span data-stu-id="a450b-850">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a450b-851">正確。</span><span class="sxs-lookup"><span data-stu-id="a450b-851">Exact.</span></span>        | <span data-ttu-id="a450b-852">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a450b-852">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="a450b-853">自動。</span><span class="sxs-lookup"><span data-stu-id="a450b-853">Auto.</span></span>         | <span data-ttu-id="a450b-854">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a450b-854">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="a450b-855">列の幅。</span><span class="sxs-lookup"><span data-stu-id="a450b-855">Column width.</span></span> | <span data-ttu-id="a450b-856">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="a450b-856">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="a450b-857">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="a450b-857">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="a450b-858">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="a450b-858">Method widthValue</span></span>

<span data-ttu-id="a450b-859">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a450b-859">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="a450b-860">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="a450b-860">Parameters - widthValue</span></span>

<span data-ttu-id="a450b-861">値</span><span class="sxs-lookup"><span data-stu-id="a450b-861">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="a450b-862">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="a450b-862">Return Value - widthValue</span></span>

<span data-ttu-id="a450b-863">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="a450b-863">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="a450b-864">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="a450b-864">Remarks - widthValue</span></span>

<span data-ttu-id="a450b-865">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="a450b-865">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="a450b-866">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="a450b-866">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="a450b-867">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="a450b-867">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="a450b-868">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="a450b-868">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="a450b-869">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="a450b-869">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="a450b-870">overrideObject</span><span class="sxs-lookup"><span data-stu-id="a450b-870">overrideObject</span></span>  

