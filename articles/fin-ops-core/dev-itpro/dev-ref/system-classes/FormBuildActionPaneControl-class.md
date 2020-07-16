---
title: FormBuildActionPaneControl クラス
description: このトピックでは、FormBuildActionPaneControl クラスについて説明します。
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
ms.openlocfilehash: 9f355094a60b14165c54bb06d716320f1310902a
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502659"
---
# <a name="class-formbuildactionpanecontrol"></a><span data-ttu-id="fcc63-103">クラス FormBuildActionPaneControl</span><span class="sxs-lookup"><span data-stu-id="fcc63-103">Class FormBuildActionPaneControl</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildActionPaneControl extends FormBuildControl
```

## <a name="remarks"></a><span data-ttu-id="fcc63-104">備考</span><span class="sxs-lookup"><span data-stu-id="fcc63-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="fcc63-105">例</span><span class="sxs-lookup"><span data-stu-id="fcc63-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="fcc63-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="fcc63-106">Methods</span></span>

| <span data-ttu-id="fcc63-107">方法</span><span class="sxs-lookup"><span data-stu-id="fcc63-107">Method</span></span>                                                                                                      | <span data-ttu-id="fcc63-108">説明</span><span class="sxs-lookup"><span data-stu-id="fcc63-108">Description</span></span>                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcc63-109">public boolean alignChild(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-109">public boolean alignChild(\[boolean value\])</span></span>                                                                |                                                                                                                                               |
| <span data-ttu-id="fcc63-110">public boolean alignChildren(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-110">public boolean alignChildren(\[boolean value\])</span></span>                                                             |                                                                                                                                               |
| <span data-ttu-id="fcc63-111">public boolean alignControl(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-111">public boolean alignControl(\[boolean value\])</span></span>                                                              | <span data-ttu-id="fcc63-112">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-112">Determines whether to align the control.</span></span>                                                                                                      |
| <span data-ttu-id="fcc63-113">public boolean allowEdit(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-113">public boolean allowEdit(\[boolean value\])</span></span>                                                                 | <span data-ttu-id="fcc63-114">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-114">Determines whether the user can change the contents of the control.</span></span>                                                                           |
| <span data-ttu-id="fcc63-115">public int allowUserSetup(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-115">public int allowUserSetup(\[int value\])</span></span>                                                                    |                                                                                                                                               |
| <span data-ttu-id="fcc63-116">public int arrangeGuide(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-116">public int arrangeGuide(\[int value\])</span></span>                                                                      |                                                                                                                                               |
| <span data-ttu-id="fcc63-117">public int arrangeMethod(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-117">public int arrangeMethod(\[int value\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="fcc63-118">public int arrangeWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-118">public int arrangeWhen(\[int value\])</span></span>                                                                       |                                                                                                                                               |
| <span data-ttu-id="fcc63-119">public boolean autoDeclaration(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-119">public boolean autoDeclaration(\[boolean value\])</span></span>                                                           | <span data-ttu-id="fcc63-120">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-120">Determines whether the system can declare a member variable that has the same name as the control.</span></span>                                            |
| <span data-ttu-id="fcc63-121">public int bottomMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-121">public int bottomMargin(\[int value\], \[AutoMode mode\])</span></span>                                                   |                                                                                                                                               |
| <span data-ttu-id="fcc63-122">public AutoMode bottomMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-122">public AutoMode bottomMarginMode(\[AutoMode mode\])</span></span>                                                         |                                                                                                                                               |
| <span data-ttu-id="fcc63-123">public int bottomMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-123">public int bottomMarginValue(\[int value\])</span></span>                                                                 |                                                                                                                                               |
| <span data-ttu-id="fcc63-124">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-124">public str caption(\[str value\])</span></span>                                                                           | <span data-ttu-id="fcc63-125">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-125">Gets or set the caption of the control.</span></span>                                                                                                       |
| <span data-ttu-id="fcc63-126">public int columns(\[int value\], \[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-126">public int columns(\[int value\], \[ColumnsMode mode\])</span></span>                                                     |                                                                                                                                               |
| <span data-ttu-id="fcc63-127">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-127">public ColumnsMode columnsMode(\[ColumnsMode mode\])</span></span>                                                        |                                                                                                                                               |
| <span data-ttu-id="fcc63-128">public int columnspace(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-128">public int columnspace(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                               |
| <span data-ttu-id="fcc63-129">public AutoMode columnspaceMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-129">public AutoMode columnspaceMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                               |
| <span data-ttu-id="fcc63-130">public int columnspaceValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-130">public int columnspaceValue(\[int value\])</span></span>                                                                  |                                                                                                                                               |
| <span data-ttu-id="fcc63-131">public int columnsValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-131">public int columnsValue(\[int value\])</span></span>                                                                      |                                                                                                                                               |
| <span data-ttu-id="fcc63-132">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-132">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>                                    | <span data-ttu-id="fcc63-133">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-133">Gets or sets the configuration key that is assigned to the control.</span></span>                                                                           |
| <span data-ttu-id="fcc63-134">public int containerId()</span><span class="sxs-lookup"><span data-stu-id="fcc63-134">public int containerId()</span></span>                                                                                    | <span data-ttu-id="fcc63-135">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-135">Retrieves the ID of the parent container for the control.</span></span>                                                                                     |
| <span data-ttu-id="fcc63-136">public str dataRelationPath(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-136">public str dataRelationPath(\[str value\])</span></span>                                                                  |                                                                                                                                               |
| <span data-ttu-id="fcc63-137">public int dataSource(\[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-137">public int dataSource(\[AnyType value\])</span></span>                                                                    | <span data-ttu-id="fcc63-138">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-138">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                      |
| <span data-ttu-id="fcc63-139">public int displayTarget(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-139">public int displayTarget(\[int value\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="fcc63-140">public int dragDrop(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-140">public int dragDrop(\[int value\])</span></span>                                                                          | <span data-ttu-id="fcc63-141">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-141">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>                                                             |
| <span data-ttu-id="fcc63-142">public boolean enabled(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-142">public boolean enabled(\[boolean value\])</span></span>                                                                   | <span data-ttu-id="fcc63-143">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-143">Determines whether to enable or disable the object.</span></span>                                                                                           |
| <span data-ttu-id="fcc63-144">public int height(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-144">public int height(int value, \[int mode\])</span></span>                                                                  | <span data-ttu-id="fcc63-145">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-145">Gets or sets the height of the control.</span></span>                                                                                                       |
| <span data-ttu-id="fcc63-146">public int heightMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-146">public int heightMode(\[int value\])</span></span>                                                                        | <span data-ttu-id="fcc63-147">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-147">Gets or sets a calculation mode for the height of the control.</span></span>                                                                                |
| <span data-ttu-id="fcc63-148">public int heightValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-148">public int heightValue(\[int value\])</span></span>                                                                       | <span data-ttu-id="fcc63-149">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-149">Gets or sets the height of the control.</span></span>                                                                                                       |
| <span data-ttu-id="fcc63-150">public str helpText(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-150">public str helpText(\[str value\])</span></span>                                                                          | <span data-ttu-id="fcc63-151">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-151">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>                                      |
| <span data-ttu-id="fcc63-152">public boolean hideIfEmpty(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-152">public boolean hideIfEmpty(\[boolean value\])</span></span>                                                               |                                                                                                                                               |
| <span data-ttu-id="fcc63-153">public str hierarchyParent(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-153">public str hierarchyParent(\[str value\])</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="fcc63-154">public int id()</span><span class="sxs-lookup"><span data-stu-id="fcc63-154">public int id()</span></span>                                                                                             | <span data-ttu-id="fcc63-155">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-155">Retrieves the ID of the control.</span></span>                                                                                                              |
| <span data-ttu-id="fcc63-156">public boolean isContainer()</span><span class="sxs-lookup"><span data-stu-id="fcc63-156">public boolean isContainer()</span></span>                                                                                | <span data-ttu-id="fcc63-157">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-157">Retrieves a value that indicates whether the control is a container control.</span></span>                                                                  |
| <span data-ttu-id="fcc63-158">public int left(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-158">public int left(int value, \[int mode\])</span></span>                                                                    |                                                                                                                                               |
| <span data-ttu-id="fcc63-159">public int leftMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-159">public int leftMargin(\[int value\], \[AutoMode mode\])</span></span>                                                     |                                                                                                                                               |
| <span data-ttu-id="fcc63-160">public AutoMode leftMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-160">public AutoMode leftMarginMode(\[AutoMode mode\])</span></span>                                                           |                                                                                                                                               |
| <span data-ttu-id="fcc63-161">public int leftMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-161">public int leftMarginValue(\[int value\])</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="fcc63-162">public int leftMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-162">public int leftMode(\[int value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="fcc63-163">public int leftValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-163">public int leftValue(\[int value\])</span></span>                                                                         |                                                                                                                                               |
| <span data-ttu-id="fcc63-164">public int moveControl(int controlId, \[int insertAfterControlId\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-164">public int moveControl(int controlId, \[int insertAfterControlId\])</span></span>                                         | <span data-ttu-id="fcc63-165">コントロールに ID で指定されているコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-165">Moves a control that is specified by ID to the control.</span></span>                                                                                       |
| <span data-ttu-id="fcc63-166">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-166">public str name(\[str value\])</span></span>                                                                              | <span data-ttu-id="fcc63-167">フォーム、レポート、テーブル、クエリ、または別のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-167">Gets or sets the name that is used in the code to identify a form, report, table, query, or another application object.</span></span> |
| <span data-ttu-id="fcc63-168">public int neededPermission(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-168">public int neededPermission(\[int value\])</span></span>                                                                  |                                                                                                                                               |
| <span data-ttu-id="fcc63-169">public int position(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-169">public int position(\[int value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="fcc63-170">public int rightMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-170">public int rightMargin(\[int value\], \[AutoMode mode\])</span></span>                                                    |                                                                                                                                               |
| <span data-ttu-id="fcc63-171">public AutoMode rightMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-171">public AutoMode rightMarginMode(\[AutoMode mode\])</span></span>                                                          |                                                                                                                                               |
| <span data-ttu-id="fcc63-172">public int rightMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-172">public int rightMarginValue(\[int value\])</span></span>                                                                  |                                                                                                                                               |
| <span data-ttu-id="fcc63-173">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-173">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                                                   |                                                                                                                                               |
| <span data-ttu-id="fcc63-174">public boolean skip(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-174">public boolean skip(\[boolean value\])</span></span>                                                                      |                                                                                                                                               |
| <span data-ttu-id="fcc63-175">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-175">public int style(\[int value\])</span></span>                                                                             |                                                                                                                                               |
| <span data-ttu-id="fcc63-176">public int top(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-176">public int top(int value, \[int mode\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="fcc63-177">public int topMargin(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-177">public int topMargin(\[int value\], \[AutoMode mode\])</span></span>                                                      |                                                                                                                                               |
| <span data-ttu-id="fcc63-178">public AutoMode topMarginMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-178">public AutoMode topMarginMode(\[AutoMode mode\])</span></span>                                                            |                                                                                                                                               |
| <span data-ttu-id="fcc63-179">public int topMarginValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-179">public int topMarginValue(\[int value\])</span></span>                                                                    |                                                                                                                                               |
| <span data-ttu-id="fcc63-180">public int topMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-180">public int topMode(\[int value\])</span></span>                                                                           |                                                                                                                                               |
| <span data-ttu-id="fcc63-181">public int topValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-181">public int topValue(\[int value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="fcc63-182">public int type(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-182">public int type(\[int value\])</span></span>                                                                              |                                                                                                                                               |
| <span data-ttu-id="fcc63-183">public int userData(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-183">public int userData(\[int value\])</span></span>                                                                          |                                                                                                                                               |
| <span data-ttu-id="fcc63-184">public int userDataItem(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-184">public int userDataItem(\[int value\])</span></span>                                                                      |                                                                                                                                               |
| <span data-ttu-id="fcc63-185">public int userDataItems(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-185">public int userDataItems(\[int value\])</span></span>                                                                     |                                                                                                                                               |
| <span data-ttu-id="fcc63-186">public boolean useUserLayout(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-186">public boolean useUserLayout(\[boolean value\])</span></span>                                                             |                                                                                                                                               |
| <span data-ttu-id="fcc63-187">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-187">public int verticalSpacing(\[int value\], \[AutoMode mode\])</span></span>                                                |                                                                                                                                               |
| <span data-ttu-id="fcc63-188">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-188">public AutoMode verticalSpacingMode(\[AutoMode mode\])</span></span>                                                      |                                                                                                                                               |
| <span data-ttu-id="fcc63-189">public int verticalSpacingValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-189">public int verticalSpacingValue(\[int value\])</span></span>                                                              |                                                                                                                                               |
| <span data-ttu-id="fcc63-190">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-190">public boolean visible(\[boolean value\])</span></span>                                                                   |                                                                                                                                               |
| <span data-ttu-id="fcc63-191">public int width(int value, \[int mode\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-191">public int width(int value, \[int mode\])</span></span>                                                                   | <span data-ttu-id="fcc63-192">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-192">Gets or sets the width of the control.</span></span>                                                                                                        |
| <span data-ttu-id="fcc63-193">public int widthMode(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-193">public int widthMode(\[int value\])</span></span>                                                                         | <span data-ttu-id="fcc63-194">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-194">Gets or sets the calculation mode of the width of the control.</span></span>                                                                                |
| <span data-ttu-id="fcc63-195">public int widthValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-195">public int widthValue(\[int value\])</span></span>                                                                        | <span data-ttu-id="fcc63-196">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-196">Gets or sets the width of the control.</span></span>                                                                                                        |
| <span data-ttu-id="fcc63-197">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span><span class="sxs-lookup"><span data-stu-id="fcc63-197">public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\])</span></span> |                                                                                                                                               |

## <a name="method-alignchild"></a><span data-ttu-id="fcc63-198">メソッド alignChild</span><span class="sxs-lookup"><span data-stu-id="fcc63-198">Method alignChild</span></span>

```xpp
public boolean alignChild([boolean value])
```

### <a name="parameters---alignchild"></a><span data-ttu-id="fcc63-199">パラメーター - alignChild</span><span class="sxs-lookup"><span data-stu-id="fcc63-199">Parameters - alignChild</span></span>

<span data-ttu-id="fcc63-200">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-200">value</span></span>  

### <a name="return-value---alignchild"></a><span data-ttu-id="fcc63-201">戻り値 - alignChild</span><span class="sxs-lookup"><span data-stu-id="fcc63-201">Return Value - alignChild</span></span>

## <a name="method-alignchildren"></a><span data-ttu-id="fcc63-202">メソッド alignChildren</span><span class="sxs-lookup"><span data-stu-id="fcc63-202">Method alignChildren</span></span>

```xpp
public boolean alignChildren([boolean value])
```

### <a name="parameters---alignchildren"></a><span data-ttu-id="fcc63-203">パラメーター - alignChildren</span><span class="sxs-lookup"><span data-stu-id="fcc63-203">Parameters - alignChildren</span></span>

<span data-ttu-id="fcc63-204">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-204">value</span></span>  

### <a name="return-value---alignchildren"></a><span data-ttu-id="fcc63-205">戻り値 - alignChildren</span><span class="sxs-lookup"><span data-stu-id="fcc63-205">Return Value - alignChildren</span></span>

## <a name="method-aligncontrol"></a><span data-ttu-id="fcc63-206">メソッド alignControl</span><span class="sxs-lookup"><span data-stu-id="fcc63-206">Method alignControl</span></span>

<span data-ttu-id="fcc63-207">コントロールを配置するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-207">Determines whether to align the control.</span></span>

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a><span data-ttu-id="fcc63-208">パラメーター - alignControl</span><span class="sxs-lookup"><span data-stu-id="fcc63-208">Parameters - alignControl</span></span>

<span data-ttu-id="fcc63-209">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-209">value</span></span>  

### <a name="return-value---aligncontrol"></a><span data-ttu-id="fcc63-210">戻り値 - alignControl</span><span class="sxs-lookup"><span data-stu-id="fcc63-210">Return Value - alignControl</span></span>

<span data-ttu-id="fcc63-211">コントロールをアラインする必要がある場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="fcc63-211">true if the control should be aligned; otherwise, false.</span></span>

### <a name="remarks---aligncontrol"></a><span data-ttu-id="fcc63-212">備考 - alignControl</span><span class="sxs-lookup"><span data-stu-id="fcc63-212">Remarks - alignControl</span></span>

<span data-ttu-id="fcc63-213">コントロールの左上隅は、最も長いラベルに従って配置されます。</span><span class="sxs-lookup"><span data-stu-id="fcc63-213">The upper-left corner of the control is aligned according to the longest label.</span></span>

## <a name="method-allowedit"></a><span data-ttu-id="fcc63-214">メソッド allowEdit</span><span class="sxs-lookup"><span data-stu-id="fcc63-214">Method allowEdit</span></span>

<span data-ttu-id="fcc63-215">ユーザーがコントロールの内容を変更できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-215">Determines whether the user can change the contents of the control.</span></span>

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a><span data-ttu-id="fcc63-216">パラメーター - allowEdit</span><span class="sxs-lookup"><span data-stu-id="fcc63-216">Parameters - allowEdit</span></span>

<span data-ttu-id="fcc63-217">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-217">value</span></span>  

### <a name="return-value---allowedit"></a><span data-ttu-id="fcc63-218">戻り値 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="fcc63-218">Return Value - allowEdit</span></span>

<span data-ttu-id="fcc63-219">コントロールを編集することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fcc63-219">true if the control can be edited; otherwise, false.</span></span>

### <a name="remarks---allowedit"></a><span data-ttu-id="fcc63-220">備考 - allowEdit</span><span class="sxs-lookup"><span data-stu-id="fcc63-220">Remarks - allowEdit</span></span>

<span data-ttu-id="fcc63-221">コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。</span><span class="sxs-lookup"><span data-stu-id="fcc63-221">When this property is set on a container control, modifications are disabled or enabled for all controls in the container.</span></span>

## <a name="method-allowusersetup"></a><span data-ttu-id="fcc63-222">メソッド allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="fcc63-222">Method allowUserSetup</span></span>

```xpp
public int allowUserSetup([int value])
```

### <a name="parameters---allowusersetup"></a><span data-ttu-id="fcc63-223">パラメーター - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="fcc63-223">Parameters - allowUserSetup</span></span>

<span data-ttu-id="fcc63-224">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-224">value</span></span>  

### <a name="return-value---allowusersetup"></a><span data-ttu-id="fcc63-225">戻り値 - allowUserSetup</span><span class="sxs-lookup"><span data-stu-id="fcc63-225">Return Value - allowUserSetup</span></span>

## <a name="method-arrangeguide"></a><span data-ttu-id="fcc63-226">メソッド arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="fcc63-226">Method arrangeGuide</span></span>

```xpp
public int arrangeGuide([int value])
```

### <a name="parameters---arrangeguide"></a><span data-ttu-id="fcc63-227">パラメーター - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="fcc63-227">Parameters - arrangeGuide</span></span>

<span data-ttu-id="fcc63-228">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-228">value</span></span>  

### <a name="return-value---arrangeguide"></a><span data-ttu-id="fcc63-229">戻り値 - arrangeGuide</span><span class="sxs-lookup"><span data-stu-id="fcc63-229">Return Value - arrangeGuide</span></span>

## <a name="method-arrangemethod"></a><span data-ttu-id="fcc63-230">メソッド arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="fcc63-230">Method arrangeMethod</span></span>

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a><span data-ttu-id="fcc63-231">パラメーター - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="fcc63-231">Parameters - arrangeMethod</span></span>

<span data-ttu-id="fcc63-232">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-232">value</span></span>  

### <a name="return-value---arrangemethod"></a><span data-ttu-id="fcc63-233">戻り値 - arrangeMethod</span><span class="sxs-lookup"><span data-stu-id="fcc63-233">Return Value - arrangeMethod</span></span>

## <a name="method-arrangewhen"></a><span data-ttu-id="fcc63-234">メソッド arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="fcc63-234">Method arrangeWhen</span></span>

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a><span data-ttu-id="fcc63-235">パラメーター - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="fcc63-235">Parameters - arrangeWhen</span></span>

<span data-ttu-id="fcc63-236">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-236">value</span></span>  

### <a name="return-value---arrangewhen"></a><span data-ttu-id="fcc63-237">戻り値 - arrangeWhen</span><span class="sxs-lookup"><span data-stu-id="fcc63-237">Return Value - arrangeWhen</span></span>

## <a name="method-autodeclaration"></a><span data-ttu-id="fcc63-238">メソッド autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="fcc63-238">Method autoDeclaration</span></span>

<span data-ttu-id="fcc63-239">システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-239">Determines whether the system can declare a member variable that has the same name as the control.</span></span>

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a><span data-ttu-id="fcc63-240">パラメーター - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="fcc63-240">Parameters - autoDeclaration</span></span>

<span data-ttu-id="fcc63-241">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-241">value</span></span>  

### <a name="return-value---autodeclaration"></a><span data-ttu-id="fcc63-242">戻り値 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="fcc63-242">Return Value - autoDeclaration</span></span>

<span data-ttu-id="fcc63-243">このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fcc63-243">true if the member variable can be declared for this control; otherwise, false.</span></span>

### <a name="remarks---autodeclaration"></a><span data-ttu-id="fcc63-244">備考 - autoDeclaration</span><span class="sxs-lookup"><span data-stu-id="fcc63-244">Remarks - autoDeclaration</span></span>

<span data-ttu-id="fcc63-245">コントロールには同じ名前を付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="fcc63-245">Controls cannot have identical names.</span></span>

## <a name="method-bottommargin"></a><span data-ttu-id="fcc63-246">メソッド bottomMargin</span><span class="sxs-lookup"><span data-stu-id="fcc63-246">Method bottomMargin</span></span>

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a><span data-ttu-id="fcc63-247">パラメーター - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="fcc63-247">Parameters - bottomMargin</span></span>

<span data-ttu-id="fcc63-248">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-248">value</span></span>  

<!-- -->

<span data-ttu-id="fcc63-249">モード</span><span class="sxs-lookup"><span data-stu-id="fcc63-249">mode</span></span>  

### <a name="return-value---bottommargin"></a><span data-ttu-id="fcc63-250">戻り値 - bottomMargin</span><span class="sxs-lookup"><span data-stu-id="fcc63-250">Return Value - bottomMargin</span></span>

## <a name="method-bottommarginmode"></a><span data-ttu-id="fcc63-251">メソッド bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-251">Method bottomMarginMode</span></span>

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a><span data-ttu-id="fcc63-252">パラメーター - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-252">Parameters - bottomMarginMode</span></span>

<span data-ttu-id="fcc63-253">モード</span><span class="sxs-lookup"><span data-stu-id="fcc63-253">mode</span></span>  

### <a name="return-value---bottommarginmode"></a><span data-ttu-id="fcc63-254">戻り値 - bottomMarginMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-254">Return Value - bottomMarginMode</span></span>

## <a name="method-bottommarginvalue"></a><span data-ttu-id="fcc63-255">メソッド bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-255">Method bottomMarginValue</span></span>

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a><span data-ttu-id="fcc63-256">パラメーター - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-256">Parameters - bottomMarginValue</span></span>

<span data-ttu-id="fcc63-257">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-257">value</span></span>  

### <a name="return-value---bottommarginvalue"></a><span data-ttu-id="fcc63-258">戻り値 - bottomMarginValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-258">Return Value - bottomMarginValue</span></span>

## <a name="method-caption"></a><span data-ttu-id="fcc63-259">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="fcc63-259">Method caption</span></span>

<span data-ttu-id="fcc63-260">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-260">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="fcc63-261">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="fcc63-261">Parameters - caption</span></span>

<span data-ttu-id="fcc63-262">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-262">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="fcc63-263">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="fcc63-263">Return Value - caption</span></span>

<span data-ttu-id="fcc63-264">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="fcc63-264">The string that is used as the caption of the control.</span></span>

## <a name="method-columns"></a><span data-ttu-id="fcc63-265">メソッド columns</span><span class="sxs-lookup"><span data-stu-id="fcc63-265">Method columns</span></span>

```xpp
public int columns([int value], [ColumnsMode mode])
```

### <a name="parameters---columns"></a><span data-ttu-id="fcc63-266">パラメーター - columns</span><span class="sxs-lookup"><span data-stu-id="fcc63-266">Parameters - columns</span></span>

<span data-ttu-id="fcc63-267">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-267">value</span></span>  

<!-- -->

<span data-ttu-id="fcc63-268">モード</span><span class="sxs-lookup"><span data-stu-id="fcc63-268">mode</span></span>  

### <a name="return-value---columns"></a><span data-ttu-id="fcc63-269">戻り値 - columns</span><span class="sxs-lookup"><span data-stu-id="fcc63-269">Return Value - columns</span></span>

## <a name="method-columnsmode"></a><span data-ttu-id="fcc63-270">メソッド columnsMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-270">Method columnsMode</span></span>

```xpp
public ColumnsMode columnsMode([ColumnsMode mode])
```

### <a name="parameters---columnsmode"></a><span data-ttu-id="fcc63-271">パラメーター - columnsMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-271">Parameters - columnsMode</span></span>

<span data-ttu-id="fcc63-272">モード</span><span class="sxs-lookup"><span data-stu-id="fcc63-272">mode</span></span>  

### <a name="return-value---columnsmode"></a><span data-ttu-id="fcc63-273">戻り値 - columnsMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-273">Return Value - columnsMode</span></span>

## <a name="method-columnspace"></a><span data-ttu-id="fcc63-274">メソッド columnspace</span><span class="sxs-lookup"><span data-stu-id="fcc63-274">Method columnspace</span></span>

```xpp
public int columnspace([int value], [AutoMode mode])
```

### <a name="parameters---columnspace"></a><span data-ttu-id="fcc63-275">パラメーター - columnspace</span><span class="sxs-lookup"><span data-stu-id="fcc63-275">Parameters - columnspace</span></span>

<span data-ttu-id="fcc63-276">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-276">value</span></span>  

<!-- -->

<span data-ttu-id="fcc63-277">モード</span><span class="sxs-lookup"><span data-stu-id="fcc63-277">mode</span></span>  

### <a name="return-value---columnspace"></a><span data-ttu-id="fcc63-278">戻り値 - columnspace</span><span class="sxs-lookup"><span data-stu-id="fcc63-278">Return Value - columnspace</span></span>

## <a name="method-columnspacemode"></a><span data-ttu-id="fcc63-279">メソッド columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-279">Method columnspaceMode</span></span>

```xpp
public AutoMode columnspaceMode([AutoMode mode])
```

### <a name="parameters---columnspacemode"></a><span data-ttu-id="fcc63-280">パラメーター - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-280">Parameters - columnspaceMode</span></span>

<span data-ttu-id="fcc63-281">モード</span><span class="sxs-lookup"><span data-stu-id="fcc63-281">mode</span></span>  

### <a name="return-value---columnspacemode"></a><span data-ttu-id="fcc63-282">戻り値 - columnspaceMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-282">Return Value - columnspaceMode</span></span>

## <a name="method-columnspacevalue"></a><span data-ttu-id="fcc63-283">メソッド columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-283">Method columnspaceValue</span></span>

```xpp
public int columnspaceValue([int value])
```

### <a name="parameters---columnspacevalue"></a><span data-ttu-id="fcc63-284">パラメーター - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-284">Parameters - columnspaceValue</span></span>

<span data-ttu-id="fcc63-285">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-285">value</span></span>  

### <a name="return-value---columnspacevalue"></a><span data-ttu-id="fcc63-286">戻り値 - columnspaceValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-286">Return Value - columnspaceValue</span></span>

## <a name="method-columnsvalue"></a><span data-ttu-id="fcc63-287">メソッド columnsValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-287">Method columnsValue</span></span>

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a><span data-ttu-id="fcc63-288">パラメーター - columnsValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-288">Parameters - columnsValue</span></span>

<span data-ttu-id="fcc63-289">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-289">value</span></span>  

### <a name="return-value---columnsvalue"></a><span data-ttu-id="fcc63-290">戻り値 - columnsValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-290">Return Value - columnsValue</span></span>

## <a name="method-configurationkey"></a><span data-ttu-id="fcc63-291">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="fcc63-291">Method configurationKey</span></span>

<span data-ttu-id="fcc63-292">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-292">Gets or sets the configuration key that is assigned to the control.</span></span>

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a><span data-ttu-id="fcc63-293">パラメーター - configurationKey</span><span class="sxs-lookup"><span data-stu-id="fcc63-293">Parameters - configurationKey</span></span>

<span data-ttu-id="fcc63-294">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-294">value</span></span>  

### <a name="return-value---configurationkey"></a><span data-ttu-id="fcc63-295">戻り値 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="fcc63-295">Return Value - configurationKey</span></span>

<span data-ttu-id="fcc63-296">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="fcc63-296">The identifier of the configuration key that is assigned to the control.</span></span>

### <a name="remarks---configurationkey"></a><span data-ttu-id="fcc63-297">備考 - configurationKey</span><span class="sxs-lookup"><span data-stu-id="fcc63-297">Remarks - configurationKey</span></span>

<span data-ttu-id="fcc63-298">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fcc63-298">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="fcc63-299">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="fcc63-299">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

## <a name="method-containerid"></a><span data-ttu-id="fcc63-300">メソッド containerId</span><span class="sxs-lookup"><span data-stu-id="fcc63-300">Method containerId</span></span>

<span data-ttu-id="fcc63-301">コントロールの親コンテナーの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-301">Retrieves the ID of the parent container for the control.</span></span>

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a><span data-ttu-id="fcc63-302">戻り値 - containerId</span><span class="sxs-lookup"><span data-stu-id="fcc63-302">Return Value - containerId</span></span>

<span data-ttu-id="fcc63-303">親コンテナーの ID。</span><span class="sxs-lookup"><span data-stu-id="fcc63-303">The ID of the parent container.</span></span>

## <a name="method-datarelationpath"></a><span data-ttu-id="fcc63-304">メソッド dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="fcc63-304">Method dataRelationPath</span></span>

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a><span data-ttu-id="fcc63-305">パラメーター - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="fcc63-305">Parameters - dataRelationPath</span></span>

<span data-ttu-id="fcc63-306">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-306">value</span></span>  

### <a name="return-value---datarelationpath"></a><span data-ttu-id="fcc63-307">戻り値 - dataRelationPath</span><span class="sxs-lookup"><span data-stu-id="fcc63-307">Return Value - dataRelationPath</span></span>

## <a name="method-datasource"></a><span data-ttu-id="fcc63-308">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="fcc63-308">Method dataSource</span></span>

<span data-ttu-id="fcc63-309">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-309">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="fcc63-310">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="fcc63-310">Parameters - dataSource</span></span>

<span data-ttu-id="fcc63-311">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-311">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="fcc63-312">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="fcc63-312">Return Value - dataSource</span></span>

<span data-ttu-id="fcc63-313">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="fcc63-313">The identifier of the data source that will be used.</span></span>

## <a name="method-displaytarget"></a><span data-ttu-id="fcc63-314">メソッド displayTarget</span><span class="sxs-lookup"><span data-stu-id="fcc63-314">Method displayTarget</span></span>

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a><span data-ttu-id="fcc63-315">パラメーター - displayTarget</span><span class="sxs-lookup"><span data-stu-id="fcc63-315">Parameters - displayTarget</span></span>

<span data-ttu-id="fcc63-316">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-316">value</span></span>  

### <a name="return-value---displaytarget"></a><span data-ttu-id="fcc63-317">戻り値 - displayTarget</span><span class="sxs-lookup"><span data-stu-id="fcc63-317">Return Value - displayTarget</span></span>

## <a name="method-dragdrop"></a><span data-ttu-id="fcc63-318">メソッド dragDrop</span><span class="sxs-lookup"><span data-stu-id="fcc63-318">Method dragDrop</span></span>

<span data-ttu-id="fcc63-319">コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-319">Determines whether to enable or disable drag-and-drop operations for the control.</span></span>

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a><span data-ttu-id="fcc63-320">パラメーター - dragDrop</span><span class="sxs-lookup"><span data-stu-id="fcc63-320">Parameters - dragDrop</span></span>

<span data-ttu-id="fcc63-321">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-321">value</span></span>  

### <a name="return-value---dragdrop"></a><span data-ttu-id="fcc63-322">戻り値 - dragDrop</span><span class="sxs-lookup"><span data-stu-id="fcc63-322">Return Value - dragDrop</span></span>

<span data-ttu-id="fcc63-323">ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。</span><span class="sxs-lookup"><span data-stu-id="fcc63-323">1 if drag-and-drop operations are enabled; otherwise, false.</span></span>

## <a name="method-enabled"></a><span data-ttu-id="fcc63-324">メソッド enabled</span><span class="sxs-lookup"><span data-stu-id="fcc63-324">Method enabled</span></span>

<span data-ttu-id="fcc63-325">オブジェクトを有効または無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-325">Determines whether to enable or disable the object.</span></span>

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a><span data-ttu-id="fcc63-326">パラメーター - enabled</span><span class="sxs-lookup"><span data-stu-id="fcc63-326">Parameters - enabled</span></span>

<span data-ttu-id="fcc63-327">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-327">value</span></span>  

### <a name="return-value---enabled"></a><span data-ttu-id="fcc63-328">戻り値 - enabled</span><span class="sxs-lookup"><span data-stu-id="fcc63-328">Return Value - enabled</span></span>

<span data-ttu-id="fcc63-329">オブジェクトが有効である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="fcc63-329">true if the object is enabled; otherwise, false.</span></span>

### <a name="remarks---enabled"></a><span data-ttu-id="fcc63-330">備考 - enabled</span><span class="sxs-lookup"><span data-stu-id="fcc63-330">Remarks - enabled</span></span>

<span data-ttu-id="fcc63-331">有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="fcc63-331">The enabled property allows for controls to be enabled or disabled at run time.</span></span> <span data-ttu-id="fcc63-332">たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="fcc63-332">For example, you can disable objects that do not apply to the current state of the application.</span></span> <span data-ttu-id="fcc63-333">また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="fcc63-333">You can also disable a control that is used only for display purposes, such as an error message, which provides read-only information.</span></span>

## <a name="method-height"></a><span data-ttu-id="fcc63-334">メソッド height</span><span class="sxs-lookup"><span data-stu-id="fcc63-334">Method height</span></span>

<span data-ttu-id="fcc63-335">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-335">Gets or sets the height of the control.</span></span>

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a><span data-ttu-id="fcc63-336">パラメーター - height</span><span class="sxs-lookup"><span data-stu-id="fcc63-336">Parameters - height</span></span>

<span data-ttu-id="fcc63-337">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-337">value</span></span>  

<!-- -->

<span data-ttu-id="fcc63-338">モード</span><span class="sxs-lookup"><span data-stu-id="fcc63-338">mode</span></span>  

### <a name="return-value---height"></a><span data-ttu-id="fcc63-339">戻り値 - height</span><span class="sxs-lookup"><span data-stu-id="fcc63-339">Return Value - height</span></span>

<span data-ttu-id="fcc63-340">ピクセル単位のコントロールの高さ。</span><span class="sxs-lookup"><span data-stu-id="fcc63-340">The height of the control in pixels.</span></span>

### <a name="remarks---height"></a><span data-ttu-id="fcc63-341">備考 - height</span><span class="sxs-lookup"><span data-stu-id="fcc63-341">Remarks - height</span></span>

<span data-ttu-id="fcc63-342">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="fcc63-342">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="fcc63-343">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="fcc63-343">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="fcc63-344">モード。</span><span class="sxs-lookup"><span data-stu-id="fcc63-344">Mode.</span></span>            | <span data-ttu-id="fcc63-345">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="fcc63-345">Height calculation.</span></span>                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcc63-346">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="fcc63-346">-1 Exact.</span></span>        | <span data-ttu-id="fcc63-347">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="fcc63-347">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="fcc63-348">0 自動。</span><span class="sxs-lookup"><span data-stu-id="fcc63-348">0 Auto.</span></span>          | <span data-ttu-id="fcc63-349">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="fcc63-349">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="fcc63-350">1 列の高さ。</span><span class="sxs-lookup"><span data-stu-id="fcc63-350">1 Column height.</span></span> | <span data-ttu-id="fcc63-351">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="fcc63-351">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="fcc63-352">高さと高さ計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="fcc63-352">The height and height calculation mode can be set separately.</span></span>

## <a name="method-heightmode"></a><span data-ttu-id="fcc63-353">メソッド heightMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-353">Method heightMode</span></span>

<span data-ttu-id="fcc63-354">コントロールの高さの計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-354">Gets or sets a calculation mode for the height of the control.</span></span>

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a><span data-ttu-id="fcc63-355">パラメーター - heightMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-355">Parameters - heightMode</span></span>

<span data-ttu-id="fcc63-356">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-356">value</span></span>  

### <a name="return-value---heightmode"></a><span data-ttu-id="fcc63-357">戻り値 - heightMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-357">Return Value - heightMode</span></span>

<span data-ttu-id="fcc63-358">計算モード。</span><span class="sxs-lookup"><span data-stu-id="fcc63-358">The calculation mode.</span></span>

### <a name="remarks---heightmode"></a><span data-ttu-id="fcc63-359">備考 - heightMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-359">Remarks - heightMode</span></span>

<span data-ttu-id="fcc63-360">次の表に従って高さを計算します:</span><span class="sxs-lookup"><span data-stu-id="fcc63-360">Calculate the height according to the following table:</span></span>

| <span data-ttu-id="fcc63-361">モード。</span><span class="sxs-lookup"><span data-stu-id="fcc63-361">Mode.</span></span>          | <span data-ttu-id="fcc63-362">高さの計算。</span><span class="sxs-lookup"><span data-stu-id="fcc63-362">Height Calculation.</span></span>                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcc63-363">正確。</span><span class="sxs-lookup"><span data-stu-id="fcc63-363">Exact.</span></span>         | <span data-ttu-id="fcc63-364">コントロールのピクセル単位の正確な高さが使用されます。</span><span class="sxs-lookup"><span data-stu-id="fcc63-364">The exact height in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="fcc63-365">自動。</span><span class="sxs-lookup"><span data-stu-id="fcc63-365">Auto.</span></span>          | <span data-ttu-id="fcc63-366">コントロールの高さは自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="fcc63-366">The height of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="fcc63-367">列の高さ</span><span class="sxs-lookup"><span data-stu-id="fcc63-367">Column height.</span></span> | <span data-ttu-id="fcc63-368">フォームのレイアウトによって、コントロールの高さが決まります。</span><span class="sxs-lookup"><span data-stu-id="fcc63-368">The layout of the form determines the height of the control.</span></span>                              |

<span data-ttu-id="fcc63-369">計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="fcc63-369">The height of the control might change when the mode is set to auto or column height.</span></span>

## <a name="method-heightvalue"></a><span data-ttu-id="fcc63-370">メソッド heightValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-370">Method heightValue</span></span>

<span data-ttu-id="fcc63-371">コントロールの高さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-371">Gets or sets the height of the control.</span></span>

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a><span data-ttu-id="fcc63-372">パラメーター - heightValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-372">Parameters - heightValue</span></span>

<span data-ttu-id="fcc63-373">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-373">value</span></span>  

### <a name="return-value---heightvalue"></a><span data-ttu-id="fcc63-374">戻り値 - heightValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-374">Return Value - heightValue</span></span>

<span data-ttu-id="fcc63-375">ピクセル単位の高さ。</span><span class="sxs-lookup"><span data-stu-id="fcc63-375">The height in pixels.</span></span>

### <a name="remarks---heightvalue"></a><span data-ttu-id="fcc63-376">備考 - heightValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-376">Remarks - heightValue</span></span>

<span data-ttu-id="fcc63-377">正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。</span><span class="sxs-lookup"><span data-stu-id="fcc63-377">The height of the control is not changed unless the exact height calculation mode is used.</span></span>

## <a name="method-helptext"></a><span data-ttu-id="fcc63-378">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="fcc63-378">Method helpText</span></span>

<span data-ttu-id="fcc63-379">フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-379">Gets or sets the help text to display at the bottom of the screen when a field or control is pointed to.</span></span>

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a><span data-ttu-id="fcc63-380">パラメーター - helpText</span><span class="sxs-lookup"><span data-stu-id="fcc63-380">Parameters - helpText</span></span>

<span data-ttu-id="fcc63-381">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-381">value</span></span>  

### <a name="return-value---helptext"></a><span data-ttu-id="fcc63-382">戻り値 - helpText</span><span class="sxs-lookup"><span data-stu-id="fcc63-382">Return Value - helpText</span></span>

<span data-ttu-id="fcc63-383">画面の下部に表示される文字列。</span><span class="sxs-lookup"><span data-stu-id="fcc63-383">The string to be displayed at the bottom of the screen.</span></span>

### <a name="remarks---helptext"></a><span data-ttu-id="fcc63-384">備考 - helpText</span><span class="sxs-lookup"><span data-stu-id="fcc63-384">Remarks - helpText</span></span>

<span data-ttu-id="fcc63-385">プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-385">Set the HelpText property for an object by using the property dialog box.</span></span> <span data-ttu-id="fcc63-386">ヘルプ テキストは 250 文字を超えてはいけません。</span><span class="sxs-lookup"><span data-stu-id="fcc63-386">The help text must not exceed 250 characters.</span></span>

## <a name="method-hideifempty"></a><span data-ttu-id="fcc63-387">メソッド hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="fcc63-387">Method hideIfEmpty</span></span>

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a><span data-ttu-id="fcc63-388">パラメーター - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="fcc63-388">Parameters - hideIfEmpty</span></span>

<span data-ttu-id="fcc63-389">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-389">value</span></span>  

### <a name="return-value---hideifempty"></a><span data-ttu-id="fcc63-390">戻り値 - hideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="fcc63-390">Return Value - hideIfEmpty</span></span>

## <a name="method-hierarchyparent"></a><span data-ttu-id="fcc63-391">メソッド hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="fcc63-391">Method hierarchyParent</span></span>

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a><span data-ttu-id="fcc63-392">パラメーター - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="fcc63-392">Parameters - hierarchyParent</span></span>

<span data-ttu-id="fcc63-393">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-393">value</span></span>  

### <a name="return-value---hierarchyparent"></a><span data-ttu-id="fcc63-394">戻り値 - hierarchyParent</span><span class="sxs-lookup"><span data-stu-id="fcc63-394">Return Value - hierarchyParent</span></span>

## <a name="method-id"></a><span data-ttu-id="fcc63-395">メソッド id</span><span class="sxs-lookup"><span data-stu-id="fcc63-395">Method id</span></span>

<span data-ttu-id="fcc63-396">コントロールの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-396">Retrieves the ID of the control.</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="fcc63-397">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="fcc63-397">Return Value - id</span></span>

<span data-ttu-id="fcc63-398">コントロールの ID。</span><span class="sxs-lookup"><span data-stu-id="fcc63-398">The ID of the control.</span></span>

## <a name="method-iscontainer"></a><span data-ttu-id="fcc63-399">メソッド isContainer</span><span class="sxs-lookup"><span data-stu-id="fcc63-399">Method isContainer</span></span>

<span data-ttu-id="fcc63-400">コントロールがコンテナー コントロールかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-400">Retrieves a value that indicates whether the control is a container control.</span></span>

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a><span data-ttu-id="fcc63-401">戻り値 - isContainer</span><span class="sxs-lookup"><span data-stu-id="fcc63-401">Return Value - isContainer</span></span>

<span data-ttu-id="fcc63-402">コントロールがコンテナー コントロールかどうかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="fcc63-402">A Boolean value that indicates whether the control is a container control.</span></span>

## <a name="method-left"></a><span data-ttu-id="fcc63-403">メソッド left</span><span class="sxs-lookup"><span data-stu-id="fcc63-403">Method left</span></span>

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a><span data-ttu-id="fcc63-404">パラメーター - left</span><span class="sxs-lookup"><span data-stu-id="fcc63-404">Parameters - left</span></span>

<span data-ttu-id="fcc63-405">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-405">value</span></span>  

<!-- -->

<span data-ttu-id="fcc63-406">モード</span><span class="sxs-lookup"><span data-stu-id="fcc63-406">mode</span></span>  

### <a name="return-value---left"></a><span data-ttu-id="fcc63-407">戻り値 - left</span><span class="sxs-lookup"><span data-stu-id="fcc63-407">Return Value - left</span></span>

## <a name="method-leftmargin"></a><span data-ttu-id="fcc63-408">メソッド leftMargin</span><span class="sxs-lookup"><span data-stu-id="fcc63-408">Method leftMargin</span></span>

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a><span data-ttu-id="fcc63-409">パラメーター - leftMargin</span><span class="sxs-lookup"><span data-stu-id="fcc63-409">Parameters - leftMargin</span></span>

<span data-ttu-id="fcc63-410">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-410">value</span></span>  

<!-- -->

<span data-ttu-id="fcc63-411">モード</span><span class="sxs-lookup"><span data-stu-id="fcc63-411">mode</span></span>  

### <a name="return-value---leftmargin"></a><span data-ttu-id="fcc63-412">戻り値 - leftMargin</span><span class="sxs-lookup"><span data-stu-id="fcc63-412">Return Value - leftMargin</span></span>

## <a name="method-leftmarginmode"></a><span data-ttu-id="fcc63-413">メソッド leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-413">Method leftMarginMode</span></span>

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a><span data-ttu-id="fcc63-414">パラメーター - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-414">Parameters - leftMarginMode</span></span>

<span data-ttu-id="fcc63-415">モード</span><span class="sxs-lookup"><span data-stu-id="fcc63-415">mode</span></span>  

### <a name="return-value---leftmarginmode"></a><span data-ttu-id="fcc63-416">戻り値 - leftMarginMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-416">Return Value - leftMarginMode</span></span>

## <a name="method-leftmarginvalue"></a><span data-ttu-id="fcc63-417">メソッド leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-417">Method leftMarginValue</span></span>

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a><span data-ttu-id="fcc63-418">パラメーター - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-418">Parameters - leftMarginValue</span></span>

<span data-ttu-id="fcc63-419">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-419">value</span></span>  

### <a name="return-value---leftmarginvalue"></a><span data-ttu-id="fcc63-420">戻り値 - leftMarginValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-420">Return Value - leftMarginValue</span></span>

## <a name="method-leftmode"></a><span data-ttu-id="fcc63-421">メソッド leftMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-421">Method leftMode</span></span>

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a><span data-ttu-id="fcc63-422">パラメーター - leftMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-422">Parameters - leftMode</span></span>

<span data-ttu-id="fcc63-423">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-423">value</span></span>  

### <a name="return-value---leftmode"></a><span data-ttu-id="fcc63-424">戻り値 - leftMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-424">Return Value - leftMode</span></span>

## <a name="method-leftvalue"></a><span data-ttu-id="fcc63-425">メソッド leftValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-425">Method leftValue</span></span>

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a><span data-ttu-id="fcc63-426">パラメーター - leftValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-426">Parameters - leftValue</span></span>

<span data-ttu-id="fcc63-427">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-427">value</span></span>  

### <a name="return-value---leftvalue"></a><span data-ttu-id="fcc63-428">戻り値 - leftValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-428">Return Value - leftValue</span></span>

## <a name="method-movecontrol"></a><span data-ttu-id="fcc63-429">メソッド moveControl</span><span class="sxs-lookup"><span data-stu-id="fcc63-429">Method moveControl</span></span>

<span data-ttu-id="fcc63-430">コントロールに ID で指定されているコントロールを移動します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-430">Moves a control that is specified by ID to the control.</span></span>

```xpp
public int moveControl(int controlId, [int insertAfterControlId])
```

### <a name="parameters---movecontrol"></a><span data-ttu-id="fcc63-431">パラメーター - moveControl</span><span class="sxs-lookup"><span data-stu-id="fcc63-431">Parameters - moveControl</span></span>

<span data-ttu-id="fcc63-432">controlId</span><span class="sxs-lookup"><span data-stu-id="fcc63-432">controlId</span></span>  

<!-- -->

<span data-ttu-id="fcc63-433">insertAfterControlId</span><span class="sxs-lookup"><span data-stu-id="fcc63-433">insertAfterControlId</span></span>  

### <a name="return-value---movecontrol"></a><span data-ttu-id="fcc63-434">戻り値 - moveControl</span><span class="sxs-lookup"><span data-stu-id="fcc63-434">Return Value - moveControl</span></span>

<span data-ttu-id="fcc63-435">コントロールが正常に移動した場合は 1、それ以外の場合、0 です。</span><span class="sxs-lookup"><span data-stu-id="fcc63-435">1 if the control was moved successfully; otherwise, 0.</span></span>

### <a name="remarks---movecontrol"></a><span data-ttu-id="fcc63-436">備考 - moveControl</span><span class="sxs-lookup"><span data-stu-id="fcc63-436">Remarks - moveControl</span></span>

<span data-ttu-id="fcc63-437">一般に、指定したコントロールをコントロールに含めることができ、現在のコンテナーから移動できる場合、このメソッドは成功します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-437">In general, if the specified control can be contained in the control and can be moved from the container that it is currently in, this method should succeed.</span></span> <span data-ttu-id="fcc63-438">ただし、場合によっては、参照グループ コントロールのインスタンス コントロールなど、コントロールを移動できません。</span><span class="sxs-lookup"><span data-stu-id="fcc63-438">However, in some cases, such as for the reference group control instance, controls cannot be moved.</span></span>

## <a name="method-name"></a><span data-ttu-id="fcc63-439">メソッド名</span><span class="sxs-lookup"><span data-stu-id="fcc63-439">Method name</span></span>

<span data-ttu-id="fcc63-440">フォーム、レポート、テーブル、クエリ、または別のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-440">Gets or sets the name that is used in the code to identify a form, report, table, query, or another application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="fcc63-441">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="fcc63-441">Parameters - name</span></span>

<span data-ttu-id="fcc63-442">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-442">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="fcc63-443">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="fcc63-443">Return Value - name</span></span>

<span data-ttu-id="fcc63-444">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="fcc63-444">The name that is used in the code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="fcc63-445">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="fcc63-445">Remarks - name</span></span>

<span data-ttu-id="fcc63-446">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="fcc63-446">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="fcc63-447">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="fcc63-447">Begins with a letter.</span></span>
-   <span data-ttu-id="fcc63-448">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="fcc63-448">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="fcc63-449">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="fcc63-449">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="fcc63-450">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="fcc63-450">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="fcc63-451">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="fcc63-451">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-neededpermission"></a><span data-ttu-id="fcc63-452">メソッド neededPermission</span><span class="sxs-lookup"><span data-stu-id="fcc63-452">Method neededPermission</span></span>

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a><span data-ttu-id="fcc63-453">パラメーター - neededPermission</span><span class="sxs-lookup"><span data-stu-id="fcc63-453">Parameters - neededPermission</span></span>

<span data-ttu-id="fcc63-454">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-454">value</span></span>  

### <a name="return-value---neededpermission"></a><span data-ttu-id="fcc63-455">戻り値 - neededPermission</span><span class="sxs-lookup"><span data-stu-id="fcc63-455">Return Value - neededPermission</span></span>

## <a name="method-position"></a><span data-ttu-id="fcc63-456">メソッドの位置</span><span class="sxs-lookup"><span data-stu-id="fcc63-456">Method position</span></span>

```xpp
public int position([int value])
```

### <a name="parameters---position"></a><span data-ttu-id="fcc63-457">パラメーター - 位置</span><span class="sxs-lookup"><span data-stu-id="fcc63-457">Parameters - position</span></span>

<span data-ttu-id="fcc63-458">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-458">value</span></span>  

### <a name="return-value---position"></a><span data-ttu-id="fcc63-459">戻り値 - position</span><span class="sxs-lookup"><span data-stu-id="fcc63-459">Return Value - position</span></span>

## <a name="method-rightmargin"></a><span data-ttu-id="fcc63-460">メソッド rightMargin</span><span class="sxs-lookup"><span data-stu-id="fcc63-460">Method rightMargin</span></span>

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a><span data-ttu-id="fcc63-461">パラメーター - rightMargin</span><span class="sxs-lookup"><span data-stu-id="fcc63-461">Parameters - rightMargin</span></span>

<span data-ttu-id="fcc63-462">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-462">value</span></span>  

<!-- -->

<span data-ttu-id="fcc63-463">モード</span><span class="sxs-lookup"><span data-stu-id="fcc63-463">mode</span></span>  

### <a name="return-value---rightmargin"></a><span data-ttu-id="fcc63-464">戻り値 - rightMargin</span><span class="sxs-lookup"><span data-stu-id="fcc63-464">Return Value - rightMargin</span></span>

## <a name="method-rightmarginmode"></a><span data-ttu-id="fcc63-465">メソッド rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-465">Method rightMarginMode</span></span>

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a><span data-ttu-id="fcc63-466">パラメーター - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-466">Parameters - rightMarginMode</span></span>

<span data-ttu-id="fcc63-467">モード</span><span class="sxs-lookup"><span data-stu-id="fcc63-467">mode</span></span>  

### <a name="return-value---rightmarginmode"></a><span data-ttu-id="fcc63-468">戻り値 - rightMarginMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-468">Return Value - rightMarginMode</span></span>

## <a name="method-rightmarginvalue"></a><span data-ttu-id="fcc63-469">メソッド rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-469">Method rightMarginValue</span></span>

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a><span data-ttu-id="fcc63-470">パラメーター - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-470">Parameters - rightMarginValue</span></span>

<span data-ttu-id="fcc63-471">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-471">value</span></span>  

### <a name="return-value---rightmarginvalue"></a><span data-ttu-id="fcc63-472">戻り値 - rightMarginValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-472">Return Value - rightMarginValue</span></span>

## <a name="method-securitykey"></a><span data-ttu-id="fcc63-473">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="fcc63-473">Method securityKey</span></span>

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a><span data-ttu-id="fcc63-474">パラメーター - securityKey</span><span class="sxs-lookup"><span data-stu-id="fcc63-474">Parameters - securityKey</span></span>

<span data-ttu-id="fcc63-475">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-475">value</span></span>  

### <a name="return-value---securitykey"></a><span data-ttu-id="fcc63-476">戻り値 - securityKey</span><span class="sxs-lookup"><span data-stu-id="fcc63-476">Return Value - securityKey</span></span>

## <a name="method-skip"></a><span data-ttu-id="fcc63-477">メソッド skip</span><span class="sxs-lookup"><span data-stu-id="fcc63-477">Method skip</span></span>

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a><span data-ttu-id="fcc63-478">パラメーター - skip</span><span class="sxs-lookup"><span data-stu-id="fcc63-478">Parameters - skip</span></span>

<span data-ttu-id="fcc63-479">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-479">value</span></span>  

### <a name="return-value---skip"></a><span data-ttu-id="fcc63-480">戻り値 - skip</span><span class="sxs-lookup"><span data-stu-id="fcc63-480">Return Value - skip</span></span>

## <a name="method-style"></a><span data-ttu-id="fcc63-481">メソッド style</span><span class="sxs-lookup"><span data-stu-id="fcc63-481">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="fcc63-482">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="fcc63-482">Parameters - style</span></span>

<span data-ttu-id="fcc63-483">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-483">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="fcc63-484">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="fcc63-484">Return Value - style</span></span>

## <a name="method-top"></a><span data-ttu-id="fcc63-485">メソッド top</span><span class="sxs-lookup"><span data-stu-id="fcc63-485">Method top</span></span>

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a><span data-ttu-id="fcc63-486">パラメーター - top</span><span class="sxs-lookup"><span data-stu-id="fcc63-486">Parameters - top</span></span>

<span data-ttu-id="fcc63-487">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-487">value</span></span>  

<!-- -->

<span data-ttu-id="fcc63-488">モード</span><span class="sxs-lookup"><span data-stu-id="fcc63-488">mode</span></span>  

### <a name="return-value---top"></a><span data-ttu-id="fcc63-489">戻り値 - top</span><span class="sxs-lookup"><span data-stu-id="fcc63-489">Return Value - top</span></span>

## <a name="method-topmargin"></a><span data-ttu-id="fcc63-490">メソッド topMargin</span><span class="sxs-lookup"><span data-stu-id="fcc63-490">Method topMargin</span></span>

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a><span data-ttu-id="fcc63-491">パラメーター - topMargin</span><span class="sxs-lookup"><span data-stu-id="fcc63-491">Parameters - topMargin</span></span>

<span data-ttu-id="fcc63-492">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-492">value</span></span>  

<!-- -->

<span data-ttu-id="fcc63-493">モード</span><span class="sxs-lookup"><span data-stu-id="fcc63-493">mode</span></span>  

### <a name="return-value---topmargin"></a><span data-ttu-id="fcc63-494">戻り値 - topMargin</span><span class="sxs-lookup"><span data-stu-id="fcc63-494">Return Value - topMargin</span></span>

## <a name="method-topmarginmode"></a><span data-ttu-id="fcc63-495">メソッド topMarginMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-495">Method topMarginMode</span></span>

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a><span data-ttu-id="fcc63-496">パラメーター - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-496">Parameters - topMarginMode</span></span>

<span data-ttu-id="fcc63-497">モード</span><span class="sxs-lookup"><span data-stu-id="fcc63-497">mode</span></span>  

### <a name="return-value---topmarginmode"></a><span data-ttu-id="fcc63-498">戻り値 - topMarginMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-498">Return Value - topMarginMode</span></span>

## <a name="method-topmarginvalue"></a><span data-ttu-id="fcc63-499">メソッド topMarginValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-499">Method topMarginValue</span></span>

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a><span data-ttu-id="fcc63-500">パラメーター - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-500">Parameters - topMarginValue</span></span>

<span data-ttu-id="fcc63-501">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-501">value</span></span>  

### <a name="return-value---topmarginvalue"></a><span data-ttu-id="fcc63-502">戻り値 - topMarginValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-502">Return Value - topMarginValue</span></span>

## <a name="method-topmode"></a><span data-ttu-id="fcc63-503">メソッド topMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-503">Method topMode</span></span>

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a><span data-ttu-id="fcc63-504">パラメーター - topMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-504">Parameters - topMode</span></span>

<span data-ttu-id="fcc63-505">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-505">value</span></span>  

### <a name="return-value---topmode"></a><span data-ttu-id="fcc63-506">戻り値 - topMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-506">Return Value - topMode</span></span>

## <a name="method-topvalue"></a><span data-ttu-id="fcc63-507">メソッド topValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-507">Method topValue</span></span>

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a><span data-ttu-id="fcc63-508">パラメーター - topValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-508">Parameters - topValue</span></span>

<span data-ttu-id="fcc63-509">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-509">value</span></span>  

### <a name="return-value---topvalue"></a><span data-ttu-id="fcc63-510">戻り値 - topValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-510">Return Value - topValue</span></span>

## <a name="method-type"></a><span data-ttu-id="fcc63-511">メソッドのタイプ</span><span class="sxs-lookup"><span data-stu-id="fcc63-511">Method type</span></span>

```xpp
public int type([int value])
```

### <a name="parameters---type"></a><span data-ttu-id="fcc63-512">パラメーター - タイプ</span><span class="sxs-lookup"><span data-stu-id="fcc63-512">Parameters - type</span></span>

<span data-ttu-id="fcc63-513">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-513">value</span></span>  

### <a name="return-value---type"></a><span data-ttu-id="fcc63-514">戻り値 - type</span><span class="sxs-lookup"><span data-stu-id="fcc63-514">Return Value - type</span></span>

## <a name="method-userdata"></a><span data-ttu-id="fcc63-515">メソッド userData</span><span class="sxs-lookup"><span data-stu-id="fcc63-515">Method userData</span></span>

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a><span data-ttu-id="fcc63-516">パラメーター - userData</span><span class="sxs-lookup"><span data-stu-id="fcc63-516">Parameters - userData</span></span>

<span data-ttu-id="fcc63-517">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-517">value</span></span>  

### <a name="return-value---userdata"></a><span data-ttu-id="fcc63-518">戻り値 - userData</span><span class="sxs-lookup"><span data-stu-id="fcc63-518">Return Value - userData</span></span>

## <a name="method-userdataitem"></a><span data-ttu-id="fcc63-519">メソッド userDataItem</span><span class="sxs-lookup"><span data-stu-id="fcc63-519">Method userDataItem</span></span>

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a><span data-ttu-id="fcc63-520">パラメーター - userDataItem</span><span class="sxs-lookup"><span data-stu-id="fcc63-520">Parameters - userDataItem</span></span>

<span data-ttu-id="fcc63-521">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-521">value</span></span>  

### <a name="return-value---userdataitem"></a><span data-ttu-id="fcc63-522">戻り値 - userDataItem</span><span class="sxs-lookup"><span data-stu-id="fcc63-522">Return Value - userDataItem</span></span>

## <a name="method-userdataitems"></a><span data-ttu-id="fcc63-523">メソッド userDataItems</span><span class="sxs-lookup"><span data-stu-id="fcc63-523">Method userDataItems</span></span>

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a><span data-ttu-id="fcc63-524">パラメーター - userDataItems</span><span class="sxs-lookup"><span data-stu-id="fcc63-524">Parameters - userDataItems</span></span>

<span data-ttu-id="fcc63-525">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-525">value</span></span>  

### <a name="return-value---userdataitems"></a><span data-ttu-id="fcc63-526">戻り値 - userDataItems</span><span class="sxs-lookup"><span data-stu-id="fcc63-526">Return Value - userDataItems</span></span>

## <a name="method-useuserlayout"></a><span data-ttu-id="fcc63-527">メソッド useUserLayout</span><span class="sxs-lookup"><span data-stu-id="fcc63-527">Method useUserLayout</span></span>

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a><span data-ttu-id="fcc63-528">パラメーター - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="fcc63-528">Parameters - useUserLayout</span></span>

<span data-ttu-id="fcc63-529">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-529">value</span></span>  

### <a name="return-value---useuserlayout"></a><span data-ttu-id="fcc63-530">戻り値 - useUserLayout</span><span class="sxs-lookup"><span data-stu-id="fcc63-530">Return Value - useUserLayout</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="fcc63-531">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="fcc63-531">Method verticalSpacing</span></span>

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="fcc63-532">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="fcc63-532">Parameters - verticalSpacing</span></span>

<span data-ttu-id="fcc63-533">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-533">value</span></span>  

<!-- -->

<span data-ttu-id="fcc63-534">モード</span><span class="sxs-lookup"><span data-stu-id="fcc63-534">mode</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="fcc63-535">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="fcc63-535">Return Value - verticalSpacing</span></span>

## <a name="method-verticalspacingmode"></a><span data-ttu-id="fcc63-536">メソッド verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-536">Method verticalSpacingMode</span></span>

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a><span data-ttu-id="fcc63-537">パラメーター - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-537">Parameters - verticalSpacingMode</span></span>

<span data-ttu-id="fcc63-538">モード</span><span class="sxs-lookup"><span data-stu-id="fcc63-538">mode</span></span>  

### <a name="return-value---verticalspacingmode"></a><span data-ttu-id="fcc63-539">戻り値 - verticalSpacingMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-539">Return Value - verticalSpacingMode</span></span>

## <a name="method-verticalspacingvalue"></a><span data-ttu-id="fcc63-540">メソッド verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-540">Method verticalSpacingValue</span></span>

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a><span data-ttu-id="fcc63-541">パラメーター - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-541">Parameters - verticalSpacingValue</span></span>

<span data-ttu-id="fcc63-542">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-542">value</span></span>  

### <a name="return-value---verticalspacingvalue"></a><span data-ttu-id="fcc63-543">戻り値 - verticalSpacingValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-543">Return Value - verticalSpacingValue</span></span>

## <a name="method-visible"></a><span data-ttu-id="fcc63-544">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="fcc63-544">Method visible</span></span>

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a><span data-ttu-id="fcc63-545">パラメーター - visible</span><span class="sxs-lookup"><span data-stu-id="fcc63-545">Parameters - visible</span></span>

<span data-ttu-id="fcc63-546">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-546">value</span></span>  

### <a name="return-value---visible"></a><span data-ttu-id="fcc63-547">戻り値 - visible</span><span class="sxs-lookup"><span data-stu-id="fcc63-547">Return Value - visible</span></span>

## <a name="method-width"></a><span data-ttu-id="fcc63-548">メソッド width</span><span class="sxs-lookup"><span data-stu-id="fcc63-548">Method width</span></span>

<span data-ttu-id="fcc63-549">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-549">Gets or sets the width of the control.</span></span>

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a><span data-ttu-id="fcc63-550">パラメーター - width</span><span class="sxs-lookup"><span data-stu-id="fcc63-550">Parameters - width</span></span>

<span data-ttu-id="fcc63-551">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-551">value</span></span>  

<!-- -->

<span data-ttu-id="fcc63-552">モード</span><span class="sxs-lookup"><span data-stu-id="fcc63-552">mode</span></span>  

### <a name="return-value---width"></a><span data-ttu-id="fcc63-553">戻り値 - width</span><span class="sxs-lookup"><span data-stu-id="fcc63-553">Return Value - width</span></span>

<span data-ttu-id="fcc63-554">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="fcc63-554">The width of the control in pixels.</span></span>

### <a name="remarks---width"></a><span data-ttu-id="fcc63-555">備考 - width</span><span class="sxs-lookup"><span data-stu-id="fcc63-555">Remarks - width</span></span>

<span data-ttu-id="fcc63-556">値のパラメータを省略すると、正確なモードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="fcc63-556">Exact mode is used if the value parameter is omitted.</span></span> <span data-ttu-id="fcc63-557">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="fcc63-557">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="fcc63-558">モード。</span><span class="sxs-lookup"><span data-stu-id="fcc63-558">Mode.</span></span>           | <span data-ttu-id="fcc63-559">幅計算。</span><span class="sxs-lookup"><span data-stu-id="fcc63-559">Width calculation.</span></span>                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcc63-560">-1 正確。</span><span class="sxs-lookup"><span data-stu-id="fcc63-560">-1 Exact.</span></span>       | <span data-ttu-id="fcc63-561">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="fcc63-561">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="fcc63-562">0 自動。</span><span class="sxs-lookup"><span data-stu-id="fcc63-562">0 Auto.</span></span>         | <span data-ttu-id="fcc63-563">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="fcc63-563">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="fcc63-564">1 列の幅。</span><span class="sxs-lookup"><span data-stu-id="fcc63-564">1 Column width.</span></span> | <span data-ttu-id="fcc63-565">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="fcc63-565">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="fcc63-566">幅と幅計算モードは別々に設定できます。</span><span class="sxs-lookup"><span data-stu-id="fcc63-566">The width and width calculation mode can be set separately.</span></span>

## <a name="method-widthmode"></a><span data-ttu-id="fcc63-567">メソッド widthMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-567">Method widthMode</span></span>

<span data-ttu-id="fcc63-568">コントロールの幅の計算方法を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-568">Gets or sets the calculation mode of the width of the control.</span></span>

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a><span data-ttu-id="fcc63-569">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-569">Parameters - widthMode</span></span>

<span data-ttu-id="fcc63-570">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-570">value</span></span>  

### <a name="return-value---widthmode"></a><span data-ttu-id="fcc63-571">戻り値 - widthMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-571">Return Value - widthMode</span></span>

<span data-ttu-id="fcc63-572">現在の計算モードを示す整数値。</span><span class="sxs-lookup"><span data-stu-id="fcc63-572">An integer value that indicates the current calculation mode.</span></span>

### <a name="remarks---widthmode"></a><span data-ttu-id="fcc63-573">備考 - widthMode</span><span class="sxs-lookup"><span data-stu-id="fcc63-573">Remarks - widthMode</span></span>

<span data-ttu-id="fcc63-574">次の表に従って幅を計算します:</span><span class="sxs-lookup"><span data-stu-id="fcc63-574">Calculate the width according to the following table:</span></span>

| <span data-ttu-id="fcc63-575">モード。</span><span class="sxs-lookup"><span data-stu-id="fcc63-575">Mode.</span></span>         | <span data-ttu-id="fcc63-576">幅計算。</span><span class="sxs-lookup"><span data-stu-id="fcc63-576">Width Calculation.</span></span>                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcc63-577">正確。</span><span class="sxs-lookup"><span data-stu-id="fcc63-577">Exact.</span></span>        | <span data-ttu-id="fcc63-578">コントロールのピクセル単位の正確な幅が使用されます。</span><span class="sxs-lookup"><span data-stu-id="fcc63-578">The exact width in pixels of the controls is used.</span></span>                                       |
| <span data-ttu-id="fcc63-579">自動。</span><span class="sxs-lookup"><span data-stu-id="fcc63-579">Auto.</span></span>         | <span data-ttu-id="fcc63-580">コントロールの幅は自動的に計算され、value パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="fcc63-580">The width of the control is calculated automatically and the value parameter is ignored.</span></span> |
| <span data-ttu-id="fcc63-581">列の幅。</span><span class="sxs-lookup"><span data-stu-id="fcc63-581">Column width.</span></span> | <span data-ttu-id="fcc63-582">フォームのレイアウトによって、コントロールの幅が決まります。</span><span class="sxs-lookup"><span data-stu-id="fcc63-582">The layout of the form determines the width of the control.</span></span>                              |

<span data-ttu-id="fcc63-583">モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。</span><span class="sxs-lookup"><span data-stu-id="fcc63-583">The width of the control might change when the mode is set to auto or column width.</span></span>

## <a name="method-widthvalue"></a><span data-ttu-id="fcc63-584">メソッド widthValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-584">Method widthValue</span></span>

<span data-ttu-id="fcc63-585">コントロールの幅を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-585">Gets or sets the width of the control.</span></span>

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a><span data-ttu-id="fcc63-586">パラメーター - widthValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-586">Parameters - widthValue</span></span>

<span data-ttu-id="fcc63-587">値</span><span class="sxs-lookup"><span data-stu-id="fcc63-587">value</span></span>  

### <a name="return-value---widthvalue"></a><span data-ttu-id="fcc63-588">戻り値 - widthValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-588">Return Value - widthValue</span></span>

<span data-ttu-id="fcc63-589">ピクセル単位のコントロールの幅。</span><span class="sxs-lookup"><span data-stu-id="fcc63-589">The width in pixels of the control.</span></span>

### <a name="remarks---widthvalue"></a><span data-ttu-id="fcc63-590">備考 - widthValue</span><span class="sxs-lookup"><span data-stu-id="fcc63-590">Remarks - widthValue</span></span>

<span data-ttu-id="fcc63-591">コントロールの幅を変更するには、正確な幅の計算モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="fcc63-591">To change the width of the control, use the exact width calculation mode.</span></span>

## <a name="method-registeroverridemethod"></a><span data-ttu-id="fcc63-592">メソッド registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="fcc63-592">Method registerOverrideMethod</span></span>

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a><span data-ttu-id="fcc63-593">パラメーター - registerOverrideMethod</span><span class="sxs-lookup"><span data-stu-id="fcc63-593">Parameters - registerOverrideMethod</span></span>

<span data-ttu-id="fcc63-594">methodToOverride</span><span class="sxs-lookup"><span data-stu-id="fcc63-594">methodToOverride</span></span>  

<!-- -->

<span data-ttu-id="fcc63-595">objectMethodToCall</span><span class="sxs-lookup"><span data-stu-id="fcc63-595">objectMethodToCall</span></span>  

<!-- -->

<span data-ttu-id="fcc63-596">overrideObject</span><span class="sxs-lookup"><span data-stu-id="fcc63-596">overrideObject</span></span>  

