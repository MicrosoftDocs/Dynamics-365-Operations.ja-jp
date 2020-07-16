---
title: FormBuildGridControl クラス
description: このトピックでは、FormBuildGridControl クラスについて説明します。
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
ms.openlocfilehash: 3fefdb87b796dae58808384fa29ef632bb89d82c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502647"
---
# <a name="class-formbuildgridcontrol"></a><span data-ttu-id="4d026-103">クラス FormBuildGridControl</span><span class="sxs-lookup"><span data-stu-id="4d026-103">Class FormBuildGridControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildGridControl extends FormBuildControl
```

<span data-ttu-id="4d026-104">FormBuildGridControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="4d026-104">The FormBuildGridControl class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d026-105">備考</span><span class="sxs-lookup"><span data-stu-id="4d026-105">Remarks</span></span>

<span data-ttu-id="4d026-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4d026-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="4d026-107">例</span><span class="sxs-lookup"><span data-stu-id="4d026-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="4d026-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="4d026-108">Methods</span></span>

| <span data-ttu-id="4d026-109">方法</span><span class="sxs-lookup"><span data-stu-id="4d026-109">Method</span></span>                                                                                                      | <span data-ttu-id="4d026-110">説明</span><span class="sxs-lookup"><span data-stu-id="4d026-110">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d026-111">public int activeBackColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-111">public int activeBackColor(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="4d026-112">public int activeForeColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-112">public int activeForeColor(\[int value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="4d026-113">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-113">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="4d026-114">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-114">Determines whether to align the control.</span></span>                                                                                                |
| <span data-ttu-id="4d026-115">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-115">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="4d026-116">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-116">Determines whether the user can change the contents of the control.</span></span>                                                                     |
| <span data-ttu-id="4d026-117">public int alternateRowShading(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-117">public int alternateRowShading(\[int value\])</span></span>                                                               |                                                                                                                                         |
| <span data-ttu-id="4d026-118">public boolean autoDataGroup(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-118">public boolean autoDataGroup(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="4d026-119">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-119">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="4d026-120">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-120">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                      |
| <span data-ttu-id="4d026-121">public int backgroundColor(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-121">public int backgroundColor(\[int value\])</span></span>                                                                   | <span data-ttu-id="4d026-122">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-122">Gets or sets the background color of the control.</span></span>                                                                                       |
| <span data-ttu-id="4d026-123">public int backStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-123">public int backStyle(\[int value\])</span></span>                                                                         | <span data-ttu-id="4d026-124">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-124">Determines whether the control background can be transparent.</span></span>                                                                          |
| <span data-ttu-id="4d026-125">public int border(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-125">public int border(\[int value\])</span></span>                                                                            | <span data-ttu-id="4d026-126">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-126">Gets or sets the style of the borderline of the control.</span></span>                                                                                |
| <span data-ttu-id="4d026-127">public int bottomMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-127">public int bottomMargin(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="4d026-128">public int colorScheme(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-128">public int colorScheme(\[int value\])</span></span>                                                                       | <span data-ttu-id="4d026-129">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-129">Gets or sets the color scheme of the control.</span></span>                                                                                           |
| <span data-ttu-id="4d026-130">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-130">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="4d026-131">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-131">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                     |
| <span data-ttu-id="4d026-132">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="4d026-132">public int containerId()</span></span>                                                                                    | <span data-ttu-id="4d026-133">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="4d026-133">Retrieves the ID of the parent container for the control.</span></span>                                                                               |
| <span data-ttu-id="4d026-134">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-134">public str countryRegionCodes(\[str value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="4d026-135">public FieldId countryRegionContextField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-135">public FieldId countryRegionContextField(\[FieldId value\])</span></span>                                                 |                                                                                                                                         |
| <span data-ttu-id="4d026-136">public str dataGroup(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-136">public str dataGroup(\[str value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="4d026-137">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-137">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="4d026-138">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-138">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="4d026-139">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-139">Gets or sets a data source that is used by the control or the form.</span></span>                                                                     |
| <span data-ttu-id="4d026-140">public str defaultAction(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-140">public str defaultAction(\[str value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="4d026-141">public str defaultActionLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-141">public str defaultActionLabel(\[str value\])</span></span>                                                                |                                                                                                                                         |
| <span data-ttu-id="4d026-142">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-142">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="4d026-143">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-143">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="4d026-144">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-144">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                       |
| <span data-ttu-id="4d026-145">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-145">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="4d026-146">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-146">Determines whether to enable or disable the object.</span></span>                                                                                     |
| <span data-ttu-id="4d026-147">public boolean exportAllowed(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-147">public boolean exportAllowed(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="4d026-148">public str exportLabel(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-148">public str exportLabel(\[str value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="4d026-149">public boolean gridLines(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-149">public boolean gridLines(\[boolean value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="4d026-150">public int gridLinesStyle(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-150">public int gridLinesStyle(\[int value\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="4d026-151">public str groupBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-151">public str groupBy(\[str value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="4d026-152">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="4d026-152">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="4d026-153">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-153">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="4d026-154">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-154">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="4d026-155">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-155">Gets or sets a calculation mode for the height of the control.</span></span>                                                                          |
| <span data-ttu-id="4d026-156">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-156">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="4d026-157">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-157">Gets or sets the height of the control.</span></span>                                                                                                 |
| <span data-ttu-id="4d026-158">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-158">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="4d026-159">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-159">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                |
| <span data-ttu-id="4d026-160">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-160">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="4d026-161">public boolean highlightActive(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-161">public boolean highlightActive(\[boolean value\])</span></span>                                                           |                                                                                                                                         |
| <span data-ttu-id="4d026-162">public int id()</span><span class="sxs-lookup"><span data-stu-id="4d026-162">public int id()</span></span>                                                                                             | <span data-ttu-id="4d026-163">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="4d026-163">Retrieves the ID of the control.</span></span>                                                                                                        |
| <span data-ttu-id="4d026-164">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="4d026-164">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="4d026-165">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="4d026-165">Retrieves a value that indicates whether the control is a container control.</span></span>                                                            |
| <span data-ttu-id="4d026-166">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="4d026-166">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                         |
| <span data-ttu-id="4d026-167">public int leftMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-167">public int leftMargin(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="4d026-168">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-168">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="4d026-169">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-169">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="4d026-170">public int moreRowsIndicator(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-170">public int moreRowsIndicator(\[int value\])</span></span>                                                                 |                                                                                                                                         |
| <span data-ttu-id="4d026-171">public int moveControl(int controlId, \[int insertAfterControlId\])</span><span class="sxs-lookup"><span data-stu-id="4d026-171">public int moveControl(int controlId, \[int insertAfterControlId\])</span></span>                                         | <span data-ttu-id="4d026-172">コントロールに指定されたコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="4d026-172">Moves a specified control to the control.</span></span>                                                                                               |
| <span data-ttu-id="4d026-173">public boolean multiSelect(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-173">public boolean multiSelect(\[boolean value\])</span></span>                                                               |                                                                                                                                         |
| <span data-ttu-id="4d026-174">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-174">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="4d026-175">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-175">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="4d026-176">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-176">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="4d026-177">public int rightMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-177">public int rightMargin(\[int value\])</span></span>                                                                       |                                                                                                                                         |
| <span data-ttu-id="4d026-178">public int scrollbars(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-178">public int scrollbars(\[int value\])</span></span>                                                                        |                                                                                                                                         |
| <span data-ttu-id="4d026-179">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-179">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                         |
| <span data-ttu-id="4d026-180">public boolean showColLabels(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-180">public boolean showColLabels(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="4d026-181">public boolean showRowLabels(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-181">public boolean showRowLabels(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="4d026-182">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-182">public boolean skip(\[boolean value\])</span></span>                                                                      | <span data-ttu-id="4d026-183">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="4d026-183">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>         |
| <span data-ttu-id="4d026-184">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-184">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                         |
| <span data-ttu-id="4d026-185">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="4d026-185">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="4d026-186">public int topMargin(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-186">public int topMargin(\[int value\])</span></span>                                                                         |                                                                                                                                         |
| <span data-ttu-id="4d026-187">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-187">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                         |
| <span data-ttu-id="4d026-188">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-188">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="4d026-189">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-189">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                         |
| <span data-ttu-id="4d026-190">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-190">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                         |
| <span data-ttu-id="4d026-191">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-191">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                         |
| <span data-ttu-id="4d026-192">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-192">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                         |
| <span data-ttu-id="4d026-193">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-193">public boolean useUserLayout(\[boolean value\])</span></span>                                                             |                                                                                                                                         |
| <span data-ttu-id="4d026-194">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4d026-194">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                         |
| <span data-ttu-id="4d026-195">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4d026-195">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                         |
| <span data-ttu-id="4d026-196">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-196">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                         |
| <span data-ttu-id="4d026-197">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-197">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                         |
| <span data-ttu-id="4d026-198">public int visibleCols(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4d026-198">public int visibleCols(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                         |
| <span data-ttu-id="4d026-199">public AutoMode visibleColsMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4d026-199">public AutoMode visibleColsMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                         |
| <span data-ttu-id="4d026-200">public int visibleColsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-200">public int visibleColsValue(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="4d026-201">public int visibleRows(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4d026-201">public int visibleRows(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                         |
| <span data-ttu-id="4d026-202">public AutoMode visibleRowsMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="4d026-202">public AutoMode visibleRowsMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                         |
| <span data-ttu-id="4d026-203">public int visibleRowsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-203">public int visibleRowsValue(\[int value\])</span></span>                                                                  |                                                                                                                                         |
| <span data-ttu-id="4d026-204">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="4d026-204">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="4d026-205">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-205">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="4d026-206">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-206">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="4d026-207">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-207">Gets or sets the calculation mode of the width of the control.</span></span>                                                                          |
| <span data-ttu-id="4d026-208">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="4d026-208">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="4d026-209">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-209">Gets or sets the width of the control.</span></span>                                                                                                  |
| <span data-ttu-id="4d026-210">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="4d026-210">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                         |

## <a name="method-activebackcolor"></a><span data-ttu-id="4d026-211">メソッド activeBackColor</span><span class="sxs-lookup"><span data-stu-id="4d026-211">Method activeBackColor</span></span>

```xpp
public int activeBackColor([int value])
```

### <a name="parameters---activebackcolor"></a><span data-ttu-id="4d026-212">パラメーター - activeBackColor</span><span class="sxs-lookup"><span data-stu-id="4d026-212">Parameters - activeBackColor</span></span>

<span data-ttu-id="4d026-213">値</span><span class="sxs-lookup"><span data-stu-id="4d026-213">value</span></span>  

### <a name="return-value---activebackcolor"></a><span data-ttu-id="4d026-214">戻り値 - activeBackColor</span><span class="sxs-lookup"><span data-stu-id="4d026-214">Return Value - activeBackColor</span></span>

## <a name="method-activeforecolor"></a><span data-ttu-id="4d026-215">メソッド activeForeColor</span><span class="sxs-lookup"><span data-stu-id="4d026-215">Method activeForeColor</span></span>

```xpp
public int activeForeColor([int value])
```

### <a name="parameters---activeforecolor"></a><span data-ttu-id="4d026-216">パラメーター - activeForeColor</span><span class="sxs-lookup"><span data-stu-id="4d026-216">Parameters - activeForeColor</span></span>

<span data-ttu-id="4d026-217">値</span><span class="sxs-lookup"><span data-stu-id="4d026-217">value</span></span>  

### <a name="return-value---activeforecolor"></a><span data-ttu-id="4d026-218">戻り値 - activeForeColor</span><span class="sxs-lookup"><span data-stu-id="4d026-218">Return Value - activeForeColor</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="4d026-219">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="4d026-219">Method alignControl</span></span>

<span data-ttu-id="4d026-220">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-220">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="4d026-221">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="4d026-221">Parameters - alignControl</span></span>

<span data-ttu-id="4d026-222">値</span><span class="sxs-lookup"><span data-stu-id="4d026-222">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="4d026-223">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="4d026-223">Return Value - alignControl</span></span>

<span data-ttu-id="4d026-224">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="4d026-224">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="4d026-225">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="4d026-225">Remarks - alignControl</span></span>

<span data-ttu-id="4d026-226">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="4d026-226">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="4d026-227">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="4d026-227">Method allowEdit</span></span>

<span data-ttu-id="4d026-228">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-228">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="4d026-229">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="4d026-229">Parameters - allowEdit</span></span>

<span data-ttu-id="4d026-230">値</span><span class="sxs-lookup"><span data-stu-id="4d026-230">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="4d026-231">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="4d026-231">Return Value - allowEdit</span></span>

<span data-ttu-id="4d026-232">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="4d026-232">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="4d026-233">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="4d026-233">Remarks - allowEdit</span></span>

<span data-ttu-id="4d026-234">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="4d026-234">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-alternaterowshading"></a><span data-ttu-id="4d026-235">メソッド alternateRowShading</span><span class="sxs-lookup"><span data-stu-id="4d026-235">Method alternateRowShading</span></span>

```xpp
public int alternateRowShading([int value])
```

### <a name="parameters---alternaterowshading"></a><span data-ttu-id="4d026-236">パラメーター - alternateRowShading</span><span class="sxs-lookup"><span data-stu-id="4d026-236">Parameters - alternateRowShading</span></span>

<span data-ttu-id="4d026-237">値</span><span class="sxs-lookup"><span data-stu-id="4d026-237">value</span></span>  

### <a name="return-value---alternaterowshading"></a><span data-ttu-id="4d026-238">戻り値 - alternateRowShading</span><span class="sxs-lookup"><span data-stu-id="4d026-238">Return Value - alternateRowShading</span></span>

## <a name="method-autodatagroup"></a><span data-ttu-id="4d026-239">メソッド autoDataGroup</span><span class="sxs-lookup"><span data-stu-id="4d026-239">Method autoDataGroup</span></span>

```xpp
public boolean autoDataGroup([boolean value])
```

### <a name="parameters---autodatagroup"></a><span data-ttu-id="4d026-240">パラメーター - autoDataGroup</span><span class="sxs-lookup"><span data-stu-id="4d026-240">Parameters - autoDataGroup</span></span>

<span data-ttu-id="4d026-241">値</span><span class="sxs-lookup"><span data-stu-id="4d026-241">value</span></span>  

### <a name="return-value---autodatagroup"></a><span data-ttu-id="4d026-242">戻り値 - autoDataGroup</span><span class="sxs-lookup"><span data-stu-id="4d026-242">Return Value - autoDataGroup</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="4d026-243">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="4d026-243">Method autoDeclaration</span></span>

<span data-ttu-id="4d026-244">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-244">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="4d026-245">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="4d026-245">Parameters - autoDeclaration</span></span>

<span data-ttu-id="4d026-246">値</span><span class="sxs-lookup"><span data-stu-id="4d026-246">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="4d026-247">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="4d026-247">Return Value - autoDeclaration</span></span>

<span data-ttu-id="4d026-248">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="4d026-248">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="4d026-249">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="4d026-249">Remarks - autoDeclaration</span></span>

<span data-ttu-id="4d026-250">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="4d026-250">Controls cannot have identical names.</span></span>

## <a name="method-backgroundcolor"></a><span data-ttu-id="4d026-251">メソッド backgroundColor</span><span class="sxs-lookup"><span data-stu-id="4d026-251">Method backgroundColor</span></span>

<span data-ttu-id="4d026-252">コントロールの背景色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-252">Gets or sets the background color of the control.</span></span>

```xpp
public int backgroundColor([int value])
```

### <a name="parameters---backgroundcolor"></a><span data-ttu-id="4d026-253">パラメーター - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="4d026-253">Parameters - backgroundColor</span></span>

<span data-ttu-id="4d026-254">値</span><span class="sxs-lookup"><span data-stu-id="4d026-254">value</span></span>  

### <a name="return-value---backgroundcolor"></a><span data-ttu-id="4d026-255">戻り値 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="4d026-255">Return Value - backgroundColor</span></span>

<span data-ttu-id="4d026-256">パックされた RGB カラーを含む整数。</span><span class="sxs-lookup"><span data-stu-id="4d026-256">An integer that contains a packed RGB color.</span></span>

### <a name="remarks---backgroundcolor"></a><span data-ttu-id="4d026-257">備考 - backgroundColor</span><span class="sxs-lookup"><span data-stu-id="4d026-257">Remarks - backgroundColor</span></span>

<span data-ttu-id="4d026-258">返される整数には、次のようにパックされた RGB カラーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4d026-258">The integer that is returned contains a packed RGB color as follows:</span></span>

-   <span data-ttu-id="4d026-259">下位バイトには赤の相対強度の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4d026-259">The low-order byte contains a value for the relative intensity of red.</span></span>
-   <span data-ttu-id="4d026-260">2 番目のバイトには緑の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="4d026-260">The second byte contains a value for green.</span></span>
-   <span data-ttu-id="4d026-261">3 番目のバイトには青の値が入っています。</span><span class="sxs-lookup"><span data-stu-id="4d026-261">The third byte contains a value for blue.</span></span>
-   <span data-ttu-id="4d026-262">上位バイトはゼロでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="4d026-262">The high-order byte must be zero.</span></span>
-   <span data-ttu-id="4d026-263">1 バイトの最大値は 255 です。</span><span class="sxs-lookup"><span data-stu-id="4d026-263">The maximum value for a single byte is 255.</span></span>

## <a name="method-backstyle"></a><span data-ttu-id="4d026-264">メソッド backStyle</span><span class="sxs-lookup"><span data-stu-id="4d026-264">Method backStyle</span></span>

<span data-ttu-id="4d026-265">コントロールの背景色を透明にできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-265">Determines whether the control background can be transparent.</span></span>

```xpp
public int backStyle([int value])
```

### <a name="parameters---backstyle"></a><span data-ttu-id="4d026-266">パラメーター - backStyle</span><span class="sxs-lookup"><span data-stu-id="4d026-266">Parameters - backStyle</span></span>

<span data-ttu-id="4d026-267">値</span><span class="sxs-lookup"><span data-stu-id="4d026-267">value</span></span>  

### <a name="return-value---backstyle"></a><span data-ttu-id="4d026-268">戻り値 - backStyle</span><span class="sxs-lookup"><span data-stu-id="4d026-268">Return Value - backStyle</span></span>

<span data-ttu-id="4d026-269">コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="4d026-269">1 if the control background can be transparent; otherwise, 0.</span></span>

## <a name="method-border"></a><span data-ttu-id="4d026-270">メソッド border</span><span class="sxs-lookup"><span data-stu-id="4d026-270">Method border</span></span>

<span data-ttu-id="4d026-271">コントロールの境界線のスタイルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-271">Gets or sets the style of the borderline of the control.</span></span>

```xpp
public int border([int value])
```

### <a name="parameters---border"></a><span data-ttu-id="4d026-272">パラメーター - border</span><span class="sxs-lookup"><span data-stu-id="4d026-272">Parameters - border</span></span>

<span data-ttu-id="4d026-273">値</span><span class="sxs-lookup"><span data-stu-id="4d026-273">value</span></span>  

### <a name="return-value---border"></a><span data-ttu-id="4d026-274">戻り値 - border</span><span class="sxs-lookup"><span data-stu-id="4d026-274">Return Value - border</span></span>

<span data-ttu-id="4d026-275">ゼロから 4 までの整数。</span><span class="sxs-lookup"><span data-stu-id="4d026-275">An integer between zero and four, inclusive.</span></span>

### <a name="remarks---border"></a><span data-ttu-id="4d026-276">備考 - border</span><span class="sxs-lookup"><span data-stu-id="4d026-276">Remarks - border</span></span>

<span data-ttu-id="4d026-277">返される整数には、次のようなコントロールの境界線のスタイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4d026-277">The integer that is returned contains the style of the borderline of the control as follows:</span></span>

| <span data-ttu-id="4d026-278">値です。</span><span class="sxs-lookup"><span data-stu-id="4d026-278">Value.</span></span> | <span data-ttu-id="4d026-279">説明。</span><span class="sxs-lookup"><span data-stu-id="4d026-279">Description.</span></span> |
|--------|--------------|
| <span data-ttu-id="4d026-280">0</span><span class="sxs-lookup"><span data-stu-id="4d026-280">0</span></span>      | <span data-ttu-id="4d026-281">自動。</span><span class="sxs-lookup"><span data-stu-id="4d026-281">Auto.</span></span>        |
| <span data-ttu-id="4d026-282">1</span><span class="sxs-lookup"><span data-stu-id="4d026-282">1</span></span>      | <span data-ttu-id="4d026-283">3D。</span><span class="sxs-lookup"><span data-stu-id="4d026-283">3D.</span></span>          |
| <span data-ttu-id="4d026-284">2</span><span class="sxs-lookup"><span data-stu-id="4d026-284">2</span></span>      | <span data-ttu-id="4d026-285">単一明細行。</span><span class="sxs-lookup"><span data-stu-id="4d026-285">Single line.</span></span> |
| <span data-ttu-id="4d026-286">3</span><span class="sxs-lookup"><span data-stu-id="4d026-286">3</span></span>      | <span data-ttu-id="4d026-287">均一。</span><span class="sxs-lookup"><span data-stu-id="4d026-287">Flat.</span></span>        |
| <span data-ttu-id="4d026-288">4</span><span class="sxs-lookup"><span data-stu-id="4d026-288">4</span></span>      | <span data-ttu-id="4d026-289">なし。</span><span class="sxs-lookup"><span data-stu-id="4d026-289">None.</span></span>        |

## <a name="method-bottommargin"></a><span data-ttu-id="4d026-290">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="4d026-290">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="4d026-291">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="4d026-291">Parameters - bottomMargin</span></span>

<span data-ttu-id="4d026-292">値</span><span class="sxs-lookup"><span data-stu-id="4d026-292">value</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="4d026-293">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="4d026-293">Return Value - bottomMargin</span></span>

## <a name="method-colorscheme"></a><span data-ttu-id="4d026-294">メソッド colorScheme</span><span class="sxs-lookup"><span data-stu-id="4d026-294">Method colorScheme</span></span>

<span data-ttu-id="4d026-295">コントロールの配色を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-295">Gets or sets the color scheme of the control.</span></span>

```xpp
public int colorScheme([int value])
```

### <a name="parameters---colorscheme"></a><span data-ttu-id="4d026-296">パラメーター - colorScheme</span><span class="sxs-lookup"><span data-stu-id="4d026-296">Parameters - colorScheme</span></span>

<span data-ttu-id="4d026-297">値</span><span class="sxs-lookup"><span data-stu-id="4d026-297">value</span></span>  

### <a name="return-value---colorscheme"></a><span data-ttu-id="4d026-298">戻り値 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="4d026-298">Return Value - colorScheme</span></span>

<span data-ttu-id="4d026-299">ゼロから 2 までの整数。</span><span class="sxs-lookup"><span data-stu-id="4d026-299">An integer between zero and two, inclusive.</span></span>

### <a name="remarks---colorscheme"></a><span data-ttu-id="4d026-300">備考 - colorScheme</span><span class="sxs-lookup"><span data-stu-id="4d026-300">Remarks - colorScheme</span></span>

<span data-ttu-id="4d026-301">配色は次の表に従って定義されます。</span><span class="sxs-lookup"><span data-stu-id="4d026-301">The color scheme is defined according to the following table:</span></span>

| <span data-ttu-id="4d026-302">値です。</span><span class="sxs-lookup"><span data-stu-id="4d026-302">Value.</span></span> | <span data-ttu-id="4d026-303">スタイル。</span><span class="sxs-lookup"><span data-stu-id="4d026-303">Style.</span></span>                        |
|--------|-------------------------------|
| <span data-ttu-id="4d026-304">0</span><span class="sxs-lookup"><span data-stu-id="4d026-304">0</span></span>      | <span data-ttu-id="4d026-305">既定。</span><span class="sxs-lookup"><span data-stu-id="4d026-305">Default.</span></span>                      |
| <span data-ttu-id="4d026-306">1</span><span class="sxs-lookup"><span data-stu-id="4d026-306">1</span></span>      | <span data-ttu-id="4d026-307">Microsoft Windows パレット。</span><span class="sxs-lookup"><span data-stu-id="4d026-307">The Microsoft Windows palette.</span></span> |
| <span data-ttu-id="4d026-308">2</span><span class="sxs-lookup"><span data-stu-id="4d026-308">2</span></span>      | <span data-ttu-id="4d026-309">真の配色。</span><span class="sxs-lookup"><span data-stu-id="4d026-309">The true-color scheme.</span></span>        |

## <a name="method-configurationkey"></a><span data-ttu-id="4d026-310">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="4d026-310">Method configurationKey</span></span>

<span data-ttu-id="4d026-311">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-311">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="4d026-312">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="4d026-312">Parameters - configurationKey</span></span>

<span data-ttu-id="4d026-313">値</span><span class="sxs-lookup"><span data-stu-id="4d026-313">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="4d026-314">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="4d026-314">Return Value - configurationKey</span></span>

<span data-ttu-id="4d026-315">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="4d026-315">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="4d026-316">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="4d026-316">Remarks - configurationKey</span></span>

<span data-ttu-id="4d026-317">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4d026-317">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="4d026-318">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="4d026-318">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="4d026-319">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="4d026-319">Method containerId</span></span>

<span data-ttu-id="4d026-320">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="4d026-320">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="4d026-321">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="4d026-321">Return Value - containerId</span></span>

<span data-ttu-id="4d026-322">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="4d026-322">The ID of the parent container.</span></span>

## <a name="method-countryregioncodes"></a><span data-ttu-id="4d026-323">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="4d026-323">Method countryRegionCodes</span></span>

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a><span data-ttu-id="4d026-324">パラメーター - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="4d026-324">Parameters - countryRegionCodes</span></span>

<span data-ttu-id="4d026-325">値</span><span class="sxs-lookup"><span data-stu-id="4d026-325">value</span></span>  

### <a name="return-value---countryregioncodes"></a><span data-ttu-id="4d026-326">戻り値 - countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="4d026-326">Return Value - countryRegionCodes</span></span>

## <a name="method-countryregioncontextfield"></a><span data-ttu-id="4d026-327">メソッド countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="4d026-327">Method countryRegionContextField</span></span>

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a><span data-ttu-id="4d026-328">パラメーター - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="4d026-328">Parameters - countryRegionContextField</span></span>

<span data-ttu-id="4d026-329">値</span><span class="sxs-lookup"><span data-stu-id="4d026-329">value</span></span>  

### <a name="return-value---countryregioncontextfield"></a><span data-ttu-id="4d026-330">戻り値 - countryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="4d026-330">Return Value - countryRegionContextField</span></span>

## <a name="method-datagroup"></a><span data-ttu-id="4d026-331">メソッド dataGroup</span><span class="sxs-lookup"><span data-stu-id="4d026-331">Method dataGroup</span></span>

```xpp
public str dataGroup([str value])
```

### <a name="parameters---datagroup"></a><span data-ttu-id="4d026-332">パラメーター - dataGroup</span><span class="sxs-lookup"><span data-stu-id="4d026-332">Parameters - dataGroup</span></span>

<span data-ttu-id="4d026-333">値</span><span class="sxs-lookup"><span data-stu-id="4d026-333">value</span></span>  

### <a name="return-value---datagroup"></a><span data-ttu-id="4d026-334">戻り値 - dataGroup</span><span class="sxs-lookup"><span data-stu-id="4d026-334">Return Value - dataGroup</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="4d026-335">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="4d026-335">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="4d026-336">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="4d026-336">Parameters - dataRelationPath</span></span>

<span data-ttu-id="4d026-337">値</span><span class="sxs-lookup"><span data-stu-id="4d026-337">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="4d026-338">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="4d026-338">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="4d026-339">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="4d026-339">Method dataSource</span></span>

<span data-ttu-id="4d026-340">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-340">Gets or sets a data source that is used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="4d026-341">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="4d026-341">Parameters - dataSource</span></span>

<span data-ttu-id="4d026-342">値</span><span class="sxs-lookup"><span data-stu-id="4d026-342">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="4d026-343">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="4d026-343">Return Value - dataSource</span></span>

<span data-ttu-id="4d026-344">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="4d026-344">The identifier of the data source to use.</span></span>

## <a name="method-defaultaction"></a><span data-ttu-id="4d026-345">メソッド defaultAction</span><span class="sxs-lookup"><span data-stu-id="4d026-345">Method defaultAction</span></span>

```xpp
public str defaultAction([str value])
```

### <a name="parameters---defaultaction"></a><span data-ttu-id="4d026-346">パラメーター - defaultAction</span><span class="sxs-lookup"><span data-stu-id="4d026-346">Parameters - defaultAction</span></span>

<span data-ttu-id="4d026-347">値</span><span class="sxs-lookup"><span data-stu-id="4d026-347">value</span></span>  

### <a name="return-value---defaultaction"></a><span data-ttu-id="4d026-348">戻り値 - defaultAction</span><span class="sxs-lookup"><span data-stu-id="4d026-348">Return Value - defaultAction</span></span>

## <a name="method-defaultactionlabel"></a><span data-ttu-id="4d026-349">メソッド defaultActionLabel</span><span class="sxs-lookup"><span data-stu-id="4d026-349">Method defaultActionLabel</span></span>

```xpp
public str defaultActionLabel([str value])
```

### <a name="parameters---defaultactionlabel"></a><span data-ttu-id="4d026-350">パラメーター - defaultActionLabel</span><span class="sxs-lookup"><span data-stu-id="4d026-350">Parameters - defaultActionLabel</span></span>

<span data-ttu-id="4d026-351">値</span><span class="sxs-lookup"><span data-stu-id="4d026-351">value</span></span>  

### <a name="return-value---defaultactionlabel"></a><span data-ttu-id="4d026-352">戻り値 - defaultActionLabel</span><span class="sxs-lookup"><span data-stu-id="4d026-352">Return Value - defaultActionLabel</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="4d026-353">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="4d026-353">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="4d026-354">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="4d026-354">Parameters - displayTarget</span></span>

<span data-ttu-id="4d026-355">値</span><span class="sxs-lookup"><span data-stu-id="4d026-355">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="4d026-356">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="4d026-356">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="4d026-357">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="4d026-357">Method dragDrop</span></span>

<span data-ttu-id="4d026-358">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-358">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="4d026-359">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="4d026-359">Parameters - dragDrop</span></span>

<span data-ttu-id="4d026-360">値</span><span class="sxs-lookup"><span data-stu-id="4d026-360">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="4d026-361">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="4d026-361">Return Value - dragDrop</span></span>

<span data-ttu-id="4d026-362">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="4d026-362">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="4d026-363">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="4d026-363">Method enabled</span></span>

<span data-ttu-id="4d026-364">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-364">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="4d026-365">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="4d026-365">Parameters - enabled</span></span>

<span data-ttu-id="4d026-366">値</span><span class="sxs-lookup"><span data-stu-id="4d026-366">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="4d026-367">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="4d026-367">Return Value - enabled</span></span>

<span data-ttu-id="4d026-368">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="4d026-368">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="4d026-369">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="4d026-369">Remarks - enabled</span></span>

<span data-ttu-id="4d026-370">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="4d026-370">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="4d026-371">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="4d026-371">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="4d026-372">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="4d026-372">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-exportallowed"></a><span data-ttu-id="4d026-373">メソッド exportAllowed</span><span class="sxs-lookup"><span data-stu-id="4d026-373">Method exportAllowed</span></span>

```xpp
public boolean exportAllowed([boolean value])
```

### <a name="parameters---exportallowed"></a><span data-ttu-id="4d026-374">パラメーター - exportAllowed</span><span class="sxs-lookup"><span data-stu-id="4d026-374">Parameters - exportAllowed</span></span>

<span data-ttu-id="4d026-375">値</span><span class="sxs-lookup"><span data-stu-id="4d026-375">value</span></span>  

### <a name="return-value---exportallowed"></a><span data-ttu-id="4d026-376">戻り値 - exportAllowed</span><span class="sxs-lookup"><span data-stu-id="4d026-376">Return Value - exportAllowed</span></span>

## <a name="method-exportlabel"></a><span data-ttu-id="4d026-377">メソッド exportLabel</span><span class="sxs-lookup"><span data-stu-id="4d026-377">Method exportLabel</span></span>

```xpp
public str exportLabel([str value])
```

### <a name="parameters---exportlabel"></a><span data-ttu-id="4d026-378">パラメーター - exportLabel</span><span class="sxs-lookup"><span data-stu-id="4d026-378">Parameters - exportLabel</span></span>

<span data-ttu-id="4d026-379">値</span><span class="sxs-lookup"><span data-stu-id="4d026-379">value</span></span>  

### <a name="return-value---exportlabel"></a><span data-ttu-id="4d026-380">戻り値 - exportLabel</span><span class="sxs-lookup"><span data-stu-id="4d026-380">Return Value - exportLabel</span></span>

## <a name="method-gridlines"></a><span data-ttu-id="4d026-381">メソッド gridLines</span><span class="sxs-lookup"><span data-stu-id="4d026-381">Method gridLines</span></span>

```xpp
public boolean gridLines([boolean value])
```

### <a name="parameters---gridlines"></a><span data-ttu-id="4d026-382">パラメーター - gridLines</span><span class="sxs-lookup"><span data-stu-id="4d026-382">Parameters - gridLines</span></span>

<span data-ttu-id="4d026-383">値</span><span class="sxs-lookup"><span data-stu-id="4d026-383">value</span></span>  

### <a name="return-value---gridlines"></a><span data-ttu-id="4d026-384">戻り値 - gridLines</span><span class="sxs-lookup"><span data-stu-id="4d026-384">Return Value - gridLines</span></span>

## <a name="method-gridlinesstyle"></a><span data-ttu-id="4d026-385">メソッド gridLinesStyle</span><span class="sxs-lookup"><span data-stu-id="4d026-385">Method gridLinesStyle</span></span>

```xpp
public int gridLinesStyle([int value])
```

### <a name="parameters---gridlinesstyle"></a><span data-ttu-id="4d026-386">パラメーター - gridLinesStyle</span><span class="sxs-lookup"><span data-stu-id="4d026-386">Parameters - gridLinesStyle</span></span>

<span data-ttu-id="4d026-387">値</span><span class="sxs-lookup"><span data-stu-id="4d026-387">value</span></span>  

### <a name="return-value---gridlinesstyle"></a><span data-ttu-id="4d026-388">戻り値 - gridLinesStyle</span><span class="sxs-lookup"><span data-stu-id="4d026-388">Return Value - gridLinesStyle</span></span>

## <a name="method-groupby"></a><span data-ttu-id="4d026-389">メソッド groupBy</span><span class="sxs-lookup"><span data-stu-id="4d026-389">Method groupBy</span></span>

```xpp
public str groupBy([str value])
```

### <a name="parameters---groupby"></a><span data-ttu-id="4d026-390">パラメーター - groupBy</span><span class="sxs-lookup"><span data-stu-id="4d026-390">Parameters - groupBy</span></span>

<span data-ttu-id="4d026-391">値</span><span class="sxs-lookup"><span data-stu-id="4d026-391">value</span></span>  

### <a name="return-value---groupby"></a><span data-ttu-id="4d026-392">戻り値 - groupBy</span><span class="sxs-lookup"><span data-stu-id="4d026-392">Return Value - groupBy</span></span>

## <a name="method-height"></a><span data-ttu-id="4d026-393">メソッド height</span><span class="sxs-lookup"><span data-stu-id="4d026-393">Method height</span></span>

<span data-ttu-id="4d026-394">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-394">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="4d026-395">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="4d026-395">Parameters - height</span></span>

<span data-ttu-id="4d026-396">値</span><span class="sxs-lookup"><span data-stu-id="4d026-396">value</span></span>  

<!-- -->

<span data-ttu-id="4d026-397">モード</span><span class="sxs-lookup"><span data-stu-id="4d026-397">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="4d026-398">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="4d026-398">Return Value - height</span></span>

<span data-ttu-id="4d026-399">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="4d026-399">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="4d026-400">備考 - height</span><span class="sxs-lookup"><span data-stu-id="4d026-400">Remarks - height</span></span>

<span data-ttu-id="4d026-401">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="4d026-401">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="4d026-402">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="4d026-402">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="4d026-403">モード。</span><span class="sxs-lookup"><span data-stu-id="4d026-403">Mode.</span></span>            | <span data-ttu-id="4d026-404">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="4d026-404">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d026-405">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="4d026-405">-1 Exact.</span></span>        | <span data-ttu-id="4d026-406">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="4d026-406">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="4d026-407">0 自動。</span><span class="sxs-lookup"><span data-stu-id="4d026-407">0 Auto.</span></span>          | <span data-ttu-id="4d026-408">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="4d026-408">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="4d026-409">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="4d026-409">1 Column height.</span></span> | <span data-ttu-id="4d026-410">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="4d026-410">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="4d026-411">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="4d026-411">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="4d026-412">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="4d026-412">Method heightMode</span></span>

<span data-ttu-id="4d026-413">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-413">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="4d026-414">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="4d026-414">Parameters - heightMode</span></span>

<span data-ttu-id="4d026-415">値</span><span class="sxs-lookup"><span data-stu-id="4d026-415">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="4d026-416">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="4d026-416">Return Value - heightMode</span></span>

<span data-ttu-id="4d026-417">計算モード。</span><span class="sxs-lookup"><span data-stu-id="4d026-417">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="4d026-418">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="4d026-418">Remarks - heightMode</span></span>

<span data-ttu-id="4d026-419">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="4d026-419">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="4d026-420">モード。</span><span class="sxs-lookup"><span data-stu-id="4d026-420">Mode.</span></span>          | <span data-ttu-id="4d026-421">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="4d026-421">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d026-422">正確。</span><span class="sxs-lookup"><span data-stu-id="4d026-422">Exact.</span></span>         | <span data-ttu-id="4d026-423">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="4d026-423">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="4d026-424">自動。</span><span class="sxs-lookup"><span data-stu-id="4d026-424">Auto.</span></span>          | <span data-ttu-id="4d026-425">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="4d026-425">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="4d026-426">列の高さ</span><span class="sxs-lookup"><span data-stu-id="4d026-426">Column height.</span></span> | <span data-ttu-id="4d026-427">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="4d026-427">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="4d026-428">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="4d026-428">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="4d026-429">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="4d026-429">Method heightValue</span></span>

<span data-ttu-id="4d026-430">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-430">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="4d026-431">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="4d026-431">Parameters - heightValue</span></span>

<span data-ttu-id="4d026-432">値</span><span class="sxs-lookup"><span data-stu-id="4d026-432">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="4d026-433">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="4d026-433">Return Value - heightValue</span></span>

<span data-ttu-id="4d026-434">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="4d026-434">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="4d026-435">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="4d026-435">Remarks - heightValue</span></span>

<span data-ttu-id="4d026-436">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="4d026-436">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="4d026-437">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="4d026-437">Method helpText</span></span>

<span data-ttu-id="4d026-438">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-438">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="4d026-439">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="4d026-439">Parameters - helpText</span></span>

<span data-ttu-id="4d026-440">値</span><span class="sxs-lookup"><span data-stu-id="4d026-440">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="4d026-441">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="4d026-441">Return Value - helpText</span></span>

<span data-ttu-id="4d026-442">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="4d026-442">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="4d026-443">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="4d026-443">Remarks - helpText</span></span>

<span data-ttu-id="4d026-444">プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-444">Set the HelpText property for an object by using the property sheet.</span></span> <span data-ttu-id="4d026-445">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="4d026-445">The help text must not exceed 250 characters.</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="4d026-446">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="4d026-446">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="4d026-447">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="4d026-447">Parameters - hierarchyParent</span></span>

<span data-ttu-id="4d026-448">値</span><span class="sxs-lookup"><span data-stu-id="4d026-448">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="4d026-449">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="4d026-449">Return Value - hierarchyParent</span></span>

## <a name="method-highlightactive"></a><span data-ttu-id="4d026-450">メソッド highlightActive</span><span class="sxs-lookup"><span data-stu-id="4d026-450">Method highlightActive</span></span>

```xpp
public boolean highlightActive([boolean value])
```

### <a name="parameters---highlightactive"></a><span data-ttu-id="4d026-451">パラメーター - highlightActive</span><span class="sxs-lookup"><span data-stu-id="4d026-451">Parameters - highlightActive</span></span>

<span data-ttu-id="4d026-452">値</span><span class="sxs-lookup"><span data-stu-id="4d026-452">value</span></span>  

### <a name="return-value---highlightactive"></a><span data-ttu-id="4d026-453">戻り値 - highlightActive</span><span class="sxs-lookup"><span data-stu-id="4d026-453">Return Value - highlightActive</span></span>

## <a name="method-id"></a><span data-ttu-id="4d026-454">メソッド id</span><span class="sxs-lookup"><span data-stu-id="4d026-454">Method id</span></span>

<span data-ttu-id="4d026-455">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="4d026-455">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="4d026-456">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="4d026-456">Return Value - id</span></span>

<span data-ttu-id="4d026-457">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="4d026-457">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="4d026-458">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="4d026-458">Method isContainer</span></span>

<span data-ttu-id="4d026-459">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="4d026-459">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="4d026-460">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="4d026-460">Return Value - isContainer</span></span>

<span data-ttu-id="4d026-461">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="4d026-461">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-left"></a><span data-ttu-id="4d026-462">メソッド left</span><span class="sxs-lookup"><span data-stu-id="4d026-462">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="4d026-463">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="4d026-463">Parameters - left</span></span>

<span data-ttu-id="4d026-464">値</span><span class="sxs-lookup"><span data-stu-id="4d026-464">value</span></span>  

<!-- -->

<span data-ttu-id="4d026-465">モード</span><span class="sxs-lookup"><span data-stu-id="4d026-465">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="4d026-466">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="4d026-466">Return Value - left</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="4d026-467">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="4d026-467">Method leftMargin</span></span>

```xpp
public int leftMargin([int value])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="4d026-468">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="4d026-468">Parameters - leftMargin</span></span>

<span data-ttu-id="4d026-469">値</span><span class="sxs-lookup"><span data-stu-id="4d026-469">value</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="4d026-470">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="4d026-470">Return Value - leftMargin</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="4d026-471">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="4d026-471">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="4d026-472">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="4d026-472">Parameters - leftMode</span></span>

<span data-ttu-id="4d026-473">値</span><span class="sxs-lookup"><span data-stu-id="4d026-473">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="4d026-474">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="4d026-474">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="4d026-475">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="4d026-475">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="4d026-476">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="4d026-476">Parameters - leftValue</span></span>

<span data-ttu-id="4d026-477">値</span><span class="sxs-lookup"><span data-stu-id="4d026-477">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="4d026-478">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="4d026-478">Return Value - leftValue</span></span>

## <a name="method-morerowsindicator"></a><span data-ttu-id="4d026-479">メソッド moreRowsIndicator</span><span class="sxs-lookup"><span data-stu-id="4d026-479">Method moreRowsIndicator</span></span>

```xpp
public int moreRowsIndicator([int value])
```

### <a name="parameters---morerowsindicator"></a><span data-ttu-id="4d026-480">パラメーター - moreRowsIndicator</span><span class="sxs-lookup"><span data-stu-id="4d026-480">Parameters - moreRowsIndicator</span></span>

<span data-ttu-id="4d026-481">値</span><span class="sxs-lookup"><span data-stu-id="4d026-481">value</span></span>  

### <a name="return-value---morerowsindicator"></a><span data-ttu-id="4d026-482">戻り値 - moreRowsIndicator</span><span class="sxs-lookup"><span data-stu-id="4d026-482">Return Value - moreRowsIndicator</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="4d026-483">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="4d026-483">Method moveControl</span></span>

<span data-ttu-id="4d026-484">コントロールに指定されたコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="4d026-484">Moves a specified control to the control.</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterControlId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="4d026-485">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="4d026-485">Parameters - moveControl</span></span>

<span data-ttu-id="4d026-486">controlId</span><span class="sxs-lookup"><span data-stu-id="4d026-486">controlId</span></span>  

<!-- -->

<span data-ttu-id="4d026-487">insertAfterControlId</span><span class="sxs-lookup"><span data-stu-id="4d026-487">insertAfterControlId</span></span>  

### <a name="return-value---movecontrol"></a><span data-ttu-id="4d026-488">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="4d026-488">Return Value - moveControl</span></span>

<span data-ttu-id="4d026-489">コントロールが正常に移動した場合は 1、それ以外の場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="4d026-489">1 if the control was moved successfully; otherwise, 0.</span></span>

### <a name="remarks---movecontrol"></a><span data-ttu-id="4d026-490">備考 - moveControl</span><span class="sxs-lookup"><span data-stu-id="4d026-490">Remarks - moveControl</span></span>

<span data-ttu-id="4d026-491">一般に、指定したコントロールをコントロールに含めることができ、現在のコンテナーから移動できる場合、このメソッドは成功します。</span><span class="sxs-lookup"><span data-stu-id="4d026-491">In general, if the specified control can be contained in the control and can be moved from the container that it is currently in, this method should succeed.</span></span> <span data-ttu-id="4d026-492">ただし、場合によっては、参照グループ コントロールのインスタンス コントロールなど、コントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="4d026-492">However, in some cases, such as for the reference group control instance, controls cannot be moved.</span></span>

## <a name="method-multiselect"></a><span data-ttu-id="4d026-493">メソッド multiSelect</span><span class="sxs-lookup"><span data-stu-id="4d026-493">Method multiSelect</span></span>

```xpp
public boolean multiSelect([boolean value])
```

### <a name="parameters---multiselect"></a><span data-ttu-id="4d026-494">パラメーター - multiSelect</span><span class="sxs-lookup"><span data-stu-id="4d026-494">Parameters - multiSelect</span></span>

<span data-ttu-id="4d026-495">値</span><span class="sxs-lookup"><span data-stu-id="4d026-495">value</span></span>  

### <a name="return-value---multiselect"></a><span data-ttu-id="4d026-496">戻り値 - multiSelect</span><span class="sxs-lookup"><span data-stu-id="4d026-496">Return Value - multiSelect</span></span>

## <a name="method-name"></a><span data-ttu-id="4d026-497">メソッド名</span><span class="sxs-lookup"><span data-stu-id="4d026-497">Method name</span></span>

<span data-ttu-id="4d026-498">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-498">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="4d026-499">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="4d026-499">Parameters - name</span></span>

<span data-ttu-id="4d026-500">値</span><span class="sxs-lookup"><span data-stu-id="4d026-500">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="4d026-501">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="4d026-501">Return Value - name</span></span>

<span data-ttu-id="4d026-502">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="4d026-502">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="4d026-503">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="4d026-503">Remarks - name</span></span>

<span data-ttu-id="4d026-504">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4d026-504">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="4d026-505">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="4d026-505">It must start with a letter.</span></span>
-   <span data-ttu-id="4d026-506">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="4d026-506">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="4d026-507">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="4d026-507">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="4d026-508">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="4d026-508">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="4d026-509">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="4d026-509">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, or classes.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="4d026-510">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="4d026-510">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="4d026-511">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="4d026-511">Parameters - neededPermission</span></span>

<span data-ttu-id="4d026-512">値</span><span class="sxs-lookup"><span data-stu-id="4d026-512">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="4d026-513">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="4d026-513">Return Value - neededPermission</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="4d026-514">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="4d026-514">Method rightMargin</span></span>

```xpp
public int rightMargin([int value])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="4d026-515">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="4d026-515">Parameters - rightMargin</span></span>

<span data-ttu-id="4d026-516">値</span><span class="sxs-lookup"><span data-stu-id="4d026-516">value</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="4d026-517">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="4d026-517">Return Value - rightMargin</span></span>

## <a name="method-scrollbars"></a><span data-ttu-id="4d026-518">メソッド scrollbars</span><span class="sxs-lookup"><span data-stu-id="4d026-518">Method scrollbars</span></span>

```xpp
public int scrollbars([int value])
```

### <a name="parameters---scrollbars"></a><span data-ttu-id="4d026-519">パラメーター - scrollbars</span><span class="sxs-lookup"><span data-stu-id="4d026-519">Parameters - scrollbars</span></span>

<span data-ttu-id="4d026-520">値</span><span class="sxs-lookup"><span data-stu-id="4d026-520">value</span></span>  

### <a name="return-value---scrollbars"></a><span data-ttu-id="4d026-521">戻り値 - scrollbars</span><span class="sxs-lookup"><span data-stu-id="4d026-521">Return Value - scrollbars</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="4d026-522">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="4d026-522">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="4d026-523">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="4d026-523">Parameters - securityKey</span></span>

<span data-ttu-id="4d026-524">値</span><span class="sxs-lookup"><span data-stu-id="4d026-524">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="4d026-525">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="4d026-525">Return Value - securityKey</span></span>

## <a name="method-showcollabels"></a><span data-ttu-id="4d026-526">メソッド showColLabels</span><span class="sxs-lookup"><span data-stu-id="4d026-526">Method showColLabels</span></span>

```xpp
public boolean showColLabels([boolean value])
```

### <a name="parameters---showcollabels"></a><span data-ttu-id="4d026-527">パラメーター - showColLabels</span><span class="sxs-lookup"><span data-stu-id="4d026-527">Parameters - showColLabels</span></span>

<span data-ttu-id="4d026-528">値</span><span class="sxs-lookup"><span data-stu-id="4d026-528">value</span></span>  

### <a name="return-value---showcollabels"></a><span data-ttu-id="4d026-529">戻り値 - showColLabels</span><span class="sxs-lookup"><span data-stu-id="4d026-529">Return Value - showColLabels</span></span>

## <a name="method-showrowlabels"></a><span data-ttu-id="4d026-530">メソッド showRowLabels</span><span class="sxs-lookup"><span data-stu-id="4d026-530">Method showRowLabels</span></span>

```xpp
public boolean showRowLabels([boolean value])
```

### <a name="parameters---showrowlabels"></a><span data-ttu-id="4d026-531">パラメーター - showRowLabels</span><span class="sxs-lookup"><span data-stu-id="4d026-531">Parameters - showRowLabels</span></span>

<span data-ttu-id="4d026-532">値</span><span class="sxs-lookup"><span data-stu-id="4d026-532">value</span></span>  

### <a name="return-value---showrowlabels"></a><span data-ttu-id="4d026-533">戻り値 - showRowLabels</span><span class="sxs-lookup"><span data-stu-id="4d026-533">Return Value - showRowLabels</span></span>

## <a name="method-skip"></a><span data-ttu-id="4d026-534">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="4d026-534">Method skip</span></span>

<span data-ttu-id="4d026-535">ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="4d026-535">Sets or returns a value that indicates whether the control is skipped when the user presses the TAB key to move to the control.</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="4d026-536">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="4d026-536">Parameters - skip</span></span>

<span data-ttu-id="4d026-537">値</span><span class="sxs-lookup"><span data-stu-id="4d026-537">value</span></span>  
<span data-ttu-id="4d026-538">コントロールの skip プロパティに割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="4d026-538">The value to assign to the skip property of the control.</span></span>

### <a name="return-value---skip"></a><span data-ttu-id="4d026-539">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="4d026-539">Return Value - skip</span></span>

<span data-ttu-id="4d026-540">コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="4d026-540">true if the control is skipped when the user presses the TAB key to move to the control; otherwise, false.</span></span>

## <a name="method-style"></a><span data-ttu-id="4d026-541">メソッド style</span><span class="sxs-lookup"><span data-stu-id="4d026-541">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="4d026-542">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="4d026-542">Parameters - style</span></span>

<span data-ttu-id="4d026-543">値</span><span class="sxs-lookup"><span data-stu-id="4d026-543">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="4d026-544">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="4d026-544">Return Value - style</span></span>

## <a name="method-top"></a><span data-ttu-id="4d026-545">メソッド top</span><span class="sxs-lookup"><span data-stu-id="4d026-545">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="4d026-546">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="4d026-546">Parameters - top</span></span>

<span data-ttu-id="4d026-547">値</span><span class="sxs-lookup"><span data-stu-id="4d026-547">value</span></span>  

<!-- -->

<span data-ttu-id="4d026-548">モード</span><span class="sxs-lookup"><span data-stu-id="4d026-548">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="4d026-549">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="4d026-549">Return Value - top</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="4d026-550">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="4d026-550">Method topMargin</span></span>

```xpp
public int topMargin([int value])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="4d026-551">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="4d026-551">Parameters - topMargin</span></span>

<span data-ttu-id="4d026-552">値</span><span class="sxs-lookup"><span data-stu-id="4d026-552">value</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="4d026-553">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="4d026-553">Return Value - topMargin</span></span>

## <a name="method-topmode"></a><span data-ttu-id="4d026-554">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="4d026-554">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="4d026-555">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="4d026-555">Parameters - topMode</span></span>

<span data-ttu-id="4d026-556">値</span><span class="sxs-lookup"><span data-stu-id="4d026-556">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="4d026-557">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="4d026-557">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="4d026-558">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="4d026-558">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="4d026-559">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="4d026-559">Parameters - topValue</span></span>

<span data-ttu-id="4d026-560">値</span><span class="sxs-lookup"><span data-stu-id="4d026-560">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="4d026-561">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="4d026-561">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="4d026-562">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="4d026-562">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="4d026-563">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="4d026-563">Parameters - type</span></span>

<span data-ttu-id="4d026-564">値</span><span class="sxs-lookup"><span data-stu-id="4d026-564">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="4d026-565">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="4d026-565">Return Value - type</span></span>

## <a name="method-userdata"></a><span data-ttu-id="4d026-566">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="4d026-566">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="4d026-567">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="4d026-567">Parameters - userData</span></span>

<span data-ttu-id="4d026-568">値</span><span class="sxs-lookup"><span data-stu-id="4d026-568">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="4d026-569">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="4d026-569">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="4d026-570">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="4d026-570">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="4d026-571">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="4d026-571">Parameters - userDataItem</span></span>

<span data-ttu-id="4d026-572">値</span><span class="sxs-lookup"><span data-stu-id="4d026-572">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="4d026-573">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="4d026-573">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="4d026-574">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="4d026-574">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="4d026-575">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="4d026-575">Parameters - userDataItems</span></span>

<span data-ttu-id="4d026-576">値</span><span class="sxs-lookup"><span data-stu-id="4d026-576">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="4d026-577">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="4d026-577">Return Value - userDataItems</span></span>

## <a name="method-useuserlayout"></a><span data-ttu-id="4d026-578">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="4d026-578">Method useUserLayout</span></span>

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a><span data-ttu-id="4d026-579">パラメーター - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="4d026-579">Parameters - useUserLayout</span></span>

<span data-ttu-id="4d026-580">値</span><span class="sxs-lookup"><span data-stu-id="4d026-580">value</span></span>  

### <a name="return-value---useuserlayout"></a><span data-ttu-id="4d026-581">戻り値 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="4d026-581">Return Value - useUserLayout</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="4d026-582">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="4d026-582">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="4d026-583">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="4d026-583">Parameters - verticalSpacing</span></span>

<span data-ttu-id="4d026-584">値</span><span class="sxs-lookup"><span data-stu-id="4d026-584">value</span></span>  

<!-- -->

<span data-ttu-id="4d026-585">モード</span><span class="sxs-lookup"><span data-stu-id="4d026-585">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="4d026-586">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="4d026-586">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="4d026-587">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="4d026-587">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="4d026-588">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="4d026-588">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="4d026-589">モード</span><span class="sxs-lookup"><span data-stu-id="4d026-589">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="4d026-590">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="4d026-590">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="4d026-591">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="4d026-591">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="4d026-592">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="4d026-592">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="4d026-593">値</span><span class="sxs-lookup"><span data-stu-id="4d026-593">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="4d026-594">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="4d026-594">Return Value - verticalSpacingValue</span></span>

## <a name="method-visible"></a><span data-ttu-id="4d026-595">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="4d026-595">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="4d026-596">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="4d026-596">Parameters - visible</span></span>

<span data-ttu-id="4d026-597">値</span><span class="sxs-lookup"><span data-stu-id="4d026-597">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="4d026-598">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="4d026-598">Return Value - visible</span></span>

## <a name="method-visiblecols"></a><span data-ttu-id="4d026-599">メソッド visibleCols</span><span class="sxs-lookup"><span data-stu-id="4d026-599">Method visibleCols</span></span>

```xpp
public int visibleCols([int value], [AutoMode mode])
```

### <a name="parameters---visiblecols"></a><span data-ttu-id="4d026-600">パラメーター - visibleCols</span><span class="sxs-lookup"><span data-stu-id="4d026-600">Parameters - visibleCols</span></span>

<span data-ttu-id="4d026-601">値</span><span class="sxs-lookup"><span data-stu-id="4d026-601">value</span></span>  

<!-- -->

<span data-ttu-id="4d026-602">モード</span><span class="sxs-lookup"><span data-stu-id="4d026-602">mode</span></span>  

### <a name="return-value---visiblecols"></a><span data-ttu-id="4d026-603">戻り値 - visibleCols</span><span class="sxs-lookup"><span data-stu-id="4d026-603">Return Value - visibleCols</span></span>

## <a name="method-visiblecolsmode"></a><span data-ttu-id="4d026-604">メソッド visibleColsMode</span><span class="sxs-lookup"><span data-stu-id="4d026-604">Method visibleColsMode</span></span>

```xpp
public AutoMode visibleColsMode([AutoMode mode])
```

### <a name="parameters---visiblecolsmode"></a><span data-ttu-id="4d026-605">パラメーター - visibleColsMode</span><span class="sxs-lookup"><span data-stu-id="4d026-605">Parameters - visibleColsMode</span></span>

<span data-ttu-id="4d026-606">モード</span><span class="sxs-lookup"><span data-stu-id="4d026-606">mode</span></span>  

### <a name="return-value---visiblecolsmode"></a><span data-ttu-id="4d026-607">戻り値 - visibleColsMode</span><span class="sxs-lookup"><span data-stu-id="4d026-607">Return Value - visibleColsMode</span></span>

## <a name="method-visiblecolsvalue"></a><span data-ttu-id="4d026-608">メソッド visibleColsValue</span><span class="sxs-lookup"><span data-stu-id="4d026-608">Method visibleColsValue</span></span>

```xpp
public int visibleColsValue([int value])
```

### <a name="parameters---visiblecolsvalue"></a><span data-ttu-id="4d026-609">パラメーター - visibleColsValue</span><span class="sxs-lookup"><span data-stu-id="4d026-609">Parameters - visibleColsValue</span></span>

<span data-ttu-id="4d026-610">値</span><span class="sxs-lookup"><span data-stu-id="4d026-610">value</span></span>  

### <a name="return-value---visiblecolsvalue"></a><span data-ttu-id="4d026-611">戻り値 - visibleColsValue</span><span class="sxs-lookup"><span data-stu-id="4d026-611">Return Value - visibleColsValue</span></span>

## <a name="method-visiblerows"></a><span data-ttu-id="4d026-612">メソッド visibleRows</span><span class="sxs-lookup"><span data-stu-id="4d026-612">Method visibleRows</span></span>

```xpp
public int visibleRows([int value], [AutoMode mode])
```

### <a name="parameters---visiblerows"></a><span data-ttu-id="4d026-613">パラメーター - visibleRows</span><span class="sxs-lookup"><span data-stu-id="4d026-613">Parameters - visibleRows</span></span>

<span data-ttu-id="4d026-614">値</span><span class="sxs-lookup"><span data-stu-id="4d026-614">value</span></span>  

<!-- -->

<span data-ttu-id="4d026-615">モード</span><span class="sxs-lookup"><span data-stu-id="4d026-615">mode</span></span>  

### <a name="return-value---visiblerows"></a><span data-ttu-id="4d026-616">戻り値 - visibleRows</span><span class="sxs-lookup"><span data-stu-id="4d026-616">Return Value - visibleRows</span></span>

## <a name="method-visiblerowsmode"></a><span data-ttu-id="4d026-617">メソッド visibleRowsMode</span><span class="sxs-lookup"><span data-stu-id="4d026-617">Method visibleRowsMode</span></span>

```xpp
public AutoMode visibleRowsMode([AutoMode mode])
```

### <a name="parameters---visiblerowsmode"></a><span data-ttu-id="4d026-618">パラメーター - visibleRowsMode</span><span class="sxs-lookup"><span data-stu-id="4d026-618">Parameters - visibleRowsMode</span></span>

<span data-ttu-id="4d026-619">モード</span><span class="sxs-lookup"><span data-stu-id="4d026-619">mode</span></span>  

### <a name="return-value---visiblerowsmode"></a><span data-ttu-id="4d026-620">戻り値 - visibleRowsMode</span><span class="sxs-lookup"><span data-stu-id="4d026-620">Return Value - visibleRowsMode</span></span>

## <a name="method-visiblerowsvalue"></a><span data-ttu-id="4d026-621">メソッド visibleRowsValue</span><span class="sxs-lookup"><span data-stu-id="4d026-621">Method visibleRowsValue</span></span>

```xpp
public int visibleRowsValue([int value])
```

### <a name="parameters---visiblerowsvalue"></a><span data-ttu-id="4d026-622">パラメーター - visibleRowsValue</span><span class="sxs-lookup"><span data-stu-id="4d026-622">Parameters - visibleRowsValue</span></span>

<span data-ttu-id="4d026-623">値</span><span class="sxs-lookup"><span data-stu-id="4d026-623">value</span></span>  

### <a name="return-value---visiblerowsvalue"></a><span data-ttu-id="4d026-624">戻り値 - visibleRowsValue</span><span class="sxs-lookup"><span data-stu-id="4d026-624">Return Value - visibleRowsValue</span></span>

## <a name="method-width"></a><span data-ttu-id="4d026-625">メソッド width</span><span class="sxs-lookup"><span data-stu-id="4d026-625">Method width</span></span>

<span data-ttu-id="4d026-626">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-626">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="4d026-627">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="4d026-627">Parameters - width</span></span>

<span data-ttu-id="4d026-628">値</span><span class="sxs-lookup"><span data-stu-id="4d026-628">value</span></span>  

<!-- -->

<span data-ttu-id="4d026-629">モード</span><span class="sxs-lookup"><span data-stu-id="4d026-629">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="4d026-630">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="4d026-630">Return Value - width</span></span>

<span data-ttu-id="4d026-631">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="4d026-631">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="4d026-632">備考 - width</span><span class="sxs-lookup"><span data-stu-id="4d026-632">Remarks - width</span></span>

<span data-ttu-id="4d026-633">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="4d026-633">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="4d026-634">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="4d026-634">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="4d026-635">モード。</span><span class="sxs-lookup"><span data-stu-id="4d026-635">Mode.</span></span>           | <span data-ttu-id="4d026-636">幅計算。</span><span class="sxs-lookup"><span data-stu-id="4d026-636">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d026-637">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="4d026-637">-1 Exact.</span></span>       | <span data-ttu-id="4d026-638">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4d026-638">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="4d026-639">0 自動。</span><span class="sxs-lookup"><span data-stu-id="4d026-639">0 Auto.</span></span>         | <span data-ttu-id="4d026-640">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="4d026-640">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="4d026-641">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="4d026-641">1 Column width.</span></span> | <span data-ttu-id="4d026-642">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="4d026-642">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="4d026-643">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="4d026-643">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="4d026-644">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="4d026-644">Method widthMode</span></span>

<span data-ttu-id="4d026-645">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-645">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="4d026-646">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="4d026-646">Parameters - widthMode</span></span>

<span data-ttu-id="4d026-647">値</span><span class="sxs-lookup"><span data-stu-id="4d026-647">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="4d026-648">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="4d026-648">Return Value - widthMode</span></span>

<span data-ttu-id="4d026-649">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="4d026-649">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="4d026-650">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="4d026-650">Remarks - widthMode</span></span>

<span data-ttu-id="4d026-651">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="4d026-651">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="4d026-652">モード。</span><span class="sxs-lookup"><span data-stu-id="4d026-652">Mode.</span></span>         | <span data-ttu-id="4d026-653">幅計算。</span><span class="sxs-lookup"><span data-stu-id="4d026-653">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d026-654">正確。</span><span class="sxs-lookup"><span data-stu-id="4d026-654">Exact.</span></span>        | <span data-ttu-id="4d026-655">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4d026-655">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="4d026-656">自動。</span><span class="sxs-lookup"><span data-stu-id="4d026-656">Auto.</span></span>         | <span data-ttu-id="4d026-657">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="4d026-657">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="4d026-658">列の幅。</span><span class="sxs-lookup"><span data-stu-id="4d026-658">Column width.</span></span> | <span data-ttu-id="4d026-659">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="4d026-659">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="4d026-660">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="4d026-660">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="4d026-661">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="4d026-661">Method widthValue</span></span>

<span data-ttu-id="4d026-662">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4d026-662">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="4d026-663">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="4d026-663">Parameters - widthValue</span></span>

<span data-ttu-id="4d026-664">値</span><span class="sxs-lookup"><span data-stu-id="4d026-664">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="4d026-665">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="4d026-665">Return Value - widthValue</span></span>

<span data-ttu-id="4d026-666">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="4d026-666">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="4d026-667">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="4d026-667">Remarks - widthValue</span></span>

<span data-ttu-id="4d026-668">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="4d026-668">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="4d026-669">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="4d026-669">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="4d026-670">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="4d026-670">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="4d026-671">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="4d026-671">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="4d026-672">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="4d026-672">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="4d026-673">overrideObject</span><span class="sxs-lookup"><span data-stu-id="4d026-673">overrideObject</span></span>  

