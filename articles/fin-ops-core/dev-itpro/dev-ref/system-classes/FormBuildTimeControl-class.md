---
title: FormBuildTimeControl クラス
description: このトピックでは、FormBuildTimeControl クラスについて説明します。
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
ms.openlocfilehash: 0de9f238131bc1f63a94831fdbac9f221e44a279
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502637"
---
# <a name="class-formbuildtimecontrol"></a><span data-ttu-id="61c86-103">クラス FormBuildTimeControl</span><span class="sxs-lookup"><span data-stu-id="61c86-103">Class FormBuildTimeControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildTimeControl extends FormBuildControl
```

<span data-ttu-id="61c86-104">FormBuildTimeControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="61c86-104">The FormBuildTimeControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="61c86-105">備考</span><span class="sxs-lookup"><span data-stu-id="61c86-105">Remarks</span></span>

<span data-ttu-id="61c86-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="61c86-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="61c86-107">例</span><span class="sxs-lookup"><span data-stu-id="61c86-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="61c86-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="61c86-108">Methods</span></span>

| <span data-ttu-id="61c86-109">方法</span><span class="sxs-lookup"><span data-stu-id="61c86-109">Method</span></span>                                                                                                      | <span data-ttu-id="61c86-110">説明</span><span class="sxs-lookup"><span data-stu-id="61c86-110">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61c86-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="61c86-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-112">Determines whether to align the control.</span></span>                                                                                                |
| <span data-ttu-id="61c86-113">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-113">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="61c86-114">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-114">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="61c86-115">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-115">Determines whether the user can change the contents of the control.</span></span>                                                                     |
| <span data-ttu-id="61c86-116">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-116">public int arrayIndex(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="61c86-117">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-117">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="61c86-118">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-118">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                      |
| <span data-ttu-id="61c86-119">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-119">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="61c86-120">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-120">Gets or sets the background color of the control.</span></span>                                                                                       |
| <span data-ttu-id="61c86-121">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-121">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="61c86-122">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-122">Determines whether the control background can be transparent.</span></span>                                                                           |
| <span data-ttu-id="61c86-123">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-123">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="61c86-124">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-124">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                             |
| <span data-ttu-id="61c86-125">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-125">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="61c86-126">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-126">Gets or sets the style of the borderline of the control.</span></span>                                                                                |
| <span data-ttu-id="61c86-127">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-127">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="61c86-128">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-128">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="61c86-129">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-129">Gets or sets the character set of the font.</span></span>                                                                                             |
| <span data-ttu-id="61c86-130">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-130">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="61c86-131">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-131">Gets or sets the color scheme of the control.</span></span>                                                                                           |
| <span data-ttu-id="61c86-132">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-132">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="61c86-133">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-133">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                     |
| <span data-ttu-id="61c86-134">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="61c86-134">public int containerId()</span></span>                                                                                    | <span data-ttu-id="61c86-135">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="61c86-135">Retrieves the ID of the parent container for the control.</span></span>                                                                               |
| <span data-ttu-id="61c86-136">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-136">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="61c86-137">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-137">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                         |
| <span data-ttu-id="61c86-138">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-138">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="61c86-139">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-139">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="61c86-140">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-140">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="61c86-141">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-141">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="61c86-142">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-142">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                |
| <span data-ttu-id="61c86-143">public int direction(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-143">public int direction(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="61c86-144">public int displayHeight(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="61c86-144">public int displayHeight(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                         |
| <span data-ttu-id="61c86-145">public AutoMode displayHeightMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="61c86-145">public AutoMode displayHeightMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                         |
| <span data-ttu-id="61c86-146">public int displayHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-146">public int displayHeightValue(\[int value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="61c86-147">public int displayLength(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="61c86-147">public int displayLength(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                         |
| <span data-ttu-id="61c86-148">public AutoMode displayLengthMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="61c86-148">public AutoMode displayLengthMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                         |
| <span data-ttu-id="61c86-149">public int displayLengthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-149">public int displayLengthValue(\[int value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="61c86-150">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-150">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="61c86-151">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-151">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="61c86-152">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-152">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                       |
| <span data-ttu-id="61c86-153">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-153">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="61c86-154">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-154">Determines whether to enable or disable the object.</span></span>                                                                                     |
| <span data-ttu-id="61c86-155">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-155">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                         |
| <span data-ttu-id="61c86-156">public int fastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-156">public int fastTabSummary(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="61c86-157">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-157">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="61c86-158">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-158">Gets or sets the name of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="61c86-159">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-159">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="61c86-160">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-160">Gets or sets the size of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="61c86-161">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-161">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="61c86-162">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-162">Gets or sets the text color for the control to use.</span></span>                                                                                     |
| <span data-ttu-id="61c86-163">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="61c86-163">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="61c86-164">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-164">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="61c86-165">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-165">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="61c86-166">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-166">Gets or sets a calculation mode for the height of the control.</span></span>                                                                          |
| <span data-ttu-id="61c86-167">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-167">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="61c86-168">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-168">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="61c86-169">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-169">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="61c86-170">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-170">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                |
| <span data-ttu-id="61c86-171">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-171">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="61c86-172">public int id()</span><span class="sxs-lookup"><span data-stu-id="61c86-172">public int id()</span></span>                                                                                             | <span data-ttu-id="61c86-173">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="61c86-173">Retrieves the ID of the control.</span></span>                                                                                                        |
| <span data-ttu-id="61c86-174">public int iMEMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-174">public int iMEMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="61c86-175">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="61c86-175">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="61c86-176">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="61c86-176">Retrieves a value that indicates whether the control is a container control.</span></span>                                                            |
| <span data-ttu-id="61c86-177">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-177">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="61c86-178">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-178">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="61c86-179">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-179">Gets or sets the label for a control.</span></span>                                                                                                   |
| <span data-ttu-id="61c86-180">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-180">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="61c86-181">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-181">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="61c86-182">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-182">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="61c86-183">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-183">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="61c86-184">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-184">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="61c86-185">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-185">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="61c86-186">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-186">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="61c86-187">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="61c86-187">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="61c86-188">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-188">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="61c86-189">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-189">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="61c86-190">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-190">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                         |
| <span data-ttu-id="61c86-191">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-191">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="61c86-192">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-192">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                         |
| <span data-ttu-id="61c86-193">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="61c86-193">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="61c86-194">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-194">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="61c86-195">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-195">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="61c86-196">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="61c86-196">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="61c86-197">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-197">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="61c86-198">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-198">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="61c86-199">public int limitText(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="61c86-199">public int limitText(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="61c86-200">public AutoMode limitTextMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="61c86-200">public AutoMode limitTextMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                         |
| <span data-ttu-id="61c86-201">public int limitTextValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-201">public int limitTextValue(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="61c86-202">public int lookupButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-202">public int lookupButton(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="61c86-203">public boolean mandatory(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-203">public boolean mandatory(\[boolean value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="61c86-204">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-204">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="61c86-205">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-205">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="61c86-206">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-206">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="61c86-207">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-207">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="61c86-208">public boolean replaceOnLookup(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-208">public boolean replaceOnLookup(\[boolean value\])</span></span>                                                           |                                                                                                                                         |
| <span data-ttu-id="61c86-209">public int searchAfterInput(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-209">public int searchAfterInput(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="61c86-210">public int searchMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-210">public int searchMode(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="61c86-211">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-211">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="61c86-212">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-212">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="61c86-213">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-213">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="61c86-214">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="61c86-214">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>         |
| <span data-ttu-id="61c86-215">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-215">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                         |
| <span data-ttu-id="61c86-216">public int timeFormat(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-216">public int timeFormat(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="61c86-217">public int timeHours(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-217">public int timeHours(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="61c86-218">public int timeMinute(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-218">public int timeMinute(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="61c86-219">public int timeSeconds(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-219">public int timeSeconds(\[int value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="61c86-220">public int timeSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-220">public int timeSeparator(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="61c86-221">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="61c86-221">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="61c86-222">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-222">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="61c86-223">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-223">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="61c86-224">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-224">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="61c86-225">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-225">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="61c86-226">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="61c86-226">Sets or returns the underline property for the text in the control.</span></span>                                                                     |
| <span data-ttu-id="61c86-227">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-227">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="61c86-228">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-228">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="61c86-229">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-229">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="61c86-230">public int value(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-230">public int value(\[int value\])</span></span>                                                                             |                                                                                                                                         |
| <span data-ttu-id="61c86-231">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="61c86-231">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="61c86-232">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="61c86-232">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="61c86-233">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-233">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="61c86-234">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-234">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="61c86-235">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-235">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="61c86-236">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="61c86-236">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="61c86-237">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-237">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="61c86-238">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-238">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="61c86-239">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-239">Gets or sets the calculation mode of the width of the control.</span></span>                                                                          |
| <span data-ttu-id="61c86-240">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="61c86-240">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="61c86-241">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-241">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="61c86-242">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="61c86-242">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="61c86-243">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="61c86-243">Method alignControl</span></span>

<span data-ttu-id="61c86-244">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-244">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="61c86-245">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="61c86-245">Parameters - alignControl</span></span>

<span data-ttu-id="61c86-246">値</span><span class="sxs-lookup"><span data-stu-id="61c86-246">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="61c86-247">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="61c86-247">Return Value - alignControl</span></span>

<span data-ttu-id="61c86-248">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="61c86-248">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="61c86-249">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="61c86-249">Remarks - alignControl</span></span>

<span data-ttu-id="61c86-250">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="61c86-250">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="61c86-251">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="61c86-251">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="61c86-252">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="61c86-252">Parameters - alignment</span></span>

<span data-ttu-id="61c86-253">値</span><span class="sxs-lookup"><span data-stu-id="61c86-253">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="61c86-254">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="61c86-254">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="61c86-255">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="61c86-255">Method allowEdit</span></span>

<span data-ttu-id="61c86-256">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-256">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="61c86-257">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="61c86-257">Parameters - allowEdit</span></span>

<span data-ttu-id="61c86-258">値</span><span class="sxs-lookup"><span data-stu-id="61c86-258">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="61c86-259">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="61c86-259">Return Value - allowEdit</span></span>

<span data-ttu-id="61c86-260">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="61c86-260">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="61c86-261">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="61c86-261">Remarks - allowEdit</span></span>

<span data-ttu-id="61c86-262">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="61c86-262">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="61c86-263">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="61c86-263">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="61c86-264">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="61c86-264">Parameters - arrayIndex</span></span>

<span data-ttu-id="61c86-265">値</span><span class="sxs-lookup"><span data-stu-id="61c86-265">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="61c86-266">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="61c86-266">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="61c86-267">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="61c86-267">Method autoDeclaration</span></span>

<span data-ttu-id="61c86-268">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-268">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="61c86-269">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="61c86-269">Parameters - autoDeclaration</span></span>

<span data-ttu-id="61c86-270">値</span><span class="sxs-lookup"><span data-stu-id="61c86-270">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="61c86-271">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="61c86-271">Return Value - autoDeclaration</span></span>

<span data-ttu-id="61c86-272">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="61c86-272">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="61c86-273">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="61c86-273">Remarks - autoDeclaration</span></span>

<span data-ttu-id="61c86-274">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="61c86-274">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="61c86-275">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="61c86-275">Method backgroundColor</span></span>

<span data-ttu-id="61c86-276">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-276">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="61c86-277">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="61c86-277">Parameters - backgroundColor</span></span>

<span data-ttu-id="61c86-278">値</span><span class="sxs-lookup"><span data-stu-id="61c86-278">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="61c86-279">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="61c86-279">Return Value - backgroundColor</span></span>

<span data-ttu-id="61c86-280">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="61c86-280">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="61c86-281">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="61c86-281">Remarks - backgroundColor</span></span>

<span data-ttu-id="61c86-282">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="61c86-282">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="61c86-283">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="61c86-283">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="61c86-284">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="61c86-284">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="61c86-285">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="61c86-285">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="61c86-286">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="61c86-286">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="61c86-287">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="61c86-287">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="61c86-288">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="61c86-288">Method backStyle</span></span>

<span data-ttu-id="61c86-289">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-289">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="61c86-290">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="61c86-290">Parameters - backStyle</span></span>

<span data-ttu-id="61c86-291">値</span><span class="sxs-lookup"><span data-stu-id="61c86-291">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="61c86-292">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="61c86-292">Return Value - backStyle</span></span>

<span data-ttu-id="61c86-293">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="61c86-293">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="61c86-294">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="61c86-294">Method bold</span></span>

<span data-ttu-id="61c86-295">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-295">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="61c86-296">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="61c86-296">Parameters - bold</span></span>

<span data-ttu-id="61c86-297">値</span><span class="sxs-lookup"><span data-stu-id="61c86-297">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="61c86-298">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="61c86-298">Return Value - bold</span></span>

<span data-ttu-id="61c86-299">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="61c86-299">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="61c86-300">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="61c86-300">Remarks - bold</span></span>

<span data-ttu-id="61c86-301">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="61c86-301">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="61c86-302">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="61c86-302">0 Use the default font weight.</span></span>
-   <span data-ttu-id="61c86-303">1 シン。</span><span class="sxs-lookup"><span data-stu-id="61c86-303">1 Thin.</span></span>
-   <span data-ttu-id="61c86-304">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="61c86-304">2 Extra-light.</span></span>
-   <span data-ttu-id="61c86-305">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="61c86-305">3 Light.</span></span>
-   <span data-ttu-id="61c86-306">4 標準。</span><span class="sxs-lookup"><span data-stu-id="61c86-306">4 Normal.</span></span>
-   <span data-ttu-id="61c86-307">5 中。</span><span class="sxs-lookup"><span data-stu-id="61c86-307">5 Medium.</span></span>
-   <span data-ttu-id="61c86-308">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="61c86-308">6 Semibold.</span></span>
-   <span data-ttu-id="61c86-309">7 太字。</span><span class="sxs-lookup"><span data-stu-id="61c86-309">7 Bold.</span></span>
-   <span data-ttu-id="61c86-310">8 極太。</span><span class="sxs-lookup"><span data-stu-id="61c86-310">8 Extra-bold.</span></span>
-   <span data-ttu-id="61c86-311">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="61c86-311">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="61c86-312">メソッド border</span><span class="sxs-lookup"><span data-stu-id="61c86-312">Method border</span></span>

<span data-ttu-id="61c86-313">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-313">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="61c86-314">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="61c86-314">Parameters - border</span></span>

<span data-ttu-id="61c86-315">値</span><span class="sxs-lookup"><span data-stu-id="61c86-315">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="61c86-316">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="61c86-316">Return Value - border</span></span>

<span data-ttu-id="61c86-317">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="61c86-317">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="61c86-318">備考 - border</span><span class="sxs-lookup"><span data-stu-id="61c86-318">Remarks - border</span></span>

<span data-ttu-id="61c86-319">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="61c86-319">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="61c86-320">値です。</span><span class="sxs-lookup"><span data-stu-id="61c86-320">Value.</span></span> | <span data-ttu-id="61c86-321">説明。</span><span class="sxs-lookup"><span data-stu-id="61c86-321">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="61c86-322">0</span><span class="sxs-lookup"><span data-stu-id="61c86-322">0</span></span>      | <span data-ttu-id="61c86-323">自動。</span><span class="sxs-lookup"><span data-stu-id="61c86-323">Auto.</span></span>        |
| <span data-ttu-id="61c86-324">1</span><span class="sxs-lookup"><span data-stu-id="61c86-324">1</span></span>      | <span data-ttu-id="61c86-325">3D。</span><span class="sxs-lookup"><span data-stu-id="61c86-325">3D.</span></span>          |
| <span data-ttu-id="61c86-326">2</span><span class="sxs-lookup"><span data-stu-id="61c86-326">2</span></span>      | <span data-ttu-id="61c86-327">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="61c86-327">Single line.</span></span> |
| <span data-ttu-id="61c86-328">3</span><span class="sxs-lookup"><span data-stu-id="61c86-328">3</span></span>      | <span data-ttu-id="61c86-329">均一。</span><span class="sxs-lookup"><span data-stu-id="61c86-329">Flat.</span></span>        |
| <span data-ttu-id="61c86-330">4</span><span class="sxs-lookup"><span data-stu-id="61c86-330">4</span></span>      | <span data-ttu-id="61c86-331">なし。</span><span class="sxs-lookup"><span data-stu-id="61c86-331">None.</span></span>        |

## <a name="method-cachedatamethod"></a><span data-ttu-id="61c86-332">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="61c86-332">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="61c86-333">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="61c86-333">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="61c86-334">値</span><span class="sxs-lookup"><span data-stu-id="61c86-334">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="61c86-335">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="61c86-335">Return Value - cacheDataMethod</span></span>

## <a name="method-characterset"></a><span data-ttu-id="61c86-336">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="61c86-336">Method characterSet</span></span>

<span data-ttu-id="61c86-337">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-337">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="61c86-338">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="61c86-338">Parameters - characterSet</span></span>

<span data-ttu-id="61c86-339">値</span><span class="sxs-lookup"><span data-stu-id="61c86-339">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="61c86-340">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="61c86-340">Return Value - characterSet</span></span>

<span data-ttu-id="61c86-341">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="61c86-341">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="61c86-342">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="61c86-342">Remarks - characterSet</span></span>

<span data-ttu-id="61c86-343">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="61c86-343">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="61c86-344">値です。</span><span class="sxs-lookup"><span data-stu-id="61c86-344">Value.</span></span> | <span data-ttu-id="61c86-345">説明。</span><span class="sxs-lookup"><span data-stu-id="61c86-345">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="61c86-346">0</span><span class="sxs-lookup"><span data-stu-id="61c86-346">0</span></span>      | <span data-ttu-id="61c86-347">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="61c86-347">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="61c86-348">1</span><span class="sxs-lookup"><span data-stu-id="61c86-348">1</span></span>      | <span data-ttu-id="61c86-349">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="61c86-349">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="61c86-350">2</span><span class="sxs-lookup"><span data-stu-id="61c86-350">2</span></span>      | <span data-ttu-id="61c86-351">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="61c86-351">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="61c86-352">77</span><span class="sxs-lookup"><span data-stu-id="61c86-352">77</span></span>     | <span data-ttu-id="61c86-353">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="61c86-353">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="61c86-354">128</span><span class="sxs-lookup"><span data-stu-id="61c86-354">128</span></span>    | <span data-ttu-id="61c86-355">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="61c86-355">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="61c86-356">129</span><span class="sxs-lookup"><span data-stu-id="61c86-356">129</span></span>    | <span data-ttu-id="61c86-357">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="61c86-357">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="61c86-358">134</span><span class="sxs-lookup"><span data-stu-id="61c86-358">134</span></span>    | <span data-ttu-id="61c86-359">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="61c86-359">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="61c86-360">136</span><span class="sxs-lookup"><span data-stu-id="61c86-360">136</span></span>    | <span data-ttu-id="61c86-361">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="61c86-361">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="61c86-362">161</span><span class="sxs-lookup"><span data-stu-id="61c86-362">161</span></span>    | <span data-ttu-id="61c86-363">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="61c86-363">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="61c86-364">162</span><span class="sxs-lookup"><span data-stu-id="61c86-364">162</span></span>    | <span data-ttu-id="61c86-365">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="61c86-365">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="61c86-366">163</span><span class="sxs-lookup"><span data-stu-id="61c86-366">163</span></span>    | <span data-ttu-id="61c86-367">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="61c86-367">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="61c86-368">186</span><span class="sxs-lookup"><span data-stu-id="61c86-368">186</span></span>    | <span data-ttu-id="61c86-369">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="61c86-369">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="61c86-370">204</span><span class="sxs-lookup"><span data-stu-id="61c86-370">204</span></span>    | <span data-ttu-id="61c86-371">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="61c86-371">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="61c86-372">238</span><span class="sxs-lookup"><span data-stu-id="61c86-372">238</span></span>    | <span data-ttu-id="61c86-373">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="61c86-373">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="61c86-374">255</span><span class="sxs-lookup"><span data-stu-id="61c86-374">255</span></span>    | <span data-ttu-id="61c86-375">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="61c86-375">OEM\_CHARSET</span></span>         |

<span data-ttu-id="61c86-376">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="61c86-376">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="61c86-377">値です。</span><span class="sxs-lookup"><span data-stu-id="61c86-377">Value.</span></span> | <span data-ttu-id="61c86-378">説明。</span><span class="sxs-lookup"><span data-stu-id="61c86-378">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="61c86-379">130</span><span class="sxs-lookup"><span data-stu-id="61c86-379">130</span></span>    | <span data-ttu-id="61c86-380">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="61c86-380">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="61c86-381">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="61c86-381">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="61c86-382">値です。</span><span class="sxs-lookup"><span data-stu-id="61c86-382">Value.</span></span> | <span data-ttu-id="61c86-383">説明。</span><span class="sxs-lookup"><span data-stu-id="61c86-383">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="61c86-384">177</span><span class="sxs-lookup"><span data-stu-id="61c86-384">177</span></span>    | <span data-ttu-id="61c86-385">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="61c86-385">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="61c86-386">178</span><span class="sxs-lookup"><span data-stu-id="61c86-386">178</span></span>    | <span data-ttu-id="61c86-387">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="61c86-387">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="61c86-388">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="61c86-388">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="61c86-389">値です。</span><span class="sxs-lookup"><span data-stu-id="61c86-389">Value.</span></span> | <span data-ttu-id="61c86-390">説明。</span><span class="sxs-lookup"><span data-stu-id="61c86-390">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="61c86-391">222</span><span class="sxs-lookup"><span data-stu-id="61c86-391">222</span></span>    | <span data-ttu-id="61c86-392">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="61c86-392">THAI\_CHARSET</span></span> |

<span data-ttu-id="61c86-393">既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="61c86-393">The default character set is set to a value, depending on the current system locale.</span></span> <span data-ttu-id="61c86-394">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="61c86-394">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="61c86-395">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="61c86-395">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="61c86-396">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="61c86-396">Method colorScheme</span></span>

<span data-ttu-id="61c86-397">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-397">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="61c86-398">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="61c86-398">Parameters - colorScheme</span></span>

<span data-ttu-id="61c86-399">値</span><span class="sxs-lookup"><span data-stu-id="61c86-399">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="61c86-400">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="61c86-400">Return Value - colorScheme</span></span>

<span data-ttu-id="61c86-401">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="61c86-401">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="61c86-402">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="61c86-402">Remarks - colorScheme</span></span>

<span data-ttu-id="61c86-403">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="61c86-403">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="61c86-404">値です。</span><span class="sxs-lookup"><span data-stu-id="61c86-404">Value.</span></span> | <span data-ttu-id="61c86-405">スタイル。</span><span class="sxs-lookup"><span data-stu-id="61c86-405">Style.</span></span>                         |
|--------|--------------------------------|
| <span data-ttu-id="61c86-406">0</span><span class="sxs-lookup"><span data-stu-id="61c86-406">0</span></span>      | <span data-ttu-id="61c86-407">既定。</span><span class="sxs-lookup"><span data-stu-id="61c86-407">Default.</span></span>                       |
| <span data-ttu-id="61c86-408">1</span><span class="sxs-lookup"><span data-stu-id="61c86-408">1</span></span>      | <span data-ttu-id="61c86-409">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="61c86-409">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="61c86-410">2</span><span class="sxs-lookup"><span data-stu-id="61c86-410">2</span></span>      | <span data-ttu-id="61c86-411">真の配色。</span><span class="sxs-lookup"><span data-stu-id="61c86-411">The true-color scheme.</span></span>         |

## <a name="method-configurationkey"></a><span data-ttu-id="61c86-412">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="61c86-412">Method configurationKey</span></span>

<span data-ttu-id="61c86-413">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-413">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="61c86-414">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="61c86-414">Parameters - configurationKey</span></span>

<span data-ttu-id="61c86-415">値</span><span class="sxs-lookup"><span data-stu-id="61c86-415">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="61c86-416">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="61c86-416">Return Value - configurationKey</span></span>

<span data-ttu-id="61c86-417">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="61c86-417">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="61c86-418">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="61c86-418">Remarks - configurationKey</span></span>

<span data-ttu-id="61c86-419">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="61c86-419">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="61c86-420">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="61c86-420">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="61c86-421">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="61c86-421">Method containerId</span></span>

<span data-ttu-id="61c86-422">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="61c86-422">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="61c86-423">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="61c86-423">Return Value - containerId</span></span>

<span data-ttu-id="61c86-424">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="61c86-424">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="61c86-425">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="61c86-425">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="61c86-426">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="61c86-426">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="61c86-427">値</span><span class="sxs-lookup"><span data-stu-id="61c86-427">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="61c86-428">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="61c86-428">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="61c86-429">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="61c86-429">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="61c86-430">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="61c86-430">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="61c86-431">値</span><span class="sxs-lookup"><span data-stu-id="61c86-431">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="61c86-432">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="61c86-432">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="61c86-433">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="61c86-433">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="61c86-434">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="61c86-434">Parameters - dataField</span></span>

<span data-ttu-id="61c86-435">値</span><span class="sxs-lookup"><span data-stu-id="61c86-435">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="61c86-436">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="61c86-436">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="61c86-437">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="61c86-437">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="61c86-438">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="61c86-438">Parameters - dataMethod</span></span>

<span data-ttu-id="61c86-439">値</span><span class="sxs-lookup"><span data-stu-id="61c86-439">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="61c86-440">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="61c86-440">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="61c86-441">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="61c86-441">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="61c86-442">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="61c86-442">Parameters - dataRelationPath</span></span>

<span data-ttu-id="61c86-443">値</span><span class="sxs-lookup"><span data-stu-id="61c86-443">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="61c86-444">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="61c86-444">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="61c86-445">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="61c86-445">Method dataSource</span></span>

<span data-ttu-id="61c86-446">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-446">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="61c86-447">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="61c86-447">Parameters - dataSource</span></span>

<span data-ttu-id="61c86-448">値</span><span class="sxs-lookup"><span data-stu-id="61c86-448">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="61c86-449">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="61c86-449">Return Value - dataSource</span></span>

<span data-ttu-id="61c86-450">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="61c86-450">The identifier of the data source that will be used.</span></span>

## <a name="method-direction"></a><span data-ttu-id="61c86-451">メソッド direction</span><span class="sxs-lookup"><span data-stu-id="61c86-451">Method direction</span></span>

```xpp
public int direction([int value])
```

### <a name="parameters---direction"></a><span data-ttu-id="61c86-452">パラメーター - direction</span><span class="sxs-lookup"><span data-stu-id="61c86-452">Parameters - direction</span></span>

<span data-ttu-id="61c86-453">値</span><span class="sxs-lookup"><span data-stu-id="61c86-453">value</span></span>  

### <a name="return-value---direction"></a><span data-ttu-id="61c86-454">戻り値 - direction</span><span class="sxs-lookup"><span data-stu-id="61c86-454">Return Value - direction</span></span>

## <a name="method-displayheight"></a><span data-ttu-id="61c86-455">メソッド displayHeight</span><span class="sxs-lookup"><span data-stu-id="61c86-455">Method displayHeight</span></span>

```xpp
public int displayHeight([int value], [AutoMode mode])
```

### <a name="parameters---displayheight"></a><span data-ttu-id="61c86-456">パラメーター - displayHeight</span><span class="sxs-lookup"><span data-stu-id="61c86-456">Parameters - displayHeight</span></span>

<span data-ttu-id="61c86-457">値</span><span class="sxs-lookup"><span data-stu-id="61c86-457">value</span></span>  

<!-- -->

<span data-ttu-id="61c86-458">モード</span><span class="sxs-lookup"><span data-stu-id="61c86-458">mode</span></span>  

### <a name="return-value---displayheight"></a><span data-ttu-id="61c86-459">戻り値 - displayHeight</span><span class="sxs-lookup"><span data-stu-id="61c86-459">Return Value - displayHeight</span></span>

## <a name="method-displayheightmode"></a><span data-ttu-id="61c86-460">メソッド displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="61c86-460">Method displayHeightMode</span></span>

```xpp
public AutoMode displayHeightMode([AutoMode mode])
```

### <a name="parameters---displayheightmode"></a><span data-ttu-id="61c86-461">パラメーター - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="61c86-461">Parameters - displayHeightMode</span></span>

<span data-ttu-id="61c86-462">モード</span><span class="sxs-lookup"><span data-stu-id="61c86-462">mode</span></span>  

### <a name="return-value---displayheightmode"></a><span data-ttu-id="61c86-463">戻り値 - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="61c86-463">Return Value - displayHeightMode</span></span>

## <a name="method-displayheightvalue"></a><span data-ttu-id="61c86-464">メソッド displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="61c86-464">Method displayHeightValue</span></span>

```xpp
public int displayHeightValue([int value])
```

### <a name="parameters---displayheightvalue"></a><span data-ttu-id="61c86-465">パラメーター - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="61c86-465">Parameters - displayHeightValue</span></span>

<span data-ttu-id="61c86-466">値</span><span class="sxs-lookup"><span data-stu-id="61c86-466">value</span></span>  

### <a name="return-value---displayheightvalue"></a><span data-ttu-id="61c86-467">戻り値 - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="61c86-467">Return Value - displayHeightValue</span></span>

## <a name="method-displaylength"></a><span data-ttu-id="61c86-468">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="61c86-468">Method displayLength</span></span>

```xpp
public int displayLength([int value], [AutoMode mode])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="61c86-469">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="61c86-469">Parameters - displayLength</span></span>

<span data-ttu-id="61c86-470">値</span><span class="sxs-lookup"><span data-stu-id="61c86-470">value</span></span>  

<!-- -->

<span data-ttu-id="61c86-471">モード</span><span class="sxs-lookup"><span data-stu-id="61c86-471">mode</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="61c86-472">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="61c86-472">Return Value - displayLength</span></span>

## <a name="method-displaylengthmode"></a><span data-ttu-id="61c86-473">メソッド displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="61c86-473">Method displayLengthMode</span></span>

```xpp
public AutoMode displayLengthMode([AutoMode mode])
```

### <a name="parameters---displaylengthmode"></a><span data-ttu-id="61c86-474">パラメーター - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="61c86-474">Parameters - displayLengthMode</span></span>

<span data-ttu-id="61c86-475">モード</span><span class="sxs-lookup"><span data-stu-id="61c86-475">mode</span></span>  

### <a name="return-value---displaylengthmode"></a><span data-ttu-id="61c86-476">戻り値 - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="61c86-476">Return Value - displayLengthMode</span></span>

## <a name="method-displaylengthvalue"></a><span data-ttu-id="61c86-477">メソッド displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="61c86-477">Method displayLengthValue</span></span>

```xpp
public int displayLengthValue([int value])
```

### <a name="parameters---displaylengthvalue"></a><span data-ttu-id="61c86-478">パラメーター - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="61c86-478">Parameters - displayLengthValue</span></span>

<span data-ttu-id="61c86-479">値</span><span class="sxs-lookup"><span data-stu-id="61c86-479">value</span></span>  

### <a name="return-value---displaylengthvalue"></a><span data-ttu-id="61c86-480">戻り値 - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="61c86-480">Return Value - displayLengthValue</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="61c86-481">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="61c86-481">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="61c86-482">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="61c86-482">Parameters - displayTarget</span></span>

<span data-ttu-id="61c86-483">値</span><span class="sxs-lookup"><span data-stu-id="61c86-483">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="61c86-484">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="61c86-484">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="61c86-485">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="61c86-485">Method dragDrop</span></span>

<span data-ttu-id="61c86-486">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-486">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="61c86-487">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="61c86-487">Parameters - dragDrop</span></span>

<span data-ttu-id="61c86-488">値</span><span class="sxs-lookup"><span data-stu-id="61c86-488">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="61c86-489">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="61c86-489">Return Value - dragDrop</span></span>

<span data-ttu-id="61c86-490">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="61c86-490">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="61c86-491">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="61c86-491">Method enabled</span></span>

<span data-ttu-id="61c86-492">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-492">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="61c86-493">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="61c86-493">Parameters - enabled</span></span>

<span data-ttu-id="61c86-494">値</span><span class="sxs-lookup"><span data-stu-id="61c86-494">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="61c86-495">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="61c86-495">Return Value - enabled</span></span>

<span data-ttu-id="61c86-496">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="61c86-496">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="61c86-497">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="61c86-497">Remarks - enabled</span></span>

<span data-ttu-id="61c86-498">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="61c86-498">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="61c86-499">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="61c86-499">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="61c86-500">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="61c86-500">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="61c86-501">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="61c86-501">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="61c86-502">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="61c86-502">Parameters - extendedDataType</span></span>

<span data-ttu-id="61c86-503">値</span><span class="sxs-lookup"><span data-stu-id="61c86-503">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="61c86-504">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="61c86-504">Return Value - extendedDataType</span></span>

## <a name="method-fasttabsummary"></a><span data-ttu-id="61c86-505">メソッド fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="61c86-505">Method fastTabSummary</span></span>

```xpp
public int fastTabSummary([int value])
```

### <a name="parameters---fasttabsummary"></a><span data-ttu-id="61c86-506">パラメーター - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="61c86-506">Parameters - fastTabSummary</span></span>

<span data-ttu-id="61c86-507">値</span><span class="sxs-lookup"><span data-stu-id="61c86-507">value</span></span>  

### <a name="return-value---fasttabsummary"></a><span data-ttu-id="61c86-508">戻り値 - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="61c86-508">Return Value - fastTabSummary</span></span>

## <a name="method-font"></a><span data-ttu-id="61c86-509">メソッド font</span><span class="sxs-lookup"><span data-stu-id="61c86-509">Method font</span></span>

<span data-ttu-id="61c86-510">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-510">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="61c86-511">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="61c86-511">Parameters - font</span></span>

<span data-ttu-id="61c86-512">値</span><span class="sxs-lookup"><span data-stu-id="61c86-512">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="61c86-513">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="61c86-513">Return Value - font</span></span>

<span data-ttu-id="61c86-514">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="61c86-514">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="61c86-515">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="61c86-515">Method fontSize</span></span>

<span data-ttu-id="61c86-516">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-516">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="61c86-517">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="61c86-517">Parameters - fontSize</span></span>

<span data-ttu-id="61c86-518">値</span><span class="sxs-lookup"><span data-stu-id="61c86-518">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="61c86-519">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="61c86-519">Return Value - fontSize</span></span>

<span data-ttu-id="61c86-520">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="61c86-520">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="61c86-521">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="61c86-521">Method foregroundColor</span></span>

<span data-ttu-id="61c86-522">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-522">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="61c86-523">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="61c86-523">Parameters - foregroundColor</span></span>

<span data-ttu-id="61c86-524">値</span><span class="sxs-lookup"><span data-stu-id="61c86-524">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="61c86-525">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="61c86-525">Return Value - foregroundColor</span></span>

<span data-ttu-id="61c86-526">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="61c86-526">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="61c86-527">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="61c86-527">Remarks - foregroundColor</span></span>

<span data-ttu-id="61c86-528">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="61c86-528">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="61c86-529">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="61c86-529">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="61c86-530">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="61c86-530">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="61c86-531">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="61c86-531">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="61c86-532">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="61c86-532">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="61c86-533">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="61c86-533">The maximum value for a single byte is 255.</span></span>

## <a name="method-height"></a><span data-ttu-id="61c86-534">メソッド height</span><span class="sxs-lookup"><span data-stu-id="61c86-534">Method height</span></span>

<span data-ttu-id="61c86-535">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-535">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="61c86-536">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="61c86-536">Parameters - height</span></span>

<span data-ttu-id="61c86-537">値</span><span class="sxs-lookup"><span data-stu-id="61c86-537">value</span></span>  

<!-- -->

<span data-ttu-id="61c86-538">モード</span><span class="sxs-lookup"><span data-stu-id="61c86-538">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="61c86-539">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="61c86-539">Return Value - height</span></span>

<span data-ttu-id="61c86-540">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="61c86-540">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="61c86-541">備考 - height</span><span class="sxs-lookup"><span data-stu-id="61c86-541">Remarks - height</span></span>

<span data-ttu-id="61c86-542">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="61c86-542">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="61c86-543">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="61c86-543">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="61c86-544">モード。</span><span class="sxs-lookup"><span data-stu-id="61c86-544">Mode.</span></span>            | <span data-ttu-id="61c86-545">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="61c86-545">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="61c86-546">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="61c86-546">-1 Exact.</span></span>        | <span data-ttu-id="61c86-547">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="61c86-547">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="61c86-548">0 自動。</span><span class="sxs-lookup"><span data-stu-id="61c86-548">0 Auto.</span></span>          | <span data-ttu-id="61c86-549">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="61c86-549">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="61c86-550">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="61c86-550">1 Column height.</span></span> | <span data-ttu-id="61c86-551">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="61c86-551">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="61c86-552">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="61c86-552">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="61c86-553">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="61c86-553">Method heightMode</span></span>

<span data-ttu-id="61c86-554">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-554">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="61c86-555">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="61c86-555">Parameters - heightMode</span></span>

<span data-ttu-id="61c86-556">値</span><span class="sxs-lookup"><span data-stu-id="61c86-556">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="61c86-557">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="61c86-557">Return Value - heightMode</span></span>

<span data-ttu-id="61c86-558">計算モード。</span><span class="sxs-lookup"><span data-stu-id="61c86-558">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="61c86-559">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="61c86-559">Remarks - heightMode</span></span>

<span data-ttu-id="61c86-560">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="61c86-560">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="61c86-561">モード。</span><span class="sxs-lookup"><span data-stu-id="61c86-561">Mode.</span></span>          | <span data-ttu-id="61c86-562">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="61c86-562">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="61c86-563">正確。</span><span class="sxs-lookup"><span data-stu-id="61c86-563">Exact.</span></span>         | <span data-ttu-id="61c86-564">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="61c86-564">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="61c86-565">自動。</span><span class="sxs-lookup"><span data-stu-id="61c86-565">Auto.</span></span>          | <span data-ttu-id="61c86-566">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="61c86-566">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="61c86-567">列の高さ</span><span class="sxs-lookup"><span data-stu-id="61c86-567">Column height.</span></span> | <span data-ttu-id="61c86-568">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="61c86-568">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="61c86-569">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="61c86-569">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="61c86-570">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="61c86-570">Method heightValue</span></span>

<span data-ttu-id="61c86-571">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-571">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="61c86-572">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="61c86-572">Parameters - heightValue</span></span>

<span data-ttu-id="61c86-573">値</span><span class="sxs-lookup"><span data-stu-id="61c86-573">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="61c86-574">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="61c86-574">Return Value - heightValue</span></span>

<span data-ttu-id="61c86-575">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="61c86-575">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="61c86-576">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="61c86-576">Remarks - heightValue</span></span>

<span data-ttu-id="61c86-577">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="61c86-577">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="61c86-578">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="61c86-578">Method helpText</span></span>

<span data-ttu-id="61c86-579">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-579">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="61c86-580">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="61c86-580">Parameters - helpText</span></span>

<span data-ttu-id="61c86-581">値</span><span class="sxs-lookup"><span data-stu-id="61c86-581">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="61c86-582">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="61c86-582">Return Value - helpText</span></span>

<span data-ttu-id="61c86-583">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="61c86-583">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="61c86-584">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="61c86-584">Remarks - helpText</span></span>

<span data-ttu-id="61c86-585">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-585">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="61c86-586">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="61c86-586">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="61c86-587">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="61c86-587">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="61c86-588">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="61c86-588">Parameters - hierarchyParent</span></span>

<span data-ttu-id="61c86-589">値</span><span class="sxs-lookup"><span data-stu-id="61c86-589">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="61c86-590">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="61c86-590">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="61c86-591">メソッド id</span><span class="sxs-lookup"><span data-stu-id="61c86-591">Method id</span></span>

<span data-ttu-id="61c86-592">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="61c86-592">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="61c86-593">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="61c86-593">Return Value - id</span></span>

<span data-ttu-id="61c86-594">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="61c86-594">The ID of the control.</span></span>

## <a name="method-imemode"></a><span data-ttu-id="61c86-595">メソッド iMEMode</span><span class="sxs-lookup"><span data-stu-id="61c86-595">Method iMEMode</span></span>

```xpp
public int iMEMode([int value])
```

### <a name="parameters---imemode"></a><span data-ttu-id="61c86-596">パラメーター - iMEMode</span><span class="sxs-lookup"><span data-stu-id="61c86-596">Parameters - iMEMode</span></span>

<span data-ttu-id="61c86-597">値</span><span class="sxs-lookup"><span data-stu-id="61c86-597">value</span></span>  

### <a name="return-value---imemode"></a><span data-ttu-id="61c86-598">戻り値 - iMEMode</span><span class="sxs-lookup"><span data-stu-id="61c86-598">Return Value - iMEMode</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="61c86-599">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="61c86-599">Method isContainer</span></span>

<span data-ttu-id="61c86-600">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="61c86-600">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="61c86-601">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="61c86-601">Return Value - isContainer</span></span>

<span data-ttu-id="61c86-602">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="61c86-602">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-italic"></a><span data-ttu-id="61c86-603">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="61c86-603">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="61c86-604">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="61c86-604">Parameters - italic</span></span>

<span data-ttu-id="61c86-605">値</span><span class="sxs-lookup"><span data-stu-id="61c86-605">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="61c86-606">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="61c86-606">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="61c86-607">メソッド label</span><span class="sxs-lookup"><span data-stu-id="61c86-607">Method label</span></span>

<span data-ttu-id="61c86-608">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-608">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="61c86-609">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="61c86-609">Parameters - label</span></span>

<span data-ttu-id="61c86-610">値</span><span class="sxs-lookup"><span data-stu-id="61c86-610">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="61c86-611">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="61c86-611">Return Value - label</span></span>

<span data-ttu-id="61c86-612">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="61c86-612">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="61c86-613">備考 - label</span><span class="sxs-lookup"><span data-stu-id="61c86-613">Remarks - label</span></span>

<span data-ttu-id="61c86-614">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-614">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="61c86-615">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="61c86-615">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="61c86-616">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="61c86-616">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="61c86-617">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="61c86-617">Parameters - labelAlignment</span></span>

<span data-ttu-id="61c86-618">値</span><span class="sxs-lookup"><span data-stu-id="61c86-618">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="61c86-619">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="61c86-619">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="61c86-620">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="61c86-620">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="61c86-621">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="61c86-621">Parameters - labelBold</span></span>

<span data-ttu-id="61c86-622">値</span><span class="sxs-lookup"><span data-stu-id="61c86-622">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="61c86-623">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="61c86-623">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="61c86-624">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="61c86-624">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="61c86-625">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="61c86-625">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="61c86-626">値</span><span class="sxs-lookup"><span data-stu-id="61c86-626">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="61c86-627">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="61c86-627">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="61c86-628">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="61c86-628">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="61c86-629">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="61c86-629">Parameters - labelFont</span></span>

<span data-ttu-id="61c86-630">値</span><span class="sxs-lookup"><span data-stu-id="61c86-630">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="61c86-631">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="61c86-631">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="61c86-632">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="61c86-632">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="61c86-633">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="61c86-633">Parameters - labelFontSize</span></span>

<span data-ttu-id="61c86-634">値</span><span class="sxs-lookup"><span data-stu-id="61c86-634">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="61c86-635">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="61c86-635">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="61c86-636">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="61c86-636">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="61c86-637">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="61c86-637">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="61c86-638">値</span><span class="sxs-lookup"><span data-stu-id="61c86-638">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="61c86-639">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="61c86-639">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="61c86-640">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="61c86-640">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="61c86-641">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="61c86-641">Parameters - labelGuide</span></span>

<span data-ttu-id="61c86-642">値</span><span class="sxs-lookup"><span data-stu-id="61c86-642">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="61c86-643">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="61c86-643">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="61c86-644">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="61c86-644">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="61c86-645">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="61c86-645">Parameters - labelHeight</span></span>

<span data-ttu-id="61c86-646">値</span><span class="sxs-lookup"><span data-stu-id="61c86-646">value</span></span>  

<!-- -->

<span data-ttu-id="61c86-647">モード</span><span class="sxs-lookup"><span data-stu-id="61c86-647">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="61c86-648">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="61c86-648">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="61c86-649">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="61c86-649">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="61c86-650">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="61c86-650">Parameters - labelHeightMode</span></span>

<span data-ttu-id="61c86-651">値</span><span class="sxs-lookup"><span data-stu-id="61c86-651">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="61c86-652">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="61c86-652">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="61c86-653">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="61c86-653">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="61c86-654">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="61c86-654">Parameters - labelHeightValue</span></span>

<span data-ttu-id="61c86-655">値</span><span class="sxs-lookup"><span data-stu-id="61c86-655">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="61c86-656">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="61c86-656">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="61c86-657">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="61c86-657">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="61c86-658">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="61c86-658">Parameters - labelItalic</span></span>

<span data-ttu-id="61c86-659">値</span><span class="sxs-lookup"><span data-stu-id="61c86-659">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="61c86-660">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="61c86-660">Return Value - labelItalic</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="61c86-661">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="61c86-661">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="61c86-662">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="61c86-662">Parameters - labelPosition</span></span>

<span data-ttu-id="61c86-663">値</span><span class="sxs-lookup"><span data-stu-id="61c86-663">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="61c86-664">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="61c86-664">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="61c86-665">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="61c86-665">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="61c86-666">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="61c86-666">Parameters - labelUnderline</span></span>

<span data-ttu-id="61c86-667">値</span><span class="sxs-lookup"><span data-stu-id="61c86-667">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="61c86-668">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="61c86-668">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="61c86-669">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="61c86-669">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="61c86-670">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="61c86-670">Parameters - labelWidth</span></span>

<span data-ttu-id="61c86-671">値</span><span class="sxs-lookup"><span data-stu-id="61c86-671">value</span></span>  

<!-- -->

<span data-ttu-id="61c86-672">モード</span><span class="sxs-lookup"><span data-stu-id="61c86-672">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="61c86-673">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="61c86-673">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="61c86-674">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="61c86-674">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="61c86-675">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="61c86-675">Parameters - labelWidthMode</span></span>

<span data-ttu-id="61c86-676">値</span><span class="sxs-lookup"><span data-stu-id="61c86-676">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="61c86-677">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="61c86-677">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="61c86-678">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="61c86-678">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="61c86-679">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="61c86-679">Parameters - labelWidthValue</span></span>

<span data-ttu-id="61c86-680">値</span><span class="sxs-lookup"><span data-stu-id="61c86-680">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="61c86-681">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="61c86-681">Return Value - labelWidthValue</span></span>

## <a name="method-left"></a><span data-ttu-id="61c86-682">メソッド left</span><span class="sxs-lookup"><span data-stu-id="61c86-682">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="61c86-683">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="61c86-683">Parameters - left</span></span>

<span data-ttu-id="61c86-684">値</span><span class="sxs-lookup"><span data-stu-id="61c86-684">value</span></span>  

<!-- -->

<span data-ttu-id="61c86-685">モード</span><span class="sxs-lookup"><span data-stu-id="61c86-685">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="61c86-686">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="61c86-686">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="61c86-687">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="61c86-687">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="61c86-688">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="61c86-688">Parameters - leftMode</span></span>

<span data-ttu-id="61c86-689">値</span><span class="sxs-lookup"><span data-stu-id="61c86-689">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="61c86-690">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="61c86-690">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="61c86-691">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="61c86-691">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="61c86-692">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="61c86-692">Parameters - leftValue</span></span>

<span data-ttu-id="61c86-693">値</span><span class="sxs-lookup"><span data-stu-id="61c86-693">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="61c86-694">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="61c86-694">Return Value - leftValue</span></span>

## <a name="method-limittext"></a><span data-ttu-id="61c86-695">メソッド limitText</span><span class="sxs-lookup"><span data-stu-id="61c86-695">Method limitText</span></span>

```xpp
public int limitText([int value], [AutoMode mode])
```

### <a name="parameters---limittext"></a><span data-ttu-id="61c86-696">パラメーター - limitText</span><span class="sxs-lookup"><span data-stu-id="61c86-696">Parameters - limitText</span></span>

<span data-ttu-id="61c86-697">値</span><span class="sxs-lookup"><span data-stu-id="61c86-697">value</span></span>  

<!-- -->

<span data-ttu-id="61c86-698">モード</span><span class="sxs-lookup"><span data-stu-id="61c86-698">mode</span></span>  

### <a name="return-value---limittext"></a><span data-ttu-id="61c86-699">戻り値 - limitText</span><span class="sxs-lookup"><span data-stu-id="61c86-699">Return Value - limitText</span></span>

## <a name="method-limittextmode"></a><span data-ttu-id="61c86-700">メソッド limitTextMode</span><span class="sxs-lookup"><span data-stu-id="61c86-700">Method limitTextMode</span></span>

```xpp
public AutoMode limitTextMode([AutoMode mode])
```

### <a name="parameters---limittextmode"></a><span data-ttu-id="61c86-701">パラメーター - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="61c86-701">Parameters - limitTextMode</span></span>

<span data-ttu-id="61c86-702">モード</span><span class="sxs-lookup"><span data-stu-id="61c86-702">mode</span></span>  

### <a name="return-value---limittextmode"></a><span data-ttu-id="61c86-703">戻り値 - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="61c86-703">Return Value - limitTextMode</span></span>

## <a name="method-limittextvalue"></a><span data-ttu-id="61c86-704">メソッド limitTextValue</span><span class="sxs-lookup"><span data-stu-id="61c86-704">Method limitTextValue</span></span>

```xpp
public int limitTextValue([int value])
```

### <a name="parameters---limittextvalue"></a><span data-ttu-id="61c86-705">パラメーター - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="61c86-705">Parameters - limitTextValue</span></span>

<span data-ttu-id="61c86-706">値</span><span class="sxs-lookup"><span data-stu-id="61c86-706">value</span></span>  

### <a name="return-value---limittextvalue"></a><span data-ttu-id="61c86-707">戻り値 - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="61c86-707">Return Value - limitTextValue</span></span>

## <a name="method-lookupbutton"></a><span data-ttu-id="61c86-708">メソッド lookupButton</span><span class="sxs-lookup"><span data-stu-id="61c86-708">Method lookupButton</span></span>

```xpp
public int lookupButton([int value])
```

### <a name="parameters---lookupbutton"></a><span data-ttu-id="61c86-709">パラメーター - lookupButton</span><span class="sxs-lookup"><span data-stu-id="61c86-709">Parameters - lookupButton</span></span>

<span data-ttu-id="61c86-710">値</span><span class="sxs-lookup"><span data-stu-id="61c86-710">value</span></span>  

### <a name="return-value---lookupbutton"></a><span data-ttu-id="61c86-711">戻り値 - lookupButton</span><span class="sxs-lookup"><span data-stu-id="61c86-711">Return Value - lookupButton</span></span>

## <a name="method-mandatory"></a><span data-ttu-id="61c86-712">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="61c86-712">Method mandatory</span></span>

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a><span data-ttu-id="61c86-713">パラメーター - mandatory</span><span class="sxs-lookup"><span data-stu-id="61c86-713">Parameters - mandatory</span></span>

<span data-ttu-id="61c86-714">値</span><span class="sxs-lookup"><span data-stu-id="61c86-714">value</span></span>  

### <a name="return-value---mandatory"></a><span data-ttu-id="61c86-715">戻り値 - mandatory</span><span class="sxs-lookup"><span data-stu-id="61c86-715">Return Value - mandatory</span></span>

## <a name="method-name"></a><span data-ttu-id="61c86-716">メソッド名</span><span class="sxs-lookup"><span data-stu-id="61c86-716">Method name</span></span>

<span data-ttu-id="61c86-717">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-717">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="61c86-718">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="61c86-718">Parameters - name</span></span>

<span data-ttu-id="61c86-719">値</span><span class="sxs-lookup"><span data-stu-id="61c86-719">value</span></span>  
<span data-ttu-id="61c86-720">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="61c86-720">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="61c86-721">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="61c86-721">Return Value - name</span></span>

<span data-ttu-id="61c86-722">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="61c86-722">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="61c86-723">備考 - name</span><span class="sxs-lookup"><span data-stu-id="61c86-723">Remarks - name</span></span>

<span data-ttu-id="61c86-724">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="61c86-724">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="61c86-725">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="61c86-725">It must start with a letter.</span></span>
-   <span data-ttu-id="61c86-726">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="61c86-726">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="61c86-727">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="61c86-727">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="61c86-728">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="61c86-728">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="61c86-729">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="61c86-729">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="61c86-730">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="61c86-730">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="61c86-731">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="61c86-731">Parameters - neededPermission</span></span>

<span data-ttu-id="61c86-732">値</span><span class="sxs-lookup"><span data-stu-id="61c86-732">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="61c86-733">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="61c86-733">Return Value - neededPermission</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="61c86-734">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="61c86-734">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="61c86-735">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="61c86-735">Parameters - promptrect</span></span>

<span data-ttu-id="61c86-736">値</span><span class="sxs-lookup"><span data-stu-id="61c86-736">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="61c86-737">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="61c86-737">Return Value - promptrect</span></span>

## <a name="method-replaceonlookup"></a><span data-ttu-id="61c86-738">メソッド replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="61c86-738">Method replaceOnLookup</span></span>

```xpp
public boolean replaceOnLookup([boolean value])
```

### <a name="parameters---replaceonlookup"></a><span data-ttu-id="61c86-739">パラメーター - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="61c86-739">Parameters - replaceOnLookup</span></span>

<span data-ttu-id="61c86-740">値</span><span class="sxs-lookup"><span data-stu-id="61c86-740">value</span></span>  

### <a name="return-value---replaceonlookup"></a><span data-ttu-id="61c86-741">戻り値 - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="61c86-741">Return Value - replaceOnLookup</span></span>

## <a name="method-searchafterinput"></a><span data-ttu-id="61c86-742">メソッド searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="61c86-742">Method searchAfterInput</span></span>

```xpp
public int searchAfterInput([int value])
```

### <a name="parameters---searchafterinput"></a><span data-ttu-id="61c86-743">パラメーター - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="61c86-743">Parameters - searchAfterInput</span></span>

<span data-ttu-id="61c86-744">値</span><span class="sxs-lookup"><span data-stu-id="61c86-744">value</span></span>  

### <a name="return-value---searchafterinput"></a><span data-ttu-id="61c86-745">戻り値 - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="61c86-745">Return Value - searchAfterInput</span></span>

## <a name="method-searchmode"></a><span data-ttu-id="61c86-746">メソッド searchMode</span><span class="sxs-lookup"><span data-stu-id="61c86-746">Method searchMode</span></span>

```xpp
public int searchMode([int value])
```

### <a name="parameters---searchmode"></a><span data-ttu-id="61c86-747">パラメーター - searchMode</span><span class="sxs-lookup"><span data-stu-id="61c86-747">Parameters - searchMode</span></span>

<span data-ttu-id="61c86-748">値</span><span class="sxs-lookup"><span data-stu-id="61c86-748">value</span></span>  

### <a name="return-value---searchmode"></a><span data-ttu-id="61c86-749">戻り値 - searchMode</span><span class="sxs-lookup"><span data-stu-id="61c86-749">Return Value - searchMode</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="61c86-750">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="61c86-750">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="61c86-751">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="61c86-751">Parameters - securityKey</span></span>

<span data-ttu-id="61c86-752">値</span><span class="sxs-lookup"><span data-stu-id="61c86-752">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="61c86-753">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="61c86-753">Return Value - securityKey</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="61c86-754">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="61c86-754">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="61c86-755">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="61c86-755">Parameters - showLabel</span></span>

<span data-ttu-id="61c86-756">値</span><span class="sxs-lookup"><span data-stu-id="61c86-756">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="61c86-757">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="61c86-757">Return Value - showLabel</span></span>

## <a name="method-skip"></a><span data-ttu-id="61c86-758">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="61c86-758">Method skip</span></span>

<span data-ttu-id="61c86-759">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="61c86-759">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="61c86-760">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="61c86-760">Parameters - skip</span></span>

<span data-ttu-id="61c86-761">値</span><span class="sxs-lookup"><span data-stu-id="61c86-761">value</span></span>  
<span data-ttu-id="61c86-762">コントロールの skip プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="61c86-762">The value to assign to the skip property of the control.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="61c86-763">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="61c86-763">Return Value - skip</span></span>

<span data-ttu-id="61c86-764">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="61c86-764">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-style"></a><span data-ttu-id="61c86-765">メソッド style</span><span class="sxs-lookup"><span data-stu-id="61c86-765">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="61c86-766">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="61c86-766">Parameters - style</span></span>

<span data-ttu-id="61c86-767">値</span><span class="sxs-lookup"><span data-stu-id="61c86-767">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="61c86-768">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="61c86-768">Return Value - style</span></span>

## <a name="method-timeformat"></a><span data-ttu-id="61c86-769">メソッド timeFormat</span><span class="sxs-lookup"><span data-stu-id="61c86-769">Method timeFormat</span></span>

```xpp
public int timeFormat([int value])
```

### <a name="parameters---timeformat"></a><span data-ttu-id="61c86-770">パラメーター - timeFormat</span><span class="sxs-lookup"><span data-stu-id="61c86-770">Parameters - timeFormat</span></span>

<span data-ttu-id="61c86-771">値</span><span class="sxs-lookup"><span data-stu-id="61c86-771">value</span></span>  

### <a name="return-value---timeformat"></a><span data-ttu-id="61c86-772">戻り値 - timeFormat</span><span class="sxs-lookup"><span data-stu-id="61c86-772">Return Value - timeFormat</span></span>

## <a name="method-timehours"></a><span data-ttu-id="61c86-773">メソッド timeHours</span><span class="sxs-lookup"><span data-stu-id="61c86-773">Method timeHours</span></span>

```xpp
public int timeHours([int value])
```

### <a name="parameters---timehours"></a><span data-ttu-id="61c86-774">パラメーター - timeHours</span><span class="sxs-lookup"><span data-stu-id="61c86-774">Parameters - timeHours</span></span>

<span data-ttu-id="61c86-775">値</span><span class="sxs-lookup"><span data-stu-id="61c86-775">value</span></span>  

### <a name="return-value---timehours"></a><span data-ttu-id="61c86-776">戻り値 - timeHours</span><span class="sxs-lookup"><span data-stu-id="61c86-776">Return Value - timeHours</span></span>

## <a name="method-timeminute"></a><span data-ttu-id="61c86-777">メソッド timeMinute</span><span class="sxs-lookup"><span data-stu-id="61c86-777">Method timeMinute</span></span>

```xpp
public int timeMinute([int value])
```

### <a name="parameters---timeminute"></a><span data-ttu-id="61c86-778">パラメーター - timeMinute</span><span class="sxs-lookup"><span data-stu-id="61c86-778">Parameters - timeMinute</span></span>

<span data-ttu-id="61c86-779">値</span><span class="sxs-lookup"><span data-stu-id="61c86-779">value</span></span>  

### <a name="return-value---timeminute"></a><span data-ttu-id="61c86-780">戻り値 - timeMinute</span><span class="sxs-lookup"><span data-stu-id="61c86-780">Return Value - timeMinute</span></span>

## <a name="method-timeseconds"></a><span data-ttu-id="61c86-781">メソッド timeSeconds</span><span class="sxs-lookup"><span data-stu-id="61c86-781">Method timeSeconds</span></span>

```xpp
public int timeSeconds([int value])
```

### <a name="parameters---timeseconds"></a><span data-ttu-id="61c86-782">パラメーター - timeSeconds</span><span class="sxs-lookup"><span data-stu-id="61c86-782">Parameters - timeSeconds</span></span>

<span data-ttu-id="61c86-783">値</span><span class="sxs-lookup"><span data-stu-id="61c86-783">value</span></span>  

### <a name="return-value---timeseconds"></a><span data-ttu-id="61c86-784">戻り値 - timeSeconds</span><span class="sxs-lookup"><span data-stu-id="61c86-784">Return Value - timeSeconds</span></span>

## <a name="method-timeseparator"></a><span data-ttu-id="61c86-785">メソッド timeSeparator</span><span class="sxs-lookup"><span data-stu-id="61c86-785">Method timeSeparator</span></span>

```xpp
public int timeSeparator([int value])
```

### <a name="parameters---timeseparator"></a><span data-ttu-id="61c86-786">パラメーター - timeSeparator</span><span class="sxs-lookup"><span data-stu-id="61c86-786">Parameters - timeSeparator</span></span>

<span data-ttu-id="61c86-787">値</span><span class="sxs-lookup"><span data-stu-id="61c86-787">value</span></span>  

### <a name="return-value---timeseparator"></a><span data-ttu-id="61c86-788">戻り値 - timeSeparator</span><span class="sxs-lookup"><span data-stu-id="61c86-788">Return Value - timeSeparator</span></span>

## <a name="method-top"></a><span data-ttu-id="61c86-789">メソッド top</span><span class="sxs-lookup"><span data-stu-id="61c86-789">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="61c86-790">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="61c86-790">Parameters - top</span></span>

<span data-ttu-id="61c86-791">値</span><span class="sxs-lookup"><span data-stu-id="61c86-791">value</span></span>  

<!-- -->

<span data-ttu-id="61c86-792">モード</span><span class="sxs-lookup"><span data-stu-id="61c86-792">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="61c86-793">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="61c86-793">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="61c86-794">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="61c86-794">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="61c86-795">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="61c86-795">Parameters - topMode</span></span>

<span data-ttu-id="61c86-796">値</span><span class="sxs-lookup"><span data-stu-id="61c86-796">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="61c86-797">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="61c86-797">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="61c86-798">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="61c86-798">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="61c86-799">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="61c86-799">Parameters - topValue</span></span>

<span data-ttu-id="61c86-800">値</span><span class="sxs-lookup"><span data-stu-id="61c86-800">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="61c86-801">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="61c86-801">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="61c86-802">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="61c86-802">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="61c86-803">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="61c86-803">Parameters - type</span></span>

<span data-ttu-id="61c86-804">値</span><span class="sxs-lookup"><span data-stu-id="61c86-804">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="61c86-805">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="61c86-805">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="61c86-806">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="61c86-806">Method underline</span></span>

<span data-ttu-id="61c86-807">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="61c86-807">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="61c86-808">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="61c86-808">Parameters - underline</span></span>

<span data-ttu-id="61c86-809">値</span><span class="sxs-lookup"><span data-stu-id="61c86-809">value</span></span>  
<span data-ttu-id="61c86-810">コントロールの underline プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="61c86-810">The value to assign to the underline property of the control; optional.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="61c86-811">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="61c86-811">Return Value - underline</span></span>

<span data-ttu-id="61c86-812">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="61c86-812">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-userdata"></a><span data-ttu-id="61c86-813">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="61c86-813">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="61c86-814">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="61c86-814">Parameters - userData</span></span>

<span data-ttu-id="61c86-815">値</span><span class="sxs-lookup"><span data-stu-id="61c86-815">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="61c86-816">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="61c86-816">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="61c86-817">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="61c86-817">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="61c86-818">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="61c86-818">Parameters - userDataItem</span></span>

<span data-ttu-id="61c86-819">値</span><span class="sxs-lookup"><span data-stu-id="61c86-819">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="61c86-820">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="61c86-820">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="61c86-821">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="61c86-821">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="61c86-822">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="61c86-822">Parameters - userDataItems</span></span>

<span data-ttu-id="61c86-823">値</span><span class="sxs-lookup"><span data-stu-id="61c86-823">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="61c86-824">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="61c86-824">Return Value - userDataItems</span></span>

## <a name="method-value"></a><span data-ttu-id="61c86-825">メソッド value</span><span class="sxs-lookup"><span data-stu-id="61c86-825">Method value</span></span>

```xpp
public int value([int value])
```

### <a name="parameters---value"></a><span data-ttu-id="61c86-826">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="61c86-826">Parameters - value</span></span>

<span data-ttu-id="61c86-827">値</span><span class="sxs-lookup"><span data-stu-id="61c86-827">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="61c86-828">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="61c86-828">Return Value - value</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="61c86-829">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="61c86-829">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="61c86-830">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="61c86-830">Parameters - verticalSpacing</span></span>

<span data-ttu-id="61c86-831">値</span><span class="sxs-lookup"><span data-stu-id="61c86-831">value</span></span>  

<!-- -->

<span data-ttu-id="61c86-832">モード</span><span class="sxs-lookup"><span data-stu-id="61c86-832">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="61c86-833">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="61c86-833">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="61c86-834">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="61c86-834">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="61c86-835">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="61c86-835">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="61c86-836">モード</span><span class="sxs-lookup"><span data-stu-id="61c86-836">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="61c86-837">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="61c86-837">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="61c86-838">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="61c86-838">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="61c86-839">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="61c86-839">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="61c86-840">値</span><span class="sxs-lookup"><span data-stu-id="61c86-840">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="61c86-841">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="61c86-841">Return Value - verticalSpacingValue</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="61c86-842">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="61c86-842">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="61c86-843">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="61c86-843">Parameters - viewEditMode</span></span>

<span data-ttu-id="61c86-844">値</span><span class="sxs-lookup"><span data-stu-id="61c86-844">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="61c86-845">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="61c86-845">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="61c86-846">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="61c86-846">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="61c86-847">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="61c86-847">Parameters - visible</span></span>

<span data-ttu-id="61c86-848">値</span><span class="sxs-lookup"><span data-stu-id="61c86-848">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="61c86-849">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="61c86-849">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="61c86-850">メソッド width</span><span class="sxs-lookup"><span data-stu-id="61c86-850">Method width</span></span>

<span data-ttu-id="61c86-851">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-851">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="61c86-852">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="61c86-852">Parameters - width</span></span>

<span data-ttu-id="61c86-853">値</span><span class="sxs-lookup"><span data-stu-id="61c86-853">value</span></span>  

<!-- -->

<span data-ttu-id="61c86-854">モード</span><span class="sxs-lookup"><span data-stu-id="61c86-854">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="61c86-855">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="61c86-855">Return Value - width</span></span>

<span data-ttu-id="61c86-856">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="61c86-856">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="61c86-857">備考 - width</span><span class="sxs-lookup"><span data-stu-id="61c86-857">Remarks - width</span></span>

<span data-ttu-id="61c86-858">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="61c86-858">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="61c86-859">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="61c86-859">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="61c86-860">モード。</span><span class="sxs-lookup"><span data-stu-id="61c86-860">Mode.</span></span>           | <span data-ttu-id="61c86-861">幅計算。</span><span class="sxs-lookup"><span data-stu-id="61c86-861">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="61c86-862">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="61c86-862">-1 Exact.</span></span>       | <span data-ttu-id="61c86-863">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="61c86-863">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="61c86-864">0 自動。</span><span class="sxs-lookup"><span data-stu-id="61c86-864">0 Auto.</span></span>         | <span data-ttu-id="61c86-865">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="61c86-865">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="61c86-866">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="61c86-866">1 Column width.</span></span> | <span data-ttu-id="61c86-867">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="61c86-867">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="61c86-868">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="61c86-868">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="61c86-869">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="61c86-869">Method widthMode</span></span>

<span data-ttu-id="61c86-870">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-870">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="61c86-871">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="61c86-871">Parameters - widthMode</span></span>

<span data-ttu-id="61c86-872">値</span><span class="sxs-lookup"><span data-stu-id="61c86-872">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="61c86-873">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="61c86-873">Return Value - widthMode</span></span>

<span data-ttu-id="61c86-874">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="61c86-874">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="61c86-875">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="61c86-875">Remarks - widthMode</span></span>

<span data-ttu-id="61c86-876">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="61c86-876">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="61c86-877">モード。</span><span class="sxs-lookup"><span data-stu-id="61c86-877">Mode.</span></span>         | <span data-ttu-id="61c86-878">幅計算。</span><span class="sxs-lookup"><span data-stu-id="61c86-878">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="61c86-879">正確。</span><span class="sxs-lookup"><span data-stu-id="61c86-879">Exact.</span></span>        | <span data-ttu-id="61c86-880">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="61c86-880">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="61c86-881">自動。</span><span class="sxs-lookup"><span data-stu-id="61c86-881">Auto.</span></span>         | <span data-ttu-id="61c86-882">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="61c86-882">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="61c86-883">列の幅。</span><span class="sxs-lookup"><span data-stu-id="61c86-883">Column width.</span></span> | <span data-ttu-id="61c86-884">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="61c86-884">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="61c86-885">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="61c86-885">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="61c86-886">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="61c86-886">Method widthValue</span></span>

<span data-ttu-id="61c86-887">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="61c86-887">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="61c86-888">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="61c86-888">Parameters - widthValue</span></span>

<span data-ttu-id="61c86-889">値</span><span class="sxs-lookup"><span data-stu-id="61c86-889">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="61c86-890">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="61c86-890">Return Value - widthValue</span></span>

<span data-ttu-id="61c86-891">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="61c86-891">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="61c86-892">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="61c86-892">Remarks - widthValue</span></span>

<span data-ttu-id="61c86-893">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="61c86-893">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="61c86-894">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="61c86-894">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="61c86-895">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="61c86-895">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="61c86-896">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="61c86-896">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="61c86-897">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="61c86-897">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="61c86-898">overrideObject</span><span class="sxs-lookup"><span data-stu-id="61c86-898">overrideObject</span></span>  

