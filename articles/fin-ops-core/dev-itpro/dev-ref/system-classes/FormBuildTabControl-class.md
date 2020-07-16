---
title: FormBuildTabControl クラス
description: このトピックでは、FormBuildTabControl クラスについて説明します。
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
ms.openlocfilehash: 8257f15a0a4eddf9a89c0e563d10807906addbac
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502640"
---
# <a name="class-formbuildtabcontrol"></a><span data-ttu-id="f5b54-103">クラス FormBuildTabControl</span><span class="sxs-lookup"><span data-stu-id="f5b54-103">Class FormBuildTabControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildTabControl extends FormBuildControl
```

<span data-ttu-id="f5b54-104">FormBuildTabControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f5b54-104">The FormBuildTabControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5b54-105">備考</span><span class="sxs-lookup"><span data-stu-id="f5b54-105">Remarks</span></span>

<span data-ttu-id="f5b54-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="f5b54-107">例</span><span class="sxs-lookup"><span data-stu-id="f5b54-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="f5b54-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="f5b54-108">Methods</span></span>

| <span data-ttu-id="f5b54-109">方法</span><span class="sxs-lookup"><span data-stu-id="f5b54-109">Method</span></span>                                                                                                      | <span data-ttu-id="f5b54-110">説明</span><span class="sxs-lookup"><span data-stu-id="f5b54-110">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b54-111">public boolean alignChild(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-111">public boolean alignChild(\[boolean value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="f5b54-112">public boolean alignChildren(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-112">public boolean alignChildren(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="f5b54-113">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-113">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="f5b54-114">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-114">Determines whether to align the control.</span></span>                                                                                                |
| <span data-ttu-id="f5b54-115">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-115">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="f5b54-116">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-116">Determines whether the user can change the contents of the control.</span></span>                                                                     |
| <span data-ttu-id="f5b54-117">public int allowUserSetup(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-117">public int allowUserSetup(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="f5b54-118">public int arrangeGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-118">public int arrangeGuide(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="f5b54-119">public int arrangeMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-119">public int arrangeMethod(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="f5b54-120">public int arrangeWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-120">public int arrangeWhen(\[int value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="f5b54-121">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-121">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="f5b54-122">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-122">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                      |
| <span data-ttu-id="f5b54-123">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-123">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="f5b54-124">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-124">Gets or sets the background color of the control.</span></span>                                                                                       |
| <span data-ttu-id="f5b54-125">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-125">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="f5b54-126">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-126">Determines whether the control background can be transparent.</span></span>                                                                          |
| <span data-ttu-id="f5b54-127">public int bottomMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-127">public int bottomMargin(\[int value\], \[AutoMode mode\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="f5b54-128">public AutoMode bottomMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-128">public AutoMode bottomMarginMode(\[AutoMode mode\])</span></span>                                                         |                                                                                                                                         |
| <span data-ttu-id="f5b54-129">public int bottomMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-129">public int bottomMarginValue(\[int value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="f5b54-130">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-130">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="f5b54-131">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-131">Gets or sets the color scheme of the control.</span></span>                                                                                           |
| <span data-ttu-id="f5b54-132">public int columns(\[int value\], \[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-132">public int columns(\[int value\], \[ColumnsMode mode\])</span></span>                                                     |                                                                                                                                         |
| <span data-ttu-id="f5b54-133">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-133">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span></span>                                                        |                                                                                                                                         |
| <span data-ttu-id="f5b54-134">public int columnspace(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-134">public int columnspace(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                         |
| <span data-ttu-id="f5b54-135">public AutoMode columnspaceMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-135">public AutoMode columnspaceMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                         |
| <span data-ttu-id="f5b54-136">public int columnspaceValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-136">public int columnspaceValue(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="f5b54-137">public int columnsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-137">public int columnsValue(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="f5b54-138">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-138">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="f5b54-139">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-139">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                     |
| <span data-ttu-id="f5b54-140">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="f5b54-140">public int containerId()</span></span>                                                                                    | <span data-ttu-id="f5b54-141">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-141">Retrieves the ID of the parent container for the control.</span></span>                                                                               |
| <span data-ttu-id="f5b54-142">public int containerScrollHorizontalOffset(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-142">public int containerScrollHorizontalOffset(\[int value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="f5b54-143">public int containerScrollVerticalOffset(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-143">public int containerScrollVerticalOffset(\[int value\])</span></span>                                                     |                                                                                                                                         |
| <span data-ttu-id="f5b54-144">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-144">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="f5b54-145">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-145">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                         |
| <span data-ttu-id="f5b54-146">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-146">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="f5b54-147">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-147">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="f5b54-148">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-148">Gets or sets a data source to be used by the control or the form.</span></span>                                                                       |
| <span data-ttu-id="f5b54-149">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-149">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="f5b54-150">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-150">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="f5b54-151">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-151">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                       |
| <span data-ttu-id="f5b54-152">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-152">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="f5b54-153">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-153">Determines whether to enable or disable the object.</span></span>                                                                                     |
| <span data-ttu-id="f5b54-154">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-154">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="f5b54-155">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-155">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="f5b54-156">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-156">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="f5b54-157">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-157">Gets or sets a calculation mode for the height of the control.</span></span>                                                                          |
| <span data-ttu-id="f5b54-158">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-158">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="f5b54-159">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-159">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="f5b54-160">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-160">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="f5b54-161">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-161">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                |
| <span data-ttu-id="f5b54-162">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-162">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                               |                                                                                                                                         |
| <span data-ttu-id="f5b54-163">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-163">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="f5b54-164">public boolean horizontalScrollBarVisible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-164">public boolean horizontalScrollBarVisible(\[boolean value\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="f5b54-165">public int id()</span><span class="sxs-lookup"><span data-stu-id="f5b54-165">public int id()</span></span>                                                                                             | <span data-ttu-id="f5b54-166">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-166">Retrieves the ID of the control.</span></span>                                                                                                        |
| <span data-ttu-id="f5b54-167">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="f5b54-167">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="f5b54-168">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-168">Retrieves a value that indicates whether the control is a container control.</span></span>                                                            |
| <span data-ttu-id="f5b54-169">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-169">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="f5b54-170">public int leftMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-170">public int leftMargin(\[int value\], \[AutoMode mode\])</span></span>                                                     |                                                                                                                                         |
| <span data-ttu-id="f5b54-171">public AutoMode leftMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-171">public AutoMode leftMarginMode(\[AutoMode mode\])</span></span>                                                           |                                                                                                                                         |
| <span data-ttu-id="f5b54-172">public int leftMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-172">public int leftMarginValue(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="f5b54-173">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-173">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="f5b54-174">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-174">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="f5b54-175">public int moveControl(int controlId, \[int insertAfterControlId\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-175">public int moveControl(int controlId, \[int insertAfterControlId\])</span></span>                                         | <span data-ttu-id="f5b54-176">コントロールに指定されたコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-176">Moves a specified control to the control.</span></span>                                                                                               |
| <span data-ttu-id="f5b54-177">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-177">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="f5b54-178">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-178">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="f5b54-179">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-179">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="f5b54-180">public int rightMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-180">public int rightMargin(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                         |
| <span data-ttu-id="f5b54-181">public AutoMode rightMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-181">public AutoMode rightMarginMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                         |
| <span data-ttu-id="f5b54-182">public int rightMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-182">public int rightMarginValue(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="f5b54-183">public int scrollbars(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-183">public int scrollbars(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="f5b54-184">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-184">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="f5b54-185">public boolean selectControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-185">public boolean selectControl(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="f5b54-186">public boolean showTabs(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-186">public boolean showTabs(\[boolean value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="f5b54-187">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-187">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="f5b54-188">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-188">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>         |
| <span data-ttu-id="f5b54-189">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-189">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                         |
| <span data-ttu-id="f5b54-190">public int tab(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-190">public int tab(\[int value\], \[AutoMode mode\])</span></span>                                                            |                                                                                                                                         |
| <span data-ttu-id="f5b54-191">public int tabAppearance(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-191">public int tabAppearance(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="f5b54-192">public boolean tabAutoChange(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-192">public boolean tabAutoChange(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="f5b54-193">public int tabLayout(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-193">public int tabLayout(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="f5b54-194">public AutoMode tabMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-194">public AutoMode tabMode(\[AutoMode mode\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="f5b54-195">public int tabPlacement(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-195">public int tabPlacement(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="f5b54-196">public int tabs(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-196">public int tabs(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="f5b54-197">public int tabValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-197">public int tabValue(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="f5b54-198">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-198">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="f5b54-199">public int topMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-199">public int topMargin(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="f5b54-200">public AutoMode topMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-200">public AutoMode topMarginMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                         |
| <span data-ttu-id="f5b54-201">public int topMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-201">public int topMarginValue(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="f5b54-202">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-202">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="f5b54-203">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-203">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="f5b54-204">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-204">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="f5b54-205">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-205">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="f5b54-206">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-206">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="f5b54-207">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-207">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="f5b54-208">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-208">public boolean useUserLayout(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="f5b54-209">public boolean verticalScrollBarVisible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-209">public boolean verticalScrollBarVisible(\[boolean value\])</span></span>                                                  |                                                                                                                                         |
| <span data-ttu-id="f5b54-210">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-210">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="f5b54-211">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-211">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="f5b54-212">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-212">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="f5b54-213">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-213">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="f5b54-214">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-214">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="f5b54-215">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-215">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="f5b54-216">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-216">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="f5b54-217">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-217">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="f5b54-218">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-218">Gets or sets the calculation mode of the width of the control.</span></span>                                                                          |
| <span data-ttu-id="f5b54-219">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-219">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="f5b54-220">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-220">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="f5b54-221">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="f5b54-221">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                         |

## <a name="method-alignchild"></a><span data-ttu-id="f5b54-222">メソッド alignChild</span><span class="sxs-lookup"><span data-stu-id="f5b54-222">Method alignChild</span></span>

```xpp
public boolean alignChild([boolean value])
```

### <a name="parameters---alignchild"></a><span data-ttu-id="f5b54-223">パラメーター - alignChild</span><span class="sxs-lookup"><span data-stu-id="f5b54-223">Parameters - alignChild</span></span>

<span data-ttu-id="f5b54-224">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-224">value</span></span>  

### <a name="return-value---alignchild"></a><span data-ttu-id="f5b54-225">戻り値 - alignChild</span><span class="sxs-lookup"><span data-stu-id="f5b54-225">Return Value - alignChild</span></span>

## <a name="method-alignchildren"></a><span data-ttu-id="f5b54-226">メソッド alignChildren</span><span class="sxs-lookup"><span data-stu-id="f5b54-226">Method alignChildren</span></span>

```xpp
public boolean alignChildren([boolean value])
```

### <a name="parameters---alignchildren"></a><span data-ttu-id="f5b54-227">パラメーター - alignChildren</span><span class="sxs-lookup"><span data-stu-id="f5b54-227">Parameters - alignChildren</span></span>

<span data-ttu-id="f5b54-228">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-228">value</span></span>  

### <a name="return-value---alignchildren"></a><span data-ttu-id="f5b54-229">戻り値 - alignChildren</span><span class="sxs-lookup"><span data-stu-id="f5b54-229">Return Value - alignChildren</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="f5b54-230">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="f5b54-230">Method alignControl</span></span>

<span data-ttu-id="f5b54-231">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-231">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="f5b54-232">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="f5b54-232">Parameters - alignControl</span></span>

<span data-ttu-id="f5b54-233">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-233">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="f5b54-234">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="f5b54-234">Return Value - alignControl</span></span>

<span data-ttu-id="f5b54-235">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="f5b54-235">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="f5b54-236">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="f5b54-236">Remarks - alignControl</span></span>

<span data-ttu-id="f5b54-237">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="f5b54-237">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="f5b54-238">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="f5b54-238">Method allowEdit</span></span>

<span data-ttu-id="f5b54-239">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-239">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="f5b54-240">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="f5b54-240">Parameters - allowEdit</span></span>

<span data-ttu-id="f5b54-241">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-241">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="f5b54-242">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="f5b54-242">Return Value - allowEdit</span></span>

<span data-ttu-id="f5b54-243">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f5b54-243">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="f5b54-244">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="f5b54-244">Remarks - allowEdit</span></span>

<span data-ttu-id="f5b54-245">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="f5b54-245">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-allowusersetup"></a><span data-ttu-id="f5b54-246">メソッド allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="f5b54-246">Method allowUserSetup</span></span>

```xpp
public int allowUserSetup([int value])
```

### <a name="parameters---allowusersetup"></a><span data-ttu-id="f5b54-247">パラメーター - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="f5b54-247">Parameters - allowUserSetup</span></span>

<span data-ttu-id="f5b54-248">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-248">value</span></span>  

### <a name="return-value---allowusersetup"></a><span data-ttu-id="f5b54-249">戻り値 - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="f5b54-249">Return Value - allowUserSetup</span></span>

## <a name="method-arrangeguide"></a><span data-ttu-id="f5b54-250">メソッド arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="f5b54-250">Method arrangeGuide</span></span>

```xpp
public int arrangeGuide([int value])
```

### <a name="parameters---arrangeguide"></a><span data-ttu-id="f5b54-251">パラメーター - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="f5b54-251">Parameters - arrangeGuide</span></span>

<span data-ttu-id="f5b54-252">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-252">value</span></span>  

### <a name="return-value---arrangeguide"></a><span data-ttu-id="f5b54-253">戻り値 - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="f5b54-253">Return Value - arrangeGuide</span></span>

## <a name="method-arrangemethod"></a><span data-ttu-id="f5b54-254">メソッド arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="f5b54-254">Method arrangeMethod</span></span>

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a><span data-ttu-id="f5b54-255">パラメーター - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="f5b54-255">Parameters - arrangeMethod</span></span>

<span data-ttu-id="f5b54-256">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-256">value</span></span>  

### <a name="return-value---arrangemethod"></a><span data-ttu-id="f5b54-257">戻り値 - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="f5b54-257">Return Value - arrangeMethod</span></span>

## <a name="method-arrangewhen"></a><span data-ttu-id="f5b54-258">メソッド arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="f5b54-258">Method arrangeWhen</span></span>

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a><span data-ttu-id="f5b54-259">パラメーター - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="f5b54-259">Parameters - arrangeWhen</span></span>

<span data-ttu-id="f5b54-260">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-260">value</span></span>  

### <a name="return-value---arrangewhen"></a><span data-ttu-id="f5b54-261">戻り値 - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="f5b54-261">Return Value - arrangeWhen</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="f5b54-262">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="f5b54-262">Method autoDeclaration</span></span>

<span data-ttu-id="f5b54-263">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-263">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="f5b54-264">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="f5b54-264">Parameters - autoDeclaration</span></span>

<span data-ttu-id="f5b54-265">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-265">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="f5b54-266">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="f5b54-266">Return Value - autoDeclaration</span></span>

<span data-ttu-id="f5b54-267">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f5b54-267">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="f5b54-268">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="f5b54-268">Remarks - autoDeclaration</span></span>

<span data-ttu-id="f5b54-269">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="f5b54-269">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="f5b54-270">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="f5b54-270">Method backgroundColor</span></span>

<span data-ttu-id="f5b54-271">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-271">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="f5b54-272">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="f5b54-272">Parameters - backgroundColor</span></span>

<span data-ttu-id="f5b54-273">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-273">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="f5b54-274">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="f5b54-274">Return Value - backgroundColor</span></span>

<span data-ttu-id="f5b54-275">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="f5b54-275">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="f5b54-276">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="f5b54-276">Remarks - backgroundColor</span></span>

<span data-ttu-id="f5b54-277">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f5b54-277">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="f5b54-278">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f5b54-278">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="f5b54-279">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="f5b54-279">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="f5b54-280">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="f5b54-280">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="f5b54-281">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="f5b54-281">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="f5b54-282">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="f5b54-282">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="f5b54-283">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="f5b54-283">Method backStyle</span></span>

<span data-ttu-id="f5b54-284">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-284">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="f5b54-285">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="f5b54-285">Parameters - backStyle</span></span>

<span data-ttu-id="f5b54-286">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-286">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="f5b54-287">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="f5b54-287">Return Value - backStyle</span></span>

<span data-ttu-id="f5b54-288">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="f5b54-288">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="f5b54-289">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="f5b54-289">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="f5b54-290">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="f5b54-290">Parameters - bottomMargin</span></span>

<span data-ttu-id="f5b54-291">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-291">value</span></span>  

<!-- -->

<span data-ttu-id="f5b54-292">モード</span><span class="sxs-lookup"><span data-stu-id="f5b54-292">mode</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="f5b54-293">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="f5b54-293">Return Value - bottomMargin</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="f5b54-294">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-294">Method bottomMarginMode</span></span>

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="f5b54-295">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-295">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="f5b54-296">モード</span><span class="sxs-lookup"><span data-stu-id="f5b54-296">mode</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="f5b54-297">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-297">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="f5b54-298">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-298">Method bottomMarginValue</span></span>

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="f5b54-299">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-299">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="f5b54-300">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-300">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="f5b54-301">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-301">Return Value - bottomMarginValue</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="f5b54-302">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="f5b54-302">Method colorScheme</span></span>

<span data-ttu-id="f5b54-303">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-303">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="f5b54-304">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="f5b54-304">Parameters - colorScheme</span></span>

<span data-ttu-id="f5b54-305">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-305">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="f5b54-306">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="f5b54-306">Return Value - colorScheme</span></span>

<span data-ttu-id="f5b54-307">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="f5b54-307">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="f5b54-308">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="f5b54-308">Remarks - colorScheme</span></span>

<span data-ttu-id="f5b54-309">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="f5b54-309">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="f5b54-310">値です。</span><span class="sxs-lookup"><span data-stu-id="f5b54-310">Value.</span></span> | <span data-ttu-id="f5b54-311">スタイル。</span><span class="sxs-lookup"><span data-stu-id="f5b54-311">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="f5b54-312">0</span><span class="sxs-lookup"><span data-stu-id="f5b54-312">0</span></span>      | <span data-ttu-id="f5b54-313">既定。</span><span class="sxs-lookup"><span data-stu-id="f5b54-313">Default.</span></span>                      |
| <span data-ttu-id="f5b54-314">1</span><span class="sxs-lookup"><span data-stu-id="f5b54-314">1</span></span>      | <span data-ttu-id="f5b54-315">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="f5b54-315">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="f5b54-316">2</span><span class="sxs-lookup"><span data-stu-id="f5b54-316">2</span></span>      | <span data-ttu-id="f5b54-317">真の配色。</span><span class="sxs-lookup"><span data-stu-id="f5b54-317">The true-color scheme.</span></span>        |

## <a name="method-columns"></a><span data-ttu-id="f5b54-318">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="f5b54-318">Method columns</span></span>

```xpp
public int columns([int value], [ColumnsMode mode])
```

### <a name="parameters---columns"></a><span data-ttu-id="f5b54-319">パラメーター - columns</span><span class="sxs-lookup"><span data-stu-id="f5b54-319">Parameters - columns</span></span>

<span data-ttu-id="f5b54-320">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-320">value</span></span>  

<!-- -->

<span data-ttu-id="f5b54-321">モード</span><span class="sxs-lookup"><span data-stu-id="f5b54-321">mode</span></span>  

### <a name="return-value---columns"></a><span data-ttu-id="f5b54-322">戻り値 - columns</span><span class="sxs-lookup"><span data-stu-id="f5b54-322">Return Value - columns</span></span>

## <a name="method-columnsmode"></a><span data-ttu-id="f5b54-323">メソッド columnsMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-323">Method columnsMode</span></span>

```xpp
public ColumnsMode columnsMode([ColumnsMode mode])
```

### <a name="parameters---columnsmode"></a><span data-ttu-id="f5b54-324">パラメーター - columnsMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-324">Parameters - columnsMode</span></span>

<span data-ttu-id="f5b54-325">モード</span><span class="sxs-lookup"><span data-stu-id="f5b54-325">mode</span></span>  

### <a name="return-value---columnsmode"></a><span data-ttu-id="f5b54-326">戻り値 - columnsMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-326">Return Value - columnsMode</span></span>

## <a name="method-columnspace"></a><span data-ttu-id="f5b54-327">メソッド columnspace</span><span class="sxs-lookup"><span data-stu-id="f5b54-327">Method columnspace</span></span>

```xpp
public int columnspace([int value], [AutoMode mode])
```

### <a name="parameters---columnspace"></a><span data-ttu-id="f5b54-328">パラメーター - columnspace</span><span class="sxs-lookup"><span data-stu-id="f5b54-328">Parameters - columnspace</span></span>

<span data-ttu-id="f5b54-329">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-329">value</span></span>  

<!-- -->

<span data-ttu-id="f5b54-330">モード</span><span class="sxs-lookup"><span data-stu-id="f5b54-330">mode</span></span>  

### <a name="return-value---columnspace"></a><span data-ttu-id="f5b54-331">戻り値 - columnspace</span><span class="sxs-lookup"><span data-stu-id="f5b54-331">Return Value - columnspace</span></span>

## <a name="method-columnspacemode"></a><span data-ttu-id="f5b54-332">メソッド columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-332">Method columnspaceMode</span></span>

```xpp
public AutoMode columnspaceMode([AutoMode mode])
```

### <a name="parameters---columnspacemode"></a><span data-ttu-id="f5b54-333">パラメーター - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-333">Parameters - columnspaceMode</span></span>

<span data-ttu-id="f5b54-334">モード</span><span class="sxs-lookup"><span data-stu-id="f5b54-334">mode</span></span>  

### <a name="return-value---columnspacemode"></a><span data-ttu-id="f5b54-335">戻り値 - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-335">Return Value - columnspaceMode</span></span>

## <a name="method-columnspacevalue"></a><span data-ttu-id="f5b54-336">メソッド columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-336">Method columnspaceValue</span></span>

```xpp
public int columnspaceValue([int value])
```

### <a name="parameters---columnspacevalue"></a><span data-ttu-id="f5b54-337">パラメーター - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-337">Parameters - columnspaceValue</span></span>

<span data-ttu-id="f5b54-338">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-338">value</span></span>  

### <a name="return-value---columnspacevalue"></a><span data-ttu-id="f5b54-339">戻り値 - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-339">Return Value - columnspaceValue</span></span>

## <a name="method-columnsvalue"></a><span data-ttu-id="f5b54-340">メソッド columnsValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-340">Method columnsValue</span></span>

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a><span data-ttu-id="f5b54-341">パラメーター - columnsValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-341">Parameters - columnsValue</span></span>

<span data-ttu-id="f5b54-342">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-342">value</span></span>  

### <a name="return-value---columnsvalue"></a><span data-ttu-id="f5b54-343">戻り値 - columnsValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-343">Return Value - columnsValue</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="f5b54-344">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="f5b54-344">Method configurationKey</span></span>

<span data-ttu-id="f5b54-345">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-345">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="f5b54-346">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="f5b54-346">Parameters - configurationKey</span></span>

<span data-ttu-id="f5b54-347">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-347">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="f5b54-348">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="f5b54-348">Return Value - configurationKey</span></span>

<span data-ttu-id="f5b54-349">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="f5b54-349">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="f5b54-350">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="f5b54-350">Remarks - configurationKey</span></span>

<span data-ttu-id="f5b54-351">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f5b54-351">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="f5b54-352">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="f5b54-352">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="f5b54-353">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="f5b54-353">Method containerId</span></span>

<span data-ttu-id="f5b54-354">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-354">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="f5b54-355">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="f5b54-355">Return Value - containerId</span></span>

<span data-ttu-id="f5b54-356">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="f5b54-356">The ID of the parent container.</span></span>

## <a name="method-containerscrollhorizontaloffset"></a><span data-ttu-id="f5b54-357">メソッド containerScrollHorizontalOffset</span><span class="sxs-lookup"><span data-stu-id="f5b54-357">Method containerScrollHorizontalOffset</span></span>

```xpp
public int containerScrollHorizontalOffset([int value])
```

### <a name="parameters---containerscrollhorizontaloffset"></a><span data-ttu-id="f5b54-358">パラメーター - containerScrollHorizontalOffset</span><span class="sxs-lookup"><span data-stu-id="f5b54-358">Parameters - containerScrollHorizontalOffset</span></span>

<span data-ttu-id="f5b54-359">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-359">value</span></span>  

### <a name="return-value---containerscrollhorizontaloffset"></a><span data-ttu-id="f5b54-360">戻り値 - containerScrollHorizontalOffset</span><span class="sxs-lookup"><span data-stu-id="f5b54-360">Return Value - containerScrollHorizontalOffset</span></span>

## <a name="method-containerscrollverticaloffset"></a><span data-ttu-id="f5b54-361">メソッド containerScrollVerticalOffset</span><span class="sxs-lookup"><span data-stu-id="f5b54-361">Method containerScrollVerticalOffset</span></span>

```xpp
public int containerScrollVerticalOffset([int value])
```

### <a name="parameters---containerscrollverticaloffset"></a><span data-ttu-id="f5b54-362">パラメーター - containerScrollVerticalOffset</span><span class="sxs-lookup"><span data-stu-id="f5b54-362">Parameters - containerScrollVerticalOffset</span></span>

<span data-ttu-id="f5b54-363">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-363">value</span></span>  

### <a name="return-value---containerscrollverticaloffset"></a><span data-ttu-id="f5b54-364">戻り値 - containerScrollVerticalOffset</span><span class="sxs-lookup"><span data-stu-id="f5b54-364">Return Value - containerScrollVerticalOffset</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="f5b54-365">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="f5b54-365">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="f5b54-366">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="f5b54-366">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="f5b54-367">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-367">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="f5b54-368">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="f5b54-368">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="f5b54-369">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="f5b54-369">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="f5b54-370">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="f5b54-370">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="f5b54-371">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-371">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="f5b54-372">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="f5b54-372">Return Value - countryRegionContextField</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="f5b54-373">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="f5b54-373">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="f5b54-374">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="f5b54-374">Parameters - dataRelationPath</span></span>

<span data-ttu-id="f5b54-375">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-375">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="f5b54-376">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="f5b54-376">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="f5b54-377">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="f5b54-377">Method dataSource</span></span>

<span data-ttu-id="f5b54-378">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-378">Gets or sets a data source to be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="f5b54-379">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="f5b54-379">Parameters - dataSource</span></span>

<span data-ttu-id="f5b54-380">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-380">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="f5b54-381">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="f5b54-381">Return Value - dataSource</span></span>

<span data-ttu-id="f5b54-382">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="f5b54-382">The identifier of the data source to be used.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="f5b54-383">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="f5b54-383">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="f5b54-384">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="f5b54-384">Parameters - displayTarget</span></span>

<span data-ttu-id="f5b54-385">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-385">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="f5b54-386">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="f5b54-386">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="f5b54-387">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="f5b54-387">Method dragDrop</span></span>

<span data-ttu-id="f5b54-388">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-388">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="f5b54-389">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="f5b54-389">Parameters - dragDrop</span></span>

<span data-ttu-id="f5b54-390">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-390">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="f5b54-391">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="f5b54-391">Return Value - dragDrop</span></span>

<span data-ttu-id="f5b54-392">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="f5b54-392">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="f5b54-393">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="f5b54-393">Method enabled</span></span>

<span data-ttu-id="f5b54-394">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-394">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="f5b54-395">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="f5b54-395">Parameters - enabled</span></span>

<span data-ttu-id="f5b54-396">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-396">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="f5b54-397">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="f5b54-397">Return Value - enabled</span></span>

<span data-ttu-id="f5b54-398">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f5b54-398">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="f5b54-399">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="f5b54-399">Remarks - enabled</span></span>

<span data-ttu-id="f5b54-400">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="f5b54-400">The enabled property allows controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="f5b54-401">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f5b54-401">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="f5b54-402">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="f5b54-402">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-height"></a><span data-ttu-id="f5b54-403">メソッド height</span><span class="sxs-lookup"><span data-stu-id="f5b54-403">Method height</span></span>

<span data-ttu-id="f5b54-404">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-404">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="f5b54-405">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="f5b54-405">Parameters - height</span></span>

<span data-ttu-id="f5b54-406">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-406">value</span></span>  

<!-- -->

<span data-ttu-id="f5b54-407">モード</span><span class="sxs-lookup"><span data-stu-id="f5b54-407">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="f5b54-408">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="f5b54-408">Return Value - height</span></span>

<span data-ttu-id="f5b54-409">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="f5b54-409">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="f5b54-410">備考 - height</span><span class="sxs-lookup"><span data-stu-id="f5b54-410">Remarks - height</span></span>

<span data-ttu-id="f5b54-411">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f5b54-411">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="f5b54-412">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="f5b54-412">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="f5b54-413">モード。</span><span class="sxs-lookup"><span data-stu-id="f5b54-413">Mode.</span></span>            | <span data-ttu-id="f5b54-414">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="f5b54-414">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b54-415">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="f5b54-415">-1 Exact.</span></span>        | <span data-ttu-id="f5b54-416">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f5b54-416">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="f5b54-417">0 自動。</span><span class="sxs-lookup"><span data-stu-id="f5b54-417">0 Auto.</span></span>          | <span data-ttu-id="f5b54-418">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="f5b54-418">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="f5b54-419">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="f5b54-419">1 Column height.</span></span> | <span data-ttu-id="f5b54-420">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="f5b54-420">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="f5b54-421">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="f5b54-421">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="f5b54-422">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-422">Method heightMode</span></span>

<span data-ttu-id="f5b54-423">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-423">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="f5b54-424">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-424">Parameters - heightMode</span></span>

<span data-ttu-id="f5b54-425">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-425">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="f5b54-426">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-426">Return Value - heightMode</span></span>

<span data-ttu-id="f5b54-427">計算モード。</span><span class="sxs-lookup"><span data-stu-id="f5b54-427">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="f5b54-428">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-428">Remarks - heightMode</span></span>

<span data-ttu-id="f5b54-429">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="f5b54-429">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="f5b54-430">モード。</span><span class="sxs-lookup"><span data-stu-id="f5b54-430">Mode.</span></span>          | <span data-ttu-id="f5b54-431">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="f5b54-431">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b54-432">正確。</span><span class="sxs-lookup"><span data-stu-id="f5b54-432">Exact.</span></span>         | <span data-ttu-id="f5b54-433">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f5b54-433">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="f5b54-434">自動。</span><span class="sxs-lookup"><span data-stu-id="f5b54-434">Auto.</span></span>          | <span data-ttu-id="f5b54-435">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="f5b54-435">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="f5b54-436">列の高さ</span><span class="sxs-lookup"><span data-stu-id="f5b54-436">Column height.</span></span> | <span data-ttu-id="f5b54-437">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="f5b54-437">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="f5b54-438">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="f5b54-438">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="f5b54-439">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-439">Method heightValue</span></span>

<span data-ttu-id="f5b54-440">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-440">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="f5b54-441">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-441">Parameters - heightValue</span></span>

<span data-ttu-id="f5b54-442">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-442">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="f5b54-443">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-443">Return Value - heightValue</span></span>

<span data-ttu-id="f5b54-444">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="f5b54-444">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="f5b54-445">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-445">Remarks - heightValue</span></span>

<span data-ttu-id="f5b54-446">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="f5b54-446">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="f5b54-447">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="f5b54-447">Method helpText</span></span>

<span data-ttu-id="f5b54-448">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-448">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="f5b54-449">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="f5b54-449">Parameters - helpText</span></span>

<span data-ttu-id="f5b54-450">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-450">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="f5b54-451">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="f5b54-451">Return Value - helpText</span></span>

<span data-ttu-id="f5b54-452">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="f5b54-452">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="f5b54-453">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="f5b54-453">Remarks - helpText</span></span>

<span data-ttu-id="f5b54-454">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-454">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="f5b54-455">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="f5b54-455">The help text must not exceed 250 characters.</span></span>

## <a name="method-hideifempty"></a><span data-ttu-id="f5b54-456">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="f5b54-456">Method hideIfEmpty</span></span>

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a><span data-ttu-id="f5b54-457">パラメーター - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="f5b54-457">Parameters - hideIfEmpty</span></span>

<span data-ttu-id="f5b54-458">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-458">value</span></span>  

### <a name="return-value---hideifempty"></a><span data-ttu-id="f5b54-459">戻り値 - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="f5b54-459">Return Value - hideIfEmpty</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="f5b54-460">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="f5b54-460">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="f5b54-461">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="f5b54-461">Parameters - hierarchyParent</span></span>

<span data-ttu-id="f5b54-462">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-462">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="f5b54-463">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="f5b54-463">Return Value - hierarchyParent</span></span>

## <a name="method-horizontalscrollbarvisible"></a><span data-ttu-id="f5b54-464">メソッド horizontalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="f5b54-464">Method horizontalScrollBarVisible</span></span>

```xpp
public boolean horizontalScrollBarVisible([boolean value])
```

### <a name="parameters---horizontalscrollbarvisible"></a><span data-ttu-id="f5b54-465">パラメーター - horizontalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="f5b54-465">Parameters - horizontalScrollBarVisible</span></span>

<span data-ttu-id="f5b54-466">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-466">value</span></span>  

### <a name="return-value---horizontalscrollbarvisible"></a><span data-ttu-id="f5b54-467">戻り値 - horizontalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="f5b54-467">Return Value - horizontalScrollBarVisible</span></span>

## <a name="method-id"></a><span data-ttu-id="f5b54-468">メソッド id</span><span class="sxs-lookup"><span data-stu-id="f5b54-468">Method id</span></span>

<span data-ttu-id="f5b54-469">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-469">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="f5b54-470">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="f5b54-470">Return Value - id</span></span>

<span data-ttu-id="f5b54-471">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="f5b54-471">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="f5b54-472">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="f5b54-472">Method isContainer</span></span>

<span data-ttu-id="f5b54-473">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-473">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="f5b54-474">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="f5b54-474">Return Value - isContainer</span></span>

<span data-ttu-id="f5b54-475">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="f5b54-475">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-left"></a><span data-ttu-id="f5b54-476">メソッド left</span><span class="sxs-lookup"><span data-stu-id="f5b54-476">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="f5b54-477">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="f5b54-477">Parameters - left</span></span>

<span data-ttu-id="f5b54-478">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-478">value</span></span>  

<!-- -->

<span data-ttu-id="f5b54-479">モード</span><span class="sxs-lookup"><span data-stu-id="f5b54-479">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="f5b54-480">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="f5b54-480">Return Value - left</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="f5b54-481">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="f5b54-481">Method leftMargin</span></span>

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="f5b54-482">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="f5b54-482">Parameters - leftMargin</span></span>

<span data-ttu-id="f5b54-483">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-483">value</span></span>  

<!-- -->

<span data-ttu-id="f5b54-484">モード</span><span class="sxs-lookup"><span data-stu-id="f5b54-484">mode</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="f5b54-485">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="f5b54-485">Return Value - leftMargin</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="f5b54-486">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-486">Method leftMarginMode</span></span>

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="f5b54-487">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-487">Parameters - leftMarginMode</span></span>

<span data-ttu-id="f5b54-488">モード</span><span class="sxs-lookup"><span data-stu-id="f5b54-488">mode</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="f5b54-489">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-489">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="f5b54-490">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-490">Method leftMarginValue</span></span>

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="f5b54-491">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-491">Parameters - leftMarginValue</span></span>

<span data-ttu-id="f5b54-492">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-492">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="f5b54-493">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-493">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="f5b54-494">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-494">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="f5b54-495">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-495">Parameters - leftMode</span></span>

<span data-ttu-id="f5b54-496">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-496">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="f5b54-497">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-497">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="f5b54-498">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-498">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="f5b54-499">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-499">Parameters - leftValue</span></span>

<span data-ttu-id="f5b54-500">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-500">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="f5b54-501">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-501">Return Value - leftValue</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="f5b54-502">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="f5b54-502">Method moveControl</span></span>

<span data-ttu-id="f5b54-503">コントロールに指定されたコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-503">Moves a specified control to the control.</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterControlId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="f5b54-504">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="f5b54-504">Parameters - moveControl</span></span>

<span data-ttu-id="f5b54-505">controlId</span><span class="sxs-lookup"><span data-stu-id="f5b54-505">controlId</span></span>  

<!-- -->

<span data-ttu-id="f5b54-506">insertAfterControlId</span><span class="sxs-lookup"><span data-stu-id="f5b54-506">insertAfterControlId</span></span>  

### <a name="return-value---movecontrol"></a><span data-ttu-id="f5b54-507">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="f5b54-507">Return Value - moveControl</span></span>

<span data-ttu-id="f5b54-508">コントロールが正常に移動した場合は 1、それ以外の場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="f5b54-508">1 if the control was moved successfully; otherwise, 0.</span></span>

### <a name="remarks---movecontrol"></a><span data-ttu-id="f5b54-509">備考 - moveControl</span><span class="sxs-lookup"><span data-stu-id="f5b54-509">Remarks - moveControl</span></span>

<span data-ttu-id="f5b54-510">一般に、指定したコントロールをコントロールに含めることができ、現在のコンテナーから移動できる場合、このメソッドは成功します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-510">In general, if the specified control can be contained in the control and can be moved from the container that it is currently in, this method should succeed.</span></span> <span data-ttu-id="f5b54-511">ただし、場合によっては、参照グループ コントロールのインスタンス コントロールなど、コントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="f5b54-511">However, in some cases, such as for the reference group control instance, controls cannot be moved.</span></span>

## <a name="method-name"></a><span data-ttu-id="f5b54-512">メソッド名</span><span class="sxs-lookup"><span data-stu-id="f5b54-512">Method name</span></span>

<span data-ttu-id="f5b54-513">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-513">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="f5b54-514">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="f5b54-514">Parameters - name</span></span>

<span data-ttu-id="f5b54-515">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-515">value</span></span>  
<span data-ttu-id="f5b54-516">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="f5b54-516">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="f5b54-517">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="f5b54-517">Return Value - name</span></span>

<span data-ttu-id="f5b54-518">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="f5b54-518">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="f5b54-519">備考 - name</span><span class="sxs-lookup"><span data-stu-id="f5b54-519">Remarks - name</span></span>

<span data-ttu-id="f5b54-520">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5b54-520">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="f5b54-521">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5b54-521">It must start with a letter.</span></span>
-   <span data-ttu-id="f5b54-522">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="f5b54-522">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="f5b54-523">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="f5b54-523">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="f5b54-524">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="f5b54-524">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="f5b54-525">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="f5b54-525">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="f5b54-526">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="f5b54-526">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="f5b54-527">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="f5b54-527">Parameters - neededPermission</span></span>

<span data-ttu-id="f5b54-528">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-528">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="f5b54-529">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="f5b54-529">Return Value - neededPermission</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="f5b54-530">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="f5b54-530">Method rightMargin</span></span>

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="f5b54-531">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="f5b54-531">Parameters - rightMargin</span></span>

<span data-ttu-id="f5b54-532">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-532">value</span></span>  

<!-- -->

<span data-ttu-id="f5b54-533">モード</span><span class="sxs-lookup"><span data-stu-id="f5b54-533">mode</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="f5b54-534">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="f5b54-534">Return Value - rightMargin</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="f5b54-535">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-535">Method rightMarginMode</span></span>

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="f5b54-536">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-536">Parameters - rightMarginMode</span></span>

<span data-ttu-id="f5b54-537">モード</span><span class="sxs-lookup"><span data-stu-id="f5b54-537">mode</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="f5b54-538">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-538">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="f5b54-539">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-539">Method rightMarginValue</span></span>

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="f5b54-540">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-540">Parameters - rightMarginValue</span></span>

<span data-ttu-id="f5b54-541">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-541">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="f5b54-542">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-542">Return Value - rightMarginValue</span></span>

## <a name="method-scrollbars"></a><span data-ttu-id="f5b54-543">メソッド scrollbars</span><span class="sxs-lookup"><span data-stu-id="f5b54-543">Method scrollbars</span></span>

```xpp
public int scrollbars([int value])
```

### <a name="parameters---scrollbars"></a><span data-ttu-id="f5b54-544">パラメーター - scrollbars</span><span class="sxs-lookup"><span data-stu-id="f5b54-544">Parameters - scrollbars</span></span>

<span data-ttu-id="f5b54-545">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-545">value</span></span>  

### <a name="return-value---scrollbars"></a><span data-ttu-id="f5b54-546">戻り値 - scrollbars</span><span class="sxs-lookup"><span data-stu-id="f5b54-546">Return Value - scrollbars</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="f5b54-547">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="f5b54-547">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="f5b54-548">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="f5b54-548">Parameters - securityKey</span></span>

<span data-ttu-id="f5b54-549">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-549">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="f5b54-550">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="f5b54-550">Return Value - securityKey</span></span>

## <a name="method-selectcontrol"></a><span data-ttu-id="f5b54-551">メソッド selectControl</span><span class="sxs-lookup"><span data-stu-id="f5b54-551">Method selectControl</span></span>

```xpp
public boolean selectControl([boolean value])
```

### <a name="parameters---selectcontrol"></a><span data-ttu-id="f5b54-552">パラメーター - selectControl</span><span class="sxs-lookup"><span data-stu-id="f5b54-552">Parameters - selectControl</span></span>

<span data-ttu-id="f5b54-553">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-553">value</span></span>  

### <a name="return-value---selectcontrol"></a><span data-ttu-id="f5b54-554">戻り値 - selectControl</span><span class="sxs-lookup"><span data-stu-id="f5b54-554">Return Value - selectControl</span></span>

## <a name="method-showtabs"></a><span data-ttu-id="f5b54-555">メソッド showTabs</span><span class="sxs-lookup"><span data-stu-id="f5b54-555">Method showTabs</span></span>

```xpp
public boolean showTabs([boolean value])
```

### <a name="parameters---showtabs"></a><span data-ttu-id="f5b54-556">パラメーター - showTabs</span><span class="sxs-lookup"><span data-stu-id="f5b54-556">Parameters - showTabs</span></span>

<span data-ttu-id="f5b54-557">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-557">value</span></span>  

### <a name="return-value---showtabs"></a><span data-ttu-id="f5b54-558">戻り値 - showTabs</span><span class="sxs-lookup"><span data-stu-id="f5b54-558">Return Value - showTabs</span></span>

## <a name="method-skip"></a><span data-ttu-id="f5b54-559">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="f5b54-559">Method skip</span></span>

<span data-ttu-id="f5b54-560">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-560">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="f5b54-561">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="f5b54-561">Parameters - skip</span></span>

<span data-ttu-id="f5b54-562">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-562">value</span></span>  
<span data-ttu-id="f5b54-563">コントロールの skip プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="f5b54-563">The value to assign to the skip property of the control.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="f5b54-564">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="f5b54-564">Return Value - skip</span></span>

<span data-ttu-id="f5b54-565">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f5b54-565">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-style"></a><span data-ttu-id="f5b54-566">メソッド style</span><span class="sxs-lookup"><span data-stu-id="f5b54-566">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="f5b54-567">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="f5b54-567">Parameters - style</span></span>

<span data-ttu-id="f5b54-568">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-568">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="f5b54-569">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="f5b54-569">Return Value - style</span></span>

## <a name="method-tab"></a><span data-ttu-id="f5b54-570">メソッド tab</span><span class="sxs-lookup"><span data-stu-id="f5b54-570">Method tab</span></span>

```xpp
public int tab([int value], [AutoMode mode])
```

### <a name="parameters---tab"></a><span data-ttu-id="f5b54-571">パラメーター - tab</span><span class="sxs-lookup"><span data-stu-id="f5b54-571">Parameters - tab</span></span>

<span data-ttu-id="f5b54-572">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-572">value</span></span>  

<!-- -->

<span data-ttu-id="f5b54-573">モード</span><span class="sxs-lookup"><span data-stu-id="f5b54-573">mode</span></span>  

### <a name="return-value---tab"></a><span data-ttu-id="f5b54-574">戻り値 - tab</span><span class="sxs-lookup"><span data-stu-id="f5b54-574">Return Value - tab</span></span>

## <a name="method-tabappearance"></a><span data-ttu-id="f5b54-575">メソッド tabAppearance</span><span class="sxs-lookup"><span data-stu-id="f5b54-575">Method tabAppearance</span></span>

```xpp
public int tabAppearance([int value])
```

### <a name="parameters---tabappearance"></a><span data-ttu-id="f5b54-576">パラメーター - tabAppearance</span><span class="sxs-lookup"><span data-stu-id="f5b54-576">Parameters - tabAppearance</span></span>

<span data-ttu-id="f5b54-577">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-577">value</span></span>  

### <a name="return-value---tabappearance"></a><span data-ttu-id="f5b54-578">戻り値 - tabAppearance</span><span class="sxs-lookup"><span data-stu-id="f5b54-578">Return Value - tabAppearance</span></span>

## <a name="method-tabautochange"></a><span data-ttu-id="f5b54-579">メソッド tabAutoChange</span><span class="sxs-lookup"><span data-stu-id="f5b54-579">Method tabAutoChange</span></span>

```xpp
public boolean tabAutoChange([boolean value])
```

### <a name="parameters---tabautochange"></a><span data-ttu-id="f5b54-580">パラメーター - tabAutoChange</span><span class="sxs-lookup"><span data-stu-id="f5b54-580">Parameters - tabAutoChange</span></span>

<span data-ttu-id="f5b54-581">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-581">value</span></span>  

### <a name="return-value---tabautochange"></a><span data-ttu-id="f5b54-582">戻り値 - tabAutoChange</span><span class="sxs-lookup"><span data-stu-id="f5b54-582">Return Value - tabAutoChange</span></span>

## <a name="method-tablayout"></a><span data-ttu-id="f5b54-583">メソッド tabLayout</span><span class="sxs-lookup"><span data-stu-id="f5b54-583">Method tabLayout</span></span>

```xpp
public int tabLayout([int value])
```

### <a name="parameters---tablayout"></a><span data-ttu-id="f5b54-584">パラメーター - tabLayout</span><span class="sxs-lookup"><span data-stu-id="f5b54-584">Parameters - tabLayout</span></span>

<span data-ttu-id="f5b54-585">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-585">value</span></span>  

### <a name="return-value---tablayout"></a><span data-ttu-id="f5b54-586">戻り値 - tabLayout</span><span class="sxs-lookup"><span data-stu-id="f5b54-586">Return Value - tabLayout</span></span>

## <a name="method-tabmode"></a><span data-ttu-id="f5b54-587">メソッド tabMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-587">Method tabMode</span></span>

```xpp
public AutoMode tabMode([AutoMode mode])
```

### <a name="parameters---tabmode"></a><span data-ttu-id="f5b54-588">パラメーター - tabMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-588">Parameters - tabMode</span></span>

<span data-ttu-id="f5b54-589">モード</span><span class="sxs-lookup"><span data-stu-id="f5b54-589">mode</span></span>  

### <a name="return-value---tabmode"></a><span data-ttu-id="f5b54-590">戻り値 - tabMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-590">Return Value - tabMode</span></span>

## <a name="method-tabplacement"></a><span data-ttu-id="f5b54-591">メソッド tabPlacement</span><span class="sxs-lookup"><span data-stu-id="f5b54-591">Method tabPlacement</span></span>

```xpp
public int tabPlacement([int value])
```

### <a name="parameters---tabplacement"></a><span data-ttu-id="f5b54-592">パラメーター - tabPlacement</span><span class="sxs-lookup"><span data-stu-id="f5b54-592">Parameters - tabPlacement</span></span>

<span data-ttu-id="f5b54-593">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-593">value</span></span>  

### <a name="return-value---tabplacement"></a><span data-ttu-id="f5b54-594">戻り値 - tabPlacement</span><span class="sxs-lookup"><span data-stu-id="f5b54-594">Return Value - tabPlacement</span></span>

## <a name="method-tabs"></a><span data-ttu-id="f5b54-595">メソッド tabs</span><span class="sxs-lookup"><span data-stu-id="f5b54-595">Method tabs</span></span>

```xpp
public int tabs([int value])
```

### <a name="parameters---tabs"></a><span data-ttu-id="f5b54-596">パラメーター - tabs</span><span class="sxs-lookup"><span data-stu-id="f5b54-596">Parameters - tabs</span></span>

<span data-ttu-id="f5b54-597">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-597">value</span></span>  

### <a name="return-value---tabs"></a><span data-ttu-id="f5b54-598">戻り値 - tabs</span><span class="sxs-lookup"><span data-stu-id="f5b54-598">Return Value - tabs</span></span>

## <a name="method-tabvalue"></a><span data-ttu-id="f5b54-599">メソッド tabValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-599">Method tabValue</span></span>

```xpp
public int tabValue([int value])
```

### <a name="parameters---tabvalue"></a><span data-ttu-id="f5b54-600">パラメーター - tabValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-600">Parameters - tabValue</span></span>

<span data-ttu-id="f5b54-601">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-601">value</span></span>  

### <a name="return-value---tabvalue"></a><span data-ttu-id="f5b54-602">戻り値 - tabValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-602">Return Value - tabValue</span></span>

## <a name="method-top"></a><span data-ttu-id="f5b54-603">メソッド top</span><span class="sxs-lookup"><span data-stu-id="f5b54-603">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="f5b54-604">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="f5b54-604">Parameters - top</span></span>

<span data-ttu-id="f5b54-605">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-605">value</span></span>  

<!-- -->

<span data-ttu-id="f5b54-606">モード</span><span class="sxs-lookup"><span data-stu-id="f5b54-606">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="f5b54-607">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="f5b54-607">Return Value - top</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="f5b54-608">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="f5b54-608">Method topMargin</span></span>

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="f5b54-609">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="f5b54-609">Parameters - topMargin</span></span>

<span data-ttu-id="f5b54-610">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-610">value</span></span>  

<!-- -->

<span data-ttu-id="f5b54-611">モード</span><span class="sxs-lookup"><span data-stu-id="f5b54-611">mode</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="f5b54-612">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="f5b54-612">Return Value - topMargin</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="f5b54-613">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-613">Method topMarginMode</span></span>

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="f5b54-614">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-614">Parameters - topMarginMode</span></span>

<span data-ttu-id="f5b54-615">モード</span><span class="sxs-lookup"><span data-stu-id="f5b54-615">mode</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="f5b54-616">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-616">Return Value - topMarginMode</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="f5b54-617">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-617">Method topMarginValue</span></span>

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="f5b54-618">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-618">Parameters - topMarginValue</span></span>

<span data-ttu-id="f5b54-619">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-619">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="f5b54-620">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-620">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="f5b54-621">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-621">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="f5b54-622">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-622">Parameters - topMode</span></span>

<span data-ttu-id="f5b54-623">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-623">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="f5b54-624">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-624">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="f5b54-625">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-625">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="f5b54-626">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-626">Parameters - topValue</span></span>

<span data-ttu-id="f5b54-627">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-627">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="f5b54-628">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-628">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="f5b54-629">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="f5b54-629">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="f5b54-630">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="f5b54-630">Parameters - type</span></span>

<span data-ttu-id="f5b54-631">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-631">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="f5b54-632">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="f5b54-632">Return Value - type</span></span>

## <a name="method-userdata"></a><span data-ttu-id="f5b54-633">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="f5b54-633">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="f5b54-634">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="f5b54-634">Parameters - userData</span></span>

<span data-ttu-id="f5b54-635">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-635">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="f5b54-636">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="f5b54-636">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="f5b54-637">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="f5b54-637">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="f5b54-638">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="f5b54-638">Parameters - userDataItem</span></span>

<span data-ttu-id="f5b54-639">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-639">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="f5b54-640">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="f5b54-640">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="f5b54-641">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="f5b54-641">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="f5b54-642">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="f5b54-642">Parameters - userDataItems</span></span>

<span data-ttu-id="f5b54-643">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-643">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="f5b54-644">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="f5b54-644">Return Value - userDataItems</span></span>

## <a name="method-useuserlayout"></a><span data-ttu-id="f5b54-645">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="f5b54-645">Method useUserLayout</span></span>

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a><span data-ttu-id="f5b54-646">パラメーター - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="f5b54-646">Parameters - useUserLayout</span></span>

<span data-ttu-id="f5b54-647">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-647">value</span></span>  

### <a name="return-value---useuserlayout"></a><span data-ttu-id="f5b54-648">戻り値 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="f5b54-648">Return Value - useUserLayout</span></span>

## <a name="method-verticalscrollbarvisible"></a><span data-ttu-id="f5b54-649">メソッド verticalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="f5b54-649">Method verticalScrollBarVisible</span></span>

```xpp
public boolean verticalScrollBarVisible([boolean value])
```

### <a name="parameters---verticalscrollbarvisible"></a><span data-ttu-id="f5b54-650">パラメーター - verticalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="f5b54-650">Parameters - verticalScrollBarVisible</span></span>

<span data-ttu-id="f5b54-651">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-651">value</span></span>  

### <a name="return-value---verticalscrollbarvisible"></a><span data-ttu-id="f5b54-652">戻り値 - verticalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="f5b54-652">Return Value - verticalScrollBarVisible</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="f5b54-653">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="f5b54-653">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="f5b54-654">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="f5b54-654">Parameters - verticalSpacing</span></span>

<span data-ttu-id="f5b54-655">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-655">value</span></span>  

<!-- -->

<span data-ttu-id="f5b54-656">モード</span><span class="sxs-lookup"><span data-stu-id="f5b54-656">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="f5b54-657">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="f5b54-657">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="f5b54-658">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-658">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="f5b54-659">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-659">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="f5b54-660">モード</span><span class="sxs-lookup"><span data-stu-id="f5b54-660">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="f5b54-661">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-661">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="f5b54-662">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-662">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="f5b54-663">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-663">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="f5b54-664">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-664">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="f5b54-665">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-665">Return Value - verticalSpacingValue</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="f5b54-666">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-666">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="f5b54-667">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-667">Parameters - viewEditMode</span></span>

<span data-ttu-id="f5b54-668">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-668">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="f5b54-669">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-669">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="f5b54-670">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="f5b54-670">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="f5b54-671">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="f5b54-671">Parameters - visible</span></span>

<span data-ttu-id="f5b54-672">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-672">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="f5b54-673">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="f5b54-673">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="f5b54-674">メソッド width</span><span class="sxs-lookup"><span data-stu-id="f5b54-674">Method width</span></span>

<span data-ttu-id="f5b54-675">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-675">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="f5b54-676">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="f5b54-676">Parameters - width</span></span>

<span data-ttu-id="f5b54-677">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-677">value</span></span>  

<!-- -->

<span data-ttu-id="f5b54-678">モード</span><span class="sxs-lookup"><span data-stu-id="f5b54-678">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="f5b54-679">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="f5b54-679">Return Value - width</span></span>

<span data-ttu-id="f5b54-680">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="f5b54-680">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="f5b54-681">備考 - width</span><span class="sxs-lookup"><span data-stu-id="f5b54-681">Remarks - width</span></span>

<span data-ttu-id="f5b54-682">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f5b54-682">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="f5b54-683">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="f5b54-683">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="f5b54-684">モード。</span><span class="sxs-lookup"><span data-stu-id="f5b54-684">Mode.</span></span>           | <span data-ttu-id="f5b54-685">幅計算。</span><span class="sxs-lookup"><span data-stu-id="f5b54-685">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b54-686">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="f5b54-686">-1 Exact.</span></span>       | <span data-ttu-id="f5b54-687">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="f5b54-687">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="f5b54-688">0 自動。</span><span class="sxs-lookup"><span data-stu-id="f5b54-688">0 Auto.</span></span>         | <span data-ttu-id="f5b54-689">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="f5b54-689">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="f5b54-690">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="f5b54-690">1 Column width.</span></span> | <span data-ttu-id="f5b54-691">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="f5b54-691">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="f5b54-692">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="f5b54-692">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="f5b54-693">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-693">Method widthMode</span></span>

<span data-ttu-id="f5b54-694">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-694">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="f5b54-695">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-695">Parameters - widthMode</span></span>

<span data-ttu-id="f5b54-696">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-696">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="f5b54-697">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-697">Return Value - widthMode</span></span>

<span data-ttu-id="f5b54-698">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f5b54-698">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="f5b54-699">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="f5b54-699">Remarks - widthMode</span></span>

<span data-ttu-id="f5b54-700">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="f5b54-700">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="f5b54-701">モード。</span><span class="sxs-lookup"><span data-stu-id="f5b54-701">Mode.</span></span>         | <span data-ttu-id="f5b54-702">幅計算。</span><span class="sxs-lookup"><span data-stu-id="f5b54-702">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b54-703">正確。</span><span class="sxs-lookup"><span data-stu-id="f5b54-703">Exact.</span></span>        | <span data-ttu-id="f5b54-704">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="f5b54-704">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="f5b54-705">自動。</span><span class="sxs-lookup"><span data-stu-id="f5b54-705">Auto.</span></span>         | <span data-ttu-id="f5b54-706">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="f5b54-706">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="f5b54-707">列の幅。</span><span class="sxs-lookup"><span data-stu-id="f5b54-707">Column width.</span></span> | <span data-ttu-id="f5b54-708">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="f5b54-708">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="f5b54-709">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="f5b54-709">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="f5b54-710">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-710">Method widthValue</span></span>

<span data-ttu-id="f5b54-711">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-711">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="f5b54-712">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-712">Parameters - widthValue</span></span>

<span data-ttu-id="f5b54-713">値</span><span class="sxs-lookup"><span data-stu-id="f5b54-713">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="f5b54-714">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-714">Return Value - widthValue</span></span>

<span data-ttu-id="f5b54-715">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="f5b54-715">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="f5b54-716">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="f5b54-716">Remarks - widthValue</span></span>

<span data-ttu-id="f5b54-717">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="f5b54-717">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="f5b54-718">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="f5b54-718">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="f5b54-719">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="f5b54-719">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="f5b54-720">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="f5b54-720">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="f5b54-721">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="f5b54-721">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="f5b54-722">overrideObject</span><span class="sxs-lookup"><span data-stu-id="f5b54-722">overrideObject</span></span>  

