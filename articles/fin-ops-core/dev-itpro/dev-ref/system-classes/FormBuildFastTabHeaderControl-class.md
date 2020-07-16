---
title: FormBuildFastTabHeaderControl クラス
description: このトピックでは、FormBuildFastTabHeaderControl クラスについて説明します。
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
ms.openlocfilehash: 976f51596f132e9846e6593e7cb706bc36855cdf
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502653"
---
# <a name="class-formbuildfasttabheadercontrol"></a><span data-ttu-id="2947e-103">クラス FormBuildFastTabHeaderControl</span><span class="sxs-lookup"><span data-stu-id="2947e-103">Class FormBuildFastTabHeaderControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildFastTabHeaderControl extends FormBuildControl
```

## <a name="remarks"></a><span data-ttu-id="2947e-104">備考</span><span class="sxs-lookup"><span data-stu-id="2947e-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="2947e-105">例</span><span class="sxs-lookup"><span data-stu-id="2947e-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="2947e-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="2947e-106">Methods</span></span>

| <span data-ttu-id="2947e-107">方法</span><span class="sxs-lookup"><span data-stu-id="2947e-107">Method</span></span>                                                                                                      | <span data-ttu-id="2947e-108">説明</span><span class="sxs-lookup"><span data-stu-id="2947e-108">Description</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2947e-109">public boolean alignChild(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-109">public boolean alignChild(\[boolean value\])</span></span>                                                                |                                                                                                                                           |
| <span data-ttu-id="2947e-110">public boolean alignChildren(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-110">public boolean alignChildren(\[boolean value\])</span></span>                                                             |                                                                                                                                           |
| <span data-ttu-id="2947e-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="2947e-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-112">Determines whether to align the control.</span></span>                                                                                                  |
| <span data-ttu-id="2947e-113">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-113">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="2947e-114">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-114">Determines whether the user can change the contents of the control.</span></span>                                                                       |
| <span data-ttu-id="2947e-115">public int allowUserSetup(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-115">public int allowUserSetup(\[int value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="2947e-116">public int arrangeGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-116">public int arrangeGuide(\[int value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="2947e-117">public int arrangeMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-117">public int arrangeMethod(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="2947e-118">public int arrangeWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-118">public int arrangeWhen(\[int value\])</span></span>                                                                       |                                                                                                                                           |
| <span data-ttu-id="2947e-119">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-119">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="2947e-120">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-120">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                        |
| <span data-ttu-id="2947e-121">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-121">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="2947e-122">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-122">Gets or sets the background color of the control.</span></span>                                                                                         |
| <span data-ttu-id="2947e-123">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-123">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="2947e-124">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-124">Determines whether the control background can be transparent.</span></span>                                                                            |
| <span data-ttu-id="2947e-125">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-125">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="2947e-126">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-126">Gets or sets the weight of font used to output text in the control.</span></span>                                                                       |
| <span data-ttu-id="2947e-127">public int bottomMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2947e-127">public int bottomMargin(\[int value\], \[AutoMode mode\])</span></span>                                                   |                                                                                                                                           |
| <span data-ttu-id="2947e-128">public AutoMode bottomMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2947e-128">public AutoMode bottomMarginMode(\[AutoMode mode\])</span></span>                                                         |                                                                                                                                           |
| <span data-ttu-id="2947e-129">public int bottomMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-129">public int bottomMarginValue(\[int value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="2947e-130">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-130">public str caption(\[str value\])</span></span>                                                                           | <span data-ttu-id="2947e-131">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-131">Gets or set the caption of the control.</span></span>                                                                                                   |
| <span data-ttu-id="2947e-132">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-132">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="2947e-133">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-133">Gets or sets the character set of the font.</span></span>                                                                                               |
| <span data-ttu-id="2947e-134">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-134">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="2947e-135">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-135">Gets or sets the color scheme of the control.</span></span>                                                                                             |
| <span data-ttu-id="2947e-136">public int columns(\[int value\], \[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2947e-136">public int columns(\[int value\], \[ColumnsMode mode\])</span></span>                                                     |                                                                                                                                           |
| <span data-ttu-id="2947e-137">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2947e-137">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span></span>                                                        |                                                                                                                                           |
| <span data-ttu-id="2947e-138">public int columnspace(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2947e-138">public int columnspace(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                           |
| <span data-ttu-id="2947e-139">public AutoMode columnspaceMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2947e-139">public AutoMode columnspaceMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="2947e-140">public int columnspaceValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-140">public int columnspaceValue(\[int value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="2947e-141">public int columnsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-141">public int columnsValue(\[int value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="2947e-142">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-142">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="2947e-143">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-143">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                       |
| <span data-ttu-id="2947e-144">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="2947e-144">public int containerId()</span></span>                                                                                    | <span data-ttu-id="2947e-145">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="2947e-145">Retrieves the ID of the parent container for the control.</span></span>                                                                                 |
| <span data-ttu-id="2947e-146">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-146">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                           |
| <span data-ttu-id="2947e-147">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-147">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                           |
| <span data-ttu-id="2947e-148">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-148">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="2947e-149">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-149">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="2947e-150">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-150">Gets or sets a data source to be used by the control or the form.</span></span>                                                                         |
| <span data-ttu-id="2947e-151">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-151">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="2947e-152">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-152">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="2947e-153">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-153">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                         |
| <span data-ttu-id="2947e-154">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-154">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="2947e-155">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-155">Determines whether to enable or disable the object.</span></span>                                                                                       |
| <span data-ttu-id="2947e-156">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-156">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="2947e-157">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-157">Gets or sets the name of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="2947e-158">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-158">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="2947e-159">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-159">Gets or sets the size of the font for the control to use.</span></span>                                                                                 |
| <span data-ttu-id="2947e-160">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="2947e-160">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="2947e-161">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-161">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="2947e-162">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-162">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="2947e-163">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-163">Gets or sets a calculation mode for the height of the control.</span></span>                                                                            |
| <span data-ttu-id="2947e-164">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-164">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="2947e-165">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-165">Gets or sets the height of the control.</span></span>                                                                                                   |
| <span data-ttu-id="2947e-166">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-166">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="2947e-167">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-167">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                  |
| <span data-ttu-id="2947e-168">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-168">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                               |                                                                                                                                           |
| <span data-ttu-id="2947e-169">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-169">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="2947e-170">public int id()</span><span class="sxs-lookup"><span data-stu-id="2947e-170">public int id()</span></span>                                                                                             | <span data-ttu-id="2947e-171">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="2947e-171">Retrieves the ID of the control.</span></span>                                                                                                          |
| <span data-ttu-id="2947e-172">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="2947e-172">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="2947e-173">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2947e-173">Retrieves a value that indicates whether the control is a container control.</span></span>                                                              |
| <span data-ttu-id="2947e-174">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-174">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="2947e-175">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="2947e-175">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="2947e-176">public int leftMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2947e-176">public int leftMargin(\[int value\], \[AutoMode mode\])</span></span>                                                     |                                                                                                                                           |
| <span data-ttu-id="2947e-177">public AutoMode leftMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2947e-177">public AutoMode leftMarginMode(\[AutoMode mode\])</span></span>                                                           |                                                                                                                                           |
| <span data-ttu-id="2947e-178">public int leftMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-178">public int leftMarginValue(\[int value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="2947e-179">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-179">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="2947e-180">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-180">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="2947e-181">public int moveControl(int controlId, \[int insertAfterControlId\])</span><span class="sxs-lookup"><span data-stu-id="2947e-181">public int moveControl(int controlId, \[int insertAfterControlId\])</span></span>                                         | <span data-ttu-id="2947e-182">コントロールに指定されたコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="2947e-182">Moves a specified control to the control.</span></span>                                                                                                 |
| <span data-ttu-id="2947e-183">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-183">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="2947e-184">フォーム、レポート、テーブル、クエリ、または別のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-184">Gets or sets the name that is used in code to identify a form, report, table, query, or another application object.</span></span> |
| <span data-ttu-id="2947e-185">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-185">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="2947e-186">public int rightMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2947e-186">public int rightMargin(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                           |
| <span data-ttu-id="2947e-187">public AutoMode rightMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2947e-187">public AutoMode rightMarginMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="2947e-188">public int rightMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-188">public int rightMarginValue(\[int value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="2947e-189">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-189">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                           |
| <span data-ttu-id="2947e-190">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-190">public boolean skip(\[boolean value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="2947e-191">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="2947e-191">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="2947e-192">public int topMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2947e-192">public int topMargin(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="2947e-193">public AutoMode topMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2947e-193">public AutoMode topMarginMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                           |
| <span data-ttu-id="2947e-194">public int topMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-194">public int topMarginValue(\[int value\])</span></span>                                                                    |                                                                                                                                           |
| <span data-ttu-id="2947e-195">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-195">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                           |
| <span data-ttu-id="2947e-196">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-196">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="2947e-197">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-197">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="2947e-198">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-198">public boolean underline(\[boolean value\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="2947e-199">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-199">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="2947e-200">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-200">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="2947e-201">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-201">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="2947e-202">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-202">public boolean useUserLayout(\[boolean value\])</span></span>                                                             |                                                                                                                                           |
| <span data-ttu-id="2947e-203">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2947e-203">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                           |
| <span data-ttu-id="2947e-204">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="2947e-204">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                           |
| <span data-ttu-id="2947e-205">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-205">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                           |
| <span data-ttu-id="2947e-206">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-206">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="2947e-207">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="2947e-207">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="2947e-208">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-208">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="2947e-209">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-209">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="2947e-210">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-210">Gets or sets the calculation mode of the width of the control.</span></span>                                                                            |
| <span data-ttu-id="2947e-211">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2947e-211">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="2947e-212">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-212">Gets or sets the width of the control.</span></span>                                                                                                    |
| <span data-ttu-id="2947e-213">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="2947e-213">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                           |

## <a name="method-alignchild"></a><span data-ttu-id="2947e-214">メソッド alignChild</span><span class="sxs-lookup"><span data-stu-id="2947e-214">Method alignChild</span></span>

```xpp
public boolean alignChild([boolean value])
```

### <a name="parameters---alignchild"></a><span data-ttu-id="2947e-215">パラメーター - alignChild</span><span class="sxs-lookup"><span data-stu-id="2947e-215">Parameters - alignChild</span></span>

<span data-ttu-id="2947e-216">値</span><span class="sxs-lookup"><span data-stu-id="2947e-216">value</span></span>  

### <a name="return-value---alignchild"></a><span data-ttu-id="2947e-217">戻り値 - alignChild</span><span class="sxs-lookup"><span data-stu-id="2947e-217">Return Value - alignChild</span></span>

## <a name="method-alignchildren"></a><span data-ttu-id="2947e-218">メソッド alignChildren</span><span class="sxs-lookup"><span data-stu-id="2947e-218">Method alignChildren</span></span>

```xpp
public boolean alignChildren([boolean value])
```

### <a name="parameters---alignchildren"></a><span data-ttu-id="2947e-219">パラメーター - alignChildren</span><span class="sxs-lookup"><span data-stu-id="2947e-219">Parameters - alignChildren</span></span>

<span data-ttu-id="2947e-220">値</span><span class="sxs-lookup"><span data-stu-id="2947e-220">value</span></span>  

### <a name="return-value---alignchildren"></a><span data-ttu-id="2947e-221">戻り値 - alignChildren</span><span class="sxs-lookup"><span data-stu-id="2947e-221">Return Value - alignChildren</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="2947e-222">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="2947e-222">Method alignControl</span></span>

<span data-ttu-id="2947e-223">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-223">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="2947e-224">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="2947e-224">Parameters - alignControl</span></span>

<span data-ttu-id="2947e-225">値</span><span class="sxs-lookup"><span data-stu-id="2947e-225">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="2947e-226">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="2947e-226">Return Value - alignControl</span></span>

<span data-ttu-id="2947e-227">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="2947e-227">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="2947e-228">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="2947e-228">Remarks - alignControl</span></span>

<span data-ttu-id="2947e-229">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="2947e-229">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="2947e-230">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="2947e-230">Method allowEdit</span></span>

<span data-ttu-id="2947e-231">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-231">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="2947e-232">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="2947e-232">Parameters - allowEdit</span></span>

<span data-ttu-id="2947e-233">値</span><span class="sxs-lookup"><span data-stu-id="2947e-233">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="2947e-234">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="2947e-234">Return Value - allowEdit</span></span>

<span data-ttu-id="2947e-235">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2947e-235">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="2947e-236">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="2947e-236">Remarks - allowEdit</span></span>

<span data-ttu-id="2947e-237">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="2947e-237">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-allowusersetup"></a><span data-ttu-id="2947e-238">メソッド allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="2947e-238">Method allowUserSetup</span></span>

```xpp
public int allowUserSetup([int value])
```

### <a name="parameters---allowusersetup"></a><span data-ttu-id="2947e-239">パラメーター - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="2947e-239">Parameters - allowUserSetup</span></span>

<span data-ttu-id="2947e-240">値</span><span class="sxs-lookup"><span data-stu-id="2947e-240">value</span></span>  

### <a name="return-value---allowusersetup"></a><span data-ttu-id="2947e-241">戻り値 - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="2947e-241">Return Value - allowUserSetup</span></span>

## <a name="method-arrangeguide"></a><span data-ttu-id="2947e-242">メソッド arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="2947e-242">Method arrangeGuide</span></span>

```xpp
public int arrangeGuide([int value])
```

### <a name="parameters---arrangeguide"></a><span data-ttu-id="2947e-243">パラメーター - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="2947e-243">Parameters - arrangeGuide</span></span>

<span data-ttu-id="2947e-244">値</span><span class="sxs-lookup"><span data-stu-id="2947e-244">value</span></span>  

### <a name="return-value---arrangeguide"></a><span data-ttu-id="2947e-245">戻り値 - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="2947e-245">Return Value - arrangeGuide</span></span>

## <a name="method-arrangemethod"></a><span data-ttu-id="2947e-246">メソッド arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="2947e-246">Method arrangeMethod</span></span>

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a><span data-ttu-id="2947e-247">パラメーター - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="2947e-247">Parameters - arrangeMethod</span></span>

<span data-ttu-id="2947e-248">値</span><span class="sxs-lookup"><span data-stu-id="2947e-248">value</span></span>  

### <a name="return-value---arrangemethod"></a><span data-ttu-id="2947e-249">戻り値 - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="2947e-249">Return Value - arrangeMethod</span></span>

## <a name="method-arrangewhen"></a><span data-ttu-id="2947e-250">メソッド arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="2947e-250">Method arrangeWhen</span></span>

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a><span data-ttu-id="2947e-251">パラメーター - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="2947e-251">Parameters - arrangeWhen</span></span>

<span data-ttu-id="2947e-252">値</span><span class="sxs-lookup"><span data-stu-id="2947e-252">value</span></span>  

### <a name="return-value---arrangewhen"></a><span data-ttu-id="2947e-253">戻り値 - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="2947e-253">Return Value - arrangeWhen</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="2947e-254">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="2947e-254">Method autoDeclaration</span></span>

<span data-ttu-id="2947e-255">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-255">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="2947e-256">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="2947e-256">Parameters - autoDeclaration</span></span>

<span data-ttu-id="2947e-257">値</span><span class="sxs-lookup"><span data-stu-id="2947e-257">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="2947e-258">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="2947e-258">Return Value - autoDeclaration</span></span>

<span data-ttu-id="2947e-259">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2947e-259">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="2947e-260">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="2947e-260">Remarks - autoDeclaration</span></span>

<span data-ttu-id="2947e-261">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="2947e-261">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="2947e-262">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="2947e-262">Method backgroundColor</span></span>

<span data-ttu-id="2947e-263">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-263">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="2947e-264">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="2947e-264">Parameters - backgroundColor</span></span>

<span data-ttu-id="2947e-265">値</span><span class="sxs-lookup"><span data-stu-id="2947e-265">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="2947e-266">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="2947e-266">Return Value - backgroundColor</span></span>

<span data-ttu-id="2947e-267">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="2947e-267">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="2947e-268">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="2947e-268">Remarks - backgroundColor</span></span>

<span data-ttu-id="2947e-269">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="2947e-269">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="2947e-270">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2947e-270">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="2947e-271">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="2947e-271">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="2947e-272">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="2947e-272">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="2947e-273">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="2947e-273">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="2947e-274">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="2947e-274">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="2947e-275">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="2947e-275">Method backStyle</span></span>

<span data-ttu-id="2947e-276">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-276">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="2947e-277">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="2947e-277">Parameters - backStyle</span></span>

<span data-ttu-id="2947e-278">値</span><span class="sxs-lookup"><span data-stu-id="2947e-278">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="2947e-279">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="2947e-279">Return Value - backStyle</span></span>

<span data-ttu-id="2947e-280">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="2947e-280">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="2947e-281">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="2947e-281">Method bold</span></span>

<span data-ttu-id="2947e-282">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-282">Gets or sets the weight of font used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="2947e-283">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="2947e-283">Parameters - bold</span></span>

<span data-ttu-id="2947e-284">値</span><span class="sxs-lookup"><span data-stu-id="2947e-284">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="2947e-285">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="2947e-285">Return Value - bold</span></span>

<span data-ttu-id="2947e-286">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="2947e-286">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="2947e-287">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="2947e-287">Remarks - bold</span></span>

<span data-ttu-id="2947e-288">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2947e-288">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="2947e-289">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="2947e-289">0 Use the default font weight.</span></span>
-   <span data-ttu-id="2947e-290">1 シン。</span><span class="sxs-lookup"><span data-stu-id="2947e-290">1 Thin.</span></span>
-   <span data-ttu-id="2947e-291">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="2947e-291">2 Extra-light.</span></span>
-   <span data-ttu-id="2947e-292">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="2947e-292">3 Light.</span></span>
-   <span data-ttu-id="2947e-293">4 標準。</span><span class="sxs-lookup"><span data-stu-id="2947e-293">4 Normal.</span></span>
-   <span data-ttu-id="2947e-294">5 中。</span><span class="sxs-lookup"><span data-stu-id="2947e-294">5 Medium.</span></span>
-   <span data-ttu-id="2947e-295">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="2947e-295">6 Semibold.</span></span>
-   <span data-ttu-id="2947e-296">7 太字。</span><span class="sxs-lookup"><span data-stu-id="2947e-296">7 Bold.</span></span>
-   <span data-ttu-id="2947e-297">8 極太。</span><span class="sxs-lookup"><span data-stu-id="2947e-297">8 Extra-bold.</span></span>
-   <span data-ttu-id="2947e-298">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="2947e-298">9 Heavy.</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="2947e-299">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="2947e-299">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="2947e-300">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="2947e-300">Parameters - bottomMargin</span></span>

<span data-ttu-id="2947e-301">値</span><span class="sxs-lookup"><span data-stu-id="2947e-301">value</span></span>  

<!-- -->

<span data-ttu-id="2947e-302">モード</span><span class="sxs-lookup"><span data-stu-id="2947e-302">mode</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="2947e-303">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="2947e-303">Return Value - bottomMargin</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="2947e-304">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="2947e-304">Method bottomMarginMode</span></span>

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="2947e-305">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="2947e-305">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="2947e-306">モード</span><span class="sxs-lookup"><span data-stu-id="2947e-306">mode</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="2947e-307">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="2947e-307">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="2947e-308">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="2947e-308">Method bottomMarginValue</span></span>

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="2947e-309">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="2947e-309">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="2947e-310">値</span><span class="sxs-lookup"><span data-stu-id="2947e-310">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="2947e-311">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="2947e-311">Return Value - bottomMarginValue</span></span>

## <a name="method-caption"></a><span data-ttu-id="2947e-312">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="2947e-312">Method caption</span></span>

<span data-ttu-id="2947e-313">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-313">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="2947e-314">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="2947e-314">Parameters - caption</span></span>

<span data-ttu-id="2947e-315">値</span><span class="sxs-lookup"><span data-stu-id="2947e-315">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="2947e-316">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="2947e-316">Return Value - caption</span></span>

<span data-ttu-id="2947e-317">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="2947e-317">The string that is used as the caption of the control.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="2947e-318">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="2947e-318">Method characterSet</span></span>

<span data-ttu-id="2947e-319">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-319">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="2947e-320">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="2947e-320">Parameters - characterSet</span></span>

<span data-ttu-id="2947e-321">値</span><span class="sxs-lookup"><span data-stu-id="2947e-321">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="2947e-322">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="2947e-322">Return Value - characterSet</span></span>

<span data-ttu-id="2947e-323">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2947e-323">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="2947e-324">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="2947e-324">Remarks - characterSet</span></span>

<span data-ttu-id="2947e-325">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="2947e-325">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="2947e-326">値です。</span><span class="sxs-lookup"><span data-stu-id="2947e-326">Value.</span></span> | <span data-ttu-id="2947e-327">説明。</span><span class="sxs-lookup"><span data-stu-id="2947e-327">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="2947e-328">0</span><span class="sxs-lookup"><span data-stu-id="2947e-328">0</span></span>      | <span data-ttu-id="2947e-329">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2947e-329">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="2947e-330">1</span><span class="sxs-lookup"><span data-stu-id="2947e-330">1</span></span>      | <span data-ttu-id="2947e-331">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2947e-331">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="2947e-332">2</span><span class="sxs-lookup"><span data-stu-id="2947e-332">2</span></span>      | <span data-ttu-id="2947e-333">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2947e-333">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="2947e-334">77</span><span class="sxs-lookup"><span data-stu-id="2947e-334">77</span></span>     | <span data-ttu-id="2947e-335">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2947e-335">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="2947e-336">128</span><span class="sxs-lookup"><span data-stu-id="2947e-336">128</span></span>    | <span data-ttu-id="2947e-337">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2947e-337">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="2947e-338">129</span><span class="sxs-lookup"><span data-stu-id="2947e-338">129</span></span>    | <span data-ttu-id="2947e-339">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2947e-339">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="2947e-340">134</span><span class="sxs-lookup"><span data-stu-id="2947e-340">134</span></span>    | <span data-ttu-id="2947e-341">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2947e-341">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="2947e-342">136</span><span class="sxs-lookup"><span data-stu-id="2947e-342">136</span></span>    | <span data-ttu-id="2947e-343">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2947e-343">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="2947e-344">161</span><span class="sxs-lookup"><span data-stu-id="2947e-344">161</span></span>    | <span data-ttu-id="2947e-345">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2947e-345">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="2947e-346">162</span><span class="sxs-lookup"><span data-stu-id="2947e-346">162</span></span>    | <span data-ttu-id="2947e-347">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2947e-347">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="2947e-348">163</span><span class="sxs-lookup"><span data-stu-id="2947e-348">163</span></span>    | <span data-ttu-id="2947e-349">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2947e-349">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="2947e-350">186</span><span class="sxs-lookup"><span data-stu-id="2947e-350">186</span></span>    | <span data-ttu-id="2947e-351">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2947e-351">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="2947e-352">204</span><span class="sxs-lookup"><span data-stu-id="2947e-352">204</span></span>    | <span data-ttu-id="2947e-353">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2947e-353">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="2947e-354">238</span><span class="sxs-lookup"><span data-stu-id="2947e-354">238</span></span>    | <span data-ttu-id="2947e-355">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2947e-355">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="2947e-356">255</span><span class="sxs-lookup"><span data-stu-id="2947e-356">255</span></span>    | <span data-ttu-id="2947e-357">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2947e-357">OEM\_CHARSET</span></span>         |

<span data-ttu-id="2947e-358">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="2947e-358">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="2947e-359">値です。</span><span class="sxs-lookup"><span data-stu-id="2947e-359">Value.</span></span> | <span data-ttu-id="2947e-360">説明。</span><span class="sxs-lookup"><span data-stu-id="2947e-360">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="2947e-361">130</span><span class="sxs-lookup"><span data-stu-id="2947e-361">130</span></span>    | <span data-ttu-id="2947e-362">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2947e-362">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="2947e-363">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="2947e-363">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="2947e-364">値です。</span><span class="sxs-lookup"><span data-stu-id="2947e-364">Value.</span></span> | <span data-ttu-id="2947e-365">説明。</span><span class="sxs-lookup"><span data-stu-id="2947e-365">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="2947e-366">177</span><span class="sxs-lookup"><span data-stu-id="2947e-366">177</span></span>    | <span data-ttu-id="2947e-367">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2947e-367">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="2947e-368">178</span><span class="sxs-lookup"><span data-stu-id="2947e-368">178</span></span>    | <span data-ttu-id="2947e-369">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2947e-369">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="2947e-370">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="2947e-370">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="2947e-371">値です。</span><span class="sxs-lookup"><span data-stu-id="2947e-371">Value.</span></span> | <span data-ttu-id="2947e-372">説明。</span><span class="sxs-lookup"><span data-stu-id="2947e-372">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="2947e-373">222</span><span class="sxs-lookup"><span data-stu-id="2947e-373">222</span></span>    | <span data-ttu-id="2947e-374">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="2947e-374">THAI\_CHARSET</span></span> |

<span data-ttu-id="2947e-375">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="2947e-375">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="2947e-376">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="2947e-376">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="2947e-377">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2947e-377">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="2947e-378">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="2947e-378">Method colorScheme</span></span>

<span data-ttu-id="2947e-379">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-379">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="2947e-380">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="2947e-380">Parameters - colorScheme</span></span>

<span data-ttu-id="2947e-381">値</span><span class="sxs-lookup"><span data-stu-id="2947e-381">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="2947e-382">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="2947e-382">Return Value - colorScheme</span></span>

<span data-ttu-id="2947e-383">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="2947e-383">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="2947e-384">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="2947e-384">Remarks - colorScheme</span></span>

<span data-ttu-id="2947e-385">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="2947e-385">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="2947e-386">値です。</span><span class="sxs-lookup"><span data-stu-id="2947e-386">Value.</span></span> | <span data-ttu-id="2947e-387">スタイル。</span><span class="sxs-lookup"><span data-stu-id="2947e-387">Style.</span></span>                         |
|--------|--------------------------------|
| <span data-ttu-id="2947e-388">0</span><span class="sxs-lookup"><span data-stu-id="2947e-388">0</span></span>      | <span data-ttu-id="2947e-389">既定。</span><span class="sxs-lookup"><span data-stu-id="2947e-389">Default.</span></span>                       |
| <span data-ttu-id="2947e-390">1</span><span class="sxs-lookup"><span data-stu-id="2947e-390">1</span></span>      | <span data-ttu-id="2947e-391">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="2947e-391">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="2947e-392">2</span><span class="sxs-lookup"><span data-stu-id="2947e-392">2</span></span>      | <span data-ttu-id="2947e-393">真の配色。</span><span class="sxs-lookup"><span data-stu-id="2947e-393">The true-color scheme.</span></span>         |

## <a name="method-columns"></a><span data-ttu-id="2947e-394">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="2947e-394">Method columns</span></span>

```xpp
public int columns([int value], [ColumnsMode mode])
```

### <a name="parameters---columns"></a><span data-ttu-id="2947e-395">パラメーター - columns</span><span class="sxs-lookup"><span data-stu-id="2947e-395">Parameters - columns</span></span>

<span data-ttu-id="2947e-396">値</span><span class="sxs-lookup"><span data-stu-id="2947e-396">value</span></span>  

<!-- -->

<span data-ttu-id="2947e-397">モード</span><span class="sxs-lookup"><span data-stu-id="2947e-397">mode</span></span>  

### <a name="return-value---columns"></a><span data-ttu-id="2947e-398">戻り値 - columns</span><span class="sxs-lookup"><span data-stu-id="2947e-398">Return Value - columns</span></span>

## <a name="method-columnsmode"></a><span data-ttu-id="2947e-399">メソッド columnsMode</span><span class="sxs-lookup"><span data-stu-id="2947e-399">Method columnsMode</span></span>

```xpp
public ColumnsMode columnsMode([ColumnsMode mode])
```

### <a name="parameters---columnsmode"></a><span data-ttu-id="2947e-400">パラメーター - columnsMode</span><span class="sxs-lookup"><span data-stu-id="2947e-400">Parameters - columnsMode</span></span>

<span data-ttu-id="2947e-401">モード</span><span class="sxs-lookup"><span data-stu-id="2947e-401">mode</span></span>  

### <a name="return-value---columnsmode"></a><span data-ttu-id="2947e-402">戻り値 - columnsMode</span><span class="sxs-lookup"><span data-stu-id="2947e-402">Return Value - columnsMode</span></span>

## <a name="method-columnspace"></a><span data-ttu-id="2947e-403">メソッド columnspace</span><span class="sxs-lookup"><span data-stu-id="2947e-403">Method columnspace</span></span>

```xpp
public int columnspace([int value], [AutoMode mode])
```

### <a name="parameters---columnspace"></a><span data-ttu-id="2947e-404">パラメーター - columnspace</span><span class="sxs-lookup"><span data-stu-id="2947e-404">Parameters - columnspace</span></span>

<span data-ttu-id="2947e-405">値</span><span class="sxs-lookup"><span data-stu-id="2947e-405">value</span></span>  

<!-- -->

<span data-ttu-id="2947e-406">モード</span><span class="sxs-lookup"><span data-stu-id="2947e-406">mode</span></span>  

### <a name="return-value---columnspace"></a><span data-ttu-id="2947e-407">戻り値 - columnspace</span><span class="sxs-lookup"><span data-stu-id="2947e-407">Return Value - columnspace</span></span>

## <a name="method-columnspacemode"></a><span data-ttu-id="2947e-408">メソッド columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="2947e-408">Method columnspaceMode</span></span>

```xpp
public AutoMode columnspaceMode([AutoMode mode])
```

### <a name="parameters---columnspacemode"></a><span data-ttu-id="2947e-409">パラメーター - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="2947e-409">Parameters - columnspaceMode</span></span>

<span data-ttu-id="2947e-410">モード</span><span class="sxs-lookup"><span data-stu-id="2947e-410">mode</span></span>  

### <a name="return-value---columnspacemode"></a><span data-ttu-id="2947e-411">戻り値 - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="2947e-411">Return Value - columnspaceMode</span></span>

## <a name="method-columnspacevalue"></a><span data-ttu-id="2947e-412">メソッド columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="2947e-412">Method columnspaceValue</span></span>

```xpp
public int columnspaceValue([int value])
```

### <a name="parameters---columnspacevalue"></a><span data-ttu-id="2947e-413">パラメーター - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="2947e-413">Parameters - columnspaceValue</span></span>

<span data-ttu-id="2947e-414">値</span><span class="sxs-lookup"><span data-stu-id="2947e-414">value</span></span>  

### <a name="return-value---columnspacevalue"></a><span data-ttu-id="2947e-415">戻り値 - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="2947e-415">Return Value - columnspaceValue</span></span>

## <a name="method-columnsvalue"></a><span data-ttu-id="2947e-416">メソッド columnsValue</span><span class="sxs-lookup"><span data-stu-id="2947e-416">Method columnsValue</span></span>

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a><span data-ttu-id="2947e-417">パラメーター - columnsValue</span><span class="sxs-lookup"><span data-stu-id="2947e-417">Parameters - columnsValue</span></span>

<span data-ttu-id="2947e-418">値</span><span class="sxs-lookup"><span data-stu-id="2947e-418">value</span></span>  

### <a name="return-value---columnsvalue"></a><span data-ttu-id="2947e-419">戻り値 - columnsValue</span><span class="sxs-lookup"><span data-stu-id="2947e-419">Return Value - columnsValue</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="2947e-420">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="2947e-420">Method configurationKey</span></span>

<span data-ttu-id="2947e-421">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-421">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="2947e-422">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="2947e-422">Parameters - configurationKey</span></span>

<span data-ttu-id="2947e-423">値</span><span class="sxs-lookup"><span data-stu-id="2947e-423">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="2947e-424">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="2947e-424">Return Value - configurationKey</span></span>

<span data-ttu-id="2947e-425">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="2947e-425">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="2947e-426">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="2947e-426">Remarks - configurationKey</span></span>

<span data-ttu-id="2947e-427">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="2947e-427">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="2947e-428">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="2947e-428">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="2947e-429">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="2947e-429">Method containerId</span></span>

<span data-ttu-id="2947e-430">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="2947e-430">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="2947e-431">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="2947e-431">Return Value - containerId</span></span>

<span data-ttu-id="2947e-432">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="2947e-432">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="2947e-433">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="2947e-433">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="2947e-434">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="2947e-434">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="2947e-435">値</span><span class="sxs-lookup"><span data-stu-id="2947e-435">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="2947e-436">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="2947e-436">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="2947e-437">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="2947e-437">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="2947e-438">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="2947e-438">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="2947e-439">値</span><span class="sxs-lookup"><span data-stu-id="2947e-439">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="2947e-440">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="2947e-440">Return Value - countryRegionContextField</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="2947e-441">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="2947e-441">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="2947e-442">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="2947e-442">Parameters - dataRelationPath</span></span>

<span data-ttu-id="2947e-443">値</span><span class="sxs-lookup"><span data-stu-id="2947e-443">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="2947e-444">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="2947e-444">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="2947e-445">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="2947e-445">Method dataSource</span></span>

<span data-ttu-id="2947e-446">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-446">Gets or sets a data source to be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="2947e-447">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="2947e-447">Parameters - dataSource</span></span>

<span data-ttu-id="2947e-448">値</span><span class="sxs-lookup"><span data-stu-id="2947e-448">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="2947e-449">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="2947e-449">Return Value - dataSource</span></span>

<span data-ttu-id="2947e-450">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="2947e-450">The identifier of the data source to be used.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="2947e-451">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="2947e-451">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="2947e-452">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="2947e-452">Parameters - displayTarget</span></span>

<span data-ttu-id="2947e-453">値</span><span class="sxs-lookup"><span data-stu-id="2947e-453">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="2947e-454">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="2947e-454">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="2947e-455">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="2947e-455">Method dragDrop</span></span>

<span data-ttu-id="2947e-456">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-456">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="2947e-457">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="2947e-457">Parameters - dragDrop</span></span>

<span data-ttu-id="2947e-458">値</span><span class="sxs-lookup"><span data-stu-id="2947e-458">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="2947e-459">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="2947e-459">Return Value - dragDrop</span></span>

<span data-ttu-id="2947e-460">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="2947e-460">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="2947e-461">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="2947e-461">Method enabled</span></span>

<span data-ttu-id="2947e-462">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-462">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="2947e-463">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="2947e-463">Parameters - enabled</span></span>

<span data-ttu-id="2947e-464">値</span><span class="sxs-lookup"><span data-stu-id="2947e-464">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="2947e-465">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="2947e-465">Return Value - enabled</span></span>

<span data-ttu-id="2947e-466">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2947e-466">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="2947e-467">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="2947e-467">Remarks - enabled</span></span>

<span data-ttu-id="2947e-468">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="2947e-468">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="2947e-469">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="2947e-469">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="2947e-470">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="2947e-470">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-font"></a><span data-ttu-id="2947e-471">メソッド font</span><span class="sxs-lookup"><span data-stu-id="2947e-471">Method font</span></span>

<span data-ttu-id="2947e-472">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-472">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="2947e-473">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="2947e-473">Parameters - font</span></span>

<span data-ttu-id="2947e-474">値</span><span class="sxs-lookup"><span data-stu-id="2947e-474">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="2947e-475">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="2947e-475">Return Value - font</span></span>

<span data-ttu-id="2947e-476">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="2947e-476">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="2947e-477">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="2947e-477">Method fontSize</span></span>

<span data-ttu-id="2947e-478">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-478">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="2947e-479">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="2947e-479">Parameters - fontSize</span></span>

<span data-ttu-id="2947e-480">値</span><span class="sxs-lookup"><span data-stu-id="2947e-480">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="2947e-481">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="2947e-481">Return Value - fontSize</span></span>

<span data-ttu-id="2947e-482">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="2947e-482">The height of the font in points.</span></span>

## <a name="method-height"></a><span data-ttu-id="2947e-483">メソッド height</span><span class="sxs-lookup"><span data-stu-id="2947e-483">Method height</span></span>

<span data-ttu-id="2947e-484">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-484">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="2947e-485">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="2947e-485">Parameters - height</span></span>

<span data-ttu-id="2947e-486">値</span><span class="sxs-lookup"><span data-stu-id="2947e-486">value</span></span>  

<!-- -->

<span data-ttu-id="2947e-487">モード</span><span class="sxs-lookup"><span data-stu-id="2947e-487">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="2947e-488">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="2947e-488">Return Value - height</span></span>

<span data-ttu-id="2947e-489">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="2947e-489">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="2947e-490">備考 - height</span><span class="sxs-lookup"><span data-stu-id="2947e-490">Remarks - height</span></span>

<span data-ttu-id="2947e-491">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="2947e-491">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="2947e-492">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="2947e-492">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="2947e-493">モード。</span><span class="sxs-lookup"><span data-stu-id="2947e-493">Mode.</span></span>            | <span data-ttu-id="2947e-494">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="2947e-494">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2947e-495">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="2947e-495">-1 Exact.</span></span>        | <span data-ttu-id="2947e-496">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="2947e-496">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="2947e-497">0 自動。</span><span class="sxs-lookup"><span data-stu-id="2947e-497">0 Auto.</span></span>          | <span data-ttu-id="2947e-498">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="2947e-498">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="2947e-499">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="2947e-499">1 Column height.</span></span> | <span data-ttu-id="2947e-500">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="2947e-500">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="2947e-501">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="2947e-501">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="2947e-502">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="2947e-502">Method heightMode</span></span>

<span data-ttu-id="2947e-503">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-503">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="2947e-504">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="2947e-504">Parameters - heightMode</span></span>

<span data-ttu-id="2947e-505">値</span><span class="sxs-lookup"><span data-stu-id="2947e-505">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="2947e-506">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="2947e-506">Return Value - heightMode</span></span>

<span data-ttu-id="2947e-507">計算モード。</span><span class="sxs-lookup"><span data-stu-id="2947e-507">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="2947e-508">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="2947e-508">Remarks - heightMode</span></span>

<span data-ttu-id="2947e-509">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="2947e-509">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="2947e-510">モード。</span><span class="sxs-lookup"><span data-stu-id="2947e-510">Mode.</span></span>          | <span data-ttu-id="2947e-511">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="2947e-511">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2947e-512">正確。</span><span class="sxs-lookup"><span data-stu-id="2947e-512">Exact.</span></span>         | <span data-ttu-id="2947e-513">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="2947e-513">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="2947e-514">自動。</span><span class="sxs-lookup"><span data-stu-id="2947e-514">Auto.</span></span>          | <span data-ttu-id="2947e-515">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="2947e-515">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="2947e-516">列の高さ</span><span class="sxs-lookup"><span data-stu-id="2947e-516">Column height.</span></span> | <span data-ttu-id="2947e-517">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="2947e-517">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="2947e-518">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="2947e-518">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="2947e-519">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="2947e-519">Method heightValue</span></span>

<span data-ttu-id="2947e-520">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-520">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="2947e-521">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="2947e-521">Parameters - heightValue</span></span>

<span data-ttu-id="2947e-522">値</span><span class="sxs-lookup"><span data-stu-id="2947e-522">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="2947e-523">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="2947e-523">Return Value - heightValue</span></span>

<span data-ttu-id="2947e-524">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="2947e-524">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="2947e-525">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="2947e-525">Remarks - heightValue</span></span>

<span data-ttu-id="2947e-526">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="2947e-526">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="2947e-527">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="2947e-527">Method helpText</span></span>

<span data-ttu-id="2947e-528">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-528">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="2947e-529">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="2947e-529">Parameters - helpText</span></span>

<span data-ttu-id="2947e-530">値</span><span class="sxs-lookup"><span data-stu-id="2947e-530">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="2947e-531">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="2947e-531">Return Value - helpText</span></span>

<span data-ttu-id="2947e-532">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="2947e-532">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="2947e-533">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="2947e-533">Remarks - helpText</span></span>

<span data-ttu-id="2947e-534">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-534">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="2947e-535">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="2947e-535">The help text must not exceed 250 characters.</span></span>

## <a name="method-hideifempty"></a><span data-ttu-id="2947e-536">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="2947e-536">Method hideIfEmpty</span></span>

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a><span data-ttu-id="2947e-537">パラメーター - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="2947e-537">Parameters - hideIfEmpty</span></span>

<span data-ttu-id="2947e-538">値</span><span class="sxs-lookup"><span data-stu-id="2947e-538">value</span></span>  

### <a name="return-value---hideifempty"></a><span data-ttu-id="2947e-539">戻り値 - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="2947e-539">Return Value - hideIfEmpty</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="2947e-540">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="2947e-540">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="2947e-541">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="2947e-541">Parameters - hierarchyParent</span></span>

<span data-ttu-id="2947e-542">値</span><span class="sxs-lookup"><span data-stu-id="2947e-542">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="2947e-543">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="2947e-543">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="2947e-544">メソッド id</span><span class="sxs-lookup"><span data-stu-id="2947e-544">Method id</span></span>

<span data-ttu-id="2947e-545">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="2947e-545">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="2947e-546">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="2947e-546">Return Value - id</span></span>

<span data-ttu-id="2947e-547">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="2947e-547">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="2947e-548">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="2947e-548">Method isContainer</span></span>

<span data-ttu-id="2947e-549">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2947e-549">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="2947e-550">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="2947e-550">Return Value - isContainer</span></span>

<span data-ttu-id="2947e-551">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="2947e-551">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-italic"></a><span data-ttu-id="2947e-552">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="2947e-552">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="2947e-553">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="2947e-553">Parameters - italic</span></span>

<span data-ttu-id="2947e-554">値</span><span class="sxs-lookup"><span data-stu-id="2947e-554">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="2947e-555">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="2947e-555">Return Value - italic</span></span>

## <a name="method-left"></a><span data-ttu-id="2947e-556">メソッド left</span><span class="sxs-lookup"><span data-stu-id="2947e-556">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="2947e-557">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="2947e-557">Parameters - left</span></span>

<span data-ttu-id="2947e-558">値</span><span class="sxs-lookup"><span data-stu-id="2947e-558">value</span></span>  

<!-- -->

<span data-ttu-id="2947e-559">モード</span><span class="sxs-lookup"><span data-stu-id="2947e-559">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="2947e-560">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="2947e-560">Return Value - left</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="2947e-561">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="2947e-561">Method leftMargin</span></span>

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="2947e-562">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="2947e-562">Parameters - leftMargin</span></span>

<span data-ttu-id="2947e-563">値</span><span class="sxs-lookup"><span data-stu-id="2947e-563">value</span></span>  

<!-- -->

<span data-ttu-id="2947e-564">モード</span><span class="sxs-lookup"><span data-stu-id="2947e-564">mode</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="2947e-565">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="2947e-565">Return Value - leftMargin</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="2947e-566">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="2947e-566">Method leftMarginMode</span></span>

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="2947e-567">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="2947e-567">Parameters - leftMarginMode</span></span>

<span data-ttu-id="2947e-568">モード</span><span class="sxs-lookup"><span data-stu-id="2947e-568">mode</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="2947e-569">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="2947e-569">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="2947e-570">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="2947e-570">Method leftMarginValue</span></span>

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="2947e-571">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="2947e-571">Parameters - leftMarginValue</span></span>

<span data-ttu-id="2947e-572">値</span><span class="sxs-lookup"><span data-stu-id="2947e-572">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="2947e-573">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="2947e-573">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="2947e-574">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="2947e-574">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="2947e-575">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="2947e-575">Parameters - leftMode</span></span>

<span data-ttu-id="2947e-576">値</span><span class="sxs-lookup"><span data-stu-id="2947e-576">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="2947e-577">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="2947e-577">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="2947e-578">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="2947e-578">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="2947e-579">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="2947e-579">Parameters - leftValue</span></span>

<span data-ttu-id="2947e-580">値</span><span class="sxs-lookup"><span data-stu-id="2947e-580">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="2947e-581">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="2947e-581">Return Value - leftValue</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="2947e-582">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="2947e-582">Method moveControl</span></span>

<span data-ttu-id="2947e-583">コントロールに指定されたコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="2947e-583">Moves a specified control to the control.</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterControlId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="2947e-584">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="2947e-584">Parameters - moveControl</span></span>

<span data-ttu-id="2947e-585">controlId</span><span class="sxs-lookup"><span data-stu-id="2947e-585">controlId</span></span>  

<!-- -->

<span data-ttu-id="2947e-586">insertAfterControlId</span><span class="sxs-lookup"><span data-stu-id="2947e-586">insertAfterControlId</span></span>  

### <a name="return-value---movecontrol"></a><span data-ttu-id="2947e-587">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="2947e-587">Return Value - moveControl</span></span>

<span data-ttu-id="2947e-588">コントロールが正常に移動した場合は 1、それ以外の場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="2947e-588">1 if the control was moved successfully; otherwise, 0.</span></span>

### <a name="remarks---movecontrol"></a><span data-ttu-id="2947e-589">備考 - moveControl</span><span class="sxs-lookup"><span data-stu-id="2947e-589">Remarks - moveControl</span></span>

<span data-ttu-id="2947e-590">一般に、指定したコントロールをコントロールに含めることができ、現在のコンテナーから移動できる場合、このメソッドは成功します。</span><span class="sxs-lookup"><span data-stu-id="2947e-590">In general, if the specified control can be contained in the control and can be moved from the container that it is currently in, this method should succeed.</span></span> <span data-ttu-id="2947e-591">ただし、場合によっては、参照グループ コントロールのインスタンス コントロールなど、コントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="2947e-591">However, in some cases, such as for the reference group control instance, controls cannot be moved.</span></span>

## <a name="method-name"></a><span data-ttu-id="2947e-592">メソッド名</span><span class="sxs-lookup"><span data-stu-id="2947e-592">Method name</span></span>

<span data-ttu-id="2947e-593">フォーム、レポート、テーブル、クエリ、または別のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-593">Gets or sets the name that is used in code to identify a form, report, table, query, or another application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="2947e-594">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="2947e-594">Parameters - name</span></span>

<span data-ttu-id="2947e-595">値</span><span class="sxs-lookup"><span data-stu-id="2947e-595">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="2947e-596">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="2947e-596">Return Value - name</span></span>

<span data-ttu-id="2947e-597">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="2947e-597">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="2947e-598">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="2947e-598">Remarks - name</span></span>

<span data-ttu-id="2947e-599">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2947e-599">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="2947e-600">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="2947e-600">It must start with a letter.</span></span>
-   <span data-ttu-id="2947e-601">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="2947e-601">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="2947e-602">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="2947e-602">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="2947e-603">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="2947e-603">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="2947e-604">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="2947e-604">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="2947e-605">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="2947e-605">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="2947e-606">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="2947e-606">Parameters - neededPermission</span></span>

<span data-ttu-id="2947e-607">値</span><span class="sxs-lookup"><span data-stu-id="2947e-607">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="2947e-608">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="2947e-608">Return Value - neededPermission</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="2947e-609">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="2947e-609">Method rightMargin</span></span>

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="2947e-610">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="2947e-610">Parameters - rightMargin</span></span>

<span data-ttu-id="2947e-611">値</span><span class="sxs-lookup"><span data-stu-id="2947e-611">value</span></span>  

<!-- -->

<span data-ttu-id="2947e-612">モード</span><span class="sxs-lookup"><span data-stu-id="2947e-612">mode</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="2947e-613">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="2947e-613">Return Value - rightMargin</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="2947e-614">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="2947e-614">Method rightMarginMode</span></span>

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="2947e-615">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="2947e-615">Parameters - rightMarginMode</span></span>

<span data-ttu-id="2947e-616">モード</span><span class="sxs-lookup"><span data-stu-id="2947e-616">mode</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="2947e-617">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="2947e-617">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="2947e-618">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="2947e-618">Method rightMarginValue</span></span>

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="2947e-619">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="2947e-619">Parameters - rightMarginValue</span></span>

<span data-ttu-id="2947e-620">値</span><span class="sxs-lookup"><span data-stu-id="2947e-620">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="2947e-621">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="2947e-621">Return Value - rightMarginValue</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="2947e-622">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="2947e-622">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="2947e-623">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="2947e-623">Parameters - securityKey</span></span>

<span data-ttu-id="2947e-624">値</span><span class="sxs-lookup"><span data-stu-id="2947e-624">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="2947e-625">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="2947e-625">Return Value - securityKey</span></span>

## <a name="method-skip"></a><span data-ttu-id="2947e-626">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="2947e-626">Method skip</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="2947e-627">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="2947e-627">Parameters - skip</span></span>

<span data-ttu-id="2947e-628">値</span><span class="sxs-lookup"><span data-stu-id="2947e-628">value</span></span>  

### <a name="return-value---skip"></a><span data-ttu-id="2947e-629">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="2947e-629">Return Value - skip</span></span>

## <a name="method-top"></a><span data-ttu-id="2947e-630">メソッド top</span><span class="sxs-lookup"><span data-stu-id="2947e-630">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="2947e-631">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="2947e-631">Parameters - top</span></span>

<span data-ttu-id="2947e-632">値</span><span class="sxs-lookup"><span data-stu-id="2947e-632">value</span></span>  

<!-- -->

<span data-ttu-id="2947e-633">モード</span><span class="sxs-lookup"><span data-stu-id="2947e-633">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="2947e-634">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="2947e-634">Return Value - top</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="2947e-635">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="2947e-635">Method topMargin</span></span>

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="2947e-636">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="2947e-636">Parameters - topMargin</span></span>

<span data-ttu-id="2947e-637">値</span><span class="sxs-lookup"><span data-stu-id="2947e-637">value</span></span>  

<!-- -->

<span data-ttu-id="2947e-638">モード</span><span class="sxs-lookup"><span data-stu-id="2947e-638">mode</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="2947e-639">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="2947e-639">Return Value - topMargin</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="2947e-640">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="2947e-640">Method topMarginMode</span></span>

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="2947e-641">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="2947e-641">Parameters - topMarginMode</span></span>

<span data-ttu-id="2947e-642">モード</span><span class="sxs-lookup"><span data-stu-id="2947e-642">mode</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="2947e-643">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="2947e-643">Return Value - topMarginMode</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="2947e-644">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="2947e-644">Method topMarginValue</span></span>

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="2947e-645">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="2947e-645">Parameters - topMarginValue</span></span>

<span data-ttu-id="2947e-646">値</span><span class="sxs-lookup"><span data-stu-id="2947e-646">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="2947e-647">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="2947e-647">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="2947e-648">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="2947e-648">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="2947e-649">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="2947e-649">Parameters - topMode</span></span>

<span data-ttu-id="2947e-650">値</span><span class="sxs-lookup"><span data-stu-id="2947e-650">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="2947e-651">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="2947e-651">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="2947e-652">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="2947e-652">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="2947e-653">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="2947e-653">Parameters - topValue</span></span>

<span data-ttu-id="2947e-654">値</span><span class="sxs-lookup"><span data-stu-id="2947e-654">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="2947e-655">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="2947e-655">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="2947e-656">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="2947e-656">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="2947e-657">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="2947e-657">Parameters - type</span></span>

<span data-ttu-id="2947e-658">値</span><span class="sxs-lookup"><span data-stu-id="2947e-658">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="2947e-659">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="2947e-659">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="2947e-660">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="2947e-660">Method underline</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="2947e-661">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="2947e-661">Parameters - underline</span></span>

<span data-ttu-id="2947e-662">値</span><span class="sxs-lookup"><span data-stu-id="2947e-662">value</span></span>  

### <a name="return-value---underline"></a><span data-ttu-id="2947e-663">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="2947e-663">Return Value - underline</span></span>

## <a name="method-userdata"></a><span data-ttu-id="2947e-664">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="2947e-664">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="2947e-665">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="2947e-665">Parameters - userData</span></span>

<span data-ttu-id="2947e-666">値</span><span class="sxs-lookup"><span data-stu-id="2947e-666">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="2947e-667">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="2947e-667">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="2947e-668">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="2947e-668">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="2947e-669">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="2947e-669">Parameters - userDataItem</span></span>

<span data-ttu-id="2947e-670">値</span><span class="sxs-lookup"><span data-stu-id="2947e-670">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="2947e-671">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="2947e-671">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="2947e-672">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="2947e-672">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="2947e-673">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="2947e-673">Parameters - userDataItems</span></span>

<span data-ttu-id="2947e-674">値</span><span class="sxs-lookup"><span data-stu-id="2947e-674">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="2947e-675">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="2947e-675">Return Value - userDataItems</span></span>

## <a name="method-useuserlayout"></a><span data-ttu-id="2947e-676">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="2947e-676">Method useUserLayout</span></span>

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a><span data-ttu-id="2947e-677">パラメーター - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="2947e-677">Parameters - useUserLayout</span></span>

<span data-ttu-id="2947e-678">値</span><span class="sxs-lookup"><span data-stu-id="2947e-678">value</span></span>  

### <a name="return-value---useuserlayout"></a><span data-ttu-id="2947e-679">戻り値 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="2947e-679">Return Value - useUserLayout</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="2947e-680">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="2947e-680">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="2947e-681">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="2947e-681">Parameters - verticalSpacing</span></span>

<span data-ttu-id="2947e-682">値</span><span class="sxs-lookup"><span data-stu-id="2947e-682">value</span></span>  

<!-- -->

<span data-ttu-id="2947e-683">モード</span><span class="sxs-lookup"><span data-stu-id="2947e-683">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="2947e-684">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="2947e-684">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="2947e-685">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="2947e-685">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="2947e-686">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="2947e-686">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="2947e-687">モード</span><span class="sxs-lookup"><span data-stu-id="2947e-687">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="2947e-688">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="2947e-688">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="2947e-689">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="2947e-689">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="2947e-690">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="2947e-690">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="2947e-691">値</span><span class="sxs-lookup"><span data-stu-id="2947e-691">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="2947e-692">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="2947e-692">Return Value - verticalSpacingValue</span></span>

## <a name="method-visible"></a><span data-ttu-id="2947e-693">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="2947e-693">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="2947e-694">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="2947e-694">Parameters - visible</span></span>

<span data-ttu-id="2947e-695">値</span><span class="sxs-lookup"><span data-stu-id="2947e-695">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="2947e-696">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="2947e-696">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="2947e-697">メソッド width</span><span class="sxs-lookup"><span data-stu-id="2947e-697">Method width</span></span>

<span data-ttu-id="2947e-698">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-698">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="2947e-699">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="2947e-699">Parameters - width</span></span>

<span data-ttu-id="2947e-700">値</span><span class="sxs-lookup"><span data-stu-id="2947e-700">value</span></span>  

<!-- -->

<span data-ttu-id="2947e-701">モード</span><span class="sxs-lookup"><span data-stu-id="2947e-701">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="2947e-702">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="2947e-702">Return Value - width</span></span>

<span data-ttu-id="2947e-703">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="2947e-703">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="2947e-704">備考 - width</span><span class="sxs-lookup"><span data-stu-id="2947e-704">Remarks - width</span></span>

<span data-ttu-id="2947e-705">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="2947e-705">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="2947e-706">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="2947e-706">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="2947e-707">モード。</span><span class="sxs-lookup"><span data-stu-id="2947e-707">Mode.</span></span>           | <span data-ttu-id="2947e-708">幅計算。</span><span class="sxs-lookup"><span data-stu-id="2947e-708">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2947e-709">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="2947e-709">-1 Exact.</span></span>       | <span data-ttu-id="2947e-710">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2947e-710">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="2947e-711">0 自動。</span><span class="sxs-lookup"><span data-stu-id="2947e-711">0 Auto.</span></span>         | <span data-ttu-id="2947e-712">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="2947e-712">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="2947e-713">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="2947e-713">1 Column width.</span></span> | <span data-ttu-id="2947e-714">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="2947e-714">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="2947e-715">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="2947e-715">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="2947e-716">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="2947e-716">Method widthMode</span></span>

<span data-ttu-id="2947e-717">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-717">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="2947e-718">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="2947e-718">Parameters - widthMode</span></span>

<span data-ttu-id="2947e-719">値</span><span class="sxs-lookup"><span data-stu-id="2947e-719">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="2947e-720">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="2947e-720">Return Value - widthMode</span></span>

<span data-ttu-id="2947e-721">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="2947e-721">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="2947e-722">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="2947e-722">Remarks - widthMode</span></span>

<span data-ttu-id="2947e-723">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="2947e-723">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="2947e-724">モード。</span><span class="sxs-lookup"><span data-stu-id="2947e-724">Mode.</span></span>         | <span data-ttu-id="2947e-725">幅計算。</span><span class="sxs-lookup"><span data-stu-id="2947e-725">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2947e-726">正確。</span><span class="sxs-lookup"><span data-stu-id="2947e-726">Exact.</span></span>        | <span data-ttu-id="2947e-727">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2947e-727">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="2947e-728">自動。</span><span class="sxs-lookup"><span data-stu-id="2947e-728">Auto.</span></span>         | <span data-ttu-id="2947e-729">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="2947e-729">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="2947e-730">列の幅。</span><span class="sxs-lookup"><span data-stu-id="2947e-730">Column width.</span></span> | <span data-ttu-id="2947e-731">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="2947e-731">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="2947e-732">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="2947e-732">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="2947e-733">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="2947e-733">Method widthValue</span></span>

<span data-ttu-id="2947e-734">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2947e-734">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="2947e-735">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="2947e-735">Parameters - widthValue</span></span>

<span data-ttu-id="2947e-736">値</span><span class="sxs-lookup"><span data-stu-id="2947e-736">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="2947e-737">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="2947e-737">Return Value - widthValue</span></span>

<span data-ttu-id="2947e-738">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="2947e-738">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="2947e-739">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="2947e-739">Remarks - widthValue</span></span>

<span data-ttu-id="2947e-740">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="2947e-740">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="2947e-741">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="2947e-741">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="2947e-742">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="2947e-742">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="2947e-743">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="2947e-743">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="2947e-744">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="2947e-744">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="2947e-745">overrideObject</span><span class="sxs-lookup"><span data-stu-id="2947e-745">overrideObject</span></span>  

