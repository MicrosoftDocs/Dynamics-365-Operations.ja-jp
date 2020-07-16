---
title: FormBuildRealControl クラス
description: このトピックでは、FormBuildRealControl クラスについて説明します。
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
ms.openlocfilehash: a692569292762b76e665d5d7a2b28a31f87ea1c7
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502958"
---
# <a name="class-formbuildrealcontrol"></a><span data-ttu-id="1a7a9-103">クラス FormBuildRealControl</span><span class="sxs-lookup"><span data-stu-id="1a7a9-103">Class FormBuildRealControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildRealControl extends FormBuildControl
```

<span data-ttu-id="1a7a9-104">FormBuildRealControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-104">The FormBuildRealControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a7a9-105">備考</span><span class="sxs-lookup"><span data-stu-id="1a7a9-105">Remarks</span></span>

<span data-ttu-id="1a7a9-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="1a7a9-107">例</span><span class="sxs-lookup"><span data-stu-id="1a7a9-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="1a7a9-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="1a7a9-108">Methods</span></span>

| <span data-ttu-id="1a7a9-109">方法</span><span class="sxs-lookup"><span data-stu-id="1a7a9-109">Method</span></span>                                                                                                      | <span data-ttu-id="1a7a9-110">説明</span><span class="sxs-lookup"><span data-stu-id="1a7a9-110">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a7a9-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="1a7a9-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-112">Determines whether to align the control.</span></span>                                                                                                |
| <span data-ttu-id="1a7a9-113">public int alignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-113">public int alignment(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="1a7a9-114">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-114">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="1a7a9-115">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-115">Determines whether the user can change the contents of the control.</span></span>                                                                     |
| <span data-ttu-id="1a7a9-116">public int allowNegative(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-116">public int allowNegative(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="1a7a9-117">public int arrayIndex(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-117">public int arrayIndex(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="1a7a9-118">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-118">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="1a7a9-119">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-119">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                      |
| <span data-ttu-id="1a7a9-120">public int autoInsSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-120">public int autoInsSeparator(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="1a7a9-121">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-121">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="1a7a9-122">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-122">Gets or sets the background color of the control.</span></span>                                                                                       |
| <span data-ttu-id="1a7a9-123">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-123">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="1a7a9-124">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-124">Determines whether the control background can be transparent.</span></span>                                                                           |
| <span data-ttu-id="1a7a9-125">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-125">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="1a7a9-126">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-126">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                             |
| <span data-ttu-id="1a7a9-127">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-127">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="1a7a9-128">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-128">Gets or sets the style of the borderline of the control.</span></span>                                                                                |
| <span data-ttu-id="1a7a9-129">public int cacheDataMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-129">public int cacheDataMethod(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="1a7a9-130">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-130">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="1a7a9-131">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-131">Gets or sets the character set of the font.</span></span>                                                                                             |
| <span data-ttu-id="1a7a9-132">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-132">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="1a7a9-133">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-133">Gets or sets the color scheme of the control.</span></span>                                                                                           |
| <span data-ttu-id="1a7a9-134">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-134">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="1a7a9-135">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-135">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                     |
| <span data-ttu-id="1a7a9-136">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="1a7a9-136">public int containerId()</span></span>                                                                                    | <span data-ttu-id="1a7a9-137">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-137">Retrieves the ID of the parent container for the control.</span></span>                                                                               |
| <span data-ttu-id="1a7a9-138">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-138">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="1a7a9-139">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-139">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                         |
| <span data-ttu-id="1a7a9-140">public FieldId dataField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-140">public FieldId dataField(\[FieldId value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="1a7a9-141">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-141">public str dataMethod(\[str value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="1a7a9-142">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-142">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="1a7a9-143">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-143">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="1a7a9-144">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-144">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                |
| <span data-ttu-id="1a7a9-145">public int decimalSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-145">public int decimalSeparator(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="1a7a9-146">public int direction(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-146">public int direction(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="1a7a9-147">public int displaceNegative(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-147">public int displaceNegative(\[int value\], \[AutoMode mode\])</span></span>                                               |                                                                                                                                         |
| <span data-ttu-id="1a7a9-148">public AutoMode displaceNegativeMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-148">public AutoMode displaceNegativeMode(\[AutoMode mode\])</span></span>                                                     |                                                                                                                                         |
| <span data-ttu-id="1a7a9-149">public int displaceNegativeValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-149">public int displaceNegativeValue(\[int value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="1a7a9-150">public int displayHeight(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-150">public int displayHeight(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                         |
| <span data-ttu-id="1a7a9-151">public AutoMode displayHeightMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-151">public AutoMode displayHeightMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                         |
| <span data-ttu-id="1a7a9-152">public int displayHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-152">public int displayHeightValue(\[int value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="1a7a9-153">public int displayLength(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-153">public int displayLength(\[int value\], \[AutoMode mode\])</span></span>                                                  |                                                                                                                                         |
| <span data-ttu-id="1a7a9-154">public AutoMode displayLengthMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-154">public AutoMode displayLengthMode(\[AutoMode mode\])</span></span>                                                        |                                                                                                                                         |
| <span data-ttu-id="1a7a9-155">public int displayLengthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-155">public int displayLengthValue(\[int value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="1a7a9-156">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-156">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="1a7a9-157">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-157">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="1a7a9-158">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-158">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                       |
| <span data-ttu-id="1a7a9-159">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-159">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="1a7a9-160">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-160">Determines whether to enable or disable the object.</span></span>                                                                                     |
| <span data-ttu-id="1a7a9-161">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-161">public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])</span></span>                                            |                                                                                                                                         |
| <span data-ttu-id="1a7a9-162">public int fastTabSummary(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-162">public int fastTabSummary(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="1a7a9-163">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-163">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="1a7a9-164">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-164">Gets or sets the name of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="1a7a9-165">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-165">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="1a7a9-166">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-166">Gets or sets the size of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="1a7a9-167">public int foregroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-167">public int foregroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="1a7a9-168">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-168">Gets or sets the text color for the control to use.</span></span>                                                                                     |
| <span data-ttu-id="1a7a9-169">public int formatMST(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-169">public int formatMST(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="1a7a9-170">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-170">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="1a7a9-171">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-171">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="1a7a9-172">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-172">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="1a7a9-173">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-173">Gets or sets a calculation mode for the height of the control.</span></span>                                                                          |
| <span data-ttu-id="1a7a9-174">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-174">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="1a7a9-175">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-175">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="1a7a9-176">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-176">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="1a7a9-177">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-177">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                |
| <span data-ttu-id="1a7a9-178">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-178">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="1a7a9-179">public int id()</span><span class="sxs-lookup"><span data-stu-id="1a7a9-179">public int id()</span></span>                                                                                             | <span data-ttu-id="1a7a9-180">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-180">Retrieves the ID of the control.</span></span>                                                                                                        |
| <span data-ttu-id="1a7a9-181">public int iMEMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-181">public int iMEMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="1a7a9-182">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="1a7a9-182">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="1a7a9-183">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-183">Retrieves a value that indicates whether the control is a container control.</span></span>                                                            |
| <span data-ttu-id="1a7a9-184">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-184">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="1a7a9-185">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-185">public str label(\[str value\])</span></span>                                                                             | <span data-ttu-id="1a7a9-186">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-186">Gets or sets the label for a control.</span></span>                                                                                                   |
| <span data-ttu-id="1a7a9-187">public int labelAlignment(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-187">public int labelAlignment(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="1a7a9-188">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-188">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="1a7a9-189">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-189">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="1a7a9-190">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-190">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="1a7a9-191">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-191">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="1a7a9-192">public int labelForegroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-192">public int labelForegroundColor(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="1a7a9-193">public int labelGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-193">public int labelGuide(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="1a7a9-194">public int labelHeight(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-194">public int labelHeight(int value, \[int mode\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="1a7a9-195">public int labelHeightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-195">public int labelHeightMode(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="1a7a9-196">public int labelHeightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-196">public int labelHeightValue(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="1a7a9-197">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-197">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                         |
| <span data-ttu-id="1a7a9-198">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-198">public int labelPosition(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="1a7a9-199">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-199">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                         |
| <span data-ttu-id="1a7a9-200">public int labelWidth(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-200">public int labelWidth(int value, \[int mode\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="1a7a9-201">public int labelWidthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-201">public int labelWidthMode(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="1a7a9-202">public int labelWidthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-202">public int labelWidthValue(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="1a7a9-203">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-203">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="1a7a9-204">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-204">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="1a7a9-205">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-205">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="1a7a9-206">public int limitText(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-206">public int limitText(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="1a7a9-207">public AutoMode limitTextMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-207">public AutoMode limitTextMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                         |
| <span data-ttu-id="1a7a9-208">public int limitTextValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-208">public int limitTextValue(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="1a7a9-209">public int lookupButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-209">public int lookupButton(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="1a7a9-210">public boolean mandatory(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-210">public boolean mandatory(\[boolean value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="1a7a9-211">public int minNoOfDecimals(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-211">public int minNoOfDecimals(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="1a7a9-212">public AutoMode minNoOfDecimalsMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-212">public AutoMode minNoOfDecimalsMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="1a7a9-213">public int minNoOfDecimalsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-213">public int minNoOfDecimalsValue(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="1a7a9-214">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-214">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="1a7a9-215">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-215">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="1a7a9-216">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-216">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="1a7a9-217">public int noOfDecimals(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-217">public int noOfDecimals(\[int value\], \[AutoMode mode\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="1a7a9-218">public AutoMode noOfDecimalsMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-218">public AutoMode noOfDecimalsMode(\[AutoMode mode\])</span></span>                                                         |                                                                                                                                         |
| <span data-ttu-id="1a7a9-219">public int noOfDecimalsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-219">public int noOfDecimalsValue(\[int value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="1a7a9-220">public int promptrect(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-220">public int promptrect(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="1a7a9-221">public Real realValue(\[Real value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-221">public Real realValue(\[Real value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="1a7a9-222">public boolean replaceOnLookup(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-222">public boolean replaceOnLookup(\[boolean value\])</span></span>                                                           |                                                                                                                                         |
| <span data-ttu-id="1a7a9-223">public int rotateSign(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-223">public int rotateSign(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="1a7a9-224">public int searchAfterInput(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-224">public int searchAfterInput(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="1a7a9-225">public int searchMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-225">public int searchMode(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="1a7a9-226">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-226">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="1a7a9-227">public boolean showLabel(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-227">public boolean showLabel(\[boolean value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="1a7a9-228">public int showZero(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-228">public int showZero(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="1a7a9-229">public int signDisplay(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-229">public int signDisplay(\[int value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="1a7a9-230">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-230">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="1a7a9-231">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-231">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>         |
| <span data-ttu-id="1a7a9-232">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-232">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                         |
| <span data-ttu-id="1a7a9-233">public int thousandSeparator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-233">public int thousandSeparator(\[int value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="1a7a9-234">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-234">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="1a7a9-235">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-235">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="1a7a9-236">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-236">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="1a7a9-237">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-237">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="1a7a9-238">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-238">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="1a7a9-239">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-239">Sets or returns the underline property for the text in the control.</span></span>                                                                     |
| <span data-ttu-id="1a7a9-240">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-240">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="1a7a9-241">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-241">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="1a7a9-242">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-242">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="1a7a9-243">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-243">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="1a7a9-244">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-244">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="1a7a9-245">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-245">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="1a7a9-246">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-246">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="1a7a9-247">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-247">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="1a7a9-248">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-248">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="1a7a9-249">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-249">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="1a7a9-250">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-250">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="1a7a9-251">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-251">Gets or sets the calculation mode of the width of the control.</span></span>                                                                          |
| <span data-ttu-id="1a7a9-252">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-252">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="1a7a9-253">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-253">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="1a7a9-254">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="1a7a9-254">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                         |

## <a name="method-aligncontrol"></a><span data-ttu-id="1a7a9-255">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="1a7a9-255">Method alignControl</span></span>

<span data-ttu-id="1a7a9-256">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-256">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="1a7a9-257">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="1a7a9-257">Parameters - alignControl</span></span>

<span data-ttu-id="1a7a9-258">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-258">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="1a7a9-259">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="1a7a9-259">Return Value - alignControl</span></span>

<span data-ttu-id="1a7a9-260">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-260">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="1a7a9-261">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="1a7a9-261">Remarks - alignControl</span></span>

<span data-ttu-id="1a7a9-262">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-262">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-alignment"></a><span data-ttu-id="1a7a9-263">メソッド alignment</span><span class="sxs-lookup"><span data-stu-id="1a7a9-263">Method alignment</span></span>

```xpp
public int alignment([int value])
```

### <a name="parameters---alignment"></a><span data-ttu-id="1a7a9-264">パラメーター - alignment</span><span class="sxs-lookup"><span data-stu-id="1a7a9-264">Parameters - alignment</span></span>

<span data-ttu-id="1a7a9-265">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-265">value</span></span>  

### <a name="return-value---alignment"></a><span data-ttu-id="1a7a9-266">戻り値 - alignment</span><span class="sxs-lookup"><span data-stu-id="1a7a9-266">Return Value - alignment</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="1a7a9-267">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="1a7a9-267">Method allowEdit</span></span>

<span data-ttu-id="1a7a9-268">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-268">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="1a7a9-269">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="1a7a9-269">Parameters - allowEdit</span></span>

<span data-ttu-id="1a7a9-270">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-270">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="1a7a9-271">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="1a7a9-271">Return Value - allowEdit</span></span>

<span data-ttu-id="1a7a9-272">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-272">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="1a7a9-273">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="1a7a9-273">Remarks - allowEdit</span></span>

<span data-ttu-id="1a7a9-274">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-274">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-allownegative"></a><span data-ttu-id="1a7a9-275">メソッド allowNegative</span><span class="sxs-lookup"><span data-stu-id="1a7a9-275">Method allowNegative</span></span>

```xpp
public int allowNegative([int value])
```

### <a name="parameters---allownegative"></a><span data-ttu-id="1a7a9-276">パラメーター - allowNegative</span><span class="sxs-lookup"><span data-stu-id="1a7a9-276">Parameters - allowNegative</span></span>

<span data-ttu-id="1a7a9-277">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-277">value</span></span>  

### <a name="return-value---allownegative"></a><span data-ttu-id="1a7a9-278">戻り値 - allowNegative</span><span class="sxs-lookup"><span data-stu-id="1a7a9-278">Return Value - allowNegative</span></span>

## <a name="method-arrayindex"></a><span data-ttu-id="1a7a9-279">メソッド arrayIndex</span><span class="sxs-lookup"><span data-stu-id="1a7a9-279">Method arrayIndex</span></span>

```xpp
public int arrayIndex([int value])
```

### <a name="parameters---arrayindex"></a><span data-ttu-id="1a7a9-280">パラメーター - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="1a7a9-280">Parameters - arrayIndex</span></span>

<span data-ttu-id="1a7a9-281">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-281">value</span></span>  

### <a name="return-value---arrayindex"></a><span data-ttu-id="1a7a9-282">戻り値 - arrayIndex</span><span class="sxs-lookup"><span data-stu-id="1a7a9-282">Return Value - arrayIndex</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="1a7a9-283">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="1a7a9-283">Method autoDeclaration</span></span>

<span data-ttu-id="1a7a9-284">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-284">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="1a7a9-285">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="1a7a9-285">Parameters - autoDeclaration</span></span>

<span data-ttu-id="1a7a9-286">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-286">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="1a7a9-287">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="1a7a9-287">Return Value - autoDeclaration</span></span>

<span data-ttu-id="1a7a9-288">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-288">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="1a7a9-289">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="1a7a9-289">Remarks - autoDeclaration</span></span>

<span data-ttu-id="1a7a9-290">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-290">Controls cannot have identical names.</span></span>

## <a name="method-autoinsseparator"></a><span data-ttu-id="1a7a9-291">メソッド autoInsSeparator</span><span class="sxs-lookup"><span data-stu-id="1a7a9-291">Method autoInsSeparator</span></span>

```xpp
public int autoInsSeparator([int value])
```

### <a name="parameters---autoinsseparator"></a><span data-ttu-id="1a7a9-292">パラメーター - autoInsSeparator</span><span class="sxs-lookup"><span data-stu-id="1a7a9-292">Parameters - autoInsSeparator</span></span>

<span data-ttu-id="1a7a9-293">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-293">value</span></span>  

### <a name="return-value---autoinsseparator"></a><span data-ttu-id="1a7a9-294">戻り値 - autoInsSeparator</span><span class="sxs-lookup"><span data-stu-id="1a7a9-294">Return Value - autoInsSeparator</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="1a7a9-295">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="1a7a9-295">Method backgroundColor</span></span>

<span data-ttu-id="1a7a9-296">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-296">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="1a7a9-297">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="1a7a9-297">Parameters - backgroundColor</span></span>

<span data-ttu-id="1a7a9-298">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-298">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="1a7a9-299">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="1a7a9-299">Return Value - backgroundColor</span></span>

<span data-ttu-id="1a7a9-300">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-300">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="1a7a9-301">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="1a7a9-301">Remarks - backgroundColor</span></span>

<span data-ttu-id="1a7a9-302">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-302">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="1a7a9-303">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-303">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="1a7a9-304">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-304">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="1a7a9-305">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-305">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="1a7a9-306">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-306">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="1a7a9-307">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-307">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="1a7a9-308">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="1a7a9-308">Method backStyle</span></span>

<span data-ttu-id="1a7a9-309">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-309">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="1a7a9-310">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="1a7a9-310">Parameters - backStyle</span></span>

<span data-ttu-id="1a7a9-311">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-311">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="1a7a9-312">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="1a7a9-312">Return Value - backStyle</span></span>

<span data-ttu-id="1a7a9-313">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-313">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="1a7a9-314">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="1a7a9-314">Method bold</span></span>

<span data-ttu-id="1a7a9-315">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-315">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="1a7a9-316">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="1a7a9-316">Parameters - bold</span></span>

<span data-ttu-id="1a7a9-317">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-317">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="1a7a9-318">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="1a7a9-318">Return Value - bold</span></span>

<span data-ttu-id="1a7a9-319">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-319">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="1a7a9-320">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="1a7a9-320">Remarks - bold</span></span>

<span data-ttu-id="1a7a9-321">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-321">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="1a7a9-322">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-322">0 Use the default font weight.</span></span>
-   <span data-ttu-id="1a7a9-323">1 シン。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-323">1 Thin.</span></span>
-   <span data-ttu-id="1a7a9-324">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-324">2 Extra-light.</span></span>
-   <span data-ttu-id="1a7a9-325">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-325">3 Light.</span></span>
-   <span data-ttu-id="1a7a9-326">4 標準。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-326">4 Normal.</span></span>
-   <span data-ttu-id="1a7a9-327">5 中。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-327">5 Medium.</span></span>
-   <span data-ttu-id="1a7a9-328">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-328">6 Semibold.</span></span>
-   <span data-ttu-id="1a7a9-329">7 太字。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-329">7 Bold.</span></span>
-   <span data-ttu-id="1a7a9-330">8 極太。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-330">8 Extra-bold.</span></span>
-   <span data-ttu-id="1a7a9-331">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-331">9 Heavy.</span></span>

## <a name="method-border"></a><span data-ttu-id="1a7a9-332">メソッド border</span><span class="sxs-lookup"><span data-stu-id="1a7a9-332">Method border</span></span>

<span data-ttu-id="1a7a9-333">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-333">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="1a7a9-334">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="1a7a9-334">Parameters - border</span></span>

<span data-ttu-id="1a7a9-335">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-335">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="1a7a9-336">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="1a7a9-336">Return Value - border</span></span>

<span data-ttu-id="1a7a9-337">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-337">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="1a7a9-338">備考 - border</span><span class="sxs-lookup"><span data-stu-id="1a7a9-338">Remarks - border</span></span>

<span data-ttu-id="1a7a9-339">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-339">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="1a7a9-340">値です。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-340">Value.</span></span> | <span data-ttu-id="1a7a9-341">説明。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-341">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="1a7a9-342">0</span><span class="sxs-lookup"><span data-stu-id="1a7a9-342">0</span></span>      | <span data-ttu-id="1a7a9-343">自動。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-343">Auto.</span></span>        |
| <span data-ttu-id="1a7a9-344">1</span><span class="sxs-lookup"><span data-stu-id="1a7a9-344">1</span></span>      | <span data-ttu-id="1a7a9-345">3D。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-345">3D.</span></span>          |
| <span data-ttu-id="1a7a9-346">2</span><span class="sxs-lookup"><span data-stu-id="1a7a9-346">2</span></span>      | <span data-ttu-id="1a7a9-347">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-347">Single line.</span></span> |
| <span data-ttu-id="1a7a9-348">3</span><span class="sxs-lookup"><span data-stu-id="1a7a9-348">3</span></span>      | <span data-ttu-id="1a7a9-349">均一。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-349">Flat.</span></span>        |
| <span data-ttu-id="1a7a9-350">4</span><span class="sxs-lookup"><span data-stu-id="1a7a9-350">4</span></span>      | <span data-ttu-id="1a7a9-351">なし。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-351">None.</span></span>        |

## <a name="method-cachedatamethod"></a><span data-ttu-id="1a7a9-352">メソッド cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="1a7a9-352">Method cacheDataMethod</span></span>

```xpp
public int cacheDataMethod([int value])
```

### <a name="parameters---cachedatamethod"></a><span data-ttu-id="1a7a9-353">パラメーター - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="1a7a9-353">Parameters - cacheDataMethod</span></span>

<span data-ttu-id="1a7a9-354">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-354">value</span></span>  

### <a name="return-value---cachedatamethod"></a><span data-ttu-id="1a7a9-355">戻り値 - cacheDataMethod</span><span class="sxs-lookup"><span data-stu-id="1a7a9-355">Return Value - cacheDataMethod</span></span>

## <a name="method-characterset"></a><span data-ttu-id="1a7a9-356">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="1a7a9-356">Method characterSet</span></span>

<span data-ttu-id="1a7a9-357">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-357">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="1a7a9-358">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="1a7a9-358">Parameters - characterSet</span></span>

<span data-ttu-id="1a7a9-359">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-359">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="1a7a9-360">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="1a7a9-360">Return Value - characterSet</span></span>

<span data-ttu-id="1a7a9-361">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-361">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="1a7a9-362">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="1a7a9-362">Remarks - characterSet</span></span>

<span data-ttu-id="1a7a9-363">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-363">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="1a7a9-364">値です。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-364">Value.</span></span> | <span data-ttu-id="1a7a9-365">説明。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-365">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="1a7a9-366">0</span><span class="sxs-lookup"><span data-stu-id="1a7a9-366">0</span></span>      | <span data-ttu-id="1a7a9-367">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a7a9-367">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="1a7a9-368">1</span><span class="sxs-lookup"><span data-stu-id="1a7a9-368">1</span></span>      | <span data-ttu-id="1a7a9-369">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a7a9-369">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="1a7a9-370">2</span><span class="sxs-lookup"><span data-stu-id="1a7a9-370">2</span></span>      | <span data-ttu-id="1a7a9-371">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a7a9-371">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="1a7a9-372">77</span><span class="sxs-lookup"><span data-stu-id="1a7a9-372">77</span></span>     | <span data-ttu-id="1a7a9-373">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a7a9-373">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="1a7a9-374">128</span><span class="sxs-lookup"><span data-stu-id="1a7a9-374">128</span></span>    | <span data-ttu-id="1a7a9-375">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a7a9-375">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="1a7a9-376">129</span><span class="sxs-lookup"><span data-stu-id="1a7a9-376">129</span></span>    | <span data-ttu-id="1a7a9-377">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a7a9-377">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="1a7a9-378">134</span><span class="sxs-lookup"><span data-stu-id="1a7a9-378">134</span></span>    | <span data-ttu-id="1a7a9-379">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a7a9-379">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="1a7a9-380">136</span><span class="sxs-lookup"><span data-stu-id="1a7a9-380">136</span></span>    | <span data-ttu-id="1a7a9-381">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a7a9-381">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="1a7a9-382">161</span><span class="sxs-lookup"><span data-stu-id="1a7a9-382">161</span></span>    | <span data-ttu-id="1a7a9-383">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a7a9-383">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="1a7a9-384">162</span><span class="sxs-lookup"><span data-stu-id="1a7a9-384">162</span></span>    | <span data-ttu-id="1a7a9-385">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a7a9-385">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="1a7a9-386">163</span><span class="sxs-lookup"><span data-stu-id="1a7a9-386">163</span></span>    | <span data-ttu-id="1a7a9-387">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a7a9-387">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="1a7a9-388">186</span><span class="sxs-lookup"><span data-stu-id="1a7a9-388">186</span></span>    | <span data-ttu-id="1a7a9-389">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a7a9-389">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="1a7a9-390">204</span><span class="sxs-lookup"><span data-stu-id="1a7a9-390">204</span></span>    | <span data-ttu-id="1a7a9-391">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a7a9-391">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="1a7a9-392">238</span><span class="sxs-lookup"><span data-stu-id="1a7a9-392">238</span></span>    | <span data-ttu-id="1a7a9-393">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a7a9-393">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="1a7a9-394">255</span><span class="sxs-lookup"><span data-stu-id="1a7a9-394">255</span></span>    | <span data-ttu-id="1a7a9-395">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a7a9-395">OEM\_CHARSET</span></span>         |

<span data-ttu-id="1a7a9-396">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-396">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="1a7a9-397">値です。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-397">Value.</span></span> | <span data-ttu-id="1a7a9-398">説明。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-398">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="1a7a9-399">130</span><span class="sxs-lookup"><span data-stu-id="1a7a9-399">130</span></span>    | <span data-ttu-id="1a7a9-400">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a7a9-400">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="1a7a9-401">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-401">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="1a7a9-402">値です。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-402">Value.</span></span> | <span data-ttu-id="1a7a9-403">説明。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-403">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="1a7a9-404">177</span><span class="sxs-lookup"><span data-stu-id="1a7a9-404">177</span></span>    | <span data-ttu-id="1a7a9-405">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a7a9-405">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="1a7a9-406">178</span><span class="sxs-lookup"><span data-stu-id="1a7a9-406">178</span></span>    | <span data-ttu-id="1a7a9-407">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a7a9-407">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="1a7a9-408">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-408">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="1a7a9-409">値です。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-409">Value.</span></span> | <span data-ttu-id="1a7a9-410">説明。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-410">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="1a7a9-411">222</span><span class="sxs-lookup"><span data-stu-id="1a7a9-411">222</span></span>    | <span data-ttu-id="1a7a9-412">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="1a7a9-412">THAI\_CHARSET</span></span> |

<span data-ttu-id="1a7a9-413">既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-413">The default character set is set to a value, depending on the current system locale.</span></span> <span data-ttu-id="1a7a9-414">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-414">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="1a7a9-415">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-415">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="1a7a9-416">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="1a7a9-416">Method colorScheme</span></span>

<span data-ttu-id="1a7a9-417">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-417">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="1a7a9-418">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="1a7a9-418">Parameters - colorScheme</span></span>

<span data-ttu-id="1a7a9-419">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-419">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="1a7a9-420">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="1a7a9-420">Return Value - colorScheme</span></span>

<span data-ttu-id="1a7a9-421">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-421">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="1a7a9-422">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="1a7a9-422">Remarks - colorScheme</span></span>

<span data-ttu-id="1a7a9-423">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-423">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="1a7a9-424">値です。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-424">Value.</span></span> | <span data-ttu-id="1a7a9-425">スタイル。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-425">Style.</span></span>                         |
|--------|--------------------------------|
| <span data-ttu-id="1a7a9-426">0</span><span class="sxs-lookup"><span data-stu-id="1a7a9-426">0</span></span>      | <span data-ttu-id="1a7a9-427">既定。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-427">Default.</span></span>                       |
| <span data-ttu-id="1a7a9-428">1</span><span class="sxs-lookup"><span data-stu-id="1a7a9-428">1</span></span>      | <span data-ttu-id="1a7a9-429">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-429">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="1a7a9-430">2</span><span class="sxs-lookup"><span data-stu-id="1a7a9-430">2</span></span>      | <span data-ttu-id="1a7a9-431">真の配色。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-431">The true-color scheme.</span></span>         |

## <a name="method-configurationkey"></a><span data-ttu-id="1a7a9-432">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="1a7a9-432">Method configurationKey</span></span>

<span data-ttu-id="1a7a9-433">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-433">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="1a7a9-434">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="1a7a9-434">Parameters - configurationKey</span></span>

<span data-ttu-id="1a7a9-435">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-435">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="1a7a9-436">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="1a7a9-436">Return Value - configurationKey</span></span>

<span data-ttu-id="1a7a9-437">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-437">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="1a7a9-438">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="1a7a9-438">Remarks - configurationKey</span></span>

<span data-ttu-id="1a7a9-439">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-439">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="1a7a9-440">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-440">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="1a7a9-441">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="1a7a9-441">Method containerId</span></span>

<span data-ttu-id="1a7a9-442">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-442">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="1a7a9-443">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="1a7a9-443">Return Value - containerId</span></span>

<span data-ttu-id="1a7a9-444">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-444">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="1a7a9-445">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="1a7a9-445">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="1a7a9-446">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="1a7a9-446">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="1a7a9-447">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-447">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="1a7a9-448">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="1a7a9-448">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="1a7a9-449">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="1a7a9-449">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="1a7a9-450">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="1a7a9-450">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="1a7a9-451">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-451">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="1a7a9-452">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="1a7a9-452">Return Value - countryRegionContextField</span></span>

## <a name="method-datafield"></a><span data-ttu-id="1a7a9-453">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="1a7a9-453">Method dataField</span></span>

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="1a7a9-454">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="1a7a9-454">Parameters - dataField</span></span>

<span data-ttu-id="1a7a9-455">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-455">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="1a7a9-456">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="1a7a9-456">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="1a7a9-457">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="1a7a9-457">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="1a7a9-458">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="1a7a9-458">Parameters - dataMethod</span></span>

<span data-ttu-id="1a7a9-459">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-459">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="1a7a9-460">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="1a7a9-460">Return Value - dataMethod</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="1a7a9-461">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="1a7a9-461">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="1a7a9-462">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="1a7a9-462">Parameters - dataRelationPath</span></span>

<span data-ttu-id="1a7a9-463">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-463">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="1a7a9-464">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="1a7a9-464">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="1a7a9-465">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="1a7a9-465">Method dataSource</span></span>

<span data-ttu-id="1a7a9-466">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-466">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="1a7a9-467">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="1a7a9-467">Parameters - dataSource</span></span>

<span data-ttu-id="1a7a9-468">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-468">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="1a7a9-469">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="1a7a9-469">Return Value - dataSource</span></span>

<span data-ttu-id="1a7a9-470">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-470">The identifier of the data source that will be used.</span></span>

## <a name="method-decimalseparator"></a><span data-ttu-id="1a7a9-471">メソッド decimalSeparator</span><span class="sxs-lookup"><span data-stu-id="1a7a9-471">Method decimalSeparator</span></span>

```xpp
public int decimalSeparator([int value])
```

### <a name="parameters---decimalseparator"></a><span data-ttu-id="1a7a9-472">パラメーター - decimalSeparator</span><span class="sxs-lookup"><span data-stu-id="1a7a9-472">Parameters - decimalSeparator</span></span>

<span data-ttu-id="1a7a9-473">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-473">value</span></span>  

### <a name="return-value---decimalseparator"></a><span data-ttu-id="1a7a9-474">戻り値 - decimalSeparator</span><span class="sxs-lookup"><span data-stu-id="1a7a9-474">Return Value - decimalSeparator</span></span>

## <a name="method-direction"></a><span data-ttu-id="1a7a9-475">メソッド direction</span><span class="sxs-lookup"><span data-stu-id="1a7a9-475">Method direction</span></span>

```xpp
public int direction([int value])
```

### <a name="parameters---direction"></a><span data-ttu-id="1a7a9-476">パラメーター - direction</span><span class="sxs-lookup"><span data-stu-id="1a7a9-476">Parameters - direction</span></span>

<span data-ttu-id="1a7a9-477">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-477">value</span></span>  

### <a name="return-value---direction"></a><span data-ttu-id="1a7a9-478">戻り値 - direction</span><span class="sxs-lookup"><span data-stu-id="1a7a9-478">Return Value - direction</span></span>

## <a name="method-displacenegative"></a><span data-ttu-id="1a7a9-479">メソッド displaceNegative</span><span class="sxs-lookup"><span data-stu-id="1a7a9-479">Method displaceNegative</span></span>

```xpp
public int displaceNegative([int value], [AutoMode mode])
```

### <a name="parameters---displacenegative"></a><span data-ttu-id="1a7a9-480">パラメーター - displaceNegative</span><span class="sxs-lookup"><span data-stu-id="1a7a9-480">Parameters - displaceNegative</span></span>

<span data-ttu-id="1a7a9-481">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-481">value</span></span>  

<!-- -->

<span data-ttu-id="1a7a9-482">モード</span><span class="sxs-lookup"><span data-stu-id="1a7a9-482">mode</span></span>  

### <a name="return-value---displacenegative"></a><span data-ttu-id="1a7a9-483">戻り値 - displaceNegative</span><span class="sxs-lookup"><span data-stu-id="1a7a9-483">Return Value - displaceNegative</span></span>

## <a name="method-displacenegativemode"></a><span data-ttu-id="1a7a9-484">メソッド displaceNegativeMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-484">Method displaceNegativeMode</span></span>

```xpp
public AutoMode displaceNegativeMode([AutoMode mode])
```

### <a name="parameters---displacenegativemode"></a><span data-ttu-id="1a7a9-485">パラメーター - displaceNegativeMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-485">Parameters - displaceNegativeMode</span></span>

<span data-ttu-id="1a7a9-486">モード</span><span class="sxs-lookup"><span data-stu-id="1a7a9-486">mode</span></span>  

### <a name="return-value---displacenegativemode"></a><span data-ttu-id="1a7a9-487">戻り値 - displaceNegativeMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-487">Return Value - displaceNegativeMode</span></span>

## <a name="method-displacenegativevalue"></a><span data-ttu-id="1a7a9-488">メソッド displaceNegativeValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-488">Method displaceNegativeValue</span></span>

```xpp
public int displaceNegativeValue([int value])
```

### <a name="parameters---displacenegativevalue"></a><span data-ttu-id="1a7a9-489">パラメーター - displaceNegativeValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-489">Parameters - displaceNegativeValue</span></span>

<span data-ttu-id="1a7a9-490">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-490">value</span></span>  

### <a name="return-value---displacenegativevalue"></a><span data-ttu-id="1a7a9-491">戻り値 - displaceNegativeValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-491">Return Value - displaceNegativeValue</span></span>

## <a name="method-displayheight"></a><span data-ttu-id="1a7a9-492">メソッド displayHeight</span><span class="sxs-lookup"><span data-stu-id="1a7a9-492">Method displayHeight</span></span>

```xpp
public int displayHeight([int value], [AutoMode mode])
```

### <a name="parameters---displayheight"></a><span data-ttu-id="1a7a9-493">パラメーター - displayHeight</span><span class="sxs-lookup"><span data-stu-id="1a7a9-493">Parameters - displayHeight</span></span>

<span data-ttu-id="1a7a9-494">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-494">value</span></span>  

<!-- -->

<span data-ttu-id="1a7a9-495">モード</span><span class="sxs-lookup"><span data-stu-id="1a7a9-495">mode</span></span>  

### <a name="return-value---displayheight"></a><span data-ttu-id="1a7a9-496">戻り値 - displayHeight</span><span class="sxs-lookup"><span data-stu-id="1a7a9-496">Return Value - displayHeight</span></span>

## <a name="method-displayheightmode"></a><span data-ttu-id="1a7a9-497">メソッド displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-497">Method displayHeightMode</span></span>

```xpp
public AutoMode displayHeightMode([AutoMode mode])
```

### <a name="parameters---displayheightmode"></a><span data-ttu-id="1a7a9-498">パラメーター - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-498">Parameters - displayHeightMode</span></span>

<span data-ttu-id="1a7a9-499">モード</span><span class="sxs-lookup"><span data-stu-id="1a7a9-499">mode</span></span>  

### <a name="return-value---displayheightmode"></a><span data-ttu-id="1a7a9-500">戻り値 - displayHeightMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-500">Return Value - displayHeightMode</span></span>

## <a name="method-displayheightvalue"></a><span data-ttu-id="1a7a9-501">メソッド displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-501">Method displayHeightValue</span></span>

```xpp
public int displayHeightValue([int value])
```

### <a name="parameters---displayheightvalue"></a><span data-ttu-id="1a7a9-502">パラメーター - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-502">Parameters - displayHeightValue</span></span>

<span data-ttu-id="1a7a9-503">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-503">value</span></span>  

### <a name="return-value---displayheightvalue"></a><span data-ttu-id="1a7a9-504">戻り値 - displayHeightValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-504">Return Value - displayHeightValue</span></span>

## <a name="method-displaylength"></a><span data-ttu-id="1a7a9-505">メソッド displayLength</span><span class="sxs-lookup"><span data-stu-id="1a7a9-505">Method displayLength</span></span>

```xpp
public int displayLength([int value], [AutoMode mode])
```

### <a name="parameters---displaylength"></a><span data-ttu-id="1a7a9-506">パラメーター - displayLength</span><span class="sxs-lookup"><span data-stu-id="1a7a9-506">Parameters - displayLength</span></span>

<span data-ttu-id="1a7a9-507">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-507">value</span></span>  

<!-- -->

<span data-ttu-id="1a7a9-508">モード</span><span class="sxs-lookup"><span data-stu-id="1a7a9-508">mode</span></span>  

### <a name="return-value---displaylength"></a><span data-ttu-id="1a7a9-509">戻り値 - displayLength</span><span class="sxs-lookup"><span data-stu-id="1a7a9-509">Return Value - displayLength</span></span>

## <a name="method-displaylengthmode"></a><span data-ttu-id="1a7a9-510">メソッド displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-510">Method displayLengthMode</span></span>

```xpp
public AutoMode displayLengthMode([AutoMode mode])
```

### <a name="parameters---displaylengthmode"></a><span data-ttu-id="1a7a9-511">パラメーター - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-511">Parameters - displayLengthMode</span></span>

<span data-ttu-id="1a7a9-512">モード</span><span class="sxs-lookup"><span data-stu-id="1a7a9-512">mode</span></span>  

### <a name="return-value---displaylengthmode"></a><span data-ttu-id="1a7a9-513">戻り値 - displayLengthMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-513">Return Value - displayLengthMode</span></span>

## <a name="method-displaylengthvalue"></a><span data-ttu-id="1a7a9-514">メソッド displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-514">Method displayLengthValue</span></span>

```xpp
public int displayLengthValue([int value])
```

### <a name="parameters---displaylengthvalue"></a><span data-ttu-id="1a7a9-515">パラメーター - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-515">Parameters - displayLengthValue</span></span>

<span data-ttu-id="1a7a9-516">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-516">value</span></span>  

### <a name="return-value---displaylengthvalue"></a><span data-ttu-id="1a7a9-517">戻り値 - displayLengthValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-517">Return Value - displayLengthValue</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="1a7a9-518">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="1a7a9-518">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="1a7a9-519">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="1a7a9-519">Parameters - displayTarget</span></span>

<span data-ttu-id="1a7a9-520">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-520">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="1a7a9-521">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="1a7a9-521">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="1a7a9-522">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="1a7a9-522">Method dragDrop</span></span>

<span data-ttu-id="1a7a9-523">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-523">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="1a7a9-524">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="1a7a9-524">Parameters - dragDrop</span></span>

<span data-ttu-id="1a7a9-525">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-525">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="1a7a9-526">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="1a7a9-526">Return Value - dragDrop</span></span>

<span data-ttu-id="1a7a9-527">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-527">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="1a7a9-528">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="1a7a9-528">Method enabled</span></span>

<span data-ttu-id="1a7a9-529">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-529">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="1a7a9-530">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="1a7a9-530">Parameters - enabled</span></span>

<span data-ttu-id="1a7a9-531">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-531">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="1a7a9-532">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="1a7a9-532">Return Value - enabled</span></span>

<span data-ttu-id="1a7a9-533">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-533">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="1a7a9-534">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="1a7a9-534">Remarks - enabled</span></span>

<span data-ttu-id="1a7a9-535">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-535">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="1a7a9-536">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-536">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="1a7a9-537">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-537">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-extendeddatatype"></a><span data-ttu-id="1a7a9-538">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="1a7a9-538">Method extendedDataType</span></span>

```xpp
public ExtendedTypeId extendedDataType([ExtendedTypeId value])
```

### <a name="parameters---extendeddatatype"></a><span data-ttu-id="1a7a9-539">パラメーター - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="1a7a9-539">Parameters - extendedDataType</span></span>

<span data-ttu-id="1a7a9-540">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-540">value</span></span>  

### <a name="return-value---extendeddatatype"></a><span data-ttu-id="1a7a9-541">戻り値 - extendedDataType</span><span class="sxs-lookup"><span data-stu-id="1a7a9-541">Return Value - extendedDataType</span></span>

## <a name="method-fasttabsummary"></a><span data-ttu-id="1a7a9-542">メソッド fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="1a7a9-542">Method fastTabSummary</span></span>

```xpp
public int fastTabSummary([int value])
```

### <a name="parameters---fasttabsummary"></a><span data-ttu-id="1a7a9-543">パラメーター - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="1a7a9-543">Parameters - fastTabSummary</span></span>

<span data-ttu-id="1a7a9-544">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-544">value</span></span>  

### <a name="return-value---fasttabsummary"></a><span data-ttu-id="1a7a9-545">戻り値 - fastTabSummary</span><span class="sxs-lookup"><span data-stu-id="1a7a9-545">Return Value - fastTabSummary</span></span>

## <a name="method-font"></a><span data-ttu-id="1a7a9-546">メソッド font</span><span class="sxs-lookup"><span data-stu-id="1a7a9-546">Method font</span></span>

<span data-ttu-id="1a7a9-547">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-547">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="1a7a9-548">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="1a7a9-548">Parameters - font</span></span>

<span data-ttu-id="1a7a9-549">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-549">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="1a7a9-550">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="1a7a9-550">Return Value - font</span></span>

<span data-ttu-id="1a7a9-551">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-551">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="1a7a9-552">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="1a7a9-552">Method fontSize</span></span>

<span data-ttu-id="1a7a9-553">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-553">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="1a7a9-554">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="1a7a9-554">Parameters - fontSize</span></span>

<span data-ttu-id="1a7a9-555">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-555">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="1a7a9-556">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="1a7a9-556">Return Value - fontSize</span></span>

<span data-ttu-id="1a7a9-557">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-557">The height of the font in points.</span></span>

## <a name="method-foregroundcolor"></a><span data-ttu-id="1a7a9-558">メソッド foregroundColor</span><span class="sxs-lookup"><span data-stu-id="1a7a9-558">Method foregroundColor</span></span>

<span data-ttu-id="1a7a9-559">使用するコントロールのテキストの色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-559">Gets or sets the text color for the control to use.</span></span>

```xpp
public int foregroundColor([int value])
```

### <a name="parameters---foregroundcolor"></a><span data-ttu-id="1a7a9-560">パラメーター - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="1a7a9-560">Parameters - foregroundColor</span></span>

<span data-ttu-id="1a7a9-561">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-561">value</span></span>  

### <a name="return-value---foregroundcolor"></a><span data-ttu-id="1a7a9-562">戻り値 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="1a7a9-562">Return Value - foregroundColor</span></span>

<span data-ttu-id="1a7a9-563">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-563">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---foregroundcolor"></a><span data-ttu-id="1a7a9-564">備考 - foregroundColor</span><span class="sxs-lookup"><span data-stu-id="1a7a9-564">Remarks - foregroundColor</span></span>

<span data-ttu-id="1a7a9-565">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-565">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="1a7a9-566">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-566">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="1a7a9-567">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-567">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="1a7a9-568">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-568">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="1a7a9-569">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-569">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="1a7a9-570">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-570">The maximum value for a single byte is 255.</span></span>

## <a name="method-formatmst"></a><span data-ttu-id="1a7a9-571">メソッド formatMST</span><span class="sxs-lookup"><span data-stu-id="1a7a9-571">Method formatMST</span></span>

```xpp
public int formatMST([int value])
```

### <a name="parameters---formatmst"></a><span data-ttu-id="1a7a9-572">パラメーター - formatMST</span><span class="sxs-lookup"><span data-stu-id="1a7a9-572">Parameters - formatMST</span></span>

<span data-ttu-id="1a7a9-573">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-573">value</span></span>  

### <a name="return-value---formatmst"></a><span data-ttu-id="1a7a9-574">戻り値 - formatMST</span><span class="sxs-lookup"><span data-stu-id="1a7a9-574">Return Value - formatMST</span></span>

## <a name="method-height"></a><span data-ttu-id="1a7a9-575">メソッド height</span><span class="sxs-lookup"><span data-stu-id="1a7a9-575">Method height</span></span>

<span data-ttu-id="1a7a9-576">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-576">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="1a7a9-577">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="1a7a9-577">Parameters - height</span></span>

<span data-ttu-id="1a7a9-578">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-578">value</span></span>  

<!-- -->

<span data-ttu-id="1a7a9-579">モード</span><span class="sxs-lookup"><span data-stu-id="1a7a9-579">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="1a7a9-580">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="1a7a9-580">Return Value - height</span></span>

<span data-ttu-id="1a7a9-581">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-581">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="1a7a9-582">備考 - height</span><span class="sxs-lookup"><span data-stu-id="1a7a9-582">Remarks - height</span></span>

<span data-ttu-id="1a7a9-583">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-583">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="1a7a9-584">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="1a7a9-584">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="1a7a9-585">モード。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-585">Mode.</span></span>            | <span data-ttu-id="1a7a9-586">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-586">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a7a9-587">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-587">-1 Exact.</span></span>        | <span data-ttu-id="1a7a9-588">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-588">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="1a7a9-589">0 自動。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-589">0 Auto.</span></span>          | <span data-ttu-id="1a7a9-590">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-590">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="1a7a9-591">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-591">1 Column height.</span></span> | <span data-ttu-id="1a7a9-592">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-592">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="1a7a9-593">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-593">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="1a7a9-594">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-594">Method heightMode</span></span>

<span data-ttu-id="1a7a9-595">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-595">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="1a7a9-596">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-596">Parameters - heightMode</span></span>

<span data-ttu-id="1a7a9-597">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-597">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="1a7a9-598">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-598">Return Value - heightMode</span></span>

<span data-ttu-id="1a7a9-599">計算モード。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-599">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="1a7a9-600">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-600">Remarks - heightMode</span></span>

<span data-ttu-id="1a7a9-601">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="1a7a9-601">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="1a7a9-602">モード。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-602">Mode.</span></span>          | <span data-ttu-id="1a7a9-603">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-603">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a7a9-604">正確。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-604">Exact.</span></span>         | <span data-ttu-id="1a7a9-605">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-605">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="1a7a9-606">自動。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-606">Auto.</span></span>          | <span data-ttu-id="1a7a9-607">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-607">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="1a7a9-608">列の高さ</span><span class="sxs-lookup"><span data-stu-id="1a7a9-608">Column height.</span></span> | <span data-ttu-id="1a7a9-609">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-609">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="1a7a9-610">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-610">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="1a7a9-611">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-611">Method heightValue</span></span>

<span data-ttu-id="1a7a9-612">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-612">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="1a7a9-613">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-613">Parameters - heightValue</span></span>

<span data-ttu-id="1a7a9-614">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-614">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="1a7a9-615">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-615">Return Value - heightValue</span></span>

<span data-ttu-id="1a7a9-616">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-616">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="1a7a9-617">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-617">Remarks - heightValue</span></span>

<span data-ttu-id="1a7a9-618">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-618">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="1a7a9-619">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="1a7a9-619">Method helpText</span></span>

<span data-ttu-id="1a7a9-620">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-620">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="1a7a9-621">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="1a7a9-621">Parameters - helpText</span></span>

<span data-ttu-id="1a7a9-622">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-622">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="1a7a9-623">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="1a7a9-623">Return Value - helpText</span></span>

<span data-ttu-id="1a7a9-624">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-624">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="1a7a9-625">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="1a7a9-625">Remarks - helpText</span></span>

<span data-ttu-id="1a7a9-626">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-626">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="1a7a9-627">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-627">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="1a7a9-628">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="1a7a9-628">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="1a7a9-629">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="1a7a9-629">Parameters - hierarchyParent</span></span>

<span data-ttu-id="1a7a9-630">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-630">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="1a7a9-631">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="1a7a9-631">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="1a7a9-632">メソッド id</span><span class="sxs-lookup"><span data-stu-id="1a7a9-632">Method id</span></span>

<span data-ttu-id="1a7a9-633">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-633">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="1a7a9-634">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="1a7a9-634">Return Value - id</span></span>

<span data-ttu-id="1a7a9-635">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-635">The ID of the control.</span></span>

## <a name="method-imemode"></a><span data-ttu-id="1a7a9-636">メソッド iMEMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-636">Method iMEMode</span></span>

```xpp
public int iMEMode([int value])
```

### <a name="parameters---imemode"></a><span data-ttu-id="1a7a9-637">パラメーター - iMEMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-637">Parameters - iMEMode</span></span>

<span data-ttu-id="1a7a9-638">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-638">value</span></span>  

### <a name="return-value---imemode"></a><span data-ttu-id="1a7a9-639">戻り値 - iMEMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-639">Return Value - iMEMode</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="1a7a9-640">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="1a7a9-640">Method isContainer</span></span>

<span data-ttu-id="1a7a9-641">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-641">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="1a7a9-642">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="1a7a9-642">Return Value - isContainer</span></span>

<span data-ttu-id="1a7a9-643">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-643">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-italic"></a><span data-ttu-id="1a7a9-644">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="1a7a9-644">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="1a7a9-645">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="1a7a9-645">Parameters - italic</span></span>

<span data-ttu-id="1a7a9-646">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-646">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="1a7a9-647">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="1a7a9-647">Return Value - italic</span></span>

## <a name="method-label"></a><span data-ttu-id="1a7a9-648">メソッド label</span><span class="sxs-lookup"><span data-stu-id="1a7a9-648">Method label</span></span>

<span data-ttu-id="1a7a9-649">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-649">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="1a7a9-650">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="1a7a9-650">Parameters - label</span></span>

<span data-ttu-id="1a7a9-651">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-651">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="1a7a9-652">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="1a7a9-652">Return Value - label</span></span>

<span data-ttu-id="1a7a9-653">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-653">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="1a7a9-654">備考 - label</span><span class="sxs-lookup"><span data-stu-id="1a7a9-654">Remarks - label</span></span>

<span data-ttu-id="1a7a9-655">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-655">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="1a7a9-656">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-656">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelalignment"></a><span data-ttu-id="1a7a9-657">メソッド labelAlignment</span><span class="sxs-lookup"><span data-stu-id="1a7a9-657">Method labelAlignment</span></span>

```xpp
public int labelAlignment([int value])
```

### <a name="parameters---labelalignment"></a><span data-ttu-id="1a7a9-658">パラメーター - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="1a7a9-658">Parameters - labelAlignment</span></span>

<span data-ttu-id="1a7a9-659">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-659">value</span></span>  

### <a name="return-value---labelalignment"></a><span data-ttu-id="1a7a9-660">戻り値 - labelAlignment</span><span class="sxs-lookup"><span data-stu-id="1a7a9-660">Return Value - labelAlignment</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="1a7a9-661">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="1a7a9-661">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="1a7a9-662">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="1a7a9-662">Parameters - labelBold</span></span>

<span data-ttu-id="1a7a9-663">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-663">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="1a7a9-664">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="1a7a9-664">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="1a7a9-665">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="1a7a9-665">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="1a7a9-666">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="1a7a9-666">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="1a7a9-667">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-667">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="1a7a9-668">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="1a7a9-668">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="1a7a9-669">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="1a7a9-669">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="1a7a9-670">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="1a7a9-670">Parameters - labelFont</span></span>

<span data-ttu-id="1a7a9-671">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-671">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="1a7a9-672">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="1a7a9-672">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="1a7a9-673">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="1a7a9-673">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="1a7a9-674">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="1a7a9-674">Parameters - labelFontSize</span></span>

<span data-ttu-id="1a7a9-675">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-675">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="1a7a9-676">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="1a7a9-676">Return Value - labelFontSize</span></span>

## <a name="method-labelforegroundcolor"></a><span data-ttu-id="1a7a9-677">メソッド labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="1a7a9-677">Method labelForegroundColor</span></span>

```xpp
public int labelForegroundColor([int value])
```

### <a name="parameters---labelforegroundcolor"></a><span data-ttu-id="1a7a9-678">パラメーター - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="1a7a9-678">Parameters - labelForegroundColor</span></span>

<span data-ttu-id="1a7a9-679">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-679">value</span></span>  

### <a name="return-value---labelforegroundcolor"></a><span data-ttu-id="1a7a9-680">戻り値 - labelForegroundColor</span><span class="sxs-lookup"><span data-stu-id="1a7a9-680">Return Value - labelForegroundColor</span></span>

## <a name="method-labelguide"></a><span data-ttu-id="1a7a9-681">メソッド labelGuide</span><span class="sxs-lookup"><span data-stu-id="1a7a9-681">Method labelGuide</span></span>

```xpp
public int labelGuide([int value])
```

### <a name="parameters---labelguide"></a><span data-ttu-id="1a7a9-682">パラメーター - labelGuide</span><span class="sxs-lookup"><span data-stu-id="1a7a9-682">Parameters - labelGuide</span></span>

<span data-ttu-id="1a7a9-683">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-683">value</span></span>  

### <a name="return-value---labelguide"></a><span data-ttu-id="1a7a9-684">戻り値 - labelGuide</span><span class="sxs-lookup"><span data-stu-id="1a7a9-684">Return Value - labelGuide</span></span>

## <a name="method-labelheight"></a><span data-ttu-id="1a7a9-685">メソッド labelHeight</span><span class="sxs-lookup"><span data-stu-id="1a7a9-685">Method labelHeight</span></span>

```xpp
public int labelHeight(int value, [int mode])
```

### <a name="parameters---labelheight"></a><span data-ttu-id="1a7a9-686">パラメーター - labelHeight</span><span class="sxs-lookup"><span data-stu-id="1a7a9-686">Parameters - labelHeight</span></span>

<span data-ttu-id="1a7a9-687">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-687">value</span></span>  

<!-- -->

<span data-ttu-id="1a7a9-688">モード</span><span class="sxs-lookup"><span data-stu-id="1a7a9-688">mode</span></span>  

### <a name="return-value---labelheight"></a><span data-ttu-id="1a7a9-689">戻り値 - labelHeight</span><span class="sxs-lookup"><span data-stu-id="1a7a9-689">Return Value - labelHeight</span></span>

## <a name="method-labelheightmode"></a><span data-ttu-id="1a7a9-690">メソッド labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-690">Method labelHeightMode</span></span>

```xpp
public int labelHeightMode([int value])
```

### <a name="parameters---labelheightmode"></a><span data-ttu-id="1a7a9-691">パラメーター - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-691">Parameters - labelHeightMode</span></span>

<span data-ttu-id="1a7a9-692">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-692">value</span></span>  

### <a name="return-value---labelheightmode"></a><span data-ttu-id="1a7a9-693">戻り値 - labelHeightMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-693">Return Value - labelHeightMode</span></span>

## <a name="method-labelheightvalue"></a><span data-ttu-id="1a7a9-694">メソッド labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-694">Method labelHeightValue</span></span>

```xpp
public int labelHeightValue([int value])
```

### <a name="parameters---labelheightvalue"></a><span data-ttu-id="1a7a9-695">パラメーター - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-695">Parameters - labelHeightValue</span></span>

<span data-ttu-id="1a7a9-696">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-696">value</span></span>  

### <a name="return-value---labelheightvalue"></a><span data-ttu-id="1a7a9-697">戻り値 - labelHeightValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-697">Return Value - labelHeightValue</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="1a7a9-698">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="1a7a9-698">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="1a7a9-699">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="1a7a9-699">Parameters - labelItalic</span></span>

<span data-ttu-id="1a7a9-700">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-700">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="1a7a9-701">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="1a7a9-701">Return Value - labelItalic</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="1a7a9-702">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="1a7a9-702">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="1a7a9-703">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="1a7a9-703">Parameters - labelPosition</span></span>

<span data-ttu-id="1a7a9-704">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-704">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="1a7a9-705">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="1a7a9-705">Return Value - labelPosition</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="1a7a9-706">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="1a7a9-706">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="1a7a9-707">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="1a7a9-707">Parameters - labelUnderline</span></span>

<span data-ttu-id="1a7a9-708">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-708">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="1a7a9-709">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="1a7a9-709">Return Value - labelUnderline</span></span>

## <a name="method-labelwidth"></a><span data-ttu-id="1a7a9-710">メソッド labelWidth</span><span class="sxs-lookup"><span data-stu-id="1a7a9-710">Method labelWidth</span></span>

```xpp
public int labelWidth(int value, [int mode])
```

### <a name="parameters---labelwidth"></a><span data-ttu-id="1a7a9-711">パラメーター - labelWidth</span><span class="sxs-lookup"><span data-stu-id="1a7a9-711">Parameters - labelWidth</span></span>

<span data-ttu-id="1a7a9-712">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-712">value</span></span>  

<!-- -->

<span data-ttu-id="1a7a9-713">モード</span><span class="sxs-lookup"><span data-stu-id="1a7a9-713">mode</span></span>  

### <a name="return-value---labelwidth"></a><span data-ttu-id="1a7a9-714">戻り値 - labelWidth</span><span class="sxs-lookup"><span data-stu-id="1a7a9-714">Return Value - labelWidth</span></span>

## <a name="method-labelwidthmode"></a><span data-ttu-id="1a7a9-715">メソッド labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-715">Method labelWidthMode</span></span>

```xpp
public int labelWidthMode([int value])
```

### <a name="parameters---labelwidthmode"></a><span data-ttu-id="1a7a9-716">パラメーター - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-716">Parameters - labelWidthMode</span></span>

<span data-ttu-id="1a7a9-717">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-717">value</span></span>  

### <a name="return-value---labelwidthmode"></a><span data-ttu-id="1a7a9-718">戻り値 - labelWidthMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-718">Return Value - labelWidthMode</span></span>

## <a name="method-labelwidthvalue"></a><span data-ttu-id="1a7a9-719">メソッド labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-719">Method labelWidthValue</span></span>

```xpp
public int labelWidthValue([int value])
```

### <a name="parameters---labelwidthvalue"></a><span data-ttu-id="1a7a9-720">パラメーター - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-720">Parameters - labelWidthValue</span></span>

<span data-ttu-id="1a7a9-721">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-721">value</span></span>  

### <a name="return-value---labelwidthvalue"></a><span data-ttu-id="1a7a9-722">戻り値 - labelWidthValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-722">Return Value - labelWidthValue</span></span>

## <a name="method-left"></a><span data-ttu-id="1a7a9-723">メソッド left</span><span class="sxs-lookup"><span data-stu-id="1a7a9-723">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="1a7a9-724">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="1a7a9-724">Parameters - left</span></span>

<span data-ttu-id="1a7a9-725">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-725">value</span></span>  

<!-- -->

<span data-ttu-id="1a7a9-726">モード</span><span class="sxs-lookup"><span data-stu-id="1a7a9-726">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="1a7a9-727">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="1a7a9-727">Return Value - left</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="1a7a9-728">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-728">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="1a7a9-729">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-729">Parameters - leftMode</span></span>

<span data-ttu-id="1a7a9-730">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-730">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="1a7a9-731">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-731">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="1a7a9-732">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-732">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="1a7a9-733">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-733">Parameters - leftValue</span></span>

<span data-ttu-id="1a7a9-734">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-734">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="1a7a9-735">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-735">Return Value - leftValue</span></span>

## <a name="method-limittext"></a><span data-ttu-id="1a7a9-736">メソッド limitText</span><span class="sxs-lookup"><span data-stu-id="1a7a9-736">Method limitText</span></span>

```xpp
public int limitText([int value], [AutoMode mode])
```

### <a name="parameters---limittext"></a><span data-ttu-id="1a7a9-737">パラメーター - limitText</span><span class="sxs-lookup"><span data-stu-id="1a7a9-737">Parameters - limitText</span></span>

<span data-ttu-id="1a7a9-738">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-738">value</span></span>  

<!-- -->

<span data-ttu-id="1a7a9-739">モード</span><span class="sxs-lookup"><span data-stu-id="1a7a9-739">mode</span></span>  

### <a name="return-value---limittext"></a><span data-ttu-id="1a7a9-740">戻り値 - limitText</span><span class="sxs-lookup"><span data-stu-id="1a7a9-740">Return Value - limitText</span></span>

## <a name="method-limittextmode"></a><span data-ttu-id="1a7a9-741">メソッド limitTextMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-741">Method limitTextMode</span></span>

```xpp
public AutoMode limitTextMode([AutoMode mode])
```

### <a name="parameters---limittextmode"></a><span data-ttu-id="1a7a9-742">パラメーター - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-742">Parameters - limitTextMode</span></span>

<span data-ttu-id="1a7a9-743">モード</span><span class="sxs-lookup"><span data-stu-id="1a7a9-743">mode</span></span>  

### <a name="return-value---limittextmode"></a><span data-ttu-id="1a7a9-744">戻り値 - limitTextMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-744">Return Value - limitTextMode</span></span>

## <a name="method-limittextvalue"></a><span data-ttu-id="1a7a9-745">メソッド limitTextValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-745">Method limitTextValue</span></span>

```xpp
public int limitTextValue([int value])
```

### <a name="parameters---limittextvalue"></a><span data-ttu-id="1a7a9-746">パラメーター - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-746">Parameters - limitTextValue</span></span>

<span data-ttu-id="1a7a9-747">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-747">value</span></span>  

### <a name="return-value---limittextvalue"></a><span data-ttu-id="1a7a9-748">戻り値 - limitTextValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-748">Return Value - limitTextValue</span></span>

## <a name="method-lookupbutton"></a><span data-ttu-id="1a7a9-749">メソッド lookupButton</span><span class="sxs-lookup"><span data-stu-id="1a7a9-749">Method lookupButton</span></span>

```xpp
public int lookupButton([int value])
```

### <a name="parameters---lookupbutton"></a><span data-ttu-id="1a7a9-750">パラメーター - lookupButton</span><span class="sxs-lookup"><span data-stu-id="1a7a9-750">Parameters - lookupButton</span></span>

<span data-ttu-id="1a7a9-751">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-751">value</span></span>  

### <a name="return-value---lookupbutton"></a><span data-ttu-id="1a7a9-752">戻り値 - lookupButton</span><span class="sxs-lookup"><span data-stu-id="1a7a9-752">Return Value - lookupButton</span></span>

## <a name="method-mandatory"></a><span data-ttu-id="1a7a9-753">メソッド mandatory</span><span class="sxs-lookup"><span data-stu-id="1a7a9-753">Method mandatory</span></span>

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a><span data-ttu-id="1a7a9-754">パラメーター - mandatory</span><span class="sxs-lookup"><span data-stu-id="1a7a9-754">Parameters - mandatory</span></span>

<span data-ttu-id="1a7a9-755">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-755">value</span></span>  

### <a name="return-value---mandatory"></a><span data-ttu-id="1a7a9-756">戻り値 - mandatory</span><span class="sxs-lookup"><span data-stu-id="1a7a9-756">Return Value - mandatory</span></span>

## <a name="method-minnoofdecimals"></a><span data-ttu-id="1a7a9-757">メソッド minNoOfDecimals</span><span class="sxs-lookup"><span data-stu-id="1a7a9-757">Method minNoOfDecimals</span></span>

```xpp
public int minNoOfDecimals([int value], [AutoMode mode])
```

### <a name="parameters---minnoofdecimals"></a><span data-ttu-id="1a7a9-758">パラメーター - minNoOfDecimals</span><span class="sxs-lookup"><span data-stu-id="1a7a9-758">Parameters - minNoOfDecimals</span></span>

<span data-ttu-id="1a7a9-759">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-759">value</span></span>  

<!-- -->

<span data-ttu-id="1a7a9-760">モード</span><span class="sxs-lookup"><span data-stu-id="1a7a9-760">mode</span></span>  

### <a name="return-value---minnoofdecimals"></a><span data-ttu-id="1a7a9-761">戻り値 - minNoOfDecimals</span><span class="sxs-lookup"><span data-stu-id="1a7a9-761">Return Value - minNoOfDecimals</span></span>

## <a name="method-minnoofdecimalsmode"></a><span data-ttu-id="1a7a9-762">メソッド minNoOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-762">Method minNoOfDecimalsMode</span></span>

```xpp
public AutoMode minNoOfDecimalsMode([AutoMode mode])
```

### <a name="parameters---minnoofdecimalsmode"></a><span data-ttu-id="1a7a9-763">パラメーター - minNoOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-763">Parameters - minNoOfDecimalsMode</span></span>

<span data-ttu-id="1a7a9-764">モード</span><span class="sxs-lookup"><span data-stu-id="1a7a9-764">mode</span></span>  

### <a name="return-value---minnoofdecimalsmode"></a><span data-ttu-id="1a7a9-765">戻り値 - minNoOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-765">Return Value - minNoOfDecimalsMode</span></span>

## <a name="method-minnoofdecimalsvalue"></a><span data-ttu-id="1a7a9-766">メソッド minNoOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-766">Method minNoOfDecimalsValue</span></span>

```xpp
public int minNoOfDecimalsValue([int value])
```

### <a name="parameters---minnoofdecimalsvalue"></a><span data-ttu-id="1a7a9-767">パラメーター - minNoOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-767">Parameters - minNoOfDecimalsValue</span></span>

<span data-ttu-id="1a7a9-768">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-768">value</span></span>  

### <a name="return-value---minnoofdecimalsvalue"></a><span data-ttu-id="1a7a9-769">戻り値 - minNoOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-769">Return Value - minNoOfDecimalsValue</span></span>

## <a name="method-name"></a><span data-ttu-id="1a7a9-770">メソッド名</span><span class="sxs-lookup"><span data-stu-id="1a7a9-770">Method name</span></span>

<span data-ttu-id="1a7a9-771">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-771">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="1a7a9-772">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="1a7a9-772">Parameters - name</span></span>

<span data-ttu-id="1a7a9-773">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-773">value</span></span>  
<span data-ttu-id="1a7a9-774">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-774">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="1a7a9-775">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="1a7a9-775">Return Value - name</span></span>

<span data-ttu-id="1a7a9-776">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-776">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="1a7a9-777">備考 - name</span><span class="sxs-lookup"><span data-stu-id="1a7a9-777">Remarks - name</span></span>

<span data-ttu-id="1a7a9-778">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-778">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="1a7a9-779">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-779">It must start with a letter.</span></span>
-   <span data-ttu-id="1a7a9-780">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-780">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="1a7a9-781">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-781">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="1a7a9-782">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-782">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="1a7a9-783">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-783">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="1a7a9-784">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="1a7a9-784">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="1a7a9-785">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="1a7a9-785">Parameters - neededPermission</span></span>

<span data-ttu-id="1a7a9-786">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-786">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="1a7a9-787">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="1a7a9-787">Return Value - neededPermission</span></span>

## <a name="method-noofdecimals"></a><span data-ttu-id="1a7a9-788">メソッド noOfDecimals</span><span class="sxs-lookup"><span data-stu-id="1a7a9-788">Method noOfDecimals</span></span>

```xpp
public int noOfDecimals([int value], [AutoMode mode])
```

### <a name="parameters---noofdecimals"></a><span data-ttu-id="1a7a9-789">パラメーター - noOfDecimals</span><span class="sxs-lookup"><span data-stu-id="1a7a9-789">Parameters - noOfDecimals</span></span>

<span data-ttu-id="1a7a9-790">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-790">value</span></span>  

<!-- -->

<span data-ttu-id="1a7a9-791">モード</span><span class="sxs-lookup"><span data-stu-id="1a7a9-791">mode</span></span>  

### <a name="return-value---noofdecimals"></a><span data-ttu-id="1a7a9-792">戻り値 - noOfDecimals</span><span class="sxs-lookup"><span data-stu-id="1a7a9-792">Return Value - noOfDecimals</span></span>

## <a name="method-noofdecimalsmode"></a><span data-ttu-id="1a7a9-793">メソッド noOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-793">Method noOfDecimalsMode</span></span>

```xpp
public AutoMode noOfDecimalsMode([AutoMode mode])
```

### <a name="parameters---noofdecimalsmode"></a><span data-ttu-id="1a7a9-794">パラメーター - noOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-794">Parameters - noOfDecimalsMode</span></span>

<span data-ttu-id="1a7a9-795">モード</span><span class="sxs-lookup"><span data-stu-id="1a7a9-795">mode</span></span>  

### <a name="return-value---noofdecimalsmode"></a><span data-ttu-id="1a7a9-796">戻り値 - noOfDecimalsMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-796">Return Value - noOfDecimalsMode</span></span>

## <a name="method-noofdecimalsvalue"></a><span data-ttu-id="1a7a9-797">メソッド noOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-797">Method noOfDecimalsValue</span></span>

```xpp
public int noOfDecimalsValue([int value])
```

### <a name="parameters---noofdecimalsvalue"></a><span data-ttu-id="1a7a9-798">パラメーター - noOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-798">Parameters - noOfDecimalsValue</span></span>

<span data-ttu-id="1a7a9-799">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-799">value</span></span>  

### <a name="return-value---noofdecimalsvalue"></a><span data-ttu-id="1a7a9-800">戻り値 - noOfDecimalsValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-800">Return Value - noOfDecimalsValue</span></span>

## <a name="method-promptrect"></a><span data-ttu-id="1a7a9-801">メソッド promptrect</span><span class="sxs-lookup"><span data-stu-id="1a7a9-801">Method promptrect</span></span>

```xpp
public int promptrect([int value])
```

### <a name="parameters---promptrect"></a><span data-ttu-id="1a7a9-802">パラメーター - promptrect</span><span class="sxs-lookup"><span data-stu-id="1a7a9-802">Parameters - promptrect</span></span>

<span data-ttu-id="1a7a9-803">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-803">value</span></span>  

### <a name="return-value---promptrect"></a><span data-ttu-id="1a7a9-804">戻り値 - promptrect</span><span class="sxs-lookup"><span data-stu-id="1a7a9-804">Return Value - promptrect</span></span>

## <a name="method-realvalue"></a><span data-ttu-id="1a7a9-805">メソッド realValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-805">Method realValue</span></span>

```xpp
public Real realValue([Real value])
```

### <a name="parameters---realvalue"></a><span data-ttu-id="1a7a9-806">パラメーター - realValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-806">Parameters - realValue</span></span>

<span data-ttu-id="1a7a9-807">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-807">value</span></span>  

### <a name="return-value---realvalue"></a><span data-ttu-id="1a7a9-808">戻り値 - realValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-808">Return Value - realValue</span></span>

## <a name="method-replaceonlookup"></a><span data-ttu-id="1a7a9-809">メソッド replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="1a7a9-809">Method replaceOnLookup</span></span>

```xpp
public boolean replaceOnLookup([boolean value])
```

### <a name="parameters---replaceonlookup"></a><span data-ttu-id="1a7a9-810">パラメーター - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="1a7a9-810">Parameters - replaceOnLookup</span></span>

<span data-ttu-id="1a7a9-811">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-811">value</span></span>  

### <a name="return-value---replaceonlookup"></a><span data-ttu-id="1a7a9-812">戻り値 - replaceOnLookup</span><span class="sxs-lookup"><span data-stu-id="1a7a9-812">Return Value - replaceOnLookup</span></span>

## <a name="method-rotatesign"></a><span data-ttu-id="1a7a9-813">メソッド rotateSign</span><span class="sxs-lookup"><span data-stu-id="1a7a9-813">Method rotateSign</span></span>

```xpp
public int rotateSign([int value])
```

### <a name="parameters---rotatesign"></a><span data-ttu-id="1a7a9-814">パラメーター - rotateSign</span><span class="sxs-lookup"><span data-stu-id="1a7a9-814">Parameters - rotateSign</span></span>

<span data-ttu-id="1a7a9-815">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-815">value</span></span>  

### <a name="return-value---rotatesign"></a><span data-ttu-id="1a7a9-816">戻り値 - rotateSign</span><span class="sxs-lookup"><span data-stu-id="1a7a9-816">Return Value - rotateSign</span></span>

## <a name="method-searchafterinput"></a><span data-ttu-id="1a7a9-817">メソッド searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="1a7a9-817">Method searchAfterInput</span></span>

```xpp
public int searchAfterInput([int value])
```

### <a name="parameters---searchafterinput"></a><span data-ttu-id="1a7a9-818">パラメーター - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="1a7a9-818">Parameters - searchAfterInput</span></span>

<span data-ttu-id="1a7a9-819">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-819">value</span></span>  

### <a name="return-value---searchafterinput"></a><span data-ttu-id="1a7a9-820">戻り値 - searchAfterInput</span><span class="sxs-lookup"><span data-stu-id="1a7a9-820">Return Value - searchAfterInput</span></span>

## <a name="method-searchmode"></a><span data-ttu-id="1a7a9-821">メソッド searchMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-821">Method searchMode</span></span>

```xpp
public int searchMode([int value])
```

### <a name="parameters---searchmode"></a><span data-ttu-id="1a7a9-822">パラメーター - searchMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-822">Parameters - searchMode</span></span>

<span data-ttu-id="1a7a9-823">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-823">value</span></span>  

### <a name="return-value---searchmode"></a><span data-ttu-id="1a7a9-824">戻り値 - searchMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-824">Return Value - searchMode</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="1a7a9-825">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="1a7a9-825">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="1a7a9-826">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="1a7a9-826">Parameters - securityKey</span></span>

<span data-ttu-id="1a7a9-827">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-827">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="1a7a9-828">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="1a7a9-828">Return Value - securityKey</span></span>

## <a name="method-showlabel"></a><span data-ttu-id="1a7a9-829">メソッド showLabel</span><span class="sxs-lookup"><span data-stu-id="1a7a9-829">Method showLabel</span></span>

```xpp
public boolean showLabel([boolean value])
```

### <a name="parameters---showlabel"></a><span data-ttu-id="1a7a9-830">パラメーター - showLabel</span><span class="sxs-lookup"><span data-stu-id="1a7a9-830">Parameters - showLabel</span></span>

<span data-ttu-id="1a7a9-831">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-831">value</span></span>  

### <a name="return-value---showlabel"></a><span data-ttu-id="1a7a9-832">戻り値 - showLabel</span><span class="sxs-lookup"><span data-stu-id="1a7a9-832">Return Value - showLabel</span></span>

## <a name="method-showzero"></a><span data-ttu-id="1a7a9-833">メソッド showZero</span><span class="sxs-lookup"><span data-stu-id="1a7a9-833">Method showZero</span></span>

```xpp
public int showZero([int value])
```

### <a name="parameters---showzero"></a><span data-ttu-id="1a7a9-834">パラメーター - showZero</span><span class="sxs-lookup"><span data-stu-id="1a7a9-834">Parameters - showZero</span></span>

<span data-ttu-id="1a7a9-835">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-835">value</span></span>  

### <a name="return-value---showzero"></a><span data-ttu-id="1a7a9-836">戻り値 - showZero</span><span class="sxs-lookup"><span data-stu-id="1a7a9-836">Return Value - showZero</span></span>

## <a name="method-signdisplay"></a><span data-ttu-id="1a7a9-837">メソッド signDisplay</span><span class="sxs-lookup"><span data-stu-id="1a7a9-837">Method signDisplay</span></span>

```xpp
public int signDisplay([int value])
```

### <a name="parameters---signdisplay"></a><span data-ttu-id="1a7a9-838">パラメーター - signDisplay</span><span class="sxs-lookup"><span data-stu-id="1a7a9-838">Parameters - signDisplay</span></span>

<span data-ttu-id="1a7a9-839">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-839">value</span></span>  

### <a name="return-value---signdisplay"></a><span data-ttu-id="1a7a9-840">戻り値 - signDisplay</span><span class="sxs-lookup"><span data-stu-id="1a7a9-840">Return Value - signDisplay</span></span>

## <a name="method-skip"></a><span data-ttu-id="1a7a9-841">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="1a7a9-841">Method skip</span></span>

<span data-ttu-id="1a7a9-842">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-842">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="1a7a9-843">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="1a7a9-843">Parameters - skip</span></span>

<span data-ttu-id="1a7a9-844">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-844">value</span></span>  
<span data-ttu-id="1a7a9-845">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-845">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="1a7a9-846">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="1a7a9-846">Return Value - skip</span></span>

<span data-ttu-id="1a7a9-847">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-847">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-style"></a><span data-ttu-id="1a7a9-848">メソッド style</span><span class="sxs-lookup"><span data-stu-id="1a7a9-848">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="1a7a9-849">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="1a7a9-849">Parameters - style</span></span>

<span data-ttu-id="1a7a9-850">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-850">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="1a7a9-851">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="1a7a9-851">Return Value - style</span></span>

## <a name="method-thousandseparator"></a><span data-ttu-id="1a7a9-852">メソッド thousandSeparator</span><span class="sxs-lookup"><span data-stu-id="1a7a9-852">Method thousandSeparator</span></span>

```xpp
public int thousandSeparator([int value])
```

### <a name="parameters---thousandseparator"></a><span data-ttu-id="1a7a9-853">パラメーター - thousandSeparator</span><span class="sxs-lookup"><span data-stu-id="1a7a9-853">Parameters - thousandSeparator</span></span>

<span data-ttu-id="1a7a9-854">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-854">value</span></span>  

### <a name="return-value---thousandseparator"></a><span data-ttu-id="1a7a9-855">戻り値 - thousandSeparator</span><span class="sxs-lookup"><span data-stu-id="1a7a9-855">Return Value - thousandSeparator</span></span>

## <a name="method-top"></a><span data-ttu-id="1a7a9-856">メソッド top</span><span class="sxs-lookup"><span data-stu-id="1a7a9-856">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="1a7a9-857">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="1a7a9-857">Parameters - top</span></span>

<span data-ttu-id="1a7a9-858">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-858">value</span></span>  

<!-- -->

<span data-ttu-id="1a7a9-859">モード</span><span class="sxs-lookup"><span data-stu-id="1a7a9-859">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="1a7a9-860">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="1a7a9-860">Return Value - top</span></span>

## <a name="method-topmode"></a><span data-ttu-id="1a7a9-861">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-861">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="1a7a9-862">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-862">Parameters - topMode</span></span>

<span data-ttu-id="1a7a9-863">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-863">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="1a7a9-864">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-864">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="1a7a9-865">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-865">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="1a7a9-866">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-866">Parameters - topValue</span></span>

<span data-ttu-id="1a7a9-867">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-867">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="1a7a9-868">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-868">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="1a7a9-869">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="1a7a9-869">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="1a7a9-870">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="1a7a9-870">Parameters - type</span></span>

<span data-ttu-id="1a7a9-871">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-871">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="1a7a9-872">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="1a7a9-872">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="1a7a9-873">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="1a7a9-873">Method underline</span></span>

<span data-ttu-id="1a7a9-874">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-874">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="1a7a9-875">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="1a7a9-875">Parameters - underline</span></span>

<span data-ttu-id="1a7a9-876">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-876">value</span></span>  
<span data-ttu-id="1a7a9-877">コントロールの underline プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-877">The value to assign to the underline property of the control; optional.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="1a7a9-878">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="1a7a9-878">Return Value - underline</span></span>

<span data-ttu-id="1a7a9-879">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-879">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-userdata"></a><span data-ttu-id="1a7a9-880">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="1a7a9-880">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="1a7a9-881">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="1a7a9-881">Parameters - userData</span></span>

<span data-ttu-id="1a7a9-882">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-882">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="1a7a9-883">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="1a7a9-883">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="1a7a9-884">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="1a7a9-884">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="1a7a9-885">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="1a7a9-885">Parameters - userDataItem</span></span>

<span data-ttu-id="1a7a9-886">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-886">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="1a7a9-887">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="1a7a9-887">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="1a7a9-888">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="1a7a9-888">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="1a7a9-889">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="1a7a9-889">Parameters - userDataItems</span></span>

<span data-ttu-id="1a7a9-890">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-890">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="1a7a9-891">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="1a7a9-891">Return Value - userDataItems</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="1a7a9-892">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="1a7a9-892">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="1a7a9-893">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="1a7a9-893">Parameters - verticalSpacing</span></span>

<span data-ttu-id="1a7a9-894">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-894">value</span></span>  

<!-- -->

<span data-ttu-id="1a7a9-895">モード</span><span class="sxs-lookup"><span data-stu-id="1a7a9-895">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="1a7a9-896">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="1a7a9-896">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="1a7a9-897">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-897">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="1a7a9-898">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-898">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="1a7a9-899">モード</span><span class="sxs-lookup"><span data-stu-id="1a7a9-899">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="1a7a9-900">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-900">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="1a7a9-901">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-901">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="1a7a9-902">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-902">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="1a7a9-903">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-903">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="1a7a9-904">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-904">Return Value - verticalSpacingValue</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="1a7a9-905">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-905">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="1a7a9-906">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-906">Parameters - viewEditMode</span></span>

<span data-ttu-id="1a7a9-907">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-907">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="1a7a9-908">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-908">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="1a7a9-909">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="1a7a9-909">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="1a7a9-910">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="1a7a9-910">Parameters - visible</span></span>

<span data-ttu-id="1a7a9-911">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-911">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="1a7a9-912">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="1a7a9-912">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="1a7a9-913">メソッド width</span><span class="sxs-lookup"><span data-stu-id="1a7a9-913">Method width</span></span>

<span data-ttu-id="1a7a9-914">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-914">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="1a7a9-915">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="1a7a9-915">Parameters - width</span></span>

<span data-ttu-id="1a7a9-916">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-916">value</span></span>  

<!-- -->

<span data-ttu-id="1a7a9-917">モード</span><span class="sxs-lookup"><span data-stu-id="1a7a9-917">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="1a7a9-918">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="1a7a9-918">Return Value - width</span></span>

<span data-ttu-id="1a7a9-919">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-919">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="1a7a9-920">備考 - width</span><span class="sxs-lookup"><span data-stu-id="1a7a9-920">Remarks - width</span></span>

<span data-ttu-id="1a7a9-921">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-921">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="1a7a9-922">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="1a7a9-922">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="1a7a9-923">モード。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-923">Mode.</span></span>           | <span data-ttu-id="1a7a9-924">幅計算。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-924">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a7a9-925">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-925">-1 Exact.</span></span>       | <span data-ttu-id="1a7a9-926">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-926">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="1a7a9-927">0 自動。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-927">0 Auto.</span></span>         | <span data-ttu-id="1a7a9-928">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-928">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="1a7a9-929">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-929">1 Column width.</span></span> | <span data-ttu-id="1a7a9-930">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-930">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="1a7a9-931">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-931">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="1a7a9-932">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-932">Method widthMode</span></span>

<span data-ttu-id="1a7a9-933">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-933">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="1a7a9-934">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-934">Parameters - widthMode</span></span>

<span data-ttu-id="1a7a9-935">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-935">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="1a7a9-936">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-936">Return Value - widthMode</span></span>

<span data-ttu-id="1a7a9-937">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-937">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="1a7a9-938">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="1a7a9-938">Remarks - widthMode</span></span>

<span data-ttu-id="1a7a9-939">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="1a7a9-939">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="1a7a9-940">モード。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-940">Mode.</span></span>         | <span data-ttu-id="1a7a9-941">幅計算。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-941">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a7a9-942">正確。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-942">Exact.</span></span>        | <span data-ttu-id="1a7a9-943">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-943">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="1a7a9-944">自動。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-944">Auto.</span></span>         | <span data-ttu-id="1a7a9-945">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-945">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="1a7a9-946">列の幅。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-946">Column width.</span></span> | <span data-ttu-id="1a7a9-947">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-947">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="1a7a9-948">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-948">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="1a7a9-949">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-949">Method widthValue</span></span>

<span data-ttu-id="1a7a9-950">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-950">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="1a7a9-951">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-951">Parameters - widthValue</span></span>

<span data-ttu-id="1a7a9-952">値</span><span class="sxs-lookup"><span data-stu-id="1a7a9-952">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="1a7a9-953">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-953">Return Value - widthValue</span></span>

<span data-ttu-id="1a7a9-954">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-954">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="1a7a9-955">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="1a7a9-955">Remarks - widthValue</span></span>

<span data-ttu-id="1a7a9-956">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="1a7a9-956">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="1a7a9-957">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="1a7a9-957">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="1a7a9-958">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="1a7a9-958">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="1a7a9-959">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="1a7a9-959">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="1a7a9-960">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="1a7a9-960">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="1a7a9-961">overrideObject</span><span class="sxs-lookup"><span data-stu-id="1a7a9-961">overrideObject</span></span>  



