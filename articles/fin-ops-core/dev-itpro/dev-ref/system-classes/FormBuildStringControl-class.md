---
title: FormBuildStringControl クラス
description: このトピックでは、FormBuildStringControl クラスについて説明します。
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
ms.openlocfilehash: d76fc96bb9d743a1819efd87e60242a9839520f2
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502641"
---
# <a name="class-formbuildstringcontrol"></a><span data-ttu-id="a9b06-103">クラス FormBuildStringControl</span><span class="sxs-lookup"><span data-stu-id="a9b06-103">Class FormBuildStringControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildStringControl extends FormBuildControl
```

<span data-ttu-id="a9b06-104">FormBuildStringControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-104">The FormBuildStringControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9b06-105">備考</span><span class="sxs-lookup"><span data-stu-id="a9b06-105">Remarks</span></span>

<span data-ttu-id="a9b06-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="a9b06-107">例</span><span class="sxs-lookup"><span data-stu-id="a9b06-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="a9b06-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="a9b06-108">Methods</span></span>

| <span data-ttu-id="a9b06-109">方法</span><span class="sxs-lookup"><span data-stu-id="a9b06-109">Method</span></span>                                                                                                      | <span data-ttu-id="a9b06-110">説明</span><span class="sxs-lookup"><span data-stu-id="a9b06-110">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9b06-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="a9b06-112">コントロールを配置するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-112">Indicates whether to align the control.</span></span>                                                                                                 |
| <span data-ttu-id="a9b06-113">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-113">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="a9b06-114">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-114">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="a9b06-115">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-115">Determines whether the user can change the contents of the control.</span></span>                                                                     |
| <span data-ttu-id="a9b06-116">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-116">public int arrayIndex(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="a9b06-117">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-117">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="a9b06-118">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-118">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                      |
| <span data-ttu-id="a9b06-119">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-119">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="a9b06-120">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-120">Gets or sets the background color of the control.</span></span>                                                                                       |
| <span data-ttu-id="a9b06-121">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-121">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="a9b06-122">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-122">Determines whether the control background can be transparent.</span></span>                                                                          |
| <span data-ttu-id="a9b06-123">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-123">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="a9b06-124">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-124">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                             |
| <span data-ttu-id="a9b06-125">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-125">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="a9b06-126">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-126">Gets or sets the style of the borderline of the control.</span></span>                                                                                |
| <span data-ttu-id="a9b06-127">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-127">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="a9b06-128">public int changeCase(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-128">public int changeCase(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="a9b06-129">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-129">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="a9b06-130">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-130">Gets or sets the character set of the font.</span></span>                                                                                             |
| <span data-ttu-id="a9b06-131">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-131">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="a9b06-132">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-132">Gets or sets the color scheme of the control.</span></span>                                                                                           |
| <span data-ttu-id="a9b06-133">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-133">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="a9b06-134">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-134">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                     |
| <span data-ttu-id="a9b06-135">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="a9b06-135">public int containerId()</span></span>                                                                                    | <span data-ttu-id="a9b06-136">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-136">Retrieves the ID of the parent container for the control.</span></span>                                                                               |
| <span data-ttu-id="a9b06-137">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-137">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="a9b06-138">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-138">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                         |
| <span data-ttu-id="a9b06-139">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-139">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="a9b06-140">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-140">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="a9b06-141">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-141">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="a9b06-142">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-142">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="a9b06-143">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-143">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                |
| <span data-ttu-id="a9b06-144">public int direction(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-144">public int direction(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="a9b06-145">public int displayHeight(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-145">public int displayHeight(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                         |
| <span data-ttu-id="a9b06-146">public AutoMode displayHeightMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-146">public AutoMode displayHeightMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                         |
| <span data-ttu-id="a9b06-147">public int displayHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-147">public int displayHeightValue(\[int value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="a9b06-148">public int displayLength(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-148">public int displayLength(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                         |
| <span data-ttu-id="a9b06-149">public AutoMode displayLengthMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-149">public AutoMode displayLengthMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                         |
| <span data-ttu-id="a9b06-150">public int displayLengthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-150">public int displayLengthValue(\[int value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="a9b06-151">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-151">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="a9b06-152">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-152">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="a9b06-153">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-153">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                       |
| <span data-ttu-id="a9b06-154">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-154">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="a9b06-155">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-155">Determines whether to enable or disable the object.</span></span>                                                                                     |
| <span data-ttu-id="a9b06-156">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-156">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                         |
| <span data-ttu-id="a9b06-157">public int fastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-157">public int fastTabSummary(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="a9b06-158">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-158">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="a9b06-159">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-159">Gets or sets the name of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="a9b06-160">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-160">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="a9b06-161">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-161">Gets or sets the size of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="a9b06-162">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-162">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="a9b06-163">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-163">Gets or sets the text color for the control to use.</span></span>                                                                                     |
| <span data-ttu-id="a9b06-164">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-164">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="a9b06-165">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-165">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="a9b06-166">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-166">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="a9b06-167">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-167">Gets or sets a calculation mode for the height of the control.</span></span>                                                                          |
| <span data-ttu-id="a9b06-168">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-168">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="a9b06-169">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-169">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="a9b06-170">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-170">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="a9b06-171">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-171">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                |
| <span data-ttu-id="a9b06-172">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-172">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="a9b06-173">public int id()</span><span class="sxs-lookup"><span data-stu-id="a9b06-173">public int id()</span></span>                                                                                             | <span data-ttu-id="a9b06-174">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-174">Retrieves the ID of the control.</span></span>                                                                                                        |
| <span data-ttu-id="a9b06-175">public int iMEMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-175">public int iMEMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="a9b06-176">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="a9b06-176">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="a9b06-177">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-177">Retrieves a value that indicates whether the control is a container control.</span></span>                                                            |
| <span data-ttu-id="a9b06-178">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-178">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="a9b06-179">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-179">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="a9b06-180">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-180">Gets or sets the label for a control.</span></span>                                                                                                   |
| <span data-ttu-id="a9b06-181">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-181">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="a9b06-182">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-182">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="a9b06-183">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-183">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="a9b06-184">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-184">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="a9b06-185">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-185">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="a9b06-186">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-186">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="a9b06-187">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-187">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="a9b06-188">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-188">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="a9b06-189">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-189">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="a9b06-190">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-190">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="a9b06-191">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-191">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                         |
| <span data-ttu-id="a9b06-192">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-192">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="a9b06-193">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-193">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                         |
| <span data-ttu-id="a9b06-194">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-194">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="a9b06-195">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-195">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="a9b06-196">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-196">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="a9b06-197">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-197">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="a9b06-198">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-198">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="a9b06-199">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-199">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="a9b06-200">public int limitText(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-200">public int limitText(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="a9b06-201">public AutoMode limitTextMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-201">public AutoMode limitTextMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                         |
| <span data-ttu-id="a9b06-202">public int limitTextValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-202">public int limitTextValue(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="a9b06-203">public int lookupButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-203">public int lookupButton(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="a9b06-204">public boolean lookupOnly(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-204">public boolean lookupOnly(\[boolean value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="a9b06-205">public boolean mandatory(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-205">public boolean mandatory(\[boolean value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="a9b06-206">public boolean multiLine(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-206">public boolean multiLine(\[boolean value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="a9b06-207">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-207">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="a9b06-208">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-208">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="a9b06-209">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-209">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="a9b06-210">public boolean passwordStyle(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-210">public boolean passwordStyle(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="a9b06-211">public FieldId presenceDataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-211">public FieldId presenceDataField(\[FieldId value\])</span></span>                                                         |                                                                                                                                         |
| <span data-ttu-id="a9b06-212">public int presenceDataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-212">public int presenceDataSource(\[AnyType value\])</span></span>                                                            |                                                                                                                                         |
| <span data-ttu-id="a9b06-213">public int presenceIndicatorAllowed(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-213">public int presenceIndicatorAllowed(\[int value\])</span></span>                                                          |                                                                                                                                         |
| <span data-ttu-id="a9b06-214">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-214">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="a9b06-215">public boolean replaceOnLookup(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-215">public boolean replaceOnLookup(\[boolean value\])</span></span>                                                           |                                                                                                                                         |
| <span data-ttu-id="a9b06-216">public int searchAfterInput(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-216">public int searchAfterInput(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="a9b06-217">public int searchMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-217">public int searchMode(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="a9b06-218">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-218">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="a9b06-219">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-219">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="a9b06-220">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-220">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="a9b06-221">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-221">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>         |
| <span data-ttu-id="a9b06-222">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-222">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                         |
| <span data-ttu-id="a9b06-223">public str text(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-223">public str text(\[str value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="a9b06-224">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-224">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="a9b06-225">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-225">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="a9b06-226">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-226">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="a9b06-227">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-227">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="a9b06-228">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-228">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="a9b06-229">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-229">Sets or returns the underline property for the text in the control.</span></span>                                                                     |
| <span data-ttu-id="a9b06-230">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-230">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="a9b06-231">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-231">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="a9b06-232">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-232">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="a9b06-233">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-233">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="a9b06-234">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-234">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="a9b06-235">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-235">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="a9b06-236">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-236">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="a9b06-237">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-237">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="a9b06-238">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-238">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="a9b06-239">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-239">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="a9b06-240">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-240">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="a9b06-241">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-241">Gets or sets the calculation mode of the width of the control.</span></span>                                                                          |
| <span data-ttu-id="a9b06-242">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-242">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="a9b06-243">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-243">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="a9b06-244">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="a9b06-244">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="a9b06-245">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="a9b06-245">Method alignControl</span></span>

<span data-ttu-id="a9b06-246">コントロールを配置するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-246">Indicates whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="a9b06-247">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="a9b06-247">Parameters - alignControl</span></span>

<span data-ttu-id="a9b06-248">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-248">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="a9b06-249">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="a9b06-249">Return Value - alignControl</span></span>

<span data-ttu-id="a9b06-250">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="a9b06-250">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="a9b06-251">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="a9b06-251">Remarks - alignControl</span></span>

<span data-ttu-id="a9b06-252">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-252">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="a9b06-253">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="a9b06-253">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="a9b06-254">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="a9b06-254">Parameters - alignment</span></span>

<span data-ttu-id="a9b06-255">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-255">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="a9b06-256">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="a9b06-256">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="a9b06-257">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="a9b06-257">Method allowEdit</span></span>

<span data-ttu-id="a9b06-258">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-258">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="a9b06-259">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="a9b06-259">Parameters - allowEdit</span></span>

<span data-ttu-id="a9b06-260">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-260">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="a9b06-261">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="a9b06-261">Return Value - allowEdit</span></span>

<span data-ttu-id="a9b06-262">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a9b06-262">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="a9b06-263">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="a9b06-263">Remarks - allowEdit</span></span>

<span data-ttu-id="a9b06-264">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="a9b06-264">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="a9b06-265">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="a9b06-265">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="a9b06-266">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="a9b06-266">Parameters - arrayIndex</span></span>

<span data-ttu-id="a9b06-267">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-267">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="a9b06-268">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="a9b06-268">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="a9b06-269">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="a9b06-269">Method autoDeclaration</span></span>

<span data-ttu-id="a9b06-270">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-270">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="a9b06-271">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="a9b06-271">Parameters - autoDeclaration</span></span>

<span data-ttu-id="a9b06-272">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-272">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="a9b06-273">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="a9b06-273">Return Value - autoDeclaration</span></span>

<span data-ttu-id="a9b06-274">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a9b06-274">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="a9b06-275">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="a9b06-275">Remarks - autoDeclaration</span></span>

<span data-ttu-id="a9b06-276">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="a9b06-276">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="a9b06-277">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="a9b06-277">Method backgroundColor</span></span>

<span data-ttu-id="a9b06-278">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-278">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="a9b06-279">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="a9b06-279">Parameters - backgroundColor</span></span>

<span data-ttu-id="a9b06-280">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-280">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="a9b06-281">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="a9b06-281">Return Value - backgroundColor</span></span>

<span data-ttu-id="a9b06-282">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="a9b06-282">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="a9b06-283">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="a9b06-283">Remarks - backgroundColor</span></span>

<span data-ttu-id="a9b06-284">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-284">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="a9b06-285">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a9b06-285">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="a9b06-286">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="a9b06-286">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="a9b06-287">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="a9b06-287">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="a9b06-288">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="a9b06-288">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="a9b06-289">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="a9b06-289">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="a9b06-290">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="a9b06-290">Method backStyle</span></span>

<span data-ttu-id="a9b06-291">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-291">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="a9b06-292">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="a9b06-292">Parameters - backStyle</span></span>

<span data-ttu-id="a9b06-293">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-293">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="a9b06-294">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="a9b06-294">Return Value - backStyle</span></span>

<span data-ttu-id="a9b06-295">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="a9b06-295">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="a9b06-296">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="a9b06-296">Method bold</span></span>

<span data-ttu-id="a9b06-297">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-297">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="a9b06-298">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="a9b06-298">Parameters - bold</span></span>

<span data-ttu-id="a9b06-299">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-299">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="a9b06-300">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="a9b06-300">Return Value - bold</span></span>

<span data-ttu-id="a9b06-301">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="a9b06-301">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="a9b06-302">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="a9b06-302">Remarks - bold</span></span>

<span data-ttu-id="a9b06-303">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-303">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="a9b06-304">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-304">0 Use the default font weight.</span></span>
-   <span data-ttu-id="a9b06-305">1 シン。</span><span class="sxs-lookup"><span data-stu-id="a9b06-305">1 Thin.</span></span>
-   <span data-ttu-id="a9b06-306">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="a9b06-306">2 Extra-light.</span></span>
-   <span data-ttu-id="a9b06-307">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="a9b06-307">3 Light.</span></span>
-   <span data-ttu-id="a9b06-308">4 標準。</span><span class="sxs-lookup"><span data-stu-id="a9b06-308">4 Normal.</span></span>
-   <span data-ttu-id="a9b06-309">5 中。</span><span class="sxs-lookup"><span data-stu-id="a9b06-309">5 Medium.</span></span>
-   <span data-ttu-id="a9b06-310">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="a9b06-310">6 Semibold.</span></span>
-   <span data-ttu-id="a9b06-311">7 太字。</span><span class="sxs-lookup"><span data-stu-id="a9b06-311">7 Bold.</span></span>
-   <span data-ttu-id="a9b06-312">8 極太。</span><span class="sxs-lookup"><span data-stu-id="a9b06-312">8 Extra-bold.</span></span>
-   <span data-ttu-id="a9b06-313">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="a9b06-313">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="a9b06-314">メソッド border</span><span class="sxs-lookup"><span data-stu-id="a9b06-314">Method border</span></span>

<span data-ttu-id="a9b06-315">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-315">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="a9b06-316">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="a9b06-316">Parameters - border</span></span>

<span data-ttu-id="a9b06-317">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-317">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="a9b06-318">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="a9b06-318">Return Value - border</span></span>

<span data-ttu-id="a9b06-319">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="a9b06-319">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="a9b06-320">備考 - border</span><span class="sxs-lookup"><span data-stu-id="a9b06-320">Remarks - border</span></span>

<span data-ttu-id="a9b06-321">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-321">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="a9b06-322">値です。</span><span class="sxs-lookup"><span data-stu-id="a9b06-322">Value.</span></span> | <span data-ttu-id="a9b06-323">説明。</span><span class="sxs-lookup"><span data-stu-id="a9b06-323">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="a9b06-324">0</span><span class="sxs-lookup"><span data-stu-id="a9b06-324">0</span></span>      | <span data-ttu-id="a9b06-325">自動。</span><span class="sxs-lookup"><span data-stu-id="a9b06-325">Auto.</span></span>        |
| <span data-ttu-id="a9b06-326">1</span><span class="sxs-lookup"><span data-stu-id="a9b06-326">1</span></span>      | <span data-ttu-id="a9b06-327">3D。</span><span class="sxs-lookup"><span data-stu-id="a9b06-327">3D.</span></span>          |
| <span data-ttu-id="a9b06-328">2</span><span class="sxs-lookup"><span data-stu-id="a9b06-328">2</span></span>      | <span data-ttu-id="a9b06-329">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="a9b06-329">Single line.</span></span> |
| <span data-ttu-id="a9b06-330">3</span><span class="sxs-lookup"><span data-stu-id="a9b06-330">3</span></span>      | <span data-ttu-id="a9b06-331">均一。</span><span class="sxs-lookup"><span data-stu-id="a9b06-331">Flat.</span></span>        |
| <span data-ttu-id="a9b06-332">4</span><span class="sxs-lookup"><span data-stu-id="a9b06-332">4</span></span>      | <span data-ttu-id="a9b06-333">なし。</span><span class="sxs-lookup"><span data-stu-id="a9b06-333">None.</span></span>        |

## <a name="method-cachedatamethod"></a><span data-ttu-id="a9b06-334">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="a9b06-334">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="a9b06-335">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="a9b06-335">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="a9b06-336">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-336">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="a9b06-337">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="a9b06-337">Return Value - cacheDataMethod</span></span>

## <a name="method-changecase"></a><span data-ttu-id="a9b06-338">メソッド changeCase</span><span class="sxs-lookup"><span data-stu-id="a9b06-338">Method changeCase</span></span>

```xpp
public int changeCase([int value])
```

### <a name="parameters---changecase"></a><span data-ttu-id="a9b06-339">パラメーター - changeCase</span><span class="sxs-lookup"><span data-stu-id="a9b06-339">Parameters - changeCase</span></span>

<span data-ttu-id="a9b06-340">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-340">value</span></span>  

### <a name="return-value---changecase"></a><span data-ttu-id="a9b06-341">戻り値 - changeCase</span><span class="sxs-lookup"><span data-stu-id="a9b06-341">Return Value - changeCase</span></span>

## <a name="method-characterset"></a><span data-ttu-id="a9b06-342">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="a9b06-342">Method characterSet</span></span>

<span data-ttu-id="a9b06-343">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-343">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="a9b06-344">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="a9b06-344">Parameters - characterSet</span></span>

<span data-ttu-id="a9b06-345">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-345">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="a9b06-346">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="a9b06-346">Return Value - characterSet</span></span>

<span data-ttu-id="a9b06-347">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a9b06-347">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="a9b06-348">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="a9b06-348">Remarks - characterSet</span></span>

<span data-ttu-id="a9b06-349">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-349">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="a9b06-350">値です。</span><span class="sxs-lookup"><span data-stu-id="a9b06-350">Value.</span></span> | <span data-ttu-id="a9b06-351">説明。</span><span class="sxs-lookup"><span data-stu-id="a9b06-351">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="a9b06-352">0</span><span class="sxs-lookup"><span data-stu-id="a9b06-352">0</span></span>      | <span data-ttu-id="a9b06-353">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a9b06-353">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="a9b06-354">1</span><span class="sxs-lookup"><span data-stu-id="a9b06-354">1</span></span>      | <span data-ttu-id="a9b06-355">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a9b06-355">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="a9b06-356">2</span><span class="sxs-lookup"><span data-stu-id="a9b06-356">2</span></span>      | <span data-ttu-id="a9b06-357">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a9b06-357">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="a9b06-358">77</span><span class="sxs-lookup"><span data-stu-id="a9b06-358">77</span></span>     | <span data-ttu-id="a9b06-359">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a9b06-359">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="a9b06-360">128</span><span class="sxs-lookup"><span data-stu-id="a9b06-360">128</span></span>    | <span data-ttu-id="a9b06-361">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a9b06-361">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="a9b06-362">129</span><span class="sxs-lookup"><span data-stu-id="a9b06-362">129</span></span>    | <span data-ttu-id="a9b06-363">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a9b06-363">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="a9b06-364">134</span><span class="sxs-lookup"><span data-stu-id="a9b06-364">134</span></span>    | <span data-ttu-id="a9b06-365">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a9b06-365">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="a9b06-366">136</span><span class="sxs-lookup"><span data-stu-id="a9b06-366">136</span></span>    | <span data-ttu-id="a9b06-367">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a9b06-367">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="a9b06-368">161</span><span class="sxs-lookup"><span data-stu-id="a9b06-368">161</span></span>    | <span data-ttu-id="a9b06-369">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a9b06-369">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="a9b06-370">162</span><span class="sxs-lookup"><span data-stu-id="a9b06-370">162</span></span>    | <span data-ttu-id="a9b06-371">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a9b06-371">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="a9b06-372">163</span><span class="sxs-lookup"><span data-stu-id="a9b06-372">163</span></span>    | <span data-ttu-id="a9b06-373">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a9b06-373">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="a9b06-374">186</span><span class="sxs-lookup"><span data-stu-id="a9b06-374">186</span></span>    | <span data-ttu-id="a9b06-375">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a9b06-375">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="a9b06-376">204</span><span class="sxs-lookup"><span data-stu-id="a9b06-376">204</span></span>    | <span data-ttu-id="a9b06-377">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a9b06-377">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="a9b06-378">238</span><span class="sxs-lookup"><span data-stu-id="a9b06-378">238</span></span>    | <span data-ttu-id="a9b06-379">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a9b06-379">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="a9b06-380">255</span><span class="sxs-lookup"><span data-stu-id="a9b06-380">255</span></span>    | <span data-ttu-id="a9b06-381">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a9b06-381">OEM\_CHARSET</span></span>         |

<span data-ttu-id="a9b06-382">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="a9b06-382">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="a9b06-383">値です。</span><span class="sxs-lookup"><span data-stu-id="a9b06-383">Value.</span></span> | <span data-ttu-id="a9b06-384">説明。</span><span class="sxs-lookup"><span data-stu-id="a9b06-384">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="a9b06-385">130</span><span class="sxs-lookup"><span data-stu-id="a9b06-385">130</span></span>    | <span data-ttu-id="a9b06-386">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a9b06-386">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="a9b06-387">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="a9b06-387">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="a9b06-388">値です。</span><span class="sxs-lookup"><span data-stu-id="a9b06-388">Value.</span></span> | <span data-ttu-id="a9b06-389">説明。</span><span class="sxs-lookup"><span data-stu-id="a9b06-389">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="a9b06-390">177</span><span class="sxs-lookup"><span data-stu-id="a9b06-390">177</span></span>    | <span data-ttu-id="a9b06-391">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a9b06-391">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="a9b06-392">178</span><span class="sxs-lookup"><span data-stu-id="a9b06-392">178</span></span>    | <span data-ttu-id="a9b06-393">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a9b06-393">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="a9b06-394">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="a9b06-394">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="a9b06-395">値です。</span><span class="sxs-lookup"><span data-stu-id="a9b06-395">Value.</span></span> | <span data-ttu-id="a9b06-396">説明。</span><span class="sxs-lookup"><span data-stu-id="a9b06-396">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="a9b06-397">222</span><span class="sxs-lookup"><span data-stu-id="a9b06-397">222</span></span>    | <span data-ttu-id="a9b06-398">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="a9b06-398">THAI\_CHARSET</span></span> |

<span data-ttu-id="a9b06-399">既定の文字セットは、現在のシステム ロケールに基づく値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-399">The default character set is set to values that are based on the current system locale.</span></span> <span data-ttu-id="a9b06-400">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-400">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="a9b06-401">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9b06-401">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="a9b06-402">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="a9b06-402">Method colorScheme</span></span>

<span data-ttu-id="a9b06-403">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-403">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="a9b06-404">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="a9b06-404">Parameters - colorScheme</span></span>

<span data-ttu-id="a9b06-405">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-405">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="a9b06-406">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="a9b06-406">Return Value - colorScheme</span></span>

<span data-ttu-id="a9b06-407">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="a9b06-407">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="a9b06-408">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="a9b06-408">Remarks - colorScheme</span></span>

<span data-ttu-id="a9b06-409">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-409">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="a9b06-410">値です。</span><span class="sxs-lookup"><span data-stu-id="a9b06-410">Value.</span></span> | <span data-ttu-id="a9b06-411">スタイル。</span><span class="sxs-lookup"><span data-stu-id="a9b06-411">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="a9b06-412">0</span><span class="sxs-lookup"><span data-stu-id="a9b06-412">0</span></span>      | <span data-ttu-id="a9b06-413">既定。</span><span class="sxs-lookup"><span data-stu-id="a9b06-413">Default.</span></span>                      |
| <span data-ttu-id="a9b06-414">1</span><span class="sxs-lookup"><span data-stu-id="a9b06-414">1</span></span>      | <span data-ttu-id="a9b06-415">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="a9b06-415">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="a9b06-416">2</span><span class="sxs-lookup"><span data-stu-id="a9b06-416">2</span></span>      | <span data-ttu-id="a9b06-417">真の配色。</span><span class="sxs-lookup"><span data-stu-id="a9b06-417">The true-color scheme.</span></span>        |

## <a name="method-configurationkey"></a><span data-ttu-id="a9b06-418">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="a9b06-418">Method configurationKey</span></span>

<span data-ttu-id="a9b06-419">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-419">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="a9b06-420">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="a9b06-420">Parameters - configurationKey</span></span>

<span data-ttu-id="a9b06-421">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-421">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="a9b06-422">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="a9b06-422">Return Value - configurationKey</span></span>

<span data-ttu-id="a9b06-423">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="a9b06-423">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="a9b06-424">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="a9b06-424">Remarks - configurationKey</span></span>

<span data-ttu-id="a9b06-425">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-425">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="a9b06-426">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="a9b06-426">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="a9b06-427">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="a9b06-427">Method containerId</span></span>

<span data-ttu-id="a9b06-428">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-428">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="a9b06-429">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="a9b06-429">Return Value - containerId</span></span>

<span data-ttu-id="a9b06-430">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="a9b06-430">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="a9b06-431">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="a9b06-431">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="a9b06-432">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="a9b06-432">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="a9b06-433">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-433">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="a9b06-434">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="a9b06-434">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="a9b06-435">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="a9b06-435">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="a9b06-436">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="a9b06-436">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="a9b06-437">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-437">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="a9b06-438">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="a9b06-438">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="a9b06-439">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="a9b06-439">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="a9b06-440">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="a9b06-440">Parameters - dataField</span></span>

<span data-ttu-id="a9b06-441">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-441">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="a9b06-442">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="a9b06-442">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="a9b06-443">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="a9b06-443">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="a9b06-444">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="a9b06-444">Parameters - dataMethod</span></span>

<span data-ttu-id="a9b06-445">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-445">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="a9b06-446">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="a9b06-446">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="a9b06-447">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="a9b06-447">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="a9b06-448">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="a9b06-448">Parameters - dataRelationPath</span></span>

<span data-ttu-id="a9b06-449">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-449">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="a9b06-450">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="a9b06-450">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="a9b06-451">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="a9b06-451">Method dataSource</span></span>

<span data-ttu-id="a9b06-452">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-452">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="a9b06-453">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="a9b06-453">Parameters - dataSource</span></span>

<span data-ttu-id="a9b06-454">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-454">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="a9b06-455">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="a9b06-455">Return Value - dataSource</span></span>

<span data-ttu-id="a9b06-456">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="a9b06-456">The identifier of the data source that will be used.</span></span>

## <a name="method-direction"></a><span data-ttu-id="a9b06-457">メソッド direction</span><span class="sxs-lookup"><span data-stu-id="a9b06-457">Method direction</span></span>

```xpp
public int direction([int value])
```

### <a name="parameters---direction"></a><span data-ttu-id="a9b06-458">パラメーター - direction</span><span class="sxs-lookup"><span data-stu-id="a9b06-458">Parameters - direction</span></span>

<span data-ttu-id="a9b06-459">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-459">value</span></span>  

### <a name="return-value---direction"></a><span data-ttu-id="a9b06-460">戻り値 - direction</span><span class="sxs-lookup"><span data-stu-id="a9b06-460">Return Value - direction</span></span>

## <a name="method-displayheight"></a><span data-ttu-id="a9b06-461">メソッド displayHeight</span><span class="sxs-lookup"><span data-stu-id="a9b06-461">Method displayHeight</span></span>

```xpp
public int displayHeight([int value], [AutoMode mode])
```

### <a name="parameters---displayheight"></a><span data-ttu-id="a9b06-462">パラメーター - displayHeight</span><span class="sxs-lookup"><span data-stu-id="a9b06-462">Parameters - displayHeight</span></span>

<span data-ttu-id="a9b06-463">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-463">value</span></span>  

<!-- -->

<span data-ttu-id="a9b06-464">モード</span><span class="sxs-lookup"><span data-stu-id="a9b06-464">mode</span></span>  

### <a name="return-value---displayheight"></a><span data-ttu-id="a9b06-465">戻り値 - displayHeight</span><span class="sxs-lookup"><span data-stu-id="a9b06-465">Return Value - displayHeight</span></span>

## <a name="method-displayheightmode"></a><span data-ttu-id="a9b06-466">メソッド displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-466">Method displayHeightMode</span></span>

```xpp
public AutoMode displayHeightMode([AutoMode mode])
```

### <a name="parameters---displayheightmode"></a><span data-ttu-id="a9b06-467">パラメーター - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-467">Parameters - displayHeightMode</span></span>

<span data-ttu-id="a9b06-468">モード</span><span class="sxs-lookup"><span data-stu-id="a9b06-468">mode</span></span>  

### <a name="return-value---displayheightmode"></a><span data-ttu-id="a9b06-469">戻り値 - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-469">Return Value - displayHeightMode</span></span>

## <a name="method-displayheightvalue"></a><span data-ttu-id="a9b06-470">メソッド displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-470">Method displayHeightValue</span></span>

```xpp
public int displayHeightValue([int value])
```

### <a name="parameters---displayheightvalue"></a><span data-ttu-id="a9b06-471">パラメーター - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-471">Parameters - displayHeightValue</span></span>

<span data-ttu-id="a9b06-472">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-472">value</span></span>  

### <a name="return-value---displayheightvalue"></a><span data-ttu-id="a9b06-473">戻り値 - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-473">Return Value - displayHeightValue</span></span>

## <a name="method-displaylength"></a><span data-ttu-id="a9b06-474">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="a9b06-474">Method displayLength</span></span>

```xpp
public int displayLength([int value], [AutoMode mode])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="a9b06-475">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="a9b06-475">Parameters - displayLength</span></span>

<span data-ttu-id="a9b06-476">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-476">value</span></span>  

<!-- -->

<span data-ttu-id="a9b06-477">モード</span><span class="sxs-lookup"><span data-stu-id="a9b06-477">mode</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="a9b06-478">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="a9b06-478">Return Value - displayLength</span></span>

## <a name="method-displaylengthmode"></a><span data-ttu-id="a9b06-479">メソッド displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-479">Method displayLengthMode</span></span>

```xpp
public AutoMode displayLengthMode([AutoMode mode])
```

### <a name="parameters---displaylengthmode"></a><span data-ttu-id="a9b06-480">パラメーター - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-480">Parameters - displayLengthMode</span></span>

<span data-ttu-id="a9b06-481">モード</span><span class="sxs-lookup"><span data-stu-id="a9b06-481">mode</span></span>  

### <a name="return-value---displaylengthmode"></a><span data-ttu-id="a9b06-482">戻り値 - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-482">Return Value - displayLengthMode</span></span>

## <a name="method-displaylengthvalue"></a><span data-ttu-id="a9b06-483">メソッド displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-483">Method displayLengthValue</span></span>

```xpp
public int displayLengthValue([int value])
```

### <a name="parameters---displaylengthvalue"></a><span data-ttu-id="a9b06-484">パラメーター - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-484">Parameters - displayLengthValue</span></span>

<span data-ttu-id="a9b06-485">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-485">value</span></span>  

### <a name="return-value---displaylengthvalue"></a><span data-ttu-id="a9b06-486">戻り値 - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-486">Return Value - displayLengthValue</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="a9b06-487">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="a9b06-487">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="a9b06-488">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="a9b06-488">Parameters - displayTarget</span></span>

<span data-ttu-id="a9b06-489">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-489">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="a9b06-490">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="a9b06-490">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="a9b06-491">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="a9b06-491">Method dragDrop</span></span>

<span data-ttu-id="a9b06-492">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-492">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="a9b06-493">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="a9b06-493">Parameters - dragDrop</span></span>

<span data-ttu-id="a9b06-494">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-494">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="a9b06-495">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="a9b06-495">Return Value - dragDrop</span></span>

<span data-ttu-id="a9b06-496">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="a9b06-496">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="a9b06-497">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="a9b06-497">Method enabled</span></span>

<span data-ttu-id="a9b06-498">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-498">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="a9b06-499">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="a9b06-499">Parameters - enabled</span></span>

<span data-ttu-id="a9b06-500">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-500">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="a9b06-501">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="a9b06-501">Return Value - enabled</span></span>

<span data-ttu-id="a9b06-502">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a9b06-502">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="a9b06-503">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="a9b06-503">Remarks - enabled</span></span>

<span data-ttu-id="a9b06-504">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-504">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="a9b06-505">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-505">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="a9b06-506">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-506">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="a9b06-507">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="a9b06-507">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="a9b06-508">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="a9b06-508">Parameters - extendedDataType</span></span>

<span data-ttu-id="a9b06-509">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-509">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="a9b06-510">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="a9b06-510">Return Value - extendedDataType</span></span>

## <a name="method-fasttabsummary"></a><span data-ttu-id="a9b06-511">メソッド fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="a9b06-511">Method fastTabSummary</span></span>

```xpp
public int fastTabSummary([int value])
```

### <a name="parameters---fasttabsummary"></a><span data-ttu-id="a9b06-512">パラメーター - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="a9b06-512">Parameters - fastTabSummary</span></span>

<span data-ttu-id="a9b06-513">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-513">value</span></span>  

### <a name="return-value---fasttabsummary"></a><span data-ttu-id="a9b06-514">戻り値 - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="a9b06-514">Return Value - fastTabSummary</span></span>

## <a name="method-font"></a><span data-ttu-id="a9b06-515">メソッド font</span><span class="sxs-lookup"><span data-stu-id="a9b06-515">Method font</span></span>

<span data-ttu-id="a9b06-516">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-516">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="a9b06-517">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="a9b06-517">Parameters - font</span></span>

<span data-ttu-id="a9b06-518">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-518">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="a9b06-519">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="a9b06-519">Return Value - font</span></span>

<span data-ttu-id="a9b06-520">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="a9b06-520">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="a9b06-521">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="a9b06-521">Method fontSize</span></span>

<span data-ttu-id="a9b06-522">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-522">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="a9b06-523">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="a9b06-523">Parameters - fontSize</span></span>

<span data-ttu-id="a9b06-524">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-524">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="a9b06-525">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="a9b06-525">Return Value - fontSize</span></span>

<span data-ttu-id="a9b06-526">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="a9b06-526">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="a9b06-527">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="a9b06-527">Method foregroundColor</span></span>

<span data-ttu-id="a9b06-528">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-528">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="a9b06-529">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="a9b06-529">Parameters - foregroundColor</span></span>

<span data-ttu-id="a9b06-530">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-530">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="a9b06-531">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="a9b06-531">Return Value - foregroundColor</span></span>

<span data-ttu-id="a9b06-532">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="a9b06-532">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="a9b06-533">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="a9b06-533">Remarks - foregroundColor</span></span>

<span data-ttu-id="a9b06-534">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-534">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="a9b06-535">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a9b06-535">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="a9b06-536">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="a9b06-536">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="a9b06-537">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="a9b06-537">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="a9b06-538">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="a9b06-538">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="a9b06-539">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="a9b06-539">The maximum value for a single byte is 255.</span></span>

## <a name="method-height"></a><span data-ttu-id="a9b06-540">メソッド height</span><span class="sxs-lookup"><span data-stu-id="a9b06-540">Method height</span></span>

<span data-ttu-id="a9b06-541">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-541">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="a9b06-542">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="a9b06-542">Parameters - height</span></span>

<span data-ttu-id="a9b06-543">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-543">value</span></span>  

<!-- -->

<span data-ttu-id="a9b06-544">モード</span><span class="sxs-lookup"><span data-stu-id="a9b06-544">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="a9b06-545">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="a9b06-545">Return Value - height</span></span>

<span data-ttu-id="a9b06-546">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="a9b06-546">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="a9b06-547">備考 - height</span><span class="sxs-lookup"><span data-stu-id="a9b06-547">Remarks - height</span></span>

<span data-ttu-id="a9b06-548">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-548">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="a9b06-549">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="a9b06-549">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="a9b06-550">モード。</span><span class="sxs-lookup"><span data-stu-id="a9b06-550">Mode.</span></span>            | <span data-ttu-id="a9b06-551">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="a9b06-551">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9b06-552">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="a9b06-552">-1 Exact.</span></span>        | <span data-ttu-id="a9b06-553">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-553">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="a9b06-554">0 自動。</span><span class="sxs-lookup"><span data-stu-id="a9b06-554">0 Auto.</span></span>          | <span data-ttu-id="a9b06-555">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-555">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="a9b06-556">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="a9b06-556">1 Column height.</span></span> | <span data-ttu-id="a9b06-557">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="a9b06-557">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="a9b06-558">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-558">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="a9b06-559">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-559">Method heightMode</span></span>

<span data-ttu-id="a9b06-560">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-560">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="a9b06-561">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-561">Parameters - heightMode</span></span>

<span data-ttu-id="a9b06-562">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-562">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="a9b06-563">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-563">Return Value - heightMode</span></span>

<span data-ttu-id="a9b06-564">計算モード。</span><span class="sxs-lookup"><span data-stu-id="a9b06-564">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="a9b06-565">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-565">Remarks - heightMode</span></span>

<span data-ttu-id="a9b06-566">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="a9b06-566">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="a9b06-567">モード。</span><span class="sxs-lookup"><span data-stu-id="a9b06-567">Mode.</span></span>          | <span data-ttu-id="a9b06-568">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="a9b06-568">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9b06-569">正確。</span><span class="sxs-lookup"><span data-stu-id="a9b06-569">Exact.</span></span>         | <span data-ttu-id="a9b06-570">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-570">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="a9b06-571">自動。</span><span class="sxs-lookup"><span data-stu-id="a9b06-571">Auto.</span></span>          | <span data-ttu-id="a9b06-572">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-572">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="a9b06-573">列の高さ</span><span class="sxs-lookup"><span data-stu-id="a9b06-573">Column height.</span></span> | <span data-ttu-id="a9b06-574">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="a9b06-574">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="a9b06-575">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="a9b06-575">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="a9b06-576">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-576">Method heightValue</span></span>

<span data-ttu-id="a9b06-577">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-577">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="a9b06-578">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-578">Parameters - heightValue</span></span>

<span data-ttu-id="a9b06-579">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-579">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="a9b06-580">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-580">Return Value - heightValue</span></span>

<span data-ttu-id="a9b06-581">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="a9b06-581">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="a9b06-582">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-582">Remarks - heightValue</span></span>

<span data-ttu-id="a9b06-583">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="a9b06-583">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="a9b06-584">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="a9b06-584">Method helpText</span></span>

<span data-ttu-id="a9b06-585">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-585">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="a9b06-586">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="a9b06-586">Parameters - helpText</span></span>

<span data-ttu-id="a9b06-587">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-587">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="a9b06-588">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="a9b06-588">Return Value - helpText</span></span>

<span data-ttu-id="a9b06-589">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="a9b06-589">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="a9b06-590">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="a9b06-590">Remarks - helpText</span></span>

<span data-ttu-id="a9b06-591">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-591">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="a9b06-592">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="a9b06-592">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="a9b06-593">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="a9b06-593">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="a9b06-594">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="a9b06-594">Parameters - hierarchyParent</span></span>

<span data-ttu-id="a9b06-595">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-595">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="a9b06-596">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="a9b06-596">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="a9b06-597">メソッド id</span><span class="sxs-lookup"><span data-stu-id="a9b06-597">Method id</span></span>

<span data-ttu-id="a9b06-598">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-598">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="a9b06-599">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="a9b06-599">Return Value - id</span></span>

<span data-ttu-id="a9b06-600">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="a9b06-600">The ID of the control.</span></span>

## <a name="method-imemode"></a><span data-ttu-id="a9b06-601">メソッド iMEMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-601">Method iMEMode</span></span>

```xpp
public int iMEMode([int value])
```

### <a name="parameters---imemode"></a><span data-ttu-id="a9b06-602">パラメーター - iMEMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-602">Parameters - iMEMode</span></span>

<span data-ttu-id="a9b06-603">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-603">value</span></span>  

### <a name="return-value---imemode"></a><span data-ttu-id="a9b06-604">戻り値 - iMEMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-604">Return Value - iMEMode</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="a9b06-605">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="a9b06-605">Method isContainer</span></span>

<span data-ttu-id="a9b06-606">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-606">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="a9b06-607">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="a9b06-607">Return Value - isContainer</span></span>

<span data-ttu-id="a9b06-608">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="a9b06-608">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-italic"></a><span data-ttu-id="a9b06-609">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="a9b06-609">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="a9b06-610">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="a9b06-610">Parameters - italic</span></span>

<span data-ttu-id="a9b06-611">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-611">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="a9b06-612">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="a9b06-612">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="a9b06-613">メソッド label</span><span class="sxs-lookup"><span data-stu-id="a9b06-613">Method label</span></span>

<span data-ttu-id="a9b06-614">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-614">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="a9b06-615">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="a9b06-615">Parameters - label</span></span>

<span data-ttu-id="a9b06-616">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-616">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="a9b06-617">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="a9b06-617">Return Value - label</span></span>

<span data-ttu-id="a9b06-618">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="a9b06-618">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="a9b06-619">備考 - label</span><span class="sxs-lookup"><span data-stu-id="a9b06-619">Remarks - label</span></span>

<span data-ttu-id="a9b06-620">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-620">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="a9b06-621">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="a9b06-621">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="a9b06-622">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="a9b06-622">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="a9b06-623">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="a9b06-623">Parameters - labelAlignment</span></span>

<span data-ttu-id="a9b06-624">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-624">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="a9b06-625">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="a9b06-625">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="a9b06-626">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="a9b06-626">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="a9b06-627">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="a9b06-627">Parameters - labelBold</span></span>

<span data-ttu-id="a9b06-628">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-628">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="a9b06-629">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="a9b06-629">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="a9b06-630">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="a9b06-630">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="a9b06-631">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="a9b06-631">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="a9b06-632">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-632">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="a9b06-633">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="a9b06-633">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="a9b06-634">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="a9b06-634">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="a9b06-635">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="a9b06-635">Parameters - labelFont</span></span>

<span data-ttu-id="a9b06-636">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-636">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="a9b06-637">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="a9b06-637">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="a9b06-638">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="a9b06-638">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="a9b06-639">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="a9b06-639">Parameters - labelFontSize</span></span>

<span data-ttu-id="a9b06-640">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-640">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="a9b06-641">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="a9b06-641">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="a9b06-642">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="a9b06-642">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="a9b06-643">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="a9b06-643">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="a9b06-644">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-644">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="a9b06-645">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="a9b06-645">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="a9b06-646">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="a9b06-646">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="a9b06-647">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="a9b06-647">Parameters - labelGuide</span></span>

<span data-ttu-id="a9b06-648">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-648">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="a9b06-649">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="a9b06-649">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="a9b06-650">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="a9b06-650">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="a9b06-651">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="a9b06-651">Parameters - labelHeight</span></span>

<span data-ttu-id="a9b06-652">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-652">value</span></span>  

<!-- -->

<span data-ttu-id="a9b06-653">モード</span><span class="sxs-lookup"><span data-stu-id="a9b06-653">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="a9b06-654">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="a9b06-654">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="a9b06-655">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-655">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="a9b06-656">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-656">Parameters - labelHeightMode</span></span>

<span data-ttu-id="a9b06-657">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-657">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="a9b06-658">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-658">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="a9b06-659">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-659">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="a9b06-660">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-660">Parameters - labelHeightValue</span></span>

<span data-ttu-id="a9b06-661">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-661">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="a9b06-662">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-662">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="a9b06-663">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="a9b06-663">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="a9b06-664">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="a9b06-664">Parameters - labelItalic</span></span>

<span data-ttu-id="a9b06-665">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-665">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="a9b06-666">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="a9b06-666">Return Value - labelItalic</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="a9b06-667">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="a9b06-667">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="a9b06-668">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="a9b06-668">Parameters - labelPosition</span></span>

<span data-ttu-id="a9b06-669">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-669">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="a9b06-670">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="a9b06-670">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="a9b06-671">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="a9b06-671">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="a9b06-672">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="a9b06-672">Parameters - labelUnderline</span></span>

<span data-ttu-id="a9b06-673">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-673">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="a9b06-674">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="a9b06-674">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="a9b06-675">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="a9b06-675">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="a9b06-676">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="a9b06-676">Parameters - labelWidth</span></span>

<span data-ttu-id="a9b06-677">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-677">value</span></span>  

<!-- -->

<span data-ttu-id="a9b06-678">モード</span><span class="sxs-lookup"><span data-stu-id="a9b06-678">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="a9b06-679">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="a9b06-679">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="a9b06-680">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-680">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="a9b06-681">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-681">Parameters - labelWidthMode</span></span>

<span data-ttu-id="a9b06-682">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-682">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="a9b06-683">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-683">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="a9b06-684">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-684">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="a9b06-685">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-685">Parameters - labelWidthValue</span></span>

<span data-ttu-id="a9b06-686">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-686">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="a9b06-687">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-687">Return Value - labelWidthValue</span></span>

## <a name="method-left"></a><span data-ttu-id="a9b06-688">メソッド left</span><span class="sxs-lookup"><span data-stu-id="a9b06-688">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="a9b06-689">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="a9b06-689">Parameters - left</span></span>

<span data-ttu-id="a9b06-690">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-690">value</span></span>  

<!-- -->

<span data-ttu-id="a9b06-691">モード</span><span class="sxs-lookup"><span data-stu-id="a9b06-691">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="a9b06-692">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="a9b06-692">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="a9b06-693">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-693">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="a9b06-694">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-694">Parameters - leftMode</span></span>

<span data-ttu-id="a9b06-695">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-695">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="a9b06-696">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-696">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="a9b06-697">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-697">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="a9b06-698">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-698">Parameters - leftValue</span></span>

<span data-ttu-id="a9b06-699">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-699">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="a9b06-700">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-700">Return Value - leftValue</span></span>

## <a name="method-limittext"></a><span data-ttu-id="a9b06-701">メソッド limitText</span><span class="sxs-lookup"><span data-stu-id="a9b06-701">Method limitText</span></span>

```xpp
public int limitText([int value], [AutoMode mode])
```

### <a name="parameters---limittext"></a><span data-ttu-id="a9b06-702">パラメーター - limitText</span><span class="sxs-lookup"><span data-stu-id="a9b06-702">Parameters - limitText</span></span>

<span data-ttu-id="a9b06-703">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-703">value</span></span>  

<!-- -->

<span data-ttu-id="a9b06-704">モード</span><span class="sxs-lookup"><span data-stu-id="a9b06-704">mode</span></span>  

### <a name="return-value---limittext"></a><span data-ttu-id="a9b06-705">戻り値 - limitText</span><span class="sxs-lookup"><span data-stu-id="a9b06-705">Return Value - limitText</span></span>

## <a name="method-limittextmode"></a><span data-ttu-id="a9b06-706">メソッド limitTextMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-706">Method limitTextMode</span></span>

```xpp
public AutoMode limitTextMode([AutoMode mode])
```

### <a name="parameters---limittextmode"></a><span data-ttu-id="a9b06-707">パラメーター - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-707">Parameters - limitTextMode</span></span>

<span data-ttu-id="a9b06-708">モード</span><span class="sxs-lookup"><span data-stu-id="a9b06-708">mode</span></span>  

### <a name="return-value---limittextmode"></a><span data-ttu-id="a9b06-709">戻り値 - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-709">Return Value - limitTextMode</span></span>

## <a name="method-limittextvalue"></a><span data-ttu-id="a9b06-710">メソッド limitTextValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-710">Method limitTextValue</span></span>

```xpp
public int limitTextValue([int value])
```

### <a name="parameters---limittextvalue"></a><span data-ttu-id="a9b06-711">パラメーター - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-711">Parameters - limitTextValue</span></span>

<span data-ttu-id="a9b06-712">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-712">value</span></span>  

### <a name="return-value---limittextvalue"></a><span data-ttu-id="a9b06-713">戻り値 - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-713">Return Value - limitTextValue</span></span>

## <a name="method-lookupbutton"></a><span data-ttu-id="a9b06-714">メソッド lookupButton</span><span class="sxs-lookup"><span data-stu-id="a9b06-714">Method lookupButton</span></span>

```xpp
public int lookupButton([int value])
```

### <a name="parameters---lookupbutton"></a><span data-ttu-id="a9b06-715">パラメーター - lookupButton</span><span class="sxs-lookup"><span data-stu-id="a9b06-715">Parameters - lookupButton</span></span>

<span data-ttu-id="a9b06-716">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-716">value</span></span>  

### <a name="return-value---lookupbutton"></a><span data-ttu-id="a9b06-717">戻り値 - lookupButton</span><span class="sxs-lookup"><span data-stu-id="a9b06-717">Return Value - lookupButton</span></span>

## <a name="method-lookuponly"></a><span data-ttu-id="a9b06-718">メソッド lookupOnly</span><span class="sxs-lookup"><span data-stu-id="a9b06-718">Method lookupOnly</span></span>

```xpp
public boolean lookupOnly([boolean value])
```

### <a name="parameters---lookuponly"></a><span data-ttu-id="a9b06-719">パラメーター - lookupOnly</span><span class="sxs-lookup"><span data-stu-id="a9b06-719">Parameters - lookupOnly</span></span>

<span data-ttu-id="a9b06-720">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-720">value</span></span>  

### <a name="return-value---lookuponly"></a><span data-ttu-id="a9b06-721">戻り値 - lookupOnly</span><span class="sxs-lookup"><span data-stu-id="a9b06-721">Return Value - lookupOnly</span></span>

## <a name="method-mandatory"></a><span data-ttu-id="a9b06-722">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="a9b06-722">Method mandatory</span></span>

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a><span data-ttu-id="a9b06-723">パラメーター - mandatory</span><span class="sxs-lookup"><span data-stu-id="a9b06-723">Parameters - mandatory</span></span>

<span data-ttu-id="a9b06-724">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-724">value</span></span>  

### <a name="return-value---mandatory"></a><span data-ttu-id="a9b06-725">戻り値 - mandatory</span><span class="sxs-lookup"><span data-stu-id="a9b06-725">Return Value - mandatory</span></span>

## <a name="method-multiline"></a><span data-ttu-id="a9b06-726">メソッド multiLine</span><span class="sxs-lookup"><span data-stu-id="a9b06-726">Method multiLine</span></span>

```xpp
public boolean multiLine([boolean value])
```

### <a name="parameters---multiline"></a><span data-ttu-id="a9b06-727">パラメーター - multiLine</span><span class="sxs-lookup"><span data-stu-id="a9b06-727">Parameters - multiLine</span></span>

<span data-ttu-id="a9b06-728">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-728">value</span></span>  

### <a name="return-value---multiline"></a><span data-ttu-id="a9b06-729">戻り値 - multiLine</span><span class="sxs-lookup"><span data-stu-id="a9b06-729">Return Value - multiLine</span></span>

## <a name="method-name"></a><span data-ttu-id="a9b06-730">メソッド名</span><span class="sxs-lookup"><span data-stu-id="a9b06-730">Method name</span></span>

<span data-ttu-id="a9b06-731">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-731">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="a9b06-732">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="a9b06-732">Parameters - name</span></span>

<span data-ttu-id="a9b06-733">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-733">value</span></span>  
<span data-ttu-id="a9b06-734">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="a9b06-734">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="a9b06-735">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="a9b06-735">Return Value - name</span></span>

<span data-ttu-id="a9b06-736">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="a9b06-736">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="a9b06-737">備考 - name</span><span class="sxs-lookup"><span data-stu-id="a9b06-737">Remarks - name</span></span>

<span data-ttu-id="a9b06-738">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9b06-738">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="a9b06-739">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9b06-739">It must start with a letter.</span></span>
-   <span data-ttu-id="a9b06-740">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="a9b06-740">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="a9b06-741">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-741">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="a9b06-742">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="a9b06-742">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="a9b06-743">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="a9b06-743">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="a9b06-744">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="a9b06-744">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="a9b06-745">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="a9b06-745">Parameters - neededPermission</span></span>

<span data-ttu-id="a9b06-746">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-746">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="a9b06-747">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="a9b06-747">Return Value - neededPermission</span></span>

## <a name="method-passwordstyle"></a><span data-ttu-id="a9b06-748">メソッド passwordStyle</span><span class="sxs-lookup"><span data-stu-id="a9b06-748">Method passwordStyle</span></span>

```xpp
public boolean passwordStyle([boolean value])
```

### <a name="parameters---passwordstyle"></a><span data-ttu-id="a9b06-749">パラメーター - passwordStyle</span><span class="sxs-lookup"><span data-stu-id="a9b06-749">Parameters - passwordStyle</span></span>

<span data-ttu-id="a9b06-750">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-750">value</span></span>  

### <a name="return-value---passwordstyle"></a><span data-ttu-id="a9b06-751">戻り値 - passwordStyle</span><span class="sxs-lookup"><span data-stu-id="a9b06-751">Return Value - passwordStyle</span></span>

## <a name="method-presencedatafield"></a><span data-ttu-id="a9b06-752">メソッド presenceDataField</span><span class="sxs-lookup"><span data-stu-id="a9b06-752">Method presenceDataField</span></span>

```xpp
public FieldId presenceDataField([FieldId value])
```

### <a name="parameters---presencedatafield"></a><span data-ttu-id="a9b06-753">パラメーター - presenceDataField</span><span class="sxs-lookup"><span data-stu-id="a9b06-753">Parameters - presenceDataField</span></span>

<span data-ttu-id="a9b06-754">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-754">value</span></span>  

### <a name="return-value---presencedatafield"></a><span data-ttu-id="a9b06-755">戻り値 - presenceDataField</span><span class="sxs-lookup"><span data-stu-id="a9b06-755">Return Value - presenceDataField</span></span>

## <a name="method-presencedatasource"></a><span data-ttu-id="a9b06-756">メソッド presenceDataSource</span><span class="sxs-lookup"><span data-stu-id="a9b06-756">Method presenceDataSource</span></span>

```xpp
public int presenceDataSource([AnyType value])
```

### <a name="parameters---presencedatasource"></a><span data-ttu-id="a9b06-757">パラメーター - presenceDataSource</span><span class="sxs-lookup"><span data-stu-id="a9b06-757">Parameters - presenceDataSource</span></span>

<span data-ttu-id="a9b06-758">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-758">value</span></span>  

### <a name="return-value---presencedatasource"></a><span data-ttu-id="a9b06-759">戻り値 - presenceDataSource</span><span class="sxs-lookup"><span data-stu-id="a9b06-759">Return Value - presenceDataSource</span></span>

## <a name="method-presenceindicatorallowed"></a><span data-ttu-id="a9b06-760">メソッド presenceIndicatorAllowed</span><span class="sxs-lookup"><span data-stu-id="a9b06-760">Method presenceIndicatorAllowed</span></span>

```xpp
public int presenceIndicatorAllowed([int value])
```

### <a name="parameters---presenceindicatorallowed"></a><span data-ttu-id="a9b06-761">パラメーター - presenceIndicatorAllowed</span><span class="sxs-lookup"><span data-stu-id="a9b06-761">Parameters - presenceIndicatorAllowed</span></span>

<span data-ttu-id="a9b06-762">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-762">value</span></span>  

### <a name="return-value---presenceindicatorallowed"></a><span data-ttu-id="a9b06-763">戻り値 - presenceIndicatorAllowed</span><span class="sxs-lookup"><span data-stu-id="a9b06-763">Return Value - presenceIndicatorAllowed</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="a9b06-764">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="a9b06-764">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="a9b06-765">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="a9b06-765">Parameters - promptrect</span></span>

<span data-ttu-id="a9b06-766">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-766">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="a9b06-767">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="a9b06-767">Return Value - promptrect</span></span>

## <a name="method-replaceonlookup"></a><span data-ttu-id="a9b06-768">メソッド replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="a9b06-768">Method replaceOnLookup</span></span>

```xpp
public boolean replaceOnLookup([boolean value])
```

### <a name="parameters---replaceonlookup"></a><span data-ttu-id="a9b06-769">パラメーター - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="a9b06-769">Parameters - replaceOnLookup</span></span>

<span data-ttu-id="a9b06-770">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-770">value</span></span>  

### <a name="return-value---replaceonlookup"></a><span data-ttu-id="a9b06-771">戻り値 - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="a9b06-771">Return Value - replaceOnLookup</span></span>

## <a name="method-searchafterinput"></a><span data-ttu-id="a9b06-772">メソッド searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="a9b06-772">Method searchAfterInput</span></span>

```xpp
public int searchAfterInput([int value])
```

### <a name="parameters---searchafterinput"></a><span data-ttu-id="a9b06-773">パラメーター - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="a9b06-773">Parameters - searchAfterInput</span></span>

<span data-ttu-id="a9b06-774">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-774">value</span></span>  

### <a name="return-value---searchafterinput"></a><span data-ttu-id="a9b06-775">戻り値 - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="a9b06-775">Return Value - searchAfterInput</span></span>

## <a name="method-searchmode"></a><span data-ttu-id="a9b06-776">メソッド searchMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-776">Method searchMode</span></span>

```xpp
public int searchMode([int value])
```

### <a name="parameters---searchmode"></a><span data-ttu-id="a9b06-777">パラメーター - searchMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-777">Parameters - searchMode</span></span>

<span data-ttu-id="a9b06-778">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-778">value</span></span>  

### <a name="return-value---searchmode"></a><span data-ttu-id="a9b06-779">戻り値 - searchMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-779">Return Value - searchMode</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="a9b06-780">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="a9b06-780">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="a9b06-781">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="a9b06-781">Parameters - securityKey</span></span>

<span data-ttu-id="a9b06-782">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-782">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="a9b06-783">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="a9b06-783">Return Value - securityKey</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="a9b06-784">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="a9b06-784">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="a9b06-785">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="a9b06-785">Parameters - showLabel</span></span>

<span data-ttu-id="a9b06-786">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-786">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="a9b06-787">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="a9b06-787">Return Value - showLabel</span></span>

## <a name="method-skip"></a><span data-ttu-id="a9b06-788">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="a9b06-788">Method skip</span></span>

<span data-ttu-id="a9b06-789">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-789">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="a9b06-790">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="a9b06-790">Parameters - skip</span></span>

<span data-ttu-id="a9b06-791">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-791">value</span></span>  
<span data-ttu-id="a9b06-792">コントロールの skip プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="a9b06-792">The value to assign to the skip property of the control.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="a9b06-793">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="a9b06-793">Return Value - skip</span></span>

<span data-ttu-id="a9b06-794">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a9b06-794">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-style"></a><span data-ttu-id="a9b06-795">メソッド style</span><span class="sxs-lookup"><span data-stu-id="a9b06-795">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="a9b06-796">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="a9b06-796">Parameters - style</span></span>

<span data-ttu-id="a9b06-797">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-797">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="a9b06-798">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="a9b06-798">Return Value - style</span></span>

## <a name="method-text"></a><span data-ttu-id="a9b06-799">メソッド text</span><span class="sxs-lookup"><span data-stu-id="a9b06-799">Method text</span></span>

```xpp
public str text([str value])
```

### <a name="parameters---text"></a><span data-ttu-id="a9b06-800">パラメーター - text</span><span class="sxs-lookup"><span data-stu-id="a9b06-800">Parameters - text</span></span>

<span data-ttu-id="a9b06-801">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-801">value</span></span>  

### <a name="return-value---text"></a><span data-ttu-id="a9b06-802">戻り値 - text</span><span class="sxs-lookup"><span data-stu-id="a9b06-802">Return Value - text</span></span>

## <a name="method-top"></a><span data-ttu-id="a9b06-803">メソッド top</span><span class="sxs-lookup"><span data-stu-id="a9b06-803">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="a9b06-804">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="a9b06-804">Parameters - top</span></span>

<span data-ttu-id="a9b06-805">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-805">value</span></span>  

<!-- -->

<span data-ttu-id="a9b06-806">モード</span><span class="sxs-lookup"><span data-stu-id="a9b06-806">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="a9b06-807">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="a9b06-807">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="a9b06-808">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-808">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="a9b06-809">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-809">Parameters - topMode</span></span>

<span data-ttu-id="a9b06-810">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-810">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="a9b06-811">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-811">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="a9b06-812">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-812">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="a9b06-813">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-813">Parameters - topValue</span></span>

<span data-ttu-id="a9b06-814">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-814">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="a9b06-815">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-815">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="a9b06-816">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="a9b06-816">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="a9b06-817">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="a9b06-817">Parameters - type</span></span>

<span data-ttu-id="a9b06-818">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-818">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="a9b06-819">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="a9b06-819">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="a9b06-820">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="a9b06-820">Method underline</span></span>

<span data-ttu-id="a9b06-821">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-821">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="a9b06-822">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="a9b06-822">Parameters - underline</span></span>

<span data-ttu-id="a9b06-823">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-823">value</span></span>  
<span data-ttu-id="a9b06-824">コントロールの underline プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="a9b06-824">The value to assign to the underline property of the control.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="a9b06-825">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="a9b06-825">Return Value - underline</span></span>

<span data-ttu-id="a9b06-826">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a9b06-826">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-userdata"></a><span data-ttu-id="a9b06-827">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="a9b06-827">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="a9b06-828">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="a9b06-828">Parameters - userData</span></span>

<span data-ttu-id="a9b06-829">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-829">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="a9b06-830">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="a9b06-830">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="a9b06-831">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="a9b06-831">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="a9b06-832">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="a9b06-832">Parameters - userDataItem</span></span>

<span data-ttu-id="a9b06-833">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-833">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="a9b06-834">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="a9b06-834">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="a9b06-835">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="a9b06-835">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="a9b06-836">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="a9b06-836">Parameters - userDataItems</span></span>

<span data-ttu-id="a9b06-837">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-837">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="a9b06-838">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="a9b06-838">Return Value - userDataItems</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="a9b06-839">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="a9b06-839">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="a9b06-840">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="a9b06-840">Parameters - verticalSpacing</span></span>

<span data-ttu-id="a9b06-841">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-841">value</span></span>  

<!-- -->

<span data-ttu-id="a9b06-842">モード</span><span class="sxs-lookup"><span data-stu-id="a9b06-842">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="a9b06-843">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="a9b06-843">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="a9b06-844">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-844">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="a9b06-845">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-845">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="a9b06-846">モード</span><span class="sxs-lookup"><span data-stu-id="a9b06-846">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="a9b06-847">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-847">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="a9b06-848">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-848">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="a9b06-849">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-849">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="a9b06-850">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-850">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="a9b06-851">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-851">Return Value - verticalSpacingValue</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="a9b06-852">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-852">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="a9b06-853">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-853">Parameters - viewEditMode</span></span>

<span data-ttu-id="a9b06-854">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-854">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="a9b06-855">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-855">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="a9b06-856">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="a9b06-856">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="a9b06-857">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="a9b06-857">Parameters - visible</span></span>

<span data-ttu-id="a9b06-858">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-858">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="a9b06-859">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="a9b06-859">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="a9b06-860">メソッド width</span><span class="sxs-lookup"><span data-stu-id="a9b06-860">Method width</span></span>

<span data-ttu-id="a9b06-861">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-861">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="a9b06-862">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="a9b06-862">Parameters - width</span></span>

<span data-ttu-id="a9b06-863">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-863">value</span></span>  

<!-- -->

<span data-ttu-id="a9b06-864">モード</span><span class="sxs-lookup"><span data-stu-id="a9b06-864">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="a9b06-865">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="a9b06-865">Return Value - width</span></span>

<span data-ttu-id="a9b06-866">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="a9b06-866">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="a9b06-867">備考 - width</span><span class="sxs-lookup"><span data-stu-id="a9b06-867">Remarks - width</span></span>

<span data-ttu-id="a9b06-868">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-868">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="a9b06-869">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="a9b06-869">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="a9b06-870">モード。</span><span class="sxs-lookup"><span data-stu-id="a9b06-870">Mode.</span></span>           | <span data-ttu-id="a9b06-871">幅計算。</span><span class="sxs-lookup"><span data-stu-id="a9b06-871">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9b06-872">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="a9b06-872">-1 Exact.</span></span>       | <span data-ttu-id="a9b06-873">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-873">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="a9b06-874">0 自動。</span><span class="sxs-lookup"><span data-stu-id="a9b06-874">0 Auto.</span></span>         | <span data-ttu-id="a9b06-875">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-875">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="a9b06-876">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="a9b06-876">1 Column width.</span></span> | <span data-ttu-id="a9b06-877">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="a9b06-877">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="a9b06-878">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-878">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="a9b06-879">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-879">Method widthMode</span></span>

<span data-ttu-id="a9b06-880">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-880">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="a9b06-881">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-881">Parameters - widthMode</span></span>

<span data-ttu-id="a9b06-882">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-882">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="a9b06-883">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-883">Return Value - widthMode</span></span>

<span data-ttu-id="a9b06-884">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="a9b06-884">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="a9b06-885">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="a9b06-885">Remarks - widthMode</span></span>

<span data-ttu-id="a9b06-886">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="a9b06-886">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="a9b06-887">モード。</span><span class="sxs-lookup"><span data-stu-id="a9b06-887">Mode.</span></span>         | <span data-ttu-id="a9b06-888">幅計算。</span><span class="sxs-lookup"><span data-stu-id="a9b06-888">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9b06-889">正確。</span><span class="sxs-lookup"><span data-stu-id="a9b06-889">Exact.</span></span>        | <span data-ttu-id="a9b06-890">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-890">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="a9b06-891">自動。</span><span class="sxs-lookup"><span data-stu-id="a9b06-891">Auto.</span></span>         | <span data-ttu-id="a9b06-892">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="a9b06-892">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="a9b06-893">列の幅。</span><span class="sxs-lookup"><span data-stu-id="a9b06-893">Column width.</span></span> | <span data-ttu-id="a9b06-894">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="a9b06-894">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="a9b06-895">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="a9b06-895">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="a9b06-896">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-896">Method widthValue</span></span>

<span data-ttu-id="a9b06-897">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-897">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="a9b06-898">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-898">Parameters - widthValue</span></span>

<span data-ttu-id="a9b06-899">値</span><span class="sxs-lookup"><span data-stu-id="a9b06-899">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="a9b06-900">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-900">Return Value - widthValue</span></span>

<span data-ttu-id="a9b06-901">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="a9b06-901">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="a9b06-902">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="a9b06-902">Remarks - widthValue</span></span>

<span data-ttu-id="a9b06-903">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="a9b06-903">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="a9b06-904">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="a9b06-904">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="a9b06-905">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="a9b06-905">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="a9b06-906">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="a9b06-906">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="a9b06-907">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="a9b06-907">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="a9b06-908">overrideObject</span><span class="sxs-lookup"><span data-stu-id="a9b06-908">overrideObject</span></span>  

