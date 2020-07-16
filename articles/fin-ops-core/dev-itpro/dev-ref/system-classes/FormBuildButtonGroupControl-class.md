---
title: FormBuildButtonGroupControl クラス
description: このトピックでは、FormBuildButtonGroupControl クラスについて説明します。
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
ms.openlocfilehash: 76602edeb443186102d500e47e5e33523e03670d
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502976"
---
# <a name="class-formbuildbuttongroupcontrol"></a><span data-ttu-id="0d385-103">クラス FormBuildButtonGroupControl</span><span class="sxs-lookup"><span data-stu-id="0d385-103">Class FormBuildButtonGroupControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildButtonGroupControl extends FormBuildControl
```

<span data-ttu-id="0d385-104">FormBuildButtonGroupControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="0d385-104">The FormBuildButtonGroupControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d385-105">備考</span><span class="sxs-lookup"><span data-stu-id="0d385-105">Remarks</span></span>

<span data-ttu-id="0d385-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0d385-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="0d385-107">例</span><span class="sxs-lookup"><span data-stu-id="0d385-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="0d385-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="0d385-108">Methods</span></span>

| <span data-ttu-id="0d385-109">方法</span><span class="sxs-lookup"><span data-stu-id="0d385-109">Method</span></span>                                                                                                      | <span data-ttu-id="0d385-110">説明</span><span class="sxs-lookup"><span data-stu-id="0d385-110">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d385-111">public boolean alignChild(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-111">public boolean alignChild(\[boolean value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="0d385-112">public boolean alignChildren(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-112">public boolean alignChildren(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="0d385-113">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-113">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="0d385-114">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-114">Determines whether to align the control.</span></span>                                                                                                |
| <span data-ttu-id="0d385-115">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-115">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="0d385-116">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-116">Determines whether the user can change the contents of the control.</span></span>                                                                     |
| <span data-ttu-id="0d385-117">public int allowUserSetup(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-117">public int allowUserSetup(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="0d385-118">public int arrangeGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-118">public int arrangeGuide(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="0d385-119">public int arrangeMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-119">public int arrangeMethod(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="0d385-120">public int arrangeWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-120">public int arrangeWhen(\[int value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="0d385-121">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-121">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="0d385-122">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-122">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                      |
| <span data-ttu-id="0d385-123">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-123">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="0d385-124">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-124">Gets or sets the background color of the control.</span></span>                                                                                       |
| <span data-ttu-id="0d385-125">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-125">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="0d385-126">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-126">Determines whether the control background can be transparent.</span></span>                                                                          |
| <span data-ttu-id="0d385-127">public int bold(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-127">public int bold(\[int value\])</span></span>                                                                              | <span data-ttu-id="0d385-128">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-128">Gets or sets the weight of font used to output text in the control.</span></span>                                                                     |
| <span data-ttu-id="0d385-129">public int bottomMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0d385-129">public int bottomMargin(\[int value\], \[AutoMode mode\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="0d385-130">public AutoMode bottomMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0d385-130">public AutoMode bottomMarginMode(\[AutoMode mode\])</span></span>                                                         |                                                                                                                                         |
| <span data-ttu-id="0d385-131">public int bottomMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-131">public int bottomMarginValue(\[int value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="0d385-132">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-132">public str caption(\[str value\])</span></span>                                                                           | <span data-ttu-id="0d385-133">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-133">Gets or set the caption of the control.</span></span>                                                                                                 |
| <span data-ttu-id="0d385-134">public int characterSet(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-134">public int characterSet(\[int value\])</span></span>                                                                      | <span data-ttu-id="0d385-135">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-135">Gets or sets the character set of the font.</span></span>                                                                                             |
| <span data-ttu-id="0d385-136">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-136">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="0d385-137">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-137">Gets or sets the color scheme of the control.</span></span>                                                                                           |
| <span data-ttu-id="0d385-138">public int columns(\[int value\], \[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0d385-138">public int columns(\[int value\], \[ColumnsMode mode\])</span></span>                                                     |                                                                                                                                         |
| <span data-ttu-id="0d385-139">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0d385-139">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span></span>                                                        |                                                                                                                                         |
| <span data-ttu-id="0d385-140">public int columnspace(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0d385-140">public int columnspace(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                         |
| <span data-ttu-id="0d385-141">public AutoMode columnspaceMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0d385-141">public AutoMode columnspaceMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                         |
| <span data-ttu-id="0d385-142">public int columnspaceValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-142">public int columnspaceValue(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="0d385-143">public int columnsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-143">public int columnsValue(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="0d385-144">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-144">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="0d385-145">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-145">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                     |
| <span data-ttu-id="0d385-146">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="0d385-146">public int containerId()</span></span>                                                                                    | <span data-ttu-id="0d385-147">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="0d385-147">Retrieves the ID of the parent container for the control.</span></span>                                                                               |
| <span data-ttu-id="0d385-148">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-148">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="0d385-149">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-149">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                         |
| <span data-ttu-id="0d385-150">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-150">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="0d385-151">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-151">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="0d385-152">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-152">Gets or sets a data source to be used by the control or the form.</span></span>                                                                       |
| <span data-ttu-id="0d385-153">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-153">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="0d385-154">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-154">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="0d385-155">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-155">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                       |
| <span data-ttu-id="0d385-156">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-156">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="0d385-157">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-157">Determines whether to enable or disable the object.</span></span>                                                                                     |
| <span data-ttu-id="0d385-158">public str font(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-158">public str font(\[str value\])</span></span>                                                                              | <span data-ttu-id="0d385-159">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-159">Gets or sets the name of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="0d385-160">public int fontSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-160">public int fontSize(\[int value\])</span></span>                                                                          | <span data-ttu-id="0d385-161">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-161">Gets or sets the size of the font for the control to use.</span></span>                                                                               |
| <span data-ttu-id="0d385-162">public int framePosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-162">public int framePosition(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="0d385-163">public int frameType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-163">public int frameType(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="0d385-164">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="0d385-164">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="0d385-165">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-165">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="0d385-166">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-166">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="0d385-167">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-167">Gets or sets a calculation mode for the height of the control.</span></span>                                                                          |
| <span data-ttu-id="0d385-168">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-168">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="0d385-169">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-169">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="0d385-170">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-170">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="0d385-171">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-171">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                |
| <span data-ttu-id="0d385-172">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-172">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                               |                                                                                                                                         |
| <span data-ttu-id="0d385-173">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-173">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="0d385-174">public int id()</span><span class="sxs-lookup"><span data-stu-id="0d385-174">public int id()</span></span>                                                                                             | <span data-ttu-id="0d385-175">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="0d385-175">Retrieves the ID of the control.</span></span>                                                                                                        |
| <span data-ttu-id="0d385-176">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="0d385-176">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="0d385-177">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0d385-177">Retrieves a value that indicates whether the control is a container control.</span></span>                                                            |
| <span data-ttu-id="0d385-178">public boolean italic(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-178">public boolean italic(\[boolean value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="0d385-179">public str keyTip(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-179">public str keyTip(\[str value\])</span></span>                                                                            |                                                                                                                                         |
| <span data-ttu-id="0d385-180">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="0d385-180">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="0d385-181">public int leftMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0d385-181">public int leftMargin(\[int value\], \[AutoMode mode\])</span></span>                                                     |                                                                                                                                         |
| <span data-ttu-id="0d385-182">public AutoMode leftMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0d385-182">public AutoMode leftMarginMode(\[AutoMode mode\])</span></span>                                                           |                                                                                                                                         |
| <span data-ttu-id="0d385-183">public int leftMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-183">public int leftMarginValue(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="0d385-184">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-184">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="0d385-185">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-185">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="0d385-186">public int moveControl(int controlId, \[int insertAfterControlId\])</span><span class="sxs-lookup"><span data-stu-id="0d385-186">public int moveControl(int controlId, \[int insertAfterControlId\])</span></span>                                         | <span data-ttu-id="0d385-187">コントロールに指定されたコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="0d385-187">Moves a specified control to the control.</span></span>                                                                                               |
| <span data-ttu-id="0d385-188">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-188">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="0d385-189">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-189">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="0d385-190">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-190">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="0d385-191">public int rightMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0d385-191">public int rightMargin(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                         |
| <span data-ttu-id="0d385-192">public AutoMode rightMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0d385-192">public AutoMode rightMarginMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                         |
| <span data-ttu-id="0d385-193">public int rightMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-193">public int rightMarginValue(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="0d385-194">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-194">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="0d385-195">public boolean sizeHeight(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-195">public boolean sizeHeight(\[boolean value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="0d385-196">public boolean sizeWidth(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-196">public boolean sizeWidth(\[boolean value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="0d385-197">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-197">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="0d385-198">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="0d385-198">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>         |
| <span data-ttu-id="0d385-199">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-199">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                         |
| <span data-ttu-id="0d385-200">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="0d385-200">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="0d385-201">public int topMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0d385-201">public int topMargin(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="0d385-202">public AutoMode topMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0d385-202">public AutoMode topMarginMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                         |
| <span data-ttu-id="0d385-203">public int topMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-203">public int topMarginValue(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="0d385-204">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-204">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="0d385-205">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-205">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="0d385-206">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-206">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="0d385-207">public boolean underline(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-207">public boolean underline(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="0d385-208">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="0d385-208">Sets or returns the underline property for the text in the control.</span></span>                                                                     |
| <span data-ttu-id="0d385-209">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-209">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="0d385-210">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-210">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="0d385-211">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-211">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="0d385-212">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-212">public boolean useUserLayout(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="0d385-213">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0d385-213">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="0d385-214">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0d385-214">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="0d385-215">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-215">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="0d385-216">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-216">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="0d385-217">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="0d385-217">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="0d385-218">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-218">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="0d385-219">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-219">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="0d385-220">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-220">Gets or sets the calculation mode of the width of the control.</span></span>                                                                          |
| <span data-ttu-id="0d385-221">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0d385-221">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="0d385-222">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-222">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="0d385-223">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="0d385-223">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                         |

## <a name="method-alignchild"></a><span data-ttu-id="0d385-224">メソッド alignChild</span><span class="sxs-lookup"><span data-stu-id="0d385-224">Method alignChild</span></span>

```xpp
public boolean alignChild([boolean value])
```

### <a name="parameters---alignchild"></a><span data-ttu-id="0d385-225">パラメーター - alignChild</span><span class="sxs-lookup"><span data-stu-id="0d385-225">Parameters - alignChild</span></span>

<span data-ttu-id="0d385-226">値</span><span class="sxs-lookup"><span data-stu-id="0d385-226">value</span></span>  

### <a name="return-value---alignchild"></a><span data-ttu-id="0d385-227">戻り値 - alignChild</span><span class="sxs-lookup"><span data-stu-id="0d385-227">Return Value - alignChild</span></span>

## <a name="method-alignchildren"></a><span data-ttu-id="0d385-228">メソッド alignChildren</span><span class="sxs-lookup"><span data-stu-id="0d385-228">Method alignChildren</span></span>

```xpp
public boolean alignChildren([boolean value])
```

### <a name="parameters---alignchildren"></a><span data-ttu-id="0d385-229">パラメーター - alignChildren</span><span class="sxs-lookup"><span data-stu-id="0d385-229">Parameters - alignChildren</span></span>

<span data-ttu-id="0d385-230">値</span><span class="sxs-lookup"><span data-stu-id="0d385-230">value</span></span>  

### <a name="return-value---alignchildren"></a><span data-ttu-id="0d385-231">戻り値 - alignChildren</span><span class="sxs-lookup"><span data-stu-id="0d385-231">Return Value - alignChildren</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="0d385-232">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="0d385-232">Method alignControl</span></span>

<span data-ttu-id="0d385-233">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-233">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="0d385-234">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="0d385-234">Parameters - alignControl</span></span>

<span data-ttu-id="0d385-235">値</span><span class="sxs-lookup"><span data-stu-id="0d385-235">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="0d385-236">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="0d385-236">Return Value - alignControl</span></span>

<span data-ttu-id="0d385-237">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="0d385-237">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="0d385-238">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="0d385-238">Remarks - alignControl</span></span>

<span data-ttu-id="0d385-239">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="0d385-239">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="0d385-240">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="0d385-240">Method allowEdit</span></span>

<span data-ttu-id="0d385-241">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-241">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="0d385-242">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="0d385-242">Parameters - allowEdit</span></span>

<span data-ttu-id="0d385-243">値</span><span class="sxs-lookup"><span data-stu-id="0d385-243">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="0d385-244">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="0d385-244">Return Value - allowEdit</span></span>

<span data-ttu-id="0d385-245">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0d385-245">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="0d385-246">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="0d385-246">Remarks - allowEdit</span></span>

<span data-ttu-id="0d385-247">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="0d385-247">When this property is set on a container control, modifications are disabled or enabled for all controls within the container.</span></span>

## <a name="method-allowusersetup"></a><span data-ttu-id="0d385-248">メソッド allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="0d385-248">Method allowUserSetup</span></span>

```xpp
public int allowUserSetup([int value])
```

### <a name="parameters---allowusersetup"></a><span data-ttu-id="0d385-249">パラメーター - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="0d385-249">Parameters - allowUserSetup</span></span>

<span data-ttu-id="0d385-250">値</span><span class="sxs-lookup"><span data-stu-id="0d385-250">value</span></span>  

### <a name="return-value---allowusersetup"></a><span data-ttu-id="0d385-251">戻り値 - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="0d385-251">Return Value - allowUserSetup</span></span>

## <a name="method-arrangeguide"></a><span data-ttu-id="0d385-252">メソッド arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="0d385-252">Method arrangeGuide</span></span>

```xpp
public int arrangeGuide([int value])
```

### <a name="parameters---arrangeguide"></a><span data-ttu-id="0d385-253">パラメーター - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="0d385-253">Parameters - arrangeGuide</span></span>

<span data-ttu-id="0d385-254">値</span><span class="sxs-lookup"><span data-stu-id="0d385-254">value</span></span>  

### <a name="return-value---arrangeguide"></a><span data-ttu-id="0d385-255">戻り値 - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="0d385-255">Return Value - arrangeGuide</span></span>

## <a name="method-arrangemethod"></a><span data-ttu-id="0d385-256">メソッド arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="0d385-256">Method arrangeMethod</span></span>

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a><span data-ttu-id="0d385-257">パラメーター - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="0d385-257">Parameters - arrangeMethod</span></span>

<span data-ttu-id="0d385-258">値</span><span class="sxs-lookup"><span data-stu-id="0d385-258">value</span></span>  

### <a name="return-value---arrangemethod"></a><span data-ttu-id="0d385-259">戻り値 - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="0d385-259">Return Value - arrangeMethod</span></span>

## <a name="method-arrangewhen"></a><span data-ttu-id="0d385-260">メソッド arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="0d385-260">Method arrangeWhen</span></span>

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a><span data-ttu-id="0d385-261">パラメーター - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="0d385-261">Parameters - arrangeWhen</span></span>

<span data-ttu-id="0d385-262">値</span><span class="sxs-lookup"><span data-stu-id="0d385-262">value</span></span>  

### <a name="return-value---arrangewhen"></a><span data-ttu-id="0d385-263">戻り値 - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="0d385-263">Return Value - arrangeWhen</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="0d385-264">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="0d385-264">Method autoDeclaration</span></span>

<span data-ttu-id="0d385-265">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-265">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="0d385-266">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="0d385-266">Parameters - autoDeclaration</span></span>

<span data-ttu-id="0d385-267">値</span><span class="sxs-lookup"><span data-stu-id="0d385-267">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="0d385-268">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="0d385-268">Return Value - autoDeclaration</span></span>

<span data-ttu-id="0d385-269">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0d385-269">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="0d385-270">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="0d385-270">Remarks - autoDeclaration</span></span>

<span data-ttu-id="0d385-271">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="0d385-271">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="0d385-272">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="0d385-272">Method backgroundColor</span></span>

<span data-ttu-id="0d385-273">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-273">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="0d385-274">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="0d385-274">Parameters - backgroundColor</span></span>

<span data-ttu-id="0d385-275">値</span><span class="sxs-lookup"><span data-stu-id="0d385-275">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="0d385-276">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="0d385-276">Return Value - backgroundColor</span></span>

<span data-ttu-id="0d385-277">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="0d385-277">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="0d385-278">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="0d385-278">Remarks - backgroundColor</span></span>

<span data-ttu-id="0d385-279">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0d385-279">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="0d385-280">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0d385-280">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="0d385-281">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="0d385-281">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="0d385-282">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="0d385-282">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="0d385-283">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="0d385-283">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="0d385-284">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="0d385-284">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="0d385-285">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="0d385-285">Method backStyle</span></span>

<span data-ttu-id="0d385-286">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-286">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="0d385-287">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="0d385-287">Parameters - backStyle</span></span>

<span data-ttu-id="0d385-288">値</span><span class="sxs-lookup"><span data-stu-id="0d385-288">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="0d385-289">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="0d385-289">Return Value - backStyle</span></span>

<span data-ttu-id="0d385-290">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="0d385-290">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bold"></a><span data-ttu-id="0d385-291">メソッド bold</span><span class="sxs-lookup"><span data-stu-id="0d385-291">Method bold</span></span>

<span data-ttu-id="0d385-292">コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-292">Gets or sets the weight of font used to output text in the control.</span></span>

```xpp
public int bold([int value])
```

### <a name="parameters---bold"></a><span data-ttu-id="0d385-293">パラメーター - bold</span><span class="sxs-lookup"><span data-stu-id="0d385-293">Parameters - bold</span></span>

<span data-ttu-id="0d385-294">値</span><span class="sxs-lookup"><span data-stu-id="0d385-294">value</span></span>  

### <a name="return-value---bold"></a><span data-ttu-id="0d385-295">戻り値 - bold</span><span class="sxs-lookup"><span data-stu-id="0d385-295">Return Value - bold</span></span>

<span data-ttu-id="0d385-296">0 から 9 までの間の整数値。</span><span class="sxs-lookup"><span data-stu-id="0d385-296">An integer value between zero and nine, inclusive.</span></span>

### <a name="remarks---bold"></a><span data-ttu-id="0d385-297">備考 - bold</span><span class="sxs-lookup"><span data-stu-id="0d385-297">Remarks - bold</span></span>

<span data-ttu-id="0d385-298">返される整数には、次のようなフォントの重量が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0d385-298">The integer that is returned contains the weight of the font as follows:</span></span>

-   <span data-ttu-id="0d385-299">0 既定のフォントの重量を使用します。</span><span class="sxs-lookup"><span data-stu-id="0d385-299">0 Use the default font weight.</span></span>
-   <span data-ttu-id="0d385-300">1 シン。</span><span class="sxs-lookup"><span data-stu-id="0d385-300">1 Thin.</span></span>
-   <span data-ttu-id="0d385-301">2 エクストラ ライト。</span><span class="sxs-lookup"><span data-stu-id="0d385-301">2 Extra-light.</span></span>
-   <span data-ttu-id="0d385-302">3. ライト。</span><span class="sxs-lookup"><span data-stu-id="0d385-302">3 Light.</span></span>
-   <span data-ttu-id="0d385-303">4 標準。</span><span class="sxs-lookup"><span data-stu-id="0d385-303">4 Normal.</span></span>
-   <span data-ttu-id="0d385-304">5 中。</span><span class="sxs-lookup"><span data-stu-id="0d385-304">5 Medium.</span></span>
-   <span data-ttu-id="0d385-305">6 セミボールド。</span><span class="sxs-lookup"><span data-stu-id="0d385-305">6 Semibold.</span></span>
-   <span data-ttu-id="0d385-306">7 太字。</span><span class="sxs-lookup"><span data-stu-id="0d385-306">7 Bold.</span></span>
-   <span data-ttu-id="0d385-307">8 極太。</span><span class="sxs-lookup"><span data-stu-id="0d385-307">8 Extra-bold.</span></span>
-   <span data-ttu-id="0d385-308">9 ヘビー。</span><span class="sxs-lookup"><span data-stu-id="0d385-308">9 Heavy.</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="0d385-309">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="0d385-309">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="0d385-310">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="0d385-310">Parameters - bottomMargin</span></span>

<span data-ttu-id="0d385-311">値</span><span class="sxs-lookup"><span data-stu-id="0d385-311">value</span></span>  

<!-- -->

<span data-ttu-id="0d385-312">モード</span><span class="sxs-lookup"><span data-stu-id="0d385-312">mode</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="0d385-313">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="0d385-313">Return Value - bottomMargin</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="0d385-314">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="0d385-314">Method bottomMarginMode</span></span>

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="0d385-315">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="0d385-315">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="0d385-316">モード</span><span class="sxs-lookup"><span data-stu-id="0d385-316">mode</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="0d385-317">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="0d385-317">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="0d385-318">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="0d385-318">Method bottomMarginValue</span></span>

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="0d385-319">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="0d385-319">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="0d385-320">値</span><span class="sxs-lookup"><span data-stu-id="0d385-320">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="0d385-321">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="0d385-321">Return Value - bottomMarginValue</span></span>

## <a name="method-caption"></a><span data-ttu-id="0d385-322">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="0d385-322">Method caption</span></span>

<span data-ttu-id="0d385-323">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-323">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="0d385-324">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="0d385-324">Parameters - caption</span></span>

<span data-ttu-id="0d385-325">値</span><span class="sxs-lookup"><span data-stu-id="0d385-325">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="0d385-326">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="0d385-326">Return Value - caption</span></span>

<span data-ttu-id="0d385-327">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="0d385-327">The string that is used as the caption of the control.</span></span>

## <a name="method-characterset"></a><span data-ttu-id="0d385-328">メソッド characterSet</span><span class="sxs-lookup"><span data-stu-id="0d385-328">Method characterSet</span></span>

<span data-ttu-id="0d385-329">フォントの文字セットを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-329">Gets or sets the character set of the font.</span></span>

```xpp
public int characterSet([int value])
```

### <a name="parameters---characterset"></a><span data-ttu-id="0d385-330">パラメーター - characterSet</span><span class="sxs-lookup"><span data-stu-id="0d385-330">Parameters - characterSet</span></span>

<span data-ttu-id="0d385-331">値</span><span class="sxs-lookup"><span data-stu-id="0d385-331">value</span></span>  

### <a name="return-value---characterset"></a><span data-ttu-id="0d385-332">戻り値 - characterSet</span><span class="sxs-lookup"><span data-stu-id="0d385-332">Return Value - characterSet</span></span>

<span data-ttu-id="0d385-333">フォントの文字セット示す整数値。</span><span class="sxs-lookup"><span data-stu-id="0d385-333">An integer value that indicates the character set of the font.</span></span>

### <a name="remarks---characterset"></a><span data-ttu-id="0d385-334">備考 - characterSet</span><span class="sxs-lookup"><span data-stu-id="0d385-334">Remarks - characterSet</span></span>

<span data-ttu-id="0d385-335">返される整数の値は、次のテーブルに従って文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="0d385-335">The values for the integer that is returned indicate the character set according to the following table:</span></span>

| <span data-ttu-id="0d385-336">値です。</span><span class="sxs-lookup"><span data-stu-id="0d385-336">Value.</span></span> | <span data-ttu-id="0d385-337">説明。</span><span class="sxs-lookup"><span data-stu-id="0d385-337">Description.</span></span>         |
|--------|----------------------|
| <span data-ttu-id="0d385-338">0</span><span class="sxs-lookup"><span data-stu-id="0d385-338">0</span></span>      | <span data-ttu-id="0d385-339">ANSI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="0d385-339">ANSI\_CHARSET</span></span>        |
| <span data-ttu-id="0d385-340">1</span><span class="sxs-lookup"><span data-stu-id="0d385-340">1</span></span>      | <span data-ttu-id="0d385-341">DEFAULT\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="0d385-341">DEFAULT\_CHARSET</span></span>     |
| <span data-ttu-id="0d385-342">2</span><span class="sxs-lookup"><span data-stu-id="0d385-342">2</span></span>      | <span data-ttu-id="0d385-343">SYMBOL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="0d385-343">SYMBOL\_CHARSET</span></span>      |
| <span data-ttu-id="0d385-344">77</span><span class="sxs-lookup"><span data-stu-id="0d385-344">77</span></span>     | <span data-ttu-id="0d385-345">MAC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="0d385-345">MAC\_CHARSET</span></span>         |
| <span data-ttu-id="0d385-346">128</span><span class="sxs-lookup"><span data-stu-id="0d385-346">128</span></span>    | <span data-ttu-id="0d385-347">SHIFTJIS\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="0d385-347">SHIFTJIS\_CHARSET</span></span>    |
| <span data-ttu-id="0d385-348">129</span><span class="sxs-lookup"><span data-stu-id="0d385-348">129</span></span>    | <span data-ttu-id="0d385-349">HANGUL\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="0d385-349">HANGUL\_CHARSET</span></span>      |
| <span data-ttu-id="0d385-350">134</span><span class="sxs-lookup"><span data-stu-id="0d385-350">134</span></span>    | <span data-ttu-id="0d385-351">GB2312\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="0d385-351">GB2312\_CHARSET</span></span>      |
| <span data-ttu-id="0d385-352">136</span><span class="sxs-lookup"><span data-stu-id="0d385-352">136</span></span>    | <span data-ttu-id="0d385-353">CHINESEBIG5\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="0d385-353">CHINESEBIG5\_CHARSET</span></span> |
| <span data-ttu-id="0d385-354">161</span><span class="sxs-lookup"><span data-stu-id="0d385-354">161</span></span>    | <span data-ttu-id="0d385-355">GREEK\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="0d385-355">GREEK\_CHARSET</span></span>       |
| <span data-ttu-id="0d385-356">162</span><span class="sxs-lookup"><span data-stu-id="0d385-356">162</span></span>    | <span data-ttu-id="0d385-357">TURKISH\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="0d385-357">TURKISH\_CHARSET</span></span>     |
| <span data-ttu-id="0d385-358">163</span><span class="sxs-lookup"><span data-stu-id="0d385-358">163</span></span>    | <span data-ttu-id="0d385-359">VIETNAMESE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="0d385-359">VIETNAMESE\_CHARSET</span></span>  |
| <span data-ttu-id="0d385-360">186</span><span class="sxs-lookup"><span data-stu-id="0d385-360">186</span></span>    | <span data-ttu-id="0d385-361">BALTIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="0d385-361">BALTIC\_CHARSET</span></span>      |
| <span data-ttu-id="0d385-362">204</span><span class="sxs-lookup"><span data-stu-id="0d385-362">204</span></span>    | <span data-ttu-id="0d385-363">RUSSIAN\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="0d385-363">RUSSIAN\_CHARSET</span></span>     |
| <span data-ttu-id="0d385-364">238</span><span class="sxs-lookup"><span data-stu-id="0d385-364">238</span></span>    | <span data-ttu-id="0d385-365">EASTEUROPE\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="0d385-365">EASTEUROPE\_CHARSET</span></span>  |
| <span data-ttu-id="0d385-366">255</span><span class="sxs-lookup"><span data-stu-id="0d385-366">255</span></span>    | <span data-ttu-id="0d385-367">OEM\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="0d385-367">OEM\_CHARSET</span></span>         |

<span data-ttu-id="0d385-368">次のテーブルの値は、韓国語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="0d385-368">The value in the following table is for the Korean language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="0d385-369">値です。</span><span class="sxs-lookup"><span data-stu-id="0d385-369">Value.</span></span> | <span data-ttu-id="0d385-370">説明。</span><span class="sxs-lookup"><span data-stu-id="0d385-370">Description.</span></span>   |
|--------|----------------|
| <span data-ttu-id="0d385-371">130</span><span class="sxs-lookup"><span data-stu-id="0d385-371">130</span></span>    | <span data-ttu-id="0d385-372">JOHAB\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="0d385-372">JOHAB\_CHARSET</span></span> |

<span data-ttu-id="0d385-373">次のテーブルの値は、中東言語版用 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="0d385-373">The values in the following table are for the Middle East language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="0d385-374">値です。</span><span class="sxs-lookup"><span data-stu-id="0d385-374">Value.</span></span> | <span data-ttu-id="0d385-375">説明。</span><span class="sxs-lookup"><span data-stu-id="0d385-375">Description.</span></span>    |
|--------|-----------------|
| <span data-ttu-id="0d385-376">177</span><span class="sxs-lookup"><span data-stu-id="0d385-376">177</span></span>    | <span data-ttu-id="0d385-377">HEBREW\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="0d385-377">HEBREW\_CHARSET</span></span> |
| <span data-ttu-id="0d385-378">178</span><span class="sxs-lookup"><span data-stu-id="0d385-378">178</span></span>    | <span data-ttu-id="0d385-379">ARABIC\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="0d385-379">ARABIC\_CHARSET</span></span> |

<span data-ttu-id="0d385-380">次のテーブルの値は、タイ語版 Microsoft Windows の値です。</span><span class="sxs-lookup"><span data-stu-id="0d385-380">The value in the following table is for the Thai language edition of Microsoft Windows.</span></span>

| <span data-ttu-id="0d385-381">値です。</span><span class="sxs-lookup"><span data-stu-id="0d385-381">Value.</span></span> | <span data-ttu-id="0d385-382">説明。</span><span class="sxs-lookup"><span data-stu-id="0d385-382">Description.</span></span>  |
|--------|---------------|
| <span data-ttu-id="0d385-383">222</span><span class="sxs-lookup"><span data-stu-id="0d385-383">222</span></span>    | <span data-ttu-id="0d385-384">THAI\_CHARSET</span><span class="sxs-lookup"><span data-stu-id="0d385-384">THAI\_CHARSET</span></span> |

<span data-ttu-id="0d385-385">既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="0d385-385">The default character set is set to a value based on the current system locale.</span></span> <span data-ttu-id="0d385-386">たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。</span><span class="sxs-lookup"><span data-stu-id="0d385-386">For example, when the system locale is English (United States), it is set as ANSI\_CHARSET.</span></span> <span data-ttu-id="0d385-387">詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d385-387">For more information, see the LOGFONT structure on the [MSDN website](https://go.microsoft.com/fwlink/?LinkID=85972).</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="0d385-388">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="0d385-388">Method colorScheme</span></span>

<span data-ttu-id="0d385-389">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-389">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="0d385-390">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="0d385-390">Parameters - colorScheme</span></span>

<span data-ttu-id="0d385-391">値</span><span class="sxs-lookup"><span data-stu-id="0d385-391">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="0d385-392">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="0d385-392">Return Value - colorScheme</span></span>

<span data-ttu-id="0d385-393">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="0d385-393">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="0d385-394">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="0d385-394">Remarks - colorScheme</span></span>

<span data-ttu-id="0d385-395">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="0d385-395">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="0d385-396">値です。</span><span class="sxs-lookup"><span data-stu-id="0d385-396">Value.</span></span> | <span data-ttu-id="0d385-397">スタイル。</span><span class="sxs-lookup"><span data-stu-id="0d385-397">Style.</span></span>                         |
|--------|--------------------------------|
| <span data-ttu-id="0d385-398">0</span><span class="sxs-lookup"><span data-stu-id="0d385-398">0</span></span>      | <span data-ttu-id="0d385-399">既定。</span><span class="sxs-lookup"><span data-stu-id="0d385-399">Default.</span></span>                       |
| <span data-ttu-id="0d385-400">1</span><span class="sxs-lookup"><span data-stu-id="0d385-400">1</span></span>      | <span data-ttu-id="0d385-401">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="0d385-401">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="0d385-402">2</span><span class="sxs-lookup"><span data-stu-id="0d385-402">2</span></span>      | <span data-ttu-id="0d385-403">真の配色。</span><span class="sxs-lookup"><span data-stu-id="0d385-403">The true-color scheme.</span></span>         |

## <a name="method-columns"></a><span data-ttu-id="0d385-404">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="0d385-404">Method columns</span></span>

```xpp
public int columns([int value], [ColumnsMode mode])
```

### <a name="parameters---columns"></a><span data-ttu-id="0d385-405">パラメーター - columns</span><span class="sxs-lookup"><span data-stu-id="0d385-405">Parameters - columns</span></span>

<span data-ttu-id="0d385-406">値</span><span class="sxs-lookup"><span data-stu-id="0d385-406">value</span></span>  

<!-- -->

<span data-ttu-id="0d385-407">モード</span><span class="sxs-lookup"><span data-stu-id="0d385-407">mode</span></span>  

### <a name="return-value---columns"></a><span data-ttu-id="0d385-408">戻り値 - columns</span><span class="sxs-lookup"><span data-stu-id="0d385-408">Return Value - columns</span></span>

## <a name="method-columnsmode"></a><span data-ttu-id="0d385-409">メソッド columnsMode</span><span class="sxs-lookup"><span data-stu-id="0d385-409">Method columnsMode</span></span>

```xpp
public ColumnsMode columnsMode([ColumnsMode mode])
```

### <a name="parameters---columnsmode"></a><span data-ttu-id="0d385-410">パラメーター - columnsMode</span><span class="sxs-lookup"><span data-stu-id="0d385-410">Parameters - columnsMode</span></span>

<span data-ttu-id="0d385-411">モード</span><span class="sxs-lookup"><span data-stu-id="0d385-411">mode</span></span>  

### <a name="return-value---columnsmode"></a><span data-ttu-id="0d385-412">戻り値 - columnsMode</span><span class="sxs-lookup"><span data-stu-id="0d385-412">Return Value - columnsMode</span></span>

## <a name="method-columnspace"></a><span data-ttu-id="0d385-413">メソッド columnspace</span><span class="sxs-lookup"><span data-stu-id="0d385-413">Method columnspace</span></span>

```xpp
public int columnspace([int value], [AutoMode mode])
```

### <a name="parameters---columnspace"></a><span data-ttu-id="0d385-414">パラメーター - columnspace</span><span class="sxs-lookup"><span data-stu-id="0d385-414">Parameters - columnspace</span></span>

<span data-ttu-id="0d385-415">値</span><span class="sxs-lookup"><span data-stu-id="0d385-415">value</span></span>  

<!-- -->

<span data-ttu-id="0d385-416">モード</span><span class="sxs-lookup"><span data-stu-id="0d385-416">mode</span></span>  

### <a name="return-value---columnspace"></a><span data-ttu-id="0d385-417">戻り値 - columnspace</span><span class="sxs-lookup"><span data-stu-id="0d385-417">Return Value - columnspace</span></span>

## <a name="method-columnspacemode"></a><span data-ttu-id="0d385-418">メソッド columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="0d385-418">Method columnspaceMode</span></span>

```xpp
public AutoMode columnspaceMode([AutoMode mode])
```

### <a name="parameters---columnspacemode"></a><span data-ttu-id="0d385-419">パラメーター - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="0d385-419">Parameters - columnspaceMode</span></span>

<span data-ttu-id="0d385-420">モード</span><span class="sxs-lookup"><span data-stu-id="0d385-420">mode</span></span>  

### <a name="return-value---columnspacemode"></a><span data-ttu-id="0d385-421">戻り値 - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="0d385-421">Return Value - columnspaceMode</span></span>

## <a name="method-columnspacevalue"></a><span data-ttu-id="0d385-422">メソッド columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="0d385-422">Method columnspaceValue</span></span>

```xpp
public int columnspaceValue([int value])
```

### <a name="parameters---columnspacevalue"></a><span data-ttu-id="0d385-423">パラメーター - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="0d385-423">Parameters - columnspaceValue</span></span>

<span data-ttu-id="0d385-424">値</span><span class="sxs-lookup"><span data-stu-id="0d385-424">value</span></span>  

### <a name="return-value---columnspacevalue"></a><span data-ttu-id="0d385-425">戻り値 - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="0d385-425">Return Value - columnspaceValue</span></span>

## <a name="method-columnsvalue"></a><span data-ttu-id="0d385-426">メソッド columnsValue</span><span class="sxs-lookup"><span data-stu-id="0d385-426">Method columnsValue</span></span>

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a><span data-ttu-id="0d385-427">パラメーター - columnsValue</span><span class="sxs-lookup"><span data-stu-id="0d385-427">Parameters - columnsValue</span></span>

<span data-ttu-id="0d385-428">値</span><span class="sxs-lookup"><span data-stu-id="0d385-428">value</span></span>  

### <a name="return-value---columnsvalue"></a><span data-ttu-id="0d385-429">戻り値 - columnsValue</span><span class="sxs-lookup"><span data-stu-id="0d385-429">Return Value - columnsValue</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="0d385-430">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="0d385-430">Method configurationKey</span></span>

<span data-ttu-id="0d385-431">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-431">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="0d385-432">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="0d385-432">Parameters - configurationKey</span></span>

<span data-ttu-id="0d385-433">値</span><span class="sxs-lookup"><span data-stu-id="0d385-433">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="0d385-434">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="0d385-434">Return Value - configurationKey</span></span>

<span data-ttu-id="0d385-435">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="0d385-435">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="0d385-436">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="0d385-436">Remarks - configurationKey</span></span>

<span data-ttu-id="0d385-437">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0d385-437">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="0d385-438">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="0d385-438">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="0d385-439">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="0d385-439">Method containerId</span></span>

<span data-ttu-id="0d385-440">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="0d385-440">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="0d385-441">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="0d385-441">Return Value - containerId</span></span>

<span data-ttu-id="0d385-442">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="0d385-442">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="0d385-443">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="0d385-443">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="0d385-444">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="0d385-444">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="0d385-445">値</span><span class="sxs-lookup"><span data-stu-id="0d385-445">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="0d385-446">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="0d385-446">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="0d385-447">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="0d385-447">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="0d385-448">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="0d385-448">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="0d385-449">値</span><span class="sxs-lookup"><span data-stu-id="0d385-449">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="0d385-450">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="0d385-450">Return Value - countryRegionContextField</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="0d385-451">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="0d385-451">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="0d385-452">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="0d385-452">Parameters - dataRelationPath</span></span>

<span data-ttu-id="0d385-453">値</span><span class="sxs-lookup"><span data-stu-id="0d385-453">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="0d385-454">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="0d385-454">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="0d385-455">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="0d385-455">Method dataSource</span></span>

<span data-ttu-id="0d385-456">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-456">Gets or sets a data source to be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="0d385-457">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="0d385-457">Parameters - dataSource</span></span>

<span data-ttu-id="0d385-458">値</span><span class="sxs-lookup"><span data-stu-id="0d385-458">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="0d385-459">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="0d385-459">Return Value - dataSource</span></span>

<span data-ttu-id="0d385-460">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="0d385-460">The identifier of the data source to be used.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="0d385-461">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="0d385-461">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="0d385-462">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="0d385-462">Parameters - displayTarget</span></span>

<span data-ttu-id="0d385-463">値</span><span class="sxs-lookup"><span data-stu-id="0d385-463">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="0d385-464">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="0d385-464">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="0d385-465">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="0d385-465">Method dragDrop</span></span>

<span data-ttu-id="0d385-466">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-466">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="0d385-467">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="0d385-467">Parameters - dragDrop</span></span>

<span data-ttu-id="0d385-468">値</span><span class="sxs-lookup"><span data-stu-id="0d385-468">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="0d385-469">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="0d385-469">Return Value - dragDrop</span></span>

<span data-ttu-id="0d385-470">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="0d385-470">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="0d385-471">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="0d385-471">Method enabled</span></span>

<span data-ttu-id="0d385-472">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-472">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="0d385-473">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="0d385-473">Parameters - enabled</span></span>

<span data-ttu-id="0d385-474">値</span><span class="sxs-lookup"><span data-stu-id="0d385-474">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="0d385-475">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="0d385-475">Return Value - enabled</span></span>

<span data-ttu-id="0d385-476">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0d385-476">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="0d385-477">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="0d385-477">Remarks - enabled</span></span>

<span data-ttu-id="0d385-478">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="0d385-478">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="0d385-479">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="0d385-479">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="0d385-480">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="0d385-480">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-font"></a><span data-ttu-id="0d385-481">メソッド font</span><span class="sxs-lookup"><span data-stu-id="0d385-481">Method font</span></span>

<span data-ttu-id="0d385-482">使用するコントロールのフォントの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-482">Gets or sets the name of the font for the control to use.</span></span>

```xpp
public str font([str value])
```

### <a name="parameters---font"></a><span data-ttu-id="0d385-483">パラメーター - font</span><span class="sxs-lookup"><span data-stu-id="0d385-483">Parameters - font</span></span>

<span data-ttu-id="0d385-484">値</span><span class="sxs-lookup"><span data-stu-id="0d385-484">value</span></span>  

### <a name="return-value---font"></a><span data-ttu-id="0d385-485">戻り値 - font</span><span class="sxs-lookup"><span data-stu-id="0d385-485">Return Value - font</span></span>

<span data-ttu-id="0d385-486">Tahoma や Verdana など、使用するフォントの名前。</span><span class="sxs-lookup"><span data-stu-id="0d385-486">The name of the font to use, such as Tahoma or Verdana.</span></span>

## <a name="method-fontsize"></a><span data-ttu-id="0d385-487">メソッド fontSize</span><span class="sxs-lookup"><span data-stu-id="0d385-487">Method fontSize</span></span>

<span data-ttu-id="0d385-488">使用するコントロールのフォントのサイズを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-488">Gets or sets the size of the font for the control to use.</span></span>

```xpp
public int fontSize([int value])
```

### <a name="parameters---fontsize"></a><span data-ttu-id="0d385-489">パラメーター - fontSize</span><span class="sxs-lookup"><span data-stu-id="0d385-489">Parameters - fontSize</span></span>

<span data-ttu-id="0d385-490">値</span><span class="sxs-lookup"><span data-stu-id="0d385-490">value</span></span>  

### <a name="return-value---fontsize"></a><span data-ttu-id="0d385-491">戻り値 - fontSize</span><span class="sxs-lookup"><span data-stu-id="0d385-491">Return Value - fontSize</span></span>

<span data-ttu-id="0d385-492">ポイント単位のフォントの高さ。</span><span class="sxs-lookup"><span data-stu-id="0d385-492">The height of the font in points.</span></span>

## <a name="method-frameposition"></a><span data-ttu-id="0d385-493">メソッド framePosition</span><span class="sxs-lookup"><span data-stu-id="0d385-493">Method framePosition</span></span>

```xpp
public int framePosition([int value])
```

### <a name="parameters---frameposition"></a><span data-ttu-id="0d385-494">パラメーター - framePosition</span><span class="sxs-lookup"><span data-stu-id="0d385-494">Parameters - framePosition</span></span>

<span data-ttu-id="0d385-495">値</span><span class="sxs-lookup"><span data-stu-id="0d385-495">value</span></span>  

### <a name="return-value---frameposition"></a><span data-ttu-id="0d385-496">戻り値 - framePosition</span><span class="sxs-lookup"><span data-stu-id="0d385-496">Return Value - framePosition</span></span>

## <a name="method-frametype"></a><span data-ttu-id="0d385-497">メソッド frameType</span><span class="sxs-lookup"><span data-stu-id="0d385-497">Method frameType</span></span>

```xpp
public int frameType([int value])
```

### <a name="parameters---frametype"></a><span data-ttu-id="0d385-498">パラメーター - frameType</span><span class="sxs-lookup"><span data-stu-id="0d385-498">Parameters - frameType</span></span>

<span data-ttu-id="0d385-499">値</span><span class="sxs-lookup"><span data-stu-id="0d385-499">value</span></span>  

### <a name="return-value---frametype"></a><span data-ttu-id="0d385-500">戻り値 - frameType</span><span class="sxs-lookup"><span data-stu-id="0d385-500">Return Value - frameType</span></span>

## <a name="method-height"></a><span data-ttu-id="0d385-501">メソッド height</span><span class="sxs-lookup"><span data-stu-id="0d385-501">Method height</span></span>

<span data-ttu-id="0d385-502">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-502">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="0d385-503">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="0d385-503">Parameters - height</span></span>

<span data-ttu-id="0d385-504">値</span><span class="sxs-lookup"><span data-stu-id="0d385-504">value</span></span>  

<!-- -->

<span data-ttu-id="0d385-505">モード</span><span class="sxs-lookup"><span data-stu-id="0d385-505">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="0d385-506">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="0d385-506">Return Value - height</span></span>

<span data-ttu-id="0d385-507">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="0d385-507">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="0d385-508">備考 - height</span><span class="sxs-lookup"><span data-stu-id="0d385-508">Remarks - height</span></span>

<span data-ttu-id="0d385-509">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0d385-509">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="0d385-510">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="0d385-510">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="0d385-511">モード。</span><span class="sxs-lookup"><span data-stu-id="0d385-511">Mode.</span></span>            | <span data-ttu-id="0d385-512">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="0d385-512">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d385-513">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="0d385-513">-1 Exact.</span></span>        | <span data-ttu-id="0d385-514">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0d385-514">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="0d385-515">0 自動。</span><span class="sxs-lookup"><span data-stu-id="0d385-515">0 Auto.</span></span>          | <span data-ttu-id="0d385-516">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="0d385-516">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="0d385-517">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="0d385-517">1 Column height.</span></span> | <span data-ttu-id="0d385-518">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="0d385-518">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="0d385-519">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="0d385-519">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="0d385-520">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="0d385-520">Method heightMode</span></span>

<span data-ttu-id="0d385-521">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-521">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="0d385-522">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="0d385-522">Parameters - heightMode</span></span>

<span data-ttu-id="0d385-523">値</span><span class="sxs-lookup"><span data-stu-id="0d385-523">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="0d385-524">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="0d385-524">Return Value - heightMode</span></span>

<span data-ttu-id="0d385-525">計算モード。</span><span class="sxs-lookup"><span data-stu-id="0d385-525">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="0d385-526">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="0d385-526">Remarks - heightMode</span></span>

<span data-ttu-id="0d385-527">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="0d385-527">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="0d385-528">モード。</span><span class="sxs-lookup"><span data-stu-id="0d385-528">Mode.</span></span>          | <span data-ttu-id="0d385-529">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="0d385-529">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d385-530">正確。</span><span class="sxs-lookup"><span data-stu-id="0d385-530">Exact.</span></span>         | <span data-ttu-id="0d385-531">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0d385-531">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="0d385-532">自動。</span><span class="sxs-lookup"><span data-stu-id="0d385-532">Auto.</span></span>          | <span data-ttu-id="0d385-533">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="0d385-533">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="0d385-534">列の高さ</span><span class="sxs-lookup"><span data-stu-id="0d385-534">Column height.</span></span> | <span data-ttu-id="0d385-535">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="0d385-535">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="0d385-536">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="0d385-536">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="0d385-537">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="0d385-537">Method heightValue</span></span>

<span data-ttu-id="0d385-538">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-538">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="0d385-539">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="0d385-539">Parameters - heightValue</span></span>

<span data-ttu-id="0d385-540">値</span><span class="sxs-lookup"><span data-stu-id="0d385-540">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="0d385-541">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="0d385-541">Return Value - heightValue</span></span>

<span data-ttu-id="0d385-542">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="0d385-542">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="0d385-543">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="0d385-543">Remarks - heightValue</span></span>

<span data-ttu-id="0d385-544">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="0d385-544">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="0d385-545">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="0d385-545">Method helpText</span></span>

<span data-ttu-id="0d385-546">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-546">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="0d385-547">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="0d385-547">Parameters - helpText</span></span>

<span data-ttu-id="0d385-548">値</span><span class="sxs-lookup"><span data-stu-id="0d385-548">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="0d385-549">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="0d385-549">Return Value - helpText</span></span>

<span data-ttu-id="0d385-550">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="0d385-550">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="0d385-551">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="0d385-551">Remarks - helpText</span></span>

<span data-ttu-id="0d385-552">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-552">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="0d385-553">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="0d385-553">The help text must not exceed 250 characters.</span></span>

## <a name="method-hideifempty"></a><span data-ttu-id="0d385-554">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="0d385-554">Method hideIfEmpty</span></span>

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a><span data-ttu-id="0d385-555">パラメーター - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="0d385-555">Parameters - hideIfEmpty</span></span>

<span data-ttu-id="0d385-556">値</span><span class="sxs-lookup"><span data-stu-id="0d385-556">value</span></span>  

### <a name="return-value---hideifempty"></a><span data-ttu-id="0d385-557">戻り値 - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="0d385-557">Return Value - hideIfEmpty</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="0d385-558">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="0d385-558">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="0d385-559">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="0d385-559">Parameters - hierarchyParent</span></span>

<span data-ttu-id="0d385-560">値</span><span class="sxs-lookup"><span data-stu-id="0d385-560">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="0d385-561">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="0d385-561">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="0d385-562">メソッド id</span><span class="sxs-lookup"><span data-stu-id="0d385-562">Method id</span></span>

<span data-ttu-id="0d385-563">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="0d385-563">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="0d385-564">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="0d385-564">Return Value - id</span></span>

<span data-ttu-id="0d385-565">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="0d385-565">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="0d385-566">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="0d385-566">Method isContainer</span></span>

<span data-ttu-id="0d385-567">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0d385-567">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="0d385-568">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="0d385-568">Return Value - isContainer</span></span>

<span data-ttu-id="0d385-569">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0d385-569">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-italic"></a><span data-ttu-id="0d385-570">メソッド italic</span><span class="sxs-lookup"><span data-stu-id="0d385-570">Method italic</span></span>

```xpp
public boolean italic([boolean value])
```

### <a name="parameters---italic"></a><span data-ttu-id="0d385-571">パラメーター - italic</span><span class="sxs-lookup"><span data-stu-id="0d385-571">Parameters - italic</span></span>

<span data-ttu-id="0d385-572">値</span><span class="sxs-lookup"><span data-stu-id="0d385-572">value</span></span>  

### <a name="return-value---italic"></a><span data-ttu-id="0d385-573">戻り値 - italic</span><span class="sxs-lookup"><span data-stu-id="0d385-573">Return Value - italic</span></span>

## <a name="method-keytip"></a><span data-ttu-id="0d385-574">メソッド keyTip</span><span class="sxs-lookup"><span data-stu-id="0d385-574">Method keyTip</span></span>

```xpp
public str keyTip([str value])
```

### <a name="parameters---keytip"></a><span data-ttu-id="0d385-575">パラメーター - keyTip</span><span class="sxs-lookup"><span data-stu-id="0d385-575">Parameters - keyTip</span></span>

<span data-ttu-id="0d385-576">値</span><span class="sxs-lookup"><span data-stu-id="0d385-576">value</span></span>  

### <a name="return-value---keytip"></a><span data-ttu-id="0d385-577">戻り値 - keyTip</span><span class="sxs-lookup"><span data-stu-id="0d385-577">Return Value - keyTip</span></span>

## <a name="method-left"></a><span data-ttu-id="0d385-578">メソッド left</span><span class="sxs-lookup"><span data-stu-id="0d385-578">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="0d385-579">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="0d385-579">Parameters - left</span></span>

<span data-ttu-id="0d385-580">値</span><span class="sxs-lookup"><span data-stu-id="0d385-580">value</span></span>  

<!-- -->

<span data-ttu-id="0d385-581">モード</span><span class="sxs-lookup"><span data-stu-id="0d385-581">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="0d385-582">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="0d385-582">Return Value - left</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="0d385-583">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="0d385-583">Method leftMargin</span></span>

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="0d385-584">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="0d385-584">Parameters - leftMargin</span></span>

<span data-ttu-id="0d385-585">値</span><span class="sxs-lookup"><span data-stu-id="0d385-585">value</span></span>  

<!-- -->

<span data-ttu-id="0d385-586">モード</span><span class="sxs-lookup"><span data-stu-id="0d385-586">mode</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="0d385-587">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="0d385-587">Return Value - leftMargin</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="0d385-588">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="0d385-588">Method leftMarginMode</span></span>

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="0d385-589">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="0d385-589">Parameters - leftMarginMode</span></span>

<span data-ttu-id="0d385-590">モード</span><span class="sxs-lookup"><span data-stu-id="0d385-590">mode</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="0d385-591">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="0d385-591">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="0d385-592">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="0d385-592">Method leftMarginValue</span></span>

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="0d385-593">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="0d385-593">Parameters - leftMarginValue</span></span>

<span data-ttu-id="0d385-594">値</span><span class="sxs-lookup"><span data-stu-id="0d385-594">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="0d385-595">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="0d385-595">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="0d385-596">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="0d385-596">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="0d385-597">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="0d385-597">Parameters - leftMode</span></span>

<span data-ttu-id="0d385-598">値</span><span class="sxs-lookup"><span data-stu-id="0d385-598">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="0d385-599">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="0d385-599">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="0d385-600">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="0d385-600">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="0d385-601">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="0d385-601">Parameters - leftValue</span></span>

<span data-ttu-id="0d385-602">値</span><span class="sxs-lookup"><span data-stu-id="0d385-602">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="0d385-603">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="0d385-603">Return Value - leftValue</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="0d385-604">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="0d385-604">Method moveControl</span></span>

<span data-ttu-id="0d385-605">コントロールに指定されたコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="0d385-605">Moves a specified control to the control.</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterControlId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="0d385-606">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="0d385-606">Parameters - moveControl</span></span>

<span data-ttu-id="0d385-607">controlId</span><span class="sxs-lookup"><span data-stu-id="0d385-607">controlId</span></span>  

<!-- -->

<span data-ttu-id="0d385-608">insertAfterControlId</span><span class="sxs-lookup"><span data-stu-id="0d385-608">insertAfterControlId</span></span>  

### <a name="return-value---movecontrol"></a><span data-ttu-id="0d385-609">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="0d385-609">Return Value - moveControl</span></span>

<span data-ttu-id="0d385-610">コントロールが正常に移動した場合は 1、それ以外の場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="0d385-610">1 if the control was moved successfully; otherwise, 0.</span></span>

### <a name="remarks---movecontrol"></a><span data-ttu-id="0d385-611">備考 - moveControl</span><span class="sxs-lookup"><span data-stu-id="0d385-611">Remarks - moveControl</span></span>

<span data-ttu-id="0d385-612">一般に、指定したコントロールをコントロールに含めることができ、現在のコンテナーから移動できる場合、このメソッドは成功します。</span><span class="sxs-lookup"><span data-stu-id="0d385-612">In general, if the specified control can be contained in the control and can be moved from the container that it is currently in, this method should succeed.</span></span> <span data-ttu-id="0d385-613">ただし、場合によっては、参照グループ コントロールのインスタンス コントロールなど、コントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="0d385-613">However, in some cases, such as for the reference group control instance, controls cannot be moved.</span></span>

## <a name="method-name"></a><span data-ttu-id="0d385-614">メソッド名</span><span class="sxs-lookup"><span data-stu-id="0d385-614">Method name</span></span>

<span data-ttu-id="0d385-615">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-615">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="0d385-616">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="0d385-616">Parameters - name</span></span>

<span data-ttu-id="0d385-617">値</span><span class="sxs-lookup"><span data-stu-id="0d385-617">value</span></span>  
<span data-ttu-id="0d385-618">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="0d385-618">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="0d385-619">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="0d385-619">Return Value - name</span></span>

<span data-ttu-id="0d385-620">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="0d385-620">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="0d385-621">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="0d385-621">Remarks - name</span></span>

<span data-ttu-id="0d385-622">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d385-622">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="0d385-623">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d385-623">It must start with a letter.</span></span>
-   <span data-ttu-id="0d385-624">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="0d385-624">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="0d385-625">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="0d385-625">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="0d385-626">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="0d385-626">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="0d385-627">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="0d385-627">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="0d385-628">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="0d385-628">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="0d385-629">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="0d385-629">Parameters - neededPermission</span></span>

<span data-ttu-id="0d385-630">値</span><span class="sxs-lookup"><span data-stu-id="0d385-630">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="0d385-631">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="0d385-631">Return Value - neededPermission</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="0d385-632">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="0d385-632">Method rightMargin</span></span>

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="0d385-633">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="0d385-633">Parameters - rightMargin</span></span>

<span data-ttu-id="0d385-634">値</span><span class="sxs-lookup"><span data-stu-id="0d385-634">value</span></span>  

<!-- -->

<span data-ttu-id="0d385-635">モード</span><span class="sxs-lookup"><span data-stu-id="0d385-635">mode</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="0d385-636">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="0d385-636">Return Value - rightMargin</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="0d385-637">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="0d385-637">Method rightMarginMode</span></span>

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="0d385-638">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="0d385-638">Parameters - rightMarginMode</span></span>

<span data-ttu-id="0d385-639">モード</span><span class="sxs-lookup"><span data-stu-id="0d385-639">mode</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="0d385-640">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="0d385-640">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="0d385-641">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="0d385-641">Method rightMarginValue</span></span>

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="0d385-642">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="0d385-642">Parameters - rightMarginValue</span></span>

<span data-ttu-id="0d385-643">値</span><span class="sxs-lookup"><span data-stu-id="0d385-643">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="0d385-644">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="0d385-644">Return Value - rightMarginValue</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="0d385-645">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="0d385-645">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="0d385-646">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="0d385-646">Parameters - securityKey</span></span>

<span data-ttu-id="0d385-647">値</span><span class="sxs-lookup"><span data-stu-id="0d385-647">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="0d385-648">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="0d385-648">Return Value - securityKey</span></span>

## <a name="method-sizeheight"></a><span data-ttu-id="0d385-649">メソッド sizeHeight</span><span class="sxs-lookup"><span data-stu-id="0d385-649">Method sizeHeight</span></span>

```xpp
public boolean sizeHeight([boolean value])
```

### <a name="parameters---sizeheight"></a><span data-ttu-id="0d385-650">パラメーター - sizeHeight</span><span class="sxs-lookup"><span data-stu-id="0d385-650">Parameters - sizeHeight</span></span>

<span data-ttu-id="0d385-651">値</span><span class="sxs-lookup"><span data-stu-id="0d385-651">value</span></span>  

### <a name="return-value---sizeheight"></a><span data-ttu-id="0d385-652">戻り値 - sizeHeight</span><span class="sxs-lookup"><span data-stu-id="0d385-652">Return Value - sizeHeight</span></span>

## <a name="method-sizewidth"></a><span data-ttu-id="0d385-653">メソッド sizeWidth</span><span class="sxs-lookup"><span data-stu-id="0d385-653">Method sizeWidth</span></span>

```xpp
public boolean sizeWidth([boolean value])
```

### <a name="parameters---sizewidth"></a><span data-ttu-id="0d385-654">パラメーター - sizeWidth</span><span class="sxs-lookup"><span data-stu-id="0d385-654">Parameters - sizeWidth</span></span>

<span data-ttu-id="0d385-655">値</span><span class="sxs-lookup"><span data-stu-id="0d385-655">value</span></span>  

### <a name="return-value---sizewidth"></a><span data-ttu-id="0d385-656">戻り値 - sizeWidth</span><span class="sxs-lookup"><span data-stu-id="0d385-656">Return Value - sizeWidth</span></span>

## <a name="method-skip"></a><span data-ttu-id="0d385-657">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="0d385-657">Method skip</span></span>

<span data-ttu-id="0d385-658">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="0d385-658">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="0d385-659">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="0d385-659">Parameters - skip</span></span>

<span data-ttu-id="0d385-660">値</span><span class="sxs-lookup"><span data-stu-id="0d385-660">value</span></span>  
<span data-ttu-id="0d385-661">コントロールの skip プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="0d385-661">The value to assign to the skip property of the control.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="0d385-662">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="0d385-662">Return Value - skip</span></span>

<span data-ttu-id="0d385-663">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0d385-663">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-style"></a><span data-ttu-id="0d385-664">メソッド style</span><span class="sxs-lookup"><span data-stu-id="0d385-664">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="0d385-665">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="0d385-665">Parameters - style</span></span>

<span data-ttu-id="0d385-666">値</span><span class="sxs-lookup"><span data-stu-id="0d385-666">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="0d385-667">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="0d385-667">Return Value - style</span></span>

## <a name="method-top"></a><span data-ttu-id="0d385-668">メソッド top</span><span class="sxs-lookup"><span data-stu-id="0d385-668">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="0d385-669">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="0d385-669">Parameters - top</span></span>

<span data-ttu-id="0d385-670">値</span><span class="sxs-lookup"><span data-stu-id="0d385-670">value</span></span>  

<!-- -->

<span data-ttu-id="0d385-671">モード</span><span class="sxs-lookup"><span data-stu-id="0d385-671">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="0d385-672">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="0d385-672">Return Value - top</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="0d385-673">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="0d385-673">Method topMargin</span></span>

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="0d385-674">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="0d385-674">Parameters - topMargin</span></span>

<span data-ttu-id="0d385-675">値</span><span class="sxs-lookup"><span data-stu-id="0d385-675">value</span></span>  

<!-- -->

<span data-ttu-id="0d385-676">モード</span><span class="sxs-lookup"><span data-stu-id="0d385-676">mode</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="0d385-677">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="0d385-677">Return Value - topMargin</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="0d385-678">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="0d385-678">Method topMarginMode</span></span>

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="0d385-679">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="0d385-679">Parameters - topMarginMode</span></span>

<span data-ttu-id="0d385-680">モード</span><span class="sxs-lookup"><span data-stu-id="0d385-680">mode</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="0d385-681">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="0d385-681">Return Value - topMarginMode</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="0d385-682">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="0d385-682">Method topMarginValue</span></span>

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="0d385-683">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="0d385-683">Parameters - topMarginValue</span></span>

<span data-ttu-id="0d385-684">値</span><span class="sxs-lookup"><span data-stu-id="0d385-684">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="0d385-685">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="0d385-685">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="0d385-686">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="0d385-686">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="0d385-687">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="0d385-687">Parameters - topMode</span></span>

<span data-ttu-id="0d385-688">値</span><span class="sxs-lookup"><span data-stu-id="0d385-688">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="0d385-689">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="0d385-689">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="0d385-690">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="0d385-690">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="0d385-691">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="0d385-691">Parameters - topValue</span></span>

<span data-ttu-id="0d385-692">値</span><span class="sxs-lookup"><span data-stu-id="0d385-692">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="0d385-693">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="0d385-693">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="0d385-694">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="0d385-694">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="0d385-695">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="0d385-695">Parameters - type</span></span>

<span data-ttu-id="0d385-696">値</span><span class="sxs-lookup"><span data-stu-id="0d385-696">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="0d385-697">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="0d385-697">Return Value - type</span></span>

## <a name="method-underline"></a><span data-ttu-id="0d385-698">メソッド underline</span><span class="sxs-lookup"><span data-stu-id="0d385-698">Method underline</span></span>

<span data-ttu-id="0d385-699">コントロール内のテキストの下線プロパティを設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="0d385-699">Sets or returns the underline property for the text in the control.</span></span>

```xpp
public boolean underline([boolean value])
```

### <a name="parameters---underline"></a><span data-ttu-id="0d385-700">パラメーター - underline</span><span class="sxs-lookup"><span data-stu-id="0d385-700">Parameters - underline</span></span>

<span data-ttu-id="0d385-701">値</span><span class="sxs-lookup"><span data-stu-id="0d385-701">value</span></span>  
<span data-ttu-id="0d385-702">コントロールの underline プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="0d385-702">The value to assign to the underline property of the control.</span></span>

### <a name="return-value---underline"></a><span data-ttu-id="0d385-703">戻り値 - underline</span><span class="sxs-lookup"><span data-stu-id="0d385-703">Return Value - underline</span></span>

<span data-ttu-id="0d385-704">コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0d385-704">true if the text in the control is underlined; otherwise, false.</span></span>

## <a name="method-userdata"></a><span data-ttu-id="0d385-705">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="0d385-705">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="0d385-706">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="0d385-706">Parameters - userData</span></span>

<span data-ttu-id="0d385-707">値</span><span class="sxs-lookup"><span data-stu-id="0d385-707">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="0d385-708">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="0d385-708">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="0d385-709">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="0d385-709">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="0d385-710">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="0d385-710">Parameters - userDataItem</span></span>

<span data-ttu-id="0d385-711">値</span><span class="sxs-lookup"><span data-stu-id="0d385-711">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="0d385-712">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="0d385-712">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="0d385-713">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="0d385-713">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="0d385-714">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="0d385-714">Parameters - userDataItems</span></span>

<span data-ttu-id="0d385-715">値</span><span class="sxs-lookup"><span data-stu-id="0d385-715">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="0d385-716">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="0d385-716">Return Value - userDataItems</span></span>

## <a name="method-useuserlayout"></a><span data-ttu-id="0d385-717">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="0d385-717">Method useUserLayout</span></span>

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a><span data-ttu-id="0d385-718">パラメーター - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="0d385-718">Parameters - useUserLayout</span></span>

<span data-ttu-id="0d385-719">値</span><span class="sxs-lookup"><span data-stu-id="0d385-719">value</span></span>  

### <a name="return-value---useuserlayout"></a><span data-ttu-id="0d385-720">戻り値 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="0d385-720">Return Value - useUserLayout</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="0d385-721">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="0d385-721">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="0d385-722">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="0d385-722">Parameters - verticalSpacing</span></span>

<span data-ttu-id="0d385-723">値</span><span class="sxs-lookup"><span data-stu-id="0d385-723">value</span></span>  

<!-- -->

<span data-ttu-id="0d385-724">モード</span><span class="sxs-lookup"><span data-stu-id="0d385-724">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="0d385-725">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="0d385-725">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="0d385-726">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="0d385-726">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="0d385-727">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="0d385-727">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="0d385-728">モード</span><span class="sxs-lookup"><span data-stu-id="0d385-728">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="0d385-729">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="0d385-729">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="0d385-730">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="0d385-730">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="0d385-731">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="0d385-731">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="0d385-732">値</span><span class="sxs-lookup"><span data-stu-id="0d385-732">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="0d385-733">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="0d385-733">Return Value - verticalSpacingValue</span></span>

## <a name="method-visible"></a><span data-ttu-id="0d385-734">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="0d385-734">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="0d385-735">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="0d385-735">Parameters - visible</span></span>

<span data-ttu-id="0d385-736">値</span><span class="sxs-lookup"><span data-stu-id="0d385-736">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="0d385-737">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="0d385-737">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="0d385-738">メソッド width</span><span class="sxs-lookup"><span data-stu-id="0d385-738">Method width</span></span>

<span data-ttu-id="0d385-739">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-739">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="0d385-740">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="0d385-740">Parameters - width</span></span>

<span data-ttu-id="0d385-741">値</span><span class="sxs-lookup"><span data-stu-id="0d385-741">value</span></span>  

<!-- -->

<span data-ttu-id="0d385-742">モード</span><span class="sxs-lookup"><span data-stu-id="0d385-742">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="0d385-743">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="0d385-743">Return Value - width</span></span>

<span data-ttu-id="0d385-744">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="0d385-744">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="0d385-745">備考 - width</span><span class="sxs-lookup"><span data-stu-id="0d385-745">Remarks - width</span></span>

<span data-ttu-id="0d385-746">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0d385-746">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="0d385-747">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="0d385-747">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="0d385-748">モード。</span><span class="sxs-lookup"><span data-stu-id="0d385-748">Mode.</span></span>           | <span data-ttu-id="0d385-749">幅計算。</span><span class="sxs-lookup"><span data-stu-id="0d385-749">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d385-750">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="0d385-750">-1 Exact.</span></span>       | <span data-ttu-id="0d385-751">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="0d385-751">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="0d385-752">0 自動。</span><span class="sxs-lookup"><span data-stu-id="0d385-752">0 Auto.</span></span>         | <span data-ttu-id="0d385-753">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="0d385-753">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="0d385-754">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="0d385-754">1 Column width.</span></span> | <span data-ttu-id="0d385-755">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="0d385-755">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="0d385-756">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="0d385-756">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="0d385-757">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="0d385-757">Method widthMode</span></span>

<span data-ttu-id="0d385-758">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-758">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="0d385-759">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="0d385-759">Parameters - widthMode</span></span>

<span data-ttu-id="0d385-760">値</span><span class="sxs-lookup"><span data-stu-id="0d385-760">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="0d385-761">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="0d385-761">Return Value - widthMode</span></span>

<span data-ttu-id="0d385-762">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="0d385-762">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="0d385-763">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="0d385-763">Remarks - widthMode</span></span>

<span data-ttu-id="0d385-764">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="0d385-764">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="0d385-765">モード。</span><span class="sxs-lookup"><span data-stu-id="0d385-765">Mode.</span></span>         | <span data-ttu-id="0d385-766">幅計算。</span><span class="sxs-lookup"><span data-stu-id="0d385-766">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d385-767">正確。</span><span class="sxs-lookup"><span data-stu-id="0d385-767">Exact.</span></span>        | <span data-ttu-id="0d385-768">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="0d385-768">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="0d385-769">自動。</span><span class="sxs-lookup"><span data-stu-id="0d385-769">Auto.</span></span>         | <span data-ttu-id="0d385-770">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="0d385-770">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="0d385-771">列の幅。</span><span class="sxs-lookup"><span data-stu-id="0d385-771">Column width.</span></span> | <span data-ttu-id="0d385-772">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="0d385-772">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="0d385-773">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="0d385-773">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="0d385-774">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="0d385-774">Method widthValue</span></span>

<span data-ttu-id="0d385-775">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0d385-775">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="0d385-776">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="0d385-776">Parameters - widthValue</span></span>

<span data-ttu-id="0d385-777">値</span><span class="sxs-lookup"><span data-stu-id="0d385-777">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="0d385-778">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="0d385-778">Return Value - widthValue</span></span>

<span data-ttu-id="0d385-779">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="0d385-779">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="0d385-780">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="0d385-780">Remarks - widthValue</span></span>

<span data-ttu-id="0d385-781">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="0d385-781">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="0d385-782">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="0d385-782">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="0d385-783">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="0d385-783">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="0d385-784">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="0d385-784">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="0d385-785">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="0d385-785">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="0d385-786">overrideObject</span><span class="sxs-lookup"><span data-stu-id="0d385-786">overrideObject</span></span>  

