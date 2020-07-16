---
title: FormBuildGroupControl クラス
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
ms.openlocfilehash: 599b16ccc0b5a55d43b513297840debc30b9d264
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502648"
---
# <a name="class-formbuildgroupcontrol"></a><span data-ttu-id="172b0-103">クラス FormBuildGroupControl</span><span class="sxs-lookup"><span data-stu-id="172b0-103">Class FormBuildGroupControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildGroupControl extends FormBuildControl
```

<span data-ttu-id="172b0-104">FormBuildGroupControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="172b0-104">The FormBuildGroupControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="172b0-105">備考</span><span class="sxs-lookup"><span data-stu-id="172b0-105">Remarks</span></span>

<span data-ttu-id="172b0-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="172b0-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="172b0-107">例</span><span class="sxs-lookup"><span data-stu-id="172b0-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="172b0-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="172b0-108">Methods</span></span>

| <span data-ttu-id="172b0-109">方法</span><span class="sxs-lookup"><span data-stu-id="172b0-109">Method</span></span>                                                                                                      | <span data-ttu-id="172b0-110">説明</span><span class="sxs-lookup"><span data-stu-id="172b0-110">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="172b0-111">public boolean alignChild(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-111">public boolean alignChild(\[boolean value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="172b0-112">public boolean alignChildren(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-112">public boolean alignChildren(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="172b0-113">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-113">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="172b0-114">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-114">Determines whether to align the control.</span></span>                                                                                                |
| <span data-ttu-id="172b0-115">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-115">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="172b0-116">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-116">Determines whether the user can change the contents of the control.</span></span>                                                                     |
| <span data-ttu-id="172b0-117">public int allowUserSetup(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-117">public int allowUserSetup(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="172b0-118">public int arrangeGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-118">public int arrangeGuide(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="172b0-119">public int arrangeMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-119">public int arrangeMethod(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="172b0-120">public int arrangeWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-120">public int arrangeWhen(\[int value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="172b0-121">public boolean autoDataGroup(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-121">public boolean autoDataGroup(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="172b0-122">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-122">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="172b0-123">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-123">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                      |
| <span data-ttu-id="172b0-124">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-124">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="172b0-125">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-125">Gets or sets the background color of the control.</span></span>                                                                                       |
| <span data-ttu-id="172b0-126">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-126">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="172b0-127">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-127">Determines whether the control background can be transparent.</span></span>                                                                          |
| <span data-ttu-id="172b0-128">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-128">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="172b0-129">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-129">Gets or sets the weight of font that is used to output text in the control.</span></span>                                                             |
| <span data-ttu-id="172b0-130">public int bottomMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="172b0-130">public int bottomMargin(\[int value\], \[AutoMode mode\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="172b0-131">public AutoMode bottomMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="172b0-131">public AutoMode bottomMarginMode(\[AutoMode mode\])</span></span>                                                         |                                                                                                                                         |
| <span data-ttu-id="172b0-132">public int bottomMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-132">public int bottomMarginValue(\[int value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="172b0-133">public boolean breakable(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-133">public boolean breakable(\[boolean value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="172b0-134">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-134">public str caption(\[str value\])</span></span>                                                                           | <span data-ttu-id="172b0-135">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-135">Gets or set the caption of the control.</span></span>                                                                                                 |
| <span data-ttu-id="172b0-136">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-136">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="172b0-137">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-137">Gets or sets the character set of the font.</span></span>                                                                                             |
| <span data-ttu-id="172b0-138">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-138">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="172b0-139">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-139">Gets or sets the color scheme of the control.</span></span>                                                                                           |
| <span data-ttu-id="172b0-140">public int columns(\[int value\], \[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="172b0-140">public int columns(\[int value\], \[ColumnsMode mode\])</span></span>                                                     |                                                                                                                                         |
| <span data-ttu-id="172b0-141">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="172b0-141">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span></span>                                                        |                                                                                                                                         |
| <span data-ttu-id="172b0-142">public int columnspace(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="172b0-142">public int columnspace(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                         |
| <span data-ttu-id="172b0-143">public AutoMode columnspaceMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="172b0-143">public AutoMode columnspaceMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                         |
| <span data-ttu-id="172b0-144">public int columnspaceValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-144">public int columnspaceValue(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="172b0-145">public int columnsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-145">public int columnsValue(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="172b0-146">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-146">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="172b0-147">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-147">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                     |
| <span data-ttu-id="172b0-148">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="172b0-148">public int containerId()</span></span>                                                                                    | <span data-ttu-id="172b0-149">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="172b0-149">Retrieves the ID of the parent container for the control.</span></span>                                                                               |
| <span data-ttu-id="172b0-150">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-150">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="172b0-151">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-151">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                         |
| <span data-ttu-id="172b0-152">public str dataGroup(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-152">public str dataGroup(\[str value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="172b0-153">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-153">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="172b0-154">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-154">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="172b0-155">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-155">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                |
| <span data-ttu-id="172b0-156">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-156">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="172b0-157">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-157">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="172b0-158">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-158">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                       |
| <span data-ttu-id="172b0-159">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-159">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="172b0-160">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-160">Determines whether to enable or disable the object.</span></span>                                                                                     |
| <span data-ttu-id="172b0-161">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-161">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="172b0-162">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-162">Gets or sets the name of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="172b0-163">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-163">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="172b0-164">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-164">Gets or sets the size of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="172b0-165">public int frameOptionButton(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-165">public int frameOptionButton(\[int value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="172b0-166">public int framePosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-166">public int framePosition(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="172b0-167">public int frameType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-167">public int frameType(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="172b0-168">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="172b0-168">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="172b0-169">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-169">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="172b0-170">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-170">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="172b0-171">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-171">Gets or sets a calculation mode for the height of the control.</span></span>                                                                          |
| <span data-ttu-id="172b0-172">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-172">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="172b0-173">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-173">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="172b0-174">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-174">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="172b0-175">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-175">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                |
| <span data-ttu-id="172b0-176">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-176">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                               |                                                                                                                                         |
| <span data-ttu-id="172b0-177">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-177">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="172b0-178">public int id()</span><span class="sxs-lookup"><span data-stu-id="172b0-178">public int id()</span></span>                                                                                             | <span data-ttu-id="172b0-179">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="172b0-179">Retrieves the ID of the control.</span></span>                                                                                                        |
| <span data-ttu-id="172b0-180">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="172b0-180">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="172b0-181">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="172b0-181">Retrieves a value that indicates whether the control is a container control.</span></span>                                                            |
| <span data-ttu-id="172b0-182">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-182">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="172b0-183">public int labelBold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-183">public int labelBold(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="172b0-184">public int labelCharacterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-184">public int labelCharacterSet(\[int value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="172b0-185">public str labelFont(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-185">public str labelFont(\[str value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="172b0-186">public int labelFontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-186">public int labelFontSize(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="172b0-187">public boolean labelItalic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-187">public boolean labelItalic(\[boolean value\])</span></span>                                                               |                                                                                                                                         |
| <span data-ttu-id="172b0-188">public boolean labelUnderline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-188">public boolean labelUnderline(\[boolean value\])</span></span>                                                            |                                                                                                                                         |
| <span data-ttu-id="172b0-189">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="172b0-189">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="172b0-190">public int leftMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="172b0-190">public int leftMargin(\[int value\], \[AutoMode mode\])</span></span>                                                     |                                                                                                                                         |
| <span data-ttu-id="172b0-191">public AutoMode leftMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="172b0-191">public AutoMode leftMarginMode(\[AutoMode mode\])</span></span>                                                           |                                                                                                                                         |
| <span data-ttu-id="172b0-192">public int leftMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-192">public int leftMarginValue(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="172b0-193">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-193">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="172b0-194">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-194">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="172b0-195">public int moveControl(int controlId, \[int insertAfterControlId\])</span><span class="sxs-lookup"><span data-stu-id="172b0-195">public int moveControl(int controlId, \[int insertAfterControlId\])</span></span>                                         | <span data-ttu-id="172b0-196">コントロールに指定されたコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="172b0-196">Moves a specified control to the control.</span></span>                                                                                               |
| <span data-ttu-id="172b0-197">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-197">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="172b0-198">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-198">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="172b0-199">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-199">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="172b0-200">public int optionValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-200">public int optionValue(\[int value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="172b0-201">public int rightMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="172b0-201">public int rightMargin(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                         |
| <span data-ttu-id="172b0-202">public AutoMode rightMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="172b0-202">public AutoMode rightMarginMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                         |
| <span data-ttu-id="172b0-203">public int rightMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-203">public int rightMarginValue(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="172b0-204">public boolean saveFilter(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-204">public boolean saveFilter(\[boolean value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="172b0-205">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-205">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="172b0-206">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-206">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="172b0-207">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="172b0-207">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>         |
| <span data-ttu-id="172b0-208">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-208">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                         |
| <span data-ttu-id="172b0-209">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="172b0-209">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="172b0-210">public int topMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="172b0-210">public int topMargin(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="172b0-211">public AutoMode topMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="172b0-211">public AutoMode topMarginMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                         |
| <span data-ttu-id="172b0-212">public int topMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-212">public int topMarginValue(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="172b0-213">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-213">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="172b0-214">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-214">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="172b0-215">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-215">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="172b0-216">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-216">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="172b0-217">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="172b0-217">Sets or returns the underline property for the text in the control.</span></span>                                                                     |
| <span data-ttu-id="172b0-218">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-218">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="172b0-219">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-219">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="172b0-220">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-220">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="172b0-221">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-221">public boolean useUserLayout(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="172b0-222">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="172b0-222">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="172b0-223">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="172b0-223">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="172b0-224">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-224">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="172b0-225">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-225">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="172b0-226">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-226">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="172b0-227">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="172b0-227">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="172b0-228">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-228">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="172b0-229">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-229">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="172b0-230">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-230">Gets or sets the calculation mode of the width of the control.</span></span>                                                                          |
| <span data-ttu-id="172b0-231">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="172b0-231">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="172b0-232">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-232">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="172b0-233">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="172b0-233">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                         |

## <a name="method-alignchild"></a><span data-ttu-id="172b0-234">メソッド alignChild</span><span class="sxs-lookup"><span data-stu-id="172b0-234">Method alignChild</span></span>

```xpp
public boolean alignChild([boolean value])
```

### <a name="parameters---alignchild"></a><span data-ttu-id="172b0-235">パラメーター - alignChild</span><span class="sxs-lookup"><span data-stu-id="172b0-235">Parameters - alignChild</span></span>

<span data-ttu-id="172b0-236">値</span><span class="sxs-lookup"><span data-stu-id="172b0-236">value</span></span>  

### <a name="return-value---alignchild"></a><span data-ttu-id="172b0-237">戻り値 - alignChild</span><span class="sxs-lookup"><span data-stu-id="172b0-237">Return Value - alignChild</span></span>

## <a name="method-alignchildren"></a><span data-ttu-id="172b0-238">メソッド alignChildren</span><span class="sxs-lookup"><span data-stu-id="172b0-238">Method alignChildren</span></span>

```xpp
public boolean alignChildren([boolean value])
```

### <a name="parameters---alignchildren"></a><span data-ttu-id="172b0-239">パラメーター - alignChildren</span><span class="sxs-lookup"><span data-stu-id="172b0-239">Parameters - alignChildren</span></span>

<span data-ttu-id="172b0-240">値</span><span class="sxs-lookup"><span data-stu-id="172b0-240">value</span></span>  

### <a name="return-value---alignchildren"></a><span data-ttu-id="172b0-241">戻り値 - alignChildren</span><span class="sxs-lookup"><span data-stu-id="172b0-241">Return Value - alignChildren</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="172b0-242">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="172b0-242">Method alignControl</span></span>

<span data-ttu-id="172b0-243">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-243">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="172b0-244">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="172b0-244">Parameters - alignControl</span></span>

<span data-ttu-id="172b0-245">値</span><span class="sxs-lookup"><span data-stu-id="172b0-245">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="172b0-246">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="172b0-246">Return Value - alignControl</span></span>

<span data-ttu-id="172b0-247">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="172b0-247">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="172b0-248">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="172b0-248">Remarks - alignControl</span></span>

<span data-ttu-id="172b0-249">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="172b0-249">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="172b0-250">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="172b0-250">Method allowEdit</span></span>

<span data-ttu-id="172b0-251">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-251">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="172b0-252">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="172b0-252">Parameters - allowEdit</span></span>

<span data-ttu-id="172b0-253">値</span><span class="sxs-lookup"><span data-stu-id="172b0-253">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="172b0-254">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="172b0-254">Return Value - allowEdit</span></span>

<span data-ttu-id="172b0-255">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="172b0-255">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="172b0-256">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="172b0-256">Remarks - allowEdit</span></span>

<span data-ttu-id="172b0-257">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="172b0-257">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-allowusersetup"></a><span data-ttu-id="172b0-258">メソッド allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="172b0-258">Method allowUserSetup</span></span>

```xpp
public int allowUserSetup([int value])
```

### <a name="parameters---allowusersetup"></a><span data-ttu-id="172b0-259">パラメーター - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="172b0-259">Parameters - allowUserSetup</span></span>

<span data-ttu-id="172b0-260">値</span><span class="sxs-lookup"><span data-stu-id="172b0-260">value</span></span>  

### <a name="return-value---allowusersetup"></a><span data-ttu-id="172b0-261">戻り値 - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="172b0-261">Return Value - allowUserSetup</span></span>

## <a name="method-arrangeguide"></a><span data-ttu-id="172b0-262">メソッド arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="172b0-262">Method arrangeGuide</span></span>

```xpp
public int arrangeGuide([int value])
```

### <a name="parameters---arrangeguide"></a><span data-ttu-id="172b0-263">パラメーター - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="172b0-263">Parameters - arrangeGuide</span></span>

<span data-ttu-id="172b0-264">値</span><span class="sxs-lookup"><span data-stu-id="172b0-264">value</span></span>  

### <a name="return-value---arrangeguide"></a><span data-ttu-id="172b0-265">戻り値 - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="172b0-265">Return Value - arrangeGuide</span></span>

## <a name="method-arrangemethod"></a><span data-ttu-id="172b0-266">メソッド arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="172b0-266">Method arrangeMethod</span></span>

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a><span data-ttu-id="172b0-267">パラメーター - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="172b0-267">Parameters - arrangeMethod</span></span>

<span data-ttu-id="172b0-268">値</span><span class="sxs-lookup"><span data-stu-id="172b0-268">value</span></span>  

### <a name="return-value---arrangemethod"></a><span data-ttu-id="172b0-269">戻り値 - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="172b0-269">Return Value - arrangeMethod</span></span>

## <a name="method-arrangewhen"></a><span data-ttu-id="172b0-270">メソッド arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="172b0-270">Method arrangeWhen</span></span>

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a><span data-ttu-id="172b0-271">パラメーター - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="172b0-271">Parameters - arrangeWhen</span></span>

<span data-ttu-id="172b0-272">値</span><span class="sxs-lookup"><span data-stu-id="172b0-272">value</span></span>  

### <a name="return-value---arrangewhen"></a><span data-ttu-id="172b0-273">戻り値 - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="172b0-273">Return Value - arrangeWhen</span></span>

## <a name="method-autodatagroup"></a><span data-ttu-id="172b0-274">メソッド autoDataGroup</span><span class="sxs-lookup"><span data-stu-id="172b0-274">Method autoDataGroup</span></span>

```xpp
public boolean autoDataGroup([boolean value])
```

### <a name="parameters---autodatagroup"></a><span data-ttu-id="172b0-275">パラメーター - autoDataGroup</span><span class="sxs-lookup"><span data-stu-id="172b0-275">Parameters - autoDataGroup</span></span>

<span data-ttu-id="172b0-276">値</span><span class="sxs-lookup"><span data-stu-id="172b0-276">value</span></span>  

### <a name="return-value---autodatagroup"></a><span data-ttu-id="172b0-277">戻り値 - autoDataGroup</span><span class="sxs-lookup"><span data-stu-id="172b0-277">Return Value - autoDataGroup</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="172b0-278">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="172b0-278">Method autoDeclaration</span></span>

<span data-ttu-id="172b0-279">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-279">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="172b0-280">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="172b0-280">Parameters - autoDeclaration</span></span>

<span data-ttu-id="172b0-281">値</span><span class="sxs-lookup"><span data-stu-id="172b0-281">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="172b0-282">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="172b0-282">Return Value - autoDeclaration</span></span>

<span data-ttu-id="172b0-283">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="172b0-283">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="172b0-284">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="172b0-284">Remarks - autoDeclaration</span></span>

<span data-ttu-id="172b0-285">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="172b0-285">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="172b0-286">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="172b0-286">Method backgroundColor</span></span>

<span data-ttu-id="172b0-287">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-287">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="172b0-288">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="172b0-288">Parameters - backgroundColor</span></span>

<span data-ttu-id="172b0-289">値</span><span class="sxs-lookup"><span data-stu-id="172b0-289">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="172b0-290">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="172b0-290">Return Value - backgroundColor</span></span>

<span data-ttu-id="172b0-291">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="172b0-291">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="172b0-292">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="172b0-292">Remarks - backgroundColor</span></span>

<span data-ttu-id="172b0-293">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="172b0-293">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="172b0-294">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="172b0-294">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="172b0-295">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="172b0-295">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="172b0-296">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="172b0-296">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="172b0-297">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="172b0-297">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="172b0-298">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="172b0-298">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="172b0-299">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="172b0-299">Method backStyle</span></span>

<span data-ttu-id="172b0-300">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-300">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="172b0-301">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="172b0-301">Parameters - backStyle</span></span>

<span data-ttu-id="172b0-302">値</span><span class="sxs-lookup"><span data-stu-id="172b0-302">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="172b0-303">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="172b0-303">Return Value - backStyle</span></span>

<span data-ttu-id="172b0-304">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="172b0-304">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="172b0-305">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="172b0-305">Method bold</span></span>

<span data-ttu-id="172b0-306">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-306">Gets or sets the weight of font that is used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="172b0-307">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="172b0-307">Parameters - bold</span></span>

<span data-ttu-id="172b0-308">値</span><span class="sxs-lookup"><span data-stu-id="172b0-308">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="172b0-309">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="172b0-309">Return Value - bold</span></span>

<span data-ttu-id="172b0-310">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="172b0-310">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="172b0-311">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="172b0-311">Remarks - bold</span></span>

<span data-ttu-id="172b0-312">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="172b0-312">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="172b0-313">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="172b0-313">0 Use the default font weight.</span></span>
-   <span data-ttu-id="172b0-314">1 シン。</span><span class="sxs-lookup"><span data-stu-id="172b0-314">1 Thin.</span></span>
-   <span data-ttu-id="172b0-315">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="172b0-315">2 Extra-light.</span></span>
-   <span data-ttu-id="172b0-316">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="172b0-316">3 Light.</span></span>
-   <span data-ttu-id="172b0-317">4 標準。</span><span class="sxs-lookup"><span data-stu-id="172b0-317">4 Normal.</span></span>
-   <span data-ttu-id="172b0-318">5 中。</span><span class="sxs-lookup"><span data-stu-id="172b0-318">5 Medium.</span></span>
-   <span data-ttu-id="172b0-319">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="172b0-319">6 Semibold.</span></span>
-   <span data-ttu-id="172b0-320">7 太字。</span><span class="sxs-lookup"><span data-stu-id="172b0-320">7 Bold.</span></span>
-   <span data-ttu-id="172b0-321">8 極太。</span><span class="sxs-lookup"><span data-stu-id="172b0-321">8 Extra-bold.</span></span>
-   <span data-ttu-id="172b0-322">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="172b0-322">9 Heavy.</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="172b0-323">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="172b0-323">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="172b0-324">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="172b0-324">Parameters - bottomMargin</span></span>

<span data-ttu-id="172b0-325">値</span><span class="sxs-lookup"><span data-stu-id="172b0-325">value</span></span>  

<!-- -->

<span data-ttu-id="172b0-326">モード</span><span class="sxs-lookup"><span data-stu-id="172b0-326">mode</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="172b0-327">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="172b0-327">Return Value - bottomMargin</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="172b0-328">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="172b0-328">Method bottomMarginMode</span></span>

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="172b0-329">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="172b0-329">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="172b0-330">モード</span><span class="sxs-lookup"><span data-stu-id="172b0-330">mode</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="172b0-331">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="172b0-331">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="172b0-332">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="172b0-332">Method bottomMarginValue</span></span>

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="172b0-333">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="172b0-333">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="172b0-334">値</span><span class="sxs-lookup"><span data-stu-id="172b0-334">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="172b0-335">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="172b0-335">Return Value - bottomMarginValue</span></span>

## <a name="method-breakable"></a><span data-ttu-id="172b0-336">メソッド breakable</span><span class="sxs-lookup"><span data-stu-id="172b0-336">Method breakable</span></span>

```xpp
public boolean breakable([boolean value])
```

### <a name="parameters---breakable"></a><span data-ttu-id="172b0-337">パラメーター - breakable</span><span class="sxs-lookup"><span data-stu-id="172b0-337">Parameters - breakable</span></span>

<span data-ttu-id="172b0-338">値</span><span class="sxs-lookup"><span data-stu-id="172b0-338">value</span></span>  

### <a name="return-value---breakable"></a><span data-ttu-id="172b0-339">戻り値 - breakable</span><span class="sxs-lookup"><span data-stu-id="172b0-339">Return Value - breakable</span></span>

## <a name="method-caption"></a><span data-ttu-id="172b0-340">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="172b0-340">Method caption</span></span>

<span data-ttu-id="172b0-341">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-341">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="172b0-342">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="172b0-342">Parameters - caption</span></span>

<span data-ttu-id="172b0-343">値</span><span class="sxs-lookup"><span data-stu-id="172b0-343">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="172b0-344">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="172b0-344">Return Value - caption</span></span>

<span data-ttu-id="172b0-345">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="172b0-345">The string that is used as the caption of the control.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="172b0-346">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="172b0-346">Method characterSet</span></span>

<span data-ttu-id="172b0-347">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-347">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="172b0-348">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="172b0-348">Parameters - characterSet</span></span>

<span data-ttu-id="172b0-349">値</span><span class="sxs-lookup"><span data-stu-id="172b0-349">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="172b0-350">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="172b0-350">Return Value - characterSet</span></span>

<span data-ttu-id="172b0-351">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="172b0-351">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="172b0-352">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="172b0-352">Remarks - characterSet</span></span>

<span data-ttu-id="172b0-353">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="172b0-353">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="172b0-354">値です。</span><span class="sxs-lookup"><span data-stu-id="172b0-354">Value.</span></span> | <span data-ttu-id="172b0-355">説明。</span><span class="sxs-lookup"><span data-stu-id="172b0-355">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="172b0-356">0</span><span class="sxs-lookup"><span data-stu-id="172b0-356">0</span></span>      | <span data-ttu-id="172b0-357">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="172b0-357">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="172b0-358">1</span><span class="sxs-lookup"><span data-stu-id="172b0-358">1</span></span>      | <span data-ttu-id="172b0-359">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="172b0-359">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="172b0-360">2</span><span class="sxs-lookup"><span data-stu-id="172b0-360">2</span></span>      | <span data-ttu-id="172b0-361">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="172b0-361">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="172b0-362">77</span><span class="sxs-lookup"><span data-stu-id="172b0-362">77</span></span>     | <span data-ttu-id="172b0-363">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="172b0-363">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="172b0-364">128</span><span class="sxs-lookup"><span data-stu-id="172b0-364">128</span></span>    | <span data-ttu-id="172b0-365">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="172b0-365">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="172b0-366">129</span><span class="sxs-lookup"><span data-stu-id="172b0-366">129</span></span>    | <span data-ttu-id="172b0-367">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="172b0-367">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="172b0-368">134</span><span class="sxs-lookup"><span data-stu-id="172b0-368">134</span></span>    | <span data-ttu-id="172b0-369">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="172b0-369">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="172b0-370">136</span><span class="sxs-lookup"><span data-stu-id="172b0-370">136</span></span>    | <span data-ttu-id="172b0-371">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="172b0-371">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="172b0-372">161</span><span class="sxs-lookup"><span data-stu-id="172b0-372">161</span></span>    | <span data-ttu-id="172b0-373">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="172b0-373">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="172b0-374">162</span><span class="sxs-lookup"><span data-stu-id="172b0-374">162</span></span>    | <span data-ttu-id="172b0-375">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="172b0-375">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="172b0-376">163</span><span class="sxs-lookup"><span data-stu-id="172b0-376">163</span></span>    | <span data-ttu-id="172b0-377">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="172b0-377">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="172b0-378">186</span><span class="sxs-lookup"><span data-stu-id="172b0-378">186</span></span>    | <span data-ttu-id="172b0-379">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="172b0-379">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="172b0-380">204</span><span class="sxs-lookup"><span data-stu-id="172b0-380">204</span></span>    | <span data-ttu-id="172b0-381">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="172b0-381">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="172b0-382">238</span><span class="sxs-lookup"><span data-stu-id="172b0-382">238</span></span>    | <span data-ttu-id="172b0-383">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="172b0-383">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="172b0-384">255</span><span class="sxs-lookup"><span data-stu-id="172b0-384">255</span></span>    | <span data-ttu-id="172b0-385">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="172b0-385">OEM\_CHARSET</span></span>         |

<span data-ttu-id="172b0-386">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="172b0-386">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="172b0-387">値です。</span><span class="sxs-lookup"><span data-stu-id="172b0-387">Value.</span></span> | <span data-ttu-id="172b0-388">説明。</span><span class="sxs-lookup"><span data-stu-id="172b0-388">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="172b0-389">130</span><span class="sxs-lookup"><span data-stu-id="172b0-389">130</span></span>    | <span data-ttu-id="172b0-390">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="172b0-390">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="172b0-391">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="172b0-391">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="172b0-392">値です。</span><span class="sxs-lookup"><span data-stu-id="172b0-392">Value.</span></span> | <span data-ttu-id="172b0-393">説明。</span><span class="sxs-lookup"><span data-stu-id="172b0-393">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="172b0-394">177</span><span class="sxs-lookup"><span data-stu-id="172b0-394">177</span></span>    | <span data-ttu-id="172b0-395">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="172b0-395">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="172b0-396">178</span><span class="sxs-lookup"><span data-stu-id="172b0-396">178</span></span>    | <span data-ttu-id="172b0-397">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="172b0-397">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="172b0-398">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="172b0-398">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="172b0-399">値です。</span><span class="sxs-lookup"><span data-stu-id="172b0-399">Value.</span></span> | <span data-ttu-id="172b0-400">説明。</span><span class="sxs-lookup"><span data-stu-id="172b0-400">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="172b0-401">222</span><span class="sxs-lookup"><span data-stu-id="172b0-401">222</span></span>    | <span data-ttu-id="172b0-402">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="172b0-402">THAI\_CHARSET</span></span> |

<span data-ttu-id="172b0-403">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="172b0-403">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="172b0-404">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="172b0-404">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="172b0-405">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="172b0-405">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="172b0-406">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="172b0-406">Method colorScheme</span></span>

<span data-ttu-id="172b0-407">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-407">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="172b0-408">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="172b0-408">Parameters - colorScheme</span></span>

<span data-ttu-id="172b0-409">値</span><span class="sxs-lookup"><span data-stu-id="172b0-409">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="172b0-410">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="172b0-410">Return Value - colorScheme</span></span>

<span data-ttu-id="172b0-411">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="172b0-411">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="172b0-412">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="172b0-412">Remarks - colorScheme</span></span>

<span data-ttu-id="172b0-413">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="172b0-413">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="172b0-414">値です。</span><span class="sxs-lookup"><span data-stu-id="172b0-414">Value.</span></span> | <span data-ttu-id="172b0-415">スタイル。</span><span class="sxs-lookup"><span data-stu-id="172b0-415">Style.</span></span>                         |
|--------|--------------------------------|
| <span data-ttu-id="172b0-416">0</span><span class="sxs-lookup"><span data-stu-id="172b0-416">0</span></span>      | <span data-ttu-id="172b0-417">既定。</span><span class="sxs-lookup"><span data-stu-id="172b0-417">Default.</span></span>                       |
| <span data-ttu-id="172b0-418">1</span><span class="sxs-lookup"><span data-stu-id="172b0-418">1</span></span>      | <span data-ttu-id="172b0-419">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="172b0-419">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="172b0-420">2</span><span class="sxs-lookup"><span data-stu-id="172b0-420">2</span></span>      | <span data-ttu-id="172b0-421">真の配色。</span><span class="sxs-lookup"><span data-stu-id="172b0-421">The true-color scheme.</span></span>         |

## <a name="method-columns"></a><span data-ttu-id="172b0-422">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="172b0-422">Method columns</span></span>

```xpp
public int columns([int value], [ColumnsMode mode])
```

### <a name="parameters---columns"></a><span data-ttu-id="172b0-423">パラメーター - columns</span><span class="sxs-lookup"><span data-stu-id="172b0-423">Parameters - columns</span></span>

<span data-ttu-id="172b0-424">値</span><span class="sxs-lookup"><span data-stu-id="172b0-424">value</span></span>  

<!-- -->

<span data-ttu-id="172b0-425">モード</span><span class="sxs-lookup"><span data-stu-id="172b0-425">mode</span></span>  

### <a name="return-value---columns"></a><span data-ttu-id="172b0-426">戻り値 - columns</span><span class="sxs-lookup"><span data-stu-id="172b0-426">Return Value - columns</span></span>

## <a name="method-columnsmode"></a><span data-ttu-id="172b0-427">メソッド columnsMode</span><span class="sxs-lookup"><span data-stu-id="172b0-427">Method columnsMode</span></span>

```xpp
public ColumnsMode columnsMode([ColumnsMode mode])
```

### <a name="parameters---columnsmode"></a><span data-ttu-id="172b0-428">パラメーター - columnsMode</span><span class="sxs-lookup"><span data-stu-id="172b0-428">Parameters - columnsMode</span></span>

<span data-ttu-id="172b0-429">モード</span><span class="sxs-lookup"><span data-stu-id="172b0-429">mode</span></span>  

### <a name="return-value---columnsmode"></a><span data-ttu-id="172b0-430">戻り値 - columnsMode</span><span class="sxs-lookup"><span data-stu-id="172b0-430">Return Value - columnsMode</span></span>

## <a name="method-columnspace"></a><span data-ttu-id="172b0-431">メソッド columnspace</span><span class="sxs-lookup"><span data-stu-id="172b0-431">Method columnspace</span></span>

```xpp
public int columnspace([int value], [AutoMode mode])
```

### <a name="parameters---columnspace"></a><span data-ttu-id="172b0-432">パラメーター - columnspace</span><span class="sxs-lookup"><span data-stu-id="172b0-432">Parameters - columnspace</span></span>

<span data-ttu-id="172b0-433">値</span><span class="sxs-lookup"><span data-stu-id="172b0-433">value</span></span>  

<!-- -->

<span data-ttu-id="172b0-434">モード</span><span class="sxs-lookup"><span data-stu-id="172b0-434">mode</span></span>  

### <a name="return-value---columnspace"></a><span data-ttu-id="172b0-435">戻り値 - columnspace</span><span class="sxs-lookup"><span data-stu-id="172b0-435">Return Value - columnspace</span></span>

## <a name="method-columnspacemode"></a><span data-ttu-id="172b0-436">メソッド columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="172b0-436">Method columnspaceMode</span></span>

```xpp
public AutoMode columnspaceMode([AutoMode mode])
```

### <a name="parameters---columnspacemode"></a><span data-ttu-id="172b0-437">パラメーター - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="172b0-437">Parameters - columnspaceMode</span></span>

<span data-ttu-id="172b0-438">モード</span><span class="sxs-lookup"><span data-stu-id="172b0-438">mode</span></span>  

### <a name="return-value---columnspacemode"></a><span data-ttu-id="172b0-439">戻り値 - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="172b0-439">Return Value - columnspaceMode</span></span>

## <a name="method-columnspacevalue"></a><span data-ttu-id="172b0-440">メソッド columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="172b0-440">Method columnspaceValue</span></span>

```xpp
public int columnspaceValue([int value])
```

### <a name="parameters---columnspacevalue"></a><span data-ttu-id="172b0-441">パラメーター - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="172b0-441">Parameters - columnspaceValue</span></span>

<span data-ttu-id="172b0-442">値</span><span class="sxs-lookup"><span data-stu-id="172b0-442">value</span></span>  

### <a name="return-value---columnspacevalue"></a><span data-ttu-id="172b0-443">戻り値 - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="172b0-443">Return Value - columnspaceValue</span></span>

## <a name="method-columnsvalue"></a><span data-ttu-id="172b0-444">メソッド columnsValue</span><span class="sxs-lookup"><span data-stu-id="172b0-444">Method columnsValue</span></span>

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a><span data-ttu-id="172b0-445">パラメーター - columnsValue</span><span class="sxs-lookup"><span data-stu-id="172b0-445">Parameters - columnsValue</span></span>

<span data-ttu-id="172b0-446">値</span><span class="sxs-lookup"><span data-stu-id="172b0-446">value</span></span>  

### <a name="return-value---columnsvalue"></a><span data-ttu-id="172b0-447">戻り値 - columnsValue</span><span class="sxs-lookup"><span data-stu-id="172b0-447">Return Value - columnsValue</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="172b0-448">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="172b0-448">Method configurationKey</span></span>

<span data-ttu-id="172b0-449">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-449">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="172b0-450">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="172b0-450">Parameters - configurationKey</span></span>

<span data-ttu-id="172b0-451">値</span><span class="sxs-lookup"><span data-stu-id="172b0-451">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="172b0-452">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="172b0-452">Return Value - configurationKey</span></span>

<span data-ttu-id="172b0-453">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="172b0-453">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="172b0-454">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="172b0-454">Remarks - configurationKey</span></span>

<span data-ttu-id="172b0-455">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="172b0-455">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="172b0-456">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="172b0-456">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="172b0-457">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="172b0-457">Method containerId</span></span>

<span data-ttu-id="172b0-458">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="172b0-458">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="172b0-459">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="172b0-459">Return Value - containerId</span></span>

<span data-ttu-id="172b0-460">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="172b0-460">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="172b0-461">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="172b0-461">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="172b0-462">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="172b0-462">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="172b0-463">値</span><span class="sxs-lookup"><span data-stu-id="172b0-463">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="172b0-464">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="172b0-464">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="172b0-465">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="172b0-465">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="172b0-466">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="172b0-466">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="172b0-467">値</span><span class="sxs-lookup"><span data-stu-id="172b0-467">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="172b0-468">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="172b0-468">Return Value - countryRegionContextField</span></span>

## <a name="method-datagroup"></a><span data-ttu-id="172b0-469">メソッド dataGroup</span><span class="sxs-lookup"><span data-stu-id="172b0-469">Method dataGroup</span></span>

```xpp
public str dataGroup([str value])
```

### <a name="parameters---datagroup"></a><span data-ttu-id="172b0-470">パラメーター - dataGroup</span><span class="sxs-lookup"><span data-stu-id="172b0-470">Parameters - dataGroup</span></span>

<span data-ttu-id="172b0-471">値</span><span class="sxs-lookup"><span data-stu-id="172b0-471">value</span></span>  

### <a name="return-value---datagroup"></a><span data-ttu-id="172b0-472">戻り値 - dataGroup</span><span class="sxs-lookup"><span data-stu-id="172b0-472">Return Value - dataGroup</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="172b0-473">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="172b0-473">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="172b0-474">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="172b0-474">Parameters - dataRelationPath</span></span>

<span data-ttu-id="172b0-475">値</span><span class="sxs-lookup"><span data-stu-id="172b0-475">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="172b0-476">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="172b0-476">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="172b0-477">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="172b0-477">Method dataSource</span></span>

<span data-ttu-id="172b0-478">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-478">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="172b0-479">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="172b0-479">Parameters - dataSource</span></span>

<span data-ttu-id="172b0-480">値</span><span class="sxs-lookup"><span data-stu-id="172b0-480">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="172b0-481">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="172b0-481">Return Value - dataSource</span></span>

<span data-ttu-id="172b0-482">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="172b0-482">The identifier of the data source that will be used.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="172b0-483">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="172b0-483">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="172b0-484">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="172b0-484">Parameters - displayTarget</span></span>

<span data-ttu-id="172b0-485">値</span><span class="sxs-lookup"><span data-stu-id="172b0-485">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="172b0-486">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="172b0-486">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="172b0-487">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="172b0-487">Method dragDrop</span></span>

<span data-ttu-id="172b0-488">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-488">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="172b0-489">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="172b0-489">Parameters - dragDrop</span></span>

<span data-ttu-id="172b0-490">値</span><span class="sxs-lookup"><span data-stu-id="172b0-490">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="172b0-491">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="172b0-491">Return Value - dragDrop</span></span>

<span data-ttu-id="172b0-492">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="172b0-492">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="172b0-493">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="172b0-493">Method enabled</span></span>

<span data-ttu-id="172b0-494">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-494">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="172b0-495">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="172b0-495">Parameters - enabled</span></span>

<span data-ttu-id="172b0-496">値</span><span class="sxs-lookup"><span data-stu-id="172b0-496">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="172b0-497">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="172b0-497">Return Value - enabled</span></span>

<span data-ttu-id="172b0-498">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="172b0-498">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="172b0-499">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="172b0-499">Remarks - enabled</span></span>

<span data-ttu-id="172b0-500">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="172b0-500">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="172b0-501">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="172b0-501">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="172b0-502">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="172b0-502">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-font"></a><span data-ttu-id="172b0-503">メソッド font</span><span class="sxs-lookup"><span data-stu-id="172b0-503">Method font</span></span>

<span data-ttu-id="172b0-504">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-504">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="172b0-505">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="172b0-505">Parameters - font</span></span>

<span data-ttu-id="172b0-506">値</span><span class="sxs-lookup"><span data-stu-id="172b0-506">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="172b0-507">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="172b0-507">Return Value - font</span></span>

<span data-ttu-id="172b0-508">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="172b0-508">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="172b0-509">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="172b0-509">Method fontSize</span></span>

<span data-ttu-id="172b0-510">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-510">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="172b0-511">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="172b0-511">Parameters - fontSize</span></span>

<span data-ttu-id="172b0-512">値</span><span class="sxs-lookup"><span data-stu-id="172b0-512">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="172b0-513">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="172b0-513">Return Value - fontSize</span></span>

<span data-ttu-id="172b0-514">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="172b0-514">The height of the font in points.</span></span>

## <a name="method-frameoptionbutton"></a><span data-ttu-id="172b0-515">メソッド frameOptionButton</span><span class="sxs-lookup"><span data-stu-id="172b0-515">Method frameOptionButton</span></span>

```xpp
public int frameOptionButton([int value])
```

### <a name="parameters---frameoptionbutton"></a><span data-ttu-id="172b0-516">パラメーター - frameOptionButton</span><span class="sxs-lookup"><span data-stu-id="172b0-516">Parameters - frameOptionButton</span></span>

<span data-ttu-id="172b0-517">値</span><span class="sxs-lookup"><span data-stu-id="172b0-517">value</span></span>  

### <a name="return-value---frameoptionbutton"></a><span data-ttu-id="172b0-518">戻り値 - frameOptionButton</span><span class="sxs-lookup"><span data-stu-id="172b0-518">Return Value - frameOptionButton</span></span>

## <a name="method-frameposition"></a><span data-ttu-id="172b0-519">メソッド framePosition</span><span class="sxs-lookup"><span data-stu-id="172b0-519">Method framePosition</span></span>

```xpp
public int framePosition([int value])
```

### <a name="parameters---frameposition"></a><span data-ttu-id="172b0-520">パラメーター - framePosition</span><span class="sxs-lookup"><span data-stu-id="172b0-520">Parameters - framePosition</span></span>

<span data-ttu-id="172b0-521">値</span><span class="sxs-lookup"><span data-stu-id="172b0-521">value</span></span>  

### <a name="return-value---frameposition"></a><span data-ttu-id="172b0-522">戻り値 - framePosition</span><span class="sxs-lookup"><span data-stu-id="172b0-522">Return Value - framePosition</span></span>

## <a name="method-frametype"></a><span data-ttu-id="172b0-523">メソッド frameType</span><span class="sxs-lookup"><span data-stu-id="172b0-523">Method frameType</span></span>

```xpp
public int frameType([int value])
```

### <a name="parameters---frametype"></a><span data-ttu-id="172b0-524">パラメーター - frameType</span><span class="sxs-lookup"><span data-stu-id="172b0-524">Parameters - frameType</span></span>

<span data-ttu-id="172b0-525">値</span><span class="sxs-lookup"><span data-stu-id="172b0-525">value</span></span>  

### <a name="return-value---frametype"></a><span data-ttu-id="172b0-526">戻り値 - frameType</span><span class="sxs-lookup"><span data-stu-id="172b0-526">Return Value - frameType</span></span>

## <a name="method-height"></a><span data-ttu-id="172b0-527">メソッド height</span><span class="sxs-lookup"><span data-stu-id="172b0-527">Method height</span></span>

<span data-ttu-id="172b0-528">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-528">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="172b0-529">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="172b0-529">Parameters - height</span></span>

<span data-ttu-id="172b0-530">値</span><span class="sxs-lookup"><span data-stu-id="172b0-530">value</span></span>  

<!-- -->

<span data-ttu-id="172b0-531">モード</span><span class="sxs-lookup"><span data-stu-id="172b0-531">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="172b0-532">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="172b0-532">Return Value - height</span></span>

<span data-ttu-id="172b0-533">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="172b0-533">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="172b0-534">備考 - height</span><span class="sxs-lookup"><span data-stu-id="172b0-534">Remarks - height</span></span>

<span data-ttu-id="172b0-535">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="172b0-535">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="172b0-536">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="172b0-536">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="172b0-537">モード。</span><span class="sxs-lookup"><span data-stu-id="172b0-537">Mode.</span></span>            | <span data-ttu-id="172b0-538">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="172b0-538">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="172b0-539">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="172b0-539">-1 Exact.</span></span>        | <span data-ttu-id="172b0-540">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="172b0-540">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="172b0-541">0 自動。</span><span class="sxs-lookup"><span data-stu-id="172b0-541">0 Auto.</span></span>          | <span data-ttu-id="172b0-542">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="172b0-542">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="172b0-543">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="172b0-543">1 Column height.</span></span> | <span data-ttu-id="172b0-544">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="172b0-544">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="172b0-545">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="172b0-545">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="172b0-546">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="172b0-546">Method heightMode</span></span>

<span data-ttu-id="172b0-547">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-547">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="172b0-548">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="172b0-548">Parameters - heightMode</span></span>

<span data-ttu-id="172b0-549">値</span><span class="sxs-lookup"><span data-stu-id="172b0-549">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="172b0-550">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="172b0-550">Return Value - heightMode</span></span>

<span data-ttu-id="172b0-551">計算モード。</span><span class="sxs-lookup"><span data-stu-id="172b0-551">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="172b0-552">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="172b0-552">Remarks - heightMode</span></span>

<span data-ttu-id="172b0-553">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="172b0-553">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="172b0-554">モード。</span><span class="sxs-lookup"><span data-stu-id="172b0-554">Mode.</span></span>          | <span data-ttu-id="172b0-555">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="172b0-555">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="172b0-556">正確。</span><span class="sxs-lookup"><span data-stu-id="172b0-556">Exact.</span></span>         | <span data-ttu-id="172b0-557">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="172b0-557">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="172b0-558">自動。</span><span class="sxs-lookup"><span data-stu-id="172b0-558">Auto.</span></span>          | <span data-ttu-id="172b0-559">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="172b0-559">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="172b0-560">列の高さ</span><span class="sxs-lookup"><span data-stu-id="172b0-560">Column height.</span></span> | <span data-ttu-id="172b0-561">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="172b0-561">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="172b0-562">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="172b0-562">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="172b0-563">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="172b0-563">Method heightValue</span></span>

<span data-ttu-id="172b0-564">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-564">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="172b0-565">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="172b0-565">Parameters - heightValue</span></span>

<span data-ttu-id="172b0-566">値</span><span class="sxs-lookup"><span data-stu-id="172b0-566">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="172b0-567">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="172b0-567">Return Value - heightValue</span></span>

<span data-ttu-id="172b0-568">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="172b0-568">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="172b0-569">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="172b0-569">Remarks - heightValue</span></span>

<span data-ttu-id="172b0-570">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="172b0-570">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="172b0-571">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="172b0-571">Method helpText</span></span>

<span data-ttu-id="172b0-572">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-572">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="172b0-573">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="172b0-573">Parameters - helpText</span></span>

<span data-ttu-id="172b0-574">値</span><span class="sxs-lookup"><span data-stu-id="172b0-574">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="172b0-575">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="172b0-575">Return Value - helpText</span></span>

<span data-ttu-id="172b0-576">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="172b0-576">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="172b0-577">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="172b0-577">Remarks - helpText</span></span>

<span data-ttu-id="172b0-578">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-578">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="172b0-579">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="172b0-579">The help text must not exceed 250 characters.</span></span>

## <a name="method-hideifempty"></a><span data-ttu-id="172b0-580">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="172b0-580">Method hideIfEmpty</span></span>

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a><span data-ttu-id="172b0-581">パラメーター - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="172b0-581">Parameters - hideIfEmpty</span></span>

<span data-ttu-id="172b0-582">値</span><span class="sxs-lookup"><span data-stu-id="172b0-582">value</span></span>  

### <a name="return-value---hideifempty"></a><span data-ttu-id="172b0-583">戻り値 - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="172b0-583">Return Value - hideIfEmpty</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="172b0-584">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="172b0-584">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="172b0-585">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="172b0-585">Parameters - hierarchyParent</span></span>

<span data-ttu-id="172b0-586">値</span><span class="sxs-lookup"><span data-stu-id="172b0-586">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="172b0-587">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="172b0-587">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="172b0-588">メソッド id</span><span class="sxs-lookup"><span data-stu-id="172b0-588">Method id</span></span>

<span data-ttu-id="172b0-589">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="172b0-589">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="172b0-590">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="172b0-590">Return Value - id</span></span>

<span data-ttu-id="172b0-591">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="172b0-591">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="172b0-592">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="172b0-592">Method isContainer</span></span>

<span data-ttu-id="172b0-593">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="172b0-593">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="172b0-594">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="172b0-594">Return Value - isContainer</span></span>

<span data-ttu-id="172b0-595">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="172b0-595">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-italic"></a><span data-ttu-id="172b0-596">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="172b0-596">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="172b0-597">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="172b0-597">Parameters - italic</span></span>

<span data-ttu-id="172b0-598">値</span><span class="sxs-lookup"><span data-stu-id="172b0-598">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="172b0-599">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="172b0-599">Return Value - italic</span></span>

## <a name="method-labelbold"></a><span data-ttu-id="172b0-600">メソッド labelBold</span><span class="sxs-lookup"><span data-stu-id="172b0-600">Method labelBold</span></span>

```xpp
public int labelBold([int value])
```

### <a name="parameters---labelbold"></a><span data-ttu-id="172b0-601">パラメーター - labelBold</span><span class="sxs-lookup"><span data-stu-id="172b0-601">Parameters - labelBold</span></span>

<span data-ttu-id="172b0-602">値</span><span class="sxs-lookup"><span data-stu-id="172b0-602">value</span></span>  

### <a name="return-value---labelbold"></a><span data-ttu-id="172b0-603">戻り値 - labelBold</span><span class="sxs-lookup"><span data-stu-id="172b0-603">Return Value - labelBold</span></span>

## <a name="method-labelcharacterset"></a><span data-ttu-id="172b0-604">メソッド labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="172b0-604">Method labelCharacterSet</span></span>

```xpp
public int labelCharacterSet([int value])
```

### <a name="parameters---labelcharacterset"></a><span data-ttu-id="172b0-605">パラメーター - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="172b0-605">Parameters - labelCharacterSet</span></span>

<span data-ttu-id="172b0-606">値</span><span class="sxs-lookup"><span data-stu-id="172b0-606">value</span></span>  

### <a name="return-value---labelcharacterset"></a><span data-ttu-id="172b0-607">戻り値 - labelCharacterSet</span><span class="sxs-lookup"><span data-stu-id="172b0-607">Return Value - labelCharacterSet</span></span>

## <a name="method-labelfont"></a><span data-ttu-id="172b0-608">メソッド labelFont</span><span class="sxs-lookup"><span data-stu-id="172b0-608">Method labelFont</span></span>

```xpp
public str labelFont([str value])
```

### <a name="parameters---labelfont"></a><span data-ttu-id="172b0-609">パラメーター - labelFont</span><span class="sxs-lookup"><span data-stu-id="172b0-609">Parameters - labelFont</span></span>

<span data-ttu-id="172b0-610">値</span><span class="sxs-lookup"><span data-stu-id="172b0-610">value</span></span>  

### <a name="return-value---labelfont"></a><span data-ttu-id="172b0-611">戻り値 - labelFont</span><span class="sxs-lookup"><span data-stu-id="172b0-611">Return Value - labelFont</span></span>

## <a name="method-labelfontsize"></a><span data-ttu-id="172b0-612">メソッド labelFontSize</span><span class="sxs-lookup"><span data-stu-id="172b0-612">Method labelFontSize</span></span>

```xpp
public int labelFontSize([int value])
```

### <a name="parameters---labelfontsize"></a><span data-ttu-id="172b0-613">パラメーター - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="172b0-613">Parameters - labelFontSize</span></span>

<span data-ttu-id="172b0-614">値</span><span class="sxs-lookup"><span data-stu-id="172b0-614">value</span></span>  

### <a name="return-value---labelfontsize"></a><span data-ttu-id="172b0-615">戻り値 - labelFontSize</span><span class="sxs-lookup"><span data-stu-id="172b0-615">Return Value - labelFontSize</span></span>

## <a name="method-labelitalic"></a><span data-ttu-id="172b0-616">メソッド labelItalic</span><span class="sxs-lookup"><span data-stu-id="172b0-616">Method labelItalic</span></span>

```xpp
public boolean labelItalic([boolean value])
```

### <a name="parameters---labelitalic"></a><span data-ttu-id="172b0-617">パラメーター - labelItalic</span><span class="sxs-lookup"><span data-stu-id="172b0-617">Parameters - labelItalic</span></span>

<span data-ttu-id="172b0-618">値</span><span class="sxs-lookup"><span data-stu-id="172b0-618">value</span></span>  

### <a name="return-value---labelitalic"></a><span data-ttu-id="172b0-619">戻り値 - labelItalic</span><span class="sxs-lookup"><span data-stu-id="172b0-619">Return Value - labelItalic</span></span>

## <a name="method-labelunderline"></a><span data-ttu-id="172b0-620">メソッド labelUnderline</span><span class="sxs-lookup"><span data-stu-id="172b0-620">Method labelUnderline</span></span>

```xpp
public boolean labelUnderline([boolean value])
```

### <a name="parameters---labelunderline"></a><span data-ttu-id="172b0-621">パラメーター - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="172b0-621">Parameters - labelUnderline</span></span>

<span data-ttu-id="172b0-622">値</span><span class="sxs-lookup"><span data-stu-id="172b0-622">value</span></span>  

### <a name="return-value---labelunderline"></a><span data-ttu-id="172b0-623">戻り値 - labelUnderline</span><span class="sxs-lookup"><span data-stu-id="172b0-623">Return Value - labelUnderline</span></span>

## <a name="method-left"></a><span data-ttu-id="172b0-624">メソッド left</span><span class="sxs-lookup"><span data-stu-id="172b0-624">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="172b0-625">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="172b0-625">Parameters - left</span></span>

<span data-ttu-id="172b0-626">値</span><span class="sxs-lookup"><span data-stu-id="172b0-626">value</span></span>  

<!-- -->

<span data-ttu-id="172b0-627">モード</span><span class="sxs-lookup"><span data-stu-id="172b0-627">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="172b0-628">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="172b0-628">Return Value - left</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="172b0-629">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="172b0-629">Method leftMargin</span></span>

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="172b0-630">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="172b0-630">Parameters - leftMargin</span></span>

<span data-ttu-id="172b0-631">値</span><span class="sxs-lookup"><span data-stu-id="172b0-631">value</span></span>  

<!-- -->

<span data-ttu-id="172b0-632">モード</span><span class="sxs-lookup"><span data-stu-id="172b0-632">mode</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="172b0-633">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="172b0-633">Return Value - leftMargin</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="172b0-634">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="172b0-634">Method leftMarginMode</span></span>

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="172b0-635">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="172b0-635">Parameters - leftMarginMode</span></span>

<span data-ttu-id="172b0-636">モード</span><span class="sxs-lookup"><span data-stu-id="172b0-636">mode</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="172b0-637">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="172b0-637">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="172b0-638">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="172b0-638">Method leftMarginValue</span></span>

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="172b0-639">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="172b0-639">Parameters - leftMarginValue</span></span>

<span data-ttu-id="172b0-640">値</span><span class="sxs-lookup"><span data-stu-id="172b0-640">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="172b0-641">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="172b0-641">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="172b0-642">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="172b0-642">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="172b0-643">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="172b0-643">Parameters - leftMode</span></span>

<span data-ttu-id="172b0-644">値</span><span class="sxs-lookup"><span data-stu-id="172b0-644">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="172b0-645">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="172b0-645">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="172b0-646">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="172b0-646">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="172b0-647">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="172b0-647">Parameters - leftValue</span></span>

<span data-ttu-id="172b0-648">値</span><span class="sxs-lookup"><span data-stu-id="172b0-648">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="172b0-649">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="172b0-649">Return Value - leftValue</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="172b0-650">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="172b0-650">Method moveControl</span></span>

<span data-ttu-id="172b0-651">コントロールに指定されたコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="172b0-651">Moves a specified control to the control.</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterControlId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="172b0-652">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="172b0-652">Parameters - moveControl</span></span>

<span data-ttu-id="172b0-653">controlId</span><span class="sxs-lookup"><span data-stu-id="172b0-653">controlId</span></span>  

<!-- -->

<span data-ttu-id="172b0-654">insertAfterControlId</span><span class="sxs-lookup"><span data-stu-id="172b0-654">insertAfterControlId</span></span>  

### <a name="return-value---movecontrol"></a><span data-ttu-id="172b0-655">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="172b0-655">Return Value - moveControl</span></span>

<span data-ttu-id="172b0-656">コントロールが正常に移動した場合は 1、それ以外の場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="172b0-656">1 if the control was moved successfully; otherwise, 0.</span></span>

### <a name="remarks---movecontrol"></a><span data-ttu-id="172b0-657">備考 - moveControl</span><span class="sxs-lookup"><span data-stu-id="172b0-657">Remarks - moveControl</span></span>

<span data-ttu-id="172b0-658">一般に、指定したコントロールをコントロールに含めることができ、現在のコンテナーから移動できる場合、このメソッドは成功します。</span><span class="sxs-lookup"><span data-stu-id="172b0-658">In general, if the specified control can be contained in the control and can be moved from the container that it is currently in, this method should succeed.</span></span> <span data-ttu-id="172b0-659">ただし、場合によっては、参照グループ コントロールのインスタンス コントロールなど、コントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="172b0-659">However, in some cases, such as for the reference group control instance, controls cannot be moved.</span></span>

## <a name="method-name"></a><span data-ttu-id="172b0-660">メソッド名</span><span class="sxs-lookup"><span data-stu-id="172b0-660">Method name</span></span>

<span data-ttu-id="172b0-661">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-661">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="172b0-662">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="172b0-662">Parameters - name</span></span>

<span data-ttu-id="172b0-663">値</span><span class="sxs-lookup"><span data-stu-id="172b0-663">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="172b0-664">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="172b0-664">Return Value - name</span></span>

<span data-ttu-id="172b0-665">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="172b0-665">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="172b0-666">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="172b0-666">Remarks - name</span></span>

<span data-ttu-id="172b0-667">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="172b0-667">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="172b0-668">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="172b0-668">It must start with a letter.</span></span>
-   <span data-ttu-id="172b0-669">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="172b0-669">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="172b0-670">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="172b0-670">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="172b0-671">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="172b0-671">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="172b0-672">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="172b0-672">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="172b0-673">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="172b0-673">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="172b0-674">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="172b0-674">Parameters - neededPermission</span></span>

<span data-ttu-id="172b0-675">値</span><span class="sxs-lookup"><span data-stu-id="172b0-675">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="172b0-676">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="172b0-676">Return Value - neededPermission</span></span>

## <a name="method-optionvalue"></a><span data-ttu-id="172b0-677">メソッド optionValue</span><span class="sxs-lookup"><span data-stu-id="172b0-677">Method optionValue</span></span>

```xpp
public int optionValue([int value])
```

### <a name="parameters---optionvalue"></a><span data-ttu-id="172b0-678">パラメーター - optionValue</span><span class="sxs-lookup"><span data-stu-id="172b0-678">Parameters - optionValue</span></span>

<span data-ttu-id="172b0-679">値</span><span class="sxs-lookup"><span data-stu-id="172b0-679">value</span></span>  

### <a name="return-value---optionvalue"></a><span data-ttu-id="172b0-680">戻り値 - optionValue</span><span class="sxs-lookup"><span data-stu-id="172b0-680">Return Value - optionValue</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="172b0-681">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="172b0-681">Method rightMargin</span></span>

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="172b0-682">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="172b0-682">Parameters - rightMargin</span></span>

<span data-ttu-id="172b0-683">値</span><span class="sxs-lookup"><span data-stu-id="172b0-683">value</span></span>  

<!-- -->

<span data-ttu-id="172b0-684">モード</span><span class="sxs-lookup"><span data-stu-id="172b0-684">mode</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="172b0-685">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="172b0-685">Return Value - rightMargin</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="172b0-686">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="172b0-686">Method rightMarginMode</span></span>

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="172b0-687">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="172b0-687">Parameters - rightMarginMode</span></span>

<span data-ttu-id="172b0-688">モード</span><span class="sxs-lookup"><span data-stu-id="172b0-688">mode</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="172b0-689">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="172b0-689">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="172b0-690">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="172b0-690">Method rightMarginValue</span></span>

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="172b0-691">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="172b0-691">Parameters - rightMarginValue</span></span>

<span data-ttu-id="172b0-692">値</span><span class="sxs-lookup"><span data-stu-id="172b0-692">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="172b0-693">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="172b0-693">Return Value - rightMarginValue</span></span>

## <a name="method-savefilter"></a><span data-ttu-id="172b0-694">メソッド saveFilter</span><span class="sxs-lookup"><span data-stu-id="172b0-694">Method saveFilter</span></span>

```xpp
public boolean saveFilter([boolean value])
```

### <a name="parameters---savefilter"></a><span data-ttu-id="172b0-695">パラメーター - saveFilter</span><span class="sxs-lookup"><span data-stu-id="172b0-695">Parameters - saveFilter</span></span>

<span data-ttu-id="172b0-696">値</span><span class="sxs-lookup"><span data-stu-id="172b0-696">value</span></span>  

### <a name="return-value---savefilter"></a><span data-ttu-id="172b0-697">戻り値 - saveFilter</span><span class="sxs-lookup"><span data-stu-id="172b0-697">Return Value - saveFilter</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="172b0-698">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="172b0-698">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="172b0-699">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="172b0-699">Parameters - securityKey</span></span>

<span data-ttu-id="172b0-700">値</span><span class="sxs-lookup"><span data-stu-id="172b0-700">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="172b0-701">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="172b0-701">Return Value - securityKey</span></span>

## <a name="method-skip"></a><span data-ttu-id="172b0-702">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="172b0-702">Method skip</span></span>

<span data-ttu-id="172b0-703">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="172b0-703">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="172b0-704">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="172b0-704">Parameters - skip</span></span>

<span data-ttu-id="172b0-705">値</span><span class="sxs-lookup"><span data-stu-id="172b0-705">value</span></span>  
<span data-ttu-id="172b0-706">コントロールの skip プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="172b0-706">The value to assign to the skip property of the control.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="172b0-707">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="172b0-707">Return Value - skip</span></span>

<span data-ttu-id="172b0-708">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="172b0-708">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-style"></a><span data-ttu-id="172b0-709">メソッド style</span><span class="sxs-lookup"><span data-stu-id="172b0-709">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="172b0-710">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="172b0-710">Parameters - style</span></span>

<span data-ttu-id="172b0-711">値</span><span class="sxs-lookup"><span data-stu-id="172b0-711">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="172b0-712">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="172b0-712">Return Value - style</span></span>

## <a name="method-top"></a><span data-ttu-id="172b0-713">メソッド top</span><span class="sxs-lookup"><span data-stu-id="172b0-713">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="172b0-714">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="172b0-714">Parameters - top</span></span>

<span data-ttu-id="172b0-715">値</span><span class="sxs-lookup"><span data-stu-id="172b0-715">value</span></span>  

<!-- -->

<span data-ttu-id="172b0-716">モード</span><span class="sxs-lookup"><span data-stu-id="172b0-716">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="172b0-717">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="172b0-717">Return Value - top</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="172b0-718">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="172b0-718">Method topMargin</span></span>

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="172b0-719">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="172b0-719">Parameters - topMargin</span></span>

<span data-ttu-id="172b0-720">値</span><span class="sxs-lookup"><span data-stu-id="172b0-720">value</span></span>  

<!-- -->

<span data-ttu-id="172b0-721">モード</span><span class="sxs-lookup"><span data-stu-id="172b0-721">mode</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="172b0-722">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="172b0-722">Return Value - topMargin</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="172b0-723">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="172b0-723">Method topMarginMode</span></span>

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="172b0-724">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="172b0-724">Parameters - topMarginMode</span></span>

<span data-ttu-id="172b0-725">モード</span><span class="sxs-lookup"><span data-stu-id="172b0-725">mode</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="172b0-726">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="172b0-726">Return Value - topMarginMode</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="172b0-727">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="172b0-727">Method topMarginValue</span></span>

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="172b0-728">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="172b0-728">Parameters - topMarginValue</span></span>

<span data-ttu-id="172b0-729">値</span><span class="sxs-lookup"><span data-stu-id="172b0-729">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="172b0-730">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="172b0-730">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="172b0-731">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="172b0-731">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="172b0-732">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="172b0-732">Parameters - topMode</span></span>

<span data-ttu-id="172b0-733">値</span><span class="sxs-lookup"><span data-stu-id="172b0-733">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="172b0-734">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="172b0-734">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="172b0-735">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="172b0-735">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="172b0-736">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="172b0-736">Parameters - topValue</span></span>

<span data-ttu-id="172b0-737">値</span><span class="sxs-lookup"><span data-stu-id="172b0-737">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="172b0-738">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="172b0-738">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="172b0-739">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="172b0-739">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="172b0-740">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="172b0-740">Parameters - type</span></span>

<span data-ttu-id="172b0-741">値</span><span class="sxs-lookup"><span data-stu-id="172b0-741">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="172b0-742">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="172b0-742">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="172b0-743">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="172b0-743">Method underline</span></span>

<span data-ttu-id="172b0-744">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="172b0-744">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="172b0-745">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="172b0-745">Parameters - underline</span></span>

<span data-ttu-id="172b0-746">値</span><span class="sxs-lookup"><span data-stu-id="172b0-746">value</span></span>  
<span data-ttu-id="172b0-747">コントロールの underline プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="172b0-747">The value to assign to the underline property of the control.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="172b0-748">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="172b0-748">Return Value - underline</span></span>

<span data-ttu-id="172b0-749">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="172b0-749">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-userdata"></a><span data-ttu-id="172b0-750">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="172b0-750">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="172b0-751">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="172b0-751">Parameters - userData</span></span>

<span data-ttu-id="172b0-752">値</span><span class="sxs-lookup"><span data-stu-id="172b0-752">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="172b0-753">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="172b0-753">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="172b0-754">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="172b0-754">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="172b0-755">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="172b0-755">Parameters - userDataItem</span></span>

<span data-ttu-id="172b0-756">値</span><span class="sxs-lookup"><span data-stu-id="172b0-756">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="172b0-757">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="172b0-757">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="172b0-758">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="172b0-758">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="172b0-759">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="172b0-759">Parameters - userDataItems</span></span>

<span data-ttu-id="172b0-760">値</span><span class="sxs-lookup"><span data-stu-id="172b0-760">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="172b0-761">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="172b0-761">Return Value - userDataItems</span></span>

## <a name="method-useuserlayout"></a><span data-ttu-id="172b0-762">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="172b0-762">Method useUserLayout</span></span>

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a><span data-ttu-id="172b0-763">パラメーター - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="172b0-763">Parameters - useUserLayout</span></span>

<span data-ttu-id="172b0-764">値</span><span class="sxs-lookup"><span data-stu-id="172b0-764">value</span></span>  

### <a name="return-value---useuserlayout"></a><span data-ttu-id="172b0-765">戻り値 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="172b0-765">Return Value - useUserLayout</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="172b0-766">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="172b0-766">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="172b0-767">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="172b0-767">Parameters - verticalSpacing</span></span>

<span data-ttu-id="172b0-768">値</span><span class="sxs-lookup"><span data-stu-id="172b0-768">value</span></span>  

<!-- -->

<span data-ttu-id="172b0-769">モード</span><span class="sxs-lookup"><span data-stu-id="172b0-769">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="172b0-770">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="172b0-770">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="172b0-771">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="172b0-771">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="172b0-772">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="172b0-772">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="172b0-773">モード</span><span class="sxs-lookup"><span data-stu-id="172b0-773">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="172b0-774">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="172b0-774">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="172b0-775">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="172b0-775">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="172b0-776">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="172b0-776">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="172b0-777">値</span><span class="sxs-lookup"><span data-stu-id="172b0-777">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="172b0-778">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="172b0-778">Return Value - verticalSpacingValue</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="172b0-779">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="172b0-779">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="172b0-780">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="172b0-780">Parameters - viewEditMode</span></span>

<span data-ttu-id="172b0-781">値</span><span class="sxs-lookup"><span data-stu-id="172b0-781">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="172b0-782">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="172b0-782">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="172b0-783">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="172b0-783">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="172b0-784">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="172b0-784">Parameters - visible</span></span>

<span data-ttu-id="172b0-785">値</span><span class="sxs-lookup"><span data-stu-id="172b0-785">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="172b0-786">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="172b0-786">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="172b0-787">メソッド width</span><span class="sxs-lookup"><span data-stu-id="172b0-787">Method width</span></span>

<span data-ttu-id="172b0-788">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-788">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="172b0-789">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="172b0-789">Parameters - width</span></span>

<span data-ttu-id="172b0-790">値</span><span class="sxs-lookup"><span data-stu-id="172b0-790">value</span></span>  

<!-- -->

<span data-ttu-id="172b0-791">モード</span><span class="sxs-lookup"><span data-stu-id="172b0-791">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="172b0-792">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="172b0-792">Return Value - width</span></span>

<span data-ttu-id="172b0-793">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="172b0-793">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="172b0-794">備考 - width</span><span class="sxs-lookup"><span data-stu-id="172b0-794">Remarks - width</span></span>

<span data-ttu-id="172b0-795">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="172b0-795">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="172b0-796">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="172b0-796">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="172b0-797">モード。</span><span class="sxs-lookup"><span data-stu-id="172b0-797">Mode.</span></span>           | <span data-ttu-id="172b0-798">幅計算。</span><span class="sxs-lookup"><span data-stu-id="172b0-798">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="172b0-799">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="172b0-799">-1 Exact.</span></span>       | <span data-ttu-id="172b0-800">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="172b0-800">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="172b0-801">0 自動。</span><span class="sxs-lookup"><span data-stu-id="172b0-801">0 Auto.</span></span>         | <span data-ttu-id="172b0-802">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="172b0-802">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="172b0-803">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="172b0-803">1 Column width.</span></span> | <span data-ttu-id="172b0-804">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="172b0-804">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="172b0-805">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="172b0-805">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="172b0-806">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="172b0-806">Method widthMode</span></span>

<span data-ttu-id="172b0-807">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-807">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="172b0-808">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="172b0-808">Parameters - widthMode</span></span>

<span data-ttu-id="172b0-809">値</span><span class="sxs-lookup"><span data-stu-id="172b0-809">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="172b0-810">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="172b0-810">Return Value - widthMode</span></span>

<span data-ttu-id="172b0-811">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="172b0-811">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="172b0-812">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="172b0-812">Remarks - widthMode</span></span>

<span data-ttu-id="172b0-813">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="172b0-813">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="172b0-814">モード。</span><span class="sxs-lookup"><span data-stu-id="172b0-814">Mode.</span></span>         | <span data-ttu-id="172b0-815">幅計算。</span><span class="sxs-lookup"><span data-stu-id="172b0-815">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="172b0-816">正確。</span><span class="sxs-lookup"><span data-stu-id="172b0-816">Exact.</span></span>        | <span data-ttu-id="172b0-817">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="172b0-817">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="172b0-818">自動。</span><span class="sxs-lookup"><span data-stu-id="172b0-818">Auto.</span></span>         | <span data-ttu-id="172b0-819">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="172b0-819">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="172b0-820">列の幅。</span><span class="sxs-lookup"><span data-stu-id="172b0-820">Column width.</span></span> | <span data-ttu-id="172b0-821">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="172b0-821">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="172b0-822">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="172b0-822">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="172b0-823">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="172b0-823">Method widthValue</span></span>

<span data-ttu-id="172b0-824">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="172b0-824">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="172b0-825">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="172b0-825">Parameters - widthValue</span></span>

<span data-ttu-id="172b0-826">値</span><span class="sxs-lookup"><span data-stu-id="172b0-826">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="172b0-827">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="172b0-827">Return Value - widthValue</span></span>

<span data-ttu-id="172b0-828">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="172b0-828">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="172b0-829">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="172b0-829">Remarks - widthValue</span></span>

<span data-ttu-id="172b0-830">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="172b0-830">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="172b0-831">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="172b0-831">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="172b0-832">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="172b0-832">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="172b0-833">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="172b0-833">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="172b0-834">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="172b0-834">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="172b0-835">overrideObject</span><span class="sxs-lookup"><span data-stu-id="172b0-835">overrideObject</span></span>  

