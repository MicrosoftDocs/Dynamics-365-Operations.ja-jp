---
title: FormBuildGuidControl クラス
description: このトピックでは、FormBuildGroupControl クラスについて説明します。
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
ms.openlocfilehash: b904a7d4f0139c72e54f6e5bd3b3745a2446fb36
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502967"
---
# <a name="class-formbuildguidcontrol"></a><span data-ttu-id="25aa4-103">クラス FormBuildGuidControl</span><span class="sxs-lookup"><span data-stu-id="25aa4-103">Class FormBuildGuidControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildGuidControl extends FormBuildControl
```

<span data-ttu-id="25aa4-104">FormBuildGuidControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-104">The FormBuildGuidControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="25aa4-105">備考</span><span class="sxs-lookup"><span data-stu-id="25aa4-105">Remarks</span></span>

<span data-ttu-id="25aa4-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="25aa4-107">例</span><span class="sxs-lookup"><span data-stu-id="25aa4-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="25aa4-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="25aa4-108">Methods</span></span>

| <span data-ttu-id="25aa4-109">方法</span><span class="sxs-lookup"><span data-stu-id="25aa4-109">Method</span></span>                                                                                                      | <span data-ttu-id="25aa4-110">説明</span><span class="sxs-lookup"><span data-stu-id="25aa4-110">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25aa4-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="25aa4-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-112">Determines whether to align the control.</span></span>                                                                                                |
| <span data-ttu-id="25aa4-113">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-113">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="25aa4-114">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-114">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="25aa4-115">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-115">Determines whether the user can change the contents of the control.</span></span>                                                                     |
| <span data-ttu-id="25aa4-116">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-116">public int arrayIndex(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="25aa4-117">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-117">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="25aa4-118">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-118">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                      |
| <span data-ttu-id="25aa4-119">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-119">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="25aa4-120">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-120">Gets or sets the background color of the control.</span></span>                                                                                       |
| <span data-ttu-id="25aa4-121">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-121">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="25aa4-122">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-122">Determines whether the control background can be transparent.</span></span>                                                                          |
| <span data-ttu-id="25aa4-123">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-123">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="25aa4-124">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-124">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                             |
| <span data-ttu-id="25aa4-125">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-125">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="25aa4-126">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-126">Gets or sets the style of the borderline of the control.</span></span>                                                                                |
| <span data-ttu-id="25aa4-127">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-127">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="25aa4-128">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-128">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="25aa4-129">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-129">Gets or sets the character set of the font.</span></span>                                                                                             |
| <span data-ttu-id="25aa4-130">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-130">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="25aa4-131">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-131">Gets or sets the color scheme of the control.</span></span>                                                                                           |
| <span data-ttu-id="25aa4-132">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-132">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="25aa4-133">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-133">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                     |
| <span data-ttu-id="25aa4-134">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="25aa4-134">public int containerId()</span></span>                                                                                    | <span data-ttu-id="25aa4-135">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-135">Retrieves the ID of the parent container for the control.</span></span>                                                                               |
| <span data-ttu-id="25aa4-136">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-136">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="25aa4-137">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-137">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                         |
| <span data-ttu-id="25aa4-138">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-138">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="25aa4-139">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-139">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="25aa4-140">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-140">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="25aa4-141">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-141">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="25aa4-142">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-142">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                |
| <span data-ttu-id="25aa4-143">public int direction(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-143">public int direction(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="25aa4-144">public int displayHeight(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-144">public int displayHeight(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                         |
| <span data-ttu-id="25aa4-145">public AutoMode displayHeightMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-145">public AutoMode displayHeightMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                         |
| <span data-ttu-id="25aa4-146">public int displayHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-146">public int displayHeightValue(\[int value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="25aa4-147">public int displayLength(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-147">public int displayLength(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                         |
| <span data-ttu-id="25aa4-148">public AutoMode displayLengthMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-148">public AutoMode displayLengthMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                         |
| <span data-ttu-id="25aa4-149">public int displayLengthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-149">public int displayLengthValue(\[int value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="25aa4-150">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-150">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="25aa4-151">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-151">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="25aa4-152">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-152">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                       |
| <span data-ttu-id="25aa4-153">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-153">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="25aa4-154">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-154">Determines whether to enable or disable the object.</span></span>                                                                                     |
| <span data-ttu-id="25aa4-155">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-155">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                         |
| <span data-ttu-id="25aa4-156">public int fastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-156">public int fastTabSummary(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="25aa4-157">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-157">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="25aa4-158">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-158">Gets or sets the name of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="25aa4-159">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-159">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="25aa4-160">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-160">Gets or sets the size of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="25aa4-161">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-161">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="25aa4-162">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-162">Gets or sets the text color for the control to use.</span></span>                                                                                     |
| <span data-ttu-id="25aa4-163">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-163">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="25aa4-164">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-164">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="25aa4-165">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-165">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="25aa4-166">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-166">Gets or sets a calculation mode for the height of the control.</span></span>                                                                          |
| <span data-ttu-id="25aa4-167">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-167">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="25aa4-168">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-168">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="25aa4-169">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-169">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="25aa4-170">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-170">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                |
| <span data-ttu-id="25aa4-171">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-171">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="25aa4-172">public int id()</span><span class="sxs-lookup"><span data-stu-id="25aa4-172">public int id()</span></span>                                                                                             | <span data-ttu-id="25aa4-173">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-173">Retrieves the ID of the control.</span></span>                                                                                                        |
| <span data-ttu-id="25aa4-174">public int iMEMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-174">public int iMEMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="25aa4-175">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="25aa4-175">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="25aa4-176">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-176">Retrieves a value that indicates whether the control is a container control.</span></span>                                                            |
| <span data-ttu-id="25aa4-177">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-177">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="25aa4-178">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-178">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="25aa4-179">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-179">Gets or sets the label for a control.</span></span>                                                                                                   |
| <span data-ttu-id="25aa4-180">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-180">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="25aa4-181">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-181">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="25aa4-182">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-182">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="25aa4-183">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-183">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="25aa4-184">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-184">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="25aa4-185">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-185">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="25aa4-186">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-186">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="25aa4-187">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-187">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="25aa4-188">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-188">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="25aa4-189">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-189">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="25aa4-190">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-190">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                         |
| <span data-ttu-id="25aa4-191">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-191">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="25aa4-192">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-192">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                         |
| <span data-ttu-id="25aa4-193">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-193">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="25aa4-194">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-194">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="25aa4-195">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-195">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="25aa4-196">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-196">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="25aa4-197">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-197">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="25aa4-198">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-198">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="25aa4-199">public int limitText(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-199">public int limitText(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="25aa4-200">public AutoMode limitTextMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-200">public AutoMode limitTextMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                         |
| <span data-ttu-id="25aa4-201">public int limitTextValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-201">public int limitTextValue(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="25aa4-202">public int lookupButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-202">public int lookupButton(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="25aa4-203">public boolean mandatory(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-203">public boolean mandatory(\[boolean value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="25aa4-204">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-204">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="25aa4-205">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-205">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="25aa4-206">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-206">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="25aa4-207">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-207">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="25aa4-208">public boolean replaceOnLookup(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-208">public boolean replaceOnLookup(\[boolean value\])</span></span>                                                           |                                                                                                                                         |
| <span data-ttu-id="25aa4-209">public int searchAfterInput(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-209">public int searchAfterInput(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="25aa4-210">public int searchMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-210">public int searchMode(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="25aa4-211">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-211">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="25aa4-212">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-212">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="25aa4-213">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-213">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="25aa4-214">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-214">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>         |
| <span data-ttu-id="25aa4-215">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-215">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                         |
| <span data-ttu-id="25aa4-216">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-216">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="25aa4-217">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-217">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="25aa4-218">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-218">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="25aa4-219">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-219">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="25aa4-220">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-220">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="25aa4-221">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-221">Sets or returns the underline property for the text in the control.</span></span>                                                                     |
| <span data-ttu-id="25aa4-222">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-222">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="25aa4-223">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-223">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="25aa4-224">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-224">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="25aa4-225">public Guid value(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-225">public Guid value(\[Guid value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="25aa4-226">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-226">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="25aa4-227">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-227">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="25aa4-228">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-228">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="25aa4-229">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-229">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="25aa4-230">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-230">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="25aa4-231">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-231">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="25aa4-232">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-232">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="25aa4-233">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-233">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="25aa4-234">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-234">Gets or sets the calculation mode of the width of the control.</span></span>                                                                          |
| <span data-ttu-id="25aa4-235">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-235">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="25aa4-236">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-236">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="25aa4-237">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="25aa4-237">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="25aa4-238">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="25aa4-238">Method alignControl</span></span>

<span data-ttu-id="25aa4-239">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-239">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="25aa4-240">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="25aa4-240">Parameters - alignControl</span></span>

<span data-ttu-id="25aa4-241">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-241">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="25aa4-242">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="25aa4-242">Return Value - alignControl</span></span>

<span data-ttu-id="25aa4-243">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="25aa4-243">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="25aa4-244">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="25aa4-244">Remarks - alignControl</span></span>

<span data-ttu-id="25aa4-245">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-245">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="25aa4-246">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="25aa4-246">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="25aa4-247">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="25aa4-247">Parameters - alignment</span></span>

<span data-ttu-id="25aa4-248">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-248">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="25aa4-249">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="25aa4-249">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="25aa4-250">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="25aa4-250">Method allowEdit</span></span>

<span data-ttu-id="25aa4-251">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-251">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="25aa4-252">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="25aa4-252">Parameters - allowEdit</span></span>

<span data-ttu-id="25aa4-253">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-253">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="25aa4-254">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="25aa4-254">Return Value - allowEdit</span></span>

<span data-ttu-id="25aa4-255">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="25aa4-255">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="25aa4-256">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="25aa4-256">Remarks - allowEdit</span></span>

<span data-ttu-id="25aa4-257">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="25aa4-257">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="25aa4-258">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="25aa4-258">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="25aa4-259">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="25aa4-259">Parameters - arrayIndex</span></span>

<span data-ttu-id="25aa4-260">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-260">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="25aa4-261">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="25aa4-261">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="25aa4-262">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="25aa4-262">Method autoDeclaration</span></span>

<span data-ttu-id="25aa4-263">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-263">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="25aa4-264">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="25aa4-264">Parameters - autoDeclaration</span></span>

<span data-ttu-id="25aa4-265">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-265">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="25aa4-266">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="25aa4-266">Return Value - autoDeclaration</span></span>

<span data-ttu-id="25aa4-267">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="25aa4-267">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="25aa4-268">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="25aa4-268">Remarks - autoDeclaration</span></span>

<span data-ttu-id="25aa4-269">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="25aa4-269">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="25aa4-270">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="25aa4-270">Method backgroundColor</span></span>

<span data-ttu-id="25aa4-271">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-271">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="25aa4-272">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="25aa4-272">Parameters - backgroundColor</span></span>

<span data-ttu-id="25aa4-273">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-273">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="25aa4-274">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="25aa4-274">Return Value - backgroundColor</span></span>

<span data-ttu-id="25aa4-275">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="25aa4-275">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="25aa4-276">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="25aa4-276">Remarks - backgroundColor</span></span>

<span data-ttu-id="25aa4-277">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-277">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="25aa4-278">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="25aa4-278">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="25aa4-279">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="25aa4-279">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="25aa4-280">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="25aa4-280">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="25aa4-281">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="25aa4-281">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="25aa4-282">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="25aa4-282">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="25aa4-283">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="25aa4-283">Method backStyle</span></span>

<span data-ttu-id="25aa4-284">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-284">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="25aa4-285">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="25aa4-285">Parameters - backStyle</span></span>

<span data-ttu-id="25aa4-286">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-286">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="25aa4-287">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="25aa4-287">Return Value - backStyle</span></span>

<span data-ttu-id="25aa4-288">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="25aa4-288">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="25aa4-289">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="25aa4-289">Method bold</span></span>

<span data-ttu-id="25aa4-290">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-290">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="25aa4-291">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="25aa4-291">Parameters - bold</span></span>

<span data-ttu-id="25aa4-292">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-292">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="25aa4-293">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="25aa4-293">Return Value - bold</span></span>

<span data-ttu-id="25aa4-294">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="25aa4-294">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="25aa4-295">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="25aa4-295">Remarks - bold</span></span>

<span data-ttu-id="25aa4-296">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-296">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="25aa4-297">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-297">0 Use the default font weight.</span></span>
-   <span data-ttu-id="25aa4-298">1 シン。</span><span class="sxs-lookup"><span data-stu-id="25aa4-298">1 Thin.</span></span>
-   <span data-ttu-id="25aa4-299">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="25aa4-299">2 Extra-light.</span></span>
-   <span data-ttu-id="25aa4-300">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="25aa4-300">3 Light.</span></span>
-   <span data-ttu-id="25aa4-301">4 標準。</span><span class="sxs-lookup"><span data-stu-id="25aa4-301">4 Normal.</span></span>
-   <span data-ttu-id="25aa4-302">5 中。</span><span class="sxs-lookup"><span data-stu-id="25aa4-302">5 Medium.</span></span>
-   <span data-ttu-id="25aa4-303">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="25aa4-303">6 Semibold.</span></span>
-   <span data-ttu-id="25aa4-304">7 太字。</span><span class="sxs-lookup"><span data-stu-id="25aa4-304">7 Bold.</span></span>
-   <span data-ttu-id="25aa4-305">8 極太。</span><span class="sxs-lookup"><span data-stu-id="25aa4-305">8 Extra-bold.</span></span>
-   <span data-ttu-id="25aa4-306">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="25aa4-306">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="25aa4-307">メソッド border</span><span class="sxs-lookup"><span data-stu-id="25aa4-307">Method border</span></span>

<span data-ttu-id="25aa4-308">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-308">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="25aa4-309">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="25aa4-309">Parameters - border</span></span>

<span data-ttu-id="25aa4-310">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-310">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="25aa4-311">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="25aa4-311">Return Value - border</span></span>

<span data-ttu-id="25aa4-312">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="25aa4-312">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="25aa4-313">備考 - border</span><span class="sxs-lookup"><span data-stu-id="25aa4-313">Remarks - border</span></span>

<span data-ttu-id="25aa4-314">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-314">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="25aa4-315">値です。</span><span class="sxs-lookup"><span data-stu-id="25aa4-315">Value.</span></span> | <span data-ttu-id="25aa4-316">説明。</span><span class="sxs-lookup"><span data-stu-id="25aa4-316">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="25aa4-317">0</span><span class="sxs-lookup"><span data-stu-id="25aa4-317">0</span></span>      | <span data-ttu-id="25aa4-318">自動。</span><span class="sxs-lookup"><span data-stu-id="25aa4-318">Auto.</span></span>        |
| <span data-ttu-id="25aa4-319">1</span><span class="sxs-lookup"><span data-stu-id="25aa4-319">1</span></span>      | <span data-ttu-id="25aa4-320">3D。</span><span class="sxs-lookup"><span data-stu-id="25aa4-320">3D.</span></span>          |
| <span data-ttu-id="25aa4-321">2</span><span class="sxs-lookup"><span data-stu-id="25aa4-321">2</span></span>      | <span data-ttu-id="25aa4-322">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="25aa4-322">Single line.</span></span> |
| <span data-ttu-id="25aa4-323">3</span><span class="sxs-lookup"><span data-stu-id="25aa4-323">3</span></span>      | <span data-ttu-id="25aa4-324">均一。</span><span class="sxs-lookup"><span data-stu-id="25aa4-324">Flat.</span></span>        |
| <span data-ttu-id="25aa4-325">4</span><span class="sxs-lookup"><span data-stu-id="25aa4-325">4</span></span>      | <span data-ttu-id="25aa4-326">なし。</span><span class="sxs-lookup"><span data-stu-id="25aa4-326">None.</span></span>        |

## <a name="method-cachedatamethod"></a><span data-ttu-id="25aa4-327">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="25aa4-327">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="25aa4-328">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="25aa4-328">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="25aa4-329">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-329">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="25aa4-330">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="25aa4-330">Return Value - cacheDataMethod</span></span>

## <a name="method-characterset"></a><span data-ttu-id="25aa4-331">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="25aa4-331">Method characterSet</span></span>

<span data-ttu-id="25aa4-332">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-332">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="25aa4-333">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="25aa4-333">Parameters - characterSet</span></span>

<span data-ttu-id="25aa4-334">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-334">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="25aa4-335">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="25aa4-335">Return Value - characterSet</span></span>

<span data-ttu-id="25aa4-336">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="25aa4-336">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="25aa4-337">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="25aa4-337">Remarks - characterSet</span></span>

<span data-ttu-id="25aa4-338">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-338">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="25aa4-339">値です。</span><span class="sxs-lookup"><span data-stu-id="25aa4-339">Value.</span></span> | <span data-ttu-id="25aa4-340">説明。</span><span class="sxs-lookup"><span data-stu-id="25aa4-340">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="25aa4-341">0</span><span class="sxs-lookup"><span data-stu-id="25aa4-341">0</span></span>      | <span data-ttu-id="25aa4-342">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="25aa4-342">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="25aa4-343">1</span><span class="sxs-lookup"><span data-stu-id="25aa4-343">1</span></span>      | <span data-ttu-id="25aa4-344">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="25aa4-344">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="25aa4-345">2</span><span class="sxs-lookup"><span data-stu-id="25aa4-345">2</span></span>      | <span data-ttu-id="25aa4-346">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="25aa4-346">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="25aa4-347">77</span><span class="sxs-lookup"><span data-stu-id="25aa4-347">77</span></span>     | <span data-ttu-id="25aa4-348">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="25aa4-348">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="25aa4-349">128</span><span class="sxs-lookup"><span data-stu-id="25aa4-349">128</span></span>    | <span data-ttu-id="25aa4-350">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="25aa4-350">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="25aa4-351">129</span><span class="sxs-lookup"><span data-stu-id="25aa4-351">129</span></span>    | <span data-ttu-id="25aa4-352">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="25aa4-352">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="25aa4-353">134</span><span class="sxs-lookup"><span data-stu-id="25aa4-353">134</span></span>    | <span data-ttu-id="25aa4-354">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="25aa4-354">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="25aa4-355">136</span><span class="sxs-lookup"><span data-stu-id="25aa4-355">136</span></span>    | <span data-ttu-id="25aa4-356">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="25aa4-356">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="25aa4-357">161</span><span class="sxs-lookup"><span data-stu-id="25aa4-357">161</span></span>    | <span data-ttu-id="25aa4-358">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="25aa4-358">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="25aa4-359">162</span><span class="sxs-lookup"><span data-stu-id="25aa4-359">162</span></span>    | <span data-ttu-id="25aa4-360">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="25aa4-360">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="25aa4-361">163</span><span class="sxs-lookup"><span data-stu-id="25aa4-361">163</span></span>    | <span data-ttu-id="25aa4-362">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="25aa4-362">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="25aa4-363">186</span><span class="sxs-lookup"><span data-stu-id="25aa4-363">186</span></span>    | <span data-ttu-id="25aa4-364">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="25aa4-364">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="25aa4-365">204</span><span class="sxs-lookup"><span data-stu-id="25aa4-365">204</span></span>    | <span data-ttu-id="25aa4-366">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="25aa4-366">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="25aa4-367">238</span><span class="sxs-lookup"><span data-stu-id="25aa4-367">238</span></span>    | <span data-ttu-id="25aa4-368">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="25aa4-368">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="25aa4-369">255</span><span class="sxs-lookup"><span data-stu-id="25aa4-369">255</span></span>    | <span data-ttu-id="25aa4-370">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="25aa4-370">OEM\_CHARSET</span></span>         |

<span data-ttu-id="25aa4-371">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="25aa4-371">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="25aa4-372">値です。</span><span class="sxs-lookup"><span data-stu-id="25aa4-372">Value.</span></span> | <span data-ttu-id="25aa4-373">説明。</span><span class="sxs-lookup"><span data-stu-id="25aa4-373">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="25aa4-374">130</span><span class="sxs-lookup"><span data-stu-id="25aa4-374">130</span></span>    | <span data-ttu-id="25aa4-375">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="25aa4-375">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="25aa4-376">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="25aa4-376">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="25aa4-377">値です。</span><span class="sxs-lookup"><span data-stu-id="25aa4-377">Value.</span></span> | <span data-ttu-id="25aa4-378">説明。</span><span class="sxs-lookup"><span data-stu-id="25aa4-378">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="25aa4-379">177</span><span class="sxs-lookup"><span data-stu-id="25aa4-379">177</span></span>    | <span data-ttu-id="25aa4-380">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="25aa4-380">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="25aa4-381">178</span><span class="sxs-lookup"><span data-stu-id="25aa4-381">178</span></span>    | <span data-ttu-id="25aa4-382">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="25aa4-382">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="25aa4-383">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="25aa4-383">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="25aa4-384">値です。</span><span class="sxs-lookup"><span data-stu-id="25aa4-384">Value.</span></span> | <span data-ttu-id="25aa4-385">説明。</span><span class="sxs-lookup"><span data-stu-id="25aa4-385">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="25aa4-386">222</span><span class="sxs-lookup"><span data-stu-id="25aa4-386">222</span></span>    | <span data-ttu-id="25aa4-387">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="25aa4-387">THAI\_CHARSET</span></span> |

<span data-ttu-id="25aa4-388">既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-388">The default character set is set to a value, depending on the current system locale.</span></span> <span data-ttu-id="25aa4-389">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-389">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="25aa4-390">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="25aa4-390">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="25aa4-391">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="25aa4-391">Method colorScheme</span></span>

<span data-ttu-id="25aa4-392">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-392">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="25aa4-393">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="25aa4-393">Parameters - colorScheme</span></span>

<span data-ttu-id="25aa4-394">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-394">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="25aa4-395">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="25aa4-395">Return Value - colorScheme</span></span>

<span data-ttu-id="25aa4-396">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="25aa4-396">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="25aa4-397">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="25aa4-397">Remarks - colorScheme</span></span>

<span data-ttu-id="25aa4-398">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-398">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="25aa4-399">値です。</span><span class="sxs-lookup"><span data-stu-id="25aa4-399">Value.</span></span> | <span data-ttu-id="25aa4-400">スタイル。</span><span class="sxs-lookup"><span data-stu-id="25aa4-400">Style.</span></span>                         |
|--------|--------------------------------|
| <span data-ttu-id="25aa4-401">0</span><span class="sxs-lookup"><span data-stu-id="25aa4-401">0</span></span>      | <span data-ttu-id="25aa4-402">既定。</span><span class="sxs-lookup"><span data-stu-id="25aa4-402">Default.</span></span>                       |
| <span data-ttu-id="25aa4-403">1</span><span class="sxs-lookup"><span data-stu-id="25aa4-403">1</span></span>      | <span data-ttu-id="25aa4-404">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="25aa4-404">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="25aa4-405">2</span><span class="sxs-lookup"><span data-stu-id="25aa4-405">2</span></span>      | <span data-ttu-id="25aa4-406">真の配色。</span><span class="sxs-lookup"><span data-stu-id="25aa4-406">The true-color scheme.</span></span>         |

## <a name="method-configurationkey"></a><span data-ttu-id="25aa4-407">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="25aa4-407">Method configurationKey</span></span>

<span data-ttu-id="25aa4-408">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-408">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="25aa4-409">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="25aa4-409">Parameters - configurationKey</span></span>

<span data-ttu-id="25aa4-410">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-410">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="25aa4-411">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="25aa4-411">Return Value - configurationKey</span></span>

<span data-ttu-id="25aa4-412">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="25aa4-412">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="25aa4-413">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="25aa4-413">Remarks - configurationKey</span></span>

<span data-ttu-id="25aa4-414">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-414">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="25aa4-415">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="25aa4-415">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="25aa4-416">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="25aa4-416">Method containerId</span></span>

<span data-ttu-id="25aa4-417">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-417">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="25aa4-418">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="25aa4-418">Return Value - containerId</span></span>

<span data-ttu-id="25aa4-419">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="25aa4-419">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="25aa4-420">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="25aa4-420">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="25aa4-421">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="25aa4-421">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="25aa4-422">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-422">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="25aa4-423">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="25aa4-423">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="25aa4-424">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="25aa4-424">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="25aa4-425">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="25aa4-425">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="25aa4-426">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-426">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="25aa4-427">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="25aa4-427">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="25aa4-428">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="25aa4-428">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="25aa4-429">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="25aa4-429">Parameters - dataField</span></span>

<span data-ttu-id="25aa4-430">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-430">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="25aa4-431">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="25aa4-431">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="25aa4-432">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="25aa4-432">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="25aa4-433">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="25aa4-433">Parameters - dataMethod</span></span>

<span data-ttu-id="25aa4-434">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-434">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="25aa4-435">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="25aa4-435">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="25aa4-436">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="25aa4-436">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="25aa4-437">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="25aa4-437">Parameters - dataRelationPath</span></span>

<span data-ttu-id="25aa4-438">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-438">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="25aa4-439">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="25aa4-439">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="25aa4-440">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="25aa4-440">Method dataSource</span></span>

<span data-ttu-id="25aa4-441">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-441">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="25aa4-442">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="25aa4-442">Parameters - dataSource</span></span>

<span data-ttu-id="25aa4-443">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-443">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="25aa4-444">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="25aa4-444">Return Value - dataSource</span></span>

<span data-ttu-id="25aa4-445">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="25aa4-445">The identifier of the data source that will be used.</span></span>

## <a name="method-direction"></a><span data-ttu-id="25aa4-446">メソッド direction</span><span class="sxs-lookup"><span data-stu-id="25aa4-446">Method direction</span></span>

```xpp
public int direction([int value])
```

### <a name="parameters---direction"></a><span data-ttu-id="25aa4-447">パラメーター - direction</span><span class="sxs-lookup"><span data-stu-id="25aa4-447">Parameters - direction</span></span>

<span data-ttu-id="25aa4-448">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-448">value</span></span>  

### <a name="return-value---direction"></a><span data-ttu-id="25aa4-449">戻り値 - direction</span><span class="sxs-lookup"><span data-stu-id="25aa4-449">Return Value - direction</span></span>

## <a name="method-displayheight"></a><span data-ttu-id="25aa4-450">メソッド displayHeight</span><span class="sxs-lookup"><span data-stu-id="25aa4-450">Method displayHeight</span></span>

```xpp
public int displayHeight([int value], [AutoMode mode])
```

### <a name="parameters---displayheight"></a><span data-ttu-id="25aa4-451">パラメーター - displayHeight</span><span class="sxs-lookup"><span data-stu-id="25aa4-451">Parameters - displayHeight</span></span>

<span data-ttu-id="25aa4-452">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-452">value</span></span>  

<!-- -->

<span data-ttu-id="25aa4-453">モード</span><span class="sxs-lookup"><span data-stu-id="25aa4-453">mode</span></span>  

### <a name="return-value---displayheight"></a><span data-ttu-id="25aa4-454">戻り値 - displayHeight</span><span class="sxs-lookup"><span data-stu-id="25aa4-454">Return Value - displayHeight</span></span>

## <a name="method-displayheightmode"></a><span data-ttu-id="25aa4-455">メソッド displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-455">Method displayHeightMode</span></span>

```xpp
public AutoMode displayHeightMode([AutoMode mode])
```

### <a name="parameters---displayheightmode"></a><span data-ttu-id="25aa4-456">パラメーター - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-456">Parameters - displayHeightMode</span></span>

<span data-ttu-id="25aa4-457">モード</span><span class="sxs-lookup"><span data-stu-id="25aa4-457">mode</span></span>  

### <a name="return-value---displayheightmode"></a><span data-ttu-id="25aa4-458">戻り値 - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-458">Return Value - displayHeightMode</span></span>

## <a name="method-displayheightvalue"></a><span data-ttu-id="25aa4-459">メソッド displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-459">Method displayHeightValue</span></span>

```xpp
public int displayHeightValue([int value])
```

### <a name="parameters---displayheightvalue"></a><span data-ttu-id="25aa4-460">パラメーター - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-460">Parameters - displayHeightValue</span></span>

<span data-ttu-id="25aa4-461">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-461">value</span></span>  

### <a name="return-value---displayheightvalue"></a><span data-ttu-id="25aa4-462">戻り値 - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-462">Return Value - displayHeightValue</span></span>

## <a name="method-displaylength"></a><span data-ttu-id="25aa4-463">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="25aa4-463">Method displayLength</span></span>

```xpp
public int displayLength([int value], [AutoMode mode])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="25aa4-464">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="25aa4-464">Parameters - displayLength</span></span>

<span data-ttu-id="25aa4-465">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-465">value</span></span>  

<!-- -->

<span data-ttu-id="25aa4-466">モード</span><span class="sxs-lookup"><span data-stu-id="25aa4-466">mode</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="25aa4-467">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="25aa4-467">Return Value - displayLength</span></span>

## <a name="method-displaylengthmode"></a><span data-ttu-id="25aa4-468">メソッド displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-468">Method displayLengthMode</span></span>

```xpp
public AutoMode displayLengthMode([AutoMode mode])
```

### <a name="parameters---displaylengthmode"></a><span data-ttu-id="25aa4-469">パラメーター - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-469">Parameters - displayLengthMode</span></span>

<span data-ttu-id="25aa4-470">モード</span><span class="sxs-lookup"><span data-stu-id="25aa4-470">mode</span></span>  

### <a name="return-value---displaylengthmode"></a><span data-ttu-id="25aa4-471">戻り値 - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-471">Return Value - displayLengthMode</span></span>

## <a name="method-displaylengthvalue"></a><span data-ttu-id="25aa4-472">メソッド displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-472">Method displayLengthValue</span></span>

```xpp
public int displayLengthValue([int value])
```

### <a name="parameters---displaylengthvalue"></a><span data-ttu-id="25aa4-473">パラメーター - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-473">Parameters - displayLengthValue</span></span>

<span data-ttu-id="25aa4-474">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-474">value</span></span>  

### <a name="return-value---displaylengthvalue"></a><span data-ttu-id="25aa4-475">戻り値 - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-475">Return Value - displayLengthValue</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="25aa4-476">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="25aa4-476">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="25aa4-477">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="25aa4-477">Parameters - displayTarget</span></span>

<span data-ttu-id="25aa4-478">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-478">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="25aa4-479">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="25aa4-479">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="25aa4-480">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="25aa4-480">Method dragDrop</span></span>

<span data-ttu-id="25aa4-481">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-481">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="25aa4-482">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="25aa4-482">Parameters - dragDrop</span></span>

<span data-ttu-id="25aa4-483">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-483">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="25aa4-484">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="25aa4-484">Return Value - dragDrop</span></span>

<span data-ttu-id="25aa4-485">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="25aa4-485">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="25aa4-486">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="25aa4-486">Method enabled</span></span>

<span data-ttu-id="25aa4-487">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-487">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="25aa4-488">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="25aa4-488">Parameters - enabled</span></span>

<span data-ttu-id="25aa4-489">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-489">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="25aa4-490">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="25aa4-490">Return Value - enabled</span></span>

<span data-ttu-id="25aa4-491">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="25aa4-491">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="25aa4-492">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="25aa4-492">Remarks - enabled</span></span>

<span data-ttu-id="25aa4-493">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-493">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="25aa4-494">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-494">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="25aa4-495">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-495">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="25aa4-496">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="25aa4-496">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="25aa4-497">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="25aa4-497">Parameters - extendedDataType</span></span>

<span data-ttu-id="25aa4-498">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-498">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="25aa4-499">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="25aa4-499">Return Value - extendedDataType</span></span>

## <a name="method-fasttabsummary"></a><span data-ttu-id="25aa4-500">メソッド fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="25aa4-500">Method fastTabSummary</span></span>

```xpp
public int fastTabSummary([int value])
```

### <a name="parameters---fasttabsummary"></a><span data-ttu-id="25aa4-501">パラメーター - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="25aa4-501">Parameters - fastTabSummary</span></span>

<span data-ttu-id="25aa4-502">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-502">value</span></span>  

### <a name="return-value---fasttabsummary"></a><span data-ttu-id="25aa4-503">戻り値 - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="25aa4-503">Return Value - fastTabSummary</span></span>

## <a name="method-font"></a><span data-ttu-id="25aa4-504">メソッド font</span><span class="sxs-lookup"><span data-stu-id="25aa4-504">Method font</span></span>

<span data-ttu-id="25aa4-505">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-505">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="25aa4-506">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="25aa4-506">Parameters - font</span></span>

<span data-ttu-id="25aa4-507">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-507">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="25aa4-508">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="25aa4-508">Return Value - font</span></span>

<span data-ttu-id="25aa4-509">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="25aa4-509">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="25aa4-510">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="25aa4-510">Method fontSize</span></span>

<span data-ttu-id="25aa4-511">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-511">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="25aa4-512">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="25aa4-512">Parameters - fontSize</span></span>

<span data-ttu-id="25aa4-513">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-513">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="25aa4-514">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="25aa4-514">Return Value - fontSize</span></span>

<span data-ttu-id="25aa4-515">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="25aa4-515">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="25aa4-516">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="25aa4-516">Method foregroundColor</span></span>

<span data-ttu-id="25aa4-517">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-517">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="25aa4-518">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="25aa4-518">Parameters - foregroundColor</span></span>

<span data-ttu-id="25aa4-519">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-519">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="25aa4-520">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="25aa4-520">Return Value - foregroundColor</span></span>

<span data-ttu-id="25aa4-521">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="25aa4-521">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="25aa4-522">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="25aa4-522">Remarks - foregroundColor</span></span>

<span data-ttu-id="25aa4-523">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-523">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="25aa4-524">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="25aa4-524">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="25aa4-525">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="25aa4-525">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="25aa4-526">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="25aa4-526">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="25aa4-527">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="25aa4-527">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="25aa4-528">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="25aa4-528">The maximum value for a single byte is 255.</span></span>

## <a name="method-height"></a><span data-ttu-id="25aa4-529">メソッド height</span><span class="sxs-lookup"><span data-stu-id="25aa4-529">Method height</span></span>

<span data-ttu-id="25aa4-530">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-530">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="25aa4-531">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="25aa4-531">Parameters - height</span></span>

<span data-ttu-id="25aa4-532">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-532">value</span></span>  

<!-- -->

<span data-ttu-id="25aa4-533">モード</span><span class="sxs-lookup"><span data-stu-id="25aa4-533">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="25aa4-534">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="25aa4-534">Return Value - height</span></span>

<span data-ttu-id="25aa4-535">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="25aa4-535">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="25aa4-536">備考 - height</span><span class="sxs-lookup"><span data-stu-id="25aa4-536">Remarks - height</span></span>

<span data-ttu-id="25aa4-537">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-537">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="25aa4-538">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="25aa4-538">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="25aa4-539">モード。</span><span class="sxs-lookup"><span data-stu-id="25aa4-539">Mode.</span></span>            | <span data-ttu-id="25aa4-540">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="25aa4-540">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="25aa4-541">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="25aa4-541">-1 Exact.</span></span>        | <span data-ttu-id="25aa4-542">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-542">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="25aa4-543">0 自動。</span><span class="sxs-lookup"><span data-stu-id="25aa4-543">0 Auto.</span></span>          | <span data-ttu-id="25aa4-544">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-544">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="25aa4-545">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="25aa4-545">1 Column height.</span></span> | <span data-ttu-id="25aa4-546">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="25aa4-546">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="25aa4-547">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-547">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="25aa4-548">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-548">Method heightMode</span></span>

<span data-ttu-id="25aa4-549">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-549">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="25aa4-550">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-550">Parameters - heightMode</span></span>

<span data-ttu-id="25aa4-551">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-551">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="25aa4-552">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-552">Return Value - heightMode</span></span>

<span data-ttu-id="25aa4-553">計算モード。</span><span class="sxs-lookup"><span data-stu-id="25aa4-553">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="25aa4-554">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-554">Remarks - heightMode</span></span>

<span data-ttu-id="25aa4-555">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="25aa4-555">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="25aa4-556">モード。</span><span class="sxs-lookup"><span data-stu-id="25aa4-556">Mode.</span></span>          | <span data-ttu-id="25aa4-557">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="25aa4-557">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="25aa4-558">正確。</span><span class="sxs-lookup"><span data-stu-id="25aa4-558">Exact.</span></span>         | <span data-ttu-id="25aa4-559">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-559">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="25aa4-560">自動。</span><span class="sxs-lookup"><span data-stu-id="25aa4-560">Auto.</span></span>          | <span data-ttu-id="25aa4-561">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-561">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="25aa4-562">列の高さ</span><span class="sxs-lookup"><span data-stu-id="25aa4-562">Column height.</span></span> | <span data-ttu-id="25aa4-563">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="25aa4-563">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="25aa4-564">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="25aa4-564">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="25aa4-565">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-565">Method heightValue</span></span>

<span data-ttu-id="25aa4-566">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-566">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="25aa4-567">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-567">Parameters - heightValue</span></span>

<span data-ttu-id="25aa4-568">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-568">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="25aa4-569">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-569">Return Value - heightValue</span></span>

<span data-ttu-id="25aa4-570">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="25aa4-570">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="25aa4-571">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-571">Remarks - heightValue</span></span>

<span data-ttu-id="25aa4-572">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="25aa4-572">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="25aa4-573">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="25aa4-573">Method helpText</span></span>

<span data-ttu-id="25aa4-574">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-574">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="25aa4-575">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="25aa4-575">Parameters - helpText</span></span>

<span data-ttu-id="25aa4-576">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-576">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="25aa4-577">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="25aa4-577">Return Value - helpText</span></span>

<span data-ttu-id="25aa4-578">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="25aa4-578">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="25aa4-579">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="25aa4-579">Remarks - helpText</span></span>

<span data-ttu-id="25aa4-580">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-580">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="25aa4-581">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="25aa4-581">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="25aa4-582">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="25aa4-582">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="25aa4-583">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="25aa4-583">Parameters - hierarchyParent</span></span>

<span data-ttu-id="25aa4-584">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-584">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="25aa4-585">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="25aa4-585">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="25aa4-586">メソッド id</span><span class="sxs-lookup"><span data-stu-id="25aa4-586">Method id</span></span>

<span data-ttu-id="25aa4-587">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-587">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="25aa4-588">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="25aa4-588">Return Value - id</span></span>

<span data-ttu-id="25aa4-589">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="25aa4-589">The ID of the control.</span></span>

## <a name="method-imemode"></a><span data-ttu-id="25aa4-590">メソッド iMEMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-590">Method iMEMode</span></span>

```xpp
public int iMEMode([int value])
```

### <a name="parameters---imemode"></a><span data-ttu-id="25aa4-591">パラメーター - iMEMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-591">Parameters - iMEMode</span></span>

<span data-ttu-id="25aa4-592">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-592">value</span></span>  

### <a name="return-value---imemode"></a><span data-ttu-id="25aa4-593">戻り値 - iMEMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-593">Return Value - iMEMode</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="25aa4-594">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="25aa4-594">Method isContainer</span></span>

<span data-ttu-id="25aa4-595">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-595">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="25aa4-596">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="25aa4-596">Return Value - isContainer</span></span>

<span data-ttu-id="25aa4-597">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="25aa4-597">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-italic"></a><span data-ttu-id="25aa4-598">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="25aa4-598">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="25aa4-599">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="25aa4-599">Parameters - italic</span></span>

<span data-ttu-id="25aa4-600">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-600">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="25aa4-601">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="25aa4-601">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="25aa4-602">メソッド label</span><span class="sxs-lookup"><span data-stu-id="25aa4-602">Method label</span></span>

<span data-ttu-id="25aa4-603">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-603">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="25aa4-604">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="25aa4-604">Parameters - label</span></span>

<span data-ttu-id="25aa4-605">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-605">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="25aa4-606">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="25aa4-606">Return Value - label</span></span>

<span data-ttu-id="25aa4-607">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="25aa4-607">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="25aa4-608">備考 - label</span><span class="sxs-lookup"><span data-stu-id="25aa4-608">Remarks - label</span></span>

<span data-ttu-id="25aa4-609">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-609">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="25aa4-610">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="25aa4-610">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="25aa4-611">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="25aa4-611">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="25aa4-612">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="25aa4-612">Parameters - labelAlignment</span></span>

<span data-ttu-id="25aa4-613">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-613">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="25aa4-614">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="25aa4-614">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="25aa4-615">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="25aa4-615">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="25aa4-616">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="25aa4-616">Parameters - labelBold</span></span>

<span data-ttu-id="25aa4-617">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-617">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="25aa4-618">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="25aa4-618">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="25aa4-619">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="25aa4-619">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="25aa4-620">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="25aa4-620">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="25aa4-621">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-621">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="25aa4-622">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="25aa4-622">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="25aa4-623">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="25aa4-623">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="25aa4-624">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="25aa4-624">Parameters - labelFont</span></span>

<span data-ttu-id="25aa4-625">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-625">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="25aa4-626">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="25aa4-626">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="25aa4-627">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="25aa4-627">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="25aa4-628">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="25aa4-628">Parameters - labelFontSize</span></span>

<span data-ttu-id="25aa4-629">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-629">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="25aa4-630">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="25aa4-630">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="25aa4-631">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="25aa4-631">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="25aa4-632">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="25aa4-632">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="25aa4-633">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-633">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="25aa4-634">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="25aa4-634">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="25aa4-635">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="25aa4-635">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="25aa4-636">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="25aa4-636">Parameters - labelGuide</span></span>

<span data-ttu-id="25aa4-637">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-637">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="25aa4-638">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="25aa4-638">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="25aa4-639">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="25aa4-639">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="25aa4-640">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="25aa4-640">Parameters - labelHeight</span></span>

<span data-ttu-id="25aa4-641">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-641">value</span></span>  

<!-- -->

<span data-ttu-id="25aa4-642">モード</span><span class="sxs-lookup"><span data-stu-id="25aa4-642">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="25aa4-643">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="25aa4-643">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="25aa4-644">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-644">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="25aa4-645">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-645">Parameters - labelHeightMode</span></span>

<span data-ttu-id="25aa4-646">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-646">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="25aa4-647">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-647">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="25aa4-648">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-648">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="25aa4-649">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-649">Parameters - labelHeightValue</span></span>

<span data-ttu-id="25aa4-650">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-650">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="25aa4-651">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-651">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="25aa4-652">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="25aa4-652">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="25aa4-653">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="25aa4-653">Parameters - labelItalic</span></span>

<span data-ttu-id="25aa4-654">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-654">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="25aa4-655">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="25aa4-655">Return Value - labelItalic</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="25aa4-656">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="25aa4-656">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="25aa4-657">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="25aa4-657">Parameters - labelPosition</span></span>

<span data-ttu-id="25aa4-658">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-658">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="25aa4-659">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="25aa4-659">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="25aa4-660">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="25aa4-660">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="25aa4-661">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="25aa4-661">Parameters - labelUnderline</span></span>

<span data-ttu-id="25aa4-662">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-662">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="25aa4-663">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="25aa4-663">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="25aa4-664">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="25aa4-664">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="25aa4-665">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="25aa4-665">Parameters - labelWidth</span></span>

<span data-ttu-id="25aa4-666">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-666">value</span></span>  

<!-- -->

<span data-ttu-id="25aa4-667">モード</span><span class="sxs-lookup"><span data-stu-id="25aa4-667">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="25aa4-668">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="25aa4-668">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="25aa4-669">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-669">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="25aa4-670">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-670">Parameters - labelWidthMode</span></span>

<span data-ttu-id="25aa4-671">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-671">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="25aa4-672">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-672">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="25aa4-673">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-673">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="25aa4-674">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-674">Parameters - labelWidthValue</span></span>

<span data-ttu-id="25aa4-675">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-675">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="25aa4-676">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-676">Return Value - labelWidthValue</span></span>

## <a name="method-left"></a><span data-ttu-id="25aa4-677">メソッド left</span><span class="sxs-lookup"><span data-stu-id="25aa4-677">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="25aa4-678">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="25aa4-678">Parameters - left</span></span>

<span data-ttu-id="25aa4-679">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-679">value</span></span>  

<!-- -->

<span data-ttu-id="25aa4-680">モード</span><span class="sxs-lookup"><span data-stu-id="25aa4-680">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="25aa4-681">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="25aa4-681">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="25aa4-682">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-682">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="25aa4-683">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-683">Parameters - leftMode</span></span>

<span data-ttu-id="25aa4-684">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-684">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="25aa4-685">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-685">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="25aa4-686">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-686">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="25aa4-687">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-687">Parameters - leftValue</span></span>

<span data-ttu-id="25aa4-688">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-688">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="25aa4-689">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-689">Return Value - leftValue</span></span>

## <a name="method-limittext"></a><span data-ttu-id="25aa4-690">メソッド limitText</span><span class="sxs-lookup"><span data-stu-id="25aa4-690">Method limitText</span></span>

```xpp
public int limitText([int value], [AutoMode mode])
```

### <a name="parameters---limittext"></a><span data-ttu-id="25aa4-691">パラメーター - limitText</span><span class="sxs-lookup"><span data-stu-id="25aa4-691">Parameters - limitText</span></span>

<span data-ttu-id="25aa4-692">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-692">value</span></span>  

<!-- -->

<span data-ttu-id="25aa4-693">モード</span><span class="sxs-lookup"><span data-stu-id="25aa4-693">mode</span></span>  

### <a name="return-value---limittext"></a><span data-ttu-id="25aa4-694">戻り値 - limitText</span><span class="sxs-lookup"><span data-stu-id="25aa4-694">Return Value - limitText</span></span>

## <a name="method-limittextmode"></a><span data-ttu-id="25aa4-695">メソッド limitTextMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-695">Method limitTextMode</span></span>

```xpp
public AutoMode limitTextMode([AutoMode mode])
```

### <a name="parameters---limittextmode"></a><span data-ttu-id="25aa4-696">パラメーター - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-696">Parameters - limitTextMode</span></span>

<span data-ttu-id="25aa4-697">モード</span><span class="sxs-lookup"><span data-stu-id="25aa4-697">mode</span></span>  

### <a name="return-value---limittextmode"></a><span data-ttu-id="25aa4-698">戻り値 - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-698">Return Value - limitTextMode</span></span>

## <a name="method-limittextvalue"></a><span data-ttu-id="25aa4-699">メソッド limitTextValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-699">Method limitTextValue</span></span>

```xpp
public int limitTextValue([int value])
```

### <a name="parameters---limittextvalue"></a><span data-ttu-id="25aa4-700">パラメーター - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-700">Parameters - limitTextValue</span></span>

<span data-ttu-id="25aa4-701">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-701">value</span></span>  

### <a name="return-value---limittextvalue"></a><span data-ttu-id="25aa4-702">戻り値 - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-702">Return Value - limitTextValue</span></span>

## <a name="method-lookupbutton"></a><span data-ttu-id="25aa4-703">メソッド lookupButton</span><span class="sxs-lookup"><span data-stu-id="25aa4-703">Method lookupButton</span></span>

```xpp
public int lookupButton([int value])
```

### <a name="parameters---lookupbutton"></a><span data-ttu-id="25aa4-704">パラメーター - lookupButton</span><span class="sxs-lookup"><span data-stu-id="25aa4-704">Parameters - lookupButton</span></span>

<span data-ttu-id="25aa4-705">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-705">value</span></span>  

### <a name="return-value---lookupbutton"></a><span data-ttu-id="25aa4-706">戻り値 - lookupButton</span><span class="sxs-lookup"><span data-stu-id="25aa4-706">Return Value - lookupButton</span></span>

## <a name="method-mandatory"></a><span data-ttu-id="25aa4-707">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="25aa4-707">Method mandatory</span></span>

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a><span data-ttu-id="25aa4-708">パラメーター - mandatory</span><span class="sxs-lookup"><span data-stu-id="25aa4-708">Parameters - mandatory</span></span>

<span data-ttu-id="25aa4-709">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-709">value</span></span>  

### <a name="return-value---mandatory"></a><span data-ttu-id="25aa4-710">戻り値 - mandatory</span><span class="sxs-lookup"><span data-stu-id="25aa4-710">Return Value - mandatory</span></span>

## <a name="method-name"></a><span data-ttu-id="25aa4-711">メソッド名</span><span class="sxs-lookup"><span data-stu-id="25aa4-711">Method name</span></span>

<span data-ttu-id="25aa4-712">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-712">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="25aa4-713">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="25aa4-713">Parameters - name</span></span>

<span data-ttu-id="25aa4-714">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-714">value</span></span>  
<span data-ttu-id="25aa4-715">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="25aa4-715">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="25aa4-716">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="25aa4-716">Return Value - name</span></span>

<span data-ttu-id="25aa4-717">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="25aa4-717">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="25aa4-718">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="25aa4-718">Remarks - name</span></span>

<span data-ttu-id="25aa4-719">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="25aa4-719">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="25aa4-720">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="25aa4-720">It must start with a letter.</span></span>
-   <span data-ttu-id="25aa4-721">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="25aa4-721">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="25aa4-722">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-722">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="25aa4-723">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="25aa4-723">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="25aa4-724">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="25aa4-724">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="25aa4-725">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="25aa4-725">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="25aa4-726">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="25aa4-726">Parameters - neededPermission</span></span>

<span data-ttu-id="25aa4-727">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-727">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="25aa4-728">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="25aa4-728">Return Value - neededPermission</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="25aa4-729">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="25aa4-729">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="25aa4-730">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="25aa4-730">Parameters - promptrect</span></span>

<span data-ttu-id="25aa4-731">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-731">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="25aa4-732">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="25aa4-732">Return Value - promptrect</span></span>

## <a name="method-replaceonlookup"></a><span data-ttu-id="25aa4-733">メソッド replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="25aa4-733">Method replaceOnLookup</span></span>

```xpp
public boolean replaceOnLookup([boolean value])
```

### <a name="parameters---replaceonlookup"></a><span data-ttu-id="25aa4-734">パラメーター - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="25aa4-734">Parameters - replaceOnLookup</span></span>

<span data-ttu-id="25aa4-735">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-735">value</span></span>  

### <a name="return-value---replaceonlookup"></a><span data-ttu-id="25aa4-736">戻り値 - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="25aa4-736">Return Value - replaceOnLookup</span></span>

## <a name="method-searchafterinput"></a><span data-ttu-id="25aa4-737">メソッド searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="25aa4-737">Method searchAfterInput</span></span>

```xpp
public int searchAfterInput([int value])
```

### <a name="parameters---searchafterinput"></a><span data-ttu-id="25aa4-738">パラメーター - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="25aa4-738">Parameters - searchAfterInput</span></span>

<span data-ttu-id="25aa4-739">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-739">value</span></span>  

### <a name="return-value---searchafterinput"></a><span data-ttu-id="25aa4-740">戻り値 - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="25aa4-740">Return Value - searchAfterInput</span></span>

## <a name="method-searchmode"></a><span data-ttu-id="25aa4-741">メソッド searchMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-741">Method searchMode</span></span>

```xpp
public int searchMode([int value])
```

### <a name="parameters---searchmode"></a><span data-ttu-id="25aa4-742">パラメーター - searchMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-742">Parameters - searchMode</span></span>

<span data-ttu-id="25aa4-743">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-743">value</span></span>  

### <a name="return-value---searchmode"></a><span data-ttu-id="25aa4-744">戻り値 - searchMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-744">Return Value - searchMode</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="25aa4-745">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="25aa4-745">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="25aa4-746">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="25aa4-746">Parameters - securityKey</span></span>

<span data-ttu-id="25aa4-747">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-747">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="25aa4-748">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="25aa4-748">Return Value - securityKey</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="25aa4-749">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="25aa4-749">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="25aa4-750">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="25aa4-750">Parameters - showLabel</span></span>

<span data-ttu-id="25aa4-751">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-751">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="25aa4-752">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="25aa4-752">Return Value - showLabel</span></span>

## <a name="method-skip"></a><span data-ttu-id="25aa4-753">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="25aa4-753">Method skip</span></span>

<span data-ttu-id="25aa4-754">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-754">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="25aa4-755">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="25aa4-755">Parameters - skip</span></span>

<span data-ttu-id="25aa4-756">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-756">value</span></span>  
<span data-ttu-id="25aa4-757">コントロールの skip プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="25aa4-757">The value to assign to the skip property of the control.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="25aa4-758">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="25aa4-758">Return Value - skip</span></span>

<span data-ttu-id="25aa4-759">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="25aa4-759">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-style"></a><span data-ttu-id="25aa4-760">メソッド style</span><span class="sxs-lookup"><span data-stu-id="25aa4-760">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="25aa4-761">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="25aa4-761">Parameters - style</span></span>

<span data-ttu-id="25aa4-762">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-762">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="25aa4-763">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="25aa4-763">Return Value - style</span></span>

## <a name="method-top"></a><span data-ttu-id="25aa4-764">メソッド top</span><span class="sxs-lookup"><span data-stu-id="25aa4-764">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="25aa4-765">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="25aa4-765">Parameters - top</span></span>

<span data-ttu-id="25aa4-766">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-766">value</span></span>  

<!-- -->

<span data-ttu-id="25aa4-767">モード</span><span class="sxs-lookup"><span data-stu-id="25aa4-767">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="25aa4-768">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="25aa4-768">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="25aa4-769">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-769">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="25aa4-770">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-770">Parameters - topMode</span></span>

<span data-ttu-id="25aa4-771">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-771">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="25aa4-772">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-772">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="25aa4-773">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-773">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="25aa4-774">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-774">Parameters - topValue</span></span>

<span data-ttu-id="25aa4-775">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-775">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="25aa4-776">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-776">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="25aa4-777">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="25aa4-777">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="25aa4-778">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="25aa4-778">Parameters - type</span></span>

<span data-ttu-id="25aa4-779">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-779">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="25aa4-780">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="25aa4-780">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="25aa4-781">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="25aa4-781">Method underline</span></span>

<span data-ttu-id="25aa4-782">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-782">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="25aa4-783">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="25aa4-783">Parameters - underline</span></span>

<span data-ttu-id="25aa4-784">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-784">value</span></span>  
<span data-ttu-id="25aa4-785">コントロールの underline プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="25aa4-785">The value to assign to the underline property of the control.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="25aa4-786">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="25aa4-786">Return Value - underline</span></span>

<span data-ttu-id="25aa4-787">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="25aa4-787">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-userdata"></a><span data-ttu-id="25aa4-788">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="25aa4-788">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="25aa4-789">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="25aa4-789">Parameters - userData</span></span>

<span data-ttu-id="25aa4-790">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-790">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="25aa4-791">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="25aa4-791">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="25aa4-792">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="25aa4-792">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="25aa4-793">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="25aa4-793">Parameters - userDataItem</span></span>

<span data-ttu-id="25aa4-794">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-794">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="25aa4-795">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="25aa4-795">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="25aa4-796">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="25aa4-796">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="25aa4-797">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="25aa4-797">Parameters - userDataItems</span></span>

<span data-ttu-id="25aa4-798">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-798">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="25aa4-799">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="25aa4-799">Return Value - userDataItems</span></span>

## <a name="method-value"></a><span data-ttu-id="25aa4-800">メソッド value</span><span class="sxs-lookup"><span data-stu-id="25aa4-800">Method value</span></span>

```xpp
public Guid value([Guid value])
```

### <a name="parameters---value"></a><span data-ttu-id="25aa4-801">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="25aa4-801">Parameters - value</span></span>

<span data-ttu-id="25aa4-802">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-802">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="25aa4-803">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="25aa4-803">Return Value - value</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="25aa4-804">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="25aa4-804">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="25aa4-805">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="25aa4-805">Parameters - verticalSpacing</span></span>

<span data-ttu-id="25aa4-806">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-806">value</span></span>  

<!-- -->

<span data-ttu-id="25aa4-807">モード</span><span class="sxs-lookup"><span data-stu-id="25aa4-807">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="25aa4-808">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="25aa4-808">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="25aa4-809">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-809">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="25aa4-810">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-810">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="25aa4-811">モード</span><span class="sxs-lookup"><span data-stu-id="25aa4-811">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="25aa4-812">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-812">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="25aa4-813">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-813">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="25aa4-814">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-814">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="25aa4-815">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-815">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="25aa4-816">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-816">Return Value - verticalSpacingValue</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="25aa4-817">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-817">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="25aa4-818">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-818">Parameters - viewEditMode</span></span>

<span data-ttu-id="25aa4-819">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-819">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="25aa4-820">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-820">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="25aa4-821">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="25aa4-821">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="25aa4-822">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="25aa4-822">Parameters - visible</span></span>

<span data-ttu-id="25aa4-823">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-823">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="25aa4-824">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="25aa4-824">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="25aa4-825">メソッド width</span><span class="sxs-lookup"><span data-stu-id="25aa4-825">Method width</span></span>

<span data-ttu-id="25aa4-826">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-826">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="25aa4-827">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="25aa4-827">Parameters - width</span></span>

<span data-ttu-id="25aa4-828">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-828">value</span></span>  

<!-- -->

<span data-ttu-id="25aa4-829">モード</span><span class="sxs-lookup"><span data-stu-id="25aa4-829">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="25aa4-830">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="25aa4-830">Return Value - width</span></span>

<span data-ttu-id="25aa4-831">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="25aa4-831">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="25aa4-832">備考 - width</span><span class="sxs-lookup"><span data-stu-id="25aa4-832">Remarks - width</span></span>

<span data-ttu-id="25aa4-833">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-833">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="25aa4-834">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="25aa4-834">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="25aa4-835">モード。</span><span class="sxs-lookup"><span data-stu-id="25aa4-835">Mode.</span></span>           | <span data-ttu-id="25aa4-836">幅計算。</span><span class="sxs-lookup"><span data-stu-id="25aa4-836">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="25aa4-837">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="25aa4-837">-1 Exact.</span></span>       | <span data-ttu-id="25aa4-838">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-838">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="25aa4-839">0 自動。</span><span class="sxs-lookup"><span data-stu-id="25aa4-839">0 Auto.</span></span>         | <span data-ttu-id="25aa4-840">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-840">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="25aa4-841">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="25aa4-841">1 Column width.</span></span> | <span data-ttu-id="25aa4-842">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="25aa4-842">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="25aa4-843">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-843">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="25aa4-844">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-844">Method widthMode</span></span>

<span data-ttu-id="25aa4-845">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-845">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="25aa4-846">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-846">Parameters - widthMode</span></span>

<span data-ttu-id="25aa4-847">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-847">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="25aa4-848">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-848">Return Value - widthMode</span></span>

<span data-ttu-id="25aa4-849">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="25aa4-849">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="25aa4-850">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="25aa4-850">Remarks - widthMode</span></span>

<span data-ttu-id="25aa4-851">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="25aa4-851">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="25aa4-852">モード。</span><span class="sxs-lookup"><span data-stu-id="25aa4-852">Mode.</span></span>         | <span data-ttu-id="25aa4-853">幅計算。</span><span class="sxs-lookup"><span data-stu-id="25aa4-853">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="25aa4-854">正確。</span><span class="sxs-lookup"><span data-stu-id="25aa4-854">Exact.</span></span>        | <span data-ttu-id="25aa4-855">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-855">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="25aa4-856">自動。</span><span class="sxs-lookup"><span data-stu-id="25aa4-856">Auto.</span></span>         | <span data-ttu-id="25aa4-857">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="25aa4-857">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="25aa4-858">列の幅。</span><span class="sxs-lookup"><span data-stu-id="25aa4-858">Column width.</span></span> | <span data-ttu-id="25aa4-859">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="25aa4-859">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="25aa4-860">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="25aa4-860">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="25aa4-861">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-861">Method widthValue</span></span>

<span data-ttu-id="25aa4-862">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-862">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="25aa4-863">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-863">Parameters - widthValue</span></span>

<span data-ttu-id="25aa4-864">値</span><span class="sxs-lookup"><span data-stu-id="25aa4-864">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="25aa4-865">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-865">Return Value - widthValue</span></span>

<span data-ttu-id="25aa4-866">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="25aa4-866">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="25aa4-867">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="25aa4-867">Remarks - widthValue</span></span>

<span data-ttu-id="25aa4-868">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="25aa4-868">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="25aa4-869">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="25aa4-869">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="25aa4-870">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="25aa4-870">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="25aa4-871">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="25aa4-871">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="25aa4-872">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="25aa4-872">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="25aa4-873">overrideObject</span><span class="sxs-lookup"><span data-stu-id="25aa4-873">overrideObject</span></span>  

