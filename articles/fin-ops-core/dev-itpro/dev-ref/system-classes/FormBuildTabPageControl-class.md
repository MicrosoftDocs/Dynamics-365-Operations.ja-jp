---
title: FormBuildTabPageControl クラス
description: このトピックでは、FormBuildTabPageControl クラスについて説明します。
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
ms.openlocfilehash: b82ddbd9265e992a30e29ccc16bc5efeb9ef60ca
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502639"
---
# <a name="class-formbuildtabpagecontrol"></a><span data-ttu-id="0f783-103">クラス FormBuildTabPageControl</span><span class="sxs-lookup"><span data-stu-id="0f783-103">Class FormBuildTabPageControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildTabPageControl extends FormBuildControl
```

<span data-ttu-id="0f783-104">FormBuildTabPageControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="0f783-104">The FormBuildTabPageControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f783-105">備考</span><span class="sxs-lookup"><span data-stu-id="0f783-105">Remarks</span></span>

<span data-ttu-id="0f783-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0f783-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="0f783-107">例</span><span class="sxs-lookup"><span data-stu-id="0f783-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="0f783-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="0f783-108">Methods</span></span>

| <span data-ttu-id="0f783-109">方法</span><span class="sxs-lookup"><span data-stu-id="0f783-109">Method</span></span>                                                                                                      | <span data-ttu-id="0f783-110">説明</span><span class="sxs-lookup"><span data-stu-id="0f783-110">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f783-111">public boolean alignChild(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-111">public boolean alignChild(\[boolean value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="0f783-112">public boolean alignChildren(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-112">public boolean alignChildren(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="0f783-113">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-113">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="0f783-114">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-114">Determines whether to align the control.</span></span>                                                                                                |
| <span data-ttu-id="0f783-115">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-115">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="0f783-116">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-116">Determines whether the user can change the contents of the control.</span></span>                                                                     |
| <span data-ttu-id="0f783-117">public int allowUserSetup(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-117">public int allowUserSetup(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="0f783-118">public int arrangeGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-118">public int arrangeGuide(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="0f783-119">public int arrangeMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-119">public int arrangeMethod(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="0f783-120">public int arrangeWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-120">public int arrangeWhen(\[int value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="0f783-121">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-121">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="0f783-122">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-122">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                      |
| <span data-ttu-id="0f783-123">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-123">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="0f783-124">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-124">Gets or sets the background color of the control.</span></span>                                                                                       |
| <span data-ttu-id="0f783-125">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-125">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="0f783-126">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-126">Determines whether the control background can be transparent.</span></span>                                                                           |
| <span data-ttu-id="0f783-127">public int bottomMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0f783-127">public int bottomMargin(\[int value\], \[AutoMode mode\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="0f783-128">public AutoMode bottomMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0f783-128">public AutoMode bottomMarginMode(\[AutoMode mode\])</span></span>                                                         |                                                                                                                                         |
| <span data-ttu-id="0f783-129">public int bottomMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-129">public int bottomMarginValue(\[int value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="0f783-130">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-130">public str caption(\[str value\])</span></span>                                                                           | <span data-ttu-id="0f783-131">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-131">Gets or set the caption of the control.</span></span>                                                                                                 |
| <span data-ttu-id="0f783-132">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-132">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="0f783-133">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-133">Gets or sets the color scheme of the control.</span></span>                                                                                           |
| <span data-ttu-id="0f783-134">public int columns(\[int value\], \[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0f783-134">public int columns(\[int value\], \[ColumnsMode mode\])</span></span>                                                     |                                                                                                                                         |
| <span data-ttu-id="0f783-135">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0f783-135">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span></span>                                                        |                                                                                                                                         |
| <span data-ttu-id="0f783-136">public int columnspace(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0f783-136">public int columnspace(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                         |
| <span data-ttu-id="0f783-137">public AutoMode columnspaceMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0f783-137">public AutoMode columnspaceMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                         |
| <span data-ttu-id="0f783-138">public int columnspaceValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-138">public int columnspaceValue(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="0f783-139">public int columnsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-139">public int columnsValue(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="0f783-140">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-140">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="0f783-141">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-141">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                     |
| <span data-ttu-id="0f783-142">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="0f783-142">public int containerId()</span></span>                                                                                    | <span data-ttu-id="0f783-143">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="0f783-143">Retrieves the ID of the parent container for the control.</span></span>                                                                               |
| <span data-ttu-id="0f783-144">public int containerScrollHorizontalOffset(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-144">public int containerScrollHorizontalOffset(\[int value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="0f783-145">public int containerScrollVerticalOffset(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-145">public int containerScrollVerticalOffset(\[int value\])</span></span>                                                     |                                                                                                                                         |
| <span data-ttu-id="0f783-146">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-146">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="0f783-147">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-147">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                         |
| <span data-ttu-id="0f783-148">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-148">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="0f783-149">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-149">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="0f783-150">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-150">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                |
| <span data-ttu-id="0f783-151">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-151">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="0f783-152">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-152">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="0f783-153">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-153">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                       |
| <span data-ttu-id="0f783-154">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-154">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="0f783-155">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-155">Determines whether to enable or disable the object.</span></span>                                                                                     |
| <span data-ttu-id="0f783-156">public int fastTabExpanded(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-156">public int fastTabExpanded(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="0f783-157">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="0f783-157">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="0f783-158">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-158">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="0f783-159">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-159">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="0f783-160">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-160">Gets or sets a calculation mode for the height of the control.</span></span>                                                                          |
| <span data-ttu-id="0f783-161">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-161">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="0f783-162">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-162">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="0f783-163">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-163">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="0f783-164">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-164">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                |
| <span data-ttu-id="0f783-165">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-165">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                               |                                                                                                                                         |
| <span data-ttu-id="0f783-166">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-166">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="0f783-167">public boolean horizontalScrollBarVisible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-167">public boolean horizontalScrollBarVisible(\[boolean value\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="0f783-168">public int id()</span><span class="sxs-lookup"><span data-stu-id="0f783-168">public int id()</span></span>                                                                                             | <span data-ttu-id="0f783-169">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="0f783-169">Retrieves the ID of the control.</span></span>                                                                                                        |
| <span data-ttu-id="0f783-170">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="0f783-170">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="0f783-171">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0f783-171">Retrieves a value that indicates whether the control is a container control.</span></span>                                                            |
| <span data-ttu-id="0f783-172">public str labelAction(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-172">public str labelAction(\[str value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="0f783-173">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="0f783-173">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="0f783-174">public int leftMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0f783-174">public int leftMargin(\[int value\], \[AutoMode mode\])</span></span>                                                     |                                                                                                                                         |
| <span data-ttu-id="0f783-175">public AutoMode leftMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0f783-175">public AutoMode leftMarginMode(\[AutoMode mode\])</span></span>                                                           |                                                                                                                                         |
| <span data-ttu-id="0f783-176">public int leftMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-176">public int leftMarginValue(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="0f783-177">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-177">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="0f783-178">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-178">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="0f783-179">public int moveControl(int controlId, \[int insertAfterControlId\])</span><span class="sxs-lookup"><span data-stu-id="0f783-179">public int moveControl(int controlId, \[int insertAfterControlId\])</span></span>                                         | <span data-ttu-id="0f783-180">コントロールに指定されたコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="0f783-180">Moves a specified control to the control.</span></span>                                                                                               |
| <span data-ttu-id="0f783-181">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-181">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="0f783-182">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-182">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="0f783-183">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-183">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="0f783-184">public int panelStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-184">public int panelStyle(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="0f783-185">public str parentPage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-185">public str parentPage(\[str value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="0f783-186">public int rightMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0f783-186">public int rightMargin(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                         |
| <span data-ttu-id="0f783-187">public AutoMode rightMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0f783-187">public AutoMode rightMarginMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                         |
| <span data-ttu-id="0f783-188">public int rightMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-188">public int rightMarginValue(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="0f783-189">public int scrollbars(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-189">public int scrollbars(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="0f783-190">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-190">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="0f783-191">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-191">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="0f783-192">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="0f783-192">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>         |
| <span data-ttu-id="0f783-193">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-193">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                         |
| <span data-ttu-id="0f783-194">public int tabAppearance(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-194">public int tabAppearance(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="0f783-195">public boolean tabAutoChange(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-195">public boolean tabAutoChange(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="0f783-196">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="0f783-196">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="0f783-197">public int topMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0f783-197">public int topMargin(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="0f783-198">public AutoMode topMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0f783-198">public AutoMode topMarginMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                         |
| <span data-ttu-id="0f783-199">public int topMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-199">public int topMarginValue(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="0f783-200">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-200">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="0f783-201">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-201">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="0f783-202">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-202">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="0f783-203">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-203">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="0f783-204">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-204">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="0f783-205">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-205">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="0f783-206">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-206">public boolean useUserLayout(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="0f783-207">public boolean verticalScrollBarVisible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-207">public boolean verticalScrollBarVisible(\[boolean value\])</span></span>                                                  |                                                                                                                                         |
| <span data-ttu-id="0f783-208">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0f783-208">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="0f783-209">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="0f783-209">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="0f783-210">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-210">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="0f783-211">public int viewEditMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-211">public int viewEditMode(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="0f783-212">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-212">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="0f783-213">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="0f783-213">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="0f783-214">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-214">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="0f783-215">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-215">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="0f783-216">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-216">Gets or sets the calculation mode of the width of the control.</span></span>                                                                          |
| <span data-ttu-id="0f783-217">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="0f783-217">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="0f783-218">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-218">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="0f783-219">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="0f783-219">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                         |

## <a name="method-alignchild"></a><span data-ttu-id="0f783-220">メソッド alignChild</span><span class="sxs-lookup"><span data-stu-id="0f783-220">Method alignChild</span></span>

```xpp
public boolean alignChild([boolean value])
```

### <a name="parameters---alignchild"></a><span data-ttu-id="0f783-221">パラメーター - alignChild</span><span class="sxs-lookup"><span data-stu-id="0f783-221">Parameters - alignChild</span></span>

<span data-ttu-id="0f783-222">値</span><span class="sxs-lookup"><span data-stu-id="0f783-222">value</span></span>  

### <a name="return-value---alignchild"></a><span data-ttu-id="0f783-223">戻り値 - alignChild</span><span class="sxs-lookup"><span data-stu-id="0f783-223">Return Value - alignChild</span></span>

## <a name="method-alignchildren"></a><span data-ttu-id="0f783-224">メソッド alignChildren</span><span class="sxs-lookup"><span data-stu-id="0f783-224">Method alignChildren</span></span>

```xpp
public boolean alignChildren([boolean value])
```

### <a name="parameters---alignchildren"></a><span data-ttu-id="0f783-225">パラメーター - alignChildren</span><span class="sxs-lookup"><span data-stu-id="0f783-225">Parameters - alignChildren</span></span>

<span data-ttu-id="0f783-226">値</span><span class="sxs-lookup"><span data-stu-id="0f783-226">value</span></span>  

### <a name="return-value---alignchildren"></a><span data-ttu-id="0f783-227">戻り値 - alignChildren</span><span class="sxs-lookup"><span data-stu-id="0f783-227">Return Value - alignChildren</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="0f783-228">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="0f783-228">Method alignControl</span></span>

<span data-ttu-id="0f783-229">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-229">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="0f783-230">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="0f783-230">Parameters - alignControl</span></span>

<span data-ttu-id="0f783-231">値</span><span class="sxs-lookup"><span data-stu-id="0f783-231">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="0f783-232">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="0f783-232">Return Value - alignControl</span></span>

<span data-ttu-id="0f783-233">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="0f783-233">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="0f783-234">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="0f783-234">Remarks - alignControl</span></span>

<span data-ttu-id="0f783-235">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="0f783-235">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="0f783-236">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="0f783-236">Method allowEdit</span></span>

<span data-ttu-id="0f783-237">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-237">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="0f783-238">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="0f783-238">Parameters - allowEdit</span></span>

<span data-ttu-id="0f783-239">値</span><span class="sxs-lookup"><span data-stu-id="0f783-239">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="0f783-240">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="0f783-240">Return Value - allowEdit</span></span>

<span data-ttu-id="0f783-241">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0f783-241">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="0f783-242">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="0f783-242">Remarks - allowEdit</span></span>

<span data-ttu-id="0f783-243">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="0f783-243">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-allowusersetup"></a><span data-ttu-id="0f783-244">メソッド allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="0f783-244">Method allowUserSetup</span></span>

```xpp
public int allowUserSetup([int value])
```

### <a name="parameters---allowusersetup"></a><span data-ttu-id="0f783-245">パラメーター - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="0f783-245">Parameters - allowUserSetup</span></span>

<span data-ttu-id="0f783-246">値</span><span class="sxs-lookup"><span data-stu-id="0f783-246">value</span></span>  

### <a name="return-value---allowusersetup"></a><span data-ttu-id="0f783-247">戻り値 - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="0f783-247">Return Value - allowUserSetup</span></span>

## <a name="method-arrangeguide"></a><span data-ttu-id="0f783-248">メソッド arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="0f783-248">Method arrangeGuide</span></span>

```xpp
public int arrangeGuide([int value])
```

### <a name="parameters---arrangeguide"></a><span data-ttu-id="0f783-249">パラメーター - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="0f783-249">Parameters - arrangeGuide</span></span>

<span data-ttu-id="0f783-250">値</span><span class="sxs-lookup"><span data-stu-id="0f783-250">value</span></span>  

### <a name="return-value---arrangeguide"></a><span data-ttu-id="0f783-251">戻り値 - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="0f783-251">Return Value - arrangeGuide</span></span>

## <a name="method-arrangemethod"></a><span data-ttu-id="0f783-252">メソッド arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="0f783-252">Method arrangeMethod</span></span>

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a><span data-ttu-id="0f783-253">パラメーター - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="0f783-253">Parameters - arrangeMethod</span></span>

<span data-ttu-id="0f783-254">値</span><span class="sxs-lookup"><span data-stu-id="0f783-254">value</span></span>  

### <a name="return-value---arrangemethod"></a><span data-ttu-id="0f783-255">戻り値 - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="0f783-255">Return Value - arrangeMethod</span></span>

## <a name="method-arrangewhen"></a><span data-ttu-id="0f783-256">メソッド arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="0f783-256">Method arrangeWhen</span></span>

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a><span data-ttu-id="0f783-257">パラメーター - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="0f783-257">Parameters - arrangeWhen</span></span>

<span data-ttu-id="0f783-258">値</span><span class="sxs-lookup"><span data-stu-id="0f783-258">value</span></span>  

### <a name="return-value---arrangewhen"></a><span data-ttu-id="0f783-259">戻り値 - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="0f783-259">Return Value - arrangeWhen</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="0f783-260">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="0f783-260">Method autoDeclaration</span></span>

<span data-ttu-id="0f783-261">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-261">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="0f783-262">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="0f783-262">Parameters - autoDeclaration</span></span>

<span data-ttu-id="0f783-263">値</span><span class="sxs-lookup"><span data-stu-id="0f783-263">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="0f783-264">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="0f783-264">Return Value - autoDeclaration</span></span>

<span data-ttu-id="0f783-265">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0f783-265">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="0f783-266">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="0f783-266">Remarks - autoDeclaration</span></span>

<span data-ttu-id="0f783-267">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="0f783-267">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="0f783-268">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="0f783-268">Method backgroundColor</span></span>

<span data-ttu-id="0f783-269">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-269">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="0f783-270">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="0f783-270">Parameters - backgroundColor</span></span>

<span data-ttu-id="0f783-271">値</span><span class="sxs-lookup"><span data-stu-id="0f783-271">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="0f783-272">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="0f783-272">Return Value - backgroundColor</span></span>

<span data-ttu-id="0f783-273">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="0f783-273">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="0f783-274">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="0f783-274">Remarks - backgroundColor</span></span>

<span data-ttu-id="0f783-275">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0f783-275">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="0f783-276">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0f783-276">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="0f783-277">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="0f783-277">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="0f783-278">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="0f783-278">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="0f783-279">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="0f783-279">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="0f783-280">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="0f783-280">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="0f783-281">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="0f783-281">Method backStyle</span></span>

<span data-ttu-id="0f783-282">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-282">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="0f783-283">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="0f783-283">Parameters - backStyle</span></span>

<span data-ttu-id="0f783-284">値</span><span class="sxs-lookup"><span data-stu-id="0f783-284">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="0f783-285">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="0f783-285">Return Value - backStyle</span></span>

<span data-ttu-id="0f783-286">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="0f783-286">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="0f783-287">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="0f783-287">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="0f783-288">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="0f783-288">Parameters - bottomMargin</span></span>

<span data-ttu-id="0f783-289">値</span><span class="sxs-lookup"><span data-stu-id="0f783-289">value</span></span>  

<!-- -->

<span data-ttu-id="0f783-290">モード</span><span class="sxs-lookup"><span data-stu-id="0f783-290">mode</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="0f783-291">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="0f783-291">Return Value - bottomMargin</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="0f783-292">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="0f783-292">Method bottomMarginMode</span></span>

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="0f783-293">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="0f783-293">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="0f783-294">モード</span><span class="sxs-lookup"><span data-stu-id="0f783-294">mode</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="0f783-295">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="0f783-295">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="0f783-296">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="0f783-296">Method bottomMarginValue</span></span>

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="0f783-297">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="0f783-297">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="0f783-298">値</span><span class="sxs-lookup"><span data-stu-id="0f783-298">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="0f783-299">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="0f783-299">Return Value - bottomMarginValue</span></span>

## <a name="method-caption"></a><span data-ttu-id="0f783-300">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="0f783-300">Method caption</span></span>

<span data-ttu-id="0f783-301">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-301">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="0f783-302">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="0f783-302">Parameters - caption</span></span>

<span data-ttu-id="0f783-303">値</span><span class="sxs-lookup"><span data-stu-id="0f783-303">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="0f783-304">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="0f783-304">Return Value - caption</span></span>

<span data-ttu-id="0f783-305">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="0f783-305">The string that is used as the caption of the control.</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="0f783-306">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="0f783-306">Method colorScheme</span></span>

<span data-ttu-id="0f783-307">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-307">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="0f783-308">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="0f783-308">Parameters - colorScheme</span></span>

<span data-ttu-id="0f783-309">値</span><span class="sxs-lookup"><span data-stu-id="0f783-309">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="0f783-310">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="0f783-310">Return Value - colorScheme</span></span>

<span data-ttu-id="0f783-311">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="0f783-311">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="0f783-312">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="0f783-312">Remarks - colorScheme</span></span>

<span data-ttu-id="0f783-313">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="0f783-313">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="0f783-314">値です。</span><span class="sxs-lookup"><span data-stu-id="0f783-314">Value.</span></span> | <span data-ttu-id="0f783-315">スタイル。</span><span class="sxs-lookup"><span data-stu-id="0f783-315">Style.</span></span>                         |
|--------|--------------------------------|
| <span data-ttu-id="0f783-316">0</span><span class="sxs-lookup"><span data-stu-id="0f783-316">0</span></span>      | <span data-ttu-id="0f783-317">既定。</span><span class="sxs-lookup"><span data-stu-id="0f783-317">Default.</span></span>                       |
| <span data-ttu-id="0f783-318">1</span><span class="sxs-lookup"><span data-stu-id="0f783-318">1</span></span>      | <span data-ttu-id="0f783-319">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="0f783-319">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="0f783-320">2</span><span class="sxs-lookup"><span data-stu-id="0f783-320">2</span></span>      | <span data-ttu-id="0f783-321">真の配色。</span><span class="sxs-lookup"><span data-stu-id="0f783-321">The true-color scheme.</span></span>         |

## <a name="method-columns"></a><span data-ttu-id="0f783-322">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="0f783-322">Method columns</span></span>

```xpp
public int columns([int value], [ColumnsMode mode])
```

### <a name="parameters---columns"></a><span data-ttu-id="0f783-323">パラメーター - columns</span><span class="sxs-lookup"><span data-stu-id="0f783-323">Parameters - columns</span></span>

<span data-ttu-id="0f783-324">値</span><span class="sxs-lookup"><span data-stu-id="0f783-324">value</span></span>  

<!-- -->

<span data-ttu-id="0f783-325">モード</span><span class="sxs-lookup"><span data-stu-id="0f783-325">mode</span></span>  

### <a name="return-value---columns"></a><span data-ttu-id="0f783-326">戻り値 - columns</span><span class="sxs-lookup"><span data-stu-id="0f783-326">Return Value - columns</span></span>

## <a name="method-columnsmode"></a><span data-ttu-id="0f783-327">メソッド columnsMode</span><span class="sxs-lookup"><span data-stu-id="0f783-327">Method columnsMode</span></span>

```xpp
public ColumnsMode columnsMode([ColumnsMode mode])
```

### <a name="parameters---columnsmode"></a><span data-ttu-id="0f783-328">パラメーター - columnsMode</span><span class="sxs-lookup"><span data-stu-id="0f783-328">Parameters - columnsMode</span></span>

<span data-ttu-id="0f783-329">モード</span><span class="sxs-lookup"><span data-stu-id="0f783-329">mode</span></span>  

### <a name="return-value---columnsmode"></a><span data-ttu-id="0f783-330">戻り値 - columnsMode</span><span class="sxs-lookup"><span data-stu-id="0f783-330">Return Value - columnsMode</span></span>

## <a name="method-columnspace"></a><span data-ttu-id="0f783-331">メソッド columnspace</span><span class="sxs-lookup"><span data-stu-id="0f783-331">Method columnspace</span></span>

```xpp
public int columnspace([int value], [AutoMode mode])
```

### <a name="parameters---columnspace"></a><span data-ttu-id="0f783-332">パラメーター - columnspace</span><span class="sxs-lookup"><span data-stu-id="0f783-332">Parameters - columnspace</span></span>

<span data-ttu-id="0f783-333">値</span><span class="sxs-lookup"><span data-stu-id="0f783-333">value</span></span>  

<!-- -->

<span data-ttu-id="0f783-334">モード</span><span class="sxs-lookup"><span data-stu-id="0f783-334">mode</span></span>  

### <a name="return-value---columnspace"></a><span data-ttu-id="0f783-335">戻り値 - columnspace</span><span class="sxs-lookup"><span data-stu-id="0f783-335">Return Value - columnspace</span></span>

## <a name="method-columnspacemode"></a><span data-ttu-id="0f783-336">メソッド columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="0f783-336">Method columnspaceMode</span></span>

```xpp
public AutoMode columnspaceMode([AutoMode mode])
```

### <a name="parameters---columnspacemode"></a><span data-ttu-id="0f783-337">パラメーター - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="0f783-337">Parameters - columnspaceMode</span></span>

<span data-ttu-id="0f783-338">モード</span><span class="sxs-lookup"><span data-stu-id="0f783-338">mode</span></span>  

### <a name="return-value---columnspacemode"></a><span data-ttu-id="0f783-339">戻り値 - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="0f783-339">Return Value - columnspaceMode</span></span>

## <a name="method-columnspacevalue"></a><span data-ttu-id="0f783-340">メソッド columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="0f783-340">Method columnspaceValue</span></span>

```xpp
public int columnspaceValue([int value])
```

### <a name="parameters---columnspacevalue"></a><span data-ttu-id="0f783-341">パラメーター - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="0f783-341">Parameters - columnspaceValue</span></span>

<span data-ttu-id="0f783-342">値</span><span class="sxs-lookup"><span data-stu-id="0f783-342">value</span></span>  

### <a name="return-value---columnspacevalue"></a><span data-ttu-id="0f783-343">戻り値 - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="0f783-343">Return Value - columnspaceValue</span></span>

## <a name="method-columnsvalue"></a><span data-ttu-id="0f783-344">メソッド columnsValue</span><span class="sxs-lookup"><span data-stu-id="0f783-344">Method columnsValue</span></span>

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a><span data-ttu-id="0f783-345">パラメーター - columnsValue</span><span class="sxs-lookup"><span data-stu-id="0f783-345">Parameters - columnsValue</span></span>

<span data-ttu-id="0f783-346">値</span><span class="sxs-lookup"><span data-stu-id="0f783-346">value</span></span>  

### <a name="return-value---columnsvalue"></a><span data-ttu-id="0f783-347">戻り値 - columnsValue</span><span class="sxs-lookup"><span data-stu-id="0f783-347">Return Value - columnsValue</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="0f783-348">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="0f783-348">Method configurationKey</span></span>

<span data-ttu-id="0f783-349">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-349">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="0f783-350">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="0f783-350">Parameters - configurationKey</span></span>

<span data-ttu-id="0f783-351">値</span><span class="sxs-lookup"><span data-stu-id="0f783-351">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="0f783-352">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="0f783-352">Return Value - configurationKey</span></span>

<span data-ttu-id="0f783-353">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="0f783-353">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="0f783-354">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="0f783-354">Remarks - configurationKey</span></span>

<span data-ttu-id="0f783-355">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="0f783-355">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="0f783-356">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="0f783-356">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="0f783-357">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="0f783-357">Method containerId</span></span>

<span data-ttu-id="0f783-358">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="0f783-358">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="0f783-359">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="0f783-359">Return Value - containerId</span></span>

<span data-ttu-id="0f783-360">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="0f783-360">The ID of the parent container.</span></span>

## <a name="method-containerscrollhorizontaloffset"></a><span data-ttu-id="0f783-361">メソッド containerScrollHorizontalOffset</span><span class="sxs-lookup"><span data-stu-id="0f783-361">Method containerScrollHorizontalOffset</span></span>

```xpp
public int containerScrollHorizontalOffset([int value])
```

### <a name="parameters---containerscrollhorizontaloffset"></a><span data-ttu-id="0f783-362">パラメーター - containerScrollHorizontalOffset</span><span class="sxs-lookup"><span data-stu-id="0f783-362">Parameters - containerScrollHorizontalOffset</span></span>

<span data-ttu-id="0f783-363">値</span><span class="sxs-lookup"><span data-stu-id="0f783-363">value</span></span>  

### <a name="return-value---containerscrollhorizontaloffset"></a><span data-ttu-id="0f783-364">戻り値 - containerScrollHorizontalOffset</span><span class="sxs-lookup"><span data-stu-id="0f783-364">Return Value - containerScrollHorizontalOffset</span></span>

## <a name="method-containerscrollverticaloffset"></a><span data-ttu-id="0f783-365">メソッド containerScrollVerticalOffset</span><span class="sxs-lookup"><span data-stu-id="0f783-365">Method containerScrollVerticalOffset</span></span>

```xpp
public int containerScrollVerticalOffset([int value])
```

### <a name="parameters---containerscrollverticaloffset"></a><span data-ttu-id="0f783-366">パラメーター - containerScrollVerticalOffset</span><span class="sxs-lookup"><span data-stu-id="0f783-366">Parameters - containerScrollVerticalOffset</span></span>

<span data-ttu-id="0f783-367">値</span><span class="sxs-lookup"><span data-stu-id="0f783-367">value</span></span>  

### <a name="return-value---containerscrollverticaloffset"></a><span data-ttu-id="0f783-368">戻り値 - containerScrollVerticalOffset</span><span class="sxs-lookup"><span data-stu-id="0f783-368">Return Value - containerScrollVerticalOffset</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="0f783-369">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="0f783-369">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="0f783-370">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="0f783-370">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="0f783-371">値</span><span class="sxs-lookup"><span data-stu-id="0f783-371">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="0f783-372">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="0f783-372">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="0f783-373">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="0f783-373">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="0f783-374">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="0f783-374">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="0f783-375">値</span><span class="sxs-lookup"><span data-stu-id="0f783-375">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="0f783-376">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="0f783-376">Return Value - countryRegionContextField</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="0f783-377">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="0f783-377">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="0f783-378">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="0f783-378">Parameters - dataRelationPath</span></span>

<span data-ttu-id="0f783-379">値</span><span class="sxs-lookup"><span data-stu-id="0f783-379">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="0f783-380">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="0f783-380">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="0f783-381">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="0f783-381">Method dataSource</span></span>

<span data-ttu-id="0f783-382">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-382">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="0f783-383">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="0f783-383">Parameters - dataSource</span></span>

<span data-ttu-id="0f783-384">値</span><span class="sxs-lookup"><span data-stu-id="0f783-384">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="0f783-385">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="0f783-385">Return Value - dataSource</span></span>

<span data-ttu-id="0f783-386">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="0f783-386">The identifier of the data source that will be used.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="0f783-387">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="0f783-387">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="0f783-388">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="0f783-388">Parameters - displayTarget</span></span>

<span data-ttu-id="0f783-389">値</span><span class="sxs-lookup"><span data-stu-id="0f783-389">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="0f783-390">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="0f783-390">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="0f783-391">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="0f783-391">Method dragDrop</span></span>

<span data-ttu-id="0f783-392">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-392">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="0f783-393">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="0f783-393">Parameters - dragDrop</span></span>

<span data-ttu-id="0f783-394">値</span><span class="sxs-lookup"><span data-stu-id="0f783-394">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="0f783-395">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="0f783-395">Return Value - dragDrop</span></span>

<span data-ttu-id="0f783-396">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="0f783-396">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="0f783-397">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="0f783-397">Method enabled</span></span>

<span data-ttu-id="0f783-398">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-398">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="0f783-399">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="0f783-399">Parameters - enabled</span></span>

<span data-ttu-id="0f783-400">値</span><span class="sxs-lookup"><span data-stu-id="0f783-400">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="0f783-401">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="0f783-401">Return Value - enabled</span></span>

<span data-ttu-id="0f783-402">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0f783-402">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="0f783-403">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="0f783-403">Remarks - enabled</span></span>

<span data-ttu-id="0f783-404">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="0f783-404">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="0f783-405">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="0f783-405">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="0f783-406">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="0f783-406">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-fasttabexpanded"></a><span data-ttu-id="0f783-407">メソッド fastTabExpanded</span><span class="sxs-lookup"><span data-stu-id="0f783-407">Method fastTabExpanded</span></span>

```xpp
public int fastTabExpanded([int value])
```

### <a name="parameters---fasttabexpanded"></a><span data-ttu-id="0f783-408">パラメーター - fastTabExpanded</span><span class="sxs-lookup"><span data-stu-id="0f783-408">Parameters - fastTabExpanded</span></span>

<span data-ttu-id="0f783-409">値</span><span class="sxs-lookup"><span data-stu-id="0f783-409">value</span></span>  

### <a name="return-value---fasttabexpanded"></a><span data-ttu-id="0f783-410">戻り値 - fastTabExpanded</span><span class="sxs-lookup"><span data-stu-id="0f783-410">Return Value - fastTabExpanded</span></span>

## <a name="method-height"></a><span data-ttu-id="0f783-411">メソッド height</span><span class="sxs-lookup"><span data-stu-id="0f783-411">Method height</span></span>

<span data-ttu-id="0f783-412">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-412">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="0f783-413">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="0f783-413">Parameters - height</span></span>

<span data-ttu-id="0f783-414">値</span><span class="sxs-lookup"><span data-stu-id="0f783-414">value</span></span>  

<!-- -->

<span data-ttu-id="0f783-415">モード</span><span class="sxs-lookup"><span data-stu-id="0f783-415">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="0f783-416">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="0f783-416">Return Value - height</span></span>

<span data-ttu-id="0f783-417">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="0f783-417">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="0f783-418">備考 - height</span><span class="sxs-lookup"><span data-stu-id="0f783-418">Remarks - height</span></span>

<span data-ttu-id="0f783-419">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0f783-419">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="0f783-420">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="0f783-420">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="0f783-421">モード。</span><span class="sxs-lookup"><span data-stu-id="0f783-421">Mode.</span></span>            | <span data-ttu-id="0f783-422">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="0f783-422">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f783-423">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="0f783-423">-1 Exact.</span></span>        | <span data-ttu-id="0f783-424">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0f783-424">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="0f783-425">0 自動。</span><span class="sxs-lookup"><span data-stu-id="0f783-425">0 Auto.</span></span>          | <span data-ttu-id="0f783-426">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="0f783-426">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="0f783-427">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="0f783-427">1 Column height.</span></span> | <span data-ttu-id="0f783-428">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="0f783-428">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="0f783-429">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="0f783-429">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="0f783-430">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="0f783-430">Method heightMode</span></span>

<span data-ttu-id="0f783-431">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-431">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="0f783-432">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="0f783-432">Parameters - heightMode</span></span>

<span data-ttu-id="0f783-433">値</span><span class="sxs-lookup"><span data-stu-id="0f783-433">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="0f783-434">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="0f783-434">Return Value - heightMode</span></span>

<span data-ttu-id="0f783-435">計算モード。</span><span class="sxs-lookup"><span data-stu-id="0f783-435">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="0f783-436">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="0f783-436">Remarks - heightMode</span></span>

<span data-ttu-id="0f783-437">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="0f783-437">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="0f783-438">モード。</span><span class="sxs-lookup"><span data-stu-id="0f783-438">Mode.</span></span>          | <span data-ttu-id="0f783-439">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="0f783-439">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f783-440">正確。</span><span class="sxs-lookup"><span data-stu-id="0f783-440">Exact.</span></span>         | <span data-ttu-id="0f783-441">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0f783-441">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="0f783-442">自動。</span><span class="sxs-lookup"><span data-stu-id="0f783-442">Auto.</span></span>          | <span data-ttu-id="0f783-443">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="0f783-443">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="0f783-444">列の高さ</span><span class="sxs-lookup"><span data-stu-id="0f783-444">Column height.</span></span> | <span data-ttu-id="0f783-445">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="0f783-445">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="0f783-446">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="0f783-446">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="0f783-447">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="0f783-447">Method heightValue</span></span>

<span data-ttu-id="0f783-448">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-448">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="0f783-449">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="0f783-449">Parameters - heightValue</span></span>

<span data-ttu-id="0f783-450">値</span><span class="sxs-lookup"><span data-stu-id="0f783-450">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="0f783-451">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="0f783-451">Return Value - heightValue</span></span>

<span data-ttu-id="0f783-452">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="0f783-452">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="0f783-453">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="0f783-453">Remarks - heightValue</span></span>

<span data-ttu-id="0f783-454">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="0f783-454">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="0f783-455">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="0f783-455">Method helpText</span></span>

<span data-ttu-id="0f783-456">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-456">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="0f783-457">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="0f783-457">Parameters - helpText</span></span>

<span data-ttu-id="0f783-458">値</span><span class="sxs-lookup"><span data-stu-id="0f783-458">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="0f783-459">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="0f783-459">Return Value - helpText</span></span>

<span data-ttu-id="0f783-460">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="0f783-460">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="0f783-461">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="0f783-461">Remarks - helpText</span></span>

<span data-ttu-id="0f783-462">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-462">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="0f783-463">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="0f783-463">The help text must not exceed 250 characters.</span></span>

## <a name="method-hideifempty"></a><span data-ttu-id="0f783-464">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="0f783-464">Method hideIfEmpty</span></span>

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a><span data-ttu-id="0f783-465">パラメーター - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="0f783-465">Parameters - hideIfEmpty</span></span>

<span data-ttu-id="0f783-466">値</span><span class="sxs-lookup"><span data-stu-id="0f783-466">value</span></span>  

### <a name="return-value---hideifempty"></a><span data-ttu-id="0f783-467">戻り値 - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="0f783-467">Return Value - hideIfEmpty</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="0f783-468">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="0f783-468">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="0f783-469">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="0f783-469">Parameters - hierarchyParent</span></span>

<span data-ttu-id="0f783-470">値</span><span class="sxs-lookup"><span data-stu-id="0f783-470">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="0f783-471">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="0f783-471">Return Value - hierarchyParent</span></span>

## <a name="method-horizontalscrollbarvisible"></a><span data-ttu-id="0f783-472">メソッド horizontalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="0f783-472">Method horizontalScrollBarVisible</span></span>

```xpp
public boolean horizontalScrollBarVisible([boolean value])
```

### <a name="parameters---horizontalscrollbarvisible"></a><span data-ttu-id="0f783-473">パラメーター - horizontalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="0f783-473">Parameters - horizontalScrollBarVisible</span></span>

<span data-ttu-id="0f783-474">値</span><span class="sxs-lookup"><span data-stu-id="0f783-474">value</span></span>  

### <a name="return-value---horizontalscrollbarvisible"></a><span data-ttu-id="0f783-475">戻り値 - horizontalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="0f783-475">Return Value - horizontalScrollBarVisible</span></span>

## <a name="method-id"></a><span data-ttu-id="0f783-476">メソッド id</span><span class="sxs-lookup"><span data-stu-id="0f783-476">Method id</span></span>

<span data-ttu-id="0f783-477">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="0f783-477">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="0f783-478">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="0f783-478">Return Value - id</span></span>

<span data-ttu-id="0f783-479">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="0f783-479">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="0f783-480">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="0f783-480">Method isContainer</span></span>

<span data-ttu-id="0f783-481">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="0f783-481">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="0f783-482">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="0f783-482">Return Value - isContainer</span></span>

<span data-ttu-id="0f783-483">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="0f783-483">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-labelaction"></a><span data-ttu-id="0f783-484">メソッド labelAction</span><span class="sxs-lookup"><span data-stu-id="0f783-484">Method labelAction</span></span>

```xpp
public str labelAction([str value])
```

### <a name="parameters---labelaction"></a><span data-ttu-id="0f783-485">パラメーター - labelAction</span><span class="sxs-lookup"><span data-stu-id="0f783-485">Parameters - labelAction</span></span>

<span data-ttu-id="0f783-486">値</span><span class="sxs-lookup"><span data-stu-id="0f783-486">value</span></span>  

### <a name="return-value---labelaction"></a><span data-ttu-id="0f783-487">戻り値 - labelAction</span><span class="sxs-lookup"><span data-stu-id="0f783-487">Return Value - labelAction</span></span>

## <a name="method-left"></a><span data-ttu-id="0f783-488">メソッド left</span><span class="sxs-lookup"><span data-stu-id="0f783-488">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="0f783-489">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="0f783-489">Parameters - left</span></span>

<span data-ttu-id="0f783-490">値</span><span class="sxs-lookup"><span data-stu-id="0f783-490">value</span></span>  

<!-- -->

<span data-ttu-id="0f783-491">モード</span><span class="sxs-lookup"><span data-stu-id="0f783-491">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="0f783-492">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="0f783-492">Return Value - left</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="0f783-493">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="0f783-493">Method leftMargin</span></span>

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="0f783-494">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="0f783-494">Parameters - leftMargin</span></span>

<span data-ttu-id="0f783-495">値</span><span class="sxs-lookup"><span data-stu-id="0f783-495">value</span></span>  

<!-- -->

<span data-ttu-id="0f783-496">モード</span><span class="sxs-lookup"><span data-stu-id="0f783-496">mode</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="0f783-497">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="0f783-497">Return Value - leftMargin</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="0f783-498">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="0f783-498">Method leftMarginMode</span></span>

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="0f783-499">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="0f783-499">Parameters - leftMarginMode</span></span>

<span data-ttu-id="0f783-500">モード</span><span class="sxs-lookup"><span data-stu-id="0f783-500">mode</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="0f783-501">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="0f783-501">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="0f783-502">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="0f783-502">Method leftMarginValue</span></span>

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="0f783-503">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="0f783-503">Parameters - leftMarginValue</span></span>

<span data-ttu-id="0f783-504">値</span><span class="sxs-lookup"><span data-stu-id="0f783-504">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="0f783-505">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="0f783-505">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="0f783-506">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="0f783-506">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="0f783-507">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="0f783-507">Parameters - leftMode</span></span>

<span data-ttu-id="0f783-508">値</span><span class="sxs-lookup"><span data-stu-id="0f783-508">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="0f783-509">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="0f783-509">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="0f783-510">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="0f783-510">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="0f783-511">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="0f783-511">Parameters - leftValue</span></span>

<span data-ttu-id="0f783-512">値</span><span class="sxs-lookup"><span data-stu-id="0f783-512">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="0f783-513">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="0f783-513">Return Value - leftValue</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="0f783-514">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="0f783-514">Method moveControl</span></span>

<span data-ttu-id="0f783-515">コントロールに指定されたコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="0f783-515">Moves a specified control to the control.</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterControlId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="0f783-516">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="0f783-516">Parameters - moveControl</span></span>

<span data-ttu-id="0f783-517">controlId</span><span class="sxs-lookup"><span data-stu-id="0f783-517">controlId</span></span>  

<!-- -->

<span data-ttu-id="0f783-518">insertAfterControlId</span><span class="sxs-lookup"><span data-stu-id="0f783-518">insertAfterControlId</span></span>  

### <a name="return-value---movecontrol"></a><span data-ttu-id="0f783-519">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="0f783-519">Return Value - moveControl</span></span>

<span data-ttu-id="0f783-520">コントロールが正常に移動した場合は 1、それ以外の場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="0f783-520">1 if the control was moved successfully; otherwise, 0.</span></span>

### <a name="remarks---movecontrol"></a><span data-ttu-id="0f783-521">備考 - moveControl</span><span class="sxs-lookup"><span data-stu-id="0f783-521">Remarks - moveControl</span></span>

<span data-ttu-id="0f783-522">一般に、指定したコントロールをコントロールに含めることができ、現在のコンテナーから移動できる場合、このメソッドは成功します。</span><span class="sxs-lookup"><span data-stu-id="0f783-522">In general, if the specified control can be contained in the control and can be moved from the container that it is currently in, this method should succeed.</span></span> <span data-ttu-id="0f783-523">ただし、場合によっては、参照グループ コントロールのインスタンス コントロールなど、コントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="0f783-523">However, in some cases, such as for the reference group control instance, controls cannot be moved.</span></span>

## <a name="method-name"></a><span data-ttu-id="0f783-524">メソッド名</span><span class="sxs-lookup"><span data-stu-id="0f783-524">Method name</span></span>

<span data-ttu-id="0f783-525">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-525">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="0f783-526">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="0f783-526">Parameters - name</span></span>

<span data-ttu-id="0f783-527">値</span><span class="sxs-lookup"><span data-stu-id="0f783-527">value</span></span>  
<span data-ttu-id="0f783-528">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="0f783-528">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="0f783-529">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="0f783-529">Return Value - name</span></span>

<span data-ttu-id="0f783-530">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="0f783-530">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="0f783-531">備考 - name</span><span class="sxs-lookup"><span data-stu-id="0f783-531">Remarks - name</span></span>

<span data-ttu-id="0f783-532">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f783-532">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="0f783-533">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f783-533">It must start with a letter.</span></span>
-   <span data-ttu-id="0f783-534">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="0f783-534">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="0f783-535">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="0f783-535">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="0f783-536">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="0f783-536">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="0f783-537">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="0f783-537">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="0f783-538">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="0f783-538">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="0f783-539">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="0f783-539">Parameters - neededPermission</span></span>

<span data-ttu-id="0f783-540">値</span><span class="sxs-lookup"><span data-stu-id="0f783-540">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="0f783-541">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="0f783-541">Return Value - neededPermission</span></span>

## <a name="method-panelstyle"></a><span data-ttu-id="0f783-542">メソッド panelStyle</span><span class="sxs-lookup"><span data-stu-id="0f783-542">Method panelStyle</span></span>

```xpp
public int panelStyle([int value])
```

### <a name="parameters---panelstyle"></a><span data-ttu-id="0f783-543">パラメーター - panelStyle</span><span class="sxs-lookup"><span data-stu-id="0f783-543">Parameters - panelStyle</span></span>

<span data-ttu-id="0f783-544">値</span><span class="sxs-lookup"><span data-stu-id="0f783-544">value</span></span>  

### <a name="return-value---panelstyle"></a><span data-ttu-id="0f783-545">戻り値 - panelStyle</span><span class="sxs-lookup"><span data-stu-id="0f783-545">Return Value - panelStyle</span></span>

## <a name="method-parentpage"></a><span data-ttu-id="0f783-546">メソッド parentPage</span><span class="sxs-lookup"><span data-stu-id="0f783-546">Method parentPage</span></span>

```xpp
public str parentPage([str value])
```

### <a name="parameters---parentpage"></a><span data-ttu-id="0f783-547">パラメーター - parentPage</span><span class="sxs-lookup"><span data-stu-id="0f783-547">Parameters - parentPage</span></span>

<span data-ttu-id="0f783-548">値</span><span class="sxs-lookup"><span data-stu-id="0f783-548">value</span></span>  

### <a name="return-value---parentpage"></a><span data-ttu-id="0f783-549">戻り値 - parentPage</span><span class="sxs-lookup"><span data-stu-id="0f783-549">Return Value - parentPage</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="0f783-550">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="0f783-550">Method rightMargin</span></span>

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="0f783-551">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="0f783-551">Parameters - rightMargin</span></span>

<span data-ttu-id="0f783-552">値</span><span class="sxs-lookup"><span data-stu-id="0f783-552">value</span></span>  

<!-- -->

<span data-ttu-id="0f783-553">モード</span><span class="sxs-lookup"><span data-stu-id="0f783-553">mode</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="0f783-554">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="0f783-554">Return Value - rightMargin</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="0f783-555">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="0f783-555">Method rightMarginMode</span></span>

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="0f783-556">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="0f783-556">Parameters - rightMarginMode</span></span>

<span data-ttu-id="0f783-557">モード</span><span class="sxs-lookup"><span data-stu-id="0f783-557">mode</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="0f783-558">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="0f783-558">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="0f783-559">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="0f783-559">Method rightMarginValue</span></span>

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="0f783-560">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="0f783-560">Parameters - rightMarginValue</span></span>

<span data-ttu-id="0f783-561">値</span><span class="sxs-lookup"><span data-stu-id="0f783-561">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="0f783-562">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="0f783-562">Return Value - rightMarginValue</span></span>

## <a name="method-scrollbars"></a><span data-ttu-id="0f783-563">メソッド scrollbars</span><span class="sxs-lookup"><span data-stu-id="0f783-563">Method scrollbars</span></span>

```xpp
public int scrollbars([int value])
```

### <a name="parameters---scrollbars"></a><span data-ttu-id="0f783-564">パラメーター - scrollbars</span><span class="sxs-lookup"><span data-stu-id="0f783-564">Parameters - scrollbars</span></span>

<span data-ttu-id="0f783-565">値</span><span class="sxs-lookup"><span data-stu-id="0f783-565">value</span></span>  

### <a name="return-value---scrollbars"></a><span data-ttu-id="0f783-566">戻り値 - scrollbars</span><span class="sxs-lookup"><span data-stu-id="0f783-566">Return Value - scrollbars</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="0f783-567">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="0f783-567">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="0f783-568">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="0f783-568">Parameters - securityKey</span></span>

<span data-ttu-id="0f783-569">値</span><span class="sxs-lookup"><span data-stu-id="0f783-569">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="0f783-570">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="0f783-570">Return Value - securityKey</span></span>

## <a name="method-skip"></a><span data-ttu-id="0f783-571">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="0f783-571">Method skip</span></span>

<span data-ttu-id="0f783-572">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="0f783-572">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="0f783-573">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="0f783-573">Parameters - skip</span></span>

<span data-ttu-id="0f783-574">値</span><span class="sxs-lookup"><span data-stu-id="0f783-574">value</span></span>  
<span data-ttu-id="0f783-575">コントロールの skip プロパティに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="0f783-575">The value to assign to the skip property of the control; optional.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="0f783-576">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="0f783-576">Return Value - skip</span></span>

<span data-ttu-id="0f783-577">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="0f783-577">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-style"></a><span data-ttu-id="0f783-578">メソッド style</span><span class="sxs-lookup"><span data-stu-id="0f783-578">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="0f783-579">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="0f783-579">Parameters - style</span></span>

<span data-ttu-id="0f783-580">値</span><span class="sxs-lookup"><span data-stu-id="0f783-580">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="0f783-581">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="0f783-581">Return Value - style</span></span>

## <a name="method-tabappearance"></a><span data-ttu-id="0f783-582">メソッド tabAppearance</span><span class="sxs-lookup"><span data-stu-id="0f783-582">Method tabAppearance</span></span>

```xpp
public int tabAppearance([int value])
```

### <a name="parameters---tabappearance"></a><span data-ttu-id="0f783-583">パラメーター - tabAppearance</span><span class="sxs-lookup"><span data-stu-id="0f783-583">Parameters - tabAppearance</span></span>

<span data-ttu-id="0f783-584">値</span><span class="sxs-lookup"><span data-stu-id="0f783-584">value</span></span>  

### <a name="return-value---tabappearance"></a><span data-ttu-id="0f783-585">戻り値 - tabAppearance</span><span class="sxs-lookup"><span data-stu-id="0f783-585">Return Value - tabAppearance</span></span>

## <a name="method-tabautochange"></a><span data-ttu-id="0f783-586">メソッド tabAutoChange</span><span class="sxs-lookup"><span data-stu-id="0f783-586">Method tabAutoChange</span></span>

```xpp
public boolean tabAutoChange([boolean value])
```

### <a name="parameters---tabautochange"></a><span data-ttu-id="0f783-587">パラメーター - tabAutoChange</span><span class="sxs-lookup"><span data-stu-id="0f783-587">Parameters - tabAutoChange</span></span>

<span data-ttu-id="0f783-588">値</span><span class="sxs-lookup"><span data-stu-id="0f783-588">value</span></span>  

### <a name="return-value---tabautochange"></a><span data-ttu-id="0f783-589">戻り値 - tabAutoChange</span><span class="sxs-lookup"><span data-stu-id="0f783-589">Return Value - tabAutoChange</span></span>

## <a name="method-top"></a><span data-ttu-id="0f783-590">メソッド top</span><span class="sxs-lookup"><span data-stu-id="0f783-590">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="0f783-591">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="0f783-591">Parameters - top</span></span>

<span data-ttu-id="0f783-592">値</span><span class="sxs-lookup"><span data-stu-id="0f783-592">value</span></span>  

<!-- -->

<span data-ttu-id="0f783-593">モード</span><span class="sxs-lookup"><span data-stu-id="0f783-593">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="0f783-594">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="0f783-594">Return Value - top</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="0f783-595">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="0f783-595">Method topMargin</span></span>

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="0f783-596">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="0f783-596">Parameters - topMargin</span></span>

<span data-ttu-id="0f783-597">値</span><span class="sxs-lookup"><span data-stu-id="0f783-597">value</span></span>  

<!-- -->

<span data-ttu-id="0f783-598">モード</span><span class="sxs-lookup"><span data-stu-id="0f783-598">mode</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="0f783-599">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="0f783-599">Return Value - topMargin</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="0f783-600">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="0f783-600">Method topMarginMode</span></span>

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="0f783-601">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="0f783-601">Parameters - topMarginMode</span></span>

<span data-ttu-id="0f783-602">モード</span><span class="sxs-lookup"><span data-stu-id="0f783-602">mode</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="0f783-603">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="0f783-603">Return Value - topMarginMode</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="0f783-604">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="0f783-604">Method topMarginValue</span></span>

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="0f783-605">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="0f783-605">Parameters - topMarginValue</span></span>

<span data-ttu-id="0f783-606">値</span><span class="sxs-lookup"><span data-stu-id="0f783-606">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="0f783-607">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="0f783-607">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="0f783-608">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="0f783-608">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="0f783-609">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="0f783-609">Parameters - topMode</span></span>

<span data-ttu-id="0f783-610">値</span><span class="sxs-lookup"><span data-stu-id="0f783-610">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="0f783-611">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="0f783-611">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="0f783-612">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="0f783-612">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="0f783-613">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="0f783-613">Parameters - topValue</span></span>

<span data-ttu-id="0f783-614">値</span><span class="sxs-lookup"><span data-stu-id="0f783-614">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="0f783-615">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="0f783-615">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="0f783-616">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="0f783-616">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="0f783-617">パラメーター - type</span><span class="sxs-lookup"><span data-stu-id="0f783-617">Parameters - type</span></span>

<span data-ttu-id="0f783-618">値</span><span class="sxs-lookup"><span data-stu-id="0f783-618">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="0f783-619">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="0f783-619">Return Value - type</span></span>

## <a name="method-userdata"></a><span data-ttu-id="0f783-620">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="0f783-620">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="0f783-621">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="0f783-621">Parameters - userData</span></span>

<span data-ttu-id="0f783-622">値</span><span class="sxs-lookup"><span data-stu-id="0f783-622">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="0f783-623">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="0f783-623">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="0f783-624">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="0f783-624">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="0f783-625">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="0f783-625">Parameters - userDataItem</span></span>

<span data-ttu-id="0f783-626">値</span><span class="sxs-lookup"><span data-stu-id="0f783-626">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="0f783-627">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="0f783-627">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="0f783-628">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="0f783-628">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="0f783-629">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="0f783-629">Parameters - userDataItems</span></span>

<span data-ttu-id="0f783-630">値</span><span class="sxs-lookup"><span data-stu-id="0f783-630">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="0f783-631">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="0f783-631">Return Value - userDataItems</span></span>

## <a name="method-useuserlayout"></a><span data-ttu-id="0f783-632">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="0f783-632">Method useUserLayout</span></span>

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a><span data-ttu-id="0f783-633">パラメーター - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="0f783-633">Parameters - useUserLayout</span></span>

<span data-ttu-id="0f783-634">値</span><span class="sxs-lookup"><span data-stu-id="0f783-634">value</span></span>  

### <a name="return-value---useuserlayout"></a><span data-ttu-id="0f783-635">戻り値 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="0f783-635">Return Value - useUserLayout</span></span>

## <a name="method-verticalscrollbarvisible"></a><span data-ttu-id="0f783-636">メソッド verticalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="0f783-636">Method verticalScrollBarVisible</span></span>

```xpp
public boolean verticalScrollBarVisible([boolean value])
```

### <a name="parameters---verticalscrollbarvisible"></a><span data-ttu-id="0f783-637">パラメーター - verticalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="0f783-637">Parameters - verticalScrollBarVisible</span></span>

<span data-ttu-id="0f783-638">値</span><span class="sxs-lookup"><span data-stu-id="0f783-638">value</span></span>  

### <a name="return-value---verticalscrollbarvisible"></a><span data-ttu-id="0f783-639">戻り値 - verticalScrollBarVisible</span><span class="sxs-lookup"><span data-stu-id="0f783-639">Return Value - verticalScrollBarVisible</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="0f783-640">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="0f783-640">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="0f783-641">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="0f783-641">Parameters - verticalSpacing</span></span>

<span data-ttu-id="0f783-642">値</span><span class="sxs-lookup"><span data-stu-id="0f783-642">value</span></span>  

<!-- -->

<span data-ttu-id="0f783-643">モード</span><span class="sxs-lookup"><span data-stu-id="0f783-643">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="0f783-644">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="0f783-644">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="0f783-645">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="0f783-645">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="0f783-646">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="0f783-646">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="0f783-647">モード</span><span class="sxs-lookup"><span data-stu-id="0f783-647">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="0f783-648">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="0f783-648">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="0f783-649">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="0f783-649">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="0f783-650">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="0f783-650">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="0f783-651">値</span><span class="sxs-lookup"><span data-stu-id="0f783-651">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="0f783-652">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="0f783-652">Return Value - verticalSpacingValue</span></span>

## <a name="method-vieweditmode"></a><span data-ttu-id="0f783-653">メソッド viewEditMode</span><span class="sxs-lookup"><span data-stu-id="0f783-653">Method viewEditMode</span></span>

```xpp
public int viewEditMode([int value])
```

### <a name="parameters---vieweditmode"></a><span data-ttu-id="0f783-654">パラメーター - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="0f783-654">Parameters - viewEditMode</span></span>

<span data-ttu-id="0f783-655">値</span><span class="sxs-lookup"><span data-stu-id="0f783-655">value</span></span>  

### <a name="return-value---vieweditmode"></a><span data-ttu-id="0f783-656">戻り値 - viewEditMode</span><span class="sxs-lookup"><span data-stu-id="0f783-656">Return Value - viewEditMode</span></span>

## <a name="method-visible"></a><span data-ttu-id="0f783-657">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="0f783-657">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="0f783-658">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="0f783-658">Parameters - visible</span></span>

<span data-ttu-id="0f783-659">値</span><span class="sxs-lookup"><span data-stu-id="0f783-659">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="0f783-660">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="0f783-660">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="0f783-661">メソッド width</span><span class="sxs-lookup"><span data-stu-id="0f783-661">Method width</span></span>

<span data-ttu-id="0f783-662">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-662">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="0f783-663">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="0f783-663">Parameters - width</span></span>

<span data-ttu-id="0f783-664">値</span><span class="sxs-lookup"><span data-stu-id="0f783-664">value</span></span>  

<!-- -->

<span data-ttu-id="0f783-665">モード</span><span class="sxs-lookup"><span data-stu-id="0f783-665">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="0f783-666">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="0f783-666">Return Value - width</span></span>

<span data-ttu-id="0f783-667">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="0f783-667">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="0f783-668">備考 - width</span><span class="sxs-lookup"><span data-stu-id="0f783-668">Remarks - width</span></span>

<span data-ttu-id="0f783-669">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0f783-669">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="0f783-670">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="0f783-670">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="0f783-671">モード。</span><span class="sxs-lookup"><span data-stu-id="0f783-671">Mode.</span></span>           | <span data-ttu-id="0f783-672">幅計算。</span><span class="sxs-lookup"><span data-stu-id="0f783-672">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f783-673">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="0f783-673">-1 Exact.</span></span>       | <span data-ttu-id="0f783-674">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="0f783-674">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="0f783-675">0 自動。</span><span class="sxs-lookup"><span data-stu-id="0f783-675">0 Auto.</span></span>         | <span data-ttu-id="0f783-676">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="0f783-676">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="0f783-677">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="0f783-677">1 Column width.</span></span> | <span data-ttu-id="0f783-678">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="0f783-678">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="0f783-679">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="0f783-679">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="0f783-680">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="0f783-680">Method widthMode</span></span>

<span data-ttu-id="0f783-681">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-681">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="0f783-682">パラメーター - widthMode</span><span class="sxs-lookup"><span data-stu-id="0f783-682">Parameters - widthMode</span></span>

<span data-ttu-id="0f783-683">値</span><span class="sxs-lookup"><span data-stu-id="0f783-683">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="0f783-684">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="0f783-684">Return Value - widthMode</span></span>

<span data-ttu-id="0f783-685">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="0f783-685">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="0f783-686">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="0f783-686">Remarks - widthMode</span></span>

<span data-ttu-id="0f783-687">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="0f783-687">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="0f783-688">モード。</span><span class="sxs-lookup"><span data-stu-id="0f783-688">Mode.</span></span>         | <span data-ttu-id="0f783-689">幅計算。</span><span class="sxs-lookup"><span data-stu-id="0f783-689">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f783-690">正確。</span><span class="sxs-lookup"><span data-stu-id="0f783-690">Exact.</span></span>        | <span data-ttu-id="0f783-691">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="0f783-691">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="0f783-692">自動。</span><span class="sxs-lookup"><span data-stu-id="0f783-692">Auto.</span></span>         | <span data-ttu-id="0f783-693">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="0f783-693">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="0f783-694">列の幅。</span><span class="sxs-lookup"><span data-stu-id="0f783-694">Column width.</span></span> | <span data-ttu-id="0f783-695">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="0f783-695">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="0f783-696">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="0f783-696">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="0f783-697">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="0f783-697">Method widthValue</span></span>

<span data-ttu-id="0f783-698">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="0f783-698">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="0f783-699">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="0f783-699">Parameters - widthValue</span></span>

<span data-ttu-id="0f783-700">値</span><span class="sxs-lookup"><span data-stu-id="0f783-700">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="0f783-701">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="0f783-701">Return Value - widthValue</span></span>

<span data-ttu-id="0f783-702">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="0f783-702">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="0f783-703">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="0f783-703">Remarks - widthValue</span></span>

<span data-ttu-id="0f783-704">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="0f783-704">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="0f783-705">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="0f783-705">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="0f783-706">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="0f783-706">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="0f783-707">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="0f783-707">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="0f783-708">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="0f783-708">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="0f783-709">overrideObject</span><span class="sxs-lookup"><span data-stu-id="0f783-709">overrideObject</span></span>  

