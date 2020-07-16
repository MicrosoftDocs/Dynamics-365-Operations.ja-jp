---
title: FormBuildComboBoxControl クラス
description: このトピックでは、FormBuildComboBoxControl クラスについて説明します。
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
ms.openlocfilehash: adfb4803b2ec86a0ac3f60ca5cf040dfe9fb67b6
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502974"
---
# <a name="class-formbuildcomboboxcontrol"></a><span data-ttu-id="6d765-103">クラス FormBuildComboBoxControl</span><span class="sxs-lookup"><span data-stu-id="6d765-103">Class FormBuildComboBoxControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildComboBoxControl extends FormBuildControl
```

<span data-ttu-id="6d765-104">FormBuildComboBoxControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="6d765-104">The FormBuildComboBoxControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d765-105">備考</span><span class="sxs-lookup"><span data-stu-id="6d765-105">Remarks</span></span>

<span data-ttu-id="6d765-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6d765-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="6d765-107">例</span><span class="sxs-lookup"><span data-stu-id="6d765-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="6d765-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="6d765-108">Methods</span></span>

| <span data-ttu-id="6d765-109">方法</span><span class="sxs-lookup"><span data-stu-id="6d765-109">Method</span></span>                                                                                                      | <span data-ttu-id="6d765-110">説明</span><span class="sxs-lookup"><span data-stu-id="6d765-110">Description</span></span>                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d765-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="6d765-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-112">Determines whether to align the control.</span></span>                                                                                                      |
| <span data-ttu-id="6d765-113">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-113">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="6d765-114">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-114">Determines whether the user can change the contents of the control.</span></span>                                                                           |
| <span data-ttu-id="6d765-115">public boolean appendNew(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-115">public boolean appendNew(\[boolean value\])</span></span>                                                                 |                                                                                                                                               |
| <span data-ttu-id="6d765-116">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-116">public int arrayIndex(\[int value\])</span></span>                                                                        |                                                                                                                                               |
| <span data-ttu-id="6d765-117">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-117">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="6d765-118">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-118">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                            |
| <span data-ttu-id="6d765-119">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-119">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="6d765-120">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-120">Gets or sets the background color of the control.</span></span>                                                                                             |
| <span data-ttu-id="6d765-121">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-121">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="6d765-122">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-122">Determines whether the control background can be transparent.</span></span>                                                                                |
| <span data-ttu-id="6d765-123">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-123">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="6d765-124">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-124">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                                   |
| <span data-ttu-id="6d765-125">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-125">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="6d765-126">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-126">Gets or sets the style of the borderline of the control.</span></span>                                                                                      |
| <span data-ttu-id="6d765-127">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-127">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="6d765-128">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-128">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="6d765-129">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-129">Gets or sets the character set of the font.</span></span>                                                                                                   |
| <span data-ttu-id="6d765-130">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-130">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="6d765-131">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-131">Gets or sets the color scheme of the control.</span></span>                                                                                                 |
| <span data-ttu-id="6d765-132">public int comboType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-132">public int comboType(\[int value\])</span></span>                                                                         |                                                                                                                                               |
| <span data-ttu-id="6d765-133">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-133">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="6d765-134">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-134">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                           |
| <span data-ttu-id="6d765-135">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="6d765-135">public int containerId()</span></span>                                                                                    | <span data-ttu-id="6d765-136">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6d765-136">Retrieves the ID of the parent container for the control.</span></span>                                                                                     |
| <span data-ttu-id="6d765-137">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-137">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                               |
| <span data-ttu-id="6d765-138">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-138">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                               |
| <span data-ttu-id="6d765-139">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-139">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                               |
| <span data-ttu-id="6d765-140">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-140">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                               |
| <span data-ttu-id="6d765-141">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-141">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                               |
| <span data-ttu-id="6d765-142">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-142">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="6d765-143">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-143">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                      |
| <span data-ttu-id="6d765-144">public int displayLength(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6d765-144">public int displayLength(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                               |
| <span data-ttu-id="6d765-145">public AutoMode displayLengthMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6d765-145">public AutoMode displayLengthMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                               |
| <span data-ttu-id="6d765-146">public int displayLengthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-146">public int displayLengthValue(\[int value\])</span></span>                                                                |                                                                                                                                               |
| <span data-ttu-id="6d765-147">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-147">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="6d765-148">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-148">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="6d765-149">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-149">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                             |
| <span data-ttu-id="6d765-150">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-150">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="6d765-151">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-151">Determines whether to enable or disable the object.</span></span>                                                                                           |
| <span data-ttu-id="6d765-152">public EnumId enumType(\[EnumId value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-152">public EnumId enumType(\[EnumId value\])</span></span>                                                                    |                                                                                                                                               |
| <span data-ttu-id="6d765-153">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-153">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                               |
| <span data-ttu-id="6d765-154">public int fastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-154">public int fastTabSummary(\[int value\])</span></span>                                                                    |                                                                                                                                               |
| <span data-ttu-id="6d765-155">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-155">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="6d765-156">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-156">Gets or sets the name of the font for the control to use.</span></span>                                                                                     |
| <span data-ttu-id="6d765-157">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-157">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="6d765-158">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-158">Gets or sets the size of the font for the control to use.</span></span>                                                                                     |
| <span data-ttu-id="6d765-159">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-159">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="6d765-160">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-160">Gets or sets the text color for the control to use.</span></span>                                                                                           |
| <span data-ttu-id="6d765-161">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6d765-161">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="6d765-162">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-162">Gets or sets the height of the control.</span></span>                                                                                                       |
| <span data-ttu-id="6d765-163">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-163">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="6d765-164">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-164">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                |
| <span data-ttu-id="6d765-165">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-165">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="6d765-166">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-166">Gets or sets the height of the control.</span></span>                                                                                                       |
| <span data-ttu-id="6d765-167">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-167">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="6d765-168">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-168">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                      |
| <span data-ttu-id="6d765-169">public boolean hideFirstEntry(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-169">public boolean hideFirstEntry(\[boolean value\])</span></span>                                                            |                                                                                                                                               |
| <span data-ttu-id="6d765-170">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-170">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="6d765-171">public int id()</span><span class="sxs-lookup"><span data-stu-id="6d765-171">public int id()</span></span>                                                                                             | <span data-ttu-id="6d765-172">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6d765-172">Retrieves the ID of the control.</span></span>                                                                                                              |
| <span data-ttu-id="6d765-173">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="6d765-173">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="6d765-174">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6d765-174">Retrieves a value that indicates whether the control is a container control.</span></span>                                                                  |
| <span data-ttu-id="6d765-175">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-175">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                               |
| <span data-ttu-id="6d765-176">public int item(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-176">public int item(\[int value\])</span></span>                                                                              |                                                                                                                                               |
| <span data-ttu-id="6d765-177">public int items(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-177">public int items(\[int value\])</span></span>                                                                             |                                                                                                                                               |
| <span data-ttu-id="6d765-178">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-178">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="6d765-179">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-179">Gets or sets the label for a control.</span></span>                                                                                                         |
| <span data-ttu-id="6d765-180">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-180">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                               |
| <span data-ttu-id="6d765-181">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-181">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                               |
| <span data-ttu-id="6d765-182">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-182">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                               |
| <span data-ttu-id="6d765-183">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-183">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                               |
| <span data-ttu-id="6d765-184">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-184">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="6d765-185">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-185">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                               |
| <span data-ttu-id="6d765-186">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-186">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                               |
| <span data-ttu-id="6d765-187">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6d765-187">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                               |
| <span data-ttu-id="6d765-188">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-188">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="6d765-189">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-189">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                               |
| <span data-ttu-id="6d765-190">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-190">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                               |
| <span data-ttu-id="6d765-191">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-191">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="6d765-192">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-192">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                               |
| <span data-ttu-id="6d765-193">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6d765-193">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                               |
| <span data-ttu-id="6d765-194">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-194">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                               |
| <span data-ttu-id="6d765-195">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-195">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="6d765-196">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6d765-196">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                               |
| <span data-ttu-id="6d765-197">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-197">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="6d765-198">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-198">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                               |
| <span data-ttu-id="6d765-199">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-199">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="6d765-200">フォーム、レポート、テーブル、クエリ、または別のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-200">Gets or sets the name that is used in the code to identify a form, report, table, query, or another application object.</span></span> |
| <span data-ttu-id="6d765-201">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-201">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                               |
| <span data-ttu-id="6d765-202">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-202">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                               |
| <span data-ttu-id="6d765-203">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-203">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                               |
| <span data-ttu-id="6d765-204">public int selection(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-204">public int selection(\[int value\])</span></span>                                                                         |                                                                                                                                               |
| <span data-ttu-id="6d765-205">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-205">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                               |
| <span data-ttu-id="6d765-206">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-206">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="6d765-207">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6d765-207">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>               |
| <span data-ttu-id="6d765-208">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-208">public str text(\[str value\])</span></span>                                                                              |                                                                                                                                               |
| <span data-ttu-id="6d765-209">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6d765-209">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="6d765-210">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-210">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                               |
| <span data-ttu-id="6d765-211">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-211">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="6d765-212">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-212">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                               |
| <span data-ttu-id="6d765-213">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-213">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="6d765-214">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6d765-214">Sets or returns the underline property for the text in the control.</span></span>                                                                           |
| <span data-ttu-id="6d765-215">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-215">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="6d765-216">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-216">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                               |
| <span data-ttu-id="6d765-217">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-217">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="6d765-218">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6d765-218">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                               |
| <span data-ttu-id="6d765-219">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6d765-219">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                               |
| <span data-ttu-id="6d765-220">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-220">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                               |
| <span data-ttu-id="6d765-221">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-221">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                               |
| <span data-ttu-id="6d765-222">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-222">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="6d765-223">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="6d765-223">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="6d765-224">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-224">Gets or sets the width of the control.</span></span>                                                                                                        |
| <span data-ttu-id="6d765-225">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-225">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="6d765-226">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-226">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                |
| <span data-ttu-id="6d765-227">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6d765-227">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="6d765-228">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-228">Gets or sets the width of the control.</span></span>                                                                                                        |
| <span data-ttu-id="6d765-229">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="6d765-229">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                               |

## <a name="method-aligncontrol"></a><span data-ttu-id="6d765-230">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="6d765-230">Method alignControl</span></span>

<span data-ttu-id="6d765-231">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-231">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="6d765-232">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="6d765-232">Parameters - alignControl</span></span>

<span data-ttu-id="6d765-233">値</span><span class="sxs-lookup"><span data-stu-id="6d765-233">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="6d765-234">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="6d765-234">Return Value - alignControl</span></span>

<span data-ttu-id="6d765-235">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="6d765-235">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="6d765-236">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="6d765-236">Remarks - alignControl</span></span>

<span data-ttu-id="6d765-237">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="6d765-237">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="6d765-238">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="6d765-238">Method allowEdit</span></span>

<span data-ttu-id="6d765-239">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-239">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="6d765-240">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="6d765-240">Parameters - allowEdit</span></span>

<span data-ttu-id="6d765-241">値</span><span class="sxs-lookup"><span data-stu-id="6d765-241">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="6d765-242">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="6d765-242">Return Value - allowEdit</span></span>

<span data-ttu-id="6d765-243">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6d765-243">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="6d765-244">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="6d765-244">Remarks - allowEdit</span></span>

<span data-ttu-id="6d765-245">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="6d765-245">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-appendnew"></a><span data-ttu-id="6d765-246">メソッド appendNew</span><span class="sxs-lookup"><span data-stu-id="6d765-246">Method appendNew</span></span>

```xpp
public boolean appendNew([boolean value])
```

### <a name="parameters---appendnew"></a><span data-ttu-id="6d765-247">パラメーター - appendNew</span><span class="sxs-lookup"><span data-stu-id="6d765-247">Parameters - appendNew</span></span>

<span data-ttu-id="6d765-248">値</span><span class="sxs-lookup"><span data-stu-id="6d765-248">value</span></span>  

### <a name="return-value---appendnew"></a><span data-ttu-id="6d765-249">戻り値 - appendNew</span><span class="sxs-lookup"><span data-stu-id="6d765-249">Return Value - appendNew</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="6d765-250">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="6d765-250">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="6d765-251">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="6d765-251">Parameters - arrayIndex</span></span>

<span data-ttu-id="6d765-252">値</span><span class="sxs-lookup"><span data-stu-id="6d765-252">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="6d765-253">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="6d765-253">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="6d765-254">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="6d765-254">Method autoDeclaration</span></span>

<span data-ttu-id="6d765-255">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-255">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="6d765-256">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="6d765-256">Parameters - autoDeclaration</span></span>

<span data-ttu-id="6d765-257">値</span><span class="sxs-lookup"><span data-stu-id="6d765-257">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="6d765-258">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="6d765-258">Return Value - autoDeclaration</span></span>

<span data-ttu-id="6d765-259">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6d765-259">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="6d765-260">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="6d765-260">Remarks - autoDeclaration</span></span>

<span data-ttu-id="6d765-261">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="6d765-261">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="6d765-262">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="6d765-262">Method backgroundColor</span></span>

<span data-ttu-id="6d765-263">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-263">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="6d765-264">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="6d765-264">Parameters - backgroundColor</span></span>

<span data-ttu-id="6d765-265">値</span><span class="sxs-lookup"><span data-stu-id="6d765-265">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="6d765-266">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="6d765-266">Return Value - backgroundColor</span></span>

<span data-ttu-id="6d765-267">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="6d765-267">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="6d765-268">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="6d765-268">Remarks - backgroundColor</span></span>

<span data-ttu-id="6d765-269">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6d765-269">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="6d765-270">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6d765-270">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="6d765-271">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="6d765-271">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="6d765-272">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="6d765-272">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="6d765-273">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="6d765-273">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="6d765-274">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="6d765-274">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="6d765-275">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="6d765-275">Method backStyle</span></span>

<span data-ttu-id="6d765-276">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-276">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="6d765-277">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="6d765-277">Parameters - backStyle</span></span>

<span data-ttu-id="6d765-278">値</span><span class="sxs-lookup"><span data-stu-id="6d765-278">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="6d765-279">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="6d765-279">Return Value - backStyle</span></span>

<span data-ttu-id="6d765-280">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="6d765-280">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="6d765-281">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="6d765-281">Method bold</span></span>

<span data-ttu-id="6d765-282">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-282">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="6d765-283">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="6d765-283">Parameters - bold</span></span>

<span data-ttu-id="6d765-284">値</span><span class="sxs-lookup"><span data-stu-id="6d765-284">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="6d765-285">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="6d765-285">Return Value - bold</span></span>

<span data-ttu-id="6d765-286">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="6d765-286">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="6d765-287">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="6d765-287">Remarks - bold</span></span>

<span data-ttu-id="6d765-288">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6d765-288">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="6d765-289">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="6d765-289">0 Use the default font weight.</span></span>
-   <span data-ttu-id="6d765-290">1 シン。</span><span class="sxs-lookup"><span data-stu-id="6d765-290">1 Thin.</span></span>
-   <span data-ttu-id="6d765-291">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="6d765-291">2 Extra-light.</span></span>
-   <span data-ttu-id="6d765-292">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="6d765-292">3 Light.</span></span>
-   <span data-ttu-id="6d765-293">4 標準。</span><span class="sxs-lookup"><span data-stu-id="6d765-293">4 Normal.</span></span>
-   <span data-ttu-id="6d765-294">5 中。</span><span class="sxs-lookup"><span data-stu-id="6d765-294">5 Medium.</span></span>
-   <span data-ttu-id="6d765-295">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="6d765-295">6 Semibold.</span></span>
-   <span data-ttu-id="6d765-296">7 太字。</span><span class="sxs-lookup"><span data-stu-id="6d765-296">7 Bold.</span></span>
-   <span data-ttu-id="6d765-297">8 極太。</span><span class="sxs-lookup"><span data-stu-id="6d765-297">8 Extra-bold.</span></span>
-   <span data-ttu-id="6d765-298">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="6d765-298">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="6d765-299">メソッド border</span><span class="sxs-lookup"><span data-stu-id="6d765-299">Method border</span></span>

<span data-ttu-id="6d765-300">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-300">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="6d765-301">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="6d765-301">Parameters - border</span></span>

<span data-ttu-id="6d765-302">値</span><span class="sxs-lookup"><span data-stu-id="6d765-302">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="6d765-303">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="6d765-303">Return Value - border</span></span>

<span data-ttu-id="6d765-304">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="6d765-304">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="6d765-305">備考 - border</span><span class="sxs-lookup"><span data-stu-id="6d765-305">Remarks - border</span></span>

<span data-ttu-id="6d765-306">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6d765-306">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="6d765-307">値です。</span><span class="sxs-lookup"><span data-stu-id="6d765-307">Value.</span></span> | <span data-ttu-id="6d765-308">説明。</span><span class="sxs-lookup"><span data-stu-id="6d765-308">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="6d765-309">0</span><span class="sxs-lookup"><span data-stu-id="6d765-309">0</span></span>      | <span data-ttu-id="6d765-310">自動。</span><span class="sxs-lookup"><span data-stu-id="6d765-310">Auto.</span></span>        |
| <span data-ttu-id="6d765-311">1</span><span class="sxs-lookup"><span data-stu-id="6d765-311">1</span></span>      | <span data-ttu-id="6d765-312">3D。</span><span class="sxs-lookup"><span data-stu-id="6d765-312">3D.</span></span>          |
| <span data-ttu-id="6d765-313">2</span><span class="sxs-lookup"><span data-stu-id="6d765-313">2</span></span>      | <span data-ttu-id="6d765-314">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="6d765-314">Single line.</span></span> |
| <span data-ttu-id="6d765-315">3</span><span class="sxs-lookup"><span data-stu-id="6d765-315">3</span></span>      | <span data-ttu-id="6d765-316">均一。</span><span class="sxs-lookup"><span data-stu-id="6d765-316">Flat.</span></span>        |
| <span data-ttu-id="6d765-317">4</span><span class="sxs-lookup"><span data-stu-id="6d765-317">4</span></span>      | <span data-ttu-id="6d765-318">なし。</span><span class="sxs-lookup"><span data-stu-id="6d765-318">None.</span></span>        |

## <a name="method-cachedatamethod"></a><span data-ttu-id="6d765-319">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="6d765-319">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="6d765-320">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="6d765-320">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="6d765-321">値</span><span class="sxs-lookup"><span data-stu-id="6d765-321">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="6d765-322">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="6d765-322">Return Value - cacheDataMethod</span></span>

## <a name="method-characterset"></a><span data-ttu-id="6d765-323">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="6d765-323">Method characterSet</span></span>

<span data-ttu-id="6d765-324">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-324">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="6d765-325">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="6d765-325">Parameters - characterSet</span></span>

<span data-ttu-id="6d765-326">値</span><span class="sxs-lookup"><span data-stu-id="6d765-326">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="6d765-327">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="6d765-327">Return Value - characterSet</span></span>

<span data-ttu-id="6d765-328">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6d765-328">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="6d765-329">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="6d765-329">Remarks - characterSet</span></span>

<span data-ttu-id="6d765-330">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="6d765-330">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="6d765-331">値です。</span><span class="sxs-lookup"><span data-stu-id="6d765-331">Value.</span></span> | <span data-ttu-id="6d765-332">説明。</span><span class="sxs-lookup"><span data-stu-id="6d765-332">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="6d765-333">0</span><span class="sxs-lookup"><span data-stu-id="6d765-333">0</span></span>      | <span data-ttu-id="6d765-334">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6d765-334">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="6d765-335">1</span><span class="sxs-lookup"><span data-stu-id="6d765-335">1</span></span>      | <span data-ttu-id="6d765-336">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6d765-336">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="6d765-337">2</span><span class="sxs-lookup"><span data-stu-id="6d765-337">2</span></span>      | <span data-ttu-id="6d765-338">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6d765-338">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="6d765-339">77</span><span class="sxs-lookup"><span data-stu-id="6d765-339">77</span></span>     | <span data-ttu-id="6d765-340">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6d765-340">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="6d765-341">128</span><span class="sxs-lookup"><span data-stu-id="6d765-341">128</span></span>    | <span data-ttu-id="6d765-342">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6d765-342">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="6d765-343">129</span><span class="sxs-lookup"><span data-stu-id="6d765-343">129</span></span>    | <span data-ttu-id="6d765-344">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6d765-344">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="6d765-345">134</span><span class="sxs-lookup"><span data-stu-id="6d765-345">134</span></span>    | <span data-ttu-id="6d765-346">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6d765-346">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="6d765-347">136</span><span class="sxs-lookup"><span data-stu-id="6d765-347">136</span></span>    | <span data-ttu-id="6d765-348">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6d765-348">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="6d765-349">161</span><span class="sxs-lookup"><span data-stu-id="6d765-349">161</span></span>    | <span data-ttu-id="6d765-350">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6d765-350">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="6d765-351">162</span><span class="sxs-lookup"><span data-stu-id="6d765-351">162</span></span>    | <span data-ttu-id="6d765-352">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6d765-352">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="6d765-353">163</span><span class="sxs-lookup"><span data-stu-id="6d765-353">163</span></span>    | <span data-ttu-id="6d765-354">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6d765-354">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="6d765-355">186</span><span class="sxs-lookup"><span data-stu-id="6d765-355">186</span></span>    | <span data-ttu-id="6d765-356">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6d765-356">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="6d765-357">204</span><span class="sxs-lookup"><span data-stu-id="6d765-357">204</span></span>    | <span data-ttu-id="6d765-358">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6d765-358">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="6d765-359">238</span><span class="sxs-lookup"><span data-stu-id="6d765-359">238</span></span>    | <span data-ttu-id="6d765-360">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6d765-360">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="6d765-361">255</span><span class="sxs-lookup"><span data-stu-id="6d765-361">255</span></span>    | <span data-ttu-id="6d765-362">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6d765-362">OEM\_CHARSET</span></span>         |

<span data-ttu-id="6d765-363">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="6d765-363">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="6d765-364">値です。</span><span class="sxs-lookup"><span data-stu-id="6d765-364">Value.</span></span> | <span data-ttu-id="6d765-365">説明。</span><span class="sxs-lookup"><span data-stu-id="6d765-365">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="6d765-366">130</span><span class="sxs-lookup"><span data-stu-id="6d765-366">130</span></span>    | <span data-ttu-id="6d765-367">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6d765-367">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="6d765-368">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="6d765-368">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="6d765-369">値です。</span><span class="sxs-lookup"><span data-stu-id="6d765-369">Value.</span></span> | <span data-ttu-id="6d765-370">説明。</span><span class="sxs-lookup"><span data-stu-id="6d765-370">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="6d765-371">177</span><span class="sxs-lookup"><span data-stu-id="6d765-371">177</span></span>    | <span data-ttu-id="6d765-372">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6d765-372">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="6d765-373">178</span><span class="sxs-lookup"><span data-stu-id="6d765-373">178</span></span>    | <span data-ttu-id="6d765-374">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6d765-374">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="6d765-375">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="6d765-375">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="6d765-376">値です。</span><span class="sxs-lookup"><span data-stu-id="6d765-376">Value.</span></span> | <span data-ttu-id="6d765-377">説明。</span><span class="sxs-lookup"><span data-stu-id="6d765-377">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="6d765-378">222</span><span class="sxs-lookup"><span data-stu-id="6d765-378">222</span></span>    | <span data-ttu-id="6d765-379">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="6d765-379">THAI\_CHARSET</span></span> |

<span data-ttu-id="6d765-380">既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="6d765-380">The default character set is set to a value, depending on the current system locale.</span></span> <span data-ttu-id="6d765-381">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="6d765-381">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="6d765-382">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6d765-382">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="6d765-383">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="6d765-383">Method colorScheme</span></span>

<span data-ttu-id="6d765-384">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-384">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="6d765-385">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="6d765-385">Parameters - colorScheme</span></span>

<span data-ttu-id="6d765-386">値</span><span class="sxs-lookup"><span data-stu-id="6d765-386">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="6d765-387">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="6d765-387">Return Value - colorScheme</span></span>

<span data-ttu-id="6d765-388">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="6d765-388">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="6d765-389">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="6d765-389">Remarks - colorScheme</span></span>

<span data-ttu-id="6d765-390">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="6d765-390">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="6d765-391">値です。</span><span class="sxs-lookup"><span data-stu-id="6d765-391">Value.</span></span> | <span data-ttu-id="6d765-392">スタイル。</span><span class="sxs-lookup"><span data-stu-id="6d765-392">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="6d765-393">0</span><span class="sxs-lookup"><span data-stu-id="6d765-393">0</span></span>      | <span data-ttu-id="6d765-394">既定。</span><span class="sxs-lookup"><span data-stu-id="6d765-394">Default.</span></span>                      |
| <span data-ttu-id="6d765-395">1</span><span class="sxs-lookup"><span data-stu-id="6d765-395">1</span></span>      | <span data-ttu-id="6d765-396">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="6d765-396">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="6d765-397">2</span><span class="sxs-lookup"><span data-stu-id="6d765-397">2</span></span>      | <span data-ttu-id="6d765-398">真の配色。</span><span class="sxs-lookup"><span data-stu-id="6d765-398">The true-color scheme.</span></span>        |

## <a name="method-combotype"></a><span data-ttu-id="6d765-399">メソッド comboType</span><span class="sxs-lookup"><span data-stu-id="6d765-399">Method comboType</span></span>

```xpp
public int comboType([int value])
```

### <a name="parameters---combotype"></a><span data-ttu-id="6d765-400">パラメーター - comboType</span><span class="sxs-lookup"><span data-stu-id="6d765-400">Parameters - comboType</span></span>

<span data-ttu-id="6d765-401">値</span><span class="sxs-lookup"><span data-stu-id="6d765-401">value</span></span>  

### <a name="return-value---combotype"></a><span data-ttu-id="6d765-402">戻り値 - comboType</span><span class="sxs-lookup"><span data-stu-id="6d765-402">Return Value - comboType</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="6d765-403">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="6d765-403">Method configurationKey</span></span>

<span data-ttu-id="6d765-404">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-404">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="6d765-405">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="6d765-405">Parameters - configurationKey</span></span>

<span data-ttu-id="6d765-406">値</span><span class="sxs-lookup"><span data-stu-id="6d765-406">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="6d765-407">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="6d765-407">Return Value - configurationKey</span></span>

<span data-ttu-id="6d765-408">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="6d765-408">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="6d765-409">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="6d765-409">Remarks - configurationKey</span></span>

<span data-ttu-id="6d765-410">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6d765-410">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="6d765-411">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="6d765-411">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="6d765-412">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="6d765-412">Method containerId</span></span>

<span data-ttu-id="6d765-413">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6d765-413">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="6d765-414">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="6d765-414">Return Value - containerId</span></span>

<span data-ttu-id="6d765-415">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="6d765-415">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="6d765-416">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="6d765-416">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="6d765-417">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="6d765-417">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="6d765-418">値</span><span class="sxs-lookup"><span data-stu-id="6d765-418">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="6d765-419">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="6d765-419">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="6d765-420">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="6d765-420">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="6d765-421">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="6d765-421">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="6d765-422">値</span><span class="sxs-lookup"><span data-stu-id="6d765-422">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="6d765-423">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="6d765-423">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="6d765-424">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="6d765-424">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="6d765-425">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="6d765-425">Parameters - dataField</span></span>

<span data-ttu-id="6d765-426">値</span><span class="sxs-lookup"><span data-stu-id="6d765-426">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="6d765-427">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="6d765-427">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="6d765-428">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="6d765-428">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="6d765-429">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="6d765-429">Parameters - dataMethod</span></span>

<span data-ttu-id="6d765-430">値</span><span class="sxs-lookup"><span data-stu-id="6d765-430">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="6d765-431">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="6d765-431">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="6d765-432">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="6d765-432">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="6d765-433">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="6d765-433">Parameters - dataRelationPath</span></span>

<span data-ttu-id="6d765-434">値</span><span class="sxs-lookup"><span data-stu-id="6d765-434">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="6d765-435">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="6d765-435">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="6d765-436">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="6d765-436">Method dataSource</span></span>

<span data-ttu-id="6d765-437">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-437">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="6d765-438">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="6d765-438">Parameters - dataSource</span></span>

<span data-ttu-id="6d765-439">値</span><span class="sxs-lookup"><span data-stu-id="6d765-439">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="6d765-440">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="6d765-440">Return Value - dataSource</span></span>

<span data-ttu-id="6d765-441">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="6d765-441">The identifier of the data source that will be used.</span></span>

## <a name="method-displaylength"></a><span data-ttu-id="6d765-442">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="6d765-442">Method displayLength</span></span>

```xpp
public int displayLength([int value], [AutoMode mode])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="6d765-443">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="6d765-443">Parameters - displayLength</span></span>

<span data-ttu-id="6d765-444">値</span><span class="sxs-lookup"><span data-stu-id="6d765-444">value</span></span>  

<!-- -->

<span data-ttu-id="6d765-445">モード</span><span class="sxs-lookup"><span data-stu-id="6d765-445">mode</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="6d765-446">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="6d765-446">Return Value - displayLength</span></span>

## <a name="method-displaylengthmode"></a><span data-ttu-id="6d765-447">メソッド displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="6d765-447">Method displayLengthMode</span></span>

```xpp
public AutoMode displayLengthMode([AutoMode mode])
```

### <a name="parameters---displaylengthmode"></a><span data-ttu-id="6d765-448">パラメーター - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="6d765-448">Parameters - displayLengthMode</span></span>

<span data-ttu-id="6d765-449">モード</span><span class="sxs-lookup"><span data-stu-id="6d765-449">mode</span></span>  

### <a name="return-value---displaylengthmode"></a><span data-ttu-id="6d765-450">戻り値 - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="6d765-450">Return Value - displayLengthMode</span></span>

## <a name="method-displaylengthvalue"></a><span data-ttu-id="6d765-451">メソッド displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="6d765-451">Method displayLengthValue</span></span>

```xpp
public int displayLengthValue([int value])
```

### <a name="parameters---displaylengthvalue"></a><span data-ttu-id="6d765-452">パラメーター - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="6d765-452">Parameters - displayLengthValue</span></span>

<span data-ttu-id="6d765-453">値</span><span class="sxs-lookup"><span data-stu-id="6d765-453">value</span></span>  

### <a name="return-value---displaylengthvalue"></a><span data-ttu-id="6d765-454">戻り値 - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="6d765-454">Return Value - displayLengthValue</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="6d765-455">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="6d765-455">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="6d765-456">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="6d765-456">Parameters - displayTarget</span></span>

<span data-ttu-id="6d765-457">値</span><span class="sxs-lookup"><span data-stu-id="6d765-457">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="6d765-458">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="6d765-458">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="6d765-459">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="6d765-459">Method dragDrop</span></span>

<span data-ttu-id="6d765-460">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-460">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="6d765-461">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="6d765-461">Parameters - dragDrop</span></span>

<span data-ttu-id="6d765-462">値</span><span class="sxs-lookup"><span data-stu-id="6d765-462">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="6d765-463">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="6d765-463">Return Value - dragDrop</span></span>

<span data-ttu-id="6d765-464">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="6d765-464">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="6d765-465">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="6d765-465">Method enabled</span></span>

<span data-ttu-id="6d765-466">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-466">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="6d765-467">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="6d765-467">Parameters - enabled</span></span>

<span data-ttu-id="6d765-468">値</span><span class="sxs-lookup"><span data-stu-id="6d765-468">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="6d765-469">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="6d765-469">Return Value - enabled</span></span>

<span data-ttu-id="6d765-470">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6d765-470">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="6d765-471">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="6d765-471">Remarks - enabled</span></span>

<span data-ttu-id="6d765-472">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="6d765-472">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="6d765-473">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="6d765-473">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="6d765-474">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="6d765-474">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-enumtype"></a><span data-ttu-id="6d765-475">メソッド enumType</span><span class="sxs-lookup"><span data-stu-id="6d765-475">Method enumType</span></span>

```xpp
public EnumId enumType([EnumId value])
```

### <a name="parameters---enumtype"></a><span data-ttu-id="6d765-476">パラメーター - enumType</span><span class="sxs-lookup"><span data-stu-id="6d765-476">Parameters - enumType</span></span>

<span data-ttu-id="6d765-477">値</span><span class="sxs-lookup"><span data-stu-id="6d765-477">value</span></span>  

### <a name="return-value---enumtype"></a><span data-ttu-id="6d765-478">戻り値 - enumType</span><span class="sxs-lookup"><span data-stu-id="6d765-478">Return Value - enumType</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="6d765-479">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="6d765-479">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="6d765-480">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="6d765-480">Parameters - extendedDataType</span></span>

<span data-ttu-id="6d765-481">値</span><span class="sxs-lookup"><span data-stu-id="6d765-481">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="6d765-482">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="6d765-482">Return Value - extendedDataType</span></span>

## <a name="method-fasttabsummary"></a><span data-ttu-id="6d765-483">メソッド fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="6d765-483">Method fastTabSummary</span></span>

```xpp
public int fastTabSummary([int value])
```

### <a name="parameters---fasttabsummary"></a><span data-ttu-id="6d765-484">パラメーター - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="6d765-484">Parameters - fastTabSummary</span></span>

<span data-ttu-id="6d765-485">値</span><span class="sxs-lookup"><span data-stu-id="6d765-485">value</span></span>  

### <a name="return-value---fasttabsummary"></a><span data-ttu-id="6d765-486">戻り値 - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="6d765-486">Return Value - fastTabSummary</span></span>

## <a name="method-font"></a><span data-ttu-id="6d765-487">メソッド font</span><span class="sxs-lookup"><span data-stu-id="6d765-487">Method font</span></span>

<span data-ttu-id="6d765-488">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-488">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="6d765-489">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="6d765-489">Parameters - font</span></span>

<span data-ttu-id="6d765-490">値</span><span class="sxs-lookup"><span data-stu-id="6d765-490">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="6d765-491">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="6d765-491">Return Value - font</span></span>

<span data-ttu-id="6d765-492">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="6d765-492">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="6d765-493">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="6d765-493">Method fontSize</span></span>

<span data-ttu-id="6d765-494">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-494">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="6d765-495">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="6d765-495">Parameters - fontSize</span></span>

<span data-ttu-id="6d765-496">値</span><span class="sxs-lookup"><span data-stu-id="6d765-496">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="6d765-497">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="6d765-497">Return Value - fontSize</span></span>

<span data-ttu-id="6d765-498">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="6d765-498">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="6d765-499">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="6d765-499">Method foregroundColor</span></span>

<span data-ttu-id="6d765-500">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-500">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="6d765-501">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="6d765-501">Parameters - foregroundColor</span></span>

<span data-ttu-id="6d765-502">値</span><span class="sxs-lookup"><span data-stu-id="6d765-502">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="6d765-503">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="6d765-503">Return Value - foregroundColor</span></span>

<span data-ttu-id="6d765-504">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="6d765-504">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="6d765-505">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="6d765-505">Remarks - foregroundColor</span></span>

<span data-ttu-id="6d765-506">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6d765-506">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="6d765-507">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6d765-507">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="6d765-508">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="6d765-508">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="6d765-509">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="6d765-509">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="6d765-510">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="6d765-510">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="6d765-511">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="6d765-511">The maximum value for a single byte is 255.</span></span>

## <a name="method-height"></a><span data-ttu-id="6d765-512">メソッド height</span><span class="sxs-lookup"><span data-stu-id="6d765-512">Method height</span></span>

<span data-ttu-id="6d765-513">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-513">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="6d765-514">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="6d765-514">Parameters - height</span></span>

<span data-ttu-id="6d765-515">値</span><span class="sxs-lookup"><span data-stu-id="6d765-515">value</span></span>  

<!-- -->

<span data-ttu-id="6d765-516">モード</span><span class="sxs-lookup"><span data-stu-id="6d765-516">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="6d765-517">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="6d765-517">Return Value - height</span></span>

<span data-ttu-id="6d765-518">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="6d765-518">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="6d765-519">備考 - height</span><span class="sxs-lookup"><span data-stu-id="6d765-519">Remarks - height</span></span>

<span data-ttu-id="6d765-520">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6d765-520">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="6d765-521">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="6d765-521">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="6d765-522">モード。</span><span class="sxs-lookup"><span data-stu-id="6d765-522">Mode.</span></span>            | <span data-ttu-id="6d765-523">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="6d765-523">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d765-524">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="6d765-524">-1 Exact.</span></span>        | <span data-ttu-id="6d765-525">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6d765-525">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="6d765-526">0 自動。</span><span class="sxs-lookup"><span data-stu-id="6d765-526">0 Auto.</span></span>          | <span data-ttu-id="6d765-527">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="6d765-527">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="6d765-528">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="6d765-528">1 Column height.</span></span> | <span data-ttu-id="6d765-529">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="6d765-529">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="6d765-530">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="6d765-530">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="6d765-531">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="6d765-531">Method heightMode</span></span>

<span data-ttu-id="6d765-532">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-532">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="6d765-533">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="6d765-533">Parameters - heightMode</span></span>

<span data-ttu-id="6d765-534">値</span><span class="sxs-lookup"><span data-stu-id="6d765-534">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="6d765-535">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="6d765-535">Return Value - heightMode</span></span>

<span data-ttu-id="6d765-536">計算モード。</span><span class="sxs-lookup"><span data-stu-id="6d765-536">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="6d765-537">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="6d765-537">Remarks - heightMode</span></span>

<span data-ttu-id="6d765-538">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="6d765-538">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="6d765-539">モード。</span><span class="sxs-lookup"><span data-stu-id="6d765-539">Mode.</span></span>          | <span data-ttu-id="6d765-540">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="6d765-540">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d765-541">正確。</span><span class="sxs-lookup"><span data-stu-id="6d765-541">Exact.</span></span>         | <span data-ttu-id="6d765-542">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6d765-542">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="6d765-543">自動。</span><span class="sxs-lookup"><span data-stu-id="6d765-543">Auto.</span></span>          | <span data-ttu-id="6d765-544">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="6d765-544">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="6d765-545">列の高さ</span><span class="sxs-lookup"><span data-stu-id="6d765-545">Column height.</span></span> | <span data-ttu-id="6d765-546">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="6d765-546">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="6d765-547">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="6d765-547">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="6d765-548">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="6d765-548">Method heightValue</span></span>

<span data-ttu-id="6d765-549">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-549">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="6d765-550">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="6d765-550">Parameters - heightValue</span></span>

<span data-ttu-id="6d765-551">値</span><span class="sxs-lookup"><span data-stu-id="6d765-551">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="6d765-552">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="6d765-552">Return Value - heightValue</span></span>

<span data-ttu-id="6d765-553">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="6d765-553">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="6d765-554">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="6d765-554">Remarks - heightValue</span></span>

<span data-ttu-id="6d765-555">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="6d765-555">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="6d765-556">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="6d765-556">Method helpText</span></span>

<span data-ttu-id="6d765-557">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-557">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="6d765-558">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="6d765-558">Parameters - helpText</span></span>

<span data-ttu-id="6d765-559">値</span><span class="sxs-lookup"><span data-stu-id="6d765-559">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="6d765-560">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="6d765-560">Return Value - helpText</span></span>

<span data-ttu-id="6d765-561">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="6d765-561">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="6d765-562">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="6d765-562">Remarks - helpText</span></span>

<span data-ttu-id="6d765-563">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-563">Set the HelpText property for an object by using the property dialogue box.</span></span> <span data-ttu-id="6d765-564">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="6d765-564">The help text must not exceed 250 characters.</span></span>

## <a name="method-hidefirstentry"></a><span data-ttu-id="6d765-565">メソッド hideFirstEntry</span><span class="sxs-lookup"><span data-stu-id="6d765-565">Method hideFirstEntry</span></span>

```xpp
public boolean hideFirstEntry([boolean value])
```

### <a name="parameters---hidefirstentry"></a><span data-ttu-id="6d765-566">パラメーター - hideFirstEntry</span><span class="sxs-lookup"><span data-stu-id="6d765-566">Parameters - hideFirstEntry</span></span>

<span data-ttu-id="6d765-567">値</span><span class="sxs-lookup"><span data-stu-id="6d765-567">value</span></span>  

### <a name="return-value---hidefirstentry"></a><span data-ttu-id="6d765-568">戻り値 - hideFirstEntry</span><span class="sxs-lookup"><span data-stu-id="6d765-568">Return Value - hideFirstEntry</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="6d765-569">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="6d765-569">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="6d765-570">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="6d765-570">Parameters - hierarchyParent</span></span>

<span data-ttu-id="6d765-571">値</span><span class="sxs-lookup"><span data-stu-id="6d765-571">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="6d765-572">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="6d765-572">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="6d765-573">メソッド id</span><span class="sxs-lookup"><span data-stu-id="6d765-573">Method id</span></span>

<span data-ttu-id="6d765-574">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6d765-574">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="6d765-575">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="6d765-575">Return Value - id</span></span>

<span data-ttu-id="6d765-576">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="6d765-576">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="6d765-577">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="6d765-577">Method isContainer</span></span>

<span data-ttu-id="6d765-578">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="6d765-578">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="6d765-579">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="6d765-579">Return Value - isContainer</span></span>

<span data-ttu-id="6d765-580">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="6d765-580">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-italic"></a><span data-ttu-id="6d765-581">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="6d765-581">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="6d765-582">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="6d765-582">Parameters - italic</span></span>

<span data-ttu-id="6d765-583">値</span><span class="sxs-lookup"><span data-stu-id="6d765-583">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="6d765-584">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="6d765-584">Return Value - italic</span></span>

## <a name="method-item"></a><span data-ttu-id="6d765-585">メソッド item</span><span class="sxs-lookup"><span data-stu-id="6d765-585">Method item</span></span>

```xpp
public int item([int value])
```

### <a name="parameters---item"></a><span data-ttu-id="6d765-586">パラメーター - item</span><span class="sxs-lookup"><span data-stu-id="6d765-586">Parameters - item</span></span>

<span data-ttu-id="6d765-587">値</span><span class="sxs-lookup"><span data-stu-id="6d765-587">value</span></span>  

### <a name="return-value---item"></a><span data-ttu-id="6d765-588">戻り値 - item</span><span class="sxs-lookup"><span data-stu-id="6d765-588">Return Value - item</span></span>

## <a name="method-items"></a><span data-ttu-id="6d765-589">メソッド items</span><span class="sxs-lookup"><span data-stu-id="6d765-589">Method items</span></span>

```xpp
public int items([int value])
```

### <a name="parameters---items"></a><span data-ttu-id="6d765-590">パラメーター - items</span><span class="sxs-lookup"><span data-stu-id="6d765-590">Parameters - items</span></span>

<span data-ttu-id="6d765-591">値</span><span class="sxs-lookup"><span data-stu-id="6d765-591">value</span></span>  

### <a name="return-value---items"></a><span data-ttu-id="6d765-592">戻り値 - items</span><span class="sxs-lookup"><span data-stu-id="6d765-592">Return Value - items</span></span>

## <a name="method-label"></a><span data-ttu-id="6d765-593">メソッド label</span><span class="sxs-lookup"><span data-stu-id="6d765-593">Method label</span></span>

<span data-ttu-id="6d765-594">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-594">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="6d765-595">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="6d765-595">Parameters - label</span></span>

<span data-ttu-id="6d765-596">値</span><span class="sxs-lookup"><span data-stu-id="6d765-596">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="6d765-597">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="6d765-597">Return Value - label</span></span>

<span data-ttu-id="6d765-598">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="6d765-598">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="6d765-599">備考 - label</span><span class="sxs-lookup"><span data-stu-id="6d765-599">Remarks - label</span></span>

<span data-ttu-id="6d765-600">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-600">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="6d765-601">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="6d765-601">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="6d765-602">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="6d765-602">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="6d765-603">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="6d765-603">Parameters - labelAlignment</span></span>

<span data-ttu-id="6d765-604">値</span><span class="sxs-lookup"><span data-stu-id="6d765-604">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="6d765-605">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="6d765-605">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="6d765-606">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="6d765-606">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="6d765-607">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="6d765-607">Parameters - labelBold</span></span>

<span data-ttu-id="6d765-608">値</span><span class="sxs-lookup"><span data-stu-id="6d765-608">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="6d765-609">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="6d765-609">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="6d765-610">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="6d765-610">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="6d765-611">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="6d765-611">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="6d765-612">値</span><span class="sxs-lookup"><span data-stu-id="6d765-612">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="6d765-613">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="6d765-613">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="6d765-614">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="6d765-614">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="6d765-615">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="6d765-615">Parameters - labelFont</span></span>

<span data-ttu-id="6d765-616">値</span><span class="sxs-lookup"><span data-stu-id="6d765-616">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="6d765-617">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="6d765-617">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="6d765-618">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="6d765-618">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="6d765-619">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="6d765-619">Parameters - labelFontSize</span></span>

<span data-ttu-id="6d765-620">値</span><span class="sxs-lookup"><span data-stu-id="6d765-620">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="6d765-621">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="6d765-621">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="6d765-622">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="6d765-622">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="6d765-623">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="6d765-623">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="6d765-624">値</span><span class="sxs-lookup"><span data-stu-id="6d765-624">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="6d765-625">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="6d765-625">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="6d765-626">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="6d765-626">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="6d765-627">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="6d765-627">Parameters - labelGuide</span></span>

<span data-ttu-id="6d765-628">値</span><span class="sxs-lookup"><span data-stu-id="6d765-628">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="6d765-629">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="6d765-629">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="6d765-630">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="6d765-630">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="6d765-631">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="6d765-631">Parameters - labelHeight</span></span>

<span data-ttu-id="6d765-632">値</span><span class="sxs-lookup"><span data-stu-id="6d765-632">value</span></span>  

<!-- -->

<span data-ttu-id="6d765-633">モード</span><span class="sxs-lookup"><span data-stu-id="6d765-633">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="6d765-634">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="6d765-634">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="6d765-635">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="6d765-635">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="6d765-636">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="6d765-636">Parameters - labelHeightMode</span></span>

<span data-ttu-id="6d765-637">値</span><span class="sxs-lookup"><span data-stu-id="6d765-637">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="6d765-638">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="6d765-638">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="6d765-639">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="6d765-639">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="6d765-640">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="6d765-640">Parameters - labelHeightValue</span></span>

<span data-ttu-id="6d765-641">値</span><span class="sxs-lookup"><span data-stu-id="6d765-641">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="6d765-642">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="6d765-642">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="6d765-643">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="6d765-643">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="6d765-644">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="6d765-644">Parameters - labelItalic</span></span>

<span data-ttu-id="6d765-645">値</span><span class="sxs-lookup"><span data-stu-id="6d765-645">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="6d765-646">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="6d765-646">Return Value - labelItalic</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="6d765-647">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="6d765-647">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="6d765-648">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="6d765-648">Parameters - labelPosition</span></span>

<span data-ttu-id="6d765-649">値</span><span class="sxs-lookup"><span data-stu-id="6d765-649">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="6d765-650">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="6d765-650">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="6d765-651">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="6d765-651">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="6d765-652">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="6d765-652">Parameters - labelUnderline</span></span>

<span data-ttu-id="6d765-653">値</span><span class="sxs-lookup"><span data-stu-id="6d765-653">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="6d765-654">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="6d765-654">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="6d765-655">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="6d765-655">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="6d765-656">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="6d765-656">Parameters - labelWidth</span></span>

<span data-ttu-id="6d765-657">値</span><span class="sxs-lookup"><span data-stu-id="6d765-657">value</span></span>  

<!-- -->

<span data-ttu-id="6d765-658">モード</span><span class="sxs-lookup"><span data-stu-id="6d765-658">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="6d765-659">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="6d765-659">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="6d765-660">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="6d765-660">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="6d765-661">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="6d765-661">Parameters - labelWidthMode</span></span>

<span data-ttu-id="6d765-662">値</span><span class="sxs-lookup"><span data-stu-id="6d765-662">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="6d765-663">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="6d765-663">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="6d765-664">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="6d765-664">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="6d765-665">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="6d765-665">Parameters - labelWidthValue</span></span>

<span data-ttu-id="6d765-666">値</span><span class="sxs-lookup"><span data-stu-id="6d765-666">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="6d765-667">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="6d765-667">Return Value - labelWidthValue</span></span>

## <a name="method-left"></a><span data-ttu-id="6d765-668">メソッド left</span><span class="sxs-lookup"><span data-stu-id="6d765-668">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="6d765-669">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="6d765-669">Parameters - left</span></span>

<span data-ttu-id="6d765-670">値</span><span class="sxs-lookup"><span data-stu-id="6d765-670">value</span></span>  

<!-- -->

<span data-ttu-id="6d765-671">モード</span><span class="sxs-lookup"><span data-stu-id="6d765-671">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="6d765-672">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="6d765-672">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="6d765-673">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="6d765-673">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="6d765-674">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="6d765-674">Parameters - leftMode</span></span>

<span data-ttu-id="6d765-675">値</span><span class="sxs-lookup"><span data-stu-id="6d765-675">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="6d765-676">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="6d765-676">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="6d765-677">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="6d765-677">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="6d765-678">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="6d765-678">Parameters - leftValue</span></span>

<span data-ttu-id="6d765-679">値</span><span class="sxs-lookup"><span data-stu-id="6d765-679">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="6d765-680">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="6d765-680">Return Value - leftValue</span></span>

## <a name="method-name"></a><span data-ttu-id="6d765-681">メソッド名</span><span class="sxs-lookup"><span data-stu-id="6d765-681">Method name</span></span>

<span data-ttu-id="6d765-682">フォーム、レポート、テーブル、クエリ、または別のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-682">Gets or sets the name that is used in the code to identify a form, report, table, query, or another application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="6d765-683">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="6d765-683">Parameters - name</span></span>

<span data-ttu-id="6d765-684">値</span><span class="sxs-lookup"><span data-stu-id="6d765-684">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="6d765-685">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="6d765-685">Return Value - name</span></span>

<span data-ttu-id="6d765-686">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="6d765-686">The name that is used in the code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="6d765-687">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="6d765-687">Remarks - name</span></span>

<span data-ttu-id="6d765-688">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d765-688">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="6d765-689">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="6d765-689">Begins with a letter.</span></span>
-   <span data-ttu-id="6d765-690">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="6d765-690">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="6d765-691">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="6d765-691">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="6d765-692">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="6d765-692">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="6d765-693">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="6d765-693">Tables cannot have the same name as other public objects, such as extended data types, base enumeration types, classes, and so on.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="6d765-694">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="6d765-694">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="6d765-695">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="6d765-695">Parameters - neededPermission</span></span>

<span data-ttu-id="6d765-696">値</span><span class="sxs-lookup"><span data-stu-id="6d765-696">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="6d765-697">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="6d765-697">Return Value - neededPermission</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="6d765-698">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="6d765-698">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="6d765-699">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="6d765-699">Parameters - promptrect</span></span>

<span data-ttu-id="6d765-700">値</span><span class="sxs-lookup"><span data-stu-id="6d765-700">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="6d765-701">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="6d765-701">Return Value - promptrect</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="6d765-702">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="6d765-702">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="6d765-703">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="6d765-703">Parameters - securityKey</span></span>

<span data-ttu-id="6d765-704">値</span><span class="sxs-lookup"><span data-stu-id="6d765-704">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="6d765-705">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="6d765-705">Return Value - securityKey</span></span>

## <a name="method-selection"></a><span data-ttu-id="6d765-706">メソッド selection</span><span class="sxs-lookup"><span data-stu-id="6d765-706">Method selection</span></span>

```xpp
public int selection([int value])
```

### <a name="parameters---selection"></a><span data-ttu-id="6d765-707">パラメーター - selection</span><span class="sxs-lookup"><span data-stu-id="6d765-707">Parameters - selection</span></span>

<span data-ttu-id="6d765-708">値</span><span class="sxs-lookup"><span data-stu-id="6d765-708">value</span></span>  

### <a name="return-value---selection"></a><span data-ttu-id="6d765-709">戻り値 - selection</span><span class="sxs-lookup"><span data-stu-id="6d765-709">Return Value - selection</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="6d765-710">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="6d765-710">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="6d765-711">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="6d765-711">Parameters - showLabel</span></span>

<span data-ttu-id="6d765-712">値</span><span class="sxs-lookup"><span data-stu-id="6d765-712">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="6d765-713">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="6d765-713">Return Value - showLabel</span></span>

## <a name="method-skip"></a><span data-ttu-id="6d765-714">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="6d765-714">Method skip</span></span>

<span data-ttu-id="6d765-715">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6d765-715">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="6d765-716">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="6d765-716">Parameters - skip</span></span>

<span data-ttu-id="6d765-717">値</span><span class="sxs-lookup"><span data-stu-id="6d765-717">value</span></span>  
<span data-ttu-id="6d765-718">コントロールの skip プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="6d765-718">The value to assign to the skip property of the control.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="6d765-719">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="6d765-719">Return Value - skip</span></span>

<span data-ttu-id="6d765-720">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6d765-720">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-text"></a><span data-ttu-id="6d765-721">メソッド text</span><span class="sxs-lookup"><span data-stu-id="6d765-721">Method text</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="6d765-722">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="6d765-722">Parameters - text</span></span>

<span data-ttu-id="6d765-723">値</span><span class="sxs-lookup"><span data-stu-id="6d765-723">value</span></span>  

### <a name="return-value---text"></a><span data-ttu-id="6d765-724">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="6d765-724">Return Value - text</span></span>

## <a name="method-top"></a><span data-ttu-id="6d765-725">メソッド top</span><span class="sxs-lookup"><span data-stu-id="6d765-725">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="6d765-726">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="6d765-726">Parameters - top</span></span>

<span data-ttu-id="6d765-727">値</span><span class="sxs-lookup"><span data-stu-id="6d765-727">value</span></span>  

<!-- -->

<span data-ttu-id="6d765-728">モード</span><span class="sxs-lookup"><span data-stu-id="6d765-728">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="6d765-729">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="6d765-729">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="6d765-730">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="6d765-730">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="6d765-731">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="6d765-731">Parameters - topMode</span></span>

<span data-ttu-id="6d765-732">値</span><span class="sxs-lookup"><span data-stu-id="6d765-732">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="6d765-733">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="6d765-733">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="6d765-734">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="6d765-734">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="6d765-735">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="6d765-735">Parameters - topValue</span></span>

<span data-ttu-id="6d765-736">値</span><span class="sxs-lookup"><span data-stu-id="6d765-736">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="6d765-737">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="6d765-737">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="6d765-738">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="6d765-738">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="6d765-739">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="6d765-739">Parameters - type</span></span>

<span data-ttu-id="6d765-740">値</span><span class="sxs-lookup"><span data-stu-id="6d765-740">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="6d765-741">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="6d765-741">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="6d765-742">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="6d765-742">Method underline</span></span>

<span data-ttu-id="6d765-743">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="6d765-743">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="6d765-744">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="6d765-744">Parameters - underline</span></span>

<span data-ttu-id="6d765-745">値</span><span class="sxs-lookup"><span data-stu-id="6d765-745">value</span></span>  
<span data-ttu-id="6d765-746">コントロールの underline プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="6d765-746">The value to assign to the underline property of the control.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="6d765-747">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="6d765-747">Return Value - underline</span></span>

<span data-ttu-id="6d765-748">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="6d765-748">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-userdata"></a><span data-ttu-id="6d765-749">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="6d765-749">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="6d765-750">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="6d765-750">Parameters - userData</span></span>

<span data-ttu-id="6d765-751">値</span><span class="sxs-lookup"><span data-stu-id="6d765-751">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="6d765-752">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="6d765-752">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="6d765-753">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="6d765-753">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="6d765-754">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="6d765-754">Parameters - userDataItem</span></span>

<span data-ttu-id="6d765-755">値</span><span class="sxs-lookup"><span data-stu-id="6d765-755">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="6d765-756">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="6d765-756">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="6d765-757">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="6d765-757">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="6d765-758">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="6d765-758">Parameters - userDataItems</span></span>

<span data-ttu-id="6d765-759">値</span><span class="sxs-lookup"><span data-stu-id="6d765-759">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="6d765-760">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="6d765-760">Return Value - userDataItems</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="6d765-761">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="6d765-761">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="6d765-762">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="6d765-762">Parameters - verticalSpacing</span></span>

<span data-ttu-id="6d765-763">値</span><span class="sxs-lookup"><span data-stu-id="6d765-763">value</span></span>  

<!-- -->

<span data-ttu-id="6d765-764">モード</span><span class="sxs-lookup"><span data-stu-id="6d765-764">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="6d765-765">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="6d765-765">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="6d765-766">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="6d765-766">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="6d765-767">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="6d765-767">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="6d765-768">モード</span><span class="sxs-lookup"><span data-stu-id="6d765-768">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="6d765-769">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="6d765-769">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="6d765-770">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="6d765-770">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="6d765-771">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="6d765-771">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="6d765-772">値</span><span class="sxs-lookup"><span data-stu-id="6d765-772">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="6d765-773">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="6d765-773">Return Value - verticalSpacingValue</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="6d765-774">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="6d765-774">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="6d765-775">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="6d765-775">Parameters - viewEditMode</span></span>

<span data-ttu-id="6d765-776">値</span><span class="sxs-lookup"><span data-stu-id="6d765-776">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="6d765-777">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="6d765-777">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="6d765-778">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="6d765-778">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="6d765-779">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="6d765-779">Parameters - visible</span></span>

<span data-ttu-id="6d765-780">値</span><span class="sxs-lookup"><span data-stu-id="6d765-780">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="6d765-781">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="6d765-781">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="6d765-782">メソッド width</span><span class="sxs-lookup"><span data-stu-id="6d765-782">Method width</span></span>

<span data-ttu-id="6d765-783">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-783">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="6d765-784">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="6d765-784">Parameters - width</span></span>

<span data-ttu-id="6d765-785">値</span><span class="sxs-lookup"><span data-stu-id="6d765-785">value</span></span>  

<!-- -->

<span data-ttu-id="6d765-786">モード</span><span class="sxs-lookup"><span data-stu-id="6d765-786">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="6d765-787">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="6d765-787">Return Value - width</span></span>

<span data-ttu-id="6d765-788">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="6d765-788">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="6d765-789">備考 - width</span><span class="sxs-lookup"><span data-stu-id="6d765-789">Remarks - width</span></span>

<span data-ttu-id="6d765-790">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="6d765-790">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="6d765-791">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="6d765-791">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="6d765-792">モード。</span><span class="sxs-lookup"><span data-stu-id="6d765-792">Mode.</span></span>           | <span data-ttu-id="6d765-793">幅計算。</span><span class="sxs-lookup"><span data-stu-id="6d765-793">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d765-794">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="6d765-794">-1 Exact.</span></span>       | <span data-ttu-id="6d765-795">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6d765-795">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="6d765-796">0 自動。</span><span class="sxs-lookup"><span data-stu-id="6d765-796">0 Auto.</span></span>         | <span data-ttu-id="6d765-797">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="6d765-797">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="6d765-798">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="6d765-798">1 Column width.</span></span> | <span data-ttu-id="6d765-799">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="6d765-799">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="6d765-800">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="6d765-800">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="6d765-801">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="6d765-801">Method widthMode</span></span>

<span data-ttu-id="6d765-802">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-802">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="6d765-803">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="6d765-803">Parameters - widthMode</span></span>

<span data-ttu-id="6d765-804">値</span><span class="sxs-lookup"><span data-stu-id="6d765-804">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="6d765-805">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="6d765-805">Return Value - widthMode</span></span>

<span data-ttu-id="6d765-806">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="6d765-806">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="6d765-807">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="6d765-807">Remarks - widthMode</span></span>

<span data-ttu-id="6d765-808">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="6d765-808">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="6d765-809">モード。</span><span class="sxs-lookup"><span data-stu-id="6d765-809">Mode.</span></span>         | <span data-ttu-id="6d765-810">幅計算。</span><span class="sxs-lookup"><span data-stu-id="6d765-810">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d765-811">正確。</span><span class="sxs-lookup"><span data-stu-id="6d765-811">Exact.</span></span>        | <span data-ttu-id="6d765-812">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="6d765-812">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="6d765-813">自動。</span><span class="sxs-lookup"><span data-stu-id="6d765-813">Auto.</span></span>         | <span data-ttu-id="6d765-814">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="6d765-814">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="6d765-815">列の幅。</span><span class="sxs-lookup"><span data-stu-id="6d765-815">Column width.</span></span> | <span data-ttu-id="6d765-816">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="6d765-816">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="6d765-817">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="6d765-817">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="6d765-818">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="6d765-818">Method widthValue</span></span>

<span data-ttu-id="6d765-819">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6d765-819">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="6d765-820">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="6d765-820">Parameters - widthValue</span></span>

<span data-ttu-id="6d765-821">値</span><span class="sxs-lookup"><span data-stu-id="6d765-821">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="6d765-822">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="6d765-822">Return Value - widthValue</span></span>

<span data-ttu-id="6d765-823">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="6d765-823">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="6d765-824">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="6d765-824">Remarks - widthValue</span></span>

<span data-ttu-id="6d765-825">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="6d765-825">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="6d765-826">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="6d765-826">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="6d765-827">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="6d765-827">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="6d765-828">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="6d765-828">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="6d765-829">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="6d765-829">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="6d765-830">overrideObject</span><span class="sxs-lookup"><span data-stu-id="6d765-830">overrideObject</span></span>  

