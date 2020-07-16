---
title: FormBuildIntControl クラス
description: このトピックでは、FormBuildIntControl クラスについて説明します。
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
ms.openlocfilehash: c60043714048b27301bb70527ef0268c76e129de
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502964"
---
# <a name="class-formbuildintcontrol"></a><span data-ttu-id="dce85-103">クラス FormBuildIntControl</span><span class="sxs-lookup"><span data-stu-id="dce85-103">Class FormBuildIntControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildIntControl extends FormBuildControl
```

<span data-ttu-id="dce85-104">FormBuildIntControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="dce85-104">The FormBuildIntControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="dce85-105">備考</span><span class="sxs-lookup"><span data-stu-id="dce85-105">Remarks</span></span>

<span data-ttu-id="dce85-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dce85-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="dce85-107">例</span><span class="sxs-lookup"><span data-stu-id="dce85-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="dce85-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="dce85-108">Methods</span></span>

| <span data-ttu-id="dce85-109">方法</span><span class="sxs-lookup"><span data-stu-id="dce85-109">Method</span></span>                                                                                                      | <span data-ttu-id="dce85-110">説明</span><span class="sxs-lookup"><span data-stu-id="dce85-110">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dce85-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="dce85-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-112">Determines whether to align the control.</span></span>                                                                                                |
| <span data-ttu-id="dce85-113">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-113">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="dce85-114">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-114">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="dce85-115">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-115">Determines whether the user can change the contents of the control.</span></span>                                                                     |
| <span data-ttu-id="dce85-116">public int allowNegative(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-116">public int allowNegative(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="dce85-117">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-117">public int arrayIndex(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="dce85-118">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-118">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="dce85-119">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-119">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                      |
| <span data-ttu-id="dce85-120">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-120">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="dce85-121">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-121">Gets or sets the background color of the control.</span></span>                                                                                       |
| <span data-ttu-id="dce85-122">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-122">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="dce85-123">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-123">Determines whether the control background can be transparent.</span></span>                                                                          |
| <span data-ttu-id="dce85-124">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-124">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="dce85-125">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-125">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                             |
| <span data-ttu-id="dce85-126">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-126">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="dce85-127">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-127">Gets or sets the style of the borderline of the control.</span></span>                                                                                |
| <span data-ttu-id="dce85-128">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-128">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="dce85-129">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-129">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="dce85-130">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-130">Gets or sets the character set of the font.</span></span>                                                                                             |
| <span data-ttu-id="dce85-131">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-131">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="dce85-132">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-132">Gets or sets the color scheme of the control.</span></span>                                                                                           |
| <span data-ttu-id="dce85-133">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-133">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="dce85-134">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-134">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                     |
| <span data-ttu-id="dce85-135">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="dce85-135">public int containerId()</span></span>                                                                                    | <span data-ttu-id="dce85-136">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="dce85-136">Retrieves the ID of the parent container for the control.</span></span>                                                                               |
| <span data-ttu-id="dce85-137">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-137">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="dce85-138">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-138">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                         |
| <span data-ttu-id="dce85-139">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-139">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="dce85-140">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-140">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="dce85-141">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-141">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="dce85-142">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-142">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="dce85-143">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-143">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                |
| <span data-ttu-id="dce85-144">public int direction(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-144">public int direction(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="dce85-145">public int displaceNegative(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="dce85-145">public int displaceNegative(\[int value\], \[AutoMode mode\])</span></span>                                               |                                                                                                                                         |
| <span data-ttu-id="dce85-146">public AutoMode displaceNegativeMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="dce85-146">public AutoMode displaceNegativeMode(\[AutoMode mode\])</span></span>                                                     |                                                                                                                                         |
| <span data-ttu-id="dce85-147">public int displaceNegativeValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-147">public int displaceNegativeValue(\[int value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="dce85-148">public int displayHeight(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="dce85-148">public int displayHeight(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                         |
| <span data-ttu-id="dce85-149">public AutoMode displayHeightMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="dce85-149">public AutoMode displayHeightMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                         |
| <span data-ttu-id="dce85-150">public int displayHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-150">public int displayHeightValue(\[int value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="dce85-151">public int displayLength(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="dce85-151">public int displayLength(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                         |
| <span data-ttu-id="dce85-152">public AutoMode displayLengthMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="dce85-152">public AutoMode displayLengthMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                         |
| <span data-ttu-id="dce85-153">public int displayLengthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-153">public int displayLengthValue(\[int value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="dce85-154">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-154">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="dce85-155">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-155">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="dce85-156">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-156">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                       |
| <span data-ttu-id="dce85-157">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-157">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="dce85-158">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-158">Determines whether to enable or disable the object.</span></span>                                                                                     |
| <span data-ttu-id="dce85-159">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-159">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                         |
| <span data-ttu-id="dce85-160">public int fastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-160">public int fastTabSummary(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="dce85-161">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-161">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="dce85-162">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-162">Gets or sets the name of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="dce85-163">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-163">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="dce85-164">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-164">Gets or sets the size of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="dce85-165">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-165">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="dce85-166">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-166">Gets or sets the text color for the control to use.</span></span>                                                                                     |
| <span data-ttu-id="dce85-167">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="dce85-167">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="dce85-168">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-168">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="dce85-169">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-169">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="dce85-170">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-170">Gets or sets a calculation mode for the height of the control.</span></span>                                                                          |
| <span data-ttu-id="dce85-171">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-171">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="dce85-172">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-172">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="dce85-173">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-173">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="dce85-174">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-174">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                |
| <span data-ttu-id="dce85-175">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-175">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="dce85-176">public int id()</span><span class="sxs-lookup"><span data-stu-id="dce85-176">public int id()</span></span>                                                                                             | <span data-ttu-id="dce85-177">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="dce85-177">Retrieves the ID of the control.</span></span>                                                                                                        |
| <span data-ttu-id="dce85-178">public int iMEMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-178">public int iMEMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="dce85-179">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="dce85-179">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="dce85-180">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="dce85-180">Retrieves a value that indicates whether the control is a container control.</span></span>                                                            |
| <span data-ttu-id="dce85-181">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-181">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="dce85-182">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-182">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="dce85-183">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-183">Gets or sets the label for a control.</span></span>                                                                                                   |
| <span data-ttu-id="dce85-184">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-184">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="dce85-185">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-185">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="dce85-186">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-186">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="dce85-187">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-187">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="dce85-188">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-188">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="dce85-189">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-189">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="dce85-190">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-190">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="dce85-191">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="dce85-191">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="dce85-192">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-192">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="dce85-193">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-193">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="dce85-194">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-194">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                         |
| <span data-ttu-id="dce85-195">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-195">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="dce85-196">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-196">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                         |
| <span data-ttu-id="dce85-197">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="dce85-197">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="dce85-198">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-198">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="dce85-199">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-199">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="dce85-200">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="dce85-200">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="dce85-201">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-201">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="dce85-202">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-202">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="dce85-203">public int limitText(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="dce85-203">public int limitText(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="dce85-204">public AutoMode limitTextMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="dce85-204">public AutoMode limitTextMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                         |
| <span data-ttu-id="dce85-205">public int limitTextValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-205">public int limitTextValue(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="dce85-206">public int lookupButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-206">public int lookupButton(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="dce85-207">public boolean mandatory(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-207">public boolean mandatory(\[boolean value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="dce85-208">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-208">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="dce85-209">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-209">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="dce85-210">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-210">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="dce85-211">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-211">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="dce85-212">public boolean replaceOnLookup(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-212">public boolean replaceOnLookup(\[boolean value\])</span></span>                                                           |                                                                                                                                         |
| <span data-ttu-id="dce85-213">public int rotateSign(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-213">public int rotateSign(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="dce85-214">public int searchAfterInput(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-214">public int searchAfterInput(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="dce85-215">public int searchMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-215">public int searchMode(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="dce85-216">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-216">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="dce85-217">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-217">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="dce85-218">public int showZero(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-218">public int showZero(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="dce85-219">public int signDisplay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-219">public int signDisplay(\[int value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="dce85-220">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-220">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="dce85-221">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="dce85-221">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>         |
| <span data-ttu-id="dce85-222">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-222">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                         |
| <span data-ttu-id="dce85-223">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="dce85-223">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="dce85-224">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-224">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="dce85-225">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-225">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="dce85-226">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-226">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="dce85-227">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-227">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="dce85-228">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="dce85-228">Sets or returns the underline property for the text in the control.</span></span>                                                                     |
| <span data-ttu-id="dce85-229">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-229">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="dce85-230">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-230">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="dce85-231">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-231">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="dce85-232">public int value(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-232">public int value(\[int value\])</span></span>                                                                             |                                                                                                                                         |
| <span data-ttu-id="dce85-233">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="dce85-233">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="dce85-234">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="dce85-234">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="dce85-235">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-235">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="dce85-236">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-236">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="dce85-237">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-237">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="dce85-238">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="dce85-238">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="dce85-239">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-239">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="dce85-240">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-240">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="dce85-241">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-241">Gets or sets the calculation mode of the width of the control.</span></span>                                                                          |
| <span data-ttu-id="dce85-242">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="dce85-242">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="dce85-243">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-243">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="dce85-244">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="dce85-244">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="dce85-245">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="dce85-245">Method alignControl</span></span>

<span data-ttu-id="dce85-246">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-246">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="dce85-247">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="dce85-247">Parameters - alignControl</span></span>

<span data-ttu-id="dce85-248">値</span><span class="sxs-lookup"><span data-stu-id="dce85-248">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="dce85-249">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="dce85-249">Return Value - alignControl</span></span>

<span data-ttu-id="dce85-250">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="dce85-250">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="dce85-251">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="dce85-251">Remarks - alignControl</span></span>

<span data-ttu-id="dce85-252">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="dce85-252">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="dce85-253">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="dce85-253">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="dce85-254">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="dce85-254">Parameters - alignment</span></span>

<span data-ttu-id="dce85-255">値</span><span class="sxs-lookup"><span data-stu-id="dce85-255">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="dce85-256">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="dce85-256">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="dce85-257">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="dce85-257">Method allowEdit</span></span>

<span data-ttu-id="dce85-258">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-258">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="dce85-259">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="dce85-259">Parameters - allowEdit</span></span>

<span data-ttu-id="dce85-260">値</span><span class="sxs-lookup"><span data-stu-id="dce85-260">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="dce85-261">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="dce85-261">Return Value - allowEdit</span></span>

<span data-ttu-id="dce85-262">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="dce85-262">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="dce85-263">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="dce85-263">Remarks - allowEdit</span></span>

<span data-ttu-id="dce85-264">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="dce85-264">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-allownegative"></a><span data-ttu-id="dce85-265">メソッド allowNegative</span><span class="sxs-lookup"><span data-stu-id="dce85-265">Method allowNegative</span></span>

```xpp
public int allowNegative([int value])
```

### <a name="parameters---allownegative"></a><span data-ttu-id="dce85-266">パラメーター - allowNegative</span><span class="sxs-lookup"><span data-stu-id="dce85-266">Parameters - allowNegative</span></span>

<span data-ttu-id="dce85-267">値</span><span class="sxs-lookup"><span data-stu-id="dce85-267">value</span></span>  

### <a name="return-value---allownegative"></a><span data-ttu-id="dce85-268">戻り値 - allowNegative</span><span class="sxs-lookup"><span data-stu-id="dce85-268">Return Value - allowNegative</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="dce85-269">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="dce85-269">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="dce85-270">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="dce85-270">Parameters - arrayIndex</span></span>

<span data-ttu-id="dce85-271">値</span><span class="sxs-lookup"><span data-stu-id="dce85-271">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="dce85-272">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="dce85-272">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="dce85-273">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="dce85-273">Method autoDeclaration</span></span>

<span data-ttu-id="dce85-274">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-274">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="dce85-275">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="dce85-275">Parameters - autoDeclaration</span></span>

<span data-ttu-id="dce85-276">値</span><span class="sxs-lookup"><span data-stu-id="dce85-276">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="dce85-277">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="dce85-277">Return Value - autoDeclaration</span></span>

<span data-ttu-id="dce85-278">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="dce85-278">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="dce85-279">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="dce85-279">Remarks - autoDeclaration</span></span>

<span data-ttu-id="dce85-280">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="dce85-280">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="dce85-281">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="dce85-281">Method backgroundColor</span></span>

<span data-ttu-id="dce85-282">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-282">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="dce85-283">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="dce85-283">Parameters - backgroundColor</span></span>

<span data-ttu-id="dce85-284">値</span><span class="sxs-lookup"><span data-stu-id="dce85-284">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="dce85-285">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="dce85-285">Return Value - backgroundColor</span></span>

<span data-ttu-id="dce85-286">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="dce85-286">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="dce85-287">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="dce85-287">Remarks - backgroundColor</span></span>

<span data-ttu-id="dce85-288">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="dce85-288">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="dce85-289">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dce85-289">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="dce85-290">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="dce85-290">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="dce85-291">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="dce85-291">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="dce85-292">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="dce85-292">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="dce85-293">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="dce85-293">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="dce85-294">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="dce85-294">Method backStyle</span></span>

<span data-ttu-id="dce85-295">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-295">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="dce85-296">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="dce85-296">Parameters - backStyle</span></span>

<span data-ttu-id="dce85-297">値</span><span class="sxs-lookup"><span data-stu-id="dce85-297">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="dce85-298">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="dce85-298">Return Value - backStyle</span></span>

<span data-ttu-id="dce85-299">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="dce85-299">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="dce85-300">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="dce85-300">Method bold</span></span>

<span data-ttu-id="dce85-301">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-301">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="dce85-302">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="dce85-302">Parameters - bold</span></span>

<span data-ttu-id="dce85-303">値</span><span class="sxs-lookup"><span data-stu-id="dce85-303">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="dce85-304">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="dce85-304">Return Value - bold</span></span>

<span data-ttu-id="dce85-305">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="dce85-305">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="dce85-306">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="dce85-306">Remarks - bold</span></span>

<span data-ttu-id="dce85-307">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="dce85-307">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="dce85-308">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="dce85-308">0 Use the default font weight.</span></span>
-   <span data-ttu-id="dce85-309">1 シン。</span><span class="sxs-lookup"><span data-stu-id="dce85-309">1 Thin.</span></span>
-   <span data-ttu-id="dce85-310">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="dce85-310">2 Extra-light.</span></span>
-   <span data-ttu-id="dce85-311">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="dce85-311">3 Light.</span></span>
-   <span data-ttu-id="dce85-312">4 標準。</span><span class="sxs-lookup"><span data-stu-id="dce85-312">4 Normal.</span></span>
-   <span data-ttu-id="dce85-313">5 中。</span><span class="sxs-lookup"><span data-stu-id="dce85-313">5 Medium.</span></span>
-   <span data-ttu-id="dce85-314">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="dce85-314">6 Semibold.</span></span>
-   <span data-ttu-id="dce85-315">7 太字。</span><span class="sxs-lookup"><span data-stu-id="dce85-315">7 Bold.</span></span>
-   <span data-ttu-id="dce85-316">8 極太。</span><span class="sxs-lookup"><span data-stu-id="dce85-316">8 Extra-bold.</span></span>
-   <span data-ttu-id="dce85-317">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="dce85-317">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="dce85-318">メソッド border</span><span class="sxs-lookup"><span data-stu-id="dce85-318">Method border</span></span>

<span data-ttu-id="dce85-319">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-319">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="dce85-320">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="dce85-320">Parameters - border</span></span>

<span data-ttu-id="dce85-321">値</span><span class="sxs-lookup"><span data-stu-id="dce85-321">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="dce85-322">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="dce85-322">Return Value - border</span></span>

<span data-ttu-id="dce85-323">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="dce85-323">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="dce85-324">備考 - border</span><span class="sxs-lookup"><span data-stu-id="dce85-324">Remarks - border</span></span>

<span data-ttu-id="dce85-325">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="dce85-325">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="dce85-326">値です。</span><span class="sxs-lookup"><span data-stu-id="dce85-326">Value.</span></span> | <span data-ttu-id="dce85-327">説明。</span><span class="sxs-lookup"><span data-stu-id="dce85-327">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="dce85-328">0</span><span class="sxs-lookup"><span data-stu-id="dce85-328">0</span></span>      | <span data-ttu-id="dce85-329">自動。</span><span class="sxs-lookup"><span data-stu-id="dce85-329">Auto.</span></span>        |
| <span data-ttu-id="dce85-330">1</span><span class="sxs-lookup"><span data-stu-id="dce85-330">1</span></span>      | <span data-ttu-id="dce85-331">3D。</span><span class="sxs-lookup"><span data-stu-id="dce85-331">3D.</span></span>          |
| <span data-ttu-id="dce85-332">2</span><span class="sxs-lookup"><span data-stu-id="dce85-332">2</span></span>      | <span data-ttu-id="dce85-333">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="dce85-333">Single line.</span></span> |
| <span data-ttu-id="dce85-334">3</span><span class="sxs-lookup"><span data-stu-id="dce85-334">3</span></span>      | <span data-ttu-id="dce85-335">均一。</span><span class="sxs-lookup"><span data-stu-id="dce85-335">Flat.</span></span>        |
| <span data-ttu-id="dce85-336">4</span><span class="sxs-lookup"><span data-stu-id="dce85-336">4</span></span>      | <span data-ttu-id="dce85-337">なし。</span><span class="sxs-lookup"><span data-stu-id="dce85-337">None.</span></span>        |

## <a name="method-cachedatamethod"></a><span data-ttu-id="dce85-338">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="dce85-338">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="dce85-339">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="dce85-339">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="dce85-340">値</span><span class="sxs-lookup"><span data-stu-id="dce85-340">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="dce85-341">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="dce85-341">Return Value - cacheDataMethod</span></span>

## <a name="method-characterset"></a><span data-ttu-id="dce85-342">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="dce85-342">Method characterSet</span></span>

<span data-ttu-id="dce85-343">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-343">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="dce85-344">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="dce85-344">Parameters - characterSet</span></span>

<span data-ttu-id="dce85-345">値</span><span class="sxs-lookup"><span data-stu-id="dce85-345">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="dce85-346">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="dce85-346">Return Value - characterSet</span></span>

<span data-ttu-id="dce85-347">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="dce85-347">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="dce85-348">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="dce85-348">Remarks - characterSet</span></span>

<span data-ttu-id="dce85-349">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="dce85-349">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="dce85-350">値です。</span><span class="sxs-lookup"><span data-stu-id="dce85-350">Value.</span></span> | <span data-ttu-id="dce85-351">説明。</span><span class="sxs-lookup"><span data-stu-id="dce85-351">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="dce85-352">0</span><span class="sxs-lookup"><span data-stu-id="dce85-352">0</span></span>      | <span data-ttu-id="dce85-353">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dce85-353">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="dce85-354">1</span><span class="sxs-lookup"><span data-stu-id="dce85-354">1</span></span>      | <span data-ttu-id="dce85-355">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dce85-355">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="dce85-356">2</span><span class="sxs-lookup"><span data-stu-id="dce85-356">2</span></span>      | <span data-ttu-id="dce85-357">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dce85-357">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="dce85-358">77</span><span class="sxs-lookup"><span data-stu-id="dce85-358">77</span></span>     | <span data-ttu-id="dce85-359">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dce85-359">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="dce85-360">128</span><span class="sxs-lookup"><span data-stu-id="dce85-360">128</span></span>    | <span data-ttu-id="dce85-361">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dce85-361">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="dce85-362">129</span><span class="sxs-lookup"><span data-stu-id="dce85-362">129</span></span>    | <span data-ttu-id="dce85-363">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dce85-363">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="dce85-364">134</span><span class="sxs-lookup"><span data-stu-id="dce85-364">134</span></span>    | <span data-ttu-id="dce85-365">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dce85-365">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="dce85-366">136</span><span class="sxs-lookup"><span data-stu-id="dce85-366">136</span></span>    | <span data-ttu-id="dce85-367">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dce85-367">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="dce85-368">161</span><span class="sxs-lookup"><span data-stu-id="dce85-368">161</span></span>    | <span data-ttu-id="dce85-369">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dce85-369">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="dce85-370">162</span><span class="sxs-lookup"><span data-stu-id="dce85-370">162</span></span>    | <span data-ttu-id="dce85-371">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dce85-371">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="dce85-372">163</span><span class="sxs-lookup"><span data-stu-id="dce85-372">163</span></span>    | <span data-ttu-id="dce85-373">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dce85-373">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="dce85-374">186</span><span class="sxs-lookup"><span data-stu-id="dce85-374">186</span></span>    | <span data-ttu-id="dce85-375">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dce85-375">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="dce85-376">204</span><span class="sxs-lookup"><span data-stu-id="dce85-376">204</span></span>    | <span data-ttu-id="dce85-377">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dce85-377">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="dce85-378">238</span><span class="sxs-lookup"><span data-stu-id="dce85-378">238</span></span>    | <span data-ttu-id="dce85-379">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dce85-379">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="dce85-380">255</span><span class="sxs-lookup"><span data-stu-id="dce85-380">255</span></span>    | <span data-ttu-id="dce85-381">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dce85-381">OEM\_CHARSET</span></span>         |

<span data-ttu-id="dce85-382">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="dce85-382">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="dce85-383">値です。</span><span class="sxs-lookup"><span data-stu-id="dce85-383">Value.</span></span> | <span data-ttu-id="dce85-384">説明。</span><span class="sxs-lookup"><span data-stu-id="dce85-384">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="dce85-385">130</span><span class="sxs-lookup"><span data-stu-id="dce85-385">130</span></span>    | <span data-ttu-id="dce85-386">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dce85-386">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="dce85-387">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="dce85-387">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="dce85-388">値です。</span><span class="sxs-lookup"><span data-stu-id="dce85-388">Value.</span></span> | <span data-ttu-id="dce85-389">説明。</span><span class="sxs-lookup"><span data-stu-id="dce85-389">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="dce85-390">177</span><span class="sxs-lookup"><span data-stu-id="dce85-390">177</span></span>    | <span data-ttu-id="dce85-391">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dce85-391">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="dce85-392">178</span><span class="sxs-lookup"><span data-stu-id="dce85-392">178</span></span>    | <span data-ttu-id="dce85-393">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dce85-393">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="dce85-394">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="dce85-394">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="dce85-395">値です。</span><span class="sxs-lookup"><span data-stu-id="dce85-395">Value.</span></span> | <span data-ttu-id="dce85-396">説明。</span><span class="sxs-lookup"><span data-stu-id="dce85-396">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="dce85-397">222</span><span class="sxs-lookup"><span data-stu-id="dce85-397">222</span></span>    | <span data-ttu-id="dce85-398">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="dce85-398">THAI\_CHARSET</span></span> |

<span data-ttu-id="dce85-399">既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="dce85-399">The default character set is set to a value, depending on the current system locale.</span></span> <span data-ttu-id="dce85-400">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="dce85-400">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="dce85-401">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dce85-401">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="dce85-402">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="dce85-402">Method colorScheme</span></span>

<span data-ttu-id="dce85-403">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-403">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="dce85-404">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="dce85-404">Parameters - colorScheme</span></span>

<span data-ttu-id="dce85-405">値</span><span class="sxs-lookup"><span data-stu-id="dce85-405">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="dce85-406">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="dce85-406">Return Value - colorScheme</span></span>

<span data-ttu-id="dce85-407">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="dce85-407">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="dce85-408">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="dce85-408">Remarks - colorScheme</span></span>

<span data-ttu-id="dce85-409">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="dce85-409">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="dce85-410">値です。</span><span class="sxs-lookup"><span data-stu-id="dce85-410">Value.</span></span> | <span data-ttu-id="dce85-411">スタイル。</span><span class="sxs-lookup"><span data-stu-id="dce85-411">Style.</span></span>                         |
|--------|--------------------------------|
| <span data-ttu-id="dce85-412">0</span><span class="sxs-lookup"><span data-stu-id="dce85-412">0</span></span>      | <span data-ttu-id="dce85-413">既定。</span><span class="sxs-lookup"><span data-stu-id="dce85-413">Default.</span></span>                       |
| <span data-ttu-id="dce85-414">1</span><span class="sxs-lookup"><span data-stu-id="dce85-414">1</span></span>      | <span data-ttu-id="dce85-415">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="dce85-415">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="dce85-416">2</span><span class="sxs-lookup"><span data-stu-id="dce85-416">2</span></span>      | <span data-ttu-id="dce85-417">真の配色。</span><span class="sxs-lookup"><span data-stu-id="dce85-417">The true color scheme.</span></span>         |

## <a name="method-configurationkey"></a><span data-ttu-id="dce85-418">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="dce85-418">Method configurationKey</span></span>

<span data-ttu-id="dce85-419">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-419">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="dce85-420">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="dce85-420">Parameters - configurationKey</span></span>

<span data-ttu-id="dce85-421">値</span><span class="sxs-lookup"><span data-stu-id="dce85-421">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="dce85-422">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="dce85-422">Return Value - configurationKey</span></span>

<span data-ttu-id="dce85-423">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="dce85-423">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="dce85-424">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="dce85-424">Remarks - configurationKey</span></span>

<span data-ttu-id="dce85-425">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="dce85-425">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="dce85-426">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="dce85-426">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="dce85-427">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="dce85-427">Method containerId</span></span>

<span data-ttu-id="dce85-428">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="dce85-428">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="dce85-429">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="dce85-429">Return Value - containerId</span></span>

<span data-ttu-id="dce85-430">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="dce85-430">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="dce85-431">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="dce85-431">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="dce85-432">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="dce85-432">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="dce85-433">値</span><span class="sxs-lookup"><span data-stu-id="dce85-433">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="dce85-434">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="dce85-434">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="dce85-435">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="dce85-435">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="dce85-436">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="dce85-436">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="dce85-437">値</span><span class="sxs-lookup"><span data-stu-id="dce85-437">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="dce85-438">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="dce85-438">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="dce85-439">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="dce85-439">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="dce85-440">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="dce85-440">Parameters - dataField</span></span>

<span data-ttu-id="dce85-441">値</span><span class="sxs-lookup"><span data-stu-id="dce85-441">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="dce85-442">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="dce85-442">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="dce85-443">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="dce85-443">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="dce85-444">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="dce85-444">Parameters - dataMethod</span></span>

<span data-ttu-id="dce85-445">値</span><span class="sxs-lookup"><span data-stu-id="dce85-445">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="dce85-446">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="dce85-446">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="dce85-447">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="dce85-447">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="dce85-448">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="dce85-448">Parameters - dataRelationPath</span></span>

<span data-ttu-id="dce85-449">値</span><span class="sxs-lookup"><span data-stu-id="dce85-449">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="dce85-450">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="dce85-450">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="dce85-451">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="dce85-451">Method dataSource</span></span>

<span data-ttu-id="dce85-452">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-452">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="dce85-453">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="dce85-453">Parameters - dataSource</span></span>

<span data-ttu-id="dce85-454">値</span><span class="sxs-lookup"><span data-stu-id="dce85-454">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="dce85-455">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="dce85-455">Return Value - dataSource</span></span>

<span data-ttu-id="dce85-456">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="dce85-456">The identifier of the data source that will be used.</span></span>

## <a name="method-direction"></a><span data-ttu-id="dce85-457">メソッド direction</span><span class="sxs-lookup"><span data-stu-id="dce85-457">Method direction</span></span>

```xpp
public int direction([int value])
```

### <a name="parameters---direction"></a><span data-ttu-id="dce85-458">パラメーター - direction</span><span class="sxs-lookup"><span data-stu-id="dce85-458">Parameters - direction</span></span>

<span data-ttu-id="dce85-459">値</span><span class="sxs-lookup"><span data-stu-id="dce85-459">value</span></span>  

### <a name="return-value---direction"></a><span data-ttu-id="dce85-460">戻り値 - direction</span><span class="sxs-lookup"><span data-stu-id="dce85-460">Return Value - direction</span></span>

## <a name="method-displacenegative"></a><span data-ttu-id="dce85-461">メソッド displaceNegative</span><span class="sxs-lookup"><span data-stu-id="dce85-461">Method displaceNegative</span></span>

```xpp
public int displaceNegative([int value], [AutoMode mode])
```

### <a name="parameters---displacenegative"></a><span data-ttu-id="dce85-462">パラメーター - displaceNegative</span><span class="sxs-lookup"><span data-stu-id="dce85-462">Parameters - displaceNegative</span></span>

<span data-ttu-id="dce85-463">値</span><span class="sxs-lookup"><span data-stu-id="dce85-463">value</span></span>  

<!-- -->

<span data-ttu-id="dce85-464">モード</span><span class="sxs-lookup"><span data-stu-id="dce85-464">mode</span></span>  

### <a name="return-value---displacenegative"></a><span data-ttu-id="dce85-465">戻り値 - displaceNegative</span><span class="sxs-lookup"><span data-stu-id="dce85-465">Return Value - displaceNegative</span></span>

## <a name="method-displacenegativemode"></a><span data-ttu-id="dce85-466">メソッド displaceNegativeMode</span><span class="sxs-lookup"><span data-stu-id="dce85-466">Method displaceNegativeMode</span></span>

```xpp
public AutoMode displaceNegativeMode([AutoMode mode])
```

### <a name="parameters---displacenegativemode"></a><span data-ttu-id="dce85-467">パラメーター - displaceNegativeMode</span><span class="sxs-lookup"><span data-stu-id="dce85-467">Parameters - displaceNegativeMode</span></span>

<span data-ttu-id="dce85-468">モード</span><span class="sxs-lookup"><span data-stu-id="dce85-468">mode</span></span>  

### <a name="return-value---displacenegativemode"></a><span data-ttu-id="dce85-469">戻り値 - displaceNegativeMode</span><span class="sxs-lookup"><span data-stu-id="dce85-469">Return Value - displaceNegativeMode</span></span>

## <a name="method-displacenegativevalue"></a><span data-ttu-id="dce85-470">メソッド displaceNegativeValue</span><span class="sxs-lookup"><span data-stu-id="dce85-470">Method displaceNegativeValue</span></span>

```xpp
public int displaceNegativeValue([int value])
```

### <a name="parameters---displacenegativevalue"></a><span data-ttu-id="dce85-471">パラメーター - displaceNegativeValue</span><span class="sxs-lookup"><span data-stu-id="dce85-471">Parameters - displaceNegativeValue</span></span>

<span data-ttu-id="dce85-472">値</span><span class="sxs-lookup"><span data-stu-id="dce85-472">value</span></span>  

### <a name="return-value---displacenegativevalue"></a><span data-ttu-id="dce85-473">戻り値 - displaceNegativeValue</span><span class="sxs-lookup"><span data-stu-id="dce85-473">Return Value - displaceNegativeValue</span></span>

## <a name="method-displayheight"></a><span data-ttu-id="dce85-474">メソッド displayHeight</span><span class="sxs-lookup"><span data-stu-id="dce85-474">Method displayHeight</span></span>

```xpp
public int displayHeight([int value], [AutoMode mode])
```

### <a name="parameters---displayheight"></a><span data-ttu-id="dce85-475">パラメーター - displayHeight</span><span class="sxs-lookup"><span data-stu-id="dce85-475">Parameters - displayHeight</span></span>

<span data-ttu-id="dce85-476">値</span><span class="sxs-lookup"><span data-stu-id="dce85-476">value</span></span>  

<!-- -->

<span data-ttu-id="dce85-477">モード</span><span class="sxs-lookup"><span data-stu-id="dce85-477">mode</span></span>  

### <a name="return-value---displayheight"></a><span data-ttu-id="dce85-478">戻り値 - displayHeight</span><span class="sxs-lookup"><span data-stu-id="dce85-478">Return Value - displayHeight</span></span>

## <a name="method-displayheightmode"></a><span data-ttu-id="dce85-479">メソッド displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="dce85-479">Method displayHeightMode</span></span>

```xpp
public AutoMode displayHeightMode([AutoMode mode])
```

### <a name="parameters---displayheightmode"></a><span data-ttu-id="dce85-480">パラメーター - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="dce85-480">Parameters - displayHeightMode</span></span>

<span data-ttu-id="dce85-481">モード</span><span class="sxs-lookup"><span data-stu-id="dce85-481">mode</span></span>  

### <a name="return-value---displayheightmode"></a><span data-ttu-id="dce85-482">戻り値 - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="dce85-482">Return Value - displayHeightMode</span></span>

## <a name="method-displayheightvalue"></a><span data-ttu-id="dce85-483">メソッド displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="dce85-483">Method displayHeightValue</span></span>

```xpp
public int displayHeightValue([int value])
```

### <a name="parameters---displayheightvalue"></a><span data-ttu-id="dce85-484">パラメーター - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="dce85-484">Parameters - displayHeightValue</span></span>

<span data-ttu-id="dce85-485">値</span><span class="sxs-lookup"><span data-stu-id="dce85-485">value</span></span>  

### <a name="return-value---displayheightvalue"></a><span data-ttu-id="dce85-486">戻り値 - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="dce85-486">Return Value - displayHeightValue</span></span>

## <a name="method-displaylength"></a><span data-ttu-id="dce85-487">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="dce85-487">Method displayLength</span></span>

```xpp
public int displayLength([int value], [AutoMode mode])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="dce85-488">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="dce85-488">Parameters - displayLength</span></span>

<span data-ttu-id="dce85-489">値</span><span class="sxs-lookup"><span data-stu-id="dce85-489">value</span></span>  

<!-- -->

<span data-ttu-id="dce85-490">モード</span><span class="sxs-lookup"><span data-stu-id="dce85-490">mode</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="dce85-491">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="dce85-491">Return Value - displayLength</span></span>

## <a name="method-displaylengthmode"></a><span data-ttu-id="dce85-492">メソッド displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="dce85-492">Method displayLengthMode</span></span>

```xpp
public AutoMode displayLengthMode([AutoMode mode])
```

### <a name="parameters---displaylengthmode"></a><span data-ttu-id="dce85-493">パラメーター - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="dce85-493">Parameters - displayLengthMode</span></span>

<span data-ttu-id="dce85-494">モード</span><span class="sxs-lookup"><span data-stu-id="dce85-494">mode</span></span>  

### <a name="return-value---displaylengthmode"></a><span data-ttu-id="dce85-495">戻り値 - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="dce85-495">Return Value - displayLengthMode</span></span>

## <a name="method-displaylengthvalue"></a><span data-ttu-id="dce85-496">メソッド displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="dce85-496">Method displayLengthValue</span></span>

```xpp
public int displayLengthValue([int value])
```

### <a name="parameters---displaylengthvalue"></a><span data-ttu-id="dce85-497">パラメーター - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="dce85-497">Parameters - displayLengthValue</span></span>

<span data-ttu-id="dce85-498">値</span><span class="sxs-lookup"><span data-stu-id="dce85-498">value</span></span>  

### <a name="return-value---displaylengthvalue"></a><span data-ttu-id="dce85-499">戻り値 - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="dce85-499">Return Value - displayLengthValue</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="dce85-500">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="dce85-500">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="dce85-501">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="dce85-501">Parameters - displayTarget</span></span>

<span data-ttu-id="dce85-502">値</span><span class="sxs-lookup"><span data-stu-id="dce85-502">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="dce85-503">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="dce85-503">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="dce85-504">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="dce85-504">Method dragDrop</span></span>

<span data-ttu-id="dce85-505">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-505">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="dce85-506">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="dce85-506">Parameters - dragDrop</span></span>

<span data-ttu-id="dce85-507">値</span><span class="sxs-lookup"><span data-stu-id="dce85-507">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="dce85-508">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="dce85-508">Return Value - dragDrop</span></span>

<span data-ttu-id="dce85-509">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="dce85-509">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="dce85-510">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="dce85-510">Method enabled</span></span>

<span data-ttu-id="dce85-511">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-511">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="dce85-512">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="dce85-512">Parameters - enabled</span></span>

<span data-ttu-id="dce85-513">値</span><span class="sxs-lookup"><span data-stu-id="dce85-513">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="dce85-514">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="dce85-514">Return Value - enabled</span></span>

<span data-ttu-id="dce85-515">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="dce85-515">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="dce85-516">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="dce85-516">Remarks - enabled</span></span>

<span data-ttu-id="dce85-517">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="dce85-517">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="dce85-518">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="dce85-518">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="dce85-519">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="dce85-519">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="dce85-520">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="dce85-520">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="dce85-521">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="dce85-521">Parameters - extendedDataType</span></span>

<span data-ttu-id="dce85-522">値</span><span class="sxs-lookup"><span data-stu-id="dce85-522">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="dce85-523">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="dce85-523">Return Value - extendedDataType</span></span>

## <a name="method-fasttabsummary"></a><span data-ttu-id="dce85-524">メソッド fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="dce85-524">Method fastTabSummary</span></span>

```xpp
public int fastTabSummary([int value])
```

### <a name="parameters---fasttabsummary"></a><span data-ttu-id="dce85-525">パラメーター - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="dce85-525">Parameters - fastTabSummary</span></span>

<span data-ttu-id="dce85-526">値</span><span class="sxs-lookup"><span data-stu-id="dce85-526">value</span></span>  

### <a name="return-value---fasttabsummary"></a><span data-ttu-id="dce85-527">戻り値 - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="dce85-527">Return Value - fastTabSummary</span></span>

## <a name="method-font"></a><span data-ttu-id="dce85-528">メソッド font</span><span class="sxs-lookup"><span data-stu-id="dce85-528">Method font</span></span>

<span data-ttu-id="dce85-529">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-529">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="dce85-530">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="dce85-530">Parameters - font</span></span>

<span data-ttu-id="dce85-531">値</span><span class="sxs-lookup"><span data-stu-id="dce85-531">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="dce85-532">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="dce85-532">Return Value - font</span></span>

<span data-ttu-id="dce85-533">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="dce85-533">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="dce85-534">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="dce85-534">Method fontSize</span></span>

<span data-ttu-id="dce85-535">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-535">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="dce85-536">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="dce85-536">Parameters - fontSize</span></span>

<span data-ttu-id="dce85-537">値</span><span class="sxs-lookup"><span data-stu-id="dce85-537">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="dce85-538">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="dce85-538">Return Value - fontSize</span></span>

<span data-ttu-id="dce85-539">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="dce85-539">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="dce85-540">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="dce85-540">Method foregroundColor</span></span>

<span data-ttu-id="dce85-541">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-541">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="dce85-542">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="dce85-542">Parameters - foregroundColor</span></span>

<span data-ttu-id="dce85-543">値</span><span class="sxs-lookup"><span data-stu-id="dce85-543">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="dce85-544">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="dce85-544">Return Value - foregroundColor</span></span>

<span data-ttu-id="dce85-545">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="dce85-545">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="dce85-546">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="dce85-546">Remarks - foregroundColor</span></span>

<span data-ttu-id="dce85-547">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="dce85-547">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="dce85-548">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dce85-548">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="dce85-549">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="dce85-549">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="dce85-550">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="dce85-550">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="dce85-551">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="dce85-551">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="dce85-552">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="dce85-552">The maximum value for a single byte is 255.</span></span>

## <a name="method-height"></a><span data-ttu-id="dce85-553">メソッド height</span><span class="sxs-lookup"><span data-stu-id="dce85-553">Method height</span></span>

<span data-ttu-id="dce85-554">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-554">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="dce85-555">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="dce85-555">Parameters - height</span></span>

<span data-ttu-id="dce85-556">値</span><span class="sxs-lookup"><span data-stu-id="dce85-556">value</span></span>  

<!-- -->

<span data-ttu-id="dce85-557">モード</span><span class="sxs-lookup"><span data-stu-id="dce85-557">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="dce85-558">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="dce85-558">Return Value - height</span></span>

<span data-ttu-id="dce85-559">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="dce85-559">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="dce85-560">備考 - height</span><span class="sxs-lookup"><span data-stu-id="dce85-560">Remarks - height</span></span>

<span data-ttu-id="dce85-561">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="dce85-561">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="dce85-562">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="dce85-562">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="dce85-563">モード。</span><span class="sxs-lookup"><span data-stu-id="dce85-563">Mode.</span></span>            | <span data-ttu-id="dce85-564">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="dce85-564">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="dce85-565">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="dce85-565">-1 Exact.</span></span>        | <span data-ttu-id="dce85-566">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="dce85-566">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="dce85-567">0 自動。</span><span class="sxs-lookup"><span data-stu-id="dce85-567">0 Auto.</span></span>          | <span data-ttu-id="dce85-568">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="dce85-568">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="dce85-569">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="dce85-569">1 Column height.</span></span> | <span data-ttu-id="dce85-570">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="dce85-570">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="dce85-571">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="dce85-571">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="dce85-572">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="dce85-572">Method heightMode</span></span>

<span data-ttu-id="dce85-573">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-573">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="dce85-574">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="dce85-574">Parameters - heightMode</span></span>

<span data-ttu-id="dce85-575">値</span><span class="sxs-lookup"><span data-stu-id="dce85-575">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="dce85-576">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="dce85-576">Return Value - heightMode</span></span>

<span data-ttu-id="dce85-577">計算モード。</span><span class="sxs-lookup"><span data-stu-id="dce85-577">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="dce85-578">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="dce85-578">Remarks - heightMode</span></span>

<span data-ttu-id="dce85-579">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="dce85-579">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="dce85-580">モード。</span><span class="sxs-lookup"><span data-stu-id="dce85-580">Mode.</span></span>          | <span data-ttu-id="dce85-581">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="dce85-581">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="dce85-582">正確。</span><span class="sxs-lookup"><span data-stu-id="dce85-582">Exact.</span></span>         | <span data-ttu-id="dce85-583">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="dce85-583">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="dce85-584">自動。</span><span class="sxs-lookup"><span data-stu-id="dce85-584">Auto.</span></span>          | <span data-ttu-id="dce85-585">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="dce85-585">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="dce85-586">列の高さ</span><span class="sxs-lookup"><span data-stu-id="dce85-586">Column height.</span></span> | <span data-ttu-id="dce85-587">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="dce85-587">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="dce85-588">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="dce85-588">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="dce85-589">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="dce85-589">Method heightValue</span></span>

<span data-ttu-id="dce85-590">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-590">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="dce85-591">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="dce85-591">Parameters - heightValue</span></span>

<span data-ttu-id="dce85-592">値</span><span class="sxs-lookup"><span data-stu-id="dce85-592">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="dce85-593">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="dce85-593">Return Value - heightValue</span></span>

<span data-ttu-id="dce85-594">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="dce85-594">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="dce85-595">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="dce85-595">Remarks - heightValue</span></span>

<span data-ttu-id="dce85-596">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="dce85-596">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="dce85-597">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="dce85-597">Method helpText</span></span>

<span data-ttu-id="dce85-598">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-598">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="dce85-599">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="dce85-599">Parameters - helpText</span></span>

<span data-ttu-id="dce85-600">値</span><span class="sxs-lookup"><span data-stu-id="dce85-600">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="dce85-601">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="dce85-601">Return Value - helpText</span></span>

<span data-ttu-id="dce85-602">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="dce85-602">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="dce85-603">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="dce85-603">Remarks - helpText</span></span>

<span data-ttu-id="dce85-604">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-604">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="dce85-605">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="dce85-605">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="dce85-606">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="dce85-606">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="dce85-607">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="dce85-607">Parameters - hierarchyParent</span></span>

<span data-ttu-id="dce85-608">値</span><span class="sxs-lookup"><span data-stu-id="dce85-608">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="dce85-609">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="dce85-609">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="dce85-610">メソッド id</span><span class="sxs-lookup"><span data-stu-id="dce85-610">Method id</span></span>

<span data-ttu-id="dce85-611">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="dce85-611">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="dce85-612">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="dce85-612">Return Value - id</span></span>

<span data-ttu-id="dce85-613">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="dce85-613">The ID of the control.</span></span>

## <a name="method-imemode"></a><span data-ttu-id="dce85-614">メソッド iMEMode</span><span class="sxs-lookup"><span data-stu-id="dce85-614">Method iMEMode</span></span>

```xpp
public int iMEMode([int value])
```

### <a name="parameters---imemode"></a><span data-ttu-id="dce85-615">パラメーター - iMEMode</span><span class="sxs-lookup"><span data-stu-id="dce85-615">Parameters - iMEMode</span></span>

<span data-ttu-id="dce85-616">値</span><span class="sxs-lookup"><span data-stu-id="dce85-616">value</span></span>  

### <a name="return-value---imemode"></a><span data-ttu-id="dce85-617">戻り値 - iMEMode</span><span class="sxs-lookup"><span data-stu-id="dce85-617">Return Value - iMEMode</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="dce85-618">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="dce85-618">Method isContainer</span></span>

<span data-ttu-id="dce85-619">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="dce85-619">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="dce85-620">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="dce85-620">Return Value - isContainer</span></span>

<span data-ttu-id="dce85-621">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="dce85-621">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-italic"></a><span data-ttu-id="dce85-622">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="dce85-622">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="dce85-623">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="dce85-623">Parameters - italic</span></span>

<span data-ttu-id="dce85-624">値</span><span class="sxs-lookup"><span data-stu-id="dce85-624">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="dce85-625">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="dce85-625">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="dce85-626">メソッド label</span><span class="sxs-lookup"><span data-stu-id="dce85-626">Method label</span></span>

<span data-ttu-id="dce85-627">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-627">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="dce85-628">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="dce85-628">Parameters - label</span></span>

<span data-ttu-id="dce85-629">値</span><span class="sxs-lookup"><span data-stu-id="dce85-629">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="dce85-630">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="dce85-630">Return Value - label</span></span>

<span data-ttu-id="dce85-631">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="dce85-631">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="dce85-632">備考 - label</span><span class="sxs-lookup"><span data-stu-id="dce85-632">Remarks - label</span></span>

<span data-ttu-id="dce85-633">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-633">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="dce85-634">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="dce85-634">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="dce85-635">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="dce85-635">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="dce85-636">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="dce85-636">Parameters - labelAlignment</span></span>

<span data-ttu-id="dce85-637">値</span><span class="sxs-lookup"><span data-stu-id="dce85-637">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="dce85-638">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="dce85-638">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="dce85-639">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="dce85-639">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="dce85-640">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="dce85-640">Parameters - labelBold</span></span>

<span data-ttu-id="dce85-641">値</span><span class="sxs-lookup"><span data-stu-id="dce85-641">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="dce85-642">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="dce85-642">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="dce85-643">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="dce85-643">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="dce85-644">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="dce85-644">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="dce85-645">値</span><span class="sxs-lookup"><span data-stu-id="dce85-645">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="dce85-646">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="dce85-646">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="dce85-647">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="dce85-647">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="dce85-648">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="dce85-648">Parameters - labelFont</span></span>

<span data-ttu-id="dce85-649">値</span><span class="sxs-lookup"><span data-stu-id="dce85-649">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="dce85-650">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="dce85-650">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="dce85-651">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="dce85-651">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="dce85-652">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="dce85-652">Parameters - labelFontSize</span></span>

<span data-ttu-id="dce85-653">値</span><span class="sxs-lookup"><span data-stu-id="dce85-653">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="dce85-654">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="dce85-654">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="dce85-655">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="dce85-655">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="dce85-656">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="dce85-656">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="dce85-657">値</span><span class="sxs-lookup"><span data-stu-id="dce85-657">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="dce85-658">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="dce85-658">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="dce85-659">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="dce85-659">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="dce85-660">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="dce85-660">Parameters - labelGuide</span></span>

<span data-ttu-id="dce85-661">値</span><span class="sxs-lookup"><span data-stu-id="dce85-661">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="dce85-662">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="dce85-662">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="dce85-663">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="dce85-663">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="dce85-664">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="dce85-664">Parameters - labelHeight</span></span>

<span data-ttu-id="dce85-665">値</span><span class="sxs-lookup"><span data-stu-id="dce85-665">value</span></span>  

<!-- -->

<span data-ttu-id="dce85-666">モード</span><span class="sxs-lookup"><span data-stu-id="dce85-666">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="dce85-667">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="dce85-667">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="dce85-668">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="dce85-668">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="dce85-669">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="dce85-669">Parameters - labelHeightMode</span></span>

<span data-ttu-id="dce85-670">値</span><span class="sxs-lookup"><span data-stu-id="dce85-670">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="dce85-671">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="dce85-671">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="dce85-672">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="dce85-672">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="dce85-673">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="dce85-673">Parameters - labelHeightValue</span></span>

<span data-ttu-id="dce85-674">値</span><span class="sxs-lookup"><span data-stu-id="dce85-674">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="dce85-675">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="dce85-675">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="dce85-676">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="dce85-676">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="dce85-677">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="dce85-677">Parameters - labelItalic</span></span>

<span data-ttu-id="dce85-678">値</span><span class="sxs-lookup"><span data-stu-id="dce85-678">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="dce85-679">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="dce85-679">Return Value - labelItalic</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="dce85-680">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="dce85-680">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="dce85-681">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="dce85-681">Parameters - labelPosition</span></span>

<span data-ttu-id="dce85-682">値</span><span class="sxs-lookup"><span data-stu-id="dce85-682">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="dce85-683">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="dce85-683">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="dce85-684">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="dce85-684">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="dce85-685">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="dce85-685">Parameters - labelUnderline</span></span>

<span data-ttu-id="dce85-686">値</span><span class="sxs-lookup"><span data-stu-id="dce85-686">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="dce85-687">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="dce85-687">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="dce85-688">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="dce85-688">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="dce85-689">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="dce85-689">Parameters - labelWidth</span></span>

<span data-ttu-id="dce85-690">値</span><span class="sxs-lookup"><span data-stu-id="dce85-690">value</span></span>  

<!-- -->

<span data-ttu-id="dce85-691">モード</span><span class="sxs-lookup"><span data-stu-id="dce85-691">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="dce85-692">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="dce85-692">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="dce85-693">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="dce85-693">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="dce85-694">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="dce85-694">Parameters - labelWidthMode</span></span>

<span data-ttu-id="dce85-695">値</span><span class="sxs-lookup"><span data-stu-id="dce85-695">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="dce85-696">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="dce85-696">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="dce85-697">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="dce85-697">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="dce85-698">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="dce85-698">Parameters - labelWidthValue</span></span>

<span data-ttu-id="dce85-699">値</span><span class="sxs-lookup"><span data-stu-id="dce85-699">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="dce85-700">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="dce85-700">Return Value - labelWidthValue</span></span>

## <a name="method-left"></a><span data-ttu-id="dce85-701">メソッド left</span><span class="sxs-lookup"><span data-stu-id="dce85-701">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="dce85-702">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="dce85-702">Parameters - left</span></span>

<span data-ttu-id="dce85-703">値</span><span class="sxs-lookup"><span data-stu-id="dce85-703">value</span></span>  

<!-- -->

<span data-ttu-id="dce85-704">モード</span><span class="sxs-lookup"><span data-stu-id="dce85-704">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="dce85-705">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="dce85-705">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="dce85-706">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="dce85-706">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="dce85-707">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="dce85-707">Parameters - leftMode</span></span>

<span data-ttu-id="dce85-708">値</span><span class="sxs-lookup"><span data-stu-id="dce85-708">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="dce85-709">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="dce85-709">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="dce85-710">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="dce85-710">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="dce85-711">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="dce85-711">Parameters - leftValue</span></span>

<span data-ttu-id="dce85-712">値</span><span class="sxs-lookup"><span data-stu-id="dce85-712">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="dce85-713">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="dce85-713">Return Value - leftValue</span></span>

## <a name="method-limittext"></a><span data-ttu-id="dce85-714">メソッド limitText</span><span class="sxs-lookup"><span data-stu-id="dce85-714">Method limitText</span></span>

```xpp
public int limitText([int value], [AutoMode mode])
```

### <a name="parameters---limittext"></a><span data-ttu-id="dce85-715">パラメーター - limitText</span><span class="sxs-lookup"><span data-stu-id="dce85-715">Parameters - limitText</span></span>

<span data-ttu-id="dce85-716">値</span><span class="sxs-lookup"><span data-stu-id="dce85-716">value</span></span>  

<!-- -->

<span data-ttu-id="dce85-717">モード</span><span class="sxs-lookup"><span data-stu-id="dce85-717">mode</span></span>  

### <a name="return-value---limittext"></a><span data-ttu-id="dce85-718">戻り値 - limitText</span><span class="sxs-lookup"><span data-stu-id="dce85-718">Return Value - limitText</span></span>

## <a name="method-limittextmode"></a><span data-ttu-id="dce85-719">メソッド limitTextMode</span><span class="sxs-lookup"><span data-stu-id="dce85-719">Method limitTextMode</span></span>

```xpp
public AutoMode limitTextMode([AutoMode mode])
```

### <a name="parameters---limittextmode"></a><span data-ttu-id="dce85-720">パラメーター - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="dce85-720">Parameters - limitTextMode</span></span>

<span data-ttu-id="dce85-721">モード</span><span class="sxs-lookup"><span data-stu-id="dce85-721">mode</span></span>  

### <a name="return-value---limittextmode"></a><span data-ttu-id="dce85-722">戻り値 - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="dce85-722">Return Value - limitTextMode</span></span>

## <a name="method-limittextvalue"></a><span data-ttu-id="dce85-723">メソッド limitTextValue</span><span class="sxs-lookup"><span data-stu-id="dce85-723">Method limitTextValue</span></span>

```xpp
public int limitTextValue([int value])
```

### <a name="parameters---limittextvalue"></a><span data-ttu-id="dce85-724">パラメーター - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="dce85-724">Parameters - limitTextValue</span></span>

<span data-ttu-id="dce85-725">値</span><span class="sxs-lookup"><span data-stu-id="dce85-725">value</span></span>  

### <a name="return-value---limittextvalue"></a><span data-ttu-id="dce85-726">戻り値 - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="dce85-726">Return Value - limitTextValue</span></span>

## <a name="method-lookupbutton"></a><span data-ttu-id="dce85-727">メソッド lookupButton</span><span class="sxs-lookup"><span data-stu-id="dce85-727">Method lookupButton</span></span>

```xpp
public int lookupButton([int value])
```

### <a name="parameters---lookupbutton"></a><span data-ttu-id="dce85-728">パラメーター - lookupButton</span><span class="sxs-lookup"><span data-stu-id="dce85-728">Parameters - lookupButton</span></span>

<span data-ttu-id="dce85-729">値</span><span class="sxs-lookup"><span data-stu-id="dce85-729">value</span></span>  

### <a name="return-value---lookupbutton"></a><span data-ttu-id="dce85-730">戻り値 - lookupButton</span><span class="sxs-lookup"><span data-stu-id="dce85-730">Return Value - lookupButton</span></span>

## <a name="method-mandatory"></a><span data-ttu-id="dce85-731">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="dce85-731">Method mandatory</span></span>

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a><span data-ttu-id="dce85-732">パラメーター - mandatory</span><span class="sxs-lookup"><span data-stu-id="dce85-732">Parameters - mandatory</span></span>

<span data-ttu-id="dce85-733">値</span><span class="sxs-lookup"><span data-stu-id="dce85-733">value</span></span>  

### <a name="return-value---mandatory"></a><span data-ttu-id="dce85-734">戻り値 - mandatory</span><span class="sxs-lookup"><span data-stu-id="dce85-734">Return Value - mandatory</span></span>

## <a name="method-name"></a><span data-ttu-id="dce85-735">メソッド名</span><span class="sxs-lookup"><span data-stu-id="dce85-735">Method name</span></span>

<span data-ttu-id="dce85-736">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-736">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="dce85-737">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="dce85-737">Parameters - name</span></span>

<span data-ttu-id="dce85-738">値</span><span class="sxs-lookup"><span data-stu-id="dce85-738">value</span></span>  
<span data-ttu-id="dce85-739">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="dce85-739">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="dce85-740">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="dce85-740">Return Value - name</span></span>

<span data-ttu-id="dce85-741">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="dce85-741">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="dce85-742">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="dce85-742">Remarks - name</span></span>

<span data-ttu-id="dce85-743">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="dce85-743">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="dce85-744">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="dce85-744">It must start with a letter.</span></span>
-   <span data-ttu-id="dce85-745">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="dce85-745">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="dce85-746">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="dce85-746">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="dce85-747">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="dce85-747">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="dce85-748">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="dce85-748">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="dce85-749">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="dce85-749">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="dce85-750">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="dce85-750">Parameters - neededPermission</span></span>

<span data-ttu-id="dce85-751">値</span><span class="sxs-lookup"><span data-stu-id="dce85-751">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="dce85-752">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="dce85-752">Return Value - neededPermission</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="dce85-753">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="dce85-753">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="dce85-754">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="dce85-754">Parameters - promptrect</span></span>

<span data-ttu-id="dce85-755">値</span><span class="sxs-lookup"><span data-stu-id="dce85-755">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="dce85-756">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="dce85-756">Return Value - promptrect</span></span>

## <a name="method-replaceonlookup"></a><span data-ttu-id="dce85-757">メソッド replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="dce85-757">Method replaceOnLookup</span></span>

```xpp
public boolean replaceOnLookup([boolean value])
```

### <a name="parameters---replaceonlookup"></a><span data-ttu-id="dce85-758">パラメーター - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="dce85-758">Parameters - replaceOnLookup</span></span>

<span data-ttu-id="dce85-759">値</span><span class="sxs-lookup"><span data-stu-id="dce85-759">value</span></span>  

### <a name="return-value---replaceonlookup"></a><span data-ttu-id="dce85-760">戻り値 - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="dce85-760">Return Value - replaceOnLookup</span></span>

## <a name="method-rotatesign"></a><span data-ttu-id="dce85-761">メソッド rotateSign</span><span class="sxs-lookup"><span data-stu-id="dce85-761">Method rotateSign</span></span>

```xpp
public int rotateSign([int value])
```

### <a name="parameters---rotatesign"></a><span data-ttu-id="dce85-762">パラメーター - rotateSign</span><span class="sxs-lookup"><span data-stu-id="dce85-762">Parameters - rotateSign</span></span>

<span data-ttu-id="dce85-763">値</span><span class="sxs-lookup"><span data-stu-id="dce85-763">value</span></span>  

### <a name="return-value---rotatesign"></a><span data-ttu-id="dce85-764">戻り値 - rotateSign</span><span class="sxs-lookup"><span data-stu-id="dce85-764">Return Value - rotateSign</span></span>

## <a name="method-searchafterinput"></a><span data-ttu-id="dce85-765">メソッド searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="dce85-765">Method searchAfterInput</span></span>

```xpp
public int searchAfterInput([int value])
```

### <a name="parameters---searchafterinput"></a><span data-ttu-id="dce85-766">パラメーター - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="dce85-766">Parameters - searchAfterInput</span></span>

<span data-ttu-id="dce85-767">値</span><span class="sxs-lookup"><span data-stu-id="dce85-767">value</span></span>  

### <a name="return-value---searchafterinput"></a><span data-ttu-id="dce85-768">戻り値 - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="dce85-768">Return Value - searchAfterInput</span></span>

## <a name="method-searchmode"></a><span data-ttu-id="dce85-769">メソッド searchMode</span><span class="sxs-lookup"><span data-stu-id="dce85-769">Method searchMode</span></span>

```xpp
public int searchMode([int value])
```

### <a name="parameters---searchmode"></a><span data-ttu-id="dce85-770">パラメーター - searchMode</span><span class="sxs-lookup"><span data-stu-id="dce85-770">Parameters - searchMode</span></span>

<span data-ttu-id="dce85-771">値</span><span class="sxs-lookup"><span data-stu-id="dce85-771">value</span></span>  

### <a name="return-value---searchmode"></a><span data-ttu-id="dce85-772">戻り値 - searchMode</span><span class="sxs-lookup"><span data-stu-id="dce85-772">Return Value - searchMode</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="dce85-773">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="dce85-773">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="dce85-774">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="dce85-774">Parameters - securityKey</span></span>

<span data-ttu-id="dce85-775">値</span><span class="sxs-lookup"><span data-stu-id="dce85-775">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="dce85-776">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="dce85-776">Return Value - securityKey</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="dce85-777">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="dce85-777">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="dce85-778">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="dce85-778">Parameters - showLabel</span></span>

<span data-ttu-id="dce85-779">値</span><span class="sxs-lookup"><span data-stu-id="dce85-779">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="dce85-780">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="dce85-780">Return Value - showLabel</span></span>

## <a name="method-showzero"></a><span data-ttu-id="dce85-781">メソッド showZero</span><span class="sxs-lookup"><span data-stu-id="dce85-781">Method showZero</span></span>

```xpp
public int showZero([int value])
```

### <a name="parameters---showzero"></a><span data-ttu-id="dce85-782">パラメーター - showZero</span><span class="sxs-lookup"><span data-stu-id="dce85-782">Parameters - showZero</span></span>

<span data-ttu-id="dce85-783">値</span><span class="sxs-lookup"><span data-stu-id="dce85-783">value</span></span>  

### <a name="return-value---showzero"></a><span data-ttu-id="dce85-784">戻り値 - showZero</span><span class="sxs-lookup"><span data-stu-id="dce85-784">Return Value - showZero</span></span>

## <a name="method-signdisplay"></a><span data-ttu-id="dce85-785">メソッド signDisplay</span><span class="sxs-lookup"><span data-stu-id="dce85-785">Method signDisplay</span></span>

```xpp
public int signDisplay([int value])
```

### <a name="parameters---signdisplay"></a><span data-ttu-id="dce85-786">パラメーター - signDisplay</span><span class="sxs-lookup"><span data-stu-id="dce85-786">Parameters - signDisplay</span></span>

<span data-ttu-id="dce85-787">値</span><span class="sxs-lookup"><span data-stu-id="dce85-787">value</span></span>  

### <a name="return-value---signdisplay"></a><span data-ttu-id="dce85-788">戻り値 - signDisplay</span><span class="sxs-lookup"><span data-stu-id="dce85-788">Return Value - signDisplay</span></span>

## <a name="method-skip"></a><span data-ttu-id="dce85-789">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="dce85-789">Method skip</span></span>

<span data-ttu-id="dce85-790">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="dce85-790">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="dce85-791">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="dce85-791">Parameters - skip</span></span>

<span data-ttu-id="dce85-792">値</span><span class="sxs-lookup"><span data-stu-id="dce85-792">value</span></span>  
<span data-ttu-id="dce85-793">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="dce85-793">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="dce85-794">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="dce85-794">Return Value - skip</span></span>

<span data-ttu-id="dce85-795">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="dce85-795">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-style"></a><span data-ttu-id="dce85-796">メソッド style</span><span class="sxs-lookup"><span data-stu-id="dce85-796">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="dce85-797">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="dce85-797">Parameters - style</span></span>

<span data-ttu-id="dce85-798">値</span><span class="sxs-lookup"><span data-stu-id="dce85-798">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="dce85-799">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="dce85-799">Return Value - style</span></span>

## <a name="method-top"></a><span data-ttu-id="dce85-800">メソッド top</span><span class="sxs-lookup"><span data-stu-id="dce85-800">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="dce85-801">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="dce85-801">Parameters - top</span></span>

<span data-ttu-id="dce85-802">値</span><span class="sxs-lookup"><span data-stu-id="dce85-802">value</span></span>  

<!-- -->

<span data-ttu-id="dce85-803">モード</span><span class="sxs-lookup"><span data-stu-id="dce85-803">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="dce85-804">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="dce85-804">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="dce85-805">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="dce85-805">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="dce85-806">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="dce85-806">Parameters - topMode</span></span>

<span data-ttu-id="dce85-807">値</span><span class="sxs-lookup"><span data-stu-id="dce85-807">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="dce85-808">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="dce85-808">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="dce85-809">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="dce85-809">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="dce85-810">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="dce85-810">Parameters - topValue</span></span>

<span data-ttu-id="dce85-811">値</span><span class="sxs-lookup"><span data-stu-id="dce85-811">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="dce85-812">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="dce85-812">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="dce85-813">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="dce85-813">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="dce85-814">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="dce85-814">Parameters - type</span></span>

<span data-ttu-id="dce85-815">値</span><span class="sxs-lookup"><span data-stu-id="dce85-815">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="dce85-816">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="dce85-816">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="dce85-817">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="dce85-817">Method underline</span></span>

<span data-ttu-id="dce85-818">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="dce85-818">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="dce85-819">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="dce85-819">Parameters - underline</span></span>

<span data-ttu-id="dce85-820">値</span><span class="sxs-lookup"><span data-stu-id="dce85-820">value</span></span>  
<span data-ttu-id="dce85-821">コントロールの underline プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="dce85-821">The value to assign to the underline property of the control; optional.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="dce85-822">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="dce85-822">Return Value - underline</span></span>

<span data-ttu-id="dce85-823">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="dce85-823">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-userdata"></a><span data-ttu-id="dce85-824">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="dce85-824">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="dce85-825">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="dce85-825">Parameters - userData</span></span>

<span data-ttu-id="dce85-826">値</span><span class="sxs-lookup"><span data-stu-id="dce85-826">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="dce85-827">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="dce85-827">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="dce85-828">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="dce85-828">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="dce85-829">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="dce85-829">Parameters - userDataItem</span></span>

<span data-ttu-id="dce85-830">値</span><span class="sxs-lookup"><span data-stu-id="dce85-830">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="dce85-831">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="dce85-831">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="dce85-832">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="dce85-832">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="dce85-833">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="dce85-833">Parameters - userDataItems</span></span>

<span data-ttu-id="dce85-834">値</span><span class="sxs-lookup"><span data-stu-id="dce85-834">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="dce85-835">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="dce85-835">Return Value - userDataItems</span></span>

## <a name="method-value"></a><span data-ttu-id="dce85-836">メソッド value</span><span class="sxs-lookup"><span data-stu-id="dce85-836">Method value</span></span>

```xpp
public int value([int value])
```

### <a name="parameters---value"></a><span data-ttu-id="dce85-837">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="dce85-837">Parameters - value</span></span>

<span data-ttu-id="dce85-838">値</span><span class="sxs-lookup"><span data-stu-id="dce85-838">value</span></span>  

### <a name="return-value---value"></a><span data-ttu-id="dce85-839">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="dce85-839">Return Value - value</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="dce85-840">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="dce85-840">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="dce85-841">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="dce85-841">Parameters - verticalSpacing</span></span>

<span data-ttu-id="dce85-842">値</span><span class="sxs-lookup"><span data-stu-id="dce85-842">value</span></span>  

<!-- -->

<span data-ttu-id="dce85-843">モード</span><span class="sxs-lookup"><span data-stu-id="dce85-843">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="dce85-844">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="dce85-844">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="dce85-845">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="dce85-845">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="dce85-846">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="dce85-846">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="dce85-847">モード</span><span class="sxs-lookup"><span data-stu-id="dce85-847">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="dce85-848">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="dce85-848">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="dce85-849">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="dce85-849">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="dce85-850">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="dce85-850">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="dce85-851">値</span><span class="sxs-lookup"><span data-stu-id="dce85-851">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="dce85-852">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="dce85-852">Return Value - verticalSpacingValue</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="dce85-853">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="dce85-853">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="dce85-854">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="dce85-854">Parameters - viewEditMode</span></span>

<span data-ttu-id="dce85-855">値</span><span class="sxs-lookup"><span data-stu-id="dce85-855">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="dce85-856">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="dce85-856">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="dce85-857">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="dce85-857">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="dce85-858">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="dce85-858">Parameters - visible</span></span>

<span data-ttu-id="dce85-859">値</span><span class="sxs-lookup"><span data-stu-id="dce85-859">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="dce85-860">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="dce85-860">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="dce85-861">メソッド width</span><span class="sxs-lookup"><span data-stu-id="dce85-861">Method width</span></span>

<span data-ttu-id="dce85-862">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-862">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="dce85-863">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="dce85-863">Parameters - width</span></span>

<span data-ttu-id="dce85-864">値</span><span class="sxs-lookup"><span data-stu-id="dce85-864">value</span></span>  

<!-- -->

<span data-ttu-id="dce85-865">モード</span><span class="sxs-lookup"><span data-stu-id="dce85-865">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="dce85-866">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="dce85-866">Return Value - width</span></span>

<span data-ttu-id="dce85-867">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="dce85-867">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="dce85-868">備考 - width</span><span class="sxs-lookup"><span data-stu-id="dce85-868">Remarks - width</span></span>

<span data-ttu-id="dce85-869">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="dce85-869">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="dce85-870">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="dce85-870">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="dce85-871">モード。</span><span class="sxs-lookup"><span data-stu-id="dce85-871">Mode.</span></span>           | <span data-ttu-id="dce85-872">幅計算。</span><span class="sxs-lookup"><span data-stu-id="dce85-872">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dce85-873">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="dce85-873">-1 Exact.</span></span>       | <span data-ttu-id="dce85-874">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="dce85-874">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="dce85-875">0 自動。</span><span class="sxs-lookup"><span data-stu-id="dce85-875">0 Auto.</span></span>         | <span data-ttu-id="dce85-876">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="dce85-876">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="dce85-877">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="dce85-877">1 Column width.</span></span> | <span data-ttu-id="dce85-878">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="dce85-878">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="dce85-879">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="dce85-879">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="dce85-880">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="dce85-880">Method widthMode</span></span>

<span data-ttu-id="dce85-881">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-881">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="dce85-882">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="dce85-882">Parameters - widthMode</span></span>

<span data-ttu-id="dce85-883">値</span><span class="sxs-lookup"><span data-stu-id="dce85-883">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="dce85-884">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="dce85-884">Return Value - widthMode</span></span>

<span data-ttu-id="dce85-885">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="dce85-885">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="dce85-886">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="dce85-886">Remarks - widthMode</span></span>

<span data-ttu-id="dce85-887">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="dce85-887">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="dce85-888">モード。</span><span class="sxs-lookup"><span data-stu-id="dce85-888">Mode.</span></span>         | <span data-ttu-id="dce85-889">幅計算。</span><span class="sxs-lookup"><span data-stu-id="dce85-889">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dce85-890">正確。</span><span class="sxs-lookup"><span data-stu-id="dce85-890">Exact.</span></span>        | <span data-ttu-id="dce85-891">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="dce85-891">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="dce85-892">自動。</span><span class="sxs-lookup"><span data-stu-id="dce85-892">Auto.</span></span>         | <span data-ttu-id="dce85-893">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="dce85-893">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="dce85-894">列の幅。</span><span class="sxs-lookup"><span data-stu-id="dce85-894">Column width.</span></span> | <span data-ttu-id="dce85-895">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="dce85-895">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="dce85-896">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="dce85-896">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="dce85-897">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="dce85-897">Method widthValue</span></span>

<span data-ttu-id="dce85-898">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="dce85-898">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="dce85-899">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="dce85-899">Parameters - widthValue</span></span>

<span data-ttu-id="dce85-900">値</span><span class="sxs-lookup"><span data-stu-id="dce85-900">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="dce85-901">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="dce85-901">Return Value - widthValue</span></span>

<span data-ttu-id="dce85-902">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="dce85-902">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="dce85-903">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="dce85-903">Remarks - widthValue</span></span>

<span data-ttu-id="dce85-904">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="dce85-904">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="dce85-905">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="dce85-905">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="dce85-906">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="dce85-906">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="dce85-907">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="dce85-907">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="dce85-908">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="dce85-908">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="dce85-909">overrideObject</span><span class="sxs-lookup"><span data-stu-id="dce85-909">overrideObject</span></span>  

